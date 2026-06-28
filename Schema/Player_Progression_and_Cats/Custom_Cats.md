---
title: "Custom Cats Schema"
description: "Properties for generating specific bespoke cats."
---

# Custom Cats Schema

## Overview
> [!NOTE]
> This schema forces the generation of a cat with exact properties, often used for tutorial or story-specific cats.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
TomTom {
    default_frame 1000
    texture 1000
    claws 1
    palette 9

    voice male1
    pitch .5
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Custom_Cats.md`](../../Directory/Cats_and_Classes/Custom_Cats.md)
- [`Tutorial_Cats.md`](../../Directory/Cats_and_Classes/Tutorial_Cats.md)
- [`Special_Strays.md`](../../Directory/Cats_and_Classes/Special_Strays.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Custom Cats

> **Associated Files:** `data/custom_cats.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 211

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `arm1`


**Definition:** The catalog ID for the cat's first arm part.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame` | Integer | The sprite frame index to display. | 2 | `1`<br>`10`<br>`100` |

</details>


---


### Object: `arm2`


**Definition:** The catalog ID for the cat's second arm part.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `frame` | Integer | The sprite frame index to display. | 2 | `1`<br>`10`<br>`100` |

</details>


---