# Passives vs Effects Block Analysis

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document shows which properties appear inside `passives` and `effects` blocks, broken down by `.gon` file category.

Three tiers are used:
- **Universal** — appears in ALL categories
- **Partially Shared** — appears in 2+ categories but not all
- **Truly Exclusive** — appears in exactly ONE category only

---

## Block: `passives`

**8 categories** | **1285 total unique properties**

- Universal (all 8 cats): **0**
- Partially shared (2–7 cats): **295**
- Truly exclusive (1 cat only): **990**

**Categories:** `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives`, `tutorial_cats.gon`

### Partially Shared Properties

| :--- | :--- | :---: |
| `AddStatusToBasicAttack` | `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | Contains status effects to add to the basic attack. | 178 
| `Brace` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 
| `Trample` | `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | The amount of bonus damage dealt when moving through an enemy. | 14 
| `Metal` | `items`, `passives` | The number of armor stacks or metal keyword effects. | 2 
| `Thorns` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | The amount of thorns damage dealt to attackers on hit. | 36 
| `SpawnOnDeath` | `characters`, `elite_buffs.gon`, `items` | Specifies an object and its faction to spawn when the unit dies. |
| `MeleeRevengeDamage` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | Defines the damage and effects applied back to a melee attacker upon being hit. | 20 
| `HealthRegenUp` | `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 
| `StatusEachTurnEnd` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies status effects applied to the unit at the end of each of its turns. | 16 
| `SpawnOnBattleStart` | `boss_elite_buffs.gon`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `passives` | Specifies the object that spawns adjacent to the unit at the start of battle. | 24 
| `Robot` | `characters`, `item_setbonuses.gon`, `passives` | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 2 
| `StatusOnBattleEnd` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | An object containing status effects or passives applied to the unit when the battle ends. | 6 
| `ElementImmune` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 16 
| `StatusOnTookDamage` | `characters`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies status effects or actions triggered when the unit takes damage. | 34 
| `SpawnThingOnDamage` | `characters`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies an object that spawns on the tile when the unit takes damage. | 18 
| `StatusImmunity` | `characters`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | A list of status effect names the unit is immune to. |
| `StatusOnKill` | `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies status effects or actions triggered when the unit kills an enemy. | 18 
| `AddPassivesToMinions` | `item_setbonuses.gon`, `items`, `passives` | An object containing passives that are granted to all minions spawned by the unit. | 30 
| `CounterAttack` | `characters`, `items`, `mutations`, `passives` | Specifies the ability used when the unit counterattacks after being hit. | 4 
| `DeathRattle` | `characters`, `item_setbonuses.gon`, `items`, `passives` | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 2 
| `Fire` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 6 
| `CritChanceUp` | `boss_elite_buffs.gon`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | The amount of critical hit chance added as a flat percentage. | 36 
| `EliteTint` | `boss_elite_buffs.gon`, `elite_buffs.gon` | An RGBA tint color (r g b a) applied to elite variants of a unit. |
| `RevengeDamage` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `items`, `mutations`, `passives` | An object defining the damage and effects that trigger when the unit is attacked. | 30 
| `DodgeChance` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `items`, `mutations`, `passives` | The percentage chance the unit has to dodge incoming attacks. | 30 
| `AddBonusRange` | `items`, `mutations`, `passives` | The number of additional tiles of range added to the unit's abilities. | 26 
| `MulticlassLevelUp` | `mutations`, `passives` | Specifies the class that this unit gains a level in when multiclassing. | 32 
| `StatusEachTurnBegin` | `items`, `mutations`, `passives` | Specifies status effects applied to the unit at the start of each of its turns. | 16 
| `AbilityReaction` | `characters`, `items`, `mutations`, `passives` | Specifies the ability used as a reaction when the unit is targeted by an ability. | 4 
| `Undead` | `characters`, `items` | If set, flags the unit as undead (e.g., 1) with associated mechanics. |
| `DamageUp` | `boss_elite_buffs.gon`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 
| `AddElementsToBasicAttack` | `characters`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies an elemental damage type that is added to the unit's basic attacks. | 32 
| `AddMovement` | `characters`, `mutations`, `passives` | The amount of bonus movement points added to the unit's base movement. | 6 
| `SpawnEachTurn` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 12 
| `MissChance` | `characters`, `items`, `mutations`, `passives` | The flat percentage chance that the unit's attacks will miss. | 24 
| `AddCorpseHealth` | `characters`, `elite_buffs.gon`, `items`, `mutations`, `passives` | The amount of bonus health the unit's corpse has before it can be resurrected. | 12 
| `ArmorDodgeChance` | `item_setbonuses.gon`, `items`, `passives` | The percentage chance to dodge incoming attacks when wearing this armor. | 2 
| `EliteParticle` | `boss_elite_buffs.gon`, `elite_buffs.gon` | Specifies the particle effect name attached to an elite unit. |
| `WaterWalk` | `characters`, `mutations`, `passives` | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 10 
| `AddCritMultiplier` | `items`, `passives` | The percentage added to the critical hit damage multiplier. | 28 
| `InnateElement` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `passives` | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 8 
| `KineticSpikes` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `items`, `mutations` | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 
| `Ice` | `characters`, `items`, `mutations`, `passives` | Applies the Slow status effect to targets hit by ice-element abilities. | 7 
| `attack` | `characters`, `passives` | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 26 
| `PassiveWhenAffectedByElement` | `characters`, `items`, `mutations`, `passives` | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 24 
| `Poison` | `characters`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 
| `ReplaceBasicMove` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies an alternative movement ability that replaces the unit's default move. | 10 
| `SizeScale` | `boss_elite_buffs.gon`, `elite_buffs.gon`, `passives` | The multiplier applied to the unit's visual and hitbox size. | 4 
| `SpawnThingOnDeath` | `characters`, `items`, `passives` | Specifies the name of an object to spawn upon death. | 4 
| `StatusOnBattleStart` | `items`, `passives` | An object containing status effects to apply to the unit at the start of every battle. | 2 
| `AddManaRegen` | `items`, `mutations`, `passives` | The flat amount of mana regenerated per turn. | 4 
| `BleedThorns` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | The amount of bleed thorns damage dealt to attackers on hit. | 8 
| `Creep` | `characters`, `elite_buffs.gon` | A variable representing the Creep element or material type. |
| `HealthMultiplier` | `boss_elite_buffs.gon`, `elite_buffs.gon` | A multiplier applied to the unit's base health. |
| `ReplaceSpawnedObjects` | `items`, `passives` | An array of [original_object replacement_object] pairs for swapping spawned objects. |
| `AbilityOnBattleStart` | `items`, `passives` | Casts the specified ability when the battle begins. | 6 
| `AddLevelUpRerolls` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | The number of additional rerolls the unit gets when leveling up. | 8 
| `AllStatsUp` | `characters`, `items`, `mutations`, `passives` | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). |
| `ExtraBasicAttacks` | `items`, `mutations`, `passives` | The number of additional basic attacks the unit can perform per turn. | 6 
| `ReflectProjectiles` | `characters`, `elite_buffs.gon`, `items`, `mutations` | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 4 
| `AbilityHealthThreshold` | `characters`, `items` | Defines an ability and conditions for its activation when the unit's health reaches a threshold. | 2 
| `AddStatusToAllDamage` | `item_setbonuses.gon`, `items`, `passives` | Adds the contained status effects to all damage dealt by the unit. | 4 
| `Bleed` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 
| `BonusAbility` | `items`, `passives` | Specifies the name of a bonus ability granted. | 12 
| `DeathRattleRevive` | `characters`, `item_setbonuses.gon`, `items` | Specifies an ability or effect that revives the unit upon death, with options for stunning behavior. |
| `PassiveAtStatThreshold` | `item_setbonuses.gon`, `items`, `passives` | An object defining passives granted when a unit's stat meets a specified threshold. | 10 
| `AlphaTurns` | `characters`, `items`, `mutations`, `passives` | The number of turns the unit acts first in battle; negative values may indicate last. | 8 
| `AmplifyStatus` | `items`, `passives` | Specifies the status effect to amplify, or an object with the status and number of stacks to add. | 8 
| `BackstabImmunity` | `characters`, `item_setbonuses.gon`, `mutations`, `passives` | If greater than 0, prevents the unit from taking extra damage from backstabs. | 6 
| `Bruise` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 
| `IgnoreTiles` | `characters`, `items`, `mutations`, `passives` | If set to 1, movement ignores tile-based penalties or restrictions. | 12 
| `MoveWhenDamaged` | `characters`, `mutations`, `passives` | Defines movement behavior when the unit takes damage, such as weights and move ability. | 2 
| `PoisonThorns` | `characters`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | The number of stacks of Poison applied to melee attackers when they hit this unit. | 6 
| `AddBonusMeleeRange` | `items`, `mutations`, `passives` | The number of additional tiles of range added to the unit's melee attacks. | 12 
| `AddSelfStatusToBasicAttack` | `items`, `passives` | Applies the contained status effects to the unit when it uses its basic attack. | 4 
| `AddStatusToBasicMeleeAttack` | `mutations`, `passives` | An object listing status effects applied by the unit's basic melee attack. | 16 
| `CritsApplyStatus` | `items`, `passives` | An object containing statuses applied to the target when the unit lands a critical hit. | 12 
| `EliteFlatTint` | `boss_elite_buffs.gon`, `elite_buffs.gon` | An RGB or RGBA tint multiplier applied uniformly to an elite unit's sprite. |
| `MoveTowardsDamageSource` | `characters`, `elite_buffs.gon`, `items`, `passives` | Determines the movement behavior when moving towards the unit that dealt damage to it. | 2 
| `Quivered` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 
| `SpawnOnBattleStartRandomEmptyTile` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies an object that spawns on a random empty tile at the start of battle. | 10 
| `StatusOnKillEnemy` | `item_setbonuses.gon`, `items`, `passives` | Specifies the effects applied when the unit kills an enemy. | 2 
| `AddTag` | `characters`, `items`, `passives` | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 2 
| `DepressionAura` | `boss_elite_buffs.gon`, `elite_buffs.gon`, `items`, `mutations`, `passives` | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 2 
| `Electric` | `characters`, `item_setbonuses.gon`, `mutations`, `passives` | Applies a Stun status effect with specified stacks and probability based on variable X. | 6 
| `EquipTemporaryItem` | `mutations`, `passives` | Specifies which temporary item is equipped. | 12 
| `ExtraWeaponAttacks` | `items`, `passives` | The number of additional weapon attacks the unit can perform. | 8 
| `Flying` | `characters`, `item_setbonuses.gon`, `items`, `passives` | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 
| `LimitDamage` | `characters`, `passives` | The maximum amount of damage the unit can take from a single hit. | 2 
| `MovementReaction` | `characters`, `items`, `passives` | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 2 
| `ReplaceBasicAttack` | `items`, `passives` | Specifies the ability ID that replaces the unit's basic attack. | 8 
| `StatusAlliesOnBattleStart` | `item_setbonuses.gon`, `items`, `passives` | An object containing status effects to apply to all allies at the start of battle. | 2 
| `StatusOnEndMove` | `characters`, `items`, `mutations`, `passives` | Specifies status effects or actions triggered when the unit finishes moving. | 6 
| `TrinketPassiveMultiplierBonus` | `item_setbonuses.gon`, `items`, `passives` | Bonus multiplier to the passive effects of equipped trinkets. | 2 
| `AddDamageToElementDamage` | `items`, `mutations`, `passives` | Defines additional damage of a specific element added to the unit's attacks. | 6 
| `BoostHeals` | `items`, `passives` | The number of stacks that increase healing received or dealt. | 2 
| `BoostWeaponDamage` | `items`, `mutations`, `passives` | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 10 
| `ChanceToRevive` | `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `passives` | The percentage chance or an object defining chance, health, and statuses on revival. | 2 
| `Food` | `characters`, `items`, `passives` | The number of food pickups spawned. | 11 
| `LimitHeal` | `characters`, `passives` | If 1, prevents the unit from being healed. | 2 
| `ManaCostReduction` | `items`, `mutations`, `passives` | The amount or percentage by which ability mana costs are reduced for this unit. | 4 
| `PassiveAtHealthThreshold` | `item_setbonuses.gon`, `items`, `passives` | An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives. | 4 
| `SmallRockBehavior` | `characters`, `passives` | Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed. |
| `StatusOnDie` | `characters`, `elite_buffs.gon`, `items`, `mutations` | Specifies status effects or actions triggered when the unit dies. | 2 
| `StatusOnTookDamageFromAbility` | `characters`, `mutations`, `passives` | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 6 
| `Water` | `characters`, `mutations`, `passives` | Form state for water element, applying a puddle or movement bonus. | 5 
| `YOffset` | `characters`, `mutations` | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 
| `AddInitiative` | `characters`, `items`, `mutations`, `passives` | The amount of bonus or penalty to the unit's turn order initiative value. | 2 
| `AddKnockbackDamage` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | The amount of additional knockback damage applied. | 8 
| `AddStatusToWeapons` | `characters`, `items`, `passives` | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 8 
| `DebuffImmunity` | `characters`, `items`, `passives` | If 1, the unit is immune to debuffs. | 2 
| `ExtraMovePoints` | `characters`, `items`, `passives` | The number of additional movement points granted to this unit. | 10 
| `KnockbackImmunity` | `characters`, `item_setbonuses.gon`, `items`, `mutations`, `passives` | If set to 1, the unit cannot be knocked back. | 6 
| `MoveOne` | `characters`, `elite_buffs.gon`, `items`, `passives` | Specifies a forced movement of exactly one tile in a direction. | 2 
| `NonStackingShield` | `boss_elite_buffs.gon`, `elite_buffs.gon` | The amount of non-stacking shield granted. |
| `PermanentMadness` | `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `passives` | The number of permanent madness stacks applied. |
| `SecurityBotProtect` | `characters`, `passives` | Specifies the ability and movement used by a security bot to protect allies. | 2 
| `SetSpellCosts` | `characters`, `items`, `passives` | Overrides the cost of all spells to this value. | 2 
| `SpawnOnDowned` | `items`, `mutations` | Specifies the character or object spawned when the unit is downed. | 14 
| `StatusAlliesOnDeath` | `items`, `passives` | Applies the contained status effects to all allies when the unit dies. | 8 
| `StatusEachRoundBegin` | `boss_elite_buffs.gon`, `elite_buffs.gon` | Applies the contained status effects at the beginning of each round. |
| `StatusEveryXSpellCasts` | `items`, `mutations`, `passives` | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 8 
| `StatusIfUnusedMovePoints` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | Specifies status effects applied if the unit ends its turn with unused movement points. | 6 
| `StatusOnCastSpell` | `items`, `mutations`, `passives` | An object listing status effects applied to the unit whenever it casts a spell. | 8 
| `TileTrail` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `passives` | Specifies the type of tile left behind as the unit moves. | 4 
| `AddTemporaryEffectsToBasicAttack` | `characters`, `items`, `mutations`, `passives` | A container object that lists temporary status effects applied to the unit's basic attack. | 6 
| `AutocastEachRound` | `characters`, `item_setbonuses.gon`, `passives` | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 
| `Burn` | `characters`, `items`, `passives` | The amount of Burn applied, either as a fixed number or a formula string. | 1 
| `ClassManaCostReduction` | `item_setbonuses.gon`, `items`, `mutations`, `passives` | Defines a reduction in mana cost for abilities of a specific class. | 4 
| `DodgeChance_Status` | `characters`, `items`, `mutations` | The flat percentage increase to dodge chance applied as a status effect. | 2 
| `MinimumKnockbackFromAllDamage` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon` | The minimum knockback distance the unit will suffer from any damage source. |
| `OverrideBasicAttack` | `items`, `passives` | Replaces the unit's basic attack with the specified ability. |
| `OverrideMaxHealth` | `characters`, `passives` | Replaces the unit's maximum health with this value. |
| `PassiveWhenOnTile` | `item_setbonuses.gon`, `items` | Grants the contained passive effects while the unit is standing on one of the specified tile types. |
| `SetFragileImmune` | `item_setbonuses.gon`, `items` | Sets the unit's material to the specified type, granting immunity to the Fragile status. |
| `SpeedUp` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `passives` | The number of stacks of a Speed buff applied, increasing the target's turn order priority. |
| `AddHiddenTag` | `characters`, `items`, `passives` | A hidden tag applied to the unit for internal logic and triggers. | 2 
| `AddStatusToElementDamage` | `items`, `passives` | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 
| `BackstabCritChance` | `item_setbonuses.gon`, `items`, `passives` | A multiplier for critical hit chance on backstab attacks. | 2 
| `BasicJump` | `items`, `mutations` | Specifies a basic jump movement ability. | 18 
| `BeefyCharmedLeech` | `item_setbonuses.gon`, `passives` | An object defining a variant of the Maggot familiar, specifically a charmed, larger leech. |
| `ChanceToBackflip` | `characters`, `items`, `mutations`, `passives` | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 
| `DelayedAutoRevive` | `characters`, `item_setbonuses.gon`, `items` | Configures an automatic revival after a delay, with specified rounds and health percentage. |
| `FaceShield` | `characters`, `items`, `passives` | If 1, the unit has a face shield that protects it from certain attacks or effects. | 2 
| `FreezePiercing` | `item_setbonuses.gon`, `items`, `passives` | The number of stacks of freeze resistance that are ignored when applying freeze. | 4 
| `IncreaseExplosionDamage` | `items`, `passives` | The flat amount by which explosion damage is increased. | 4 
| `InjuryImmunity` | `characters`, `items`, `passives` | The number of turns the unit is immune to injuries. | 2 
| `LevelUpClassOverride` | `items`, `passives` | Specifies which class the unit gains upon leveling up, overriding the default class. | 4 
| `MoveQuivered` | `items`, `passives` | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 
| `PassiveWhileHasStatus` | `characters`, `mutations` | An object containing `status` and `passives` that grants the listed passives while the unit has the specified status. | 2 
| `SetBrittleImmune` | `item_setbonuses.gon`, `items` | Sets the unit's material to the specified type, granting immunity to the Brittle status. |
| `SpawnObjectOnPopCorpse` | `items`, `passives` | Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped. | 2 
| `StatusOnAllyCatDeath` | `items`, `mutations`, `passives` | An object listing status effects applied to the unit when an allied cat dies. | 4 
| `StatusOnGainCoins` | `characters`, `items`, `passives` | Specifies status effects applied when this unit gains coins. | 4 
| `StunImmunity` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon` | If 1, the unit is immune to stun. The optional object configures whether to cleanse stun on apply. |
| `TrinketActiveEffectsMultiplierBonus` | `item_setbonuses.gon`, `items`, `passives` | Bonus multiplier to the active effects of equipped trinkets. | 2 
| `AbilityWhenTaggedCharacterMovesNear` | `characters`, `mutations`, `passives` | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 4 
| `AddPassivesToCharmed` | `items`, `passives` | Grants the contained passive effects to units under the charm status. | 4 
| `AmplifyKnockback` | `items`, `passives` | The additional distance (in tiles) a unit is knocked back. | 4 
| `BlacklistPickupType` | `mutations`, `passives` | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 8 
| `CatchProjectiles` | `items`, `passives` | An object defining chance to catch projectiles and optionally apply statuses. | 2 
| `Confusion` | `items`, `mutations` | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 
| `DisableAbilitiesWithTag` | `mutations`, `passives` | Specifies a tag that disables any ability with that tag on the unit. | 8 
| `ElementalManaCostReduction` | `items`, `passives` | An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount. | 4 
| `ExtraStatusWhenDealingDamage` | `items`, `passives` | Defines additional statuses applied to the target or source when dealing damage, with conditionals. | 2 
| `food` | `characters`, `mutations`, `passives` | The range [min, max] of food items dropped. | 11 
| `FreePathfindElement` | `characters`, `mutations`, `passives` | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 6 
| `HeadArmorPassiveMultiplierBonus` | `items`, `passives` | A multiplier bonus applied to passive effects granted by head armor. |
| `IncreaseExplosionSize` | `items`, `passives` | The number of extra tiles added to the radius of explosions. | 2 
| `MakeSpellsRequireCharge` | `items`, `passives` | If true, spells require a charge-up turn before casting. | 2 
| `PassiveWhenAtFullMana` | `mutations`, `passives` | An object listing passive effects that are active only while the unit's mana is full. | 6 
| `SharkySmellsBlood` | `characters`, `items` | If 1, the unit is attracted to damaged units and may prioritize them. |
| `StatusKilledCharacters` | `mutations`, `passives` | An object listing status effects applied to the unit when it kills a character. | 6 
| `StatusOnEatFood` | `items`, `mutations`, `passives` | An object listing status effects applied to the unit when it eats food. | 4 
| `StatusOnPopCorpse` | `items`, `passives` | Specifies the effects applied when the unit pops a corpse. | 2 
| `StatusOnTurnEndIfCastNSpells` | `item_setbonuses.gon`, `passives` | An object that applies a status effect at the end of the turn if the unit has cast a specified number of spells. | 4 
| `StatusOnTurnEndIfDidntCastAbilityTypes` | `item_setbonuses.gon`, `items`, `passives` | Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s). |
| `AddStatusToSpells` | `characters`, `items`, `passives` | Specifies status effects added to all spell attacks used by this unit. | 2 
| `AllyDamageReduction` | `items`, `passives` | The amount by which damage dealt to allies is reduced. | 4 
| `ApplyStatusesToRandomEnemiesEachTurn` | `items`, `passives` | An object specifying statuses to apply to random enemies each turn, with an optional 'count' field. | 2 
| `AutoEquipConsumables` | `item_setbonuses.gon`, `items`, `passives` | The number of consumables automatically equipped per turn. | 2 
| `Blind` | `items`, `mutations` | The amount of blind stacks applied, or an [stacks, probability] array. | 6 
| `BuffImmunity` | `characters`, `items`, `passives` | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. |
| `bug` | `item_setbonuses.gon`, `items` | A variable key likely indicating a known issue or placeholder value. |
| `ChanceToBlockAndCounter` | `items`, `passives` | The percentage chance or an object defining chance and conditions to block and counter an attack. | 2 
| `CreepTile` | `characters`, `elite_buffs.gon` | A variable key referencing a tile type that applies a creep or detrimental effect. |
| `DamageNeighborsAfterMove` | `boss_elite_buffs.gon`, `elite_buffs.gon`, `passives` | Defines the spell damage and effects applied to neighboring tiles after the unit moves. | 2 
| `DisableAbilities` | `items`, `passives` | Specifies which category of abilities to disable, such as 'all_items' or 'basic_attack'. |
| `ExtraDispersedTurns` | `characters`, `elite_buffs.gon` | The number of additional or fewer turns in the dispersed turn order. |
| `FaceArmorPassiveMultiplierBonus` | `items`, `passives` | A multiplier bonus applied to the effects of face armor passives. |
| `FlowersOnEndTurn` | `item_setbonuses.gon`, `items`, `passives` | The number of flowers spawned on the unit's tile at the end of each turn. | 2 
| `IncreaseSpellRange` | `item_setbonuses.gon`, `items`, `passives` | The number of extra tiles added to the range of spells. | 2 
| `Jester` | `items`, `passives` | An array of dialogue quotes for the Jester class. | 32 
| `KillsToMeat` | `items`, `passives` | Specifies the type of meat item spawned when killing certain enemies. | 2 
| `PassiveAfterXKills` | `item_setbonuses.gon`, `items`, `passives` | Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key. | 2 
| `PassiveWhenDead` | `characters`, `items` | Passive effects that remain active while the unit is dead. |
| `Poop` | `items`, `mutations`, `passives` | A deployable object that acts as a hazard or obstacle, spawning a Poop movieclip with its own name and sound effects. | 2 
| `PoopWhenHit` | `items`, `mutations`, `passives` | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 4 
| `ProtectTargetedAllies` | `characters`, `passives` | Specifies the ability used to protect targeted allies, including an optional target filter. | 2 
| `RandomPassivePool` | `characters`, `passives` | A pool of random passives from which one is chosen for this unit. |
| `RangedTrueShot` | `items`, `passives` | Ranged attacks cannot miss or be dodged, guaranteeing a hit. Value acts as a binary flag. | 2 
| `rock` | `items`, `passives` | A variable used in logic contexts. | 46 
| `ShowHiddenThings` | `mutations`, `passives` | If nonzero, reveals hidden objects or tiles on the map. | 6 
| `SpawnCatCopyOnBattleStart` | `item_setbonuses.gon`, `passives` | An object that spawns a copy of the unit's cat at the start of battle, with sub-keys for the copy object and chain-prevention tag. | 4 
| `SpawnExtraThingsOnBattleStart` | `items`, `mutations` | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 2 
| `StatusAfterCastSpell` | `items`, `passives` | An object containing status effects to apply to the unit immediately after it casts any spell. | 2 
| `StatusOnBreakItem` | `items`, `passives` | An object containing status effects to apply when the unit breaks a weapon or armor item. | 2 
| `StatusOnHealed` | `items`, `passives` | An object that applies a status effect to the unit whenever it is healed. | 4 
| `TauntAlways` | `items`, `passives` | If non-zero, the unit is always taunted, forcing it to target the first enemy in range. | 4 
| `WeaponsDontLoseDurability` | `characters`, `passives` | If set to 1, weapons equipped by this unit do not lose durability. | 2 
| `AddSelfStatusToWeapons` | `items`, `passives` | An object whose nested keys define status effects applied to the unit's own weapons. | 2 
| `AddStartingMana` | `item_setbonuses.gon`, `passives` | The amount of bonus mana the unit starts each battle with. | 2 
| `AddStatusToKnockbackDamage` | `items`, `passives` | An object whose nested keys define statuses applied to damage caused by knockback. | 2 
| `AddUnfilledMaxHealth` | `elite_buffs.gon`, `passives` | The amount of maximum health added, but not healed (the health bar remains at its current level). | 2 
| `BasicAttackCritChance` | `items`, `passives` | A multiplier for the critical hit chance of basic attacks, either as a float or percentage. |
| `BoomerCatExplode` | `characters`, `passives` | An object defining the explosion ability for a boomerang cat, including its spell template and graphics. |
| `BouncyProjectiles` | `items`, `passives` | An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior. | 2 
| `CanRemoveCursedItems` | `items`, `mutations`, `passives` | If nonzero, allows the unit to remove cursed items from equipment slots. | 2 
| `CCImmunity` | `characters`, `passives` | If set to 1, this unit is immune to crowd control effects. | 2 
| `consumable` | `mutations`, `passives` | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 140 
| `ConsumableEffectsMultiplierBonus` | `items`, `passives` | A multiplier bonus applied to the effects of consumable items. | 2 
| `DoubleCastWeapons` | `items`, `passives` | The number of additional weapon casts per attack. | 2 
| `Eternal` | `items`, `passives` | Defines the Eternal revival effect, setting stacks and the health percentage restored. | 2 
| `ExtraBasicMoves_Status` | `item_setbonuses.gon`, `items`, `passives` | The number of extra basic moves per turn granted. |
| `Fighter` | `mutations`, `passives` | Specifies the 'Fighter' form within FormChanger, used for boss dialogue. | 80 
| `FireTile` | `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon` | Represents a tile of fire on the map, which deals damage to units on it over time. |
| `FlyDamageIncrease` | `items`, `passives` | The number of stacks or alias for damage increase against flying units. | 2 
| `GainExtraShield` | `items`, `passives` | The amount of shield gained on turn start. | 2 
| `HouseFoodRequirementMultiplier` | `mutations`, `passives` | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 4 
| `Hunter` | `mutations`, `passives` | Defines a list of quotes for the Hunter class (vs boss, embark, return early). | 68 
| `InfiniteRebirth` | `characters`, `passives` | Specifies the health and effects for unlimited rebirth upon death. | 2 
| `int` | `items`, `passives` | The Intelligence stat value or modifier. | 401 
| `Lava_Distortion` | `boss_elite_buffs.gon`, `elite_buffs.gon` | A configuration object for a visual distortion effect, typically defining a movieclip and render settings. |
| `LuckUp` | `boss_elite_buffs.gon`, `elite_buffs.gon`, `items` | The amount of Luck stat changed on the source, affecting random chance outcomes. |
| `Mage` | `mutations`, `passives` | Defines a list of quotes for the Mage class. | 70 
| `MoveAndUseAbilityEachTurnBeginIfPossible` | `items`, `passives` | Specifies the name of the ability the unit will move and attempt to use at the start of each of its turns. |
| `MoveAwayFromDamageSource` | `characters`, `mutations`, `passives` | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 2 
| `musical` | `items`, `mutations` | A variable key likely related to musical abilities or sound effects. | 4 
| `NeckArmorPassiveMultiplierBonus` | `items`, `passives` | A multiplier bonus applied to the passives of the unit's neck armor slot. |
| `PassiveWhileInMonkMeleeStance` | `items`, `passives` | Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance. | 2 
| `RemoveLineOfSightRestrictions` | `items`, `passives` | Line of sight requirements for targeting are ignored, allowing the unit to target any visible cell regardless of obstacles. | 2 
| `ScaledStatusOnSpendMana` | `items`, `passives` | An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent. | 2 
| `SetDefaultFacePassive` | `items`, `passives` | Specifies the name of the default face passive to be assigned to this unit. |
| `Shadowstep` | `mutations`, `passives` | An object defining the Shadowstep ability, which allows the unit to teleport behind a target before an attack. | 2 
| `SharePickups` | `characters`, `passives` | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 2 
| `SpawnCreepOnHit` | `characters`, `passives` | If set to 1, spawns creep on the tile when this unit takes damage. |
| `StatusEachTurnEndForEachTurn` | `items`, `passives` | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 
| `StatusOnCollectPickup` | `items`, `passives` | An object containing status effects to apply when the unit collects a pickup item. | 2 
| `StatusOnPickupCoins` | `items`, `passives` | Specifies the effects applied when the unit picks up coins. | 2 
| `StatusOnUseBasicAttack` | `items`, `passives` | Specifies the effects applied when the unit performs a basic attack. | 2 
| `StatusWhenAllySpendsMana` | `items`, `passives` | Specifies the effects applied when an ally spends mana. | 2 
| `StrengthUp` | `characters`, `passives` | The number of stacks of Strength Up applied to the source, increasing its Strength stat. |
| `Thief` | `mutations`, `passives` | Form identifier for the Thief boss type. | 76 
| `ToadJump_BasicMove` | `mutations`, `passives` | An object defining a basic movement ability for a toad-like unit. | 4 
| `TowerDefenseReflex` | `characters`, `passives` | Specifies the ability or attack used when the unit counterattacks in tower defense reflex mode. | 2 
| `UncappedHP` | `characters`, `passives` | If 1, the unit's maximum HP is not capped by standard limits. | 2 
| `UpgradeSpawnedPickups` | `item_setbonuses.gon`, `passives` | The number of times spawned pickups are upgraded in quality. | 2 
| `Vegan` | `mutations`, `passives` | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 4 
| `WeaponDamageMultiplierBonus` | `items`, `passives` | Bonus multiplier to weapon damage. | 2 
| `Wind` | `characters`, `mutations` | Defines the properties for the Wind element, such as knockback amount. |
| `AbsorbBuff` | `boss_elite_buffs.gon`, `elite_buffs.gon` | A visual effect object (e.g., ManaParticle) that plays when mana or a buff is absorbed. |
| `all_items` | `items`, `passives` | A variable field for specifying all items; no standard examples provided. |
| `AlphaCat` | `items`, `passives` | The number of AlphaCat stacks applied to the source on kill. | 2 
| `BackflipWhenTargeted` | `items`, `mutations` | The number of backflip charges, or an object defining its ability. | 2 
| `BasicAttackCantMiss` | `items`, `mutations` | If nonzero, the unit's basic attack cannot miss. | 2 
| `BellyFlop_BasicMove` | `items`, `passives` | Specifies the belly flop basic move ability. |
| `CapMovementAbilityRange` | `items`, `passives` | The maximum range allowed for movement abilities. |
| `ConjureBonusAbility` | `characters`, `mutations` | Specifies the name of the bonus ability to conjure. | 2 
| `CreateGlobalModifiers` | `characters`, `items` | Defines global gameplay modifiers to activate. |
| `DoNothing` | `item_setbonuses.gon`, `items` | Specifies a passive or item ability that performs no action. |
| `EquipRandomTemporaryItemFromPool` | `mutations`, `passives` | Specifies the item pool (e.g., 'pills' or 'weapons') from which a random temporary item is equipped. | 4 
| `ExplosionImmunity` | `items`, `passives` | If non-zero, grants immunity to explosion damage. | 2 
| `ExtraTrinketUses` | `items`, `passives` | The number of additional uses granted to trinkets. | 2 
| `FindExtraItemFromPoolOnBattleEnd` | `item_setbonuses.gon`, `items` | Specifies the item pool from which an extra item is granted at the end of combat. |
| `GlobalManaBurnAura` | `boss_elite_buffs.gon`, `elite_buffs.gon` | The amount of mana burned from all enemies per turn. |
| `Holy` | `item_setbonuses.gon`, `items` | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. |
| `HPGainBlock` | `items`, `passives` | If true, the unit cannot gain health from any source. |
| `MakeBasicAttackPull` | `items`, `mutations` | If nonzero, the unit's basic attack pulls the target closer. | 2 
| `MoveSpeedMultiplier` | `items`, `passives` | A multiplier for the unit's movement speed. |
| `NonStackingDivineShield` | `boss_elite_buffs.gon`, `elite_buffs.gon` | The number of Divine Shield stacks that do not stack with duplicates. |
| `PassiveEnergized` | `boss_elite_buffs.gon`, `elite_buffs.gon` | Enables an electrified visual effect (using Particle_Electric particle) on the unit, indicating a charged or energized state. |
| `PassiveTar` | `boss_elite_buffs.gon`, `elite_buffs.gon` | Enables a dripping tar particle effect (using Particle_TarDrip) on the unit, indicating a tar-related passive. |
| `Phasing` | `characters`, `passives` | If set to 1, allows the character to phase through solid objects or obstacles. | 2 
| `pills` | `item_setbonuses.gon`, `mutations` | The amount of pills granted as a consumable reward. | 2 
| `random` | `characters`, `mutations` | A random value used for stat or attribute adjustment. | 1 
| `red` | `boss_elite_buffs.gon`, `elite_buffs.gon` | Configuration for one of the dialog options (label 'EVENT_RED_ANSW'), with a fixed chance and associated animation, in a choice event. | 2 
| `Slow` | `mutations`, `passives` | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 
| `SparkleBuff` | `boss_elite_buffs.gon`, `elite_buffs.gon` | A variable defining a sparkle particle effect buffer for visual feedback. |
| `SpikeBuff` | `boss_elite_buffs.gon`, `elite_buffs.gon` | A variable defining a spike/bramble particle effect buffer for visual feedback. |
| `StatusAfterXTurns` | `characters`, `items` | Applies a status effect or forces an ability usage after a set number of turns. |
| `StatusEachRoundEnd` | `elite_buffs.gon`, `mutations` | An object listing status effects applied to the unit at the end of each round. | 2 
| `StatusOnEatPill` | `item_setbonuses.gon`, `passives` | Specifies the effects applied when the unit consumes a pill item. |
| `WeaponActiveEffectsMultiplierBonus` | `item_setbonuses.gon`, `passives` | Bonus multiplier to the active effects of the equipped weapon. |
| `WeaponPassiveMultiplierBonus` | `item_setbonuses.gon`, `passives` | Bonus multiplier to the passive effects of the equipped weapon. |
| `ZombieCatFamiliar` | `items`, `passives` | Defines the ZombieCat familiar, a companion entity that follows the unit in combat. | 4 
| Property | Categories | Total Uses |

