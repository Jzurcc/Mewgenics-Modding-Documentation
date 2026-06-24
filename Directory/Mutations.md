# Mutations Directory

### `body`
**Description:** +1 Thorns.  
**Source:** `body.gon`  

| Field | Value |
| :--- | :--- |
| Body Part | body |

<details>
<summary><b>Raw .gon</b></summary>

```
body {
    300 { 
        con 1
    }

    301 { 
        desc "MUTATION_BODY_301_DESC"
        passives {
            Thorns 1
        }
    }

    302 { 
        tag animal
        spd -1
        shield 5
    }

    303 { 
        tag animal
        shield 10
        spd -2
    }

    304 { 
        spd 1
        int 1
    }

    305 { 
        lck 1
    }

    306 { 
        shield 12
        con -3
    }

    307 { 
        tag animal
        cha 1
    }

    308 { 
        str 1
        con 1
        int -1
    }

    309 { 
        desc "MUTATION_BODY_309_DESC"

        passives {
            MeleeRevengeDamage {
                type status
                damage 0
                knockback 2
            }
        }
    }

    310 { 
        cha 1
    }

    311 { 
        con 1
    }
    
    312 { 
        desc "MUTATION_BODY_312_DESC"
        passives {
            SpawnThingOnDamage {
                object Coin
                chance 100%
            }
        }
    }

    313 { 
        desc "MUTATION_BODY_313_DESC"
        passives {
            KineticSpikes 1
        }
    }

    314 { 
        desc "MUTATION_BODY_314_DESC"
        cha -1
        passives {   
            Thorns 2 
        }
    }

    315 { 
        desc "MUTATION_BODY_315_DESC"
        passives {
            Brace 1
        }
    }
    
    316 { 
        shield 2
    }

    317 { 
        desc "MUTATION_BODY_317_DESC"
        con 1
        passives {
		    DrinkWater 1
        }
    }

    318 { 
         desc "MUTATION_BODY_318_DESC" 

        passives { 
            SpawnEachTurn {
                object CharmedFly
                chance 25% 
            } 
        }
    }

    319 { 
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

    320 { 
        shield 1
    }
     
    321 { 
        desc "MUTATION_BODY_321_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }

    322 { 
        desc "MUTATION_BODY_322_DESC"
        passives {
            StatusOnBattleEnd {
                FindItemFromPool consumables
            }
        }
    }

    323 { 
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

    324 { 
        desc "MUTATION_BODY_324_DESC"
        passives {
            StatusOnKill {
                RangeUp 1
            }
        }
    }
	
    750 { 
        desc "MUTATION_BODY_750_DESC" 
        passives {        
            Thorns 1 
        } 
    }
	
    753 { 
		shield 5
    }
	
    758 { 
		desc "MUTATION_BODY_758_DESC" 
		con 1
		passives {
			Quivered 1
		}
    }

    900 { 
        con -2
        spd 1
    }


    
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

    
    700 { 
        tag birth_defect
        con -2
    }
    701 { 
        tag birth_defect
        spd -2
    }
    702 { 
        tag birth_defect
        con -1
    }    
	703 { 
        desc "MUTATION_BODY_703_DESC"
        tag birth_defect

        passives {
            Bruise 1
        }
    }
	704 { 
        tag birth_defect
        spd -3
		con 2
    }
	
}
```

</details>

---

### `ears`
**Description:** +1 Health and Mana Regeneration while wet.  
**Source:** `ears.gon`  

| Field | Value |
| :--- | :--- |
| Body Part | ears |

<details>
<summary><b>Raw .gon</b></summary>

