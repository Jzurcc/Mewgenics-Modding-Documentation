---
title: "Cat Mutations Schema"
description: "Defines body part variations and their impacts."
---

# Cat Mutations Schema

## Overview
> [!NOTE]
> This schema handles visual body mutations (like two tails or a cyclops eye) and the corresponding stat changes they apply to the cat.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
body {
    300 { //Rock Bod
        con 1
    }

    301 { //Cactus Bod
        desc "MUTATION_BODY_301_DESC"
        passives {
            Thorns 1
        }
    }

    302 { //Turtle Bod
        tag animal
        spd -1
        shield 5
    }

    303 { //Snail Bod
        tag animal
        shield 10
        spd -2
    }

    304 { //Robot Body
        spd 1
        int 1
    }

    305 { //Conjoined Bod
        lck 1
    }

    306 { //Skin & Bones
        shield 12
        con -3
    }

    307 { //Udders
        tag animal
        cha 1
    }

    308 { //Beach Bod
        str 1
        con 1
        int -1
    }

    309 { //Maggot Bod
        desc "MUTATION_BODY_309_DESC"

        passives {
            MeleeRevengeDamage {
                type status
                damage 0
                knockback 2
            }
        }
    }

    310 { //Puffball Bod
        cha 1
    }

    311 { //Square Bod
        con 1
    }
    
    312 { //Money Bag Bod
        desc "MUTATION_BODY_312_DESC"
        passives {
            SpawnThingOnDamage {
                object Coin
                chance 100%
            }
        }
    }

    313 { //Spike Bod
        desc "MUTATION_BODY_313_DESC"
        passives {
            KineticSpikes 1
        }
    }

    314 { //Porcupine
        desc "MUTATION_BODY_314_DESC"
        cha -1
        passives {   
            Thorns 2 
        }
    }

    315 { //Carapace
        desc "MUTATION_BODY_315_DESC"
        passives {
            Brace 1
        }
    }
    
    316 { //Pangolin
        shield 2
    }

    317 { //Camel Hump
        desc "MUTATION_BODY_317_DESC"
        con 1
        passives {
		    DrinkWater 1
        }
    }

    318 { //Egg Sack Back
         desc "MUTATION_BODY_318_DESC" 

        passives { 
            SpawnEachTurn {
                object CharmedFly
                chance 25% 
            } 
        }
    }

    319 { //Fractured Bod
        desc "MUTATION_BODY_319_DESC"
        
        passives {
            StatusOnTookDamageFromAbility {
                RandomStatusFromPool { 
                    Charge 1
                    Thorns 1
                    KineticSpikes 1
                    DiminishingHealthRegen 1
                    RandomStatUp 1
                    Shield 1
                }
            }
        } 
    }

    320 { //Brick Bod
        shield 1
    }
     
    321 { //Kitten Bod
        desc "MUTATION_BODY_321_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }

    322 { //Backpack
        desc "MUTATION_BODY_322_DESC"
        passives {
            StatusOnBattleEnd {
                FindItemFromPool consumables
            }
        }
    }

    323 { //Fatty
        desc "MUTATION_BODY_323_DESC"
        spd -3
        passives {
            MoveWhenDamaged {
                move_ability MoveOne
                weights chaotic
            }
            Trample 3
        }
    }

    324 { //Eyeball
        desc "MUTATION_BODY_324_DESC"
        passives {
            StatusOnKill {
                RangeUp 1
            }
        }
    }
	
    750 { //spike body
        desc "MUTATION_BODY_750_DESC" 
        passives {        
            Thorns 1 
        } 
    }
	
    753 { //mermaid body
		shield 5
    }
	
    758 { //human head body
		desc "MUTATION_BODY_758_DESC" 
		con 1
		passives {
			Quivered 1
		}
    }

    900 { //slender
        con -2
        spd 1
    }


    //simple stat mod parts
    400 {
        tag common
        str 2
        con -1
    }
    401 {
        tag common
        str 2
        dex -1
    }
    402 {
        tag common
        str 2
        cha -1
    }
    403 {
        tag common
        str 2
        int -1
    }
    404 {
        tag common
        str 2
        spd -1
    }
    405 {
        tag common
        str 2
        lck -1
    }
    406 {
        tag common
        con 2
        str -1
    }
    407 {
        tag common
        con 2
        dex -1
    }
    408 {
        tag common
        con 2
        cha -1
    }
    409 {
        tag common
        con 2
        int -1
    }
    410 {
        tag common
        con 2
        spd -1
    }
    411 {
        tag common
        con 2
        lck -1
    }
    412 {
        tag common
        dex 2
        con -1
    }
    413 {
        tag common
        dex 2
        str -1
    }
    414 {
        tag common
        dex 2
        cha -1
    }
    415 {
        tag common
        dex 2
        int -1
    }
    416 {
        tag common
        dex 2
        spd -1
    }
    417 {
        tag common
        dex 2
        lck -1
    }
    418 {
        tag common
        int 2
        con -1
    }
    419 {
        tag common
        int 2
        dex -1
    }
    420 {
        tag common
        int 2
        cha -1
    }
    421 {
        tag common
        int 2
        str -1
    }
    422 {
        tag common
        int 2
        spd -1
    }
    423 {
        tag common
        int 2
        lck -1
    }
    424 {
        tag common
        cha 2
        con -1
    }
    425 {
        tag common
        cha 2
        dex -1
    }
    426 {
        tag common
        cha 2
        str -1
    }
    427 {
        tag common
        cha 2
        int -1
    }
    428 {
        tag common
        cha 2
        spd -1
    }
    429 {
        tag common
        cha 2
        lck -1
    }
    430 {
        tag common
        lck 2
        con -1
    }
    431 {
        tag common
        lck 2
        dex -1
    }
    432 {
        tag common
        lck 2
        cha -1
    }
    433 {
        tag common
        lck 2
        int -1
    }
    434 {
        tag common
        lck 2
        spd -1
    }
    435 {
        tag common
        lck 2
        str -1
    }
    436 {
        tag common
        spd 2
        con -1
    }
    437 {
        tag common
        spd 2
        str -1
    }
    438 {
        tag common
        spd 2
        cha -1
    }
    439 {
        tag common
        spd 2
        int -1
    }
    440 {
        tag common
        spd 2
        dex -1
    }
    441 {
        tag common
        spd 2
        lck -1
    }

    442 {
        tag melted
        cha -1
    }

    //birth defects
    700 { //Gastroschisis
        tag birth_defect
        con -2
    }
    701 { //Deformed Ribcage
        tag birth_defect
        spd -2
    }
    702 { //Malnurished
        tag birth_defect
        con -1
    }    
	703 { //Body Welts
        desc "MUTATION_BODY_703_DESC"
        tag birth_defect

        passives {
            Bruise 1
        }
    }
	704 { //Conjoined Body
        tag birth_defect
        spd -3
		con 2
    }
	
}
```

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Mutations.md`](../../Directory/Cats_and_Classes/Mutations.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Cat Mutations

> **Associated Files:** `data/mutations/`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

> **Total Count:** 489

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1571 | passives<br>class<br>tag |
| [`desc`](../Reference_and_Meta/Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 4710 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`shield`](../Reference_and_Meta/Enums.md#enum-shield) | Enum / Integer  | The shield value granted by this mutation, or 'aux' to use the unit's auxiliary stat. | 291 | `"max((aux-1)*2, 0)"`<br>`1`<br>`10` |
| [`cha`](../Reference_and_Meta/Enums.md#enum-cha) | Enum / Integer  | The Charisma stat value or modifier. | 337 | `+1`<br>`-1`<br>`-2` |
| [`con`](../Reference_and_Meta/Enums.md#enum-con) | Enum / Integer  | The Constitution stat value or modifier. | 361 | `-1`<br>`-2`<br>`-3` |
| [`spd`](../Reference_and_Meta/Enums.md#enum-spd) | Enum / Integer  | The Speed stat value or modifier. | 332 | `-1`<br>`-10`<br>`-2` |
| [`int`](../Reference_and_Meta/Enums.md#enum-int) | Enum / Integer  | The Intelligence stat value or modifier. | 355 | `-1`<br>`-10`<br>`-2` |
| [`lck`](../Reference_and_Meta/Enums.md#enum-lck) | Enum / Integer  | The Luck stat value or modifier. | 283 | `-1`<br>`-2`<br>`-3` |
| [`str`](../Reference_and_Meta/Enums.md#enum-str) | Enum / Integer  | The Strength stat value or modifier. | 335 | `-1`<br>`-2`<br>`-3` |
| [`dex`](../Reference_and_Meta/Enums.md#enum-dex) | Enum / Integer  | The Dexterity stat value or modifier. | 250 | `-1`<br>`-2`<br>`-3` |
| `divine_shield` | Integer | The number of stacks of the Divine Shield status this mutation provides. | 35 | `0`<br>`1`<br>`2` |
| [`speed`](../Reference_and_Meta/Arrays.md#array-speed) | Array / Float  | The speed of the projectile or move, can be a value or a range. | 475 | `-30`<br>`-4`<br>`.5` |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 990 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`attack`](../Reference_and_Meta/Enums.md#enum-attack) | Enum | Specifies the primary attack ability for the class, either as a string name or a detailed object. | 883 | `AZ_BreakNeck`<br>`AcidShot`<br>`AmoebaAttach` |

</details>


---


### Object: `passives`


**Definition:** A container object listing passive effects granted to the unit.  
**Total Count:** 2807

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`PassiveWhenAffectedByElement`](./Cat_Mutations.md#object-passivewhenaffectedbyelement), [`PassiveWhileHasStatus`](./Cat_Mutations.md#object-passivewhilehasstatus), [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 2628 | passives<br>class<br>tag |
| [`AddStatusToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 248 | `{ . . . }` |
| `Brace` | Array / Integer | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 169 | `1`<br>`10`<br>`2` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 127 | `1`<br>`3`<br>`4` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 130 | `1`<br>`2`<br>`3` |
| [`MeleeRevengeDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 73 | `{ . . . }` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |
| [`StatusEachTurnEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnend) | Object  | Specifies status effects applied to the unit at the end of each of its turns. | 57 | `{ . . . }` |
| [`StatusOnBattleEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 53 | `{ . . . }` |
| [`ElementImmune`](../Reference_and_Meta/Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 51 | `Creep`<br>`Electric`<br>`Fire` |
| [`CounterAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-counterattack) | Object  | Specifies the ability used when the unit counterattacks after being hit. | 39 | `{ . . . }` |
| [`StatusImmunity`](../Reference_and_Meta/Arrays.md#array-statusimmunity) | Array  | A list of status effect names the unit is immune to. | 38 | `Burn`<br>`Poison`<br>`Tarred` |
| [`StatusOnKill`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 40 | `{ . . . }` |
| [`StatusOnTookDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontookdamage) | Object  | Specifies status effects or actions triggered when the unit takes damage. | 46 | `{ . . . }` |
| [`SpawnThingOnDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnthingondamage) | Object  | Specifies an object that spawns on the tile when the unit takes damage. | 38 | `{ . . . }` |
| [`AbilityReaction`](../Reference_and_Meta/Enums.md#enum-abilityreaction) | Enum  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 25 | `AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 25 | `-1`<br>`-2`<br>`1` |
| [`StatusEachTurnBegin`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 27 | `{ . . . }` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 50 | `1`<br>`10`<br>`100` |
| `AddBonusRange` | Integer | The number of additional tiles of range added to the unit's abilities. | 32 | `1`<br>`10`<br>`2` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 41 | `1`<br>`2`<br>`3` |
| [`RevengeDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 31 | `{ . . . }` |
| [`SpawnEachTurn`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawneachturn) | Object  | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 22 | `{ . . . }` |
| `AddCorpseHealth` | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 20 | `-999`<br>`-999999`<br>`100` |
| [`AllStatsUp`](../Reference_and_Meta/Arrays.md#array-allstatsup) | Array / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 125 | `-1`<br>`-2`<br>`1` |
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 35 | `10%`<br>`15%`<br>`2%` |
| `WaterWalk` | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 21 | `1` |
| `AddManaRegen` | Integer | The flat amount of mana regenerated per turn. | 16 | `1`<br>`2`<br>`3` |
| [`MulticlassLevelUp`](../Reference_and_Meta/Enums.md#enum-multiclasslevelup) | Enum  | Specifies the class that this unit gains a level in when multiclassing. | 28 | `Butcher`<br>`Druid`<br>`Fighter` |
| `ReflectProjectiles` | Integer | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 15 | `1`<br>`10%`<br>`100%` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 23 | `1`<br>`2`<br>`3` |
| `ExtraBasicAttacks` | Integer | The number of additional basic attacks the unit can perform per turn. | 15 | `1`<br>`2` |
| [`MoveWhenDamaged`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-movewhendamaged) | Object  | Defines movement behavior when the unit takes damage, such as weights and move ability. | 12 | `{ . . . }` |
| [`ReplaceBasicMove`](../Reference_and_Meta/Enums.md#enum-replacebasicmove) | Enum  | Specifies an alternative movement ability that replaces the unit's default move. | 17 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |
| `AddLevelUpRerolls` | Integer | The number of additional rerolls the unit gets when leveling up. | 14 | `1`<br>`2`<br>`3` |
| `BackstabImmunity` | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 12 | `1` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `1`<br>`2`<br>`3` |
| `DepressionAura` | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 11 | `1`<br>`2` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `10`<br>`15`<br>`20` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 15 | `1`<br>`2`<br>`3` |
| [`StatusOnDie`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusondie) | Object  | Specifies status effects or actions triggered when the unit dies. | 9 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 8 | `Default`<br>`FormChange`<br>`Druid` | `AddElementsToBasicAttack` | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 174 | Default<br>FormChange<br>Druid |
| `AddInitiative` | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 10 | `-10`<br>`-100`<br>`-20` |
| `AlphaTurns` | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 13 | `-1`<br>`1` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| `ManaCostReduction` | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 13 | `-2`<br>`1`<br>`2` |
| [`StatusOnEndMove`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 10 | `{ . . . }` |
| [`AddDamageToElementDamage`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 9 | `{ . . . }` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 26 | `1`<br>`10`<br>`100` |
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 15 | `1` |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`Quivered`](../Reference_and_Meta/Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 36 | `1`<br>`2`<br>`5` |
| [`SpawnOnBattleStartRandomEmptyTile`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile) | Object  | Specifies an object that spawns on a random empty tile at the start of battle. | 11 | `{ . . . }` |
| [`StatusOnTookDamageFromAbility`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusontookdamagefromability) | Object  | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 9 | `{ . . . }` |
| `YOffset` | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 11 | `-.18`<br>`.25`<br>`.35` |
| `AddBonusMeleeRange` | Integer | The number of additional tiles of range added to the unit's melee attacks. | 11 | `1`<br>`10`<br>`2` |
| [`ClassManaCostReduction`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-classmanacostreduction) | Object  | Defines a reduction in mana cost for abilities of a specific class. | 7 | `{ . . . }` |
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 11 | `1` |
| [`StatusIfUnusedMovePoints`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusifunusedmovepoints) | Object  | Specifies status effects applied if the unit ends its turn with unused movement points. | 8 | `{ . . . }` |
| `AddKnockbackDamage` | Integer | The amount of additional knockback damage applied. | 8 | `1`<br>`2`<br>`3` |
| [`AddTemporaryEffectsToBasicAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 7 | `{ . . . }` |
| `BoostWeaponDamage` | Integer | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 9 | `1`<br>`2`<br>`5` |
| [`ChanceToBackflip`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 6 | `{ . . . }` |
| [`EquipTemporaryItem`](../Reference_and_Meta/Enums.md#enum-equiptemporaryitem) | Enum  | Specifies which temporary item is equipped. | 12 | `Bottles`<br>`ButcherHook_Temporary`<br>`FoodBig` |
| [`PassiveWhenAffectedByElement`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 18 | `{ . . . }` |
| [`StatusEveryXSpellCasts`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseveryxspellcasts) | Object  | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 8 | `{ . . . }` |
| [`StatusOnAllyCatDeath`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusonallycatdeath) | Object  | An object listing status effects applied to the unit when an allied cat dies. | 6 | `{ . . . }` |
| [`StatusOnCastSpell`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoncastspell) | Object  | An object listing status effects applied to the unit whenever it casts a spell. | 8 | `{ . . . }` |
| [`AbilityWhenTaggedCharacterMovesNear`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear) | Object  | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 5 | `{ . . . }` |
| [`AddStatusToBasicMeleeAttack`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-addstatustobasicmeleeattack) | Object  | An object listing status effects applied by the unit's basic melee attack. | 11 | `{ . . . }` |
| [`Confusion`](../Reference_and_Meta/Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `1`<br>`10`<br>`2` |
| [`SpawnExtraThingsOnBattleStart`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-spawnextrathingsonbattlestart) | Object  | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 32 | `{ . . . }` |
| [`StatusOnEatFood`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statusoneatfood) | Object  | An object listing status effects applied to the unit when it eats food. | 5 | `{ . . . }` |
| `CanRemoveCursedItems` | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 3 | `1` |
| [`FreePathfindElement`](../Reference_and_Meta/Enums.md#enum-freepathfindelement) | Enum  | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 8 | `Grass`<br>`Water` |
| [`MoveAwayFromDamageSource`](../Reference_and_Meta/Enums.md#enum-moveawayfromdamagesource) | Enum  | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 3 | `BasicJump`<br>`MoveOne` |
| [`PassiveWhenAtFullMana`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passivewhenatfullmana) | Object  | An object listing passive effects that are active only while the unit's mana is full. | 5 | `{ . . . }` |
| [`PassiveWhileHasStatus`](../Reference_and_Meta/Miscellaneous.md#object-passivewhilehasstatus) | Object  | An object containing `status` and `passives` that grants the listed passives while the unit has the specified status. | 6 | `{ . . . }` |
| [`PoopWhenHit`](../Reference_and_Meta/Enums.md#enum-poopwhenhit) | Enum  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 4 | `Poop` |
| [`StatusKilledCharacters`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuskilledcharacters) | Object  | An object listing status effects applied to the unit when it kills a character. | 5 | `{ . . . }` |
| [`BackflipWhenTargeted`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-backflipwhentargeted) | Object  | The number of backflip charges, or an object defining its ability. | 15 | `{ . . . }` |
| `BasicAttackCantMiss` | Integer | If nonzero, the unit's basic attack cannot miss. | 2 | `1` |
| [`BlacklistPickupType`](../Reference_and_Meta/Enums.md#enum-blacklistpickuptype) | Enum  | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 5 | `catnip`<br>`food` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 43 | `-1`<br>`1`<br>`2` |
| [`ConjureBonusAbility`](../Reference_and_Meta/Enums.md#enum-conjurebonusability) | Enum  | Specifies the name of the bonus ability to conjure. | 8 | `Class`<br>`Colorless`<br>`Mage` |
| [`DisableAbilitiesWithTag`](../Reference_and_Meta/Enums.md#enum-disableabilitieswithtag) | Enum  | Specifies a tag that disables any ability with that tag on the unit. | 5 | `consumable`<br>`meat`<br>`musical` |
| `HouseFoodRequirementMultiplier` | Integer | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 3 | `0` |
| `MakeBasicAttackPull` | Integer | If nonzero, the unit's basic attack pulls the target closer. | 2 | `1` |
| `ShowHiddenThings` | Integer | If nonzero, reveals hidden objects or tiles on the map. | 4 | `1` |
| [`Slow`](../Reference_and_Meta/Arrays.md#array-slow) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 75 | `-1`<br>`1`<br>`2` |
| [`SpawnOnDowned`](../Reference_and_Meta/Enums.md#enum-spawnondowned) | Enum  | Specifies the character or object spawned when the unit is downed. | 8 | `CharmedFly`<br>`CharmedKitten`<br>`CharmedSpookie` |
| [`StatusEachRoundEnd`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-statuseachroundend) | Object  | An object listing status effects applied to the unit at the end of each round. | 3 | `{ . . . }` |
| `Vegan` | Integer | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 8 | `1` |

</details>


---


### Object: `AddStatusToBasicAttack`


**Definition:** Contains status effects to add to the basic attack.  
**Total Count:** 248

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root), [`passives`](./Cat_Mutations.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 121 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 56 | `Default`<br>`FormChange`<br>`Druid` | `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 45 | Default<br>FormChange<br>Druid |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 33 | `1`<br>`10`<br>`2` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| `Bruise` | Integer | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 133 | `1`<br>`2`<br>`3` |
| [`ChangeTile`](../Reference_and_Meta/Enums.md#enum-changetile) | Enum  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). | 74 | `BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Slow`](../Reference_and_Meta/Arrays.md#array-slow) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 75 | `-1`<br>`1`<br>`2` |
| [`Stun`](../Reference_and_Meta/Arrays.md#array-stun) | Array  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 138 | `1`<br>`2`<br>`3` |
| [`Confusion`](../Reference_and_Meta/Arrays.md#array-confusion) | Array / Integer  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 86 | `1`<br>`10`<br>`2` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array  | The amount of freeze stacks applied, or an [stacks, probability] array. | 51 | `1`<br>`2`<br>`[1 .01]` |
| `Leeches` | Integer | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 25 | `1`<br>`2`<br>`3` |
| `SoulLink` | Integer | The number of soul link stacks applied. | 15 | `1` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 47 | `1`<br>`2`<br>`3` |
| [`VisualFXTile`](../Reference_and_Meta/Enums.md#enum-visualfxtile) | Enum  | Specifies the name of the visual effect to play on the target tile. | 39 | `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| `FaceAway` | Integer | If set, forces the target to face away from the source. | 18 | `1` |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 9 | `1`<br>`10`<br>`2` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 47 | `0`<br>`1`<br>`10%` |
| [`Instakill`](../Reference_and_Meta/Arrays.md#array-instakill) | Array  | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 12 | `25`<br>`50`<br>`999` |
| [`Petrify`](../Reference_and_Meta/Arrays.md#array-petrify) | Array  | The amount of petrify stacks applied, or an [stacks, probability] array. | 35 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`RandomStatusFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 35 | `{ . . . }` |
| `VaporizeInanimate` | Integer | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 8 | `1` |
| [`Webbed`](../Reference_and_Meta/Arrays.md#array-webbed) | Array  | The amount of webbed stacks applied, or an [stacks, probability] array. | 19 | `1`<br>`2`<br>`[1 .1]` |

</details>


---


### Object: `PassiveWhenAffectedByElement`


**Definition:** An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element.  
**Total Count:** 18

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root), [`passives`](./Cat_Mutations.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 80 | `Electric`<br>`Fire`<br>`Gravity` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 30 | passives<br>class<br>tag |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2807 | `{ . . . }` |

</details>


---


### Object: `effects`


**Definition:** Applies a list of status effects or visual effects to targets.  
**Total Count:** 2166

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`MeleeRevengeDamage`](./Cat_Mutations.md#object-meleerevengedamage), [`RevengeDamage`](./Cat_Mutations.md#object-revengedamage)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1085 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 750 | `Default`<br>`FormChange`<br>`Druid` | `Confusion` | Array / Integer | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 624 | Default<br>FormChange<br>Druid |
| [`Fear`](../Reference_and_Meta/Arrays.md#array-fear) | Array  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 108 | `1`<br>`10`<br>`2` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 43 | `-1`<br>`1`<br>`2` |
| [`Charmed`](../Reference_and_Meta/Arrays.md#array-charmed) | Array  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 47 | `1`<br>`2`<br>`3` |
| [`Petrify`](../Reference_and_Meta/Arrays.md#array-petrify) | Array  | The amount of petrify stacks applied, or an [stacks, probability] array. | 35 | `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`RandomStatusFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 35 | `{ . . . }` |

</details>


---


### Object: `RevengeDamage`


**Definition:** An object defining the damage and effects that trigger when the unit is attacked.  
**Total Count:** 31

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 10 | `damage_instance`<br>`spell`<br>`false` |
| [`effects`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 2166 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 29 | `Default`<br>`FormChange`<br>`Druid` | [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 3 | Default<br>FormChange<br>Druid |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 836 | `[attack move spell]`<br>`attack`<br>`battle` |

</details>

---`damage_instance`<br>`spell`<br>`self_damage`


### Object: `MeleeRevengeDamage`


**Definition:** Defines the damage and effects applied back to a melee attacker upon being hit.  
**Total Count:** 73

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Damaging Keys}`](../Engine_Scripts_and_Logic/Engine_DamagingKeys.md#valid-property-keys) | Variable | Parent object containing damage-related subkeys for revenge or retaliatory effects. | 36 | `damage_instance`<br>`spell`<br>`false` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 49 | `Default`<br>`FormChange`<br>`Druid` | [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 6 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 46 | passives<br>class<br>tag |
| [`knockback`](../Reference_and_Meta/Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 314 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](../Reference_and_Meta/Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 836 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`Freeze`](../Reference_and_Meta/Arrays.md#array-freeze) | Array  | The amount of freeze stacks applied, or an [stacks, probability] array. | 51 | `1`<br>`2`<br>`[1 .01]` |
| [`Immobile`](../Reference_and_Meta/Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 47 | `0`<br>`1`<br>`10%` |`damage_instance`<br>`spell`<br>`self_damage`

</details>


---


### Object: `SpawnThingOnDamage`


**Definition:** Specifies an object that spawns on the tile when the unit takes damage.  
**Total Count:** 38

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1014 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 101 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `AddStatusToBasicMeleeAttack`


**Definition:** An object listing status effects applied by the unit's basic melee attack.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| `Knockback` | Equation | The number of tiles the target is pushed away from the source on hit. | 33 | `1`<br>`10`<br>`2` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 0 | Default<br>FormChange<br>Druid |
| [`KnockUpAndAway`](../Reference_and_Meta/Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. | 25 | `{ . . . }` |

</details>


---


### Object: `StatusOnTookDamage`


**Definition:** Specifies status effects or actions triggered when the unit takes damage.  
**Total Count:** 46

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 30 | passives<br>class<br>tag |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| [`ChangeTilesUnder`](../Reference_and_Meta/Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 9 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| `LuckUp` | Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 51 | `-1`<br>`-2`<br>`-4` |

</details>


---


### Object: `StatusEachTurnBegin`


**Definition:** Specifies status effects applied to the unit at the start of each of its turns.  
**Total Count:** 27

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 9 | passives<br>class<br>tag |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 3 | `Default`<br>`FormChange`<br>`Druid` | `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | Default<br>FormChange<br>Druid |
| `SpeedUp` | Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 91 | `-1`<br>`-2`<br>`-4` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `10`<br>`15`<br>`20` |
| [`MoveQuivered`](../Reference_and_Meta/Arrays.md#array-movequivered) | Array  | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 22 | `1`<br>`2`<br>`[1, 0.1]` |

</details>


---


### Object: `RandomStatusFromPool`


**Definition:** A collection of status effects; one is randomly chosen and applied to the target.  
**Total Count:** 35

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicAttack`](./Cat_Mutations.md#object-addstatustobasicattack), [`StatusOnTookDamageFromAbility`](./Cat_Mutations.md#object-statusontookdamagefromability), [`effects`](./Cat_Mutations.md#object-effects)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 31 | passives<br>class<br>tag |
| `Shield` | Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 12 | `Default`<br>`FormChange`<br>`Druid` | `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 24 | Default<br>FormChange<br>Druid |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 41 | `1`<br>`2`<br>`3` |
| `Poison` | Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 203 | `1`<br>`10`<br>`2` |
| [`Bleed`](../Reference_and_Meta/Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 171 | `1`<br>`10`<br>`2` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| `Weakness` | Integer | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 59 | `1`<br>`2`<br>`3` |
| [`Blind`](../Reference_and_Meta/Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 43 | `-1`<br>`1`<br>`2` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 12 | `1`<br>`2`<br>`3` |
| `Burn` | Equation | The amount of Burn applied, either as a fixed number or a formula string. | 154 | `1`<br>`10`<br>`2` |
| `RandomStatUp` | Equation | The amount of random stat increase applied, either as a fixed number or a formula string. | 52 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |

</details>


---


### Object: `SpawnEachTurn`


**Definition:** Specifies an object that spawns on a random adjacent tile each turn, with optional chance.  
**Total Count:** 22

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1014 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 101 | `.02`<br>`.1`<br>`.15` |
| `good` | Boolean | If true, indicates the positive outcome branch for events or spawning contexts. | 572 | `false`<br>`true` |

</details>


---


### Object: `StatusEachTurnEnd`


**Definition:** Specifies status effects applied to the unit at the end of each of its turns.  
**Total Count:** 57

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root), [`passives`](./Cat_Mutations.md#object-passives)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 42 | passives<br>class<br>tag |
| `Shield` | Equation | The amount of shield granted to the source, absorbing incoming damage. | 109 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 5 | `Default`<br>`FormChange`<br>`Druid` | `RandomStatUp` | Integer | The amount of random stat increase applied, either as a fixed number or a formula string. | 7 | Default<br>FormChange<br>Druid |
| `IntelligenceUp` | Array / Equation | The amount of Intelligence added as a flat bonus. | 45 | `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| `RandomStatDown` | Equation | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 12 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |

</details>


---


### Object: `SpawnOnBattleStartRandomEmptyTile`


**Definition:** Specifies an object that spawns on a random empty tile at the start of battle.  
**Total Count:** 11

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1014 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 75 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `Conditional_RandomChance`


**Definition:** An object containing effects that execute only if a random roll succeeds, with an odds value defined inside.  
**Total Count:** 4

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusKilledCharacters`](./Cat_Mutations.md#object-statuskilledcharacters)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 0 | passives<br>class<br>tag |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 50 | `.1`<br>`.16666666`<br>`.3` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 4 | `Default`<br>`FormChange`<br>`Druid` | `AutoReanimate` | Integer | The percentage chance for the unit to automatically reanimate upon death. | 4 | Default<br>FormChange<br>Druid |

</details>


---


### Object: `StatusEveryXSpellCasts`


**Definition:** An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 234 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 9 | passives<br>class<br>tag |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |
| `RandomMagicMissile` | Integer | The number of random magic missiles fired, or an object defining its properties. | 41 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusKilledCharacters`


**Definition:** An object listing status effects applied to the unit when it kills a character.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnBattleEnd`


**Definition:** An object containing status effects or passives applied to the unit when the battle ends.  
**Total Count:** 53

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 56 | passives<br>class<br>tag |
| [`FindItemFromPool`](../Reference_and_Meta/Enums.md#enum-finditemfrompool) | Enum  | Specifies the loot pool from which to find an item, with an optional chance. | 43 | `blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 6 | `-1`<br>`1`<br>`2` |

</details>


---


### Object: `StatusOnEndMove`


**Definition:** Specifies status effects or actions triggered when the unit finishes moving.  
**Total Count:** 10

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |

</details>


---


### Object: `StatusOnTookDamageFromAbility`


**Definition:** Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental).  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 6 | passives<br>class<br>tag |
| [`RandomStatusFromPool`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 35 | `{ . . . }` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `AbilityWhenTaggedCharacterMovesNear`


**Definition:** An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 589 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`range`](../Reference_and_Meta/Enums.md#enum-range) | Enum / Integer  | The distance in tiles for the trigger effect; `global` means any distance. | 28 | `1`<br>`10`<br>`2` |
| [`tag`](../Reference_and_Meta/Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 990 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |

</details>


---


### Object: `AddDamageToElementDamage`


**Definition:** Defines additional damage of a specific element added to the unit's attacks.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage`](../Reference_and_Meta/Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 1684 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`element`](../Reference_and_Meta/Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 80 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


### Object: `AddTemporaryEffectsToBasicAttack`


**Definition:** A container object that lists temporary status effects applied to the unit's basic attack.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Fury` | Integer | The amount of Fury (bonus damage or charges) gained. | 12 | `10`<br>`55`<br>`75` |

</details>


---


### Object: `BackflipWhenTargeted`


**Definition:** The number of backflip charges, or an object defining its ability.  
**Total Count:** 15

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 589 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 234 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `ChanceToBackflip`


**Definition:** An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 589 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 101 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `ClassManaCostReduction`


**Definition:** Defines a reduction in mana cost for abilities of a specific class.  
**Total Count:** 7

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reduction` | Integer | The amount or percentage by which mana cost is reduced. | 18 | `1`<br>`2`<br>`3` |
| [`class`](../Reference_and_Meta/Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1484 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |

</details>


---


### Object: `Conditional_FirstApplicationThisTurn`


**Definition:** Container for effects applied only on the first application of this ability during the turn.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#object-statusonendmove)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 5 | Default<br>FormChange<br>Druid |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `Conditional_GoodRoll`


**Definition:** Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability.  
**Total Count:** 37

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`StatusOnEndMove`](./Cat_Mutations.md#object-statusonendmove)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Float | The probability of the effect occurring, expressed as a decimal or percentage. | 50 | `.1`<br>`.16666666`<br>`.3` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 37 | Default<br>FormChange<br>Druid |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 15 | passives<br>class<br>tag |
| [`ChangeTilesUnder`](../Reference_and_Meta/Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 9 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |

</details>


---


### Object: `CounterAttack`


**Definition:** Specifies the ability used when the unit counterattacks after being hit.  
**Total Count:** 39

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](../Reference_and_Meta/Enums.md#enum-ability) | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 589 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 101 | `.02`<br>`.1`<br>`.15` |

</details>


---


### Object: `KnockUpAndAway`


**Definition:** Contains parameters for launching the target upward and away from the source, including stacks and distance.  
**Total Count:** 25

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`AddStatusToBasicMeleeAttack`](./Cat_Mutations.md#object-addstatustobasicmeleeattack)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 27 | `-3`<br>`10`<br>`2` |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 234 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


### Object: `MoveWhenDamaged`


**Definition:** Defines movement behavior when the unit takes damage, such as weights and move ability.  
**Total Count:** 12

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](../Reference_and_Meta/Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. | 14 | `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |
| [`move_ability`](../Reference_and_Meta/Enums.md#enum-move_ability) | Enum | Specifies the movement ability (e.g., BirdFly, TrampleMoveOne) used for the movement action. | 13 | `BirdFly`<br>`MD_WalkOne`<br>`MoveOne` |

</details>


---


### Object: `PassiveWhenAtFullMana`


**Definition:** An object listing passive effects that are active only while the unit's mana is full.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 3 | passives<br>class<br>tag |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |

</details>


---


### Object: `PassiveWhileHasStatus`


**Definition:** An object containing `status` and `passives` that grants the listed passives while the unit has the specified status.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`status`](../Reference_and_Meta/Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 160 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 10 | passives<br>class<br>tag |
| [`passives`](../Core_Entities_and_Combat/Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 2807 | `{ . . . }` |

</details>


---


### Object: `SpawnExtraThingsOnBattleStart`


**Definition:** An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start.  
**Total Count:** 32

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`number`](../Reference_and_Meta/Arrays.md#array-number) | Array / Integer | The number of objects to spawn; can be a single integer or an array `[min, max]` for a random range. | 75 | `1`<br>`10`<br>`2` |
| [`object`](../Reference_and_Meta/Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 1014 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |

</details>


---


### Object: `StatusEachRoundEnd`


**Definition:** An object listing status effects applied to the unit at the end of each round.  
**Total Count:** 3

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 2 | `Default`<br>`FormChange`<br>`Druid` | [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | Inherits standard status effect and passive mechanics. You can inject any key from the Engine Status and Passive Keys list here to apply buffs, debuffs, or triggered behaviors. | 1 | Default<br>FormChange<br>Druid |
| [`UseAbility`](../Reference_and_Meta/Enums.md#enum-useability) | Enum  | The name of the ability the target is forced to use. | 14 | `GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>


---


### Object: `StatusEveryXSpellCastsEachTurn`


**Definition:** An object with a 'stacks' value defining status effects applied every X spell casts within a single turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Equation | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 234 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `HealthGain` | Integer | The amount of health restored to the source. | 63 | `1`<br>`10`<br>`2` |

</details>


---


### Object: `StatusIfDidntMove`


**Definition:** An object containing status effects to apply to the unit if it did not move during its turn.  
**Total Count:** 1

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 1 | passives<br>class<br>tag |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusIfUnusedMovePoints`


**Definition:** Specifies status effects applied if the unit ends its turn with unused movement points.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 7 | passives<br>class<br>tag |
| `ManaGain` | Equation | The amount of mana restored to the source, which can be an expression. | 40 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [{Logic Keys}](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | 1 | `Default`<br>`FormChange`<br>`Druid`

</details>


---


### Object: `StatusOnAllyCatDeath`


**Definition:** An object listing status effects applied to the unit when an allied cat dies.  
**Total Count:** 6

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>tag |
| `DamageUp` | Array / Equation | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 113 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |

</details>


---


### Object: `StatusOnCastSpell`


**Definition:** An object listing status effects applied to the unit whenever it casts a spell.  
**Total Count:** 8

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>tag |
| `Charge` | Equation | The number of charge stacks applied. | 43 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusOnDie`


**Definition:** Specifies status effects or actions triggered when the unit dies.  
**Total Count:** 9

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 5 | passives<br>class<br>tag |
| [`ScatterCoins`](../Reference_and_Meta/Arrays.md#array-scattercoins) | Array / Integer  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 8 | `5`<br>`[1 .5]` |

</details>


---


### Object: `StatusOnEatFood`


**Definition:** An object listing status effects applied to the unit when it eats food.  
**Total Count:** 5

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 4 | passives<br>class<br>tag |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 95 | `1`<br>`2`<br>`3` |

</details>


---


### Object: `StatusOnKill`


**Definition:** Specifies status effects or actions triggered when the unit kills an enemy.  
**Total Count:** 40

<details>
<summary><b>Expand</b></summary>

> **Referenced by:** [`ROOT`](./Cat_Mutations.md#object-root)

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md#valid-property-keys) | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 20 | passives<br>class<br>tag |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. | 6 | `1` |

</details>


---


<details>
<summary><b>Conditional_RandomChance</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
<details>
<summary><b>StatusKilledCharacters</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 0 | passives<br>class<br>tag |

</details>
<details>
<summary><b>StatusOnEndMove</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | A generic key for defining a status effect or passive, where the key name is the identifier and the value is its configuration. | 8 | passives<br>class<br>tag |

</details>