### Truly Exclusive Properties (one category only)

#### `boss_elite_buffs.gon` — no truly exclusive properties

#### `characters` (418 truly exclusive)

| :--- | :---: |
| Property | Count |
| `FormChanger` | 106 |
| `RandomArmorPickup` | 56 |
| `FormChangeWhileHasStatus` | 35 |
| `ImmediateAbilityReaction` | 26 |
| `BossRewards` | 20 |
| `BirdRewards` | 18 |
| `Buddy` | 17 |
| `HealthPickup` | 16 |
| `CharacterLightSource` | 16 |
| `Antidote` | 14 |
| `TransformOnDeath` | 13 |
| `NoHealthOnlyShield` | 12 |
| `StripStatuses` | 10 |
| `CoinPickup` | 10 |
| `StatusCollector` | 9 |
| `TransformOnElementInfluence` | 9 |
| `FormChangeOnElementInfluence` | 9 |
| `FormChangeOffMap` | 8 |
| `Plant` | 8 |
| `FadeInsteadOfDie` | 8 |
| `RandomizeAIWeightsEachTurn` | 8 |
| `TransformInXTurns` | 7 |
| `AbilityWhenBuddyDies` | 7 |
| `ChanceToSpitOnDamage` | 7 |
| `Webbed` | 6 |
| `KaijuKnockbackImmune` | 6 |
| `Divide4OnDeath` | 6 |
| `FormChangeWhilePrimingAbility` | 6 |
| `AddDamage` | 6 |
| `HealthGain` | 6 |
| `CaveFamilyEnrage` | 6 |
| `TagGreed` | 6 |
| `MoveTowardsKillers` | 5 |
| `Angel` | 5 |
| `TransformOnDeathImmediately` | 5 |
| `StartOffMap` | 5 |
| `AddMaxHealth` | 4 |
| `Ammo` | 4 |
| `CountAsCorpse` | 4 |
| `PrioritizeFarAwayTargets` | 4 |
| `LoopingSoundWhileAlive` | 4 |
| `DisplayDangerAOE` | 4 |
| `Bird` | 4 |
| `AbilityAfterEnemyCastSpell_Stackable` | 4 |
| `ChangeTileOnPop` | 4 |
| `Maggot` | 4 |
| `GroundFlopper` | 4 |
| `AddMeleeKnockback` | 4 |
| `BackstabAllDirections` | 4 |
| `BaitAura` | 4 |
| `Trapper` | 4 |
| `CookedChickenLeg` | 4 |
| `WeremanTransformationReceiver` | 4 |
| `bishop_hat` | 3 |
| `CanMutateTo` | 3 |
| `BBTransformMutant` | 3 |
| `DigestDeadBodies` | 3 |
| `ThornUpX` | 3 |
| `move` | 3 |
| `MimicSpawnerAttacks` | 3 |
| `SupportFormChangeInsteadOfRun` | 3 |
| `BaseStatMultiply` | 3 |
| `MutateViaAbility` | 3 |
| `FormChangeHealthThreshold` | 3 |
| `ManaPickup` | 3 |
| `SharePickupsWithSpawner` | 3 |
| `RunInXTurns` | 3 |
| `CaveManTransform` | 3 |
| `TileTrail_Ahead` | 3 |
| `CerberubsShotgunReactionX` | 3 |
| `WaterTile` | 3 |
| `MinimumKnockbackFromPhysicalAttacks` | 3 |
| `BonusTurnPattern` | 3 |
| `PrioritizeHitDifferentTargets` | 3 |
| `AggroTargetIsCurrentTurn` | 3 |
| `TVOff` | 3 |
| `ArmorPickup` | 3 |
| `OilTile` | 2 |
| `MotherTumorSpawnInCapture` | 2 |
| `TransformWhenBuddyDies` | 2 |
| `ai` | 2 |
| `pickup` | 2 |
| `GoopWalk` | 2 |
| `KaijuWinCon` | 2 |
| `partial_animation_suffix` | 2 |
| `PrioritizeAggroTarget` | 2 |
| `ReaperRevenge` | 2 |
| `PrioritizeWeakestEnemy` | 2 |
| `UnlockOrientation` | 2 |
| `MamaCatAnimations` | 2 |
| `AggroTargetIsBuddy` | 2 |
| `SlotMachineRollPool` | 2 |
| `DemonicGlyphFrames` | 2 |
| `SafeDoomed` | 2 |
| `Shove` | 2 |
| `UseAbility` | 2 |
| `FormChangeDuringWeatherElement` | 2 |
| `DecoyExplode` | 2 |
| `Bomb_FuseLoop` | 2 |
| `ChangeTileOnDeath` | 2 |
| `PassiveWhileNotHasStatus` | 2 |
| `DefaultMove` | 2 |
| `MagicDamageImmune` | 2 |
| `Guillotina2Rage` | 2 |
| `BungaEntrance` | 2 |
| `StatusOnSpawnIn` | 2 |
| `BungaSwipe` | 2 |
| `FinalBossShield` | 2 |
| `TransformOnElementInfluencex` | 2 |
| `passives` | 2 |
| `ImmobilePassive` | 2 |
| `FaceLastDamage` | 2 |
| `SurviveAt1HP` | 2 |
| `CherubimReaction` | 2 |
| `PrioritizePlayerCats` | 2 |
| `LennyCatSlap` | 2 |
| `CanShield` | 2 |
| `MegafetusMelee` | 2 |
| `ChanceToDisableActionsIfNotCharmed` | 2 |
| `ExpireOnSpawnerTurnEnd` | 2 |
| `BiggestFood` | 2 |
| `MiniVolcanoReaction` | 2 |
| `AllDamageImmune_IncludingSpeculative` | 2 |
| `AbilityOnRoundEnd` | 2 |
| `GrenadeExplode` | 2 |
| `DissuadeInstakills` | 2 |
| `AlwaysHitDifferentTargets` | 2 |
| `DiesToElement` | 2 |
| `WideBackstab` | 1 |
| `BasicMelee_4Hits` | 1 |
| `BBExplode` | 1 |
| `ThrobbingKing2` | 1 |
| `SpewerSuckTar` | 1 |
| `TVBotDisableAttack` | 1 |
| `TakeWeaponFromSpawner` | 1 |
| `choose_favorite_cat` | 1 |
| `Attacker` | 1 |
| `ChubsGoop` | 1 |
| `SpreadWater` | 1 |
| `DisplayBuddyCatOnSpawn` | 1 |
| `MotherGrowController` | 1 |
| `FinalBossShieldHealth` | 1 |
| `Hyde` | 1 |
| `HPAltStates` | 1 |
| `BonusBirdsKilled` | 1 |
| `MoonHead_Digest` | 1 |
| `unlit_candle` | 1 |
| `DamageFromBehindOnly` | 1 |
| `GasCanBehavior` | 1 |
| `Twister_loop` | 1 |
| `TT_Thrash` | 1 |
| `MiniVolcano_Spurt` | 1 |
| `RunWhenKittensDead` | 1 |
| `DodgeChanceWithBlindSpot` | 1 |
| `StatusEachTurnBeginIfHasStatus` | 1 |
| `SCSneakUp` | 1 |
| `Tall` | 1 |
| `BlackHolePassive` | 1 |
| `ChanceToFormChangeOnAbilityDamage` | 1 |
| `DicerArt` | 1 |
| `WispDodge` | 1 |
| `DiceBehavior` | 1 |
| `SimonFlopper` | 1 |
| `Tatters` | 1 |
| `AggroTargetIsLowestHealthEnemyTillItDies` | 1 |
| `DybbukPossessionFallback` | 1 |
| `AddStatusToReceivedDamage` | 1 |
| `TrexSwitchTarget` | 1 |
| `Dybbuk1HPTracker` | 1 |
| `SproutsGrantMovement` | 1 |
| `RatKing` | 1 |
| `CrowAttackLink` | 1 |
| `tumor` | 1 |
| `BigUFO_ambient_looping` | 1 |
| `Legacy_Marshmallow_StolenCatID` | 1 |
| `CounterAttackAfterEnemyCastSpell` | 1 |
| `ChaosBossFormChangeGuide` | 1 |
| `GirlDinoCry` | 1 |
| `IllusionTint` | 1 |
| `LegacySpawnSavedCatIfExists` | 1 |
| `animation_suffix` | 1 |
| `Tarred` | 1 |
| `CatGoop` | 1 |
| `ManglerEnrage` | 1 |
| `MoonHeadCrackedVisual` | 1 |
| `NubsGoop` | 1 |
| `StatusEachTurnEndIfEnabledAtStartOfTurn` | 1 |
| `DieWhenSpawnerDies` | 1 |
| `Boulder` | 1 |
| `TeslaBolt` | 1 |
| `sprout` | 1 |
| `NoHead` | 1 |
| `ForceDodgeEverything` | 1 |
| `LoveBotCounter` | 1 |
| `None` | 1 |
| `HeadTumorResponse` | 1 |
| `EraseSpawnCoins` | 1 |
| `TVBotDisableSpells` | 1 |
| `YeticatSnowball_Counter` | 1 |
| `EnrageOnDamage` | 1 |
| `FlushmasterCelebration` | 1 |
| `TT_ManaBurn` | 1 |
| `SmallSlimeX` | 1 |
| `LockOrientationFaceTile` | 1 |
| `AbilityOnBattleStart_UseAI` | 1 |
| `Disguised` | 1 |
| `SpiderReturn` | 1 |
| `SpewerSuckNormal` | 1 |
| `MedSlimeX` | 1 |
| `Rage` | 1 |
| `OrthogonalAIDangerZone` | 1 |
| `ChaosHeadDropIn` | 1 |
| `MechExplode` | 1 |
| `BloatyExplodey` | 1 |
| `AlienBeastEyeStalks` | 1 |
| `TallTumorManaBurn` | 1 |
| `SlotMachine_DeathExplode` | 1 |
| `FormChangeWhenBuddyDies` | 1 |
| `TheCreator_SpawnCloneTeam` | 1 |
| `StatusWhenStatusCompletelyRemoved` | 1 |
| `ToxGasBlast` | 1 |
| `GlitchTile` | 1 |
| `CerberubsStraightReaction` | 1 |
| `HydrantFountain` | 1 |
| `GasCloudBehavior2` | 1 |
| `AllStatsAura` | 1 |
| `FinalBossHitCountdownHoly` | 1 |
| `BombBehavior` | 1 |
| `ScalingAttackAnimation` | 1 |
| `StatusOnEnemyConfused` | 1 |
| `TKNG_DeathExplode` | 1 |
| `TattersFear` | 1 |
| `BoyDinoCry` | 1 |
| `SpawnCreepOnHitKnockback` | 1 |
| `DivineShield` | 1 |
| `BasicAIDangerZone` | 1 |
| `TKNG_Hop` | 1 |
| `ShadowTile` | 1 |
| `CerberubsAggroTargetBehavior` | 1 |
| `zaratana` | 1 |
| `Chubs` | 1 |
| `DodgeWhenTargeted` | 1 |
| `TC_DashReaction` | 1 |
| `BungaCheers` | 1 |
| `BBTransformZealot` | 1 |
| `AvoidDamagingCharmedEnemies` | 1 |
| `TNTExplodey` | 1 |
| `GasserExplode` | 1 |
| `FaceAwayLastDamage` | 1 |
| `PackHunting` | 1 |
| `ManglerMonsterHeartAttack` | 1 |
| `CaveWomanDropTransform` | 1 |
| `AdvancedTint` | 1 |
| `BirthwortReactionShot` | 1 |
| `MegaDinoDropController` | 1 |
| `FinalBossBecomeTheChild` | 1 |
| `TransformOnStatusThreshold` | 1 |
| `TormentorRuneAbsorb` | 1 |
| `GoopImmunity` | 1 |
| `GirlDino` | 1 |
| `MegaGuppy_SummonTheChild` | 1 |
| `Wall` | 1 |
| `GSOpen` | 1 |
| `BloatEyeMovement2` | 1 |
| `fetus` | 1 |
| `SpewerSuckLava` | 1 |
| `ThrobShot_Reaction` | 1 |
| `BoyDino` | 1 |
| `BumbleButt` | 1 |
| `AggroTargetIsGovernedByHitEffect` | 1 |
| `grown_hitler_clone` | 1 |
| `GuillotinaDeathHead` | 1 |
| `CraterCreeperOut` | 1 |
| `ManglerMonsterPassive` | 1 |
| `FleshyMindConfusion` | 1 |
| `JohnnyNeedsWashing` | 1 |
| `Terminator2Run` | 1 |
| `StatusOverlappingCharactersAndDie` | 1 |
| `ChubsRage` | 1 |
| `Guillotina3Head` | 1 |
| `MoonHead_KillHands` | 1 |
| `Clot` | 1 |
| `Carcus` | 1 |
| `MuteDemonicGlyphDisplay` | 1 |
| `SpawnerCatDataReference` | 1 |
| `TireBehavior` | 1 |
| `FearMelee` | 1 |
| `FullBlockEverything` | 1 |
| `TVBotScreen` | 1 |
| `CollectiveCounter` | 1 |
| `AllSpellsCostActPoints` | 1 |
| `FinalBossSyncAnimations` | 1 |
| `BoneWormShotMed` | 1 |
| `ExtraTurnsPerTaggedUnit` | 1 |
| `BishopHat` | 1 |
| `SkipFirstRounds` | 1 |
| `TileElementDamageImmunity` | 1 |
| `Cracked` | 1 |
| `ModularPickup` | 1 |
| `MotherTumorPassive` | 1 |
| `Gamete` | 1 |
| `InvaderExplode` | 1 |
| `SyncFormsWithBuddy` | 1 |
| `DestroyerShieldBash` | 1 |
| `GeminiTwin` | 1 |
| `FinalBossHitCountdownBoris` | 1 |
| `TormentorHeal` | 1 |
| `TutorialBossRiggedFight` | 1 |
| `MultiSpawnOnDeath` | 1 |
| `FullBlockEverythingTo0Damage` | 1 |
| `LennyCatDies` | 1 |
| `Guillotina3Body` | 1 |
| `MoveAwayWhenEnemyAdjacent` | 1 |
| `UltraOrnstein` | 1 |
| `HealNeighborsEachTurn` | 1 |
| `Chummy` | 1 |
| `celebrate` | 1 |
| `DieWhenOnlyGolemsLeft` | 1 |
| `AlienBeastDangerZones` | 1 |
| `ThornUp` | 1 |
| `AggroTargetIsLastEnemyThatDealtDamage` | 1 |
| `AwardCoinsOnDeath` | 1 |
| `UseAbilityWhenOutOfStatus` | 1 |
| `T3Counter` | 1 |
| `IDBrambleBurst` | 1 |
| `DisguisedTrapper` | 1 |
| `SpewerAltGraphics` | 1 |
| `Dip` | 1 |
| `Nubs` | 1 |
| `AnkyloSpin` | 1 |
| `AggroTargetIsLowestMaxHealthCat` | 1 |
| `FinalBossBeamQueue` | 1 |
| `MoonHead_Blow` | 1 |
| `AdventureTokenPassivePool` | 1 |
| `BloatEyePassive2` | 1 |
| `DemonicGlyphStealer` | 1 |
| `ManglerMonsterExplode` | 1 |
| `BattlefieldUniqueRandomPassive` | 1 |
| `GametePop` | 1 |
| `RunWhenLastPlayerCatIsCharmed` | 1 |
| `HiddenDoomed` | 1 |
| `JohnnyWasher` | 1 |
| `DiesToPiercingAndSpikes` | 1 |
| `BlockAllDamage` | 1 |
| `MedSlime` | 1 |
| `pyrophina` | 1 |
| `TVBotDisableMove` | 1 |
| `ReturnBoundItemOnBattleEnd` | 1 |
| `cat` | 1 |
| `StartDead` | 1 |
| `Guillotina2Body` | 1 |
| `WhitelistPickupType` | 1 |
| `CanCreeperOut` | 1 |
| `TheChild_Wrath` | 1 |
| `Ornstein` | 1 |
| `uifloaters_offset` | 1 |
| `InsertIntoBackgroundPlaceholder` | 1 |
| `Digest` | 1 |
| `ManglerMonsterDashAttack` | 1 |
| `EventBounterHunterPassive` | 1 |
| `DeathWormTrampleDash_Reaction` | 1 |
| `UFO_BigExplode` | 1 |
| `HarpoonTrapPassive` | 1 |
| `TerminatorChase` | 1 |
| `MoonWormCurl` | 1 |
| `T3HitlerSpawningPhase` | 1 |
| `hitler_clone_fetus` | 1 |
| `TrackAmountKilledByPlayer` | 1 |
| `ElectricArcs` | 1 |
| `MoveAfterAnyAttemptedAttack` | 1 |
| `HCHumanDie` | 1 |
| `GlobalManaDrainAura` | 1 |
| `CloakerHex` | 1 |
| `DrMangler` | 1 |
| `IceBlockBehavior` | 1 |
| `MutateAfterXTurns` | 1 |
| `MiniNukeExplodey` | 1 |
| `Smough` | 1 |
| `DustCloudBehavior` | 1 |
| `UpTireBehavior` | 1 |
| `IDSprout` | 1 |
| `InheritSpawnerStats` | 1 |
| `UseAbilityWhenShieldDepleted` | 1 |
| `TwisterFling` | 1 |
| `HemBounce` | 1 |
| `ManglersMonster` | 1 |
| `TumorBarrier` | 1 |
| `TerminatorSkin` | 1 |
| `FinalBossHitCountdownExplosive` | 1 |
| `ChaosBossPieces` | 1 |
| `ElementWeakness` | 1 |
| `CaveCatDad` | 1 |
| `FlingObjectsOnTop` | 1 |
| `DisableSpells` | 1 |
| `Terminator2Chase` | 1 |
| `MulticatHeads` | 1 |
| `HarpoonTrapPull` | 1 |
| `Telekinesis` | 1 |
| `UnlimitedDeathRattleRevive` | 1 |
| `ToxPuff` | 1 |
| `UltraSmough` | 1 |
| `HitlerExecute` | 1 |
| `GA_PrimeExplode` | 1 |
| `Guillotina2Head` | 1 |
| `TinkererBasicAttackSwitching` | 1 |
| `CapReceivedDamage` | 1 |
| `BombFlyExplode` | 1 |
| `SwimmingFormChange` | 1 |
| `SupportDieInsteadOfRun` | 1 |
| `DivineShieldPickup` | 1 |
| `SmallSlime` | 1 |
| `CatPartsTransform` | 1 |
| `Mount` | 1 |
| `T3Pebbles_PrimeBoulderDrop` | 1 |
| `MonkCatReactionAbilities` | 1 |
| `FinalBossPupils` | 1 |
| `FrankPinky` | 1 |
| `ZeroKnockbackDamage` | 1 |

