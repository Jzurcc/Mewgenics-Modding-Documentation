# Mewgenics Mod Developer Documentation: Mutations, Diseases, and Injuries

This document details how the game applies permanent alterations to a cat's viability over the course of a run, encompassing physical body mutations, systemic diseases, and trauma injuries.

---

## 1. Mutations (`data/mutations/`)

Mutations physically alter a cat's graphics (specifically substituting symbols in `catparts.swf`) and apply permanent stat and passive ability modifications. They are separated into `.gon` files by body part (e.g., `eyes.gon`, `tail.gon`, `body.gon`).

```gon
eyes {
    306 { //Confusing Eyes
        desc "MUTATION_EYES_306_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [3, .1]
            }
        }
    }
}
```
* **Stat Modifiers:** Standard keywords (`str`, `int`, `lck`, etc.) can be used to permanently buff or debuff a cat.
* **Tags:** Tags like `animal` or `birth_defect` are used internally for specific events or item synergies (e.g., items that scale off how many `animal` parts a cat has).
* **Passives:** The exact same passive engine used for Items and Classes is leveraged here.

---

## 2. Diseases and Disorders (`data/passives/disorders.gon`)

Diseases are not standalone objects; they are highly specialized passive ability definitions. They are injected onto a cat using the `SpreadDisease` passive hook.

Because they are fundamentally passives, they can hook into any aspect of combat, such as triggering negative effects on hit or during the end of a turn. Items that cure diseases (like pills) specifically target these internal tags to wipe the passive from the cat's data structure.

---

## 3. Injuries (`data/injuries.gon`)

When a cat "dies" but returns to the house, or suffers trauma during a text event, they are inflicted with an Injury.

```gon
str {
    text "INJURY_NAME_BROKENPAW"
    id 0
    stats { str -1 }
    scars { arms [10 20] }
    alt_animations [
        [walk, brokenPawWalk]
    ]
}
```
* **Stats:** Permanent negative stat modifiers applied to the base cat.
* **Scars:** Hooks into `catparts.swf` to permanently overlay scar graphics onto specific frames of the cat's limbs or body.
* **Animations:** Completely overrides the skeletal animation rig for specific states (e.g., forcing a limping `walk` animation instead of the default run).

---

## Master Reference Database

The tables below are automatically extracted from the game's `.gon` files, outlining every mutation, disease, and injury.

### 4. Master Mutations Database