```
ears {
    300 { 
        tag animal
        str 1 
    }
    301 { 
        tag animal
        int 1 
    }
    302 { 
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
    303 { 
        tag animal
        desc "MUTATION_EARS_303_DESC"

        str 1
        passives {
            AddStatusToBasicMeleeAttack {
                Knockback 1
            }
        }
    }
    304 { 
        cha 1
    }
    305 { 
        shield 1
    }
    306 { 
        tag animal
        spd 1
    }
    307 { 
        int 1
    }
    308 { 
        str 1
        cha -1
    }
    309 { 
        tag animal
        desc "MUTATION_EARS_309_DESC"

        passives {
            AddStatusToBasicAttack {
                Bleed 1
            }
        }
    }
    310 { 
        int 1
    }

    
    
    


    313 { 
        tag animal
        desc "MUTATION_EARS_313_DESC"

        shield 1
        passives {
            AddStatusToBasicMeleeAttack {
                Knockback 1
            }
        }
    }

    314 { 
        tag animal
        desc "MUTATION_EARS_314_DESC"
        passives {
            Thorns 1
            AddStatusToBasicMeleeAttack {
                Bleed 1 
            }
        }
    }
    
    315 { 
        tag animal
        desc "MUTATION_EARS_315_DESC" 

        passives { 
            SpawnEachTurn {
                object CharmedFly
                good false 
                chance 50% 
            }
            
            
            Poison 1
        }
    }


    316 { 
        tag animal
        desc "MUTATION_EARS_316_DESC"

        passives {
            ShowHiddenThings 1
            DodgeChance 5%
        }
    }

    317 { 
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

    318 { 
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

    319 { 
        tag animal
        desc "MUTATION_EARS_319_DESC"

        passives {
            StatusOnTookDamage {
                Charge 1
            }
        }
    }

    320 { 
        desc "MUTATION_EARS_320_DESC"

        passives {
            KineticSpikes 1 
        }
    }


    
    321 { 
        desc "MUTATION_EARS_321_DESC"

        passives {
            MeleeRevengeDamage {
                knockback 1
            }
        }
    }


    322 { 
        tag animal
        cha 1 
    }

    323 { 
        desc "MUTATION_EARS_323_DESC"

        passives {
            AddStatusToBasicAttack {
                FlatLeech 1
            } 
        }
    }

    
    
    
    
    
    
    
    
    
    
    

    325 { 
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

    326 { 
        desc "MUTATION_EARS_326_DESC"

        passives {
            SpawnEachTurn {
                chance 5%
                object  CharmedMaggot
            } 
        }
    }

    327 { 
        tag animal
        desc "MUTATION_EARS_327_DESC"
            passives {
                SpawnOnBattleStartRandomEmptyTile {
                    object RandomFoodPickup 
                }
            } 
    }

    328 { 
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

    329 { 
        tag animal
        desc "MUTATION_EARS_329_DESC" 
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        }  

    }

    330 { 
        desc "MUTATION_EARS_330_DESC"
        passives {
            Thorns 1
            MeleeRevengeDamage {
                Immobile 10%
            }
        }
    }

    331 { 
        desc "MUTATION_EARS_331_DESC"
        passives {
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }

    332 { 
        desc "MUTATION_EARS_332_DESC"
        passives {
            Brace 1
        }
    }
    
    333 { 
        shield 3 
    }

    334 { 
        desc "MUTATION_EARS_334_DESC"
        passives {
            SpawnOnBattleStartRandomEmptyTile {
                object Coin
                number [1 3]
            }
        }
    }

    335 { 
        desc "MUTATION_EARS_335_DESC"
        passives { 
            Bleed 1 
            Quivered 1
        }
    }

    336 { 
        desc "MUTATION_EARS_336_DESC"
        passives {
            StatusIfUnusedMovePoints {
                ManaGain 3 
            } 
        }
    }

    337 { 
        desc "MUTATION_EARS_337_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 1
            }
        }
    }
    
    338 { 
        desc "MUTATION_EARS_338_DESC"
        passives {
            MeleeRevengeDamage {
                Freeze [1 0.15]
            }
        }
    }

    339 { 
        desc "MUTATION_EARS_339_DESC"
        passives { 
            ElementImmune Electric
        }
    }

    
    340 { 
        divine_shield 1
    }

    341 { 
        desc "MUTATION_EARS_341_DESC" 
        passives {
            ChanceToBackflip {
                ability BackflipDodge
                chance 10%
            } 
        }
    }

    342 { 
        desc "MUTATION_EARS_342_DESC" 
        con -1
        passives {
            SpawnThingOnDamage {
                object CharmedFlea
                good false 
                chance 20%
            }
        }
    }

    343 { 
        tag animal
        desc "MUTATION_EARS_343_DESC" 
        passives {        
            Thorns 1 
        } 
    }

    344 { 
        desc "MUTATION_EARS_344_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }

    345 { 
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
    
    750 { 
        tag animal
        desc "MUTATION_EARS_750_DESC"  

        passives {
            ReplaceBasicMove_Mutation BasicJump
        }
    }

    751 { 
        desc "MUTATION_EARS_751_DESC" 
        passives {
            DodgeChance 10%
        }
    }

    752 { 
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

    753 { 
        tag animal
        desc "MUTATION_EARS_753_DESC" 
        passives { 
            AddKnockbackDamage 1
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }

    754 { 
        desc "MUTATION_EARS_754_DESC" 
        spd 1 
        passives {
            AddDamageToElementDamage {
                element Electric
                damage 1
            } 
        }
    }
    
    755 { 
        desc "MUTATION_EARS_755_DESC" 
        passives { 
            StatusOnCastSpell {
                Charge 1
            }   
        }
    }


    900 { 
        desc "MUTATION_EARS_900_DESC"

        passives {
            DodgeChance 10%
        }
    }


    1500 { 
        tag animal
        desc "MUTATION_EARS_1500_DESC"

        passives {
            DodgeChance 2%
        }
    }

    
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

    
    700 { 
        tag birth_defect
        lck -2
    }
    701 { 
        tag birth_defect
        int -2
    }
	702 { 
        tag birth_defect
        cha -1
    }
	703 { 
        desc "MUTATION_EARS_703_DESC"
        tag birth_defect

        passives {
            Confusion 2
        }
    }
	704 { 
        desc "MUTATION_EARS_704_DESC"
        tag birth_defect

        passives {
            Immobile 1
        }
    }
	-2 { 
        tag birth_defect
        dex -2
    }
}
```

</details>

---

### `eyebrows`
**Description:** You have a 10% chance to inflict Confusion on units who contact or attack you.  
**Source:** `eyebrows.gon`  

| Field | Value |
| :--- | :--- |
| Body Part | eyebrows |

<details>
<summary><b>Raw .gon</b></summary>

```
eyebrows {
    300 { 
        spd 1
    }

    301 { 
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

    302 { 
        shield 2
    }

    303 { 
        cha 1
    }

    304 { 
        tag animal
        dex 1
    }

    305 { 
        lck 1
    }

    306 { 
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

    307 { 
        desc MUTATION_EYEBROWS_307_DESC

        passives {
            HealthRegenUp 1
            AddManaRegen 1
        }
    }

    308 { 
        cha 1
    }

    309 { 
        desc MUTATION_EYEBROWS_309_DESC

        passives {
            Thorns 1
        }
    }

    310 { 
        desc MUTATION_EYEBROWS_310_DESC
        tag extra

        passives {
            AddBonusRange 1
        }
    }

    311 { 
        desc MUTATION_EYEBROWS_311_DESC

        passives { 
            StatusEveryXSpellCastsEachTurn {
                stacks 3
                HealthGain 2
            }
        }
    } 

    
    
    
    313 { 
        desc MUTATION_EYEBROWS_313_DESC
    
        passives { 
            SpawnExtraThingsOnBattleStart {
                object RandomPickup
                number [1 2]
            }
        }
    }

    314 { 
        desc MUTATION_EYEBROWS_314_DESC

        passives {
            StatusOnAllyCatDeath {
                DamageUp 2
            }
        }
    } 

    315 { 
        desc MUTATION_EYEBROWS_315_DESC

        passives { 
            AddLevelUpRerolls 1
        }
    }

    900 { 
        desc MUTATION_EYEBROWS_900_DESC

        passives {
            AddStatusToBasicAttack {
                Freeze [1 .01]
            }
            DodgeChance 5%
        }
    }

        
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
	
    
    700 { 
        tag birth_defect
        lck -1
    }
	701 { 
        tag birth_defect
        cha -1
    }
	702 { 
        tag birth_defect
        int -1
    }
    -2 { 
        tag birth_defect
        cha -2
    }
}
```

