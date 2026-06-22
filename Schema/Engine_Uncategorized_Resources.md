# Engine: Uncategorized & Structural Resources

> These identifiers appear in the `Passive Identifiers.txt` list but are **not** part of the standard `passive_pool`. They exist as structural property contexts or known scalar values in other sections. Entries with a full property table have their own structured block; others are listed with the contexts where they appear as a property key value.

---

## Conditionals & Logic (36)

### `Conditional_AbilityTargetIsSelf`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Conditional_AbilityTargetIsSelf` | Block | Conditional constraint. Nested properties only trigger if this is true. | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Conditional_ActiveWeather_Any`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | {'type': '`Block`', 'df': 'Removes an equipped item and replaces it with a parasite from a specified pool. | 1 |
| [`weather`](./Arrays.md#array-weather) | Array | {'type': '`Array`', 'df': 'An array of weather states to check against.'} | 1 |

</details>


---

### `Conditional_AffectedByElement`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'The specific element type to check for.'} | 3 |
| `BonusCritChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusCritChance' effect/state."} | 2 |
| `Burn` | Number | {'type': '`Number`', 'df': "Applies or references the 'Burn' effect/state."} | 1 |
| [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative) | Block | {'type': '`Block`', 'df': "A simulation block used by the AI to test hypothetical outcomes before committing to an action. | 1 |

</details>


---

### `Conditional_Backstab`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusCritChance` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusCritChance' effect/state."} | 1 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 1 |

</details>


---

### `Conditional_BossOrBig`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Immobile`](./Arrays.md#array-immobile) | Array | {'type': '`Array`', 'df': "Applies or references the 'Immobile' effect/state."} | 2 |

</details>


---

### `Conditional_Buddy`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is currently in the specified transformation form. | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | {'type': 'Block', 'df': 'State block triggered when this object or entity is eaten/consumed by another character.'} | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 1 |

</details>


---

### `Conditional_CanBeHealed`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': 'Selects and applies a random status effect from the provided nested block. | 1 |

</details>


---

### `Conditional_DebuffRoll`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DestroyEquipmentAndAttachParasite`](./Abilities_and_Spells.md#context-destroyequipmentandattachparasite) | Block | {'type': '`Block`', 'df': 'Removes an equipped item and replaces it with a parasite from a specified pool. | 1 |
| `odds` | Number | {'type': '`Number`', 'df': 'The probability (0.0 to 1.0) of applying the debuff.'} | 1 |

</details>


---

### `Conditional_DestructibleCorpse`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyToTile`](./Abilities_and_Spells.md#context-applytotile) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 2 |
| `VaporizeCorpse` | Number | {'type': '`Number`', 'df': "Applies or references the 'VaporizeCorpse' effect/state."} | 2 |

</details>


---

### `Conditional_Displaceable`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`LaunchOffScreen`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'LaunchOffScreen' effect/state."} | 1 |
| `LaunchOffScreenInstakill` | Number | {'type': '`Number`', 'df': "Applies or references the 'LaunchOffScreenInstakill' effect/state."} | 1 |
| `TempInitiativeChange` | Number | {'type': '`Number`', 'df': "Applies or references the 'TempInitiativeChange' effect/state."} | 1 |

</details>


---

### `Conditional_Familiar`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |
| `BonusDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |

</details>


---

### `Conditional_FinishedSpawning`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'Imprison' effect/state."} | 1 |

</details>


---

### `Conditional_Flying`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Conditional_Flying` | Block | Examples: `{ ... }` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Conditional_FormulaIsPositive`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`formula`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'The math expression to evaluate.'} | 8 |
| [`Burn`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'Burn' effect/state."} | 2 |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies or references the 'Immobile' effect/state."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 2 |
| `Freeze` | Number | {'type': '`Number`', 'df': "Applies or references the 'Freeze' effect/state."} | 1 |
| [`OverrideKnockbackDamage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'OverrideKnockbackDamage' effect/state."} | 1 |
| [`Slow`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'Slow' effect/state."} | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 1 |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies or references the 'Stun' effect/state."} | 1 |

</details>


---

### `Conditional_HasCleansableDebuffs`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GenericBuff` | Number | {'type': '`Number`', 'df': "Applies or references the 'GenericBuff' effect/state."} | 1 |
| `PartialCleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'PartialCleanse' effect/state."} | 1 |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': 'Selects and applies a random status effect from the provided nested block. | 1 |

</details>


---

### `Conditional_HasKnockback`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#context-knockupandaway) | Block | {'type': '`Block`', 'df': 'Logic: Applies vertical and horizontal displacement. | 1 |
| `RemoveKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'RemoveKnockback' effect/state."} | 1 |
| [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#context-temppassiveuntilsettled) | Block | {'type': '`Block`', 'df': 'Passive: Active only until the physics engine stops moving the character. | 1 |

</details>


---

### `Conditional_HealthThreshold`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `threshold_flat` | Number | {'type': '`Number`', 'df': 'A flat numerical health value threshold.'} | 4 |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'SpawnThingIfHitKills' effect/state."} | 2 |
| `threshold_percent` | Number | {'type': '`Number`', 'df': 'A percentage-based health threshold (e.g. 50%).'} | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`BonusDamage`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `CaptureFamiliar` | Number | {'type': '`Number`', 'df': "Applies or references the 'CaptureFamiliar' effect/state."} | 1 |
| `Die` | Number | {'type': '`Number`', 'df': "Applies or references the 'Die' effect/state."} | 1 |
| `DieViolently` | Number | {'type': '`Number`', 'df': "Applies or references the 'DieViolently' effect/state."} | 1 |
| `FactionConversion` | Number | {'type': '`Number`', 'df': "Applies or references the 'FactionConversion' effect/state."} | 1 |
| `FlatLeech` | Number | {'type': '`Number`', 'df': "Applies or references the 'FlatLeech' effect/state."} | 1 |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies or references the 'FullHeal' effect/state."} | 1 |
| `Instakill` | Number | {'type': '`Number`', 'df': "Applies or references the 'Instakill' effect/state."} | 1 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 1 |
| [`threshold_expr`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `Conditional_InForm`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum | {'type': '`Enum/String`', 'df': 'The specific form ID to check for.'} | 7 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | {'type': '`Enum/String`', 'df': 'Transforms the character into a different state or form (e.g., Rage, HasCat).'} | 5 |
| `CritChanceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CritChanceUp' effect/state."} | 1 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 1 |
| `DodgeChance_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'DodgeChance_Status' effect/state."} | 1 |
| [`ForceImmediateMoveAndAttack`](./Abilities_and_Spells.md#context-forceimmediatemoveandattack) | Block | {'type': '`Block`', 'df': 'Forces the character to immediately move to a target and use a specified ability. | 1 |
| `SpeedUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpeedUp' effect/state."} | 1 |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | {'type': '`Enum/String`', 'df': 'Forces the character or target to instantly use a specified ability.'} | 1 |

</details>


---

### `Conditional_IsPhysicalAttack`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#context-addstatustoreceiveddamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Characters_and_Bosses.md#context-knockupandaway) | Block | {'type': '`Block`', 'df': 'Logic: Applies vertical and horizontal displacement. | 1 |
| `RemoveKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'RemoveKnockback' effect/state."} | 1 |
| [`TempPassiveUntilSettled`](./Characters_and_Bosses.md#context-temppassiveuntilsettled) | Block | {'type': '`Block`', 'df': 'Passive: Active only until the physics engine stops moving the character. | 1 |

</details>


---

### `Conditional_IsSelf`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideDamage' effect/state."} | 1 |

</details>


---

### `Conditional_IsTrample`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetKnockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetKnockback' effect/state."} | 1 |

</details>


---

### `Conditional_LastHit`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](./Abilities_and_Spells.md#context-knockupandaway) | Block | {'type': '`Block`', 'df': 'Displaces the target vertically and horizontally away from the source. | 2 |
| `BonusDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 1 |
| [`DelayCastAbility`](./Enums.md#enum-delaycastability) | Enum | {'type': '`Enum/String`', 'df': 'Queues an ability to be cast automatically after a certain delay or trigger.'} | 1 |

</details>


---

### `Conditional_LivingPlayerCat`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`Consumed`](./Abilities_and_Spells.md#context-consumed) | Block | {'type': '`Block`', 'df': 'State block triggered when this object or entity is eaten/consumed by another character. | 1 |
| [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus) | Block | {'type': '`Block`', 'df': "Grants nested passives only while the character possesses the specified status. | 1 |

</details>


---

### `Conditional_ManaThreshold`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairTrinket' effect/state."} | 1 |
| `threshold_flat` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `Conditional_NotAlly`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Confusion` | Number | {'type': '`Number`', 'df': "Applies or references the 'Confusion' effect/state."} | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 1 |

</details>


---

### `Conditional_NotBig`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | Number | {'type': '`Number`', 'df': "Applies or references the 'DisplaceTowardsSource' effect/state."} | 1 |

</details>


---

### `Conditional_NotBossOrBig`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Immobile` | Number | {'type': '`Number`', 'df': "Applies or references the 'Immobile' effect/state."} | 2 |

</details>


---

### `Conditional_NotShielded`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Knockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'Knockback' effect/state."} | 2 |

</details>


---

### `Conditional_Object`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag) | Block | {'type': 'Block', 'df': 'Conditional trigger: Executes nested logic if the target possesses the specified entity tag.'} | 3 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 3 |
| [`CanApplyToInanimate`](./Abilities_and_Spells.md#context-canapplytoinanimate) | Block | {'type': 'Block', 'df': 'Modifier block that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters.'} | 1 |
| `RepairWeapon` | Number | {'type': '`Number`', 'df': "Applies or references the 'RepairWeapon' effect/state."} | 1 |

</details>


---

### `Conditional_OncePerBattle`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'CompleteItemQuest' effect/state."} | 2 |
| `TriggerGameEnding` | Number | {'type': '`Number`', 'df': "Applies or references the 'TriggerGameEnding' effect/state."} | 2 |
| [`key`](./Enums.md#enum-key) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>


---

### `Conditional_PlayerCat`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ConjureRandomAbilityFromCat` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConjureRandomAbilityFromCat' effect/state."} | 2 |
| `Adrenaline` | Number | {'type': '`Number`', 'df': "Applies or references the 'Adrenaline' effect/state."} | 1 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| `Cleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'Cleanse' effect/state."} | 1 |
| `GenericDebuff` | Number | {'type': '`Number`', 'df': "Applies or references the 'GenericDebuff' effect/state."} | 1 |
| [`KnockOutClone`](./Enums.md#enum-knockoutclone) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'KnockOutClone' effect/state."} | 1 |
| `Scrambled` | Number | {'type': '`Number`', 'df': "Applies or references the 'Scrambled' effect/state."} | 1 |
| `T2CopyCat` | Number | {'type': '`Number`', 'df': "Applies or references the 'T2CopyCat' effect/state."} | 1 |

</details>


---

### `Conditional_RandomChance`
> Found in: *Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyPassives`](./Abilities_and_Spells.md#context-applypassives) | Block | {'type': '`Block`', 'df': "Grants the nested passive abilities dynamically. | 1 |
| `odds` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |

</details>


---

### `Conditional_SourceAbilityHasTag`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |
| [`ScatterCoins`](./Abilities_and_Spells.md#context-scattercoins) | Block | {'type': '`Block`', 'df': 'Throws coins out into the level randomly. | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 1 |

</details>


---

### `Conditional_SourceHasStatus`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>


---

### `Conditional_Speculative`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IgnoreDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'IgnoreDamage' effect/state."} | 3 |
| `BonusDamageBasedOnDistance` | Number | {'type': '`Number`', 'df': "Applies or references the 'BonusDamageBasedOnDistance' effect/state."} | 2 |
| [`Conditional_HealthThreshold`](./Abilities_and_Spells.md#context-conditional_healththreshold) | Block | {'type': 'Block', 'df': "Conditional trigger: Executes nested logic if the target's health falls below the specified threshold."} | 2 |
| `BonusDamage` | Number | {'type': 'Number', 'df': "Applies or references the 'BonusDamage' effect/state."} | 1 |
| `CapDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'CapDamage' effect/state."} | 1 |
| [`Else`](./Abilities_and_Spells.md#context-else) | Block | {'type': 'Block', 'df': 'Fallback block that executes if the preceding `Conditional_` block evaluated to false.'} | 1 |
| `Knockback` | Number | {'type': '`Number`', 'df': "Applies or references the 'Knockback' effect/state."} | 1 |
| `RandomBonusDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomBonusDamage' effect/state."} | 1 |

</details>


---

### `Conditional_Tiny`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Conditional_Tiny` | Block | Examples: `{ ... }` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Reactions & Event Triggers (77)

### `AbilityAfterEnemyCastSpell_Stackable`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityAfterEnemyCastSpell_Stackable` | Enum | Examples: `ThornUpX, ThornUp` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityOnBattleStart_Immediate`
> Found in: *Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 34

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityOnBattleStart_Immediate` | Enum | Examples: `SummonBrambles2, FlowerEventSleep, BrambleRandomTileEvent` | 34 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityOnBattleStart_UseAI`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityOnBattleStart_UseAI` | Enum | Examples: `TheCreator_SpawnCloneTeam` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityOnRoundEnd`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| `force_display_name` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |

</details>


---

### `AbilityOnRoundEndOnce`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 1 |
| `even_of_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `AllUnitsExplodeOnDeath`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllUnitsExplodeOnDeath` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlliesScrambleSpellAfterCast`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlliesScrambleSpellAfterCast` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyToSourceOnKill`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveItem' effect/state."} | 3 |
| `AlphaCat` | Number | {'type': '`Number`', 'df': "Applies or references the 'AlphaCat' effect/state."} | 2 |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'CompleteItemQuest' effect/state."} | 2 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 2 |
| `ManaGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'ManaGain' effect/state."} | 2 |
| `Revive` | Number | {'type': '`Number`', 'df': "Applies or references the 'Revive' effect/state."} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |
| [`EvolveAbilityFromPool`](./Enums.md#enum-evolveabilityfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Upgrades or transforms an existing ability into a new one from the specified pool.'} | 1 |
| `RefreshActPoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshActPoints' effect/state."} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 1 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'TakeExtraTurn' effect/state."} | 1 |
| [`TransformWeapon`](./Abilities_and_Spells.md#context-transformweapon) | Block | {'type': '`Block`', 'df': 'Transforms the equipped weapon into another specific weapon state. | 1 |
| [`WeaponAuxMultiplier`](./Enums.md#enum-weaponauxmultiplier) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'WeaponAuxMultiplier' effect/state."} | 1 |

</details>


---

### `ArmorBreakOnHit`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance_to_break` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `durability_loss` | Number | {'type': '`Number`', 'df': ''} | 2 |

</details>


---

### `BackflipWhenTargeted`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific dodge ability to trigger (e.g., DestroyerDodge).'} | 4 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 4 |

</details>


---

### `BonusAbility_DelayedApplication`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusAbility_DelayedApplication` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BramblesOnHit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BramblesOnHit` | Number | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CanLevelUpWhenDead`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CanLevelUpWhenDead` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChanceToSpitOnDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 7 |
| `flat_chance` | Number | {'type': '`Number`', 'df': ''} | 5 |
| `chance_per_damage` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `backstabs_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `even_on_0_damage_if_knockback` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `ChangeTileOnDeath`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChangeTileOnDeath` | Enum | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CherubimReaction`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Leave`](./Enums.md#enum-leave) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'Leave' effect/state."} | 2 |
| [`Return`](./Enums.md#enum-return) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'Return' effect/state."} | 2 |

</details>


---

### `CounterAttackAfterEnemyCastSpell`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CounterAttackAfterEnemyCastSpell` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CounterNextAttacks`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CounterNextAttacks` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Counterspell`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Counterspell` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CrackMoonHead`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CrackMoonHead` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeathRattleRevive`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 8 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |

</details>


---

### `DelayedAutoRevive`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `health` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `rounds` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `DelayedFury`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DelayedFury` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DelayedPain`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DelayedPain` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DelayedWindTrail`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DelayedWindTrail` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DieWhenOnlyGolemsLeft`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DieWhenOnlyGolemsLeft` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Divide4OnDeath`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Divide4OnDeath` | Enum | Examples: `Clot, MedSlime, BiggestFood` | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleCastSpellIfManaCostUnderThreshold`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpellIfManaCostUnderThreshold` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleCastSpellThisTurn`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleCastSpellsEachTurn_Status`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpellsEachTurn_Status` | Number | Applies or references the  | 3 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DustOnHit`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the object/particle to spawn.'} | 3 |

</details>


---

### `EnrageOnDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EnrageOnDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FindExtraItemFromPoolOnBattleEnd`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FindExtraItemFromPoolOnBattleEnd` | Enum | Examples: `combat_reward_easy, pills` | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlatHealWhenDealDamage`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FlatHealWhenDealDamage` | Number | Examples: `1` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlowersOnHit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FlowersOnHit` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FreeFirstCastAndAfterSpendMana`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FreeFirstCastAndAfterSpendMana` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainManaWhenAnythingDies`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GainManaWhenAnythingDies` | Number | Examples: `1` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ImmediateAbilityReaction`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 13 |
| `ability_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `backstabs_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `damage_threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `even_if_blocked` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `health_threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `buddy_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `target_furthest_valid` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `IncAuxCounterClamped`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `max` | Number | {'type': '`Number`', 'df': ''} | 3 |

</details>


---

### `IncAuxCounterCycle`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `change` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `max` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `IncreaseItemAuxOnKill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IncreaseItemAuxOnKill` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MadnessChanceOnTurnBegin`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MiniVolcanoReaction`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MiniVolcanoReaction` | Enum | Examples: `ThrobShot_Reaction, MiniVolcano_Spurt` | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MonkCatReactionAbilities`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`spell`](./Enums.md#enum-spell) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`trinket`](./Enums.md#enum-trinket) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`weapon`](./Enums.md#enum-weapon) | Enum | {'type': '`Enum/String`', 'df': 'Weapon item constraint.'} | 1 |

</details>


---

### `MoonHeadCrackedVisual`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MoonHeadCrackedVisual` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MoonHeadFinisherEnabler`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MoonHeadFinisherEnabler` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MutateAfterXTurns`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MutateAfterXTurns` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ObjectOnHit`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID of the object to spawn (e.g., Poop).'} | 2 |

</details>


---

### `ObjectOnHitEmpty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ObjectOnHitEmpty` | Enum | Examples: `SmallRock, AnimalEgg2, AnimalEgg` | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ObjectOnHitFullyEmpty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ObjectOnHitFullyEmpty` | Enum | Examples: `RandomArmorPickup` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PassiveWhenDead`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToTrampleDamage`](./Characters_and_Bosses.md#context-addstatustotrampledamage) | Block | {'type': '`Block`', 'df': "Modifier: Injects a status effect into the character's trample damage. | 1 |

</details>


---

### `PassiveWhenOnTile`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | {'type': '`Block`', 'df': 'Passives granted by equipping this. | 6 |
| [`tile`](./Arrays.md#array-tile) | Array | {'type': '`Array`', 'df': ''} | 6 |

</details>


---

### `PreEmptiveCounterNextAttacks`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PreEmptiveCounterNextAttacks` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReformMoonHead`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReformMoonHead` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnKill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnKill` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnKillEnemy`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnKillEnemy` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnKillTagged`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnKillTagged` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairOnKill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RepairOnKill` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReplaceBlankTilesOnBattleStart`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReplaceBlankTilesOnBattleStart` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RerollItemsOnBattleEnd`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RerollItemsOnBattleEnd` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReturnBoundItemOnBattleEnd`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReturnBoundItemOnBattleEnd` | Number | Applies or references the  | 3 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SoundEventOnHit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SoundEventOnHit` | Enum | Examples: `Batterup_Connect` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatusAfterXStacks`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `ExtraBasicMoves_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'ExtraBasicMoves_Status' effect/state."} | 1 |
| `RefreshActPoints` | Number | {'type': '`Number`', 'df': "Applies or references the 'RefreshActPoints' effect/state."} | 1 |
| `expires_on_end_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `StatusAfterXTurns`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': 'Logic: Forces the execution of a specific ability.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `StatusCharactersOnRoundEnd`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./Miscellaneous.md#context-conditional_goodroll) | Block | Examples: `{ ... }` | 1 |
| `FloatingRockTrap` | Number | Examples: `1` | 1 |
| `Thorns` | Number | Examples: `1` | 1 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Examples: `rock` | 1 |

</details>


---

### `StatusCharactersOnRoundStart`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./Miscellaneous.md#context-conditional_goodroll) | Block | Examples: `{ ... }` | 1 |
| [`Else`](./Miscellaneous.md#context-else) | Block | Examples: `{ ... }` | 1 |
| [`Madness`](./Arrays.md#array-madness) | Array | Examples: `[ 1 .25 ]` | 1 |

</details>


---

### `StatusOnEnemyCastSpell`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | Examples: `1` | 1 |
| `HealthGain` | Number | Examples: `1` | 1 |

</details>


---

### `StatusRandomEnemiesOnBattleStart`
> Found in: *Events & Encounters, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `count` | Number | {'type': '`Number`', 'df': 'Quantity.'} | 3 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 2 |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 1 |

</details>


---

### `TempCounterAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempCounterAttack` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempPreEmptiveCounterAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempPreEmptiveCounterAttack` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerBleedOnBleed`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TriggerBleedOnBleed` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerDOTStatuses`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TriggerDOTStatuses` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerGameEnding`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TriggerGameEnding` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerMotherConsume`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TriggerMotherConsume` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerMotherGrow`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TriggerMotherGrow` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UnlimitedDeathRattleRevive`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `UseAbilityWhenOutOfStatus`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>


---

## Stat Modifiers & Scaling (180)

### `AIFavorLowHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AIFavorLowHealth` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityDamageMultiplier`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityDamageMultiplier` | Number | Examples: `1.5` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledAtHealthThreshold`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledAtHealthThreshold` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfHasStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledIfHasStatus` | Enum | Examples: `DemonicGlyph_Bite, DemonicGlyph_Summon` | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfNotHasStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledIfNotHasStatus` | Enum | Examples: `BackflipWhenTargeted` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledOncePerFightAtHealthThreshold`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Number | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityHealthThreshold`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 12 |
| `threshold` | Mixed | {'type': '`Number`', 'df': ''} | 11 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 6 |
| `immediate` | Boolean | {'type': '`Boolean`', 'df': ''} | 5 |
| `use_ai` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `also_use_if_buddy_is_dead` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`threshold_min`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `AbsorbManaFromOtherSpells`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbsorbManaFromOtherSpells` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddAdvantageToEvent`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `add` | Number | {'type': '`Number`', 'df': ''} | 1 |
| [`options`](./Arrays.md#array-options) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'Classification type.'} | 1 |

</details>


---

### `AddConstitution`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddConstitution` | Number | Examples: `2` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddDamage` | Number | Applies or references the  | 16 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddElementsToSpells`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddElementsToSpells` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddEndOfCombatRegen`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddEndOfCombatRegen` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddLeechesStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddLeechesStatus` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddPostProcessEffect`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean | Examples: `false` | 1 |
| [`shader`](./Enums.md#enum-shader) | Enum | Examples: `shimmervignette` | 1 |

</details>


---

### `AddSpiritBombCharges`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddSpiritBombCharges` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddStatusToBackstabs`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bleed` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bleed' effect/state."} | 1 |

</details>


---

### `AddStatusToFirstSpellEachTurn`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](./Miscellaneous.md#context-conditional_isself) | Block | Examples: `{ ... }` | 1 |
| [`Else`](./Miscellaneous.md#context-else) | Block | Examples: `{ ... }` | 1 |

</details>


---

### `AddStatusToReceivedDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack) | Block | {'type': '`Block`', 'df': "Conditional: Executes logic if the triggering attack is physical. | 1 |
| [`Else`](./Characters_and_Bosses.md#context-else) | Block | {'type': '`Block`', 'df': 'Fallback logic block for conditionals. | 1 |

</details>


---

### `AddTilesetObjects`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FloatingDebris`](./Miscellaneous.md#context-floatingdebris) | Block | Examples: `{ ... }` | 1 |

</details>


---

### `AddWeaponAux`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddWeaponAux` | Mixed | Examples: `"-max(min(X+1, item_aux), 0)", 1, -item_aux` | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsLastEnemyThatDealtDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AggroTargetIsLastEnemyThatDealtDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsLowestHealthEnemyTillItDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsLowestMaxHealthCat`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AggroTargetIsLowestMaxHealthCat` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllSpellsCostActPoints`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllSpellsCostActPoints` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllSpellsCostCharge`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllSpellsCostCharge` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllStatsUpPerDisorder`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUpPerDisorder` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlwaysChosenForLevelUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlwaysChosenForLevelUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyMultipleTimes`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool) | Block | {'type': '`Block`', 'df': 'Selects and applies a random status effect from the provided nested block. | 3 |
| `stacks` | Mixed | {'type': '`Number`', 'df': 'The number of times the nested effects block should be repeatedly executed.'} | 3 |

</details>


---

### `ApplyStatusesNextTurnBegin`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'Quivered' effect/state."} | 1 |

</details>


---

### `BalanceStats`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BalanceStats` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BaseStatMultiply`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BaseStatMultiply` | Enum | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusDamageBasedOnDistance`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusDamageBasedOnDistance` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusDamageBasedOnMana`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusDamageBasedOnMana` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusHealthRegenPerDisorder`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusHealthRegenPerDisorder` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusTurnPattern`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusTurnPattern` | Array | Examples: `[ { evenly_dispersed_bonus_turns 1 round_end_bonus_turns ..., [ { dispersed_b...` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BoostReceivedHealing`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BoostReceivedHealing` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleCharismaUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BrittleCharismaUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleConstitutionUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BrittleConstitutionUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleDexterityUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BrittleDexterityUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleIntelligenceUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BrittleIntelligenceUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleLuckUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BrittleLuckUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleSpeedUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BrittleSpeedUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleStrengthUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BrittleStrengthUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CantSpreadDiseases`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CantSpreadDiseases` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CapBasicAttackDamage`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CapBasicAttackDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CapDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CapDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CapReceivedDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CapReceivedDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CastAgainWithStatus`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverrideDamage` | Number | {'type': '`Number`', 'df': "Applies or references the 'OverrideDamage' effect/state."} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `CatPartsSizeScale`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `head` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `CatPartsSizeScaleStatus`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `arm1` | Number | {'type': '`Number`', 'df': 'Scale multiplier for the front arm.'} | 1 |
| `arm2` | Number | {'type': '`Number`', 'df': 'Scale multiplier for the back arm.'} | 1 |
| `body` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `mouth` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `CharacterTypeGainsStatusAtBattleStart`
> Found in: *Events & Encounters, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 5 |
| `Fear` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fear' effect/state."} | 2 |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies or references the 'Stun' effect/state."} | 2 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |

</details>


---

### `ChargeFists`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChargeFists` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CharismaIsMaxStat`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CharismaIsMaxStat` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ConjureBonusAbility`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to conjure.'} | 2 |
| `upgraded` | Boolean | {'type': '`Boolean`', 'df': 'If true, conjures the upgraded version of the ability.'} | 2 |

</details>


---

### `ConjureSingleUseBonusAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ConjureSingleUseBonusAbility` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ContextualHeal`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ContextualHeal` | Number | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ConvertDamageToScaledStatus`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DelayedPain` | Number | {'type': '`Number`', 'df': "Applies or references the 'DelayedPain' effect/state."} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `CurrentWeaponAddElectricElement`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponAddElectricElement` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CurrentWeaponAddPoison`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponAddPoison` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageBasedOnMissingHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageBasedOnMissingHealth` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageFromBehindOnly`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageFromBehindOnly` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageTrinket`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageTrinket` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageWeapon`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageWeapon` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoDamage`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The flat damage amount.'} | 5 |
| [`type`](./Enums.md#enum-type) | Enum | {'type': '`Enum/String`', 'df': 'The classification of the damage (e.g., spell, melee).'} | 5 |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`effects`](./Abilities_and_Spells.md#context-effects) | Block | {'type': '`Block`', 'df': 'Non-damaging status applications and logic triggers executed on impact. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array | {'type': '`Array`', 'df': ''} | 2 |

</details>


---

### `DontHealEnemies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DontHealEnemies` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleReceivedNegativeStatus`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleReceivedNegativeStatus` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleReceivedPositiveStatus`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleReceivedPositiveStatus` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleStatus` | Enum | Examples: `Bleed, Poison, Burn` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DuplicateRandomEquippedItem`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DuplicateRandomEquippedItem` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExistUntilIdleUpkeep`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExistUntilIdleUpkeep` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExtraBasicAttacks_Status`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExtraBasicAttacks_Status` | Number | Applies or references the  | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FaceAwayLastDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `override_hit_animation` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `use_turn_animations` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `FaceLastDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `FactionUprising`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`extra_statuses`](./Miscellaneous.md#context-extra_statuses) | Block | Examples: `{ ... }` | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | Examples: `bird` | 1 |

</details>


---

### `FlatAIBonus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FlatAIBonus` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalMeleeRevengeDamage`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `HPAltStates`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>


---

### `HealNeighborsEachTurn`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `HealPercentMaxHP`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealPercentMaxHP` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HealRandomInjury`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealRandomInjury` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HealTo`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealTo` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HealthMultiplier`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthMultiplier` | Mixed | Examples: `1.5, .5, .8` | 15 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IgnoreDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IgnoreDamage` | Number | Applies or references the  | 18 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IncreaseCumulativeBlastDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IncreaseCumulativeBlastDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `InstantMaxHealthUp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `InstantMaxHealthUp` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JesterLevelUpRerolls`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `JesterLevelUpRerolls` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KnockUpAndAway`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Conditional_LastHit`](./Abilities_and_Spells.md#context-conditional_lasthit), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `distance` | Number | {'type': '`Number`', 'df': 'The distance in tiles to knock the target away.'} | 20 |
| `stacks` | Mixed | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 18 |
| `height` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `circular_variance` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `LateStatusApplication`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'CurrentWeaponDamageUp' effect/state."} | 3 |
| `AddWeaponAux` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddWeaponAux' effect/state."} | 1 |

</details>


---

### `LowGravityRangeBoost`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LowGravityRangeBoost` | Number | Examples: `2` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManaGainRange`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `min` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `MaxHPUp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MaxHPUp` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MergeDamageInstance`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean | {'type': '`Boolean`', 'df': 'If false, prevents the damage from instantly popping the target.'} | 1 |
| `force_no_hit_animation` | Boolean | {'type': '`Boolean`', 'df': 'If true, suppresses the flinch/hit animation.'} | 1 |

</details>


---

### `MulticatHeads`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MulticatHeads` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MultiplyReceivedHealing`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MultiplyReceivedHealing` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextAbilityHeals`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NextAbilityHeals` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextActionLuckUp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NextActionLuckUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextAttackBonusRange`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NextAttackBonusRange` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextAttackSpecialCrit`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Number | {'type': '`Number`', 'df': 'Flat addition to the critical damage multiplier.'} | 1 |
| `extra_coins_per_stack` | Number | {'type': '`Number`', 'df': 'Grants bonus coins based on stacks.'} | 1 |
| `luck_increase` | Number | {'type': '`Number`', 'df': 'Increases luck stat for the attack.'} | 1 |

</details>


---

### `NextBattleStatusStacks`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Number | {'type': '`Number`', 'df': "Applies or references the 'MadnessChanceOnTurnBegin' effect/state."} | 1 |
| `fights` | Number | {'type': '`Number`', 'df': 'The number of encounters this buff/debuff persists for.'} | 1 |

</details>


---

### `NextDamageReduceAndHealAllies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NextDamageReduceAndHealAllies` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextTurnDoubleRangedDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NextTurnDoubleRangedDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NoHealthRegen`
> Found in: *Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NoHealthRegen` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `OverHealToStatuses`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomStatUp' effect/state."} | 1 |
| `TakeExtraTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'TakeExtraTurn' effect/state."} | 1 |
| `stack_scale` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `OverManaReducesManaCosts`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverManaReducesManaCosts` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PassiveWhileHasStatus`
> Found in: *Cat Mutations, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Cat_Mutations.md#context-passives) | Block | Examples: `{ ... }` | 1 |
| [`status`](./Enums.md#enum-status) | Enum | Examples: `Bleed` | 1 |

</details>


---

### `PassiveWhileNotHasStatus`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | {'type': '`Block`', 'df': "Block listing intrinsic passive modifiers. | 2 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 2 |

</details>


---

### `PermanentUpgradeRandomActive`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentUpgradeRandomActive` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PermanentUpgradeRandomActiveOrPassive`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentUpgradeRandomActiveOrPassive` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RNGCannonRandomDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RNGCannonRandomDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomBonusDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomBonusDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomPermanentStatsDistinct`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEatPill`](./Miscellaneous.md#context-statusoneatpill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stats`](./Arrays.md#array-stats) | Array | Examples: `[ 1 -1 ]` | 1 |

</details>


---

### `RandomSeededStatModifier`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomSeededStatModifier` | Array | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomStatDown`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomStatDown` | Array | Examples: `"ceil(X/3)", "ceil(X/2)"` | 20 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RebukeDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RebukeDamage` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReduceManaCostExcludeBrainstorm`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReduceManaCostExcludeBrainstorm` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReduceSpellCostsPerDisorder`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReduceSpellCostsPerDisorder` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReduceSpellCostsPerParasite`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReduceSpellCostsPerParasite` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RefreshNonManaItemAbilities`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RefreshNonManaItemAbilities` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnAnyDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnAnyDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnElementalDamageReceived`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnElementalDamageReceived` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnSpendMana`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnSpendMana` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnTotalDamageReceived`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnTotalDamageReceived` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnUseAbilityWithManaCost`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnUseAbilityWithManaCost` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoteFlatLeech`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoteFlatLeech` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoteLeech`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoteLeech` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScaledStatusAlliesOnSpendMana`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](./Items_and_Equipment.md#context-conditional_adjacent) | Block | {'type': '`Block`', 'df': 'Conditional constraint. Nested properties only trigger if this is true. | 1 |

</details>


---

### `SelfStatusCarefulness`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SelfStatusCarefulness` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetHealth`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetHealth` | Number | Applies or references the  | 18 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShadowCrit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ShadowCrit` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShowFakeDamage`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |
| [`style`](./Arrays.md#array-style) | Array | {'type': '`Array`', 'df': 'The visual font style for the text (e.g., [crit]).'} | 1 |

</details>


---

### `SpeedUp_WithoutInitiative`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpeedUp_WithoutInitiative` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StanceSwitchToRanged`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StanceSwitchToRanged` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatBounty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StatBounty` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatDependentPassive`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddDamageToBasicAttack`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': "Applies or references the 'AddDamageToBasicAttack' effect/state."} | 1 |

</details>


---

### `StatusAdjacentOnTheirTurnEnd`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveAway' effect/state."} | 1 |

</details>


---

### `StatusCollector`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 7 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies or references the 'Poison' effect/state."} | 4 |
| `Slow` | Number | {'type': '`Number`', 'df': "Applies or references the 'Slow' effect/state."} | 4 |

</details>


---

### `StatusEachRoundBegin`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number | Examples: `12, 4, 8` | 8 |

</details>


---

### `StatusEachRoundEnd`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | Examples: `Spit` | 1 |

</details>


---

### `StatusEachTurnBeginIfHasStatus`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |
| `DamageUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DamageUp' effect/state."} | 1 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 1 |
| [`animation`](./Enums.md#enum-animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `consume` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>


---

### `StatusEachTurnEndIfEnabledAtStartOfTurn`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': 'Logic: Forces the execution of a specific ability.'} | 1 |

</details>


---

### `StatusEveryXSpellCastsEachTurn`
> Found in: *Cat Mutations, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | Examples: `2` | 1 |
| `stacks` | Number | Examples: `3` | 1 |

</details>


---

### `StatusIfUnusedActPoints`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`BackflipWhenTargeted`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack.'} | 1 |
| [`Craft`](./Items_and_Equipment.md#context-craft) | Block | {'type': '`Block`', 'df': 'Synthesizes or spawns a new item from a specific pool. | 1 |

</details>


---

### `StatusOnBackstab`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 1 |
| `SerratedClaws` | Number | {'type': '`Number`', 'df': "Applies or references the 'SerratedClaws' effect/state."} | 1 |

</details>


---

### `StatusOnBreak`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`GainCoinsRange`](./Items_and_Equipment.md#context-gaincoinsrange) | Block | {'type': '`Block`', 'df': 'Grants the player a randomized amount of coins within a min/max range. | 5 |
| `Bruise` | Number | {'type': '`Number`', 'df': "Applies or references the 'Bruise' effect/state."} | 3 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ChangeTilesUnder' effect/state."} | 3 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | {'type': '`Enum/String`', 'df': 'Generates an item drop from the specified loot pool.'} | 3 |
| `HealthGain` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthGain' effect/state."} | 3 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 3 |
| `PermanentConstitution` | Number | {'type': '`Number`', 'df': "Applies or references the 'PermanentConstitution' effect/state."} | 3 |
| [`ApplyToRandomPartyMemberIfPossible`](./Items_and_Equipment.md#context-applytorandompartymemberifpossible) | Block | {'type': '`Block`', 'df': "Redirects the nested effects to apply to a random living member of the player's party. | 1 |
| `ConstitutionUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'ConstitutionUp' effect/state."} | 1 |
| `DexterityUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'DexterityUp' effect/state."} | 1 |
| [`FindItem`](./Enums.md#enum-finditem) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'FindItem' effect/state."} | 1 |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GainDisorder' effect/state."} | 1 |
| `IntelligenceUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'IntelligenceUp' effect/state."} | 1 |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a specific character or entity upon impact.'} | 1 |
| `StrengthUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'StrengthUp' effect/state."} | 1 |

</details>


---

### `StatusOnDie`
> Found in: *Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ScatterCoins`](./Arrays.md#array-scattercoins) | Array | Examples: `5, [ 1 .5 ]` | 6 |

</details>


---

### `StatusOnEnemyConfused`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ImmediateUseAbility' effect/state."} | 1 |

</details>


---

### `StatusOnEnemyDeath`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | {'type': '`Number`', 'df': "Applies or references the 'Charge' effect/state."} | 1 |

</details>


---

### `StatusOnFallAsleep`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 1 |
| `FillMana` | Number | {'type': '`Number`', 'df': "Applies or references the 'FillMana' effect/state."} | 1 |
| `HealRandomInjury` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealRandomInjury' effect/state."} | 1 |

</details>


---

### `StatusOnFullMana`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#context-conditional_onceperbattle) | Block | {'type': '`Block`', 'df': 'Conditional trigger: Executes nested logic only once per encounter/battle. | 1 |

</details>


---

### `StatusOnSetPieceBreak`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | Examples: `rare` | 1 |
| `PermanentCharisma` | Number | Examples: `1` | 1 |
| `PermanentConstitution` | Number | Examples: `1` | 1 |
| `PermanentDexterity` | Number | Examples: `1` | 1 |
| `PermanentIntelligence` | Number | Examples: `1` | 1 |
| `PermanentLuck` | Number | Examples: `1` | 1 |
| `PermanentSpeed` | Number | Examples: `1` | 1 |
| `PermanentStrength` | Number | Examples: `1` | 1 |
| [`set`](./Enums.md#enum-set) | Enum | Examples: `Recycled` | 1 |

</details>


---

### `StatusOverlappingCharactersAndDie`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies or references the 'Poison' effect/state."} | 1 |

</details>


---

### `StripStatuses`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StripStatuses` | Number | Applies or references the  | 20 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SwapHighestAndLowestStat`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SwapHighestAndLowestStat` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TakeBonusTurnWithAIControl`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | {'type': '`Boolean`', 'df': 'If true, allows the AI to cast spells during this bonus turn.'} | 2 |

</details>


---

### `TallTumorManaBurn`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TallTumorManaBurn` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TeamBonusAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TeamBonusAbility` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempCritChanceUp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempCritChanceUp` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempManaCostReduction`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempManaCostReduction` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempMeleeRangeUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempMeleeRangeUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempNoManaRegen`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempNoManaRegen` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempPassiveWhileHasStatus`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ReplaceSpell`](./Abilities_and_Spells.md#context-replacespell) | Block | {'type': '`Block`', 'df': "Replaces a spell in the character's hand/deck with a different one. | 4 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The required status effect.'} | 3 |
| [`MeleeRevengeDamage`](./Abilities_and_Spells.md#context-meleerevengedamage) | Block | {'type': '`Block`', 'df': 'Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 2 |
| `AddManaRegen` | Number | {'type': '`Number`', 'df': "Applies or references the 'AddManaRegen' effect/state."} | 1 |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 1 |

</details>


---

### `TempRangeUp`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempRangeUp` | Number | Applies or references the  | 16 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TickDownStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TickDownStatus` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TimeDelayStatusApplication`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `delay` | Mixed | {'type': '`Number`', 'df': 'The float time delay in seconds.'} | 4 |
| [`SwitchMusic`](./Abilities_and_Spells.md#context-switchmusic) | Block | {'type': '`Block`', 'df': 'Changes the background music track or layer during combat. | 2 |
| `Cleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'Cleanse' effect/state."} | 1 |
| [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers) | Block | {'type': '`Block`', 'df': "Generates global map or encounter rules/modifiers. | 1 |
| [`DoScreenShake`](./Abilities_and_Spells.md#context-doscreenshake) | Block | {'type': '`Block`', 'df': 'Triggers a camera screen shake effect. | 1 |
| [`FormChange`](./Enums.md#enum-formchange) | Enum | {'type': '`Enum/String`', 'df': 'Transforms the character into a different state or form (e.g., Rage, HasCat).'} | 1 |
| `FullHeal` | Number | {'type': '`Number`', 'df': "Applies or references the 'FullHeal' effect/state."} | 1 |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GlobalSpawnCharacter' effect/state."} | 1 |
| `PlayBackground` | Number | {'type': '`Number`', 'df': "Applies or references the 'PlayBackground' effect/state."} | 1 |
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveAmbientLightEffects' effect/state."} | 1 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 1 |

</details>


---

### `TormentorHeal`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TormentorHeal` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TowerDefenseStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TowerDefenseStatus` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TowerDefenseStatus2`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TowerDefenseStatus2` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Trapper_Status`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Trapper_Status` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UndoDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `UndoDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UpTireBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `UpTireBehavior` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UpgradeRandomAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `UpgradeRandomAbility` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VisualCountDownThenApplyStatus`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ForceUseAbility' effect/state."} | 1 |

</details>


---

### `WeaponAuxMultiplier`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `WeaponAuxMultiplier` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsCountStatusStacks`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsCountStatusStacks` | Enum | Examples: `DodgeChance_Status` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsMultipliedPercentHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsMultipliedPercentHealth` | Array | Examples: `[ 6 2 ], [ 14 1 ], [ 1 12 ]` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsOtherHealsThisTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsOtherHealsThisTurn` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsRecycleCostReduction`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsRecycleCostReduction` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsTargetHealth`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`BonusDamage`](./Math_Equations.md) | Equation | {'type': '`String`', 'df': "Applies or references the 'BonusDamage' effect/state."} | 2 |

</details>


---

### `XIsTimesDamageTaken`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsTimesDamageTaken` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Immunities & Defenses (42)

### `AllDamageImmune_IncludingSpeculative`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AllDamageImmune_IncludingSpeculative` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyShieldToApplierBasedOnMaxHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ApplyShieldToApplierBasedOnMaxHealth` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlockAllDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BlockAllDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlockDamageUnderThreshold`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BlockDamageUnderThreshold` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlockNegativeStatus`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BlockNegativeStatus` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BreakWhenNoShield`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BreakWhenNoShield` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CanShield`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CanShield` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChanceToBlock`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChanceToBlock` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CharmImmunity`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CharmImmunity` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DivineShieldPickup`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DivineShieldPickup` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DodgeChanceWithBlindSpot`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DodgeChanceWithBlindSpot` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DodgeChance_Status`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Number | Applies or references the  | 36 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DodgeWhenTargeted`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |

</details>


---

### `ForceDodgeEverything`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceDodgeEverything` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FullBlockEverything`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FullBlockEverything` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FullBlockEverythingTo0Damage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FullBlockEverythingTo0Damage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GoopImmunity`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GoopImmunity` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IceBlockBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IceBlockBehavior` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Invulnerable`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Invulnerable` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KaijuKnockbackImmune`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `KaijuKnockbackImmune` | Number | Applies or references the  | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KnockbackDamageImmuneUntilSettled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `KnockbackDamageImmuneUntilSettled` | Number | Applies or references the  | 20 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MagicDamageImmune`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MagicDamageImmune` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NoHealthOnlyShield`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NoHealthOnlyShield` | Number | Applies or references the  | 24 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NonStackingShield`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number | Examples: `12, 4, 8` | 16 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `OverHealToShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverHealToShield` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PassiveWhileShielded`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'HealthRegenUp' effect/state."} | 1 |

</details>


---

### `ReloadOnGainDivineShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnGainDivineShield` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ResetArmorShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ResetArmorShield` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScaledStatusOnHolyShieldBlock`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Number | {'type': '`Number`', 'df': 'Fires a randomized number of magic missiles.'} | 1 |

</details>


---

### `SetBrittleImmune`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetBrittleImmune` | String | Examples: `JankAlloy, Alloy, Paper` | 7 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetFragileImmune`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetFragileImmune` | String | Examples: `Cardboard, Paper, Cool` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetShield` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpellShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpellShield` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatusOnDodge`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Number | {'type': '`Number`', 'df': "Applies or references the 'DodgeChance_Status' effect/state."} | 1 |

</details>


---

### `StatusOnTakeHealthOrShieldDamage`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array | {'type': '`Array`', 'df': "Applies or references the 'DivineShield' effect/state."} | 2 |
| [`Conditional_GoodRoll`](./Items_and_Equipment.md#context-conditional_goodroll) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 1 |
| `Metronome` | Number | {'type': '`Number`', 'df': 'Executes a random musical or metronome ability.'} | 1 |

</details>


---

### `StunImmunity`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `TempInjuryImmunity`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempInjuryImmunity` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ThornsDamageImmuneUntilSettled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ThornsDamageImmuneUntilSettled` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TileDamageImmuneUntilSettled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TileDamageImmuneUntilSettled` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TileElementDamageImmunity`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TileElementDamageImmunity` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UseAbilityWhenShieldDepleted`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `UseAbilityWhenShieldDepleted` | Enum | Examples: `T3Pebbles_PrimeBoulderDrop` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WispDodge`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `WispDodge` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Auras & Area of Effect (20)

### `AOEBonus`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AOEBonus` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlienBeastDangerZones`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlienBeastDangerZones` | Array | Examples: `[ AlienBeastScream AlienBeastEat AlienBeastPuke AlienBeas...` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllStatsAura`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`range`](./Enums.md#enum-range) | Enum | {'type': '`Enum/String`', 'df': 'Distance or area of effect in tiles.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `AlluringDoodieEater`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| [`damage_instance`](./Items_and_Equipment.md#context-damage_instance) | Block | {'type': '`Block`', 'df': ' | 1 |

</details>


---

### `AllyDodgeChanceAura`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| `range` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 1 |

</details>


---

### `BaitAura`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `range` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 4 |

</details>


---

### `BasicAIDangerZone`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BasicAIDangerZone` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BattlefieldUniqueRandomPassive`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Bite' effect/state."} | 1 |
| `DemonicGlyph_Bounce` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Bounce' effect/state."} | 1 |
| `DemonicGlyph_Fire` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Fire' effect/state."} | 1 |
| `DemonicGlyph_Movement` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Movement' effect/state."} | 1 |
| `DemonicGlyph_Summon` | Number | {'type': '`Number`', 'df': "Applies or references the 'DemonicGlyph_Summon' effect/state."} | 1 |

</details>


---

### `BrittleDuringElement`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BrittleDuringElement` | Enum | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChargeSpiritBombAura`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChargeSpiritBombAura` | Enum | Examples: `DonateEnergy2, DonateEnergy` | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageDistanceAOEFalloff`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DamageDistanceAOEFalloff` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplayDangerAOE`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisplayDangerAOE` | Enum | Examples: `TheChild_Wrath, MoonHead_Blow, attack` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoDistortionRing`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number | {'type': '`Number`', 'df': ''} | 6 |
| `radius` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 6 |
| `speed` | Number | {'type': '`Number`', 'df': ''} | 6 |

</details>


---

### `FragileDuringElement`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FragileDuringElement` | Enum | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalFlowerTrapperAura`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Tangled`](./Arrays.md#array-tangled) | Array | Examples: `[ 1 .1 ]` | 1 |

</details>


---

### `GlobalHealthRegenAura`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalHealthRegenAura` | Number | Examples: `3` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalManaBurnAura`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalManaBurnAura` | Number | Examples: `-1` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalManaDrainAura`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalManaDrainAura` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `OrthogonalAIDangerZone`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OrthogonalAIDangerZone` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBasicAttackBonusAOE`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempBasicAttackBonusAOE` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Movement & Positioning (79)

### `AbilityEnabledIfMovementTrapped`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledIfMovementTrapped` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddExtraTurnsBeforeRun`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddExtraTurnsBeforeRun` | Number | Examples: `2` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddMeleeKnockback`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddMeleeKnockback` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusKnockbackDamage`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BonusKnockbackDamage` | Number | Applies or references the  | 7 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BypassRockKnockback`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BypassRockKnockback` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChanceToForceEvent`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| [`event`](./Enums.md#enum-event) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `CharmedFacingForceAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CharmedFacingForceAttack` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DashFury`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DashFury` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyph_Movement`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Movement` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisableTrample`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisableTrample` | Number | Applies or references the  | 20 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Displace`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Displace` | Number | Applies or references the  | 24 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplaceToAbilityTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisplaceToAbilityTarget` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplaceToOriginalPosition`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisplaceToOriginalPosition` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplaceTowardsSource`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FastKnockback`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FastKnockback` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlingObjectsOnTop`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FlingObjectsOnTop` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceDisplace`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceDisplace` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceImmediateMove`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceImmediateMove` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceImmediateMoveAndAttack`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ability to execute after moving.'} | 1 |
| `even_if_cant_reach` | Boolean | {'type': '`Boolean`', 'df': 'If true, executes the attack even if the move fails to reach the target.'} | 1 |

</details>


---

### `ForceMoveAndAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveAndAttack` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceMoveNonAlliesInRangeTowardsTile`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveNonAlliesInRangeTowardsTile` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceMoveTowards`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Number | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceMoveTowardsEnemies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveTowardsEnemies` | Mixed | Examples: `DumbMove_Impl, 1, MoveOne` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceMoveTowardsTaggedObject`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The movement ability to use.'} | 2 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'The entity tag to seek out.'} | 1 |

</details>


---

### `ForceTransferWeapon`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceTransferWeapon` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceUseAbilityOnTarget`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 1 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |

</details>


---

### `InterchangeMoveActPoints`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `InterchangeMoveActPoints` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JustInCaseTrample`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `JustInCaseTrample` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KnockbackDirectionIsFacingDirection`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `KnockbackDirectionIsFacingDirection` | Mixed | Examples: `rotate_right, flip, 1` | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KnockbackIfCrit`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `override_chain_knockback` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `LeaveBehindOnceEachMove`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LeaveBehindOnceEachMove` | Enum | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LowGravityKnockbackBoost`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LowGravityKnockbackBoost` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MinimumKnockbackFromAllDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MinimumKnockbackFromAllDamage` | Number | Applies or references the  | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MinimumKnockbackFromPhysicalAttacks`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MinimumKnockbackFromPhysicalAttacks` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MotherTumorDebugForcePass`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MotherTumorDebugForcePass` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MoveAfterAnyAttemptedAttack`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `MoveAwayWhenEnemyAdjacent`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `once_per_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`weights`](./Enums.md#enum-weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `MoveTowardsKillers`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`character_filter`](./Arrays.md#array-character_filter) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>


---

### `OverrideKnockbackDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 34

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `OverrideKnockbackDamage` | Mixed | Applies or references the  | 34 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomKnockback`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | {'type': '`Number`', 'df': 'Maximum knockback distance.'} | 2 |
| `min` | Number | {'type': '`Number`', 'df': 'Minimum knockback distance.'} | 2 |

</details>


---

### `RandomKnockbackDirection`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomKnockbackDirection` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RefreshMovePointsIfHit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RefreshMovePointsIfHit` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveActPoints`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoveActPoints` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveAmbientLightEffects`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoveAmbientLightEffects` | Enum | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveExtraDispersedTurn`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoveExtraDispersedTurn` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveGlobalModifiers`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoveGlobalModifiers` | Array | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveItem`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoveItem` | Enum | Examples: `BlackShard, BlackShard_Glowing` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveKnockback`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoveKnockback` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveMovePoints`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoveMovePoints` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveStatus`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoveStatus` | Enum | Examples: `DodgeChance_Status, SpeedUp_WithoutInitiative` | 32 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveStatusStacks`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'The number of stacks to remove.'} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'The specific status effect ID to remove.'} | 1 |

</details>


---

### `RemoveTurnsThisRound`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RemoveTurnsThisRound` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReplaceBasicMove_Mutation`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReplaceBasicMove_Mutation` | Enum | Examples: `BasicJump, BasicDig` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RunInXTurns`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RunInXTurns` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RunWhenKittensDead`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RunWhenKittensDead` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RunWhenLastPlayerCatIsCharmed`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `SetDistanceDisplace`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetDistanceDisplace` | Number | Applies or references the  | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetKnockback`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetKnockback` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpeculativeMoveSelfCorpseOffMap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SproutsGrantMovement`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SproutsGrantMovement` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatusIfDidntMove`
> Found in: *Cat Mutations, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Charge` | Number | Examples: `3` | 1 |

</details>


---

### `StatusWhenStatusCompletelyRemoved`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`UseAbility`](./Characters_and_Bosses.md#context-useability) | Block | {'type': '`Block`', 'df': "Logic: Forces execution of an ability. | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>


---

### `StripKnockback`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StripKnockback` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SupportDieInsteadOfRun`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `TVBotDisableMove`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TVBotDisableMove` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBonusKnockback`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempBonusKnockback` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBonusKnockbackDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempBonusKnockbackDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempTrampleUntilSettled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempTrampleUntilSettled` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Terminator2Chase`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Terminator2Chase` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Terminator2Run`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `TerminatorChase`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`move`](./Enums.md#enum-move) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `TilesMovedToCritChance`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TilesMovedToCritChance` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TilesMovedToMana`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TilesMovedToMana` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TilesMovedToNeighborHeal`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TilesMovedToNeighborHeal` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TilesMovedToStrength`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TilesMovedToStrength` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TwisterDisplaceWithDamage`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Mixed | {'type': '`Number`', 'df': 'The damage formula or inherit flag.'} | 6 |
| `max_dist` | Number | {'type': '`Number`', 'df': 'Maximum displacement distance.'} | 6 |
| `min_dist` | Number | {'type': '`Number`', 'df': 'Minimum displacement distance.'} | 2 |
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `TwisterFling`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | {'type': '`Number`', 'df': 'The base damage properties of an attack.'} | 1 |
| `max_dist` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `min_dist` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `UseMoveAbilityWithAI`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 1 |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | {'type': '`Enum/String`', 'df': 'The AI positioning logic profile to use.'} | 1 |

</details>


---

### `ZeroKnockbackDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ZeroKnockbackDamage` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Spawns, Summons & Familiars (50)

### `AbilityWhenBuddyDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityWhenBuddyDies` | Enum | Examples: `GirlDinoCry, ChubsRage, Guillotina2Rage` | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsBuddy`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AggroTargetIsBuddy` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyPassivesToSpawnerWhileAlive`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'HideEquipment' effect/state."} | 1 |

</details>


---

### `Buddy`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`obj`](./Enums.md#enum-obj) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `reclaim_if_lost` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `DemonicGlyph_Summon`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Summon` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DieWhenSpawnerDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DieWhenSpawnerDies` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplayBuddyCatOnSpawn`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisplayBuddyCatOnSpawn` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DropAsFamiliarOnArmorBreak`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DropAsFamiliarOnArmorBreak` | Enum | Examples: `HeadGrubFamiliar, FaceGrubFamiliar, NeckGrubFamiliar` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DropAsFamiliarOnTookDamage`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DropAsFamiliarOnTookDamage` | Enum | Examples: `PhantomMaskRock` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EraseSpawnCoins`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EraseSpawnCoins` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExpireOnSpawnerTurnEnd`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExpireOnSpawnerTurnEnd` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalFamiliarDamageBoost`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalFamiliarDamageBoost` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalFamiliarMoveBoost`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalFamiliarMoveBoost` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalSpawnCharacter`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalSpawnCharacter` | Enum | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalSpawnOnRoundEnd`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `NeutralZombieKitten, NeutralTwister` | 2 |
| [`number`](./Arrays.md#array-number) | Array | Examples: `[ 1 2 ]` | 1 |

</details>


---

### `InheritSpawnerStats`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `InheritSpawnerStats` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LegacySpawnSavedCatIfExists`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LegacySpawnSavedCatIfExists` | Enum | Examples: `Legacy_Marshmallow_StolenCatID` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MimicSpawnerAttacks`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MimicSpawnerAttacks` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MotherTumorSpawnInCapture`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#context-cat) | Block | {'type': '`Block`', 'df': 'Character Form: Base form for standard cats. | 2 |
| [`NonCat`](./Characters_and_Bosses.md#context-noncat) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NonCat' state. | 2 |
| [`Nothing`](./Characters_and_Bosses.md#context-nothing) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Nothing' state. | 1 |

</details>


---

### `MultiSpawnOnDeath`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | {'type': '`Array`', 'df': 'The numerical quantity.'} | 1 |
| [`obj`](./Enums.md#enum-obj) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `PopAndSpawn`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID to spawn in place.'} | 2 |
| `clone_items` | Boolean | {'type': '`Boolean`', 'df': 'If true, transfers inventory to the new entity.'} | 1 |
| `clone_referenced_catdata` | Boolean | {'type': '`Boolean`', 'df': 'If true, copies the genetic data of the popped cat.'} | 1 |
| `no_splatter` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `SharePickupsWithSpawner`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SharePickupsWithSpawner` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnBearTrap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnBearTrap` | Number | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnBearTrapIfHitKills`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnCatCloneOnCorpsePopped`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnCatCloneOnCorpsePopped` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnCatCopyWhenDowned`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `PlayerCat_AncestralShade, PlayerCat_NecroShade` | 2 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum | Examples: `necroset_shade, ancestorset_shade` | 2 |

</details>


---

### `SpawnCreep`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnCreep` | Number | Applies or references the  | 18 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnCreepOnHitKnockback`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnCreepOnHitKnockback` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnCustomTrap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnCustomTrap` | Enum | Examples: `SpikeTrap, EggSackTrap, CharmTrap` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnExtraThingsOnBattleStart`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array | Examples: `[ 1 2 ]` | 1 |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `RandomPickup` | 1 |

</details>


---

### `SpawnFlames`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnFlames` | Array | Examples: `[ 1 .20 ], [ 1 .20+.1*level ]` | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnItemLinkedFamiliar`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>


---

### `SpawnNearEnemies`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnNearEnemies` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnNeutralWebTrapOnMiss`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnNeutralWebTrapOnMiss` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnOnDeath`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 79

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`obj`](./Arrays.md#array-obj) | Array | {'type': '`Array`', 'df': ''} | 3 |
| [`additional_statuses`](./Characters_and_Bosses.md#context-additional_statuses) | Block | {'type': '`Block`', 'df': "Generic statuses added to the character. | 1 |

</details>


---

### `SpawnOnDowned`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnOnDowned` | Enum | Examples: `CharmedKitten, CharmedFly` | 16 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnRandomPickupsOnTaggedUnitKilled`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array | {'type': '`Array`', 'df': 'Quantity.'} | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 1 |

</details>


---

### `SpawnRock`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnRock` | Array | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnThingIfHitKills`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnThingIfHitKills` | Enum | Examples: `Food, BiggestFood, BigFood` | 20 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnTilePuddleOnBattleStart`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max_radius` | Number | Examples: `3.5` | 1 |
| `min_radius` | Number | Examples: `1.5` | 1 |
| [`tile`](./Enums.md#enum-tile) | Enum | Examples: `OilTile` | 1 |

</details>


---

### `SpawnVolcanoOnBattleStart`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `MiniVolcano, Sprout, PunchingBag` | 3 |
| `max_radius` | Number | Examples: `2.2` | 2 |
| `min_radius` | Mixed | Examples: `1, .2` | 2 |
| [`puddle_tile`](./Arrays.md#array-puddle_tile) | Array | Examples: `[ BrambleTile TallBrambleTile ], LavaTile` | 2 |
| [`number`](./Arrays.md#array-number) | Array | Examples: `[ 3 5 ]` | 1 |

</details>


---

### `SpawnWebTrap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnWebTrap` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnerCatDataReference`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpawnerCatDataReference` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatusAllCharactersOnSpawn`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Boss`](./Items_and_Equipment.md#context-conditional_boss) | Block | {'type': '`Block`', 'df': "Conditional trigger: Executes nested logic if the target is a Boss. | 2 |
| `Poison` | Number | {'type': '`Number`', 'df': "Applies or references the 'Poison' effect/state."} | 1 |

</details>


---

### `StatusOnSpawnIn`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Number | {'type': '`Number`', 'df': "Applies or references the 'CaptureFamiliar' effect/state."} | 1 |
| `SetHealth` | Number | {'type': '`Number`', 'df': "Applies or references the 'SetHealth' effect/state."} | 1 |

</details>


---

### `SyncFormsWithBuddy`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `T3HitlerSpawningPhase`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>


---

### `T3HitlerTriggerInitialSpawns`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `T3HitlerTriggerInitialSpawns` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TakeWeaponFromSpawner`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TakeWeaponFromSpawner` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TossTargetIsBuddy`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TossTargetIsBuddy` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Loot, Rewards & Economy (34)

### `AddLootMultiplier`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddLootMultiplier` | Number | Examples: `1` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ArmorPickup`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | {'type': '`Array`', 'df': ''} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 3 |

</details>


---

### `AwardCoinsOnDeath`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AwardCoinsOnDeath` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BirdRewards`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_rewards`](./Characters_and_Bosses.md#context-ally_rewards) | Block | {'type': '`Block`', 'df': 'Loot logic triggered if an ally dies. | 18 |
| [`statuses`](./Characters_and_Bosses.md#context-statuses) | Block | {'type': '`Block`', 'df': "Status effects possessed by the character. | 5 |

</details>


---

### `ChaosHeadDropIn`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`new_music`](./Enums.md#enum-new_music) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 1 |

</details>


---

### `CoinPickup`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CoinPickup` | Number | Applies or references the  | 20 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CoinTossBounce`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CoinTossBounce` | Equation | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CollectsPickups`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 34

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CollectsPickups` | Number | Applies or references the  | 34 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CollectsPickupsWithAltEffects`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Tech` | Number | {'type': '`Number`', 'df': "Applies or references the 'Tech' effect/state."} | 2 |
| `CurrentWeaponAddPoison` | Number | {'type': '`Number`', 'df': "Applies or references the 'CurrentWeaponAddPoison' effect/state."} | 1 |
| `LuckUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'LuckUp' effect/state."} | 1 |
| `Quivered` | Number | {'type': '`Number`', 'df': "Applies or references the 'Quivered' effect/state."} | 1 |
| `RandomStatUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'RandomStatUp' effect/state."} | 1 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 1 |

</details>


---

### `DemonicGlyphStealer`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyphStealer` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleLoot`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleLoot` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DropSoulJarOnDeath`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DropSoulJarOnDeath` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FindItem`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FindItem` | Enum | Applies or references the  | 5 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceCollectsPickups`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceCollectsPickups` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainCoins`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GainCoins` | Number | Applies or references the  | 20 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainCoinsRange`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `max` | Number | {'type': '`Number`', 'df': 'Maximum coins granted.'} | 4 |
| `min` | Number | {'type': '`Number`', 'df': 'Minimum coins granted.'} | 4 |

</details>


---

### `HealthPickup`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | {'type': '`Array`', 'df': ''} | 15 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 15 |
| `stored_food_value` | Number | {'type': '`Number`', 'df': ''} | 15 |
| `anything_eats` | Boolean | {'type': '`Boolean`', 'df': ''} | 4 |
| `force_frame` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `Lifesteal`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Lifesteal` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManaPickup`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | {'type': '`Array`', 'df': ''} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 3 |

</details>


---

### `ManaSteal`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaSteal` | Number | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManaStealToHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManaStealToHealth` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MegaDinoDropController`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`leg_return`](./Enums.md#enum-leg_return) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `stable_legs` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `ModularPickup`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Cleanse` | Number | {'type': '`Number`', 'df': "Applies or references the 'Cleanse' effect/state."} | 1 |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `MultiplyCoinsOnBattleStart`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MultiplyCoinsOnBattleStart` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnGainCoins`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnGainCoins` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScatterCoins`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stackable` | Boolean | {'type': '`Boolean`', 'df': 'If true, multiple instances of this trigger can stack.'} | 2 |
| [`stacks`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': 'Number of stacks or intensity to apply.'} | 2 |

</details>


---

### `ScatterHeldCoin`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ScatterHeldCoin` | Array | Examples: `1, [ 1 .3 ], [ 1 .5 ]` | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScatterRandomPickups`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ScatterRandomPickups` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealDemonicGlyph`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StealDemonicGlyph` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealEquipment`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StealEquipment` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StealTurn` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealthCritChance`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StealthCritChance` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealthUntilBasicAttack`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StealthUntilBasicAttack` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WhitelistPickupType`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `WhitelistPickupType` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Form Changes & Transformations (34)

### `CatPartsTransform`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ear1` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the front ear.'} | 10 |
| `tail` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the tail.'} | 10 |
| `ear2` | Number | {'type': '`Number`', 'df': ''} | 9 |
| `arm2` | Number | {'type': '`Number`', 'df': ''} | 8 |
| `mouth` | Number | {'type': '`Number`', 'df': ''} | 8 |
| `arm1` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the front arm.'} | 7 |
| `leg1` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the front leg.'} | 5 |
| `leg2` | Number | {'type': '`Number`', 'df': ''} | 5 |
| `head` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the head.'} | 3 |
| `texture` | Number | {'type': '`Number`', 'df': ''} | 3 |
| `body` | Number | {'type': '`Number`', 'df': 'Sprite variant ID for the body.'} | 2 |
| `eye1` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `eye2` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `eyebrow1` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `eyebrow2` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `palette` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `ChanceToFormChangeOnAbilityDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0) of executing this action.'} | 1 |
| [`form`](./Enums.md#enum-form) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `ChaosBossFormChange`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChaosBossFormChange` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChaosBossFormChangeGuide`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `passives_health_threshold` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `DurabilityTransform`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array | {'type': '`Array`', 'df': ''} | 11 |
| [`ge`](./Arrays.md#array-ge) | Array | {'type': '`Array`', 'df': ''} | 4 |

</details>


---

### `FormChange`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `form` | Mixed | {'type': '`String`', 'df': ''} | 75 |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |

</details>


---

### `FormChangeDuringWeatherElement`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 2 |
| [`form`](./Enums.md#enum-form) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>


---

### `FormChangeHealthThreshold`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| [`form_below`](./Enums.md#enum-form_below) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `threshold` | Mixed | {'type': '`Number`', 'df': ''} | 3 |
| `count_shield` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `FormChangeOffMap`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum | {'type': '`Enum/String`', 'df': ''} | 8 |
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum | {'type': '`Enum/String`', 'df': ''} | 8 |

</details>


---

### `FormChangeOnElementInfluence`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 9 |
| [`form`](./Enums.md#enum-form) | Enum | {'type': '`Enum/String`', 'df': ''} | 9 |
| [`exclude`](./Enums.md#enum-exclude) | Enum | {'type': '`Enum/String`', 'df': ''} | 5 |
| [`particle`](./Enums.md#enum-particle) | Enum | {'type': '`Enum/String`', 'df': ''} | 5 |
| [`sfx`](./Enums.md#enum-sfx) | Enum | {'type': '`Enum/String`', 'df': ''} | 5 |

</details>


---

### `FormChangeWhenBuddyDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FormChangeWhenBuddyDies` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FormChangeWhileHasStatus`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 35 |
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum | {'type': '`Enum/String`', 'df': ''} | 30 |
| [`form_has`](./Enums.md#enum-form_has) | Enum | {'type': '`Enum/String`', 'df': ''} | 25 |

</details>


---

### `FormChangeWhilePrimingAbility`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |
| [`priming`](./Enums.md#enum-priming) | Enum | {'type': '`Enum/String`', 'df': ''} | 6 |

</details>


---

### `FormChanger`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 106

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum | {'type': '`Enum/String`', 'df': ''} | 56 |
| [`Default`](./Characters_and_Bosses.md#context-default) | Block | {'type': '`Block`', 'df': 'Character Form: The baseline default behavior state. | 37 |
| [`Normal`](./Characters_and_Bosses.md#context-normal) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Normal\' state. | 11 |
| [`Rage`](./Characters_and_Bosses.md#context-rage) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Rage\' state. | 10 |
| [`HasCat`](./Characters_and_Bosses.md#context-hascat) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HasCat\' state. | 5 |
| [`OffMap`](./Characters_and_Bosses.md#context-offmap) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'OffMap' state. | 4 |
| [`default`](./Characters_and_Bosses.md#context-default) | Block | {'type': '`Block`', 'df': 'Baseline configuration. | 4 |
| [`hot`](./Characters_and_Bosses.md#context-hot) | Block | {'type': '`Block`', 'df': 'Visual effect indicator. | 4 |
| [`AllAlive`](./Characters_and_Bosses.md#context-allalive) | Block | {'type': '`Block`', 'df': 'Encounter State: Logic executed when all specific entities are currently alive. | 3 |
| [`Down`](./Characters_and_Bosses.md#context-down) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Down\' state. | 3 |
| [`Full`](./Characters_and_Bosses.md#context-full) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Full\' state. | 3 |
| [`OneAlive`](./Characters_and_Bosses.md#context-onealive) | Block | {'type': '`Block`', 'df': 'Encounter State: Logic executed when exactly one target is alive. | 3 |
| [`TwoAlive`](./Characters_and_Bosses.md#context-twoalive) | Block | {'type': '`Block`', 'df': 'Encounter State: Logic executed when exactly two targets are alive. | 3 |
| [`Up`](./Characters_and_Bosses.md#context-up) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Up\' state. | 3 |
| [`Big`](./Characters_and_Bosses.md#context-big) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'Big\' state. | 2 |
| [`Boris`](./Characters_and_Bosses.md#context-boris) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'Boris\' state. | 2 |
| [`CaveMan`](./Characters_and_Bosses.md#context-caveman) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveMan\' state. | 2 |
| [`CaveManSpear`](./Characters_and_Bosses.md#context-cavemanspear) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveManSpear\' state. | 2 |
| [`Empty`](./Characters_and_Bosses.md#context-empty) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Empty\' state. | 2 |
| [`Explosive`](./Characters_and_Bosses.md#context-explosive) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Explosive\' state. | 2 |
| [`Holding`](./Characters_and_Bosses.md#context-holding) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Holding\' state. | 2 |
| [`Holy`](./Characters_and_Bosses.md#context-holy) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Holy\' state. | 2 |
| [`NotPriming`](./Characters_and_Bosses.md#context-notpriming) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats when not charging an ability. | 2 |
| [`Priming`](./Characters_and_Bosses.md#context-priming) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats when charging an ability. | 2 |
| [`Rain`](./Characters_and_Bosses.md#context-rain) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Rain' state. | 2 |
| [`Small`](./Characters_and_Bosses.md#context-small) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Small\' state. | 2 |
| [`SquirrelForm`](./Characters_and_Bosses.md#context-squirrelform) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'SquirrelForm' state. | 2 |
| [`Turtled`](./Characters_and_Bosses.md#context-turtled) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Turtled' state. | 2 |
| [`active`](./Characters_and_Bosses.md#context-active) | Block | {'type': '`Block`', 'df': 'Defines actively executed abilities. | 2 |
| [`ai`](./Characters_and_Bosses.md#context-ai) | Block | {'type': 'Block', 'df': 'Core block defining the AI behavior logic and weights.'} | 2 |
| [`attack`](./Enums.md#enum-attack) | Enum | {'type': 'Enum/String', 'df': ''} | 2 |
| `partial_animation_suffix` | Number | {'type': 'String', 'df': ''} | 2 |
| [`passive`](./Characters_and_Bosses.md#context-passive) | Block | {'type': '`Block`', 'df': 'Intrinsic passive modifier. | 2 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | {'type': 'Block', 'df': 'Block listing intrinsic passive modifiers.'} | 2 |
| [`Alert`](./Characters_and_Bosses.md#context-alert) | Block | {'type': '`Block`', 'df': 'AI State: The behavior profile used when the character is alerted to enemies. | 1 |
| [`Angry`](./Characters_and_Bosses.md#context-angry) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'Angry\' state. | 1 |
| [`Attacker`](./Characters_and_Bosses.md#context-attacker) | Block | {'type': '`Block`', 'df': 'AI Role: Designates the character as an attacker rather than support. | 1 |
| [`BellyFull`](./Characters_and_Bosses.md#context-bellyfull) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'BellyFull\' state. | 1 |
| [`BigHolding`](./Characters_and_Bosses.md#context-bigholding) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'BigHolding\' state. | 1 |
| [`BigHoldingCat`](./Characters_and_Bosses.md#context-bigholdingcat) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'BigHoldingCat\' state. | 1 |
| [`Bishop`](./Characters_and_Bosses.md#context-bishop) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'Bishop\' state. | 1 |
| [`BlackHole`](./Characters_and_Bosses.md#context-blackhole) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior and stats for the \'BlackHole\' state. | 1 |
| [`Bomb`](./Characters_and_Bosses.md#context-bomb) | Block | {'type': '`Block`', 'df': "Character Form / AI State: Behavior and stats for the 'Bomb' state. | 1 |
| [`Bully`](./Characters_and_Bosses.md#context-bully) | Block | {'type': '`Block`', 'df': "Character Form / AI State: Behavior and stats for the 'Bully' state. | 1 |
| `Butcher` | Block | {'type': '`Block`', 'df': "Applies or references the 'Butcher' effect/state."} | 1 |
| [`CaveBaby`](./Characters_and_Bosses.md#context-cavebaby) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveBaby\' state. | 1 |
| [`CaveWoman`](./Characters_and_Bosses.md#context-cavewoman) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveWoman\' state. | 1 |
| [`CaveWomanHasCat`](./Characters_and_Bosses.md#context-cavewomanhascat) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'CaveWomanHasCat\' state. | 1 |
| [`Charging`](./Characters_and_Bosses.md#context-charging) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior when charging an attack. | 1 |
| [`Close`](./Characters_and_Bosses.md#context-close) | Block | {'type': '`Block`', 'df': 'AI Movement logic: Maneuvers into close/melee range. | 1 |
| `Colorless` | Block | {'type': '`Block`', 'df': "Applies or references the 'Colorless' effect/state."} | 1 |
| [`Cultist`](./Characters_and_Bosses.md#context-cultist) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Cultist\' state. | 1 |
| [`Damaged`](./Characters_and_Bosses.md#context-damaged) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior when health is critically low. | 1 |
| [`Default_Ceiling`](./Characters_and_Bosses.md#context-default_ceiling) | Block | {'type': '`Block`', 'df': 'Character Form: The baseline behavior state while attached to the ceiling. | 1 |
| [`Default_Ground`](./Characters_and_Bosses.md#context-default_ground) | Block | {'type': '`Block`', 'df': 'Character Form: The baseline behavior state while on the ground. | 1 |
| [`DesireMech`](./Characters_and_Bosses.md#context-desiremech) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'DesireMech' state. | 1 |
| [`Die`](./Characters_and_Bosses.md#context-die) | Block | {'type': '`Block`', 'df': 'Character Form / Logic: Forces the character to die. | 1 |
| `Druid` | Block | {'type': '`Block`', 'df': "Applies or references the 'Druid' effect/state."} | 1 |
| [`Drunker`](./Characters_and_Bosses.md#context-drunker) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Drunker' state. | 1 |
| [`DualSword`](./Characters_and_Bosses.md#context-dualsword) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'DualSword\' state. | 1 |
| [`DualSword_Primed`](./Characters_and_Bosses.md#context-dualsword_primed) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'DualSword_Primed\' state. | 1 |
| [`Dumb`](./Characters_and_Bosses.md#context-dumb) | Block | {'type': '`Block`', 'df': 'AI Profile: A simplified, less optimal decision-making profile. | 1 |
| [`Explody`](./Characters_and_Bosses.md#context-explody) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Explody' state. | 1 |
| [`FightPhase`](./Characters_and_Bosses.md#context-fightphase) | Block | {'type': '`Block`', 'df': 'Boss Logic: Main combat phase. | 1 |
| `Fighter` | Block | {'type': '`Block`', 'df': "Applies or references the 'Fighter' effect/state."} | 1 |
| [`Fire`](./Characters_and_Bosses.md#context-fire) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Fire' state. | 1 |
| [`FireFull`](./Characters_and_Bosses.md#context-firefull) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'FireFull' state. | 1 |
| [`Flop`](./Characters_and_Bosses.md#context-flop) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Flop\' state. | 1 |
| [`Flop2`](./Characters_and_Bosses.md#context-flop2) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Flop2\' state. | 1 |
| [`Flush`](./Characters_and_Bosses.md#context-flush) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Flush' state. | 1 |
| [`FlushBubs`](./Characters_and_Bosses.md#context-flushbubs) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'FlushBubs' state. | 1 |
| [`FlushHost`](./Characters_and_Bosses.md#context-flushhost) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'FlushHost' state. | 1 |
| [`FlushNettle`](./Characters_and_Bosses.md#context-flushnettle) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'FlushNettle' state. | 1 |
| [`Grappling`](./Characters_and_Bosses.md#context-grappling) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Behavior while grappling an opponent. | 1 |
| [`Grown`](./Characters_and_Bosses.md#context-grown) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Grown\' state. | 1 |
| [`GuaranteedJackpot`](./Characters_and_Bosses.md#context-guaranteedjackpot) | Block | {'type': '`Block`', 'df': 'Loot Logic: Guarantees a high-tier drop. | 1 |
| [`Guarding`](./Characters_and_Bosses.md#context-guarding) | Block | {'type': '`Block`', 'df': 'Character Form / AI State: Defensive behavior state. | 1 |
| [`HalfDead`](./Characters_and_Bosses.md#context-halfdead) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HalfDead\' state. | 1 |
| [`HasDeadCat`](./Characters_and_Bosses.md#context-hasdeadcat) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HasDeadCat\' state. | 1 |
| [`HasRock`](./Characters_and_Bosses.md#context-hasrock) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HasRock\' state. | 1 |
| [`Headless`](./Characters_and_Bosses.md#context-headless) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Headless\' state. | 1 |
| [`Hint_CrackedVisuals`](./Characters_and_Bosses.md#context-hint_crackedvisuals) | Block | {'type': '`Block`', 'df': 'Visual: Overlay effects for cracked/damaged terrain or objects. | 1 |
| [`Hint_CrackedVisuals2`](./Characters_and_Bosses.md#context-hint_crackedvisuals2) | Block | {'type': '`Block`', 'df': 'Visual: Secondary cracked visual overlay. | 1 |
| [`Hint_CrackedVisuals3`](./Characters_and_Bosses.md#context-hint_crackedvisuals3) | Block | {'type': '`Block`', 'df': 'Visual: Tertiary cracked visual overlay. | 1 |
| [`HumanDead`](./Characters_and_Bosses.md#context-humandead) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'HumanDead\' state. | 1 |
| `Hunter` | Block | {'type': '`Block`', 'df': "Applies or references the 'Hunter' effect/state."} | 1 |
| [`InitialPhase`](./Characters_and_Bosses.md#context-initialphase) | Block | {'type': '`Block`', 'df': 'Boss Logic: The starting phase of an encounter. | 1 |
| [`Insane_Ceiling`](./Characters_and_Bosses.md#context-insane_ceiling) | Block | {'type': '`Block`', 'df': 'Character Form: Insane behavior state while attached to the ceiling. | 1 |
| [`Insane_Ground`](./Characters_and_Bosses.md#context-insane_ground) | Block | {'type': '`Block`', 'df': 'Character Form: Insane behavior state while on the ground. | 1 |
| [`Johnny`](./Characters_and_Bosses.md#context-johnny) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Johnny' state. | 1 |
| [`JohnnyBubs`](./Characters_and_Bosses.md#context-johnnybubs) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'JohnnyBubs' state. | 1 |
| [`JohnnyHost`](./Characters_and_Bosses.md#context-johnnyhost) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'JohnnyHost' state. | 1 |
| [`JohnnyNettle`](./Characters_and_Bosses.md#context-johnnynettle) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'JohnnyNettle' state. | 1 |
| [`Joystick`](./Characters_and_Bosses.md#context-joystick) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Joystick\' state. | 1 |
| [`LastHit`](./Characters_and_Bosses.md#context-lasthit) | Block | {'type': '`Block`', 'df': 'Logic: Executes logic on the final hit of a multi-hit attack. | 1 |
| [`Lifted`](./Characters_and_Bosses.md#context-lifted) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Lifted\' state. | 1 |
| [`Lit`](./Characters_and_Bosses.md#context-lit) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Lit' state. | 1 |
| `Mage` | Block | {'type': '`Block`', 'df': "Applies or references the 'Mage' effect/state."} | 1 |
| `Medic` | Block | {'type': '`Block`', 'df': "Applies or references the 'Medic' effect/state."} | 1 |
| `Monk` | Block | {'type': '`Block`', 'df': "Applies or references the 'Monk' effect/state."} | 1 |
| [`Mounted`](./Characters_and_Bosses.md#context-mounted) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Mounted\' state. | 1 |
| [`MouthFull`](./Characters_and_Bosses.md#context-mouthfull) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'MouthFull\' state. | 1 |
| [`Mutant`](./Characters_and_Bosses.md#context-mutant) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Mutant\' state. | 1 |
| `Necromancer` | Block | {'type': '`Block`', 'df': "Applies or references the 'Necromancer' effect/state."} | 1 |
| [`NeutronStar`](./Characters_and_Bosses.md#context-neutronstar) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NeutronStar' state. | 1 |
| `NoDeathRattle` | Block | {'type': '`Block`', 'df': "Applies or references the 'NoDeathRattle' effect/state."} | 1 |
| [`NoEyes`](./Characters_and_Bosses.md#context-noeyes) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'NoEyes\' state. | 1 |
| [`NoStick`](./Characters_and_Bosses.md#context-nostick) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NoStick' state. | 1 |
| [`NormalFull`](./Characters_and_Bosses.md#context-normalfull) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NormalFull' state. | 1 |
| [`Nuke`](./Characters_and_Bosses.md#context-nuke) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Nuke' state. | 1 |
| [`Obey`](./Characters_and_Bosses.md#context-obey) | Block | {'type': '`Block`', 'df': 'AI State: Enforced compliance logic (e.g., when Charmed). | 1 |
| [`Off`](./Characters_and_Bosses.md#context-off) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Off' state. | 1 |
| [`OffScreen`](./Characters_and_Bosses.md#context-offscreen) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'OffScreen' state. | 1 |
| [`OneEye`](./Characters_and_Bosses.md#context-oneeye) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'OneEye\' state. | 1 |
| [`Open`](./Characters_and_Bosses.md#context-open) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Open' state. | 1 |
| [`OpenCat`](./Characters_and_Bosses.md#context-opencat) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'OpenCat' state. | 1 |
| [`Out`](./Characters_and_Bosses.md#context-out) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Out' state. | 1 |
| [`Possessing`](./Characters_and_Bosses.md#context-possessing) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Possessing\' state. | 1 |
| [`Primed`](./Characters_and_Bosses.md#context-primed) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Primed' state. | 1 |
| `Psychic` | Block | {'type': '`Block`', 'df': "Applies or references the 'Psychic' effect/state."} | 1 |
| [`Pulp2`](./Characters_and_Bosses.md#context-pulp2) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp2' state. | 1 |
| [`Pulp3`](./Characters_and_Bosses.md#context-pulp3) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp3' state. | 1 |
| [`Pulp4`](./Characters_and_Bosses.md#context-pulp4) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp4' state. | 1 |
| [`Pulp5`](./Characters_and_Bosses.md#context-pulp5) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp5' state. | 1 |
| [`Pulp6`](./Characters_and_Bosses.md#context-pulp6) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp6' state. | 1 |
| [`Pulp7`](./Characters_and_Bosses.md#context-pulp7) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Pulp7' state. | 1 |
| [`Sitting`](./Characters_and_Bosses.md#context-sitting) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Sitting' state. | 1 |
| [`SmallHolding`](./Characters_and_Bosses.md#context-smallholding) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'SmallHolding\' state. | 1 |
| [`SmallHoldingCat`](./Characters_and_Bosses.md#context-smallholdingcat) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'SmallHoldingCat\' state. | 1 |
| [`SpawningPhase`](./Characters_and_Bosses.md#context-spawningphase) | Block | {'type': '`Block`', 'df': 'Boss Logic: Phase focused on summoning minions. | 1 |
| [`Standing`](./Characters_and_Bosses.md#context-standing) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Standing' state. | 1 |
| [`Standing2`](./Characters_and_Bosses.md#context-standing2) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Standing2' state. | 1 |
| [`Start_Ceiling`](./Characters_and_Bosses.md#context-start_ceiling) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Start_Ceiling' state. | 1 |
| [`Stop`](./Characters_and_Bosses.md#context-stop) | Block | {'type': '`Block`', 'df': 'AI Movement: Forces the character to cease movement. | 1 |
| [`SwordAndShield`](./Characters_and_Bosses.md#context-swordandshield) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'SwordAndShield' state. | 1 |
| [`SwordAndShield_Primed`](./Characters_and_Bosses.md#context-swordandshield_primed) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'SwordAndShield_Primed\' state. | 1 |
| `Tank` | Block | {'type': '`Block`', 'df': "Applies or references the 'Tank' effect/state."} | 1 |
| [`Tar`](./Characters_and_Bosses.md#context-tar) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Tar' state. | 1 |
| [`TarFull`](./Characters_and_Bosses.md#context-tarfull) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'TarFull' state. | 1 |
| `Thief` | Block | {'type': '`Block`', 'df': "Applies or references the 'Thief' effect/state."} | 1 |
| [`Throb`](./Characters_and_Bosses.md#context-throb) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Throb' state. | 1 |
| [`ThrobBubs`](./Characters_and_Bosses.md#context-throbbubs) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'ThrobBubs' state. | 1 |
| [`ThrobHost`](./Characters_and_Bosses.md#context-throbhost) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'ThrobHost' state. | 1 |
| [`ThrobNettle`](./Characters_and_Bosses.md#context-throbnettle) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'ThrobNettle' state. | 1 |
| `Tinkerer` | Block | {'type': '`Block`', 'df': "Applies or references the 'Tinkerer' effect/state."} | 1 |
| [`Transformed`](./Characters_and_Bosses.md#context-transformed) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Transformed' state. | 1 |
| [`TwoEyes`](./Characters_and_Bosses.md#context-twoeyes) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'TwoEyes' state. | 1 |
| [`Unlit`](./Characters_and_Bosses.md#context-unlit) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Unlit' state. | 1 |
| `Unmounted` | Block | {'type': '`Block`', 'df': "Applies or references the 'Unmounted' effect/state."} | 1 |
| [`Unwashed`](./Characters_and_Bosses.md#context-unwashed) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Unwashed' state. | 1 |
| [`Washed`](./Characters_and_Bosses.md#context-washed) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'Washed' state. | 1 |
| [`Washer`](./Characters_and_Bosses.md#context-washer) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Washer\' state. | 1 |
| [`Water`](./Characters_and_Bosses.md#context-water) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Water\' state. | 1 |
| [`WereMan`](./Characters_and_Bosses.md#context-wereman) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'WereMan\' state. | 1 |
| [`Zealot`](./Characters_and_Bosses.md#context-zealot) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'Zealot\' state. | 1 |
| [`ZealotBomb`](./Characters_and_Bosses.md#context-zealotbomb) | Block | {'type': '`Block`', 'df': 'Character Form: Behavior and stats for the \'ZealotBomb\' state. | 1 |
| `sync_brain_patterns` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `uifloaters_offset` | Number | {'type': 'Number', 'df': ''} | 1 |

</details>


---

### `ItemAuxTransform`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array | {'type': '`Array`', 'df': ''} | 6 |
| [`ge`](./Arrays.md#array-ge) | Array | {'type': '`Array`', 'df': ''} | 2 |
| [`lt`](./Arrays.md#array-lt) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>


---

### `PreventDeathTransforms`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PreventDeathTransforms` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SupportFormChangeInsteadOfRun`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| `wait_till_turn` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `SwimmingFormChange`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`form_out`](./Enums.md#enum-form_out) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `TransformAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 56

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TransformAbility` | Enum | Examples: `Pounce2, Pounce, MonkeyThrow` | 56 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformBasicAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 28

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TransformBasicAttack` | Enum | Examples: `ThrowPoop, TigerSwipes, TigerSwipes2` | 28 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformBasicMove`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TransformBasicMove` | Enum | Examples: `BasicDashAttackMove_NoKnockback` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformEquipment`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | {'type': '`Enum/String`', 'df': 'The original item ID.'} | 1 |
| [`to`](./Enums.md#enum-to) | Enum | {'type': '`Enum/String`', 'df': 'The new item ID.'} | 1 |

</details>


---

### `TransformInXTurns`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool), [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array | {'type': '`Array`', 'df': ''} | 8 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 8 |
| [`initiative`](./Enums.md#enum-initiative) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`animation`](./Enums.md#enum-animation) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`turns`](./Arrays.md#array-turns) | Array | {'type': '`Array`', 'df': 'Turn counter tracking.'} | 1 |

</details>


---

### `TransformItemOnElementInfluence`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 5 |
| `full_repair` | Boolean | {'type': '`Boolean`', 'df': ''} | 5 |
| [`item`](./Enums.md#enum-item) | Enum | {'type': '`Enum/String`', 'df': 'Item ID to reference.'} | 5 |

</details>


---

### `TransformNow`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TransformNow` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformOnDeath`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 26

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TransformOnDeath` | Enum | Examples: `SimonFlopper, Carcus, RatKing` | 26 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformOnDeathImmediately`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |
| [`obj`](./Enums.md#enum-obj) | Enum | {'type': '`Enum/String`', 'df': ''} | 4 |

</details>


---

### `TransformOnElementInfluence`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 9 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 9 |

</details>


---

### `TransformOnElementInfluencex`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 2 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>


---

### `TransformOnStatusThreshold`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `TransformWeapon`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | {'type': '`Enum/String`', 'df': 'The original weapon ID.'} | 1 |
| [`to`](./Enums.md#enum-to) | Enum | {'type': '`Enum/String`', 'df': 'The transformed weapon ID.'} | 1 |

</details>


---

### `TransformWhenBuddyDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TransformWhenBuddyDies` | Enum | Examples: `UltraOrnstein, UltraSmough` | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerWerewolfTransform`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TriggerWerewolfTransform` | Array | Examples: `[ 1 .15 ], .5, [ 1 .5 ]` | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WeremanTransformationReceiver`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `WeremanTransformationReceiver` | Enum | Examples: `CaveManTransform, CaveWomanDropTransform` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Boss & Special Mechanics (30)

### `AddRandomEliteBuff`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AddRandomEliteBuff` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlphaAllStatsUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlphaAllStatsUp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlphaDodgeChance`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlphaDodgeChance` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlphaStatusOnTurnBegin`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Number | {'type': '`Number`', 'df': "Applies or references the 'DoubleCastSpellThisTurn' effect/state."} | 1 |

</details>


---

### `BossRewards`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum | {'type': '`Enum/String`', 'df': ''} | 20 |
| [`rare`](./Enums.md#enum-rare) | Enum | {'type': '`Enum/String`', 'df': ''} | 16 |

</details>


---

### `ChampionUpgradeNextMinion`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChampionUpgradeNextMinion` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChaosBossFlipMidTeleport`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChaosBossFlipMidTeleport` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChaosBossPieces`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>


---

### `ClearFinalBossBattlefield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ClearFinalBossBattlefield` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EliteFlatTint`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EliteFlatTint` | Array | Examples: `[ 1.1 1.1 1.1 ], [ 1.1 1.1 1.3 ], [ 1.1 1.1 1 ]` | 11 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EliteParticle`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 19

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EliteParticle` | Enum | Examples: `SpikeBuff, Lava_Distortion, SparkleBuff` | 19 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EliteTint`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 30

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EliteTint` | Array | Examples: `[ .4 .4 .4 ], [ .6 .6 .6 .50 ], red` | 30 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EliteUpgradeNextMinion`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EliteUpgradeNextMinion` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_PartyBoss`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExplodeCharacter_PartyBoss` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FinalBossBeamQueue`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`release`](./Enums.md#enum-release) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`transform`](./Enums.md#enum-transform) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `FinalBossBecomeTheChild`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GlobalSpawnCharacter' effect/state."} | 1 |
| `PlayBackground` | Number | {'type': '`Number`', 'df': "Applies or references the 'PlayBackground' effect/state."} | 1 |
| [`SwitchMusic`](./Characters_and_Bosses.md#context-switchmusic) | Block | {'type': '`Block`', 'df': 'Event Trigger: Changes background music track. | 1 |

</details>


---

### `FinalBossHitCountdownBoris`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Characters_and_Bosses.md#context-forceuseability) | Block | {'type': '`Enum/String`', 'df': 'Logic: Forces the execution of a specific ability.'} | 2 |
| `icon` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `icon_ready` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `FinalBossHitCountdownExplosive`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Characters_and_Bosses.md#context-forceuseability) | Block | {'type': '`Enum/String`', 'df': 'Logic: Forces the execution of a specific ability.'} | 2 |
| `icon` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `icon_ready` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `FinalBossHitCountdownHoly`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `icon` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `icon_ready` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `FinalBossPupils`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `radius` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 1 |
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>


---

### `FinalBossQueueBeam`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FinalBossQueueBeam` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FinalBossShield`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FinalBossShield` | Enum | Examples: `None, DestroyerShieldBash` | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FinalBossShieldHealth`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`state_health`](./Arrays.md#array-state_health) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>


---

### `FinalBossSyncAnimations`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`other_form_change_abilities`](./Characters_and_Bosses.md#context-other_form_change_abilities) | Block | {'type': '`Block`', 'df': "Lists secondary abilities used to change forms. | 1 |

</details>


---

### `NukeQuestFinalBossModifications`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`self_damage`](./Abilities_and_Spells.md#context-self_damage) | Block | {'type': '`Block`', 'df': 'Recoil or self-inflicted damage/effects applied to the caster. | 2 |
| [`damage_instance`](./Abilities_and_Spells.md#context-damage_instance) | Block | {'type': '`Block`', 'df': ' | 1 |
| [`splash_damage`](./Abilities_and_Spells.md#context-splash_damage) | Block | {'type': '`Block`', 'df': 'Secondary Area of Effect blast parameters. | 1 |

</details>


---

### `ScaldingOrbMoonBossOneShot`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'CompleteItemQuest' effect/state."} | 1 |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'RemoveItem' effect/state."} | 1 |

</details>


---

### `SignalFinalBossShieldBroke`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SignalFinalBossShieldBroke` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpecialBossMultipartInstakill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpecialBossMultipartInstakill` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TutorialBossRiggedFight`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TutorialBossRiggedFight` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UpgradeTaggedSpawnsToChampions`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `UpgradeTaggedSpawnsToChampions` | Enum | Examples: `worm, bug` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Uncategorized (406)

### `AIControlNextTurn`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `AbilityDisableIfLivingCrow`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityDisableIfLivingCrow` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnableIfConsumedCharacterHasTag`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnableIfConsumedCharacterHasTag` | Enum | Examples: `sp_pill_fire, sp_pill_tar, sp_pill_normal` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfBasicAttackUsedThisTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfNoAggroTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledIfNoAggroTarget` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfSpecificItemEquipped`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledIfSpecificItemEquipped` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledOncePerRound`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledOncePerRound` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledPercentEachTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityEnabledPercentEachTurn` | Number | Applies or references the  | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityInheritsWeaponEffects`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AbilityInheritsWeaponEffects` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AcidRain`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AcidRain` | Number | Examples: `2` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Adrenaline`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Adrenaline` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AdvancedTint`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AdvancedTint` | Array | Examples: `[ .6 .6 .6 1 .5 .5 .5 0 ]` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AdventureTokenPassivePool`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`StacyMutant_Brace`](./Characters_and_Bosses.md#context-stacymutant_brace) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Brace' state. | 1 |
| [`StacyMutant_Counter`](./Characters_and_Bosses.md#context-stacymutant_counter) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Counter' state. | 1 |
| [`StacyMutant_Damage`](./Characters_and_Bosses.md#context-stacymutant_damage) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Damage' state. | 1 |
| [`StacyMutant_DoubleHead`](./Characters_and_Bosses.md#context-stacymutant_doublehead) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state. | 1 |
| [`StacyMutant_Fire`](./Characters_and_Bosses.md#context-stacymutant_fire) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Fire' state. | 1 |
| [`StacyMutant_Health`](./Characters_and_Bosses.md#context-stacymutant_health) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Health' state. | 1 |
| [`StacyMutant_Holy`](./Characters_and_Bosses.md#context-stacymutant_holy) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Holy' state. | 1 |
| [`StacyMutant_Ice`](./Characters_and_Bosses.md#context-stacymutant_ice) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Ice' state. | 1 |
| [`StacyMutant_Lightning`](./Characters_and_Bosses.md#context-stacymutant_lightning) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Lightning' state. | 1 |
| [`StacyMutant_Mirror`](./Characters_and_Bosses.md#context-stacymutant_mirror) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Mirror' state. | 1 |
| [`StacyMutant_Speed`](./Characters_and_Bosses.md#context-stacymutant_speed) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Speed' state. | 1 |
| [`StacyMutant_Thorns`](./Characters_and_Bosses.md#context-stacymutant_thorns) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'StacyMutant_Thorns' state. | 1 |

</details>


---

### `AggroTargetIsCurrentTurn`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AggroTargetIsCurrentTurn` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsGovernedByHitEffect`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `AlienBeastEyeStalks`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlienBeastEyeStalks` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlliesTakeExtraTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlliesTakeExtraTurn` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllyInfested`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Miscellaneous.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | Examples: `allies` | 1 |
| [`object`](./Enums.md#enum-object) | Enum | Examples: `CharmedMaggot` | 1 |

</details>


---

### `AlternateIdleAnimation`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlternateIdleAnimation` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlwaysHitDifferentTargets`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AlwaysHitDifferentTargets` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Ammo`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 26

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Ammo` | Number | Applies or references the  | 26 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Angel`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Angel` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyPassives`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`Conditional_RandomChance`](./Abilities_and_Spells.md#context-conditional_randomchance), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`StatusOnBattleEnd`](./Abilities_and_Spells.md#context-statusonbattleend) | Block | {'type': '`Block`', 'df': "Applies the nested status effects when the encounter finishes. | 3 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'AddTag' effect/state."} | 2 |
| `Flying` | Number | {'type': '`Number`', 'df': "Applies or references the 'Flying' effect/state."} | 2 |
| `IgnoreTiles` | Number | {'type': '`Number`', 'df': "Applies or references the 'IgnoreTiles' effect/state."} | 2 |
| [`YOffset`](./Enums.md#enum-yoffset) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'YOffset' effect/state."} | 2 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ElementImmune' effect/state."} | 1 |
| `KnockbackImmunity` | Number | {'type': '`Number`', 'df': "Applies or references the 'KnockbackImmunity' effect/state."} | 1 |
| `Plant` | Number | {'type': '`Number`', 'df': "Applies or references the 'Plant' effect/state."} | 1 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'ReplaceBasicAttack' effect/state."} | 1 |

</details>


---

### `ApplyToConsumed`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeleteObject` | Number | {'type': '`Number`', 'df': "Applies or references the 'DeleteObject' effect/state."} | 3 |
| `Die` | Number | {'type': '`Number`', 'df': "Applies or references the 'Die' effect/state."} | 1 |

</details>


---

### `ApplyToOthersWithSharedTagAndFaction`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Marked` | Number | {'type': '`Number`', 'df': "Applies or references the 'Marked' effect/state."} | 1 |

</details>


---

### `ApplyToRandomClosestAlly`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Number | {'type': '`Number`', 'df': "Applies or references the 'ForceMoveTowards' effect/state."} | 1 |

</details>


---

### `ApplyToRandomPartyMemberIfPossible`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'GainDisorderFromPool_PostCast' effect/state."} | 2 |

</details>


---

### `ApplyToTile`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#context-conditional_destructiblecorpse)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](./Enums.md#enum-objectonhit) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a specific physics/item object upon impact.'} | 2 |
| `SpawnBearTrap` | Number | {'type': '`Number`', 'df': "Applies or references the 'SpawnBearTrap' effect/state."} | 2 |

</details>


---

### `ArcLightning`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | {'type': '`Boolean`', 'df': 'If true, the arc will not bounce to friendly targets.'} | 4 |
| `max_distance` | Number | {'type': '`Number`', 'df': 'The maximum tile range the lightning can jump between bounces.'} | 4 |
| `stacks` | Number | {'type': '`Number`', 'df': 'The maximum number of targets the lightning can bounce to.'} | 4 |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| `ignore_self` | Boolean | {'type': '`Boolean`', 'df': 'If true, prevents the arc from bouncing back to the caster.'} | 1 |

</details>


---

### `Attraction`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Attraction` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AvoidDamagingCharmedEnemies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `AvoidDamagingCharmedEnemies` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BackstabAllDirections`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BackstabAllDirections` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BackstabFront`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BackstabFront` | Number | Examples: `1` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BasicAttackCantMiss`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BasicAttackCantMiss` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BearTrapTrail`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BearTrapTrail` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlackHolePassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BlackHolePassive` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlackHoleSuck`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BlackHoleSuck` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlessingOfPeace`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BlessingOfPeace` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BloatEyePassive2`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BloatEyePassive2` | Enum | Examples: `BloatEyeMovement2` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BloodRain`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Bloodzerked`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bloodzerked` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BodyGuard`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to use when intercepting (e.g., BodyGuardSwap).'} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 2 |

</details>


---

### `BombBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BombBehavior` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BombRatTurtle`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BombRatTurtle` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BoneArmorPassive`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BoneArmorPassive` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BounceRock`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BounceRock` | Array | Examples: `SmallRock, SmallLavaRock, [ 1 .2 ]` | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Bound`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Bound` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BreakAtAux`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BreakAtAux` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BreakIntoRocks`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BreakIntoRocks` | Enum | Examples: `SmallRock, Coin` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BreakOnElement`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BreakOnElement` | Enum | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Brittle`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 48

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Brittle` | Number | Applies or references the  | 48 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BungaCheers`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `BungaEntrance`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 2 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `health_threshold` | Number | {'type': '`Number`', 'df': ''} | 2 |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |

</details>


---

### `ButterflySwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ButterflySwarm` | Number | Examples: `2` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CanApplyToInanimate`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | {'type': '`Enum/String`', 'df': 'Spawns a specific character or entity upon impact.'} | 10 |
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | {'type': '`Enum/String`', 'df': "Applies or references the 'BreakIntoRocks' effect/state."} | 4 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 3 |
| `Vaporize` | Number | {'type': '`Number`', 'df': "Applies or references the 'Vaporize' effect/state."} | 3 |
| `GetAggroTarget` | Number | {'type': '`Number`', 'df': "Applies or references the 'GetAggroTarget' effect/state."} | 2 |
| `PreventDeathTransforms` | Number | {'type': '`Number`', 'df': "Applies or references the 'PreventDeathTransforms' effect/state."} | 1 |
| [`Temporary`](./Abilities_and_Spells.md#context-temporary) | Block | {'type': '`Block`', 'df': 'A wrapper block for applying status effects that automatically expire. | 1 |

</details>


---

### `CanMutateTo`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CanMutateTo` | Array | Examples: `[ TumorousMaggot ChargeyMaggot SwappyMaggot ], Hyde, [ Lumpy Leaper ]` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CancelPrimedAbilities`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CancelPrimedAbilities` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CanceledQueuedInput`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CanceledQueuedInput` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CantCatchDiseases`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CantCatchDiseases` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CatchBoomerang`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CatchBoomerang` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CaveFamilyEnrage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 6 |
| `count` | Number | {'type': '`Number`', 'df': 'The numerical quantity.'} | 6 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 6 |

</details>


---

### `CaveWomanBirthControl`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CaveWomanBirthControl` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CerberubsAggroTargetBehavior`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`default_form`](./Enums.md#enum-default_form) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `ChanceToAmbush`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChanceToAmbush` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChanceToBreakFree`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ability triggered upon successfully breaking free.'} | 11 |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum | {'type': '`Enum/String`', 'df': 'The ability triggered if the break free attempt fails.'} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Percentage base chance to break free.'} | 3 |

</details>


---

### `ChanceToDisableActionsIfNotCharmed`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChanceToDisableActionsIfNotCharmed` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeCatClass`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 28

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChangeCatClass` | Enum | Examples: `Fighter, Mage, Hunter` | 28 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeFaction`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChangeFaction` | Enum | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeTileOnPop`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChangeTileOnPop` | Enum | Examples: `CreepTile, GlitchTile, OilTile` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeTileUnderCharacterAtStart`
> Found in: *Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChangeTileUnderCharacterAtStart` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeTilesUnder`
> Found in: *Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ChangeTilesUnder` | Enum | Applies or references the  | 18 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CharacterLightSource`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array | {'type': '`Array`', 'df': ''} | 16 |
| `size` | Number | {'type': '`Number`', 'df': ''} | 16 |
| [`glow`](./Arrays.md#array-glow) | Array | {'type': '`Array`', 'df': ''} | 8 |

</details>


---

### `ClearDefaultDebris`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ClearDefaultDebris` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ClearStarving`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ClearStarving` | Number | Applies or references the  | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CloneWeaponTemp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CloneWeaponTemp` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CockroachSwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CockroachSwarm` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CollideWithConsumed`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CollideWithConsumed` | Equation | Examples: `1+bonus_melee_damage, 4+bonus_melee_damage, 5+bonus_melee_damage` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CollideWithThrowTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CollideWithThrowTarget` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CompleteItemQuest`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CompleteItemQuest` | Enum | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ConjureRandomAbilityFromCat`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ConjureRandomAbilityFromCat` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Consumed`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | {'type': '`Enum/String`', 'df': 'Ability triggered by the consumed entity while inside the consumer.'} | 13 |
| `force_contact` | Boolean | {'type': '`Boolean`', 'df': 'If true, enforces physical overlap.'} | 11 |
| `instant` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |
| `mount_mode` | Mixed | {'type': '`Enum/String`', 'df': 'If true, treats the consumption as riding/mounting instead of eating.'} | 8 |
| `wet` | Boolean | {'type': '`Boolean`', 'df': ''} | 8 |
| `do_not_pop_corpse` | Boolean | {'type': '`Boolean`', 'df': ''} | 7 |
| `drop_on_death` | Mixed | {'type': '`Enum/String`', 'df': ''} | 7 |
| `drop_on_self_death` | Boolean | {'type': '`Boolean`', 'df': ''} | 3 |
| [`extra_statuses`](./Abilities_and_Spells.md#context-extra_statuses) | Block | {'type': '`Block`', 'df': "Additional generic status applications. | 3 |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| `kill_on_consume` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `use_placeholder` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `CopyBasicAttackEffects`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CopyBasicAttackEffects` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CopyCatPassive_Initializer`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CopyCatPassive_Initializer` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CopyPassiveSlot`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CopyPassiveSlot` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CopySpells`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |
| `upgraded` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `CorpseVaporizer`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CorpseVaporizer` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CountAsCorpse`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CountAsCorpse` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CreateGlobalModifiers`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `BloodRain` | Number | {'type': '`Number`', 'df': "Applies or references the 'BloodRain' effect/state."} | 2 |
| [`LowerAmbientLight`](./Abilities_and_Spells.md#context-lowerambientlight) | Block | {'type': '`Block`', 'df': "A visual effect that dims the map's lighting. | 2 |

</details>


---

### `CrowAttackLink`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `CrowAttackLink` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CyborgTurns`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`TakeBonusTurnWithAIControl`](./Miscellaneous.md#context-takebonusturnwithaicontrol) | Block | Examples: `{ ... }` | 1 |
| `stacks` | Number | Examples: `1` | 1 |

</details>


---

### `DeadAltAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeadAltAbility` | Enum | Examples: `CarrionShot_Afterlife2, CarrionShot_Afterlife, LifeDrain_Afterlife` | 24 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeathwormUnderground`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeathwormUnderground` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DecoySwapper`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DecoySwapper` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeferVaporize`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeferVaporize` | Number | Applies or references the  | 18 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DelayCastAbility`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to cast later.'} | 1 |
| `lingering` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |
| `relative` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `DeleteInanimateObjectsChance`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeleteInanimateObjectsChance` | Number | Examples: `25` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeleteObject`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeleteObject` | Number | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeleteTraps`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DeleteTraps` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyphFrames`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyphFrames` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyph_Bite`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyph_Bounce`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bounce` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyph_Fire`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DemonicGlyph_Fire` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DestroyEquipmentAndAttachParasite`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#context-conditional_activeweather_any), [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#context-conditional_debuffroll), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | {'type': '`Enum/String`', 'df': 'The item pool to draw the parasite from.'} | 5 |
| `chance` | Mixed | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 3 |

</details>


---

### `DestroyNeckArmor`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DestroyNeckArmor` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DestroyTrinket`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DestroyTrinket` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DestroyWeapon`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DestroyWeapon` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DestroyWeaponThrow`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DestroyWeaponThrow` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DiceBehavior`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `dice_size` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `knockback_damage` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `DicerArt`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DicerArt` | Array | Examples: `[ 59 52 65 50 54 63 64 ]` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Die`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`keyword_tooltips`](./Characters_and_Bosses.md#context-keyword_tooltips) | Block | {'type': '`Block`', 'df': "Forces specific UI tooltips to appear. | 1 |
| [`passives`](./Characters_and_Bosses.md#context-passives) | Block | {'type': '`Block`', 'df': "Block listing intrinsic passive modifiers. | 1 |

</details>


---

### `DieViaAbilityInternally`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DieViaAbilityInternally` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DieViolently`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DieViolently` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DiesToElement`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 1 |
| `instant` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `DiesToPiercingAndSpikes`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `deferred` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `DigestDeadBodies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DigestDeadBodies` | Enum | Examples: `MoonHead_Digest, LennyCatDies, Digest` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DinoLegAnimation`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DinoLegAnimation` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisablePassiveSlot`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisablePassiveSlot` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisableSpells`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisableSpells` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisableWeapon`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisableWeapon` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Disguised`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Disguised` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisguisedTrapper`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DisguisedTrapper` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DissolveRandomArmorPiece`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DissolveRandomArmorPiece` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DissuadeInstakills`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DissuadeInstakills` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoScreenShake`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `intensity` | Number | {'type': '`Number`', 'df': ''} | 10 |
| `time` | Mixed | {'type': '`Number`', 'df': ''} | 10 |

</details>


---

### `DoubleCast`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleCast` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleCastTaggedSpells`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DoubleCastTaggedSpells` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DrainAllyCatsForFleshGolem`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DrainAllyCatsForFleshGolem` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DrinkWater`
> Found in: *Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DrinkWater` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Drowsy`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Drowsy` | Number | Applies or references the  | 15 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DustCloudBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `DustCloudBehavior` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Dybbuk1HPTracker`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Dybbuk1HPTracker` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DybbukPossessed`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `ElectricArcs`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ElectricArcs` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ElementWeakness`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ElementWeakness` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EmptyMind`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EmptyMind` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EnableWeather`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EnableWeather` | Enum | Examples: `KaijuMeteornado, KaijuFirestorm, KaijuMeteornadoSolo` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EndTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 28

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EndTurn` | Number | Applies or references the  | 28 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Enlarge`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Enlarge` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EnterMount`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EnterMount` | Enum | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EventBounterHunterPassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EventBounterHunterPassive` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EventBounty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `EventBounty` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EvolveAbilityFromPool`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 13 |
| `upgraded` | Boolean | {'type': '`Boolean`', 'df': ''} | 13 |

</details>


---

### `ExcludeFromEvents`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExcludeFromEvents` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExplodeCharacter` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_DeathBloom`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExplodeCharacter_DeathBloom` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_DeathBloom2`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExplodeCharacter_DeathBloom2` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_NoDie`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExplodeCharacter_NoDie` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_Party`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExplodeCharacter_Party` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_RockCrusher`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExplodeCharacter_RockCrusher` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_RockCrusher_PetrifyBreak`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplosionIfHitSomething`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExplosionIfHitSomething` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExtraDispersedTurns`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExtraDispersedTurns` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExtraTurnsPerTaggedUnit`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ExtraTurnsPerTaggedUnit` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FaceCamera`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FaceCamera` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FactionDisguiseSource`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FactionDisguiseSource` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FadeInsteadOfDie`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FadeInsteadOfDie` | Number | Applies or references the  | 20 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FireArmor2`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FireArmor2` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FireStorm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FireStorm` | Number | Examples: `33, 0` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FireflySwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FireflySwarm` | Number | Examples: `2` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Flammable`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 26

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Flammable` | Number | Applies or references the  | 26 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FloatingRockTrap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FloatingRockTrap` | Number | Applies or references the  | 13 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlushmasterCelebration`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FlushmasterCelebration` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlySwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FlySwarm` | Number | Examples: `50` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Fog`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fog` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Fragile`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fragile` | Number | Applies or references the  | 44 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FrankBolts`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FrankBolts` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FreeFirstCast`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FreeFirstCast` | Number | Applies or references the  | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FreeFirstCastEachMatch`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `FreeFirstCastEachMatch` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainDisorder`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GainDisorder` | Enum | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainDisorderFromPool`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Enum | {'type': '`Enum/String`', 'df': 'Probability (0.0 to 1.0) of executing this action.'} | 1 |
| [`pool`](./Enums.md#enum-pool) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `GainDisorderFromPool_PostCast`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GainDisorderFromPool_PostCast` | Enum | Examples: `forbidden_spell_consequences_crippling, forbidden_spell_consequences` | 32 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GasCanBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GasCanBehavior` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GasCloudBehavior2`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GasCloudBehavior2` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GeminiTwin`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GeminiTwin` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GenericBuff`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GenericBuff` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GenericDebuff`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 30

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GenericDebuff` | Number | Applies or references the  | 30 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GetAggroTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GetAggroTarget` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GiveBoundItemToTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GiveBoundItemToTarget` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalEnemyAutoRevive`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GoopWalk`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GoopWalk` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Grappled`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Grappled` | Number | Examples: `1, [ 1 .75 ], [ 1 .50 ]` | 16 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Grappling`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`exit_animations`](./Characters_and_Bosses.md#context-exit_animations) | Block | {'type': '`Block`', 'df': 'Animations played when leaving a form/state. | 1 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `GroundFlopper`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GroundFlopper` | Enum | Examples: `DefaultMove, MoveOne` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GuillotinaDeathHead`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `GuillotinaDeathHead` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HarpoonTrapPassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HarpoonTrapPassive` | Enum | Examples: `HarpoonTrapPull` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HeatWave`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HeatWave` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HeavyHits`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HeavyHits` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Hex`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Hex` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HiddenDoomed`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HiddenDoomed` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HideEquipment`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HideEquipment` | Enum | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HideSomeHudStuff`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `HideSomeHudStuff` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HitlerExecute`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 1 |
| [`tag`](./Enums.md#enum-tag) | Enum | {'type': '`Enum/String`', 'df': 'Specific entity tag required.'} | 1 |
| `threshold` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `IgnoreDebuffs`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IgnoreDebuffs` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IgnoreSelf`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 150

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IgnoreSelf` | Mixed | Applies or references the  | 150 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IllusionTint`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `IllusionTint` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ImmediateUseAbility`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'ID of the ability to trigger or reference.'} | 1 |
| `even_if_stunned` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `ImmediateUseAbility_Instant`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ImmediateUseAbility_Instant` | Enum | Examples: `head_CrownOfHorns` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ImmediateUseDirectionalAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ImmediateUseDirectionalAbility` | Enum | Examples: `BowlDash, BowlDash2` | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ImmobilePassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ImmobilePassive` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Imprison`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Imprison` | Enum | Examples: `BeefyCharmedLeech, CharmedLeech, Tumor` | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `InsertIntoBackgroundPlaceholder`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `InsertIntoBackgroundPlaceholder` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Instakill`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Instakill` | Number | Applies or references the  | 24 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `InterchangeDisabler`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `InterchangeDisabler` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JohnnyCriesForWashers`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `JohnnyCriesForWashers` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JohnnyNeedsWashing`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`form_washed`](./Enums.md#enum-form_washed) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `JohnnyWasher`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `JohnnyWasher` | Enum | Examples: `BBTransformZealot` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JudgementDay`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `JudgementDay` | Number | Examples: `25` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JumpAttackLeaveBehind`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `JumpAttackLeaveBehind` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KaijuWinCon`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `KaijuWinCon` | Enum | Examples: `pyrophina, zaratana` | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KillEnemyOfTypeAtBattleStart`
> Found in: *Events & Encounters, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`enemy_type`](./Enums.md#enum-enemy_type) | Enum | {'type': '`Enum/String`', 'df': ''} | 2 |
| [`fallback_spawn`](./Arrays.md#array-fallback_spawn) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>


---

### `KnockOutClone`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `KnockOutClone` | Enum | Examples: `PlayerCat_MiniMiniMe` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LaunchOffScreen`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LaunchOffScreen` | Equation | Examples: `10+bonus_melee_ability_damage` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LaunchOffScreenInstakill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LaunchOffScreenInstakill` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LeaveBehind`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': 'The entity ID to spawn.'} | 4 |

</details>


---

### `LockOrientationFaceTile`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LockOrientationFaceTile` | Array | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LoopingSoundWhileAlive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `LoopingSoundWhileAlive` | Enum | Examples: `Twister_loop, BigUFO_ambient_looping, Bomb_FuseLoop` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LowerAmbientLight`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | {'type': '`Array`', 'df': 'The target opacity/dimness level.'} | 2 |
| `speed` | Number | {'type': '`Number`', 'df': 'The transition speed.'} | 2 |

</details>


---

### `MakeBasicAttackPull`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MakeBasicAttackPull` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MakeWeaponUnbreakable`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MakeWeaponUnbreakable` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MamaCatAnimations`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MamaCatAnimations` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManglerAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManglerAttack` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManglerMonsterPassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManglerMonsterPassive` | Enum | Examples: `ManglerMonsterDashAttack` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManglerShuffle`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ManglerShuffle` | Boolean | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MassAttackThis`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MassAttackThis` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Math`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Stun` | Number | {'type': '`Number`', 'df': "Applies or references the 'Stun' effect/state."} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 2 |
| [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource) | Block | {'type': '`Block`', 'df': 'Redirects the nested effects to apply to the caster/source of the ability instead of the target. | 1 |

</details>


---

### `Meaty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Meaty` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MeteorShower`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MeteorShower` | Number | Examples: `25` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Meteornado`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Meteornado` | Number | Examples: `1` | 3 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Metronome`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array | {'type': '`Array`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `MimicMetronome`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MimicMetronome` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ModelingClayPassive`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ModelingClayPassive` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ModifyAbility`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`cost`](./Items_and_Equipment.md#context-cost) | Block | {'type': '`Block`', 'df': 'Currency value in shops/merchants. | 2 |
| [`meta`](./Items_and_Equipment.md#context-meta) | Block | {'type': '`Block`', 'df': ' | 2 |

</details>


---

### `MonkStanceSwitch`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MonkStanceSwitch` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MonkStances`
> Found in: *Cat Classes, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MonkStances` | Array | Examples: `[ BasicMonkMelee BasicMonkRanged ]` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MotherGrowController`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eat_damage`](./Characters_and_Bosses.md#context-eat_damage) | Block | {'type': '`Block`', 'df': 'Damage dealt when this entity consumes another. | 1 |
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `MotherTumorPassive`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Cat`](./Characters_and_Bosses.md#context-cat) | Block | {'type': '`Block`', 'df': 'Character Form: Base form for standard cats. | 1 |
| [`NonCat`](./Characters_and_Bosses.md#context-noncat) | Block | {'type': '`Block`', 'df': "Character Form: Behavior and stats for the 'NonCat' state. | 1 |
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `Mount`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `MutateViaAbility`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MutateViaAbility` | Enum | Examples: `BBTransformMutant` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MuteDemonicGlyphDisplay`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `MuteDemonicGlyphDisplay` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Muted`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Muted` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextPlayerCatTakesExtraTurn`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NextPlayerCatTakesExtraTurn` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NoCorpses`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `NoCorpses` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ObjectDetector`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability (0.0 to 1.0 or percentage) of this occurring.'} | 1 |
| [`object`](./Enums.md#enum-object) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `Ostracized`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Ostracized` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PackHunting`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PackHunting` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PartialPurge`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PartialPurge` | Number | Applies or references the  | 20 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PassiveIfStrAuxEquals`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](./Items_and_Equipment.md#context-passives) | Block | {'type': '`Block`', 'df': 'Passives granted by equipping this. | 7 |
| [`value`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 7 |

</details>


---

### `PassiveIfWeaponIsUsable`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Brace` | Number | {'type': '`Number`', 'df': "Applies or references the 'Brace' effect/state."} | 2 |

</details>


---

### `PassiveWhileHasDurability`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`MovementReaction`](./Items_and_Equipment.md#context-movementreaction) | Block | {'type': '`Block`', 'df': "Applies or references the 'MovementReaction' effect/state. | 1 |

</details>


---

### `PassiveWhileNotTakingTurn`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Abilities_and_Spells.md#context-addstatustobasicattack) | Block | {'type': '`Block`', 'df': "Injects a status effect payload that applies whenever the character performs a basic attack. | 1 |

</details>


---

### `PermanentCharisma`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentCharisma` | Number | Applies or references the  | 5 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PermanentConfusion`
> Found in: *Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentConfusion` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PermanentLuck`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PermanentLuck` | Number | Applies or references the  | 5 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PersistentElement`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PersistentElement` | Enum | Examples: `Holy` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PhysicalAttacksMiss`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PhysicalAttacksMiss` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Plant`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Plant` | Number | Applies or references the  | 18 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PlayBackground`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PlayBackground` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PoisonLace`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PoisonLace` | Mixed | Examples: `"X/5", 1, "X/3"` | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PoolMetronome`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | {'type': '`Array`', 'df': 'An array of ability IDs to randomly choose from.'} | 1 |

</details>


---

### `Possessed`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Possessed` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PreventSpecificInjury`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PreventSpecificInjury` | Equation | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizeAggroTarget`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PrioritizeAggroTarget` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizeFarAwayTargets`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PrioritizeFarAwayTargets` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizeHitDifferentTargets`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PrioritizeHitDifferentTargets` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizePlayerCats`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PrioritizePlayerCats` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizeWeakestEnemy`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PrioritizeWeakestEnemy` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ProbeCharmed`
> Found in: *Abilities & Spells, Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ProbeCharmed` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PullSourceToTarget`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PullSourceToTarget` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PurgeAll`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `PurgeAll` | Number | Applies or references the  | 22 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `QuakeAreaChance`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `chance` | Number | {'type': '`Number`', 'df': 'Probability of triggering the quake.'} | 2 |
| `radius` | Number | {'type': '`Number`', 'df': 'The tile radius of the quake.'} | 2 |

</details>


---

### `QueueUseAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `QueueUseAbility` | Enum | Examples: `Spider_GoInsane` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomLightning`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomLightning` | Number | Examples: `50` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomTaggedMutation`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomTaggedMutation` | Enum | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomWeatherEachFight`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomWeatherEachFight` | Array | Examples: `[ Fog Rain Windy Sandstorm HeatWave Snow Thunderstorm Bli...` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomizeAIWeightsEachTurn`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RandomizeAIWeightsEachTurn` | Array | Examples: `[ { decision_weights default move_weights stay_close } { ..., [ { decision_we...` | 16 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RealTimePressure`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RealTimePressure` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReclaimItemOnBreak`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReclaimItemOnBreak` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReflectProjectiles`
> Found in: *Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number | {'type': '`Number`', 'df': 'Recoil or self-inflicted damage/effects applied to the caster.'} | 7 |

</details>


---

### `RefreshEquipmentAbilityOnElement`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Enum | {'type': '`Enum/String`', 'df': 'Specific element type required or applied.'} | 2 |
| [`text`](./Strings.md#string-text) | String | {'type': '`String`', 'df': ''} | 2 |

</details>


---

### `RefreshItemAbilities`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RefreshItemAbilities` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RefreshOncePerFightAbilities`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RefreshOncePerFightAbilities` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RefreshWeaponAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RefreshWeaponAbility` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Regurge`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Regurge` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnAllyCatDies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnAllyCatDies` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnAllyDies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnAllyDies` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnBackstab`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReloadOnBackstab` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairAll`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RepairAll` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairAllCondition`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RepairAllCondition` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairArmorCondition`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RepairArmorCondition` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairTrinket`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RepairTrinket` | Number | Applies or references the  | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReplaceBasicAttack_Mutation`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReplaceBasicAttack_Mutation` | Enum | Examples: `FetusSpit` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReplaceSpell`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The new ability ID to insert.'} | 4 |
| `slot` | Number | {'type': '`Number`', 'df': 'The spell slot index to replace.'} | 4 |

</details>


---

### `RerollEnemy`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RerollEnemy` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReturnDinoLegs`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ReturnDinoLegs` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReviveNextRound`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `revive_health` | Number | {'type': '`Number`', 'df': 'The flat amount of health to revive with.'} | 3 |
| `AllStatsUp` | Number | {'type': '`Number`', 'df': "Applies or references the 'AllStatsUp' effect/state."} | 2 |
| `Shield` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shield' effect/state."} | 2 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 2 |
| `DivineShield` | Number | {'type': '`Number`', 'df': "Applies or references the 'DivineShield' effect/state."} | 1 |

</details>


---

### `RockyArmorPassive`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RockyArmorPassive` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RockyArmorSalvage`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `RockyArmorSalvage` | Enum | Examples: `.75` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SafeDie`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SafeDie` | Number | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Sandstorm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Sandstorm` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScalingAttackAnimation`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`default`](./Enums.md#enum-default) | Enum | {'type': '`Enum/String`', 'df': 'Baseline configuration.'} | 1 |
| [`thresholds`](./Arrays.md#array-thresholds) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>


---

### `SchizoIllusionAIModifier`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SchizoIllusionAIModifier` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScrambleEverything`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ScrambleEverything` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScrambleLastUsedSpell`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `permanent` | Boolean | {'type': '`Boolean`', 'df': 'If true, the scramble persists for the rest of the run.'} | 1 |

</details>


---

### `Scrambled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Scrambled` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SelfStun`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SelfStun` | Array | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SendRock`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SendRock` | Number | Applies or references the  | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SerratedClaws`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SerratedClaws` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetAnimationAlts`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`dead`](./Enums.md#enum-dead) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`dying`](./Enums.md#enum-dying) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |

</details>


---

### `SetCrazyEyeBackgroundWeights`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array | {'type': '`Array`', 'df': ''} | 3 |

</details>


---

### `SetFaction`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SetFaction` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetItemAux`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum | {'type': '`Enum/String`', 'df': 'Equipment slot (weapon, hat, face, chest, etc.).'} | 3 |
| [`value`](./Math_Equations.md) | Equation | {'type': '`Enum/String`', 'df': ''} | 3 |

</details>


---

### `SharkySmellsBlood`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SharkySmellsBlood` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Shatter`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Shatter` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShootHereCommand`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ShootHereCommand` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShootHereReceiver`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ShootHereReceiver` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShortCircuit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ShortCircuit` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShowText`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `ShowText` | String | Examples: `"COMBAT_POPUP_BRAINSTORM"` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SkipFirstRounds`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `pop_chance` | Number | {'type': '`Number`', 'df': ''} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `SlotMachineRollPool`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SlotResult_Jackpot_Coins` | Number | {'type': '`Number`', 'df': "Applies or references the 'SlotResult_Jackpot_Coins' effect/state."} | 2 |
| `SlotResult_Explode` | Number | {'type': '`Number`', 'df': "Applies or references the 'SlotResult_Explode' effect/state."} | 1 |
| `SlotResult_Nothing` | Number | {'type': '`Number`', 'df': "Applies or references the 'SlotResult_Nothing' effect/state."} | 1 |
| `SlotResult_RandomPickup` | Number | {'type': '`Number`', 'df': "Applies or references the 'SlotResult_RandomPickup' effect/state."} | 1 |

</details>


---

### `SmallHitExplosion`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SmallHitExplosion` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SmartMetronome`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |
| `upgraded` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `SmellBlood`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SmellBlood` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Snow`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Miscellaneous.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Examples: `Snow` | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | Examples: `amb_snow.ogg` | 1 |
| [`particles`](./Arrays.md#array-particles) | Array | Examples: `[ Snow ]` | 1 |
| `prewarm` | Number | Examples: `20` | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Examples: `day_snow` | 1 |

</details>


---

### `SolarFlare`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `damage` | Number | Examples: `5` | 1 |
| [`effects`](./Miscellaneous.md#context-effects) | Block | Examples: `{ ... }` | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | Examples: `[ Fire ]` | 1 |

</details>


---

### `SourceSwapsBackEndOfTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SourceSwapsBackEndOfTurn` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpecialGodRays`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Big`](./Miscellaneous.md#context-big) | Block | Examples: `{ ... }` | 2 |

</details>


---

### `SpecificInjury`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpecificInjury` | Equation | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpewerAltGraphics`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Fire` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'Fire' state."} | 1 |
| `FireFull` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'FireFull' state."} | 1 |
| `Normal` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'Normal' state."} | 1 |
| `NormalFull` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'NormalFull' state."} | 1 |
| `Tar` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'Tar' state."} | 1 |
| `TarFull` | Number | {'type': '`Number`', 'df': "Character Form: Behavior and stats for the 'TarFull' state."} | 1 |

</details>


---

### `SpiderInfested`
> Found in: *Abilities & Spells, Events & Encounters, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpiderInfested` | Number | Applies or references the  | 18 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpitConsumed`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpitConsumed` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpreadWater`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SpreadWater` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StackingFlowerTrail`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | {'type': '`Enum/String`', 'df': ''} | 3 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 3 |

</details>


---

### `StackingSandstorm`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StackingSandstorm` | Number | Applies or references the  | 3 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StanceSwitchToMelee`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StanceSwitchToMelee` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StartDead`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StartDead` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StartOffMap`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StartOffMap` | Number | Applies or references the  | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StevenBolts`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `StevenBolts` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SurviveAt1HP`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SurviveAt1HP` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SwallowSmallCharacter`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `SwallowSmallCharacter` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SwapWeapon`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array | {'type': '`Array`', 'df': 'An array of weapon item IDs to draw from.'} | 1 |

</details>


---

### `SwitchMusic`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | {'type': '`Enum/String`', 'df': 'The specific audio layer to transition to (e.g., map, battle).'} | 6 |
| [`new_song`](./Enums.md#enum-new_song) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the new music track.'} | 5 |
| `crossfade_speed` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `Switcheroo`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Switcheroo` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `T2CopyCat`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `T2CopyCat` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TVBotDisableAttack`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TVBotDisableAttack` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TVBotDisableSpells`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TVBotDisableSpells` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TVBotScreen`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Die` | Number | {'type': '`Number`', 'df': 'Character Form / Logic: Forces the character to die.'} | 1 |
| `Dumb` | Number | {'type': '`Number`', 'df': 'AI Profile: A simplified, less optimal decision-making profile.'} | 1 |
| `Fuck` | Number | {'type': '`Number`', 'df': "Applies or references the 'Fuck' effect/state."} | 1 |
| `Obey` | Number | {'type': '`Number`', 'df': 'AI State: Enforced compliance logic (e.g., when Charmed).'} | 1 |
| `Shit` | Number | {'type': '`Number`', 'df': "Applies or references the 'Shit' effect/state."} | 1 |
| `Stop` | Number | {'type': '`Number`', 'df': 'AI Movement: Forces the character to cease movement.'} | 1 |

</details>


---

### `TagGreed`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TagGreed` | Enum | Examples: `food, pickup, bishop_hat` | 12 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TagMetronome`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TagMetronome` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TakeExtraTurnEndOfRound`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TakeExtraTurnEndOfRound` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Tall`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Tall` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Tangled`
> Found in: *Abilities & Spells, Events & Encounters, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum | {'type': '`Enum/String`', 'df': 'The alternative sprite art to use while tangled.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `TargetedMetronome`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TargetedMetronome` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Taunting`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Taunting` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TeamCastAbility`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The underlying logic ability executed by the team.'} | 2 |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | {'type': '`Enum/String`', 'df': 'Requires participants to share this tag.'} | 2 |
| `same_orientation` | Boolean | {'type': '`Boolean`', 'df': ''} | 1 |

</details>


---

### `TeleportBackAtTurnEnd`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TeleportBackAtTurnEnd` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBackstab`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempBackstab` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBackstabBleed`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempBackstabBleed` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBackstabPiercing`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempBackstabPiercing` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBackstabPoison`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempBackstabPoison` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempPassiveUntilSettled`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`MeleeRevengeDamage`](./Characters_and_Bosses.md#context-meleerevengedamage) | Block | {'type': '`Block`', 'df': 'Reaction: Deals damage or status effects to an attacker upon receiving melee damage. | 2 |

</details>


---

### `TempPenetrate`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TempPenetrate` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TerminatorSkin`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`groups`](./Arrays.md#array-groups) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`status`](./Enums.md#enum-status) | Enum | {'type': '`Enum/String`', 'df': 'ID of the status effect to apply or check.'} | 1 |

</details>


---

### `TileTrail_Ahead`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TileTrail_Ahead` | Enum | Examples: `OilTile, WaterTile, FireTile` | 8 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TinkererBasicAttackSwitching`
> Found in: *Cat Classes, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`innate_passives`](./Cat_Classes.md#context-innate_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum | Examples: `TinkererCraft` | 1 |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum | Examples: `TinkererThrow` | 1 |

</details>


---

### `TintItem`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array | {'type': '`Array`', 'df': ''} | 1 |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum | {'type': '`Enum/String`', 'df': ''} | 1 |
| [`mul`](./Arrays.md#array-mul) | Array | {'type': '`Array`', 'df': ''} | 1 |

</details>


---

### `TireBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TireBehavior` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TossTargetIsAggroTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TossTargetIsAggroTarget` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TossTargetIsNotInWater`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TossTargetIsNotInWater` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TrackAmountKilledByPlayer`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TrackAmountKilledByPlayer` | Enum | Examples: `BonusBirdsKilled` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TradeLife`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TradeLife` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TrailBlazer`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TrailBlazer` | Mixed | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Trapper`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The specific ability ID to cast.'} | 4 |
| `cancel_movement` | Boolean | {'type': '`Boolean`', 'df': ''} | 2 |
| `pathfinding_avoidance` | Number | {'type': '`Number`', 'df': ''} | 2 |
| `range` | Number | {'type': '`Number`', 'df': 'Distance or area of effect in tiles.'} | 2 |

</details>


---

### `TrueShot`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TrueShot` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TunnelVision`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `crit_chance` | Number | {'type': '`Number`', 'df': ''} | 1 |

</details>


---

### `TurnAround`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TurnAround` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TurnControlDelay`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TurnControlDelay` | Enum | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TurnRight`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `TurnRight` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Uncontrollable`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Uncontrollable` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Undead`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 50

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Undead` | Number | Applies or references the  | 50 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UnlockOrientation`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `UnlockOrientation` | Number | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UseAbility`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | {'type': '`Enum/String`', 'df': 'The ID of the ability to trigger.'} | 1 |
| `respect_prime` | Boolean | {'type': '`Boolean`', 'df': "If true, respects the ability's prime/cooldown state."} | 1 |

</details>


---

### `UseAbility_NonStack`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `UseAbility_NonStack` | Enum | Examples: `GenericRage, BBTransformZealot` | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Vaporize`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 66

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Vaporize` | Number | Applies or references the  | 66 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeCorpse`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `VaporizeCorpse` | Number | Applies or references the  | 36 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeCorpseFlipAdvantage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `VaporizeCorpseFlipAdvantage` | Array | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeDice`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `VaporizeDice` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeInanimate`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `VaporizeInanimate` | Number | Applies or references the  | 16 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `VaporizeTarget` | Number | Applies or references the  | 6 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VisualFX`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `VisualFX` | Enum | Examples: `Holyatk, MagicMissleBlast, WaterConduct` | 27 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VisualFlySwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `VisualFlySwarm` | Number | Examples: `1` | 1 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WaggleClone`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `cWaggle` | Flag |  | 1 |
| `cWaggle2x2` | Flag |  | 1 |
| `cWaggle3x3` | Flag |  | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `Wall`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Wall` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Webbed`
> Found in: *Abilities & Spells, Cat Mutations, Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Webbed` | Number | Applies or references the  | 23 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Wet`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Wet` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WideBackstab`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `WideBackstab` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Windy`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Miscellaneous.md#context-root)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Examples: `Windy` | 1 |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | Examples: `amb_windy.ogg` | 1 |
| [`particles`](./Arrays.md#array-particles) | Array | Examples: `[ WindFull ]` | 1 |
| `prewarm` | Number | Examples: `5` | 1 |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Examples: `day_windy` | 1 |

</details>


---

### `XIsConsumedCharacterMaxHP`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsConsumedCharacterMaxHP` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsCountDeaths`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsCountDeaths` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsFreeArmorSlots`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsFreeArmorSlots` | Number | Applies or references the  | 14 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsIncreaseEachTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsIncreaseEachTurn` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsLivingAlliesWithTag`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsLivingAlliesWithTag` | Enum | Examples: `hitler_clone_fetus, dc_crow, terminator_mini` | 10 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsLivingCharactersWithTag`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsLivingCharactersWithTag` | Enum | Applies or references the  | 4 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsRampAndReset`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `XIsRampAndReset` | Number | Applies or references the  | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsSpellStormRampAndReset`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `reset_percent` | Number | {'type': '`Number`', 'df': 'The percentage of stacks to keep after resetting.'} | 1 |
| `stacks` | Number | {'type': '`Number`', 'df': 'Number of stacks or intensity to apply.'} | 1 |

</details>


---

### `YOffset`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `YOffset` | Enum | Applies or references the  | 22 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Zombie`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Property Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `Zombie` | Number | Examples: `1` | 2 |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---
