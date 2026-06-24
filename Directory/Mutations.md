# Mutations Directory

## Body Mutations

### `300`
**Name:** Rock Bod  
**Source:** `body.gon`  

```
300 { //Rock Bod
        con 1
    }
```

---

### `301`
**Name:** Cactus Bod  
**Description:** +1 Thorns.  
**Source:** `body.gon`  

```
301 { //Cactus Bod
        desc "MUTATION_BODY_301_DESC"
        passives {
            Thorns 1
        }
    }
```

---

### `302`
**Name:** Turtle Bod  
**Source:** `body.gon`  

```
302 { //Turtle Bod
        tag animal
        spd -1
        shield 5
    }
```

---

### `303`
**Name:** Snail Bod  
**Source:** `body.gon`  

```
303 { //Snail Bod
        tag animal
        shield 10
        spd -2
    }
```

---

### `304`
**Name:** Robot Body  
**Source:** `body.gon`  

```
304 { //Robot Body
        spd 1
        int 1
    }
```

---

### `305`
**Name:** Conjoined Bod  
**Source:** `body.gon`  

```
305 { //Conjoined Bod
        lck 1
    }
```

---

### `306`
**Name:** Skin & Bones  
**Source:** `body.gon`  

```
306 { //Skin & Bones
        shield 12
        con -3
    }
```

---

### `307`
**Name:** Udders  
**Source:** `body.gon`  

```
307 { //Udders
        tag animal
        cha 1
    }
```

---

### `308`
**Name:** Beach Bod  
**Source:** `body.gon`  

```
308 { //Beach Bod
        str 1
        con 1
        int -1
    }
```

---

### `309`
**Name:** Maggot Bod  
**Description:** Units that contact you get knocked back 2 tiles.  
**Source:** `body.gon`  

```
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
```

---

### `310`
**Name:** Puffball Bod  
**Source:** `body.gon`  

```
310 { //Puffball Bod
        cha 1
    }
```

---

### `311`
**Name:** Square Bod  
**Source:** `body.gon`  

```
311 { //Square Bod
        con 1
    }
```

---

### `312`
**Name:** Money Bag Bod  
**Description:** Spawn a coin when you take damage.  
**Source:** `body.gon`  

```
312 { //Money Bag Bod
        desc "MUTATION_BODY_312_DESC"
        passives {
            SpawnThingOnDamage {
                object Coin
                chance 100%
            }
        }
    }
```

---

### `313`
**Name:** Spike Bod  
**Description:** +1 Kinetic Spikes.  
**Source:** `body.gon`  

```
313 { //Spike Bod
        desc "MUTATION_BODY_313_DESC"
        passives {
            KineticSpikes 1
        }
    }
```

---

### `314`
**Name:** Porcupine  
**Description:** +2 Thorns.  
**Source:** `body.gon`  

```
314 { //Porcupine
        desc "MUTATION_BODY_314_DESC"
        cha -1
        passives {   
            Thorns 2 
        }
    }
```

---

### `315`
**Name:** Carapace  
**Description:** +1 Brace.  
**Source:** `body.gon`  

```
315 { //Carapace
        desc "MUTATION_BODY_315_DESC"
        passives {
            Brace 1
        }
    }
```

---

### `316`
**Name:** Pangolin  
**Source:** `body.gon`  

```
316 { //Pangolin
        shield 2
    }
```

---

### `317`
**Name:** Camel Hump  
**Description:** Immune to Heat Wave weather.  
**Source:** `body.gon`  

```
317 { //Camel Hump
        desc "MUTATION_BODY_317_DESC"
        con 1
        passives {
		    DrinkWater 1
        }
    }
```

---

### `318`
**Name:** Egg Sack Back  
**Description:** 25% chance to spawn a Charmed Fly each turn.  
**Source:** `body.gon`  

```
318 { //Egg Sack Back
         desc "MUTATION_BODY_318_DESC" 

        passives { 
            SpawnEachTurn {
                object CharmedFly
                chance 25% 
            } 
        }
    }
```

---

### `319`
**Name:** Fractured Bod  
**Description:** When you take damage from an attack, gain a random buff.  
**Source:** `body.gon`  

```
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
```

---

### `320`
**Name:** Brick Bod  
**Source:** `body.gon`  

```
320 { //Brick Bod
        shield 1
    }
```

---

### `321`
**Name:** Kitten Bod  
**Description:** Spawn a Charmed Kitten familiar when you get downed.  
**Source:** `body.gon`  

```
321 { //Kitten Bod
        desc "MUTATION_BODY_321_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }
```

---

### `322`
**Name:** Backpack  
**Description:** Gain an extra consumable item at the end of each battle.  
**Source:** `body.gon`  

```
322 { //Backpack
        desc "MUTATION_BODY_322_DESC"
        passives {
            StatusOnBattleEnd {
                FindItemFromPool consumables
            }
        }
    }
```

---

### `323`
**Name:** Fatty  
**Description:** Trample. When damaged, move 1 tile in a random direction.  
**Source:** `body.gon`  

```
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
```

---

### `324`
**Name:** Eyeball  
**Description:** Gain +1 range when you get a kill.  
**Source:** `body.gon`  

```
324 { //Eyeball
        desc "MUTATION_BODY_324_DESC"
        passives {
            StatusOnKill {
                RangeUp 1
            }
        }
    }
```

---

### `750`
**Name:** spike body  
**Description:** +1 Thorns.  
**Source:** `body.gon`  

```
750 { //spike body
        desc "MUTATION_BODY_750_DESC" 
        passives {        
            Thorns 1 
        } 
    }
```

---

### `753`
**Name:** mermaid body  
**Source:** `body.gon`  

```
753 { //mermaid body
		shield 5
    }
```

---

### `758`
**Name:** human head body  
**Description:** Start with +1 Bonus Attack.  
**Source:** `body.gon`  

```
758 { //human head body
		desc "MUTATION_BODY_758_DESC" 
		con 1
		passives {
			Quivered 1
		}
    }
```

---

### `900`
**Name:** slender  
**Source:** `body.gon`  

```
900 { //slender
        con -2
        spd 1
    }
```

---

### `400`
**Source:** `body.gon`  

```
400 {
        tag common
        str 2
        con -1
    }
```

---

### `401`
**Source:** `body.gon`  

```
401 {
        tag common
        str 2
        dex -1
    }
```

---

### `402`
**Source:** `body.gon`  

```
402 {
        tag common
        str 2
        cha -1
    }
```

---

### `403`
**Source:** `body.gon`  

```
403 {
        tag common
        str 2
        int -1
    }
```

---

### `404`
**Source:** `body.gon`  

```
404 {
        tag common
        str 2
        spd -1
    }
```

---

### `405`
**Source:** `body.gon`  

```
405 {
        tag common
        str 2
        lck -1
    }
```

---

### `406`
**Source:** `body.gon`  

```
406 {
        tag common
        con 2
        str -1
    }
```

---

### `407`
**Source:** `body.gon`  

```
407 {
        tag common
        con 2
        dex -1
    }
```

---

### `408`
**Source:** `body.gon`  

```
408 {
        tag common
        con 2
        cha -1
    }
```

---

### `409`
**Source:** `body.gon`  

```
409 {
        tag common
        con 2
        int -1
    }
```

---

### `410`
**Source:** `body.gon`  

```
410 {
        tag common
        con 2
        spd -1
    }
```

---

### `411`
**Source:** `body.gon`  

```
411 {
        tag common
        con 2
        lck -1
    }
```

---

### `412`
**Source:** `body.gon`  

```
412 {
        tag common
        dex 2
        con -1
    }
```

---

### `413`
**Source:** `body.gon`  

```
413 {
        tag common
        dex 2
        str -1
    }
```

---

### `414`
**Source:** `body.gon`  

```
414 {
        tag common
        dex 2
        cha -1
    }
```

---

### `415`
**Source:** `body.gon`  

```
415 {
        tag common
        dex 2
        int -1
    }
```

---

### `416`
**Source:** `body.gon`  

```
416 {
        tag common
        dex 2
        spd -1
    }
```

---

### `417`
**Source:** `body.gon`  

```
417 {
        tag common
        dex 2
        lck -1
    }
```

---

### `418`
**Source:** `body.gon`  

```
418 {
        tag common
        int 2
        con -1
    }
```

---

### `419`
**Source:** `body.gon`  

```
419 {
        tag common
        int 2
        dex -1
    }
```

---

### `420`
**Source:** `body.gon`  

```
420 {
        tag common
        int 2
        cha -1
    }
```

---

### `421`
**Source:** `body.gon`  

```
421 {
        tag common
        int 2
        str -1
    }
```

---

### `422`
**Source:** `body.gon`  

```
422 {
        tag common
        int 2
        spd -1
    }
```

---

### `423`
**Source:** `body.gon`  

```
423 {
        tag common
        int 2
        lck -1
    }
```

---

### `424`
**Source:** `body.gon`  

```
424 {
        tag common
        cha 2
        con -1
    }
```

---

### `425`
**Source:** `body.gon`  

```
425 {
        tag common
        cha 2
        dex -1
    }
```

---

### `426`
**Source:** `body.gon`  

```
426 {
        tag common
        cha 2
        str -1
    }
```

---

### `427`
**Source:** `body.gon`  

```
427 {
        tag common
        cha 2
        int -1
    }
```

---

### `428`
**Source:** `body.gon`  

```
428 {
        tag common
        cha 2
        spd -1
    }
```

---

### `429`
**Source:** `body.gon`  

```
429 {
        tag common
        cha 2
        lck -1
    }
```

---

### `430`
**Source:** `body.gon`  

```
430 {
        tag common
        lck 2
        con -1
    }
```

---

### `431`
**Source:** `body.gon`  

```
431 {
        tag common
        lck 2
        dex -1
    }
```

---

### `432`
**Source:** `body.gon`  

```
432 {
        tag common
        lck 2
        cha -1
    }
```

---

### `433`
**Source:** `body.gon`  

```
433 {
        tag common
        lck 2
        int -1
    }
```

---

### `434`
**Source:** `body.gon`  

```
434 {
        tag common
        lck 2
        spd -1
    }
```

---

### `435`
**Source:** `body.gon`  

```
435 {
        tag common
        lck 2
        str -1
    }
```

---

### `436`
**Source:** `body.gon`  

```
436 {
        tag common
        spd 2
        con -1
    }
```

---

### `437`
**Source:** `body.gon`  

```
437 {
        tag common
        spd 2
        str -1
    }
```

---

### `438`
**Source:** `body.gon`  

```
438 {
        tag common
        spd 2
        cha -1
    }
```

---

### `439`
**Source:** `body.gon`  

```
439 {
        tag common
        spd 2
        int -1
    }
```

---

### `440`
**Source:** `body.gon`  

```
440 {
        tag common
        spd 2
        dex -1
    }
```

---

### `441`
**Source:** `body.gon`  

```
441 {
        tag common
        spd 2
        lck -1
    }
```

---

### `442`
**Source:** `body.gon`  

```
442 {
        tag melted
        cha -1
    }
```

---

### `700`
**Name:** Gastroschisis  
**Source:** `body.gon`  

```
700 { //Gastroschisis
        tag birth_defect
        con -2
    }
```

---

### `701`
**Name:** Deformed Ribcage  
**Source:** `body.gon`  

```
701 { //Deformed Ribcage
        tag birth_defect
        spd -2
    }
```

---

### `702`
**Name:** Malnurished  
**Source:** `body.gon`  

```
702 { //Malnurished
        tag birth_defect
        con -1
    }
```

---

### `703`
**Name:** Body Welts  
**Description:** Start each battle with Bruise 1.  
**Source:** `body.gon`  

```
703 { //Body Welts
        desc "MUTATION_BODY_703_DESC"
        tag birth_defect

        passives {
            Bruise 1
        }
    }
```

---

### `704`
**Name:** Conjoined Body  
**Source:** `body.gon`  

```
704 { //Conjoined Body
        tag birth_defect
        spd -3
		con 2
    }
```

---

## Ears Mutations

### `300`
**Name:** horn  
**Source:** `ears.gon`  

```
300 { //horn
        tag animal
        str 1 //designed as: +1 melee damage
    }
```

---

### `301`
**Name:** antenna  
**Source:** `ears.gon`  

```
301 { //antenna
        tag animal
        int 1 //designed as +1 mana regen
    }
```

---

### `302`
**Name:** fishy  
**Description:** +1 Health and Mana Regeneration while wet.  
**Source:** `ears.gon`  

```
302 { //fishy
        tag animal
        desc "MUTATION_EARS_302_DESC"

        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    HealthRegenUp 1
                    AddManaRegen 1
                }
            }
        }
    }
```

---

### `303`
**Name:** bullhorn  
**Description:** Adds +1 Knockback to your basic attack if it's melee.  
**Source:** `ears.gon`  

```
303 { //bullhorn
        tag animal
        desc "MUTATION_EARS_303_DESC"

        str 1
        passives {
            AddStatusToBasicMeleeAttack {
                Knockback 1
            }
        }
    }
```

---

### `304`
**Name:** pigtails  
**Source:** `ears.gon`  

```
304 { //pigtails
        cha 1
    }
```

---

### `305`
**Name:** boil  
**Source:** `ears.gon`  

```
305 { //boil
        shield 1
    }
```

---

### `306`
**Name:** bunny ear  
**Source:** `ears.gon`  

```
306 { //bunny ear
        tag animal
        spd 1
    }
```

---

### `307`
**Name:** brains  
**Source:** `ears.gon`  

```
307 { //brains
        int 1
    }
```

---

### `308`
**Name:** shrek  
**Source:** `ears.gon`  

```
308 { //shrek
        str 1
        cha -1
    }
```

---

### `309`
**Name:** antlers  
**Description:** Adds +1 Bleed to your basic attack.  
**Source:** `ears.gon`  

```
309 { //antlers
        tag animal
        desc "MUTATION_EARS_309_DESC"

        passives {
            AddStatusToBasicAttack {
                Bleed 1
            }
        }
    }
```

---

### `310`
**Name:** human  
**Source:** `ears.gon`  

```
310 { //human
        int 1
    }
```

---

### `311`
**Name:** TODO(no effect or comment here???)  
**Source:** `ears.gon`  

```
311 { //TODO(no effect or comment here???)
    //
    //}
```

---

### `313`
**Name:** Ram horns  
**Description:** Adds +1 Knockback to your basic attack if it's melee.  
**Source:** `ears.gon`  

```
313 { //Ram horns
        tag animal
        desc "MUTATION_EARS_313_DESC"

        shield 1
        passives {
            AddStatusToBasicMeleeAttack {
                Knockback 1
            }
        }
    }
```

---

### `314`
**Name:** Deer horns  
**Description:** Thorns 1. Your basic attack inflicts Bleed if it's melee.  
**Source:** `ears.gon`  

```
314 { //Deer horns
        tag animal
        desc "MUTATION_EARS_314_DESC"
        passives {
            Thorns 1
            AddStatusToBasicMeleeAttack {
                Bleed 1 
            }
        }
    }
```

---

### `315`
**Name:** Fly Ears  
**Description:** 50% chance to spawn a Charmed Fly each turn. Start with Poison 1.  
**Source:** `ears.gon`  

```
315 { //Fly Ears
        tag animal
        desc "MUTATION_EARS_315_DESC" 

        passives { 
            SpawnEachTurn {
                object CharmedFly
                good false //good relative to the thing attacking, for luck calculations
                chance 50% 
            }
            
            // damage 1 per turn
            Poison 1
        }
    }
```

---

### `316`
**Name:** Bat Ears  
**Description:** You can see hidden things. 5% dodge chance.  
**Source:** `ears.gon`  

```
316 { //Bat Ears
        tag animal
        desc "MUTATION_EARS_316_DESC"

        passives {
            ShowHiddenThings 1
            DodgeChance 5%
        }
    }
```

---

### `317`
**Name:** Bone Ears  
**Description:** Whenever you down a unit, you have a 10% chance to reanimate that unit with 50% HP.  
**Source:** `ears.gon`  

```
317 { // Bone Ears
        desc "MUTATION_EARS_317_DESC"

        passives { 
            StatusKilledCharacters {
                Conditional_RandomChance {
                    odds 10%
                    AutoReanimate 50%
                }
            } 
        }
    }
```

---

### `318`
**Name:** Frog Eyes  
**Description:** You have Brace 1 while wet.  
**Source:** `ears.gon`  

```
318 { // Frog Eyes
        tag animal
        desc "MUTATION_EARS_318_DESC"

        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    Brace 1
                }
            } 
        }
    }
```

---

### `319`
**Name:** Pierced Ears  
**Description:** Gain +1 Charge when you take damage.  
**Source:** `ears.gon`  

```
319 { // Pierced Ears
        tag animal
        desc "MUTATION_EARS_319_DESC"

        passives {
            StatusOnTookDamage {
                Charge 1
            }
        }
    }
```

---

### `320`
**Name:** Alien Ears  
**Description:** +1 Kinetic Spikes.  
**Source:** `ears.gon`  

```
320 { // Alien Ears
        desc "MUTATION_EARS_320_DESC"

        passives {
            KineticSpikes 1 
        }
    }
```

---

### `321`
**Name:** Spring Ears  
**Description:** Units that contact you get knocked back 1 tile.  
**Source:** `ears.gon`  

```
321 { // Spring Ears
        desc "MUTATION_EARS_321_DESC"

        passives {
            MeleeRevengeDamage {
                knockback 1
            }
        }
    }
```

---

### `322`
**Name:** Lamb Ears  
**Source:** `ears.gon`  

```
322 { // Lamb Ears 
        tag animal
        cha 1 
    }
```

---

### `323`
**Name:** Vamp Ears  
**Description:** Gain 1 HP when your basic attack deals damage.  
**Source:** `ears.gon`  

```
323 { // Vamp Ears
        desc "MUTATION_EARS_323_DESC"

        passives {
            AddStatusToBasicAttack {
                FlatLeech 1
            } 
        }
    }
```

---

### `324`
**Name:** Extra Paw  
**Description:** 10% chance of counter attack when hit  
**Source:** `ears.gon`  

```
324 { // Extra Paw
    //     desc "10% chance of counter attack when hit"
    //     tag extra
    //
    //     passives {   
    //         CounterAttack { 
    //             chance 10%
    //         }
    //     }
    // }
```

---

### `325`
**Name:** Tree Branch  
**Description:** If you're wet, gain +1 Charge and +1 [img:shield] at the end of your turn.  
**Source:** `ears.gon`  

```
325 { // Tree Branch
        desc "MUTATION_EARS_325_DESC"

        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    StatusEachTurnEnd {
                        Shield 1
                        Charge 1
                    }
                } 
            } 
        }
    }
```

---

### `326`
**Name:** Worm Ear  
**Description:** 5% chance to spawn a Maggot familiar each turn.  
**Source:** `ears.gon`  