</details>

---

### `eyes`
**Description:** Your basic attack has a 10% chance to inflict Fear.  
**Source:** `eyes.gon`  

| Field | Value |
| :--- | :--- |
| Body Part | eyes |

<details>
<summary><b>Raw .gon</b></summary>

```
eyes {
    300 { 
        desc "MUTATION_EYES_300_DESC"

        passives {
            AddStatusToBasicAttack {
                Fear [1 .1]
            }
        }
    }
    301 { 
        dex 1
    }
    302 { 
        desc "MUTATION_EYES_302_DESC"
        passives {
            Thorns 1
        }
    }
    303 { 
        int 1
        cha 1
    }
    304 { 
        desc "MUTATION_EYES_304_DESC"
        passives {
            AddInitiative -20
        }
    }
    305 { 
        str -1
        dex -1
        int 3
    }

    306 { 
        desc "MUTATION_EYES_306_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [3, .1]
            }
        }
    }
    307 { 
        desc "MUTATION_EYES_307_DESC"
        passives {
            GainManaWhenAnythingDies 1
        }
    }
    308 { 
        tag animal
        desc "MUTATION_EYES_308_DESC"
        passives {
            DodgeChance 5%
        }
    }
    309 { 
        desc "MUTATION_EYES_309_DESC"
        passives {
            AddCorpseHealth 2
        }
    }
    310 { 
        tag animal
        desc "MUTATION_EYES_310_DESC"
        passives {
            HealthRegenUp 1
        }
    }
    311 { 
        tag animal
        desc "MUTATION_EYES_311_DESC"
        passives {
            BackstabImmunity 1
        }
    }

    312 { 
        desc "MUTATION_EYES_312_DESC"
        shield 1
        passives {
            Brace 1
        }
    }

    313 { 
        desc "MUTATION_EYES_313_DESC"
		divine_shield 1
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        } 
    }

    314 { 
        desc "MUTATION_EYES_314_DESC"
        passives {
            SpawnOnDowned CharmedFly
            SpawnOnDowned CharmedFly
            SpawnOnDowned CharmedFly
            AddCorpseHealth 2
        }
    }
   
    315 { 
        desc "MUTATION_EYES_315_DESC"
        passives {
            KineticSpikes 1
        }
    }
   
    316 { 
        desc "MUTATION_EYES_316_DESC"
        passives { 
            CounterAttack {
                chance 15%
                ability ChainLightning
            }
        }
    }

    317 { 
        desc "MUTATION_EYES_317_DESC"
        passives { 
            StatusEachTurnEnd {
                RandomStatUp 1
            } 
        }
    }
  
    318 { 
        tag animal
        desc "MUTATION_EYES_318_DESC"
        passives {
            ShowHiddenThings 1
            AddKnockbackDamage 1
        }
    }

    319 { 
        desc "MUTATION_EYES_319_DESC"
        passives {
            Blind -1  
            Thorns 1
            DamageUp 1
        }
    }
   
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    

    324 { 
        desc "MUTATION_EYES_324_DESC"
        passives {
            SpawnOnBattleStartRandomEmptyTile {
                object Coin
                number 2
            }
        }
    }

    325 { 
        desc "MUTATION_EYES_325_DESC"
        passives {
            Thorns 1
        }
    }

    326 { 
        desc "MUTATION_EYES_326_DESC"
        passives {
            StatusEveryXSpellCasts {
                stacks 4
                Charge 2
            }
        }
    }

    327 { 
        cha 2 
    }

    328 { 
        tag animal
        desc "MUTATION_EYES_328_DESC"
        
        passives {
            CritChanceUp 10
        }
    }

    329 { 
        desc "MUTATION_EYES_329_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [1, .15]
            }
        }
    }

    
    
    
    
    
    

    331 { 
        desc "MUTATION_EYES_331_DESC"
        passives {
            EquipRandomTemporaryItemFromPool pills
        }
    }

    332 { 
        desc "MUTATION_EYES_332_DESC"
        passives {
            Bleed 1  
            StatusOnTookDamage {
                Charge 1
            }
        }
    }
    
    333 { 
        desc "MUTATION_EYES_333_DESC"
        passives {
            BasicAttackCantMiss 1
        }
    }

    334 { 
        desc "MUTATION_EYES_334_DESC"
        passives {
            Blind -1
            SpawnThingOnDamage {
                object CharmedFlea
                good false 
                chance 100%
            }
        }
    } 
        
    335 { 
        desc "MUTATION_EYES_335_DESC"
        passives {
            AddStatusToBasicAttack {
                Charmed [1, .10]  
            }
        }
    }
            
    336 { 
        desc "MUTATION_EYES_336_DESC" 
        passives { 
            AddElementsToBasicAttack Electric
            AddStatusToBasicAttack {
                Stun [1 .05]
            }
        }
    }
        
    337 { 
        desc "MUTATION_EYES_337_DESC"
        passives {
            AddStatusToBasicAttack {
                Slow 1
            }
            AddElementsToBasicAttack Ice
        }
    }

    338 { 
        desc "MUTATION_EYES_338_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 1
            }
            AddElementsToBasicAttack Fire
        }
    }

    339 { 
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

    340 { 
        desc "MUTATION_EYES_340_DESC"
        passives {
            AddStatusToBasicAttack {
                Leeches 1
            }
        }
    }

    
    341 { 
        desc "MUTATION_EYES_341_DESC"
        passives {
            StatusOnEndMove {
                Conditional_FirstApplicationThisTurn {
                    Charge 1
                }
            }
        }
    }

    342 { 
        desc "MUTATION_EYES_342_DESC"
        passives { 
            AddStatusToBasicAttack {
                Poison 1
            } 
            Poison 1
        }
    }

    343 { 
        desc "MUTATION_EYES_343_DESC"
        passives { 
            RevengeDamage {
                effects {
                    Fear [1, .05]
                }
            }
        }
    }
    
    344 { 
        desc "MUTATION_EYES_344_DESC"
        passives { 
            RevengeDamage {
                effects {
                    Blind [1, .10]
                }
            }
        }
    }

    345 { 
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
    
    346 { 
        desc "MUTATION_EYES_346_DESC" 
        shield 1
        passives { 
            SpawnThingOnDamage {
                object SmallRock
                good false 
                chance 100%
            } 
        }
    }

    347 { 
        desc "MUTATION_EYES_347_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [2, .15]
            }
        }
    }
    
    348 { 
        desc "MUTATION_EYES_348_DESC" 
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1 
        }
    } 

    349 { 
        desc "MUTATION_EYES_349_DESC"
        passives {
            StatusEveryXSpellCasts {
                stacks 8
                RandomMagicMissile 4
            }
        }
    }
    351 { 
        desc "MUTATION_EYES_351_DESC"
        passives {
            ConjureBonusAbility random
        }
    }
    352 { 
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
   
    353 { 
        tag animal
        desc "MUTATION_EYES_353_DESC"
        passives {
            BackstabImmunity 1 
        }
    }
   
   
     
    442 {
        desc "MUTATION_EYES_442_DESC"
        passives {
            ReflectProjectiles 10%
        }
    }
	
    750 {
		int 1
    }
	
    754 {
        desc "MUTATION_EYES_754_DESC"
        passives {
			AddBonusRange 1
            AddElementsToBasicAttack Gravity
        } 
    }
	
    755 {
        desc "MUTATION_EYES_755_DESC"
		passives {
			AddStatusToBasicAttack {
				Fear [1 .15]
			}
		}
    }
   
   
   
    900 { 
        desc "MUTATION_EYES_900_DESC"
   
        passives {
            AddStatusToBasicAttack {
                Slow [1 .1]
            }
        }
    }
   
   
   
    
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
   
    
    700 { 
        tag birth_defect
        cha -2
    }
   
    701 { 
        tag birth_defect
        lck -2
    }
   
    
    702 {
        cha 1
        int 1
        con -2
    }
    -2 { 
        desc "MUTATION_EYES_M2_DESC"
        tag birth_defect
   
        passives {
            Blind -1
        }
    }
    704 { 
        desc "MUTATION_EYES_704_DESC"
        tag birth_defect
   
        passives {
            MissChance 10
        }
   
    }
    705 { 
        tag birth_defect
        desc "MUTATION_EYES_705_DESC"
   
        passives {
            StatusEachTurnBegin {
                MissChance 5
            }
        }
   
    }
    706 { 
        desc "MUTATION_EYES_706_DESC"
        tag birth_defect
   
        passives {
            Confusion 2
        }
    }
   
    1029 { 
        desc "MUTATION_EYES_1029_DESC"
   
        passives {
            CritChanceUp 5
        }
    }
}
```

