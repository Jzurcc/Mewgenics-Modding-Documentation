# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Injuries

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `deathsound` | [`Enum/String`](./Enums.md#enum-deathsound) | `Injury_BrokenPaw, Injury_BrokenRib, Injury_TornTendon` |  |
| `id` | Number | `1, 2, 0` |  |
| `text` | String | `"INJURY_NAME_TORNTENDON", "INJURY_NAME_BROKENPAW", "INJURY_NAME_BROKENRIB"` |  |
| `stats` | [`Block`](./Injuries.md#context-stats) | `{ ... }` |  |
| `scars` | [`Block`](./Injuries.md#context-scars) | `{ ... }` |  |
| `alt_animations` | [`Array`](./Arrays.md#array-alt_animations) | `[ [ dying, brokenPaw ], [ [ dying, dislocatedShoulder ], [ [ dying, intestinalProlapse ]` |  |

</details>

---

### Context: `stats`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `con` | Number | `-1` |  |
| `lck` | Number | `-2, -1` |  |
| `cha` | Number | `-1` |  |
| `dex` | Number | `-1` |  |
| `int` | Number | `-1` |  |
| `str` | Number | `-1` |  |
| `spd` | Number | `-1` |  |

</details>

---

### Context: `scars`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Injuries.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `head` | [`Array`](./Arrays.md#array-head) | `[ 34 41 ], [ 15 22 ], [ 23 33 ]` |  |
| `body` | [`Array`](./Arrays.md#array-body) | `[ 2 9 ], [ 16 25 ], [ 26 30 ]` |  |
| `arms` | [`Array`](./Arrays.md#array-arms) | `[ 10 20 ]` |  |
| `legs` | [`Array`](./Arrays.md#array-legs) | `[ 2 9 ]` |  |
| `limbs` | [`Array`](./Arrays.md#array-limbs) | `[ 21 31 ]` |  |

</details>

---