```
326 { // Worm Ear
        desc "MUTATION_EARS_326_DESC"

        passives {
            SpawnEachTurn {
                chance 5%
                object  CharmedMaggot
            } 
        }
    }
```

---

### `327`
**Name:** Ant Antenna  
**Description:** An extra food pickup will spawn in each battle.  
**Source:** `ears.gon`  

```
327 { // Ant Antenna
        tag animal
        desc "MUTATION_EARS_327_DESC"
            passives {
                SpawnOnBattleStartRandomEmptyTile {
                    object RandomFoodPickup 
                }
            } 
    }
```

---

### `328`
**Name:** Snake Ears  
**Description:** 5% chance to Petrify on damage and when hit.  
**Source:** `ears.gon`  

```
328 { // Snake Ears
        tag animal
        desc "MUTATION_EARS_328_DESC"
            
        passives {
            AddStatusToBasicAttack {
                Petrify [1, .05]
            } 
            RevengeDamage {
                effects {
                    Petrify [1, .05]
                } 
            }
        }
    }
```

---

### `329`
**Name:** External Gills  
**Description:** Your basic attack leaves water tiles.  
**Source:** `ears.gon`  

```
329 { // External Gills
        tag animal
        desc "MUTATION_EARS_329_DESC" 
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        }  

    }
```

---

### `330`
**Name:** Hook Ears  
**Description:** Thorns 1. 10% chance to inflict Immobile on units that contact you.  
**Source:** `ears.gon`  

```
330 { // Hook Ears
        desc "MUTATION_EARS_330_DESC"
        passives {
            Thorns 1
            MeleeRevengeDamage {
                Immobile 10%
            }
        }
    }
```

---

### `331`
**Name:** Mace Ears  
**Description:** Your basic attack has +1 Knockback.  
**Source:** `ears.gon`  

```
331 { // Mace Ears
        desc "MUTATION_EARS_331_DESC"
        passives {
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }
```

---

### `332`
**Name:** Blubber Lobes  
**Description:** Brace 1.  
**Source:** `ears.gon`  

```
332 { // Blubber Lobes
        desc "MUTATION_EARS_332_DESC"
        passives {
            Brace 1
        }
    }
```

---

### `333`
**Name:** Metal Plate  
**Source:** `ears.gon`  

```
333 { // Metal Plate
        shield 3 
    }
```

---

### `334`
**Name:** Metal Detector  
**Description:** Spawn 1-3 more coins/scrap around the map on random tiles at the start of each battle.  
**Source:** `ears.gon`  

```
334 { // Metal Detector
        desc "MUTATION_EARS_334_DESC"
        passives {
            SpawnOnBattleStartRandomEmptyTile {
                object Coin
                number [1 3]
            }
        }
    }
```

---

### `335`
**Name:** Docked Ears  
**Description:** Start with Bleed 1 and a bonus attack.  
**Source:** `ears.gon`  

```
335 { // Docked Ears
        desc "MUTATION_EARS_335_DESC"
        passives { 
            Bleed 1 
            Quivered 1
        }
    }
```

---

### `336`
**Name:** Large Leaves  
**Description:** You gain 3 mana at the end of your turn if you didn't use your movement action.  
**Source:** `ears.gon`  

```
336 { // Large Leaves
        desc "MUTATION_EARS_336_DESC"
        passives {
            StatusIfUnusedMovePoints {
                ManaGain 3 
            } 
        }
    }
```

---

### `337`
**Name:** Burning ears  
**Description:** Your basic attack inflicts Burn 1.  
**Source:** `ears.gon`  

```
337 { // Burning ears
        desc "MUTATION_EARS_337_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 1
            }
        }
    }
```

---

### `338`
**Name:** Frozen ears  
**Description:** Your basic attack has a 15% chance to inflict Freeze.  
**Source:** `ears.gon`  

```
338 { // Frozen ears
        desc "MUTATION_EARS_338_DESC"
        passives {
            MeleeRevengeDamage {
                Freeze [1 0.15]
            }
        }
    }
```

---

### `339`
**Name:** Lightning Rods  
**Description:** You have electric immunity.  
**Source:** `ears.gon`  

```
339 { // Lightning Rods
        desc "MUTATION_EARS_339_DESC"
        passives { 
            ElementImmune Electric
        }
    }
```

---

### `340`
**Name:** Aura Ears  
**Source:** `ears.gon`  

```
340 { // Aura Ears
        divine_shield 1
    }
```

---

### `341`
**Name:** Large Ears  
**Description:** 10% chance to backflip when targeted.  
**Source:** `ears.gon`  

```
341 { //Large Ears 
        desc "MUTATION_EARS_341_DESC" 
        passives {
            ChanceToBackflip {
                ability BackflipDodge
                chance 10%
            } 
        }
    }
```

---

### `342`
**Name:** Infested Ears  
**Description:** 20% chance to spawn a Charmed Flea when damaged.  
**Source:** `ears.gon`  

```
342 { //Infested Ears 
        desc "MUTATION_EARS_342_DESC" 
        con -1
        passives {
            SpawnThingOnDamage {
                object CharmedFlea
                good false //good relative to the thing attacking, for luck calculations
                chance 20%
            }
        }
    }
```

---

### `343`
**Name:** Long Antlers  
**Description:** Thorns 1.  
**Source:** `ears.gon`  

```
343 { //Long Antlers
        tag animal
        desc "MUTATION_EARS_343_DESC" 
        passives {        
            Thorns 1 
        } 
    }
```

---

### `344`
**Name:** Kitten  
**Description:** Spawn a Charmed Kitten familiar when you get downed.  
**Source:** `ears.gon`  

```
344 { //Kitten
        desc "MUTATION_EARS_344_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }
```

---

### `345`
**Name:** Mouse Ears  
**Description:** Units that contact or attack you have a 15% chance to get Charmed.  
**Source:** `ears.gon`  

```
345 { //Mouse Ears
        tag animal
        desc "MUTATION_EARS_345_DESC"  

        passives {
            RevengeDamage {
                effects {
                    Charmed [1, .15]           
                } 
            }
        }
    }
```

---

### `750`
**Name:** Jackrabbit Ears  
**Description:** Your movement action is a jump.  
**Source:** `ears.gon`  

```
750 { //Jackrabbit Ears
        tag animal
        desc "MUTATION_EARS_750_DESC"  

        passives {
            ReplaceBasicMove_Mutation BasicJump
        }
    }
```

---

### `751`
**Name:** Folded Ears  
**Description:** +10% dodge chance.  
**Source:** `ears.gon`  

```
751 { // Folded Ears
        desc "MUTATION_EARS_751_DESC" 
        passives {
            DodgeChance 10%
        }
    }
```

---

### `752`
**Name:** Fin Ears  
**Description:** You have +2 Damage while wet.  
**Source:** `ears.gon`  

```
752 { // Fin Ears
        tag animal
        desc "MUTATION_EARS_752_DESC" 
        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    DamageUp 2 
                }
            } 
        }
    }
```

---

### `753`
**Name:** Goat Horns  
**Description:** +1 Knockback damage. Your basic attack has +1 Knockback.  
**Source:** `ears.gon`  

```
753 { // Goat Horns
        tag animal
        desc "MUTATION_EARS_753_DESC" 
        passives { 
            AddKnockbackDamage 1
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }
```

---

### `754`
**Name:** Electric Ears  
**Description:** Electric damage you deal is increased by 1.  
**Source:** `ears.gon`  

```
754 { // Electric Ears
        desc "MUTATION_EARS_754_DESC" 
        spd 1 
        passives {
            AddDamageToElementDamage {
                element Electric
                damage 1
            } 
        }
    }
```

---

### `755`
**Name:** Head Ferns  
**Description:** Gain +1 Charge every time you cast a spell.  
**Source:** `ears.gon`  

```
755 { // Head Ferns
        desc "MUTATION_EARS_755_DESC" 
        passives { 
            StatusOnCastSpell {
                Charge 1
            }   
        }
    }
```

---

### `900`
**Name:** slender  
**Description:** +10% dodge chance.  
**Source:** `ears.gon`  

```
900 { //slender
        desc "MUTATION_EARS_900_DESC"

        passives {
            DodgeChance 10%
        }
    }
```

---

### `1500`
**Name:** rat ears  
**Description:** +2% dodge chance  
**Source:** `ears.gon`  

```
1500 { //rat ears
        tag animal
        desc "MUTATION_EARS_1500_DESC"

        passives {
            DodgeChance 2%
        }
    }
```

---

### `400`
**Source:** `ears.gon`  

```
400 {
        tag common
        str 2
        con -1
    }
```

---

### `401`
**Source:** `ears.gon`  

```
401 {
        tag common
        str 2
        dex -1
    }
```

---

### `402`
**Source:** `ears.gon`  

```
402 {
        tag common
        str 2
        cha -1
    }
```

---

### `403`
**Source:** `ears.gon`  

```
403 {
        tag common
        str 2
        int -1
    }
```

---

### `404`
**Source:** `ears.gon`  

```
404 {
        tag common
        str 2
        spd -1
    }
```

---

### `405`
**Source:** `ears.gon`  

```
405 {
        tag common
        str 2
        lck -1
    }
```

---

### `406`
**Source:** `ears.gon`  

```
406 {
        tag common
        con 2
        str -1
    }
```

---

### `407`
**Source:** `ears.gon`  

```
407 {
        tag common
        con 2
        dex -1
    }
```

---

### `408`
**Source:** `ears.gon`  

```
408 {
        tag common
        con 2
        cha -1
    }
```

---

### `409`
**Source:** `ears.gon`  

```
409 {
        tag common
        con 2
        int -1
    }
```

---

### `410`
**Source:** `ears.gon`  

```
410 {
        tag common
        con 2
        spd -1
    }
```

---

### `411`
**Source:** `ears.gon`  

```
411 {
        tag common
        con 2
        lck -1
    }
```

---

### `412`
**Source:** `ears.gon`  

```
412 {
        tag common
        dex 2
        con -1
    }
```

---

### `413`
**Source:** `ears.gon`  

```
413 {
        tag common
        dex 2
        str -1
    }
```

---

### `414`
**Source:** `ears.gon`  

```
414 {
        tag common
        dex 2
        cha -1
    }
```

---

### `415`
**Source:** `ears.gon`  

```
415 {
        tag common
        dex 2
        int -1
    }
```

---

### `416`
**Source:** `ears.gon`  

```
416 {
        tag common
        dex 2
        spd -1
    }
```

---

### `417`
**Source:** `ears.gon`  

```
417 {
        tag common
        dex 2
        lck -1
    }
```

---

### `418`
**Source:** `ears.gon`  

```
418 {
        tag common
        int 2
        con -1
    }
```

---

### `419`
**Source:** `ears.gon`  

```
419 {
        tag common
        int 2
        dex -1
    }
```

---

### `420`
**Source:** `ears.gon`  

```
420 {
        tag common
        int 2
        cha -1
    }
```

---

### `421`
**Source:** `ears.gon`  

```
421 {
        tag common
        int 2
        str -1
    }
```

---

### `422`
**Source:** `ears.gon`  

```
422 {
        tag common
        int 2
        spd -1
    }
```

---

### `423`
**Source:** `ears.gon`  

```
423 {
        tag common
        int 2
        lck -1
    }
```

---

### `424`
**Source:** `ears.gon`  

```
424 {
        tag common
        cha 2
        con -1
    }
```

---

### `425`
**Source:** `ears.gon`  

```
425 {
        tag common
        cha 2
        dex -1
    }
```

---

### `426`
**Source:** `ears.gon`  

```
426 {
        tag common
        cha 2
        str -1
    }
```

---

### `427`
**Source:** `ears.gon`  

```
427 {
        tag common
        cha 2
        int -1
    }
```

---

### `428`
**Source:** `ears.gon`  

```
428 {
        tag common
        cha 2
        spd -1
    }
```

---

### `429`
**Source:** `ears.gon`  

```
429 {
        tag common
        cha 2
        lck -1
    }
```

---

### `430`
**Source:** `ears.gon`  

```
430 {
        tag common
        lck 2
        con -1
    }
```

---

### `431`
**Source:** `ears.gon`  

```
431 {
        tag common
        lck 2
        dex -1
    }
```

---

### `432`
**Source:** `ears.gon`  

```
432 {
        tag common
        lck 2
        cha -1
    }
```

---

### `433`
**Source:** `ears.gon`  

```
433 {
        tag common
        lck 2
        int -1
    }
```

---

### `434`
**Source:** `ears.gon`  

```
434 {
        tag common
        lck 2
        spd -1
    }
```

---

### `435`
**Source:** `ears.gon`  

```
435 {
        tag common
        lck 2
        str -1
    }
```

---

### `436`
**Source:** `ears.gon`  

```
436 {
        tag common
        spd 2
        con -1
    }
```

---

### `437`
**Source:** `ears.gon`  

```
437 {
        tag common
        spd 2
        str -1
    }
```

---

### `438`
**Source:** `ears.gon`  

```
438 {
        tag common
        spd 2
        cha -1
    }
```

---

### `439`
**Source:** `ears.gon`  

```
439 {
        tag common
        spd 2
        int -1
    }
```

---

### `440`
**Source:** `ears.gon`  

```
440 {
        tag common
        spd 2
        dex -1
    }
```

---

### `441`
**Source:** `ears.gon`  

```
441 {
        tag common
        spd 2
        lck -1
    }
```

---

### `700`
**Name:** anotia  
**Source:** `ears.gon`  

```
700 { //anotia
        tag birth_defect
        lck -2
    }
```

---

### `701`
**Name:** turner syndrome  
**Source:** `ears.gon`  

```
701 { //turner syndrome
        tag birth_defect
        int -2
    }
```

---

### `702`
**Name:** underdeveloped ears  
**Source:** `ears.gon`  

```
702 { //underdeveloped ears
        tag birth_defect
        cha -1
    }
```

---

### `703`
**Name:** low ears  
**Description:** Start each battle with Confusion 2.  
**Source:** `ears.gon`  

```
703 { //low ears
        desc "MUTATION_EARS_703_DESC"
        tag birth_defect

        passives {
            Confusion 2
        }
    }
```

---

### `704`
**Name:** wilted ears  
**Description:** Start each battle with Immobile 1.  
**Source:** `ears.gon`  

```
704 { //wilted ears
        desc "MUTATION_EARS_704_DESC"
        tag birth_defect

        passives {
            Immobile 1
        }
    }
```

---

### `2`
**Name:** no ears (completely missing part) //TODO: deaf (unaffected by musical abilities)  
**Source:** `ears.gon`  

```
2 { //no ears (completely missing part) //TODO: deaf (unaffected by musical abilities)
        tag birth_defect
        dex -2
    }
```

---

## Eyebrows Mutations

### `300`
**Name:** Bolt Brows  
**Source:** `eyebrows.gon`  

```
300 { // Bolt Brows
        spd 1
    }
```

---

### `301`
**Name:** Confusing Brows  
**Description:** You have a 10% chance to inflict Confusion on units who contact or attack you.  
**Source:** `eyebrows.gon`  

```
301 { // Confusing Brows
        desc MUTATION_EYEBROWS_301_DESC

        passives {
            RevengeDamage {
                type status
                damage 0
                effects {
                    Confusion [1, .1]
                }
            }
        }
    }
```

---

### `302`
**Name:** Metal Brows  
**Source:** `eyebrows.gon`  

```
302 { // Metal Brows
        shield 2
    }
```

---

### `303`
**Name:** Fancy Makeup  
**Source:** `eyebrows.gon`  

```
303 { // Fancy Makeup
        cha 1
    }
```

---

### `304`
**Name:** Wolfy Brows  
**Source:** `eyebrows.gon`  

```
304 { // Wolfy Brows
        tag animal
        dex 1
    }
```

---

### `305`
**Name:** Dotty Brows  
**Source:** `eyebrows.gon`  

```
305 { // Dotty Brows
        lck 1
    }
```

---

### `306`
**Name:** Clown Makeup  
**Description:** You have a 5% chance to inflict Fear on units who contact or attack you.  
**Source:** `eyebrows.gon`  

```
306 { // Clown Makeup
        desc MUTATION_EYEBROWS_306_DESC

        passives {
            RevengeDamage {
                type status
                damage 0
                effects {
                    Fear [1, .05]
                }
            }
        }
    }
```

---

### `307`
**Name:** Antennae  
**Description:** +1 Mana Regeneration. +1 Health Regeneration.  
**Source:** `eyebrows.gon`  

```
307 { // Antennae
        desc MUTATION_EYEBROWS_307_DESC

        passives {
            HealthRegenUp 1
            AddManaRegen 1
        }
    }
```

---

### `308`
**Name:** Long Lashes  
**Source:** `eyebrows.gon`  

```
308 { // Long Lashes
        cha 1
    }
```

---

### `309`
**Name:** Spiny Brows  
**Description:** +1 Thorns.  
**Source:** `eyebrows.gon`  

```
309 { // Spiny Brows
        desc MUTATION_EYEBROWS_309_DESC

        passives {
            Thorns 1
        }
    }
```

---

### `310`
**Name:** Extra Eye  
**Description:** +1 Range.  
**Source:** `eyebrows.gon`  

```
310 { //Extra Eye
        desc MUTATION_EYEBROWS_310_DESC
        tag extra

        passives {
            AddBonusRange 1
        }
    }
```

---

### `311`
**Name:** Stacked Brows  
**Description:** When you cast your third spell each turn, heal 2.  
**Source:** `eyebrows.gon`  

```
311 { //Stacked Brows
        desc MUTATION_EYEBROWS_311_DESC

        passives { 
            StatusEveryXSpellCastsEachTurn {
                stacks 3
                HealthGain 2
            }
        }
    }
```

---

### `312`
**Source:** `eyebrows.gon`  

```
312 { //
    //}
```

---

### `313`
**Name:** Square Glasses  
**Description:** Spawn 1-2 extra pickups in each battle.  
**Source:** `eyebrows.gon`  

```
313 { //Square Glasses
        desc MUTATION_EYEBROWS_313_DESC
    
        passives { 
            SpawnExtraThingsOnBattleStart {
                object RandomPickup
                number [1 2]
            }
        }
    }
```

---

### `314`
**Name:** Holy Brows  
**Description:** When an allied cat dies, gain +2 Damage.  
**Source:** `eyebrows.gon`  

```
314 { // Holy Brows
        desc MUTATION_EYEBROWS_314_DESC

        passives {
            StatusOnAllyCatDeath {
                DamageUp 2
            }
        }
    }
```

---

### `315`
**Name:** Triangle Eyes  
**Description:** You can reroll your options when you level up.  
**Source:** `eyebrows.gon`  

```
315 { //Triangle Eyes
        desc MUTATION_EYEBROWS_315_DESC

        passives { 
            AddLevelUpRerolls 1
        }
    }
```

---

### `900`
**Name:** slender  
**Description:** +5% dodge chance. Your basic attack has a 1% chance to inflict Freeze.  
**Source:** `eyebrows.gon`  

