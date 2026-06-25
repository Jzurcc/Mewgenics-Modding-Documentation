# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Combat Rewards

> **Associated Files:** `data/combat_reward_table.gon`

### Object: `boss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 33

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| `item_chance` | Float |  | 12 |

</details>

---

### Object: `hard`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 21

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| [`item_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |

</details>

---

### Object: `miniboss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| [`item_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |

</details>

---

### Object: `normal`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`1`](#object-1), [`2`](#object-2), [`3`](#object-3), [`4`](#object-4)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| [`item_chance`](./Math_Equations.md) | Equation |  (Must be float values) | 12 |

</details>

---

### Numerical Objects

> The following objects are numeric keys or array indices.

### Object: `1`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Float |  | 4 |
| `food_bonus` | Float |  | 4 |
| [`boss`](#object-boss) | Object |  | 3 |
| [`hard`](#object-hard) | Object |  | 3 |
| [`miniboss`](#object-miniboss) | Object |  | 3 |
| [`normal`](#object-normal) | Object |  | 3 |
| `chapters` | Object |  | 1 |

</details>

---

### Object: `2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Float |  | 4 |
| `food_bonus` | Float |  | 4 |
| [`boss`](#object-boss) | Object |  | 3 |
| [`hard`](#object-hard) | Object |  | 3 |
| [`miniboss`](#object-miniboss) | Object |  | 3 |
| [`normal`](#object-normal) | Object |  | 3 |
| `chapters` | Object |  | 1 |

</details>

---

### Object: `3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Float |  | 4 |
| `food_bonus` | Float |  | 4 |
| [`boss`](#object-boss) | Object |  | 3 |
| [`hard`](#object-hard) | Object |  | 3 |
| [`miniboss`](#object-miniboss) | Object |  | 3 |
| [`normal`](#object-normal) | Object |  | 3 |
| `chapters` | Object |  | 1 |

</details>

---

### Object: `4`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`boss`](#object-boss) | Object |  | 3 |
| [`hard`](#object-hard) | Object |  | 3 |
| [`miniboss`](#object-miniboss) | Object |  | 3 |
| [`normal`](#object-normal) | Object |  | 3 |
| `coins_bonus` | Float |  | 3 |
| `food_bonus` | Float |  | 3 |

</details>

---

