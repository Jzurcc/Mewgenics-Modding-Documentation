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
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |
| [`tooltip_stackless`](./Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 76 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `icon_frame` | Integer | The sprite frame index for the buff icon. | 74 | `141`<br>`148`<br>`149` |
| [`tooltip_stacks`](./Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 69 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`alias`](./Enums.md#enum-alias) | Enum | Specifies the reference name of another status effect to alias or copy properties from. | 57 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [`tooltip_stacks_singular`](./Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 15 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |
| [`tooltip_stacks_neg`](./Strings.md#string-tooltip_stacks_neg) | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. | 13 | `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| [`name_stacks_neg`](./Strings.md#string-name_stacks_neg) | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. | 11 | `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stacks_pos`](./Strings.md#string-tooltip_stacks_pos) | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. | 10 | `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |
| [`name_reference_applier`](./Strings.md#string-name_reference_applier) | String | A localization key for the name displayed to the applier of this status effect. | 3 | `"KEYWORD_ATTRACTION_REF"`<br>`"KEYWORD_LEECHES_NAME_APPLIER"`<br>`"KEYWORD_MANALEECHES_NAME_APPLIER"` |
| [`tooltip_reference_applier`](./Strings.md#string-tooltip_reference_applier) | String | A localization key for the tooltip description displayed to the applier of this status effect. | 3 | `"KEYWORD_ATTRACTION_DESC_REF"`<br>`"KEYWORD_LEECHES_DESC_APPLIER"`<br>`"KEYWORD_MANALEECHES_DESC_APPLIER"` |
| [`tooltip_stackless_neg`](./Strings.md#string-tooltip_stackless_neg) | String | Localization key for the tooltip of the negative variant when not showing stack count. | 3 | `"KEYWORD_DAMAGEDOWN_DESC_STACKLESS"`<br>`"KEYWORD_MOVEMENTDOWN_DESC_STACKLESS"`<br>`"KEYWORD_TEMPINITDOWN_DESC"` |
| [`tooltip_stackless_pos`](./Strings.md#string-tooltip_stackless_pos) | String | Localization key for the tooltip of the positive variant when not showing stack count. | 2 | `"KEYWORD_DAMAGEUP_DESC_STACKLESS"`<br>`"KEYWORD_MOVEMENTUP_DESC_STACKLESS"` |

</details>


---