# Progression Unlocks Directory

## File: `adventure_progression_unlocks.gon`

### `class_unlock_medic`
**Source:** `adventure_progression_unlocks.gon`  

```
class_unlock_medic {
	complete_chapter alley
	trigger_npc_sequence class_unlock_medic
}
```

---

### `class_unlock_thief`
**Source:** `adventure_progression_unlocks.gon`  

```
class_unlock_thief {
	complete_chapter sewers
	trigger_npc_sequence class_unlock_thief
}
```

---

### `class_unlock_necromancer`
**Source:** `adventure_progression_unlocks.gon`  

```
class_unlock_necromancer {
	complete_chapter boneyard
	trigger_npc_sequence class_unlock_necromancer
}
```

---

### `class_unlock_psychic`
**Source:** `adventure_progression_unlocks.gon`  

```
class_unlock_psychic {
	complete_chapter moon
	trigger_npc_sequence class_unlock_psychic
}
```

---

### `class_unlock_tinkerer`
**Source:** `adventure_progression_unlocks.gon`  

```
class_unlock_tinkerer {
	complete_chapter bunker
	trigger_npc_sequence class_unlock_tinkerer
}
```

---

### `class_unlock_druid`
**Source:** `adventure_progression_unlocks.gon`  

```
class_unlock_druid {
	complete_chapter crater
	trigger_npc_sequence class_unlock_druid
}
```

---

### `class_unlock_butcher`
**Source:** `adventure_progression_unlocks.gon`  

```
class_unlock_butcher {
	complete_chapter core
	trigger_npc_sequence class_unlock_butcher
}
```

---

### `class_unlock_monk`
**Source:** `adventure_progression_unlocks.gon`  

```
class_unlock_monk {
	complete_chapter lab
	trigger_npc_sequence class_unlock_monk
}
```

---

### `class_unlock_jester`
**Source:** `adventure_progression_unlocks.gon`  

```
class_unlock_jester {
	complete_chapter dimensionx
	trigger_npc_sequence class_unlock_jester
	unlock_boss jestercat
}
```

---

### `map_unlock_hardpath`
**Source:** `adventure_progression_unlocks.gon`  

```
map_unlock_hardpath {
	complete_chapter sewers
	//popup blah
	set_mapgen_flag HardPathUnlocked
}
```

---

### `map_unlock_sewers`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_SEWERS`: "You can now adventure to The Sewers!"

```
map_unlock_sewers {
	complete_chapter alley
	popup {
		prompt AREA_UNLOCK_SEWERS
		frame UnlockArea_Sewers
	}

	set_mapgen_flag SewersUnlocked
}
```

---

### `map_unlock_junkyard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_JUNKYARD`: "You can now adventure to The Junkyard!"

```
map_unlock_junkyard {
	//triggered via unlockcheck_on_complete on alley boss
	requires_hard_path true
	popup {
		prompt AREA_UNLOCK_JUNKYARD
		immediate true
		frame UnlockArea_Junkyard
	}
	set_mapgen_flag JunkyardUnlocked
}
```

---

### `map_unlock_boneyard`
**Source:** `adventure_progression_unlocks.gon`  

```
map_unlock_boneyard {
	complete_chapter junkyard
	trigger_npc_sequence_tomorrow butch_boneyard_intro
	trigger_npc_sequence_tomorrow organ_boneyard_intro
	queue_cutscene_immediate dybbuk
	set_mapgen_flag BoneyardUnlocked
}
```

---

### `map_unlock_caves`
**Source:** `adventure_progression_unlocks.gon`  

```
map_unlock_caves {
	complete_chapter sewers
	trigger_npc_sequence_tomorrow frank_caves_intro
	queue_cutscene_immediate caves_intro
	set_mapgen_flag CavesUnlocked
}
```

---

### `map_unlock_desert`
**Source:** `adventure_progression_unlocks.gon`  

```
map_unlock_desert {
	complete_chapters [caves boneyard]
	trigger_npc_sequence_tomorrow jack_desert_intro
	queue_cutscene_immediate desert_intro
	set_mapgen_flag DesertUnlocked
}
```

---

### `map_unlock_bunker`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_BUNKER`: "You can now adventure to The Bunker!"

```
map_unlock_bunker {
	complete_chapter desert
	popup {
		prompt AREA_UNLOCK_BUNKER
		frame UnlockArea_Bunker
	}
	set_mapgen_flag BunkerUnlocked
}
```

---

### `map_unlock_crater`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_CRATER`: "You can now adventure to The Crater!"

```
map_unlock_crater {
	complete_chapter desert
	popup {
		prompt AREA_UNLOCK_CRATER
		frame UnlockArea_Crater
	}
	set_mapgen_flag CraterUnlocked
}
```

---

### `map_unlock_core`
**Source:** `adventure_progression_unlocks.gon`  

```
map_unlock_core {
	complete_chapter bunker
	queue_cutscene_immediate core_intro
	set_mapgen_flag CoreUnlocked
}
```

---

### `map_unlock_moon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_MOON`: "You can now adventure to The Moon!"

```
map_unlock_moon {
	complete_chapter crater
	queue_cutscene_immediate moon_intro
	/*popup {
		prompt AREA_UNLOCK_MOON
		frame UnlockArea_Moon
	}*/
	set_mapgen_flag MoonUnlocked
}
```

---

### `map_unlock_lab`
**Source:** `adventure_progression_unlocks.gon`  

```
map_unlock_lab {
	complete_chapters [core moon]
	set_savefile_flag PlotFlag_Beanies_Homeless
	queue_cutscene_immediate lab_intro
	trigger_npc_sequence beanies_lab_intro
	set_mapgen_flag LabUnlocked
}
```

---

### `map_unlock_iceage`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_ICEAGE`: "You can now adventure to the past!"

```
map_unlock_iceage {
	//complete_chapter lab
	popup {
		prompt AREA_UNLOCK_ICEAGE
		immediate true
		frame UnlockArea_IceAge
	}
	set_mapgen_flag IceAgeUnlocked
}
```

---

### `map_unlock_jurassic`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_JURASSIC`: "You can now adventure even further into the past!"

```
map_unlock_jurassic {
	complete_chapter iceage
	trigger_npc_sequence beanies_jurassic_intro
	queue_cutscene_immediate jurassic_intro


	/*popup {
		prompt AREA_UNLOCK_JURASSIC
		frame UnlockArea_Jurassic
	}*/
	set_mapgen_flag JurassicUnlocked
}
```

---

### `map_unlock_future`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_FUTURE`: "You can now adventure to the future!"

```
map_unlock_future {
	complete_chapter jurassic
	trigger_npc_sequence beanies_future_intro

	popup {
		prompt AREA_UNLOCK_FUTURE
		frame UnlockArea_Future
	}
	set_mapgen_flag FutureUnlocked
}
```

---

### `see_future_dialog_trigger`
**Source:** `adventure_progression_unlocks.gon`  

```
see_future_dialog_trigger {
	visit_chapter future
	trigger_npc_sequence beanies_seefuture
}
```

---

### `map_unlock_theend`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_THEEND`: "You can now adventure even further into the future!"

```
map_unlock_theend {
	complete_chapter future
	trigger_npc_sequence beanies_theend_intro
	queue_cutscene_immediate theend_intro

	/*popup {
		prompt AREA_UNLOCK_THEEND
		frame UnlockArea_TheEnd
	}*/
	set_mapgen_flag TheEndUnlocked
}
```

---

### `see_theend_dialog_trigger`
**Source:** `adventure_progression_unlocks.gon`  

```
see_theend_dialog_trigger {
	visit_chapter theend
	trigger_npc_sequence beanies_seetheend
}
```

---

### `houseboss_unlock_guillotina_1`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_guillotina_1 {
	complete_chapter boneyard
	trigger_house_boss guillotina_1
}
```

---

### `houseboss_unlock_guillotina_2`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_guillotina_2 {
	beat_house_boss guillotina_1
	trigger_house_boss guillotina_2
}
```

---

### `houseboss_unlock_guillotina_3`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_guillotina_3 {
	beat_house_boss guillotina_2
	trigger_house_boss guillotina_3
}
```

---

### `houseboss_unlock_pyrophina`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_pyrophina {
	complete_chapter core
	trigger_house_boss pyrophina
}
```

---

### `houseboss_unlock_zaratana`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_zaratana {
	complete_chapter moon
	trigger_house_boss zaratana
}
```

---

### `houseboss_unlock_kaijufighta`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_kaijufighta {
	beat_house_boss pyrophina
	require_beat_house_boss zaratana
	trigger_house_boss pyrophina_vs_zaratana
}
```

---

### `houseboss_unlock_kaijufightb`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_kaijufightb {
	beat_house_boss zaratana
	require_beat_house_boss pyrophina
	trigger_house_boss pyrophina_vs_zaratana
}
```

---

### `houseboss_unlock_terminator_1`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_terminator_1 {
	complete_chapter future
	trigger_house_boss terminator_1
}
```

---

### `houseboss_unlock_terminator_2`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_terminator_2 {
	beat_house_boss terminator_1
	trigger_house_boss terminator_2
}
```

---

### `houseboss_unlock_terminator_3`
**Source:** `adventure_progression_unlocks.gon`  

```
houseboss_unlock_terminator_3 {
	beat_house_boss terminator_2
	trigger_house_boss terminator_3
}
```

---

### `trigger_starcat_tip`
**Source:** `adventure_progression_unlocks.gon`  

```
trigger_starcat_tip {
	beat_house_boss any
	trigger_npc_sequence butch_first_house_boss_beat
}
```

---

### `npc_houseboss_intro_guillotina_1`
**Source:** `adventure_progression_unlocks.gon`  

```
npc_houseboss_intro_guillotina_1 {
	trigger_npc_sequence butch_tina1
}
```

---

### `npc_houseboss_intro_guillotina_2`
**Source:** `adventure_progression_unlocks.gon`  

```
npc_houseboss_intro_guillotina_2 {
	trigger_npc_sequence tink_tina2
}
```

---

### `npc_houseboss_intro_guillotina_3`
**Source:** `adventure_progression_unlocks.gon`  

```
npc_houseboss_intro_guillotina_3 {
	trigger_npc_sequence organ_tina3
}
```

---

### `npc_houseboss_intro_pyrophina`
**Source:** `adventure_progression_unlocks.gon`  

```
npc_houseboss_intro_pyrophina {
	trigger_npc_sequence butch_pyro
}
```

---

### `npc_houseboss_intro_zaratana`
**Source:** `adventure_progression_unlocks.gon`  

```
npc_houseboss_intro_zaratana {
	trigger_npc_sequence jack_zara
}
```

---

### `npc_houseboss_intro_pyrophina_vs_zaratana`
**Source:** `adventure_progression_unlocks.gon`  

```
npc_houseboss_intro_pyrophina_vs_zaratana {
	trigger_npc_sequence tracy_kaijufight
}
```

---

### `npc_houseboss_intro_terminator_1`
**Source:** `adventure_progression_unlocks.gon`  

```
npc_houseboss_intro_terminator_1 {
	trigger_npc_sequence tink_terminator
}
```

---

### `npc_houseboss_intro_terminator_2`
**Source:** `adventure_progression_unlocks.gon`  

```
npc_houseboss_intro_terminator_2 {
	trigger_npc_sequence frank_terminator2
}
```

---

### `npc_houseboss_intro_terminator_3`
**Source:** `adventure_progression_unlocks.gon`  

```
npc_houseboss_intro_terminator_3 {
	trigger_npc_sequence beanies_hitler3
}
```

---

### `quest_begin_gristle`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_THROBBINGGRISTLE`: ""Throbbing Gristle" found and added to Quest Items!"

```
quest_begin_gristle {
	beat_house_boss guillotina_1
	unlock_quest_item ThrobbingGristle
	popup {
		prompt QUEST_BEGIN_THROBBINGGRISTLE
		frame QuestUnlock_Gristle
	}
}
```

---

### `quest_begin_leech`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_PUTRIDLEECH`: ""Putrid Leech" found and added to Quest Items!"

```
quest_begin_leech {
	beat_house_boss guillotina_2
	unlock_quest_item PutridLeech
	popup {
		prompt QUEST_BEGIN_PUTRIDLEECH
		frame QuestUnlock_Leech
	}
}
```

---

### `quest_begin_tinahead`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_GUILLOTINASHEAD`: ""Guillotina's Head" found and added to Quest Items!"

```
quest_begin_tinahead {
	beat_house_boss guillotina_3
	unlock_quest_item GuillotinasHead
	popup {
		prompt QUEST_BEGIN_GUILLOTINASHEAD
		frame QuestUnlock_Head
	}
}
```

---

### `quest_begin_scaldingorb`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_SCALDINGORB`: ""Scalding Orb" found and added to Quest Items!"

