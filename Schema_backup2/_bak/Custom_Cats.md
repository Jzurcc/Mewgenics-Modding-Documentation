# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Math_Equations.md).

## Custom Cats

> **Associated Files:** `data/custom_cats.gon`


### Context: `ROOT` (211 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `texture` | Number |  | 211 |
| `default_frame` | Number |  | 210 |
| `palette` | Number |  | 210 |
| `righteye` | Number |  | 200 |
| [`voice`](./Enums.md#enum-voice) | Enum |  | 200 |
| `lefteye` | Number |  | 198 |
| `claws` | Number |  | 196 |
| `mouth` | Number |  | 192 |
| `rightear` | Number |  | 188 |
| `leftear` | Number |  | 187 |
| `head` | Number |  | 184 |
| `tail` | Number |  | 180 |
| `arm2` | Number |  | 179 |
| `arm1` | Number |  | 177 |
| `righteyebrow` | Number |  | 176 |
| `lefteyebrow` | Number |  | 175 |
| `leg1` | Number |  | 174 |
| `body` | Number |  | 173 |
| `leg2` | Number |  | 172 |
| [`pitch`](./Enums.md#enum-pitch) | Enum |  | 116 |
| [`class_anis`](./Enums.md#enum-class_anis) | Enum |  | 40 |
| [`default_face`](./Enums.md#enum-default_face) | Enum |  | 15 |
| `face` | Number |  | 2 |

</details>

---

### Context: `arm1` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `frame` | Number |  | 2 |
| `texture` | Number |  | 2 |

</details>

---

### Context: `arm2` (2 instances)

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `frame` | Number |  | 2 |
| `texture` | Number |  | 2 |

</details>

---

