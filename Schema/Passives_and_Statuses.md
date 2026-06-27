# Mewgenics Mod Developer Documentation: Master Schema Dictionary
> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

This document is an exhaustive, auto-generated dictionary of every `.gon` property found across all 8 major engine systems. Due to the sheer volume of properties, you will need to infer their exact engine functionality through testing or context clues.

## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 885

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 3307 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2985 | `passives`<br>`class`<br>`tag` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 2423 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1910 | `{ . . . }` |
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 600 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 461 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 241 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`shield`](./Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 191 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 89 | `+1`<br>`-1`<br>`-2` |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 79 | `-1`<br>`-2`<br>`-3` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 78 | `-1`<br>`-10`<br>`-2` |
| [`int`](./Enums.md#enum-int) | Enum / Integer  || 66 | `-1`<br>`-10`<br>`-2` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer  || 53 | `-1`<br>`-2`<br>`-3` |
| [`str`](./Enums.md#enum-str) | Enum / Integer  || 45 | `-1`<br>`-2`<br>`-3` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer  || 30 | `-1`<br>`-2`<br>`-3` |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 28 | `{ . . . }` |
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 20 | `0`<br>`1`<br>`2` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 18 | `1`<br>`10`<br>`100` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 18 | `1`<br>`2`<br>`3` |
| [`lock_item_slot`](./Passives_and_Statuses.md#object-lock_item_slot) | Object  || 16 | `{ . . . }` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 12 | `10`<br>`15`<br>`20` |
| [`name_mod`](./Strings.md#string-name_mod) | String || 11 | `"CAT_NAME_MOD_AMOEBA"`<br>`"CAT_NAME_MOD_COOL"`<br>`"CAT_NAME_MOD_DWARF"` |
| [`SpawnOnBattleStart`](./Passives_and_Statuses.md#object-spawnonbattlestart) | Enum / Object  | Specifies the object that spawns adjacent to the unit at the start of battle. | 9 | `{ . . . }`<br>`BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 7 | `1`<br>`3`<br>`4` |
| [`override_basic_attack`](./Enums.md#enum-override_basic_attack) | Enum || 6 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`BoostWeaponDamage`](./Passives_and_Statuses.md#object-boostweapondamage) | Object  | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 5 | `{ . . . }` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | `1`<br>`2`<br>`5` |
| [`desc_multiclass`](./Strings.md#string-desc_multiclass) | String || 5 | `"PASSIVE_BARBED2_MULTICLASS_DESC"`<br>`"PASSIVE_BARBED_MULTICLASS_DESC"`<br>`"PASSIVE_GRAPPLINGHOOK2_MULTICLASS_DESC"` |
| [`bonus_items`](./Arrays.md#array-bonus_items) | Array | An array of item names granted as bonus rewards. | 5 | `[Eyeball]`<br>`[FoodBig FoodBig FoodBig FoodBig]`<br>`[Pipe]` |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum  || 4 | `Bleed`<br>`Burn`<br>`Poison` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 4 | `1`<br>`2`<br>`3` |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 4 | `Burn`<br>`Poison`<br>`Tarred` |
| `auto_plus_signs_on_name` | Boolean || 4 | `false` |
| [`BlastResistance`](./Passives_and_Statuses.md#object-blastresistance) | Array / Float / Object  || 3 | `{ . . . }`<br>`2`<br>`3`<br>`4` |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 3 | `-1`<br>`1`<br>`2` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 3 | `1`<br>`2`<br>`3` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 3 | `1`<br>`2`<br>`[1, 0.1]` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 3 | `1`<br>`2`<br>`3` |
| `YOffset` | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 3 | `-.18`<br>`.25`<br>`.35` |
| [`AbilityReaction`](./Passives_and_Statuses.md#object-abilityreaction) | Enum / Object  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 2 | `{ . . . }`<br>`AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| [`CounterAttack`](./Passives_and_Statuses.md#object-counterattack) | Array / Enum / Object  | Specifies the ability used when the unit counterattacks after being hit. | 2 | `{ . . . }`<br>`BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 2 | `0`<br>`1`<br>`10%` |
| [`PoopWhenHit`](./Passives_and_Statuses.md#object-poopwhenhit) | Object  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 2 | `{ . . . }` |
| [`ReflectProjectiles`](./Passives_and_Statuses.md#object-reflectprojectiles) | Integer / Object  | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 2 | `{ . . . }`<br>`1`<br>`10%`<br>`100%` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 2 | `.4`<br>`.6`<br>`.7` |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#object-empty_armor_scaled_stats) | Object  | Defines the stat bonuses applied when no armor is equipped in a slot. | 2 | `{ . . . }` |
| [`Vegan`](./Passives_and_Statuses.md#object-vegan) | Float / Object  | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 2 | `{ . . . }`<br>`1` |
| [`AfterImage`](./Passives_and_Statuses.md#object-afterimage) | Object  | Specifies the object or skill used to create an afterimage of the unit. | 1 | `{ . . . }` |
| [`AllyBonusAbilityAura`](./Passives_and_Statuses.md#object-allybonusabilityaura) | Enum / Object  || 1 | `{ . . . }`<br>`NubbyToss` |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 1 | `1` |
| [`AutocastEachTurnBegin`](./Passives_and_Statuses.md#object-autocasteachturnbegin) | Enum / Object  || 1 | `{ . . . }`<br>`MindCrack_EldritchVisage`<br>`MindCrack_EldritchVisage2` |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Integer / Object  | The number of backflip charges, or an object defining its ability. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| `BackstabCritChance` | Float || 1 | `.25`<br>`1` |
| [`BoostDamageGlobalAura`](./Passives_and_Statuses.md#object-boostdamageglobalaura) | Array / Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`BraceForEachNeighboringEnemy`](./Passives_and_Statuses.md#object-braceforeachneighboringenemy) | Array / Float / Object  || 1 | `{ . . . }`<br>`1`<br>`2` |
| [`ChainKnockback`](./Passives_and_Statuses.md#object-chainknockback) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`ChanceToBlockAndCounter`](./Passives_and_Statuses.md#object-chancetoblockandcounter) | Integer / Object  || 1 | `{ . . . }`<br>`15%`<br>`25%`<br>`33%` |
| [`ChanceToRevive`](./Passives_and_Statuses.md#object-chancetorevive) | Integer / Object  || 1 | `{ . . . }`<br>`100`<br>`25` |
| [`CharmAllFlies`](./Passives_and_Statuses.md#object-charmallflies) | Array / Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`CollectPickupsOnBattleEnd`](./Passives_and_Statuses.md#object-collectpickupsonbattleend) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`Conductor`](./Passives_and_Statuses.md#object-conductor) | Boolean (Flag) / Float / Object  || 1 | `{ . . . }`<br>`2` |
| [`ConjureBonusAbility`](./Passives_and_Statuses.md#object-conjurebonusability) | Enum / Object  | Specifies the name of the bonus ability to conjure. | 1 | `{ . . . }`<br>`Class`<br>`Colorless`<br>`Mage` |
| [`DamageReductionAura`](./Passives_and_Statuses.md#object-damagereductionaura) | Array / Float / Object  || 1 | `{ . . . }` |
| [`DeathChill`](./Passives_and_Statuses.md#object-deathchill) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`DeathRattle`](./Passives_and_Statuses.md#object-deathrattle) | Enum / Object  | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 1 | `{ . . . }`<br>`BBExplode`<br>`BloatyExplodey`<br>`BombFlyExplode` |
| [`DejaVu`](./Passives_and_Statuses.md#object-dejavu) | Float / Object  || 1 | `{ . . . }`<br>`10%` |
| `DepressionAura` | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 1 | `1`<br>`2` |
| [`DirtyClaws`](./Passives_and_Statuses.md#object-dirtyclaws) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`DukeOfFlies`](./Passives_and_Statuses.md#object-dukeofflies) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`Empath`](./Passives_and_Statuses.md#object-empath) | Float / Object  || 1 | `{ . . . }`<br>`100%`<br>`50%` |
| [`EnergyStorm`](./Passives_and_Statuses.md#object-energystorm) | Float / Object  || 1 | `{ . . . }`<br>`3` |
| [`FlyDamageIncrease`](./Passives_and_Statuses.md#object-flydamageincrease) | Object  || 1 | `{ . . . }` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 1 | `1` |
| [`FollowUp`](./Passives_and_Statuses.md#object-followup) | Enum / Object  || 1 | `{ . . . }`<br>`FollowUpDash`<br>`FollowUpDash2` |
| [`FullPower`](./Passives_and_Statuses.md#object-fullpower) | Float / Object  || 1 | `{ . . . }`<br>`3` |
| [`HealingAura`](./Passives_and_Statuses.md#object-healingaura) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`ImmortalLeeches`](./Passives_and_Statuses.md#object-immortalleeches) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`KillsHeal`](./Passives_and_Statuses.md#object-killsheal) | Float / Object  || 1 | `{ . . . }`<br>`5`<br>`50%` |
| [`LateBloomer`](./Passives_and_Statuses.md#object-latebloomer) | Array / Float / Object  || 1 | `{ . . . }` |
| `LineOfSightTrueSightAura` | Float || 1 | `.5`<br>`0` |
| [`LowHealthAllyDodgeChanceAura`](./Passives_and_Statuses.md#object-lowhealthallydodgechanceaura) | Array / Float / Object  || 1 | `{ . . . }` |
| [`MegaMinions`](./Passives_and_Statuses.md#object-megaminions) | Float / Object  || 1 | `{ . . . }`<br>`3` |
| `Metal` | Integer || 1 | `1` |
| [`MetalDetector`](./Passives_and_Statuses.md#object-metaldetector) | Float / Object  || 1 | `{ . . . }`<br>`10`<br>`5` |
| [`MoveAwayFromDamageSource`](./Passives_and_Statuses.md#object-moveawayfromdamagesource) | Object  | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 1 | `{ . . . }` |
| [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#object-movetowardsdamagesource) | Enum / Object  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 1 | `{ . . . }`<br>`MoveOne` |
| [`MoveWhenDamaged`](./Passives_and_Statuses.md#object-movewhendamaged) | Enum / Object  | Defines movement behavior when the unit takes damage, such as weights and move ability. | 1 | `{ . . . }`<br>`TKNG_Hop`<br>`move` |
| [`NumbingLeeches`](./Passives_and_Statuses.md#object-numbingleeches) | Float / Object  || 1 | `{ . . . }`<br>`3` |
| [`ProtectTargetedAllies`](./Passives_and_Statuses.md#object-protecttargetedallies) | Object  | Specifies the ability used to protect targeted allies, including an optional target filter. | 1 | `{ . . . }` |
| [`Quiver`](./Passives_and_Statuses.md#object-quiver) | Float / Object  || 1 | `{ . . . }`<br>`1`<br>`2` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Robot`](./Passives_and_Statuses.md#object-robot) | Integer / Object  | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 1 | `{ . . . }`<br>`1` |
| [`SharePickups`](./Passives_and_Statuses.md#object-sharepickups) | Object  | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 1 | `{ . . . }` |
| [`ShoulderCheck`](./Passives_and_Statuses.md#object-shouldercheck) | Float / Object  || 1 | `{ . . . }`<br>`100%`<br>`33%` |
| [`ShovingMatch`](./Passives_and_Statuses.md#object-shovingmatch) | Enum / Object  || 1 | `{ . . . }`<br>`attack` |
| [`SpawnExtraThingsOnBattleStart`](./Passives_and_Statuses.md#object-spawnextrathingsonbattlestart) | Object  | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 1 | `{ . . . }` |
| [`SpawnObjectOnPopCorpse`](./Passives_and_Statuses.md#object-spawnobjectonpopcorpse) | Enum / Object  || 1 | `{ . . . }`<br>`Catnip`<br>`Coin`<br>`Food` |
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer  | The number of stealth stacks applied. | 1 | `1`<br>`2`<br>`[1 .1]` |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#object-schadenfreude_scaled_stats) | Object  | Defines the stat bonuses (str, dex, con, int, cha) applied by the Schadenfreude trait at a given level. | 1 | `{ . . . }` |
| [`grant_ability`](./Enums.md#enum-grant_ability) | Enum || 1 | `Rest` |
| [`StrengthForEachNeighboringEnemy`](./Passives_and_Statuses.md#object-strengthforeachneighboringenemy) | Array / Float / Object  || 1 | `{ . . . }`<br>`2`<br>`3` |
| [`StrengthInNumbersAura`](./Passives_and_Statuses.md#object-strengthinnumbersaura) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`Study`](./Passives_and_Statuses.md#object-study) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| `SwapHighestAndLowestStat` | Integer || 1 | `1` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 1 | `1`<br>`3` |
| [`TileDamageMultiplier`](./Passives_and_Statuses.md#object-tiledamagemultiplier) | Float / Object  || 1 | `{ . . . }`<br>`2` |
| [`Vengeful`](./Passives_and_Statuses.md#object-vengeful) | Float / Object  || 1 | `{ . . . }`<br>`1` |
| [`Weakness`](./Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |

</details>


---


### Object: `passives`


**Definition:** Object listing intrinsic passive modifiers.  
**Total Count:** 884

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Passives_and_Statuses.md#context-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#context-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#context-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#context-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2039 | `passives`<br>`class`<br>`tag` |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 133 | `{ . . . }` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 94 | `1`<br>`10`<br>`2` |
| [`Metal`](./Enums.md) | Integer || 90 | `1` |
| [`Trample`](./Arrays.md#array-trample) | Array / Integer  | The amount of bonus damage dealt when moving through an enemy. | 88 | `1`<br>`3`<br>`4` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 65 | `1`<br>`2`<br>`3` |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 59 | `{ . . . }` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 52 | `1`<br>`2`<br>`3` |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#object-statuseachturnend) | Object  | Specifies status effects applied to the unit at the end of each of its turns. | 49 | `{ . . . }` |
| [`Robot`](./Passives_and_Statuses.md#object-robot) | Object  | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 47 | `{ . . . }` |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 45 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 39 | `Creep`<br>`Electric`<br>`Fire` |
| [`SpawnOnBattleStart`](./Passives_and_Statuses.md#object-spawnonbattlestart) | Enum / Object  | Specifies the object that spawns adjacent to the unit at the start of battle. | 36 | `{ . . . }`<br>`BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| [`DeathRattle`](./Passives_and_Statuses.md#object-deathrattle) | Enum / Object  | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 35 | `{ . . . }`<br>`BBExplode`<br>`BloatyExplodey`<br>`BombFlyExplode` |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum  | Specifies the ability used when the unit counterattacks after being hit. | 34 | `BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 34 | `Burn`<br>`Poison`<br>`Tarred` |
| [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 29 | `{ . . . }` |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage) | Object  | Specifies status effects or actions triggered when the unit takes damage. | 29 | `{ . . . }` |
| [`SpawnThingOnDamage`](./Passives_and_Statuses.md#object-spawnthingondamage) | Object  | Specifies an object that spawns on the tile when the unit takes damage. | 28 | `{ . . . }` |
| [`AbilityReaction`](./Passives_and_Statuses.md#object-abilityreaction) | Enum / Object  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 23 | `{ . . . }`<br>`AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions) | Object  || 21 | `{ . . . }` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 21 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`AddMovement`](./Enums.md) | Integer | The amount of bonus movement points added to the unit's base movement. | 20 | `-1`<br>`-2`<br>`1` |
| [`ArmorDodgeChance`](./Enums.md) | Integer || 19 | `10%`<br>`15%`<br>`20%` |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 18 | `{ . . . }` |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 16 | `1`<br>`10`<br>`100` |
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 15 | `1`<br>`10`<br>`2` |
| [`RevengeDamage`](./Passives_and_Statuses.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 15 | `{ . . . }` |
| [`SpawnEachTurn`](./Passives_and_Statuses.md#object-spawneachturn) | Object  | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 15 | `{ . . . }` |
| [`StatusOnBattleStart`](./Passives_and_Statuses.md#object-statusonbattlestart) | Object  || 15 | `{ . . . }` |
| [`AddCorpseHealth`](./Enums.md) | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 14 | `-999`<br>`-999999`<br>`100` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | `-1`<br>`-2`<br>`1` |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 14 | `10%`<br>`15%`<br>`2%` |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum  | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 14 | `Earth`<br>`Electric`<br>`Fire` |
| [`SizeScale`](./Enums.md) | Float | The multiplier applied to the unit's visual and hitbox size. | 14 | `.4`<br>`.6`<br>`.7` |
| [`WaterWalk`](./Enums.md) | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 14 | `1` |
| [`AddManaRegen`](./Enums.md) | Integer | The flat amount of mana regenerated per turn. | 13 | `1`<br>`2`<br>`3` |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum  | Specifies the class that this unit gains a level in when multiclassing. | 12 | `Butcher`<br>`Druid`<br>`Fighter` |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum  | Specifies the name of an object to spawn upon death. | 12 | `Boulder`<br>`CharmedDemonKitten`<br>`CharmedFlySwarm` |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum  || 11 | `Flush`<br>`Heathens`<br>`Heathens2` |
| [`AddStatusToAllDamage`](./Passives_and_Statuses.md#object-addstatustoalldamage) | Object  || 11 | `{ . . . }` |
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 11 | `1`<br>`2`<br>`3` |
| [`ExtraBasicAttacks`](./Enums.md) | Integer | The number of additional basic attacks the unit can perform per turn. | 11 | `1`<br>`2` |
| [`MoveWhenDamaged`](./Passives_and_Statuses.md#object-movewhendamaged) | Object  | Defines movement behavior when the unit takes damage, such as weights and move ability. | 11 | `{ . . . }` |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum  | Specifies an alternative movement ability that replaces the unit's default move. | 11 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |
| [`AddLevelUpRerolls`](./Enums.md) | Integer | The number of additional rerolls the unit gets when leveling up. | 10 | `1`<br>`2`<br>`3` |
| [`LimitDamage`](./Enums.md) | Integer | The maximum amount of damage the unit can take from a single hit. | 10 | `1` |
| [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#object-movetowardsdamagesource) | Object  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 10 | `{ . . . }` |
| [`StatusOnKillEnemy`](./Passives_and_Statuses.md#object-statusonkillenemy) | Object  || 10 | `{ . . . }` |
| [`AddSelfStatusToBasicAttack`](./Passives_and_Statuses.md#object-addselfstatustobasicattack) | Object  || 9 | `{ . . . }` |
| [`AddTag`](./Enums.md#enum-addtag) | Enum  | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 9 | `bug`<br>`cat`<br>`fetus` |
| [`BackstabImmunity`](./Enums.md) | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 9 | `1` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 9 | `1`<br>`2`<br>`3` |
| [`DepressionAura`](./Enums.md) | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 9 | `1`<br>`2` |
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 9 | `1` |
| [`LimitHeal`](./Enums.md) | Integer | If 1, prevents the unit from being healed. | 9 | `0`<br>`1` |
| [`MissChance`](./Enums.md) | Integer | The flat percentage chance that the unit's attacks will miss. | 9 | `10`<br>`15`<br>`20` |
| [`MovementReaction`](./Passives_and_Statuses.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 9 | `{ . . . }` |
| [`PoisonThorns`](./Enums.md) | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 9 | `1`<br>`2`<br>`3` |
| [`SmallRockBehavior`](./Enums.md) | Integer | Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed. | 9 | `0`<br>`5` |
| [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#object-statusalliesonbattlestart) | Object  || 9 | `{ . . . }` |
| [`TrinketPassiveMultiplierBonus`](./Enums.md) | Integer || 9 | `1`<br>`2` |
| [`BoostHeals`](./Enums.md) | Integer || 8 | `-2`<br>`1`<br>`2` |
| [`ChanceToRevive`](./Passives_and_Statuses.md#object-chancetorevive) | Integer / Object  || 8 | `{ . . . }`<br>`100`<br>`25` |
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 8 | `1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`AddElementsToBasicAttack`](./Enums.md) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 7 | `Electric`<br>`Fire`<br>`Gravity` |
| [`AddInitiative`](./Enums.md) | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 7 | `-10`<br>`-100`<br>`-20` |
| [`AlphaTurns`](./Enums.md) | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 7 | `-1`<br>`1` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 7 | `1`<br>`10`<br>`2` |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum  | Specifies the name of a bonus ability granted. | 7 | `Bloodzerk`<br>`BonusToss`<br>`BonusToss2` |
| [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#object-damageneighborsonendmove) | Object  || 7 | `{ . . . }` |
| [`DebuffImmunity`](./Enums.md) | Integer | If 1, the unit is immune to debuffs. | 7 | `1` |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 7 | `-2`<br>`1`<br>`2` |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum  || 7 | `BasicExplosiveShot`<br>`BasicMelee`<br>`BasicMetronome` |
| [`OverrideMaxHealth`](./Enums.md) | Integer | Replaces the unit's maximum health with this value. | 7 | `1`<br>`25` |
| [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#object-passiveathealththreshold) | Object  || 7 | `{ . . . }` |
| [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#object-passiveatstatthreshold) | Object  || 7 | `{ . . . }` |
| [`SecurityBotProtect`](./Passives_and_Statuses.md#object-securitybotprotect) | Object  | Specifies the ability and movement used by a security bot to protect allies. | 7 | `{ . . . }` |
| [`SetSpellCosts`](./Enums.md) | Integer | Overrides the cost of all spells to this value. | 7 | `0`<br>`1`<br>`3` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 7 | `-1`<br>`-2`<br>`-4` |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 7 | `{ . . . }` |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 6 | `{ . . . }` |
| [`AmplifyStatus`](./Passives_and_Statuses.md#object-amplifystatus) | Enum / Object  || 6 | `{ . . . }`<br>`Bleed`<br>`Burn`<br>`Poison` |
| [`ExtraWeaponAttacks`](./Enums.md) | Integer || 6 | `1`<br>`2` |
| [`IgnoreTiles`](./Enums.md) | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 6 | `1` |
| [`Poison`](./Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 6 | `1`<br>`10`<br>`2` |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 6 | `1`<br>`2`<br>`5` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 6 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile) | Object  | Specifies an object that spawns on a random empty tile at the start of battle. | 6 | `{ . . . }` |
| [`StatusOnTookDamageFromAbility`](./Passives_and_Statuses.md#object-statusontookdamagefromability) | Object  | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 6 | `{ . . . }` |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum  | Specifies the type of tile left behind as the unit moves. | 6 | `BrambleTile`<br>`CreepTile`<br>`FireTile` |
| [`AddBonusMeleeRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's melee attacks. | 5 | `1`<br>`10`<br>`2` |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum  | A hidden tag applied to the unit for internal logic and triggers. | 5 | `bowling_ball`<br>`grown_hitler_clone`<br>`hitler_clone_fetus` |
| [`AutocastEachRound`](./Passives_and_Statuses.md#object-autocasteachround) | Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 5 | `{ . . . }` |
| [`BackstabCritChance`](./Enums.md) | Integer || 5 | `.25`<br>`1` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 5 | `1`<br>`10`<br>`2` |
| [`ClassManaCostReduction`](./Passives_and_Statuses.md#object-classmanacostreduction) | Object  | Defines a reduction in mana cost for abilities of a specific class. | 5 | `{ . . . }` |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#object-critsapplystatus) | Object  || 5 | `{ . . . }` |
| [`FaceShield`](./Enums.md) | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 5 | `0`<br>`1` |
| [`HeadArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 5 | `1`<br>`2` |
| [`InjuryImmunity`](./Enums.md) | Integer | The number of turns the unit is immune to injuries. | 5 | `1` |
| [`KnockbackImmunity`](./Enums.md) | Integer | If set to 1, the unit cannot be knocked back. | 5 | `1` |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#object-statusifunusedmovepoints) | Object  | Specifies status effects applied if the unit ends its turn with unused movement points. | 5 | `{ . . . }` |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Passives_and_Statuses.md#object-statusonturnendifdidntcastabilitytypes) | Object  || 5 | `{ . . . }` |
| [`TrinketActiveEffectsMultiplierBonus`](./Enums.md) | Integer || 5 | `1`<br>`2` |
| [`AddCritMultiplier`](./Enums.md) | Integer || 4 | `100%`<br>`125%`<br>`150%` |
| [`AddKnockbackDamage`](./Enums.md) | Integer | The amount of additional knockback damage applied. | 4 | `1`<br>`2`<br>`3` |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#object-addstatustoelementdamage) | Object  || 4 | `{ . . . }` |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#object-addstatustoweapons) | Object  | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 4 | `{ . . . }` |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 4 | `{ . . . }` |
| [`BlastResistance`](./Enums.md) | Integer || 4 | `2`<br>`3`<br>`4` |
| [`BoostWeaponDamage`](./Passives_and_Statuses.md#object-boostweapondamage) | Integer / Object  | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`5` |
| [`BuffImmunity`](./Enums.md) | Integer | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 4 | `1` |
| [`CatchProjectiles`](./Passives_and_Statuses.md#object-catchprojectiles) | Object  || 4 | `{ . . . }` |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 | `{ . . . }` |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum  | Specifies which temporary item is equipped. | 4 | `Bottles`<br>`ButcherHook_Temporary`<br>`FoodBig` |
| [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#object-extrastatuswhendealingdamage) | Object  || 4 | `{ . . . }` |
| [`FaceArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 4 | `1`<br>`2` |
| [`ForceSpecificInjury`](./Enums.md) | Enum || 4 | `cha`<br>`int`<br>`lck` |
| [`FreezePiercing`](./Enums.md) | Integer || 4 | `1` |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | `1`<br>`2`<br>`3` |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 4 | `1`<br>`2`<br>`7` |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum  || 4 | `Colorless`<br>`Jester` |
| [`MakeSpellsRequireCharge`](./Enums.md) | Integer || 4 | `1` |
| [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#object-passiveifallarmorempty) | Object  || 4 | `{ . . . }` |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 4 | `{ . . . }` |
| [`StatusAlliesOnDeath`](./Passives_and_Statuses.md#object-statusalliesondeath) | Object  || 4 | `{ . . . }` |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#object-statuseveryxspellcasts) | Object  | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 4 | `{ . . . }` |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#object-statusonallycatdeath) | Object  | An object listing status effects applied to the unit when an allied cat dies. | 4 | `{ . . . }` |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#object-statusoncastspell) | Object  | An object listing status effects applied to the unit whenever it casts a spell. | 4 | `{ . . . }` |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#object-statusongaincoins) | Object  | Specifies status effects applied when this unit gains coins. | 4 | `{ . . . }` |
| [`StatusOnPopCorpse`](./Passives_and_Statuses.md#object-statusonpopcorpse) | Object  || 4 | `{ . . . }` |
| [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear) | Object  | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 3 | `{ . . . }` |
| [`AddPassivesToCharmed`](./Passives_and_Statuses.md#object-addpassivestocharmed) | Object  || 3 | `{ . . . }` |
| [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#object-addstatustobasicmeleeattack) | Object  | An object listing status effects applied by the unit's basic melee attack. | 3 | `{ . . . }` |
| [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#object-addstatustoelementabilities) | Object  || 3 | `{ . . . }` |
| [`AddStatusToSpells`](./Passives_and_Statuses.md#object-addstatustospells) | Object  | Specifies status effects added to all spell attacks used by this unit. | 3 | `{ . . . }` |
| [`AllyBonusAbilityAura`](./Passives_and_Statuses.md#object-allybonusabilityaura) | Enum / Object  || 3 | `{ . . . }`<br>`NubbyToss` |
| [`AmplifyKnockback`](./Enums.md) | Integer || 3 | `10`<br>`2` |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Passives_and_Statuses.md#object-applystatusestorandomenemieseachturn) | Object  || 3 | `{ . . . }` |
| [`AutoEquipConsumables`](./Enums.md) | Integer || 3 | `1` |
| [`BasicAttackCritChance`](./Enums.md) | Integer || 3 | `.1`<br>`100%` |
| [`BasicAttackDamageMultiplier`](./Enums.md) | Float || 3 | `0`<br>`33.333334%`<br>`50%` |
| [`ChanceToBlockAndCounter`](./Enums.md) | Equation / Object || 3 | `15%`<br>`25%`<br>`33%` |
| [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#object-damageneighborsaftermove) | Object  || 3 | `{ . . . }` |
| [`ElementalManaCostReduction`](./Passives_and_Statuses.md#object-elementalmanacostreduction) | Object  || 3 | `{ . . . }` |
| [`ExtraBasicMoves_Status`](./Enums.md) | Integer | The number of extra basic moves per turn granted. | 3 | `1` |
| [`ExtraMovePoints`](./Enums.md) | Integer | The number of additional movement points granted to this unit. | 3 | `1` |
| [`FlowersOnEndTurn`](./Enums.md) | Integer || 3 | `1`<br>`3`<br>`4` |
| [`IncreaseSpellRange`](./Enums.md) | Integer || 3 | `10`<br>`2`<br>`20` |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum  || 3 | `Food` |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum  || 3 | `Cannibalize`<br>`EatShit`<br>`face_EatNeverstone` |
| [`MoveQuivered`](./Enums.md) | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 3 | `1`<br>`2`<br>`[1, 0.1]` |
| [`NeckArmorPassiveMultiplierBonus`](./Enums.md) | Integer || 3 | `1`<br>`2` |
| [`PassiveAfterXKills`](./Passives_and_Statuses.md#object-passiveafterxkills) | Object  || 3 | `{ . . . }` |
| [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#object-passiveifemptyface) | Object  || 3 | `{ . . . }` |
| [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#object-passiveifemptyhead) | Object  || 3 | `{ . . . }` |
| [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#object-passiveifemptyneck) | Object  || 3 | `{ . . . }` |
| [`ProtectTargetedAllies`](./Enums.md#enum-protecttargetedallies) | Enum  | Specifies the ability used to protect targeted allies, including an optional target filter. | 3 | `SwapPositions_WideLoad`<br>`SwapPositions_WideLoad2` |
| [`RandomPassivePool`](./Passives_and_Statuses.md#object-randompassivepool) | Object  | A pool of random passives from which one is chosen for this unit. | 3 | `{ . . . }` |
| [`RangedTrueShot`](./Enums.md) | Integer || 3 | `1` |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md#enum-replacebasicattackwhencastable) | Enum  || 3 | `BasicSuplex`<br>`Hone`<br>`Hone2` |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array  || 3 | `[Boulder AnimatedBoulder]`<br>`[Boulder AnimatedLavaBoulder]`<br>`[Crow Crow2]` |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum  || 3 | `euphoric`<br>`insane` |
| [`SpawnCreepOnHit`](./Enums.md) | Integer | If set to 1, spawns creep on the tile when this unit takes damage. | 3 | `1` |
| [`SpawnObjectOnPopCorpse`](./Enums.md#enum-spawnobjectonpopcorpse) | Enum  || 3 | `Catnip`<br>`Coin`<br>`Food` |
| [`StatusAfterCastSpell`](./Passives_and_Statuses.md#object-statusaftercastspell) | Object  || 3 | `{ . . . }` |
| [`StatusOnBreakItem`](./Passives_and_Statuses.md#object-statusonbreakitem) | Object  || 3 | `{ . . . }` |
| [`StatusOnCrit`](./Passives_and_Statuses.md#object-statusoncrit) | Object  || 3 | `{ . . . }` |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#object-statusoneatfood) | Object  | An object listing status effects applied to the unit when it eats food. | 3 | `{ . . . }` |
| [`StatusOnOverHealed`](./Passives_and_Statuses.md#object-statusonoverhealed) | Object  || 3 | `{ . . . }` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object  || 3 | `{ . . . }` |
| [`StatusOnTurnEndIfCastNSpells`](./Passives_and_Statuses.md#object-statusonturnendifcastnspells) | Object  || 3 | `{ . . . }` |
| [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#object-statusonuseabilitywithtag) | Object  || 3 | `{ . . . }` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`WeaponsDontLoseDurability`](./Enums.md) | Integer | If set to 1, weapons equipped by this unit do not lose durability. | 3 | `0`<br>`1` |
| [`AddDamageToBasicAttack`](./Enums.md) | Integer || 2 | `1`<br>`2`<br>`4` |
| [`AddSelfStatusToWeapons`](./Passives_and_Statuses.md#object-addselfstatustoweapons) | Object  || 2 | `{ . . . }` |
| [`AddStartingMana`](./Enums.md) | Integer | The amount of bonus mana the unit starts each battle with. | 2 | `20`<br>`5` |
| [`AddStatusToKnockbackDamage`](./Passives_and_Statuses.md#object-addstatustoknockbackdamage) | Object  || 2 | `{ . . . }` |
| [`AddUnfilledMaxHealth`](./Enums.md) | Integer || 2 | `10`<br>`20`<br>`50` |
| [`AllyDamageReduction`](./Enums.md) | Integer || 2 | `0` |
| [`AllyManaRegenAura`](./Passives_and_Statuses.md#object-allymanaregenaura) | Object  || 2 | `{ . . . }` |
| [`AutocastEachTurn`](./Enums.md#enum-autocasteachturn) | Enum  || 2 | `DarkOneStrike`<br>`ViolentOutburst` |
| [`AutocastEachTurnBegin`](./Passives_and_Statuses.md#object-autocasteachturnbegin) | Enum / Object  || 2 | `{ . . . }`<br>`MindCrack_EldritchVisage`<br>`MindCrack_EldritchVisage2` |
| [`BasicAttackAOEBonus`](./Enums.md) | Integer || 2 | `1`<br>`2` |
| [`BouncyProjectiles`](./Passives_and_Statuses.md#object-bouncyprojectiles) | Object  || 2 | `{ . . . }` |
| [`CCImmunity`](./Enums.md) | Integer | If set to 1, this unit is immune to crowd control effects. | 2 | `1` |
| [`CanRemoveCursedItems`](./Enums.md) | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 2 | `1` |
| [`CapMovementAbilityRange`](./Enums.md) | Integer || 2 | `1` |
| [`ChangeTauntPriority`](./Enums.md) | Integer || 2 | `-1` |
| [`ConsumableEffectsMultiplierBonus`](./Enums.md) | Integer || 2 | `1` |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum  || 2 | `all_items`<br>`all_spells`<br>`basic_attack` |
| [`DoubleCastWeapons`](./Enums.md) | Integer || 2 | `1`<br>`2` |
| [`Eternal`](./Passives_and_Statuses.md#object-eternal) | Object  || 2 | `{ . . . }` |
| [`FlyDamageIncrease`](./Enums.md) | Integer || 2 | `1`<br>`4` |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum  | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 2 | `Grass`<br>`Water` |
| [`GainExtraShield`](./Enums.md) | Integer || 2 | `2`<br>`4` |
| [`HPGainBlock`](./Enums.md) | Integer || 2 | `1` |
| [`InfiniteRebirth`](./Passives_and_Statuses.md#object-infiniterebirth) | Object  | Specifies the health and effects for unlimited rebirth upon death. | 2 | `{ . . . }` |
| [`ManaCostReductionTagged`](./Passives_and_Statuses.md#object-manacostreductiontagged) | Object  || 2 | `{ . . . }` |
| [`MoveAwayFromDamageSource`](./Enums.md#enum-moveawayfromdamagesource) | Enum  | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 2 | `BasicJump`<br>`MoveOne` |
| [`MoveSpeedMultiplier`](./Enums.md) | Float || 2 | `.5` |
| [`NubbyTossPriority`](./Enums.md) | Integer || 2 | `1` |
| [`PassiveLevelUpAtCombatEnd`](./Enums.md) | Integer || 2 | `1` |
| [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#object-passivewhenatfullmana) | Object  | An object listing passive effects that are active only while the unit's mana is full. | 2 | `{ . . . }` |
| [`PassiveWhileInMonkMeleeStance`](./Passives_and_Statuses.md#object-passivewhileinmonkmeleestance) | Object  || 2 | `{ . . . }` |
| [`PoopWhenHit`](./Enums.md#enum-poopwhenhit) | Enum  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 2 | `Poop` |
| [`RemoveLineOfSightRestrictions`](./Enums.md) | Integer || 2 | `1` |
| [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#object-scaledstatusonspendmana) | Object  || 2 | `{ . . . }` |
| [`SharePickups`](./Enums.md) | Integer | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 2 | `1` |
| [`SpawnCatCopyOnBattleStart`](./Passives_and_Statuses.md#object-spawncatcopyonbattlestart) | Object  || 2 | `{ . . . }` |
| [`StatsAtLowHealth`](./Passives_and_Statuses.md#object-statsatlowhealth) | Object  || 2 | `{ . . . }` |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 | `{ . . . }` |
| [`StatusKilledCharacters`](./Passives_and_Statuses.md#object-statuskilledcharacters) | Object  | An object listing status effects applied to the unit when it kills a character. | 2 | `{ . . . }` |
| [`StatusOnCollectPickup`](./Passives_and_Statuses.md#object-statusoncollectpickup) | Object  || 2 | `{ . . . }` |
| [`StatusOnEatPill`](./Passives_and_Statuses.md#object-statusoneatpill) | Object  || 2 | `{ . . . }` |
| [`StatusOnHealed`](./Passives_and_Statuses.md#object-statusonhealed) | Object  || 2 | `{ . . . }` |
| [`StatusOnPickupCoins`](./Passives_and_Statuses.md#object-statusonpickupcoins) | Object  || 2 | `{ . . . }` |
| [`StatusOnTurnEndIfManaExact`](./Passives_and_Statuses.md#object-statusonturnendifmanaexact) | Object  || 2 | `{ . . . }` |
| [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#object-statusonturnendifmanaorhealthexact) | Object  || 2 | `{ . . . }` |
| [`StatusOnUseBasicAttack`](./Passives_and_Statuses.md#object-statusonusebasicattack) | Object  || 2 | `{ . . . }` |
| [`StatusWhenAllySpendsMana`](./Passives_and_Statuses.md#object-statuswhenallyspendsmana) | Object  || 2 | `{ . . . }` |
| [`TauntAlways`](./Enums.md) | Integer || 2 | `1` |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum  | Specifies the ability or attack used when the unit counterattacks in tower defense reflex mode. | 2 | `BasicRanged_1DMG`<br>`attack` |
| [`UncappedHP`](./Enums.md) | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 2 | `1` |
| [`UpgradeSpawnedPickups`](./Enums.md) | Integer || 2 | `1`<br>`2` |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`WeaponActiveEffectsMultiplierBonus`](./Enums.md) | Integer || 2 | `2` |
| [`WeaponDamageMultiplierBonus`](./Enums.md) | Integer || 2 | `1`<br>`2` |
| [`WeaponPassiveMultiplierBonus`](./Enums.md) | Integer || 2 | `2` |
| [`AbsorbManaAura`](./Enums.md) | Integer || 1 | `1` |
| [`AddAllyNeighborsToAttackRange`](./Enums.md) | Integer || 1 | `1` |
| [`AddLevelUpStatMultiplier`](./Enums.md) | Integer || 1 | `1` |
| [`AddPassiveToSpawnedRocks`](./Passives_and_Statuses.md#object-addpassivetospawnedrocks) | Object  || 1 | `{ . . . }` |
| [`AddPassivesToSummonAbilityMinions`](./Passives_and_Statuses.md#object-addpassivestosummonabilityminions) | Object  || 1 | `{ . . . }` |
| [`AddSpellDamage`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`AddStatusToBasicAttackWithCooldown`](./Passives_and_Statuses.md#object-addstatustobasicattackwithcooldown) | Object  || 1 | `{ . . . }` |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#object-addstatustoexplosions) | Object  || 1 | `{ . . . }` |
| [`AddStatusToFirstBasicAttack`](./Passives_and_Statuses.md#object-addstatustofirstbasicattack) | Object  || 1 | `{ . . . }` |
| [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#object-addstatustomeleedamage) | Object  || 1 | `{ . . . }` |
| [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#object-addstatustoreceiveddamage_excludestatuses) | Object  || 1 | `{ . . . }` |
| [`AddStatusToTrampleDamage`](./Passives_and_Statuses.md#object-addstatustotrampledamage) | Object  || 1 | `{ . . . }` |
| [`AddStatusesIfPersistentWeatherElement`](./Passives_and_Statuses.md#object-addstatusesifpersistentweatherelement) | Object  || 1 | `{ . . . }` |
| [`AddStatusesToReceivedElementalDamage`](./Passives_and_Statuses.md#object-addstatusestoreceivedelementaldamage) | Object  || 1 | `{ . . . }` |
| [`AddWeaponScaling`](./Enums.md) | Integer || 1 | `1` |
| [`AfterImage`](./Enums.md#enum-afterimage) | Enum  | Specifies the object or skill used to create an afterimage of the unit. | 1 | `PlayerCat_ThiefShade`<br>`PlayerCat_ThiefShade2` |
| [`AllowPassTurn`](./Enums.md) | Integer || 1 | `0`<br>`1` |
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum  || 1 | `attack` |
| [`AllyHealthRegenAura`](./Passives_and_Statuses.md#object-allyhealthregenaura) | Object  || 1 | `{ . . . }` |
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum  || 1 | `CatapultJump`<br>`CatapultJump2` |
| [`AllyMultiplyKnockbackDamage`](./Enums.md) | Integer || 1 | `2` |
| [`AlphaCat`](./Enums.md) | Integer | The number of AlphaCat stacks applied to the source on kill. | 1 | `1` |
| [`AlternateCraftingPools`](./Passives_and_Statuses.md#object-alternatecraftingpools) | Object  || 1 | `{ . . . }` |
| [`AmplifyPositiveStatus`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`Autism`](./Passives_and_Statuses.md#object-autism) | Object  || 1 | `{ . . . }` |
| [`AutoCritLowDamage`](./Enums.md) | Integer || 1 | `2`<br>`3` |
| [`BackstabWeakness`](./Enums.md) | Float || 1 | `0.75` |
| [`BasicAttackStatusCarefulness`](./Enums.md) | Integer || 1 | `1` |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum  | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 1 | `catnip`<br>`food` |
| [`BonusFoodEachBattle`](./Enums.md) | Integer || 1 | `2`<br>`20` |
| [`BoobyTrapItems`](./Passives_and_Statuses.md#object-boobytrapitems) | Object  || 1 | `{ . . . }` |
| [`BoostAllyStatsOnDeath`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`BoostDamageAura`](./Enums.md) | Integer || 1 | `1` |
| [`BoostRangeAura`](./Enums.md) | Integer || 1 | `1` |
| [`BraceForEachNeighboringEnemy`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`CantDodge`](./Enums.md) | Integer || 1 | `1` |
| [`CapDamageFromAllies`](./Enums.md) | Integer || 1 | `1` |
| [`CatAPultAnimation`](./Passives_and_Statuses.md#object-catapultanimation) | Object  || 1 | `{ . . . }` |
| [`ChainKnockback`](./Enums.md) | Integer || 1 | `1` |
| [`CharmAllFlies`](./Enums.md) | Integer || 1 | `1` |
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum  || 1 | `BasicMonkMelee` |
| [`CoinsAddDamage`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`CollectPickupsOnBattleEnd`](./Passives_and_Statuses.md#object-collectpickupsonbattleend) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`Conductor`](./Enums.md) | Integer || 1 | `2` |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md#enum-confusioneffectontaggedabilities) | Enum  || 1 | `consumable` |
| [`ConjureCastSpellsForAllies`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`ConsumablesInfiniteRange`](./Enums.md) | Integer || 1 | `1` |
| [`ConsumablesMeleeRange`](./Enums.md) | Integer || 1 | `1` |
| [`DamageEnemiesOnHeal`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`DamageEnemiesOnKill`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`DamageIfDidntUseSpecificAbility`](./Passives_and_Statuses.md#object-damageifdidntusespecificability) | Object  || 1 | `{ . . . }` |
| [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#object-damageneighbortileswhencastspell) | Object  || 1 | `{ . . . }` |
| [`DamageReductionAura`](./Passives_and_Statuses.md#object-damagereductionaura) | Object  || 1 | `{ . . . }` |
| [`DeathChill`](./Enums.md) | Integer || 1 | `1` |
| [`DejaVu`](./Enums.md) | Integer || 1 | `10%` |
| [`Diabetes`](./Passives_and_Statuses.md#object-diabetes) | Object  || 1 | `{ . . . }` |
| [`DirtyClaws`](./Enums.md) | Integer || 1 | `1` |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum  | Specifies a tag that disables any ability with that tag on the unit. | 1 | `consumable`<br>`meat`<br>`musical` |
| [`Doomed`](./Enums.md) | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 1 | `1`<br>`2`<br>`3` |
| [`DukeOfFlies`](./Enums.md) | Integer || 1 | `1` |
| [`Dyslexia`](./Arrays.md#array-dyslexia) | Array  || 1 | `[3 5]`<br>`[6 9]` |
| [`EMP`](./Passives_and_Statuses.md#object-emp) | Object  || 1 | `{ . . . }` |
| [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement) | Object  || 1 | `{ . . . }` |
| [`Empath`](./Enums.md) | Integer || 1 | `100%`<br>`50%` |
| [`EnemiesGetPickupsKnockedOut`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`EnergyStorm`](./Passives_and_Statuses.md#object-energystorm) | Integer / Object  || 1 | `{ . . . }`<br>`3` |
| [`EquipmentPassiveMultiplierBonus`](./Enums.md) | Integer || 1 | `1` |
| [`EquipmentSetBonusBonus`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`EscapeSequence`](./Passives_and_Statuses.md#object-escapesequence) | Object  || 1 | `{ . . . }` |
| [`ExhaustionRoundChange`](./Enums.md) | Integer || 1 | `3` |
| [`ExplodeOverkilledEnemies`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`ExplosionImmunity`](./Enums.md) | Integer || 1 | `1` |
| [`ExtraInjuryOnDeath`](./Enums.md) | Integer || 1 | `1` |
| [`ExtraTrinketUses`](./Enums.md) | Integer || 1 | `1`<br>`10` |
| [`FamiliarSecondaryDamageImmunity`](./Enums.md) | Integer || 1 | `1` |
| [`FlowerPowerAuraBrace`](./Enums.md) | Integer || 1 | `1` |
| [`FlowerPowerAuraStrength`](./Enums.md) | Integer || 1 | `1` |
| [`FollowUp`](./Enums.md#enum-followup) | Enum  || 1 | `FollowUpDash`<br>`FollowUpDash2` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`FreeSpellsAtFullMana`](./Enums.md) | Integer || 1 | `1` |
| [`FrontstabBasicAttackCritChance`](./Enums.md) | Integer || 1 | `100%` |
| [`FullHeal`](./Enums.md) | Integer | If non-zero, fully restores the target's health. | 1 | `0`<br>`1` |
| [`FullHealthCritChance`](./Enums.md) | Integer || 1 | `100` |
| [`FullPower`](./Enums.md) | Integer || 1 | `3` |
| [`FurnitureStats`](./Passives_and_Statuses.md#object-furniturestats) | Object  || 1 | `{ . . . }` |
| [`GravityWell`](./Passives_and_Statuses.md#object-gravitywell) | Object  || 1 | `{ . . . }` |
| [`HealDamagesEnemies`](./Enums.md) | Integer || 1 | `1` |
| [`HealsAlsoRegenMana`](./Enums.md) | Integer || 1 | `2`<br>`50%` |
| [`HealsCanRevive`](./Enums.md) | Integer || 1 | `1`<br>`3` |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum  || 1 | `any`<br>`crow` |
| [`HouseFoodRequirementMultiplier`](./Enums.md) | Integer | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 1 | `0` |
| [`Hypomania`](./Enums.md) | Integer || 1 | `3` |
| [`ImmortalLeeches`](./Enums.md) | Integer || 1 | `1` |
| [`IncreaseHealingSpellRange`](./Enums.md) | Integer || 1 | `2` |
| [`InvertBrainFaction`](./Enums.md) | Integer || 1 | `1` |
| [`KillsHeal`](./Enums.md) | Integer || 1 | `5`<br>`50%` |
| [`LateBloomer`](./Passives_and_Statuses.md#object-latebloomer) | Object  || 1 | `{ . . . }` |
| [`LightningAspectCharge`](./Enums.md) | Integer || 1 | `0`<br>`1` |
| [`LightningRod`](./Passives_and_Statuses.md#object-lightningrod) | Object  || 1 | `{ . . . }` |
| [`LimitSelfKnockbackDamage`](./Enums.md) | Integer || 1 | `1` |
| [`LimitedTileTrail`](./Enums.md#enum-limitedtiletrail) | Enum  || 1 | `FlowerTile` |
| [`LineOfSightTrueSightAura`](./Enums.md) | Float || 1 | `.5`<br>`0` |
| [`LobbedHook`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`LowHealthAllyDodgeChanceAura`](./Passives_and_Statuses.md#object-lowhealthallydodgechanceaura) | Object  || 1 | `{ . . . }` |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| [`MakeBasicAttackPassThroughThings`](./Enums.md) | Integer || 1 | `1` |
| [`ManaRegenMultiplierIfManaEmpty`](./Enums.md) | Integer || 1 | `2` |
| [`MaxAccuracy`](./Enums.md) | Integer || 1 | `1` |
| [`MaxStartingMana`](./Enums.md) | Integer || 1 | `1` |
| [`MegaMinions`](./Passives_and_Statuses.md#object-megaminions) | Integer / Object  || 1 | `{ . . . }`<br>`3` |
| [`MetalDetector`](./Enums.md) | Integer || 1 | `10`<br>`5` |
| [`MinimumTech`](./Enums.md) | Integer || 1 | `1` |
| [`NoManaRegen`](./Enums.md) | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 1 | `1` |
| [`NoReflection`](./Enums.md) | Integer || 1 | `1` |
| [`NumbingLeeches`](./Enums.md) | Integer || 1 | `3` |
| [`OverhealGainsBothShield`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`OverrideMaxMana`](./Enums.md) | Integer || 1 | `1` |
| [`OverridePalette`](./Enums.md) | Integer || 1 | `87` |
| [`Paranoia`](./Enums.md#enum-paranoia) | Enum  || 1 | `ParanoiaBasicMelee` |
| [`ParasitesArentCursed`](./Enums.md) | Integer || 1 | `1` |
| [`PassiveAtFullHealth`](./Passives_and_Statuses.md#object-passiveatfullhealth) | Object  || 1 | `{ . . . }` |
| [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#object-passiveatinjurythreshold) | Object  || 1 | `{ . . . }` |
| [`PassiveLevelScaledStatus`](./Passives_and_Statuses.md#object-passivelevelscaledstatus) | Object  || 1 | `{ . . . }` |
| [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#object-passiveuntilcastspell) | Object  || 1 | `{ . . . }` |
| [`PassiveUntilGetKill`](./Passives_and_Statuses.md#object-passiveuntilgetkill) | Object  || 1 | `{ . . . }` |
| [`PassiveWhenTheAlpha`](./Passives_and_Statuses.md#object-passivewhenthealpha) | Object  || 1 | `{ . . . }` |
| [`PassiveWhileInMonkRangedStance`](./Passives_and_Statuses.md#object-passivewhileinmonkrangedstance) | Object  || 1 | `{ . . . }` |
| [`PassiveWhilePreviewingMonkRangedStance`](./Passives_and_Statuses.md#object-passivewhilepreviewingmonkrangedstance) | Object  || 1 | `{ . . . }` |
| [`PassiveWhileWearingMetal`](./Passives_and_Statuses.md#object-passivewhilewearingmetal) | Object  || 1 | `{ . . . }` |
| [`PermanentImmobile`](./Enums.md) | Integer | The permanent amount of immobility stacks applied. | 1 | `1` |
| [`PermanentItems`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`PermanentKitten`](./Enums.md) | Integer || 1 | `1` |
| [`Phasing`](./Enums.md) | Integer | If set to 1, allows the character to phase through solid objects or obstacles. | 1 | `1` |
| [`Quiver`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`RealTimePressure_OneUnit`](./Enums.md) | Integer || 1 | `5` |
| [`ReceivedStatusReplacement`](./Arrays.md#array-receivedstatusreplacement) | Array  || 1 | `[Sleep SleepParalysis]` |
| [`RemoveOncePerFightRestriction`](./Enums.md) | Integer || 1 | `1` |
| [`ReplaceBasicAttackWhenDead`](./Enums.md#enum-replacebasicattackwhendead) | Enum  || 1 | `Haunt` |
| [`ReviveOnWin`](./Enums.md) | Integer || 1 | `100%` |
| [`RobotsInheritArmor`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`RockDetector`](./Enums.md) | Integer || 1 | `10` |
| [`ScaledStatusOnBleedDamage`](./Passives_and_Statuses.md#object-scaledstatusonbleeddamage) | Object  || 1 | `{ . . . }` |
| [`ScaledStatusOnOverMana`](./Passives_and_Statuses.md#object-scaledstatusonovermana) | Object  || 1 | `{ . . . }` |
| [`SchrodingerDisorder`](./Enums.md) | Integer || 1 | `50%` |
| [`Scleroderma`](./Enums.md) | Integer || 1 | `1` |
| [`SelfDamageWhenDealDamage`](./Passives_and_Statuses.md#object-selfdamagewhendealdamage) | Object  || 1 | `{ . . . }` |
| [`ShareHealthRegen`](./Enums.md) | Integer || 1 | `1` |
| [`ShoulderCheck`](./Enums.md) | Integer || 1 | `100%`<br>`33%` |
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum  || 1 | `attack` |
| [`ShowHiddenThings`](./Enums.md) | Integer | If nonzero, reveals hidden objects or tiles on the map. | 1 | `1` |
| [`Slow`](./Enums.md) | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 1 | `-1`<br>`1`<br>`2` |
| [`SmallEnemiesIgnoreYou`](./Enums.md) | Integer || 1 | `1` |
| [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#object-smiteenemieswhokill) | Object  || 1 | `{ . . . }` |
| [`SpecialFriends`](./Passives_and_Statuses.md#object-specialfriends) | Object  || 1 | `{ . . . }` |
| [`SplittableMove`](./Enums.md) | Integer || 1 | `1`<br>`3` |
| [`SpreadExtraDebuffs`](./Enums.md) | Integer || 1 | `1`<br>`2` |
| [`SpreadPainBonus`](./Enums.md) | Integer || 1 | `2` |
| [`StatMinimum`](./Enums.md) | Integer || 1 | `5`<br>`7` |
| [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#object-statusadjacentontheirturnbegin) | Object  || 1 | `{ . . . }` |
| [`StatusAlliesOnGainCoins`](./Passives_and_Statuses.md#object-statusalliesongaincoins) | Object  || 1 | `{ . . . }` |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#object-statusalliesonkill) | Object  || 1 | `{ . . . }` |
| [`StatusAllyWhenAllySpendsMana`](./Passives_and_Statuses.md#object-statusallywhenallyspendsmana) | Object  || 1 | `{ . . . }` |
| [`StatusAnyCatAllyWhoKills`](./Passives_and_Statuses.md#object-statusanycatallywhokills) | Object  || 1 | `{ . . . }` |
| [`StatusDamagers`](./Passives_and_Statuses.md#object-statusdamagers) | Object  || 1 | `{ . . . }` |
| [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#object-statuseachturnendperenemykill) | Object  || 1 | `{ . . . }` |
| [`StatusEnemiesOnDeath`](./Passives_and_Statuses.md#object-statusenemiesondeath) | Object  || 1 | `{ . . . }` |
| [`StatusEveryXTurnBegins`](./Passives_and_Statuses.md#object-statuseveryxturnbegins) | Object  || 1 | `{ . . . }` |
| [`StatusIfBattleAlreadyBegan`](./Passives_and_Statuses.md#object-statusifbattlealreadybegan) | Object  || 1 | `{ . . . }` |
| [`StatusKillers`](./Passives_and_Statuses.md#object-statuskillers) | Object  | An object containing nested conditionals that apply status effects when the unit kills an enemy. | 1 | `{ . . . }` |
| [`StatusOnAnyDeath`](./Passives_and_Statuses.md#object-statusonanydeath) | Object  || 1 | `{ . . . }` |
| [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#object-statusonbattleendifkillthresholdmet) | Object  || 1 | `{ . . . }` |
| [`StatusOnDealtDamage`](./Passives_and_Statuses.md#object-statusondealtdamage) | Object  || 1 | `{ . . . }` |
| [`StatusOnDealtDamageThreshold`](./Passives_and_Statuses.md#object-statusondealtdamagethreshold) | Object  || 1 | `{ . . . }` |
| [`StatusOnGainShield`](./Passives_and_Statuses.md#object-statusongainshield) | Object  || 1 | `{ . . . }` |
| [`StatusOnHeal`](./Passives_and_Statuses.md#object-statusonheal) | Object  || 1 | `{ . . . }` |
| [`StatusOnLoseShield`](./Passives_and_Statuses.md#object-statusonloseshield) | Object  || 1 | `{ . . . }` |
| [`StatusOnOverMana`](./Passives_and_Statuses.md#object-statusonovermana) | Object  || 1 | `{ . . . }` |
| [`StatusOnTakeHealthDamage`](./Passives_and_Statuses.md#object-statusontakehealthdamage) | Object  || 1 | `{ . . . }` |
| [`StatusOnTookDamageFromEnemyAbility`](./Passives_and_Statuses.md#object-statusontookdamagefromenemyability) | Object  || 1 | `{ . . . }` |
| [`StatusOnTriggerTrap`](./Passives_and_Statuses.md#object-statusontriggertrap) | Object  || 1 | `{ . . . }` |
| [`StatusOnUseElementAbility`](./Passives_and_Statuses.md#object-statusonuseelementability) | Object  || 1 | `{ . . . }` |
| [`StatusPerInjury`](./Passives_and_Statuses.md#object-statusperinjury) | Object  || 1 | `{ . . . }` |
| [`StatusReplacement`](./Arrays.md#array-statusreplacement) | Array  || 1 | `[Petrify PetrifyCharmed]` |
| [`StatusThingsKnockedBack`](./Passives_and_Statuses.md#object-statusthingsknockedback) | Object  || 1 | `{ . . . }` |
| [`Stealth`](./Enums.md) | Integer | The number of stealth stacks applied. | 1 | `1`<br>`2`<br>`[1 .1]` |
| [`StrengthForEachNeighboringEnemy`](./Enums.md) | Integer || 1 | `2`<br>`3` |
| [`StrengthInNumbersAura`](./Passives_and_Statuses.md#object-strengthinnumbersaura) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`StrictLimitDamage`](./Enums.md) | Integer || 1 | `1` |
| [`Study`](./Passives_and_Statuses.md#object-study) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`TaggedPickupEffectReplacement`](./Passives_and_Statuses.md#object-taggedpickupeffectreplacement) | Object  || 1 | `{ . . . }` |
| [`TauntAtFullHealth`](./Enums.md) | Integer || 1 | `1` |
| [`Tech`](./Enums.md) | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 1 | `1`<br>`3` |
| [`TempInitiativeChange`](./Enums.md) | Integer | The flat change to the unit's initiative value. | 1 | `-100`<br>`-999`<br>`100` |
| [`TheHunger`](./Passives_and_Statuses.md#object-thehunger) | Object  || 1 | `{ . . . }` |
| [`TileDamageMultiplier`](./Passives_and_Statuses.md#object-tiledamagemultiplier) | Integer / Object  || 1 | `{ . . . }`<br>`2` |
| [`TourettesMeows`](./Passives_and_Statuses.md#object-tourettesmeows) | Object  || 1 | `{ . . . }` |
| [`TowerDefense`](./Passives_and_Statuses.md#object-towerdefense) | Object  || 1 | `{ . . . }` |
| [`TrapEffectsMultiplier`](./Enums.md) | Integer || 1 | `2` |
| [`Triskaidekaphobia`](./Enums.md) | Integer || 1 | `13` |
| [`UncappedMana`](./Enums.md) | Integer || 1 | `1` |
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum  || 1 | `Colorless` |
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum  || 1 | `Colorless` |
| [`Vegan`](./Enums.md) | Integer | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 1 | `1` |
| [`Vengeful`](./Enums.md) | Integer || 1 | `1` |
| [`WeaponCountsAsBasicAttack`](./Enums.md) | Integer || 1 | `1` |
| [`WobblyCat`](./Enums.md) | Integer || 1 | `25%` |

</details>


---


### Object: `stats`


**Definition:** Core character metrics (Health, Strength, etc.).  
**Total Count:** 97

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 34 | `-1`<br>`-2`<br>`-3` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 27 | `-1`<br>`-10`<br>`-2` |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 24 | `+1`<br>`-1`<br>`-2` |
| [`int`](./Enums.md#enum-int) | Enum / Integer  || 24 | `-1`<br>`-10`<br>`-2` |
| [`str`](./Enums.md#enum-str) | Enum / Integer  || 22 | `-1`<br>`-2`<br>`-3` |
| [`dex`](./Enums.md#enum-dex) | Enum / Integer  || 18 | `-1`<br>`-2`<br>`-3` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer  || 16 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `AddStatusToBasicAttack`


**Definition:** Injects a status effect payload that applies whenever the character performs a basic attack.  
**Total Count:** 92

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 205 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 | `Default`<br>`FormChange`<br>`Druid` | [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 30 | `1`<br>`10`<br>`2` |
| [`Poison`](./Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 29 | `1`<br>`10`<br>`2` |
| [`Knockback`](./Enums.md) | Equation | The number of tiles the target is pushed away from the source on hit. | 24 | `1`<br>`10`<br>`2` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 16 | `1`<br>`10`<br>`2` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 13 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 12 | `1`<br>`2`<br>`3` |
| [`ChangeTile`](./Passives_and_Statuses.md#object-changetile) | Enum / Object  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 10 | `{ . . . }`<br>`BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Slow`](./Enums.md) | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 10 | `-1`<br>`1`<br>`2` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`2`<br>`3` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 7 | `1`<br>`10`<br>`2` |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 7 | `1`<br>`2`<br>`3` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  || 5 | `{ . . . }` |
| [`Leech`](./Enums.md) | Integer | The amount of health leeched from the target (heals the attacker). | 5 | `1`<br>`2` |
| [`Rot`](./Enums.md) | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 5 | `-999999`<br>`1`<br>`2` |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum  | Specifies the object or projectile to spawn and bounce from the target. | 4 | `AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`DamageOrHealConditionally`](./Enums.md) | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 4 | `1` |
| [`DistanceBonusDamage`](./Passives_and_Statuses.md#object-distancebonusdamage) | Object  || 4 | `{ . . . }` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 4 | `1`<br>`2`<br>`[1 .01]` |
| [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 4 | `1`<br>`2`<br>`3` |
| [`SoulLink`](./Enums.md) | Integer | The number of soul link stacks applied. | 4 | `1` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 3 | `1`<br>`2`<br>`3` |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object  || 3 | `{ . . . }` |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| [`MagicWeakness`](./Enums.md) | Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`3` |
| [`Piercing`](./Enums.md) | Integer || 3 | `1` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 3 | `{ . . . }` |
| [`ApplyStatusIfCrit`](./Passives_and_Statuses.md#object-applystatusifcrit) | Object  || 2 | `{ . . . }` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 2 | `{ . . . }` |
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 2 | `-1`<br>`1`<br>`2` |
| [`BurgleCoin`](./Enums.md) | Integer | The number of coins stolen from the target, or an array of `[number, probability]`. | 2 | `1`<br>`3`<br>`[1 .5]` |
| [`Conditional_Adjacent`](./Passives_and_Statuses.md#object-conditional_adjacent) | Object  || 2 | `{ . . . }` |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#object-conditional_shielded) | Object  || 2 | `{ . . . }` |
| [`KnockOutCoin`](./Arrays.md#array-knockoutcoin) | Array / Integer  | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 2 | `1`<br>`[1 .5]` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`ManaLeeches`](./Enums.md) | Integer | The number of mana leech stacks applied. | 2 | `1`<br>`2` |
| [`OverrideChainKnockback`](./Enums.md) | Integer | The custom number of tiles for chain knockback, overriding the default. | 2 | `0`<br>`1`<br>`10` |
| [`SpawnBearTrapOnMiss`](./Enums.md) | Integer || 2 | `1` |
| [`BigSplashDamage`](./Enums.md) | Integer || 1 | `2` |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |
| [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#object-conditional_sourcehastag) | Object  || 1 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`OverrideChainKnockbackDamage`](./Enums.md) | Equation | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). | 1 | `0`<br>`3+bonus_melee_ability_damage` |
| [`SplashDamage`](./Enums.md) | Integer | The radius (in tiles) for splash damage applied to adjacent targets. | 1 | `1`<br>`2` |

</details>


---


### Object: `effects`


**Definition:** Non-damaging status applications and logic triggers executed on impact.  
**Total Count:** 30

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#context-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#context-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#context-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#context-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#context-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#context-fire), [`ice`](./Passives_and_Statuses.md#context-ice), [`lightning`](./Passives_and_Statuses.md#context-lightning), [`triattack`](./Passives_and_Statuses.md#context-triattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1695 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 750 | `Default`<br>`FormChange`<br>`Druid` | [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 98 | `1`<br>`2`<br>`3` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 85 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 79 | `1`<br>`2`<br>`3` |
| [`Poison`](./Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 67 | `1`<br>`10`<br>`2` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 54 | `1`<br>`10`<br>`2` |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum  | Specifies the name of the visual effect to play on the target tile. | 34 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 31 | `1`<br>`10`<br>`2` |
| [`Slow`](./Enums.md) | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 29 | `-1`<br>`1`<br>`2` |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 24 | `0`<br>`1`<br>`10%` |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 23 | `1`<br>`2`<br>`3` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 22 | `1`<br>`2`<br>`3` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 19 | `1`<br>`2`<br>`[1 .01]` |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 19 | `1`<br>`2`<br>`3` |
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. | 15 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`Leeches`](./Enums.md) | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 14 | `1`<br>`2`<br>`3` |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 9 | `1`<br>`3`<br>`5` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 8 | `{ . . . }` |

</details>


---


### Object: `AddPassivesToMinions`


**Definition:** Applies the 'AddPassivesToMinions' effect.  
**Total Count:** 29

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 35 | `passives`<br>`class`<br>`tag` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 7 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 7 | `1`<br>`10`<br>`2` |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 6 | `-25`<br>`10`<br>`2` |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 4 | `{ . . . }` |
| [`IncreaseExplosionDamage`](./Enums.md) | Integer || 4 | `1`<br>`2`<br>`3` |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum  | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 3 | `Grass`<br>`Water` |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum  || 3 | `crow`<br>`grub_familiar`<br>`rock` |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 2 | `-3`<br>`4`<br>`6` |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#object-addstatustoexplosions) | Object  || 2 | `{ . . . }` |
| [`EMP`](./Passives_and_Statuses.md#object-emp) | Object  || 2 | `{ . . . }` |
| [`FamiliarBonusAbility`](./Enums.md#enum-familiarbonusability) | Enum  || 2 | `FamiliarSelfDestruct`<br>`FamiliarSelfDestruct2` |
| [`ForceAttack`](./Enums.md) | Integer | If set to 1, forces the target to perform an attack against a random or specified target. | 2 | `1` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 2 | `1`<br>`2`<br>`3` |
| [`HolyShieldTransferToSpawner`](./Enums.md) | Integer || 2 | `1` |
| [`IncreaseExplosionSize`](./Enums.md) | Integer || 2 | `1`<br>`2`<br>`7` |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 2 | `{ . . . }` |
| [`PoisonThorns`](./Enums.md) | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 2 | `1`<br>`2`<br>`3` |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#object-statusalliesonkill) | Object  || 2 | `{ . . . }` |
| [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 2 | `{ . . . }` |
| [`WaterWalk`](./Enums.md) | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 2 | `1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`AddUnfilledMaxHealth`](./Enums.md) | Integer || 1 | `10`<br>`20`<br>`50` |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`GrassTileHealing`](./Enums.md) | Integer || 1 | `1` |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| [`SafeExplosions`](./Enums.md) | Integer || 1 | `1` |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 1 | `1` |
| [`UncappedHP`](./Enums.md) | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 1 | `1` |

</details>


---


### Object: `SpawnOnBattleStart`


**Definition:** No definition provided.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 38 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](./Arrays.md#array-number) | Array / Integer || 29 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnTookDamage`


**Definition:** Event Trigger: Applies nested statuses when took damage.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 38 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 14 | `Default`<br>`FormChange`<br>`Druid` | [`StrengthUp`](./Enums.md) | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 4 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 3 | `-1`<br>`-2`<br>`1` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 3 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 3 | `-1`<br>`-2`<br>`-4` |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 3 | `{ . . . }` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 3 | `1`<br>`2`<br>`3` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  || 2 | `{ . . . }` |
| [`Craft`](./Passives_and_Statuses.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 2 | `{ . . . }` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`RandomStatUp`](./Enums.md) | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`TempDamageUp`](./Enums.md) | Integer | The amount of temporary damage increase applied. | 2 | `-1`<br>`1`<br>`2` |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 1 | `1`<br>`2`<br>`3` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`MovementUp`](./Enums.md) | Integer | The amount of movement increase or decrease applied. | 1 | `-2`<br>`1`<br>`2` |
| [`RandomInjury`](./Enums.md) | Integer | The number of random injuries applied. | 1 | `1` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [`TempMovement`](./Enums.md) | Integer | The amount of temporary movement range added, or a string alias like 'mov'. | 1 | `1`<br>`20`<br>`mov` |

</details>


---


### Object: `StatusEachTurnEnd`


**Definition:** Applies or references the 'StatusEachTurnEnd' effect/state.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 55 | `passives`<br>`class`<br>`tag` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 12 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`NonStackingDivineShield`](./Enums.md) | Integer | The number of Divine Shield stacks that do not stack with duplicates. | 6 | `1` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 5 | `-1`<br>`-2`<br>`-4` |
| [`EmptyMana`](./Enums.md) | Integer || 2 | `1` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`RangeUp`](./Enums.md) | Integer | The number of stacks of bonus attack range applied. | 2 | `1` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 1 | `1` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum  || 1 | `weapon` |

</details>


---


### Object: `lock_item_slot`


**Definition:** No definition provided.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 16 | `0`<br>`1`<br>`2` |
| `frame` | Integer | The sprite frame index to display. | 3 | `1`<br>`10`<br>`100` |

</details>


---


### Object: `StatusOnBattleEnd`


**Definition:** Applies the nested status effects when the encounter finishes.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 52 | `passives`<br>`class`<br>`tag` |
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 | `true` |
| [`RandomMutation`](./Enums.md) | Integer | The number of random mutations to apply. | 9 | `1`<br>`3` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 8 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`RandomPermanentStat`](./Enums.md) | Integer | The amount of a random permanent stat change (positive or negative). | 8 | `-1`<br>`-2`<br>`-3` |
| [`CureDisease`](./Passives_and_Statuses.md#object-curedisease) | Object  || 6 | `{ . . . }` |
| [`PermanentIntelligence`](./Enums.md) | Integer | The permanent amount of intelligence added or removed. | 3 | `-1`<br>`1`<br>`2` |
| [`NextBattleStatus`](./Passives_and_Statuses.md#object-nextbattlestatus) | Object  || 2 | `{ . . . }` |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution stat added or removed. | 2 | `-1`<br>`-2`<br>`1` |
| [`PermanentSpeed`](./Enums.md) | Integer | The permanent amount of speed added or removed. | 2 | `-1`<br>`1`<br>`2` |
| [`PermanentStrength`](./Enums.md) | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 1 | `1`<br>`2` |

</details>


---


### Object: `StatusOnKill`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 5 | `1`<br>`10`<br>`2` |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. | 3 | `BoneClub`<br>`Kidney` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object  || 2 | `{ . . . }` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the source. | 2 | `1` |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of movement points restored to the source. | 2 | `1` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [`RandomStatUp`](./Enums.md) | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Stealth`](./Enums.md) | Integer | The number of stealth stacks applied. | 1 | `1`<br>`2`<br>`[1 .1]` |
| [`TakeBonusTurnWithStatus`](./Passives_and_Statuses.md#object-takebonusturnwithstatus) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `StatusOnStanceSwitch`


**Definition:** Event Trigger: Applies nested statuses when stance switch.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#context-passiveifemptyneck), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 14 | `passives`<br>`class`<br>`tag` |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 6 | `1`<br>`10`<br>`2` |
| `NextBasicAttackCritsThisTurn` | `Number` | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. | 2 | `1` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 2 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`RandomStatUp`](./Enums.md) | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`PartialCleanse`](./Enums.md) | Integer | The number of stacks of temporary status effects to remove from the target. | 1 | `1`<br>`9999` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `SpreadDisease`


**Definition:** Provides a chance to transmit a disease status to adjacent targets.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#context-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#context-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum | Determines which disease is applied when spreading disease. | 13 | `BirdFlu`<br>`Cancer`<br>`CommonCold` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 12 | `.02`<br>`.1`<br>`.15` |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 6 | `true` |

</details>


---


### Object: `StatusEachTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to each turn begin.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 24 | `passives`<br>`class`<br>`tag` |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 5 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`FillMana`](./Enums.md) | Array / Integer | The amount of mana restored, or an [amount, probability] array. | 2 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`RandomStatUp`](./Enums.md) | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


### Object: `Conditional_Ally`


**Definition:** Conditional trigger: Executes nested logic if the target is friendly to the caster.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#context-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#context-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#context-statuskilledcharacters)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 28 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 5 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `-1`<br>`-2`<br>`1` |
| `Cleanse` | `Number` | The number of stacks of negative status effects removed from the target. | 3 | `0`<br>`1` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 2 | `{ . . . }` |
| `ClearNegativeEffects` | `Number` | The number of negative effects cleared from the target. | 2 | `1` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 2 | `{ . . . }` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`TempSpeedUp`](./Enums.md) | Integer | The number of stacks of temporary Speed Up applied to the unit. | 2 | `10`<br>`4`<br>`X` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `CritsApplyStatus`


**Definition:** Applies the 'CritsApplyStatus' effect.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 12 | `passives`<br>`class`<br>`tag` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  || 2 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 2 | `{ . . . }` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 2 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`Bleed`](./Enums.md) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `1`<br>`2`<br>`3` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |

</details>


---


### Object: `Temporary`


**Definition:** A wrapper object for applying status effects that automatically expire.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#context-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 57 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 56 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 52 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `expires_on_begin_turn` | Boolean | If true, the temporary effect expires at the start of the target's turn. | 25 | `true` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 21 | `true` |

</details>


---


### Object: `PassiveAtStatThreshold`


**Definition:** Applies the 'PassiveAtStatThreshold' effect.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 13 | `passives`<br>`class`<br>`tag` |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 13 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 13 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 13 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


### Object: `threshold`


**Definition:** Examples: `4*champion_multiplier, 3*champion_multiplier, 1`  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#context-passiveatstatthreshold)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`int`](./Enums.md#enum-int) | Enum / Integer  || 8 | `-1`<br>`-10`<br>`-2` |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 2 | `+1`<br>`-1`<br>`-2` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 2 | `-1`<br>`-10`<br>`-2` |

</details>


---


### Object: `RevengeDamage`


**Definition:** Reaction trigger: Deals damage to the attacker when hit.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 31 | `damage_instance`<br>`spell`<br>`false` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 29 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 29 | `Default`<br>`FormChange`<br>`Druid` | `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 3 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |

</details>


---


### Object: `MeleeRevengeDamage`


**Definition:** Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 70 | `damage_instance`<br>`spell`<br>`self_damage` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 49 | `Default`<br>`FormChange`<br>`Druid` | [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 47 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 43 | `passives`<br>`class`<br>`tag` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 22 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 10 | `[`<br>`[Heat Fire]` |
| [`Poison`](./Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 1 | `{ . . . }` |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PassiveIfAllArmorEmpty`


**Definition:** Applies the 'PassiveIfAllArmorEmpty' effect.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)`damage_instance`<br>`spell`<br>`self_damage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`AddSpellDamage`](./Enums.md) | Integer || 2 | `1`<br>`2` |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum  | Specifies the ability used when the unit counterattacks after being hit. | 2 | `BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| [`ExtraMovePoints`](./Enums.md) | Integer | The number of additional movement points granted to this unit. | 2 | `1` |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 2 | `-2`<br>`1`<br>`2` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object  || 2 | `{ . . . }` |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#object-critsapplystatus) | Object  || 1 | `{ . . . }` |
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 1 | `1` |

</details>


---


### Object: `RandomStatusFromPool`


**Definition:** Selects and applies a random status effect from the provided nested object.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 33 | `passives`<br>`class`<br>`tag` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 12 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 | `Default`<br>`FormChange`<br>`Druid` | [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 10 | `1`<br>`2`<br>`3` |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 9 | `1`<br>`2`<br>`4` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 9 | `1`<br>`2`<br>`3` |
| [`Poison`](./Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 9 | `1`<br>`10`<br>`2` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 8 | `1`<br>`10`<br>`2` |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 8 | `1`<br>`2`<br>`3` |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`2`<br>`3` |
| [`Slow`](./Enums.md) | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 7 | `-1`<br>`1`<br>`2` |
| [`Blind`](./Enums.md) | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 6 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 6 | `1`<br>`2`<br>`3` |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 6 | `1`<br>`2`<br>`3` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 5 | `-1`<br>`-2`<br>`1` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 5 | `1`<br>`10`<br>`2` |
| [`MoveQuivered`](./Enums.md) | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 5 | `1`<br>`2`<br>`[1, 0.1]` |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | `1`<br>`2`<br>`5` |
| [`BleedThorns`](./Enums.md) | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 4 | `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 4 | `-1`<br>`-2`<br>`1` |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 4 | `1`<br>`2`<br>`3` |
| [`MagicWeakness`](./Enums.md) | Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 4 | `1`<br>`2`<br>`3` |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`3`<br>`5` |
| [`Reflect`](./Enums.md) | Integer | The amount of reflect stacks applied. | 4 | `1`<br>`5` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 4 | `-1`<br>`-2`<br>`-4` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`2`<br>`3` |
| [`Tarred`](./Enums.md) | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 4 | `1`<br>`2`<br>`[1 .1]` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 3 | `1`<br>`2`<br>`3` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`[1 .01]` |
| [`Immobile`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 3 | `0`<br>`1`<br>`10%` |
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`Sleep`](./Enums.md) | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`3` |
| [`StatusGroup`](./Passives_and_Statuses.md#object-statusgroup) | Object  | A container grouping multiple status effects to be applied simultaneously. | 3 | `{ . . . }` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 3 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 1 | `1`<br>`[1 .5]` |

</details>


---


### Object: `StatusOnCrit`


**Definition:** Event Trigger: Applies nested statuses when crit.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 3 | `-1`<br>`-2`<br>`-4` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 1 | `1`<br>`10`<br>`100` |
| [`RandomStatUp`](./Enums.md) | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `Conditional_Enemy`


**Definition:** Conditional trigger: Executes nested logic if the target is hostile to the caster.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#context-conditional_notboss)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 34 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 | `Default`<br>`FormChange`<br>`Druid` | [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 9 | `1`<br>`10`<br>`2` |
| [`Conditional_PartyMember`](./Passives_and_Statuses.md#object-conditional_partymember) | Object  || 2 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 2 | `{ . . . }` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 2 | `{ . . . }` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `DamageNeighborsOnEndMove`


**Definition:** Combat Trigger: Deals damage to neighbors on end move.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 7 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 7 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 7 | `damage_instance`<br>`spell`<br>`false` |
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 6 | `true` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 6 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |

</details>


---


### Object: `ForceUseAbility`


**Definition:** No definition provided.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin), [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A probability (decimal or percentage) for a form change or other effect to occur. | 3 | `.02`<br>`.1`<br>`.15` |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


---


### Object: `PassiveIfEmptyFace`


**Definition:** Applies the 'PassiveIfEmptyFace' effect.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | `passives`<br>`class`<br>`tag` |
| [`AddCritMultiplier`](./Enums.md) | Integer || 2 | `100%`<br>`125%`<br>`150%` |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `1`<br>`10`<br>`100` |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | `10%`<br>`15%`<br>`2%` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object  || 2 | `{ . . . }` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PassiveIfEmptyHead`


**Definition:** Applies the 'PassiveIfEmptyHead' effect.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | `passives`<br>`class`<br>`tag` |
| [`AddCritMultiplier`](./Enums.md) | Integer || 2 | `100%`<br>`125%`<br>`150%` |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `1`<br>`10`<br>`100` |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | `10%`<br>`15%`<br>`2%` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object  || 2 | `{ . . . }` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PassiveIfEmptyNeck`


**Definition:** Applies the 'PassiveIfEmptyNeck' effect.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | `passives`<br>`class`<br>`tag` |
| [`AddCritMultiplier`](./Enums.md) | Integer || 2 | `100%`<br>`125%`<br>`150%` |
| [`CritChanceUp`](./Enums.md) | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `1`<br>`10`<br>`100` |
| [`DodgeChance`](./Enums.md) | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | `10%`<br>`15%`<br>`2%` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object  || 2 | `{ . . . }` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusAlliesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies on death.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | `triggers_limit` | Number || 2 | `1` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`HealAndOverhealToShield`](./Enums.md) | Integer || 2 | `12`<br>`20` |
| [`Reanimate`](./Enums.md) | Integer | The percentage chance to reanimate the target. | 2 | `100%`<br>`33%`<br>`50%` |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 2 | `1` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| [`FullHeal`](./Enums.md) | Integer | If non-zero, fully restores the target's health. | 1 | `0`<br>`1` |

</details>


---


### Object: `StatusOnUseAbilityWithTag`


**Definition:** Event Trigger: Applies nested statuses when use ability with tag.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 7 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | `passives`<br>`class`<br>`tag` |
| [`RefreshActPoints`](./Enums.md) | Integer | The amount of action points restored to the source. | 3 | `1` |
| `exclude_basicattack` | Boolean || 2 | `true` |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object  || 2 | `{ . . . }` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [`RandomStatUp`](./Enums.md) | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |

</details>


---


### Object: `AddStatusToElementAbilities`


**Definition:** Applies the 'AddStatusToElementAbilities' effect.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 6 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 2 | `{ . . . }`<br>`BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  || 2 | `{ . . . }` |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object  || 2 | `{ . . . }` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AddStatusToWeapons`


**Definition:** Applies the 'AddStatusToWeapons' effect.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`PullSourceToKnockbackImmuneTarget`](./Enums.md) | Integer | The amount of pull force applied to the source toward a knockback-immune target. | 2 | `1` |
| [`Cleave`](./Enums.md) | Integer | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 1 | `1` |
| [`LeechPercent`](./Enums.md) | Integer || 1 | `50` |

</details>


---


### Object: `CureDisease`


**Definition:** Applies the 'CureDisease' effect.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 6 | `.02`<br>`.1`<br>`.15` |
| [`disease`](./Enums.md#enum-disease) | Enum | Determines which disease is applied when spreading disease. | 6 | `BirdFlu`<br>`Cancer`<br>`CommonCold` |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 1 | `true` |

</details>


---


### Object: `Else`


**Definition:** Fallback object that executes if the preceding `Conditional_` block evaluated to false.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 66 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 23 | `Default`<br>`FormChange`<br>`Druid` |
| `CaptureFamiliar` | `Number` | The number of times to attempt to capture the target as a familiar. | 2 | `1` |
| `FactionConversion` | `Number` | Converts the target to the caster's faction. | 2 | `1` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`Marked`](./Enums.md) | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`3`<br>`5` |
| [`PermanentCharm`](./Enums.md) | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | `1` |
| [`TempSpeedUp`](./Enums.md) | Integer | The number of stacks of temporary Speed Up applied to the unit. | 1 | `10`<br>`4`<br>`X` |

</details>


---


### Object: `keyword_tooltips`


**Definition:** Forces specific UI tooltips to appear when hovering over the ability.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 16 | `passives`<br>`class`<br>`tag` |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `ManaCostReductionTagged`


**Definition:** Applies the 'ManaCostReductionTagged' effect.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer || 6 | `1`<br>`2`<br>`3` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 6 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |

</details>


---


### Object: `SpawnEachTurn`


**Definition:** Applies or references the 'SpawnEachTurn' effect/state.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 22 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`chance`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A probability (decimal or percentage) for a form change or other effect to occur. | 20 | `.02`<br>`.1`<br>`.15` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 2 | `false`<br>`true` |
| [`number`](./Arrays.md#array-number) | Array / Integer  || 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `SpawnThingOnDamage`


**Definition:** Applies or references the 'SpawnThingOnDamage' effect/state.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 38 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 20 | `false`<br>`true` |
| `spawn_on_death_hit` | Boolean | If true, spawning only occurs when the damage is lethal. | 10 | `false` |
| `consider_all_layers` | Boolean | If true, considers all map layers when determining the spawn location. | 2 | `true` |

</details>


---


### Object: `AddStatusToAllDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToBasicMeleeAttack`


**Definition:** Examples: `{ ... }`  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | `passives`<br>`class`<br>`tag` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | `1`<br>`2`<br>`3` |
| [`FaceAway`](./Enums.md) | Integer | If set, forces the target to face away from the source. | 2 | `1` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 1 | `{ . . . }` |

</details>


---


### Object: `StatusOnCastSpell`


**Definition:** Event Trigger: Applies nested statuses when cast spell.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 4 | `1`<br>`2`<br>`3` |
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer || 2 | `1`<br>`3`<br>`5` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnOverHealed`


**Definition:** Event Trigger: Applies nested statuses when over healed.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` | [`ForceUseAbility_NonStack`](./Enums.md) | Enum || 2 | `Endeavor_Auto`<br>`Indigestion_Fart`<br>`Indigestion_Fart2` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 2 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `SpawnScaledRotFly` | Number | The number of scaled Rot Flies to spawn when over-healed. | 1 | `0`<br>`1` |
| [`CurrentWeaponDamageUp`](./Enums.md) | Integer || 1 | `1`<br>`3`<br>`5` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `AddDamageToElementDamage`


**Definition:** Applies or references the 'AddDamageToElementDamage' effect/state.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 9 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 9 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `AddPassivesToCharmed`


**Definition:** Applies the 'AddPassivesToCharmed' effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 3 | `{ . . . }` |
| [`AddMaxHealth`](./Enums.md) | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 2 | `-25`<br>`10`<br>`2` |
| [`AddSpeed`](./Enums.md) | Integer | The amount of speed added (or subtracted) to the unit. | 2 | `-3`<br>`4`<br>`6` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |

</details>


---


### Object: `AddStatusToElementDamage`


**Definition:** Applies the 'AddStatusToElementDamage' effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 6 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | `passives`<br>`class`<br>`tag` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 3 | `1`<br>`10`<br>`2` |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object  || 2 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddStatusToExplosions`


**Definition:** Applies the 'AddStatusToExplosions' effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddElement`](./Enums.md#enum-addelement) | Enum | Specifies the element to add to explosions. | 4 | `Fire`<br>`Napalm` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 4 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AllyBonusAbilityAura`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `square` | Boolean || 2 | `true` |

</details>


---


### Object: `AllyManaRegenAura`


**Definition:** Applies the 'AllyManaRegenAura' effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 4 | `1`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `AmplifyStatus`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `addstacks` | Number || 3 | `2` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 3 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


### Object: `AutocastEachRound`


**Definition:** Forces the character to automatically cast a specific ability at the start of each combat round.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 9 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 6 | `true` |
| `force_display_name` | Boolean | If true, forces the display name to show for the ability. | 2 | `true` |

</details>


---


### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#context-statusonuseabilitywithtag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 2 | `1` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [`FillMana`](./Arrays.md#array-fillmana) | Array / Integer  | The amount of mana restored, or an [amount, probability] array. | 1 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| [`ManaGain`](./Enums.md) | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


### Object: `DistanceBonusDamage`


**Definition:** Applies the 'DistanceBonusDamage' effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_range` | Integer | The minimum range of the ability. | 4 | `0`<br>`1`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `EMP`


**Definition:** Applies the 'EMP' effect.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](./Passives_and_Statuses.md#object-spell_graphics_override) | Object  || 4 | `{ . . . }` |
| [`status_explosion_override`](./Enums.md#enum-status_explosion_override) | Enum || 4 | `WaterConduct` |

</details>


---


### Object: `empty_armor_scaled_stats`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cha`](./Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 1 | `+1`<br>`-1`<br>`-2` |
| [`int`](./Enums.md#enum-int) | Enum / Integer  || 1 | `-1`<br>`-10`<br>`-2` |
| [`spd`](./Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 1 | `-1`<br>`-10`<br>`-2` |

</details>


---


### Object: `PassiveAtHealthThreshold`


**Definition:** Applies or references the 'PassiveAtHealthThreshold' effect/state.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 9 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | `passives`<br>`class`<br>`tag` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 9 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 9 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


### Object: `PassiveWhenAffectedByElement`


**Definition:** Examples: `{ ... }`  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 18 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 18 | `passives`<br>`class`<br>`tag` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 18 | `{ . . . }` |

</details>


---


### Object: `PassiveWhenAtFullMana`


**Definition:** State Trigger: Grants nested passives when at full mana.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 2 | `{ . . . }` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `1`<br>`10`<br>`2` |
| [`Flying`](./Enums.md) | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | `1` |
| [`AddMovement`](./Enums.md) | Integer | The amount of bonus movement points added to the unit's base movement. | 1 | `-1`<br>`-2`<br>`1` |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum  | Specifies an alternative movement ability that replaces the unit's default move. | 1 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |

</details>


---


### Object: `spell_graphics_override`


**Definition:** No definition provided.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#context-emp)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`area_particle`](./Enums.md#enum-area_particle) | Enum || 4 | `Bolt`<br>`BurnTrigger`<br>`Earthquake` |
| [`center_particle`](./Enums.md#enum-center_particle) | Enum || 4 | `BigMagicMissileBlast`<br>`Explosion`<br>`FireBlastMushroom` |
| [`palette`](./Enums.md#enum-palette) | Enum / Integer  | Specifies the color palette index for the ability's visuals. | 4 | `-1`<br>`0`<br>`1` |
| [`particle`](./Enums.md#enum-particle) | Enum | Specifies the particle effect displayed. | 4 | `ArrowFromAbove`<br>`BigMagicMissileBlast`<br>`Bolt` |

</details>


---


### Object: `StatusAlliesOnKill`


**Definition:** Event Trigger: Applies nested statuses to allies on kill.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#context-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusIfUnusedMovePoints`


**Definition:** Event Trigger: Applies nested statuses to if unused move points.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 4 | `1`<br>`10`<br>`2` |
| [`ManaGain`](./Enums.md) | Equation | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`MoveQuivered`](./Enums.md) | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`[1, 0.1]` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| [`ConstitutionUp`](./Enums.md) | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnTurnEndIfCastNSpells`


**Definition:** Event Trigger: Applies nested statuses when turn end if cast n spells.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spells`](./Arrays.md#array-spells) | Array  | The list of spell ability IDs the unit possesses. | 5 | `1`<br>`2`<br>`5` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`DoubleCastSpell`](./Enums.md) | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. | 3 | `1`<br>`2` |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| [`MoveQuivered`](./Enums.md) | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`[1, 0.1]` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `StatusOnTurnEndIfManaExact`


**Definition:** Event Trigger: Applies nested statuses when turn end if mana exact.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation || 4 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` |
| [`FreeSpell`](./Enums.md) | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 2 | `1`<br>`2` |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| [`MoveQuivered`](./Enums.md) | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`[1, 0.1]` |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | `1`<br>`3` |

</details>


---


### Object: `StatusOnTurnEndIfManaOrHealthExact`


**Definition:** Event Trigger: Applies nested statuses when turn end if mana or health exact.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation || 4 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | `1`<br>`3` |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 2 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `AbilityReaction`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 10 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 7 | `true` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `AddSelfStatusToBasicAttack`


**Definition:** Applies or references the 'AddSelfStatusToBasicAttack' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 11 | `passives`<br>`class`<br>`tag` |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 7 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** Applies the 'AddTemporaryEffectsToBasicAttack' effect.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 4 | `10`<br>`55`<br>`75` |
| `CastAgain` | Integer / String | The number of additional times the ability can be cast this turn. | 2 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `Conditional_BadRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized bad outcome probability.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`odds`](./Enums.md#enum-odds) | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 8 | `.1`<br>`.16666666`<br>`.3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 5 | `{ . . . }` |

</details>


---


### Object: `Conditional_HasStatus`


**Definition:** Conditional trigger: Executes nested logic if the target currently has the specified status effect.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#context-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 20 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 20 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `DeathRattle`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `pop_corpse` | Boolean | If true, the corpse is destroyed instead of left behind on death. | 11 | `false` |

</details>


---


### Object: `ElementalManaCostReduction`


**Definition:** Applies the 'ElementalManaCostReduction' effect.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer || 5 | `1`<br>`2`<br>`3` |
| [`element`](./Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 5 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `FindItemFromPool`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`chance`](./Enums.md#enum-chance) | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 3 | `.02`<br>`.1`<br>`.15` |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 2 | `2`<br>`3`<br>`4` |

</details>


---


### Object: `MoveTowardsDamageSource`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 5 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| `move_far` | Boolean | If true, the unit moves the maximum distance towards the damage source. | 4 | `false` |

</details>


---


### Object: `ObjectOnHitCharacter`


**Definition:** No definition provided.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#context-statuseachturnendperenemykill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `ObjectOnHitCharacter` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 7 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 5 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `SpawnCatCopyOnBattleStart`


**Definition:** Applies the 'SpawnCatCopyOnBattleStart' effect.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 4 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum | A tag that prevents chaining of spawns from the same source. | 4 | `ancestorset_shade`<br>`eb_twin`<br>`minime_clone` |

</details>


---


### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 11 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](./Arrays.md#array-number) | Array / Integer || 10 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `statuses`


**Definition:** Status effects possessed by the character.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#context-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#context-statusonbattleendifkillthresholdmet)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 12 | `passives`<br>`class`<br>`tag` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `-1`<br>`-2`<br>`1` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 2 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`PermanentDexterity`](./Enums.md) | Integer | The permanent amount of dexterity added or removed. | 2 | `1`<br>`2` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusEveryXSpellCasts`


**Definition:** Applies or references the 'StatusEveryXSpellCasts' effect/state.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | `1`<br>`3` |
| [`ReduceManaCost`](./Enums.md) | Integer | The number of stacks reducing mana cost of abilities. | 1 | `1`<br>`2` |
| [`RepairWeapon`](./Enums.md) | Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | `1`<br>`6`<br>`99` |
| [`RepairWeaponCondition`](./Enums.md) | Integer | The amount of weapon condition restored. | 1 | `1` |

</details>


---


### Object: `StatusGroup`


**Definition:** Groups multiple status effects together for batch application.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#context-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | `passives`<br>`class`<br>`tag` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [`DexterityUp`](./Enums.md) | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |
| [`SpawnCoinAnywhere`](./Enums.md) | Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 1 | `1`<br>`[1 .5]` |

</details>


---


### Object: `StatusKilledCharacters`


**Definition:** Event Trigger: Applies nested statuses to killed characters.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnAllyCatDeath`


**Definition:** Event Trigger: Applies nested statuses when ally cat death.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 6 | `passives`<br>`class`<br>`tag` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`FillMana`](./Arrays.md#array-fillmana) | Array / Integer  | The amount of mana restored, or an [amount, probability] array. | 1 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [`PercentHeal`](./Enums.md) | Integer || 1 | `50` |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 1 | `1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnBattleStart`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 7 | `Default`<br>`FormChange`<br>`Druid` | [`FullHeal`](./Enums.md) | Integer | If non-zero, fully restores the target's health. | 2 | `0`<br>`1` |
| [`Sleep`](./Enums.md) | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusOnEatFood`


**Definition:** Event Trigger: Applies nested statuses when eat food.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 2 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 1 | `0`<br>`1` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`RandomStatUp`](./Enums.md) | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |

</details>


---


### Object: `StatusOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses when gain coins.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 2 | `{ . . . }` |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnHealed`


**Definition:** Event Trigger: Applies nested statuses when healed.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnKillEnemy`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 11 | `passives`<br>`class`<br>`tag` |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| [`ManaGain`](./Enums.md) | Equation | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of movement points restored to the source. | 1 | `1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnTookDamageFromAbility`


**Definition:** Event Trigger: Applies statuses when taking damage from an ability.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 8 | `passives`<br>`class`<br>`tag` |
| [`DiminishingHealthRegen`](./Enums.md) | Integer | The number of diminishing health regen stacks applied. | 2 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`Shield`](./Enums.md) | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** AI Trigger: Executes an ability when a character with a specific tag moves adjacent.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`range`](./Engine_Uncategorized_Resources.md#valid-property-keys) | Variable | The distance in tiles for the trigger effect; `global` means any distance. | 5 | `1`<br>`10`<br>`2` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 5 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |

</details>


---


### Object: `AddPassivesToSummonAbilityMinions`


**Definition:** Applies the 'AddPassivesToSummonAbilityMinions' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Doomed`](./Enums.md) | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 2 | `1`<br>`2`<br>`3` |
| [`MovementUp`](./Enums.md) | Integer | The amount of movement increase or decrease applied. | 2 | `-2`<br>`1`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddPassiveToSpawnedRocks`


**Definition:** Applies the 'AddPassiveToSpawnedRocks' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | The amount of filled max health added to spawned rocks. | 2 | `3`<br>`7` |
| `JoinSpawnerFaction` | Number | The faction ID that spawned rocks should join. | 2 | `1` |

</details>


---


### Object: `AddSelfStatusToWeapons`


**Definition:** Applies the 'AddSelfStatusToWeapons' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToAllDamageAbilities`


**Definition:** Applies the 'AddStatusToAllDamageAbilities' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| [`Piercing`](./Enums.md) | Integer || 1 | `1` |
| [`Weakness`](./Enums.md) | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `AddStatusToBasicAttackWithCooldown`


**Definition:** Applies the 'AddStatusToBasicAttackWithCooldown' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | `Number` | If non-zero, forces the charmed target to use its basic attack on a random nearby unit. | 2 | `1` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `AddStatusToFirstBasicAttack`


**Definition:** Applies the 'AddStatusToFirstBasicAttack' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToMeleeDamage`


**Definition:** Applies the 'AddStatusToMeleeDamage' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DelayedWind`](./Passives_and_Statuses.md#object-delayedwind) | Object  | Defines the properties for a delayed wind effect applied on melee damage. | 1 | `{ . . . }` |
| [`DelayedWindCone`](./Passives_and_Statuses.md#object-delayedwindcone) | Object  || 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddStatusToTrampleDamage`


**Definition:** Applies the 'AddStatusToTrampleDamage' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AllyHealthRegenAura`


**Definition:** Applies the 'AllyHealthRegenAura' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `1`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `AlternateCraftingPools`


**Definition:** Applies the 'AlternateCraftingPools' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tinkerer_0`](./Enums.md#enum-tinkerer_0) | Enum || 2 | `tinkerer_0_bombs` |
| [`tinkerer_1`](./Enums.md#enum-tinkerer_1) | Enum || 2 | `tinkerer_1_bombs` |

</details>


---


### Object: `ApplyStatusesToRandomEnemiesEachTurn`


**Definition:** Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` |
| [`Bounty`](./Enums.md) | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 3 | `1`<br>`3` |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 2 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `ApplyStatusIfCrit`


**Definition:** Conditional trigger: Executes the nested logic only if the triggering action was a critical hit.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `Key`<br>`passives`<br>`class` |
| [`Purge`](./Enums.md) | Integer | The number of status effects to purge from the target. | 2 | `0`<br>`3` |

</details>


---


### Object: `ApplyToSource`


**Definition:** Redirects the nested effects to apply to the caster/source of the ability instead of the target.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#context-conditional_ally)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 43 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 20 | `Default`<br>`FormChange`<br>`Druid` | [`AllStatsUp`](./Enums.md) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 6 | `-1`<br>`-2`<br>`1` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 5 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


### Object: `AutocastEachTurnBegin`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `advantage_polarity` | Number || 1 | `-1` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `BoobyTrapItems`


**Definition:** Applies the 'BoobyTrapItems' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`on_break`](./Passives_and_Statuses.md#object-on_break) | Object  || 2 | `{ . . . }` |
| [`on_throw`](./Passives_and_Statuses.md#object-on_throw) | Object  || 2 | `{ . . . }` |

</details>


---


### Object: `BoostWeaponDamage`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 4 | `-999999`<br>`.05*X`<br>`.25` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 4 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 4 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


### Object: `BouncyProjectiles`


**Definition:** Applies the 'BouncyProjectiles' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_bounces` | Integer || 3 | `-1`<br>`1`<br>`10` |
| [`max_range`](./Enums.md#enum-max_range) | Enum / Integer   || 3 | `"4+(1-clamp(spd,0,1))*2"`<br>`"max(5-int, 1)"`<br>`-1` |

</details>


---


### Object: `CatAPultAnimation`


**Definition:** Applies the 'CatAPultAnimation' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`animation`](./Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |

</details>


---


### Object: `CatchProjectiles`


**Definition:** Applies or references the 'CatchProjectiles' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_chance` | Integer || 5 | `100%`<br>`15%` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 5 | `.02`<br>`.1`<br>`.15` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 5 | `1`<br>`2`<br>`5` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `ChanceToBackflip`


**Definition:** Applies or references the 'ChanceToBackflip' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 6 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 6 | `.02`<br>`.1`<br>`.15` |

</details>

---`damage_instance`<br>`spell`<br>`self_damage`


### Object: `ChangeTile`


**Definition:** Transforms the terrain tile under the target.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](./Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 12 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| `aoe` | Integer | The radius (in tiles) of the area affected by the tile change. | 2 | `1` |

</details>


---


### Object: `ClassManaCostReduction`


**Definition:** Applies or references the 'ClassManaCostReduction' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer || 7 | `1`<br>`2`<br>`3` |
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 6 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |

</details>


---


### Object: `Conditional_Adjacent`


**Definition:** Conditional object: Executes nested logic only if the target is/has Adjacent.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`10`<br>`2` |
| [`BonusCritChance`](./Enums.md) | Integer | The flat percentage increase to critical hit chance. | 2 | `100`<br>`25`<br>`50` |
| [`BonusDamage`](./Enums.md) | Equation | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag`

</details>


---


### Object: `Conditional_Boss`


**Definition:** Conditional trigger: Executes nested logic if the target is a Boss.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 19 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | [`Stun`](./Enums.md) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `Conditional_Corpse`


**Definition:** Conditional trigger: Executes nested logic if the target is a dead body/corpse.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#context-addstatustoelementdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 10 | `passives`<br>`class`<br>`tag` |
| `Revive` | `Number` | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 7 | `1`<br>`100%`<br>`50%` |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 2 | `-10`<br>`0`<br>`1` |
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 2 | `1` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| [`SafeDoomed`](./Enums.md) | Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 2 | `1`<br>`2`<br>`level` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` |
| [`DamageUp`](./Enums.md) | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `Conditional_HasTag`


**Definition:** Conditional trigger: Executes nested logic if the target possesses the specified entity tag.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 46 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 46 | `passives`<br>`class`<br>`tag` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 11 | `Default`<br>`FormChange`<br>`Druid` |
| `FlatLeechIfDamaged` | `Number` | The flat amount of health leeched when the unit takes damage. | 1 | `3`<br>`5` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `Conditional_NotBoss`


**Definition:** Conditional trigger: Executes nested logic if the target is NOT a Boss.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#context-statuskillers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `Conditional_NotBoss` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `Conditional_PartyMember`


**Definition:** Conditional constraint. Nested properties only trigger if this is true.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#context-conditional_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `Conditional_PartyMember` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `Conditional_Shielded`


**Definition:** Conditional trigger: Executes nested logic if the target currently has a Shield status.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` | `BonusCritChance` | `Number` | The flat percentage increase to critical hit chance. | 2 | `100`<br>`25`<br>`50` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `Craft`


**Definition:** Synthesizes or spawns a new item from a specific pool.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#context-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 15 | `2`<br>`3`<br>`4` |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 14 | `0`<br>`1`<br>`2` |

</details>


---


### Object: `DamageNeighborsAfterMove`


**Definition:** Examples: `{ ... }`  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 4 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 4 | `{ . . . }` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 4 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 4 | `damage_instance`<br>`spell`<br>`false` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 4 | `[`<br>`[Heat Fire]` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `DamageNeighborTilesWhenCastSpell`


**Definition:** Combat Trigger: Deals damage to neighbor tiles when cast spell.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`fire`](./Passives_and_Statuses.md#object-fire) | Object  || 1 | `{ . . . }` |
| [`ice`](./Passives_and_Statuses.md#object-ice) | Object  || 1 | `{ . . . }` |
| [`lightning`](./Passives_and_Statuses.md#object-lightning) | Object  || 1 | `{ . . . }` |
| [`triattack`](./Passives_and_Statuses.md#object-triattack) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `DamageReductionAura`


**Definition:** Combat Trigger: Deals damage to reduction aura.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 2 | `false`<br>`true` |
| [`range`](./Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `1`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `Earth`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Math_Equations.md) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |

</details>


---


### Object: `Electric`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `ElementalAttunement`


**Definition:** Applies the 'ElementalAttunement' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |`damage_instance`<br>`spell`<br>`self_damage`
| :--- | :--- | :--- | :--- | :--- |
| [`Earth`](./Passives_and_Statuses.md#object-earth) | Object  | Defines the Earth element effects, including damage value. | 2 | `{ . . . }` |
| [`Electric`](./Passives_and_Statuses.md#object-electric) | Object  | Applies a Stun status effect with specified stacks and probability based on variable X. | 2 | `{ . . . }` |
| [`Fire`](./Passives_and_Statuses.md#object-fire) | Integer / Object  | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 2 | `{ . . . }`<br>`1` |
| [`Grass`](./Passives_and_Statuses.md#object-grass) | Object  | Specifies the status effects applied to allies standing on grass tiles. | 2 | `{ . . . }` |
| [`Gravity`](./Passives_and_Statuses.md#object-gravity) | Object  | An object defining the effects granted by Gravity elemental attunement. | 2 | `{ . . . }` |
| [`Holy`](./Passives_and_Statuses.md#object-holy) | Enum / Object  | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 2 | `{ . . . }`<br>`MegaGuppy_TransformHoly` |
| [`Ice`](./Passives_and_Statuses.md#object-ice) | Object  | Applies the Slow status effect to targets hit by ice-element abilities. | 2 | `{ . . . }` |
| [`Shadow`](./Passives_and_Statuses.md#object-shadow) | Object  | An object defining the effects granted by Shadow elemental attunement. | 2 | `{ . . . }` |
| [`Water`](./Passives_and_Statuses.md#object-water) | Object  | Form state for water element, applying a puddle or movement bonus. | 2 | `{ . . . }` |
| [`Wind`](./Passives_and_Statuses.md#object-wind) | Object  | Defines the properties for the Wind element, such as knockback amount. | 2 | `{ . . . }` |

</details>


---


### Object: `EscapeSequence`


**Definition:** Applies the 'EscapeSequence' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | `Number` | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. | 2 | `20` |
| `SafeExplosionIfHitSomething` | Number | The radius of a safe explosion that only occurs if it hits an obstacle or entity. | 2 | `10`<br>`5` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `Eternal`


**Definition:** Applies the 'Eternal' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health_percent` | Integer || 3 | `100%`<br>`50%` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [`TakeExtraTurn`](./Enums.md) | Integer | The number of extra turns granted to the source. | 1 | `1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `ExtraStatusWhenDealingDamage`


**Definition:** Applies or references the 'ExtraStatusWhenDealingDamage' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Grass`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`Poison`](./Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Gravity`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `GravityWell`


**Definition:** Applies the 'GravityWell' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |
| [`cant_miss`](./Enums.md) | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 2 | `true` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [{Damaging Keys}](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2 | `Key`<br>`damage_instance`<br>`spell`

</details>


---


### Object: `HealAlliesEachTurn`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean || 2 | `false` |
| `mana` | Equation || 2 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `Holy`


**Definition:** Character Form: Behavior and stats for the \'Holy\' state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` |
| [`FlatLeech`](./Enums.md) | Enum | The flat amount of health restored to the source when dealing damage, applied after the hit. | 2 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `HolyDamageBlessing`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#context-passiveuntilgetkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage_multiplier` | Number || 2 | `2`<br>`3` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Ice`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `InfiniteRebirth`


**Definition:** Applies the 'InfiniteRebirth' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 3 | `0`<br>`1`<br>`10` |
| `playercat_health` | Integer | The percentage of maximum health the player cat must have to trigger the rebirth. | 3 | `100%`<br>`25%` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` |
| [`TempSpeedUp`](./Enums.md) | Integer | The number of stacks of temporary Speed Up applied to the unit. | 2 | `10`<br>`4`<br>`X` |

</details>


---


### Object: `LateBloomer`


**Definition:** Applies the 'LateBloomer' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `LightningRod`


**Definition:** Applies the 'LightningRod' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Tech`](./Enums.md) | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` |

</details>


---


### Object: `LowHealthAllyDodgeChanceAura`


**Definition:** Applies the 'LowHealthAllyDodgeChanceAura' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `theshold` | Number || 2 | `5` |

</details>


---


### Object: `MovementReaction`


**Definition:** Reaction: Triggers an effect or ability when forced to move.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 11 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 7 | `false`<br>`true` |

</details>


---


### Object: `NextBattleStatus`


**Definition:** Applies the 'NextBattleStatus' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#context-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `on_break`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | The radius of a safe explosion that only occurs if it hits an obstacle or entity. | 2 | `10`<br>`5` |

</details>


---


### Object: `on_throw`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#context-boobytrapitems)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HitExplosion` | `Number` | The radius of the explosion triggered on hit. | 2 | `10`<br>`5`<br>`X` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `PassiveAfterXKills`


**Definition:** Applies or references the 'PassiveAfterXKills' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |

</details>


---


### Object: `PassiveAtFullHealth`


**Definition:** Applies the 'PassiveAtFullHealth' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TakeExtraDamage` | Number | The percentage of extra damage taken while at full health. | 2 | `200%` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`ManaCostReduction`](./Enums.md) | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 2 | `-2`<br>`1`<br>`2` |

</details>


---


### Object: `PassiveAtInjuryThreshold`


**Definition:** Applies the 'PassiveAtInjuryThreshold' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `bleeding`<br>`burned`<br>`cha` |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 2 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


### Object: `PassiveGroup`


**Definition:** Passive: A collection of passives grouped together for easier management.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#context-randompassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 14 | `passives`<br>`class`<br>`tag` |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum  | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. | 2 | `happy`<br>`insane`<br>`sad` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [`CharismaUp`](./Enums.md) | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 1 | `-1`<br>`-2`<br>`1` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `PassiveUntilCastSpell`


**Definition:** Applies the 'PassiveUntilCastSpell' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HealAlliesEachTurn`](./Passives_and_Statuses.md#object-healallieseachturn) | Object  | An object defining how much health and mana are healed to all allies each turn. | 2 | `{ . . . }` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`StatusAlliesEachTurn`](./Passives_and_Statuses.md#object-statusallieseachturn) | Object  || 1 | `{ . . . }` |

</details>


---


### Object: `PassiveUntilGetKill`


**Definition:** Applies the 'PassiveUntilGetKill' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](./Passives_and_Statuses.md#object-holydamageblessing) | Object  | An object defining the damage multiplier and status effects applied as a holy damage blessing. | 2 | `{ . . . }` |

</details>


---


### Object: `PassiveWhenTheAlpha`


**Definition:** State Trigger: Grants nested passives when the alpha.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | The number of extra turns granted at the end of each round while the unit is the alpha. | 2 | `1` |

</details>


---


### Object: `PassiveWhileInMonkMeleeStance`


**Definition:** Applies the 'PassiveWhileInMonkMeleeStance' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| [`Brace`](./Enums.md) | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 3 | `1`<br>`10`<br>`2` |
| [`HealthRegenUp`](./Enums.md) | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PassiveWhileInMonkRangedStance`


**Definition:** Applies the 'PassiveWhileInMonkRangedStance' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 2 | `1`<br>`10`<br>`2` |
| [`AddSpellDamage`](./Enums.md) | Integer || 2 | `1`<br>`2` |
| [`KineticSpikes`](./Enums.md) | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PassiveWhilePreviewingMonkRangedStance`


**Definition:** Applies the 'PassiveWhilePreviewingMonkRangedStance' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`AddBonusRange`](./Enums.md) | Integer | The number of additional tiles of range added to the unit's abilities. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `PassiveWhileWearingMetal`


**Definition:** Applies the 'PassiveWhileWearingMetal' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](./Enums.md#enum-addelementstoweapon) | Enum | Specifies the element to add to the unit's attacks while wearing metal equipment. | 2 | `Electric` |

</details>


---


### Object: `RepressedMemoriesMetronome`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#context-scaledstatusonspendmana)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 2 | `2`<br>`3`<br>`4` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `ScaledStatusOnOverMana`


**Definition:** Applies the 'ScaledStatusOnOverMana' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 2 | `1`<br>`10`<br>`2` |
| [`Cleanse`](./Enums.md) | Integer | The number of stacks of negative status effects removed from the target. | 1 | `0`<br>`1` |

</details>


---


### Object: `ScaledStatusOnSpendMana`


**Definition:** Applies the 'ScaledStatusOnSpendMana' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#object-repressedmemoriesmetronome) | Object  | An object defining the metronome status effect and its pool triggered on mana spend. | 2 | `{ . . . }` |

</details>


---


### Object: `schadenfreude_scaled_stats`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](./Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 1 | `-1`<br>`-2`<br>`-3` |
| [`str`](./Enums.md#enum-str) | Enum / Integer  || 1 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `SecurityBotProtect`


**Definition:** AI Logic: Guarding behavior for Security Bot units.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move`](./Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 5 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |

</details>


---


### Object: `Shadow`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`crit_chance`](./Engine_DamagingKeys.md#valid-property-keys) | `String` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 2 | `-999999`<br>`.05*X`<br>`.25` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


### Object: `SmiteEnemiesWhoKill`


**Definition:** Applies the 'SmiteEnemiesWhoKill' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 2 | `damage_instance`<br>`spell`<br>`false` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `SpecialFriends`


**Definition:** Applies the 'SpecialFriends' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatsAtLowHealth`


**Definition:** Applies the 'StatsAtLowHealth' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`speed`](./Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 1 | `-30`<br>`-4`<br>`.5` |
| `strength` | Integer | The base strength stat, used for physical damage calculations. | 1 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `StatusAfterCastSpell`


**Definition:** Applies or references the 'StatusAfterCastSpell' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | [`TempSpellDamageUp`](./Enums.md) | Integer | The amount of temporary spell damage increase applied. | 2 | `1` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`TempDamageUp`](./Enums.md) | Integer | The amount of temporary damage increase applied. | 1 | `-1`<br>`1`<br>`2` |

</details>


---


### Object: `StatusAlliesOnBattleStart`


**Definition:** Applies or references the 'StatusAlliesOnBattleStart' effect/state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | `passives`<br>`class`<br>`tag` |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum  | Specifies which temporary item is equipped. | 2 | `Bottles`<br>`ButcherHook_Temporary`<br>`FoodBig` |

</details>


---


### Object: `StatusAlliesOnGainCoins`


**Definition:** Event Trigger: Applies nested statuses to allies on gain coins.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| `scaled` | Boolean || 1 | `true` |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


---


### Object: `StatusAllyWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to ally when ally spends mana.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


`damage_instance`<br>`spell`<br>`self_damage`


### Object: `StatusAnyCatAllyWhoKills`


**Definition:** Event Trigger: Applies nested statuses to any cat ally who kills.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusDamagers`


**Definition:** Event Trigger: Applies nested statuses to damagers.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Event Trigger: Applies nested statuses to each turn end for each turn.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` |
| [`RandomMagicMissile`](./Enums.md) | Integer | The number of random magic missiles fired, or an object defining its properties. | 3 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusEachTurnEndPerEnemyKill`


**Definition:** Event Trigger: Applies nested statuses to each turn end per enemy kill.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 2 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |

</details>


---


### Object: `StatusEnemiesOnDeath`


**Definition:** Event Trigger: Applies nested statuses to enemies on death.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusEveryXTurnBegins`


**Definition:** Event Trigger: Applies nested statuses to every x turn begins.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |

</details>


---


### Object: `StatusKillers`


**Definition:** Instantly kills the target if they possess the specified status effects.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnAnyDeath`


**Definition:** Event Trigger: Applies nested statuses when any death.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `StatusOnBattleEndIfKillThresholdMet`


**Definition:** Event Trigger: Applies nested statuses when battle end if kill threshold met.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `kills` | Number || 2 | `3` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 2 | `{ . . . }` |

</details>


---


### Object: `StatusOnBreakItem`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 2 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnCollectPickup`


**Definition:** Event Trigger: Applies nested statuses when collect pickup.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Tech`](./Enums.md) | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>


---


### Object: `StatusOnDealtDamage`


**Definition:** Event Trigger: Applies nested statuses when dealt damage.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TempDexterityUp`](./Enums.md) | Integer | The number of temporary dexterity stacks applied, or a string alias like 'X'. | 2 | `2`<br>`X` |
| [`TempStrengthUp`](./Enums.md) | Integer | The number of stacks of temporary Strength Up applied to the unit. | 2 | `1`<br>`2`<br>`X` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` | [`TempLuckUp`](./Enums.md) | Integer || 1 | `2`<br>`99` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `StatusOnDealtDamageThreshold`


**Definition:** Event Trigger: Applies nested statuses when dealt damage threshold.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count_overkill` | Boolean || 2 | `true` |
| `ignore_during_movement` | Boolean || 2 | `true` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of movement points restored to the source. | 2 | `1` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnEndMove`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnGainShield`


**Definition:** Event Trigger: Applies nested statuses when gain shield.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 2 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnHeal`


**Definition:** Event Trigger: Applies nested statuses when heal.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [`RandomStatUp`](./Enums.md) | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |

</details>


---


### Object: `StatusOnOverMana`


**Definition:** Event Trigger: Applies nested statuses when over mana.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`IntelligenceUp`](./Enums.md) | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`SpellDamageUp`](./Enums.md) | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | `1`<br>`3` |
| [`DivineShield`](./Enums.md) | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |

</details>


---


### Object: `StatusOnPickupCoins`


**Definition:** Event Trigger: Applies nested statuses when pickup coins.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| [`RefreshMovePoints`](./Enums.md) | Integer | The amount of movement points restored to the source. | 2 | `1` |
| [`DexterityUp`](./Enums.md) | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnPopCorpse`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 3 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnTookDamageFromEnemyAbility`


**Definition:** Event Trigger: Applies nested statuses when took damage from enemy ability.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| [`MoveQuivered`](./Enums.md) | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`[1, 0.1]` |

</details>


---


### Object: `StatusOnTriggerTrap`


**Definition:** Event Trigger: Applies nested statuses when trigger trap.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DexterityUp`](./Enums.md) | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 2 | `-1`<br>`1`<br>`2` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`Quivered`](./Enums.md) | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |

</details>


---


### Object: `StatusOnUseBasicAttack`


**Definition:** Event Trigger: Applies nested statuses when use basic attack.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| [`FlippedFacingForceAttack`](./Enums.md) | Integer || 2 | `1` |

</details>


---


### Object: `StatusOnUseElementAbility`


**Definition:** Event Trigger: Applies nested statuses when use element ability.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 2 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`SpeedUp`](./Enums.md) | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `StatusPerInjury`


**Definition:** Event Trigger: Applies nested statuses to per injury.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cap` | Number || 2 | `10`<br>`50%` |
| [`injury`](./Engine_EventKeys.md#valid-property-keys) | `String` || 2 | `bleeding`<br>`burned`<br>`cha` |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Variable | Inherits event response capabilities. You can inject any key from the Engine Event Keys list here to trigger outcomes like rewards, combat, or map generation. | 2 | `common`<br>`rare`<br>`cha` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`StrengthUp`](./Enums.md) | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusThingsKnockedBack`


**Definition:** Event Trigger: Applies nested statuses to things knocked back.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Drag` | Number | The distance (in tiles) that the unit drags knocked-back targets toward itself. | 2 | `1`<br>`2` |

</details>


---


### Object: `StatusWhenAllySpendsMana`


**Definition:** Event Trigger: Applies nested statuses to when ally spends mana.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | `passives`<br>`class`<br>`tag` |
| [`OneUseSpellDamageUp`](./Enums.md) | Integer | Increases spell damage by the specified amount, but the effect is consumed after a single use. Alias for SpellDamageUp. | 2 | `2` |
| [`ManaGain`](./Enums.md) | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `TaggedPickupEffectReplacement`


**Definition:** Applies the 'TaggedPickupEffectReplacement' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 2 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| [`HealthGain`](./Enums.md) | Integer / String | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `TowerDefense`


**Definition:** Applies the 'TowerDefense' effect.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root), [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Water`


**Definition:** Character Form: Behavior and stats for the \'Water\' state.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AOEPuddle`](./Math_Equations.md) | Equation | Specifies the pattern or shape of an area-of-effect puddle left on the ground. | 2 | `X-1` |

</details>


---


### Object: `Wind`


**Definition:** No definition provided.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#context-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](./Math_Equations.md) | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 2 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |

</details>


---


### Object: `AbilityChargeRefundChance`


**Definition:** Applies the 'AbilityChargeRefundChance' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `advantage_softcap` | Float || 1 | `3.5` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `AddStatusesIfPersistentWeatherElement`


**Definition:** Applies the 'AddStatusesIfPersistentWeatherElement' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AddStatusesToReceivedElementalDamage`


**Definition:** Applies the 'AddStatusesToReceivedElementalDamage' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`Burn`](./Enums.md) | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AddStatusToKnockbackDamage`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToReceivedDamage_ExcludeStatuses`


**Definition:** Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToSpells`


**Definition:** Modifier: Injects a status effect into a specific action.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddTemporaryEffectsToEquipment`


**Definition:** Applies the 'AddTemporaryEffectsToEquipment' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CastAgain` | Integer / String | The number of additional times the ability can be cast this turn. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `Autism`


**Definition:** Applies the 'Autism' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `innate` | Number || 1 | `-2` |
| `learned` | Number || 1 | `1` |

</details>


---


### Object: `ChanceToRevive`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 5 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 3 | `{ . . . }` |

</details>


---


### Object: `CollectPickupsOnBattleEnd`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean || 1 | `true` |

</details>


---


### Object: `Conditional_DoesDamage`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#context-addstatustoreceiveddamage_excludestatuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `Conditional_DoesDamage` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` |

</details>


---


### Object: `Conditional_GoodRoll`


**Definition:** Conditional trigger: Executes nested logic based on a randomized favorable outcome probability.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#context-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | - | `Conditional_GoodRoll` |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 37 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 37 | `Default`<br>`FormChange`<br>`Druid` |
| `UseRandomSpell_Madness` | `Number` | The number of random spells cast when Madness triggers. | 1 | `1` |

</details>


---


### Object: `Conditional_SourceHasTag`


**Definition:** Conditional object: Executes nested logic only if the target is/has SourceHasTag.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#context-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  || 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `DamageIfDidntUseSpecificAbility`


**Definition:** Combat Trigger: Deals damage to if didnt use specific ability.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |

</details>


---


### Object: `DelayedWind`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 1 | `-3`<br>`10`<br>`2` |

</details>


---


### Object: `DelayedWindCone`


**Definition:** Creates a delayed Area of Effect cone.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#context-addstatustomeleedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 2 | `-3`<br>`10`<br>`2` |

</details>


---


### Object: `Diabetes`


**Definition:** Applies the 'Diabetes' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [`Confusion`](./Enums.md) | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `EnergyStorm`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cycle_start` | Number || 1 | `2`<br>`3` |
| `period` | Number || 1 | `3` |

</details>


---


### Object: `fire`


**Definition:** Character Form: Behavior and stats for the 'Fire' state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 | `damage_instance`<br>`spell`<br>`false` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `ForceMoveAway`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#context-statusadjacentontheirturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean | If true, this option requires no cost to activate. | 1 | `false` |

</details>


---


### Object: `FurnitureStats`


**Definition:** Applies the 'FurnitureStats' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Appeal` | Number | The amount of appeal provided by the furniture piece to the room. | 1 | `-1`<br>`-2`<br>`-4` |
| `Comfort` | Number | The amount of comfort provided by the furniture piece to the room. | 1 | `-1`<br>`-2`<br>`-3` |
| `Stimulation` | Number | The amount of stimulation provided by the furniture piece to the room. | 1 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `ice`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 | `damage_instance`<br>`spell`<br>`false` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `lightning`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 | `damage_instance`<br>`spell`<br>`false` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `MegaMinions`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cycle_start` | Number || 1 | `2`<br>`3` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `MoveWhenDamaged`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 9 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |

</details>


---


### Object: `PassiveLevelScaledStatus`


**Definition:** Applies the 'PassiveLevelScaledStatus' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SizeScalePercent`](./Math_Equations.md) | Equation | A formula string that calculates the percentage scale of the unit's size based on a variable X (e.g., level). | 1 | `"sqrt(1.0+(.05*(X-1)))*100"` |
| [`Shield`](./Enums.md) | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Trample`](./Arrays.md#array-trample) | Array / Integer  | The amount of bonus damage dealt when moving through an enemy. | 1 | `1`<br>`3`<br>`4` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` | [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Key`<br>`Default`<br>`FormChange`

</details>


---


### Object: `RandomPassivePool`


**Definition:** Logic: Grants a random passive from the specified pool upon spawning.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` |
| [`PassiveGroup`](./Passives_and_Statuses.md#object-passivegroup) | Object  | A group of passive abilities that can be randomly assigned. | 2 | `{ . . . }` |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


---


### Object: `ReplaceBrain`


**Definition:** Applies the 'ReplaceBrain' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](./Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 4 | `DicerBrain`<br>`GenericBrain`<br>`MountBrain` |
| [`decision_weights`](./Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 4 | `always_cast`<br>`always_cast_careless`<br>`angry` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 4 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |

</details>


---


### Object: `Robot`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean || 2 | `true` |

</details>


---


### Object: `ScaledStatusOnBleedDamage`


**Definition:** Applies the 'ScaledStatusOnBleedDamage' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`Charge`](./Enums.md) | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `ScaledStatusOnLoseShield`


`damage_instance`<br>`spell`<br>`self_damage`
**Definition:** Applies the 'ScaledStatusOnLoseShield' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `ScaledStatusOnOverHealed`


**Definition:** Applies the 'ScaledStatusOnOverHealed' effect.  
**Total Count:** 1
`damage_instance`<br>`spell`<br>`self_damage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | The number of scaled Rot Flies to spawn when over-healed. | 1 | `0`<br>`1` |

</details>


---


### Object: `SelfDamageWhenDealDamage`


**Definition:** Applies the 'SelfDamageWhenDealDamage' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `StackingDodgeChanceOnTookDamage`


**Definition:** Applies the 'StackingDodgeChanceOnTookDamage' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`amount`](./Arrays.md#array-amount) | Array  | For ambient light, the target brightness value (as a float or percentage array for RGB). | 1 | `.1`<br>`.25`<br>`.35` |
| `cap` | Number || 1 | `10`<br>`50%` |

</details>


---


### Object: `StatusAdjacentOnTheirTurnBegin`


**Definition:** Event Trigger: Applies nested statuses to adjacent on their turn begin.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusAlliesEachTurn`


**Definition:** Applies or references the 'StatusAlliesEachTurn' effect/state.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#context-passiveuntilcastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` |
| `exclude_self` | Boolean || 1 | `false` |
| [`RandomStatUp`](./Enums.md) | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |

</details>


---


### Object: `StatusAlliesOnSpendMana`


**Definition:** Event Trigger: Applies nested statuses to allies on spend mana.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusAlliesScaledByCursedOnDeath`


**Definition:** Event Trigger: Applies nested statuses to allies scaled by cursed on death.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`LuckUp`](./Enums.md) | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `StatusIfBattleAlreadyBegan`


**Definition:** Event Trigger: Applies nested statuses to if battle already began.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`PermanentMadness`](./Enums.md) | Integer | The number of permanent madness stacks applied. | 1 | `1` |

</details>


---


### Object: `StatusOnEatPill`


**Definition:** Examples: `{ ... }`  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnLoseShield`


**Definition:** Event Trigger: Applies nested statuses when lose shield.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`Thorns`](./Enums.md) | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusOnTakeHealthDamage`


**Definition:** Event Trigger: Applies nested statuses when take health damage.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`PermanentConstitution`](./Enums.md) | Integer | The amount of permanent Constitution stat added or removed. | 1 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`


**Definition:** Event Trigger: Applies statuses when this action occurs.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 5 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`ManaGain`](./Enums.md) | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StrengthInNumbersAura`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `count_self` | Boolean || 1 | `true` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `Study`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `marked` | Number || 1 | `2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `TakeBonusTurnWithStatus`


**Definition:** Grants the character an immediate extra turn while afflicted with specific statuses.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#context-statusonkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 5 | `passives`<br>`class`<br>`tag` |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `TheHunger`


**Definition:** Applies the 'TheHunger' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [`Madness`](./Enums.md) | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `TileDamageMultiplier`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#context-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number || 1 | `0` |
| `multiplier` | Number | A multiplier applied to tile damage dealt to enemies. | 1 | `2` |

</details>


---


### Object: `TourettesMeows`


**Definition:** Applies the 'TourettesMeows' effect.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#context-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cooldown`](./Arrays.md#array-cooldown) | Array || 1 | `[8 15]` |
| [`pool`](./Arrays.md#array-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 | `2`<br>`3`<br>`4` |

</details>


---


### Object: `triattack`


**Definition:** No definition provided.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#context-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Variable | Inherits all standard damage properties. You can inject any key from the Engine Damaging Keys list here (such as `knockback`, `piercing`, or `elements`). | 1 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


<details>
<summary><b>AddSelfStatusToWeapons</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>AddStatusToAllDamage</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>AddStatusToBasicAttackWithCooldown</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>AddStatusToFirstBasicAttack</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>AddStatusToKnockbackDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>AddStatusToMeleeDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>AddStatusToReceivedDamage_ExcludeStatuses</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>AddStatusToSpells</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>AddStatusToTrampleDamage</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>Conditional_Adjacent</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>Conditional_DoesDamage</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>Conditional_GoodRoll</b></summary>

> **Total Count:** 30

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>Conditional_NotBoss</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>Conditional_PartyMember</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>Conditional_Shielded</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>ExtraStatusWhenDealingDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>NextBattleStatus</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>PassiveLevelScaledStatus</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusAdjacentOnTheirTurnBegin</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
`damage_instance`<br>`spell`<br>`self_damage`

</details>
<details>
<summary><b>StatusAlliesOnSpendMana</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusAnyCatAllyWhoKills</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusEnemiesOnDeath</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 0

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusKillers</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusOnDealtDamage</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusOnEatPill</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |

</details>
<details>
<summary><b>StatusOnOverHealed</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>
## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.


### Object: `AIControlNextTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean || 1 | `true` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `AbilityHealthThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 12 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 7 | `true` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 6 | `false`<br>`true` |
| `use_ai` | Boolean | If true, the ability uses AI targeting logic when triggered at the threshold. | 2 | `true` |
| `also_use_if_buddy_is_dead` | Boolean | If true, the ability is also triggered when the unit's buddy is dead. | 1 | `true` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 1 | `-1`<br>`1`<br>`10` |
| `threshold_min` | Enum | The minimum health threshold formula (e.g., X) for the ability to trigger. | 1 | `X` |


### Object: `AbilityOnRoundEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `force_display_name` | Boolean | If true, forces the display name to show for the ability. | 2 | `true` |


### Object: `AbilityOnRoundEndOnce`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_of_stunned` | Boolean || 1 | `true` |


### Object: `AddAdvantageToEvent`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array / Integer  || 1 | `5`<br>`[0.05 0.05 0.05]` |
| [`options`](./Arrays.md#array-options) | Array  || 1 | `[smash bash open]` |
| [`type`](./Enums.md#enum-type) | Enum  | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |


### Object: `AddStatusToBackstabs`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |


### Object: `AddStatusToFirstSpellEachTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsSelf`](./Miscellaneous.md#object-conditional_isself) | Object  || 1 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` 


### Object: `AddStatusToReceivedDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_IsPhysicalAttack`](./Miscellaneous.md#object-conditional_isphysicalattack) | Object  || 1 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` 


### Object: `AfterImage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `skilltemp` | Boolean || 2 | `true` |


### Object: `AggroTargetIsGovernedByHitEffect`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 1 | `false`<br>`true` |


### Object: `AllStatsAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`aura_requires_tag`](./Enums.md#enum-aura_requires_tag) | Enum   | Specifies the tag that units must have to be affected by this aura. | 1 | `humanoid` |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 1 | `1`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `AllStatsUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `AlluringDoodieEater`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |


### Object: `AllyDodgeChanceAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 1 | `1`<br>`10`<br>`2` |


### Object: `AlphaAllStatsUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `AlphaCat`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Ammo`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ArmorBreakOnHit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer || 2 | `10%`<br>`5%` |
| `durability_loss` | Integer || 2 | `0` |


### Object: `ArmorPickup`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array   | Specifies the minimum and maximum animation frame for the health pickup. | 3 | `[1 2]`<br>`[11 12]`<br>`[13 13]` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `BackflipWhenTargeted`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 7 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `BaitAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 4 | `1`<br>`10`<br>`2` |


### Object: `BattlefieldUniqueRandomPassive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Integer || 1 | `1` |
| `DemonicGlyph_Bounce` | Integer || 1 | `1` |
| `DemonicGlyph_Fire` | Integer || 1 | `1` |
| `DemonicGlyph_Movement` | Integer || 1 | `1` |
| `DemonicGlyph_Summon` | Integer || 1 | `1` |


### Object: `Bird`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BirdRewards`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_rewards`](./Miscellaneous.md#object-ally_rewards) | Object  || 18 | `{ . . . }` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 5 | `{ . . . }` |


### Object: `BlastResistance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Bleed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BleedThorns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Blind`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BoostDamageAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BoostDamageGlobalAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BossRewards`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`common`](./Enums.md#enum-common) | Enum  | Defines the common reward block for a boss encounter. | 20 | `100`<br>`14`<br>`5` |
| [`rare`](./Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 16 | `1`<br>`10`<br>`15` |


### Object: `Brace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BraceForEachNeighboringEnemy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Brittle`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BrittleDuringElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Bruise`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Buddy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 3 | `false`<br>`true` |
| [`obj`](./Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 3 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| `reclaim_if_lost` | Boolean | If true, the buddy can be reclaimed after being lost. | 1 | `true` |


### Object: `BuffImmunity`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exclude`](./Enums.md#enum-exclude) | Enum  | Specifies an element or effect that does not trigger the form change. | 1 | `SpellDamageUp`<br>`fire`<br>`water` |


### Object: `BungaCheers`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_damage`](./Enums.md#enum-ally_damage) | Enum   | Specifies the cheer effect when an ally takes damage. | 1 | `littleboo` |
| [`ally_dead`](./Enums.md#enum-ally_dead) | Enum   | Specifies the cheer effect when an ally dies. | 1 | `bigboo` |
| [`enemy_damage`](./Enums.md#enum-enemy_damage) | Enum   | Specifies the cheer effect when an enemy takes damage. | 1 | `littlecheer` |
| [`enemy_dead`](./Enums.md#enum-enemy_dead) | Enum   | Specifies the cheer effect when an enemy dies. | 1 | `bigcheer` |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum   | Specifies the tag used to identify allied warriors for this ability. | 1 | `bungawarrior`<br>`finalboss_clonecat` |


### Object: `BungaEntrance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` |
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 | `-1`<br>`150`<br>`50` |
| [`warrior_tag`](./Enums.md#enum-warrior_tag) | Enum   | Specifies the tag used to identify allied warriors for this ability. | 2 | `bungawarrior`<br>`finalboss_clonecat` |


### Object: `Burn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CatPartsSizeScale`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head`](./Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 1 | `-1`<br>`1`<br>`1.3` |


### Object: `CatPartsTransform`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`palette`](./Enums.md#enum-palette) | Enum / Integer  | Specifies the color palette index for the ability's visuals. | 17 | `-1`<br>`0`<br>`1` |
| `ear1` | Integer || 13 | `-2`<br>`1005`<br>`1013` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 13 | `-1`<br>`1000`<br>`1001` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 11 | `-1`<br>`-2`<br>`1` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 10 | `-1`<br>`-2`<br>`1` |
| `ear2` | Integer | The catalog ID for the cat's second ear part. | 10 | `1005`<br>`1013`<br>`1036` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 8 | `-1`<br>`-2`<br>`1` |
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 8 | `-1`<br>`1`<br>`10` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 8 | `-1`<br>`-2`<br>`1` |
| [`head`](./Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 6 | `-1`<br>`1`<br>`1.3` |
| `texture` | Integer | The catalog ID for the cat's texture. | 6 | `-1`<br>`1`<br>`1000` |
| `body` | Float | The catalog ID for the cat's body part. | 5 | `-1`<br>`1`<br>`1.1` |
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 3 | `-1`<br>`-2`<br>`1013` |
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 3 | `-1`<br>`1013`<br>`1057` |
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 1 | `-2`<br>`1069` |
| `eyebrow2` | Integer | The catalog ID for the cat's second eyebrow part. | 1 | `1070` |


### Object: `CaveFamilyEnrage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 6 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 6 | `0`<br>`1`<br>`10` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 6 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |


### Object: `CerberubsAggroTargetBehavior`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alert_form`](./Enums.md#enum-alert_form) | Enum   | Specifies the form to use when the unit is alerted. | 1 | `Alert` |
| [`default_form`](./Enums.md#enum-default_form) | Enum   | Specifies the default form before aggro. | 1 | `Normal` |


### Object: `ChainKnockback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ChanceToBlockAndCounter`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `backstab_only` | Boolean || 1 | `true` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |


### Object: `ChanceToForceEvent`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`event`](./Enums.md#enum-event) | Enum  || 1 | `Blessing`<br>`Death`<br>`Tragedy` |


### Object: `ChanceToFormChangeOnAbilityDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`form`](./Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 1 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |


### Object: `ChanceToSpitOnDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 7 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `flat_chance` | Integer | The base percentage chance to spit when taking damage. | 5 | `100%`<br>`50%` |
| `chance_per_damage` | Integer | The additional percentage chance to spit per point of damage taken. | 3 | `0%`<br>`2%` |
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 1 | `true` |
| `even_on_0_damage_if_knockback` | Boolean | If true, the reaction triggers on zero damage if knockback occurs. | 1 | `true` |


### Object: `ChaosBossFormChangeGuide`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array   | An array of piece names that are considered actively part of the current form. | 1 | `[Johnny Throb Flush]` |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array   | An array of piece names that are considered passively part of the current form. | 1 | `[Host Nettle Bubs]` |
| `passives_health_threshold` | Integer | The health percentage threshold at which the boss's passive abilities change. | 1 | `50%` |


### Object: `ChaosBossPieces`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`active_pieces`](./Arrays.md#array-active_pieces) | Array   | An array of piece names that are considered actively part of the current form. | 1 | `[Johnny Throb Flush]` |
| [`passive_pieces`](./Arrays.md#array-passive_pieces) | Array   | An array of piece names that are considered passively part of the current form. | 1 | `[Host Nettle Bubs]` |


### Object: `ChaosHeadDropIn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`new_music`](./Enums.md#enum-new_music) | Enum   | Specifies the music track to play during the boss's head drop-in animation. | 1 | `chaos_boss_part2` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |


### Object: `CharacterLightSource`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`color`](./Arrays.md#array-color) | Array  | The RGB color of the light source. | 16 | `[.27 .47 .18]`<br>`[.3, .7, 1]`<br>`[.32 .10 .10]` |
| [`size`](./Enums.md#enum-size) | Enum / Float  | The scale factor (size multiplier) of the spawned unit. | 16 | `.2`<br>`.5`<br>`1` |
| [`glow`](./Arrays.md#array-glow) | Array  | The RGBA glow color of the light source. | 8 | `[.3, .7, 1, .5]`<br>`[.7, .3, 1, .5]`<br>`[.7, .8, .9, .5]` |


### Object: `Charge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CharmAllFlies`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CherubimReaction`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Leave`](./Engine_LogicKeys.md#object-leave) | Enum / Object  || 2 | `{ . . . }`<br>`CherubimLeave`<br>`LELeave` |
| [`Return`](./Engine_LogicKeys.md#object-return) | Enum / Object  || 2 | `{ . . . }`<br>`CherubimReturn`<br>`LEReturn` |


### Object: `Conductor`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `Confusion`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ConjureBonusAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 2 | `true` |


### Object: `Consumed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum   || 12 | `auto`<br>`true` |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum   | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 | `deferred`<br>`false`<br>`true` |


### Object: `ConvertDamageToScaledStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 | `1` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `CounterAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 5 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `melee_only` | Boolean || 1 | `true` |
| `ranged_only` | Boolean | If true, the reaction only triggers on ranged attacks. | 1 | `true` |
| `without_orienting` | Boolean | If true, the counter-attack does not rotate the character to face the attacker. | 1 | `true` |


### Object: `CounterNextAttacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CreateGlobalModifiers`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BloodRain`](./Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object  | If non-zero, enables the blood rain visual effect. | 3 | `{ . . . }`<br>`1` |
| [`LowerAmbientLight`](./Miscellaneous.md#object-lowerambientlight) | Object  || 3 | `{ . . . }` |


### Object: `CritChanceUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CyborgTurns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TakeBonusTurnWithAIControl`](./Miscellaneous.md#object-takebonusturnwithaicontrol) | Object  || 1 | `{ . . . }` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `DamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DeathChill`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DeathRattleRevive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 8 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 8 | `true` |


### Object: `DejaVu`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DelayedAutoRevive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 6 | `0`<br>`1`<br>`10` |
| `rounds` | Integer | The number of rounds after which the auto-revive triggers. | 6 | `1`<br>`2` |


### Object: `DepressionAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `aura_effects_allies` | Boolean | If false, the aura does not affect allies. | 4 | `false` |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 4 | `1`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `DiceBehavior`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer | The number of sides on the die. | 1 | `6` |
| `knockback_damage` | Integer | The amount of damage dealt by the knockback. | 1 | `5` |


### Object: `DiesToElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  || 1 | `Electric`<br>`Fire`<br>`Gravity` |
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 1 | `true` |


### Object: `DiesToPiercingAndSpikes`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean | If true, the destruction is deferred until the character is settled. | 1 | `true` |


### Object: `DirtyClaws`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DivineShield`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DodgeChance_Status`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DodgeWhenTargeted`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |


### Object: `Doomed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DukeOfFlies`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DurabilityTransform`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eq`](./Arrays.md#array-eq) | Array  || 7 | `[0 EstusFlask_Empty]`<br>`[0 JarOfNothing]`<br>`[0 WaterBottle_Empty]` |
| [`ge`](./Arrays.md#array-ge) | Array  || 4 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |


### Object: `DybbukPossessionFallback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_ability`](./Enums.md#enum-exit_ability) | Enum   | Determines the ability used when the Dybbuk possession ends. | 1 | `DybbukReturn` |
| [`form`](./Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 1 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |


### Object: `Dyslexia`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `Empath`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `ExtraBasicAttacks_Status`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ExtraBasicMoves_Status`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FaceAwayLastDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 1 | `true` |
| `override_hit_animation` | Boolean | If true, the character's hit animation is overridden by the face-away animation. | 1 | `true` |
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 | `true` |


### Object: `FaceLastDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 1 | `true` |


### Object: `FinalBossBeamQueue`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`queue`](./Enums.md#enum-queue) | Enum  | Specifies the ability queued to fire the boss's beam. | 1 | `TheChild_TargetBeam` |
| [`release`](./Enums.md#enum-release) | Enum  | Specifies the ability queued to release the boss's stored beams. | 1 | `TheChild_ReleaseBeams` |
| [`transform`](./Enums.md#enum-transform) | Enum  | Specifies the ability queued to transform the boss into its next form. | 1 | `TheChild_TransformBoris` |


### Object: `FinalBossBecomeTheChild`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum  || 1 | `MegaGuppy` |
| `PlayBackground` | Integer || 1 | `0`<br>`1` |
| [`SwitchMusic`](./Miscellaneous.md#object-switchmusic) | Object  || 1 | `{ . . . }` |


### Object: `FinalBossHitCountdownBoris`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 | `800`<br>`802`<br>`804` |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 | `801`<br>`803`<br>`805` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` 


### Object: `FinalBossHitCountdownExplosive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 | `800`<br>`802`<br>`804` |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 | `801`<br>`803`<br>`805` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` 


### Object: `FinalBossHitCountdownHoly`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 1 | `800`<br>`802`<br>`804` |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 1 | `801`<br>`803`<br>`805` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `FinalBossPupils`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`look_at_offset`](./Arrays.md#array-look_at_offset) | Array   | A 3D vector offset from the head position that the pupils should look at. | 1 | `[0 2.5 0]` |
| [`radius`](./Arrays.md#array-radius) | Array / Integer  || 1 | `0`<br>`1`<br>`13` |
| `reset_center_because_no_target_halflife` | Float | The half-life for the pupil position to reset to center when no target is available. | 1 | `.1` |
| `reset_center_because_of_animation_halflife` | Float | The half-life for the pupil position to reset to center during an animation. | 1 | `.05` |
| `teleport_tracking_halflife` | Float | The half-life for the pupil tracking to reacquire a target after a teleport. | 1 | `.01` |
| `tracking_acquisition_halflife` | Float | The half-life for the pupil tracking to smoothly acquire a new target. | 1 | `.1` |
| [`virtual_head_position`](./Arrays.md#array-virtual_head_position) | Array   | A 3D vector representing the virtual position of the head for pupil tracking. | 1 | `[11 2 11]` |


### Object: `FinalBossShieldHealth`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`break_ability`](./Enums.md#enum-break_ability) | Enum   | Specifies the ability used to break the shield. | 1 | `DestroyerBreakShield` |
| [`state_health`](./Arrays.md#array-state_health) | Array   | An array of health thresholds defining state transitions. | 1 | `[` |


### Object: `FinalBossSyncAnimations`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`other_character`](./Enums.md#enum-other_character) | Enum   | Specifies the name of the other boss character whose animations are synced. | 1 | `MegaGuppy` |
| [`other_form_change_abilities`](./Miscellaneous.md#object-other_form_change_abilities) | Object  || 1 | `{ . . . }` |


### Object: `Flammable`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FlyDamageIncrease`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 1 | `false`<br>`true` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `Flying`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FollowUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FormChangeDuringWeatherElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  || 2 | `Electric`<br>`Fire`<br>`Gravity` |
| [`form`](./Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 2 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |


### Object: `FormChangeHealthThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_above`](./Enums.md#enum-form_above) | Enum   | The form to change to when health is above the threshold. | 3 | `Default`<br>`Full`<br>`Standing` |
| [`form_below`](./Enums.md#enum-form_below) | Enum   | The form to change to when health is below the threshold. | 3 | `Damaged`<br>`DesireMech`<br>`Standing2` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 3 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `count_shield` | Boolean | If true, shields count towards the health threshold calculation. | 1 | `true` |


### Object: `FormChangeOffMap`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_offmap`](./Enums.md#enum-form_offmap) | Enum   | Specifies the form name to use when the unit is off the map. | 8 | `Default_Ceiling`<br>`Insane_Ceiling`<br>`OffMap` |
| [`form_onmap`](./Enums.md#enum-form_onmap) | Enum   | Specifies the form name to use when the unit returns to the map. | 8 | `Default`<br>`Default_Ground`<br>`FightPhase` |


### Object: `FormChangeOnElementInfluence`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  || 9 | `Electric`<br>`Fire`<br>`Gravity` |
| [`form`](./Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 9 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| [`exclude`](./Enums.md#enum-exclude) | Enum  | Specifies an element or effect that does not trigger the form change. | 5 | `SpellDamageUp`<br>`fire`<br>`water` |
| [`particle`](./Enums.md#enum-particle) | Enum  | Specifies the particle effect displayed. | 5 | `ArrowFromAbove`<br>`BigMagicMissileBlast`<br>`Bolt` |
| [`sfx`](./Enums.md#enum-sfx) | Enum  | Specifies the sound effect to play when the form change triggers. | 5 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |


### Object: `FormChangeWhileHasStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum  || 35 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`form_hasnot`](./Enums.md#enum-form_hasnot) | Enum   | Specifies a form that the unit must not be in for the status-triggered form change to occur. | 30 | `Big`<br>`CaveWoman`<br>`Close` |
| [`form_has`](./Enums.md#enum-form_has) | Enum   | Specifies a form that the unit must be in for the status-triggered form change to occur. | 25 | `BellyFull`<br>`CaveWomanHasCat`<br>`FireFull` |


### Object: `FormChangeWhilePrimingAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`not_priming`](./Enums.md#enum-not_priming) | Enum   | Specifies the form name to use when the unit is not priming an ability. | 6 | `DualSword`<br>`NotPriming`<br>`SwordAndShield` |
| [`priming`](./Enums.md#enum-priming) | Enum  | Specifies the form name to use while the unit is priming an ability. | 6 | `DualSword_Primed`<br>`Priming`<br>`SwordAndShield_Primed` |


### Object: `FormChanger`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`initial_form`](./Enums.md#enum-initial_form) | Enum / Integer   | Specifies the starting form name for a unit with FormChanger. | 56 | `0`<br>`1`<br>`5` |
| [`Default`](./Miscellaneous.md#object-default) | Enum / Object  || 37 | `{ . . . }`<br>`release` |
| [`Normal`](./Miscellaneous.md#object-normal) | Integer / Object  || 11 | `{ . . . }`<br>`0` |
| [`Rage`](./Miscellaneous.md#object-rage) | Object  || 10 | `{ . . . }` |
| [`HasCat`](./Miscellaneous.md#object-hascat) | Object  || 5 | `{ . . . }` |
| [`OffMap`](./Miscellaneous.md#object-offmap) | Object  || 4 | `{ . . . }` |
| [`default`](./Miscellaneous.md#object-default) | Enum / Object  || 4 | `{ . . . }`<br>`bite1` |
| [`hot`](./Miscellaneous.md#object-hot) | Object  || 4 | `{ . . . }` |
| [`AllAlive`](./Miscellaneous.md#object-allalive) | Object  || 3 | `{ . . . }` |
| [`Down`](./Miscellaneous.md#object-down) | Object  || 3 | `{ . . . }` |
| [`Full`](./Miscellaneous.md#object-full) | Object  || 3 | `{ . . . }` |
| [`OneAlive`](./Miscellaneous.md#object-onealive) | Object  || 3 | `{ . . . }` |
| [`TwoAlive`](./Miscellaneous.md#object-twoalive) | Object  || 3 | `{ . . . }` |
| [`Up`](./Miscellaneous.md#object-up) | Object  || 3 | `{ . . . }` |
| [`Big`](./Miscellaneous.md#object-big) | Object  || 2 | `{ . . . }` |
| [`Boris`](./Miscellaneous.md#object-boris) | Enum / Object  || 2 | `{ . . . }`<br>`MegaGuppy_TransformBoris` |
| [`CaveMan`](./Miscellaneous.md#object-caveman) | Object  || 2 | `{ . . . }` |
| [`CaveManSpear`](./Miscellaneous.md#object-cavemanspear) | Object  || 2 | `{ . . . }` |
| [`Empty`](./Miscellaneous.md#object-empty) | Object  || 2 | `{ . . . }` |
| [`Explosive`](./Miscellaneous.md#object-explosive) | Enum / Object  || 2 | `{ . . . }`<br>`MegaGuppy_TransformExplosive` |
| [`Holding`](./Miscellaneous.md#object-holding) | Object  || 2 | `{ . . . }` |
| [`Holy`](./Passives_and_Statuses.md#object-holy) | Enum / Object  || 2 | `{ . . . }`<br>`MegaGuppy_TransformHoly` |
| [`NotPriming`](./Miscellaneous.md#object-notpriming) | Object  || 2 | `{ . . . }` |
| [`Priming`](./Miscellaneous.md#object-priming) | Object  || 2 | `{ . . . }` |
| [`Rain`](./Miscellaneous.md#object-rain) | Object  | Defines the rain weather effect with associated particle, sound, and rendering settings. | 2 | `{ . . . }` |
| [`Small`](./Miscellaneous.md#object-small) | Object  || 2 | `{ . . . }` |
| [`SquirrelForm`](./Miscellaneous.md#object-squirrelform) | Object  || 2 | `{ . . . }` |
| [`Turtled`](./Miscellaneous.md#object-turtled) | Object  || 2 | `{ . . . }` |
| [`active`](./Miscellaneous.md#object-active) | Object  || 2 | `{ . . . }` |
| [`passive`](./Miscellaneous.md#object-passive) | Object  || 2 | `{ . . . }` |
| [`Alert`](./Miscellaneous.md#object-alert) | Object  || 1 | `{ . . . }` |
| [`Angry`](./Miscellaneous.md#object-angry) | Object  || 1 | `{ . . . }` |
| [`Attacker`](./Miscellaneous.md#object-attacker) | Object  || 1 | `{ . . . }` |
| [`BellyFull`](./Miscellaneous.md#object-bellyfull) | Object  || 1 | `{ . . . }` |
| [`BigHolding`](./Miscellaneous.md#object-bigholding) | Object  || 1 | `{ . . . }` |
| [`BigHoldingCat`](./Miscellaneous.md#object-bigholdingcat) | Object  || 1 | `{ . . . }` |
| [`Bishop`](./Miscellaneous.md#object-bishop) | Boolean (Flag) / Object  || 1 | `{ . . . }` |
| [`BlackHole`](./Miscellaneous.md#object-blackhole) | Object  || 1 | `{ . . . }` |
| [`Bomb`](./Miscellaneous.md#object-bomb) | Boolean (Flag) / Object  || 1 | `{ . . . }` |
| [`Bully`](./Miscellaneous.md#object-bully) | Object  || 1 | `{ . . . }` |
| [`Butcher`](./Engine_LogicKeys.md#object-butcher) | Object  || 1 | `{ . . . }` |
| [`CaveBaby`](./Miscellaneous.md#object-cavebaby) | Object  || 1 | `{ . . . }` |
| [`CaveWoman`](./Miscellaneous.md#object-cavewoman) | Object  || 1 | `{ . . . }` |
| [`CaveWomanHasCat`](./Miscellaneous.md#object-cavewomanhascat) | Object  || 1 | `{ . . . }` |
| [`Charging`](./Miscellaneous.md#object-charging) | Object  || 1 | `{ . . . }` |
| [`Close`](./Miscellaneous.md#object-close) | Object  || 1 | `{ . . . }` |
| [`Colorless`](./Engine_LogicKeys.md#object-colorless) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Cultist`](./Miscellaneous.md#object-cultist) | Object  || 1 | `{ . . . }` |
| [`Damaged`](./Miscellaneous.md#object-damaged) | Object  || 1 | `{ . . . }` |
| [`Default_Ceiling`](./Miscellaneous.md#object-default_ceiling) | Object  || 1 | `{ . . . }` |
| [`Default_Ground`](./Miscellaneous.md#object-default_ground) | Object  || 1 | `{ . . . }` |
| [`DesireMech`](./Miscellaneous.md#object-desiremech) | Object  || 1 | `{ . . . }` |
| [`Die`](./Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 1 | `{ . . . }`<br>`1`<br>`6` |
| [`Druid`](./Engine_LogicKeys.md#object-druid) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Drunker`](./Miscellaneous.md#object-drunker) | Object  || 1 | `{ . . . }` |
| [`DualSword`](./Miscellaneous.md#object-dualsword) | Object  || 1 | `{ . . . }` |
| [`DualSword_Primed`](./Miscellaneous.md#object-dualsword_primed) | Object  || 1 | `{ . . . }` |
| [`Dumb`](./Miscellaneous.md#object-dumb) | Integer / Object  || 1 | `{ . . . }`<br>`3` |
| [`Explody`](./Miscellaneous.md#object-explody) | Object  || 1 | `{ . . . }` |
| [`FightPhase`](./Miscellaneous.md#object-fightphase) | Object  || 1 | `{ . . . }` |
| [`Fighter`](./Engine_LogicKeys.md#object-fighter) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Fire`](./Passives_and_Statuses.md#object-fire) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`FireFull`](./Miscellaneous.md#object-firefull) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`Flop`](./Miscellaneous.md#object-flop) | Object  || 1 | `{ . . . }` |
| [`Flop2`](./Miscellaneous.md#object-flop2) | Object  || 1 | `{ . . . }` |
| [`Flush`](./Miscellaneous.md#object-flush) | Object  || 1 | `{ . . . }` |
| [`FlushBubs`](./Miscellaneous.md#object-flushbubs) | Object  || 1 | `{ . . . }` |
| [`FlushHost`](./Miscellaneous.md#object-flushhost) | Object  || 1 | `{ . . . }` |
| [`FlushNettle`](./Miscellaneous.md#object-flushnettle) | Object  || 1 | `{ . . . }` |
| [`Grappling`](./Miscellaneous.md#object-grappling) | Object  || 1 | `{ . . . }` |
| [`Grown`](./Miscellaneous.md#object-grown) | Object  || 1 | `{ . . . }` |
| [`GuaranteedJackpot`](./Miscellaneous.md#object-guaranteedjackpot) | Object  || 1 | `{ . . . }` |
| [`Guarding`](./Miscellaneous.md#object-guarding) | Object  || 1 | `{ . . . }` |
| [`HalfDead`](./Miscellaneous.md#object-halfdead) | Object  || 1 | `{ . . . }` |
| [`HasDeadCat`](./Miscellaneous.md#object-hasdeadcat) | Object  || 1 | `{ . . . }` |
| [`HasRock`](./Miscellaneous.md#object-hasrock) | Object  || 1 | `{ . . . }` |
| [`Headless`](./Miscellaneous.md#object-headless) | Object  || 1 | `{ . . . }` |
| [`Hint_CrackedVisuals`](./Miscellaneous.md#object-hint_crackedvisuals) | Object  || 1 | `{ . . . }` |
| [`Hint_CrackedVisuals2`](./Miscellaneous.md#object-hint_crackedvisuals2) | Object  || 1 | `{ . . . }` |
| [`Hint_CrackedVisuals3`](./Miscellaneous.md#object-hint_crackedvisuals3) | Object  || 1 | `{ . . . }` |
| [`HumanDead`](./Miscellaneous.md#object-humandead) | Object  || 1 | `{ . . . }` |
| [`Hunter`](./Engine_LogicKeys.md#object-hunter) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`InitialPhase`](./Miscellaneous.md#object-initialphase) | Object  || 1 | `{ . . . }` |
| [`Insane_Ceiling`](./Miscellaneous.md#object-insane_ceiling) | Object  || 1 | `{ . . . }` |
| [`Insane_Ground`](./Miscellaneous.md#object-insane_ground) | Object  || 1 | `{ . . . }` |
| [`Johnny`](./Miscellaneous.md#object-johnny) | Object  || 1 | `{ . . . }` |
| [`JohnnyBubs`](./Miscellaneous.md#object-johnnybubs) | Object  || 1 | `{ . . . }` |
| [`JohnnyHost`](./Miscellaneous.md#object-johnnyhost) | Object  || 1 | `{ . . . }` |
| [`JohnnyNettle`](./Miscellaneous.md#object-johnnynettle) | Object  || 1 | `{ . . . }` |
| [`Joystick`](./Miscellaneous.md#object-joystick) | Object  || 1 | `{ . . . }` |
| [`LastHit`](./Miscellaneous.md#object-lasthit) | Object  || 1 | `{ . . . }` |
| [`Lifted`](./Miscellaneous.md#object-lifted) | Object  || 1 | `{ . . . }` |
| [`Lit`](./Miscellaneous.md#object-lit) | Object  || 1 | `{ . . . }` |
| [`Mage`](./Engine_LogicKeys.md#object-mage) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Medic`](./Engine_LogicKeys.md#object-medic) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Monk`](./Engine_LogicKeys.md#object-monk) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Mounted`](./Miscellaneous.md#object-mounted) | Object  || 1 | `{ . . . }` |
| [`MouthFull`](./Miscellaneous.md#object-mouthfull) | Object  || 1 | `{ . . . }` |
| [`Mutant`](./Miscellaneous.md#object-mutant) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`Necromancer`](./Engine_LogicKeys.md#object-necromancer) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`NeutronStar`](./Miscellaneous.md#object-neutronstar) | Object  || 1 | `{ . . . }` |
| `NoDeathRattle` | Object || 1 | `{ . . . }` |
| [`NoEyes`](./Miscellaneous.md#object-noeyes) | Object  || 1 | `{ . . . }` |
| [`NoStick`](./Miscellaneous.md#object-nostick) | Object  || 1 | `{ . . . }` |
| [`NormalFull`](./Miscellaneous.md#object-normalfull) | Integer / Object  || 1 | `{ . . . }`<br>`0` |
| [`Nuke`](./Miscellaneous.md#object-nuke) | Object  || 1 | `{ . . . }` |
| [`Obey`](./Miscellaneous.md#object-obey) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`Off`](./Miscellaneous.md#object-off) | Object  || 1 | `{ . . . }` |
| [`OffScreen`](./Miscellaneous.md#object-offscreen) | Object  || 1 | `{ . . . }` |
| [`OneEye`](./Miscellaneous.md#object-oneeye) | Object  || 1 | `{ . . . }` |
| [`Open`](./Miscellaneous.md#object-open) | Object  || 1 | `{ . . . }` |
| [`OpenCat`](./Miscellaneous.md#object-opencat) | Object  || 1 | `{ . . . }` |
| [`Out`](./Miscellaneous.md#object-out) | Object  || 1 | `{ . . . }` |
| [`Possessing`](./Miscellaneous.md#object-possessing) | Object  || 1 | `{ . . . }` |
| [`Primed`](./Miscellaneous.md#object-primed) | Object  || 1 | `{ . . . }` |
| [`Psychic`](./Engine_LogicKeys.md#object-psychic) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Pulp2`](./Miscellaneous.md#object-pulp2) | Object  || 1 | `{ . . . }` |
| [`Pulp3`](./Miscellaneous.md#object-pulp3) | Object  || 1 | `{ . . . }` |
| [`Pulp4`](./Miscellaneous.md#object-pulp4) | Object  || 1 | `{ . . . }` |
| [`Pulp5`](./Miscellaneous.md#object-pulp5) | Object  || 1 | `{ . . . }` |
| [`Pulp6`](./Miscellaneous.md#object-pulp6) | Object  || 1 | `{ . . . }` |
| [`Pulp7`](./Miscellaneous.md#object-pulp7) | Object  || 1 | `{ . . . }` |
| [`Sitting`](./Miscellaneous.md#object-sitting) | Object  || 1 | `{ . . . }` |
| [`SmallHolding`](./Miscellaneous.md#object-smallholding) | Object  || 1 | `{ . . . }` |
| [`SmallHoldingCat`](./Miscellaneous.md#object-smallholdingcat) | Object  || 1 | `{ . . . }` |
| [`SpawningPhase`](./Miscellaneous.md#object-spawningphase) | Object  || 1 | `{ . . . }` |
| [`Standing`](./Miscellaneous.md#object-standing) | Object  || 1 | `{ . . . }` |
| [`Standing2`](./Miscellaneous.md#object-standing2) | Object  || 1 | `{ . . . }` |
| [`Start_Ceiling`](./Miscellaneous.md#object-start_ceiling) | Object  || 1 | `{ . . . }` |
| [`Stop`](./Miscellaneous.md#object-stop) | Integer / Object  || 1 | `{ . . . }`<br>`2` |
| [`SwordAndShield`](./Miscellaneous.md#object-swordandshield) | Object  || 1 | `{ . . . }` |
| [`SwordAndShield_Primed`](./Miscellaneous.md#object-swordandshield_primed) | Object  || 1 | `{ . . . }` |
| [`Tank`](./Engine_LogicKeys.md#object-tank) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Tar`](./Miscellaneous.md#object-tar) | Integer / Object  || 1 | `{ . . . }`<br>`2` |
| [`TarFull`](./Miscellaneous.md#object-tarfull) | Integer / Object  || 1 | `{ . . . }`<br>`2` |
| [`Thief`](./Engine_LogicKeys.md#object-thief) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Throb`](./Miscellaneous.md#object-throb) | Object  || 1 | `{ . . . }` |
| [`ThrobBubs`](./Miscellaneous.md#object-throbbubs) | Object  || 1 | `{ . . . }` |
| [`ThrobHost`](./Miscellaneous.md#object-throbhost) | Object  || 1 | `{ . . . }` |
| [`ThrobNettle`](./Miscellaneous.md#object-throbnettle) | Object  || 1 | `{ . . . }` |
| [`Tinkerer`](./Engine_LogicKeys.md#object-tinkerer) | Array / Object  || 1 | `{ . . . }`<br>`[` |
| [`Transformed`](./Miscellaneous.md#object-transformed) | Object  || 1 | `{ . . . }` |
| [`TwoEyes`](./Miscellaneous.md#object-twoeyes) | Object  || 1 | `{ . . . }` |
| [`Unlit`](./Miscellaneous.md#object-unlit) | Object  || 1 | `{ . . . }` |
| `Unmounted` | Object || 1 | `{ . . . }` |
| [`Unwashed`](./Miscellaneous.md#object-unwashed) | Object  || 1 | `{ . . . }` |
| [`Washed`](./Miscellaneous.md#object-washed) | Object  || 1 | `{ . . . }` |
| [`Washer`](./Miscellaneous.md#object-washer) | Object  || 1 | `{ . . . }` |
| [`Water`](./Passives_and_Statuses.md#object-water) | Object  || 1 | `{ . . . }` |
| [`WereMan`](./Miscellaneous.md#object-wereman) | Object  || 1 | `{ . . . }` |
| [`Zealot`](./Miscellaneous.md#object-zealot) | Object  || 1 | `{ . . . }` |
| [`ZealotBomb`](./Miscellaneous.md#object-zealotbomb) | Object  || 1 | `{ . . . }` |
| `sync_brain_patterns` | Boolean | If true, synchronizes brain patterns across form changes. | 1 | `true` |


### Object: `Fragile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FragileDuringElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FrankBolts`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `FullPower`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `GlobalFamiliarDamageBoost`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `GlobalFamiliarMoveBoost`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `GlobalFlowerTrapperAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Tangled`](./Miscellaneous.md#object-tangled) | Array / Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |


### Object: `GlobalMeleeRevengeDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 1 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |


### Object: `HPAltStates`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`clipname`](./Enums.md#enum-clipname) | Enum  | Specifies the animation clip name to use for the alt state. | 1 | `poopmain` |
| [`thresholds`](./Arrays.md#array-thresholds) | Array  | An array of health percentage thresholds that trigger an alt state. | 1 | `[` |


### Object: `HealNeighborsEachTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 1 | `false`<br>`true` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `HealingAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `HealthPickup`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array   | Specifies the minimum and maximum animation frame for the health pickup. | 15 | `[1 2]`<br>`[11 12]`<br>`[13 13]` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 15 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `stored_food_value` | Integer | The amount of food value stored in this pickup. | 15 | `0`<br>`1`<br>`2` |
| `anything_eats` | Boolean | If true, any unit can consume this health pickup. | 4 | `true` |
| `force_frame` | Integer | Forces the health pickup to use a specific animation frame. | 1 | `12` |


### Object: `HealthRegenUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `HitlerExecute`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |


### Object: `Hypomania`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `ImmediateAbilityReaction`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 13 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 6 | `true` |
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 2 | `true` |
| `damage_threshold` | Integer | The amount of damage that must be dealt to trigger the ability reaction. | 2 | `10` |
| `even_if_blocked` | Boolean | If true, the reaction triggers even if the damage is blocked. | 2 | `true` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` |
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 2 | `-1`<br>`150`<br>`50` |
| `buddy_damage_only` | Boolean | If true, only damage dealt by the unit's buddy triggers the reaction. | 1 | `true` |
| `target_furthest_valid` | Boolean | If true, the reaction targets the furthest valid enemy. | 1 | `true` |


### Object: `Immobile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ImmortalLeeches`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ItemAuxTransform`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`le`](./Arrays.md#array-le) | Array  || 3 | `[10 MoneyBag_Small]`<br>`[25 MoneyBag_Medium]`<br>`[50 MoneyBag_Large]` |
| [`ge`](./Arrays.md#array-ge) | Array  || 2 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |
| [`lt`](./Arrays.md#array-lt) | Array  || 1 | `[10 NuclearKnife]` |


### Object: `JohnnyNeedsWashing`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_unwashed`](./Enums.md#enum-form_unwashed) | Enum   | Specifies the form name for the unwashed state. | 1 | `Unwashed` |
| [`form_washed`](./Enums.md#enum-form_washed) | Enum   | Specifies the form name for the washed state. | 1 | `Washed` |


### Object: `KillsHeal`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `KineticSpikes`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Lifesteal`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `LuckUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Madness`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `tickdown_this_turn` | Boolean | If true, madness stacks decrease at the start of this turn instead of the next. | 1 | `true` |


### Object: `ManaPickup`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`frame_range`](./Arrays.md#array-frame_range) | Array   | Specifies the minimum and maximum animation frame for the health pickup. | 3 | `[1 2]`<br>`[11 12]`<br>`[13 13]` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `MegaDinoDropController`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head_drop`](./Enums.md#enum-head_drop) | Enum   | Specifies the ability triggered when the head drops down. | 1 | `MD_HeadDrop` |
| [`leg_leave`](./Enums.md#enum-leg_leave) | Enum   | Specifies the ability triggered when the legs leave the body. | 1 | `MD_LegLeave` |
| [`leg_return`](./Enums.md#enum-leg_return) | Enum   | Specifies the ability triggered when the legs return to the body. | 1 | `MD_LegReturn` |
| `stable_legs` | Integer | The number of legs that must be stable for the head to drop. | 1 | `3` |


### Object: `Metal`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MetalDetector`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MissChance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ModularPickup`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 1 | `{ . . . }`<br>`0`<br>`1` |
| [`sound_event`](./Enums.md#enum-sound_event) | Enum   | Specifies the sound event to play when the pickup is used. | 1 | `EatAntidote` |


### Object: `MonkCatReactionAbilities`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](./Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 1 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`spell`](./Enums.md#enum-spell) | Enum  | Specifies the spell ability to use as a reaction. | 1 | `MCHadouken` |
| [`trinket`](./Enums.md#enum-trinket) | Enum  | The name of the trinket item the unit starts with. | 1 | `MCHadouken`<br>`MonkStyleChanger` |
| [`weapon`](./Enums.md#enum-weapon) | Enum  || 1 | `AstroTaser`<br>`ButcherHook`<br>`CaveCatClub` |


### Object: `MotherGrowController`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eat_damage`](./Miscellaneous.md#object-eat_damage) | Object  || 1 | `{ . . . }` |
| [`tumor_object`](./Enums.md#enum-tumor_object) | Enum   | Specifies the name of the tumor object to spawn. | 1 | `MotherTumor` |


### Object: `MotherTumorPassive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](./Miscellaneous.md#object-cat) | Object  || 1 | `{ . . . }` |
| [`NonCat`](./Miscellaneous.md#object-noncat) | Object  || 1 | `{ . . . }` |
| [`considered_forms`](./Arrays.md#array-considered_forms) | Array   | An array of form names the tumor considers for interaction. | 1 | `[Big BigHolding BigHoldingCat]` |
| [`grow_ability`](./Enums.md#enum-grow_ability) | Enum   | Specifies the ability used by the tumor to grow. | 1 | `MotherTumorGrow` |
| [`pass_ani`](./Enums.md#enum-pass_ani) | Enum   | Specifies the animation played when passing something to the tumor. | 1 | `pass` |
| [`receive_ani`](./Enums.md#enum-receive_ani) | Enum   | Specifies the animation played when receiving something from the tumor. | 1 | `receive` |


### Object: `MotherTumorSpawnInCapture`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](./Miscellaneous.md#object-cat) | Object  || 2 | `{ . . . }` |
| [`NonCat`](./Miscellaneous.md#object-noncat) | Object  || 2 | `{ . . . }` |
| [`Nothing`](./Miscellaneous.md#object-nothing) | Object  || 1 | `{ . . . }` |


### Object: `Mount`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eject_ability`](./Enums.md#enum-eject_ability) | Enum   | Specifies the ability used to eject the mounted character. | 1 | `MechSuitEject` |
| [`enter_ability`](./Enums.md#enum-enter_ability) | Enum   | Specifies the ability used to enter the mount. | 1 | `EnterMech` |


### Object: `MoveAfterAnyAttemptedAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 1 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |


### Object: `MoveAwayFromDamageSource`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum   | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |


### Object: `MoveAwayWhenEnemyAdjacent`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum   | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| `once_per_turn` | Boolean | If true, the movement away can only trigger once per turn. | 1 | `true` |
| [`weights`](./Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 1 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |


### Object: `MoveQuivered`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MoveTowardsKillers`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`character_filter`](./Arrays.md#array-character_filter) | Array   | Specifies which characters to consider as killers when moving towards them. | 3 | `[SpiderCat, TallSpiderCat]` |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum   | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 3 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |


### Object: `MultiSpawnOnDeath`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |
| [`obj`](./Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 1 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |


### Object: `MutateAfterXTurns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `NoManaRegen`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `NonStackingDivineShield`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `NumbingLeeches`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ObjectDetector`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `Paranoia`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `PassiveIfStrAuxEquals`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 7 | `{ . . . }` |
| `value` | Enum | The numeric value or formula associated with the buff. | 7 | `.5`<br>`0`<br>`1` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | `passives`<br>`class`<br>`tag` 


### Object: `PassiveIfWeaponIsUsable`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `{ . . . }`<br>`1`<br>`10`<br>`2` |


### Object: `PassiveWhenDead`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` | [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 1 | `{ . . . }`<br>`SpiderReturn` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` 


### Object: `PassiveWhenOnTile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 7 | `{ . . . }` |
| [`tile`](./Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 7 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 7 | `passives`<br>`class`<br>`tag` 


### Object: `PassiveWhileHasDurability`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MovementReaction`](./Passives_and_Statuses.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` | [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Key`<br>`Default`<br>`FormChange` 


### Object: `PassiveWhileNotHasStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| [`status`](./Enums.md#enum-status) | Enum  || 2 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` 


### Object: `PassiveWhileShielded`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |


### Object: `PermanentImmobile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `PermanentMadness`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Poison`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `PoisonThorns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `PoopWhenHit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `ProtectTargetedAllies`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`target_filter`](./Enums.md#enum-target_filter) | Enum   | Specifies which targets the protection applies to, based on their unit type or tag. | 2 | `Kitten`<br>`any` |


### Object: `Quiver`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Quivered`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ReduceManaCost`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ReflectProjectiles`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 8 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |


### Object: `RefreshEquipmentAbilityOnElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  || 2 | `Electric`<br>`Fire`<br>`Gravity` |
| `text` | String || 2 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |


### Object: `RunWhenLastPlayerCatIsCharmed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | If true, allows the decision to run to occur mid-turn instead of at the end. | 1 | `true` |
| [`legacy_savekey`](./Enums.md#enum-legacy_savekey) | Enum   | Specifies the save key used to persist a legacy stolen cat ID. | 1 | `Legacy_Marshmallow_StolenCatID` |


### Object: `SafeDoomed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ScaldingOrbMoonBossOneShot`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](./Enums.md#enum-completeitemquest) | Enum  || 1 | `BlackShard`<br>`Nuke`<br>`ScaldingOrb` |
| [`RemoveItem`](./Enums.md#enum-removeitem) | Enum  || 1 | `BlackShard`<br>`BlackShard_Glowing`<br>`ScaldingOrb` |


### Object: `ScaledStatusAlliesOnSpendMana`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](./Passives_and_Statuses.md#object-conditional_adjacent) | Object  || 1 | `{ . . . }` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` | [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Key`<br>`Default`<br>`FormChange` 


### Object: `ScaledStatusOnHolyShieldBlock`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomMagicMissile`](./Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`2` |


### Object: `ScalingAttackAnimation`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](./Miscellaneous.md#object-default) | Enum / Object  || 1 | `{ . . . }`<br>`bite1` |
| [`thresholds`](./Arrays.md#array-thresholds) | Array  | An array of health percentage thresholds that trigger an alt state. | 1 | `[` |


### Object: `SchrodingerDisorder`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `Scleroderma`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `SharePickups`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | If true, coins are included in the shared pickup pool. | 1 | `true` |


### Object: `ShoulderCheck`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ShovingMatch`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SkipFirstRounds`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_chance` | Integer | The percentage chance that the first round is skipped. | 1 | `50%` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `SlotMachineRollPool`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SlotResult_Jackpot_Coins`](./Engine_LogicKeys.md#object-slotresult_jackpot_coins) | Integer / Object  || 2 | `{ . . . }`<br>`1` |
| [`SlotResult_Explode`](./Engine_LogicKeys.md#object-slotresult_explode) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`SlotResult_Nothing`](./Engine_LogicKeys.md#object-slotresult_nothing) | Integer / Object  || 1 | `{ . . . }`<br>`7` |
| [`SlotResult_RandomPickup`](./Engine_LogicKeys.md#object-slotresult_randompickup) | Integer / Object  || 1 | `{ . . . }`<br>`11` |


### Object: `Slow`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SmallRockBehavior`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 4 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 4 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `chain` | Boolean | Specifies the ability to chain into and execute. | 2 | `AcidSplash`<br>`CaveSplash`<br>`FireFullSmall` |


### Object: `SpawnCatCopyWhenDowned`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`prevent_chain_tag`](./Enums.md#enum-prevent_chain_tag) | Enum   | A tag that prevents chaining of spawns from the same source. | 2 | `ancestorset_shade`<br>`eb_twin`<br>`minime_clone` |


### Object: `SpawnExtraThingsOnBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`number`](./Arrays.md#array-number) | Array / Integer  || 31 | `1`<br>`10`<br>`2` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 23 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`tile`](./Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 7 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| [`trap`](./Enums.md#enum-trap) | Enum  || 2 | `BearTrap`<br>`LandMine`<br>`WaterKittenTrap` |


### Object: `SpawnItemLinkedFamiliar`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `break_on_pop_only` | Boolean || 2 | `true` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `SpawnObjectOnPopCorpse`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |
| `except_tiny` | Boolean || 1 | `true` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `SpawnOnDeath`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](./Enums.md#enum-faction) | Enum  | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 4 | `allies`<br>`auto`<br>`birds` |
| [`obj`](./Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 4 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| [`additional_statuses`](./Miscellaneous.md#object-additional_statuses) | Object  || 1 | `{ . . . }` |


### Object: `SpawnRandomPickupsOnTaggedUnitKilled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |


### Object: `SpeedUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SpellDamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SpewerAltGraphics`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Fire`](./Passives_and_Statuses.md#object-fire) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`FireFull`](./Miscellaneous.md#object-firefull) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| [`Normal`](./Miscellaneous.md#object-normal) | Integer / Object  || 1 | `{ . . . }`<br>`0` |
| [`NormalFull`](./Miscellaneous.md#object-normalfull) | Integer / Object  || 1 | `{ . . . }`<br>`0` |
| [`Tar`](./Miscellaneous.md#object-tar) | Integer / Object  || 1 | `{ . . . }`<br>`2` |
| [`TarFull`](./Miscellaneous.md#object-tarfull) | Integer / Object  || 1 | `{ . . . }`<br>`2` |


### Object: `SproutsGrantMovement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StackingFlowerTrail`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum   || 3 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `StatDependentPassive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | String || 1 | `1`<br>`2`<br>`4` |


### Object: `StatusAdjacentOnTheirTurnEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Integer | The distance to force the target away from the source. | 1 | `1` |


### Object: `StatusAfterXTurns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 2 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` 


### Object: `StatusAllCharactersOnSpawn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |


### Object: `StatusCollector`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 7 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`10`<br>`2` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |


### Object: `StatusEachRoundBegin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number || 8 | `12`<br>`16`<br>`3` |


### Object: `StatusEachRoundEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoDamage`](./Miscellaneous.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 1 | `{ . . . }` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 1 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |


### Object: `StatusEachTurnBeginIfHasStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [`animation`](./Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 1 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| `consume` | Boolean | If true, the status is consumed after triggering. | 1 | `true` |
| [`status`](./Enums.md#enum-status) | Enum  || 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |


### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` 


### Object: `StatusEveryXSpellCastsEachTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `StatusIfDidntMove`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |


### Object: `StatusIfUnusedActPoints`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of backflip charges, or an object defining its ability. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| [`Craft`](./Passives_and_Statuses.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 1 | `{ . . . }` |


### Object: `StatusOnBackstab`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| `SerratedClaws` | Integer || 1 | `1` |


### Object: `StatusOnBreak`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 20 | `passives`<br>`class`<br>`tag` | [`Bruise`](#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 3 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 3 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `HealthGain` | Integer | The amount of health restored to the source. | 3 | `1`<br>`10`<br>`2` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 3 | `1`<br>`2`<br>`3` |
| [`ApplyToRandomPartyMemberIfPossible`](./Miscellaneous.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. | 1 | `{ . . . }` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |


### Object: `StatusOnDie`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 9 | `passives`<br>`class`<br>`tag` | [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`RandomMagicMissile`](./Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `RemoveAmbientLightEffects` | Float | The fade-out duration in seconds for ambient light effects. | 1 | `.5`<br>`4` |
| [`ScatterCoins`](./Miscellaneous.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 1 | `{ . . . }` |


### Object: `StatusOnDodge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 1 | `1`<br>`10`<br>`100` |


### Object: `StatusOnEnemyCastSpell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |


### Object: `StatusOnEnemyConfused`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 1 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |


### Object: `StatusOnEnemyDeath`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |


### Object: `StatusOnFallAsleep`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 1 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 1 | `1` |


### Object: `StatusOnFullMana`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Miscellaneous.md#object-conditional_onceperbattle) | Object  || 1 | `{ . . . }` |


### Object: `StatusOnSetPieceBreak`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag` | [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 1 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. | 1 | `1`<br>`2` |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 1 | `-1`<br>`-2`<br>`1` |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 1 | `1`<br>`2` |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 1 | `-1`<br>`1`<br>`2` |
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. | 1 | `1`<br>`2` |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 1 | `-1`<br>`1`<br>`2` |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 1 | `1`<br>`2` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 1 | `80s`<br>`90s`<br>`AdvancedAlloy` |


### Object: `StatusOnSpawnIn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 1 | `1` |
| `SetHealth` | Integer || 1 | `1`<br>`100%`<br>`50%` |


### Object: `StatusOnTakeHealthOrShieldDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 4 | `passives`<br>`class`<br>`tag` | `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| [`Metronome`](./Miscellaneous.md#object-metronome) | Boolean (Flag) / Float / Object  | The number of times Metronome triggers, or an object with stacks and banned abilities. | 1 | `{ . . . }`<br>`1`<br>`2` |
| [{Logic Keys}](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` 


### Object: `StatusOverlappingCharactersAndDie`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |


### Object: `StatusRandomEnemiesOnBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |


### Object: `StatusWhenStatusCompletelyRemoved`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 1 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [`status`](./Enums.md#enum-status) | Enum  || 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |


### Object: `Stealth`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StrengthForEachNeighboringEnemy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StrengthUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StunImmunity`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | If true, removes any existing stun effect when this immunity is applied. | 1 | `false` |


### Object: `SupportDieInsteadOfRun`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](./Enums.md#enum-alt_dead_ani) | Enum   | Specifies the alternative death animation to use when the support unit dies instead of running. | 1 | `off` |
| [`alt_dying_ani`](./Enums.md#enum-alt_dying_ani) | Enum   | Specifies the alternative dying animation to use. | 1 | `shutdown` |


### Object: `SupportFormChangeInsteadOfRun`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `wait_till_turn` | Boolean | If true, the form change will not occur until the unit's next turn. | 1 | `true` |


### Object: `SwimmingFormChange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_in`](./Enums.md#enum-form_in) | Enum   | Determines the form to change into when entering water. | 1 | `Water` |
| [`form_out`](./Enums.md#enum-form_out) | Enum   | Determines the form to change into when leaving water. | 1 | `Out` |


### Object: `SyncFormsWithBuddy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`no_buddy`](./Enums.md#enum-no_buddy) | Enum   | Specifies an alternative form to use when there is no buddy. | 1 | `Rage` |


### Object: `T3HitlerSpawningPhase`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_use_groups`](./Arrays.md#array-spell_use_groups) | Array   | List of spell use groups that the spawning phase can use. | 1 | `[` |


### Object: `TVBotScreen`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Die`](./Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 1 | `{ . . . }`<br>`1`<br>`6` |
| [`Dumb`](./Miscellaneous.md#object-dumb) | Integer / Object  || 1 | `{ . . . }`<br>`3` |
| `Fuck` | Integer || 1 | `5` |
| [`Obey`](./Miscellaneous.md#object-obey) | Integer / Object  || 1 | `{ . . . }`<br>`1` |
| `Shit` | Integer || 1 | `4` |
| [`Stop`](./Miscellaneous.md#object-stop) | Integer / Object  || 1 | `{ . . . }`<br>`2` |


### Object: `Tech`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TempInitiativeChange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Terminator2Run`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](./Enums.md#enum-move_ability) | Enum   | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 1 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |


### Object: `TerminatorChase`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 1 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |


### Object: `TerminatorSkin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`groups`](./Arrays.md#array-groups) | Array  | Groups of actors that this skin applies to. | 1 | `[` |
| [`status`](./Enums.md#enum-status) | Enum  || 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |


### Object: `Thorns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TinkererBasicAttackSwitching`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`craft_ability`](./Enums.md#enum-craft_ability) | Enum   | The ability used for the craft action in the Tinkerer's basic attack switching. | 3 | `TinkererCraft` |
| [`throw_ability`](./Enums.md#enum-throw_ability) | Enum   | The ability used for the throw action in the Tinkerer's basic attack switching. | 3 | `TinkererThrow` |


### Object: `TintItem`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`add`](./Arrays.md#array-add) | Array / Integer  || 1 | `5`<br>`[0.05 0.05 0.05]` |
| [`ignore_if_str_aux_equals`](./Enums.md#enum-ignore_if_str_aux_equals) | Enum   || 1 | `ModelingClay_Default` |
| [`mul`](./Arrays.md#array-mul) | Array  || 1 | `[0.45 0.3 0.25]` |


### Object: `Trample`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TransformInXTurns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 8 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`initiative`](./Enums.md#enum-initiative) | Enum / Integer  | The unit's turn order priority; can be an integer modifier or 'keep_turns_end_turn' to force end of turn after acting. | 4 | `-10`<br>`-100`<br>`-20` |
| [`animation`](./Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |


### Object: `TransformItemOnElementInfluence`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  || 5 | `Electric`<br>`Fire`<br>`Gravity` |
| `full_repair` | Boolean || 5 | `true` |
| [`item`](./Enums.md#enum-item) | Enum  || 5 | `1`<br>`2`<br>`EstusFlask_Full` |


### Object: `TransformOnDeathImmediately`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`first_turn`](./Enums.md#enum-first_turn) | Enum   | Determines when the spawned unit takes its first turn relative to the spawn event. | 4 | `end_of_round`<br>`initiative`<br>`keep_turns` |
| [`obj`](./Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 4 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |


### Object: `TransformOnElementInfluence`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  || 9 | `Electric`<br>`Fire`<br>`Gravity` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 9 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `TransformOnElementInfluencex`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](./Arrays.md#array-element) | Array / Enum  || 2 | `Electric`<br>`Fire`<br>`Gravity` |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `TransformOnStatusThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`status`](./Enums.md#enum-status) | Enum  || 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 1 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |


### Object: `Trapper`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `cancel_movement` | Boolean | If true, the trapper cancels the trapped unit's movement. | 2 | `false` |
| `pathfinding_avoidance` | Integer | The weight that makes other units avoid traversing this tile during pathfinding. | 2 | `250` |
| [`range`](./Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `1`<br>`10`<br>`2` |


### Object: `Triskaidekaphobia`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `TunnelVision`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Equation | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 1 | `-999999`<br>`.05*X`<br>`.25` |


### Object: `TwisterFling`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 1 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 1 | `2`<br>`20`<br>`3` |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 1 | `2`<br>`3`<br>`4` |


### Object: `UnlimitedDeathRattleRevive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 1 | `true` |


### Object: `UseAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `respect_prime` | Boolean || 2 | `true` |


### Object: `UseAbilityWhenOutOfStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`status`](./Enums.md#enum-status) | Enum  || 1 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |


### Object: `Vegan`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `Vengeful`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Weakness`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `WobblyCat`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `Zombie`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |