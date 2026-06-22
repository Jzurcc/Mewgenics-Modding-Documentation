# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Combat Rewards

### Context: `boss`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Enums.md#enum-consumable_chance) | Enum/String |  | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| `item_chance` | Number |  | 12 |

</details>

---

### Context: `hard`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Enums.md#enum-consumable_chance) | Enum/String |  | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| [`item_chance`](./Enums.md#enum-item_chance) | Enum/String |  | 12 |

</details>

---

### Context: `miniboss`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Enums.md#enum-consumable_chance) | Enum/String |  | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| [`item_chance`](./Enums.md#enum-item_chance) | Enum/String |  | 12 |

</details>

---

### Context: `normal`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Definition | Count (X/12) |
| :--- | :--- | :--- | :--- |
| [`coins`](./Arrays.md#array-coins) | Array |  | 12 |
| [`consumable_chance`](./Enums.md#enum-consumable_chance) | Enum/String |  | 12 |
| [`food`](./Arrays.md#array-food) | Array |  | 12 |
| [`item_chance`](./Enums.md#enum-item_chance) | Enum/String |  | 12 |

</details>

---

### Context: `1`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| [`coins_bonus`](./Enums.md#enum-coins_bonus) | Enum/String |  | 4 |
| `food_bonus` | Number |  | 4 |
| [`boss`](./Combat_Rewards.md#context-boss) | Block |  | 3 |
| [`hard`](./Combat_Rewards.md#context-hard) | Block |  | 3 |
| [`miniboss`](./Combat_Rewards.md#context-miniboss) | Block |  | 3 |
| [`normal`](./Combat_Rewards.md#context-normal) | Block |  | 3 |
| `chapters` | Block |  | 1 |

</details>

---

### Context: `2`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Number |  | 4 |
| `food_bonus` | Number |  | 4 |
| [`boss`](./Combat_Rewards.md#context-boss) | Block |  | 3 |
| [`hard`](./Combat_Rewards.md#context-hard) | Block |  | 3 |
| [`miniboss`](./Combat_Rewards.md#context-miniboss) | Block |  | 3 |
| [`normal`](./Combat_Rewards.md#context-normal) | Block |  | 3 |
| `chapters` | Block |  | 1 |

</details>

---

### Context: `3`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Number |  | 4 |
| `food_bonus` | Number |  | 4 |
| [`boss`](./Combat_Rewards.md#context-boss) | Block |  | 3 |
| [`hard`](./Combat_Rewards.md#context-hard) | Block |  | 3 |
| [`miniboss`](./Combat_Rewards.md#context-miniboss) | Block |  | 3 |
| [`normal`](./Combat_Rewards.md#context-normal) | Block |  | 3 |
| `chapters` | Block |  | 1 |

</details>

---

### Context: `4`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| [`boss`](./Combat_Rewards.md#context-boss) | Block |  | 3 |
| `coins_bonus` | Number |  | 3 |
| `food_bonus` | Number |  | 3 |
| [`hard`](./Combat_Rewards.md#context-hard) | Block |  | 3 |
| [`miniboss`](./Combat_Rewards.md#context-miniboss) | Block |  | 3 |
| [`normal`](./Combat_Rewards.md#context-normal) | Block |  | 3 |

</details>

---