#### `elite_buffs.gon` (10 truly exclusive)

| :--- | :---: |
| Property | Count |
| `ToxicBubbles` | 1 |
| `NonChampionFlySwarm` | 1 |
| `SmokeBuff` | 1 |
| `StatusOnEnemyCastSpell` | 1 |
| `RemoveExtraDispersedTurn` | 1 |
| `ShineBuff` | 1 |
| `AbilityDamageMultiplier` | 1 |
| `FlyBuff` | 1 |
| `FireExtinguish_Steam` | 1 |
| `SandStormBuff` | 1 |

#### `item_setbonuses.gon` (28 truly exclusive)

| :--- | :---: |
| Property | Count |
| `SpawnCatCopyWhenDowned` | 2 |
| `Paper` | 2 |
| `StatusOnSetPieceBreak` | 2 |
| `UpgradeTaggedSpawnsToChampions` | 2 |
| `AdvancedAlloy` | 1 |
| `DoubleCastSpellsEachTurn_Status` | 1 |
| `CyborgTurns` | 1 |
| `Wood` | 1 |
| `AddConstitution` | 1 |
| `GlobalFlowerTrapperAura` | 1 |
| `GlobalFamiliarMoveBoost` | 1 |
| `EliteAlloy` | 1 |
| `MaxTeleport` | 1 |
| `Cardboard` | 1 |
| `Lucky` | 1 |
| `RockyArmorSalvage` | 1 |
| `Cool` | 1 |
| `AddStatusToFirstSpellEachTurn` | 1 |
| `TriggerBleedOnBleed` | 1 |
| `JankAlloy` | 1 |
| `GlobalFamiliarDamageBoost` | 1 |
| `Alloy` | 1 |
| `OverManaReducesManaCosts` | 1 |
| `Bionic` | 1 |
| `worm` | 1 |
| `BonusHealthRegenPerDisorder` | 1 |
| `set_SpaceArmorJump` | 1 |
| `set_WitchJump` | 1 |

