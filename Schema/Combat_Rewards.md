# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Combat Rewards

> **Associated Files:** `data/combat_reward_table.gon`

### Object: `boss`


**Definition:** No definition provided.  
**Total Count:** 33


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Integer | The amount of coins (or a random range [min max]) awarded when the spawn trigger occurs. | 3 |  |
| [`food`](./Arrays.md#array-food) | Array | The range [min, max] of food units awarded as a reward. | 3 |  |
| [`consumable_chance`](./Math_Equations.md) | Equation | (Must be float values) | 3 |  |
| `item_chance` | Float | The probability (0 to 1) that an item drops from this encounter. | 3 |  |

</details>

---

### Object: `hard`


**Definition:** No definition provided.  
**Total Count:** 21


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Integer | The amount of coins (or a random range [min max]) awarded when the spawn trigger occurs. | 3 |  |
| [`food`](./Arrays.md#array-food) | Array | The range [min, max] of food units awarded as a reward. | 3 |  |
| [`consumable_chance`](./Math_Equations.md) | Equation | (Must be float values) | 3 |  |
| [`item_chance`](./Math_Equations.md) | Equation | (Must be float values) | 3 |  |

</details>

---

### Object: `miniboss`


**Definition:** No definition provided.  
**Total Count:** 13


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Integer | The amount of coins (or a random range [min max]) awarded when the spawn trigger occurs. | 3 |  |
| [`food`](./Arrays.md#array-food) | Array | The range [min, max] of food units awarded as a reward. | 3 |  |
| [`consumable_chance`](./Math_Equations.md) | Equation | (Must be float values) | 3 |  |
| [`item_chance`](./Math_Equations.md) | Equation | (Must be float values) | 3 |  |

</details>

---

### Object: `normal`


**Definition:** Character Form: Behavior and stats for the \'Normal\' state.  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Integer | The amount of coins (or a random range [min max]) awarded when the spawn trigger occurs. | 3 |  |
| [`food`](./Arrays.md#array-food) | Array | The range [min, max] of food units awarded as a reward. | 3 |  |
| [`consumable_chance`](./Math_Equations.md) | Equation | (Must be float values) | 3 |  |
| [`item_chance`](./Math_Equations.md) | Equation | (Must be float values) | 3 |  |

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

