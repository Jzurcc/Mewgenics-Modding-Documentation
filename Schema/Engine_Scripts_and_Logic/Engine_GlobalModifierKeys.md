---
title: "Global Modifier Keys Schema"
description: "Global state flags affecting the entire run."
---

# Global Modifier Keys Schema


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
> This schema affects run-wide variables, often used by high-level difficulty settings or sweeping modifiers like double health.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
HardMode {
    global_enemy_hp_multiplier 1.5
    global_gold_drops 0.5
}
```

---



## Engine: Global Modifier IDs

This document lists every confirmed Global Modifier ID. These are game-state flags that affect the entire battle or run (e.g. `BloodRain`, `NoCorpses`, `LowerAmbientLight`). Used as keys in `CreateGlobalModifiers {}`.

> **Referenced by:** [`CreateGlobalModifiers` (Abilities_and_Spells)](../Core_Entities_and_Combat/Abilities_and_Spells.md#object-createglobalmodifiers), [`CreateGlobalModifiers` (Characters_and_Bosses)](../Core_Entities_and_Combat/Characters_and_Bosses.md#object-createglobalmodifiers), [`global_passives` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-global_passives), [`CreateGlobalModifiers` (Items_and_Equipment)](../Core_Entities_and_Combat/Items_and_Equipment.md#object-createglobalmodifiers)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CreateGlobalModifiers`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 5 | `{ . . . }` |
| [`BloodRain`](./Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object  | If non-zero, enables the blood rain visual effect. | 9 | `{ . . . }`<br>`1` |
| `NextPlayerCatTakesExtraTurn` | Integer | The number of extra turns the active player cat gains. | 1 | `1` |
| `NoCorpses` | Integer | If set to 1, corpses are prevented from spawning. | 2 | `1` |

</details>

### Valid Nested Objects

The following objects all behave as `{Global Modifier Keys}` containers. Each has its own unique parameters listed below its entry.


---


#### `CreateGlobalModifiers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`LowerAmbientLight`](./Engine_GlobalModifierKeys.md#object-lowerambientlight) | Object  | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 7 | `{ . . . }` |
| [`BloodRain`](./Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object  | If non-zero, enables the blood rain visual effect. | 9 | `{ . . . }`<br>`1` |

</details>
## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.


### Object: `LowerAmbientLight`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `speed` | Array / Float  | The speed of the projectile or move, can be a value or a range. | 3 | `-30`<br>`-4`<br>`.5` |
| `amount` | Array / Float | For ambient light, the target brightness value (as a float or percentage array for RGB). | 3 | `.1`<br>`.25`<br>`.35` |
### Object: `BloodRain`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](../Reference_and_Meta/Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](../World_Maps_and_Events/Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`template`](../Reference_and_Meta/Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`cost`](../Reference_and_Meta/Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](../Reference_and_Meta/Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| [`movieclip`](../Reference_and_Meta/Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`render_mode`](../Reference_and_Meta/Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| `emit_rate` | Float | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `particle_lifetime` | Float | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| [`simulation_space`](../Reference_and_Meta/Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| [`projection_matrix`](../Reference_and_Meta/Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| [`emit_direction`](../Reference_and_Meta/Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `speed_start` | Float | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| [`live_bounds`](../Reference_and_Meta/Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`scripts`](../Reference_and_Meta/Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `size_start` | Array / Float | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`emit_box`](../Reference_and_Meta/Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| `speed_scale` | Float | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| [`force`](../Reference_and_Meta/Arrays.md#array-force) | Array  | The force vector applied to particles. | 1 | `0`<br>`1`<br>`1.5` |
| `alpha` | Float | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.005`<br>`.01`<br>`.03` |