| Body Part | ID | Description | Stats | Tags | Passives Logic |
| :--- | :--- | :--- | :--- | :--- | :--- |
| body | 301 | +1 Thorns. |  |  | `Thorns 1` |
| body | 309 | Units that contact you get knocked back 2 tiles. |  |  | `MeleeRevengeDamage {<br>                type status<br>                damage 0<br>                knockback 2<br>            }` |
| body | 312 | Spawn a coin when you take damage. |  |  | `SpawnThingOnDamage {<br>                object Coin<br>                chance 100%<br>            }` |
| body | 313 | +1 Kinetic Spikes. |  |  | `KineticSpikes 1` |
| body | 314 | +2 Thorns. |  |  | `Thorns 2` |
| body | 315 | +1 Brace. |  |  | `Brace 1` |
| body | 317 | Immune to Heat Wave weather. |  |  | `DrinkWater 1` |
| body | 318 | 25% chance to spawn a Charmed Fly each turn. |  |  | `SpawnEachTurn {<br>                object CharmedFly<br>                chance 25% <br>            }` |
| body | 319 | When you take damage from an attack, gain a random buff. |  |  | `StatusOnTookDamageFromAbility {<br>                RandomStatusFromPool { <br>                    Charge 1<br>                    Thorns 1<br>                    KineticSpikes 1<br>                    DiminishingHealthRegen 1<br>                    RandomStatUp 1<br>                    Shield 1<br>                }<br>            }` |
| body | 321 | Spawn a Charmed Kitten familiar when you get downed. |  |  | `SpawnOnDowned CharmedKitten` |
| body | 322 | Gain an extra consumable item at the end of each battle. |  |  | `StatusOnBattleEnd {<br>                FindItemFromPool consumables<br>            }` |
| body | 323 | Trample. When damaged, move 1 tile in a random direction. |  |  | `MoveWhenDamaged {<br>                move_ability MoveOne<br>                weights chaotic<br>            }<br>            Trample 3` |
| body | 324 | Gain +1 range when you get a kill. |  |  | `StatusOnKill {<br>                RangeUp 1<br>            }` |
| body | 703 | Start each battle with Bruise 1. |  | birth_defect | `Bruise 1` |
| body | 750 | +1 Thorns.  |  |  | `Thorns 1` |
| body | 758 | Start with +1 Bonus Attack. |  |  | `Quivered 1` |
| ears | 1500 | +2% dodge chance |  | animal | `DodgeChance 2%` |
| ears | 302 | +1 Health and Mana Regeneration while wet. |  | animal | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    HealthRegenUp 1<br>                    AddManaRegen 1<br>                }<br>            }` |
| ears | 303 | Adds +1 Knockback to your basic attack if it's melee. |  | animal | `AddStatusToBasicMeleeAttack {<br>                Knockback 1<br>            }` |
| ears | 309 | Adds +1 Bleed to your basic attack. |  | animal | `AddStatusToBasicAttack {<br>                Bleed 1<br>            }` |
| ears | 313 | Adds +1 Knockback to your basic attack if it's melee. |  | animal | `AddStatusToBasicMeleeAttack {<br>                Knockback 1<br>            }` |
| ears | 314 | Thorns 1. Your basic attack inflicts Bleed if it's melee. |  | animal | `Thorns 1<br>            AddStatusToBasicMeleeAttack {<br>                Bleed 1 <br>            }` |
| ears | 315 | 50% chance to spawn a Charmed Fly each turn. Start with Poison 1. |  | animal | `SpawnEachTurn {<br>                object CharmedFly<br>                good false //good relative to the thing attacking, for luck calculations<br>                chance 50% <br>            }<br>            <br>            // damage 1 per turn<br>            Poison 1` |
| ears | 316 | You can see hidden things. 5% dodge chance. |  | animal | `ShowHiddenThings 1<br>            DodgeChance 5%` |
| ears | 317 | Whenever you down a unit, you have a 10% chance to reanimate that unit with 50% HP. |  |  | `StatusKilledCharacters {<br>                Conditional_RandomChance {<br>                    odds 10%<br>                    AutoReanimate 50%<br>                }<br>            }` |
| ears | 318 | You have Brace 1 while wet. |  | animal | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    Brace 1<br>                }<br>            }` |
| ears | 319 | Gain +1 Charge when you take damage. |  | animal | `StatusOnTookDamage {<br>                Charge 1<br>            }` |
| ears | 320 | +1 Kinetic Spikes. |  |  | `KineticSpikes 1` |
| ears | 321 | Units that contact you get knocked back 1 tile. |  |  | `MeleeRevengeDamage {<br>                knockback 1<br>            }` |
| ears | 323 | Gain 1 HP when your basic attack deals damage. |  |  | `AddStatusToBasicAttack {<br>                FlatLeech 1<br>            }` |
| ears | 325 | If you're wet, gain +1 Charge and +1 [img:shield] at the end of your turn. |  |  | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    StatusEachTurnEnd {<br>                        Shield 1<br>                        Charge 1<br>                    }<br>                } <br>            }` |
| ears | 326 | 5% chance to spawn a Maggot familiar each turn. |  |  | `SpawnEachTurn {<br>                chance 5%<br>                object  CharmedMaggot<br>            }` |
| ears | 327 | An extra food pickup will spawn in each battle. |  | animal | `SpawnOnBattleStartRandomEmptyTile {<br>                    object RandomFoodPickup <br>                }` |
| ears | 328 | 5% chance to Petrify on damage and when hit. |  | animal | `AddStatusToBasicAttack {<br>                Petrify [1, .05]<br>            } <br>            RevengeDamage {<br>                effects {<br>                    Petrify [1, .05]<br>                } <br>            }` |
| ears | 329 | Your basic attack leaves water tiles. |  | animal | `AddStatusToBasicAttack {<br>                ChangeTile WaterTile<br>            }<br>            AddElementsToBasicAttack Water` |
| ears | 330 | Thorns 1. 10% chance to inflict Immobile on units that contact you. |  |  | `Thorns 1<br>            MeleeRevengeDamage {<br>                Immobile 10%<br>            }` |
| ears | 331 | Your basic attack has +1 Knockback. |  |  | `AddStatusToBasicAttack {<br>                Knockback 1<br>            }` |
| ears | 332 | Brace 1. |  |  | `Brace 1` |
| ears | 334 | Spawn 1-3 more coins/scrap around the map on random tiles at the start of each battle. |  |  | `SpawnOnBattleStartRandomEmptyTile {<br>                object Coin<br>                number [1 3]<br>            }` |
| ears | 335 | Start with Bleed 1 and a bonus attack. |  |  | `Bleed 1 <br>            Quivered 1` |
| ears | 336 | You gain 3 mana at the end of your turn if you didn't use your movement action. |  |  | `StatusIfUnusedMovePoints {<br>                ManaGain 3 <br>            }` |
| ears | 337 | Your basic attack inflicts Burn 1. |  |  | `AddStatusToBasicAttack {<br>                Burn 1<br>            }` |
| ears | 338 | Your basic attack has a 15% chance to inflict Freeze. |  |  | `MeleeRevengeDamage {<br>                Freeze [1 0.15]<br>            }` |
| ears | 339 | You have electric immunity. |  |  | `ElementImmune Electric` |
| ears | 341 | 10% chance to backflip when targeted. |  |  | `ChanceToBackflip {<br>                ability BackflipDodge<br>                chance 10%<br>            }` |
| ears | 342 | 20% chance to spawn a Charmed Flea when damaged. |  |  | `SpawnThingOnDamage {<br>                object CharmedFlea<br>                good false //good relative to the thing attacking, for luck calculations<br>                chance 20%<br>            }` |
| ears | 343 | Thorns 1. |  | animal | `Thorns 1` |
| ears | 344 | Spawn a Charmed Kitten familiar when you get downed. |  |  | `SpawnOnDowned CharmedKitten` |
| ears | 345 | Units that contact or attack you have a 15% chance to get Charmed. |  | animal | `RevengeDamage {<br>                effects {<br>                    Charmed [1, .15]           <br>                } <br>            }` |
| ears | 703 | Start each battle with Confusion 2. |  | birth_defect | `Confusion 2` |
| ears | 704 | Start each battle with Immobile 1. |  | birth_defect | `Immobile 1` |
| ears | 750 | Your movement action is a jump. |  | animal | `ReplaceBasicMove_Mutation BasicJump` |
| ears | 751 | +10% dodge chance. |  |  | `DodgeChance 10%` |
| ears | 752 | You have +2 Damage while wet. |  | animal | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    DamageUp 2 <br>                }<br>            }` |
| ears | 753 | +1 Knockback damage. Your basic attack has +1 Knockback. |  | animal | `AddKnockbackDamage 1<br>            AddStatusToBasicAttack {<br>                Knockback 1<br>            }` |
| ears | 754 | Electric damage you deal is increased by 1. |  |  | `AddDamageToElementDamage {<br>                element Electric<br>                damage 1<br>            }` |
| ears | 755 | Gain +1 Charge every time you cast a spell. |  |  | `StatusOnCastSpell {<br>                Charge 1<br>            }` |
| ears | 900 | +10% dodge chance. |  |  | `DodgeChance 10%` |
| eyebrows | 301 |  |  |  | `RevengeDamage {<br>                type status<br>                damage 0<br>                effects {<br>                    Confusion [1, .1]<br>                }<br>            }` |
| eyebrows | 306 |  |  |  | `RevengeDamage {<br>                type status<br>                damage 0<br>                effects {<br>                    Fear [1, .05]<br>                }<br>            }` |
| eyebrows | 307 |  |  |  | `HealthRegenUp 1<br>            AddManaRegen 1` |
| eyebrows | 309 |  |  |  | `Thorns 1` |
| eyebrows | 310 |  |  | extra | `AddBonusRange 1` |
| eyebrows | 311 |  |  |  | `StatusEveryXSpellCastsEachTurn {<br>                stacks 3<br>                HealthGain 2<br>            }` |
| eyebrows | 313 |  |  |  | `SpawnExtraThingsOnBattleStart {<br>                object RandomPickup<br>                number [1 2]<br>            }` |
| eyebrows | 314 |  |  |  | `StatusOnAllyCatDeath {<br>                DamageUp 2<br>            }` |
| eyebrows | 315 |  |  |  | `AddLevelUpRerolls 1` |
| eyebrows | 900 |  |  |  | `AddStatusToBasicAttack {<br>                Freeze [1 .01]<br>            }<br>            DodgeChance 5%` |
| eyes | -2 | Blind. |  | birth_defect | `Blind -1` |
| eyes | 1029 | +5% crit chance. |  |  | `CritChanceUp 5` |
| eyes | 300 | Your basic attack has a 10% chance to inflict Fear. |  |  | `AddStatusToBasicAttack {<br>                Fear [1 .1]<br>            }` |
| eyes | 302 | +1 Thorns. |  |  | `Thorns 1` |
| eyes | 304 | Take your turn later. |  |  | `AddInitiative -20` |
| eyes | 306 | Your basic attack has a 10% chance to inflict Confusion 3. |  |  | `AddStatusToBasicAttack {<br>                Confusion [3, .1]<br>            }` |
| eyes | 307 | Gain 1 mana when anything dies. |  |  | `GainManaWhenAnythingDies 1` |
| eyes | 308 | +5% dodge chance. |  | animal | `DodgeChance 5%` |
| eyes | 309 | +2 corpse health. |  |  | `AddCorpseHealth 2` |
| eyes | 310 | +1 Health Regeneration |  | animal | `HealthRegenUp 1` |
| eyes | 311 | You do not take extra damage from backstabs. |  | animal | `BackstabImmunity 1` |
| eyes | 312 | +1 Brace. |  |  | `Brace 1` |
| eyes | 313 | Your basic attack creates water tiles. |  |  | `AddStatusToBasicAttack {<br>                ChangeTile WaterTile<br>            }<br>            AddElementsToBasicAttack Water` |
| eyes | 314 | When you are downed, spawn 3 Flies. +2 corpse health. |  |  | `SpawnOnDowned CharmedFly<br>            SpawnOnDowned CharmedFly<br>            SpawnOnDowned CharmedFly<br>            AddCorpseHealth 2` |
| eyes | 315 | +1 Kinetic Spikes. |  |  | `KineticSpikes 1` |
| eyes | 316 | 15% chance to counter attack with Chain Lightning when you get hit. |  |  | `CounterAttack {<br>                chance 15%<br>                ability ChainLightning<br>            }` |
| eyes | 317 | Gain a random stat up at the end of each turn. |  |  | `StatusEachTurnEnd {<br>                RandomStatUp 1<br>            }` |
| eyes | 318 | You can see hidden things. +1 Knockback damage. |  | animal | `ShowHiddenThings 1<br>            AddKnockbackDamage 1` |
| eyes | 319 | Blind. +1 Damage. +1 Thorns. |  |  | `Blind -1  <br>            Thorns 1<br>            DamageUp 1` |
| eyes | 324 | Spawn 2 extra coins each battle. |  |  | `SpawnOnBattleStartRandomEmptyTile {<br>                object Coin<br>                number 2<br>            }` |
| eyes | 325 | Thorns 1. |  |  | `Thorns 1` |
| eyes | 326 | Gain 2 Charge each time you cast 4 spells. |  |  | `StatusEveryXSpellCasts {<br>                stacks 4<br>                Charge 2<br>            }` |
| eyes | 328 | +10% crit chance. |  | animal | `CritChanceUp 10` |
| eyes | 329 | Your basic attack has a 15% chance to inflict Confusion. |  |  | `AddStatusToBasicAttack {<br>                Confusion [1, .15]<br>            }` |
| eyes | 331 | At the start of each battle, gain a random temporary pill if your trinket slot is empty. |  |  | `EquipRandomTemporaryItemFromPool pills` |
| eyes | 332 | Start each battle Bleeding. Gain 1 Charge each time you take damage. |  |  | `Bleed 1  <br>            StatusOnTookDamage {<br>                Charge 1<br>            }` |
| eyes | 333 | Your basic attack can't miss. |  |  | `BasicAttackCantMiss 1` |
| eyes | 334 | Blind. Spawn a Flea when you take damage.  |  |  | `Blind -1<br>            SpawnThingOnDamage {<br>                object CharmedFlea<br>                good false //good relative to the thing attacking, for luck calculations<br>                chance 100%<br>            }` |
| eyes | 335 | Your basic attack has a 10% chance to Charm. |  |  | `AddStatusToBasicAttack {<br>                Charmed [1, .10]  <br>            }` |
| eyes | 336 | Your basic attack is electric element and has a 5% chance to stun. |  |  | `AddElementsToBasicAttack Electric<br>            AddStatusToBasicAttack {<br>                Stun [1 .05]<br>            }` |
| eyes | 337 | Your basic attack is ice element and inflicts Slow. |  |  | `AddStatusToBasicAttack {<br>                Slow 1<br>            }<br>            AddElementsToBasicAttack Ice` |
| eyes | 338 | Your basic attack inflicts Burn. |  |  | `AddStatusToBasicAttack {<br>                Burn 1<br>            }<br>            AddElementsToBasicAttack Fire` |
| eyes | 339 | +1 Health Regeneration while wet. Your basic attack is water element. |  |  | `AddElementsToBasicAttack Water  <br>            PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    HealthRegenUp 1<br>                } <br>            }` |
| eyes | 340 | Your basic attack inflicts Leech. |  |  | `AddStatusToBasicAttack {<br>                Leeches 1<br>            }` |
| eyes | 341 | Gain Charge 1 the first time you move each turn. |  |  | `StatusOnEndMove {<br>                Conditional_FirstApplicationThisTurn {<br>                    Charge 1<br>                }<br>            }` |
| eyes | 342 | Your basic attack inflicts Poison 1. Start each battle Poisoned. |  |  | `AddStatusToBasicAttack {<br>                Poison 1<br>            } <br>            Poison 1` |
| eyes | 343 | You have a 5% chance to inflict Fear on units who contact or attack you. |  |  | `RevengeDamage {<br>                effects {<br>                    Fear [1, .05]<br>                }<br>            }` |
| eyes | 344 | You have a 10% chance to Blind units who contact or attack you. |  |  | `RevengeDamage {<br>                effects {<br>                    Blind [1, .10]<br>                }<br>            }` |
| eyes | 345 | Inflict a random debuff on units who contact you. |  |  | `MeleeRevengeDamage {<br>                effects {<br>                    RandomStatusFromPool {<br>                        Poison 1<br>                        Burn 1<br>                        Bleed 1<br>                        Blind 1 <br>                        Weakness 1 <br>                    }<br>                } <br>            }` |
| eyes | 346 | Spawn a rock when damaged.  |  |  | `SpawnThingOnDamage {<br>                object SmallRock<br>                good false //good relative to the thing attacking, for luck calculations<br>                chance 100%<br>            }` |
| eyes | 347 | Your basic attack has a 15% chance to inflict Confusion 2. |  |  | `AddStatusToBasicAttack {<br>                Confusion [2, .15]<br>            }` |
| eyes | 348 | +1 range, +1 reach. |  |  | `AddBonusRange 1<br>            AddBonusMeleeRange 1` |
| eyes | 349 | Emit 4 Sparkles each time you cast 8 spells. |  |  | `StatusEveryXSpellCasts {<br>                stacks 8<br>                RandomMagicMissile 4<br>            }` |
| eyes | 351 | Your bonus ability is a different random spell each battle. |  |  | `ConjureBonusAbility random` |
| eyes | 352 | You have All Stats Up while Bleeding. |  |  | `PassiveWhileHasStatus {<br>                status Bleed<br>                passives {<br>                    AllStatsUp 1  <br>                } <br>            }` |
| eyes | 353 | You take no extra damage from backstabs. |  | animal | `BackstabImmunity 1` |
| eyes | 442 | 10% chance to reflect projectiles. |  |  | `ReflectProjectiles 10%` |
| eyes | 704 | 10% miss chance. |  | birth_defect | `MissChance 10` |
| eyes | 705 | Gain 5% miss chance every turn. |  | birth_defect | `StatusEachTurnBegin {<br>                MissChance 5<br>            }` |
| eyes | 706 | Start each battle with Confusion 2. |  | birth_defect | `Confusion 2` |
| eyes | 754 | +1 range. Your basic attack is gravity element. |  |  | `AddBonusRange 1<br>            AddElementsToBasicAttack Gravity` |
| eyes | 755 | Your basic attack has a 15% chance to inflict Fear. |  |  | `AddStatusToBasicAttack {<br>				Fear [1 .15]<br>			}` |
| eyes | 900 | Your basic attack has a 10% chance to inflict Slow. |  |  | `AddStatusToBasicAttack {<br>                Slow [1 .1]<br>            }` |
| head | 303 | +1 Thorns. |  |  | `Thorns 1` |
| head | 304 | +2 Health Regeneration +5% dodge chance. |  | melted | `HealthRegenUp 2<br>            DodgeChance 5%` |
| head | 307 | Units that contact you get knocked back 1 tile. |  |  | `MeleeRevengeDamage {<br>                type status<br>                damage 0<br>                knockback 1<br>            }` |
| head | 308 | +1 movement range while wet. Water does not slow movement. |  | animal | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    AddMovement 1<br>                }<br>            } <br>            WaterWalk 1` |
| head | 311 | Spawn a coin when you take damage. |  |  | `SpawnThingOnDamage {<br>                object Coin <br>                chance 100%<br>            }` |
| head | 312 | Your basic attack pulls units towards you. |  |  | `MakeBasicAttackPull 1` |
| head | 313 | Poop when you take damage. |  |  | `PoopWhenHit Poop` |
| head | 314 | Gain +1 [img:int] at the end of each turn. |  |  | `StatusEachTurnEnd {<br>               IntelligenceUp 1<br>            }` |
| head | 315 | At the start of each battle, swap your highest and lowest stats. |  |  | `SwapHighestAndLowestStat 1` |
| head | 316 | When you take damage from an attack, gain a random buff. |  |  | `StatusOnTookDamageFromAbility {<br>                RandomStatusFromPool { <br>                    Charge 1<br>                    Thorns 1<br>                    KineticSpikes 1<br>                    DiminishingHealthRegen 1<br>                    RandomStatUp 1<br>                    Shield 1<br>                }<br>            }` |
| head | 317 | +5% dodge chance. |  |  | `DodgeChance 5%` |
| head | 318 | +1 range. |  |  | `AddBonusRange 1` |
| head | 319 | Gain +1 [img:int] permanently at the end of each battle. Start each battle with Bruise 2. |  |  | `Bruise 2<br>            StatusOnBattleEnd {<br>                PermanentIntelligence 1<br>            }` |
| head | 320 | Your basic attack has +2 Knockback. |  |  | `AddStatusToBasicAttack {<br>                Knockback 2<br>            }` |
| head | 321 | You have a 5% chance to inflict Fear on units who contact or attack you. |  |  | `RevengeDamage {<br>                effects {<br>                    Fear [1, .05]<br>                }<br>            }` |
| head | 703 | Attacks against your face count as backstabs. |  | birth_defect | `BackstabFront 1` |
| head | 704 | 20% miss chance. Your spells cost 1 less mana. |  | birth_defect | `MissChance 20<br>            ManaCostReduction 1` |
| head | 706 | Brace 1. |  | birth_defect | `Brace 1` |
| head | 750 | +1 Thorns. |  |  | `Thorns 1` |
| head | 753 | You are immune to ice. |  |  | `ElementImmune Ice<br>			StatusImmunity [Freeze, Slow]` |
| head | 759 | Take an extra turn at the start of the battle. |  |  | `AlphaTurns 1` |
| head | 900 | +1 range. +1 reach. |  |  | `AddBonusRange 1<br>            AddBonusMeleeRange 1` |
| legs | 300 | +1 movement range while wet. Water does not slow movement. |  | animal | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    AddMovement 1<br>                }<br>            }<br><br>            WaterWalk 1` |
| legs | 301 | Your basic attack has a 5% chance to Stun. |  | animal | `AddStatusToBasicAttack {<br>                Stun [1, .05]<br>            }` |
| legs | 302 | Knockback immunity. |  | animal | `KnockbackImmunity 1` |
| legs | 303 | Your basic attack has a 5% chance to Immobilize. |  | animal | `AddStatusToBasicAttack {<br>                Immobile [1, .05]<br>            }` |
| legs | 305 | +5% dodge chance. |  |  | `DodgeChance 5%` |
| legs | 309 | Your basic attack has a 10% chance to inflict Bleed 3. |  |  | `AddStatusToBasicAttack {<br>                Bleed [3, .1]<br>            }` |
| legs | 310 | Your movement action is a jump. |  |  |  |
| legs | 312 | Your basic attack has +1 Knockback. |  |  | `AddStatusToBasicAttack {<br>                Knockback 1<br>            }` |
| legs | 313 | +1 reach. |  |  | `AddBonusMeleeRange 1` |
| legs | 314 | Your weapons have +1 Damage. |  |  | `BoostWeaponDamage 1` |
| legs | 315 | Ice immunity. |  |  | `ElementImmune Ice` |
| legs | 317 | Your basic attack inflicts Bleed 1 if it's melee. |  |  | `AddStatusToBasicMeleeAttack {<br>                Bleed 1<br>            }` |
| legs | 319 | 10% chance to gain a bonus move each turn. |  |  | `StatusEachTurnBegin {<br>                MoveQuivered [1, 0.1]<br>            }` |
| legs | 320 | 10% chance to gain a bonus attack each turn. |  |  | `StatusEachTurnBegin {<br>                Quivered [1, 0.1]<br>            }` |
| legs | 321 | Moving through water tiles costs 0 movement. |  |  | `FreePathfindElement Water` |
| legs | 325 | Collarless spells cost -1 mana. |  | extra | `ClassManaCostReduction {<br>                class Colorless<br>                reduction 1<br>            }` |
| legs | 326 | Your basic attack inflicts a random debuff. |  |  | `AddStatusToBasicAttack {<br>                RandomStatusFromPool {<br>                    Poison 1<br>                    Burn 1<br>                    Bleed 1<br>                    Blind 1 <br>                    Weakness 1 <br>                }<br>            }` |
| legs | 327 | Gain 2 random stat ups and 1 random stat down at the end of each turn. |  |  | `StatusEachTurnEnd {<br>               RandomStatUp 2<br>               RandomStatDown 1<br>           }` |
| legs | 328 | Equip a temporary Bottles weapon at the start of the battle. |  |  | `EquipTemporaryItem Bottles` |
| legs | 329 | Equip a temporary Water Bottle trinket at the start of the battle. |  |  | `EquipTemporaryItem WaterBottle_Full` |
| legs | 330 | +1 Health Regeneration |  |  | `HealthRegenUp 1` |
| legs | 331 | +1 movement range. Your movement action is a jump. |  |  | `AddMovement 1` |
| legs | 332 | 50% chance to spawn a pickup on an adjacent tile when you end your turn.  |  |  | `SpawnEachTurn {<br>                object RandomPickup<br>                chance 50%<br>            }` |
| legs | 333 | Your basic attack has wind element and +1 Knockback. |  |  | `AddStatusToBasicAttack {<br>                Knockback 1<br>                VisualFXTile fx_windSpell<br>            }<br>            AddElementsToBasicAttack Wind` |
| legs | 334 | Your basic attack tosses units into the air if it's melee. |  |  | `AddStatusToBasicMeleeAttack { <br>               KnockUpAndAway {<br>                   stacks 3<br>                   distance 3<br>               }<br>           }` |
| legs | 335 | +1 Bleed Thorns. Spawn glass when you take damage. |  |  | `BleedThorns 1 <br>            StatusOnTookDamage {<br>                ChangeTilesUnder GlassTile <br>            }` |
| legs | 336 | Your basic attack inflicts Soul Link. |  | bird | `AddStatusToBasicAttack {<br>                SoulLink 1<br>            }` |
| legs | 337 | You are immune to tile effects. |  |  | `IgnoreTiles 1` |
| legs | 339 | Fly away when hit. |  | bird | `MoveAwayFromDamageSource BasicJump` |
| legs | 340 | When you take damage, gain +1 [img:lck]. |  |  | `StatusOnTookDamage {<br>               LuckUp 1<br>           }` |
| legs | 341 | Your basic attack makes units face away from you. |  |  | `AddStatusToBasicAttack { <br>                FaceAway 1<br>            }` |
| legs | 343 | Spawn a Charmed Kitten familiar when you get downed. |  |  | `SpawnOnDowned CharmedKitten` |
| legs | 703 | Water does not slow movement. |  | birth_defect | `WaterWalk 1` |
| legs | 705 | Trample. |  | birth_defect | `Trample 3` |
| legs | 707 | Permanently Slow. |  | birth_defect | `Slow -1` |
| legs | 754 | Your movement action is a jump. Your basic attack inflicts Bruise. |  |  | `ReplaceBasicMove ToadJump_BasicMove<br>		    AddStatusToBasicAttack {<br>                Bruise 1<br>            }` |
| legs | 757 | Trample. |  |  | `Trample 3` |
| legs | 758 | You have All Stats Up while wet. |  |  | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    AllStatsUp 1<br>                }<br>            }` |
| legs | 759 | You have All Stats Up while wet. |  |  | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    AllStatsUp 1<br>                }<br>            }` |
| legs | 761 | Your movement action is a jump. Your basic attack inflicts Bleed. |  |  | `ReplaceBasicMove ToadJump_BasicMove<br>		    AddStatusToBasicAttack {<br>                Bleed 1<br>            }` |
| legs | 762 | Ignore the effects of tiles and traps. |  |  | `IgnoreTiles 1<br>            YOffset .25` |
| legs | 763 | Ignore the effects of tiles and traps. |  |  | `IgnoreTiles 1<br>            YOffset .25` |
| legs | 900 | Ignore the effects of tiles and traps. |  |  | `IgnoreTiles 1<br>            YOffset .25` |
| mouth | -2 | Can't eat food, use consumables, or use musical abilities. |  | birth_defect | `Vegan 1<br>            HouseFoodRequirementMultiplier 0<br>            DisableAbilitiesWithTag consumable<br>            DisableAbilitiesWithTag musical<br>            BlacklistPickupType food<br>            BlacklistPickupType catnip` |
| mouth | 1026 | Your basic attack has a 10% chance to inflict Webbed. |  | animal | `AddStatusToBasicAttack {<br>                Webbed [1 .1]<br>            }` |
| mouth | 1500 | Your basic attack inflicts Poison. |  | animal | `AddStatusToBasicAttack {<br>                Poison 1<br>            }` |
| mouth | 301 | Gain 1 health when you deal damage. |  | animal | `FlatHealWhenDealDamage 1` |
| mouth | 302 | +1 Health Regeneration |  |  | `HealthRegenUp 1` |
| mouth | 304 | Your basic attack inflicts Poison. |  | animal | `AddStatusToBasicAttack {<br>                Poison 1<br>            }` |
| mouth | 305 | +100 corpse health. |  |  | `AddCorpseHealth 100` |
| mouth | 306 | 10% chance to spawn a Fly when you take damage. |  |  | `SpawnThingOnDamage {<br>                object Fly<br>                good false //good relative to the thing attacking, for luck calculations<br>                chance 10%<br>            }` |
| mouth | 307 | Your basic attack has a 1% chance to instakill. |  |  | `AddStatusToBasicAttack {<br>                Instakill [25, .01]<br>            }` |
| mouth | 308 | +1 Health Regeneration |  |  | `HealthRegenUp 1` |
| mouth | 309 | Your basic attack has a 10% chance to inflict Fear. |  |  | `AddStatusToBasicAttack {<br>                Fear [1 .1]<br>            }` |
| mouth | 311 | Your basic attack inflicts Leech 1. |  |  | `AddStatusToBasicAttack {<br>                Leeches 1<br>            }` |
| mouth | 312 | Your basic attack has a 10% chance to inflict Immobile if it's melee. |  |  | `AddStatusToBasicMeleeAttack {<br>                Immobile [1, .1]<br>            }` |
| mouth | 313 | At the end of each round, spit at an enemy . |  |  | `StatusEachRoundEnd {<br>                UseAbility Spit<br>             }` |
| mouth | 314 | Spawn 5-10 coins when downed. |  |  | `StatusOnDie {<br>                 ScatterCoins 5<br>                 ScatterCoins [1 .5]<br>                 ScatterCoins [1 .5]<br>                 ScatterCoins [1 .5]<br>                 ScatterCoins [1 .5]<br>                 ScatterCoins [1 .5]<br>             }` |
| mouth | 315 | 10% chance to gain a bonus attack each turn. |  |  | `StatusEachTurnBegin {<br>                Quivered [1, 0.1]<br>            }` |
| mouth | 316 | Your basic attack inflicts Bruise. |  |  | `AddStatusToBasicAttack {<br>                Bruise 1<br>            }` |
| mouth | 317 | Spawn glass when you take damage. +1 Bleed Thorns.  |  |  | `BleedThorns 1 <br>            StatusOnTookDamage {<br>                ChangeTilesUnder GlassTile <br>            }` |
| mouth | 318 | Your movement action is Dig. |  |  | `ReplaceBasicMove_Mutation BasicDig` |
| mouth | 319 | Water does not slow movement. +1 Health Regeneration while wet. |  |  | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    HealthRegenUp 1 <br>                }<br>            } <br>            WaterWalk 1` |
| mouth | 322 | Your basic attack inflicts Bleed. |  |  | `AddStatusToBasicAttack {<br>                Bleed 1<br>            }` |
| mouth | 323 | +2 Health Regeneration while wet. |  |  | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    HealthRegenUp 2 <br>                }<br>            }` |
| mouth | 324 | +1 range. |  |  | `AddBonusRange 1` |
| mouth | 326 | Gain +1 Health Regeneration whenever you eat food. |  |  | `StatusOnEatFood {<br>                HealthRegenUp 1 <br>            }` |
| mouth | 327 | You can reroll your options when you level up. |  |  | `AddLevelUpRerolls 1` |
| mouth | 328 | Can't eat food, use consumables, or use musical abilities. +2 Health Regeneration  |  |  | `HealthRegenUp 2<br><br>            Vegan 1<br>            HouseFoodRequirementMultiplier 0<br>            DisableAbilitiesWithTag consumable<br>            DisableAbilitiesWithTag musical<br>            BlacklistPickupType food<br>            BlacklistPickupType catnip` |
| mouth | 705 | Your basic attack can be used two extra times each turn but is replaced with a 1-damage spit attack. |  |  | `ExtraBasicAttacks 2<br>            ReplaceBasicAttack_Mutation FetusSpit` |
| mouth | 750 | Your basic attack destroys inanimate objects and turns tiles into dirt. |  |  | `AddStatusToBasicAttack {<br>                ChangeTile DirtTile<br>				VaporizeInanimate 1<br>            }` |
| mouth | 752 | Your basic attack creates water tiles. |  |  | `AddStatusToBasicAttack {<br>                ChangeTile WaterTile<br>            }<br>            AddElementsToBasicAttack Water` |
| mouth | 754 | Adjacent units get All Stats Down. |  |  | `DepressionAura 1` |
| mouth | 755 | Ice Immunity. |  |  | `ElementImmune Ice` |
| mouth | 757 | Your basic attack inflicts Bleed. |  |  | `AddStatusToBasicAttack {<br>				Bleed 1<br>			}` |
| mouth | 760 | When a food pickup spawns within 2 tiles of you, move to it. |  | food | `AbilityWhenTaggedCharacterMovesNear {<br>                ability move<br>                tag food<br>                range 2<br>            }` |
| mouth | 900 | Your basic attack has a 10% chance to inflict Fear. |  |  | `AddStatusToBasicAttack {<br>                Fear [1 .1]<br>            }` |
| tail | 301 | Poop when you take damage. |  | animal | `PoopWhenHit Poop` |
| tail | 302 | Your basic attack inflicts Poison. |  | animal | `AddStatusToBasicAttack {<br>                Poison 1<br>            }` |
| tail | 303 | Your basic attack has a 5% chance to Stun. |  |  | `AddStatusToBasicAttack {<br>                Stun [1, .05]<br>            }` |
| tail | 305 | +1 Thorns. |  |  | `Thorns 1` |
| tail | 308 | +5% dodge chance. |  |  | `DodgeChance 5%` |
| tail | 310 | Your basic attack has a 10% chance to repeat once. |  |  | `AddTemporaryEffectsToBasicAttack {<br>                Fury 10<br>            }` |
| tail | 311 | Thorns 1. |  |  | `Thorns 1` |
| tail | 313 | Your basic attack creates water tiles. |  |  | `AddStatusToBasicAttack {<br>                ChangeTile WaterTile<br>            }<br>            AddElementsToBasicAttack Water` |
| tail | 314 | Whenever you down a unit, you have a 10% chance to reanimate that unit with 50% HP. |  |  | `StatusKilledCharacters {<br>                Conditional_RandomChance {<br>                    odds 10%<br>                    AutoReanimate 50%<br>                }<br>            }` |
| tail | 315 | 20% chance to spawn a Maggot when hit. |  |  | `SpawnThingOnDamage {<br>                object Maggot<br>                good false //good relative to the thing attacking, for luck calculations<br>                chance 20%<br>            }` |
| tail | 316 | 25% chance to spawn tall grass wherever you end your movement. |  |  | `StatusOnEndMove {<br>                Conditional_GoodRoll {<br>                    odds 25%<br>                    ChangeTilesUnder TallGrassTile<br>                }<br>            }` |
| tail | 317 | When hit, fart a Poison 4 attack with Knockback behind you. |  |  | `AbilityReaction SkunkTail` |
| tail | 318 | Your basic attack inflicts Poison. |  |  | `AddStatusToBasicAttack {<br>                Poison 1<br>            }` |
| tail | 319 | Units who contact you get Poisoned. |  |  | `PoisonThorns 1` |
| tail | 320 | Bleed 1. Bleed Thorns 2. |  |  | `Bleed 1 <br>            BleedThorns 2` |
| tail | 322 | Gain +1 [img:spd] each turn. |  |  | `StatusEachTurnBegin {<br>                SpeedUp 1<br>            }` |
| tail | 323 | Your movement action is a jump. |  |  | `ReplaceBasicMove_Mutation BasicJump` |
| tail | 325 | Units that contact you get knocked back 2 tiles. |  |  | `MeleeRevengeDamage {<br>                knockback 2<br>            }` |
| tail | 326 | 10% dodge chance. Bruise 1. |  |  | `Bruise 1<br>            DodgeChance 10%` |
| tail | 327 | If you don't move, gain 3 Charge at the end of the turn. |  |  | `StatusIfDidntMove {<br>                Charge 3<br>            }` |
| tail | 329 | You can unequip cursed items and parasites. |  |  | `CanRemoveCursedItems 1` |
| tail | 331 | You can reroll your options when you level up. |  |  | `AddLevelUpRerolls 1` |
| tail | 332 | +25% chance to reflect projectiles. |  |  | `ReflectProjectiles 25%` |
| tail | 334 | Your basic attack inflicts Burn 1. |  |  | `AddStatusToBasicAttack {<br>                Burn 1 <br>            }<br>            AddElementsToBasicAttack Fire` |
| tail | 336 | +1 Thorns. |  |  | `Thorns 1` |
| tail | 337 | Your basic attack is wind element. |  | bird | `AddStatusToBasicAttack {<br>                Knockback 1<br>                VisualFXTile fx_windSpell<br>            }<br>            AddElementsToBasicAttack Wind` |
| tail | 338 | Your basic attack inflicts Burn 1. |  |  | `AddStatusToBasicAttack {<br>                Burn 1 <br>            }<br>            AddElementsToBasicAttack Fire` |
| tail | 339 | While at full mana, you have +2 Damage. |  |  | `PassiveWhenAtFullMana {<br>                DamageUp 2<br>            }` |
| tail | 341 | Gain +1 Charge when you take damage. |  |  | `StatusOnTookDamage {<br>                Charge 1<br>            }` |
| tail | 342 | Spawn a Charmed Kitten familiar when you get downed. |  |  | `SpawnOnDowned CharmedKitten` |
| tail | 703 | Start each battle with Immobile 1. |  | birth_defect | `Immobile 1` |
| tail | 704 | Hunter abilities are also offered when you level up. |  | birth_defect | `MulticlassLevelUp Hunter` |
| tail | 751 | +1 Brace. |  |  | `Brace 1` |
| tail | 754 | +1 Thorns. |  |  | `Thorns 1` |
| tail | 755 | Water does not slow movement. |  |  | `WaterWalk 1` |
| tail | 756 | +1 Bleed Thorns. |  |  | `BleedThorns 1` |
| tail | 757 | Your movement action is shadowstep. |  |  | `ReplaceBasicMove Shadowstep` |
| tail | 759 | Start with +1 Bonus Attack. |  |  | `Quivered 1` |
| tail | 760 | Start with 2 backflips. |  |  | `BackflipWhenTargeted {<br>                stacks 2<br>                ability BackflipDodge<br>            }` |
| texture | 300 | +1 Health Regeneration |  |  | `HealthRegenUp 1` |
| texture | 301 | +1 Health and Mana Regeneration while wet. |  |  | `PassiveWhenAffectedByElement {<br>                element water<br>                passives {<br>                    HealthRegenUp 1<br>                    AddManaRegen 1<br>                }<br>            }` |
| texture | 303 | Start each battle with a random stat up. |  |  | `RandomStatUp 1` |
| texture | 304 | Units that contact or attack you have a 10% chance to become Confused. |  |  | `RevengeDamage {<br>                type status<br>                damage 0<br>                effects {<br>                    Confusion [1, .1]<br>                }<br>            }` |
| texture | 307 | +5% dodge chance. |  |  | `DodgeChance 5%` |
| texture | 309 | Your basic attack has a 5% chance to inflict Fear. You have a 5% chance to inflict Fear on units who contact or attack you. |  |  | `RevengeDamage {<br>                type status<br>                damage 0<br>                effects {<br>                    Fear [1, .05]<br>                }<br>            }<br><br>            AddStatusToBasicAttack {<br>                Fear [1, .05]<br>            }` |
| texture | 310 | Gain double the effects of pickups you collect. |  |  | `AddLootMultiplier 1` |
| texture | 702 | Start each battle with Bleed 1. |  | birth_defect | `Bleed 1` |
| texture | 703 | Mage abilities are also offered when you level up. |  | birth_defect | `MulticlassLevelUp Mage` |
| texture | 704 | Fighter abilities are also offered when you level up. |  | birth_defect | `MulticlassLevelUp Fighter` |
| texture | 705 | Thief abilities are also offered when you level up. |  | birth_defect | `MulticlassLevelUp Thief` |
| texture | 706 | 10% dodge chance. |  | birth_defect | `DodgeChance_Status 10` |
| texture | 750 | Units who contact you get Poison 2. |  |  | `PoisonThorns 2` |

