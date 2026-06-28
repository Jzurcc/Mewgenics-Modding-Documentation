---
title: "Combat Rewards Schema"
description: "Loot tables and combat reward generation logic."
---

# Combat Rewards Schema

## Overview
This schema dictates what the player receives after finishing a battle, distributing gold, items, and experience based on the difficulty.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
StandardEncounter {
    pool "StandardEncounter"
    gold { min 10 max 25 }
    item_chance 15%
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
**Total Count:** 33

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 3 | `1`<br>`2`<br>`25` |
| [`food`](../Reference_and_Meta/Arrays.md#array-food) | Array | The range [min, max] of food items dropped. | 3 | `[1 3]`<br>`[10 15]`<br>`[2 5]` |
| `consumable_chance` | Equation | The probability of dropping a consumable. | 3 | `.25`<br>`.3`<br>`.5` |
| `item_chance` | Float | The probability of dropping an item. | 3 | `.25`<br>`.5`<br>`1` |

</details>


---


### Object: `hard`


**Definition:** Configuration for hard difficulty, including elite/champ budgets and rewards.
**Total Count:** 21

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 3 | `1`<br>`2`<br>`25` |
| [`food`](../Reference_and_Meta/Arrays.md#array-food) | Array | The range [min, max] of food items dropped. | 3 | `[1 3]`<br>`[10 15]`<br>`[2 5]` |
| `consumable_chance` | Equation | The probability of dropping a consumable. | 3 | `.25`<br>`.3`<br>`.5` |
| `item_chance` | Equation | The probability of dropping an item. | 3 | `.25`<br>`.5`<br>`1` |

</details>


---


### Object: `miniboss`


**Definition:** An array or object defining the reward table for miniboss encounters, including coin ranges, food ranges, and loot chances.
**Total Count:** 13

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 3 | `1`<br>`2`<br>`25` |
| [`food`](../Reference_and_Meta/Arrays.md#array-food) | Array | The range [min, max] of food items dropped. | 3 | `[1 3]`<br>`[10 15]`<br>`[2 5]` |
| `consumable_chance` | Equation | The probability of dropping a consumable. | 3 | `.25`<br>`.3`<br>`.5` |
| `item_chance` | Equation | The probability of dropping an item. | 3 | `.25`<br>`.5`<br>`1` |

</details>


---


### Object: `normal`


**Definition:** An array or object defining the reward table for normal encounters, including coin ranges, food ranges, and loot chances.
**Total Count:** 12

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `coins` | Integer | The amount of coins required to use this ability or obtained from this source. | 3 | `1`<br>`2`<br>`25` |
| [`food`](../Reference_and_Meta/Arrays.md#array-food) | Array | The range [min, max] of food items dropped. | 3 | `[1 3]`<br>`[10 15]`<br>`[2 5]` |
| `consumable_chance` | Equation | The probability of dropping a consumable. | 3 | `.25`<br>`.3`<br>`.5` |
| `item_chance` | Equation | The probability of dropping an item. | 3 | `.25`<br>`.5`<br>`1` |

</details>


---


### Numerical Objects

> The following objects are numeric keys or array indices.


### Object: `1`


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


### Object: `3`


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