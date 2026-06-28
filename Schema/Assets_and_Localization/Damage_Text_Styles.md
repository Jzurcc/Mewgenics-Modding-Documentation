---
title: "Damage Text Styles Schema"
description: "Configuration for floating combat text."
---

# Damage Text Styles Schema

## Overview
> [!NOTE]
> This schema customizes how numbers look when they pop out of enemies, differentiating normal hits, crits, and healing.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
CriticalHitStyle {
    style "critical_hit"
    color { r 1.0 g 0.8 b 0.0 }
    scale 1.5
    shake true
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Damage_Text_Styles.md`](../../Directory/System_and_Engine/Damage_Text_Styles.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Damage Text Styles

> **Associated Files:** `data/damage_text_styles.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 26

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |
| [`color`](../Reference_and_Meta/Arrays.md#array-color) | Array | The RGB color of the light source. | 26 | `[.27 .47 .18]`<br>`[.3, .7, 1]`<br>`[.32 .10 .10]` |
| `right_icon` | String | The name of the icon to display on the right side of the damage text. | 10 | `coin`<br>`divineshield`<br>`heal` |
| `back_icon` | String | The name of the icon to display behind the damage text. | 8 | `bleed`<br>`burn`<br>`confusion` |
| [`outline_color`](../Reference_and_Meta/Enums.md#enum-outline_color) | Enum | The color of the text outline. | 2 | `white` |
| [`suffix`](./Strings.md#string-suffix) | String | A string appended to the damage text. | 1 | `"!!!"` |

</details>


---