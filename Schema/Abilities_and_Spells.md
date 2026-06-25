# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Abilities & Spells

> **Associated Files:** `data/abilities/, data/ability_templates/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2343

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`graphics`](./Abilities_and_Spells.md#object-graphics) | Object | Object defining visual animations and sequence timings. | 5218 |
| [`meta`](./Abilities_and_Spells.md#object-meta) | Object | Object defining UI display data (Name, Description, Icon). | 4719 |
| [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance) | Object | Object defining the combat math and status effects applied upon successful hit. | 4688 |
| [`template`](./Enums.md#enum-template) | Enum | Inherits baseline internal logic from a hardcoded engine template. | 4348 |
| [`target`](./Abilities_and_Spells.md#object-target) | Object | Object defining the shape, range, and restrictions of the ability's aiming phase. | 3724 |
| [`cost`](./Abilities_and_Spells.md#object-cost) | Object | Object defining resource requirements (Mana, Act Points, Moves) needed to cast. | 3702 |
| [`variant_of`](./Enums.md#enum-variant_of) | Enum | Inherits properties from a previously defined ability (used for upgrading tiers). | 2364 |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 1200 |
| [`spawn`](./Abilities_and_Spells.md#object-spawn) | Object | Parameters for summoning new characters, objects, or entities. | 692 |
| [`self_damage`](./Abilities_and_Spells.md#object-self-damage) | Object | Recoil or self-inflicted damage/effects applied to the caster. | 436 |
| [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives) | Object | Passives granted to the character while this ability is equipped. | 272 |
| `durability` | Number | Consumes item durability. | 264 |
| [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects) | Object | Status applications that wear off automatically or at the end of the turn. | 176 |
| [`sounds`](./Abilities_and_Spells.md#object-sounds) | Object | Audio cues triggered by the ability. | 78 |
| [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage) | Object | Secondary Area of Effect blast parameters. | 68 |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 |
| [`keyword_tooltips`](./Abilities_and_Spells.md#object-keyword_tooltips) | Object | Forces specific UI tooltips to appear when hovering over the ability. | 62 |
| [`ai_ability`](./Enums.md#enum-ai_ability) | Enum | Overrides the ability used when triggered by AI. | 58 |
| [`chain_ability`](./Enums.md#enum-chain_ability) | Enum | An ability that automatically executes sequentially after this one. | 30 |
| [`sub_ability`](./Enums.md#enum-sub_ability) | Enum | A secondary ability component referenced by complex templates. | 16 |
| [`tags`](./Arrays.md#array-tags) | Array | Array of string categories used by the engine for filtering (e.g. [weapon_throw, spell]). | 8 |
| [`chapter`](./Engine_EventKeys.md#valid-property-keys) | Enum/String |  | 6 |
| [`cloned_ability`](./Enums.md#enum-cloned_ability) | Enum | Copies the properties of another ability dynamically. | 4 |
| [`empty_self_damage`](./Abilities_and_Spells.md#object-empty_self_damage) | Object | Recoil damage specifically applied when the attack misses all targets. | 4 |
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | Enum/String |  | 3 |
| [`bonk_damage`](./Abilities_and_Spells.md#object-bonk_damage) | Object | Damage dealt when knocked into a wall or obstacle. | 2 |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Object | The base damage properties of an attack. | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `damage_threshold_altanimations`


**Definition:** Triggers different hit animations based on the amount of damage dealt.  
**Total Count:** 1

<details>
<summary><b>Conditional_NotBoss</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 13 |

</details>

<details>
<summary><b>Conditional_FormulaIsPositive</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 8 |

</details>

<details>
<summary><b>Conditional_DestructibleCorpse</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

<details>
<summary><b>Conditional_OncePerBattle</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

<details>
<summary><b>LateStatusApplication</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 4 |

</details>

<details>
<summary><b>StatusKillers</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |

</details>

<details>
<summary><b>ApplyToRandomPartyMemberIfPossible</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>Conditional_Displaceable</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>Conditional_NotBossOrBig</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

<details>
<summary><b>XIsTargetHealth</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---


<details>
<summary><b>ApplyToOthersWithSharedTagAndFaction</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>Conditional_CanBeHealed</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>Conditional_FinishedSpawning</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>Conditional_IsSelf</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>Conditional_IsTrample</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>Conditional_NotBig</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>PassiveWhileNotTakingTurn</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |

</details>

<details>
<summary><b>Conditional_BossOrBig</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>Conditional_DebuffRoll</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#object-graphics)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `heaviestMelee` | Number | Animation trigger for massive damage. | 2 |
| `heavyMelee` | Number | Animation trigger if damage exceeds this threshold. | 2 |

</details>


---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

---

### Object: `additional_passives`


**Definition:** Passives granted intrinsically to a spawned entity.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#object-spawn)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhileNotTakingTurn`](./Abilities_and_Spells.md#object-passivewhilenottakingturn), [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `AfterImage`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the visual decoy to spawn (e.g., PlayerCat_ThiefShade). | 4 |
| `skilltemp` | Boolean | If true, the decoy is automatically destroyed once the skill finishes executing. | 4 |

</details>


### Object: `AlphaStatusOnTurnBegin`


**Definition:** Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyMultipleTimes`


**Definition:** A loop object that executes its nested logic multiple times.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | The number of times the nested effects block should be repeatedly executed. | 6 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyPassives`


**Definition:** Grants the nested passive abilities dynamically.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_RandomChance`](./Abilities_and_Spells.md#object-conditional_randomchance), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyPassivesToSpawnerWhileAlive`


**Definition:** Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyStatusesNextTurnBegin`


**Definition:** Delays the application of the nested status effects until the start of the target's next turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyStatusIfCrit`


**Definition:** Conditional trigger: Executes the nested logic only if the triggering action was a critical hit.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyToConsumed`


**Definition:** Redirects the nested effects to apply to the entity that just consumed this object.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeleteObject` | `Number` | Applies or references the 'DeleteObject' effect/state. | 6 |
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyToOthersWithSharedTagAndFaction`


**Definition:** Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>


### Object: `ApplyToRandomClosestAlly`


**Definition:** Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyToRandomPartyMemberIfPossible`


**Definition:** Redirects the nested effects to apply to a random living member of the player's party.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool_PostCast`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyToSource`


**Definition:** Redirects the nested effects to apply to the caster/source of the ability instead of the target.  
**Total Count:** 51

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#object-applystatusifcrit), [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional_goodroll), [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional_hasstatus), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional_healththreshold), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat), [`Conditional_PlayerCat`](./Abilities_and_Spells.md#object-conditional_playercat), [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#object-else), [`Math`](./Abilities_and_Spells.md#object-math), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `Enum/String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 8 |
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `Enum/String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 8 |
| [`AddWeaponAux`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'AddWeaponAux' effect/state. | 6 |
| [`Craft`](./Abilities_and_Spells.md#object-craft) | Object | Synthesizes or spawns a new item from a specific pool. | 6 |
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 6 |
| `AddLeechesStatus` | `Number` | Applies or references the 'AddLeechesStatus' effect/state. | 4 |
| `Cleanse` | `Number` | Applies or references the 'Cleanse' effect/state. | 4 |
| [`DoDamage`](./Abilities_and_Spells.md#object-dodamage) | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 4 |
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'RemoveStatus' effect/state. | 4 |
| `DisableWeapon` | `Number` | Applies or references the 'DisableWeapon' effect/state. | 2 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 2 |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 2 |
| `ManaGain` | `Number` | Applies or references the 'ManaGain' effect/state. | 2 |
| `RefreshMovePoints` | `Number` | Applies or references the 'RefreshMovePoints' effect/state. | 2 |
| [`SpecificInjury`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'SpecificInjury' effect/state. | 2 |
| `StanceSwitchToMelee` | `Number` | Applies or references the 'StanceSwitchToMelee' effect/state. | 2 |
| `StanceSwitchToRanged` | `Number` | Applies or references the 'StanceSwitchToRanged' effect/state. | 2 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 2 |
| `TempTrampleUntilSettled` | `Number` | Applies or references the 'TempTrampleUntilSettled' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyToSourceOnKill`


**Definition:** Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RemoveItem`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'RemoveItem' effect/state. | 6 |
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'CompleteItemQuest' effect/state. | 4 |
| `ManaGain` | `Number` | Applies or references the 'ManaGain' effect/state. | 4 |
| `Revive` | `Number` | Applies or references the 'Revive' effect/state. | 4 |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `Enum/String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 2 |
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 2 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 2 |
| [`TransformWeapon`](./Abilities_and_Spells.md#object-transformweapon) | Object | Transforms the equipped weapon into another specific weapon state. | 2 |
| [`WeaponAuxMultiplier`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'WeaponAuxMultiplier' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ApplyToTile`


**Definition:** Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#object-conditional_destructiblecorpse)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](./Abilities_and_Spells.md#object-objectonhit) | `Enum/String` | Spawns a specific physics/item object upon impact. | 4 |
| `SpawnBearTrap` | `Number` | Applies or references the 'SpawnBearTrap' effect/state. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ArcLightning`


**Definition:** Executes a chain-lightning logic block that bounces between targets.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc will not bounce to friendly targets. | 8 |
| `max_distance` | Number | The maximum tile range the lightning can jump between bounces. | 8 |
| `stacks` | Number | The maximum number of targets the lightning can bounce to. | 8 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |
| `ignore_self` | Boolean | If true, prevents the arc from bouncing back to the caster. | 2 |

</details>


### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to autocast. | 18 |
| `even_if_stunned` | Boolean | If true, bypasses stun and hard-CC restrictions to cast anyway. | 12 |

</details>


### Object: `BackflipWhenTargeted`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific dodge ability to trigger (e.g., DestroyerDodge). | 14 |
| `stacks` | Number | Number of stacks or intensity to apply. | 14 |

</details>


### Object: `BodyGuard`


**Definition:** Protects an ally by intercepting attacks directed at them.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The specific ability ID to use when intercepting (e.g., BodyGuardSwap). | 4 |
| `stacks` | Number | Number of stacks or intensity to apply. | 4 |

</details>


### Object: `bonk_damage`


**Definition:** Damage dealt when knocked into a wall or obstacle.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `bonus_passives`


**Definition:** Passives granted to the character while this ability is equipped.  
**Total Count:** 138

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `BounceObject`


**Definition:** Spawns a physics object that visually bounces off the target.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`obj`](./Enums.md#enum-obj) | Enum | The entity ID of the object to spawn (e.g., chapter_corpse_medium). | 6 |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) of spawning the object. | 4 |
| `slide` | Number |  | 2 |

</details>


### Object: `CanApplyToInanimate`


**Definition:** Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | Applies or references the 'BreakIntoRocks' effect/state. | 8 |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 6 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 6 |
| `GetAggroTarget` | Number | Applies or references the 'GetAggroTarget' effect/state. | 4 |
| `PreventDeathTransforms` | Number | Applies or references the 'PreventDeathTransforms' effect/state. | 2 |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `CatPartsSizeScaleStatus`


**Definition:** Visually scales specific body parts of a character.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | Scale multiplier for the front arm. | 2 |
| `arm2` | Number | Scale multiplier for the back arm. | 2 |
| `body` | Number |  | 2 |
| `mouth` | Number |  | 2 |

</details>


### Object: `CatPartsTransform`


**Definition:** Transforms specific body parts into different visual variants.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `palette` | Number |  | 34 |
| `ear1` | Number | Sprite variant ID for the front ear. | 26 |
| `tail` | Number | Sprite variant ID for the tail. | 26 |
| `arm2` | Number |  | 22 |
| `arm1` | Number | Sprite variant ID for the front arm. | 20 |
| `ear2` | Number |  | 20 |
| `leg1` | Number | Sprite variant ID for the front leg. | 16 |
| `leg2` | Number |  | 16 |
| `mouth` | Number |  | 16 |
| `head` | Number | Sprite variant ID for the head. | 12 |
| `texture` | Number |  | 12 |
| `body` | Number | Sprite variant ID for the body. | 10 |
| `eye1` | Number |  | 6 |
| `eye2` | Number |  | 6 |
| `eyebrow1` | Number |  | 2 |
| `eyebrow2` | Number |  | 2 |

</details>


### Object: `ChanceToBreakFree`


**Definition:** Provides a probability to escape a grapple or restraining effect.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ability triggered upon successfully breaking free. | 22 |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum | The ability triggered if the break free attempt fails. | 6 |
| `stacks` | Number | Percentage base chance to break free. | 6 |

</details>


### Object: `ChangeTile`


**Definition:** Transforms the terrain tile under the target.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tile`](./Arrays.md#array-tile) | Array | The specific tile type to change into (e.g., GlassTile). | 22 |
| `aoe` | Number |  | 4 |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Probability (0.0 to 1.0 or percentage) of this occurring. | 4 |

</details>


### Object: `Cleave`


**Definition:** No definition provided.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0) that the cleave effect triggers. | 2 |

</details>


### Object: `CollectsPickupsWithAltEffects`


**Definition:** Triggers alternative nested effects when collecting items or pickups.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponAddPoison` | Number | Applies or references the 'CurrentWeaponAddPoison' effect/state. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_ActiveWeather_Any`


**Definition:** Conditional trigger: Executes nested logic if the current map weather matches any in the list.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weather`](./Arrays.md#array-weather) | Array | An array of weather states to check against. | 1 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_AffectedByElement`


**Definition:** Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional-healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 7 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. | 6 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_Ally`


**Definition:** Conditional trigger: Executes nested logic if the target is friendly to the caster.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional-enemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 44 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 8 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 6 |
| `KnockbackDamageImmuneUntilSettled` | `Number` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 6 |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 6 |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 4 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 2 |
| `ChanceToBreak` | `Number` | Applies or references the 'ChanceToBreak' effect/state. | 2 |
| [`Conditional_Corpse`](./Abilities_and_Spells.md#object-conditional-corpse) | Object | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 2 |
| [`Conditional_PlayerCat`](./Abilities_and_Spells.md#object-conditional-playercat) | Object | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 2 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 2 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 2 |
| `RepairAll` | `Number` | Applies or references the 'RepairAll' effect/state. | 2 |
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ShowText' effect/state. | 2 |
| `ThornsDamageImmuneUntilSettled` | `Number` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 2 |
| `TileDamageImmuneUntilSettled` | `Number` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_Backstab`


**Definition:** Conditional trigger: Executes nested logic if the attacker is positioned behind the target.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | `Number` | Applies or references the 'BonusCritChance' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Enum | The probability (0.0 to 1.0) of triggering the 'bad roll' failure state. | 16 |
| `DieViolently` | `Number` | Applies or references the 'DieViolently' effect/state. | 2 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_Boss`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 37 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional-hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 12 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional-speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 12 |
| [`Else`](./Abilities_and_Spells.md#object-else) | Object | Fallback object that executes if the preceding `Conditional_` block evaluated to false. | 8 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 8 |
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'RemoveStatus' effect/state. | 8 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional-healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 7 |
| [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional-object) | Object | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 6 |
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'VisualFX' effect/state. | 6 |
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | String | Applies or references the 'BonusDamage' effect/state. | 4 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional-displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |
| `ExplodeCharacter_NoDie` | `Number` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 2 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 2 |
| [`XIsTargetHealth`](./Abilities_and_Spells.md#object-xistargethealth) | Object | Math variable assignment: Evaluates X as the target's current health. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_BossOrBig`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>


### Object: `Conditional_Buddy`


**Definition:** Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional-hastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 47 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 37 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional-hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 20 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional-speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 12 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional-healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 7 |
| [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional-object) | Object | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 6 |
| [`extra_statuses`](./Abilities_and_Spells.md#object-extra-statuses) | Object | Additional generic status applications. | 4 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional-displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_CanBeHealed`


**Definition:** Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>


### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional-notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 16 |
| `Revive` | `Number` | Applies or references the 'Revive' effect/state. | 13 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 4 |
| [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional-enemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 2 |
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 2 |
| [`Conditional_FinishedSpawning`](./Abilities_and_Spells.md#object-conditional-finishedspawning) | Object | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_DebuffRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized debuff probability.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of applying the debuff. | 2 |

</details>


### Object: `Conditional_DestructibleCorpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyToTile`](./Abilities_and_Spells.md#object-applytotile) | Object | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 4 |
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_Displaceable`


**Definition:** Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_Enemy`


**Definition:** Conditional trigger: Executes nested logic if the target is hostile to the caster.  
**Total Count:** 44

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Corpse`](./Abilities_and_Spells.md#object-conditional_corpse), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional-healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 7 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional-notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 6 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 4 |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 2 |
| `BonusDamage` | `Number` | Applies or references the 'BonusDamage' effect/state. | 2 |
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 2 |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_Familiar`


**Definition:** Conditional trigger: Executes nested logic if the target is a familiar.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_FinishedSpawning`


**Definition:** Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Imprison`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'Imprison' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier to track this specific application. | 6 |
| [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object | Grants nested passives only while the character possesses the specified status. | 6 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_FormulaIsPositive`


**Definition:** Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formula`](./Math_Equations.md) | Equation | The math expression to evaluate. | 16 |
| [`OverrideKnockbackDamage`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'OverrideKnockbackDamage' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `odds` | Number | The probability (0.0 to 1.0) of triggering the 'good roll' success state. | 72 |
| [`GainDisorderFromPool_PostCast`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 14 |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object | Redirects the nested effects to apply to a random living member of the player's party. | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 |
| [`GainDisorder`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'GainDisorder' effect/state. | 2 |
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ImmediateUseAbility' effect/state. | 2 |
| `RefreshWeaponAbility` | `Number` | Applies or references the 'RefreshWeaponAbility' effect/state. | 2 |
| [`ShowText`](./Engine_LogicKeys.md#valid-property-keys) | `String` | Applies or references the 'ShowText' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_HasCleansableDebuffs`


**Definition:** Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GenericBuff` | `Number` | Applies or references the 'GenericBuff' effect/state. | 2 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_HasStatus`


**Definition:** Conditional trigger: Executes nested logic if the target currently has the specified status effect.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The specific status ID to check for. | 40 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 47

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | The specific string tag to check for. | 91 |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional-hastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 47 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 37 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional-hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 20 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional-notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 12 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional-speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 12 |
| `FloatingRockTrap` | `Number` | Applies or references the 'FloatingRockTrap' effect/state. | 12 |
| [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional-boss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 8 |
| `IgnoreDamage` | `Number` | Applies or references the 'IgnoreDamage' effect/state. | 8 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional-healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 7 |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 6 |
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ImmediateUseAbility' effect/state. | 6 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 4 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 4 |
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 4 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 4 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 2 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional-displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |
| [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional-inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 2 |
| `CrackMoonHead` | `Number` | Applies or references the 'CrackMoonHead' effect/state. | 2 |
| `DeleteObject` | `Number` | Applies or references the 'DeleteObject' effect/state. | 2 |
| `DisplaceTowardsSource` | `Number` | Applies or references the 'DisplaceTowardsSource' effect/state. | 2 |
| `FaceAway` | `Number` | Applies or references the 'FaceAway' effect/state. | 2 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 2 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 2 |
| [`PopAndSpawn`](./Abilities_and_Spells.md#object-popandspawn) | Object | Destroys the target and replaces it with a new spawned entity. | 2 |
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'RemoveStatus' effect/state. | 2 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 2 |
| `ScatterRandomPickups` | `Number` | Applies or references the 'ScatterRandomPickups' effect/state. | 2 |
| `SetKnockback` | `Number` | Applies or references the 'SetKnockback' effect/state. | 2 |
| [`UseAbility`](./Abilities_and_Spells.md#object-useability) | `Enum/String` | Forces the character or target to instantly use a specified ability. | 2 |
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_HealthThreshold`


**Definition:** Conditional trigger: Executes nested logic if the target's health falls below the specified threshold.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional_notboss), [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `threshold_flat` | Number | A flat numerical health value threshold. | 10 |
| [`SpawnThingIfHitKills`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'SpawnThingIfHitKills' effect/state. | 4 |
| `threshold_percent` | Number | A percentage-based health threshold (e.g. 50%). | 4 |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 |
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'BonusDamage' effect/state. | 2 |
| `CaptureFamiliar` | `Number` | Applies or references the 'CaptureFamiliar' effect/state. | 2 |
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 2 |
| `DieViolently` | `Number` | Applies or references the 'DieViolently' effect/state. | 2 |
| `FactionConversion` | `Number` | Applies or references the 'FactionConversion' effect/state. | 2 |
| `FlatLeech` | `Number` | Applies or references the 'FlatLeech' effect/state. | 2 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 2 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 2 |
| [`threshold_expr`](./Math_Equations.md) | Equation |  | 2 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_InForm`


**Definition:** Conditional trigger: Executes nested logic if the target is currently in the specified transformation form.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum | The specific form ID to check for. | 14 |
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `Enum/String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 10 |
| [`ForceImmediateMoveAndAttack`](./Abilities_and_Spells.md#object-forceimmediatemoveandattack) | Object | Forces the character to immediately move to a target and use a specified ability. | 2 |
| [`UseAbility`](./Abilities_and_Spells.md#object-useability) | `Enum/String` | Forces the character or target to instantly use a specified ability. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_IsSelf`


**Definition:** Conditional trigger: Executes nested logic if the target is the caster themselves.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_IsTrample`


**Definition:** Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetKnockback` | `Number` | Applies or references the 'SetKnockback' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_LastHit`


**Definition:** Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 4 |
| `BonusDamage` | `Number` | Applies or references the 'BonusDamage' effect/state. | 2 |
| [`DelayCastAbility`](./Abilities_and_Spells.md#object-delaycastability) | `Enum/String` | Queues an ability to be cast automatically after a certain delay or trigger. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_LivingPlayerCat`


**Definition:** Conditional trigger: Executes nested logic if the target is an alive player-controlled cat.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`extra_statuses`](./Abilities_and_Spells.md#object-extra-statuses) | Object | Additional generic status applications. | 4 |
| [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object | Grants nested passives only while the character possesses the specified status. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_NotAlly`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT friendly to the caster.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_NotBig`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT classified as large.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | `Number` | Applies or references the 'DisplaceTowardsSource' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_NotBoss`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT a Boss.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_NotBossOrBig`


**Definition:** Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>


### Object: `Conditional_NotShielded`


**Definition:** Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_Object`


**Definition:** Conditional trigger: Executes nested logic if the target is an inanimate object or furniture.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Engine_LogicKeys.md#valid-property-keys) | Enum/String | The specific string tag to check for. | 981 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 37 |
| [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional-boss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 21 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional-hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 20 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional-notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 16 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional-speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 12 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional-healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 7 |
| [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional-inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 7 |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional-hastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 6 |
| [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional-object) | Object | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 6 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 2 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional-displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_OncePerBattle`


**Definition:** Conditional trigger: Executes nested logic only once per encounter/battle.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`key`](./Enums.md#enum-key) | Enum |  | 6 |
| [`CompleteItemQuest`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'CompleteItemQuest' effect/state. | 4 |
| `TriggerGameEnding` | `Number` | Applies or references the 'TriggerGameEnding' effect/state. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_PlayerCat`


**Definition:** Conditional trigger: Executes nested logic if the target is a player-controlled cat.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ConjureRandomAbilityFromCat` | `Number` | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 4 |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 2 |
| `Cleanse` | `Number` | Applies or references the 'Cleanse' effect/state. | 2 |
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 2 |
| [`KnockOutClone`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'KnockOutClone' effect/state. | 2 |
| `T2CopyCat` | `Number` | Applies or references the 'T2CopyCat' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_RandomChance`


**Definition:** Conditional trigger: Executes nested logic based on a flat percentage random roll.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `odds` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 8 |
| [`ApplyPassives`](./Abilities_and_Spells.md#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 4 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_Shielded`


**Definition:** Conditional trigger: Executes nested logic if the target currently has a Shield status.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>


### Object: `Conditional_SourceAbilityHasTag`


**Definition:** Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_SourceHasStatus`


**Definition:** Conditional trigger: Executes nested logic if the caster currently has the specified status.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Conditional_Speculative`


**Definition:** A simulation object used by the AI to test hypothetical outcomes before committing to an action.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#object-conditional_affectedbyelement), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional-hastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 47 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 37 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional-hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 20 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional-speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 12 |
| [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional-object) | Object | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 6 |
| `IgnoreDamage` | `Number` | Applies or references the 'IgnoreDamage' effect/state. | 6 |
| `BonusDamageBasedOnDistance` | `Number` | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 4 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional-healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 4 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 2 |
| `CapDamage` | `Number` | Applies or references the 'CapDamage' effect/state. | 2 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional-displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |
| `RandomBonusDamage` | `Number` | Applies or references the 'RandomBonusDamage' effect/state. | 2 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ConjureBonusAbility`


**Definition:** Adds a temporary bonus ability to the character's hand/deck.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to conjure. | 4 |
| `upgraded` | Boolean | If true, conjures the upgraded version of the ability. | 4 |

</details>


### Object: `Consumed`


**Definition:** State object triggered when this object or entity is eaten/consumed by another character.  
**Total Count:** 18

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Ability triggered by the consumed entity while inside the consumer. | 34 |
| `force_contact` | `Boolean` | If true, enforces physical overlap. | 30 |
| `instant` | `Boolean` |  | 24 |
| [`mount_mode`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | If true, treats the consumption as riding/mounting instead of eating. | 24 |
| `do_not_pop_corpse` | `Boolean` |  | 22 |
| [`drop_on_death`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` |  | 22 |
| `wet` | `Boolean` |  | 16 |
| `drop_on_self_death` | `Boolean` |  | 6 |
| [`extra_statuses`](./Abilities_and_Spells.md#object-extra-statuses) | Object | Additional generic status applications. | 6 |
| `use_placeholder` | Boolean |  | 6 |
| [`drop_body_ability`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` |  | 2 |
| `kill_on_consume` | `Boolean` |  | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `CopySpells`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| `upgraded` | Boolean |  | 2 |

</details>


### Object: `cost`


**Definition:** Object defining resource requirements (Mana, Act Points, Moves) needed to cast.  
**Total Count:** 1853

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `mana` | Number | MP pool and how much it restores per turn. | 3210 |
| `infcantrip` | Boolean | Can be cast infinitely as long as costs are met. | 1620 |
| `cantrip` | Boolean | Does not end the turn when cast. | 1120 |
| `once_per_fight` | Mixed | Exhausts for the remainder of combat after one use. | 196 |
| `act_points` | Number | Consumes primary action points (default 1). | 172 |
| `move_points` | Number | Consumes movement points. | 118 |
| `prime` | Number | Requires a "priming" turn before it fires. | 60 |
| `allow_offmap_casts` | Boolean | Can be used while the character is hidden/removed from grid. | 44 |
| `cant_cast` | Mixed | Explicitly disables casting (used for passive-triggered only abilities). | 36 |
| [`charge`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Cooldown timers measured in turns. | 36 |
| `must_be_consuming` | Boolean | Requires the character to be eating/holding something. | 34 |
| `must_not_be_consuming` | Boolean | Cannot be holding/eating an entity. | 28 |
| `requires_reload` | Boolean | Must spend an action to reload before casting again. | 28 |
| `can_cast_while_dead` | Boolean | Usable by corpses (e.g., DeathRattle triggers). | 24 |
| [`cantrip_group`](./Enums.md#enum-cantrip_group) | Enum | Groups cantrips so using one exhausts the others. | 24 |
| `must_be_offmap` | Boolean | Requires the character to be hidden/dug underground. | 24 |
| `X_cant_be_zero` | Boolean | Applies or references the 'X_cant_be_zero' effect/state. | 22 |
| `disallow_cost_modification` | Boolean | Prevents passives from making this cheaper. | 18 |
| `coins` | Number | Consumes currency to cast. | 16 |
| `durability` | Number | Consumes item durability. | 16 |
| `main_turn_only` | Boolean | Cannot be cast during bonus or dispersed turns. | 16 |
| `requires_destructible_weapon` | Boolean | The equipped weapon must be breakable. | 16 |
| `requires_exact_character_aux` | Number | Hardcoded character specific lock. | 16 |
| `must_not_be_a_summon` | Boolean | Summons/Familiars cannot cast this. | 14 |
| `start_reloaded` | Boolean | Spawns with the ability pre-loaded. | 14 |
| `must_be_first_action` | Boolean | Can only be used at the very start of the turn. | 8 |
| `enabled_formula` | Mixed | Mathematical string required to be >0 to cast. | 6 |
| `must_be_first_nonmove_action` | Boolean | Can move first, but cannot use other abilities first. | 6 |
| `must_have_weapon` | Boolean | Requires a weapon equipped in the item slot. | 4 |
| `can_be_refreshed` | Boolean | Passives/Effects can reset this ability's cooldown. | 2 |
| `can_pay_over_multiple_turns` | Boolean | Allows channeling costs over time. | 2 |
| `can_self_refresh` | Boolean | The ability has mechanics to reset its own cooldown. | 2 |
| `damage_cant_be_zero` | Boolean | Requires the ability to have >0 calculated damage to cast. | 2 |
| `initial_charge` | Number | How many turns it starts on cooldown at battle start. | 2 |
| `manacost_cant_be_zero` | Boolean | Fails to cast if mana cost is reduced to 0. | 2 |
| `minimum_con` | Number | Stat thresholds required to cast. | 2 |
| `minimum_spd` | Number | Stat thresholds required to cast. | 2 |
| `require_default_size` | Boolean | 2x2 or altered characters cannot cast this. | 2 |
| `requires_attack_damage_threshold` | Number | Needs a certain amount of innate damage. | 2 |
| `requires_consumed_trinket` | Boolean | Must have eaten a specific item type. | 2 |
| `requires_empty_trinket` | Boolean | Must not have an accessory equipped. | 2 |
| `requires_hp_threshold` | Number | Must be below/above a certain health percentage. | 2 |
| `requires_weapon` | Boolean | Prerequisite: Must meet this condition. | 2 |

</details>


### Object: `Craft`


**Definition:** Synthesizes or spawns a new item from a specific pool.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 30 |
| [`slot`](./Enums.md#enum-slot) | Enum |  | 28 |
| `temporary` | Boolean |  | 8 |
| `works_with_tech` | Boolean |  | 8 |

</details>


### Object: `CreateGlobalModifiers`


**Definition:** Generates global map or encounter rules/modifiers.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BloodRain` | `Number` | Applies or references the 'BloodRain' effect/state. | 6 |
| [`LowerAmbientLight`](./Abilities_and_Spells.md#object-lowerambientlight) | Object | A visual effect that dims the map's lighting. | 6 |
| [`{Global Modifier Keys}`](./Engine_GlobalModifierKeys.md#valid-property-keys) | Boolean | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `damage`


**Definition:** The base damage properties of an attack.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 2 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 2 |

</details>


### Object: `damage_instance`


**Definition:** Object defining the combat math and status effects applied upon successful hit.  
**Total Count:** 2346

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 3574 |
| `damage` | Number | The base damage properties of an attack. | 2894 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 718 |
| [`knockback`](./Engine_DamagingKeys.md#valid-property-keys) | Mixed | The base physics pushing power (in tiles). | 508 |
| `ai_base_score` | Number | How highly the AI values using this ability. | 446 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 352 |
| `heal` | `Number` | Restores health instead of dealing damage. | 244 |
| `cant_miss` | `Boolean` | Guarantees the hit, bypassing dodge mechanics. | 220 |
| `incidentally_collects_pickups` | `Boolean` | Automatically grabs items in the AoE. | 206 |
| [`custom_additional_ai_weight`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` | Granular AI preference adjustments (e.g., `prefer_dont_move`). | 164 |
| `piercing` | `Boolean` | Ignores a percentage of target defense/armor. | 104 |
| `makes_contact` | `Boolean` | If false, explicitly avoids triggering contact-based passives. | 80 |
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` | Z-index targeting (e.g., `characters`, `self`). | 52 |
| [`blocked_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` | Base damage dealt if the attack is blocked. | 48 |
| [`raw_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` | Unmitigated, unscaled base numbers. | 44 |
| `crit_chance` | `Number` | Override for base critical hit probability. | 32 |
| `override_trample_damage` | `Boolean` | Custom damage value for trample moves. | 30 |
| `contact_requires_adjacency` | Boolean | Contact effects only trigger if standing next to the target. | 28 |
| `can_revive` | `Boolean` | Healing instance that can bring dead allies back to life. | 16 |
| `show_damage_on_0` | `Boolean` | Forces the "-0" floater text to appear. | 12 |
| `force_play_hit_animation` | `Boolean` | Forces the flinch animation even on 0 damage. | 10 |
| `blocked_multiplier` | `Number` | Multiplier applied when hitting a blocking target. | 8 |
| [`accuracy`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` | Hit chance modifier. | 6 |
| `can_collect_pickups` | `Boolean` | The damage instance can grab items on the ground. | 6 |
| `can_instapop` | `Boolean` | Allows the attack to instantly destroy specific weak entities. | 4 |
| `disallow_modifications` | `Boolean` | Prevents passives from altering this damage instance. | 4 |
| `force_no_contact` | `Boolean` | Bypasses all contact-based retaliation (Thorns, etc). | 4 |
| `non_lethal` | `Boolean` | Reduces target to 1 HP but will never kill. | 4 |
| [`raw_heal`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | Unmitigated, unscaled base numbers. | 4 |
| `two_way_contact` | `Boolean` | Both caster and target trigger contact effects on each other. | 4 |
| `damage_shield_only` | `Boolean` | Depletes shields but cannot harm base health. | 2 |
| [`faction`](./Enums.md#enum-faction) | Enum | Determines alignment (`enemies`, `cats`, `neutral`). | 2 |
| [`final_hit_bonus_damage`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` | Extra damage applied on the last hit of a multihit. | 2 |
| `force_adjacent_and_diagonal_contact` | `Boolean` | Treats diagonal hits as physical contact. | 2 |
| `force_no_knockback` | `Boolean` | Prevents the target from being pushed. | 2 |
| `hint_dont_lowgravboost` | `Boolean` | AI hint to ignore wind physics. | 2 |
| [`hit_animation_alt`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` | Custom flinch animation for the target. | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `DelayCastAbility`


**Definition:** Queues an ability to be cast automatically after a certain delay or trigger.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to cast later. | 2 |
| `lingering` | Boolean |  | 2 |
| `relative` | Boolean |  | 2 |

</details>


### Object: `DelayedWindCone`


**Definition:** Creates a delayed Area of Effect cone.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | Distance or area of effect in tiles. | 4 |
| `damage` | Number | The base damage properties of an attack. | 2 |

</details>


### Object: `DestroyEquipmentAndAttachParasite`


**Definition:** Removes an equipped item and replaces it with a parasite from a specified pool.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#object-conditional_activeweather_any), [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#object-conditional_debuffroll), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Probability (0.0 to 1.0 or percentage) of this occurring. | 8 |
| [`pool`](./Arrays.md#array-pool) | Array | The item pool to draw the parasite from. | 4 |

</details>


### Object: `DoDamage`


**Definition:** Explicitly triggers a secondary damage instance independent of the main attack.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Else`](./Abilities_and_Spells.md#object-else), [`post_spawn_statuses`](./Abilities_and_Spells.md#object-post_spawn_statuses)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The flat damage amount. | 14 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of the damage (e.g., spell, melee). | 14 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum |  | 8 |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 8 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `DoDistortionRing`


**Definition:** Creates a visual distortion ring effect on the screen.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number |  | 12 |
| `radius` | Number | Distance or area of effect in tiles. | 12 |
| `speed` | Number |  | 12 |

</details>


### Object: `DoScreenShake`


**Definition:** Triggers a camera screen shake effect.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number |  | 20 |
| [`time`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed |  | 20 |

</details>


### Object: `DustOnHit`


**Definition:** Spawns a specific particle or cloud object upon impact.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The ID of the object/particle to spawn. | 6 |

</details>


### Object: `DybbukPossessed`


**Definition:** Defines the abilities and behaviors available when possessing another entity.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum |  | 2 |
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum |  | 2 |

</details>


### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 0

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DoDamage`](./Abilities_and_Spells.md#object-dodamage), [`MeleeRevengeDamage`](./Abilities_and_Spells.md#object-meleerevengedamage), [`ROOT`](./Abilities_and_Spells.md#object-root), [`RevengeDamage`](./Abilities_and_Spells.md#object-revengedamage), [`bonk_damage`](./Abilities_and_Spells.md#object-bonk_damage), [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance), [`empty_self_damage`](./Abilities_and_Spells.md#object-empty_self_damage), [`self_damage`](./Abilities_and_Spells.md#object-self_damage), [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Engine_LogicKeys.md#valid-property-keys) | Enum/String | The entity tag to seek out. | 981 |
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | Enum/String | Transforms the character into a different state or form (e.g., Rage, HasCat). | 204 |
| `IgnoreSelf` | `Number` | Applies or references the 'IgnoreSelf' effect/state. | 150 |
| [`ChangeTile`](./Abilities_and_Spells.md#object-changetile) | `Enum/String` | Transforms the terrain tile under the target. | 124 |
| [`Else`](./Abilities_and_Spells.md#object-else) | Object | Fallback object that executes if the preceding `Conditional_` block evaluated to false. | 118 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 88 |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional-hastag) | Object | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. | 76 |
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'VisualFXTile' effect/state. | 72 |
| [`BounceObject`](./Abilities_and_Spells.md#object-bounceobject) | `Enum/String` | Spawns a physics object that visually bounces off the target. | 70 |
| [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional-enemy) | Object | Conditional trigger: Executes nested logic if the target is hostile to the caster. | 70 |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 68 |
| [`TransformAbility`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'TransformAbility' effect/state. | 56 |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 54 |
| [`ManaGain`](./Engine_LogicKeys.md#valid-property-keys) | String | Applies or references the 'ManaGain' effect/state. | 52 |
| [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional-ally) | Object | Conditional trigger: Executes nested logic if the target is friendly to the caster. | 50 |
| [`EvolveAbilityFromPool`](./Abilities_and_Spells.md#object-evolveabilityfrompool) | `Enum/String` | Upgrades or transforms an existing ability into a new one from the specified pool. | 42 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 42 |
| `CollectsPickups` | `Number` | Applies or references the 'CollectsPickups' effect/state. | 34 |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 34 |
| `OverrideKnockbackDamage` | `Number` | Applies or references the 'OverrideKnockbackDamage' effect/state. | 32 |
| [`Consumed`](./Abilities_and_Spells.md#object-consumed) | Object | State object triggered when this object or entity is eaten/consumed by another character. | 30 |
| `VaporizeCorpse` | `Number` | Applies or references the 'VaporizeCorpse' effect/state. | 30 |
| [`ChangeCatClass`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ChangeCatClass' effect/state. | 28 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 28 |
| `EndTurn` | `Number` | Applies or references the 'EndTurn' effect/state. | 28 |
| `FaceAway` | `Number` | Applies or references the 'FaceAway' effect/state. | 28 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 28 |
| `RefreshMovePoints` | `Number` | Applies or references the 'RefreshMovePoints' effect/state. | 28 |
| `TakeExtraTurn` | `Number` | Applies or references the 'TakeExtraTurn' effect/state. | 28 |
| [`TransformBasicAttack`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'TransformBasicAttack' effect/state. | 28 |
| [`CatPartsTransform`](./Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms specific body parts into different visual variants. | 26 |
| [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional-boss) | Object | Conditional trigger: Executes nested logic if the target is a Boss. | 26 |
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 26 |
| `Displace` | `Number` | Applies or references the 'Displace' effect/state. | 24 |
| [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 22 |
| [`ChanceToBreakFree`](./Abilities_and_Spells.md#object-chancetobreakfree) | Object | Provides a probability to escape a grapple or restraining effect. | 22 |
| [`DoScreenShake`](./Abilities_and_Spells.md#object-doscreenshake) | Object | Triggers a camera screen shake effect. | 22 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 22 |
| [`Conditional_FormulaIsPositive`](./Abilities_and_Spells.md#object-conditional-formulaispositive) | Object | Conditional trigger: Executes nested logic if the evaluated mathematical formula returns a value greater than 0. | 20 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional-speculative) | Object | A simulation object used by the AI to test hypothetical outcomes before committing to an action. | 20 |
| `PartialPurge` | `Number` | Applies or references the 'PartialPurge' effect/state. | 20 |
| `PurgeAll` | `Number` | Applies or references the 'PurgeAll' effect/state. | 20 |
| `RefreshActPoints` | `Number` | Applies or references the 'RefreshActPoints' effect/state. | 20 |
| [`VisualFX`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'VisualFX' effect/state. | 20 |
| [`ApplyPassives`](./Abilities_and_Spells.md#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 18 |
| `DeferVaporize` | `Number` | Applies or references the 'DeferVaporize' effect/state. | 18 |
| `SpawnCreep` | `Number` | Applies or references the 'SpawnCreep' effect/state. | 18 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 16 |
| `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. | 16 |
| `OverrideChainKnockback` | `Number` | Applies or references the 'OverrideChainKnockback' effect/state. | 16 |
| [`SpreadDisease`](./Abilities_and_Spells.md#object-spreaddisease) | Object | Provides a chance to transmit a disease status to adjacent targets. | 16 |
| [`ApplyStatusIfCrit`](./Abilities_and_Spells.md#object-applystatusifcrit) | Object | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 14 |
| `BramblesOnHit` | `Number` | Applies or references the 'BramblesOnHit' effect/state. | 14 |
| `ContextualHeal` | `Number` | Applies or references the 'ContextualHeal' effect/state. | 14 |
| `ForceAttack` | `Number` | Forces the character to execute an immediate attack. | 14 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 14 |
| `KnockbackDamageImmuneUntilSettled` | `Number` | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 14 |
| `ManaSteal` | `Number` | Applies or references the 'ManaSteal' effect/state. | 14 |
| `ClearStarving` | `Number` | Applies or references the 'ClearStarving' effect/state. | 12 |
| [`Conditional_Corpse`](./Abilities_and_Spells.md#object-conditional-corpse) | Object | Conditional trigger: Executes nested logic if the target is a dead body/corpse. | 12 |
| [`ConjureBonusAbility`](./Abilities_and_Spells.md#object-conjurebonusability) | `Enum/String` | Adds a temporary bonus ability to the character's hand/deck. | 12 |
| [`Craft`](./Abilities_and_Spells.md#object-craft) | Object | Synthesizes or spawns a new item from a specific pool. | 12 |
| [`DoDistortionRing`](./Abilities_and_Spells.md#object-dodistortionring) | Object | Creates a visual distortion ring effect on the screen. | 12 |
| `Metronome` | `Number` | Executes a random musical or metronome ability. | 12 |
| [`RemoveStatus`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'RemoveStatus' effect/state. | 12 |
| `SetDistanceDisplace` | `Number` | Applies or references the 'SetDistanceDisplace' effect/state. | 12 |
| `SetHealth` | `Number` | Applies or references the 'SetHealth' effect/state. | 12 |
| [`SpawnThingIfHitKills`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'SpawnThingIfHitKills' effect/state. | 12 |
| [`TeamCastAbility`](./Abilities_and_Spells.md#object-teamcastability) | `Enum/String` | Requires or involves multiple characters to execute the ability. | 12 |
| [`TwisterDisplaceWithDamage`](./Abilities_and_Spells.md#object-twisterdisplacewithdamage) | Object | A whirlwind effect that randomly displaces targets and deals damage. | 12 |
| [`CollectsPickupsWithAltEffects`](./Abilities_and_Spells.md#object-collectspickupswithalteffects) | Object | Triggers alternative nested effects when collecting items or pickups. | 10 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional-hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 10 |
| [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional-inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 10 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional-notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 10 |
| [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional-object) | Object | Conditional trigger: Executes nested logic if the target is an inanimate object or furniture. | 10 |
| [`Conditional_PlayerCat`](./Abilities_and_Spells.md#object-conditional-playercat) | Object | Conditional trigger: Executes nested logic if the target is a player-controlled cat. | 10 |
| `FillMana` | `Number` | Applies or references the 'FillMana' effect/state. | 10 |
| `FlatLeech` | `Number` | Applies or references the 'FlatLeech' effect/state. | 10 |
| `ForceMoveAway` | `Number` | Applies or references the 'ForceMoveAway' effect/state. | 10 |
| `ForceMoveTowards` | `Number` | Applies or references the 'ForceMoveTowards' effect/state. | 10 |
| `HitExplosion` | `Number` | Applies or references the 'HitExplosion' effect/state. | 10 |
| [`Imprison`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'Imprison' effect/state. | 10 |
| [`KnockbackDirectionIsFacingDirection`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. | 10 |
| `MonkStanceSwitch` | `Number` | Applies or references the 'MonkStanceSwitch' effect/state. | 10 |
| [`ObjectOnHit`](./Abilities_and_Spells.md#object-objectonhit) | `Enum/String` | Spawns a specific physics/item object upon impact. | 10 |
| [`ObjectOnHitEmpty`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ObjectOnHitEmpty' effect/state. | 10 |
| [`PopAndSpawn`](./Abilities_and_Spells.md#object-popandspawn) | `Enum/String` | Destroys the target and replaces it with a new spawned entity. | 10 |
| `Purge` | `Number` | Applies or references the 'Purge' effect/state. | 10 |
| `RefreshMovePointsIfHit` | `Number` | Applies or references the 'RefreshMovePointsIfHit' effect/state. | 10 |
| `Revive` | `Number` | Applies or references the 'Revive' effect/state. | 10 |
| `SafeDie` | `Number` | Applies or references the 'SafeDie' effect/state. | 10 |
| `SpawnBearTrap` | `Number` | Applies or references the 'SpawnBearTrap' effect/state. | 10 |
| `UpgradeRandomAbility` | `Number` | Applies or references the 'UpgradeRandomAbility' effect/state. | 10 |
| [`ApplyToConsumed`](./Abilities_and_Spells.md#object-applytoconsumed) | Object | Redirects the nested effects to apply to the entity that just consumed this object. | 8 |
| [`ArcLightning`](./Abilities_and_Spells.md#object-arclightning) | Object | Executes a chain-lightning logic block that bounces between targets. | 8 |
| [`BounceRock`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'BounceRock' effect/state. | 8 |
| [`Conditional_Familiar`](./Abilities_and_Spells.md#object-conditional-familiar) | Object | Conditional trigger: Executes nested logic if the target is a familiar. | 8 |
| [`EnableWeather`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'EnableWeather' effect/state. | 8 |
| `ExplosionIfHitSomething` | `Number` | Applies or references the 'ExplosionIfHitSomething' effect/state. | 8 |
| `FaceCamera` | `Number` | Applies or references the 'FaceCamera' effect/state. | 8 |
| [`LateStatusApplication`](./Abilities_and_Spells.md#object-latestatusapplication) | Object | Applies a status effect after all primary damage and effects have fully resolved. | 8 |
| `Reanimate` | `Number` | Applies or references the 'Reanimate' effect/state. | 8 |
| `RemoveActPoints` | `Number` | Applies or references the 'RemoveActPoints' effect/state. | 8 |
| `SendRock` | `Number` | Applies or references the 'SendRock' effect/state. | 8 |
| [`SpecificInjury`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'SpecificInjury' effect/state. | 8 |
| [`SwitchMusic`](./Abilities_and_Spells.md#object-switchmusic) | Object | Changes the background music track or layer during combat. | 8 |
| [`TakeBonusTurnWithStatus`](./Abilities_and_Spells.md#object-takebonusturnwithstatus) | Object | Grants the character an immediate extra turn while afflicted with specific statuses. | 8 |
| [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication) | Object | Delays the nested effects by a specified amount of real-time seconds. | 8 |
| [`UseAbility`](./Abilities_and_Spells.md#object-useability) | `Enum/String` | Forces the character or target to instantly use a specified ability. | 8 |
| `VaporizeInanimate` | `Number` | Applies or references the 'VaporizeInanimate' effect/state. | 8 |
| [`ApplyMultipleTimes`](./Abilities_and_Spells.md#object-applymultipletimes) | Object | A loop object that executes its nested logic multiple times. | 6 |
| [`CatPartsSizeScaleStatus`](./Abilities_and_Spells.md#object-catpartssizescalestatus) | Object | Visually scales specific body parts of a character. | 6 |
| [`CollideWithConsumed`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'CollideWithConsumed' effect/state. | 6 |
| [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#object-conditional-affectedbyelement) | Object | Conditional trigger: Executes nested logic if the target is currently afflicted by the specified element. | 6 |
| [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#object-conditional-firstapplicationthisturn) | Object | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. | 6 |
| [`Conditional_LastHit`](./Abilities_and_Spells.md#object-conditional-lasthit) | Object | Conditional trigger: Executes nested logic if this attack is the final hit of a multi-hit sequence. | 6 |
| `CorpseVaporizer` | `Number` | Applies or references the 'CorpseVaporizer' effect/state. | 6 |
| `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 6 |
| `DeleteObject` | `Number` | Applies or references the 'DeleteObject' effect/state. | 6 |
| `DestroyTrinket` | `Number` | Applies or references the 'DestroyTrinket' effect/state. | 6 |
| `DestroyWeapon` | `Number` | Applies or references the 'DestroyWeapon' effect/state. | 6 |
| `DestroyWeaponThrow` | `Number` | Applies or references the 'DestroyWeaponThrow' effect/state. | 6 |
| `Die` | `Number` | Applies or references the 'Die' effect/state. | 6 |
| `DisplaceTowardsSource` | `Number` | Applies or references the 'DisplaceTowardsSource' effect/state. | 6 |
| [`DoubleStatus`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'DoubleStatus' effect/state. | 6 |
| [`DustOnHit`](./Abilities_and_Spells.md#object-dustonhit) | Object | Spawns a specific particle or cloud object upon impact. | 6 |
| `ForceDisplace` | `Number` | Applies or references the 'ForceDisplace' effect/state. | 6 |
| `ForceMoveTowardsEnemies` | `Number` | Applies or references the 'ForceMoveTowardsEnemies' effect/state. | 6 |
| `InstantMaxHealthUp` | `Number` | Applies or references the 'InstantMaxHealthUp' effect/state. | 6 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 6 |
| `PlayBackground` | Number | Applies or references the 'PlayBackground' effect/state. | 6 |
| `PullSourceToTarget` | `Number` | Applies or references the 'PullSourceToTarget' effect/state. | 6 |
| `RefreshWeaponAbility` | `Number` | Applies or references the 'RefreshWeaponAbility' effect/state. | 6 |
| `RepairAll` | `Number` | Applies or references the 'RepairAll' effect/state. | 6 |
| `RepairOnKill` | `Number` | Applies or references the 'RepairOnKill' effect/state. | 6 |
| [`SetCrazyEyeBackgroundWeights`](./Abilities_and_Spells.md#object-setcrazyeyebackgroundweights) | Object | Adjusts visual rendering weights for the 'Crazy Eye' background effect. | 6 |
| [`SpawnCustomTrap`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'SpawnCustomTrap' effect/state. | 6 |
| `SpawnNeutralWebTrapOnMiss` | `Number` | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. | 6 |
| `SpawnRock` | `Number` | Applies or references the 'SpawnRock' effect/state. | 6 |
| `VaporizeTarget` | `Number` | Applies or references the 'VaporizeTarget' effect/state. | 6 |
| `AddSpiritBombCharges` | `Number` | Applies or references the 'AddSpiritBombCharges' effect/state. | 4 |
| `BonusKnockbackDamage` | `Number` | Applies or references the 'BonusKnockbackDamage' effect/state. | 4 |
| `Bound` | `Number` | Applies or references the 'Bound' effect/state. | 4 |
| `BurgleCoin` | `Number` | Applies or references the 'BurgleCoin' effect/state. | 4 |
| `CancelPrimedAbilities` | `Number` | Applies or references the 'CancelPrimedAbilities' effect/state. | 4 |
| [`ChangeFaction`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ChangeFaction' effect/state. | 4 |
| `CharmedForceAttack` | `Number` | Applies or references the 'CharmedForceAttack' effect/state. | 4 |
| `CollideWithThrowTarget` | `Number` | Applies or references the 'CollideWithThrowTarget' effect/state. | 4 |
| [`Conditional_BadRoll`](./Abilities_and_Spells.md#object-conditional-badroll) | Object | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 4 |
| [`Conditional_BossOrBig`](./Abilities_and_Spells.md#object-conditional-bossorbig) | Object | Conditional trigger: Executes nested logic if the target is a Boss or has a large size classification. | 4 |
| [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional-buddy) | Object | Conditional trigger: Executes nested logic if the target is the caster's summoned buddy/familiar. | 4 |
| [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#object-conditional-destructiblecorpse) | Object | Conditional trigger: Executes nested logic if the target is a corpse that can be destroyed or vaporized. | 4 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional-healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 4 |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#object-conditional-isself) | Object | Conditional trigger: Executes nested logic if the target is the caster themselves. | 4 |
| [`Conditional_NotAlly`](./Abilities_and_Spells.md#object-conditional-notally) | Object | Conditional trigger: Executes nested logic if the target is NOT friendly to the caster. | 4 |
| [`Conditional_NotBossOrBig`](./Abilities_and_Spells.md#object-conditional-notbossorbig) | Object | Conditional trigger: Executes nested logic if the target is NEITHER a Boss nor large. | 4 |
| [`Conditional_NotShielded`](./Abilities_and_Spells.md#object-conditional-notshielded) | Object | Conditional trigger: Executes nested logic if the target does NOT currently have a Shield status. | 4 |
| [`Conditional_OncePerBattle`](./Abilities_and_Spells.md#object-conditional-onceperbattle) | Object | Conditional trigger: Executes nested logic only once per encounter/battle. | 4 |
| [`Conditional_Shielded`](./Abilities_and_Spells.md#object-conditional-shielded) | Object | Conditional trigger: Executes nested logic if the target currently has a Shield status. | 4 |
| `CopySpells` | `Number` | Duplicates existing spells currently in the character's hand. | 4 |
| `Counterspell` | `Number` | Applies or references the 'Counterspell' effect/state. | 4 |
| `DamageBasedOnMissingHealth` | `Number` | Applies or references the 'DamageBasedOnMissingHealth' effect/state. | 4 |
| `DamageDistanceAOEFalloff` | `Number` | Applies or references the 'DamageDistanceAOEFalloff' effect/state. | 4 |
| `DamageTrinket` | `Number` | Applies or references the 'DamageTrinket' effect/state. | 4 |
| `DelayedFury` | `Number` | Applies or references the 'DelayedFury' effect/state. | 4 |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object | Removes an equipped item and replaces it with a parasite from a specified pool. | 4 |
| `DieViaAbilityInternally` | `Number` | Applies or references the 'DieViaAbilityInternally' effect/state. | 4 |
| `DisplaceToOriginalPosition` | `Number` | Applies or references the 'DisplaceToOriginalPosition' effect/state. | 4 |
| [`extra_statuses`](./Abilities_and_Spells.md#object-extra-statuses) | Object | Additional generic status applications. | 4 |
| `FlowersOnHit` | `Number` | Applies or references the 'FlowersOnHit' effect/state. | 4 |
| `ForceMoveNonAlliesInRangeTowardsTile` | `Number` | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. | 4 |
| [`ForceMoveTowardsTaggedObject`](./Abilities_and_Spells.md#object-forcemovetowardstaggedobject) | Object | Forces the character to move towards the nearest object with a specific tag. | 4 |
| `IgnoreDamage` | `Number` | Applies or references the 'IgnoreDamage' effect/state. | 4 |
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ImmediateUseAbility' effect/state. | 4 |
| [`ImmediateUseDirectionalAbility`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. | 4 |
| `JohnnyCriesForWashers` | `Number` | Applies or references the 'JohnnyCriesForWashers' effect/state. | 4 |
| `LeaveBehindRockOnKnockback` | `Number` | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 4 |
| [`LowerAmbientLight`](./Abilities_and_Spells.md#object-lowerambientlight) | Object | A visual effect that dims the map's lighting. | 4 |
| [`Math`](./Abilities_and_Spells.md#object-math) | Object | Triggers the Tinkerer's Math ability sequence. | 4 |
| `MaxHPUp` | `Number` | Applies or references the 'MaxHPUp' effect/state. | 4 |
| `NextAttackSpecialCrit` | `Number` | Modifies the character's next attack to have special critical properties. | 4 |
| [`OverHealToStatuses`](./Abilities_and_Spells.md#object-overhealtostatuses) | Object | Converts excessive healing beyond maximum health into specific status effects. | 4 |
| `PermanentStrength` | `Number` | Applies or references the 'PermanentStrength' effect/state. | 4 |
| `PermanentUpgradeRandomActive` | `Number` | Applies or references the 'PermanentUpgradeRandomActive' effect/state. | 4 |
| `PullSourceToKnockbackImmuneTarget` | `Number` | Applies or references the 'PullSourceToKnockbackImmuneTarget' effect/state. | 4 |
| [`QuakeAreaChance`](./Abilities_and_Spells.md#object-quakeareachance) | Object | Provides a probability to trigger an earthquake Area of Effect. | 4 |
| `RandomDistanceDisplace` | `Number` | Displaces the target by a randomized distance. | 4 |
| [`RandomKnockback`](./Abilities_and_Spells.md#object-randomknockback) | Object | Applies a randomized amount of knockback force. | 4 |
| `RebukeDamage` | `Number` | Applies or references the 'RebukeDamage' effect/state. | 4 |
| `RemoveMovePoints` | `Number` | Applies or references the 'RemoveMovePoints' effect/state. | 4 |
| `RepairArmorCondition` | `Number` | Applies or references the 'RepairArmorCondition' effect/state. | 4 |
| `RepairWeaponCondition` | `Number` | Applies or references the 'RepairWeaponCondition' effect/state. | 4 |
| `ResetArmorShield` | `Number` | Applies or references the 'ResetArmorShield' effect/state. | 4 |
| `ScatterHeldCoin` | `Number` | Applies or references the 'ScatterHeldCoin' effect/state. | 4 |
| `ScrambleEverything` | `Number` | Applies or references the 'ScrambleEverything' effect/state. | 4 |
| `SetShield` | `Number` | Applies or references the 'SetShield' effect/state. | 4 |
| `Shatter` | `Number` | Applies or references the 'Shatter' effect/state. | 4 |
| `SignalFinalBossShieldBroke` | `Number` | Applies or references the 'SignalFinalBossShieldBroke' effect/state. | 4 |
| `SmartMetronome` | `Number` | Executes a 'smart' random ability that aims to be beneficial based on context. | 4 |
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 4 |
| `StanceSwitchToMelee` | `Number` | Applies or references the 'StanceSwitchToMelee' effect/state. | 4 |
| `SwallowSmallCharacter` | `Number` | Applies or references the 'SwallowSmallCharacter' effect/state. | 4 |
| [`TakeBonusTurnWithAIControl`](./Abilities_and_Spells.md#object-takebonusturnwithaicontrol) | Object | Grants the character an immediate extra turn, but forces the AI to control them during it. | 4 |
| `TempTrampleUntilSettled` | `Number` | Applies or references the 'TempTrampleUntilSettled' effect/state. | 4 |
| `TradeLife` | `Number` | Applies or references the 'TradeLife' effect/state. | 4 |
| `TriggerDOTStatuses` | `Number` | Applies or references the 'TriggerDOTStatuses' effect/state. | 4 |
| [`TriggerWerewolfTransform`](./Engine_LogicKeys.md#valid-property-keys) | `Array` | Applies or references the 'TriggerWerewolfTransform' effect/state. | 4 |
| `AIFavorLowHealth` | `Number` | Applies or references the 'AIFavorLowHealth' effect/state. | 2 |
| `AlliesTakeExtraTurn` | `Number` | Applies or references the 'AlliesTakeExtraTurn' effect/state. | 2 |
| [`AlternateIdleAnimation`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'AlternateIdleAnimation' effect/state. | 2 |
| `ApplyShieldToApplierBasedOnMaxHealth` | `Number` | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. | 2 |
| [`ApplyStatusesNextTurnBegin`](./Abilities_and_Spells.md#object-applystatusesnextturnbegin) | Object | Delays the application of the nested status effects until the start of the target's next turn. | 2 |
| [`ApplyToOthersWithSharedTagAndFaction`](./Abilities_and_Spells.md#object-applytootherswithsharedtagandfaction) | Object | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. | 2 |
| [`ApplyToRandomClosestAlly`](./Abilities_and_Spells.md#object-applytorandomclosestally) | Object | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. | 2 |
| `BombRatTurtle` | `Number` | Applies or references the 'BombRatTurtle' effect/state. | 2 |
| `BonusDamageBasedOnMana` | `Number` | Applies or references the 'BonusDamageBasedOnMana' effect/state. | 2 |
| `BypassRockKnockback` | `Number` | Applies or references the 'BypassRockKnockback' effect/state. | 2 |
| `CanceledQueuedInput` | `Number` | Applies or references the 'CanceledQueuedInput' effect/state. | 2 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 2 |
| `ChaosBossFlipMidTeleport` | `Number` | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. | 2 |
| `ChaosBossFormChange` | `Number` | Applies or references the 'ChaosBossFormChange' effect/state. | 2 |
| `CharmedFacingForceAttack` | `Number` | Applies or references the 'CharmedFacingForceAttack' effect/state. | 2 |
| `ClearFinalBossBattlefield` | `Number` | Applies or references the 'ClearFinalBossBattlefield' effect/state. | 2 |
| `CloneWeaponTemp` | `Number` | Applies or references the 'CloneWeaponTemp' effect/state. | 2 |
| [`CoinTossBounce`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'CoinTossBounce' effect/state. | 2 |
| [`Conditional_AbilityTargetIsSelf`](./Engine_LogicKeys.md#valid-property-keys) | Object | Conditional constraint. Nested properties only trigger if this is true. | 2 |
| [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#object-conditional-activeweather-any) | Object | Conditional trigger: Executes nested logic if the current map weather matches any in the list. | 2 |
| [`Conditional_Backstab`](./Abilities_and_Spells.md#object-conditional-backstab) | Object | Conditional trigger: Executes nested logic if the attacker is positioned behind the target. | 2 |
| [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#object-conditional-canbehealed) | Object | Conditional trigger: Executes nested logic if the target's health is below maximum and they are capable of receiving healing. | 2 |
| [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#object-conditional-debuffroll) | Object | Conditional trigger: Executes nested logic based on a randomized debuff probability. | 2 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional-displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |
| [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#object-conditional-hascleansabledebuffs) | Object | Conditional trigger: Executes nested logic if the target currently has negative status effects that can be cleansed. | 2 |
| [`Conditional_IsTrample`](./Abilities_and_Spells.md#object-conditional-istrample) | Object | Conditional trigger: Executes nested logic if the current movement/attack is classified as a trample. | 2 |
| [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional-livingplayercat) | Object | Conditional trigger: Executes nested logic if the target is an alive player-controlled cat. | 2 |
| [`Conditional_NotBig`](./Abilities_and_Spells.md#object-conditional-notbig) | Object | Conditional trigger: Executes nested logic if the target is NOT classified as large. | 2 |
| [`Conditional_RandomChance`](./Abilities_and_Spells.md#object-conditional-randomchance) | Object | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 2 |
| [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional-sourceabilityhastag) | Object | Conditional trigger: Executes nested logic if the ability that triggered this effect has the specified tag. | 2 |
| [`Conditional_SourceHasStatus`](./Abilities_and_Spells.md#object-conditional-sourcehasstatus) | Object | Conditional trigger: Executes nested logic if the caster currently has the specified status. | 2 |
| [`ConjureSingleUseBonusAbility`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. | 2 |
| `CurrentWeaponAddElectricElement` | `Number` | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. | 2 |
| `DamageWeapon` | `Number` | Applies or references the 'DamageWeapon' effect/state. | 2 |
| [`DeathwormUnderground`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'DeathwormUnderground' effect/state. | 2 |
| `DecoySwapper` | `Number` | Applies or references the 'DecoySwapper' effect/state. | 2 |
| [`DelayCastAbility`](./Abilities_and_Spells.md#object-delaycastability) | Object | Queues an ability to be cast automatically after a certain delay or trigger. | 2 |
| [`DelayedWindCone`](./Abilities_and_Spells.md#object-delayedwindcone) | Object | Creates a delayed Area of Effect cone. | 2 |
| `DeleteTraps` | `Number` | Applies or references the 'DeleteTraps' effect/state. | 2 |
| `DestroyNeckArmor` | `Number` | Applies or references the 'DestroyNeckArmor' effect/state. | 2 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 2 |
| [`DinoLegAnimation`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'DinoLegAnimation' effect/state. | 2 |
| `Disguised` | `Number` | Applies or references the 'Disguised' effect/state. | 2 |
| `DissolveRandomArmorPiece` | `Number` | Applies or references the 'DissolveRandomArmorPiece' effect/state. | 2 |
| `DontHealEnemies` | `Number` | Applies or references the 'DontHealEnemies' effect/state. | 2 |
| `DoubleCastSpellsEachTurn_Status` | `Number` | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. | 2 |
| `DrainAllyCatsForFleshGolem` | `Number` | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. | 2 |
| `DuplicateRandomEquippedItem` | `Number` | Applies or references the 'DuplicateRandomEquippedItem' effect/state. | 2 |
| `Enlarge` | `Number` | Applies or references the 'Enlarge' effect/state. | 2 |
| [`EnterMount`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'EnterMount' effect/state. | 2 |
| `ExistUntilIdleUpkeep` | `Number` | Applies or references the 'ExistUntilIdleUpkeep' effect/state. | 2 |
| `ExplodeCharacter` | `Number` | Applies or references the 'ExplodeCharacter' effect/state. | 2 |
| `ExplodeCharacter_DeathBloom` | `Number` | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. | 2 |
| `ExplodeCharacter_DeathBloom2` | `Number` | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. | 2 |
| `ExplodeCharacter_NoDie` | `Number` | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 2 |
| `FactionConversion` | `Number` | Applies or references the 'FactionConversion' effect/state. | 2 |
| `FactionDisguiseSource` | `Number` | Applies or references the 'FactionDisguiseSource' effect/state. | 2 |
| `FastKnockback` | `Number` | Applies or references the 'FastKnockback' effect/state. | 2 |
| `FinalBossQueueBeam` | `Number` | Applies or references the 'FinalBossQueueBeam' effect/state. | 2 |
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 2 |
| `ForceCollectsPickups` | `Number` | Applies or references the 'ForceCollectsPickups' effect/state. | 2 |
| `ForceMoveAndAttack` | `Number` | Applies or references the 'ForceMoveAndAttack' effect/state. | 2 |
| `ForceTransferWeapon` | `Number` | Applies or references the 'ForceTransferWeapon' effect/state. | 2 |
| `GenericBuff` | `Number` | Applies or references the 'GenericBuff' effect/state. | 2 |
| `GiveBoundItemToTarget` | `Number` | Applies or references the 'GiveBoundItemToTarget' effect/state. | 2 |
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | Enum/String | Applies or references the 'GlobalSpawnCharacter' effect/state. | 2 |
| `HealPercentMaxHP` | `Number` | Applies or references the 'HealPercentMaxHP' effect/state. | 2 |
| `HealTo` | `Number` | Applies or references the 'HealTo' effect/state. | 2 |
| `IgnoreDebuffs` | `Number` | Applies or references the 'IgnoreDebuffs' effect/state. | 2 |
| [`IncAuxCounterCycle`](./Abilities_and_Spells.md#object-incauxcountercycle) | Object | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. | 2 |
| `IncreaseCumulativeBlastDamage` | `Number` | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. | 2 |
| `IncreaseItemAuxOnKill` | `Number` | Applies or references the 'IncreaseItemAuxOnKill' effect/state. | 2 |
| `InterchangeMoveActPoints` | `Number` | Applies or references the 'InterchangeMoveActPoints' effect/state. | 2 |
| `MadnessChanceOnTurnBegin` | Number | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 2 |
| `MakeWeaponUnbreakable` | `Number` | Applies or references the 'MakeWeaponUnbreakable' effect/state. | 2 |
| `ManaStealToHealth` | `Number` | Applies or references the 'ManaStealToHealth' effect/state. | 2 |
| `ManglerAttack` | `Number` | Applies or references the 'ManglerAttack' effect/state. | 2 |
| `ManglerShuffle` | `Boolean` | Applies or references the 'ManglerShuffle' effect/state. | 2 |
| `MassAttackThis` | `Number` | Applies or references the 'MassAttackThis' effect/state. | 2 |
| `MimicMetronome` | `Number` | Applies or references the 'MimicMetronome' effect/state. | 2 |
| `MotherTumorDebugForcePass` | `Number` | Applies or references the 'MotherTumorDebugForcePass' effect/state. | 2 |
| [`NextBasicAttackCritsThisTurn`](./Abilities_and_Spells.md#object-nextbasicattackcritsthisturn) | Object | Guarantees the next basic attack executed this turn will be a critical hit. | 2 |
| [`NextBattleStatusStacks`](./Abilities_and_Spells.md#object-nextbattlestatusstacks) | Object | Carries over the specified status effects into the next encounter/battle. | 2 |
| [`ObjectOnHitFullyEmpty`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. | 2 |
| `OverHealToShield` | `Number` | Applies or references the 'OverHealToShield' effect/state. | 2 |
| [`OverrideChainKnockbackDamage`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'OverrideChainKnockbackDamage' effect/state. | 2 |
| `PermanentCharisma` | `Number` | Applies or references the 'PermanentCharisma' effect/state. | 2 |
| `PermanentLuck` | `Number` | Applies or references the 'PermanentLuck' effect/state. | 2 |
| `PermanentUpgradeRandomActiveOrPassive` | `Number` | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. | 2 |
| [`PoolMetronome`](./Abilities_and_Spells.md#object-poolmetronome) | Object | Executes a random ability drawn from a specific pool. | 2 |
| [`QueueUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'QueueUseAbility' effect/state. | 2 |
| `RandomKnockbackDirection` | `Number` | Applies or references the 'RandomKnockbackDirection' effect/state. | 2 |
| `RandomStatDown` | Number | Applies or references the 'RandomStatDown' effect/state. | 2 |
| `ReformMoonHead` | `Number` | Applies or references the 'ReformMoonHead' effect/state. | 2 |
| `RefreshItemAbilities` | `Number` | Applies or references the 'RefreshItemAbilities' effect/state. | 2 |
| `RefreshNonManaItemAbilities` | `Number` | Applies or references the 'RefreshNonManaItemAbilities' effect/state. | 2 |
| `RefreshOncePerFightAbilities` | `Number` | Applies or references the 'RefreshOncePerFightAbilities' effect/state. | 2 |
| `Regurge` | `Number` | Applies or references the 'Regurge' effect/state. | 2 |
| [`RemoveStatusStacks`](./Abilities_and_Spells.md#object-removestatusstacks) | Object | Removes a specific number of stacks of a status effect. | 2 |
| `RepairAllCondition` | `Number` | Applies or references the 'RepairAllCondition' effect/state. | 2 |
| `RerollEnemy` | `Number` | Applies or references the 'RerollEnemy' effect/state. | 2 |
| `ReturnDinoLegs` | `Number` | Applies or references the 'ReturnDinoLegs' effect/state. | 2 |
| `RNGCannonRandomDamage` | `Number` | Applies or references the 'RNGCannonRandomDamage' effect/state. | 2 |
| `ScatterRandomPickups` | `Number` | Applies or references the 'ScatterRandomPickups' effect/state. | 2 |
| [`ScrambleLastUsedSpell`](./Abilities_and_Spells.md#object-scramblelastusedspell) | Object | Randomizes or scrambles the properties of the last spell cast. | 2 |
| `SelfStun` | `Number` | Applies or references the 'SelfStun' effect/state. | 2 |
| `ShadowCrit` | `Number` | Applies or references the 'ShadowCrit' effect/state. | 2 |
| `ShootHereCommand` | `Number` | Applies or references the 'ShootHereCommand' effect/state. | 2 |
| `ShootHereReceiver` | `Number` | Applies or references the 'ShootHereReceiver' effect/state. | 2 |
| `SmallHitExplosion` | `Number` | Applies or references the 'SmallHitExplosion' effect/state. | 2 |
| `SmellBlood` | `Number` | Applies or references the 'SmellBlood' effect/state. | 2 |
| [`SoundEventOnHit`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'SoundEventOnHit' effect/state. | 2 |
| [`SourceSwapsBackEndOfTurn`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. | 2 |
| `SpawnWebTrap` | `Number` | Applies or references the 'SpawnWebTrap' effect/state. | 2 |
| [`SpecialBossMultipartInstakill`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'SpecialBossMultipartInstakill' effect/state. | 2 |
| `SpitConsumed` | `Number` | Applies or references the 'SpitConsumed' effect/state. | 2 |
| `SplashDamage` | `Number` | Applies or references the 'SplashDamage' effect/state. | 2 |
| `StackingSandstorm` | `Number` | Applies or references the 'StackingSandstorm' effect/state. | 2 |
| `StealDemonicGlyph` | `Number` | Applies or references the 'StealDemonicGlyph' effect/state. | 2 |
| [`StealEquipment`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'StealEquipment' effect/state. | 2 |
| `StealthCritChance` | `Number` | Applies or references the 'StealthCritChance' effect/state. | 2 |
| `StealTurn` | `Number` | Applies or references the 'StealTurn' effect/state. | 2 |
| `SwapHighestAndLowestStat` | `Number` | Applies or references the 'SwapHighestAndLowestStat' effect/state. | 2 |
| [`SwapWeapon`](./Abilities_and_Spells.md#object-swapweapon) | Object | Replaces the character's currently equipped weapon with one from a specified pool. | 2 |
| `T3HitlerTriggerInitialSpawns` | `Number` | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. | 2 |
| [`TagMetronome`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'TagMetronome' effect/state. | 2 |
| `TakeExtraTurnEndOfRound` | `Number` | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. | 2 |
| `TargetedMetronome` | `Number` | Applies or references the 'TargetedMetronome' effect/state. | 2 |
| [`TeamBonusAbility`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'TeamBonusAbility' effect/state. | 2 |
| [`TeleportBackAtTurnEnd`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'TeleportBackAtTurnEnd' effect/state. | 2 |
| `TempBackstabBleed` | `Number` | Applies or references the 'TempBackstabBleed' effect/state. | 2 |
| `TempBackstabPiercing` | `Number` | Applies or references the 'TempBackstabPiercing' effect/state. | 2 |
| `TempBackstabPoison` | `Number` | Applies or references the 'TempBackstabPoison' effect/state. | 2 |
| `TempBasicAttackBonusAOE` | `Number` | Applies or references the 'TempBasicAttackBonusAOE' effect/state. | 2 |
| `TempLuckUp` | `Number` | Applies or references the 'TempLuckUp' effect/state. | 2 |
| `TempPenetrate` | `Number` | Applies or references the 'TempPenetrate' effect/state. | 2 |
| `ThornsDamageImmuneUntilSettled` | `Number` | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 2 |
| [`TickDownStatus`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'TickDownStatus' effect/state. | 2 |
| `TileDamageImmuneUntilSettled` | `Number` | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 2 |
| [`TransformBasicMove`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'TransformBasicMove' effect/state. | 2 |
| [`TransformEquipment`](./Abilities_and_Spells.md#object-transformequipment) | Object | Upgrades or transforms a specific equipped item into another. | 2 |
| [`TransformNow`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'TransformNow' effect/state. | 2 |
| `Trapper_Status` | `Number` | Applies or references the 'Trapper_Status' effect/state. | 2 |
| `TriggerGameEnding` | `Number` | Applies or references the 'TriggerGameEnding' effect/state. | 2 |
| `TriggerMotherConsume` | `Number` | Applies or references the 'TriggerMotherConsume' effect/state. | 2 |
| `TriggerMotherGrow` | `Number` | Applies or references the 'TriggerMotherGrow' effect/state. | 2 |
| `TurnAround` | `Number` | Applies or references the 'TurnAround' effect/state. | 2 |
| [`TurnControlDelay`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'TurnControlDelay' effect/state. | 2 |
| `TurnRight` | `Number` | Applies or references the 'TurnRight' effect/state. | 2 |
| `UndoDamage` | `Number` | Applies or references the 'UndoDamage' effect/state. | 2 |
| [`UseMoveAbilityWithAI`](./Abilities_and_Spells.md#object-usemoveabilitywithai) | Object | Forces the character to execute a movement ability using specific AI weights. | 2 |
| `VaporizeDice` | `Number` | Applies or references the 'VaporizeDice' effect/state. | 2 |
| [`VisualCountDownThenApplyStatus`](./Abilities_and_Spells.md#object-visualcountdownthenapplystatus) | Object | Displays a visual countdown above the target before applying the nested effects. | 2 |
| [`WaggleClone`](./Abilities_and_Spells.md#object-waggleclone) | Object | Spawns visual clones or alternative hitbox variants of the projectile. | 2 |
| [`Conditional_FinishedSpawning`](./Abilities_and_Spells.md#object-conditional-finishedspawning) | Object | Conditional trigger: Executes nested logic if the target has fully completed its spawn animation/sequence. | 1 |
| [`element`](./Engine_LogicKeys.md#valid-property-keys) | Enum/String | The specific element type to check for. | 1 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 71

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Conditional_Buddy`](./Abilities_and_Spells.md#object-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag), [`Conditional_Object`](./Abilities_and_Spells.md#object-conditional_object), [`Conditional_Speculative`](./Abilities_and_Spells.md#object-conditional_speculative), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Engine_LogicKeys.md#valid-property-keys) | Enum/String | The specific string tag to check for. | 981 |
| [`Conditional_NotBoss`](./Abilities_and_Spells.md#object-conditional-notboss) | Object | Conditional trigger: Executes nested logic if the target is NOT a Boss. | 16 |
| [`GainDisorderFromPool_PostCast`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 14 |
| [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource) | Object | Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 12 |
| [`BonusDamage`](./Engine_LogicKeys.md#valid-property-keys) | String | Applies or references the 'BonusDamage' effect/state. | 12 |
| [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional-inform) | Object | Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 7 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 6 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 6 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 4 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 4 |
| [`Conditional_HasStatus`](./Abilities_and_Spells.md#object-conditional-hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 4 |
| [`extra_statuses`](./Abilities_and_Spells.md#object-extra-statuses) | Object | Additional generic status applications. | 4 |
| `FactionConversion` | Number | Applies or references the 'FactionConversion' effect/state. | 4 |
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | Object | Transforms the character into a different state or form (e.g., Rage, HasCat). | 4 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 4 |
| `RandomStatDown` | Number | Applies or references the 'RandomStatDown' effect/state. | 4 |
| `Revive` | `Number` | Applies or references the 'Revive' effect/state. | 4 |
| `SpawnBearTrapIfHitKills` | `Number` | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 4 |
| [`SpawnThingIfHitKills`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'SpawnThingIfHitKills' effect/state. | 4 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 3 |
| [`ApplyToRandomPartyMemberIfPossible`](./Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object | Redirects the nested effects to apply to a random living member of the player's party. | 2 |
| [`CatPartsTransform`](./Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms specific body parts into different visual variants. | 2 |
| [`Conditional_Displaceable`](./Abilities_and_Spells.md#object-conditional-displaceable) | Object | Conditional trigger: Executes nested logic if the target is not immune to knockback or forced movement. | 2 |
| [`Conditional_GoodRoll`](./Abilities_and_Spells.md#object-conditional-goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 2 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#object-conditional-healththreshold) | Object | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. | 2 |
| [`Consumed`](./Abilities_and_Spells.md#object-consumed) | Object | State object triggered when this object or entity is eaten/consumed by another character. | 2 |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object | Removes an equipped item and replaces it with a parasite from a specified pool. | 2 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 2 |
| [`DoDamage`](./Abilities_and_Spells.md#object-dodamage) | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 2 |
| `ExplodeCharacter` | `Number` | Applies or references the 'ExplodeCharacter' effect/state. | 2 |
| `ExplodeCharacter_Party` | `Number` | Applies or references the 'ExplodeCharacter_Party' effect/state. | 2 |
| `FaceCamera` | `Number` | Applies or references the 'FaceCamera' effect/state. | 2 |
| `FlatAIBonus` | `Number` | Applies or references the 'FlatAIBonus' effect/state. | 2 |
| `ForceImmediateMove` | `Number` | Applies or references the 'ForceImmediateMove' effect/state. | 2 |
| `GenericDebuff` | `Number` | Applies or references the 'GenericDebuff' effect/state. | 2 |
| [`ImmediateUseAbility`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'ImmediateUseAbility' effect/state. | 2 |
| `Instakill` | `Number` | Applies or references the 'Instakill' effect/state. | 2 |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#object-knockupandaway) | Object | Displaces the target vertically and horizontally away from the source. | 2 |
| `OverrideDamage` | `Number` | Applies or references the 'OverrideDamage' effect/state. | 2 |
| `PurgeAll` | `Number` | Applies or references the 'PurgeAll' effect/state. | 2 |
| `RemoveMovePoints` | `Number` | Applies or references the 'RemoveMovePoints' effect/state. | 2 |
| `RemoveTurnsThisRound` | `Number` | Applies or references the 'RemoveTurnsThisRound' effect/state. | 2 |
| `SetHealth` | `Number` | Applies or references the 'SetHealth' effect/state. | 2 |
| `SetShield` | `Number` | Applies or references the 'SetShield' effect/state. | 2 |
| [`ShowFakeDamage`](./Abilities_and_Spells.md#object-showfakedamage) | Object | Displays a visual damage number without actually modifying health. | 2 |
| `SpeculativeMoveSelfCorpseOffMap` | `Number` | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 2 |
| [`Temporary`](./Abilities_and_Spells.md#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 2 |
| `VaporizeInanimate` | `Number` | Applies or references the 'VaporizeInanimate' effect/state. | 2 |
| [`XIsTargetHealth`](./Abilities_and_Spells.md#object-xistargethealth) | Object | Math variable assignment: Evaluates X as the target's current health. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `empty_self_damage`


**Definition:** Recoil damage specifically applied when the attack misses all targets.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 4 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `EvolveAbilityFromPool`


**Definition:** Upgrades or transforms an existing ability into a new one from the specified pool.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum |  | 26 |
| `upgraded` | Boolean |  | 26 |

</details>


### Object: `extra_statuses`


**Definition:** Additional generic status applications.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Consumed`](./Abilities_and_Spells.md#object-consumed)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `FindItemFromPool`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability of finding the item. | 6 |
| [`pool`](./Enums.md#enum-pool) | Enum | The item pool to draw from. | 4 |

</details>


### Object: `ForceAttack`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `immediate` | Boolean |  | 4 |

</details>


### Object: `ForceImmediateMoveAndAttack`


**Definition:** Forces the character to immediately move to a target and use a specified ability.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#object-conditional_inform)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ability to execute after moving. | 2 |
| `even_if_cant_reach` | Boolean | If true, executes the attack even if the move fails to reach the target. | 2 |

</details>


### Object: `ForceMoveTowardsTaggedObject`


**Definition:** Forces the character to move towards the nearest object with a specific tag.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The movement ability to use. | 4 |
| [`tag`](./Enums.md#enum-tag) | Enum | The entity tag to seek out. | 2 |

</details>


### Object: `FormChange`


**Definition:** Transforms the character into a different state or form (e.g., Rage, HasCat).  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Engine_LogicKeys.md#valid-property-keys) | Mixed |  | 150 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |

</details>


### Object: `GainCoinsRange`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum coins granted. | 22 |
| `min` | Number | Minimum coins granted. | 22 |

</details>


### Object: `graphics`


**Definition:** Object defining visual animations and sequence timings.  
**Total Count:** 2609

<details>
<summary><b>Expand</b></summary

> **Referenced by:** [`ROOT`](#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | The primary flash animation label triggered. | 3118 |
| [`particle`](./Enums.md#enum-particle) | Enum | References an impact or cast particle effect. | 976 |
| [`projectile`](./Enums.md#enum-projectile) | Enum | References a projectile entity. | 460 |
| `lob` | Boolean |  | 260 |
| `delay` | Number | Frame delay before firing projectile/effect. | 186 |
| `dont_visualize_ai` | Boolean |  | 172 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 166 |
| [`dash_animation`](./Enums.md#enum-dash_animation) | Enum | State-specific animations for trample/dash abilities. | 130 |
| [`dash_start_animation`](./Enums.md#enum-dash_start_animation) | Enum |  | 126 |
| `speed` | Number | Rotations per second. | 122 |
| [`affected_particle`](./Enums.md#enum-affected_particle) | Enum | Visuals applied to the target receiving the effect. | 102 |
| [`dash_attack_animation`](./Enums.md#enum-dash_attack_animation) | Enum |  | 90 |
| `lob_height` | Number | Adjustments for arcing projectiles. | 90 |
| [`animation_in`](./Enums.md#enum-animation_in) | Enum | Used for transition states (like burrowing). | 86 |
| [`animation_out`](./Enums.md#enum-animation_out) | Enum | Used for transition states (like burrowing). | 86 |
| [`jump_attack_animation`](./Enums.md#enum-jump_attack_animation) | Enum | Overrides for jump physics. | 78 |
| `use_projectile` | Boolean |  | 70 |
| `palette` | Number | Swaps the color palette ID. | 66 |
| [`full_jump_animation`](./Enums.md#enum-full_jump_animation) | Enum |  | 48 |
| `full_jump_sync_frames` | Number |  | 48 |
| `use_rotation` | Boolean |  | 48 |
| [`dash_end_animation`](./Enums.md#enum-dash_end_animation) | Enum |  | 44 |
| `full_jump_windup_frames` | Number |  | 40 |
| `visual_delay_but_simultaneous_damage` | Number |  | 36 |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum | Specific spawn points for particles. | 34 |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum | Specific spawn points for particles. | 32 |
| `fall_from_sky` | Boolean | Spawns the projectile from the top of the screen. | 32 |
| [`move_start_animation`](./Enums.md#enum-move_start_animation) | Enum |  | 28 |
| `use_placeholder` | Boolean |  | 28 |
| [`move_end_animation`](./Enums.md#enum-move_end_animation) | Enum |  | 26 |
| `face_toss_target` | Boolean |  | 24 |
| `ignore_slowtiles` | Boolean |  | 24 |
| [`chain_distance`](./Enums.md#enum-chain_distance) | Enum | Creates a tethered repeating graphic (like a hook). | 22 |
| [`chain_movieclip`](./Enums.md#enum-chain_movieclip) | Enum | Creates a tethered repeating graphic (like a hook). | 22 |
| `darken_screen` | Boolean | Dims the background during the ability cast. | 22 |
| [`beam_cap`](./Enums.md#enum-beam_cap) | Enum | Flash movieclips used to render continuous laser beams. | 20 |
| [`beam_clip`](./Enums.md#enum-beam_clip) | Enum | Flash movieclips used to render continuous laser beams. | 20 |
| `bounce_on_hit` | Boolean | Visual hop when striking a target. | 20 |
| `darken_screen_exclude_characters_on_tile` | Boolean |  | 20 |
| [`end`](./Enums.md#enum-end) | Enum | Segments for continuous channeled animations. | 20 |
| [`jump_start_animation`](./Enums.md#enum-jump_start_animation) | Enum |  | 20 |
| [`loop`](./Enums.md#enum-loop) | Enum | Segments for continuous channeled animations. | 20 |
| [`prime_animation`](./Enums.md#enum-prime_animation) | Enum |  | 20 |
| [`start`](./Enums.md#enum-start) | Enum | Segments for continuous channeled animations. | 20 |
| `max_tiles_single_loop` | Number |  | 18 |
| `sync_speed` | Number |  | 18 |
| `fx_is_placeholder_animation` | Boolean |  | 16 |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 14 |
| `fx_random_flip` | Boolean |  | 14 |
| [`land_animation`](./Enums.md#enum-land_animation) | Enum |  | 14 |
| [`miss_particle`](./Enums.md#enum-miss_particle) | Enum | Specific spawn points for particles. | 14 |
| `use_super_armor` | Boolean | Prevents flinch animations from interrupting this cast. | 14 |
| [`air_animation`](./Enums.md#enum-air_animation) | Enum | Animation played while entity is airborne. | 12 |
| [`custom_priming_animation`](./Enums.md#enum-custom_priming_animation) | Enum | Animation used while charging an ability. | 12 |
| `darken_screen_exclude_self` | Boolean |  | 12 |
| `darken_screen_start_early` | Boolean |  | 12 |
| [`fall_randomize_timing`](./Enums.md#enum-fall_randomize_timing) | Enum |  | 12 |
| `min_throw_height` | Number |  | 12 |
| `single_projectile` | Boolean |  | 12 |
| [`detatched_animation`](./Enums.md#enum-detatched_animation) | Enum | Plays an animation separated from the character body. | 10 |
| `detatched_animation_reach` | Number |  | 10 |
| [`empty_animation`](./Enums.md#enum-empty_animation) | Enum |  | 10 |
| [`mode`](./Enums.md#enum-mode) | Enum |  | 10 |
| [`random_delay`](./Arrays.md#array-random_delay) | Array | Adds chaotic timing to multi-projectile casts. | 9 |
| `fixed_jump_height` | Number |  | 8 |
| [`rocket_swirl`](#object-rocket_swirl) | Object | Visual parameters for swirling projectile paths. | 8 |
| `sync_frames` | Number |  | 8 |
| [`dash_decelerating_animation`](./Enums.md#enum-dash_decelerating_animation) | Enum |  | 6 |
| `decelerate` | Number | Visual slowdown at the end of a movement. | 6 |
| `delay_from_map_edge` | Boolean | Delays effect based on distance from the screen edge. | 6 |
| `easing` | Number | Smoothing function for movement animations. | 6 |
| [`fixed_jump_speed`](./Enums.md#enum-fixed_jump_speed) | Number |  | 6 |
| [`grab_animation`](./Enums.md#enum-grab_animation) | Enum |  | 6 |
| [`lob_yoff`](./Enums.md#enum-lob_yoff) | Enum | Adjustments for arcing projectiles. | 6 |
| `lock_orientation_during_dash` | Boolean | Prevents the sprite from flipping mid-dash. | 6 |
| [`miss_random_delay`](./Arrays.md#array-miss_random_delay) | Array |  | 6 |
| `use_projectile_spawn_offset` | Boolean |  | 6 |
| `use_rotation_once` | Boolean |  | 6 |
| `always_play_animations` | Boolean | Bypasses speed-up/skip logic. | 4 |
| `detatched_animation_cutoff` | Boolean |  | 4 |
| `do_damage_immediately` | Boolean | Applies math before the animation actually hits. | 4 |
| `jump_height_multiplier` | Enum | Overrides for jump physics. | 4 |
| [`mask_center`](./Enums.md#enum-mask_center) | Enum |  | 4 |
| [`mask_extent`](./Enums.md#enum-mask_extent) | Enum |  | 4 |
| `max_throw_height` | Number |  | 4 |
| [`particle_mat`](./Enums.md#enum-particle_mat) | Enum |  | 4 |
| [`preturn_animation`](./Enums.md#enum-preturn_animation) | Enum |  | 4 |
| [`primed_alt_animation`](./Strings.md#string-primed_alt_animation) | String |  | 4 |
| [`pseudoprojectile`](./Enums.md#enum-pseudoprojectile) | Enum |  | 4 |
| `reverse_orientation` | Boolean |  | 4 |
| `self_damage_mid_port` | Boolean |  | 4 |
| `throw_speed` | Number |  | 4 |
| `use_hit_alts` | Boolean |  | 4 |
| [`affected_animation`](./Enums.md#enum-affected_animation) | Enum | Visuals applied to the target receiving the effect. | 2 |
| [`ally_animation`](./Enums.md#enum-ally_animation) | Enum | Distinct animation used when targeting a friendly unit. | 2 |
| [`animate_name`](./Enums.md#enum-animate_name) | String | Animates the ability name text on cast. | 2 |
| `apex_distance` | Number | Calculations for the peak of a jump/lob arc. | 2 |
| [`apex_time`](./Enums.md#enum-apex_time) | Enum | Calculations for the peak of a jump/lob arc. | 2 |
| `bypass_combatspeed` | Boolean |  | 2 |
| [`damage_threshold_altanimations`](#object-damage_threshold_altanimations) | Object | Triggers different hit animations based on the amount of damage dealt. | 2 |
| [`dash_bonk_animation`](./Enums.md#enum-dash_bonk_animation) | Enum |  | 2 |
| `delay_from_map_center` | Boolean | Positional based timing delays. | 2 |
| `delay_from_reverse_map_edge` | Boolean |  | 2 |
| `do_animation_offscreen` | Boolean |  | 2 |
| `do_not_clear_placeholder` | Boolean |  | 2 |
| `face_targets` | Boolean | Forces the sprite to look at the target tile. | 2 |
| `first_castpoint_is_self_damage_only` | Boolean |  | 2 |
| [`hang_time`](./Enums.md#enum-hang_time) | Enum |  | 2 |
| `jump_speed_multiplier` | Number |  | 2 |
| [`lob_speed`](./Enums.md#enum-lob_speed) | Enum | Adjustments for arcing projectiles. | 2 |
| `max_range` | Number | The maximum and minimum distance required to cast. | 2 |
| `min_range` | Number | The maximum and minimum distance required to cast. | 2 |
| `othercat_placeholder_available` | Boolean |  | 2 |
| [`precast_delay`](./Enums.md#enum-precast_delay) | Enum |  | 2 |
| `uncatchable` | Boolean |  | 2 |
| `use_directional_animations` | Boolean |  | 2 |
| `use_origin_offsets` | Boolean |  | 2 |
| [`spawn_offset`](./Arrays.md#array-spawn_offset) | Array |  | 1 |

</details>


### Object: `IncAuxCounterClamped`


**Definition:** Increments a generic auxiliary counter on the character, capped by a maximum value.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#object-randomstatusfrompool)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number |  | 6 |
| `max` | Number |  | 6 |

</details>


### Object: `IncAuxCounterCycle`


**Definition:** Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number |  | 2 |
| `max` | Number |  | 2 |

</details>


### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TemporaryItem` | Number | Applies or references the 'TemporaryItem' effect/state. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `KnockOutCoin`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | Probability (0.0 to 1.0 or percentage) of this occurring. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>


### Object: `KnockUpAndAway`


**Definition:** Displaces the target vertically and horizontally away from the source.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#object-applytosource), [`Conditional_LastHit`](./Abilities_and_Spells.md#object-conditional_lasthit), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | The distance in tiles to knock the target away. | 48 |
| [`stacks`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Number of stacks or intensity to apply. | 44 |
| `height` | Number |  | 4 |
| `circular_variance` | Number |  | 2 |

</details>


### Object: `LateStatusApplication`


**Definition:** Applies a status effect after all primary damage and effects have fully resolved.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>


### Object: `LeaveBehind`


**Definition:** Spawns a specific object at the character's previous location when they move.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#object-temporary_effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID to spawn. | 8 |

</details>


### Object: `LowerAmbientLight`


**Definition:** A visual effect that dims the map's lighting.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CreateGlobalModifiers`](./Abilities_and_Spells.md#object-createglobalmodifiers)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `speed` | Number | The transition speed. | 6 |
| [`amount`](./Arrays.md#array-amount) | Array | The target opacity/dimness level. | 2 |

</details>


### Object: `Madness`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| `tickdown_this_turn` | Boolean |  | 2 |

</details>


### Object: `Math`


**Definition:** Triggers the Tinkerer's Math ability sequence.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 94 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `MergeDamageInstance`


**Definition:** Combines damage numbers or visual hit effects.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `can_instapop` | `Boolean` | If false, prevents the damage from instantly popping the target. | 2 |
| `force_no_hit_animation` | Boolean | If true, suppresses the flinch/hit animation. | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `meta`


**Definition:** Object defining UI display data (Name, Description, Icon).  
**Total Count:** 2374

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`desc`](./Strings.md#string-desc) | String | The localization key for the ability's display description. | 3282 |
| [`name`](./Strings.md#string-name) | String | The localization key for the ability's display name. | 3222 |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 1752 |
| [`type_icon`](./Strings.md#string-type_icon) | String |  | 566 |
| `animate_name` | Boolean | If true, adds a visual pop/animation to the name text when cast. | 354 |
| [`icon_shell_frame`](./Strings.md#string-icon_shell_frame) | Mixed |  | 56 |
| [`is_move`](./Enums.md#enum-is_move) | Mixed |  | 40 |
| [`ability_icon`](./Enums.md#enum-ability_icon) | Enum | The UI icon to display in the action bar. | 28 |
| [`icon_damage_display`](./Strings.md#string-icon_damage_display) | String |  | 16 |
| [`icon_damage_display_eq`](./Math_Equations.md) | Equation |  | 14 |
| `is_basic_attack` | Boolean |  | 12 |
| [`tooltip_values`](./Arrays.md#array-tooltip_values) | Array |  | 9 |
| `is_weapon` | Boolean |  | 8 |
| [`icon_damage_type`](./Enums.md#enum-icon_damage_type) | Enum |  | 6 |
| `is_trinket` | Boolean |  | 6 |
| `dont_visualize_ai` | Boolean |  | 4 |
| [`icon_damage_display_suffix`](./Strings.md#string-icon_damage_display_suffix) | String |  | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum |  | 2 |

</details>


### Object: `Metronome`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array |  | 1 |

</details>


### Object: `NextAttackSpecialCrit`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Number | Flat addition to the critical damage multiplier. | 2 |
| `extra_coins_per_stack` | Number | Grants bonus coins based on stacks. | 2 |
| `luck_increase` | Number | Increases luck stat for the attack. | 2 |

</details>


### Object: `NextBasicAttackCritsThisTurn`


**Definition:** Guarantees the next basic attack executed this turn will be a critical hit.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cant_miss` | `Boolean` | If true, ensures the attack cannot be dodged. | 2 |
| `piercing` | `Boolean` | If true, the attack ignores armor. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `NextBattleStatusStacks`


**Definition:** Carries over the specified status effects into the next encounter/battle.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `fights` | Number | The number of encounters this buff/debuff persists for. | 2 |
| `MadnessChanceOnTurnBegin` | `Number` | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `NukeQuestFinalBossModifications`


**Definition:** Special encounter trigger for the Nuke Quest ending.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage_instance`](./Abilities_and_Spells.md#object-damage_instance) | Object |  | 2 |
| [`splash_damage`](./Abilities_and_Spells.md#object-splash_damage) | Object | Secondary Area of Effect blast parameters. | 2 |

</details>


### Object: `ObjectOnHit`


**Definition:** Spawns a specific physics/item object upon impact.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the object to spawn (e.g., Poop). | 4 |

</details>


### Object: `ObjectOnHitCharacter`


**Definition:** No definition provided.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID of the character to spawn (e.g., CharmedFlea). | 14 |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Mixed | Probability (0.0 to 1.0) of spawning. | 4 |

</details>


### Object: `OverHealToStatuses`


**Definition:** Converts excessive healing beyond maximum health into specific status effects.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stack_scale` | Number |  | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `PassiveWhileNotTakingTurn`


**Definition:** Grants nested passives that are only active while it is NOT the character's turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>


### Object: `PoolMetronome`


**Definition:** Executes a random ability drawn from a specific pool.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of ability IDs to randomly choose from. | 1 |

</details>


### Object: `PopAndSpawn`


**Definition:** Destroys the target and replaces it with a new spawned entity.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | The entity ID to spawn in place. | 4 |
| `clone_items` | Boolean | If true, transfers inventory to the new entity. | 2 |
| `clone_referenced_catdata` | Boolean | If true, copies the genetic data of the popped cat. | 2 |
| `no_splatter` | Boolean |  | 2 |

</details>


### Object: `post_spawn_statuses`


**Definition:** Status effects applied immediately after an entity spawns.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`spawn`](./Abilities_and_Spells.md#object-spawn)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DoDamage`](./Abilities_and_Spells.md#object-dodamage) | Object | Explicitly triggers a secondary damage instance independent of the main attack. | 4 |
| [`EnterMount`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'EnterMount' effect/state. | 2 |
| [`VisualFXTile`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'VisualFXTile' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `QuakeAreaChance`


**Definition:** Provides a probability to trigger an earthquake Area of Effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | Probability of triggering the quake. | 4 |
| `radius` | Number | The tile radius of the quake. | 4 |

</details>


### Object: `RandomDistanceDisplace`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `min_dist` | Number | The minimum tile distance they will be moved. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>


### Object: `RandomKnockback`


**Definition:** Applies a randomized amount of knockback force.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | Maximum knockback distance. | 4 |
| `min` | Number | Minimum knockback distance. | 4 |

</details>


### Object: `RandomMagicMissile`


**Definition:** No definition provided.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `full_size` | Boolean | If true, fires normal sized missiles instead of mini ones. | 4 |
| `stacks` | Number | Number of stacks or intensity to apply. | 4 |

</details>


### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 19

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyMultipleTimes`](./Abilities_and_Spells.md#object-applymultipletimes), [`Conditional_CanBeHealed`](./Abilities_and_Spells.md#object-conditional_canbehealed), [`Conditional_HasCleansableDebuffs`](./Abilities_and_Spells.md#object-conditional_hascleansabledebuffs), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `RemoveStatusStacks`


**Definition:** Removes a specific number of stacks of a status effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | The number of stacks to remove. | 8 |
| [`status`](./Enums.md#enum-status) | Enum | The specific status effect ID to remove. | 8 |

</details>


### Object: `ReplaceSpell`


**Definition:** Replaces a spell in the character's hand/deck with a different one.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#object-temppassivewhilehasstatus)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The new ability ID to insert. | 8 |
| `slot` | Number | The spell slot index to replace. | 8 |

</details>


### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 58 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `ReviveNextRound`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `revive_health` | Number | The flat amount of health to revive with. | 8 |
| `stacks` | Number | Number of stacks or intensity to apply. | 4 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `rocket_swirl`


**Definition:** Visual parameters for swirling projectile paths.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`graphics`](./Abilities_and_Spells.md#object-graphics)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`radius`](./Arrays.md#array-radius) | Array | Swirl radius. | 4 |
| [`speed`](./Arrays.md#array-speed) | Array | Rotations per second. | 4 |

</details>


### Object: `ScatterCoins`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#object-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stackable` | Boolean | If true, multiple instances of this trigger can stack. | 4 |
| [`stacks`](./Math_Equations.md) | Equation | Number of stacks or intensity to apply. | 4 |

</details>


### Object: `ScrambleLastUsedSpell`


**Definition:** Randomizes or scrambles the properties of the last spell cast.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `permanent` | Boolean | If true, the scramble persists for the rest of the run. | 2 |

</details>


### Object: `self_damage`


**Definition:** Recoil or self-inflicted damage/effects applied to the caster.  
**Total Count:** 220

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 400 |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Mixed | The base damage properties of an attack. | 94 |
| `piercing` | `Boolean` |  | 24 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 22 |
| `cant_miss` | `Boolean` |  | 20 |
| `knockback` | Number |  | 20 |
| `heal` | `Number` |  | 12 |
| `ai_base_score` | Number |  | 4 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 4 |
| `non_lethal` | `Boolean` |  | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `SetAnimationAlts`


**Definition:** Overrides specific animation states with alternative animations.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#object-conditional_hastag)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dead`](./Enums.md#enum-dead) | Enum |  | 2 |
| [`dying`](./Enums.md#enum-dying) | Enum |  | 2 |

</details>


### Object: `SetCrazyEyeBackgroundWeights`


**Definition:** Adjusts visual rendering weights for the 'Crazy Eye' background effect.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array |  | 3 |

</details>


### Object: `ShowFakeDamage`


**Definition:** Displays a visual damage number without actually modifying health.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| [`style`](./Arrays.md#array-style) | Array | The visual font style for the text (e.g., [crit]). | 1 |

</details>


### Object: `SmartMetronome`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| `upgraded` | Boolean |  | 2 |

</details>


### Object: `sounds`


**Definition:** Audio cues triggered by the ability.  
**Total Count:** 39

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ontrigger`](./Enums.md#enum-ontrigger) | Enum |  | 64 |
| [`oncast`](./Enums.md#enum-oncast) | Enum |  | 6 |
| [`oncastpoint`](./Enums.md#enum-oncastpoint) | Enum |  | 6 |
| [`ontrigger_intentional`](./Enums.md#enum-ontrigger_intentional) | Enum |  | 2 |

</details>


### Object: `spawn`


**Definition:** Parameters for summoning new characters, objects, or entities.  
**Total Count:** 192

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum |  | 330 |
| [`faction`](./Enums.md#enum-faction) | Enum |  | 118 |
| `ai_base_score` | Number |  | 62 |
| [`additional_passives`](./Abilities_and_Spells.md#object-additional_passives) | Object | Passives granted intrinsically to a spawned entity. | 40 |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum |  | 34 |
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` |  | 28 |
| [`catdata`](./Enums.md#enum-catdata) | Enum | Defines genetic/clone data cloning. | 26 |
| `clone_items` | Boolean | If true, transfers inventory to the clone. | 24 |
| `lob` | Boolean |  | 8 |
| [`post_spawn_statuses`](./Abilities_and_Spells.md#object-post_spawn_statuses) | Object | Status effects applied immediately after an entity spawns. | 8 |
| `size` | Number |  | 8 |
| `face_camera` | Boolean |  | 4 |
| `inherit_elite_buffs` | Boolean |  | 4 |
| `start_dead` | Boolean |  | 4 |
| [`appearance`](./Enums.md#enum-appearance) | Enum |  | 2 |
| [`auto_cast_on_spawn`](./Enums.md#enum-auto_cast_on_spawn) | Enum |  | 2 |
| [`chapter`](./Enums.md#enum-chapter) | Enum |  | 2 |
| [`custom_additional_ai_weight`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` |  | 2 |
| `include_passives` | Boolean |  | 2 |
| `redirect_location_if_blocked` | Boolean |  | 2 |
| [`spawnin_animation`](./Enums.md#enum-spawnin_animation) | Enum |  | 2 |
| `trigger_battle_start` | Boolean |  | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `splash_damage`


**Definition:** Secondary Area of Effect blast parameters.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`NukeQuestFinalBossModifications`](./Abilities_and_Spells.md#object-nukequestfinalbossmodifications), [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | The base damage properties of an attack. | 64 |
| [`effects`](./Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 34 |
| `knockback` | Number | Knockback force of the splash blast. | 26 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 24 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 13 |
| `makes_contact` | `Boolean` |  | 12 |
| `override_trample_damage` | `Boolean` |  | 4 |
| `ai_base_score` | Number |  | 2 |
| `crit_chance` | `Number` |  | 2 |
| `force_no_knockback` | `Boolean` |  | 2 |
| `force_play_hit_animation` | `Boolean` |  | 2 |
| [`layer`](./Engine_DamagingKeys.md#valid-property-keys) | `Enum/String` |  | 2 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `SpreadDisease`


**Definition:** Provides a chance to transmit a disease status to adjacent targets.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | The specific status effect ID representing the disease. | 26 |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of transmitting. | 24 |

</details>


### Object: `StatusGroup`


**Definition:** Groups multiple status effects together for batch application.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `StatusKillers`


**Definition:** Instantly kills the target if they possess the specified status effects.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>


### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyPassives`](./Abilities_and_Spells.md#object-applypassives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 50 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `SwapWeapon`


**Definition:** Replaces the character's currently equipped weapon with one from a specified pool.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | An array of weapon item IDs to draw from. | 1 |

</details>


### Object: `SwitchMusic`


**Definition:** Changes the background music track or layer during combat.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#object-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | The specific audio layer to transition to (e.g., map, battle). | 14 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | The ID of the new music track. | 12 |
| `crossfade_speed` | Number |  | 2 |

</details>


### Object: `TakeBonusTurnWithAIControl`


**Definition:** Grants the character an immediate extra turn, but forces the AI to control them during it.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 6 |

</details>


### Object: `TakeBonusTurnWithStatus`


**Definition:** Grants the character an immediate extra turn while afflicted with specific statuses.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `Tangled`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum | The alternative sprite art to use while tangled. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>


### Object: `target`


**Definition:** Object defining the shape, range, and restrictions of the ability's aiming phase.  
**Total Count:** 1862

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_range` | Number | The maximum and minimum distance required to cast. | 2176 |
| `max_aoe` | Number | The maximum and minimum radius/length of the AoE. | 1590 |
| `min_range` | Number | The maximum and minimum distance required to cast. | 1166 |
| [`target_mode`](./Enums.md#enum-target_mode) | Enum | How the cursor operates (`tile`, `direction`, `none`). | 1006 |
| [`aoe_mode`](./Enums.md#enum-aoe_mode) | Enum | The shape of the area (`standard`, `line`, `cross`, `square`, `custom`). | 864 |
| [`restrictions`](./Arrays.md#array-restrictions) | Array | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 632 |
| [`knockback_mode`](./Enums.md#enum-knockback_mode) | Enum | How physics vectors apply (`character_to_tile`, `pull_to_character`, `zero`, `orientation`). | 530 |
| [`min_aoe`](./Enums.md#enum-min_aoe) | Mixed | The maximum and minimum radius/length of the AoE. | 506 |
| `aoe_excludes_self` | Boolean | Prevents the AoE from hitting the caster. | 482 |
| `aoe_considers_character_size` | Boolean | Scales the AoE based on the caster's tile size (e.g., 2x2). | 340 |
| [`aoe_restrictions`](./Arrays.md#array-aoe_restrictions) | Array | Array of conditions the AoE tiles must meet (e.g., `must_have_line_of_sight_unpurgable`). | 276 |
| [`range_mode`](./Enums.md#enum-range_mode) | Enum | How range is counted (`standard`, `ground_move`). | 228 |
| [`X_is`](./Enums.md#enum-x_is) | Enum | Applies or references the 'X_is' effect/state. | 172 |
| `multihit` | Number | Hardcoded number of times the ability hits the target. | 124 |
| `max_targets` | Number | Limits on how many distinct entities can be targeted. | 112 |
| `range_excludes_blocking` | Boolean | Cannot target through walls/obstacles. | 106 |
| `prioritize_dont_change_direction` | Mixed | AI preference to maintain current facing angle. | 104 |
| [`custom_aoe`](./Arrays.md#array-custom_aoe) | Array | Array of exact coordinates for a custom shape (e.g., `[[1, -1] [1, 0]]`). | 83 |
| [`target_requires_tag`](./Enums.md#enum-target_requires_tag) | Enum | Target must possess this exact character tag. | 80 |
| [`aoe_symmetry`](./Enums.md#enum-aoe_symmetry) | Enum | Determines if the AoE mirrors on axes. | 56 |
| `prioritize_face_camera` | Mixed | AI preference to face South. | 52 |
| `straight_shot` | Boolean | Ensures projectiles do not arc. | 48 |
| `can_multihit` | Boolean | If true, overlapping AoEs can hit the same target multiple times. | 34 |
| `allow_any_orientation` | Boolean | Allows casting regardless of the character's facing direction. | 32 |
| `range_considers_character_size` | Boolean | Range calculation accounts for large entities. | 32 |
| `throw_consumed_character` | Boolean | Throws the entity currently held/eaten. | 30 |
| `min_targets` | Number | Limits on how many distinct entities can be targeted. | 28 |
| `aoe_leading_edge_only` | Boolean | Only the outermost edge of the AoE shape applies effects. | 26 |
| `allow_diagonals` | Boolean | Allows targeting on diagonal grid axes. | 24 |
| `range_display_include_character_size` | Boolean | Visual: offsets the range indicator for 2x2 units. | 24 |
| `stagger_multihit_targets` | Boolean | Delays hits slightly between multiple targets. | 24 |
| `upgrade_straight_shot_to_piercing` | Boolean | Allows the projectile to pass through multiple targets. | 22 |
| `delayed_trigger` | Boolean | Delays the actual execution of the target effect. | 20 |
| `consider_trample` | Boolean | AI consideration for moving through units. | 18 |
| `N` | Number | Variable modifier parameter. | 14 |
| `always_bounce` | Boolean | Forces the attack/projectile to bounce regardless of hit. | 12 |
| `multihit_max` | Number | Variable limits for random multihit abilities. | 12 |
| `multihit_min` | Number | Variable limits for random multihit abilities. | 12 |
| `reorient_thrown_character` | Boolean | Forces a thrown entity to face a certain way. | 12 |
| [`toss_direction_restriction`](./Enums.md#enum-toss_direction_restriction) | Enum | Limits which ways an entity can be tossed. | 12 |
| `aoe_hint_teamcast` | Boolean | Visual hint for cooperative casting abilities. | 10 |
| [`aoe_tile_requires_element`](./Enums.md#enum-aoe_tile_requires_element) | Enum | Only affects tiles painted with a specific element. | 10 |
| `distance_sort_targets` | Mixed | Prioritizes targets based on proximity. | 10 |
| `dont_orient_aoe` | Boolean | Prevents the AoE shape from rotating with the character. | 10 |
| `hint_can_target_pickups` | Boolean | UI hint that the player can target items on the ground. | 10 |
| `max_bounces` | Number | Hard cap on how many times a bouncing effect can trigger. | 10 |
| `splash_damage_aoe_begin` | Number | At what radius splash damage starts applying. | 10 |
| [`aoe_chance`](./Enums.md#enum-aoe_chance) | Enum | Percentage chance for the AoE to trigger. | 8 |
| `as_the_crow_flies` | Boolean | Calculates range ignoring all pathing terrain obstacles. | 8 |
| `force_ai_target_as_spell` | Boolean | Forces the AI to treat a physical move like a spell for targeting logic. | 8 |
| `range_display_include_aoe` | Boolean | Visual: shows the full AoE potential when previewing range. | 8 |
| `shotgun_mode` | Boolean | Deals more damage/hits if targets are closer. | 8 |
| `shuffle_tile_order` | Boolean | Randomizes the execution order of AoE tiles. | 8 |
| `upgrade_straight_shot_to_boomerang` | Boolean | Makes the projectile return to caster. | 8 |
| [`custom_range`](./Arrays.md#array-custom_range) | Array | Overrides standard range scaling. | 7 |
| [`custom_aoe_util`](./Arrays.md#array-custom_aoe_util) | Array | Utility variants of custom AoE definitions. | 6 |
| `dont_orient` | Boolean | Prevents the character from turning to face the target. | 6 |
| `low_health_character_threshold` | Mixed | AI targeting threshold for seeking weak targets. | 6 |
| `randomize_target_within_range` | Number | Picks a random valid tile instead of the user's click. | 6 |
| [`special_tile_tag`](./Enums.md#enum-special_tile_tag) | Enum | Targets only tiles with this specific tag. | 6 |
| `track_target` | Boolean | Projectile/Effect follows moving targets. | 6 |
| `corpse_priority` | Number | AI preference for targeting dead bodies. | 4 |
| `hint_can_target_empty` | Boolean | UI hint that the player can click an empty tile. | 4 |
| `low_gravity_boostable` | Boolean | Can be affected by low gravity wind/effects. | 4 |
| [`mouse_offset`](./Arrays.md#array-mouse_offset) | Array | Visual offset for the targeting cursor. | 4 |
| `prioritize_change_direction` | Boolean | AI preference to attack from different angles. | 4 |
| [`range_bonuses`](./Enums.md#enum-range_bonuses) | Enum | How much extra range is added by stats/passives. | 4 |
| `range_display_include_direction` | Boolean | Visual: shows directional arrows. | 4 |
| `recalc_target_on_castpoint` | Boolean | Re-checks if target is valid at the exact frame of cast. | 4 |
| `redirect_location_if_blocked` | Boolean | Shifts target to adjacent tile if original is invalid. | 4 |
| `trample_allies_too` | Boolean | Trample movement damages allies in the path. | 4 |
| [`adjust_target`](./Enums.md#enum-adjust_target) | Enum | Tweaks target selection post-cast. | 2 |
| `allow_diagonal_passthrough` | Boolean | Permits diagonal targeting through tight corners. | 2 |
| `ally_priority` | Number | AI preference for targeting allies. | 2 |
| `aoe_display_exclude_restrictions` | Boolean | Visual only: Hides invalid tiles from the AoE preview. | 2 |
| `aoe_rotate_around_character_center` | Boolean | Anchors the AoE rotation to the character rather than the tile. | 2 |
| `aoe_spell_on_land` | Boolean | Visual trigger when a jump lands. | 2 |
| `bonus_pathing_leniency` | Number | Gives the AI leeway when calculating complex paths. | 2 |
| `damage_collided_only` | Boolean | Only damages the first entity the projectile/dash hits. | 2 |
| `enemy_priority` | Number | AI preference for targeting enemies. | 2 |
| `force_no_contact` | `Boolean` | Bypasses all contact-based retaliation (Thorns, etc). | 2 |
| `hint_can_target_static` | Boolean | UI hint that the player can target inanimate objects. | 2 |
| [`knockback_modifier`](./Enums.md#enum-knockback_modifier) | Enum | Multiplier for the knockback physics force. | 2 |
| `lingering` | Boolean | Target zone remains active across multiple turns. | 2 |
| `mirror_custom_aoe` | Boolean | Flips the custom AoE array. | 2 |
| [`prioritize_throw_target_with_passive`](./Enums.md#enum-prioritize_throw_target_with_passive) | Enum | AI prefers throwing targets that have specific passives. | 2 |
| `randomize_knockback_direction_except_for_finisher` | Boolean | Chaotic knockback unless it kills the target. | 2 |
| `range_excludes_self` | Boolean | Cannot click on the caster's tile. | 2 |
| `range_max` | Number | Alternate syntax for `max_range`/`min_range`. | 2 |
| `range_min` | Number | Alternate syntax for `max_range`/`min_range`. | 2 |
| [`range_symmetry`](./Enums.md#enum-range_symmetry) | Enum | Mirrors the range grid. | 2 |
| `remain_off_map` | Boolean | Keeps entity removed from the grid. | 2 |
| [`restructions`](./Enums.md#enum-restructions) | Enum | Array of constraints (e.g., `must_have_line_of_sight`, `must_be_moveable`). | 2 |
| `reverse_target_direction` | Boolean | Inverts the targeting vector. | 2 |
| `spin_steps` | Number | Number of rotational increments for spin targeting. | 2 |
| [`target_requires_element`](./Arrays.md#array-target_requires_element) | Array | Target must be afflicted with this element. | 2 |
| `uncounterable` | Boolean | Bypasses counter-attack passives. | 2 |
| [`custom_aoe_mirror`](./Arrays.md#array-custom_aoe_mirror) | Array | How the custom shape mirrors when facing left vs right. | 1 |
| [`custom_aoe_util_mirror`](./Arrays.md#array-custom_aoe_util_mirror) | Array |  | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `TeamCastAbility`


**Definition:** Requires or involves multiple characters to execute the ability.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The underlying logic ability executed by the team. | 4 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Requires participants to share this tag. | 4 |
| `same_orientation` | Boolean |  | 2 |

</details>


### Object: `Temporary`


**Definition:** A wrapper object for applying status effects that automatically expire.  
**Total Count:** 41

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CanApplyToInanimate`](./Abilities_and_Spells.md#object-canapplytoinanimate), [`Conditional_Ally`](./Abilities_and_Spells.md#object-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#object-conditional_enemy), [`Conditional_NotAlly`](./Abilities_and_Spells.md#object-conditional_notally), [`Else`](./Abilities_and_Spells.md#object-else), [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | Number of stacks or intensity to apply. | 114 |
| [`status`](./Enums.md#enum-status) | Enum | The status effect to apply. | 112 |
| `turns` | Number | Duration in turns. | 104 |
| `expires_on_begin_turn` | Boolean | If true, ticks down at the start of the turn rather than the end. | 50 |
| `expires_on_end_turn` | Boolean |  | 42 |
| `data` | Number |  | 4 |
| `expires_on_appliers_turn` | Boolean |  | 4 |
| `expires_on_move` | Boolean |  | 2 |

</details>


### Object: `temporary_effects`


**Definition:** Status applications that wear off automatically or at the end of the turn.  
**Total Count:** 88

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Abilities_and_Spells.md#object-root)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CastAgain` | Number | Applies or references the 'CastAgain' effect/state. | 40 |
| `DisableTrample` | Number | Applies or references the 'DisableTrample' effect/state. | 20 |
| `Fury` | Number | Applies or references the 'Fury' effect/state. | 14 |
| `JustInCaseTrample` | Number | Applies or references the 'JustInCaseTrample' effect/state. | 10 |
| [`LeaveBehind`](./Abilities_and_Spells.md#object-leavebehind) | Object | Spawns a specific object at the character's previous location when they move. | 10 |
| `DashFury` | Number | Applies or references the 'DashFury' effect/state. | 6 |
| `BearTrapTrail` | Number | Applies or references the 'BearTrapTrail' effect/state. | 4 |
| `DelayedWindTrail` | Number | Applies or references the 'DelayedWindTrail' effect/state. | 2 |
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum | Applies or references the 'JumpAttackLeaveBehind' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `TempPassiveWhileHasStatus`


**Definition:** Grants nested passives only while the character possesses the specified status.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#object-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#object-conditional_livingplayercat)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The required status effect. | 6 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `TimeDelayStatusApplication`


**Definition:** Delays the nested effects by a specified amount of real-time seconds.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`delay`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Mixed | The float time delay in seconds. | 8 |
| [`SwitchMusic`](./Abilities_and_Spells.md#object-switchmusic) | Object | Changes the background music track or layer during combat. | 4 |
| `Cleanse` | `Number` | Applies or references the 'Cleanse' effect/state. | 2 |
| [`DoScreenShake`](./Abilities_and_Spells.md#object-doscreenshake) | Object | Triggers a camera screen shake effect. | 2 |
| [`FormChange`](./Abilities_and_Spells.md#object-formchange) | `Enum/String` | Transforms the character into a different state or form (e.g., Rage, HasCat). | 2 |
| `FullHeal` | `Number` | Applies or references the 'FullHeal' effect/state. | 2 |
| [`GlobalSpawnCharacter`](./Engine_LogicKeys.md#valid-property-keys) | `Enum/String` | Applies or references the 'GlobalSpawnCharacter' effect/state. | 2 |
| `PlayBackground` | `Number` | Applies or references the 'PlayBackground' effect/state. | 2 |
| `Vaporize` | `Number` | Applies or references the 'Vaporize' effect/state. | 2 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `TransformEquipment`


**Definition:** Upgrades or transforms a specific equipped item into another.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original item ID. | 2 |
| [`to`](./Enums.md#enum-to) | Enum | The new item ID. | 2 |

</details>


### Object: `TransformWeapon`


**Definition:** Transforms the equipped weapon into another specific weapon state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#object-applytosourceonkill)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | The original weapon ID. | 4 |
| [`to`](./Enums.md#enum-to) | Enum | The transformed weapon ID. | 4 |

</details>


### Object: `TwisterDisplaceWithDamage`


**Definition:** A whirlwind effect that randomly displaces targets and deals damage.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`damage`](./Abilities_and_Spells.md#object-damage) | Mixed | The damage formula or inherit flag. | 12 |
| `max_dist` | Number | Maximum displacement distance. | 12 |
| `min_dist` | Number | Minimum displacement distance. | 4 |
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum |  | 2 |

</details>


### Object: `UseAbility`


**Definition:** Forces the character or target to instantly use a specified ability.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | The ID of the ability to trigger. | 4 |
| `respect_prime` | Boolean | If true, respects the ability's prime/cooldown state. | 4 |

</details>


### Object: `UseMoveAbilityWithAI`


**Definition:** Forces the character to execute a movement ability using specific AI weights.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | ID of the ability to trigger or reference. | 2 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | The AI positioning logic profile to use. | 2 |

</details>


### Object: `VisualCountDownThenApplyStatus`


**Definition:** Displays a visual countdown above the target before applying the nested effects.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 0 |

</details>


### Object: `WaggleClone`


**Definition:** Spawns visual clones or alternative hitbox variants of the projectile.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#object-effects)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cWaggle`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Flag |  | 2 |
| [`cWaggle2x2`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Flag |  | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |
| [`cWaggle3x3`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Flag |  | 1 |

</details>


### Object: `XIsSpellStormRampAndReset`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#object-bonus_passives)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reset_percent` | Number | The percentage of stacks to keep after resetting. | 2 |
| `stacks` | Number | Number of stacks or intensity to apply. | 2 |

</details>


### Object: `XIsTargetHealth`


**Definition:** Math variable assignment: Evaluates X as the target's current health.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#object-conditional_boss), [`Else`](./Abilities_and_Spells.md#object-else)

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |

</details>


