# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Injuries

> **Associated Files:** `data/injuries.gon`

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Blocks}`](./Engine_LogicBlocks.md#all-confirmed-logic-block-values) | Block | Any valid logic block. See Engine_LogicBlocks.md for the full list. |  |
| [`deathsound`](./Enums.md#enum-deathsound) | Enum |  | 13 |
| `id` | Integer |  | 13 |
| [`text`](./Strings.md#string-text) | String |  | 13 |
| [`stats`](#context-stats) | Block |  | 12 |
| [`scars`](#context-scars) | Block |  | 10 |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  | 9 |

</details>

---

### Context: `stats`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 12

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Integer |  | 3 |
| `lck` | Integer |  | 3 |
| `cha` | Integer |  | 2 |
| `dex` | Integer |  | 2 |
| `int` | Integer |  | 2 |
| `str` | Integer |  | 2 |
| `spd` | Integer |  | 1 |

</details>

---

### Context: `scars`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 10

> **Referenced by:** [`ROOT`](#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`head`](./Arrays.md#array-head) | Array |  | 6 |
| [`body`](./Arrays.md#array-body) | Array |  | 3 |
| [`arms`](./Arrays.md#array-arms) | Array |  | 1 |
| [`legs`](./Arrays.md#array-legs) | Array |  | 1 |
| [`limbs`](./Arrays.md#array-limbs) | Array |  | 1 |

</details>

---

