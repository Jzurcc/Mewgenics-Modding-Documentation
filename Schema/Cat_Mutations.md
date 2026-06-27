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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2985 | `passives`<br>`class`<br>`tag` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 2423 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`shield`](./Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 191 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 89 | `+1`<br>`-1`<br>`-2` |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 79 | `-1`<br>`-2`<br>`-3` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 78 | `-1`<br>`-10`<br>`-2` |
| [`int`](./Enums.md#enum-int) | Enum / Integer  | The Intelligence stat value or modifier. | 66 | `-1`<br>`-10`<br>`-2` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer  | The Luck stat value or modifier. | 53 | `-1`<br>`-2`<br>`-3` |
| [`str`](./Enums.md#enum-str) | Enum / Integer  | The Strength stat value or modifier. | 45 | `-1`<br>`-2`<br>`-3` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer  | The Dexterity stat value or modifier. | 30 | `-1`<br>`-2`<br>`-3` |
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 20 | `0`<br>`1`<br>`2` |
| [`speed`](./Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 19 | `-30`<br>`-4`<br>`.5` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 7 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`attack`](./Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 7 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2039 | `passives`<br>`class`<br>`tag` |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 133 | `{ . . . }` |
| [`Brace`](./Enums.md) | Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 94 | `1`<br>`10`<br>`2` |
| [`Trample`](./Enums.md) | Integer | The amount of bonus damage dealt when moving through an enemy. | 88 | `1`<br>`3`<br>`4` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 65 | `1`<br>`2`<br>`3` |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 59 | `{ . . . }` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 52 | `1`<br>`2`<br>`3` |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#object-statuseachturnend) | Object  | Specifies status effects applied to the unit at the end of each of its turns. | 49 | `{ . . . }` |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 45 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 39 | `Creep`<br>`Electric`<br>`Fire` |
| [`CounterAttack`](./Passives_and_Statuses.md#object-counterattack) | Object  | Specifies the ability used when the unit counterattacks after being hit. | 34 | `{ . . . }` |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array  | A list of status effect names the unit is immune to. | 34 | `Burn`<br>`Poison`<br>`Tarred` |
| [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 29 | `{ . . . }` |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage) | Object  | Specifies status effects or actions triggered when the unit takes damage. | 29 | `{ . . . }` |
| [`SpawnThingOnDamage`](./Passives_and_Statuses.md#object-spawnthingondamage) | Object  | Specifies an object that spawns on the tile when the unit takes damage. | 28 | `{ . . . }` |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 23 | `AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 21 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`AddMovement`](./Enums.md) | Integer | The amount of bonus movement points added to the unit's base movement. | 20 | `-1`<br>`-2`<br>`1` |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 18 | `{ . . . }` |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 16 | `1`<br>`10`<br>`100` |
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 15 | `1`<br>`10`<br>`2` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 15 | `1`<br>`2`<br>`3` |
| [`RevengeDamage`](./Passives_and_Statuses.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 15 | `{ . . . }` |
| [`SpawnEachTurn`](./Passives_and_Statuses.md#object-spawneachturn) | Object  | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 15 | `{ . . . }` |
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 14 | `-999`<br>`-999999`<br>`100` |
| [`AllStatsUp`](./Enums.md) | Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | `-1`<br>`-2`<br>`1` |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 14 | `10%`<br>`15%`<br>`2%` |
| [`WaterWalk`](./Enums.md) | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 14 | `1` |
| [`AddManaRegen`](./Enums.md) | Integer | The flat amount of mana regenerated per turn. | 13 | `1`<br>`2`<br>`3` |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum  | Specifies the class that this unit gains a level in when multiclassing. | 12 | `Butcher`<br>`Druid`<br>`Fighter` |
| [`ReflectProjectiles`](./Enums.md) | Integer | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 12 | `1`<br>`10%`<br>`100%` |
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 11 | `1`<br>`2`<br>`3` |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform per turn. | 11 | `1`<br>`2` |
| [`MoveWhenDamaged`](./Passives_and_Statuses.md#object-movewhendamaged) | Object  | Defines movement behavior when the unit takes damage, such as weights and move ability. | 11 | `{ . . . }` |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum  | Specifies an alternative movement ability that replaces the unit's default move. | 11 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls the unit gets when leveling up. | 10 | `1`<br>`2`<br>`3` |
| [`BackstabImmunity`](./Enums.md) | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 9 | `1` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 9 | `1`<br>`2`<br>`3` |
| [`DepressionAura`](./Enums.md) | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 9 | `1`<br>`2` |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 9 | `10`<br>`15`<br>`20` |
| [`PoisonThorns`](./Enums.md) | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 9 | `1`<br>`2`<br>`3` |
| [`StatusOnDie`](./Passives_and_Statuses.md#object-statusondie) | Object  | Specifies status effects or actions triggered when the unit dies. | 8 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 7 | `Electric`<br>`Fire`<br>`Gravity` |
| [`AddInitiative`](./Enums.md) | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 7 | `-10`<br>`-100`<br>`-20` |
| [`AlphaTurns`](./Enums.md) | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 7 | `-1`<br>`1` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 7 | `1`<br>`10`<br>`2` |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 7 | `-2`<br>`1`<br>`2` |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 7 | `{ . . . }` |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 6 | `{ . . . }` |
| [`DodgeChance_Status`](./Enums.md) | Integer | The flat percentage increase to dodge chance applied as a status effect. | 6 | `1`<br>`10`<br>`100` |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 6 | `1` |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 6 | `1`<br>`10`<br>`2` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`2`<br>`5` |
| [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile) | Object  | Specifies an object that spawns on a random empty tile at the start of battle. | 6 | `{ . . . }` |
| [`StatusOnTookDamageFromAbility`](./Passives_and_Statuses.md#object-statusontookdamagefromability) | Object  | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 6 | `{ . . . }` |
| [`YOffset`](./Enums.md) | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 | `-.18`<br>`.25`<br>`.35` |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's melee attacks. | 5 | `1`<br>`10`<br>`2` |
| [`ClassManaCostReduction`](./Passives_and_Statuses.md#object-classmanacostreduction) | Object  | Defines a reduction in mana cost for abilities of a specific class. | 5 | `{ . . . }` |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 5 | `1` |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#object-statusifunusedmovepoints) | Object  | Specifies status effects applied if the unit ends its turn with unused movement points. | 5 | `{ . . . }` |
| [`AddKnockbackDamage`](./Enums.md) | Integer | The amount of additional knockback damage applied. | 4 | `1`<br>`2`<br>`3` |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 4 | `{ . . . }` |
| [`BoostWeaponDamage`](./Enums.md) | Integer | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 4 | `1`<br>`2`<br>`5` |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 | `{ . . . }` |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum  | Specifies which temporary item is equipped. | 4 | `Bottles`<br>`ButcherHook_Temporary`<br>`FoodBig` |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 4 | `{ . . . }` |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#object-statuseveryxspellcasts) | Object  | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 4 | `{ . . . }` |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#object-statusonallycatdeath) | Object  | An object listing status effects applied to the unit when an allied cat dies. | 4 | `{ . . . }` |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#object-statusoncastspell) | Object  | An object listing status effects applied to the unit whenever it casts a spell. | 4 | `{ . . . }` |
| [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear) | Object  | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 3 | `{ . . . }` |
| [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#object-addstatustobasicmeleeattack) | Object  | An object listing status effects applied by the unit's basic melee attack. | 3 | `{ . . . }` |
| [`Confusion`](./Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`SpawnExtraThingsOnBattleStart`](./Passives_and_Statuses.md#object-spawnextrathingsonbattlestart) | Object  | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 3 | `{ . . . }` |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#object-statusoneatfood) | Object  | An object listing status effects applied to the unit when it eats food. | 3 | `{ . . . }` |
| [`CanRemoveCursedItems`](./Enums.md) | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 2 | `1` |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum  | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 2 | `Grass`<br>`Water` |
| [`MoveAwayFromDamageSource`](./Enums.md#enum-moveawayfromdamagesource) | Enum  | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 2 | `BasicJump`<br>`MoveOne` |
| [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#object-passivewhenatfullmana) | Object  | An object listing passive effects that are active only while the unit's mana is full. | 2 | `{ . . . }` |
| [`PassiveWhileHasStatus`](./Miscellaneous.md#object-passivewhilehasstatus) | Object  | An object containing `status` and `passives` that grants the listed passives while the unit has the specified status. | 2 | `{ . . . }` |
| [`PoopWhenHit`](./Enums.md#enum-poopwhenhit) | Enum  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 2 | `Poop` |
| [`StatusKilledCharacters`](./Passives_and_Statuses.md#object-statuskilledcharacters) | Object  | An object listing status effects applied to the unit when it kills a character. | 2 | `{ . . . }` |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Object  | The number of backflip charges, or an object defining its ability. | 1 | `{ . . . }` |
| [`BasicAttackCantMiss`](./Enums.md) | Integer | If nonzero, the unit's basic attack cannot miss. | 1 | `1` |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum  | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 1 | `catnip`<br>`food` |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 1 | `-1`<br>`1`<br>`2` |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum  | Specifies the name of the bonus ability to conjure. | 1 | `Class`<br>`Colorless`<br>`Mage` |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum  | Specifies a tag that disables any ability with that tag on the unit. | 1 | `consumable`<br>`meat`<br>`musical` |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 1 | `0` |
| [`MakeBasicAttackPull`](./Enums.md) | Integer | If nonzero, the unit's basic attack pulls the target closer. | 1 | `1` |
| [`ShowHiddenThings`](./Enums.md) | Integer | If nonzero, reveals hidden objects or tiles on the map. | 1 | `1` |
| [`Slow`](./Arrays.md#array-slow) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | `-1`<br>`1`<br>`2` |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum  | Specifies the character or object spawned when the unit is downed. | 1 | `CharmedFly`<br>`CharmedKitten`<br>`CharmedSpookie` |
| [`StatusEachRoundEnd`](./Passives_and_Statuses.md#object-statuseachroundend) | Object  | An object listing status effects applied to the unit at the end of each round. | 1 | `{ . . . }` |
| [`Vegan`](./Enums.md) | Integer | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 1 | `1` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 205 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 | `Default`<br>`FormChange`<br>`Druid` | [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 30 | `1`<br>`10`<br>`2` |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 29 | `1`<br>`10`<br>`2` |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is pushed away from the source on hit. | 24 | `1`<br>`10`<br>`2` |
| [`Burn`](./Enums.md) | Integer | The amount of Burn applied, either as a fixed number or a formula string. | 16 | `1`<br>`10`<br>`2` |
| [`Fear`](./Arrays.md#array-fear) | Array  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 13 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 12 | `1`<br>`2`<br>`3` |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 10 | `BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Slow`](./Arrays.md#array-slow) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 10 | `-1`<br>`1`<br>`2` |
| [`Stun`](./Arrays.md#array-stun) | Array  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`2`<br>`3` |
| [`Confusion`](./Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 7 | `1`<br>`10`<br>`2` |
| [`Freeze`](./Arrays.md#array-freeze) | Array  | The amount of freeze stacks applied, or an [stacks, probability] array. | 4 | `1`<br>`2`<br>`[1 .01]` |
| [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 4 | `1`<br>`2`<br>`3` |
| [`SoulLink`](./Enums.md) | Integer | The number of soul link stacks applied. | 4 | `1` |
| [`Charmed`](./Arrays.md#array-charmed) | Array  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 3 | `1`<br>`2`<br>`3` |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum  | Specifies the name of the visual effect to play on the target tile. | 2 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| [`FaceAway`](./Enums.md) | Integer | If set, forces the target to face away from the source. | 1 | `1` |
| [`FlatLeech`](./Enums.md) | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 1 | `1`<br>`10`<br>`2` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| [`Instakill`](./Arrays.md#array-instakill) | Array  | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 1 | `25`<br>`50`<br>`999` |
| [`Petrify`](./Arrays.md#array-petrify) | Array  | The amount of petrify stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [`VaporizeInanimate`](./Enums.md) | Integer | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 1 | `1` |
| [`Webbed`](./Arrays.md#array-webbed) | Array  | The amount of webbed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .1]` |

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
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 18 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 18 | `passives`<br>`class`<br>`tag` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 18 | `{ . . . }` |

</details>


---


### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#context-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#context-revengedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1695 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 750 | `Default`<br>`FormChange`<br>`Druid` | [`Confusion`](./Enums.md) | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 37 | `1`<br>`10`<br>`2` |
| [`Fear`](./Arrays.md#array-fear) | Array  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 31 | `1`<br>`10`<br>`2` |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 24 | `-1`<br>`1`<br>`2` |
| [`Charmed`](./Arrays.md#array-charmed) | Array  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 22 | `1`<br>`2`<br>`3` |
| [`Petrify`](./Arrays.md#array-petrify) | Array  | The amount of petrify stacks applied, or an [stacks, probability] array. | 15 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 14 | `{ . . . }` |

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
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 31 | `damage_instance`<br>`spell`<br>`false` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 29 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 29 | `Default`<br>`FormChange`<br>`Druid` | [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 8 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 5 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>

---`damage_instance`<br>`spell`<br>`self_damage`


### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 70 | `damage_instance`<br>`spell`<br>`false` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 49 | `Default`<br>`FormChange`<br>`Druid` | [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 47 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 43 | `passives`<br>`class`<br>`tag` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 24 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 22 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 10 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`Freeze`](./Arrays.md#array-freeze) | Array  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |`damage_instance`<br>`spell`<br>`self_damage`

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
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 38 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 20 | `false`<br>`true` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 12 | `.02`<br>`.1`<br>`.15` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | `passives`<br>`class`<br>`tag` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`10`<br>`2` |
| [`Knockback`](./Enums.md) | Integer | The number of tiles the target is pushed away from the source on hit. | 2 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`Immobile`](./Enums.md) | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| [`KnockUpAndAway`](./Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 1 | `{ . . . }` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 38 | `passives`<br>`class`<br>`tag` |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 8 | `1`<br>`2`<br>`3` |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 2 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 24 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`Quivered`](./Enums.md) | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 1 | `10`<br>`15`<br>`20` |
| [`MoveQuivered`](./Arrays.md#array-movequivered) | Array  | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`[1, 0.1]` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 33 | `passives`<br>`class`<br>`tag` |
| [`Shield`](./Enums.md) | Integer | The amount of shield granted to the source, absorbing incoming damage. | 12 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 | `Default`<br>`FormChange`<br>`Druid` | [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 10 | `1`<br>`2`<br>`3` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 9 | `1`<br>`2`<br>`3` |
| [`Poison`](./Enums.md) | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 9 | `1`<br>`10`<br>`2` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 8 | `1`<br>`10`<br>`2` |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 8 | `1`<br>`2`<br>`3` |
| [`Weakness`](./Enums.md) | Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`2`<br>`3` |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 6 | `1`<br>`2`<br>`3` |
| [`Burn`](./Enums.md) | Integer | The amount of Burn applied, either as a fixed number or a formula string. | 5 | `1`<br>`10`<br>`2` |
| [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 5 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |

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
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 22 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 20 | `.02`<br>`.1`<br>`.15` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 55 | `passives`<br>`class`<br>`tag` |
| [`Shield`](./Enums.md) | Integer | The amount of shield granted to the source, absorbing incoming damage. | 5 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 5 | `Default`<br>`FormChange`<br>`Druid` | [`RandomStatUp`](./Enums.md) | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 3 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`IntelligenceUp`](./Enums.md) | Integer | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| [`RandomStatDown`](./Enums.md) | Integer | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |

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
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 11 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 10 | `1`<br>`10`<br>`2` |

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
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 4 | `.1`<br>`.16666666`<br>`.3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | [`AutoReanimate`](./Enums.md) | Integer | The percentage chance for the unit to automatically reanimate upon death. | 2 | `100%`<br>`50%` |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 1 | `1`<br>`10`<br>`2` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 52 | `passives`<br>`class`<br>`tag` |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 8 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`PermanentIntelligence`](./Enums.md) | Integer | The permanent amount of intelligence added or removed. | 3 | `-1`<br>`1`<br>`2` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 2 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid`

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 5 | `1`<br>`10`<br>`2` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 5 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |

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
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 9 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 9 | `Electric`<br>`Fire`<br>`Gravity` |

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
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 4 | `10`<br>`55`<br>`75` |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 7 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 6 | `.02`<br>`.1`<br>`.15` |

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
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 7 | `1`<br>`2`<br>`3` |
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 6 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

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
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 37 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 37 | `Default`<br>`FormChange`<br>`Druid` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 28 | `passives`<br>`class`<br>`tag` |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 1 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |

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
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

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
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 24 | `-3`<br>`10`<br>`2` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 22 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

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
| [`weights`](./Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 9 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 2 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |

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
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 6 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | `passives`<br>`class`<br>`tag` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 6 | `{ . . . }` |

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
| [`number`](./Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 31 | `1`<br>`10`<br>`2` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 23 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

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
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `Key`<br>`passives`<br>`class` |
| [`UseAbility`](./Enums.md#enum-useability) | Enum  | The name of the ability the target is forced to use. | 1 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

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
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`HealthGain`](./Enums.md) | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`ManaGain`](./Enums.md) | Integer | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | `passives`<br>`class`<br>`tag` |
| [`DamageUp`](./Enums.md) | Integer | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`Charge`](./Enums.md) | Integer | The number of charge stacks applied. | 4 | `1`<br>`2`<br>`3` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | `passives`<br>`class`<br>`tag` |
| [`ScatterCoins`](./Arrays.md#array-scattercoins) | Array / Integer  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 | `5`<br>`[1 .5]` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |

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
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 | `passives`<br>`class`<br>`tag` |
| [`RangeUp`](./Enums.md) | Integer | The number of stacks of bonus attack range applied. | 1 | `1` |

</details>


---


<details>
<summary><b>Conditional_RandomChance</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 | `passives`<br>`class`<br>`tag` |

</details>