```
quest_begin_scaldingorb {
	beat_house_boss pyrophina
	unlock_quest_item ScaldingOrb
	popup {
		prompt QUEST_BEGIN_SCALDINGORB
		frame QuestUnlock_Orb
	}
}
```

---

### `quest_begin_blackshard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_BLACKSHARD`: ""Black Shard" found and added to Quest Items!"

```
quest_begin_blackshard {
	beat_house_boss zaratana
	unlock_quest_item BlackShard
	popup {
		prompt QUEST_BEGIN_BLACKSHARD
		frame QuestUnlock_Shard
	}
}
```

---

### `quest_begin_pcollar`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_PYROPHINASCOLLAR`: "Pyrophina thanks you for helping her defeat Zaratana! <br/> "Pyrophina's Collar" added to Quest Items!"

```
quest_begin_pcollar {
	beat_house_boss pyrophina_vs_zaratana
	surviving_kaiju pyrophina
	unlock_quest_item PyrophinasCollar
	popup {
		prompt QUEST_BEGIN_PYROPHINASCOLLAR
		frame QuestUnlock_KaijuCollar
	}
}
```

---

### `quest_begin_zcollar`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_ZARATANASCOLLAR`: "Zaratana thanks you for helping her defeat Pyrophina! <br/> "Zaratana's Collar" added to Quest Items!"

```
quest_begin_zcollar {
	beat_house_boss pyrophina_vs_zaratana
	surviving_kaiju zaratana
	unlock_quest_item ZaratanasCollar
	popup {
		prompt QUEST_BEGIN_ZARATANASCOLLAR
		frame QuestUnlock_KaijuCollar
	}
}
```

---

### `quest_begin_receiver`
**Source:** `adventure_progression_unlocks.gon`  

```
quest_begin_receiver {
	beat_house_boss terminator_1
	trigger_npc_sequence beanies_terminator1_defeat
}
```

---

### `quest_begin_transmitter`
**Source:** `adventure_progression_unlocks.gon`  

```
quest_begin_transmitter {
	beat_house_boss terminator_2
	trigger_npc_sequence beanies_terminator2_defeat
}
```

---

### `quest_begin_amplifier`
**Source:** `adventure_progression_unlocks.gon`  

```
quest_begin_amplifier {
	beat_house_boss terminator_3
	trigger_npc_sequence beanies_hitler3_defeat
}
```

---

### `quest_begin_receiver2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_RECEIVER`: ""Receiver Antenna" found and added to Quest Items!"

```
quest_begin_receiver2 {
	unlock_quest_item ReceiverAntenna
	popup {
		prompt QUEST_BEGIN_RECEIVER
		frame QuestUnlock_Receiver
		immediate true
	}
}
```

---

### `quest_begin_transmitter2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_TRANSMITTER`: ""Transmitter Antenna" found and added to Quest Items!"

```
quest_begin_transmitter2 {
	unlock_quest_item TransmitterAntenna
	popup {
		prompt QUEST_BEGIN_TRANSMITTER
		frame QuestUnlock_Transmitter
		immediate true
	}
}
```

---

### `quest_begin_amplifier2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_AMPLIFIER`: ""Signal Amplifier" found and added to Quest Items!"

```
quest_begin_amplifier2 {
	unlock_quest_item SignalAmplifier
	popup {
		prompt QUEST_BEGIN_AMPLIFIER
		frame QuestUnlock_Amplifier
		immediate true
	}
}
```

---

### `time_machine_quest_trigger`
**Source:** `adventure_progression_unlocks.gon`  

```
time_machine_quest_trigger {
	trigger_npc_sequence beanies_timemachine_intro
}
```

---

### `time_machine_quest_begin`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_COOLER`: ""Cryogenic Time Chamber" added to Quest Items!"

```
time_machine_quest_begin {
	unlock_quest_item CryogenicTimeChamber_Empty

	popup {
		prompt QUEST_BEGIN_COOLER
		immediate true
		frame QuestUnlock_Cooler
	}
}
```

---

### `time_machine_quest_finalstep`
**Source:** `adventure_progression_unlocks.gon`  

```
time_machine_quest_finalstep {
	trigger_npc_sequence beanies_timemachine_2
}
```

---

### `meat_world_unlock`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_MEATWORLD`: "You can now adventure to The Throbbing Domain!"

```
meat_world_unlock {
	set_mapgen_flag MeatWorldUnlocked
	trigger_npc_sequence organ_throbbingdomain_intro

	popup {
		prompt AREA_UNLOCK_MEATWORLD
		immediate true
		frame UnlockArea_Meatworld
	}
}
```

---

### `meat_world_open`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_MEATWORLDFULL`: "The Throbbing King requests your audience. You now have full access to his domain!"

```
meat_world_open {
	set_mapgen_flag MeatWorldUnlockedFull

	/*popup {
		prompt AREA_UNLOCK_MEATWORLDFULL
		immediate true
		frame UnlockArea_Meatworld
	}*/
}
```

---

### `map_unlock_dimensionx`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_THERIFT`: "You can now adventure to The Rift!"

```
map_unlock_dimensionx {
	set_mapgen_flag DimensionXUnlocked

	/*popup {
		prompt AREA_UNLOCK_THERIFT
		immediate true
		frame AreaUnlock_Rift
	}*/
}
```

---

### `moon_obelisk`
**Source:** `adventure_progression_unlocks.gon`  

```
moon_obelisk {
	complete_item_quest ScaldingOrb
	set_mapgen_flag MoonObeliskUnlocked
	post_combat_cutscene obelisk1_moon
}
```

---

### `core_obelisk`
**Source:** `adventure_progression_unlocks.gon`  

```
core_obelisk {
	complete_item_quest BlackShard
	set_mapgen_flag CoreObeliskUnlocked
	post_combat_cutscene obelisk1_core
}
```

---

### `moon_obelisk2`
**Source:** `adventure_progression_unlocks.gon`  

```
moon_obelisk2 {
	complete_item_quest ScaldingOrb
	require_mapgen_flag CoreObeliskUnlocked
	set_mapgen_flag BothObelisksUnlocked
	post_combat_cutscene obelisk2_moon
}
```

---

### `core_obelisk2`
**Source:** `adventure_progression_unlocks.gon`  

```
core_obelisk2 {
	complete_item_quest BlackShard
	require_mapgen_flag MoonObeliskUnlocked
	set_mapgen_flag BothObelisksUnlocked
	post_combat_cutscene obelisk2_core
}
```

---

### `end_of_time_unlock`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_ENDOFTIME`: "The time machine can now travel to The Infinite!"

```
end_of_time_unlock {
	set_mapgen_flag EndOfTimeUnlocked

	/*popup {
		prompt AREA_UNLOCK_ENDOFTIME
		immediate true
		frame AreaUnlock_Infinite
	}*/
}
```

---

### `nuke_quest_begin`
**Source:** `adventure_progression_unlocks.gon`  

```
nuke_quest_begin {
	complete_chapter endoftime
	trigger_npc_sequence beanies_bombquest_begin

	preempt_npc_sequence beanies_bombquest_amnesia
}
```

---

### `nuke_quest_jar1`
**Source:** `adventure_progression_unlocks.gon`  

```
nuke_quest_jar1 {
	complete_item_quest JarOfRadiation
	repeatable true
	trigger_npc_sequence beanies_bombquest_2 //this one is optional to see and should be cleared if you progess past it or fail the quest
}
```

---

### `nuke_quest_jar2`
**Source:** `adventure_progression_unlocks.gon`  

```
nuke_quest_jar2 {
	complete_item_quest JarOfRadiatedBlood
	repeatable true
	trigger_npc_sequence beanies_bombquest_3

	preempt_npc_sequence beanies_bombquest_2
}
```

---

### `fail_nuke1`
**Source:** `adventure_progression_unlocks.gon`  

```
fail_nuke1 {
	fail_item_quest JarOfRadiation
	repeatable true
	trigger_npc_sequence beanies_bombquest_fail_jarofradiation
}
```

---

### `fail_nuke2`
**Source:** `adventure_progression_unlocks.gon`  

```
fail_nuke2 {
	fail_item_quest JarOfRadiatedBlood
	repeatable true
	trigger_npc_sequence beanies_bombquest_fail_jarofblood

	preempt_npc_sequence beanies_bombquest_2
	preempt_npc_sequence beanies_bombquest_3
}
```

---

### `fail_nuke3`
**Source:** `adventure_progression_unlocks.gon`  

```
fail_nuke3 {
	fail_item_quest JarOfChaos
	repeatable true
	trigger_npc_sequence beanies_bombquest_fail_jarofchaos

	preempt_npc_sequence beanies_bombquest_2
	preempt_npc_sequence beanies_bombquest_3
}
```

---

### `fail_nuke4`
**Source:** `adventure_progression_unlocks.gon`  

```
fail_nuke4 {
	fail_item_quest Nuke
	repeatable true
	trigger_npc_sequence beanies_bombquest_fail_nuke
}
```

---

### `reset_nuke_quest`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_JAR`: ""Jar of Radiation!" added to Quest Items!"

```
reset_nuke_quest { //manually triggered via dialog
	repeatable true

	unlock_quest_item JarOfRadiation

	popup {
		prompt QUEST_BEGIN_JAR
		immediate true
		frame QuestUnlock_Jar
	}

	reset_npc_sequence beanies_bombquest_2
	reset_npc_sequence beanies_bombquest_3
	reset_npc_sequence beanies_bombquest_fail_jarofradiation
	reset_npc_sequence beanies_bombquest_fail_jarofblood
	reset_npc_sequence beanies_bombquest_fail_jarofchaos
	reset_npc_sequence beanies_bombquest_fail_nuke
	reset_npc_sequence beanies_bombquest_amnesia
}
```

---

### `nuke_quest_get_nuke`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `QUEST_BEGIN_NUKE`: ""Nuke" added to Quest Items!"

```
nuke_quest_get_nuke { //manually triggered via dialog
	finish_quest JarOfChaos //this one ("finish_quest") means "trigger finishing this quest" not "this triggers when the quest is done" (which would be the "complete_item_quest" condition)
	unlock_quest_item Nuke

	repeatable true

	popup {
		prompt QUEST_BEGIN_NUKE
		immediate true
		frame QuestUnlock_Nuke
	}
}
```

---

### `nuke_quest_complete`
**Source:** `adventure_progression_unlocks.gon`  

```
nuke_quest_complete {
	complete_item_quest Nuke

	repeatable true

	set_savefile_flag PlotFlag_FrankBeanies
	trigger_npc_sequence frank_ending
	trigger_npc_sequence beanies_bombquest_amnesia
	trigger_npc_sequence steven_postendgame

	//reset_unlock nuke_quest_begin //killing God again normally can trigger the nuke quest a second time
	//reset_npc_sequence beanies_bombquest_begin

	increment_savefile_counter GameStat_CountNukeQuestCompletions
}
```

---

### `nuke_quest_loop`
**Source:** `adventure_progression_unlocks.gon`  

```
nuke_quest_loop {
	repeatable true

	reset_unlock nuke_quest_begin //killing God again normally can trigger the nuke quest a second time
	reset_npc_sequence beanies_bombquest_begin
}
```

---

### `class_unlock_fighter_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_FIGHTER`: "Fighters can now learn "Pawbreaker"!"

```
class_unlock_fighter_ability {
	complete_chapter_with_class [caves Fighter]
	popup {
		prompt ABILITY_UNLOCK_FIGHTER
		immediate true
	}
	unlock_ability Pawbreaker
}
```

---

### `class_unlock_hunter_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_HUNTER`: "Hunters can now learn "Ball of Spiders"!"

```
class_unlock_hunter_ability {
	complete_chapter_with_class [caves Hunter]
	popup {
		prompt ABILITY_UNLOCK_HUNTER
		immediate true
	}
	unlock_ability BallOfSpiders
}
```

---

### `class_unlock_mage_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_MAGE`: "Mages can now learn "Hyper Beam"!"

```
class_unlock_mage_ability {
	complete_chapter_with_class [caves Mage]
	popup {
		prompt ABILITY_UNLOCK_MAGE
		immediate true
	}
	unlock_ability HyperBeam
}
```

---

### `class_unlock_medic_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_MEDIC`: "Clerics can now learn "Ethereal""

```
class_unlock_medic_ability {
	complete_chapter_with_class [caves Medic]
	popup {
		prompt ABILITY_UNLOCK_MEDIC
		immediate true
	}
	unlock_ability Ethereal
}
```

---

### `class_unlock_thief_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_THIEF`: "Thieves can now learn "Nail Flurry"!"

