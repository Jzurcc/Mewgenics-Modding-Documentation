---
title: "Boss Cutscene Info Schema"
description: "Camera and timing configuration for boss intros."
---

# Boss Cutscene Info Schema

## Overview
> [!NOTE]
> This schema triggers cinematic elements before a major battle, handling the camera panning, timing, and title cards.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
error {
    name BOSS_ERROR_NAME
    frame_label error

    quotes [
        BOSS_ERROR_QUOTE_1
    ]
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Boss_Cutscene_Info.md`](../../Directory/Enemies_and_Combat/Boss_Cutscene_Info.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Boss Cutscene Info

> **Associated Files:** `data/boss_cutscene_info.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 67

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`frame_label`](../Reference_and_Meta/Enums.md#enum-frame_label) | Enum | Specifies the frame or cutscene animation label for the boss encounter. | 67 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 36 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 5 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---