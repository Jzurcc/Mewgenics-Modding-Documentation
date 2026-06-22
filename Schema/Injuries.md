# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Injuries

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/13) |
| :--- | :--- | :--- | :--- |
| [`deathsound`](./Enums.md#enum-deathsound) | Enum/String |  | 13 |
| `id` | Number |  | 13 |
| `text` | String |  | 13 |
| [`stats`](./Injuries.md#context-stats) | Block |  | 12 |
| [`scars`](./Injuries.md#context-scars) | Block |  | 10 |
| [`alt_animations`](./Arrays.md#array-alt_animations) | Array |  | 9 |

</details>

---

### Context: `scars`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

| Property Key | Type | Definition | Count (X/6) |
| :--- | :--- | :--- | :--- |
| [`head`](./Arrays.md#array-head) | Array |  | 6 |
| [`body`](./Arrays.md#array-body) | Array |  | 3 |
| [`arms`](./Arrays.md#array-arms) | Array |  | 1 |
| [`legs`](./Arrays.md#array-legs) | Array |  | 1 |
| [`limbs`](./Arrays.md#array-limbs) | Array |  | 1 |

</details>

---

### Context: `stats`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

| Property Key | Type | Definition | Count (X/3) |
| :--- | :--- | :--- | :--- |
| `con` | Number |  | 3 |
| `lck` | Number |  | 3 |
| `cha` | Number |  | 2 |
| `dex` | Number |  | 2 |
| `int` | Number |  | 2 |
| `str` | Number |  | 2 |
| `spd` | Number |  | 1 |

</details>

---

