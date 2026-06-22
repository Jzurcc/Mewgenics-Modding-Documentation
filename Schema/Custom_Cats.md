# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Custom Cats

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `texture` | Number | `1000, 1002, 1050` |  |
| `default_frame` | Number | `1000, 1001, 1002` |  |
| `palette` | Number | `137, 9, 16` |  |
| `righteye` | Number | `1001, 1, 1006` |  |
| `voice` | [`Enum/String`](./Enums.md#enum-voice) | `male1, male4, female2` |  |
| `lefteye` | Number | `1001, 1033, 1006` |  |
| `claws` | Number | `2, 1032, 1` |  |
| `mouth` | Number | `2, 1001, 1005` |  |
| `rightear` | Number | `1001, 1004, 3` |  |
| `leftear` | Number | `1005, 1, 1004` |  |
| `head` | Number | `1001, 1080, 1028` |  |
| `tail` | Number | `1001, 1010, 26` |  |
| `arm2` | Number | `1001, 42, 3` |  |
| `arm1` | Number | `2, 1018, 3` |  |
| `righteyebrow` | Number | `1001, 1005, 1006` |  |
| `lefteyebrow` | Number | `1001, 1005, 1006` |  |
| `leg1` | Number | `1001, 1, 3` |  |
| `body` | Number | `1000, 1001, 1028` |  |
| `leg2` | Number | `1019, 1001, 3` |  |
| `pitch` | Number | `2, .7, .5` |  |
| `class_anis` | [`Enum/String`](./Enums.md#enum-class_anis) | `Tank, Mage, Hunter` |  |
| `default_face` | [`Enum/String`](./Enums.md#enum-default_face) | `mad, worried, happy` |  |
| `face` | Number | `1019, 1004` |  |

</details>

---

### Context: `arm1`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame` | Number | `1040` |  |
| `texture` | Number | `1` |  |

</details>

---

### Context: `arm2`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `frame` | Number | `1040` |  |
| `texture` | Number | `1` |  |

</details>

---

