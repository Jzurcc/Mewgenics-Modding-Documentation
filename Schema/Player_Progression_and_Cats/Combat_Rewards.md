---
title: "Combat Rewards Schema"
description: "Loot tables and combat reward generation logic."
---

# Combat Rewards Schema


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
> This schema dictates what the player receives after finishing a battle, distributing gold, items, and experience based on the difficulty.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
acts {
	0 { //tutorial, everything hardcoded
	}

	1 { //alley and such
		food_bonus 1
		coins_bonus .5

		chapters {
			1 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [2 5]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [5 8]
					item_chance 1
					consumable_chance .5
				}
			}
			2 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [4 8]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [6 12]
					item_chance 1
					consumable_chance .5
				}
			}
			3 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
			4 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
		}
	}

	2 { //desert and such
		food_bonus 1.75
		coins_bonus .75

		chapters {
			1 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [2 5]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [5 8]
					item_chance 1
					consumable_chance .5
				}
			}
			2 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [4 8]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [6 12]
					item_chance 1
					consumable_chance .5
				}
			}
			3 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
			4 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
		}
	}

	3 { //lab and such
		food_bonus 2.5
		coins_bonus 1

		chapters {
			1 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [2 5]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [5 8]
					item_chance 1
					consumable_chance .5
				}
			}
			2 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [4 8]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [6 12]
					item_chance 1
					consumable_chance .5
				}
			}
			3 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
			4 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
		}
	}
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Combat_Rewards.md`](../../Directory/Enemies_and_Combat/Combat_Rewards.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Combat Rewards

> **Associated Files:** `data/combat_reward_table.gon`


### Object: `boss`


**Definition:** An object defining the properties of a boss encounter, such as rewards or level.  
**Total Count:** 213

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](./Combat_Rewards.md#object-1), [`2`](./Combat_Rewards.md#object-2), [`3`](./Combat_Rewards.md#object-3), [`4`](./Combat_Rewards.md#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`food`](../Reference_and_Meta/Arrays.md#array-food) | Array | The range [min, max] of food items dropped. | 12 | `[1 3]`<br>`[10 15]`<br>`[2 5]` |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 12 | `1`<br>`2`<br>`25` |
| `consumable_chance` | Float | The probability of dropping a consumable. | 12 | `.25`<br>`.3`<br>`.5` |
| `item_chance` | Float | The probability of dropping an item. | 12 | `.25`<br>`.5`<br>`1` |

</details>


---


### Object: `miniboss`


**Definition:** An array or object defining the reward table for miniboss encounters, including coin ranges, food ranges, and loot chances.  
**Total Count:** 54

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](./Combat_Rewards.md#object-1), [`2`](./Combat_Rewards.md#object-2), [`3`](./Combat_Rewards.md#object-3), [`4`](./Combat_Rewards.md#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`food`](../Reference_and_Meta/Arrays.md#array-food) | Array | The range [min, max] of food items dropped. | 12 | `[1 3]`<br>`[10 15]`<br>`[2 5]` |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 12 | `1`<br>`2`<br>`25` |
| `consumable_chance` | Float | The probability of dropping a consumable. | 12 | `.25`<br>`.3`<br>`.5` |
| `item_chance` | Float | The probability of dropping an item. | 12 | `.25`<br>`.5`<br>`1` |

</details>


---


### Object: `hard`


**Definition:** Configuration for hard difficulty, including elite/champ budgets and rewards.  
**Total Count:** 47

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](./Combat_Rewards.md#object-1), [`2`](./Combat_Rewards.md#object-2), [`3`](./Combat_Rewards.md#object-3), [`4`](./Combat_Rewards.md#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`food`](../Reference_and_Meta/Arrays.md#array-food) | Array | The range [min, max] of food items dropped. | 12 | `[1 3]`<br>`[10 15]`<br>`[2 5]` |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 12 | `1`<br>`2`<br>`25` |
| `consumable_chance` | Float | The probability of dropping a consumable. | 12 | `.25`<br>`.3`<br>`.5` |
| `item_chance` | Float | The probability of dropping an item. | 12 | `.25`<br>`.5`<br>`1` |

</details>


---


### Object: `normal`


**Definition:** An array or object defining the reward table for normal encounters, including coin ranges, food ranges, and loot chances.  
**Total Count:** 41

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](./Combat_Rewards.md#object-1), [`2`](./Combat_Rewards.md#object-2), [`3`](./Combat_Rewards.md#object-3), [`4`](./Combat_Rewards.md#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`food`](../Reference_and_Meta/Arrays.md#array-food) | Array | The range [min, max] of food items dropped. | 12 | `[1 3]`<br>`[10 15]`<br>`[2 5]` |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 12 | `1`<br>`2`<br>`25` |
| `consumable_chance` | Float | The probability of dropping a consumable. | 12 | `.25`<br>`.3`<br>`.5` |
| `item_chance` | Float | The probability of dropping an item. | 12 | `.25`<br>`.5`<br>`1` |

</details>


---


### Numerical Objects

> The following objects are numeric keys or array indices.


### Object: `3`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `2`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `1`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `4`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---