```
class_unlock_thief_ability {
	complete_chapter_with_class [caves Thief]
	popup {
		prompt ABILITY_UNLOCK_THIEF
		immediate true
	}
	unlock_ability NailFlurry
}
```

---

### `class_unlock_tank_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_TANK`: "Tanks can now learn "Suplex"!"

```
class_unlock_tank_ability {
	complete_chapter_with_class [caves Tank]
	popup {
		prompt ABILITY_UNLOCK_TANK
		immediate true
	}
	unlock_ability Suplex
}
```

---

### `class_unlock_necro_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_NECROMANCER`: "Necromancers can now learn "Summon Shade"!"

```
class_unlock_necro_ability {
	complete_chapter_with_class [caves Necromancer]
	popup {
		prompt ABILITY_UNLOCK_NECROMANCER
		immediate true
	}
	unlock_ability SummonShade
}
```

---

### `class_unlock_psychic_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_PSYCHIC`: "Psychics can now learn "Supernova"!"

```
class_unlock_psychic_ability {
	complete_chapter_with_class [caves Psychic]
	popup {
		prompt ABILITY_UNLOCK_PSYCHIC
		immediate true
	}
	unlock_ability Supernova
}
```

---

### `class_unlock_tinkerer_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_TINKERER`: "Tinkerers can now learn "Mech Suit"!"

```
class_unlock_tinkerer_ability {
	complete_chapter_with_class [caves Tinkerer]
	popup {
		prompt ABILITY_UNLOCK_TINKERER
		immediate true
	}
	unlock_ability MechSuit
}
```

---

### `class_unlock_butcher_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_BUTCHER`: "Butchers can now learn "Slice and Dice"!"

```
class_unlock_butcher_ability {
	complete_chapter_with_class [caves Butcher]
	popup {
		prompt ABILITY_UNLOCK_BUTCHER
		immediate true
	}
	unlock_ability SliceAndDice
}
```

---

### `class_unlock_druid_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_DRUID`: "Druids can now learn "Summon Bear"!"

```
class_unlock_druid_ability {
	complete_chapter_with_class [caves Druid]
	popup {
		prompt ABILITY_UNLOCK_DRUID
		immediate true
	}
	unlock_ability SummonBear
}
```

---

### `class_unlock_monk_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_MONK`: "Monks can now learn "Hundred Hand Slap"!"

```
class_unlock_monk_ability {
	complete_chapter_with_class [caves Monk]
	popup {
		prompt ABILITY_UNLOCK_MONK
		immediate true
	}
	unlock_ability HundredHandSlap
}
```

---

### `class_unlock_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_COLORLESS`: "All cats can now learn "Metronome"!"

```
class_unlock_colorless_ability {
	complete_chapter_with_class [caves Colorless]
	popup {
		prompt ABILITY_UNLOCK_COLORLESS
		immediate true
	}
	unlock_ability Metronome
}
```

---

### `class_unlock_jester_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_JESTER`: "Jesters have some more tricks up their sleeves!"

```
class_unlock_jester_ability {
	complete_chapter_with_class [caves Jester]
	popup {
		prompt ABILITY_UNLOCK_JESTER
		immediate true
	}
	unlock_ability SmartMetronome
	unlock_ability RNGCannon
	unlock_ability Bump
	unlock_ability PowerUp
}
```

---

### `class_unlock_fighter_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_FIGHTER`: "Fighters can now learn "Dual Wield"!"

```
class_unlock_fighter_passive {
	complete_chapter_with_class [boneyard Fighter]
	popup {
		prompt PASSIVE_UNLOCK_FIGHTER
		immediate true
	}
	unlock_passive DualWield
}
```

---

### `class_unlock_hunter_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_HUNTER`: "Hunters can now learn "Thrill of the Hunt"!"

```
class_unlock_hunter_passive {
	complete_chapter_with_class [boneyard Hunter]
	popup {
		prompt PASSIVE_UNLOCK_HUNTER
		immediate true
	}
	unlock_passive ThrillOfTheHunt
}
```

---

### `class_unlock_mage_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_MAGE`: "Mages can now learn "Three"!"

```
class_unlock_mage_passive {
	complete_chapter_with_class [boneyard Mage]
	popup {
		prompt PASSIVE_UNLOCK_MAGE
		immediate true
	}
	unlock_passive EnergyStorm
}
```

---

### `class_unlock_medic_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_MEDIC`: "Clerics can now learn "Evil Patron"!"

```
class_unlock_medic_passive {
	complete_chapter_with_class [boneyard Medic]
	popup {
		prompt PASSIVE_UNLOCK_MEDIC
		immediate true
	}
	unlock_passive EvilPatron
}
```

---

### `class_unlock_thief_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_THIEF`: "Thieves can now learn "First Strike"!"

```
class_unlock_thief_passive {
	complete_chapter_with_class [boneyard Thief]
	popup {
		prompt PASSIVE_UNLOCK_THIEF
		immediate true
	}
	unlock_passive AlphaStrike
}
```

---

### `class_unlock_tank_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_TANK`: "Tanks can now learn "Bouncer"!"

```
class_unlock_tank_passive {
	complete_chapter_with_class [boneyard Tank]
	popup {
		prompt PASSIVE_UNLOCK_TANK
		immediate true
	}
	unlock_passive Bouncer
}
```

---

### `class_unlock_necro_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_NECROMANCER`: "Necromancers can now learn "Servus Mortem"!"

```
class_unlock_necro_passive {
	complete_chapter_with_class [boneyard Necromancer]
	popup {
		prompt PASSIVE_UNLOCK_NECROMANCER
		immediate true
	}
	unlock_passive DeathIncarnate
}
```

---

### `class_unlock_psychic_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_PSYCHIC`: "Psychics can now learn "Gravity Well"!"

```
class_unlock_psychic_passive {
	complete_chapter_with_class [boneyard Psychic]
	popup {
		prompt PASSIVE_UNLOCK_PSYCHIC
		immediate true
	}
	unlock_passive GravityWell
}
```

---

### `class_unlock_tinkerer_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_TINKERER`: "Tinkerers can now learn "Armor Specialist"!"

```
class_unlock_tinkerer_passive {
	complete_chapter_with_class [boneyard Tinkerer]
	popup {
		prompt PASSIVE_UNLOCK_TINKERER
		immediate true
	}
	unlock_passive ArmorSpecialist
}
```

---

### `class_unlock_butcher_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_BUTCHER`: "Butchers can now learn "Indigestion"!"

```
class_unlock_butcher_passive {
	complete_chapter_with_class [boneyard Butcher]
	popup {
		prompt PASSIVE_UNLOCK_BUTCHER
		immediate true
	}
	unlock_passive Indigestion
}
```

---

### `class_unlock_druid_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_DRUID`: "Druids can now learn "Suicide Squad"!"

```
class_unlock_druid_passive {
	complete_chapter_with_class [boneyard Druid]
	popup {
		prompt PASSIVE_UNLOCK_DRUID
		immediate true
	}
	unlock_passive SuicideSquad
}
```

---

### `class_unlock_monk_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_MONK`: "Monks can now learn "Unstoppable"!"

```
class_unlock_monk_passive {
	complete_chapter_with_class [boneyard Monk]
	popup {
		prompt PASSIVE_UNLOCK_MONK
		immediate true
	}
	unlock_passive Unstoppable
}
```

---

### `class_unlock_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_COLORLESS`: "All cats can now learn "Skill Share"!"

```
class_unlock_colorless_passive {
	complete_chapter_with_class [boneyard Colorless]
	popup {
		prompt PASSIVE_UNLOCK_COLORLESS
		immediate true
	}
	unlock_passive SkillShare
}
```

---

### `class_unlock_jester_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_JESTER`: "Jesters have some more tricks up their sleeves!"

```
class_unlock_jester_passive {
	complete_chapter_with_class [boneyard Jester]
	popup {
		prompt PASSIVE_UNLOCK_JESTER
		immediate true
	}
	unlock_passive SuperLuck
    unlock_passive Goofball
}
```

---

### `class_unlock_fighter_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_FIGHTER_COLORLESS`: "All cats can now learn "Path of the Fighter"!"

```
class_unlock_fighter_colorless_ability {
	complete_chapter_with_class [core Fighter]
	popup {
		prompt ABILITY_UNLOCK_FIGHTER_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheFighter
}
```

---

### `class_unlock_hunter_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_HUNTER_COLORLESS`: "All cats can now learn "Path of the Hunter"!"

```
class_unlock_hunter_colorless_ability {
	complete_chapter_with_class [core Hunter]
	popup {
		prompt ABILITY_UNLOCK_HUNTER_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheHunter
}
```

---

### `class_unlock_mage_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_MAGE_COLORLESS`: "All cats can now learn "Path of the Mage"!"

```
class_unlock_mage_colorless_ability {
	complete_chapter_with_class [core Mage]
	popup {
		prompt ABILITY_UNLOCK_MAGE_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheMage
}
```

---

### `class_unlock_medic_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_MEDIC_COLORLESS`: "All cats can now learn "Path of the Cleric"!"

```
class_unlock_medic_colorless_ability {
	complete_chapter_with_class [core Medic]
	popup {
		prompt ABILITY_UNLOCK_MEDIC_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheCleric
}
```

---

### `class_unlock_thief_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_THIEF_COLORLESS`: "All cats can now learn "Path of the Thief"!"

```
class_unlock_thief_colorless_ability {
	complete_chapter_with_class [core Thief]
	popup {
		prompt ABILITY_UNLOCK_THIEF_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheThief
}
```

---

### `class_unlock_tank_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_TANK_COLORLESS`: "All cats can now learn "Path of the Tank"!"

```
class_unlock_tank_colorless_ability {
	complete_chapter_with_class [core Tank]
	popup {
		prompt ABILITY_UNLOCK_TANK_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheTank
}
```

---

### `class_unlock_necro_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_NECROMANCER_COLORLESS`: "All cats can now learn "Path of the Necromancer"!"

```
class_unlock_necro_colorless_ability {
	complete_chapter_with_class [core Necromancer]
	popup {
		prompt ABILITY_UNLOCK_NECROMANCER_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheNecromancer
}
```

---

### `class_unlock_psychic_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_PSYCHIC_COLORLESS`: "All cats can now learn "Path of the Psychic"!"

```
class_unlock_psychic_colorless_ability {
	complete_chapter_with_class [core Psychic]
	popup {
		prompt ABILITY_UNLOCK_PSYCHIC_COLORLESS
		immediate true
	}
	unlock_ability PathOfThePsychic
}
```

---

### `class_unlock_tinkerer_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_TINKERER_COLORLESS`: "All cats can now learn "Path of the Tinkerer"!"

```
class_unlock_tinkerer_colorless_ability {
	complete_chapter_with_class [core Tinkerer]
	popup {
		prompt ABILITY_UNLOCK_TINKERER_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheTinkerer
}
```

---

### `class_unlock_butcher_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_BUTCHER_COLORLESS`: "All cats can now learn "Path of the Butcher"!"

```
class_unlock_butcher_colorless_ability {
	complete_chapter_with_class [core Butcher]
	popup {
		prompt ABILITY_UNLOCK_BUTCHER_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheButcher
}
```

---

### `class_unlock_druid_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_DRUID_COLORLESS`: "All cats can now learn "Path of the Druid"!"

```
class_unlock_druid_colorless_ability {
	complete_chapter_with_class [core Druid]
	popup {
		prompt ABILITY_UNLOCK_DRUID_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheDruid
}
```

---

### `class_unlock_monk_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_MONK_COLORLESS`: "All cats can now learn "Path of the Monk"!"

```
class_unlock_monk_colorless_ability {
	complete_chapter_with_class [core Monk]
	popup {
		prompt ABILITY_UNLOCK_MONK_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheMonk
}
```

---

### `class_unlock_colorless_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_COLORLESS_COLORLESS`: "All cats can now learn "Path of the Void"!"

```
class_unlock_colorless_colorless_ability {
	complete_chapter_with_class [core Colorless]
	popup {
		prompt ABILITY_UNLOCK_COLORLESS_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheVoid
}
```

---

### `class_unlock_jester_colorless_ability`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ABILITY_UNLOCK_JESTER_COLORLESS`: "All cats can now learn "Path of the Jester"!"

```
class_unlock_jester_colorless_ability {
	complete_chapter_with_class [core Jester]
	popup {
		prompt ABILITY_UNLOCK_JESTER_COLORLESS
		immediate true
	}
	unlock_ability PathOfTheJester
}
```

---

### `class_unlock_fighter_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_FIGHTER_COLORLESS`: "All cats can now learn "Fighter's Soul"!"

```
class_unlock_fighter_colorless_passive {
	complete_chapter_with_class [moon Fighter]
	popup {
		prompt PASSIVE_UNLOCK_FIGHTER_COLORLESS
		immediate true
	}
	unlock_passive FightersSoul
}
```

