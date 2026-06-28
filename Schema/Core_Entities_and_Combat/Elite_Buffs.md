---
title: "Elite Buffs Schema"
description: "Defines modifiers applied to elite enemy variants."
---

# Elite Buffs Schema


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
> This schema determines how standard enemies are modified when they spawn as an "Elite", including stat multipliers and bonus abilities.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
Spiky {//animated spikes
	value 1
	icon_frame 500
	passives {
		EliteParticle SpikeBuff
		Thorns 2
		EliteTint [.6 .6 .6 .50]
	}
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Elite_Buffs.md`](../../Directory/Enemies_and_Combat/Elite_Buffs.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Elite Buffs

> **Associated Files:** `data/elite_buffs.gon, data/boss_elite_buffs.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 54

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 54 | passives<br>class<br>tag |
| `value` | Float | The numeric value or formula associated with the buff. | 54 | `.5`<br>`0`<br>`1` |
| `icon_frame` | Integer | The sprite frame index for the buff icon. | 54 | `141`<br>`148`<br>`149` |
| `unique` | Boolean | If true, this buff can only appear once per unit. | 36 | `true` |
| `specific_chapter` | Integer | The chapter in which this buff is exclusive to. | 8 | `1`<br>`2`<br>`3` |
| [`minion_alt`](../Reference_and_Meta/Enums.md#enum-minion_alt) | Enum | The alternative minion type to spawn for this buff. | 5 | `SlightlyDepressing`<br>`SubTwin`<br>`SubUndying` |
| `rollable` | Boolean | If false, this buff cannot be randomly rolled onto enemies. | 5 | `false` |
| `only_at_battle_start` | Boolean | If true, this buff only applies at the start of battle. | 2 | `true` |
| `requires_corpse` | Boolean | If true, this buff requires a corpse to function. | 2 | `true` |
| `roll_limit` | Integer | The maximum number of times this buff can be rolled. | 2 | `2` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `passives`


**Definition:** A container object listing passive effects granted to the unit.  
**Total Count:** 2807

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](./Elite_Buffs.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 54 | passives<br>class<br>tag |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |
`damage_instance`<br>`spell`<br>`self_damage`

</details>


---


### Object: `effects`


**Definition:** Applies a list of status effects or visual effects to targets.  
**Total Count:** 2166

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`DamageNeighborsAfterMove`](./Elite_Buffs.md#object-damageneighborsaftermove), [`MeleeRevengeDamage`](./Elite_Buffs.md#object-meleerevengedamage), [`RevengeDamage`](./Elite_Buffs.md#object-revengedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


---


### Object: `AddStatusToBasicAttack`


**Definition:** Contains status effects to add to the basic attack.  
**Total Count:** 248

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `MeleeRevengeDamage`


**Definition:** Defines the damage and effects applied back to a melee attacker upon being hit.  
**Total Count:** 73

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 3 | `damage_instance`<br>`spell`<br>`false` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 3 | `{ . . . }` |
| `knockback` | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 2 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |`damage_instance`<br>`spell`<br>`self_damage`

</details>


---


### Object: `StatusEachTurnEnd`


**Definition:** Specifies status effects applied to the unit at the end of each of its turns.  
**Total Count:** 57

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |

</details>


---


### Object: `SpawnOnBattleStart`


**Definition:** Specifies the object that spawns adjacent to the unit at the start of battle.  
**Total Count:** 54

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`prevent_chain_tag`](../Reference_and_Meta/Enums.md#enum-prevent_chain_tag) | Enum | A tag that prevents chaining of spawns from the same source. | 2 | `ancestorset_shade`<br>`eb_twin`<br>`minime_clone` |

</details>


---


### Object: `StatusOnKill`


**Definition:** Specifies status effects or actions triggered when the unit kills an enemy.  
**Total Count:** 40

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `RevengeDamage`


**Definition:** An object defining the damage and effects that trigger when the unit is attacked.  
**Total Count:** 31

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


### Object: `ReflectProjectiles`


**Definition:** The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `statuses`


**Definition:** Defines the status effects applied when the parent trigger event occurs.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ChanceToRevive`](./Elite_Buffs.md#object-chancetorevive)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Zombie` | Number | The number of stacks or value for the Zombie status. | 2 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |

</details>


---


### Object: `DepressionAura`


**Definition:** The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `range` | Integer | The distance in tiles for the trigger effect; `global` means any distance. | 4 | `1`<br>`10`<br>`2` |
| `aura_effects_allies` | Boolean | If false, the aura does not affect allies. | 4 | `false` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 4 | `{ . . . }` |

</details>


---


### Object: `StatusOnDie`


**Definition:** Specifies status effects or actions triggered when the unit dies.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `ChanceToRevive`


**Definition:** The percentage chance or an object defining chance, health, and statuses on revival.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 2 | `0`<br>`1`<br>`10` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`statuses`](./Elite_Buffs.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 2 | `{ . . . }` |

</details>


---


### Object: `StatusEachRoundBegin`


**Definition:** Applies the contained status effects at the beginning of each round.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>tag |

</details>


---


### Object: `DamageNeighborsAfterMove`


**Definition:** Defines the spell damage and effects applied to neighboring tiles after the unit moves.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`false` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |

</details>


---


### Object: `StatusEachRoundEnd`


**Definition:** An object listing status effects applied to the unit at the end of each round.  
**Total Count:** 3

<details>`damage_instance`<br>`spell`<br>`self_damage`
<summary><b>Expand</b></summary

> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


### Object: `StatusOnKill`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>


### Object: `StatusOnEnemyCastSpell`


**Definition:** Defines a status effect applied to the unit each time an enemy casts a spell.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary
`damage_instance`<br>`spell`<br>`self_damage`
> **Referenced by:** [`passives`](./Elite_Buffs.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---
### Object: `StatusOnDie`


<details>
<summary><b>Expand</b></summary>`damage_instance`<br>`spell`<br>`self_damage`

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `AddStatusToBasicAttack`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>
<details>`damage_instance`<br>`spell`<br>`self_damage`
<summary><b>StatusEachTurnEnd</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Damaging Keys}` | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 0 | `damage_instance`<br>`spell`<br>`false` |

</details>