# Cats and Classes/Mutations Directory

<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Abilities</strong></td>
    <td><a href="../Abilities/Ability_Pools.md">Ability Pools</a> • <a href="../Abilities/Cat_Abilities.md">Cat Abilities</a> • <a href="../Abilities/Enemy_and_Boss_Abilities.md">Enemy & Boss Abilities</a> • <a href="../Abilities/System_and_Item_Abilities.md">System & Item Abilities</a></td>
  </tr>
  <tr>
    <td><strong>Cats and Classes</strong></td>
    <td><a href="../Cats_and_Classes/Cat_Quotes.md">Cat Quotes</a> • <a href="../Cats_and_Classes/Classes.md">Classes</a> • <a href="../Cats_and_Classes/Custom_Cats.md">Custom Cats</a> • <a href="../Cats_and_Classes/Mutations.md">Mutations</a> • <a href="../Cats_and_Classes/Special_Strays.md">Special Strays</a> • <a href="../Cats_and_Classes/Tutorial_Cats.md">Tutorial Cats</a></td>
  </tr>
  <tr>
    <td><strong>Enemies and Combat</strong></td>
    <td><a href="../Enemies_and_Combat/Boss_Cutscene_Info.md">Boss Cutscene Info</a> • <a href="../Enemies_and_Combat/Combat_Rewards.md">Combat Rewards</a> • <a href="../Enemies_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Enemies_and_Combat/Enemies_and_Characters.md">Enemies & Characters</a> • <a href="../Enemies_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Enemies_and_Combat/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../Enemies_and_Combat/Team_Names.md">Team Names</a></td>
  </tr>
  <tr>
    <td><strong>Items and Passives</strong></td>
    <td><a href="../Items_and_Passives/Item_Pools.md">Item Pools</a> • <a href="../Items_and_Passives/Item_Set_Bonuses.md">Item Set Bonuses</a> • <a href="../Items_and_Passives/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Items_and_Passives/Passive_Pools.md">Passive Pools</a> • <a href="../Items_and_Passives/Passives.md">Passives</a></td>
  </tr>
  <tr>
    <td><strong>Statuses and Injuries</strong></td>
    <td><a href="../Statuses_and_Injuries/Disorders.md">Disorders</a> • <a href="../Statuses_and_Injuries/Injuries.md">Injuries</a> • <a href="../Statuses_and_Injuries/Status_Effect_Keywords.md">Status Effect Keywords</a> • <a href="../Statuses_and_Injuries/Statuses.md">Statuses</a></td>
  </tr>
  <tr>
    <td><strong>System and Engine</strong></td>
    <td><a href="../System_and_Engine/Damage_Text_Styles.md">Damage Text Styles</a> • <a href="../System_and_Engine/Difficulties.md">Difficulties</a> • <a href="../System_and_Engine/Particles_and_VFX_Dictionary.md">Particles & VFX Dictionary</a> • <a href="../System_and_Engine/Progression_Unlocks.md">Progression Unlocks</a></td>
  </tr>
  <tr>
    <td><strong>World and Events</strong></td>
    <td><a href="../World_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_and_Events/Furniture_and_Metaprogression.md">Furniture & Metaprogression</a> • <a href="../World_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_and_Events/Map_Generation_and_Routing.md">Map Generation & Routing</a> • <a href="../World_and_Events/NPC_Scripts.md">NPC Scripts</a> • <a href="../World_and_Events/Shops.md">Shops</a></td>
  </tr>
</table>

</details>

## File: `body.gon`

### `body`
**Description:** +1 Thorns.  
**Source:** `body.gon`  

**Localization Strings:**
- `MUTATION_BODY_309_DESC`: "Units that contact you get knocked back 2 tiles."
- `MUTATION_BODY_312_DESC`: "Spawn a coin when you take damage."
- `MUTATION_BODY_313_DESC`: "+1 Kinetic Spikes."
- `MUTATION_BODY_314_DESC`: "+2 Thorns."
- `MUTATION_BODY_315_DESC`: "+1 Brace."
- `MUTATION_BODY_317_DESC`: "Immune to Heat Wave weather."
- `MUTATION_BODY_318_DESC`: "25% chance to spawn a Charmed Fly each turn."
- `MUTATION_BODY_319_DESC`: "When you take damage from an attack, gain a random buff."
- `MUTATION_BODY_321_DESC`: "Spawn a Charmed Kitten familiar when you get downed."
- `MUTATION_BODY_322_DESC`: "Gain an extra consumable item at the end of each battle."
- `MUTATION_BODY_323_DESC`: "Trample. When damaged, move 1 tile in a random direction."
- `MUTATION_BODY_324_DESC`: "Gain +1 range when you get a kill."
- `MUTATION_BODY_750_DESC`: "+1 Thorns."
- `MUTATION_BODY_758_DESC`: "Start with +1 Bonus Attack."
- `MUTATION_BODY_703_DESC`: "Start each battle with Bruise 1."