```
900 { //slender
        desc MUTATION_EYEBROWS_900_DESC

        passives {
            AddStatusToBasicAttack {
                Freeze [1 .01]
            }
            DodgeChance 5%
        }
    }
```

---

### `400`
**Source:** `eyebrows.gon`  

```
400 {
        tag common
        str 2
        con -1
    }
```

---

### `401`
**Source:** `eyebrows.gon`  

```
401 {
        tag common
        str 2
        dex -1
    }
```

---

### `402`
**Source:** `eyebrows.gon`  

```
402 {
        tag common
        str 2
        cha -1
    }
```

---

### `403`
**Source:** `eyebrows.gon`  

```
403 {
        tag common
        str 2
        int -1
    }
```

---

### `404`
**Source:** `eyebrows.gon`  

```
404 {
        tag common
        str 2
        spd -1
    }
```

---

### `405`
**Source:** `eyebrows.gon`  

```
405 {
        tag common
        str 2
        lck -1
    }
```

---

### `406`
**Source:** `eyebrows.gon`  

```
406 {
        tag common
        con 2
        str -1
    }
```

---

### `407`
**Source:** `eyebrows.gon`  

```
407 {
        tag common
        con 2
        dex -1
    }
```

---

### `408`
**Source:** `eyebrows.gon`  

```
408 {
        tag common
        con 2
        cha -1
    }
```

---

### `409`
**Source:** `eyebrows.gon`  

```
409 {
        tag common
        con 2
        int -1
    }
```

---

### `410`
**Source:** `eyebrows.gon`  

```
410 {
        tag common
        con 2
        spd -1
    }
```

---

### `411`
**Source:** `eyebrows.gon`  

```
411 {
        tag common
        con 2
        lck -1
    }
```

---

### `412`
**Source:** `eyebrows.gon`  

```
412 {
        tag common
        dex 2
        con -1
    }
```

---

### `413`
**Source:** `eyebrows.gon`  

```
413 {
        tag common
        dex 2
        str -1
    }
```

---

### `414`
**Source:** `eyebrows.gon`  

```
414 {
        tag common
        dex 2
        cha -1
    }
```

---

### `415`
**Source:** `eyebrows.gon`  

```
415 {
        tag common
        dex 2
        int -1
    }
```

---

### `416`
**Source:** `eyebrows.gon`  

```
416 {
        tag common
        dex 2
        spd -1
    }
```

---

### `417`
**Source:** `eyebrows.gon`  

```
417 {
        tag common
        dex 2
        lck -1
    }
```

---

### `418`
**Source:** `eyebrows.gon`  

```
418 {
        tag common
        int 2
        con -1
    }
```

---

### `419`
**Source:** `eyebrows.gon`  

```
419 {
        tag common
        int 2
        dex -1
    }
```

---

### `420`
**Source:** `eyebrows.gon`  

```
420 {
        tag common
        int 2
        cha -1
    }
```

---

### `421`
**Source:** `eyebrows.gon`  

```
421 {
        tag common
        int 2
        str -1
    }
```

---

### `422`
**Source:** `eyebrows.gon`  

```
422 {
        tag common
        int 2
        spd -1
    }
```

---

### `423`
**Source:** `eyebrows.gon`  

```
423 {
        tag common
        int 2
        lck -1
    }
```

---

### `424`
**Source:** `eyebrows.gon`  

```
424 {
        tag common
        cha 2
        con -1
    }
```

---

### `425`
**Source:** `eyebrows.gon`  

```
425 {
        tag common
        cha 2
        dex -1
    }
```

---

### `426`
**Source:** `eyebrows.gon`  

```
426 {
        tag common
        cha 2
        str -1
    }
```

---

### `427`
**Source:** `eyebrows.gon`  

```
427 {
        tag common
        cha 2
        int -1
    }
```

---

### `428`
**Source:** `eyebrows.gon`  

```
428 {
        tag common
        cha 2
        spd -1
    }
```

---

### `429`
**Source:** `eyebrows.gon`  

```
429 {
        tag common
        cha 2
        lck -1
    }
```

---

### `430`
**Source:** `eyebrows.gon`  

```
430 {
        tag common
        lck 2
        con -1
    }
```

---

### `431`
**Source:** `eyebrows.gon`  

```
431 {
        tag common
        lck 2
        dex -1
    }
```

---

### `432`
**Source:** `eyebrows.gon`  

```
432 {
        tag common
        lck 2
        cha -1
    }
```

---

### `433`
**Source:** `eyebrows.gon`  

```
433 {
        tag common
        lck 2
        int -1
    }
```

---

### `434`
**Source:** `eyebrows.gon`  

```
434 {
        tag common
        lck 2
        spd -1
    }
```

---

### `435`
**Source:** `eyebrows.gon`  

```
435 {
        tag common
        lck 2
        str -1
    }
```

---

### `436`
**Source:** `eyebrows.gon`  

```
436 {
        tag common
        spd 2
        con -1
    }
```

---

### `437`
**Source:** `eyebrows.gon`  

```
437 {
        tag common
        spd 2
        str -1
    }
```

---

### `438`
**Source:** `eyebrows.gon`  

```
438 {
        tag common
        spd 2
        cha -1
    }
```

---

### `439`
**Source:** `eyebrows.gon`  

```
439 {
        tag common
        spd 2
        int -1
    }
```

---

### `440`
**Source:** `eyebrows.gon`  

```
440 {
        tag common
        spd 2
        dex -1
    }
```

---

### `441`
**Source:** `eyebrows.gon`  

```
441 {
        tag common
        spd 2
        lck -1
    }
```

---

### `700`
**Name:** bushy  
**Source:** `eyebrows.gon`  

```
700 { //bushy
        tag birth_defect
        lck -1
    }
```

---

### `701`
**Name:** no eyebrows  
**Source:** `eyebrows.gon`  

```
701 { //no eyebrows
        tag birth_defect
        cha -1
    }
```

---

### `702`
**Name:** unibrow  
**Source:** `eyebrows.gon`  

```
702 { //unibrow
        tag birth_defect
        int -1
    }
```

---

### `2`
**Name:** no eyebrows (completely missing part)  
**Source:** `eyebrows.gon`  

```
2 { //no eyebrows (completely missing part)
        tag birth_defect
        cha -2
    }
```

---

## Eyes Mutations

### `300`
**Name:** Button Eyes  
**Description:** Your basic attack has a 10% chance to inflict Fear.  
**Source:** `eyes.gon`  

```
300 { //Button Eyes
        desc "MUTATION_EYES_300_DESC"

        passives {
            AddStatusToBasicAttack {
                Fear [1 .1]
            }
        }
    }
```

---

### `301`
**Name:** Demon Eyes  
**Source:** `eyes.gon`  

```
301 { //Demon Eyes  
        dex 1
    }
```

---

### `302`
**Name:** Pop Eyes  
**Description:** +1 Thorns.  
**Source:** `eyes.gon`  

```
302 { //Pop Eyes 
        desc "MUTATION_EYES_302_DESC"
        passives {
            Thorns 1
        }
    }
```

---

### `303`
**Name:** Gem Eyes  
**Source:** `eyes.gon`  

```
303 { //Gem Eyes  
        int 1
        cha 1
    }
```

---

### `304`
**Name:** Holes  
**Description:** Take your turn later.  
**Source:** `eyes.gon`  

```
304 { //Holes  
        desc "MUTATION_EYES_304_DESC"
        passives {
            AddInitiative -20
        }
    }
```

---

### `305`
**Name:** Zen Eyes  
**Source:** `eyes.gon`  

```
305 { //Zen Eyes  
        str -1
        dex -1
        int 3
    }
```

---

### `306`
**Name:** Confusing Eyes  
**Description:** Your basic attack has a 10% chance to inflict Confusion 3.  
**Source:** `eyes.gon`  

```
306 { //Confusing Eyes
        desc "MUTATION_EYES_306_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [3, .1]
            }
        }
    }
```

---

### `307`
**Name:** Half Moon Eyes  
**Description:** Gain 1 mana when anything dies.  
**Source:** `eyes.gon`  

```
307 { //Half Moon Eyes
        desc "MUTATION_EYES_307_DESC"
        passives {
            GainManaWhenAnythingDies 1
        }
    }
```

---

### `308`
**Name:** Spider Eyes  
**Description:** +5% dodge chance.  
**Source:** `eyes.gon`  

```
308 { //Spider Eyes
        tag animal
        desc "MUTATION_EYES_308_DESC"
        passives {
            DodgeChance 5%
        }
    }
```

---

### `309`
**Name:** Doll Eyes  
**Description:** +2 corpse health.  
**Source:** `eyes.gon`  

```
309 { //Doll Eyes
        desc "MUTATION_EYES_309_DESC"
        passives {
            AddCorpseHealth 2
        }
    }
```

---

### `310`
**Name:** Octo Eyes  
**Description:** +1 Health Regeneration  
**Source:** `eyes.gon`  

```
310 { //Octo Eyes
        tag animal
        desc "MUTATION_EYES_310_DESC"
        passives {
            HealthRegenUp 1
        }
    }
```

---

### `311`
**Name:** gecko eye  
**Description:** You do not take extra damage from backstabs.  
**Source:** `eyes.gon`  

```
311 { //gecko eye
        tag animal
        desc "MUTATION_EYES_311_DESC"
        passives {
            BackstabImmunity 1
        }
    }
```

---

### `312`
**Name:** Metal Eyes  
**Description:** +1 Brace.  
**Source:** `eyes.gon`  

```
312 { // Metal Eyes
        desc "MUTATION_EYES_312_DESC"
        shield 1
        passives {
            Brace 1
        }
    }
```

---

### `313`
**Name:** Issac's Eyes  
**Description:** Your basic attack creates water tiles.  
**Source:** `eyes.gon`  

```
313 { // Issac's Eyes
        desc "MUTATION_EYES_313_DESC"
		divine_shield 1
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        } 
    }
```

---

### `314`
**Name:** Dead Eyes  
**Description:** When you are downed, spawn 3 Flies. +2 corpse health.  
**Source:** `eyes.gon`  

```
314 { // Dead Eyes
        desc "MUTATION_EYES_314_DESC"
        passives {
            SpawnOnDowned CharmedFly
            SpawnOnDowned CharmedFly
            SpawnOnDowned CharmedFly
            AddCorpseHealth 2
        }
    }
```

---

### `315`
**Name:** Kinetic eyes  
**Description:** +1 Kinetic Spikes.  
**Source:** `eyes.gon`  

```
315 { // Kinetic eyes
        desc "MUTATION_EYES_315_DESC"
        passives {
            KineticSpikes 1
        }
    }
```

---

### `316`
**Name:** Lightning eyes  
**Description:** 15% chance to counter attack with Chain Lightning when you get hit.  
**Source:** `eyes.gon`  

```
316 { // Lightning eyes
        desc "MUTATION_EYES_316_DESC"
        passives { 
            CounterAttack {
                chance 15%
                ability ChainLightning
            }
        }
    }
```

---

### `317`
**Name:** Dice Eyes  
**Description:** Gain a random stat up at the end of each turn.  
**Source:** `eyes.gon`  

```
317 { // Dice Eyes
        desc "MUTATION_EYES_317_DESC"
        passives { 
            StatusEachTurnEnd {
                RandomStatUp 1
            } 
        }
    }
```

---

### `318`
**Name:** Goat Eyes  
**Description:** You can see hidden things. +1 Knockback damage.  
**Source:** `eyes.gon`  

```
318 { // Goat Eyes
        tag animal
        desc "MUTATION_EYES_318_DESC"
        passives {
            ShowHiddenThings 1
            AddKnockbackDamage 1
        }
    }
```

---

### `319`
**Name:** Horn Eyes  
**Description:** Blind. +1 Damage. +1 Thorns.  
**Source:** `eyes.gon`  

```
319 { // Horn Eyes
        desc "MUTATION_EYES_319_DESC"
        passives {
            Blind -1  
            Thorns 1
            DamageUp 1
        }
    }
```

---

### `320`
**Name:** Odd Eyes  
**Source:** `eyes.gon`  

```
320 { // Odd Eyes
    //    desc ""
    //    passives {
    //
    //    }
    //}
```

---

### `321`
**Name:** Robo Eyes  
**Source:** `eyes.gon`  

```
321 { // Robo Eyes
    //    desc ""
    //    passives {
    //
    //    }
    //}
```

---

### `323`
**Name:** Alien Eyes  
**Source:** `eyes.gon`  

```
323 { // Alien Eyes
    //    desc ""
    //    passives {
    //
    //    }
    //}
```

---

### `324`
**Name:** Treasure Eyes  
**Description:** Spawn 2 extra coins each battle.  
**Source:** `eyes.gon`  

```
324 { // Treasure Eyes
        desc "MUTATION_EYES_324_DESC"
        passives {
            SpawnOnBattleStartRandomEmptyTile {
                object Coin
                number 2
            }
        }
    }
```

---

### `325`
**Name:** Nail Eyes  
**Description:** Thorns 1.  
**Source:** `eyes.gon`  

```
325 { // Nail Eyes
        desc "MUTATION_EYES_325_DESC"
        passives {
            Thorns 1
        }
    }
```

---

### `326`
**Name:** 4 Eyes  
**Description:** Gain 2 Charge each time you cast 4 spells.  
**Source:** `eyes.gon`  

```
326 { // 4 Eyes
        desc "MUTATION_EYES_326_DESC"
        passives {
            StatusEveryXSpellCasts {
                stacks 4
                Charge 2
            }
        }
    }
```

---

### `327`
**Name:** Baby Blue Eyes  
**Source:** `eyes.gon`  

```
327 { // Baby Blue Eyes
        cha 2 
    }
```

---

### `328`
**Name:** Bull's Eye'  
**Description:** +10% crit chance.  
**Source:** `eyes.gon`  

```
328 { // Bull's Eye'
        tag animal
        desc "MUTATION_EYES_328_DESC"
        
        passives {
            CritChanceUp 10
        }
    }
```

---

### `329`
**Name:** Spinning Eyes  
**Description:** Your basic attack has a 15% chance to inflict Confusion.  
**Source:** `eyes.gon`  

```
329 { // Spinning Eyes
        desc "MUTATION_EYES_329_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [1, .15]
            }
        }
    }
```

---

### `330`
**Name:** Crow Eyes  
**Description:** 10% chance lethal damage only brings you to 1 hp  
**Source:** `eyes.gon`  

```
330 { // Crow Eyes
    //    desc "10% chance lethal damage only brings you to 1 hp"
    //    passives {
    //        
    //    }
    //}
```

---

### `331`
**Name:** Glassy Eyes  
**Description:** At the start of each battle, gain a random temporary pill if your trinket slot is empty.  
**Source:** `eyes.gon`  

```
331 { // Glassy Eyes
        desc "MUTATION_EYES_331_DESC"
        passives {
            EquipRandomTemporaryItemFromPool pills
        }
    }
```

---

### `332`
**Name:** Bleeding Eyes  
**Description:** Start each battle Bleeding. Gain 1 Charge each time you take damage.  
**Source:** `eyes.gon`  

```
332 { // Bleeding Eyes
        desc "MUTATION_EYES_332_DESC"
        passives {
            Bleed 1  
            StatusOnTookDamage {
                Charge 1
            }
        }
    }
```

---

### `333`
**Name:** Huge Eyes  
**Description:** Your basic attack can't miss.  
**Source:** `eyes.gon`  

```
333 { // Huge Eyes
        desc "MUTATION_EYES_333_DESC"
        passives {
            BasicAttackCantMiss 1
        }
    }
```

---

### `334`
**Name:** Infested Eyes  
**Description:** Blind. Spawn a Flea when you take damage.  
**Source:** `eyes.gon`  

```
334 { // Infested Eyes
        desc "MUTATION_EYES_334_DESC"
        passives {
            Blind -1
            SpawnThingOnDamage {
                object CharmedFlea
                good false //good relative to the thing attacking, for luck calculations
                chance 100%
            }
        }
    }
```

---

### `335`
**Name:** Fake Eyelashes  
**Description:** Your basic attack has a 10% chance to Charm.  
**Source:** `eyes.gon`  

```
335 { // Fake Eyelashes
        desc "MUTATION_EYES_335_DESC"
        passives {
            AddStatusToBasicAttack {
                Charmed [1, .10]  
            }
        }
    }
```

---

### `336`
**Name:** Bolt Eyes  
**Description:** Your basic attack is electric element and has a 5% chance to stun.  
**Source:** `eyes.gon`  

```
336 { // Bolt Eyes
        desc "MUTATION_EYES_336_DESC" 
        passives { 
            AddElementsToBasicAttack Electric
            AddStatusToBasicAttack {
                Stun [1 .05]
            }
        }
    }
```

---

### `337`
**Name:** Ice Eyes  
**Description:** Your basic attack is ice element and inflicts Slow.  
**Source:** `eyes.gon`  

```
337 { // Ice Eyes
        desc "MUTATION_EYES_337_DESC"
        passives {
            AddStatusToBasicAttack {
                Slow 1
            }
            AddElementsToBasicAttack Ice
        }
    }
```

---

### `338`
**Name:** Fire Eyes  
**Description:** Your basic attack inflicts Burn.  
**Source:** `eyes.gon`  

```
338 { // Fire Eyes
        desc "MUTATION_EYES_338_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 1
            }
            AddElementsToBasicAttack Fire
        }
    }
```

---

### `339`
**Name:** Water Eyes  
**Description:** +1 Health Regeneration while wet. Your basic attack is water element.  
**Source:** `eyes.gon`  

```
339 { // Water Eyes
        desc "MUTATION_EYES_339_DESC"
        passives {
            AddElementsToBasicAttack Water  
            PassiveWhenAffectedByElement {
                element water
                passives {
                    HealthRegenUp 1
                } 
            } 
        }
    }
```

---

### `340`
**Name:** Leech Eyes  
**Description:** Your basic attack inflicts Leech.  
**Source:** `eyes.gon`  

```
340 { // Leech Eyes
        desc "MUTATION_EYES_340_DESC"
        passives {
            AddStatusToBasicAttack {
                Leeches 1
            }
        }
    }
```

---

### `341`
**Name:** Flower Eyes  
**Description:** Gain Charge 1 the first time you move each turn.  
**Source:** `eyes.gon`  

```
341 { // Flower Eyes
        desc "MUTATION_EYES_341_DESC"
        passives {
            StatusOnEndMove {
                Conditional_FirstApplicationThisTurn {
                    Charge 1
                }
            }
        }
    }
```

---

### `342`
**Name:** Poison Eyes  
**Description:** Your basic attack inflicts Poison 1. Start each battle Poisoned.  
**Source:** `eyes.gon`  

```
342 { // Poison Eyes
        desc "MUTATION_EYES_342_DESC"
        passives { 
            AddStatusToBasicAttack {
                Poison 1
            } 
            Poison 1
        }
    }
```

---

### `343`
**Name:** Clown Eyes  
**Description:** You have a 5% chance to inflict Fear on units who contact or attack you.  
**Source:** `eyes.gon`  

```
343 { // Clown Eyes
        desc "MUTATION_EYES_343_DESC"
        passives { 
            RevengeDamage {
                effects {
                    Fear [1, .05]
                }
            }
        }
    }
```

---

### `344`
**Name:** Sun Eyes  
**Description:** You have a 10% chance to Blind units who contact or attack you.  
**Source:** `eyes.gon`  

```
344 { // Sun Eyes
        desc "MUTATION_EYES_344_DESC"
        passives { 
            RevengeDamage {
                effects {
                    Blind [1, .10]
                }
            }
        }
    }
```

---

### `345`
**Name:** Evil Eyes  
**Description:** Inflict a random debuff on units who contact you.  
**Source:** `eyes.gon`  

```
345 { // Evil Eyes
        desc "MUTATION_EYES_345_DESC"
        passives { 
            MeleeRevengeDamage {
                effects {
                    RandomStatusFromPool {
                        Poison 1
                        Burn 1
                        Bleed 1
                        Blind 1 
                        Weakness 1 
                    }
                } 
            }
        }
    }
```

---

### `346`
**Name:** Rock Eyes  
**Description:** Spawn a rock when damaged.  
**Source:** `eyes.gon`  

```
346 { // Rock Eyes
        desc "MUTATION_EYES_346_DESC" 
        shield 1
        passives { 
            SpawnThingOnDamage {
                object SmallRock
                good false //good relative to the thing attacking, for luck calculations
                chance 100%
            } 
        }
    }
```

---

### `347`
**Name:** Hypno Eyes  
**Description:** Your basic attack has a 15% chance to inflict Confusion 2.  
**Source:** `eyes.gon`  

```
347 { // Hypno Eyes
        desc "MUTATION_EYES_347_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [2, .15]
            }
        }
    }
```

---

### `348`
**Name:** Pop Eyes  
**Description:** +1 range, +1 reach.  
**Source:** `eyes.gon`  

```
348 { // Pop Eyes
        desc "MUTATION_EYES_348_DESC" 
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1 
        }
    }
```

---

### `349`
**Name:** 8 Eyes  
**Description:** Emit 4 Sparkles each time you cast 8 spells.  
**Source:** `eyes.gon`  

```
349 { // 8 Eyes
        desc "MUTATION_EYES_349_DESC"
        passives {
            StatusEveryXSpellCasts {
                stacks 8
                RandomMagicMissile 4
            }
        }
    }
```

---

### `351`
**Name:** Chaos Eyes  
**Description:** Your bonus ability is a different random spell each battle.  
**Source:** `eyes.gon`  

```
351 { // Chaos Eyes
        desc "MUTATION_EYES_351_DESC"
        passives {
            ConjureBonusAbility random
        }
    }
```

---

### `352`
**Name:** Runny Mascara  
**Description:** You have All Stats Up while Bleeding.  
**Source:** `eyes.gon`  

```
352 { // Runny Mascara
        desc "MUTATION_EYES_352_DESC"

        passives {
            PassiveWhileHasStatus {
                status Bleed
                passives {
                    AllStatsUp 1  
                } 
            }
        }
    }
```

---

### `353`
**Name:** Chameleon Eyes  
**Description:** You take no extra damage from backstabs.  
**Source:** `eyes.gon`  

```
353 { // Chameleon Eyes
        tag animal
        desc "MUTATION_EYES_353_DESC"
        passives {
            BackstabImmunity 1 
        }
    }
```

---

### `442`
**Description:** 10% chance to reflect projectiles.  
**Source:** `eyes.gon`  

```
442 {
        desc "MUTATION_EYES_442_DESC"
        passives {
            ReflectProjectiles 10%
        }
    }
```

---

### `750`
**Name:** glasses  
**Source:** `eyes.gon`  

```
750 {//glasses
		int 1
    }
```

---

### `754`
**Name:** alien eyes  
**Description:** +1 range. Your basic attack is gravity element.  
**Source:** `eyes.gon`  

```
754 {//alien eyes
        desc "MUTATION_EYES_754_DESC"
        passives {
			AddBonusRange 1
            AddElementsToBasicAttack Gravity
        } 
    }
```

---

### `755`
**Name:** mothman eyes  
**Description:** Your basic attack has a 15% chance to inflict Fear.  
**Source:** `eyes.gon`  

```
755 {//mothman eyes
        desc "MUTATION_EYES_755_DESC"
		passives {
			AddStatusToBasicAttack {
				Fear [1 .15]
			}
		}
    }
```

---

### `900`
**Name:** slender  
**Description:** Your basic attack has a 10% chance to inflict Slow.  
**Source:** `eyes.gon`  

```
900 { //slender
        desc "MUTATION_EYES_900_DESC"
   
        passives {
            AddStatusToBasicAttack {
                Slow [1 .1]
            }
        }
    }
```

---

### `400`
**Source:** `eyes.gon`  

```
400 {
        tag common
        str 2
        con -1
    }
```

---

### `401`
**Source:** `eyes.gon`  

```
401 {
        tag common
        str 2
        dex -1
    }
```

---

### `402`
**Source:** `eyes.gon`  

```
402 {
        tag common
        str 2
        cha -1
    }
```

---

### `403`
**Source:** `eyes.gon`  

```
403 {
        tag common
        str 2
        int -1
    }
```

---

### `404`
**Source:** `eyes.gon`  

```
404 {
        tag common
        str 2
        spd -1
    }
```

---

### `405`
**Source:** `eyes.gon`  

```
405 {
        tag common
        str 2
        lck -1
    }
```

---

### `406`
**Source:** `eyes.gon`  

```
406 {
        tag common
        con 2
        str -1
    }
```

---

### `407`
**Source:** `eyes.gon`  

```
407 {
        tag common
        con 2
        dex -1
    }
```

---

### `408`
**Source:** `eyes.gon`  

```
408 {
        tag common
        con 2
        cha -1
    }
```

---

### `409`
**Source:** `eyes.gon`  

```
409 {
        tag common
        con 2
        int -1
    }
```

---

### `410`
**Source:** `eyes.gon`  

```
410 {
        tag common
        con 2
        spd -1
    }
```

---

### `411`
**Source:** `eyes.gon`  

```
411 {
        tag common
        con 2
        lck -1
    }
```

---

### `412`
**Source:** `eyes.gon`  

```
412 {
        tag common
        dex 2
        con -1
    }
```

---

### `413`
**Source:** `eyes.gon`  

```
413 {
        tag common
        dex 2
        str -1
    }
```

---

### `414`
**Source:** `eyes.gon`  

```
414 {
        tag common
        dex 2
        cha -1
    }
```

---

### `415`
**Source:** `eyes.gon`  

```
415 {
        tag common
        dex 2
        int -1
    }
```

---

### `416`
**Source:** `eyes.gon`  

```
416 {
        tag common
        dex 2
        spd -1
    }
```

---

### `417`
**Source:** `eyes.gon`  

```
417 {
        tag common
        dex 2
        lck -1
    }
```

---

### `418`
**Source:** `eyes.gon`  

```
418 {
        tag common
        int 2
        con -1
    }
```

---

### `419`
**Source:** `eyes.gon`  

```
419 {
        tag common
        int 2
        dex -1
    }
```

---

### `420`
**Source:** `eyes.gon`  

```
420 {
        tag common
        int 2
        cha -1
    }
```

---

### `421`
**Source:** `eyes.gon`  

```
421 {
        tag common
        int 2
        str -1
    }
```

---

### `422`
**Source:** `eyes.gon`  

```
422 {
        tag common
        int 2
        spd -1
    }
```

---

### `423`
**Source:** `eyes.gon`  

```
423 {
        tag common
        int 2
        lck -1
    }
```

---

### `424`
**Source:** `eyes.gon`  

```
424 {
        tag common
        cha 2
        con -1
    }
```

---

### `425`
**Source:** `eyes.gon`  

```
425 {
        tag common
        cha 2
        dex -1
    }
```

---

### `426`
**Source:** `eyes.gon`  

```
426 {
        tag common
        cha 2
        str -1
    }
```

---

### `427`
**Source:** `eyes.gon`  

```
427 {
        tag common
        cha 2
        int -1
    }
```

---

### `428`
**Source:** `eyes.gon`  

```
428 {
        tag common
        cha 2
        spd -1
    }
```

---

### `429`
**Source:** `eyes.gon`  

```
429 {
        tag common
        cha 2
        lck -1
    }
```

---

### `430`
**Source:** `eyes.gon`  

```
430 {
        tag common
        lck 2
        con -1
    }
```

---

### `431`
**Source:** `eyes.gon`  

```
431 {
        tag common
        lck 2
        dex -1
    }
```

---

### `432`
**Source:** `eyes.gon`  

```
432 {
        tag common
        lck 2
        cha -1
    }
```

---

### `433`
**Source:** `eyes.gon`  

```
433 {
        tag common
        lck 2
        int -1
    }
```

---

### `434`
**Source:** `eyes.gon`  

```
434 {
        tag common
        lck 2
        spd -1
    }
```

---

### `435`
**Source:** `eyes.gon`  

```
435 {
        tag common
        lck 2
        str -1
    }
```

---

### `436`
**Source:** `eyes.gon`  

```
436 {
        tag common
        spd 2
        con -1
    }
```

---

### `437`
**Source:** `eyes.gon`  

```
437 {
        tag common
        spd 2
        str -1
    }
```

---

### `438`
**Source:** `eyes.gon`  

```
438 {
        tag common
        spd 2
        cha -1
    }
```

---

### `439`
**Source:** `eyes.gon`  

```
439 {
        tag common
        spd 2
        int -1
    }
```

---

### `440`
**Source:** `eyes.gon`  

```
440 {
        tag common
        spd 2
        dex -1
    }
```

---

### `441`
**Source:** `eyes.gon`  

```
441 {
        tag common
        spd 2
        lck -1
    }
```

---

### `700`
**Name:** graves disease  
**Source:** `eyes.gon`  

```
700 { //graves disease
        tag birth_defect
        cha -2
    }
```

---

### `701`
**Name:** anophthalmia  
**Source:** `eyes.gon`  

```
701 { //anophthalmia
        tag birth_defect
        lck -2
    }
```

---

### `702`
**Source:** `eyes.gon`  

```
702 {
        cha 1
        int 1
        con -2
    }
```

---

### `2`
**Name:** no eyes (frame 703, but completely missing parts are special and keyed in on -2)  
**Description:** Blind.  
**Source:** `eyes.gon`  

```
2 { //no eyes (frame 703, but completely missing parts are special and keyed in on -2)
        desc "MUTATION_EYES_M2_DESC"
        tag birth_defect
   
        passives {
            Blind -1
        }
    }
```

---

### `704`
**Name:** lazy eye  
**Description:** 10% miss chance.  
**Source:** `eyes.gon`  

```
704 { //lazy eye
        desc "MUTATION_EYES_704_DESC"
        tag birth_defect
   
        passives {
            MissChance 10
        }
   
    }
```

---

### `705`
**Name:** cataracts  
**Description:** Gain 5% miss chance every turn.  
**Source:** `eyes.gon`  

```
705 { //cataracts
        tag birth_defect
        desc "MUTATION_EYES_705_DESC"
   
        passives {
            StatusEachTurnBegin {
                MissChance 5
            }
        }
   
    }
```

---

### `706`
**Name:** crossed eyes  
**Description:** Start each battle with Confusion 2.  
**Source:** `eyes.gon`  

```
706 { //crossed eyes
        desc "MUTATION_EYES_706_DESC"
        tag birth_defect
   
        passives {
            Confusion 2
        }
    }
```

---

### `1029`
**Name:** spider eye  
**Description:** +5% crit chance.  
**Source:** `eyes.gon`  

```
1029 { //spider eye
        desc "MUTATION_EYES_1029_DESC"
   
        passives {
            CritChanceUp 5
        }
    }
```

---

## Head Mutations

### `300`
**Name:** Square head  
**Source:** `head.gon`  

```
300 { //Square head
        con 1
    }
```

---

### `301`
**Name:** Sloth head  
**Source:** `head.gon`  

```
301 { //Sloth head
        int -1
        str 1
        con 1
    }
```

---

### `302`
**Name:** Big brain  
**Source:** `head.gon`  

```
302 { //Big brain
        int 2
        con -1
    }
```

---

### `303`
**Name:** Spioke head  
**Description:** +1 Thorns.  
**Source:** `head.gon`  

```
303 { //Spioke head
        desc "MUTATION_HEAD_303_DESC"
        passives {
            Thorns 1
        }
    }
```

---

### `304`
**Name:** Sludge head  
**Description:** +2 Health Regeneration +5% dodge chance.  
**Source:** `head.gon`  

```
304 { //Sludge head
        tag melted
        desc "MUTATION_HEAD_304_DESC"

        cha -2
        passives {
            HealthRegenUp 2
            DodgeChance 5%
        }
    }
```

---

### `305`
**Name:** Strong Chin  
**Source:** `head.gon`  

```
305 { //Strong Chin
        cha 1
    }
```

---

### `306`
**Name:** Alien head  
**Source:** `head.gon`  

```
306 { //Alien head
        int 1
    }
```

---

### `307`
**Name:** Bump-on-the-head Head  
**Description:** Units that contact you get knocked back 1 tile.  
**Source:** `head.gon`  

```
307 { //Bump-on-the-head Head
        desc "MUTATION_HEAD_307_DESC"

        shield 1
        passives {
            MeleeRevengeDamage {
                type status
                damage 0
                knockback 1
            }
        }
    }
```

---

### `308`
**Name:** Frog Head  
**Description:** +1 movement range while wet. Water does not slow movement.  
**Source:** `head.gon`  

```
308 { //Frog Head
        tag animal
        desc "MUTATION_HEAD_308_DESC"

        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    AddMovement 1
                }
            } 
            WaterWalk 1
        }
    }
```

---

### `309`
**Name:** half moon  
**Source:** `head.gon`  

```
309 { //half moon
        lck 2
    }
```

---

### `310`
**Name:** rock head  
**Source:** `head.gon`  

```
310 { //rock head
        shield 2
    }
```

---

### `311`
**Name:** Money Bag head  
**Description:** Spawn a coin when you take damage.  
**Source:** `head.gon`  

```
311 { //Money Bag head
        desc "MUTATION_HEAD_311_DESC"
    
        passives {
            SpawnThingOnDamage {
                object Coin 
                chance 100%
            }
        }
    }
```

---

### `312`
**Name:** Magnet Head  
**Description:** Your basic attack pulls units towards you.  
**Source:** `head.gon`  

```
312 { //Magnet Head
        desc "MUTATION_HEAD_312_DESC"

        passives {
            MakeBasicAttackPull 1
        } 
    }
```

---

### `313`
**Name:** Poop Head  
**Description:** Poop when you take damage.  
**Source:** `head.gon`  

```
313 { //Poop Head
        desc "MUTATION_HEAD_313_DESC"

        passives {
            PoopWhenHit Poop
        }
    }
```

---

### `314`
**Name:** Pyramid Head  
**Description:** Gain +1 [img:int] at the end of each turn.  
**Source:** `head.gon`  

```
314 { //Pyramid Head
        desc "MUTATION_HEAD_314_DESC"
    
        passives {
            StatusEachTurnEnd {
               IntelligenceUp 1
            } 
        }
    }
```

---

### `315`
**Name:** Upside Down Head  
**Description:** At the start of each battle, swap your highest and lowest stats.  
**Source:** `head.gon`  

```
315 { //Upside Down Head
        desc "MUTATION_HEAD_315_DESC"
   
        passives {
            SwapHighestAndLowestStat 1
        }
    }
```

---

### `316`
**Name:** Fractured Head  
**Description:** When you take damage from an attack, gain a random buff.  
**Source:** `head.gon`  

```
316 { //Fractured Head
        desc "MUTATION_HEAD_316_DESC"
        
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
```

---

### `317`
**Name:** Sideways Head  
**Description:** +5% dodge chance.  
**Source:** `head.gon`  

```
317 { //Sideways Head
        desc "MUTATION_HEAD_317_DESC"

        passives {
            DodgeChance 5% 
        }
    }
```

---

### `318`
**Name:** Long Neck  
**Description:** +1 range.  
**Source:** `head.gon`  

```
318 { //Long Neck
        desc "MUTATION_HEAD_318_DESC"

        passives {
            AddBonusRange 1
        }
    }
```

---

### `319`
**Name:** Exposed Brain  
**Description:** Gain +1 [img:int] permanently at the end of each battle. Start each battle with Bruise 2.  
**Source:** `head.gon`  

```
319 { //Exposed Brain
        desc "MUTATION_HEAD_319_DESC"

        passives {
            Bruise 2
            StatusOnBattleEnd {
                PermanentIntelligence 1
            }
        }
    }
```

---

### `320`
**Name:** Bubble Head  
**Description:** Your basic attack has +2 Knockback.  
**Source:** `head.gon`  

```
320 { //Bubble Head
        desc "MUTATION_HEAD_320_DESC"

        passives {
            AddStatusToBasicAttack {
                Knockback 2
            }
        }
    }
```

---

### `321`
**Name:** Button Head  
**Description:** You have a 5% chance to inflict Fear on units who contact or attack you.  
**Source:** `head.gon`  

```
321 { //Button Head
        desc "MUTATION_HEAD_321_DESC"

        passives { 
            RevengeDamage {
                effects {
                    Fear [1, .05]
                }
            }
        }
    }
```

---

### `750`
**Name:** spiked head  
**Description:** +1 Thorns.  
**Source:** `head.gon`  

```
750 { //spiked head
		desc "MUTATION_HEAD_750_DESC"
        passives { 
			Thorns 1
        }
    }
```

---

### `753`
**Name:** tyler head  
**Description:** You are immune to ice.  
**Source:** `head.gon`  

```
753 { //tyler head
        desc "MUTATION_HEAD_753_DESC"

		passives {
			ElementImmune Ice
			StatusImmunity [Freeze, Slow]
		}
    }
```

---

### `757`
**Name:** grey head  
**Source:** `head.gon`  

```
757 { //grey head
		int 2
    }
```

---

### `759`
**Name:** Human Head  
**Description:** Take an extra turn at the start of the battle.  
**Source:** `head.gon`  

```
759 { //Human Head
        desc "MUTATION_HEAD_759_DESC"
        spd -2

        passives {
            AlphaTurns 1
        }
    }
```

---

### `400`
**Source:** `head.gon`  

```
400 {
        tag common
        str 2
        con -1
    }
```

---

### `401`
**Source:** `head.gon`  

```
401 {
        tag common
        str 2
        dex -1
    }
```

---

### `402`
**Source:** `head.gon`  

```
402 {
        tag common
        str 2
        cha -1
    }
```

---

### `403`
**Source:** `head.gon`  

```
403 {
        tag common
        str 2
        int -1
    }
```

---

### `404`
**Source:** `head.gon`  

```
404 {
        tag common
        str 2
        spd -1
    }
```

---

### `405`
**Source:** `head.gon`  

```
405 {
        tag common
        str 2
        lck -1
    }
```

---

### `406`
**Source:** `head.gon`  

```
406 {
        tag common
        con 2
        str -1
    }
```

---

### `407`
**Source:** `head.gon`  

```
407 {
        tag common
        con 2
        dex -1
    }
```

---

### `408`
**Source:** `head.gon`  

```
408 {
        tag common
        con 2
        cha -1
    }
```

---

### `409`
**Source:** `head.gon`  

```
409 {
        tag common
        con 2
        int -1
    }
```

---

### `410`
**Source:** `head.gon`  

```
410 {
        tag common
        con 2
        spd -1
    }
```

---

### `411`
**Source:** `head.gon`  

```
411 {
        tag common
        con 2
        lck -1
    }
```

---

### `412`
**Source:** `head.gon`  

```
412 {
        tag common
        dex 2
        con -1
    }
```

---

### `413`
**Source:** `head.gon`  

```
413 {
        tag common
        dex 2
        str -1
    }
```

---

### `414`
**Source:** `head.gon`  

```
414 {
        tag common
        dex 2
        cha -1
    }
```

---

### `415`
**Source:** `head.gon`  

```
415 {
        tag common
        dex 2
        int -1
    }
```

---

### `416`
**Source:** `head.gon`  

```
416 {
        tag common
        dex 2
        spd -1
    }
```

---

### `417`
**Source:** `head.gon`  

```
417 {
        tag common
        dex 2
        lck -1
    }
```

---

### `418`
**Source:** `head.gon`  

```
418 {
        tag common
        int 2
        con -1
    }
```

---

### `419`
**Source:** `head.gon`  

```
419 {
        tag common
        int 2
        dex -1
    }
```

---

### `420`
**Source:** `head.gon`  

```
420 {
        tag common
        int 2
        cha -1
    }
```

---

### `421`
**Source:** `head.gon`  

```
421 {
        tag common
        int 2
        str -1
    }
```

---

### `422`
**Source:** `head.gon`  

```
422 {
        tag common
        int 2
        spd -1
    }
```

---

### `423`
**Source:** `head.gon`  

```
423 {
        tag common
        int 2
        lck -1
    }
```

---

### `424`
**Source:** `head.gon`  

```
424 {
        tag common
        cha 2
        con -1
    }
```

---

### `425`
**Source:** `head.gon`  

```
425 {
        tag common
        cha 2
        dex -1
    }
```

---

### `426`
**Source:** `head.gon`  

```
426 {
        tag common
        cha 2
        str -1
    }
```

---

### `427`
**Source:** `head.gon`  

```
427 {
        tag common
        cha 2
        int -1
    }
```

---

### `428`
**Source:** `head.gon`  

```
428 {
        tag common
        cha 2
        spd -1
    }
```

---

### `429`
**Source:** `head.gon`  

```
429 {
        tag common
        cha 2
        lck -1
    }
```

---

### `430`
**Source:** `head.gon`  

```
430 {
        tag common
        lck 2
        con -1
    }
```

---

### `431`
**Source:** `head.gon`  

```
431 {
        tag common
        lck 2
        dex -1
    }
```

---

### `432`
**Source:** `head.gon`  

```
432 {
        tag common
        lck 2
        cha -1
    }
```

---

### `433`
**Source:** `head.gon`  

```
433 {
        tag common
        lck 2
        int -1
    }
```

---

### `434`
**Source:** `head.gon`  

```
434 {
        tag common
        lck 2
        spd -1
    }
```

---

### `435`
**Source:** `head.gon`  

```
435 {
        tag common
        lck 2
        str -1
    }
```

---

### `436`
**Source:** `head.gon`  

```
436 {
        tag common
        spd 2
        con -1
    }
```

---

### `437`
**Source:** `head.gon`  

```
437 {
        tag common
        spd 2
        str -1
    }
```

---

### `438`
**Source:** `head.gon`  

```
438 {
        tag common
        spd 2
        cha -1
    }
```

---

### `439`
**Source:** `head.gon`  

```
439 {
        tag common
        spd 2
        int -1
    }
```

---

### `440`
**Source:** `head.gon`  

```
440 {
        tag common
        spd 2
        dex -1
    }
```

---

### `441`
**Source:** `head.gon`  

```
441 {
        tag common
        spd 2
        lck -1
    }
```

---

### `700`
**Name:** microcephaly  
**Source:** `head.gon`  

```
700 { //microcephaly
        tag birth_defect
        int -2
    }
```

---

### `701`
**Name:** macrocephaly  
**Source:** `head.gon`  

```
701 { //macrocephaly
        tag birth_defect
        int -2
    }
```

---

### `702`
**Name:** concave head  
**Source:** `head.gon`  

```
702 { //concave head
        tag birth_defect
        int -1
    }
```

---

### `703`
**Name:** soft spot  
**Description:** Attacks against your face count as backstabs.  
**Source:** `head.gon`  

```
703 { //soft spot
        desc "MUTATION_HEAD_703_DESC"
        tag birth_defect

        passives {
            BackstabFront 1
        }
    }
```

---

### `704`
**Name:** cyclops  
**Description:** 20% miss chance.
Your spells cost 1 less mana.  
**Source:** `head.gon`  

```
704 { //cyclops
        desc "MUTATION_HEAD_704_DESC"
        tag birth_defect

        passives {
            MissChance 20
            ManaCostReduction 1
        }
    }
```

---

### `705`
**Name:** conjoined head  
**Source:** `head.gon`  

```
705 { //conjoined head
        tag birth_defect
        cha -3
		int 2
    }
```

---

### `706`
**Name:** sloth  
**Description:** Brace 1.  
**Source:** `head.gon`  

```
706 { //sloth
        desc "MUTATION_HEAD_706_DESC"
        tag birth_defect
        cha -3

        passives {
            Brace 1
        }
    }
```

---

### `900`
**Name:** slender  
**Description:** +1 range. +1 reach.  
**Source:** `head.gon`  

```
900 { //slender
        desc "MUTATION_HEAD_900_DESC"

        cha -1
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1
        }
    }
```

---

## Legs Mutations

### `300`
**Name:** Frog legs  
**Description:** +1 movement range while wet. Water does not slow movement.  
**Source:** `legs.gon`  

```
300 { //Frog legs
        tag animal
        desc "MUTATION_LEGS_300_DESC"

        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    AddMovement 1
                }
            }

            WaterWalk 1
        }
    }
```

---

### `301`
**Name:** Hooves  
**Description:** Your basic attack has a 5% chance to Stun.  
**Source:** `legs.gon`  

```
301 { //Hooves
        tag animal
        desc "MUTATION_LEGS_301_DESC"

        spd 1
        passives {
            AddStatusToBasicAttack {
                Stun [1, .05]
            }
        }
    }
```

---

### `302`
**Name:** Tentacles  
**Description:** Knockback immunity.  
**Source:** `legs.gon`  

```
302 { //Tentacles
        tag animal
        desc "MUTATION_LEGS_302_DESC"

        passives {
            KnockbackImmunity 1
        }
    }
```

---

### `303`
**Name:** Lobster Claws  
**Description:** Your basic attack has a 5% chance to Immobilize.  
**Source:** `legs.gon`  

```
303 { //Lobster Claws
        tag animal
        desc "MUTATION_LEGS_303_DESC"

        passives {
            AddStatusToBasicAttack {
                Immobile [1, .05]
            }
        }
    }
```

---

### `304`
**Name:** Muscular Legs  
**Source:** `legs.gon`  

```
304 { //Muscular Legs
        str 1
    }
```

---

### `305`
**Name:** Tar Legs  
**Description:** +5% dodge chance.  
**Source:** `legs.gon`  

```
305 { //Tar Legs
        desc "MUTATION_LEGS_305_DESC"

        passives {
            DodgeChance 5%
        }
    }
```

---

### `306`
**Name:** Bug Legs  
**Source:** `legs.gon`  

```
306 { //Bug Legs
        tag animal
        dex 1
    }
```

---

### `307`
**Name:** Tires  
**Source:** `legs.gon`  

```
307 { //Tires
        spd 1
    }
```

---

### `308`
**Name:** Human Legs  
**Source:** `legs.gon`  

```
308 { //Human Legs
        lck 1
    }
```

---

### `309`
**Name:** Knife Legs  
**Description:** Your basic attack has a 10% chance to inflict Bleed 3.  
**Source:** `legs.gon`  

```
309 { //Knife Legs
        desc "MUTATION_LEGS_309_DESC"

        passives {
            AddStatusToBasicAttack {
                Bleed [3, .1]
            }
        }
    }
```

---

### `310`
**Name:** Spring Legs  
**Description:** Your movement action is a jump.  
**Source:** `legs.gon`  

```
310 { //Spring Legs
        desc "MUTATION_LEGS_310_DESC" 
        override_move BasicJump
    }
```

---

### `311`
**Name:** Square Legs  
**Source:** `legs.gon`  

```
311 { //Square Legs
        con 1
    }
```

---

### `312`
**Name:** Balloon Legs  
**Description:** Your basic attack has +1 Knockback.  
**Source:** `legs.gon`  

```
312 { //Balloon Legs
        desc "MUTATION_LEGS_312_DESC" 

        passives {
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }
```

---

### `313`
**Name:** Snake Legs  
**Description:** +1 reach.  
**Source:** `legs.gon`  

```
313 { //Snake Legs
        desc "MUTATION_LEGS_313_DESC"
        passives { 
            AddBonusMeleeRange 1 
        }
    }
```

---

### `314`
**Name:** Weapon Legs  
**Description:** Your weapons have +1 Damage.  
**Source:** `legs.gon`  

```
314 { //Weapon Legs
        desc "MUTATION_LEGS_314_DESC"
        passives {
            BoostWeaponDamage 1
        }
    }
```

---

### `315`
**Name:** Socks  
**Description:** Ice immunity.  
**Source:** `legs.gon`  

```
315 { //Socks
        desc "MUTATION_LEGS_315_DESC"
        passives {
            ElementImmune Ice
        }
    }
```

---

### `316`
**Name:** Hook legs  
**Source:** `legs.gon`  

```
316 { //Hook legs 
//        passives {
//            MakeBasicAttackPull 1 
//        }  
//    }
```

---

### `317`
**Name:** Raptor Claws  
**Description:** Your basic attack inflicts Bleed 1 if it's melee.  
**Source:** `legs.gon`  

```
317 { //Raptor Claws
        desc "MUTATION_LEGS_317_DESC"
        passives {
            AddStatusToBasicMeleeAttack {
                Bleed 1
            }
        }
    }
```

---

### `318`
**Name:** Stigmata  
**Source:** `legs.gon`  

```
318 { //Stigmata
        divine_shield 1
    }
```

---

### `319`
**Name:** High Tops  
**Description:** 10% chance to gain a bonus move each turn.  
**Source:** `legs.gon`  

```
319 { //High Tops
        desc "MUTATION_LEGS_319_DESC"

        passives {
            StatusEachTurnBegin {
                MoveQuivered [1, 0.1]
            }
        }
    }
```

---

### `320`
**Name:** Talons  
**Description:** 10% chance to gain a bonus attack each turn.  
**Source:** `legs.gon`  

```
320 { //Talons
        desc "MUTATION_LEGS_320_DESC"

        passives { 
            StatusEachTurnBegin {
                Quivered [1, 0.1]
            }  
        }
    }
```

---

### `321`
**Name:** Flippers  
**Description:** Moving through water tiles costs 0 movement.  
**Source:** `legs.gon`  

```
321 { //Flippers
        desc "MUTATION_LEGS_321_DESC"

        passives {
            FreePathfindElement Water
        }
    }
```

---

### `322`
**Name:** Bear Claws  
**Source:** `legs.gon`  

```
322 { //Bear Claws 
		str 1
		con 1
    }
```

---

### `323`
**Name:** Beetle Feet  
**Source:** `legs.gon`  

```
323 { //Beetle Feet
        spd 2
    }
```

---

### `324`
**Name:** Branches  
**Source:** `legs.gon`  

```
324 { //Branches 
        con 1
    }
```

---

### `325`
**Name:** Extra Head  
**Description:** Collarless spells cost -1 mana.  
**Source:** `legs.gon`  

```
325 { //Extra Head
        desc "MUTATION_LEGS_325_DESC"
        tag extra
        spd -2

        passives {
            ClassManaCostReduction {
                class Colorless
                reduction 1
            }
        }
    }
```

---

### `326`
**Name:** Needle Feet  
**Description:** Your basic attack inflicts a random debuff.  
**Source:** `legs.gon`  

```
326 { //Needle Feet
        desc "MUTATION_LEGS_326_DESC"
        passives { 
            AddStatusToBasicAttack {
                RandomStatusFromPool {
                    Poison 1
                    Burn 1
                    Bleed 1
                    Blind 1 
                    Weakness 1 
                }
            } 
        }
    }
```

---

### `327`
**Name:** Mushroom Legs  
**Description:** Gain 2 random stat ups and 1 random stat down at the end of each turn.  
**Source:** `legs.gon`  

```
327 { //Mushroom Legs 
        desc "MUTATION_LEGS_327_DESC"
        passives {
           StatusEachTurnEnd {
               RandomStatUp 2
               RandomStatDown 1
           }
        }
    }
```

---

### `328`
**Name:** Glass Bottle  
**Description:** Equip a temporary Bottles weapon at the start of the battle.  
**Source:** `legs.gon`  

```
328 { //Glass Bottle 
        desc "MUTATION_LEGS_328_DESC"
        passives {
            EquipTemporaryItem Bottles
        }
    }
```

---

### `329`
**Name:** Water Bottle  
**Description:** Equip a temporary Water Bottle trinket at the start of the battle.  
**Source:** `legs.gon`  

```
329 { //Water Bottle 
        desc "MUTATION_LEGS_329_DESC"
        passives {
            EquipTemporaryItem WaterBottle_Full
        }
    }
```

---

### `330`
**Name:** Sausage Legs  
**Description:** +1 Health Regeneration  
**Source:** `legs.gon`  

```
330 { //Sausage Legs 
        desc "MUTATION_LEGS_330_DESC"
        
        passives {
            HealthRegenUp 1
        }
    }
```

---

### `331`
**Name:** Jet Legs  
**Description:** +1 movement range. Your movement action is a jump.  
**Source:** `legs.gon`  

```
331 { //Jet Legs 
        desc "MUTATION_LEGS_331_DESC"
        override_move BasicJump
        passives {
           AddMovement 1
        }
    }
```

---

### `332`
**Name:** Peg Legs  
**Description:** 50% chance to spawn a pickup on an adjacent tile when you end your turn.  
**Source:** `legs.gon`  

```
332 { //Peg Legs 
        desc "MUTATION_LEGS_332_DESC"
        spd -1
        passives {
            SpawnEachTurn {
                object RandomPickup
                chance 50%
            }  
        } 
    }
```

---

### `333`
**Name:** Wing Legs  
**Description:** Your basic attack has wind element and +1 Knockback.  
**Source:** `legs.gon`  

```
333 { //Wing Legs 
        desc "MUTATION_LEGS_333_DESC"
        passives {
            AddStatusToBasicAttack {
                Knockback 1
                VisualFXTile fx_windSpell
            }
            AddElementsToBasicAttack Wind
        }
    }
```

---

### `334`
**Name:** Ape Legs  
**Description:** Your basic attack tosses units into the air if it's melee.  
**Source:** `legs.gon`  

```
334 { //Ape Legs 
        desc "MUTATION_LEGS_334_DESC"
        str 1
        passives {
           AddStatusToBasicMeleeAttack { 
               KnockUpAndAway {
                   stacks 3
                   distance 3
               }
           }
        }
    }
```

---

### `335`
**Name:** Glass Legs  
**Description:** +1 Bleed Thorns. Spawn glass when you take damage.  
**Source:** `legs.gon`  

```
335 { //Glass Legs 
        desc "MUTATION_LEGS_335_DESC"
        
        passives {
            BleedThorns 1 
            StatusOnTookDamage {
                ChangeTilesUnder GlassTile 
            }
        } 
    }
```

---

### `336`
**Name:** Crow Legs  
**Description:** Your basic attack inflicts Soul Link.  
**Source:** `legs.gon`  

```
336 { //Crow Legs 
        desc "MUTATION_LEGS_336_DESC"
        tag bird

        passives {
            AddStatusToBasicAttack {
                SoulLink 1
            } 
        }
    }
```

---

### `337`
**Name:** Floating Legs  
**Description:** You are immune to tile effects.  
**Source:** `legs.gon`  

```
337 { //Floating Legs 
        desc "MUTATION_LEGS_337_DESC"
        passives {
            IgnoreTiles 1
        }
    }
```

---

### `339`
**Name:** Wing Legs 2  
**Description:** Fly away when hit.  
**Source:** `legs.gon`  

```
339 { //Wing Legs 2 
        desc "MUTATION_LEGS_339_DESC"
        tag bird
        
        spd 2
        passives { 
            MoveAwayFromDamageSource BasicJump
        }
    }
```

---

### `340`
**Name:** Lucky Toe  
**Description:** When you take damage, gain +1 [img:lck].  
**Source:** `legs.gon`  

```
340 { //Lucky Toe 
        desc "MUTATION_LEGS_340_DESC"
        passives {
           StatusOnTookDamage {
               LuckUp 1
           }
        }
    }
```

---

### `341`
**Name:** Whip Legs  
**Description:** Your basic attack makes units face away from you.  
**Source:** `legs.gon`  

```
341 { //Whip Legs 
        desc "MUTATION_LEGS_341_DESC"
        passives {
            AddStatusToBasicAttack { 
                FaceAway 1
            }
        }
    }
```

---

### `343`
**Name:** Kitten Legs  
**Description:** Spawn a Charmed Kitten familiar when you get downed.  
**Source:** `legs.gon`  

```
343 { //Kitten Legs 
        desc "MUTATION_LEGS_343_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }
```

---

### `754`
**Name:** Wing Hoof Legs  
**Description:** Your movement action is a jump. Your basic attack inflicts Bruise.  
**Source:** `legs.gon`  

```
754 { //Wing Hoof Legs 
        desc "MUTATION_LEGS_754_DESC"  
        passives {
            ReplaceBasicMove ToadJump_BasicMove
		    AddStatusToBasicAttack {
                Bruise 1
            }	
        }
    }
```

---

### `756`
**Name:** Sonichu Legs  
**Source:** `legs.gon`  

```
756 { //Sonichu Legs 
		spd 2
    }
```

---

### `757`
**Name:** bigfoot Legs  
**Description:** Trample.  
**Source:** `legs.gon`  

```
757 { //bigfoot Legs 
        desc "MUTATION_LEGS_757_DESC"  
        passives {
			Trample 3
        }
    }
```

---

### `758`
**Name:** nessie Legs  
**Description:** You have All Stats Up while wet.  
**Source:** `legs.gon`  

```
758 { //nessie Legs 
        desc "MUTATION_LEGS_758_DESC"  
        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    AllStatsUp 1
                }
            }  
        }
    }
```

---

### `759`
**Name:** nessie Legs  
**Description:** You have All Stats Up while wet.  
**Source:** `legs.gon`  

```
759 { //nessie Legs 
        desc "MUTATION_LEGS_759_DESC"  
        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    AllStatsUp 1
                }
            }  
        }
    }
```

---

### `761`
**Name:** mothman Legs  
**Description:** Your movement action is a jump. Your basic attack inflicts Bleed.  
**Source:** `legs.gon`  

```
761 { //mothman Legs 
        desc "MUTATION_LEGS_761_DESC"  
        passives {
            ReplaceBasicMove ToadJump_BasicMove
		    AddStatusToBasicAttack {
                Bleed 1
            }	
        }
    }
```

---

### `762`
**Name:** slender  
**Description:** Ignore the effects of tiles and traps.  
**Source:** `legs.gon`  

```
762 { //slender
        desc "MUTATION_LEGS_762_DESC"

        passives {
            IgnoreTiles 1
            YOffset .25
        }
    }
```

---

### `763`
**Name:** slender  
**Description:** Ignore the effects of tiles and traps.  
**Source:** `legs.gon`  

```
763 { //slender
        desc "MUTATION_LEGS_763_DESC"

        passives {
            IgnoreTiles 1
            YOffset .25
        }
    }
```

---

### `900`
**Name:** slender  
**Description:** Ignore the effects of tiles and traps.  
**Source:** `legs.gon`  

```
900 { //slender
        desc "MUTATION_LEGS_900_DESC"

        passives {
            IgnoreTiles 1
            YOffset .25
        }
    }
```

---

### `400`
**Source:** `legs.gon`  

```
400 {
        tag common
        str 2
        con -1
    }
```

---

### `401`
**Source:** `legs.gon`  

```
401 {
        tag common
        str 2
        dex -1
    }
```

---

### `402`
**Source:** `legs.gon`  

```
402 {
        tag common
        str 2
        cha -1
    }
```

---

### `403`
**Source:** `legs.gon`  

```
403 {
        tag common
        str 2
        int -1
    }
```

---

### `404`
**Source:** `legs.gon`  

```
404 {
        tag common
        str 2
        spd -1
    }
```

---

### `405`
**Source:** `legs.gon`  

```
405 {
        tag common
        str 2
        lck -1
    }
```

---

### `406`
**Source:** `legs.gon`  

```
406 {
        tag common
        con 2
        str -1
    }
```

---

### `407`
**Source:** `legs.gon`  

```
407 {
        tag common
        con 2
        dex -1
    }
```

---

### `408`
**Source:** `legs.gon`  

```
408 {
        tag common
        con 2
        cha -1
    }
```

---

### `409`
**Source:** `legs.gon`  

```
409 {
        tag common
        con 2
        int -1
    }
```

---

### `410`
**Source:** `legs.gon`  

```
410 {
        tag common
        con 2
        spd -1
    }
```

---

### `411`
**Source:** `legs.gon`  

```
411 {
        tag common
        con 2
        lck -1
    }
```

---

### `412`
**Source:** `legs.gon`  

```
412 {
        tag common
        dex 2
        con -1
    }
```

---

### `413`
**Source:** `legs.gon`  

```
413 {
        tag common
        dex 2
        str -1
    }
```

---

### `414`
**Source:** `legs.gon`  

```
414 {
        tag common
        dex 2
        cha -1
    }
```

---

### `415`
**Source:** `legs.gon`  

```
415 {
        tag common
        dex 2
        int -1
    }
```

---

### `416`
**Source:** `legs.gon`  

```
416 {
        tag common
        dex 2
        spd -1
    }
```

---

### `417`
**Source:** `legs.gon`  

```
417 {
        tag common
        dex 2
        lck -1
    }
```

---

### `418`
**Source:** `legs.gon`  

```
418 {
        tag common
        int 2
        con -1
    }
```

---

### `419`
**Source:** `legs.gon`  

```
419 {
        tag common
        int 2
        dex -1
    }
```

---

### `420`
**Source:** `legs.gon`  

```
420 {
        tag common
        int 2
        cha -1
    }
```

---

### `421`
**Source:** `legs.gon`  

```
421 {
        tag common
        int 2
        str -1
    }
```

---

### `422`
**Source:** `legs.gon`  

```
422 {
        tag common
        int 2
        spd -1
    }
```

---

### `423`
**Source:** `legs.gon`  

```
423 {
        tag common
        int 2
        lck -1
    }
```

---

### `424`
**Source:** `legs.gon`  

```
424 {
        tag common
        cha 2
        con -1
    }
```

---

### `425`
**Source:** `legs.gon`  

```
425 {
        tag common
        cha 2
        dex -1
    }
```

---

### `426`
**Source:** `legs.gon`  

```
426 {
        tag common
        cha 2
        str -1
    }
```

---

### `427`
**Source:** `legs.gon`  

```
427 {
        tag common
        cha 2
        int -1
    }
```

---

### `428`
**Source:** `legs.gon`  

```
428 {
        tag common
        cha 2
        spd -1
    }
```

---

### `429`
**Source:** `legs.gon`  

```
429 {
        tag common
        cha 2
        lck -1
    }
```

---

### `430`
**Source:** `legs.gon`  

```
430 {
        tag common
        lck 2
        con -1
    }
```

---

### `431`
**Source:** `legs.gon`  

```
431 {
        tag common
        lck 2
        dex -1
    }
```

---

### `432`
**Source:** `legs.gon`  

```
432 {
        tag common
        lck 2
        cha -1
    }
```

---

### `433`
**Source:** `legs.gon`  

```
433 {
        tag common
        lck 2
        int -1
    }
```

---

### `434`
**Source:** `legs.gon`  

```
434 {
        tag common
        lck 2
        spd -1
    }
```

---

### `435`
**Source:** `legs.gon`  

```
435 {
        tag common
        lck 2
        str -1
    }
```

---

### `436`
**Source:** `legs.gon`  

```
436 {
        tag common
        spd 2
        con -1
    }
```

---

### `437`
**Source:** `legs.gon`  

```
437 {
        tag common
        spd 2
        str -1
    }
```

---

### `438`
**Source:** `legs.gon`  

```
438 {
        tag common
        spd 2
        cha -1
    }
```

---

### `439`
**Source:** `legs.gon`  

```
439 {
        tag common
        spd 2
        int -1
    }
```

---

### `440`
**Source:** `legs.gon`  

```
440 {
        tag common
        spd 2
        dex -1
    }
```

---

### `441`
**Source:** `legs.gon`  

```
441 {
        tag common
        spd 2
        lck -1
    }
```

---

### `700`
**Name:** lobster claw  
**Source:** `legs.gon`  

```
700 { //lobster claw
        tag birth_defect
        str -2
    }
```

---

### `701`
**Name:** extra finger  
**Source:** `legs.gon`  

```
701 { //extra finger
        tag birth_defect
        dex -2
    }
```

---

### `702`
**Name:** club foot  
**Source:** `legs.gon`  

```
702 { //club foot
        tag birth_defect
        spd -2
    }
```

---

### `703`
**Name:** syndactyly  
**Description:** Water does not slow movement.  
**Source:** `legs.gon`  

```
703 { //syndactyly
        desc "MUTATION_LEGS_703_DESC"

        tag birth_defect
        spd -2

        passives {
            WaterWalk 1
        }
    }
```

---

### `704`
**Name:** curled paw  
**Source:** `legs.gon`  

```
704 { //curled paw
        tag birth_defect
        str -1
    }
```

---

### `705`
**Name:** club foot2  
**Description:** Trample.  
**Source:** `legs.gon`  

```
705 { //club foot2
        desc "MUTATION_LEGS_705_DESC"
        tag birth_defect
        speed -4 
        passives {
            Trample 3
        }
    }
```

---

### `706`
**Name:** backwards knees  
**Source:** `legs.gon`  

```
706 { //backwards knees
        tag birth_defect
        spd -1
    }
```

---

### `707`
**Name:** blob legs  
**Description:** Permanently Slow.  
**Source:** `legs.gon`  

```
707 { //blob legs
        desc "MUTATION_LEGS_707_DESC"
        tag birth_defect
        str 1

        passives {
            Slow -1
        }
    }
```

---

## Mouth Mutations

### `300`
**Name:** Sabertoothed  
**Source:** `mouth.gon`  

```
300 { //Sabertoothed  
        tag animal
        str 1
    }
```

---

### `301`
**Name:** Hippo Teeth  
**Description:** Gain 1 health when you deal damage.  
**Source:** `mouth.gon`  

```
301 { //Hippo Teeth
        tag animal
        desc "MUTATION_MOUTH_301_DESC"

        passives {
            FlatHealWhenDealDamage 1
        }
    }
```

---

### `302`
**Name:** Flesh Kid  
**Description:** +1 Health Regeneration  
**Source:** `mouth.gon`  

```
302 { //Flesh Kid  
        desc "MUTATION_MOUTH_302_DESC"        

        passives {
            HealthRegenUp 1
        }
    }
```

---

### `303`
**Name:** Delerious  
**Source:** `mouth.gon`  

```
303 { //Delerious  
        tag melted
        int 1
    }
```

---

### `304`
**Name:** Spider  
**Description:** Your basic attack inflicts Poison.  
**Source:** `mouth.gon`  

```
304 { //Spider
        tag animal  
        desc "MUTATION_MOUTH_304_DESC"

        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }
```

---

### `305`
**Name:** Ash  
**Description:** +100 corpse health.  
**Source:** `mouth.gon`  

```
305 { //Ash  
        desc "MUTATION_MOUTH_305_DESC"
        passives {
            AddCorpseHealth 100
        }
    }
```

---

### `306`
**Name:** Famine  
**Description:** 10% chance to spawn a Fly when you take damage.  
**Source:** `mouth.gon`  

```
306 { //Famine  
        desc "MUTATION_MOUTH_306_DESC"

        passives {
            SpawnThingOnDamage {
                object Fly
                good false //good relative to the thing attacking, for luck calculations
                chance 10%
            }
        }
    }
```

---

### `307`
**Name:** Alien Chomp  
**Description:** Your basic attack has a 1% chance to instakill.  
**Source:** `mouth.gon`  

```
307 { //Alien Chomp  
        desc "MUTATION_MOUTH_307_DESC"

        passives {
            AddStatusToBasicAttack {
                Instakill [25, .01]
            }
        }
    }
```

---

### `308`
**Name:** Licky  
**Description:** +1 Health Regeneration  
**Source:** `mouth.gon`  

```
308 { //Licky  
        desc "MUTATION_MOUTH_308_DESC"

        passives {
            HealthRegenUp 1
        }
    }
```

---

### `309`
**Name:** Jacko  
**Description:** Your basic attack has a 10% chance to inflict Fear.  
**Source:** `mouth.gon`  

```
309 { //Jacko  
        desc "MUTATION_MOUTH_309_DESC"

        passives {
            AddStatusToBasicAttack {
                Fear [1 .1]
            }
        }
    }
```

---

### `310`
**Name:** Lip Fillers  
**Source:** `mouth.gon`  

```
310 { //Lip Fillers 
        cha 1
    }
```

---

### `311`
**Name:** Leech Mouth  
**Description:** Your basic attack inflicts Leech 1.  
**Source:** `mouth.gon`  

```
311 { //Leech Mouth
        desc "MUTATION_MOUTH_311_DESC"

        passives {
            AddStatusToBasicAttack {
                Leeches 1
            }
        }
    }
```

---

### `312`
**Name:** Bear Trap Mouth  
**Description:** Your basic attack has a 10% chance to inflict Immobile if it's melee.  
**Source:** `mouth.gon`  

```
312 { //Bear Trap Mouth
        desc "MUTATION_MOUTH_312_DESC"
        str 1
        passives {
            AddStatusToBasicMeleeAttack {
                Immobile [1, .1]
            }
        }
    }
```

---

### `313`
**Name:** Full Mouth  
**Description:** At the end of each round, spit at an enemy .  
**Source:** `mouth.gon`  

```
313 { //Full Mouth
         desc "MUTATION_MOUTH_313_DESC"

         passives {
             StatusEachRoundEnd {
                UseAbility Spit
             }
         }
    }
```

---

### `314`
**Name:** Gold Tooth  
**Description:** Spawn 5-10 coins when downed.  
**Source:** `mouth.gon`  

```
314 { //Gold Tooth
         desc "MUTATION_MOUTH_314_DESC"

         passives {
             StatusOnDie {
                 ScatterCoins 5
                 ScatterCoins [1 .5]
                 ScatterCoins [1 .5]
                 ScatterCoins [1 .5]
                 ScatterCoins [1 .5]
                 ScatterCoins [1 .5]
             }
         }
    }
```

---

### `315`
**Name:** Double Mouth  
**Description:** 10% chance to gain a bonus attack each turn.  
**Source:** `mouth.gon`  

```
315 { //Double Mouth
        desc "MUTATION_MOUTH_315_DESC"

        passives { 
            StatusEachTurnBegin {
                Quivered [1, 0.1]
            }  
        }
    }
```

---

### `316`
**Name:** Horse Face  
**Description:** Your basic attack inflicts Bruise.  
**Source:** `mouth.gon`  

```
316 { //Horse Face
         desc "MUTATION_MOUTH_316_DESC"
         cha -1
         passives{
            AddStatusToBasicAttack {
                Bruise 1
            }
         }
    }
```

---

### `317`
**Name:** Glass Teeth  
**Description:** Spawn glass when you take damage. +1 Bleed Thorns.  
**Source:** `mouth.gon`  

```
317 { //Glass Teeth
        desc "MUTATION_MOUTH_317_DESC"
        passives {   
            BleedThorns 1 
            StatusOnTookDamage {
                ChangeTilesUnder GlassTile 
            }
        } 
    }
```

---

### `318`
**Name:** mole mouth  
**Description:** Your movement action is Dig.  
**Source:** `mouth.gon`  

```
318 { //mole mouth
        desc "MUTATION_MOUTH_318_DESC"
        passives {
            ReplaceBasicMove_Mutation BasicDig
        }
    }
```

---

### `319`
**Name:** Catfish Mouth  
**Description:** Water does not slow movement. +1 Health Regeneration while wet.  
**Source:** `mouth.gon`  

```
319 { //Catfish Mouth
        desc "MUTATION_MOUTH_319_DESC"
        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    HealthRegenUp 1 
                }
            } 
            WaterWalk 1
        }
    }
```

---

### `320`
**Name:** Bird Beak  
**Description:** Double the odds of birds appearing.  
**Source:** `mouth.gon`  

```
320 { //Bird Beak
//        desc "Double the odds of birds appearing."
//   }
```

---

### `321`
**Name:** Zipper Mouth  
**Source:** `mouth.gon`  

```
321 { //Zipper Mouth 
         shield 3
    }
```

---

### `322`
**Name:** Shark Mouth  
**Description:** Your basic attack inflicts Bleed.  
**Source:** `mouth.gon`  

```
322 { //Shark Mouth
        desc "MUTATION_MOUTH_322_DESC"
        passives{
            AddStatusToBasicAttack {
                Bleed 1
            }
        }
    }
```

---

### `323`
**Name:** Gills  
**Description:** +2 Health Regeneration while wet.  
**Source:** `mouth.gon`  

```
323 { //Gills
        desc "MUTATION_MOUTH_323_DESC"
        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    HealthRegenUp 2 
                }
            }  
        }
    }
```

---

### `324`
**Name:** Eyeball  
**Description:** +1 range.  
**Source:** `mouth.gon`  

```
324 { //Eyeball
        desc "MUTATION_MOUTH_324_DESC"      
        passives {
            AddBonusRange 1
        }
    }
```

---

### `325`
**Name:** Wide Mouth  
**Description:** Your melee attack hits 3 tiles in front of you  
**Source:** `mouth.gon`  

```
325 { //Wide Mouth
//         desc "Your melee attack hits 3 tiles in front of you"
//    }
```

---

### `326`
**Name:** Double Mouth 2  
**Description:** Gain +1 Health Regeneration whenever you eat food.  
**Source:** `mouth.gon`  

```
326 { //Double Mouth 2
        desc "MUTATION_MOUTH_326_DESC"
        passives { 
            StatusOnEatFood {
                HealthRegenUp 1 
            }
        }
    }
```

---

### `327`
**Name:** Clown Lips  
**Description:** You can reroll your options when you level up.  
**Source:** `mouth.gon`  

```
327 { //Clown Lips
        desc "MUTATION_MOUTH_327_DESC"
        passives { 
            AddLevelUpRerolls 1
        }
    }
```

---

### `328`
**Name:** Bandage Mouth  
**Description:** Can't eat food, use consumables, or use musical abilities. +2 Health Regeneration  
**Source:** `mouth.gon`  

```
328 { //Bandage Mouth
        desc "MUTATION_MOUTH_328_DESC"
        passives { 
            HealthRegenUp 2

            Vegan 1
            HouseFoodRequirementMultiplier 0
            DisableAbilitiesWithTag consumable
            DisableAbilitiesWithTag musical
            BlacklistPickupType food
            BlacklistPickupType catnip
        }
    }
```

---

### `750`
**Name:** beaver teeth  
**Description:** Your basic attack destroys inanimate objects and turns tiles into dirt.  
**Source:** `mouth.gon`  

```
750 { //beaver teeth
        desc "MUTATION_MOUTH_750_DESC"
        passives { 
			AddStatusToBasicAttack {
                ChangeTile DirtTile
				VaporizeInanimate 1
            }	
        }
    }
```

---

### `751`
**Name:** pig snout  
**Source:** `mouth.gon`  

```
751 { //pig snout
		con 2
    }
```

---

### `752`
**Name:** Dog tongue  
**Description:** Your basic attack creates water tiles.  
**Source:** `mouth.gon`  

```
752 { //Dog tongue
        desc "MUTATION_MOUTH_752_DESC"
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        } 
    }
```

---

### `754`
**Name:** Isaacs mouth  
**Description:** Adjacent units get All Stats Down.  
**Source:** `mouth.gon`  

```
754 { //Isaacs mouth
        desc "MUTATION_MOUTH_754_DESC"
		passives {
			DepressionAura 1
		}
    }
```

---

### `755`
**Name:** Edmund beard  
**Description:** Ice Immunity.  
**Source:** `mouth.gon`  

```
755 { //Edmund beard
        desc "MUTATION_MOUTH_755_DESC"
		passives {
			ElementImmune Ice
		}
    }
```

---

### `756`
**Name:** Tylers beard  
**Source:** `mouth.gon`  

```
756 { //Tylers beard
		int 1
    }
```

---

### `757`
**Name:** Mermaid mouth  
**Description:** Your basic attack inflicts Bleed.  
**Source:** `mouth.gon`  

```
757 { //Mermaid mouth
        desc "MUTATION_MOUTH_757_DESC"
		passives {
			AddStatusToBasicAttack {
				Bleed 1
			}
		}
    }
```

---

### `760`
**Name:** bigfoot mouth  
**Description:** When a food pickup spawns within 2 tiles of you, move to it.  
**Source:** `mouth.gon`  

```
760 { //bigfoot mouth
        desc "MUTATION_MOUTH_760_DESC"
        passives {
            AbilityWhenTaggedCharacterMovesNear {
                ability move
                tag food
                range 2
            }
        }
    }
```

---

### `900`
**Name:** Slender  
**Description:** Your basic attack has a 10% chance to inflict Fear.  
**Source:** `mouth.gon`  

```
900 { //Slender
        desc "MUTATION_MOUTH_900_DESC"

        passives {
            AddStatusToBasicAttack {
                Fear [1 .1]
            }
        }
    }
```

---

### `1500`
**Name:** rat mouth  
**Description:** Your basic attack inflicts Poison.  
**Source:** `mouth.gon`  

```
1500 { //rat mouth
        tag animal
        desc "MUTATION_MOUTH_1500_DESC"

        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }
```

---

### `1026`
**Name:** spider mouth  
**Description:** Your basic attack has a 10% chance to inflict Webbed.  
**Source:** `mouth.gon`  

```
1026 { //spider mouth
        tag animal
        desc "MUTATION_MOUTH_1026_DESC"

        passives {
            AddStatusToBasicAttack {
                Webbed [1 .1]
            }
        }
    }
```

---

### `400`
**Source:** `mouth.gon`  

```
400 {
        tag common
        str 2
        con -1
    }
```

---

### `401`
**Source:** `mouth.gon`  

```
401 {
        tag common
        str 2
        dex -1
    }
```

---

### `402`
**Source:** `mouth.gon`  

```
402 {
        tag common
        str 2
        cha -1
    }
```

---

### `403`
**Source:** `mouth.gon`  

```
403 {
        tag common
        str 2
        int -1
    }
```

---

### `404`
**Source:** `mouth.gon`  

```
404 {
        tag common
        str 2
        spd -1
    }
```

---

### `405`
**Source:** `mouth.gon`  

```
405 {
        tag common
        str 2
        lck -1
    }
```

---

### `406`
**Source:** `mouth.gon`  

```
406 {
        tag common
        con 2
        str -1
    }
```

---

### `407`
**Source:** `mouth.gon`  

```
407 {
        tag common
        con 2
        dex -1
    }
```

---

### `408`
**Source:** `mouth.gon`  

```
408 {
        tag common
        con 2
        cha -1
    }
```

---

### `409`
**Source:** `mouth.gon`  

```
409 {
        tag common
        con 2
        int -1
    }
```

---

### `410`
**Source:** `mouth.gon`  

```
410 {
        tag common
        con 2
        spd -1
    }
```

---

### `411`
**Source:** `mouth.gon`  

```
411 {
        tag common
        con 2
        lck -1
    }
```

---

### `412`
**Source:** `mouth.gon`  

```
412 {
        tag common
        dex 2
        con -1
    }
```

---

### `413`
**Source:** `mouth.gon`  

```
413 {
        tag common
        dex 2
        str -1
    }
```

---

### `414`
**Source:** `mouth.gon`  

```
414 {
        tag common
        dex 2
        cha -1
    }
```

---

### `415`
**Source:** `mouth.gon`  

```
415 {
        tag common
        dex 2
        int -1
    }
```

---

### `416`
**Source:** `mouth.gon`  

```
416 {
        tag common
        dex 2
        spd -1
    }
```

---

### `417`
**Source:** `mouth.gon`  

```
417 {
        tag common
        dex 2
        lck -1
    }
```

---

### `418`
**Source:** `mouth.gon`  

```
418 {
        tag common
        int 2
        con -1
    }
```

---

### `419`
**Source:** `mouth.gon`  

```
419 {
        tag common
        int 2
        dex -1
    }
```

---

### `420`
**Source:** `mouth.gon`  

```
420 {
        tag common
        int 2
        cha -1
    }
```

---

### `421`
**Source:** `mouth.gon`  

```
421 {
        tag common
        int 2
        str -1
    }
```

---

### `422`
**Source:** `mouth.gon`  

```
422 {
        tag common
        int 2
        spd -1
    }
```

---

### `423`
**Source:** `mouth.gon`  

```
423 {
        tag common
        int 2
        lck -1
    }
```

---

### `424`
**Source:** `mouth.gon`  

```
424 {
        tag common
        cha 2
        con -1
    }
```

---

### `425`
**Source:** `mouth.gon`  

```
425 {
        tag common
        cha 2
        dex -1
    }
```

---

### `426`
**Source:** `mouth.gon`  

```
426 {
        tag common
        cha 2
        str -1
    }
```

---

### `427`
**Source:** `mouth.gon`  

```
427 {
        tag common
        cha 2
        int -1
    }
```

---

### `428`
**Source:** `mouth.gon`  

```
428 {
        tag common
        cha 2
        spd -1
    }
```

---

### `429`
**Source:** `mouth.gon`  

```
429 {
        tag common
        cha 2
        lck -1
    }
```

---

### `430`
**Source:** `mouth.gon`  

```
430 {
        tag common
        lck 2
        con -1
    }
```

---

### `431`
**Source:** `mouth.gon`  

```
431 {
        tag common
        lck 2
        dex -1
    }
```

---

### `432`
**Source:** `mouth.gon`  

```
432 {
        tag common
        lck 2
        cha -1
    }
```

---

### `433`
**Source:** `mouth.gon`  

```
433 {
        tag common
        lck 2
        int -1
    }
```

---

### `434`
**Source:** `mouth.gon`  

```
434 {
        tag common
        lck 2
        spd -1
    }
```

---

### `435`
**Source:** `mouth.gon`  

```
435 {
        tag common
        lck 2
        str -1
    }
```

---

### `436`
**Source:** `mouth.gon`  

```
436 {
        tag common
        spd 2
        con -1
    }
```

---

### `437`
**Source:** `mouth.gon`  

```
437 {
        tag common
        spd 2
        str -1
    }
```

---

### `438`
**Source:** `mouth.gon`  

```
438 {
        tag common
        spd 2
        cha -1
    }
```

---

### `439`
**Source:** `mouth.gon`  

```
439 {
        tag common
        spd 2
        int -1
    }
```

---

### `440`
**Source:** `mouth.gon`  

```
440 {
        tag common
        spd 2
        dex -1
    }
```

---

### `441`
**Source:** `mouth.gon`  

```
441 {
        tag common
        spd 2
        lck -1
    }
```

---

### `700`
**Name:** cleft pallet  
**Source:** `mouth.gon`  

```
700 { //cleft pallet
        tag birth_defect
        cha -2
    }
```

---

### `701`
**Name:** anodontia  
**Source:** `mouth.gon`  

```
701 { //anodontia
        tag birth_defect
        str -1
        dex -1
    }
```

---

### `2`
**Name:** no mouth (frame 702)  
**Description:** Can't eat food, use consumables, or use musical abilities.  
**Source:** `mouth.gon`  

```
2 { //no mouth (frame 702)
        desc "MUTATION_MOUTH_M2_DESC"
        tag birth_defect
        
        passives {
            Vegan 1
            HouseFoodRequirementMultiplier 0
            DisableAbilitiesWithTag consumable
            DisableAbilitiesWithTag musical
            BlacklistPickupType food
            BlacklistPickupType catnip
        }
    }
```

---

### `703`
**Name:** underbite  
**Source:** `mouth.gon`  

```
703 { //underbite
        tag birth_defect
        int -2
		con 1
    }
```

---

### `704`
**Name:** overbite  
**Source:** `mouth.gon`  

```
704 { //overbite
        tag birth_defect
        cha -2
		str 1
    }
```

---

### `705`
**Name:** Fetus Mouth  
**Description:** Your basic attack can be used two extra times each turn but is replaced with a 1-damage spit attack.  
**Source:** `mouth.gon`  

```
705 { // Fetus Mouth
        desc "MUTATION_MOUTH_705_DESC"

        attack FetusSpit
        passives {
            ExtraBasicAttacks 2
            ReplaceBasicAttack_Mutation FetusSpit
        }
    }
```

---

## Tail Mutations

### `300`
**Name:** Extra Paw  
**Source:** `tail.gon`  

```
300 { //Extra Paw
        tag extra    
        str 1
    }
```

---

### `301`
**Name:** Turtle Head  
**Description:** Poop when you take damage.  
**Source:** `tail.gon`  

```
301 { //Turtle Head
        tag animal
        desc "MUTATION_TAIL_301_DESC"

        passives {
            PoopWhenHit Poop
        }
    }
```

---

### `302`
**Name:** Scorpion Tail  
**Description:** Your basic attack inflicts Poison.  
**Source:** `tail.gon`  

```
302 { //Scorpion Tail
        tag animal
        desc "MUTATION_TAIL_302_DESC"

        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }
```

---

### `303`
**Name:** Rock Tail  
**Description:** Your basic attack has a 5% chance to Stun.  
**Source:** `tail.gon`  

```
303 { //Rock Tail
        desc "MUTATION_TAIL_303_DESC"

        passives {
            AddStatusToBasicAttack {
                Stun [1, .05]
            }
        }
    }
```

---

### `304`
**Name:** Monkey Tail  
**Source:** `tail.gon`  

```
304 { //Monkey Tail
        tag animal
        dex 1
    }
```

---

### `305`
**Name:** Cacuts Tail  
**Description:** +1 Thorns.  
**Source:** `tail.gon`  

```
305 { //Cacuts Tail
        desc "MUTATION_TAIL_305_DESC"

        passives {
            Thorns 1
        }
    }
```

---

### `306`
**Name:** Big Lump Tail  
**Source:** `tail.gon`  

```
306 { //Big Lump Tail
        con 1
    }
```

---

### `307`
**Name:** Antenna Tail  
**Source:** `tail.gon`  

```
307 { //Antenna Tail
        spd 1
    }
```

---

### `308`
**Name:** Baby Tail  
**Description:** +5% dodge chance.  
**Source:** `tail.gon`  

```
308 { //Baby Tail
        desc "MUTATION_TAIL_308_DESC"

        lck 1
        passives {
            DodgeChance 5%
        }
    }
```

---

### `309`
**Name:** Baboon's' Ass  
**Source:** `tail.gon`  

```
309 { //Baboon's' Ass
        tag animal
        cha 1
    }
```

---

### `310`
**Name:** Hand Tail  
**Description:** Your basic attack has a 10% chance to repeat once.  
**Source:** `tail.gon`  

```
310 { //Hand Tail
        desc "MUTATION_TAIL_310_DESC"

        passives {
            AddTemporaryEffectsToBasicAttack {
                Fury 10
            }
        }
    }
```

---

### `311`
**Name:** Thorn Tail  
**Description:** Thorns 1.  
**Source:** `tail.gon`  

```
311 { //Thorn Tail 
        desc "MUTATION_TAIL_311_DESC" 
        passives {        
            Thorns 1 
        } 
    }
```

---

### `312`
**Name:** Holy Tail  
**Source:** `tail.gon`  

```
312 { //Holy Tail 
        divine_shield 1
    }
```

---

### `313`
**Name:** Hose Tail  
**Description:** Your basic attack creates water tiles.  
**Source:** `tail.gon`  

```
313 { //Hose Tail
        desc "MUTATION_TAIL_313_DESC" 
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        } 
    }
```

---

### `314`
**Name:** Bone Tail  
**Description:** Whenever you down a unit, you have a 10% chance to reanimate that unit with 50% HP.  
**Source:** `tail.gon`  

```
314 { //Bone Tail
        desc "MUTATION_TAIL_314_DESC"

        passives { 
            StatusKilledCharacters {
                Conditional_RandomChance {
                    odds 10%
                    AutoReanimate 50%
                }
            } 
        }
    }
```

---

### `315`
**Name:** Maggot Tail  
**Description:** 20% chance to spawn a Maggot when hit.  
**Source:** `tail.gon`  

```
315 { //Maggot Tail
        desc "MUTATION_TAIL_315_DESC"  
        passives {
            SpawnThingOnDamage {
                object Maggot
                good false //good relative to the thing attacking, for luck calculations
                chance 20%
            }
        }
    }
```

---

### `316`
**Name:** Grass Tail  
**Description:** 25% chance to spawn tall grass wherever you end your movement.  
**Source:** `tail.gon`  

```
316 { //Grass Tail
        desc "MUTATION_TAIL_316_DESC" 
        passives {     
            StatusOnEndMove {
                Conditional_GoodRoll {
                    odds 25%
                    ChangeTilesUnder TallGrassTile
                }
            }
        } 
    }
```

---

### `317`
**Name:** Skunk Tail  
**Description:** When hit, fart a Poison 4 attack with Knockback behind you.  
**Source:** `tail.gon`  

```
317 { //Skunk Tail
        desc "MUTATION_TAIL_317_DESC" 
        passives {
            AbilityReaction SkunkTail
        }
    }
```

---

### `318`
**Name:** Rattle  
**Description:** Your basic attack inflicts Poison.  
**Source:** `tail.gon`  

```
318 { //Rattle
        desc "MUTATION_TAIL_318_DESC" 
        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        } 
    }
```

---

### `319`
**Name:** Snake Tail  
**Description:** Units who contact you get Poisoned.  
**Source:** `tail.gon`  

```
319 { //Snake Tail
        desc "MUTATION_TAIL_319_DESC" 
        passives {
            PoisonThorns 1
        } 
    }
```

---

### `320`
**Name:** Glass Tail  
**Description:** Bleed 1. Bleed Thorns 2.  
**Source:** `tail.gon`  

```
320 { //Glass Tail
        desc "MUTATION_TAIL_320_DESC" 
        passives {
            Bleed 1 
            BleedThorns 2                
        } 
    }
```

---

### `321`
**Name:** Extra Head  
**Source:** `tail.gon`  

```
321 { //Extra Head
        tag extra
        int 1
    }
```

---

### `322`
**Name:** Exhaust Pipe  
**Description:** Gain +1 [img:spd] each turn.  
**Source:** `tail.gon`  

```
322 { //Exhaust Pipe
        desc "MUTATION_TAIL_322_DESC" 
        passives {     
            StatusEachTurnBegin {
                SpeedUp 1
            }
        } 
    }
```

---

### `323`
**Name:** Jetpack Tail  
**Description:** Your movement action is a jump.  
**Source:** `tail.gon`  

```
323 { //Jetpack Tail
        desc "MUTATION_TAIL_323_DESC" 
        passives {
            ReplaceBasicMove_Mutation BasicJump
        } 
    }
```

---

### `324`
**Name:** Wing Tail  
**Source:** `tail.gon`  

```
324 { //Wing Tail
        spd 2 
    }
```

---

### `325`
**Name:** Spring Tail  
**Description:** Units that contact you get knocked back 2 tiles.  
**Source:** `tail.gon`  

```
325 { //Spring Tail
        desc "MUTATION_TAIL_325_DESC" 
        passives {
            MeleeRevengeDamage {
                knockback 2
            }
        } 
    }
```

---

### `326`
**Name:** Eyeball Tail  
**Description:** 10% dodge chance. Bruise 1.  
**Source:** `tail.gon`  

```
326 { //Eyeball Tail
        desc "MUTATION_TAIL_326_DESC" 
        passives {
            Bruise 1
            DodgeChance 10%

        }
    }
```

---

### `327`
**Name:** Tree Branch Tail  
**Description:** If you don't move, gain 3 Charge at the end of the turn.  
**Source:** `tail.gon`  

```
327 { //Tree Branch Tail
        desc "MUTATION_TAIL_327_DESC" 
        passives {
            StatusIfDidntMove {
                Charge 3
            }
        } 
    }
```

---

### `329`
**Name:** Mr. Worm  
**Description:** You can unequip cursed items and parasites.  
**Source:** `tail.gon`  

```
329 { //Mr. Worm
        desc "MUTATION_TAIL_329_DESC" 
        passives {   
            CanRemoveCursedItems 1
        } 
    }
```

---

### `331`
**Name:** Dice Tail  
**Description:** You can reroll your options when you level up.  
**Source:** `tail.gon`  

```
331 { //Dice Tail
        desc "MUTATION_TAIL_331_DESC"
        passives { 
            AddLevelUpRerolls 1
        } 
    }
```

---

### `332`
**Name:** Tennis Racket  
**Description:** +25% chance to reflect projectiles.  
**Source:** `tail.gon`  

```
332 { //Tennis Racket
        desc "MUTATION_TAIL_332_DESC"
        passives { 
            ReflectProjectiles 25%
        }
    }
```

---

### `334`
**Name:** Fire Flower Tail  
**Description:** Your basic attack inflicts Burn 1.  
**Source:** `tail.gon`  

```
334 { //Fire Flower Tail
        desc "MUTATION_TAIL_334_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 1 
            }
            AddElementsToBasicAttack Fire
        } 
    }
```

---

### `336`
**Name:** Horn Tail  
**Description:** +1 Thorns.  
**Source:** `tail.gon`  

```
336 { //Horn Tail
        desc "MUTATION_TAIL_336_DESC"
        passives {
            Thorns 1
        }
    }
```

---

### `337`
**Name:** Tail Feather  
**Description:** Your basic attack is wind element.  
**Source:** `tail.gon`  

```
337 { //Tail Feather
        desc "MUTATION_TAIL_337_DESC"
        tag bird

        passives {
            AddStatusToBasicAttack {
                Knockback 1
                VisualFXTile fx_windSpell
            }
            AddElementsToBasicAttack Wind
        }
    }
```

---

### `338`
**Name:** Flame Tail  
**Description:** Your basic attack inflicts Burn 1.  
**Source:** `tail.gon`  

```
338 { //Flame Tail
        desc "MUTATION_TAIL_338_DESC"

        passives {
            AddStatusToBasicAttack {
                Burn 1 
            }
            AddElementsToBasicAttack Fire
        } 
    }
```

---

### `339`
**Name:** Light Bulb  
**Description:** While at full mana, you have +2 Damage.  
**Source:** `tail.gon`  

```
339 { //Light Bulb
        desc "MUTATION_TAIL_339_DESC"

        passives {
            PassiveWhenAtFullMana {
                DamageUp 2
            }
        }
    }
```

---

### `341`
**Name:** Tongue Tail  
**Description:** Gain +1 Charge when you take damage.  
**Source:** `tail.gon`  

```
341 { //Tongue Tail
        desc "MUTATION_TAIL_341_DESC" 
        passives {
            StatusOnTookDamage {
                Charge 1
            }
        } 
    }
```

---

### `342`
**Name:** Kitten Tail  
**Description:** Spawn a Charmed Kitten familiar when you get downed.  
**Source:** `tail.gon`  

```
342 { //Kitten Tail
        desc "MUTATION_TAIL_342_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }
```

---

