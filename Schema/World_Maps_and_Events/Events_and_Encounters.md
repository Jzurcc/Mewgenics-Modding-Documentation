---
title: "Events & Encounters Schema"
description: "Dialogue encounters and choice nodes."
---

# Events & Encounters Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

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

> **Total Count:** 350

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 305 | `common`<br>`rare`<br>`cha` |
| [`intro`](./Events_and_Encounters.md#object-intro) | Object  | An object defining the introductory cutscene for the event, including title, cat selection, and visuals. | 214 | `{ . . . }` |
| [`main`](./Events_and_Encounters.md#object-main) | Object  | An object containing the primary prompt and options for an event. | 214 | `{ . . . }` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 101 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 88 | `1`<br>`10`<br>`15` |
| `weight` | Float | A multiplier or priority value for random selection or effect magnitude. | 63 | `.25`<br>`.5`<br>`1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 31 | `{ . . . }` |
| `get_item_from_pool` | String | Grants an item from the specified pool or a specific item name. | 27 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 12 | `{ . . . }` |
| [`rare`](../Reference_and_Meta/Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 9 | `1`<br>`10`<br>`15` |
| [`open`](./Events_and_Encounters.md#object-open) | Object  | An object defining the player action to open a container, including its stat check and outcomes. | 4 | `{ . . . }` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 3 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 3 | `cha`<br>`coins`<br>`con` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 | `false`<br>`true` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 3 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 3 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 3 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 3 | `1`<br>`10`<br>`15` |
| [`pick`](./Events_and_Encounters.md#object-pick) | Object  | An object defining the player action to pick or collect an object, including its stat check and outcomes. | 3 | `{ . . . }` |
| [`smash`](./Events_and_Encounters.md#object-smash) | Object  | An object defining the player action to smash an object, including its stat check and outcomes. | 2 | `{ . . . }` |
| [`destroy`](./Events_and_Encounters.md#object-destroy) | Object  | An object defining the player action to destroy an object, including its stat check and outcomes. | 2 | `{ . . . }` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 2 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 2 | `{ . . . }` |
| [`common`](../Reference_and_Meta/Enums.md#enum-common) | Enum  | Defines the common reward block for a boss encounter. | 1 | `100`<br>`14`<br>`5` |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 0 | `{ . . . }` |
| `lck` | Integer | The Luck stat value or modifier. | 0 | `-1`<br>`-2`<br>`-3` |
| `int` | Integer | The Intelligence stat value or modifier. | 0 | `-1`<br>`-10`<br>`-2` |
| `str` | Integer | The Strength stat value or modifier. | 0 | `-1`<br>`-2`<br>`-3` |
| `dex` | Integer | The Dexterity stat value or modifier. | 0 | `-1`<br>`-2`<br>`-3` |
| `cha` | Integer | The Charisma stat value or modifier. | 0 | `+1`<br>`-1`<br>`-2` |
| `spd` | Integer | The Speed stat value or modifier. | 0 | `-1`<br>`-10`<br>`-2` |
| `con` | Integer | The Constitution stat value or modifier. | 0 | `-1`<br>`-2`<br>`-3` |
| [`cutscene`](../Assets_and_Localization/Strings.md#string-cutscene) | String | Specifies the name of a cutscene to play. | 0 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| [`normal`](../Reference_and_Meta/Arrays.md#array-normal) | Array | An array or object defining the reward table for normal encounters, including coin ranges, food ranges, and loot chances. | 0 | `[` |
| [`battle`](../Assets_and_Localization/Strings.md#string-battle) | String | Defines a battle encounter by preset, level file path, or reverb settings. | 0 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 0 | `{ . . . }` |
| `complete_item_quest` | String | Marks the specified item quest as completed. | 0 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 3 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 3 | `cha`<br>`coins`<br>`con` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 633 | `common`<br>`rare`<br>`cha` |
| `prompt` | `String` | The text or localization key for the popup or prompt displayed to the player. | 619 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 151 | `1`<br>`10`<br>`15` |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 98 | `{ . . . }` |
| `get_item_from_pool` | `String` | Grants an item from the specified pool or a specific item name. | 78 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 46 | `{ . . . }` |
| [`damage`](./Events_and_Encounters.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 35 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 35 | `[` |
| `gain_coins` | `Array` | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 32 | `1`<br>`10`<br>`15` |
| `injury` | `String` | Specifies the type of injury applied, such as bleeding or stat reduction. | 28 | `bleeding`<br>`burned`<br>`cha` |
| `self_damage` | `Number` | Defines damage or effects applied to the caster when using the ability. | 26 | `1`<br>`10`<br>`100%` |
| `random_mutation` | `Number` | The number of random mutations applied to the unit. | 26 | `1`<br>`10`<br>`2` |
| `gain_disorder_from_pool` | `String` | Specifies a pool of disorders from which one is randomly gained. | 24 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| `play_animation` | `String` | Specifies an animation to play, optionally as an array with a probability weight. | 23 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| `event_now_same_cat` | `String` | Specifies a world event that will now occur for the same cat category as the current event. | 23 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| `gain_food` | `Number` | An array specifying the minimum and maximum amount of food gained, or a single integer. | 22 | `-5`<br>`20`<br>`30` |
| `gain_familiar` | `String` | Specifies which familiar type (by its class name) the unit gains. | 21 | `CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 19 | `{ . . . }` |
| `get_item` | `String` | Specifies an item to add to the player's inventory when this event triggers. | 16 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| `party_heal` | `Number` | The amount of health healed for the entire party. | 16 | `1`<br>`10`<br>`100%` |
| `party_damage` | `Number` | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 15 | `1`<br>`10`<br>`2` |
| `heal` | `Equation` | An equation string that determines the amount of health restored by this damage instance. | 13 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| `gain_disorder` | `String` | Specifies a disorder to add to the current cat when this event triggers. | 12 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| `clear_adventure_token` | `String` | Specifies an adventure token to clear (disable or mark as false) when this event triggers. | 12 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasTakenNeedle`<br>`AdventureToken_RedNeedle` |
| `get_parasite_from_pool` | `String` | Specifies the pool name or explicit list of parasites to obtain from. | 11 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 11 | `{ . . . }` |
| `full_heal` | `Number` | If set to 1, fully restores the unit's health. | 10 | `1` |
| `ally_ambush_next_fights` | `Number` | The number of upcoming fights that will start with an ally ambush. | 10 | `1`<br>`2` |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 9 | `{ . . . }` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 9 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `override_end_option_prompt` | `String` | Specifies a custom prompt string to display for the end option of this event choice. | 9 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| `ambush_next_basic_fights` | `Number` | The number of basic fights to trigger as ambushes. | 9 | `1` |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random_mutation_from_set) | Object  | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 8 | `{ . . . }` |
| `get_parasite` | `String` | Specifies a parasite item to attach to a unit when this event triggers. | 7 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `next_event_bonus` | `Number` | A modifier to the next event's outcome roll or selection chance. | 7 | `-1`<br>`-2`<br>`1` |
| `increment_legacy_counter` | `String` | Specifies a legacy counter to increment by one when this event triggers. | 6 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 6 | `{ . . . }` |
| `lose_item` | `String` | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 5 | `equipped`<br>`inventory`<br>`parasite` |
| `kill` | `String` | Kills the specified target type (e.g., 'cat'). | 5 | `cat` |
| `shop_now` | `String` | Triggers the specified shop to appear immediately. | 5 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| `add_weather` | `String` | Specifies a weather effect type to apply to the current map. | 4 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| `event_now` | `String` | Triggers the specified event immediately. | 3 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 2 | `{ . . . }` |
| `lose_specific_item` | `String` | Removes the specified item from the player's inventory. | 2 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| [`next_event_from_set`](./Events_and_Encounters.md#object-next_event_from_set) | Object  | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 2 | `{ . . . }` |
| `spin` | `String` | Specifies an action to re-roll or spin again, such as for a random reward wheel. | 2 | `again` |
| `party_heal_disorder` | `Number` | The number of disorders to heal from all party members. | 2 | `2` |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party_permanent_stats_exclude_self) | Object  | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 2 | `{ . . . }` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `heal_disorder` | `Number` | Specifies which disorder type to heal, or the number of disorders to heal. | 1 | `1`<br>`2`<br>`Anxiety` |
| `decrement_legacy_counter` | `String` | Specifies which legacy counter or token to decrement by one. | 1 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyToken_StartDigging` |
| `heal_injury` | `Number` | The number of injury points to heal on the target unit. | 1 | `1`<br>`5` |
| `learn_ability_from_pool` | `String` | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 1 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| `upgrade_ability` | `String` | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 1 | `random` |
| `get_and_equip_item` | `String` | Specifies the item to obtain and immediately equip. | 1 | `Catnip`<br>`FlyLarva` |
| `clear_result_animation` | `Number` | The number of result animations to clear or skip. | 1 | `1` |
| `self_heal` | `Number` | The amount of health the unit heals itself. | 1 | `10` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 625 | `common`<br>`rare`<br>`cha` |
| `prompt` | `String` | The text or localization key for the popup or prompt displayed to the player. | 614 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 179 | `1`<br>`10`<br>`15` |
| `get_item_from_pool` | `String` | Grants an item from the specified pool or a specific item name. | 130 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 86 | `{ . . . }` |
| `gain_disorder` | `String` | Specifies a disorder to add to the current cat when this event triggers. | 67 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| `injury` | `String` | Specifies the type of injury applied, such as bleeding or stat reduction. | 53 | `bleeding`<br>`burned`<br>`cha` |
| `gain_disorder_from_pool` | `String` | Specifies a pool of disorders from which one is randomly gained. | 51 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| `get_item` | `String` | Specifies an item to add to the player's inventory when this event triggers. | 49 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 40 | `{ . . . }` |
| `random_mutation` | `Number` | The number of random mutations applied to the unit. | 40 | `1`<br>`10`<br>`2` |
| `get_parasite` | `String` | Specifies a parasite item to attach to a unit when this event triggers. | 36 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `gain_familiar` | `String` | Specifies which familiar type (by its class name) the unit gains. | 33 | `CharmedBear`<br>`CharmedDaddyShark`<br>`CharmedDustDevil` |
| `event_now_same_cat` | `String` | Specifies a world event that will now occur for the same cat category as the current event. | 31 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 28 | `[` |
| `get_parasite_from_pool` | `String` | Specifies the pool name or explicit list of parasites to obtain from. | 25 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| [`conditional_reward`](../Reference_and_Meta/Miscellaneous.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 22 | `{ . . . }` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 21 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`damage`](./Events_and_Encounters.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 18 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 18 | `{ . . . }` |
| `gain_coins` | `Array` | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 17 | `1`<br>`10`<br>`15` |
| [`spawn_unit_next_fight`](./Events_and_Encounters.md#object-spawn_unit_next_fight) | Object  | An object defining a unit to spawn during the next fight, including its object, count, and spawn side. | 17 | `{ . . . }` |
| `next_event_bonus` | `Number` | A modifier to the next event's outcome roll or selection chance. | 14 | `-1`<br>`-2`<br>`1` |
| `self_damage` | `Number` | Defines damage or effects applied to the caster when using the ability. | 13 | `1`<br>`10`<br>`100%` |
| [`random_mutation_from_set`](./Events_and_Encounters.md#object-random_mutation_from_set) | Object  | Defines a set of mutation categories and their specific IDs to apply a random mutation from. | 13 | `{ . . . }` |
| `play_animation` | `Array` | Specifies an animation to play, optionally as an array with a probability weight. | 12 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`party_status_next_fight`](./Events_and_Encounters.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 12 | `{ . . . }` |
| `party_heal` | `Number` | The amount of health healed for the entire party. | 11 | `1`<br>`10`<br>`100%` |
| `party_damage` | `Number` | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 10 | `1`<br>`10`<br>`2` |
| `learn_passive` | `String` | Teaches the unit the specified passive ability. | 10 | `Blessed`<br>`CobraStyle`<br>`DeathProof` |
| `increment_legacy_counter` | `String` | Specifies a legacy counter to increment by one when this event triggers. | 9 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| `battle` | `String` | Defines a battle encounter by preset, level file path, or reverb settings. | 9 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| `party_random_mutation` | `Number` | The number of random mutations applied to the entire party. | 8 | `1` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 7 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `gain_food` | `Array` | An array specifying the minimum and maximum amount of food gained, or a single integer. | 7 | `-5`<br>`20`<br>`30` |
| `ambush_next_basic_fights` | `Number` | The number of basic fights to trigger as ambushes. | 7 | `1` |
| `lose_item` | `String` | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 7 | `equipped`<br>`inventory`<br>`parasite` |
| [`leave_party_temporarily`](./Events_and_Encounters.md#object-leave_party_temporarily) | Object  | Defines parameters for a unit leaving the party temporarily, such as skipped fights and return conditions. | 7 | `{ . . . }` |
| `shop_now` | `String` | Triggers the specified shop to appear immediately. | 6 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| `hide_appearance_changes` | `Number` | If set to 1, visual appearance changes from status effects or mutations are not shown on the unit. | 6 | `1` |
| `override_end_option_prompt` | `String` | Specifies a custom prompt string to display for the end option of this event choice. | 5 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| `ally_ambush_next_fights` | `Number` | The number of upcoming fights that will start with an ally ambush. | 5 | `1`<br>`2` |
| `decrement_legacy_counter` | `String` | Specifies which legacy counter or token to decrement by one. | 5 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyToken_StartDigging` |
| `add_weather` | `String` | Specifies a weather effect type to apply to the current map. | 4 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| `full_heal` | `Number` | If set to 1, fully restores the unit's health. | 4 | `1` |
| `learn_ability` | `String` | Specifies which specific ability the target unit learns. | 4 | `BarfBall`<br>`FutureSight` |
| `kill` | `String` | Kills the specified target type (e.g., 'cat'). | 3 | `cat` |
| `level_up` | `String` | Specifies which units to level up, such as 'all' or 'self'. | 3 | `all`<br>`self` |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 3 | `{ . . . }` |
| `next_event_from_set` | `String` | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 3 | `CatHole`<br>`Tragedy`<br>`WatchingHead2` |
| `gain_cat_familiar` | `Number` | The number of cat familiars gained. | 3 | `1` |
| `make_old` | `String` | Applies the 'old' status or age increase to the specified target, typically 'self'. | 3 | `self` |
| `spawn_reflection_next_fight` | `Number` | The number of reflections to spawn in the next battle, optionally with a mutation. | 3 | `1` |
| `lose_item_from_inventory` | `String` | Specifies which item or item category is removed from the unit's inventory. | 3 | `cat` |
| `event_now` | `String` | Triggers the specified event immediately. | 2 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| `lose_specific_item` | `String` | Removes the specified item from the player's inventory. | 2 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| `upgrade_ability` | `String` | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 2 | `random` |
| `party_heal_disorder` | `Number` | The number of disorders to heal from all party members. | 2 | `2` |
| `upgrade_passive` | `String` | Specifies which passive ability to upgrade, or 'random' for a random choice. | 2 | `random` |
| [`party_permanent_stats_exclude_self`](./Events_and_Encounters.md#object-party_permanent_stats_exclude_self) | Object  | An object specifying permanent stat bonuses (str, dex, con, int, spd) applied to all party members except the triggering unit. | 2 | `{ . . . }` |
| `party_heal_injury` | `Number` | The amount of injury to heal for the entire party. | 2 | `99` |
| `set_age` | `Number` | The age value to set for the target unit. | 2 | `1` |
| `trigger_adventure_unlock` | `String` | Triggers the specified adventure or map unlock quest. | 1 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| `heal_disorder` | `Number` | Specifies which disorder type to heal, or the number of disorders to heal. | 1 | `1`<br>`2`<br>`Anxiety` |
| `learn_ability_from_pool` | `String` | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 1 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| `learn_passive_from_pool` | `String` | An array specifying a pool or list of passives from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked passive. | 1 | `AnyUnlocked`<br>`Necromancer`<br>`[MiniMe SkillShare]` |
| `gain_immortal_familiar` | `String` | Specifies the immortal familiar to add to the party. | 1 | `CharmedFlea`<br>`CharmedFleaSpecial`<br>`CharmedPooter` |
| `get_and_equip_item` | `String` | Specifies the item to obtain and immediately equip. | 1 | `Catnip`<br>`FlyLarva` |
| `party_injury` | `String` | Specifies the type of injury to inflict on the party (e.g., 'random'). | 1 | `random` |
| [`party_permanent_stats`](./Events_and_Encounters.md#object-party_permanent_stats) | Object  | An object defining permanent stat increases applied to the party. | 1 | `{ . . . }` |
| `scramble_abilities` | `String` | Specifies which abilities to randomize, such as 'all'. | 1 | `all` |
| `ambush` | `String` | Specifies the path to a level file for an ambush encounter. | 1 | `"events/chupacabra.lvl"`<br>`putalevelhere.lvl` |
| `clear_result_animation` | `Number` | The number of result animations to clear or skip. | 1 | `1` |
| `lose_all_equipped_items` | `String` | Specifies the target (e.g., 'cat') from which to remove all currently equipped items. | 1 | `cat` |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party_random_mutation_from_set) | Object  | An object specifying the count and mutation parts to randomly apply to the party. | 1 | `{ . . . }` |
| `scramble_basic_attack` | `String` | Specifies which basic attacks to randomize or scramble. | 1 | `all` |
| `play_result_animation` | `String` | Specifies which result animation to play (e.g., 'resultVeryGood'). | 1 | `resultVeryGood` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 7 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 7 | `cha`<br>`coins`<br>`con` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 757 | `common`<br>`rare`<br>`cha` |
| [`common`](../Reference_and_Meta/Enums.md#enum-common) | Enum  | Defines the common reward block for a boss encounter. | 633 | `100`<br>`14`<br>`5` |
| [`rare`](../Reference_and_Meta/Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 602 | `1`<br>`10`<br>`15` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 82 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 55 | `1`<br>`10`<br>`15` |
| `get_item_from_pool` | String | Grants an item from the specified pool or a specific item name. | 36 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| `clear_adventure_token` | String | Specifies an adventure token to clear (disable or mark as false) when this event triggers. | 24 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasTakenNeedle`<br>`AdventureToken_RedNeedle` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 9 | `[` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 9 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `set_subject` | `String` | Specifies which subject or frame to use for the event's visual. | 9 | `dimensionx_head2`<br>`endorb2`<br>`monkey_paw_1finger` |
| `injury` | String | Specifies the type of injury applied, such as bleeding or stat reduction. | 5 | `bleeding`<br>`burned`<br>`cha` |
| `next_event_bonus` | Number | A modifier to the next event's outcome roll or selection chance. | 5 | `-1`<br>`-2`<br>`1` |
| `trigger_adventure_unlock` | `String` | Triggers the specified adventure or map unlock quest. | 5 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| [`play_animation`](../Reference_and_Meta/Arrays.md#array-play_animation) | Array | Specifies an animation to play, optionally as an array with a probability weight. | 4 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| `gain_disorder_from_pool` | String | Specifies a pool of disorders from which one is randomly gained. | 4 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| `cutscene_on_exit` | `String` | Determines which cutscene to play when the player leaves the current location. | 3 | `infinite_intro`<br>`king_intro` |
| [`gain_coins`](../Reference_and_Meta/Arrays.md#array-gain_coins) | Array | An array specifying the minimum and maximum amount of coins gained, or a single integer. | 2 | `1`<br>`10`<br>`15` |
| `event_now` | String | Triggers the specified event immediately. | 2 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| [`party_damage`](../Reference_and_Meta/Arrays.md#array-party_damage) | Array / Integer | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 1 | `1`<br>`10`<br>`2` |
| `get_parasite_from_pool` | String | Specifies the pool name or explicit list of parasites to obtain from. | 0 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| `ambush_next_basic_fights` | Number | The number of basic fights to trigger as ambushes. | 0 | `1` |
| `level_up` | String | Specifies which units to level up, such as 'all' or 'self'. | 0 | `all`<br>`self` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 546 | `common`<br>`rare`<br>`cha` |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 326 | `{ . . . }` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 289 | `1`<br>`10`<br>`15` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 197 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `play_animation` | String | Specifies an animation to play, optionally as an array with a probability weight. | 114 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| `increment_legacy_counter` | String | Specifies a legacy counter to increment by one when this event triggers. | 52 | `WorldEventLegacyCounter_CrackInTheWall`<br>`WorldEventLegacyCounter_CustomTokenString`<br>`WorldEventLegacyCounter_FooCounter` |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 35 | `{ . . . }` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 26 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `get_item_from_pool` | String | Grants an item from the specified pool or a specific item name. | 26 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| `get_item` | String | Specifies an item to add to the player's inventory when this event triggers. | 22 | `AlienBlaster`<br>`BagOfGrass`<br>`BearTrapMask` |
| `cutscene` | `String` | Specifies the name of a cutscene to play. | 19 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| `random_mutation` | Number | The number of random mutations applied to the unit. | 12 | `1`<br>`10`<br>`2` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 12 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `complete_item_quest` | `String` | Marks the specified item quest as completed. | 12 | `BlackShard`<br>`CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full` |
| `begin_chapter` | `String` | Specifies the chapter file to begin, transitioning to that chapter. | 12 | `dimensionx.gon`<br>`endoftime.gon`<br>`future.gon` |
| `event_now_same_cat` | String | Specifies a world event that will now occur for the same cat category as the current event. | 11 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| `gain_disorder` | String | Specifies a disorder to add to the current cat when this event triggers. | 10 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| `event_now` | String | Triggers the specified event immediately. | 10 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 9 | `[` |
| [`rare`](../Reference_and_Meta/Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 8 | `1`<br>`10`<br>`15` |
| `lose_specific_item` | String | Removes the specified item from the player's inventory. | 8 | `CryogenicTimeChamber_Full`<br>`PutridLeech`<br>`PyrophinasCollar` |
| `trigger_adventure_unlock` | `String` | Triggers the specified adventure or map unlock quest. | 7 | `end_of_time_unlock`<br>`legacy_event_unlock_momsknife`<br>`map_unlock_dimensionx` |
| `add_weather` | String | Specifies a weather effect type to apply to the current map. | 6 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`mutation`](./Events_and_Encounters.md#object-mutation) | Object  | An object defining specific body part mutations applied to the unit. | 5 | `{ . . . }` |
| `heal_disorder` | Number | Specifies which disorder type to heal, or the number of disorders to heal. | 5 | `1`<br>`2`<br>`Anxiety` |
| `injury` | String | Specifies the type of injury applied, such as bleeding or stat reduction. | 4 | `bleeding`<br>`burned`<br>`cha` |
| `level_up` | String | Specifies which units to level up, such as 'all' or 'self'. | 4 | `all`<br>`self` |
| [`random_pool_consider_luck`](../Reference_and_Meta/Arrays.md#array-random_pool_consider_luck) | Array | An array or weighted pool of rewards that are rolled considering the unit's luck stat. | 4 | `[` |
| `get_parasite` | String | Specifies a parasite item to attach to a unit when this event triggers. | 3 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `kill` | String | Kills the specified target type (e.g., 'cat'). | 3 | `cat` |
| `heal_injury` | `Number` | The number of injury points to heal on the target unit. | 3 | `1`<br>`5` |
| `unlock_item_quest` | `String` | Specifies the item whose quest is unlocked or advanced. | 3 | `CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full`<br>`JarOfChaos` |
| [`transform_item`](../Reference_and_Meta/Arrays.md#array-transform_item) | Array | An array specifying source and destination item IDs to transform one into the other. | 3 | `[JarOfRadiatedBlood JarOfChaos]`<br>`[JarOfRadiation JarOfRadiatedBlood]` |
| `gain_disorder_from_pool` | String | Specifies a pool of disorders from which one is randomly gained. | 2 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| [`override_end_option_prompt`](../Assets_and_Localization/Strings.md#string-override_end_option_prompt) | String | Specifies a custom prompt string to display for the end option of this event choice. | 2 | `"EVENT_LOCKEDDOOR_PROMPT1"`<br>`"EVENT_LOCKEDDOOR_PROMPT2"`<br>`"EVENT_MYSTERIOUSSTRANGER_END_AGAIN"` |
| `learn_ability_from_pool` | String | An array specifying a pool or list of abilities from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked ability. | 2 | `AnyUnlocked`<br>`Necromancer`<br>`[Smack Meow Hiss]` |
| `cutscene_on_exit` | String | Determines which cutscene to play when the player leaves the current location. | 2 | `infinite_intro`<br>`king_intro` |
| `learn_passive_from_pool` | String | An array specifying a pool or list of passives from which one is randomly selected and learned. The string 'AnyUnlocked' selects any unlocked passive. | 2 | `AnyUnlocked`<br>`Necromancer`<br>`[MiniMe SkillShare]` |
| [`party_gain_disorder_from_pool`](../Reference_and_Meta/Arrays.md#array-party_gain_disorder_from_pool) | Array | An array specifying the pool or list of disorders for the party to gain. | 2 | `[Dwarfism]`<br>`[Gigantism]`<br>`all_disorders` |
| `clear_surviving_kaiju` | `String` | Specifies which surviving kaiju to clear or remove. | 2 | `pyrophina`<br>`zaratana` |
| `heal` | `Equation` | An equation string that determines the amount of health restored by this damage instance. | 1 | `"ceil(X*item_aux/100)"`<br>`0`<br>`1` |
| `next_event_bonus` | Number | A modifier to the next event's outcome roll or selection chance. | 1 | `-1`<br>`-2`<br>`1` |
| `ally_ambush_next_fights` | Number | The number of upcoming fights that will start with an ally ambush. | 1 | `1`<br>`2` |
| `lose_item` | String | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 1 | `equipped`<br>`inventory`<br>`parasite` |
| `shop_now` | `String` | Triggers the specified shop to appear immediately. | 1 | `Event_RareShop`<br>`Event_SmallShop`<br>`Shop` |
| [`global_effect_next_fight`](./Events_and_Encounters.md#object-global_effect_next_fight) | Object  | Defines a global status effect or modifier to apply in the next fight. | 1 | `{ . . . }` |
| `next_event_from_set` | String | Specifies the next event to trigger, or defines a set of events with count and category constraints. | 1 | `CatHole`<br>`Tragedy`<br>`WatchingHead2` |
| `upgrade_ability` | `String` | Specifies which ability to upgrade. The value 'random' selects a random eligible ability. | 1 | `random` |
| `upgrade_passive` | `String` | Specifies which passive ability to upgrade, or 'random' for a random choice. | 1 | `random` |
| `get_full_item_set_from_pool` | `String` | Specifies the item pool rarity from which to generate a full set of items. | 1 | `common` |
| `scramble_abilities` | `String` | Specifies which abilities to randomize, such as 'all'. | 1 | `all` |
| `scramble_passives` | `String` | Specifies which passive abilities to randomize or scramble. | 1 | `all` |
| `clone_self_to_party` | `Number` | The number of clones of the unit added to the party. | 1 | `1` |
| `copy_items_to_party` | `Number` | The number of times the unit's items are copied to the party. | 1 | `1` |
| `copy_party_items` | `Number` | The number of times party items are copied to the unit. | 1 | `1` |
| [`gain_clone_familiar`](./Events_and_Encounters.md#object-gain_clone_familiar) | Object  | An object that triggers the gaining of a clone familiar, with a specified object name. | 1 | `{ . . . }` |
| `trigger_butterfly_effect` | `Number` | The number of times to trigger the butterfly effect event. | 1 | `1` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |

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
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 52 | `2`<br>`3`<br>`4` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 49 | `common`<br>`rare`<br>`cha` |
| [`restrict`](../Reference_and_Meta/Arrays.md#array-restrict) | Array | Limits the pool of items to specific categories such as weapon, armor, or consumables. | 39 | `[weapon armor]`<br>`[weapon consumables armor]`<br>`[weapon, trinket, armor]` |
| `prompt` | `String` | The text or localization key for the popup or prompt displayed to the player. | 1 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 310 | `common`<br>`rare`<br>`cha` |
| [`reward`](./Events_and_Encounters.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 307 | `{ . . . }` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 224 | `1`<br>`10`<br>`15` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 42 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `injury` | String | Specifies the type of injury applied, such as bleeding or stat reduction. | 10 | `bleeding`<br>`burned`<br>`cha` |
| `play_animation` | String | Specifies an animation to play, optionally as an array with a probability weight. | 10 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 9 | `{ . . . }` |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 7 | `{ . . . }` |
| `event_now_same_cat` | `String` | Specifies a world event that will now occur for the same cat category as the current event. | 7 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| `get_parasite` | `String` | Specifies a parasite item to attach to a unit when this event triggers. | 5 | `AlluringDoodie`<br>`BadSplinters`<br>`Beepis` |
| `gain_disorder_from_pool` | String | Specifies a pool of disorders from which one is randomly gained. | 4 | `Crazy_disorders`<br>`Steven_disorders`<br>`[BlackFetin OrangeFetin PurpleFetin]` |
| `battle` | `String` | Defines a battle encounter by preset, level file path, or reverb settings. | 4 | `"desert/boss/dustdevil/DustDevil.lvl"`<br>`"events/Death.lvl"`<br>`"events/GlowingBear"` |
| `kill` | `String` | Kills the specified target type (e.g., 'cat'). | 4 | `cat` |
| [`cutscene`](../Assets_and_Localization/Strings.md#string-cutscene) | String | Specifies the name of a cutscene to play. | 3 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| `get_parasite_from_pool` | String | Specifies the pool name or explicit list of parasites to obtain from. | 3 | `[AmoebaHat AmoebaNeck AmoebaFace]`<br>`barbed_armor`<br>`barbed_items` |
| `event_now` | String | Triggers the specified event immediately. | 3 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| `next_event_bonus` | Number | A modifier to the next event's outcome roll or selection chance. | 2 | `-1`<br>`-2`<br>`1` |
| [`permanent_stats`](./Events_and_Encounters.md#object-permanent_stats) | Object  | Defines permanent stat changes to apply to the unit (e.g., con, cha). | 1 | `{ . . . }` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `lose_item` | `String` | Specifies which item slot or type to lose (e.g., 'equipped', 'inventory'). | 1 | `equipped`<br>`inventory`<br>`parasite` |
| `gain_immortal_familiar` | `String` | Specifies the immortal familiar to add to the party. | 1 | `CharmedFlea`<br>`CharmedFleaSpecial`<br>`CharmedPooter` |
| [`party_random_mutation_from_set`](./Events_and_Encounters.md#object-party_random_mutation_from_set) | Object  | An object specifying the count and mutation parts to randomly apply to the party. | 1 | `{ . . . }` |
| `select_item_from_pool_for_cutscene_only` | `String` | Selects an item from a named pool for display in a cutscene without granting it. | 1 | `glitched_items` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |

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
| [`subject_frame`](../Reference_and_Meta/Enums.md#enum-subject_frame) | Enum | Specifies the specific art or visual frame used for the event's subject. | 214 | `a_beggar`<br>`a_few_coins`<br>`a_large_poop` |
| [`cat_choice`](../Reference_and_Meta/Enums.md#enum-cat_choice) | Enum | Determines how the cat is selected for an event, such as randomly. | 214 | `random` |
| [`event_clip`](../Reference_and_Meta/Enums.md#enum-event_clip) | Enum | Specifies the type of visual clip or animation used for the event frame. | 214 | `NonWheelEvent` |
| [`subject_clip`](../Reference_and_Meta/Enums.md#enum-subject_clip) | Enum | Specifies the type of visual clip used for the subject frame. | 214 | `EventSubject` |
| [`title`](../Assets_and_Localization/Strings.md#string-title) | String | The display title or name of the event. | 214 | `"Ability Pool Test"`<br>`"Blessing!"`<br>`"EVENT_ABEGGAR_NAME"` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 214 | `common`<br>`rare`<br>`cha` |
| [`choose_cat_with_item`](../Reference_and_Meta/Enums.md#enum-choose_cat_with_item) | Enum | Selects a cat that has a specific item equipped. | 17 | `CryogenicTimeChamber_Full`<br>`GuillotinasHead`<br>`PutridLeech` |
| `different_from_last_x_cats` | Number | The number of past events the chosen cat must differ from to avoid repeats. | 3 | `1`<br>`2`<br>`3` |
| `subject_frame_inner` | Number | An index for the inner frame variant of the subject art. | 3 | `2`<br>`4` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 1 | `1`<br>`10`<br>`15` |
| `choose_cat_with_min_health` | Number | Selects a cat with at least the specified percentage of health remaining. | 1 | `75%` |
| `choose_cat_with_highest_stat` | Equation | Selects the cat with the highest value of the specified stat. | 1 | `int` |
| [`choose_cat_with_item_slot_equipped`](../Reference_and_Meta/Enums.md#enum-choose_cat_with_item_slot_equipped) | Enum | Selects a cat that has an item equipped in the specified slot. | 1 | `weapon` |
| `choose_cat_with_most_injuries` | Boolean | If true, selects the cat with the highest number of injuries. | 1 | `true` |
| `choose_cat_with_parasite` | Boolean | If true, selects a cat that has a parasite. | 1 | `true` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 214 | `common`<br>`rare`<br>`cha` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 210 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| [`options`](../Reference_and_Meta/Arrays.md#array-options) | Array  | An array of named option objects within an event, each defining a possible action the player can take. | 210 | `[smash bash open]` |
| [`setup`](./Events_and_Encounters.md#object-setup) | Object  | Defines actions or checks to run before the main event logic, often setting up conditions or tokens. | 23 | `{ . . . }` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 11 | `{ . . . }` |
| `goto` | `String` | Determines which labeled point in the event's script to jump to next, controlling flow. | 4 | `end` |
| [`outcome`](./Events_and_Encounters.md#object-outcome) | Object  | An object defining the possible outcomes of an event, typically containing a random pool or weighted lists of rewards and animations. | 4 | `{ . . . }` |
| `max_options` | `Number` | The maximum number of event options presented to the player. | 3 | `2`<br>`3` |
| `shuffle_options` | `Boolean` | If true, randomizes the order of event options presented to the player. | 3 | `true` |
| [`open`](./Events_and_Encounters.md#object-open) | Object | An object defining the player action to open a container, including its stat check and outcomes. | 0 | `{ . . . }` |
| [`ignore`](./Events_and_Encounters.md#object-ignore) | Object | An object defining the player action to ignore the event, including its stat check and outcomes. | 0 | `{ . . . }` |
| [`examine`](./Events_and_Encounters.md#object-examine) | Object | An object defining the player action to examine an object, including its stat check and outcomes. | 0 | `{ . . . }` |
| [`leave`](./Events_and_Encounters.md#object-leave) | Object  | An object defining the player action to leave or ignore the event, including its stat check and outcomes. | 0 | `{ . . . }` |
| [`pick`](./Events_and_Encounters.md#object-pick) | Object | An object defining the player action to pick or collect an object, including its stat check and outcomes. | 0 | `{ . . . }` |
| [`buy2`](./Events_and_Encounters.md#object-buy2) | Object | Defines an event option that allows the player to buy an item for 10 coins. | 0 | `{ . . . }` |
| [`buy3`](./Events_and_Encounters.md#object-buy3) | Object | Defines an event option that allows the player to buy an item for 25 coins. | 0 | `{ . . . }` |

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
| [`ignore`](./Events_and_Encounters.md#object-ignore) | Object  | An object defining the player action to ignore the event, including its stat check and outcomes. | 47 | `{ . . . }` |
| [`examine`](./Events_and_Encounters.md#object-examine) | Object  | An object defining the player action to examine an object, including its stat check and outcomes. | 39 | `{ . . . }` |
| [`leave`](./Events_and_Encounters.md#object-leave) | Object  | An object defining the player action to leave or ignore the event, including its stat check and outcomes. | 24 | `{ . . . }` |
| [`loot`](./Events_and_Encounters.md#object-loot) | Object  | An object defining the player action to loot a container or corpse, including its stat check and outcomes. | 24 | `{ . . . }` |
| [`eat`](./Events_and_Encounters.md#object-eat) | Object  | An object defining the player action to consume something, including its stat check and outcomes. | 23 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 22 | `common`<br>`rare`<br>`cha` |
| [`smash`](./Events_and_Encounters.md#object-smash) | Object  | An object defining the player action to smash an object, including its stat check and outcomes. | 14 | `{ . . . }` |
| [`bash`](./Events_and_Encounters.md#object-bash) | Object  | An object defining the player action to bash open a container, including its stat check and outcomes. | 12 | `{ . . . }` |
| [`destroy`](./Events_and_Encounters.md#object-destroy) | Object  | An object defining the player action to destroy an object, including its stat check and outcomes. | 12 | `{ . . . }` |
| [`sneak`](./Events_and_Encounters.md#object-sneak) | Object  | An object defining the player action to sneak past a threat, including its stat check and outcomes. | 10 | `{ . . . }` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 7 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`open`](./Events_and_Encounters.md#object-open) | Object  | An object defining the player action to open a container, including its stat check and outcomes. | 7 | `{ . . . }` |
| [`take`](./Events_and_Encounters.md#object-take) | Object  | An object defining the player action to take an item, including its stat check and outcomes. | 7 | `{ . . . }` |
| [`charm`](./Events_and_Encounters.md#object-charm) | Object  | Specifies the player character's attempt to charm or persuade the encounter. | 7 | `{ . . . }` |
| [`a`](./Events_and_Encounters.md#object-a) | Object  | An object defining the first custom option in a test or debug event. | 7 | `{ . . . }` |
| [`b`](./Events_and_Encounters.md#object-b) | Object  | An object defining the second custom option in a test or debug event. | 7 | `{ . . . }` |
| [`c`](./Events_and_Encounters.md#object-c) | Object  | An object defining the third custom option in a test or debug event. | 7 | `{ . . . }` |
| [`touch`](./Events_and_Encounters.md#object-touch) | Object  | Specifies the player character's attempt to physically touch or interact with the encounter. | 7 | `{ . . . }` |
| [`enter`](./Events_and_Encounters.md#object-enter) | Object  | Specifies the player character's attempt to enter or go inside the encounter location. | 6 | `{ . . . }` |
| [`fight`](./Events_and_Encounters.md#object-fight) | Object  | Specifies the player character's attempt to fight or force their way through the encounter. | 6 | `{ . . . }` |
| [`lick`](./Events_and_Encounters.md#object-lick) | Object  | Specifies the player character's attempt to lick the encounter. | 6 | `{ . . . }` |
| [`activate_p`](./Events_and_Encounters.md#object-activate_p) | Object  | Specifies the player character's attempt to activate the object (press a button/lever). | 6 | `{ . . . }` |
| [`activate_z`](./Events_and_Encounters.md#object-activate_z) | Object  | Specifies the player character's attempt to activate the object (pull a lever/switch). | 6 | `{ . . . }` |
| [`d`](./Events_and_Encounters.md#object-d) | Object  | Specifies a debug or test option for game development purposes. | 6 | `{ . . . }` |
| [`inspect`](./Events_and_Encounters.md#object-inspect) | Object  | Specifies the player character's attempt to inspect or examine the encounter. | 6 | `{ . . . }` |
| [`run`](./Events_and_Encounters.md#object-run) | Object  | Specifies the player character's attempt to run away or flee from the encounter. | 5 | `{ . . . }` |
| [`drink`](./Events_and_Encounters.md#object-drink) | Object  | Specifies the player character's attempt to drink from or consume the encounter. | 5 | `{ . . . }` |
| [`kiss`](./Events_and_Encounters.md#object-kiss) | Object  | Specifies the player character's attempt to kiss the encounter. | 5 | `{ . . . }` |
| [`damage`](./Events_and_Encounters.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 4 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`home`](./Events_and_Encounters.md#object-home) | Object  | Specifies the option to go home (exit to the main hub). | 4 | `{ . . . }` |
| [`bite`](./Events_and_Encounters.md#object-bite) | Object  | Specifies the player character's attempt to bite the encounter. | 4 | `{ . . . }` |
| [`skip`](./Events_and_Encounters.md#object-skip) | Object  | Specifies the option to skip or decline the current encounter. | 4 | `{ . . . }` |
| [`go_around`](./Events_and_Encounters.md#object-go_around) | Object  | Specifies the player character's attempt to go around or bypass the encounter. | 4 | `{ . . . }` |
| [`past`](./Events_and_Encounters.md#object-past) | Object  | Specifies the option to travel to a past era (Ice Age, Jurassic, etc.). | 4 | `{ . . . }` |
| [`investigate`](./Events_and_Encounters.md#object-investigate) | Object  | Specifies the player character's attempt to investigate the encounter. | 3 | `{ . . . }` |
| [`repell`](./Events_and_Encounters.md#object-repell) | Object  | Specifies the player character's attempt to rappel down or climb into the encounter. | 3 | `{ . . . }` |
| `scale` | Float | The scale multiplier applied to the unit's visual size. | 2 | `.5`<br>`.6`<br>`.7` |
| [`poop`](./Events_and_Encounters.md#object-poop) | Object  | Defines a poop event or interaction, often part of a random encounter or response in dialogue. | 2 | `{ . . . }` |
| [`boogers`](./Events_and_Encounters.md#object-boogers) | Object  | Specifies the player character's attempt to pick or examine boogers. | 2 | `{ . . . }` |
| [`copy`](./Events_and_Encounters.md#object-copy) | Object  | Specifies the player character's attempt to copy or replicate something from the encounter. | 2 | `{ . . . }` |
| [`find_another_way`](./Events_and_Encounters.md#object-find_another_way) | Object  | Specifies the player character's attempt to find an alternative path around the encounter. | 2 | `{ . . . }` |
| [`move_closer`](./Events_and_Encounters.md#object-move_closer) | Object  | Specifies the player character's attempt to move closer to the encounter. | 2 | `{ . . . }` |
| [`play`](./Events_and_Encounters.md#object-play) | Object  | Specifies the player character's attempt to play or interact playfully with the encounter. | 2 | `{ . . . }` |
| [`print`](./Events_and_Encounters.md#object-print) | Object  | Specifies the player character's attempt to print or output something from the encounter. | 2 | `{ . . . }` |
| [`repair`](./Events_and_Encounters.md#object-repair) | Object  | Specifies the player character's attempt to repair the encounter object. | 2 | `{ . . . }` |
| [`sacrifice`](./Events_and_Encounters.md#object-sacrifice) | Object  | Specifies the player character's attempt to make a sacrifice at the encounter. | 2 | `{ . . . }` |
| `speed` | Array / Float  | The speed of the projectile or move, can be a value or a range. | 1 | `-30`<br>`-4`<br>`.5` |
| `head` | Float | The catalog ID for the cat's head part. | 1 | `-1`<br>`1`<br>`1.3` |
| [`face`](../Reference_and_Meta/Enums.md#enum-face) | Enum  | The face equipment item assigned to the unit. | 1 | `1004`<br>`1019`<br>`AtomicMark` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 1 | `-1`<br>`1000`<br>`1001` |
| [`neck`](../Reference_and_Meta/Enums.md#enum-neck) | Enum  | The neck equipment item assigned to the unit. | 1 | `AngelicAura`<br>`AngelicAura_Terminator`<br>`DruidNeck` |
| `body` | Float | The catalog ID for the cat's body part. | 1 | `-1`<br>`1`<br>`1.1` |
| [`cross`](./Events_and_Encounters.md#object-cross) | Object  | An event response to traverse an obstacle, with no stat requirement. | 1 | `{ . . . }` |
| [`teleport`](./Events_and_Encounters.md#object-teleport) | Object  | Defines a dialogue option that transports the unit to an alternative location in the event. | 1 | `{ . . . }` |
| [`future`](./Events_and_Encounters.md#object-future) | Object  | Specifies the name, map flag, or connection for the Future area. | 1 | `{ . . . }` |
| [`throw`](./Events_and_Encounters.md#object-throw) | Object  | Defines a dialogue option that allows the unit to throw an object. | 1 | `{ . . . }` |
| [`blue`](./Events_and_Encounters.md#object-blue) | Object  | Specifies the player character's attempt to choose the blue option. | 1 | `{ . . . }` |
| [`red`](./Events_and_Encounters.md#object-red) | Object  | Configuration for one of the dialog options (label 'EVENT_RED_ANSW'), with a fixed chance and associated animation, in a choice event. | 1 | `{ . . . }` |
| [`infinite`](./Events_and_Encounters.md#object-infinite) | Object  | An event response to choose infinite, with a chapter exit hint and no stat requirement. | 1 | `{ . . . }` |
| [`fire`](./Events_and_Encounters.md#object-fire) | Object  | An event response that uses fire, with no stat requirement. | 1 | `{ . . . }` |
| [`brace`](./Events_and_Encounters.md#object-brace) | Object  | Specifies the player character's attempt to brace themselves for the encounter. | 1 | `{ . . . }` |
| [`holy`](./Events_and_Encounters.md#object-holy) | Object  | An event response that uses holy power, with no stat requirement. | 1 | `{ . . . }` |
| [`scream`](./Events_and_Encounters.md#object-scream) | Object  | The dialogue option to scream at the Meat Golem with no stat requirement. | 1 | `{ . . . }` |
| [`ice`](./Events_and_Encounters.md#object-ice) | Object  | An event response that uses ice, with no stat requirement. | 1 | `{ . . . }` |
| [`receive`](./Events_and_Encounters.md#object-receive) | Object  | The dialogue option to receive an item from a legacy event. | 1 | `{ . . . }` |
| [`counter`](./Events_and_Encounters.md#object-counter) | Object  | An event response that uses a countering action, with no stat requirement. | 1 | `{ . . . }` |
| [`dig`](./Events_and_Encounters.md#object-dig) | Object  | A strength-based event response to excavate, limited by a token counter maximum. | 1 | `{ . . . }` |
| [`jump`](./Events_and_Encounters.md#object-jump) | Object  | A speed-based event response to leap. | 1 | `{ . . . }` |
| [`power`](./Events_and_Encounters.md#object-power) | Object  | The dialogue option for the Genie good event that selects the power reward. | 1 | `{ . . . }` |
| [`use_weapon`](./Events_and_Encounters.md#object-use_weapon) | Object  | Defines a dialogue option that prompts the unit to use their equipped weapon. | 1 | `{ . . . }` |
| [`attach_antenna`](./Events_and_Encounters.md#object-attach_antenna) | Object  | Specifies the player character's attempt to attach a device or antenna to the encounter. | 1 | `{ . . . }` |
| [`protection`](./Events_and_Encounters.md#object-protection) | Object  | Specifies the player character's attempt to offer or ask for protection. | 1 | `{ . . . }` |
| [`turnon`](./Events_and_Encounters.md#object-turnon) | Object  | Specifies the player character's attempt to turn on or activate the encounter. | 1 | `{ . . . }` |
| [`catch`](./Events_and_Encounters.md#object-catch) | Object  | An object defining a response option for catching an entity, including stat checks and rewards. | 1 | `{ . . . }` |
| [`free`](./Events_and_Encounters.md#object-free) | Object  | If true, this option requires no cost to activate. | 1 | `{ . . . }` |
| [`knife`](./Events_and_Encounters.md#object-knife) | Object  | An event response to obtain a knife, with no stat requirement. | 1 | `{ . . . }` |
| [`lever`](./Events_and_Encounters.md#object-lever) | Object  | An event response to pull a lever, with a fixed chance and no stat requirement. | 1 | `{ . . . }` |
| [`lightning`](./Events_and_Encounters.md#object-lightning) | Object  | An event response using lightning, with no stat requirement. | 1 | `{ . . . }` |
| [`run_away`](./Events_and_Encounters.md#object-run_away) | Object  | The dialogue option that uses the spd stat to run away from a Giant Sleeping Shark. | 1 | `{ . . . }` |
| [`thorns`](./Events_and_Encounters.md#object-thorns) | Object  | Defines a dialogue option that applies a thorns effect to the unit. | 1 | `{ . . . }` |
| [`altar_sacrifice`](./Events_and_Encounters.md#object-altar_sacrifice) | Object  | Specifies the player character's attempt to sacrifice a cat at the altar. | 1 | `{ . . . }` |
| [`arm`](./Events_and_Encounters.md#object-arm) | Object  | Specifies the player character's attempt to put their arm inside the encounter. | 1 | `{ . . . }` |
| [`attach_amplifier`](./Events_and_Encounters.md#object-attach_amplifier) | Object  | Specifies the player character's attempt to attach an amplifier to the encounter. | 1 | `{ . . . }` |
| [`attach_leech`](./Events_and_Encounters.md#object-attach_leech) | Object  | Specifies the player character's attempt to attach a leech to the encounter. | 1 | `{ . . . }` |
| [`bash_past_alt`](./Events_and_Encounters.md#object-bash_past_alt) | Object  | Specifies the player character's attempt to bash through the encounter (alternate version for specific chapters). | 1 | `{ . . . }` |
| [`bite_it_off`](./Events_and_Encounters.md#object-bite_it_off) | Object  | Specifies the player character's attempt to bite off part of the encounter. | 1 | `{ . . . }` |
| [`book`](./Events_and_Encounters.md#object-book) | Object  | Specifies the player character's attempt to read or take the book. | 1 | `{ . . . }` |
| [`break_ice`](./Events_and_Encounters.md#object-break_ice) | Object  | Specifies the player character's attempt to break the ice covering the encounter. | 1 | `{ . . . }` |
| [`break_lock`](./Events_and_Encounters.md#object-break_lock) | Object  | Specifies the player character's attempt to break the lock on the encounter. | 1 | `{ . . . }` |
| [`bribe`](./Events_and_Encounters.md#object-bribe) | Object  | Specifies the player character's attempt to bribe the encounter. | 1 | `{ . . . }` |
| [`button`](./Events_and_Encounters.md#object-button) | Object  | Specifies the player character's attempt to push the button. | 1 | `{ . . . }` |
| [`buy1`](./Events_and_Encounters.md#object-buy1) | Object  | Specifies the player character's attempt to buy one of the offered items. | 1 | `{ . . . }` |
| [`challenge_to_game`](./Events_and_Encounters.md#object-challenge_to_game) | Object  | Specifies the player character's attempt to challenge the encounter to a game. | 1 | `{ . . . }` |
| [`chaos_ending`](./Events_and_Encounters.md#object-chaos_ending) | Object  | Specifies the option to trigger the chaos ending cutscene. | 1 | `{ . . . }` |
| [`chapter_cutscene`](./Events_and_Encounters.md#object-chapter_cutscene) | Object  | Specifies the option to trigger a chapter intro cutscene. | 1 | `{ . . . }` |
| [`charm_past_alt`](./Events_and_Encounters.md#object-charm_past_alt) | Object  | Specifies the player character's attempt to charm the encounter (alternate version for specific chapters). | 1 | `{ . . . }` |
| [`climb`](./Events_and_Encounters.md#object-climb) | Object  | Specifies the player character's attempt to climb over the encounter. | 1 | `{ . . . }` |
| [`comfort`](./Events_and_Encounters.md#object-comfort) | Object  | A charisma-based event response that soothes the encounter subject. | 1 | `{ . . . }` |
| [`communicate`](./Events_and_Encounters.md#object-communicate) | Object  | A charisma-based event response to establish communication. | 1 | `{ . . . }` |
| [`concheck`](./Events_and_Encounters.md#object-concheck) | Object  | A constitution-based event response to test endurance. | 1 | `{ . . . }` |
| [`cut_wires`](./Events_and_Encounters.md#object-cut_wires) | Object  | An intelligence-based event response to disable wires. | 1 | `{ . . . }` |
| [`damage_1`](./Events_and_Encounters.md#object-damage_1) | Object  | A constitution-based event response that deals minor damage. | 1 | `{ . . . }` |
| [`damage_full`](./Events_and_Encounters.md#object-damage_full) | Object  | A constitution-based event response that deals full damage. | 1 | `{ . . . }` |
| [`damage_half`](./Events_and_Encounters.md#object-damage_half) | Object  | A constitution-based event response that deals halved damage. | 1 | `{ . . . }` |
| [`desert_cutscene`](./Events_and_Encounters.md#object-desert_cutscene) | Object  | An event response that triggers a desert-themed cutscene, with no stat requirement. | 1 | `{ . . . }` |
| [`dexcheck`](./Events_and_Encounters.md#object-dexcheck) | Object  | A dexterity-based event response to test agility. | 1 | `{ . . . }` |
| [`disarm`](./Events_and_Encounters.md#object-disarm) | Object  | A dexterity-based event response to remove a trap. | 1 | `{ . . . }` |
| [`dive`](./Events_and_Encounters.md#object-dive) | Object  | A dexterity-based event response to plunge into water. | 1 | `{ . . . }` |
| [`donate`](./Events_and_Encounters.md#object-donate) | Object  | An event response to give a donation, with no stat requirement but a coin cost. | 1 | `{ . . . }` |
| [`donate_5`](./Events_and_Encounters.md#object-donate_5) | Object  | An event response to donate 5 coins. | 1 | `{ . . . }` |
| [`double`](./Events_and_Encounters.md#object-double) | Object  | An event response that doubles something, with no stat requirement. | 1 | `{ . . . }` |
| [`eat_meat`](./Events_and_Encounters.md#object-eat_meat) | Object  | A constitution-based event response to consume meat. | 1 | `{ . . . }` |
| [`enter_crater`](./Events_and_Encounters.md#object-enter_crater) | Object  | A luck-based event response to enter a crater. | 1 | `{ . . . }` |
| [`fiddle`](./Events_and_Encounters.md#object-fiddle) | Object  | A quest-based event response to tamper, requiring no specific quest token. | 1 | `{ . . . }` |
| [`fill_jar`](./Events_and_Encounters.md#object-fill_jar) | Object  | A quest-based event response to fill a jar, with no stat requirement. | 1 | `{ . . . }` |
| [`find`](./Events_and_Encounters.md#object-find) | Object  | An event response to search, with no stat requirement. | 1 | `{ . . . }` |
| [`flush_yourself`](./Events_and_Encounters.md#object-flush_yourself) | Object  | An event response to flush oneself, requiring a minimum counter value. | 1 | `{ . . . }` |
| [`follow`](./Events_and_Encounters.md#object-follow) | Object  | A speed-based event response to pursue. | 1 | `{ . . . }` |
| [`give_parasite`](./Events_and_Encounters.md#object-give_parasite) | Object  | An event response to give a parasite, requiring the cat to have a parasite. | 1 | `{ . . . }` |
| [`hack`](./Events_and_Encounters.md#object-hack) | Object  | An intelligence-based event response to hack a system. | 1 | `{ . . . }` |
| [`hp`](./Events_and_Encounters.md#object-hp) | Object  | An event response that trades health, with no stat requirement. | 1 | `{ . . . }` |
| [`intcheck`](./Events_and_Encounters.md#object-intcheck) | Object  | An intelligence-based event response to test intellect. | 1 | `{ . . . }` |
| [`intimidation`](./Events_and_Encounters.md#object-intimidation) | Object  | An event response that intimidates, with no stat requirement. | 1 | `{ . . . }` |
| [`itchies`](./Events_and_Encounters.md#object-itchies) | Object  | An event response that causes itches, with no stat requirement. | 1 | `{ . . . }` |
| [`join`](./Events_and_Encounters.md#object-join) | Object  | A charisma-based event response to join in. | 1 | `{ . . . }` |
| [`jump_over`](./Events_and_Encounters.md#object-jump_over) | Object  | A dexterity-based event response to vault over. | 1 | `{ . . . }` |
| [`keep_going`](./Events_and_Encounters.md#object-keep_going) | Object  | An event response to persevere, with no stat requirement. | 1 | `{ . . . }` |
| [`kiss_meat`](./Events_and_Encounters.md#object-kiss_meat) | Object  | A charisma-based event response to kiss meat. | 1 | `{ . . . }` |
| [`leave_it_in`](./Events_and_Encounters.md#object-leave_it_in) | Object  | An event response to leave an object in place, with no stat requirement. | 1 | `{ . . . }` |
| [`leg`](./Events_and_Encounters.md#object-leg) | Object  | A luck-based event response to use a leg. | 1 | `{ . . . }` |
| [`lick_alt`](./Events_and_Encounters.md#object-lick_alt) | Object  | A constitution-based event response to lick, restricted to specific chapters. | 1 | `{ . . . }` |
| [`listen`](./Events_and_Encounters.md#object-listen) | Object  | An intelligence-based event response to listen. | 1 | `{ . . . }` |
| [`looks`](./Events_and_Encounters.md#object-looks) | Object  | The dialogue option for the Genie good event that selects the looks reward. | 1 | `{ . . . }` |
| [`loot_heart`](./Events_and_Encounters.md#object-loot_heart) | Object  | The dialogue option to take the heart from the Dead King as a quest action. | 1 | `{ . . . }` |
| [`makeup`](./Events_and_Encounters.md#object-makeup) | Object  | The dialogue option for the makeup event, associated with the Tink2 encounter. | 1 | `{ . . . }` |
| [`mind`](./Events_and_Encounters.md#object-mind) | Object  | The dialogue option for the Genie bad event that selects the curse mind reward. | 1 | `{ . . . }` |
| [`nothanks`](./Events_and_Encounters.md#object-nothanks) | Object  | The generic decline dialogue option that triggers a leave animation. | 1 | `{ . . . }` |
| [`outsmart`](./Events_and_Encounters.md#object-outsmart) | Object  | The dialogue option that uses the int stat to outsmart the tutorial encounter. | 1 | `{ . . . }` |
| [`patch_up`](./Events_and_Encounters.md#object-patch_up) | Object  | The dialogue option that uses the int stat to patch up the dying fetus. | 1 | `{ . . . }` |
| [`pick_lock`](./Events_and_Encounters.md#object-pick_lock) | Object  | The dialogue option that uses the dex stat to pick a lock on a crate. | 1 | `{ . . . }` |
| [`pirouette`](./Events_and_Encounters.md#object-pirouette) | Object  | The dialogue option for the Tink1 encounter that performs a pirouette. | 1 | `{ . . . }` |
| [`place_gristle`](./Events_and_Encounters.md#object-place_gristle) | Object  | The dialogue option to place gristle on the Wall of Flesh as a quest action. | 1 | `{ . . . }` |
| [`pull`](./Events_and_Encounters.md#object-pull) | Object  | The dialogue option that uses the str stat to pull a knife from a wall. | 1 | `{ . . . }` |
| [`pull_it_out`](./Events_and_Encounters.md#object-pull_it_out) | Object  | The dialogue option to pull out a stalactite from the Jagged Pathway. | 1 | `{ . . . }` |
| [`pull_lever`](./Events_and_Encounters.md#object-pull_lever) | Object  | The dialogue option to pull the lever on the Odd Device. | 1 | `{ . . . }` |
| [`purify`](./Events_and_Encounters.md#object-purify) | Object  | The dialogue option that uses the lck stat to purify the Mysterious Chamber. | 1 | `{ . . . }` |
| [`push_buttons`](./Events_and_Encounters.md#object-push_buttons) | Object  | The dialogue option to push buttons on the Odd Device. | 1 | `{ . . . }` |
| [`push_through`](./Events_and_Encounters.md#object-push_through) | Object  | The dialogue option that uses the str stat to push through the Jagged Pathway. | 1 | `{ . . . }` |
| [`put_in_coins`](./Events_and_Encounters.md#object-put_in_coins) | Object  | The dialogue option to put coins into the Vending Machine, requiring a minimum of 10 coins. | 1 | `{ . . . }` |
| [`put_out_of_misery`](./Events_and_Encounters.md#object-put_out_of_misery) | Object  | The dialogue option that uses the str stat to put the dying fetus out of its misery. | 1 | `{ . . . }` |
| [`reach_inside`](./Events_and_Encounters.md#object-reach_inside) | Object  | The dialogue option that uses the spd stat to reach inside a Small Black Hole. | 1 | `{ . . . }` |
| [`read`](./Events_and_Encounters.md#object-read) | Object  | The dialogue option that uses the int stat to read the Mysterious Manual. | 1 | `{ . . . }` |
| [`red_needle`](./Events_and_Encounters.md#object-red_needle) | Object  | The dialogue option that uses the lck stat to select the red needle, requiring not having the RedNeedle token. | 1 | `{ . . . }` |
| [`reflect`](./Events_and_Encounters.md#object-reflect) | Object  | The dialogue option for the StacyMutant4 encounter that chooses to reflect. | 1 | `{ . . . }` |
| [`remove`](./Events_and_Encounters.md#object-remove) | Object  | The dialogue option that uses the str stat to remove a stuck corpse. | 1 | `{ . . . }` |
| [`remove_the_nail`](./Events_and_Encounters.md#object-remove_the_nail) | Object  | The dialogue option that uses the dex stat to remove the nail from a big toe. | 1 | `{ . . . }` |
| [`repair_quest`](./Events_and_Encounters.md#object-repair_quest) | Object  | The dialogue option to repair the broken time machine as a quest action. | 1 | `{ . . . }` |
| [`rest`](./Events_and_Encounters.md#object-rest) | Object  | The dialogue option that uses the lck stat to rest on a cat bed. | 1 | `{ . . . }` |
| [`rub`](./Events_and_Encounters.md#object-rub) | Object  | The dialogue option that uses the lck stat to rub the Genie Lamp. | 1 | `{ . . . }` |
| [`run_again`](./Events_and_Encounters.md#object-run_again) | Object  | The dialogue option that uses the spd stat to run away from Death again, requiring he hasn't chased you yet. | 1 | `{ . . . }` |
| [`sacrifice_full_favor`](./Events_and_Encounters.md#object-sacrifice_full_favor) | Object  | The dialogue option to sacrifice a cat at the Volcano with full favor as a quest action. | 1 | `{ . . . }` |
| [`sacrifice_normal`](./Events_and_Encounters.md#object-sacrifice_normal) | Object  | The dialogue option to perform a normal sacrifice at the Meat Altar, requiring the GuillotinasHead not equipped. | 1 | `{ . . . }` |
| [`sacrifice_partial_favor`](./Events_and_Encounters.md#object-sacrifice_partial_favor) | Object  | The dialogue option to sacrifice a cat at the Volcano with partial favor as a quest action. | 1 | `{ . . . }` |
| [`sacrifice_quest`](./Events_and_Encounters.md#object-sacrifice_quest) | Object  | The dialogue option to perform a quest sacrifice at the Meat Altar, requiring the GuillotinasHead equipped. | 1 | `{ . . . }` |
| [`slip_through`](./Events_and_Encounters.md#object-slip_through) | Object  | The dialogue option that uses the dex stat to slip through a Barbed Wire Fence. | 1 | `{ . . . }` |
| [`sneak_by`](./Events_and_Encounters.md#object-sneak_by) | Object  | The dialogue option that uses the dex stat to sneak by a Giant Sleeping Shark. | 1 | `{ . . . }` |
| [`sneak_past_alt`](./Events_and_Encounters.md#object-sneak_past_alt) | Object  | The dialogue option using dex to sneak past a stray cat, available only in the Ice Age or Jurassic chapters. | 1 | `{ . . . }` |
| [`soul`](./Events_and_Encounters.md#object-soul) | Object  | The dialogue option for the Genie bad event that selects the curse soul reward. | 1 | `{ . . . }` |
| [`surprise`](./Events_and_Encounters.md#object-surprise) | Object  | The dialogue option for the Butch2 encounter that surprises the target. | 1 | `{ . . . }` |
| [`sweet_talk`](./Events_and_Encounters.md#object-sweet_talk) | Object  | The dialogue option that uses the cha stat to sweet-talk Death. | 1 | `{ . . . }` |
| [`swim`](./Events_and_Encounters.md#object-swim) | Object  | The dialogue option that uses the str stat to swim through a Strong Current. | 1 | `{ . . . }` |
| [`take_blood`](./Events_and_Encounters.md#object-take_blood) | Object  | The dialogue option to drain blood from the Dead King as a quest action. | 1 | `{ . . . }` |
| [`talk`](./Events_and_Encounters.md#object-talk) | Object  | The dialogue option that uses the cha stat to talk to a Spookie Apparation. | 1 | `{ . . . }` |
| [`talk_to`](./Events_and_Encounters.md#object-talk_to) | Object  | The dialogue option that uses the cha stat to talk to someone during a Dust Storm. | 1 | `{ . . . }` |
| [`tappytoes`](./Events_and_Encounters.md#object-tappytoes) | Object  | The dialogue option for the Tink1 encounter that performs a tappytoes action. | 1 | `{ . . . }` |
| [`timemachine`](./Events_and_Encounters.md#object-timemachine) | Object  | Defines a dialogue option that triggers a time travel sequence. | 1 | `{ . . . }` |
| [`traverse`](./Events_and_Encounters.md#object-traverse) | Object  | Defines a dialogue option that moves the unit through a traversal area. | 1 | `{ . . . }` |
| [`upgrade_yourself`](./Events_and_Encounters.md#object-upgrade_yourself) | Object  | Defines a dialogue option that upgrades the unit's attributes or abilities. | 1 | `{ . . . }` |
| [`use_item`](./Events_and_Encounters.md#object-use_item) | Object  | Defines a dialogue option that prompts the unit to use an item from their inventory. | 1 | `{ . . . }` |
| [`use_toilet_con`](./Events_and_Encounters.md#object-use_toilet_con) | Object  | Defines a dialogue option that interacts with a toilet using the Constitution stat. | 1 | `{ . . . }` |
| [`use_toilet_str`](./Events_and_Encounters.md#object-use_toilet_str) | Object  | Defines a dialogue option that interacts with a toilet using the Strength stat. | 1 | `{ . . . }` |
| [`w1`](./Events_and_Encounters.md#object-w1) | Object  | Defines a dialogue option for the first weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w2`](./Events_and_Encounters.md#object-w2) | Object  | Defines a dialogue option for the second weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w3`](./Events_and_Encounters.md#object-w3) | Object  | Defines a dialogue option for the third weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w4`](./Events_and_Encounters.md#object-w4) | Object  | Defines a dialogue option for the fourth weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w5`](./Events_and_Encounters.md#object-w5) | Object  | Defines a dialogue option for the fifth weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`w6`](./Events_and_Encounters.md#object-w6) | Object  | Defines a dialogue option for the sixth weather choice in the Crater Weather event. | 1 | `{ . . . }` |
| [`wealth`](./Events_and_Encounters.md#object-wealth) | Object  | Defines a dialogue option that grants the unit money or valuable items. | 1 | `{ . . . }` |
| [`wheezies`](./Events_and_Encounters.md#object-wheezies) | Object  | Defines a dialogue option that triggers a wheezing effect or condition. | 1 | `{ . . . }` |
| [`wish_genes`](./Events_and_Encounters.md#object-wish_genes) | Object  | Defines a dialogue option in the Monkey Paw event that modifies the unit's genetics. | 1 | `{ . . . }` |
| [`wish_items`](./Events_and_Encounters.md#object-wish_items) | Object  | Defines a dialogue option in the Monkey Paw event that grants items. | 1 | `{ . . . }` |
| [`wish_strength`](./Events_and_Encounters.md#object-wish_strength) | Object  | Defines a dialogue option in the Monkey Paw event that increases Strength. | 1 | `{ . . . }` |
| [`withstand`](./Events_and_Encounters.md#object-withstand) | Object  | Defines a dialogue option that allows the unit to withstand a hazard using Constitution. | 1 | `{ . . . }` |
| [`yank_it_out`](./Events_and_Encounters.md#object-yank_it_out) | Object  | Defines a dialogue option that yanks out an object using Strength. | 1 | `{ . . . }` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 0 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 0 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 0 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 0 | `cha`<br>`coins`<br>`con` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 0 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 0 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 0 | `1`<br>`10`<br>`15` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |
| [`revive`](./Events_and_Encounters.md#object-revive) | Object  | The dialogue option that uses the lck stat to revive the Dead Mammoth. | 0 | `{ . . . }` |
| [`shake`](./Events_and_Encounters.md#object-shake) | Object  | The dialogue option that uses the str stat to shake the Vending Machine. | 0 | `{ . . . }` |
| [`blue_needle`](./Events_and_Encounters.md#object-blue_needle) | Object  | Specifies the player character's attempt to take the blue needle. | 0 | `{ . . . }` |
| [`crack_open`](./Events_and_Encounters.md#object-crack_open) | Object  | A strength-based event response to break something open. | 0 | `{ . . . }` |
| [`donate_10`](./Events_and_Encounters.md#object-donate_10) | Object  | An event response to donate 10 coins. | 0 | `{ . . . }` |
| [`donate_15`](./Events_and_Encounters.md#object-donate_15) | Object  | An event response to donate 15 coins. | 0 | `{ . . . }` |
| [`donate_20`](./Events_and_Encounters.md#object-donate_20) | Object  | An event response to donate 20 coins. | 0 | `{ . . . }` |
| [`pilfer`](./Events_and_Encounters.md#object-pilfer) | Object  | The dialogue option that uses the lck stat to pilfer from a pile of skulls. | 0 | `{ . . . }` |
| [`wish_levelups`](./Events_and_Encounters.md#object-wish_levelups) | Object  | Defines a dialogue option in the Monkey Paw event that grants level-ups. | 0 | `{ . . . }` |
| [`yellow_needle`](./Events_and_Encounters.md#object-yellow_needle) | Object  | Defines a dialogue option to interact with a yellow needle. | 0 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |

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
| [`has_token`](../Reference_and_Meta/Enums.md#enum-has_token) | Enum | Requires the player to have a specific legacy token or flag. | 80 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| [`counter_range`](../Reference_and_Meta/Arrays.md#array-counter_range) | Array | Requires the value of a counter to fall within a specified inclusive range. | 37 | `[WorldEventLegacyCounter_CrackInTheWall 1 1]`<br>`[WorldEventLegacyCounter_CrackInTheWall 2 2]`<br>`[WorldEventLegacyCounter_CrackInTheWall 3 3]` |
| [`not_has_token`](../Reference_and_Meta/Enums.md#enum-not_has_token) | Enum | Requires that the player does not have a specific legacy token or flag. | 30 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_MysteriousJarRepeat` |
| [`counter_minimum`](../Reference_and_Meta/Arrays.md#array-counter_minimum) | Array | Requires the value of a counter to be at least the specified number. | 25 | `[WorldEventLegacyCounter_CrackInTheWall 4]`<br>`[WorldEventLegacyCounter_FooCounter 5]`<br>`[WorldEventLegacyCounter_Jack 100]` |
| [`cat_has_item_equipped`](../Reference_and_Meta/Enums.md#enum-cat_has_item_equipped) | Enum | Requires that the selected cat has a specific item equipped. | 22 | `CryogenicTimeChamber_Empty`<br>`CryogenicTimeChamber_Full`<br>`FaceCovering` |
| [`counter_maximum`](../Reference_and_Meta/Arrays.md#array-counter_maximum) | Array | Requires the value of a counter to be at most the specified number. | 18 | `[WorldEventLegacyCounter_CrackInTheWall 0]`<br>`[WorldEventLegacyCounter_CrackInTheWall 3]`<br>`[WorldEventLegacyCounter_FooCounter 10]` |
| [`is_not_chapter`](../Reference_and_Meta/Arrays.md#array-is_not_chapter) | Array | Requires that the current game chapter is not one of the specified chapters. | 16 | `[future theend]`<br>`[iceage jurassic]`<br>`[jurassic iceage]` |
| [`is_chapter`](../Reference_and_Meta/Arrays.md#array-is_chapter) | Array | Requires that the current game chapter is one of the specified chapters. | 8 | `[future theend]`<br>`[future]`<br>`[iceage jurassic]` |
| [`not_cat_has_item_equipped`](../Reference_and_Meta/Enums.md#enum-not_cat_has_item_equipped) | Enum | Requires that the selected cat does not have a specific item equipped. | 2 | `CryogenicTimeChamber_Full`<br>`GuillotinasHead`<br>`Horns` |
| `minimum_party_size` | Number | The minimum number of cats required in the party. | 2 | `2` |
| `not_on_quest` | Number | A quest ID that the party must not currently be on. | 2 | `1` |
| `cat_has_injury_count_min` | Number | Requires that the selected cat has at least the specified number of injuries. | 1 | `2` |
| [`cat_has_item_slot_equipped`](../Reference_and_Meta/Enums.md#enum-cat_has_item_slot_equipped) | Enum | Requires that the selected cat has an item equipped in the specified slot. | 1 | `weapon` |
| `cat_has_parasite` | Boolean | If true, requires that the selected cat has a parasite. | 1 | `true` |

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
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 115 | passives<br>class<br>tag |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 35 | `1`<br>`10`<br>`2` |
| `Fear` | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 32 | `1`<br>`10`<br>`2` |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 24 | `1`<br>`10`<br>`2` |
| [`AbilityOnBattleStart_Immediate`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart_immediate) | Enum | Specifies the ability triggered instantly at the start of battle. | 14 | `BrambleRandomTileEvent`<br>`FlowerEventSleep`<br>`Flush` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 7 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 7 | `-1`<br>`-2`<br>`-4` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 6 | `-1`<br>`-2`<br>`1` |
| `CharismaUp` | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 5 | `-1`<br>`-2`<br>`1` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 5 | `1`<br>`10`<br>`2` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 5 | `1`<br>`10`<br>`2` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 4 | `1`<br>`2`<br>`3` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 4 | `-1`<br>`1`<br>`2` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 4 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `Sleep` | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 4 | `1`<br>`2`<br>`3` |
| `Stun` | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`2`<br>`3` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 4 | `1`<br>`2`<br>`3` |
| `Blind` | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 4 | `-1`<br>`1`<br>`2` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`[1 .1]` |
| `AddStartingMana` | Integer | The amount of bonus mana the unit starts each battle with. | 3 | `20`<br>`5` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 3 | `-1`<br>`-2`<br>`-4` |
| `NoHealthRegen` | Integer | Prevents the unit from regenerating health normally. | 3 | `1` |
| `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 13 | Default<br>FormChange<br>Druid |
| `Slow` | Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | `-1`<br>`1`<br>`2` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 1 | `10`<br>`15`<br>`20` |
| `Rot` | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 1 | `-999999`<br>`1`<br>`2` |
| `Tarred` | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |
| [`AbilityOnBattleStart`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart) | Enum | Casts the specified ability when the battle begins. | 1 | `Flush`<br>`Heathens`<br>`Heathens2` |
| `AlphaTurns` | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 1 | `-1`<br>`1` |
| `AddInitiative` | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 1 | `-10`<br>`-100`<br>`-20` |
| `Fights` | Integer | The number of fights this status or effect persists for. | 1 | `1`<br>`3`<br>`99` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. | 1 | `1`<br>`2`<br>`4` |
| `TempStrengthUp` | Integer | The number of stacks of temporary Strength Up applied to the unit. | 1 | `1`<br>`2`<br>`X` |
| `NoManaRegen` | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 1 | `1` |
| `PermanentConfusion` | Integer | If set to 1, the unit is permanently confused and cannot be cured. | 1 | `1` |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. | 1 | `1` |
| [`ChangeTileUnderCharacterAtStart`](../Reference_and_Meta/Enums.md#enum-changetileundercharacteratstart) | Enum | Specifies the tile type to change the tile under the character to at the start of battle. | 1 | `GlassTile` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |

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
| `con` | Integer | The Constitution stat value or modifier. | 38 | `-1`<br>`-2`<br>`-3` |
| `random` | Number | A random value used for stat or attribute adjustment. | 26 | `-1`<br>`-2`<br>`1` |
| `int` | Integer | The Intelligence stat value or modifier. | 25 | `-1`<br>`-10`<br>`-2` |
| `str` | Integer | The Strength stat value or modifier. | 22 | `-1`<br>`-2`<br>`-3` |
| `lck` | Integer | The Luck stat value or modifier. | 21 | `-1`<br>`-2`<br>`-3` |
| `spd` | Integer | The Speed stat value or modifier. | 20 | `-1`<br>`-10`<br>`-2` |
| `cha` | Integer | The Charisma stat value or modifier. | 17 | `+1`<br>`-1`<br>`-2` |
| `dex` | Integer | The Dexterity stat value or modifier. | 14 | `-1`<br>`-2`<br>`-3` |

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
| [`reward`](./Events_and_Encounters.md#object-reward) | Object  | An object containing sub-objects defining the rewards for different rarity tiers (e.g., common, rare), each with their own set of actions and items. | 124 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 124 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 122 | `common`<br>`rare`<br>`cha` |
| [`else`](./Events_and_Encounters.md#object-else) | Object  | Specifies the fallback outcome when the primary condition in a conditional reward is not met. | 35 | `{ . . . }` |
| [`prompt`](../Assets_and_Localization/Strings.md#string-prompt) | String | The text or localization key for the popup or prompt displayed to the player. | 2 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |

</details>


---


### Object: `gain_familiar`


**Definition:** Specifies which familiar type (by its class name) the unit gains.  
**Total Count:** 101

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `initial_health` | Integer | The starting health of the unit when spawned. | 1 | `1`<br>`10`<br>`14` |

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
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 17 | `0`<br>`1`<br>`10` |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 12 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| `asymmetric` | Boolean | If true, the mutation is applied asymmetrically (e.g., different on each side). | 8 | `false`<br>`true` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 11 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 11 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 7 | `common`<br>`rare`<br>`cha` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 | `{ . . . }` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 4 | `examine`<br>`lever`<br>`open` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 57 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 57 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 56 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 55 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 49 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 3 | `{ . . . }` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 2 | `dimensionx`<br>`endoftime`<br>`future` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 44 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 44 | `cha`<br>`coins`<br>`con` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 41 | `false`<br>`true` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 38 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 28 | `{ . . . }` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 3 | `examine`<br>`lever`<br>`open` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 21 | `common`<br>`rare`<br>`cha` |
| `cutscene` | `String` | Specifies the name of a cutscene to play. | 21 | `"chaos_ending_bad"`<br>`"chaos_ending_good"`<br>`"chapterintros/bunker"` |
| `skip_result_screen` | Boolean | If true, the result screen is skipped after the cutscene completes. | 21 | `true` |

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
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 41 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 35 | `0`<br>`1`<br>`10` |
| [`spawn_side`](../Reference_and_Meta/Enums.md#enum-spawn_side) | Enum | Specifies which side the spawned unit appears on. Possible values: "cats", "enemies", or "anywhere". | 32 | `"cats"`<br>`anywhere`<br>`cats` |
| [`side`](../Reference_and_Meta/Enums.md#enum-side) | Enum | Determines the team the spawned unit belongs to. Possible values include "enemies". | 3 | `enemies` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 33 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 33 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 33 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 31 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 25 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 37 | `common`<br>`rare`<br>`cha` |
| `prompt` | `String` | The text or localization key for the popup or prompt displayed to the player. | 19 | `"Donate 3 times before you can receive a reward!"`<br>`"EVENT_ABEGGAR_LEAVE"`<br>`"EVENT_ABEGGAR_QUES"` |
| `event_now_same_cat` | `String` | Specifies a world event that will now occur for the same cat category as the current event. | 6 | `BigToe`<br>`Blessing`<br>`BodyOfGlorg_Gift` |
| `set_adventure_token` | `String` | Specifies an adventure token to set (enable or mark as true) when this event triggers. | 6 | `AdventureToken_BlueNeedle`<br>`AdventureToken_HasRunFromDeath`<br>`AdventureToken_HasTakenNeedle` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 5 | `1`<br>`10`<br>`15` |
| `party_damage` | `Number` | An array specifying the minimum and maximum damage dealt to the party, or a single integer or percentage. | 5 | `1`<br>`10`<br>`2` |
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional_reward) | Object | An object defining a reward that is granted only if specified conditions are met. | 4 | `{ . . . }` |
| `event_now` | `String` | Triggers the specified event immediately. | 4 | `MeatGolem`<br>`Mirage`<br>`MysteriousMachine_Bad` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 3 | `[` |
| `get_item_from_pool` | `Array`  | Grants an item from the specified pool or a specific item name. | 2 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| `gain_disorder` | `String` | Specifies a disorder to add to the current cat when this event triggers. | 2 | `AcidReflux`<br>`Albinism`<br>`Anxiety` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`self_status_next_fight`](./Events_and_Encounters.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 1 | `{ . . . }` |
| [`random_mutation`](./Events_and_Encounters.md#object-random_mutation) | Object  | The number of random mutations applied to the unit. | 1 | `{ . . . }` |
| `set_legacy_token` | `String` | Specifies a legacy token to set (enable or mark as true) when this event triggers. | 1 | `AlienOvergrowthUnlocked`<br>`AntennaQuest_Orb`<br>`AntennaQuest_Rift` |
| `next_event_bonus` | `Number` | A modifier to the next event's outcome roll or selection chance. | 1 | `-1`<br>`-2`<br>`1` |

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
| `eyes` | Number | The ID for the eye mutation appearance. | 12 | `-1`<br>`-2`<br>`1029` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 11 | `-1`<br>`-2`<br>`1` |
| `ears` | Number | The ID for the ear mutation appearance. | 10 | `-1`<br>`-2`<br>`1500` |
| `eyebrows` | Number | The ID for the eyebrow mutation appearance. | 8 | `-1`<br>`-2`<br>`440` |
| `head` | Float | The catalog ID for the cat's head part. | 7 | `-1`<br>`1`<br>`1.3` |
| `legs` | Number | The ID or range of IDs for the leg mutation appearance. | 7 | `-1`<br>`306`<br>`322` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 6 | `-1`<br>`1000`<br>`1001` |
| `body` | Float | The catalog ID for the cat's body part. | 6 | `-1`<br>`1`<br>`1.1` |
| `arms` | Number | The ID or range of IDs for the arm mutation appearance. | 6 | `900`<br>`[10 20]` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 4 | `-1`<br>`-2`<br>`1` |
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 3 | `-1`<br>`-2`<br>`1013` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 2 | `-1`<br>`-2`<br>`1` |
| `ear1` | Integer | The catalog ID for the cat's first ear part. | 2 | `-2`<br>`1005`<br>`1013` |
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 2 | `-2`<br>`1069` |
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 1 | `-1`<br>`1013`<br>`1057` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 1 | `dimensionx`<br>`endoftime`<br>`future` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 26 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 26 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 26 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 26 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 24 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 22 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 2 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 23 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 23 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 23 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 23 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 23 | `{ . . . }` |

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
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 23 | passives<br>class<br>tag |
| `Fear` | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 7 | `1`<br>`10`<br>`2` |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 6 | `1`<br>`10`<br>`2` |
| [`AbilityOnBattleStart_Immediate`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart_immediate) | Enum | Specifies the ability triggered instantly at the start of battle. | 3 | `BrambleRandomTileEvent`<br>`FlowerEventSleep`<br>`Flush` |
| `NoHealthRegen` | Integer | Prevents the unit from regenerating health normally. | 3 | `1` |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `Immobile` | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |
| `Tarred` | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |
| `Tangled` | Integer | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 1 | `1`<br>`2`<br>`[1, .05]` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

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
| [`conditional_reward`](./Events_and_Encounters.md#object-conditional_reward) | Object  | An object defining a reward that is granted only if specified conditions are met. | 42 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 23 | `common`<br>`rare`<br>`cha` |
| `set_frame` | `Number` | The specific animation frame to set for an object or UI element. | 3 | `1`<br>`10`<br>`15` |

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
| `mouth` | Number | The catalog ID for the cat's mouth part. | 9 | `-1`<br>`-2`<br>`1` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 8 | `0`<br>`1`<br>`10` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 7 | `-1`<br>`1000`<br>`1001` |
| `eyes` | Number | The ID for the eye mutation appearance. | 5 | `-1`<br>`-2`<br>`1029` |
| `ears` | Number | The ID for the ear mutation appearance. | 5 | `-1`<br>`-2`<br>`1500` |
| `legs` | Number | The ID or range of IDs for the leg mutation appearance. | 5 | `-1`<br>`306`<br>`322` |
| `body` | Float | The catalog ID for the cat's body part. | 4 | `-1`<br>`1`<br>`1.1` |
| `head` | Float | The catalog ID for the cat's head part. | 3 | `-1`<br>`1`<br>`1.3` |
| `eyebrows` | Number | The ID for the eyebrow mutation appearance. | 3 | `-1`<br>`-2`<br>`440` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 2 | `-1`<br>`-2`<br>`1` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 2 | `-1`<br>`-2`<br>`1` |
| `texture` | Integer | The catalog ID for the cat's texture. | 1 | `-1`<br>`1`<br>`1000` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 1 | `-1`<br>`-2`<br>`1` |
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 1 | `-1`<br>`1`<br>`10` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 16 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 16 | `cha`<br>`coins`<br>`con` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 14 | `false`<br>`true` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 13 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 8 | `{ . . . }` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 2 | `examine`<br>`lever`<br>`open` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 4 | `cha`<br>`coins`<br>`con` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 4 | `dimensionx`<br>`endoftime`<br>`future` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 2 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 1 | `examine`<br>`lever`<br>`open` |
| `fixed_chance` | Number | A fixed percentage chance for a specific outcome or option to occur. | 1 | `50%` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| `fixed_chance` | Number | A fixed percentage chance for a specific outcome or option to occur. | 1 | `50%` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 12 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 12 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 12 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 12 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 12 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 14 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 14 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 14 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 14 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 13 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 11 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 11 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 11 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 11 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 11 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>tag |
| `Fights` | Integer | The number of fights this status or effect persists for. | 6 | `1`<br>`3`<br>`99` |
| [`CharacterTypeGainsStatusAtBattleStart`](./Events_and_Encounters.md#object-charactertypegainsstatusatbattlestart) | Object | Defines status effects applied to characters with a specific tag at the start of a battle. | 5 | `{ . . . }` |
| [`StatusRandomEnemiesOnBattleStart`](./Events_and_Encounters.md#object-statusrandomenemiesonbattlestart) | Object | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 3 | `{ . . . }` |
| [`KillEnemyOfTypeAtBattleStart`](./Events_and_Encounters.md#object-killenemyoftypeatbattlestart) | Object  | Specifies that a specific enemy type is killed at the start of the next battle. | 2 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

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
| [`event`](../Reference_and_Meta/Enums.md#enum-event) | Enum | Specifies the event to force, either by name or by a nested object defining its type and level. | 5 | `Blessing`<br>`Death`<br>`Tragedy` |
| `same_cat` | Boolean | If true, the next event from the set uses the same cat as the previous event. | 5 | `true` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 4 | `0`<br>`1`<br>`10` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 1 | `dimensionx`<br>`endoftime`<br>`future` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 6 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 5 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 1 | `dimensionx`<br>`endoftime`<br>`future` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 8 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 8 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 8 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 8 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 7 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

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
| `fights_skipped` | Number | The number of fights the temporarily absent cat will skip before returning. | 7 | `0`<br>`1` |
| [`return_as`](../Reference_and_Meta/Enums.md#enum-return_as) | Enum | Specifies the role or faction the temporarily absent cat returns as. | 3 | `enemy` |
| [`return_during`](../Reference_and_Meta/Enums.md#enum-return_during) | Enum | Specifies the encounter type during which the temporarily absent cat returns. | 3 | `boss` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 4 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 4 | `common`<br>`rare`<br>`cha` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 5 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 5 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 5 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 5 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 2 | `{ . . . }` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 7 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 7 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 7 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>tag |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 5 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| `Stun` | Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `Fear` | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | Default<br>FormChange<br>Druid |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 7 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 7 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 6 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 | `{ . . . }` |

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
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 | `0`<br>`1`<br>`10` |
| `Fear` | Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| `Bleed` | Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 6 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 6 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 | `{ . . . }` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 7 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 6 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 6 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 7 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 7 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 7 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 7 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 7 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 5 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 5 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 5 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 5 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 6 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 6 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 5 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 5 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 5 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 5 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 5 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 6 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 5 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 6 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 6 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 6 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 6 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 6 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 6 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 6 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 6 | `{ . . . }` |

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


### Object: `skip`


**Definition:** Specifies the option to skip or decline the current encounter.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 4 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 4 | `common`<br>`rare`<br>`cha` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 4 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 4 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 4 | `{ . . . }` |
| [`hint_chapter_exit`](../Reference_and_Meta/Enums.md#enum-hint_chapter_exit) | Enum | Specifies the chapter to which the exit hint points. | 4 | `dimensionx`<br>`endoftime`<br>`future` |

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
| `con` | Integer | The Constitution stat value or modifier. | 4 | `-1`<br>`-2`<br>`-3` |
| `int` | Integer | The Intelligence stat value or modifier. | 4 | `-1`<br>`-10`<br>`-2` |
| `cha` | Integer | The Charisma stat value or modifier. | 4 | `+1`<br>`-1`<br>`-2` |
| `str` | Integer | The Strength stat value or modifier. | 4 | `-1`<br>`-2`<br>`-3` |
| `spd` | Integer | The Speed stat value or modifier. | 4 | `-1`<br>`-10`<br>`-2` |
| `lck` | Integer | The Luck stat value or modifier. | 4 | `-1`<br>`-2`<br>`-3` |
| `dex` | Integer | The Dexterity stat value or modifier. | 4 | `-1`<br>`-2`<br>`-3` |

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
| [`play_animation`](../Reference_and_Meta/Arrays.md#array-play_animation) | Array / Enum | Specifies an animation to play, optionally as an array with a probability weight. | 4 | `[resultBlessing .5]`<br>`[resultGood .5]`<br>`[resultLeave 0]` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 4 | `common`<br>`rare`<br>`cha` |
| [`random_pool`](../Reference_and_Meta/Arrays.md#array-random_pool) | Array | An array of possible items or rewards from which one is randomly selected. | 3 | `[` |
| `add_weather` | `String` | Specifies a weather effect type to apply to the current map. | 1 | `AlienOvergrowth`<br>`Birdemic`<br>`GeomagneticStorm` |
| [`weather_roll`](../Reference_and_Meta/Arrays.md#array-weather_roll) | Array | An array that defines weather roll parameters for an outcome. | 1 | `[` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 4 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 4 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 4 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 4 | `{ . . . }` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 3 | `cha`<br>`coins`<br>`con` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 3 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 3 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 | `{ . . . }` |

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
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

</details>


---


### Object: `pick`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Assets_and_Localization/Strings.md#string-animation) | String | Specifies the animation played when the ability is used. | 3 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 3 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 3 | `cha`<br>`coins`<br>`con` |
| `copy_results` | String | Specifies the identifier of another option whose outcomes are replicated. | 3 | `examine`<br>`lever`<br>`open` |

</details>
### Object: `party_permanent_stats`


**Definition:** An object defining permanent stat increases applied to the party.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`main`](./Events_and_Encounters.md#object-main), [`rare`](./Events_and_Encounters.md#object-rare)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `con` | Integer | The Constitution stat value or modifier. | 2 | `-1`<br>`-2`<br>`-3` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 3 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 3 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 3 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 3 | `common`<br>`rare`<br>`cha` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 2 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 2 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| `get_item_from_pool` | `String` | Grants an item from the specified pool or a specific item name. | 1 | `Bird_items`<br>`Coin_items`<br>`Eye_items` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 2 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 2 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 | `{ . . . }` |

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
| `mouth` | Number | The catalog ID for the cat's mouth part. | 2 | `-1`<br>`-2`<br>`1` |
| `eyes` | Number | The ID for the eye mutation appearance. | 2 | `-1`<br>`-2`<br>`1029` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 2 | `0`<br>`1`<br>`10` |
| `ears` | Number | The ID for the ear mutation appearance. | 2 | `-1`<br>`-2`<br>`1500` |
| `eyebrows` | Number | The ID for the eyebrow mutation appearance. | 2 | `-1`<br>`-2`<br>`440` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 2 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| `fixed_chance` | Number | A fixed percentage chance for a specific outcome or option to occur. | 1 | `50%` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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


### Object: `free`


**Definition:** If true, this option requires no cost to activate.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 2 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 2 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 2 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 2 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 2 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 0 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

</details>


---


---


## Auto-Discovered Objects


### Object: `yank_it_out`


**Definition:** Defines a dialogue option that yanks out an object using Strength.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 0 | `common`<br>`rare`<br>`cha` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 0 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 0 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 0 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 0 | `common`<br>`rare`<br>`cha` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `buy3`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Assets_and_Localization/Strings.md#string-animation) | String | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`good`](./Events_and_Encounters.md#object-good) | Object  | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `{ . . . }` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| `animation_fail` | String | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

</details>


### Object: `buy2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Assets_and_Localization/Strings.md#string-animation) | String | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`good`](./Events_and_Encounters.md#object-good) | Object  | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `{ . . . }` |
| `stat` | String | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| `animation_fail` | String | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

</details>


### Object: `buy1`


**Definition:** Specifies the player character's attempt to buy one of the offered items.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`options`](./Events_and_Encounters.md#object-options)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`animation_fail`](../Reference_and_Meta/Enums.md#enum-animation_fail) | Enum | Specifies the animation to play when an action fails. | 1 | `choice_no_coins` |
| `stat_max` | Number | The maximum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |
| `stat_min` | Number | The minimum stat value required for an event option to succeed. | 1 | `1`<br>`10`<br>`15` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`copy_results`](../Reference_and_Meta/Enums.md#enum-copy_results) | Enum | Specifies the identifier of another option whose outcomes are replicated. | 1 | `examine`<br>`lever`<br>`open` |
| `fixed_chance` | Number | A fixed percentage chance for a specific outcome or option to occur. | 1 | `50%` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 0 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`label`](../Reference_and_Meta/Enums.md#enum-label) | Enum | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`requirements`](./Events_and_Encounters.md#object-requirements) | Object  | An object defining the conditions that must be met for a reward or event branch to be available. | 1 | `{ . . . }` |

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
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 1 | `common`<br>`rare`<br>`cha` |
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| `stat` | Equation | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |
| [`bad`](./Events_and_Encounters.md#object-bad) | Object  | Defines the bad outcome branch of an event option, including its frame and rewards. | 1 | `{ . . . }` |

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
| [`label`](../Assets_and_Localization/Strings.md#string-label) | String | Specifies the localization key or display string for an event option. | 1 | `"1 injury"`<br>`"1"`<br>`"5"` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |
| [`stat`](../Reference_and_Meta/Enums.md#enum-stat) | Enum | Specifies the stat used for a success check in an event option. | 1 | `cha`<br>`coins`<br>`con` |

</details>


---

