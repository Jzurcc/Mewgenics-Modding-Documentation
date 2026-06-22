# Mewgenics Mod Developer Documentation: Master Schema Dictionary
This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.


> **Note on Math Equations:** In Mewgenics, many fields labeled as `Number` secretly support inline math equations (e.g. `mov + 5` or `max(str, int)`). However, because the base game never used equations for those fields, we cannot guarantee it. Fields that are *confirmed* to support equations are explicitly marked as [`Equation`](./Enums.md#enum-mathequation).

## Elite Buffs

### Context: `ROOT`

<details>
<summary><b>Click to View Properties</b></summary>

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `icon_frame` | Number | `500, 501, 502` |  |
| `passives` | [`Block`](./Elite_Buffs.md#context-passives) | `{ ... }` |  |
| `value` | Number | `1` |  |
| `unique` | Boolean | `true` |  |
| `specific_chapter` | Number | `2, 1, 3` |  |
| `minion_alt` | [`Enum/String`](./Enums.md#enum-minion_alt) | `SlightlyDepressing, SubUndying, SubTwin` |  |
| `rollable` | Boolean | `false` |  |
| `only_at_battle_start` | Boolean | `true` |  |
| `requires_corpse` | Boolean | `true` |  |
| `roll_limit` | Number | `2` |  |

</details>

---

### Context: `passives`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ROOT`](./Elite_Buffs.md#context-root)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `EliteTint` | [`Array`](./Arrays.md#array-elitetint) | `[ .4 .4 .4 ], [ .6 .6 .6 .50 ], red` |  |
| `EliteParticle` | [`Enum/String`](./Enums.md#enum-eliteparticle) | `SparkleBuff, Lava_Distortion, SpikeBuff` |  |
| `HealthMultiplier` | [`Enum/String`](./Enums.md#enum-healthmultiplier) | `.5, 1.5, .8` |  |
| `EliteFlatTint` | [`Array`](./Arrays.md#array-eliteflattint) | `[ 1.1 1.1 1.3 ], [ 1.1 1.1 1.1 ], [ 1.1 1.1 1 ]` |  |
| `NonStackingShield` | Number | `7, 5, 3` |  |
| `SizeScale` | Number | `1.2, .8, .75` |  |
| `StatusEachRoundBegin` | [`Block`](./Elite_Buffs.md#context-statuseachroundbegin) | `{ ... }` |  |
| `DepressionAura` | [`Block`](./Elite_Buffs.md#context-depressionaura) | `{ ... }` |  |
| `DodgeChance` | Number | `10%` |  |
| `ElementImmune` | [`Enum/String`](./Enums.md#enum-elementimmune) | `Creep, Fire` |  |
| `MeleeRevengeDamage` | [`Block`](./Elite_Buffs.md#context-meleerevengedamage) | `{ ... }` |  |
| `TileTrail` | [`Enum/String`](./Enums.md#enum-tiletrail) | `FireTile, CreepTile` |  |
| `AddCorpseHealth` | Number | `-999999, 2` |  |
| `Brace` | Number | `2, 1` |  |
| `ChanceToRevive` | [`Block`](./Elite_Buffs.md#context-chancetorevive) | `{ ... }` |  |
| `CritChanceUp` | Number | `10` |  |
| `DamageNeighborsAfterMove` | [`Block`](./Elite_Buffs.md#context-damageneighborsaftermove) | `{ ... }` |  |
| `DamageUp` | Number | `2` |  |
| `ExtraDispersedTurns` | Number | `1, -1` |  |
| `GlobalManaBurnAura` | Number | `-1` |  |
| `InnateElement` | [`Enum/String`](./Enums.md#enum-innateelement) | `Fire` |  |
| `KineticSpikes` | Number | `1` |  |
| `LuckUp` | Number | `3` |  |
| `MinimumKnockbackFromAllDamage` | Number | `1` |  |
| `NonStackingDivineShield` | Number | `1` |  |
| `RevengeDamage` | [`Block`](./Elite_Buffs.md#context-revengedamage) | `{ ... }` |  |
| `SpawnOnBattleStart` | [`Block`](./Elite_Buffs.md#context-spawnonbattlestart) | `{ ... }` |  |
| `SpeedUp` | Number | `4` |  |
| `StatusEachTurnEnd` | [`Block`](./Elite_Buffs.md#context-statuseachturnend) | `{ ... }` |  |
| `StunImmunity` | Number | `1` |  |
| `Thorns` | Number | `2, 1` |  |
| `AbilityDamageMultiplier` | Number | `1.5` |  |
| `AddStatusToBasicAttack` | [`Block`](./Elite_Buffs.md#context-addstatustobasicattack) | `{ ... }` |  |
| `AddUnfilledMaxHealth` | Number | `20` |  |
| `HealthRegenUp` | Number | `3` |  |
| `MoveTowardsDamageSource` | [`Enum/String`](./Enums.md#enum-movetowardsdamagesource) | `MoveOne` |  |
| `PermanentMadness` | Number | `1` |  |
| `ReflectProjectiles` | [`Block`](./Elite_Buffs.md#context-reflectprojectiles) | `{ ... }` |  |
| `RemoveExtraDispersedTurn` | Number | `1` |  |
| `SpawnOnDeath` | [`Enum/String`](./Enums.md#enum-spawnondeath) | `NonChampionFlySwarm` |  |
| `StatusEachRoundEnd` | [`Block`](./Elite_Buffs.md#context-statuseachroundend) | `{ ... }` |  |
| `StatusOnDie` | [`Block`](./Elite_Buffs.md#context-statusondie) | `{ ... }` |  |
| `StatusOnEnemyCastSpell` | [`Block`](./Elite_Buffs.md#context-statusonenemycastspell) | `{ ... }` |  |
| `StatusOnKill` | [`Block`](./Elite_Buffs.md#context-statusonkill) | `{ ... }` |  |
| `Trample` | Number | `3` |  |

</details>

---

### Context: `DepressionAura`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean | `false` |  |
| `range` | Number | `1, global` |  |
| `stacks` | Number | `1` |  |

</details>

---

### Context: `DamageNeighborsAfterMove`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `damage` | Number | `1` |  |
| `effects` | [`Block`](./Elite_Buffs.md#context-effects) | `{ ... }` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Electric ]` |  |
| `type` | [`Enum/String`](./Enums.md#enum-type) | `spell` |  |

</details>

---

### Context: `StatusEachRoundBegin`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number | `7, 5, 3` |  |

</details>

---

### Context: `ChanceToRevive`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `health` | Number | `50%` |  |
| `stacks` | Number | `100` |  |
| `statuses` | [`Block`](./Elite_Buffs.md#context-statuses) | `{ ... }` |  |

</details>

---

### Context: `effects`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Elite_Buffs.md#context-damageneighborsaftermove), [`MeleeRevengeDamage`](./Elite_Buffs.md#context-meleerevengedamage), [`RevengeDamage`](./Elite_Buffs.md#context-revengedamage)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Tarred` | Number | `1` |  |
| `VisualFXTile` | [`Enum/String`](./Enums.md#enum-visualfxtile) | `WaterConduct` |  |
| `Burn` | Number | `1` |  |

</details>

---

### Context: `MeleeRevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `knockback` | Number | `1` |  |
| `effects` | [`Block`](./Elite_Buffs.md#context-effects) | `{ ... }` |  |
| `elements` | [`Array`](./Arrays.md#array-elements) | `[ Fire ]` |  |

</details>

---

### Context: `SpawnOnBattleStart`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `object` | [`Enum/String`](./Enums.md#enum-object) | `twin` |  |
| `prevent_chain_tag` | [`Enum/String`](./Enums.md#enum-prevent_chain_tag) | `eb_twin` |  |

</details>

---

### Context: `RevengeDamage`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `effects` | [`Block`](./Elite_Buffs.md#context-effects) | `{ ... }` |  |

</details>

---

### Context: `StatusEachTurnEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `NonStackingDivineShield` | Number | `1` |  |

</details>

---

### Context: `StatusOnEnemyCastSpell`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |  |
| `HealthGain` | Number | `1` |  |

</details>

---

### Context: `StatusOnKill`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AllStatsUp` | Number | `1` |  |
| `HealthGain` | Number | `4` |  |

</details>

---

### Context: `statuses`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Elite_Buffs.md#context-chancetorevive)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Zombie` | Number | `1` |  |

</details>

---

### Context: `AddStatusToBasicAttack`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `Poison` | Number | `1` |  |

</details>

---

### Context: `ReflectProjectiles`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `self_damage` | Number | `2` |  |

</details>

---

### Context: `StatusEachRoundEnd`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `AddRandomEliteBuff` | Number | `1` |  |

</details>

---

### Context: `StatusOnDie`

<details>
<summary><b>Click to View Properties</b></summary>

> **Referenced by:** [`passives`](./Elite_Buffs.md#context-passives)

| Property Key | Type | Example | Definition |
| :--- | :--- | :--- | :--- |
| `StackingSandstorm` | Number | `1` |  |

</details>

---

