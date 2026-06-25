# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.



## Injuries

> **Associated Files:** `data/injuries.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 13

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`deathsound`](./Enums.md#enum-deathsound) | Enum |  | 13 |
| [`text`](./Strings.md#string-text) | String |  | 13 |
| `id` | Integer |  | 16 |
| [`stats`](#object-stats) | Object |  | 982 |
| [`scars`](#object-scars) | Object |  | 10 |

</details>

---

### Object: `stats`



**Definition:** Core character metrics (Health, Strength, etc.).  
**Total Count:** 497


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `con` | Integer |  | 65 |
| `lck` | Integer |  | 29 |
| `cha` | Integer |  | 46 |
| `dex` | Integer |  | 34 |
| `int` | Integer |  | 46 |
| `str` | Integer |  | 42 |
| `spd` | Integer |  | 53 |

</details>

---

### Object: `scars`



**Definition:** No definition provided.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`head`](./Arrays.md#array-head) | Array |  | 6 |
| [`body`](./Arrays.md#array-body) | Array |  | 3 |
| [`arms`](./Arrays.md#array-arms) | Array |  | 1 |
| [`legs`](./Arrays.md#array-legs) | Array |  | 1 |
| [`limbs`](./Arrays.md#array-limbs) | Array |  | 1 |

</details>

---

