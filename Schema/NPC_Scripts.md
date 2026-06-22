# Mewgenics Mod Developer Documentation: NPC Scripts Schema

This document covers the scripting format used in `npc_scripts/*.gon` files.
These files define the dialogue sequences, progression unlocks, and camera scripting
for the six house NPCs: Beanies, Tracy, Frank, Jack, Organ Grinder, and Tink.

> **Note:** The `combat_tutorial.gon` file uses the same format but is excluded here
> as it is a tutorial script, not NPC progression scripting.

## File Structure

Every NPC script file follows this top-level layout:

```gon
movieclip <SceneName>       // The Flash movieclip/scene used for this NPC's office
default_npc <NPCName>       // The NPC identifier this script controls

states_and_transitions {
    states {
        <state_name> ["<anim1>" "<anim2>"]   // Named camera/animation states
    }
    transitions { }         // (unused in base game, reserved for future use)
}

sequences {
    <sequence_name> {       // Named trigger point — called by the engine or do_sequence
        <command> <arg>     // Engine commands executed top-to-bottom
        ...
    }
}
```

---

## Top-Level Fields

| Field | Type | Description |
| :--- | :--- | :--- |
| `movieclip` | Enum | The scene/room identifier for this NPC's UI screen. |
| `default_npc` | Enum | The NPC this script is attached to. |
| `states_and_transitions` | Block | Defines named animation/camera states and (unused) transition rules. |
| `sequences` | Block | Contains all named sequence blocks — the main scripting body. |

---

## Sequence Commands

Commands are statements inside a `sequences { <name> { ... } }` block.
They execute top-to-bottom when the engine triggers the named sequence.

| Command | Argument Type | Description | Examples |
| :--- | :--- | :--- | :--- |
| `begin_accepting_cats` | NPC Name | Mark the specified NPC as now accepting cats (enables their mechanic). | `beanies`, `butch`, `jack` |
| `cancelable` | Boolean | Marks this sequence as cancelable (player can skip). | `true`, `true`, `true` |
| `dialog` | String (loc key) | Display a dialogue line. Waits for player to click through. | `NPC_BEANIES_ENDING_1`, `NPC_BEANIES_ENDING_2`, `NPC_BEANIES_ENDING_3` |
| `dialog_and_autopass` | String (loc key) | Display a dialogue line that auto-dismisses (used with `wait_for_cancel`). | `NPC_BEANIES_INTRO_15`, `NPC_JACK_UNPROMPTED_1`, `NPC_JACK_PURCHASE_ITEM_1` |
| `do_random_sequence` | Array of Sequence Names | Pick and execute one sequence at random from the list. | `[unprompted1, unprompted2, unprompted3, unprompted4, unprompted5, unprompted6]`, `[upgrade_storage_max1, upgrade_storage_max2, upgrade_storage_max3, upgrade_storage_max4, upgrade_storage_max5]`, `[upgrade_storage_max1, upgrade_storage_max2, upgrade_storage_max3, upgrade_storage_max4, upgrade_storage_max5]` |
| `do_sequence` | Sequence Name | Jump to and execute another named sequence immediately. | `forward_to_tips`, `forward_to_tips`, `forward_to_tips` |
| `force_current_cat_use_ability` | Ability Name | Force the currently-selected cat to use a specified ability (used in tutorials). |  |
| `gather_questitem_info` | (none) | Populate internal quest item data for display in the next dialog. | `newest`, `newest`, `success` |
| `get` | Enum | Trigger a get-reward action. Common value: `npc_reward` (give the player the NPC's queued reward). | `npc_reward`, `npc_reward`, `sidequest_reward` |
| `get_random_furniture_piece` | (none) | Select a random furniture piece to reference in subsequent dialog. |  |
| `get_token` | Token ID | Retrieve a specific game token/flag value. |  |
| `if` | Condition | Conditional branch — executes next block only if condition is true. |  |
| `lock_controls` | Number (1) | Disable player input. Typically used at the start of a scripted scene. | `1`, `1`, `1` |
| `lock_mouse` | Number (1) | Disable mouse cursor input specifically. |  |
| `play_cutscene` | Cutscene ID | Trigger a full cutscene by ID. | `credits_1` |
| `restart_npc_music` | (none) | Restart the background music track for this NPC's scene. | `1` |
| `screenshake` | Integer | Trigger a screenshake effect of the given intensity. | `[1, 30]`, `[.5, 10]` |
| `set_npc_voice` | Voice ID | Switch the NPC's voice/audio profile. | `beanies` |
| `set_organ_name` | String | Set the name of the Organ Grinder (used during naming sequence). | `"Tyler"`, `"Tyler"` |
| `set_state` | State Name | Change the NPC's animation/camera state (e.g. `idle`, `closeup`, `zoomedout`). | `verycloseup`, `closeup`, `zoomedout` |
| `sfx` | Sound ID | Play a sound effect. | `BeaniesEnding_Banging`, `Intro_LabDisposal`, `PickupCoin` |
| `sidequest_fail` | (none) | Mark the current sidequest as failed. |  |
| `sidequest_reward` | (none) | Grant the player the reward for completing the current sidequest. |  |
| `tooltip_dialog` | String (loc key) | Display a tooltip-style dialogue popup. | `NPC_JACK_SHOP_TOOLTIP`, `NPC_ORGANGRINDER_SHOP_TOOLTIP`, `NPC_TRACY_SHOP_TOOLTIP` |
| `trigger_unlock` | Unlock ID | Fire a progression unlock trigger by ID. | `song_unlock_get_in_the_cage`, `time_machine_quest_begin`, `quest_begin_receiver2` |
| `unlock_class` | Class Name | Unlock a player class for use in future runs. | `Medic`, `Thief`, `Necromancer` |
| `unlock_controls` | Number (1) | Re-enable player input after a `lock_controls`. | `1`, `1`, `1` |
| `unlock_mouse` | Number (1) | Re-enable mouse cursor input. |  |
| `wait_for` | Enum | Pause execution until a specific engine event fires. | `choose_cat1`, `choose_cat2`, `reject_cat` |
| `wait_for_cancel` | Integer | Pause execution for N seconds, or until the player cancels if the sequence is cancelable. | `1`, `1`, `1` |

---

## NPC Sequence Reference

Each NPC has a set of named sequences. These are the trigger points the engine
calls into — you can hook custom dialogue or reward logic by matching these names.

### Tracy Progression

- **File:** `npc_scripts/tracy_progression.gon`
- **NPC:** `Tracy`
- **Movieclip:** `TracyOffice`
- **States:** `idle`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `also` | `dialog` |
| `cant_afford` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `hide_text` | `cancelable`, `dialog_and_autopass` |
| `out_of_stock` | `dialog`, `set_state` |
| `purchase_item` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `tooltip` | `cancelable`, `tooltip_dialog`, `wait_for_cancel` |
| `tracy_blankcollar1` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_blankcollar2` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_blankcollar3` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodbonus1` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage1` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage10` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage2` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage3` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage4` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage5` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage6` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage7` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage8` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_foodstorage9` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_idol1` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_idol2` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_idol3` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_idol4` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_idol5` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_idol6` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_idol7` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_introduction` | `begin_accepting_cats`, `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_kaijufight` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_max1` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_max2` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_max3` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_max4` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_max5` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_max_intro` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `tracy_max_repeating` | `do_random_sequence` |
| `unknown` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `unprompted` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |

---

### Tracy Adventure Shop Script

- **File:** `npc_scripts/tracy_adventure_shop_script.gon`
- **NPC:** `Tracy`
- **Movieclip:** `Shop`
- **States:** `idle`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `cant_afford` | `do_random_sequence` |
| `cant_afford_a` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `cant_afford_b` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `cant_afford_c` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `cant_afford_d` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `cant_afford_iceage` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `cant_afford_jurassic` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `cant_afford_moon` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `cant_afford_theend` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `hide_text` | `cancelable`, `dialog_and_autopass` |
| `purchase_item` | `do_random_sequence` |
| `purchase_item_a` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `purchase_item_b` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `purchase_item_c` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `purchase_item_d` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `purchase_item_iceage` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `purchase_item_jurassic` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `purchase_item_moon` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `purchase_item_theend` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `tooltip` | `cancelable`, `tooltip_dialog`, `wait_for_cancel` |
| `welcome` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_boneyard` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_bunker` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_caves` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_core` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_crater` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_desert` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_future` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_iceage` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_junkyard` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_jurassic` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_lab` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_moon` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_sewers` | `cancelable`, `dialog`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_theend` | `cancelable`, `dialog`, `dialog_and_autopass`, `set_npc_voice`, `wait_for_cancel` |
| `welcome_water` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `welcome_water_cheap` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |

---

### Jack Progression

- **File:** `npc_scripts/jack_progression.gon`
- **NPC:** `BabyJack`
- **Movieclip:** `JackOffice`
- **States:** `idle`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `Jack_Gainaltfurniture` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `also` | `dialog` |
| `cant_afford` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `hide_text` | `cancelable`, `dialog_and_autopass` |
| `jack_begin_accepting_cats` | `begin_accepting_cats`, `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_desert_intro` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_max1` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_max2` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_max3` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_max4` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_max5` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_max_intro` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_max_repeating` | `do_random_sequence` |
| `jack_shopupgrade1` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_shopupgrade2` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_shopupgrade3` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_shopupgrade4` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `jack_zara` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `out_of_stock` | `dialog`, `set_state` |
| `purchase_item` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `tooltip` | `cancelable`, `tooltip_dialog`, `wait_for_cancel` |
| `unknown` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `unprompted` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |

---

### Frank Progression

- **File:** `npc_scripts/frank_progression.gon`
- **NPC:** `Frank`
- **Movieclip:** `FrankOffice`
- **States:** `idle`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `also` | `dialog` |
| `forward_to_tips` | `do_random_sequence` |
| `frank_caves_intro` | `dialog`, `set_state` |
| `frank_ending` | `dialog`, `set_state` |
| `frank_max1` | `dialog`, `get`, `set_state` |
| `frank_max2` | `dialog`, `get`, `set_state` |
| `frank_max3` | `dialog`, `get`, `set_state` |
| `frank_max4` | `dialog`, `get`, `set_state` |
| `frank_max5` | `dialog`, `get`, `set_state` |
| `frank_max_intro` | `dialog`, `get`, `set_state` |
| `frank_max_repeating` | `do_random_sequence` |
| `frank_terminator2` | `dialog`, `set_state` |
| `frank_tips_1` | `dialog` |
| `frank_tips_10` | `dialog` |
| `frank_tips_2` | `dialog` |
| `frank_tips_3` | `dialog` |
| `frank_tips_4` | `dialog` |
| `frank_tips_5` | `dialog` |
| `frank_tips_6` | `dialog` |
| `frank_tips_7` | `dialog` |
| `frank_tips_8` | `dialog` |
| `frank_tips_9` | `dialog` |
| `house_upgrade_4throom` | `dialog`, `get`, `set_state` |
| `house_upgrade_attic` | `dialog`, `get`, `set_state` |
| `house_upgrade_basement` | `dialog`, `get` |
| `house_upgrade_basement2` | `dialog`, `get` |
| `house_upgrade_basement3` | `dialog`, `get` |
| `house_upgrade_basement4` | `dialog`, `get` |
| `house_upgrade_basement5` | `dialog`, `get` |
| `house_upgrade_largehouse` | `dialog`, `get`, `set_state` |
| `house_upgrade_mediumhouse` | `dialog`, `get`, `set_state` |
| `unknown` | `dialog`, `get` |
| `unprompted` | `do_random_sequence` |
| `unprompted_a` | `dialog`, `do_sequence` |
| `unprompted_b` | `dialog`, `do_sequence` |
| `unprompted_c` | `dialog`, `do_sequence` |
| `unprompted_d` | `dialog`, `do_sequence` |
| `unprompted_e` | `dialog`, `do_sequence` |
| `unprompted_f` | `dialog`, `do_sequence` |
| `unprompted_g` | `dialog`, `do_sequence` |
| `unprompted_h` | `dialog`, `do_sequence` |
| `unprompted_i` | `dialog`, `do_sequence` |

---

### Beanies Progression

- **File:** `npc_scripts/beanies_progression.gon`
- **NPC:** `Beanies`
- **Movieclip:** `BeaniesOffice`
- **States:** `idle`, `verycloseup`, `closeup`, `zoomedout`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `also` | `dialog` |
| `beanies_begin_accepting_cats` | `begin_accepting_cats`, `dialog`, `set_state` |
| `beanies_bombquest_2` | `dialog`, `set_state` |
| `beanies_bombquest_3` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_bombquest_amnesia` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_bombquest_begin` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_bombquest_fail_jarofblood` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_bombquest_fail_jarofchaos` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_bombquest_fail_jarofradiation` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_bombquest_fail_nuke` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_future_intro` | `dialog`, `set_state` |
| `beanies_hitler3` | `dialog`, `set_state` |
| `beanies_hitler3_defeat` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_iloveyou` | `dialog` |
| `beanies_jurassic_intro` | `dialog`, `set_state` |
| `beanies_lab_intro` | `dialog`, `play_cutscene`, `restart_npc_music`, `set_state`, `trigger_unlock` |
| `beanies_quest_complete` | `gather_questitem_info` |
| `beanies_quest_fail` | `gather_questitem_info` |
| `beanies_quests_intro` | `dialog`, `gather_questitem_info`, `get`, `set_state` |
| `beanies_quests_repeat` | `dialog`, `gather_questitem_info`, `get`, `set_state` |
| `beanies_screenshake_test` | `dialog`, `screenshake`, `sfx` |
| `beanies_seefuture` | `dialog`, `set_state` |
| `beanies_seetheend` | `dialog`, `set_state` |
| `beanies_terminator1_defeat` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_terminator2_defeat` | `dialog`, `set_state`, `trigger_unlock` |
| `beanies_theend_intro` | `dialog`, `set_state` |
| `beanies_timemachine_2` | `dialog`, `set_state` |
| `beanies_timemachine_intro` | `dialog`, `set_state`, `trigger_unlock` |
| `beaniesquest_complete_` | `get` |
| `beaniesquest_complete_AI` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_AirHorn` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_AngryFace` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_AnimalHands` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_BubbleBoy` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_ChadImplant` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_ChaosDevice` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_DimensionalDivider` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_DiseaseJar` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_ExperimentalTreatment` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_FartFace` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_FigLeaf` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_Generic` | `dialog`, `get` |
| `beaniesquest_complete_GlassCannon` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_HardPill` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_HiveMind` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_MagicMirror` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_MeStone` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_MultilinkCable` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_MysteriousDice` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_MysteriousGlasses` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_NDEDevice` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_NuclearKnife` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_PartialLobotomy` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_PartyDetonator` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_PersonalHeater` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_PersuasionDevice` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_PrincessHat` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_RealityScrambler` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_Redacted` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_SpiderInjector` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_Stopwatch` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_StorageLocker` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_TheIOU` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_TheLoner` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_Trapfest99` | `dialog`, `get`, `set_state` |
| `beaniesquest_complete_UltraVision3000` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_` | `get` |
| `beaniesquest_fail_AI` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_AirHorn` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_AngryFace` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_AnimalHands` | `dialog`, `get` |
| `beaniesquest_fail_BubbleBoy` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_ChadImplant` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_ChaosDevice` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_DimensionalDivider` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_DiseaseJar` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_ExperimentalTreatment` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_FartFace` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_FigLeaf` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_Generic` | `dialog`, `get` |
| `beaniesquest_fail_GlassCannon` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_HardPill` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_HiveMind` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_MagicMirror` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_MeStone` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_MultilinkCable` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_MysteriousDice` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_MysteriousGlasses` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_NDEDevice` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_NuclearKnife` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_PartialLobotomy` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_PartyDetonator` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_PersonalHeater` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_PersuasionDevice` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_PrincessHat` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_RealityScrambler` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_Redacted` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_SpiderInjector` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_Stopwatch` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_StorageLocker` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_TheIOU` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_TheLoner` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_Trapfest99` | `dialog`, `get`, `set_state` |
| `beaniesquest_fail_UltraVision3000` | `dialog`, `get`, `set_state` |
| `beaniesquest_intro_` | — |
| `beaniesquest_intro_AI` | `dialog`, `set_state` |
| `beaniesquest_intro_AirHorn` | `dialog`, `set_state` |
| `beaniesquest_intro_AngryFace` | `dialog`, `set_state` |
| `beaniesquest_intro_AnimalHands` | `dialog`, `set_state` |
| `beaniesquest_intro_BubbleBoy` | `dialog`, `set_state` |
| `beaniesquest_intro_ChadImplant` | `dialog`, `set_state` |
| `beaniesquest_intro_ChaosDevice` | `dialog`, `set_state` |
| `beaniesquest_intro_DimensionalDivider` | `dialog`, `set_state` |
| `beaniesquest_intro_DiseaseJar` | `dialog`, `set_state` |
| `beaniesquest_intro_ExperimentalTreatment` | `dialog`, `set_state` |
| `beaniesquest_intro_FartFace` | `dialog`, `set_state` |
| `beaniesquest_intro_FigLeaf` | `dialog`, `set_state` |
| `beaniesquest_intro_Generic` | `dialog` |
| `beaniesquest_intro_GlassCannon` | `dialog`, `set_state` |
| `beaniesquest_intro_HardPill` | `dialog`, `set_state` |
| `beaniesquest_intro_HiveMind` | `dialog`, `set_state` |
| `beaniesquest_intro_MagicMirror` | `dialog`, `set_state` |
| `beaniesquest_intro_MeStone` | `dialog`, `set_state` |
| `beaniesquest_intro_MultilinkCable` | `dialog`, `set_state` |
| `beaniesquest_intro_MysteriousDice` | `dialog`, `set_state` |
| `beaniesquest_intro_MysteriousGlasses` | `dialog`, `set_state` |
| `beaniesquest_intro_NDEDevice` | `dialog`, `set_state` |
| `beaniesquest_intro_NuclearKnife` | `dialog`, `set_state` |
| `beaniesquest_intro_PartialLobotomy` | `dialog`, `set_state` |
| `beaniesquest_intro_PartyDetonator` | `dialog`, `set_state` |
| `beaniesquest_intro_PersonalHeater` | `dialog`, `set_state` |
| `beaniesquest_intro_PersuasionDevice` | `dialog`, `set_state` |
| `beaniesquest_intro_PrincessHat` | `dialog`, `set_state` |
| `beaniesquest_intro_RealityScrambler` | `dialog`, `set_state` |
| `beaniesquest_intro_Redacted` | `dialog`, `set_state` |
| `beaniesquest_intro_SpiderInjector` | `dialog`, `set_state` |
| `beaniesquest_intro_Stopwatch` | `dialog`, `set_state` |
| `beaniesquest_intro_StorageLocker` | `dialog`, `set_state` |
| `beaniesquest_intro_TheIOU` | `dialog`, `set_state` |
| `beaniesquest_intro_TheLoner` | `dialog` |
| `beaniesquest_intro_Trapfest99` | `dialog`, `set_state` |
| `beaniesquest_intro_UltraVision3000` | `dialog`, `set_state` |
| `unknown` | `dialog`, `get` |
| `unprompted` | `do_random_sequence` |
| `unprompted1` | `dialog` |
| `unprompted2` | `dialog` |
| `unprompted3` | `dialog` |
| `unprompted4` | `dialog` |
| `unprompted5` | `dialog` |
| `unprompted6` | `dialog` |

---

### Beanies Gameintro

- **File:** `npc_scripts/beanies_gameintro.gon`
- **NPC:** `Beanies`
- **Movieclip:** `BeaniesIntro`
- **States:** `verycloseup`, `closeup`, `choosecats`, `zoomedout`, `closerup`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `intro` | `dialog`, `dialog_and_autopass`, `lock_controls`, `set_state`, `sfx`, `unlock_controls`, `wait_for` |

---

### Beanies Gameending

- **File:** `npc_scripts/beanies_gameending.gon`
- **NPC:** `Beanies`
- **Movieclip:** `BeaniesTimeMachine`
- **States:** `idle`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `ending` | `dialog`, `screenshake`, `sfx` |

---

### Organ Progression

- **File:** `npc_scripts/organ_progression.gon`
- **NPC:** `OrganGrinder`
- **Movieclip:** `OrganOffice`
- **States:** `idle`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `also` | `dialog` |
| `collected_new_items` | `dialog`, `dialog_and_autopass`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `collected_nothing` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `gone` | `set_state` |
| `hide_text` | `cancelable`, `dialog_and_autopass` |
| `organ_boneyard_intro` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_intro` | `begin_accepting_cats`, `dialog`, `dialog_and_autopass`, `lock_controls`, `set_organ_name`, `set_state`, `unlock_controls` |
| `organ_max1` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_max2` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_max3` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_max4` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_max5` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_max_intro` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_max_repeating` | `do_random_sequence` |
| `organ_rename` | `dialog`, `lock_controls`, `set_organ_name`, `set_state`, `unlock_controls` |
| `organ_throbbingdomain_intro` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_tina3` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_unlock` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_upgrade1` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_upgrade2` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_upgrade3` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_upgrade4` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_upgrade5` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `organ_upgrade6` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `out_of_stock` | `dialog`, `set_state` |
| `purchase_item` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |
| `tooltip` | `cancelable`, `tooltip_dialog`, `wait_for_cancel` |
| `unknown` | `dialog`, `get`, `lock_controls`, `set_state`, `unlock_controls` |
| `unprompted` | `cancelable`, `dialog_and_autopass`, `wait_for_cancel` |

---

### Tink Progression

- **File:** `npc_scripts/tink_progression.gon`
- **NPC:** `Tink`
- **Movieclip:** `TinkOffice`
- **States:** `idle`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `also` | `dialog` |
| `forward_to_tips` | `do_random_sequence` |
| `tink_aggression` | `dialog`, `get`, `set_state` |
| `tink_basestats` | `dialog`, `get`, `set_state` |
| `tink_begin_accepting_cats` | `begin_accepting_cats`, `dialog`, `set_state` |
| `tink_inbreeding` | `dialog`, `get`, `set_state` |
| `tink_max1` | `dialog`, `get`, `set_state` |
| `tink_max10` | `dialog`, `get`, `set_state` |
| `tink_max2` | `dialog`, `get`, `set_state` |
| `tink_max3` | `dialog`, `get`, `set_state` |
| `tink_max4` | `dialog`, `get`, `set_state` |
| `tink_max5` | `dialog`, `get`, `set_state` |
| `tink_max6` | `dialog`, `get` |
| `tink_max7` | `dialog`, `get`, `set_state` |
| `tink_max8` | `dialog`, `get`, `set_state` |
| `tink_max9` | `dialog`, `get`, `set_state` |
| `tink_max_intro` | `dialog`, `get`, `set_state` |
| `tink_max_repeating` | `do_random_sequence` |
| `tink_prettybow` | `dialog`, `get`, `set_state` |
| `tink_relationships` | `dialog`, `get`, `set_state` |
| `tink_sexuality` | `dialog`, `get`, `set_state` |
| `tink_tags` | `dialog`, `get`, `set_state` |
| `tink_terminator` | `dialog`, `set_state` |
| `tink_tina2` | `dialog`, `set_state` |
| `tink_tips_appeal` | `dialog` |
| `tink_tips_basestats` | `dialog` |
| `tink_tips_cleaning` | `dialog` |
| `tink_tips_comfort` | `dialog` |
| `tink_tips_health` | `dialog` |
| `tink_tips_inbreeding` | `dialog` |
| `tink_tips_intro` | `dialog`, `do_sequence` |
| `tink_tips_multiclassing` | `dialog` |
| `tink_tips_mutation` | `dialog` |
| `tink_tips_stimulation` | `dialog` |
| `unknown` | `dialog`, `get` |
| `unprompted` | `do_random_sequence` |
| `unprompted_a` | `dialog`, `do_sequence` |
| `unprompted_b` | `dialog`, `do_sequence` |
| `unprompted_c` | `dialog`, `do_sequence` |
| `unprompted_d` | `dialog`, `do_sequence` |
| `unprompted_e` | `dialog`, `do_sequence` |
| `unprompted_f` | `dialog`, `do_sequence` |
| `unprompted_g` | `dialog`, `do_sequence` |
| `unprompted_h` | `dialog`, `do_sequence` |
| `unprompted_i` | `dialog`, `do_sequence` |

---

### Steven Progression

- **File:** `npc_scripts/steven_progression.gon`
- **NPC:** `Steven`
- **Movieclip:** `N/A`
- **States:** `idle`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `also` | `dialog` |
| `steven_100` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_introduction` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_milliontrashed` | `dialog`, `get`, `set_state` |
| `steven_postendgame` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_resummon` | `dialog`, `lock_controls`, `unlock_controls` |
| `steven_unlock_act1_crazy` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_unlock_act1_impossible` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_unlock_act2_crazy` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_unlock_act2_hard` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_unlock_act2_impossible` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_unlock_act3_crazy` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_unlock_act3_hard` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `steven_unlock_act3_impossible` | `dialog`, `lock_controls`, `set_state`, `unlock_controls` |
| `unknown` | `dialog`, `get` |
| `unprompted` | `do_random_sequence` |
| `unprompted_a` | `dialog` |
| `unprompted_b` | `dialog` |
| `unprompted_c` | `dialog` |
| `unprompted_d` | `dialog` |
| `unprompted_e` | `dialog` |
| `unprompted_f` | `dialog` |
| `unprompted_g` | `dialog` |
| `unprompted_h` | `dialog` |
| `unprompted_i` | `dialog` |

---

### Butch Progression

- **File:** `npc_scripts/butch_progression.gon`
- **NPC:** `Butch`
- **Movieclip:** `ButchOffice`
- **States:** `idle`, `verycloseup`, `closeup`, `zoomedout`

**Sequences:**

| Sequence Name | Engine Commands Used |
| :--- | :--- |
| `also` | `dialog` |
| `butch_begin_accepting_cats` | `begin_accepting_cats`, `dialog`, `set_state` |
| `butch_boneyard_intro` | `dialog`, `set_state` |
| `butch_first_house_boss_beat` | `dialog`, `set_state` |
| `butch_pyro` | `dialog`, `set_state` |
| `butch_tina1` | `dialog`, `set_state` |
| `butch_tips_backstab` | `dialog` |
| `butch_tips_charisma` | `dialog` |
| `butch_tips_combat` | `dialog` |
| `butch_tips_disorders` | `dialog` |
| `butch_tips_drafting` | `dialog` |
| `butch_tips_elements` | `dialog` |
| `butch_tips_hard` | `dialog` |
| `butch_tips_headhome` | `dialog` |
| `butch_tips_houseboss` | `dialog` |
| `butch_tips_info` | `dialog` |
| `butch_tips_intelligence` | `dialog` |
| `butch_tips_intro` | `dialog`, `do_sequence` |
| `butch_tips_items` | `dialog` |
| `butch_tips_lesscats` | `dialog` |
| `butch_tips_magicdamage` | `dialog` |
| `butch_tips_passives` | `dialog` |
| `butch_tips_reorient` | `dialog` |
| `butch_tips_rewards` | `dialog` |
| `butch_tips_tacticalview` | `dialog` |
| `butch_tips_turnorder` | `dialog` |
| `butch_tips_wellrounded` | `dialog` |
| `class_unlock_butcher` | `dialog`, `set_state`, `unlock_class` |
| `class_unlock_druid` | `dialog`, `unlock_class` |
| `class_unlock_jester` | `dialog`, `set_state`, `unlock_class` |
| `class_unlock_medic` | `dialog`, `set_state`, `unlock_class` |
| `class_unlock_monk` | `dialog`, `set_state`, `unlock_class` |
| `class_unlock_necromancer` | `dialog`, `set_state`, `unlock_class` |
| `class_unlock_psychic` | `dialog`, `set_state`, `unlock_class` |
| `class_unlock_thief` | `dialog`, `set_state`, `unlock_class` |
| `class_unlock_tinkerer` | `dialog`, `set_state`, `unlock_class` |
| `forward_to_tips` | `do_random_sequence` |
| `test_gamepad_prompts` | `dialog` |
| `unknown` | `dialog`, `get` |
| `unprompted` | `do_random_sequence` |
| `unprompted_a` | `dialog`, `do_sequence` |
| `unprompted_b` | `dialog`, `do_sequence` |
| `unprompted_c` | `dialog`, `do_sequence` |
| `unprompted_d` | `dialog`, `do_sequence` |
| `unprompted_e` | `dialog`, `do_sequence` |
| `unprompted_f` | `dialog`, `do_sequence` |
| `unprompted_g` | `dialog`, `do_sequence` |
| `unprompted_h` | `dialog`, `do_sequence` |
| `unprompted_i` | `dialog`, `do_sequence` |
| `upgrade_storage_1` | `dialog`, `get`, `set_state` |
| `upgrade_storage_2` | `dialog`, `get`, `set_state` |
| `upgrade_storage_3` | `dialog`, `get`, `set_state` |
| `upgrade_storage_4` | `dialog`, `get`, `set_state` |
| `upgrade_storage_5` | `dialog`, `get`, `set_state` |
| `upgrade_storage_6` | `dialog`, `get`, `set_state` |
| `upgrade_storage_7` | `dialog`, `get`, `set_state` |
| `upgrade_storage_max1` | `dialog`, `get`, `set_state` |
| `upgrade_storage_max2` | `dialog`, `get` |
| `upgrade_storage_max3` | `dialog`, `get`, `set_state` |
| `upgrade_storage_max4` | `dialog`, `get`, `set_state` |
| `upgrade_storage_max5` | `dialog`, `get`, `set_state` |
| `upgrade_storage_repeating_crazy` | `do_random_sequence` |
| `upgrade_storage_repeating_hard` | `do_random_sequence` |
| `upgrade_storage_repeating_impossible` | `do_random_sequence` |
| `upgrade_storage_repeating_intro` | `dialog`, `get`, `set_state` |
| `upgrade_storage_repeating_normal` | `do_random_sequence` |

---