### `750`
**Name:** Bunny Tail*  
**Source:** `tail.gon`  

```
750 { //Bunny Tail*
		cha 1
    }
```

---

### `751`
**Name:** Beaver Tail*  
**Description:** +1 Brace.  
**Source:** `tail.gon`  

```
751 { //Beaver Tail*
        desc "MUTATION_TAIL_751_DESC"  
        passives {
			Brace 1
        }
    }
```

---

### `752`
**Name:** Pig Tail*  
**Source:** `tail.gon`  

```
752 { //Pig Tail*
		con 1
    }
```

---

### `753`
**Name:** Skunk Tail 2*  
**Source:** `tail.gon`  

```
753 { //Skunk Tail 2*
        passives {

        }
    }
```

---

### `754`
**Name:** Spiked Tail*  
**Description:** +1 Thorns.  
**Source:** `tail.gon`  

```
754 { //Spiked Tail*
        desc "MUTATION_TAIL_754_DESC"  
        passives {
			Thorns 1
        }
    }
```

---

### `755`
**Name:** mermaid Tail*  
**Description:** Water does not slow movement.  
**Source:** `tail.gon`  

```
755 { //mermaid Tail*
        desc "MUTATION_TAIL_755_DESC"  
        passives {
            WaterWalk 1
        }
    }
```

---

### `756`
**Name:** Devil Tail*  
**Description:** +1 Bleed Thorns.  
**Source:** `tail.gon`  

```
756 { //Devil Tail*
        desc "MUTATION_TAIL_756_DESC"  
        passives {
			BleedThorns 1
        }
    }
```

---

### `757`
**Name:** sonichu Tail*  
**Description:** Your movement action is shadowstep.  
**Source:** `tail.gon`  

```
757 { //sonichu Tail*
        desc "MUTATION_TAIL_757_DESC"  
        passives {
            ReplaceBasicMove Shadowstep
        }
    }
```

---

### `759`
**Name:** slender Tail*  
**Description:** Start with +1 Bonus Attack.  
**Source:** `tail.gon`  

```
759 { //slender Tail*
        desc "MUTATION_TAIL_759_DESC"  
		passives {
			Quivered 1
		}
    }
```

---

### `760`
**Name:** human head tail  
**Description:** Start with 2 backflips.  
**Source:** `tail.gon`  

```
760 { //human head tail
        desc "MUTATION_TAIL_760_DESC"  
        passives {
            BackflipWhenTargeted {
                stacks 2
                ability BackflipDodge
            }
        }
    }
```

---

### `900`
**Name:** slender  
**Source:** `tail.gon`  

```
900 { //slender
        spd 1
    }
```

---

### `1500`
**Name:** rat tail  
**Source:** `tail.gon`  

```
1500 { //rat tail
        tag animal
        dex 1
    }
```

---

### `400`
**Source:** `tail.gon`  

```
400 {
        tag common
        str 2
        con -1
    }
```

---

### `401`
**Source:** `tail.gon`  

```
401 {
        tag common
        str 2
        dex -1
    }
```

---

### `402`
**Source:** `tail.gon`  

```
402 {
        tag common
        str 2
        cha -1
    }
```

---

### `403`
**Source:** `tail.gon`  

```
403 {
        tag common
        str 2
        int -1
    }
```

---

### `404`
**Source:** `tail.gon`  

```
404 {
        tag common
        str 2
        spd -1
    }
```

---

### `405`
**Source:** `tail.gon`  

```
405 {
        tag common
        str 2
        lck -1
    }
```

---

### `406`
**Source:** `tail.gon`  

```
406 {
        tag common
        con 2
        str -1
    }
```

---

### `407`
**Source:** `tail.gon`  

```
407 {
        tag common
        con 2
        dex -1
    }
```

---

### `408`
**Source:** `tail.gon`  

```
408 {
        tag common
        con 2
        cha -1
    }
```

---

### `409`
**Source:** `tail.gon`  

```
409 {
        tag common
        con 2
        int -1
    }
```

---

### `410`
**Source:** `tail.gon`  

```
410 {
        tag common
        con 2
        spd -1
    }
```

---

### `411`
**Source:** `tail.gon`  

```
411 {
        tag common
        con 2
        lck -1
    }
```

---

### `412`
**Source:** `tail.gon`  

```
412 {
        tag common
        dex 2
        con -1
    }
```

---

### `413`
**Source:** `tail.gon`  

```
413 {
        tag common
        dex 2
        str -1
    }
```

---

### `414`
**Source:** `tail.gon`  

```
414 {
        tag common
        dex 2
        cha -1
    }
```

---

### `415`
**Source:** `tail.gon`  

```
415 {
        tag common
        dex 2
        int -1
    }
```

---

### `416`
**Source:** `tail.gon`  

```
416 {
        tag common
        dex 2
        spd -1
    }
```

---

### `417`
**Source:** `tail.gon`  

```
417 {
        tag common
        dex 2
        lck -1
    }
```

---

### `418`
**Source:** `tail.gon`  

```
418 {
        tag common
        int 2
        con -1
    }
```

---

### `419`
**Source:** `tail.gon`  

```
419 {
        tag common
        int 2
        dex -1
    }
```

---

### `420`
**Source:** `tail.gon`  

```
420 {
        tag common
        int 2
        cha -1
    }
```

---

### `421`
**Source:** `tail.gon`  

```
421 {
        tag common
        int 2
        str -1
    }
```

---

### `422`
**Source:** `tail.gon`  

```
422 {
        tag common
        int 2
        spd -1
    }
```

---

### `423`
**Source:** `tail.gon`  

```
423 {
        tag common
        int 2
        lck -1
    }
```

---

### `424`
**Source:** `tail.gon`  

```
424 {
        tag common
        cha 2
        con -1
    }
```

---

### `425`
**Source:** `tail.gon`  

```
425 {
        tag common
        cha 2
        dex -1
    }
```

---

### `426`
**Source:** `tail.gon`  

```
426 {
        tag common
        cha 2
        str -1
    }
```

---

### `427`
**Source:** `tail.gon`  

```
427 {
        tag common
        cha 2
        int -1
    }
```

---

### `428`
**Source:** `tail.gon`  

```
428 {
        tag common
        cha 2
        spd -1
    }
```

---

### `429`
**Source:** `tail.gon`  

```
429 {
        tag common
        cha 2
        lck -1
    }
```

---

### `430`
**Source:** `tail.gon`  

```
430 {
        tag common
        lck 2
        con -1
    }
```

---

### `431`
**Source:** `tail.gon`  

```
431 {
        tag common
        lck 2
        dex -1
    }
```

---

### `432`
**Source:** `tail.gon`  

```
432 {
        tag common
        lck 2
        cha -1
    }
```

---

### `433`
**Source:** `tail.gon`  

```
433 {
        tag common
        lck 2
        int -1
    }
```

---

### `434`
**Source:** `tail.gon`  

```
434 {
        tag common
        lck 2
        spd -1
    }
```

---

### `435`
**Source:** `tail.gon`  

```
435 {
        tag common
        lck 2
        str -1
    }
```

---

### `436`
**Source:** `tail.gon`  

```
436 {
        tag common
        spd 2
        con -1
    }
```

---

### `437`
**Source:** `tail.gon`  

```
437 {
        tag common
        spd 2
        str -1
    }
```

---

### `438`
**Source:** `tail.gon`  

```
438 {
        tag common
        spd 2
        cha -1
    }
```

---

### `439`
**Source:** `tail.gon`  

```
439 {
        tag common
        spd 2
        int -1
    }
```

---

### `440`
**Source:** `tail.gon`  

```
440 {
        tag common
        spd 2
        dex -1
    }
```

---

### `441`
**Source:** `tail.gon`  

```
441 {
        tag common
        spd 2
        lck -1
    }
```

---

### `700`
**Name:** kinked tail  
**Source:** `tail.gon`  

```
700 { //kinked tail
        tag birth_defect
        lck -2
    }
```

---

### `701`
**Name:** lipoma  
**Source:** `tail.gon`  

```
701 { //lipoma
        tag birth_defect
        spd -1
        cha -1
    }
```

---

### `2`
**Name:** no tail (702)  
**Source:** `tail.gon`  

```
2 { //no tail (702)
        tag birth_defect
        dex -1
    }
```

---

### `703`
**Name:** heavy tail  
**Description:** Start each battle with Immobile 1.  
**Source:** `tail.gon`  

```
703 { //heavy tail
        desc "MUTATION_TAIL_703_DESC"
        tag birth_defect
        con 1

        passives {
            Immobile 1
        }
    }
```

---

### `704`
**Name:** forked tail  
**Description:** Hunter abilities are also offered when you level up.  
**Source:** `tail.gon`  

```
704 { //forked tail
        desc "MUTATION_TAIL_704_DESC"
        tag birth_defect
        lck -2

        passives {
            MulticlassLevelUp Hunter
        }
    }
```

---

## Texture Mutations

### `300`
**Name:** Stitches  
**Description:** +1 Health Regeneration  
**Source:** `texture.gon`  

```
300 { //Stitches
        desc "MUTATION_TEXTURE_300_DESC"

        cha -1
        passives {
            HealthRegenUp 1
        }
    }
```

---

### `301`
**Name:** Fish Scales  
**Description:** +1 Health and Mana Regeneration while wet.  
**Source:** `texture.gon`  

```
301 { //Fish Scales
        desc "MUTATION_TEXTURE_301_DESC"

        passives {
            PassiveWhenAffectedByElement {
                element water
                passives {
                    HealthRegenUp 1
                    AddManaRegen 1
                }
            }
        }
    }
```

---

### `302`
**Name:** Conjoined  
**Source:** `texture.gon`  

```
302 { //Conjoined
        lck 1
    }
```

---

### `303`
**Name:** Patches  
**Description:** Start each battle with a random stat up.  
**Source:** `texture.gon`  

```
303 { //Patches
        desc "MUTATION_TEXTURE_303_DESC"

        passives {
            RandomStatUp 1
        }
    }
```

---

### `304`
**Name:** Confusing Hide  
**Description:** Units that contact or attack you have a 10% chance to become Confused.  
**Source:** `texture.gon`  

```
304 { //Confusing Hide
        desc "MUTATION_TEXTURE_304_DESC"

        passives {
            RevengeDamage {
                type status
                damage 0
                effects {
                    Confusion [1, .1]
                }
            }
        }
    }
```

---

### `305`
**Name:** Robot Hide  
**Source:** `texture.gon`  

```
305 { //Robot Hide
        int 1
    }
```

---

### `306`
**Name:** Veiny  
**Source:** `texture.gon`  

```
306 { //Veiny
        str 1
    }
```

---

### `307`
**Name:** Eyeballs  
**Description:** +5% dodge chance.  
**Source:** `texture.gon`  

```
307 { //Eyeballs
        desc "MUTATION_TEXTURE_307_DESC"

        passives {
            DodgeChance 5%
        }
    }
```

---

### `308`
**Name:** Heart Tattoo  
**Source:** `texture.gon`  

```
308 { //Heart Tattoo
        cha 1
    }
```

---

### `309`
**Name:** Tatted Up  
**Description:** Your basic attack has a 5% chance to inflict Fear. You have a 5% chance to inflict Fear on units who contact or attack you.  
**Source:** `texture.gon`  

```
309 {//Tatted Up
        desc "MUTATION_TEXTURE_309_DESC"

        passives {
            RevengeDamage {
                type status
                damage 0
                effects {
                    Fear [1, .05]
                }
            }

            AddStatusToBasicAttack {
                Fear [1, .05]
            }
        }
    }
```

---

### `310`
**Name:** Cash Hide  
**Description:** Gain double the effects of pickups you collect.  
**Source:** `texture.gon`  

```
310 { //Cash Hide
        desc "MUTATION_TEXTURE_310_DESC"

        passives {
            AddLootMultiplier 1
        }
    }
```

---

### `750`
**Name:** skunk Hide  
**Description:** Units who contact you get Poison 2.  
**Source:** `texture.gon`  

```
750 { //skunk Hide
        desc "MUTATION_TEXTURE_750_DESC"

        passives {
            PoisonThorns 2
        }
    }
```

---

### `400`
**Source:** `texture.gon`  

```
400 {
        tag common
        str 2
        con -1
    }
```

---

### `401`
**Source:** `texture.gon`  

```
401 {
        tag common
        str 2
        dex -1
    }
```

---

### `402`
**Source:** `texture.gon`  

```
402 {
        tag common
        str 2
        cha -1
    }
```

---

### `403`
**Source:** `texture.gon`  

```
403 {
        tag common
        str 2
        int -1
    }
```

---

### `404`
**Source:** `texture.gon`  

```
404 {
        tag common
        str 2
        spd -1
    }
```

---

### `405`
**Source:** `texture.gon`  

```
405 {
        tag common
        str 2
        lck -1
    }
```

---

### `406`
**Source:** `texture.gon`  

```
406 {
        tag common
        con 2
        str -1
    }
```

---

### `407`
**Source:** `texture.gon`  

```
407 {
        tag common
        con 2
        dex -1
    }
```

---

### `408`
**Source:** `texture.gon`  

```
408 {
        tag common
        con 2
        cha -1
    }
```

---

### `409`
**Source:** `texture.gon`  

```
409 {
        tag common
        con 2
        int -1
    }
```

---

### `410`
**Source:** `texture.gon`  

```
410 {
        tag common
        con 2
        spd -1
    }
```

---

### `411`
**Source:** `texture.gon`  

```
411 {
        tag common
        con 2
        lck -1
    }
```

---

### `412`
**Source:** `texture.gon`  

```
412 {
        tag common
        dex 2
        con -1
    }
```

---

### `413`
**Source:** `texture.gon`  

```
413 {
        tag common
        dex 2
        str -1
    }
```

---

### `414`
**Source:** `texture.gon`  

```
414 {
        tag common
        dex 2
        cha -1
    }
```

---

### `415`
**Source:** `texture.gon`  

```
415 {
        tag common
        dex 2
        int -1
    }
```

---

### `416`
**Source:** `texture.gon`  

```
416 {
        tag common
        dex 2
        spd -1
    }
```

---

### `417`
**Source:** `texture.gon`  

```
417 {
        tag common
        dex 2
        lck -1
    }
```

---

### `418`
**Source:** `texture.gon`  

```
418 {
        tag common
        int 2
        con -1
    }
```

---

### `419`
**Source:** `texture.gon`  

```
419 {
        tag common
        int 2
        dex -1
    }
```

---

### `420`
**Source:** `texture.gon`  

```
420 {
        tag common
        int 2
        cha -1
    }
```

---

### `421`
**Source:** `texture.gon`  

```
421 {
        tag common
        int 2
        str -1
    }
```

---

### `422`
**Source:** `texture.gon`  

```
422 {
        tag common
        int 2
        spd -1
    }
```

---

### `423`
**Source:** `texture.gon`  

```
423 {
        tag common
        int 2
        lck -1
    }
```

---

### `424`
**Source:** `texture.gon`  

```
424 {
        tag common
        cha 2
        con -1
    }
```

---

### `425`
**Source:** `texture.gon`  

```
425 {
        tag common
        cha 2
        dex -1
    }
```

---

### `426`
**Source:** `texture.gon`  

```
426 {
        tag common
        cha 2
        str -1
    }
```

---

### `427`
**Source:** `texture.gon`  

```
427 {
        tag common
        cha 2
        int -1
    }
```

---

### `428`
**Source:** `texture.gon`  

```
428 {
        tag common
        cha 2
        spd -1
    }
```

---

### `429`
**Source:** `texture.gon`  

```
429 {
        tag common
        cha 2
        lck -1
    }
```

---

### `430`
**Source:** `texture.gon`  

```
430 {
        tag common
        lck 2
        con -1
    }
```

---

### `431`
**Source:** `texture.gon`  

```
431 {
        tag common
        lck 2
        dex -1
    }
```

---

### `432`
**Source:** `texture.gon`  

```
432 {
        tag common
        lck 2
        cha -1
    }
```

---

### `433`
**Source:** `texture.gon`  

```
433 {
        tag common
        lck 2
        int -1
    }
```

---

### `434`
**Source:** `texture.gon`  

```
434 {
        tag common
        lck 2
        spd -1
    }
```

---

### `435`
**Source:** `texture.gon`  

```
435 {
        tag common
        lck 2
        str -1
    }
```

---

### `436`
**Source:** `texture.gon`  

```
436 {
        tag common
        spd 2
        con -1
    }
```

---

### `437`
**Source:** `texture.gon`  

```
437 {
        tag common
        spd 2
        str -1
    }
```

---

### `438`
**Source:** `texture.gon`  

```
438 {
        tag common
        spd 2
        cha -1
    }
```

---

### `439`
**Source:** `texture.gon`  

```
439 {
        tag common
        spd 2
        int -1
    }
```

---

### `440`
**Source:** `texture.gon`  

```
440 {
        tag common
        spd 2
        dex -1
    }
```

---

### `441`
**Source:** `texture.gon`  

```
441 {
        tag common
        spd 2
        lck -1
    }
```

---

### `700`
**Name:** neurofibromatosis  
**Source:** `texture.gon`  

```
700 { //neurofibromatosis
        tag birth_defect
        cha -2
    }
```

---

### `701`
**Name:** melanocytic nevus  
**Source:** `texture.gon`  

```
701 { //melanocytic nevus
        tag birth_defect
        cha -2
        shield 1
    }
```

---

### `702`
**Name:** bleeding  
**Description:** Start each battle with Bleed 1.  
**Source:** `texture.gon`  

```
702 { //bleeding
        desc "MUTATION_TEXTURE_702_DESC"
        tag birth_defect

        passives {
            Bleed 1
        }
    }
```

---

### `703`
**Name:** blue spots  
**Description:** Mage abilities are also offered when you level up.  
**Source:** `texture.gon`  

```
703 { //blue spots
        desc "MUTATION_TEXTURE_703_DESC"
        tag birth_defect
        cha -2

        passives {
            MulticlassLevelUp Mage
        }
    }
```

---

### `704`
**Name:** red dots  
**Description:** Fighter abilities are also offered when you level up.  
**Source:** `texture.gon`  

```
704 { //red dots
        desc "MUTATION_TEXTURE_704_DESC"
        tag birth_defect
        cha -2

        passives {
            MulticlassLevelUp Fighter
        }
    }
```

---

### `705`
**Name:** jaundice  
**Description:** Thief abilities are also offered when you level up.  
**Source:** `texture.gon`  

```
705 { //jaundice
        desc "MUTATION_TEXTURE_705_DESC"
        tag birth_defect
        cha -2

        passives {
            MulticlassLevelUp Thief
        }
    }
```

---

### `706`
**Name:** vitiligo  
**Description:** 10% dodge chance.  
**Source:** `texture.gon`  

```
706 { //vitiligo
        desc "MUTATION_TEXTURE_706_DESC"
        tag birth_defect
        cha -1

        passives {
            DodgeChance_Status 10
        }
    }
```

---