</details>

---

### `head`
**Description:** +1 Thorns.  
**Source:** `head.gon`  

| Field | Value |
| :--- | :--- |
| Body Part | head |

<details>
<summary><b>Raw .gon</b></summary>

```
head {
    300 { 
        con 1
    }
    301 { 
        int -1
        str 1
        con 1
    }
    302 { 
        int 2
        con -1
    }
    303 { 
        desc "MUTATION_HEAD_303_DESC"
        passives {
            Thorns 1
        }
    }
    304 { 
        tag melted
        desc "MUTATION_HEAD_304_DESC"

        cha -2
        passives {
            HealthRegenUp 2
            DodgeChance 5%
        }
    }
    305 { 
        cha 1
    }
    306 { 
        int 1
    }
    307 { 
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
    308 { 
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
    309 { 
        lck 2
    }
    310 { 
        shield 2
    }

    311 { 
        desc "MUTATION_HEAD_311_DESC"
    
        passives {
            SpawnThingOnDamage {
                object Coin 
                chance 100%
            }
        }
    }

    312 { 
        desc "MUTATION_HEAD_312_DESC"

        passives {
            MakeBasicAttackPull 1
        } 
    } 
    
    313 { 
        desc "MUTATION_HEAD_313_DESC"

        passives {
            PoopWhenHit Poop
        }
    }
    
    314 { 
        desc "MUTATION_HEAD_314_DESC"
    
        passives {
            StatusEachTurnEnd {
               IntelligenceUp 1
            } 
        }
    }

    315 { 
        desc "MUTATION_HEAD_315_DESC"
   
        passives {
            SwapHighestAndLowestStat 1
        }
    }
    
    316 { 
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
    
    317 { 
        desc "MUTATION_HEAD_317_DESC"

        passives {
            DodgeChance 5% 
        }
    }

    318 { 
        desc "MUTATION_HEAD_318_DESC"

        passives {
            AddBonusRange 1
        }
    }
    
    319 { 
        desc "MUTATION_HEAD_319_DESC"

        passives {
            Bruise 2
            StatusOnBattleEnd {
                PermanentIntelligence 1
            }
        }
    } 
      
    320 { 
        desc "MUTATION_HEAD_320_DESC"

        passives {
            AddStatusToBasicAttack {
                Knockback 2
            }
        }
    } 

    321 { 
        desc "MUTATION_HEAD_321_DESC"

        passives { 
            RevengeDamage {
                effects {
                    Fear [1, .05]
                }
            }
        }
    } 
	
    750 { 
		desc "MUTATION_HEAD_750_DESC"
        passives { 
			Thorns 1
        }
    } 
	
    753 { 
        desc "MUTATION_HEAD_753_DESC"

		passives {
			ElementImmune Ice
			StatusImmunity [Freeze, Slow]
		}
    } 	
	
    757 { 
		int 2
    } 
	
    759 { 
        desc "MUTATION_HEAD_759_DESC"
        spd -2

        passives {
            AlphaTurns 1
        }
    } 
	
     
    
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


    
    700 { 
        tag birth_defect
        int -2
    }
    701 { 
        tag birth_defect
        int -2
    }
	702 { 
        tag birth_defect
        int -1
    }
	703 { 
        desc "MUTATION_HEAD_703_DESC"
        tag birth_defect

        passives {
            BackstabFront 1
        }
    }
	704 { 
        desc "MUTATION_HEAD_704_DESC"
        tag birth_defect

        passives {
            MissChance 20
            ManaCostReduction 1
        }
    }
	705 { 
        tag birth_defect
        cha -3
		int 2
    }
	706 { 
        desc "MUTATION_HEAD_706_DESC"
        tag birth_defect
        cha -3

        passives {
            Brace 1
        }
    }

    900 { 
        desc "MUTATION_HEAD_900_DESC"

        cha -1
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1
        }
    }
}
```