#### `items` (156 truly exclusive)

| :--- | :---: |
| Property | Count |
| `Brittle` | 24 |
| `Fragile` | 22 |
| `StatusOnBreak` | 22 |
| `water` | 14 |
| `Flammable` | 13 |
| `PassiveIfStrAuxEquals` | 7 |
| `DurabilityTransform` | 7 |
| `BrittleDuringElement` | 7 |
| `ItemAuxTransform` | 6 |
| `TransformItemOnElementInfluence` | 5 |
| `SpellDamageUp` | 5 |
| `StatusOnTakeHealthOrShieldDamage` | 4 |
| `BreakAtAux` | 4 |
| `FragileDuringElement` | 4 |
| `RandomSeededStatModifier` | 4 |
| `StatusRandomEnemiesOnBattleStart` | 4 |
| `AddEndOfCombatRegen` | 3 |
| `ChanceToBlock` | 3 |
| `TrueShot` | 3 |
| `BoneArmorPassive` | 3 |
| `DropAsFamiliarOnArmorBreak` | 3 |
| `BreakOnElement` | 3 |
| `AllStatsUpPerDisorder` | 3 |
| `CopyPassiveSlot` | 3 |
| `CantSpreadDiseases` | 3 |
| `CharmedTinyTumor` | 3 |
| `StatusAllCharactersOnSpawn` | 3 |
| `StackingFlowerTrail` | 3 |
| `CantCatchDiseases` | 3 |
| `RockyArmorPassive` | 3 |
| `DisablePassiveSlot` | 2 |
| `CanLevelUpWhenDead` | 2 |
| `ArmorBreakOnHit` | 2 |
| `Uncontrollable` | 2 |
| `RefreshEquipmentAbilityOnElement` | 2 |
| `BreakWhenNoShield` | 2 |
| `StatusOnBackstab` | 2 |
| `SpawnItemLinkedFamiliar` | 2 |
| `euphoric` | 2 |
| `PassiveIfWeaponIsUsable` | 2 |
| `LeaveBehindOnceEachMove` | 2 |
| `CharmedPooter` | 2 |
| `StatusIfUnusedActPoints` | 2 |
| `SpawnNearEnemies` | 2 |
| `CharmedFlySwarm` | 2 |
| `ReduceSpellCostsPerParasite` | 1 |
| `PassiveWhileShielded` | 1 |
| `BasicMetronome` | 1 |
| `ReclaimItemOnBreak` | 1 |
| `TintItem` | 1 |
| `face_FartFace` | 1 |
| `face_EatNeverstone` | 1 |
| `CharmImmunity` | 1 |
| `AlwaysChosenForLevelUp` | 1 |
| `AlphaAllStatsUp` | 1 |
| `AlluringDoodieEater` | 1 |
| `head_HeadBrandJump` | 1 |
| `wp_TheLonerAuto` | 1 |
| `RandomDualSoulLink` | 1 |
| `PreventSpecificInjury` | 1 |
| `StatusOnDodge` | 1 |
| `SetFaction` | 1 |
| `ScaledStatusOnHolyShieldBlock` | 1 |
| `CapBasicAttackDamage` | 1 |
| `DoubleReceivedPositiveStatus` | 1 |
| `basic_attack` | 1 |
| `HeadGrubFamiliar` | 1 |
| `BlockNegativeStatus` | 1 |
| `Scrap` | 1 |
| `StatusOnEnemyDeath` | 1 |
| `TunnelVision` | 1 |
| `BasicTankMelee` | 1 |
| `StripKnockback` | 1 |
| `the_nuke_bearer` | 1 |
| `CatPartsSizeScale` | 1 |
| `CharismaIsMaxStat` | 1 |
| `CounterNextAttacks` | 1 |
| `CharmedCultist` | 1 |
| `RerollItemsOnBattleEnd` | 1 |
| `AOEBonus` | 1 |
| `combat_reward_easy` | 1 |
| `SpawnCatCloneOnCorpsePopped` | 1 |
| `AbilityOnRoundEndOnce` | 1 |
| `head_SpiderInjectorFixed` | 1 |
| `ExcludeFromEvents` | 1 |
| `AllyDodgeChanceAura` | 1 |
| `CharmedGamete` | 1 |
| `AIControlNextTurn` | 1 |
| `DropSoulJarOnDeath` | 1 |
| `ObjectDetector` | 1 |
| `tk_PetrifiedPinky` | 1 |
| `enemies` | 1 |
| `FaceGrubFamiliar` | 1 |
| `Coin` | 1 |
| `Charge` | 1 |
| `CharmedSpookie` | 1 |
| `ChanceToAmbush` | 1 |
| `BasicExplosiveShot` | 1 |
| `DropAsFamiliarOnTookDamage` | 1 |
| `AddAdvantageToEvent` | 1 |
| `BoostReceivedHealing` | 1 |
| `IsaacBasicAttack` | 1 |
| `AllUnitsExplodeOnDeath` | 1 |
| `SoulJar_Full` | 1 |
| `Catnip` | 1 |
| `Tragedy` | 1 |
| `StatusOnFullMana` | 1 |
| `StevenBolts` | 1 |
| `ChanceToForceEvent` | 1 |
| `AlliesScrambleSpellAfterCast` | 1 |
| `GlobalMeleeRevengeDamage` | 1 |
| `ModelingClayPassive` | 1 |
| `JesterLevelUpRerolls` | 1 |
| `StatusAdjacentOnTheirTurnEnd` | 1 |
| `MultiplyCoinsOnBattleStart` | 1 |
| `GlassTile` | 1 |
| `Lifesteal` | 1 |
| `WasteTime` | 1 |
| `face_LeechBrood` | 1 |
| `PhysicalAttacksMiss` | 1 |
| `ReplaceBlankTilesOnBattleStart` | 1 |
| `AddStatusToBackstabs` | 1 |
| `ReduceManaCost` | 1 |
| `CharmedReaper` | 1 |
| `SpawnRandomPickupsOnTaggedUnitKilled` | 1 |
| `head_Pestilence` | 1 |
| `StatDependentPassive` | 1 |
| `ConvertDamageToScaledStatus` | 1 |
| `PhantomMaskRock` | 1 |
| `ReduceSpellCostsPerDisorder` | 1 |
| `BlockDamageUnderThreshold` | 1 |
| `all_spells` | 1 |
| `ScaldingOrbMoonBossOneShot` | 1 |
| `PassiveWhileHasDurability` | 1 |
| `head_SpiderInjector` | 1 |
| `ScaledStatusAlliesOnSpendMana` | 1 |
| `ExtraBasicAttacks_Status` | 1 |
| `BasicPoke` | 1 |
| `neck_NukeBonus` | 1 |
| `neck_NukeExplode` | 1 |
| `BasicSpin` | 1 |
| `FrankBolts` | 1 |
| `DoubleCastSpellIfManaCostUnderThreshold` | 1 |
| `StatusAlliesEachTurn` | 1 |
| `DoubleCastTaggedSpells` | 1 |
| `MultiplyReceivedHealing` | 1 |
| `TheIntruder` | 1 |
| `head_EmoSong` | 1 |
| `BuffCharmedKitten` | 1 |
| `BalanceStats` | 1 |
| `StatusOnFallAsleep` | 1 |
| `NeckGrubFamiliar` | 1 |
| `AllSpellsCostCharge` | 1 |
| `DoubleReceivedNegativeStatus` | 1 |
| `face_FartFaceFixed` | 1 |
| `HideSomeHudStuff` | 1 |

