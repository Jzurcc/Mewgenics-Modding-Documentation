# Engine: Uncategorized & Structural Resources

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

> These identifiers appear in the `Passive Identifiers.txt` list but are **not** part of the standard `passive_pool`. They exist as structural property contexts or known scalar values in other sections. Entries with a full property table have their own structured block; others are listed with the contexts where they appear as a property key value.

---

## Conditionals & Logic (36)

### `Conditional_AbilityTargetIsSelf`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Conditional_ActiveWeather_Any`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DestroyEquipmentAndAttachParasite`](Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 ||
| [`weather`](./Arrays.md#array-weather) | Array | Specifies one or more weather types to check for. | 1 ||

</details>


---

### `Conditional_AffectedByElement`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusCritChance` | Integer | The flat percentage increase to critical hit chance. | 2 ||
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||

</details>


---

### `Conditional_Backstab`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusCritChance` | Integer | The flat percentage increase to critical hit chance. | 1 ||
| [`Fear`](./Arrays.md#array-fear) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 ||

</details>


---

### `Conditional_BossOrBig`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 ||

</details>


---

### `Conditional_Buddy`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Consumed`](Abilities_and_Spells.md#object-consumed) | Object | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||

</details>


---

### `Conditional_CanBeHealed`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 1 ||

</details>


---

### `Conditional_DebuffRoll`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DestroyEquipmentAndAttachParasite`](Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. | 1 ||
| [`odds`](./Enums.md#enum-odds) | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 1 ||

</details>


---

### `Conditional_DestructibleCorpse`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ApplyToTile`](Abilities_and_Spells.md#object-applytotile) | Object | Defines effects to apply to the target tile. | 2 ||
| `VaporizeCorpse` | Integer | If set, vaporizes the target's corpse, preventing revival. | 2 ||

</details>


---

### `Conditional_Displaceable`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`LaunchOffScreen`](./Math_Equations.md) | Equation | A formula string that determines the knockback force to launch the unit off-screen. | 1 ||
| `LaunchOffScreenInstakill` | Integer | If non-zero, the unit is instantly killed and launched off-screen. | 1 ||
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. | 1 ||

</details>


---

### `Conditional_Familiar`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 ||
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 ||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 1 ||
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 ||

</details>


---

### `Conditional_FinishedSpawning`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | Specifies the type of unit or object to summon as a prison. | 1 ||

</details>


---

### `Conditional_Flying`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Conditional_FormulaIsPositive`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 ||
| [`formula`](./Math_Equations.md) | Equation | A mathematical expression evaluated to determine if its result is positive, enabling the parent conditional. | 8 ||
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 ||
| [`Slow`](./Arrays.md#array-slow) | Equation | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 ||
| [`Burn`](./Math_Equations.md) | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 ||
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 ||
| [`OverrideKnockbackDamage`](./Math_Equations.md) | Equation | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 1 ||
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 ||
| [`Stun`](./Arrays.md#array-stun) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 1 ||

</details>


---

### `Conditional_HasCleansableDebuffs`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GenericBuff` | Integer | A generic buff value applied to the unit. | 1 ||
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 1 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 1 ||

</details>


---

### `Conditional_HasKnockback`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Characters_and_Bosses.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 ||
| `RemoveKnockback` | Integer | The number of knockback stacks removed from the received damage. | 1 ||
| [`TempPassiveUntilSettled`](Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | An object containing a temporary passive that is applied until the character's position is settled. | 1 ||

</details>


---

### `Conditional_HealthThreshold`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Speculative`](./Abilities_and_Spells.md#context-conditional_speculative), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 4 ||
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 2 ||
| `threshold_percent` | Integer | The percentage of max health below which the target must be for the conditional to trigger. | 2 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| [`BonusDamage`](./Math_Equations.md) | Equation | The amount of flat bonus damage added (negative values reduce damage). | 1 ||
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 1 ||
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 1 ||
| `DieViolently` | Integer | If true, causes the target to die with a violent, explosive visual effect. | 1 ||
| `FactionConversion` | Integer | Converts the target to the caster's faction. | 1 ||
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 1 ||
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 1 ||
| [`Instakill`](./Arrays.md#array-instakill) | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 ||
| [`threshold_expr`](./Math_Equations.md) | Equation | A mathematical expression whose result is used as the dynamic health threshold for the conditional. | 1 ||
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 1 ||

</details>


---

### `Conditional_InForm`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 7 ||
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 ||
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 5 ||
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 ||
| [`ForceImmediateMoveAndAttack`](Abilities_and_Spells.md#object-forceimmediatemoveandattack) | Object | An object that forces the unit to instantly move toward the target and perform a specified ability attack. | 1 ||
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 ||
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 1 ||

</details>


---

### `Conditional_IsPhysicalAttack`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToReceivedDamage`](./Characters_and_Bosses.md#context-addstatustoreceiveddamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 ||
| `RemoveKnockback` | Integer | The number of knockback stacks removed from the received damage. | 1 ||
| [`TempPassiveUntilSettled`](Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | An object containing a temporary passive that is applied until the character's position is settled. | 1 ||

</details>


---

### `Conditional_IsSelf`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideDamage` | Integer | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 ||

</details>


---

### `Conditional_IsTrample`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SetKnockback` | Integer | The knockback distance to set for the damage instance, overriding default. | 1 ||

</details>


---

### `Conditional_LastHit`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 ||
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 2 ||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 1 ||
| [`DelayCastAbility`](Abilities_and_Spells.md#object-delaycastability) | Enum / Object | Specifies the name of an ability to cast after a delay. | 1 ||

</details>


---

### `Conditional_LivingPlayerCat`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| [`Consumed`](Abilities_and_Spells.md#object-consumed) | Object | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 1 ||
| [`TempPassiveWhileHasStatus`](Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object | An object defining passives temporarily granted to the unit while it has a specific status effect. | 1 ||

</details>


---

### `Conditional_ManaThreshold`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 1 ||
| `threshold_flat` | Integer | The flat health value (in hit points) below which the target must be for the conditional to trigger. | 1 ||

</details>


---

### `Conditional_NotAlly`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 ||
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 ||

</details>


---

### `Conditional_NotBig`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | Integer | If set, displaces the target towards the source of the effect. | 1 ||

</details>


---

### `Conditional_NotBossOrBig`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 ||

</details>


---

### `Conditional_NotShielded`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. | 2 ||

</details>


---

### `Conditional_Object`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CanApplyToInanimate`](Abilities_and_Spells.md#object-canapplytoinanimate) | Object | An object containing effects that can be applied to inanimate objects. | 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 ||

</details>


---

### `Conditional_OncePerBattle`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | Specifies the item quest ID to mark as complete on kill. | 2 ||
| [`key`](./Enums.md#enum-key) | Enum | A unique string identifier used to track if an effect has been applied once per turn, preventing reapplication. | 2 ||
| `TriggerGameEnding` | Integer | If set to 1, triggers the game's ending sequence; 0 disables it. | 2 ||

</details>


---

### `Conditional_PlayerCat`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 ||
| `ConjureRandomAbilityFromCat` | Integer | The number of random abilities created or given to the cat unit from a pool of cat-themed abilities. | 2 ||
| `Adrenaline` | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. | 1 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| `GenericDebuff` | Integer | The number of stacks of a generic, untooltipped debuff applied to the target. | 1 ||
| [`KnockOutClone`](./Enums.md#enum-knockoutclone) | Enum | Specifies the ability ID used to knock out or remove the player's clone unit from battle. | 1 ||
| `Scrambled` | Integer | The number of stacks of Scrambled applied. | 1 ||
| `T2CopyCat` | Integer | The number of T2 Clone copies created or applied to the target cat. | 1 ||

</details>


---

### `Conditional_RandomChance`
> Found in: *Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Specifies the passives or status effects to apply to the unit. | 1 ||
| [`odds`](./Enums.md#enum-odds) | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 1 ||

</details>


---

### `Conditional_SourceAbilityHasTag`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 ||

</details>


---

### `Conditional_SourceHasStatus`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||

</details>


---

### `Conditional_Speculative`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`Conditional_AffectedByElement`](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IgnoreDamage` | Integer | If set, the target ignores all damage for the duration. | 3 ||
| `BonusDamageBasedOnDistance` | Integer | The flat bonus damage added per tile of distance between the source and target. | 2 ||
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 1 ||
| `CapDamage` | Integer | The maximum amount of damage dealt, capping the total after all modifiers are applied. | 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. | 1 ||
| `RandomBonusDamage` | Integer | The maximum random bonus damage added to the base damage; the actual bonus is a random value between 0 and this number. | 1 ||

</details>


---

### `Conditional_Tiny`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Reactions & Event Triggers (77)

### `AbilityAfterEnemyCastSpell_Stackable`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md#enum-abilityafterenemycastspell_stackable) | Enum | The ability to cast after an enemy spell, which can stack in effect. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityOnBattleStart_Immediate`
> Found in: *Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 34

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AbilityOnBattleStart_Immediate`](./Enums.md#enum-abilityonbattlestart_immediate) | Enum | Specifies the ability triggered instantly at the start of battle. | 34 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityOnBattleStart_UseAI`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AbilityOnBattleStart_UseAI`](./Enums.md#enum-abilityonbattlestart_useai) | Enum | Specifies the ability the unit will use at the start of battle via AI resolution. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityOnRoundEnd`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `force_display_name` | Boolean | If true, forces the display name to show for the ability. | 2 ||

</details>


---

### `AbilityOnRoundEndOnce`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `even_of_stunned` | Boolean | If true, the ability triggers only on even rounds and when the unit is stunned. | 1 ||

</details>


---

### `AllUnitsExplodeOnDeath`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllUnitsExplodeOnDeath` | Integer | The radius of the explosion that triggers when any unit dies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlliesScrambleSpellAfterCast`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlliesScrambleSpellAfterCast` | Integer | The number of times an ally's next spell cast will be scrambled (randomly redirected or modified) after the owner casts a spell. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyToSourceOnKill`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

> **Referenced by:** [`Conditional_Ally`](./Abilities_and_Spells.md#context-conditional_ally), [`Conditional_Enemy`](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | Specifies the item ID to remove from the source on kill. | 3 ||
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 ||
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | Specifies the item quest ID to mark as complete on kill. | 2 ||
| `HealthGain` | Integer | The amount of health restored to the source. | 2 ||
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 2 ||
| [`Revive`](Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 ||
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 ||
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 1 ||
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 1 ||
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 ||
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 1 ||
| [`TransformWeapon`](Abilities_and_Spells.md#object-transformweapon) | Object | An object with `from` and `to` fields specifying the weapon transformation. | 1 ||
| [`WeaponAuxMultiplier`](./Enums.md#enum-weaponauxmultiplier) | Number | A multiplier string (e.g., '.5') for the weapon's auxiliary counter on kill. | 1 ||

</details>


---

### `ArmorBreakOnHit`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer | The percentage chance that the armor breaks on hit. | 2 ||
| `durability_loss` | Integer | The amount of durability lost when the armor break effect triggers. | 2 ||

</details>


---

### `BackflipWhenTargeted`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 ||

</details>


---

### `BonusAbility_DelayedApplication`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BonusAbility_DelayedApplication`](./Enums.md#enum-bonusability_delayedapplication) | Enum | Specifies the name of a bonus ability to apply with a delay. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BramblesOnHit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BramblesOnHit` | Integer | If set to 1, spawns bramble tiles on the target's location on hit. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CanLevelUpWhenDead`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CanLevelUpWhenDead` | Integer | If 1, allows the unit to gain experience and level up while dead. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChanceToSpitOnDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `flat_chance` | Integer | The base percentage chance to spit when taking damage. | 5 ||
| `chance_per_damage` | Integer | The additional percentage chance to spit per point of damage taken. | 3 ||
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 1 ||
| `even_on_0_damage_if_knockback` | Boolean | If true, the reaction triggers on zero damage if knockback occurs. | 1 ||

</details>


---

### `ChangeTileOnDeath`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ChangeTileOnDeath`](./Enums.md#enum-changetileondeath) | Enum | Specifies the tile type that replaces the current tile when this unit dies. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CherubimReaction`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Return`](Engine_LogicKeys.md#object-return) | Enum / Object | Specifies the ability used when this unit returns to the field. | 26 ||
| [`Leave`](Engine_LogicKeys.md#object-leave) | Enum / Object | Specifies the ability used when this unit leaves the field. | 16 ||

</details>


---

### `CounterAttackAfterEnemyCastSpell`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md#enum-counterattackafterenemycastspell) | Enum | Specifies the ability the unit uses to counterattack after an enemy casts a spell. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CounterNextAttacks`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CounterNextAttacks` | Integer | The number of incoming attacks the unit will counterattack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Counterspell`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Counterspell`](Engine_StatusAndPassiveKeys.md#object-counterspell) | Integer / Object | If non-zero, negates the next incoming enemy spell and triggers the configured counterspell effects. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CrackMoonHead`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CrackMoonHead` | Integer | If set, cracks the MoonHead's head, triggering its death sequence. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeathRattleRevive`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 8 ||

</details>


---

### `DelayedAutoRevive`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 67 ||
| `rounds` | Integer | The number of rounds after which the auto-revive triggers. | 1 ||

</details>


---

### `DelayedFury`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DelayedFury` | Integer | The percentage of Fury damage that is stored and applied after a delay. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DelayedPain`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DelayedWindTrail`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DelayedWindTrail` | Integer | If set to 1, creates a delayed wind trail behind the unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DieWhenOnlyGolemsLeft`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DieWhenOnlyGolemsLeft` | Integer | If 1, the unit dies when only golem-type allies remain on the field. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Divide4OnDeath`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Divide4OnDeath`](./Enums.md#enum-divide4ondeath) | Enum | The object that spawns in four instances upon this unit's death. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleCastSpellIfManaCostUnderThreshold`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCastSpellIfManaCostUnderThreshold` | Integer | If a spell's mana cost is under this threshold, it will be cast twice. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleCastSpellThisTurn`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleCastSpellsEachTurn_Status`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCastSpellsEachTurn_Status` | Integer | The number of turns the unit gains Double Cast for spells each turn. | 3 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DustOnHit`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||

</details>


---

### `EnrageOnDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `EnrageOnDamage` | Integer | If set to 1, the unit gains enrage stacks when taking damage. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FindExtraItemFromPoolOnBattleEnd`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum | Specifies the item pool from which an extra item is granted at the end of combat. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlatHealWhenDealDamage`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlatHealWhenDealDamage` | Number | The flat amount of health healed each time damage is dealt. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlowersOnHit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlowersOnHit` | Integer | The number of flowers spawned on the tile upon hitting the target. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FreeFirstCastAndAfterSpendMana`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FreeFirstCastAndAfterSpendMana` | Integer | If set to 1, the first cast of the ability and each cast after spending mana costs no resources. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainManaWhenAnythingDies`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GainManaWhenAnythingDies` | Number | The amount of mana gained whenever any unit dies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ImmediateAbilityReaction`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 6 ||
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 2 ||
| `damage_threshold` | Integer | The amount of damage that must be dealt to trigger the ability reaction. | 2 ||
| `even_if_blocked` | Boolean | If true, the reaction triggers even if the damage is blocked. | 2 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 ||
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 ||
| `buddy_damage_only` | Boolean | If true, only damage dealt by the unit's buddy triggers the reaction. | 1 ||
| `target_furthest_valid` | Boolean | If true, the reaction targets the furthest valid enemy. | 1 ||

</details>


---

### `IncAuxCounterClamped`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 3 ||
| `max` | Integer | The maximum amount of coins that can be gained. | 3 ||

</details>


---

### `IncAuxCounterCycle`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 1 ||
| `max` | Integer | The maximum amount of coins that can be gained. | 1 ||

</details>


---

### `IncreaseItemAuxOnKill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IncreaseItemAuxOnKill` | Integer | If true, increases the item's aux counter on kill. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MadnessChanceOnTurnBegin`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Integer | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MiniVolcanoReaction`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MiniVolcanoReaction`](./Enums.md#enum-minivolcanoreaction) | Enum | Specifies the ability triggered when a mini volcano erupts near this unit. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MonkCatReactionAbilities`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell`](./Enums.md#enum-spell) | Enum | Specifies the spell ability to use as a reaction. | 924 ||
| [`trinket`](./Enums.md#enum-trinket) | Enum | The name of the trinket item the unit starts with. | 544 ||
| [`weapon`](./Enums.md#enum-weapon) | Enum | The name of the weapon item the unit starts with. | 474 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 122 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 26 ||

</details>


---

### `MoonHeadCrackedVisual`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MoonHeadCrackedVisual`](./Enums.md#enum-moonheadcrackedvisual) | Enum | Specifies the visual state for the character's cracked head appearance. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MoonHeadFinisherEnabler`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MoonHeadFinisherEnabler` | Integer | Determines the finisher state for MoonHead abilities; negative values may disable. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MutateAfterXTurns`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MutateAfterXTurns` | Integer | The number of turns after which the character automatically mutates (or transforms). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ObjectOnHit`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||

</details>


---

### `ObjectOnHitEmpty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum | Specifies the object to spawn on hitting an empty cell. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ObjectOnHitFullyEmpty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum | Specifies the object (e.g., RandomArmorPickup) to spawn on the target when the attacker's inventory is completely empty. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PassiveWhenDead`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object | An object whose nested keys define statuses applied to trample damage. | 2 ||

</details>


---

### `PassiveWhenOnTile`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`tile`](./Arrays.md#array-tile) | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 26 ||

</details>


---

### `PreEmptiveCounterNextAttacks`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReformMoonHead`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReformMoonHead` | Integer | If non-zero, triggers the Moon Head's reformation mechanic (e.g., after it eats a cat). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnKill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnKill` | Integer | If set, this ability's reload charge is restored on kill (any kill). | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnKillEnemy`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnKillEnemy` | Integer | If set, this ability's reload charge is restored only when killing an enemy. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnKillTagged`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ReloadOnKillTagged`](./Enums.md#enum-reloadonkilltagged) | Enum | Specifies the tag of enemies that, when killed, restore a charge. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairOnKill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairOnKill` | Integer | The number of charges restored to the ability upon killing a target. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReplaceBlankTilesOnBattleStart`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum | Specifies a tile type (e.g., GlassTile) that replaces all blank tiles on the battle grid at the start of combat. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RerollItemsOnBattleEnd`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RerollItemsOnBattleEnd` | Integer | If set to 1, all items in the unit's inventory are rerolled to new random items at the end of battle. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReturnBoundItemOnBattleEnd`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReturnBoundItemOnBattleEnd` | Integer | If set to 1, items bound to this character are returned to their owner at the end of battle. | 3 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SoundEventOnHit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum | Specifies the sound event ID to play on hit (e.g., "Batterup_Connect"). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatusAfterXStacks`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatusOnCollectPickup`](./Items_and_Equipment.md#context-statusoncollectpickup)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 2 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 ||
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 1 ||
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 1 ||
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 1 ||

</details>


---

### `StatusAfterXTurns`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `StatusCharactersOnRoundEnd`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 ||
| `FloatingRockTrap` | Integer | The number of stacks of Floating Rock Trap applied to the target, dealing damage when stepped on. | 1 ||
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Specifies a tag (e.g., 'crow', 'rock', 'grub_familiar') used to filter which units a status or effect applies to. | 1 ||

</details>


---

### `StatusCharactersOnRoundStart`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 ||

</details>


---

### `StatusOnEnemyCastSpell`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 ||
| `HealthGain` | Integer | The amount of health restored to the source. | 1 ||

</details>


---

### `StatusRandomEnemiesOnBattleStart`
> Found in: *Events & Encounters, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 ||
| [`Fear`](./Arrays.md#array-fear) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 ||

</details>


---

### `TempCounterAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempPreEmptiveCounterAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempPreEmptiveCounterAttack` | Integer | The number of turns of temporary pre-emptive counterattack status. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerBleedOnBleed`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TriggerBleedOnBleed` | Number | If non-zero, causes the unit to trigger additional bleed effects whenever it applies bleed to an enemy. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerDOTStatuses`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TriggerDOTStatuses` | Integer | If set to 1, triggers damage over time statuses on the target immediately. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerGameEnding`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TriggerGameEnding` | Integer | If set to 1, triggers the game's ending sequence; 0 disables it. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerMotherConsume`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TriggerMotherConsume` | Integer | The number of times the Mother consume effect is triggered. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerMotherGrow`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TriggerMotherGrow` | Integer | The number of times the Mother grow effect is triggered. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UnlimitedDeathRattleRevive`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 ||

</details>


---

### `UseAbilityWhenOutOfStatus`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||

</details>


---

## Stat Modifiers & Scaling (180)

### `AIFavorLowHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AIFavorLowHealth` | Integer | The AI's favorability weight for targeting low-health units. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityDamageMultiplier`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityDamageMultiplier` | Number | Multiplier for all ability damage dealt by the unit. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledAtHealthThreshold`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityEnabledAtHealthThreshold` | Integer | The health percentage threshold at which the ability becomes enabled. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfHasStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AbilityEnabledIfHasStatus`](./Enums.md#enum-abilityenabledifhasstatus) | Enum | Specifies the status effect that must be present on the unit for the ability to be enabled. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfNotHasStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md#enum-abilityenabledifnothasstatus) | Enum | Specifies the status that must be absent for ability to be enabled. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledOncePerFightAtHealthThreshold`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Integer | The health threshold (absolute or percentage) at which this ability becomes enabled once per fight. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityHealthThreshold`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`ROOT`](./Characters_and_Bosses.md#context-root), [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 11 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 6 ||
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 5 ||
| `use_ai` | Boolean | If true, the ability uses AI targeting logic when triggered at the threshold. | 2 ||
| `also_use_if_buddy_is_dead` | Boolean | If true, the ability is also triggered when the unit's buddy is dead. | 1 ||
| [`threshold_min`](./Math_Equations.md) | Equation | The minimum health threshold formula (e.g., X) for the ability to trigger. | 1 ||

</details>


---

### `AbsorbManaFromOtherSpells`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbsorbManaFromOtherSpells` | Integer | If set, this ability absorbs mana from other spells when cast. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddAdvantageToEvent`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 54 ||
| [`add`](./Arrays.md#array-add) | Array / Integer | The amount or an array of values added to the event's advantage or item tint. | 1 ||
| [`options`](./Arrays.md#array-options) | Array | An array of named option objects within an event, each defining a possible action the player can take. | 1 ||

</details>


---

### `AddConstitution`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddConstitution` | Number | The amount of constitution added to the unit. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 16 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddElementsToSpells`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddElementsToSpells`](./Enums.md#enum-addelementstospells) | Enum | Specifies which element to add to spells. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddEndOfCombatRegen`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddEndOfCombatRegen` | Integer | The amount of health regenerated after combat ends. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddLeechesStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddLeechesStatus` | Integer | The number of stacks of Leech status applied to the source, healing when dealing damage. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddPostProcessEffect`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean | If true, the post-process effect requires a framebuffer to be active. | 1 ||
| [`shader`](./Enums.md#enum-shader) | Enum | Specifies which shader to use for the post-process effect. | 1 ||

</details>


---

### `AddSpiritBombCharges`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddSpiritBombCharges` | Integer | The number of charges added to the Spirit Bomb ability. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddStatusToBackstabs`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 ||

</details>


---

### `AddStatusToFirstSpellEachTurn`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||

</details>


---

### `AddStatusToReceivedDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 ||

</details>


---

### `AddTilesetObjects`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FloatingDebris`](Engine_LogicKeys.md#object-floatingdebris) | Object | An object defining parameters for spawning floating debris tileset objects. | 1 ||

</details>


---

### `AddWeaponAux`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsLastEnemyThatDealtDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AggroTargetIsLastEnemyThatDealtDamage` | Integer | If 1, the unit's aggro target is the last enemy that damaged it. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsLowestHealthEnemyTillItDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Integer | If 1, the unit focuses the lowest health enemy until that enemy dies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsLowestMaxHealthCat`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AggroTargetIsLowestMaxHealthCat` | Integer | If 1, the unit targets the cat ally with the lowest maximum health. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllSpellsCostActPoints`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllSpellsCostActPoints` | Integer | If 1, all spells require action points instead of mana or other resources. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllSpellsCostCharge`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllSpellsCostCharge` | Integer | The number of charges required to cast any spell, adding a universal charge cost. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllStatsUpPerDisorder`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUpPerDisorder` | Integer | The amount by which all stats increase for each disorder (negative status) the unit has. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlwaysChosenForLevelUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlwaysChosenForLevelUp` | Integer | If set to 1, this unit is always presented as a level-up option when gaining a level. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyMultipleTimes`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 3 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||

</details>


---

### `ApplyStatusesNextTurnBegin`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 ||

</details>


---

### `BalanceStats`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BalanceStats` | Integer | If set to 1, the unit's stats are balanced (redistributed) towards an average value. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BaseStatMultiply`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BaseStatMultiply`](./Enums.md#enum-basestatmultiply) | Number | A multiplier applied to the unit's base stats. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusDamageBasedOnDistance`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamageBasedOnDistance` | Integer | The flat bonus damage added per tile of distance between the source and target. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusDamageBasedOnMana`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamageBasedOnMana` | Integer | The amount of bonus damage dealt, scaled by the target's current mana. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusHealthRegenPerDisorder`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusHealthRegenPerDisorder` | Number | The amount of additional health regenerated per turn for each disorder the unit has. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusTurnPattern`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BonusTurnPattern`](./Arrays.md#array-bonusturnpattern) | Array | An array defining the pattern of bonus turns granted to this unit. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BoostReceivedHealing`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BoostReceivedHealing` | Integer | The amount of bonus healing received from all sources. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleCharismaUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleConstitutionUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleDexterityUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleIntelligenceUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleLuckUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleSpeedUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BrittleStrengthUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CantSpreadDiseases`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CantSpreadDiseases` | Integer | The number of stacks that prevent the unit from spreading diseases. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CapBasicAttackDamage`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CapBasicAttackDamage` | Integer | The maximum amount of damage that can be dealt by a basic attack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CapDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CapDamage` | Integer | The maximum amount of damage dealt, capping the total after all modifiers are applied. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CapReceivedDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CapReceivedDamage` | Integer | If 1, the unit caps incoming damage to a maximum per hit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CastAgainWithStatus`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddTemporaryEffectsToBasicAttack`](./Items_and_Equipment.md#context-addtemporaryeffectstobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideDamage` | Integer | Overrides the damage of the current action to this flat value (can be negative to heal). | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `CatPartsSizeScale`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head`](./Enums.md#enum-head) | Enum / Number | The catalog ID for the cat's head part. | 784 ||

</details>


---

### `CatPartsSizeScaleStatus`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mouth`](./Enums.md#enum-mouth) | Number | The catalog ID for the cat's mouth part. | 386 ||
| `arm2` | Number | The catalog ID for the cat's second arm part. | 358 ||
| `arm1` | Number | The catalog ID for the cat's first arm part. | 354 ||
| [`body`](./Arrays.md#array-body) | Number | The catalog ID for the cat's body part. | 346 ||

</details>


---

### `CharacterTypeGainsStatusAtBattleStart`
> Found in: *Events & Encounters, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`Fear`](./Arrays.md#array-fear) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 ||
| [`Stun`](./Arrays.md#array-stun) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 ||
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 ||

</details>


---

### `ChargeFists`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ChargeFists`](Engine_StatusAndPassiveKeys.md#object-chargefists) | Integer / Object | The number of charge stacks applied to unarmed attacks. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CharismaIsMaxStat`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CharismaIsMaxStat` | Integer | Treats the Charisma stat as the character's maximum stat for calculations. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ConjureBonusAbility`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 2 ||

</details>


---

### `ConjureSingleUseBonusAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum | Specifies the bonus ability to conjure for single use (e.g., 'random' for a random one). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ContextualHeal`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ContextualHeal` | Integer | The amount of healing applied contextually (e.g., to allies). | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ConvertDamageToScaledStatus`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `CurrentWeaponAddElectricElement`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CurrentWeaponAddElectricElement` | Integer | The number of turns the current weapon gains the electric element. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CurrentWeaponAddPoison`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CurrentWeaponAddPoison` | Integer | The number of poison stacks added to the target's current weapon; an integer value applies that many stacks. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageBasedOnMissingHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageBasedOnMissingHealth` | Integer | The percentage of the target's missing health dealt as additional damage. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageFromBehindOnly`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageFromBehindOnly` | Integer | If 1, the unit can only be damaged when attacked from behind. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageTrinket`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageTrinket` | Integer | The amount of durability damage dealt to the target's equipped trinket. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageWeapon`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageWeapon` | Integer | The amount of durability damage dealt to the equipped weapon. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoDamage`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`post_spawn_statuses`](./Abilities_and_Spells.md#context-post_spawn_statuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 62 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 54 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum | Specifies whether the damage effect applies to tiles; 'all' damages every tile in the area. | 2 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 ||

</details>


---

### `DontHealEnemies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DontHealEnemies` | Integer | If true, the healing effect does not affect enemy units. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleReceivedNegativeStatus`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleReceivedNegativeStatus` | Integer | If true, the unit receives double the stacks of negative status effects applied to it. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleReceivedPositiveStatus`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleReceivedPositiveStatus` | Integer | If true, the unit receives double the stacks of positive status effects applied to it. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum | The name of a status effect whose stacks are doubled when applied. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DuplicateRandomEquippedItem`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DuplicateRandomEquippedItem` | Integer | If true, creates a copy of a random equipped item. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExistUntilIdleUpkeep`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExistUntilIdleUpkeep` | Integer | If true, the entity persists until the source unit enters idle upkeep. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExtraBasicAttacks_Status`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FaceAwayLastDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 1 ||
| `override_hit_animation` | Boolean | If true, the character's hit animation is overridden by the face-away animation. | 1 ||
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 ||

</details>


---

### `FaceLastDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 ||

</details>


---

### `FactionUprising`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`extra_statuses`](Abilities_and_Spells.md#object-extra_statuses) | Object | An object containing additional status effects (with stack counts) applied to the consumed unit. | 1 ||

</details>


---

### `FlatAIBonus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlatAIBonus` | Integer | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalMeleeRevengeDamage`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 ||

</details>


---

### `HPAltStates`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum | Specifies the animation clip name to use for the alt state. | 1 ||
| [`thresholds`](./Arrays.md#array-thresholds) | Array | An array of health percentage thresholds that trigger an alt state. | 1 ||

</details>


---

### `HealNeighborsEachTurn`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `HealPercentMaxHP`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealPercentMaxHP` | Integer | The percentage of max HP healed (e.g., 100 for full heal). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HealRandomInjury`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HealTo`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealTo` | Integer | The target HP percentage to heal the unit to (e.g., '50%' for half max HP). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HealthMultiplier`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthMultiplier` | Float | A multiplier applied to the unit's base health. | 15 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IgnoreDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IgnoreDamage` | Integer | If set, the target ignores all damage for the duration. | 18 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IncreaseCumulativeBlastDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IncreaseCumulativeBlastDamage` | Integer | If true, increases the cumulative blast damage counter. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `InstantMaxHealthUp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `InstantMaxHealthUp` | Integer | The amount of permanent maximum health increase. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JesterLevelUpRerolls`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `JesterLevelUpRerolls` | Integer | The number of additional rerolls granted when leveling up. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KnockUpAndAway`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Conditional_LastHit`](./Abilities_and_Spells.md#context-conditional_lasthit), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 20 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 18 ||
| `height` | Integer | The height in tiles the target is launched into the air. | 16 ||
| `circular_variance` | Integer | The random variance in the knockback direction, in tiles. | 1 ||

</details>


---

### `LateStatusApplication`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Integer | The amount of temporary damage increase to the current weapon. | 3 ||
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. | 1 ||

</details>


---

### `LowGravityRangeBoost`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `LowGravityRangeBoost` | Number | The increase in attack range under low gravity. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManaGainRange`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusEachTurnBegin`](./Items_and_Equipment.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 1 ||
| `min` | Integer | The minimum amount of coins that will be gained. | 1 ||

</details>


---

### `MaxHPUp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MaxHPUp` | Integer | The amount of maximum health permanently increased. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MergeDamageInstance`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean | If false, the ability cannot instantly kill or remove the target, often used for non-lethal effects. | 1 ||
| `force_no_hit_animation` | Boolean | If true, suppresses the hit animation when merging damage instances. | 1 ||

</details>


---

### `MulticatHeads`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MulticatHeads` | Integer | The number of additional heads the Multicat has. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MultiplyReceivedHealing`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MultiplyReceivedHealing` | Integer | The multiplier applied to all healing the unit receives. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextAbilityHeals`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NextAbilityHeals` | Integer | The number of stacks causing the next ability to heal instead of damage. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextActionLuckUp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NextActionLuckUp` | Integer | The number of stacks increasing luck for the next action. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextAttackBonusRange`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NextAttackBonusRange` | Integer | The added range for the unit's next basic attack. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextAttackSpecialCrit`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Integer | The additional critical hit damage multiplier. | 1 ||
| `extra_coins_per_stack` | Integer | The number of extra coins gained per stack of the associated status. | 1 ||
| `luck_increase` | Integer | The flat increase to the unit's luck stat. | 1 ||

</details>


---

### `NextBattleStatusStacks`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `fights` | Integer | The number of future battles the status effect will be applied at the start of. | 4 ||
| `MadnessChanceOnTurnBegin` | Integer | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 1 ||

</details>


---

### `NextDamageReduceAndHealAllies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NextDamageReduceAndHealAllies` | Integer | The number of stacks reducing next damage and healing nearby allies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextTurnDoubleRangedDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NextTurnDoubleRangedDamage` | Integer | The number of stacks doubling ranged damage on the next turn. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NoHealthRegen`
> Found in: *Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NoHealthRegen` | Number | Prevents the unit from regenerating health normally. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `OverHealToStatuses`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 ||
| `stack_scale` | Integer | The scaling factor for how many stacks of the over-heal status are applied. | 1 ||
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 1 ||

</details>


---

### `OverManaReducesManaCosts`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverManaReducesManaCosts` | Number | If set to 1, any mana the unit has above their maximum reduces the cost of abilities. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PassiveWhileHasStatus`
> Found in: *Cat Mutations, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||

</details>


---

### `PassiveWhileNotHasStatus`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 2 ||

</details>


---

### `PermanentUpgradeRandomActive`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PermanentUpgradeRandomActive` | Integer | The number of random active abilities permanently upgraded. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PermanentUpgradeRandomActiveOrPassive`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PermanentUpgradeRandomActiveOrPassive` | Integer | The number of random active or passive abilities permanently upgraded. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RNGCannonRandomDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RNGCannonRandomDamage` | Integer | The maximum random damage value for the RNG Cannon attack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomBonusDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomBonusDamage` | Integer | The maximum random bonus damage added to the base damage; the actual bonus is a random value between 0 and this number. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomPermanentStatsDistinct`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`StatusOnEatPill`](./Miscellaneous.md#context-statusoneatpill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 982 ||

</details>


---

### `RandomSeededStatModifier`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | An array defining a random, seeded modifier to stats, typically in the format [modifier, offset]. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomStatDown`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomStatDown`](./Arrays.md#array-randomstatdown) | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 20 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RebukeDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RebukeDamage` | Integer | The amount of damage dealt by a rebuke backlash effect. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReduceManaCostExcludeBrainstorm`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReduceManaCostExcludeBrainstorm` | Integer | The number of stacks reducing mana cost, excluding Brainstorm. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReduceSpellCostsPerDisorder`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReduceSpellCostsPerDisorder` | Integer | The amount of mana cost reduction per disorder the unit has. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReduceSpellCostsPerParasite`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReduceSpellCostsPerParasite` | Integer | The amount of mana cost reduction per parasite the unit is hosting. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RefreshNonManaItemAbilities`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RefreshNonManaItemAbilities` | Integer | The number of times non-mana item abilities are recharged. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnAnyDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnAnyDamage` | Integer | If set to 1, restores a charge when any damage is taken. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnElementalDamageReceived`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ReloadOnElementalDamageReceived`](./Enums.md#enum-reloadonelementaldamagereceived) | Enum | Specifies the elemental type of damage that, when received, restores a charge. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnSpendMana`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnSpendMana` | Integer | If set to 1, restores a charge when mana is spent. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnTotalDamageReceived`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnTotalDamageReceived` | Integer | The threshold of total damage received to restore a reload charge. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnUseAbilityWithManaCost`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnUseAbilityWithManaCost` | Integer | Specifies the amount of mana cost that, when used, restores a charge. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoteFlatLeech`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RemoteFlatLeech` | Integer | The flat amount of remote leech applied to the target on basic attack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoteLeech`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RemoteLeech` | Integer | The amount of remote leech applied to the target on basic attack. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScaledStatusAlliesOnSpendMana`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---

### `SelfStatusCarefulness`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SelfStatusCarefulness` | Integer | The carefulness level when applying statuses to self, used to control stacking. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetHealth`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SetHealth` | Integer | Sets the target's health to a specific flat value or percentage. | 18 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShadowCrit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ShadowCrit` | Integer | If non-zero, enables the Shadow Crit mechanic, granting bonus critical hit chance or damage from stealth. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShowFakeDamage`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`style`](./Arrays.md#array-style) | Array | Specifies the visual styles (e.g., crit) used for the fake damage display. | 1 ||

</details>


---

### `SpeedUp_WithoutInitiative`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StanceSwitchToRanged`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StanceSwitchToRanged` | Integer | If set, switches the source to ranged stance. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatBounty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StatBounty` | Integer | The number of stacks of the StatBounty status effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatDependentPassive`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddDamageToBasicAttack`](./Math_Equations.md) | Equation | Additional damage added to the basic attack, either as a flat value or formula. | 4 ||

</details>


---

### `StatusAdjacentOnTheirTurnEnd`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Integer | The distance to force the target away from the source. | 1 ||

</details>


---

### `StatusCollector`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 ||
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 7 ||
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 ||

</details>


---

### `StatusEachRoundBegin`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number | The amount of non-stacking shield granted. | 8 ||

</details>


---

### `StatusEachRoundEnd`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 1 ||

</details>


---

### `StatusEachTurnBeginIfHasStatus`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 11 ||
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 ||
| `consume` | Boolean | If true, the status is consumed after triggering. | 2 ||
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 ||
| `HealthGain` | Integer | The amount of health restored to the source. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||

</details>


---

### `StatusEachTurnEndIfEnabledAtStartOfTurn`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 ||

</details>


---

### `StatusEveryXSpellCastsEachTurn`
> Found in: *Cat Mutations, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `StatusIfUnusedActPoints`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BackflipWhenTargeted`](./Math_Equations.md) | Equation | The number of backflip charges, or an object defining its ability. | 2 ||
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 2 ||

</details>


---

### `StatusOnBackstab`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 ||
| `SerratedClaws` | Integer | The number of stacks of the SerratedClaws status applied, or an object defining its display strings. | 1 ||

</details>


---

### `StatusOnBreak`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 ||
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 ||
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 5 ||
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | The tile type to change the ground tiles under the target to. | 3 ||
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 3 ||
| `HealthGain` | Integer | The amount of health restored to the source. | 3 ||
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 3 ||
| [`ApplyToRandomPartyMemberIfPossible`](Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object | Contains an inner effect block that is applied to a random living party member if one exists. | 1 ||
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 ||
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. | 1 ||
| [`FindItem`](./Enums.md#enum-finditem) | Enum | The name of the specific item to find and add to the source's inventory. | 1 ||
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | Specifies the name of the disorder gained. | 1 ||
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. | 1 ||
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 ||
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 ||

</details>


---

### `StatusOnDie`
> Found in: *Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 6 ||

</details>


---

### `StatusOnEnemyConfused`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](Engine_StatusAndPassiveKeys.md#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. | 1 ||

</details>


---

### `StatusOnEnemyDeath`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer | The number of charge stacks applied. | 1 ||

</details>


---

### `StatusOnFallAsleep`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 ||
| [`FillMana`](./Arrays.md#array-fillmana) | Integer | The amount of mana restored, or an [amount, probability] array. | 1 ||
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 1 ||

</details>


---

### `StatusOnFullMana`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---

### `StatusOnSetPieceBreak`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`set`](./Enums.md#enum-set) | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. | 1504 ||
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 1 ||
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. | 1 ||
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 1 ||
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 1 ||
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 1 ||
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. | 1 ||
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 1 ||
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 1 ||

</details>


---

### `StatusOverlappingCharactersAndDie`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 ||

</details>


---

### `StripStatuses`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StripStatuses` | Integer | If 1, removes all status effects from the unit at the beginning of its turn. | 20 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SwapHighestAndLowestStat`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SwapHighestAndLowestStat` | Integer | If non-zero, swaps the unit's highest base stat value with its lowest. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TakeBonusTurnWithAIControl`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 2 ||

</details>


---

### `TallTumorManaBurn`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TallTumorManaBurn`](./Enums.md#enum-talltumormanaburn) | Enum | Specifies the mana burn ability used by the TallTumor. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TeamBonusAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum | Specifies the ability ID granted to allies as a team bonus. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempCritChanceUp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempCritChanceUp` | Integer | The amount of temporary critical hit chance (in percentage points) added. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempManaCostReduction`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempManaCostReduction` | Integer | The number of stacks of temporary mana cost reduction. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempMeleeRangeUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempMeleeRangeUp` | Integer | The number of tiles added to the unit's melee attack range as a temporary buff. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempNoManaRegen`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempNoManaRegen` | Integer | The number of turns the unit cannot regenerate mana. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempPassiveWhileHasStatus`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`Conditional_FirstApplicationThisTurn`](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 ||
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | Defines the damage and effects applied back to a melee attacker upon being hit. | 20 ||
| `AddManaRegen` | Integer | The flat amount of mana regenerated per turn. | 4 ||
| [`ReplaceSpell`](Abilities_and_Spells.md#object-replacespell) | Object | Defines which spell slot to replace and with which ability. | 4 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 3 ||

</details>


---

### `TempRangeUp`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempRangeUp` | Integer | The amount of temporary range increase applied. | 16 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TickDownStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum | Specifies the name of the status effect whose duration is reduced by one tick. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TimeDelayStatusApplication`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`delay`](./Enums.md#enum-delay) | Number | The delay in seconds before the ability's effect triggers. | 4 ||
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 ||
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object | Defines a new song or layer for the background music. | 2 ||
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | Defines global gameplay modifiers to activate. | 1 ||
| [`DoScreenShake`](Abilities_and_Spells.md#object-doscreenshake) | Integer / Object | If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake. | 1 ||
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 1 ||
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 1 ||
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Specifies the name of a character to spawn globally. | 1 ||
| `PlayBackground` | Integer | Specifies the background index to play. | 1 ||
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Number | The fade-out duration in seconds for ambient light effects. | 1 ||
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 1 ||

</details>


---

### `TormentorHeal`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TormentorHeal` | Integer | If set to 1, the Tormentor can heal itself. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TowerDefenseStatus`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TowerDefenseStatus` | Integer | The number of stacks of the sentry/tower defense status, granting stationary attack capabilities. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TowerDefenseStatus2`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TowerDefenseStatus2` | Integer | The number of stacks of the enhanced sentry/tower defense status. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Trapper_Status`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Trapper_Status` | Integer | The number of trap-related status stacks applied. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UndoDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `UndoDamage` | Integer | The amount of damage reversed. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UpTireBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `UpTireBehavior` | Integer | The behavior type integer for the Tire's upward form. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UpgradeRandomAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `UpgradeRandomAbility` | Integer | The number of random abilities upgraded upon effect. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VisualCountDownThenApplyStatus`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 1 ||

</details>


---

### `WeaponAuxMultiplier`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`WeaponAuxMultiplier`](./Enums.md#enum-weaponauxmultiplier) | Number | A multiplier string (e.g., '.5') for the weapon's auxiliary counter on kill. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsCountStatusStacks`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`XIsCountStatusStacks`](./Enums.md#enum-xiscountstatusstacks) | Enum | Specifies the status field whose stacks are counted to set X. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsMultipliedPercentHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`XIsMultipliedPercentHealth`](./Arrays.md#array-xismultipliedpercenthealth) | Array | The [stacks, probability] for multiplying health by a percentage. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsOtherHealsThisTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `XIsOtherHealsThisTurn` | Integer | If set, tracks other heals this turn for some effect. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsRecycleCostReduction`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `XIsRecycleCostReduction` | Integer | Specifies the amount of recycle cost reduction applied to X. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsTargetHealth`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_Boss`](./Abilities_and_Spells.md#context-conditional_boss), [`Else`](./Abilities_and_Spells.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BonusDamage`](./Math_Equations.md) | Equation | The amount of flat bonus damage added (negative values reduce damage). | 2 ||

</details>


---

### `XIsTimesDamageTaken`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `XIsTimesDamageTaken` | Integer | If set, multiplier for damage taken to apply some effect. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Immunities & Defenses (42)

### `AllDamageImmune_IncludingSpeculative`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllDamageImmune_IncludingSpeculative` | Integer | If set to 1, this unit is immune to all damage, including speculative damage. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyShieldToApplierBasedOnMaxHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ApplyShieldToApplierBasedOnMaxHealth` | Integer | The amount of shield applied to the applier based on a fraction of their max health. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlockAllDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BlockAllDamage` | Integer | If 1, the unit blocks all incoming damage. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlockDamageUnderThreshold`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BlockDamageUnderThreshold` | Integer | The maximum amount of damage from a single hit that will be completely blocked. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlockNegativeStatus`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BlockNegativeStatus` | Integer | The percentage chance to completely block the application of a negative status effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BreakWhenNoShield`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BreakWhenNoShield` | Integer | If 1, the armor breaks when the unit has no shield remaining. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CanShield`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CanShield` | Integer | If set to 1, this unit can generate shields. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChanceToBlock`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ChanceToBlock` | Integer | The percentage chance to block incoming damage. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CharmImmunity`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CharmImmunity` | Integer | If true, the unit is immune to the Charmed status effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DivineShieldPickup`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DivineShieldPickup` | Integer | The number of divine shield charges granted on pickup. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DodgeChanceWithBlindSpot`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChanceWithBlindSpot` | Integer | The percentage chance to dodge attacks while a blind spot condition is active. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DodgeChance_Status`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DodgeWhenTargeted`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||

</details>


---

### `ForceDodgeEverything`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceDodgeEverything` | Integer | If set to 1, the unit will always dodge all incoming attacks. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FullBlockEverything`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FullBlockEverything` | Integer | If set to 1, the unit fully blocks all incoming damage. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FullBlockEverythingTo0Damage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FullBlockEverythingTo0Damage` | Integer | If set to 1, the unit reduces all incoming damage to 0. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GoopImmunity`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GoopImmunity` | Integer | If set to 1, the unit is immune to goop status effects. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IceBlockBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IceBlockBehavior` | Integer | An integer flag that controls the behavior mode of an ice block entity. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Invulnerable`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Invulnerable` | Integer | The number of Invulnerable stacks, making the unit immune to damage. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KaijuKnockbackImmune`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `KaijuKnockbackImmune` | Integer | If 1, the unit is immune to knockback from kaiju sources. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KnockbackDamageImmuneUntilSettled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `KnockbackDamageImmuneUntilSettled` | Integer | If non-zero, makes the target immune to damage from knockback until they stop moving. | 20 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MagicDamageImmune`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MagicDamageImmune` | Integer | If set to 1, this unit is immune to magic damage. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NoHealthOnlyShield`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NoHealthOnlyShield` | Integer | If set (e.g., 1), the unit has no health and only a shield for damage absorption. | 24 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NonStackingShield`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number | The amount of non-stacking shield granted. | 16 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `OverHealToShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverHealToShield` | Integer | The amount of excess healing converted into temporary shield points. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PassiveWhileShielded`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 ||

</details>


---

### `ReloadOnGainDivineShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnGainDivineShield` | Integer | If set to 1, restores a charge when a Divine Shield is gained. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ResetArmorShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ResetArmorShield` | Integer | The amount of armor shield restored. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScaledStatusOnHolyShieldBlock`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. | 1 ||

</details>


---

### `SetBrittleImmune`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SetBrittleImmune`](./Enums.md#enum-setbrittleimmune) | String | Sets the unit's material to the specified type, granting immunity to the Brittle status. | 7 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetFragileImmune`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SetFragileImmune`](./Enums.md#enum-setfragileimmune) | String | Sets the unit's material to the specified type, granting immunity to the Fragile status. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SetShield` | Integer | Sets the target's shield value to a specific flat amount. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpellShield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpellShield` | Integer | The number of stacks of SpellShield, which blocks incoming spells. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatusOnDodge`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 ||

</details>


---

### `StatusOnTakeHealthOrShieldDamage`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Metronome`](Abilities_and_Spells.md#object-metronome) | Integer / Object | The number of times Metronome triggers, or an object with stacks and banned abilities. | 4 ||
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 ||

</details>


---

### `StunImmunity`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | If true, removes any existing stun effect when this immunity is applied. | 1 ||

</details>


---

### `TempInjuryImmunity`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempInjuryImmunity` | Integer | The number of stacks of temporary immunity to Injuries. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ThornsDamageImmuneUntilSettled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ThornsDamageImmuneUntilSettled` | Integer | The number of turns the target is immune to thorns damage until it settles. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TileDamageImmuneUntilSettled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TileDamageImmuneUntilSettled` | Integer | The number of turns the target is immune to tile damage until it settles. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TileElementDamageImmunity`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TileElementDamageImmunity`](./Enums.md#enum-tileelementdamageimmunity) | Enum | Determines which tile element type the character is immune to damage from. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UseAbilityWhenShieldDepleted`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`UseAbilityWhenShieldDepleted`](./Enums.md#enum-useabilitywhenshielddepleted) | Enum | The ability to use when the unit's shield is fully depleted. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WispDodge`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `WispDodge` | Integer | If 1, the unit gains the Wisp's dodge ability. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Auras & Area of Effect (20)

### `AOEBonus`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AOEBonus` | Integer | The bonus number of additional targets or tiles affected by an area-of-effect ability. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlienBeastDangerZones`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AlienBeastDangerZones`](./Arrays.md#array-alienbeastdangerzones) | Array | An array of ability names that mark dangerous zones for the Alien Beast fight. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllStatsAura`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum | Specifies the tag that units must have to be affected by this aura. | 1 ||
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `AlluringDoodieEater`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 4688 ||
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

</details>


---

### `AllyDodgeChanceAura`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 1 ||

</details>


---

### `BaitAura`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 4 ||

</details>


---

### `BasicAIDangerZone`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BasicAIDangerZone` | Integer | The radius of the danger zone used by the basic AI for area denial. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BattlefieldUniqueRandomPassive`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Integer | The weight for the demonic glyph of bite, or its configuration. | 1 ||
| `DemonicGlyph_Bounce` | Integer | The weight for the demonic glyph of bounce, or its configuration. | 1 ||
| `DemonicGlyph_Fire` | Integer | The weight for the demonic glyph of fire, or its configuration. | 1 ||
| `DemonicGlyph_Movement` | Integer | The weight for the demonic glyph of movement, or its configuration. | 1 ||
| `DemonicGlyph_Summon` | Integer | The weight for the demonic glyph of summon, or its configuration. | 1 ||

</details>


---

### `BrittleDuringElement`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum | Makes the unit brittle while in contact with the specified element. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChargeSpiritBombAura`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ChargeSpiritBombAura`](./Enums.md#enum-chargespiritbombaura) | Enum | Specifies the ability to charge for spirit bomb aura. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DamageDistanceAOEFalloff`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageDistanceAOEFalloff` | Integer | The falloff multiplier applied to AoE damage based on distance from the center of the effect. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplayDangerAOE`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DisplayDangerAOE`](./Enums.md#enum-displaydangeraoe) | Enum | The ability whose area of effect is displayed to warn players. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoDistortionRing`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 6 ||
| [`radius`](./Arrays.md#array-radius) | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 6 ||
| [`speed`](./Arrays.md#array-speed) | Array / Number | The speed of the projectile or move, can be a value or a range. | 6 ||

</details>


---

### `FragileDuringElement`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum | Specifies an element during which the unit becomes fragile, taking increased damage. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalFlowerTrapperAura`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 1 ||

</details>


---

### `GlobalHealthRegenAura`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalHealthRegenAura` | Number | The amount of health regenerated per turn to all units in range. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalManaBurnAura`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalManaBurnAura` | Number | The amount of mana burned from all enemies per turn. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalManaDrainAura`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalManaDrainAura` | Integer | The amount of mana drained per turn from all units in range. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `OrthogonalAIDangerZone`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OrthogonalAIDangerZone` | Integer | The range (in tiles) for the AI's orthogonal danger zone detection. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBasicAttackBonusAOE`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempBasicAttackBonusAOE` | Integer | The amount of temporary area-of-effect bonus on basic attacks. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Movement & Positioning (79)

### `AbilityEnabledIfMovementTrapped`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityEnabledIfMovementTrapped` | Integer | If set, ability is enabled only when the unit's movement is trapped. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddExtraTurnsBeforeRun`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddExtraTurnsBeforeRun` | Number | The number of additional turns added before the run ends. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AddMeleeKnockback`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddMeleeKnockback` | Integer | The amount of additional knockback dealt by melee attacks. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BonusKnockbackDamage`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusKnockbackDamage` | Integer | The extra damage dealt per tile of knockback. | 7 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BypassRockKnockback`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BypassRockKnockback` | Integer | If set to a non-zero number, bypasses normal rock knockback behavior. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChanceToForceEvent`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`event`](./Enums.md#enum-event) | Enum | Specifies the event to force, either by name or by a nested object defining its type and level. | 3 ||
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

</details>


---

### `CharmedFacingForceAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CharmedFacingForceAttack` | Integer | If set to a non-zero number, the charmed target is forced to attack the direction they are facing. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DashFury`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DashFury` | Integer | The amount of Fury gained after dashing. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyph_Movement`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Movement` | Integer | The weight for the demonic glyph of movement, or its configuration. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisableTrample`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisableTrample` | Integer | If set to 1, trample damage is disabled for the duration of the effect. | 20 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Displace`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Displace` | Integer | If set to 1, the unit is displaced to another location (e.g., teleport). | 24 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplaceToAbilityTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisplaceToAbilityTarget` | Integer | If set, displaces the source to the ability's target location. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplaceToOriginalPosition`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisplaceToOriginalPosition` | Integer | If non-zero, returns the unit to its original position after the effect resolves. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplaceTowardsSource`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisplaceTowardsSource` | Integer | If set, displaces the target towards the source of the effect. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FastKnockback`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FastKnockback` | Integer | The number of tiles the target is knocked back with fast animation. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlingObjectsOnTop`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlingObjectsOnTop` | Integer | The number of objects to fling on top of this unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceDisplace`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceDisplace` | Integer | The distance the target is forced to displace. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceImmediateMove`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceImmediateMove` | Integer | If non-zero, forces the character to move instantly without waiting for normal action order. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceImmediateMoveAndAttack`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_InForm`](./Abilities_and_Spells.md#context-conditional_inform)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `even_if_cant_reach` | Boolean | If true, forces the unit to attempt to move and attack even if the target is not reachable. | 1 ||

</details>


---

### `ForceMoveAndAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAndAttack` | Integer | If true, forces the target to move and attack its nearest enemy. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceMoveNonAlliesInRangeTowardsTile`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveNonAlliesInRangeTowardsTile` | Integer | The tile range within which non-allied units are forcibly moved towards a specified tile. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceMoveTowards`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Integer | The number of tiles to force the target to move toward the caster. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceMoveTowardsEnemies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveTowardsEnemies` | Variable | Specifies the ability or distance to force the target to move towards enemies. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceMoveTowardsTaggedObject`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||

</details>


---

### `ForceTransferWeapon`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceTransferWeapon` | Integer | If true, forces the weapon to be transferred to the target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceUseAbilityOnTarget`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Items_and_Equipment.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

</details>


---

### `InterchangeMoveActPoints`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `InterchangeMoveActPoints` | Integer | If true, swaps the unit's remaining move points and action points. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JustInCaseTrample`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `JustInCaseTrample` | Integer | If set to a non-zero value, applies a trample effect as a fallback. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KnockbackDirectionIsFacingDirection`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `KnockbackDirectionIsFacingDirection` | Variable | Specifies how to alter knockback direction relative to the unit's facing: 1 (same), flip (opposite), rotate_right. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KnockbackIfCrit`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToAllDamage`](./Items_and_Equipment.md#context-addstatustoalldamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 ||
| `override_chain_knockback` | Integer | The distance in tiles the unit is knocked back if a critical hit triggers chain knockback. | 1 ||

</details>


---

### `LeaveBehindOnceEachMove`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum | Specifies the object left behind on the tile once per move. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LowGravityKnockbackBoost`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `LowGravityKnockbackBoost` | Number | The multiplier or bonus to knockback force under low gravity. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MinimumKnockbackFromAllDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MinimumKnockbackFromAllDamage` | Integer | The minimum knockback distance the unit will suffer from any damage source. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MinimumKnockbackFromPhysicalAttacks`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MinimumKnockbackFromPhysicalAttacks` | Integer | The minimum knockback distance applied when hit by a physical attack. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MotherTumorDebugForcePass`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MotherTumorDebugForcePass` | Integer | If non-zero, forces the Mother Tumor boss to pass its turn, skipping its normal action. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MoveAfterAnyAttemptedAttack`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 1 ||

</details>


---

### `MoveAwayWhenEnemyAdjacent`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 ||
| `once_per_turn` | Boolean | If true, the movement away can only trigger once per turn. | 1 ||
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 1 ||

</details>


---

### `MoveTowardsKillers`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`character_filter`](./Arrays.md#array-character_filter) | Array | Specifies which characters to consider as killers when moving towards them. | 3 ||
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 3 ||

</details>


---

### `OverrideKnockbackDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 34

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideKnockbackDamage` | Equation | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 34 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomKnockback`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 2 ||
| `min` | Integer | The minimum amount of coins that will be gained. | 2 ||

</details>


---

### `RandomKnockbackDirection`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomKnockbackDirection` | Integer | The number of random directions the target can be knocked back (e.g., 4 selects from 4 cardinal directions). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RefreshMovePointsIfHit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RefreshMovePointsIfHit` | Integer | The amount of movement points restored on hit. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveActPoints`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RemoveActPoints` | Integer | The number of action points removed from the target. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveAmbientLightEffects`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Number | The fade-out duration in seconds for ambient light effects. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveExtraDispersedTurn`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RemoveExtraDispersedTurn` | Number | If set to 1, the unit's turn order is not delayed by the 'Dispersed' status effect. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveGlobalModifiers`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array | List of global modifier names to remove upon death. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveItem`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | Specifies the item ID to remove from the source on kill. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveKnockback`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RemoveKnockback` | Integer | The number of knockback stacks removed from the received damage. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveMovePoints`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RemoveMovePoints` | Integer | The number of move points to remove from the target, preventing them from moving. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveStatus`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | The name of the status effect to remove from the source. | 32 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RemoveStatusStacks`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||

</details>


---

### `RemoveTurnsThisRound`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RemoveTurnsThisRound` | Integer | The number of turns to remove from the target's turn order this round. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReplaceBasicMove_Mutation`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ReplaceBasicMove_Mutation`](./Enums.md#enum-replacebasicmove_mutation) | Enum | Replaces the unit's basic movement with the specified mutation-based move. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RunInXTurns`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RunInXTurns` | Integer | The number of turns after which this unit will flee the battle. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RunWhenKittensDead`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RunWhenKittensDead` | Integer | If set to 1, causes the character to attempt to flee when all associated kittens are dead. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RunWhenLastPlayerCatIsCharmed`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | If true, allows the decision to run to occur mid-turn instead of at the end. | 1 ||
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum | Specifies the save key used to persist a legacy stolen cat ID. | 1 ||

</details>


---

### `SetDistanceDisplace`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SetDistanceDisplace` | Integer | The fixed distance to displace the target. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetKnockback`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SetKnockback` | Integer | The knockback distance to set for the damage instance, overriding default. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpeculativeMoveSelfCorpseOffMap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpeculativeMoveSelfCorpseOffMap` | Integer | If true, attempts to remove the character's corpse from the map, used for speculative AI targeting. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SproutsGrantMovement`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SproutsGrantMovement` | Integer | If set to 1, sprouts on the character grant additional movement (aliases to MovementUp). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatusIfDidntMove`
> Found in: *Cat Mutations, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer | The number of charge stacks applied. | 1 ||

</details>


---

### `StatusWhenStatusCompletelyRemoved`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 1 ||

</details>


---

### `StripKnockback`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StripKnockback` | Integer | If non-zero, removes all knockback effects from the unit's attacks or abilities. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SupportDieInsteadOfRun`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum | Specifies the alternative death animation to use when the support unit dies instead of running. | 1 ||
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum | Specifies the alternative dying animation to use. | 1 ||

</details>


---

### `TVBotDisableMove`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TVBotDisableMove` | Integer | If set to 1, disables the TVBot's ability to move. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBonusKnockback`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempBonusKnockback` | Integer | The number of stacks of temporary bonus knockback distance. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBonusKnockbackDamage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempBonusKnockbackDamage` | Integer | The number of stacks of temporary bonus knockback damage. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempTrampleUntilSettled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempTrampleUntilSettled` | Integer | The number of stacks of temporary Trample applied to the source, allowing movement through enemies until the source ends its turn. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Terminator2Chase`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Terminator2Chase`](./Enums.md#enum-terminator2chase) | Enum | Specifies the movement ability used by Terminator2 when chasing the target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Terminator2Run`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 10 ||
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 ||

</details>


---

### `TerminatorChase`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 122 ||

</details>


---

### `TilesMovedToCritChance`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TilesMovedToCritChance` | Integer | The number of stacks of a status that grants critical hit chance based on tiles moved. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TilesMovedToMana`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TilesMovedToMana` | Integer | The number of stacks of a status that grants mana based on tiles moved. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TilesMovedToNeighborHeal`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum | Specifies the scaling type for healing neighbors based on tiles moved (e.g., 'level'). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TilesMovedToStrength`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TilesMovedToStrength` | Integer | The number of stacks of a status that grants strength based on tiles moved. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TwisterDisplaceWithDamage`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 6 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 2 ||
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum | Specifies a prefix string; units with a matching prefix in their ID are excluded from the displacement effect. | 1 ||

</details>


---

### `TwisterFling`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 1 ||
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 1 ||

</details>


---

### `UseMoveAbilityWithAI`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 10 ||

</details>


---

### `ZeroKnockbackDamage`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ZeroKnockbackDamage` | Integer | If 1, the unit takes no damage from knockback effects. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Spawns, Summons & Familiars (50)

### `AbilityWhenBuddyDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AbilityWhenBuddyDies`](./Enums.md#enum-abilitywhenbuddydies) | Enum | Specifies the ability to cast when a nearby allied unit dies. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsBuddy`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AggroTargetIsBuddy` | Integer | If set to 1, the unit's aggro target is its buddy (linked partner). | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyPassivesToSpawnerWhileAlive`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Specifies which equipment slot is visually hidden. | 1 ||

</details>


---

### `Buddy`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 3 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 3 ||
| `reclaim_if_lost` | Boolean | If true, the buddy can be reclaimed after being lost. | 1 ||

</details>


---

### `DemonicGlyph_Summon`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Summon` | Integer | The weight for the demonic glyph of summon, or its configuration. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DieWhenSpawnerDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DieWhenSpawnerDies` | Integer | If 1, the unit dies when its spawner unit dies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisplayBuddyCatOnSpawn`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisplayBuddyCatOnSpawn` | Integer | The number of buddy cat objects to display when the unit spawns. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DropAsFamiliarOnArmorBreak`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Specifies the familiar type to drop onto the tile when this status holder's armor breaks. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DropAsFamiliarOnTookDamage`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum | Specifies the familiar type to be dropped when the unit takes damage. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EraseSpawnCoins`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `EraseSpawnCoins` | Integer | If set to 1, the unit erases spawn coins from the map on spawn. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExpireOnSpawnerTurnEnd`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExpireOnSpawnerTurnEnd` | Integer | If set to 1, this unit is removed from battle at the end of its spawner's turn. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalFamiliarDamageBoost`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalFamiliarDamageBoost` | Number | The amount of damage boost applied to all familiars globally. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalFamiliarMoveBoost`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalFamiliarMoveBoost` | Number | The amount of movement boost applied to all familiars globally. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalSpawnCharacter`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Specifies the name of a character to spawn globally. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalSpawnOnRoundEnd`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 1 ||

</details>


---

### `InheritSpawnerStats`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `InheritSpawnerStats` | Integer | If set to 1, the unit inherits the stats of its spawner. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LegacySpawnSavedCatIfExists`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`LegacySpawnSavedCatIfExists`](./Enums.md#enum-legacyspawnsavedcatifexists) | Enum | Specifies the legacy saved cat ID to spawn if it exists in the save data. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MimicSpawnerAttacks`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MimicSpawnerAttacks` | Integer | If positive, the number of attacks mimicked; if -1, mimics all attacks from spawner. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MotherTumorSpawnInCapture`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](Characters_and_Bosses.md#object-cat) | Object | Defines the behavior and form change for captured cat units. | 10 ||
| [`NonCat`](Characters_and_Bosses.md#object-noncat) | Object | Defines the behavior and form change for captured non-cat units. | 2 ||
| [`Nothing`](Characters_and_Bosses.md#object-nothing) | Object | Defines the behavior when nothing is captured, typically just an animation. | 1 ||

</details>


---

### `MultiSpawnOnDeath`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 1 ||

</details>


---

### `PopAndSpawn`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| `clone_items` | Boolean | If true, the spawned unit clones the items of the original unit. | 1 ||
| `clone_referenced_catdata` | Boolean | If true, the spawned unit is a clone of the referenced cat data, including its stats and equipment. | 1 ||
| `no_splatter` | Boolean | If true, prevents the blood splatter visual effect from appearing when the object spawns or is popped. | 1 ||

</details>


---

### `SharePickupsWithSpawner`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SharePickupsWithSpawner` | Integer | If set to 1, pickups collected by this unit are also given to its spawner. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnBearTrap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnBearTrap` | Integer | If non-zero, spawns a bear trap on the tile. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnBearTrapIfHitKills`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnBearTrapIfHitKills` | Integer | If non-zero, spawns a bear trap at the target's location upon a killing blow. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnCatCloneOnCorpsePopped`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnCatCloneOnCorpsePopped` | Integer | The number of cat clones spawned when a corpse is popped (destroyed) by the unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnCatCopyWhenDowned`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum | A tag that prevents chaining of spawns from the same source. | 2 ||

</details>


---

### `SpawnCreep`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnCreep` | Integer | If set to 1, spawns a creep tile under the target. | 18 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnCreepOnHitKnockback`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnCreepOnHitKnockback` | Integer | If set to 1, spawns creep on the tile where a hit knocks back an enemy. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnCustomTrap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum | Specifies the name of a custom trap blueprint to spawn at the target location. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnExtraThingsOnBattleStart`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 1 ||

</details>


---

### `SpawnFlames`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SpawnFlames`](./Arrays.md#array-spawnflames) | Array | An array containing the number of flame tiles to spawn and the chance per tile. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnItemLinkedFamiliar`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| `break_on_pop_only` | Boolean | If true, the linked familiar spawn only breaks when the item is popped. | 2 ||

</details>


---

### `SpawnNearEnemies`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnNearEnemies` | Integer | The number of units to spawn near each enemy at the start of battle. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnNeutralWebTrapOnMiss`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnNeutralWebTrapOnMiss` | Integer | The number of neutral web traps spawned on the tile if the attack misses. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnOnDeath`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 79

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 3 ||
| [`obj`](./Arrays.md#array-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 3 ||
| [`additional_statuses`](Characters_and_Bosses.md#object-additional_statuses) | Object | Additional status effects applied to the spawned unit on death. | 1 ||

</details>


---

### `SpawnOnDowned`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum | Specifies the character or object spawned when the unit is downed. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnRandomPickupsOnTaggedUnitKilled`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 ||

</details>


---

### `SpawnRock`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SpawnRock`](./Arrays.md#array-spawnrock) | Array / Integer | The number of rocks to spawn, or an array with stacks and probability. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnThingIfHitKills`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SpawnThingIfHitKills`](./Enums.md#enum-spawnthingifhitkills) | Enum | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 20 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnTilePuddleOnBattleStart`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](./Enums.md#enum-tile) | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 26 ||
| `max_radius` | Number | The maximum radius of the spawned puddle or volcano in tiles. | 1 ||
| [`min_radius`](./Enums.md#enum-min_radius) | Number | The minimum radius of the spawned puddle or volcano in tiles. | 1 ||

</details>


---

### `SpawnVolcanoOnBattleStart`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| `max_radius` | Number | The maximum radius of the spawned puddle or volcano in tiles. | 2 ||
| [`min_radius`](./Enums.md#enum-min_radius) | Number | The minimum radius of the spawned puddle or volcano in tiles. | 2 ||
| [`puddle_tile`](./Arrays.md#array-puddle_tile) | Array | An array specifying the tile types to use for the puddle or volcano. | 2 ||
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 1 ||

</details>


---

### `SpawnWebTrap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnWebTrap` | Integer | The number of web traps to spawn on the target tile. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpawnerCatDataReference`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnerCatDataReference` | Integer | A reference ID pointing to the spawner cat's data, used by minions to link back to their spawner. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StatusAllCharactersOnSpawn`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 ||

</details>


---

### `StatusOnSpawnIn`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 1 ||
| `SetHealth` | Integer | Sets the target's health to a specific flat value or percentage. | 1 ||

</details>


---

### `SyncFormsWithBuddy`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum | Specifies an alternative form to use when there is no buddy. | 1 ||

</details>


---

### `T3HitlerSpawningPhase`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array | List of spell use groups that the spawning phase can use. | 1 ||

</details>


---

### `T3HitlerTriggerInitialSpawns`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `T3HitlerTriggerInitialSpawns` | Integer | If non-zero, triggers the initial spawn sequence for the T3 Hitler boss. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TakeWeaponFromSpawner`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TakeWeaponFromSpawner` | Integer | If set to 1, the minion inherits the weapon from its spawner. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TossTargetIsBuddy`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TossTargetIsBuddy` | Integer | If set to 1, the toss target is the unit's buddy. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Loot, Rewards & Economy (34)

### `AddLootMultiplier`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddLootMultiplier` | Number | The multiplier added to loot drops from this unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ArmorPickup`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the minimum and maximum animation frame for the health pickup. | 3 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||

</details>


---

### `AwardCoinsOnDeath`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AwardCoinsOnDeath` | Integer | The amount of coins awarded to the killer when this unit dies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BirdRewards`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_rewards`](Characters_and_Bosses.md#object-ally_rewards) | Object | Defines the rewards granted to the ally when the BirdRewards passive triggers. | 18 ||
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 5 ||

</details>


---

### `ChaosHeadDropIn`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`new_music`](./Enums.md#enum-new_music) | Enum | Specifies the music track to play during the boss's head drop-in animation. | 1 ||

</details>


---

### `CoinPickup`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CoinPickup` | Integer | The amount of coins awarded when this pickup is collected. | 20 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CoinTossBounce`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CoinTossBounce` | Equation | Specifies the ability triggered when the coin lands on its edge after a bounce. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CollectsPickups`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 34

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CollectsPickups` | Integer | If set to 1 or greater, the unit collects pickups (e.g., items) on contact. | 34 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CollectsPickupsWithAltEffects`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 ||
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 ||
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 ||
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 ||
| `CurrentWeaponAddPoison` | Integer | The number of poison stacks added to the target's current weapon; an integer value applies that many stacks. | 1 ||
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 ||

</details>


---

### `DemonicGlyphStealer`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyphStealer` | Integer | If 1, the unit can steal demonic glyphs from other units. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleLoot`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoubleLoot`](Engine_StatusAndPassiveKeys.md#object-doubleloot) | Integer / Object | The multiplier for loot drops, where 1 or 2 doubles the loot. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DropSoulJarOnDeath`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum | Specifies the type of soul jar to be dropped when the unit dies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FindItem`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FindItem`](./Enums.md#enum-finditem) | Enum | The name of the specific item to find and add to the source's inventory. | 5 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ForceCollectsPickups`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceCollectsPickups` | Integer | If true, the unit automatically collects nearby pickups. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainCoins`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer | The amount of coins gained, or a [min, max] range. | 20 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainCoinsRange`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 4 ||
| `min` | Integer | The minimum amount of coins that will be gained. | 4 ||

</details>


---

### `HealthPickup`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the minimum and maximum animation frame for the health pickup. | 15 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 15 ||
| `stored_food_value` | Integer | The amount of food value stored in this pickup. | 15 ||
| `anything_eats` | Boolean | If true, any unit can consume this health pickup. | 4 ||
| `force_frame` | Integer | Forces the health pickup to use a specific animation frame. | 1 ||

</details>


---

### `Lifesteal`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManaPickup`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array | Specifies the minimum and maximum animation frame for the health pickup. | 3 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||

</details>


---

### `ManaSteal`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ManaSteal` | Integer | The amount of mana stolen (negative values may drain instead). | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManaStealToHealth`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ManaStealToHealth` | Integer | The amount of mana stolen and converted to health (negative values may drain health). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MegaDinoDropController`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum | Specifies the ability triggered when the head drops down. | 1 ||
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum | Specifies the ability triggered when the legs leave the body. | 1 ||
| [`leg_return`](./Enums.md#enum-leg_return) | Enum | Specifies the ability triggered when the legs return to the body. | 1 ||
| `stable_legs` | Integer | The number of legs that must be stable for the head to drop. | 1 ||

</details>


---

### `ModularPickup`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleanse`](Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 ||
| [`sound_event`](./Enums.md#enum-sound_event) | Enum | Specifies the sound event to play when the pickup is used. | 1 ||

</details>


---

### `MultiplyCoinsOnBattleStart`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MultiplyCoinsOnBattleStart` | Integer | The multiplier applied to the unit's coin count at the start of battle. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnGainCoins`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnGainCoins` | Integer | If set to 1, restores a charge when coins are gained. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScatterCoins`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_SourceAbilityHasTag`](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Else`](./Abilities_and_Spells.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stackable` | Boolean | If true, the scatter coins effect can stack with multiple applications. | 2 ||
| [`stacks`](./Math_Equations.md) | Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||

</details>


---

### `ScatterHeldCoin`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ScatterHeldCoin`](./Arrays.md#array-scatterheldcoin) | Array / Integer | The number of coins scattered, with an optional probability as a second element. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScatterRandomPickups`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ScatterRandomPickups` | Integer | The number of random pickups scattered around the target's location. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealDemonicGlyph`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StealDemonicGlyph` | Integer | The number of Demonic Glyphs stolen from the target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealEquipment`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum | Specifies the type of equipment to steal (e.g., "any") from the target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StealTurn` | Integer | The number of turns stolen from the target to grant to the attacker. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealthCritChance`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StealthCritChance` | Integer | The percentage chance to critically hit while stealthed. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StealthUntilBasicAttack`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StealthUntilBasicAttack` | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WhitelistPickupType`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`WhitelistPickupType`](./Enums.md#enum-whitelistpickuptype) | Enum | Specifies the type of pickup that this unit is allowed to collect. | 2 ||

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

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head`](./Enums.md#enum-head) | Enum / Number | The catalog ID for the cat's head part. | 784 ||
| `texture` | Integer | The catalog ID for the cat's texture. | 422 ||
| [`palette`](./Enums.md#enum-palette) | Enum / Integer | Specifies the color palette index for the ability's visuals. | 420 ||
| [`mouth`](./Enums.md#enum-mouth) | Number | The catalog ID for the cat's mouth part. | 386 ||
| `tail` | Integer | The catalog ID for the cat's tail part. | 362 ||
| `arm2` | Number | The catalog ID for the cat's second arm part. | 358 ||
| `arm1` | Number | The catalog ID for the cat's first arm part. | 354 ||
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 348 ||
| [`body`](./Arrays.md#array-body) | Number | The catalog ID for the cat's body part. | 346 ||
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 344 ||
| `ear1` | Integer | The catalog ID for the cat's first ear part. | 10 ||
| `ear2` | Integer | The catalog ID for the cat's second ear part. | 9 ||
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 1 ||
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 1 ||
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 1 ||
| `eyebrow2` | Integer | The catalog ID for the cat's second eyebrow part. | 1 ||

</details>


---

### `ChanceToFormChangeOnAbilityDamage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 1 ||

</details>


---

### `ChaosBossFormChange`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ChaosBossFormChange` | Integer | If set to a non-zero number, triggers a chaos boss form change. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChaosBossFormChangeGuide`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | An array of piece names that are considered actively part of the current form. | 1 ||
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | An array of piece names that are considered passively part of the current form. | 1 ||
| `passives_health_threshold` | Integer | The health percentage threshold at which the boss's passive abilities change. | 1 ||

</details>


---

### `DurabilityTransform`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array | An array specifying a [durability, item] pair to transform to when durability equals a specific value. | 11 ||
| [`ge`](./Arrays.md#array-ge) | Array | An array specifying a [durability, item] pair to transform to when durability is greater than or equal to a specific value. | 4 ||

</details>


---

### `FormChange`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`ApplyToSource`](./Abilities_and_Spells.md#context-applytosource), [`RandomStatusFromPool`](./Abilities_and_Spells.md#context-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 75 ||
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

</details>


---

### `FormChangeDuringWeatherElement`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 2 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||

</details>


---

### `FormChangeHealthThreshold`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum | The form to change to when health is above the threshold. | 3 ||
| [`form_below`](./Enums.md#enum-form_below) | Enum | The form to change to when health is below the threshold. | 3 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 3 ||
| `count_shield` | Boolean | If true, shields count towards the health threshold calculation. | 1 ||

</details>


---

### `FormChangeOffMap`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum | Specifies the form name to use when the unit is off the map. | 8 ||
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum | Specifies the form name to use when the unit returns to the map. | 8 ||

</details>


---

### `FormChangeOnElementInfluence`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum / Integer | Specifies the name of the form the unit changes into. | 9 ||
| [`exclude`](./Enums.md#enum-exclude) | Enum | Specifies an element or effect that does not trigger the form change. | 5 ||
| [`particle`](./Enums.md#enum-particle) | Enum | Specifies the particle effect displayed. | 5 ||
| [`sfx`](./Enums.md#enum-sfx) | Enum | Specifies the sound effect to play when the form change triggers. | 5 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||

</details>


---

### `FormChangeWhenBuddyDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FormChangeWhenBuddyDies`](./Enums.md#enum-formchangewhenbuddydies) | Enum | Specifies the form name the unit changes into when its buddy dies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FormChangeWhileHasStatus`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 35 ||
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum | Specifies a form that the unit must not be in for the status-triggered form change to occur. | 30 ||
| [`form_has`](./Enums.md#enum-form_has) | Enum | Specifies a form that the unit must be in for the status-triggered form change to occur. | 25 ||

</details>


---

### `FormChangeWhilePrimingAbility`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum | Specifies the form name to use when the unit is not priming an ability. | 6 ||
| [`priming`](./Enums.md#enum-priming) | Enum | Specifies the form name to use while the unit is priming an ability. | 6 ||

</details>


---

### `FormChanger`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 106

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 928 ||
| [`Default`](Characters_and_Bosses.md#object-default) | Enum / Object | The default form configuration for a unit, containing its standard stats and abilities. | 199 ||
| [`default`](Characters_and_Bosses.md#object-default) | Enum / Object | The default configuration or value used when no specific override is provided. | 199 ||
| [`Colorless`](Engine_LogicKeys.md#object-colorless) | Object | Specifies the 'Colorless' form within FormChanger, used for boss dialogue. | 140 ||
| [`Druid`](Engine_LogicKeys.md#object-druid) | Object | Specifies the 'Druid' form within FormChanger, used for boss dialogue. | 80 ||
| [`Fighter`](Engine_LogicKeys.md#object-fighter) | Object | Specifies the 'Fighter' form within FormChanger, used for boss dialogue. | 80 ||
| [`Thief`](Engine_LogicKeys.md#object-thief) | Object | Form identifier for the Thief boss type. | 76 ||
| [`Tank`](Engine_LogicKeys.md#object-tank) | Object | Form identifier for the Tank boss type, used for dialogue references. | 74 ||
| [`Butcher`](Engine_LogicKeys.md#object-butcher) | Object | Specifies the 'Butcher' form within FormChanger, used for boss dialogue. | 72 ||
| [`Necromancer`](Engine_LogicKeys.md#object-necromancer) | Object | Defines a list of quotes for the Necromancer class. | 72 ||
| [`Mage`](Engine_LogicKeys.md#object-mage) | Object | Defines a list of quotes for the Mage class. | 70 ||
| [`Tinkerer`](Engine_LogicKeys.md#object-tinkerer) | Object | Form identifier for the Tinkerer boss type. | 70 ||
| [`Hunter`](Engine_LogicKeys.md#object-hunter) | Object | Defines a list of quotes for the Hunter class (vs boss, embark, return early). | 68 ||
| [`Monk`](Engine_LogicKeys.md#object-monk) | Object | Defines a list of quotes for the Monk class. | 66 ||
| [`Psychic`](Engine_LogicKeys.md#object-psychic) | Object | Form identifier for the Psychic boss type, used for dialogue references. | 66 ||
| [`Medic`](Engine_LogicKeys.md#object-medic) | Object | Defines a list of quotes for the Medic class. | 58 ||
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 26 ||
| [`Normal`](Characters_and_Bosses.md#object-normal) | Integer / Object | The normal form configuration, used as a baseline state for shape-shifting units. | 24 ||
| [`Cultist`](Characters_and_Bosses.md#object-cultist) | Object | Defines the 'Cultist' form, a basic melee form with its own name and tooltip. | 11 ||
| [`Nuke`](Characters_and_Bosses.md#object-nuke) | Object | Defines a nuke form with no attack or movement options. | 10 ||
| [`Rage`](Characters_and_Bosses.md#object-rage) | Object | The rage form configuration, applied when the unit enters an enraged state. | 10 ||
| [`Unlit`](Characters_and_Bosses.md#object-unlit) | Object | Form state for an unlit candle, muting demonic glyph display. | 9 ||
| [`CaveMan`](Characters_and_Bosses.md#object-caveman) | Object | Defines the 'CaveMan' form of a CavePerson enemy, including its animation, attack, and passives. | 7 ||
| [`Fire`](Characters_and_Bosses.md#object-fire) | Integer / Object | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 6 ||
| [`initial_form`](./Enums.md#enum-initial_form) | Enum / Integer | Specifies the starting form name for a unit with FormChanger. | 6 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 6 ||
| [`Angry`](Characters_and_Bosses.md#object-angry) | Object | Defines the 'Angry' form, an enraged state with its own AI. | 5 ||
| [`HasCat`](Characters_and_Bosses.md#object-hascat) | Object | The form configuration applied when the unit is holding or has swallowed a cat. | 5 ||
| [`Water`](Characters_and_Bosses.md#object-water) | Object | Form state for water element, applying a puddle or movement bonus. | 5 ||
| [`Flush`](Characters_and_Bosses.md#object-flush) | Object | Defines a form that executes a sequence of actions (FlushX, side switch, form switch) and has a spell with a localized name. | 4 ||
| [`hot`](Characters_and_Bosses.md#object-hot) | Object | The form configuration applied when the unit is in a hot state, granting fire element. | 4 ||
| [`OffMap`](Characters_and_Bosses.md#object-offmap) | Object | The form configuration applied when the unit is off the battlefield map. | 4 ||
| [`passive`](Characters_and_Bosses.md#object-passive) | Object | Defines the passive form, where the unit does nothing (uses DoNothing attack) and is inactive. | 4 ||
| [`AllAlive`](Characters_and_Bosses.md#object-allalive) | Object | The form configuration applied when all family members are alive. | 3 ||
| [`CaveBaby`](Characters_and_Bosses.md#object-cavebaby) | Object | Defines the 'CaveBaby' form of a CavePerson enemy, with reduced health and baby attack. | 3 ||
| [`Down`](Characters_and_Bosses.md#object-down) | Object | The form configuration applied when the unit is in a knocked-down or prone state. | 3 ||
| [`Full`](Characters_and_Bosses.md#object-full) | Object | The form configuration applied when the unit is in a full state. | 3 ||
| [`OneAlive`](Characters_and_Bosses.md#object-onealive) | Object | The form configuration applied when only one family member remains alive. | 3 ||
| [`Open`](Characters_and_Bosses.md#object-open) | Object | Defines an open form with increased movement and a specific attack. | 3 ||
| [`TwoAlive`](Characters_and_Bosses.md#object-twoalive) | Object | A form that activates when two specific units are alive, granting the contained passives and abilities. | 3 ||
| [`Up`](Characters_and_Bosses.md#object-up) | Object | Defines the 'Up' form, including its animation, AI behavior, and passives such as UpTireBehavior. | 3 ||
| [`active`](Characters_and_Bosses.md#object-active) | Object | Defines the active form, containing passives and abilities that are active while in this form. | 2 ||
| [`Big`](Characters_and_Bosses.md#object-big) | Object | Defines the 'Big' form, including its animation, attack, passives, and positional data. | 2 ||
| [`CaveManSpear`](Characters_and_Bosses.md#object-cavemanspear) | Object | Defines the 'CaveManSpear' form of a CavePerson enemy, with a spear attack and corresponding animation. | 2 ||
| [`Explosive`](Characters_and_Bosses.md#object-explosive) | Enum / Object | Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives. | 2 ||
| [`Holding`](Characters_and_Bosses.md#object-holding) | Object | Defines the 'Holding' form, used when the unit is holding an object, with associated movement and form change behaviors. | 2 ||
| [`Holy`](Characters_and_Bosses.md#object-holy) | Enum / Object | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 2 ||
| [`LastHit`](Characters_and_Bosses.md#object-lasthit) | Object | Defines a form that grants 2 dispersed bonus turns after the last hit. | 2 ||
| [`NeutronStar`](Characters_and_Bosses.md#object-neutronstar) | Object | Defines the neutron star form with custom graphics and a random pattern AI (rumble or explode). | 2 ||
| [`NotPriming`](Characters_and_Bosses.md#object-notpriming) | Object | Defines the 'NotPriming' form, which allows the unit to take main turns and grants bonus turns. | 2 ||
| [`Priming`](Characters_and_Bosses.md#object-priming) | Object | Defines the 'Priming' form, where the unit does not take main turns but gains bonus turns at round end. | 2 ||
| [`Small`](Characters_and_Bosses.md#object-small) | Object | Defines the 'Small' form, typically used for smaller size variants, with its own attack and animation. | 2 ||
| [`SquirrelForm`](Characters_and_Bosses.md#object-squirrelform) | Object | Defines the 'SquirrelForm', a transformation used by units like DeathMetal, granting melee attack and speed bonuses. | 2 ||
| [`Turtled`](Characters_and_Bosses.md#object-turtled) | Object | Defines the 'Turtled' form, a defensive state where the unit cannot attack or move. | 2 ||
| `uifloaters_offset` | Number | The vertical offset for UI floaters (e.g., damage numbers) above the unit. | 2 ||
| [`Zealot`](Characters_and_Bosses.md#object-zealot) | Object | Form state for the zealot variant of a cultist, with a stabbing attack. | 2 ||
| [`Alert`](Characters_and_Bosses.md#object-alert) | Object | Defines the 'Alert' form, an alerted state with a pattern brain AI. | 1 ||
| [`Attacker`](Characters_and_Bosses.md#object-attacker) | Object | Defines the 'Attacker' form, focusing on offensive actions like attacking and charging. | 1 ||
| [`BellyFull`](Characters_and_Bosses.md#object-bellyfull) | Object | Defines the 'BellyFull' form, used when the unit has the Consuming status, with appropriate animation. | 1 ||
| [`BigHolding`](Characters_and_Bosses.md#object-bigholding) | Object | Defines the 'BigHolding' form, a larger variant while holding an object, triggered by the Consuming status. | 1 ||
| [`BigHoldingCat`](Characters_and_Bosses.md#object-bigholdingcat) | Object | Defines the 'BigHoldingCat' form, a cat-sized variant of the holding form while Consuming. | 1 ||
| [`Bishop`](Characters_and_Bosses.md#object-bishop) | Object | Defines the 'Bishop' form for Cultist enemies, with its own attack (BBXLightning) and animation. | 1 ||
| [`BlackHole`](Characters_and_Bosses.md#object-blackhole) | Object | Defines the 'BlackHole' form, a variant of NeutronStar with its own animation and name. | 1 ||
| [`Bomb`](Characters_and_Bosses.md#object-bomb) | Object | Defines the 'Bomb' form, an explosive state that triggers an ability on death. | 1 ||
| [`Boris`](Characters_and_Bosses.md#object-boris) | Enum / Object | Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives. | 1 ||
| [`Bully`](Characters_and_Bosses.md#object-bully) | Object | Defines the 'Bully' form, which allows the unit to take turns and enables its passives. | 1 ||
| [`CaveWoman`](Characters_and_Bosses.md#object-cavewoman) | Object | Defines the 'CaveWoman' form of a CavePerson enemy, with kick attack and higher health. | 1 ||
| [`CaveWomanHasCat`](Characters_and_Bosses.md#object-cavewomanhascat) | Object | Defines the 'CaveWomanHasCat' form, a variant of CaveWoman that attacks with a cat slap. | 1 ||
| [`Charging`](Characters_and_Bosses.md#object-charging) | Object | Defines the 'Charging' form, a wind-up state for a powerful attack. | 1 ||
| [`Close`](Characters_and_Bosses.md#object-close) | Object | Defines the 'Close' form, which triggers GSOpen ability upon reaction. | 1 ||
| [`Damaged`](Characters_and_Bosses.md#object-damaged) | Object | Defines the 'Damaged' form, an injured state with a specific AI pattern to drink and attack. | 1 ||
| [`Default_Ceiling`](Characters_and_Bosses.md#object-default_ceiling) | Object | Defines the 'Default_Ceiling' form for SpiderQueen, with AI pattern to spawn spiders. | 1 ||
| [`Default_Ground`](Characters_and_Bosses.md#object-default_ground) | Object | Defines the 'Default_Ground' form for SpiderQueen, with AI pattern to web and attack. | 1 ||
| [`DesireMech`](Characters_and_Bosses.md#object-desiremech) | Object | Defines the 'DesireMech' form, a mech suit form with its own AI pattern. | 1 ||
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 1 ||
| [`Drunker`](Characters_and_Bosses.md#object-drunker) | Object | Defines the 'Drunker' form, a drunken state with altered animation. | 1 ||
| [`DualSword`](Characters_and_Bosses.md#object-dualsword) | Object | Defines the 'DualSword' form of TheDestroyer, increasing move speed and using a dual sword attack. | 1 ||
| [`DualSword_Primed`](Characters_and_Bosses.md#object-dualsword_primed) | Object | Defines the 'DualSword_Primed' form, a powered-up dual sword state with holy animation. | 1 ||
| [`Dumb`](Characters_and_Bosses.md#object-dumb) | Integer / Object | Defines the 'Dumb' form, which can be either a numeric value or an object with passives that disable spells and turn off TV. | 1 ||
| [`Empty`](Characters_and_Bosses.md#object-empty) | Object | Defines the 'Empty' form, typically indicating a state with no content (e.g., empty stomach). | 1 ||
| [`Explody`](Characters_and_Bosses.md#object-explody) | Object | Defines the 'Explody' form, an explosive state that uses ToxExplode attack and cannot move. | 1 ||
| [`FightPhase`](Characters_and_Bosses.md#object-fightphase) | Object | Defines the 'FightPhase' form, a combat form with float move and shoot attack, taking turns. | 1 ||
| [`FireFull`](Characters_and_Bosses.md#object-firefull) | Integer / Object | Defines the 'FireFull' form, a fully charged fire state with its own animation and visual combo. | 1 ||
| [`Flop`](Characters_and_Bosses.md#object-flop) | Object | Defines the initial flopped down state, using animation suffix 'Down' and a pattern AI that requires 4 wiggles to exit. | 1 ||
| [`Flop2`](Characters_and_Bosses.md#object-flop2) | Object | Defines a subsequent flopped down state triggered on hit, with variable wiggles (2-6) to recover. | 1 ||
| [`FlushBubs`](Characters_and_Bosses.md#object-flushbubs) | Object | Defines a form granting an immediate ability reaction for Cerberubs shotgun. | 1 ||
| [`FlushHost`](Characters_and_Bosses.md#object-flushhost) | Object | Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage. | 1 ||
| [`FlushNettle`](Characters_and_Bosses.md#object-flushnettle) | Object | Defines a form that gains thorns and kinetic spikes after an enemy casts a spell. | 1 ||
| [`Grappling`](Characters_and_Bosses.md#object-grappling) | Object | Defines a grappling form with a specific animation suffix and exit animations. | 1 ||
| [`Grown`](Characters_and_Bosses.md#object-grown) | Object | Defines the grown form with a custom attack, name, UI floater offset, and a health weak threshold. | 1 ||
| [`GuaranteedJackpot`](Characters_and_Bosses.md#object-guaranteedjackpot) | Object | Defines a form that guarantees a jackpot coin result from slot machine rolls. | 1 ||
| [`Guarding`](Characters_and_Bosses.md#object-guarding) | Object | Defines a guarding form with a high brace passive. | 1 ||
| [`HalfDead`](Characters_and_Bosses.md#object-halfdead) | Object | Defines the half-dead form with reduced movement and a dash attack. | 1 ||
| [`HasDeadCat`](Characters_and_Bosses.md#object-hasdeadcat) | Object | Defines a form when Lenny's cat is dead, with a slap attack and conditional form change while the status is active. | 1 ||
| [`HasRock`](Characters_and_Bosses.md#object-hasrock) | Object | Defines a form where the unit has a rock, with a bash attack. | 1 ||
| [`Headless`](Characters_and_Bosses.md#object-headless) | Object | Defines a headless form with increased movement. | 1 ||
| [`Hint_CrackedVisuals`](Characters_and_Bosses.md#object-hint_crackedvisuals) | Object | Defines a visual state with cracked animation suffix. | 1 ||
| [`Hint_CrackedVisuals2`](Characters_and_Bosses.md#object-hint_crackedvisuals2) | Object | Defines a visual state with charging cracked animation. | 1 ||
| [`Hint_CrackedVisuals3`](Characters_and_Bosses.md#object-hint_crackedvisuals3) | Object | Defines a visual state with swallowed cracked animation. | 1 ||
| [`HumanDead`](Characters_and_Bosses.md#object-humandead) | Object | Defines a form when the human half is dead, with a spin attack and custom tooltip. | 1 ||
| [`InitialPhase`](Characters_and_Bosses.md#object-initialphase) | Object | Defines the initial phase form with a float move, shoot attack, and the ability to take turns. | 1 ||
| [`Insane_Ceiling`](Characters_and_Bosses.md#object-insane_ceiling) | Object | Defines the insane ceiling form with pattern AI and animation suffix. | 1 ||
| [`Insane_Ground`](Characters_and_Bosses.md#object-insane_ground) | Object | Defines the insane ground form with pattern AI and animation suffix. | 1 ||
| [`Johnny`](Characters_and_Bosses.md#object-johnny) | Object | Defines a form that executes a mega blast, side switch, and form switch in sequence. | 1 ||
| [`JohnnyBubs`](Characters_and_Bosses.md#object-johnnybubs) | Object | Defines a form granting an immediate ability reaction for Cerberubs shotgun. | 1 ||
| [`JohnnyHost`](Characters_and_Bosses.md#object-johnnyhost) | Object | Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage. | 1 ||
| [`JohnnyNettle`](Characters_and_Bosses.md#object-johnnynettle) | Object | Defines a form that gains thorns and kinetic spikes after an enemy casts a spell. | 1 ||
| [`Joystick`](Characters_and_Bosses.md#object-joystick) | Object | Defines a form with joystick animation and an immediate ability reaction (fumble even/odd). | 1 ||
| [`Lifted`](Characters_and_Bosses.md#object-lifted) | Object | Defines a lifted form with no attack or movement options. | 1 ||
| [`Lit`](Characters_and_Bosses.md#object-lit) | Object | Defines a lit form that changes when wind element influence is applied. | 1 ||
| [`Mounted`](Characters_and_Bosses.md#object-mounted) | Object | Defines a mounted form with 'Cat' animation suffix. | 1 ||
| [`MouthFull`](Characters_and_Bosses.md#object-mouthfull) | Object | Defines a form with mouth full animation that changes while the Consuming status is active. | 1 ||
| [`Mutant`](Characters_and_Bosses.md#object-mutant) | Integer / Object | As an object, defines the mutant form with reduced move speed and custom name. As an integer, defines spawn weight. | 1 ||
| `NoDeathRattle` | Object | Defines a form that suppresses death rattle and triggers a heart attack when a buddy dies. | 1 ||
| [`NoEyes`](Characters_and_Bosses.md#object-noeyes) | Object | Defines a form with no eyes animation. | 1 ||
| [`NormalFull`](Characters_and_Bosses.md#object-normalfull) | Integer / Object | As an object, defines the normal full form with a spit attack and conditional form change. As an integer, specifies alt graphics index. | 1 ||
| [`NoStick`](Characters_and_Bosses.md#object-nostick) | Object | Defines a form without a stick, using a jab attack with pattern AI. | 1 ||
| [`Obey`](Characters_and_Bosses.md#object-obey) | Integer / Object | As an object, defines an obey form that disables attacks and reacts with TV off. As an integer, defines a value (e.g., weight or count). | 1 ||
| [`Off`](Characters_and_Bosses.md#object-off) | Object | Defines an off form with a 'Off' animation suffix. | 1 ||
| [`OffScreen`](Characters_and_Bosses.md#object-offscreen) | Object | Defines an off-screen form that does not take turns and drops in chaos heads. | 1 ||
| [`OneEye`](Characters_and_Bosses.md#object-oneeye) | Object | Defines a form with one eye that triggers an ability at 40% health threshold. | 1 ||
| [`OpenCat`](Characters_and_Bosses.md#object-opencat) | Object | Defines an open cat form that changes when the Consuming status is active. | 1 ||
| [`Out`](Characters_and_Bosses.md#object-out) | Object | Defines a form that is 'out' with a ground flopper movement passive. | 1 ||
| [`Possessing`](Characters_and_Bosses.md#object-possessing) | Object | Form state when the unit is possessing another entity. | 1 ||
| [`Primed`](Characters_and_Bosses.md#object-primed) | Object | Form state representing the unit being primed, with specific attack and AI behavior. | 1 ||
| [`Pulp2`](Characters_and_Bosses.md#object-pulp2) | Object | Form state for the second stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp3`](Characters_and_Bosses.md#object-pulp3) | Object | Form state for the third stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp4`](Characters_and_Bosses.md#object-pulp4) | Object | Form state for the fourth stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp5`](Characters_and_Bosses.md#object-pulp5) | Object | Form state for the fifth stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp6`](Characters_and_Bosses.md#object-pulp6) | Object | Form state for the sixth stage of pulping, with no attacks or movement. | 1 ||
| [`Pulp7`](Characters_and_Bosses.md#object-pulp7) | Object | Form state for the seventh stage of pulping, with no attacks or movement. | 1 ||
| [`Rain`](Characters_and_Bosses.md#object-rain) | Object | Defines the rain weather effect with associated particle, sound, and rendering settings. | 1 ||
| [`Sitting`](Characters_and_Bosses.md#object-sitting) | Object | Form state where the unit is sitting, with no movement or attack. | 1 ||
| [`SmallHolding`](Characters_and_Bosses.md#object-smallholding) | Object | Form state when the unit is holding a small object, triggering a form change while consuming. | 1 ||
| [`SmallHoldingCat`](Characters_and_Bosses.md#object-smallholdingcat) | Object | Form state when the unit is holding a cat, triggering a form change while consuming. | 1 ||
| [`SpawningPhase`](Characters_and_Bosses.md#object-spawningphase) | Object | Form state for the spawning phase, where the unit is immobile and cannot take turns. | 1 ||
| [`Standing`](Characters_and_Bosses.md#object-standing) | Object | Form state where the unit is standing, with default movement and attack. | 1 ||
| [`Standing2`](Characters_and_Bosses.md#object-standing2) | Object | Form state where the unit is standing with a jumping movement ability. | 1 ||
| [`Start_Ceiling`](Characters_and_Bosses.md#object-start_ceiling) | Object | Form state for starting on the ceiling, with a form change trigger when entering the map. | 1 ||
| [`Stop`](Characters_and_Bosses.md#object-stop) | Integer / Object | If an integer, the number of turns the unit is stopped. If an object, the form configuration for the stopped state. | 1 ||
| [`SwordAndShield`](Characters_and_Bosses.md#object-swordandshield) | Object | Form state with sword and shield, using the DestroyerAttack ability. | 1 ||
| [`SwordAndShield_Primed`](Characters_and_Bosses.md#object-swordandshield_primed) | Object | Primed form state of SwordAndShield with holy animation and no final boss shield. | 1 ||
| `sync_brain_patterns` | Boolean | If true, synchronizes brain patterns across form changes. | 1 ||
| [`Tar`](Characters_and_Bosses.md#object-tar) | Integer / Object | If an integer, the number of tar stacks. If an object, the form state for the tar-covered unit. | 1 ||
| [`TarFull`](Characters_and_Bosses.md#object-tarfull) | Integer / Object | If an integer, the number of full tar stacks. If an object, the form state for the fully tar-covered unit. | 1 ||
| [`Throb`](Characters_and_Bosses.md#object-throb) | Object | Form state for the Chaos unit's throb behavior, with a spread pattern. | 1 ||
| [`ThrobBubs`](Characters_and_Bosses.md#object-throbbubs) | Object | Form state for Chaos unit throb that reacts with a shotgun attack. | 1 ||
| [`ThrobHost`](Characters_and_Bosses.md#object-throbhost) | Object | Form state for Chaos unit acting as host, reflecting projectiles. | 1 ||
| [`ThrobNettle`](Characters_and_Bosses.md#object-throbnettle) | Object | Form state for Chaos unit with thorns and kinetic spikes that stack after enemy spells. | 1 ||
| [`Transformed`](Characters_and_Bosses.md#object-transformed) | Object | Form state after transformation, ending the turn on form switch. | 1 ||
| [`TwoEyes`](Characters_and_Bosses.md#object-twoeyes) | Object | Form state with two eyes, triggering ability at a health threshold. | 1 ||
| `Unmounted` | Object | Form state when the unit is unmounted from its mech suit, with no additional properties. | 1 ||
| [`Unwashed`](Characters_and_Bosses.md#object-unwashed) | Object | Form state for the unwashed version of Johnny, with its own AI pattern. | 1 ||
| [`Washed`](Characters_and_Bosses.md#object-washed) | Object | Form state for the washed version of Johnny, with a blast attack. | 1 ||
| [`Washer`](Characters_and_Bosses.md#object-washer) | Object | Form state for the washer variant of a cultist, with basic melee attack. | 1 ||
| [`WereMan`](Characters_and_Bosses.md#object-wereman) | Object | Form state for the were-man transformation, with fury swipe attack and sabertooth faction. | 1 ||
| [`ZealotBomb`](Characters_and_Bosses.md#object-zealotbomb) | Object | Form state for the bomb zealot variant, with an explosion attack. | 1 ||

</details>


---

### `ItemAuxTransform`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array | An array specifying a [aux value, item] pair to transform to when the aux value is less than or equal to a specific value. | 6 ||
| [`ge`](./Arrays.md#array-ge) | Array | An array specifying a [durability, item] pair to transform to when durability is greater than or equal to a specific value. | 2 ||
| [`lt`](./Arrays.md#array-lt) | Array | An array specifying a [aux value, item] pair to transform to when the aux value is strictly less than a specific value. | 1 ||

</details>


---

### `PreventDeathTransforms`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PreventDeathTransforms` | Integer | Number of death transforms prevented for non-boss characters. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SupportFormChangeInsteadOfRun`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `wait_till_turn` | Boolean | If true, the form change will not occur until the unit's next turn. | 1 ||

</details>


---

### `SwimmingFormChange`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum | Determines the form to change into when entering water. | 1 ||
| [`form_out`](./Enums.md#enum-form_out) | Enum | Determines the form to change into when leaving water. | 1 ||

</details>


---

### `TransformAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 56

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum | Specifies the ability that replaces the current ability. | 56 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformBasicAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 28

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum | Specifies the ability that replaces the unit's basic attack. | 28 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformBasicMove`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum | Specifies the name of the basic move to transform into. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformEquipment`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 1 ||
| [`to`](./Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 1 ||

</details>


---

### `TransformInXTurns`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`RandomPassivePool`](./Characters_and_Bosses.md#context-randompassivepool), [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 11 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 ||
| [`initiative`](./Enums.md#enum-initiative) | Enum / Integer | The unit's turn order priority; can be an integer modifier or 'keep_turns_end_turn' to force end of turn after acting. | 4 ||
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 ||

</details>


---

### `TransformItemOnElementInfluence`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `full_repair` | Boolean | If true, the item's durability is fully restored when transformed by element influence. | 5 ||
| [`item`](./Enums.md#enum-item) | Enum | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 5 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||

</details>


---

### `TransformNow`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum | Specifies the name of the form to immediately transform into. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformOnDeath`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 26

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformOnDeath`](./Enums.md#enum-transformondeath) | Array / Enum | Specifies the unit or list of units to transform into upon death. | 26 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TransformOnDeathImmediately`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum | Determines when the spawned unit takes its first turn relative to the spawn event. | 4 ||
| [`obj`](./Enums.md#enum-obj) | Array / Enum | Specifies one or more object names to bounce towards the target. | 4 ||

</details>


---

### `TransformOnElementInfluence`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||

</details>


---

### `TransformOnElementInfluencex`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||

</details>


---

### `TransformOnStatusThreshold`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 ||

</details>


---

### `TransformWeapon`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ApplyToSourceOnKill`](./Abilities_and_Spells.md#context-applytosourceonkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum | Specifies the source equipment item to be transformed. | 1 ||
| [`to`](./Enums.md#enum-to) | Enum | Specifies the target equipment item after transformation. | 1 ||

</details>


---

### `TransformWhenBuddyDies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformWhenBuddyDies`](./Enums.md#enum-transformwhenbuddydies) | Enum | Specifies the form the unit transforms into when its buddy dies. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TriggerWerewolfTransform`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array / Number | The number of stacks and probability of triggering the werewolf transformation. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WeremanTransformationReceiver`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`WeremanTransformationReceiver`](./Enums.md#enum-weremantransformationreceiver) | Enum | Determines which transformation animation or effect is applied when this unit is turned by a were-creature. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

## Boss & Special Mechanics (30)

### `AddRandomEliteBuff`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddRandomEliteBuff` | Number | The number of random elite buffs to apply to the unit. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlphaAllStatsUp`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlphaAllStatsUp` | Integer | The amount by which all of the unit's stats are increased if it is the alpha (highest stat total or designated leader). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlphaDodgeChance`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlphaDodgeChance` | Integer | The dodge chance granted to the alpha (leader) unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlphaStatusOnTurnBegin`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 1 ||

</details>


---

### `BossRewards`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum | Defines the common reward block for a boss encounter. | 1067 ||
| [`rare`](./Enums.md#enum-rare) | Enum | Defines the rare reward block for a boss encounter. | 673 ||

</details>


---

### `ChampionUpgradeNextMinion`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ChampionUpgradeNextMinion` | Integer | The number of champion upgrades applied to the next spawned minion. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChaosBossFlipMidTeleport`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ChaosBossFlipMidTeleport` | Integer | If set to a non-zero number, causes the chaos boss to flip direction mid-teleport. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChaosBossPieces`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array | An array of piece names that are considered actively part of the current form. | 1 ||
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array | An array of piece names that are considered passively part of the current form. | 1 ||

</details>


---

### `ClearFinalBossBattlefield`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ClearFinalBossBattlefield` | Integer | If set to a non-zero number, clears the battlefield during the final boss fight. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EliteFlatTint`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`EliteFlatTint`](./Arrays.md#array-eliteflattint) | Array | An RGB or RGBA tint multiplier applied uniformly to an elite unit's sprite. | 11 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EliteParticle`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 19

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`EliteParticle`](./Enums.md#enum-eliteparticle) | Enum | Specifies the particle effect name attached to an elite unit. | 19 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EliteTint`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 30

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`EliteTint`](./Arrays.md#array-elitetint) | Array | An RGBA tint color (r g b a) applied to elite variants of a unit. | 30 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EliteUpgradeNextMinion`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `EliteUpgradeNextMinion` | Integer | The number of elite upgrades applied to the next spawned minion. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_PartyBoss`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExplodeCharacter_PartyBoss` | Integer | The damage dealt to the party boss when it explodes. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FinalBossBeamQueue`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum | Specifies the ability queued to fire the boss's beam. | 1 ||
| [`release`](./Enums.md#enum-release) | Enum | Specifies the ability queued to release the boss's stored beams. | 1 ||
| [`transform`](./Enums.md#enum-transform) | Enum | Specifies the ability queued to transform the boss into its next form. | 1 ||

</details>


---

### `FinalBossBecomeTheChild`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Specifies the name of a character to spawn globally. | 1 ||
| `PlayBackground` | Integer | Specifies the background index to play. | 1 ||
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object | Defines a new song or layer for the background music. | 1 ||

</details>


---

### `FinalBossHitCountdownBoris`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`icon`](./Enums.md#enum-icon) | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 4 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 2 ||
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `FinalBossHitCountdownExplosive`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`icon`](./Enums.md#enum-icon) | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 4 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 2 ||
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `FinalBossHitCountdownHoly`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`icon`](./Enums.md#enum-icon) | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 4 ||
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `FinalBossPupils`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array | A 3D vector offset from the head position that the pupils should look at. | 1 ||
| [`radius`](./Arrays.md#array-radius) | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 1 ||
| [`reset_center_because_no_target_halflife`](./Enums.md#enum-reset_center_because_no_target_halflife) | Number | The half-life for the pupil position to reset to center when no target is available. | 1 ||
| [`reset_center_because_of_animation_halflife`](./Enums.md#enum-reset_center_because_of_animation_halflife) | Number | The half-life for the pupil position to reset to center during an animation. | 1 ||
| [`teleport_tracking_halflife`](./Enums.md#enum-teleport_tracking_halflife) | Number | The half-life for the pupil tracking to reacquire a target after a teleport. | 1 ||
| [`tracking_acquisition_halflife`](./Enums.md#enum-tracking_acquisition_halflife) | Number | The half-life for the pupil tracking to smoothly acquire a new target. | 1 ||
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array | A 3D vector representing the virtual position of the head for pupil tracking. | 1 ||

</details>


---

### `FinalBossQueueBeam`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FinalBossQueueBeam` | Integer | If true, queues the final boss beam attack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FinalBossShield`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FinalBossShield`](./Enums.md#enum-finalbossshield) | Enum | Specifies the shield ability used by a final boss, or None for no shield. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FinalBossShieldHealth`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum | Specifies the ability used to break the shield. | 1 ||
| [`state_health`](./Arrays.md#array-state_health) | Array | An array of health thresholds defining state transitions. | 1 ||

</details>


---

### `FinalBossSyncAnimations`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum | Specifies the name of the other boss character whose animations are synced. | 1 ||
| [`other_form_change_abilities`](Characters_and_Bosses.md#object-other_form_change_abilities) | Object | An object mapping form names to the other character's form change abilities. | 1 ||

</details>


---

### `NukeQuestFinalBossModifications`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 4688 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. | 436 ||
| [`splash_damage`](Abilities_and_Spells.md#object-splash_damage) | Object | Defines additional damage or effects applied to nearby targets around the primary target. | 68 ||

</details>


---

### `ScaldingOrbMoonBossOneShot`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | Specifies the item quest ID to mark as complete on kill. | 1 ||
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum | Specifies the item ID to remove from the source on kill. | 1 ||

</details>


---

### `SignalFinalBossShieldBroke`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SignalFinalBossShieldBroke` | Integer | If set to a non-zero number, signals that the final boss's shield has been broken. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpecialBossMultipartInstakill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum | Specifies the boss ID (e.g., "moonboss") whose multipart instakill mechanic is triggered. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TutorialBossRiggedFight`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TutorialBossRiggedFight` | Integer | The turn count at which the tutorial boss fight becomes rigged. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UpgradeTaggedSpawnsToChampions`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`UpgradeTaggedSpawnsToChampions`](./Enums.md#enum-upgradetaggedspawnstochampions) | Enum | Specifies which tag of spawns are upgraded to champion versions. | 2 ||

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

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `AbilityDisableIfLivingCrow`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityDisableIfLivingCrow` | Integer | If set, disables the ability if there is a living crow on the field. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnableIfConsumedCharacterHasTag`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum | Specifies the tag that a consumed character must have for the ability to be enabled. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfBasicAttackUsedThisTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Integer | If set, ability is enabled only if the unit used a basic attack this turn. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfNoAggroTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityEnabledIfNoAggroTarget` | Integer | If set, ability is enabled only when the unit has no aggro target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledIfSpecificItemEquipped`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md#enum-abilityenabledifspecificitemequipped) | Enum | Specifies the item that must be equipped for ability to be enabled. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledOncePerRound`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityEnabledOncePerRound` | Integer | If set, the ability can only be used once per round. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityEnabledPercentEachTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityEnabledPercentEachTurn` | Integer | The percentage chance each turn that this ability is enabled. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AbilityInheritsWeaponEffects`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AbilityInheritsWeaponEffects` | Integer | If set, the ability inherits properties from the unit's weapon, with higher values indicating different inheritance modes. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AcidRain`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AcidRain` | Number | If non-zero, enables the Acid Rain weather effect dealing damage each turn. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Adrenaline`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Adrenaline` | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AdvancedTint`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AdvancedTint`](./Arrays.md#array-advancedtint) | Array | An RGBA color array for advanced sprite tinting. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AdventureTokenPassivePool`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`StacyMutant_Brace`](Characters_and_Bosses.md#object-stacymutant_brace) | Object | A passive group granting the Brace ability and cosmetic changes. | 1 ||
| [`StacyMutant_Counter`](Characters_and_Bosses.md#object-stacymutant_counter) | Object | A passive group granting a counter attack and a bleed effect on basic attacks. | 1 ||
| [`StacyMutant_Damage`](Characters_and_Bosses.md#object-stacymutant_damage) | Object | A passive group increasing damage and decreasing max health with cosmetic changes. | 1 ||
| [`StacyMutant_DoubleHead`](Characters_and_Bosses.md#object-stacymutant_doublehead) | Object | A passive group granting an extra dispersed turn and cosmetic changes. | 1 ||
| [`StacyMutant_Fire`](Characters_and_Bosses.md#object-stacymutant_fire) | Object | A passive group granting fire immunity and a lava shot basic attack. | 1 ||
| [`StacyMutant_Health`](Characters_and_Bosses.md#object-stacymutant_health) | Object | A passive group increasing max health, reducing speed, and scaling size. | 1 ||
| [`StacyMutant_Holy`](Characters_and_Bosses.md#object-stacymutant_holy) | Object | A passive group granting a divine shield and cosmetic changes. | 1 ||
| [`StacyMutant_Ice`](Characters_and_Bosses.md#object-stacymutant_ice) | Object | A passive group granting ice immunity and an ice breath basic attack. | 1 ||
| [`StacyMutant_Lightning`](Characters_and_Bosses.md#object-stacymutant_lightning) | Object | A passive group granting electric immunity and a lightning dash basic attack. | 1 ||
| [`StacyMutant_Mirror`](Characters_and_Bosses.md#object-stacymutant_mirror) | Object | A passive group granting projectile reflection and random magic missile each turn. | 1 ||
| [`StacyMutant_Speed`](Characters_and_Bosses.md#object-stacymutant_speed) | Object | A passive group increasing speed, reducing damage, and scaling size. | 1 ||
| [`StacyMutant_Thorns`](Characters_and_Bosses.md#object-stacymutant_thorns) | Object | A passive group granting thorns damage and cosmetic changes. | 1 ||

</details>


---

### `AggroTargetIsCurrentTurn`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AggroTargetIsCurrentTurn` | Integer | If set to 1, the unit's aggro target is the unit currently taking its turn. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AggroTargetIsGovernedByHitEffect`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 1 ||

</details>


---

### `AlienBeastEyeStalks`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlienBeastEyeStalks` | Integer | The number of eye stalk segments on the Alien Beast. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlliesTakeExtraTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlliesTakeExtraTurn` | Integer | The number of extra turns granted to allies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AllyInfested`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Miscellaneous.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| [`faction`](./Enums.md#enum-faction) | Enum | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 1 ||

</details>


---

### `AlternateIdleAnimation`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum | Specifies the name of an alternative idle animation to play. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AlwaysHitDifferentTargets`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlwaysHitDifferentTargets` | Integer | If set to 1, attacks always target different units, never the same target twice. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Ammo`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 26

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Ammo` | Integer | The amount of ammo to add or remove (negative values subtract). | 26 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Angel`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Angel` | Integer | If 1, the unit is an angel type, which may affect behavior like reviving. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ApplyPassives`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

> **Referenced by:** [`Conditional_RandomChance`](./Abilities_and_Spells.md#context-conditional_randomchance), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 16 ||
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 12 ||
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 8 ||
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 6 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object | An object containing status effects or passives applied to the unit when the battle ends. | 6 ||
| [`YOffset`](./Enums.md#enum-yoffset) | Number | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 ||
| [`AddTag`](./Enums.md#enum-addtag) | Enum | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 2 ||
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 ||
| `Plant` | Integer | If set to 1, marks the unit as a Plant type, granting associated immunities and interactions. | 1 ||

</details>


---

### `ApplyToConsumed`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteObject` | Integer | If set, deletes the target object from the map. | 3 ||
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 1 ||

</details>


---

### `ApplyToOthersWithSharedTagAndFaction`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Marked`](Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 ||

</details>


---

### `ApplyToRandomClosestAlly`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Integer | The number of tiles to force the target to move toward the caster. | 1 ||

</details>


---

### `ApplyToRandomPartyMemberIfPossible`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_GoodRoll`](./Abilities_and_Spells.md#context-conditional_goodroll), [`Else`](./Abilities_and_Spells.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | Specifies the pool of disorders the unit can gain after the spell is cast. | 2 ||

</details>


---

### `ApplyToTile`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_DestructibleCorpse`](./Abilities_and_Spells.md#context-conditional_destructiblecorpse)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](Abilities_and_Spells.md#object-objectonhit) | Enum / Object | Specifies the object to spawn on the hit tile. | 2 ||
| `SpawnBearTrap` | Integer | If non-zero, spawns a bear trap on the tile. | 2 ||

</details>


---

### `ArcLightning`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 4 ||
| `max_distance` | Integer | The maximum range in tiles for the arc lightning to chain to subsequent targets. | 4 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 ||
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| `ignore_self` | Boolean | If true, the arc lightning effect does not chain to or affect the source unit itself. | 1 ||

</details>


---

### `Attraction`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `AvoidDamagingCharmedEnemies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AvoidDamagingCharmedEnemies` | Integer | If 1, the unit avoids dealing damage to charmed enemies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BackstabAllDirections`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BackstabAllDirections` | Integer | If 1, the unit deals backstab damage from all directions. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BackstabFront`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BackstabFront` | Number | If set to 1, allows backstab bonuses to apply when attacking from the front. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BasicAttackCantMiss`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BasicAttackCantMiss` | Integer | If nonzero, the unit's basic attack cannot miss. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BearTrapTrail`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BearTrapTrail` | Integer | If set to 1, leaves bear traps behind as the unit moves. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlackHolePassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BlackHolePassive` | Integer | If 1, the unit has black hole passive mechanics. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlackHoleSuck`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BlackHoleSuck` | Integer | The strength of the black hole's pull effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BlessingOfPeace`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BlessingOfPeace` | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BloatEyePassive2`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BloatEyePassive2`](./Enums.md#enum-bloateyepassive2) | Enum | Specifies the movement ability for the Bloat Eye enemy. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BloodRain`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BloodRain`](Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object | If non-zero, enables the blood rain visual effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Bloodzerked`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bloodzerked` | Integer | The number of Bloodzerk stacks applied. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BodyGuard`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||

</details>


---

### `BombBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BombBehavior` | Integer | If 1, the unit explodes after a set duration or on death. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BombRatTurtle`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BombRatTurtle`](Engine_StatusAndPassiveKeys.md#object-bombratturtle) | Integer / Object | The number of bomb rat turtle spawns triggered. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BoneArmorPassive`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BoneArmorPassive` | Integer | The number of stacks of bone armor granted, which absorbs damage. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BounceRock`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BounceRock`](./Arrays.md#array-bouncerock) | Array / Enum | Specifies the rock object to bounce. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Bound`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bound` | Integer | The number of stacks of the Bound status effect applied to the target. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BreakAtAux`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BreakAtAux` | Integer | The number of auxiliary item uses before this item breaks. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BreakIntoRocks`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | Specifies the type of rock (e.g., 'Coin', 'SmallRock') to spawn when breaking an inanimate object. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BreakOnElement`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum | Specifies an element that, when dealt to the unit, causes its armor or item to break. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Brittle`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 48

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Brittle` | Integer | The number of stacks of the Brittle status, or an object defining its properties. | 48 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `BungaCheers`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum | Specifies the cheer effect when an ally takes damage. | 1 ||
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum | Specifies the cheer effect when an ally dies. | 1 ||
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum | Specifies the cheer effect when an enemy takes damage. | 1 ||
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum | Specifies the cheer effect when an enemy dies. | 1 ||
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | Specifies the tag used to identify allied warriors for this ability. | 1 ||

</details>


---

### `BungaEntrance`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 ||
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 ||
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum | Specifies the tag used to identify allied warriors for this ability. | 2 ||

</details>


---

### `ButterflySwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ButterflySwarm` | Number | The number of butterflies spawned for the Butterfly Swarm effect. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CanApplyToInanimate`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_NotBoss`](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_Object`](./Abilities_and_Spells.md#context-conditional_object), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 10 ||
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum | Specifies the type of rock (e.g., 'Coin', 'SmallRock') to spawn when breaking an inanimate object. | 4 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 3 ||
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 3 ||
| `GetAggroTarget` | Integer | The number of aggro targets to acquire. | 2 ||
| `PreventDeathTransforms` | Integer | Number of death transforms prevented for non-boss characters. | 1 ||
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 1 ||

</details>


---

### `CanMutateTo`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CanMutateTo`](./Arrays.md#array-canmutateto) | Array / Enum | Specifies the mutation forms this unit can transform into, either a single form or an array of possible forms. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CancelPrimedAbilities`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CancelPrimedAbilities` | Integer | If non-zero, cancels any primed abilities on the target. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CanceledQueuedInput`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CanceledQueuedInput` | Integer | If set to a non-zero number, cancels any queued input from the target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CantCatchDiseases`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CantCatchDiseases` | Integer | The number of stacks that prevent the unit from contracting diseases. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CatchBoomerang`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CatchBoomerang` | Integer | If set, allows the ability to catch a boomerang, with the integer representing the number of catches. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CaveFamilyEnrage`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 ||

</details>


---

### `CaveWomanBirthControl`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CaveWomanBirthControl` | Integer | If true, restricts or controls the spawning of additional units via birth mechanics. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CerberubsAggroTargetBehavior`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum | Specifies the form to use when the unit is alerted. | 1 ||
| [`default_form`](./Enums.md#enum-default_form) | Enum | Specifies the default form before aggro. | 1 ||

</details>


---

### `ChanceToAmbush`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ChanceToAmbush` | Integer | The percentage chance for the unit to ambush an enemy. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChanceToBreakFree`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum | Specifies the ability to be used when the parent condition (e.g., breaking free) fails. | 3 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||

</details>


---

### `ChanceToDisableActionsIfNotCharmed`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ChanceToDisableActionsIfNotCharmed` | Integer | The percentage chance to disable actions of enemies that are not charmed. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeCatClass`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 28

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum | Specifies the new class to assign to the unit. | 28 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeFaction`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum | Specifies the name of the faction to switch the target to. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeTileOnPop`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ChangeTileOnPop`](./Enums.md#enum-changetileonpop) | Enum | The type of tile that appears when this unit is destroyed. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeTileUnderCharacterAtStart`
> Found in: *Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ChangeTileUnderCharacterAtStart`](./Enums.md#enum-changetileundercharacteratstart) | Enum | Specifies the tile type to change the tile under the character to at the start of battle. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ChangeTilesUnder`
> Found in: *Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | The tile type to change the ground tiles under the target to. | 18 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CharacterLightSource`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array | The RGB color of the light source. | 10 ||
| [`glow`](./Arrays.md#array-glow) | Array | The RGBA glow color of the light source. | 8 ||
| [`size`](./Enums.md#enum-size) | Enum / Number | The scale factor (size multiplier) of the spawned unit. | 3 ||

</details>


---

### `ClearDefaultDebris`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ClearDefaultDebris` | Number | If true, removes all default debris from the battlefield. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ClearStarving`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ClearStarving` | Integer | The number of stacks of Starving cleared. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CloneWeaponTemp`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CloneWeaponTemp` | Integer | The number of turns the cloned weapon persists before being removed. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CockroachSwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CockroachSwarm` | Number | If true, the unit spawns as a Cockroach Swarm, with its specific mechanics and effects. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CollideWithConsumed`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CollideWithConsumed` | Equation | Damage formula for collision with consumed objects, e.g., '4+bonus_melee_damage'. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CollideWithThrowTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CollideWithThrowTarget` | Integer | Determines whether the thrown object collides with the primary target (0 disables collision). | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CompleteItemQuest`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum | Specifies the item quest ID to mark as complete on kill. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ConjureRandomAbilityFromCat`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ConjureRandomAbilityFromCat` | Integer | The number of random abilities created or given to the cat unit from a pool of cat-themed abilities. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Consumed`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

> **Referenced by:** [`Conditional_Buddy`](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_LivingPlayerCat`](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Specifies the name of the ability the consumed unit uses to attempt escape. | 13 ||
| `force_contact` | Boolean | If true, the consumed unit is forced into contact with the consumer. | 11 ||
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 8 ||
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | Specifies the mounting mode; values include 'auto' or 'true'. | 8 ||
| `wet` | Boolean | If true, the consumed unit is considered wet (e.g., for elemental interactions). | 8 ||
| `do_not_pop_corpse` | Boolean | If true, the consumed unit's corpse is not popped upon consumption. | 7 ||
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 7 ||
| `drop_on_self_death` | Boolean | If true, the consumed unit is dropped when the consumer dies. | 3 ||
| [`extra_statuses`](Abilities_and_Spells.md#object-extra_statuses) | Object | An object containing additional status effects (with stack counts) applied to the consumed unit. | 3 ||
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Specifies the ability used to drop the consumed body. | 1 ||
| `kill_on_consume` | Boolean | If true, the consumed unit is killed immediately upon consumption. | 1 ||
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 1 ||

</details>


---

### `CopyBasicAttackEffects`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CopyBasicAttackEffects` | Integer | If set, the ability copies the effects from the unit's basic attack. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CopyCatPassive_Initializer`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CopyCatPassive_Initializer` | Integer | The number of copies of this passive to initialize. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CopyPassiveSlot`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CopyPassiveSlot` | Integer | An index (0-based) specifying which equipment slot's passive to copy onto this unit. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CopySpells`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 1 ||

</details>


---

### `CorpseVaporizer`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CorpseVaporizer` | Integer | The number of corpses vaporized on hit. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CountAsCorpse`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CountAsCorpse` | Integer | If 1, the unit counts as a corpse for interactions like raising or necromancy. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CreateGlobalModifiers`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BloodRain`](Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object | If non-zero, enables the blood rain visual effect. | 2 ||
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 2 ||

</details>


---

### `CrowAttackLink`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CrowAttackLink` | Integer | If 1, allows this unit's attacks to chain or link to nearby enemies like a crow. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `CyborgTurns`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Miscellaneous.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`TakeBonusTurnWithAIControl`](Abilities_and_Spells.md#object-takebonusturnwithaicontrol) | Object | An object configuring whether the bonus turn happens at the end of the round and whether spells are included. | 1 ||

</details>


---

### `DeadAltAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DeadAltAbility`](./Enums.md#enum-deadaltability) | Enum | Specifies an alternative ability used when the unit is dead. | 24 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeathwormUnderground`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum | Specifies the ability triggered when the Deathworm emerges from underground. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DecoySwapper`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DecoySwapper` | Integer | If true, the decoy swaps places with the source when spawned. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeferVaporize`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeferVaporize` | Integer | If set to 1, the unit's vaporize (instant death) is delayed until the end of the current action. | 18 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DelayCastAbility`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `lingering` | Boolean | If true, the ability effect lingers after the initial cast. | 1 ||
| `relative` | Boolean | If true, the delay is calculated relative to the current turn count rather than as an absolute time. | 1 ||

</details>


---

### `DeleteInanimateObjectsChance`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteInanimateObjectsChance` | Number | The percentage chance per tick to delete all inanimate objects on the battlefield. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeleteObject`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteObject` | Integer | If set, deletes the target object from the map. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DeleteTraps`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteTraps` | Integer | If true, removes all traps from the map. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyphFrames`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyphFrames` | Integer | The number of animation frames for the demonic glyph effect. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyph_Bite`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Integer | The weight for the demonic glyph of bite, or its configuration. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyph_Bounce`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bounce` | Integer | The weight for the demonic glyph of bounce, or its configuration. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DemonicGlyph_Fire`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Fire` | Integer | The weight for the demonic glyph of fire, or its configuration. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DestroyEquipmentAndAttachParasite`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`Conditional_ActiveWeather_Any`](./Abilities_and_Spells.md#context-conditional_activeweather_any), [`Conditional_DebuffRoll`](./Abilities_and_Spells.md#context-conditional_debuffroll), [`Else`](./Abilities_and_Spells.md#context-else), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| [`pool`](./Arrays.md#array-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 ||

</details>


---

### `DestroyNeckArmor`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DestroyNeckArmor` | Integer | If true, destroys the target's neck armor slot. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DestroyTrinket`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DestroyTrinket` | Integer | The number of trinkets destroyed. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DestroyWeapon`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DestroyWeapon` | Integer | The number of weapons destroyed. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DestroyWeaponThrow`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DestroyWeaponThrow` | Integer | The number of weapons destroyed after being thrown. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DiceBehavior`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer | The number of sides on the die. | 1 ||
| `knockback_damage` | Integer | The amount of damage dealt by the knockback. | 1 ||

</details>


---

### `DicerArt`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DicerArt`](./Arrays.md#array-dicerart) | Array | An array of art offset values for the Dicer enemy. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Die`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. | 62 ||

</details>


---

### `DieViaAbilityInternally`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DieViaAbilityInternally` | Integer | If non-zero, causes the target to die via an internal ability trigger. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DieViolently`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DieViolently` | Integer | If true, causes the target to die with a violent, explosive visual effect. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DiesToElement`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 1 ||

</details>


---

### `DiesToPiercingAndSpikes`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean | If true, the destruction is deferred until the character is settled. | 1 ||

</details>


---

### `DigestDeadBodies`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DigestDeadBodies`](./Enums.md#enum-digestdeadbodies) | Enum | Specifies the ability or animation used when digesting a dead body. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DinoLegAnimation`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum | Specifies the animation trigger for the dinosaur leg (e.g., 'poop' for the poop animation). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisablePassiveSlot`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisablePassiveSlot` | Integer | If non-zero, disables the specified passive slot index (0 or 1). | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisableSpells`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisableSpells` | Integer | If 1, the unit cannot cast spells. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisableWeapon`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DisableWeapon` | Integer | If set, disables the source's weapon, preventing its use. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Disguised`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Disguised` | Integer | If true, the unit is disguised, appearing as a different faction or model. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DisguisedTrapper`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DisguisedTrapper`](./Enums.md#enum-disguisedtrapper) | Enum | Specifies the passive used when disguised as a trapper, e.g. FearMelee. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DissolveRandomArmorPiece`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DissolveRandomArmorPiece` | Integer | If true, destroys a random armor piece (head, body, neck) on the target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DissuadeInstakills`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DissuadeInstakills` | Integer | If set to 1, this unit cannot be instantly killed. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoScreenShake`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 10 ||
| `time` | Variable | The duration in seconds of the screen shake effect. | 10 ||

</details>


---

### `DoubleCast`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCast` | Integer | The number of double-cast stacks, allowing a spell to be cast twice. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DoubleCastTaggedSpells`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum | Specifies the spell tag (e.g., musical) that causes spells to be cast twice. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DrainAllyCatsForFleshGolem`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DrainAllyCatsForFleshGolem` | Integer | The amount of health drained from ally cats to heal the Flesh Golem. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DrinkWater`
> Found in: *Abilities & Spells, Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DrinkWater` | Integer | The number of water-drink actions performed. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Drowsy`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 15 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DustCloudBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DustCloudBehavior` | Integer | An integer flag that controls the behavior mode of a dust cloud entity. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Dybbuk1HPTracker`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Dybbuk1HPTracker` | Integer | A flag indicating the unit tracks that it has 1 HP remaining for Dybbuk possession mechanics. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `DybbukPossessed`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Else`](./Abilities_and_Spells.md#context-else)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum | Determines the ability used when the Dybbuk possession ends. | 1 ||
| [`punch_self_ability`](./Enums.md#enum-punch_self_ability) | Enum | Determines the ability used for the possessed unit to attack itself. | 1 ||

</details>


---

### `ElectricArcs`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ElectricArcs` | Integer | The number of electric arcs emitted by this unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ElementWeakness`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ElementWeakness`](./Enums.md#enum-elementweakness) | Enum | Determines which element the unit is weak to, e.g. Fire. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EmptyMind`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`EmptyMind`](Engine_StatusAndPassiveKeys.md#object-emptymind) | Integer / Object | The number of Empty Mind stacks, likely disabling special abilities. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EnableWeather`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum | Specifies the weather effect to enable. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EndTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 28

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `EndTurn` | Integer | If set to 1, ends the current unit's turn immediately after this effect. | 28 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Enlarge`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Enlarge`](Engine_StatusAndPassiveKeys.md#object-enlarge) | Integer / Object | The number of turns the unit is enlarged, increasing its size and stats. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EnterMount`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Specifies the name of the mount status to apply to the unit. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EventBounterHunterPassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `EventBounterHunterPassive` | Integer | A flag enabling the event bounty hunter passive behavior. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EventBounty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `EvolveAbilityFromPool`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 21

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 13 ||
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 ||

</details>


---

### `ExcludeFromEvents`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum | Specifies the event type (e.g., Tragedy) that this unit is excluded from participating in. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExplodeCharacter` | Integer | The radius (in tiles) of an explosion centered on the character. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_DeathBloom`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExplodeCharacter_DeathBloom` | Integer | The amount of damage dealt by the DeathBloom explosion. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_DeathBloom2`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExplodeCharacter_DeathBloom2` | Integer | The amount of damage dealt by the DeathBloom2 explosion. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_NoDie`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExplodeCharacter_NoDie` | Integer | The damage dealt when a character explodes without dying. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_Party`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExplodeCharacter_Party` | Integer | The radius (in tiles) of an explosion centered on the character that also damages party members. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_RockCrusher`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExplodeCharacter_RockCrusher` | Integer | The number of RockCrusher explosion triggers applied to non-boss characters. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplodeCharacter_RockCrusher_PetrifyBreak`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | The damage dealt when a petrified RockCrusher explodes. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExplosionIfHitSomething`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExplosionIfHitSomething` | Integer | The radius of explosion triggered if the attack hits an entity. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExtraDispersedTurns`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ExtraDispersedTurns` | Integer | The number of additional or fewer turns in the dispersed turn order. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ExtraTurnsPerTaggedUnit`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md#enum-extraturnspertaggedunit) | Enum | Specifies the tag of units that grant extra turns when present. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FaceCamera`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FaceCamera` | Integer | If non-zero, forces the character to rotate and face the camera. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FactionDisguiseSource`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FactionDisguiseSource` | Integer | If true, the unit adopts the faction of the source unit for disguise. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FadeInsteadOfDie`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FadeInsteadOfDie` | Integer | If non-zero, the unit fades out instead of dying. | 20 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FireArmor2`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FireArmor2`](Engine_StatusAndPassiveKeys.md#object-firearmor2) | Integer / Object | The number of Fire Armor2 stacks (likely a variant). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FireStorm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FireStorm` | Number | The percentage chance or combo definition for the Fire Storm effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FireflySwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FireflySwarm` | Number | The number of fireflies in the swarm effect. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Flammable`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 26

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Flammable` | Integer | The number of stacks of Flammable, or an object defining its properties. | 26 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FloatingRockTrap`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FloatingRockTrap` | Integer | The number of stacks of Floating Rock Trap applied to the target, dealing damage when stepped on. | 13 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlushmasterCelebration`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FlushmasterCelebration`](./Enums.md#enum-flushmastercelebration) | Enum | Specifies the celebration animation or effect name used by the Flushmaster. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FlySwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FlySwarm`](Engine_StatusAndPassiveKeys.md#object-flyswarm) | Object | Summons a fly swarm with the given chance or intensity percentage. | 5 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Fog`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fog` | Number | When an integer, the intensity of fog; when an object, defines the fog particle effect. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Fragile`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 44

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fragile` | Integer | The number of stacks of the Fragile status, causing increased damage taken. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FrankBolts`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FrankBolts`](Passives_and_Statuses.md#object-frankbolts) | Integer / Object | The number of Frank Bolts applied or available. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FreeFirstCast`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FreeFirstCast` | Integer | The number of free casts of this ability per battle. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `FreeFirstCastEachMatch`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FreeFirstCastEachMatch` | Integer | If set to 1, the first cast of the ability each match costs no resources. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainDisorder`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | Specifies the name of the disorder gained. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GainDisorderFromPool`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`AddStatusToBasicAttack`](./Characters_and_Bosses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| [`pool`](./Enums.md#enum-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 ||

</details>


---

### `GainDisorderFromPool_PostCast`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 32

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool_PostCast`](./Enums.md#enum-gaindisorderfrompool_postcast) | Enum | Specifies the pool of disorders the unit can gain after the spell is cast. | 32 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GasCanBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GasCanBehavior` | Integer | An integer flag that controls the behavior mode of a gas can entity. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GasCloudBehavior2`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GasCloudBehavior2` | Integer | An integer flag that controls a secondary behavior mode of a gas cloud entity. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GeminiTwin`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GeminiTwin` | Integer | If set to 1, this unit is the twin in a Gemini pair. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GenericBuff`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GenericBuff` | Integer | A generic buff value applied to the unit. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GenericDebuff`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 30

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GenericDebuff` | Integer | The number of stacks of a generic, untooltipped debuff applied to the target. | 30 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GetAggroTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GetAggroTarget` | Integer | The number of aggro targets to acquire. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GiveBoundItemToTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GiveBoundItemToTarget` | Integer | If true, gives the source's bound item to the target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GlobalEnemyAutoRevive`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GlobalEnemyAutoRevive` | Integer | The percentage chance for all enemies to automatically revive after being defeated. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GoopWalk`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GoopWalk` | Integer | If set to 1, this unit can move through goop tiles without being slowed or damaged. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Grappled`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Grappled`](./Arrays.md#array-grappled) | Array / Integer | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. | 16 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Grappling`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`FormChanger`](./Characters_and_Bosses.md#context-formchanger)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 6 ||
| [`exit_animations`](Characters_and_Bosses.md#object-exit_animations) | Object | An object mapping exit conditions to their corresponding animation names. | 1 ||

</details>


---

### `GroundFlopper`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GroundFlopper`](./Enums.md#enum-groundflopper) | Enum | The movement ability used when this unit is on the ground. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `GuillotinaDeathHead`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GuillotinaDeathHead` | Integer | If set to 1, the unit spawns a head object upon death via guillotine. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HarpoonTrapPassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HarpoonTrapPassive`](./Enums.md#enum-harpoontrappassive) | Enum | Specifies the ability name used when the harpoon trap is triggered. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HeatWave`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HeatWave` | Number | When an integer, the intensity of the heat wave; when an object, defines the visual effects or status properties. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HeavyHits`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HeavyHits` | Integer | The number of Heavy Hits stacks increasing attack impact. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Hex`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HiddenDoomed`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HiddenDoomed` | Integer | The number of stacks of a hidden doomed status effect applied to the unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HideEquipment`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Specifies which equipment slot is visually hidden. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HideSomeHudStuff`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HideSomeHudStuff` | Integer | If set to 1, hides certain HUD elements. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `HitlerExecute`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 ||

</details>


---

### `IgnoreDebuffs`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IgnoreDebuffs` | Integer | If true, the effect ignores debuffs on the target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IgnoreSelf`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 150

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IgnoreSelf` | Variable | If set to 1 or true, the damage instance ignores the source unit (does not affect itself). | 150 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `IllusionTint`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IllusionTint` | Integer | If non-zero, applies an illusionary tint to the unit's sprite. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ImmediateUseAbility`
> Found in: *Abilities & Spells, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`StatusEachTurnEnd`](./Items_and_Equipment.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 ||

</details>


---

### `ImmediateUseAbility_Instant`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility_Instant`](./Enums.md#enum-immediateuseability_instant) | Enum | Specifies the name of an ability to use instantly as a passive effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ImmediateUseDirectionalAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum | Specifies the name of a directional ability to be used immediately by the unit. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ImmobilePassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ImmobilePassive` | Integer | If set to 1, this unit cannot move from its starting position. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Imprison`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Imprison`](./Enums.md#enum-imprison) | Enum | Specifies the type of unit or object to summon as a prison. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `InsertIntoBackgroundPlaceholder`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `InsertIntoBackgroundPlaceholder` | Integer | If set to 1, the unit is inserted into a background placeholder slot. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Instakill`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Instakill`](./Arrays.md#array-instakill) | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 24 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `InterchangeDisabler`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `InterchangeDisabler` | Integer | If set to 1, prevents the unit from being interchanged with another unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JohnnyCriesForWashers`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `JohnnyCriesForWashers` | Integer | The number of washers (currency) requested by the Johnny NPC. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JohnnyNeedsWashing`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum | Specifies the form name for the unwashed state. | 1 ||
| [`form_washed`](./Enums.md#enum-form_washed) | Enum | Specifies the form name for the washed state. | 1 ||

</details>


---

### `JohnnyWasher`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`JohnnyWasher`](./Enums.md#enum-johnnywasher) | Enum | Specifies the ability name used by the washer form to clean Johnny. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JudgementDay`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `JudgementDay` | Number | When an integer, the turn count or damage for Judgement Day; when an object, defines the weather status. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `JumpAttackLeaveBehind`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`JumpAttackLeaveBehind`](./Enums.md#enum-jumpattackleavebehind) | Enum | Specifies the entity to leave behind at the jump attack's landing point. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KaijuWinCon`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KaijuWinCon`](./Enums.md#enum-kaijuwincon) | Enum | Determines which kaiju victory condition is active for this unit. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `KillEnemyOfTypeAtBattleStart`
> Found in: *Events & Encounters, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`global_effect_next_fight`](./Events_and_Encounters.md#context-global_effect_next_fight)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`enemy_type`](./Enums.md#enum-enemy_type) | Enum | Specifies the type of enemy to kill at the start of battle. | 2 ||
| [`fallback_spawn`](./Arrays.md#array-fallback_spawn) | Array | An array of enemy names to spawn as a fallback if no matching enemy type is present. | 1 ||

</details>


---

### `KnockOutClone`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`KnockOutClone`](./Enums.md#enum-knockoutclone) | Enum | Specifies the ability ID used to knock out or remove the player's clone unit from battle. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LaunchOffScreen`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `LaunchOffScreen` | Equation | A formula string that determines the knockback force to launch the unit off-screen. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LaunchOffScreenInstakill`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `LaunchOffScreenInstakill` | Integer | If non-zero, the unit is instantly killed and launched off-screen. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LeaveBehind`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

> **Referenced by:** [`temporary_effects`](./Abilities_and_Spells.md#context-temporary_effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||

</details>


---

### `LockOrientationFaceTile`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`LockOrientationFaceTile`](./Arrays.md#array-lockorientationfacetile) | Array | A tile coordinate [x y] that the unit's orientation is locked to face. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LoopingSoundWhileAlive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`LoopingSoundWhileAlive`](./Enums.md#enum-loopingsoundwhilealive) | Enum | The looping sound effect played while the unit is alive. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `LowerAmbientLight`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`CreateGlobalModifiers`](./Abilities_and_Spells.md#context-createglobalmodifiers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array | For ambient light, the target brightness value (as a float or percentage array for RGB). | 8 ||
| [`speed`](./Arrays.md#array-speed) | Array / Number | The speed of the projectile or move, can be a value or a range. | 6 ||

</details>


---

### `MakeBasicAttackPull`
> Found in: *Cat Mutations, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MakeBasicAttackPull` | Integer | If nonzero, the unit's basic attack pulls the target closer. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MakeWeaponUnbreakable`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MakeWeaponUnbreakable` | Integer | If true, makes the equipped weapon unbreakable. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MamaCatAnimations`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MamaCatAnimations` | Integer | If set to 1, enables special mama cat animations. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManglerAttack`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ManglerAttack` | Integer | If true, the attack triggers the Mangler's attack pattern. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManglerMonsterPassive`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ManglerMonsterPassive`](./Enums.md#enum-manglermonsterpassive) | Enum | Specifies the ability name used for the Mangler monster's dash attack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ManglerShuffle`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ManglerShuffle` | Boolean | If true, the order of effects in this damage instance is randomized before application. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MassAttackThis`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MassAttackThis` | Integer | The number of additional targets this attack hits via the Mass Attack mechanic. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Math`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||
| [`Stun`](./Arrays.md#array-stun) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 ||
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 1 ||

</details>


---

### `Meaty`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Meaty` | Integer | The number of Meaty stacks increasing health or size. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MeteorShower`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MeteorShower` | Number | The chance (as a percentage) for a meteor shower to occur on a given turn. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Meteornado`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Meteornado` | Number | The number of Meteornado status stacks applied, or an object defining its visual effects. | 3 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Metronome`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array | A list of ability IDs that are excluded from random selection or usage in the Metronome effect. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `MimicMetronome`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MimicMetronome` | Integer | The number of random abilities the Metronome effect selects from this unit's ability pool. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ModelingClayPassive`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ModelingClayPassive` | Integer | If set to 1, enables the passive that duplicates the equipped item on the unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ModifyAbility`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Items_and_Equipment.md#context-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 4719 ||
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 3702 ||

</details>


---

### `MonkStanceSwitch`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MonkStanceSwitch` | Integer | The number of times to switch monk stance. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MonkStances`
> Found in: *Cat Classes, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MonkStances`](./Arrays.md#array-monkstances) | Array | An array of stance ability names the Monk can switch between. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MotherGrowController`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eat_damage`](Characters_and_Bosses.md#object-eat_damage) | Object | An object defining the damage properties of the eat attack. | 1 ||
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum | Specifies the name of the tumor object to spawn. | 1 ||

</details>


---

### `MotherTumorPassive`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](Characters_and_Bosses.md#object-cat) | Object | Defines the behavior and form change for captured cat units. | 10 ||
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array | An array of form names the tumor considers for interaction. | 1 ||
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum | Specifies the ability used by the tumor to grow. | 1 ||
| [`NonCat`](Characters_and_Bosses.md#object-noncat) | Object | Defines the behavior and form change for captured non-cat units. | 1 ||
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum | Specifies the animation played when passing something to the tumor. | 1 ||
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum | Specifies the animation played when receiving something from the tumor. | 1 ||

</details>


---

### `Mount`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum | Specifies the ability used to eject the mounted character. | 1 ||
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum | Specifies the ability used to enter the mount. | 1 ||

</details>


---

### `MutateViaAbility`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MutateViaAbility`](./Enums.md#enum-mutateviaability) | Enum | Specifies the ability that triggers a mutation form change. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `MuteDemonicGlyphDisplay`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MuteDemonicGlyphDisplay` | Integer | If set to 1, suppresses the display of demonic glyphs on the character. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Muted`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Muted` | Integer | The number of Muted stacks, disabling certain abilities. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NextPlayerCatTakesExtraTurn`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NextPlayerCatTakesExtraTurn` | Integer | The number of extra turns the active player cat gains. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `NoCorpses`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NoCorpses` | Integer | If set to 1, corpses are prevented from spawning. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ObjectDetector`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 545 ||
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

</details>


---

### `Ostracized`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Ostracized` | Integer | The number of stacks of Ostracized applied. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PackHunting`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PackHunting` | Integer | If set to 1, enables pack hunting behavior for the character. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PartialPurge`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PartialPurge` | Integer | The amount of beneficial status effects removed from the target. | 20 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PassiveIfStrAuxEquals`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`value`](./Math_Equations.md) | Equation | The numeric value or formula associated with the buff. | 485 ||

</details>


---

### `PassiveIfWeaponIsUsable`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 ||

</details>


---

### `PassiveWhileHasDurability`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 2 ||

</details>


---

### `PassiveWhileNotTakingTurn`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 178 ||

</details>


---

### `PermanentCharisma`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. | 5 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PermanentConfusion`
> Found in: *Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PermanentConfusion` | Number | If set to 1, the unit is permanently confused and cannot be cured. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PermanentLuck`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. | 5 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PersistentElement`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`PersistentElement`](./Enums.md#enum-persistentelement) | Enum | Specifies the element type that this status effect permanently imbues (e.g., Holy). | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PhysicalAttacksMiss`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PhysicalAttacksMiss` | Integer | If set to 1, all physical attacks against the unit automatically miss. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Plant`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Plant` | Integer | If set to 1, marks the unit as a Plant type, granting associated immunities and interactions. | 18 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PlayBackground`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PlayBackground` | Integer | Specifies the background index to play. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PoisonLace`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`PoisonLace`](Engine_StatusAndPassiveKeys.md#object-poisonlace) | Integer / Object / String | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PoolMetronome`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 ||

</details>


---

### `Possessed`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PreventSpecificInjury`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PreventSpecificInjury` | Equation | Specifies a body part tag (e.g., 'int' for head) that cannot receive injuries. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizeAggroTarget`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PrioritizeAggroTarget` | Integer | A priority weight for targeting the current aggro target. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizeFarAwayTargets`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PrioritizeFarAwayTargets` | Integer | The weight for AI to prioritize targets based on distance; higher values favor farther targets. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizeHitDifferentTargets`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PrioritizeHitDifferentTargets` | Integer | If set to 1, the unit's AI prioritizes hitting different targets rather than focusing one. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizePlayerCats`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PrioritizePlayerCats` | Integer | A priority weight for targeting player-controlled cats. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PrioritizeWeakestEnemy`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PrioritizeWeakestEnemy` | Integer | A priority weight for targeting the weakest enemy unit. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ProbeCharmed`
> Found in: *Abilities & Spells, Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PullSourceToTarget`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PullSourceToTarget` | Integer | The amount of tiles the source is pulled towards the target after the attack. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `PurgeAll`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PurgeAll` | Integer | If non-zero, removes all temporary status effects (buffs, debuffs) from the target. | 22 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `QuakeAreaChance`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`radius`](./Arrays.md#array-radius) | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 2 ||
| [`chance`](./Enums.md#enum-chance) | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

</details>


---

### `QueueUseAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum | Specifies the ability ID to be used immediately after the current action resolves. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomLightning`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomLightning` | Number | Chance per turn or action for a random lightning strike to occur, expressed as a percentage (e.g., 50%). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomTaggedMutation`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomTaggedMutation`](./Enums.md#enum-randomtaggedmutation) | Enum | Specifies the tag to filter random mutations by. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomWeatherEachFight`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomWeatherEachFight`](./Arrays.md#array-randomweathereachfight) | Array | An array of weather types from which one is randomly selected at the start of each battle. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RandomizeAIWeightsEachTurn`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomizeAIWeightsEachTurn`](./Arrays.md#array-randomizeaiweightseachturn) | Array | The range of random weights applied to AI actions each turn. | 16 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RealTimePressure`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RealTimePressure` | Integer | The number of real-time seconds before a pressure effect or penalty applies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReclaimItemOnBreak`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReclaimItemOnBreak` | Integer | If set to 1, the item returns to the inventory when it breaks instead of being lost. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReflectProjectiles`
> Found in: *Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. | 436 ||

</details>


---

### `RefreshEquipmentAbilityOnElement`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`text`](./Strings.md#string-text) | String | The localization key for the name of this injury. | 13 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||

</details>


---

### `RefreshItemAbilities`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RefreshItemAbilities` | Integer | The number of times all item abilities are recharged (cooldowns reset). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RefreshOncePerFightAbilities`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RefreshOncePerFightAbilities` | Integer | The number of times abilities limited to once per fight are refreshed. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RefreshWeaponAbility`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RefreshWeaponAbility` | Integer | The number of times the weapon's ability is refreshed. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Regurge`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Regurge`](Engine_StatusAndPassiveKeys.md#object-regurge) | Integer / Object | The number of regurgitation triggers. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnAllyCatDies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnAllyCatDies` | Integer | If set to 1, restores a charge when an allied cat dies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnAllyDies`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnAllyDies` | Integer | If set to 1, restores a charge when any ally dies. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReloadOnBackstab`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReloadOnBackstab` | Integer | If set to 1, restores a charge when performing a backstab. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairAll`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairAll` | Integer | The amount of durability restored to all equipped items. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairAllCondition`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairAllCondition` | Integer | If non-zero, fully repairs the condition of all equipped items. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairArmorCondition`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairArmorCondition` | Integer | The amount of armor condition restored. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RepairTrinket`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReplaceBasicAttack_Mutation`
> Found in: *Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ReplaceBasicAttack_Mutation`](./Enums.md#enum-replacebasicattack_mutation) | Enum | Specifies the mutation-based ability (e.g., FetusSpit) that replaces the unit's standard basic attack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReplaceSpell`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`TempPassiveWhileHasStatus`](./Abilities_and_Spells.md#context-temppassivewhilehasstatus)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 4 ||

</details>


---

### `RerollEnemy`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RerollEnemy` | Integer | The number of times the target enemy is re-rolled (transformed into a new random enemy). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReturnDinoLegs`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ReturnDinoLegs` | Integer | If non-zero, returns the Dino Legs ability to the unit after it is consumed. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ReviveNextRound`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`additional_passives`](./Abilities_and_Spells.md#context-additional_passives), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 ||
| `revive_health` | Integer | The amount of health (as a flat integer or percentage) the unit revives with. | 3 ||
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 ||

</details>


---

### `RockyArmorPassive`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RockyArmorPassive` | Integer | The number of stacks of the Rocky Armor status effect granted. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `RockyArmorSalvage`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RockyArmorSalvage`](./Enums.md#enum-rockyarmorsalvage) | Enum | A multiplier for the percentage of armor value salvaged when the unit takes damage. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SafeDie`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SafeDie` | Integer | The number of times the unit can survive a fatal hit. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Sandstorm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Sandstorm`](Engine_StatusAndPassiveKeys.md#object-sandstorm) | Object | A self-buff ability that creates a sandstorm, applying a status effect (may be 'Sandstorm 1' or an object definition with a specific template). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScalingAttackAnimation`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](Characters_and_Bosses.md#object-default) | Enum / Object | The default configuration or value used when no specific override is provided. | 199 ||
| [`thresholds`](./Arrays.md#array-thresholds) | Array | An array of health percentage thresholds that trigger an alt state. | 1 ||

</details>


---

### `SchizoIllusionAIModifier`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SchizoIllusionAIModifier` | Integer | If non-zero, modifies the AI behavior for schizo illusions. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScrambleEverything`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ScrambleEverything` | Integer | The percentage chance to scramble all abilities and passives on the target. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ScrambleLastUsedSpell`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `permanent` | Boolean | If true, the scrambled spell selection persists permanently rather than resetting after use. | 1 ||

</details>


---

### `Scrambled`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Scrambled` | Integer | The number of stacks of Scrambled applied. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SelfStun`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SelfStun`](./Arrays.md#array-selfstun) | Array / Integer | The number of stacks of self-stun applied, with an optional probability as a second element. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SendRock`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SendRock` | Integer | The number of rocks to send as projectiles. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SerratedClaws`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SerratedClaws` | Integer | The number of stacks of the SerratedClaws status applied, or an object defining its display strings. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetAnimationAlts`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`Conditional_HasTag`](./Abilities_and_Spells.md#context-conditional_hastag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dead`](./Enums.md#enum-dead) | Enum | Determines the animation set used when the unit is dead. | 1 ||
| [`dying`](./Enums.md#enum-dying) | Enum | Determines the animation set used when the unit is in a dying state. | 1 ||

</details>


---

### `SetCrazyEyeBackgroundWeights`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 3 ||

</details>


---

### `SetFaction`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum | Specifies the faction the unit belongs to (e.g., 'enemies'). | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SetItemAux`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`Conditional_Shielded`](./Items_and_Equipment.md#context-conditional_shielded), [`StatusOnBattleEnd`](./Items_and_Equipment.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`value`](./Math_Equations.md) | Equation | The numeric value or formula associated with the buff. | 485 ||
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 3 ||

</details>


---

### `SharkySmellsBlood`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SharkySmellsBlood` | Integer | If 1, the unit is attracted to damaged units and may prioritize them. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Shatter`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Shatter`](Engine_StatusAndPassiveKeys.md#object-shatter) | Integer / Object | The amount of damage dealt when a frozen or petrified status is shattered, or a template definition for a Shatter ability. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShootHereCommand`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ShootHereCommand` | Integer | If non-zero, commands an allied unit to shoot at this unit's target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShootHereReceiver`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ShootHereReceiver` | Integer | If non-zero, marks this unit as the receiver of a Shoot Here command. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShortCircuit`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ShortCircuit`](Engine_StatusAndPassiveKeys.md#object-shortcircuit) | Integer / Object | The number of stacks of the ShortCircuit status effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `ShowText`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ShowText` | String | Specifies the localization key for a popup text displayed on the target. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SkipFirstRounds`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_chance` | Integer | The percentage chance that the first round is skipped. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `SlotMachineRollPool`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SlotResult_Explode`](Engine_LogicKeys.md#object-slotresult_explode) | Integer / Object | The result of an explosion roll, or the weight of that result. | 2 ||
| [`SlotResult_Jackpot_Coins`](Engine_LogicKeys.md#object-slotresult_jackpot_coins) | Integer / Object | The result of a jackpot roll that spawns coins, or the weight of that result in the pool. | 2 ||
| [`SlotResult_Nothing`](Engine_LogicKeys.md#object-slotresult_nothing) | Integer / Object | The result of a nothing roll, or the weight of that result. | 1 ||
| [`SlotResult_RandomPickup`](Engine_LogicKeys.md#object-slotresult_randompickup) | Integer / Object | The result of a random pickup roll, or the weight of that result. | 1 ||

</details>


---

### `SmallHitExplosion`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SmallHitExplosion` | Integer | The number of small explosion VFX to spawn on hit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SmartMetronome`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 1 ||

</details>


---

### `SmellBlood`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SmellBlood`](Engine_StatusAndPassiveKeys.md#object-smellblood) | Integer / Object | If non-zero, activates the Smell Blood ability which reveals nearby injured units. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Snow`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Miscellaneous.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 13 ||
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 ||
| [`particles`](./Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 ||
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 ||
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 ||

</details>


---

### `SolarFlare`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 62 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 ||

</details>


---

### `SourceSwapsBackEndOfTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum | Specifies the ability ID to use to swap the source unit back at the end of the turn. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpecialGodRays`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`effects`](./Miscellaneous.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Big`](Characters_and_Bosses.md#object-big) | Object | Defines the 'Big' form, including its animation, attack, passives, and positional data. | 2 ||

</details>


---

### `SpecificInjury`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpecificInjury` | Equation | The stat (str, spd, int) to which a specific injury is applied, reducing that stat. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpewerAltGraphics`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Normal`](Characters_and_Bosses.md#object-normal) | Integer / Object | The normal form configuration, used as a baseline state for shape-shifting units. | 24 ||
| [`Fire`](Characters_and_Bosses.md#object-fire) | Integer / Object | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 6 ||
| [`FireFull`](Characters_and_Bosses.md#object-firefull) | Integer / Object | Defines the 'FireFull' form, a fully charged fire state with its own animation and visual combo. | 1 ||
| [`NormalFull`](Characters_and_Bosses.md#object-normalfull) | Integer / Object | As an object, defines the normal full form with a spit attack and conditional form change. As an integer, specifies alt graphics index. | 1 ||
| [`Tar`](Characters_and_Bosses.md#object-tar) | Integer / Object | If an integer, the number of tar stacks. If an object, the form state for the tar-covered unit. | 1 ||
| [`TarFull`](Characters_and_Bosses.md#object-tarfull) | Integer / Object | If an integer, the number of full tar stacks. If an object, the form state for the fully tar-covered unit. | 1 ||

</details>


---

### `SpiderInfested`
> Found in: *Abilities & Spells, Events & Encounters, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. | 18 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpitConsumed`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpitConsumed` | Integer | If non-zero, marks the object consumed by the Spit ability as having been used. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SpreadWater`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpreadWater` | Integer | If set to 1, causes the character to spread water onto adjacent tiles. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StackingFlowerTrail`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 3 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 ||

</details>


---

### `StackingSandstorm`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StackingSandstorm` | Integer | If non-zero, enables the stacking sandstorm mechanic which increases damage per stack. | 3 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StanceSwitchToMelee`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StanceSwitchToMelee` | Integer | If set, switches the source to melee stance. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StartDead`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StartDead` | Integer | The percentage chance that the character starts the battle already dead. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StartOffMap`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StartOffMap` | Integer | If 1, the unit begins the encounter off the map. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `StevenBolts`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StevenBolts` | Integer | The number of Steven Bolts (a special resource or charge) the unit has for a unique ability. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SurviveAt1HP`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SurviveAt1HP` | Integer | If 1, the unit survives a fatal hit with 1 HP instead of dying. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SwallowSmallCharacter`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SwallowSmallCharacter` | Integer | The percentage chance to swallow a smaller character on hit. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `SwapWeapon`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 ||

</details>


---

### `SwitchMusic`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

> **Referenced by:** [`TimeDelayStatusApplication`](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum | Specifies the music layer to switch to (e.g., 'event', 'battle', 'map'). | 6 ||
| [`new_song`](./Enums.md#enum-new_song) | Enum | Specifies the song to switch to; 'same' keeps the current song playing on the new layer. | 5 ||
| `crossfade_speed` | Integer | The duration in seconds for the crossfade transition between music tracks. | 1 ||

</details>


---

### `Switcheroo`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Switcheroo`](Engine_StatusAndPassiveKeys.md#object-switcheroo) | Integer / Object | The number of stacks of the Switcheroo status effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `T2CopyCat`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `T2CopyCat` | Integer | The number of T2 Clone copies created or applied to the target cat. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TVBotDisableAttack`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TVBotDisableAttack` | Integer | If set to 1, disables the TVBot's ability to attack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TVBotDisableSpells`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TVBotDisableSpells` | Integer | If set to 1, disables the TVBot's ability to use spells. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TVBotScreen`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 1 ||
| [`Dumb`](Characters_and_Bosses.md#object-dumb) | Integer / Object | Defines the 'Dumb' form, which can be either a numeric value or an object with passives that disable spells and turn off TV. | 1 ||
| `Fuck` | Integer | The number of times the TV bot screen displays the 'Fuck' message. | 1 ||
| [`Obey`](Characters_and_Bosses.md#object-obey) | Integer / Object | As an object, defines an obey form that disables attacks and reacts with TV off. As an integer, defines a value (e.g., weight or count). | 1 ||
| `Shit` | Integer | The number of times the TV bot screen displays the 'Shit' message. | 1 ||
| [`Stop`](Characters_and_Bosses.md#object-stop) | Integer / Object | If an integer, the number of turns the unit is stopped. If an object, the form configuration for the stopped state. | 1 ||

</details>


---

### `TagGreed`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TagGreed`](./Enums.md#enum-taggreed) | Enum | The tag of items that this unit will move towards to collect. | 12 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TagMetronome`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum | Specifies a tag (e.g., "musical") used to filter which abilities the Metronome effect can pick. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TakeExtraTurnEndOfRound`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TakeExtraTurnEndOfRound` | Integer | The number of extra turns taken at the end of the round. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Tall`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tall` | Integer | If set to 1, the character occupies a taller hitbox or sprite space. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Tangled`
> Found in: *Abilities & Spells, Events & Encounters, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum | Specifies an alternative art asset name to use for the status. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `TargetedMetronome`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TargetedMetronome` | Integer | The number of random targets hit by the Targeted Metronome effect. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Taunting`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Taunting` | Integer | The number of stacks of Taunting, which forces enemies to target the unit. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TeamCastAbility`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum | Specifies a tag that the target unit must have for the team cast to trigger. | 2 ||
| `same_orientation` | Boolean | If true, the team cast ability only triggers if the caster and target face the same direction. | 1 ||

</details>


---

### `TeleportBackAtTurnEnd`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum | Specifies the ability ID used to teleport the unit back to its starting position at turn end. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBackstab`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempBackstab` | Integer | The amount of temporary backstab bonus, typically as a percentage. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBackstabBleed`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempBackstabBleed` | Integer | The number of temporary Bleed status stacks applied on a backstab attack. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBackstabPiercing`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempBackstabPiercing` | Integer | The amount of temporary piercing added to backstab attacks. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempBackstabPoison`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempBackstabPoison` | Integer | The amount of temporary poison stacks applied with backstab attacks. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TempPassiveUntilSettled`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`Conditional_HasKnockback`](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#context-conditional_isphysicalattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | Defines the damage and effects applied back to a melee attacker upon being hit. | 20 ||

</details>


---

### `TempPenetrate`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempPenetrate` | Integer | The amount of temporary penetration applied to attacks. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TerminatorSkin`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`groups`](./Arrays.md#array-groups) | Array | Groups of actors that this skin applies to. | 1 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 1 ||

</details>


---

### `TileTrail_Ahead`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | Specifies the type of tile to place one tile ahead of the unit's movement. | 8 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TinkererBasicAttackSwitching`
> Found in: *Cat Classes, Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`innate_passives`](./Cat_Classes.md#context-innate_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum | The ability used for the craft action in the Tinkerer's basic attack switching. | 1 ||
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum | The ability used for the throw action in the Tinkerer's basic attack switching. | 1 ||

</details>


---

### `TintItem`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array / Integer | The amount or an array of values added to the event's advantage or item tint. | 1 ||
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum | Specifies the string aux value at which to ignore the tinting operation. | 1 ||
| [`mul`](./Arrays.md#array-mul) | Array | An array of three floats (RGB) used to multiply the item's tint color. | 1 ||

</details>


---

### `TireBehavior`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TireBehavior` | Integer | If set to 1, activates special tire-related behavior for the character. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TossTargetIsAggroTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TossTargetIsAggroTarget` | Integer | If set to 1, the toss target is the unit's current aggro target. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TossTargetIsNotInWater`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TossTargetIsNotInWater` | Integer | If set to 1, the toss target must not be in water terrain. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TrackAmountKilledByPlayer`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer) | Enum | Specifies the name of the counter used to track how many of this type the player has killed. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TradeLife`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TradeLife`](Engine_StatusAndPassiveKeys.md#object-tradelife) | Integer / Object | The amount of health life traded, or a template for a TradeLife ability. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TrailBlazer`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TrailBlazer` | Variable | The number of trail blazer stacks applied, or a string alias like 'mov'. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Trapper`
> Found in: *Characters & Bosses, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

> **Referenced by:** [`passives`](./Characters_and_Bosses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `cancel_movement` | Boolean | If true, the trapper cancels the trapped unit's movement. | 2 ||
| `pathfinding_avoidance` | Integer | The weight that makes other units avoid traversing this tile during pathfinding. | 2 ||
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 ||

</details>


---

### `TrueShot`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TrueShot` | Integer | The number of stacks of a buff that makes the unit's attacks unmissable. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TunnelVision`
> Found in: *Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`passives`](./Items_and_Equipment.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`crit_chance`](./Enums.md#enum-crit_chance) | Number | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 1 ||

</details>


---

### `TurnAround`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TurnAround` | Integer | The number of times the unit turns around. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TurnControlDelay`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TurnControlDelay`](./Enums.md#enum-turncontroldelay) | Number | Specifies the delay in seconds before the unit regains turn control. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `TurnRight`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TurnRight` | Integer | The number of times the unit turns to the right. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Uncontrollable`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Uncontrollable` | Integer | If non-zero, the unit becomes uncontrollable by the player. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Undead`
> Found in: *Characters & Bosses, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 50

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Undead` | Integer | If set, flags the unit as undead (e.g., 1) with associated mechanics. | 50 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UnlockOrientation`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `UnlockOrientation` | Integer | If 1, allows the unit to freely rotate or face any direction regardless of movement. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `UseAbility`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Items & Equipment, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 730 ||
| `respect_prime` | Boolean | If true, the ability will only be used if the unit is primed for it. | 1 ||

</details>


---

### `UseAbility_NonStack`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Specifies an ability to use on kill that does not stack with itself. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Vaporize`
> Found in: *Abilities & Spells, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 66

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 66 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeCorpse`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `VaporizeCorpse` | Integer | If set, vaporizes the target's corpse, preventing revival. | 36 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeCorpseFlipAdvantage`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`VaporizeCorpseFlipAdvantage`](./Arrays.md#array-vaporizecorpseflipadvantage) | Array | The number of stacks and probability of vaporizing a corpse to gain loot flip advantage. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeDice`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `VaporizeDice` | Integer | The number of dice vaporized. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeInanimate`
> Found in: *Abilities & Spells, Cat Mutations, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `VaporizeInanimate` | Integer | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 16 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VaporizeTarget`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `VaporizeTarget` | Integer | If non-zero, instantly destroys the target, leaving no corpse. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VisualFX`
> Found in: *Abilities & Spells, Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum | Specifies the name of the visual effect to play. | 27 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `VisualFlySwarm`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `VisualFlySwarm` | Number | If non-zero, enables the visual fly swarm effect on the unit. | 1 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WaggleClone`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`effects`](./Abilities_and_Spells.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cWaggle`](Abilities_and_Spells.md#object-cwaggle) | Object | Defines a clone variant of the Waggle unit with its own graphics and properties. | 2 ||
| [`cWaggle2x2`](Abilities_and_Spells.md#object-cwaggle2x2) | Object | Defines a larger 2x2 tile clone variant of the Waggle unit. | 2 ||
| [`cWaggle3x3`](Abilities_and_Spells.md#object-cwaggle3x3) | Object | Defines an even larger 3x3 tile clone variant of the Waggle unit. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `Wall`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Wall` | Integer | If 1, the unit is treated as an impassable wall. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Webbed`
> Found in: *Abilities & Spells, Cat Mutations, Events & Encounters, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Webbed`](./Arrays.md#array-webbed) | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 23 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Wet`
> Found in: *Items & Equipment, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Wet` | Integer | The number of stacks of the Wet status effect applied. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `WideBackstab`
> Found in: *Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `WideBackstab` | Integer | The additional width for backstab attacks, in tiles. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Windy`
> Found in: *Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

> **Referenced by:** [`ROOT`](./Miscellaneous.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ambient_sound`](./Enums.md#enum-ambient_sound) | Enum | The filename of the ambient sound loop played during this weather type. | 13 ||
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 ||
| [`particles`](./Arrays.md#array-particles) | Array | A list of particle system identifiers used to render the weather effects. | 1 ||
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 ||
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum | Determines which skybox background frame is displayed for this weather. | 1 ||

</details>


---

### `XIsConsumedCharacterMaxHP`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `XIsConsumedCharacterMaxHP` | Integer | Specifies the multiplier used to set X to the maximum HP of the consumed character. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsCountDeaths`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `XIsCountDeaths` | Integer | If set to 1, X is equal to the number of deaths in the match. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsFreeArmorSlots`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `XIsFreeArmorSlots` | Integer | The number of armor slots that are free (no cost) for the unit. | 14 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsIncreaseEachTurn`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `XIsIncreaseEachTurn` | Integer | Specifies the amount by which X increases each turn. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsLivingAlliesWithTag`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`XIsLivingAlliesWithTag`](./Enums.md#enum-xislivingallieswithtag) | Enum | Specifies the tag that living allies must have for this passive to affect them. | 10 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsLivingCharactersWithTag`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`XIsLivingCharactersWithTag`](./Enums.md#enum-xislivingcharacterswithtag) | Enum | Specifies the tag that living characters must have for this passive to affect them. | 4 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsRampAndReset`
> Found in: *Abilities & Spells, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `XIsRampAndReset` | Integer | If set to 1, X ramps up over time and resets after use; 0 disables this behavior. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `XIsSpellStormRampAndReset`
> Found in: *Abilities & Spells, Miscellaneous*


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

> **Referenced by:** [`bonus_passives`](./Abilities_and_Spells.md#context-bonus_passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reset_percent` | Integer | The percentage of the ramp-up value to reset to upon casting. | 1 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||

</details>


---

### `YOffset`
> Found in: *Abilities & Spells, Cat Mutations, Characters & Bosses, Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`YOffset`](./Enums.md#enum-yoffset) | Number | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---

### `Zombie`
> Found in: *Miscellaneous*

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Zombie` | Number | The number of stacks or value for the Zombie status. | 2 ||

> *Note: This entry has no own context block. The row above reflects how this identifier appears as a property key inside other contexts, not as a standalone structured block.*

</details>

---


---

## Auto-Discovered Objects


### Object: `cWaggle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `cWaggle2x2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

### Object: `cWaggle3x3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>