---

### `class_unlock_hunter_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_HUNTER_COLORLESS`: "All cats can now learn "Hunter's Soul"!"

```
class_unlock_hunter_colorless_passive {
	complete_chapter_with_class [moon Hunter]
	popup {
		prompt PASSIVE_UNLOCK_HUNTER_COLORLESS
		immediate true
	}
	unlock_passive HuntersSoul
}
```

---

### `class_unlock_mage_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_MAGE_COLORLESS`: "All cats can now learn "Mage's Soul"!"

```
class_unlock_mage_colorless_passive {
	complete_chapter_with_class [moon Mage]
	popup {
		prompt PASSIVE_UNLOCK_MAGE_COLORLESS
		immediate true
	}
	unlock_passive MagesSoul
}
```

---

### `class_unlock_medic_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_MEDIC_COLORLESS`: "All cats can now learn "Cleric's Soul"!"

```
class_unlock_medic_colorless_passive {
	complete_chapter_with_class [moon Medic]
	popup {
		prompt PASSIVE_UNLOCK_MEDIC_COLORLESS
		immediate true
	}
	unlock_passive ClericsSoul
}
```

---

### `class_unlock_thief_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_THIEF_COLORLESS`: "All cats can now learn "Thief's Soul"!"

```
class_unlock_thief_colorless_passive {
	complete_chapter_with_class [moon Thief]
	popup {
		prompt PASSIVE_UNLOCK_THIEF_COLORLESS
		immediate true
	}
	unlock_passive ThiefsSoul
}
```

---

### `class_unlock_tank_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_TANK_COLORLESS`: "All cats can now learn "Tank's Soul"!"

```
class_unlock_tank_colorless_passive {
	complete_chapter_with_class [moon Tank]
	popup {
		prompt PASSIVE_UNLOCK_TANK_COLORLESS
		immediate true
	}
	unlock_passive TanksSoul
}
```

---

### `class_unlock_necro_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_NECROMANCER_COLORLESS`: "All cats can now learn "Necromancer's Soul"!"

```
class_unlock_necro_colorless_passive {
	complete_chapter_with_class [moon Necromancer]
	popup {
		prompt PASSIVE_UNLOCK_NECROMANCER_COLORLESS
		immediate true
	}
	unlock_passive NecromancersSoul
}
```

---

### `class_unlock_psychic_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_PSYCHIC_COLORLESS`: "All cats can now learn "Psychic's Soul"!"

```
class_unlock_psychic_colorless_passive {
	complete_chapter_with_class [moon Psychic]
	popup {
		prompt PASSIVE_UNLOCK_PSYCHIC_COLORLESS
		immediate true
	}
	unlock_passive PsychicsSoul
}
```

---

### `class_unlock_tinkerer_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_TINKERER_COLORLESS`: "All cats can now learn "Tinkerer's Soul"!"

```
class_unlock_tinkerer_colorless_passive {
	complete_chapter_with_class [moon Tinkerer]
	popup {
		prompt PASSIVE_UNLOCK_TINKERER_COLORLESS
		immediate true
	}
	unlock_passive TinkerersSoul
}
```

---

### `class_unlock_butcher_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_BUTCHER_COLORLESS`: "All cats can now learn "Butcher's Soul"!"

```
class_unlock_butcher_colorless_passive {
	complete_chapter_with_class [moon Butcher]
	popup {
		prompt PASSIVE_UNLOCK_BUTCHER_COLORLESS
		immediate true
	}
	unlock_passive ButchersSoul
}
```

---

### `class_unlock_druid_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_DRUID_COLORLESS`: "All cats can now learn "Druid's Soul"!"

```
class_unlock_druid_colorless_passive {
	complete_chapter_with_class [moon Druid]
	popup {
		prompt PASSIVE_UNLOCK_DRUID_COLORLESS
		immediate true
	}
	unlock_passive DruidsSoul
}
```

---

### `class_unlock_monk_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_MONK_COLORLESS`: "All cats can now learn "Monk's Soul"!"

```
class_unlock_monk_colorless_passive {
	complete_chapter_with_class [moon Monk]
	popup {
		prompt PASSIVE_UNLOCK_MONK_COLORLESS
		immediate true
	}
	unlock_passive MonksSoul
}
```

---

### `class_unlock_colorless_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_COLORLESS_COLORLESS`: "All cats can now learn "Void Soul"!"

```
class_unlock_colorless_colorless_passive {
	complete_chapter_with_class [moon Colorless]
	popup {
		prompt PASSIVE_UNLOCK_COLORLESS_COLORLESS
		immediate true
	}
	unlock_passive VoidSoul
}
```

---

### `class_unlock_jester_colorless_passive`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `PASSIVE_UNLOCK_JESTER_COLORLESS`: "All cats can now learn "Jester's Soul"!"

```
class_unlock_jester_colorless_passive {
	complete_chapter_with_class [moon Jester]
	popup {
		prompt PASSIVE_UNLOCK_JESTER_COLORLESS
		immediate true
	}
	unlock_passive JestersSoul
}
```

---