#### `mutations` (21 truly exclusive)

| :--- | :---: |
| Property | Count |
| `CharmedKitten` | 4 |
| `ReplaceBasicMove_Mutation` | 3 |
| `CharmedFly` | 3 |
| `catnip` | 2 |
| `Immobile` | 2 |
| `RandomStatUp` | 1 |
| `DrinkWater` | 1 |
| `Bottles` | 1 |
| `SwapHighestAndLowestStat` | 1 |
| `GainManaWhenAnythingDies` | 1 |
| `StatusIfDidntMove` | 1 |
| `Gravity` | 1 |
| `StatusEveryXSpellCastsEachTurn` | 1 |
| `BackstabFront` | 1 |
| `FetusSpit` | 1 |
| `WaterBottle_Full` | 1 |
| `ReplaceBasicAttack_Mutation` | 1 |
| `AddLootMultiplier` | 1 |
| `SkunkTail` | 1 |
| `FlatHealWhenDealDamage` | 1 |
| `BasicDig` | 1 |

#### `passives` (354 truly exclusive)

| :--- | :---: |
| Property | Count |
| `PassiveLevelUpAtCombatEnd` | 10 |
| `ForceSpecificInjury` | 8 |
| `StatusOnCrit` | 8 |
| `PassiveIfAllArmorEmpty` | 8 |
| `PassiveIfEmptyHead` | 7 |
| `PassiveIfEmptyNeck` | 7 |
| `BlastResistance` | 7 |
| `DamageNeighborsOnEndMove` | 7 |
| `StatusOnUseAbilityWithTag` | 7 |
| `PassiveIfEmptyFace` | 7 |
| `ManaCostReductionTagged` | 6 |
| `ReplaceBasicAttackWhenCastable` | 6 |
| `AddStatusToElementAbilities` | 6 |
| `BasicAttackDamageMultiplier` | 6 |
| `StatusOnStanceSwitch` | 6 |
| `Colorless` | 6 |
| `StatusOnOverHealed` | 5 |
| `BasicAttackAOEBonus` | 5 |
| `CharmedTinySpider` | 5 |
| `AddDamageToBasicAttack` | 4 |
| `StatusOnTurnEndIfManaOrHealthExact` | 4 |
| `AllyBonusAbilityAura` | 4 |
| `AllyManaRegenAura` | 4 |
| `StatusOnTurnEndIfManaExact` | 4 |
| `BasicMonkMelee` | 3 |
| `ConsumablesInfiniteRange` | 3 |
| `AutocastEachTurnBegin` | 3 |
| `CobraReflex` | 3 |
| `UncappedMana` | 3 |
| `CharmedDemonKitten` | 3 |
| `PermanentItems` | 2 |
| `EnergyStorm` | 2 |
| `CatAPultAnimation` | 2 |
| `PassiveAtInjuryThreshold` | 2 |
| `BasicMedicRanged` | 2 |
| `ShareHealthRegen` | 2 |
| `StatusOnGainShield` | 2 |
| `EquipmentPassiveMultiplierBonus` | 2 |
| `IncreaseHealingSpellRange` | 2 |
| `Study` | 2 |
| `PassiveUntilCastSpell` | 2 |
| `NoReflection` | 2 |
| `GravityWell` | 2 |
| `StrengthForEachNeighboringEnemy` | 2 |
| `FullHealthCritChance` | 2 |
| `OverhealGainsBothShield` | 2 |
| `LateBloomer` | 2 |
| `FamiliarSecondaryDamageImmunity` | 2 |
| `SpreadExtraDebuffs` | 2 |
| `BasicMagicMissile` | 2 |
| `LightningRod` | 2 |
| `DamageReductionAura` | 2 |
| `StatusAnyCatAllyWhoKills` | 2 |
| `BraceForEachNeighboringEnemy` | 2 |
| `ScaledStatusOnOverMana` | 2 |
| `StatusOnAnyDeath` | 2 |
| `EnemiesGetPickupsKnockedOut` | 2 |
| `AddPassivesToSummonAbilityMinions` | 2 |
| `Quiver` | 2 |
| `LobbedHook` | 2 |
| `StatusAlliesOnGainCoins` | 2 |
| `spd` | 2 |
| `StatusOnTriggerTrap` | 2 |
| `FeralMelee` | 2 |
| `RobotsInheritArmor` | 2 |
| `DamageEnemiesOnHeal` | 2 |
| `Haunt` | 2 |
| `RemoveOncePerFightRestriction` | 2 |
| `StatusOnHeal` | 2 |
| `CharmAllFlies` | 2 |
| `FlowerTile` | 2 |
| `SmallEnemiesIgnoreYou` | 2 |
| `AllyMultiplyKnockbackDamage` | 2 |
| `ShoulderCheck` | 2 |
| `StatusThingsKnockedBack` | 2 |
| `PassiveWhileWearingMetal` | 2 |
| `FlowerPowerAuraStrength` | 2 |
| `Necro_SoulDagger_Uncharged` | 2 |
| `TileDamageMultiplier` | 2 |
| `AddSpellDamage` | 2 |
| `HealDamagesEnemies` | 2 |
| `AbsorbManaAura` | 2 |
| `BasicSuplex` | 2 |
| `Empath` | 2 |
| `AfterImage` | 2 |
| `SplittableMove` | 2 |
| `UpgradeLevelUpClassPassives` | 2 |
| `BasicAttackStatusCarefulness` | 2 |
| `BoobyTrapItems` | 2 |
| `StatusOnOverMana` | 2 |
| `ShovingMatch` | 2 |
| `Tech` | 2 |
| `EscapeSequence` | 2 |
| `Druid` | 2 |
| `Psychic` | 2 |
| `Conductor` | 2 |
| `Grass` | 2 |
| `DamageNeighborTilesWhenCastSpell` | 2 |
| `Medic` | 2 |
| `AddStatusToMeleeDamage` | 2 |
| `StatusEveryXTurnBegins` | 2 |
| `PassiveAtFullHealth` | 2 |
| `StatusReplacement` | 2 |
| `MakeBasicAttackPassThroughThings` | 2 |
| `DeathChill` | 2 |
| `MegaMinions` | 2 |
| `ConjureCastSpellsForAllies` | 2 |
| `DukeOfFlies` | 2 |
| `StatusAlliesOnKill` | 2 |
| `MetalDetector` | 2 |
| `StatusOnBattleEndIfKillThresholdMet` | 2 |
| `HolyShieldTransferToTaggedMinions` | 2 |
| `ElementalAttunement` | 2 |
| `Monk` | 2 |
| `Vengeful` | 2 |
| `TowerDefense` | 2 |
| `Tank` | 2 |
| `NubbyTossPriority` | 2 |
| `Necromancer` | 2 |
| `StatusKillers` | 2 |
| `TaggedPickupEffectReplacement` | 2 |
| `StatsAtLowHealth` | 2 |
| `ChainKnockback` | 2 |
| `HealsAlsoRegenMana` | 2 |
| `StatusEnemiesOnDeath` | 2 |
| `PassiveWhileInMonkRangedStance` | 2 |
| `StatusAllyWhenAllySpendsMana` | 2 |
| `UpgradeLevelUpClassActives` | 2 |
| `BasicDruidAbilityVersatile` | 2 |
| `SpecialFriends` | 2 |
| `AllyDamageReaction` | 2 |
| `ChangeTauntPriority` | 2 |
| `CollectPickupsOnBattleEnd` | 2 |
| `CapDamageFromAllies` | 2 |
| `StatusOnDealtDamageThreshold` | 2 |
| `StatusDamagers` | 2 |
| `AddWeaponScaling` | 2 |
| `PassiveUntilGetKill` | 2 |
| `RockDetector` | 2 |
| `ImmortalLeeches` | 2 |
| `cha` | 2 |
| `FlowerPowerAuraBrace` | 2 |
| `Tinkerer` | 2 |
| `GrassTile` | 2 |
| `StatusOnTookDamageFromEnemyAbility` | 2 |
| `AllyHealthRegenAura` | 2 |
| `AddStatusToFirstBasicAttack` | 2 |
| `bowling_ball` | 2 |
| `AllowPassTurn` | 2 |
| `LineOfSightTrueSightAura` | 2 |
| `ButcherHook_Temporary` | 2 |
| `NumbingLeeches` | 2 |
| `ReviveOnWin` | 2 |
| `AmplifyPositiveStatus` | 2 |
| `AlternateCraftingPools` | 2 |
| `StatusEachTurnEndPerEnemyKill` | 2 |
| `StrengthInNumbersAura` | 2 |
| `StatMinimum` | 2 |
| `Rot` | 2 |
| `Dyslexia` | 2 |
| `PassiveWhilePreviewingMonkRangedStance` | 2 |
| `BonusFoodEachBattle` | 2 |
| `AddPassiveToSpawnedRocks` | 2 |
| `PassiveWhenTheAlpha` | 2 |
| `AddStatusToExplosions` | 2 |
| `AllyMoveAbilityAura` | 2 |
| `EquipmentSetBonusBonus` | 2 |
| `AddStatusToAllDamageAbilities` | 2 |
| `ExplodeOverkilledEnemies` | 2 |
| `StatusPerInjury` | 2 |
| `LightningAspectCharge` | 2 |
| `lck` | 2 |
| `AddStatusToTrampleDamage` | 2 |
| `NubbyToss` | 2 |
| `AutocastEachTurn` | 2 |
| `DejaVu` | 2 |
| `Butcher` | 2 |
| `TrapEffectsMultiplier` | 2 |
| `CoinsAddDamage` | 2 |
| `WeaponCountsAsBasicAttack` | 2 |
| `ParasitesArentCursed` | 2 |
| `HealsCanRevive` | 2 |
| `Weakness` | 2 |
| `LowHealthAllyDodgeChanceAura` | 2 |
| `EMP` | 2 |
| `SpreadPainBonus` | 2 |
| `Stealth` | 2 |
| `MinimumTech` | 2 |
| `Earth` | 2 |
| `AutoCritLowDamage` | 2 |
| `SmiteEnemiesWhoKill` | 2 |
| `FullPower` | 2 |
| `StatusOnDealtDamage` | 2 |
| `KillsHeal` | 2 |
| `DamageEnemiesOnKill` | 2 |
| `StatusOnUseElementAbility` | 2 |
| `FollowUp` | 2 |
| `DirtyClaws` | 2 |
| `AddStatusToBasicAttackWithCooldown` | 2 |
| `ReplaceBasicAttackWhenDead` | 2 |
| `Seppuku` | 2 |
| `ManaRegenMultiplierIfManaEmpty` | 2 |
| `BoostAllyStatsOnDeath` | 2 |
| `FrontstabCritChance` | 1 |
| `FurnitureStats` | 1 |
| `BasicDashAttackMove` | 1 |
| `Triskaidekaphobia` | 1 |
| `AbilityChargeRefundChance` | 1 |
| `CantDodge` | 1 |
| `AmplifyNegativeStatus` | 1 |
| `FollowUpDash2` | 1 |
| `BoostRangeGlobalAura` | 1 |
| `SleepDart` | 1 |
| `HolyDamageMultiplierBonus` | 1 |
| `DarkOneStrike` | 1 |
| `Autism` | 1 |
| `Heathens2` | 1 |
| `MindCrack_EldritchVisage2` | 1 |
| `SwapPositions_WideLoad` | 1 |
| `MaxStartingMana` | 1 |
| `ReplaceBrain` | 1 |
| `Shank2` | 1 |
| `RandomReap` | 1 |
| `Hypomania` | 1 |
| `Doomed` | 1 |
| `BoostRangeAura` | 1 |
| `ScaledStatusOnOverHealed` | 1 |
| `PassiveLevelScaledStatus` | 1 |
| `StatusOnTakeHealthDamage` | 1 |
| `FoodBig` | 1 |
| `StatusAlliesScaledByCursedOnDeath` | 1 |
| `GrassTileHealing` | 1 |
| `LimitSelfKnockbackDamage` | 1 |
| `StatusOnLoseShield` | 1 |
| `neck_ChefsApron` | 1 |
| `InvertBrainFaction` | 1 |
| `BasicMelee` | 1 |
| `Madness` | 1 |
| `TourettesMeows` | 1 |
| `FullHealthManaRegen` | 1 |
| `AlliesAvoidTraps` | 1 |
| `SleepDart2` | 1 |
| `AddKnockbackToEverything` | 1 |
| `FreeSpellsAtFullMana` | 1 |
| `AddRangedCritChance` | 1 |
| `ParanoiaBasicMelee` | 1 |
| `RealTimePressure_OneUnit` | 1 |
| `FighterBonusThrow` | 1 |
| `OverrideMaxMana` | 1 |
| `MegaFart` | 1 |
| `PissYourself` | 1 |
| `BonusToss` | 1 |
| `LimitedTileTrail` | 1 |
| `BonusRangeBasedOnDex` | 1 |
| `AddAllyNeighborsToAbilityRange` | 1 |
| `AllyMultiplyKnockbackDistance` | 1 |
| `Spook` | 1 |
| `Gassy_AssBlast` | 1 |
| `WobblyCat` | 1 |
| `FoodMedium` | 1 |
| `BackstabWeakness` | 1 |
| `BoostDamageAura` | 1 |
| `BasicButcherMeleeWideDoubleSpin` | 1 |
| `GerdShot` | 1 |
| `EachSpellFreeAtFullMana` | 1 |
| `SpreadPainBonusCrit` | 1 |
| `NoManaRegen` | 1 |
| `TauntAtFullHealth` | 1 |
| `BasicAttackStatusSwap` | 1 |
| `insane` | 1 |
| `SwapPositions_WideLoad2` | 1 |
| `Groom` | 1 |
| `RandomReap2` | 1 |
| `EatShit` | 1 |
| `StackingDodgeChanceOnTookDamage` | 1 |
| `ForceUseAbility` | 1 |
| `Hone2` | 1 |
| `FullHealthAllStatsUp` | 1 |
| `AddStatusesToReceivedElementalDamage` | 1 |
| `MoveRandomly` | 1 |
| `SpawnMeatOnMove` | 1 |
| `AddLevelUpStatMultiplier` | 1 |
| `ExhaustionRoundChange` | 1 |
| `SafeExplosions` | 1 |
| `Hone` | 1 |
| `MockingbirdForm` | 1 |
| `AllyChainKnockback` | 1 |
| `ViolentOutburst` | 1 |
| `AddTemporaryEffectsToEquipment` | 1 |
| `PlayerCat_ThiefShade` | 1 |
| `BonusHealthRegenBasedOnDex` | 1 |
| `TempInitiativeChange` | 1 |
| `StrictLimitDamage` | 1 |
| `PlayerCat_ThiefShade2` | 1 |
| `AddStatusToReceivedDamage_ExcludeStatuses` | 1 |
| `AddChaScalingSpellDamage` | 1 |
| `SelfDamageWhenDealDamage` | 1 |
| `Shank` | 1 |
| `ReflexPunchJab` | 1 |
| `BasicButcherMeleeWideSpin` | 1 |
| `MaxAccuracy` | 1 |
| `Heathens` | 1 |
| `MindCrack_EldritchVisage` | 1 |
| `Gassy_AssBlast2` | 1 |
| `RefreshMoveOnWeaponConnect` | 1 |
| `BasicRanged_1DMG` | 1 |
| `AllyUncappedHPAura` | 1 |
| `AllDamageCrits` | 1 |
| `UncappedHPBonusStr` | 1 |
| `HealingAura` | 1 |
| `OverridePalette` | 1 |
| `ConsumablesMeleeRange` | 1 |
| `ScaledStatusOnLoseShield` | 1 |
| `Paranoia` | 1 |
| `ConductorManaRegen` | 1 |
| `StatusAlliesOnSpendMana` | 1 |
| `SchrodingerDisorder` | 1 |
| `HealAtStart` | 1 |
| `TheHunger` | 1 |
| `ReceivedStatusReplacement` | 1 |
| `CapTechSpent` | 1 |
| `Scleroderma` | 1 |
| `ReplaceSpellsWhenDead` | 1 |
| `FrontstabBasicAttackCritChance` | 1 |
| `ConfusionEffectOnTaggedAbilities` | 1 |
| `FullHeal` | 1 |
| `BonusToss2` | 1 |
| `ReflexPunchJab2` | 1 |
| `CatapultJump2` | 1 |
| `BoostDamageGlobalAura` | 1 |
| `IncreaseItemUsesOnEquip` | 1 |
| `RandomSoulLink` | 1 |
| `PermanentImmobile` | 1 |
| `CatapultJump` | 1 |
| `AddAllyNeighborsToAttackRange` | 1 |
| `weapons` | 1 |
| `StatusIfBattleAlreadyBegan` | 1 |
| `PoisonMultiplier` | 1 |
| `Diabetes` | 1 |
| `StatusCarefulness` | 1 |
| `PermanentKitten` | 1 |
| `meat` | 1 |
| `any` | 1 |
| `SlitWrists` | 1 |
| `ExtraInjuryOnDeath` | 1 |
| `DamageIfDidntUseSpecificAbility` | 1 |
| `GrowHead` | 1 |
| `FollowUpDash` | 1 |
| `Bloodzerk` | 1 |
| `Cannibalize` | 1 |
| `ScaledStatusOnBleedDamage` | 1 |
| `StatusAdjacentOnTheirTurnBegin` | 1 |
| `crow` | 1 |
| `AddStatusesIfPersistentWeatherElement` | 1 |

