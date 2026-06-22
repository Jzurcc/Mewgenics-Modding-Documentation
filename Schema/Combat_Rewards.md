# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Combat Rewards

### Context: `boss`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | [`Array`](./Arrays.md#array-coins) | `[ 10 20 ]` |  |
| `consumable_chance` | [`Enum/String`](./Enums.md#enum-consumable_chance) | `.5` |  |
| `food` | [`Array`](./Arrays.md#array-food) | `[ 5 8 ], [ 6 12 ], [ 10 15 ]` |  |
| `item_chance` | Number | `1` |  |

</details>

---

### Context: `hard`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | [`Array`](./Arrays.md#array-coins) | `[ 1 6 ]` |  |
| `consumable_chance` | [`Enum/String`](./Enums.md#enum-consumable_chance) | `.25` |  |
| `food` | [`Array`](./Arrays.md#array-food) | `[ 4 7 ]` |  |
| `item_chance` | [`Enum/String`](./Enums.md#enum-item_chance) | `.25` |  |

</details>

---

### Context: `miniboss`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | [`Array`](./Arrays.md#array-coins) | `[ 10 20 ]` |  |
| `consumable_chance` | [`Enum/String`](./Enums.md#enum-consumable_chance) | `.3` |  |
| `food` | [`Array`](./Arrays.md#array-food) | `[ 5 10 ], [ 2 5 ], [ 4 8 ]` |  |
| `item_chance` | [`Enum/String`](./Enums.md#enum-item_chance) | `.5` |  |

</details>

---

### Context: `normal`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`1`](./Combat_Rewards.md#context-1), [`2`](./Combat_Rewards.md#context-2), [`3`](./Combat_Rewards.md#context-3), [`4`](./Combat_Rewards.md#context-4)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins` | [`Array`](./Arrays.md#array-coins) | `[ 1 6 ]` |  |
| `consumable_chance` | [`Enum/String`](./Enums.md#enum-consumable_chance) | `.25` |  |
| `food` | [`Array`](./Arrays.md#array-food) | `[ 1 3 ]` |  |
| `item_chance` | [`Enum/String`](./Enums.md#enum-item_chance) | `.25` |  |

</details>

---

### Context: `1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | [`Enum/String`](./Enums.md#enum-coins_bonus) | `.5, 1` |  |
| `food_bonus` | Number | `1` |  |
| `boss` | [`Block`](./Combat_Rewards.md#context-boss) | `{ ... }` |  |
| `hard` | [`Block`](./Combat_Rewards.md#context-hard) | `{ ... }` |  |
| `miniboss` | [`Block`](./Combat_Rewards.md#context-miniboss) | `{ ... }` |  |
| `normal` | [`Block`](./Combat_Rewards.md#context-normal) | `{ ... }` |  |
| `chapters` | Block | `{ ... }` |  |

</details>

---

### Context: `2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Number | `1, .75` |  |
| `food_bonus` | Number | `1, 1.75` |  |
| `boss` | [`Block`](./Combat_Rewards.md#context-boss) | `{ ... }` |  |
| `hard` | [`Block`](./Combat_Rewards.md#context-hard) | `{ ... }` |  |
| `miniboss` | [`Block`](./Combat_Rewards.md#context-miniboss) | `{ ... }` |  |
| `normal` | [`Block`](./Combat_Rewards.md#context-normal) | `{ ... }` |  |
| `chapters` | Block | `{ ... }` |  |

</details>

---

### Context: `3`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `coins_bonus` | Number | `1` |  |
| `food_bonus` | Number | `2.5, 1` |  |
| `boss` | [`Block`](./Combat_Rewards.md#context-boss) | `{ ... }` |  |
| `hard` | [`Block`](./Combat_Rewards.md#context-hard) | `{ ... }` |  |
| `miniboss` | [`Block`](./Combat_Rewards.md#context-miniboss) | `{ ... }` |  |
| `normal` | [`Block`](./Combat_Rewards.md#context-normal) | `{ ... }` |  |
| `chapters` | Block | `{ ... }` |  |

</details>

---

### Context: `4`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `boss` | [`Block`](./Combat_Rewards.md#context-boss) | `{ ... }` |  |
| `coins_bonus` | Number | `1` |  |
| `food_bonus` | Number | `1` |  |
| `hard` | [`Block`](./Combat_Rewards.md#context-hard) | `{ ... }` |  |
| `miniboss` | [`Block`](./Combat_Rewards.md#context-miniboss) | `{ ... }` |  |
| `normal` | [`Block`](./Combat_Rewards.md#context-normal) | `{ ... }` |  |

</details>

---

