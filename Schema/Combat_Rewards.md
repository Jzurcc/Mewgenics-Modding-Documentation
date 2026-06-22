# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Combat Rewards

> **Associated Files:** `data/combat_reward_table.gon`

### Context: `boss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`1`](#context-1), [`2`](#context-2), [`3`](#context-3), [`4`](#context-4)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| `item_chance` | Integer |  | 12 |

</details>

---

### Context: `hard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`1`](#context-1), [`2`](#context-2), [`3`](#context-3), [`4`](#context-4)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| [`item_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |

</details>

---

### Context: `miniboss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`1`](#context-1), [`2`](#context-2), [`3`](#context-3), [`4`](#context-4)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| [`item_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |

</details>

---

### Context: `normal`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`1`](#context-1), [`2`](#context-2), [`3`](#context-3), [`4`](#context-4)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| [`item_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |

</details>

---

### Numerical Contexts

> The following contexts are numeric keys or array indices.

### Context: `1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Float |  | 4 |
| `food_bonus` | Integer |  | 4 |
| [`boss`](#context-boss) | Block |  | 3 |
| [`hard`](#context-hard) | Block |  | 3 |
| [`miniboss`](#context-miniboss) | Block |  | 3 |
| [`normal`](#context-normal) | Block |  | 3 |
| `chapters` | Block |  | 1 |

</details>

---

### Context: `2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Float |  | 4 |
| `food_bonus` | Integer |  | 4 |
| [`boss`](#context-boss) | Block |  | 3 |
| [`hard`](#context-hard) | Block |  | 3 |
| [`miniboss`](#context-miniboss) | Block |  | 3 |
| [`normal`](#context-normal) | Block |  | 3 |
| `chapters` | Block |  | 1 |

</details>

---

### Context: `3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Float |  | 4 |
| `food_bonus` | Integer |  | 4 |
| [`boss`](#context-boss) | Block |  | 3 |
| [`hard`](#context-hard) | Block |  | 3 |
| [`miniboss`](#context-miniboss) | Block |  | 3 |
| [`normal`](#context-normal) | Block |  | 3 |
| `chapters` | Block |  | 1 |

</details>

---

### Context: `4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`boss`](#context-boss) | Block |  | 3 |
| `coins_bonus` | Float |  | 3 |
| `food_bonus` | Integer |  | 3 |
| [`hard`](#context-hard) | Block |  | 3 |
| [`miniboss`](#context-miniboss) | Block |  | 3 |
| [`normal`](#context-normal) | Block |  | 3 |

</details>

---