#### `tutorial_cats.gon` (3 truly exclusive)

| :--- | :---: |
| Property | Count |
| `passive0` | 2 |
| `HotBlooded` | 1 |
| `SelfAssured` | 1 |

---

## Block: `effects`

**9 categories** | **754 total unique properties**

- Universal (all 9 cats): **0**
- Partially shared (2–8 cats): **35**
- Truly exclusive (1 cat only): **719**

**Categories:** `abilities`, `boss_elite_buffs.gon`, `characters`, `elite_buffs.gon`, `item_setbonuses.gon`, `items`, `mutations`, `passives`, `weather.gon`

### Partially Shared Properties

| :--- | :--- | :---: |
| `Stun` | `abilities`, `characters`, `items`, `passives` | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. |
| `Burn` | `abilities`, `boss_elite_buffs.gon`, `characters`, `items`, `passives`, `weather.gon` | The amount of Burn applied, either as a fixed number or a formula string. | 1 
| `Bruise` | `abilities`, `item_setbonuses.gon`, `items`, `passives` | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 
| `Poison` | `abilities`, `items`, `passives` | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 
| `Bleed` | `abilities`, `passives` | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 
| `Confusion` | `abilities`, `characters`, `items`, `mutations` | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 
| `VisualFXTile` | `abilities`, `boss_elite_buffs.gon`, `elite_buffs.gon`, `items`, `passives` | Specifies the name of the visual effect to play on the target tile. |
| `BounceObject` | `abilities`, `items` | Specifies the object or projectile to spawn and bounce from the target. |
| `Fear` | `abilities`, `items`, `mutations`, `passives` | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. |
| `Slow` | `abilities`, `items`, `passives` | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 
| `Blind` | `abilities`, `items`, `mutations`, `weather.gon` | The amount of blind stacks applied, or an [stacks, probability] array. | 6 
| `Immobile` | `abilities`, `items`, `passives` | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 
| `Weakness` | `abilities`, `passives` | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 
| `Charmed` | `abilities`, `mutations`, `passives` | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. |
| `ConstitutionUp` | `abilities`, `characters` | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. |
| `Vaporize` | `abilities`, `characters` | Removes the target from play, preventing its corpse from being interacted with. |
| `Freeze` | `abilities`, `items`, `passives` | The amount of freeze stacks applied, or an [stacks, probability] array. |
| `Madness` | `abilities`, `passives` | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. |
| `Petrify` | `abilities`, `mutations`, `passives` | The amount of petrify stacks applied, or an [stacks, probability] array. |
| `WaterConduct` | `abilities`, `boss_elite_buffs.gon`, `elite_buffs.gon`, `items`, `passives` | Specifies whether an ability or item conducts electricity through water tiles. |
| `Conditional_GoodRoll` | `abilities`, `items` | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. |
| `Leeches` | `abilities`, `passives` | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 
| `RandomStatusFromPool` | `abilities`, `mutations` | A collection of status effects; one is randomly chosen and applied to the target. |
| `Cleave` | `abilities`, `items` | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. |
| `Thorns` | `abilities`, `characters` | The amount of thorns damage dealt to attackers on hit. | 36 
| `Marked` | `abilities`, `passives` | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. |
| `VisualFX` | `abilities`, `items` | Specifies the name of the visual effect to play. |
| `Grappled` | `abilities`, `items` | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. |
| `SpreadDisease` | `abilities`, `passives` | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. |
| `Tarred` | `abilities`, `boss_elite_buffs.gon`, `elite_buffs.gon` | The amount of tarred stacks applied, or an [stacks, probability] array. |
| `BurnTrigger` | `abilities`, `passives` | Specifies an ability or passive that triggers a burn effect. |
| `Holy` | `abilities`, `weather.gon` | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. |
| `Bolt` | `abilities`, `items` | Specifies a bolt-type ability or item effect. | 2 
| `CharmedDip` | `abilities`, `items` | The number of charmed dip pickups spawned. |
| `VisualFlySwarm` | `abilities`, `weather.gon` | If non-zero, enables the visual fly swarm effect on the unit. |
| Property | Categories | Total Uses |

### Truly Exclusive Properties (one category only)

#### `abilities` (674 truly exclusive)

