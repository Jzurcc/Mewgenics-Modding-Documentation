# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Cat Mutations

> **Associated Files:** `data/mutations/`


### Object: `ROOT`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 489

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2985 |  |
| [`desc`](./Strings.md#string-desc) | Enum | Specifies the localized description string for the item or ability. | 2423 |  |
| `shield` | Enum / Integer | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 191 |  |
| `cha` | Enum / Integer | The Charisma stat value or modifier. | 89 |  |
| `con` | Enum / Integer | The Constitution stat value or modifier. | 79 |  |
| `spd` | Enum / Integer | The Speed stat value or modifier. | 78 |  |
| `int` | Enum / Integer | The Intelligence stat value or modifier. | 66 |  |
| `lck` | Enum / Integer | The Luck stat value or modifier. | 53 |  |
| `str` | Enum / Integer | The Strength stat value or modifier. | 45 |  |
| `dex` | Enum / Integer | The Dexterity stat value or modifier. | 30 |  |
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 20 |  |
| `speed` | Array / Number | The speed of the projectile or move, can be a value or a range. | 19 |  |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 7 |  |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 7 |  |

</details>

---

### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 284


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#context-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#context-passivewhilehasstatus), [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2039 |  |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 133 ||
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 94 | 1 |
| [`Trample`](./Enums.md) | Integer | The amount of bonus damage dealt when moving through an enemy. | 88 | 3 |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 65 | 2 |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | Defines the damage and effects applied back to a melee attacker upon being hit. | 59 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 52 | 2 |
| [`StatusEachTurnEnd`](#object-statuseachturnend) | Object | Specifies status effects applied to the unit at the end of each of its turns. | 49 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object | An object containing status effects or passives applied to the unit when the battle ends. | 45 ||
| [`ElementImmune`](./Enums.md) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 39 | Ice |
| [`CounterAttack`](#object-counterattack) | Object | Specifies the ability used when the unit counterattacks after being hit. | 34 ||
| [`StatusImmunity`](./Enums.md) | Array | A list of status effect names the unit is immune to. | 34 | [Freeze] |
| [`StatusOnKill`](#object-statusonkill) | Object | Specifies status effects or actions triggered when the unit kills an enemy. | 29 ||
| [`StatusOnTookDamage`](#object-statusontookdamage) | Object | Specifies status effects or actions triggered when the unit takes damage. | 29 ||
| [`SpawnThingOnDamage`](#object-spawnthingondamage) | Object | Specifies an object that spawns on the tile when the unit takes damage. | 28 ||
| [`AbilityReaction`](./Enums.md) | Enum | Specifies the ability used as a reaction when the unit is targeted by an ability. | 23 | SkunkTail |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 21 | 2 |
| [`AddMovement`](./Enums.md) | Integer | The amount of bonus movement points added to the unit's base movement. | 20 | 1 |
| [`StatusEachTurnBegin`](#object-statuseachturnbegin) | Object | Specifies status effects applied to the unit at the start of each of its turns. | 18 ||
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 16 | 5 |
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 15 | 1 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 15 | 1 |
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object | An object defining the damage and effects that trigger when the unit is attacked. | 15 ||
| [`SpawnEachTurn`](#object-spawneachturn) | Object | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 15 ||
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 14 | 2 |
| [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | 1 |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 14 | 2 |
| [`WaterWalk`](./Enums.md) | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 14 | 1 |
| [`AddManaRegen`](./Enums.md) | Integer | The flat amount of mana regenerated per turn. | 13 | 1 |
| [`MulticlassLevelUp`](./Enums.md) | Enum | Specifies the class that this unit gains a level in when multiclassing. | 12 | Hunter |
| [`ReflectProjectiles`](./Enums.md) | Integer | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 12 | 10 |
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 11 | 2 |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform per turn. | 11 | 2 |
| [`MoveWhenDamaged`](#object-movewhendamaged) | Object | Defines movement behavior when the unit takes damage, such as weights and move ability. | 11 ||
| [`ReplaceBasicMove`](./Enums.md) | Enum | Specifies an alternative movement ability that replaces the unit's default move. | 11 | ToadJump_BasicMove |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls the unit gets when leveling up. | 10 | 1 |
| [`BackstabImmunity`](./Enums.md) | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 9 | 1 |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 9 | 2 |
| [`DepressionAura`](./Enums.md) | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 9 | 1 |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 9 | 20 |
| [`PoisonThorns`](./Enums.md) | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 9 | 2 |
| [`StatusOnDie`](#object-statusondie) | Object | Specifies status effects or actions triggered when the unit dies. | 8 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 |
| [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 7 | Ice |
| [`AddInitiative`](./Enums.md) | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 7 | -20 |
| [`AlphaTurns`](./Enums.md) | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 7 | 1 |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 7 | [3] |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 7 | 1 |
| [`StatusOnEndMove`](#object-statusonendmove) | Object | Specifies status effects or actions triggered when the unit finishes moving. | 7 ||
| [`AddDamageToElementDamage`](#object-adddamagetoelementdamage) | Object | Defines additional damage of a specific element added to the unit's attacks. | 6 ||
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 6 | 10 |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 6 | 1 |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 6 | 1 |
| [`Quivered`](./Enums.md) | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 6 | [0.1] |
| [`SpawnOnBattleStartRandomEmptyTile`](#object-spawnonbattlestartrandomemptytile) | Object | Specifies an object that spawns on a random empty tile at the start of battle. | 6 ||
| [`StatusOnTookDamageFromAbility`](#object-statusontookdamagefromability) | Object | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 6 ||
| [`YOffset`](./Enums.md) | Number | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 | .25 |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's melee attacks. | 5 | 1 |
| [`ClassManaCostReduction`](#object-classmanacostreduction) | Object | Defines a reduction in mana cost for abilities of a specific class. | 5 ||
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 5 | 1 |
| [`StatusIfUnusedMovePoints`](#object-statusifunusedmovepoints) | Object | Specifies status effects applied if the unit ends its turn with unused movement points. | 5 ||
| [`AddKnockbackDamage`](./Enums.md) | Integer | The amount of additional knockback damage applied. | 4 | 1 |
| [`AddTemporaryEffectsToBasicAttack`](#object-addtemporaryeffectstobasicattack) | Object | A container object that lists temporary status effects applied to the unit's basic attack. | 4 ||
| [`BoostWeaponDamage`](./Enums.md) | Integer | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 4 | 1 |
| [`ChanceToBackflip`](#object-chancetobackflip) | Object | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 ||
| [`EquipTemporaryItem`](./Enums.md) | Enum | Specifies which temporary item is equipped. | 4 | WaterBottle_Full |
| [`PassiveWhenAffectedByElement`](#object-passivewhenaffectedbyelement) | Object | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 4 ||
| [`StatusEveryXSpellCasts`](#object-statuseveryxspellcasts) | Object | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 4 ||
| [`StatusOnAllyCatDeath`](#object-statusonallycatdeath) | Object | An object listing status effects applied to the unit when an allied cat dies. | 4 ||
| [`StatusOnCastSpell`](#object-statusoncastspell) | Object | An object listing status effects applied to the unit whenever it casts a spell. | 4 ||
| [`AbilityWhenTaggedCharacterMovesNear`](#object-abilitywhentaggedcharactermovesnear) | Object | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 3 ||
| [`AddStatusToBasicMeleeAttack`](#object-addstatustobasicmeleeattack) | Object | An object listing status effects applied by the unit's basic melee attack. | 3 ||
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | [2] |
| [`SpawnExtraThingsOnBattleStart`](#object-spawnextrathingsonbattlestart) | Object | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 3 ||
| [`StatusOnEatFood`](#object-statusoneatfood) | Object | An object listing status effects applied to the unit when it eats food. | 3 ||
| [`CanRemoveCursedItems`](./Enums.md) | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 2 | 1 |
| [`FreePathfindElement`](./Enums.md) | Enum | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 2 | Water |
| [`MoveAwayFromDamageSource`](./Enums.md) | Enum | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 2 | BasicJump |
| [`PassiveWhenAtFullMana`](#object-passivewhenatfullmana) | Object | An object listing passive effects that are active only while the unit's mana is full. | 2 ||
| [`PassiveWhileHasStatus`](#object-passivewhilehasstatus) | Object | An object containing `status` and `passives` that grants the listed passives while the unit has the specified status. | 2 ||
| [`PoopWhenHit`](./Enums.md) | Enum | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 2 | Poop |
| [`StatusKilledCharacters`](#object-statuskilledcharacters) | Object | An object listing status effects applied to the unit when it kills a character. | 2 ||
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Object | The number of backflip charges, or an object defining its ability. | 1 ||
| [`BasicAttackCantMiss`](./Enums.md) | Integer | If nonzero, the unit's basic attack cannot miss. | 1 | 1 |
| [`BlacklistPickupType`](./Enums.md) | Enum | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 1 | catnip |
| [`Blind`](./Enums.md) | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 1 | [.10] |
| [`ConjureBonusAbility`](./Enums.md) | Enum | Specifies the name of the bonus ability to conjure. | 1 | random |
| [`DisableAbilitiesWithTag`](./Enums.md) | Enum | Specifies a tag that disables any ability with that tag on the unit. | 1 | consumable |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 1 | 0 |
| [`MakeBasicAttackPull`](./Enums.md) | Integer | If nonzero, the unit's basic attack pulls the target closer. | 1 | 1 |
| [`ShowHiddenThings`](./Enums.md) | Integer | If nonzero, reveals hidden objects or tiles on the map. | 1 | 1 |
| [`Slow`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | [.1] |
| [`SpawnOnDowned`](./Enums.md) | Enum | Specifies the character or object spawned when the unit is downed. | 1 | CharmedFly |
| [`StatusEachRoundEnd`](#object-statuseachroundend) | Object | An object listing status effects applied to the unit at the end of each round. | 1 ||
| [`Vegan`](./Enums.md) | Integer | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 1 | 1 |

</details>

---

### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 52


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 205 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 30 | [3] |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 29 | 1 |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is pushed away from the source on hit. | 24 | 2 |
| [`Burn`](./Enums.md) | Integer | The amount of Burn applied, either as a fixed number or a formula string. | 16 | 1 |
| [`Fear`](./Enums.md) | Array | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 13 | [.15] |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 12 | 2 |
| [`ChangeTile`](./Enums.md) | Enum | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 10 | WaterTile |
| [`Slow`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 10 | [.1] |
| [`Stun`](./Enums.md) | Array | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 8 | [.05] |
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 7 | [2] |
| [`Freeze`](./Enums.md) | Array | The amount of freeze stacks applied, or an [stacks, probability] array. | 4 | [0.15] |
| [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 4 | 1 |
| [`SoulLink`](./Enums.md) | Integer | The number of soul link stacks applied. | 4 | 1 |
| [`Charmed`](./Enums.md) | Array | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 3 | [.15] |
| [`VisualFXTile`](./Enums.md) | Enum | Specifies the name of the visual effect to play on the target tile. | 2 | fx_windSpell |
| [`FaceAway`](./Enums.md) | Integer | If set, forces the target to face away from the source. | 1 | 1 |
| [`FlatLeech`](./Enums.md) | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 1 | 1 |
| [`Immobile`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | [.05] |
| [`Instakill`](./Enums.md) | Array | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | [25] |
| [`Petrify`](./Enums.md) | Array | The amount of petrify stacks applied, or an [stacks, probability] array. | 1 | [.05] |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 1 ||
| [`VaporizeInanimate`](./Enums.md) | Integer | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 1 | 1 |
| [`Webbed`](./Enums.md) | Array | The amount of webbed stacks applied, or an [stacks, probability] array. | 1 | [.1] |

</details>

---

### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 12


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 18 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 18 ||
| [`passives`](#object-passives) | Object | A container object listing passive effects granted to the unit. | 18 ||

</details>

---

### Object: `effects`
### Object: `effects`

**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 10


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1695 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 750 |
| [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 37 | [2] |
| [`Fear`](./Enums.md) | Array | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 31 | [.15] |
| [`Blind`](./Enums.md) | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 24 | [.10] |
| [`Charmed`](./Enums.md) | Array | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 22 | [.15] |
| [`Petrify`](./Enums.md) | Array | The amount of petrify stacks applied, or an [stacks, probability] array. | 15 | [.05] |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 14 ||

</details>

---

### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 9


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 31 ||
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 29 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 29 |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 8 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 5 ||

</details>

---

### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 70 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 49 |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 47 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 43 ||
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 24 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 22 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 10 ||
| [`Freeze`](./Enums.md) | Array | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | [0.15] |
| [`Immobile`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | [.05] |

</details>

---

### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 7


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 38 ||
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 20 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 12 ||

</details>

---

### Object: `AddStatusToBasicMeleeAttack`


**Definition:** Examples: `{ ... }`  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 ||
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 2 | [3] |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is pushed away from the source on hit. | 2 | 2 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`Immobile`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | [.05] |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 ||

</details>

---

### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 6


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 38 ||
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 8 | 2 |
| [`ChangeTilesUnder`](./Enums.md) | Enum | The tile type to change the ground tiles under the target to. | 2 | GlassTile |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | 1 |

</details>

---

### Object: `StatusEachTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to each turn begin.  
**Total Count:** 5


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 24 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 |
| [`Quivered`](./Enums.md) | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | [0.1] |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | 1 |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 1 | 20 |
| [`MoveQuivered`](./Enums.md) | Array | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | [0.1] |

</details>

---

### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#context-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#context-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 33 ||
| [`Shield`](./Enums.md) | Integer | The amount of shield granted to the source, absorbing incoming damage. | 12 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 10 | 2 |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 9 | 1 |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 9 | 1 |
| [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 8 | [3] |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 8 | 2 |
| [`Weakness`](./Enums.md) | Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 8 | 1 |
| [`Blind`](./Enums.md) | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | [.10] |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 6 | 1 |
| [`Burn`](./Enums.md) | Integer | The amount of Burn applied, either as a fixed number or a formula string. | 5 | 1 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 5 | 2 |

</details>

---

### Object: `SpawnEachTurn`


**Definition:** Applies or references the 'SpawnEachTurn' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 22 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 20 ||
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 ||

</details>

---

### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 4


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root), [`passives`](./Cat_Mutations.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 55 ||
| [`Shield`](./Enums.md) | Integer | The amount of shield granted to the source, absorbing incoming damage. | 5 | 1 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 5 |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 3 | 2 |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 2 | 1 |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 1 | 2 |
| [`RandomStatDown`](./Enums.md) | Integer | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 1 | 1 |

</details>

---

### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state.  
**Total Count:** 3


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 11 ||
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 10 ||

</details>

---

### Object: `Conditional_RandomChance`


**Definition:** Conditional trigger: Executes nested logic based on a flat percentage random roll.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#context-statuskilledcharacters)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 4 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 |
| [`AutoReanimate`](./Enums.md) | Integer | The percentage chance for the unit to automatically reanimate upon death. | 2 | 50 |

</details>

---

### Object: `StatusEveryXSpellCasts`


**Definition:** Applies or references the 'StatusEveryXSpellCasts' effect/state.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 2 | 2 |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | 4 |

</details>

---

### Object: `StatusKilledCharacters`


**Definition:** Event Trigger: Applies nested statuses to killed characters.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 52 ||
| [`FindItemFromPool`](./Enums.md) | Enum | Specifies the loot pool from which to find an item, with an optional chance. | 8 | consumables |
| [`PermanentIntelligence`](./Enums.md) | Integer | The permanent amount of intelligence added or removed. | 3 | 1 |

</details>

---

### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>

---

### Object: `StatusOnTookDamageFromAbility`


**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 2


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 2 ||
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |

</details>

---

### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 ||
| `range` | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 5 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 5 ||

</details>

---

### Object: `AddDamageToElementDamage`


**Definition:** Applies or references the 'AddDamageToElementDamage' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 9 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 9 ||

</details>

---

### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 4 ||

</details>

---

### Object: `BackflipWhenTargeted`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 7 ||

</details>

---

### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 6 ||

</details>

---

### Object: `ClassManaCostReduction`


**Definition:** Applies or references the 'ClassManaCostReduction' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 7 ||
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 6 ||

</details>

---

### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 1 | 2 |

</details>

---

### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#context-statusonendmove)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 37 ||
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 37 | |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 28 ||
| [`ChangeTilesUnder`](./Enums.md) | Enum | The tile type to change the ground tiles under the target to. | 1 | GlassTile |

</details>

---

### Object: `CounterAttack`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 ||
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||

</details>

---

### Object: `KnockUpAndAway`


**Definition:** Displaces the target vertically and horizontally away from the source.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#context-addstatustobasicmeleeattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 24 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 22 ||

</details>

---

### Object: `MoveWhenDamaged`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Enums.md#enum-weights) | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. | 9 ||
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 2 ||

</details>

---

### Object: `PassiveWhenAtFullMana`


**Definition:** State Trigger: Grants nested passives when at full mana.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | 2 |

</details>

---

### Object: `PassiveWhileHasStatus`


**Definition:** Passive: Activates only while the character has the specified status.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 6 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [`passives`](#object-passives) | Object | A container object listing passive effects granted to the unit. | 6 ||

</details>

---

### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 31 ||
| [`object`](./Enums.md#enum-object) | Array / Enum | Specifies the object or unit to be spawned. | 23 ||

</details>

---

### Object: `StatusEachRoundEnd`


**Definition:** Applies or references the 'StatusEachRoundEnd' effect/state.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`UseAbility`](./Enums.md) | Enum | The name of the ability the target is forced to use. | 1 | Spit |

</details>

---

### Object: `StatusEveryXSpellCastsEachTurn`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 ||
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | 2 |

</details>

---

### Object: `StatusIfDidntMove`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 ||
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 1 | 2 |

</details>

---

### Object: `StatusIfUnusedMovePoints`


**Definition:** Event Trigger: Applies nested statuses to if unused move points.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`ManaGain`](./Enums.md) | Integer | The amount of mana restored to the source, which can be an expression. | 2 | 3 |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 |

</details>

---

### Object: `StatusOnAllyCatDeath`


**Definition:** Event Trigger: Applies nested statuses when ally cat death.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 ||
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | 2 |

</details>

---

### Object: `StatusOnCastSpell`


**Definition:** Event Trigger: Applies nested statuses when cast spell.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 ||
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 4 | 2 |

</details>

---

### Object: `StatusOnDie`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 ||
| [`ScatterCoins`](./Enums.md) | Array / Integer | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 | [.5] |

</details>

---

### Object: `StatusOnEatFood`


**Definition:** Event Trigger: Applies nested statuses when eat food.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 ||
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | 2 |

</details>

---

### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1


<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 ||
| [`RangeUp`](./Enums.md) | Integer | The number of stacks of bonus attack range applied. | 1 | 1 |

</details>

---


<details>
<summary><b>Conditional_RandomChance</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 ||

</details>

<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 ||

</details>

<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 ||

</details>
