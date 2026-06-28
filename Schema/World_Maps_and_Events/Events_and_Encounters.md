---
title: "Events & Encounters Schema"
description: "Dialogue encounters and choice nodes."
---

# Events & Encounters Schema

## Overview
> [!NOTE]
> This schema handles narrative choice nodes where players are presented with text, make decisions, and receive outcomes like items or damage.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
TrashBin { //originally in treasure_box.gon
    intro {
        title "EVENT_TRASHBIN_NAME"
        cat_choice random
        subject_clip EventSubject
        subject_frame trashcan
        event_clip NonWheelEvent
    }

    main {
        prompt "EVENT_TRASHBIN_QUES"

        options {
            examine {
                label "EVENT_EXAMINE_ANSW"
                stat int

                good {
                    prompt "EVENT_TRASHBIN_REW1"
                    set_frame 2
                    reward {
                        common {
                            random_pool [
                                { 
                                    party_heal 5 
                                    gain_food [2 4]
                                }
                                { 
                                    prompt "EVENT_TRASHBIN_REW2"
                                    spawn_unit_next_fight {
                                        object RandomNonCoinPickup
                                        count 8
                                        spawn_side anywhere
                                    } 
                                    spawn_unit_next_fight {
                                        object [Junk Junk TrashBag]
                                        count [3 6]
                                        spawn_side anywhere
                                    } 
                                }
                                { 
                                    full_heal 1
                                }
                                { 
                                    gain_coins [5 15]
                                }
                            ]
                        }
                        rare {
                            random_pool [
                                {
                                    party_heal 100%
                                    gain_food [10 25]
                                }
                                { 
                                    party_heal 3
                                    party_permanent_stats {
                                        con 1
                                    }
                                }
                                { 
                                    get_item_from_pool food
                                    get_item_from_pool food
                                    get_item_from_pool food
                                    get_item_from_pool food
                                }
                            ]
                        }
                    }
                }
                bad {
                    prompt "EVENT_TRASHBIN_REW3"
                    set_frame 2
                    reward {
                        common {
                            self_status_next_fight {
                                Poison 2
                            }
                        }
                        rare {
                            self_status_next_fight {
                                Poison 2
                            }
                            get_parasite_from_pool sludge_armor
                        }
                    }
                }
            }

            pick {
                label "EVENT_PICK_ANSW"
                stat dex
                animation choice_dex_alt

                copy_results examine
            }

            open {
                label "EVENT_OPEN_ANSW"
                stat lck

                copy_results examine
            }
        }
    }
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Events_and_Encounters.md`](../../Directory/World_and_Events/Events_and_Encounters.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Events & Encounters

> **Associated Files:** `data/events/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 214

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 883 | `common`<br>`rare`<br>`cha` |
| [`intro`](./NPC_Scripts.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 220 | `{ . . . }` |
| [`main`](../Reference_and_Meta/Miscellaneous.md#object-main) | Object  | An object containing the primary prompt and options for an event. | 215 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 271 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 337 | `+1`<br>`-1`<br>`-2` |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 361 | `-1`<br>`-2`<br>`-3` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 332 | `-1`<br>`-10`<br>`-2` |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 355 | `-1`<br>`-10`<br>`-2` |
| [`lck`](../Reference_and_Meta/Enums.md#enum-lck) | Enum / Integer | The Luck stat value or modifier. | 283 | `-1`<br>`-2`<br>`-3` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer | The Strength stat value or modifier. | 335 | `-1`<br>`-2`<br>`-3` |
| [`rare`](../Reference_and_Meta/Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 1061 | `1`<br>`10`<br>`15` |
| [`dex`](../Reference_and_Meta/Enums.md#enum-dex) | Enum / Integer | The Dexterity stat value or modifier. | 250 | `-1`<br>`-2`<br>`-3` |
| [`battle`](../Assets_and_Localization/Strings.md#string-battle) | String | Defines a battle encounter by preset, level file path, or reverb settings. | 36 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| [`normal`](../Reference_and_Meta/Arrays.md#array-normal) | Array | An array or object defining the reward table for normal encounters, including coin ranges, food ranges, and loot chances. | 41 | `[` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`common`](../Reference_and_Meta/Enums.md#enum-common) | Enum  | Defines the common reward block for a boss encounter. | 1226 | `100`<br>`14`<br>`5` |
| `complete_item_quest` | String | Marks the specified item quest as completed. | 22 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1009 | `1`<br>`10`<br>`15` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`reward`](../Reference_and_Meta/Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 764 | `{ . . . }` |
| [`pick`](../Reference_and_Meta/Miscellaneous.md#object-pick) | Object  | An object defining the player action to pick or collect an object, including its stat check and outcomes. | 3 | `{ . . . }` |
| `get_item_from_pool` | String | Grants an item from the specified pool or a specific item name. | 349 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| `weight` | `Number` | A multiplier or priority value for random selection or effect magnitude. | 94 | `.25`<br>`.5`<br>`1` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| [`open`](../Reference_and_Meta/Miscellaneous.md#object-open) | Object  | An object defining the player action to open a container, including its stat check and outcomes. | 72 | `{ . . . }` |
| [`smash`](../Reference_and_Meta/Miscellaneous.md#object-smash) | Object  | An object defining the player action to smash an object, including its stat check and outcomes. | 21 | `{ . . . }` |
| [`conditional_reward`](../Reference_and_Meta/Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 126 | `{ . . . }` |
| [`cutscene`](../Assets_and_Localization/Strings.md#string-cutscene) | String | Specifies the name of a cutscene to play. | 46 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| [`destroy`](../Reference_and_Meta/Miscellaneous.md#object-destroy) | Object  | An object defining the player action to destroy an object, including its stat check and outcomes. | 14 | `{ . . . }` |
| [`mutation`](../Reference_and_Meta/Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 31 | `{ . . . }` |

</details>


---


### Object: `reward`


**Definition:** An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items.  
**Total Count:** 764

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`bad`](./Events_and_Encounters.md#object-bad), [`conditional_reward`](./Events_and_Encounters.md#object-conditional_reward), [`good`](./Events_and_Encounters.md#object-good)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1364 | `common`<br>`rare`<br>`cha` |
| [`common`](../Reference_and_Meta/Enums.md#enum-common) | Enum  | Defines the common reward block for a boss encounter. | 1226 | `100`<br>`14`<br>`5` |
| [`rare`](../Reference_and_Meta/Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 1061 | `1`<br>`10`<br>`15` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1009 | `1`<br>`10`<br>`15` |
| `set_subject` | `String` | Specifies which subject or frame to use for the event's visual. | 11 | `dimensionx_head2`<br>`endorb2`<br>`monkey_paw_1finger` |
| `get_item_from_pool` | String | Grants an item from the specified pool or a specific item name. | 349 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 59 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 90 | `[` |
| `clear_adventure_token` | String | Specifies an adventure token to clear (disable or mark as false) when this event triggers. | 48 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasTakenNeedle`<br>`AdventureToken_RedNeedle` |
| `next_event_bonus` | Number | A modifier to the next event's outcome roll or selection chance. | 32 | `-1`<br>`-2`<br>`1` |
| `trigger_adventure_unlock` | `String` | Triggers the specified adventure or map unlock quest. | 13 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| [`play_animation`](../Reference_and_Meta/Arrays.md#array-play_animation) | Array | Specifies an animation to play, optionally as an array with a probability weight. | 179 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| `cutscene_on_exit` | `String` | Determines which cutscene to play when the player leaves the current location. | 5 | `infinite_intro`<br>`king_intro` |
| `gain_disorder_from_pool` | String | Specifies a pool of disorders from which one is randomly gained. | 88 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| `injury` | String | Specifies the type of injury applied, such as bleeding or stat reduction. | 109 | `bleeding`<br>`burned`<br>`cha` |
| [`gain_coins`](../Reference_and_Meta/Arrays.md#array-gain_coins) | Array | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 57 | `1`<br>`10`<br>`15` |
| `ambush_next_basic_fights` | Number | The number of basic fights to trigger as ambushes. | 18 | `1` |
| `event_now` | String | Triggers the specified event immediately. | 25 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| `get_parasite_from_pool` | String | Specifies the pool name or explicit list of parasites to obtain from. | 43 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| `level_up` | String | Specifies which units to level up, such as 'all' or 'self'. | 13 | `all`<br>`self` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 38 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| [`party_damage`](../Reference_and_Meta/Arrays.md#array-party_damage) | Array / Integer | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 36 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `common`


**Definition:** Defines the common reward block for a boss encounter.  
**Total Count:** 1226

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`reward`](./Events_and_Encounters.md#object-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 658 | `common`<br>`rare`<br>`cha` |
| `prompt` | `String` | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1009 | `1`<br>`10`<br>`15` |
| [`self_status_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 199 | `{ . . . }` |
| `get_item_from_pool` | `String` | Grants an item from the specified pool or a specific item name. | 349 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`permanent_stats`](../Reference_and_Meta/Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 148 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 90 | `[` |
| `gain_coins` | `Array` | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 57 | `1`<br>`10`<br>`15` |
| `injury` | `String` | Specifies the type of injury applied, such as bleeding or stat reduction. | 109 | `bleeding`<br>`burned`<br>`cha` |
| `self_damage` | `Number` | Defines damage or effects applied to the caster when using the ability. | 271 | `1`<br>`10`<br>`100%` |
| `random_mutation` | `Number` | The number of random mutations applied to the unit. | 86 | `1`<br>`10`<br>`2` |
| `gain_disorder_from_pool` | `String` | Specifies a pool of disorders from which one is randomly gained. | 88 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| `play_animation` | `String` | Specifies an animation to play, optionally as an array with a probability weight. | 179 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| `event_now_same_cat` | `String` | Specifies a world event that will now occur for the same cat category as the current event. | 100 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| `gain_food` | `Number` | An array specifying the minimum and maximum amount of food gained, or a single integer. | 36 | `-5`<br>`20`<br>`30` |
| [`spawn_unit_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 42 | `{ . . . }` |
| `gain_familiar` | `String` | Specifies which familiar type (by its class name) the unit gains. | 101 | `CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| `party_heal` | `Number` | The amount of health healed for the entire party. | 34 | `1`<br>`10`<br>`100%` |
| `party_damage` | `Number` | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 36 | `1`<br>`10`<br>`2` |
| `get_item` | `String` | Specifies an item to add to the player's inventory when this event triggers. | 125 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| `heal` | `Equation` | An equation string that determines the amount of health restored by this damage instance. | 168 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| `gain_disorder` | `String` | Specifies a disorder to add to the current cat when this event triggers. | 98 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| `override_end_option_prompt` | `String` | Specifies a custom prompt string to display for the end option of this event choice. | 22 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| [`party_status_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 26 | `{ . . . }` |
| `get_parasite_from_pool` | `String` | Specifies the pool name or explicit list of parasites to obtain from. | 43 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| `ally_ambush_next_fights` | `Number` | The number of upcoming fights that will start with an ally ambush. | 18 | `1`<br>`2` |
| `full_heal` | `Number` | If set to 1, fully restores the unit's health. | 20 | `1` |
| `ambush_next_basic_fights` | `Number` | The number of basic fights to trigger as ambushes. | 18 | `1` |
| [`conditional_reward`](../Reference_and_Meta/Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 126 | `{ . . . }` |
| [`random_mutation_from_set`](../Reference_and_Meta/Miscellaneous.md#object-random_mutation_from_set) | Object  | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 22 | `{ . . . }` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 59 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `get_parasite` | `String` | Specifies a parasite item to attach to a unit when this event triggers. | 60 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `next_event_bonus` | `Number` | A modifier to the next event's outcome roll or selection chance. | 32 | `-1`<br>`-2`<br>`1` |
| `clear_adventure_token` | `String` | Specifies an adventure token to clear (disable or mark as false) when this event triggers. | 48 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasTakenNeedle`<br>`AdventureToken_RedNeedle` |
| [`global_effect_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 11 | `{ . . . }` |
| `increment_legacy_counter` | `String` | Specifies a legacy counter to increment by one when this event triggers. | 69 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| `kill` | `String` | Kills the specified target type (e.g., 'cat'). | 16 | `cat` |
| `lose_item` | `String` | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 18 | `equipped`<br>`inventory`<br>`parasite` |
| `shop_now` | `String` | Triggers the specified shop to appear immediately. | 15 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| `add_weather` | `String` | Specifies a weather effect type to apply to the current map. | 67 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| `event_now` | `String` | Triggers the specified event immediately. | 25 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| `lose_specific_item` | `String` | Removes the specified item from the player's inventory. | 13 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| [`next_event_from_set`](../Reference_and_Meta/Miscellaneous.md#object-next_event_from_set) | Object  | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 10 | `{ . . . }` |
| `party_heal_disorder` | `Number` | The number of disorders to heal from all party members. | 5 | `2` |
| [`party_permanent_stats_exclude_self`](../Reference_and_Meta/Miscellaneous.md#object-party_permanent_stats_exclude_self) | Object  | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 4 | `{ . . . }` |
| `spin` | `String` | Specifies an action to re-roll or spin again, such as for a random reward wheel. | 8 | `again` |
| `clear_result_animation` | `Number` | The number of result animations to clear or skip. | 2 | `1` |
| `decrement_legacy_counter` | `String` | Specifies which legacy counter or token to decrement by one. | 7 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyToken_StartDigging` |
| `get_and_equip_item` | `String` | Specifies the item to obtain and immediately equip. | 3 | `Catnip`<br>`FlyLarva` |
| `heal_disorder` | `Number` | Specifies which disorder type to heal, or the number of disorders to heal. | 11 | `1`<br>`2`<br>`Anxiety` |
| `heal_injury` | `Number` | The number of injury points to heal on the target unit. | 6 | `1`<br>`5` |
| `learn_ability_from_pool` | `String` | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 6 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| [`mutation`](../Reference_and_Meta/Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 31 | `{ . . . }` |
| `self_heal` | `Number` | The amount of health the unit heals itself. | 1 | `10` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 38 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `upgrade_ability` | `String` | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 6 | `random` |

</details>


---


### Object: `rare`


**Definition:** Defines the rare reward block for a boss encounter.  
**Total Count:** 1061

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`attack`](./Events_and_Encounters.md#object-attack), [`good`](./Events_and_Encounters.md#object-good), [`loot`](./Events_and_Encounters.md#object-loot), [`main`](./Events_and_Encounters.md#object-main), [`options`](./Events_and_Encounters.md#object-options), [`reward`](./Events_and_Encounters.md#object-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 705 | `common`<br>`rare`<br>`cha` |
| `prompt` | `String` | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1009 | `1`<br>`10`<br>`15` |
| `get_item_from_pool` | `String` | Grants an item from the specified pool or a specific item name. | 349 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`permanent_stats`](../Reference_and_Meta/Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 148 | `{ . . . }` |
| `gain_disorder` | `String` | Specifies a disorder to add to the current cat when this event triggers. | 98 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| `injury` | `String` | Specifies the type of injury applied, such as bleeding or stat reduction. | 109 | `bleeding`<br>`burned`<br>`cha` |
| `gain_disorder_from_pool` | `String` | Specifies a pool of disorders from which one is randomly gained. | 88 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`self_status_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 199 | `{ . . . }` |
| `random_mutation` | `Number` | The number of random mutations applied to the unit. | 86 | `1`<br>`10`<br>`2` |
| `get_item` | `String` | Specifies an item to add to the player's inventory when this event triggers. | 125 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| `event_now_same_cat` | `String` | Specifies a world event that will now occur for the same cat category as the current event. | 100 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 90 | `[` |
| `get_parasite` | `String` | Specifies a parasite item to attach to a unit when this event triggers. | 60 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `get_parasite_from_pool` | `String` | Specifies the pool name or explicit list of parasites to obtain from. | 43 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`spawn_unit_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 42 | `{ . . . }` |
| [`conditional_reward`](../Reference_and_Meta/Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 126 | `{ . . . }` |
| [`mutation`](../Reference_and_Meta/Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 31 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `gain_coins` | `Array` | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 57 | `1`<br>`10`<br>`15` |
| `gain_familiar` | `String` | Specifies which familiar type (by its class name) the unit gains. | 101 | `CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 59 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `next_event_bonus` | `Number` | A modifier to the next event's outcome roll or selection chance. | 32 | `-1`<br>`-2`<br>`1` |
| `self_damage` | `Number` | Defines damage or effects applied to the caster when using the ability. | 271 | `1`<br>`10`<br>`100%` |
| [`party_status_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 26 | `{ . . . }` |
| [`random_mutation_from_set`](../Reference_and_Meta/Miscellaneous.md#object-random_mutation_from_set) | Object  | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 22 | `{ . . . }` |
| `play_animation` | `Array` | Specifies an animation to play, optionally as an array with a probability weight. | 179 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| `learn_passive` | `String` | Teaches the unit the specified passive ability. | 12 | `Blessed`<br>`CobraStyle`<br>`DeathProof` |
| `party_heal` | `Number` | The amount of health healed for the entire party. | 34 | `1`<br>`10`<br>`100%` |
| `party_damage` | `Number` | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 36 | `1`<br>`10`<br>`2` |
| `battle` | `String` | Defines a battle encounter by preset, level file path, or reverb settings. | 36 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| `override_end_option_prompt` | `String` | Specifies a custom prompt string to display for the end option of this event choice. | 22 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| `party_random_mutation` | `Number` | The number of random mutations applied to the entire party. | 9 | `1` |
| `ambush_next_basic_fights` | `Number` | The number of basic fights to trigger as ambushes. | 18 | `1` |
| [`leave_party_temporarily`](../Reference_and_Meta/Miscellaneous.md#object-leave_party_temporarily) | Object  | Defines parameters for a unit leaving the party temporarily, such as skipped fights and return conditions. | 9 | `{ . . . }` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 38 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `hide_appearance_changes` | `Number` | If set to 1, visual appearance changes from status effects or mutations are not shown on the unit. | 6 | `1` |
| `shop_now` | `String` | Triggers the specified shop to appear immediately. | 15 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| `gain_food` | `Array` | An array specifying the minimum and maximum amount of food gained, or a single integer. | 36 | `-5`<br>`20`<br>`30` |
| `increment_legacy_counter` | `String` | Specifies a legacy counter to increment by one when this event triggers. | 69 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| `lose_item` | `String` | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 18 | `equipped`<br>`inventory`<br>`parasite` |
| `ally_ambush_next_fights` | `Number` | The number of upcoming fights that will start with an ally ambush. | 18 | `1`<br>`2` |
| `full_heal` | `Number` | If set to 1, fully restores the unit's health. | 20 | `1` |
| `learn_ability` | `String` | Specifies which specific ability the target unit learns. | 5 | `BarfBall`<br>`FutureSight` |
| `decrement_legacy_counter` | `String` | Specifies which legacy counter or token to decrement by one. | 7 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyToken_StartDigging` |
| `gain_cat_familiar` | `Number` | The number of cat familiars gained. | 6 | `1` |
| [`global_effect_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 11 | `{ . . . }` |
| `kill` | `String` | Kills the specified target type (e.g., 'cat'). | 16 | `cat` |
| `make_old` | `String` | Applies the 'old' status or age increase to the specified target, typically 'self'. | 5 | `self` |
| `next_event_from_set` | `String` | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 10 | `CatHole`<br>`Tragedy`<br>`WatchingHead2` |
| `spawn_reflection_next_fight` | `Number` | The number of reflections to spawn in the next battle, optionally with a mutation. | 5 | `1` |
| `add_weather` | `String` | Specifies a weather effect type to apply to the current map. | 67 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| `level_up` | `String` | Specifies which units to level up, such as 'all' or 'self'. | 13 | `all`<br>`self` |
| `event_now` | `String` | Triggers the specified event immediately. | 25 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| `lose_specific_item` | `String` | Removes the specified item from the player's inventory. | 13 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| `party_heal_disorder` | `Number` | The number of disorders to heal from all party members. | 5 | `2` |
| `party_heal_injury` | `Number` | The amount of injury to heal for the entire party. | 3 | `99` |
| [`party_permanent_stats_exclude_self`](../Reference_and_Meta/Miscellaneous.md#object-party_permanent_stats_exclude_self) | Object  | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 4 | `{ . . . }` |
| `set_age` | `Number` | The age value to set for the target unit. | 3 | `1` |
| `upgrade_ability` | `String` | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 6 | `random` |
| `upgrade_passive` | `String` | Specifies which passive ability to upgrade, or 'random' for a random choice. | 5 | `random` |
| `lose_item_from_inventory` | `String` | Specifies which item or item category is removed from the unit's inventory. | 4 | `cat` |
| `ambush` | `String` | Specifies the path to a level file for an ambush encounter. | 2 | `"events/chupacabra.lvl"`<br>`putalevelhere.lvl` |
| `clear_result_animation` | `Number` | The number of result animations to clear or skip. | 2 | `1` |
| `gain_immortal_familiar` | `String` | Specifies the immortal familiar to add to the party. | 3 | `CharmedFlea`<br>`CharmedFleaSpecial`<br>`CharmedPooter` |
| `get_and_equip_item` | `String` | Specifies the item to obtain and immediately equip. | 3 | `Catnip`<br>`FlyLarva` |
| `heal_disorder` | `Number` | Specifies which disorder type to heal, or the number of disorders to heal. | 11 | `1`<br>`2`<br>`Anxiety` |
| `learn_ability_from_pool` | `String` | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 6 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| `learn_passive_from_pool` | `String` | An array specifying a pool or list of passives from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked passive. | 5 | `AnyUnlocked`<br>`Necromancer`<br>`[MiniMe SkillShare]` |
| `lose_all_equipped_items` | `String` | Specifies the target (e.g., 'cat') from which to remove all currently equipped items. | 2 | `cat` |
| `party_injury` | `String` | Specifies the type of injury to inflict on the party (e.g., 'random'). | 3 | `random` |
| [`party_permanent_stats`](../Reference_and_Meta/Miscellaneous.md#object-party_permanent_stats) | Object  | An object defining permanent stat increases applied to the party. | 3 | `{ . . . }` |
| [`party_random_mutation_from_set`](../Reference_and_Meta/Miscellaneous.md#object-party_random_mutation_from_set) | Object  | An object specifying the count and mutation parts to randomly apply to the party. | 2 | `{ . . . }` |
| `play_result_animation` | `String` | Specifies which result animation to play (e.g., 'resultVeryGood'). | 1 | `resultVeryGood` |
| `scramble_abilities` | `String` | Specifies which abilities to randomize, such as 'all'. | 3 | `all` |
| `scramble_basic_attack` | `String` | Specifies which basic attacks to randomize or scramble. | 2 | `all` |
| `trigger_adventure_unlock` | `String` | Triggers the specified adventure or map unlock quest. | 13 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |

</details>


---


### Object: `good`


**Definition:** If true, indicates the positive outcome branch for events or spawning contexts.  
**Total Count:** 572

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`a`](./Events_and_Encounters.md#object-a), [`activate_p`](./Events_and_Encounters.md#object-activate_p), [`activate_z`](./Events_and_Encounters.md#object-activate_z), [`altar_sacrifice`](./Events_and_Encounters.md#object-altar_sacrifice), [`arm`](./Events_and_Encounters.md#object-arm), [`attach_amplifier`](./Events_and_Encounters.md#object-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#object-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#object-attach_leech), [`attack`](./Events_and_Encounters.md#object-attack), [`b`](./Events_and_Encounters.md#object-b), [`bash`](./Events_and_Encounters.md#object-bash), [`bash_past_alt`](./Events_and_Encounters.md#object-bash_past_alt), [`bite`](./Events_and_Encounters.md#object-bite), [`bite_it_off`](./Events_and_Encounters.md#object-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#object-blue_needle), [`boogers`](./Events_and_Encounters.md#object-boogers), [`book`](./Events_and_Encounters.md#object-book), [`brace`](./Events_and_Encounters.md#object-brace), [`break_ice`](./Events_and_Encounters.md#object-break_ice), and 177 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 464 | `common`<br>`rare`<br>`cha` |
| [`reward`](../Reference_and_Meta/Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 764 | `{ . . . }` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1009 | `1`<br>`10`<br>`15` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `play_animation` | String | Specifies an animation to play, optionally as an array with a probability weight. | 179 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 38 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `cutscene` | `String` | Specifies the name of a cutscene to play. | 46 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| [`conditional_reward`](../Reference_and_Meta/Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 126 | `{ . . . }` |
| `begin_chapter` | `String` | Specifies the chapter file to begin, transitioning to that chapter. | 13 | `dimensionx.gon`<br>`endoftime.gon`<br>`future.gon` |
| `complete_item_quest` | `String` | Marks the specified item quest as completed. | 22 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full` |
| `random_mutation` | Number | The number of random mutations applied to the unit. | 86 | `1`<br>`10`<br>`2` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 59 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`rare`](../Reference_and_Meta/Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 1061 | `1`<br>`10`<br>`15` |
| `event_now` | String | Triggers the specified event immediately. | 25 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| `event_now_same_cat` | String | Specifies a world event that will now occur for the same cat category as the current event. | 100 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| `lose_specific_item` | String | Removes the specified item from the player's inventory. | 13 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| `gain_disorder` | String | Specifies a disorder to add to the current cat when this event triggers. | 98 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| `trigger_adventure_unlock` | `String` | Triggers the specified adventure or map unlock quest. | 13 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| `increment_legacy_counter` | String | Specifies a legacy counter to increment by one when this event triggers. | 69 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| `add_weather` | String | Specifies a weather effect type to apply to the current map. | 67 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 90 | `[` |
| `get_item` | String | Specifies an item to add to the player's inventory when this event triggers. | 125 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| `get_item_from_pool` | String | Grants an item from the specified pool or a specific item name. | 349 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`mutation`](../Reference_and_Meta/Miscellaneous.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 31 | `{ . . . }` |
| [`random_pool_consider_luck`](../Reference_and_Meta/Arrays.md#array-random_pool_consider_luck) | Array | An array or weighted pool of rewards that are rolled considering the unit's luck stat. | 6 | `[` |
| `heal_disorder` | Number | Specifies which disorder type to heal, or the number of disorders to heal. | 11 | `1`<br>`2`<br>`Anxiety` |
| `level_up` | String | Specifies which units to level up, such as 'all' or 'self'. | 13 | `all`<br>`self` |
| `get_parasite` | String | Specifies a parasite item to attach to a unit when this event triggers. | 60 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `heal_injury` | `Number` | The number of injury points to heal on the target unit. | 6 | `1`<br>`5` |
| `kill` | String | Kills the specified target type (e.g., 'cat'). | 16 | `cat` |
| `unlock_item_quest` | `String` | Specifies the item whose quest is unlocked or advanced. | 4 | `CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full`<br>`JarOfChaos` |
| [`transform_item`](../Reference_and_Meta/Arrays.md#array-transform_item) | Array | An array specifying source and destination item IDs to transform one into the other. | 4 | `[JarOfRadiatedBlood JarOfChaos]`<br>`[JarOfRadiation JarOfRadiatedBlood]` |
| `injury` | String | Specifies the type of injury applied, such as bleeding or stat reduction. | 109 | `bleeding`<br>`burned`<br>`cha` |
| `clear_surviving_kaiju` | `String` | Specifies which surviving kaiju to clear or remove. | 2 | `pyrophina`<br>`zaratana` |
| `cutscene_on_exit` | String | Determines which cutscene to play when the player leaves the current location. | 5 | `infinite_intro`<br>`king_intro` |
| [`override_end_option_prompt`](../Assets_and_Localization/Strings.md#string-override_end_option_prompt) | String | Specifies a custom prompt string to display for the end option of this event choice. | 22 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| `learn_ability_from_pool` | String | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 6 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| `learn_passive_from_pool` | String | An array specifying a pool or list of passives from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked passive. | 5 | `AnyUnlocked`<br>`Necromancer`<br>`[MiniMe SkillShare]` |
| [`party_gain_disorder_from_pool`](../Reference_and_Meta/Arrays.md#array-party_gain_disorder_from_pool) | Array | An array specifying the pool or list of disorders for the party to gain. | 3 | `[Dwarfism]`<br>`[Gigantism]`<br>`all_disorders` |
| `gain_disorder_from_pool` | String | Specifies a pool of disorders from which one is randomly gained. | 88 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| `ally_ambush_next_fights` | Number | The number of upcoming fights that will start with an ally ambush. | 18 | `1`<br>`2` |
| `clone_self_to_party` | `Number` | The number of clones of the unit added to the party. | 1 | `1` |
| `copy_items_to_party` | `Number` | The number of times the unit's items are copied to the party. | 1 | `1` |
| `copy_party_items` | `Number` | The number of times party items are copied to the unit. | 1 | `1` |
| [`gain_clone_familiar`](../Reference_and_Meta/Miscellaneous.md#object-gain_clone_familiar) | Object  | An object that triggers the gaining of a clone familiar, with a specified object name. | 1 | `{ . . . }` |
| `get_full_item_set_from_pool` | `String` | Specifies the item pool rarity from which to generate a full set of items. | 3 | `common` |
| [`global_effect_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 11 | `{ . . . }` |
| `heal` | `Equation` | An equation string that determines the amount of health restored by this damage instance. | 168 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| `lose_item` | String | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 18 | `equipped`<br>`inventory`<br>`parasite` |
| `next_event_bonus` | Number | A modifier to the next event's outcome roll or selection chance. | 32 | `-1`<br>`-2`<br>`1` |
| `next_event_from_set` | String | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 10 | `CatHole`<br>`Tragedy`<br>`WatchingHead2` |
| `scramble_abilities` | `String` | Specifies which abilities to randomize, such as 'all'. | 3 | `all` |
| `scramble_passives` | `String` | Specifies which passive abilities to randomize or scramble. | 2 | `all` |
| `shop_now` | `String` | Triggers the specified shop to appear immediately. | 15 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| `trigger_butterfly_effect` | `Number` | The number of times to trigger the butterfly effect event. | 1 | `1` |
| `upgrade_ability` | `String` | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 6 | `random` |
| `upgrade_passive` | `String` | Specifies which passive ability to upgrade, or 'random' for a random choice. | 5 | `random` |

</details>


---


### Object: `bad`


**Definition:** Defines the bad outcome branch of an event option, including its frame and rewards.  
**Total Count:** 343

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`arm`](./Events_and_Encounters.md#object-arm), [`attack`](./Events_and_Encounters.md#object-attack), [`bash`](./Events_and_Encounters.md#object-bash), [`bash_past_alt`](./Events_and_Encounters.md#object-bash_past_alt), [`bite`](./Events_and_Encounters.md#object-bite), [`bite_it_off`](./Events_and_Encounters.md#object-bite_it_off), [`blue_needle`](./Events_and_Encounters.md#object-blue_needle), [`body`](./Events_and_Encounters.md#object-body), [`break_ice`](./Events_and_Encounters.md#object-break_ice), [`break_lock`](./Events_and_Encounters.md#object-break_lock), [`bribe`](./Events_and_Encounters.md#object-bribe), [`catch`](./Events_and_Encounters.md#object-catch), [`challenge_to_game`](./Events_and_Encounters.md#object-challenge_to_game), [`charm`](./Events_and_Encounters.md#object-charm), [`charm_past_alt`](./Events_and_Encounters.md#object-charm_past_alt), [`climb`](./Events_and_Encounters.md#object-climb), [`comfort`](./Events_and_Encounters.md#object-comfort), [`communicate`](./Events_and_Encounters.md#object-communicate), [`concheck`](./Events_and_Encounters.md#object-concheck), and 106 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 249 | `common`<br>`rare`<br>`cha` |
| [`reward`](../Reference_and_Meta/Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 764 | `{ . . . }` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1009 | `1`<br>`10`<br>`15` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `play_animation` | String | Specifies an animation to play, optionally as an array with a probability weight. | 179 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| `battle` | `String` | Defines a battle encounter by preset, level file path, or reverb settings. | 36 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| `gain_disorder_from_pool` | String | Specifies a pool of disorders from which one is randomly gained. | 88 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| `kill` | `String` | Kills the specified target type (e.g., 'cat'). | 16 | `cat` |
| [`self_status_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 199 | `{ . . . }` |
| [`cutscene`](../Assets_and_Localization/Strings.md#string-cutscene) | String | Specifies the name of a cutscene to play. | 46 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| `event_now` | String | Triggers the specified event immediately. | 25 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| `event_now_same_cat` | `String` | Specifies a world event that will now occur for the same cat category as the current event. | 100 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| `get_parasite_from_pool` | String | Specifies the pool name or explicit list of parasites to obtain from. | 43 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`conditional_reward`](../Reference_and_Meta/Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 126 | `{ . . . }` |
| `injury` | String | Specifies the type of injury applied, such as bleeding or stat reduction. | 109 | `bleeding`<br>`burned`<br>`cha` |
| `next_event_bonus` | Number | A modifier to the next event's outcome roll or selection chance. | 32 | `-1`<br>`-2`<br>`1` |
| `gain_immortal_familiar` | `String` | Specifies the immortal familiar to add to the party. | 3 | `CharmedFlea`<br>`CharmedFleaSpecial`<br>`CharmedPooter` |
| `get_parasite` | `String` | Specifies a parasite item to attach to a unit when this event triggers. | 60 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `lose_item` | `String` | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 18 | `equipped`<br>`inventory`<br>`parasite` |
| [`party_random_mutation_from_set`](../Reference_and_Meta/Miscellaneous.md#object-party_random_mutation_from_set) | Object  | An object specifying the count and mutation parts to randomly apply to the party. | 2 | `{ . . . }` |
| [`permanent_stats`](../Reference_and_Meta/Miscellaneous.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 148 | `{ . . . }` |
| `select_item_from_pool_for_cutscene_only` | `String` | Selects an item from a named pool for display in a cutscene without granting it. | 2 | `glitched_items` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 38 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |

</details>


---


### Object: `intro`


**Definition:** An object defining the introductory cutscene for the event, including title, cat selection, and visuals.  
**Total Count:** 220

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cat_choice`](../Reference_and_Meta/Enums.md#enum-cat_choice) | Enum | Determines how the cat is selected for an event, such as randomly. | 214 | `random` |
| [`event_clip`](../Reference_and_Meta/Enums.md#enum-event_clip) | Enum | Specifies the type of visual clip or animation used for the event frame. | 214 | `NonWheelEvent` |
| [`subject_clip`](../Reference_and_Meta/Enums.md#enum-subject_clip) | Enum | Specifies the type of visual clip used for the subject frame. | 214 | `EventSubject` |
| [`subject_frame`](../Reference_and_Meta/Enums.md#enum-subject_frame) | Enum | Specifies the specific art or visual frame used for the event's subject. | 215 | `a_beggar`<br>`a_few_coins`<br>`a_large_poop` |
| [`title`](../Assets_and_Localization/Strings.md#string-title) | String | The display title or name of the event. | 214 | `"Ability Pool Test"`<br>`"Blessing!"`<br>`"EVENT_ABEGGAR_NAME"` |
| [`choose_cat_with_item`](../Reference_and_Meta/Enums.md#enum-choose_cat_with_item) | Enum | Selects a cat that has a specific item equipped. | 17 | `CryogenicTimeChamber_Full`<br>`GuillotinasHead`<br>`PutridLeech` |
| `different_from_last_x_cats` | Number | The number of past events the chosen cat must differ from to avoid repeats. | 3 | `1`<br>`2`<br>`3` |
| `subject_frame_inner` | Number | An index for the inner frame variant of the subject art. | 3 | `2`<br>`4` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 214 | `common`<br>`rare`<br>`cha` |
| `choose_cat_with_highest_stat` | Equation | Selects the cat with the highest value of the specified stat. | 1 | `int` |
| [`choose_cat_with_item_slot_equipped`](../Reference_and_Meta/Enums.md#enum-choose_cat_with_item_slot_equipped) | Enum | Selects a cat that has an item equipped in the specified slot. | 1 | `weapon` |
| `choose_cat_with_min_health` | Number | Selects a cat with at least the specified percentage of health remaining. | 2 | `75%` |
| `choose_cat_with_most_injuries` | Boolean | If true, selects the cat with the highest number of injuries. | 1 | `true` |
| `choose_cat_with_parasite` | Boolean | If true, selects a cat that has a parasite. | 1 | `true` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1009 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `main`


**Definition:** An object containing the primary prompt and options for an event.  
**Total Count:** 215

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 220 | `common`<br>`rare`<br>`cha` |
| [`options`](../Reference_and_Meta/Arrays.md#array-options) | Array  | An array of named option objects within an event, each defining a possible action the player can take. | 211 | `[smash bash open]` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| [`setup`](../Reference_and_Meta/Miscellaneous.md#object-setup) | Object  | Defines actions or checks to run before the main event logic, often setting up conditions or tokens. | 24 | `{ . . . }` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `goto` | `String` | Determines which labeled point in the event's script to jump to next, controlling flow. | 4 | `end` |
| [`outcome`](../Reference_and_Meta/Miscellaneous.md#object-outcome) | Object  | An object defining the possible outcomes of an event, typically containing a random pool or weighted lists of rewards and animations. | 4 | `{ . . . }` |
| `max_options` | `Number` | The maximum number of event options presented to the player. | 3 | `2`<br>`3` |
| `shuffle_options` | `Boolean` | If true, randomizes the order of event options presented to the player. | 3 | `true` |
| [`leave`](../Reference_and_Meta/Miscellaneous.md#object-leave) | Object  | An object defining the player action to leave or ignore the event, including its stat check and outcomes. | 41 | `{ . . . }` |
| [`ignore`](../Reference_and_Meta/Miscellaneous.md#object-ignore) | Object | An object defining the player action to ignore the event, including its stat check and outcomes. | 57 | `{ . . . }` |
| [`open`](../Reference_and_Meta/Miscellaneous.md#object-open) | Object | An object defining the player action to open a container, including its stat check and outcomes. | 72 | `{ . . . }` |
| [`buy2`](../Reference_and_Meta/Miscellaneous.md#object-buy2) | Object | Defines an event option that allows the player to buy an item for 10 coins. | 1 | `{ . . . }` |
| [`buy3`](../Reference_and_Meta/Miscellaneous.md#object-buy3) | Object | Defines an event option that allows the player to buy an item for 25 coins. | 1 | `{ . . . }` |
| [`examine`](../Reference_and_Meta/Miscellaneous.md#object-examine) | Object | An object defining the player action to examine an object, including its stat check and outcomes. | 50 | `{ . . . }` |
| [`pick`](../Reference_and_Meta/Miscellaneous.md#object-pick) | Object | An object defining the player action to pick or collect an object, including its stat check and outcomes. | 3 | `{ . . . }` |

</details>


---


### Object: `options`


**Definition:** An array of named option objects within an event, each defining a possible action the player can take.  
**Total Count:** 211

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#object-main)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ignore`](../Reference_and_Meta/Miscellaneous.md#object-ignore) | Object  | An object defining the player action to ignore the event, including its stat check and outcomes. | 57 | `{ . . . }` |
| [`examine`](../Reference_and_Meta/Miscellaneous.md#object-examine) | Object  | An object defining the player action to examine an object, including its stat check and outcomes. | 50 | `{ . . . }` |
| [`leave`](../Reference_and_Meta/Miscellaneous.md#object-leave) | Object  | An object defining the player action to leave or ignore the event, including its stat check and outcomes. | 41 | `{ . . . }` |
| [`loot`](../Reference_and_Meta/Miscellaneous.md#object-loot) | Object  | An object defining the player action to loot a container or corpse, including its stat check and outcomes. | 27 | `{ . . . }` |
| [`eat`](../Reference_and_Meta/Miscellaneous.md#object-eat) | Object  | An object defining the player action to consume something, including its stat check and outcomes. | 27 | `{ . . . }` |
| [`smash`](../Reference_and_Meta/Miscellaneous.md#object-smash) | Object  | An object defining the player action to smash an object, including its stat check and outcomes. | 21 | `{ . . . }` |
| [`destroy`](../Reference_and_Meta/Miscellaneous.md#object-destroy) | Object  | An object defining the player action to destroy an object, including its stat check and outcomes. | 14 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 144 | `common`<br>`rare`<br>`cha` |
| [`bash`](../Reference_and_Meta/Miscellaneous.md#object-bash) | Object  | An object defining the player action to bash open a container, including its stat check and outcomes. | 15 | `{ . . . }` |
| [`sneak`](../Reference_and_Meta/Miscellaneous.md#object-sneak) | Object  | An object defining the player action to sneak past a threat, including its stat check and outcomes. | 11 | `{ . . . }` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`open`](../Reference_and_Meta/Miscellaneous.md#object-open) | Object  | An object defining the player action to open a container, including its stat check and outcomes. | 72 | `{ . . . }` |
| [`take`](../Reference_and_Meta/Miscellaneous.md#object-take) | Object  | An object defining the player action to take an item, including its stat check and outcomes. | 9 | `{ . . . }` |
| [`a`](../Reference_and_Meta/Miscellaneous.md#object-a) | Object  | An object defining the first custom option in a test or debug event. | 7 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 883 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`b`](../Reference_and_Meta/Miscellaneous.md#object-b) | Object  | An object defining the second custom option in a test or debug event. | 7 | `{ . . . }` |
| [`c`](../Reference_and_Meta/Miscellaneous.md#object-c) | Object  | An object defining the third custom option in a test or debug event. | 7 | `{ . . . }` |
| [`charm`](../Reference_and_Meta/Miscellaneous.md#object-charm) | Object  | Specifies the player character's attempt to charm or persuade the encounter. | 8 | `{ . . . }` |
| [`fight`](../Reference_and_Meta/Miscellaneous.md#object-fight) | Object  | Specifies the player character's attempt to fight or force their way through the encounter. | 7 | `{ . . . }` |
| [`touch`](../Reference_and_Meta/Miscellaneous.md#object-touch) | Object  | Specifies the player character's attempt to physically touch or interact with the encounter. | 7 | `{ . . . }` |
| [`activate_p`](../Reference_and_Meta/Miscellaneous.md#object-activate_p) | Object  | Specifies the player character's attempt to activate the object (press a button/lever). | 6 | `{ . . . }` |
| [`activate_z`](../Reference_and_Meta/Miscellaneous.md#object-activate_z) | Object  | Specifies the player character's attempt to activate the object (pull a lever/switch). | 6 | `{ . . . }` |
| [`d`](../Reference_and_Meta/Miscellaneous.md#object-d) | Object  | Specifies a debug or test option for game development purposes. | 6 | `{ . . . }` |
| [`enter`](../Reference_and_Meta/Miscellaneous.md#object-enter) | Object  | Specifies the player character's attempt to enter or go inside the encounter location. | 10 | `{ . . . }` |
| [`inspect`](../Reference_and_Meta/Miscellaneous.md#object-inspect) | Object  | Specifies the player character's attempt to inspect or examine the encounter. | 6 | `{ . . . }` |
| [`lick`](../Reference_and_Meta/Miscellaneous.md#object-lick) | Object  | Specifies the player character's attempt to lick the encounter. | 7 | `{ . . . }` |
| [`drink`](../Reference_and_Meta/Miscellaneous.md#object-drink) | Object  | Specifies the player character's attempt to drink from or consume the encounter. | 6 | `{ . . . }` |
| [`kiss`](../Reference_and_Meta/Miscellaneous.md#object-kiss) | Object  | Specifies the player character's attempt to kiss the encounter. | 6 | `{ . . . }` |
| [`run`](../Reference_and_Meta/Miscellaneous.md#object-run) | Object  | Specifies the player character's attempt to run away or flee from the encounter. | 8 | `{ . . . }` |
| [`bite`](../Reference_and_Meta/Miscellaneous.md#object-bite) | Object  | Specifies the player character's attempt to bite the encounter. | 9 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`go_around`](../Reference_and_Meta/Miscellaneous.md#object-go_around) | Object  | Specifies the player character's attempt to go around or bypass the encounter. | 4 | `{ . . . }` |
| [`home`](../Reference_and_Meta/Miscellaneous.md#object-home) | Object  | Specifies the option to go home (exit to the main hub). | 20 | `{ . . . }` |
| [`past`](../Reference_and_Meta/Miscellaneous.md#object-past) | Object  | Specifies the option to travel to a past era (Ice Age, Jurassic, etc.). | 4 | `{ . . . }` |
| [`skip`](../Reference_and_Meta/Miscellaneous.md#object-skip) | Object  | Specifies the option to skip or decline the current encounter. | 5 | `{ . . . }` |
| [`investigate`](../Reference_and_Meta/Miscellaneous.md#object-investigate) | Object  | Specifies the player character's attempt to investigate the encounter. | 3 | `{ . . . }` |
| [`repell`](../Reference_and_Meta/Miscellaneous.md#object-repell) | Object  | Specifies the player character's attempt to rappel down or climb into the encounter. | 3 | `{ . . . }` |
| [`attach_antenna`](../Reference_and_Meta/Miscellaneous.md#object-attach_antenna) | Object  | Specifies the player character's attempt to attach a device or antenna to the encounter. | 2 | `{ . . . }` |
| [`boogers`](../Reference_and_Meta/Miscellaneous.md#object-boogers) | Object  | Specifies the player character's attempt to pick or examine boogers. | 2 | `{ . . . }` |
| [`copy`](../Reference_and_Meta/Miscellaneous.md#object-copy) | Object  | Specifies the player character's attempt to copy or replicate something from the encounter. | 2 | `{ . . . }` |
| [`find_another_way`](../Reference_and_Meta/Miscellaneous.md#object-find_another_way) | Object  | Specifies the player character's attempt to find an alternative path around the encounter. | 2 | `{ . . . }` |
| [`move_closer`](../Reference_and_Meta/Miscellaneous.md#object-move_closer) | Object  | Specifies the player character's attempt to move closer to the encounter. | 2 | `{ . . . }` |
| [`play`](../Reference_and_Meta/Miscellaneous.md#object-play) | Object  | Specifies the player character's attempt to play or interact playfully with the encounter. | 2 | `{ . . . }` |
| [`poop`](../Reference_and_Meta/Miscellaneous.md#object-poop) | Object  | Defines a poop event or interaction, often part of a random encounter or response in dialogue. | 19 | `{ . . . }` |
| [`print`](../Reference_and_Meta/Miscellaneous.md#object-print) | Object  | Specifies the player character's attempt to print or output something from the encounter. | 2 | `{ . . . }` |
| [`protection`](../Reference_and_Meta/Miscellaneous.md#object-protection) | Object  | Specifies the player character's attempt to offer or ask for protection. | 2 | `{ . . . }` |
| [`repair`](../Reference_and_Meta/Miscellaneous.md#object-repair) | Object  | Specifies the player character's attempt to repair the encounter object. | 2 | `{ . . . }` |
| [`sacrifice`](../Reference_and_Meta/Miscellaneous.md#object-sacrifice) | Object  | Specifies the player character's attempt to make a sacrifice at the encounter. | 2 | `{ . . . }` |
| `scale` | Float | The scale multiplier applied to the unit's visual size. | 157 | `.5`<br>`.6`<br>`.7` |
| [`turnon`](../Reference_and_Meta/Miscellaneous.md#object-turnon) | Object  | Specifies the player character's attempt to turn on or activate the encounter. | 2 | `{ . . . }` |
| [`altar_sacrifice`](../Reference_and_Meta/Miscellaneous.md#object-altar_sacrifice) | Object  | Specifies the player character's attempt to sacrifice a cat at the altar. | 1 | `{ . . . }` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| [`arm`](../Reference_and_Meta/Miscellaneous.md#object-arm) | Object  | Specifies the player character's attempt to put their arm inside the encounter. | 1 | `{ . . . }` |
| [`attach_amplifier`](../Reference_and_Meta/Miscellaneous.md#object-attach_amplifier) | Object  | Specifies the player character's attempt to attach an amplifier to the encounter. | 1 | `{ . . . }` |
| [`attach_leech`](../Reference_and_Meta/Miscellaneous.md#object-attach_leech) | Object  | Specifies the player character's attempt to attach a leech to the encounter. | 1 | `{ . . . }` |
| [`bash_past_alt`](../Reference_and_Meta/Miscellaneous.md#object-bash_past_alt) | Object  | Specifies the player character's attempt to bash through the encounter (alternate version for specific chapters). | 1 | `{ . . . }` |
| [`bite_it_off`](../Reference_and_Meta/Miscellaneous.md#object-bite_it_off) | Object  | Specifies the player character's attempt to bite off part of the encounter. | 1 | `{ . . . }` |
| [`blue`](../Reference_and_Meta/Miscellaneous.md#object-blue) | Object  | Specifies the player character's attempt to choose the blue option. | 18 | `{ . . . }` |
| [`blue_needle`](../Reference_and_Meta/Miscellaneous.md#object-blue_needle) | Object  | Specifies the player character's attempt to take the blue needle. | 1 | `{ . . . }` |
| `body` | Float | The catalog ID for the cat's body part. | 203 | `-1`<br>`1`<br>`1.1` |
| [`book`](../Reference_and_Meta/Miscellaneous.md#object-book) | Object  | Specifies the player character's attempt to read or take the book. | 1 | `{ . . . }` |
| [`brace`](../Reference_and_Meta/Miscellaneous.md#object-brace) | Object  | Specifies the player character's attempt to brace themselves for the encounter. | 5 | `{ . . . }` |
| [`break_ice`](../Reference_and_Meta/Miscellaneous.md#object-break_ice) | Object  | Specifies the player character's attempt to break the ice covering the encounter. | 1 | `{ . . . }` |
| [`break_lock`](../Reference_and_Meta/Miscellaneous.md#object-break_lock) | Object  | Specifies the player character's attempt to break the lock on the encounter. | 1 | `{ . . . }` |
| [`bribe`](../Reference_and_Meta/Miscellaneous.md#object-bribe) | Object  | Specifies the player character's attempt to bribe the encounter. | 1 | `{ . . . }` |
| [`button`](../Reference_and_Meta/Miscellaneous.md#object-button) | Object  | Specifies the player character's attempt to push the button. | 1 | `{ . . . }` |
| [`buy1`](../Reference_and_Meta/Miscellaneous.md#object-buy1) | Object  | Specifies the player character's attempt to buy one of the offered items. | 1 | `{ . . . }` |
| [`catch`](../Reference_and_Meta/Miscellaneous.md#object-catch) | Object  | An object defining a response option for catching an entity, including stat checks and rewards. | 2 | `{ . . . }` |
| [`challenge_to_game`](../Reference_and_Meta/Miscellaneous.md#object-challenge_to_game) | Object  | Specifies the player character's attempt to challenge the encounter to a game. | 1 | `{ . . . }` |
| [`chaos_ending`](../Reference_and_Meta/Miscellaneous.md#object-chaos_ending) | Object  | Specifies the option to trigger the chaos ending cutscene. | 1 | `{ . . . }` |
| [`chapter_cutscene`](../Reference_and_Meta/Miscellaneous.md#object-chapter_cutscene) | Object  | Specifies the option to trigger a chapter intro cutscene. | 1 | `{ . . . }` |
| [`charm_past_alt`](../Reference_and_Meta/Miscellaneous.md#object-charm_past_alt) | Object  | Specifies the player character's attempt to charm the encounter (alternate version for specific chapters). | 1 | `{ . . . }` |
| [`climb`](../Reference_and_Meta/Miscellaneous.md#object-climb) | Object  | Specifies the player character's attempt to climb over the encounter. | 1 | `{ . . . }` |
| [`comfort`](../Reference_and_Meta/Miscellaneous.md#object-comfort) | Object  | A charisma-based event response that soothes the encounter subject. | 1 | `{ . . . }` |
| [`communicate`](../Reference_and_Meta/Miscellaneous.md#object-communicate) | Object  | A charisma-based event response to establish communication. | 1 | `{ . . . }` |
| [`concheck`](../Reference_and_Meta/Miscellaneous.md#object-concheck) | Object  | A constitution-based event response to test endurance. | 1 | `{ . . . }` |
| [`counter`](../Reference_and_Meta/Miscellaneous.md#object-counter) | Object  | An event response that uses a countering action, with no stat requirement. | 3 | `{ . . . }` |
| [`crack_open`](../Reference_and_Meta/Miscellaneous.md#object-crack_open) | Object  | A strength-based event response to break something open. | 1 | `{ . . . }` |
| [`cross`](../Reference_and_Meta/Miscellaneous.md#object-cross) | Object  | An event response to traverse an obstacle, with no stat requirement. | 74 | `{ . . . }` |
| [`cut_wires`](../Reference_and_Meta/Miscellaneous.md#object-cut_wires) | Object  | An intelligence-based event response to disable wires. | 1 | `{ . . . }` |
| [`damage_1`](../Reference_and_Meta/Miscellaneous.md#object-damage_1) | Object  | A constitution-based event response that deals minor damage. | 1 | `{ . . . }` |
| [`damage_full`](../Reference_and_Meta/Miscellaneous.md#object-damage_full) | Object  | A constitution-based event response that deals full damage. | 1 | `{ . . . }` |
| [`damage_half`](../Reference_and_Meta/Miscellaneous.md#object-damage_half) | Object  | A constitution-based event response that deals halved damage. | 1 | `{ . . . }` |
| [`desert_cutscene`](../Reference_and_Meta/Miscellaneous.md#object-desert_cutscene) | Object  | An event response that triggers a desert-themed cutscene, with no stat requirement. | 1 | `{ . . . }` |
| [`dexcheck`](../Reference_and_Meta/Miscellaneous.md#object-dexcheck) | Object  | A dexterity-based event response to test agility. | 1 | `{ . . . }` |
| [`dig`](../Reference_and_Meta/Miscellaneous.md#object-dig) | Object  | A strength-based event response to excavate, limited by a token counter maximum. | 3 | `{ . . . }` |
| [`disarm`](../Reference_and_Meta/Miscellaneous.md#object-disarm) | Object  | A dexterity-based event response to remove a trap. | 1 | `{ . . . }` |
| [`dive`](../Reference_and_Meta/Miscellaneous.md#object-dive) | Object  | A dexterity-based event response to plunge into water. | 1 | `{ . . . }` |
| [`donate`](../Reference_and_Meta/Miscellaneous.md#object-donate) | Object  | An event response to give a donation, with no stat requirement but a coin cost. | 1 | `{ . . . }` |
| [`donate_10`](../Reference_and_Meta/Miscellaneous.md#object-donate_10) | Object  | An event response to donate 10 coins. | 1 | `{ . . . }` |
| [`donate_15`](../Reference_and_Meta/Miscellaneous.md#object-donate_15) | Object  | An event response to donate 15 coins. | 1 | `{ . . . }` |
| [`donate_20`](../Reference_and_Meta/Miscellaneous.md#object-donate_20) | Object  | An event response to donate 20 coins. | 1 | `{ . . . }` |
| [`donate_5`](../Reference_and_Meta/Miscellaneous.md#object-donate_5) | Object  | An event response to donate 5 coins. | 1 | `{ . . . }` |
| [`double`](../Reference_and_Meta/Miscellaneous.md#object-double) | Object  | An event response that doubles something, with no stat requirement. | 1 | `{ . . . }` |
| [`eat_meat`](../Reference_and_Meta/Miscellaneous.md#object-eat_meat) | Object  | A constitution-based event response to consume meat. | 1 | `{ . . . }` |
| [`enter_crater`](../Reference_and_Meta/Miscellaneous.md#object-enter_crater) | Object  | A luck-based event response to enter a crater. | 1 | `{ . . . }` |
| [`face`](../Reference_and_Meta/Enums.md#enum-face) | Enum  | The face equipment item assigned to the unit. | 228 | `1004`<br>`1019`<br>`AtomicMark` |
| [`fiddle`](../Reference_and_Meta/Miscellaneous.md#object-fiddle) | Object  | A quest-based event response to tamper, requiring no specific quest token. | 1 | `{ . . . }` |
| [`fill_jar`](../Reference_and_Meta/Miscellaneous.md#object-fill_jar) | Object  | A quest-based event response to fill a jar, with no stat requirement. | 1 | `{ . . . }` |
| [`find`](../Reference_and_Meta/Miscellaneous.md#object-find) | Object  | An event response to search, with no stat requirement. | 1 | `{ . . . }` |
| [`fire`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-fire) | Object  | An event response that uses fire, with no stat requirement. | 7 | `{ . . . }` |
| [`flush_yourself`](../Reference_and_Meta/Miscellaneous.md#object-flush_yourself) | Object  | An event response to flush oneself, requiring a minimum counter value. | 1 | `{ . . . }` |
| [`follow`](../Reference_and_Meta/Miscellaneous.md#object-follow) | Object  | A speed-based event response to pursue. | 1 | `{ . . . }` |
| [`free`](../Reference_and_Meta/Miscellaneous.md#object-free) | Object  | If true, this option requires no cost to activate. | 2 | `{ . . . }` |
| [`future`](../Reference_and_Meta/Miscellaneous.md#object-future) | Object  | Specifies the name, map flag, or connection for the Future area. | 30 | `{ . . . }` |
| [`give_parasite`](../Reference_and_Meta/Miscellaneous.md#object-give_parasite) | Object  | An event response to give a parasite, requiring the cat to have a parasite. | 1 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`hack`](../Reference_and_Meta/Miscellaneous.md#object-hack) | Object  | An intelligence-based event response to hack a system. | 1 | `{ . . . }` |
| [`head`](../Reference_and_Meta/Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 449 | `-1`<br>`1`<br>`1.3` |
| [`holy`](../Reference_and_Meta/Miscellaneous.md#object-holy) | Object  | An event response that uses holy power, with no stat requirement. | 5 | `{ . . . }` |
| [`hp`](../Reference_and_Meta/Miscellaneous.md#object-hp) | Object  | An event response that trades health, with no stat requirement. | 1 | `{ . . . }` |
| [`ice`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-ice) | Object  | An event response that uses ice, with no stat requirement. | 4 | `{ . . . }` |
| [`infinite`](../Reference_and_Meta/Miscellaneous.md#object-infinite) | Object  | An event response to choose infinite, with a chapter exit hint and no stat requirement. | 10 | `{ . . . }` |
| [`intcheck`](../Reference_and_Meta/Miscellaneous.md#object-intcheck) | Object  | An intelligence-based event response to test intellect. | 1 | `{ . . . }` |
| [`intimidation`](../Reference_and_Meta/Miscellaneous.md#object-intimidation) | Object  | An event response that intimidates, with no stat requirement. | 1 | `{ . . . }` |
| [`itchies`](../Reference_and_Meta/Miscellaneous.md#object-itchies) | Object  | An event response that causes itches, with no stat requirement. | 1 | `{ . . . }` |
| [`join`](../Reference_and_Meta/Miscellaneous.md#object-join) | Object  | A charisma-based event response to join in. | 1 | `{ . . . }` |
| [`jump`](../Reference_and_Meta/Miscellaneous.md#object-jump) | Object  | A speed-based event response to leap. | 3 | `{ . . . }` |
| [`jump_over`](../Reference_and_Meta/Miscellaneous.md#object-jump_over) | Object  | A dexterity-based event response to vault over. | 1 | `{ . . . }` |
| [`keep_going`](../Reference_and_Meta/Miscellaneous.md#object-keep_going) | Object  | An event response to persevere, with no stat requirement. | 1 | `{ . . . }` |
| [`kiss_meat`](../Reference_and_Meta/Miscellaneous.md#object-kiss_meat) | Object  | A charisma-based event response to kiss meat. | 1 | `{ . . . }` |
| [`knife`](../Reference_and_Meta/Miscellaneous.md#object-knife) | Object  | An event response to obtain a knife, with no stat requirement. | 2 | `{ . . . }` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`leave_it_in`](../Reference_and_Meta/Miscellaneous.md#object-leave_it_in) | Object  | An event response to leave an object in place, with no stat requirement. | 1 | `{ . . . }` |
| [`leg`](../Reference_and_Meta/Miscellaneous.md#object-leg) | Object  | A luck-based event response to use a leg. | 1 | `{ . . . }` |
| [`lever`](../Reference_and_Meta/Miscellaneous.md#object-lever) | Object  | An event response to pull a lever, with a fixed chance and no stat requirement. | 2 | `{ . . . }` |
| [`lick_alt`](../Reference_and_Meta/Miscellaneous.md#object-lick_alt) | Object  | A constitution-based event response to lick, restricted to specific chapters. | 1 | `{ . . . }` |
| [`lightning`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-lightning) | Object  | An event response using lightning, with no stat requirement. | 2 | `{ . . . }` |
| [`listen`](../Reference_and_Meta/Miscellaneous.md#object-listen) | Object  | An intelligence-based event response to listen. | 1 | `{ . . . }` |
| [`looks`](../Reference_and_Meta/Miscellaneous.md#object-looks) | Object  | The dialogue option for the Genie good event that selects the looks reward. | 1 | `{ . . . }` |
| [`loot_heart`](../Reference_and_Meta/Miscellaneous.md#object-loot_heart) | Object  | The dialogue option to take the heart from the Dead King as a quest action. | 1 | `{ . . . }` |
| [`makeup`](../Reference_and_Meta/Miscellaneous.md#object-makeup) | Object  | The dialogue option for the makeup event, associated with the Tink2 encounter. | 1 | `{ . . . }` |
| [`mind`](../Reference_and_Meta/Miscellaneous.md#object-mind) | Object  | The dialogue option for the Genie bad event that selects the curse mind reward. | 1 | `{ . . . }` |
| [`neck`](../Reference_and_Meta/Enums.md#enum-neck) | Enum  | The neck equipment item assigned to the unit. | 209 | `AngelicAura`<br>`AngelicAura_Terminator`<br>`DruidNeck` |
| [`nothanks`](../Reference_and_Meta/Miscellaneous.md#object-nothanks) | Object  | The generic decline dialogue option that triggers a leave animation. | 1 | `{ . . . }` |
| [`outsmart`](../Reference_and_Meta/Miscellaneous.md#object-outsmart) | Object  | The dialogue option that uses the int stat to outsmart the tutorial encounter. | 1 | `{ . . . }` |
| [`patch_up`](../Reference_and_Meta/Miscellaneous.md#object-patch_up) | Object  | The dialogue option that uses the int stat to patch up the dying fetus. | 1 | `{ . . . }` |
| [`pick_lock`](../Reference_and_Meta/Miscellaneous.md#object-pick_lock) | Object  | The dialogue option that uses the dex stat to pick a lock on a crate. | 1 | `{ . . . }` |
| [`pilfer`](../Reference_and_Meta/Miscellaneous.md#object-pilfer) | Object  | The dialogue option that uses the lck stat to pilfer from a pile of skulls. | 1 | `{ . . . }` |
| [`pirouette`](../Reference_and_Meta/Miscellaneous.md#object-pirouette) | Object  | The dialogue option for the Tink1 encounter that performs a pirouette. | 1 | `{ . . . }` |
| [`place_gristle`](../Reference_and_Meta/Miscellaneous.md#object-place_gristle) | Object  | The dialogue option to place gristle on the Wall of Flesh as a quest action. | 1 | `{ . . . }` |
| [`power`](../Reference_and_Meta/Miscellaneous.md#object-power) | Object  | The dialogue option for the Genie good event that selects the power reward. | 3 | `{ . . . }` |
| [`pull`](../Reference_and_Meta/Miscellaneous.md#object-pull) | Object  | The dialogue option that uses the str stat to pull a knife from a wall. | 1 | `{ . . . }` |
| [`pull_it_out`](../Reference_and_Meta/Miscellaneous.md#object-pull_it_out) | Object  | The dialogue option to pull out a stalactite from the Jagged Pathway. | 1 | `{ . . . }` |
| [`pull_lever`](../Reference_and_Meta/Miscellaneous.md#object-pull_lever) | Object  | The dialogue option to pull the lever on the Odd Device. | 1 | `{ . . . }` |
| [`purify`](../Reference_and_Meta/Miscellaneous.md#object-purify) | Object  | The dialogue option that uses the lck stat to purify the Mysterious Chamber. | 1 | `{ . . . }` |
| [`push_buttons`](../Reference_and_Meta/Miscellaneous.md#object-push_buttons) | Object  | The dialogue option to push buttons on the Odd Device. | 1 | `{ . . . }` |
| [`push_through`](../Reference_and_Meta/Miscellaneous.md#object-push_through) | Object  | The dialogue option that uses the str stat to push through the Jagged Pathway. | 1 | `{ . . . }` |
| [`put_in_coins`](../Reference_and_Meta/Miscellaneous.md#object-put_in_coins) | Object  | The dialogue option to put coins into the Vending Machine, requiring a minimum of 10 coins. | 1 | `{ . . . }` |
| [`put_out_of_misery`](../Reference_and_Meta/Miscellaneous.md#object-put_out_of_misery) | Object  | The dialogue option that uses the str stat to put the dying fetus out of its misery. | 1 | `{ . . . }` |
| [`reach_inside`](../Reference_and_Meta/Miscellaneous.md#object-reach_inside) | Object  | The dialogue option that uses the spd stat to reach inside a Small Black Hole. | 1 | `{ . . . }` |
| [`read`](../Reference_and_Meta/Miscellaneous.md#object-read) | Object  | The dialogue option that uses the int stat to read the Mysterious Manual. | 1 | `{ . . . }` |
| [`receive`](../Reference_and_Meta/Miscellaneous.md#object-receive) | Object  | The dialogue option to receive an item from a legacy event. | 4 | `{ . . . }` |
| [`red`](../Reference_and_Meta/Miscellaneous.md#object-red) | Object  | Configuration for one of the dialog options (label 'EVENT_RED_ANSW'), with a fixed chance and associated animation, in a choice event. | 16 | `{ . . . }` |
| [`red_needle`](../Reference_and_Meta/Miscellaneous.md#object-red_needle) | Object  | The dialogue option that uses the lck stat to select the red needle, requiring not having the RedNeedle token. | 1 | `{ . . . }` |
| [`reflect`](../Reference_and_Meta/Miscellaneous.md#object-reflect) | Object  | The dialogue option for the StacyMutant4 encounter that chooses to reflect. | 1 | `{ . . . }` |
| [`remove`](../Reference_and_Meta/Miscellaneous.md#object-remove) | Object  | The dialogue option that uses the str stat to remove a stuck corpse. | 1 | `{ . . . }` |
| [`remove_the_nail`](../Reference_and_Meta/Miscellaneous.md#object-remove_the_nail) | Object  | The dialogue option that uses the dex stat to remove the nail from a big toe. | 1 | `{ . . . }` |
| [`repair_quest`](../Reference_and_Meta/Miscellaneous.md#object-repair_quest) | Object  | The dialogue option to repair the broken time machine as a quest action. | 1 | `{ . . . }` |
| [`rest`](../Reference_and_Meta/Miscellaneous.md#object-rest) | Object  | The dialogue option that uses the lck stat to rest on a cat bed. | 1 | `{ . . . }` |
| [`revive`](../Reference_and_Meta/Miscellaneous.md#object-revive) | Object  | The dialogue option that uses the lck stat to revive the Dead Mammoth. | 4 | `{ . . . }` |
| [`rub`](../Reference_and_Meta/Miscellaneous.md#object-rub) | Object  | The dialogue option that uses the lck stat to rub the Genie Lamp. | 1 | `{ . . . }` |
| [`run_again`](../Reference_and_Meta/Miscellaneous.md#object-run_again) | Object  | The dialogue option that uses the spd stat to run away from Death again, requiring he hasn't chased you yet. | 1 | `{ . . . }` |
| [`run_away`](../Reference_and_Meta/Miscellaneous.md#object-run_away) | Object  | The dialogue option that uses the spd stat to run away from a Giant Sleeping Shark. | 2 | `{ . . . }` |
| [`sacrifice_full_favor`](../Reference_and_Meta/Miscellaneous.md#object-sacrifice_full_favor) | Object  | The dialogue option to sacrifice a cat at the Volcano with full favor as a quest action. | 1 | `{ . . . }` |
| [`sacrifice_normal`](../Reference_and_Meta/Miscellaneous.md#object-sacrifice_normal) | Object  | The dialogue option to perform a normal sacrifice at the Meat Altar, requiring the GuillotinasHead not equipped. | 1 | `{ . . . }` |
| [`sacrifice_partial_favor`](../Reference_and_Meta/Miscellaneous.md#object-sacrifice_partial_favor) | Object  | The dialogue option to sacrifice a cat at the Volcano with partial favor as a quest action. | 1 | `{ . . . }` |
| [`sacrifice_quest`](../Reference_and_Meta/Miscellaneous.md#object-sacrifice_quest) | Object  | The dialogue option to perform a quest sacrifice at the Meat Altar, requiring the GuillotinasHead equipped. | 1 | `{ . . . }` |
| [`scream`](../Reference_and_Meta/Miscellaneous.md#object-scream) | Object  | The dialogue option to scream at the Meat Golem with no stat requirement. | 5 | `{ . . . }` |
| [`shake`](../Reference_and_Meta/Miscellaneous.md#object-shake) | Object  | The dialogue option that uses the str stat to shake the Vending Machine. | 2 | `{ . . . }` |
| [`slip_through`](../Reference_and_Meta/Miscellaneous.md#object-slip_through) | Object  | The dialogue option that uses the dex stat to slip through a Barbed Wire Fence. | 1 | `{ . . . }` |
| [`sneak_by`](../Reference_and_Meta/Miscellaneous.md#object-sneak_by) | Object  | The dialogue option that uses the dex stat to sneak by a Giant Sleeping Shark. | 1 | `{ . . . }` |
| [`sneak_past_alt`](../Reference_and_Meta/Miscellaneous.md#object-sneak_past_alt) | Object  | The dialogue option using dex to sneak past a stray cat, available only in the Ice Age or Jurassic chapters. | 1 | `{ . . . }` |
| [`soul`](../Reference_and_Meta/Miscellaneous.md#object-soul) | Object  | The dialogue option for the Genie bad event that selects the curse soul reward. | 1 | `{ . . . }` |
| [`speed`](../Reference_and_Meta/Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 475 | `-30`<br>`-4`<br>`.5` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| [`surprise`](../Reference_and_Meta/Miscellaneous.md#object-surprise) | Object  | The dialogue option for the Butch2 encounter that surprises the target. | 1 | `{ . . . }` |
| [`sweet_talk`](../Reference_and_Meta/Miscellaneous.md#object-sweet_talk) | Object  | The dialogue option that uses the cha stat to sweet-talk Death. | 1 | `{ . . . }` |
| [`swim`](../Reference_and_Meta/Miscellaneous.md#object-swim) | Object  | The dialogue option that uses the str stat to swim through a Strong Current. | 1 | `{ . . . }` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 219 | `-1`<br>`1000`<br>`1001` |
| [`take_blood`](../Reference_and_Meta/Miscellaneous.md#object-take_blood) | Object  | The dialogue option to drain blood from the Dead King as a quest action. | 1 | `{ . . . }` |
| [`talk`](../Reference_and_Meta/Miscellaneous.md#object-talk) | Object  | The dialogue option that uses the cha stat to talk to a Spookie Apparation. | 1 | `{ . . . }` |
| [`talk_to`](../Reference_and_Meta/Miscellaneous.md#object-talk_to) | Object  | The dialogue option that uses the cha stat to talk to someone during a Dust Storm. | 1 | `{ . . . }` |
| [`tappytoes`](../Reference_and_Meta/Miscellaneous.md#object-tappytoes) | Object  | The dialogue option for the Tink1 encounter that performs a tappytoes action. | 1 | `{ . . . }` |
| [`teleport`](../Reference_and_Meta/Miscellaneous.md#object-teleport) | Object  | Defines a dialogue option that transports the unit to an alternative location in the event. | 56 | `{ . . . }` |
| [`thorns`](../Reference_and_Meta/Miscellaneous.md#object-thorns) | Object  | Defines a dialogue option that applies a thorns effect to the unit. | 2 | `{ . . . }` |
| [`throw`](../Reference_and_Meta/Miscellaneous.md#object-throw) | Object  | Defines a dialogue option that allows the unit to throw an object. | 21 | `{ . . . }` |
| [`timemachine`](../Reference_and_Meta/Miscellaneous.md#object-timemachine) | Object  | Defines a dialogue option that triggers a time travel sequence. | 1 | `{ . . . }` |
| [`traverse`](../Reference_and_Meta/Miscellaneous.md#object-traverse) | Object  | Defines a dialogue option that moves the unit through a traversal area. | 1 | `{ . . . }` |
| [`upgrade_yourself`](../Reference_and_Meta/Miscellaneous.md#object-upgrade_yourself) | Object  | Defines a dialogue option that upgrades the unit's attributes or abilities. | 1 | `{ . . . }` |
| [`use_item`](../Reference_and_Meta/Miscellaneous.md#object-use_item) | Object  | Defines a dialogue option that prompts the unit to use an item from their inventory. | 1 | `{ . . . }` |
| [`use_toilet_con`](../Reference_and_Meta/Miscellaneous.md#object-use_toilet_con) | Object  | Defines a dialogue option that interacts with a toilet using the Constitution stat. | 1 | `{ . . . }` |
| [`use_toilet_str`](../Reference_and_Meta/Miscellaneous.md#object-use_toilet_str) | Object  | Defines a dialogue option that interacts with a toilet using the Strength stat. | 1 | `{ . . . }` |
| [`use_weapon`](./NPC_Scripts.md#object-use_weapon) | Object  | Defines a dialogue option that prompts the unit to use their equipped weapon. | 3 | `{ . . . }` |
| [`w1`](../Reference_and_Meta/Miscellaneous.md#object-w1) | Object  | Defines a dialogue option for the first weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w2`](../Reference_and_Meta/Miscellaneous.md#object-w2) | Object  | Defines a dialogue option for the second weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w3`](../Reference_and_Meta/Miscellaneous.md#object-w3) | Object  | Defines a dialogue option for the third weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w4`](../Reference_and_Meta/Miscellaneous.md#object-w4) | Object  | Defines a dialogue option for the fourth weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w5`](../Reference_and_Meta/Miscellaneous.md#object-w5) | Object  | Defines a dialogue option for the fifth weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w6`](../Reference_and_Meta/Miscellaneous.md#object-w6) | Object  | Defines a dialogue option for the sixth weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`wealth`](../Reference_and_Meta/Miscellaneous.md#object-wealth) | Object  | Defines a dialogue option that grants the unit money or valuable items. | 1 | `{ . . . }` |
| [`wheezies`](../Reference_and_Meta/Miscellaneous.md#object-wheezies) | Object  | Defines a dialogue option that triggers a wheezing effect or condition. | 1 | `{ . . . }` |
| [`wish_genes`](../Reference_and_Meta/Miscellaneous.md#object-wish_genes) | Object  | Defines a dialogue option in the Monkey Paw event that modifies the unit's genetics. | 1 | `{ . . . }` |
| [`wish_items`](../Reference_and_Meta/Miscellaneous.md#object-wish_items) | Object  | Defines a dialogue option in the Monkey Paw event that grants items. | 1 | `{ . . . }` |
| [`wish_levelups`](../Reference_and_Meta/Miscellaneous.md#object-wish_levelups) | Object  | Defines a dialogue option in the Monkey Paw event that grants level-ups. | 1 | `{ . . . }` |
| [`wish_strength`](../Reference_and_Meta/Miscellaneous.md#object-wish_strength) | Object  | Defines a dialogue option in the Monkey Paw event that increases Strength. | 1 | `{ . . . }` |
| [`withstand`](../Reference_and_Meta/Miscellaneous.md#object-withstand) | Object  | Defines a dialogue option that allows the unit to withstand a hazard using Constitution. | 1 | `{ . . . }` |
| [`yank_it_out`](../Reference_and_Meta/Miscellaneous.md#object-yank_it_out) | Object  | Defines a dialogue option that yanks out an object using Strength. | 1 | `{ . . . }` |
| [`yellow_needle`](../Reference_and_Meta/Miscellaneous.md#object-yellow_needle) | Object  | Defines a dialogue option to interact with a yellow needle. | 1 | `{ . . . }` |

</details>


---


### Object: `requirements`


**Definition:** An object defining the conditions that must be met for a reward or event branch to be available.  
**Total Count:** 205

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`activate_p`](./Events_and_Encounters.md#object-activate_p), [`activate_z`](./Events_and_Encounters.md#object-activate_z), [`attach_amplifier`](./Events_and_Encounters.md#object-attach_amplifier), [`attach_antenna`](./Events_and_Encounters.md#object-attach_antenna), [`attach_leech`](./Events_and_Encounters.md#object-attach_leech), [`bash`](./Events_and_Encounters.md#object-bash), [`bash_past_alt`](./Events_and_Encounters.md#object-bash_past_alt), [`blue_needle`](./Events_and_Encounters.md#object-blue_needle), [`charm`](./Events_and_Encounters.md#object-charm), [`charm_past_alt`](./Events_and_Encounters.md#object-charm_past_alt), [`conditional_reward`](./Events_and_Encounters.md#object-conditional_reward), [`dig`](./Events_and_Encounters.md#object-dig), [`donate_10`](./Events_and_Encounters.md#object-donate_10), [`donate_15`](./Events_and_Encounters.md#object-donate_15), [`donate_20`](./Events_and_Encounters.md#object-donate_20), [`donate_5`](./Events_and_Encounters.md#object-donate_5), [`fiddle`](./Events_and_Encounters.md#object-fiddle), [`fight`](./Events_and_Encounters.md#object-fight), [`fill_jar`](./Events_and_Encounters.md#object-fill_jar), and 31 more...

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`has_token`](../Reference_and_Meta/Enums.md#enum-has_token) | Enum | Requires the player to have a specific legacy token or flag. | 82 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`counter_range`](../Reference_and_Meta/Arrays.md#array-counter_range) | Array | Requires the value of a counter to fall within a specified inclusive range. | 38 | `[WorldEventLegacyCounter_CrackInTheWall 1 1]`<br>`[WorldEventLegacyCounter_CrackInTheWall 2 2]`<br>`[WorldEventLegacyCounter_CrackInTheWall 3 3]` |
| [`not_has_token`](../Reference_and_Meta/Enums.md#enum-not_has_token) | Enum | Requires that the player does not have a specific legacy token or flag. | 31 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_MysteriousJarRepeat` |
| [`counter_minimum`](../Reference_and_Meta/Arrays.md#array-counter_minimum) | Array | Requires the value of a counter to be at least the specified number. | 26 | `[WorldEventLegacyCounter_CrackInTheWall 4]`<br>`[WorldEventLegacyCounter_FooCounter 5]`<br>`[WorldEventLegacyCounter_Jack 100]` |
| [`cat_has_item_equipped`](../Reference_and_Meta/Enums.md#enum-cat_has_item_equipped) | Enum | Requires that the selected cat has a specific item equipped. | 24 | `CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full`<br>`FaceCovering` |
| [`counter_maximum`](../Reference_and_Meta/Arrays.md#array-counter_maximum) | Array | Requires the value of a counter to be at most the specified number. | 19 | `[WorldEventLegacyCounter_CrackInTheWall 0]`<br>`[WorldEventLegacyCounter_CrackInTheWall 3]`<br>`[WorldEventLegacyCounter_FooCounter 10]` |
| [`is_not_chapter`](../Reference_and_Meta/Arrays.md#array-is_not_chapter) | Array | Requires that the current game chapter is not one of the specified chapters. | 16 | `[future theend]`<br>`[iceage jurassic]`<br>`[jurassic iceage]` |
| [`is_chapter`](../Reference_and_Meta/Arrays.md#array-is_chapter) | Array | Requires that the current game chapter is one of the specified chapters. | 8 | `[future theend]`<br>`[future]`<br>`[iceage jurassic]` |
| [`not_cat_has_item_equipped`](../Reference_and_Meta/Enums.md#enum-not_cat_has_item_equipped) | Enum | Requires that the selected cat does not have a specific item equipped. | 3 | `CryogenicTimeChamber_Full`<br>`GuillotinasHead`<br>`Horns` |
| `minimum_party_size` | Number | The minimum number of cats required in the party. | 2 | `2` |
| `not_on_quest` | Number | A quest ID that the party must not currently be on. | 2 | `1` |
| `cat_has_injury_count_min` | Number | Requires that the selected cat has at least the specified number of injuries. | 1 | `2` |
| [`cat_has_item_slot_equipped`](../Reference_and_Meta/Enums.md#enum-cat_has_item_slot_equipped) | Enum | Requires that the selected cat has an item equipped in the specified slot. | 1 | `weapon` |
| `cat_has_parasite` | Boolean | If true, requires that the selected cat has a parasite. | 1 | `true` |

</details>


---


### Object: `self_status_next_fight`


**Definition:** An object defining status effects applied to the unit at the start of the next fight.  
**Total Count:** 199

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`bad`](./Events_and_Encounters.md#object-bad), [`buy1`](./Events_and_Encounters.md#object-buy1), [`common`](./Events_and_Encounters.md#object-common), [`else`](./Events_and_Encounters.md#object-else), [`main`](./Events_and_Encounters.md#object-main), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 105 | passives<br>class<br>tag |
| `Fear` | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 13 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 13 | Default<br>FormChange<br>Druid |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 71 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`AbilityOnBattleStart_Immediate`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart_immediate) | Enum | Specifies the ability triggered instantly at the start of battle. | 17 | `BrambleRandomTileEvent`<br>`FlowerEventSleep`<br>`Flush` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 46 | `-1`<br>`-2`<br>`1` |
| `AddStartingMana` | Integer | The amount of bonus mana the unit starts each battle with. | 7 | `20`<br>`5` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| `CharismaUp` | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 16 | `-1`<br>`-2`<br>`1` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `1`<br>`10`<br>`2` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 19 | `1`<br>`2`<br>`[1 .1]` |
| `Blind` | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 43 | `-1`<br>`1`<br>`2` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `1`<br>`2`<br>`3` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 25 | `-1`<br>`1`<br>`2` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `NoHealthRegen` | Integer | Prevents the unit from regenerating health normally. | 7 | `1` |
| `Sleep` | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 35 | `1`<br>`2`<br>`3` |
| `Stun` | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |
| [`AbilityOnBattleStart`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart) | Enum | Casts the specified ability when the battle begins. | 15 | `Flush`<br>`Heathens`<br>`Heathens2` |
| `AddInitiative` | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 10 | `-10`<br>`-100`<br>`-20` |
| `AlphaTurns` | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 13 | `-1`<br>`1` |
| [`ChangeTileUnderCharacterAtStart`](../Reference_and_Meta/Enums.md#enum-changetileundercharacteratstart) | Enum | Specifies the tile type to change the tile under the character to at the start of battle. | 1 | `GlassTile` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| `Fights` | Integer | The number of fights this status or effect persists for. | 10 | `1`<br>`3`<br>`99` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |
| `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 45 | `1`<br>`2`<br>`3` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `10`<br>`15`<br>`20` |
| `NoManaRegen` | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 3 | `1` |
| `PermanentConfusion` | Integer | If set to 1, the unit is permanently confused and cannot be cured. | 3 | `1` |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. | 3 | `1` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `Rot` | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 20 | `-999999`<br>`1`<br>`2` |
| `Slow` | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 75 | `-1`<br>`1`<br>`2` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. | 10 | `1`<br>`2`<br>`4` |
| `Tarred` | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 17 | `1`<br>`2`<br>`[1 .1]` |
| `TempStrengthUp` | Integer | The number of stacks of temporary Strength Up applied to the unit. | 7 | `1`<br>`2`<br>`X` |

</details>


---


### Object: `permanent_stats`


**Definition:** Defines permanent stat changes to apply to the unit (e.g., con, cha).  
**Total Count:** 148

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`bad`](./Events_and_Encounters.md#object-bad), [`common`](./Events_and_Encounters.md#object-common), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 361 | `-1`<br>`-2`<br>`-3` |
| `random` | Number | A random value used for stat or attribute adjustment. | 302 | `-1`<br>`-2`<br>`1` |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 355 | `-1`<br>`-10`<br>`-2` |
| [`lck`](../Reference_and_Meta/Enums.md#enum-lck) | Enum / Integer | The Luck stat value or modifier. | 283 | `-1`<br>`-2`<br>`-3` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 332 | `-1`<br>`-10`<br>`-2` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer | The Strength stat value or modifier. | 335 | `-1`<br>`-2`<br>`-3` |
| `cha` | Integer | The Charisma stat value or modifier. | 337 | `+1`<br>`-1`<br>`-2` |
| [`dex`](../Reference_and_Meta/Enums.md#enum-dex) | Enum / Integer | The Dexterity stat value or modifier. | 250 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `conditional_reward`


**Definition:** An object defining a reward that is granted only if specified conditions are met.  
**Total Count:** 126

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#object-bad), [`common`](./Events_and_Encounters.md#object-common), [`else`](./Events_and_Encounters.md#object-else), [`good`](./Events_and_Encounters.md#object-good), [`rare`](./Events_and_Encounters.md#object-rare), [`setup`](./Events_and_Encounters.md#object-setup)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 174 | `common`<br>`rare`<br>`cha` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`reward`](../Reference_and_Meta/Miscellaneous.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 764 | `{ . . . }` |
| [`else`](../Reference_and_Meta/Miscellaneous.md#object-else) | Object  | Specifies the fallback outcome when the primary condition in a conditional reward is not met. | 38 | `{ . . . }` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |

</details>


---


### Object: `ignore`


**Definition:** An object defining the player action to ignore the event, including its stat check and outcomes.  
**Total Count:** 57

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 59 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 13 | `dimensionx`<br>`endoftime`<br>`future` |

</details>


---


### Object: `examine`


**Definition:** An object defining the player action to examine an object, including its stat check and outcomes.  
**Total Count:** 50

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 57 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 14 | `examine`<br>`lever`<br>`open` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `spawn_unit_next_fight`


**Definition:** An object defining a unit to spawn during the next fight, including its object, count, and spawn side.  
**Total Count:** 42

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#object-common), [`rare`](./Events_and_Encounters.md#object-rare), [`reward`](./Events_and_Encounters.md#object-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 1014 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 99 | `0`<br>`1`<br>`10` |
| [`spawn_side`](../Reference_and_Meta/Enums.md#enum-spawn_side) | Enum | Specifies which side the spawned unit appears on. Possible values: "cats", "enemies", or "anywhere". | 33 | `"cats"`<br>`anywhere`<br>`cats` |
| [`side`](../Reference_and_Meta/Enums.md#enum-side) | Enum | Determines the team the spawned unit belongs to. Possible values include "enemies". | 5 | `enemies` |

</details>


---


### Object: `get_item_from_pool`


**Definition:** Grants an item from the specified pool or a specific item name.  
**Total Count:** 349

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#object-common), [`rare`](./Events_and_Encounters.md#object-rare), [`reward`](./Events_and_Encounters.md#object-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 154 | `2`<br>`3`<br>`4` |
| [`restrict`](../Reference_and_Meta/Arrays.md#array-restrict) | Array | Limits the pool of items to specific categories such as weapon, armor, or consumables. | 45 | `[weapon armor]`<br>`[weapon consumables armor]`<br>`[weapon, trinket, armor]` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 32 | `common`<br>`rare`<br>`cha` |
| `prompt` | `String` | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |

</details>


---


### Object: `else`


**Definition:** Specifies the fallback outcome when the primary condition in a conditional reward is not met.  
**Total Count:** 38

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`conditional_reward`](./Events_and_Encounters.md#object-conditional_reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 31 | `common`<br>`rare`<br>`cha` |
| `prompt` | `String` | The text or localization key for the popup or prompt displayed to the player. | 2178 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `event_now_same_cat` | `String` | Specifies a world event that will now occur for the same cat category as the current event. | 100 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 59 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `party_damage` | `Number` | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 36 | `1`<br>`10`<br>`2` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1009 | `1`<br>`10`<br>`15` |
| `event_now` | `String` | Triggers the specified event immediately. | 25 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`conditional_reward`](../Reference_and_Meta/Miscellaneous.md#object-conditional_reward) | Object | An object defining a reward that is granted only if specified conditions are met. | 126 | `{ . . . }` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 90 | `[` |
| `get_item_from_pool` | `Array`  | Grants an item from the specified pool or a specific item name. | 349 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| `gain_disorder` | `String` | Specifies a disorder to add to the current cat when this event triggers. | 98 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `next_event_bonus` | `Number` | A modifier to the next event's outcome roll or selection chance. | 32 | `-1`<br>`-2`<br>`1` |
| [`random_mutation`](../Reference_and_Meta/Miscellaneous.md#object-random_mutation) | Object  | The number of random mutations applied to the unit. | 86 | `{ . . . }` |
| [`self_status_next_fight`](../Reference_and_Meta/Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 199 | `{ . . . }` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 38 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |

</details>


---


### Object: `leave`


**Definition:** An object defining the player action to leave or ignore the event, including its stat check and outcomes.  
**Total Count:** 41

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`main`](./Events_and_Encounters.md#object-main), [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 32 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `loot`


**Definition:** An object defining the player action to loot a container or corpse, including its stat check and outcomes.  
**Total Count:** 27

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 63 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |

</details>


---


### Object: `mutation`


**Definition:** An object defining specific body part mutations applied to the unit.  
**Total Count:** 31

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#object-common), [`good`](./Events_and_Encounters.md#object-good), [`rare`](./Events_and_Encounters.md#object-rare), [`spawn_reflection_next_fight`](./Events_and_Encounters.md#object-spawn_reflection_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `eyes` | Number | The ID for the eye mutation appearance. | 101 | `-1`<br>`-2`<br>`1029` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 316 | `-1`<br>`-2`<br>`1` |
| `ears` | Number | The ID for the ear mutation appearance. | 20 | `-1`<br>`-2`<br>`1500` |
| `eyebrows` | Number | The ID for the eyebrow mutation appearance. | 14 | `-1`<br>`-2`<br>`440` |
| [`head`](../Reference_and_Meta/Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 449 | `-1`<br>`1`<br>`1.3` |
| `legs` | Number | The ID or range of IDs for the leg mutation appearance. | 14 | `-1`<br>`306`<br>`322` |
| `arms` | Number | The ID or range of IDs for the arm mutation appearance. | 7 | `900`<br>`[10 20]` |
| `body` | Float | The catalog ID for the cat's body part. | 203 | `-1`<br>`1`<br>`1.1` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 219 | `-1`<br>`1000`<br>`1001` |
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 7 | `-1`<br>`-2`<br>`1013` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 202 | `-1`<br>`-2`<br>`1` |
| `ear1` | Integer | The catalog ID for the cat's first ear part. | 19 | `-2`<br>`1005`<br>`1013` |
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 3 | `-2`<br>`1069` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 194 | `-1`<br>`-2`<br>`1` |
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 5 | `-1`<br>`1013`<br>`1057` |

</details>


---


### Object: `party_status_next_fight`


**Definition:** An object defining status effects to apply to the party at the start of the next fight.  
**Total Count:** 26

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#object-common), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 22 | passives<br>class<br>tag |
| `Fear` | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`AbilityOnBattleStart_Immediate`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart_immediate) | Enum | Specifies the ability triggered instantly at the start of battle. | 17 | `BrambleRandomTileEvent`<br>`FlowerEventSleep`<br>`Flush` |
| `NoHealthRegen` | Integer | Prevents the unit from regenerating health normally. | 7 | `1` |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 50 | `1`<br>`2`<br>`4` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| `Immobile` | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 47 | `0`<br>`1`<br>`10%` |
| `Tangled` | Integer | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 10 | `1`<br>`2`<br>`[1, .05]` |
| `Tarred` | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 17 | `1`<br>`2`<br>`[1 .1]` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 19 | `1`<br>`2`<br>`[1 .1]` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `eat`


**Definition:** An object defining the player action to consume something, including its stat check and outcomes.  
**Total Count:** 27

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 66 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `setup`


**Definition:** Defines actions or checks to run before the main event logic, often setting up conditions or tokens.  
**Total Count:** 24

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#object-main)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`conditional_reward`](../Reference_and_Meta/Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 126 | `{ . . . }` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1009 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `cutscene`


**Definition:** Specifies the name of a cutscene to play.  
**Total Count:** 46

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#object-bad), [`good`](./Events_and_Encounters.md#object-good)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 22 | `common`<br>`rare`<br>`cha` |
| `cutscene` | `String` | Specifies the name of a cutscene to play. | 46 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| `skip_result_screen` | Boolean | If true, the result screen is skipped after the cutscene completes. | 22 | `true` |

</details>


---


### Object: `random_mutation_from_set`


**Definition:** Defines a set of mutation categories and their specific IDs to apply a random mutation from.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#object-common), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 316 | `-1`<br>`-2`<br>`1` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 99 | `0`<br>`1`<br>`10` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 219 | `-1`<br>`1000`<br>`1001` |
| `ears` | Number | The ID for the ear mutation appearance. | 20 | `-1`<br>`-2`<br>`1500` |
| `eyes` | Number | The ID for the eye mutation appearance. | 101 | `-1`<br>`-2`<br>`1029` |
| `legs` | Number | The ID or range of IDs for the leg mutation appearance. | 14 | `-1`<br>`306`<br>`322` |
| `body` | Float | The catalog ID for the cat's body part. | 203 | `-1`<br>`1`<br>`1.1` |
| `eyebrows` | Number | The ID for the eyebrow mutation appearance. | 14 | `-1`<br>`-2`<br>`440` |
| [`head`](../Reference_and_Meta/Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 449 | `-1`<br>`1`<br>`1.3` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 202 | `-1`<br>`-2`<br>`1` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 204 | `-1`<br>`-2`<br>`1` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 194 | `-1`<br>`-2`<br>`1` |
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 189 | `-1`<br>`1`<br>`10` |
| `texture` | Integer | The catalog ID for the cat's texture. | 223 | `-1`<br>`1`<br>`1000` |

</details>


---


### Object: `random_mutation`


**Definition:** The number of random mutations applied to the unit.  
**Total Count:** 86

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#object-common), [`else`](./Events_and_Encounters.md#object-else), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 99 | `0`<br>`1`<br>`10` |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 990 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| `asymmetric` | Boolean | If true, the mutation is applied asymmetrically (e.g., different on each side). | 10 | `false`<br>`true` |

</details>


---


### Object: `smash`


**Definition:** An object defining the player action to smash an object, including its stat check and outcomes.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 18 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 14 | `examine`<br>`lever`<br>`open` |

</details>


---


### Object: `destroy`


**Definition:** An object defining the player action to destroy an object, including its stat check and outcomes.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 22 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `bash`


**Definition:** An object defining the player action to bash open a container, including its stat check and outcomes.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 16 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |

</details>


---


### Object: `global_effect_next_fight`


**Definition:** Defines a global status effect or modifier to apply in the next fight.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#object-common), [`good`](./Events_and_Encounters.md#object-good), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 16 | passives<br>class<br>tag |
| `Fights` | Integer | The number of fights this status or effect persists for. | 10 | `1`<br>`3`<br>`99` |
| [`CharacterTypeGainsStatusAtBattleStart`](../Reference_and_Meta/Miscellaneous.md#object-charactertypegainsstatusatbattlestart) | Object | Defines status effects applied to characters with a specific tag at the start of a battle. | 8 | `{ . . . }` |
| [`StatusRandomEnemiesOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusrandomenemiesonbattlestart) | Object | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 7 | `{ . . . }` |
| [`KillEnemyOfTypeAtBattleStart`](../Reference_and_Meta/Miscellaneous.md#object-killenemyoftypeatbattlestart) | Object  | Specifies that a specific enemy type is killed at the start of the next battle. | 2 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `open`


**Definition:** An object defining the player action to open a container, including its stat check and outcomes.  
**Total Count:** 72

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Events_and_Encounters.md#object-root), [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 12 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 14 | `examine`<br>`lever`<br>`open` |

</details>


---


### Object: `sneak`


**Definition:** An object defining the player action to sneak past a threat, including its stat check and outcomes.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 32 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |

</details>


---


### Object: `leave_party_temporarily`


**Definition:** Defines parameters for a unit leaving the party temporarily, such as skipped fights and return conditions.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `fights_skipped` | Number | The number of fights the temporarily absent cat will skip before returning. | 9 | `0`<br>`1` |
| [`return_as`](../Reference_and_Meta/Enums.md#enum-return_as) | Enum | Specifies the role or faction the temporarily absent cat returns as. | 4 | `enemy` |
| [`return_during`](../Reference_and_Meta/Enums.md#enum-return_during) | Enum | Specifies the encounter type during which the temporarily absent cat returns. | 4 | `boss` |

</details>


---


### Object: `take`


**Definition:** An object defining the player action to take an item, including its stat check and outcomes.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 17 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `a`


**Definition:** An object defining the first custom option in a test or debug event.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `attack`


**Definition:** Specifies the primary attack ability for the class, either as a string name or a detailed object.  
**Total Count:** 883

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 12 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |

</details>


---


### Object: `b`


**Definition:** An object defining the second custom option in a test or debug event.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `c`


**Definition:** An object defining the third custom option in a test or debug event.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `charm`


**Definition:** Specifies the player character's attempt to charm or persuade the encounter.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 18 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |

</details>


---


### Object: `fight`


**Definition:** Specifies the player character's attempt to fight or force their way through the encounter.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 13 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |

</details>


---


### Object: `touch`


**Definition:** Specifies the player character's attempt to physically touch or interact with the encounter.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `activate_p`


**Definition:** Specifies the player character's attempt to activate the object (press a button/lever).  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `activate_z`


**Definition:** Specifies the player character's attempt to activate the object (pull a lever/switch).  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `d`


**Definition:** Specifies a debug or test option for game development purposes.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `enter`


**Definition:** Specifies the player character's attempt to enter or go inside the encounter location.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 10 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 13 | `dimensionx`<br>`endoftime`<br>`future` |

</details>


---


### Object: `inspect`


**Definition:** Specifies the player character's attempt to inspect or examine the encounter.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 6 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `lick`


**Definition:** Specifies the player character's attempt to lick the encounter.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 11 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |

</details>


---


### Object: `next_event_from_set`


**Definition:** Specifies the next event to trigger, or defines a set of events with count and category constraints.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#object-common), [`good`](./Events_and_Encounters.md#object-good), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`event`](../Reference_and_Meta/Enums.md#enum-event) | Enum | Specifies the event to force, either by name or by a nested object defining its type and level. | 15 | `Blessing`<br>`Death`<br>`Tragedy` |
| `same_cat` | Boolean | If true, the next event from the set uses the same cat as the previous event. | 6 | `true` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 99 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `CharacterTypeGainsStatusAtBattleStart`


**Definition:** Defines status effects applied to characters with a specific tag at the start of a battle.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#object-global_effect_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 990 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>tag |
| `Fear` | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| `Stun` | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `drink`


**Definition:** Specifies the player character's attempt to drink from or consume the encounter.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 13 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `kiss`


**Definition:** Specifies the player character's attempt to kiss the encounter.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 13 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `run`


**Definition:** Specifies the player character's attempt to run away or flee from the encounter.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 9 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `bite`


**Definition:** Specifies the player character's attempt to bite the encounter.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `damage`


**Definition:** Specifies the amount of damage dealt, can be a number or expression.  
**Total Count:** 1684

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `go_around`


**Definition:** Specifies the player character's attempt to go around or bypass the encounter.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 8 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `home`


**Definition:** Specifies the option to go home (exit to the main hub).  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 13 | `dimensionx`<br>`endoftime`<br>`future` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `outcome`


**Definition:** An object defining the possible outcomes of an event, typically containing a random pool or weighted lists of rewards and animations.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#object-main)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`play_animation`](../Reference_and_Meta/Arrays.md#array-play_animation) | Array / Enum | Specifies an animation to play, optionally as an array with a probability weight. | 179 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 90 | `[` |
| `add_weather` | `String` | Specifies a weather effect type to apply to the current map. | 67 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`weather_roll`](../Reference_and_Meta/Arrays.md#array-weather_roll) | Array | An array that defines weather roll parameters for an outcome. | 1 | `[` |

</details>


---


### Object: `party_permanent_stats_exclude_self`


**Definition:** An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`common`](./Events_and_Encounters.md#object-common), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 337 | `+1`<br>`-1`<br>`-2` |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 361 | `-1`<br>`-2`<br>`-3` |
| [`dex`](../Reference_and_Meta/Enums.md#enum-dex) | Enum / Integer | The Dexterity stat value or modifier. | 250 | `-1`<br>`-2`<br>`-3` |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 355 | `-1`<br>`-10`<br>`-2` |
| [`lck`](../Reference_and_Meta/Enums.md#enum-lck) | Enum / Integer | The Luck stat value or modifier. | 283 | `-1`<br>`-2`<br>`-3` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 332 | `-1`<br>`-10`<br>`-2` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer | The Strength stat value or modifier. | 335 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `past`


**Definition:** Specifies the option to travel to a past era (Ice Age, Jurassic, etc.).  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 13 | `dimensionx`<br>`endoftime`<br>`future` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `skip`


**Definition:** Specifies the option to skip or decline the current encounter.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 4 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `investigate`


**Definition:** Specifies the player character's attempt to investigate the encounter.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `party_permanent_stats`


**Definition:** An object defining permanent stat increases applied to the party.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#object-main), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 361 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `repell`


**Definition:** Specifies the player character's attempt to rappel down or climb into the encounter.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 8 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `spawn_reflection_next_fight`


**Definition:** The number of reflections to spawn in the next battle, optionally with a mutation.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusRandomEnemiesOnBattleStart`


**Definition:** An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#object-global_effect_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 99 | `0`<br>`1`<br>`10` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| `Fear` | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `attach_antenna`


**Definition:** Specifies the player character's attempt to attach a device or antenna to the encounter.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `boogers`


**Definition:** Specifies the player character's attempt to pick or examine boogers.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `copy`


**Definition:** Specifies the player character's attempt to copy or replicate something from the encounter.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `find_another_way`


**Definition:** Specifies the player character's attempt to find an alternative path around the encounter.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `gain_familiar`


**Definition:** Specifies which familiar type (by its class name) the unit gains.  
**Total Count:** 101

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `initial_health` | Integer | The starting health of the unit when spawned. | 12 | `1`<br>`10`<br>`14` |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1014 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `KillEnemyOfTypeAtBattleStart`


**Definition:** Specifies that a specific enemy type is killed at the start of the next battle.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#object-global_effect_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`enemy_type`](../Reference_and_Meta/Enums.md#enum-enemy_type) | Enum | Specifies the type of enemy to kill at the start of battle. | 2 | `any`<br>`cat` |
| [`fallback_spawn`](../Reference_and_Meta/Arrays.md#array-fallback_spawn) | Array | An array of enemy names to spawn as a fallback if no matching enemy type is present. | 1 | `[TomTom Kitten CatCaller Mangy]` |

</details>


---


### Object: `move_closer`


**Definition:** Specifies the player character's attempt to move closer to the encounter.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 4 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `party_random_mutation_from_set`


**Definition:** An object specifying the count and mutation parts to randomly apply to the party.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bad`](./Events_and_Encounters.md#object-bad), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 99 | `0`<br>`1`<br>`10` |
| `ears` | Number | The ID for the ear mutation appearance. | 20 | `-1`<br>`-2`<br>`1500` |
| `eyebrows` | Number | The ID for the eyebrow mutation appearance. | 14 | `-1`<br>`-2`<br>`440` |
| `eyes` | Number | The ID for the eye mutation appearance. | 101 | `-1`<br>`-2`<br>`1029` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 316 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `play`


**Definition:** Specifies the player character's attempt to play or interact playfully with the encounter.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 4 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `poop`


**Definition:** Defines a poop event or interaction, often part of a random encounter or response in dialogue.  
**Total Count:** 19

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `print`


**Definition:** Specifies the player character's attempt to print or output something from the encounter.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `protection`


**Definition:** Specifies the player character's attempt to offer or ask for protection.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `random_chance`


**Definition:** Defines a block with a percentage chance and an action to execute if the chance succeeds.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`reward`](./Events_and_Encounters.md#object-reward)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 101 | `.02`<br>`.1`<br>`.15` |
| `get_item_from_pool` | `String` | Grants an item from the specified pool or a specific item name. | 349 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |

</details>


---


### Object: `repair`


**Definition:** Specifies the player character's attempt to repair the encounter object.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |

</details>


---


### Object: `sacrifice`


**Definition:** Specifies the player character's attempt to make a sacrifice at the encounter.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `scale`


**Definition:** The scale multiplier applied to the unit's visual size.  
**Total Count:** 157

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `turnon`


**Definition:** Specifies the player character's attempt to turn on or activate the encounter.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `altar_sacrifice`


**Definition:** Specifies the player character's attempt to sacrifice a cat at the altar.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `arm`


**Definition:** Specifies the player character's attempt to put their arm inside the encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `attach_amplifier`


**Definition:** Specifies the player character's attempt to attach an amplifier to the encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `attach_leech`


**Definition:** Specifies the player character's attempt to attach a leech to the encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `bash_past_alt`


**Definition:** Specifies the player character's attempt to bash through the encounter (alternate version for specific chapters).  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `bite_it_off`


**Definition:** Specifies the player character's attempt to bite off part of the encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `blue`


**Definition:** Specifies the player character's attempt to choose the blue option.  
**Total Count:** 18

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 14 | `examine`<br>`lever`<br>`open` |
| `fixed_chance` | Number | A fixed percentage chance for a specific outcome or option to occur. | 4 | `50%` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `blue_needle`


**Definition:** Specifies the player character's attempt to take the blue needle.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `body`


**Definition:** The catalog ID for the cat's body part.  
**Total Count:** 203

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `book`


**Definition:** Specifies the player character's attempt to read or take the book.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `brace`


**Definition:** Specifies the player character's attempt to brace themselves for the encounter.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `break_ice`


**Definition:** Specifies the player character's attempt to break the ice covering the encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `break_lock`


**Definition:** Specifies the player character's attempt to break the lock on the encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `bribe`


**Definition:** Specifies the player character's attempt to bribe the encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `button`


**Definition:** Specifies the player character's attempt to push the button.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 14 | `examine`<br>`lever`<br>`open` |
| `fixed_chance` | Number | A fixed percentage chance for a specific outcome or option to occur. | 4 | `50%` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `buy1`


**Definition:** Specifies the player character's attempt to buy one of the offered items.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `catch`


**Definition:** An object defining a response option for catching an entity, including stat checks and rewards.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `challenge_to_game`


**Definition:** Specifies the player character's attempt to challenge the encounter to a game.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `chaos_ending`


**Definition:** Specifies the option to trigger the chaos ending cutscene.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `chapter_cutscene`


**Definition:** Specifies the option to trigger a chapter intro cutscene.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `charm_past_alt`


**Definition:** Specifies the player character's attempt to charm the encounter (alternate version for specific chapters).  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `climb`


**Definition:** Specifies the player character's attempt to climb over the encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `comfort`


**Definition:** A charisma-based event response that soothes the encounter subject.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `communicate`


**Definition:** A charisma-based event response to establish communication.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `concheck`


**Definition:** A constitution-based event response to test endurance.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `counter`


**Definition:** An event response that uses a countering action, with no stat requirement.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `crack_open`


**Definition:** A strength-based event response to break something open.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `cross`


**Definition:** An event response to traverse an obstacle, with no stat requirement.  
**Total Count:** 74

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `cut_wires`


**Definition:** An intelligence-based event response to disable wires.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `damage_1`


**Definition:** A constitution-based event response that deals minor damage.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `damage_full`


**Definition:** A constitution-based event response that deals full damage.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `damage_half`


**Definition:** A constitution-based event response that deals halved damage.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `desert_cutscene`


**Definition:** An event response that triggers a desert-themed cutscene, with no stat requirement.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `dexcheck`


**Definition:** A dexterity-based event response to test agility.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `dig`


**Definition:** A strength-based event response to excavate, limited by a token counter maximum.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `disarm`


**Definition:** A dexterity-based event response to remove a trap.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `dive`


**Definition:** A dexterity-based event response to plunge into water.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `donate`


**Definition:** An event response to give a donation, with no stat requirement but a coin cost.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `donate_10`


**Definition:** An event response to donate 10 coins.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `donate_15`


**Definition:** An event response to donate 15 coins.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `donate_20`


**Definition:** An event response to donate 20 coins.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `donate_5`


**Definition:** An event response to donate 5 coins.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `double`


**Definition:** An event response that doubles something, with no stat requirement.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `eat_meat`


**Definition:** A constitution-based event response to consume meat.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `enter_crater`


**Definition:** A luck-based event response to enter a crater.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `face`


**Definition:** The face equipment item assigned to the unit.  
**Total Count:** 228

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `fiddle`


**Definition:** A quest-based event response to tamper, requiring no specific quest token.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `fill_jar`


**Definition:** A quest-based event response to fill a jar, with no stat requirement.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `find`


**Definition:** An event response to search, with no stat requirement.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `fire`


**Definition:** An event response that uses fire, with no stat requirement.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `flush_yourself`


**Definition:** An event response to flush oneself, requiring a minimum counter value.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |

</details>


---


### Object: `follow`


**Definition:** A speed-based event response to pursue.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `free`


**Definition:** If true, this option requires no cost to activate.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `future`


**Definition:** Specifies the name, map flag, or connection for the Future area.  
**Total Count:** 30

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 13 | `dimensionx`<br>`endoftime`<br>`future` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `gain_clone_familiar`


**Definition:** An object that triggers the gaining of a clone familiar, with a specified object name.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`good`](./Events_and_Encounters.md#object-good)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1014 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `give_parasite`


**Definition:** An event response to give a parasite, requiring the cat to have a parasite.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |

</details>


---


### Object: `hack`


**Definition:** An intelligence-based event response to hack a system.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `head`


**Definition:** The catalog ID for the cat's head part.  
**Total Count:** 449

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `holy`


**Definition:** An event response that uses holy power, with no stat requirement.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `hp`


**Definition:** An event response that trades health, with no stat requirement.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `ice`


**Definition:** An event response that uses ice, with no stat requirement.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `infinite`


**Definition:** An event response to choose infinite, with a chapter exit hint and no stat requirement.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 13 | `dimensionx`<br>`endoftime`<br>`future` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `intcheck`


**Definition:** An intelligence-based event response to test intellect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `intimidation`


**Definition:** An event response that intimidates, with no stat requirement.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `itchies`


**Definition:** An event response that causes itches, with no stat requirement.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `join`


**Definition:** A charisma-based event response to join in.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `jump`


**Definition:** A speed-based event response to leap.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `jump_over`


**Definition:** A dexterity-based event response to vault over.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `keep_going`


**Definition:** An event response to persevere, with no stat requirement.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `kiss_meat`


**Definition:** A charisma-based event response to kiss meat.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `knife`


**Definition:** An event response to obtain a knife, with no stat requirement.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `leave_it_in`


**Definition:** An event response to leave an object in place, with no stat requirement.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `leg`


**Definition:** A luck-based event response to use a leg.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `lever`


**Definition:** An event response to pull a lever, with a fixed chance and no stat requirement.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `fixed_chance` | Number | A fixed percentage chance for a specific outcome or option to occur. | 4 | `50%` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `lick_alt`


**Definition:** A constitution-based event response to lick, restricted to specific chapters.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `lightning`


**Definition:** An event response using lightning, with no stat requirement.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `listen`


**Definition:** An intelligence-based event response to listen.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `looks`


**Definition:** The dialogue option for the Genie good event that selects the looks reward.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `loot_heart`


**Definition:** The dialogue option to take the heart from the Dead King as a quest action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `makeup`


**Definition:** The dialogue option for the makeup event, associated with the Tink2 encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `mind`


**Definition:** The dialogue option for the Genie bad event that selects the curse mind reward.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `neck`


**Definition:** The neck equipment item assigned to the unit.  
**Total Count:** 209

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `nothanks`


**Definition:** The generic decline dialogue option that triggers a leave animation.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `outsmart`


**Definition:** The dialogue option that uses the int stat to outsmart the tutorial encounter.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `patch_up`


**Definition:** The dialogue option that uses the int stat to patch up the dying fetus.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `pick_lock`


**Definition:** The dialogue option that uses the dex stat to pick a lock on a crate.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `pilfer`


**Definition:** The dialogue option that uses the lck stat to pilfer from a pile of skulls.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `pirouette`


**Definition:** The dialogue option for the Tink1 encounter that performs a pirouette.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `place_gristle`


**Definition:** The dialogue option to place gristle on the Wall of Flesh as a quest action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `power`


**Definition:** The dialogue option for the Genie good event that selects the power reward.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `pull`


**Definition:** The dialogue option that uses the str stat to pull a knife from a wall.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `pull_it_out`


**Definition:** The dialogue option to pull out a stalactite from the Jagged Pathway.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `pull_lever`


**Definition:** The dialogue option to pull the lever on the Odd Device.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `purify`


**Definition:** The dialogue option that uses the lck stat to purify the Mysterious Chamber.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `push_buttons`


**Definition:** The dialogue option to push buttons on the Odd Device.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `push_through`


**Definition:** The dialogue option that uses the str stat to push through the Jagged Pathway.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `put_in_coins`


**Definition:** The dialogue option to put coins into the Vending Machine, requiring a minimum of 10 coins.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `put_out_of_misery`


**Definition:** The dialogue option that uses the str stat to put the dying fetus out of its misery.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `reach_inside`


**Definition:** The dialogue option that uses the spd stat to reach inside a Small Black Hole.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `read`


**Definition:** The dialogue option that uses the int stat to read the Mysterious Manual.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `receive`


**Definition:** The dialogue option to receive an item from a legacy event.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `red`


**Definition:** Configuration for one of the dialog options (label 'EVENT_RED_ANSW'), with a fixed chance and associated animation, in a choice event.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `fixed_chance` | Number | A fixed percentage chance for a specific outcome or option to occur. | 4 | `50%` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `red_needle`


**Definition:** The dialogue option that uses the lck stat to select the red needle, requiring not having the RedNeedle token.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `reflect`


**Definition:** The dialogue option for the StacyMutant4 encounter that chooses to reflect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `remove`


**Definition:** The dialogue option that uses the str stat to remove a stuck corpse.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `remove_the_nail`


**Definition:** The dialogue option that uses the dex stat to remove the nail from a big toe.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `repair_quest`


**Definition:** The dialogue option to repair the broken time machine as a quest action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `rest`


**Definition:** The dialogue option that uses the lck stat to rest on a cat bed.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `revive`


**Definition:** The dialogue option that uses the lck stat to revive the Dead Mammoth.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `rub`


**Definition:** The dialogue option that uses the lck stat to rub the Genie Lamp.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `run_again`


**Definition:** The dialogue option that uses the spd stat to run away from Death again, requiring he hasn't chased you yet.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `run_away`


**Definition:** The dialogue option that uses the spd stat to run away from a Giant Sleeping Shark.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `sacrifice_full_favor`


**Definition:** The dialogue option to sacrifice a cat at the Volcano with full favor as a quest action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sacrifice_normal`


**Definition:** The dialogue option to perform a normal sacrifice at the Meat Altar, requiring the GuillotinasHead not equipped.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sacrifice_partial_favor`


**Definition:** The dialogue option to sacrifice a cat at the Volcano with partial favor as a quest action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `sacrifice_quest`


**Definition:** The dialogue option to perform a quest sacrifice at the Meat Altar, requiring the GuillotinasHead equipped.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `scream`


**Definition:** The dialogue option to scream at the Meat Golem with no stat requirement.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `shake`


**Definition:** The dialogue option that uses the str stat to shake the Vending Machine.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `slip_through`


**Definition:** The dialogue option that uses the dex stat to slip through a Barbed Wire Fence.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sneak_by`


**Definition:** The dialogue option that uses the dex stat to sneak by a Giant Sleeping Shark.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sneak_past_alt`


**Definition:** The dialogue option using dex to sneak past a stray cat, available only in the Ice Age or Jurassic chapters.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `soul`


**Definition:** The dialogue option for the Genie bad event that selects the curse soul reward.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `speed`


**Definition:** The speed of the projectile or move, can be a value or a range.  
**Total Count:** 475

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `surprise`


**Definition:** The dialogue option for the Butch2 encounter that surprises the target.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `sweet_talk`


**Definition:** The dialogue option that uses the cha stat to sweet-talk Death.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `swim`


**Definition:** The dialogue option that uses the str stat to swim through a Strong Current.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `tail`


**Definition:** The catalog ID for the cat's tail part.  
**Total Count:** 219

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `take_blood`


**Definition:** The dialogue option to drain blood from the Dead King as a quest action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `talk`


**Definition:** The dialogue option that uses the cha stat to talk to a Spookie Apparation.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `talk_to`


**Definition:** The dialogue option that uses the cha stat to talk to someone during a Dust Storm.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `tappytoes`


**Definition:** The dialogue option for the Tink1 encounter that performs a tappytoes action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `teleport`


**Definition:** Defines a dialogue option that transports the unit to an alternative location in the event.  
**Total Count:** 56

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `thorns`


**Definition:** Defines a dialogue option that applies a thorns effect to the unit.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `throw`


**Definition:** Defines a dialogue option that allows the unit to throw an object.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `timemachine`


**Definition:** Defines a dialogue option that triggers a time travel sequence.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `traverse`


**Definition:** Defines a dialogue option that moves the unit through a traversal area.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |

</details>


---


### Object: `upgrade_yourself`


**Definition:** Defines a dialogue option that upgrades the unit's attributes or abilities.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `use_item`


**Definition:** Defines a dialogue option that prompts the unit to use an item from their inventory.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `use_toilet_con`


**Definition:** Defines a dialogue option that interacts with a toilet using the Constitution stat.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `use_toilet_str`


**Definition:** Defines a dialogue option that interacts with a toilet using the Strength stat.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `use_weapon`


**Definition:** Defines a dialogue option that prompts the unit to use their equipped weapon.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |

</details>


---


### Object: `w1`


**Definition:** Defines a dialogue option for the first weather choice in the Crater Weather event.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w2`


**Definition:** Defines a dialogue option for the second weather choice in the Crater Weather event.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w3`


**Definition:** Defines a dialogue option for the third weather choice in the Crater Weather event.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w4`


**Definition:** Defines a dialogue option for the fourth weather choice in the Crater Weather event.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w5`


**Definition:** Defines a dialogue option for the fifth weather choice in the Crater Weather event.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `w6`


**Definition:** Defines a dialogue option for the sixth weather choice in the Crater Weather event.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wealth`


**Definition:** Defines a dialogue option that grants the unit money or valuable items.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wheezies`


**Definition:** Defines a dialogue option that triggers a wheezing effect or condition.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `wish_genes`


**Definition:** Defines a dialogue option in the Monkey Paw event that modifies the unit's genetics.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wish_items`


**Definition:** Defines a dialogue option in the Monkey Paw event that grants items.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wish_levelups`


**Definition:** Defines a dialogue option in the Monkey Paw event that grants level-ups.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `wish_strength`


**Definition:** Defines a dialogue option in the Monkey Paw event that increases Strength.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `withstand`


**Definition:** Defines a dialogue option that allows the unit to withstand a hazard using Constitution.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `yank_it_out`


**Definition:** Defines a dialogue option that yanks out an object using Strength.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `yellow_needle`


**Definition:** Defines a dialogue option to interact with a yellow needle.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`requirements`](../Reference_and_Meta/Miscellaneous.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 205 | `{ . . . }` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>


---


---


## Auto-Discovered Objects


### Object: `buy2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Assets_and_Localization/Strings.md#string-animation) | String | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `animation_fail` | String | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`good`](../Reference_and_Meta/Miscellaneous.md#object-good) | Object  | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `{ . . . }` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |

</details>


### Object: `buy3`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Assets_and_Localization/Strings.md#string-animation) | String | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `animation_fail` | String | Specifies the animation to play when an action fails. | 11 | `choice_no_coins` |
| [`bad`](../Reference_and_Meta/Miscellaneous.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 343 | `{ . . . }` |
| [`good`](../Reference_and_Meta/Miscellaneous.md#object-good) | Object  | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `{ . . . }` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 11 | `1`<br>`10`<br>`15` |

</details>


### Object: `pick`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Assets_and_Localization/Strings.md#string-animation) | String | Specifies the animation played when the ability is used. | 1815 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `copy_results` | String | Specifies the identifier of another option whose outcomes are replicated. | 14 | `examine`<br>`lever`<br>`open` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 574 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 550 | `cha`<br>`coins`<br>`con` |

</details>