| :--- | :---: |
| Property | Count |
| `FormChange` | 102 |
| `IgnoreSelf` | 75 |
| `ChangeTile` | 62 |
| `Else` | 59 |
| `Shield` | 49 |
| `Cleanse` | 44 |
| `Conditional_HasTag` | 38 |
| `Conditional_Enemy` | 35 |
| `SpeedUp` | 34 |
| `Temporary` | 34 |
| `AllStatsUp` | 29 |
| `DamageUp` | 28 |
| `TransformAbility` | 28 |
| `ApplyToSource` | 27 |
| `ManaGain` | 26 |
| `Conditional_Ally` | 25 |
| `Leech` | 22 |
| `StrengthUp` | 22 |
| `EvolveAbilityFromPool` | 21 |
| `IntelligenceUp` | 21 |
| `Sleep` | 21 |
| `Brace` | 18 |
| `RandomStatUp` | 17 |
| `KnockUpAndAway` | 17 |
| `CollectsPickups` | 17 |
| `OverrideKnockbackDamage` | 16 |
| `VaporizeCorpse` | 15 |
| `Consumed` | 15 |
| `TransformBasicAttack` | 14 |
| `ChangeCatClass` | 14 |
| `FaceAway` | 14 |
| `DivineShield` | 14 |
| `TakeExtraTurn` | 14 |
| `EndTurn` | 14 |
| `RefreshMovePoints` | 14 |
| `RandomMagicMissile` | 13 |
| `GenericDebuff` | 13 |
| `Conditional_Boss` | 13 |
| `CatPartsTransform` | 13 |
| `LuckUp` | 12 |
| `Displace` | 12 |
| `SmallRock` | 12 |
| `X` | 12 |
| `ChanceToBreakFree` | 11 |
| `DoScreenShake` | 11 |
| `ApplyToSourceOnKill` | 11 |
| `WaterTile` | 11 |
| `item_aux` | 11 |
| `FullHeal` | 11 |
| `PurgeAll` | 10 |
| `RefreshActPoints` | 10 |
| `Conditional_FormulaIsPositive` | 10 |
| `MagicWeakness` | 10 |
| `Conditional_Speculative` | 10 |
| `DexterityUp` | 10 |
| `PartialPurge` | 10 |
| `Ammo` | 9 |
| `ApplyPassives` | 9 |
| `GlassTile` | 9 |
| `SpawnCreep` | 9 |
| `DeferVaporize` | 9 |
| `HealthRegenUp` | 8 |
| `LavaTile` | 8 |
| `ChanceToBreak` | 8 |
| `CanApplyToInanimate` | 8 |
| `Rot` | 8 |
| `PoisonPoof` | 8 |
| `OverrideChainKnockback` | 8 |
| `ManaSteal` | 7 |
| `AlphaCat` | 7 |
| `ApplyStatusIfCrit` | 7 |
| `TempRangeUp` | 7 |
| `Tech` | 7 |
| `ContextualHeal` | 7 |
| `KnockbackDamageImmuneUntilSettled` | 7 |
| `ForceAttack` | 7 |
| `BramblesOnHit` | 7 |
| `TriggerWerewolfTransform` | 7 |
| `Instakill` | 7 |
| `ObjectOnHitCharacter` | 6 |
| `Metronome` | 6 |
| `ConjureBonusAbility` | 6 |
| `Conditional_Corpse` | 6 |
| `Craft` | 6 |
| `TwisterDisplaceWithDamage` | 6 |
| `BounceRock` | 6 |
| `DoDistortionRing` | 6 |
| `TeamCastAbility` | 6 |
| `BackflipWhenTargeted` | 6 |
| `SetDistanceDisplace` | 6 |
| `ClearStarving` | 6 |
| `RemoveStatus` | 6 |
| `SpiderInfested` | 6 |
| `true` | 6 |
| `Drowsy` | 6 |
| `RandomInjury` | 6 |
| `CharismaUp` | 6 |
| `SetHealth` | 6 |
| `ScatterHeldCoin` | 6 |
| `SpawnThingIfHitKills` | 6 |
| `Purge` | 5 |
| `Revive` | 5 |
| `ForceMoveAway` | 5 |
| `Webbed` | 5 |
| `PopAndSpawn` | 5 |
| `FillMana` | 5 |
| `FlatLeech` | 5 |
| `MonkStanceSwitch` | 5 |
| `SafeDie` | 5 |
| `SoulLink` | 5 |
| `MovementUp` | 5 |
| `Conditional_PlayerCat` | 5 |
| `RefreshMovePointsIfHit` | 5 |
| `ObjectOnHitEmpty` | 5 |
| `UpgradeRandomAbility` | 5 |
| `KnockbackDirectionIsFacingDirection` | 5 |
| `Conditional_NotBoss` | 5 |
| `Imprison` | 5 |
| `HitExplosion` | 5 |
| `ObjectOnHit` | 5 |
| `Conditional_InForm` | 5 |
| `ForceMoveTowards` | 5 |
| `Conditional_HasStatus` | 5 |
| `CollectsPickupsWithAltEffects` | 5 |
| `SpawnBearTrap` | 5 |
| `Stealth` | 5 |
| `TempDamageUp` | 5 |
| `Conditional_Object` | 5 |
| `DodgeChance_Status` | 5 |
| `SpawnRock` | 5 |
| `FaceCamera` | 4 |
| `Die` | 4 |
| `TallGrassTile` | 4 |
| `ArcLightning` | 4 |
| `UseAbility` | 4 |
| `VaporizeInanimate` | 4 |
| `ZombieCatFamiliar` | 4 |
| `ApplyToConsumed` | 4 |
| `RandomStatDown` | 4 |
| `SpecificInjury` | 4 |
| `TimeDelayStatusApplication` | 4 |
| `Charge` | 4 |
| `RemoveActPoints` | 4 |
| `TakeBonusTurnWithStatus` | 4 |
| `BurgleCoin` | 4 |
| `MagicMissleBlast` | 4 |
| `Default` | 4 |
| `Conditional_Familiar` | 4 |
| `SendRock` | 4 |
| `Reanimate` | 4 |
| `HealthGain` | 4 |
| `ExplosionIfHitSomething` | 4 |
| `EnableWeather` | 4 |
| `LateStatusApplication` | 4 |
| `SwitchMusic` | 4 |
| `Food` | 4 |
| `MoveQuivered` | 3 |
| `active` | 3 |
| `chapter_corpse_medium` | 3 |
| `PullSourceToTarget` | 3 |
| `TempSpeedUp` | 3 |
| `Explosion` | 3 |
| `DestroyWeaponThrow` | 3 |
| `Tumor` | 3 |
| `Doomed` | 3 |
| `ReviveNextRound` | 3 |
| `TempStrengthUp` | 3 |
| `NextAttackBonusRange` | 3 |
| `Reflect` | 3 |
| `PoisonLace` | 3 |
| `DoubleStatus` | 3 |
| `Conditional_LastHit` | 3 |
| `RepairOnKill` | 3 |
| `OverrideDamage` | 3 |
| `CurrentWeaponDamageUp` | 3 |
| `RepairAll` | 3 |
| `RefreshWeaponAbility` | 3 |
| `KineticSpikes` | 3 |
| `Conditional_AffectedByElement` | 3 |
| `SpawnNeutralWebTrapOnMiss` | 3 |
| `BrambleTile` | 3 |
| `CatPartsSizeScaleStatus` | 3 |
| `SpawnCustomTrap` | 3 |
| `CorpseVaporizer` | 3 |
| `ApplyMultipleTimes` | 3 |
| `SpellDamageUp` | 3 |
| `DestroyTrinket` | 3 |
| `VaporizeTarget` | 3 |
| `DeleteObject` | 3 |
| `InstantMaxHealthUp` | 3 |
| `Mage` | 3 |
| `DamageOrHealConditionally` | 3 |
| `PlayBackground` | 3 |
| `Conditional_FirstApplicationThisTurn` | 3 |
| `level` | 3 |
| `ExtraBasicAttacks_Status` | 3 |
| `ForceDisplace` | 3 |
| `CollideWithConsumed` | 3 |
| `ForceMoveTowardsEnemies` | 3 |
| `PermanentConstitution` | 3 |
| `CharmedTinySpider` | 3 |
| `DestroyWeapon` | 3 |
| `Tangled` | 3 |
| `SetCrazyEyeBackgroundWeights` | 3 |
| `DisplaceTowardsSource` | 3 |
| `DustOnHit` | 3 |
| `OilTile` | 2 |
| `TakeBonusTurnWithAIControl` | 2 |
| `TrailBlazer` | 2 |
| `RepairWeapon` | 2 |
| `StanceSwitchToMelee` | 2 |
| `CreepTile` | 2 |
| `Conditional_Shielded` | 2 |
| `Possessed` | 2 |
| `JohnnyCriesForWashers` | 2 |
| `Math` | 2 |
| `CharmedForceAttack` | 2 |
| `DamageTrinket` | 2 |
| `Explosive` | 2 |
| `AddSpiritBombCharges` | 2 |
| `MaxHPUp` | 2 |
| `Conditional_NotAlly` | 2 |
| `ChangeFaction` | 2 |
| `CopySpells` | 2 |
| `str` | 2 |
| `Trample` | 2 |
| `LeaveBehindRockOnKnockback` | 2 |
| `SpawnCoinAnywhere` | 2 |
| `HasDeadCat` | 2 |
| `SpeculativeMoveSelfCorpseOffMap` | 2 |
| `Conditional_IsSelf` | 2 |
| `TempDexterityUp` | 2 |
| `DieViaAbilityInternally` | 2 |
| `ScrambleEverything` | 2 |
| `ForceMoveNonAlliesInRangeTowardsTile` | 2 |
| `TempMovement` | 2 |
| `RandomDistanceDisplace` | 2 |
| `IgnoreDamage` | 2 |
| `Counterspell` | 2 |
| `sabertooths` | 2 |
| `SmallLavaRock` | 2 |
| `BodyGuard` | 2 |
| `ResetArmorShield` | 2 |
| `PartialCleanse` | 2 |
| `DestroyEquipmentAndAttachParasite` | 2 |
| `TempCritChanceUp` | 2 |
| `QuakeAreaChance` | 2 |
| `DelayedFury` | 2 |
| `SetShield` | 2 |
| `ShortCircuit` | 2 |
| `KnockOutCoin` | 2 |
| `Boris` | 2 |
| `OffMap` | 2 |
| `PullSourceToKnockbackImmuneTarget` | 2 |
| `Druid` | 2 |
| `Psychic` | 2 |
| `NextAttackSpecialCrit` | 2 |
| `passive` | 2 |
| `ImmediateUseAbility` | 2 |
| `Pulp2` | 2 |
| `SmartMetronome` | 2 |
| `FreeSpell` | 2 |
| `SignalFinalBossShieldBroke` | 2 |
| `TempSpellDamageUp` | 2 |
| `HornCharge` | 2 |
| `PermanentStrength` | 2 |
| `Monk` | 2 |
| `RebukeDamage` | 2 |
| `Bound` | 2 |
| `Tank` | 2 |
| `random` | 2 |
| `CollideWithThrowTarget` | 2 |
| `Shatter` | 2 |
| `Conditional_HealthThreshold` | 2 |
| `flip` | 2 |
| `Fighter` | 2 |
| `SelfStun` | 2 |
| `Conditional_BossOrBig` | 2 |
| `FireTile` | 2 |
| `ForceMoveTowardsTaggedObject` | 2 |
| `Ostracized` | 2 |
| `RangeUp` | 2 |
| `BonusKnockbackDamage` | 2 |
| `Conditional_DestructibleCorpse` | 2 |
| `ManaLeeches` | 2 |
| `OverHealToStatuses` | 2 |
| `Knockback` | 2 |
| `Tinkerer` | 2 |
| `PermanentUpgradeRandomActive` | 2 |
| `RandomKnockback` | 2 |
| `FlowersOnHit` | 2 |
| `TempInitiativeChange` | 2 |
| `TempTrampleUntilSettled` | 2 |
| `DirtTile` | 2 |
| `TradeLife` | 2 |
| `CritChanceUp` | 2 |
| `BloatEye` | 2 |
| `DoubleLoot` | 2 |
| `Conditional_NotShielded` | 2 |
| `Lifesteal` | 2 |
| `DisplaceToOriginalPosition` | 2 |
| `SpawnFlames` | 2 |
| `Conditional_BadRoll` | 2 |
| `DiminishingHealthRegen` | 2 |
| `Conditional_OncePerBattle` | 2 |
| `RepairWeaponCondition` | 2 |
| `ThrowPoop` | 2 |
| `mov` | 2 |
| `DamageDistanceAOEFalloff` | 2 |
| `BlankTile` | 2 |
| `RemoveMovePoints` | 2 |
| `BiggestFood` | 2 |
| `ImmediateUseDirectionalAbility` | 2 |
| `TriggerDOTStatuses` | 2 |
| `Conditional_Buddy` | 2 |
| `Pilfer` | 2 |
| `Hex` | 2 |
| `CancelPrimedAbilities` | 2 |
| `DamageBasedOnMissingHealth` | 2 |
| `RepairArmorCondition` | 2 |
| `SwallowSmallCharacter` | 2 |
| `Conditional_NotBossOrBig` | 2 |
| `Colorless` | 2 |
| `int` | 2 |
| `SizeScale` | 2 |
| `DoubleCastSpell` | 2 |
| `ChampionUpgradeNextMinion` | 1 |
| `TeleportBackAtTurnEnd` | 1 |
| `VaporizeDice` | 1 |
| `T3HitlerTriggerInitialSpawns` | 1 |
| `DrinkWater` | 1 |
| `DoubleCastSpellsEachTurn_Status` | 1 |
| `SquirrelForm` | 1 |
| `ManglerShuffle` | 1 |
| `AnimalEgg2` | 1 |
| `ShootHereReceiver` | 1 |
| `MimicMetronome` | 1 |
| `Possessing` | 1 |
| `BowlDash2` | 1 |
| `ExplodeCharacter_DeathBloom2` | 1 |
| `Tease2` | 1 |
| `Conditional_HasCleansableDebuffs` | 1 |
| `CharmedFacingForceAttack` | 1 |
| `HardenSkin2` | 1 |
| `false` | 1 |
| `SmellBlood` | 1 |
| `CloneWeaponTemp` | 1 |
| `SwapHighestAndLowestStat` | 1 |
| `BigMagicMissileBlast` | 1 |
| `Pulp4` | 1 |
| `Pounce2` | 1 |
| `HealRandomInjury` | 1 |
| `Taunting` | 1 |
| `DelayedWindCone` | 1 |
| `TowerDefenseStatus2` | 1 |
| `Conditional_RandomChance` | 1 |
| `DeathwormUnderground` | 1 |
| `Conditional_ActiveWeather_Any` | 1 |
| `VisualCountDownThenApplyStatus` | 1 |
| `EggSackTrap` | 1 |
| `PermanentDexterity` | 1 |
| `ChaosBossFormChange` | 1 |
| `ManglerThrowRemote` | 1 |
| `SpitConsumed` | 1 |
| `SourceSwapsBackEndOfTurn` | 1 |
| `MadnessChanceOnTurnBegin` | 1 |
| `UndoDamage` | 1 |
| `TriggerMotherConsume` | 1 |
| `TilesMovedToStrength` | 1 |
| `DeleteTraps` | 1 |
| `DinoLegAnimation` | 1 |
| `NextActionLuckUp` | 1 |
| `ExplodeCharacter_DeathBloom` | 1 |
| `NoStick` | 1 |
| `HealBig` | 1 |
| `SpawningPhase` | 1 |
| `ExistUntilIdleUpkeep` | 1 |
| `AlliesTakeExtraTurn` | 1 |
| `Amoeba` | 1 |
| `Dumb` | 1 |
| `ForceCollectsPickups` | 1 |
| `StackingSandstorm` | 1 |
| `Synthesize` | 1 |
| `TigerSwipes` | 1 |
| `FastKnockback` | 1 |
| `Meaty` | 1 |
| `Spider_GoInsane` | 1 |
| `Thief` | 1 |
| `Boulder` | 1 |
| `spd` | 1 |
| `CanceledQueuedInput` | 1 |
| `CharmedFlea_Champion` | 1 |
| `Conditional_Displaceable` | 1 |
| `GenericBuff` | 1 |
| `enter` | 1 |
| `Conditional_IsTrample` | 1 |
| `ThrowSpiritBomb` | 1 |
| `AntlerSwipe2` | 1 |
| `Scavenge2` | 1 |
| `TempBonusKnockbackDamage` | 1 |
| `PermanentLuck` | 1 |
| `Grown` | 1 |
| `TickDownStatus` | 1 |
| `SpecialBossMultipartInstakill` | 1 |
| `UseMoveAbilityWithAI` | 1 |
| `DualSword` | 1 |
| `BigFood` | 1 |
| `DelayCastAbility` | 1 |
| `Prance` | 1 |
| `SoundEventOnHit` | 1 |
| `ProbeCharmed` | 1 |
| `TransformEquipment` | 1 |
| `Scavenge` | 1 |
| `ConjureSingleUseBonusAbility` | 1 |
| `HardenSkin` | 1 |
| `TilesMovedToNeighborHeal` | 1 |
| `Disguised` | 1 |
| `TileDamageImmuneUntilSettled` | 1 |
| `ExtraBasicMoves_Status` | 1 |
| `BypassRockKnockback` | 1 |
| `WaterTile_Current` | 1 |
| `Conditional_AbilityTargetIsSelf` | 1 |
| `ThornsDamageImmuneUntilSettled` | 1 |
| `ManaStealToHealth` | 1 |
| `IceArmor` | 1 |
| `KaijuMeteornadoSolo` | 1 |
| `ShadowCrit` | 1 |
| `Conditional_LivingPlayerCat` | 1 |
| `HealTo` | 1 |
| `PermanentCharisma` | 1 |
| `Attraction` | 1 |
| `Class` | 1 |
| `GainCoinsRange` | 1 |
| `TriggerMotherGrow` | 1 |
| `NonStackingDivineShield` | 1 |
| `RefreshItemAbilities` | 1 |
| `ExplodeCharacter` | 1 |
| `AnimalEgg` | 1 |
| `TempBackstab` | 1 |
| `Chitter` | 1 |
| `LastThought` | 1 |
| `SwapWeapon` | 1 |
| `TallFlowerTile` | 1 |
| `Pulp7` | 1 |
| `PermanentSpeed` | 1 |
| `ShootHere` | 1 |
| `DrainAllyCatsForFleshGolem` | 1 |
| `FloatingGlassTile` | 1 |
| `moonboss` | 1 |
| `poop` | 1 |
| `TempBackstabPiercing` | 1 |
| `Batterup_Connect` | 1 |
| `QueueUseAbility` | 1 |
| `MegaGuppy` | 1 |
| `DecoySwapper` | 1 |
| `StatBounty` | 1 |
| `TigerSwipes2` | 1 |
| `TempBonusKnockback` | 1 |
| `HeadTumor` | 1 |
| `GirlDinoPoop` | 1 |
| `OverrideChainKnockbackDamage` | 1 |
| `IncreaseCumulativeBlastDamage` | 1 |
| `FlatAIBonus` | 1 |
| `Medic` | 1 |
| `Bloodzerked` | 1 |
| `TilesMovedToCritChance` | 1 |
| `T2CopyCatInternal` | 1 |
| `NextAbilityHeals` | 1 |
| `DontHealEnemies` | 1 |
| `TempPenetrate` | 1 |
| `Switcheroo` | 1 |
| `GroundedSpear` | 1 |
| `FireArmor` | 1 |
| `EmptyMind` | 1 |
| `ChaosBossFlipMidTeleport` | 1 |
| `Enlarge` | 1 |
| `RefreshOncePerFightAbilities` | 1 |
| `AlternateIdleAnimation` | 1 |
| `TempPreEmptiveCounterAttack` | 1 |
| `Lacerate` | 1 |
| `TempBackstabPoison` | 1 |
| `TilesMovedToMana` | 1 |
| `ShootHereCommand` | 1 |
| `SmallHitExplosion` | 1 |
| `Necromancer` | 1 |
| `BirthSquirrel2` | 1 |
| `insane` | 1 |
| `Conditional_NotBig` | 1 |
| `FinalBossQueueBeam` | 1 |
| `SkeletonCatFamiliar` | 1 |
| `BeefyCharmedLeech` | 1 |
| `BirthSquirrel` | 1 |
| `ObjectOnHitFullyEmpty` | 1 |
| `ApplyStatusesNextTurnBegin` | 1 |
| `CaptureFamiliar` | 1 |
| `Synthesize2` | 1 |
| `Conditional_SourceHasStatus` | 1 |
| `NextDamageReduceAndHealAllies` | 1 |
| `ForceUseAbility` | 1 |
| `ThiefSwapBack` | 1 |
| `Huddle_Impl` | 1 |
| `ApplyShieldToApplierBasedOnMaxHealth` | 1 |
| `MotherTumorDebugForcePass` | 1 |
| `Trapper_Status` | 1 |
| `DamageWeapon` | 1 |
| `ScatterRandomPickups` | 1 |
| `TagMetronome` | 1 |
| `Maggot` | 1 |
| `Carcus` | 1 |
| `ChangeTilesUnder` | 1 |
| `ForceTransferWeapon` | 1 |
| `TeamBonusAbility` | 1 |
| `Pulp5` | 1 |
| `StealDemonicGlyph` | 1 |
| `TeamFlex_Impl` | 1 |
| `Invulnerable` | 1 |
| `Conditional_CanBeHealed` | 1 |
| `TempBackstabBleed` | 1 |
| `TempLuckUp` | 1 |
| `DuplicateRandomEquippedItem` | 1 |
| `AIFavorLowHealth` | 1 |
| `CharmedFlea` | 1 |
| `ManglerAttack` | 1 |
| `DoubleCast` | 1 |
| `SpiritBomb2` | 1 |
| `TheDestroyer` | 1 |
| `ChargeFists` | 1 |
| `OverHealToShield` | 1 |
| `BasicDashAttackMove_NoKnockback` | 1 |
| `TempCounterAttack` | 1 |
| `CharmedLeech` | 1 |
| `Stop` | 1 |
| `GrassTile` | 1 |
| `KaijuMeteornado` | 1 |
| `HalfDead` | 1 |
| `ClearFinalBossBattlefield` | 1 |
| `MockSong2` | 1 |
| `TriggerGameEnding` | 1 |
| `RandomDifferentTile` | 1 |
| `BonusDamageBasedOnMana` | 1 |
| `Conditional_Backstab` | 1 |
| `CoinTossBounce` | 1 |
| `GlobalSpawnCharacter` | 1 |
| `StealthCritChance` | 1 |
| `SplashDamage` | 1 |
| `Hitler` | 1 |
| `Standing` | 1 |
| `FetusNoJar` | 1 |
| `RerollEnemy` | 1 |
| `IgnoreDebuffs` | 1 |
| `Pulp6` | 1 |
| `ApplyToOthersWithSharedTagAndFaction` | 1 |
| `TurnControlDelay` | 1 |
| `SetDefaultFace` | 1 |
| `Prance2` | 1 |
| `Infested` | 1 |
| `DybbukPossessed` | 1 |
| `KaijuFirestorm` | 1 |
| `TurnAround` | 1 |
| `HeavyHits` | 1 |
| `Lacerate2` | 1 |
| `BombRatTurtle` | 1 |
| `HealPercentMaxHP` | 1 |
| `SleepParalysis` | 1 |
| `Timber` | 1 |
| `Reposition2` | 1 |
| `RefreshNonManaItemAbilities` | 1 |
| `Dip` | 1 |
| `LavaBoulder` | 1 |
| `RemoveStatusStacks` | 1 |
| `TakeExtraTurnEndOfRound` | 1 |
| `RandomPermanentStat` | 1 |
| `Sprout` | 1 |
| `FlashBack` | 1 |
| `TinySpider` | 1 |
| `StealTurn` | 1 |
| `TowerDefenseStatus` | 1 |
| `DumbMove_Impl` | 1 |
| `DeathWormEat` | 1 |
| `Regurge` | 1 |
| `FactionDisguiseSource` | 1 |
| `IncAuxCounterCycle` | 1 |
| `FireBlastSmall` | 1 |
| `NextBasicAttackCritsThisTurn` | 1 |
| `TurnRight` | 1 |
| `BerserkDash` | 1 |
| `ReduceManaCost` | 1 |
| `StatusGroup` | 1 |
| `IncreaseItemAuxOnKill` | 1 |
| `NextTurnDoubleRangedDamage` | 1 |
| `TempBasicAttackBonusAOE` | 1 |
| `ApplyToRandomClosestAlly` | 1 |
| `ReturnDinoLegs` | 1 |
| `TargetedMetronome` | 1 |
| `Reposition` | 1 |
| `Jester` | 1 |
| `TeamFlex_Impl2` | 1 |
| `Conditional_DebuffRoll` | 1 |
| `Off` | 1 |
| `cm_Lard_Impl` | 1 |
| `RepairAllCondition` | 1 |
| `RandomKnockbackDirection` | 1 |
| `GiveBoundItemToTarget` | 1 |
| `SpiritBomb` | 1 |
| `CharmTrap` | 1 |
| `PermanentImmobile` | 1 |
| `SpikeTrap` | 1 |
| `Pulp3` | 1 |
| `DieViolently` | 1 |
| `RNGCannonRandomDamage` | 1 |
| `AntlerSwipe` | 1 |
| `EliteUpgradeNextMinion` | 1 |
| `Conditional_SourceAbilityHasTag` | 1 |
| `JesterMinusColorless` | 1 |
| `Tormentor` | 1 |
| `TransformNow` | 1 |
| `sytheCut` | 1 |
| `HitlerCloneTransform` | 1 |
| `LastThought2` | 1 |
| `Butcher` | 1 |
| `FireArmor2` | 1 |
| `BowlDash` | 1 |
| `Holyatk` | 1 |
| `CurrentWeaponAddElectricElement` | 1 |
| `RandomArmorPickup` | 1 |
| `MassAttackThis` | 1 |
| `any` | 1 |
| `PoolMetronome` | 1 |
| `TransformBasicMove` | 1 |
| `DissolveRandomArmorPiece` | 1 |
| `ThrowSpiritBomb2` | 1 |
| `Hunter` | 1 |
| `StealEquipment` | 1 |
| `DestroyNeckArmor` | 1 |
| `Spin` | 1 |
| `MakeWeaponUnbreakable` | 1 |
| `CreateGlobalModifiers` | 1 |
| `WaggleClone` | 1 |
| `VaporizeCorpseFlipAdvantage` | 1 |
| `FactionConversion` | 1 |
| `MonkeyThrow` | 1 |
| `TempManaCostReduction` | 1 |
| `StemCat_HalfHealth` | 1 |
| `Pounce` | 1 |
| `EnterMount` | 1 |
| `PermanentIntelligence` | 1 |
| `InterchangeMoveActPoints` | 1 |
| `ReformMoonHead` | 1 |
| `MotherTumorGrow` | 1 |
| `ScrambleLastUsedSpell` | 1 |
| `IceTile` | 1 |
| `SpellShield` | 1 |
| `musical` | 1 |
| `MonkeyThrow2` | 1 |
| `Bomb` | 1 |
| `Obey` | 1 |
| `MockSong` | 1 |
| `rotate_right` | 1 |
| `MD_PoopChain` | 1 |
| `Open` | 1 |
| `IceShardsSmall` | 1 |
| `ForceMoveAndAttack` | 1 |
| `PermanentUpgradeRandomActiveOrPassive` | 1 |
| `berserkIdle` | 1 |
| `MoveOne` | 1 |
| `NextBattleStatusStacks` | 1 |
| `SpawnWebTrap` | 1 |
| `Tease` | 1 |
| `Muted` | 1 |
| `TempInjuryImmunity` | 1 |
| `ExplodeCharacter_NoDie` | 1 |
| `BerserkDash2` | 1 |
| `NoDeathrattle` | 1 |
| `ReduceManaCostExcludeBrainstorm` | 1 |

