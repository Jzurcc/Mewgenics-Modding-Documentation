# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see AUDIT_GAPS.md. For enum values, see [Enums.md](../Reference_and_Meta/Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

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