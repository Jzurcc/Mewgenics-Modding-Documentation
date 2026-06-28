---
title: "Passives & Statuses Schema"
description: "Defines buffs, debuffs, and permanent modifiers."
---

# Passives & Statuses Schema

## Overview
> [!NOTE]
> This schema controls passive effects (like permanent Poison immunity) and temporary status effects (like being On Fire for 3 turns).

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
Putrefy {
    name "PASSIVE_PUTREFY_NAME"
    desc "PASSIVE_PUTREFY_DESCRIPTION"
    class Butcher

    1 {
        passives {
            AddStatusToBasicAttack {
                Rot 1
            }
        }
    }
    2 {
        desc "PASSIVE_PUTREFY2_DESCRIPTION"
        passives {
            AddStatusToBasicAttack {
                Rot -999999
            }
        }
    }
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Passives.md`](../../Directory/Items_and_Passives/Passives.md)
- [`Statuses.md`](../../Directory/Statuses_and_Injuries/Statuses.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Passives & Statuses

> **Associated Files:** `data/passives/, data/passive_pools.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 511

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](../Reference_and_Meta/Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 511 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 510 | passives<br>class<br>tag |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 510 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 510 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 116 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 35 | `{ . . . }` |
| [`lock_item_slot`](./Passives_and_Statuses.md#object-lock_item_slot) | Object | An object that restricts which equipment slots can be used. | 16 | `{ . . . }` |
| [`desc_multiclass`](../Assets_and_Localization/Strings.md#string-desc_multiclass) | String | A localization key for the multiclass description of a passive ability. | 5 | `"PASSIVE_BARBED2_MULTICLASS_DESC"`<br>`"PASSIVE_BARBED_MULTICLASS_DESC"`<br>`"PASSIVE_GRAPPLINGHOOK2_MULTICLASS_DESC"` |
| [`name_mod`](../Assets_and_Localization/Strings.md#string-name_mod) | String | A localization key for a name modifier applied to the character's name. | 4 | `"CAT_NAME_MOD_AMOEBA"`<br>`"CAT_NAME_MOD_COOL"`<br>`"CAT_NAME_MOD_DWARF"` |
| `auto_plus_signs_on_name` | Boolean | If false, plus signs are not automatically added to the status's display name. | 4 | `false` |
| [`tags`](../Reference_and_Meta/Arrays.md#array-tags) | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 3 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`override_basic_attack`](../Reference_and_Meta/Enums.md#enum-override_basic_attack) | Enum | Specifies the ability that replaces the unit's basic attack. | 2 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`shield`](../Reference_and_Meta/Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 2 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`bonus_items`](../Reference_and_Meta/Arrays.md#array-bonus_items) | Array | An array of item names granted as bonus rewards. | 1 | `[Eyeball]`<br>`[FoodBig FoodBig FoodBig FoodBig]`<br>`[Pipe]` |
| [`grant_ability`](../Reference_and_Meta/Enums.md#enum-grant_ability) | Enum | Specifies the name of an ability to grant to the player or unit. | 1 | `Rest` |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 0 | `-1`<br>`-2`<br>`-3` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 0 | `-1`<br>`-10`<br>`-2` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 0 | `1`<br>`10`<br>`100` |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 0 | `+1`<br>`-1`<br>`-2` |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 0 | `-1`<br>`-10`<br>`-2` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer | The Strength stat value or modifier. | 0 | `-1`<br>`-2`<br>`-3` |
| [`SpawnOnBattleStart`](./Passives_and_Statuses.md#object-spawnonbattlestart) | Enum / Object  | Specifies the object that spawns adjacent to the unit at the start of battle. | 0 | `{ . . . }`<br>`BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| [`lck`](../Reference_and_Meta/Enums.md#enum-lck) | Enum / Integer | The Luck stat value or modifier. | 0 | `-1`<br>`-2`<br>`-3` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 0 | `10`<br>`15`<br>`20` |
| [`dex`](../Reference_and_Meta/Enums.md#enum-dex) | Enum / Integer | The Dexterity stat value or modifier. | 0 | `-1`<br>`-2`<br>`-3` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 0 | `1`<br>`3`<br>`4` |
| [`AmplifyStatus`](../Reference_and_Meta/Enums.md#enum-amplifystatus) | Enum | Specifies the status effect to amplify, or an object with the status and number of stacks to add. | 0 | `Bleed`<br>`Burn`<br>`Poison` |
| [`BoostWeaponDamage`](./Passives_and_Statuses.md#object-boostweapondamage) | Object  | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 0 | `{ . . . }` |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. | 0 | `{ . . . }` |
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 0 | `0`<br>`1`<br>`2` |
| [`StatusImmunity`](../Reference_and_Meta/Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 0 | `Burn`<br>`Poison`<br>`Tarred` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 0 | `1`<br>`2`<br>`[1, 0.1]` |
| [`BlastResistance`](./Passives_and_Statuses.md#object-blastresistance) | Array / Float / Object | The amount of damage reduction against blast-type damage. | 0 | `{ . . . }`<br>`2`<br>`3`<br>`4` |
| [`empty_armor_scaled_stats`](./Passives_and_Statuses.md#object-empty_armor_scaled_stats) | Object  | Defines the stat bonuses applied when no armor is equipped in a slot. | 0 | `{ . . . }` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 0 | `1`<br>`2`<br>`3` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 0 | `1`<br>`2`<br>`5` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 0 | `.4`<br>`.6`<br>`.7` |
| [`Empath`](./Passives_and_Statuses.md#object-empath) | Float / Object | The percentage of damage shared with nearby allies from the Empath disorder. | 0 | `{ . . . }`<br>`100%`<br>`50%` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 0 | `1` |
| [`AfterImage`](./Passives_and_Statuses.md#object-afterimage) | Object  | Specifies the object or skill used to create an afterimage of the unit. | 0 | `{ . . . }` |
| [`Conductor`](./Passives_and_Statuses.md#object-conductor) | Boolean (Flag) / Float / Object | The number of times the Conduct effect is applied. | 0 | `{ . . . }`<br>`2` |
| [`ChainKnockback`](./Passives_and_Statuses.md#object-chainknockback) | Float / Object | If 1, enables knockback to chain to additional targets. | 0 | `{ . . . }`<br>`1` |
| [`DirtyClaws`](./Passives_and_Statuses.md#object-dirtyclaws) | Float / Object | The number of additional damage instances from Dirty Claws on attack. | 0 | `{ . . . }`<br>`1` |
| [`EnergyStorm`](./Passives_and_Statuses.md#object-energystorm) | Float / Object | The period or definition for the Energy Storm, dealing periodic damage in an area. | 0 | `{ . . . }`<br>`3` |
| [`LateBloomer`](./Passives_and_Statuses.md#object-latebloomer) | Array / Float / Object | Specifies the stats gained after a set number of turns or stacks. | 0 | `{ . . . }` |
| [`Quiver`](./Passives_and_Statuses.md#object-quiver) | Float / Object | Grants additional ammunition capacity or reload charges for ranged weapon abilities, increasing how many times they can be fired. | 0 | `{ . . . }`<br>`1`<br>`2` |
| [`ShoulderCheck`](./Passives_and_Statuses.md#object-shouldercheck) | Float / Object | The chance (as a percentage) to perform a Shoulder Check, pushing a target back after a melee attack. | 0 | `{ . . . }`<br>`100%`<br>`33%` |
| [`ShovingMatch`](./Passives_and_Statuses.md#object-shovingmatch) | Enum / Object | Determines which stat (e.g., 'attack') is used for the Shoving Match shoving contest. | 0 | `{ . . . }`<br>`attack` |
| [`DukeOfFlies`](./Passives_and_Statuses.md#object-dukeofflies) | Float / Object | The number of flies spawned when the unit dies. | 0 | `{ . . . }`<br>`1` |
| [`FollowUp`](./Passives_and_Statuses.md#object-followup) | Enum / Object | Specifies the name of the follow-up ability triggered after an attack. | 0 | `{ . . . }`<br>`FollowUpDash`<br>`FollowUpDash2` |
| [`FullPower`](./Passives_and_Statuses.md#object-fullpower) | Float / Object | The number of stacks applied per turn while at full health or full mana. | 0 | `{ . . . }`<br>`3` |
| [`ImmortalLeeches`](./Passives_and_Statuses.md#object-immortalleeches) | Float / Object | The number of leech stacks that persist beyond death. | 0 | `{ . . . }`<br>`1` |
| [`KillsHeal`](./Passives_and_Statuses.md#object-killsheal) | Float / Object | The amount or percentage of health restored on kill. | 0 | `{ . . . }`<br>`5`<br>`50%` |
| [`MegaMinions`](./Passives_and_Statuses.md#object-megaminions) | Float / Object | The number of extra minions spawned or maximum minion count. | 0 | `{ . . . }`<br>`3` |
| [`MetalDetector`](./Passives_and_Statuses.md#object-metaldetector) | Float / Object | The number of extra metal drops or scrap found per turn. | 0 | `{ . . . }`<br>`10`<br>`5` |
| [`NumbingLeeches`](./Passives_and_Statuses.md#object-numbingleeches) | Float / Object | The number of leeches that apply a numbing effect, reducing the target's output or disabling certain actions. Also the name of a Necromancer passive. | 0 | `{ . . . }`<br>`3` |
| [`Study`](./Passives_and_Statuses.md#object-study) | Float / Object | The number of stacks of the Study status applied. | 0 | `{ . . . }`<br>`1` |
| [`Vengeful`](./Passives_and_Statuses.md#object-vengeful) | Float / Object | The number of Vengeful stacks, causing retaliation damage when hit. | 0 | `{ . . . }`<br>`1` |
| [`DeathChill`](./Passives_and_Statuses.md#object-deathchill) | Float / Object | The number of Chill stacks applied to the killer upon death. | 0 | `{ . . . }`<br>`1` |
| [`DejaVu`](./Passives_and_Statuses.md#object-dejavu) | Float / Object | The percentage chance or definition for the DejaVu disorder, causing repeated events. | 0 | `{ . . . }`<br>`10%` |
| [`HealingAura`](./Passives_and_Statuses.md#object-healingaura) | Float / Object | The amount of healing per turn granted to nearby allies. | 0 | `{ . . . }`<br>`1` |
| [`schadenfreude_scaled_stats`](./Passives_and_Statuses.md#object-schadenfreude_scaled_stats) | Object  | Defines the stat bonuses (str, dex, con, int, cha) applied by the Schadenfreude trait at a given level. | 0 | `{ . . . }` |
| `Metal` | Integer | The number of armor stacks or metal keyword effects. | 0 | `1` |
| [`Weakness`](./Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 0 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Robot`](./Passives_and_Statuses.md#object-robot) | Integer / Object  | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 0 | `{ . . . }`<br>`1` |
| [`CounterAttack`](./Passives_and_Statuses.md#object-counterattack) | Array / Enum / Object  | Specifies the ability used when the unit counterattacks after being hit. | 0 | `{ . . . }`<br>`BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| [`DeathRattle`](./Passives_and_Statuses.md#object-deathrattle) | Enum / Object  | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 0 | `{ . . . }`<br>`BBExplode`<br>`BloatyExplodey`<br>`BombFlyExplode` |
| [`AbilityReaction`](./Passives_and_Statuses.md#object-abilityreaction) | Enum / Object  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 0 | `{ . . . }`<br>`AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 0 | `1` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 0 | `1`<br>`3` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 0 | `1`<br>`2`<br>`3` |
| [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#object-movetowardsdamagesource) | Enum / Object  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 0 | `{ . . . }`<br>`MoveOne` |
| [`Stealth`](../Reference_and_Meta/Arrays.md#array-stealth) | Array / Integer  | The number of stealth stacks applied. | 0 | `1`<br>`2`<br>`[1 .1]` |
| [`ChanceToRevive`](./Passives_and_Statuses.md#object-chancetorevive) | Integer / Object | The percentage chance or an object defining chance, health, and statuses on revival. | 0 | `{ . . . }`<br>`100`<br>`25` |
| `BackstabCritChance` | Float | A multiplier for critical hit chance on backstab attacks. | 0 | `.25`<br>`1` |
| [`SpawnObjectOnPopCorpse`](./Passives_and_Statuses.md#object-spawnobjectonpopcorpse) | Enum / Object | Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped. | 0 | `{ . . . }`<br>`Catnip`<br>`Coin`<br>`Food` |
| [`AllyBonusAbilityAura`](./Passives_and_Statuses.md#object-allybonusabilityaura) | Enum / Object | Specifies an ability name granted to adjacent allies in an aura, optionally with a square radius. | 0 | `{ . . . }`<br>`NubbyToss` |
| [`ChanceToBlockAndCounter`](./Passives_and_Statuses.md#object-chancetoblockandcounter) | Integer / Object | The percentage chance or an object defining chance and conditions to block and counter an attack. | 0 | `{ . . . }`<br>`15%`<br>`25%`<br>`33%` |
| [`FlyDamageIncrease`](./Passives_and_Statuses.md#object-flydamageincrease) | Object | The number of stacks or alias for damage increase against flying units. | 0 | `{ . . . }` |
| [`ProtectTargetedAllies`](./Passives_and_Statuses.md#object-protecttargetedallies) | Object  | Specifies the ability used to protect targeted allies, including an optional target filter. | 0 | `{ . . . }` |
| [`AutocastEachTurnBegin`](./Passives_and_Statuses.md#object-autocasteachturnbegin) | Enum / Object | Specifies the ability automatically cast at the start of each turn, optionally with chance and polarity. | 0 | `{ . . . }`<br>`MindCrack_EldritchVisage`<br>`MindCrack_EldritchVisage2` |
| [`BraceForEachNeighboringEnemy`](./Passives_and_Statuses.md#object-braceforeachneighboringenemy) | Array / Float / Object | The number of Brace stacks gained for each adjacent enemy. | 0 | `{ . . . }`<br>`1`<br>`2` |
| [`CharmAllFlies`](./Passives_and_Statuses.md#object-charmallflies) | Array / Float / Object | If 1, charms all fly-type enemies, causing them to become allies. | 0 | `{ . . . }`<br>`1` |
| [`DamageReductionAura`](./Passives_and_Statuses.md#object-damagereductionaura) | Array / Float / Object | Defines an aura that reduces incoming damage, with range, ally-only, and stack settings. | 0 | `{ . . . }` |
| [`LowHealthAllyDodgeChanceAura`](./Passives_and_Statuses.md#object-lowhealthallydodgechanceaura) | Array / Float / Object | Specifies the health threshold and dodge chance granted to nearby low-health allies. | 0 | `{ . . . }` |
| [`SharePickups`](./Passives_and_Statuses.md#object-sharepickups) | Object  | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 0 | `{ . . . }` |
| [`StrengthForEachNeighboringEnemy`](./Passives_and_Statuses.md#object-strengthforeachneighboringenemy) | Array / Float / Object | The amount of strength gained for each adjacent enemy. | 0 | `{ . . . }`<br>`2`<br>`3` |
| [`BoostDamageGlobalAura`](./Passives_and_Statuses.md#object-boostdamageglobalaura) | Array / Float / Object | The amount of damage boost applied by a global aura to all allies. | 0 | `{ . . . }`<br>`1` |
| [`CollectPickupsOnBattleEnd`](./Passives_and_Statuses.md#object-collectpickupsonbattleend) | Float / Object | The number of pickups automatically collected from corpses on the battlefield when the battle ends. | 0 | `{ . . . }`<br>`1` |
| `LineOfSightTrueSightAura` | Float | The multiplier or chance for line of sight true sight aura to reveal hidden units. | 0 | `.5`<br>`0` |
| [`StrengthInNumbersAura`](./Passives_and_Statuses.md#object-strengthinnumbersaura) | Float / Object | The amount of strength gained per nearby ally within the aura. | 0 | `{ . . . }`<br>`1` |
| [`TileDamageMultiplier`](./Passives_and_Statuses.md#object-tiledamagemultiplier) | Float / Object | Multiplier for damage dealt to environmental tiles. | 0 | `{ . . . }`<br>`2` |
| [`Vegan`](./Passives_and_Statuses.md#object-vegan) | Float / Object  | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 0 | `{ . . . }`<br>`1` |
| `RandomStatUp` | Equation / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 0 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 0 | `0`<br>`1`<br>`10%` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 0 | `-1`<br>`1`<br>`2` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 0 | `1`<br>`2`<br>`3` |
| [`SpawnExtraThingsOnBattleStart`](./Passives_and_Statuses.md#object-spawnextrathingsonbattlestart) | Object  | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 0 | `{ . . . }` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 0 | `1`<br>`2`<br>`3` |
| [`ReflectProjectiles`](./Passives_and_Statuses.md#object-reflectprojectiles) | Integer / Object  | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 0 | `{ . . . }`<br>`1`<br>`10%`<br>`100%` |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Integer / Object  | The number of backflip charges, or an object defining its ability. | 0 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| [`MoveWhenDamaged`](./Passives_and_Statuses.md#object-movewhendamaged) | Enum / Object  | Defines movement behavior when the unit takes damage, such as weights and move ability. | 0 | `{ . . . }`<br>`TKNG_Hop`<br>`move` |
| `YOffset` | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 0 | `-.18`<br>`.25`<br>`.35` |
| `DepressionAura` | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 0 | `1`<br>`2` |
| [`ConjureBonusAbility`](./Passives_and_Statuses.md#object-conjurebonusability) | Enum / Object  | Specifies the name of the bonus ability to conjure. | 0 | `{ . . . }`<br>`Class`<br>`Colorless`<br>`Mage` |
| [`PoopWhenHit`](./Passives_and_Statuses.md#object-poopwhenhit) | Object  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 0 | `{ . . . }` |
| [`MoveAwayFromDamageSource`](./Passives_and_Statuses.md#object-moveawayfromdamagesource) | Object  | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 0 | `{ . . . }` |
| `SwapHighestAndLowestStat` | Integer | If non-zero, swaps the unit's highest base stat value with its lowest. | 0 | `1` |

</details>


---


### Object: `passives`


**Definition:** A container object listing passive effects granted to the unit.  
**Total Count:** 2807

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAfterXKills`](./Passives_and_Statuses.md#object-passiveafterxkills), [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#object-passiveathealththreshold), [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#object-passiveatinjurythreshold), [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#object-passiveatstatthreshold), [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement), [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 880 | passives<br>class<br>tag |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 80 | `{ . . . }` |
| [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions) | Object | An object containing passives that are granted to all minions spawned by the unit. | 29 | `{ . . . }` |
| [`MulticlassLevelUp`](../Reference_and_Meta/Enums.md#enum-multiclasslevelup) | Enum  | Specifies the class that this unit gains a level in when multiclassing. | 24 | `Butcher`<br>`Druid`<br>`Fighter` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 22 | `1`<br>`10`<br>`100` |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage) | Object  | Specifies status effects or actions triggered when the unit takes damage. | 21 | `{ . . . }` |
| [`SpawnOnBattleStart`](./Passives_and_Statuses.md#object-spawnonbattlestart) | Enum / Object  | Specifies the object that spawns adjacent to the unit at the start of battle. | 21 | `{ . . . }`<br>`BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#object-statuseachturnend) | Object  | Specifies status effects applied to the unit at the end of each of its turns. | 20 | `{ . . . }` |
| `AddCritMultiplier` | Integer | The percentage added to the critical hit damage multiplier. | 17 | `100%`<br>`125%`<br>`150%` |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 16 | `{ . . . }` |
| [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 14 | `{ . . . }` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 14 | `10`<br>`15`<br>`20` |
| [`ReplaceSpawnedObjects`](../Reference_and_Meta/Arrays.md#array-replacespawnedobjects) | Array | An array of [original_object replacement_object] pairs for swapping spawned objects. | 13 | `[Boulder AnimatedBoulder]`<br>`[Boulder AnimatedLavaBoulder]`<br>`[Crow Crow2]` |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 12 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 | `Default`<br>`FormChange`<br>`Druid` | `AddElementsToBasicAttack` | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 174 | Default<br>FormChange<br>Druid |
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 11 | `10%`<br>`15%`<br>`2%` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 11 | `1`<br>`10`<br>`2` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 11 | `1`<br>`2`<br>`3` |
| [`BonusAbility`](../Reference_and_Meta/Enums.md#enum-bonusability) | Enum  | Specifies the name of a bonus ability granted. | 11 | `Bloodzerk`<br>`BonusToss`<br>`BonusToss2` |
| `AddBonusRange` | Integer | The number of additional tiles of range added to the unit's abilities. | 11 | `1`<br>`10`<br>`2` |
| [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#object-passiveatstatthreshold) | Object | An object defining passives granted when a unit's stat meets a specified threshold. | 10 | `{ . . . }` |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#object-critsapplystatus) | Object | An object containing statuses applied to the target when the unit lands a critical hit. | 10 | `{ . . . }` |
| `PassiveLevelUpAtCombatEnd` | Integer | The number of times a passive levels up automatically when combat ends. | 10 | `1` |
| `ExtraBasicAttacks` | Integer | The number of additional basic attacks the unit can perform per turn. | 9 | `1`<br>`2` |
| [`Trample`](../Reference_and_Meta/Arrays.md#array-trample) | Array / Integer  | The amount of bonus damage dealt when moving through an enemy. | 9 | `1`<br>`3`<br>`4` |
| [`RevengeDamage`](./Passives_and_Statuses.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 9 | `{ . . . }` |
| `SizeScale` | Float | The multiplier applied to the unit's visual and hitbox size. | 8 | `.4`<br>`.6`<br>`.7` |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 8 | `{ . . . }` |
| [`StatusImmunity`](../Reference_and_Meta/Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 8 | `Burn`<br>`Poison`<br>`Tarred` |
| [`ReplaceBasicAttack`](../Reference_and_Meta/Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 8 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`InnateElement`](../Reference_and_Meta/Enums.md#enum-innateelement) | Enum  | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 8 | `Earth`<br>`Electric`<br>`Fire` |
| [`AmplifyStatus`](./Passives_and_Statuses.md#object-amplifystatus) | Enum / Object | Specifies the status effect to amplify, or an object with the status and number of stacks to add. | 8 | `{ . . . }`<br>`Bleed`<br>`Burn`<br>`Poison` |
| [`EquipTemporaryItem`](../Reference_and_Meta/Enums.md#enum-equiptemporaryitem) | Enum  | Specifies which temporary item is equipped. | 8 | `Bottles`<br>`ButcherHook_Temporary`<br>`FoodBig` |
| `ForceSpecificInjury` | Enum | Forces the unit to receive an injury to the specified stat. | 8 | `cha`<br>`int`<br>`lck` |
| [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#object-passiveifallarmorempty) | Object | Grants the contained passive effects when no armor is equipped in any slot. | 8 | `{ . . . }` |
| [`StatusOnCrit`](./Passives_and_Statuses.md#object-statusoncrit) | Object | An object containing statuses applied to the unit when it lands a critical hit. | 8 | `{ . . . }` |
| [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#object-damageneighborsonendmove) | Object | Deals damage and knockback to units on neighboring tiles when the unit finishes moving. | 7 | `{ . . . }` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 7 | `1`<br>`2`<br>`3` |
| `AddCorpseHealth` | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 7 | `-999`<br>`-999999`<br>`100` |
| [`AbilityOnBattleStart`](../Reference_and_Meta/Enums.md#enum-abilityonbattlestart) | Enum | Casts the specified ability when the battle begins. | 7 | `Flush`<br>`Heathens`<br>`Heathens2` |
| `BlastResistance` | Integer | The amount of damage reduction against blast-type damage. | 7 | `2`<br>`3`<br>`4` |
| [`ElementImmune`](../Reference_and_Meta/Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 7 | `Creep`<br>`Electric`<br>`Fire` |
| [`StatusAlliesOnDeath`](./Passives_and_Statuses.md#object-statusalliesondeath) | Object | Applies the contained status effects to all allies when the unit dies. | 7 | `{ . . . }` |
| [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#object-passiveifemptyface) | Object | Grants the contained passive effects when the face armor slot is empty. | 7 | `{ . . . }` |
| [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#object-passiveifemptyhead) | Object | Grants the contained passive effects when the head armor slot is empty. | 7 | `{ . . . }` |
| [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#object-passiveifemptyneck) | Object | Grants the contained passive effects when the neck armor slot is empty. | 7 | `{ . . . }` |
| [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#object-statusonuseabilitywithtag) | Object | Applies the contained status effects when the unit uses an ability with the specified tag. | 7 | `{ . . . }` |
| `SetSpellCosts` | Integer | Overrides the cost of all spells to this value. | 6 | `0`<br>`1`<br>`3` |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 6 | `1`<br>`10`<br>`2` |
| [`SpawnThingOnDamage`](./Passives_and_Statuses.md#object-spawnthingondamage) | Object  | Specifies an object that spawns on the tile when the unit takes damage. | 6 | `{ . . . }` |
| [`SpawnEachTurn`](./Passives_and_Statuses.md#object-spawneachturn) | Object  | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 6 | `{ . . . }` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object | Applies the contained status effects when the unit changes stances. | 6 | `{ . . . }` |
| `AlphaTurns` | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 6 | `-1`<br>`1` |
| [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#object-addstatustoelementabilities) | Object | Adds the contained status effects to all abilities with the specified element. | 6 | `{ . . . }` |
| `BasicAttackDamageMultiplier` | Float | A multiplier applied to the damage of the basic attack. | 6 | `0`<br>`33.333334%`<br>`50%` |
| [`ReplaceBasicAttackWhenCastable`](../Reference_and_Meta/Enums.md#enum-replacebasicattackwhencastable) | Enum | Replaces the basic attack with the specified ability when that ability can be cast. | 6 | `BasicSuplex`<br>`Hone`<br>`Hone2` |
| `ExtraWeaponAttacks` | Integer | The number of additional weapon attacks the unit can perform. | 6 | `1`<br>`2` |
| [`BoostWeaponDamage`](./Passives_and_Statuses.md#object-boostweapondamage) | Integer / Object  | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 6 | `{ . . . }`<br>`1`<br>`2`<br>`5` |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#object-addstatustoweapons) | Object  | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 6 | `{ . . . }` |
| [`ManaCostReductionTagged`](./Passives_and_Statuses.md#object-manacostreductiontagged) | Object | Reduces the mana cost of abilities with the specified tag by the given reduction amount. | 6 | `{ . . . }` |
| `ExtraMovePoints` | Integer | The number of additional movement points granted to this unit. | 6 | `1` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 5 | `-1`<br>`-2`<br>`1` |
| `AddManaRegen` | Integer | The flat amount of mana regenerated per turn. | 5 | `1`<br>`2`<br>`3` |
| [`ReplaceBasicMove`](../Reference_and_Meta/Enums.md#enum-replacebasicmove) | Enum  | Specifies an alternative movement ability that replaces the unit's default move. | 5 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |
| [`AddStatusToAllDamage`](./Passives_and_Statuses.md#object-addstatustoalldamage) | Object | Adds the contained status effects to all damage dealt by the unit. | 5 | `{ . . . }` |
| [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#object-addstatustobasicmeleeattack) | Object  | An object listing status effects applied by the unit's basic melee attack. | 5 | `{ . . . }` |
| [`StatusOnOverHealed`](./Passives_and_Statuses.md#object-statusonoverhealed) | Object | An object that applies a status effect to the unit whenever it receives overhealing (healing beyond max health). | 5 | `{ . . . }` |
| `AddBonusMeleeRange` | Integer | The number of additional tiles of range added to the unit's melee attacks. | 5 | `1`<br>`10`<br>`2` |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#object-statusoncastspell) | Object  | An object listing status effects applied to the unit whenever it casts a spell. | 5 | `{ . . . }` |
| `BasicAttackAOEBonus` | Integer | The additional area of effect radius for the basic attack. | 5 | `1`<br>`2` |
| [`AbilityReaction`](./Passives_and_Statuses.md#object-abilityreaction) | Enum / Object  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 4 | `{ . . . }`<br>`AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| `AddLevelUpRerolls` | Integer | The number of additional rerolls the unit gets when leveling up. | 4 | `1`<br>`2`<br>`3` |
| `BoostHeals` | Integer | The number of stacks that increase healing received or dealt. | 4 | `-2`<br>`1`<br>`2` |
| `BackstabCritChance` | Integer | A multiplier for critical hit chance on backstab attacks. | 4 | `.25`<br>`1` |
| `MakeSpellsRequireCharge` | Integer | If true, spells require a charge-up turn before casting. | 4 | `1` |
| [`AllyBonusAbilityAura`](./Passives_and_Statuses.md#object-allybonusabilityaura) | Enum / Object | Specifies an ability name granted to adjacent allies in an aura, optionally with a square radius. | 4 | `{ . . . }`<br>`NubbyToss` |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 4 | `-1`<br>`-2`<br>`1` |
| [`SpawnThingOnDeath`](../Reference_and_Meta/Enums.md#enum-spawnthingondeath) | Enum  | Specifies the name of an object to spawn upon death. | 4 | `Boulder`<br>`CharmedDemonKitten`<br>`CharmedFlySwarm` |
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 4 | `1` |
| [`AutocastEachRound`](./Passives_and_Statuses.md#object-autocasteachround) | Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 | `{ . . . }` |
| `IncreaseExplosionDamage` | Integer | The flat amount by which explosion damage is increased. | 4 | `1`<br>`2`<br>`3` |
| [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#object-passiveathealththreshold) | Object | An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives. | 4 | `{ . . . }` |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 4 | `{ . . . }` |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#object-statusifunusedmovepoints) | Object  | Specifies status effects applied if the unit ends its turn with unused movement points. | 4 | `{ . . . }` |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#object-addstatustoelementdamage) | Object | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 | `{ . . . }` |
| `FreezePiercing` | Integer | The number of stacks of freeze resistance that are ignored when applying freeze. | 4 | `1` |
| [`LevelUpClassOverride`](../Reference_and_Meta/Enums.md#enum-levelupclassoverride) | Enum | Specifies which class the unit gains upon leveling up, overriding the default class. | 4 | `Colorless`<br>`Jester` |
| [`AddPassivesToCharmed`](./Passives_and_Statuses.md#object-addpassivestocharmed) | Object | Grants the contained passive effects to units under the charm status. | 4 | `{ . . . }` |
| [`StatusOnTurnEndIfCastNSpells`](./Passives_and_Statuses.md#object-statusonturnendifcastnspells) | Object | An object that applies a status effect at the end of the turn if the unit has cast a specified number of spells. | 4 | `{ . . . }` |
| `AddDamageToBasicAttack` | Integer | Additional damage added to the basic attack, either as a flat value or formula. | 4 | `1`<br>`2`<br>`4` |
| [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#object-passivewhenatfullmana) | Object  | An object listing passive effects that are active only while the unit's mana is full. | 4 | `{ . . . }` |
| [`AllyManaRegenAura`](./Passives_and_Statuses.md#object-allymanaregenaura) | Object | An object granting a mana regeneration aura to allies, with sub-keys for stacks and range. | 4 | `{ . . . }` |
| [`StatusOnTurnEndIfManaExact`](./Passives_and_Statuses.md#object-statusonturnendifmanaexact) | Object | An object that applies a status effect at the end of the turn if the unit's mana is exactly a specified value. | 4 | `{ . . . }` |
| [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#object-statusonturnendifmanaorhealthexact) | Object | An object that applies a status effect at the end of the turn if the unit's mana or health is exactly a specified value. | 4 | `{ . . . }` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 4 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 4 | `1`<br>`2`<br>`[1, 0.1]` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`10`<br>`2` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 3 | `1`<br>`2`<br>`3` |
| `Slow` | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 3 | `-1`<br>`1`<br>`2` |
| [`DeathRattle`](./Passives_and_Statuses.md#object-deathrattle) | Enum / Object  | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 3 | `{ . . . }`<br>`BBExplode`<br>`BloatyExplodey`<br>`BombFlyExplode` |
| [`StatusOnBattleStart`](./Passives_and_Statuses.md#object-statusonbattlestart) | Object | An object containing status effects to apply to the unit at the start of every battle. | 3 | `{ . . . }` |
| [`AddTag`](../Reference_and_Meta/Enums.md#enum-addtag) | Enum  | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 3 | `bug`<br>`cat`<br>`fetus` |
| [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#object-movetowardsdamagesource) | Object  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 3 | `{ . . . }` |
| [`StatusOnKillEnemy`](./Passives_and_Statuses.md#object-statusonkillenemy) | Object | Specifies the effects applied when the unit kills an enemy. | 3 | `{ . . . }` |
| `TrinketPassiveMultiplierBonus` | Integer | Bonus multiplier to the passive effects of equipped trinkets. | 3 | `1`<br>`2` |
| [`StatusOnTookDamageFromAbility`](./Passives_and_Statuses.md#object-statusontookdamagefromability) | Object  | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 3 | `{ . . . }` |
| `TrinketActiveEffectsMultiplierBonus` | Integer | Bonus multiplier to the active effects of equipped trinkets. | 3 | `1`<br>`2` |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#object-statusonallycatdeath) | Object  | An object listing status effects applied to the unit when an allied cat dies. | 3 | `{ . . . }` |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#object-statusoneatfood) | Object  | An object listing status effects applied to the unit when it eats food. | 3 | `{ . . . }` |
| [`StatusKilledCharacters`](./Passives_and_Statuses.md#object-statuskilledcharacters) | Object  | An object listing status effects applied to the unit when it kills a character. | 3 | `{ . . . }` |
| [`AutocastEachTurnBegin`](./Passives_and_Statuses.md#object-autocasteachturnbegin) | Enum / Object | Specifies the ability automatically cast at the start of each turn, optionally with chance and polarity. | 3 | `{ . . . }`<br>`MindCrack_EldritchVisage`<br>`MindCrack_EldritchVisage2` |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`5` |
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 3 | `1` |
| [`TileTrail`](../Reference_and_Meta/Enums.md#enum-tiletrail) | Enum  | Specifies the type of tile left behind as the unit moves. | 3 | `BrambleTile`<br>`CreepTile`<br>`FireTile` |
| [`AddSelfStatusToBasicAttack`](./Passives_and_Statuses.md#object-addselfstatustobasicattack) | Object | Applies the contained status effects to the unit when it uses its basic attack. | 3 | `{ . . . }` |
| [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile) | Object  | Specifies an object that spawns on a random empty tile at the start of battle. | 3 | `{ . . . }` |
| `AddKnockbackDamage` | Integer | The amount of additional knockback damage applied. | 3 | `1`<br>`2`<br>`3` |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#object-statuseveryxspellcasts) | Object  | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 3 | `{ . . . }` |
| [`FreePathfindElement`](../Reference_and_Meta/Enums.md#enum-freepathfindelement) | Enum  | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 3 | `Grass`<br>`Water` |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 3 | `{ . . . }` |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#object-statusongaincoins) | Object  | Specifies status effects applied when this unit gains coins. | 3 | `{ . . . }` |
| `AmplifyKnockback` | Integer | The additional distance (in tiles) a unit is knocked back. | 3 | `10`<br>`2` |
| [`ElementalManaCostReduction`](./Passives_and_Statuses.md#object-elementalmanacostreduction) | Object | An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount. | 3 | `{ . . . }` |
| `AllyDamageReduction` | Integer | The amount by which damage dealt to allies is reduced. | 3 | `0` |
| [`SpawnCatCopyOnBattleStart`](./Passives_and_Statuses.md#object-spawncatcopyonbattlestart) | Object | An object that spawns a copy of the unit's cat at the start of battle, with sub-keys for the copy object and chain-prevention tag. | 3 | `{ . . . }` |
| [`StatusOnHealed`](./Passives_and_Statuses.md#object-statusonhealed) | Object | An object that applies a status effect to the unit whenever it is healed. | 3 | `{ . . . }` |
| `TauntAlways` | Integer | If non-zero, the unit is always taunted, forcing it to target the first enemy in range. | 3 | `1` |
| [`CobraReflex`](../Reference_and_Meta/Enums.md#enum-cobrareflex) | Enum | Specifies which basic attack or ability grants increased dodge or counterattack chance. | 3 | `BasicMonkMelee` |
| `ConsumablesInfiniteRange` | Integer | If non-zero, consumable items can be used at any range without distance restrictions. | 3 | `1` |
| `UncappedMana` | Integer | If non-zero, the unit has no maximum mana limit. | 3 | `1` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 2 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `Weakness` | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 2 | `1` |
| `AddInitiative` | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 2 | `-10`<br>`-100`<br>`-20` |
| [`Dyslexia`](../Reference_and_Meta/Arrays.md#array-dyslexia) | Array | An array [minRange maxRange] defining the random range of spell range swap caused by Dyslexia. | 2 | `[3 5]`<br>`[6 9]` |
| [`OverrideBasicAttack`](../Reference_and_Meta/Enums.md#enum-overridebasicattack) | Enum | Replaces the unit's basic attack with the specified ability. | 2 | `BasicExplosiveShot`<br>`BasicMelee`<br>`BasicMetronome` |
| `HeadArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to passive effects granted by head armor. | 2 | `1`<br>`2` |
| `BasicAttackCritChance` | Integer | A multiplier for the critical hit chance of basic attacks, either as a float or percentage. | 2 | `.1`<br>`100%` |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](../Reference_and_Meta/Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Specifies the name of the ability the unit will move and attempt to use at the start of each of its turns. | 2 | `Cannibalize`<br>`EatShit`<br>`face_EatNeverstone` |
| `NubbyTossPriority` | Integer | Determines the priority order for the Nubby Toss action relative to other available actions. | 2 | `1` |
| [`AutocastEachTurn`](../Reference_and_Meta/Enums.md#enum-autocasteachturn) | Enum | Specifies the ability automatically cast at the end of each turn. | 2 | `DarkOneStrike`<br>`ViolentOutburst` |
| `ChangeTauntPriority` | Integer | The amount to adjust the unit's taunt priority, affecting enemy targeting. | 2 | `-1` |
| [`StatsAtLowHealth`](./Passives_and_Statuses.md#object-statsatlowhealth) | Object | An object containing a 'threshold' (health value) and stat bonuses (e.g., 'strength', 'speed') that are applied when the unit's health is below the threshold. | 2 | `{ . . . }` |
| [`TaggedPickupEffectReplacement`](./Passives_and_Statuses.md#object-taggedpickupeffectreplacement) | Object | Specifies a replacement effect for picking up items with a given tag. | 2 | `{ . . . }` |
| `Metal` | Integer | The number of armor stacks or metal keyword effects. | 2 | `1` |
| [`CounterAttack`](../Reference_and_Meta/Enums.md#enum-counterattack) | Enum  | Specifies the ability used when the unit counterattacks after being hit. | 2 | `BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| `WaterWalk` | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 2 | `1` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | `1` |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 2 | `{ . . . }` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 2 | `1`<br>`2`<br>`3` |
| [`MovementReaction`](./Passives_and_Statuses.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 2 | `{ . . . }` |
| `Stealth` | Integer | The number of stealth stacks applied. | 2 | `1`<br>`2`<br>`[1 .1]` |
| [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#object-statusalliesonbattlestart) | Object | An object containing status effects to apply to all allies at the start of battle. | 2 | `{ . . . }` |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 2 | `{ . . . }` |
| [`ChanceToRevive`](./Passives_and_Statuses.md#object-chancetorevive) | Integer / Object | The percentage chance or an object defining chance, health, and statuses on revival. | 2 | `{ . . . }`<br>`100`<br>`25` |
| `DebuffImmunity` | Integer | If 1, the unit is immune to debuffs. | 2 | `1` |
| [`SecurityBotProtect`](./Passives_and_Statuses.md#object-securitybotprotect) | Object  | Specifies the ability and movement used by a security bot to protect allies. | 2 | `{ . . . }` |
| [`CatchProjectiles`](./Passives_and_Statuses.md#object-catchprojectiles) | Object | An object defining chance to catch projectiles and optionally apply statuses. | 2 | `{ . . . }` |
| [`ClassManaCostReduction`](./Passives_and_Statuses.md#object-classmanacostreduction) | Object  | Defines a reduction in mana cost for abilities of a specific class. | 2 | `{ . . . }` |
| `IncreaseExplosionSize` | Integer | The number of extra tiles added to the radius of explosions. | 2 | `1`<br>`2`<br>`7` |
| `AddStartingMana` | Integer | The amount of bonus mana the unit starts each battle with. | 2 | `20`<br>`5` |
| [`AfterImage`](../Reference_and_Meta/Enums.md#enum-afterimage) | Enum  | Specifies the object or skill used to create an afterimage of the unit. | 2 | `PlayerCat_ThiefShade`<br>`PlayerCat_ThiefShade2` |
| `Conductor` | Integer | The number of times the Conduct effect is applied. | 2 | `2` |
| [`AddHiddenTag`](../Reference_and_Meta/Enums.md#enum-addhiddentag) | Enum  | A hidden tag applied to the unit for internal logic and triggers. | 2 | `bowling_ball`<br>`grown_hitler_clone`<br>`hitler_clone_fetus` |
| `FaceShield` | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 2 | `0`<br>`1` |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 2 | `{ . . . }` |
| [`SpawnObjectOnPopCorpse`](../Reference_and_Meta/Enums.md#enum-spawnobjectonpopcorpse) | Enum | Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped. | 2 | `Catnip`<br>`Coin`<br>`Food` |
| `AddSpellDamage` | Integer | The flat amount of spell damage added to all spell attacks. | 2 | `1`<br>`2` |
| `ChainKnockback` | Integer | If 1, enables knockback to chain to additional targets. | 2 | `1` |
| `DirtyClaws` | Integer | The number of additional damage instances from Dirty Claws on attack. | 2 | `1` |
| [`EMP`](./Passives_and_Statuses.md#object-emp) | Object | Defines the EMP effect, including spell graphics override for pulsed area damage. | 2 | `{ . . . }` |
| [`EnergyStorm`](./Passives_and_Statuses.md#object-energystorm) | Integer / Object | The period or definition for the Energy Storm, dealing periodic damage in an area. | 2 | `{ . . . }`<br>`3` |
| [`GravityWell`](./Passives_and_Statuses.md#object-gravitywell) | Object | Specifies the damage and effect applied to units pulled into a gravity well. | 2 | `{ . . . }` |
| [`LateBloomer`](./Passives_and_Statuses.md#object-latebloomer) | Object | Specifies the stats gained after a set number of turns or stacks. | 2 | `{ . . . }` |
| `Quiver` | Integer | Grants additional ammunition capacity or reload charges for ranged weapon abilities, increasing how many times they can be fired. | 2 | `1`<br>`2` |
| [`TowerDefense`](./Passives_and_Statuses.md#object-towerdefense) | Object | Specifies the range and damage of the Tower Defense counterattack. | 2 | `{ . . . }` |
| [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#object-extrastatuswhendealingdamage) | Object | Defines additional statuses applied to the target or source when dealing damage, with conditionals. | 2 | `{ . . . }` |
| [`StatusOnPopCorpse`](./Passives_and_Statuses.md#object-statusonpopcorpse) | Object | Specifies the effects applied when the unit pops a corpse. | 2 | `{ . . . }` |
| [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear) | Object  | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 2 | `{ . . . }` |
| [`Eternal`](./Passives_and_Statuses.md#object-eternal) | Object | Defines the Eternal revival effect, setting stacks and the health percentage restored. | 2 | `{ . . . }` |
| [`InfiniteRebirth`](./Passives_and_Statuses.md#object-infiniterebirth) | Object  | Specifies the health and effects for unlimited rebirth upon death. | 2 | `{ . . . }` |
| [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement) | Object | Defines the elemental effects (Fire, Ice, etc.) applied by the attunement. | 2 | `{ . . . }` |
| `Empath` | Integer | The percentage of damage shared with nearby allies from the Empath disorder. | 2 | `100%`<br>`50%` |
| `ShoulderCheck` | Integer | The chance (as a percentage) to perform a Shoulder Check, pushing a target back after a melee attack. | 2 | `100%`<br>`33%` |
| [`ShovingMatch`](../Reference_and_Meta/Enums.md#enum-shovingmatch) | Enum | Determines which stat (e.g., 'attack') is used for the Shoving Match shoving contest. | 2 | `attack` |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Passives_and_Statuses.md#object-applystatusestorandomenemieseachturn) | Object | An object specifying statuses to apply to random enemies each turn, with an optional 'count' field. | 2 | `{ . . . }` |
| `AutoEquipConsumables` | Integer | The number of consumables automatically equipped per turn. | 2 | `1` |
| [`ChanceToBlockAndCounter`](./Passives_and_Statuses.md#object-chancetoblockandcounter) | Equation / Object | The percentage chance or an object defining chance and conditions to block and counter an attack. | 2 | `15%`<br>`25%`<br>`33%` |
| [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#object-damageneighborsaftermove) | Object | Defines the spell damage and effects applied to neighboring tiles after the unit moves. | 2 | `{ . . . }` |
| `FlowersOnEndTurn` | Integer | The number of flowers spawned on the unit's tile at the end of each turn. | 2 | `1`<br>`3`<br>`4` |
| `IncreaseSpellRange` | Integer | The number of extra tiles added to the range of spells. | 2 | `10`<br>`2`<br>`20` |
| [`KillsToMeat`](../Reference_and_Meta/Enums.md#enum-killstomeat) | Enum | Specifies the type of meat item spawned when killing certain enemies. | 2 | `Food` |
| [`PassiveAfterXKills`](./Passives_and_Statuses.md#object-passiveafterxkills) | Object | Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key. | 2 | `{ . . . }` |
| [`ProtectTargetedAllies`](../Reference_and_Meta/Enums.md#enum-protecttargetedallies) | Enum  | Specifies the ability used to protect targeted allies, including an optional target filter. | 2 | `SwapPositions_WideLoad`<br>`SwapPositions_WideLoad2` |
| `RangedTrueShot` | Integer | Ranged attacks cannot miss or be dodged, guaranteeing a hit. Value acts as a binary flag. | 2 | `1` |
| [`StatusAfterCastSpell`](./Passives_and_Statuses.md#object-statusaftercastspell) | Object | An object containing status effects to apply to the unit immediately after it casts any spell. | 2 | `{ . . . }` |
| [`StatusOnBreakItem`](./Passives_and_Statuses.md#object-statusonbreakitem) | Object | An object containing status effects to apply when the unit breaks a weapon or armor item. | 2 | `{ . . . }` |
| `AddUnfilledMaxHealth` | Integer | The amount of maximum health added, but not healed (the health bar remains at its current level). | 2 | `10`<br>`20`<br>`50` |
| `FlyDamageIncrease` | Integer | The number of stacks or alias for damage increase against flying units. | 2 | `1`<br>`4` |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 | `{ . . . }` |
| `UncappedHP` | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 2 | `1` |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#object-addstatustoexplosions) | Object | An object whose nested keys define statuses applied to explosion damage. | 2 | `{ . . . }` |
| `DukeOfFlies` | Integer | The number of flies spawned when the unit dies. | 2 | `1` |
| [`EscapeSequence`](./Passives_and_Statuses.md#object-escapesequence) | Object | Defines an escape sequence with safe explosion displacement and random distance displacement. | 2 | `{ . . . }` |
| [`FollowUp`](../Reference_and_Meta/Enums.md#enum-followup) | Enum | Specifies the name of the follow-up ability triggered after an attack. | 2 | `FollowUpDash`<br>`FollowUpDash2` |
| `FullPower` | Integer | The number of stacks applied per turn while at full health or full mana. | 2 | `3` |
| `ImmortalLeeches` | Integer | The number of leech stacks that persist beyond death. | 2 | `1` |
| `KillsHeal` | Integer | The amount or percentage of health restored on kill. | 2 | `5`<br>`50%` |
| [`LightningRod`](./Passives_and_Statuses.md#object-lightningrod) | Object | Specifies the unit tags and conditions that cause lightning strikes. | 2 | `{ . . . }` |
| [`MegaMinions`](./Passives_and_Statuses.md#object-megaminions) | Integer / Object | The number of extra minions spawned or maximum minion count. | 2 | `{ . . . }`<br>`3` |
| `MetalDetector` | Integer | The number of extra metal drops or scrap found per turn. | 2 | `10`<br>`5` |
| `NumbingLeeches` | Integer | The number of leeches that apply a numbing effect, reducing the target's output or disabling certain actions. Also the name of a Necromancer passive. | 2 | `3` |
| `ShowHiddenThings` | Integer | If nonzero, reveals hidden objects or tiles on the map. | 2 | `1` |
| [`SpecialFriends`](./Passives_and_Statuses.md#object-specialfriends) | Object | An object containing a set of status effects applied to allied units that are considered 'special friends' (e.g., granted by a passive). | 2 | `{ . . . }` |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#object-statusalliesonkill) | Object | An object containing status effects to apply to all allies when any ally kills an enemy. | 2 | `{ . . . }` |
| [`Study`](./Passives_and_Statuses.md#object-study) | Integer / Object | The number of stacks of the Study status applied. | 2 | `{ . . . }`<br>`1` |
| `Vengeful` | Integer | The number of Vengeful stacks, causing retaliation damage when hit. | 2 | `1` |
| [`AddSelfStatusToWeapons`](./Passives_and_Statuses.md#object-addselfstatustoweapons) | Object | An object whose nested keys define status effects applied to the unit's own weapons. | 2 | `{ . . . }` |
| [`BouncyProjectiles`](./Passives_and_Statuses.md#object-bouncyprojectiles) | Object | An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior. | 2 | `{ . . . }` |
| `CCImmunity` | Integer | If set to 1, this unit is immune to crowd control effects. | 2 | `1` |
| `ConsumableEffectsMultiplierBonus` | Integer | A multiplier bonus applied to the effects of consumable items. | 2 | `1` |
| `DoubleCastWeapons` | Integer | The number of additional weapon casts per attack. | 2 | `1`<br>`2` |
| `GainExtraShield` | Integer | The amount of shield gained on turn start. | 2 | `2`<br>`4` |
| [`PassiveWhileInMonkMeleeStance`](./Passives_and_Statuses.md#object-passivewhileinmonkmeleestance) | Object | Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance. | 2 | `{ . . . }` |
| `RemoveLineOfSightRestrictions` | Integer | Line of sight requirements for targeting are ignored, allowing the unit to target any visible cell regardless of obstacles. | 2 | `1` |
| [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#object-scaledstatusonspendmana) | Object | An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent. | 2 | `{ . . . }` |
| `SharePickups` | Integer | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 2 | `1` |
| [`StatusOnCollectPickup`](./Passives_and_Statuses.md#object-statusoncollectpickup) | Object | An object containing status effects to apply when the unit collects a pickup item. | 2 | `{ . . . }` |
| [`StatusOnPickupCoins`](./Passives_and_Statuses.md#object-statusonpickupcoins) | Object | Specifies the effects applied when the unit picks up coins. | 2 | `{ . . . }` |
| [`StatusOnUseBasicAttack`](./Passives_and_Statuses.md#object-statusonusebasicattack) | Object | Specifies the effects applied when the unit performs a basic attack. | 2 | `{ . . . }` |
| [`StatusWhenAllySpendsMana`](./Passives_and_Statuses.md#object-statuswhenallyspendsmana) | Object | Specifies the effects applied when an ally spends mana. | 2 | `{ . . . }` |
| [`TowerDefenseReflex`](../Reference_and_Meta/Enums.md#enum-towerdefensereflex) | Enum  | Specifies the ability or attack used when the unit counterattacks in tower defense reflex mode. | 2 | `BasicRanged_1DMG`<br>`attack` |
| `UpgradeSpawnedPickups` | Integer | The number of times spawned pickups are upgraded in quality. | 2 | `1`<br>`2` |
| `WeaponDamageMultiplierBonus` | Integer | Bonus multiplier to weapon damage. | 2 | `1`<br>`2` |
| [`AddStatusToTrampleDamage`](./Passives_and_Statuses.md#object-addstatustotrampledamage) | Object | An object whose nested keys define statuses applied to trample damage. | 2 | `{ . . . }` |
| `BraceForEachNeighboringEnemy` | Integer | The number of Brace stacks gained for each adjacent enemy. | 2 | `1`<br>`2` |
| `CharmAllFlies` | Integer | If 1, charms all fly-type enemies, causing them to become allies. | 2 | `1` |
| [`DamageReductionAura`](./Passives_and_Statuses.md#object-damagereductionaura) | Object | Defines an aura that reduces incoming damage, with range, ally-only, and stack settings. | 2 | `{ . . . }` |
| `DeathChill` | Integer | The number of Chill stacks applied to the killer upon death. | 2 | `1` |
| `DejaVu` | Integer | The percentage chance or definition for the DejaVu disorder, causing repeated events. | 2 | `10%` |
| [`LowHealthAllyDodgeChanceAura`](./Passives_and_Statuses.md#object-lowhealthallydodgechanceaura) | Object | Specifies the health threshold and dodge chance granted to nearby low-health allies. | 2 | `{ . . . }` |
| [`StatusKillers`](./Passives_and_Statuses.md#object-statuskillers) | Object  | An object containing nested conditionals that apply status effects when the unit kills an enemy. | 2 | `{ . . . }` |
| `StrengthForEachNeighboringEnemy` | Integer | The amount of strength gained for each adjacent enemy. | 2 | `2`<br>`3` |
| `AbsorbManaAura` | Integer | The amount of mana absorbed from nearby enemies each turn. | 2 | `1` |
| [`AddPassiveToSpawnedRocks`](./Passives_and_Statuses.md#object-addpassivetospawnedrocks) | Object | An object whose nested keys define passives applied to rocks spawned by the unit. | 2 | `{ . . . }` |
| [`AddPassivesToSummonAbilityMinions`](./Passives_and_Statuses.md#object-addpassivestosummonabilityminions) | Object | An object whose nested keys define passives applied to minions summoned by abilities. | 2 | `{ . . . }` |
| [`AddStatusToBasicAttackWithCooldown`](./Passives_and_Statuses.md#object-addstatustobasicattackwithcooldown) | Object | An object whose nested keys define statuses applied to basic attacks, subject to a cooldown. | 2 | `{ . . . }` |
| [`AddStatusToFirstBasicAttack`](./Passives_and_Statuses.md#object-addstatustofirstbasicattack) | Object | An object whose nested keys define statuses applied only to the unit's first basic attack. | 2 | `{ . . . }` |
| [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#object-addstatustomeleedamage) | Object | An object whose nested keys define statuses applied to melee damage. | 2 | `{ . . . }` |
| `AddWeaponScaling` | Integer | The amount of scaling added to damage based on the weapon's stats. | 2 | `1` |
| `AllowPassTurn` | Integer | If set to 1, the unit can skip its turn. If 0, it cannot. | 2 | `0`<br>`1` |
| [`AllyDamageReaction`](../Reference_and_Meta/Enums.md#enum-allydamagereaction) | Enum | Specifies the ability to use when an ally takes damage, such as 'attack'. | 2 | `attack` |
| [`AllyHealthRegenAura`](./Passives_and_Statuses.md#object-allyhealthregenaura) | Object | An object defining an aura that grants health regeneration to allies, typically with 'stacks' and 'range' fields. | 2 | `{ . . . }` |
| [`AllyMoveAbilityAura`](../Reference_and_Meta/Enums.md#enum-allymoveabilityaura) | Enum | Determines the movement ability granted to allies within an aura. | 2 | `CatapultJump`<br>`CatapultJump2` |
| `AllyMultiplyKnockbackDamage` | Integer | A multiplier for knockback damage dealt to allies. | 2 | `2` |
| [`AlternateCraftingPools`](./Passives_and_Statuses.md#object-alternatecraftingpools) | Object | An object mapping crafting pool categories to alternate pools for the unit. | 2 | `{ . . . }` |
| `AmplifyPositiveStatus` | Integer | The number of stacks that amplify the intensity of positive statuses on allies. | 2 | `1`<br>`2` |
| `AutoCritLowDamage` | Integer | The amount of damage below which attacks automatically critically strike. | 2 | `2`<br>`3` |
| `BasicAttackStatusCarefulness` | Integer | The number of stacks of Carefulness applied by basic attacks. | 2 | `1` |
| `BonusFoodEachBattle` | Integer | The amount of bonus food earned at the end of each battle. | 2 | `2`<br>`20` |
| [`BoobyTrapItems`](./Passives_and_Statuses.md#object-boobytrapitems) | Object | An object defining effects to apply when items are thrown or broken. | 2 | `{ . . . }` |
| `BoostAllyStatsOnDeath` | Integer | The number of stacks that boost ally stats when this unit dies. | 2 | `1`<br>`2` |
| `CapDamageFromAllies` | Integer | The maximum amount of damage the unit can take from allies per hit. | 2 | `1` |
| [`CatAPultAnimation`](./Passives_and_Statuses.md#object-catapultanimation) | Object | An object specifying the ability and animation used for the CatAPult passive. | 2 | `{ . . . }` |
| `CoinsAddDamage` | Integer | The amount of damage added based on the number of coins the unit has. | 2 | `1`<br>`2` |
| [`CollectPickupsOnBattleEnd`](./Passives_and_Statuses.md#object-collectpickupsonbattleend) | Integer / Object | The number of pickups automatically collected from corpses on the battlefield when the battle ends. | 2 | `{ . . . }`<br>`1` |
| `ConjureCastSpellsForAllies` | Integer | The number of additional spells conjured for allies when casting. | 2 | `1`<br>`2` |
| `DamageEnemiesOnHeal` | Integer | The amount of damage dealt to enemies whenever the unit is healed. | 2 | `1`<br>`2` |
| `DamageEnemiesOnKill` | Integer | The amount of damage dealt to enemies whenever the unit kills an enemy. | 2 | `1`<br>`2` |
| [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#object-damageneighbortileswhencastspell) | Object | Defines the spell damage and effects applied to neighbor tiles when a spell is cast. | 2 | `{ . . . }` |
| `EnemiesGetPickupsKnockedOut` | Integer | The number of pickups knocked out of enemies when they are defeated. | 2 | `1`<br>`2` |
| `EquipmentPassiveMultiplierBonus` | Integer | A multiplier bonus applied to passive effects from equipment. | 2 | `1` |
| `EquipmentSetBonusBonus` | Integer | The number of additional set bonuses granted from equipment. | 2 | `1`<br>`2` |
| `ExplodeOverkilledEnemies` | Integer | The number of explosions caused by overkilled enemies. | 2 | `1`<br>`2` |
| `FamiliarSecondaryDamageImmunity` | Integer | If non-zero, grants immunity to secondary damage sources for familiars. | 2 | `1` |
| `FlowerPowerAuraBrace` | Integer | The amount of brace (defense) granted by the Flower Power aura. | 2 | `1` |
| `FlowerPowerAuraStrength` | Integer | The amount of strength (attack) granted by the Flower Power aura. | 2 | `1` |
| `FullHealthCritChance` | Integer | The additional critical hit chance percentage when at full health. | 2 | `100` |
| `HealDamagesEnemies` | Integer | If true, healing actions also damage enemies by this amount. | 2 | `1` |
| `HealsAlsoRegenMana` | Integer | The percentage or amount of mana regenerated whenever healing is applied. | 2 | `2`<br>`50%` |
| `HealsCanRevive` | Integer | The number of times per battle healing can revive a fallen ally. | 2 | `1`<br>`3` |
| [`HolyShieldTransferToTaggedMinions`](../Reference_and_Meta/Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | Specifies the tag of minions that receive holy shield on the owner's death. | 2 | `any`<br>`crow` |
| `IncreaseHealingSpellRange` | Integer | The number of extra tiles added to the range of healing spells. | 2 | `2` |
| `LightningAspectCharge` | Integer | The number of charges gained that enhance the next lightning attack. | 2 | `0`<br>`1` |
| `LineOfSightTrueSightAura` | Float | The multiplier or chance for line of sight true sight aura to reveal hidden units. | 2 | `.5`<br>`0` |
| `LobbedHook` | Integer | The number of hooks that arc over obstacles to pull targets. | 2 | `1`<br>`2` |
| `MakeBasicAttackPassThroughThings` | Integer | If true, basic attacks pass through obstacles and other units. | 2 | `1` |
| `ManaRegenMultiplierIfManaEmpty` | Integer | The multiplier applied to mana regen when mana is empty. | 2 | `2` |
| `MinimumTech` | Integer | The minimum tech level guaranteed when crafting or upgrading. | 2 | `1` |
| `NoReflection` | Integer | The unit's reflected damage effects are disabled. Value acts as a binary flag. | 2 | `1` |
| `OverhealGainsBothShield` | Integer | Any healing beyond maximum health also grants shield points equal to the overheal amount. Value controls the conversion rate. | 2 | `1`<br>`2` |
| `ParasitesArentCursed` | Integer | Parasites attached to the unit are not considered cursed items, preventing negative curse effects. Value is a binary flag. | 2 | `1` |
| [`PassiveAtFullHealth`](./Passives_and_Statuses.md#object-passiveatfullhealth) | Object | Applies a set of passive effects (e.g., mana cost reduction, extra damage taken) only while the unit is at maximum health. | 2 | `{ . . . }` |
| [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#object-passiveatinjurythreshold) | Object | Applies a set of passive effects when the unit's injury level ('injury' sub-key) meets or exceeds the specified 'threshold' using the comparison 'mode'. | 2 | `{ . . . }` |
| [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#object-passiveuntilcastspell) | Object | Applies a set of passive effects (e.g., healing allies each turn) that remain active until the unit casts a spell. | 2 | `{ . . . }` |
| [`PassiveUntilGetKill`](./Passives_and_Statuses.md#object-passiveuntilgetkill) | Object | Applies a set of passive effects (e.g., Holy Damage Blessing with burn) that remain active until the unit scores a kill. | 2 | `{ . . . }` |
| [`PassiveWhenTheAlpha`](./Passives_and_Statuses.md#object-passivewhenthealpha) | Object | Activates a set of passive effects (e.g., TogglableRoundEndExtraTurn) only while the unit holds the Alpha status on the team. | 2 | `{ . . . }` |
| [`PassiveWhileInMonkRangedStance`](./Passives_and_Statuses.md#object-passivewhileinmonkrangedstance) | Object | Applies specific passive effects (e.g., AddBonusRange, AddSpellDamage) while the unit is in the Monk's ranged combat stance. | 2 | `{ . . . }` |
| [`PassiveWhilePreviewingMonkRangedStance`](./Passives_and_Statuses.md#object-passivewhilepreviewingmonkrangedstance) | Object | Applies specific passive effects (e.g., AddBonusRange) while the unit is previewing the Monk's ranged stance before committing to it. | 2 | `{ . . . }` |
| [`PassiveWhileWearingMetal`](./Passives_and_Statuses.md#object-passivewhilewearingmetal) | Object | Applies a set of passive effects (e.g., AddElementsToWeapon with Electric) while the unit is equipped with metal armor or accessories. | 2 | `{ . . . }` |
| `PermanentItems` | Integer | The number of equipment slots that are immune to being unequipped or removed, permanently binding items to those slots. | 2 | `1`<br>`2` |
| `RemoveOncePerFightRestriction` | Integer | Abilities or effects with a 'once per fight' limitation can be used multiple times per fight. Value acts as a binary flag. | 2 | `1` |
| [`ReplaceBasicAttackWhenDead`](../Reference_and_Meta/Enums.md#enum-replacebasicattackwhendead) | Enum | Specifies the ability (e.g., Haunt) that replaces the unit's basic attack when it is in a dead state. | 2 | `Haunt` |
| `ReviveOnWin` | Integer | Chance (as a percentage) for the unit to automatically revive after the battle ends, if it was dead at the time of victory. | 2 | `100%` |
| `RobotsInheritArmor` | Integer | Robots summoned or controlled by the unit inherit a percentage of the unit's armor value. Value controls the inheritance amount. | 2 | `1`<br>`2` |
| `RockDetector` | Integer | Grants the ability to detect or sense rock-type objects or terrain within the specified range (e.g., 10 tiles). | 2 | `10` |
| [`ScaledStatusOnOverMana`](./Passives_and_Statuses.md#object-scaledstatusonovermana) | Object | An object containing status effect definitions to apply when the unit gains mana that exceeds its maximum mana, with the number of stacks scaled by the amount of over-mana. | 2 | `{ . . . }` |
| `ShareHealthRegen` | Integer | The amount of health regeneration shared with nearby allies. | 2 | `1` |
| `SmallEnemiesIgnoreYou` | Integer | If non-zero, enemies considered 'small' will ignore this unit and not target it. | 2 | `1` |
| [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#object-smiteenemieswhokill) | Object | An object defining a smite effect applied to enemies who kill another unit, typically dealing damage and applying a stun. | 2 | `{ . . . }` |
| `SplittableMove` | Integer | The number of times a move action can be split into smaller segments. | 2 | `1`<br>`3` |
| `SpreadExtraDebuffs` | Integer | The number of additional debuffs to spread to nearby enemies when applying a debuff. | 2 | `1`<br>`2` |
| `SpreadPainBonus` | Integer | The amount of bonus damage dealt to enemies who are also affected by the Spread Pain effect. | 2 | `2` |
| `StatMinimum` | Integer | The minimum value that a particular stat cannot fall below. | 2 | `5`<br>`7` |
| [`StatusAlliesOnGainCoins`](./Passives_and_Statuses.md#object-statusalliesongaincoins) | Object | An object containing status effects to apply to allies when the unit gains coins, with an optional 'scaled' boolean to scale stacks. | 2 | `{ . . . }` |
| [`StatusAllyWhenAllySpendsMana`](./Passives_and_Statuses.md#object-statusallywhenallyspendsmana) | Object | An object with a 'threshold' (mana amount) and status effects to apply to an ally whenever any ally spends at least that much mana. | 2 | `{ . . . }` |
| [`StatusAnyCatAllyWhoKills`](./Passives_and_Statuses.md#object-statusanycatallywhokills) | Object | An object containing status effects to apply to any cat ally who kills an enemy. | 2 | `{ . . . }` |
| [`StatusDamagers`](./Passives_and_Statuses.md#object-statusdamagers) | Object | An object defining status effects that damage the unit, with parameters for each status. | 2 | `{ . . . }` |
| [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#object-statuseachturnendperenemykill) | Object | An object containing status effects to apply at the end of each turn for each enemy killed during that turn. | 2 | `{ . . . }` |
| [`StatusEnemiesOnDeath`](./Passives_and_Statuses.md#object-statusenemiesondeath) | Object | An object containing status effects to apply to all enemies when the unit dies. | 2 | `{ . . . }` |
| [`StatusEveryXTurnBegins`](./Passives_and_Statuses.md#object-statuseveryxturnbegins) | Object | An object with a 'turns' value defining status effects applied every X turns at the start of the turn. | 2 | `{ . . . }` |
| [`StatusOnAnyDeath`](./Passives_and_Statuses.md#object-statusonanydeath) | Object | An object containing status effects to apply whenever any unit (ally or enemy) dies. | 2 | `{ . . . }` |
| [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#object-statusonbattleendifkillthresholdmet) | Object | An object containing a 'kills' threshold and status effects to apply at the end of battle if the unit's kill count meets or exceeds the threshold. | 2 | `{ . . . }` |
| [`StatusOnDealtDamage`](./Passives_and_Statuses.md#object-statusondealtdamage) | Object | An object containing status effects to apply to the unit whenever it deals damage to an enemy. | 2 | `{ . . . }` |
| [`StatusOnDealtDamageThreshold`](./Passives_and_Statuses.md#object-statusondealtdamagethreshold) | Object | Specifies the effects applied when the unit deals damage equal to or exceeding the defined threshold. | 2 | `{ . . . }` |
| [`StatusOnGainShield`](./Passives_and_Statuses.md#object-statusongainshield) | Object | Specifies the effects applied when the unit gains a shield. | 2 | `{ . . . }` |
| [`StatusOnHeal`](./Passives_and_Statuses.md#object-statusonheal) | Object | Specifies the effects applied when the unit receives healing. | 2 | `{ . . . }` |
| [`StatusOnOverMana`](./Passives_and_Statuses.md#object-statusonovermana) | Object | Specifies the effects applied when the unit's mana exceeds its maximum. | 2 | `{ . . . }` |
| [`StatusOnTookDamageFromEnemyAbility`](./Passives_and_Statuses.md#object-statusontookdamagefromenemyability) | Object | Specifies the effects applied when the unit takes damage from an enemy ability. | 2 | `{ . . . }` |
| [`StatusOnTriggerTrap`](./Passives_and_Statuses.md#object-statusontriggertrap) | Object | Specifies the effects applied when the unit triggers a trap. | 2 | `{ . . . }` |
| [`StatusOnUseElementAbility`](./Passives_and_Statuses.md#object-statusonuseelementability) | Object | Specifies the effects applied when the unit uses an ability matching the specified element. | 2 | `{ . . . }` |
| [`StatusPerInjury`](./Passives_and_Statuses.md#object-statusperinjury) | Object | Specifies the effects granted per injury the unit has, up to an optional cap. | 2 | `{ . . . }` |
| [`StatusReplacement`](../Reference_and_Meta/Arrays.md#array-statusreplacement) | Array | Specifies status replacements, where the first status is replaced by the second when applied. | 2 | `[Petrify PetrifyCharmed]` |
| [`StatusThingsKnockedBack`](./Passives_and_Statuses.md#object-statusthingsknockedback) | Object | Specifies the effects applied when the unit knocks back another unit. | 2 | `{ . . . }` |
| [`StrengthInNumbersAura`](./Passives_and_Statuses.md#object-strengthinnumbersaura) | Integer / Object | The amount of strength gained per nearby ally within the aura. | 2 | `{ . . . }`<br>`1` |
| [`TileDamageMultiplier`](./Passives_and_Statuses.md#object-tiledamagemultiplier) | Integer / Object | Multiplier for damage dealt to environmental tiles. | 2 | `{ . . . }`<br>`2` |
| `TrapEffectsMultiplier` | Integer | Multiplier for the potency of trap effects triggered by the unit. | 2 | `2` |
| [`UpgradeLevelUpClassActives`](../Reference_and_Meta/Enums.md#enum-upgradelevelupclassactives) | Enum | Specifies the upgrade path for class active abilities on level up. | 2 | `Colorless` |
| [`UpgradeLevelUpClassPassives`](../Reference_and_Meta/Enums.md#enum-upgradelevelupclasspassives) | Enum | Specifies the upgrade path for class passive abilities on level up. | 2 | `Colorless` |
| `WeaponCountsAsBasicAttack` | Integer | If non-zero, the weapon's ability counts as a basic attack. | 2 | `1` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 1 | `0`<br>`1` |
| [`MoveWhenDamaged`](./Passives_and_Statuses.md#object-movewhendamaged) | Object  | Defines movement behavior when the unit takes damage, such as weights and move ability. | 1 | `{ . . . }` |
| `LimitDamage` | Integer | The maximum amount of damage the unit can take from a single hit. | 1 | `1` |
| `DepressionAura` | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 1 | `1`<br>`2` |
| `LimitHeal` | Integer | If 1, prevents the unit from being healed. | 1 | `0`<br>`1` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 1 | `1`<br>`2`<br>`3` |
| `SmallRockBehavior` | Integer | Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed. | 1 | `0`<br>`5` |
| [`Paranoia`](../Reference_and_Meta/Enums.md#enum-paranoia) | Enum | Specifies the type of paranoid melee attack the unit will use instead of their normal attack. | 1 | `ParanoiaBasicMelee` |
| `Vegan` | Integer | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 1 | `1` |
| `OverrideMaxHealth` | Integer | Replaces the unit's maximum health with this value. | 1 | `1`<br>`25` |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 1 | `1` |
| `Triskaidekaphobia` | Integer | The threshold number (typically 13) at which a negative effect triggers due to the disorder Triskaidekaphobia. | 1 | `13` |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Passives_and_Statuses.md#object-statusonturnendifdidntcastabilitytypes) | Object | Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s). | 1 | `{ . . . }` |
| [`BlacklistPickupType`](../Reference_and_Meta/Enums.md#enum-blacklistpickuptype) | Enum  | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 1 | `catnip`<br>`food` |
| [`Diabetes`](./Passives_and_Statuses.md#object-diabetes) | Object | Defines the Diabetes disorder, including its name, description, and associated passive effects. | 1 | `{ . . . }` |
| [`DisableAbilitiesWithTag`](../Reference_and_Meta/Enums.md#enum-disableabilitieswithtag) | Enum  | Specifies a tag that disables any ability with that tag on the unit. | 1 | `consumable`<br>`meat`<br>`musical` |
| `Hypomania` | Integer | When an integer, the stacks of Hypomania; when an object, defines the Hypomania disorder status. | 1 | `3` |
| `Scleroderma` | Integer | If set to 1, the unit's skin becomes hard, reducing damage but also movement. | 1 | `1` |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. | 1 | `-100`<br>`-999`<br>`100` |
| [`TheHunger`](./Passives_and_Statuses.md#object-thehunger) | Object | Defines the Hunger passive, which applies Madness or other effects each turn, representing a disorder. | 1 | `{ . . . }` |
| `WobblyCat` | Integer | The chance (as a percentage) or stack count for the WobblyCat disorder. | 1 | `25%` |
| `BuffImmunity` | Integer | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 1 | `1` |
| `FaceArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the effects of face armor passives. | 1 | `1`<br>`2` |
| [`RandomPassivePool`](./Passives_and_Statuses.md#object-randompassivepool) | Object  | A pool of random passives from which one is chosen for this unit. | 1 | `{ . . . }` |
| [`DisableAbilities`](../Reference_and_Meta/Enums.md#enum-disableabilities) | Enum | Specifies which category of abilities to disable, such as 'all_items' or 'basic_attack'. | 1 | `all_items`<br>`all_spells`<br>`basic_attack` |
| [`PoopWhenHit`](../Reference_and_Meta/Enums.md#enum-poopwhenhit) | Enum  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 1 | `Poop` |
| [`Autism`](./Passives_and_Statuses.md#object-autism) | Object | An object defining the Autism disorder, including its name, description, class, and stat modifications for innate and learned levels. | 1 | `{ . . . }` |
| `SchrodingerDisorder` | Integer | A percentage chance for the unit to be simultaneously alive and dead (Schrödinger's cat) at the start of battle. | 1 | `50%` |
| `NeckArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the passives of the unit's neck armor slot. | 1 | `1`<br>`2` |
| [`SetDefaultFacePassive`](../Reference_and_Meta/Enums.md#enum-setdefaultfacepassive) | Enum | Specifies the name of the default face passive to be assigned to this unit. | 1 | `euphoric`<br>`insane` |
| `SpawnCreepOnHit` | Integer | If set to 1, spawns creep on the tile when this unit takes damage. | 1 | `1` |
| `CanRemoveCursedItems` | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 1 | `1` |
| [`MoveAwayFromDamageSource`](../Reference_and_Meta/Enums.md#enum-moveawayfromdamagesource) | Enum  | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 1 | `BasicJump`<br>`MoveOne` |
| `HouseFoodRequirementMultiplier` | Integer | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 1 | `0` |
| `NoManaRegen` | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 1 | `1` |
| `PermanentImmobile` | Integer | The permanent amount of immobility stacks applied. | 1 | `1` |
| `CapMovementAbilityRange` | Integer | The maximum range allowed for movement abilities. | 1 | `1` |
| `HPGainBlock` | Integer | If true, the unit cannot gain health from any source. | 1 | `1` |
| `MoveSpeedMultiplier` | Float | A multiplier for the unit's movement speed. | 1 | `.5` |
| [`StatusOnEatPill`](./Passives_and_Statuses.md#object-statusoneatpill) | Object | Specifies the effects applied when the unit consumes a pill item. | 1 | `{ . . . }` |
| `WeaponActiveEffectsMultiplierBonus` | Integer | Bonus multiplier to the active effects of the equipped weapon. | 1 | `2` |
| `WeaponPassiveMultiplierBonus` | Integer | Bonus multiplier to the passive effects of the equipped weapon. | 1 | `2` |
| `BoostDamageAura` | Integer | The amount of bonus damage granted to allies within the aura's range. | 1 | `1` |
| `MaxAccuracy` | Integer | The maximum allowed accuracy percentage for the unit. | 1 | `1` |
| `MaxStartingMana` | Integer | The maximum amount of mana the unit starts with. | 1 | `1` |
| `AddAllyNeighborsToAttackRange` | Integer | The number of ally-occupied tiles added to the unit's attack range. | 1 | `1` |
| `AddLevelUpStatMultiplier` | Integer | Multiplier applied to stat gains on level up. | 1 | `1` |
| [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#object-addstatustoreceiveddamage_excludestatuses) | Object | An object defining statuses applied to the attacking unit when the owner receives damage, excluding damage from sources carrying the specified statuses. | 1 | `{ . . . }` |
| [`AddStatusesIfPersistentWeatherElement`](./Passives_and_Statuses.md#object-addstatusesifpersistentweatherelement) | Object | Specifies statuses applied if the persistent weather matches the given elements. | 1 | `{ . . . }` |
| [`AddStatusesToReceivedElementalDamage`](./Passives_and_Statuses.md#object-addstatusestoreceivedelementaldamage) | Object | An object defining statuses applied to the unit when it takes elemental damage of the specified types. | 1 | `{ . . . }` |
| `BackstabWeakness` | Float | A multiplier for damage taken from backstab attacks. | 1 | `0.75` |
| `BoostRangeAura` | Integer | The amount of bonus range (in tiles) granted to allies within the aura's range. | 1 | `1` |
| `CantDodge` | Integer | If set to 1, the unit cannot dodge any incoming attacks. | 1 | `1` |
| [`ConfusionEffectOnTaggedAbilities`](../Reference_and_Meta/Enums.md#enum-confusioneffectontaggedabilities) | Enum | Specifies the type of ability tag (e.g., consumable) that triggers a confusion effect when used. | 1 | `consumable` |
| `ConsumablesMeleeRange` | Integer | Causes consumable items to have a melee range instead of their default range. | 1 | `1` |
| [`DamageIfDidntUseSpecificAbility`](./Passives_and_Statuses.md#object-damageifdidntusespecificability) | Object | Deals a specified amount of damage if the unit did not use a designated ability on its previous turn. | 1 | `{ . . . }` |
| `ExhaustionRoundChange` | Integer | The number of rounds added to the exhaustion counter. | 1 | `3` |
| `ExtraInjuryOnDeath` | Integer | The number of additional injuries inflicted upon death. | 1 | `1` |
| `FreeSpellsAtFullMana` | Integer | The number of spells that cost no mana when mana is full. | 1 | `1` |
| `FrontstabBasicAttackCritChance` | Integer | The percentage chance for basic attacks to critically hit when attacking from the front. | 1 | `100%` |
| [`FurnitureStats`](./Passives_and_Statuses.md#object-furniturestats) | Object | Defines the Comfort, Stimulation, and Appeal stats of furniture. | 1 | `{ . . . }` |
| `InvertBrainFaction` | Integer | If set to 1, inverts the unit's faction (e.g., allies become enemies). | 1 | `1` |
| `LimitSelfKnockbackDamage` | Integer | The maximum amount of damage taken from self-inflicted knockback. | 1 | `1` |
| [`LimitedTileTrail`](../Reference_and_Meta/Enums.md#enum-limitedtiletrail) | Enum | Specifies the type of tile left behind as a trail when the unit moves. | 1 | `FlowerTile` |
| `OverrideMaxMana` | Integer | Sets the unit's maximum mana to this integer value, overriding the default. | 1 | `1` |
| `OverridePalette` | Integer | Forces the unit to use a specific color palette index. | 1 | `87` |
| [`PassiveLevelScaledStatus`](./Passives_and_Statuses.md#object-passivelevelscaledstatus) | Object | An object containing status effects whose values scale with the unit's level, using X as the level variable. | 1 | `{ . . . }` |
| `PermanentKitten` | Integer | If set to 1, the unit retains its kitten form permanently instead of aging. | 1 | `1` |
| `RealTimePressure_OneUnit` | Integer | The amount of real-time pressure (countdown) applied to the unit each turn. | 1 | `5` |
| [`ReceivedStatusReplacement`](../Reference_and_Meta/Arrays.md#array-receivedstatusreplacement) | Array | An array specifying a status that replaces another status when it would be applied (e.g., Sleep becomes SleepParalysis). | 1 | `[Sleep SleepParalysis]` |
| [`ScaledStatusOnBleedDamage`](./Passives_and_Statuses.md#object-scaledstatusonbleeddamage) | Object | An object that applies a scaled status (e.g., Charge) on the unit when they take bleed damage. | 1 | `{ . . . }` |
| [`SelfDamageWhenDealDamage`](./Passives_and_Statuses.md#object-selfdamagewhendealdamage) | Object | An object defining the damage the unit takes to itself whenever it deals damage to an enemy. | 1 | `{ . . . }` |
| [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#object-statusadjacentontheirturnbegin) | Object | Defines a status effect applied to adjacent units when their turn begins, such as forcing them to move away. | 1 | `{ . . . }` |
| [`StatusIfBattleAlreadyBegan`](./Passives_and_Statuses.md#object-statusifbattlealreadybegan) | Object | Defines a status effect that is applied only if the battle has already started (not on the first turn). | 1 | `{ . . . }` |
| [`StatusOnLoseShield`](./Passives_and_Statuses.md#object-statusonloseshield) | Object | Defines a status effect applied to the unit each time it loses a shield point. | 1 | `{ . . . }` |
| [`StatusOnTakeHealthDamage`](./Passives_and_Statuses.md#object-statusontakehealthdamage) | Object | Defines a status effect applied to the unit each time it takes health damage, such as a permanent stat reduction. | 1 | `{ . . . }` |
| `StrictLimitDamage` | Integer | The amount of damage strict limit applies, capping incoming damage to a fixed value per hit. | 1 | `1` |
| `TauntAtFullHealth` | Integer | The number of stacks of Taunt applied to the unit when it is at full health. | 1 | `1` |
| [`TourettesMeows`](./Passives_and_Statuses.md#object-tourettesmeows) | Object | Defines a passive that triggers random vocalizations (hiss, hit, normal) at random cooldown intervals. | 1 | `{ . . . }` |
| [`Robot`](./Passives_and_Statuses.md#object-robot) | Object  | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 1 | `{ . . . }` |
| `ArmorDodgeChance` | Integer | The percentage chance to dodge incoming attacks when wearing this armor. | 1 | `10%`<br>`15%`<br>`20%` |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 1 | `1` |
| `ManaCostReduction` | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 1 | `-2`<br>`1`<br>`2` |
| `InjuryImmunity` | Integer | The number of turns the unit is immune to injuries. | 1 | `1` |
| `BackstabImmunity` | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 1 | `1` |
| [`AddStatusToSpells`](./Passives_and_Statuses.md#object-addstatustospells) | Object  | Specifies status effects added to all spell attacks used by this unit. | 1 | `{ . . . }` |
| `WeaponsDontLoseDurability` | Integer | If set to 1, weapons equipped by this unit do not lose durability. | 1 | `0`<br>`1` |
| [`AddStatusToKnockbackDamage`](./Passives_and_Statuses.md#object-addstatustoknockbackdamage) | Object | An object whose nested keys define statuses applied to damage caused by knockback. | 1 | `{ . . . }` |
| `ExplosionImmunity` | Integer | If non-zero, grants immunity to explosion damage. | 1 | `1` |
| `ExtraTrinketUses` | Integer | The number of additional uses granted to trinkets. | 1 | `1`<br>`10` |
| `Phasing` | Integer | If set to 1, allows the character to phase through solid objects or obstacles. | 1 | `1` |

</details>


---


### Object: `effects`


**Definition:** Applies a list of status effects or visual effects to targets.  
**Total Count:** 2166

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#object-damageneighborsaftermove), [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#object-damageneighborsonendmove), [`GravityWell`](./Passives_and_Statuses.md#object-gravitywell), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage), [`RevengeDamage`](./Passives_and_Statuses.md#object-revengedamage), [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#object-smiteenemieswhokill), [`fire`](./Passives_and_Statuses.md#object-fire), [`ice`](./Passives_and_Statuses.md#object-ice), [`lightning`](./Passives_and_Statuses.md#object-lightning), [`triattack`](./Passives_and_Statuses.md#object-triattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 17 | `Default`<br>`FormChange`<br>`Druid` | `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 624 | Default<br>FormChange<br>Druid |
| [`VisualFXTile`](../Reference_and_Meta/Enums.md#enum-visualfxtile) | Enum  | Specifies the name of the visual effect to play on the target tile. | 12 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 7 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 3 | `1`<br>`2`<br>`[1 .01]` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| `Slow` | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 2 | `-1`<br>`1`<br>`2` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| [`Petrify`](../Reference_and_Meta/Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `1`<br>`2`<br>`3` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| `Weakness` | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| `Immobile` | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |
| `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| `Marked` | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`3`<br>`5` |
| `Leeches` | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `stats`


**Definition:** A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.).  
**Total Count:** 498

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 48 | `-1`<br>`-2`<br>`-3` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 41 | `-1`<br>`-10`<br>`-2` |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 33 | `+1`<br>`-1`<br>`-2` |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 32 | `-1`<br>`-10`<br>`-2` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer | The Strength stat value or modifier. | 31 | `-1`<br>`-2`<br>`-3` |
| [`dex`](../Reference_and_Meta/Enums.md#enum-dex) | Enum / Integer | The Dexterity stat value or modifier. | 23 | `-1`<br>`-2`<br>`-3` |
| [`lck`](../Reference_and_Meta/Enums.md#enum-lck) | Enum / Integer | The Luck stat value or modifier. | 21 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `AddStatusToBasicAttack`


**Definition:** Contains status effects to add to the basic attack.  
**Total Count:** 248

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToCharmed`](./Passives_and_Statuses.md#object-addpassivestocharmed), [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions), [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#object-passivewhenatfullmana), [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 51 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 16 | `Default`<br>`FormChange`<br>`Druid` | `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 45 | Default<br>FormChange<br>Druid |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 12 | `1`<br>`10`<br>`2` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 7 | `1`<br>`10`<br>`2` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 5 | `1`<br>`2`<br>`3` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 5 | `{ . . . }` |
| `Weakness` | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`2`<br>`3` |
| [`BounceObject`](../Reference_and_Meta/Enums.md#enum-bounceobject) | Enum  | Specifies the object or projectile to spawn and bounce from the target. | 4 | `AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`DistanceBonusDamage`](./Passives_and_Statuses.md#object-distancebonusdamage) | Object | An object that adds bonus damage based on the distance from the target, with sub-keys for stacks and minimum range. | 4 | `{ . . . }` |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 3 | `1`<br>`10`<br>`2` |
| `Slow` | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 3 | `-1`<br>`1`<br>`2` |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 3 | `{ . . . }` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 3 | `1`<br>`2` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 3 | `{ . . . }` |
| `Piercing` | Integer | The amount of armor or damage reduction ignored by the attack or ability. | 3 | `1` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`ChangeTile`](./Passives_and_Statuses.md#object-changetile) | Enum / Object  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 2 | `{ . . . }`<br>`BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`[1 .01]` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `MagicWeakness` | Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`3` |
| `Rot` | Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 2 | `-999999`<br>`1`<br>`2` |
| `SoulLink` | Integer | The number of soul link stacks applied. | 2 | `1` |
| [`ApplyStatusIfCrit`](./Passives_and_Statuses.md#object-applystatusifcrit) | Object | Defines effects that are applied only when the attack scores a critical hit. | 2 | `{ . . . }` |
| `BurgleCoin` | Integer | The number of coins stolen from the target, or an array of `[number, probability]`. | 2 | `1`<br>`3`<br>`[1 .5]` |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#object-conditional_shielded) | Object | An object containing effects that are only applied if the target has a shield active. | 2 | `{ . . . }` |
| [`KnockOutCoin`](../Reference_and_Meta/Arrays.md#array-knockoutcoin) | Array / Integer  | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 2 | `1`<br>`[1 .5]` |
| [`Conditional_Adjacent`](./Passives_and_Statuses.md#object-conditional_adjacent) | Object | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 2 | `{ . . . }` |
| `SpawnBearTrapOnMiss` | Integer | The number of bear traps to spawn on the tile adjacent to the target when the unit misses an attack. | 2 | `1` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |
| `Blind` | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 1 | `-1`<br>`1`<br>`2` |
| `Leeches` | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 1 | `1`<br>`2`<br>`3` |
| `OverrideChainKnockback` | Integer | The custom number of tiles for chain knockback, overriding the default. | 1 | `0`<br>`1`<br>`10` |
| `DamageOrHealConditionally` | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 1 | `1` |
| `ManaLeeches` | Integer | The number of mana leech stacks applied. | 1 | `1`<br>`2` |
| `OverrideChainKnockbackDamage` | Equation | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). | 1 | `0`<br>`3+bonus_melee_ability_damage` |
| `SplashDamage` | Integer | The radius (in tiles) for splash damage applied to adjacent targets. | 1 | `1`<br>`2` |
| `BigSplashDamage` | Integer | The additional tile radius of the splash damage effect applied by an attack. | 1 | `2` |
| [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#object-conditional_sourcehastag) | Object | Defines a conditional block that applies effects only if the source of the effect has a specified tag. | 1 | `{ . . . }` |

</details>


---


### Object: `Fire`


**Definition:** Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack.  
**Total Count:** 168

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `Holy`


**Definition:** Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives.  
**Total Count:** 86

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `FlatLeech` | Enum | The flat amount of health restored to the source when dealing damage, applied after the hit. | 2 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid`
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `Else`


**Definition:** Contains the fallback effects to apply when a preceding conditional check fails.  
**Total Count:** 86

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack), [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy), [`CritsApplyStatus`](./Passives_and_Statuses.md#object-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Marked` | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`3`<br>`5` |
| `CaptureFamiliar` | `Number` | The number of times to attempt to capture the target as a familiar. | 2 | `1` |
| `FactionConversion` | `Number` | Converts the target to the caster's faction. | 2 | `1` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | `1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| `TempSpeedUp` | Integer | The number of stacks of temporary Speed Up applied to the unit. | 1 | `10`<br>`4`<br>`X` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Electric`


**Definition:** Applies a Stun status effect with specified stacks and probability based on variable X.  
**Total Count:** 78

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `Wind`


**Definition:** Defines the properties for the Wind element, such as knockback amount.  
**Total Count:** 75

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Equation | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 2 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |

</details>


---


### Object: `ChangeTile`


**Definition:** Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect).  
**Total Count:** 74

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](../Reference_and_Meta/Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 1 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| `aoe` | Integer | The radius (in tiles) of the area affected by the tile change. | 1 | `1` |

</details>


---


### Object: `MeleeRevengeDamage`


**Definition:** Defines the damage and effects applied back to a melee attacker upon being hit.  
**Total Count:** 73

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 6 | Default<br>FormChange<br>Druid |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 7 | `damage_instance`<br>`spell`<br>`self_damage` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>tag |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 4 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 4 | `[`<br>`[Heat Fire]` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| `Weakness` | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 1 | `{ . . . }` |

</details>


---


### Object: `Water`


**Definition:** Form state for water element, applying a puddle or movement bonus.  
**Total Count:** 71

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AOEPuddle` | Equation | Specifies the pattern or shape of an area-of-effect puddle left on the ground. | 2 | `X-1` |

</details>


---


### Object: `Ice`


**Definition:** Applies the Slow status effect to targets hit by ice-element abilities.  
**Total Count:** 61

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `ApplyToSource`


**Definition:** An object of effects that are applied to the source of the ability (the caster).  
**Total Count:** 59

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack), [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 14 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Temporary`


**Definition:** Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions.  
**Total Count:** 57

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll), [`StatusOnGainShield`](./Passives_and_Statuses.md#object-statusongainshield), [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage), [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#object-statusonturnendifmanaorhealthexact)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 11 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 11 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 11 | `{ . . . }` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 6 | `true` |
| `expires_on_begin_turn` | Boolean | If true, the temporary effect expires at the start of the target's turn. | 5 | `true` |

</details>


---


### Object: `StatusEachTurnEnd`


**Definition:** Specifies status effects applied to the unit at the end of each of its turns.  
**Total Count:** 57

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 18 | passives<br>class<br>tag |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 6 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 4 | `-1`<br>`-2`<br>`-4` |
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. | 4 | `1` |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. | 2 | `1` |
| `EmptyMana` | Integer | If non-zero, sets the unit's mana to empty when applied. | 2 | `1` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 1 | `1` |
| [`UseAbility_Madness`](../Reference_and_Meta/Enums.md#enum-useability_madness) | Enum | Determines which ability type (e.g., weapon) is forcibly used when Madness triggers. | 1 | `weapon` |

</details>


---


### Object: `SpawnOnBattleStart`


**Definition:** Specifies the object that spawns adjacent to the unit at the start of battle.  
**Total Count:** 54

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 14 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 13 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnBattleEnd`


**Definition:** An object containing status effects or passives applied to the unit when the battle ends.  
**Total Count:** 53

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 16 | passives<br>class<br>tag |
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 10 | `true` |
| [`CureDisease`](./Passives_and_Statuses.md#object-curedisease) | Object | Attempts to cure the specified disease with the given chance. | 6 | `{ . . . }` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 3 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `RandomPermanentStat` | Integer | The amount of a random permanent stat change (positive or negative). | 3 | `-1`<br>`-2`<br>`-3` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 2 | `1`<br>`3` |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 2 | `-1`<br>`1`<br>`2` |
| [`NextBattleStatus`](./Passives_and_Statuses.md#object-nextbattlestatus) | Object | A set of status effects (e.g., stat buffs, full heal) automatically applied to the unit at the start of the next battle. | 2 | `{ . . . }` |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 1 | `-1`<br>`-2`<br>`1` |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 1 | `-1`<br>`1`<br>`2` |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 1 | `1`<br>`2` |

</details>


---


### Object: `threshold`


**Definition:** The health threshold value, either as a formula using X (max health) or a fixed integer.  
**Total Count:** 49

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#object-passiveatstatthreshold)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 6 | `-1`<br>`-10`<br>`-2` |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 2 | `+1`<br>`-1`<br>`-2` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 2 | `-1`<br>`-10`<br>`-2` |

</details>


---


### Object: `Robot`


**Definition:** If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties.  
**Total Count:** 49

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_energize_self` | Boolean | If true, the unit can energize itself. | 1 | `true` |

</details>


---


### Object: `Conditional_HasTag`


**Definition:** Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block.  
**Total Count:** 47

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToAllDamage`](./Passives_and_Statuses.md#object-addstatustoalldamage), [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 2 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| `FlatLeechIfDamaged` | `Number` | The flat amount of health leeched when the unit takes damage. | 1 | `3`<br>`5` |

</details>


---


### Object: `StatusOnTookDamage`


**Definition:** Specifies status effects or actions triggered when the unit takes damage.  
**Total Count:** 46

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | `StrengthUp` | Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 13 | Default<br>FormChange<br>Druid |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 3 | `-1`<br>`-2`<br>`-4` |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 3 | `{ . . . }` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 2 | `-1`<br>`-2`<br>`1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`Craft`](./Passives_and_Statuses.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 2 | `{ . . . }` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 2 | `-1`<br>`1`<br>`2` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 1 | `{ . . . }` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 1 | `1`<br>`2`<br>`3` |
| `MovementUp` | Integer | The amount of movement increase or decrease applied. | 1 | `-2`<br>`1`<br>`2` |
| `RandomInjury` | Integer | The number of random injuries applied. | 1 | `1` |
| `TempMovement` | Integer | The amount of temporary movement range added, or a string alias like 'mov'. | 1 | `1`<br>`20`<br>`mov` |

</details>


---


### Object: `Conditional_Enemy`


**Definition:** An object containing status effects or actions applied only if the target is an enemy.  
**Total Count:** 44

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#object-addstatustoelementabilities), [`Conditional_NotBoss`](./Passives_and_Statuses.md#object-conditional_notboss)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 8 | Default<br>FormChange<br>Druid |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 2 | `{ . . . }` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 2 | `{ . . . }` |
| [`Conditional_PartyMember`](./Passives_and_Statuses.md#object-conditional_partymember) | Object | A conditional block that executes its child actions only if the target is a party member. | 2 | `{ . . . }` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `FindItemFromPool`


**Definition:** Specifies the loot pool from which to find an item, with an optional chance.  
**Total Count:** 43

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 | `2`<br>`3`<br>`4` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `StatusOnKill`


**Definition:** Specifies status effects or actions triggered when the unit kills an enemy.  
**Total Count:** 40

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | `HealthGain` | Integer / String | The amount of health restored to the source. | 8 | Default<br>FormChange<br>Druid |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 2 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `RefreshMovePoints` | Integer | The amount of movement points restored to the source. | 2 | `1` |
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 2 | `1` |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object | Container for effects applied only on the first application of this ability during the turn. | 2 | `{ . . . }` |
| [`EquipPermanentItem`](../Reference_and_Meta/Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. | 2 | `BoneClub`<br>`Kidney` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| `Stealth` | Integer | The number of stealth stacks applied. | 1 | `1`<br>`2`<br>`[1 .1]` |
| [`TakeBonusTurnWithStatus`](./Passives_and_Statuses.md#object-takebonusturnwithstatus) | Object | Container for status effects applied when taking a bonus turn. | 1 | `{ . . . }` |

</details>


---


### Object: `Gravity`


**Definition:** An object defining the effects granted by Gravity elemental attunement.  
**Total Count:** 39

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `SpawnThingOnDamage`


**Definition:** Specifies an object that spawns on the tile when the unit takes damage.  
**Total Count:** 38

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 6 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 3 | `false`<br>`true` |
| `spawn_on_death_hit` | Boolean | If true, spawning only occurs when the damage is lethal. | 2 | `false` |
| `consider_all_layers` | Boolean | If true, considers all map layers when determining the spawn location. | 1 | `true` |

</details>


---


### Object: `Conditional_GoodRoll`


**Definition:** Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 1 | `.1`<br>`.16666666`<br>`.3` |
| `UseRandomSpell_Madness` | `Number` | The number of random spells cast when Madness triggers. | 1 | `1` |

</details>


---


### Object: `Conditional_Ally`


**Definition:** Defines effects that apply only if the target is an ally, with an optional else block for non-allies.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack), [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#object-addstatustoelementabilities), [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#object-conditional_sourcehastag), [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#object-extrastatuswhendealingdamage), [`StatusKilledCharacters`](./Passives_and_Statuses.md#object-statuskilledcharacters)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Cleanse` | `Number` | The number of stacks of negative status effects removed from the target. | 2 | `0`<br>`1` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 2 | `{ . . . }` |
| `TempSpeedUp` | Integer | The number of stacks of temporary Speed Up applied to the unit. | 2 | `10`<br>`4`<br>`X` |
| `ClearNegativeEffects` | `Number` | The number of negative effects cleared from the target. | 2 | `1` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 1 | Default<br>FormChange<br>Druid |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 1 | `{ . . . }` |

</details>


---


### Object: `DeathRattle`


**Definition:** Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag.  
**Total Count:** 36

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `pop_corpse` | Boolean | If true, the corpse is destroyed instead of left behind on death. | 2 | `false` |

</details>


---


### Object: `AddPassivesToMinions`


**Definition:** An object containing passives that are granted to all minions spawned by the unit.  
**Total Count:** 36

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 27 | passives<br>class<br>tag |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 5 | `{ . . . }` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 4 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `IncreaseExplosionDamage` | Integer | The flat amount by which explosion damage is increased. | 4 | `1`<br>`2`<br>`3` |
| [`FreePathfindElement`](../Reference_and_Meta/Enums.md#enum-freepathfindelement) | Enum  | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 3 | `Grass`<br>`Water` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 2 | `1`<br>`2`<br>`3` |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |
| [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 2 | `{ . . . }` |
| `WaterWalk` | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 2 | `1` |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 2 | `{ . . . }` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 2 | `1`<br>`2`<br>`3` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 2 | `-25`<br>`10`<br>`2` |
| `ForceAttack` | Integer | If set to 1, forces the target to perform an attack against a random or specified target. | 2 | `1` |
| `IncreaseExplosionSize` | Integer | The number of extra tiles added to the radius of explosions. | 2 | `1`<br>`2`<br>`7` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 2 | `-3`<br>`4`<br>`6` |
| [`EMP`](./Passives_and_Statuses.md#object-emp) | Object | Defines the EMP effect, including spell graphics override for pulsed area damage. | 2 | `{ . . . }` |
| [`tag_filter`](../Reference_and_Meta/Enums.md#enum-tag_filter) | Enum | Specifies a tag (e.g., 'crow', 'rock', 'grub_familiar') used to filter which units a status or effect applies to. | 2 | `crow`<br>`grub_familiar`<br>`rock` |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#object-addstatustoexplosions) | Object | An object whose nested keys define statuses applied to explosion damage. | 2 | `{ . . . }` |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#object-statusalliesonkill) | Object | An object containing status effects to apply to all allies when any ally kills an enemy. | 2 | `{ . . . }` |
| [`FamiliarBonusAbility`](../Reference_and_Meta/Enums.md#enum-familiarbonusability) | Enum | Specifies the name of the bonus ability added to familiars. | 2 | `FamiliarSelfDestruct`<br>`FamiliarSelfDestruct2` |
| `HolyShieldTransferToSpawner` | Integer | If true, holy shield is transferred to the unit that spawned this one on death. | 2 | `1` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 1 | `1` |
| `UncappedHP` | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 1 | `1` |
| `GrassTileHealing` | Integer | The amount of healing received per turn while on a grass tile. | 1 | `1` |
| `SafeExplosions` | Integer | Explosions caused by the unit do not damage friendly units. Value acts as a binary flag. | 1 | `1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `AddUnfilledMaxHealth` | Integer || 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `RandomStatusFromPool`


**Definition:** A collection of status effects; one is randomly chosen and applied to the target.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally), [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy), [`StatusOnGainCoins`](./Passives_and_Statuses.md#object-statusongaincoins), [`StatusOnHealed`](./Passives_and_Statuses.md#object-statusonhealed), [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 3 | `-1`<br>`-2`<br>`1` |
| [`StatusGroup`](./Passives_and_Statuses.md#object-statusgroup) | Object  | A container grouping multiple status effects to be applied simultaneously. | 3 | `{ . . . }` |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`10`<br>`2` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `1`<br>`10`<br>`2` |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | `1`<br>`2`<br>`3` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| `Slow` | Enum / Integer | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 2 | `-1`<br>`1`<br>`2` |
| `Weakness` | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`[1 .01]` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| `Immobile` | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 2 | `0`<br>`1`<br>`10%` |
| `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `Charge` | Equation | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |
| `Blind` | Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 2 | `-1`<br>`1`<br>`2` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 2 | `1`<br>`2`<br>`3` |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| [`Petrify`](../Reference_and_Meta/Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| `Sleep` | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`3` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 2 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `Marked` | Integer | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`3`<br>`5` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 2 | `1`<br>`2`<br>`3` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`[1, 0.1]` |
| `MagicWeakness` | Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`3` |
| `Tarred` | Integer | The amount of tarred stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`[1 .1]` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 2 | `1`<br>`2`<br>`3` |
| `Reflect` | Integer | The amount of reflect stacks applied. | 2 | `1`<br>`5` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| `SpawnCoinAnywhere` | Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 1 | `1`<br>`[1 .5]` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 24 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `keyword_tooltips`


**Definition:** Associates keyword tooltips with the ability, often used for status effects.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Weakness` | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `ForceUseAbility`


**Definition:** The name of the ability the source is forced to use, optionally with a chance.  
**Total Count:** 33

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin), [`StatusEachTurnEnd`](./Passives_and_Statuses.md#object-statuseachturnend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 3 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 3 | `.02`<br>`.1`<br>`.15` |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


---


### Object: `RevengeDamage`


**Definition:** An object defining the damage and effects that trigger when the unit is attacked.  
**Total Count:** 31

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 9 | `damage_instance`<br>`spell`<br>`false` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 3 | Default<br>FormChange<br>Druid |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 8 | `{ . . . }` |

</details>


---


### Object: `ObjectOnHitCharacter`


**Definition:** Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit.  
**Total Count:** 31

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnEnd`](./Passives_and_Statuses.md#object-statuseachturnend), [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#object-statuseachturnendperenemykill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | passives<br>class<br>tag |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `Earth`


**Definition:** Defines the Earth element effects, including damage value.  
**Total Count:** 30

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |

</details>


---


### Object: `StatusEachTurnBegin`


**Definition:** Specifies status effects applied to the unit at the start of each of its turns.  
**Total Count:** 27

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>tag |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 3 | `{ . . . }` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 1 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `FillMana` | Array / Integer | The amount of mana restored, or an [amount, probability] array. | 10 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Grass`


**Definition:** Specifies the status effects applied to allies standing on grass tiles.  
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Enum / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `AbilityReaction`


**Definition:** Specifies the ability used as a reaction when the unit is targeted by an ability.  
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 1 | `true` |

</details>


---


### Object: `SpawnEachTurn`


**Definition:** Specifies an object that spawns on a random adjacent tile each turn, with optional chance.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum | Specifies the object or unit to be spawned. | 6 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 5 | `.02`<br>`.1`<br>`.15` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 2 | `1`<br>`10`<br>`2` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 1 | `false`<br>`true` |

</details>


---


### Object: `Conditional_Boss`


**Definition:** Contains effects that apply only if the target is a boss enemy.  
**Total Count:** 21

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#object-statuskillers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 1 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 14 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Craft`


**Definition:** Specifies the loot pool and slot to craft an item for the source.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 2 | `2`<br>`3`<br>`4` |
| [`slot`](../Reference_and_Meta/Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 2 | `0`<br>`1`<br>`2` |

</details>


---


### Object: `Conditional_HasStatus`


**Definition:** Contains an inner effect block that only executes if the target has the specified status effect.  
**Total Count:** 20

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`CritsApplyStatus`](./Passives_and_Statuses.md#object-critsapplystatus), [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 3 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `PassiveWhenAffectedByElement`


**Definition:** An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element.  
**Total Count:** 18

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 4 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `StatusOnBattleStart`


**Definition:** An object containing status effects to apply to the unit at the start of every battle.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Sleep` | Integer | The amount of sleep stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `FullHeal` | Integer | If non-zero, fully restores the target's health. | 3 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `Shadow`


**Definition:** An object defining the effects granted by Shadow elemental attunement.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | `String` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 2 | `-999999`<br>`.05*X`<br>`.25` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


### Object: `lock_item_slot`


**Definition:** An object that restricts which equipment slots can be used.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`slot`](../Reference_and_Meta/Enums.md#enum-slot) | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 16 | `0`<br>`1`<br>`2` |
| `frame` | Integer | The sprite frame index to display. | 3 | `1`<br>`10`<br>`100` |

</details>


---


### Object: `Conditional_NotBoss`


**Definition:** Contains effects that apply only if the target is not a boss enemy.  
**Total Count:** 16

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKillers`](./Passives_and_Statuses.md#object-statuskillers)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 2 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnStanceSwitch`


**Definition:** Applies the contained status effects when the unit changes stances.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#object-passiveifallarmorempty), [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#object-passiveifemptyface), [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#object-passiveifemptyhead), [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#object-passiveifemptyneck), [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 13 | passives<br>class<br>tag |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 6 | `1`<br>`10`<br>`2` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 2 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `NextBasicAttackCritsThisTurn` | `Number` | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. | 2 | `1` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 1 | `1`<br>`9999` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `statuses`


**Definition:** Defines the status effects applied when the parent trigger event occurs.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ChanceToRevive`](./Passives_and_Statuses.md#object-chancetorevive), [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#object-statusonbattleendifkillthresholdmet)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 2 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 2 | `1`<br>`2` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `PassiveGroup`


**Definition:** A group of passive abilities that can be randomly assigned.  
**Total Count:** 14

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomPassivePool`](./Passives_and_Statuses.md#object-randompassivepool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`SetDefaultFace`](../Reference_and_Meta/Enums.md#enum-setdefaultface) | Enum  | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. | 2 | `happy`<br>`insane`<br>`sad` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `CharismaUp` | Integer | The amount of charisma change, or a keyword like 'item_aux'. | 1 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `SpreadDisease`


**Definition:** Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack), [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#object-addstatustobasicmeleeattack), [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage), [`effects`](./Passives_and_Statuses.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`disease`](../Reference_and_Meta/Enums.md#enum-disease) | Enum | Determines which disease is applied when spreading disease. | 12 | `BirdFlu`<br>`Cancer`<br>`CommonCold` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 11 | `.02`<br>`.1`<br>`.15` |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 6 | `true` |

</details>


---


### Object: `PassiveAtStatThreshold`


**Definition:** An object defining passives granted when a unit's stat meets a specified threshold.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 10 | passives<br>class<br>tag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 10 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 10 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`mode`](../Reference_and_Meta/Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 10 | `equal`<br>`greater`<br>`greater_or_equal` |

</details>


---


### Object: `AddStatusToAllDamage`


**Definition:** Adds the contained status effects to all damage dealt by the unit.  
**Total Count:** 13

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `MoveWhenDamaged`


**Definition:** Defines movement behavior when the unit takes damage, such as weights and move ability.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](../Reference_and_Meta/Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 1 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |

</details>


---


### Object: `CritsApplyStatus`


**Definition:** An object containing statuses applied to the target when the unit lands a critical hit.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#object-passiveifallarmorempty), [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 5 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| `Weakness` | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`2`<br>`3` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 2 | `{ . . . }` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 2 | `{ . . . }` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 1 | `1`<br>`2`<br>`3` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| `Immobile` | Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 1 | `0`<br>`1`<br>`10%` |

</details>


---


### Object: `AmplifyStatus`


**Definition:** Specifies the status effect to amplify, or an object with the status and number of stacks to add.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 3 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| `addstacks` | Number | The number of stacks added to the amplified status effect. | 3 | `2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 3 | `{ . . . }` |

</details>


---


### Object: `StatusOnKillEnemy`


**Definition:** Specifies the effects applied when the unit kills an enemy.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `RefreshMovePoints` | Integer | The amount of movement points restored to the source. | 1 | `1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Specifies an object that spawns on a random empty tile at the start of battle.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 3 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `MoveTowardsDamageSource`


**Definition:** Determines the movement behavior when moving towards the unit that dealt damage to it.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](../Reference_and_Meta/Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 3 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| `move_far` | Boolean | If true, the unit moves the maximum distance towards the damage source. | 3 | `false` |

</details>


---


### Object: `MovementReaction`


**Definition:** Specifies an ability to cast when a unit moves within range, with options for targeting and conditions.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 2 | `false`<br>`true` |

</details>


---


### Object: `Conditional_Corpse`


**Definition:** Contains an inner effect block that only executes if the target is a corpse.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToElementDamage`](./Passives_and_Statuses.md#object-addstatustoelementdamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| `TakeExtraTurn` | `Number` | The number of extra turns granted to the source. | 2 | `1` |
| `Revive` | `Number` | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `1`<br>`100%`<br>`50%` |
| `OverrideDamage` | `Number` | Overrides the damage of the current action to this flat value (can be negative to heal). | 2 | `-10`<br>`0`<br>`1` |
| `SafeDoomed` | Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 2 | `1`<br>`2`<br>`level` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 1 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddStatusToBasicMeleeAttack`


**Definition:** An object listing status effects applied by the unit's basic melee attack.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 3 | `1`<br>`10`<br>`2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | `1`<br>`2`<br>`3` |
| `FaceAway` | Integer | If set, forces the target to face away from the source. | 2 | `1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid` | [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. | 0 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `AddSelfStatusToBasicAttack`


**Definition:** Applies the contained status effects to the unit when it uses its basic attack.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 7 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnEndMove`


**Definition:** Specifies status effects or actions triggered when the unit finishes moving.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StatusAlliesOnBattleStart`


**Definition:** An object containing status effects to apply to all allies at the start of battle.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`EquipTemporaryItem`](../Reference_and_Meta/Enums.md#enum-equiptemporaryitem) | Enum  | Specifies which temporary item is equipped. | 2 | `Bottles`<br>`ButcherHook_Temporary`<br>`FoodBig` |

</details>


---


### Object: `AutocastEachRound`


**Definition:** Contains an ability name and optional 'even_if_stunned' flag to autocast each round.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` |
| `force_display_name` | Boolean | If true, forces the display name to show for the ability. | 2 | `true` |

</details>


---


### Object: `StatusOnTookDamageFromAbility`


**Definition:** Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental).  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 2 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `Shield` | Integer / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `PassiveAtHealthThreshold`


**Definition:** An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 4 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 4 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`mode`](../Reference_and_Meta/Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 4 | `equal`<br>`greater`<br>`greater_or_equal` |

</details>


---


### Object: `ChanceToRevive`


**Definition:** The percentage chance or an object defining chance, health, and statuses on revival.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 1 | `{ . . . }` |

</details>


---


### Object: `BoostWeaponDamage`


**Definition:** The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`false` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `crit_chance` | `String` | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 2 | `-999999`<br>`.05*X`<br>`.25` |

</details>


---


### Object: `ApplyStatusIfCrit`


**Definition:** Defines effects that are applied only when the attack scores a critical hit.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Purge` | Integer | The number of status effects to purge from the target. | 2 | `0`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 3 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddDamageToElementDamage`


**Definition:** Defines additional damage of a specific element added to the unit's attacks.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 4 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 4 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `StatusOnCrit`


**Definition:** An object containing statuses applied to the unit when it lands a critical hit.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 3 | `-1`<br>`-2`<br>`-4` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 1 | `1`<br>`10`<br>`100` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnCastSpell`


**Definition:** An object listing status effects applied to the unit whenever it casts a spell.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `Charge` | Equation | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |
| `CurrentWeaponDamageUp` | Integer | The amount of temporary damage increase to the current weapon. | 2 | `1`<br>`3`<br>`5` |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusIfUnusedMovePoints`


**Definition:** Specifies status effects applied if the unit ends its turn with unused movement points.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`[1, 0.1]` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 1 | `1`<br>`10`<br>`2` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `ConstitutionUp` | Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 1 | `-1`<br>`-2`<br>`1` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusEveryXSpellCasts`


**Definition:** An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 3 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | `1`<br>`3` |
| `RepairWeapon` | Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 1 | `1`<br>`6`<br>`99` |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. | 1 | `1`<br>`2` |
| `RepairWeaponCondition` | Integer | The amount of weapon condition restored. | 1 | `1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `AllStatsUp` | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 3 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusAlliesOnDeath`


**Definition:** Applies the contained status effects to all allies when the unit dies.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 2 | `1` |
| `Reanimate` | Integer | The percentage chance to reanimate the target. | 2 | `100%`<br>`33%`<br>`50%` |
| `HealAndOverhealToShield` | Integer | The amount of healing that also converts overhealing into shield. | 2 | `12`<br>`20` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`[1 .01]` |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 1 | `0`<br>`1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `triggers_limit` | Number || 3 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `SecurityBotProtect`


**Definition:** Specifies the ability and movement used by a security bot to protect allies.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum | Specifies the name of the class's default movement ability. | 3 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |

</details>


---


### Object: `PassiveIfAllArmorEmpty`


**Definition:** Grants the contained passive effects when no armor is equipped in any slot.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)`damage_instance`<br>`spell`<br>`self_damage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>tag |
| [`CounterAttack`](../Reference_and_Meta/Enums.md#enum-counterattack) | Enum  | Specifies the ability used when the unit counterattacks after being hit. | 2 | `BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object | Applies the contained status effects when the unit changes stances. | 2 | `{ . . . }` |
| `ManaCostReduction` | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 2 | `-2`<br>`1`<br>`2` |
| `ExtraMovePoints` | Integer | The number of additional movement points granted to this unit. | 2 | `1` |
| `AddSpellDamage` | Integer | The flat amount of spell damage added to all spell attacks. | 2 | `1`<br>`2` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 1 | `1` |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#object-critsapplystatus) | Object | An object containing statuses applied to the target when the unit lands a critical hit. | 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Container for effects applied only on the first application of this ability during the turn.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill), [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#object-statusonuseabilitywithtag)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`FillMana`](../Reference_and_Meta/Arrays.md#array-fillmana) | Array / Integer  | The amount of mana restored, or an [amount, probability] array. | 1 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 5 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Conditional_BadRoll`


**Definition:** An object containing an `odds` value and effects that are applied when a random roll succeeds.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 8 | Default<br>FormChange<br>Druid |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 3 | `.1`<br>`.16666666`<br>`.3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `CatchProjectiles`


**Definition:** An object defining chance to catch projectiles and optionally apply statuses.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| `ally_chance` | Integer | The percentage chance for an ally to catch incoming projectiles. | 2 | `100%`<br>`15%` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `AddStatusToWeapons`


**Definition:** Specifies status effects to add to the unit's weapon attacks, with their stack counts.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`10`<br>`2` |
| `Cleave` | Integer | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 1 | `1` |
| `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 1 | `50` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `PullSourceToKnockbackImmuneTarget` | Integer | The amount of pull force applied to the source toward a knockback-immune target. | 3 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnUseAbilityWithTag`


**Definition:** Applies the contained status effects when the unit uses an ability with the specified tag.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 7 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 3 | `1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object | Container for effects applied only on the first application of this ability during the turn. | 2 | `{ . . . }` |
| `exclude_basicattack` | Boolean | If true, basic attacks are excluded from triggering the status effect. | 2 | `true` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | `HealthGain` | Integer / String | The amount of health restored to the source. | 0 | Default<br>FormChange<br>Druid |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |

</details>


---


### Object: `PassiveIfEmptyNeck`


**Definition:** Grants the contained passive effects when the neck armor slot is empty.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `1`<br>`10`<br>`100` |
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | `10%`<br>`15%`<br>`2%` |
| `AddCritMultiplier` | Integer | The percentage added to the critical hit damage multiplier. | 2 | `100%`<br>`125%`<br>`150%` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object | Applies the contained status effects when the unit changes stances. | 2 | `{ . . . }` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PassiveIfEmptyHead`


**Definition:** Grants the contained passive effects when the head armor slot is empty.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `1`<br>`10`<br>`100` |
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | `10%`<br>`15%`<br>`2%` |
| `AddCritMultiplier` | Integer | The percentage added to the critical hit damage multiplier. | 2 | `100%`<br>`125%`<br>`150%` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object | Applies the contained status effects when the unit changes stances. | 2 | `{ . . . }` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PassiveIfEmptyFace`


**Definition:** Grants the contained passive effects when the face armor slot is empty.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `1`<br>`10`<br>`100` |
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 2 | `10%`<br>`15%`<br>`2%` |
| `AddCritMultiplier` | Integer | The percentage added to the critical hit damage multiplier. | 2 | `100%`<br>`125%`<br>`150%` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object | Applies the contained status effects when the unit changes stances. | 2 | `{ . . . }` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `ForceMoveAway`


**Definition:** The distance to force the target away from the source.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#object-statusadjacentontheirturnbegin)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `free` | Boolean | If true, this option requires no cost to activate. | 1 | `false` |

</details>


---


### Object: `fire`


**Definition:** An event response that uses fire, with no stat requirement.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#object-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`false` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `DamageNeighborsOnEndMove`


**Definition:** Deals damage and knockback to units on neighboring tiles when the unit finishes moving.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 7 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 7 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 7 | `damage_instance`<br>`spell`<br>`false` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 6 | `{ . . . }` |
| `cant_miss` | `Boolean` | If true, the damage instance always hits its target regardless of accuracy or evasion. | 6 | `true` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ClassManaCostReduction`


**Definition:** Defines a reduction in mana cost for abilities of a specific class.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 2 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 2 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** A container object that lists temporary status effects applied to the unit's basic attack.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CastAgain` | Integer / String | The number of additional times the ability can be cast this turn. | 2 | `1`<br>`2`<br>`3` |
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 1 | `10`<br>`55`<br>`75` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `TowerDefense`


**Definition:** Specifies the range and damage of the Tower Defense counterattack.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnGainCoins`


**Definition:** Specifies status effects applied when this unit gains coins.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 2 | `{ . . . }` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnAllyCatDeath`


**Definition:** An object listing status effects applied to the unit when an allied cat dies.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 1 | `1` |
| [`FillMana`](../Reference_and_Meta/Arrays.md#array-fillmana) | Array / Integer  | The amount of mana restored, or an [amount, probability] array. | 1 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| `PercentHeal` | Integer | The percentage of max HP healed when this effect triggers. | 1 | `50` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusGroup`


**Definition:** A container grouping multiple status effects to be applied simultaneously.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| `SpawnCoinAnywhere` | Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 2 | `1`<br>`[1 .5]` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |

</details>


---


### Object: `ManaCostReductionTagged`


**Definition:** Reduces the mana cost of abilities with the specified tag by the given reduction amount.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 6 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 6 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `LateBloomer`


**Definition:** Specifies the stats gained after a set number of turns or stacks.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `GravityWell`


**Definition:** Specifies the damage and effect applied to units pulled into a gravity well.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 2 | `true` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [{Damaging Keys}](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | 0 | Default<br>FormChange<br>Druid | `Key`<br>`damage_instance`<br>`spell`

</details>


---


### Object: `EnergyStorm`


**Definition:** The period or definition for the Energy Storm, dealing periodic damage in an area.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cycle_start` | Number | The turn number at which the energy storm cycle begins. | 1 | `2`<br>`3` |
| `period` | Number | The number of turns between each cycle of the energy storm. | 1 | `3` |

</details>


---


### Object: `EMP`


**Definition:** Defines the EMP effect, including spell graphics override for pulsed area damage.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_graphics_override`](./Passives_and_Statuses.md#object-spell_graphics_override) | Object | An object defining custom particle effects and palette for the EMP spell. | 4 | `{ . . . }` |
| [`status_explosion_override`](../Reference_and_Meta/Enums.md#enum-status_explosion_override) | Enum | Specifies the status effect particle type to override for the EMP explosion. | 4 | `WaterConduct` |

</details>


---


### Object: `CureDisease`


**Definition:** Attempts to cure the specified disease with the given chance.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 6 | `.02`<br>`.1`<br>`.15` |
| [`disease`](../Reference_and_Meta/Enums.md#enum-disease) | Enum | Determines which disease is applied when spreading disease. | 6 | `BirdFlu`<br>`Cancer`<br>`CommonCold` |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 1 | `true` |

</details>


---


### Object: `Conditional_PartyMember`


**Definition:** A conditional block that executes its child actions only if the target is a party member.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `ChanceToBackflip`


**Definition:** An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |

</details>

---`damage_instance`<br>`spell`<br>`self_damage`


### Object: `AddStatusToElementDamage`


**Definition:** An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 4 | `Electric`<br>`Fire`<br>`Gravity` |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 2 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddStatusToElementAbilities`


**Definition:** Adds the contained status effects to all abilities with the specified element.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 6 | `Electric`<br>`Fire`<br>`Gravity` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 6 | `Default`<br>`FormChange`<br>`Druid` | [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 2 | Default<br>FormChange<br>Druid |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 2 | `{ . . . }` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 2 | `{ . . . }` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `TheHunger`


**Definition:** Defines the Hunger passive, which applies Madness or other effects each turn, representing a disorder.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `TakeBonusTurnWithStatus`


**Definition:** Container for status effects applied when taking a bonus turn.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Madness` | Integer | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnTurnEndIfDidntCastAbilityTypes`


**Definition:** Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s).  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnTurnEndIfCastNSpells`


**Definition:** An object that applies a status effect at the end of the turn if the unit has cast a specified number of spells.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`spells`](../Reference_and_Meta/Arrays.md#array-spells) | Array  | The list of spell ability IDs the unit possesses. | 4 | `1`<br>`2`<br>`5` |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| `DoubleCastSpell` | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. | 2 | `1`<br>`2` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`[1, 0.1]` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnPopCorpse`


**Definition:** Specifies the effects applied when the unit pops a corpse.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusOnOverHealed`


**Definition:** An object that applies a status effect to the unit whenever it receives overhealing (healing beyond max health).  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 2 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `CurrentWeaponDamageUp` | Integer | The amount of temporary damage increase to the current weapon. | 1 | `1`<br>`3`<br>`5` |
| `SpawnScaledRotFly` | Number | The number of scaled Rot Flies to spawn when over-healed. | 1 | `0`<br>`1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | `ForceUseAbility_NonStack` | Enum || 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnOverHealed`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>
## Discovered Objects

> These tables were auto-generated by the schema audit tool. They document objects found in the `.gon` files that were not previously documented.


### Object: `StatusOnEatFood`


**Definition:** An object listing status effects applied to the unit when it eats food.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 2 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `Cleanse` | Integer | The number of stacks of negative status effects removed from the target. | 1 | `0`<br>`1` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 1 | `"min(-int, 0)"`<br>`-1`<br>`-2` |

</details>


---


### Object: `StatusKilledCharacters`


**Definition:** An object listing status effects applied to the unit when it kills a character.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `PassiveWhenAtFullMana`


**Definition:** An object listing passive effects that are active only while the unit's mana is full.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 2 | `{ . . . }` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `1`<br>`10`<br>`2` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | `1` |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 1 | `-1`<br>`-2`<br>`1` |
| [`ReplaceBasicMove`](../Reference_and_Meta/Enums.md#enum-replacebasicmove) | Enum  | Specifies an alternative movement ability that replaces the unit's default move. | 1 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |

</details>


---


### Object: `InfiniteRebirth`


**Definition:** Specifies the health and effects for unlimited rebirth upon death.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 2 | `0`<br>`1`<br>`10` |
| `TempSpeedUp` | Integer | The number of stacks of temporary Speed Up applied to the unit. | 2 | `10`<br>`4`<br>`X` |
| `playercat_health` | Integer | The percentage of maximum health the player cat must have to trigger the rebirth. | 2 | `100%`<br>`25%` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `ExtraStatusWhenDealingDamage`


**Definition:** Defines additional statuses applied to the target or source when dealing damage, with conditionals.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `Eternal`


**Definition:** Defines the Eternal revival effect, setting stacks and the health percentage restored.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `health_percent` | Integer | The amount of health (as a percentage) the unit retains after being revived or survived a fatal hit. | 2 | `100%`<br>`50%` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 1 | `1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `ElementalManaCostReduction`


**Definition:** An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 3 | `Electric`<br>`Fire`<br>`Gravity` |
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 3 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `ElementalAttunement`


**Definition:** Defines the elemental effects (Fire, Ice, etc.) applied by the attunement.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |`damage_instance`<br>`spell`<br>`self_damage`
| :--- | :--- | :--- | :--- | :--- |
| [`Fire`](./Passives_and_Statuses.md#object-fire) | Integer / Object  | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 2 | `{ . . . }`<br>`1` |
| [`Holy`](./Passives_and_Statuses.md#object-holy) | Enum / Object  | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 2 | `{ . . . }`<br>`MegaGuppy_TransformHoly` |
| [`Electric`](./Passives_and_Statuses.md#object-electric) | Object  | Applies a Stun status effect with specified stacks and probability based on variable X. | 2 | `{ . . . }` |
| [`Wind`](./Passives_and_Statuses.md#object-wind) | Object  | Defines the properties for the Wind element, such as knockback amount. | 2 | `{ . . . }` |
| [`Water`](./Passives_and_Statuses.md#object-water) | Object  | Form state for water element, applying a puddle or movement bonus. | 2 | `{ . . . }` |
| [`Ice`](./Passives_and_Statuses.md#object-ice) | Object  | Applies the Slow status effect to targets hit by ice-element abilities. | 2 | `{ . . . }` |
| [`Gravity`](./Passives_and_Statuses.md#object-gravity) | Object  | An object defining the effects granted by Gravity elemental attunement. | 2 | `{ . . . }` |
| [`Earth`](./Passives_and_Statuses.md#object-earth) | Object  | Defines the Earth element effects, including damage value. | 2 | `{ . . . }` |
| [`Grass`](./Passives_and_Statuses.md#object-grass) | Object  | Specifies the status effects applied to allies standing on grass tiles. | 2 | `{ . . . }` |
| [`Shadow`](./Passives_and_Statuses.md#object-shadow) | Object  | An object defining the effects granted by Shadow elemental attunement. | 2 | `{ . . . }` |

</details>


---


### Object: `Diabetes`


**Definition:** Defines the Diabetes disorder, including its name, description, and associated passive effects.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| `Confusion` | Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `Conditional_Shielded`


**Definition:** An object containing effects that are only applied if the target has a shield active.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | `BonusCritChance` | `Number` | The flat percentage increase to critical hit chance. | 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddStatusToAllDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `AddPassivesToCharmed`


**Definition:** Grants the contained passive effects to units under the charm status.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 5 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 2 | `-25`<br>`10`<br>`2` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 2 | `-3`<br>`4`<br>`6` |

</details>


---


### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 2 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `range` | Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Study`


**Definition:** The number of stacks of the Study status applied.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `marked` | Number | The number of Marked stacks applied to the target. | 1 | `2` |

</details>


---


### Object: `StatusOnTurnEndIfManaOrHealthExact`


**Definition:** An object that applies a status effect at the end of the turn if the unit's mana or health is exactly a specified value.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation | The amount of mana required to cast, as a formula or stat. | 4 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 3 | `{ . . . }` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | `1`<br>`3` |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnTurnEndIfManaExact`


**Definition:** An object that applies a status effect at the end of the turn if the unit's mana is exactly a specified value.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation | The amount of mana required to cast, as a formula or stat. | 4 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 2 | `1`<br>`2` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 1 | `1`<br>`3` |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`[1, 0.1]` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnHealed`


**Definition:** An object that applies a status effect to the unit whenever it is healed.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 1 | `{ . . . }` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 1 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnBreakItem`


**Definition:** An object containing status effects to apply when the unit breaks a weapon or armor item.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 2 | `1`<br>`2`<br>`3` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusEachTurnEndForEachTurn`


**Definition:** Statuses applied at the end of each turn, with the number of turns as nested values.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusAlliesOnKill`


**Definition:** An object containing status effects to apply to all allies when any ally kills an enemy.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusAfterCastSpell`


**Definition:** An object containing status effects to apply to the unit immediately after it casts any spell.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 1 | `-1`<br>`1`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | `TempSpellDamageUp` | Integer | The amount of temporary spell damage increase applied. | 4 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `spell_graphics_override`


**Definition:** An object defining custom particle effects and palette for the EMP spell.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`EMP`](./Passives_and_Statuses.md#object-emp)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`particle`](../Reference_and_Meta/Enums.md#enum-particle) | Enum | Specifies the particle effect displayed. | 4 | `ArrowFromAbove`<br>`BigMagicMissileBlast`<br>`Bolt` |
| [`palette`](../Reference_and_Meta/Enums.md#enum-palette) | Enum / Integer  | Specifies the color palette index for the ability's visuals. | 4 | `-1`<br>`0`<br>`1` |
| [`center_particle`](../Reference_and_Meta/Enums.md#enum-center_particle) | Enum | Specifies the FX particle effect emitted at the center of the ability's origin tile. | 4 | `BigMagicMissileBlast`<br>`Explosion`<br>`FireBlastMushroom` |
| [`area_particle`](../Reference_and_Meta/Enums.md#enum-area_particle) | Enum | Specifies the FX particle effect emitted across the affected area tiles. | 4 | `Bolt`<br>`BurnTrigger`<br>`Earthquake` |

</details>


---


### Object: `SpecialFriends`


**Definition:** An object containing a set of status effects applied to allied units that are considered 'special friends' (e.g., granted by a passive).  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `SpawnCatCopyOnBattleStart`


**Definition:** An object that spawns a copy of the unit's cat at the start of battle, with sub-keys for the copy object and chain-prevention tag.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`prevent_chain_tag`](../Reference_and_Meta/Enums.md#enum-prevent_chain_tag) | Enum | A tag that prevents chaining of spawns from the same source. | 3 | `ancestorset_shade`<br>`eb_twin`<br>`minime_clone` |

</details>


---


### Object: `ReplaceBrain`


**Definition:** Defines a replacement AI brain and behavior pattern for the mutant.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`brain`](../Reference_and_Meta/Enums.md#enum-brain) | Enum | Specifies the AI brain type used for decision-making logic. | 1 | `DicerBrain`<br>`GenericBrain`<br>`MountBrain` |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum | Determines the movement strategy used by the AI when executing this move ability. | 1 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`decision_weights`](../Reference_and_Meta/Enums.md#enum-decision_weights) | Enum | Specifies the named set of decision weight presets used by the AI. | 1 | `always_cast`<br>`always_cast_careless`<br>`angry` |

</details>


---


### Object: `RandomPassivePool`


**Definition:** A pool of random passives from which one is chosen for this unit.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`PassiveGroup`](./Passives_and_Statuses.md#object-passivegroup) | Object  | A group of passive abilities that can be randomly assigned. | 2 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


---


### Object: `PassiveAfterXKills`


**Definition:** Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `MegaMinions`


**Definition:** The number of extra minions spawned or maximum minion count.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `cycle_start` | Number | The turn number at which the energy storm cycle begins. | 1 | `2`<br>`3` |

</details>


---


### Object: `LightningRod`


**Definition:** Specifies the unit tags and conditions that cause lightning strikes.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `ice`


**Definition:** An event response that uses ice, with no stat requirement.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#object-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`false` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `EscapeSequence`


**Definition:** Defines an escape sequence with safe explosion displacement and random distance displacement.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomDistanceDisplace` | `Number` | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. | 2 | `20` |
| `SafeExplosionIfHitSomething` | Number | The radius of a safe explosion that only occurs if it hits an obstacle or entity. | 2 | `10`<br>`5` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `empty_armor_scaled_stats`


**Definition:** Defines the stat bonuses applied when no armor is equipped in a slot.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer | The Intelligence stat value or modifier. | 2 | `-1`<br>`-10`<br>`-2` |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 2 | `+1`<br>`-1`<br>`-2` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 2 | `-1`<br>`-10`<br>`-2` |

</details>


---


### Object: `DistanceBonusDamage`


**Definition:** An object that adds bonus damage based on the distance from the target, with sub-keys for stacks and minimum range.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_range` | Integer | The minimum range of the ability. | 4 | `0`<br>`1`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `DamageNeighborsAfterMove`


**Definition:** Defines the spell damage and effects applied to neighboring tiles after the unit moves.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid`
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`false` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |

</details>


---


### Object: `Conditional_Adjacent`


**Definition:** An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 2 | `passives`<br>`class`<br>`tag`
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`10`<br>`2` |
| `BonusDamage` | Equation | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `BonusCritChance` | Integer | The flat percentage increase to critical hit chance. | 2 | `100`<br>`25`<br>`50` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `Autism`


**Definition:** An object defining the Autism disorder, including its name, description, class, and stat modifications for innate and learned levels.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `innate` | Number | The amount of innate bonus or penalty applied to the Autism status. | 1 | `-2` |
| `learned` | Number | The amount of learned bonus applied to the Autism status. | 1 | `1` |

</details>


---


### Object: `ApplyStatusesToRandomEnemiesEachTurn`


**Definition:** An object specifying statuses to apply to random enemies each turn, with an optional 'count' field.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `Bounty` | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 2 | `1`<br>`3` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 1 | `0`<br>`1`<br>`10` |

</details>


---


### Object: `AllyManaRegenAura`


**Definition:** An object granting a mana regeneration aura to allies, with sub-keys for stacks and range.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 4 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AllyBonusAbilityAura`


**Definition:** Specifies an ability name granted to adjacent allies in an aura, optionally with a square radius.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `square` | Boolean | If true, the aura uses a square shape instead of a circle. | 2 | `true` |

</details>


---


### Object: `AddStatusToSpells`


**Definition:** Specifies status effects added to all spell attacks used by this unit.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 1 | `{ . . . }` |

</details>


---


### Object: `AddStatusToExplosions`


**Definition:** An object whose nested keys define statuses applied to explosion damage.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions), [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddElement`](../Reference_and_Meta/Enums.md#enum-addelement) | Enum | Specifies the element to add to explosions. | 8 | `Fire`<br>`Napalm` |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 4 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |

</details>


---


### Object: `StatusWhenAllySpendsMana`


**Definition:** Specifies the effects applied when an ally spends mana.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `OneUseSpellDamageUp` | Integer | Increases spell damage by the specified amount, but the effect is consumed after a single use. Alias for SpellDamageUp. | 2 | `2` |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 1 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnUseBasicAttack`


**Definition:** Specifies the effects applied when the unit performs a basic attack.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `FlippedFacingForceAttack` | Integer | If non-zero, forces the unit to attack after flipping its facing direction. | 2 | `1` |

</details>


---


### Object: `StatusOnPickupCoins`


**Definition:** Specifies the effects applied when the unit picks up coins.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RefreshMovePoints` | Integer | The amount of movement points restored to the source. | 2 | `1` |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 1 | `-1`<br>`-2`<br>`-4` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 1 | `-1`<br>`1`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnCollectPickup`


**Definition:** An object containing status effects to apply when the unit collects a pickup item.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>


---


### Object: `StatusKillers`


**Definition:** An object containing nested conditionals that apply status effects when the unit kills an enemy.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StatusKilledCharacters`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `ScaledStatusOnSpendMana`


**Definition:** An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RepressedMemoriesMetronome`](./Passives_and_Statuses.md#object-repressedmemoriesmetronome) | Object  | An object defining the metronome status effect and its pool triggered on mana spend. | 2 | `{ . . . }` |

</details>


---


### Object: `PassiveWhileInMonkMeleeStance`


**Definition:** Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `1`<br>`10`<br>`2` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `LowHealthAllyDodgeChanceAura`


**Definition:** Specifies the health threshold and dodge chance granted to nearby low-health allies.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `theshold` | Number | The health threshold below which allies receive the dodge chance aura. | 2 | `5` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |

</details>


---


### Object: `DamageReductionAura`


**Definition:** Defines an aura that reduces incoming damage, with range, ally-only, and stack settings.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `1`<br>`10`<br>`2` |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 2 | `false`<br>`true` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |

</details>


---


### Object: `BouncyProjectiles`


**Definition:** An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`max_range`](../Reference_and_Meta/Enums.md#enum-max_range) | Enum / Integer | The maximum range of the ability, can be a static number or an expression. | 2 | `"4+(1-clamp(spd,0,1))*2"`<br>`"max(5-int, 1)"`<br>`-1` |
| `max_bounces` | Integer | The maximum number of bounces for a projectile; -1 means infinite. | 2 | `-1`<br>`1`<br>`10` |

</details>


---


### Object: `AutocastEachTurnBegin`


**Definition:** Specifies the ability automatically cast at the start of each turn, optionally with chance and polarity.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `advantage_polarity` | Number | The polarity advantage for autocast timing; negative values give an advantage. | 1 | `-1` |

</details>


---


### Object: `AddStatusToTrampleDamage`


**Definition:** An object whose nested keys define statuses applied to trample damage.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `AddStatusToKnockbackDamage`


**Definition:** An object whose nested keys define statuses applied to damage caused by knockback.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `AddSelfStatusToWeapons`


**Definition:** An object whose nested keys define status effects applied to the unit's own weapons.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `TileDamageMultiplier`


**Definition:** Multiplier for damage dealt to environmental tiles.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ally_multiplier` | Number | A multiplier applied to tile damage dealt to allies. | 1 | `0` |
| `multiplier` | Number | A multiplier applied to tile damage dealt to enemies. | 1 | `2` |

</details>


---


### Object: `TaggedPickupEffectReplacement`


**Definition:** Specifies a replacement effect for picking up items with a given tag.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 2 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `StrengthInNumbersAura`


**Definition:** The amount of strength gained per nearby ally within the aura.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 1 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `count_self` | Boolean | If true, the unit counts itself in the strength-in-numbers calculation. | 1 | `true` |

</details>


---


### Object: `StatusThingsKnockedBack`


**Definition:** Specifies the effects applied when the unit knocks back another unit.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Drag` | Number | The distance (in tiles) that the unit drags knocked-back targets toward itself. | 2 | `1`<br>`2` |

</details>


---


### Object: `StatusPerInjury`


**Definition:** Specifies the effects granted per injury the unit has, up to an optional cap.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `injury` | `String` | Specifies the type of injury applied, such as bleeding or stat reduction. | 2 | `bleeding`<br>`burned`<br>`cha` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `cap` | Number | The maximum value or percentage cap for the stacking effect. | 2 | `10`<br>`50%` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `StrengthUp` | Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 1 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnUseElementAbility`


**Definition:** Specifies the effects applied when the unit uses an ability matching the specified element.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 2 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnTriggerTrap`


**Definition:** Specifies the effects applied when the unit triggers a trap.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 2 | `-1`<br>`1`<br>`2` |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`2`<br>`5` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnTookDamageFromEnemyAbility`


**Definition:** Specifies the effects applied when the unit takes damage from an enemy ability.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Quivered` | Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `MoveQuivered` | Float | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`[1, 0.1]` |

</details>


---


### Object: `StatusOnOverMana`


**Definition:** Specifies the effects applied when the unit's mana exceeds its maximum.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 2 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 2 | `1`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 1 | `1`<br>`2`<br>`4` |

</details>


---


### Object: `StatusOnHeal`


**Definition:** Specifies the effects applied when the unit receives healing.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnGainShield`


**Definition:** Specifies the effects applied when the unit gains a shield.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 2 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnEndMove`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `StatusOnEatPill`


**Definition:** Specifies the effects applied when the unit consumes a pill item.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StatusOnDealtDamageThreshold`


**Definition:** Specifies the effects applied when the unit deals damage equal to or exceeding the defined threshold.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `RefreshMovePoints` | Integer | The amount of movement points restored to the source. | 2 | `1` |
| `count_overkill` | Boolean | If true, overkill damage counts toward the damage threshold. | 2 | `true` |
| `ignore_during_movement` | Boolean | If true, damage dealt during movement does not count toward the threshold. | 2 | `true` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 1 | `-1`<br>`-2`<br>`1` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnDealtDamage`


**Definition:** An object containing status effects to apply to the unit whenever it deals damage to an enemy.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempStrengthUp` | Integer | The number of stacks of temporary Strength Up applied to the unit. | 2 | `1`<br>`2`<br>`X` |
| `TempDexterityUp` | Integer | The number of temporary dexterity stacks applied, or a string alias like 'X'. | 2 | `2`<br>`X` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | `TempLuckUp` | Integer || 0 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusOnDealtDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `StatusOnBattleEndIfKillThresholdMet`


**Definition:** An object containing a 'kills' threshold and status effects to apply at the end of battle if the unit's kill count meets or exceeds the threshold.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 2 | `{ . . . }` |
| `kills` | Number | The number of kills required to meet the threshold for the battle-end status effect. | 2 | `3` |

</details>


---


### Object: `StatusOnAnyDeath`


**Definition:** An object containing status effects to apply whenever any unit (ally or enemy) dies.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `StatusKillers`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `StatusEveryXTurnBegins`


**Definition:** An object with a 'turns' value defining status effects applied every X turns at the start of the turn.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `DivineShield` | Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `StatusEnemiesOnDeath`


**Definition:** An object containing status effects to apply to all enemies when the unit dies.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StatusEnemiesOnDeath`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `StatusEachTurnEndPerEnemyKill`


**Definition:** An object containing status effects to apply at the end of each turn for each enemy killed during that turn.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 2 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `StatusDamagers`


**Definition:** An object defining status effects that damage the unit, with parameters for each status.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusAnyCatAllyWhoKills`


**Definition:** An object containing status effects to apply to any cat ally who kills an enemy.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StatusAnyCatAllyWhoKills`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `StatusAllyWhenAllySpendsMana`


**Definition:** An object with a 'threshold' (mana amount) and status effects to apply to an ally whenever any ally spends at least that much mana.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer  | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


`damage_instance`<br>`spell`<br>`self_damage`


### Object: `StatusAlliesOnGainCoins`


**Definition:** An object containing status effects to apply to allies when the unit gains coins, with an optional 'scaled' boolean to scale stacks.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer / String | The amount of health restored to the source. | 2 | `1`<br>`10`<br>`2` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `scaled` | Boolean | If true, the status effect applied to allies is scaled based on the coins gained. | 1 | `true` |

`damage_instance`<br>`spell`<br>`self_damage`


</details>


---


### Object: `StatusAlliesEachTurn`


**Definition:** Defines a status effect applied to all allies each turn, with an optional exclusion of the owner and conditional checks.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#object-passiveuntilcastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 1 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `exclude_self` | Boolean | If true, the effect does not apply to the source unit itself. | 1 | `false` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatsAtLowHealth`


**Definition:** An object containing a 'threshold' (health value) and stat bonuses (e.g., 'strength', 'speed') that are applied when the unit's health is below the threshold.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`speed`](../Reference_and_Meta/Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 1 | `-30`<br>`-4`<br>`.5` |
| `strength` | Integer | The base strength stat, used for physical damage calculations. | 1 | `1`<br>`10`<br>`15` |

</details>


---


### Object: `SmiteEnemiesWhoKill`


**Definition:** An object defining a smite effect applied to enemies who kill another unit, typically dealing damage and applying a stun.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 2 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 2 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 2 | `damage_instance`<br>`spell`<br>`false` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `schadenfreude_scaled_stats`


**Definition:** Defines the stat bonuses (str, dex, con, int, cha) applied by the Schadenfreude trait at a given level.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 2 | `-1`<br>`-2`<br>`-3` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer | The Strength stat value or modifier. | 2 | `-1`<br>`-2`<br>`-3` |

</details>


---


### Object: `ScaledStatusOnOverMana`


**Definition:** An object containing status effect definitions to apply when the unit gains mana that exceeds its maximum mana, with the number of stacks scaled by the amount of over-mana.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 2 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `Cleanse` | Integer | The number of stacks of negative status effects removed from the target. | 1 | `0`<br>`1` |

</details>


---


### Object: `RepressedMemoriesMetronome`


**Definition:** An object defining the metronome status effect and its pool triggered on mana spend.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#object-scaledstatusonspendmana)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 2 | `2`<br>`3`<br>`4` |

</details>


---


### Object: `PassiveWhileWearingMetal`


**Definition:** Applies a set of passive effects (e.g., AddElementsToWeapon with Electric) while the unit is equipped with metal armor or accessories.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddElementsToWeapon`](../Reference_and_Meta/Enums.md#enum-addelementstoweapon) | Enum | Specifies the element to add to the unit's attacks while wearing metal equipment. | 2 | `Electric` |

</details>


---


### Object: `PassiveWhilePreviewingMonkRangedStance`


**Definition:** Applies specific passive effects (e.g., AddBonusRange) while the unit is previewing the Monk's ranged stance before committing to it.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddBonusRange` | Integer | The number of additional tiles of range added to the unit's abilities. | 2 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `PassiveWhileInMonkRangedStance`


**Definition:** Applies specific passive effects (e.g., AddBonusRange, AddSpellDamage) while the unit is in the Monk's ranged combat stance.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddBonusRange` | Integer | The number of additional tiles of range added to the unit's abilities. | 2 | `1`<br>`10`<br>`2` |
| `AddSpellDamage` | Integer | The flat amount of spell damage added to all spell attacks. | 2 | `1`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 1 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `PassiveWhenTheAlpha`


**Definition:** Activates a set of passive effects (e.g., TogglableRoundEndExtraTurn) only while the unit holds the Alpha status on the team.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TogglableRoundEndExtraTurn` | Number | The number of extra turns granted at the end of each round while the unit is the alpha. | 2 | `1` |

</details>


---


### Object: `PassiveUntilGetKill`


**Definition:** Applies a set of passive effects (e.g., Holy Damage Blessing with burn) that remain active until the unit scores a kill.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HolyDamageBlessing`](./Passives_and_Statuses.md#object-holydamageblessing) | Object  | An object defining the damage multiplier and status effects applied as a holy damage blessing. | 2 | `{ . . . }` |

</details>


---


### Object: `PassiveUntilCastSpell`


**Definition:** Applies a set of passive effects (e.g., healing allies each turn) that remain active until the unit casts a spell.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HealAlliesEachTurn`](./Passives_and_Statuses.md#object-healallieseachturn) | Object  | An object defining how much health and mana are healed to all allies each turn. | 2 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [`StatusAlliesEachTurn`](./Passives_and_Statuses.md#object-statusallieseachturn) | Object | Defines a status effect applied to all allies each turn, with an optional exclusion of the owner and conditional checks. | 1 | `{ . . . }` |

</details>


---


### Object: `PassiveAtInjuryThreshold`


**Definition:** Applies a set of passive effects when the unit's injury level ('injury' sub-key) meets or exceeds the specified 'threshold' using the comparison 'mode'.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2 | `{ . . . }` |
| `injury` | `String` | Specifies the type of injury applied, such as bleeding or stat reduction. | 2 | `bleeding`<br>`burned`<br>`cha` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 2 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`mode`](../Reference_and_Meta/Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 2 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`{Event Keys}`](../Engine_Scripts_and_Logic/Engine_EventKeys.md#valid-property-keys) | Variable | Represents a key for an event entry within an item pool. | 2 | `common`<br>`rare`<br>`cha` |

</details>


---


### Object: `PassiveAtFullHealth`


**Definition:** Applies a set of passive effects (e.g., mana cost reduction, extra damage taken) only while the unit is at maximum health.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ManaCostReduction` | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 2 | `-2`<br>`1`<br>`2` |
| `TakeExtraDamage` | Number | The percentage of extra damage taken while at full health. | 2 | `200%` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>


---


### Object: `on_throw`


**Definition:** An object defining effects that trigger when the item is thrown.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#object-boobytrapitems)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HitExplosion` | `Number` | The radius of the explosion triggered on hit. | 2 | `10`<br>`5`<br>`X` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `on_break`


**Definition:** An object defining effects that trigger when the item is broken.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`BoobyTrapItems`](./Passives_and_Statuses.md#object-boobytrapitems)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SafeExplosionIfHitSomething` | Number | The radius of a safe explosion that only occurs if it hits an obstacle or entity. | 2 | `10`<br>`5` |

</details>


---


### Object: `NextBattleStatus`


**Definition:** A set of status effects (e.g., stat buffs, full heal) automatically applied to the unit at the start of the next battle.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `NextBattleStatus`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `lightning`


**Definition:** An event response using lightning, with no stat requirement.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#object-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`false` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `HolyDamageBlessing`


**Definition:** An object defining the damage multiplier and status effects applied as a holy damage blessing.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilGetKill`](./Passives_and_Statuses.md#object-passiveuntilgetkill)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| `damage_multiplier` | Number | A multiplier for holy damage dealt. | 2 | `2`<br>`3` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `HealAlliesEachTurn`


**Definition:** An object defining how much health and mana are healed to all allies each turn.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#object-passiveuntilcastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `mana` | Equation | The amount of mana required to cast, as a formula or stat. | 2 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `exclude_self` | Boolean | If true, the effect does not apply to the source unit itself. | 2 | `false` |

</details>


---


### Object: `ExtraStatusWhenDealingDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `DelayedWindCone`


**Definition:** An object containing parameters for a delayed wind cone, such as damage and distance.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#object-addstatustomeleedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 1 | `-3`<br>`10`<br>`2` |

</details>


---


### Object: `DamageNeighborTilesWhenCastSpell`


**Definition:** Defines the spell damage and effects applied to neighbor tiles when a spell is cast.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`fire`](./Passives_and_Statuses.md#object-fire) | Object | An event response that uses fire, with no stat requirement. | 1 | `{ . . . }` |
| [`ice`](./Passives_and_Statuses.md#object-ice) | Object | An event response that uses ice, with no stat requirement. | 1 | `{ . . . }` |
| [`lightning`](./Passives_and_Statuses.md#object-lightning) | Object | An event response using lightning, with no stat requirement. | 1 | `{ . . . }` |
| [`triattack`](./Passives_and_Statuses.md#object-triattack) | Object | An object defining the properties of a triangular attack that damages neighbor tiles when casting a spell. | 1 | `{ . . . }` |

</details>


---


### Object: `Conditional_Shielded`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_PartyMember`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_NotBoss`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `Conditional_Adjacent`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>
### Object: `CollectPickupsOnBattleEnd`


**Definition:** The number of pickups automatically collected from corpses on the battlefield when the battle ends.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pop_corpses` | Boolean | If true, corpses are destroyed to collect pickups when the battle ends. | 1 | `true` |

</details>


---


### Object: `CatAPultAnimation`


**Definition:** An object specifying the ability and animation used for the CatAPult passive.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum | Specifies the animation played when the ability is used. | 2 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |

</details>


---


### Object: `BoobyTrapItems`


**Definition:** An object defining effects to apply when items are thrown or broken.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`on_break`](./Passives_and_Statuses.md#object-on_break) | Object | An object defining effects that trigger when the item is broken. | 2 | `{ . . . }` |
| [`on_throw`](./Passives_and_Statuses.md#object-on_throw) | Object | An object defining effects that trigger when the item is thrown. | 2 | `{ . . . }` |

</details>


---


### Object: `AlternateCraftingPools`


**Definition:** An object mapping crafting pool categories to alternate pools for the unit.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tinkerer_0`](../Reference_and_Meta/Enums.md#enum-tinkerer_0) | Enum | Specifies the first alternate crafting pool to use. | 2 | `tinkerer_0_bombs` |
| [`tinkerer_1`](../Reference_and_Meta/Enums.md#enum-tinkerer_1) | Enum | Specifies the second alternate crafting pool to use. | 2 | `tinkerer_1_bombs` |

</details>


---


### Object: `AllyHealthRegenAura`


**Definition:** An object defining an aura that grants health regeneration to allies, typically with 'stacks' and 'range' fields.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer | The distance in tiles for the trigger effect; `global` means any distance. | 2 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `AddStatusToTrampleDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `AddStatusToMeleeDamage`


**Definition:** An object whose nested keys define statuses applied to melee damage.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DelayedWindCone`](./Passives_and_Statuses.md#object-delayedwindcone) | Object | An object containing parameters for a delayed wind cone, such as damage and distance. | 1 | `{ . . . }` |
| [`DelayedWind`](./Passives_and_Statuses.md#object-delayedwind) | Object  | Defines the properties for a delayed wind effect applied on melee damage. | 1 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AddStatusToMeleeDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `AddStatusToFirstBasicAttack`


**Definition:** An object whose nested keys define statuses applied only to the unit's first basic attack.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `AddStatusToFirstBasicAttack`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `AddStatusToBasicAttackWithCooldown`


**Definition:** An object whose nested keys define statuses applied to basic attacks, subject to a cooldown.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CharmedForceAttack` | `Number` | If non-zero, forces the charmed target to use its basic attack on a random nearby unit. | 2 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 2 | `{ . . . }` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddStatusToBasicAttackWithCooldown`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |

</details>
### Object: `AddStatusToAllDamageAbilities`


**Definition:** Adds the contained status effects to all damaging abilities (spells and attacks).  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 1 | `1`<br>`10`<br>`2` |
| `Weakness` | Enum / Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 1 | `1`<br>`2`<br>`3` |
| `Piercing` | Integer | The amount of armor or damage reduction ignored by the attack or ability. | 1 | `1` |

</details>


---


### Object: `AddSelfStatusToWeapons`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `AddPassiveToSpawnedRocks`


**Definition:** An object whose nested keys define passives applied to rocks spawned by the unit.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddFilledMaxHealth` | Number | The amount of filled max health added to spawned rocks. | 2 | `3`<br>`7` |
| `JoinSpawnerFaction` | Number | The faction ID that spawned rocks should join. | 2 | `1` |

</details>


---


### Object: `AddPassivesToSummonAbilityMinions`


**Definition:** An object whose nested keys define passives applied to minions summoned by abilities.  
**Total Count:** 2

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root), [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `MovementUp` | Integer | The amount of movement increase or decrease applied. | 2 | `-2`<br>`1`<br>`2` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 2 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `triattack`


**Definition:** An object defining the properties of a triangular attack that damages neighbor tiles when casting a spell.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#object-damageneighbortileswhencastspell)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 1 | `damage_instance`<br>`spell`<br>`false` |

</details>


---


### Object: `TourettesMeows`


**Definition:** Defines a passive that triggers random vocalizations (hiss, hit, normal) at random cooldown intervals.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](../Reference_and_Meta/Arrays.md#array-pool) | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 1 | `2`<br>`3`<br>`4` |
| [`cooldown`](../Reference_and_Meta/Arrays.md#array-cooldown) | Array | An array [min max] defining the random cooldown range in turns between Tourette's meow outbursts. | 1 | `[8 15]` |

</details>


---


### Object: `StatusOnTakeHealthDamage`


**Definition:** Defines a status effect applied to the unit each time it takes health damage, such as a permanent stat reduction.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 1 | `-1`<br>`-2`<br>`1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnLoseShield`


**Definition:** Defines a status effect applied to the unit each time it loses a shield point.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusOnEatPill`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `StatusIfBattleAlreadyBegan`


**Definition:** Defines a status effect that is applied only if the battle has already started (not on the first turn).  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 1 | `1` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusAlliesScaledByCursedOnDeath`


**Definition:** An object containing status effects to apply to allies when the unit dies, with stacks scaled by the number of Cursed stacks the unit had.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 1 | `-1`<br>`-2`<br>`-4` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `StatusAlliesOnSpendMana`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `StatusAlliesOnSpendMana`


**Definition:** An object containing status effects to apply to allies when the unit spends mana.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StatusAdjacentOnTheirTurnBegin`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |
`damage_instance`<br>`spell`<br>`self_damage`

</details>
### Object: `StatusAdjacentOnTheirTurnBegin`


**Definition:** Defines a status effect applied to adjacent units when their turn begins, such as forcing them to move away.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `StackingDodgeChanceOnTookDamage`


**Definition:** An object with 'amount' (percent) and 'cap' (percent) defining a stacking dodge chance buff that increases each time the unit takes damage, up to a maximum.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`amount`](../Reference_and_Meta/Arrays.md#array-amount) | Array  | For ambient light, the target brightness value (as a float or percentage array for RGB). | 1 | `.1`<br>`.25`<br>`.35` |
| `cap` | Number | The maximum value or percentage cap for the stacking effect. | 1 | `10`<br>`50%` |

</details>


---


### Object: `SelfDamageWhenDealDamage`


**Definition:** An object defining the damage the unit takes to itself whenever it deals damage to an enemy.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 1 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>


---


### Object: `ScaledStatusOnOverHealed`


**Definition:** An object containing status effect definitions to apply when the unit receives healing that exceeds its maximum health, with the number of stacks scaled by the amount of over-healing.  
**Total Count:** 1
`damage_instance`<br>`spell`<br>`self_damage`

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SpawnScaledRotFly` | Number | The number of scaled Rot Flies to spawn when over-healed. | 1 | `0`<br>`1` |

</details>


---


### Object: `ScaledStatusOnLoseShield`


`damage_instance`<br>`spell`<br>`self_damage`
**Definition:** Applies a scaled status effect (e.g., Thorns proportional to shield lost) when the unit loses shield points. Value includes a 'shield' sub-key for threshold.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `ScaledStatusOnBleedDamage`


**Definition:** An object that applies a scaled status (e.g., Charge) on the unit when they take bleed damage.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Equation | The number of charge stacks applied. | 1 | `1`<br>`2`<br>`3` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `PassiveLevelScaledStatus`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `PassiveLevelScaledStatus`


**Definition:** An object containing status effects whose values scale with the unit's level, using X as the level variable.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Trample`](../Reference_and_Meta/Arrays.md#array-trample) | Array / Integer  | The amount of bonus damage dealt when moving through an enemy. | 1 | `1`<br>`3`<br>`4` |
| `Shield` | Equation / String | The amount of shield granted to the source, absorbing incoming damage. | 1 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `SizeScalePercent` | Equation | A formula string that calculates the percentage scale of the unit's size based on a variable X (e.g., level). | 1 | `"sqrt(1.0+(.05*(X-1)))*100"` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | `passives`<br>`class`<br>`tag` | [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | 0 | Default<br>FormChange<br>Druid | `Key`<br>`Default`<br>`FormChange`

</details>


---


### Object: `FurnitureStats`


**Definition:** Defines the Comfort, Stimulation, and Appeal stats of furniture.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Comfort` | Number | The amount of comfort provided by the furniture piece to the room. | 1 | `-1`<br>`-2`<br>`-3` |
| `Appeal` | Number | The amount of appeal provided by the furniture piece to the room. | 1 | `-1`<br>`-2`<br>`-4` |
| `Stimulation` | Number | The amount of stimulation provided by the furniture piece to the room. | 1 | `-1`<br>`-2`<br>`1` |

</details>


---


### Object: `DelayedWind`


**Definition:** Defines the properties for a delayed wind effect applied on melee damage.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#object-addstatustomeleedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 1 | `-3`<br>`10`<br>`2` |

</details>


---


### Object: `DamageIfDidntUseSpecificAbility`


**Definition:** Deals a specified amount of damage if the unit did not use a designated ability on its previous turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |

</details>


---


### Object: `Conditional_SourceHasTag`


**Definition:** Defines a conditional block that applies effects only if the source of the effect has a specified tag.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 1 | `{ . . . }` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `Conditional_GoodRoll`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `Conditional_DoesDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `Conditional_DoesDamage`


**Definition:** An object defining status effects and their probabilities to apply when the unit deals damage.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#object-addstatustoreceiveddamage_excludestatuses)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `AddTemporaryEffectsToEquipment`


**Definition:** An object whose nested keys define temporary status effects added to equipment.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CastAgain` | Integer / String | The number of additional times the ability can be cast this turn. | 1 | `1`<br>`2`<br>`3` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---


### Object: `AddStatusToSpells`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>
### Object: `AddStatusToReceivedDamage_ExcludeStatuses`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `AddStatusToReceivedDamage_ExcludeStatuses`


**Definition:** An object defining statuses applied to the attacking unit when the owner receives damage, excluding damage from sources carrying the specified statuses.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `AddStatusToKnockbackDamage`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
### Object: `AddStatusesToReceivedElementalDamage`


**Definition:** An object defining statuses applied to the unit when it takes elemental damage of the specified types.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `AddStatusesIfPersistentWeatherElement`


**Definition:** Specifies statuses applied if the persistent weather matches the given elements.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`passives`](./Passives_and_Statuses.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`elements`](../Reference_and_Meta/Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 1 | `[`<br>`[Heat Fire]` |
| `Burn` | Enum / Equation | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |

</details>


---


### Object: `AbilityChargeRefundChance`


**Definition:** An object containing a percentage chance to refund an ability charge, with an advantage softcap.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Passives_and_Statuses.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `advantage_softcap` | Float | The soft cap multiplier for ability charge refund advantage. | 1 | `3.5` |

</details>


---


### Object: `Zombie`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
### Object: `WobblyCat`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `Weakness`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Vengeful`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Vegan`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `UseAbilityWhenOutOfStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 0 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `UseAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `respect_prime` | Boolean | If true, the ability will only be used if the unit is primed for it. | 0 | `true` |


### Object: `UnlimitedDeathRattleRevive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 0 | `true` |


### Object: `TwisterFling`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 0 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 0 | `2`<br>`20`<br>`3` |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 0 | `2`<br>`3`<br>`4` |


### Object: `TVBotScreen`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Die`](../Reference_and_Meta/Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 0 | `{ . . . }`<br>`1`<br>`6` |
| [`Dumb`](../Reference_and_Meta/Miscellaneous.md#object-dumb) | Integer / Object | Defines the 'Dumb' form, which can be either a numeric value or an object with passives that disable spells and turn off TV. | 0 | `{ . . . }`<br>`3` |
| [`Obey`](../Reference_and_Meta/Miscellaneous.md#object-obey) | Integer / Object | As an object, defines an obey form that disables attacks and reacts with TV off. As an integer, defines a value (e.g., weight or count). | 0 | `{ . . . }`<br>`1` |
| [`Stop`](../Reference_and_Meta/Miscellaneous.md#object-stop) | Integer / Object | If an integer, the number of turns the unit is stopped. If an object, the form configuration for the stopped state. | 0 | `{ . . . }`<br>`2` |
| `Fuck` | Integer | The number of times the TV bot screen displays the 'Fuck' message. | 0 | `5` |
| `Shit` | Integer | The number of times the TV bot screen displays the 'Shit' message. | 0 | `4` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `TunnelVision`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_chance` | Equation | The chance for the damage instance to critically hit, expressed as a percentage or equation; values above 1 default to 100%. | 0 | `-999999`<br>`.05*X`<br>`.25` |


### Object: `Triskaidekaphobia`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `Trapper`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 0 | `1`<br>`10`<br>`2` |
| `cancel_movement` | Boolean | If true, the trapper cancels the trapped unit's movement. | 0 | `false` |
| `pathfinding_avoidance` | Integer | The weight that makes other units avoid traversing this tile during pathfinding. | 0 | `250` |


### Object: `TransformOnStatusThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 0 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 0 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `TransformOnElementInfluencex`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 0 | `Electric`<br>`Fire`<br>`Gravity` |


### Object: `TransformOnElementInfluence`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 0 | `Electric`<br>`Fire`<br>`Gravity` |


### Object: `TransformOnDeathImmediately`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`first_turn`](../Reference_and_Meta/Enums.md#enum-first_turn) | Enum   | Determines when the spawned unit takes its first turn relative to the spawn event. | 0 | `end_of_round`<br>`initiative`<br>`keep_turns` |
| [`obj`](../Reference_and_Meta/Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 0 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |


### Object: `TransformItemOnElementInfluence`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 0 | `Electric`<br>`Fire`<br>`Gravity` |
| [`item`](../Reference_and_Meta/Enums.md#enum-item) | Enum | Specifies the item to transform into, either by name, a nested item object, or a numeric value. | 0 | `1`<br>`2`<br>`EstusFlask_Full` |
| `full_repair` | Boolean | If true, the item's durability is fully restored when transformed by element influence. | 0 | `true` |


### Object: `TransformInXTurns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 0 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`turns`](../Reference_and_Meta/Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 0 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`initiative`](../Reference_and_Meta/Enums.md#enum-initiative) | Enum / Integer  | The unit's turn order priority; can be an integer modifier or 'keep_turns_end_turn' to force end of turn after acting. | 0 | `-10`<br>`-100`<br>`-20` |


### Object: `Trample`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TintItem`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`add`](../Reference_and_Meta/Arrays.md#array-add) | Array / Integer | The amount or an array of values added to the event's advantage or item tint. | 0 | `5`<br>`[0.05 0.05 0.05]` |
| [`ignore_if_str_aux_equals`](../Reference_and_Meta/Enums.md#enum-ignore_if_str_aux_equals) | Enum | Specifies the string aux value at which to ignore the tinting operation. | 0 | `ModelingClay_Default` |
| [`mul`](../Reference_and_Meta/Arrays.md#array-mul) | Array | An array of three floats (RGB) used to multiply the item's tint color. | 0 | `[0.45 0.3 0.25]` |


### Object: `TinkererBasicAttackSwitching`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`craft_ability`](../Reference_and_Meta/Enums.md#enum-craft_ability) | Enum   | The ability used for the craft action in the Tinkerer's basic attack switching. | 0 | `TinkererCraft` |
| [`throw_ability`](../Reference_and_Meta/Enums.md#enum-throw_ability) | Enum   | The ability used for the throw action in the Tinkerer's basic attack switching. | 0 | `TinkererThrow` |


### Object: `Thorns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `TerminatorSkin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 0 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`groups`](../Reference_and_Meta/Arrays.md#array-groups) | Array  | Groups of actors that this skin applies to. | 0 | `[` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `TerminatorChase`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 0 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |


### Object: `Terminator2Run`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_weights`](../Reference_and_Meta/Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 0 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |
| [`move_ability`](../Reference_and_Meta/Enums.md#enum-move_ability) | Enum   | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 0 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |


### Object: `TempInitiativeChange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Tech`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `T3HitlerSpawningPhase`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`spell_use_groups`](../Reference_and_Meta/Arrays.md#array-spell_use_groups) | Array   | List of spell use groups that the spawning phase can use. | 0 | `[` |


### Object: `SyncFormsWithBuddy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`no_buddy`](../Reference_and_Meta/Enums.md#enum-no_buddy) | Enum   | Specifies an alternative form to use when there is no buddy. | 0 | `Rage` |


### Object: `SwimmingFormChange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_in`](../Reference_and_Meta/Enums.md#enum-form_in) | Enum   | Determines the form to change into when entering water. | 0 | `Water` |
| [`form_out`](../Reference_and_Meta/Enums.md#enum-form_out) | Enum   | Determines the form to change into when leaving water. | 0 | `Out` |


### Object: `SupportFormChangeInsteadOfRun`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `wait_till_turn` | Boolean | If true, the form change will not occur until the unit's next turn. | 0 | `true` |


### Object: `SupportDieInsteadOfRun`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_dead_ani`](../Reference_and_Meta/Enums.md#enum-alt_dead_ani) | Enum   | Specifies the alternative death animation to use when the support unit dies instead of running. | 0 | `off` |
| [`alt_dying_ani`](../Reference_and_Meta/Enums.md#enum-alt_dying_ani) | Enum   | Specifies the alternative dying animation to use. | 0 | `shutdown` |


### Object: `StunImmunity`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cleanse_on_apply` | Boolean | If true, removes any existing stun effect when this immunity is applied. | 0 | `false` |


### Object: `StrengthUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StrengthForEachNeighboringEnemy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Stealth`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `StatusWhenStatusCompletelyRemoved`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 0 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 0 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusRandomEnemiesOnBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 0 | `1`<br>`10`<br>`2` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 0 | `1`<br>`10`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 0 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 0 | `1`<br>`2`<br>`[1 .01]` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 0 | `1`<br>`2`<br>`3` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusOverlappingCharactersAndDie`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 0 | `1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusOnTakeHealthOrShieldDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` 
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 0 | `{ . . . }` |
| [`Metronome`](../Reference_and_Meta/Miscellaneous.md#object-metronome) | Boolean (Flag) / Float / Object  | The number of times Metronome triggers, or an object with stacks and banned abilities. | 0 | `{ . . . }`<br>`1`<br>`2` |


### Object: `StatusOnSpawnIn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `SetHealth` | Integer | Sets the target's health to a specific flat value or percentage. | 0 | `1`<br>`100%`<br>`50%` |
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 0 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusOnSetPieceBreak`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 2 | passives<br>class<br>tag |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 0 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 0 | `-1`<br>`-2`<br>`1` |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 0 | `-1`<br>`1`<br>`2` |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 0 | `1`<br>`2` |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 0 | `-1`<br>`1`<br>`2` |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. | 0 | `1`<br>`2` |
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. | 0 | `1`<br>`2` |
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. | 0 | `1`<br>`2` |


### Object: `StatusOnFullMana`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_OncePerBattle`](./Items_and_Equipment.md#object-conditional_onceperbattle) | Object | An object containing effects that can only trigger once per battle, preventing double-activation. | 0 | `{ . . . }` |


### Object: `StatusOnFallAsleep`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 0 | `-1`<br>`-2`<br>`1` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 0 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 0 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusOnEnemyDeath`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Equation | The number of charge stacks applied. | 0 | `1`<br>`2`<br>`3` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusOnEnemyConfused`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](../Reference_and_Meta/Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 0 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |


### Object: `StatusOnEnemyCastSpell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 0 | `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 0 | `1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusOnDodge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 0 | `1`<br>`10`<br>`100` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusOnDie`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 5 | passives<br>class<br>tag |
| [`RandomMagicMissile`](../Reference_and_Meta/Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 0 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`ScatterCoins`](../Reference_and_Meta/Miscellaneous.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 0 | `{ . . . }` |
| `RemoveAmbientLightEffects` | Float | The fade-out duration in seconds for ambient light effects. | 0 | `.5`<br>`4` |


### Object: `StatusOnBreak`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | [`Bruise`](#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 11 | passives<br>class<br>tag |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 0 | `1`<br>`2`<br>`3` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 0 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `HealthGain` | Integer | The amount of health restored to the source. | 0 | `1`<br>`10`<br>`2` |
| [`ConstitutionUp`](../Reference_and_Meta/Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 0 | `-1`<br>`-2`<br>`1` |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 0 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 0 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 0 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `DexterityUp` | Array / Equation | The amount of dexterity change, or a keyword like 'item_aux'. | 0 | `-1`<br>`1`<br>`2` |
| [`ApplyToRandomPartyMemberIfPossible`](../Reference_and_Meta/Miscellaneous.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. | 0 | `{ . . . }` |


### Object: `StatusOnBackstab`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. | 0 | `1`<br>`10`<br>`2` |
| `SerratedClaws` | Integer | The number of stacks of the SerratedClaws status applied, or an object defining its display strings. | 0 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusIfUnusedActPoints`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of backflip charges, or an object defining its ability. | 1 | Default<br>FormChange<br>Druid |
| [`Craft`](./Passives_and_Statuses.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 0 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusIfDidntMove`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Equation | The number of charge stacks applied. | 0 | `1`<br>`2`<br>`3` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusEveryXSpellCastsEachTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `HealthGain` | Integer | The amount of health restored to the source. | 0 | `1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusEachTurnEndIfEnabledAtStartOfTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 0 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |


### Object: `StatusEachTurnBeginIfHasStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`animation`](../Reference_and_Meta/Enums.md#enum-animation) | Enum  | Specifies the animation played when the ability is used. | 0 | `"bat"`<br>`"rally"`<br>`ColorlessStartTurn` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 0 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 0 | `-1`<br>`-2`<br>`1` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 0 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 0 | `1`<br>`10`<br>`2` |
| `consume` | Boolean | If true, the status is consumed after triggering. | 0 | `true` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusEachRoundEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 0 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [`DoDamage`](../Reference_and_Meta/Miscellaneous.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. | 0 | `{ . . . }` |


### Object: `StatusEachRoundBegin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `NonStackingShield` | Number | The amount of non-stacking shield granted. | 0 | `12`<br>`16`<br>`3` |


### Object: `StatusCollector`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 0 | `1`<br>`10`<br>`2` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 0 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| `StrengthUp` | Enum / Equation | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 0 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusAllCharactersOnSpawn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` | [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 0 | Default<br>FormChange<br>Druid |
| [`Poison`](../Reference_and_Meta/Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 0 | `1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatusAfterXTurns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 0 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |


### Object: `StatusAdjacentOnTheirTurnEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveAway` | Integer | The distance to force the target away from the source. | 0 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `StatDependentPassive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamageToBasicAttack` | String | Additional damage added to the basic attack, either as a flat value or formula. | 0 | `1`<br>`2`<br>`4` |


### Object: `StackingFlowerTrail`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`stack_key`](../Reference_and_Meta/Enums.md#enum-stack_key) | Enum | Specifies the key of the status stack to check for the condition. | 0 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |


### Object: `SproutsGrantMovement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `SpewerAltGraphics`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Fire`](./Passives_and_Statuses.md#object-fire) | Integer / Object | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 0 | `{ . . . }`<br>`1` |
| [`Normal`](../Reference_and_Meta/Miscellaneous.md#object-normal) | Integer / Object | The normal form configuration, used as a baseline state for shape-shifting units. | 0 | `{ . . . }`<br>`0` |
| [`Tar`](../Reference_and_Meta/Miscellaneous.md#object-tar) | Integer / Object | If an integer, the number of tar stacks. If an object, the form state for the tar-covered unit. | 0 | `{ . . . }`<br>`2` |
| [`FireFull`](../Reference_and_Meta/Miscellaneous.md#object-firefull) | Integer / Object | Defines the 'FireFull' form, a fully charged fire state with its own animation and visual combo. | 0 | `{ . . . }`<br>`1` |
| [`NormalFull`](../Reference_and_Meta/Miscellaneous.md#object-normalfull) | Integer / Object | As an object, defines the normal full form with a spit attack and conditional form change. As an integer, specifies alt graphics index. | 0 | `{ . . . }`<br>`0` |
| [`TarFull`](../Reference_and_Meta/Miscellaneous.md#object-tarfull) | Integer / Object | If an integer, the number of full tar stacks. If an object, the form state for the fully tar-covered unit. | 0 | `{ . . . }`<br>`2` |


### Object: `SpellDamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SpeedUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SpawnRandomPickupsOnTaggedUnitKilled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 0 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 0 | `0`<br>`1`<br>`10` |


### Object: `SpawnOnDeath`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`faction`](../Reference_and_Meta/Enums.md#enum-faction) | Enum  | Specifies the faction of a spawned unit or projectile, determining its team allegiance and AI behavior. | 0 | `allies`<br>`auto`<br>`birds` |
| [`obj`](../Reference_and_Meta/Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 0 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| [`additional_statuses`](../Reference_and_Meta/Miscellaneous.md#object-additional_statuses) | Object | Additional status effects applied to the spawned unit on death. | 0 | `{ . . . }` |


### Object: `SpawnObjectOnPopCorpse`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 0 | `0`<br>`1`<br>`10` |
| `except_tiny` | Boolean | If true, the spawning effect is not triggered for tiny (small) corpses. | 0 | `true` |


### Object: `SpawnItemLinkedFamiliar`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `break_on_pop_only` | Boolean | If true, the linked familiar spawn only breaks when the item is popped. | 0 | `true` |


### Object: `SpawnExtraThingsOnBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`tile`](../Reference_and_Meta/Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 0 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 0 | `1`<br>`10`<br>`2` |
| [`trap`](../Reference_and_Meta/Enums.md#enum-trap) | Enum | The type of trap to spawn. Specifies which trap template to use. | 0 | `BearTrap`<br>`LandMine`<br>`WaterKittenTrap` |


### Object: `SpawnCatCopyWhenDowned`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`prevent_chain_tag`](../Reference_and_Meta/Enums.md#enum-prevent_chain_tag) | Enum   | A tag that prevents chaining of spawns from the same source. | 0 | `ancestorset_shade`<br>`eb_twin`<br>`minime_clone` |


### Object: `SmallRockBehavior`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Equation / Object | Specifies the amount of damage dealt, can be a number or expression. | 0 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 0 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `chain` | Boolean | Specifies the ability to chain into and execute. | 0 | `AcidSplash`<br>`CaveSplash`<br>`FireFullSmall` |


### Object: `Slow`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SlotMachineRollPool`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SlotResult_Jackpot_Coins`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-slotresult_jackpot_coins) | Integer / Object | The result of a jackpot roll that spawns coins, or the weight of that result in the pool. | 0 | `{ . . . }`<br>`1` |
| [`SlotResult_Explode`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-slotresult_explode) | Integer / Object | The result of an explosion roll, or the weight of that result. | 0 | `{ . . . }`<br>`1` |
| [`SlotResult_Nothing`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-slotresult_nothing) | Integer / Object | The result of a nothing roll, or the weight of that result. | 0 | `{ . . . }`<br>`7` |
| [`SlotResult_RandomPickup`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-slotresult_randompickup) | Integer / Object | The result of a random pickup roll, or the weight of that result. | 0 | `{ . . . }`<br>`11` |


### Object: `SkipFirstRounds`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `pop_chance` | Integer | The percentage chance that the first round is skipped. | 0 | `50%` |


### Object: `ShovingMatch`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ShoulderCheck`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `SharePickups`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_coins` | Boolean | If true, coins are included in the shared pickup pool. | 0 | `true` |


### Object: `Scleroderma`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `SchrodingerDisorder`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `ScalingAttackAnimation`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](../Reference_and_Meta/Miscellaneous.md#object-default) | Enum / Object | The default configuration or value used when no specific override is provided. | 0 | `{ . . . }`<br>`bite1` |
| [`thresholds`](../Reference_and_Meta/Arrays.md#array-thresholds) | Array  | An array of health percentage thresholds that trigger an alt state. | 0 | `[` |


### Object: `ScaledStatusOnHolyShieldBlock`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomMagicMissile`](../Reference_and_Meta/Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 0 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `ScaledStatusAlliesOnSpendMana`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | 0 | Default<br>FormChange<br>Druid | `Key`<br>`Default`<br>`FormChange` 
| [`Conditional_Adjacent`](./Passives_and_Statuses.md#object-conditional_adjacent) | Object | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 0 | `{ . . . }` |


### Object: `ScaldingOrbMoonBossOneShot`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CompleteItemQuest`](../Reference_and_Meta/Enums.md#enum-completeitemquest) | Enum | Specifies the item quest ID to mark as complete on kill. | 0 | `BlackShard`<br>`Nuke`<br>`ScaldingOrb` |
| [`RemoveItem`](../Reference_and_Meta/Enums.md#enum-removeitem) | Enum | Specifies the item ID to remove from the source on kill. | 0 | `BlackShard`<br>`BlackShard_Glowing`<br>`ScaldingOrb` |


### Object: `SafeDoomed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `RunWhenLastPlayerCatIsCharmed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allow_decision_mid_turn` | Boolean | If true, allows the decision to run to occur mid-turn instead of at the end. | 0 | `true` |
| [`legacy_savekey`](../Reference_and_Meta/Enums.md#enum-legacy_savekey) | Enum   | Specifies the save key used to persist a legacy stolen cat ID. | 0 | `Legacy_Marshmallow_StolenCatID` |


### Object: `RefreshEquipmentAbilityOnElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 0 | `Electric`<br>`Fire`<br>`Gravity` |
| [`text`](../Assets_and_Localization/Strings.md#string-text) | String | The localization key for the name of this injury. | 0 | `""`<br>`"COMBAT_POPUP_RECHARGED"`<br>`"INJURY_NAME_BROKENLEG"` |


### Object: `ReflectProjectiles`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](../Reference_and_Meta/Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 0 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |


### Object: `ReduceManaCost`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Quivered`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Quiver`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ProtectTargetedAllies`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`target_filter`](../Reference_and_Meta/Enums.md#enum-target_filter) | Enum   | Specifies which targets the protection applies to, based on their unit type or tag. | 0 | `Kitten`<br>`any` |


### Object: `PoopWhenHit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 0 | `.02`<br>`.1`<br>`.15` |


### Object: `PoisonThorns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Poison`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `PermanentMadness`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `PermanentImmobile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `PassiveWhileShielded`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 0 | `1`<br>`2`<br>`3` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `PassiveWhileNotHasStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 0 | `{ . . . }` |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 0 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |


### Object: `PassiveWhileHasDurability`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | 0 | Default<br>FormChange<br>Druid | `Key`<br>`Default`<br>`FormChange` 
| [`MovementReaction`](./Passives_and_Statuses.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 0 | `{ . . . }` |


### Object: `PassiveWhenOnTile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 0 | `{ . . . }` |
| [`tile`](../Reference_and_Meta/Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 0 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |


### Object: `PassiveWhenDead`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` | [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 0 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` 


### Object: `PassiveIfWeaponIsUsable`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 0 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `PassiveIfStrAuxEquals`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 0 | `{ . . . }` |
| `value` | Enum | The numeric value or formula associated with the buff. | 0 | `.5`<br>`0`<br>`1` |


### Object: `Paranoia`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `ObjectDetector`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 0 | `.02`<br>`.1`<br>`.15` |


### Object: `NumbingLeeches`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `NonStackingDivineShield`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `NoManaRegen`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MutateAfterXTurns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MultiSpawnOnDeath`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 0 | `0`<br>`1`<br>`10` |
| [`obj`](../Reference_and_Meta/Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 0 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |


### Object: `MoveTowardsKillers`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](../Reference_and_Meta/Enums.md#enum-move_ability) | Enum   | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 0 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| [`character_filter`](../Reference_and_Meta/Arrays.md#array-character_filter) | Array   | Specifies which characters to consider as killers when moving towards them. | 0 | `[SpiderCat, TallSpiderCat]` |


### Object: `MoveQuivered`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MoveAwayWhenEnemyAdjacent`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](../Reference_and_Meta/Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 0 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |
| [`move_ability`](../Reference_and_Meta/Enums.md#enum-move_ability) | Enum   | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 0 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |
| `once_per_turn` | Boolean | If true, the movement away can only trigger once per turn. | 0 | `true` |


### Object: `MoveAwayFromDamageSource`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`move_ability`](../Reference_and_Meta/Enums.md#enum-move_ability) | Enum   | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 0 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |


### Object: `MoveAfterAnyAttemptedAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](../Reference_and_Meta/Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 0 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |


### Object: `Mount`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eject_ability`](../Reference_and_Meta/Enums.md#enum-eject_ability) | Enum   | Specifies the ability used to eject the mounted character. | 0 | `MechSuitEject` |
| [`enter_ability`](../Reference_and_Meta/Enums.md#enum-enter_ability) | Enum   | Specifies the ability used to enter the mount. | 0 | `EnterMech` |


### Object: `MotherTumorSpawnInCapture`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](../Reference_and_Meta/Miscellaneous.md#object-cat) | Object | Defines the behavior and form change for captured cat units. | 0 | `{ . . . }` |
| [`NonCat`](../Reference_and_Meta/Miscellaneous.md#object-noncat) | Object | Defines the behavior and form change for captured non-cat units. | 0 | `{ . . . }` |
| [`Nothing`](../Reference_and_Meta/Miscellaneous.md#object-nothing) | Object | Defines the behavior when nothing is captured, typically just an animation. | 0 | `{ . . . }` |


### Object: `MotherTumorPassive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cat`](../Reference_and_Meta/Miscellaneous.md#object-cat) | Object | Defines the behavior and form change for captured cat units. | 0 | `{ . . . }` |
| [`NonCat`](../Reference_and_Meta/Miscellaneous.md#object-noncat) | Object | Defines the behavior and form change for captured non-cat units. | 0 | `{ . . . }` |
| [`considered_forms`](../Reference_and_Meta/Arrays.md#array-considered_forms) | Array   | An array of form names the tumor considers for interaction. | 0 | `[Big BigHolding BigHoldingCat]` |
| [`grow_ability`](../Reference_and_Meta/Enums.md#enum-grow_ability) | Enum   | Specifies the ability used by the tumor to grow. | 0 | `MotherTumorGrow` |
| [`pass_ani`](../Reference_and_Meta/Enums.md#enum-pass_ani) | Enum   | Specifies the animation played when passing something to the tumor. | 0 | `pass` |
| [`receive_ani`](../Reference_and_Meta/Enums.md#enum-receive_ani) | Enum   | Specifies the animation played when receiving something from the tumor. | 0 | `receive` |


### Object: `MotherGrowController`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eat_damage`](../Reference_and_Meta/Miscellaneous.md#object-eat_damage) | Object | An object defining the damage properties of the eat attack. | 0 | `{ . . . }` |
| [`tumor_object`](../Reference_and_Meta/Enums.md#enum-tumor_object) | Enum   | Specifies the name of the tumor object to spawn. | 0 | `MotherTumor` |


### Object: `MonkCatReactionAbilities`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum  | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 0 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |
| [`move`](../Reference_and_Meta/Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 0 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`spell`](../Reference_and_Meta/Enums.md#enum-spell) | Enum  | Specifies the spell ability to use as a reaction. | 0 | `MCHadouken` |
| [`trinket`](../Reference_and_Meta/Enums.md#enum-trinket) | Enum  | The name of the trinket item the unit starts with. | 0 | `MCHadouken`<br>`MonkStyleChanger` |
| [`weapon`](../Reference_and_Meta/Enums.md#enum-weapon) | Enum | The name of the weapon item the unit starts with. | 0 | `AstroTaser`<br>`ButcherHook`<br>`CaveCatClub` |


### Object: `ModularPickup`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleanse`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 0 | `{ . . . }`<br>`0`<br>`1` |
| [`sound_event`](../Reference_and_Meta/Enums.md#enum-sound_event) | Enum   | Specifies the sound event to play when the pickup is used. | 0 | `EatAntidote` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `MissChance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MetalDetector`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Metal`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `MegaDinoDropController`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head_drop`](../Reference_and_Meta/Enums.md#enum-head_drop) | Enum   | Specifies the ability triggered when the head drops down. | 0 | `MD_HeadDrop` |
| [`leg_leave`](../Reference_and_Meta/Enums.md#enum-leg_leave) | Enum   | Specifies the ability triggered when the legs leave the body. | 0 | `MD_LegLeave` |
| [`leg_return`](../Reference_and_Meta/Enums.md#enum-leg_return) | Enum   | Specifies the ability triggered when the legs return to the body. | 0 | `MD_LegReturn` |
| `stable_legs` | Integer | The number of legs that must be stable for the head to drop. | 0 | `3` |


### Object: `ManaPickup`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`frame_range`](../Reference_and_Meta/Arrays.md#array-frame_range) | Array   | Specifies the minimum and maximum animation frame for the health pickup. | 0 | `[1 2]`<br>`[11 12]`<br>`[13 13]` |


### Object: `Madness`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `tickdown_this_turn` | Boolean | If true, madness stacks decrease at the start of this turn instead of the next. | 0 | `true` |


### Object: `LuckUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Lifesteal`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `KineticSpikes`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `KillsHeal`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `JohnnyNeedsWashing`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_unwashed`](../Reference_and_Meta/Enums.md#enum-form_unwashed) | Enum   | Specifies the form name for the unwashed state. | 0 | `Unwashed` |
| [`form_washed`](../Reference_and_Meta/Enums.md#enum-form_washed) | Enum   | Specifies the form name for the washed state. | 0 | `Washed` |


### Object: `ItemAuxTransform`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`le`](../Reference_and_Meta/Arrays.md#array-le) | Array | An array specifying a [aux value, item] pair to transform to when the aux value is less than or equal to a specific value. | 0 | `[10 MoneyBag_Small]`<br>`[25 MoneyBag_Medium]`<br>`[50 MoneyBag_Large]` |
| [`ge`](../Reference_and_Meta/Arrays.md#array-ge) | Array | An array specifying a [durability, item] pair to transform to when durability is greater than or equal to a specific value. | 0 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |
| [`lt`](../Reference_and_Meta/Arrays.md#array-lt) | Array | An array specifying a [aux value, item] pair to transform to when the aux value is strictly less than a specific value. | 0 | `[10 NuclearKnife]` |


### Object: `ImmortalLeeches`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Immobile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ImmediateAbilityReaction`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 0 | `true` |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 0 | `true` |
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 0 | `true` |
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 0 | `-1`<br>`150`<br>`50` |
| `damage_threshold` | Integer | The amount of damage that must be dealt to trigger the ability reaction. | 0 | `10` |
| `even_if_blocked` | Boolean | If true, the reaction triggers even if the damage is blocked. | 0 | `true` |
| `buddy_damage_only` | Boolean | If true, only damage dealt by the unit's buddy triggers the reaction. | 0 | `true` |
| `target_furthest_valid` | Boolean | If true, the reaction targets the furthest valid enemy. | 0 | `true` |


### Object: `Hypomania`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `HPAltStates`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`thresholds`](../Reference_and_Meta/Arrays.md#array-thresholds) | Array  | An array of health percentage thresholds that trigger an alt state. | 0 | `[` |
| [`clipname`](../Reference_and_Meta/Enums.md#enum-clipname) | Enum  | Specifies the animation clip name to use for the alt state. | 0 | `poopmain` |


### Object: `HitlerExecute`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 0 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 0 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |


### Object: `HealthRegenUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `HealthPickup`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`frame_range`](../Reference_and_Meta/Arrays.md#array-frame_range) | Array   | Specifies the minimum and maximum animation frame for the health pickup. | 0 | `[1 2]`<br>`[11 12]`<br>`[13 13]` |
| `stored_food_value` | Integer | The amount of food value stored in this pickup. | 0 | `0`<br>`1`<br>`2` |
| `anything_eats` | Boolean | If true, any unit can consume this health pickup. | 0 | `true` |
| `force_frame` | Integer | Forces the health pickup to use a specific animation frame. | 0 | `12` |


### Object: `HealNeighborsEachTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 0 | `false`<br>`true` |


### Object: `HealingAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `GlobalMeleeRevengeDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 0 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |


### Object: `GlobalFlowerTrapperAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Tangled`](../Reference_and_Meta/Miscellaneous.md#object-tangled) | Array / Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 0 | `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `GlobalFamiliarMoveBoost`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `GlobalFamiliarDamageBoost`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `FullPower`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FrankBolts`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `FragileDuringElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Fragile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FormChangeWhilePrimingAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`priming`](../Reference_and_Meta/Enums.md#enum-priming) | Enum  | Specifies the form name to use while the unit is priming an ability. | 0 | `DualSword_Primed`<br>`Priming`<br>`SwordAndShield_Primed` |
| [`not_priming`](../Reference_and_Meta/Enums.md#enum-not_priming) | Enum   | Specifies the form name to use when the unit is not priming an ability. | 0 | `DualSword`<br>`NotPriming`<br>`SwordAndShield` |


### Object: `FormChangeWhileHasStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 0 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`form_hasnot`](../Reference_and_Meta/Enums.md#enum-form_hasnot) | Enum   | Specifies a form that the unit must not be in for the status-triggered form change to occur. | 0 | `Big`<br>`CaveWoman`<br>`Close` |
| [`form_has`](../Reference_and_Meta/Enums.md#enum-form_has) | Enum   | Specifies a form that the unit must be in for the status-triggered form change to occur. | 0 | `BellyFull`<br>`CaveWomanHasCat`<br>`FireFull` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `FormChanger`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`default`](../Reference_and_Meta/Miscellaneous.md#object-default) | Enum / Object | The default configuration or value used when no specific override is provided. | 0 | `{ . . . }`<br>`bite1` |
| [`Colorless`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-colorless) | Array / Object | Specifies the 'Colorless' form within FormChanger, used for boss dialogue. | 0 | `{ . . . }`<br>`[` |
| [`Fire`](./Passives_and_Statuses.md#object-fire) | Integer / Object | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 0 | `{ . . . }`<br>`1` |
| [`Druid`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-druid) | Array / Object | Specifies the 'Druid' form within FormChanger, used for boss dialogue. | 0 | `{ . . . }`<br>`[` |
| [`Necromancer`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-necromancer) | Array / Object | Defines a list of quotes for the Necromancer class. | 0 | `{ . . . }`<br>`[` |
| [`Butcher`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-butcher) | Object | Specifies the 'Butcher' form within FormChanger, used for boss dialogue. | 0 | `{ . . . }` |
| [`Fighter`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-fighter) | Array / Object | Specifies the 'Fighter' form within FormChanger, used for boss dialogue. | 0 | `{ . . . }`<br>`[` |
| [`Hunter`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-hunter) | Array / Object | Defines a list of quotes for the Hunter class (vs boss, embark, return early). | 0 | `{ . . . }`<br>`[` |
| [`Mage`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-mage) | Array / Object | Defines a list of quotes for the Mage class. | 0 | `{ . . . }`<br>`[` |
| [`Thief`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-thief) | Array / Object | Form identifier for the Thief boss type. | 0 | `{ . . . }`<br>`[` |
| [`Tinkerer`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-tinkerer) | Array / Object | Form identifier for the Tinkerer boss type. | 0 | `{ . . . }`<br>`[` |
| [`Tank`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-tank) | Array / Object | Form identifier for the Tank boss type, used for dialogue references. | 0 | `{ . . . }`<br>`[` |
| [`Monk`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-monk) | Array / Object | Defines a list of quotes for the Monk class. | 0 | `{ . . . }`<br>`[` |
| [`Psychic`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-psychic) | Array / Object | Form identifier for the Psychic boss type, used for dialogue references. | 0 | `{ . . . }`<br>`[` |
| [`Medic`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-medic) | Array / Object | Defines a list of quotes for the Medic class. | 0 | `{ . . . }`<br>`[` |
| [`Holy`](./Passives_and_Statuses.md#object-holy) | Enum / Object | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 0 | `{ . . . }`<br>`MegaGuppy_TransformHoly` |
| [`Default`](../Reference_and_Meta/Miscellaneous.md#object-default) | Enum / Object | The default form configuration for a unit, containing its standard stats and abilities. | 0 | `{ . . . }`<br>`release` |
| [`Water`](./Passives_and_Statuses.md#object-water) | Object | Form state for water element, applying a puddle or movement bonus. | 0 | `{ . . . }` |
| [`initial_form`](../Reference_and_Meta/Enums.md#enum-initial_form) | Enum / Integer   | Specifies the starting form name for a unit with FormChanger. | 0 | `0`<br>`1`<br>`5` |
| [`Big`](../Reference_and_Meta/Miscellaneous.md#object-big) | Object | Defines the 'Big' form, including its animation, attack, passives, and positional data. | 0 | `{ . . . }` |
| [`Normal`](../Reference_and_Meta/Miscellaneous.md#object-normal) | Integer / Object | The normal form configuration, used as a baseline state for shape-shifting units. | 0 | `{ . . . }`<br>`0` |
| [`Rage`](../Reference_and_Meta/Miscellaneous.md#object-rage) | Object | The rage form configuration, applied when the unit enters an enraged state. | 0 | `{ . . . }` |
| [`Rain`](../Reference_and_Meta/Miscellaneous.md#object-rain) | Object  | Defines the rain weather effect with associated particle, sound, and rendering settings. | 0 | `{ . . . }` |
| [`Bomb`](../Reference_and_Meta/Miscellaneous.md#object-bomb) | Boolean (Flag) / Object | Defines the 'Bomb' form, an explosive state that triggers an ability on death. | 0 | `{ . . . }` |
| [`Cultist`](../Reference_and_Meta/Miscellaneous.md#object-cultist) | Object | Defines the 'Cultist' form, a basic melee form with its own name and tooltip. | 0 | `{ . . . }` |
| [`Up`](../Reference_and_Meta/Miscellaneous.md#object-up) | Object | Defines the 'Up' form, including its animation, AI behavior, and passives such as UpTireBehavior. | 0 | `{ . . . }` |
| [`Small`](../Reference_and_Meta/Miscellaneous.md#object-small) | Object | Defines the 'Small' form, typically used for smaller size variants, with its own attack and animation. | 0 | `{ . . . }` |
| [`Nuke`](../Reference_and_Meta/Miscellaneous.md#object-nuke) | Object | Defines a nuke form with no attack or movement options. | 0 | `{ . . . }` |
| [`Full`](../Reference_and_Meta/Miscellaneous.md#object-full) | Object | The form configuration applied when the unit is in a full state. | 0 | `{ . . . }` |
| [`Zealot`](../Reference_and_Meta/Miscellaneous.md#object-zealot) | Object | Form state for the zealot variant of a cultist, with a stabbing attack. | 0 | `{ . . . }` |
| [`HasCat`](../Reference_and_Meta/Miscellaneous.md#object-hascat) | Object | The form configuration applied when the unit is holding or has swallowed a cat. | 0 | `{ . . . }` |
| [`hot`](../Reference_and_Meta/Miscellaneous.md#object-hot) | Object | The form configuration applied when the unit is in a hot state, granting fire element. | 0 | `{ . . . }` |
| [`Bishop`](../Reference_and_Meta/Miscellaneous.md#object-bishop) | Boolean (Flag) / Object | Defines the 'Bishop' form for Cultist enemies, with its own attack (BBXLightning) and animation. | 0 | `{ . . . }` |
| [`Mutant`](../Reference_and_Meta/Miscellaneous.md#object-mutant) | Integer / Object | As an object, defines the mutant form with reduced move speed and custom name. As an integer, defines spawn weight. | 0 | `{ . . . }`<br>`1` |
| [`Down`](../Reference_and_Meta/Miscellaneous.md#object-down) | Object | The form configuration applied when the unit is in a knocked-down or prone state. | 0 | `{ . . . }` |
| [`CaveMan`](../Reference_and_Meta/Miscellaneous.md#object-caveman) | Object | Defines the 'CaveMan' form of a CavePerson enemy, including its animation, attack, and passives. | 0 | `{ . . . }` |
| [`Die`](../Reference_and_Meta/Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 0 | `{ . . . }`<br>`1`<br>`6` |
| [`Johnny`](../Reference_and_Meta/Miscellaneous.md#object-johnny) | Object | Defines a form that executes a mega blast, side switch, and form switch in sequence. | 0 | `{ . . . }` |
| [`OffMap`](../Reference_and_Meta/Miscellaneous.md#object-offmap) | Object | The form configuration applied when the unit is off the battlefield map. | 0 | `{ . . . }` |
| [`passive`](../Reference_and_Meta/Miscellaneous.md#object-passive) | Object | Defines the passive form, where the unit does nothing (uses DoNothing attack) and is inactive. | 0 | `{ . . . }` |
| [`CaveBaby`](../Reference_and_Meta/Miscellaneous.md#object-cavebaby) | Object | Defines the 'CaveBaby' form of a CavePerson enemy, with reduced health and baby attack. | 0 | `{ . . . }` |
| [`Flush`](../Reference_and_Meta/Miscellaneous.md#object-flush) | Object | Defines a form that executes a sequence of actions (FlushX, side switch, form switch) and has a spell with a localized name. | 0 | `{ . . . }` |
| [`Boris`](../Reference_and_Meta/Miscellaneous.md#object-boris) | Enum / Object | Specifies the 'Boris' form within FormChanger, with its own animation suffix and passives. | 0 | `{ . . . }`<br>`MegaGuppy_TransformBoris` |
| [`Empty`](../Reference_and_Meta/Miscellaneous.md#object-empty) | Object | Defines the 'Empty' form, typically indicating a state with no content (e.g., empty stomach). | 0 | `{ . . . }` |
| [`WereMan`](../Reference_and_Meta/Miscellaneous.md#object-wereman) | Object | Form state for the were-man transformation, with fury swipe attack and sabertooth faction. | 0 | `{ . . . }` |
| [`SquirrelForm`](../Reference_and_Meta/Miscellaneous.md#object-squirrelform) | Object | Defines the 'SquirrelForm', a transformation used by units like DeathMetal, granting melee attack and speed bonuses. | 0 | `{ . . . }` |
| [`active`](../Reference_and_Meta/Miscellaneous.md#object-active) | Object | Defines the active form, containing passives and abilities that are active while in this form. | 0 | `{ . . . }` |
| [`CaveWoman`](../Reference_and_Meta/Miscellaneous.md#object-cavewoman) | Object | Defines the 'CaveWoman' form of a CavePerson enemy, with kick attack and higher health. | 0 | `{ . . . }` |
| [`LastHit`](../Reference_and_Meta/Miscellaneous.md#object-lasthit) | Object | Defines a form that grants 2 dispersed bonus turns after the last hit. | 0 | `{ . . . }` |
| [`Tar`](../Reference_and_Meta/Miscellaneous.md#object-tar) | Integer / Object | If an integer, the number of tar stacks. If an object, the form state for the tar-covered unit. | 0 | `{ . . . }`<br>`2` |
| [`CaveManSpear`](../Reference_and_Meta/Miscellaneous.md#object-cavemanspear) | Object | Defines the 'CaveManSpear' form of a CavePerson enemy, with a spear attack and corresponding animation. | 0 | `{ . . . }` |
| [`Holding`](../Reference_and_Meta/Miscellaneous.md#object-holding) | Object | Defines the 'Holding' form, used when the unit is holding an object, with associated movement and form change behaviors. | 0 | `{ . . . }` |
| [`BigHolding`](../Reference_and_Meta/Miscellaneous.md#object-bigholding) | Object | Defines the 'BigHolding' form, a larger variant while holding an object, triggered by the Consuming status. | 0 | `{ . . . }` |
| [`BigHoldingCat`](../Reference_and_Meta/Miscellaneous.md#object-bigholdingcat) | Object | Defines the 'BigHoldingCat' form, a cat-sized variant of the holding form while Consuming. | 0 | `{ . . . }` |
| [`BlackHole`](../Reference_and_Meta/Miscellaneous.md#object-blackhole) | Object | Defines the 'BlackHole' form, a variant of NeutronStar with its own animation and name. | 0 | `{ . . . }` |
| [`DualSword`](../Reference_and_Meta/Miscellaneous.md#object-dualsword) | Object | Defines the 'DualSword' form of TheDestroyer, increasing move speed and using a dual sword attack. | 0 | `{ . . . }` |
| [`Explosive`](../Reference_and_Meta/Miscellaneous.md#object-explosive) | Enum / Object | Specifies the 'Explosive' form within FormChanger, with its own animation suffix and passives. | 0 | `{ . . . }`<br>`MegaGuppy_TransformExplosive` |
| [`Turtled`](../Reference_and_Meta/Miscellaneous.md#object-turtled) | Object | Defines the 'Turtled' form, a defensive state where the unit cannot attack or move. | 0 | `{ . . . }` |
| [`Default_Ground`](../Reference_and_Meta/Miscellaneous.md#object-default_ground) | Object | Defines the 'Default_Ground' form for SpiderQueen, with AI pattern to web and attack. | 0 | `{ . . . }` |
| [`FireFull`](../Reference_and_Meta/Miscellaneous.md#object-firefull) | Integer / Object | Defines the 'FireFull' form, a fully charged fire state with its own animation and visual combo. | 0 | `{ . . . }`<br>`1` |
| [`NeutronStar`](../Reference_and_Meta/Miscellaneous.md#object-neutronstar) | Object | Defines the neutron star form with custom graphics and a random pattern AI (rumble or explode). | 0 | `{ . . . }` |
| [`OneAlive`](../Reference_and_Meta/Miscellaneous.md#object-onealive) | Object | The form configuration applied when only one family member remains alive. | 0 | `{ . . . }` |
| [`TwoAlive`](../Reference_and_Meta/Miscellaneous.md#object-twoalive) | Object | A form that activates when two specific units are alive, granting the contained passives and abilities. | 0 | `{ . . . }` |
| [`NotPriming`](../Reference_and_Meta/Miscellaneous.md#object-notpriming) | Object | Defines the 'NotPriming' form, which allows the unit to take main turns and grants bonus turns. | 0 | `{ . . . }` |
| [`Priming`](../Reference_and_Meta/Miscellaneous.md#object-priming) | Object | Defines the 'Priming' form, where the unit does not take main turns but gains bonus turns at round end. | 0 | `{ . . . }` |
| [`Dumb`](../Reference_and_Meta/Miscellaneous.md#object-dumb) | Integer / Object | Defines the 'Dumb' form, which can be either a numeric value or an object with passives that disable spells and turn off TV. | 0 | `{ . . . }`<br>`3` |
| [`Insane_Ground`](../Reference_and_Meta/Miscellaneous.md#object-insane_ground) | Object | Defines the insane ground form with pattern AI and animation suffix. | 0 | `{ . . . }` |
| [`MouthFull`](../Reference_and_Meta/Miscellaneous.md#object-mouthfull) | Object | Defines a form with mouth full animation that changes while the Consuming status is active. | 0 | `{ . . . }` |
| [`NormalFull`](../Reference_and_Meta/Miscellaneous.md#object-normalfull) | Integer / Object | As an object, defines the normal full form with a spit attack and conditional form change. As an integer, specifies alt graphics index. | 0 | `{ . . . }`<br>`0` |
| [`Off`](../Reference_and_Meta/Miscellaneous.md#object-off) | Object | Defines an off form with a 'Off' animation suffix. | 0 | `{ . . . }` |
| [`Possessing`](../Reference_and_Meta/Miscellaneous.md#object-possessing) | Object | Form state when the unit is possessing another entity. | 0 | `{ . . . }` |
| [`Standing`](../Reference_and_Meta/Miscellaneous.md#object-standing) | Object | Form state where the unit is standing, with default movement and attack. | 0 | `{ . . . }` |
| [`TarFull`](../Reference_and_Meta/Miscellaneous.md#object-tarfull) | Integer / Object | If an integer, the number of full tar stacks. If an object, the form state for the fully tar-covered unit. | 0 | `{ . . . }`<br>`2` |
| [`Throb`](../Reference_and_Meta/Miscellaneous.md#object-throb) | Object | Form state for the Chaos unit's throb behavior, with a spread pattern. | 0 | `{ . . . }` |
| [`Unlit`](../Reference_and_Meta/Miscellaneous.md#object-unlit) | Object | Form state for an unlit candle, muting demonic glyph display. | 0 | `{ . . . }` |
| [`Unwashed`](../Reference_and_Meta/Miscellaneous.md#object-unwashed) | Object | Form state for the unwashed version of Johnny, with its own AI pattern. | 0 | `{ . . . }` |
| [`AllAlive`](../Reference_and_Meta/Miscellaneous.md#object-allalive) | Object | The form configuration applied when all family members are alive. | 0 | `{ . . . }` |
| [`Alert`](../Reference_and_Meta/Miscellaneous.md#object-alert) | Object | Defines the 'Alert' form, an alerted state with a pattern brain AI. | 0 | `{ . . . }` |
| [`Angry`](../Reference_and_Meta/Miscellaneous.md#object-angry) | Object | Defines the 'Angry' form, an enraged state with its own AI. | 0 | `{ . . . }` |
| [`BellyFull`](../Reference_and_Meta/Miscellaneous.md#object-bellyfull) | Object | Defines the 'BellyFull' form, used when the unit has the Consuming status, with appropriate animation. | 0 | `{ . . . }` |
| [`Charging`](../Reference_and_Meta/Miscellaneous.md#object-charging) | Object | Defines the 'Charging' form, a wind-up state for a powerful attack. | 0 | `{ . . . }` |
| [`Default_Ceiling`](../Reference_and_Meta/Miscellaneous.md#object-default_ceiling) | Object | Defines the 'Default_Ceiling' form for SpiderQueen, with AI pattern to spawn spiders. | 0 | `{ . . . }` |
| [`DualSword_Primed`](../Reference_and_Meta/Miscellaneous.md#object-dualsword_primed) | Object | Defines the 'DualSword_Primed' form, a powered-up dual sword state with holy animation. | 0 | `{ . . . }` |
| [`Grappling`](../Reference_and_Meta/Miscellaneous.md#object-grappling) | Object | Defines a grappling form with a specific animation suffix and exit animations. | 0 | `{ . . . }` |
| [`Grown`](../Reference_and_Meta/Miscellaneous.md#object-grown) | Object | Defines the grown form with a custom attack, name, UI floater offset, and a health weak threshold. | 0 | `{ . . . }` |
| [`Guarding`](../Reference_and_Meta/Miscellaneous.md#object-guarding) | Object | Defines a guarding form with a high brace passive. | 0 | `{ . . . }` |
| [`HasDeadCat`](../Reference_and_Meta/Miscellaneous.md#object-hasdeadcat) | Object | Defines a form when Lenny's cat is dead, with a slap attack and conditional form change while the status is active. | 0 | `{ . . . }` |
| [`Headless`](../Reference_and_Meta/Miscellaneous.md#object-headless) | Object | Defines a headless form with increased movement. | 0 | `{ . . . }` |
| [`Insane_Ceiling`](../Reference_and_Meta/Miscellaneous.md#object-insane_ceiling) | Object | Defines the insane ceiling form with pattern AI and animation suffix. | 0 | `{ . . . }` |
| [`Joystick`](../Reference_and_Meta/Miscellaneous.md#object-joystick) | Object | Defines a form with joystick animation and an immediate ability reaction (fumble even/odd). | 0 | `{ . . . }` |
| [`Lit`](../Reference_and_Meta/Miscellaneous.md#object-lit) | Object | Defines a lit form that changes when wind element influence is applied. | 0 | `{ . . . }` |
| [`Obey`](../Reference_and_Meta/Miscellaneous.md#object-obey) | Integer / Object | As an object, defines an obey form that disables attacks and reacts with TV off. As an integer, defines a value (e.g., weight or count). | 0 | `{ . . . }`<br>`1` |
| [`Open`](../Reference_and_Meta/Miscellaneous.md#object-open) | Object | Defines an open form with increased movement and a specific attack. | 0 | `{ . . . }` |
| [`OpenCat`](../Reference_and_Meta/Miscellaneous.md#object-opencat) | Object | Defines an open cat form that changes when the Consuming status is active. | 0 | `{ . . . }` |
| [`Pulp2`](../Reference_and_Meta/Miscellaneous.md#object-pulp2) | Object | Form state for the second stage of pulping, with no attacks or movement. | 0 | `{ . . . }` |
| [`SmallHolding`](../Reference_and_Meta/Miscellaneous.md#object-smallholding) | Object | Form state when the unit is holding a small object, triggering a form change while consuming. | 0 | `{ . . . }` |
| [`SmallHoldingCat`](../Reference_and_Meta/Miscellaneous.md#object-smallholdingcat) | Object | Form state when the unit is holding a cat, triggering a form change while consuming. | 0 | `{ . . . }` |
| [`SpawningPhase`](../Reference_and_Meta/Miscellaneous.md#object-spawningphase) | Object | Form state for the spawning phase, where the unit is immobile and cannot take turns. | 0 | `{ . . . }` |
| [`Start_Ceiling`](../Reference_and_Meta/Miscellaneous.md#object-start_ceiling) | Object | Form state for starting on the ceiling, with a form change trigger when entering the map. | 0 | `{ . . . }` |
| [`Stop`](../Reference_and_Meta/Miscellaneous.md#object-stop) | Integer / Object | If an integer, the number of turns the unit is stopped. If an object, the form configuration for the stopped state. | 0 | `{ . . . }`<br>`2` |
| [`SwordAndShield`](../Reference_and_Meta/Miscellaneous.md#object-swordandshield) | Object | Form state with sword and shield, using the DestroyerAttack ability. | 0 | `{ . . . }` |
| [`SwordAndShield_Primed`](../Reference_and_Meta/Miscellaneous.md#object-swordandshield_primed) | Object | Primed form state of SwordAndShield with holy animation and no final boss shield. | 0 | `{ . . . }` |
| [`Washer`](../Reference_and_Meta/Miscellaneous.md#object-washer) | Object | Form state for the washer variant of a cultist, with basic melee attack. | 0 | `{ . . . }` |
| [`Attacker`](../Reference_and_Meta/Miscellaneous.md#object-attacker) | Object | Defines the 'Attacker' form, focusing on offensive actions like attacking and charging. | 0 | `{ . . . }` |
| [`Bully`](../Reference_and_Meta/Miscellaneous.md#object-bully) | Object | Defines the 'Bully' form, which allows the unit to take turns and enables its passives. | 0 | `{ . . . }` |
| [`CaveWomanHasCat`](../Reference_and_Meta/Miscellaneous.md#object-cavewomanhascat) | Object | Defines the 'CaveWomanHasCat' form, a variant of CaveWoman that attacks with a cat slap. | 0 | `{ . . . }` |
| [`Close`](../Reference_and_Meta/Miscellaneous.md#object-close) | Object | Defines the 'Close' form, which triggers GSOpen ability upon reaction. | 0 | `{ . . . }` |
| [`Damaged`](../Reference_and_Meta/Miscellaneous.md#object-damaged) | Object | Defines the 'Damaged' form, an injured state with a specific AI pattern to drink and attack. | 0 | `{ . . . }` |
| [`DesireMech`](../Reference_and_Meta/Miscellaneous.md#object-desiremech) | Object | Defines the 'DesireMech' form, a mech suit form with its own AI pattern. | 0 | `{ . . . }` |
| [`Drunker`](../Reference_and_Meta/Miscellaneous.md#object-drunker) | Object | Defines the 'Drunker' form, a drunken state with altered animation. | 0 | `{ . . . }` |
| [`Explody`](../Reference_and_Meta/Miscellaneous.md#object-explody) | Object | Defines the 'Explody' form, an explosive state that uses ToxExplode attack and cannot move. | 0 | `{ . . . }` |
| [`FightPhase`](../Reference_and_Meta/Miscellaneous.md#object-fightphase) | Object | Defines the 'FightPhase' form, a combat form with float move and shoot attack, taking turns. | 0 | `{ . . . }` |
| [`Flop`](../Reference_and_Meta/Miscellaneous.md#object-flop) | Object | Defines the initial flopped down state, using animation suffix 'Down' and a pattern AI that requires 4 wiggles to exit. | 0 | `{ . . . }` |
| [`Flop2`](../Reference_and_Meta/Miscellaneous.md#object-flop2) | Object | Defines a subsequent flopped down state triggered on hit, with variable wiggles (2-6) to recover. | 0 | `{ . . . }` |
| [`FlushBubs`](../Reference_and_Meta/Miscellaneous.md#object-flushbubs) | Object | Defines a form granting an immediate ability reaction for Cerberubs shotgun. | 0 | `{ . . . }` |
| [`FlushHost`](../Reference_and_Meta/Miscellaneous.md#object-flushhost) | Object | Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage. | 0 | `{ . . . }` |
| [`FlushNettle`](../Reference_and_Meta/Miscellaneous.md#object-flushnettle) | Object | Defines a form that gains thorns and kinetic spikes after an enemy casts a spell. | 0 | `{ . . . }` |
| [`GuaranteedJackpot`](../Reference_and_Meta/Miscellaneous.md#object-guaranteedjackpot) | Object | Defines a form that guarantees a jackpot coin result from slot machine rolls. | 0 | `{ . . . }` |
| [`HalfDead`](../Reference_and_Meta/Miscellaneous.md#object-halfdead) | Object | Defines the half-dead form with reduced movement and a dash attack. | 0 | `{ . . . }` |
| [`HasRock`](../Reference_and_Meta/Miscellaneous.md#object-hasrock) | Object | Defines a form where the unit has a rock, with a bash attack. | 0 | `{ . . . }` |
| [`HumanDead`](../Reference_and_Meta/Miscellaneous.md#object-humandead) | Object | Defines a form when the human half is dead, with a spin attack and custom tooltip. | 0 | `{ . . . }` |
| [`JohnnyBubs`](../Reference_and_Meta/Miscellaneous.md#object-johnnybubs) | Object | Defines a form granting an immediate ability reaction for Cerberubs shotgun. | 0 | `{ . . . }` |
| [`JohnnyHost`](../Reference_and_Meta/Miscellaneous.md#object-johnnyhost) | Object | Defines a host form with a partial animation suffix and a reflect projectiles passive that deals 2 self-damage. | 0 | `{ . . . }` |
| [`JohnnyNettle`](../Reference_and_Meta/Miscellaneous.md#object-johnnynettle) | Object | Defines a form that gains thorns and kinetic spikes after an enemy casts a spell. | 0 | `{ . . . }` |
| [`Lifted`](../Reference_and_Meta/Miscellaneous.md#object-lifted) | Object | Defines a lifted form with no attack or movement options. | 0 | `{ . . . }` |
| [`NoEyes`](../Reference_and_Meta/Miscellaneous.md#object-noeyes) | Object | Defines a form with no eyes animation. | 0 | `{ . . . }` |
| [`NoStick`](../Reference_and_Meta/Miscellaneous.md#object-nostick) | Object | Defines a form without a stick, using a jab attack with pattern AI. | 0 | `{ . . . }` |
| [`OneEye`](../Reference_and_Meta/Miscellaneous.md#object-oneeye) | Object | Defines a form with one eye that triggers an ability at 40% health threshold. | 0 | `{ . . . }` |
| [`Out`](../Reference_and_Meta/Miscellaneous.md#object-out) | Object | Defines a form that is 'out' with a ground flopper movement passive. | 0 | `{ . . . }` |
| [`Primed`](../Reference_and_Meta/Miscellaneous.md#object-primed) | Object | Form state representing the unit being primed, with specific attack and AI behavior. | 0 | `{ . . . }` |
| [`Pulp3`](../Reference_and_Meta/Miscellaneous.md#object-pulp3) | Object | Form state for the third stage of pulping, with no attacks or movement. | 0 | `{ . . . }` |
| [`Pulp4`](../Reference_and_Meta/Miscellaneous.md#object-pulp4) | Object | Form state for the fourth stage of pulping, with no attacks or movement. | 0 | `{ . . . }` |
| [`Pulp5`](../Reference_and_Meta/Miscellaneous.md#object-pulp5) | Object | Form state for the fifth stage of pulping, with no attacks or movement. | 0 | `{ . . . }` |
| [`Pulp6`](../Reference_and_Meta/Miscellaneous.md#object-pulp6) | Object | Form state for the sixth stage of pulping, with no attacks or movement. | 0 | `{ . . . }` |
| [`Pulp7`](../Reference_and_Meta/Miscellaneous.md#object-pulp7) | Object | Form state for the seventh stage of pulping, with no attacks or movement. | 0 | `{ . . . }` |
| [`Sitting`](../Reference_and_Meta/Miscellaneous.md#object-sitting) | Object | Form state where the unit is sitting, with no movement or attack. | 0 | `{ . . . }` |
| [`Standing2`](../Reference_and_Meta/Miscellaneous.md#object-standing2) | Object | Form state where the unit is standing with a jumping movement ability. | 0 | `{ . . . }` |
| [`ThrobBubs`](../Reference_and_Meta/Miscellaneous.md#object-throbbubs) | Object | Form state for Chaos unit throb that reacts with a shotgun attack. | 0 | `{ . . . }` |
| [`ThrobHost`](../Reference_and_Meta/Miscellaneous.md#object-throbhost) | Object | Form state for Chaos unit acting as host, reflecting projectiles. | 0 | `{ . . . }` |
| [`ThrobNettle`](../Reference_and_Meta/Miscellaneous.md#object-throbnettle) | Object | Form state for Chaos unit with thorns and kinetic spikes that stack after enemy spells. | 0 | `{ . . . }` |
| [`Transformed`](../Reference_and_Meta/Miscellaneous.md#object-transformed) | Object | Form state after transformation, ending the turn on form switch. | 0 | `{ . . . }` |
| [`Washed`](../Reference_and_Meta/Miscellaneous.md#object-washed) | Object | Form state for the washed version of Johnny, with a blast attack. | 0 | `{ . . . }` |
| [`ZealotBomb`](../Reference_and_Meta/Miscellaneous.md#object-zealotbomb) | Object | Form state for the bomb zealot variant, with an explosion attack. | 0 | `{ . . . }` |
| [`Hint_CrackedVisuals`](../Reference_and_Meta/Miscellaneous.md#object-hint_crackedvisuals) | Object | Defines a visual state with cracked animation suffix. | 0 | `{ . . . }` |
| [`Hint_CrackedVisuals2`](../Reference_and_Meta/Miscellaneous.md#object-hint_crackedvisuals2) | Object | Defines a visual state with charging cracked animation. | 0 | `{ . . . }` |
| [`Hint_CrackedVisuals3`](../Reference_and_Meta/Miscellaneous.md#object-hint_crackedvisuals3) | Object | Defines a visual state with swallowed cracked animation. | 0 | `{ . . . }` |
| [`InitialPhase`](../Reference_and_Meta/Miscellaneous.md#object-initialphase) | Object | Defines the initial phase form with a float move, shoot attack, and the ability to take turns. | 0 | `{ . . . }` |
| [`Mounted`](../Reference_and_Meta/Miscellaneous.md#object-mounted) | Object | Defines a mounted form with 'Cat' animation suffix. | 0 | `{ . . . }` |
| `NoDeathRattle` | Object | Defines a form that suppresses death rattle and triggers a heart attack when a buddy dies. | 0 | `{ . . . }` |
| [`OffScreen`](../Reference_and_Meta/Miscellaneous.md#object-offscreen) | Object | Defines an off-screen form that does not take turns and drops in chaos heads. | 0 | `{ . . . }` |
| [`TwoEyes`](../Reference_and_Meta/Miscellaneous.md#object-twoeyes) | Object | Form state with two eyes, triggering ability at a health threshold. | 0 | `{ . . . }` |
| `Unmounted` | Object | Form state when the unit is unmounted from its mech suit, with no additional properties. | 0 | `{ . . . }` |
| `sync_brain_patterns` | Boolean | If true, synchronizes brain patterns across form changes. | 0 | `true` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `FormChangeOnElementInfluence`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`particle`](../Reference_and_Meta/Enums.md#enum-particle) | Enum  | Specifies the particle effect displayed. | 0 | `ArrowFromAbove`<br>`BigMagicMissileBlast`<br>`Bolt` |
| [`sfx`](../Reference_and_Meta/Enums.md#enum-sfx) | Enum  | Specifies the sound effect to play when the form change triggers. | 0 | `BeaniesEnding_Banging`<br>`FireExtinguish`<br>`Intro_LabDisposal` |
| [`form`](../Reference_and_Meta/Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 0 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 0 | `Electric`<br>`Fire`<br>`Gravity` |
| [`exclude`](../Reference_and_Meta/Enums.md#enum-exclude) | Enum  | Specifies an element or effect that does not trigger the form change. | 0 | `SpellDamageUp`<br>`fire`<br>`water` |


### Object: `FormChangeOffMap`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form_offmap`](../Reference_and_Meta/Enums.md#enum-form_offmap) | Enum   | Specifies the form name to use when the unit is off the map. | 0 | `Default_Ceiling`<br>`Insane_Ceiling`<br>`OffMap` |
| [`form_onmap`](../Reference_and_Meta/Enums.md#enum-form_onmap) | Enum   | Specifies the form name to use when the unit returns to the map. | 0 | `Default`<br>`Default_Ground`<br>`FightPhase` |


### Object: `FormChangeHealthThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 0 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`form_above`](../Reference_and_Meta/Enums.md#enum-form_above) | Enum   | The form to change to when health is above the threshold. | 0 | `Default`<br>`Full`<br>`Standing` |
| [`form_below`](../Reference_and_Meta/Enums.md#enum-form_below) | Enum   | The form to change to when health is below the threshold. | 0 | `Damaged`<br>`DesireMech`<br>`Standing2` |
| `count_shield` | Boolean | If true, shields count towards the health threshold calculation. | 0 | `true` |


### Object: `FormChangeDuringWeatherElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](../Reference_and_Meta/Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 0 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 0 | `Electric`<br>`Fire`<br>`Gravity` |


### Object: `FollowUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Flying`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FlyDamageIncrease`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 0 | `false`<br>`true` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Flammable`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `FinalBossSyncAnimations`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`other_character`](../Reference_and_Meta/Enums.md#enum-other_character) | Enum   | Specifies the name of the other boss character whose animations are synced. | 0 | `MegaGuppy` |
| [`other_form_change_abilities`](../Reference_and_Meta/Miscellaneous.md#object-other_form_change_abilities) | Object | An object mapping form names to the other character's form change abilities. | 0 | `{ . . . }` |


### Object: `FinalBossShieldHealth`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`break_ability`](../Reference_and_Meta/Enums.md#enum-break_ability) | Enum   | Specifies the ability used to break the shield. | 0 | `DestroyerBreakShield` |
| [`state_health`](../Reference_and_Meta/Arrays.md#array-state_health) | Array   | An array of health thresholds defining state transitions. | 0 | `[` |


### Object: `FinalBossPupils`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`radius`](../Reference_and_Meta/Arrays.md#array-radius) | Array / Integer | The range in tiles of the distortion ring effect; an array [min, max] specifies a random radius within that range. | 0 | `0`<br>`1`<br>`13` |
| [`look_at_offset`](../Reference_and_Meta/Arrays.md#array-look_at_offset) | Array   | A 3D vector offset from the head position that the pupils should look at. | 0 | `[0 2.5 0]` |
| `reset_center_because_no_target_halflife` | Float | The half-life for the pupil position to reset to center when no target is available. | 0 | `.1` |
| `reset_center_because_of_animation_halflife` | Float | The half-life for the pupil position to reset to center during an animation. | 0 | `.05` |
| `teleport_tracking_halflife` | Float | The half-life for the pupil tracking to reacquire a target after a teleport. | 0 | `.01` |
| `tracking_acquisition_halflife` | Float | The half-life for the pupil tracking to smoothly acquire a new target. | 0 | `.1` |
| [`virtual_head_position`](../Reference_and_Meta/Arrays.md#array-virtual_head_position) | Array   | A 3D vector representing the virtual position of the head for pupil tracking. | 0 | `[11 2 11]` |


### Object: `FinalBossHitCountdownHoly`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 0 | `800`<br>`802`<br>`804` |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 0 | `801`<br>`803`<br>`805` |


### Object: `FinalBossHitCountdownExplosive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 0 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 0 | `800`<br>`802`<br>`804` |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 0 | `801`<br>`803`<br>`805` |


### Object: `FinalBossHitCountdownBoris`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 0 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `icon` | Integer | The sprite ID or atlas key for the countdown icon when not ready. | 0 | `800`<br>`802`<br>`804` |
| `icon_ready` | Integer | The sprite ID or atlas key for the countdown icon when the ability is ready. | 0 | `801`<br>`803`<br>`805` |


### Object: `FinalBossBecomeTheChild`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`SwitchMusic`](../Reference_and_Meta/Miscellaneous.md#object-switchmusic) | Object | Defines a new song or layer for the background music. | 0 | `{ . . . }` |
| `PlayBackground` | Integer | Specifies the background index to play. | 0 | `0`<br>`1` |
| [`GlobalSpawnCharacter`](../Reference_and_Meta/Enums.md#enum-globalspawncharacter) | Enum | Specifies the name of a character to spawn globally. | 0 | `MegaGuppy` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `FinalBossBeamQueue`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`transform`](../Reference_and_Meta/Enums.md#enum-transform) | Enum  | Specifies the ability queued to transform the boss into its next form. | 0 | `TheChild_TransformBoris` |
| [`release`](../Reference_and_Meta/Enums.md#enum-release) | Enum  | Specifies the ability queued to release the boss's stored beams. | 0 | `TheChild_ReleaseBeams` |
| [`queue`](../Reference_and_Meta/Enums.md#enum-queue) | Enum  | Specifies the ability queued to fire the boss's beam. | 0 | `TheChild_TargetBeam` |


### Object: `FaceLastDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 0 | `true` |


### Object: `FaceAwayLastDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability_damage_only` | Boolean | If true, the reaction only triggers on ability damage, not basic attacks. | 0 | `true` |
| `use_turn_animations` | Boolean | If true, uses turn-based animations for the face change. | 0 | `true` |
| `override_hit_animation` | Boolean | If true, the character's hit animation is overridden by the face-away animation. | 0 | `true` |


### Object: `ExtraBasicMoves_Status`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `ExtraBasicAttacks_Status`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Empath`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `Dyslexia`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `DybbukPossessionFallback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](../Reference_and_Meta/Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 0 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| [`exit_ability`](../Reference_and_Meta/Enums.md#enum-exit_ability) | Enum   | Determines the ability used when the Dybbuk possession ends. | 0 | `DybbukReturn` |


### Object: `DurabilityTransform`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`eq`](../Reference_and_Meta/Arrays.md#array-eq) | Array | An array specifying a [durability, item] pair to transform to when durability equals a specific value. | 0 | `[0 EstusFlask_Empty]`<br>`[0 JarOfNothing]`<br>`[0 WaterBottle_Empty]` |
| [`ge`](../Reference_and_Meta/Arrays.md#array-ge) | Array | An array specifying a [durability, item] pair to transform to when durability is greater than or equal to a specific value. | 0 | `[10 NuclearKnife_Glowing]`<br>`[2 WaterBottle_Full]`<br>`[20 BlackShard_Glowing]` |


### Object: `DukeOfFlies`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Doomed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DodgeWhenTargeted`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |


### Object: `DodgeChance_Status`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DivineShield`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DirtyClaws`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DiesToPiercingAndSpikes`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `deferred` | Boolean | If true, the destruction is deferred until the character is settled. | 0 | `true` |


### Object: `DiesToElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 0 | `Electric`<br>`Fire`<br>`Gravity` |
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 0 | `true` |


### Object: `DiceBehavior`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dice_size` | Integer | The number of sides on the die. | 0 | `6` |
| `knockback_damage` | Integer | The amount of damage dealt by the knockback. | 0 | `5` |


### Object: `DepressionAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 0 | `1`<br>`10`<br>`2` |
| `aura_effects_allies` | Boolean | If false, the aura does not affect allies. | 0 | `false` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `DelayedAutoRevive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `health` | Integer | The maximum hit points of the unit. | 0 | `0`<br>`1`<br>`10` |
| `rounds` | Integer | The number of rounds after which the auto-revive triggers. | 0 | `1`<br>`2` |


### Object: `DejaVu`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DeathRattleRevive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 0 | `true` |


### Object: `DeathChill`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `DamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CyborgTurns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`TakeBonusTurnWithAIControl`](../Reference_and_Meta/Miscellaneous.md#object-takebonusturnwithaicontrol) | Object | An object configuring whether the bonus turn happens at the end of the round and whether spells are included. | 0 | `{ . . . }` |


### Object: `CritChanceUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CreateGlobalModifiers`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`BloodRain`](../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object  | If non-zero, enables the blood rain visual effect. | 0 | `{ . . . }`<br>`1` |
| [`LowerAmbientLight`](../Reference_and_Meta/Miscellaneous.md#object-lowerambientlight) | Object | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 0 | `{ . . . }` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `CounterNextAttacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CounterAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 0 | `.02`<br>`.1`<br>`.15` |
| `ranged_only` | Boolean | If true, the reaction only triggers on ranged attacks. | 0 | `true` |
| `melee_only` | Boolean | If true, the counterattack or block effect only triggers in response to melee attacks. | 0 | `true` |
| `without_orienting` | Boolean | If true, the counter-attack does not rotate the character to face the attacker. | 0 | `true` |


### Object: `ConvertDamageToScaledStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 0 | `1` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Consumed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`mount_mode`](../Reference_and_Meta/Enums.md#enum-mount_mode) | Boolean / Enum | Specifies the mounting mode; values include 'auto' or 'true'. | 0 | `auto`<br>`true` |
| [`drop_on_death`](../Reference_and_Meta/Enums.md#enum-drop_on_death) | Boolean / Enum   | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 0 | `deferred`<br>`false`<br>`true` |


### Object: `ConjureBonusAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 0 | `true` |


### Object: `Confusion`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Conductor`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | `passives`<br>`class`<br>`tag` 


### Object: `CherubimReaction`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Leave`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-leave) | Enum / Object | Specifies the ability used when this unit leaves the field. | 0 | `{ . . . }`<br>`CherubimLeave`<br>`LELeave` |
| [`Return`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#object-return) | Enum / Object | Specifies the ability used when this unit returns to the field. | 0 | `{ . . . }`<br>`CherubimReturn`<br>`LEReturn` |


### Object: `CharmAllFlies`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Charge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CharacterLightSource`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`size`](../Reference_and_Meta/Enums.md#enum-size) | Enum / Float  | The scale factor (size multiplier) of the spawned unit. | 0 | `.2`<br>`.5`<br>`1` |
| [`color`](../Reference_and_Meta/Arrays.md#array-color) | Array  | The RGB color of the light source. | 0 | `[.27 .47 .18]`<br>`[.3, .7, 1]`<br>`[.32 .10 .10]` |
| [`glow`](../Reference_and_Meta/Arrays.md#array-glow) | Array  | The RGBA glow color of the light source. | 0 | `[.3, .7, 1, .5]`<br>`[.7, .3, 1, .5]`<br>`[.7, .8, .9, .5]` |


### Object: `ChaosHeadDropIn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 0 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`new_music`](../Reference_and_Meta/Enums.md#enum-new_music) | Enum   | Specifies the music track to play during the boss's head drop-in animation. | 0 | `chaos_boss_part2` |


### Object: `ChaosBossPieces`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`active_pieces`](../Reference_and_Meta/Arrays.md#array-active_pieces) | Array   | An array of piece names that are considered actively part of the current form. | 0 | `[Johnny Throb Flush]` |
| [`passive_pieces`](../Reference_and_Meta/Arrays.md#array-passive_pieces) | Array   | An array of piece names that are considered passively part of the current form. | 0 | `[Host Nettle Bubs]` |


### Object: `ChaosBossFormChangeGuide`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`active_pieces`](../Reference_and_Meta/Arrays.md#array-active_pieces) | Array   | An array of piece names that are considered actively part of the current form. | 0 | `[Johnny Throb Flush]` |
| [`passive_pieces`](../Reference_and_Meta/Arrays.md#array-passive_pieces) | Array   | An array of piece names that are considered passively part of the current form. | 0 | `[Host Nettle Bubs]` |
| `passives_health_threshold` | Integer | The health percentage threshold at which the boss's passive abilities change. | 0 | `50%` |


### Object: `ChanceToSpitOnDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `backstabs_only` | Boolean | If true, the reaction only triggers on backstab damage. | 0 | `true` |
| `flat_chance` | Integer | The base percentage chance to spit when taking damage. | 0 | `100%`<br>`50%` |
| `chance_per_damage` | Integer | The additional percentage chance to spit per point of damage taken. | 0 | `0%`<br>`2%` |
| `even_on_0_damage_if_knockback` | Boolean | If true, the reaction triggers on zero damage if knockback occurs. | 0 | `true` |


### Object: `ChanceToFormChangeOnAbilityDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 0 | `.02`<br>`.1`<br>`.15` |
| [`form`](../Reference_and_Meta/Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 0 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |


### Object: `ChanceToForceEvent`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 0 | `.02`<br>`.1`<br>`.15` |
| [`event`](../Reference_and_Meta/Enums.md#enum-event) | Enum | Specifies the event to force, either by name or by a nested object defining its type and level. | 0 | `Blessing`<br>`Death`<br>`Tragedy` |


### Object: `ChanceToBlockAndCounter`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 0 | `.02`<br>`.1`<br>`.15` |
| `backstab_only` | Boolean | If true, the block and counter effect only triggers on attacks made from behind the target. | 0 | `true` |


### Object: `ChainKnockback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `CerberubsAggroTargetBehavior`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alert_form`](../Reference_and_Meta/Enums.md#enum-alert_form) | Enum   | Specifies the form to use when the unit is alerted. | 0 | `Alert` |
| [`default_form`](../Reference_and_Meta/Enums.md#enum-default_form) | Enum   | Specifies the default form before aggro. | 0 | `Normal` |


### Object: `CaveFamilyEnrage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 0 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`count`](../Reference_and_Meta/Arrays.md#array-count) | Array / Integer  | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 0 | `0`<br>`1`<br>`10` |


### Object: `CatPartsTransform`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head`](../Reference_and_Meta/Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 0 | `-1`<br>`1`<br>`1.3` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 0 | `-1`<br>`-2`<br>`1` |
| [`palette`](../Reference_and_Meta/Enums.md#enum-palette) | Enum / Integer  | Specifies the color palette index for the ability's visuals. | 0 | `-1`<br>`0`<br>`1` |
| `texture` | Integer | The catalog ID for the cat's texture. | 0 | `-1`<br>`1`<br>`1000` |
| `tail` | Integer | The catalog ID for the cat's tail part. | 0 | `-1`<br>`1000`<br>`1001` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 0 | `-1`<br>`-2`<br>`1` |
| `body` | Float | The catalog ID for the cat's body part. | 0 | `-1`<br>`1`<br>`1.1` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 0 | `-1`<br>`-2`<br>`1` |
| `leg1` | Integer | The catalog ID for the cat's first leg part. | 0 | `-1`<br>`-2`<br>`1` |
| `leg2` | Integer | The catalog ID for the cat's second leg part. | 0 | `-1`<br>`1`<br>`10` |
| `ear1` | Integer | The catalog ID for the cat's first ear part. | 0 | `-2`<br>`1005`<br>`1013` |
| `ear2` | Integer | The catalog ID for the cat's second ear part. | 0 | `1005`<br>`1013`<br>`1036` |
| `eye1` | Integer | The catalog ID for the cat's first eye part. | 0 | `-1`<br>`-2`<br>`1013` |
| `eye2` | Integer | The catalog ID for the cat's second eye part. | 0 | `-1`<br>`1013`<br>`1057` |
| `eyebrow1` | Integer | The catalog ID for the cat's first eyebrow part. | 0 | `-2`<br>`1069` |
| `eyebrow2` | Integer | The catalog ID for the cat's second eyebrow part. | 0 | `1070` |


### Object: `CatPartsSizeScale`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`head`](../Reference_and_Meta/Enums.md#enum-head) | Enum / Float  | The catalog ID for the cat's head part. | 0 | `-1`<br>`1`<br>`1.3` |


### Object: `Burn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BungaEntrance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 0 | `true` |
| `health_threshold` | Integer | The health value at or below which the reaction triggers. -1 disables this check. | 0 | `-1`<br>`150`<br>`50` |
| [`warrior_tag`](../Reference_and_Meta/Enums.md#enum-warrior_tag) | Enum   | Specifies the tag used to identify allied warriors for this ability. | 0 | `bungawarrior`<br>`finalboss_clonecat` |


### Object: `BungaCheers`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`warrior_tag`](../Reference_and_Meta/Enums.md#enum-warrior_tag) | Enum   | Specifies the tag used to identify allied warriors for this ability. | 0 | `bungawarrior`<br>`finalboss_clonecat` |
| [`ally_damage`](../Reference_and_Meta/Enums.md#enum-ally_damage) | Enum   | Specifies the cheer effect when an ally takes damage. | 0 | `littleboo` |
| [`ally_dead`](../Reference_and_Meta/Enums.md#enum-ally_dead) | Enum   | Specifies the cheer effect when an ally dies. | 0 | `bigboo` |
| [`enemy_damage`](../Reference_and_Meta/Enums.md#enum-enemy_damage) | Enum   | Specifies the cheer effect when an enemy takes damage. | 0 | `littlecheer` |
| [`enemy_dead`](../Reference_and_Meta/Enums.md#enum-enemy_dead) | Enum   | Specifies the cheer effect when an enemy dies. | 0 | `bigcheer` |


### Object: `BuffImmunity`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exclude`](../Reference_and_Meta/Enums.md#enum-exclude) | Enum  | Specifies an element or effect that does not trigger the form change. | 0 | `SpellDamageUp`<br>`fire`<br>`water` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Buddy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `allies_only` | Boolean | If true, the effect only applies to allied units. | 0 | `false`<br>`true` |
| [`obj`](../Reference_and_Meta/Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 0 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| `reclaim_if_lost` | Boolean | If true, the buddy can be reclaimed after being lost. | 0 | `true` |


### Object: `Bruise`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BrittleDuringElement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Brittle`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BraceForEachNeighboringEnemy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Brace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BossRewards`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`common`](../Reference_and_Meta/Enums.md#enum-common) | Enum  | Defines the common reward block for a boss encounter. | 0 | `100`<br>`14`<br>`5` |
| [`rare`](../Reference_and_Meta/Enums.md#enum-rare) | Enum  | Defines the rare reward block for a boss encounter. | 0 | `1`<br>`10`<br>`15` |


### Object: `BoostDamageGlobalAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `BoostDamageAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `Blind`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BleedThorns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `Bleed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BlastResistance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BirdRewards`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ally_rewards`](../Reference_and_Meta/Miscellaneous.md#object-ally_rewards) | Object | Defines the rewards granted to the ally when the BirdRewards passive triggers. | 0 | `{ . . . }` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 0 | `{ . . . }` |


### Object: `Bird`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `BattlefieldUniqueRandomPassive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DemonicGlyph_Bite` | Integer | The weight for the demonic glyph of bite, or its configuration. | 0 | `1` |
| `DemonicGlyph_Movement` | Integer | The weight for the demonic glyph of movement, or its configuration. | 0 | `1` |
| `DemonicGlyph_Summon` | Integer | The weight for the demonic glyph of summon, or its configuration. | 0 | `1` |
| `DemonicGlyph_Bounce` | Integer | The weight for the demonic glyph of bounce, or its configuration. | 0 | `1` |
| `DemonicGlyph_Fire` | Integer | The weight for the demonic glyph of fire, or its configuration. | 0 | `1` |


### Object: `BaitAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 0 | `1`<br>`10`<br>`2` |


### Object: `BackflipWhenTargeted`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `ArmorPickup`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`frame_range`](../Reference_and_Meta/Arrays.md#array-frame_range) | Array   | Specifies the minimum and maximum animation frame for the health pickup. | 0 | `[1 2]`<br>`[11 12]`<br>`[13 13]` |


### Object: `ArmorBreakOnHit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance_to_break` | Integer | The percentage chance that the armor breaks on hit. | 0 | `10%`<br>`5%` |
| `durability_loss` | Integer | The amount of durability lost when the armor break effect triggers. | 0 | `0` |


### Object: `Ammo`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `AlphaCat`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `AlphaAllStatsUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `AllyDodgeChanceAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 0 | `.02`<br>`.1`<br>`.15` |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 0 | `1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `AlluringDoodieEater`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](../Reference_and_Meta/Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 0 | `{ . . . }` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 0 | `.02`<br>`.1`<br>`.15` |


### Object: `AllStatsUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |


### Object: `AllStatsAura`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 0 | `1`<br>`10`<br>`2` |
| [`aura_requires_tag`](../Reference_and_Meta/Enums.md#enum-aura_requires_tag) | Enum   | Specifies the tag that units must have to be affected by this aura. | 0 | `humanoid` |


### Object: `AIControlNextTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 0 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 0 | `true` |


### Object: `AggroTargetIsGovernedByHitEffect`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 0 | `false`<br>`true` |


### Object: `AfterImage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 0 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `skilltemp` | Boolean | If true, the afterimage is treated as a skill temporary effect. | 0 | `true` |


### Object: `AddStatusToReceivedDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 0 | `{ . . . }` |
| [`Conditional_IsPhysicalAttack`](./Characters_and_Bosses.md#object-conditional_isphysicalattack) | Object | A conditional block that executes its child actions only if the triggering event is a physical attack. | 0 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` 


### Object: `AddStatusToFirstSpellEachTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 0 | `{ . . . }` |
| [`Conditional_IsSelf`](./Abilities_and_Spells.md#object-conditional_isself) | Object | An object containing effects that are only applied if the target is the source unit itself. | 0 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 0 | `Default`<br>`FormChange`<br>`Druid` 


### Object: `AddStatusToBackstabs`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 0 | `1`<br>`10`<br>`2` |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |


### Object: `AddAdvantageToEvent`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum  | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 0 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`options`](../Reference_and_Meta/Arrays.md#array-options) | Array | An array of named option objects within an event, each defining a possible action the player can take. | 0 | `[smash bash open]` |
| [`add`](../Reference_and_Meta/Arrays.md#array-add) | Array / Integer | The amount or an array of values added to the event's advantage or item tint. | 0 | `5`<br>`[0.05 0.05 0.05]` |


### Object: `AbilityOnRoundEndOnce`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_of_stunned` | Boolean | If true, the ability triggers only on even rounds and when the unit is stunned. | 0 | `true` |


### Object: `AbilityOnRoundEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `force_display_name` | Boolean | If true, forces the display name to show for the ability. | 0 | `true` |


### Object: `AbilityHealthThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 0 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 0 | `false`<br>`true` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 0 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `aux` | Integer | An auxiliary integer value used for item properties, such as hunger value. | 0 | `-1`<br>`1`<br>`10` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 0 | `true` |
| `use_ai` | Boolean | If true, the ability uses AI targeting logic when triggered at the threshold. | 0 | `true` |
| `also_use_if_buddy_is_dead` | Boolean | If true, the ability is also triggered when the unit's buddy is dead. | 0 | `true` |
| `threshold_min` | Enum | The minimum health threshold formula (e.g., X) for the ability to trigger. | 0 | `X` |

