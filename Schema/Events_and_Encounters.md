# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Events & Encounters

> **Associated Files:** `data/events/`


### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 214

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4118 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 890 |
| [`intro`](./Events_and_Encounters.md#context-intro) | Block | Event Node: The initial text block when a story event first loads. | 214 |
| [`main`](./Events_and_Encounters.md#context-main) | Block | Event Node: The central hub or recurring menu of a story event. | 214 |
| [`label`](./Strings.md#string-label) | String |  | 16 |
| `stat` | Mixed |  | 16 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 12 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 8 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 8 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 4 |
| `stat_max` | Number |  | 4 |
| `stat_min` | Number |  | 4 |
| [`open`](./Events_and_Encounters.md#context-open) | Block | Examples: `{ ... }` | 3 |
| `pick` | Block | Examples: `{ ... }` | 3 |
| [`ignore`](./Events_and_Encounters.md#context-ignore) | Block | Event Node: Story branch or dialog option representing the \'Ignore\' action. | 2 |
| `cha` | Number |  | 2 |
| `con` | Number |  | 2 |
| `int` | Number |  | 2 |
| `lck` | Number |  | 2 |
| `spd` | Number |  | 2 |
| `str` | Number |  | 2 |
| [`destroy`](./Events_and_Encounters.md#context-destroy) | Block | Event Node: Story branch or dialog option representing the \'Destroy\' action. | 1 |
| [`examine`](./Events_and_Encounters.md#context-examine) | Block | Examples: `{ ... }` | 1 |
| [`smash`](./Events_and_Encounters.md#context-smash) | Block | Examples: `{ ... }` | 1 |
| `buy2` | Block | Examples: `{ ... }` | 1 |
| `buy3` | Block | Examples: `{ ... }` | 1 |
| `dex` | Number |  | 1 |

</details>

---

### Context: `reward`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 757

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward), [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1364 |

</details>

---

### Context: `common`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 633

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 658 |
| [`damage`](./Arrays.md#array-damage) | Array | Event Node: Story branch or dialog option representing the 'Damage' action. | 35 |

</details>

---

### Context: `rare`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 633

> **Referenced by:** [`attack`](./Events_and_Encounters.md#context-attack), [`good`](./Events_and_Encounters.md#context-good), [`loot`](./Events_and_Encounters.md#context-loot), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options), [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 705 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 18 |

</details>

---

### Context: `good`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 550

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`a`](./Events_and_Encounters.md#context-a), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`altar_sacrifice`](./Events_and_Encounters.md#context-altar_sacrifice), [`arm`](./Events_and_Encounters.md#context-arm), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`attack`](./Events_and_Encounters.md#context-attack), [`b`](./Events_and_Encounters.md#context-b), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`bite`](./Events_and_Encounters.md#context-bite), [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`boogers`](./Events_and_Encounters.md#context-boogers), [`book`](./Events_and_Encounters.md#context-book), [`brace`](./Events_and_Encounters.md#context-brace), [`break_ice`](./Events_and_Encounters.md#context-break_ice), and 177 more...

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 464 |

</details>

---

### Context: `bad`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 341

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`arm`](./Events_and_Encounters.md#context-arm), [`attack`](./Events_and_Encounters.md#context-attack), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`bite`](./Events_and_Encounters.md#context-bite), [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`body`](./Events_and_Encounters.md#context-body), [`break_ice`](./Events_and_Encounters.md#context-break_ice), [`break_lock`](./Events_and_Encounters.md#context-break_lock), [`bribe`](./Events_and_Encounters.md#context-bribe), [`catch`](./Events_and_Encounters.md#context-catch), [`challenge_to_game`](./Events_and_Encounters.md#context-challenge_to_game), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`climb`](./Events_and_Encounters.md#context-climb), [`comfort`](./Events_and_Encounters.md#context-comfort), [`communicate`](./Events_and_Encounters.md#context-communicate), [`concheck`](./Events_and_Encounters.md#context-concheck), and 106 more...

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 249 |

</details>

---

### Context: `intro`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 214

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cat_choice`](./Enums.md#enum-cat_choice) | Enum |  | 214 |
| [`event_clip`](./Enums.md#enum-event_clip) | Enum |  | 214 |
| [`subject_clip`](./Enums.md#enum-subject_clip) | Enum |  | 214 |
| [`subject_frame`](./Enums.md#enum-subject_frame) | Enum |  | 214 |
| [`title`](./Strings.md#string-title) | String |  | 214 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 214 |
| [`choose_cat_with_item`](./Enums.md#enum-choose_cat_with_item) | Enum |  | 17 |
| `different_from_last_x_cats` | Number |  | 3 |
| `subject_frame_inner` | Number |  | 3 |
| [`choose_cat_with_highest_stat`](./Math_Equations.md) | Equation |  | 1 |
| [`choose_cat_with_item_slot_equipped`](./Enums.md#enum-choose_cat_with_item_slot_equipped) | Enum |  | 1 |
| `choose_cat_with_min_health` | Number |  | 1 |
| `choose_cat_with_most_injuries` | Boolean |  | 1 |
| `choose_cat_with_parasite` | Boolean |  | 1 |

</details>

---

### Context: `main`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 214

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 220 |

</details>

---

### Context: `options`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 210

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 262 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 144 |
| [`ignore`](./Events_and_Encounters.md#context-ignore) | Block | Event Node: Story branch or dialog option representing the \'Ignore\' action. | 55 |
| [`examine`](./Events_and_Encounters.md#context-examine) | Block | Event Node: Story branch or dialog option representing the \'Examine\' action. | 43 |
| [`loot`](./Events_and_Encounters.md#context-loot) | Block | Event Node: Story branch or dialog option representing the \'Loot\' action. | 25 |
| [`eat`](./Events_and_Encounters.md#context-eat) | Block | Event Node: Story branch or dialog option representing the \'Eat\' action. | 23 |
| [`smash`](./Events_and_Encounters.md#context-smash) | Block | Event Node: Story branch or dialog option representing the \'Smash\' action. | 15 |
| [`destroy`](./Events_and_Encounters.md#context-destroy) | Block | Event Node: Story branch or dialog option representing the \'Destroy\' action. | 13 |
| [`bash`](./Events_and_Encounters.md#context-bash) | Block | Event Node: Story branch or dialog option representing the \'Bash\' action. | 12 |
| [`sneak`](./Events_and_Encounters.md#context-sneak) | Block | Event Node: Story branch or dialog option representing the \'Sneak\' action. | 11 |
| [`open`](./Events_and_Encounters.md#context-open) | Block | Event Node: Story branch or dialog option representing the \'Open\' action. | 8 |
| [`take`](./Events_and_Encounters.md#context-take) | Block | Event Node: Story branch or dialog option representing the \'Take\' action. | 8 |
| [`a`](./Events_and_Encounters.md#context-a) | Block | Event Node: Story branch or dialog option representing the \'A\' action. | 7 |
| [`attack`](./Events_and_Encounters.md#context-attack) | Block | Event Node: Story branch or dialog option representing the \'Attack\' action. | 7 |
| [`b`](./Events_and_Encounters.md#context-b) | Block | Event Node: Story branch or dialog option representing the \'B\' action. | 7 |
| [`c`](./Events_and_Encounters.md#context-c) | Block | Event Node: Story branch or dialog option representing the \'C\' action. | 7 |
| [`charm`](./Events_and_Encounters.md#context-charm) | Block | Event Node: Story branch or dialog option representing the \'Charm\' action. | 7 |
| [`fight`](./Events_and_Encounters.md#context-fight) | Block | Event Node: Story branch or dialog option representing the \'Fight\' action. | 7 |
| [`touch`](./Events_and_Encounters.md#context-touch) | Block | Event Node: Story branch or dialog option representing the \'Touch\' action. | 7 |
| [`activate_p`](./Events_and_Encounters.md#context-activate_p) | Block | Event Node: Story branch or dialog option representing the 'Activate P' action. | 6 |
| [`activate_z`](./Events_and_Encounters.md#context-activate_z) | Block | Event Node: Story branch or dialog option representing the 'Activate Z' action. | 6 |
| [`d`](./Events_and_Encounters.md#context-d) | Block | Event Node: Story branch or dialog option representing the \'D\' action. | 6 |
| [`enter`](./Events_and_Encounters.md#context-enter) | Block | Event Node: Story branch or dialog option representing the \'Enter\' action. | 6 |
| [`inspect`](./Events_and_Encounters.md#context-inspect) | Block | Event Node: Story branch or dialog option representing the \'Inspect\' action. | 6 |
| [`lick`](./Events_and_Encounters.md#context-lick) | Block | Event Node: Story branch or dialog option representing the \'Lick\' action. | 6 |
| [`drink`](./Events_and_Encounters.md#context-drink) | Block | Event Node: Story branch or dialog option representing the \'Drink\' action. | 5 |
| [`kiss`](./Events_and_Encounters.md#context-kiss) | Block | Event Node: Story branch or dialog option representing the \'Kiss\' action. | 5 |
| [`run`](./Events_and_Encounters.md#context-run) | Block | Event Node: Story branch or dialog option representing the \'Run\' action. | 5 |
| [`bite`](./Events_and_Encounters.md#context-bite) | Block | Event Node: Story branch or dialog option representing the 'Bite' action. | 4 |
| [`damage`](./Events_and_Encounters.md#context-damage) | Block | Event Node: Story branch or dialog option representing the 'Damage' action. | 4 |
| [`go_around`](./Events_and_Encounters.md#context-go_around) | Block | Event Node: Story branch or dialog option representing the \'Go Around\' action. | 4 |
| [`home`](./Events_and_Encounters.md#context-home) | Block | Event Node: Story branch or dialog option representing the 'Home' action. | 4 |
| [`past`](./Events_and_Encounters.md#context-past) | Block | Event Node: Story branch or dialog option representing the 'Past' action. | 4 |
| [`skip`](./Events_and_Encounters.md#context-skip) | Block | Event Node: Story branch or dialog option representing the \'Skip\' action. | 4 |
| [`investigate`](./Events_and_Encounters.md#context-investigate) | Block | Event Node: Story branch or dialog option representing the \'Investigate\' action. | 3 |
| [`repell`](./Events_and_Encounters.md#context-repell) | Block | Event Node: Story branch or dialog option representing the \'Repell\' action. | 3 |
| [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna) | Block | Event Node: Story branch or dialog option representing the 'Attach Antenna' action. | 2 |
| [`boogers`](./Events_and_Encounters.md#context-boogers) | Block | Event Node: Story branch or dialog option representing the \'Boogers\' action. | 2 |
| [`copy`](./Events_and_Encounters.md#context-copy) | Block | Event Node: Story branch or dialog option representing the \'Copy\' action. | 2 |
| [`find_another_way`](./Events_and_Encounters.md#context-find_another_way) | Block | Event Node: Story branch or dialog option representing the \'Find Another Way\' action. | 2 |
| [`move_closer`](./Events_and_Encounters.md#context-move_closer) | Block | Event Node: Story branch or dialog option representing the \'Move Closer\' action. | 2 |
| [`play`](./Events_and_Encounters.md#context-play) | Block | Event Node: Story branch or dialog option representing the \'Play\' action. | 2 |
| [`poop`](./Events_and_Encounters.md#context-poop) | Block | Event Node: Story branch or dialog option representing the \'Poop\' action. | 2 |
| [`print`](./Events_and_Encounters.md#context-print) | Block | Event Node: Story branch or dialog option representing the \'Print\' action. | 2 |
| [`protection`](./Events_and_Encounters.md#context-protection) | Block | Event Node: Story branch or dialog option representing the \'Protection\' action. | 2 |
| [`repair`](./Events_and_Encounters.md#context-repair) | Block | Event Node: Story branch or dialog option representing the \'Repair\' action. | 2 |
| [`sacrifice`](./Events_and_Encounters.md#context-sacrifice) | Block | Event Node: Story branch or dialog option representing the \'Sacrifice\' action. | 2 |
| [`turnon`](./Events_and_Encounters.md#context-turnon) | Block | Event Node: Story branch or dialog option representing the \'Turnon\' action. | 2 |
| [`altar_sacrifice`](./Events_and_Encounters.md#context-altar_sacrifice) | Block | Event Action: Triggers the altar sacrifice progression logic. | 1 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`arm`](./Events_and_Encounters.md#context-arm) | Block | Event Node: Story branch or dialog option representing the \'Arm\' action. | 1 |
| [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier) | Block | Event Node: Story branch or dialog option representing the 'Attach Amplifier' action. | 1 |
| [`attach_leech`](./Events_and_Encounters.md#context-attach_leech) | Block | Event Node: Story branch or dialog option representing the 'Attach Leech' action. | 1 |
| [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt) | Block | Event Node: Story branch or dialog option representing the \'Bash Past Alt\' action. | 1 |
| [`bite_it_off`](./Events_and_Encounters.md#context-bite_it_off) | Block | Event Node: Story branch or dialog option representing the \'Bite It Off\' action. | 1 |
| [`blue_needle`](./Events_and_Encounters.md#context-blue_needle) | Block | Event Node: Story branch or dialog option representing the \'Blue Needle\' action. | 1 |
| [`blue`](./Events_and_Encounters.md#context-blue) | Block | Event Node: Story branch or dialog option representing the \'Blue\' action. | 1 |
| [`body`](./Events_and_Encounters.md#context-body) | Block | Event Node: Story branch or dialog option representing the 'Body' action. | 1 |
| [`book`](./Events_and_Encounters.md#context-book) | Block | Event Node: Story branch or dialog option representing the \'Book\' action. | 1 |
| [`brace`](./Events_and_Encounters.md#context-brace) | Block | Event Node: Story branch or dialog option representing the \'Brace\' action. | 1 |
| [`break_ice`](./Events_and_Encounters.md#context-break_ice) | Block | Event Node: Story branch or dialog option representing the \'Break Ice\' action. | 1 |
| [`break_lock`](./Events_and_Encounters.md#context-break_lock) | Block | Event Node: Story branch or dialog option representing the \'Break Lock\' action. | 1 |
| [`bribe`](./Events_and_Encounters.md#context-bribe) | Block | Event Node: Story branch or dialog option representing the 'Bribe' action. | 1 |
| [`button`](./Events_and_Encounters.md#context-button) | Block | Event Node: Story branch or dialog option representing the \'Button\' action. | 1 |
| [`buy1`](./Events_and_Encounters.md#context-buy1) | Block | Event Node: Story branch or dialog option representing the \'Buy1\' action. | 1 |
| [`catch`](./Events_and_Encounters.md#context-catch) | Block | Event Node: Story branch or dialog option representing the \'Catch\' action. | 1 |
| [`challenge_to_game`](./Events_and_Encounters.md#context-challenge_to_game) | Block | Event Node: Story branch or dialog option representing the \'Challenge To Game\' action. | 1 |
| [`chaos_ending`](./Events_and_Encounters.md#context-chaos_ending) | Block | Event Node: Triggers the Chaos Boss victory sequence. | 1 |
| [`chapter_cutscene`](./Events_and_Encounters.md#context-chapter_cutscene) | Block | Event Node: Triggers an intermission cutscene. | 1 |
| [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt) | Block | Event Node: Story branch or dialog option representing the \'Charm Past Alt\' action. | 1 |
| [`climb`](./Events_and_Encounters.md#context-climb) | Block | Event Node: Story branch or dialog option representing the \'Climb\' action. | 1 |
| [`comfort`](./Events_and_Encounters.md#context-comfort) | Block | Event Node: Story branch or dialog option representing the \'Comfort\' action. | 1 |
| [`communicate`](./Events_and_Encounters.md#context-communicate) | Block | Event Node: Story branch or dialog option representing the \'Communicate\' action. | 1 |
| [`concheck`](./Events_and_Encounters.md#context-concheck) | Block | Event Node: Stat check branch evaluating the \'con\' attribute. | 1 |
| [`counter`](./Events_and_Encounters.md#context-counter) | Block | Event Node: Story branch or dialog option representing the \'Counter\' action. | 1 |
| [`crack_open`](./Events_and_Encounters.md#context-crack_open) | Block | Event Node: Story branch or dialog option representing the \'Crack Open\' action. | 1 |
| [`cross`](./Events_and_Encounters.md#context-cross) | Block | Event Node: Story branch or dialog option representing the \'Cross\' action. | 1 |
| [`cut_wires`](./Events_and_Encounters.md#context-cut_wires) | Block | Event Node: Story branch or dialog option representing the \'Cut Wires\' action. | 1 |
| [`damage_1`](./Events_and_Encounters.md#context-damage_1) | Block | Event Node: Story branch or dialog option representing the \'Damage 1\' action. | 1 |
| [`damage_full`](./Events_and_Encounters.md#context-damage_full) | Block | Event Node: Story branch or dialog option representing the \'Damage Full\' action. | 1 |
| [`damage_half`](./Events_and_Encounters.md#context-damage_half) | Block | Event Node: Story branch or dialog option representing the \'Damage Half\' action. | 1 |
| [`desert_cutscene`](./Events_and_Encounters.md#context-desert_cutscene) | Block | Event Node: Triggers the desert transition cutscene. | 1 |
| [`dexcheck`](./Events_and_Encounters.md#context-dexcheck) | Block | Event Node: Stat check branch evaluating the \'dex\' attribute. | 1 |
| [`dig`](./Events_and_Encounters.md#context-dig) | Block | Event Node: Story branch or dialog option representing the \'Dig\' action. | 1 |
| [`disarm`](./Events_and_Encounters.md#context-disarm) | Block | Event Node: Story branch or dialog option representing the \'Disarm\' action. | 1 |
| [`dive`](./Events_and_Encounters.md#context-dive) | Block | Event Node: Story branch or dialog option representing the \'Dive\' action. | 1 |
| [`donate_10`](./Events_and_Encounters.md#context-donate_10) | Block | Event Node: Story branch or dialog option representing the \'Donate 10\' action. | 1 |
| [`donate_15`](./Events_and_Encounters.md#context-donate_15) | Block | Event Node: Story branch or dialog option representing the \'Donate 15\' action. | 1 |
| [`donate_20`](./Events_and_Encounters.md#context-donate_20) | Block | Event Node: Story branch or dialog option representing the \'Donate 20\' action. | 1 |
| [`donate_5`](./Events_and_Encounters.md#context-donate_5) | Block | Event Node: Story branch or dialog option representing the \'Donate 5\' action. | 1 |
| [`donate`](./Events_and_Encounters.md#context-donate) | Block | Event Node: Story branch or dialog option representing the \'Donate\' action. | 1 |
| [`double`](./Events_and_Encounters.md#context-double) | Block | Event Node: Story branch or dialog option representing the \'Double\' action. | 1 |
| [`eat_meat`](./Events_and_Encounters.md#context-eat_meat) | Block | Event Node: Story branch or dialog option representing the \'Eat Meat\' action. | 1 |
| [`enter_crater`](./Events_and_Encounters.md#context-enter_crater) | Block | Event Node: Story branch or dialog option representing the \'Enter Crater\' action. | 1 |
| [`face`](./Events_and_Encounters.md#context-face) | Block | Event Node: Story branch or dialog option representing the \'Face\' action. | 1 |
| [`fiddle`](./Events_and_Encounters.md#context-fiddle) | Block | Event Node: Story branch or dialog option representing the 'Fiddle' action. | 1 |
| [`fill_jar`](./Events_and_Encounters.md#context-fill_jar) | Block | Event Node: Story branch or dialog option representing the 'Fill Jar' action. | 1 |
| [`find`](./Events_and_Encounters.md#context-find) | Block | Event Node: Story branch or dialog option representing the \'Find\' action. | 1 |
| [`fire`](./Events_and_Encounters.md#context-fire) | Block | Event Node: Story branch or dialog option representing the \'Fire\' action. | 1 |
| [`flush_yourself`](./Events_and_Encounters.md#context-flush_yourself) | Block | Event Node: Story branch or dialog option representing the \'Flush Yourself\' action. | 1 |
| [`follow`](./Events_and_Encounters.md#context-follow) | Block | Event Node: Story branch or dialog option representing the \'Follow\' action. | 1 |
| [`free`](./Events_and_Encounters.md#context-free) | Block | Event Node: Story branch or dialog option representing the \'Free\' action. | 1 |
| [`future`](./Events_and_Encounters.md#context-future) | Block | Event Node: Story branch or dialog option representing the 'Future' action. | 1 |
| [`give_parasite`](./Events_and_Encounters.md#context-give_parasite) | Block | Event Action: Equips a parasite item to a character. | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the 'Good' action. | 1 |
| [`hack`](./Events_and_Encounters.md#context-hack) | Block | Event Node: Story branch or dialog option representing the \'Hack\' action. | 1 |
| [`head`](./Events_and_Encounters.md#context-head) | Block | Event Node: Story branch or dialog option representing the \'Head\' action. | 1 |
| [`holy`](./Events_and_Encounters.md#context-holy) | Block | Event Node: Story branch or dialog option representing the \'Holy\' action. | 1 |
| [`hp`](./Events_and_Encounters.md#context-hp) | Block | Event Node: Story branch or dialog option representing the \'Hp\' action. | 1 |
| [`ice`](./Events_and_Encounters.md#context-ice) | Block | Event Node: Story branch or dialog option representing the \'Ice\' action. | 1 |
| [`infinite`](./Events_and_Encounters.md#context-infinite) | Block | Event Node: A looping or endlessly repeating story branch. | 1 |
| [`intcheck`](./Events_and_Encounters.md#context-intcheck) | Block | Event Node: Stat check branch evaluating the \'int\' attribute. | 1 |
| [`intimidation`](./Events_and_Encounters.md#context-intimidation) | Block | Event Node: Story branch or dialog option representing the \'Intimidation\' action. | 1 |
| [`itchies`](./Events_and_Encounters.md#context-itchies) | Block | Event Node: Story branch or dialog option representing the \'Itchies\' action. | 1 |
| [`join`](./Events_and_Encounters.md#context-join) | Block | Event Node: Story branch or dialog option representing the \'Join\' action. | 1 |
| [`jump_over`](./Events_and_Encounters.md#context-jump_over) | Block | Event Node: Story branch or dialog option representing the \'Jump Over\' action. | 1 |
| [`jump`](./Events_and_Encounters.md#context-jump) | Block | Event Node: Story branch or dialog option representing the \'Jump\' action. | 1 |
| [`keep_going`](./Events_and_Encounters.md#context-keep_going) | Block | Event Node: Story branch or dialog option representing the \'Keep Going\' action. | 1 |
| [`kiss_meat`](./Events_and_Encounters.md#context-kiss_meat) | Block | Event Node: Story branch or dialog option representing the \'Kiss Meat\' action. | 1 |
| [`knife`](./Events_and_Encounters.md#context-knife) | Block | Event Node: Story branch or dialog option representing the \'Knife\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`leave_it_in`](./Events_and_Encounters.md#context-leave_it_in) | Block | Event Node: Story branch or dialog option representing the \'Leave It In\' action. | 1 |
| [`leg`](./Events_and_Encounters.md#context-leg) | Block | Event Node: Story branch or dialog option representing the \'Leg\' action. | 1 |
| [`lever`](./Events_and_Encounters.md#context-lever) | Block | Event Node: Story branch or dialog option representing the \'Lever\' action. | 1 |
| [`lick_alt`](./Events_and_Encounters.md#context-lick_alt) | Block | Event Node: Story branch or dialog option representing the \'Lick Alt\' action. | 1 |
| [`lightning`](./Events_and_Encounters.md#context-lightning) | Block | Event Node: Story branch or dialog option representing the \'Lightning\' action. | 1 |
| [`listen`](./Events_and_Encounters.md#context-listen) | Block | Event Node: Story branch or dialog option representing the \'Listen\' action. | 1 |
| [`looks`](./Events_and_Encounters.md#context-looks) | Block | Event Node: Story branch or dialog option representing the 'Looks' action. | 1 |
| [`loot_heart`](./Events_and_Encounters.md#context-loot_heart) | Block | Event Node: Story branch or dialog option representing the 'Loot Heart' action. | 1 |
| [`makeup`](./Events_and_Encounters.md#context-makeup) | Block | Event Node: Story branch or dialog option representing the \'Makeup\' action. | 1 |
| [`mind`](./Events_and_Encounters.md#context-mind) | Block | Event Node: Story branch or dialog option representing the 'Mind' action. | 1 |
| [`neck`](./Events_and_Encounters.md#context-neck) | Block | Event Node: Story branch or dialog option representing the \'Neck\' action. | 1 |
| [`nothanks`](./Events_and_Encounters.md#context-nothanks) | Block | Event Node: Story branch or dialog option representing the \'Nothanks\' action. | 1 |
| [`outsmart`](./Events_and_Encounters.md#context-outsmart) | Block | Event Node: Story branch or dialog option representing the \'Outsmart\' action. | 1 |
| [`patch_up`](./Events_and_Encounters.md#context-patch_up) | Block | Event Node: Story branch or dialog option representing the \'Patch Up\' action. | 1 |
| [`pick_lock`](./Events_and_Encounters.md#context-pick_lock) | Block | Event Node: Story branch or dialog option representing the \'Pick Lock\' action. | 1 |
| [`pilfer`](./Events_and_Encounters.md#context-pilfer) | Block | Event Node: Story branch or dialog option representing the \'Pilfer\' action. | 1 |
| [`pirouette`](./Events_and_Encounters.md#context-pirouette) | Block | Event Node: Story branch or dialog option representing the \'Pirouette\' action. | 1 |
| [`place_gristle`](./Events_and_Encounters.md#context-place_gristle) | Block | Event Node: Story branch or dialog option representing the 'Place Gristle' action. | 1 |
| [`power`](./Events_and_Encounters.md#context-power) | Block | Event Node: Story branch or dialog option representing the 'Power' action. | 1 |
| [`pull_it_out`](./Events_and_Encounters.md#context-pull_it_out) | Block | Event Node: Story branch or dialog option representing the \'Pull It Out\' action. | 1 |
| [`pull_lever`](./Events_and_Encounters.md#context-pull_lever) | Block | Event Node: Story branch or dialog option representing the \'Pull Lever\' action. | 1 |
| [`pull`](./Events_and_Encounters.md#context-pull) | Block | Event Node: Story branch or dialog option representing the \'Pull\' action. | 1 |
| [`purify`](./Events_and_Encounters.md#context-purify) | Block | Event Node: Story branch or dialog option representing the \'Purify\' action. | 1 |
| [`push_buttons`](./Events_and_Encounters.md#context-push_buttons) | Block | Event Node: Story branch or dialog option representing the \'Push Buttons\' action. | 1 |
| [`push_through`](./Events_and_Encounters.md#context-push_through) | Block | Event Node: Story branch or dialog option representing the \'Push Through\' action. | 1 |
| [`put_in_coins`](./Events_and_Encounters.md#context-put_in_coins) | Block | Event Node: Story branch or dialog option representing the \'Put In Coins\' action. | 1 |
| [`put_out_of_misery`](./Events_and_Encounters.md#context-put_out_of_misery) | Block | Event Node: Story branch or dialog option representing the \'Put Out Of Misery\' action. | 1 |
| [`reach_inside`](./Events_and_Encounters.md#context-reach_inside) | Block | Event Node: Story branch or dialog option representing the \'Reach Inside\' action. | 1 |
| [`read`](./Events_and_Encounters.md#context-read) | Block | Event Node: Story branch or dialog option representing the \'Read\' action. | 1 |
| [`receive`](./Events_and_Encounters.md#context-receive) | Block | Event Node: Story branch or dialog option representing the \'Receive\' action. | 1 |
| [`red_needle`](./Events_and_Encounters.md#context-red_needle) | Block | Event Node: Story branch or dialog option representing the \'Red Needle\' action. | 1 |
| [`red`](./Events_and_Encounters.md#context-red) | Block | Event Node: Story branch or dialog option representing the \'Red\' action. | 1 |
| [`reflect`](./Events_and_Encounters.md#context-reflect) | Block | Event Node: Story branch or dialog option representing the \'Reflect\' action. | 1 |
| [`remove_the_nail`](./Events_and_Encounters.md#context-remove_the_nail) | Block | Event Node: Story branch or dialog option representing the \'Remove The Nail\' action. | 1 |
| [`remove`](./Events_and_Encounters.md#context-remove) | Block | Event Node: Story branch or dialog option representing the \'Remove\' action. | 1 |
| [`repair_quest`](./Events_and_Encounters.md#context-repair_quest) | Block | Event Node: Story branch or dialog option representing the 'Repair Quest' action. | 1 |
| [`rest`](./Events_and_Encounters.md#context-rest) | Block | Event Node: Story branch or dialog option representing the \'Rest\' action. | 1 |
| [`revive`](./Events_and_Encounters.md#context-revive) | Block | Event Node: Story branch or dialog option representing the \'Revive\' action. | 1 |
| [`rub`](./Events_and_Encounters.md#context-rub) | Block | Event Node: Story branch or dialog option representing the \'Rub\' action. | 1 |
| [`run_again`](./Events_and_Encounters.md#context-run_again) | Block | Event Node: Story branch or dialog option representing the \'Run Again\' action. | 1 |
| [`run_away`](./Events_and_Encounters.md#context-run_away) | Block | Event Node: Story branch or dialog option representing the \'Run Away\' action. | 1 |
| [`sacrifice_full_favor`](./Events_and_Encounters.md#context-sacrifice_full_favor) | Block | Event Node: Story branch or dialog option representing the \'Sacrifice Full Favor\' action. | 1 |
| [`sacrifice_normal`](./Events_and_Encounters.md#context-sacrifice_normal) | Block | Event Node: Story branch or dialog option representing the 'Sacrifice Normal' action. | 1 |
| [`sacrifice_partial_favor`](./Events_and_Encounters.md#context-sacrifice_partial_favor) | Block | Event Node: Story branch or dialog option representing the \'Sacrifice Partial Favor\' action. | 1 |
| [`sacrifice_quest`](./Events_and_Encounters.md#context-sacrifice_quest) | Block | Event Node: Story branch or dialog option representing the 'Sacrifice Quest' action. | 1 |
| [`scream`](./Events_and_Encounters.md#context-scream) | Block | Event Node: Story branch or dialog option representing the \'Scream\' action. | 1 |
| [`shake`](./Events_and_Encounters.md#context-shake) | Block | Event Node: Story branch or dialog option representing the \'Shake\' action. | 1 |
| [`slip_through`](./Events_and_Encounters.md#context-slip_through) | Block | Event Node: Story branch or dialog option representing the \'Slip Through\' action. | 1 |
| [`sneak_by`](./Events_and_Encounters.md#context-sneak_by) | Block | Event Node: Story branch or dialog option representing the \'Sneak By\' action. | 1 |
| [`sneak_past_alt`](./Events_and_Encounters.md#context-sneak_past_alt) | Block | Event Node: Story branch or dialog option representing the \'Sneak Past Alt\' action. | 1 |
| [`soul`](./Events_and_Encounters.md#context-soul) | Block | Event Node: Story branch or dialog option representing the 'Soul' action. | 1 |
| [`speed`](./Events_and_Encounters.md#context-speed) | Block | Event Node: Story branch or dialog option representing the \'Speed\' action. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`surprise`](./Events_and_Encounters.md#context-surprise) | Block | Event Node: Story branch or dialog option representing the \'Surprise\' action. | 1 |
| [`sweet_talk`](./Events_and_Encounters.md#context-sweet_talk) | Block | Event Node: Story branch or dialog option representing the \'Sweet Talk\' action. | 1 |
| [`swim`](./Events_and_Encounters.md#context-swim) | Block | Event Node: Story branch or dialog option representing the \'Swim\' action. | 1 |
| [`tail`](./Events_and_Encounters.md#context-tail) | Block | Event Node: Story branch or dialog option representing the \'Tail\' action. | 1 |
| [`take_blood`](./Events_and_Encounters.md#context-take_blood) | Block | Event Node: Story branch or dialog option representing the 'Take Blood' action. | 1 |
| [`talk_to`](./Events_and_Encounters.md#context-talk_to) | Block | Event Node: Story branch or dialog option representing the \'Talk To\' action. | 1 |
| [`talk`](./Events_and_Encounters.md#context-talk) | Block | Event Node: Story branch or dialog option representing the 'Talk' action. | 1 |
| [`tappytoes`](./Events_and_Encounters.md#context-tappytoes) | Block | Event Node: Story branch or dialog option representing the \'Tappytoes\' action. | 1 |
| [`teleport`](./Events_and_Encounters.md#context-teleport) | Block | Event Node: Story branch or dialog option representing the \'Teleport\' action. | 1 |
| [`thorns`](./Events_and_Encounters.md#context-thorns) | Block | Event Node: Story branch or dialog option representing the \'Thorns\' action. | 1 |
| [`throw`](./Events_and_Encounters.md#context-throw) | Block | Event Node: Story branch or dialog option representing the \'Throw\' action. | 1 |
| [`timemachine`](./Events_and_Encounters.md#context-timemachine) | Block | Event Node: Story branch or dialog option representing the \'Timemachine\' action. | 1 |
| [`traverse`](./Events_and_Encounters.md#context-traverse) | Block | Event Node: Story branch or dialog option representing the \'Traverse\' action. | 1 |
| [`upgrade_yourself`](./Events_and_Encounters.md#context-upgrade_yourself) | Block | Event Reward: Upgrades an existing ability or item. | 1 |
| [`use_item`](./Events_and_Encounters.md#context-use_item) | Block | Event Requirement: Requires the player to consume a specific item to proceed. | 1 |
| [`use_toilet_con`](./Events_and_Encounters.md#context-use_toilet_con) | Block | Event Node: Story branch or dialog option representing the \'Use Toilet Con\' action. | 1 |
| [`use_toilet_str`](./Events_and_Encounters.md#context-use_toilet_str) | Block | Event Node: Story branch or dialog option representing the \'Use Toilet Str\' action. | 1 |
| [`use_weapon`](./Events_and_Encounters.md#context-use_weapon) | Block | Event Requirement: Uses the properties of the equipped weapon to resolve an outcome. | 1 |
| [`w1`](./Events_and_Encounters.md#context-w1) | Block | Event Node: Story branch or dialog option representing the \'W1\' action. | 1 |
| [`w2`](./Events_and_Encounters.md#context-w2) | Block | Event Node: Story branch or dialog option representing the \'W2\' action. | 1 |
| [`w3`](./Events_and_Encounters.md#context-w3) | Block | Event Node: Story branch or dialog option representing the \'W3\' action. | 1 |
| [`w4`](./Events_and_Encounters.md#context-w4) | Block | Event Node: Story branch or dialog option representing the \'W4\' action. | 1 |
| [`w5`](./Events_and_Encounters.md#context-w5) | Block | Event Node: Story branch or dialog option representing the \'W5\' action. | 1 |
| [`w6`](./Events_and_Encounters.md#context-w6) | Block | Event Node: Story branch or dialog option representing the \'W6\' action. | 1 |
| [`wealth`](./Events_and_Encounters.md#context-wealth) | Block | Event Node: Story branch or dialog option representing the 'Wealth' action. | 1 |
| [`wheezies`](./Events_and_Encounters.md#context-wheezies) | Block | Event Node: Story branch or dialog option representing the \'Wheezies\' action. | 1 |
| [`wish_genes`](./Events_and_Encounters.md#context-wish_genes) | Block | Event Node: Story branch or dialog option representing the \'Wish Genes\' action. | 1 |
| [`wish_items`](./Events_and_Encounters.md#context-wish_items) | Block | Event Node: Story branch or dialog option representing the \'Wish Items\' action. | 1 |
| [`wish_levelups`](./Events_and_Encounters.md#context-wish_levelups) | Block | Event Node: Story branch or dialog option representing the \'Wish Levelups\' action. | 1 |
| [`wish_strength`](./Events_and_Encounters.md#context-wish_strength) | Block | Event Node: Story branch or dialog option representing the \'Wish Strength\' action. | 1 |
| [`withstand`](./Events_and_Encounters.md#context-withstand) | Block | Event Node: Story branch or dialog option representing the \'Withstand\' action. | 1 |
| [`yank_it_out`](./Events_and_Encounters.md#context-yank_it_out) | Block | Event Node: Story branch or dialog option representing the \'Yank It Out\' action. | 1 |
| [`yellow_needle`](./Events_and_Encounters.md#context-yellow_needle) | Block | Event Node: Story branch or dialog option representing the \'Yellow Needle\' action. | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `get_item_from_pool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 209

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 40 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 32 |
| [`restrict`](./Arrays.md#array-restrict) | Array |  | 30 |

</details>

---

### Context: `requirements`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 203

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`activate_p`](./Events_and_Encounters.md#context-activate_p), [`activate_z`](./Events_and_Encounters.md#context-activate_z), [`attach_amplifier`](./Events_and_Encounters.md#context-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#context-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#context-attach_leech), [`bash`](./Events_and_Encounters.md#context-bash), [`bash_past_alt`](./Events_and_Encounters.md#context-bash_past_alt), [`blue_needle`](./Events_and_Encounters.md#context-blue_needle), [`charm`](./Events_and_Encounters.md#context-charm), [`charm_past_alt`](./Events_and_Encounters.md#context-charm_past_alt), [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward), [`dig`](./Events_and_Encounters.md#context-dig), [`donate_10`](./Events_and_Encounters.md#context-donate_10), [`donate_15`](./Events_and_Encounters.md#context-donate_15), [`donate_20`](./Events_and_Encounters.md#context-donate_20), [`donate_5`](./Events_and_Encounters.md#context-donate_5), [`fiddle`](./Events_and_Encounters.md#context-fiddle), [`fight`](./Events_and_Encounters.md#context-fight), [`fill_jar`](./Events_and_Encounters.md#context-fill_jar), and 31 more...

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`has_token`](./Enums.md#enum-has_token) | Enum |  | 80 |
| [`counter_range`](./Arrays.md#array-counter_range) | Array |  | 37 |
| [`not_has_token`](./Enums.md#enum-not_has_token) | Enum |  | 30 |
| [`counter_minimum`](./Arrays.md#array-counter_minimum) | Array |  | 25 |
| [`cat_has_item_equipped`](./Enums.md#enum-cat_has_item_equipped) | Enum |  | 22 |
| [`counter_maximum`](./Arrays.md#array-counter_maximum) | Array |  | 18 |
| [`is_not_chapter`](./Arrays.md#array-is_not_chapter) | Array |  | 16 |
| [`is_chapter`](./Arrays.md#array-is_chapter) | Array |  | 8 |
| [`not_cat_has_item_equipped`](./Enums.md#enum-not_cat_has_item_equipped) | Enum |  | 2 |
| `minimum_party_size` | Number |  | 2 |
| `not_on_quest` | Number |  | 2 |
| [`cat_has_item_slot_equipped`](./Enums.md#enum-cat_has_item_slot_equipped) | Enum |  | 1 |
| `cat_has_injury_count_min` | Number |  | 1 |
| `cat_has_parasite` | Boolean |  | 1 |

</details>

---

### Context: `self_status_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 141

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`buy1`](./Events_and_Encounters.md#context-buy1), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 103 |

</details>

---

### Context: `permanent_stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 133

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 35 |
| `random` | Number |  | 25 |
| `int` | Number |  | 21 |
| `lck` | Number |  | 18 |
| `spd` | Number |  | 18 |
| `str` | Number |  | 16 |
| `cha` | Mixed |  | 14 |
| `dex` | Number |  | 9 |

</details>

---

### Context: `conditional_reward`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 124

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`setup`](./Events_and_Encounters.md#context-setup)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 175 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 124 |
| [`else`](./Events_and_Encounters.md#context-else) | Block | Event Node: Story branch or dialog option representing the \'Else\' action. | 37 |

</details>

---

### Context: `random_mutation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 66

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`else`](./Events_and_Encounters.md#context-else), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | Quantity. | 15 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 12 |
| `asymmetric` | Boolean |  | 8 |

</details>

---

### Context: `ignore`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 57

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 59 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 57 |
| `label` | Mixed |  | 57 |
| `stat` | Mixed |  | 56 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 55 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 3 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 2 |

</details>

---

### Context: `examine`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 57 |
| [`stat`](./Math_Equations.md) | Equation |  | 43 |
| `label` | Mixed |  | 43 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 41 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `spawn_unit_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 40

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare), [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array |  | 40 |
| [`count`](./Arrays.md#array-count) | Array | Quantity. | 34 |
| [`spawn_side`](./Enums.md#enum-spawn_side) | Enum |  | 31 |
| [`side`](./Enums.md#enum-side) | Enum |  | 3 |

</details>

---

### Context: `else`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 37

> **Referenced by:** [`conditional_reward`](./Events_and_Encounters.md#context-conditional_reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 32 |
| `damage` | Number | Event Node: Story branch or dialog option representing the 'Damage' action. | 1 |

</details>

---

### Context: `leave`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`main`](./Events_and_Encounters.md#context-main), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 32 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 31 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 30 |
| [`label`](./Strings.md#string-label) | String |  | 30 |
| `stat` | Mixed |  | 30 |

</details>

---

### Context: `loot`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 25

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 63 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 26 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 25 |
| [`stat`](./Math_Equations.md) | Equation |  | 25 |
| `label` | Mixed |  | 25 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 |

</details>

---

### Context: `mutation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare), [`spawn_reflection_next_fight`](./Events_and_Encounters.md#context-spawn_reflection_next_fight)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `eyes` | Number |  | 12 |
| `mouth` | Number |  | 11 |
| `ears` | Number |  | 10 |
| `eyebrows` | Number |  | 8 |
| `head` | Number | Event Node: Story branch or dialog option representing the 'Head' action. | 7 |
| `legs` | Number |  | 7 |
| `arms` | Number |  | 6 |
| `body` | Number | Event Node: Story branch or dialog option representing the 'Body' action. | 6 |
| `tail` | Number | Event Node: Story branch or dialog option representing the 'Tail' action. | 6 |
| `eye1` | Number |  | 3 |
| `arm1` | Number |  | 2 |
| `ear1` | Number |  | 2 |
| `eyebrow1` | Number |  | 2 |
| `leg1` | Number |  | 2 |
| `eye2` | Number |  | 1 |

</details>

---

### Context: `eat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 66 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 23 |
| [`stat`](./Math_Equations.md) | Equation |  | 23 |
| `label` | Mixed |  | 23 |

</details>

---

### Context: `party_status_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 22 |

</details>

---

### Context: `setup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `cutscene`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 22 |
| `skip_result_screen` | Boolean |  | 21 |

</details>

---

### Context: `random_mutation_from_set`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mouth` | Number |  | 9 |
| `count` | Number | Quantity. | 8 |
| `tail` | Number | Event Node: Story branch or dialog option representing the 'Tail' action. | 7 |
| `ears` | Number |  | 5 |
| `eyes` | Number |  | 5 |
| `legs` | Number |  | 5 |
| `body` | Number | Event Node: Story branch or dialog option representing the 'Body' action. | 4 |
| `eyebrows` | Number |  | 3 |
| `head` | Number | Event Node: Story branch or dialog option representing the 'Head' action. | 3 |
| `arm1` | Number |  | 2 |
| `arm2` | Number |  | 2 |
| `leg1` | Number |  | 1 |
| `leg2` | Number |  | 1 |
| `texture` | Number |  | 1 |

</details>

---

### Context: `smash`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 18 |
| [`label`](./Strings.md#string-label) | String |  | 15 |
| `stat` | Mixed |  | 15 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 14 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |

</details>

---

### Context: `destroy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 22 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 14 |
| [`label`](./Strings.md#string-label) | String |  | 14 |
| [`stat`](./Math_Equations.md) | Equation |  | 14 |

</details>

---

### Context: `bash`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 16 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 12 |
| [`label`](./Strings.md#string-label) | String |  | 12 |
| [`stat`](./Math_Equations.md) | Equation |  | 12 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `open`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#context-root), [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`label`](./Strings.md#string-label) | String |  | 8 |
| [`stat`](./Math_Equations.md) | Equation |  | 8 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |

</details>

---

### Context: `sneak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 32 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 11 |
| [`stat`](./Math_Equations.md) | Equation |  | 11 |
| `label` | Mixed |  | 11 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `global_effect_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 16 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| [`KillEnemyOfTypeAtBattleStart`](./Events_and_Encounters.md#context-killenemyoftypeatbattlestart) | Block | Encounter Modifier: Instantly kills one enemy of the specified type at the start of battle. | 2 |

</details>

---

### Context: `take`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 17 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 8 |
| [`label`](./Strings.md#string-label) | String |  | 8 |
| [`stat`](./Math_Equations.md) | Equation |  | 8 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `a`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 7 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `attack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 12 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |

</details>

---

### Context: `b`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 7 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `c`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`label`](./Strings.md#string-label) | String |  | 7 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 7 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 7 |

</details>

---

### Context: `charm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 18 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| `label` | Mixed |  | 7 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 13 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| [`stat`](./Math_Equations.md) | Equation |  | 7 |
| `label` | Mixed |  | 7 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `leave_party_temporarily`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `fights_skipped` | Number |  | 7 |
| [`return_as`](./Enums.md#enum-return_as) | Enum |  | 3 |
| [`return_during`](./Enums.md#enum-return_during) | Enum |  | 3 |

</details>

---

### Context: `touch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 7 |
| `label` | Mixed |  | 7 |
| `stat` | Mixed |  | 7 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 6 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `activate_p`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Enums.md#enum-label) | Enum |  | 6 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 6 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 6 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `activate_z`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Enums.md#enum-label) | Enum |  | 6 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 6 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 6 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `d`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Strings.md#string-label) | String |  | 6 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 6 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `enter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 10 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| `label` | Mixed |  | 6 |
| `stat` | Mixed |  | 5 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 1 |

</details>

---

### Context: `inspect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| [`label`](./Strings.md#string-label) | String |  | 6 |
| [`stat`](./Math_Equations.md) | Equation |  | 6 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 6 |

</details>

---

### Context: `lick`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 11 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 6 |
| `label` | Mixed |  | 6 |
| `stat` | Mixed |  | 6 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `next_event_from_set`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`good`](./Events_and_Encounters.md#context-good), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`event`](./Enums.md#enum-event) | Enum |  | 5 |
| `same_cat` | Boolean |  | 5 |
| `count` | Number | Quantity. | 4 |

</details>

---

### Context: `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 5 |

</details>

---

### Context: `drink`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 13 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |
| `label` | Mixed |  | 5 |

</details>

---

### Context: `kiss`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 13 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 5 |
| [`label`](./Strings.md#string-label) | String |  | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |

</details>

---

### Context: `run`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 9 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 5 |
| [`label`](./Strings.md#string-label) | String |  | 5 |
| [`stat`](./Math_Equations.md) | Equation |  | 5 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `bite`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`label`](./Enums.md#enum-label) | Enum |  | 4 |
| [`stat`](./Math_Equations.md) | Equation |  | 4 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `damage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`label`](./Strings.md#string-label) | String |  | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 3 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |

</details>

---

### Context: `go_around`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`label`](./Strings.md#string-label) | String |  | 4 |
| `stat` | Mixed |  | 3 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `home`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 4 |
| [`label`](./Enums.md#enum-label) | Enum |  | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 4 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `outcome`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weather_roll`](./Arrays.md#array-weather_roll) | Array |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `party_permanent_stats_exclude_self`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`common`](./Events_and_Encounters.md#context-common), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cha` | Number |  | 4 |
| `con` | Number |  | 4 |
| `dex` | Number |  | 4 |
| `int` | Number |  | 4 |
| `lck` | Number |  | 4 |
| `spd` | Number |  | 4 |
| `str` | Number |  | 4 |

</details>

---

### Context: `past`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 4 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 4 |
| [`label`](./Enums.md#enum-label) | Enum |  | 4 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 4 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `skip`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | String |  | 4 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 4 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |

</details>

---

### Context: `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | All valid keys from the specified engine key are applicable to this context/block. | 7 |
| `count` | Number | Quantity. | 3 |

</details>

---

### Context: `investigate`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 3 |
| [`label`](./Strings.md#string-label) | String |  | 3 |
| [`stat`](./Math_Equations.md) | Equation |  | 3 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `repell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 8 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 3 |
| [`label`](./Strings.md#string-label) | String |  | 3 |
| [`stat`](./Math_Equations.md) | Equation |  | 3 |

</details>

---

### Context: `spawn_reflection_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `KillEnemyOfTypeAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`enemy_type`](./Enums.md#enum-enemy_type) | Enum |  | 2 |
| [`fallback_spawn`](./Arrays.md#array-fallback_spawn) | Array |  | 1 |

</details>

---

### Context: `attach_antenna`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Enums.md#enum-label) | Enum |  | 2 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `boogers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `copy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |

</details>

---

### Context: `find_another_way`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `move_closer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |

</details>

---

### Context: `party_permanent_stats`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`main`](./Events_and_Encounters.md#context-main), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 2 |

</details>

---

### Context: `party_random_mutation_from_set`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bad`](./Events_and_Encounters.md#context-bad), [`rare`](./Events_and_Encounters.md#context-rare)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | Quantity. | 2 |
| `ears` | Number |  | 2 |
| `eyebrows` | Number |  | 2 |
| `eyes` | Number |  | 2 |
| `mouth` | Number |  | 2 |

</details>

---

### Context: `play`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |

</details>

---

### Context: `poop`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |

</details>

---

### Context: `print`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |

</details>

---

### Context: `protection`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 2 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |

</details>

---

### Context: `repair`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| `label` | Mixed |  | 2 |
| `stat` | Mixed |  | 2 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `sacrifice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `scale`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |

</details>

---

### Context: `turnon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 2 |
| [`label`](./Strings.md#string-label) | String |  | 2 |
| [`stat`](./Math_Equations.md) | Equation |  | 2 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `altar_sacrifice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `arm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `attach_amplifier`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `attach_leech`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `bash_past_alt`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `bite_it_off`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `blue`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `fixed_chance` | Number |  | 1 |

</details>

---

### Context: `blue_needle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `body`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `book`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `brace`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `break_ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `break_lock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `bribe`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `button`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`copy_results`](./Enums.md#enum-copy_results) | Enum |  | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `fixed_chance` | Number |  | 1 |

</details>

---

### Context: `buy1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `catch`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `challenge_to_game`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `chaos_ending`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `chapter_cutscene`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `charm_past_alt`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `climb`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `comfort`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `communicate`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `concheck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `counter`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `crack_open`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `cross`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `cut_wires`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `damage_1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `damage_full`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `damage_half`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `desert_cutscene`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `dexcheck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `dig`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `disarm`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `dive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `donate`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `donate_10`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `donate_15`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `donate_20`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `donate_5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `double`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `eat_meat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `enter_crater`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `face`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `fiddle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `fill_jar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `find`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `fire`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `flush_yourself`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `follow`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `free`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `future`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `gain_clone_familiar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`good`](./Events_and_Encounters.md#context-good)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |

</details>

---

### Context: `gain_familiar`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 1 |
| `initial_health` | Number |  | 1 |

</details>

---

### Context: `give_parasite`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |

</details>

---

### Context: `hack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `head`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `holy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `hp`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `ice`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `infinite`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`hint_chapter_exit`](./Enums.md#enum-hint_chapter_exit) | Enum |  | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `intcheck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `intimidation`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `itchies`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `join`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `jump`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `jump_over`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `keep_going`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `kiss_meat`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `knife`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `leave_it_in`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `leg`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `lever`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `fixed_chance` | Number |  | 1 |

</details>

---

### Context: `lick_alt`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `lightning`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `listen`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `looks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `loot_heart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `makeup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `mind`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `neck`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `nothanks`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `outsmart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `patch_up`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `pick_lock`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `pilfer`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `pirouette`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `place_gristle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `power`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `pull`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `pull_it_out`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `pull_lever`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `purify`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `push_buttons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `push_through`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `put_in_coins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation_fail`](./Enums.md#enum-animation_fail) | Enum |  | 1 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `stat_max` | Number |  | 1 |
| `stat_min` | Number |  | 1 |

</details>

---

### Context: `put_out_of_misery`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `random_chance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`reward`](./Events_and_Encounters.md#context-reward)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| `chance` | Number | Probability weight for this outcome. | 1 |

</details>

---

### Context: `reach_inside`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `read`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `receive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `red`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| `fixed_chance` | Number |  | 1 |

</details>

---

### Context: `red_needle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `reflect`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `remove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `remove_the_nail`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `repair_quest`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `rest`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `revive`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `rub`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `run_again`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `run_away`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `sacrifice_full_favor`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `sacrifice_normal`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `sacrifice_partial_favor`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `sacrifice_quest`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `scream`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `shake`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `slip_through`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `sneak_by`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `sneak_past_alt`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `soul`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `speed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `surprise`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `sweet_talk`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `swim`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `tail`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `take_blood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `talk`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `talk_to`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `tappytoes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `teleport`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `thorns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `throw`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `timemachine`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `traverse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |

</details>

---

### Context: `upgrade_yourself`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `use_item`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `use_toilet_con`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `use_toilet_str`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `use_weapon`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 0 |

</details>

---

### Context: `w1`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `w2`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `w3`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `w4`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `w5`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `w6`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `wealth`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Enums.md#enum-label) | Enum |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wheezies`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 1 |

</details>

---

### Context: `wish_genes`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wish_items`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wish_levelups`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `wish_strength`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Enums.md#enum-stat) | Enum |  | 1 |

</details>

---

### Context: `withstand`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 3 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `yank_it_out`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

### Context: `yellow_needle`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`options`](./Events_and_Encounters.md#context-options)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 2 |
| [`good`](./Events_and_Encounters.md#context-good) | Block | Event Node: Story branch or dialog option representing the \'Good\' action. | 1 |
| [`label`](./Strings.md#string-label) | String |  | 1 |
| [`requirements`](./Events_and_Encounters.md#context-requirements) | Block | Event Block: Pre-requisites (e.g., minimum gold, specific item, or minimum stat value) needed to select an option. | 1 |
| [`stat`](./Math_Equations.md) | Equation |  | 1 |

</details>

---