```
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

---

## File: `ears.gon`

### `ears`
**Description:** +1 Health and Mana Regeneration while wet.  
**Source:** `ears.gon`  

**Localization Strings:**
- `MUTATION_EARS_303_DESC`: "Adds +1 Knockback to your basic attack if it's melee."
- `MUTATION_EARS_309_DESC`: "Adds +1 Bleed to your basic attack."
- `MUTATION_EARS_313_DESC`: "Adds +1 Knockback to your basic attack if it's melee."
- `MUTATION_EARS_314_DESC`: "Thorns 1. Your basic attack inflicts Bleed if it's melee."
- `MUTATION_EARS_315_DESC`: "50% chance to spawn a Charmed Fly each turn. Start with Poison 1."
- `MUTATION_EARS_316_DESC`: "You can see hidden things. 5% dodge chance."
- `MUTATION_EARS_317_DESC`: "Whenever you down a unit, you have a 10% chance to reanimate that unit with 50% HP."
- `MUTATION_EARS_318_DESC`: "You have Brace 1 while wet."
- `MUTATION_EARS_319_DESC`: "Gain +1 Charge when you take damage."
- `MUTATION_EARS_320_DESC`: "+1 Kinetic Spikes."
- `MUTATION_EARS_321_DESC`: "Units that contact you get knocked back 1 tile."
- `MUTATION_EARS_323_DESC`: "Gain 1 HP when your basic attack deals damage."
- `MUTATION_EARS_325_DESC`: "If you're wet, gain +1 Charge and +1 [img:shield] at the end of your turn."
- `MUTATION_EARS_326_DESC`: "5% chance to spawn a Maggot familiar each turn."
- `MUTATION_EARS_327_DESC`: "An extra food pickup will spawn in each battle."
- `MUTATION_EARS_328_DESC`: "5% chance to Petrify on damage and when hit."
- `MUTATION_EARS_329_DESC`: "Your basic attack leaves water tiles."
- `MUTATION_EARS_330_DESC`: "Thorns 1. 10% chance to inflict Immobile on units that contact you."
- `MUTATION_EARS_331_DESC`: "Your basic attack has +1 Knockback."
- `MUTATION_EARS_332_DESC`: "Brace 1."
- `MUTATION_EARS_334_DESC`: "Spawn 1-3 more coins/scrap around the map on random tiles at the start of each battle."
- `MUTATION_EARS_335_DESC`: "Start with Bleed 1 and a bonus attack."
- `MUTATION_EARS_336_DESC`: "You gain 3 mana at the end of your turn if you didn't use your movement action."
- `MUTATION_EARS_337_DESC`: "Your basic attack inflicts Burn 1."
- `MUTATION_EARS_338_DESC`: "Your basic attack has a 15% chance to inflict Freeze."
- `MUTATION_EARS_339_DESC`: "You have electric immunity."
- `MUTATION_EARS_341_DESC`: "10% chance to backflip when targeted."
- `MUTATION_EARS_342_DESC`: "20% chance to spawn a Charmed Flea when damaged."
- `MUTATION_EARS_343_DESC`: "Thorns 1."
- `MUTATION_EARS_344_DESC`: "Spawn a Charmed Kitten familiar when you get downed."
- `MUTATION_EARS_345_DESC`: "Units that contact or attack you have a 15% chance to get Charmed."
- `MUTATION_EARS_750_DESC`: "Your movement action is a jump."
- `MUTATION_EARS_751_DESC`: "+10% dodge chance."
- `MUTATION_EARS_752_DESC`: "You have +2 Damage while wet."
- `MUTATION_EARS_753_DESC`: "+1 Knockback damage. Your basic attack has +1 Knockback."
- `MUTATION_EARS_754_DESC`: "Electric damage you deal is increased by 1."
- `MUTATION_EARS_755_DESC`: "Gain +1 Charge every time you cast a spell."
- `MUTATION_EARS_900_DESC`: "+10% dodge chance."
- `MUTATION_EARS_1500_DESC`: "+2% dodge chance"
- `MUTATION_EARS_703_DESC`: "Start each battle with Confusion 2."
- `MUTATION_EARS_704_DESC`: "Start each battle with Immobile 1."

```
ears {
    300 { //horn
        tag animal
        str 1 //designed as: +1 melee damage
    }
    301 { //antenna
        tag animal
        int 1 //designed as +1 mana regen
    }
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
    304 { //pigtails
        cha 1
    }
    305 { //boil
        shield 1
    }
    306 { //bunny ear
        tag animal
        spd 1
    }
    307 { //brains
        int 1
    }
    308 { //shrek
        str 1
        cha -1
    }
    309 { //antlers
        tag animal
        desc "MUTATION_EARS_309_DESC"

        passives {
            AddStatusToBasicAttack {
                Bleed 1
            }
        }
    }
    310 { //human
        int 1
    }

    //311 { //TODO(no effect or comment here???)
    //
    //}


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


    316 { //Bat Ears
        tag animal
        desc "MUTATION_EARS_316_DESC"

        passives {
            ShowHiddenThings 1
            DodgeChance 5%
        }
    }

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

    319 { // Pierced Ears
        tag animal
        desc "MUTATION_EARS_319_DESC"

        passives {
            StatusOnTookDamage {
                Charge 1
            }
        }
    }

    320 { // Alien Ears
        desc "MUTATION_EARS_320_DESC"

        passives {
            KineticSpikes 1 
        }
    }


    
    321 { // Spring Ears
        desc "MUTATION_EARS_321_DESC"

        passives {
            MeleeRevengeDamage {
                knockback 1
            }
        }
    }


    322 { // Lamb Ears 
        tag animal
        cha 1 
    }

    323 { // Vamp Ears
        desc "MUTATION_EARS_323_DESC"

        passives {
            AddStatusToBasicAttack {
                FlatLeech 1
            } 
        }
    }

    // // Tyler to add % chance
    // 324 { // Extra Paw
    //     desc "10% chance of counter attack when hit"
    //     tag extra
    //
    //     passives {   
    //         CounterAttack { 
    //             chance 10%
    //         }
    //     }
    // }

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

    326 { // Worm Ear
        desc "MUTATION_EARS_326_DESC"

        passives {
            SpawnEachTurn {
                chance 5%
                object  CharmedMaggot
            } 
        }
    }

    327 { // Ant Antenna
        tag animal
        desc "MUTATION_EARS_327_DESC"
            passives {
                SpawnOnBattleStartRandomEmptyTile {
                    object RandomFoodPickup 
                }
            } 
    }

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

    330 { // Hook Ears
        desc "MUTATION_EARS_330_DESC"
        passives {
            Thorns 1
            MeleeRevengeDamage {
                Immobile 10%
            }
        }
    }

    331 { // Mace Ears
        desc "MUTATION_EARS_331_DESC"
        passives {
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }

    332 { // Blubber Lobes
        desc "MUTATION_EARS_332_DESC"
        passives {
            Brace 1
        }
    }
    
    333 { // Metal Plate
        shield 3 
    }

    334 { // Metal Detector
        desc "MUTATION_EARS_334_DESC"
        passives {
            SpawnOnBattleStartRandomEmptyTile {
                object Coin
                number [1 3]
            }
        }
    }

    335 { // Docked Ears
        desc "MUTATION_EARS_335_DESC"
        passives { 
            Bleed 1 
            Quivered 1
        }
    }

    336 { // Large Leaves
        desc "MUTATION_EARS_336_DESC"
        passives {
            StatusIfUnusedMovePoints {
                ManaGain 3 
            } 
        }
    }

    337 { // Burning ears
        desc "MUTATION_EARS_337_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 1
            }
        }
    }
    
    338 { // Frozen ears
        desc "MUTATION_EARS_338_DESC"
        passives {
            MeleeRevengeDamage {
                Freeze [1 0.15]
            }
        }
    }

    339 { // Lightning Rods
        desc "MUTATION_EARS_339_DESC"
        passives { 
            ElementImmune Electric
        }
    }

    
    340 { // Aura Ears
        divine_shield 1
    }

    341 { //Large Ears 
        desc "MUTATION_EARS_341_DESC" 
        passives {
            ChanceToBackflip {
                ability BackflipDodge
                chance 10%
            } 
        }
    }

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

    343 { //Long Antlers
        tag animal
        desc "MUTATION_EARS_343_DESC" 
        passives {        
            Thorns 1 
        } 
    }

    344 { //Kitten
        desc "MUTATION_EARS_344_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }

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
    
    750 { //Jackrabbit Ears
        tag animal
        desc "MUTATION_EARS_750_DESC"  

        passives {
            ReplaceBasicMove_Mutation BasicJump
        }
    }

    751 { // Folded Ears
        desc "MUTATION_EARS_751_DESC" 
        passives {
            DodgeChance 10%
        }
    }

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
    
    755 { // Head Ferns
        desc "MUTATION_EARS_755_DESC" 
        passives { 
            StatusOnCastSpell {
                Charge 1
            }   
        }
    }


    900 { //slender
        desc "MUTATION_EARS_900_DESC"

        passives {
            DodgeChance 10%
        }
    }


    1500 { //rat ears
        tag animal
        desc "MUTATION_EARS_1500_DESC"

        passives {
            DodgeChance 2%
        }
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

    //Birth Defects
    700 { //anotia
        tag birth_defect
        lck -2
    }
    701 { //turner syndrome
        tag birth_defect
        int -2
    }
	702 { //underdeveloped ears
        tag birth_defect
        cha -1
    }
	703 { //low ears
        desc "MUTATION_EARS_703_DESC"
        tag birth_defect

        passives {
            Confusion 2
        }
    }
	704 { //wilted ears
        desc "MUTATION_EARS_704_DESC"
        tag birth_defect

        passives {
            Immobile 1
        }
    }
	-2 { //no ears (completely missing part) //TODO: deaf (unaffected by musical abilities)
        tag birth_defect
        dex -2
    }
}
```

---

## File: `eyebrows.gon`

### `eyebrows`
**Description:** You have a 10% chance to inflict Confusion on units who contact or attack you.  
**Source:** `eyebrows.gon`  

**Localization Strings:**
- `MUTATION_EYEBROWS_306_DESC`: "You have a 5% chance to inflict Fear on units who contact or attack you."
- `MUTATION_EYEBROWS_307_DESC`: "+1 Mana Regeneration. +1 Health Regeneration."
- `MUTATION_EYEBROWS_309_DESC`: "+1 Thorns."
- `MUTATION_EYEBROWS_310_DESC`: "+1 Range."
- `MUTATION_EYEBROWS_311_DESC`: "When you cast your third spell each turn, heal 2."
- `MUTATION_EYEBROWS_313_DESC`: "Spawn 1-2 extra pickups in each battle."
- `MUTATION_EYEBROWS_314_DESC`: "When an allied cat dies, gain +2 Damage."
- `MUTATION_EYEBROWS_315_DESC`: "You can reroll your options when you level up."
- `MUTATION_EYEBROWS_900_DESC`: "+5% dodge chance. Your basic attack has a 1% chance to inflict Freeze."

```
eyebrows {
    300 { // Bolt Brows
        spd 1
    }

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

    302 { // Metal Brows
        shield 2
    }

    303 { // Fancy Makeup
        cha 1
    }

    304 { // Wolfy Brows
        tag animal
        dex 1
    }

    305 { // Dotty Brows
        lck 1
    }

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

    307 { // Antennae
        desc MUTATION_EYEBROWS_307_DESC

        passives {
            HealthRegenUp 1
            AddManaRegen 1
        }
    }

    308 { // Long Lashes
        cha 1
    }

    309 { // Spiny Brows
        desc MUTATION_EYEBROWS_309_DESC

        passives {
            Thorns 1
        }
    }

    310 { //Extra Eye
        desc MUTATION_EYEBROWS_310_DESC
        tag extra

        passives {
            AddBonusRange 1
        }
    }

    311 { //Stacked Brows
        desc MUTATION_EYEBROWS_311_DESC

        passives { 
            StatusEveryXSpellCastsEachTurn {
                stacks 3
                HealthGain 2
            }
        }
    } 

    //312 { //
    //}
    
    313 { //Square Glasses
        desc MUTATION_EYEBROWS_313_DESC
    
        passives { 
            SpawnExtraThingsOnBattleStart {
                object RandomPickup
                number [1 2]
            }
        }
    }

    314 { // Holy Brows
        desc MUTATION_EYEBROWS_314_DESC

        passives {
            StatusOnAllyCatDeath {
                DamageUp 2
            }
        }
    } 

    315 { //Triangle Eyes
        desc MUTATION_EYEBROWS_315_DESC

        passives { 
            AddLevelUpRerolls 1
        }
    }

    900 { //slender
        desc MUTATION_EYEBROWS_900_DESC

        passives {
            AddStatusToBasicAttack {
                Freeze [1 .01]
            }
            DodgeChance 5%
        }
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
	
    //Birth Defects
    700 { //bushy
        tag birth_defect
        lck -1
    }
	701 { //no eyebrows
        tag birth_defect
        cha -1
    }
	702 { //unibrow
        tag birth_defect
        int -1
    }
    -2 { //no eyebrows (completely missing part)
        tag birth_defect
        cha -2
    }
}
```

---

## File: `eyes.gon`

### `eyes`
**Description:** Your basic attack has a 10% chance to inflict Fear.  
**Source:** `eyes.gon`  

**Localization Strings:**
- `MUTATION_EYES_302_DESC`: "+1 Thorns."
- `MUTATION_EYES_304_DESC`: "Take your turn later."
- `MUTATION_EYES_306_DESC`: "Your basic attack has a 10% chance to inflict Confusion 3."
- `MUTATION_EYES_307_DESC`: "Gain 1 mana when anything dies."
- `MUTATION_EYES_308_DESC`: "+5% dodge chance."
- `MUTATION_EYES_309_DESC`: "+2 corpse health."
- `MUTATION_EYES_310_DESC`: "+1 Health Regeneration"
- `MUTATION_EYES_311_DESC`: "You do not take extra damage from backstabs."
- `MUTATION_EYES_312_DESC`: "+1 Brace."
- `MUTATION_EYES_313_DESC`: "Your basic attack creates water tiles."
- `MUTATION_EYES_314_DESC`: "When you are downed, spawn 3 Flies. +2 corpse health."
- `MUTATION_EYES_315_DESC`: "+1 Kinetic Spikes."
- `MUTATION_EYES_316_DESC`: "15% chance to counter attack with Chain Lightning when you get hit."
- `MUTATION_EYES_317_DESC`: "Gain a random stat up at the end of each turn."
- `MUTATION_EYES_318_DESC`: "You can see hidden things. +1 Knockback damage."
- `MUTATION_EYES_319_DESC`: "Blind. +1 Damage. +1 Thorns."
- `MUTATION_EYES_324_DESC`: "Spawn 2 extra coins each battle."
- `MUTATION_EYES_325_DESC`: "Thorns 1."
- `MUTATION_EYES_326_DESC`: "Gain 2 Charge each time you cast 4 spells."
- `MUTATION_EYES_328_DESC`: "+10% crit chance."
- `MUTATION_EYES_329_DESC`: "Your basic attack has a 15% chance to inflict Confusion."
- `MUTATION_EYES_331_DESC`: "At the start of each battle, gain a random temporary pill if your trinket slot is empty."
- `MUTATION_EYES_332_DESC`: "Start each battle Bleeding. Gain 1 Charge each time you take damage."
- `MUTATION_EYES_333_DESC`: "Your basic attack can't miss."
- `MUTATION_EYES_334_DESC`: "Blind. Spawn a Flea when you take damage."
- `MUTATION_EYES_335_DESC`: "Your basic attack has a 10% chance to Charm."
- `MUTATION_EYES_336_DESC`: "Your basic attack is electric element and has a 5% chance to stun."
- `MUTATION_EYES_337_DESC`: "Your basic attack is ice element and inflicts Slow."
- `MUTATION_EYES_338_DESC`: "Your basic attack inflicts Burn."
- `MUTATION_EYES_339_DESC`: "+1 Health Regeneration while wet. Your basic attack is water element."
- `MUTATION_EYES_340_DESC`: "Your basic attack inflicts Leech."
- `MUTATION_EYES_341_DESC`: "Gain Charge 1 the first time you move each turn."
- `MUTATION_EYES_342_DESC`: "Your basic attack inflicts Poison 1. Start each battle Poisoned."
- `MUTATION_EYES_343_DESC`: "You have a 5% chance to inflict Fear on units who contact or attack you."
- `MUTATION_EYES_344_DESC`: "You have a 10% chance to Blind units who contact or attack you."
- `MUTATION_EYES_345_DESC`: "Inflict a random debuff on units who contact you."
- `MUTATION_EYES_346_DESC`: "Spawn a rock when damaged."
- `MUTATION_EYES_347_DESC`: "Your basic attack has a 15% chance to inflict Confusion 2."
- `MUTATION_EYES_348_DESC`: "+1 range, +1 reach."
- `MUTATION_EYES_349_DESC`: "Emit 4 Sparkles each time you cast 8 spells."
- `MUTATION_EYES_351_DESC`: "Your bonus ability is a different random spell each battle."
- `MUTATION_EYES_352_DESC`: "You have All Stats Up while Bleeding."
- `MUTATION_EYES_353_DESC`: "You take no extra damage from backstabs."
- `MUTATION_EYES_442_DESC`: "10% chance to reflect projectiles."
- `MUTATION_EYES_754_DESC`: "+1 range. Your basic attack is gravity element."
- `MUTATION_EYES_755_DESC`: "Your basic attack has a 15% chance to inflict Fear."
- `MUTATION_EYES_900_DESC`: "Your basic attack has a 10% chance to inflict Slow."
- `MUTATION_EYES_M2_DESC`: "Blind."
- `MUTATION_EYES_704_DESC`: "10% miss chance."
- `MUTATION_EYES_705_DESC`: "Gain 5% miss chance every turn."
- `MUTATION_EYES_706_DESC`: "Start each battle with Confusion 2."
- `MUTATION_EYES_1029_DESC`: "+5% crit chance."

```
eyes {
    300 { //Button Eyes
        desc "MUTATION_EYES_300_DESC"

        passives {
            AddStatusToBasicAttack {
                Fear [1 .1]
            }
        }
    }
    301 { //Demon Eyes  
        dex 1
    }
    302 { //Pop Eyes 
        desc "MUTATION_EYES_302_DESC"
        passives {
            Thorns 1
        }
    }
    303 { //Gem Eyes  
        int 1
        cha 1
    }
    304 { //Holes  
        desc "MUTATION_EYES_304_DESC"
        passives {
            AddInitiative -20
        }
    }
    305 { //Zen Eyes  
        str -1
        dex -1
        int 3
    }

    306 { //Confusing Eyes
        desc "MUTATION_EYES_306_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [3, .1]
            }
        }
    }
    307 { //Half Moon Eyes
        desc "MUTATION_EYES_307_DESC"
        passives {
            GainManaWhenAnythingDies 1
        }
    }
    308 { //Spider Eyes
        tag animal
        desc "MUTATION_EYES_308_DESC"
        passives {
            DodgeChance 5%
        }
    }
    309 { //Doll Eyes
        desc "MUTATION_EYES_309_DESC"
        passives {
            AddCorpseHealth 2
        }
    }
    310 { //Octo Eyes
        tag animal
        desc "MUTATION_EYES_310_DESC"
        passives {
            HealthRegenUp 1
        }
    }
    311 { //gecko eye
        tag animal
        desc "MUTATION_EYES_311_DESC"
        passives {
            BackstabImmunity 1
        }
    }

    312 { // Metal Eyes
        desc "MUTATION_EYES_312_DESC"
        shield 1
        passives {
            Brace 1
        }
    }

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

    314 { // Dead Eyes
        desc "MUTATION_EYES_314_DESC"
        passives {
            SpawnOnDowned CharmedFly
            SpawnOnDowned CharmedFly
            SpawnOnDowned CharmedFly
            AddCorpseHealth 2
        }
    }
   
    315 { // Kinetic eyes
        desc "MUTATION_EYES_315_DESC"
        passives {
            KineticSpikes 1
        }
    }
   
    316 { // Lightning eyes
        desc "MUTATION_EYES_316_DESC"
        passives { 
            CounterAttack {
                chance 15%
                ability ChainLightning
            }
        }
    }

    317 { // Dice Eyes
        desc "MUTATION_EYES_317_DESC"
        passives { 
            StatusEachTurnEnd {
                RandomStatUp 1
            } 
        }
    }
  
    318 { // Goat Eyes
        tag animal
        desc "MUTATION_EYES_318_DESC"
        passives {
            ShowHiddenThings 1
            AddKnockbackDamage 1
        }
    }

    319 { // Horn Eyes
        desc "MUTATION_EYES_319_DESC"
        passives {
            Blind -1  
            Thorns 1
            DamageUp 1
        }
    }
   
    //320{ // Odd Eyes
    //    desc ""
    //    passives {
    //
    //    }
    //}
    //   
    //321{ // Robo Eyes
    //    desc ""
    //    passives {
    //
    //    }
    //}
    //
    //   
    //323{ // Alien Eyes
    //    desc ""
    //    passives {
    //
    //    }
    //}

    324 { // Treasure Eyes
        desc "MUTATION_EYES_324_DESC"
        passives {
            SpawnOnBattleStartRandomEmptyTile {
                object Coin
                number 2
            }
        }
    }

    325 { // Nail Eyes
        desc "MUTATION_EYES_325_DESC"
        passives {
            Thorns 1
        }
    }

    326 { // 4 Eyes
        desc "MUTATION_EYES_326_DESC"
        passives {
            StatusEveryXSpellCasts {
                stacks 4
                Charge 2
            }
        }
    }

    327 { // Baby Blue Eyes
        cha 2 
    }

    328 { // Bull's Eye'
        tag animal
        desc "MUTATION_EYES_328_DESC"
        
        passives {
            CritChanceUp 10
        }
    }

    329 { // Spinning Eyes
        desc "MUTATION_EYES_329_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [1, .15]
            }
        }
    }

    //330 { // Crow Eyes
    //    desc "10% chance lethal damage only brings you to 1 hp"
    //    passives {
    //        
    //    }
    //}

    331 { // Glassy Eyes
        desc "MUTATION_EYES_331_DESC"
        passives {
            EquipRandomTemporaryItemFromPool pills
        }
    }

    332 { // Bleeding Eyes
        desc "MUTATION_EYES_332_DESC"
        passives {
            Bleed 1  
            StatusOnTookDamage {
                Charge 1
            }
        }
    }
    
    333 { // Huge Eyes
        desc "MUTATION_EYES_333_DESC"
        passives {
            BasicAttackCantMiss 1
        }
    }

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
        
    335 { // Fake Eyelashes
        desc "MUTATION_EYES_335_DESC"
        passives {
            AddStatusToBasicAttack {
                Charmed [1, .10]  
            }
        }
    }
            
    336 { // Bolt Eyes
        desc "MUTATION_EYES_336_DESC" 
        passives { 
            AddElementsToBasicAttack Electric
            AddStatusToBasicAttack {
                Stun [1 .05]
            }
        }
    }
        
    337 { // Ice Eyes
        desc "MUTATION_EYES_337_DESC"
        passives {
            AddStatusToBasicAttack {
                Slow 1
            }
            AddElementsToBasicAttack Ice
        }
    }

    338 { // Fire Eyes
        desc "MUTATION_EYES_338_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 1
            }
            AddElementsToBasicAttack Fire
        }
    }

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

    340 { // Leech Eyes
        desc "MUTATION_EYES_340_DESC"
        passives {
            AddStatusToBasicAttack {
                Leeches 1
            }
        }
    }

    
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

    342 { // Poison Eyes
        desc "MUTATION_EYES_342_DESC"
        passives { 
            AddStatusToBasicAttack {
                Poison 1
            } 
            Poison 1
        }
    }

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

    347 { // Hypno Eyes
        desc "MUTATION_EYES_347_DESC"
        passives {
            AddStatusToBasicAttack {
                Confusion [2, .15]
            }
        }
    }
    
    348 { // Pop Eyes
        desc "MUTATION_EYES_348_DESC" 
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1 
        }
    } 

    349 { // 8 Eyes
        desc "MUTATION_EYES_349_DESC"
        passives {
            StatusEveryXSpellCasts {
                stacks 8
                RandomMagicMissile 4
            }
        }
    }
    351 { // Chaos Eyes
        desc "MUTATION_EYES_351_DESC"
        passives {
            ConjureBonusAbility random
        }
    }
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
   
    353 { // Chameleon Eyes
        tag animal
        desc "MUTATION_EYES_353_DESC"
        passives {
            BackstabImmunity 1 
        }
    }
   
   
     //mirror eyes
    442 {
        desc "MUTATION_EYES_442_DESC"
        passives {
            ReflectProjectiles 10%
        }
    }
	
    750 {//glasses
		int 1
    }
	
    754 {//alien eyes
        desc "MUTATION_EYES_754_DESC"
        passives {
			AddBonusRange 1
            AddElementsToBasicAttack Gravity
        } 
    }
	
    755 {//mothman eyes
        desc "MUTATION_EYES_755_DESC"
		passives {
			AddStatusToBasicAttack {
				Fear [1 .15]
			}
		}
    }
   
   
   
    900 { //slender
        desc "MUTATION_EYES_900_DESC"
   
        passives {
            AddStatusToBasicAttack {
                Slow [1 .1]
            }
        }
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
   
    //Birth Defects
    700 { //graves disease
        tag birth_defect
        cha -2
    }
   
    701 { //anophthalmia
        tag birth_defect
        lck -2
    }
   
    //Human eyes
    702 {
        cha 1
        int 1
        con -2
    }
    -2 { //no eyes (frame 703, but completely missing parts are special and keyed in on -2)
        desc "MUTATION_EYES_M2_DESC"
        tag birth_defect
   
        passives {
            Blind -1
        }
    }
    704 { //lazy eye
        desc "MUTATION_EYES_704_DESC"
        tag birth_defect
   
        passives {
            MissChance 10
        }
   
    }
    705 { //cataracts
        tag birth_defect
        desc "MUTATION_EYES_705_DESC"
   
        passives {
            StatusEachTurnBegin {
                MissChance 5
            }
        }
   
    }
    706 { //crossed eyes
        desc "MUTATION_EYES_706_DESC"
        tag birth_defect
   
        passives {
            Confusion 2
        }
    }
   
    1029 { //spider eye
        desc "MUTATION_EYES_1029_DESC"
   
        passives {
            CritChanceUp 5
        }
    }
}
```

---

## File: `head.gon`

### `head`
**Description:** +1 Thorns.  
**Source:** `head.gon`  

**Localization Strings:**
- `MUTATION_HEAD_304_DESC`: "+2 Health Regeneration +5% dodge chance."
- `MUTATION_HEAD_307_DESC`: "Units that contact you get knocked back 1 tile."
- `MUTATION_HEAD_308_DESC`: "+1 movement range while wet. Water does not slow movement."
- `MUTATION_HEAD_311_DESC`: "Spawn a coin when you take damage."
- `MUTATION_HEAD_312_DESC`: "Your basic attack pulls units towards you."
- `MUTATION_HEAD_313_DESC`: "Poop when you take damage."
- `MUTATION_HEAD_314_DESC`: "Gain +1 [img:int] at the end of each turn."
- `MUTATION_HEAD_315_DESC`: "At the start of each battle, swap your highest and lowest stats."
- `MUTATION_HEAD_316_DESC`: "When you take damage from an attack, gain a random buff."
- `MUTATION_HEAD_317_DESC`: "+5% dodge chance."
- `MUTATION_HEAD_318_DESC`: "+1 range."
- `MUTATION_HEAD_319_DESC`: "Gain +1 [img:int] permanently at the end of each battle. Start each battle with Bruise 2."
- `MUTATION_HEAD_320_DESC`: "Your basic attack has +2 Knockback."
- `MUTATION_HEAD_321_DESC`: "You have a 5% chance to inflict Fear on units who contact or attack you."
- `MUTATION_HEAD_750_DESC`: "+1 Thorns."
- `MUTATION_HEAD_753_DESC`: "You are immune to ice."
- `MUTATION_HEAD_759_DESC`: "Take an extra turn at the start of the battle."
- `MUTATION_HEAD_703_DESC`: "Attacks against your face count as backstabs."
- `MUTATION_HEAD_704_DESC`: "20% miss chance. <br/> Your spells cost 1 less mana."
- `MUTATION_HEAD_706_DESC`: "Brace 1."
- `MUTATION_HEAD_900_DESC`: "+1 range. +1 reach."

```
head {
    300 { //Square head
        con 1
    }
    301 { //Sloth head
        int -1
        str 1
        con 1
    }
    302 { //Big brain
        int 2
        con -1
    }
    303 { //Spioke head
        desc "MUTATION_HEAD_303_DESC"
        passives {
            Thorns 1
        }
    }
    304 { //Sludge head
        tag melted
        desc "MUTATION_HEAD_304_DESC"

        cha -2
        passives {
            HealthRegenUp 2
            DodgeChance 5%
        }
    }
    305 { //Strong Chin
        cha 1
    }
    306 { //Alien head
        int 1
    }
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
    309 { //half moon
        lck 2
    }
    310 { //rock head
        shield 2
    }

    311 { //Money Bag head
        desc "MUTATION_HEAD_311_DESC"
    
        passives {
            SpawnThingOnDamage {
                object Coin 
                chance 100%
            }
        }
    }

    312 { //Magnet Head
        desc "MUTATION_HEAD_312_DESC"

        passives {
            MakeBasicAttackPull 1
        } 
    } 
    
    313 { //Poop Head
        desc "MUTATION_HEAD_313_DESC"

        passives {
            PoopWhenHit Poop
        }
    }
    
    314 { //Pyramid Head
        desc "MUTATION_HEAD_314_DESC"
    
        passives {
            StatusEachTurnEnd {
               IntelligenceUp 1
            } 
        }
    }

    315 { //Upside Down Head
        desc "MUTATION_HEAD_315_DESC"
   
        passives {
            SwapHighestAndLowestStat 1
        }
    }
    
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
    
    317 { //Sideways Head
        desc "MUTATION_HEAD_317_DESC"

        passives {
            DodgeChance 5% 
        }
    }

    318 { //Long Neck
        desc "MUTATION_HEAD_318_DESC"

        passives {
            AddBonusRange 1
        }
    }
    
    319 { //Exposed Brain
        desc "MUTATION_HEAD_319_DESC"

        passives {
            Bruise 2
            StatusOnBattleEnd {
                PermanentIntelligence 1
            }
        }
    } 
      
    320 { //Bubble Head
        desc "MUTATION_HEAD_320_DESC"

        passives {
            AddStatusToBasicAttack {
                Knockback 2
            }
        }
    } 

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
	
    750 { //spiked head
		desc "MUTATION_HEAD_750_DESC"
        passives { 
			Thorns 1
        }
    } 
	
    753 { //tyler head
        desc "MUTATION_HEAD_753_DESC"

		passives {
			ElementImmune Ice
			StatusImmunity [Freeze, Slow]
		}
    } 	
	
    757 { //grey head
		int 2
    } 
	
    759 { //Human Head
        desc "MUTATION_HEAD_759_DESC"
        spd -2

        passives {
            AlphaTurns 1
        }
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


    //Birth Defects
    700 { //microcephaly
        tag birth_defect
        int -2
    }
    701 { //macrocephaly
        tag birth_defect
        int -2
    }
	702 { //concave head
        tag birth_defect
        int -1
    }
	703 { //soft spot
        desc "MUTATION_HEAD_703_DESC"
        tag birth_defect

        passives {
            BackstabFront 1
        }
    }
	704 { //cyclops
        desc "MUTATION_HEAD_704_DESC"
        tag birth_defect

        passives {
            MissChance 20
            ManaCostReduction 1
        }
    }
	705 { //conjoined head
        tag birth_defect
        cha -3
		int 2
    }
	706 { //sloth
        desc "MUTATION_HEAD_706_DESC"
        tag birth_defect
        cha -3

        passives {
            Brace 1
        }
    }

    900 { //slender
        desc "MUTATION_HEAD_900_DESC"

        cha -1
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1
        }
    }
}
```

---

## File: `legs.gon`

### `legs`
**Description:** +1 movement range while wet. Water does not slow movement.  
**Source:** `legs.gon`  

**Localization Strings:**
- `MUTATION_LEGS_301_DESC`: "Your basic attack has a 5% chance to Stun."
- `MUTATION_LEGS_302_DESC`: "Knockback immunity."
- `MUTATION_LEGS_303_DESC`: "Your basic attack has a 5% chance to Immobilize."
- `MUTATION_LEGS_305_DESC`: "+5% dodge chance."
- `MUTATION_LEGS_309_DESC`: "Your basic attack has a 10% chance to inflict Bleed 3."
- `MUTATION_LEGS_310_DESC`: "Your movement action is a jump."
- `MUTATION_LEGS_312_DESC`: "Your basic attack has +1 Knockback."
- `MUTATION_LEGS_313_DESC`: "+1 reach."
- `MUTATION_LEGS_314_DESC`: "Your weapons have +1 Damage."
- `MUTATION_LEGS_315_DESC`: "Ice immunity."
- `MUTATION_LEGS_317_DESC`: "Your basic attack inflicts Bleed 1 if it's melee."
- `MUTATION_LEGS_319_DESC`: "10% chance to gain a bonus move each turn."
- `MUTATION_LEGS_320_DESC`: "10% chance to gain a bonus attack each turn."
- `MUTATION_LEGS_321_DESC`: "Moving through water tiles costs 0 movement."
- `MUTATION_LEGS_325_DESC`: "Collarless spells cost -1 mana."
- `MUTATION_LEGS_326_DESC`: "Your basic attack inflicts a random debuff."
- `MUTATION_LEGS_327_DESC`: "Gain 2 random stat ups and 1 random stat down at the end of each turn."
- `MUTATION_LEGS_328_DESC`: "Equip a temporary Bottles weapon at the start of the battle."
- `MUTATION_LEGS_329_DESC`: "Equip a temporary Water Bottle trinket at the start of the battle."
- `MUTATION_LEGS_330_DESC`: "+1 Health Regeneration"
- `MUTATION_LEGS_331_DESC`: "+1 movement range. Your movement action is a jump."
- `MUTATION_LEGS_332_DESC`: "50% chance to spawn a pickup on an adjacent tile when you end your turn."
- `MUTATION_LEGS_333_DESC`: "Your basic attack has wind element and +1 Knockback."
- `MUTATION_LEGS_334_DESC`: "Your basic attack tosses units into the air if it's melee."
- `MUTATION_LEGS_335_DESC`: "+1 Bleed Thorns. Spawn glass when you take damage."
- `MUTATION_LEGS_336_DESC`: "Your basic attack inflicts Soul Link."
- `MUTATION_LEGS_337_DESC`: "You are immune to tile effects."
- `MUTATION_LEGS_339_DESC`: "Fly away when hit."
- `MUTATION_LEGS_340_DESC`: "When you take damage, gain +1 [img:lck]."
- `MUTATION_LEGS_341_DESC`: "Your basic attack makes units face away from you."
- `MUTATION_LEGS_343_DESC`: "Spawn a Charmed Kitten familiar when you get downed."
- `MUTATION_LEGS_754_DESC`: "Your movement action is a jump. Your basic attack inflicts Bruise."
- `MUTATION_LEGS_757_DESC`: "Trample."
- `MUTATION_LEGS_758_DESC`: "You have All Stats Up while wet."
- `MUTATION_LEGS_759_DESC`: "You have All Stats Up while wet."
- `MUTATION_LEGS_761_DESC`: "Your movement action is a jump. Your basic attack inflicts Bleed."
- `MUTATION_LEGS_762_DESC`: "Ignore the effects of tiles and traps."
- `MUTATION_LEGS_763_DESC`: "Ignore the effects of tiles and traps."
- `MUTATION_LEGS_900_DESC`: "Ignore the effects of tiles and traps."
- `MUTATION_LEGS_703_DESC`: "Water does not slow movement."
- `MUTATION_LEGS_705_DESC`: "Trample."
- `MUTATION_LEGS_707_DESC`: "Permanently Slow."

```
legs {
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

    302 { //Tentacles
        tag animal
        desc "MUTATION_LEGS_302_DESC"

        passives {
            KnockbackImmunity 1
        }
    }

    303 { //Lobster Claws
        tag animal
        desc "MUTATION_LEGS_303_DESC"

        passives {
            AddStatusToBasicAttack {
                Immobile [1, .05]
            }
        }
    }

    304 { //Muscular Legs
        str 1
    }

    305 { //Tar Legs
        desc "MUTATION_LEGS_305_DESC"

        passives {
            DodgeChance 5%
        }
    }

    306 { //Bug Legs
        tag animal
        dex 1
    }

    307 { //Tires
        spd 1
    }

    308 { //Human Legs
        lck 1
    }

    309 { //Knife Legs
        desc "MUTATION_LEGS_309_DESC"

        passives {
            AddStatusToBasicAttack {
                Bleed [3, .1]
            }
        }
    } 

    310 { //Spring Legs
        desc "MUTATION_LEGS_310_DESC" 
        override_move BasicJump
    }
    
    311 { //Square Legs
        con 1
    }

    312 { //Balloon Legs
        desc "MUTATION_LEGS_312_DESC" 

        passives {
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }

    313 { //Snake Legs
        desc "MUTATION_LEGS_313_DESC"
        passives { 
            AddBonusMeleeRange 1 
        }
    }

    314 { //Weapon Legs
        desc "MUTATION_LEGS_314_DESC"
        passives {
            BoostWeaponDamage 1
        }
    }

    315 { //Socks
        desc "MUTATION_LEGS_315_DESC"
        passives {
            ElementImmune Ice
        }
    }
     

    // For Tyler - didn't see an easy way to do this effect. 
//    316 { //Hook legs 
//        passives {
//            MakeBasicAttackPull 1 
//        }  
//    }

    317 { //Raptor Claws
        desc "MUTATION_LEGS_317_DESC"
        passives {
            AddStatusToBasicMeleeAttack {
                Bleed 1
            }
        }
    }


    318 { //Stigmata
        divine_shield 1
    }


    319 { //High Tops
        desc "MUTATION_LEGS_319_DESC"

        passives {
            StatusEachTurnBegin {
                MoveQuivered [1, 0.1]
            }
        }
    }


    320 { //Talons
        desc "MUTATION_LEGS_320_DESC"

        passives { 
            StatusEachTurnBegin {
                Quivered [1, 0.1]
            }  
        }
    }

    321 { //Flippers
        desc "MUTATION_LEGS_321_DESC"

        passives {
            FreePathfindElement Water
        }
    }


    322 { //Bear Claws 
		str 1
		con 1
    }


    323 { //Beetle Feet
        spd 2
    }


    324 { //Branches 
        con 1
    }


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


    327 { //Mushroom Legs 
        desc "MUTATION_LEGS_327_DESC"
        passives {
           StatusEachTurnEnd {
               RandomStatUp 2
               RandomStatDown 1
           }
        }
    }

    328 { //Glass Bottle 
        desc "MUTATION_LEGS_328_DESC"
        passives {
            EquipTemporaryItem Bottles
        }
    }

    329 { //Water Bottle 
        desc "MUTATION_LEGS_329_DESC"
        passives {
            EquipTemporaryItem WaterBottle_Full
        }
    }


    330 { //Sausage Legs 
        desc "MUTATION_LEGS_330_DESC"
        
        passives {
            HealthRegenUp 1
        }
    }


    331 { //Jet Legs 
        desc "MUTATION_LEGS_331_DESC"
        override_move BasicJump
        passives {
           AddMovement 1
        }
    }


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
     
    335 { //Glass Legs 
        desc "MUTATION_LEGS_335_DESC"
        
        passives {
            BleedThorns 1 
            StatusOnTookDamage {
                ChangeTilesUnder GlassTile 
            }
        } 
    }


    336 { //Crow Legs 
        desc "MUTATION_LEGS_336_DESC"
        tag bird

        passives {
            AddStatusToBasicAttack {
                SoulLink 1
            } 
        }
    }


    337 { //Floating Legs 
        desc "MUTATION_LEGS_337_DESC"
        passives {
            IgnoreTiles 1
        }
    }

    //338 missing

    339 { //Wing Legs 2 
        desc "MUTATION_LEGS_339_DESC"
        tag bird
        
        spd 2
        passives { 
            MoveAwayFromDamageSource BasicJump
        }
    }


    340 { //Lucky Toe 
        desc "MUTATION_LEGS_340_DESC"
        passives {
           StatusOnTookDamage {
               LuckUp 1
           }
        }
    }


    341 { //Whip Legs 
        desc "MUTATION_LEGS_341_DESC"
        passives {
            AddStatusToBasicAttack { 
                FaceAway 1
            }
        }
    }

    //342 missing

    343 { //Kitten Legs 
        desc "MUTATION_LEGS_343_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }
	
    754 { //Wing Hoof Legs 
        desc "MUTATION_LEGS_754_DESC"  
        passives {
            ReplaceBasicMove ToadJump_BasicMove
		    AddStatusToBasicAttack {
                Bruise 1
            }	
        }
    }

    756 { //Sonichu Legs 
		spd 2
    }
	
    757 { //bigfoot Legs 
        desc "MUTATION_LEGS_757_DESC"  
        passives {
			Trample 3
        }
    }
	
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

    761 { //mothman Legs 
        desc "MUTATION_LEGS_761_DESC"  
        passives {
            ReplaceBasicMove ToadJump_BasicMove
		    AddStatusToBasicAttack {
                Bleed 1
            }	
        }
    }

    762 { //slender
        desc "MUTATION_LEGS_762_DESC"

        passives {
            IgnoreTiles 1
            YOffset .25
        }
    }
	
    763 { //slender
        desc "MUTATION_LEGS_763_DESC"

        passives {
            IgnoreTiles 1
            YOffset .25
        }
    }
	



    900 { //slender
        desc "MUTATION_LEGS_900_DESC"

        passives {
            IgnoreTiles 1
            YOffset .25
        }
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

    //Birth Defects
    700 { //lobster claw
        tag birth_defect
        str -2
    }
    701 { //extra finger
        tag birth_defect
        dex -2
    }
    702 { //club foot
        tag birth_defect
        spd -2
    }
    703 { //syndactyly
        desc "MUTATION_LEGS_703_DESC"

        tag birth_defect
        spd -2

        passives {
            WaterWalk 1
        }
    }
	704 { //curled paw
        tag birth_defect
        str -1
    }
	705 { //club foot2
        desc "MUTATION_LEGS_705_DESC"
        tag birth_defect
        speed -4 
        passives {
            Trample 3
        }
    }
	706 { //backwards knees
        tag birth_defect
        spd -1
    }
	707 { //blob legs
        desc "MUTATION_LEGS_707_DESC"
        tag birth_defect
        str 1

        passives {
            Slow -1
        }
    }
}
```

---

## File: `mouth.gon`

### `mouth`
**Description:** Gain 1 health when you deal damage.  
**Source:** `mouth.gon`  

**Localization Strings:**
- `MUTATION_MOUTH_302_DESC`: "+1 Health Regeneration"
- `MUTATION_MOUTH_304_DESC`: "Your basic attack inflicts Poison."
- `MUTATION_MOUTH_305_DESC`: "+100 corpse health."
- `MUTATION_MOUTH_306_DESC`: "10% chance to spawn a Fly when you take damage."
- `MUTATION_MOUTH_307_DESC`: "Your basic attack has a 1% chance to instakill."
- `MUTATION_MOUTH_308_DESC`: "+1 Health Regeneration"
- `MUTATION_MOUTH_309_DESC`: "Your basic attack has a 10% chance to inflict Fear."
- `MUTATION_MOUTH_311_DESC`: "Your basic attack inflicts Leech 1."
- `MUTATION_MOUTH_312_DESC`: "Your basic attack has a 10% chance to inflict Immobile if it's melee."
- `MUTATION_MOUTH_313_DESC`: "At the end of each round, spit at an enemy ."
- `MUTATION_MOUTH_314_DESC`: "Spawn 5-10 coins when downed."
- `MUTATION_MOUTH_315_DESC`: "10% chance to gain a bonus attack each turn."
- `MUTATION_MOUTH_316_DESC`: "Your basic attack inflicts Bruise."
- `MUTATION_MOUTH_317_DESC`: "Spawn glass when you take damage. +1 Bleed Thorns."
- `MUTATION_MOUTH_318_DESC`: "Your movement action is Dig."
- `MUTATION_MOUTH_319_DESC`: "Water does not slow movement. +1 Health Regeneration while wet."
- `MUTATION_MOUTH_322_DESC`: "Your basic attack inflicts Bleed."
- `MUTATION_MOUTH_323_DESC`: "+2 Health Regeneration while wet."
- `MUTATION_MOUTH_324_DESC`: "+1 range."
- `MUTATION_MOUTH_326_DESC`: "Gain +1 Health Regeneration whenever you eat food."
- `MUTATION_MOUTH_327_DESC`: "You can reroll your options when you level up."
- `MUTATION_MOUTH_328_DESC`: "Can't eat food, use consumables, or use musical abilities. +2 Health Regeneration"
- `MUTATION_MOUTH_750_DESC`: "Your basic attack destroys inanimate objects and turns tiles into dirt."
- `MUTATION_MOUTH_752_DESC`: "Your basic attack creates water tiles."
- `MUTATION_MOUTH_754_DESC`: "Adjacent units get All Stats Down."
- `MUTATION_MOUTH_755_DESC`: "Ice Immunity."
- `MUTATION_MOUTH_757_DESC`: "Your basic attack inflicts Bleed."
- `MUTATION_MOUTH_760_DESC`: "When a food pickup spawns within 2 tiles of you, move to it."
- `MUTATION_MOUTH_900_DESC`: "Your basic attack has a 10% chance to inflict Fear."
- `MUTATION_MOUTH_1500_DESC`: "Your basic attack inflicts Poison."
- `MUTATION_MOUTH_1026_DESC`: "Your basic attack has a 10% chance to inflict Webbed."
- `MUTATION_MOUTH_M2_DESC`: "Can't eat food, use consumables, or use musical abilities."
- `MUTATION_MOUTH_705_DESC`: "Your basic attack can be used two extra times each turn but is replaced with a 1-damage spit attack."

```
mouth {
    300 { //Sabertoothed  
        tag animal
        str 1
    }
    301 { //Hippo Teeth
        tag animal
        desc "MUTATION_MOUTH_301_DESC"

        passives {
            FlatHealWhenDealDamage 1
        }
    }
    302 { //Flesh Kid  
        desc "MUTATION_MOUTH_302_DESC"        

        passives {
            HealthRegenUp 1
        }
    }
    303 { //Delerious  
        tag melted
        int 1
    }
    304 { //Spider
        tag animal  
        desc "MUTATION_MOUTH_304_DESC"

        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }
    305 { //Ash  
        desc "MUTATION_MOUTH_305_DESC"
        passives {
            AddCorpseHealth 100
        }
    }
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
    307 { //Alien Chomp  
        desc "MUTATION_MOUTH_307_DESC"

        passives {
            AddStatusToBasicAttack {
                Instakill [25, .01]
            }
        }
    }
    308 { //Licky  
        desc "MUTATION_MOUTH_308_DESC"

        passives {
            HealthRegenUp 1
        }
    }
    309 { //Jacko  
        desc "MUTATION_MOUTH_309_DESC"

        passives {
            AddStatusToBasicAttack {
                Fear [1 .1]
            }
        }
    }
    310 { //Lip Fillers 
        cha 1
    }

    311 { //Leech Mouth
        desc "MUTATION_MOUTH_311_DESC"

        passives {
            AddStatusToBasicAttack {
                Leeches 1
            }
        }
    }

    312 { //Bear Trap Mouth
        desc "MUTATION_MOUTH_312_DESC"
        str 1
        passives {
            AddStatusToBasicMeleeAttack {
                Immobile [1, .1]
            }
        }
    }

    313 { //Full Mouth
         desc "MUTATION_MOUTH_313_DESC"

         passives {
             StatusEachRoundEnd {
                UseAbility Spit
             }
         }
    }


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


    315 { //Double Mouth
        desc "MUTATION_MOUTH_315_DESC"

        passives { 
            StatusEachTurnBegin {
                Quivered [1, 0.1]
            }  
        }
    }


    316 { //Horse Face
         desc "MUTATION_MOUTH_316_DESC"
         cha -1
         passives{
            AddStatusToBasicAttack {
                Bruise 1
            }
         }
    } 

    317 { //Glass Teeth
        desc "MUTATION_MOUTH_317_DESC"
        passives {   
            BleedThorns 1 
            StatusOnTookDamage {
                ChangeTilesUnder GlassTile 
            }
        } 
    }


    318 { //mole mouth
        desc "MUTATION_MOUTH_318_DESC"
        passives {
            ReplaceBasicMove_Mutation BasicDig
        }
    }


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

    // for Tyler - BirdChance() right? Seems like you'll need to do something to modify this from a mutation. Also, by how much?
//   320 { //Bird Beak
//        desc "Double the odds of birds appearing."
//   }


    321 { //Zipper Mouth 
         shield 3
    }


    322 { //Shark Mouth
        desc "MUTATION_MOUTH_322_DESC"
        passives{
            AddStatusToBasicAttack {
                Bleed 1
            }
        }
    }


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


    324 { //Eyeball
        desc "MUTATION_MOUTH_324_DESC"      
        passives {
            AddBonusRange 1
        }
    }

    // For Tyler - Add a new  ReplaceBasicAttack_Mutation I guess 
//    325 { //Wide Mouth
//         desc "Your melee attack hits 3 tiles in front of you"
//    }


    326 { //Double Mouth 2
        desc "MUTATION_MOUTH_326_DESC"
        passives { 
            StatusOnEatFood {
                HealthRegenUp 1 
            }
        }
    } 

    327 { //Clown Lips
        desc "MUTATION_MOUTH_327_DESC"
        passives { 
            AddLevelUpRerolls 1
        }
    }

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
	
    750 { //beaver teeth
        desc "MUTATION_MOUTH_750_DESC"
        passives { 
			AddStatusToBasicAttack {
                ChangeTile DirtTile
				VaporizeInanimate 1
            }	
        }
    }
	
    751 { //pig snout
		con 2
    }
	
    752 { //Dog tongue
        desc "MUTATION_MOUTH_752_DESC"
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        } 
    }
	
    754 { //Isaacs mouth
        desc "MUTATION_MOUTH_754_DESC"
		passives {
			DepressionAura 1
		}
    }
	
    755 { //Edmund beard
        desc "MUTATION_MOUTH_755_DESC"
		passives {
			ElementImmune Ice
		}
    }
	
    756 { //Tylers beard
		int 1
    }

    757 { //Mermaid mouth
        desc "MUTATION_MOUTH_757_DESC"
		passives {
			AddStatusToBasicAttack {
				Bleed 1
			}
		}
    }
	
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

    900 { //Slender
        desc "MUTATION_MOUTH_900_DESC"

        passives {
            AddStatusToBasicAttack {
                Fear [1 .1]
            }
        }
    }


    1500 { //rat mouth
        tag animal
        desc "MUTATION_MOUTH_1500_DESC"

        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }

    1026 { //spider mouth
        tag animal
        desc "MUTATION_MOUTH_1026_DESC"

        passives {
            AddStatusToBasicAttack {
                Webbed [1 .1]
            }
        }
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


    //Birth Defects
    700 { //cleft pallet
        tag birth_defect
        cha -2
    }
    701 { //anodontia
        tag birth_defect
        str -1
        dex -1
    }
	-2 { //no mouth (frame 702)
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
	703 { //underbite
        tag birth_defect
        int -2
		con 1
    }
	704 { //overbite
        tag birth_defect
        cha -2
		str 1
    }

    705 { // Fetus Mouth
        desc "MUTATION_MOUTH_705_DESC"

        attack FetusSpit
        passives {
            ExtraBasicAttacks 2
            ReplaceBasicAttack_Mutation FetusSpit
        }
    }
}
```

---

## File: `tail.gon`

### `tail`
**Description:** Poop when you take damage.  
**Source:** `tail.gon`  

**Localization Strings:**
- `MUTATION_TAIL_302_DESC`: "Your basic attack inflicts Poison."
- `MUTATION_TAIL_303_DESC`: "Your basic attack has a 5% chance to Stun."
- `MUTATION_TAIL_305_DESC`: "+1 Thorns."
- `MUTATION_TAIL_308_DESC`: "+5% dodge chance."
- `MUTATION_TAIL_310_DESC`: "Your basic attack has a 10% chance to repeat once."
- `MUTATION_TAIL_311_DESC`: "Thorns 1."
- `MUTATION_TAIL_313_DESC`: "Your basic attack creates water tiles."
- `MUTATION_TAIL_314_DESC`: "Whenever you down a unit, you have a 10% chance to reanimate that unit with 50% HP."
- `MUTATION_TAIL_315_DESC`: "20% chance to spawn a Maggot when hit."
- `MUTATION_TAIL_316_DESC`: "25% chance to spawn tall grass wherever you end your movement."
- `MUTATION_TAIL_317_DESC`: "When hit, fart a Poison 4 attack with Knockback behind you."
- `MUTATION_TAIL_318_DESC`: "Your basic attack inflicts Poison."
- `MUTATION_TAIL_319_DESC`: "Units who contact you get Poisoned."
- `MUTATION_TAIL_320_DESC`: "Bleed 1. Bleed Thorns 2."
- `MUTATION_TAIL_322_DESC`: "Gain +1 [img:spd] each turn."
- `MUTATION_TAIL_323_DESC`: "Your movement action is a jump."
- `MUTATION_TAIL_325_DESC`: "Units that contact you get knocked back 2 tiles."
- `MUTATION_TAIL_326_DESC`: "10% dodge chance. Bruise 1."
- `MUTATION_TAIL_327_DESC`: "If you don't move, gain 3 Charge at the end of the turn."
- `MUTATION_TAIL_329_DESC`: "You can unequip cursed items and parasites."
- `MUTATION_TAIL_331_DESC`: "You can reroll your options when you level up."
- `MUTATION_TAIL_332_DESC`: "+25% chance to reflect projectiles."
- `MUTATION_TAIL_334_DESC`: "Your basic attack inflicts Burn 1."
- `MUTATION_TAIL_336_DESC`: "+1 Thorns."
- `MUTATION_TAIL_337_DESC`: "Your basic attack is wind element."
- `MUTATION_TAIL_338_DESC`: "Your basic attack inflicts Burn 1."
- `MUTATION_TAIL_339_DESC`: "While at full mana, you have +2 Damage."
- `MUTATION_TAIL_341_DESC`: "Gain +1 Charge when you take damage."
- `MUTATION_TAIL_342_DESC`: "Spawn a Charmed Kitten familiar when you get downed."
- `MUTATION_TAIL_751_DESC`: "+1 Brace."
- `MUTATION_TAIL_754_DESC`: "+1 Thorns."
- `MUTATION_TAIL_755_DESC`: "Water does not slow movement."
- `MUTATION_TAIL_756_DESC`: "+1 Bleed Thorns."
- `MUTATION_TAIL_757_DESC`: "Your movement action is shadowstep."
- `MUTATION_TAIL_759_DESC`: "Start with +1 Bonus Attack."
- `MUTATION_TAIL_760_DESC`: "Start with 2 backflips."
- `MUTATION_TAIL_703_DESC`: "Start each battle with Immobile 1."
- `MUTATION_TAIL_704_DESC`: "Hunter abilities are also offered when you level up."

```
tail {

    300 { //Extra Paw
        tag extra    
        str 1
    }

    301 { //Turtle Head
        tag animal
        desc "MUTATION_TAIL_301_DESC"

        passives {
            PoopWhenHit Poop
        }
    }

    302 { //Scorpion Tail
        tag animal
        desc "MUTATION_TAIL_302_DESC"

        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }

    303 { //Rock Tail
        desc "MUTATION_TAIL_303_DESC"

        passives {
            AddStatusToBasicAttack {
                Stun [1, .05]
            }
        }
    }

    304 { //Monkey Tail
        tag animal
        dex 1
    }

    305 { //Cacuts Tail
        desc "MUTATION_TAIL_305_DESC"

        passives {
            Thorns 1
        }
    }

    306 { //Big Lump Tail
        con 1
    }

    307 { //Antenna Tail
        spd 1
    }

    308 { //Baby Tail
        desc "MUTATION_TAIL_308_DESC"

        lck 1
        passives {
            DodgeChance 5%
        }
    }
    
    309 { //Baboon's' Ass
        tag animal
        cha 1
    }
    
    310 { //Hand Tail
        desc "MUTATION_TAIL_310_DESC"

        passives {
            AddTemporaryEffectsToBasicAttack {
                Fury 10
            }
        }
    }
    
    311 { //Thorn Tail 
        desc "MUTATION_TAIL_311_DESC" 
        passives {        
            Thorns 1 
        } 
    }
    
    312 { //Holy Tail 
        divine_shield 1
    } 

    313 { //Hose Tail
        desc "MUTATION_TAIL_313_DESC" 
        passives {
            AddStatusToBasicAttack {
                ChangeTile WaterTile
            }
            AddElementsToBasicAttack Water 
        } 
    } 

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

    317 { //Skunk Tail
        desc "MUTATION_TAIL_317_DESC" 
        passives {
            AbilityReaction SkunkTail
        }
    }

    318 { //Rattle
        desc "MUTATION_TAIL_318_DESC" 
        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        } 
    }

    319 { //Snake Tail
        desc "MUTATION_TAIL_319_DESC" 
        passives {
            PoisonThorns 1
        } 
    }

    320 { //Glass Tail
        desc "MUTATION_TAIL_320_DESC" 
        passives {
            Bleed 1 
            BleedThorns 2                
        } 
    }

    321 { //Extra Head
        tag extra
        int 1
    }
    
    322 { //Exhaust Pipe
        desc "MUTATION_TAIL_322_DESC" 
        passives {     
            StatusEachTurnBegin {
                SpeedUp 1
            }
        } 
    }

    323 { //Jetpack Tail
        desc "MUTATION_TAIL_323_DESC" 
        passives {
            ReplaceBasicMove_Mutation BasicJump
        } 
    }

    324 { //Wing Tail
        spd 2 
    }
    
    325 { //Spring Tail
        desc "MUTATION_TAIL_325_DESC" 
        passives {
            MeleeRevengeDamage {
                knockback 2
            }
        } 
    }

    326 { //Eyeball Tail
        desc "MUTATION_TAIL_326_DESC" 
        passives {
            Bruise 1
            DodgeChance 10%

        }
    }

    327 { //Tree Branch Tail
        desc "MUTATION_TAIL_327_DESC" 
        passives {
            StatusIfDidntMove {
                Charge 3
            }
        } 
    }

    //328 missing?

    329 { //Mr. Worm
        desc "MUTATION_TAIL_329_DESC" 
        passives {   
            CanRemoveCursedItems 1
        } 
    }

    //330 missing

    331 { //Dice Tail
        desc "MUTATION_TAIL_331_DESC"
        passives { 
            AddLevelUpRerolls 1
        } 
    }

    332 { //Tennis Racket
        desc "MUTATION_TAIL_332_DESC"
        passives { 
            ReflectProjectiles 25%
        }
    }

    //333 missing

    334 { //Fire Flower Tail
        desc "MUTATION_TAIL_334_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 1 
            }
            AddElementsToBasicAttack Fire
        } 
    }

    //335 missing

    336 { //Horn Tail
        desc "MUTATION_TAIL_336_DESC"
        passives {
            Thorns 1
        }
    }

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

    338 { //Flame Tail
        desc "MUTATION_TAIL_338_DESC"

        passives {
            AddStatusToBasicAttack {
                Burn 1 
            }
            AddElementsToBasicAttack Fire
        } 
    }

    339 { //Light Bulb
        desc "MUTATION_TAIL_339_DESC"

        passives {
            PassiveWhenAtFullMana {
                DamageUp 2
            }
        }
    }

    //340 missing

    341 { //Tongue Tail
        desc "MUTATION_TAIL_341_DESC" 
        passives {
            StatusOnTookDamage {
                Charge 1
            }
        } 
    }
    342 { //Kitten Tail
        desc "MUTATION_TAIL_342_DESC"  
        passives {
            SpawnOnDowned CharmedKitten
        }
    }

	750 { //Bunny Tail*
		cha 1
    }

	751 { //Beaver Tail*
        desc "MUTATION_TAIL_751_DESC"  
        passives {
			Brace 1
        }
    }
	
	752 { //Pig Tail*
		con 1
    }
	
	/*753 { //Skunk Tail 2*
        passives {

        }
    }*/
	
	754 { //Spiked Tail*
        desc "MUTATION_TAIL_754_DESC"  
        passives {
			Thorns 1
        }
    }
	
	755 { //mermaid Tail*
        desc "MUTATION_TAIL_755_DESC"  
        passives {
            WaterWalk 1
        }
    }
	
	756 { //Devil Tail*
        desc "MUTATION_TAIL_756_DESC"  
        passives {
			BleedThorns 1
        }
    }
	
	757 { //sonichu Tail*
        desc "MUTATION_TAIL_757_DESC"  
        passives {
            ReplaceBasicMove Shadowstep
        }
    }
	
	759 { //slender Tail*
        desc "MUTATION_TAIL_759_DESC"  
		passives {
			Quivered 1
		}
    }
      
	760 { //human head tail
        desc "MUTATION_TAIL_760_DESC"  
        passives {
            BackflipWhenTargeted {
                stacks 2
                ability BackflipDodge
            }
        }
    }
      

    900 { //slender
        spd 1
    }

    1500 { //rat tail
        tag animal
        dex 1
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


    //Birth Defects
    700 { //kinked tail
        tag birth_defect
        lck -2
    }
    701 { //lipoma
        tag birth_defect
        spd -1
        cha -1
    }
	-2 { //no tail (702)
        tag birth_defect
        dex -1
    }
	703 { //heavy tail
        desc "MUTATION_TAIL_703_DESC"
        tag birth_defect
        con 1

        passives {
            Immobile 1
        }
    }
	704 { //forked tail
        desc "MUTATION_TAIL_704_DESC"
        tag birth_defect
        lck -2

        passives {
            MulticlassLevelUp Hunter
        }
    }
}
```

---

## File: `texture.gon`

### `texture`
**Description:** +1 Health Regeneration  
**Source:** `texture.gon`  

**Localization Strings:**
- `MUTATION_TEXTURE_301_DESC`: "+1 Health and Mana Regeneration while wet."
- `MUTATION_TEXTURE_303_DESC`: "Start each battle with a random stat up."
- `MUTATION_TEXTURE_304_DESC`: "Units that contact or attack you have a 10% chance to become Confused."
- `MUTATION_TEXTURE_307_DESC`: "+5% dodge chance."
- `MUTATION_TEXTURE_309_DESC`: "Your basic attack has a 5% chance to inflict Fear. You have a 5% chance to inflict Fear on units who contact or attack you."
- `MUTATION_TEXTURE_310_DESC`: "Gain double the effects of pickups you collect."
- `MUTATION_TEXTURE_750_DESC`: "Units who contact you get Poison 2."
- `MUTATION_TEXTURE_702_DESC`: "Start each battle with Bleed 1."
- `MUTATION_TEXTURE_703_DESC`: "Mage abilities are also offered when you level up."
- `MUTATION_TEXTURE_704_DESC`: "Fighter abilities are also offered when you level up."
- `MUTATION_TEXTURE_705_DESC`: "Thief abilities are also offered when you level up."
- `MUTATION_TEXTURE_706_DESC`: "10% dodge chance."

```
texture {
    300 { //Stitches
        desc "MUTATION_TEXTURE_300_DESC"

        cha -1
        passives {
            HealthRegenUp 1
        }
    }

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

    302 { //Conjoined
        lck 1
    }

    303 { //Patches
        desc "MUTATION_TEXTURE_303_DESC"

        passives {
            RandomStatUp 1
        }
    }

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

    305 { //Robot Hide
        int 1
    }

    306 { //Veiny
        str 1
    }

    307 { //Eyeballs
        desc "MUTATION_TEXTURE_307_DESC"

        passives {
            DodgeChance 5%
        }
    }

    308 { //Heart Tattoo
        cha 1
    }

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

    310 { //Cash Hide
        desc "MUTATION_TEXTURE_310_DESC"

        passives {
            AddLootMultiplier 1
        }
    }
	
    750 { //skunk Hide
        desc "MUTATION_TEXTURE_750_DESC"

        passives {
            PoisonThorns 2
        }
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


    //Birth Defects
    700 { //neurofibromatosis
        tag birth_defect
        cha -2
    }
    701 { //melanocytic nevus
        tag birth_defect
        cha -2
        shield 1
    }
	702 { //bleeding
        desc "MUTATION_TEXTURE_702_DESC"
        tag birth_defect

        passives {
            Bleed 1
        }
    }
	703 { //blue spots
        desc "MUTATION_TEXTURE_703_DESC"
        tag birth_defect
        cha -2

        passives {
            MulticlassLevelUp Mage
        }
    }
	704 { //red dots
        desc "MUTATION_TEXTURE_704_DESC"
        tag birth_defect
        cha -2

        passives {
            MulticlassLevelUp Fighter
        }
    }
	705 { //jaundice
        desc "MUTATION_TEXTURE_705_DESC"
        tag birth_defect
        cha -2

        passives {
            MulticlassLevelUp Thief
        }
    }
	706 { //vitiligo
        desc "MUTATION_TEXTURE_706_DESC"
        tag birth_defect
        cha -1

        passives {
            DodgeChance_Status 10
        }
    }
}
```

---