### `class_unlock_fighter_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_fighter_weapon {
	complete_chapter_with_class [jurassic Fighter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate BattleAxe
}
```

---

### `class_unlock_hunter_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_hunter_weapon {
	complete_chapter_with_class [jurassic Hunter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate InfinityArrow
}
```

---

### `class_unlock_mage_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_mage_weapon {
	complete_chapter_with_class [jurassic Mage]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StaffOfFlame
}
```

---

### `class_unlock_medic_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_medic_weapon {
	complete_chapter_with_class [jurassic Medic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate AnointingOil
}
```

---

### `class_unlock_thief_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_thief_weapon {
	complete_chapter_with_class [jurassic Thief]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate LacedNeedle
}
```

---

### `class_unlock_tank_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tank_weapon {
	complete_chapter_with_class [jurassic Tank]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate Girder
}
```

---

### `class_unlock_necro_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_necro_weapon {
	complete_chapter_with_class [jurassic Necromancer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate UnderworldStaff
}
```

---

### `class_unlock_psychic_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_psychic_weapon {
	complete_chapter_with_class [jurassic Psychic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate BentSpoon
}
```

---

### `class_unlock_tinkerer_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tinkerer_weapon {
	complete_chapter_with_class [jurassic Tinkerer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate BallPeenHammer
}
```

---

### `class_unlock_butcher_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_butcher_weapon {
	complete_chapter_with_class [jurassic Butcher]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ButchersCleaver
}
```

---

### `class_unlock_druid_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_druid_weapon {
	complete_chapter_with_class [jurassic Druid]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate RainStaff
}
```

---

### `class_unlock_monk_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_monk_weapon {
	complete_chapter_with_class [jurassic Monk]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate Bo
}
```

---

### `class_unlock_colorless_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_colorless_weapon {
	complete_chapter_with_class [jurassic Colorless]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate LilKitty
}
```

---

### `class_unlock_jester_weapon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_jester_weapon {
	complete_chapter_with_class [jurassic Jester]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate NinnyStick
}
```

---

### `class_unlock_fighter_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_fighter_trinket {
	complete_chapter_with_class [theend Fighter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate RageJuice
}
```

---

### `class_unlock_hunter_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_hunter_trinket {
	complete_chapter_with_class [theend Hunter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate HuntersFlute
}
```

---

### `class_unlock_mage_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_mage_trinket {
	complete_chapter_with_class [theend Mage]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate RingOfFrost
}
```

---

### `class_unlock_medic_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_medic_trinket {
	complete_chapter_with_class [theend Medic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate HolyWater
}
```

---

### `class_unlock_thief_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_thief_trinket {
	complete_chapter_with_class [theend Thief]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate LuckyCoinPurse
}
```

---

### `class_unlock_tank_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tank_trinket {
	complete_chapter_with_class [theend Tank]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TankJuice
}
```

---

### `class_unlock_necro_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_necro_trinket {
	complete_chapter_with_class [theend Necromancer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate SatanicBible
}
```

---

### `class_unlock_psychic_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_psychic_trinket {
	complete_chapter_with_class [theend Psychic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TarotDeck
}
```

---

### `class_unlock_tinkerer_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tinkerer_trinket {
	complete_chapter_with_class [theend Tinkerer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ScrapBag
}
```

---

### `class_unlock_butcher_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_butcher_trinket {
	complete_chapter_with_class [theend Butcher]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate Cookbook
}
```

---

### `class_unlock_druid_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_druid_trinket {
	complete_chapter_with_class [theend Druid]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate DruidsWhistle
}
```

---

### `class_unlock_monk_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_monk_trinket {
	complete_chapter_with_class [theend Monk]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate EmptyHand
}
```

---

### `class_unlock_colorless_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_colorless_trinket {
	complete_chapter_with_class [theend Colorless]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate BallOfYarn
}
```

---

### `class_unlock_jester_trinket`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_jester_trinket {
	complete_chapter_with_class [theend Jester]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ToyGun
}
```

---

### `class_unlock_fighter_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_fighter_helmet {
	complete_chapter_with_class [meatworld Fighter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate FighterHelm
}
```

---

### `class_unlock_hunter_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_hunter_helmet {
	complete_chapter_with_class [meatworld Hunter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate HunterCap
}
```

---

### `class_unlock_mage_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_mage_helmet {
	complete_chapter_with_class [meatworld Mage]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate MageHat
}
```

---

### `class_unlock_medic_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_medic_helmet {
	complete_chapter_with_class [meatworld Medic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ClericHat
}
```

---

### `class_unlock_thief_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_thief_helmet {
	complete_chapter_with_class [meatworld Thief]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ThiefHood
}
```

---

### `class_unlock_tank_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tank_helmet {
	complete_chapter_with_class [meatworld Tank]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TankHelmet
}
```

---

### `class_unlock_necro_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_necro_helmet {
	complete_chapter_with_class [meatworld Necromancer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate SpiderHat
}
```

---

### `class_unlock_psychic_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_psychic_helmet {
	complete_chapter_with_class [meatworld Psychic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TinfoilHat
}
```

---

### `class_unlock_tinkerer_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tinkerer_helmet {
	complete_chapter_with_class [meatworld Tinkerer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ScrappersHat
}
```

---

### `class_unlock_butcher_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_butcher_helmet {
	complete_chapter_with_class [meatworld Butcher]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate FleshShroud
}
```

---

### `class_unlock_druid_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_druid_helmet {
	complete_chapter_with_class [meatworld Druid]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate MushroomHat
}
```

---

### `class_unlock_monk_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_monk_helmet {
	complete_chapter_with_class [meatworld Monk]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate HeadBrand
}
```

---

### `class_unlock_colorless_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_colorless_helmet {
	complete_chapter_with_class [meatworld Colorless]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate CatEars
}
```

---

### `class_unlock_jester_helmet`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_jester_helmet {
	complete_chapter_with_class [meatworld Jester]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate CapAndBells
}
```

---

### `class_unlock_fighter_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_fighter_face {
	complete_chapter_with_class [dimensionx Fighter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate FighterScar
}
```

---

### `class_unlock_hunter_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_hunter_face {
	complete_chapter_with_class [dimensionx Hunter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate HunterMonocle
}
```

---

### `class_unlock_mage_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_mage_face {
	complete_chapter_with_class [dimensionx Mage]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate MageRobe
}
```

---

### `class_unlock_medic_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_medic_face {
	complete_chapter_with_class [dimensionx Medic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ClericTears
}
```

---

### `class_unlock_thief_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_thief_face {
	complete_chapter_with_class [dimensionx Thief]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ThiefTattoo
}
```

---

### `class_unlock_tank_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tank_face {
	complete_chapter_with_class [dimensionx Tank]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TankTattoo
}
```

---

### `class_unlock_necro_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_necro_face {
	complete_chapter_with_class [dimensionx Necromancer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate DeathMask
}
```

---

### `class_unlock_psychic_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_psychic_face {
	complete_chapter_with_class [dimensionx Psychic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate MysticEye
}
```

---

### `class_unlock_tinkerer_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tinkerer_face {
	complete_chapter_with_class [dimensionx Tinkerer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ScrappersMask
}
```

---

### `class_unlock_butcher_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_butcher_face {
	complete_chapter_with_class [dimensionx Butcher]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate IronJaw
}
```

---

### `class_unlock_druid_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_druid_face {
	complete_chapter_with_class [dimensionx Druid]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate GreenmanMask
}
```

---

### `class_unlock_monk_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_monk_face {
	complete_chapter_with_class [dimensionx Monk]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate FaceBrand
}
```

---

### `class_unlock_colorless_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_colorless_face {
	complete_chapter_with_class [dimensionx Colorless]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate CatWhiskers
}
```

---

### `class_unlock_jester_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_jester_face {
	complete_chapter_with_class [dimensionx Jester]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ClownMakeup
}
```

---

### `class_unlock_fighter_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_fighter_neck {
	complete_chapter_with_class [endoftime Fighter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate FighterShoulderPad
}
```

---

### `class_unlock_hunter_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_hunter_neck {
	complete_chapter_with_class [endoftime Hunter]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate HunterQuiver
}
```

---

### `class_unlock_mage_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_mage_neck {
	complete_chapter_with_class [endoftime Mage]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate MageScarf
}
```

---

### `class_unlock_medic_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_medic_neck {
	complete_chapter_with_class [endoftime Medic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ClericRelic
}
```

---

### `class_unlock_thief_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_thief_neck {
	complete_chapter_with_class [endoftime Thief]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ThiefCloak
}
```

---

### `class_unlock_tank_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tank_neck {
	complete_chapter_with_class [endoftime Tank]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TankPads
}
```

---

### `class_unlock_necro_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_necro_neck {
	complete_chapter_with_class [endoftime Necromancer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate LeechNecklace
}
```

---

### `class_unlock_psychic_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_psychic_neck {
	complete_chapter_with_class [endoftime Psychic]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate DivinersCloth
}
```

---

### `class_unlock_tinkerer_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tinkerer_neck {
	complete_chapter_with_class [endoftime Tinkerer]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ScrappersBackpack
}
```

---

### `class_unlock_butcher_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_butcher_neck {
	complete_chapter_with_class [endoftime Butcher]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate HookedNecklace
}
```

---

### `class_unlock_druid_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_druid_neck {
	complete_chapter_with_class [endoftime Druid]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate RingOfMushrooms
}
```

---

### `class_unlock_monk_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_monk_neck {
	complete_chapter_with_class [endoftime Monk]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate PrayerBeads
}
```

---

### `class_unlock_colorless_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_colorless_neck {
	complete_chapter_with_class [endoftime Colorless]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate CatCollar
}
```

---

### `class_unlock_jester_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_jester_neck {
	complete_chapter_with_class [endoftime Jester]
	popup {
		prompt ITEM_UNLOCK_GENERIC
		immediate true
	}
	unlock_item_immediate Ruffle
}
```

---

### `class_unlock_fighter_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_fighter_trinket2 {
	complete_checklist_with_class Fighter
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate Steroids
}
```

---

### `class_unlock_hunter_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_hunter_trinket2 {
	complete_checklist_with_class Hunter
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate BagOfSeeds
}
```

---

### `class_unlock_mage_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_mage_trinket2 {
	complete_checklist_with_class Mage
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate SpellBook
}
```

---

### `class_unlock_medic_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_medic_trinket2 {
	complete_checklist_with_class Medic
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate PrayerCard
}
```

---

### `class_unlock_thief_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_thief_trinket2 {
	complete_checklist_with_class Thief
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate BagOfBags
}
```

---

### `class_unlock_tank_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tank_trinket2 {
	complete_checklist_with_class Tank
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TankToy
}
```

---

### `class_unlock_necro_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_necro_trinket2 {
	complete_checklist_with_class Necromancer
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate CambionConception
}
```

---

### `class_unlock_psychic_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_psychic_trinket2 {
	complete_checklist_with_class Psychic
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate FriendshipBracelet
}
```

---

### `class_unlock_tinkerer_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_tinkerer_trinket2 {
	complete_checklist_with_class Tinkerer
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate Fireworks
}
```

---

### `class_unlock_butcher_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_butcher_trinket2 {
	complete_checklist_with_class Butcher
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate SackOfMeat
}
```

---

### `class_unlock_druid_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_druid_trinket2 {
	complete_checklist_with_class Druid
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TinyCage
}
```

---

### `class_unlock_monk_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_monk_trinket2 {
	complete_checklist_with_class Monk
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TinyPebble
}
```

---

### `class_unlock_colorless_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_colorless_trinket2 {
	complete_checklist_with_class Colorless
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate SkillSplit
}
```

---

### `class_unlock_jester_trinket2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_jester_trinket2 {
	complete_checklist_with_class Jester
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate JokerCard
}
```

---

### `class_unlock_box0`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_box0 {
	fully_complete_difficulty 0
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TheBoxCardboard
}
```

---

### `class_unlock_box1`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_box1 {
	fully_complete_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TheBoxChest
}
```

---

### `class_unlock_box2`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_box2 {
	fully_complete_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TheBox
}
```

---

### `class_unlock_box3`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_box3 {
	fully_complete_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TheBlackBox
}
```

---

### `class_unlock_monocolorless_head`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_monocolorless_head {
	complete_chapter_with_class [meatworld Colorless]
	requires_monoclass_run true

	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate CopycatHat
}
```

---

### `class_unlock_monocolorless_face`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_monocolorless_face {
	complete_chapter_with_class [dimensionx Colorless]
	requires_monoclass_run true

	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate CopycatMask
}
```

---

### `class_unlock_monocolorless_neck`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
class_unlock_monocolorless_neck {
	complete_chapter_with_class [endoftime Colorless]
	requires_monoclass_run true

	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate CopycatScarf
}
```

---

### `song_unlock_alley`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_ALLEY`: ""Eatin' Rats" is now in the radio playlist!"

```
song_unlock_alley {
	beat_chapter_boss alley
	repeat 6 //trigger this 3 times to actually get the unlock
	unlock_song eatin_rats

	popup {
		prompt SONG_UNLOCK_ALLEY
		immediate true
	}
}
```

---

### `song_unlock_sewers`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_SEWERS`: ""Flush" is now in the radio playlist!"

```
song_unlock_sewers {
	beat_chapter_boss sewers
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song flush

	popup {
		prompt SONG_UNLOCK_SEWERS
		immediate true
	}
}
```

---

### `song_unlock_junkyard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_JUNKYARD`: ""Chumbucket Kitty" is now in the radio playlist!"

```
song_unlock_junkyard {
	beat_chapter_boss junkyard
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song chumbucket_kitty

	popup {
		prompt SONG_UNLOCK_JUNKYARD
		immediate true
	}
}
```

---

### `song_unlock_caves`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_CAVES`: ""Crystalline Dreams" is now in the radio playlist!"

```
song_unlock_caves {
	beat_chapter_boss crystaline_dreams
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song queenhippo

	popup {
		prompt SONG_UNLOCK_CAVES
		immediate true
	}
}
```

---

### `song_unlock_boneyard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_BONEYARD`: ""Them Kitty Bones" is now in the radio playlist!"

```
song_unlock_boneyard {
	beat_chapter_boss boneyard
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song them_kitty_bones

	popup {
		prompt SONG_UNLOCK_BONEYARD
		immediate true
	}
}
```

---

### `song_unlock_meatworld`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_MEATWORLD`: ""Sweet Delicious" is now in the radio playlist!"

```
song_unlock_meatworld {
	beat_chapter_boss meatworld
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song sweet_delicious

	popup {
		prompt SONG_UNLOCK_MEATWORLD
		immediate true
	}
}
```

---

### `song_unlock_throbbingking`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_THROBBINGKING`: ""Throbbing King" is now in the radio playlist!"

```
song_unlock_throbbingking {
	beat_chapter_boss meatworld
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song radio_throbbing_king

	popup {
		prompt SONG_UNLOCK_THROBBINGKING
		immediate true
	}
}
```

---

### `song_unlock_guillotina`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_GUILLOTINA`: ""Guillotina" is now in the radio playlist!"

```
song_unlock_guillotina {
	beat_house_boss guillotina_3
	unlock_song you_know_who

	popup {
		prompt SONG_UNLOCK_GUILLOTINA
		immediate true
	}
}
```

---

### `song_unlock_desert`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_DESERT`: ""Lonesome Road" is now in the radio playlist!"

```
song_unlock_desert {
	beat_chapter_boss desert
	repeat 6 //trigger this 3 times to actually get the unlock
	unlock_song lonesome_road

	popup {
		prompt SONG_UNLOCK_DESERT
		immediate true
	}
}
```

---

### `song_unlock_crater`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_CRATER`: ""Feline Invader" is now in the radio playlist!"

```
song_unlock_crater {
	beat_chapter_boss crater
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song feline_invader

	popup {
		prompt SONG_UNLOCK_CRATER
		immediate true
	}
}
```

---

### `song_unlock_bunker`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_BUNKER`: ""Alone in the Dark" is now in the radio playlist!"

```
song_unlock_bunker {
	beat_chapter_boss bunker
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song alone_in_the_dark

	popup {
		prompt SONG_UNLOCK_BUNKER
		immediate true
	}
}
```

---

### `song_unlock_moon`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_MOON`: ""So High" is now in the radio playlist!"

```
song_unlock_moon {
	beat_chapter_boss moon
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song so_high

	popup {
		prompt SONG_UNLOCK_MOON
		immediate true
	}
}
```

---

### `song_unlock_core`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_CORE`: ""Down with the Devil" is now in the radio playlist!"

```
song_unlock_core {
	beat_chapter_boss core
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song down_with_the_devil

	popup {
		prompt SONG_UNLOCK_CORE
		immediate true
	}
}
```

---

### `song_unlock_dimensionx`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_DIMENSIONX`: ""Chaos" is now in the radio playlist!"

```
song_unlock_dimensionx {
	beat_chapter_boss dimensionx
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song chaos

	popup {
		prompt SONG_UNLOCK_DIMENSIONX
		immediate true
	}
}
```

---

### `song_unlock_scrambled`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_SCRAMBLED`: ""Scrambled" is now in the radio playlist!"

```
song_unlock_scrambled { //silent unlock for visiting the rift for the first time (cut boss song)
	visit_chapter dimensionx
	unlock_song radio_scrambled

	/*popup {
		prompt SONG_UNLOCK_SCRAMBLED
		immediate true
	}*/
}
```

---

### `song_unlock_crazy_days`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_CHAOS_FORWARD`: ""Crazy Days" is now in the radio playlist!"

```
song_unlock_crazy_days {
	beat_chapter_boss dimensionx
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song crazy_days

	popup {
		prompt SONG_UNLOCK_CHAOS_FORWARD
		immediate true
	}
}
```

---

### `song_unlock_bolt_of_lightning`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_CHAOS_BACKWARD`: ""Bolt of Lightning" is now in the radio playlist!"

```
song_unlock_bolt_of_lightning {
	beat_chapter_boss dimensionx
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song bolt_of_lightning

	popup {
		prompt SONG_UNLOCK_CHAOS_BACKWARD
		immediate true
	}
}
```

---

### `song_unlock_kaijufight`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_KAIJUS`: ""Brush Your Teeth" is now in the radio playlist!"

```
song_unlock_kaijufight {
	beat_house_boss pyrophina_vs_zaratana
	unlock_song brush_your_teeth

	popup {
		prompt SONG_UNLOCK_KAIJUS
		immediate true
	}
}
```

---

### `song_unlock_lab`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_LAB`: ""Endless Misery" is now in the radio playlist!"

```
song_unlock_lab {
	beat_chapter_boss lab
	repeat 6 //trigger this 3 times to actually get the unlock
	unlock_song endless_misery

	popup {
		prompt SONG_UNLOCK_LAB
		immediate true
	}
}
```

---

### `song_unlock_future`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_FUTURE`: ""Humanicide" is now in the radio playlist!"

```
song_unlock_future {
	beat_chapter_boss future
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song humanicide

	popup {
		prompt SONG_UNLOCK_FUTURE
		immediate true
	}
}
```

---

### `song_unlock_iceage`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_ICEAGE`: ""Mom I Really Hate You" is now in the radio playlist!"

```
song_unlock_iceage {
	beat_chapter_boss iceage
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song mom_i_really_hate_you

	popup {
		prompt SONG_UNLOCK_ICEAGE
		immediate true
	}
}
```

---

### `song_unlock_theend`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_THEEND`: ""We're Dead" is now in the radio playlist!"

```
song_unlock_theend {
	beat_chapter_boss theend
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song were_dead

	popup {
		prompt SONG_UNLOCK_THEEND
		immediate true
	}
}
```

---

### `song_unlock_jurassic`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_JURASSIC`: ""Tuff" is now in the radio playlist!"

```
song_unlock_jurassic {
	beat_chapter_boss jurassic
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song tuff

	popup {
		prompt SONG_UNLOCK_JURASSIC
		immediate true
	}
}
```

---

### `song_unlock_endoftime`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_THEINFINITE`: ""Angel Wings" is now in the radio playlist!"

```
song_unlock_endoftime {
	beat_chapter_boss endoftime
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song angel_wings

	popup {
		prompt SONG_UNLOCK_THEINFINITE
		immediate true
	}
}
```

---

### `song_unlock_finalboss`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_FINALBOSS`: ""Dig Your Own Grave" is now in the radio playlist!"

```
song_unlock_finalboss {
	beat_chapter_boss endoftime
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_song radio_final_boss

	popup {
		prompt SONG_UNLOCK_FINALBOSS
		immediate true
	}
}
```

---

### `song_unlock_terminator`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_TERMINATOR`: ""Taser Paws" is now in the radio playlist!"

```
song_unlock_terminator {
	beat_house_boss terminator_2
	unlock_song taser_paws

	popup {
		prompt SONG_UNLOCK_TERMINATOR
		immediate true
	}
}
```

---

### `song_unlock_crack_of_doom`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_HITLERIII`: ""Crack of Doom" is now in the radio playlist!"

```
song_unlock_crack_of_doom {
	beat_house_boss terminator_3
	unlock_song crack_of_doom

	popup {
		prompt SONG_UNLOCK_HITLERIII
		immediate true
	}
}
```

---

### `song_unlock_get_in_the_cage`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_CREDITS_1`: ""Get in the Cage" is now in the radio playlist!"

```
song_unlock_get_in_the_cage {
	complete_item_quest Nuke //fallback for existing players
	unlock_song get_in_the_cage

	popup {
		prompt SONG_UNLOCK_CREDITS_1
		immediate false
	}
}
```

---

### `song_unlock_future_meets_the_past`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `SONG_UNLOCK_CREDITS_2`: ""Future Meets the Past" is now in the radio playlist!"

```
song_unlock_future_meets_the_past {
	complete_item_quest Nuke
	unlock_song future_meets_the_past

	popup {
		prompt SONG_UNLOCK_CREDITS_2
		immediate false
	}
}
```

---

### `legacy_event_unlock_momsknife`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
legacy_event_unlock_momsknife {
	unlock_item MomsKnife
	popup { 
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
}
```

---

### `boss_unlock_queenhippo`
**Source:** `adventure_progression_unlocks.gon`  

```
boss_unlock_queenhippo {
	complete_chapter alley
	repeat 3 //trigger this 3 times to actually get the unlock
	unlock_boss queenhippo
}
```

---

### `boss_unlock_gambit`
**Source:** `adventure_progression_unlocks.gon`  

```
boss_unlock_gambit { //ensure that zodiac is the first boss you fight in the desert
	complete_chapter desert
	repeat 1
	unlock_boss gambit
}
```

---

### `boss_unlock_ratking`
**Source:** `adventure_progression_unlocks.gon`  

```
boss_unlock_ratking { //ensure that flushmaster is the first miniboss you fight in the sewers
	complete_chapter sewers
	repeat 1
	unlock_boss ratking
}
```

---

### `boss_unlock_bumblefoot`
**Source:** `adventure_progression_unlocks.gon`  

```
boss_unlock_bumblefoot { //ensure that lenny is the first miniboss you fight in the bunker
	complete_chapter bunker
	repeat 1
	unlock_boss bumblefoot
}
```

---

### `boss_unlock_infestedduo`
**Source:** `adventure_progression_unlocks.gon`  

```
boss_unlock_infestedduo { //ensure that rocky bobo is the first miniboss you fight in the crater
	complete_chapter crater
	repeat 1
	unlock_boss infestedduo
}
```

---

### `levelgroup_unlock_bigsharksA`
**Source:** `adventure_progression_unlocks.gon`  

```
levelgroup_unlock_bigsharksA {
	complete_chapter caves
	unlock_levelgroup bigsharklevels
}
```

---

### `levelgroup_unlock_bigsharksB`
**Source:** `adventure_progression_unlocks.gon`  

```
levelgroup_unlock_bigsharksB {
	complete_chapter boneyard
	unlock_levelgroup bigsharklevels
}
```

---

### `weather_unlock_restlessdead`
**Source:** `adventure_progression_unlocks.gon`  

```
weather_unlock_restlessdead {
	complete_chapter boneyard
	repeat 3
	set_savefile_flag RestlessDeadUnlocked
}
```

---

### `weather_unlock_robotuprising`
**Source:** `adventure_progression_unlocks.gon`  

```
weather_unlock_robotuprising {
	complete_chapter bunker
	repeat 3
	set_savefile_flag RobotUprisingUnlocked
}
```

---

### `weather_unlock_hauntednight`
**Source:** `adventure_progression_unlocks.gon`  

```
weather_unlock_hauntednight {
	complete_chapter boneyard
	repeat 3
	set_savefile_flag HauntedNightUnlocked
}
```

---

### `weather_unlock_alieninvasion`
**Source:** `adventure_progression_unlocks.gon`  

```
weather_unlock_alieninvasion {
	complete_chapter moon
	repeat 3
	set_savefile_flag AlienInvasionUnlocked
}
```

---

### `trigger_butch_tips`
**Source:** `adventure_progression_unlocks.gon`  

```
trigger_butch_tips {
	fail_adventure anywhere
	repeat 2
	trigger_npc_sequence butch_tips_intro
}
```

---

### `trigger_tink_tips`
**Source:** `adventure_progression_unlocks.gon`  

```
trigger_tink_tips { //triggered manually
	trigger_npc_sequence tink_tips_intro
}
```

---

### `unlock_jack`
**Source:** `adventure_progression_unlocks.gon`  

```
unlock_jack {
	complete_adventure anywhere
	requires_unlocked_npc tracy

	unlock_npc_tomorrow jack
}
```

---

### `trigger_jack_begin_accepting_cats`
**Source:** `adventure_progression_unlocks.gon`  

```
trigger_jack_begin_accepting_cats { //triggered manually
	requires_unlocked_npc jack
	trigger_npc_sequence jack_begin_accepting_cats
}
```

---

### `unlock_tracy`
**Source:** `adventure_progression_unlocks.gon`  

```
unlock_tracy {
	complete_adventure anywhere
	requires_unlocked_npc frank
	unlock_npc_tomorrow tracy
	trigger_npc_sequence tracy_introduction
}
```

---

### `unlock_beanies`
**Source:** `adventure_progression_unlocks.gon`  

```
unlock_beanies {
	complete_chapters [caves boneyard] //same requirement as unlock desert
	unlock_npc_tomorrow beanies
	trigger_npc_sequence beanies_begin_accepting_cats
}
```

---

### `unlock_steven`
**Source:** `adventure_progression_unlocks.gon`  

```
unlock_steven {
	visit_chapter iceage
	unlock_npc_tomorrow steven
	trigger_npc_sequence steven_introduction
}
```

---

### `difficulty_unlock_act1_hard`
**Source:** `adventure_progression_unlocks.gon`  

```
difficulty_unlock_act1_hard {
	complete_act_difficulty [1 0]
	unlock_act_difficulty [1 1]
	//trigger_npc_sequence steven_introduction (actual trigger for this is visit ice age)
}
```

---

### `difficulty_unlock_act1_crazy`
**Source:** `adventure_progression_unlocks.gon`  

```
difficulty_unlock_act1_crazy {
	complete_act_difficulty [1 1]
	unlock_act_difficulty [1 2]

	trigger_npc_sequence steven_unlock_act1_crazy
}
```

---

### `difficulty_unlock_act1_impossible`
**Source:** `adventure_progression_unlocks.gon`  

```
difficulty_unlock_act1_impossible {
	complete_act_difficulty [1 2]
	unlock_act_difficulty [1 3]

	trigger_npc_sequence steven_unlock_act1_impossible
}
```

---

### `difficulty_unlock_act2_hard`
**Source:** `adventure_progression_unlocks.gon`  

```
difficulty_unlock_act2_hard {
	complete_act_difficulty [2 0]
	unlock_act_difficulty [2 1]

	trigger_npc_sequence steven_unlock_act2_hard
}
```

---

### `difficulty_unlock_act2_crazy`
**Source:** `adventure_progression_unlocks.gon`  

```
difficulty_unlock_act2_crazy {
	complete_act_difficulty [2 1]
	unlock_act_difficulty [2 2]

	trigger_npc_sequence steven_unlock_act2_crazy
}
```

---

### `difficulty_unlock_act2_impossible`
**Source:** `adventure_progression_unlocks.gon`  

```
difficulty_unlock_act2_impossible {
	complete_act_difficulty [2 2]
	unlock_act_difficulty [2 3]

	trigger_npc_sequence steven_unlock_act2_impossible
}
```

---

### `difficulty_unlock_act3_hard`
**Source:** `adventure_progression_unlocks.gon`  

```
difficulty_unlock_act3_hard {
	complete_act_difficulty [3 0]
	unlock_act_difficulty [3 1]

	trigger_npc_sequence steven_unlock_act3_hard
}
```

---

### `difficulty_unlock_act3_crazy`
**Source:** `adventure_progression_unlocks.gon`  

```
difficulty_unlock_act3_crazy {
	complete_act_difficulty [3 1]
	unlock_act_difficulty [3 2]

	trigger_npc_sequence steven_unlock_act3_crazy
}
```

---

### `difficulty_unlock_act3_impossible`
**Source:** `adventure_progression_unlocks.gon`  

```
difficulty_unlock_act3_impossible {
	complete_act_difficulty [3 2]
	unlock_act_difficulty [3 3]

	trigger_npc_sequence steven_unlock_act3_impossible
}
```

---

### `desert_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_DESERT`: "You can now adventure to The Desert!"

```
desert_intro_popup {
	popup {
		prompt AREA_UNLOCK_DESERT
		frame UnlockArea_Desert
	}
}
```

---

### `caves_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_CAVES`: "You can now adventure to The Caves!"

```
caves_intro_popup {
	popup {
		prompt AREA_UNLOCK_CAVES
		frame UnlockArea_Caves
	}
}
```

---

### `dybbuk_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_BONEYARD`: "You can now adventure to The Boneyard!"

```
dybbuk_popup { //boneyard intro
	popup {
		prompt AREA_UNLOCK_BONEYARD
		frame UnlockArea_Boneyard
	}
}
```

---

### `core_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_CORE`: "You can now adventure to The Core!"

```
core_intro_popup {
	popup {
		prompt AREA_UNLOCK_CORE
		frame UnlockArea_Core
	}
}
```

---

### `moon_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_MOON`: "You can now adventure to The Moon!"

```
moon_intro_popup {
	popup {
		prompt AREA_UNLOCK_MOON
		frame UnlockArea_Moon
	}
}
```

---

### `lab_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_LAB`: "You can now adventure to The Lab!"

```
lab_intro_popup {
	popup {
		prompt AREA_UNLOCK_LAB
		frame UnlockArea_Lab
	}
}
```

---

### `theend_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_THEEND`: "You can now adventure even further into the future!"

```
theend_intro_popup {
	popup {
		prompt AREA_UNLOCK_THEEND
		frame UnlockArea_TheEnd
	}
}
```

---

### `jurassic_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_JURASSIC`: "You can now adventure even further into the past!"

```
jurassic_intro_popup {
	popup {
		prompt AREA_UNLOCK_JURASSIC
		frame UnlockArea_Jurassic
	}
}
```

---

### `guillotina_1_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_GUILLOTINA_1`: "Guillotina is coming for you!"

```
guillotina_1_popup {
	popup {
		prompt CUTSCENE_GUILLOTINA_1
		//frame Guillotina1
	}
}
```

---

### `house_boss_returns_tina1_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_GUILLOTINA_1_REMATCH`: "Guillotina is coming for you!"

```
house_boss_returns_tina1_popup {
	popup {
		prompt CUTSCENE_GUILLOTINA_1_REMATCH
		//frame Guillotina1
	}
}
```

---

### `guillotina_2_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_GUILLOTINA_2`: "Guillotina is returning!"

```
guillotina_2_popup {
	popup {
		prompt CUTSCENE_GUILLOTINA_2
		//frame Guillotina1
	}
}
```

---

### `house_boss_returns_tina2_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_GUILLOTINA_2_REMATCH`: "Guillotina is returning!"

```
house_boss_returns_tina2_popup {
	popup {
		prompt CUTSCENE_GUILLOTINA_2_REMATCH
		//frame Guillotina1
	}
}
```

---

### `guillotina_3_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_GUILLOTINA_3`: "Guillotina is out for revenge!"

```
guillotina_3_popup {
	popup {
		prompt CUTSCENE_GUILLOTINA_3
		//frame Guillotina1
	}
}
```

---

### `house_boss_returns_tina3_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_GUILLOTINA_3_REMATCH`: "Guillotina is out for revenge!"

```
house_boss_returns_tina3_popup {
	popup {
		prompt CUTSCENE_GUILLOTINA_3_REMATCH
		//frame Guillotina1
	}
}
```

---

### `pyro_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_PYROPHINA`: "Pyrophina is on the way!"

```
pyro_intro_popup {
	popup {
		prompt CUTSCENE_PYROPHINA
		//frame Guillotina1
	}
}
```

---

### `house_boss_returns_pyro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_PYROPHINA_REMATCH`: "Pyrophina is on the way!"

```
house_boss_returns_pyro_popup {
	popup {
		prompt CUTSCENE_PYROPHINA_REMATCH
		//frame Guillotina1
	}
}
```

---

### `moonboss_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_ZARATANA`: "Zaratana is on the way!"

```
moonboss_intro_popup {
	popup {
		prompt CUTSCENE_ZARATANA
		//frame Guillotina1
	}
}
```

---

### `house_boss_returns_zara_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_ZARATANA_REMATCH`: "Zaratana is on the way!"

```
house_boss_returns_zara_popup {
	popup {
		prompt CUTSCENE_ZARATANA_REMATCH
		//frame Guillotina1
	}
}
```

---

### `kaiju_fight_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_KAIJUFIGHT`: "The kaijus are bringing the fight to you!"

```
kaiju_fight_popup {
	popup {
		prompt CUTSCENE_KAIJUFIGHT
		//frame Guillotina1
	}
}
```

---

### `house_boss_returns_kaijufight_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_KAIJUFIGHT_REMATCH`: "The kaijus are bringing the fight to you!"

```
house_boss_returns_kaijufight_popup {
	popup {
		prompt CUTSCENE_KAIJUFIGHT_REMATCH
		//frame Guillotina1
	}
}
```

---

### `terminator_1_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_TERMINATOR_1`: "The C-800 seeks you!"

```
terminator_1_popup {
	popup {
		prompt CUTSCENE_TERMINATOR_1
		//frame Guillotina1
	}
}
```

---

### `house_boss_returns_t1_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_TERMINATOR_1_REMATCH`: "The C-800 seeks you!"

```
house_boss_returns_t1_popup {
	popup {
		prompt CUTSCENE_TERMINATOR_1_REMATCH
		//frame Guillotina1
	}
}
```

---

### `t1000_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_TERMINATOR_2`: "The C-1000 is on the prowl!"

```
t1000_intro_popup {
	popup {
		prompt CUTSCENE_TERMINATOR_2
		//frame Guillotina1
	}
}
```

---

### `house_boss_returns_t2_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_TERMINATOR_2_REMATCH`: "The C-1000 is on the prowl!"

```
house_boss_returns_t2_popup {
	popup {
		prompt CUTSCENE_TERMINATOR_2_REMATCH
		//frame Guillotina1
	}
}
```

---

### `hitler_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_TERMINATOR_3`: "Hitler is back!"

```
hitler_intro_popup {
	popup {
		prompt CUTSCENE_TERMINATOR_3
		//frame Guillotina1
	}
}
```

---

### `house_boss_returns_t3_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_TERMINATOR_3_REMATCH`: "Hitler is back!"

```
house_boss_returns_t3_popup {
	popup {
		prompt CUTSCENE_TERMINATOR_3_REMATCH
		//frame Guillotina1
	}
}
```

---

### `pyro_ending_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_THERIFT`: "You can now adventure to The Rift!"

```
pyro_ending_popup {
	popup {
		prompt AREA_UNLOCK_THERIFT
		frame UnlockArea_Rift
	}
}
```

---

### `zara_ending_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_THERIFT`: "You can now adventure to The Rift!"

```
zara_ending_popup {
	popup {
		prompt AREA_UNLOCK_THERIFT
		frame UnlockArea_Rift
	}
}
```

---

### `king_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_MEATWORLDFULL`: "The Throbbing King requests your audience. You now have full access to his domain!"

```
king_intro_popup {
	popup {
		prompt AREA_UNLOCK_MEATWORLDFULL
		frame UnlockArea_Meatworld
	}
}
```

---

### `infinite_intro_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `AREA_UNLOCK_ENDOFTIME`: "The time machine can now travel to The Infinite!"

```
infinite_intro_popup {
	popup {
		prompt AREA_UNLOCK_ENDOFTIME
		frame UnlockArea_Infinite
	}
}
```

---

### `obelisk1_core_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_OBELISK1_CORE_POPUP`: "One obelisk is raised, but the one on the moon remains buried."

```
obelisk1_core_popup {
	popup {
		prompt CUTSCENE_OBELISK1_CORE_POPUP
	}
}
```

---

### `obelisk1_moon_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_OBELISK1_MOON_POPUP`: "One obelisk is raised, but the one in the core remains buried."

```
obelisk1_moon_popup {
	popup {
		prompt CUTSCENE_OBELISK1_MOON_POPUP
	}
}
```

---

### `obelisk2_core_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_OBELISK2_POPUP`: "Both obelisks have connected, but still await activation."

```
obelisk2_core_popup {
	popup {
		prompt CUTSCENE_OBELISK2_POPUP
	}
}
```

---

### `obelisk2_moon_popup`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `CUTSCENE_OBELISK2_POPUP`: "Both obelisks have connected, but still await activation."

```
obelisk2_moon_popup {
	popup {
		prompt CUTSCENE_OBELISK2_POPUP
	}
}
```

---

### `steven_unlock_throb_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_throb_hard {
	beat_chapter_boss meatworld
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ThrobbingCrown
}
```

---

### `steven_unlock_rift_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_rift_hard {
	beat_chapter_boss dimensionx
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate CrownOfChaos
}
```

---

### `steven_unlock_infinite_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_infinite_hard {
	beat_chapter_boss endoftime
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ChildsCrown
}
```

---

### `steven_unlock_tina1_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_tina1_hard {
	beat_house_boss guillotina_1
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TinasBellyButton
}
```

---

### `steven_unlock_tina2_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_tina2_hard {
	beat_house_boss guillotina_2
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TinasLarynx
}
```

---

### `steven_unlock_tina3_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_tina3_hard {
	beat_house_boss guillotina_3
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate TinasFriend
}
```

---

### `steven_unlock_pyro_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_pyro_hard {
	beat_house_boss pyrophina
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate PyrophinasToenail
}
```

---

### `steven_unlock_zara_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_zara_hard {
	beat_house_boss zaratana
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ZaratanaTurd
}
```

---

### `steven_unlock_kfight_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_kfight_hard {
	beat_house_boss pyrophina_vs_zaratana
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate ScorchedEarth
}
```

---

### `steven_unlock_t1_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_t1_hard {
	beat_house_boss terminator_1
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate RoboticArm
}
```

---

### `steven_unlock_t2_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_t2_hard {
	beat_house_boss terminator_2
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate LiquidMetal
}
```

---

### `steven_unlock_t3_hard`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_t3_hard {
	beat_house_boss terminator_3
	required_difficulty 1
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate HitlersToupe
}
```

---

### `steven_unlock_throb_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_throb_crazy {
	beat_chapter_boss meatworld
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensGobbler
}
```

---

### `steven_unlock_rift_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_rift_crazy {
	beat_chapter_boss dimensionx
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensFartFace
}
```

---

### `steven_unlock_infinite_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_infinite_crazy {
	beat_chapter_boss endoftime
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensShotgun
}
```

---

### `steven_unlock_tina1_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_tina1_crazy {
	beat_house_boss guillotina_1
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensMustache
}
```

---

### `steven_unlock_tina2_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_tina2_crazy {
	beat_house_boss guillotina_2
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensGristle
}
```

---

### `steven_unlock_tina3_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_tina3_crazy {
	beat_house_boss guillotina_3
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensBagofRocks
}
```

---

### `steven_unlock_pyro_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_pyro_crazy {
	beat_house_boss pyrophina
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensHelmet
}
```

---

### `steven_unlock_zara_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_zara_crazy {
	beat_house_boss zaratana
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensFriend
}
```

---

### `steven_unlock_kfight_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_kfight_crazy {
	beat_house_boss pyrophina_vs_zaratana
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenStone
}
```

---

### `steven_unlock_t1_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_t1_crazy {
	beat_house_boss terminator_1
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenMarrow
}
```

---

### `steven_unlock_t2_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_t2_crazy {
	beat_house_boss terminator_2
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensBottle
}
```

---

### `steven_unlock_t3_crazy`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_t3_crazy {
	beat_house_boss terminator_3
	required_difficulty 2
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensHat
}
```

---

### `steven_unlock_throb_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_throb_impossible {
	beat_chapter_boss meatworld
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenHat1
}
```

---

### `steven_unlock_rift_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_rift_impossible {
	beat_chapter_boss dimensionx
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenMask1
}
```

---

### `steven_unlock_infinite_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_infinite_impossible {
	beat_chapter_boss endoftime
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenNeck1
}
```

---

### `steven_unlock_tina1_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_tina1_impossible {
	beat_house_boss guillotina_1
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenTrinket1
}
```

---

### `steven_unlock_tina2_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_tina2_impossible {
	beat_house_boss guillotina_2
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenWeapon1
}
```

---

### `steven_unlock_tina3_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_tina3_impossible {
	beat_house_boss guillotina_3
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensConsumable1
}
```

---

### `steven_unlock_pyro_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_pyro_impossible {
	beat_house_boss pyrophina
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenHat2
}
```

---

### `steven_unlock_zara_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_zara_impossible {
	beat_house_boss zaratana
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenMask2
}
```

---

### `steven_unlock_kfight_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_kfight_impossible {
	beat_house_boss pyrophina_vs_zaratana
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenNeck2
}
```

---

### `steven_unlock_t1_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_t1_impossible {
	beat_house_boss terminator_1
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenTrinket2
}
```

---

### `steven_unlock_t2_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_t2_impossible {
	beat_house_boss terminator_2
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevenWeapon2
}
```

---

### `steven_unlock_t3_impossible`
**Source:** `adventure_progression_unlocks.gon`  

**Localization Strings:**
- `ITEM_UNLOCK_GENERIC`: ""{item}" has been unlocked!"

```
steven_unlock_t3_impossible {
	beat_house_boss terminator_3
	required_difficulty 3
	popup {
		prompt ITEM_UNLOCK_GENERIC
		frame UnlockItem
		immediate true
	}
	unlock_item_immediate StevensConsumable2
}
```

---

## File: `npc_favor_unlocks.gon`

### `beanies_questinfo`
**Source:** `npc_favor_unlocks.gon`  

```
beanies_questinfo {
	destinations { //area | coin reward
		caves 200
		boneyard 200
		meatworld 300

		moon 300
		core 300
		dimensionx 400

		jurassic 400
		theend 400
		endoftime 500
	}

	prereqs {
		moon mapflag_IceAgeUnlocked
		core mapflag_IceAgeUnlocked
		dimensionx mapflag_IceAgeUnlocked

		jurassic endoftime
		theend endoftime
		endoftime endoftime
	}

	intro [PersuasionDevice]
	main_pool [
		ChaosDevice
		MagicMirror
		MeStone
		AngryFace
		FartFace

		SpiderInjector
		PartyDetonator
		AirHorn
		TheLoner
		GlassCannon

		PrincessHat
		HardPill
		BubbleBoy
		Redacted
		Stopwatch

		StorageLocker
		MysteriousDice
		ExperimentalTreatment
		UltraVision3000
		NuclearKnife
	]
}
```

---

### `Beanies`
**Source:** `npc_favor_unlocks.gon`  

**Localization Strings:**
- `FAVOR_BEANIES_INTRO`: "A special job."
- `FAVOR_BEANIES_REPEAT`: "A side quest item."

```
Beanies {
	beanies_quests_intro {
		generate_beanies_quest intro
		favor 1

		reward_text "FAVOR_BEANIES_INTRO"
	}

	beanies_quests_repeat {
		generate_beanies_quest main_pool
		favor 5
		repeat infinite

		reward_text "FAVOR_BEANIES_REPEAT"
		level_display max
	}
}
```

---

### `Butch`
**Source:** `npc_favor_unlocks.gon`  

**Localization Strings:**
- `FAVOR_BUTCH_UPGRADE`: "Upgrade your item storage."

```
Butch {
	//start at 3x3 + 7 upgrades = 10x10

	//tutorial
	upgrade_storage_1 {
		storage_expansion 1
		required_act 0
		required_chapter 0
		favor 1

		reward_text "FAVOR_BUTCH_UPGRADE"
	}

	//act 1
	upgrade_storage_2 {
		storage_expansion 1
		required_act 1
		required_chapter 2
		favor 10

		reward_text "FAVOR_BUTCH_UPGRADE"
	}

	upgrade_storage_3 {
		storage_expansion 1
		required_act 1
		required_chapter 3
		favor 10

		reward_text "FAVOR_BUTCH_UPGRADE"
	}

	//act 2
	upgrade_storage_4 {
		storage_expansion 1
		required_act 2
		required_chapter 2
		favor 15

		reward_text "FAVOR_BUTCH_UPGRADE"
	}

	upgrade_storage_5 {
		storage_expansion 1
		required_act 2
		required_chapter 3
		favor 15

		reward_text "FAVOR_BUTCH_UPGRADE"
	}

	//act 3
	upgrade_storage_6 {
		storage_expansion 1
		required_act 3
		required_chapter 2
		favor 20

		reward_text "FAVOR_BUTCH_UPGRADE"
	}

	upgrade_storage_7 {
		storage_expansion 1
		required_act 3
		required_chapter 3
		favor 20

		reward_text "FAVOR_BUTCH_UPGRADE"
	}


	upgrade_storage_repeating_intro {
		rep_reward_count 1
		required_act 3
		required_chapter 4
		required_difficulty 0

		favor 10

		reward_text "FAVOR_BUTCH_UPGRADE"
		level_display max
	}
	upgrade_storage_repeating_normal {
		rep_reward_count 1
		required_act 3
		required_chapter 4
		required_difficulty 0

		favor 10
		repeat 20 //with the intro one, this goes from 100 to 121 (11x11)

		reward_text "FAVOR_BUTCH_UPGRADE"
		level_display max
	}
	upgrade_storage_repeating_hard {
		rep_reward_count 1
		required_act 3
		required_chapter 4
		required_difficulty 1

		favor 10
		repeat 23

		reward_text "FAVOR_BUTCH_UPGRADE"
		level_display max
	}
	upgrade_storage_repeating_crazy {
		rep_reward_count 1
		required_act 3
		required_chapter 4
		required_difficulty 2

		favor 10
		repeat 25

		reward_text "FAVOR_BUTCH_UPGRADE"
		level_display max
	}
	upgrade_storage_repeating_impossible {
		rep_reward_count 1
		required_act 3
		required_chapter 4
		required_difficulty 3

		favor 10
		repeat infinite

		reward_text "FAVOR_BUTCH_UPGRADE"
		level_display max
	}
}
```

---

### `Tink`
**Name:** favor  
**Source:** `npc_favor_unlocks.gon`  

**Localization Strings:**
- `FAVOR_TINK_BOW`: "It's a secret!"
- `FAVOR_TINK_BASESTATS`: "Information to help breed cats."
- `FAVOR_TINK_INBREEDING`: "A way to check a cat's ancestry."
- `FAVOR_TINK_SEXUALITY`: "Gaydar."
- `FAVOR_TINK_TAGS`: "Something to help organize your cats."
- `FAVOR_TINK_AGRESSION`: "Information to help understand a cat's personality."
- `FAVOR_TINK_RELATIONSHIPS`: "Information to help understand a cat's relationships."
- `FAVOR_TINK_MAX`: "25 coins"

```
Tink {
	tink_prettybow {
		favor 1
		gift_item TinksBow

		reward_text "FAVOR_TINK_BOW"
	}

	tink_basestats { //ability to view base stats / stat modifications separately
		favor 10
		set_savefile_flag catinfo_unlock_basestats

		reward_text "FAVOR_TINK_BASESTATS"
	}

	tink_inbreeding { //an icon for how inbred a cat is, plus a family tree view
		favor 10
		set_savefile_flag catinfo_unlock_inbreeding

		reward_text "FAVOR_TINK_INBREEDING"
	}

	tink_sexuality { //an icon for libido, plus gay/bi flags
		favor 10
		set_savefile_flag catinfo_unlock_sexuality

		reward_text "FAVOR_TINK_SEXUALITY"
	}

	tink_tags { //ability to manually add symbols to a cat's name
		favor 10
		set_savefile_flag catinfo_unlock_tags

		reward_text "FAVOR_TINK_TAGS"
	}

	tink_aggression { //an icon for how aggressive a cat is
		favor 10
		set_savefile_flag catinfo_unlock_aggression

		reward_text "FAVOR_TINK_AGRESSION"
	}

	tink_relationships { //an icon representing who a cat loves and who a cat hates
		favor 10
		set_savefile_flag catinfo_unlock_relationships

		reward_text "FAVOR_TINK_RELATIONSHIPS"
	}

	tink_max_intro {
		favor 10
		coins 25

		reward_text "FAVOR_TINK_MAX"
		level_display max
	}
	tink_max_repeating {
		favor 10
		coins 25
		repeat infinite

		reward_text "FAVOR_TINK_MAX"
		level_display max
	}
}
```

---

### `Frank`
**Source:** `npc_favor_unlocks.gon`  

**Localization Strings:**
- `FAVOR_FRANK_ATTIC`: "An attic."
- `FAVOR_FRANK_ROOM`: "Another room for your house."
- `FAVOR_FRANK_PARASITE`: "A random parasite."

```
Frank {
	house_upgrade_attic {
		house_upgrade SmallHouse_Attic
		favor 1

		reward_text "FAVOR_FRANK_ATTIC"
	}

	house_upgrade_mediumhouse {
		house_upgrade MediumHouse
		house_upgrade MediumHouse_SmallRoom
		favor 25

		reward_text "FAVOR_FRANK_ROOM"
	}

	house_upgrade_largehouse {
		house_upgrade LargeHouse
		house_upgrade LargeHouse_Floor2Large
		favor 50

		reward_text "FAVOR_FRANK_ROOM"
	}

	house_upgrade_4throom {
		house_upgrade LargeHouse_Floor2Small
		favor 100

		reward_text "FAVOR_FRANK_ROOM"
	}

	/*house_upgrade_basement {
		house_upgrade BasementUpgrade
		favor 50
	}

	house_upgrade_basement2 {
		house_upgrade BasementUpgrade2
		favor 100
	}

	house_upgrade_basement3 {
		house_upgrade BasementUpgrade3
		favor 250
	}

	house_upgrade_basement4 {
		house_upgrade BasementUpgrade4
		favor 500
	}

	house_upgrade_basement5 {
		house_upgrade BasementUpgrade5
		favor 1000
	}*/

	frank_max_intro {
		favor 10
		gift_item_from_pool parasites

		reward_text "FAVOR_FRANK_PARASITE"
		level_display max
	}
	frank_max_repeating {
		favor 10
		repeat infinite
		gift_item_from_pool parasites

		reward_text "FAVOR_FRANK_PARASITE"
		level_display max
	}
}
```

---

### `Jack`
**Source:** `npc_favor_unlocks.gon`  

**Localization Strings:**
- `FAVOR_JACK_UPGRADE`: "More furniture for sale."
- `FAVOR_JACK_MAX`: "Increase the chance of rare furniture in the shop."

```
Jack {
	jack_shopupgrade1 {
		favor 1
		shop_level_up 1 //to 3 items in the shop

		reward_text "FAVOR_JACK_UPGRADE"
	}
	jack_shopupgrade2 {
		favor 10
		shop_level_up 1 //to 4 items in the shop

		reward_text "FAVOR_JACK_UPGRADE"
	}
	jack_shopupgrade3 {
		favor 20
		shop_level_up 1 //to 5 items in the shop

		reward_text "FAVOR_JACK_UPGRADE"
	}
	jack_shopupgrade4 {
		favor 30
		shop_level_up 1 //to 6 items in the shop

		reward_text "FAVOR_JACK_UPGRADE"
	}

	jack_max_intro {
		favor 10
		rep_reward_count 1

		reward_text "FAVOR_JACK_MAX"
		level_display max
	}
	jack_max_repeating {
		favor 10
		repeat infinite
		rep_reward_count 1

		reward_text "FAVOR_JACK_MAX"
		level_display max
	}
}
```

---

### `Tracy`
**Source:** `npc_favor_unlocks.gon`  

**Localization Strings:**
- `FAVOR_TRACY_FOOD`: "Stocks a food box."
- `FAVOR_TRACY_COLLAR`: "Stocks a blank collar."
- `FAVOR_TRACY_IDOL`: "Stocks a special furniture idol."
- `FAVOR_TRACY_RARE`: "Stock a random rare item for cheap."

```
Tracy {
	tracy_foodstorage1 {
		favor 1
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_blankcollar1 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type blankcollar
			cost 150
		}

		reward_text "FAVOR_TRACY_COLLAR"
	}
	tracy_foodstorage2 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_idol1 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type random_unique_idol
			cost 150
		}

		reward_text "FAVOR_TRACY_IDOL"
	}
	tracy_foodstorage3 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_blankcollar2 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type blankcollar
			cost 150
		}

		reward_text "FAVOR_TRACY_COLLAR"
	}
	tracy_foodstorage4 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_idol2 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type random_unique_idol
			cost 150
		}

		reward_text "FAVOR_TRACY_IDOL"
	}
	tracy_foodstorage5 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_blankcollar3 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type blankcollar
			cost 150
		}

		reward_text "FAVOR_TRACY_COLLAR"
	}
	tracy_foodstorage6 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_idol3 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type random_unique_idol
			cost 150
		}

		reward_text "FAVOR_TRACY_IDOL"
	}
	tracy_foodstorage7 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_idol4 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type random_unique_idol
			cost 150
		}

		reward_text "FAVOR_TRACY_IDOL"
	}
	tracy_foodstorage8 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_idol5 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type random_unique_idol
			cost 150
		}

		reward_text "FAVOR_TRACY_IDOL"
	}
	tracy_foodstorage9 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_idol6 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type random_unique_idol
			cost 150
		}

		reward_text "FAVOR_TRACY_IDOL"
	}
	tracy_foodstorage10 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type special_foodbox
			cost 100
		}

		reward_text "FAVOR_TRACY_FOOD"
	}
	tracy_idol7 {
		favor 10
		required_age 5
		shop_level_up 1

		tracy_special_item {
			type random_unique_idol
			cost 150
		}

		reward_text "FAVOR_TRACY_IDOL"
	}

	tracy_max_intro {
		favor 10
		required_age 5

		tracy_special_item {
			type bonus_rare_item
			cost 10
		}

		reward_text "FAVOR_TRACY_RARE"
		level_display max
	}
	tracy_max_repeating {
		favor 10
		required_age 5
		repeat infinite

		tracy_special_item {
			type bonus_rare_item
			cost 10
		}

		reward_text "FAVOR_TRACY_RARE"
		level_display max
	}
}
```

---

### `OrganGrinder`
**Source:** `npc_favor_unlocks.gon`  

**Localization Strings:**
- `FAVOR_GRINDER_UPGRADE`: "Recovers more stuff from lost runs."
- `FAVOR_GRINDER_SYRINGE`: "A random disorder syringe."

```
OrganGrinder {
	organ_unlock { //organ grinder initial unlock 
		favor 1
		shop_level_up 1 //(3 items, 20% recovery, no item advantage) minimum gold/food recovered: 8

		reward_text "FAVOR_GRINDER_UPGRADE"
	}
	organ_upgrade1 {
		favor 10
		shop_level_up 1 //(3 items, 25% recovery, +3 item advantage) minimum gold/food recovered: 10

		reward_text "FAVOR_GRINDER_UPGRADE"
	}
	organ_upgrade2 {
		favor 25
		shop_level_up 1 //(3 items, 30% recovery, +6 item advantage) minimum gold/food recovered: 12

		reward_text "FAVOR_GRINDER_UPGRADE"
	}
	organ_upgrade3 {
		favor 50
		shop_level_up 1 //(3 items, 35% recovery, +9 item advantage) minimum gold/food recovered: 14

		reward_text "FAVOR_GRINDER_UPGRADE"
	}
	organ_upgrade4 {
		favor 75
		shop_level_up 1 //(3 items, 40% recovery, +12 item advantage) minimum gold/food recovered: 16

		reward_text "FAVOR_GRINDER_UPGRADE"
	}
	organ_upgrade5 {
		favor 100
		shop_level_up 1 //(3 items, 45% recovery, +15 item advantage) minimum gold/food recovered: 18

		reward_text "FAVOR_GRINDER_UPGRADE"
	}
	organ_upgrade6 {
		favor 150
		shop_level_up 1 //(3 items, 50% recovery, +18 item advantage) minimum gold/food recovered: 20

		reward_text "FAVOR_GRINDER_UPGRADE"
	}

	organ_max_intro {
		favor 10
		gift_item disorder_needle

		reward_text "FAVOR_GRINDER_SYRINGE"
		level_display max
	}
	organ_max_repeating {
		favor 10
		repeat infinite
		gift_item disorder_needle

		reward_text "FAVOR_GRINDER_SYRINGE"
		level_display max
	}
}
```

---

### `Steven`
**Source:** `npc_favor_unlocks.gon`  

```
Steven {
	steven_milliontrashed {
		favor 1000000
		repeat infinite
		level_display max
	}
}
```

---