#### `boss_elite_buffs.gon` — no truly exclusive properties

#### `characters` (1 truly exclusive)

| :--- | :---: |
| Property | Count |
| `BlackHoleSuck` | 1 |

#### `elite_buffs.gon` — no truly exclusive properties

#### `item_setbonuses.gon` — no truly exclusive properties

#### `items` (1 truly exclusive)

| :--- | :---: |
| Property | Count |
| `RandomPickup` | 3 |

#### `mutations` — no truly exclusive properties

#### `passives` (1 truly exclusive)

| :--- | :---: |
| Property | Count |
| `IcePoof` | 4 |

#### `weather.gon` (42 truly exclusive)

| :--- | :---: |
| Property | Count |
| `SpawnExtraThingsOnBattleStart` | 28 |
| `Windy` | 4 |
| `LowerAmbientLight` | 4 |
| `Rain` | 4 |
| `FactionUprising` | 4 |
| `SpawnVolcanoOnBattleStart` | 3 |
| `StatusCharactersOnRoundEnd` | 3 |
| `Meteornado` | 3 |
| `CharacterTypeGainsStatusAtBattleStart` | 2 |
| `StatusCharactersOnRoundStart` | 2 |
| `Snow` | 2 |
| `FireStorm` | 2 |
| `GlobalSpawnOnRoundEnd` | 2 |
| `RandomLightning` | 2 |
| `StatusAllCharactersOnSpawn` | 2 |
| `SpecialGodRays` | 2 |
| `PersistentElement` | 1 |
| `Sandstorm` | 1 |
| `Fog` | 1 |
| `FindExtraItemFromPoolOnBattleEnd` | 1 |
| `AcidRain` | 1 |
| `JudgementDay` | 1 |
| `MeteorShower` | 1 |
| `ghost` | 1 |
| `LowGravityKnockbackBoost` | 1 |
| `RandomWeatherEachFight` | 1 |
| `LowGravityRangeBoost` | 1 |
| `ClearDefaultDebris` | 1 |
| `AddPostProcessEffect` | 1 |
| `SolarFlare` | 1 |
| `robot` | 1 |
| `AddTilesetObjects` | 1 |
| `pills` | 1 |
| `CockroachSwarm` | 1 |
| `GlobalHealthRegenAura` | 1 |
| `FireflySwarm` | 1 |
| `FlySwarm` | 1 |
| `DeleteInanimateObjectsChance` | 1 |
| `HeatWave` | 1 |
| `ButterflySwarm` | 1 |
| `SpawnTilePuddleOnBattleStart` | 1 |
| `alien` | 1 |