</details>

---

### `legs`
**Description:** +1 movement range while wet. Water does not slow movement.  
**Source:** `legs.gon`  

| Field | Value |
| :--- | :--- |
| Body Part | legs |

<details>
<summary><b>Raw .gon</b></summary>

```
legs {
    300 { 
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

    301 { 
        tag animal
        desc "MUTATION_LEGS_301_DESC"

        spd 1
        passives {
            AddStatusToBasicAttack {
                Stun [1, .05]
            }
        }
    }

    302 { 
        tag animal
        desc "MUTATION_LEGS_302_DESC"

        passives {
            KnockbackImmunity 1
        }
    }

    303 { 
        tag animal
        desc "MUTATION_LEGS_303_DESC"

        passives {
            AddStatusToBasicAttack {
                Immobile [1, .05]
            }
        }
    }

    304 { 
        str 1
    }

    305 { 
        desc "MUTATION_LEGS_305_DESC"

        passives {
            DodgeChance 5%
        }
    }

    306 { 
        tag animal
        dex 1
    }

    307 { 
        spd 1
    }

    308 { 
        lck 1
    }

    309 { 
        desc "MUTATION_LEGS_309_DESC"

        passives {
            AddStatusToBasicAttack {
                Bleed [3, .1]
            }
        }
    } 

    310 { 
        desc "MUTATION_LEGS_310_DESC" 
        override_move BasicJump
    }
    
    311 { 
        con 1
    }

    312 { 
        desc "MUTATION_LEGS_312_DESC" 

        passives {
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }

    313 { 
        desc "MUTATION_LEGS_313_DESC"
        passives { 
            AddBonusMeleeRange 1 
        }
    }

    314 { 
        desc "MUTATION_LEGS_314_DESC"
        passives {
            BoostWeaponDamage 1
        }
    }

    315 { 
        desc "MUTATION_LEGS_315_DESC"
        passives {
            ElementImmune Ice
        }
    }
     

    






    317 { 
        desc "MUTATION_LEGS_317_DESC"
        passives {
            AddStatusToBasicMeleeAttack {
                Bleed 1
            }
        }
    }


    318 { 
        divine_shield 1
    }


    319 { 
        desc "MUTATION_LEGS_319_DESC"

        passives {
            StatusEachTurnBegin {
                MoveQuivered [1, 0.1]
            }
        }
    }


    320 { 
        desc "MUTATION_LEGS_320_DESC"

        passives { 
            StatusEachTurnBegin {
                Quivered [1, 0.1]
            }  
        }
    }

    321 { 
        desc "MUTATION_LEGS_321_DESC"

        passives {
            FreePathfindElement Water
        }
    }


    322 { 
		str 1
		con 1
    }


    323 { 
        spd 2
    }


    324 { 
        con 1
    }


    325 { 
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


    326 { 
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


    327 { 
        desc "MUTATION_LEGS_327_DESC"
        passives {
           StatusEachTurnEnd {
               RandomStatUp 2
               RandomStatDown 1
           }
        }
    }

    328 { 
        desc "MUTATION_LEGS_328_DESC"
        passives {
            EquipTemporaryItem Bottles
        }
    }

    329 { 
        desc "MUTATION_LEGS_329_DESC"
        passives {
            EquipTemporaryItem WaterBottle_Full
        }
    }


    330 { 
        desc "MUTATION_LEGS_330_DESC"
        
        passives {
            HealthRegenUp 1
        }
    }


    331 { 
        desc "MUTATION_LEGS_331_DESC"
        override_move BasicJump
        passives {
           AddMovement 1
        }
    }


    332 { 
        desc "MUTATION_LEGS_332_DESC"
        spd -1
        passives {
            SpawnEachTurn {
                object RandomPickup
                chance 50%
            }  
        } 
    }

    333 { 
        desc "MUTATION_LEGS_333_DESC"
        passives {
            AddStatusToBasicAttack {
                Knockback 1
                VisualFXTile fx_windSpell
            }
            AddElementsToBasicAttack Wind
        }
    }
     
    334 { 
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
     
    335 { 
        desc "MUTATION_LEGS_335_DESC"
        
        passives {
            BleedThorns 1 
            StatusOnTookDamage {
                ChangeTilesUnder GlassTile 
            }
        } 
    }


    336 { 
        desc "MUTATION_LEGS_336_DESC"
        tag bird

        passives {
            AddStatusToBasicAttack {
                SoulLink 1
            } 
        }
    }


    337 { 
        desc "MUTATION_LEGS_337_DESC"
        passives {
            IgnoreTiles 1
        }
    }

    

    339 { 
        desc "MUTATION_LEGS_339_DESC"
        tag bird
        
        spd 2
        passives { 
            MoveAwayFromDamageSource BasicJump
        }
    }


    340 { 
        desc "MUTATION_LEGS_340_DESC"
        passives {
           StatusOnTookDamage {
               LuckUp 1
           }
        }
    }


    341 { 
        desc "MUTATION_LEGS_341_DESC"
        passives {
            AddStatusToBasicAttack { 
                FaceAway 1
            }
        }
    }

    

    343 { 
        desc "MUTATION_LEGS_343_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }
	
    754 { 
        desc "MUTATION_LEGS_754_DESC"  
        passives {
            ReplaceBasicMove ToadJump_BasicMove
		    AddStatusToBasicAttack {
                Bruise 1
            }	
        }
    }

    756 { 
		spd 2
    }
	
    757 { 
        desc "MUTATION_LEGS_757_DESC"  
        passives {
			Trample 3
        }
    }
	
    758 { 
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
	
    759 { 
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

    761 { 
        desc "MUTATION_LEGS_761_DESC"  
        passives {
            ReplaceBasicMove ToadJump_BasicMove
		    AddStatusToBasicAttack {
                Bleed 1
            }	
        }
    }

    762 { 
        desc "MUTATION_LEGS_762_DESC"

        passives {
            IgnoreTiles 1
            YOffset .25
        }
    }
	
    763 { 
        desc "MUTATION_LEGS_763_DESC"

        passives {
            IgnoreTiles 1
            YOffset .25
        }
    }
	



    900 { 
        desc "MUTATION_LEGS_900_DESC"

        passives {
            IgnoreTiles 1
            YOffset .25
        }
    }

        
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

    
    700 { 
        tag birth_defect
        str -2
    }
    701 { 
        tag birth_defect
        dex -2
    }
    702 { 
        tag birth_defect
        spd -2
    }
    703 { 
        desc "MUTATION_LEGS_703_DESC"

        tag birth_defect
        spd -2

        passives {
            WaterWalk 1
        }
    }
	704 { 
        tag birth_defect
        str -1
    }
	705 { 
        desc "MUTATION_LEGS_705_DESC"
        tag birth_defect
        speed -4 
        passives {
            Trample 3
        }
    }
	706 { 
        tag birth_defect
        spd -1
    }
	707 { 
        desc "MUTATION_LEGS_707_DESC"
        tag birth_defect
        str 1

        passives {
            Slow -1
        }
    }
}
```