---

### 5. Master Diseases Database

| Internal ID | Name | Description | Passives Logic |
| :--- | :--- | :--- | :--- |
| Rabies | Rabies | Your basic attack is a melee attack. You can't equip face armor. After each battle, gain +2 [img:str] and -1 [img:int]. If your [img:int] is 0 or less, you have Madness. | `StatusOnBattleEnd {<br>            PermanentStrength 2<br>            PermanentIntelligence -1<br>            even_if_dead true<br>        }<br><br>        PassiveAtStatThreshold {<br>            mode less_or_equal<br>            threshold {<br>                int 0<br>            }<br>            passives {<br>                PermanentMadness 1<br>            }<br>        }<br><br>        AddStatusToBasicMeleeAttack {<br>            SpreadDisease {<br>                chance 25%<br>                disease Rabies<br>            }<br>        }<br><br>        OverrideBasicAttack BasicMelee` |
| Boils | Boils | +1 Brace. You spawn a puddle of creep whenever you get hit. You can't equip face armor. | `SpawnCreepOnHit 1<br>        Brace 1` |
| Depression | Depression | Adjacent units get All Stats Down 2. | `AllStatsUp -1<br>        DepressionAura 2` |
| BrokenLimb | Broken Limb | You can't equip trinkets or consumables. +2 Thorns. | `Thorns 2` |
| WrenchedNeck | Wrenched Neck | You can't equip neck armor. Double the effects of your head armor. | `HeadArmorPassiveMultiplierBonus 1` |
| Declawed | Declawed | You can't equip weapons. |  |
| HeadTrauma | Head Trauma | You can't equip head armor. Your Collarless spells cost -2 mana. | `ClassManaCostReduction {<br>            class Colorless<br>            reduction 2<br>        }` |
| DeepCut | Deep Cut | Bleed 1. You can't equip trinkets or consumables.  Bonus ability: Bloodzerk. | `Bleed 1<br>        BonusAbility Bloodzerk` |
| PuncturedEye | Punctured Eye | +10% miss chance. You can't equip face armor. Gain an eyeball trinket. | `MissChance 10` |
| OCD | Obsessive Compulsive Disorder | Bonus Ability: Groom At the end of your turn, if you didn't use Groom, take 2 damage. | `DamageIfDidntUseSpecificAbility {<br>            ability Groom<br>            damage 2<br>        }<br>        BonusAbility Groom` |
| Distemper | Distemper | At the end of each battle gain +10% crit chance, +25% crit damage, and +5% miss chance. Permanently. You can't equip face armor. | `MissChance 5<br>            CritChanceUp 10<br>			AddCritMultiplier 25%<br>            PassiveLevelUpAtCombatEnd 1` |
| BrainDamage | Brain Damage | You can't use item actions. +2 Brace. | `DisableAbilities all_items<br>		Brace 2` |
| SeveredThumb | Severed Thumb | You can't equip weapons. Spawn a Food pickup at the start of each battle. | `AbilityOnBattleStart neck_ChefsApron` |
| PTSD | Post-Traumatic Stress Disorder | When you take damage, gain Fear and +2 Damage. | `StatusOnTookDamage {<br>            Conditional_HasStatus {<br>                status Fear<br>            } Else {<br>                Fear 1<br>            }<br>            DamageUp 2<br>        }` |
| IBS | Irritable Bowel Syndrome | When you take damage, poop. | `PoopWhenHit Poop` |
| Dyskinesia | Dyskinesia | When you end your movement, knockback all adjacent units 1 tile. | `DamageNeighborsOnEndMove {<br>            type status<br>            damage 0<br>            knockback 1<br>        }` |
| Anemia | Anemia | When you take damage, you have a 10% chance to gain Bleed 1. Gain 2 Charge for each damage you take from Bleed. | `AddStatusToReceivedDamage_ExcludeStatuses {<br>            Conditional_DoesDamage {<br>                Bleed [1 .1]<br>            }<br>        }<br>        ScaledStatusOnBleedDamage {<br>            Charge 2<br>        }` |
| Empath | Empath | Take 1 damage when you deal damage. Your heals heal for 1 extra. | `SelfDamageWhenDealDamage {<br>            type status<br>            damage 1<br>        }<br>        BoostHeals 1` |
| Infestation | Infestation | At the start of your turn, you have a 50% chance to spawn a Maggot Familiar and 15% chance to spawn an enemy Flea. | `SpawnEachTurn {<br>            chance 15%<br>            object Flea<br>            good false<br>        }<br>        SpawnEachTurn {<br>            chance 50%<br>            object CharmedMaggot<br>        }` |
| Leprosy | Leprosy | Bruise 2. When you get hit, spawn a food pickup. | `Bruise 2<br>        SpawnThingOnDamage {<br>            object Food<br>            good true<br>        }` |
| ASRFight | Acute Stress Reaction: Fight | Gain +6 [img:str] while you have 5 or fewer HP. | `StatsAtLowHealth {<br>            threshold 5<br>            strength 6<br>        }` |
| ASRFlight | Acute Stress Reaction: Flight | Gain +6 [img:spd] while you have 5 or fewer HP. | `StatsAtLowHealth {<br>			threshold 5<br>            speed 6<br>        }` |
| BloodFrenzy | Blood Frenzy | When you kill a unit, take an extra turn with Madness. | `StatusOnKill {<br>            TakeBonusTurnWithStatus {<br>                Madness 1<br>            }<br>        }` |
| Shunned | Shunned | Take your turn last. Your heals heal for 2 less. +15% dodge chance. | `AddInitiative -100<br>        BoostHeals -2<br>        DodgeChance 15%` |
| Dysentery | Dysentery | 50% chance to make a burning poop directly behind you when you end your turn. | `//PoopOnTurnEnd 50%<br>        StatusEachTurnEnd {<br>            ForceUseAbility {<br>                chance .5<br>                ability DysenteryPoop<br>            }<br>        }` |
| Anxiety | Anxiety | +10% Dodge chance. When you take damage, run away from the source. | `DodgeChance 10%<br>        MoveWhenDamaged {<br>            weights stay_far_always_move<br>        }` |
| Kamikazee | Kamikaze | You explode when you are downed.  | `DeathRattle BoomerCatExplode` |
| Traumatophobia | Traumatophobia | Whenever you take damage, move 1 tile away from the source. | `MoveAwayFromDamageSource MoveOne` |
| StockholmSyndrome | Stockholm Syndrome | Whenever you take damage, move toward the source. | `MoveTowardsDamageSource {<br>            move_ability move<br>            move_far false<br>        }` |
| ViolentOutbursts | Violent Outbursts | When you end your turn, dash forward 2 tiles, attack with Knockback, and take 1 damage. | `AutocastEachTurn ViolentOutburst` |
| GamblingAddict | Gambling Addiction | +33% miss chance. 100% critical hit chance. | `MissChance 33<br>        CritChanceUp 100` |
| Scleroderma | Scleroderma | At the start of each battle, you lose all but 1 HP, but gain that much [img:shield]. | `Scleroderma 1` |
| Pacifist | Pacifist | You can't kill units. If you end your turn without using your basic attack gain 7 mana. | `AddStatusToAllDamage {<br>            NonLethal 1<br>        }<br>		<br>		StatusOnTurnEndIfDidntCastAbilityTypes {<br>			type attack<br>			ManaGain 7<br>		}` |
| Gigachad | GIGACHAD |  |  |
| ImposterSyndrome | Impostor Syndrome | You're quite suspicious… | `InvertBrainFaction 1` |
| Vegan | Vegan | You don't eat meat. | `Vegan 1<br>        HouseFoodRequirementMultiplier 0<br>        DisableAbilitiesWithTag meat<br>        BlacklistPickupType food` |
| FrozenKnee | The Zoomies | Your movement action is a dash attack. | `ReplaceBasicMove BasicDashAttackMove` |
| SchrodingerDisorder | Schrödinger's Syndrome | 50% chance to start each battle dead, or alive with max hp and All Stats Up 2 and an extra turn at the start of the battle. | `AllStatsUp 2<br>		AlphaTurns 1<br>        SchrodingerDisorder 50%` |
| ScalyScabs | Scaly Scabs |  |  |
| FattyLiver | Fatty Liver | Whenever you lose HP, you permanently lose 1 [img:con]. | `StatusOnTakeHealthDamage {<br>            PermanentConstitution -1<br>        }` |
| CommonCold | The Common Cold | Start each battle with All Stats Down. 30% chance of recovering at the end of each round. Contagious. | `AllStatsUp -1<br><br>        StatusOnBattleEnd {<br>            even_if_dead true<br>            CureDisease {<br>                chance 30%<br>                disease CommonCold<br>            }<br>        }<br><br>        DamageNeighborsOnEndMove {<br>            type status<br>            cant_miss true<br>            damage 0<br>            <br>            effects {<br>                SpreadDisease {<br>                    chance 50%<br>                    disease CommonCold<br>                    can_apply_to_anything true<br>                }<br>            }<br>        }<br><br>        AddStatusToBasicAttack {<br>            SpreadDisease {<br>                chance 50%<br>                disease CommonCold<br>                can_apply_to_anything true<br>            }<br>        }` |
| Pox | Pox | 10% chance to skip your turn to scratch yourself. Your basic attack has a 50% chance to inflict Poison 1. 5% chance of recovering at the end of each round. Contagious. | `AutocastEachTurnBegin {<br>            ability PoxScratch<br>            chance 10%<br>            advantage_polarity -1<br>        }<br><br>        StatusOnBattleEnd {<br>            even_if_dead true<br>            CureDisease {<br>                chance 5%<br>                disease Pox<br>            }<br>        }<br><br>        DamageNeighborsOnEndMove {<br>            type status<br>            cant_miss true<br>            damage 0<br>            <br>            effects {<br>                SpreadDisease {<br>                    chance 50%<br>                    disease Pox<br>                }<br>            }<br>        }<br><br>        AddStatusToBasicAttack {<br>            Poison [1 .5]<br>        }` |
| Psychosis | Psychosis | After your first turn, you have permanent madness. | `SetDefaultFacePassive insane<br>        StatusEachTurnEnd {<br>            PermanentMadness 1<br>        }<br>        StatusIfBattleAlreadyBegan {<br>            PermanentMadness 1<br>        }` |
| Necrosis | Necrosis | When you take damage, you get -1 [img:con], -1 [img:str], and spawn poisoned food. | `SpawnThingOnDamage {<br>            object PoisonFood<br>            consider_all_layers true<br>        }<br>        StatusOnTookDamage {<br>            StrengthUp -1<br>            ConstitutionUp -1<br>        }` |
| Touched | Touched | You can no longer heal HP. | `HPGainBlock 1` |
| Charred | Charred | Bruise 1. You cannot be Burned. | `StatusImmunity Burn<br>        Bruise 1` |
| Invincible | Immortal | All damage you take is reduced to 1. When you take damage, suffer a random injury. | `LimitDamage 1<br>        StatusOnTookDamage {<br>            RandomInjury 1<br>        }` |
| ExplosiveGas | Bad Gas | On the first round, take your turn last. At the start of that turn, do a Mega Fart attack that inflicts Poison 2.  | `AbilityOnBattleStart MegaFart<br>        TempInitiativeChange -999` |
| Toxoplasmosis | Toxoplasmosis | Start each battle with a Rat Familiar. Your basic attack charms Rat enemies. | `SpawnOnBattleStart {<br>            object CharmedRat<br>        }<br>        AddStatusToBasicAttack {<br>            Conditional_HasTag {<br>                tag rat<br>                Charmed 1<br>            }<br>            SpreadDisease {<br>                disease Toxoplasmosis<br>            }<br>        }` |
| Ebola | Ebola | Start each battle with Bleed 3. Your basic attack inflicts Bleed 2. 5% chance of recovering at the end of each round. Contagious. | `Bleed 3<br>        AddStatusToBasicAttack {<br>            Bleed 2<br>        }<br><br>        StatusOnBattleEnd {<br>            even_if_dead true<br>            CureDisease {<br>                chance 5%<br>                disease Ebola<br>            }<br>        }<br><br>        DamageNeighborsOnEndMove {<br>            type status<br>            cant_miss true<br>            damage 0<br>            <br>            effects {<br>                SpreadDisease {<br>                    chance 25%<br>                    disease Ebola<br>                    can_apply_to_anything true<br>                }<br>            }<br>        }<br>        MeleeRevengeDamage {<br>            effects {<br>                SpreadDisease {<br>                    chance 100%<br>                    disease Ebola<br>                    can_apply_to_anything true<br>                }<br>            }<br>        }` |
| Fidgety | Fidgety | When you end your turn, automatically use your weapon on a random unit in range, for free. | `StatusEachTurnEnd {<br>            UseAbility_Madness weapon<br>        }` |
| Narcolepsy | Narcolepsy | At the end of your turn, fall asleep, heal 10 HP and gain 7 mana. | `AddManaRegen 7<br>        StatusEachTurnEnd {<br>            ForceUseAbility Rest<br>        }` |
| Paranoia | Paranoia | When a unit ends its movement directly behind you, attack it and gain Fear.  | `Paranoia ParanoiaBasicMelee` |
| EatingDisorder | Eating Disorder | Double the effects of your consumables but you are confused on how to eat them. | `ConsumableEffectsMultiplierBonus 1<br>        ConfusionEffectOnTaggedAbilities consumable` |
| Gastritis | Gastritis | At the end of your turn, fart and Poison all adjacent units. | `StatusEachTurnEnd {<br>            ForceUseAbility MiniFart<br>        }` |
| Hypomania | Hypomania | Start each battle with 3 bonus turns, then never take a turn. | `Hypomania 3` |
| Hypersomnia | Hypersomnia | Start each battle asleep and with full health. | `StatusOnBattleStart {<br>            Sleep 1<br>        }<br>        FullHeal 1` |
| KidneyStones | Kidney Stone | When you end your turn take 1 damage and pass a kidney stone. | `StatusEachTurnEnd {<br>            ForceUseAbility KidneyStone<br>        }` |
| Cancer | Cancer | At the end of each battle, lose 3 random stats permanently and gain a random mutation. | `StatusOnBattleEnd {<br>            even_if_dead true<br>            <br>            RandomPermanentStat -3<br>            RandomMutation 1<br>        }` |
| Stinky | Stinky | Adjacent units move away from you at the start of their turns. | `StatusAdjacentOnTheirTurnBegin {<br>            ForceMoveAway {<br>                free false //consume the move point<br>            }<br>        }` |
| Incontinence | Incontinence | When you take damage, pee yourself. | `AbilityReaction PissYourself` |
| Fossilized | Fossilized | +2 Brace. Slide like a rock whenever you get hit. | `Brace 2<br>        SmallRockBehavior 5<br>        LimitSelfKnockbackDamage 1<br>        AddTag rock` |
| Triskaidekaphobia | Triskaidekaphobia | Your spells cost 0 mana. The 13th spell you cast on an adventure kills you and destroys your body. | `SetSpellCosts 0<br>        Triskaidekaphobia 13` |
| Autism | Autism | Spells you were born with cost -2 mana. Other spells cost +1 mana. | `Autism {<br>            innate -2<br>            learned 1<br>        }` |
| Tourettes | Tourette's Syndrome | At the start of your turn, you have a 33% chance to cast one of your spells at a random target for free. | `TourettesMeows {<br>            cooldown [8 15]<br>            pool [Hit Hiss Normal]<br>        }<br><br>        StatusEachTurnBegin {<br>            Conditional_GoodRoll {<br>                odds 33%<br>                UseRandomSpell_Madness 1<br>            }<br>        }` |
| Albinism | Albinism | Fire damage you take inflicts +3 Burn. Your basic attack has a 25% chance to inflict Fear. | `OverridePalette 87<br><br>        AddStatusToBasicAttack {<br>            Fear [1 .25]<br>        }<br>        AddStatusesToReceivedElementalDamage {<br>            elements [Heat Fire]<br>            Burn 3<br>        }<br>        AddStatusesIfPersistentWeatherElement {<br>            elements [Heat Fire]<br>            Burn 3<br>        }` |
| SleepParalysis | Sleep Paralysis | When you fall asleep, a Sleep Paralysis Demon with Madness spawns! You can't wake up until it's killed. Learn the spell Rest (if you have a free spell slot). | `ReceivedStatusReplacement [Sleep SleepParalysis]` |
| Diabetes | Diabetes | When you end your turn, if you haven't eaten food, gain All Stats Down and Confusion 1. Each time you eat food, cleanse all your debuffs and gain +1 [img:int]. | `Diabetes {<br>            AllStatsUp -1<br>            Confusion 1<br>        }<br>        StatusOnEatFood {<br>            Cleanse 0<br>			IntelligenceUp 1<br>        }` |
| Bipolar | Bipolar Disorder | Start each battle with either  +5 [img:int], +5 [img:cha], and +5 [img:spd] or  All Stats Down 2. | `RandomPassivePool {<br>            PassiveGroup {<br>                IntelligenceUp 5<br>                CharismaUp 5<br>                SpeedUp 5<br>                SetDefaultFace happy<br>            }<br>            PassiveGroup {<br>                AllStatsUp -2<br>                SetDefaultFace sad<br>            }<br>        }` |
| Soulless | Soulless | You are immune to buffs and debuffs. When you die, you don't leave a corpse. | `DebuffImmunity 1<br>        BuffImmunity 1<br>        AddCorpseHealth -999999` |
| Premonitions | The Shining | Your attacks can't miss. +15% dodge chance and +15% chance to gain Fear at the start of each turn. | `MaxAccuracy 1<br>        DodgeChance 15%<br>        StatusEachTurnBegin {<br>            Fear [1 .15]<br>        }` |
| PillPopper | Addict | Start each battle with All Stats Down 2. Gain All Stats Up 3 whenever you eat a pill. You have a 50% chance to find a pill at the end of each battle. | `AllStatsUp -2<br>        StatusOnBattleEnd {<br>            FindItemFromPool {<br>                chance .5<br>                pool pills<br>            }<br>        }<br>        StatusOnEatPill {<br>            AllStatsUp 3<br>        }` |
| BorrowedTime | Borrowed Time | +50% dodge chance. Doomed 3. | `DodgeChance 50%<br>        Doomed 3` |
| Brave | Brave | Take your turn earlier. Immune to Fear and Madness. Attacks against you never miss. | `AddInitiative 999<br>        StatusImmunity [Fear Madness PermanentMadness]<br>        CantDodge 1` |
| Scatological | Scatological | Heal 5 HP when you damage poop. At the start of your turn, if you're near poop, you automatically move toward it and eat it. | `MoveAndUseAbilityEachTurnBeginIfPossible EatShit<br>        AddStatusToAllDamage {<br>            Conditional_HasTag {<br>                tag poop<br>                FlatLeechIfDamaged 5<br>            }<br>        }` |
| Cannibal | Necrophage | At the start of your turn, if there's a dead body near you, move towards it and eat it to gain All Stats Up and heal 4 HP. | `MoveAndUseAbilityEachTurnBeginIfPossible Cannibalize` |
| CrohnsDisease | Crohn's Disease | At the end of your turn, you have a 20% chance to poop all over the place! | `StatusEachTurnEnd {<br>            ForceUseAbility {<br>                chance .2<br>                ability CrohnsPoop<br>            }<br>        }` |
| Pica | Pica | When you collect a coin or scrap pickup, heal instead of gaining the pickup's normal effect. | `TaggedPickupEffectReplacement {<br>            tag money<br><br>            HealthGain 3*X //3 health per coin<br>        }<br>        TaggedPickupEffectReplacement {<br>            tag scrap<br><br>            HealthGain 2*X //2 health per shield<br>        }` |
| FelineAids | Feline Aids | Your basic attack inflicts Poison 3 and Weakness 1. Inflict Poison 3 and Weakness 1 on units that contact you. Gain -1 [img:con] and -1 [img:spd] at the end of each battle permanently. | `AddStatusToBasicAttack {<br>            Poison 3<br>            Weakness 1<br><br>            SpreadDisease {<br>                chance 5%<br>                disease FelineAids<br>            }<br>        }<br>        MeleeRevengeDamage {<br>            Poison 3<br>            Weakness 1<br><br>            SpreadDisease {<br>                chance 5%<br>                disease FelineAids<br>            }<br>        }<br>        StatusOnBattleEnd {<br>            even_if_dead true<br>            <br>            PermanentConstitution -1<br>            PermanentSpeed -1<br>        }` |
| Dyslexia | Dyslexia | Swap 3's and 5's in the mana costs and damage values of your spells while in a battle. 6's and 9's are also swapped. | `Dyslexia [3 5]<br>        Dyslexia [6 9]` |
| Covid | Covid | Start each battle with All Stats Down, Poison 1, and Weakness 1. Your basic attack inflicts Poison 1 and Weakness 1. 15% chance of recovering at the end of each round. Contagious. | `AllStatsUp -1<br>        Poison 1<br>        Weakness 1<br><br>        StatusOnBattleEnd {<br>            even_if_dead true<br>            CureDisease {<br>                chance 15%<br>                disease Covid<br>                can_apply_to_anything true<br>            }<br>        }<br><br>        DamageNeighborsOnEndMove {<br>            type status<br>            cant_miss true<br>            damage 0<br>            <br>            effects {<br>                SpreadDisease {<br>                    chance 75%<br>                    disease Covid<br>                    can_apply_to_anything true<br>                }<br>            }<br>        }<br><br>        AddStatusToBasicAttack {<br>            Poison 1<br>            Weakness 1<br>        }` |
| Flu | The Flu | Start each battle with Slow 5 and Weakness 5. Your basic attack inflicts Slow 1 and Weakness 1. 20% chance of recovering at the end of each round. Contagious.  | `Slow 5<br>        Weakness 5<br><br>        StatusOnBattleEnd {<br>            even_if_dead true<br>            CureDisease {<br>                chance 20%<br>                disease Flu<br>            }<br>        }<br><br>        DamageNeighborsOnEndMove {<br>            type status<br>            cant_miss true<br>            damage 0<br>            <br>            effects {<br>                SpreadDisease {<br>                    chance 50%<br>                    disease Flu<br>                    can_apply_to_anything true<br>                }<br>            }<br>        }<br><br>        AddStatusToBasicAttack {<br>            Weakness 1<br>            Slow 1<br>        }` |
| BirdFlu | Bird Flu | Start each battle in Mockingbird Form. You have a 20% chance to recover at the end of each battle. Contagious. | `//AbilityOnBattleStart MockingbirdForm<br>        ForceUseAbility MockingbirdForm<br><br>        StatusOnBattleEnd {<br>            even_if_dead true<br>            CureDisease {<br>                chance 20%<br>                disease BirdFlu<br>            }<br>        }<br><br>        DamageNeighborsOnEndMove {<br>            type status<br>            cant_miss true<br>            damage 0<br>            <br>            effects {<br>                SpreadDisease {<br>                    chance 50%<br>                    disease BirdFlu<br>                }<br>            }<br>        }` |
| Nudist | Nudist | +50% dodge chance. You can't wear armor. | `DodgeChance 50%` |
| Elephantiasis | Elephantiasis | At the end of each battle, gain -1 [img:spd] and +2 starting [img:shield] permanently. After 8 battles, gain Trample. | `StatusOnBattleEnd {<br>            even_if_dead true<br>            PermanentSpeed -1<br>        }<br>        PassiveLevelUpAtCombatEnd 1<br><br>        PassiveLevelScaledStatus {<br>            Shield "2*(X-1)"<br>            SizeScalePercent "sqrt(1.0+(.05*(X-1)))*100"<br><br>            Trample [3, X-8] //if X is 11 then the chance here switches from 0 to 1<br>        }` |
| Gigantism | Gigantism | Trample. | `Trample 3<br>        SizeScale 1.3` |
| Dwarfism | Dwarfism | +10% dodge chance. | `DodgeChance 10%<br>        SizeScale .7` |
| PrimordialDwarf | Primordial Dwarf |  | `SizeScale .4` |
| Sociopathy | Sociopathy | You have Madness on your first turn. | `Madness 1` |
| SkillShare_Disorder | Munchausen by Proxy | If you have a 2nd disorder, all other cats in your party gain it at the start of each battle. | `//hard coded just like skill share` |
| Schizophrenia | Schizophrenia | At the end of your turn, spawn a hallucination. It has Madness, attacks any unit except you, and fades after its turn. | `StatusEachTurnEnd {<br>            ForceUseAbility Hallucinate_Disorder<br>        }` |
| Lycanthropy | Lycanthropy | 33% chance to enter Wolf Form at the start of your turn. | `StatusEachTurnBegin {<br>            ForceUseAbility {<br>                ability TigerForm<br>                chance 33%<br>            }<br>        }` |
| WobblyCat | Wobbly Cat Syndrome | 25% chance to block attacks and get knocked back 10 tiles instead. | `WobblyCat 25%` |
| Singleton | Singleton | Your max HP and mana are reduced to 1. Damage you take is reduced to 1. Your spells cost 1 mana. | `OverrideMaxHealth 1<br>        OverrideMaxMana 1<br>        StrictLimitDamage 1<br>        LimitHeal 1<br>        SetSpellCosts 1` |
| Insomnia | Insomnia | You can't fall asleep. You can move an extra time each turn. Exhaustion sets in on round 3. | `ExtraBasicMoves_Status 1<br>        StatusImmunity [Sleep SleepParalysis]<br>        ExhaustionRoundChange 3` |
| Phony | Phony | Start each battle with full mana. You can't regenerate mana. | `NoManaRegen 1<br>        MaxStartingMana 1` |
| AcidReflux | Acid Reflux | Your basic attack becomes a lobbed shot with splash damage but deals 2 damage to you. | `OverrideBasicAttack GerdShot` |
| SpontaneousCombustion | Spontaneous Combustion | When you take damage from an ability, you have a 15% chance to inflict Burn 5 on yourself and adjacent units. | `AbilityReaction {<br>            chance 15%<br>            ability_damage_only true<br>            ability SpontaneouslyCombust<br>        }` |
| TheHunger | The Hunger | Your basic attack has lifesteal. If you don't deal damage to a unit on your turn, gain Madness 1. | `AddStatusToBasicAttack {<br>            Leech 1<br>        }<br>        TheHunger {<br>            Madness 1<br>        }` |
| Paralyzed | Paraplegic | The range of all your movement, dash, and jump abilities are capped at 1 unless they teleport. Enemies won't prioritize attacking you. | `CapMovementAbilityRange 1<br>        ChangeTauntPriority -1<br>        MoveSpeedMultiplier .5` |
| GlassBones | Osteogenesis Imperfecta | +2 Bruise, +2 Bleed Thorns, and +2 Thorns. When you're downed, you get injured an extra time. | `BleedThorns 2<br>        Thorns 2<br>        Bruise 2<br>        ExtraInjuryOnDeath 1` |
| Gargantuan | Gargantuan | You are permanently immobile. | `SizeScale 1.65<br>        PermanentImmobile 1` |
| BrainDead | Brain Dead | Gain twice as many stats when you level up. +1 Reroll when leveling up. | `AddLevelUpRerolls 1<br>        AddLevelUpStatMultiplier 1` |
| TamperedGenes | Tainted Genes | At the end of each battle gain a random mutation. When you're downed, your corpse is destroyed. | `AddCorpseHealth -999999<br>        SpawnThingOnDeath ZombieCatFamiliar<br>        StatusOnBattleEnd {<br>            RandomMutation 1<br>        }` |
| SensoryOverloadFace | Sensory Overload | All but your face slot is locked. Your face item's effects are tripled! | `FaceArmorPassiveMultiplierBonus 2` |
| SensoryOverloadTrinket | Sensory Overload | All but your trinket slot is locked. Your trinket's effects are tripled!  | `TrinketPassiveMultiplierBonus 2<br>        TrinketActiveEffectsMultiplierBonus 2` |
| SensoryOverloadHead | Sensory Overload | All but your head slot is locked. Your head item's effects are tripled!  | `HeadArmorPassiveMultiplierBonus 2` |
| SensoryOverloadNeck | Sensory Overload | All but your neck slot is locked. Your neck item's effects are tripled!  | `NeckArmorPassiveMultiplierBonus 2` |
| SensoryOverloadWeapon | Sensory Overload | All but your weapon slot is locked. Your weapon's effects are tripled!  | `WeaponPassiveMultiplierBonus 2<br>        WeaponActiveEffectsMultiplierBonus 2` |
| EternalYouth | Eternal Youth | You are a kitten... forever! +1 [img:comfort], +1 [img:stimulation], +1 [img:appeal] | `PermanentKitten 1<br>        ChangeTauntPriority -1<br><br>        FurnitureStats {<br>            Comfort 1<br>            Stimulation 1<br>            Appeal 1<br>        }` |
| DejaVu | Deja Vu | 10% chance to cancel actions. [s:.7]Deja Vu will go away when this cat returns to the house.\[/s\] | `DejaVu 10%` |
| DownsSyndrome | Down's Syndrome |  |  |
| Tachysensia | Tachysensia |  |  |
| SavantSyndrome | Savant Syndrome |  |  |
| WilliamsSyndrome | Williams Syndrome | Your attacks may Charm. | `AddStatusToBasicAttack {<br>            Charmed [1 .25]<br>        }` |
| SpinaBifida | Spina Bifida |  |  |
| DarkOne | Dark One | At end of your turn, deal 1 damage to all units and heal for the damage dealt. Whenever you down an ally gain All Stats Up. | `AutocastEachTurn DarkOneStrike<br>        StatusKilledCharacters {<br>            Conditional_Ally {<br>                ApplyToSource {<br>                    AllStatsUp 1<br>                }<br>            }<br>        }` |
| ADHD | ADHD | You have 5 seconds to make decisions, or else this cat acts on its own. | `RealTimePressure_OneUnit 5` |
| FlamingFists | Flaming Fists | Your basic attacks inflict Burn 1. Start with Burn 1. | `Burn 1<br>        AddStatusToBasicAttack {<br>            Burn 1<br>        }` |
| IntestinalProlapse | Intestinal Prolapse | You receive double damage from behind. | `BackstabWeakness 0.75` |
| BlessingOfGlorg | Blessing of Glorg | You can unequip cursed items. | `CanRemoveCursedItems 1` |
| BlackFetin | Black Fetin | You have a 10% to be AI controlled each turn. When an ally cat is downed, restore all your mana.  | `StatusOnAllyCatDeath {<br>			FillMana 1<br>		}<br>        StatusEachTurnBegin {<br>            Conditional_BadRoll {<br>                odds .1<br><br>                Temporary {<br>                    status Uncontrollable<br>                    stacks 1<br>                    turns 1<br>                    expires_on_end_turn true<br>                }<br>            }<br>        }` |
| OrangeFetin | Orange Fetin | You have a 10% to be AI controlled each turn. When you kill an enemy, gain 3 mana and heal 2 hp. | `StatusOnKillEnemy {<br>			ManaGain 3<br>			HealthGain 2<br>		}<br>		StatusEachTurnBegin {<br>            Conditional_BadRoll {<br>                odds .1<br><br>                Temporary {<br>                    status Uncontrollable<br>                    stacks 1<br>                    turns 1<br>                    expires_on_end_turn true<br>                }<br>            }<br>        }` |
| PurpleFetin | Purple Fetin | You have a 10% to be AI controlled each turn. You can reroll your level up options 3 times. | `AddLevelUpRerolls 3<br>        StatusEachTurnBegin {<br>            Conditional_BadRoll {<br>                odds .1<br><br>                Temporary {<br>                    status Uncontrollable<br>                    stacks 1<br>                    turns 1<br>                    expires_on_end_turn true<br>                }<br>            }<br>        }` |
| Chungus | Chungus |  |  |

---

### 6. Master Injuries Database

| Internal ID | Name | Stats Penalty |
| :--- | :--- | :--- |
| str | Broken Paw | str -1 |
| dex | Torn Tendon | dex -1 |
| con | Broken Rib | con -1 |
| int | Concussion | int -1 |
| cha | Disfigured | cha -1 |
| spd | Broken Leg | spd -1 |
| lck | Jinxed | lck -1 |
| burned | Immolated | cha -1 |
| bleeding | Exsanguinated | str -1 |
| poisoned | Poisoned | con -1 |
| cursed | Cursed | lck -2 |
| radiated | Radiated | con -1 |
| fade |  |  |