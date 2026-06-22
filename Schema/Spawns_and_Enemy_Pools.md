# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Spawns & Enemy Pools

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `Fly, Worm, Rat` |  |
| `value` | Number | `0, 1, .5` |  |
| `early_spawn` | Boolean | `true` |  |
| `orientation` | [`Enum/String`](./Enums.md#enum-orientation) | `east, north, south` |  |
| `tag_location` | [`Enum/String`](./Enums.md#enum-tag_location) | `FinalBossCloneSpot, ChaosValidPosition, HitlerMiniInitial` |  |
| `forced_placement` | Boolean | `true` |  |
| `trap` | [`Enum/String`](./Enums.md#enum-trap) | `WaterKittenTrap, WebTrap` |  |
| `image` | String | `"empty.png"` |  |
| `name` | String | `"Empty"` |  |
| `reserved` | [`Enum/String`](./Enums.md#enum-reserved) | `for` |  |
| `utility` | [`Enum/String`](./Enums.md#enum-utility) | `PlayerSpawn` |  |

</details>

---

### Context: `editor`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `category` | Number | `4, 1, 3` |  |
| `image` | [`Array`](./Arrays.md#array-image) | `[ "fly.png" ], [ "rat.png" ], [ "shadow.png" "cat.png" ]` |  |
| `name` | String | `"Fly", "Rat", "Player Cat Spawn"` |  |
| `paint` | Boolean | `false, true` |  |
| `image_tint` | [`Array`](./Arrays.md#array-image_tint) | `[ blue none ], [ yellow ], [ blue ]` |  |
| `subcategory` | Number | `2, 1, 3` |  |
| `layer` | Number | `2` |  |

</details>

---

### Context: `weather_element_alt`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `element` | [`Enum/String`](./Enums.md#enum-element) | `Ice` | Specific element type required or applied. |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `IceElemental` |  |

</details>

---

