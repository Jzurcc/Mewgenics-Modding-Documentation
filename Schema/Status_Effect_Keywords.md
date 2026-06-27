# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


## Status Effect Keywords

> **Associated Files:** `data/keyword_tooltips.gon`

### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 236

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 291 |  |
| [`tooltip_stackless`](./Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 76 |  |
| `icon_frame` | Integer | The sprite frame index for the buff icon. | 74 |  |
| [`tooltip_stacks`](./Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 69 |  |
| [`alias`](./Enums.md#enum-alias) | Enum | Specifies the reference name of another status effect to alias or copy properties from. | 57 |  |
| [`tooltip_stacks_singular`](./Strings.md#string-tooltip_stacks_singular) | String |  | 15 |  |
| [`tooltip_stacks_neg`](./Strings.md#string-tooltip_stacks_neg) | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. | 13 |  |
| [`name_stacks_neg`](./Strings.md#string-name_stacks_neg) | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. | 11 |  |
| [`tooltip_stacks_pos`](./Strings.md#string-tooltip_stacks_pos) | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. | 10 |  |
| [`name_reference_applier`](./Strings.md#string-name_reference_applier) | String | A localization key for the name displayed to the applier of this status effect. | 3 |  |
| [`tooltip_reference_applier`](./Strings.md#string-tooltip_reference_applier) | String | A localization key for the tooltip description displayed to the applier of this status effect. | 3 |  |
| [`tooltip_stackless_neg`](./Strings.md#string-tooltip_stackless_neg) | String | Localization key for the tooltip of the negative variant when not showing stack count. | 3 |  |
| [`tooltip_stackless_pos`](./Strings.md#string-tooltip_stackless_pos) | String | Localization key for the tooltip of the positive variant when not showing stack count. | 2 |  |

</details>

---

