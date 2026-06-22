# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Elite Buffs

### Context: `ROOT`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition | Count (X/54) |
| :--- | :--- | :--- | :--- |
| `icon_frame` | Number |  | 54 |
| [`passives`](./Elite_Buffs.md#context-passives) | Block |  | 54 |
| `value` | Number |  | 54 |
| `unique` | Boolean |  | 36 |
| `specific_chapter` | Number |  | 8 |
| [`minion_alt`](./Enums.md#enum-minion_alt) | Enum/String |  | 5 |
| `rollable` | Boolean |  | 5 |
| `only_at_battle_start` | Boolean |  | 2 |
| `requires_corpse` | Boolean |  | 2 |
| `roll_limit` | Number |  | 2 |

</details>

---

### Context: `passives`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Elite_Buffs.md#context-root)

| Property Key | Type | Definition | Count (X/30) |
| :--- | :--- | :--- | :--- |
| [`EliteTint`](./Arrays.md#array-elitetint) | Array |  | 30 |
| [`EliteParticle`](./Enums.md#enum-eliteparticle) | Enum/String |  | 19 |
| `HealthMultiplier` | Number |  | 15 |
| [`EliteFlatTint`](./Arrays.md#array-eliteflattint) | Array |  | 11 |
| `NonStackingShield` | Number |  | 8 |
| `SizeScale` | Number |  | 8 |
| [`StatusEachRoundBegin`](./Elite_Buffs.md#context-statuseachroundbegin) | Block |  | 8 |
| [`DepressionAura`](./Elite_Buffs.md#context-depressionaura) | Block |  | 4 |
| `DodgeChance` | Number |  | 3 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum/String |  | 3 |
| [`MeleeRevengeDamage`](./Elite_Buffs.md#context-meleerevengedamage) | Block |  | 3 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum/String |  | 3 |
| `AddCorpseHealth` | Number |  | 2 |
| `Brace` | Number |  | 2 |
| [`ChanceToRevive`](./Elite_Buffs.md#context-chancetorevive) | Block |  | 2 |
| `CritChanceUp` | Number |  | 2 |
| [`DamageNeighborsAfterMove`](./Elite_Buffs.md#context-damageneighborsaftermove) | Block |  | 2 |
| `DamageUp` | Number |  | 2 |
| `ExtraDispersedTurns` | Number |  | 2 |
| `GlobalManaBurnAura` | Number |  | 2 |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum/String |  | 2 |
| `KineticSpikes` | Number |  | 2 |
| `LuckUp` | Number |  | 2 |
| `MinimumKnockbackFromAllDamage` | Number |  | 2 |
| `NonStackingDivineShield` | Number |  | 2 |
| [`RevengeDamage`](./Elite_Buffs.md#context-revengedamage) | Block |  | 2 |
| [`SpawnOnBattleStart`](./Elite_Buffs.md#context-spawnonbattlestart) | Block |  | 2 |
| `SpeedUp` | Number |  | 2 |
| [`StatusEachTurnEnd`](./Elite_Buffs.md#context-statuseachturnend) | Block |  | 2 |
| `StunImmunity` | Number |  | 2 |
| `Thorns` | Number |  | 2 |
| `AbilityDamageMultiplier` | Number |  | 1 |
| [`AddStatusToBasicAttack`](./Elite_Buffs.md#context-addstatustobasicattack) | Block |  | 1 |
| `AddUnfilledMaxHealth` | Number |  | 1 |
| `HealthRegenUp` | Number |  | 1 |
| [`MoveTowardsDamageSource`](./Enums.md#enum-movetowardsdamagesource) | Enum/String |  | 1 |
| `PermanentMadness` | Number |  | 1 |
| [`ReflectProjectiles`](./Elite_Buffs.md#context-reflectprojectiles) | Block |  | 1 |
| `RemoveExtraDispersedTurn` | Number |  | 1 |
| [`SpawnOnDeath`](./Enums.md#enum-spawnondeath) | Enum/String |  | 1 |
| [`StatusEachRoundEnd`](./Elite_Buffs.md#context-statuseachroundend) | Block |  | 1 |
| [`StatusOnDie`](./Elite_Buffs.md#context-statusondie) | Block |  | 1 |
| [`StatusOnEnemyCastSpell`](./Elite_Buffs.md#context-statusonenemycastspell) | Block |  | 1 |
| [`StatusOnKill`](./Elite_Buffs.md#context-statusonkill) | Block |  | 1 |
| `Trample` | Number |  | 1 |

</details>

---

### Context: `StatusEachRoundBegin`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/8) |
| :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number |  | 8 |

</details>

---

### Context: `DepressionAura`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/4) |
| :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean |  | 4 |
| `range` | Number |  | 4 |
| `stacks` | Number |  | 4 |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `health` | Number |  | 2 |
| `stacks` | Number |  | 2 |
| [`statuses`](./Elite_Buffs.md#context-statuses) | Block |  | 2 |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `damage` | Number |  | 2 |
| [`effects`](./Elite_Buffs.md#context-effects) | Block |  | 2 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 2 |
| [`type`](./Enums.md#enum-type) | Enum/String |  | 2 |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `knockback` | Number |  | 2 |
| [`effects`](./Elite_Buffs.md#context-effects) | Block |  | 1 |
| [`elements`](./Arrays.md#array-elements) | Array |  | 1 |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`effects`](./Elite_Buffs.md#context-effects) | Block |  | 2 |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Enum/String |  | 2 |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum/String |  | 2 |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `NonStackingDivineShield` | Number |  | 2 |

</details>

---

### Context: `effects`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Elite_Buffs.md#context-damageneighborsaftermove), [`MeleeRevengeDamage`](./Elite_Buffs.md#context-meleerevengedamage), [`RevengeDamage`](./Elite_Buffs.md#context-revengedamage)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Tarred` | Number |  | 2 |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum/String |  | 2 |
| `Burn` | Number |  | 1 |

</details>

---

### Context: `statuses`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Elite_Buffs.md#context-chancetorevive)

| Property Key | Type | Definition | Count (X/2) |
| :--- | :--- | :--- | :--- |
| `Zombie` | Number |  | 2 |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `Poison` | Number |  | 1 |

</details>

---

### Context: `ReflectProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number |  | 1 |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AddRandomEliteBuff` | Number |  | 1 |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `StackingSandstorm` | Number |  | 1 |

</details>

---

### Context: `StatusOnEnemyCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number |  | 1 |
| `HealthGain` | Number |  | 1 |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Definition | Count (X/1) |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number |  | 1 |
| `HealthGain` | Number |  | 1 |

</details>

---

