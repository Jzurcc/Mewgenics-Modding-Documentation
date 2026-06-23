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
| [`{Graphics Keys}`](./Engine_GraphicsKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 4118 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Block | All valid keys from the specified engine key are applicable to this context/block. | 206 |
| [`deathsound`](./Enums.md#enum-deathsound) | Enum |  | 13 |
| [`text`](./Strings.md#string-text) | String |  | 13 |
| `id` | Integer |  | 13 |
| [`stats`](#context-stats) | Block |  | 12 |
| [`scars`](#context-scars) | Block |  | 10 |

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

