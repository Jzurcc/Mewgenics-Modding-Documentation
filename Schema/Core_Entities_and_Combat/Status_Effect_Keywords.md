---
title: "Status Keywords Schema"
description: "Defines standard keywords for tooltips."
---

# Status Keywords Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

## Overview
> [!NOTE]
> This schema links specific status effects to tooltip text formats so players can easily read what an effect does when hovering over it.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
Adrenaline {
    name "KEYWORD_ADRENALINE_NAME"
    tooltip "KEYWORD_ADRENALINE_DESC"
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Status_Effect_Keywords.md`](../../Directory/Statuses_and_Injuries/Status_Effect_Keywords.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Status Effect Keywords

> **Associated Files:** `data/keyword_tooltips.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 236

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tooltip_stackless`](../Assets_and_Localization/Strings.md#string-tooltip_stackless) | String | A localization key for the tooltip description of this status effect when it has no stack count. | 76 | `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| [`tooltip_stacks`](../Assets_and_Localization/Strings.md#string-tooltip_stacks) | String | A localization key for the tooltip description of this status effect when displayed with its stack count. | 69 | `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| [`alias`](../Reference_and_Meta/Enums.md#enum-alias) | Enum | Specifies the reference name of another status effect to alias or copy properties from. | 57 | `AllStatsUp`<br>`Brace`<br>`Brittle` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 21 | `{ . . . }` |
| `icon_frame` | Integer | The sprite frame index for the buff icon. | 20 | `141`<br>`148`<br>`149` |
| [`tooltip_stacks_singular`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_singular) | String | The localization key for the singular form of the stack count in the tooltip. | 15 | `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |
| [`tooltip_stacks_neg`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_neg) | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. | 13 | `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| [`name_stacks_neg`](../Assets_and_Localization/Strings.md#string-name_stacks_neg) | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. | 11 | `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stacks_pos`](../Assets_and_Localization/Strings.md#string-tooltip_stacks_pos) | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. | 10 | `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |
| [`name_reference_applier`](../Assets_and_Localization/Strings.md#string-name_reference_applier) | String | A localization key for the name displayed to the applier of this status effect. | 3 | `"KEYWORD_ATTRACTION_REF"`<br>`"KEYWORD_LEECHES_NAME_APPLIER"`<br>`"KEYWORD_MANALEECHES_NAME_APPLIER"` |
| [`tooltip_reference_applier`](../Assets_and_Localization/Strings.md#string-tooltip_reference_applier) | String | A localization key for the tooltip description displayed to the applier of this status effect. | 3 | `"KEYWORD_ATTRACTION_DESC_REF"`<br>`"KEYWORD_LEECHES_DESC_APPLIER"`<br>`"KEYWORD_MANALEECHES_DESC_APPLIER"` |
| [`tooltip_stackless_neg`](../Assets_and_Localization/Strings.md#string-tooltip_stackless_neg) | String | Localization key for the tooltip of the negative variant when not showing stack count. | 3 | `"KEYWORD_DAMAGEDOWN_DESC_STACKLESS"`<br>`"KEYWORD_MOVEMENTDOWN_DESC_STACKLESS"`<br>`"KEYWORD_TEMPINITDOWN_DESC"` |
| [`tooltip_stackless_pos`](../Assets_and_Localization/Strings.md#string-tooltip_stackless_pos) | String | Localization key for the tooltip of the positive variant when not showing stack count. | 2 | `"KEYWORD_DAMAGEUP_DESC_STACKLESS"`<br>`"KEYWORD_MOVEMENTUP_DESC_STACKLESS"` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---