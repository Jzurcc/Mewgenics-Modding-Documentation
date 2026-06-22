# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## NPC Scripts


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`states`](./NPC_Scripts.md#context-states) | Block | Examples: `{ ... }` | 12 |
| [`transitions`](./NPC_Scripts.md#context-transitions) | Block | Examples: `{ ... }` | 12 |
| [`unprompted`](./NPC_Scripts.md#context-unprompted) | Block | Examples: `{ ... }` | 9 |
| [`also`](./NPC_Scripts.md#context-also) | Block | Examples: `{ ... }` | 8 |
| [`unknown`](./NPC_Scripts.md#context-unknown) | Block | Examples: `{ ... }` | 8 |
| [`hide_text`](./NPC_Scripts.md#context-hide_text) | Block | Examples: `{ ... }` | 4 |
| [`purchase_item`](./NPC_Scripts.md#context-purchase_item) | Block | Examples: `{ ... }` | 4 |
| [`tooltip`](./NPC_Scripts.md#context-tooltip) | Block | Examples: `{ ... }` | 4 |
| [`unprompted_a`](./NPC_Scripts.md#context-unprompted_a) | Block | Examples: `{ ... }` | 4 |
| [`unprompted_b`](./NPC_Scripts.md#context-unprompted_b) | Block | Examples: `{ ... }` | 4 |
| [`unprompted_c`](./NPC_Scripts.md#context-unprompted_c) | Block | Examples: `{ ... }` | 4 |
| [`unprompted_d`](./NPC_Scripts.md#context-unprompted_d) | Block | Examples: `{ ... }` | 4 |
| [`unprompted_e`](./NPC_Scripts.md#context-unprompted_e) | Block | Examples: `{ ... }` | 4 |
| [`unprompted_f`](./NPC_Scripts.md#context-unprompted_f) | Block | Examples: `{ ... }` | 4 |
| [`unprompted_g`](./NPC_Scripts.md#context-unprompted_g) | Block | Examples: `{ ... }` | 4 |
| [`unprompted_h`](./NPC_Scripts.md#context-unprompted_h) | Block | Examples: `{ ... }` | 4 |
| [`unprompted_i`](./NPC_Scripts.md#context-unprompted_i) | Block | Examples: `{ ... }` | 4 |
| [`cant_afford`](./NPC_Scripts.md#context-cant_afford) | Block | Examples: `{ ... }` | 3 |
| [`forward_to_tips`](./NPC_Scripts.md#context-forward_to_tips) | Block | Examples: `{ ... }` | 3 |
| [`out_of_stock`](./NPC_Scripts.md#context-out_of_stock) | Block | Examples: `{ ... }` | 3 |
| [`Jack_Gainaltfurniture`](./NPC_Scripts.md#context-jack_gainaltfurniture) | Block | Examples: `{ ... }` | 1 |
| [`beanies_begin_accepting_cats`](./NPC_Scripts.md#context-beanies_begin_accepting_cats) | Block | Examples: `{ ... }` | 1 |
| [`beanies_bombquest_2`](./NPC_Scripts.md#context-beanies_bombquest_2) | Block | Examples: `{ ... }` | 1 |
| [`beanies_bombquest_3`](./NPC_Scripts.md#context-beanies_bombquest_3) | Block | Examples: `{ ... }` | 1 |
| [`beanies_bombquest_amnesia`](./NPC_Scripts.md#context-beanies_bombquest_amnesia) | Block | Examples: `{ ... }` | 1 |
| [`beanies_bombquest_begin`](./NPC_Scripts.md#context-beanies_bombquest_begin) | Block | Examples: `{ ... }` | 1 |
| [`beanies_bombquest_fail_jarofblood`](./NPC_Scripts.md#context-beanies_bombquest_fail_jarofblood) | Block | Examples: `{ ... }` | 1 |
| [`beanies_bombquest_fail_jarofchaos`](./NPC_Scripts.md#context-beanies_bombquest_fail_jarofchaos) | Block | Examples: `{ ... }` | 1 |
| [`beanies_bombquest_fail_jarofradiation`](./NPC_Scripts.md#context-beanies_bombquest_fail_jarofradiation) | Block | Examples: `{ ... }` | 1 |
| [`beanies_bombquest_fail_nuke`](./NPC_Scripts.md#context-beanies_bombquest_fail_nuke) | Block | Examples: `{ ... }` | 1 |
| [`beanies_future_intro`](./NPC_Scripts.md#context-beanies_future_intro) | Block | Examples: `{ ... }` | 1 |
| [`beanies_hitler3`](./NPC_Scripts.md#context-beanies_hitler3) | Block | Examples: `{ ... }` | 1 |
| [`beanies_hitler3_defeat`](./NPC_Scripts.md#context-beanies_hitler3_defeat) | Block | Examples: `{ ... }` | 1 |
| [`beanies_iloveyou`](./NPC_Scripts.md#context-beanies_iloveyou) | Block | Examples: `{ ... }` | 1 |
| [`beanies_infinite_intro`](./NPC_Scripts.md#context-beanies_infinite_intro) | Block | Examples: `{ ... }` | 1 |
| [`beanies_jurassic_intro`](./NPC_Scripts.md#context-beanies_jurassic_intro) | Block | Examples: `{ ... }` | 1 |
| [`beanies_lab_intro`](./NPC_Scripts.md#context-beanies_lab_intro) | Block | Examples: `{ ... }` | 1 |
| [`beanies_quest_complete`](./NPC_Scripts.md#context-beanies_quest_complete) | Block | Examples: `{ ... }` | 1 |
| [`beanies_quest_fail`](./NPC_Scripts.md#context-beanies_quest_fail) | Block | Examples: `{ ... }` | 1 |
| [`beanies_quests_intro`](./NPC_Scripts.md#context-beanies_quests_intro) | Block | Examples: `{ ... }` | 1 |
| [`beanies_quests_repeat`](./NPC_Scripts.md#context-beanies_quests_repeat) | Block | Examples: `{ ... }` | 1 |
| [`beanies_rift_intro`](./NPC_Scripts.md#context-beanies_rift_intro) | Block | Examples: `{ ... }` | 1 |
| [`beanies_screenshake_test`](./NPC_Scripts.md#context-beanies_screenshake_test) | Block | Examples: `{ ... }` | 1 |
| [`beanies_seefuture`](./NPC_Scripts.md#context-beanies_seefuture) | Block | Examples: `{ ... }` | 1 |
| [`beanies_seetheend`](./NPC_Scripts.md#context-beanies_seetheend) | Block | Examples: `{ ... }` | 1 |
| [`beanies_terminator1_defeat`](./NPC_Scripts.md#context-beanies_terminator1_defeat) | Block | Examples: `{ ... }` | 1 |
| [`beanies_terminator2_defeat`](./NPC_Scripts.md#context-beanies_terminator2_defeat) | Block | Examples: `{ ... }` | 1 |
| [`beanies_theend_intro`](./NPC_Scripts.md#context-beanies_theend_intro) | Block | Examples: `{ ... }` | 1 |
| [`beanies_timemachine_2`](./NPC_Scripts.md#context-beanies_timemachine_2) | Block | Examples: `{ ... }` | 1 |
| [`beanies_timemachine_intro`](./NPC_Scripts.md#context-beanies_timemachine_intro) | Block | Examples: `{ ... }` | 1 |
| [`beanies_vscreator1`](./NPC_Scripts.md#context-beanies_vscreator1) | Block | Examples: `{ ... }` | 1 |
| [`beanies_vscreator2`](./NPC_Scripts.md#context-beanies_vscreator2) | Block | Examples: `{ ... }` | 1 |
| [`beanies_vscreator3`](./NPC_Scripts.md#context-beanies_vscreator3) | Block | Examples: `{ ... }` | 1 |
| [`beanies_vscreator4`](./NPC_Scripts.md#context-beanies_vscreator4) | Block | Examples: `{ ... }` | 1 |
| [`beanies_vscreatorintro`](./NPC_Scripts.md#context-beanies_vscreatorintro) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_AI`](./NPC_Scripts.md#context-beaniesquest_complete_ai) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_AirHorn`](./NPC_Scripts.md#context-beaniesquest_complete_airhorn) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_AngryFace`](./NPC_Scripts.md#context-beaniesquest_complete_angryface) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_AnimalHands`](./NPC_Scripts.md#context-beaniesquest_complete_animalhands) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_BubbleBoy`](./NPC_Scripts.md#context-beaniesquest_complete_bubbleboy) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_ChadImplant`](./NPC_Scripts.md#context-beaniesquest_complete_chadimplant) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_ChaosDevice`](./NPC_Scripts.md#context-beaniesquest_complete_chaosdevice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_DimensionalDivider`](./NPC_Scripts.md#context-beaniesquest_complete_dimensionaldivider) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_DiseaseJar`](./NPC_Scripts.md#context-beaniesquest_complete_diseasejar) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_ExperimentalTreatment`](./NPC_Scripts.md#context-beaniesquest_complete_experimentaltreatment) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_FartFace`](./NPC_Scripts.md#context-beaniesquest_complete_fartface) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_FigLeaf`](./NPC_Scripts.md#context-beaniesquest_complete_figleaf) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_Generic`](./NPC_Scripts.md#context-beaniesquest_complete_generic) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_GlassCannon`](./NPC_Scripts.md#context-beaniesquest_complete_glasscannon) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_HardPill`](./NPC_Scripts.md#context-beaniesquest_complete_hardpill) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_HiveMind`](./NPC_Scripts.md#context-beaniesquest_complete_hivemind) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_MagicMirror`](./NPC_Scripts.md#context-beaniesquest_complete_magicmirror) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_MeStone`](./NPC_Scripts.md#context-beaniesquest_complete_mestone) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_MultilinkCable`](./NPC_Scripts.md#context-beaniesquest_complete_multilinkcable) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_MysteriousDice`](./NPC_Scripts.md#context-beaniesquest_complete_mysteriousdice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_MysteriousGlasses`](./NPC_Scripts.md#context-beaniesquest_complete_mysteriousglasses) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_NDEDevice`](./NPC_Scripts.md#context-beaniesquest_complete_ndedevice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_NuclearKnife`](./NPC_Scripts.md#context-beaniesquest_complete_nuclearknife) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_PartialLobotomy`](./NPC_Scripts.md#context-beaniesquest_complete_partiallobotomy) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_PartyDetonator`](./NPC_Scripts.md#context-beaniesquest_complete_partydetonator) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_PersonalHeater`](./NPC_Scripts.md#context-beaniesquest_complete_personalheater) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_PersuasionDevice`](./NPC_Scripts.md#context-beaniesquest_complete_persuasiondevice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_PrincessHat`](./NPC_Scripts.md#context-beaniesquest_complete_princesshat) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_RealityScrambler`](./NPC_Scripts.md#context-beaniesquest_complete_realityscrambler) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_Redacted`](./NPC_Scripts.md#context-beaniesquest_complete_redacted) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_SpiderInjector`](./NPC_Scripts.md#context-beaniesquest_complete_spiderinjector) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_Stopwatch`](./NPC_Scripts.md#context-beaniesquest_complete_stopwatch) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_StorageLocker`](./NPC_Scripts.md#context-beaniesquest_complete_storagelocker) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_TheIOU`](./NPC_Scripts.md#context-beaniesquest_complete_theiou) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_TheLoner`](./NPC_Scripts.md#context-beaniesquest_complete_theloner) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_Trapfest99`](./NPC_Scripts.md#context-beaniesquest_complete_trapfest99) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_complete_UltraVision3000`](./NPC_Scripts.md#context-beaniesquest_complete_ultravision3000) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_AI`](./NPC_Scripts.md#context-beaniesquest_fail_ai) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_AirHorn`](./NPC_Scripts.md#context-beaniesquest_fail_airhorn) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_AngryFace`](./NPC_Scripts.md#context-beaniesquest_fail_angryface) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_AnimalHands`](./NPC_Scripts.md#context-beaniesquest_fail_animalhands) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_BubbleBoy`](./NPC_Scripts.md#context-beaniesquest_fail_bubbleboy) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_ChadImplant`](./NPC_Scripts.md#context-beaniesquest_fail_chadimplant) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_ChaosDevice`](./NPC_Scripts.md#context-beaniesquest_fail_chaosdevice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_DimensionalDivider`](./NPC_Scripts.md#context-beaniesquest_fail_dimensionaldivider) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_DiseaseJar`](./NPC_Scripts.md#context-beaniesquest_fail_diseasejar) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_ExperimentalTreatment`](./NPC_Scripts.md#context-beaniesquest_fail_experimentaltreatment) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_FartFace`](./NPC_Scripts.md#context-beaniesquest_fail_fartface) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_FigLeaf`](./NPC_Scripts.md#context-beaniesquest_fail_figleaf) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_Generic`](./NPC_Scripts.md#context-beaniesquest_fail_generic) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_GlassCannon`](./NPC_Scripts.md#context-beaniesquest_fail_glasscannon) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_HardPill`](./NPC_Scripts.md#context-beaniesquest_fail_hardpill) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_HiveMind`](./NPC_Scripts.md#context-beaniesquest_fail_hivemind) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_MagicMirror`](./NPC_Scripts.md#context-beaniesquest_fail_magicmirror) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_MeStone`](./NPC_Scripts.md#context-beaniesquest_fail_mestone) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_MultilinkCable`](./NPC_Scripts.md#context-beaniesquest_fail_multilinkcable) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_MysteriousDice`](./NPC_Scripts.md#context-beaniesquest_fail_mysteriousdice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_MysteriousGlasses`](./NPC_Scripts.md#context-beaniesquest_fail_mysteriousglasses) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_NDEDevice`](./NPC_Scripts.md#context-beaniesquest_fail_ndedevice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_NuclearKnife`](./NPC_Scripts.md#context-beaniesquest_fail_nuclearknife) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_PartialLobotomy`](./NPC_Scripts.md#context-beaniesquest_fail_partiallobotomy) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_PartyDetonator`](./NPC_Scripts.md#context-beaniesquest_fail_partydetonator) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_PersonalHeater`](./NPC_Scripts.md#context-beaniesquest_fail_personalheater) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_PersuasionDevice`](./NPC_Scripts.md#context-beaniesquest_fail_persuasiondevice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_PrincessHat`](./NPC_Scripts.md#context-beaniesquest_fail_princesshat) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_RealityScrambler`](./NPC_Scripts.md#context-beaniesquest_fail_realityscrambler) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_Redacted`](./NPC_Scripts.md#context-beaniesquest_fail_redacted) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_SpiderInjector`](./NPC_Scripts.md#context-beaniesquest_fail_spiderinjector) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_Stopwatch`](./NPC_Scripts.md#context-beaniesquest_fail_stopwatch) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_StorageLocker`](./NPC_Scripts.md#context-beaniesquest_fail_storagelocker) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_TheIOU`](./NPC_Scripts.md#context-beaniesquest_fail_theiou) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_TheLoner`](./NPC_Scripts.md#context-beaniesquest_fail_theloner) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_Trapfest99`](./NPC_Scripts.md#context-beaniesquest_fail_trapfest99) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_fail_UltraVision3000`](./NPC_Scripts.md#context-beaniesquest_fail_ultravision3000) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_AI`](./NPC_Scripts.md#context-beaniesquest_intro_ai) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_AirHorn`](./NPC_Scripts.md#context-beaniesquest_intro_airhorn) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_AngryFace`](./NPC_Scripts.md#context-beaniesquest_intro_angryface) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_AnimalHands`](./NPC_Scripts.md#context-beaniesquest_intro_animalhands) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_BubbleBoy`](./NPC_Scripts.md#context-beaniesquest_intro_bubbleboy) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_ChadImplant`](./NPC_Scripts.md#context-beaniesquest_intro_chadimplant) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_ChaosDevice`](./NPC_Scripts.md#context-beaniesquest_intro_chaosdevice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_DimensionalDivider`](./NPC_Scripts.md#context-beaniesquest_intro_dimensionaldivider) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_DiseaseJar`](./NPC_Scripts.md#context-beaniesquest_intro_diseasejar) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_ExperimentalTreatment`](./NPC_Scripts.md#context-beaniesquest_intro_experimentaltreatment) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_FartFace`](./NPC_Scripts.md#context-beaniesquest_intro_fartface) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_FigLeaf`](./NPC_Scripts.md#context-beaniesquest_intro_figleaf) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_Generic`](./NPC_Scripts.md#context-beaniesquest_intro_generic) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_GlassCannon`](./NPC_Scripts.md#context-beaniesquest_intro_glasscannon) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_HardPill`](./NPC_Scripts.md#context-beaniesquest_intro_hardpill) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_HiveMind`](./NPC_Scripts.md#context-beaniesquest_intro_hivemind) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_MagicMirror`](./NPC_Scripts.md#context-beaniesquest_intro_magicmirror) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_MeStone`](./NPC_Scripts.md#context-beaniesquest_intro_mestone) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_MultilinkCable`](./NPC_Scripts.md#context-beaniesquest_intro_multilinkcable) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_MysteriousDice`](./NPC_Scripts.md#context-beaniesquest_intro_mysteriousdice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_MysteriousGlasses`](./NPC_Scripts.md#context-beaniesquest_intro_mysteriousglasses) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_NDEDevice`](./NPC_Scripts.md#context-beaniesquest_intro_ndedevice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_NuclearKnife`](./NPC_Scripts.md#context-beaniesquest_intro_nuclearknife) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_PartialLobotomy`](./NPC_Scripts.md#context-beaniesquest_intro_partiallobotomy) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_PartyDetonator`](./NPC_Scripts.md#context-beaniesquest_intro_partydetonator) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_PersonalHeater`](./NPC_Scripts.md#context-beaniesquest_intro_personalheater) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_PersuasionDevice`](./NPC_Scripts.md#context-beaniesquest_intro_persuasiondevice) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_PrincessHat`](./NPC_Scripts.md#context-beaniesquest_intro_princesshat) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_RealityScrambler`](./NPC_Scripts.md#context-beaniesquest_intro_realityscrambler) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_Redacted`](./NPC_Scripts.md#context-beaniesquest_intro_redacted) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_SpiderInjector`](./NPC_Scripts.md#context-beaniesquest_intro_spiderinjector) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_Stopwatch`](./NPC_Scripts.md#context-beaniesquest_intro_stopwatch) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_StorageLocker`](./NPC_Scripts.md#context-beaniesquest_intro_storagelocker) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_TheIOU`](./NPC_Scripts.md#context-beaniesquest_intro_theiou) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_TheLoner`](./NPC_Scripts.md#context-beaniesquest_intro_theloner) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_Trapfest99`](./NPC_Scripts.md#context-beaniesquest_intro_trapfest99) | Block | Examples: `{ ... }` | 1 |
| [`beaniesquest_intro_UltraVision3000`](./NPC_Scripts.md#context-beaniesquest_intro_ultravision3000) | Block | Examples: `{ ... }` | 1 |
| [`boss_fight_intro`](./NPC_Scripts.md#context-boss_fight_intro) | Block | Examples: `{ ... }` | 1 |
| [`boss_fight_round2`](./NPC_Scripts.md#context-boss_fight_round2) | Block | Examples: `{ ... }` | 1 |
| [`butch_begin_accepting_cats`](./NPC_Scripts.md#context-butch_begin_accepting_cats) | Block | Examples: `{ ... }` | 1 |
| [`butch_boneyard_intro`](./NPC_Scripts.md#context-butch_boneyard_intro) | Block | Examples: `{ ... }` | 1 |
| [`butch_first_house_boss_beat`](./NPC_Scripts.md#context-butch_first_house_boss_beat) | Block | Examples: `{ ... }` | 1 |
| [`butch_pyro`](./NPC_Scripts.md#context-butch_pyro) | Block | Examples: `{ ... }` | 1 |
| [`butch_tina1`](./NPC_Scripts.md#context-butch_tina1) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_backstab`](./NPC_Scripts.md#context-butch_tips_backstab) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_charisma`](./NPC_Scripts.md#context-butch_tips_charisma) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_combat`](./NPC_Scripts.md#context-butch_tips_combat) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_disorders`](./NPC_Scripts.md#context-butch_tips_disorders) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_drafting`](./NPC_Scripts.md#context-butch_tips_drafting) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_elements`](./NPC_Scripts.md#context-butch_tips_elements) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_hard`](./NPC_Scripts.md#context-butch_tips_hard) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_headhome`](./NPC_Scripts.md#context-butch_tips_headhome) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_houseboss`](./NPC_Scripts.md#context-butch_tips_houseboss) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_info`](./NPC_Scripts.md#context-butch_tips_info) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_intelligence`](./NPC_Scripts.md#context-butch_tips_intelligence) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_intro`](./NPC_Scripts.md#context-butch_tips_intro) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_items`](./NPC_Scripts.md#context-butch_tips_items) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_lesscats`](./NPC_Scripts.md#context-butch_tips_lesscats) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_magicdamage`](./NPC_Scripts.md#context-butch_tips_magicdamage) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_passives`](./NPC_Scripts.md#context-butch_tips_passives) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_reorient`](./NPC_Scripts.md#context-butch_tips_reorient) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_rewards`](./NPC_Scripts.md#context-butch_tips_rewards) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_tacticalview`](./NPC_Scripts.md#context-butch_tips_tacticalview) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_turnorder`](./NPC_Scripts.md#context-butch_tips_turnorder) | Block | Examples: `{ ... }` | 1 |
| [`butch_tips_wellrounded`](./NPC_Scripts.md#context-butch_tips_wellrounded) | Block | Examples: `{ ... }` | 1 |
| [`can_still_use_attack`](./NPC_Scripts.md#context-can_still_use_attack) | Block | Examples: `{ ... }` | 1 |
| [`can_still_use_attack_didntspell`](./NPC_Scripts.md#context-can_still_use_attack_didntspell) | Block | Examples: `{ ... }` | 1 |
| [`cant_afford_a`](./NPC_Scripts.md#context-cant_afford_a) | Block | Examples: `{ ... }` | 1 |
| [`cant_afford_b`](./NPC_Scripts.md#context-cant_afford_b) | Block | Examples: `{ ... }` | 1 |
| [`cant_afford_c`](./NPC_Scripts.md#context-cant_afford_c) | Block | Examples: `{ ... }` | 1 |
| [`cant_afford_d`](./NPC_Scripts.md#context-cant_afford_d) | Block | Examples: `{ ... }` | 1 |
| [`cant_afford_iceage`](./NPC_Scripts.md#context-cant_afford_iceage) | Block | Examples: `{ ... }` | 1 |
| [`cant_afford_jurassic`](./NPC_Scripts.md#context-cant_afford_jurassic) | Block | Examples: `{ ... }` | 1 |
| [`cant_afford_moon`](./NPC_Scripts.md#context-cant_afford_moon) | Block | Examples: `{ ... }` | 1 |
| [`cant_afford_theend`](./NPC_Scripts.md#context-cant_afford_theend) | Block | Examples: `{ ... }` | 1 |
| [`class_unlock_butcher`](./NPC_Scripts.md#context-class_unlock_butcher) | Block | Examples: `{ ... }` | 1 |
| [`class_unlock_druid`](./NPC_Scripts.md#context-class_unlock_druid) | Block | Examples: `{ ... }` | 1 |
| [`class_unlock_jester`](./NPC_Scripts.md#context-class_unlock_jester) | Block | Examples: `{ ... }` | 1 |
| [`class_unlock_medic`](./NPC_Scripts.md#context-class_unlock_medic) | Block | Examples: `{ ... }` | 1 |
| [`class_unlock_monk`](./NPC_Scripts.md#context-class_unlock_monk) | Block | Examples: `{ ... }` | 1 |
| [`class_unlock_necromancer`](./NPC_Scripts.md#context-class_unlock_necromancer) | Block | Examples: `{ ... }` | 1 |
| [`class_unlock_psychic`](./NPC_Scripts.md#context-class_unlock_psychic) | Block | Examples: `{ ... }` | 1 |
| [`class_unlock_thief`](./NPC_Scripts.md#context-class_unlock_thief) | Block | Examples: `{ ... }` | 1 |
| [`class_unlock_tinkerer`](./NPC_Scripts.md#context-class_unlock_tinkerer) | Block | Examples: `{ ... }` | 1 |
| [`collected_new_items`](./NPC_Scripts.md#context-collected_new_items) | Block | Examples: `{ ... }` | 1 |
| [`collected_nothing`](./NPC_Scripts.md#context-collected_nothing) | Block | Examples: `{ ... }` | 1 |
| [`do_not_end_turn`](./NPC_Scripts.md#context-do_not_end_turn) | Block | Examples: `{ ... }` | 1 |
| [`done_spitting_fail_ally`](./NPC_Scripts.md#context-done_spitting_fail_ally) | Block | Examples: `{ ... }` | 1 |
| [`done_spitting_fail_miss`](./NPC_Scripts.md#context-done_spitting_fail_miss) | Block | Examples: `{ ... }` | 1 |
| [`done_spitting_fail_rat`](./NPC_Scripts.md#context-done_spitting_fail_rat) | Block | Examples: `{ ... }` | 1 |
| [`done_spitting_success`](./NPC_Scripts.md#context-done_spitting_success) | Block | Examples: `{ ... }` | 1 |
| [`ending`](./NPC_Scripts.md#context-ending) | Block | Examples: `{ ... }` | 1 |
| [`finish_adventure`](./NPC_Scripts.md#context-finish_adventure) | Block | Examples: `{ ... }` | 1 |
| [`first_fight_intro`](./NPC_Scripts.md#context-first_fight_intro) | Block | Examples: `{ ... }` | 1 |
| [`first_house_boss_tomorrow`](./NPC_Scripts.md#context-first_house_boss_tomorrow) | Block | Examples: `{ ... }` | 1 |
| [`first_house_hint_retired`](./NPC_Scripts.md#context-first_house_hint_retired) | Block | Examples: `{ ... }` | 1 |
| [`frank_caves_intro`](./NPC_Scripts.md#context-frank_caves_intro) | Block | Examples: `{ ... }` | 1 |
| [`frank_ending`](./NPC_Scripts.md#context-frank_ending) | Block | Examples: `{ ... }` | 1 |
| [`frank_max1`](./NPC_Scripts.md#context-frank_max1) | Block | Examples: `{ ... }` | 1 |
| [`frank_max2`](./NPC_Scripts.md#context-frank_max2) | Block | Examples: `{ ... }` | 1 |
| [`frank_max3`](./NPC_Scripts.md#context-frank_max3) | Block | Examples: `{ ... }` | 1 |
| [`frank_max4`](./NPC_Scripts.md#context-frank_max4) | Block | Examples: `{ ... }` | 1 |
| [`frank_max5`](./NPC_Scripts.md#context-frank_max5) | Block | Examples: `{ ... }` | 1 |
| [`frank_max_intro`](./NPC_Scripts.md#context-frank_max_intro) | Block | Examples: `{ ... }` | 1 |
| [`frank_max_repeating`](./NPC_Scripts.md#context-frank_max_repeating) | Block | Examples: `{ ... }` | 1 |
| [`frank_terminator2`](./NPC_Scripts.md#context-frank_terminator2) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_1`](./NPC_Scripts.md#context-frank_tips_1) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_10`](./NPC_Scripts.md#context-frank_tips_10) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_2`](./NPC_Scripts.md#context-frank_tips_2) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_3`](./NPC_Scripts.md#context-frank_tips_3) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_4`](./NPC_Scripts.md#context-frank_tips_4) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_5`](./NPC_Scripts.md#context-frank_tips_5) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_6`](./NPC_Scripts.md#context-frank_tips_6) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_7`](./NPC_Scripts.md#context-frank_tips_7) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_8`](./NPC_Scripts.md#context-frank_tips_8) | Block | Examples: `{ ... }` | 1 |
| [`frank_tips_9`](./NPC_Scripts.md#context-frank_tips_9) | Block | Examples: `{ ... }` | 1 |
| [`gone`](./NPC_Scripts.md#context-gone) | Block | Examples: `{ ... }` | 1 |
| [`house_intro`](./NPC_Scripts.md#context-house_intro) | Block | Examples: `{ ... }` | 1 |
| [`house_kitten_box`](./NPC_Scripts.md#context-house_kitten_box) | Block | Examples: `{ ... }` | 1 |
| [`house_pass_day`](./NPC_Scripts.md#context-house_pass_day) | Block | Examples: `{ ... }` | 1 |
| [`house_pass_day2`](./NPC_Scripts.md#context-house_pass_day2) | Block | Examples: `{ ... }` | 1 |
| [`house_pipe`](./NPC_Scripts.md#context-house_pipe) | Block | Examples: `{ ... }` | 1 |
| [`house_retired_cat_box`](./NPC_Scripts.md#context-house_retired_cat_box) | Block | Examples: `{ ... }` | 1 |
| [`house_starred_box`](./NPC_Scripts.md#context-house_starred_box) | Block | Examples: `{ ... }` | 1 |
| [`house_strays`](./NPC_Scripts.md#context-house_strays) | Block | Examples: `{ ... }` | 1 |
| [`house_upgrade_4throom`](./NPC_Scripts.md#context-house_upgrade_4throom) | Block | Examples: `{ ... }` | 1 |
| [`house_upgrade_attic`](./NPC_Scripts.md#context-house_upgrade_attic) | Block | Examples: `{ ... }` | 1 |
| [`house_upgrade_basement`](./NPC_Scripts.md#context-house_upgrade_basement) | Block | Examples: `{ ... }` | 1 |
| [`house_upgrade_basement2`](./NPC_Scripts.md#context-house_upgrade_basement2) | Block | Examples: `{ ... }` | 1 |
| [`house_upgrade_basement3`](./NPC_Scripts.md#context-house_upgrade_basement3) | Block | Examples: `{ ... }` | 1 |
| [`house_upgrade_basement4`](./NPC_Scripts.md#context-house_upgrade_basement4) | Block | Examples: `{ ... }` | 1 |
| [`house_upgrade_basement5`](./NPC_Scripts.md#context-house_upgrade_basement5) | Block | Examples: `{ ... }` | 1 |
| [`house_upgrade_largehouse`](./NPC_Scripts.md#context-house_upgrade_largehouse) | Block | Examples: `{ ... }` | 1 |
| [`house_upgrade_mediumhouse`](./NPC_Scripts.md#context-house_upgrade_mediumhouse) | Block | Examples: `{ ... }` | 1 |
| [`intro`](./NPC_Scripts.md#context-intro) | Block | Examples: `{ ... }` | 1 |
| [`introduce_hard_path`](./NPC_Scripts.md#context-introduce_hard_path) | Block | Examples: `{ ... }` | 1 |
| [`jack_begin_accepting_cats`](./NPC_Scripts.md#context-jack_begin_accepting_cats) | Block | Examples: `{ ... }` | 1 |
| [`jack_desert_intro`](./NPC_Scripts.md#context-jack_desert_intro) | Block | Examples: `{ ... }` | 1 |
| [`jack_introduction`](./NPC_Scripts.md#context-jack_introduction) | Block | Examples: `{ ... }` | 1 |
| [`jack_max1`](./NPC_Scripts.md#context-jack_max1) | Block | Examples: `{ ... }` | 1 |
| [`jack_max2`](./NPC_Scripts.md#context-jack_max2) | Block | Examples: `{ ... }` | 1 |
| [`jack_max3`](./NPC_Scripts.md#context-jack_max3) | Block | Examples: `{ ... }` | 1 |
| [`jack_max4`](./NPC_Scripts.md#context-jack_max4) | Block | Examples: `{ ... }` | 1 |
| [`jack_max5`](./NPC_Scripts.md#context-jack_max5) | Block | Examples: `{ ... }` | 1 |
| [`jack_max_intro`](./NPC_Scripts.md#context-jack_max_intro) | Block | Examples: `{ ... }` | 1 |
| [`jack_max_repeating`](./NPC_Scripts.md#context-jack_max_repeating) | Block | Examples: `{ ... }` | 1 |
| [`jack_shopupgrade1`](./NPC_Scripts.md#context-jack_shopupgrade1) | Block | Examples: `{ ... }` | 1 |
| [`jack_shopupgrade2`](./NPC_Scripts.md#context-jack_shopupgrade2) | Block | Examples: `{ ... }` | 1 |
| [`jack_shopupgrade3`](./NPC_Scripts.md#context-jack_shopupgrade3) | Block | Examples: `{ ... }` | 1 |
| [`jack_shopupgrade4`](./NPC_Scripts.md#context-jack_shopupgrade4) | Block | Examples: `{ ... }` | 1 |
| [`jack_zara`](./NPC_Scripts.md#context-jack_zara) | Block | Examples: `{ ... }` | 1 |
| [`level_up_didnt_select_sunburn`](./NPC_Scripts.md#context-level_up_didnt_select_sunburn) | Block | Examples: `{ ... }` | 1 |
| [`level_up_intro`](./NPC_Scripts.md#context-level_up_intro) | Block | Examples: `{ ... }` | 1 |
| [`level_up_selected_sunburn`](./NPC_Scripts.md#context-level_up_selected_sunburn) | Block | Examples: `{ ... }` | 1 |
| [`low_on_food`](./NPC_Scripts.md#context-low_on_food) | Block | Examples: `{ ... }` | 1 |
| [`map_click_node`](./NPC_Scripts.md#context-map_click_node) | Block | Examples: `{ ... }` | 1 |
| [`map_equip_items`](./NPC_Scripts.md#context-map_equip_items) | Block | Examples: `{ ... }` | 1 |
| [`map_equip_items2`](./NPC_Scripts.md#context-map_equip_items2) | Block | Examples: `{ ... }` | 1 |
| [`melee_attack_rat`](./NPC_Scripts.md#context-melee_attack_rat) | Block | Examples: `{ ... }` | 1 |
| [`melee_cat_spit`](./NPC_Scripts.md#context-melee_cat_spit) | Block | Examples: `{ ... }` | 1 |
| [`melee_cat_spit_fail_ally`](./NPC_Scripts.md#context-melee_cat_spit_fail_ally) | Block | Examples: `{ ... }` | 1 |
| [`melee_cat_spit_fail_miss`](./NPC_Scripts.md#context-melee_cat_spit_fail_miss) | Block | Examples: `{ ... }` | 1 |
| [`melee_cat_spit_fail_rat`](./NPC_Scripts.md#context-melee_cat_spit_fail_rat) | Block | Examples: `{ ... }` | 1 |
| [`melee_cat_spit_ignore`](./NPC_Scripts.md#context-melee_cat_spit_ignore) | Block | Examples: `{ ... }` | 1 |
| [`melee_cat_spit_success`](./NPC_Scripts.md#context-melee_cat_spit_success) | Block | Examples: `{ ... }` | 1 |
| [`melee_killed_rat`](./NPC_Scripts.md#context-melee_killed_rat) | Block | Examples: `{ ... }` | 1 |
| [`melee_move2`](./NPC_Scripts.md#context-melee_move2) | Block | Examples: `{ ... }` | 1 |
| [`melee_out_of_actions`](./NPC_Scripts.md#context-melee_out_of_actions) | Block | Examples: `{ ... }` | 1 |
| [`new_adventure`](./NPC_Scripts.md#context-new_adventure) | Block | Examples: `{ ... }` | 1 |
| [`organ_boneyard_intro`](./NPC_Scripts.md#context-organ_boneyard_intro) | Block | Examples: `{ ... }` | 1 |
| [`organ_intro`](./NPC_Scripts.md#context-organ_intro) | Block | Examples: `{ ... }` | 1 |
| [`organ_max1`](./NPC_Scripts.md#context-organ_max1) | Block | Examples: `{ ... }` | 1 |
| [`organ_max2`](./NPC_Scripts.md#context-organ_max2) | Block | Examples: `{ ... }` | 1 |
| [`organ_max3`](./NPC_Scripts.md#context-organ_max3) | Block | Examples: `{ ... }` | 1 |
| [`organ_max4`](./NPC_Scripts.md#context-organ_max4) | Block | Examples: `{ ... }` | 1 |
| [`organ_max5`](./NPC_Scripts.md#context-organ_max5) | Block | Examples: `{ ... }` | 1 |
| [`organ_max_intro`](./NPC_Scripts.md#context-organ_max_intro) | Block | Examples: `{ ... }` | 1 |
| [`organ_max_repeating`](./NPC_Scripts.md#context-organ_max_repeating) | Block | Examples: `{ ... }` | 1 |
| [`organ_rename`](./NPC_Scripts.md#context-organ_rename) | Block | Examples: `{ ... }` | 1 |
| [`organ_throbbingdomain_intro`](./NPC_Scripts.md#context-organ_throbbingdomain_intro) | Block | Examples: `{ ... }` | 1 |
| [`organ_tina3`](./NPC_Scripts.md#context-organ_tina3) | Block | Examples: `{ ... }` | 1 |
| [`organ_unlock`](./NPC_Scripts.md#context-organ_unlock) | Block | Examples: `{ ... }` | 1 |
| [`organ_upgrade1`](./NPC_Scripts.md#context-organ_upgrade1) | Block | Examples: `{ ... }` | 1 |
| [`organ_upgrade2`](./NPC_Scripts.md#context-organ_upgrade2) | Block | Examples: `{ ... }` | 1 |
| [`organ_upgrade3`](./NPC_Scripts.md#context-organ_upgrade3) | Block | Examples: `{ ... }` | 1 |
| [`organ_upgrade4`](./NPC_Scripts.md#context-organ_upgrade4) | Block | Examples: `{ ... }` | 1 |
| [`organ_upgrade5`](./NPC_Scripts.md#context-organ_upgrade5) | Block | Examples: `{ ... }` | 1 |
| [`organ_upgrade6`](./NPC_Scripts.md#context-organ_upgrade6) | Block | Examples: `{ ... }` | 1 |
| [`purchase_item_a`](./NPC_Scripts.md#context-purchase_item_a) | Block | Examples: `{ ... }` | 1 |
| [`purchase_item_b`](./NPC_Scripts.md#context-purchase_item_b) | Block | Examples: `{ ... }` | 1 |
| [`purchase_item_c`](./NPC_Scripts.md#context-purchase_item_c) | Block | Examples: `{ ... }` | 1 |
| [`purchase_item_d`](./NPC_Scripts.md#context-purchase_item_d) | Block | Examples: `{ ... }` | 1 |
| [`purchase_item_iceage`](./NPC_Scripts.md#context-purchase_item_iceage) | Block | Examples: `{ ... }` | 1 |
| [`purchase_item_jurassic`](./NPC_Scripts.md#context-purchase_item_jurassic) | Block | Examples: `{ ... }` | 1 |
| [`purchase_item_moon`](./NPC_Scripts.md#context-purchase_item_moon) | Block | Examples: `{ ... }` | 1 |
| [`purchase_item_theend`](./NPC_Scripts.md#context-purchase_item_theend) | Block | Examples: `{ ... }` | 1 |
| [`ranged_attack_tomtom`](./NPC_Scripts.md#context-ranged_attack_tomtom) | Block | Examples: `{ ... }` | 1 |
| [`ranged_attack_tomtom_fail_ally`](./NPC_Scripts.md#context-ranged_attack_tomtom_fail_ally) | Block | Examples: `{ ... }` | 1 |
| [`ranged_attack_tomtom_fail_miss`](./NPC_Scripts.md#context-ranged_attack_tomtom_fail_miss) | Block | Examples: `{ ... }` | 1 |
| [`ranged_attack_tomtom_fail_rat`](./NPC_Scripts.md#context-ranged_attack_tomtom_fail_rat) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_attack`](./NPC_Scripts.md#context-ranged_cat_attack) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_early_attack2_ally`](./NPC_Scripts.md#context-ranged_cat_early_attack2_ally) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_early_attack2_miss`](./NPC_Scripts.md#context-ranged_cat_early_attack2_miss) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_early_attack2_rat`](./NPC_Scripts.md#context-ranged_cat_early_attack2_rat) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_early_attack_ally`](./NPC_Scripts.md#context-ranged_cat_early_attack_ally) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_early_attack_miss`](./NPC_Scripts.md#context-ranged_cat_early_attack_miss) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_early_attack_rat`](./NPC_Scripts.md#context-ranged_cat_early_attack_rat) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_failmove`](./NPC_Scripts.md#context-ranged_cat_failmove) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_intro`](./NPC_Scripts.md#context-ranged_cat_intro) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_roll`](./NPC_Scripts.md#context-ranged_cat_roll) | Block | Examples: `{ ... }` | 1 |
| [`ranged_cat_rolled_first`](./NPC_Scripts.md#context-ranged_cat_rolled_first) | Block | Examples: `{ ... }` | 1 |
| [`steven_100`](./NPC_Scripts.md#context-steven_100) | Block | Examples: `{ ... }` | 1 |
| [`steven_introduction`](./NPC_Scripts.md#context-steven_introduction) | Block | Examples: `{ ... }` | 1 |
| [`steven_milliontrashed`](./NPC_Scripts.md#context-steven_milliontrashed) | Block | Examples: `{ ... }` | 1 |
| [`steven_postendgame`](./NPC_Scripts.md#context-steven_postendgame) | Block | Examples: `{ ... }` | 1 |
| [`steven_resummon`](./NPC_Scripts.md#context-steven_resummon) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_1`](./NPC_Scripts.md#context-steven_savescum_1) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_100`](./NPC_Scripts.md#context-steven_savescum_100) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_1alt1`](./NPC_Scripts.md#context-steven_savescum_1alt1) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_1alt2`](./NPC_Scripts.md#context-steven_savescum_1alt2) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_1alt3`](./NPC_Scripts.md#context-steven_savescum_1alt3) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_2`](./NPC_Scripts.md#context-steven_savescum_2) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_2alt1`](./NPC_Scripts.md#context-steven_savescum_2alt1) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_2alt2`](./NPC_Scripts.md#context-steven_savescum_2alt2) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_2alt3`](./NPC_Scripts.md#context-steven_savescum_2alt3) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_3`](./NPC_Scripts.md#context-steven_savescum_3) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_3alt1`](./NPC_Scripts.md#context-steven_savescum_3alt1) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_3alt2`](./NPC_Scripts.md#context-steven_savescum_3alt2) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_3alt3`](./NPC_Scripts.md#context-steven_savescum_3alt3) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_4`](./NPC_Scripts.md#context-steven_savescum_4) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_4alt1`](./NPC_Scripts.md#context-steven_savescum_4alt1) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_4alt2`](./NPC_Scripts.md#context-steven_savescum_4alt2) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_4alt3`](./NPC_Scripts.md#context-steven_savescum_4alt3) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_houseboss_1`](./NPC_Scripts.md#context-steven_savescum_houseboss_1) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_houseboss_100`](./NPC_Scripts.md#context-steven_savescum_houseboss_100) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_houseboss_2`](./NPC_Scripts.md#context-steven_savescum_houseboss_2) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_houseboss_3`](./NPC_Scripts.md#context-steven_savescum_houseboss_3) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_intro`](./NPC_Scripts.md#context-steven_savescum_intro) | Block | Examples: `{ ... }` | 1 |
| [`steven_savescum_intro_houseboss`](./NPC_Scripts.md#context-steven_savescum_intro_houseboss) | Block | Examples: `{ ... }` | 1 |
| [`steven_unlock_act1_crazy`](./NPC_Scripts.md#context-steven_unlock_act1_crazy) | Block | Examples: `{ ... }` | 1 |
| [`steven_unlock_act1_impossible`](./NPC_Scripts.md#context-steven_unlock_act1_impossible) | Block | Examples: `{ ... }` | 1 |
| [`steven_unlock_act2_crazy`](./NPC_Scripts.md#context-steven_unlock_act2_crazy) | Block | Examples: `{ ... }` | 1 |
| [`steven_unlock_act2_hard`](./NPC_Scripts.md#context-steven_unlock_act2_hard) | Block | Examples: `{ ... }` | 1 |
| [`steven_unlock_act2_impossible`](./NPC_Scripts.md#context-steven_unlock_act2_impossible) | Block | Examples: `{ ... }` | 1 |
| [`steven_unlock_act3_crazy`](./NPC_Scripts.md#context-steven_unlock_act3_crazy) | Block | Examples: `{ ... }` | 1 |
| [`steven_unlock_act3_hard`](./NPC_Scripts.md#context-steven_unlock_act3_hard) | Block | Examples: `{ ... }` | 1 |
| [`steven_unlock_act3_impossible`](./NPC_Scripts.md#context-steven_unlock_act3_impossible) | Block | Examples: `{ ... }` | 1 |
| [`take_cats_inside`](./NPC_Scripts.md#context-take_cats_inside) | Block | Examples: `{ ... }` | 1 |
| [`test_gamepad_prompts`](./NPC_Scripts.md#context-test_gamepad_prompts) | Block | Examples: `{ ... }` | 1 |
| [`tink_aggression`](./NPC_Scripts.md#context-tink_aggression) | Block | Examples: `{ ... }` | 1 |
| [`tink_basestats`](./NPC_Scripts.md#context-tink_basestats) | Block | Examples: `{ ... }` | 1 |
| [`tink_begin_accepting_cats`](./NPC_Scripts.md#context-tink_begin_accepting_cats) | Block | Examples: `{ ... }` | 1 |
| [`tink_inbreeding`](./NPC_Scripts.md#context-tink_inbreeding) | Block | Examples: `{ ... }` | 1 |
| [`tink_max1`](./NPC_Scripts.md#context-tink_max1) | Block | Examples: `{ ... }` | 1 |
| [`tink_max10`](./NPC_Scripts.md#context-tink_max10) | Block | Examples: `{ ... }` | 1 |
| [`tink_max2`](./NPC_Scripts.md#context-tink_max2) | Block | Examples: `{ ... }` | 1 |
| [`tink_max3`](./NPC_Scripts.md#context-tink_max3) | Block | Examples: `{ ... }` | 1 |
| [`tink_max4`](./NPC_Scripts.md#context-tink_max4) | Block | Examples: `{ ... }` | 1 |
| [`tink_max5`](./NPC_Scripts.md#context-tink_max5) | Block | Examples: `{ ... }` | 1 |
| [`tink_max6`](./NPC_Scripts.md#context-tink_max6) | Block | Examples: `{ ... }` | 1 |
| [`tink_max7`](./NPC_Scripts.md#context-tink_max7) | Block | Examples: `{ ... }` | 1 |
| [`tink_max8`](./NPC_Scripts.md#context-tink_max8) | Block | Examples: `{ ... }` | 1 |
| [`tink_max9`](./NPC_Scripts.md#context-tink_max9) | Block | Examples: `{ ... }` | 1 |
| [`tink_max_intro`](./NPC_Scripts.md#context-tink_max_intro) | Block | Examples: `{ ... }` | 1 |
| [`tink_max_repeating`](./NPC_Scripts.md#context-tink_max_repeating) | Block | Examples: `{ ... }` | 1 |
| [`tink_prettybow`](./NPC_Scripts.md#context-tink_prettybow) | Block | Examples: `{ ... }` | 1 |
| [`tink_relationships`](./NPC_Scripts.md#context-tink_relationships) | Block | Examples: `{ ... }` | 1 |
| [`tink_sexuality`](./NPC_Scripts.md#context-tink_sexuality) | Block | Examples: `{ ... }` | 1 |
| [`tink_tags`](./NPC_Scripts.md#context-tink_tags) | Block | Examples: `{ ... }` | 1 |
| [`tink_terminator`](./NPC_Scripts.md#context-tink_terminator) | Block | Examples: `{ ... }` | 1 |
| [`tink_tina2`](./NPC_Scripts.md#context-tink_tina2) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_appeal`](./NPC_Scripts.md#context-tink_tips_appeal) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_basestats`](./NPC_Scripts.md#context-tink_tips_basestats) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_cleaning`](./NPC_Scripts.md#context-tink_tips_cleaning) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_comfort`](./NPC_Scripts.md#context-tink_tips_comfort) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_health`](./NPC_Scripts.md#context-tink_tips_health) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_inbreeding`](./NPC_Scripts.md#context-tink_tips_inbreeding) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_intro`](./NPC_Scripts.md#context-tink_tips_intro) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_multiclassing`](./NPC_Scripts.md#context-tink_tips_multiclassing) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_mutation`](./NPC_Scripts.md#context-tink_tips_mutation) | Block | Examples: `{ ... }` | 1 |
| [`tink_tips_stimulation`](./NPC_Scripts.md#context-tink_tips_stimulation) | Block | Examples: `{ ... }` | 1 |
| [`tracy_blankcollar1`](./NPC_Scripts.md#context-tracy_blankcollar1) | Block | Examples: `{ ... }` | 1 |
| [`tracy_blankcollar2`](./NPC_Scripts.md#context-tracy_blankcollar2) | Block | Examples: `{ ... }` | 1 |
| [`tracy_blankcollar3`](./NPC_Scripts.md#context-tracy_blankcollar3) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodbonus1`](./NPC_Scripts.md#context-tracy_foodbonus1) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage1`](./NPC_Scripts.md#context-tracy_foodstorage1) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage10`](./NPC_Scripts.md#context-tracy_foodstorage10) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage2`](./NPC_Scripts.md#context-tracy_foodstorage2) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage3`](./NPC_Scripts.md#context-tracy_foodstorage3) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage4`](./NPC_Scripts.md#context-tracy_foodstorage4) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage5`](./NPC_Scripts.md#context-tracy_foodstorage5) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage6`](./NPC_Scripts.md#context-tracy_foodstorage6) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage7`](./NPC_Scripts.md#context-tracy_foodstorage7) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage8`](./NPC_Scripts.md#context-tracy_foodstorage8) | Block | Examples: `{ ... }` | 1 |
| [`tracy_foodstorage9`](./NPC_Scripts.md#context-tracy_foodstorage9) | Block | Examples: `{ ... }` | 1 |
| [`tracy_idol1`](./NPC_Scripts.md#context-tracy_idol1) | Block | Examples: `{ ... }` | 1 |
| [`tracy_idol2`](./NPC_Scripts.md#context-tracy_idol2) | Block | Examples: `{ ... }` | 1 |
| [`tracy_idol3`](./NPC_Scripts.md#context-tracy_idol3) | Block | Examples: `{ ... }` | 1 |
| [`tracy_idol4`](./NPC_Scripts.md#context-tracy_idol4) | Block | Examples: `{ ... }` | 1 |
| [`tracy_idol5`](./NPC_Scripts.md#context-tracy_idol5) | Block | Examples: `{ ... }` | 1 |
| [`tracy_idol6`](./NPC_Scripts.md#context-tracy_idol6) | Block | Examples: `{ ... }` | 1 |
| [`tracy_idol7`](./NPC_Scripts.md#context-tracy_idol7) | Block | Examples: `{ ... }` | 1 |
| [`tracy_introduction`](./NPC_Scripts.md#context-tracy_introduction) | Block | Examples: `{ ... }` | 1 |
| [`tracy_kaijufight`](./NPC_Scripts.md#context-tracy_kaijufight) | Block | Examples: `{ ... }` | 1 |
| [`tracy_max1`](./NPC_Scripts.md#context-tracy_max1) | Block | Examples: `{ ... }` | 1 |
| [`tracy_max2`](./NPC_Scripts.md#context-tracy_max2) | Block | Examples: `{ ... }` | 1 |
| [`tracy_max3`](./NPC_Scripts.md#context-tracy_max3) | Block | Examples: `{ ... }` | 1 |
| [`tracy_max4`](./NPC_Scripts.md#context-tracy_max4) | Block | Examples: `{ ... }` | 1 |
| [`tracy_max5`](./NPC_Scripts.md#context-tracy_max5) | Block | Examples: `{ ... }` | 1 |
| [`tracy_max_intro`](./NPC_Scripts.md#context-tracy_max_intro) | Block | Examples: `{ ... }` | 1 |
| [`tracy_max_repeating`](./NPC_Scripts.md#context-tracy_max_repeating) | Block | Examples: `{ ... }` | 1 |
| [`try_again_attack_rat`](./NPC_Scripts.md#context-try_again_attack_rat) | Block | Examples: `{ ... }` | 1 |
| [`try_again_melee_move`](./NPC_Scripts.md#context-try_again_melee_move) | Block | Examples: `{ ... }` | 1 |
| [`tutorial_cat_dies`](./NPC_Scripts.md#context-tutorial_cat_dies) | Block | Examples: `{ ... }` | 1 |
| [`unprompted1`](./NPC_Scripts.md#context-unprompted1) | Block | Examples: `{ ... }` | 1 |
| [`unprompted2`](./NPC_Scripts.md#context-unprompted2) | Block | Examples: `{ ... }` | 1 |
| [`unprompted3`](./NPC_Scripts.md#context-unprompted3) | Block | Examples: `{ ... }` | 1 |
| [`unprompted4`](./NPC_Scripts.md#context-unprompted4) | Block | Examples: `{ ... }` | 1 |
| [`unprompted5`](./NPC_Scripts.md#context-unprompted5) | Block | Examples: `{ ... }` | 1 |
| [`unprompted6`](./NPC_Scripts.md#context-unprompted6) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_1`](./NPC_Scripts.md#context-upgrade_storage_1) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_2`](./NPC_Scripts.md#context-upgrade_storage_2) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_3`](./NPC_Scripts.md#context-upgrade_storage_3) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_4`](./NPC_Scripts.md#context-upgrade_storage_4) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_5`](./NPC_Scripts.md#context-upgrade_storage_5) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_6`](./NPC_Scripts.md#context-upgrade_storage_6) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_7`](./NPC_Scripts.md#context-upgrade_storage_7) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_max1`](./NPC_Scripts.md#context-upgrade_storage_max1) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_max2`](./NPC_Scripts.md#context-upgrade_storage_max2) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_max3`](./NPC_Scripts.md#context-upgrade_storage_max3) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_max4`](./NPC_Scripts.md#context-upgrade_storage_max4) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_max5`](./NPC_Scripts.md#context-upgrade_storage_max5) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_repeating_crazy`](./NPC_Scripts.md#context-upgrade_storage_repeating_crazy) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_repeating_hard`](./NPC_Scripts.md#context-upgrade_storage_repeating_hard) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_repeating_impossible`](./NPC_Scripts.md#context-upgrade_storage_repeating_impossible) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_repeating_intro`](./NPC_Scripts.md#context-upgrade_storage_repeating_intro) | Block | Examples: `{ ... }` | 1 |
| [`upgrade_storage_repeating_normal`](./NPC_Scripts.md#context-upgrade_storage_repeating_normal) | Block | Examples: `{ ... }` | 1 |
| [`use_attack_after_used_weapon`](./NPC_Scripts.md#context-use_attack_after_used_weapon) | Block | Examples: `{ ... }` | 1 |
| [`use_weapon`](./NPC_Scripts.md#context-use_weapon) | Block | Examples: `{ ... }` | 1 |
| [`welcome`](./NPC_Scripts.md#context-welcome) | Block | Examples: `{ ... }` | 1 |
| [`welcome_boneyard`](./NPC_Scripts.md#context-welcome_boneyard) | Block | Examples: `{ ... }` | 1 |
| [`welcome_bunker`](./NPC_Scripts.md#context-welcome_bunker) | Block | Examples: `{ ... }` | 1 |
| [`welcome_caves`](./NPC_Scripts.md#context-welcome_caves) | Block | Examples: `{ ... }` | 1 |
| [`welcome_core`](./NPC_Scripts.md#context-welcome_core) | Block | Examples: `{ ... }` | 1 |
| [`welcome_crater`](./NPC_Scripts.md#context-welcome_crater) | Block | Examples: `{ ... }` | 1 |
| [`welcome_desert`](./NPC_Scripts.md#context-welcome_desert) | Block | Examples: `{ ... }` | 1 |
| [`welcome_future`](./NPC_Scripts.md#context-welcome_future) | Block | Examples: `{ ... }` | 1 |
| [`welcome_iceage`](./NPC_Scripts.md#context-welcome_iceage) | Block | Examples: `{ ... }` | 1 |
| [`welcome_junkyard`](./NPC_Scripts.md#context-welcome_junkyard) | Block | Examples: `{ ... }` | 1 |
| [`welcome_jurassic`](./NPC_Scripts.md#context-welcome_jurassic) | Block | Examples: `{ ... }` | 1 |
| [`welcome_lab`](./NPC_Scripts.md#context-welcome_lab) | Block | Examples: `{ ... }` | 1 |
| [`welcome_moon`](./NPC_Scripts.md#context-welcome_moon) | Block | Examples: `{ ... }` | 1 |
| [`welcome_sewers`](./NPC_Scripts.md#context-welcome_sewers) | Block | Examples: `{ ... }` | 1 |
| [`welcome_theend`](./NPC_Scripts.md#context-welcome_theend) | Block | Examples: `{ ... }` | 1 |
| [`welcome_water`](./NPC_Scripts.md#context-welcome_water) | Block | Examples: `{ ... }` | 1 |
| [`welcome_water_cheap`](./NPC_Scripts.md#context-welcome_water_cheap) | Block | Examples: `{ ... }` | 1 |

</details>

---

### Context: `states`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
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

### Context: `transitions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
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

### Context: `unprompted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ unprompted_a unprompted_b unprompted_c unprompted_d unp..., [ unprompted1 u...` | 5 |
| `cancelable` | Boolean | Examples: `true` | 3 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_JACK_UNPROMPTED_1, NPC_ORGANGRINDER_UNPROMPTED_1, NPC_TRACY_UNPROMPTED_2` | 3 |
| `wait_for_cancel` | Number | Examples: `1` | 3 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_UNPROMPTED_1, NPC_TRACY_UNPROMPTED_1` | 2 |

</details>

---

### Context: `also`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_ALSO_1, NPC_BEANIES_ALSO_1, NPC_BUTCH_ALSO_1` | 8 |

</details>

---

### Context: `unknown`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNKNOWN_1, NPC_FRANK_UNKNOWN_1, NPC_BEANIES_UNKNOWN_1` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 6 |
| `lock_controls` | Number | Examples: `1` | 3 |
| `unlock_controls` | Number | Examples: `1` | 3 |

</details>

---

### Context: `hide_text`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 4 |
| [`dialog_and_autopass`](./Strings.md#string-dialog_and_autopass) | String | Examples: `""` | 4 |

</details>

---

### Context: `purchase_item`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 3 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_PURCHASE_ITEM_1, NPC_ORGANGRINDER_PURCHASE_ITEM_1, NPC_JACK_PURCHAS...` | 3 |
| `wait_for_cancel` | Number | Examples: `1` | 3 |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ purchase_item_a purchase_item_b purchase_item_c purchas...` | 1 |

</details>

---

### Context: `tooltip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 4 |
| [`tooltip_dialog`](./Enums.md#enum-tooltip_dialog) | Enum | Examples: `NPC_TRACY_SHOP_TOOLTIP, NPC_ORGANGRINDER_SHOP_TOOLTIP, NPC_JACK_SHOP_TOOLTIP` | 4 |
| `wait_for_cancel` | Number | Examples: `1` | 4 |

</details>

---

### Context: `unprompted_a`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_A_1, NPC_FRANK_UNPROMPTED_A_2, NPC_BUTCH_UNPROMPTED_A_1` | 8 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 |

</details>

---

### Context: `unprompted_b`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_B_1, NPC_FRANK_UNPROMPTED_B_1, NPC_FRANK_UNPROMPTED_B_2` | 6 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 |

</details>

---

### Context: `unprompted_c`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_C_1, NPC_FRANK_UNPROMPTED_C_2, NPC_BUTCH_UNPROMPTED_C_1` | 5 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 |

</details>

---

### Context: `unprompted_d`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_D_1, NPC_BUTCH_UNPROMPTED_D_1, NPC_FRANK_UNPROMPTED_D_2` | 7 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 |

</details>

---

### Context: `unprompted_e`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_E_1, NPC_BUTCH_UNPROMPTED_E_1, NPC_FRANK_UNPROMPTED_E_2` | 6 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 |

</details>

---

### Context: `unprompted_f`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_F_1, NPC_FRANK_UNPROMPTED_F_2, NPC_FRANK_UNPROMPTED_F_1` | 7 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 |

</details>

---

### Context: `unprompted_g`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_G_2, NPC_BUTCH_UNPROMPTED_G_1, NPC_FRANK_UNPROMPTED_G_1` | 8 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 |

</details>

---

### Context: `unprompted_h`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UNPROMPTED_H_1, NPC_FRANK_UNPROMPTED_H_2, NPC_FRANK_UNPROMPTED_H_1` | 9 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 |

</details>

---

### Context: `unprompted_i`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_UNPROMPTED_I_2, NPC_BUTCH_UNPROMPTED_I_1, NPC_FRANK_UNPROMPTED_I_1` | 8 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `forward_to_tips` | 3 |

</details>

---

### Context: `cant_afford`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_CANT_AFFORD_1, NPC_JACK_CANT_AFFORD_1` | 2 |
| `wait_for_cancel` | Number | Examples: `1` | 2 |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ cant_afford_a cant_afford_b cant_afford_c cant_afford_d ]` | 1 |

</details>

---

### Context: `forward_to_tips`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ butch_tips_intelligence butch_tips_charisma butch_tips_..., [ frank_tips_1 ...` | 3 |

</details>

---

### Context: `out_of_stock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_OUT_OF_STOCK_1, NPC_JACK_OUT_OF_STOCK_1, NPC_TRACY_OUT_OF_ST...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `blocking` | 3 |

</details>

---

### Context: `Jack_Gainaltfurniture`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_GAINALTFURNITURE_3, NPC_JACK_JACK_GAINALTFURNITURE_1, NPC_JACK_...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 4 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `beanies_begin_accepting_cats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_2, NPC_BEANIES_BEANIES_BEGIN_ACCEPTI...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `beanies` | 1 |

</details>

---

### Context: `beanies_bombquest_2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_2_2, NPC_BEANIES_BEANIES_BOMBQUEST_2_1, NPC_BEA...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |

</details>

---

### Context: `beanies_bombquest_3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_3_1, NPC_BEANIES_BEANIES_BOMBQUEST_3_2, NPC_BEA...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 3 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `nuke_quest_get_nuke` | 1 |

</details>

---

### Context: `beanies_bombquest_amnesia`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_1, NPC_BEANIES_BEANIES_BOMBQUEST_AMNESI...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `nuke_quest_loop` | 1 |

</details>

---

### Context: `beanies_bombquest_begin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_2, NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_1,...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 7 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 |

</details>

---

### Context: `beanies_bombquest_fail_jarofblood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_3, NPC_BEANIES_BEANIES_BOMBQUES...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 |

</details>

---

### Context: `beanies_bombquest_fail_jarofchaos`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_3, NPC_BEANIES_BEANIES_BOMBQUES...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 |

</details>

---

### Context: `beanies_bombquest_fail_jarofradiation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_1, NPC_BEANIES_BEANIES_BOMB...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 |

</details>

---

### Context: `beanies_bombquest_fail_nuke`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_3, NPC_BEANIES_BEANIES_BOMBQUEST_FAIL...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 7 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `reset_nuke_quest` | 1 |

</details>

---

### Context: `beanies_future_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_FUTURE_INTRO_2, NPC_BEANIES_BEANIES_FUTURE_INTRO_3, NPC_B...` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 5 |

</details>

---

### Context: `beanies_hitler3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_HITLER3_2, NPC_BEANIES_BEANIES_HITLER3_1, NPC_BEANIES_BEA...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |

</details>

---

### Context: `beanies_hitler3_defeat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_2, NPC_BEANIES_BEANIES_HITLER3_DEFEAT_1, N...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 7 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `quest_begin_amplifier2` | 1 |

</details>

---

### Context: `beanies_iloveyou`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_ILOVEYOU_2, NPC_BEANIES_BEANIES_ILOVEYOU_3, NPC_BEANIES_B...` | 3 |

</details>

---

### Context: `beanies_infinite_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_INFINITE_INTRO_3, NPC_POPUP_BEANIES_INFINITE_INTRO_2, NPC_P...` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.25` | 1 |

</details>

---

### Context: `beanies_jurassic_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_JURASSIC_INTRO_1, NPC_BEANIES_BEANIES_JURASSIC_INTRO_2, N...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |

</details>

---

### Context: `beanies_lab_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_LAB_INTRO_1, NPC_BEANIES_BEANIES_LAB_INTRO_3, NPC_BEANIES...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 11 |
| [`play_cutscene`](./Enums.md#enum-play_cutscene) | Enum | Examples: `credits_1` | 1 |
| `restart_npc_music` | Number | Examples: `1` | 1 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `song_unlock_get_in_the_cage` | 1 |

</details>

---

### Context: `beanies_quest_complete`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_complete` | 1 |
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `success` | 1 |

</details>

---

### Context: `beanies_quest_fail`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_fail` | 1 |
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `fail` | 1 |

</details>

---

### Context: `beanies_quests_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_QUESTS_INTRO_3, NPC_BEANIES_BEANIES_QUESTS_INTRO_1, NPC_B...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_intro` | 1 |
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `newest` | 1 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `beanies_quests_repeat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_QUESTS_REPEAT_1, NPC_BEANIES_BEANIES_QUESTS_REPEAT_3, NPC...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`do_sidequest_sequence`](./Enums.md#enum-do_sidequest_sequence) | Enum | Examples: `beaniesquest_intro` | 1 |
| [`gather_questitem_info`](./Enums.md#enum-gather_questitem_info) | Enum | Examples: `newest` | 1 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `beanies_rift_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_RIFT_INTRO_1, NPC_POPUP_BEANIES_RIFT_INTRO_2, NPC_POPUP_BEA...` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.25` | 1 |

</details>

---

### Context: `beanies_screenshake_test`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_1, NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_...` | 7 |
| [`screenshake`](./Arrays.md#array-screenshake) | Array | Examples: `[ .5 10 ]` | 1 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `PickupCoin` | 1 |

</details>

---

### Context: `beanies_seefuture`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_SEEFUTURE_3, NPC_BEANIES_BEANIES_SEEFUTURE_2, NPC_BEANIES...` | 15 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 9 |

</details>

---

### Context: `beanies_seetheend`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_SEETHEEND_1, NPC_BEANIES_BEANIES_SEETHEEND_2, NPC_BEANIES...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |

</details>

---

### Context: `beanies_terminator1_defeat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_1, NPC_BEANIES_BEANIES_TERMINATOR1_DEF...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `quest_begin_receiver2` | 1 |

</details>

---

### Context: `beanies_terminator2_defeat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_3, NPC_BEANIES_BEANIES_TERMINATOR2_DEF...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `quest_begin_transmitter2` | 1 |

</details>

---

### Context: `beanies_theend_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_THEEND_INTRO_3, NPC_BEANIES_BEANIES_THEEND_INTRO_2, NPC_B...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 2 |

</details>

---

### Context: `beanies_timemachine_2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TIMEMACHINE_2_2, NPC_BEANIES_BEANIES_TIMEMACHINE_2_3, NPC...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 9 |

</details>

---

### Context: `beanies_timemachine_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_2, NPC_BEANIES_BEANIES_TIMEMACHINE_INTR...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`trigger_unlock`](./Enums.md#enum-trigger_unlock) | Enum | Examples: `time_machine_quest_begin` | 1 |

</details>

---

### Context: `beanies_vscreator1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR1_1, NPC_POPUP_BEANIES_VSCREATOR1_3, NPC_POPUP_BEA...` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 2 |

</details>

---

### Context: `beanies_vscreator2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR2_1, NPC_POPUP_BEANIES_VSCREATOR2_3, NPC_POPUP_BEA...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 2 |

</details>

---

### Context: `beanies_vscreator3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR3_2, NPC_POPUP_BEANIES_VSCREATOR3_3, NPC_POPUP_BEA...` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_intensestatic` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 2 |

</details>

---

### Context: `beanies_vscreator4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATOR4_2, NPC_POPUP_BEANIES_VSCREATOR4_3, NPC_POPUP_BEA...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_intensestatic` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 2 |
| [`force_current_cat_use_ability`](./Enums.md#enum-force_current_cat_use_ability) | Enum | Examples: `neck_NukeBonus_remote` | 1 |

</details>

---

### Context: `beanies_vscreatorintro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BEANIES_VSCREATORINTRO_1, NPC_POPUP_BEANIES_VSCREATORINTRO_2, NPC_P...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, beanies_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_BeaniesAppear, UISFX_BeaniesAway` | 2 |

</details>

---

### Context: `beaniesquest_complete_AI`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_3, NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_AirHorn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_AngryFace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_1, NPC_BEANIES_BEANIESQUEST_COMPL...` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 |

</details>

---

### Context: `beaniesquest_complete_AnimalHands`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_2, NPC_BEANIES_BEANIESQUEST_COM...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_BubbleBoy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_3, NPC_BEANIES_BEANIESQUEST_COMPL...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_ChadImplant`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_2, NPC_BEANIES_BEANIESQUEST_COM...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_ChaosDevice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHAOSDEVICE_1, NPC_BEANIES_BEANIESQUEST_COM...` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 |

</details>

---

### Context: `beaniesquest_complete_DimensionalDivider`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_2, NPC_BEANIES_BEANIESQU...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_DiseaseJar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_1, NPC_BEANIES_BEANIESQUEST_COMP...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_ExperimentalTreatment`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_3, NPC_BEANIES_BEANIE...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_FartFace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_3, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_FigLeaf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_3, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_Generic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_GENERIC_2, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_GlassCannon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_1, NPC_BEANIES_BEANIESQUEST_COM...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_HardPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_1, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_HiveMind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_2, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_MagicMirror`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_2, NPC_BEANIES_BEANIESQUEST_COM...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_MeStone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_3, NPC_BEANIES_BEANIESQUEST_COMPLET...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_MultilinkCable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_2, NPC_BEANIES_BEANIESQUEST_...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_MysteriousDice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_3, NPC_BEANIES_BEANIESQUEST_...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_MysteriousGlasses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_1, NPC_BEANIES_BEANIESQUE...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_NDEDevice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_1, NPC_BEANIES_BEANIESQUEST_COMPL...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_NuclearKnife`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_2, NPC_BEANIES_BEANIESQUEST_CO...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_PartialLobotomy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_1, NPC_BEANIES_BEANIESQUEST...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_PartyDetonator`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_2, NPC_BEANIES_BEANIESQUEST_...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_PersonalHeater`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_3, NPC_BEANIES_BEANIESQUEST_...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_PersuasionDevice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_1, NPC_BEANIES_BEANIESQUES...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_PrincessHat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_1, NPC_BEANIES_BEANIESQUEST_COM...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_RealityScrambler`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_1, NPC_BEANIES_BEANIESQUES...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_Redacted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_2, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_SpiderInjector`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_1, NPC_BEANIES_BEANIESQUEST_...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_Stopwatch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_1, NPC_BEANIES_BEANIESQUEST_COMPL...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_StorageLocker`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_3, NPC_BEANIES_BEANIESQUEST_C...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_TheIOU`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_1, NPC_BEANIES_BEANIESQUEST_COMPLETE...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_TheLoner`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_2, NPC_BEANIES_BEANIESQUEST_COMPLE...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_complete_Trapfest99`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_2, NPC_BEANIES_BEANIESQUEST_COMP...` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 |

</details>

---

### Context: `beaniesquest_complete_UltraVision3000`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_1, NPC_BEANIES_BEANIESQUEST...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_reward` | 1 |

</details>

---

### Context: `beaniesquest_fail_AI`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_AI_3, NPC_BEANIES_BEANIESQUEST_FAIL_AI_2, NPC_B...` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_AirHorn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_1, NPC_BEANIES_BEANIESQUEST_FAIL_AIRHOR...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_AngryFace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_2, NPC_BEANIES_BEANIESQUEST_FAIL_ANGR...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_AnimalHands`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_ANIMALHANDS_1, NPC_BEANIES_BEANIESQUEST_FAIL_AN...` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_BubbleBoy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_2, NPC_BEANIES_BEANIESQUEST_FAIL_BUBB...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_ChadImplant`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_3, NPC_BEANIES_BEANIESQUEST_FAIL_CH...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_ChaosDevice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_1, NPC_BEANIES_BEANIESQUEST_FAIL_CH...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_DimensionalDivider`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_3, NPC_BEANIES_BEANIESQUEST_...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_DiseaseJar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_3, NPC_BEANIES_BEANIESQUEST_FAIL_DIS...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_ExperimentalTreatment`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_3, NPC_BEANIES_BEANIESQUE...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_FartFace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_2, NPC_BEANIES_BEANIESQUEST_FAIL_FARTF...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_FigLeaf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_1, NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEA...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_Generic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_GENERIC_1, NPC_BEANIES_BEANIESQUEST_FAIL_GENERI...` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_GlassCannon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_1, NPC_BEANIES_BEANIESQUEST_FAIL_GL...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_HardPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_1, NPC_BEANIES_BEANIESQUEST_FAIL_HARDP...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_HiveMind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_2, NPC_BEANIES_BEANIESQUEST_FAIL_HIVEM...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_MagicMirror`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_3, NPC_BEANIES_BEANIESQUEST_FAIL_MA...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_MeStone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MESTONE_2, NPC_BEANIES_BEANIESQUEST_FAIL_MESTON...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_MultilinkCable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MULTILINKCABLE_2, NPC_BEANIES_BEANIESQUEST_FAIL...` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 |

</details>

---

### Context: `beaniesquest_fail_MysteriousDice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_2, NPC_BEANIES_BEANIESQUEST_FAIL...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_MysteriousGlasses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSGLASSES_3, NPC_BEANIES_BEANIESQUEST_F...` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 |

</details>

---

### Context: `beaniesquest_fail_NDEDevice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_2, NPC_BEANIES_BEANIESQUEST_FAIL_NDED...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_NuclearKnife`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_3, NPC_BEANIES_BEANIESQUEST_FAIL_N...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_PartialLobotomy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_1, NPC_BEANIES_BEANIESQUEST_FAI...` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 |

</details>

---

### Context: `beaniesquest_fail_PartyDetonator`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_1, NPC_BEANIES_BEANIESQUEST_FAIL...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_PersonalHeater`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_3, NPC_BEANIES_BEANIESQUEST_FAIL...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_PersuasionDevice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_1, NPC_BEANIES_BEANIESQUEST_FA...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_PrincessHat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_1, NPC_BEANIES_BEANIESQUEST_FAIL_PR...` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 |

</details>

---

### Context: `beaniesquest_fail_RealityScrambler`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_1, NPC_BEANIES_BEANIESQUEST_FA...` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 |

</details>

---

### Context: `beaniesquest_fail_Redacted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_1, NPC_BEANIES_BEANIESQUEST_FAIL_REDAC...` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 |

</details>

---

### Context: `beaniesquest_fail_SpiderInjector`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_2, NPC_BEANIES_BEANIESQUEST_FAIL...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_Stopwatch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_2, NPC_BEANIES_BEANIESQUEST_FAIL_STOP...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_StorageLocker`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_3, NPC_BEANIES_BEANIESQUEST_FAIL_...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_TheIOU`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_1, NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_TheLoner`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_3, NPC_BEANIES_BEANIESQUEST_FAIL_THELO...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_Trapfest99`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_2, NPC_BEANIES_BEANIESQUEST_FAIL_TRA...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `set_state, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_fail_UltraVision3000`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_3, NPC_BEANIES_BEANIESQUEST_FAI...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `sidequest_fail` | 1 |

</details>

---

### Context: `beaniesquest_intro_AI`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_AI_1, NPC_BEANIES_BEANIESQUEST_INTRO_AI_2, NPC...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |

</details>

---

### Context: `beaniesquest_intro_AirHorn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_2, NPC_BEANIES_BEANIESQUEST_INTRO_AIRH...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |

</details>

---

### Context: `beaniesquest_intro_AngryFace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_2, NPC_BEANIES_BEANIESQUEST_INTRO_AN...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |

</details>

---

### Context: `beaniesquest_intro_AnimalHands`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_1, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |

</details>

---

### Context: `beaniesquest_intro_BubbleBoy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_1, NPC_BEANIES_BEANIESQUEST_INTRO_BU...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |

</details>

---

### Context: `beaniesquest_intro_ChadImplant`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_1, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |

</details>

---

### Context: `beaniesquest_intro_ChaosDevice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_3, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |

</details>

---

### Context: `beaniesquest_intro_DimensionalDivider`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_1, NPC_BEANIES_BEANIESQUEST...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |

</details>

---

### Context: `beaniesquest_intro_DiseaseJar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_1, NPC_BEANIES_BEANIESQUEST_INTRO_D...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle` | 1 |

</details>

---

### Context: `beaniesquest_intro_ExperimentalTreatment`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_2, NPC_BEANIES_BEANIESQU...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 3 |

</details>

---

### Context: `beaniesquest_intro_FartFace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_1, NPC_BEANIES_BEANIESQUEST_INTRO_FAR...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |

</details>

---

### Context: `beaniesquest_intro_FigLeaf`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_1, NPC_BEANIES_BEANIESQUEST_INTRO_FIGL...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |

</details>

---

### Context: `beaniesquest_intro_Generic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_GENERIC_1, NPC_BEANIES_BEANIESQUEST_INTRO_GENE...` | 3 |

</details>

---

### Context: `beaniesquest_intro_GlassCannon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_2, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 |

</details>

---

### Context: `beaniesquest_intro_HardPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_2, NPC_BEANIES_BEANIESQUEST_INTRO_HAR...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |

</details>

---

### Context: `beaniesquest_intro_HiveMind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_1, NPC_BEANIES_BEANIESQUEST_INTRO_HIV...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |

</details>

---

### Context: `beaniesquest_intro_MagicMirror`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_3, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |

</details>

---

### Context: `beaniesquest_intro_MeStone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_1, NPC_BEANIES_BEANIESQUEST_INTRO_MEST...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 2 |

</details>

---

### Context: `beaniesquest_intro_MultilinkCable`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_2, NPC_BEANIES_BEANIESQUEST_INT...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Context: `beaniesquest_intro_MysteriousDice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_3, NPC_BEANIES_BEANIESQUEST_INT...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |

</details>

---

### Context: `beaniesquest_intro_MysteriousGlasses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_1, NPC_BEANIES_BEANIESQUEST_...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |

</details>

---

### Context: `beaniesquest_intro_NDEDevice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_2, NPC_BEANIES_BEANIESQUEST_INTRO_ND...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |

</details>

---

### Context: `beaniesquest_intro_NuclearKnife`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_3, NPC_BEANIES_BEANIESQUEST_INTRO...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |

</details>

---

### Context: `beaniesquest_intro_PartialLobotomy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_3, NPC_BEANIES_BEANIESQUEST_IN...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |

</details>

---

### Context: `beaniesquest_intro_PartyDetonator`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_1, NPC_BEANIES_BEANIESQUEST_INT...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |

</details>

---

### Context: `beaniesquest_intro_PersonalHeater`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_3, NPC_BEANIES_BEANIESQUEST_INT...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |

</details>

---

### Context: `beaniesquest_intro_PersuasionDevice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_3, NPC_BEANIES_BEANIESQUEST_I...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 5 |

</details>

---

### Context: `beaniesquest_intro_PrincessHat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_2, NPC_BEANIES_BEANIESQUEST_INTRO_...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |

</details>

---

### Context: `beaniesquest_intro_RealityScrambler`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_3, NPC_BEANIES_BEANIESQUEST_I...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 |

</details>

---

### Context: `beaniesquest_intro_Redacted`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_2, NPC_BEANIES_BEANIESQUEST_INTRO_RED...` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |

</details>

---

### Context: `beaniesquest_intro_SpiderInjector`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_2, NPC_BEANIES_BEANIESQUEST_INT...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Context: `beaniesquest_intro_Stopwatch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_2, NPC_BEANIES_BEANIESQUEST_INTRO_ST...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |

</details>

---

### Context: `beaniesquest_intro_StorageLocker`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_2, NPC_BEANIES_BEANIESQUEST_INTR...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |

</details>

---

### Context: `beaniesquest_intro_TheIOU`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_3, NPC_BEANIES_BEANIESQUEST_INTRO_THEIO...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 6 |

</details>

---

### Context: `beaniesquest_intro_TheLoner`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_2, NPC_BEANIES_BEANIESQUEST_INTRO_THE...` | 4 |

</details>

---

### Context: `beaniesquest_intro_Trapfest99`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_2, NPC_BEANIES_BEANIESQUEST_INTRO_T...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 3 |

</details>

---

### Context: `beaniesquest_intro_UltraVision3000`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_1, NPC_BEANIES_BEANIESQUEST_IN...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 7 |

</details>

---

### Context: `boss_fight_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BOSS_FIGHT_INTRO_2, NPC_POPUP_BOSS_FIGHT_INTRO_1, NPC_POPUP_BOSS_FI...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 4 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.25, .5` | 2 |

</details>

---

### Context: `boss_fight_round2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_BOSS_FIGHT_ROUND2_1, NPC_POPUP_BOSS_FIGHT_ROUND2_3, NPC_POPUP_BOSS_...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_turnorder, offscreen, butch_right` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 3 |

</details>

---

### Context: `butch_begin_accepting_cats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_3, NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `butch` | 1 |

</details>

---

### Context: `butch_boneyard_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_BONEYARD_INTRO_3, NPC_BUTCH_BUTCH_BONEYARD_INTRO_1, NPC_BUTCH...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 7 |

</details>

---

### Context: `butch_first_house_boss_beat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_2, NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEA...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |

</details>

---

### Context: `butch_pyro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_PYRO_2, NPC_BUTCH_BUTCH_PYRO_1, NPC_BUTCH_BUTCH_PYRO_3` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 4 |

</details>

---

### Context: `butch_tina1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TINA1_3, NPC_BUTCH_BUTCH_TINA1_2, NPC_BUTCH_BUTCH_TINA1_1` | 14 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |

</details>

---

### Context: `butch_tips_backstab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_BACKSTAB_1, NPC_BUTCH_BUTCH_TIPS_BACKSTAB_3, NPC_BUTCH_B...` | 3 |

</details>

---

### Context: `butch_tips_charisma`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_CHARISMA_1, NPC_BUTCH_BUTCH_TIPS_CHARISMA_2, NPC_BUTCH_B...` | 3 |

</details>

---

### Context: `butch_tips_combat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_COMBAT_1, NPC_BUTCH_BUTCH_TIPS_COMBAT_2, NPC_BUTCH_BUTCH...` | 4 |

</details>

---

### Context: `butch_tips_disorders`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_DISORDERS_3, NPC_BUTCH_BUTCH_TIPS_DISORDERS_2, NPC_BUTCH...` | 3 |

</details>

---

### Context: `butch_tips_drafting`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_DRAFTING_2, NPC_BUTCH_BUTCH_TIPS_DRAFTING_3, NPC_BUTCH_B...` | 3 |

</details>

---

### Context: `butch_tips_elements`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_ELEMENTS_1, NPC_BUTCH_BUTCH_TIPS_ELEMENTS_2, NPC_BUTCH_B...` | 5 |

</details>

---

### Context: `butch_tips_hard`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_HARD_3, NPC_BUTCH_BUTCH_TIPS_HARD_1, NPC_BUTCH_BUTCH_TIP...` | 5 |

</details>

---

### Context: `butch_tips_headhome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_HEADHOME_2, NPC_BUTCH_BUTCH_TIPS_HEADHOME_1, NPC_BUTCH_B...` | 4 |

</details>

---

### Context: `butch_tips_houseboss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_3, NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_1, NPC_BUTCH...` | 3 |

</details>

---

### Context: `butch_tips_info`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_INFO_2, NPC_BUTCH_BUTCH_TIPS_INFO_1` | 2 |

</details>

---

### Context: `butch_tips_intelligence`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_2, NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_3, NPC...` | 4 |

</details>

---

### Context: `butch_tips_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_INTRO_1, NPC_BUTCH_BUTCH_TIPS_INTRO_3, NPC_BUTCH_BUTCH_T...` | 4 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `butch_tips_intelligence` | 1 |

</details>

---

### Context: `butch_tips_items`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_ITEMS_1, NPC_BUTCH_BUTCH_TIPS_ITEMS_2` | 2 |

</details>

---

### Context: `butch_tips_lesscats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_LESSCATS_2, NPC_BUTCH_BUTCH_TIPS_LESSCATS_1, NPC_BUTCH_B...` | 3 |

</details>

---

### Context: `butch_tips_magicdamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_2, NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_1, NPC_B...` | 4 |

</details>

---

### Context: `butch_tips_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_PASSIVES_1, NPC_BUTCH_BUTCH_TIPS_PASSIVES_3, NPC_BUTCH_B...` | 3 |

</details>

---

### Context: `butch_tips_reorient`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_REORIENT_2, NPC_BUTCH_BUTCH_TIPS_REORIENT_1, NPC_BUTCH_B...` | 5 |

</details>

---

### Context: `butch_tips_rewards`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_REWARDS_3, NPC_BUTCH_BUTCH_TIPS_REWARDS_2, NPC_BUTCH_BUT...` | 4 |

</details>

---

### Context: `butch_tips_tacticalview`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_1, NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_2, NPC...` | 3 |

</details>

---

### Context: `butch_tips_turnorder`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_TURNORDER_3, NPC_BUTCH_BUTCH_TIPS_TURNORDER_1, NPC_BUTCH...` | 3 |

</details>

---

### Context: `butch_tips_wellrounded`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_3, NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_2, NPC_B...` | 5 |

</details>

---

### Context: `can_still_use_attack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 3 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_1, NPC_POPUP_CAN_STILL_USE_ATTACK_2` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_3` | 1 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `can_still_use_attack_didntspell` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `can_still_use_attack_didntspell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 3 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_2` | 1 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `can_still_use_attack` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `cant_afford_a`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_A_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `cant_afford_b`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_B_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `cant_afford_c`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_C_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `cant_afford_d`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_D_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `cant_afford_iceage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_ICEAGE_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `cant_afford_jurassic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_JURASSIC_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `cant_afford_moon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_MOON_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `cant_afford_theend`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_CANT_AFFORD_THEEND_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `class_unlock_butcher`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_2, NPC_BUTCH_CLASS_UNLOCK_BUTCHER_3, NPC_BUTCH...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Butcher` | 1 |

</details>

---

### Context: `class_unlock_druid`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_DRUID_1, NPC_BUTCH_CLASS_UNLOCK_DRUID_3, NPC_BUTCH_CLA...` | 4 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Druid` | 1 |

</details>

---

### Context: `class_unlock_jester`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_JESTER_1, NPC_BUTCH_CLASS_UNLOCK_JESTER_3, NPC_BUTCH_C...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 3 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Jester` | 1 |

</details>

---

### Context: `class_unlock_medic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_MEDIC_2, NPC_BUTCH_CLASS_UNLOCK_MEDIC_1, NPC_BUTCH_CLA...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 3 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Medic` | 1 |

</details>

---

### Context: `class_unlock_monk`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_MONK_3, NPC_BUTCH_CLASS_UNLOCK_MONK_1, NPC_BUTCH_CLASS...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Monk` | 1 |

</details>

---

### Context: `class_unlock_necromancer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_3, NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_2, N...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Necromancer` | 1 |

</details>

---

### Context: `class_unlock_psychic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_3, NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_2, NPC_BUTCH...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Psychic` | 1 |

</details>

---

### Context: `class_unlock_thief`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_THIEF_2, NPC_BUTCH_CLASS_UNLOCK_THIEF_1, NPC_BUTCH_CLA...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Thief` | 1 |

</details>

---

### Context: `class_unlock_tinkerer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_CLASS_UNLOCK_TINKERER_3, NPC_BUTCH_CLASS_UNLOCK_TINKERER_1, NPC_BUT...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`unlock_class`](./Enums.md#enum-unlock_class) | Enum | Examples: `Tinkerer` | 1 |

</details>

---

### Context: `collected_new_items`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_3, NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle2, blocking` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_5` | 1 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `collected_nothing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_COLLECTED_NOTHING_1, NPC_ORGANGRINDER_COLLECTED_NOTHING_3, N...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle2, blocking` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `do_not_end_turn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `do_not_end_turn` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_DO_NOT_END_TURN_1` | 1 |

</details>

---

### Context: `done_spitting_fail_ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_FAIL_ALLY_2, NPC_POPUP_DONE_SPITTING_FAIL_ALLY_3, NPC...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `done_spitting_fail_miss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_FAIL_MISS_1, NPC_POPUP_DONE_SPITTING_FAIL_MISS_2` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `done_spitting_fail_rat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_FAIL_RAT_1, NPC_POPUP_DONE_SPITTING_FAIL_RAT_2` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway` | 1 |

</details>

---

### Context: `done_spitting_success`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_DONE_SPITTING_SUCCESS_2, NPC_POPUP_DONE_SPITTING_SUCCESS_3, NPC_POP...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ending`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_ENDING_1, NPC_BEANIES_ENDING_2, NPC_BEANIES_ENDING_3` | 19 |
| [`screenshake`](./Arrays.md#array-screenshake) | Array | Examples: `[ 1 30 ]` | 1 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `BeaniesEnding_Banging` | 1 |

</details>

---

### Context: `finish_adventure`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FINISH_ADVENTURE_1, NPC_POPUP_FINISH_ADVENTURE_2, NPC_POPUP_FINISH_...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, butch_point_food, butch_point_save` | 5 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 5 |

</details>

---

### Context: `first_fight_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FIRST_FIGHT_INTRO_3, NPC_POPUP_FIRST_FIGHT_INTRO_2, NPC_POPUP_FIRST...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_team, butch_point_enemies` | 8 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveHint, UISFX_ButchHint, UISFX_ButchMove` | 6 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected, cat_turn` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_FIRST_FIGHT_INTRO_14` | 1 |
| [`set_mood`](./Enums.md#enum-set_mood) | Enum | Examples: `default` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `first_house_boss_tomorrow`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_3, NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_1,...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `first_house_hint_retired`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_2, NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_3, N...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `frank_caves_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_CAVES_INTRO_1, NPC_FRANK_FRANK_CAVES_INTRO_2, NPC_FRANK_FRANK...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup` | 5 |

</details>

---

### Context: `frank_ending`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_ENDING_1, NPC_FRANK_FRANK_ENDING_2, NPC_FRANK_FRANK_ENDING_3` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 8 |

</details>

---

### Context: `frank_max1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX1_2, NPC_FRANK_FRANK_MAX1_3, NPC_FRANK_FRANK_MAX1_1` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `frank_max2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX2_1, NPC_FRANK_FRANK_MAX2_3, NPC_FRANK_FRANK_MAX2_2` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `frank_max3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX3_3, NPC_FRANK_FRANK_MAX3_2, NPC_FRANK_FRANK_MAX3_1` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `frank_max4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX4_3, NPC_FRANK_FRANK_MAX4_1, NPC_FRANK_FRANK_MAX4_2` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `frank_max5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX5_1, NPC_FRANK_FRANK_MAX5_2, NPC_FRANK_FRANK_MAX5_3` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `frank_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_MAX_INTRO_2, NPC_FRANK_FRANK_MAX_INTRO_3, NPC_FRANK_FRANK_MAX...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `frank_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ frank_max1 frank_max2 frank_max3 frank_max4 frank_max5 ]` | 1 |

</details>

---

### Context: `frank_terminator2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TERMINATOR2_2, NPC_FRANK_FRANK_TERMINATOR2_3, NPC_FRANK_FRANK...` | 15 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 8 |

</details>

---

### Context: `frank_tips_1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_1_1, NPC_FRANK_FRANK_TIPS_1_2, NPC_FRANK_FRANK_TIPS_1_3` | 4 |

</details>

---

### Context: `frank_tips_10`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_10_2, NPC_FRANK_FRANK_TIPS_10_1, NPC_FRANK_FRANK_TIPS_10_3` | 4 |

</details>

---

### Context: `frank_tips_2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_2_1, NPC_FRANK_FRANK_TIPS_2_2, NPC_FRANK_FRANK_TIPS_2_3` | 3 |

</details>

---

### Context: `frank_tips_3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_3_3, NPC_FRANK_FRANK_TIPS_3_2, NPC_FRANK_FRANK_TIPS_3_1` | 3 |

</details>

---

### Context: `frank_tips_4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_4_3, NPC_FRANK_FRANK_TIPS_4_2, NPC_FRANK_FRANK_TIPS_4_1` | 3 |

</details>

---

### Context: `frank_tips_5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_5_1, NPC_FRANK_FRANK_TIPS_5_3, NPC_FRANK_FRANK_TIPS_5_2` | 5 |

</details>

---

### Context: `frank_tips_6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_6_2, NPC_FRANK_FRANK_TIPS_6_1, NPC_FRANK_FRANK_TIPS_6_3` | 3 |

</details>

---

### Context: `frank_tips_7`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_7_3, NPC_FRANK_FRANK_TIPS_7_2, NPC_FRANK_FRANK_TIPS_7_1` | 3 |

</details>

---

### Context: `frank_tips_8`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_8_2, NPC_FRANK_FRANK_TIPS_8_1, NPC_FRANK_FRANK_TIPS_8_3` | 3 |

</details>

---

### Context: `frank_tips_9`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_FRANK_TIPS_9_2, NPC_FRANK_FRANK_TIPS_9_1` | 2 |

</details>

---

### Context: `gone`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `gone` | 1 |

</details>

---

### Context: `house_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_INTRO_1, NPC_POPUP_HOUSE_INTRO_2, NPC_POPUP_HOUSE_INTRO_3` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left, tink_point_cats` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_HOUSE_INTRO_11` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click` | 1 |

</details>

---

### Context: `house_kitten_box`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_KITTEN_BOX_2, NPC_POPUP_HOUSE_KITTEN_BOX_1` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `house_pass_day`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_PASS_DAY_3, NPC_POPUP_HOUSE_PASS_DAY_1, NPC_POPUP_HOUSE_PASS_...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left, tink_point_food` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 3 |

</details>

---

### Context: `house_pass_day2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_PASS_DAY2_3, NPC_POPUP_HOUSE_PASS_DAY2_1, NPC_POPUP_HOUSE_PAS...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `house_pipe`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_PIPE_1, NPC_POPUP_HOUSE_PIPE_2, NPC_POPUP_HOUSE_PIPE_3` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `frank_right, offscreen, frank_point_pipe` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 4 |

</details>

---

### Context: `house_retired_cat_box`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMove` | 2 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_RETIRED_CAT_BOX_1` | 1 |

</details>

---

### Context: `house_starred_box`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_STARRED_BOX_1, NPC_POPUP_HOUSE_STARRED_BOX_2` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `house_strays`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_HOUSE_STRAYS_3, NPC_POPUP_HOUSE_STRAYS_2, NPC_POPUP_HOUSE_STRAYS_1` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left, tink_point_strays` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 3 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_HOUSE_STRAYS_5` | 1 |
| [`request_cat_info`](./Enums.md#enum-request_cat_info) | Enum | Examples: `stray` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click` | 1 |

</details>

---

### Context: `house_upgrade_4throom`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_4THROOM_3, NPC_FRANK_HOUSE_UPGRADE_4THROOM_2, NPC_FRA...` | 17 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 10 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `house_upgrade_attic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_ATTIC_3, NPC_FRANK_HOUSE_UPGRADE_ATTIC_2, NPC_FRANK_H...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `house_upgrade_basement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT_1` | 1 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `house_upgrade_basement2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT2_1` | 1 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `house_upgrade_basement3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT3_1` | 1 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `house_upgrade_basement4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT4_1` | 1 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `house_upgrade_basement5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_BASEMENT5_1` | 1 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `house_upgrade_largehouse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_3, NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_1, N...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `house_upgrade_mediumhouse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_2, NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_3,...` | 21 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 12 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_INTRO_3, NPC_BEANIES_INTRO_1, NPC_BEANIES_INTRO_2` | 26 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 10 |
| [`set_mood`](./Enums.md#enum-set_mood) | Enum | Examples: `veryhappy, happy, default` | 9 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `reject_cat, choose_cat2, choose_cat1` | 3 |
| `delay` | Mixed | Examples: `.05, 5.4` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_BEANIES_INTRO_15` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `Intro_LabDisposal` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `introduce_hard_path`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_INTRODUCE_HARD_PATH_1, NPC_POPUP_INTRODUCE_HARD_PATH_3, NPC_POPUP_I...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, offscreen` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `jack_begin_accepting_cats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_2, NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_3, N...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 5 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `jack` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_desert_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_DESERT_INTRO_1, NPC_JACK_JACK_DESERT_INTRO_3, NPC_JACK_JACK_DES...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 5 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_introduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_JACK_INTRODUCTION_2, NPC_POPUP_JACK_INTRODUCTION_3, NPC_POPUP_JACK_...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `jack_point_furniture, offscreen, jack_right` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 4 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_JACK_INTRODUCTION_7` | 1 |
| [`get_random_furniture_piece`](./Arrays.md#array-get_random_furniture_piece) | Array | Examples: `[ small_trash_cans small_trash_can2 ]` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `open_furniture` | 1 |

</details>

---

### Context: `jack_max1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 4 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX1_3, NPC_JACK_JACK_MAX1_2, NPC_JACK_JACK_MAX1_1` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_max2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX2_2, NPC_JACK_JACK_MAX2_1, NPC_JACK_JACK_MAX2_3` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_max3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX3_1, NPC_JACK_JACK_MAX3_2, NPC_JACK_JACK_MAX3_3` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_max4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX4_1, NPC_JACK_JACK_MAX4_3, NPC_JACK_JACK_MAX4_2` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_max5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX5_2, NPC_JACK_JACK_MAX5_1, NPC_JACK_JACK_MAX5_3` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_MAX_INTRO_3, NPC_JACK_JACK_MAX_INTRO_2, NPC_JACK_JACK_MAX_INTRO_1` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ jack_max1 jack_max2 jack_max3 jack_max4 jack_max5 ]` | 1 |

</details>

---

### Context: `jack_shopupgrade1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE1_3, NPC_JACK_JACK_SHOPUPGRADE1_2, NPC_JACK_JACK_SHO...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_shopupgrade2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE2_2, NPC_JACK_JACK_SHOPUPGRADE2_1, NPC_JACK_JACK_SHO...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_shopupgrade3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE3_3, NPC_JACK_JACK_SHOPUPGRADE3_2, NPC_JACK_JACK_SHO...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_shopupgrade4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_SHOPUPGRADE4_3, NPC_JACK_JACK_SHOPUPGRADE4_2, NPC_JACK_JACK_SHO...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `jack_zara`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_JACK_JACK_ZARA_3, NPC_JACK_JACK_ZARA_1, NPC_JACK_JACK_ZARA_2` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, idle, blocking` | 4 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `level_up_didnt_select_sunburn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_1, NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SU...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, offscreen` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `level_up_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LEVEL_UP_INTRO_1, NPC_POPUP_LEVEL_UP_INTRO_2, NPC_POPUP_LEVEL_UP_IN...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_levelup, butch_point_hotblooded, butch_point_sunburn` | 5 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 4 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click, hovered_passive` | 2 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_LEVEL_UP_INTRO_6` | 1 |
| `lock_mouse` | Number | Examples: `1` | 1 |
| `unlock_mouse` | Number | Examples: `1` | 1 |

</details>

---

### Context: `level_up_selected_sunburn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_2, NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_1,...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, offscreen` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `low_on_food`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `tink_point_box, tink_left, tink_point_food` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 4 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_LOW_ON_FOOD_3, NPC_POPUP_LOW_ON_FOOD_1, NPC_POPUP_LOW_ON_FOOD_2` | 3 |

</details>

---

### Context: `map_click_node`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_mapnode, offscreen` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MAP_CLICK_NODE_1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `mapnode_selected` | 1 |

</details>

---

### Context: `map_equip_items`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_left, butch_point_inventory, offscreen` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 3 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MAP_EQUIP_ITEMS_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MAP_EQUIP_ITEMS_2` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `inventory_selected` | 1 |

</details>

---

### Context: `map_equip_items2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_point_inventory` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint` | 2 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `map_equip_items2` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MAP_EQUIP_ITEMS2_1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `inventory_selected` | 1 |

</details>

---

### Context: `melee_attack_rat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMoveHint, UISFX_ButchMove` | 3 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_ATTACK_RAT_2, NPC_POPUP_MELEE_ATTACK_RAT_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_ATTACK_RAT_3` | 1 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `ranged_cat_attack` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `melee_cat_spit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_spells` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 3 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_2, NPC_POPUP_MELEE_CAT_SPIT_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_3` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `melee_cat_spit_fail_ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_2, NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_1, N...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_4` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `melee_cat_spit_fail_miss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_2, NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_3, N...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_4` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `melee_cat_spit_fail_rat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_1, NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_2, NPC...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_4` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `melee_cat_spit_ignore`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `melee_cat_spit_ignore` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_IGNORE_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_IGNORE_2` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `melee_cat_spit_success`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_2, NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_3, NPC_P...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_4` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `melee_killed_rat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_passives, butch_point_team_nocircle` | 5 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHintDelay1, UISFX_ButchMove` | 4 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_KILLED_RAT_2, NPC_POPUP_MELEE_KILLED_RAT_1, NPC_POPUP_MELEE_K...` | 3 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `click, hovered_passive` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_KILLED_RAT_3` | 1 |
| `unlock_mouse` | Number | Examples: `1` | 1 |

</details>

---

### Context: `melee_move2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_move` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMoveHint, UISFX_ButchMove` | 3 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `melee_move2` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_MOVE2_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_MOVE2_2` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `melee_out_of_actions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveHint, UISFX_ButchHintDelay1, UISFX_ButchHint` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_mana, butch_point_cost, butch_point_spells` | 5 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_MELEE_OUT_OF_ACTIONS_2, NPC_POPUP_MELEE_OUT_OF_ACTIONS_1, NPC_POPUP...` | 3 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_MELEE_OUT_OF_ACTIONS_4` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `end_turn` | 1 |

</details>

---

### Context: `new_adventure`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `tink_point_box, offscreen, tink_left` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 3 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_NEW_ADVENTURE_2, NPC_POPUP_NEW_ADVENTURE_1` | 2 |

</details>

---

### Context: `organ_boneyard_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_3, NPC_ORGANGRINDER_ORGAN_BONEYARD_INTR...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 6 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_INTRO_1, NPC_ORGANGRINDER_ORGAN_INTRO_2, NPC_ORGANGRIN...` | 19 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 9 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `organgrinder` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_INTRO_20` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| [`set_organ_name`](./Strings.md#string-set_organ_name) | String | Examples: `"Tyler"` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_max1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX1_1, NPC_ORGANGRINDER_ORGAN_MAX1_3, NPC_ORGANGRINDE...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, idle, idle2` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_max2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX2_1, NPC_ORGANGRINDER_ORGAN_MAX2_3, NPC_ORGANGRINDE...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_max3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX3_3, NPC_ORGANGRINDER_ORGAN_MAX3_1, NPC_ORGANGRINDE...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_max4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX4_2, NPC_ORGANGRINDER_ORGAN_MAX4_3, NPC_ORGANGRINDE...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_max5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX5_1, NPC_ORGANGRINDER_ORGAN_MAX5_2, NPC_ORGANGRINDE...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_MAX_INTRO_3, NPC_ORGANGRINDER_ORGAN_MAX_INTRO_1, NPC_O...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ organ_max1 organ_max2 organ_max3 organ_max4 organ_max5 ]` | 1 |

</details>

---

### Context: `organ_rename`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_RENAME_3, NPC_ORGANGRINDER_ORGAN_RENAME_1, NPC_ORGANGR...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| `lock_controls` | Number | Examples: `1` | 1 |
| [`set_organ_name`](./Strings.md#string-set_organ_name) | String | Examples: `"Tyler"` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_throbbingdomain_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_2, NPC_ORGANGRINDER_ORGAN_THROBB...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 9 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_tina3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_TINA3_1, NPC_ORGANGRINDER_ORGAN_TINA3_2, NPC_ORGANGRIN...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 13 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_unlock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UNLOCK_1, NPC_ORGANGRINDER_ORGAN_UNLOCK_3, NPC_ORGANGR...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_upgrade1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE1_3, NPC_ORGANGRINDER_ORGAN_UPGRADE1_1, NPC_ORG...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_upgrade2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE2_2, NPC_ORGANGRINDER_ORGAN_UPGRADE2_3, NPC_ORG...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_upgrade3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE3_1, NPC_ORGANGRINDER_ORGAN_UPGRADE3_2, NPC_ORG...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_upgrade4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE4_1, NPC_ORGANGRINDER_ORGAN_UPGRADE4_2, NPC_ORG...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_upgrade5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE5_1, NPC_ORGANGRINDER_ORGAN_UPGRADE5_3, NPC_ORG...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `organ_upgrade6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_ORGANGRINDER_ORGAN_UPGRADE6_1, NPC_ORGANGRINDER_ORGAN_UPGRADE6_2, NPC_ORG...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, idle2` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `purchase_item_a`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_A_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `purchase_item_b`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_B_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `purchase_item_c`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_C_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `purchase_item_d`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_D_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `purchase_item_iceage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_ICEAGE_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `purchase_item_jurassic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_JURASSIC_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `purchase_item_moon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_MOON_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `purchase_item_theend`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_PURCHASE_ITEM_THEEND_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `ranged_attack_tomtom`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_1, NPC_POPUP_RANGED_ATTACK_TOMTOM_2` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_attack_tomtom_fail_ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_ALLY_1, NPC_POPUP_RANGED_ATTACK_TOMTOM_FA...` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_attack_tomtom_fail_miss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_MISS_2, NPC_POPUP_RANGED_ATTACK_TOMTOM_FA...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_attack_tomtom_fail_rat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_RAT_1, NPC_POPUP_RANGED_ATTACK_TOMTOM_FAI...` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_cat_attack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ATTACK_1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `ranged_cat_early_attack2_ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_ALLY_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK2...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_cat_early_attack2_miss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_MISS_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK2...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_cat_early_attack2_rat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_RAT_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_cat_early_attack_ally`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_ALLY_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK_A...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_cat_early_attack_miss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_MISS_3, NPC_POPUP_RANGED_CAT_EARLY_ATTACK_M...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_cat_early_attack_rat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RAT_2, NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RA...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_cat_failmove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_FAILMOVE_1, NPC_POPUP_RANGED_CAT_FAILMOVE_2, NPC_POPUP_R...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `ranged_cat_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_attack, butch_point_move` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveHint, UISFX_ButchHint, UISFX_ButchMove` | 4 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_INTRO_3, NPC_POPUP_RANGED_CAT_INTRO_1, NPC_POPUP_RANGED_...` | 3 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_INTRO_4` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `ranged_cat_roll`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_point_cost2, butch_right, butch_point_spells` | 6 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchHintDelay2, UISFX_ButchHint, UISFX_ButchMove` | 6 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLL_1, NPC_POPUP_RANGED_CAT_ROLL_2, NPC_POPUP_RANGED_CA...` | 5 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLL_6` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `ranged_cat_rolled_first`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_3, NPC_POPUP_RANGED_CAT_ROLLED_FIRST_1, NPC...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_move` | 3 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_4` | 1 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `steven_100`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_100_2, NPC_STEVEN_STEVEN_100_1, NPC_STEVEN_STEVEN_100_3` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 3 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_introduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_INTRODUCTION_2, NPC_STEVEN_STEVEN_INTRODUCTION_3, NPC_STEVE...` | 19 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, talking` | 13 |
| [`blocking`](./Enums.md#enum-blocking) | Enum | Examples: `idlenoani` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_milliontrashed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_MILLIONTRASHED_3, NPC_STEVEN_STEVEN_MILLIONTRASHED_1, NPC_S...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, talking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `steven_postendgame`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_POSTENDGAME_1, NPC_STEVEN_STEVEN_POSTENDGAME_2, NPC_STEVEN_...` | 15 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 10 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_resummon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_RESUMMON_1` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_savescum_1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_1alt1 steven_savescum_1alt2 steven_save...` | 1 |

</details>

---

### Context: `steven_savescum_100`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_100_3, NPC_POPUP_STEVEN_SAVESCUM_100_2, NPC_POPUP_S...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_1alt1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_2, NPC_POPUP_STEVEN_SAVESCUM_1ALT1_1, NPC_POP...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_1alt2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_1, NPC_POPUP_STEVEN_SAVESCUM_1ALT2_2, NPC_POP...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_1alt3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_2, NPC_POPUP_STEVEN_SAVESCUM_1ALT3_1, NPC_POP...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_2alt1 steven_savescum_2alt2 steven_save...` | 1 |

</details>

---

### Context: `steven_savescum_2alt1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_2, NPC_POPUP_STEVEN_SAVESCUM_2ALT1_1, NPC_POP...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `steven_cat, offscreen, steven_center` | 3 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_2alt2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_2, NPC_POPUP_STEVEN_SAVESCUM_2ALT2_3, NPC_POP...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `steven_cat, offscreen, steven_center` | 3 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_2alt3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_3, NPC_POPUP_STEVEN_SAVESCUM_2ALT3_2, NPC_POP...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `steven_cat, offscreen, steven_center` | 4 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_3alt1 steven_savescum_3alt2 steven_save...` | 1 |

</details>

---

### Context: `steven_savescum_3alt1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_3, NPC_POPUP_STEVEN_SAVESCUM_3ALT1_2, NPC_POP...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_3alt2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_3, NPC_POPUP_STEVEN_SAVESCUM_3ALT2_1, NPC_POP...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_3alt3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_3, NPC_POPUP_STEVEN_SAVESCUM_3ALT3_2, NPC_POP...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ steven_savescum_4alt1 steven_savescum_4alt2 steven_save...` | 1 |

</details>

---

### Context: `steven_savescum_4alt1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_4ALT1_2, NPC_POPUP_STEVEN_SAVESCUM_4ALT1_1, NPC_POP...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_4alt2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_4ALT2_2, NPC_POPUP_STEVEN_SAVESCUM_4ALT2_1, NPC_POP...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_4alt3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_4ALT3_2, NPC_POPUP_STEVEN_SAVESCUM_4ALT3_3, NPC_POP...` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_houseboss_1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_1, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 |

</details>

---

### Context: `steven_savescum_houseboss_100`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_100_2, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOS...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 |

</details>

---

### Context: `steven_savescum_houseboss_2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_3, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 |

</details>

---

### Context: `steven_savescum_houseboss_3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_1, NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_...` | 19 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 |

</details>

---

### Context: `steven_savescum_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_INTRO_1, NPC_POPUP_STEVEN_SAVESCUM_INTRO_3, NPC_POP...` | 24 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `adventure` | 1 |

</details>

---

### Context: `steven_savescum_intro_houseboss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_3, NPC_POPUP_STEVEN_SAVESCUM_INTRO_...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, steven_center` | 2 |
| [`autosave`](./Enums.md#enum-autosave) | Enum | Examples: `housebossprep` | 1 |

</details>

---

### Context: `steven_unlock_act1_crazy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 8 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_3, NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_2,...` | 6 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_unlock_act1_impossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_3, NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMP...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `talking, closeup, idle` | 4 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_unlock_act2_crazy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_1, NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_2,...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 5 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_unlock_act2_hard`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_3, NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_2, N...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, talking` | 4 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_unlock_act2_impossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_2, NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMP...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, talking, idle` | 4 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_unlock_act3_crazy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_3, NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_2,...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 4 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_unlock_act3_hard`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_2, NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_1, N...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 8 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `steven_unlock_act3_impossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_3, NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMP...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 6 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `take_cats_inside`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, tink_left` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `take_cats_inside` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TAKE_CATS_INSIDE_1` | 1 |

</details>

---

### Context: `test_gamepad_prompts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dialog` | Mixed | Examples: `"Switch to gamepad now if you wanna see gamepad bindings.", NPC_POPUP_FIRST_F...` | 8 |

</details>

---

### Context: `tink_aggression`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_AGGRESSION_2, NPC_TINK_TINK_AGGRESSION_1, NPC_TINK_TINK_AGGRESS...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, zoomedout, idle` | 11 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_basestats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_BASESTATS_1, NPC_TINK_TINK_BASESTATS_2, NPC_TINK_TINK_BASESTATS_3` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_begin_accepting_cats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_3, NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_2, N...` | 21 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 12 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `tink` | 1 |

</details>

---

### Context: `tink_inbreeding`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_INBREEDING_2, NPC_TINK_TINK_INBREEDING_3, NPC_TINK_TINK_INBREED...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX1_3, NPC_TINK_TINK_MAX1_1, NPC_TINK_TINK_MAX1_2` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max10`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX10_3, NPC_TINK_TINK_MAX10_1, NPC_TINK_TINK_MAX10_2` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX2_3, NPC_TINK_TINK_MAX2_2, NPC_TINK_TINK_MAX2_1` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX3_2, NPC_TINK_TINK_MAX3_3, NPC_TINK_TINK_MAX3_1` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX4_3, NPC_TINK_TINK_MAX4_2, NPC_TINK_TINK_MAX4_1` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX5_3, NPC_TINK_TINK_MAX5_1, NPC_TINK_TINK_MAX5_2` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX6_2, NPC_TINK_TINK_MAX6_1, NPC_TINK_TINK_MAX6_3` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max7`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX7_2, NPC_TINK_TINK_MAX7_3, NPC_TINK_TINK_MAX7_1` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 |

</details>

---

### Context: `tink_max8`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX8_2, NPC_TINK_TINK_MAX8_1, NPC_TINK_TINK_MAX8_3` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max9`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX9_2, NPC_TINK_TINK_MAX9_1, NPC_TINK_TINK_MAX9_3` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_MAX_INTRO_2, NPC_TINK_TINK_MAX_INTRO_3, NPC_TINK_TINK_MAX_INTRO_1` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, zoomedout` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ tink_max1 tink_max2 tink_max3 tink_max4 tink_max5 tink_...` | 1 |

</details>

---

### Context: `tink_prettybow`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_PRETTYBOW_3, NPC_TINK_TINK_PRETTYBOW_2, NPC_TINK_TINK_PRETTYBOW_1` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_relationships`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_RELATIONSHIPS_3, NPC_TINK_TINK_RELATIONSHIPS_1, NPC_TINK_TINK_R...` | 20 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 13 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_sexuality`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_SEXUALITY_2, NPC_TINK_TINK_SEXUALITY_3, NPC_TINK_TINK_SEXUALITY_1` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_tags`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TAGS_1, NPC_TINK_TINK_TAGS_2, NPC_TINK_TINK_TAGS_3` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `tink_terminator`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TERMINATOR_2, NPC_TINK_TINK_TERMINATOR_1, NPC_TINK_TINK_TERMINA...` | 15 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 5 |

</details>

---

### Context: `tink_tina2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TINA2_2, NPC_TINK_TINK_TINA2_1, NPC_TINK_TINK_TINA2_3` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |

</details>

---

### Context: `tink_tips_appeal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_APPEAL_3, NPC_TINK_TINK_TIPS_APPEAL_2, NPC_TINK_TINK_TIPS_...` | 4 |

</details>

---

### Context: `tink_tips_basestats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_BASESTATS_2, NPC_TINK_TINK_TIPS_BASESTATS_1, NPC_TINK_TINK...` | 3 |

</details>

---

### Context: `tink_tips_cleaning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_CLEANING_2, NPC_TINK_TINK_TIPS_CLEANING_1, NPC_TINK_TINK_T...` | 4 |

</details>

---

### Context: `tink_tips_comfort`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_COMFORT_3, NPC_TINK_TINK_TIPS_COMFORT_2, NPC_TINK_TINK_TIP...` | 4 |

</details>

---

### Context: `tink_tips_health`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_HEALTH_1, NPC_TINK_TINK_TIPS_HEALTH_3, NPC_TINK_TINK_TIPS_...` | 5 |

</details>

---

### Context: `tink_tips_inbreeding`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_INBREEDING_1, NPC_TINK_TINK_TIPS_INBREEDING_2, NPC_TINK_TI...` | 5 |

</details>

---

### Context: `tink_tips_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_INTRO_3, NPC_TINK_TINK_TIPS_INTRO_1, NPC_TINK_TINK_TIPS_IN...` | 4 |
| [`do_sequence`](./Enums.md#enum-do_sequence) | Enum | Examples: `tink_tips_comfort` | 1 |

</details>

---

### Context: `tink_tips_multiclassing`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_MULTICLASSING_3, NPC_TINK_TINK_TIPS_MULTICLASSING_2, NPC_T...` | 5 |

</details>

---

### Context: `tink_tips_mutation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_MUTATION_2, NPC_TINK_TINK_TIPS_MUTATION_1, NPC_TINK_TINK_T...` | 4 |

</details>

---

### Context: `tink_tips_stimulation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TINK_TINK_TIPS_STIMULATION_3, NPC_TINK_TINK_TIPS_STIMULATION_2, NPC_TINK_...` | 7 |

</details>

---

### Context: `tracy_blankcollar1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_BLANKCOLLAR1_1, NPC_TRACY_TRACY_BLANKCOLLAR1_3, NPC_TRACY_TRA...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 8 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_blankcollar2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_BLANKCOLLAR2_1, NPC_TRACY_TRACY_BLANKCOLLAR2_3, NPC_TRACY_TRA...` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_blankcollar3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_BLANKCOLLAR3_2, NPC_TRACY_TRACY_BLANKCOLLAR3_3, NPC_TRACY_TRA...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodbonus1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODBONUS1_2, NPC_TRACY_TRACY_FOODBONUS1_1` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE1_3, NPC_TRACY_TRACY_FOODSTORAGE1_1, NPC_TRACY_TRA...` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage10`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE10_2, NPC_TRACY_TRACY_FOODSTORAGE10_1, NPC_TRACY_T...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE2_3, NPC_TRACY_TRACY_FOODSTORAGE2_2, NPC_TRACY_TRA...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE3_1, NPC_TRACY_TRACY_FOODSTORAGE3_2, NPC_TRACY_TRA...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 9 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE4_3, NPC_TRACY_TRACY_FOODSTORAGE4_1, NPC_TRACY_TRA...` | 15 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 9 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE5_1, NPC_TRACY_TRACY_FOODSTORAGE5_3, NPC_TRACY_TRA...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE6_1, NPC_TRACY_TRACY_FOODSTORAGE6_2, NPC_TRACY_TRA...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage7`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE7_2, NPC_TRACY_TRACY_FOODSTORAGE7_3, NPC_TRACY_TRA...` | 12 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage8`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE8_2, NPC_TRACY_TRACY_FOODSTORAGE8_1, NPC_TRACY_TRA...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_foodstorage9`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_FOODSTORAGE9_3, NPC_TRACY_TRACY_FOODSTORAGE9_2, NPC_TRACY_TRA...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_idol1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL1_3, NPC_TRACY_TRACY_IDOL1_2, NPC_TRACY_TRACY_IDOL1_1` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_idol2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL2_3, NPC_TRACY_TRACY_IDOL2_1, NPC_TRACY_TRACY_IDOL2_2` | 8 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_idol3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL3_2, NPC_TRACY_TRACY_IDOL3_1, NPC_TRACY_TRACY_IDOL3_3` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_idol4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL4_2, NPC_TRACY_TRACY_IDOL4_3, NPC_TRACY_TRACY_IDOL4_1` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, idle, blocking` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_idol5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL5_3, NPC_TRACY_TRACY_IDOL5_2, NPC_TRACY_TRACY_IDOL5_1` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle, blocking` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_idol6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL6_1, NPC_TRACY_TRACY_IDOL6_3, NPC_TRACY_TRACY_IDOL6_2` | 11 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_idol7`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_IDOL7_1, NPC_TRACY_TRACY_IDOL7_3, NPC_TRACY_TRACY_IDOL7_2` | 17 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 11 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_introduction`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_INTRODUCTION_3, NPC_TRACY_TRACY_INTRODUCTION_2, NPC_TRACY_TRA...` | 22 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 13 |
| [`begin_accepting_cats`](./Enums.md#enum-begin_accepting_cats) | Enum | Examples: `tracy` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_kaijufight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_KAIJUFIGHT_2, NPC_TRACY_TRACY_KAIJUFIGHT_1, NPC_TRACY_TRACY_K...` | 10 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 7 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_max1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 5 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX1_2, NPC_TRACY_TRACY_MAX1_1, NPC_TRACY_TRACY_MAX1_3` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_max2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 5 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX2_3, NPC_TRACY_TRACY_MAX2_2, NPC_TRACY_TRACY_MAX2_1` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_max3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX3_2, NPC_TRACY_TRACY_MAX3_1, NPC_TRACY_TRACY_MAX3_3` | 4 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `idle, blocking` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_max4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX4_3, NPC_TRACY_TRACY_MAX4_2, NPC_TRACY_TRACY_MAX4_1` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, blocking` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_max5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX5_1, NPC_TRACY_TRACY_MAX5_2, NPC_TRACY_TRACY_MAX5_3` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, blocking` | 7 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_max_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_TRACY_MAX_INTRO_2, NPC_TRACY_TRACY_MAX_INTRO_1, NPC_TRACY_TRACY_MAX...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, zoomedout, blocking` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| `lock_controls` | Number | Examples: `1` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |

</details>

---

### Context: `tracy_max_repeating`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ tracy_max1 tracy_max2 tracy_max3 tracy_max4 tracy_max5 ]` | 1 |

</details>

---

### Context: `try_again_attack_rat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_1, NPC_POPUP_TRY_AGAIN_ATTACK_RAT_3, NPC_POPUP...` | 3 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_attack` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHintDelay1, UISFX_ButchMove` | 3 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `try_again_attack_rat` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_4` | 1 |
| [`reset_turn`](./Enums.md#enum-reset_turn) | Enum | Examples: `act` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `try_again_melee_move`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TRY_AGAIN_MELEE_MOVE_1, NPC_POPUP_TRY_AGAIN_MELEE_MOVE_2` | 2 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMove` | 2 |
| [`clear_token`](./Enums.md#enum-clear_token) | Enum | Examples: `try_again_melee_move` | 1 |
| [`reset_turn`](./Enums.md#enum-reset_turn) | Enum | Examples: `both` | 1 |

</details>

---

### Context: `tutorial_cat_dies`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_TUTORIAL_CAT_DIES_1, NPC_POPUP_TUTORIAL_CAT_DIES_3, NPC_POPUP_TUTOR...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right` | 2 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchMove` | 2 |

</details>

---

### Context: `unprompted1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED1_1` | 1 |

</details>

---

### Context: `unprompted2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED2_1, NPC_BEANIES_UNPROMPTED2_2` | 2 |

</details>

---

### Context: `unprompted3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED3_2, NPC_BEANIES_UNPROMPTED3_1, NPC_BEANIES_UNPROMPTED3_3` | 3 |

</details>

---

### Context: `unprompted4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED4_1` | 1 |

</details>

---

### Context: `unprompted5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED5_1, NPC_BEANIES_UNPROMPTED5_2` | 2 |

</details>

---

### Context: `unprompted6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BEANIES_UNPROMPTED6_2, NPC_BEANIES_UNPROMPTED6_3, NPC_BEANIES_UNPROMPTED6_1` | 3 |

</details>

---

### Context: `upgrade_storage_1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_1_3, NPC_BUTCH_UPGRADE_STORAGE_1_2, NPC_BUTCH_UPGRA...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_2_2, NPC_BUTCH_UPGRADE_STORAGE_2_1, NPC_BUTCH_UPGRA...` | 6 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_3_1, NPC_BUTCH_UPGRADE_STORAGE_3_3, NPC_BUTCH_UPGRA...` | 9 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_4_1, NPC_BUTCH_UPGRADE_STORAGE_4_3, NPC_BUTCH_UPGRA...` | 17 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `verycloseup, closeup, idle` | 9 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_5_2, NPC_BUTCH_UPGRADE_STORAGE_5_1, NPC_BUTCH_UPGRA...` | 16 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_6_2, NPC_BUTCH_UPGRADE_STORAGE_6_3, NPC_BUTCH_UPGRA...` | 15 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 9 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_7`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_7_2, NPC_BUTCH_UPGRADE_STORAGE_7_3, NPC_BUTCH_UPGRA...` | 13 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 5 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_max1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX1_3, NPC_BUTCH_UPGRADE_STORAGE_MAX1_2, NPC_BUTCH...` | 6 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup` | 1 |

</details>

---

### Context: `upgrade_storage_max2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX2_2, NPC_BUTCH_UPGRADE_STORAGE_MAX2_3, NPC_BUTCH...` | 4 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_max3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX3_2, NPC_BUTCH_UPGRADE_STORAGE_MAX3_3, NPC_BUTCH...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_max4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX4_3, NPC_BUTCH_UPGRADE_STORAGE_MAX4_2, NPC_BUTCH...` | 5 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_max5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_MAX5_3, NPC_BUTCH_UPGRADE_STORAGE_MAX5_2, NPC_BUTCH...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `zoomedout, closeup, idle` | 3 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_repeating_crazy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 |

</details>

---

### Context: `upgrade_storage_repeating_hard`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 |

</details>

---

### Context: `upgrade_storage_repeating_impossible`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 |

</details>

---

### Context: `upgrade_storage_repeating_intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_3, NPC_BUTCH_UPGRADE_STORAGE_REPEAT...` | 7 |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `closeup, idle` | 2 |
| [`get`](./Enums.md#enum-get) | Enum | Examples: `npc_reward` | 1 |

</details>

---

### Context: `upgrade_storage_repeating_normal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`do_random_sequence`](./Arrays.md#array-do_random_sequence) | Array | Examples: `[ upgrade_storage_max1 upgrade_storage_max2 upgrade_stora...` | 1 |

</details>

---

### Context: `use_attack_after_used_weapon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `butch_right, butch_point_attack, butch_point_weapon` | 4 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 4 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_1, NPC_POPUP_USE_ATTACK_AFTER_USED_WEA...` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_3` | 1 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `use_weapon` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `use_weapon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`set_state`](./Enums.md#enum-set_state) | Enum | Examples: `offscreen, butch_right, butch_point_weapon` | 3 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | Examples: `UISFX_ButchMoveAway, UISFX_ButchHint, UISFX_ButchMove` | 3 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_POPUP_USE_WEAPON_2, NPC_POPUP_USE_WEAPON_1` | 2 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_POPUP_USE_WEAPON_3` | 1 |
| [`get_token`](./Enums.md#enum-get_token) | Enum | Examples: `use_attack_after_used_weapon` | 1 |
| `unlock_controls` | Number | Examples: `1` | 1 |
| [`wait_for`](./Enums.md#enum-wait_for) | Enum | Examples: `action_selected` | 1 |

</details>

---

### Context: `welcome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_2` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_boneyard`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BONEYARD_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BONEYARD_2` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_bunker`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BUNKER_2, NPC_TRACY_SHOP_WELCOME_BUNKER_1` | 2 |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_BUNKER_3` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_caves`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CAVES_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CAVES_2` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_core`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CORE_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_crater`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CRATER_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_CRATER_2` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_desert`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_DESERT_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_future`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_FUTURE_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_iceage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_ICEAGE_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_ICEAGE_2` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_junkyard`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_JUNKYARD_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_jurassic`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_JURASSIC_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_JURASSIC_2` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_lab`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_LAB_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_LAB_2` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_moon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_MOON_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_sewers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_SEWERS_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_SEWERS_2` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_theend`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog`](./Enums.md#enum-dialog) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_THEEND_1` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_THEEND_2` | 1 |
| [`set_npc_voice`](./Enums.md#enum-set_npc_voice) | Enum | Examples: `beanies` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_water`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_WATER_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

### Context: `welcome_water_cheap`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./NPC_Scripts.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cancelable` | Boolean | Examples: `true` | 1 |
| [`delay`](./Enums.md#enum-delay) | Enum | Examples: `.5` | 1 |
| [`dialog_and_autopass`](./Enums.md#enum-dialog_and_autopass) | Enum | Examples: `NPC_TRACY_SHOP_WELCOME_WATER_CHEAP_1` | 1 |
| `wait_for_cancel` | Number | Examples: `1` | 1 |

</details>

---