</details>

---

### `mouth`
**Description:** Gain 1 health when you deal damage.  
**Source:** `mouth.gon`  

| Field | Value |
| :--- | :--- |
| Body Part | mouth |

<details>
<summary><b>Raw .gon</b></summary>

```
mouth {
    300 { 
        tag animal
        str 1
    }
    301 { 
        tag animal
        desc "MUTATION_MOUTH_301_DESC"

        passives {
            FlatHealWhenDealDamage 1
        }
    }
    302 { 
        desc "MUTATION_MOUTH_302_DESC"        

        passives {
            HealthRegenUp 1
        }
    }
    303 { 
        tag melted
        int 1
    }
    304 { 
        tag animal  
        desc "MUTATION_MOUTH_304_DESC"

        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }
    305 { 
        desc "MUTATION_MOUTH_305_DESC"
        passives {
            AddCorpseHealth 100
        }
    }
    306 { 
        desc "MUTATION_MOUTH_306_DESC"

        passives {
            SpawnThingOnDamage {
                object Fly
                good false 
                chance 10%
            }
        }
    }
    307 { 
        desc "MUTATION_MOUTH_307_DESC"

        passives {
            AddStatusToBasicAttack {
                Instakill [25, .01]
            }
        }
    }
    308 { 
        desc "MUTATION_MOUTH_308_DESC"

        passives {
            HealthRegenUp 1
        }
    }
    309 { 
        desc "MUTATION_MOUTH_309_DESC"

        passives {
            AddStatusToBasicAttack {
                Fear [1 .1]
            }
        }
    }
    310 { 
        cha 1
    }

    311 { 
        desc "MUTATION_MOUTH_311_DESC"

        passives {
            AddStatusToBasicAttack {
                Leeches 1
            }
        }
    }

    312 { 
        desc "MUTATION_MOUTH_312_DESC"
        str 1
        passives {
            AddStatusToBasicMeleeAttack {
                Immobile [1, .1]
            }
        }
    }

    313 { 
         desc "MUTATION_MOUTH_313_DESC"

         passives {
             StatusEachRoundEnd {
                UseAbility Spit
             }
         }
    }


    314 { 
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


    315 { 
        desc "MUTATION_MOUTH_315_DESC"

        passives { 
            StatusEachTurnBegin {
                Quivered [1, 0.1]
            }  
        }
    }


    316 { 
         desc "MUTATION_MOUTH_316_DESC"
         cha -1
         passives{
            AddStatusToBasicAttack {
                Bruise 1
            }
         }
    } 

    317 { 
        desc "MUTATION_MOUTH_317_DESC"
        passives {   
            BleedThorns 1 
            StatusOnTookDamage {
                ChangeTilesUnder GlassTile 
            }
        } 
    }


    318 { 
        desc "MUTATION_MOUTH_318_DESC"
        passives {
            ReplaceBasicMove_Mutation BasicDig
        }
    }


    319 { 
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

    





    321 { 
         shield 3
    }


    322 { 
        desc "MUTATION_MOUTH_322_DESC"
        passives{
            AddStatusToBasicAttack {
                Bleed 1
            }
        }
    }


    323 { 
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


    324 { 
        desc "MUTATION_MOUTH_324_DESC"      
        passives {
            AddBonusRange 1
        }
    }

    





    326 { 
        desc "MUTATION_MOUTH_326_DESC"
        passives { 
            StatusOnEatFood {
                HealthRegenUp 1 
            }
        }
    } 

    327 { 
        desc "MUTATION_MOUTH_327_DESC"
        passives { 
            AddLevelUpRerolls 1
        }
    }

    328 { 
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
	
    750 { 
        desc "MUTATION_MOUTH_750_DESC"
        passives { 
			AddStatusToBasicAttack {
                ChangeTile DirtTile
				VaporizeInanimate 1
            }	
        }
    }
	
    751 { 
		con 2
    }
	
    752 { 
        desc "MUTATION_MOUTH_752_DESC"
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        } 
    }
	
    754 { 
        desc "MUTATION_MOUTH_754_DESC"
		passives {
			DepressionAura 1
		}
    }
	
    755 { 
        desc "MUTATION_MOUTH_755_DESC"
		passives {
			ElementImmune Ice
		}
    }
	
    756 { 
		int 1
    }

    757 { 
        desc "MUTATION_MOUTH_757_DESC"
		passives {
			AddStatusToBasicAttack {
				Bleed 1
			}
		}
    }
	
    760 { 
        desc "MUTATION_MOUTH_760_DESC"
        passives {
            AbilityWhenTaggedCharacterMovesNear {
                ability move
                tag food
                range 2
            }
        }
    }

    900 { 
        desc "MUTATION_MOUTH_900_DESC"

        passives {
            AddStatusToBasicAttack {
                Fear [1 .1]
            }
        }
    }


    1500 { 
        tag animal
        desc "MUTATION_MOUTH_1500_DESC"

        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }

    1026 { 
        tag animal
        desc "MUTATION_MOUTH_1026_DESC"

        passives {
            AddStatusToBasicAttack {
                Webbed [1 .1]
            }
        }
    }


    
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


    
    700 { 
        tag birth_defect
        cha -2
    }
    701 { 
        tag birth_defect
        str -1
        dex -1
    }
	-2 { 
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
	703 { 
        tag birth_defect
        int -2
		con 1
    }
	704 { 
        tag birth_defect
        cha -2
		str 1
    }

    705 { 
        desc "MUTATION_MOUTH_705_DESC"

        attack FetusSpit
        passives {
            ExtraBasicAttacks 2
            ReplaceBasicAttack_Mutation FetusSpit
        }
    }
}
```

</details>

---

### `tail`
**Description:** Poop when you take damage.  
**Source:** `tail.gon`  

| Field | Value |
| :--- | :--- |
| Body Part | tail |

<details>
<summary><b>Raw .gon</b></summary>

```
tail {

    300 { 
        tag extra    
        str 1
    }

    301 { 
        tag animal
        desc "MUTATION_TAIL_301_DESC"

        passives {
            PoopWhenHit Poop
        }
    }

    302 { 
        tag animal
        desc "MUTATION_TAIL_302_DESC"

        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }

    303 { 
        desc "MUTATION_TAIL_303_DESC"

        passives {
            AddStatusToBasicAttack {
                Stun [1, .05]
            }
        }
    }

    304 { 
        tag animal
        dex 1
    }

    305 { 
        desc "MUTATION_TAIL_305_DESC"

        passives {
            Thorns 1
        }
    }

    306 { 
        con 1
    }

    307 { 
        spd 1
    }

    308 { 
        desc "MUTATION_TAIL_308_DESC"

        lck 1
        passives {
            DodgeChance 5%
        }
    }
    
    309 { 
        tag animal
        cha 1
    }
    
    310 { 
        desc "MUTATION_TAIL_310_DESC"

        passives {
            AddTemporaryEffectsToBasicAttack {
                Fury 10
            }
        }
    }
    
    311 { 
        desc "MUTATION_TAIL_311_DESC" 
        passives {        
            Thorns 1 
        } 
    }
    
    312 { 
        divine_shield 1
    } 

    313 { 
        desc "MUTATION_TAIL_313_DESC" 
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        } 
    } 

    314 { 
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

    315 { 
        desc "MUTATION_TAIL_315_DESC"  
        passives {
            SpawnThingOnDamage {
                object Maggot
                good false 
                chance 20%
            }
        }
    }

    316 { 
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

    317 { 
        desc "MUTATION_TAIL_317_DESC" 
        passives {
            AbilityReaction SkunkTail
        }
    }

    318 { 
        desc "MUTATION_TAIL_318_DESC" 
        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        } 
    }

    319 { 
        desc "MUTATION_TAIL_319_DESC" 
        passives {
            PoisonThorns 1
        } 
    }

    320 { 
        desc "MUTATION_TAIL_320_DESC" 
        passives {
            Bleed 1 
            BleedThorns 2                
        } 
    }

    321 { 
        tag extra
        int 1
    }
    
    322 { 
        desc "MUTATION_TAIL_322_DESC" 
        passives {     
            StatusEachTurnBegin {
                SpeedUp 1
            }
        } 
    }

    323 { 
        desc "MUTATION_TAIL_323_DESC" 
        passives {
            ReplaceBasicMove_Mutation BasicJump
        } 
    }

    324 { 
        spd 2 
    }
    
    325 { 
        desc "MUTATION_TAIL_325_DESC" 
        passives {
            MeleeRevengeDamage {
                knockback 2
            }
        } 
    }

    326 { 
        desc "MUTATION_TAIL_326_DESC" 
        passives {
            Bruise 1
            DodgeChance 10%

        }
    }

    327 { 
        desc "MUTATION_TAIL_327_DESC" 
        passives {
            StatusIfDidntMove {
                Charge 3
            }
        } 
    }

    

    329 { 
        desc "MUTATION_TAIL_329_DESC" 
        passives {   
            CanRemoveCursedItems 1
        } 
    }

    

    331 { 
        desc "MUTATION_TAIL_331_DESC"
        passives { 
            AddLevelUpRerolls 1
        } 
    }

    332 { 
        desc "MUTATION_TAIL_332_DESC"
        passives { 
            ReflectProjectiles 25%
        }
    }

    

    334 { 
        desc "MUTATION_TAIL_334_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 1 
            }
            AddElementsToBasicAttack Fire
        } 
    }

    

    336 { 
        desc "MUTATION_TAIL_336_DESC"
        passives {
            Thorns 1
        }
    }

    337 { 
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

    338 { 
        desc "MUTATION_TAIL_338_DESC"

        passives {
            AddStatusToBasicAttack {
                Burn 1 
            }
            AddElementsToBasicAttack Fire
        } 
    }

    339 { 
        desc "MUTATION_TAIL_339_DESC"

        passives {
            PassiveWhenAtFullMana {
                DamageUp 2
            }
        }
    }

    

    341 { 
        desc "MUTATION_TAIL_341_DESC" 
        passives {
            StatusOnTookDamage {
                Charge 1
            }
        } 
    }
    342 { 
        desc "MUTATION_TAIL_342_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }

	750 { 
		cha 1
    }

	751 { 
        desc "MUTATION_TAIL_751_DESC"  
        passives {
			Brace 1
        }
    }
	
	752 { 
		con 1
    }
	
	/*753 { 
        passives {

        }
    }*/
	
	754 { 
        desc "MUTATION_TAIL_754_DESC"  
        passives {
			Thorns 1
        }
    }
	
	755 { 
        desc "MUTATION_TAIL_755_DESC"  
        passives {
            WaterWalk 1
        }
    }
	
	756 { 
        desc "MUTATION_TAIL_756_DESC"  
        passives {
			BleedThorns 1
        }
    }
	
	757 { 
        desc "MUTATION_TAIL_757_DESC"  
        passives {
            ReplaceBasicMove Shadowstep
        }
    }
	
	759 { 
        desc "MUTATION_TAIL_759_DESC"  
		passives {
			Quivered 1
		}
    }
      
	760 { 
        desc "MUTATION_TAIL_760_DESC"  
        passives {
            BackflipWhenTargeted {
                stacks 2
                ability BackflipDodge
            }
        }
    }
      

    900 { 
        spd 1
    }

    1500 { 
        tag animal
        dex 1
    }

        
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


    
    700 { 
        tag birth_defect
        lck -2
    }
    701 { 
        tag birth_defect
        spd -1
        cha -1
    }
	-2 { 
        tag birth_defect
        dex -1
    }
	703 { 
        desc "MUTATION_TAIL_703_DESC"
        tag birth_defect
        con 1

        passives {
            Immobile 1
        }
    }
	704 { 
        desc "MUTATION_TAIL_704_DESC"
        tag birth_defect
        lck -2

        passives {
            MulticlassLevelUp Hunter
        }
    }
}
```

