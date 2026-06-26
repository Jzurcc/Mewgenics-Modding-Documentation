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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 291 |  |
| [`tooltip_stackless`](./Strings.md#string-tooltip_stackless) | String | The localized string key for the stackless version of the status effect's tooltip. | 76 |  |
| `icon_frame` | Integer | The sprite frame index for the elite buff's icon. | 74 |  |
| [`tooltip_stacks`](./Strings.md#string-tooltip_stacks) | String | The localized string key for the stackable version of the status effect's tooltip. | 69 |  |
| [`alias`](./Enums.md#enum-alias) | Enum | Specifies an alias keyword for referencing this status effect in tooltips or logic. | 57 |  |
| [`tooltip_stacks_singular`](./Strings.md#string-tooltip_stacks_singular) | String |  | 15 |  |
| [`tooltip_stacks_neg`](./Strings.md#string-tooltip_stacks_neg) | String | The localization key for the tooltip description when the status has negative stacks. | 13 |  |
| [`name_stacks_neg`](./Strings.md#string-name_stacks_neg) | String | The localization key for the tooltip name when the status has negative stacks. | 11 |  |
| [`tooltip_stacks_pos`](./Strings.md#string-tooltip_stacks_pos) | String | The localization key for the tooltip description when the status has positive stacks. | 10 |  |
| [`name_reference_applier`](./Strings.md#string-name_reference_applier) | String | The localized string key for the name of the unit that applied this status effect. | 3 |  |
| [`tooltip_reference_applier`](./Strings.md#string-tooltip_reference_applier) | String | The localized string key for the tooltip description of the unit that applied this status effect. | 3 |  |
| [`tooltip_stackless_neg`](./Strings.md#string-tooltip_stackless_neg) | String | The localization key for the tooltip description when the status has no stacks and is negative. | 3 |  |
| [`tooltip_stackless_pos`](./Strings.md#string-tooltip_stackless_pos) | String | The localization key for the tooltip description when the status has no stacks and is positive. | 2 |  |

</details>

---