</details>

---

### `texture`
**Description:** +1 Health Regeneration  
**Source:** `texture.gon`  

| Field | Value |
| :--- | :--- |
| Body Part | texture |

<details>
<summary><b>Raw .gon</b></summary>

```
texture {
    300 { 
        desc "MUTATION_TEXTURE_300_DESC"

        cha -1
        passives {
            HealthRegenUp 1
        }
    }

    301 { 
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

    302 { 
        lck 1
    }

    303 { 
        desc "MUTATION_TEXTURE_303_DESC"

        passives {
            RandomStatUp 1
        }
    }

    304 { 
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

    305 { 
        int 1
    }

    306 { 
        str 1
    }

    307 { 
        desc "MUTATION_TEXTURE_307_DESC"

        passives {
            DodgeChance 5%
        }
    }

    308 { 
        cha 1
    }

    309 {
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

    310 { 
        desc "MUTATION_TEXTURE_310_DESC"

        passives {
            AddLootMultiplier 1
        }
    }
	
    750 { 
        desc "MUTATION_TEXTURE_750_DESC"

        passives {
            PoisonThorns 2
        }
    }

       
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


    
    700 { 
        tag birth_defect
        cha -2
    }
    701 { 
        tag birth_defect
        cha -2
        shield 1
    }
	702 { 
        desc "MUTATION_TEXTURE_702_DESC"
        tag birth_defect

        passives {
            Bleed 1
        }
    }
	703 { 
        desc "MUTATION_TEXTURE_703_DESC"
        tag birth_defect
        cha -2

        passives {
            MulticlassLevelUp Mage
        }
    }
	704 { 
        desc "MUTATION_TEXTURE_704_DESC"
        tag birth_defect
        cha -2

        passives {
            MulticlassLevelUp Fighter
        }
    }
	705 { 
        desc "MUTATION_TEXTURE_705_DESC"
        tag birth_defect
        cha -2

        passives {
            MulticlassLevelUp Thief
        }
    }
	706 { 
        desc "MUTATION_TEXTURE_706_DESC"
        tag birth_defect
        cha -1

        passives {
            DodgeChance_Status 10
        }
    }
}
```

</details>

---

