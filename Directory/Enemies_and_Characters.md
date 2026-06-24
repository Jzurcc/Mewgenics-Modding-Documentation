# Enemies & Characters Directory

### `BirdBase`
**Name:** Bird  
**Source:** `bonus_birds.gon`  

```
BirdBase {
    graphics {
        movieclip BirdSmall
        name "ENEMY_BIRD_NAME"

        tooltip "ENEMY_BIRD_DESC"
    }

    properties {
        tag animal
        hidden_tag [bird bonusbird]
        faction birds
        kill_required false
        movement 3
        health 2
        initiative -999
    }

    abilities {
        move DefaultMove
        attack BasicMelee

        spells [
            BirdFly
        ]
    }

    passives {
        CounterAttack attack
        MoveAwayFromDamageSource {
            move_ability BirdFly
        }
        Bird CookedChickenLeg

        TrackAmountKilledByPlayer BonusBirdsKilled
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights bird
    }
}
```

---

### `BirdSmall`
**Name:** Little Bird  
**Source:** `bonus_birds.gon`  

```
BirdSmall {
    variant_of BirdBase

    graphics {
        movieclip BirdSmall
        name "ENEMY_LITTLEBIRD_NAME"
        shadow_size .5
    }

    properties {
        health 2
        movement 5
    }

    passives {
        BirdRewards {

            statuses {
                AllStatsUp 1
            }
            ally_rewards {
                FindItemFromPool chapter
            }
        }
        RunInXTurns 1
    }
}
```

---

### `BirdMed`
**Name:** Medium Bird  
**Source:** `bonus_birds.gon`  

```
BirdMed {
    variant_of BirdBase

    graphics {
        movieclip BirdMed
        name "ENEMY_MEDBIRD_NAME"
    }

    properties {
        health 7
        movement 4
    }

    passives {
        BirdRewards {

            statuses {
                AllStatsUp 1
            }
            ally_rewards {
                FindItemFromPool chapter
            }
        }
        RunInXTurns 2
    }
}
```

---

### `BirdLarge`
**Name:** Big Bird  
**Source:** `bonus_birds.gon`  

```
BirdLarge {
    variant_of BirdBase

    graphics {
        movieclip BirdLarge
        name "ENEMY_BIGBIRD_NAME"
    }

    properties {
        health 16
        movement 3
    }

    passives {
        BirdRewards {

            statuses {
                AllStatsUp 1
            }
            ally_rewards {
                FindItemFromPool chapter
            }
        }
        RunInXTurns 3
    }
}
```

---

### `BlackBird`
**Name:** Black Bird  
**Source:** `bonus_birds.gon`  

```
BlackBird {
    variant_of BirdSmall

    graphics {
        name "ENEMY_BLACKBIRD_NAME"
        scale .8
    }

    sound {
        alt_sounds [[SE_BirdSmall_DyingCall SE_BirdDying_Blackbird]]
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool blackbird_pool
            }
        }
    }
}
```

---

### `Dove`
**Name:** Dove  
**Source:** `bonus_birds.gon`  

```
Dove {
    variant_of BirdSmall

    graphics {
        name "ENEMY_DOVE_NAME"
        piece_alt_frame 3
        scale .8
    }

    sound {
        alt_sounds [[SE_BirdSmall_DyingCall SE_BirdDying_Dove]]
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool dove_pool
            }
        }
    }
}
```

---

### `HummingBird`
**Name:** Hummingbird  
**Source:** `bonus_birds.gon`  

```
HummingBird {
    variant_of BirdSmall

    graphics {
        name "ENEMY_HUMMINGBIRD_NAME"
        piece_alt_frame 5
        scale .5
    }

    sound {
        alt_sounds [[SE_BirdSmall_DyingCall SE_BirdDying_Hummingbird]]
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool hummingbird_pool
            }
        }
    }
}
```

---

### `Cherub`
**Name:** Cherub  
**Source:** `bonus_birds.gon`  

```
Cherub {
    variant_of BirdSmall

    graphics {
        name "ENEMY_CHERUB_NAME"
        piece_alt_frame 7
    }

    passives {
        Angel 1

        BirdRewards {
            ally_rewards {
                FindItemFromPool cherub_pool
            }
        }
    }
}
```

---

### `Cherub_FinalBoss`
**Source:** `bonus_birds.gon`  

```
Cherub_FinalBoss {
    variant_of Cherub
    graphics {
        override_portrait Cherub
        tooltip "ENEMY_CHERUB_FINALBOSS_DESC"
    }
    properties {
        hidden_tag angeljunk
    }
    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool none
            }
        }
    }
}
```

---

### `Pigeon`
**Name:** Pigeon  
**Source:** `bonus_birds.gon`  

```
Pigeon {
    variant_of BirdMed

    graphics {
        name "ENEMY_PIGEON_NAME"
        piece_alt_frame 9
        scale .8
    }

    sound {
        alt_sounds [[SE_BirdMed_DyingCall SE_BirdDying_Pigeon]]
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool pigeon_pool
            }
        }
    }
}
```

---

### `Seagull`
**Name:** Seagull  
**Source:** `bonus_birds.gon`  

```
Seagull {
    variant_of BirdMed

    graphics {
        name "ENEMY_SEAGULL_NAME"
        piece_alt_frame 11
        scale .9
    }

    sound {
        alt_sounds [[SE_BirdMed_DyingCall SE_BirdDying_Seagull]]
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool seagull_pool
            }
        }
    }
}
```

---

### `Raven`
**Name:** Raven  
**Source:** `bonus_birds.gon`  

```
Raven {
    variant_of BirdMed

    graphics {
        name "ENEMY_RAVEN_NAME"
        piece_alt_frame 13
    }

    sound {
        alt_sounds [[SE_BirdMed_DyingCall SE_BirdDying_Raven]]
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool raven_pool
            }
        }

        AddStatusToBasicAttack {
            Madness 1
        }
    }
}
```

---

### `Mutant`
**Name:** Mutant  
**Source:** `bonus_birds.gon`  

```
Mutant {
    variant_of BirdMed

    graphics {
        name "ENEMY_MUTANT_NAME"
        piece_alt_frame 15
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool none

                RandomStatusFromPool {
                    StatusGroup {
                        FindItemFromPool mutant_pool
                    }
                    StatusGroup {
                        FindItemFromPool parasites
                        FindItemFromPool parasites
                        FindItemFromPool parasites
                    }
                }
            }
        }

        AddStatusToBasicAttack {
            Bruise 1
            Knockback 3
        }
    }
}
```

---

### `Chicken`
**Name:** Chicken  
**Source:** `bonus_birds.gon`  

```
Chicken {
    variant_of BirdLarge

    graphics {
        name "ENEMY_CHICKEN_NAME"
        piece_alt_frame 17
    }

    sound {
        alt_sounds [[SE_BirdLarge_DyingCall SE_BirdDying_Chicken]]
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool chicken_pool
            }
        }
    }
}
```

---

### `Turkey`
**Name:** Turkey  
**Source:** `bonus_birds.gon`  

```
Turkey {
    variant_of BirdLarge

    graphics {
        name "ENEMY_TURKEY_NAME"
        piece_alt_frame 19
    }

    sound {
        alt_sounds [[SE_BirdLarge_DyingCall SE_BirdDying_Turkey]]
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool turkey_pool
            }
        }
    }
}
```

---

### `Eagle`
**Name:** Eagle  
**Source:** `bonus_birds.gon`  

```
Eagle {
    variant_of BirdLarge

    graphics {
        name "ENEMY_EAGLE_NAME"
        piece_alt_frame 21
    }

    sound {
        alt_sounds [[SE_BirdLarge_DyingCall SE_BirdDying_Eagle]]
    }

    stats {
        strength 8
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool eagle_pool
            }
        }

        AddStatusToBasicAttack {
            Bleed 1
        }
    }
}
```

---

### `Harpy`
**Name:** Harpy  
**Source:** `bonus_birds.gon`  

```
Harpy {
    variant_of BirdLarge

    graphics {
        name "ENEMY_HARPY_NAME"
        piece_alt_frame 23
    }

    passives {
        BirdRewards {
            ally_rewards {
                FindItemFromPool harpy_pool
            }
        }

        AddStatusToBasicAttack {
            Fear 1
        }
    }
}
```

---

### `SmallBirdPool`
**Source:** `bonus_birds.gon`  

```
SmallBirdPool {
    alt_spawn_pool {
        BlackBird 3000
        Dove 1000
        HummingBird 300
        Cherub 1
    }

    properties {
        can_be_champion false
    }
}
```

---

### `MedBirdPool`
**Source:** `bonus_birds.gon`  

```
MedBirdPool {
    alt_spawn_pool {
        Pigeon 3000
        Seagull 1000
        Raven 300
        Mutant 1
    }

    properties {
        can_be_champion false
    }
}
```

---

### `LargeBirdPool`
**Source:** `bonus_birds.gon`  

```
LargeBirdPool {
    alt_spawn_pool {
        Chicken 3000
        Turkey 1000
        Eagle 300
        Harpy 1
    }

    properties {
        can_be_champion false
    }
}
```

---

### `Bird`
**Source:** `bonus_birds.gon`  

```
Bird {
    alt_spawn_pool {
        SmallBirdPool 1
        MedBirdPool 1
        LargeBirdPool 1
    }

    properties {
        can_be_champion false
    }
}
```

---

### `BomberRat`
**Name:** Radical Rat  
**Source:** `bosses.gon`  

```
BomberRat {
    graphics {
        movieclip BomberRat
        name "ENEMY_RADICALRAT_NAME"
        projectile_spawn_offset [.25 1]
		tooltip "ENEMY_RADICALRAT_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag rat
        faction enemies
        type boss

        mana_regen 999
        mana 100
        initiative -100
        movement 5
        health 67
        
        dispersed_bonus_turns 2
        dispersed_bonus_turns_consider_initiative false
        dispersed_bonus_turns_before_cats true
        last_turn_is_main_turn true
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [
            SpawnBomb
            BombRatTurtle
            RockToss_BomberRat
        ]
    }

    passives {
        FormChanger {
            Default { 
            }
            Rain {
                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [*RockToss_BomberRat, RockToss_BomberRat]
                    }

                    decision_weights extra_careless
                    move_weights keep_distance_always_move
                }
            }

            initial_form Default
        }

        FormChangeDuringWeatherElement {
            element Water
            form Rain
        }

        BossRewards {
            common RatBomb
            rare RadGlasses
        }
    }
    
    ai {
        brain PatternBrain
        decision_weights extra_careless
        move_weights chaotic_runaway

        mainturn_pattern {
            do **BombRatTurtle
        }
        
        bonusturn_pattern {
            do *SpawnBomb
        }
        
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `Fatso`
**Name:** Boris  
**Source:** `bosses.gon`  

```
Fatso {
    graphics {
        movieclip Fatso
        name "ENEMY_BORIS_NAME"
        water_mask square
		tooltip "ENEMY_BORIS_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [cat blob]
        faction enemies
        type boss
        movement 2
        dispersed_bonus_turns 3
        mana_regen 999
        mana 100
        
        health 200

        size 2x2
        move_block everything_even_when_dead

        last_turn_is_main_turn true
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [
            TrampleDash
            MoveOne
        ]
    }

    passives {
        Trample 3
        
        MoveTowardsDamageSource MoveOne

        BossRewards {
			common Blubber
			rare BorisBrain
		}
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights stay_close
        auto_orient false
        
        mainturn_pattern {
            do **TrampleDash
        }
        
        bonusturn_pattern {
            do move
        }
    }
}
```

---

### `RatPile`
**Name:** Rat Pile  
**Source:** `bosses.gon`  

```
RatPile {
    graphics {
        movieclip RatPile
        name "ENEMY_RATPILE_NAME"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag rat
        faction enemies
        type boss
        
        mana_regen 999
        mana 100
        
        health 50

        size 3x3
        move_block everything_even_when_dead
        can_be_backstabbed false
        knockback_immune true
        
        corpse_health 0
    }

    abilities {
        move None
        attack None
        
        spells [
            SpawnRat
            HealSelf
        ]
    }

    passives {
        Trample 5
        TransformOnDeath RatKing

        SpawnThingOnDamage {
            object Rat
            auto_cast Dash_Enemy
        }
    }
    
    ai {
        brain PatternBrain
        
        mainturn_pattern {
            do HealSelf
        }
        
        decision_weights spawn_randomly
        move_weights stay_close
        auto_orient false
    }
}
```

---

### `RatKing_Old`
**Name:** Rat King  
**Source:** `bosses.gon`  

```
RatKing_Old {
    graphics {
        movieclip RatKing
        name "ENEMY_RATKING_NAME"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 10
        speed 5
        charisma 5
    }
    
    properties {
        tag rat
        faction enemies
        type boss
        
        mana_regen 999
        mana 100
        
        health 50
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            RangedHeal_Enemy
        ]
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights heal_others
        move_weights keep_distance
    }
}
```

---

### `DustDevil`
**Name:** Dust Devil  
**Source:** `bosses.gon`  

```
DustDevil {
    graphics {
        movieclip DustDevil
        name "ENEMY_DUSTDEVIL_NAME"
        tooltip ENEMY_DUSTDEVIL_DESC
        uifloaters_offset 1.5
        scale .80
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag demon
        faction enemies
        type boss
        initiative -999
        dispersed_bonus_turns 2
        movement 1

        
        mana_regen 999
        mana 100
        
        health 100

        elements [
            Dust
        ]
    }

    abilities {
        move DustMove
        attack DustMelee
        
        spells [
            DustDash
            DustTeleport
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        bonusturn_pattern {
            do DustDash
        }


        mainturn_pattern {
            do_all [attack DustTeleport]
        }


        decision_weights dustdevil
        move_weights dustdevil
    }
}
```

---

### `Wizard`
**Name:** Wizard  
**Source:** `bosses.gon`  

```
Wizard {
    graphics {
        movieclip Wizard
        name "ENEMY_WIZARD_NAME"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        
        faction enemies
        type boss
        initiative 999
        dispersed_bonus_turns 3

        
        mana_regen 999
        mana 100
        
        health 75
    }

    abilities {
        move DefaultMove
        attack BasicShortRanged
        
        spells [
            WizSpellShield
            WizBlizzard
            WizFlamethrower
            WizStorm
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do_strict [*WizSpellShield, WizBlizzard]
        }

        bonusturn_pattern {
            do_strict [WizFlamethrower]
            do_strict [WizStorm]
            do_strict []
        }

        decision_weights always_cast
        move_weights keep_distance
        fallback_advances_pattern true
        stun_advances_pattern true
    }
}
```

---

### `GeminiCats`
**Name:** Gemini Cats  
**Source:** `bosses.gon`  

```
GeminiCats {
    graphics {
        movieclip Gemini
        name "ENEMY_GEMINICATS_NAME"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        mana_regen 999
        mana 100
        
        health 100

        size gemini

        
    }

    abilities {
        move DefaultMove
        attack GeminiBite
        
        spells [
            GeminiSwipe
            GeminiSpecial
        ]
    }

    passives {
        GeminiTwin 1
    }
    
    ai {
        brain PlayerBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Ornstein`
**Name:** Ornstein  
**Source:** `bosses.gon`  

```
Ornstein {
    graphics {
        movieclip Ornstein
        name "ENEMY_ORNSTEIN_NAME"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        
        faction enemies
        type boss
        dispersed_bonus_turns 2

        
        mana_regen 999
        mana 100
        
        health 75
    }

    abilities {
        move DefaultMove
        attack SpearPoke
        
        spells [
            YeetTowardsBuddy
            Magnetize
        ]
    }

    passives {
        Buddy Smough
        TransformWhenBuddyDies UltraOrnstein
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do SpearPoke
        }

        bonusturn_pattern {
            do Magnetize
            do YeetTowardsBuddy
        }

        decision_weights default
        move_weights keep_distance_always_move
        fallback_advances_pattern true
        stun_advances_pattern true
    }
}
```

---

### `Smough`
**Name:** Smough  
**Source:** `bosses.gon`  

```
Smough {
    graphics {
        movieclip Smough
        name "ENEMY_SMOUGH_NAME"
        shadow_size 2
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        
        faction enemies
        type boss
        initiative -999
        movement 1

        size 2x2
        move_block everything_even_when_dead

        
        mana_regen 999
        mana 100
        
        health 50
        shield 50
    }

    abilities {
        move DefaultMove
        attack HammerSmash
        
        spells [
        ]
    }

    passives {
        Buddy Ornstein
        TransformWhenBuddyDies UltraSmough
        Trample 3
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `UltraSmough`
**Name:** Ultra Smough  
**Source:** `bosses.gon`  

```
UltraSmough {
    graphics {
        movieclip UltraSmough
        name "ENEMY_ULTRASMOUGH_NAME"
        shadow_size 2
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        
        faction enemies
        type boss
        movement 1

        size 2x2
        move_block everything_even_when_dead
        dispersed_bonus_turns 2

        
        mana_regen 999
        mana 100
        
        health 75 
    }

    abilities {
        move DefaultMove
        attack HammerSmash
        
        spells [
            SpawnJunk
            FatLeap
        ]
    }

    passives {
        Trample 3
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do HammerSmash
        }

        bonusturn_pattern {
            do *SpawnJunk
            do FatLeap
        }

        decision_weights default
        move_weights stay_close
        fallback_advances_pattern true
        stun_advances_pattern true
    }
}
```

---

### `UltraOrnstein`
**Name:** Ultra Ornstein  
**Source:** `bosses.gon`  

```
UltraOrnstein {
    graphics {
        movieclip UltraOrnstein
        name "ENEMY_ULTRAORNSTEIN_NAME"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 7
        charisma 5
    }
    
    properties {
        
        faction enemies
        type boss
        dispersed_bonus_turns 3

        
        mana_regen 999
        mana 100
        
        health 100 
    }

    abilities {
        move Teleport
        attack SpearPoke
        
        spells [
            XLightning
            Magnetize
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do SpearPoke
        }

        bonusturn_pattern {
            do Magnetize
            do XLightning
            do Magnetize
        }

        decision_weights default
        move_weights keep_distance_always_move
        fallback_advances_pattern true
        stun_advances_pattern true
    }
}
```

---

### `WallOfCats_Wall`
**Name:** Wall of Cats  
**Source:** `bosses.gon`  

```
WallOfCats_Wall {
    graphics {
        movieclip WoC_Wall
        name "ENEMY_WALLOFCATS_NAME"
        art_flip -1
        dont_sink true
        depth_offset 5
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        lock_orientation [-1, 0]
        faction none
        type boss
        size 5x10

        takes_turns false
        inanimate true
        knockback_immune true
        can_be_backstabbed false
        layer all
        kill_required false
        mouseover_priority 10
    }

    abilities {

    }

    passives {
        Wall 1
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `WallOfCats_Eye`
**Name:** Wall of Cats  
**Source:** `bosses.gon`  

```
WallOfCats_Eye {
    graphics {
        movieclip WoC_Eye
        name "ENEMY_WALLOFCATS_NAME"
        art_flip -1
        dont_sink true
        shadow none
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        lock_orientation [-1, 0]
        faction enemies
        ignore_tiles true
        type boss
        health 40

        knockback_immune true
        can_be_backstabbed false
        kill_required true
        disperse_main_turns true
        corpse_health 0
    }

    abilities {
        move WallMove
        attack WallEyeShot
    }

    passives {

    }
    
    ai {
        brain PatternBrain
        pattern {
            move_then_do attack
        }

        decision_weights always_cast
        move_weights random
    }
}
```

---

### `WallOfCats_Mouth`
**Name:** Wall of Cats  
**Source:** `bosses.gon`  

```
WallOfCats_Mouth {
    graphics {
        movieclip WoC_Mouth
        name "ENEMY_WALLOFCATS_NAME"
        art_flip -1
        dont_sink true
        shadow none
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        lock_orientation [-1, 0]
        faction enemies
        flying true
        type boss
        size 2x2
        health 70

        knockback_immune true
        can_be_backstabbed false
        kill_required true
        disperse_main_turns true
        corpse_health 0
    }

    abilities {
        move WallMove
        attack WallBlow
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights always_cast
        move_weights random
    }
}
```

---

### `Simon`
**Name:** Throbbing King  
**Source:** `bosses.gon`  

```
Simon {
    graphics {
        movieclip Simon
        name "ENEMY_THROBBINGKING_NAME"
        shadow_size 2
        uifloaters_offset 2
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        movement 3
        mana_regen 999
        mana 100
        
        health 250

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack BasicBigMelee
        
        spells [
            SimonSays_Scatter
            SimonSays_ComeHere
            SimonSays_GoAway
            

            Simon_Tentacle
            Simon_Trash
            Simon_Shot
        ]
    }

    passives {
        BonusTurnPattern [ 
            {
                dispersed_bonus_turns 2
                round_end_bonus_turns 1
            }

            {
                round_end_bonus_turns 1
                takes_main_turn false
            }
        ]

        Trample 3
        TransformOnDeath SimonFlopper
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights keep_distance_always_move
        stun_advances_pattern true
        auto_orient false
        
        mainturn_pattern {
            do_priority [attack Simon_Shot]
        }

        dispersed_bonusturn_pattern {
            do Simon_Trash
            do Simon_Tentacle
        }
        
        round_end_bonusturn_pattern {
            do_random [SimonSays_Scatter, SimonSays_ComeHere, SimonSays_GoAway]
            do_nothing []
        }
    }
}
```

---

### `SimonFlopper`
**Name:** Throbbing King  
**Source:** `bosses.gon`  

```
SimonFlopper {
    graphics {
        movieclip SimonFlop
        name "ENEMY_THROBBINGKING_NAME"
        shadow_size 2
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        movement 5
        mana_regen 999
        mana 100
        dispersed_bonus_turns 3
        
        health 250

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack BasicBigMelee
        
        spells [
            SimonFlopper_WiggleFake
            SimonFlopper_WiggleChance
            SimonFlopper_WiggleGuaranteed
            SimonFlopper_Tentacle
            SimonFlopper_SpawnMinion
        ]
    }

    passives {
        FormChanger {
            Flop { 
                animation_suffix "Down"

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights keep_distance_always_move
                    auto_orient false
                    reset_pattern_on_formswitch true

                    pattern {
                        do **SimonFlopper_WiggleFake
                        do **SimonFlopper_WiggleFake
                        do **SimonFlopper_WiggleFake
                        do **SimonFlopper_WiggleGuaranteed
                    }
                }
                passives {
                    BackstabAllDirections 1
                }
            }
            Flop2 { 
                animation_suffix "Down"

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights keep_distance_always_move
                    auto_orient false
                    reset_pattern_on_formswitch true

                    pattern {
                        do **SimonFlopper_WiggleFake
                        do **SimonFlopper_WiggleChance
                        do **SimonFlopper_WiggleChance
                        do **SimonFlopper_WiggleChance
                        do **SimonFlopper_WiggleChance
                        do **SimonFlopper_WiggleGuaranteed
                    }
                }
                passives {
                    BackstabAllDirections 1
                }
            }
            Normal {
                animation_suffix "Up"

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights keep_distance_always_move
                    auto_orient false

                    pattern {
                        do SimonFlopper_Tentacle
                        move_then_do SimonFlopper_SpawnMinion
                    }
                    fallback {
                        do attack
                    }
                }
                passives {
                    ChanceToFormChangeOnAbilityDamage {
                        chance 15%
                        form Flop2
                    }
                }
            }

            initial_form Flop
        }

        Trample 3
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_always_move
        auto_orient false
    }
}
```

---

### `Bumblefoot`
**Name:** Bumblefoot  
**Source:** `bosses.gon`  

```
Bumblefoot {
    graphics {
        movieclip Bumblefoot
        name "ENEMY_BUMBLEFOOT_NAME"
        shadow_size 2
        uifloaters_offset 2
        no_horizontal_flip true
        projectile_spawn_offset [0 1.5]
        water_mask medium
		tooltip "ENEMY_BUMBLEFOOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag rat
        faction enemies
        type boss
        movement 5
        mana_regen 999
        mana 100
        health 150
        dispersed_bonus_turns 2

        size 2x2
        move_block everything_even_when_dead
        knockback_immune true

        elements [
            Earth
        ]
    }

    abilities {
        move None
        attack None
        
        spells [
            BumblefootLeap
            BumblefootEatCorpse
            BumblefootAttemptEatCat
            BumblefootEatCat
            BumblefootBoneShot
            BumbleButt
        ]
    }

    passives {
        FormChanger {
            Up { 
                animation_suffix "Up"

                ai {
                    brain PatternBrain
                    decision_weights careless
                    move_weights stay_close
                    auto_orient false
                    reset_pattern_on_formswitch true

                    pattern {
                        do BumblefootLeap
                    }
                }
                passives {
                    BackstabImmunity 1
                }
            }
            Down {
                animation_suffix "Down"

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights random
                    auto_orient false
                    reset_pattern_on_formswitch true

                    pattern {
                        do BumblefootBoneShot
                        do_priority [BumblefootEatCorpse, BumblefootEatCat, BumblefootBoneShot]
                    }
                }
                passives {
                    BackstabAllDirections 1
                    ImmediateAbilityReaction BumbleButt
                }
            }

            initial_form Up
        }

        Trample 3
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_always_move
        auto_orient false
    }
}
```

---

### `RockyBobo`
**Name:** Rocky Bobo  
**Source:** `bosses.gon`  

```
RockyBobo {
    graphics {
        movieclip RockyBobo
        name "ENEMY_ROCKYBOBO_NAME"
        move_speed_sync_frames 22.5
        uifloaters_offset 2
        
        shadow_size 2
        water_mask medmed
		tooltip "ENEMY_ROCKYBOBO_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [cat rock]
        faction enemies
        type boss
        movement 4
        dispersed_bonus_turns 2
        mana_regen 999
        mana 100
        
        health 75
        shield 65

        size 2x2
        move_block everything_even_when_dead

        elements [
            Rock
        ]
    }

    abilities {
        move DefaultMove
        attack RockySlam
        
        spells [
            RockSong
        ]
    }

    passives {
        Trample 3
        MoveTowardsDamageSource {
            ability move
            move_short true
            move_far false
            do_not_move_on_top true
            face_towards_after true
            can_move_zero true
        }
    }
    
    ai {
        brain PatternBrain
        mainturn_pattern {
            move_then_do RockSong
        }
        bonusturn_pattern {
            do **RockySlam
        }
        decision_weights always_cast
        move_weights blind_move_far
        auto_orient false
    }
}
```

---

### `Chubs`
**Name:** Chubs  
**Source:** `bosses.gon`  

```
Chubs {
    graphics {
        movieclip Chubs
        name "ENEMY_CHUBS_NAME"
        water_mask medium
		tooltip "ENEMY_CHUBS_DESC"
    }

    stats {
        strength 5
        dexterity 8
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag dog
        faction enemies
        type boss
        movement 3
        mana_regen 999
        mana 100
        
        health 140
        evenly_dispersed_bonus_turns 1
        disperse_main_turns true
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack ChubsSpin
        
        spells [
            ChubsGoop
            ChubsRage
        ]
    }

    passives {
        Buddy Nubs
        ImmediateAbilityReaction ChubsGoop
        AbilityWhenBuddyDies ChubsRage
		
		BossRewards {
			common ChubsCollar
		}
        
        FormChanger {
            Normal { 
                passives {
                    RandomizeAIWeightsEachTurn [
                        {
                            decision_weights blind
                            move_weights chubs_and_nubs_blind
                        }

                        {
                            decision_weights blind
                            move_weights stay_close_always_move
                        }
                    ]
                }
            }
            Rage {
                animation_suffix "Rage"
                attack ChubsSpinRage

                ai {
                    brain PatternBrain

                    pattern {
                        move_then_do attack
                    }

                    decision_weights blind
                    move_weights chubs_and_nubs_rage
                }
            }

            initial_form Normal
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            move_then_do attack
        }

        decision_weights blind
        move_weights chubs_and_nubs_blind
    }
}
```

---

### `Nubs`
**Name:** Nubs  
**Source:** `bosses.gon`  

```
Nubs {
    graphics {
        movieclip Nubs
        name "ENEMY_NUBS_NAME"
        water_mask big
		tooltip "ENEMY_NUBS_DESC"
    }

    stats {
        strength 5
        dexterity 8
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag dog
        faction enemies
        type boss
        movement 1
        mana_regen 999
        mana 100
        corpse_health 0
        health 100
        evenly_dispersed_bonus_turns 1
        disperse_main_turns true
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack NubsJump
        
        spells [
            NubsNuke
            NubsGoop
        ]
    }

    passives {
        Buddy Chubs
        ImmediateAbilityReaction NubsGoop
		
		BossRewards {
			common NubsCollar
		}

        FormChanger {
            Normal { 
                passives {
                    RandomizeAIWeightsEachTurn [
                        {
                            decision_weights blind
                            move_weights chubs_and_nubs_blind
                        }

                        {
                            decision_weights blind
                            move_weights chubs_and_nubs_blind
                        }

                        {
                            decision_weights nubs_fakeblind
                            move_weights chubs_and_nubs_blind
                        }

                        {
                            decision_weights blind
                            move_weights stay_close_always_move
                        }
                    ]
                }
            }
            Rage {
                ai {
                    brain PatternBrain

                    pattern {
                        do *NubsNuke
                    }

                    decision_weights blind
                    move_weights chubs_and_nubs_rage
                }

                turns {
                    takes_main_turn false
                    round_end_bonus_turns 1
                }
            }

            initial_form Normal
        }

        FormChangeWhenBuddyDies Rage
    }
    
    ai {
        brain PatternBrain

        pattern {
            move_then_do NubsJump
        }

        decision_weights blind
        move_weights chubs_and_nubs_blind
    }
}
```

---

### `SpiderQueen`
**Name:** Spinnerette  
**Source:** `bosses.gon`  

```
SpiderQueen {
    graphics {
        movieclip SpiderQueen
        name "ENEMY_SPIDERQUEEN_NAME"
        shadow_size 2
        uifloaters_offset 2
        water_mask medium
        move_speed_sync_frames 7
		tooltip "ENEMY_SPIDERQUEEN_DESC"
    }

    stats {
        strength 10
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag bug
        faction enemies
        type boss
        movement 3
        mana_regen 999
        mana 100
        health 250
        
        takes_main_turn false 

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack BasicBigMelee
        
        spells [
            Leave
            SpiderSpawn
            QueenWeb
            QueenMinis
            Spider_GoInsane
            Spider_CalmDown
            SpiderReturn
            ButtWeb
            ButtWeb_AlreadyEnraged
            ExtraMove
        ]
    }

    passives {
	
		BossRewards {
			common Spinnerets
			rare SpiderBaby
		}
        FormChanger {
            Start_Ceiling { 
                passives {
                    FormChangeOffMap {
                        form_offmap Start_Ceiling
                        form_onmap Default_Ground
                    }

                    MoveTowardsKillers {
                        move_ability SpiderReturn
                        character_filter [SpiderCat, TallSpiderCat]
                    }
                    AutocastEachRound SpiderReturn
                    StartOffMap 1
                }
            }

            Default_Ground {
                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [*QueenWeb, attack, QueenMinis]
                        do_priority [*QueenMinis, QueenWeb]
                        do_priority [attack, Leave]
                    }

                    decision_weights careless
                    move_weights keep_distance_always_move
                    reset_pattern_on_formswitch true
                }

                passives {
                    FormChangeOffMap {
                        form_offmap Default_Ceiling
                        form_onmap Default_Ground
                    }
                    ImmediateAbilityReaction {
                        ability ButtWeb
                        backstabs_only true
                        ability_damage_only true
                    }
                }

                turns {
                    takes_main_turn true
                    dispersed_bonus_turns 2
                }
            }
            Default_Ceiling { 
                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [SpiderSpawn]
                        do_priority [SpiderSpawn]
                        do_priority [SpiderReturn]
                    }

                    decision_weights default_spawn_at_preferred_distance
                    move_weights stay_close_always_move
                    reset_pattern_on_formswitch true
                    end_turn_on_formswitch true
                }

                passives {
                    FormChangeOffMap {
                        form_offmap Default_Ceiling
                        form_onmap Default_Ground
                    }

                    MoveTowardsKillers {
                        move_ability SpiderReturn
                        character_filter [SpiderCat, TallSpiderCat]
                    }
                }

                turns {
                    takes_main_turn true
                    dispersed_bonus_turns 2
                }
            }
            Insane_Ground {
                animation_suffix "Insane"

                ai {
                    brain PatternBrain

                    virtual_abilities {
                        MoveAway {
                            ability ExtraMove
                            move_weights stay_far
                        }
                    }

                    pattern {
                        do_priority [attack, QueenMinis]
                        do_priority [attack, QueenMinis]
                        do_priority [attack, MoveAway, Spider_CalmDown]
                    }

                    decision_weights careless
                    move_weights stay_close_always_move
                    reset_pattern_on_formswitch true
                }

                passives {
                    FormChangeOffMap {
                        form_offmap Insane_Ceiling
                        form_onmap Insane_Ground
                    }
                    AddMovement 2

                    ImmediateAbilityReaction {
                        ability ButtWeb_AlreadyEnraged
                        backstabs_only true
                        ability_damage_only true
                    }
                }

                turns {
                    takes_main_turn true
                    dispersed_bonus_turns 2
                }
            }
            Insane_Ceiling {
                animation_suffix "Insane"

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [SpiderSpawn]
                        do_priority [SpiderSpawn]
                        do_priority [SpiderReturn]
                    }

                    decision_weights default_spawn_at_preferred_distance
                    move_weights stay_close_always_move
                    reset_pattern_on_formswitch true
                    end_turn_on_formswitch true
                }

                passives {
                    FormChangeOffMap {
                        form_offmap Insane_Ceiling
                        form_onmap Insane_Ground
                    }

                    MoveTowardsKillers {
                        move_ability SpiderReturn
                        character_filter [SpiderCat, TallSpiderCat]
                    }
                }

                turns {
                    takes_main_turn true
                    dispersed_bonus_turns 2
                }
            }

            initial_form Start_Ceiling
        }

        Trample 3
        StatusImmunity Webbed

        SpawnThingOnDamage {
            object TinySpider
            good false 
            spawn_on_death_hit false
            chance 50%
        }
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `Johnny`
**Name:** Johnny  
**Source:** `bosses.gon`  

```
Johnny {
    graphics {
        movieclip Johnny
        name "ENEMY_JOHNNY_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_JOHNNY_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag humanoid
        faction enemies
        type boss
        movement 2
        dispersed_bonus_turns 2
        knockback_immune true

        health 250

        size 2x2
        lock_orientation [0, -1]
        move_block everything_even_when_dead
        boss_minions_runaway false
        banned_elite_buffs [Twin]
    }

    abilities {
        move None
        attack None

        spells [
            JohnnyCryOne
            JohnnyCryTwo
            JohnnyPush
            JohnnyPull
            JohnnyMindControl
            JohnnyBlast
            JohnnyMegaBlast
        ]
    }

    passives {
        Trample 3
		
		BossRewards {
			common JohnnysUndies
			rare JohnnysStool
		}

        FormChanger {
            Unwashed {
                partial_animation_suffix Unwashed

                ai {
                    brain PatternBrain

                    pattern {
                        do JohnnyCryOne
                        do JohnnyCryOne
                        do JohnnyCryOne
                        do JohnnyCryTwo
                    }

                    clamp_pattern true

                    decision_weights always_cast
                    move_weights stay_close
                    reset_pattern_on_formswitch true
                    end_turn_on_formswitch false
                }
            }
            Washed {
                ai {
                    brain PatternBrain
                    attack JohnnyBlast

                    pattern {
                        do_best [JohnnyPush JohnnyPull]
                        do JohnnyMindControl
                        do JohnnyBlast
                        do JohnnyMegaBlast
                    }

                    fallback {
                        do JohnnyBlast
                    }

                    decision_weights careless
                    move_weights stay_close
                    reset_pattern_on_formswitch false
                    end_turn_on_formswitch false
                }

                passives {
                    InnateElement Water
                }
            }

            initial_form Unwashed
        }

        JohnnyNeedsWashing {
            form_washed Washed
            form_unwashed Unwashed
        }
    }
    
    ai {
        brain NoBrain 
        
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `AlienBeast`
**Name:** Crater Maker  
**Source:** `bosses.gon`  

```
AlienBeast {
    graphics {
        movieclip AlienBeast
        name "ENEMY_CRATERMAKER_NAME"
        projectile_spawn_offset [0 1]
        shadow_size 3
        uifloaters_offset 2.5
        water_mask square
		tooltip "ENEMY_CRATERMAKER_DESC"
    }

    stats {
        strength 9
        dexterity 9
        constitution 9
        intelligence 9
        speed 9
        charisma 9
    }
    
    properties {
        tag alien
        faction enemies
        type boss
        
        health 280

        size 3x3
        movement 2

        move_block everything_even_when_dead
        round_start_bonus_turns 1
        
        initiative -999
    }

    abilities {
        move DefaultMove
        attack BasicBigMelee

        spells [
            AlienBeastScream  
            AlienBeastEat     
            AlienBeastPuke    
            AlienBeastRampage 

            AlienBeastGoop
            AlienBeastOpenEyes

            AlienBeastMoveOne
        ]
    }

    passives {
        Trample 3
		
		BossRewards {
			common FriendlyAmoeba
			rare AlienStalk
		}
		
        ImmediateAbilityReaction {
            ability_damage_only true
            ability AlienBeastGoop
        }
        AlienBeastEyeStalks 3
        AlienBeastDangerZones [AlienBeastScream AlienBeastEat AlienBeastPuke AlienBeastRampage]
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveOneForPuke {
                ability AlienBeastMoveOne
                move_for_ability AlienBeastPuke
                move_weights keep_distance
            }
        }

        bonusturn_pattern {
            do_all [attack AlienBeastOpenEyes]
        }
        mainturn_pattern {
            do_all [*AlienBeastScream *AlienBeastEat *AlienBeastPuke *AlienBeastRampage]
        }
        
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `TheCoven`
**Name:** The Coven  
**Source:** `bosses.gon`  

```
TheCoven {
    graphics {
        movieclip TheCoven
        name "ENEMY_COVEN_NAME"
        uifloaters_offset 2.5
        water_mask square
        scale .8
        
        shadow TormentorShadow
		tooltip "ENEMY_COVEN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid tumor]
        hidden_tag the_coven
        faction enemies
        type boss
        lock_orientation [0, -1]
        
        health 350
        initiative -999

        size 3x3
        movement 1

        move_block everything_even_when_dead
        evenly_dispersed_bonus_turns 1
        can_be_backstabbed false
        knockback_immune true
        banned_elite_buffs [Twin]
    }

    abilities {
        move None
        attack BasicMelee

        spells [
            CovenRise1
            CovenRise2
            CovenRise3
            CovenRise4
            CovenSummon
            CovenPestilence
            CovenFamine
            CovenWar
        ]
    }

    passives {
        Trample 3
        DemonicGlyphFrames 1
		
		BossRewards {
			common PentagramSigil
		}

        FormChanger {
            0 {
                ai {
                    brain PatternBrain
                    end_turn_on_formswitch true

                    pattern {
                        do CovenRise1
                    }
        
                    decision_weights default
                    move_weights stay_close
                }
            }
            1 {
                animation_suffix 1

                ai {
                    brain PatternBrain
                    end_turn_on_formswitch true

                    pattern {
                        do_all [CovenPestilence CovenRise2]
                    }
        
                    decision_weights default
                    move_weights stay_close
                }
            }
            2 {
                animation_suffix 2

                ai {
                    brain PatternBrain
                    end_turn_on_formswitch true

                    pattern {
                        do_all [CovenFamine CovenRise3]
                    }
        
                    decision_weights default
                    move_weights stay_close
                }
            }
            3 {
                animation_suffix 3

                ai {
                    brain PatternBrain
                    end_turn_on_formswitch true

                    pattern {
                        do_all [CovenWar CovenRise4]
                    }
        
                    decision_weights default
                    move_weights stay_close
                }
            }
            4 {
                animation_suffix 4

                ai {
                    brain PatternBrain
                    end_turn_on_formswitch true

                    pattern {
                        do CovenSummon
                    }
        
                    decision_weights default
                    move_weights stay_close
                }
            }

            initial_form 0
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do none
        }
        
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Tormentor`
**Name:** Tormentor  
**Source:** `bosses.gon`  

```
Tormentor {
    graphics {
        movieclip Tormentor
        name "ENEMY_TORMENTOR_NAME"
        uifloaters_offset 4
        water_mask square
        scale .8
        
        shadow TormentorShadow
        
        status_display_count_max 5
		tooltip "ENEMY_TORMENTOR_DESC"
        dont_sink true
    }

    stats {
        strength 8
        dexterity 8
        constitution 8
        intelligence 8
        speed 8
        charisma 8
        luck 8
    }
    
    properties {
        tag demon
        faction enemies
        type boss
        flying true
        
        health 170

        size 3x3
        movement 2

        move_block everything_even_when_dead
        dispersed_bonus_turns 0
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack BasicMelee

        spells [
            TormentorRuneAbsorb
            TormentorBite
            TormentorSpawn
            TormentorSuck
        ]
    }

    passives {
        TormentorHeal 1
        UseAbility TormentorRuneAbsorb
        DemonicGlyphFrames 1
        DemonicGlyphStealer 1
		
		BossRewards {
			common LuciferSigil
		}

        FormChanger {
            NotPriming {
                turns {
                    takes_main_turn true
                    round_end_bonus_turns 1
                    dispersed_bonus_turns 0
                    wait_till_next_round_to_update_turns true
                }

                passives {
                    PassiveWhileHasStatus {
                        status DemonicGlyph_Bite
                        passives {
                            ExtraDispersedTurns 1
                        }
                    }
                    PassiveWhileHasStatus {
                        status DemonicGlyph_Summon
                        passives {
                            ExtraDispersedTurns 1
                        }
                    }
                }
            }
            Priming {
                turns {
                    takes_main_turn false
                    round_end_bonus_turns 1
                    dispersed_bonus_turns 0
                    wait_till_next_round_to_update_turns true
                }

                passives {

                }
            }
        }

        FormChangeWhilePrimingAbility {
            priming Priming
            not_priming NotPriming
        }
        PassiveWhileHasStatus {
            status DemonicGlyph_Fire
            passives {
                AddDamage 2
                AddStatusToBasicAttack {
                    Burn 2
                }
            }
        }
        PassiveWhileHasStatus {
            status DemonicGlyph_Movement
            passives {
                AddMovement 1
                Trample 6
            }
        }
        PassiveWhileNotHasStatus { 
            status DemonicGlyph_Movement
            passives {
                Trample 3
            }
        }
        PassiveWhileHasStatus {
            status DemonicGlyph_Bounce
            passives {
                MeleeRevengeDamage {
                    knockback 2
                }
            }
        }
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights stay_close
        stun_advances_pattern true
        reset_pattern_on_formswitch true
        reset_pattern_on_round_begin true

        virtual_abilities {
            SuckMF {
                ability TormentorSuck
                decision_weights careless
                move_weights keep_distance
            }
        }
        
        mainturn_pattern {
            do attack
        }
        bonusturn_pattern {
            do_priority [TormentorBite TormentorSpawn attack]
            do_priority [TormentorSpawn TormentorBite attack]
        }
        
        round_end_bonusturn_pattern {
            do SuckMF
        }
    }
}
```

---

### `MoonHead`
**Name:** Man In The Moon  
**Source:** `bosses.gon`  

```
MoonHead {
    graphics {
        movieclip MoonHead
        name "ENEMY_MANINTHEMOON_NAME"
        uifloaters_offset 2
        water_mask square
        shadow_size 3
		tooltip "ENEMY_MANINTHEMOON_DESC"
		no_splatter true
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [alien rock]
        hidden_tag [moonhead moonboss]

        faction enemies
        type boss
        
        health 400

        size 3x3
        movement 0

        move_block everything_even_when_dead
        round_end_bonus_turns 1
        initiative 100
        knockback_immune true
        corpse_health 0

        lock_orientation [-1 0]
        banned_elite_buffs [Twin]
    }

    abilities {
        move None
        attack None

        spells [
            MoonHead_BeginCharge
            MoonHead_EatCat
            MoonHead_Barrage
            MoonHead_Blow

            MoonHead_Finisher

            MoonHead_Digest
            MoonHead_SpitCat
            MoonHead_ChewCat
            
            MoonHead_SacrificeHand
            MoonHead_SpawnHand
            MoonHead_SpitCat_AndDie
            MoonHead_CommandHeadPunch
            MoonHead_RefreshBrace
            MoonHead_CallForHelp
        ]
    }

    passives {
        Brace 10

        
            

           
            
        

        DeathRattle MoonHead_KillHands
		
		BossRewards {
			common Asteroid
			rare AlienTech
		}

        FormChanger {
            Default {
                partial_animation_suffix ""

                ai {
                    brain PatternBrain

                    pattern {
                        do MoonHead_BeginCharge
                    }
                    round_end_bonusturn_pattern {
                        
                        do_all [MoonHead_CallForHelp MoonHead_RefreshBrace]
                    }

                    decision_weights careless
                    move_weights stay_close
                    end_turn_on_formswitch false
                }
            }
            Charging {
                partial_animation_suffix "Charging"
                attack MoonHead_Blow

                passives {
                    MovementReaction {
                        ability MoonHead_EatCat
                        enemies_only true
                    }

                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has HasCat
                    }

                    DisplayDangerAOE MoonHead_Blow
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do MoonHead_Blow
                    }

                    end_turn_on_formswitch true
                    decision_weights careless
                    move_weights stay_close
                }
            }
            HasCat {
                partial_animation_suffix "Swallowed"
                attack MoonHead_ChewCat

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot Default
                    }

                    DigestDeadBodies MoonHead_Digest
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do MoonHead_ChewCat
                    }
                    round_end_bonusturn_pattern {
                        
                        do_all [MoonHead_ChewCat MoonHead_CallForHelp MoonHead_RefreshBrace]
                    }

                    decision_weights careless
                    move_weights stay_close
                    end_turn_on_formswitch false
                }
            }

            
            Hint_CrackedVisuals {
                animation_suffix "Cracked"
            }
            Hint_CrackedVisuals2 {
                animation_suffix "ChargingCracked"
            }
            Hint_CrackedVisuals3 {
                animation_suffix "SwallowedCracked"
            }
        }

        MoonHeadCrackedVisual Cracked
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `MoonHand`
**Name:** Moon Hand  
**Source:** `bosses.gon`  

```
MoonHand {
    graphics {
        movieclip MoonHand
        name "ENEMY_MOONHAND_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_MOONHAND_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [alien rock]
        hidden_tag [moonhand moonboss]

        faction enemies
        type boss

        movement 3
        health 100
        flying true
        disperse_main_turns true
        kill_required false
    }

    abilities {
        move DefaultMove
        attack MoonHandSlap
        
        spells [
            MoonHandGrab
            MoonHandDash
            MoonHandThrow
            MoonHandDrop_Deathrattle
            MoonHandDrop
            MoonHandMegaSqueeze
            MoonHandPunchHead
        ]
    }

    passives {
        FaceAwayLastDamage {
            use_turn_animations true
            override_hit_animation true
            ability_damage_only true
        }
        WideBackstab 1

        LimitDamage 1
        LimitHeal 0
        StripStatuses 1

        FormChangeWhileHasStatus {
            status Consuming
            form_has HasCat
            form_hasnot Default
        }

        FormChanger {
            Default {
                passives {
                    AbilityReaction {
                        ability MoonHandDash
                        backstabs_only true
                        ability_damage_only true
                        match_knockback_direction true
                        cancel_knockback true
                        even_on_0_damage_if_knockback true
                    }
                    /*Trapper {
                        ability MoonHandGrab
                        non_active_turn_only true
                        on_self_move true
                    }*/
                    MovementReaction {
                        ability MoonHandGrab
                        on_self_move_too true
                        forward_only true
                        self_move_exclude_self_abilities true
                    }
                }

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights stay_close

                    pattern {
                        do attack
                    }
                }
            }
            HasCat {
                animation_suffix "Grabbing"
                attack MoonHandSqueeze
                move None

                passives {
                    ChanceToSpitOnDamage {
                        backstabs_only true
                        flat_chance 100%
                        ability MoonHandDrop
                        even_on_0_damage_if_knockback true
                    }
                    DeathRattle {
                        ability MoonHandDrop_Deathrattle
                        pop_corpse false
                        is_dying_animation true
                    }
                }

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights stay_close

                    pattern {
                        
                        do attack
                    }
                }
            }
        }
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `BungaThrone`
**Name:** Throne  
**Source:** `bosses.gon`  

```
BungaThrone {
    graphics {
        movieclip BungaThrone
        name "ENEMY_BUNGATHRONE_NAME"
        uifloaters_offset 3
        depth_offset .01
		tooltip "ENEMY_BUNGATHRONE_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag skeleton
        faction none
        type object

        takes_turns false
        kill_required false

        health 0
        shield 100
        

        size 2x2
        lock_orientation [-1 0]
        move_block everything_even_when_dead
    }

    abilities {
        move None
        attack None
    }

    passives {
        Trample 3
        NoHealthOnlyShield 1
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `LordBunga`
**Name:** Lord Bunga  
**Source:** `bosses.gon`  

```
LordBunga {
    graphics {
        movieclip LordBunga
        name "ENEMY_LORDBUNGA_NAME"
        uifloaters_offset 3
		tooltip "ENEMY_LORDBUNGA_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag humanoid
        faction cavemen
        type boss
        movement 2
        dispersed_bonus_turns 2

        health 300

        size 2x2
        lock_orientation [-1 0]
        move_block everything_even_when_dead
        boss_minions_runaway false
        banned_elite_buffs [Twin]
    }

    abilities {
        move DoNothing
        attack DoNothing

        spells [
            BungaEntrance
            BungaEatCat
            BungaSwipe
            BungaRoar
        ]
    }

    passives {
        Trample 3
		
		BossRewards {
			common BungasBone
			rare BungasCrown
		}

        FormChanger {
            Sitting {
                animation_suffix Chair
                move DoNothing
                attack DoNothing

                passives {
                    KnockbackImmunity 1

                    BungaCheers {
                        warrior_tag bungawarrior
                        ally_damage littleboo
                        ally_dead bigboo
                        enemy_damage littlecheer
                        enemy_dead bigcheer
                    }

                    BungaEntrance {
                        warrior_tag bungawarrior
                        ability BungaEntrance
                        health_threshold 150
                        even_if_stunned true
                    }
                }

                turns {
                    takes_turns false
                }

                ai {
                    brain NoBrain
                }
            }
            Standing {
                move DefaultMove
                attack BungaSmash

                passives {
                    UnlockOrientation 1
                    CounterAttack BungaSwipe
                    FormChangeHealthThreshold {
                        threshold 50
                        form_below Standing2
                        form_above Standing
                    }
                }

                turns {
                    takes_turns true
                    dispersed_bonus_turns 1
                }

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights stay_close

                    pattern {
                        do_all [*BungaEatCat attack BungaRoar move]
                    }
                }
            }
            Standing2 {
                move BungaJumpMove
                attack BungaSmash

                passives {
                    UnlockOrientation 1
                    CounterAttack BungaSwipe
                    AddMovement 2
                }

                turns {
                    takes_turns true
                    dispersed_bonus_turns 1
                }

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights stay_close

                    pattern {
                        do_all [*BungaEatCat attack BungaRoar move]
                    }
                }
            }

            initial_form Sitting
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `QueenHippo`
**Name:** Queen Hippo  
**Source:** `bosses.gon`  

```
QueenHippo {
    graphics {
        movieclip QueenHippo
        name "ENEMY_QUEENHIPPO_NAME"
        uifloaters_offset 1.75
		tooltip "ENEMY_QUEENHIPPO_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss

        health 80

        movement 0

        dispersed_bonus_turns 1
        round_end_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack QueenHippoAttack
        
        spells [
            QueenHippoUppercut
            QueenHippoTire
            QueenHippoHeartAttack
        ]
    }

    passives {
        Brace 4
		
		BossRewards {
			common MissingNipple
			rare QueensCrown
		}

        UseAbilityWhenOutOfStatus {
            status Brace
            ability QueenHippoHeartAttack
        }
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights stay_close

        pattern {
            do_all [*QueenHippoUppercut QueenHippoAttack move]
        }
        round_end_bonusturn_pattern {
            do_all [*QueenHippoUppercut QueenHippoAttack move QueenHippoTire]
        }
    }
}
```

---

### `Trampy`
**Name:** Trampy  
**Source:** `bosses.gon`  

```
Trampy {
    graphics {
        movieclip Trampy
        name "ENEMY_TRAMPY_NAME"
        uifloaters_offset 1.75
		tooltip "ENEMY_TRAMPY_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss

        health 99

        movement 3

        dispersed_bonus_turns 3
        base_crit_chance 0
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            TrampyDrink
            TrampyDump
            TrampySpit
            TrampyFleas
            TrampySleep
        ]
    }

    passives {
        MissChance 20
        
        

        FormChanger {
            Default {
                /*ai {
                    brain PatternBrain
                    decision_weights extra_careless
                    move_weights trampy_chaos

                    pattern {
                        do_random [attack TrampyDump TrampySpit TrampyFleas TrampySleep]
                        do_random [attack TrampyDump TrampySpit TrampyFleas TrampySleep]
                        do_random [attack TrampyDump TrampySpit TrampyFleas TrampySleep]
                        do_priority [*TrampyDrink TrampyDrink]
                    }
                    stun_advances_pattern false
                    fallback_advances_pattern false
                }*/
            }
            Drunker {
                partial_animation_suffix Drunk
            }
            initial_form Default
        }
    }
    
    ai {
        brain PatternBrain
        decision_weights extra_careless
        move_weights trampy_chaos

        pattern {
            
            do TrampyDump
            do TrampySpit
            do TrampyFleas
            do_priority [*TrampyDrink TrampyDrink]
            do attack
            do TrampySleep
        }

        stun_advances_pattern false
        fallback_advances_pattern false
    }
}
```

---

### `Dybbuk`
**Name:** Dybbuk  
**Source:** `bosses.gon`  

```
Dybbuk {
    graphics {
        movieclip Dybbuk
        name "ENEMY_DYBBUK_NAME"
        no_splatter true
		scale 1.1
		tooltip "ENEMY_DYBBUK_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [cat ghost]
        faction enemies
        type boss

        health 85

        movement 3

        dispersed_bonus_turns 2
        corpse_health 0
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack DybbukLick
        
        spells [
            DybbukWisps
            DybbukReanimate
            DybbukEscape


            DybbukPossess
            DybbukReturn
            DybbukRePossess
        ]
    }

    passives {
        Dybbuk1HPTracker 1
        DybbukPossessionFallback {
            form Possessing
            exit_ability DybbukReturn
        }
		
		BossRewards {
			common CoffinArmor
			rare DybbuksRib
		}

        FormChanger {
            Default {

                passives {
                    SurviveAt1HP 1

                    AbilityHealthThreshold {
                        even_if_stunned true
                        threshold 1
                        ability DybbukPossess
                        use_ai true
                    }

                }
            }
            Possessing {
                animation_suffix "Possessing"

                turns {
                    takes_turns false
                }

                passives {
                    SurviveAt1HP 1
                }
            }
            LastHit {
                turns {
                    takes_turns true
                    dispersed_bonus_turns 2
                }
            }
            Bully {
                turns {
                    takes_turns true
                }

                passives {
                    AddInitiative -9999
                }

                ai {
                    brain PatternBrain

                    virtual_abilities {
                        Escape {
                            ability DybbukEscape
                            move_weights keep_distance_always_move
                        }
                    }

                    pattern {
                        do_all_shuffle [attack DybbukWisps DybbukRePossess]
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
        }


        ChanceToBackflip {
            chance 100%
            ability DybbukBackflipDodge
        }
        Undead 1
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            Escape {
                ability DybbukEscape
                move_weights keep_distance_always_move
            }
        }

        pattern {
            do_random [Escape attack DybbukReanimate]
            do_random [Escape attack DybbukReanimate DybbukWisps]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `HitlerHead`
**Name:** Hitler  
**Source:** `bosses.gon`  

```
HitlerHead {
    graphics {
        movieclip HitlerHead
        name "ENEMY_HITLERHEAD_NAME"
        uifloaters_offset 3
        shadow_size 2
        art_flip -1
		tooltip "ENEMY_HITLERHEAD_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid robot]
        faction enemies
        type boss
        movement 2
        dispersed_bonus_turns 2

        health 200
        shield 200

        size 2x2
        lock_orientation [-1 0]
        move_block everything_even_when_dead
        boss_minions_runaway false
    }

    abilities {
        move DoNothing
        attack DoNothing

        spells [
            HitlerHeadGrowA
            HitlerHeadGrowB
            HitlerHeadTransform
        ]
    }

    passives {
        Trample 3
        Brace 1
        Robot 1
    }
    
    ai {
        brain PatternBrain
        pattern {
            do_priority [HitlerHeadTransform HitlerHeadGrowA]
            do_priority [HitlerHeadTransform HitlerHeadGrowB]
        }

        decision_weights always_cast
        move_weights keep_distance
    }
}
```

---

### `Hitler`
**Name:** Hitler  
**Source:** `bosses.gon`  

```
Hitler {
    graphics {
        movieclip Hitler
        name "ENEMY_HITLER_NAME"
        uifloaters_offset 4
        shadow_size 2
		tooltip "ENEMY_HITLER_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid robot]
        faction enemies
        type boss
        movement 4
        dispersed_bonus_turns 2

        health 200
        shield 200

        size 2x2
        move_block everything_even_when_dead
        boss_minions_runaway false
    }

    abilities {
        move GooseStep
        attack HitlerShoot

        spells [
            HitlerHeil
            HitlerSuicide
            HitlerNuke
        ]
    }

    passives {
        Trample 3
        Robot 1
		
		BossRewards {
			common HitlersPistol
			rare HitlersMustache
		}

        FormChanger {
            Default {
                passives {
                    HitlerExecute {
                        tag grown_hitler_clone
                        ability HitlerShoot
                        threshold 15
                    }

                    ImmediateAbilityReaction {
                        ability HitlerSuicide
                        health_threshold 50
                    }
                }
            }
            Nuke {
                animation_suffix Nuke
                attack None
                move None

                passives {
                    DebuffImmunity 1
                    BuffImmunity 1
                    AddInitiative -10
                }

                turns {
                    dispersed_bonus_turns 0
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do HitlerNuke
                    }

                    move_weights stay_close
                    decision_weights always_cast
                }
            }
        }
        
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [attack *HitlerHeil move]
        }
        mainturn_pattern {
            do_priority [*HitlerHeil attack move]
        }

        move_weights stay_close_move_far
        decision_weights default
    }
}
```

---

### `MegaDinoLeg`
**Name:** Dreadnoughtus  
**Source:** `bosses.gon`  

```
MegaDinoLeg {
    graphics {
        movieclip MegaDinoLeg
        name "ENEMY_DREADNOUGHTUSLEG_NAME"
        uifloaters_offset 2
        water_mask medium
        shadow_size 2
        art_flip -1
        always_huge_mask true
		tooltip "ENEMY_DREADNOUGHTUSLEG_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [dinosaur]
        hidden_tag [megadino megadinoleg]

        faction enemies
        type boss
        
        health 55

        size 2x2
        movement 2

        move_block everything_even_when_dead
        
        corpse_health indestructible
        kill_required false

        disperse_main_turns true

        lock_orientation [-1 0]
        banned_elite_buffs [Twin]
    }

    abilities {
        move MD_Walk
        attack MD_Stomp

        spells [
            MD_Lift
            MD_Kick
            MD_LegLeave
            MD_LegReturn
        ]
    }

    passives {
        Trample 3

        FormChanger {
            Default {
                turns {
                    takes_turns true
                }
                passives {
                    MoveTowardsDamageSource {
                        check_in_form Default
                        move_ability MD_WalkOne
                        ignore_tagged_sources megadino
                    }
                }
            }
            Lifted {
                animation_suffix "Lift"
                attack None
                move None

                passives {
                    ForceDodgeEverything 1
                    Flying 1
                }

                turns {
                    takes_turns false
                }
            }
            OffMap {
                turns {
                    takes_turns false
                }
            }
        }

        UnlimitedDeathRattleRevive {
            ability MD_Lift
            even_if_stunned true
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*attack move]
        }

        decision_weights careless
        move_weights stay_close
    }
}
```

---

### `MegaDinoHead`
**Name:** Dreadnoughtus  
**Source:** `bosses.gon`  

```
MegaDinoHead {
    graphics {
        movieclip MegaDinoHead
        name "ENEMY_DREADNOUGHTUSHEAD_NAME"
        uifloaters_offset 2
        water_mask square
        shadow_size 3
        art_flip -1
        always_huge_mask true
		tooltip "ENEMY_DREADNOUGHTUSHEAD_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [dinosaur]
        hidden_tag megadino

        faction enemies
        type boss
        
        health 600

        size 3x3
        movement 0

        move_block everything_even_when_dead
        knockback_immune true
        initiative -100

        corpse_health indestructible

        lock_orientation [-1 0]
        banned_elite_buffs [Twin]
    }

    abilities {
        move None
        attack None

        spells [
            MD_HeadLeave
            MD_HeadDrop
            MD_Poop
        ]
    }

    passives {
        Trample 3
        StartOffMap 1
		
		BossRewards {
			common MegaPoop
			rare GreenWhistle
		}

        FormChanger {
            Default {
                passives {
                    StunImmunity {
                        cleanse_on_apply false
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do MD_HeadLeave
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }
            OffMap {
                ai {
                    brain PatternBrain

                    pattern {
                        do MD_Poop
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }
            initial_form OffMap
        }

        MegaDinoDropController {
            leg_leave MD_LegLeave
            leg_return MD_LegReturn
            head_drop MD_HeadDrop
            stable_legs 3
        }
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `MotherTumor`
**Name:** The Mother  
**Source:** `bosses.gon`  

```
MotherTumor {
    graphics {
        movieclip MotherTumor
        name "ENEMY_MOTHERTUMOR_NAME"
		tooltip "ENEMY_MOTHERTUMOR_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [tumor]
        hidden_tag [themother]
        faction enemies
        type boss

        health 5

        movement 0

        takes_turns false
        corpse_health 0
        lock_orientation [0 -1]
        can_be_backstabbed false
        knockback_immune true
        held_coins 0
        kill_required false
        can_be_elite false
    }

    abilities {
        move None
        attack None
        
        spells [
            MotherTumorGrow
        ]
    }

    passives {
        StunImmunity 1
        MotherTumorSpawnInCapture {
            Cat {
                animation spawnHoldingCat
                formchange SmallHoldingCat
                statuses {
                    Consumed {
                        instant true
                        mount_mode auto
                        force_contact true
                        do_not_pop_corpse true
                        struggle_ability Thrash
                        drop_on_death deferred
                    }
                }
            }
            NonCat {
                animation spawnHolding
                formchange SmallHolding
                statuses {
                    Consumed {
                        instant true
                        mount_mode auto
                        use_placeholder true
                        force_contact true
                        do_not_pop_corpse true
                        struggle_ability Thrash
                        drop_on_death deferred
                    }
                }
            }
            Nothing {
                animation spawn
            }
        }

        FormChanger {
            Small {
                animation_suffix ""
            }
            SmallHolding {
                animation_suffix "Holding"

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot Small
                    }
                }
            }
            SmallHoldingCat {
                animation_suffix "HoldingCat"

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot Small
                    }
                }
            }
            Big {
                animation_suffix "Big"
            }
            BigHolding {
                animation_suffix "BigHolding"

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot Big
                    }
                }
            }
            BigHoldingCat {
                animation_suffix "BigHoldingCat"

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot Big
                    }
                }
            }
        }

        
        MotherTumorPassive {
            considered_forms [Big BigHolding BigHoldingCat] 
        
            pass_ani pass
            receive_ani receive
            grow_ability MotherTumorGrow

            
            Cat {
                formchange BigHoldingCat
                statuses {
                    Consumed {
                        instant true
                        mount_mode auto
                        force_contact true
                        do_not_pop_corpse true
                        struggle_ability Thrash
                        drop_on_death deferred
                    }
                }
            }
            NonCat {
                formchange BigHolding
                statuses {
                    Consumed {
                        instant true
                        mount_mode auto
                        use_placeholder true
                        force_contact true
                        do_not_pop_corpse true
                        struggle_ability Thrash
                        drop_on_death deferred
                    }
                }
            }
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `MotherTumorBig`
**Source:** `bosses.gon`  

```
MotherTumorBig {
    variant_of MotherTumor

    properties {
        health 9
    }

    passives {
        MotherTumorSpawnInCapture {
            Cat {
                formchange BigHoldingCat
            }
            NonCat {
                formchange BigHolding
            }
        }
        FormChanger {
            initial_form Big
        }
    }
}
```

---

### `TheMother`
**Name:** The Mother  
**Source:** `bosses.gon`  

```
TheMother {
    graphics {
        movieclip TheMother
        name "ENEMY_MOTHER_NAME"
        uifloaters_offset 3
        water_mask square
        shadow_size 3
        art_flip -1
		tooltip "ENEMY_MOTHER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 0
        charisma 5
        luck 5
    }
    
    properties {
        tag [tumor]
        hidden_tag [themother]

        faction enemies
        type boss
        
        health 450

        size 3x3
        movement 0

        move_block everything_even_when_dead
        knockback_immune true
        evenly_dispersed_bonus_turns 1
        boss_minions_runaway false

        lock_orientation [-1 0]
        banned_elite_buffs [Twin]
    }

    abilities {
        move None
        attack SpawnMotherSpike

        spells [
            MotherConsume
            TheMother_Birth
        ]
    }

    passives {
	
		BossRewards {
			common MothersTeeth
			rare MothersLove
		}
		
        MotherGrowController {
            tumor_object MotherTumor
            eat_damage {
                type melee
                damage 0
                piercing true
                cant_miss true
                makes_contact true

                effects {
                    Vaporize 20
                }
            }
        }
        PrioritizeFarAwayTargets 10
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [MotherConsume TheMother_Birth SpawnMotherSpike]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `MotherSpike`
**Name:** The Mother  
**Source:** `bosses.gon`  

```
MotherSpike {
    graphics {
        movieclip MotherSpike
        name "ENEMY_MOTHERSPIKE_NAME"
        uifloaters_offset 2
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [tumor]
        hidden_tag [themother themotherspike]
        faction enemies
        type boss

        health 10
        visually_spiky true

        movement 0

        takes_turns false
        corpse_health 0
        can_be_backstabbed false
        knockback_immune true
        held_coins 0
        kill_required false
        can_be_elite false
    }

    abilities {
        move None
        attack None
        
        spells [
            
        ]
    }

    passives {
        Thorns 5
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `TomTom`
**Name:** Tom Tom  
**Source:** `cat_enemies.gon`  

```
TomTom {
    graphics {
        movieclip _CAT
        name "ENEMY_TOMTOM_NAME"
        custom_cat_data TomTom
        scale 1.1
        shadow_size 1.1

        tooltip "ENEMY_TOMTOM_DESC"
    }

    sound { alt_sounds [[SE_CatWalk SE_Cat_StompWalk]] }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 15
        base_mana_regen 999
        faction enemies
    }

    abilities {
        move DefaultMove
        attack WideSwipe
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Mangy`
**Name:** Mangy  
**Source:** `cat_enemies.gon`  

```
Mangy {
    graphics {
        movieclip _CAT
        name "ENEMY_MANGY_NAME"
        custom_cat_data Mangy
        scale 1
        shadow_size 1

        tooltip "ENEMY_MANGY_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 7
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack PoisonShot
        
        spells [

        ]
    }

    passives {
        SpawnThingOnDamage {
            object Maggot
            good false 
            spawn_on_death_hit false
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Kitten`
**Name:** Kitten  
**Source:** `cat_enemies.gon`  

```
Kitten {
    graphics {
        movieclip _CAT
        name "ENEMY_KITTEN_NAME"
        custom_cat_data Kitten
        scale .8
        shadow_size .8

        tooltip "ENEMY_KITTEN_DESC"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 5
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            
        ]
    }

    passives {
        MoveWhenDamaged {
            weights stay_far_always_move
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `CatCaller`
**Name:** Cat Caller  
**Source:** `cat_enemies.gon`  

```
CatCaller {
    graphics {
        movieclip _CAT
        name "ENEMY_CATCALLER_NAME"
        custom_cat_data CatCaller
        alt_animations [[idle girlyIdle]]

        tooltip "ENEMY_CATCALLER_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        auto_run_priority support
        health 7
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            CatCall
        ]
    }

    passives {
        CounterAttack attack
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights keep_far_distance

        pattern {
            do_priority [*CatCall, CatCall]
        }
    }
}
```

---

### `Multicat`
**Name:** Multicat  
**Source:** `cat_enemies.gon`  

```
Multicat {
    graphics {
        movieclip Multicat
        name "ENEMY_MULTICAT_NAME"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        health 30
        faction enemies
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        
        
        MulticatHeads 0
    }
    
    ai {
        brain GenericBrain
        decision_weights angry
        move_weights stay_close
    }
}
```

---

### `GlassSpitter`
**Name:** Glass Spitter  
**Source:** `cat_enemies.gon`  

```
GlassSpitter {
    graphics {
        movieclip _CAT
        name "ENEMY_GLASSSPITTER_NAME"
        custom_cat_data GlassSpitter
        alt_animations[[idle twitchyIdle]]

        tooltip "ENEMY_GLASSSPITTER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 5
        shield 5
        base_mana_regen 999
        faction enemies
    }

    abilities {
        move DefaultMove
        attack SpitGlass
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_ranged_distance
    }
}
```

---

### `Siren`
**Name:** Siren  
**Source:** `cat_enemies.gon`  

```
Siren {
    graphics {
        movieclip _CAT
        name "ENEMY_SIREN_NAME"
        custom_cat_data Siren

        tooltip "ENEMY_SIREN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat siren]
        type cat
        auto_run_priority support
        health 7
        base_mana_regen 999
        faction enemies
        initiative 5
    }

    abilities {
        move DefaultMove
        attack SirenCall
        
        spells [

        ]
    }

    passives {
        HealNeighborsEachTurn {
            stacks 3
            allies_only true
        }
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights stay_near_allies_siren

        pattern {
            do SirenCall
        }
    }
}
```

---

### `Jekyll`
**Name:** Jekyll  
**Source:** `cat_enemies.gon`  

```
Jekyll {
    graphics {
        movieclip _CAT
        name "ENEMY_JEKYLL_NAME"
        custom_cat_data Jekyll
        scale .75
        alt_animations[[idle cuteIdle]]

        tooltip "ENEMY_JEKYLL_DESC"
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 7
        base_mana_regen 999
        faction enemies
        initiative 12
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        CanMutateTo Hyde
        MutateAfterXTurns 3
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights stay_far

        mainturn_pattern {
            move_then_do attack
        }
    }
}
```

---

### `Hyde`
**Name:** Hyde  
**Source:** `cat_enemies.gon`  

```
Hyde {
    graphics {
        movieclip _CAT
        name "ENEMY_HYDE_NAME"
        custom_cat_data Hyde
        scale .85
        spawnin_animation "howl"

        tooltip "ENEMY_HYDE_DESC"
    }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 20
        base_mana_regen 999
        faction enemies
        initiative 10
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack FurySwipes_Enemy
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close_always_move
    }
}
```

---

### `SpikedCat`
**Name:** Spiked Cat  
**Source:** `cat_enemies.gon`  

```
SpikedCat {
    graphics {
        movieclip _CAT
        name "ENEMY_SPIKEDCAT_NAME"
        custom_cat_data SpikedCat
        alt_animations[[idle twitchyIdle]]

        tooltip "ENEMY_SPIKEDCAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        type cat
        health 5
        shield 8
        base_mana_regen 999
        faction enemies
        initiative 10
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        Thorns 3
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `PopeyeCat`
**Name:** Popeye  
**Source:** `cat_enemies.gon`  

```
PopeyeCat {
    graphics {
        movieclip _CAT
        name "ENEMY_POPEYE_NAME"
        custom_cat_data PopeyeCat
        scale 1.1
        alt_animations[[idle dopeyIdle]]

        tooltip "ENEMY_POPEYE_DESC"
    }

    stats {
        strength 8
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 17
        base_mana_regen 999
        faction enemies
    }

    abilities {
        move DefaultMove
        attack PopeyeDash
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_popeye
    }
}
```

---

### `GassyCat`
**Name:** Gassy  
**Source:** `cat_enemies.gon`  

```
GassyCat {
    graphics {
        movieclip _CAT
        name "ENEMY_GASSY_NAME"
        custom_cat_data GassyCat
        alt_animations[[idle dopeyIdle]]

        tooltip "ENEMY_GASSY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 12
        shield 3
        base_mana_regen 999
        faction enemies
        initiative 10
        movement 5
    }

    abilities {
        move DefaultMove
        attack GasBlast
        
        spells [

        ]
    }

    passives {
        AbilityReaction attack
    }
    
    ai {
        brain GenericBrain
        decision_weights extra_careless
        move_weights stay_close
        random_orient true
    }
}
```

---

### `SharkyCat`
**Name:** Sharky  
**Source:** `cat_enemies.gon`  

```
SharkyCat {
    graphics {
        movieclip _CAT
        name "ENEMY_SHARKY_NAME"
        custom_cat_data SharkyCat
        alt_animations[[idle albinoIdle]]

        tooltip "ENEMY_SHARKY_DESC"
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat fish]
        type cat
        health 7
        shield 7
        base_mana_regen 999
        faction enemies
        initiative 10
        movement 3
        view_bleeding_characters_as_enemies true
    }

    abilities {
        move DefaultMove
        attack SharkDash
        
        spells [

        ]
    }

    passives {
        SharkySmellsBlood 1
        WaterWalk 1
    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights stay_close_always_move
    }
}
```

---

### `BoomerCat`
**Name:** Boomer  
**Source:** `cat_enemies.gon`  

```
BoomerCat {
    graphics {
        movieclip _CAT
        name "ENEMY_BOOMER_NAME"
        custom_cat_data BoomerCat
        alt_animations[[idle dopeyIdle]]

        tooltip "ENEMY_BOOMER_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 15

        base_mana_regen 999
        faction enemies
        initiative 10
        movement 3
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            BoomerCatExplode
        ]
    }

    passives {
        DeathRattle BoomerCatExplode
        AddMeleeKnockback 1
    }
    
    ai {
        brain GenericBrain
        consider_spells false
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `WaterKitten`
**Name:** Water Kitten  
**Source:** `cat_enemies.gon`  

```
WaterKitten {
    graphics {
        movieclip _CAT
        name "ENEMY_WATERKITTEN_NAME"
        custom_cat_data WaterKitten
        scale .8
        shadow_size .8
        spawnin_animation "digUp"
        alt_animations[[idle cuteIdle]]

        tooltip "ENEMY_WATERKITTEN_DESC"
    }

    equipment {
        neck Slime
        head Banana
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }

    properties {
        tag cat
        type cat
        health 5
        shield 1
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack BasicMelee
 
        spells [
            WaterTrailMove
        ]
    }

    passives {
        MoveWhenDamaged {
            weights stay_far_always_move
            move_ability WaterTrailMove
        }
        WaterWalk 1
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `AlbinoTomTom`
**Name:** Albino Tom Tom  
**Source:** `cat_enemies.gon`  

```
AlbinoTomTom {
    graphics {
        movieclip _CAT
        name "ENEMY_ALBINOTOMTOM_NAME"
        custom_cat_data AlbinoTomTom
        scale 1.1
        shadow_size 1.1
        alt_animations[[idle albinoIdle]]

        tooltip "ENEMY_ALBINOTOMTOM_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 17
        round_end_bonus_turns 1
        base_mana_regen 999
        faction enemies
    }

    abilities {
        move DefaultMove
        attack WideSwipe
        
        spells [

        ]
    }

    passives {
        AddMeleeKnockback 2
        /*AddStatusToBasicAttack {
            Fear 1
        }*/
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `SpiderCat`
**Name:** Spider Kitten  
**Source:** `cat_enemies.gon`  

```
SpiderCat {
    graphics {
        movieclip _CAT
        name "ENEMY_SPIDERKITTEN_NAME"
        custom_cat_data SpiderCat
        scale .8

        tooltip "ENEMY_SPIDERKITTEN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat bug]
        type cat

        health 20
        initial_health 10
        dispersed_bonus_turns 1

        base_mana_regen 999
        faction enemies
        movement 3
        initiative 16
    }

    abilities {
        move DefaultMove
        attack WebShot
        
        spells [
            SmallSpiderMelee
        ]
    }

    passives {
        StatusImmunity Webbed
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights keep_distance

        fallback_advances_pattern false
        stun_advances_pattern false

        pattern {
            do_priority [WebShot, SmallSpiderMelee]
            do_priority [SmallSpiderMelee, WebShot]
        }
    }
}
```

---

### `TallSpiderCat`
**Name:** Spider Cat  
**Source:** `cat_enemies.gon`  

```
TallSpiderCat {
    graphics {
        movieclip _CAT
        name "ENEMY_SPIDERCAT_NAME"
        custom_cat_data TallSpiderCat

        tooltip "ENEMY_SPIDERCAT_DESC"
        uifloaters_offset 1.5
    }

    stats {
        strength 7
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat bug]
        type cat

        health 28
        initial_health 14

        base_mana_regen 999
        faction enemies
        movement 6
    }

    abilities {
        move DefaultMove
        attack TallSpiderMelee
        
        spells [

        ]
    }

    passives {
        YOffset .35
        IgnoreTiles 1
        StatusImmunity Webbed
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Toadie`
**Name:** Toadie  
**Source:** `cat_enemies.gon`  

```
Toadie {
    graphics {
        movieclip _CAT
        name "ENEMY_TOADIE_NAME"
        custom_cat_data Toadie

        tooltip "ENEMY_TOADIE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 14

        base_mana_regen 999
        faction enemies
        initiative 10
        movement 4
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            Disguise
            MoveTwoCantrip
            FearMelee
        ]
    }

    passives {
        DisguisedTrapper FearMelee
    }
    
    ai {
        virtual_abilities {
            MoveAway {
                ability MoveTwoCantrip
                move_weights keep_distance_always_move
            }
        }

        brain PatternBrain
        decision_weights default
        move_weights keep_distance

        pattern {
            do_all [BasicMelee MoveAway Disguise]
        }
    }
}
```

---

### `Toadie_Hidden`
**Source:** `cat_enemies.gon`  

```
Toadie_Hidden {
    variant_of Toadie

    passives {
        Disguised 1

        SkipFirstRounds {
            stacks 2
            pop_chance 50%
        }
    }
}
```

---

### `ZombieCat`
**Name:** Zombie Cat  
**Source:** `cat_enemies.gon`  

```
ZombieCat {
    graphics {
        movieclip _CAT
        name "ENEMY_ZOMBIECAT_NAME"
        custom_cat_data ZombieCat
        spawnin_animation digUp
        alt_animations[[idle zombieIdle] [walk zombieWalk]]
        move_speed_sync_frames 40

        tooltip "ENEMY_ZOMBIECAT_DESC"
    }

    stats {
        strength 7
        dexterity 5
        constitution 9
        intelligence 1
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat zombie]
        type cat
        health 20

        dispersed_bonus_turns 1
        base_mana_regen 999
        faction enemies
        movement 2
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            ZombieFeast
        ]
    }

    passives {
        Undead 1
        SpawnThingOnDamage {
            object PoisonFood
            consider_all_layers true
        }
        StatusOnTookDamage {
            StrengthUp -1
            ConstitutionUp -1
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [ZombieFeast, attack]
        }

        decision_weights zombie
        move_weights zombie
    }
}
```

---

### `SkeletonCat`
**Name:** Skeleton Cat  
**Source:** `cat_enemies.gon`  

```
SkeletonCat {
    graphics {
        movieclip _CAT
        name "ENEMY_SKELETONCAT_NAME"
        custom_cat_data SkeletonCat

        alt_animations[[idle skeletonIdle]]

		
        tooltip "ENEMY_SKELETONCAT_DESC"
    }

    sound {
        alt_sounds [[SE_CatWalk SE_SkeletonCatWalk]]
    }

    stats {
        strength 9
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat skeleton]
        type cat
        health 0
        shield 1

        base_mana_regen 999
        faction enemies
        initiative 10
        movement 3
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        NoHealthOnlyShield 1
        Undead 1
        StatusImmunity [Poison, Bleed]

        TransformOnDeathImmediately {
            obj SkeletonCatCorpse
            first_turn keep_turns
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `SkeletonCatCorpse`
**Name:** Skeleton Cat  
**Source:** `cat_enemies.gon`  

```
SkeletonCatCorpse {
    graphics {
        movieclip _CAT
        name "ENEMY_SKELETONCAT_NAME"
        custom_cat_data SkeletonCat
        alt_animations [[idle dead] [weak dead] [hit skeletonCorpseHit] [deadhit skeletonCorpseHit] [stunned dead] [dying dead] [dead skeletonDead]]
        spawnin_animation skeletonDie

        tooltip "ENEMY_SKELETONCATBODY_DESC"
    }

    properties {
        tag [cat skeleton]
        type cat
        health 0
        shield 12

        faction enemies
        initiative 10
        corpse_health 0
        exclude_from_hallucinate true
    }

    abilities {
        move None
        attack None
    }

    passives {
        NoHealthOnlyShield 1
        Undead 1
        StatusImmunity [Poison, Bleed]
        CountAsCorpse 1

        TransformInXTurns {
            stacks 1
            object SkeletonCatRevived
            initiative keep_turns_end_turn
        }
    }
    ai {
        brain NoBrain
    }
}
```

---

### `SkeletonCatRevived`
**Source:** `cat_enemies.gon`  

```
SkeletonCatRevived {
    variant_of SkeletonCat
    graphics {
        spawnin_animation skeletonRevive
    }
    properties {
        exclude_from_hallucinate true
    }
}
```

---

### `TallSkeletonCat`
**Name:** Tall Skeleton Cat  
**Source:** `cat_enemies.gon`  

```
TallSkeletonCat {
    graphics {
        movieclip _CAT
        name "ENEMY_TALLSKELETONCAT_NAME"
        custom_cat_data TallSkeletonCat
        alt_animations[[idle skeletonBigIdle]]

        tooltip "ENEMY_TALLSKELETONCAT_DESC"
        uifloaters_offset 1.5
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat skeleton]
        type cat
        health 0
        shield 15

        base_mana_regen 999
        faction enemies
        initiative 10
        movement 3
        corpse_health 0
        act_points 2
    }

    abilities {
        move DefaultMove
        attack BadBone
        
        spells [
            BadBone_copy
            GoodBone
            GoodBone_copy
        ]
    }

    passives {
        YOffset .35
        Undead 1
        PrioritizeHitDifferentTargets 1
        NoHealthOnlyShield 1
        StatusImmunity [Poison, Bleed]

        TransformOnDeathImmediately {
            obj TallSkeletonCatCorpse
            first_turn keep_turns
        }
    }
    
    ai {
        brain PatternBrain
        pattern {
            do_priority_alternating [*BadBone, *GoodBone, BadBone_copy, GoodBone_copy, BadBone, GoodBone]
        }
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `TallSkeletonCatCorpse`
**Name:** Tall Skeleton Cat  
**Source:** `cat_enemies.gon`  

```
TallSkeletonCatCorpse {
    graphics {
        movieclip _CAT
        name "ENEMY_TALLSKELETONCAT_NAME"
        custom_cat_data TallSkeletonCat
        alt_animations [[idle dead] [weak dead] [hit skeletonCorpseHit] [deadhit skeletonCorpseHit] [stunned dead] [dying dead] [dead skeletonDead]]
        spawnin_animation skeletonDie

        tooltip "ENEMY_TALLSKELETONCATBODY_DESC"
    }

    properties {
        tag [cat skeleton]
        type cat
        health 0
        shield 1

        faction enemies
        initiative 10
        corpse_health 0
        exclude_from_hallucinate true
    }

    abilities {
        move None
        attack None
    }

    passives {
        NoHealthOnlyShield 1
        Undead 1
        StatusImmunity [Poison, Bleed]
        CountAsCorpse 1

        TransformInXTurns {
            stacks 1
            object TallSkeletonCatRevived
            initiative keep_turns_end_turn
        }
    }
    ai {
        brain NoBrain
    }
}
```

---

### `TallSkeletonCatRevived`
**Source:** `cat_enemies.gon`  

```
TallSkeletonCatRevived {
    variant_of TallSkeletonCat
    graphics {
        spawnin_animation revive
    }
    properties {
        exclude_from_hallucinate true
    }
}
```

---

### `WolfCat`
**Name:** Werecat  
**Source:** `cat_enemies.gon`  

```
WolfCat {
    graphics {
        movieclip _CAT
        name "ENEMY_WERECAT_NAME"
        custom_cat_data WolfCat
        scale 1
        spawnin_animation "howl"
        alt_animations[[idle werecatIdle]]

        tooltip "ENEMY_WERECAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 6
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat dog]
        type cat
        health 16
        base_mana_regen 999
        faction enemies

        act_points 2
        move_points 2
        movement 2
    }

    abilities {
        move DefaultMove
        attack WolfDash
        
        spells [
            WolfLeap
        ]
    }

    passives {
        PrioritizeHitDifferentTargets 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [WolfDash WolfLeap]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `GolemCat`
**Name:** Golem  
**Source:** `cat_enemies.gon`  

```
GolemCat {
    graphics {
        movieclip _CAT
        name "ENEMY_GOLEM_NAME"
        custom_cat_data GolemCat
        scale 1.1

        tooltip "ENEMY_GOLEM_DESC"
    }

    stats {
        strength 15
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat golem]
        type cat
        health 15

        base_mana_regen 999
        faction enemies
        initiative 10
        movement 2
        kill_required false
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        BlockAllDamage 1
        DieWhenOnlyGolemsLeft 1
        AddMeleeKnockback 2
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `ScorpionCat`
**Name:** Scorpion Cat  
**Source:** `cat_enemies.gon`  

```
ScorpionCat {
    graphics {
        movieclip _CAT
        name "ENEMY_SCORPIONCAT_NAME"
        custom_cat_data ScorpionCat
		
		tooltip "ENEMY_SCORPIONCAT_DESC"
    }

    sound {
        alt_sounds [[SE_CatWalk SE_ScorpionCatWalk]]
    }

    stats {
        strength 3
        dexterity 3
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat bug]
        type cat
        health 5
        shield 5

        base_mana_regen 999
        faction enemies
        initiative 10
        movement 2
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack ScorpionSting
        
        spells [
            ScorpionHold
        ]
    }

    passives {
        Brace 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }
        bonusturn_pattern {
            do ScorpionHold
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Mangy2`
**Name:** Mummified Mangy  
**Source:** `cat_enemies.gon`  

```
Mangy2 {
    graphics {
        movieclip _CAT
        name "ENEMY_MUMMIFIEDMANGY_NAME"
        custom_cat_data Mangy2
		
		tooltip "ENEMY_MUMMIFIEDMANGY_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat zombie]
        type cat
        health 7
        faction enemies
        base_mana_regen 999
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack PoisonShot
        
        spells [

        ]
    }

    passives {
        Undead 1
        SpawnThingOnDamage {
            object Maggot
            good false 
            spawn_on_death_hit false
        }
        TransformOnDeath Carcus
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `GunCat`
**Name:** Bounty Hunter  
**Source:** `cat_enemies.gon`  

```
GunCat {
    graphics {
        movieclip _CAT
        name "ENEMY_BOUNTYHUNTER_NAME"
        custom_cat_data GunCat
		
		tooltip "ENEMY_BOUNTYHUNTER_DESC"
    }
    
    equipment {
        weapon GunslingerPistol
        neck Poncho
        face WesternHat
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 9
        faction enemies
        base_mana_regen 999
        movement 2
    }

    abilities {
        move DefaultMove
        attack GuncatShoot
        
        spells [

        ]
    }

    passives {
        WeaponsDontLoseDurability 1
        PrioritizeFarAwayTargets 10
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_always_move
        consider_spells false
    }
}
```

---

### `HornyCat`
**Name:** Horny Cat  
**Source:** `cat_enemies.gon`  

```
HornyCat {
    graphics {
        movieclip _CAT
        name "ENEMY_HORNYCAT_NAME"
        custom_cat_data HornyCat
        alt_animations[[idle horntoadIdle]]
		tooltip "ENEMY_HORNYCAT_DESC"
    }
    

    stats {
        strength 4
        dexterity 3
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat animal]
        type cat
        health 7
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack HornyToadShot
        
        spells [

        ]
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Infested`
**Name:** Infested Kitten  
**Source:** `cat_enemies.gon`  

```
Infested {
    graphics {
        movieclip _CAT
        name "ENEMY_INFESTEDKITTEN_NAME"
        custom_cat_data Infested
        scale .8
        shadow_size .8

        tooltip "ENEMY_INFESTEDKITTEN_DESC"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 7
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            
        ]
    }

    passives {
        MoveWhenDamaged {
            weights stay_far_always_move
        }
        AddStatusToBasicAttack {
            Possessed 1
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `RockHead`
**Name:** Rock Head  
**Source:** `cat_enemies.gon`  

```
RockHead {
    graphics {
        movieclip _CAT
        name "ENEMY_ROCKHEAD_NAME"
        custom_cat_data RockHead
        scale 1.1
        shadow_size 1.1
		
		tooltip "ENEMY_ROCKHEAD_DESC" 
    }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat rock]
        type cat
        health 1
        shield 10
        base_mana_regen 999
        dispersed_bonus_turns 1
        faction enemies
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack CatSpin
        
        spells [
            SmallTrampleDash
        ]
    }

    passives {
        SpawnThingOnDeath Boulder
        TransformOnDeathImmediately NoHead
        FaceShield 0

        RandomizeAIWeightsEachTurn [
            {
                decision_weights blind
                move_weights chubs_and_nubs_blind
            }

            {
                decision_weights blind
                move_weights stay_close_always_move
            }
        ]
    }
    
    ai {
        brain PatternBrain
        decision_weights blind
        move_weights chubs_and_nubs_blind
        auto_orient false

        pattern {
            do attack
            do SmallTrampleDash
        }
    }
}
```

---

### `NoHead`
**Name:** Headless  
**Source:** `cat_enemies.gon`  

```
NoHead {
    graphics {
        movieclip _CAT
        name "ENEMY_HEADLESS_NAME"
        custom_cat_data NoHead
        scale 1.1
        shadow_size 1.1
		
		tooltip "ENEMY_HEADLESS_DESC"
    }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 7
        base_mana_regen 999
        faction enemies
        initiative 10
    }

    abilities {
        move DefaultMove
        attack CatSpin
        
        spells [
            CatGoop
        ]
    }

    passives {
        ImmediateAbilityReaction CatGoop
        RandomizeAIWeightsEachTurn [
            {
                decision_weights blind
                move_weights chubs_and_nubs_blind
            }

            {
                decision_weights blind
                move_weights stay_close_always_move
            }
        ]
    }
    
    ai {
        brain PatternBrain
        decision_weights blind
        move_weights chubs_and_nubs_blind
        auto_orient false

        pattern {
            do attack
        }
    }
}
```

---

### `AtomicKitten`
**Name:** Atomic Kitten  
**Source:** `cat_enemies.gon`  

```
AtomicKitten {
    graphics {
        movieclip _CAT
        name "ENEMY_ATOMICKITTEN_NAME"
        custom_cat_data AtomicKitten
        alt_animations[[idle atomicIdle]]

        tooltip "ENEMY_ATOMICKITTEN_DESC"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }

    equipment {
        face AtomicMark
    }
    
    properties {
        tag cat
        type cat
        health 1
        divine_shield 2
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move Teleport
        attack AtomicBurst
        
        spells [
            
        ]
    }

    passives {
        MoveWhenDamaged {
            weights chaotic
        }
        DeathRattle BoomerCatExplode

        CharacterLightSource {
            color [.3, .7, 1]
            size 2
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do *AtomicBurst
        }

        decision_weights always_cast
        move_weights stay_close
    }
}
```

---

### `RoboTom`
**Name:** Robo-Cat  
**Source:** `cat_enemies.gon`  

```
RoboTom {
    graphics {
        movieclip _CAT
        name "ENEMY_ROBOCAT_NAME"
        custom_cat_data RoboTom
        scale 1.1
        shadow_size 1.1
		alt_animations[[walk robotWalk]]

		tooltip "ENEMY_ROBOCAT_DESC"
    }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat robot]
        type cat
        health 1
		shield 11
        dispersed_bonus_turns 1
        base_mana_regen 999
        faction enemies
        initiative 10
    }

    abilities {
        move DefaultMove
        attack WideSwipe
        
        spells [

        ]
    }

    passives {
        Brace 3
        AddMeleeKnockback 10
        Robot 1
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `CatCultist`
**Name:** Cat Cultist  
**Source:** `cat_enemies.gon`  

```
CatCultist {
    graphics {
        movieclip _CAT
        name "ENEMY_CATCULTIST_NAME"
        custom_cat_data CatCultist
        scale 1
        shadow_size 1
        alt_animations[[idle cultistIdle]]

        tooltip "ENEMY_CATCULTIST_DESC"
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 11
        faction enemies
        base_mana_regen 999

        act_points 0
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            CultistCut
        ]
    }

    passives {
        StatusOnTookDamageFromAbility {
            ExtraBasicAttacks_Status 1
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [*CultistCut, attack]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `DemonHooker`
**Name:** Chain Demon  
**Source:** `cat_enemies.gon`  

```
DemonHooker {
    graphics {
        movieclip _CAT
        name "ENEMY_DEMONHOOKER_NAME"
        custom_cat_data DemonHooker
        scale 1.2
        shadow_size 1

        tooltip "ENEMY_DEMONHOOKER_DESC"
    }

    equipment {
        weapon ButcherHook
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat demon]
        type cat
        health 13
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack DH_Attack
        
        spells [
            DH_MeatHook
        ]
    }

    passives {
        ElementImmune Fire
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [DH_MeatHook *attack attack]
        }

        decision_weights default
        move_weights prefer_lava_always_move
    }
}
```

---

### `Belcher`
**Name:** Belcher  
**Source:** `cat_enemies.gon`  

```
Belcher {
    graphics {
        movieclip _CAT
        name "ENEMY_BELCHER_NAME"
        custom_cat_data Belcher
        scale 1
        shadow_size 1

        tooltip "ENEMY_BELCHER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat demon]
        type cat
        health 12
        movement 2
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack BelcherLavashot
        
        spells [
            
        ]
    }

    passives {
        ElementImmune Fire
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `TumorCat`
**Name:** Tumor Cat  
**Source:** `cat_enemies.gon`  

```
TumorCat {
    graphics {
        movieclip _CAT
        name "ENEMY_TUMORCAT_NAME"
        custom_cat_data CoreFreak
        scale 1
        shadow_size 1

        tooltip "ENEMY_TUMORCAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat tumor]
        type cat
        health 11
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack TC_Attack
        
        spells [
            TC_DashReaction
        ]
    }

    passives {
        AbilityReaction TC_DashReaction
        Brace 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do *attack
        }

        decision_weights default
        move_weights semi_blind
    }
}
```

---

### `Rover`
**Name:** Rover  
**Source:** `cat_enemies.gon`  

```
Rover {
    graphics {
        movieclip _CAT
        name "ENEMY_ROVER_NAME"
        custom_cat_data Rover
        scale 1
        shadow_size 1
        alt_animations[[walk driveWalk]]

        tooltip "ENEMY_ROVER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [robot cat]
        type cat
        health 6
        shield 8
        movement 2
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack RoverDash
        
        spells [
            
        ]
    }

    passives {
        Brace 2
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Astro`
**Name:** Astronaut  
**Source:** `cat_enemies.gon`  

```
Astro {
    graphics {
        movieclip _CAT
        name "ENEMY_ASTRONAUT_NAME"
        custom_cat_data Astro
        scale 1
        shadow_size 1

        tooltip "ENEMY_ASTRONAUT_DESC"
    }

    equipment {
        weapon AstroTaser
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }

    sound {   
        alt_sounds [[SE_CatSwishJump SE_CE_Astro_Jump]]  
    }

    
    properties {
        tag cat
        type cat
        health 8
        shield 5
        movement 1 
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move BasicJump
        attack BasicMelee
        
        spells [
            
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        pattern {
            do weapon
        }
        fallback {
            do attack
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Drcat`
**Name:** Dr. Cat  
**Source:** `cat_enemies.gon`  

```
Drcat {
    graphics {
        movieclip _CAT
        name "ENEMY_DRCAT_NAME"
        custom_cat_data Drcat
        scale 1
        shadow_size 1

        tooltip "ENEMY_DRCAT_DESC"
    }

    equipment {
        weapon OddRemote_Enemy
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 10
        faction enemies
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        pattern {
            do weapon
        }
        fallback {
            do attack
        }

        decision_weights always_cast
        move_weights keep_distance_always_move
    }
}
```

---

### `Mangy3`
**Name:** Infested  
**Source:** `cat_enemies.gon`  

```
Mangy3 {
    graphics {
        movieclip _CAT
        name "ENEMY_INFESTED_NAME"
        custom_cat_data Mangy3
        scale 1
        shadow_size 1

        tooltip "ENEMY_INFESTED_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 10
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack ParasiteShot
        
        spells [

        ]
    }

    passives {
        SpawnThingOnDeath Gamete
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Needlecat`
**Name:** Spun Cat  
**Source:** `cat_enemies.gon`  

```
Needlecat {
    graphics {
        movieclip _CAT
        name "ENEMY_SPUNCAT_NAME"
        custom_cat_data Needlecat
        scale 1
        shadow_size 1

        tooltip "ENEMY_SPUNCAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 10
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            
        ]
    }

    passives {
        FormChanger { 
            Colorless{}
            Fighter{}
            Hunter{}
            Mage{}
            Medic{}
            Tank{}
            Thief{}
            Butcher{}
            Druid{}
            Necromancer{}
            Psychic{}
            Monk{}
            Tinkerer{}
        }

        RandomPassivePool {
            PassiveGroup {
                ReplaceBasicAttack BasicMelee
                CatPartsTransform {
                    palette Fighter
                }
                FormChange Fighter
            }
            PassiveGroup {
                ReplaceBasicAttack BasicRanged
                CatPartsTransform {
                    palette Hunter
                }
                FormChange Hunter
            }
            PassiveGroup {
                ReplaceBasicAttack BasicMagicShortRanged
                CatPartsTransform {
                    palette Mage
                }
                FormChange Mage
            }
            PassiveGroup {
                ReplaceBasicAttack BasicMedicMelee
                CatPartsTransform {
                    palette Medic
                }
                FormChange Medic
                StatusCarefulness 1 
            }
            PassiveGroup {
                ReplaceBasicAttack BasicTankMelee
                CatPartsTransform {
                    palette Tank
                }
                FormChange Tank
            }
            PassiveGroup {
                ReplaceBasicAttack BasicStraightShot
                CatPartsTransform {
                    palette Thief
                }
                FormChange Thief
            }
            PassiveGroup {
                ReplaceBasicAttack BasicButcherMelee
                CatPartsTransform {
                    palette Butcher
                }
                FormChange Butcher
            }
            PassiveGroup {
                ReplaceBasicAttack BasicDruidAbility
                CatPartsTransform {
                    palette Druid
                }
                FormChange Druid
                StatusCarefulness 1 
                SelfStatusCarefulness 1
            }
            PassiveGroup {
                ReplaceBasicAttack BasicNecroRanged
                CatPartsTransform {
                    palette Necromancer
                }
                FormChange Necromancer
            }
            PassiveGroup {
                ReplaceBasicAttack BasicPsychicPull
                CatPartsTransform {
                    palette Psychic
                }
                FormChange Psychic
            }
            PassiveGroup {
                ReplaceBasicAttack BasicMonkMelee
                CatPartsTransform {
                    palette Monk
                }
                FormChange Monk
                ExtraBasicAttacks 1
            }
            PassiveGroup {
                TinkererBasicAttackSwitching {
                    craft_ability TinkererCraft
                    throw_ability TinkererThrow
                }
                CatPartsTransform {
                    palette Tinkerer
                }
                FormChange Tinkerer
                SelfStatusCarefulness 1 
            }
        }

        RandomPassivePool {
            AddStatusToBasicAttack {
                Burn 1
            }
            AddStatusToBasicAttack {
                Poison 1
            }
            AddStatusToBasicAttack {
                Bleed 1
            }
            AddStatusToBasicAttack {
                RandomStatUp -1
            }
            AddStatusToBasicAttack {
                Bruise 1
            }
            AddStatusToBasicAttack {
                Rot 1
            }
            AddStatusToBasicAttack {
                Fear 1
            }
            AddStatusToBasicAttack {
                Slow 1
            }
            AddStatusToBasicAttack {
                DamageUp -1
            }
            AddStatusToBasicAttack {
                Weakness 1
            }
        }
    }
    
    ai {
        brain GenericBrain

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Stacy2p0`
**Name:** Stacy #{stacy_number}  
**Source:** `cat_enemies.gon`  

```
Stacy2p0 {
    graphics {
        movieclip _CAT
        name "ENEMY_STACYNO_NAME"
        custom_cat_data Stacy2p0
        scale .85
        shadow_size .85

        tooltip "ENEMY_STACYNO_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 11
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack StacyCharm
        
        spells [
            StacyHeal
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [StacyCharm StacyHeal]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Raptor`
**Name:** Raptor  
**Source:** `cat_enemies.gon`  

```
Raptor {
    graphics {
        movieclip _CAT
        name "ENEMY_RAPTOR_NAME"
        custom_cat_data Raptor
        scale 1
        uifloaters_offset 1.5
        alt_animations[[idle raptorIdle] [walk raptorWalk]]

        tooltip "ENEMY_RAPTOR_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat dinosaur]
        type cat
        health 12
        base_mana_regen 999
        faction enemies
        initiative 10
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack FurySwipes_Enemy
        
        spells [

        ]
    }

    passives {
        YOffset .35
        PackHunting 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [move attack]
        }

        decision_weights default
        move_weights towards_aggro_stay_close
    }
}
```

---

### `RaptorBaby`
**Name:** Raptor Kitten  
**Source:** `cat_enemies.gon`  

```
RaptorBaby {
    graphics {
        movieclip _CAT
        name "ENEMY_RAPTORKITTEN_NAME"
        tooltip ENEMY_RAPTORKITTEN_DESC
        custom_cat_data RaptorBaby
        scale .85
        shadow_size .85
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 8
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat dinosaur]
        type cat
        health 6
        faction enemies
        movement 3
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack RaptorBabyBite
        
        spells [
            DoubleDistanceMove
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveAway {
                ability DoubleDistanceMove
                move_weights stay_far
            }
            MoveTowards {
                ability move
                move_for_ability attack
                move_weights stay_close
            }
        }

        pattern {
            do_all [MoveTowards attack MoveAway]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Ankylosaurus`
**Name:** Ankylosaurus  
**Source:** `cat_enemies.gon`  

```
Ankylosaurus {
    graphics {
        movieclip _CAT
        name "ENEMY_ANKYLOSAURUS_NAME"
        tooltip ENEMY_ANKYLOSAURUS_DESC
        custom_cat_data Ankylosaurus
        scale 1.1
        shadow_size 1.1
    }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat dinosaur]
        type cat
        health 16
        base_mana_regen 999
        faction enemies
    }

    abilities {
        move DefaultMove
        attack AnkyloSwipe
        
        spells [
            AnkyloSpin
        ]
    }

    passives {
        Brace 2
        Thorns 2
        AbilityReaction AnkyloSpin
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [attack move]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Maelestes`
**Name:** Maelestes  
**Source:** `cat_enemies.gon`  

```
Maelestes {
    graphics {
        movieclip _CAT
        name "ENEMY_MAELESTES_NAME"
        custom_cat_data Maelestes
        scale .7
        shadow_size .7

        tooltip "ENEMY_MAELESTES_DESC"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 10
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat rat]
        type cat
        health 6
        faction enemies
        base_mana_regen 999
        can_collect_coins true
        can_eat_food true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            MaelestesPickup
            MaelestesSteal
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [MaelestesPickup MaelestesSteal weapon trinket attack]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Parasaurolophus`
**Name:** Parasaurolophus  
**Source:** `cat_enemies.gon`  

```
Parasaurolophus {
    graphics {
        movieclip _CAT
        name "ENEMY_PARASAUROLOPHUS_NAME"
        custom_cat_data Parasaurolophus
        scale 1.1
        uifloaters_offset 1.5

        tooltip "ENEMY_PARASAUROLOPHUS_DESC"
    }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat dinosaur]
        type cat
        health 18
        base_mana_regen 999
        faction enemies
        initiative 10
        dispersed_bonus_turns 1
        movement 1
    }

    abilities {
        move DefaultMove
        attack Parasaurolophus_Push
        
        spells [
            Parasaurolophus_Throw
        ]
    }

    passives {
        YOffset .35
        WaterWalk 1
        FreePathfindElement Water
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [*Parasaurolophus_Push Parasaurolophus_Push Parasaurolophus_Throw]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Yeticat`
**Name:** Yeti Cat  
**Source:** `cat_enemies.gon`  

```
Yeticat {
    graphics {
        movieclip _CAT
        name "ENEMY_YETICAT_NAME"
        custom_cat_data Yeticat
        scale 1.1
        shadow_size 1.1
		
		tooltip "ENEMY_YETICAT_DESC"
    }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat humanoid]
        type cat
        health 15
        base_mana_regen 999
        faction enemies
        movement 2
    }

    abilities {
        move DefaultMove
        attack YeticatSnowball
        
        spells [

        ]
    }

    passives {
        CounterAttack YeticatSnowball_Counter
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `SabertoothCat`
**Name:** Sabertooth Cat  
**Source:** `cat_enemies.gon`  

```
SabertoothCat {
    graphics {
        movieclip _CAT
        name "ENEMY_SABERTOOTHCAT_NAME"
        custom_cat_data SabertoothCat
        scale 1
        alt_animations[[idle werecatIdle]]
		
		tooltip "ENEMY_SABERTOOTHCAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 17
        base_mana_regen 999
        faction sabertooths
    }

    abilities {
        move DefaultMove
        attack SabertoothCatPounce
        
        spells [
            SabertoothCatTransformSwipe
            SabertoothCatDoubleSwipe
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*SabertoothCatDoubleSwipe /*SabertoothCatTransformSwipe*/ attack SabertoothCatTransformSwipe attack]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `SabertoothCub`
**Name:** Sabertooth Kitten  
**Source:** `cat_enemies.gon`  

```
SabertoothCub {
    graphics {
        movieclip _CAT
        name "ENEMY_SABERTOOTHKITTEN_NAME"
        custom_cat_data SabertoothCub
        scale .8
        alt_animations[[idle werecatIdle]]
		tooltip "ENEMY_SABERTOOTHKITTEN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 10
        dispersed_bonus_turns 1
        base_mana_regen 999
        faction sabertooths
    }

    abilities {
        move DefaultMove
        attack SabertoothCubDoubleSwipe
        
        spells [
            SabertoothCatTransformSwipe
            SabertoothCubLick
        ]
    }

    passives {
        MoveWhenDamaged {
            weights stay_far_always_move
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [/*SabertoothCatTransformSwipe*/ SabertoothCubLick attack]
        }

        decision_weights default
        move_weights stay_near_allies
    }
}
```

---

### `MammothBaby`
**Name:** Mammoth Kitten  
**Source:** `cat_enemies.gon`  

```
MammothBaby {
    graphics {
        movieclip _CAT
        name "ENEMY_MAMMOTHKITTEN_NAME"
        custom_cat_data MammothBaby
        scale 1.1
        shadow_size 1.1
		tooltip "ENEMY_MAMMOTHKITTEN_DESC"
    }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat animal]
        type cat
        health 25
        base_mana_regen 999
        faction mammoths
        corpse_health 3
    }

    abilities {
        move DefaultMove
        attack MammothBabyThrow
        
        spells [
            MammothBabyStomp
        ]
    }

    passives {
        SpawnOnDeath BiggestFood
        Trample 3
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*MammothBabyStomp MammothBabyThrow]
        }

        decision_weights semi_simple
        move_weights stay_close
    }
}
```

---

### `Skinned`
**Name:** Skinned  
**Source:** `cat_enemies.gon`  

```
Skinned {
    graphics {
        movieclip _CAT
        name "ENEMY_SKINNED_NAME"
        custom_cat_data Skinned
        scale 1
        shadow_size 1
        alt_animations[[idle skinnedIdle]]

        tooltip "ENEMY_SKINNED_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 30
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack SkinnedTripleDash
        
        spells [
            
        ]
    }

    passives {
        StatusOnTookDamageFromAbility {
            Bleed 1
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `StemCat`
**Name:** Stem Cat  
**Source:** `cat_enemies.gon`  

```
StemCat {
    graphics {
        movieclip _CAT
        name "ENEMY_STEMCAT_NAME"
        custom_cat_data StemCat
        scale 1
        shadow_size 1

        tooltip "ENEMY_STEMCAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 13
        faction enemies
        base_mana_regen 999
        movement 3
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            
        ]
    }

    passives {
        HealthRegenUp 2
        SpawnThingOnDamage {
            object Clot
            good false 
            spawn_on_death_hit false
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `StemCat_HalfHealth`
**Source:** `cat_enemies.gon`  

```
StemCat_HalfHealth {
    variant_of StemCat

    properties {
        initial_health 4
    }
}
```

---

### `FutureBot`
**Name:** Katzebot  
**Source:** `cat_enemies.gon`  

```
FutureBot {
    graphics {
        movieclip _CAT
        name "ENEMY_KATZEBOT_NAME"
        custom_cat_data FutureBot
        scale .9
        shadow_size .9

        tooltip "ENEMY_KATZEBOT_DESC"
    }

    sound { alt_sounds [[SE_CatWalk SE_FuturebotWalk]]}

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 6
        shield 12
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack FutureBotPunch
        
        spells [
            FutureBotPunchAggro
            FutureBotSuplex
        ]
    }

    passives {
        Brace 2
        AggroTargetIsLowestHealthEnemyTillItDies 1
        Robot 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [FutureBotPunchAggro *FutureBotSuplex move FutureBotSuplex]
        }

        decision_weights default
        move_weights towards_aggro_stay_close
    }
}
```

---

### `FatCat`
**Name:** Übercat  
**Source:** `cat_enemies.gon`  

```
FatCat {
    graphics {
        movieclip _CAT
        name "ENEMY_FATCAT_NAME"
        custom_cat_data FatCat
        scale 1
        shadow_size 1

        tooltip "ENEMY_FATCAT_DESC"
        move_speed_multiplier .66
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat blob]
        type cat
        health 18
        faction enemies
        base_mana_regen 999
        can_eat_food true
        movement 2
    }

    abilities {
        move DefaultMove
        attack FatCatBellyFlop
        
        spells [
            
        ]
    }

    passives {
        YOffset -.18

        Trample 3
        ReflectProjectiles {
            self_damage 2
        }
        UncappedHP 1
        TagGreed food
        MeleeRevengeDamage {
            type status
            damage 0
            knockback 2
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `CancerCat`
**Name:** Cancer Cat  
**Source:** `cat_enemies.gon`  

```
CancerCat {
    graphics {
        movieclip _CAT
        name "ENEMY_CANCERCAT_NAME"
        custom_cat_data CancerCat
        scale 1
        shadow_size 1

        tooltip "ENEMY_CANCERCAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat skeleton tumor]
        type cat
        health 8
        shield 10
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack CancerMelee
        
        spells [
            CancerExplode
        ]
    }

    passives {
        Brace 2

        StatusAfterXTurns {
            stacks 3
            ForceUseAbility CancerExplode
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `CollectiveCat`
**Name:** The Collective  
**Source:** `cat_enemies.gon`  

```
CollectiveCat {
    graphics {
        movieclip _CAT
        name "ENEMY_COLLECTIVE_NAME"
        custom_cat_data CollectiveCat
        scale 1
        shadow_size 1

        tooltip "ENEMY_COLLECTIVE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        hidden_tag collective
        type cat
        health 19
        faction enemies
    }

    abilities {
        move DefaultMove
        attack CollectiveSpin
        
        spells [
            CollectiveCounter
        ]
    }

    passives {
        CounterAttack CollectiveCounter
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `ShadeCat`
**Name:** Shade Cat  
**Source:** `cat_enemies.gon`  

```
ShadeCat {
    graphics {
        movieclip _CAT
        name "ENEMY_SHADECAT_NAME"
        custom_cat_data ShadeCat
        scale 1
        shadow_size 1

        tooltip "ENEMY_SHADECAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat demon]
        type cat
        health 20
        faction enemies
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack SCAttack
        
        spells [
            SCSneakUp
        ]
    }

    passives {
        AbilityReaction SCSneakUp
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `PoopCat`
**Name:** Poop Cat  
**Source:** `cat_enemies.gon`  

```
PoopCat {
    graphics {
        movieclip _CAT
        name "ENEMY_POOPCAT_NAME"
        custom_cat_data PoopCat
        scale 1.2
        shadow_size 1.2

        tooltip "ENEMY_POOPCAT_DESC"
    }

    sound {
        alt_sounds [[SE_CatWalk SE_PoopCatWalk]]
    }
    

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat poop]
        type cat
        health 25
        base_mana_regen 999
        faction enemies
		dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack PoopCatMelee
        
        spells [

        ]
    }

    passives {
        PoisonThorns 3
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `JackCat`
**Name:** Jack  
**Source:** `cat_enemies.gon`  

```
JackCat {
    graphics {
        movieclip _CAT
        name "ENEMY_JACKCAT_NAME"
        custom_cat_data JackCat
        scale 1
        shadow_size 1

        tooltip "ENEMY_JACKCAT_DESC"
    }
    

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat humanoid]
        type cat
        health 16
        base_mana_regen 999
        faction enemies
    }

    abilities {
        move DefaultMove
        attack JackAttack
        
        spells [
            JackShield
        ]
    }

    passives {
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [JackShield attack]
        }

        decision_weights default
        move_weights stay_near_allies
    }
}
```

---

### `ChaosStacy`
**Name:** Chaos Stacy  
**Source:** `cat_enemies.gon`  

```
ChaosStacy {
    graphics {
        movieclip _CAT
        name "ENEMY_CHAOSSTACY_NAME"
        custom_cat_data StacyX

        tooltip "ENEMY_CHAOSSTACY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 26
        faction enemies
        base_mana_regen 999
        dispersed_bonus_turns 1
        movement 4
    }

    abilities {
        move DefaultMove
        attack ChaosStacyAttack
        
        spells [

        ]
    }

    passives {
        ReflectProjectiles 1

        MeleeRevengeDamage {
            type status
            damage 0
            knockback 2
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [attack]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `AngelicCat`
**Name:** Angelic Cat  
**Source:** `cat_enemies.gon`  

```
AngelicCat {
    graphics {
        movieclip _CAT
        name "ENEMY_ANGELICCAT_NAME"
        custom_cat_data AngelicCat

        tooltip "ENEMY_ANGELICCAT_DESC"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat angel]
        type cat
        health 30
        divine_shield 1
        faction enemies
        movement 5
    }

    abilities {
        move BasicJump
        attack AngelcatWind
        
        spells [

        ]
    }

    passives {
        Angel 1
        PrioritizeFarAwayTargets 1
        StatusEachTurnEnd {
            DivineShield 1
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_move_far
    }
}
```

---

### `TrailerCat`
**Name:** ENEMY_TRAILERCAT1_NAME  
**Source:** `cat_enemies.gon`  

```
TrailerCat {
    graphics {
        movieclip _CAT
        name "ENEMY_TRAILERCAT1_NAME"
        custom_cat_data TrailerCat

        tooltip "ENEMY_TRAILERCAT1_DESC"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat angel]
        type cat
        health 30
        divine_shield 1
        faction enemies
        movement 5
    }

    abilities {
        move BasicJump
        attack AngelcatWind
        
        spells [

        ]
    }

    passives {
        Angel 1
        PrioritizeFarAwayTargets 1
        StatusEachTurnEnd {
            DivineShield 1
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_move_far
    }
}
```

---

### `TrailerCat2`
**Name:** ENEMY_TRAILERCAT2_NAME  
**Source:** `cat_enemies.gon`  

```
TrailerCat2 {
    graphics {
        movieclip _CAT
        name "ENEMY_TRAILERCAT2_NAME"
        custom_cat_data TrailerCat2

        tooltip "ENEMY_TRAILERCAT2_DESC"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat angel]
        type cat
        health 30
        divine_shield 1
        faction enemies
        movement 5
    }

    abilities {
        move BasicJump
        attack AngelcatWind
        
        spells [

        ]
    }

    passives {
        Angel 1
        PrioritizeFarAwayTargets 1
        StatusEachTurnEnd {
            DivineShield 1
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_move_far
    }
}
```

---

### `TrailerCat3`
**Name:** ENEMY_TRAILERCAT3_NAME  
**Source:** `cat_enemies.gon`  

```
TrailerCat3 {
    graphics {
        movieclip _CAT
        name "ENEMY_TRAILERCAT3_NAME"
        custom_cat_data TrailerCat3

        tooltip "ENEMY_TRAILERCAT3_DESC"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat angel]
        type cat
        health 30
        divine_shield 1
        faction enemies
        movement 5
    }

    abilities {
        move BasicJump
        attack AngelcatWind
        
        spells [

        ]
    }

    passives {
        Angel 1
        PrioritizeFarAwayTargets 1
        StatusEachTurnEnd {
            DivineShield 1
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_move_far
    }
}
```

---

### `TrailerCat4`
**Name:** ENEMY_TRAILERCAT4_NAME  
**Source:** `cat_enemies.gon`  

```
TrailerCat4 {
    graphics {
        movieclip _CAT
        name "ENEMY_TRAILERCAT4_NAME"
        custom_cat_data TrailerCat4

        tooltip "ENEMY_TRAILERCAT4_DESC"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat angel]
        type cat
        health 30
        divine_shield 1
        faction enemies
        movement 5
    }

    abilities {
        move BasicJump
        attack AngelcatWind
        
        spells [

        ]
    }

    passives {
        Angel 1
        PrioritizeFarAwayTargets 1
        StatusEachTurnEnd {
            DivineShield 1
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_move_far
    }
}
```

---

### `TrailerCat5`
**Name:** ENEMY_TRAILERCAT5_NAME  
**Source:** `cat_enemies.gon`  

```
TrailerCat5 {
    graphics {
        movieclip _CAT
        name "ENEMY_TRAILERCAT5_NAME"
        custom_cat_data TrailerCat5

        tooltip "ENEMY_TRAILERCAT5_DESC"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat angel]
        type cat
        health 30
        divine_shield 1
        faction enemies
        movement 5
    }

    abilities {
        move BasicJump
        attack AngelcatWind
        
        spells [

        ]
    }

    passives {
        Angel 1
        PrioritizeFarAwayTargets 1
        StatusEachTurnEnd {
            DivineShield 1
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_move_far
    }
}
```

---

### `LoanShark`
**Name:** Loan Shark  
**Source:** `cat_enemies.gon`  

```
LoanShark {
    graphics {
        movieclip _CAT
        name "ENEMY_LOANSHARK_NAME"
        custom_cat_data LoanShark
        alt_animations[[idle albinoIdle]]

        tooltip "ENEMY_LOANSHARK_DESC"
    }
	
    equipment {
        head LoansharksFedora
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat fish]
        type cat
        health 37
        shield 37
        base_mana_regen 999
        faction enemies
        initiative 100
        movement 4
        view_bleeding_characters_as_enemies true
    }

    abilities {
        move DefaultMove
        attack SharkDash
        
        spells [

        ]
    }

    passives {
        SharkySmellsBlood 1
        WaterWalk 1
    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights stay_close_always_move
    }
}
```

---

### `TankCat`
**Name:** Maisie  
**Source:** `cat_minibosses.gon`  

```
TankCat {
    graphics {
        movieclip _CAT
        name "ENEMY_MAISIE_NAME"
        custom_cat_data TankCat

        tooltip "ENEMY_MAISIE_DESC"
    }

    equipment {
        face MetalPlate
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        movement 5
        corpse_health 3
        dispersed_bonus_turns 1
        dispersed_bonus_turns_consider_initiative false
        
        health 90
    }

    abilities {
        move DefaultMove
        attack BasicTankMelee
        
        spells [
            SwapPositions_TankCat
            LickyLicky
        ]
    }

    passives {
		ProtectTargetedAllies {
            ability SwapPositions_TankCat
            target_filter Kitten
        }

        MamaCatAnimations 1

        RunWhenKittensDead 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [LickyLicky attack]
        }

        decision_weights default_no_revive
        move_weights keep_distance_always_move
    }
}
```

---

### `MageCat`
**Name:** Lucy  
**Source:** `cat_minibosses.gon`  

```
MageCat {
    graphics {
        movieclip _CAT
        name "ENEMY_LUCY_NAME"
        custom_cat_data MageCat

        tooltip "ENEMY_LUCY_DESC"
    }

    equipment {
        neck MageCollar
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        initiative -999
        evenly_dispersed_bonus_turns 1
        
        /*mana_regen -2 
        mana 100
        initial_mana 100
        mana_matters true*/
        
        health 75
    }

    abilities {
        move DefaultMove
        attack BasicMagicShortRanged
        
        spells [
            MCBlizzard
            MCFlamethrower
            MCStorm
        ]
    }

    passives {
       
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_strict [MCBlizzard]
            do_strict [MCFlamethrower]
            do_strict [MCStorm]
        }

        decision_weights always_cast
        move_weights keep_distance_always_move
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `HunterCat`
**Name:** Fenrir  
**Source:** `cat_minibosses.gon`  

```
HunterCat {
    graphics {
        movieclip _CAT
        name "ENEMY_FENRIR_NAME"
        custom_cat_data HunterCat

        tooltip "ENEMY_FENRIR_DESC"
    }

    equipment {
        face HuntersPatch
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 4
        
        mana_regen 999
        mana 100
        
        health 60
    }

    abilities {
        move HunterMinibossMove
        attack BasicRanged_Hunter
        
        spells [
            BearTrap_Enemy
            Shove
        ]
    }

    passives {
        CounterAttack Shove
       
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do attack
        }

        bonusturn_pattern {
            do BearTrap_Enemy
        }

        decision_weights default
        move_weights prefer_tall_grass_always_move
    }
}
```

---

### `ThiefCat`
**Name:** Dack  
**Source:** `cat_minibosses.gon`  

```
ThiefCat {
    graphics {
        movieclip _CAT
        name "ENEMY_DACK_NAME"
        custom_cat_data ThiefCat

        tooltip "ENEMY_DACK_DESC"
    }

    equipment {
        head CoinBag
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 3
        
        mana_regen 999
        mana 100
        
        health 60
        can_collect_coins true
        held_coins 5
        movement 3
    }

    abilities {
        move DefaultMove
        attack THC_KnockCoinsRanged
        
        spells [
            THC_PoisonSwat
            THC_Roll
            THC_CoinRoll
        ]
    }

    passives {
        
        
        EraseSpawnCoins 1

        StatusOnGainCoins {
            BackflipWhenTargeted {
                stacks 1
                ability BackflipDodge
            }
        }

       /* AddStatusToReceivedAbilityDamage {
            ScatterHeldCoin 1
        }*/
        AwardCoinsOnDeath 10
    }
    
    ai {
        pattern {
            do_all [*THC_PoisonSwat attack *THC_CoinRoll THC_CoinRoll *THC_Roll]
        }

        brain PatternBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `MedicCat`
**Name:** Marshmallow  
**Source:** `cat_minibosses.gon`  

```
MedicCat { 
    graphics {
        movieclip _CAT
        name "Marshmallow"
        custom_cat_data MedicCat

        tooltip "Bad miniboss. this needs to be redesigned."
    }

    equipment {
        neck AngelicAura
    }

    stats {
        strength 4
        dexterity 4
        constitution 3
        intelligence 3
        speed 3
        charisma  4
        luck 4
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 2
        
        mana_regen 999
        mana 100
        
        health 20
        can_collect_coins true
    }

    abilities {
        move DefaultMove
        attack BasicShortRanged
        
        spells [
            HealBomb
            MassHeal
        ]
    }

    passives {
        Phylactery {
            obj Phylactery
            statuses {
                AllStatsUp 1
                TakeExtraTurn 1
            }
        }
        RunWhenMaxPhylacteryHeal 1
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do attack
        }

        bonusturn_pattern {
            do HealBomb
            do MassHeal
        }

        fallback {
            do attack
        }

        decision_weights prioritize_healing
        move_weights keep_distance_always_move
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `MedicCat`
**Name:** Marshmallow  
**Source:** `cat_minibosses.gon`  

```
MedicCat {
    graphics {
        movieclip _CAT
        name "ENEMY_MARSHMALLOW_NAME"
        custom_cat_data MedicCat

        tooltip "ENEMY_MARSHMALLOW_DESC"
    }

    equipment {
        neck AngelicAura
    }

    stats {
        strength 5
        dexterity 1
        constitution 3
        intelligence 4
        speed 4
        charisma  5
        luck 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 2
        
        mana_regen 999
        mana 100
        
        health 60
        divine_shield 2
        movement 3
    }

    abilities {
        move DefaultMove
        attack BasicMedicMelee
        
        spells [
            MarshmallowConvert
            MarshmallowZealot
        ]
    }

    passives {
        AvoidDamagingCharmedEnemies 1
        RunWhenLastPlayerCatIsCharmed {
            allow_decision_mid_turn true
            legacy_savekey Legacy_Marshmallow_StolenCatID
        }
        LegacySpawnSavedCatIfExists Legacy_Marshmallow_StolenCatID
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            CloseConvert {
                ability MarshmallowConvert
                move_weights stay_close
            }
        }

        mainturn_pattern {
            do_all [*MarshmallowZealot, CloseConvert, attack]
        }
        bonusturn_pattern {
            do_all [CloseConvert, attack]
        }

        decision_weights default
        move_weights keep_close_distance_always_move
    }
}
```

---

### `FighterCat`
**Name:** Magnus  
**Source:** `cat_minibosses.gon`  

```
FighterCat {
    graphics {
        movieclip _CAT
        name "ENEMY_MAGNUS_NAME"
        custom_cat_data FighterCat

        tooltip "ENEMY_MAGNUS_DESC"
    }

    equipment {
        neck SamsonsChains
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 1
        dispersed_bonus_turns_consider_initiative false
        movement 2
        
        mana_regen 999
        mana 100
        
        health 70
    }

    abilities {
        move DefaultMove
        attack BasicMelee_Fighter
        
        spells [
            ChainDash
            Spin_Enemy
        ]
    }

    passives {
        /*RunWhenWonFight {
            allow_decision_mid_turn true
        }*/
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do ChainDash
        }

        bonusturn_pattern {
            do Spin_Enemy
        }

        decision_weights semi_simple
        move_weights keep_distance_always_move
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `StacyMutant`
**Name:** Stacy Mutant  
**Source:** `cat_minibosses.gon`  

```
StacyMutant {
    graphics {
        movieclip _CAT
        name "ENEMY_STACYMUTANT_NAME"
        custom_cat_data Stacy2p0 
		scale 1.3
        tooltip "ENEMY_STACYMUTANT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type boss
        health 125
        faction enemies
        base_mana_regen 999
        evenly_dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            SM_MagicMissile
            SM_Flamethrower
            SM_IceShards
            SM_LightningStorm

            SM_BleedCounter
        ]
    }

    passives {	
	    BossRewards {
		    common Stacy100
		    rare UnstableDNA
	    }

        AdventureTokenPassivePool { 
            
            StacyMutant_Fire {
                ElementImmune Fire
                ReplaceBasicAttack SM_Lavashot
                
                CatPartsTransform {
					head 1019
					texture 19
					palette 78
				}

                ReplaceBrain {
                    brain PatternBrain
                    
                    pattern {
                        do_all [attack SM_Flamethrower]
                        do move
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
            StacyMutant_Ice {
                ElementImmune Ice
                ReplaceBasicAttack SM_IceBreath
                AddMovement -1
                
                CatPartsTransform {
                    head 1020
                    texture 29
                    palette 77
				}

                ReplaceBrain {
                    brain PatternBrain

                    pattern {
                        do_all [*attack SM_IceShards]
                        do move
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }
            StacyMutant_Lightning {
                ElementImmune Electric
                ReplaceBasicAttack SM_LightningDash
                
                CatPartsTransform {
                    head 1027
                    texture 60
                    palette 76
				}

                ReplaceBrain {
                    brain PatternBrain

                    pattern {
                        do_all [attack SM_LightningStorm]
                        do move
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }

            
            StacyMutant_Thorns {
                Thorns 3
                
				CatPartsTransform {
                    body 1012
                }
            }
            StacyMutant_Brace {
                Brace 3
                
				CatPartsTransform {
                    body 1013
                }
            }
            StacyMutant_Holy {
                DivineShield 7
                
				CatPartsTransform {
                    body 1024
                }
            }

            
            StacyMutant_Health {
                AddMaxHealth 25
                AddSpeed -3
                SizeScale 1.2
                
				CatPartsTransform {
                    leg1 1043
                    leg2 1043
                    arm1 1043
                    arm2 1043
                    tail 1034
                }  
            }
            StacyMutant_Damage {
                AddDamage 2
                AddMaxHealth -25
                
				CatPartsTransform {
                    leg1 1044
                    leg2 1044
                    arm1 1044
                    arm2 1044
                    tail 1035
                }  
            }
            StacyMutant_Speed {
                AddDamage -1
                AddSpeed 6
                SizeScale .8
                
				CatPartsTransform {
                    leg1 1045
                    leg2 1045
                    arm1 1045
                    arm2 1045
                    tail 1036
                }
            }

            
            StacyMutant_DoubleHead {
                ExtraDispersedTurns 1
                CatPartsTransform {
                    ear1 1028
                }  
            }
            StacyMutant_Counter {
                
                CounterAttack SM_BleedCounter
                AddStatusToBasicAttack {
                    Bleed 1
                }
                CatPartsTransform {
                    ear1 1029
                }  
            }
            StacyMutant_Mirror {
                
                ReflectProjectiles 100%
                StatusEachTurnEndForEachTurn {
                    RandomMagicMissile 1
                }
                CatPartsTransform {
                    eye1 1057
                    eye2 1057
                }  
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
            do SM_MagicMissile
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `ColorlessCat_Tutorial`
**Name:** Pebbles  
**Source:** `cat_minibosses.gon`  

```
ColorlessCat_Tutorial {
    graphics {
        movieclip _CAT
        name "ENEMY_PEBBLES_NAME"
        custom_cat_data Pebbles

        tooltip "ENEMY_PEBBLES_DESC"
    }

    equipment {
        head Pebble
    }

    stats {
        strength 3
        dexterity 3
        constitution 3
        intelligence 3
        speed 3
        charisma  3
        luck 3
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 1
        dispersed_bonus_turns_consider_initiative false
        movement 4

        health 50
    }

    abilities {
        move DefaultMove
        attack ColorlessCat_Push
        
        spells [
            RockToss_ColorlessCat
            RockToss_ColorlessCat_AsCloseAsPossible
            ColorlessCat_BoulderDrop
        ]
    }

    passives {
        TutorialBossRiggedFight 16
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [ColorlessCat_BoulderDrop, attack, RockToss_ColorlessCat]
            do_priority [ColorlessCat_BoulderDrop, RockToss_ColorlessCat, attack]
        }

        fallback {
            do RockToss_ColorlessCat_AsCloseAsPossible
        }

        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `NecroCat`
**Name:** Morana  
**Source:** `cat_minibosses.gon`  

```
NecroCat {
    graphics {
        movieclip _CAT
        name "ENEMY_MORANA_NAME"
        custom_cat_data NecroCat
		tooltip "ENEMY_MORANA_DESC"
    }

    equipment {
        face NecromancerMask
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        health 75
        corpse_health 5
        dispersed_bonus_turns 1
        round_end_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicNecroRanged
        
        spells [
            NCReanimate
            NCGravecrawl
        ]
    }

    passives {
        InfiniteRebirth {
            health 25%
            playercat_health 25%
            immediate true
        }
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            NCGravecrawlFAR {
                ability NCGravecrawl
                move_weights stay_far
            }
        }

        pattern {
            do_all [attack]
        }
        round_end_bonusturn_pattern {
            do_priority [NCReanimate NCGravecrawlFAR]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `TinkererCat`
**Name:** Franklin  
**Source:** `cat_minibosses.gon`  

```
TinkererCat {
    graphics {
        movieclip _CAT
        name "ENEMY_FRANKLIN_NAME"
        custom_cat_data TinkererCat
		tooltip "ENEMY_FRANKLIN_DESC"
    }

    equipment {
        head TinkererHat
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        health 45
		shield 20
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            TCMechSuit
            TCCatBot
        ]
    }

    passives {

        FormChanger {
            Default {
            }
            DesireMech {
                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [*TCMechSuit TCMechSuit]
                    }
                    decision_weights default
                    move_weights keep_distance
                }
            }
        }

        FormChangeHealthThreshold {
            threshold 25
            count_shield true
            form_below DesireMech
            form_above Default
        }

        TinkererBasicAttackSwitching {
            craft_ability TinkererCraft
            throw_ability TinkererThrow
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [weapon *attack weapon attack move]
            do_all [*TCCatBot weapon *attack weapon attack move]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `TCMechSuit`
**Source:** `cat_minibosses.gon`  

```
TCMechSuit {
    variant_of MechSuit

    stats {
        strength 4
        dexterity 3
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }

    passives {
        AllSpellsCostActPoints 1
        SetSpellCosts 0
    }
}
```

---

### `ButcherCat`
**Name:** Gein  
**Source:** `cat_minibosses.gon`  

```
ButcherCat {
    graphics {
        movieclip _CAT
        name "ENEMY_GEIN_NAME"
        custom_cat_data ButcherCat
		tooltip "ENEMY_GEIN_DESC"
    }

    equipment {
        face ButcherMask
        weapon ButcherHook
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        health 73
        movement 1
        can_eat_food true
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicButcherMeleeWideSpin
        
        spells [
            MoveTwo
        ]
    }

    passives {
        Trample 3
        MovementReaction {
            ability weapon
            enemies_only true
        }
        AbilityWhenTaggedCharacterMovesNear {
            ability MoveTwo
            tag food
            range 4
        }
        AddStatusToWeapons {
            Bleed 1
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [*attack attack]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `PsychicCat`
**Name:** Alice  
**Source:** `cat_minibosses.gon`  

```
PsychicCat {
    graphics {
        movieclip _CAT
        name "ENEMY_ALICE_NAME"
        custom_cat_data PsychicCat
		tooltip "ENEMY_ALICE_DESC"
    }

    equipment {
        face PsychicMask
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        health 66
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicPsychicPull
        
        spells [
            PsychicChoke_Enemy
            PsychicCatBackflip
        ]
    }

    passives {
        CounterAttackAfterEnemyCastSpell Telekinesis
    }
    
    ai {
        brain PatternBrain 

        pattern {
            do_all [attack PsychicChoke_Enemy]
            do_all [attack PsychicChoke_Enemy PsychicCatBackflip]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `DruidCat`
**Name:** Draven  
**Source:** `cat_minibosses.gon`  

```
DruidCat {
    graphics {
        movieclip _CAT
        name "ENEMY_DRAVEN_NAME"
        custom_cat_data DruidCat
		tooltip "ENEMY_DRAVEN_DESC"
    }

    equipment {
        neck DruidNeck
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        hidden_tag dc_cat
        faction enemies
        type boss
        health 70
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack DruidCatBasic
        
        spells [
            DCSquirrelForm
            DCBirthSquirrel
        ]
    }

    passives {
        FormChanger {
            Default {
            }
            SquirrelForm {
                attack BasicMelee
                tooltip ENEMY_DRAVENSQUIRRELFORM_DESC

                passives {
                    SpeedUp 6
                    AddTemporaryEffectsToBasicAttack {
                        Fury 75
                    }

                }
                ai {
                    brain PatternBrain

                    pattern {
                        do_all [*DCBirthSquirrel attack DCBirthSquirrel]
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [DCSquirrelForm attack]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `DruidCrow`
**Name:** Draven's Crow  
**Source:** `cat_minibosses.gon`  

```
DruidCrow {
    variant_of Crow

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }

    graphics {
        name "Draven's Crow"
        tooltip ""
    }

    properties {
        faction enemies
        hidden_tag dc_crow
        base_crit_chance -999
    }

    passives {
    }
}
```

---

### `DruidCrow`
**Name:** Draven's Crow  
**Source:** `cat_minibosses.gon`  

```
DruidCrow {
    graphics {
        movieclip Crow
        name "ENEMY_DRAVENCROW_NAME"
        uifloaters_offset 1
        shadow_size .75
        scale .8
		tooltip "ENEMY_DRAVENCROW_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [animal crow]
        hidden_tag dc_crow
        faction enemies

        base_movement 4
        mana_matters false

        corpse_health 1

        flying true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            DCAeroblast
        ]
    }

    passives {
        Bird CookedChickenLeg

        SecurityBotProtect {
            enemies_only true
            tag_restriction dc_cat
        }
    }
    
    ai {
        brain PatternBrain 

        pattern {
            do_all [attack DCAeroblast]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `MonkCat`
**Name:** Chan Hung  
**Source:** `cat_minibosses.gon`  

```
MonkCat {
    graphics {
        movieclip _CAT
        name "Chan Hung"
        custom_cat_data MonkCat
    }

    equipment {
        face MonkMask
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        health 65
        dispersed_bonus_turns 2
    }

    abilities {
        move DefaultMove
        attack BasicMonkMelee
        
        spells [
            MCMonkStyleChange
        ]
    }

    passives {
        PrioritizeHitDifferentTargets 1
        ExtraBasicAttacks 1
        MonkStances [BasicMonkMelee BasicMonkRanged]

        FormChanger {
            Melee {
                passives {
                    ChanceToBlockAndCounter {
                        chance 100%
                        melee_only true
                    }
                }
            }
            Ranged {
                passives {
                    ChanceToBlockAndCounter {
                        chance 100%
                        ranged_only true
                    }
                }
            }
        }
        FormChangerMatchMonkStances {
            melee Melee
            ranged Ranged
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*MCMonkStyleChange attack attack]
        }

        stun_advances_pattern false
        fallback_advances_pattern false
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `MonkCat`
**Name:** Chan Hung  
**Source:** `cat_minibosses.gon`  

```
MonkCat {
    graphics {
        movieclip _CAT
        name "ENEMY_CHANHUNG_NAME"
        custom_cat_data MonkCat
		tooltip "ENEMY_CHANHUNG_DESC"
    }

    equipment {
        face MonkMask
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        health 65
        movement 3
        initiative -20
    }

    abilities {
        move DefaultMove
        attack MCMelee
        
        spells [
            MCHadouken
            MCKineticCharge
        ]
    }

    passives {
        MonkCatReactionAbilities {
            move move
            attack attack
            weapon attack
            spell MCHadouken
            trinket MCHadouken
        }
        AggroTargetIsCurrentTurn 1
        PrioritizeAggroTarget 1
        Brace 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do MCKineticCharge
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `JesterCat`
**Name:** Arthur  
**Source:** `cat_minibosses.gon`  

```
JesterCat {
    graphics {
        movieclip _CAT
        name "ENEMY_ARTHUR_NAME"
        custom_cat_data JesterCat
		tooltip "ENEMY_ARTHUR_DESC"
    }

    equipment {
        head JesterHat
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 10
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        health 75
        dispersed_bonus_turns 2
        base_crit_chance 0
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            Metronome_Enemy
        ]
    }

    passives {
        RandomizeAIWeightsEachTurn [
            {
                decision_weights default
                move_weights keep_distance
            }

            {
                decision_weights default
                move_weights stay_close_ish
            }
        ]
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [Metronome_Enemy attack]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Chupacabra`
**Name:** Chupacabra  
**Source:** `cat_minibosses.gon`  

```
Chupacabra {
    graphics {
        movieclip _CAT
        name "ENEMY_CHUPACABRA_NAME"
        custom_cat_data Chupacabra
		scale .8
        tooltip "ENEMY_CHUPACAPBRA_DESC"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 2
        dispersed_bonus_turns_consider_initiative false
        movement 4
        scale 1.3
        mana_regen 999
        mana 100
        
        health 77
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            WolfLeap
            SharkDash
        ]
    }

    passives {
	    MoveWhenDamaged {
            weights stay_far_always_move
        }
        AddStatusToBasicAttack {
            Leech 2
        }
        AddStatusToSpells {
            Leech 2
        }
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do WolfLeap
        }

        bonusturn_pattern {
            do SharkDash
        }

        decision_weights semi_simple
        move_weights keep_distance_always_move
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `Hellspawn`
**Name:** Hellspawn  
**Source:** `cat_minibosses.gon`  

```
Hellspawn {
    graphics {
        movieclip _CAT
        name "ENEMY_HELLSPAWN_NAME"
        custom_cat_data Hellspawn1
		tooltip "ENEMY_HELLSPAWN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        health 69
        movement 1
        can_eat_food true
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicButcherMelee
        
        spells [
            MoveTwo
        ]
    }

    passives {
        StatusOnTookDamageFromAbility {
            TakeExtraTurn 1
        }
        AbilityWhenTaggedCharacterMovesNear {
            ability MoveTwo
            tag food
            range 2
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [*attack attack]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `InfestedDuo`
**Name:** Paraisaria  
**Source:** `cat_minibosses.gon`  

```
InfestedDuo {
    graphics {
        movieclip _CAT
        name "ENEMY_PARAISARIA_NAME"
        custom_cat_data InfestedDuo
        scale 1.2
        shadow_size 1.2

        tooltip "ENEMY_PARAISARIA_DESC"
    }
    
    equipment {
        head BulbHead
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat plant]
        type boss
        health 65
        base_mana_regen 999
        faction enemies
        movement 1
        disperse_main_turns true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            IDSprout
            IDBrambleBurst
            IDBrambleShot
        ]
    }

    passives {
        Plant 1
        ElementImmune Creep
        Thorns 2
        AddStatusToBasicAttack {
            Poison 1
        }
        AbilityReaction IDSprout
        ExtraTurnsPerTaggedUnit sprout
        DeathRattle IDBrambleBurst
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [attack IDBrambleShot]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `CaveCatDad`
**Name:** Frod Rocksnow  
**Source:** `cat_minibosses.gon`  

```
CaveCatDad {
    graphics {
        movieclip _CAT
        name "ENEMY_FRODROCKSNOW_NAME"
        custom_cat_data DaddyCat
        scale 1.4
        shadow_size 1.4

        tooltip "ENEMY_FRODROCKSNOW_DESC"
    }

    equipment {
        weapon CaveCatClub
    }

    stats {
        strength 8
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        hidden_tag cavefamily
        type boss
        health 70
        base_mana_regen 999
        faction enemies
        movement 2
        disperse_main_turns true
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack CaveDad_ClubBasic
        
        spells [
            RockToss_CaveDad
            CaveCatEnrageOne
            CaveCatEnrageTwo
        ]
    }

    passives {
        FormChanger {
            AllAlive {
                passives {
                    CaveFamilyEnrage {
                        ability CaveCatEnrageOne
                        tag cavefamily
                        count 1 
                    }
                }
            }
            TwoAlive {
                passives {
                    Brace 2
                    CaveFamilyEnrage {
                        ability CaveCatEnrageTwo
                        tag cavefamily
                        count 0 
                    }
                }
                turns {
                    evenly_dispersed_bonus_turns 1
                }
            }
            OneAlive {
                passives {
                    Brace 4
                }
                turns {
                    evenly_dispersed_bonus_turns 2
                }
            }
        }
        
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [attack RockToss_CaveDad]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `CaveCatMom`
**Name:** Wolma Rocksnow  
**Source:** `cat_minibosses.gon`  

```
CaveCatMom {
    graphics {
        movieclip _CAT
        name "ENEMY_WOLMAROCKSNOW_NAME"
        custom_cat_data MommyCat
        scale 1.2
        shadow_size 1.2

        tooltip "ENEMY_WOLMAROCKSNOW_DESC"
    }
    
    equipment {
        head Dreadlocks
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        hidden_tag cavefamily
        type boss
        health 60
        base_mana_regen 999
        faction enemies
        movement 3
        disperse_main_turns true
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack CaveMom_Basic
        
        spells [
            CaveMom_TossDad
            CaveMom_TossElsewhere
            CaveMom_Heal
            CaveCatEnrageOne
            CaveCatEnrageTwo
        ]
    }

    passives {
        Buddy CaveCatDad 

        FormChanger {
            AllAlive {
                passives {
                    CaveFamilyEnrage {
                        ability CaveCatEnrageOne
                        tag cavefamily
                        count 1 
                    }
                }
            }
            TwoAlive {
                passives {
                    Brace 2
                    CaveFamilyEnrage {
                        ability CaveCatEnrageTwo
                        tag cavefamily
                        count 0 
                    }
                }
                turns {
                    evenly_dispersed_bonus_turns 1
                }
            }
            OneAlive {
                passives {
                    Brace 4
                }
                turns {
                    evenly_dispersed_bonus_turns 2
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [*CaveMom_TossDad *CaveMom_TossElsewhere attack CaveMom_Heal]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `CaveCatBaby`
**Name:** Poobles Rocksnow  
**Source:** `cat_minibosses.gon`  

```
CaveCatBaby {
    graphics {
        movieclip _CAT
        name "ENEMY_POOBLESROCKSNOW_NAME"
        custom_cat_data BabyCat
        scale .9
        shadow_size .9

        tooltip "ENEMY_POOBLESROCKSNOW_DESC"
    }
    
    equipment {
        head BabyHair
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 9
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        hidden_tag cavefamily
        type boss
        health 50
        base_mana_regen 999
        faction enemies
        disperse_main_turns true
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack CaveCatPounce
        
        spells [
            BearTrap_CaveBaby
            CaveCatEnrageOne
            CaveCatEnrageTwo
        ]
    }

    passives {
        MoveWhenDamaged {
            weights stay_near_allies_always_move
        }

        FormChanger {
            AllAlive {
                passives {
                    CaveFamilyEnrage {
                        ability CaveCatEnrageOne
                        tag cavefamily
                        count 1 
                    }
                }
            }
            TwoAlive {
                passives {
                    Brace 2
                    CaveFamilyEnrage {
                        ability CaveCatEnrageTwo
                        tag cavefamily
                        count 0 
                    }
                }
                turns {
                    evenly_dispersed_bonus_turns 1
                }
            }
            OneAlive {
                passives {
                    Brace 4
                }
                turns {
                    evenly_dispersed_bonus_turns 2
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [MoveForPounce move BearTrap_CaveBaby attack]
        }

        virtual_abilities {
            MoveForPounce {
                ability move
                move_for_ability attack
                move_weights keep_distance
            }
        }

        decision_weights default
        move_weights keep_distance


    }
}
```

---

### `Dclaude`
**Name:** D'Claude  
**Source:** `cat_minibosses.gon`  

```
Dclaude {
    graphics {
        movieclip _CAT
        name "ENEMY_DCLAUDE_NAME"
        custom_cat_data Dclaude
		scale 1.2
        tooltip "ENEMY_DCLAUDE_DESC"
    }

    equipment {

    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 1
        dispersed_bonus_turns_consider_initiative false
        movement 5
        
        mana_regen 999
        mana 100
        
        health 75
    }

    abilities {
        move DefaultMove
        attack BasicMelee_Fighter
        
        spells [
            Dclaude_Declaw
            QueenHippoAttack
        ]
    }

    passives {
		CounterAttack attack
		
        ReflectProjectiles {
            self_damage 2
        }
        AbilityReaction {
            ability attack
            backstabs_only true
        }
		
        RandomizeAIWeightsEachTurn [
            {
                decision_weights default
                move_weights stay_close
            }

            {
                decision_weights no_act
                move_weights stay_close
            }
        ]
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do Dclaude_Declaw
        }

        bonusturn_pattern {
            do QueenHippoAttack
        }

        decision_weights semi_simple
        move_weights keep_distance_always_move
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `WhiteRabbit`
**Name:** White Rabbit  
**Source:** `cat_minibosses.gon`  

```
WhiteRabbit {
    graphics {
        movieclip _CAT
        name "ENEMY_WHITERABBIT_NAME"
        custom_cat_data WhiteRabbit

        tooltip "ENEMY_WHITERABBIT_DESC"
    }

    equipment {
        face Rabiesface
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 4
        dispersed_bonus_turns_consider_initiative false
        movement 2
        
        mana_regen 999
        mana 100
        
        health 50
    }

    abilities {
        move DefaultMove
        attack BasicMelee_Fighter
        
        spells [
            ChainDash
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do ChainDash
        }

        decision_weights semi_simple
        move_weights keep_distance_always_move
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `Crow`
**Name:** {SpawnedBy}'s Crow  
**Source:** `druid_friends.gon`  

```
Crow {
    graphics {
        movieclip Crow
        name "ENTITY_CROW_NAME"
        uifloaters_offset 1
        shadow_size .75
        scale .8

        tooltip "ENTITY_CROW_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [animal crow]
        hidden_tag bird
        faction allies
        inherit_faction true

        base_movement 4
        base_initiative 0
        base_health 0
        base_mana 0
        base_mana_regen 0
        base_health_regen 0
        base_initial_mana 0
        base_crit_chance 0
        mana_matters true

        weak_threshold 5 
        can_collect_coins true
        can_eat_food true
        access_to_player_inventory true
        corpse_health 1

        flying true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        can_get_bonus true
        
        spells [
            CrowFlutter
            CrowFlap
        ]
    }

    passives {
        InheritSpawnerStats 1
        CrowAttackLink 1
        Bird CookedChickenLeg
    }
    
    ai {
        brain PlayerBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Crow2`
**Source:** `druid_friends.gon`  

```
Crow2 {
    variant_of Crow

    abilities {
        spells [
            CrowFlutter2
            CrowFlap2
        ]
    }
}
```

---

### `Crow3`
**Source:** `druid_friends.gon`  

```
Crow3 {
    variant_of Crow

    abilities {
        spells [
            CrowFlutter3
            CrowFlap3
        ]
    }
}
```

---

### `BabySquirrel`
**Name:** Baby Squirrel  
**Source:** `druid_friends.gon`  

```
BabySquirrel {
    graphics {
        movieclip Squirrel
        name "ENTITY_BABYSQUIRREL_NAME"
        shadow_size .50
        scale .6
        move_speed_multiplier 1.75
    }

    stats {
        strength 1
        dexterity 1
        constitution 1
        intelligence 1
        speed 9
        charisma 1
    }
    
    properties {
        tag [animal squirrel]
        type small
        faction allies
        inherit_faction true
        movement 6
        health 1
        weak_threshold 0
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        can_get_bonus true
    }

    passives {

    }
    
    ai {
        brain PlayerBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Squirrel`
**Name:** Squirrel  
**Source:** `druid_friends.gon`  

```
Squirrel {
    graphics {
        movieclip Squirrel
        name "ENTITY_SQUIRREL_NAME"
        shadow_size .50
        move_speed_multiplier 1.75
    }

    stats {
        strength 2
        dexterity 1
        constitution 1
        intelligence 1
        speed 8
        charisma 1
    }
    
    properties {
        tag [animal squirrel]
        type small
        faction allies
        inherit_faction true
        movement 5
        health 1
        weak_threshold 0
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack SquirrelFurySwipes
        can_get_bonus true
    }

    passives {

    }
    
    ai {
        brain PlayerBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Snake`
**Name:** Snake  
**Source:** `druid_friends.gon`  

```
Snake {
    graphics {
        movieclip Snake
        name "ENTITY_SNAKE_NAME"
        uifloaters_offset .5
    }

    stats {
        strength 2
        dexterity 2
        constitution 2
        intelligence 2
        speed 5
        charisma 2
    }
    
    properties {
        tag animal
        type small
        faction allies
        inherit_faction true
        movement 5
        health 1
        weak_threshold 0
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        can_get_bonus true
    }

    passives {
        
        AddStatusToBasicAttack {
            Poison 1
        }
    }
    
    ai {
        brain PlayerBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Snake2`
**Source:** `druid_friends.gon`  

```
Snake2 {
    variant_of Snake
    passives {
        DodgeChance_Status 66
    }
}
```

---

### `Turtle`
**Name:** Turtle  
**Source:** `druid_friends.gon`  

```
Turtle {
    graphics {
        movieclip Turtle
        name "ENTITY_TURTLE_NAME"
        move_speed_multiplier .5
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 8
    }
    
    properties {
        tag [animal dog]
        type small
        faction allies
        inherit_faction true
        movement 1
        health 1
        shield 10
        weak_threshold 0
        corpse_health 1
        can_be_overkilled false
    }

    abilities {
        move DefaultMove
        attack BasicTankMelee
        can_get_bonus true
    }

    passives {
    }
    
    ai {
        brain PlayerBrain
        decision_weights semi_simple
        move_weights stay_close
    }
}
```

---

### `Toad`
**Name:** Toad  
**Source:** `druid_friends.gon`  

```
Toad {
    graphics {
        movieclip Frog
        name "ENTITY_TOAD_NAME"
    }

    stats {
        strength 2
        dexterity 1
        constitution 2
        intelligence 2
        speed 4
        charisma 2
    }
    
    properties {
        tag animal
        type small
        faction allies
        inherit_faction true
        view_bugs_as_enemies true
        movement 4
        health 1
        weak_threshold 0
        corpse_health 0
    }

    abilities {
        move BasicJump
        attack BasicHook
        can_get_bonus true
    }

    passives {
    }
    
    ai {
        brain PlayerBrain
        decision_weights semi_simple
        move_weights stay_close
    }
}
```

---

### `Toad2`
**Source:** `druid_friends.gon`  

```
Toad2 {
    variant_of Toad

    graphics {
        scale 1.2
    }

    stats {
        dexterity 5
    }

    properties {
        health 4
    }

    passives {
        ExtraMovePoints 1
    }
}
```

---

### `NeutralToad`
**Name:** Frog  
**Source:** `druid_friends.gon`  

```
NeutralToad {
    variant_of Toad

    graphics {
        name "ENTITY_FROG_NAME"
    }

    properties {
        faction none
        kill_required false
    }
    ai {
        brain GenericBrain
        move_weights random
    }
}
```

---

### `Bear`
**Name:** Bear  
**Source:** `druid_friends.gon`  

```
Bear {
    graphics {
        movieclip Bear
        name "ENTITY_BEAR_NAME"
        shadow_size 2
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag animal
        faction allies
        inherit_faction true
        movement 3
        health 15
        weak_threshold 0
        

        size 2x2
    }

    abilities {
        move DefaultMove
        attack BasicBigMelee
        can_get_bonus true
    }

    passives {
        Trample 3
        AddStatusToBasicAttack {
            Bleed 1
        }
    }
    
    ai {
        brain PlayerBrain
        decision_weights semi_simple
        move_weights stay_close
    }
}
```

---

### `Bear2`
**Source:** `druid_friends.gon`  

```
Bear2 {
    variant_of Bear

    abilities {
        attack BearFurySwipes
    }
}
```

---

### `MaddenedBear`
**Source:** `druid_friends.gon`  

```
MaddenedBear { 
    variant_of Bear
    passives {
        PermanentMadness 1
    }
    properties {
        faction enemies
    }
    ai {
        brain GenericBrain
    }
}
```

---

### `Catepillar`
**Name:** Caterpillar  
**Source:** `druid_friends.gon`  

```
Catepillar {
    graphics {
        movieclip Caterpillar
        name "ENTITY_CATERPILLAR_NAME"
        shadow_size .8
        move_speed_sync_frames 22

        tooltip "ENTITY_CATERPILLAR_DESC"
    }

    stats {
        strength 1
        dexterity 1
        constitution 1
        intelligence 1
        speed 1
        charisma 1
        luck 1
    }
    
    properties {
        tag animal
        type small
        faction allies
        inherit_faction true
        movement 1
        health 1
        weak_threshold 1
        
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        can_get_bonus true
    }

    passives {
        StatusEachTurnEnd {
            AllStatsUp 1
            HealthGain 4
        }
        TransformOnStatusThreshold {
            status AllStatsUp
            threshold 5
            object Moth
        }
    }
    
    ai {
        brain PlayerBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Moth`
**Name:** Moth  
**Source:** `druid_friends.gon`  

```
Moth {
    graphics {
        movieclip Moth
        name "ENTITY_MOTH_NAME"
        shadow_size .8
    }

    stats {
        strength 8
        dexterity 8
        constitution 8
        intelligence 8
        speed 8
        charisma 8
        luck 8
    }
    
    properties {
        tag animal
        type small
        faction allies
        inherit_faction true
        movement 5
        health 24
        flying true
        mana_matters true
    }

    abilities {
        move DefaultMove
        attack BasicShortLobbed
        can_get_bonus true

        spells [
            CrowFlutter
            SleepPowder
        ]
    }

    passives {
    }
    
    ai {
        brain PlayerBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `AnimalEgg`
**Name:** Egg  
**Source:** `druid_friends.gon`  

```
AnimalEgg {
    graphics {
        movieclip AnimalEgg
        name "ENTITY_EGG_NAME"
        tooltip ENTITY_EGG_DESC
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag animal
        faction allies
        inherit_faction true
        movement 0
        health 4
        shield 4
        corpse_health 0
        can_be_overkilled false
    }

    abilities {
        move None
        attack None

        spells [
            
        ]
    }

    passives {
        TransformInXTurns {
            stacks 2
            object [Squirrel Crow Snake Turtle Toad Catepillar]
            animation hatch
        }
    }
    
    ai {
        brain NoBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `AnimalEgg2`
**Source:** `druid_friends.gon`  

```
AnimalEgg2 {
    variant_of AnimalEgg

    passives {
        TransformInXTurns {
            stacks 1
        }
    }
}
```

---

### `GlowingMushroom`
**Name:** Glowing Mushroom  
**Source:** `druid_friends.gon`  

```
GlowingMushroom {
    graphics {
        movieclip GlowingMushroom
        name "ENTITY_GLOWMUSHROOM_NAME"
        tooltip ENTITY_GLOWMUSHROOM_DESC
        shadow_size .25
    }

    properties {
        type object
        tag plant

        faction allies
        inherit_faction true

        health 1
        corpse_health 0
        can_be_backstabbed false
        kill_required false

        ai_scale .01
    }

    abilities {
        move None
        attack None

        spells [
            GlowingMushroomGiveMana
        ]
    }

    passives {
        Plant 1
        ElementImmune Creep
        
        CharacterLightSource {
            color [.3, .7, 1]
            glow [.3, .7, 1, .5]
            size 4
        }
    }
    
    ai {
        brain PatternBrain
        pattern {
            do GlowingMushroomGiveMana
        }

        decision_weights always_cast
        move_weights stay_close
    }
}
```

---

### `GlowingMushroom2`
**Source:** `druid_friends.gon`  

```
GlowingMushroom2 {
    variant_of GlowingMushroom

    graphics {
        tooltip ENTITY_GLOWMUSHROOM2_DESC
    }

    abilities {
        spells [
            GlowingMushroomGiveMana2
        ]
    }
    ai {
        pattern {
            do GlowingMushroomGiveMana2
        }
    }
}
```

---

### `RandomDruidFamiliar`
**Source:** `druid_friends.gon`  

```
RandomDruidFamiliar {
    alt_spawn_pool {
        Squirrel 10
        Snake 10
        Turtle 10
        Toad 10
        Catepillar 10
        Bear 1
    }
}
```

---

### `Rat`
**Name:** Lil' Rat  
**Source:** `enemies.gon`  

```
Rat {
    graphics {
        movieclip Rat
        name "ENEMY_LILRAT_NAME"
        shadow_size .70

        tooltip "ENEMY_LILRAT_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag rat
        faction enemies
        
        movement 1
        health 5
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack Dash_Enemy
        
        spells [

        ]
    }

    passives {
        CanMutateTo [Lumpy, Leaper]
    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights keep_distance_always_move
    }
}
```

---

### `Pooter`
**Name:** Pooter  
**Source:** `enemies.gon`  

```
Pooter {
    graphics {
        movieclip Pooter
        name "ENEMY_POOTER_NAME"
        shadow_size .50
        uifloaters_offset 1

        tooltip "ENEMY_POOTER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag bug
        health 6
        movement 2
        faction enemies
        flying true
    }

    abilities {
        move DefaultMove
        attack BasicShortLobbed
        
        spells [

        ]
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights keep_distance
    }
}
```

---

### `Worm`
**Name:** Worm  
**Source:** `enemies.gon`  

```
Worm {
    graphics {
        movieclip Worm
        name "ENEMY_WORM_NAME"
        projectile_spawn_offset [.5 1]
        shadow none

        tooltip "ENEMY_WORM_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        health 5 
        movement 5
        faction enemies
    }

    abilities {
        move Teleport
        attack BasicRanged
        
        spells [

        ]
    }

    passives {
        MoveWhenDamaged move
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights random
    }
}
```

---

### `MadLad`
**Name:** Mad Lad  
**Source:** `enemies.gon`  

```
MadLad {
    graphics {
        movieclip MadLad
        name "ENEMY_MADLAD_NAME"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        health 30
        faction enemies
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        EnrageOnDamage 1
        CounterAttack attack
    }
    
    ai {
        brain GenericBrain
        decision_weights angry
        move_weights stay_close
    }
}
```

---

### `Gasser`
**Name:** Gasser  
**Source:** `enemies.gon`  

```
Gasser {
    graphics {
        movieclip Gasser
        name "ENEMY_GASSER_NAME"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        health 15
        faction enemies
        flying true
        mana_regen 999
        exclude_from_hallucinate true 
    }

    abilities {
        move DefaultMove
        attack SpawnGas
        
        spells [
            GasserExplode
        ]
    }

    passives {
        
        StatusImmunity Poison
        DeathRattle GasserExplode
    }
    
    ai {
        brain GenericBrain
        consider_spells false
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Rager`
**Name:** Rager  
**Source:** `enemies.gon`  

```
Rager {
    graphics {
        movieclip Rager
        name "ENEMY_RAGER_NAME"
        default_attack_animation bite1
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        health 30
        movement 3
        faction enemies
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            RageUp
        ]
    }

    passives {
        ScalingAttackAnimation {
            default bite1
            thresholds [
                [5, bite2] 
                [10, bite3] 
            ]
        }
    }
    
    ai {
        brain PatternBrain
        
        mainturn_pattern {
            do_strict [BasicMelee, RageUp]
        }
    
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Cutter`
**Name:** Cutter  
**Source:** `enemies.gon`  

```
Cutter {
    graphics {
        movieclip Cutter
        name "ENEMY_CUTTER_NAME"
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        
        health 50
        movement 5
        faction enemies
        round_end_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            CutterCut
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain
        
        mainturn_pattern {
            do attack
        }

        round_end_bonusturn_pattern {
            do CutterCut
        }
    
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Hive`
**Name:** Blorb  
**Source:** `enemies.gon`  

```
Hive {
    graphics {
        movieclip Hive
        name "ENEMY_BLORB_NAME"
        scale .8
		
		tooltip "ENEMY_BLORB_DESC"
    }

    stats {
        strength 1
        dexterity 1
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag tumor
        health 8
        faction enemies
        corpse_health 0
        movement 2
    }

    abilities {
        move DefaultMove
        attack BigGunkShot
        
        spells [

        ]
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `FloatingHive`
**Name:** Florb  
**Source:** `enemies.gon`  

```
FloatingHive {
    graphics {
        movieclip FloatingHive
        name "ENEMY_FLORB_NAME"
        uifloaters_offset 1.5
        scale .8
		
		tooltip "ENEMY_FLORB_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag tumor
        health 10
        movement 6
        faction enemies
        flying true
        corpse_health 0
        movement 3
    }

    abilities {
        move DefaultMove
        attack GunkShot
        
        spells [

        ]
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Lumpy`
**Name:** Lumpy  
**Source:** `enemies.gon`  

```
Lumpy {
    graphics {
        movieclip BloatRat
        name "ENEMY_LUMPY_NAME"
        water_mask medium

        tooltip "ENEMY_LUMPY_DESC"
    }

    stats {
        strength 3
        dexterity 4
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [rat blob]
        faction enemies
        initiative 5
        movement 3
        health 9
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack CreepRanged
        
        spells [

        ]
    }

    passives {
        SpawnCreepOnHit 1
        ElementImmune Creep
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Leaper`
**Name:** Leaper  
**Source:** `enemies.gon`  

```
Leaper {
    graphics {
        movieclip FatRat
        name "ENEMY_LEAPER_NAME"
        water_mask medium

        tooltip "ENEMY_LEAPER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [rat blob]
        faction enemies
        
        movement 2
        health 9
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack RatLeap
        
        spells [

        ]
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights keep_ranged_distance
    }
}
```

---

### `BombFly`
**Name:** Bomb Fly  
**Source:** `enemies.gon`  

```
BombFly {
    graphics {
        movieclip BombFly
        name "ENEMY_BOMBFLY_NAME"
        tooltip ENEMY_BOMBFLY_DESC
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [bug bomb]
        health 6
        movement 3
        faction enemies
        flying true
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        DeathRattle BombFlyExplode
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `TumorousMaggot`
**Name:** Burfer Maggot  
**Source:** `enemies.gon`  

```
TumorousMaggot {
    graphics {
        movieclip Burfer
        name "ENEMY_BURFERMAGGOT_NAME"

        tooltip "ENEMY_BURFERMAGGOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        health 14
        movement 3
        faction enemies
    }

    abilities {
        move DefaultMove
        attack PrisonShot
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `ChargeyMaggot`
**Name:** Chargey Maggot  
**Source:** `enemies.gon`  

```
ChargeyMaggot {
    graphics {
        movieclip ChargeyMaggot
        name "ENEMY_CHARGEYMAGGOT_NAME"

        tooltip "ENEMY_CHARGEYMAGGOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        health 9
        movement 2
        faction enemies
    }

    abilities {
        move DefaultMove
        attack SmallTrampleDash
        
        spells [

        ]
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `SwappyMaggot`
**Name:** Diggy Maggot  
**Source:** `enemies.gon`  

```
SwappyMaggot {
    graphics {
        movieclip DiggyMaggot
        name "ENEMY_DIGGYMAGGOT_NAME"

        tooltip "ENEMY_DIGGYMAGGOT_DESC"
    }

    stats {
        strength 7
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        health 8
        movement 20
        faction enemies
        corpse_health 0
    }

    abilities {
        move SwapPositions
        attack Lick
        
        spells [

        ]
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights random
    }
}
```

---

### `TarBaby`
**Name:** Tar Baby  
**Source:** `enemies.gon`  

```
TarBaby {
    graphics {
        movieclip TarBaby
        name "ENEMY_TARBABY_NAME"

        tooltip "ENEMY_TARBABY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        health 9
        movement 4
        faction enemies
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack TarBall
        
        spells [

        ]
    }

    passives {
        TileTrail_Ahead OilTile
        GoopWalk 1
        StatusImmunity Tarred
        DiesToElement {
            element Fire
            instant true
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `ChumBag`
**Name:** Chum Bag  
**Source:** `enemies.gon`  

```
ChumBag {
    graphics {
        movieclip ChumBag
        name "ENEMY_CHUMBAG_NAME"

        tooltip "ENEMY_CHUMBAG_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
    }
    
    properties {
        tag [blob trash]
        hidden_tag container
        auto_run_priority stationary
        health 1
        movement 4
        faction enemies
        corpse_health 0
    }

    abilities {
        move None
        attack ChumShot_Damage
        
        spells [
            ChumShot_Maggot
        ]
    }

    passives {
        TransformOnDeath Chummy
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do_priority [ChumShot_Damage, ChumShot_Maggot]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Chummy`
**Name:** Chummy  
**Source:** `enemies.gon`  

```
Chummy {
    graphics {
        movieclip Chummy
        name "ENEMY_CHUMMY_NAME"

        tooltip "ENEMY_CHUMMY_DESC"
    }

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        health 10
        movement 3
        faction enemies
    }

    abilities {
        move DefaultMove
        attack ChumDash
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Host`
**Name:** Host  
**Source:** `enemies.gon`  

```
Host {
    graphics {
        movieclip Host
        name "ENEMY_HOST_NAME"
        water_mask medium

        tooltip "ENEMY_HOST_DESC"
    }

    stats {
        strength 3
        dexterity 3
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [blob undead]
        auto_run_priority stationary
        health 13
        movement 2
        faction enemies
        dispersed_bonus_turns 1
    }

    abilities {
        move None
        attack HostSpit

        spells [
            HostShove
        ]
    }

    passives {
        ReflectProjectiles {
            self_damage 2
        }

        MeleeRevengeDamage {
            type status
            damage 0
            knockback 2
        }

    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do_priority [HostShove, HostSpit]
        }

        decision_weights careless
        move_weights keep_distance
    }
}
```

---

### `Pile`
**Name:** Pile  
**Source:** `enemies.gon`  

```
Pile {
    graphics {
        movieclip Pile
        name "ENEMY_PILE_NAME"
        projectile_spawn_offset [0 1]
        water_mask medium

        tooltip "ENEMY_PILE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag poop
        auto_run_priority stationary
        health 8
        movement 0
        faction enemies
        corpse_health 0
        can_be_backstabbed false
    }

    abilities {
        move None
        attack DipShot
        
        spells [
            SpawnDip
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do_priority [DipShot, SpawnDip]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Floater`
**Name:** Floater  
**Source:** `enemies.gon`  

```
Floater {
    graphics {
        movieclip Floater
        name "ENEMY_FLOATER_NAME"
        scale .75

        tooltip "ENEMY_FLOATER_DESC"

    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag poop
        faction enemies
        
        movement 3
        health 8
        base_mana_regen 999
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack FloaterMelee
        
        spells [

        ]
    }

    passives {
        WaterWalk 1
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `WaterLeech`
**Name:** Water Leech  
**Source:** `enemies.gon`  

```
WaterLeech {
    graphics {
        movieclip WaterLeech
        name "ENEMY_WATERLEECH_NAME"

        tooltip "ENEMY_WATERLEECH_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        faction enemies
        
        movement 3
        health 18
        initial_health 8
        
        base_mana_regen 999
    }

    abilities {
        move SwimmerMove
        attack LeechDash
        
        spells [
            DefaultMove
        ]
    }

    passives {
        WaterWalk 1

        FormChanger {
            Water {
                partial_animation_suffix "Water"

                passives {
                    AddMovement 2
                }
            }
            Out {
                passives {
                    GroundFlopper DefaultMove
                }
            }

            initial_form Water
        }

        SwimmingFormChange {
            form_in Water
            form_out Out
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights careless
        move_weights keep_distance_always_move
    }
}
```

---

### `DaddyShark`
**Name:** Daddy Shark  
**Source:** `enemies.gon`  

```
DaddyShark {
    graphics {
        movieclip DaddyShark
        name "ENEMY_DADDYSHARK_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed

        tooltip "ENEMY_DADDYSHARK_DESC"
        show_infinity_damage_warning true
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
    }
    
    properties {
        tag [cat fish]
        health 28
        movement 1
        faction enemies

        size 2x2
        move_block everything_even_when_dead
        view_bleeding_characters_as_enemies true
    }

    abilities {
        move DefaultMove
        attack DaddyHungry

        spells [

        ]
    }

    passives {
        Trample 3
        SharkySmellsBlood 1
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `BabyShark`
**Name:** Baby Shark  
**Source:** `enemies.gon`  

```
BabyShark {
    graphics {
        movieclip BabyShark
        name "ENEMY_BABYSHARK_NAME"
        shadow_size .75

        tooltip "ENEMY_BABYSHARK_DESC"
    }

    stats {
        strength 1
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [cat fish]
        health 5
        movement 4
        faction enemies
        type small
        view_bleeding_characters_as_enemies true
    }

    abilities {
        move DefaultMove
        attack BabySharkMelee
        
        spells [

        ]
    }

    passives {
        SharkySmellsBlood 1
    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights stay_close
    }
}
```

---

### `TenTickles`
**Name:** Ten Tickles  
**Source:** `enemies.gon`  

```
TenTickles {
    graphics {
        movieclip TenTickles
        name "ENEMY_TENTICKLES_NAME"
        uifloaters_offset 1.5

        tooltip "ENEMY_TENTICKLES_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag fetus
        faction enemies
        
        movement 20
        health 14
        base_mana_regen 999
        corpse_health 0
    }

    abilities {
        move TenTicklesSwim
        attack TenTicklesAttack
        
        spells [

        ]
    }

    passives {
        TileTrail_Ahead WaterTile
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights chaotic
    }
}
```

---

### `Fetus`
**Name:** Fetus  
**Source:** `enemies.gon`  

```
Fetus {
    graphics {
        movieclip Fetus
        name "ENEMY_FETUS_NAME"

        tooltip "ENEMY_FETUS_DESC"
    }

    stats {
        strength 5
        dexterity 4
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag fetus
        faction enemies
        
        movement 2
        health 12
		initial_health 8
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack BasicShortLobbed_Water
        
        spells [
            DefaultMove
            DrinkUp
        ]
    }

    passives {
        WaterWalk 1

        FormChanger {
            Full {
            }
            Damaged {
                ai {
                    brain PatternBrain

                    pattern {
                        move_then_do_priority [DrinkUp attack]
                    }

                    decision_weights default
                    move_weights keep_distance_always_move_towards_water
                }
            }

            initial_form Full
        }

        FormChangeHealthThreshold {
            threshold X-4      
            form_below Damaged 
            form_above Full    
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [attack DrinkUp]
        }

        decision_weights default
        move_weights keep_distance_always_move_prefer_water
    }
}
```

---

### `FetusGusher`
**Name:** Fetus Gusher  
**Source:** `enemies.gon`  

```
FetusGusher {
    graphics {
        movieclip FetusGusher
        name "ENEMY_FETUSGUSHER_NAME"

        tooltip "ENEMY_FETUSGUSHER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag fetus
        faction enemies
        
        movement 3
        health 12
        base_mana_regen 999
        round_end_bonus_turns 1
    }

    abilities {
        move SwimmerMove
        attack FetusGush
        
        spells [
            DefaultMove
        ]
    }

    passives {
        GroundFlopper DefaultMove
        WaterWalk 1
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `Bat`
**Name:** Bat  
**Source:** `enemies.gon`  

```
Bat {
    graphics {
        movieclip Bat
        name "ENEMY_BAT_NAME"
        default_attack_animation attack2
        move_speed_multiplier 1.75
        uifloaters_offset 1.5
        scale .75

        tooltip "ENEMY_BAT_DESC"
    }

    stats {
        strength 1
        dexterity 5
        constitution 5
        intelligence 5
        speed 8
        charisma 5
        luck 8
    }
    
    properties {
        tag fetus
        faction enemies
        
        movement 6
        health 5

        flying true
    }

    abilities {
        move DefaultMove
        attack BatFlurry
        
        spells [
            
        ]
    }

    passives {
        DodgeChance 50%

        MoveAfterAnyAttemptedAttack {
            weights bat_chaos_runaway
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights keep_distance_always_move
    }
}
```

---

### `BrainDrain`
**Name:** Brain Drain  
**Source:** `enemies.gon`  

```
BrainDrain {
    graphics {
        movieclip MindFetus
        name "ENEMY_BRAINDRAIN_NAME"
        uifloaters_offset 1.75

        tooltip "ENEMY_BRAINDRAIN_DESC"
    }

    stats {
        strength 3
        dexterity 3
        constitution 3
        intelligence 3
        speed 3
        charisma 3
    }
    
    properties {
        tag fetus
        faction enemies
        movement 1
        
        health 8
        flying true
    }

    abilities {
        move DefaultMove
        attack BrainDrainMagicMissile
        
        spells [
            Counterspell
        ]
    }

    passives {
        StatusEachTurnBeginIfHasStatus {
            status Counterspell
            consume true
            animation pulse3

            AllStatsUp 2
            DamageUp 2
            HealthGain 8
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_far
    }
}
```

---

### `SkullOoze`
**Name:** Skull Ooze  
**Source:** `enemies.gon`  

```
SkullOoze {
    graphics {
        movieclip AcidOoze
        name "ENEMY_SKULLOOZE_NAME"

        tooltip "ENEMY_SKULLOOZE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag blob
        health 12
        movement 2
        faction enemies
    }

    abilities {
        move DefaultMove
        attack AcidShot
        
        spells [
        ]
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights keep_distance
    }
}
```

---

### `KirbyFetus`
**Name:** Korbee  
**Source:** `enemies.gon`  

```
KirbyFetus {
    graphics {
        movieclip Kirby
        name "ENEMY_KORBEE_NAME"
        scale .8
        shadow_size .8
        water_mask medium

        tooltip "ENEMY_KORBEE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag fetus
        health 12
        movement 4
        faction enemies
    }

    abilities {
        move DefaultMove
        attack KirbySuck
        
        spells [

        ]
    }

    passives {
        FormChanger {
            Empty {
                animation_suffix ""
            }
            Full {
                animation_suffix "Full"
                attack KirbySpit

                passives {
                    ImmobilePassive 1
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do attack
                    }
                    decision_weights default
                    move_weights keep_distance
                }

                statuses_on_enter_form {
                    UseAbility KirbySpit
                }
            }

            initial_form Empty
        }

        FormChangeWhileHasStatus {
            status Consuming
            form_has Full
            form_hasnot Empty
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `MegaFetus`
**Name:** Mega Fetus  
**Source:** `enemies.gon`  

```
MegaFetus {
    graphics {
        movieclip MegaFetus
        name "ENEMY_MEGAFETUS_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed
        four_way_animations true
        move_speed_sync_frames 35

        tooltip "ENEMY_MEGAFETUS_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
    }
    
    properties {
        tag fetus
        health 25
        movement 3
        faction enemies

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack MegafetusSpin

        spells [
            MegafetusMelee
        ]
    }

    passives {
        Trample 3

        CounterAttack MegafetusMelee
    }
    
    ai {
        brain GenericBrain
        consider_spells false
        decision_weights semi_simple
        move_weights stay_close
    }
}
```

---

### `Tatters`
**Name:** Tatters  
**Source:** `enemies.gon`  

```
Tatters {
    graphics {
        movieclip Tatters
        name "ENEMY_TATTERS_NAME"
        uifloaters_offset 1.3

        tooltip "ENEMY_TATTERS_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [ghost skeleton]
        faction enemies
        movement 5
        health 20
        initial_health 1
        shield 8
        flying true
    }

    abilities {
        move Teleport
        attack TattersLeeches

        spells [
            TattersFear
        ]
    }

    passives {
        CounterAttack TattersFear
        
        Undead 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Spookie`
**Name:** Spookie  
**Source:** `enemies.gon`  

```
Spookie {
    graphics {
        movieclip Spookie
        name "ENEMY_SPOOKIE_NAME"
        spawnin_animation portin

        tooltip "ENEMY_SPOOKIE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag ghost
        faction enemies
        movement 4
        health 9
        flying true
        corpse_health 0
    }

    abilities {
        move Teleport
        attack SpookieLick

        spells [
            DefaultMove
        ]
    }

    passives {
        Undead 1

        CharacterLightSource {
            color [.8, .9, 1]
            size 1.5
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [SpookieLick DefaultMove]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Scary`
**Name:** Scary  
**Source:** `enemies.gon`  

```
Scary {
    graphics {
        movieclip Scary
        name "ENEMY_SCARY_NAME"
        uifloaters_offset 1.5
        spawnin_animation portin

        tooltip "ENEMY_SCARY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag ghost
        faction enemies
        movement 4
        health 14
        flying true
        corpse_health 0
    }

    abilities {
        move Teleport
        attack ScaryFear

        spells [
            ScaryHaunt
        ]
    }

    passives {
        Undead 1

        CharacterLightSource {
            color [.8, .9, 1]
            size 1.7
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_random [ScaryHaunt ScaryFear]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Reaper`
**Name:** Reaper  
**Source:** `enemies.gon`  

```
Reaper {
    graphics {
        movieclip Reaper
        name "ENEMY_REAPER_NAME"
        uifloaters_offset 1.5
        move_speed_multiplier .66

        tooltip "ENEMY_REAPER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [ghost skeleton]
        faction enemies
        movement 2
        health 18
        corpse_health 0
        flying true
    }

    abilities {
        move FloatMove
        attack ReaperSpin

        spells [
            ReaperRevenge
        ]
    }

    passives {
        MoveTowardsKillers ReaperRevenge
        
        Undead 1
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveClose {
                ability move
                move_for_ability attack
                move_weights stay_close_avoid_allies
            }
        }

        pattern {
            do_all [*attack, MoveClose, move]
        }

        decision_weights reaper
        move_weights stay_close_avoid_allies
    }
}
```

---

### `TallRobes`
**Name:** Robes  
**Source:** `enemies.gon`  

```
TallRobes {
    graphics {
        movieclip TallHaunt
        name "ENEMY_TALLROBES_NAME"
        uifloaters_offset 1.5
        projectile_spawn_offset [.25 1.5]

        tooltip "ENEMY_TALLROBES_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [ghost skeleton]
        faction enemies
        movement 3
        health 4
        shield 6
        flying true
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack HexShot

        spells [
            SpawnWisp
            
        ]
    }

    passives {
        Undead 1
        TransformOnDeath Tatters
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [HexShot SpawnWisp]
        }

        decision_weights default
        move_weights stay_near_allies
    }
}
```

---

### `Shambler`
**Name:** Shambler  
**Source:** `enemies.gon`  

```
Shambler {
    graphics {
        movieclip Shambler
        name "ENEMY_SHAMBLER_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed
        move_speed_sync_frames 33

        projectile_spawn_offset [1 2]

        tooltip "ENEMY_SHAMBLER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
    }
    
    properties {
        tag zombie
        health 28
        movement 3
        faction enemies

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack ShamblerDash

        spells [
            ShamblerToss
        ]
    }

    passives {
        Trample 3
        Undead 1
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            DashRandomly {
                ability ShamblerDash
                decision_weights blind
            }
        }

        pattern {
            do_priority [ShamblerToss DashRandomly ShamblerToss]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `GraveWorm`
**Name:** Grave Worm  
**Source:** `enemies.gon`  

```
GraveWorm {
    graphics {
        movieclip GraveWorm
        name "ENEMY_GRAVEWORM_NAME"
        projectile_spawn_offset [.1 1.5]
        uifloaters_offset 1.7
        shadow none
        scale .75
        tooltip "ENEMY_GRAVEWORM_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        health 10
        movement 4
        faction enemies
        corpse_health 0
    }

    abilities {
        move Teleport
        attack BasicRanged
        
        spells [

        ]
    }

    passives {
        MoveWhenDamaged move
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights random
    }
}
```

---

### `ButtZombie`
**Name:** Butt Zombie  
**Source:** `enemies.gon`  

```
ButtZombie {
    graphics {
        movieclip GroundZombie
        name "ENEMY_BUTTZOMBIE_NAME"
        uifloaters_offset 1
        shadow none
        scale .85
        tooltip "ENEMY_BUTTZOMBIE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag zombie
        health 15
        movement 5
        faction enemies
        corpse_health 0
        act_points 4
    }

    abilities {
        move Teleport
        attack BasicMelee
        
        spells [
            ButtFlip
            Spin_Enemy

            TeleportFlipUp
            ButtFart
        ]
    }

    passives {
        FormChanger {
            Up { 
                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights stay_close
                    reset_pattern_on_formswitch true

                    virtual_abilities {
                        MoveClose {
                            ability move
                            move_for_ability Spin_Enemy
                            move_weights stay_close
                        }
                    }

                    pattern {
                        do_all [MoveClose, *attack, *attack, *attack, *attack, attack, attack, attack, attack]
                    }
                }
                passives {
                    AlwaysHitDifferentTargets 1
                    BackstabImmunity 1
                    

                    AbilityReaction {
                        ability ButtFlip
                        ability_damage_only true
                    }
                }
            }
            Down {
                animation_suffix "Down"
                attack ButtFart
                move TeleportFlipUp

                ai {
                    brain PatternBrain
                    decision_weights always_cast
                    move_weights stay_close_always_move
                    auto_orient false
                    reset_pattern_on_formswitch true

                    virtual_abilities {
                        Unflip {
                            ability TeleportFlipUp
                            move_for_ability Spin_Enemy
                            move_weights stay_close_always_move
                        }
                    }

                    pattern {
                        do_all [*ButtFart, Unflip]
                    }
                }
                passives {
                    BackstabAllDirections 1
                }
            }

            initial_form Up
        }
        Undead 1
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `SkeletonShambler`
**Name:** Skeleton Shambler  
**Source:** `enemies.gon`  

```
SkeletonShambler {
    graphics {
        movieclip Shambler
        name "ENEMY_SKELESHAMBLER_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed
        piece_alt_frame 11
        move_speed_sync_frames 33

        projectile_spawn_offset [1 2]
		tooltip "ENEMY_SKELESHAMBLER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
    }
    
    properties {
        tag skeleton

        health 0
        shield 12

        movement 3
        faction enemies

        size 2x2
        move_block everything_even_when_dead

        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack ShamblerDash

        spells [
            ShamblerToss
        ]
    }

    passives {
        Trample 3
        NoHealthOnlyShield 1
        Undead 1
        StatusImmunity [Poison, Bleed]

        TransformOnDeathImmediately {
            obj SkeletonShamblerCorpse
            first_turn keep_turns
        }
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            DashRandomly {
                ability ShamblerDash
                decision_weights blind
            }
        }

        pattern {
            do_priority [ShamblerToss DashRandomly ShamblerToss]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `SkeletonShamblerCorpse`
**Name:** Skeleton Shambler  
**Source:** `enemies.gon`  

```
SkeletonShamblerCorpse {
    graphics {
        movieclip Shambler
        name "ENEMY_SKELESHAMBLERDEAD_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed
        piece_alt_frame 11
        move_speed_sync_frames 33

        projectile_spawn_offset [1 2]
        spawnin_animation disassemble
        alt_animations [[idle idleDisassembled] [weak idleDisassembled] [hit hitDisassembled] [stunned idleDisassembled] [dying dyingDisassembled] [dead empty]]
		tooltip "ENEMY_SKELESHAMBLERDEAD_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
    }

    properties {
        tag skeleton
        health 0
        shield 3

        faction enemies
        corpse_health 0
        can_be_overkilled false

        size 2x2
        move_block everything_even_when_dead
        exclude_from_hallucinate true
    }

    abilities {
        move None
        attack None
    }

    passives {
        NoHealthOnlyShield 1
        Undead 1
        StatusImmunity [Poison, Bleed]
        CountAsCorpse 1

        TransformInXTurns {
            stacks 1
            object SkeletonShamblerRevived
            initiative keep_turns_end_turn
        }
    }
    ai {
        brain NoBrain
    }
}
```

---

### `SkeletonShamblerRevived`
**Source:** `enemies.gon`  

```
SkeletonShamblerRevived {
    variant_of SkeletonShambler
    graphics {
        spawnin_animation reassemble
    }
    properties {
        exclude_from_hallucinate true
    }
}
```

---

### `Thump`
**Name:** Thump  
**Source:** `enemies.gon`  

```
Thump {
    graphics {
        movieclip Thump
        name "ENEMY_THUMP_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed
        four_way_animations true
        scale 1.15
        tooltip "ENEMY_THUMP_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag rock
        health 12
        movement 3
        faction enemies
        corpse_health 0

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move ThumpSlam_Mov
        attack ThumpSlam

        spells [
            
        ]
    }

    passives {
        Trample 3
        DamageFromBehindOnly 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do **ThumpSlam
        }

        decision_weights default
        move_weights stay_close
        auto_orient false
    }
}
```

---

### `FlySwarm`
**Name:** Fly Swarm  
**Source:** `enemies.gon`  

```
FlySwarm {
    graphics {
        movieclip FlySwarm
        name "ENEMY_FLYSWARM_NAME"
        

        tooltip "ENEMY_FLYSWARM_DESC"
    }

    stats {
        strength 1
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag bug
        faction enemies
        
        corpse_health 0
        movement 3
        health 5
        base_mana_regen 999
        flying true
        
        deathpoof_size 1
        can_be_backstabbed false
        weak_threshold 0
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            FormShrinkFour
            FormShrinkThree
            FormShrinkTwo
            FormShrinkOne
        ]
    }

    passives {
        FormChanger {
            5 { 
                partial_animation_suffix 5
                attack BasicMelee_5Hits
                passives {
                    AbilityHealthThreshold {
                        threshold 4*champion_multiplier
                        immediate true
                        even_if_stunned true
                        ability FormShrinkFour
                    }
                }
            }
            4 {
                partial_animation_suffix 4
                attack BasicMelee_4Hits
                passives {
                    AbilityHealthThreshold {
                        threshold 3*champion_multiplier
                        immediate true
                        even_if_stunned true
                        ability FormShrinkThree
                    }
                }
            }
            3 {
                partial_animation_suffix 3
                attack BasicMelee_3Hits
                passives {
                    AbilityHealthThreshold {
                        threshold 2*champion_multiplier
                        immediate true
                        even_if_stunned true
                        ability FormShrinkTwo
                    }
                }
            }
            2 {
                partial_animation_suffix 2
                attack BasicMelee_2Hits
                passives {
                    AbilityHealthThreshold {
                        threshold 1*champion_multiplier
                        immediate true
                        even_if_stunned true
                        ability FormShrinkOne
                    }
                }
            }
            1 {
                passives {

                }
            }

            initial_form 5
        }
        LimitDamage 1
        LimitHeal 1
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
        consider_spells false
    }
}
```

---

### `NonChampionFlySwarm`
**Source:** `enemies.gon`  

```
NonChampionFlySwarm {
    variant_of FlySwarm
    properties {
        can_be_champion false
    }
}
```

---

### `SnakeyBones`
**Name:** Bone Worm  
**Source:** `enemies.gon`  

```
SnakeyBones {
    graphics {
        movieclip SnakeyBones
        name "ENEMY_BONEWORM_NAME"
        scale .85
        tooltip "ENEMY_BONEWORM_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [worm skeleton]
        auto_run_priority stationary
        health 0
        shield 8
        faction enemies
        corpse_health 0
        can_be_overkilled false
    }

    abilities {
        move None
        attack 
        BoneWormShotSmall
        
        spells [
            FormShrinkTwoSnakey
            FormShrinkOneSnakey
            FormGrowTwoSnakey
            FormGrowThreeSnakey
            FormGrowTwo
            FormGrowThree
        ]
    }

    passives {
        NoHealthOnlyShield 1
        Undead 1
        StatusImmunity [Poison, Bleed]
        PrioritizeHitDifferentTargets 1

        FormChanger {
            3 {
                partial_animation_suffix 3
                uifloaters_offset 3

                attack BoneWormShotTall
                passives {
                    LimitDamage 1
                    ImmediateAbilityReaction {
                        even_if_stunned true
                        ability FormShrinkTwoSnakey
                    }
                    Tall 1
                }

                ai {
                    brain PatternBrain

                    mainturn_pattern {
                        do_all [attack, attack]
                    }

                    auto_orient false
                    decision_weights default
                    move_weights keep_distance
                }
            }
            2 {
                partial_animation_suffix 2
                uifloaters_offset 2.2

                attack BoneWormShotMed
                passives {
                    LimitDamage 1
                    ImmediateAbilityReaction {
                        even_if_stunned true
                        ability FormShrinkOneSnakey
                    }
                }

                ai {
                    brain PatternBrain

                    mainturn_pattern {
                        do_all [attack, FormGrowThreeSnakey]
                    }

                    auto_orient false
                    decision_weights default
                    move_weights keep_distance
                }
            }
            1 {
                partial_animation_suffix 1
                uifloaters_offset 1.4

                passives {
                    
                }

                ai {
                    brain PatternBrain

                    mainturn_pattern {
                        do_all [attack, FormGrowTwoSnakey]
                    }

                    auto_orient false
                    decision_weights default
                    move_weights keep_distance
                }
            }

            initial_form 1
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Carcus`
**Name:** Carcass  
**Source:** `enemies.gon`  

```
Carcus {
    graphics {
        movieclip Carcus
        name "ENEMY_CARCASS_NAME"
        water_mask medium
        scale .85

        tooltip "ENEMY_CARCASS_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 0
        charisma 5
    }
    
    properties {
        tag animal
        health 1
        movement 0
        faction enemies
        corpse_health 0
        can_be_backstabbed false
    }

    abilities {
        move None
        attack CarcusSpawn
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        auto_orient false
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Peashy`
**Name:** Peashy  
**Source:** `enemies.gon`  

```
Peashy {
    graphics {
        movieclip Peashy
        name "ENEMY_PEASHY_NAME"
        uifloaters_offset 1.5
        scale .75

        tooltip "ENEMY_PEASHY_DESC"
    }

    stats {
        strength 5
        dexterity 4
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag plant
        faction enemies
        
        movement 3
        health 14
    }

    abilities {
        move DefaultMove
        attack BasicStraightShot
        
        spells [
            GenericRage
            PeashyStab
        ]
    }

    passives {
        Thorns 1
        FaceShield 0

        FormChanger {
            Default { 
                passives {
                    StatusOnKill {
                        HealthGain 5
                        UseAbility_NonStack GenericRage
                    }
                }
            }
            Rage {
                animation_suffix "Rage"
                move_speed_multiplier 2

                ai {
                    brain PatternBrain
                    decision_weights peashy_rage
                    move_weights stay_close_always_move

                    pattern {
                        do_priority [PeashyStab, attack]
                    }
                }
                passives {
                    StatusOnKill {
                        HealthGain 5
                    }
                }
            }

            initial_form Default
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights peashy
        move_weights keep_distance_always_move
        consider_spells false
    }
}
```

---

### `BabyDeathWorm`
**Name:** Baby Deathworm  
**Source:** `enemies.gon`  

```
BabyDeathWorm {
    graphics {
        movieclip BabyDeathWorm
        name "ENEMY_BABYDEATHWORM_NAME"
        shadow none
		tooltip "ENEMY_BABYDEATHWORM_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        faction enemies
        
        movement 4
        health 8
        corpse_health 0
    }

    abilities {
        move Teleport
        attack Dash_BabyDeathWorm
        
        spells [

        ]
    }

    passives {
        MovementReaction {
            ability Dash_BabyDeathWorm
            blind_spot true
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do move
        }

        decision_weights default
        move_weights keep_distance_always_move
        consider_spells false
    }
}
```

---

### `DeathWorm`
**Name:** Death Worm  
**Source:** `enemies.gon`  

```
DeathWorm {
    graphics {
        movieclip DeathWorm
        name "ENEMY_DEATHWORM_NAME"
        shadow none
        uifloaters_offset 1
        water_mask medium
		tooltip "ENEMY_DEATHWORM_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        faction enemies
        movement 1

        health 15

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack DeathWormTrampleDash
        
        spells [
            DeathWormEat
            DeathWormReturn
            DeathWormTrampleDash_Reaction
        ]
    }

    passives {
        Trample 3
        CounterAttack DeathWormTrampleDash_Reaction
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [DeathWormReturn, *attack, attack, move]
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `Cultist`
**Name:** Cultist  
**Source:** `enemies.gon`  

```
Cultist {
    graphics {
        movieclip BunkerBoy
        name "ENEMY_CULTIST_NAME"
        uifloaters_offset 2
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag humanoid
        faction enemies
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            BBPickupCrown
            BBSpin
            BBCut
            BBPullBomb
            BBTransformMutant
            BBTransformZealot
            BBToss
            BBBless
        ]
    }

    passives {
        FormChanger {
            Cultist {
                animation_suffix "Cultist"
                attack BasicMelee
                name "ENEMY_CULTISTLACKEY_NAME"
                tooltip "ENEMY_CULTISTLACKEY_DESC"

                passives {
                    TagGreed bishop_hat

                    StatusOnKill {
                        UseAbility_NonStack BBTransformZealot
                    }

                    MutateViaAbility BBTransformMutant
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [BBPickupCrown, attack, BBToss]
                        do_priority [BBPickupCrown, BBToss, attack]
                    }

                    decision_weights default
                    move_weights stay_close
                    end_turn_on_formswitch true
                    randomize_pattern_start true
                }
            }
            Zealot {
                animation_suffix "Zealot"
                attack BBStabby
                name "ENEMY_CULTISTZEALOT_NAME"
				tooltip "ENEMY_CULTISTZEALOT_DESC"

                passives {
                    TagGreed bishop_hat

                    AbilityHealthThreshold {
                        threshold "max(X*.33, 5)"
                        ability BBPullBomb
                    }

                    MutateViaAbility BBTransformMutant
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [BBPickupCrown, attack, BBSpin, BBCut]
                        do_priority [BBPickupCrown, BBSpin, attack, BBCut]
                    }

                    decision_weights default
                    move_weights stay_close
                    end_turn_on_formswitch true
                    randomize_pattern_start true
                }
            }
            ZealotBomb {
                animation_suffix "BombZealot"
                attack BBExplode
                name "ENEMY_BOMBZEALOT_NAME"
				tooltip "ENEMY_BOMBZEALOT_DESC"

                passives {
                    DeathRattle BBExplode
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do attack
                    }

                    decision_weights extra_careless
                    move_weights stay_close
                    end_turn_on_formswitch true
                }
            }
            Mutant {
                animation_suffix "Mutant"
                attack BBMutantSwipe
                move_speed_multiplier .5
                name "ENEMY_CULTISTMUTANT_NAME"
				tooltip "ENEMY_CULTISTMUTANT_DESC"

                passives {
                    AddMovement -2
                    AddTag tumor

                    AddCorpseHealth -999
                    TransformOnDeath [Hive FloatingHive]
                }

                turns {
                    dispersed_bonus_turns 1
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do attack
                    }

                    decision_weights default
                    move_weights stay_close
                    end_turn_on_formswitch true
                }
            }
            Bishop {
                animation_suffix "Bishop"
                attack BBXLightning
                uifloaters_offset 2.5
                name "ENEMY_CULTISTBISHOP_NAME"
                tooltip "ENEMY_CULTISTBISHOP_DESC"

                passives {
                    Flying 1

                    AddCorpseHealth -999
                    TransformOnDeath BishopHat
                }

                turns {
                    dispersed_bonus_turns 1
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [attack, BBBless]
                        do_priority [BBBless, attack]
                    }

                    decision_weights default
                    move_weights stay_close
                    end_turn_on_formswitch true
                }
            }

            Washer { 
                partial_animation_suffix "Cultist"
                attack BasicMelee
                name "ENEMY_CULTISTWASHER_NAME"
				tooltip "ENEMY_CULTISTWASHER_DESC"

                passives {
                    TagGreed bishop_hat
                    StatusOnKill {
                        UseAbility_NonStack BBTransformZealot
                    }
                    MutateViaAbility BBTransformMutant
                    JohnnyWasher BBTransformZealot
                    AddMovement -2
                }

                ai {
                    brain PatternBrain

                    pattern {
                        move_then_do_priority [BBPickupCrown, *attack, *BBToss]
                        move_then_do_priority [BBPickupCrown, *BBToss, *attack]
                    }

                    decision_weights default
                    move_weights wash_johnny
                    end_turn_on_formswitch true
                    randomize_pattern_start true
                }
            }

            initial_form Cultist
        }
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `CultistZealot`
**Source:** `enemies.gon`  

```
CultistZealot {
    variant_of Cultist
	
    passives {
       FormChanger {
           initial_form Zealot
       }
    }
}
```

---

### `CultistMutant`
**Source:** `enemies.gon`  

```
CultistMutant {
    variant_of Cultist

    properties {
        hint_no_corpse true
    }

    passives {
        FormChanger {
            initial_form Mutant
        }
        Brace 2 
    }
}
```

---

### `CultistBishop`
**Source:** `enemies.gon`  

```
CultistBishop {
    variant_of Cultist

    properties {
        hint_no_corpse true
    }

    passives {
        FormChanger {
            initial_form Bishop
        }
        DivineShield 2 
        KineticSpikes 1
    }
}
```

---

### `CultistWasher`
**Source:** `enemies.gon`  

```
CultistWasher {
    variant_of Cultist
    passives {
        FormChanger {
            initial_form Washer
        }
    }
}
```

---

### `BishopHat`
**Name:** Bishop Hat  
**Source:** `enemies.gon`  

```
BishopHat {
    graphics {
        movieclip BishopHat
        name "ENEMY_BISHOPHAT_NAME"
        tooltip "ENEMY_BISHOPHAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag bishop_hat
        faction enemies
        takes_turns false
        can_be_champion false
        health 1
        shield 5
        kill_required false
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack None
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `LoveBot`
**Name:** Love Bot  
**Source:** `enemies.gon`  

```
LoveBot {
    graphics {
        movieclip LoveBot
        name "ENEMY_LOVEBOT_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_LOVEBOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag robot
        faction enemies
        auto_run_priority support

        health 0
        shield 13
        can_be_overkilled false

        banned_elite_buffs [Mad]
    }

    abilities {
        move DefaultMove
        attack LoveBotHeal

        spells [
            LoveBotCounter
        ]
    }

    passives {
        Brace 1
        NoHealthOnlyShield 1
        Robot 1
        CounterAttack LoveBotCounter
    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights stay_near_allies
        consider_spells false
    }
}
```

---

### `SecurityBot`
**Name:** Security Bot  
**Source:** `enemies.gon`  

```
SecurityBot {
    graphics {
        movieclip SecurityBot
        name "ENEMY_SECURITYBOT_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_SECURITYBOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag robot
        faction enemies
        auto_run_priority support

        health 0
        shield 12
        can_be_overkilled false
        movement 1
    }

    abilities {
        move DefaultMove
        attack SBotAttack

        spells [
            SBotAngryMove
            SBotRecharge
            SBotAnger
        ]
    }

    passives {
        Brace 2
        NoHealthOnlyShield 1
        Robot 1
        SecurityBotProtect {
            ability attack
            move SBotAngryMove
        }

        FormChanger {
            Default {
            }
            Angry {
                partial_animation_suffix "Angry"

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [attack, *SBotRecharge]
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }
        }

        SupportFormChangeInsteadOfRun {
            ability SBotAnger
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do *SBotRecharge
        }

        decision_weights default
        move_weights security_bot
    }
}
```

---

### `KillDozer`
**Name:** Killdozer  
**Source:** `enemies.gon`  

```
KillDozer {
    graphics {
        movieclip KillDozer
        name "ENEMY_KILLDOZER_NAME"
        water_mask square
        uifloaters_offset 2
        move_speed_sync_frames 48
		tooltip "ENEMY_KILLDOZER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid robot]
        faction enemies
        movement 2
        mana_regen 999
        mana 100
        
        health 8
        shield 14

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack KillDoze
        
        spells [
            MoveOne
        ]
    }

    passives {
        Trample 3
        MoveTowardsDamageSource MoveOne
        Robot 1
        Brace 2
        Thorns 3
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights stay_close
        auto_orient false
        
        mainturn_pattern {
            do KillDoze
        }
    }
}
```

---

### `Carnibulb`
**Name:** Carnibulb  
**Source:** `enemies.gon`  

```
Carnibulb {
    graphics {
        movieclip Carnibulb
        name "ENEMY_CARNIBULB_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed

        tooltip "ENEMY_CARNIBULB_DESC"
        show_infinity_damage_warning true
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 0
        charisma 5
    }
    
    properties {
        tag plant
        health 22
        movement 1
        faction enemies

        size 2x2
        move_block everything_even_when_dead
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack CarnibulbEat

        spells [
            Sprout
        ]
    }

    passives {
        Trample 3
        Plant 1
        ElementImmune Creep

        AddMovement -1 
        SproutsGrantMovement 1
    }
    
    ai {
        brain PatternBrain
        pattern {
            do_priority [*CarnibulbEat CarnibulbEat *Sprout]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Sprout`
**Name:** Sprout  
**Source:** `enemies.gon`  

```
Sprout {
    graphics {
        movieclip Sprout
        name "ENEMY_SPROUT_NAME"
        uifloaters_offset 1.5
		scale .8
		tooltip "ENEMY_SPROUT_DESC" 
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag plant
        hidden_tag sprout
        type small
        faction enemies

        health 1
        initiative -999
        can_be_backstabbed false
        corpse_health 0
    }

    abilities {
        move None
        attack SproutSpore
    }

    passives {
        Plant 1
        ElementImmune Creep
    }
    
    ai {
        brain GenericBrain
        decision_weights always_cast
        move_weights stay_close
    }
}
```

---

### `GeoLad`
**Name:** GeoLad  
**Source:** `enemies.gon`  

```
GeoLad {
    graphics {
        movieclip GeoLad
        name "ENEMY_GEOLAD_NAME"
        tooltip "ENEMY_GEOLAD_DESC"
        no_splatter true
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag rock
        faction enemies

        health 4
        shield 8
        can_be_backstabbed false
        corpse_health 0
        movement 2
    }

    abilities {
        move DefaultMove
        attack BasicMelee

        spells [
            QuakeJump
        ]
    }

    passives {
        Brace 1
        AddStatusToBasicAttack {
            Stun 1
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*attack, QuakeJump, attack]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `BrambleBaby`
**Name:** Bramble Baby  
**Source:** `enemies.gon`  

```
BrambleBaby {
    graphics {
        movieclip BrambleBaby
        name "ENEMY_BRAMBLEBABY_NAME"
        tooltip "ENEMY_BRAMBLEBABY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag plant
        faction enemies

        health 8
    }

    abilities {
        move Teleport
        attack BramblePull

        spells [
            BrambleBabyEntangle
        ]
    }

    passives {
        Plant 1
        ElementImmune Creep
        Thorns 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*attack, move, BrambleBabyEntangle]
        }

        decision_weights default
        move_weights chaotic
    }
}
```

---

### `Hemlock`
**Name:** Hemlock  
**Source:** `enemies.gon`  

```
Hemlock {
    graphics {
        movieclip Hemlock
        name "ENEMY_HEMLOCK_NAME"
        tooltip "ENEMY_HEMLOCK_DESC"
        uifloaters_offset 2
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag plant
        faction enemies
        flying true
        auto_run_priority support

        health 10
    }

    abilities {
        move DefaultMove
        attack HemShot

        spells [
            HemBounce
            HemDeathPop
            HemHeal
        ]
    }

    passives {
        Plant 1
        ElementImmune Creep
        AbilityReaction HemBounce
        TowerDefenseReflex attack
        /*DeathRattle {
            ability HemDeathPop
            pop_corpse false
            is_dying_animation true
        }*/
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [move HemHeal]
        }

        decision_weights default
        move_weights stay_near_allies
    }
}
```

---

### `Nettle`
**Name:** Nettle  
**Source:** `enemies.gon`  

```
Nettle {
    graphics {
        movieclip Nettle
        name "ENEMY_NETTLE_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_NETTLE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag plant
        faction enemies

        health 11
    }

    abilities {
        move DefaultMove
        attack BasicMelee

        spells [
            ThornUp
        ]
    }

    passives {
        Plant 1
        ElementImmune Creep
        AbilityAfterEnemyCastSpell_Stackable ThornUp
        
        AddStatusToBasicAttack {
            Bleed 1
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Birthwort`
**Name:** Birthwort  
**Source:** `enemies.gon`  

```
Birthwort {
    graphics {
        movieclip Birthwort
        name "ENEMY_BIRTHWORT_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_BIRTHWORT_DESC" 
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag plant
        faction enemies

        health 24
        initial_health 18
        movement 2
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicMelee

        spells [
            BirthwortReactionShot
            BirthwortTrample
            BirthwortHeal
        ]
    }

    passives {
        Plant 1
        ElementImmune Creep
        ImmediateAbilityReaction BirthwortReactionShot
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            ForceTrample {
                ability BirthwortTrample
                decision_weights always_cast_careless
            }
        }

        pattern {
            do_all [*attack *BirthwortTrample move ForceTrample *attack BirthwortHeal]
        }

        decision_weights careless
        move_weights blind_move_far
    }
}
```

---

### `Amoeba`
**Name:** Amoeba  
**Source:** `enemies.gon`  

```
Amoeba {
    graphics {
        movieclip Amoeba
        name "ENEMY_AMOEBA_NAME"
        tooltip "ENEMY_AMOEBA_DESC"
        shadow_size .5
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag blob
        faction enemies

        health 3
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack AmoebaAttach

        spells [
            PickupRock
        ]
    }

    passives {
        FormChangeWhileHasStatus {
            status Consuming
            form_has HasRock
            form_hasnot Default
        }

        FormChanger {
            Default {
                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [PickupRock attack]
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }
            HasRock {
                animation_suffix "rock"

                attack AmoebaRockBash

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [attack]
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }

            initial_form Default
        }
    }
    
    ai {
        brain NoBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Tremblo`
**Name:** Tremblo  
**Source:** `enemies.gon`  

```
Tremblo {
    graphics {
        movieclip Tremblo
        name "ENEMY_TREMBLO_NAME"
        tooltip "ENEMY_TREMBLO_DESC"
        uifloaters_offset 1.5
        no_splatter true
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag rock
        faction enemies

        health 4
        shield 10
        can_be_backstabbed false
        corpse_health 0
        movement 2
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack TrembloSmash

        spells [
            TrembloSuck
            TrembloEat
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do attack
        }
        bonusturn_pattern {
            do_all [TrembloSuck *TrembloEat TrembloEat]
        }
        fallback {
            do_priority [attack TrembloEat]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `CraterCreeper`
**Name:** Crater Creeper  
**Source:** `enemies.gon`  

```
CraterCreeper {
    graphics {
        movieclip CanCreeper
        name "ENEMY_CRATERCREEPER_NAME"
        water_mask medmed
        piece_alt_frame 11

        tooltip "ENEMY_CRATERCREEPER_DESC"
    }

    sound {
        alt_sounds [[DamageBlocked DamageBlocked_CanCreeper]]
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [blob rock]
        faction enemies
        dispersed_bonus_turns 1
        movement 3
        corpse_health 0

        
        mana_regen 999
        mana 100
        
        health 8
		shield 8
        always_triggers_traps true
    }

    abilities {
        move DefaultMove
        attack CraterCreeperRockBlast
        
        spells [
            CraterCreeperSlide
        ]
    }

    passives {
        SpawnCreepOnHit 1
        SpawnCreepOnHitKnockback 1
        CanShield 1
        IgnoreTiles 1
        ChangeTileOnPop CreepTile
        TransformOnDeath CraterCreeperOut
        ElementImmune Creep
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveCenter {
                ability move
                move_weights stay_near_map_center
            }
        }

        mainturn_pattern {
            do attack
        }


        bonusturn_pattern {
            do_strict [*CraterCreeperSlide, MoveCenter]
        }

        decision_weights default
        move_weights stay_close_always_move
        auto_orient false
    }
}
```

---

### `CraterCreeperOut`
**Name:** Crater Creeper  
**Source:** `enemies.gon`  

```
CraterCreeperOut {
    graphics {
        movieclip CanCreeperOut
        name "ENEMY_CRATERCREEPER2_NAME"
        projectile_spawn_offset [0 1]

        tooltip "ENEMY_CRATERCREEPER2_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 8
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies
        dispersed_bonus_turns 1
        corpse_health 1

        
        mana_regen 999
        mana 100
        
        health 8
    }

    abilities {
        move Swim
        attack ShortCreepshotCrater
        
        spells [
            MoveOne
        ]
    }

    passives {
        GroundFlopper MoveOne
        WaterWalk 1
        ElementImmune Creep
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `CoreFreak`
**Name:** Core Freak  
**Source:** `enemies.gon`  

```
CoreFreak {
    graphics {
        movieclip CoreFreak
        name "ENEMY_COREFREAK_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_COREFREAK_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [humanoid tumor]
        faction enemies
        movement 2
		health 14
    }

    abilities {
        move DefaultMove
        attack CoreFreakAttack
        
        spells [
            CoreFreakFury
        ]
    }

    passives {
        
    }
    
    ai {
        virtual_abilities {
            MoveAway {
                ability move
                move_weights blind_move_far
            }
        }

        pattern {
            do_strict [*attack, MoveAway, *CoreFreakFury]
        }
        fallback {
            do_all [move, *CoreFreakFury]
        }

        brain PatternBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `PokerDemon`
**Name:** Hot Poker  
**Source:** `enemies.gon`  

```
PokerDemon {
    graphics {
        movieclip PokerDemon
        name "ENEMY_HOTPOKER_NAME"
        uifloaters_offset 2
        scale .8

        tooltip "ENEMY_HOTPOKER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [demon]
        faction enemies
        health 11
        movement 3
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack PokerAttack
        
        spells [
            PokerPokeCat
            PokerPokeAlly
        ]
    }

    passives {
        AlwaysHitDifferentTargets 1
        ElementImmune Fire
    }
    
    ai {
        pattern {
            do_strict [attack, PokerPokeCat]
        }

        fallback {
            do PokerPokeAlly
        }

        brain PatternBrain
        decision_weights default
        move_weights stay_close_move_far
    }
}
```

---

### `Whisperer`
**Name:** Whisperer  
**Source:** `enemies.gon`  

```
Whisperer {
    graphics {
        movieclip Whisperer
        name "ENEMY_WHISPERER_NAME"
        uifloaters_offset 2
        move_speed_multiplier .5
		tooltip "ENEMY_WHISPERER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [humanoid tumor]
        faction enemies
        movement 2
		health 14
    }

    abilities {
        move DefaultMove
        attack WhispererThrowDamage
        
        spells [
            WhispererThrowBuff
            WhispererWhisper
        ]
    }

    passives {
    }
    
    ai {
        pattern {
            do_priority [WhispererWhisper, WhispererThrowDamage, WhispererThrowBuff]
        }


        brain PatternBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `CloakedDemon`
**Name:** Cloaked Demon  
**Source:** `enemies.gon`  

```
CloakedDemon {
    graphics {
        movieclip CloakedDemon
        name "ENEMY_CLOAKEDDEMON_NAME"
        uifloaters_offset 2

        tooltip "ENEMY_CLOAKEDDEMON_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag demon
        faction enemies
        movement 2
        dispersed_bonus_turns 1
		health 13
    }

    abilities {
        move DefaultMove
        attack CloakerHex
        
        spells [
            TwistingFlames
        ]
    }

    passives {
        ElementImmune Fire
        CounterAttack CloakerHex
    }
    
    ai {

        virtual_abilities {
            TF_TargetEnemies {
                ability TwistingFlames
                decision_weights util_target_enemies
            }
            TF_TargetAllies {
                ability TwistingFlames
                decision_weights util_target_allies
            }
        }

        pattern {
            do_priority [TF_TargetEnemies TF_TargetAllies]
            do_priority [TF_TargetAllies TF_TargetEnemies]
        }


        brain PatternBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `BigDemon`
**Name:** Brute  
**Source:** `enemies.gon`  

```
BigDemon {
    graphics {
        movieclip BigDemon
        name "ENEMY_BRUTE_NAME"
        uifloaters_offset 2

        tooltip "ENEMY_BRUTE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag demon
        faction enemies
        health 20
        movement 2
    }

    abilities {
        move DefaultMove
        attack DemonUppercut
        
        spells [
            DemonRockThrow
            NeckSnap
        ]
    }

    passives {
        ElementImmune Fire
    }
    
    ai {
        pattern {
            do_all [NeckSnap DemonUppercut *DemonRockThrow move]
        }

        brain PatternBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `MegaTumor`
**Name:** Mega Tumor  
**Source:** `enemies.gon`  

```
MegaTumor {
    graphics {
        movieclip MegaTumor
        name "ENEMY_MEGATUMOR_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed
        move_speed_multiplier .5

        tooltip "ENEMY_MEGATUMOR_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag tumor
        health 20
        movement 1
        faction enemies
        can_be_backstabbed false

        size 2x2
        lock_orientation [0, -1]
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack TumorDash

        spells [
            TumorPowerup
        ]
    }

    passives {
        Trample 3
        Brace 2

        ElementImmune Fire
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [move TumorDash *TumorPowerup]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `HeadTumor`
**Name:** Tumorhead  
**Source:** `enemies.gon`  

```
HeadTumor {
    graphics {
        movieclip HeadTumor
        name "ENEMY_TUMORHEAD_NAME"
        scale .8
		tooltip "ENEMY_TUMORHEAD_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [humanoid tumor]
        faction enemies
        movement 2
        health 10
    }

    abilities {
        move DefaultMove
        attack HeadTumorAttack
        
        spells [
            HeadTumorResponse
        ]
    }

    passives {
        Brace 1
        AbilityReaction HeadTumorResponse
    }
    
    ai {
        pattern {
            do attack
        }

        brain PatternBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `TallTumor`
**Name:** Tall Tumor  
**Source:** `enemies.gon`  

```
TallTumor {
    graphics {
        movieclip TallTumor
        name "ENEMY_TALLTUMOR_NAME"
        uifloaters_offset 2.5
        move_speed_multiplier .5

        tooltip "ENEMY_TALLTUMOR_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag tumor
        faction enemies
        movement 2
        initial_health 8
        health 16

        auto_run_priority support
    }

    abilities {
        move DefaultMove
        attack TT_Thrash
        
        spells [
            TT_ManaBurn
        ]
    }

    passives {
        CounterAttack TT_Thrash
        TallTumorManaBurn TT_ManaBurn
    }
    
    ai {
        pattern {
            do move
        }

        brain PatternBrain
        decision_weights careless
        move_weights stay_far
    }
}
```

---

### `BigAsteroid`
**Name:** Big Asteroid  
**Source:** `enemies.gon`  

```
BigAsteroid {
    graphics {
        movieclip BigAsteroid
        name "ENEMY_BIGASTEROID_NAME"

        uifloaters_offset 1.5
		tooltip "ENEMY_BIGASTEROID_DESC" 
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag rock
        faction enemies
        health 5
        shield 7
        movement 2

        flying true
    }

    abilities {
        move DefaultMove
        attack BigAsteroidBarrage
        
        spells [
        ]
    }

    passives {
        SmallRockBehavior {
            damage 9
            knockback 2 
            chain true
        }
        LimitDamage 1
        LimitHeal 0
        StripStatuses 1
        
    }
    
    ai {
        brain GenericBrain
        decision_weights careless
        move_weights stay_close
    }
}
```

---

### `SmallAsteroid`
**Name:** Small Asteroid  
**Source:** `enemies.gon`  

```
SmallAsteroid {
    graphics {
        movieclip SmallAsteroid
        name "ENEMY_SMALLASTEROID_NAME"

        uifloaters_offset 1
		tooltip "ENEMY_SMALLASTEROID_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag rock
        faction enemies
        health 1
        shield 3
        movement 3

        flying true
    }

    abilities {
        move DefaultMove
        attack SmallAsteroidBarrage
        
        spells [
        ]
    }

    passives {
        SmallRockBehavior {
            damage 5
            knockback 5 
            chain true
        }
        LimitDamage 1
        LimitHeal 0
        StripStatuses 1
        
    }
    
    ai {
        brain GenericBrain
        decision_weights careless
        move_weights stay_close
    }
}
```

---

### `SmallUFO`
**Name:** Saucie  
**Source:** `enemies.gon`  

```
SmallUFO {
    graphics {
        movieclip SmallUFO
        name "ENEMY_SAUCIE_NAME"
		tooltip "ENEMY_SAUCIE_DESC"
        projectile_spawn_offset [0 .5]
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [alien robot]
        faction enemies
        health 6
		shield 6
        movement 1

        flying true
        dispersed_bonus_turns 2
    }

    abilities {
        move DefaultMove
        attack UFO_CrossLasers
        
        spells [
            UFO_Detect
            UFO_Shield
        ]
    }

    passives {
        Robot 1
        DeathRattle {
            ability UFO_SpelunkyDeath
            immediate true
            cancel_knockback true
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [UFO_CrossLasers, UFO_Detect, UFO_Shield]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `BigUFO`
**Name:** Megasaucer  
**Source:** `enemies.gon`  

```
BigUFO {
    graphics {
        movieclip BigUFO
        name "ENEMY_MEGASAUCER_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_MEGASAUCER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [alien robot]
        faction enemies
        movement 2
        flying true
        
        health 6
		shield 10
        divine_shield 3

        corpse_health 0

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack UFO_Dash
        
        spells [
            UFO_Megalaser
            UFO_Summon
            UFO_BigShield
        ]
    }

    passives {
        Trample 3
        Robot 1
        DeathRattle UFO_BigExplode
        LoopingSoundWhileAlive BigUFO_ambient_looping
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights keep_distance
        auto_orient false
        
        pattern {
            do_random [UFO_Summon UFO_Dash UFO_Megalaser]
        }
        fallback {
            do UFO_BigShield
        }
    }
}
```

---

### `YellowBlaster`
**Name:** Y-Blaster  
**Source:** `enemies.gon`  

```
YellowBlaster {
    graphics {
        movieclip YellowBlaster
        name "ENEMY_YBLASTER_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_YBLASTER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [alien]
        faction enemies
        health 12
        movement 3
        auto_run_priority support
    }

    abilities {
        move DefaultMove
        attack YA_Laser
        
        spells [
            YA_Charge
            YA_Jetpack
        ]
    }

    passives {
        Trapper {
            ability YA_Laser
            range 10
            cancel_movement false
        }
        MoveAwayWhenEnemyAdjacent {
            move_ability YA_Jetpack
            weights stay_far_always_move
            once_per_turn true
        }

        FormChanger {
            Default {
            }
            Attacker {
                ai {
                    brain PatternBrain

                    pattern {
                        do_all [attack, YA_Charge]
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
        }

        SupportFormChangeInsteadOfRun Attacker
    }
    
    ai {
        brain PatternBrain

        pattern {
            do *YA_Charge
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `GreyAlien`
**Name:** G-Alien  
**Source:** `enemies.gon`  

```
GreyAlien {
    graphics {
        movieclip GreyAlien
        name "ENEMY_GALIEN_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_GALIEN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [alien]
        faction enemies
        health 10
        movement 3
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack GA_Telekinesis
        
        spells [
            GA_Counterspell
            GA_Megablast
            GA_Suggest

            GA_PrimeExplode
        ]
    }

    passives {
        FormChanger {
            Default {
                ai {
                    brain PatternBrain

                    pattern {
                        do_all [attack move *GA_Counterspell]
                        do_all [GA_Suggest move *GA_Counterspell]
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
            Primed {
                attack GA_Telekinesis_Big
                partial_animation_suffix primed

                ai {
                    brain PatternBrain

                    pattern {
                        do_all [attack]
                        do_all [GA_Megablast move]
                    }

                    decision_weights default
                    move_weights keep_distance
                }

                passives {
                    DeathRattle GA_PrimeExplode
                }
            }

            sync_brain_patterns true
        }

        FormChangeWhileHasStatus {
            status Counterspell
            form_has Primed
            form_hasnot Default
        }
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `GreenProber`
**Name:** B-Prober  
**Source:** `enemies.gon`  

```
GreenProber {
    graphics {
        movieclip GreenProber
        name "ENEMY_BPROBER_NAME"
        uifloaters_offset 1.5
        scale .9
		tooltip "ENEMY_BPROBER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [alien]
        faction enemies
        health 10
        movement 3
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            GP_Probe
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [GP_Probe attack]
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `Waggle`
**Name:** Waggle  
**Source:** `enemies.gon`  

```
Waggle {
    graphics {
        movieclip Waggle
        name "ENEMY_WAGGLE_NAME"
		tooltip "ENEMY_WAGGLE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [blob]
        faction enemies
        health 7
        movement 3
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            WaggleClone
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [attack WaggleClone]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `cWaggle`
**Source:** `enemies.gon`  

```
cWaggle {
    variant_of Waggle
    graphics {
        spawnin_animation spawn
    }
}
```

---

### `cWaggle2x2`
**Source:** `enemies.gon`  

```
cWaggle2x2 {
    variant_of cWaggle

    graphics {
        scale 2.5
    }
    
    stats {
        strength 10
    }
    abilities {
        attack BasicBigMelee
    }
    passives {
        Trample 3
    }
    properties {
        health 18
        size 2x2
        move_block everything_even_when_dead
    }
}
```

---

### `cWaggle3x3`
**Source:** `enemies.gon`  

```
cWaggle3x3 {
    variant_of cWaggle2x2

    graphics {
        scale 4
        uifloaters_offset 2
        tooltip "ENEMY_3X3WAGGLE_DESC"
    }
    stats {
        strength 15
    }
    properties {
        health 40
        size 3x3
    }
}
```

---

### `RatCat`
**Name:** Half-Rat  
**Source:** `enemies.gon`  

```
RatCat {
    graphics {
        movieclip RatCat
        name "ENEMY_HALFRAT_NAME"
        shadow_size .70
		tooltip "ENEMY_HALFRAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [rat cat]
        faction enemies
        
        movement 1
        health 10
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack ChainDash
        
        spells [

        ]
    }

    passives {
        AddStatusToBasicAttack {
            GainDisorderFromPool {
                pool diseases
                chance .1
            }
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights keep_distance_always_move
    }
}
```

---

### `Gamete`
**Name:** Gamete  
**Source:** `enemies.gon`  

```
Gamete {
    graphics {
        movieclip Gamete
        name "ENEMY_GAMETE_NAME"
        scale .8
        move_speed_sync_frames 41
		tooltip "ENEMY_GAMETE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies
        
        movement 4
        health 8
        base_mana_regen 999
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [
            GametePop
        ]
    }

    passives {
        FormChanger {
            Small {
                attack GameteInflate
            }
            Big {
                animation_suffix Big
                attack GameteSpawn

                passives {
                    DeathRattle GametePop
                }
            }
            initial_form Small
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights always_cast
        move_weights stay_far_always_move
        consider_spells false
    }
}
```

---

### `NubsCat`
**Name:** Half-Dog  
**Source:** `enemies.gon`  

```
NubsCat {
    graphics {
        movieclip NubsCat
        name "ENEMY_HALFDOG_NAME"
        water_mask big
		tooltip "ENEMY_HALFDOG_DESC"
    }

    stats {
        strength 5
        dexterity 8
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [dog cat]
        faction enemies
        movement 1
        corpse_health 0
        health 17
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack NubsJump
        
        spells [
            NubsCatJumpReaction
        ]
    }

    passives {
        ImmediateAbilityReaction {
            ability NubsCatJumpReaction
            target_furthest_valid true
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            move_then_do NubsJump
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `CatHuman`
**Name:** Half-Human λ  
**Source:** `enemies.gon`  

```
CatHuman {
    graphics {
        movieclip CatHuman
        name ENEMY_CATHUMAN_NAME
        uifloaters_offset 1.5
		tooltip "ENEMY_CATHUMAN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [humanoid cat]
        faction enemies
        movement 2
        corpse_health 0
        health 18
    }

    abilities {
        move DefaultMove
        attack CHToss
        
        spells [
            CHCry
            CHSpawn
        ]
    }

    passives {
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [CHToss]
        }
        fallback {
            do_random [CHSpawn CHCry]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `HumanCat`
**Name:** Half-Human δ  
**Source:** `enemies.gon`  

```
HumanCat {
    graphics {
        movieclip HumanCat
        name ENEMY_HUMANCAT_NAME
		tooltip "ENEMY_HUMANCAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [humanoid cat]
        faction enemies
        movement 3
        health 9
    }

    abilities {
        move DefaultMove
        attack HCAttack
        
        spells [
            HCHumanDie
        ]
    }

    passives {
        FormChanger { 
            Default {
                passives {
                    DeathRattleRevive HCHumanDie
                    DodgeChanceWithBlindSpot 25%
                }
            }
            HumanDead {
                animation_suffix DH
                tooltip "ENEMY_HUMANCAT2_DESC"

                attack HCSpin
            }

            initial_form Default
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `CopBot`
**Name:** Cop Bot  
**Source:** `enemies.gon`  

```
CopBot {
    graphics {
        movieclip CopBot
        name "ENEMY_COPBOT_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_COPBOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [robot]
        faction enemies
        movement 3
        health 2
        shield 16
        auto_run_priority support
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            CBShoot_ZodiacStyle
            CBReload
        ]
    }

    passives {
        SecurityBotProtect {
            enemies_only true
            ability CBShoot_ZodiacStyle
            move None
        }
        Ammo 1
        AggroTargetIsLastEnemyThatDealtDamage 1
        FaceShield 0
        Robot 1
        Trample 3
        SupportDieInsteadOfRun {
            alt_dying_ani shutdown
            alt_dead_ani off
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [attack CBReload]
        }

        decision_weights cop
        move_weights stay_close
    }
}
```

---

### `CopBot_Uprising`
**Source:** `enemies.gon`  

```
CopBot_Uprising {
    variant_of CopBot

    properties { 
        auto_run_priority default
    }
}
```

---

### `DrDitto`
**Name:** Dr. Ditto  
**Source:** `enemies.gon`  

```
DrDitto {
    graphics {
        movieclip DrDitto
        name "ENEMY_DRDITTO_NAME"
        uifloaters_offset 1.5
        scale .9
		tooltip "ENEMY_DRDITTO_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [humanoid]
        faction enemies
        movement 2
        health 9
    }

    abilities {
        move DefaultMove
        attack DrDRockets
        
        spells [
            DrDGlare
        ]
    }

    passives {
        DelayedAutoRevive {
            rounds 1
            health 50%
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*DrDGlare DrDRockets]
        }

        decision_weights careless
        move_weights keep_distance_always_move
    }
}
```

---

### `PoisonFrog`
**Name:** Poison Frog  
**Source:** `enemies.gon`  

```
PoisonFrog {
    variant_of Toad

    graphics {
        movieclip Frog
        name "ENEMY_POISONFROG_NAME"
        tint green
    }

    properties {
        faction enemies
        kill_required true
        health 5
    }

    passives {
        AddStatusToBasicAttack {
            Poison 1
        }
    }
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights keep_distance
    }
}
```

---

### `MegaMutant`
**Name:** Mega Mutant  
**Source:** `enemies.gon`  

```
MegaMutant {
    graphics {
        movieclip MegaMutant
        name "ENEMY_MEGAMUTANT_NAME"
        uifloaters_offset 2
        shadow_size 2
        water_mask medmed
        move_speed_sync_frames 44
        scale .8
		tooltip "ENEMY_MEGAMUTANT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid cat]
        health 26
        movement 1
        faction enemies
        dispersed_bonus_turns 1

        size 2x2
        move_block everything_even_when_dead

        banned_elite_buffs [Protected]
    }

    abilities {
        move DefaultMove
        attack MM_Slap

        spells [
            MM_Quake
            MM_Guard
            MM_Unguard
            MM_Grab
        ]
    }

    passives {
        Trample 3

        FormChanger {
            Default {
                passives {
                    AbilityReaction {
                        ability MM_Guard
                        ability_damage_only true
                        only_when_not_your_turn true
                    }
                }
            }
            Guarding {
                partial_animation_suffix "Guarding"

                passives {
                    Brace 99
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do *MM_Unguard
                    }

                    decision_weights careless
                    move_weights stay_close
                    reset_pattern_on_formswitch false
                    end_turn_on_formswitch false
                    
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*MM_Slap MM_Quake]
            do_all [*MM_Slap MM_Grab]
        }

        decision_weights careless
        move_weights stay_close
        reset_pattern_on_formswitch false
        end_turn_on_formswitch false
    }
}
```

---

### `CavePerson`
**Name:** Caveman  
**Source:** `enemies.gon`  

```
CavePerson {
    graphics {
        movieclip CavePerson
        name "ENEMY_CAVEMAN_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_CAVEMAN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag humanoid
        faction cavemen
        health 32
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            WereManPounce
            WereManTransformSwipe

            CaveWomanGrab
            CaveWomanDrop
            CaveWomanBirth
            CaveWomanThrow
            CaveWomanDropTransform

            CaveManPickupSpear
            CaveManChestPound
            CaveManTransform
            CaveManSpearRun

            CaveBabyGrow
            CaveBabyFoodMove
        ]
    }

    passives {
        FormChanger {
            CaveBaby {
                animation_suffix "CaveBaby"
                name "ENEMY_CAVEBABY_NAME"
				tooltip "ENEMY_CAVEBABY_DESC"

                attack CaveBabyMelee

                passives {
                    WhitelistPickupType food

                    AbilityHealthThreshold {
                        threshold_min X
                        immediate true
                        even_if_stunned true
                        ability CaveBabyGrow
                    }
                }

                ai {
                    brain PatternBrain

                    virtual_abilities {
                        FoodMove {
                            ability CaveBabyFoodMove
                            move_weights stay_close_move_if_possible
                        }
                    }

                    pattern {
                        do_all [*attack, FoodMove, attack, FoodMove, move]
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }
            CaveMan {
                animation_suffix "CaveMan"
                name "ENEMY_CAVEMANMAN_NAME"
                attack CaveMan3HitCombo
				tooltip "ENEMY_CAVEMANMAN_DESC"

                passives {
                    PrioritizeWeakestEnemy 1
                    WeremanTransformationReceiver CaveManTransform
                }

                ai {
                    brain PatternBrain

                    virtual_abilities {
                        SpearRun {
                            ability CaveManSpearRun
                            move_for_ability CaveManPickupSpear
                            move_weights util_minmove
                        }
                    }

                    pattern {
                        do_all [SpearRun CaveManPickupSpear attack CaveManChestPound]
                    }

                    decision_weights default
                    move_weights stay_close
                    end_turn_on_formswitch true
                }
            }
            CaveManSpear {
                animation_suffix "SpearCaveMan"
                name "ENEMY_SPEARCAVEMAN_NAME"
                attack CaveManThrowSpear
				tooltip "ENEMY_SPEARCAVEMAN_DESC"

                passives {
                    WeremanTransformationReceiver CaveManTransform
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [attack CaveManChestPound]
                    }

                    decision_weights default
                    move_weights keep_ranged_distance
                }
            }
            CaveWoman {
                animation_suffix "CaveWoman"
                name "ENEMY_CAVEMANWOMAN_NAME"
                attack CaveWomanKick
				tooltip "ENEMY_CAVEMANWOMAN_DESC"

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has CaveWomanHasCat
                    }
                    WeremanTransformationReceiver CaveManTransform
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [CaveWomanGrab attack CaveWomanBirth]
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }
            CaveWomanHasCat {
                animation_suffix "CatCaveWoman"
                name "ENEMY_CAVEMANWOMAN2_NAME"
                attack CaveWomanCatSlap
				tooltip "ENEMY_CAVEMANWOMAN2_DESC"

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot CaveWoman
                    }
                    WeremanTransformationReceiver CaveWomanDropTransform
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [attack CaveWomanThrow]
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }
            WereMan {
                animation_suffix "WereMan"
                name "ENEMY_WEREMAN_NAME"
                attack WereManFurySwipes
				tooltip "ENEMY_WEREMAN_DESC"

                passives {
                    AddTag cat
                   
                }

                /*statuses_on_enter_form {
                    FullHeal 1
                }*/

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [/*WereManTransformSwipe*/ attack WereManPounce]
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }

            initial_form CaveBaby
        }
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `CaveBaby`
**Source:** `enemies.gon`  

```
CaveBaby {
    variant_of CavePerson

    properties {
        initial_health 10
        health 20
    }

    passives {
       FormChanger {
           initial_form CaveBaby
       }
    }
}
```

---

### `CaveMan`
**Source:** `enemies.gon`  

```
CaveMan {
    variant_of CavePerson
    passives {
       FormChanger {
           initial_form CaveManSpear
       }
    }
}
```

---

### `CaveManNoSpear`
**Source:** `enemies.gon`  

```
CaveManNoSpear {
    variant_of CavePerson
    passives {
       FormChanger {
           initial_form CaveMan
       }
    }
}
```

---

### `CaveWoman`
**Source:** `enemies.gon`  

```
CaveWoman {
    variant_of CavePerson

    properties {
        health 30
    }

    passives {
       FormChanger {
           initial_form CaveWoman
       }
    }
}
```

---

### `WereMan`
**Source:** `enemies.gon`  

```
WereMan {
    variant_of CavePerson

    properties {
        faction sabertooths
    }

    passives {
       FormChanger {
           initial_form WereMan
       }
    }
}
```

---

### `CaveChief`
**Name:** Caveman Chief  
**Source:** `enemies.gon`  

```
CaveChief {
    graphics {
        movieclip CaveChief
        name "ENEMY_CAVEMANCHIEF_NAME"
        uifloaters_offset 2

        tooltip "ENEMY_CAVEMANCHIEF_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag humanoid
        faction cavemen
        dispersed_bonus_turns 1
        movement 2
        health 30
        shield 15
    }

    abilities {
        move DefaultMove
        attack CaveChiefSlam
        
        spells [
            CaveChiefBat
            CaveChiefRally
            CaveChiefFear
        ]
    }

    passives {
        AllStatsAura {
            stacks 1
            range global
            aura_requires_tag humanoid
        }
    }

    ai {
        brain PatternBrain

        pattern {
            do_priority [CaveChiefBat attack CaveChiefRally CaveChiefFear]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Yeti`
**Name:** Yeti  
**Source:** `enemies.gon`  

```
Yeti {
    graphics {
        movieclip Yeti
        name "ENEMY_YETI_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_YETI_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag humanoid
        faction enemies
        dispersed_bonus_turns 1
        health 40
        act_points 3
    }

    abilities {
        move DefaultMove
        attack YetiSlam
        
        spells [
            YetiBite
            YetiKick
            YetiIceBreath
        ]
    }

    passives {

    }

    ai {
        brain PatternBrain

        pattern {
            do_all_shuffle [YetiSlam YetiSlam YetiSlam
                            YetiBite YetiBite YetiBite 
                            YetiKick YetiKick YetiKick]
        }

        fallback {
            do YetiIceBreath
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `Fuzzer`
**Name:** Fuzzer  
**Source:** `enemies.gon`  

```
Fuzzer {
    graphics {
        movieclip Fuzzer
        name "ENEMY_FUZZER_NAME"
		tooltip "ENEMY_FUZZER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag blob
        faction enemies
        health 10
        corpse_health 0
    }

    abilities {
        move FuzzerJump
        attack BasicMelee
        
        spells [
            FuzzerJump_post
            FuzzerReact
        ]
    }

    passives {
        ZeroKnockbackDamage 1
        SmallRockBehavior 0 

        MeleeRevengeDamage {
            effects {
                Confusion 1
            }
        }

        AddStatusToBasicAttack {
            Confusion 1
        }

        StatusOnEnemyConfused {
            ImmediateUseAbility FuzzerReact
        }
    }

    ai {
        brain PatternBrain

        pattern {
            do_strict [attack **FuzzerJump_post]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Mammoth`
**Name:** Wooly Mammoth  
**Source:** `enemies.gon`  

```
Mammoth {
    graphics {
        movieclip Mammoth
        name "ENEMY_WOOLYMAMMOTH_NAME"
        uifloaters_offset 2
        shadow_size 2
        water_mask square

        move_speed_multiplier .75
		tooltip "ENEMY_WOOLYMAMMOTH_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag animal
        health 60
        movement 2
        faction mammoths
        dispersed_bonus_turns 1
        corpse_health 5

        size 2x2
        move_block everything_even_when_dead

        elements [
            Earth
        ]
    }

    abilities {
        move DefaultMove
        attack MammothThrow

        spells [
            MammothTrampleDash
            MammothStomp
        ]
    }

    passives {
        Trample 3
        Divide4OnDeath BiggestFood
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*MammothStomp attack]
            do_all [*MammothStomp MammothTrampleDash *attack]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `BungaWarrior1`
**Name:** Bunga's Champion  
**Source:** `enemies.gon`  

```
BungaWarrior1 {
    graphics {
        movieclip BungaElite1
        name "ENEMY_BUNGACHAMP_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_BUNGACHAMP_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag humanoid
        hidden_tag bungawarrior
        faction cavemen

        health 100
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            WereManPounce
            WereManTransformSwipe

            CaveWomanGrab
            CaveWomanDrop
            CaveWomanBirth
            CaveWomanThrow
            CaveWomanDropTransform

            CaveManPickupSpear
            CaveManChestPound
            CaveManTransform
            CaveManSpearRun

            CaveBabyGrow
            CaveBabyFoodMove
        ]
    }

    passives {
        FormChanger {
            CaveMan {
                animation_suffix "CaveMan"
                attack CaveMan3HitCombo

                passives {
                    PrioritizeWeakestEnemy 1
                }

                ai {
                    brain PatternBrain

                    virtual_abilities {
                        SpearRun {
                            ability CaveManSpearRun
                            move_for_ability CaveManPickupSpear
                            move_weights util_minmove
                        }
                    }

                    pattern {
                        do_all [SpearRun CaveManPickupSpear attack CaveManChestPound]
                    }

                    decision_weights default
                    move_weights stay_close
                    end_turn_on_formswitch true
                }
            }
            CaveManSpear {
                animation_suffix "SpearCaveMan"
                attack CaveManThrowSpear

                passives {

                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [attack CaveManChestPound]
                    }

                    decision_weights default
                    move_weights keep_ranged_distance
                }
            }


            initial_form CaveManSpear
        }
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `BungaWarrior2`
**Source:** `enemies.gon`  

```
BungaWarrior2 {
    variant_of BungaWarrior1
    graphics {
        movieclip BungaElite2
    }
}
```

---

### `Trex`
**Name:** T-Rex  
**Source:** `enemies.gon`  

```
Trex {
    graphics {
        movieclip Trex
        name "ENEMY_TREX_NAME"
        uifloaters_offset 2
        shadow_size 2
        water_mask square
		tooltip "ENEMY_TREX_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag dinosaur
        health 45
        movement 2
        faction enemies

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack TrexEat

        spells [
            TrexStomp
            TrexSwitchTarget
            TrexReacquireTarget
        ]
    }

    passives {
        Trample 3
        CounterAttack TrexSwitchTarget
        AggroTargetIsGovernedByHitEffect {
            enemies_only false
        }
        PrioritizeAggroTarget 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*TrexReacquireTarget *attack attack move attack TrexStomp]
        }

        decision_weights default
        move_weights towards_aggro_stay_close
    }
}
```

---

### `Stegosaurus`
**Name:** Stegosaurus  
**Source:** `enemies.gon`  

```
Stegosaurus {
    graphics {
        movieclip Stegosaurus
        name "ENEMY_STEGOSAURUS_NAME"
        uifloaters_offset 2
        shadow_size 2
        scale .9
        water_mask square
		tooltip "ENEMY_STEGOSAURUS_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag dinosaur
        health 45
        movement 2
        faction enemies
        dispersed_bonus_turns 1

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack StegoTailSwipe

        spells [
            StegoEatGrass
            StegoSpin
            StegoGrassStomp
        ]
    }

    passives {
        Trample 3
        CounterAttack {
            ability StegoTailSwipe
            without_orienting true
        }
    }
    
    ai {
        brain PatternBrain
        
        virtual_abilities {
            MoveForGrass {
                ability StegoGrassStomp
                move_for_ability StegoEatGrass
                move_weights minimum_move
            }
        }

        pattern {
            do_priority [*StegoSpin StegoSpin]
            do_all [MoveForGrass StegoEatGrass StegoSpin]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Triceratops`
**Name:** Triceratops  
**Source:** `enemies.gon`  

```
Triceratops {
    graphics {
        movieclip Triceratops
        name "ENEMY_TRICERATOPS_NAME"
        uifloaters_offset 2
        shadow_size 2
        water_mask square
		tooltip "ENEMY_TRICERATOPS_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag dinosaur
        health 45
        movement 2
        faction enemies
        
        round_end_bonus_turns 1

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack TriceratopsGore

        spells [
            TriceratopsTrample
        ]
    }

    passives {
        Trample 3
        FaceLastDamage 1
        CounterAttack attack
        Brace 2
    }
    
    ai {
        brain PatternBrain

        pattern {
            do TriceratopsTrample
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Pterodactyl`
**Name:** Pterodactyl  
**Source:** `enemies.gon`  

```
Pterodactyl {
    graphics {
        movieclip Pterodactyl
        name "ENEMY_PTERODACTYL_NAME"
        scale .8
        uifloaters_offset 2
		tooltip "ENEMY_PTERODACTYL_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag dinosaur
        faction enemies
        flying true
        health 30
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            PteroGrab
            PteroEscape
        ]
    }

    passives {
        FormChanger {
            Default {

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has HasCat
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [PteroGrab, attack]
                    }

                    decision_weights default
                    move_weights stay_close
                }
            }
            HasCat {
                animation_suffix "Cat"
                attack PteroPeck

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot Default
                    }
                    ChanceToSpitOnDamage {
                        flat_chance 50%
                        chance_per_damage 0%
                        ability PteroEscape
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do attack
                    }

                    decision_weights default
                    move_weights stay_far
                }
            }

            initial_form Default
        }
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `PrehistoricPooter`
**Name:** Prehistoric Pooter  
**Source:** `enemies.gon`  

```
PrehistoricPooter {
    graphics {
        movieclip Pooter
        name "ENEMY_PREHISTORICPOOTER_NAME"
        shadow_size .75
        scale 1.2
        uifloaters_offset 1
        piece_alt_frame 3

        tooltip "ENEMY_PREHISTORICPOOTER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag bug
        health 13
        movement 2
        faction enemies
        flying true
    }

    abilities {
        move DefaultMove
        attack PrehistoricPooterShot
        
        spells [

        ]
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights keep_distance
    }
}
```

---

### `DinoEggs`
**Name:** Dino Nest  
**Source:** `enemies.gon`  

```
DinoEggs {
    graphics {
        movieclip DinoEggs
        name "ENEMY_DINONEST_NAME"
        water_mask medium
        scale .85

        tooltip "ENEMY_DINONEST_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 0
        charisma 5
    }
    
    properties {
        tag animal
        health 6
        movement 0
        faction enemies
        corpse_health 0
        can_be_backstabbed false
    }

    abilities {
        move None
        attack DinoEggsSpawn
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        auto_orient false
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `FatMan`
**Name:** Überman  
**Source:** `enemies.gon`  

```
FatMan {
    graphics {
        movieclip FatMan
        name "ENEMY_FATMAN_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed
		tooltip "ENEMY_FATMAN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 10
        intelligence 3
        speed 1
        charisma 2
    }
    
    properties {
        tag [humanoid blob]
        health 20
        movement 1
        faction enemies

        corpse_health 5
        dispersed_bonus_turns 1

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack FatManLunge

        spells [

        ]
    }

    passives {
        Trample 3

        ReflectProjectiles {
            self_damage 2
        }
        AbilityReaction {
            ability attack
            backstabs_only true
        }
        MeleeRevengeDamage {
            type status
            damage 0
            knockback 2
        }

        RandomizeAIWeightsEachTurn [
            {
                decision_weights default
                move_weights stay_close
            }

            {
                decision_weights no_act
                move_weights stay_close
            }
        ]
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `FatWoman`
**Name:** Überwoman  
**Description:** Melee attacker with Knockback.
Reflects projectiles. Units that contact it get knocked back.
Trample.  
**Source:** `enemies.gon`  

```
FatWoman {
    variant_of FatMan

    graphics {
        movieclip FatWoman
        name "ENEMY_FATWOMAN_NAME"
        desc ENEMY_FATWOMAN_DESC
    }
}
```

---

### `SoldierBot`
**Name:** Schutzbot  
**Source:** `enemies.gon`  

```
SoldierBot {
    graphics {
        movieclip SoldierBot
        name "ENEMY_SCHUTZBOT_NAME"
        uifloaters_offset 2
        scale .8
		tooltip "ENEMY_SCHUTZBOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties { 
        tag [robot]
        faction enemies
        movement 3
        health 8
        shield 20
    }

    abilities {
        move DefaultMove
        attack SZBShoot
        
        spells [
            SZBReload
            SZBBackflipDodge
        ]
    }

    passives {
        SecurityBotProtect {
            enemies_only true
            ability SZBShoot
            move None
        }
        Ammo 3
        Robot 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*attack~ attack~ SZBReload]
        }

        decision_weights cop
        move_weights keep_distance
    }
}
```

---

### `HangerBot`
**Name:** Hängenbot  
**Source:** `enemies.gon`  

```
HangerBot {
    graphics {
        movieclip HangerBot
        name "ENEMY_HANGERBOT_NAME"
        uifloaters_offset 2
        scale .8
		tooltip "ENEMY_HANGERBOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [robot]
        faction enemies
        movement 3
        health 10
        shield 15
        flying true

        banned_elite_buffs [Protected]
    }

    abilities {
        move Teleport
        attack HangerBotAttack
        
        spells [
            HangerBotSpawn
            HangerBotLeave
            HangerBotReturn
        ]
    }

    passives {
        Robot 1
        AbilityReaction {
            ability HangerBotLeave
            ability_damage_only true
            only_when_not_your_turn true
        }
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            ReturnA {
                ability HangerBotReturn
                move_weights stay_close
            }
        }

        pattern {
            do_priority [ReturnA attack HangerBotSpawn]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `DoctorBot`
**Name:** Doktorbot  
**Source:** `enemies.gon`  

```
DoctorBot {
    graphics {
        movieclip DocBot
        name "ENEMY_DOKTORBOT_NAME"
        uifloaters_offset 2
        scale .8
		tooltip "ENEMY_DOKTORBOT_DESC"
		
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [robot]
        faction enemies
        movement 3
        health 8
        shield 10
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack DoctorBotHeal
        
        spells [
            DoctorPickup
            DoctorSpawn
        ]
    }

    passives {
        Robot 1
        Brace 2
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [DoctorBotHeal DoctorPickup DoctorSpawn]
        }


        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `JarHead`
**Name:** Krughead  
**Source:** `enemies.gon`  

```
JarHead {
    graphics {
        movieclip JarHead
        name "ENEMY_KRUGHEAD_NAME"
        tooltip "ENEMY_KRUGHEAD_DESC"

		scale .8
        uifloaters_offset 1.5

    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [humanoid]
        faction enemies
        movement 5
        health 6
        shield 12
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            JarHeadOrder
        ]
    }

    passives {
        Brace 2
        MagicDamageImmune 1
        DebuffImmunity 1
        CounterAttack attack
        DeathRattle {
            ability JarHeadDeath
            pop_corpse false
            is_dying_animation true
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [JarHeadOrder attack]
        }

        decision_weights default
        move_weights stay_near_allies
    }
}
```

---

### `FetusJar`
**Name:** Fötusjar  
**Source:** `enemies.gon`  

```
FetusJar {
    graphics {
        movieclip FetusJar
        name "ENEMY_FETUSJAR_NAME"
        tooltip "ENEMY_FETUSJAR_DESC"

        uifloaters_offset 1.5

        scale .8
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [humanoid fetus]
        faction enemies
        movement 3
        health 6
        shield 8
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack FurySwipes_Enemy
        
        spells [
            
        ]
    }

    passives {
        Brace 2
        MagicDamageImmune 1
        DebuffImmunity 1
        DeathRattle {
            ability FetusJarDeath
            pop_corpse false
            is_dying_animation true
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `FetusNoJar`
**Name:** Der Fötus  
**Source:** `enemies.gon`  

```
FetusNoJar {
    graphics {
        movieclip FetusNoJar
        name "ENEMY_FETUSNOJAR_NAME"
        scale .8
		tooltip "ENEMY_FETUSNOJAR_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [humanoid fetus]
        faction enemies
        movement 5
        health 8
    }

    abilities {
        move DefaultMove
        attack FurySwipes_Enemy
        
        spells [
            FetusAirstrikeTrigger
            FetusPullBomb
        ]
    }

    passives {
        FormChanger {
            Default {
                passives {
                    AbilityHealthThreshold {
                        threshold "max(X*.5, 5)"
                        ability FetusPullBomb
                    }
                }
            }
            Bomb {
                partial_animation_suffix Button
                passives {
                    DeathRattle {
                        ability FetusAirstrikeTrigger
                        pop_corpse false
                        is_dying_animation true
                    }
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [ attack]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `TVBot`
**Name:** Fernsehbot  
**Source:** `enemies.gon`  

```
TVBot {
    graphics {
        movieclip EmptyV
        name "ENEMY_TVBOT_NAME"
        scale .8
		tooltip "ENEMY_TVBOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [robot]
        auto_run_priority support
        faction enemies
        movement 3
        health 1
        shield 14
        flying true
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [
            TVOff
            TVChangeObey
            TVChangeStop
            TVChangeDumb
            TVChangeDie
        ]
    }

    passives {
        Robot 1

        FormChanger {
            Obey {
                keyword_tooltips {TVBotObey 1}

                passives {
                    ImmediateAbilityReaction TVOff
                    TVBotDisableAttack 1
                }
            }
            Stop {
                keyword_tooltips {TVBotStop 1}

                passives {
                    ImmediateAbilityReaction TVOff
                    TVBotDisableMove 1
                }
            }
            Dumb {
                keyword_tooltips {TVBotDumb 1}

                passives {
                    ImmediateAbilityReaction TVOff
                    TVBotDisableSpells 1
                }
            }
            /*Shit {
            }
            Fuck {
            }*/
            Die {
                keyword_tooltips {TVBotDie 1}

                passives {
                    
                }
            }
            Off {
                animation_suffix Off
            }


            initial_form Off
        }

        SupportFormChangeInsteadOfRun {
            ability TVChangeDie
            wait_till_turn true
        }

        TVBotScreen {
            Obey 1
            Stop 2
            Dumb 3
            Shit 4
            Fuck 5
            Die 6
        }

        CharacterLightSource {
            color [.7, .8, .9]
            glow [.7, .8, .9, .5]
            size 4
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_random [**TVChangeObey **TVChangeStop **TVChangeDumb]
        }
        fallback {
            do_nothing []
        }

        auto_orient false
        animate_choice false
        decision_weights default
        move_weights keep_distance_face_camera
    }
}
```

---

### `TallBot`
**Name:** Großerbot  
**Source:** `enemies.gon`  

```
TallBot {
    graphics {
        movieclip TallBot
        name "ENEMY_TALLBOT_NAME"
        uifloaters_offset 2.5
		tooltip "ENEMY_TALLBOT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [robot]
        faction enemies
        movement 2
        health 10
        shield 20
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack TallBotSuplex
        
        spells [
            TallBotRocket
        ]
    }

    passives {
        Robot 1
        Brace 2
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }
        fallback {
            do TallBotRocket
        }


        decision_weights default
        move_weights stay_close
    }
}
```

---

### `BoyShade`
**Name:** Herald  
**Source:** `enemies.gon`  

```
BoyShade {
    graphics {
        movieclip ShadeM
        name "ENEMY_HERALD_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_HERALD_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [demon]
        faction enemies
        movement 4
        health 30
    }

    abilities {
        move Teleport
        attack BasicMelee
        
        spells [
            ShadeDuplicate
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*ShadeDuplicate attack ShadeDuplicate move]
        }


        decision_weights default
        move_weights stay_close
    }
}
```

---

### `BoyShadeClone`
**Name:** Herald's Shadow  
**Source:** `enemies.gon`  

```
BoyShadeClone {
    graphics {
        movieclip ShadeMShadow
        name "ENEMY_HERALDSHADOW_NAME"
        uifloaters_offset 1.5
        randomize_starting_frame false
		tooltip "ENEMY_HERALDSHADOW_DESC"

    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [demon]
        faction enemies
        movement 4
        health 1
        initiative -99
        corpse_health 0
    }

    abilities {
        move Teleport
        attack BasicMelee
        
        spells [
            
        ]
    }

    passives {
        DieWhenSpawnerDies 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }


        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Gasper`
**Name:** Gasper  
**Source:** `enemies.gon`  

```
Gasper {
    graphics {
        movieclip Tox
        name "ENEMY_GASPER_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_GASPER_DESC"

    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        hidden_tag poison_cloud_immune
        health 17
        faction enemies
        flying true
        corpse_health 0
        movement 4
    }

    abilities {
        move DefaultMove
        attack SpawnGas
        
        spells [
            SpawnGasAOE
            ToxGasBlast
        ]
    }

    passives {
        
        StatusImmunity Poison
        
        

        FormChanger {
            Default {
                passives {
                    DeathRattleRevive ToxPuff
                    AbilityReaction ToxGasBlast
                }
            }
            Explody {
                animation_suffix Expl
                attack ToxExplode
                move None

                passives {
                    DisplayDangerAOE attack
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do attack
                    }

                    decision_weights always_cast_careless
                    move_weights stay_close
                }
            }

            initial_form Default
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [move *SpawnGasAOE]
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `Floast`
**Name:** Floast  
**Source:** `enemies.gon`  

```
Floast {
    graphics {
        movieclip Floast
        name "ENEMY_FLOAST_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_FLOAST_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [tumor skeleton]
        health 10
        shield 8
        faction enemies
        flying true
        movement 2
    }

    abilities {
        move DefaultMove
        attack FloastPull
        
        spells [
            FloastThrow
            FloastSpawn
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [*FloastThrow FloastPull FloastSpawn]
        }

        decision_weights default
        move_weights keep_far_distance
    }
}
```

---

### `Gorger`
**Name:** Gorger  
**Source:** `enemies.gon`  

```
Gorger {
    graphics {
        movieclip ShamblingShade
        name "ENEMY_GORGER_NAME"
        uifloaters_offset 1.5
        shadow_size 3
        water_mask medmed
		tooltip "ENEMY_GORGER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
    }
    
    properties {
        tag [demon]
        health 60
        movement 1
        faction enemies

        size 3x3
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack GorgerGorge

        spells [
            GorgerRun
        ]
    }

    passives {
        Trample 3
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [*attack attack GorgerRun]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Slag`
**Name:** Slag  
**Source:** `enemies.gon`  

```
Slag {
    graphics {
        movieclip Slag
        name "ENEMY_SLAG_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed
		tooltip "ENEMY_SLAG_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
    }
    
    properties {
        tag [tumor skeleton]
        health 40
        movement 2
        faction enemies

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack SlagBoner

        spells [
            SlagSpawn
        ]
    }

    passives {
        Trample 3

        SpawnThingOnDamage {
            object TumorBarrier
            melee_ability_only true
            
        }
        AbilityReaction {
            ability SlagSpawn
            ability_damage_only true
            ranged_only true
            verify_target true
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `HitlerClone`
**Name:** Führerfötus  
**Source:** `enemies.gon`  

```
HitlerClone {
    graphics {
        movieclip FetusNoJar
        name "ENEMY_HITLERCLONE_FETUS_NAME"
		tooltip "ENEMY_HITLERCLONE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [humanoid]
        hidden_tag hitler_clone
        faction enemies
        movement 3
        health 17
    }

    abilities {
        move DefaultMove
        attack FurySwipes_Hitler
        
        spells [
            HitlerCloneTransform
            HitlerCloneLick
            HitlerCloneHeil
        ]
    }

    passives {
        FormChanger {
            Default {
                passives {
                    AddTag fetus
                    AddHiddenTag hitler_clone_fetus
                }

                ai {
                    brain PatternBrain
                    pattern {
                        move_then_do attack
                    }

                    decision_weights simple
                    move_weights random
                }
            }
            Grown {
                animation_suffix Grown
                name "ENEMY_HITLERCLONE_NAME"
                uifloaters_offset 1.5
                attack HitlerCloneSwipes
                weak_threshold 15

                passives {
                    AddHiddenTag grown_hitler_clone
                }

                ai {
                    brain PatternBrain
                    pattern {
                        do_priority [attack HitlerCloneLick]
                    }

                    decision_weights default
                    move_weights stay_close_always_move
                }
            }
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `TumorBarrier`
**Name:** Edema  
**Source:** `enemies.gon`  

```
TumorBarrier {
    graphics {
        movieclip TumorBarrier
        name "ENEMY_EDEMA_NAME"
		tooltip "ENEMY_EDEMA_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
    }
    
    properties {
        tag [tumor]
        health 8
        movement 0
        faction enemies
        corpse_health 0
    }

    abilities {
        move None
        attack None

        spells [
            
        ]
    }

    passives {
        RandomPassivePool {
            TransformInXTurns {
                stacks 2
                object HuskG
            }
            TransformInXTurns {
                stacks 3
                object HuskG
            }
        }
        DeathRattle {
            ability TumorPrisonDeathrattle
            is_dying_animation true
            target_killer true
        }
    }
    
    ai {
        brain NoBrain

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Husk`
**Name:** Husk  
**Source:** `enemies.gon`  

```
Husk {
    graphics {
        movieclip Husk
        name "ENEMY_HUSK_NAME"
        uifloaters_offset 1.75
        scale .9
		tooltip "ENEMY_HUSK_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
    }
    
    properties {
        tag [tumor skeleton]
        hidden_tag husk
        health 10
        shield 10
        movement 3
        faction enemies
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack HuskSwipes

        spells [
            
        ]
    }

    passives {
        TransformOnDeath TumorBarrier
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `HuskG`
**Source:** `enemies.gon`  

```
HuskG {
    variant_of Husk
    graphics {
        spawnin_animation grow
    }
}
```

---

### `ConjoinedHusk`
**Name:** Conjoined Husk  
**Source:** `enemies.gon`  

```
ConjoinedHusk {
    graphics {
        movieclip ConjoinedHusk
        name "ENEMY_CONJOINEDHUSK_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_CONJOINEDHUSK_DESC"
		
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [tumor skeleton]
        health 20
        shield 20
        movement 3
    }

    abilities {
        move DefaultMove
        attack CHuskBone
        
        spells [
            CHuskGrab
            CHuskDrop
            CHuskDropFail
            CHuskCatShade
        ]
    }

    passives {
        FormChanger {
            Default {
            }
            HasCat {
                attack CHuskCatShade
                animation_suffix "Cat"

                ai {
                    brain PatternBrain

                    pattern {
                        move_then_do CHuskCatShade
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
        }

        FormChangeWhileHasStatus {
            status Consuming
            form_has HasCat
            form_hasnot Default
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [CHuskGrab attack]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `PlayerCat_HuskShade`
**Source:** `enemies.gon`  

```
PlayerCat_HuskShade {
    variant_of PlayerCat

    graphics {
        tint [0 0 0 1]
    }

    properties {
        corpse_health 0
        can_grant_extra_turns false
        faction enemies

        is_player_cat false
        access_to_player_inventory false
        allow_passive_spelltransforming true
        force_not_familiar true
    }

    passives {
        FadeInsteadOfDie 1
    }

    ai {
        brain GenericBrain
    }
}
```

---

### `GirlShade`
**Name:** Heraldess  
**Source:** `enemies.gon`  

```
GirlShade {
    graphics {
        movieclip ShadeF
        name "ENEMY_HERALDESS_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_HERALDESS_DESC"
    }

    stats {
        strength 8
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties { 
        tag [demon]
        faction enemies
        movement 2
        health 33
    }

    abilities {
        move DefaultMove
        attack GSClosedAttack
        
        spells [
            GSSuck
            GSOpen
            GSScream
        ]
    }

    passives {
        FormChanger {
            Close {

                passives {
                    AbilityReaction GSOpen
                }
            }
            Open {
                animation_suffix Open
                attack GSOpenAttack

                passives {
                    AddMovement 2
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has OpenCat
                    }
                    CounterAttack [attack GSScream]
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [GSSuck attack]
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
            OpenCat {
                animation_suffix OpenCat

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot Close
                    }
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `MeatSlime`
**Name:** Meat Slime  
**Source:** `enemies.gon`  

```
MeatSlime {
    graphics {
        movieclip MeatSlime
        name "ENEMY_MEATSLIME_NAME"
        shadow MedSlimeShadow

        tooltip "ENEMY_MEATSLIME_DESC"
    }

    stats {
        strength 5
        dexterity 3
        constitution 3
        intelligence 3
        speed 3
        charisma 3
    }
    
    properties {
        tag blob
        faction enemies
        movement 3
        corpse_health 0
        
        health 16
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
        ]
    }

    passives {
        Divide4OnDeath Clot
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `ThrobbingTurret`
**Name:** Throbbing Turret  
**Source:** `enemies.gon`  

```
ThrobbingTurret {
    graphics {
        movieclip ThrobbingTurret
        name "ENEMY_THROBBINGTURRET_NAME"
        projectile_spawn_offset [0 1]
        water_mask medium
		tooltip "ENEMY_THROBBINGTURRET_DESC"

    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        
        health 10
        movement 0
        faction enemies
        corpse_health 0
        can_be_backstabbed false
    }

    abilities {
        move None
        attack ThrobShot
        
        spells [
            SpawnClot
            ThrobShot_Reaction
        ]
    }

    passives {
        MiniVolcanoReaction ThrobShot_Reaction
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do_priority [ThrobShot, SpawnClot]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Parasiter`
**Name:** Throbbing Servant  
**Source:** `enemies.gon`  

```
Parasiter {
    graphics {
        movieclip Parasiter
        name "ENEMY_THROBSERVANT_NAME"
		tooltip "ENEMY_THROBSERVANT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag humanoid
        faction enemies

        health 15
        movement 2
    }

    abilities {
        move DefaultMove
        attack ParasiterShoot
        
        spells [
            ParasiterSpawn
        ]
    }

    passives {

    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do_priority [ParasiterShoot, ParasiterSpawn]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `FleshLad`
**Name:** Flesh Lad  
**Source:** `enemies.gon`  

```
FleshLad {
    graphics {
        movieclip FleshLad
        name "ENEMY_FLESHLAD_NAME"
		tooltip "ENEMY_FLESHLAD_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies

        health 23
        movement 2
    }

    abilities {
        move DefaultMove
        attack FleshLadDoublehit
        
        spells [
            FleshLadUppercut
        ]
    }

    passives {
        StatusOnTookDamageFromAbility {
            ExtraBasicAttacks_Status 1
            HealthRegenUp 1
        }
        StatusEachTurnEnd {
            SpeedUp 2
        }
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do_all [attack~ FleshLadUppercut]
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `FleshyMind`
**Name:** Fleshy Mind  
**Source:** `enemies.gon`  

```
FleshyMind {
    graphics {
        movieclip FleshyMind
        name "ENEMY_FLESHYMIND_NAME"
		scale .8
		tooltip "ENEMY_FLESHYMIND_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies

        health 23
        movement 2
    }

    abilities {
        move DefaultMove
        attack FleshyMindDisable
        
        spells [
            FleshyMindConfusion
        ]
    }

    passives {
        CounterAttack FleshyMindConfusion
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do attack
        }

        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `ButchTinkBoris`
**Name:** Butch & Tink  
**Source:** `enemies.gon`  

```
ButchTinkBoris {
    graphics {
        movieclip ButchTinkX
        name "ENEMY_BUTCHTINK_NAME"
        water_mask square
		tooltip "ENEMY_BUTCHTINK_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid blob]
        faction enemies
        movement 2
        dispersed_bonus_turns 3
        mana_regen 999
        mana 100
        
        health 160

        size 2x2
        move_block everything_even_when_dead

        last_turn_is_main_turn true
        two_fronts true
        two_fronts_switch true
        can_be_backstabbed false
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [
            TrampleDash
            MoveOne
        ]
    }

    passives {
        Trample 3
        MoveTowardsDamageSource MoveOne
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights stay_close
        auto_orient false
        
        mainturn_pattern {
            do **TrampleDash
        }
        
        bonusturn_pattern {
            do move
        }
    }
}
```

---

### `TracyFetus`
**Name:** Tracy  
**Source:** `enemies.gon`  

```
TracyFetus {
    graphics {
        movieclip TracyX
        name "ENEMY_TRACY_NAME"
        uifloaters_offset 1.5
        shadow_size 2
        water_mask medmed
        four_way_animations true
        move_speed_sync_frames 35

        tooltip "ENEMY_TRACY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
    }
    
    properties {
        tag humanoid
        health 30
        movement 4
        faction enemies

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack MegafetusSpin

        spells [
            MegafetusMelee
        ]
    }

    passives {
        Trample 3

        CounterAttack MegafetusMelee
    }
    
    ai {
        brain GenericBrain
        consider_spells false
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `BeaniesRat`
**Name:** Dr. Beanies  
**Source:** `enemies.gon`  

```
BeaniesRat {
    graphics {
        movieclip BeaniesX
        name "ENEMY_DRBEANINES_NAME"
        projectile_spawn_offset [.25 1]
		tooltip "ENEMY_DRBEANIES_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag humanoid
        faction enemies

        mana_regen 999
        mana 100
        initiative -100
        movement 5
        health 67
        
        dispersed_bonus_turns 2
        dispersed_bonus_turns_consider_initiative false
        dispersed_bonus_turns_before_cats true
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [
            SpawnBomb
            BombRatTurtle
            RockToss_BomberRat
        ]
    }

    passives {
        FormChanger {
            Default { 
            }
            Rain {
                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [*RockToss_BomberRat, RockToss_BomberRat]
                    }

                    decision_weights extra_careless
                    move_weights keep_distance_always_move
                }
            }

            initial_form Default
        }

        FormChangeDuringWeatherElement {
            element Water
            form Rain
        }
    }
    
    ai {
        brain PatternBrain
        decision_weights extra_careless
        move_weights chaotic_runaway

        mainturn_pattern {
            do **BombRatTurtle
        }
        
        bonusturn_pattern {
            do *SpawnBomb
        }
        
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `FrankFetus`
**Name:** Frank  
**Source:** `enemies.gon`  

```
FrankFetus {
    graphics {
        movieclip FrankX
        name "ENEMY_FRANK_NAME"
        scale .8
        shadow_size .8
        water_mask medium

        tooltip "ENEMY_FRANK_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag humanoid
        health 12
        movement 4
        faction enemies
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack KirbySuck
        
        spells [

        ]
    }

    passives {
        FormChanger {
            Empty {
                animation_suffix ""
            }
            Full {
                animation_suffix "Full"
                attack KirbySpit

                passives {
                    ImmobilePassive 1
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do attack
                    }
                    decision_weights default
                    move_weights keep_distance
                }

                statuses_on_enter_form {
                    UseAbility KirbySpit
                }
            }

            initial_form Empty
        }

        FormChangeWhileHasStatus {
            status Consuming
            form_has Full
            form_hasnot Empty
        }

        SpawnOnDeath FrankPinky
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Cherubim`
**Name:** Cherubim  
**Source:** `enemies.gon`  

```
Cherubim {
    graphics {
        movieclip Revalark
        name "ENEMY_CHERUBIUM_NAME"
        uifloaters_offset 1.5

        tooltip "ENEMY_CHERUBIUM_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [bird angel]
        faction enemies

        health 20
        divine_shield 1
        movement 2
        flying true
        dispersed_bonus_turns 1
        corpse_health 0

        banned_elite_buffs [Protected]
    }
     
    abilities {
        move DefaultMove
        attack CherubimHeal
        
        spells [
            CherubimLeave
            CherubimReturn
        ]
    }

    passives {
        Bird CookedChickenLeg
        Angel 1

        FormChanger {
            Default {

                passives {
                    CherubimReaction {
                        Leave CherubimLeave
                        Return CherubimReturn
                    }
                }
            }
            OffMap {
                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [CherubimReturn]
                    }

                    decision_weights default
                    move_weights keep_distance_always_move
                }
            }
        }

        FormChangeOffMap {
            form_offmap OffMap
            form_onmap Default
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [attack CherubimLeave]
        }

        decision_weights default
        move_weights keep_distance_always_move
        end_turn_on_formswitch true
    }
}
```

---

### `Seraphim`
**Name:** Seraphim  
**Source:** `enemies.gon`  

```
Seraphim {
    graphics {
        movieclip Angel
        name "ENEMY_SERAPHIM_NAME"
        uifloaters_offset 1.5

        tooltip "ENEMY_SERAPHIM_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid angel]
        faction enemies

        health 15
        divine_shield 4
        movement 2
        flying true
        dispersed_bonus_turns 1
    }
     
    abilities {
        move DefaultMove
        attack SeraphimX
        
        spells [
            SeraphimRevive
        ]
    }

    passives {
        Angel 1

        RevengeDamage {
            type status
            damage 0
            knockback 5
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [SeraphimRevive attack]
        }

        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `AngelicKitten`
**Name:** Angelic Kitten  
**Source:** `enemies.gon`  

```
AngelicKitten {
    graphics {
        movieclip AngelicCatFetus
        name "ENEMY_ANGELICKITTEN_NAME"
        uifloaters_offset 1.5

        tooltip "ENEMY_ANGELICKITTEN_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [cat angel]
        faction enemies

        health 3
        movement 3
        flying true
    }
     
    abilities {
        move DefaultMove
        attack CherubMelee
        
        spells [
            CherubAttract
            CherubDoom
        ]
    }

    passives {
        Angel 1

        DeathRattle {
            ability CherubDoom
            is_dying_animation true
            must_target_killer true
            pop_corpse false
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*attack CherubAttract move]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Gatekeeper`
**Name:** Gatekeeper  
**Source:** `enemies.gon`  

```
Gatekeeper {
    graphics {
        movieclip Gatekeeper
        name "ENEMY_GATEKEEPER_NAME"
        uifloaters_offset 1.5

        tooltip "ENEMY_GATEKEEPER_DESC"
        show_infinity_damage_warning true
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag [zombie]
        faction enemies

        health 10
        shield 20
        movement 2
    }
     
    abilities {
        move DefaultMove
        attack GKSuck
        
        spells [
            GKLeap
            GKSpawn
        ]
    }

    passives {
        Undead 1
        AggroTargetIsLowestMaxHealthCat 1
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            LeapClose {
                ability GKLeap
                move_weights towards_aggro
            }
        }

        pattern {
            do_all [attack *GKSpawn LeapClose]
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `FamiliarMaggot`
**Source:** `familiars.gon`  

```
FamiliarMaggot {
    variant_of Maggot

    properties {
        faction allies
        inherit_faction true
    }

    abilities {
        can_get_bonus true
    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `FamiliarTumorousMaggot`
**Source:** `familiars.gon`  

```
FamiliarTumorousMaggot {
    variant_of TumorousMaggot

    properties {
        faction allies
        inherit_faction true
    }

    abilities {
        can_get_bonus true
    }

    /*ai {
        brain PlayerBrain
    }*/
}
```

---

### `FamiliarChargeyMaggot`
**Source:** `familiars.gon`  

```
FamiliarChargeyMaggot {
    variant_of ChargeyMaggot

    properties {
        faction allies
        inherit_faction true
    }

    abilities {
        can_get_bonus true
    }

   /* ai {
        brain PlayerBrain
    }*/
}
```

---

### `FamiliarSwappyMaggot`
**Source:** `familiars.gon`  

```
FamiliarSwappyMaggot {
    variant_of SwappyMaggot

    properties {
        faction allies
        inherit_faction true
    }

    abilities {
        can_get_bonus true
    }

    /*ai {
        brain PlayerBrain
    }*/
}
```

---

### `FamiliarPooter`
**Source:** `familiars.gon`  

```
FamiliarPooter {
    variant_of Pooter
	
	graphics {
		tint [.7 1 .7 1]
	}

    properties {
        faction allies
        inherit_faction true
    }

    abilities {
        can_get_bonus true
    }

    ai {
        brain PlayerBrain
    }
}
```

---

### `CharmedPooter`
**Source:** `familiars.gon`  

```
CharmedPooter {
    variant_of Pooter

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedFlySwarm`
**Source:** `familiars.gon`  

```
CharmedFlySwarm {
    variant_of FlySwarm

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedFlea`
**Source:** `familiars.gon`  

```
CharmedFlea {
    variant_of Flea

	graphics {
		tint [.7 1 .7 1]
	}

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedFleaSpecial`
**Name:** Florian the Flea  
**Source:** `familiars.gon`  

```
CharmedFleaSpecial {
    variant_of CharmedFlea
    graphics {
        name "FAMILIAR_FLORIANTHEFLEA_NAME"
        tooltip "FAMILIAR_FLORIANTHEFLEA_DESC"
    }
    
    properties {
        health 10
    }

    abilities {
        attack BasicDrainMelee
    }
    
}
```

---

### `CharmedTinySpider`
**Source:** `familiars.gon`  

```
CharmedTinySpider {
    variant_of TinySpider

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedFly`
**Source:** `familiars.gon`  

```
CharmedFly {
    variant_of Fly

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `SteelFly`
**Name:** Steel Fly  
**Source:** `familiars.gon`  

```
SteelFly {
    variant_of CharmedFly

    graphics {
        name "FAMILIAR_FLY_STEEL_NAME"
        tooltip "FAMILIAR_FLY_STEEL_DESC"
        piece_alt_frame 5
    }

    properties {
        kill_required false
    }
    
    passives {
        AllDamageImmune_IncludingSpeculative 1
    }
}
```

---

### `CharmedDip`
**Source:** `familiars.gon`  

```
CharmedDip {
    variant_of Dip

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedFloater`
**Source:** `familiars.gon`  

```
CharmedFloater {
    variant_of Floater

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedPile`
**Source:** `familiars.gon`  

```
CharmedPile {
    variant_of Pile

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedMaggot`
**Source:** `familiars.gon`  

```
CharmedMaggot {
    variant_of Maggot

	graphics {
		tint [.7 1 .7 1]
	}

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedTumorousMaggot`
**Source:** `familiars.gon`  

```
CharmedTumorousMaggot {
    variant_of TumorousMaggot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedChargeyMaggot`
**Source:** `familiars.gon`  

```
CharmedChargeyMaggot {
    variant_of ChargeyMaggot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedSwappyMaggot`
**Source:** `familiars.gon`  

```
CharmedSwappyMaggot {
    variant_of SwappyMaggot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedRat`
**Source:** `familiars.gon`  

```
CharmedRat {
    variant_of Rat

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedKitten`
**Source:** `familiars.gon`  

```
CharmedKitten {
    variant_of Kitten

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `BuffCharmedKitten`
**Source:** `familiars.gon`  

```
BuffCharmedKitten {
    variant_of CharmedKitten

    passives {
        AllStatsUp 2
        HealthGain 8
    }
}
```

---

### `CharmedTomTom`
**Source:** `familiars.gon`  

```
CharmedTomTom {
    variant_of TomTom
	
	graphics {
		tint [.7 1 .7 1]
	}

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `BuffFamiliarMaggot`
**Source:** `familiars.gon`  

```
BuffFamiliarMaggot {
    variant_of Maggot

    properties {
        faction allies
        inherit_faction true
    }

    passives {
        AddDamage 1
        AddMaxHealth 5
        HealthGain 5 
    }

    abilities {
        can_get_bonus true
    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `BuffFamiliarPooter`
**Source:** `familiars.gon`  

```
BuffFamiliarPooter {
    variant_of Pooter

    properties {
        faction allies
        inherit_faction true
    }

    passives {
        AddDamage 1
        AddMaxHealth 5
        HealthGain 5 
    }

    abilities {
        can_get_bonus true
    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `BuffFamiliarFlea`
**Source:** `familiars.gon`  

```
BuffFamiliarFlea {
    variant_of Flea

    properties {
        faction allies
        inherit_faction true
    }

    passives {
        AddDamage 1
        AddMaxHealth 5
        HealthGain 5 
    }

    abilities {
        can_get_bonus true
    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `BuffFamiliarFly`
**Source:** `familiars.gon`  

```
BuffFamiliarFly {
    variant_of Fly

    properties {
        faction allies
        inherit_faction true
    }

    passives {
        AddDamage 1
        AddMaxHealth 5
        HealthGain 5 
    }

    abilities {
        can_get_bonus true
    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `RotFly`
**Name:** Rot Fly  
**Source:** `familiars.gon`  

```
RotFly {
    variant_of Fly

    graphics {
        name "FAMILIAR_ROTFLY_NAME"
        piece_alt_frame 3
    }

    properties {
        kill_required false
    }
}
```

---

### `AllyRotFly`
**Name:** Rot Fly  
**Source:** `familiars.gon`  

```
AllyRotFly {
    variant_of Fly

    graphics {
        name "FAMILIAR_ROTFLY_NAME"
        piece_alt_frame 3
    }

    properties {
        kill_required false
        inherit_faction true
    }
}
```

---

### `Deathbot`
**Name:** Deathbot  
**Source:** `familiars.gon`  

```
Deathbot {
    graphics {
        movieclip Deathbot
        name "FAMILIAR_DEATHBOT_NAME"
    }

    sound {
        alt_sounds [[HitGround SE_BuildBot_Land]]
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag robot
        faction allies
        inherit_faction true
        movement 4
        health 12
        weak_threshold 0
        corpse_health 0
        ai_scale .5
    }

    abilities {
        move DefaultMove
        attack Flamethrower
    }

    passives {
        Robot 1
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `TinkererTurret`
**Name:** Turret  
**Source:** `familiars.gon`  

```
TinkererTurret {
    graphics {
        movieclip Turret
        name "FAMILIAR_TURRET_NAME"
    }

    sound {
        alt_sounds [[HitGround SE_BuildBot_Land]]
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag robot
        faction allies
        movement 4
        health 3
        weak_threshold 0
        corpse_health 0
        ai_scale .5
        inherit_faction true
        auto_run_priority stationary
    }

    abilities {
        move None
        attack TurretShot
    }

    passives {
        Robot 1
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights keep_distance
        never_hit_ally_corpses true
    }
}
```

---

### `RocketTurret`
**Name:** Rocket Turret  
**Source:** `familiars.gon`  

```
RocketTurret {
    variant_of TinkererTurret

    graphics {
        name "FAMILIAR_ROCKETTURRET_NAME"
    }

    abilities {
        attack RocketTurretShot
    }

    ai {
        decision_weights default
    }
}
```

---

### `CharmedDemonKitten`
**Name:** Demon Kitten  
**Source:** `familiars.gon`  

```
CharmedDemonKitten {
    variant_of Hyde

    graphics {
        name "FAMILIAR_DEMONKITTEN_NAME"
        scale .8
        shadow_size .8
        spawnin_animation spawnin
    }

    stats {
        strength 5
    }

    properties {
        faction allies
        inherit_faction true

        health 14
    }
}
```

---

### `CharmedLeech`
**Name:** Leech  
**Source:** `familiars.gon`  

```
CharmedLeech {
    variant_of Maggot

    graphics {
        name "FAMILIAR_LEECH_NAME"
        
        piece_alt_frame 3
    }

    properties {
        faction allies
        inherit_faction true
    }

    passives {
        AddStatusToBasicAttack {
            RemoteFlatLeech 1
        }
    }
}
```

---

### `BeefyCharmedLeech`
**Name:** Beefy Leech  
**Source:** `familiars.gon`  

```
BeefyCharmedLeech {
    variant_of Maggot

    graphics {
        name "FAMILIAR_BEEFYLEECH_NAME"
        
        piece_alt_frame 3
        scale 1.5
    }

    stats {
        strength 4
    }

    properties {
        faction allies
        inherit_faction true
        health 8
        movement 4
        corpse_health 1
    }

    passives {
        AddStatusToBasicAttack {
            RemoteLeech 1
        }
    }
}
```

---

### `BestBud`
**Name:** Best Bud  
**Source:** `familiars.gon`  

```
BestBud {
    variant_of Maggot

    graphics {
        name "FAMILIAR_BESTBUD_NAME"
        
        piece_alt_frame 3
        scale 1.5
    }

    stats {
        strength 4
    }

    properties {
        faction allies
        inherit_faction true
        health 8
        movement 4
        corpse_health 1
    }

    passives {
        StatusOnSpawnIn {
            CaptureFamiliar 1
        }
        AddStatusToBasicAttack {
            RemoteLeech 1
        }
    }

    abilities {
        can_get_bonus true
    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `Catbot`
**Name:** Catbot  
**Source:** `familiars.gon`  

```
Catbot {
    graphics {
        movieclip _CAT
        name "FAMILIAR_CATBOT_NAME"
        custom_cat_data RoboTom
        alt_animations[[idle catbotIdle] [walk stompwalk]]
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat robot]
        type cat
        health 10
        base_mana_regen 999
        faction allies
        ai_scale .5
        inherit_faction true
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [

        ]
    }

    passives {
        TakeWeaponFromSpawner 1
        Robot 1
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `ZombieCatFamiliar`
**Name:** Zombie Kitten  
**Source:** `familiars.gon`  

```
ZombieCatFamiliar {
    graphics {
        movieclip _CAT
        name "FAMILIAR_ZOMBIEKITTEN_NAME"
        custom_cat_data ZombieCat
        spawnin_animation "digUp"

        scale .8
        shadow_size .8

        alt_animations[[idle zombieIdle] [walk zombieWalk]]
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 1
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat zombie]
        type cat
        health 6

        base_mana_regen 999
        faction allies
        movement 2
        ai_scale .5
        inherit_faction true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            ZombieFeastSmall
        ]
    }

    passives {
        Undead 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [ZombieFeastSmall, attack]
        }

        decision_weights zombie
        move_weights zombie
    }
}
```

---

### `NeutralZombieKitten`
**Source:** `familiars.gon`  

```
NeutralZombieKitten {
    variant_of ZombieCatFamiliar
    properties {
        faction third_party
    }
}
```

---

### `FeralZombieKitten`
**Source:** `familiars.gon`  

```
FeralZombieKitten {
    variant_of ZombieCatFamiliar
    properties {
        faction third_party
        inherit_faction false
    }

    passives {
        
        PermanentMadness 1
    }
}
```

---

### `SkeletonCatFamiliar`
**Name:** Skeleton Kitten  
**Source:** `familiars.gon`  

```
SkeletonCatFamiliar {
    graphics {
        movieclip _CAT
        name "FAMILIAR_SKELETONKITTEN_NAME"
        custom_cat_data SkeletonCat

        alt_animations[[idle skeletonIdle]]

        spawnin_animation "digUp"

        scale .8
        shadow_size .8
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag [cat skeleton]
        type cat
        health 0
        shield 6

        base_mana_regen 999
        initiative 10
        movement 2
        corpse_health 0

        faction allies
        ai_scale .5
        inherit_faction true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        NoHealthOnlyShield 1
        Undead 1
        StatusImmunity [Poison, Bleed]

        TransformOnDeathImmediately {
            obj SkeletonCatCorpseFamiliar
            first_turn keep_turns
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `SkeletonCatCorpseFamiliar`
**Name:** Skeleton Kitten  
**Source:** `familiars.gon`  

```
SkeletonCatCorpseFamiliar {
    graphics {
        movieclip _CAT
        name "FAMILIAR_SKELETONKITTEN_NAME"
        custom_cat_data SkeletonCat
        alt_animations [[idle dead] [weak dead] [hit skeletonCorpseHit] [deadhit skeletonCorpseHit] [stunned dead] [dying dead] [dead skeletonDead]]
        spawnin_animation skeletonDie

        scale .8
        shadow_size .8
    }

    properties {
        tag [cat skeleton]
        type cat
        health 0
        shield 6

        faction allies
        ai_scale .5
        inherit_faction true
        initiative 10
        corpse_health 0
    }

    abilities {
        move None
        attack None
    }

    passives {
        NoHealthOnlyShield 1
        Undead 1
        StatusImmunity [Poison, Bleed]
        CountAsCorpse 1

        TransformInXTurns {
            stacks 1
            object SkeletonCatRevivedFamiliar
            initiative keep_turns_end_turn
        }
    }
    ai {
        brain NoBrain
    }
}
```

---

### `SkeletonCatRevivedFamiliar`
**Source:** `familiars.gon`  

```
SkeletonCatRevivedFamiliar {
    variant_of SkeletonCatFamiliar
    graphics {
        spawnin_animation revive
    }
}
```

---

### `Bombchu`
**Name:** Bombchu  
**Source:** `familiars.gon`  

```
Bombchu {
    graphics {
        movieclip Bombchu
        name "FAMILIAR_BOMBCHU_NAME"
    }

    sound {
        alt_sounds [[HitGround SE_BuildBot_Land]]
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag robot
        faction allies
        inherit_faction true
        movement 1
        health 5
        base_mana_regen 999
        ai_scale .5
    }

    abilities {
        move DefaultMove
        attack RocketSkates_Bombchu
        
        spells [

        ]
    }

    passives {
        DeathRattle DecoyExplode
        Robot 1
        LoopingSoundWhileAlive Bomb_FuseLoop
    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights keep_distance_always_move
    }
}
```

---

### `MechSuit`
**Name:** Mech Suit  
**Source:** `familiars.gon`  

```
MechSuit {
    graphics {
        movieclip MechSuit
        name "FAMILIAR_MECHSUIT_NAME"
        uifloaters_offset 2
        shadow_size 2
    }

    stats {
        strength 8
        dexterity 5
        constitution 5
        intelligence 5
        speed 3
        charisma 5
        luck 5
    }
    
    properties {
        tag [robot mount]
        mana_matters true
        
        faction none
        inherit_faction false
        takes_main_turn false
        kill_required false

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack MechSuitPunch
        
        spells [
            MechSuitBarrage
            MechSuitDash
            MechSuitEject
        ]
    }

    passives {
        Robot 1
        Trample 3
        Mount {
            enter_ability EnterMech
            eject_ability MechSuitEject
        }
        DeathRattle MechExplode

        FormChanger {
            Unmounted {

            }
            Mounted {
                animation_suffix "Cat"
            }
        }
    }
    
    ai {
        brain MountBrain
        decision_weights default
        move_weights stay_close
        animate_choice true
    }
}
```

---

### `RoboVacuum`
**Name:** Robo-Vac  
**Source:** `familiars.gon`  

```
RoboVacuum {
    graphics {
        movieclip Roomba
        name "FAMILIAR_ROBOVAC_NAME"
        move_speed_multiplier 1.75
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag robot
        faction allies
        inherit_faction true
        movement 8
        health 3
        base_mana_regen 999
        ai_scale .5

        corpse_health 0
        can_collect_coins true
        can_eat_food true
    }

    abilities {
        move DefaultMove
        attack Roomba_Bump
        
        spells [

        ]
    }

    passives {
        SharePickupsWithSpawner 1
        TagGreed pickup
        Robot 1
    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights blind_move_far
    }
}
```

---

### `RoboVacuum2`
**Source:** `familiars.gon`  

```
RoboVacuum2 {
    variant_of RoboVacuum

    passives {
        SharePickupsWithSpawner 0 
        SharePickups {
            include_coins true
        }
    }
}
```

---

### `NurseBot`
**Name:** Nurse Bot  
**Source:** `familiars.gon`  

```
NurseBot {
    graphics {
        movieclip LoveBot
        name "FAMILIAR_NURSEBOT_NAME"
        uifloaters_offset 2
        scale .7
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag robot
        faction allies
        inherit_faction true
        auto_run_priority support

        health 5
        shield 5
    }

    abilities {
        move DefaultMove
        attack NurseBotHealCat

        spells [
            NurseBotHeal
        ]
    }

    passives {
        Robot 1
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [NurseBotHealCat NurseBotHeal]
        }

        decision_weights default
        move_weights stay_near_allies
    }
}
```

---

### `TeslaCoil`
**Name:** Tesla Coil  
**Source:** `familiars.gon`  

```
TeslaCoil {
    graphics {
        movieclip TeslaCoil
        name "FAMILIAR_TESLACOIL_NAME"
        shadow_size .25
    }

    properties {
        type object
        tag robot

        faction allies
        inherit_faction true

        health 5
        corpse_health 0
        can_be_backstabbed false
        kill_required false

        ai_scale .25
    }

    abilities {
        move None
        attack TeslaBolt

        spells [
            
        ]
    }

    passives {
        Robot {
            alternate_energized_effect {
                SpellDamageUp 1
            }
        }

        CounterAttack TeslaBolt
    }
    
    ai {
        brain PatternBrain
        pattern {
            do attack
        }

        decision_weights teslacoil
        move_weights stay_close
    }
}
```

---

### `FamiliarFetus`
**Name:** Fetus  
**Source:** `familiars.gon`  

```
FamiliarFetus {
    graphics {
        movieclip Fetus
        name "ENEMY_FETUS_NAME"
        tooltip "ENEMY_FETUS_DESC"
    }
    
    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag fetus
        faction allies
        inherit_faction true
        
        movement 2
        health 12
        base_mana_regen 3
    }
    
    abilities {
        move DefaultMove
        attack BasicShortLobbed_Water
        can_get_bonus true
        
        spells [
            DrinkUp
        ]
    }
    
    passives {
        WaterWalk 1
    }
    
    ai {
        brain PlayerBrain
        
        pattern {
            do_priority [attack DrinkUp]
        }
        
        decision_weights default
        move_weights keep_distance_always_move_prefer_water
    }
}
```

---

### `FamiliarFetusGusher`
**Name:** Fetus Gusher  
**Source:** `familiars.gon`  

```
FamiliarFetusGusher {
    graphics {
        movieclip FetusGusher
        name "ENEMY_FETUSGUSHER_NAME"
        tooltip "ENEMY_FETUSGUSHER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag fetus
        faction allies
        inherit_faction true
        
        movement 3
        health 15
        base_mana_regen 3
        round_end_bonus_turns 1
    }
    
    abilities {
        move SwimmerMove
        attack FetusGush
        can_get_bonus true
    }
    
    passives {
        WaterWalk 1
    }
    
    ai {
        brain PlayerBrain
        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `FamiliarBrainDrain`
**Source:** `familiars.gon`  

```
FamiliarBrainDrain {
    variant_of BrainDrain

    properties {
        faction allies
        inherit_faction true
    }

    abilities {
        can_get_bonus true
    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `FamiliarKirbyFetus`
**Source:** `familiars.gon`  

```
FamiliarKirbyFetus {
    variant_of KirbyFetus

    properties {
        faction allies
        inherit_faction true
    }
    
    abilities {
        can_get_bonus true
    }

    ai {
        brain PlayerBrain
    }

    ai_if_spawned_as_enemy {
        brain PatternBrain

        pattern {
            do KirbySuck
        }
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `SleepParalysisDemon`
**Name:** {SpawnedBy}'s Sleep Paralysis Demon  
**Source:** `familiars.gon`  

```
SleepParalysisDemon {
    variant_of Hyde

    graphics {
        name "FAMILIAR_SLEEPDEMON_NAME"
        spawnin_animation howl
        tint [0 0 0 1]

        tooltip "FAMILIAR_SLEEPDEMON_DESC"
    }

    stats {
        strength 7
    }

    properties {
        faction solitary_enemies
        corpse_health 0
        health 19
    }
}
```

---

### `RandomLivingPoop`
**Source:** `familiars.gon`  

```
RandomLivingPoop {
    alt_spawn_pool {
        CharmedDip 1
        CharmedFloater 1
        CharmedPile 1
    }

    properties {
        can_be_champion true
    }
}
```

---

### `GrubFamiliarBase`
**Name:** Grub  
**Source:** `familiars.gon`  

```
GrubFamiliarBase {
    variant_of Maggot

    graphics {
        name "FAMILIAR_GRUB_NAME"
    }

    properties {
        hidden_tag grub_familiar
        faction allies
        inherit_faction true
    }
    
    passives {
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            set_GrubFamiliarReturn
        ]
    }

    ai {
        decision_weights heal_others
        move_weights stay_close_always_move
    }
}
```

---

### `HeadGrubFamiliar`
**Name:** Head Grub  
**Source:** `familiars.gon`  

```
HeadGrubFamiliar {
    variant_of GrubFamiliarBase

    graphics {
        name "ARMOR_HEADGRUB_NAME"
    }
}
```

---

### `FaceGrubFamiliar`
**Name:** Face Grub  
**Source:** `familiars.gon`  

```
FaceGrubFamiliar {
    variant_of GrubFamiliarBase

    graphics {
        name "ARMOR_FACEGRUB_NAME"
    }
}
```

---

### `NeckGrubFamiliar`
**Name:** Neck Grub  
**Source:** `familiars.gon`  

```
NeckGrubFamiliar {
    variant_of GrubFamiliarBase

    graphics {
        name "ARMOR_NECKGRUB_NAME"
    }
}
```

---

### `CharmedPinky`
**Source:** `familiars.gon`  

```
CharmedPinky {
    variant_of Pinky

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedLeaper`
**Source:** `familiars.gon`  

```
CharmedLeaper {
    variant_of Leaper

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedHyde`
**Source:** `familiars.gon`  

```
CharmedHyde {
    variant_of Hyde

    stats {
        constitution 8
    }

    properties {
        faction allies
        inherit_faction true
    }

    abilities {
        can_get_bonus true
    }
    
    /*ai {
        brain PlayerBrain
    }*/
}
```

---

### `CharmedSpookie`
**Source:** `familiars.gon`  

```
CharmedSpookie {
    variant_of Spookie

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedDaddyShark`
**Source:** `familiars.gon`  

```
CharmedDaddyShark {
    variant_of DaddyShark

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedHeadTumor`
**Source:** `familiars.gon`  

```
CharmedHeadTumor {
    variant_of HeadTumor

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedFetus`
**Source:** `familiars.gon`  

```
CharmedFetus {
    variant_of Fetus

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedFetus2`
**Source:** `familiars.gon`  

```
CharmedFetus2 {
    variant_of CharmedFetus
    
    properties {
        health 24 
    }
}
```

---

### `CharmedLoveBot`
**Source:** `familiars.gon`  

```
CharmedLoveBot {
    variant_of LoveBot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedSecurityBot`
**Source:** `familiars.gon`  

```
CharmedSecurityBot {
    variant_of SecurityBot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedCopBot`
**Source:** `familiars.gon`  

```
CharmedCopBot {
    variant_of CopBot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedSoldierBot`
**Source:** `familiars.gon`  

```
CharmedSoldierBot {
    variant_of SoldierBot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedHangerBot`
**Source:** `familiars.gon`  

```
CharmedHangerBot {
    variant_of HangerBot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedDoctorBot`
**Source:** `familiars.gon`  

```
CharmedDoctorBot {
    variant_of DoctorBot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedTallBot`
**Source:** `familiars.gon`  

```
CharmedTallBot {
    variant_of TallBot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedFutureBot`
**Source:** `familiars.gon`  

```
CharmedFutureBot {
    variant_of FutureBot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedCaveBaby`
**Source:** `familiars.gon`  

```
CharmedCaveBaby {
    variant_of CaveBaby

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedMammoth`
**Source:** `familiars.gon`  

```
CharmedMammoth {
    variant_of Mammoth

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedTarBaby`
**Source:** `familiars.gon`  

```
CharmedTarBaby {
    variant_of TarBaby

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedRaptorBaby`
**Source:** `familiars.gon`  

```
CharmedRaptorBaby {
    variant_of RaptorBaby

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedCancerCat`
**Source:** `familiars.gon`  

```
CharmedCancerCat {
    variant_of CancerCat

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedFloast`
**Source:** `familiars.gon`  

```
CharmedFloast {
    variant_of Floast

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CatCopyClot`
**Name:** {SpawnedBy}'s Clot  
**Source:** `familiars.gon`  

```
CatCopyClot {
    variant_of Clot

    graphics {
        name "FAMILIAR_CATCOPYCLOT_NAME"
        tooltip "FAMILIAR_CATCOPYCLOT_DESC"
    }

    properties {
        faction allies
        inherit_faction true
    }

    abilities {
        spells [
            ClotEvolveCatCopy
            ClotFailEvolve
        ]
    }

    passives {
        SpawnerCatDataReference 1
    }

    ai {
        pattern {
            move_then_do_random [ClotEvolveCatCopy ClotFailEvolve]
        }
    }
}
```

---

### `CharmedRattleSnake`
**Source:** `familiars.gon`  

```
CharmedRattleSnake {
    variant_of RattleSnake

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedDustDevil`
**Source:** `familiars.gon`  

```
CharmedDustDevil {
    variant_of DustDevil

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedSnakeyBones`
**Source:** `familiars.gon`  

```
CharmedSnakeyBones {
    variant_of SnakeyBones

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedHornyCat`
**Source:** `familiars.gon`  

```
CharmedHornyCat {
    variant_of HornyCat

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedGunCat`
**Source:** `familiars.gon`  

```
CharmedGunCat {
    variant_of GunCat

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedScorpionCat`
**Source:** `familiars.gon`  

```
CharmedScorpionCat {
    variant_of ScorpionCat

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedMangy2`
**Source:** `familiars.gon`  

```
CharmedMangy2 {
    variant_of Mangy2

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedBabyDeathWorm`
**Source:** `familiars.gon`  

```
CharmedBabyDeathWorm {
    variant_of BabyDeathWorm

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedBigDemon`
**Source:** `familiars.gon`  

```
CharmedBigDemon {
    variant_of BigDemon

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedStacy`
**Source:** `familiars.gon`  

```
CharmedStacy {
    variant_of Stacy2p0

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedCultist`
**Source:** `familiars.gon`  

```
CharmedCultist {
    variant_of Cultist

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedTinySpider`
**Source:** `familiars.gon`  

```
CharmedTinySpider {
    variant_of TinySpider

	graphics {
		tint [.7 1 .7 1]
	}

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedLice`
**Source:** `familiars.gon`  

```
CharmedLice {
    variant_of Lice

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedGamete`
**Source:** `familiars.gon`  

```
CharmedGamete {
    variant_of Gamete

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedClot`
**Source:** `familiars.gon`  

```
CharmedClot {
    variant_of Clot

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedAmoeba`
**Source:** `familiars.gon`  

```
CharmedAmoeba {
    variant_of Amoeba
	scale .5

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedReaper`
**Source:** `familiars.gon`  

```
CharmedReaper {
    variant_of Reaper

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `Triachnid`
**Name:** Triachnid  
**Source:** `familiars.gon`  

```
Triachnid {
    graphics {
        movieclip Triachnid
        name "FAMILIAR_TRIACHNID_NAME"
        tooltip "FAMILIAR_TRIACHNID_DESC"
        move_speed_multiplier 1.75
		scale 1.3
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag bug
        faction allies
        inherit_faction true
        movement 8
        health 3
        base_mana_regen 999
        ai_scale .5
		dispersed_bonus_turns 1

        corpse_health 0
        can_collect_coins true
        can_eat_food true
    }

    abilities {
        move DefaultMove
        
        spells [
			tw_TriachnidSpawn
        ]
    }

    passives {
        SharePickupsWithSpawner 1
        TagGreed pickup
    }
    
    ai {
        brain GenericBrain
        decision_weights semi_simple
        move_weights blind_move_far
    }
}
```

---

### `CharmedMegaDino`
**Source:** `familiars.gon`  

```
CharmedMegaDino {
    variant_of MegaDinoLeg

    properties {
        faction allies
        inherit_faction true
    }
}
```

---

### `CharmedBear`
**Source:** `familiars.gon`  

```
CharmedBear {
    variant_of Bear

    ai {
        brain GenericBrain
    }
}
```

---

### `CharmedWhiteRabbit`
**Source:** `familiars.gon`  

```
CharmedWhiteRabbit {
    variant_of WhiteRabbit

    graphics {
        tooltip "FAMILIAR_WHITERABBIT_DESC"
    }

    passives {
        StatusEachTurnEnd {
            Conditional_BadRoll {
                odds 0.5
                Madness 1
            }
        }
    }

    properties {
        faction allies
        inherit_faction true
        dispersed_bonus_turns 0
    }
}
```

---

### `CharmedTinaFly`
**Name:** Tina's Friend  
**Source:** `familiars.gon`  

```
CharmedTinaFly {
    variant_of Fly

    graphics {
        name "FAMILIAR_TINAFLY_NAME"
		scale 1.2
		tint blue
    }

    properties {
		health 10
        faction allies
        inherit_faction true
    }
	
    passives {
        AddDamage 4
        HealthGain 1 
    } 
}
```

---

### `CharmedTinyTumor`
**Source:** `familiars.gon`  

```
CharmedTinyTumor {
    variant_of TinyTumor

    graphics {
		scale 1
    }
	
    damage_instance {
        effects {
            ConstitutionUp -1
        }
    }
	
    properties {
        faction allies
        inherit_faction true
        dispersed_bonus_turns 0
    }
}
```

---

### `CharmedMammothBaby`
**Source:** `familiars.gon`  

```
CharmedMammothBaby {
    variant_of MammothBaby

    properties {
        faction allies
        inherit_faction true
        dispersed_bonus_turns 0
    }
}
```

---

### `CharmedGeoLad`
**Source:** `familiars.gon`  

```
CharmedGeoLad {
    variant_of GeoLad

    properties {
        faction allies
        inherit_faction true
        dispersed_bonus_turns 0
    }
}
```

---

### `TheLost`
**Name:** The Lost  
**Source:** `familiars.gon`  

```
TheLost {
    variant_of Scary
	
    graphics {
        name "FAMILIAR_THELOST_NAME"
		scale .7
    }
	
    properties {
        faction allies
        inherit_faction true
        dispersed_bonus_turns 1
    }
}
```

---

### `TheIntruder`
**Name:** The Intruder  
**Source:** `familiars.gon`  

```
TheIntruder {
    variant_of TallSpiderCat

    graphics {
        name "FAMILIAR_THEINTRUDER_NAME"
		scale .5
    }
	
    properties {
        faction allies
        inherit_faction true
        dispersed_bonus_turns 2
    }
}
```

---

### `FamiliarFleshLad`
**Source:** `familiars.gon`  

```
FamiliarFleshLad {
    variant_of FleshLad

    graphics {
        tooltip "FAMILIAR_FLESHLAD_DESC"
    }

    properties {
        faction allies
        inherit_faction true
    }

    abilities {
        can_get_bonus true
    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `PhantomMaskRock`
**Name:** Phantom Mask  
**Source:** `familiars.gon`  

```
PhantomMaskRock {
    graphics {
        movieclip Mask
        shadow_size .50
        uifloaters_offset .5
		scale .7
        name "FAMILIAR_PHANTOMMASK_NAME"
        tooltip "FAMILIAR_PHANTOMMASK_DESC"
    }

    properties {
        faction allies
        tag rock
        type object
        takes_turns true
        
        can_be_backstabbed false
        kill_required false
        move_block nothing
        corpse_health 0
        initiative -80
        movement 2
        ai_scale .25

        health 1
    }

    abilities {
        move DefaultMove
        attack AnimatedRockAttack
        
        spells [
            
        ]
    }

    passives {
        SmallRockBehavior 5
        LimitHeal 0
        StripStatuses 1
        ReturnBoundItemOnBattleEnd 1
        AllDamageImmune_IncludingSpeculative 1
    }
    
    ai {
        brain GenericBrain
        decision_weights default_ignore_selfdamage
        move_weights stay_close
    }
}
```

---

### `TheCreator`
**Name:** The Creator  
**Source:** `finalboss.gon`  

```
TheCreator {
    graphics {
        movieclip FinalBossPhase1
        name "ENEMY_THECREATOR_NAME"
        uifloaters_offset 4
        water_mask square
        shadow_size 2
        dont_sink true
		tooltip "ENEMY_THECREATOR_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 0
        charisma 5
        luck 5
    }
    
    properties {
        faction enemies
        type boss
        tag [god humanoid]
        
        health 999

        size 2x2
        movement 0

        move_block everything_even_when_dead
        knockback_immune true
        takes_turns false

        lock_orientation [0 -1]
        banned_elite_buffs [Twin Depressing]
    }

    abilities {
        move None
        attack None

        spells [
            TheCreator_SpawnCloneTeam
            TheCreator_Reaction
            BecomeTheDestroyer
        ]
    }

    passives {
        CharacterLightSource {
            color [1, 1, 1]
            glow [1, 1, 1, .5]
            size 4
        }
        FullBlockEverythingTo0Damage 1
        AbilityOnBattleStart_UseAI TheCreator_SpawnCloneTeam
        DebuffImmunity 1
        BuffImmunity 1
        AbilityReaction {
            ability TheCreator_Reaction
            even_on_0_damage true
        }

        BungaEntrance {
            warrior_tag finalboss_clonecat
            ability BecomeTheDestroyer
            health_threshold -1
            even_if_stunned true
        }
    }
    
    ai {
        brain PatternBrain
        pattern {
            do_nothing []
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `PlayerCat_FinalBossClone`
**Name:** Good {Catname}  
**Source:** `finalboss.gon`  

```
PlayerCat_FinalBossClone {
    variant_of PlayerCat

    graphics {
        spawnin_animation portin
        name "ENEMY_CREATORCLONE_NAME"
    }

    properties {
        faction enemies
        hidden_tag finalboss_clonecat

        can_be_overkilled true
        allow_passive_spelltransforming true
        
        
        access_to_player_inventory false
        corpse_health 1
        is_player_cat false
        exclude_from_hallucinate true
        base_initiative -1

        disallow_items all

        force_not_familiar true

        banned_elite_buffs [Depressing]
    }

    passives {
        AdvancedTint [
            .6, .6, .6, 1 
            .5, .5, .5, 0      
        ]
    }

    ai {
        brain GenericBrain
    }
}
```

---

### `PlayerCat_FinalBossClone_Champion`
**Source:** `finalboss.gon`  

```
PlayerCat_FinalBossClone_Champion {
    variant_of PlayerCat_FinalBossClone

    properties {
        disallow_items Nuke
        champion true
    }
}
```

---

### `PlayerCat_FinalBossClone_Elite`
**Source:** `finalboss.gon`  

```
PlayerCat_FinalBossClone_Elite {
    variant_of PlayerCat_FinalBossClone

    properties {
        disallow_items Nuke
        champion true
        elite true
    }
}
```

---

### `TheDestroyer`
**Name:** The Destroyer  
**Source:** `finalboss.gon`  

```
TheDestroyer {
    graphics {
        movieclip FinalBossPhase2
        name "ENEMY_DESTROYER_NAME"
        uifloaters_offset 4
        water_mask square
        shadow_size 2
        no_splatter true
		tooltip "ENEMY_DESTROYER_DESC"
    }

    stats {
        strength 9
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        faction enemies
        type boss
        tag [god cat]
        
        health 500

        size 2x2
        movement 3

        move_block everything_even_when_dead
        dispersed_bonus_turns 1
        corpse_health 0
        can_be_overkilled false

        banned_elite_buffs [Twin]

        weak_threshold 0
    }

    abilities {
        move DefaultMove
        attack DestroyerAttack

        spells [
            DestroyerChargeBackflips
            DestroyerHolyAttack
            DestroyerThrowShield
            DestroyerDashAttack

            Destroyer2HolyAttack
            DestroyerPulse
            Destroyer2Pulse
            DestroyerDodge
            DestroyerBreakShield
            DestroyerRaise
        ]
    }

    passives {
        Trample 3

        FinalBossShieldHealth {
            state_health [
                0  
                35 
                35 
                35 
                35 
                0  
            ]
            break_ability DestroyerBreakShield
        }

        FinalBossBecomeTheChild {
            GlobalSpawnCharacter MegaGuppy
            PlayBackground 1
            SwitchMusic {
                new_song same
                new_layer event
            }
        }
        StatusOnDie {
            RemoveAmbientLightEffects 4
            RemoveGlobalModifiers [BloodRain]
        }

        FormChanger {
            SwordAndShield {
                attack DestroyerAttack

                passives {
                    FaceLastDamage {
                        use_turn_animations true
                    }
                    FinalBossShield DestroyerShieldBash

                    FormChangeWhilePrimingAbility {
                        priming SwordAndShield_Primed
                        not_priming SwordAndShield
                    }

                    AbilityOnRoundEnd {
                        ability DestroyerRaise
                        force_display_name true
                    }

                    CharacterLightSource {
                        color [1, 1, 1]
                        glow [1, 1, 1, .5]
                        size 2
                    }
                }

                ai {
                    brain PatternBrain
                    pattern {
                        do_priority [**DestroyerThrowShield attack]
                        do_priority [**DestroyerThrowShield DestroyerHolyAttack]
                        do_priority [**DestroyerThrowShield attack] 
                    }

                    decision_weights default
                    move_weights stay_close
                    fallback_advances_pattern true
                }
            }
            SwordAndShield_Primed {
                animation_suffix "Holy"
                attack DestroyerAttack

                passives {
                    FinalBossShield None
                    ImmediateAbilityReaction {
                        ability DestroyerPulse
                        even_if_blocked true
                    }

                    FormChangeWhilePrimingAbility {
                        priming SwordAndShield_Primed
                        not_priming SwordAndShield
                    }

                    CharacterLightSource {
                        color [1, 1, 1]
                        glow [1, 1, 1, .5]
                        size 8
                    }
                }

                ai { 
                    brain PatternBrain
                    pattern {
                        do move
                    }

                    decision_weights default
                    move_weights stay_close
                    fallback_advances_pattern true
                }
            }

            DualSword {
                move_speed_multiplier 1.5
                animation_suffix "2"
                attack DestroyerAttack2
                tooltip "ENEMY_DESTROYER2_DESC"

                passives {
                    StatusWhenStatusCompletelyRemoved {
                        status BackflipWhenTargeted
                        UseAbility {
                            ability Destroyer2HolyAttack
                            respect_prime true
                        }
                    }
                    FormChangeWhilePrimingAbility {
                        priming DualSword_Primed
                        not_priming DualSword
                    }

                    AbilityOnRoundEnd {
                        ability DestroyerRaise
                        force_display_name true
                    }

                    CharacterLightSource {
                        color [1, .9, .9]
                        size 4
                    }
                }

                ai {
                    brain PatternBrain
                    pattern {
                        do_all [attack *DestroyerDashAttack DestroyerDashAttack DestroyerChargeBackflips]
                    }

                    decision_weights default
                    move_weights keep_distance
                    fallback_advances_pattern true
                }
            }
            DualSword_Primed {
                move_speed_multiplier 1.5
                animation_suffix "Holy2"
                attack DestroyerAttack2
                tooltip "ENEMY_DESTROYER2_DESC"

                passives {
                    ImmediateAbilityReaction {
                        ability Destroyer2Pulse
                        even_if_blocked true
                    }
                    FormChangeWhilePrimingAbility {
                        priming DualSword_Primed
                        not_priming DualSword
                    }

                    CharacterLightSource {
                        color [1, .9, .9]
                        size 8
                    }
                }

                ai {
                    brain PatternBrain
                    pattern {
                        do_all [attack *DestroyerDashAttack DestroyerDashAttack DestroyerChargeBackflips]
                    }

                    decision_weights default
                    move_weights keep_distance
                    fallback_advances_pattern true
                }
            }
        }
    }
    
    ai {
        brain PatternBrain
        pattern {
            do_nothing []
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `TheDestroyer2`
**Source:** `finalboss.gon`  

```
TheDestroyer2 {
    variant_of TheDestroyer
	
    graphics {
		
    }

    passives {
        FormChanger {
            initial_form DualSword
        }
        CreateGlobalModifiers {
            LowerAmbientLight {
                amount [50% 60% 60%]
                speed 4
            }
            BloodRain 1
        }
    }
}
```

---

### `TheChild`
**Name:** The Child  
**Source:** `finalboss.gon`  

```
TheChild {
    graphics {
        movieclip FinalBossPhase3
        name "ENEMY_THECHILD_NAME"
        uifloaters_offset 2
        shadow_size 2
        water_mask square
		tooltip "ENEMY_THECHILD_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        faction enemies
        type boss
        tag [god cat fetus]
        
        health 400

        size 2x2
        movement 3
        flying true

        move_block everything_even_when_dead
        takes_turns false
        corpse_health indestructible

        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack None

        spells [
            TheChild_ReleaseBeams
            TheChild_TargetBeam
            TheChild_Wrath
            TheChild_Pulse

            TheChild_TransformHoly
            TheChild_TransformExplosive
            TheChild_TransformBoris
        ]
    }

    passives {
        CharacterLightSource {
            color [1, 1, 1]
            glow [1, .75, .5, .5]
            size 2
        }
        Trample 3
        StunImmunity 1
        FinalBossSyncAnimations {
            other_character MegaGuppy

            other_form_change_abilities {
                Holy MegaGuppy_TransformHoly
                Boris MegaGuppy_TransformBoris
                Explosive MegaGuppy_TransformExplosive
            }
        }
        

        FormChanger {
            Holy {
                animation_suffix "1"

                passives {
                    FinalBossHitCountdownHoly {
                        stacks 7
                        icon 804
                        icon_ready 805
                    }
                    FinalBossBeamQueue {
                        queue TheChild_TargetBeam
                        release TheChild_ReleaseBeams
                        transform TheChild_TransformBoris
                    }
                }
            }
            Boris {
                animation_suffix "2"

                passives {
                    MoveTowardsDamageSource {
                        move_ability MoveOne
                        check_in_form Boris
                        check_has_status FinalBossHitCountdownBoris
                    }

                    FinalBossHitCountdownBoris {
                        stacks 7
                        icon 802
                        icon_ready 803

                        ForceUseAbility {
                            ability TheChild_Pulse
                            show_name true
                        }
                        ForceUseAbility TheChild_TransformExplosive
                    }
                }
            }
            Explosive {
                animation_suffix "3"

                passives {
                    FinalBossHitCountdownExplosive {
                        stacks 7
                        icon 800
                        icon_ready 801

                        ForceUseAbility {
                            ability TheChild_Wrath
                            show_name true
                        }
                        ForceUseAbility TheChild_TransformHoly
                    }
                    PassiveWhileNotHasStatus {
                        status ExistUntilIdleUpkeep
                        passives {
                            DisplayDangerAOE TheChild_Wrath
                        }
                    }
                }
            }
        }
    }
    
    ai {
        brain PatternBrain
        pattern {
            do_nothing []
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `MegaGuppy`
**Name:** The Father  
**Source:** `finalboss.gon`  

```
MegaGuppy {
    graphics {
        movieclip FinalBossMegaGuppy
        name "ENEMY_THEFATHER_NAME"
        uifloaters_offset 2
        shadow_size 2
        
        non_blocking_animations ["hit", "critical"]
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        faction enemies
        type boss
        tag [god cat]
        
        health 999

        size 1x1

        initiative -999

        move_block everything_even_when_dead
        can_be_champion false
        lock_orientation [0 -1]
        allow_offmap_corpse true

        weak_threshold 0
    }

    abilities {
        move None
        attack None

        spells [
            MegaGuppy_SlamRight
            MegaGuppy_SlamLeft

            MegaGuppy_TransformHoly
            MegaGuppy_TransformExplosive
            MegaGuppy_TransformBoris
            MegaGuppy_SummonTheChild
        ]
    }

    passives {
        StartOffMap 1
        InsertIntoBackgroundPlaceholder 1
        UseAbility MegaGuppy_SummonTheChild
        FinalBossPupils {
            radius 13
            virtual_head_position [11 2 11]
            look_at_offset [0 2.5 0]

            teleport_tracking_halflife .01
            reset_center_because_of_animation_halflife .05
            reset_center_because_no_target_halflife .1
            tracking_acquisition_halflife .1
        }

        FormChanger {
            Holy {
                animation_suffix "1"
            }
            Boris {
                animation_suffix "2"
            }
            Explosive {
                animation_suffix "3"
            }
        }
    }
    
    ai {
        brain PatternBrain
        pattern {
            do MegaGuppy_SlamRight
            do MegaGuppy_SlamLeft
        }

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Debug_MegaGuppyPhase3`
**Source:** `finalboss.gon`  

```
Debug_MegaGuppyPhase3 {
    variant_of Dummy    

    passives {
        StartOffMap 1
    }

    properties {
        takes_main_turn false
        round_start_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            DbgBackgroundTransitionTest
        ]
    }

    ai {
        brain PatternBrain
        pattern {
            do DbgBackgroundTransitionTest
        }
    }
}
```

---

### `Guillotina2Head`
**Name:** Guillotina  
**Source:** `guillotina.gon`  

```
Guillotina2Head {
    graphics {
        movieclip Guillotina2Head
        name "ENEMY_GUILLOTINA_NAME"
        move_speed_sync_frames 29
		tooltip "ENEMY_TINA2HEAD_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 8
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        dispersed_bonus_turns 2
        dispersed_bonus_turns_before_cats true
        initiative 999
        corpse_health indestructible

        
        mana_regen 999
        mana 100
        
        health 250
        weak_threshold 50
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack TinaHeadGutSpear
        
        spells [
            YeetTowardsBuddy
            Magnetize
            Guillotina2Rage
            GuillotinaTossCollide
            Tina2Call
        ]
    }

    passives {
        Buddy Guillotina2Body

        FormChanger {
            Normal { 
                passives {
                    AbilityWhenBuddyDies Guillotina2Rage
                }
            }
            Rage {
                partial_animation_suffix "Rage"

                ai {
                    brain PatternBrain

                    pattern {
                        do_random [Magnetize, attack, GuillotinaTossCollide, YeetTowardsBuddy, Tina2Call, Tina2Call]
                    }

                    fallback {
                        do_best [Magnetize, attack, GuillotinaTossCollide, YeetTowardsBuddy, Tina2Call]
                    }

                    decision_weights default
                    move_weights keep_distance_always_move
                    fallback_advances_pattern true
                    stun_advances_pattern true
                }

                turns {
                    dispersed_bonus_turns 3
                }
            }

            initial_form Normal
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do Magnetize
            do attack
            do YeetTowardsBuddy
        }

        fallback {
            do_priority [attack, Magnetize, YeetTowardsBuddy]
        }

        decision_weights default
        move_weights keep_distance_always_move
        fallback_advances_pattern true
        stun_advances_pattern true
    }
}
```

---

### `Guillotina2Body`
**Name:** Guillotina  
**Source:** `guillotina.gon`  

```
Guillotina2Body {
    graphics {
        movieclip Guillotina2Body
        name "ENEMY_GUILLOTINA_NAME"
        shadow_size 2
        uifloaters_offset 2
		tooltip "ENEMY_TINA2BODY_DESC"
    }

    stats {
        strength 8
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        initiative -999
        movement 1
        corpse_health indestructible

        size 2x2
        move_block everything_even_when_dead

        
        mana_regen 999
        mana 100
        
        health 250
        weak_threshold 50
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack TinaBodySlam
        
        spells [
            TinaBodySlamMax
            Guillotina2Rage
            TinaBodySlamRage
            TinaTantrum
        ]
    }

    passives {
        Buddy Guillotina2Head
        Trample 3

        FormChanger {
            Normal { 
                passives {
                    AbilityWhenBuddyDies Guillotina2Rage
                }
            }
            Rage {
                partial_animation_suffix "Rage"
        
                ai {
                    brain PatternBrain

                    pattern {
                        do TinaTantrum
                        do TinaBodySlamRage
                    }

                    decision_weights careless
                    move_weights stay_close_move_far
                }

                turns {
                    dispersed_bonus_turns 1
                }

                passives {
                    AddMovement 3
                }
            }
        
            initial_form Normal
        }

        PassiveWhenDead {
            AddStatusToTrampleDamage {
                Bruise 1
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [*TinaBodySlamMax, *TinaBodySlam, TinaBodySlamMax, TinaBodySlam]
        }

        decision_weights careless
        move_weights stay_close
    }
}
```

---

### `Guillotina1`
**Name:** Guillotina  
**Source:** `guillotina.gon`  

```
Guillotina1 {
    graphics {
        movieclip Guillotina1
        name "ENEMY_GUILLOTINA_NAME"
        shadow_size 2
        uifloaters_offset 2
		tooltip "ENEMY_TINA1_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 4
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        movement 3
        corpse_health indestructible

        size 2x2
        move_block everything_even_when_dead
        dispersed_bonus_turns 2

        
        mana_regen 999
        mana 100
        
        health 400
        weak_threshold 50
    }

    abilities {
        move DefaultMove
        attack TinaBasicBigMelee
        
        spells [
            TinaBasicJump
            TinaJumpAttack
            TinaSuck
            TinaSpit
            TinaThrow

            Guillotina1Rage
            
            BellyPound
            Digest
            TinaSuck2
            TinaSpit2
        ]
    }

    passives {
        Trample 3
        GuillotinaDeathHead 1

        FormChanger {
            
            Normal { 
                attack TinaBasicBigMeleeA

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has MouthFull
                        form_hasnot Normal
                    }
                    AbilityHealthThreshold {
                        threshold 200
                        ability Guillotina1Rage
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [*Guillotina1Rage, TinaJumpAttack, *TinaThrow, TinaThrow, move]
                        do_priority [*Guillotina1Rage, *TinaThrow, TinaThrow, TinaJumpAttack, move]
                        do_priority [*Guillotina1Rage, *TinaSuck]
                    }

                    decision_weights default
                    move_weights stay_close
                    reset_pattern_on_formswitch true
                    fallback_advances_pattern true
                }
            }
            MouthFull {
                partial_animation_suffix "MouthFull"

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has MouthFull
                        form_hasnot Normal
                    }
                    ChanceToSpitOnDamage {
                        chance_per_damage 2%
                        ability TinaSpit
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do *TinaSpit
                    }

                    decision_weights default
                    move_weights stay_close
                    end_turn_on_formswitch true
                    reset_pattern_on_formswitch true
                }
            }

            
            Rage {
                partial_animation_suffix "Rage"

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has BellyFull
                        form_hasnot Rage
                    }
                    AddMovement 1
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [TinaJumpAttack, *attack, attack, move]
                        do_priority [*attack, attack, TinaJumpAttack, move]
                        do_priority [*TinaSuck2, TinaSuck2, *attack, attack]
                    }

                    decision_weights default
                    move_weights stay_close
                    reset_pattern_on_formswitch true
                }
            }
            BellyFull {
                partial_animation_suffix "Belly"

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has BellyFull
                        form_hasnot Rage
                    }
                    ChanceToSpitOnDamage {
                        chance_per_damage 2%
                        ability TinaSpit2
                    }
                    DigestDeadBodies Digest
                    AddMovement 1
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [*attack, attack, BellyPound]
                        do *BellyPound
                        do_priority [*attack, attack, BellyPound]
                        do *Digest
                    }

                    decision_weights default
                    move_weights stay_close
                    end_turn_on_formswitch true
                    reset_pattern_on_formswitch true
                }
            }

            initial_form Normal
        }
    }
    
    ai {
        brain NoBrain

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Guillotina3Body`
**Name:** Guillotina  
**Source:** `guillotina.gon`  

```
Guillotina3Body {
    graphics {
        movieclip Guillotina3Body
        name "ENEMY_GUILLOTINA_NAME"
        shadow_size 2
        uifloaters_offset 2
		tooltip "ENEMY_TINA3BODY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        movement 2
        corpse_health 0

        size 2x2
        move_block everything_even_when_dead
        dispersed_bonus_turns 2

        
        mana_regen 999
        mana 100
        
        health 400
        weak_threshold 50
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [
            G3RunToHead
            G3GrabHead
            G3TossHead
            G3Scream_Hex
            G3Shake
            G3SpawnMama
            G3RageShake
        ]
    }

    passives {
        Trample 3
        Buddy Guillotina3Head

        FormChanger {
            
            Normal { 

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has Holding
                        form_hasnot Normal
                    }
                    AbilityHealthThreshold {
                        threshold 250
                        ability G3SpawnMama
                        use_ai true
                        also_use_if_buddy_is_dead true
                    }
                    AggroTargetIsBuddy 1
                }

                ai {
                    brain PatternBrain
                    auto_orient false

                    virtual_abilities {
                        MoveToHead {
                            ability G3RunToHead
                            move_for_ability G3GrabHead
                            move_weights minimum_move
                        }
                    }

                    bonusturn_pattern {
                        do_priority [G3GrabHead move *G3GrabHead]
                    }
                    pattern {
                        do **G3Shake
                    }

                    decision_weights default
                    move_weights towards_aggro
                    reset_pattern_on_formswitch true
                    fallback_advances_pattern true
                }
            }
            Holding {
                partial_animation_suffix "Holding"

                passives {
                    AddMovement 1
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has Holding
                        form_hasnot Normal
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do *G3Scream_Hex
                        do G3TossHead
                    }

                    decision_weights default
                    move_weights stay_far
                    end_turn_on_formswitch true
                    reset_pattern_on_formswitch true
                }
            }

            
            Rage {
                partial_animation_suffix "Rage"

                passives {
                    AddMovement 1

                    SpawnThingOnDamage {
                        object Maggot
                        good false 
                        spawn_on_death_hit false
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do move
                        do_all [move G3RageShake]
                    }

                    decision_weights default
                    move_weights blind_move_far
                    reset_pattern_on_formswitch true
                }
            }

            initial_form Normal
        }
    }
    
    ai {
        brain NoBrain

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Guillotina3Head`
**Name:** Guillotina  
**Source:** `guillotina.gon`  

```
Guillotina3Head {
    graphics {
        movieclip Guillotina3Head
        name "ENEMY_GUILLOTINA_NAME"
        
	    tooltip "ENEMY_TINA3HEAD_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        corpse_health indestructible

        
        mana_regen 999
        mana 100
        
        health 200
        weak_threshold 50
        banned_elite_buffs [Twin]
    }

    abilities {
        move None
        attack G3PrisonSpit
        
        spells [
            G3CoughFly
            G3CallForHelp
        ]
    }

    passives {
        Buddy Guillotina3Body
        
        AbilityReaction {
            ability G3CallForHelp
            only_when_not_your_turn true
            enemies_only true
            ability_damage_only true
        }
        MinimumKnockbackFromPhysicalAttacks 1
        Trample 3

        FormChanger {
            Normal {
                turns {
                    takes_turns true
                }
            }
            Holding {
                turns {
                    takes_turns false
                }
            }
            Rage {
                
                turns {
                    takes_turns true
                }

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights stay_close

                    pattern {
                        do G3CallForHelp
                    }
                }
            }
        }
        SyncFormsWithBuddy {
            no_buddy Rage
        }
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights stay_close

        pattern {
            do_priority [attack G3CallForHelp]
        }
    }
}
```

---

### `MamaMaggotTina`
**Source:** `guillotina.gon`  

```
MamaMaggotTina {
    variant_of MaggotLord

    graphics {
        spawnin_animation tinaspawnin
    }
}
```

---

### `IceBlock`
**Name:** Ice Cube  
**Source:** `inanimate_objects.gon`  

```
IceBlock {
    graphics {
        movieclip IceCube
        name "OBJECT_ICECUBE_NAME"
        water_mask square

        tooltip "OBJECT_ICECUBE_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        inanimate true
        corpse_health 0
        can_be_backstabbed false
        kill_required false
        
        elements [
            Ice
        ]
    }

    abilities {
        move None
        attack None
    }

    passives {
        IceBlockBehavior 1
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `GasCloud`
**Name:** Gas Cloud  
**Source:** `inanimate_objects.gon`  

```
GasCloud {
    graphics {
        movieclip GasCloud
        name "OBJECT_GASCLOUD_NAME"
        depth_offset -.1
    }

    properties {
        faction none
        type object
        takes_turns false
        inanimate true
        layer gas
        flying true
        corpse_health 0
        can_be_backstabbed false
        kill_required false
        
        elements [
            Poison
        ]
    }

    abilities {
        move None
        attack None
    }

    passives {
        GasCloudBehavior 2
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `DustCloud`
**Name:** Dust Cloud  
**Source:** `inanimate_objects.gon`  

```
DustCloud {
    graphics {
        movieclip DustCloud
        name "OBJECT_DUSTCLOUD_NAME"
        depth_offset -.1
    }

    properties {
        faction none
        type object
        takes_turns false
        inanimate true
        layer gas
        flying true
        corpse_health 0
        can_be_backstabbed false
        kill_required false
        
        elements [
            Dust
        ]
    }

    abilities {
        move None
        attack None
    }

    passives {
        DustCloudBehavior 1
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Bomb`
**Name:** Rat Bomb  
**Source:** `inanimate_objects.gon`  

```
Bomb {
    graphics {
        movieclip Bomb
        name "OBJECT_RATBOMB_NAME"

        tooltip "OBJECT_RATBOMB_DESC"
    }

    sound {
        alt_sounds [[HitGround Bomb_Land]]
    }

    properties {
        health 1
        tag bomb
        initiative -20
        can_be_backstabbed false
        faction none
        inherit_faction true
        type object
        
        
        corpse_health 1
        kill_required false
        ai_scale .5
    }
    
    abilities {
        move None
        attack BombExplode
    }

    passives {
        BombBehavior 1
        LoopingSoundWhileAlive Bomb_FuseLoop
    }
    
    ai {
        brain GenericBrain
        animate_choice false
    }
}
```

---

### `Rock`
**Name:** Rock  
**Source:** `inanimate_objects.gon`  

```
Rock {
    graphics {
        movieclip BigRock
        name "OBJECT_ROCK_NAME"
        shadow_size .50
        water_mask medium
    }
    sound {
		alt_sounds [[HitGround Obj_BigRockLand]]
	}
    

    properties {
        faction none
        type object
        takes_turns false
        health 30
        corpse_health 0
        knockback_immune true
        can_be_backstabbed false
        kill_required false
        
        elements [
            Rock
        ]
    }

    abilities {
        move None
        attack None
    }

    passives {

    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Junk`
**Name:** Junk  
**Source:** `inanimate_objects.gon`  

```
Junk {
    graphics {
        movieclip Junk
        name "OBJECT_JUNK_NAME"
        shadow None
        water_mask square
		
		tooltip "OBJECT_JUNK_DESC"
    }
    sound {
	    alt_sounds [[HitGround Obj_JunkLand]]
    }

    properties {
        faction none
        type object
        tag trash
        takes_turns false
        health 1
        corpse_health 0
        can_be_backstabbed false
        kill_required false
    }

    abilities {
        move None
        attack None
    }

    passives {

    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Tumor`
**Name:** Tumor  
**Source:** `inanimate_objects.gon`  

```
Tumor {
    graphics {
        movieclip Tumor
        name "OBJECT_TUMOR_NAME"
        scale .8
        shadow None
    }
    sound {
		alt_sounds [[HitGround Obj_TumorLand]]
	}

    properties {
        faction none
        type object
        takes_turns false
        health 1
        corpse_health 0
        can_be_backstabbed false
        kill_required false
        visually_spiky true
    }

    abilities {
        move None
        attack None
    }

    passives {
        Thorns 1
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `TrashBag`
**Name:** Trash Bag  
**Source:** `inanimate_objects.gon`  

```
TrashBag {
    graphics {
        movieclip TrashBag
        name "OBJECT_TRASHBAG_NAME"
        water_mask medmed

        tooltip "OBJECT_TRASHBAG_DESC"
    }
    sound {
    	alt_sounds [[HitGround Obj_TrashBagLand]]
    }

    properties {
        faction none
        type object
        tag [trash container]
        takes_turns false
        corpse_health 0
        health 25
        can_be_backstabbed false
        can_collect_coins true
        held_coins [5 10]
        kill_required false
    }

    abilities {
        move None
        attack None
    }

    passives {
        SpawnThingOnDamage {
            object RandomPickup
            coins 1
        }

        BirdRewards {
            statuses {
            }
            ally_rewards {
                Conditional_GoodRoll {
                    odds 5%
                    FindItemFromPool chapter
                }
            }
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Dumpster_interactive`
**Name:** Dumpster  
**Source:** `inanimate_objects.gon`  

```
Dumpster_interactive {
    graphics {
        movieclip Dumpster
        name "OBJECT_DUMPSTER_NAME"
        shade_occluded_objects true
        water_mask square

        tooltip "OBJECT_DUMPSTER_DESC"
    }

    properties {
        faction none
        type object
        size 2x2
        takes_turns false
        corpse_health 0
        health 100
        can_be_backstabbed false
        can_collect_coins true
        held_coins [2 15]
        kill_required false
    }

    abilities {
        move None
        attack None
    }

    passives {
        SpawnThingOnDamage {
            object Coin
            coins 1
            chance .25
            good true 
        }
        SpawnThingOnDamage {
            object Food
            chance .25
            good true 
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `SmallRock`
**Name:** Small Rock  
**Source:** `inanimate_objects.gon`  

```
SmallRock {
    graphics {
        movieclip SmallRock
        name "OBJECT_SMALLROCK_NAME"
        shadow_size .50
        uifloaters_offset .5

        tooltip "OBJECT_SMALLROCK_DESC"
    }
    sound {
        alt_sounds [[HitGround Obj_Rock_Land]]
    }

    properties {
        faction none
        tag rock
        type object
        takes_turns false
        
        can_be_backstabbed false
        kill_required false
        move_block nothing
        corpse_health 0

        health 3
    }

    abilities {
        move None
        attack None
    }

    passives {
        SmallRockBehavior 5
        LimitDamage 1
        LimitHeal 0
        StripStatuses 1

        FormChanger {
            default {

                passives {
                    FormChangeOnElementInfluence {
                        element very_hot
                        exclude water
                        form hot
                    }
                }
            }
            hot {
                name "OBJECT_HOTROCK_NAME"
                animation_suffix "Hot"

                passives {
                    InnateElement Fire
                    MeleeRevengeDamage {
                        effects {
                            Burn 2
                        }
                        elements [
                            Fire
                        ]
                    }
                    
                    FormChangeOnElementInfluence {
                        element water
                        form default
                        particle FireExtinguish
                        sfx FireExtinguish
                    }
                }
            }
            initial_form default
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `SmallLavaRock`
**Source:** `inanimate_objects.gon`  

```
SmallLavaRock {
    variant_of SmallRock

    passives {
        FormChanger {
            initial_form hot
        }
    }
}
```

---

### `AnimatedSmallRock`
**Name:** Pet Rock  
**Source:** `inanimate_objects.gon`  

```
AnimatedSmallRock {
    graphics {
        movieclip PetRock
        name "OBJECT_PETROCK_NAME"
        shadow_size .50
        uifloaters_offset .5

        tooltip "OBJECT_PETROCK_DESC"
    }
    sound {
        alt_sounds [[HitGround Obj_Rock_Land]]
    }

    properties {
        faction allies
        tag rock
        type object
        takes_turns true
        
        can_be_backstabbed false
        kill_required false
        move_block nothing
        corpse_health 0
        initiative -80
        movement 2
        ai_scale .25

        health 3
    }

    abilities {
        move DefaultMove
        attack AnimatedRockAttack
        
        spells [
            
        ]
    }

    passives {
        SmallRockBehavior 5
        LimitDamage 1
        LimitHeal 0
        StripStatuses 1

        FormChanger {
            default {

                passives {
                    FormChangeOnElementInfluence {
                        element very_hot
                        exclude water
                        form hot
                    }
                }
            }
            hot {
                name "OBJECT_HOTPETROCK_NAME"
                animation_suffix "Hot"

                passives {
                    InnateElement Fire
                    MeleeRevengeDamage {
                        effects {
                            Burn 2
                        }
                        elements [
                            Fire
                        ]
                    }
                    
                    FormChangeOnElementInfluence {
                        element water
                        form default
                        particle FireExtinguish
                        sfx FireExtinguish
                    }
                }
            }
            initial_form default
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default_ignore_selfdamage
        move_weights stay_close
    }
}
```

---

### `AnimatedSmallLavaRock`
**Source:** `inanimate_objects.gon`  

```
AnimatedSmallLavaRock {
    variant_of AnimatedSmallRock

    passives {
        FormChanger {
            initial_form hot
        }
    }
}
```

---

### `Boulder`
**Name:** Boulder  
**Source:** `inanimate_objects.gon`  

```
Boulder {
    graphics {
        movieclip Boulder
        name "OBJECT_BOULDER_NAME"

        tooltip "OBJECT_BOULDER_DESC"
    }
    sound {
        alt_sounds [
            [HitGround Obj_BoulderLand]
            [SE_PetRock_Dash SE_PetBoulder_Dash]
        ]
    }

    properties {
        faction none
        tag rock
        type object
        takes_turns false
        
        can_be_backstabbed false
        kill_required false
        corpse_health 0

        health 8
    }

    abilities {
        move None
        attack None
    }

    passives {
        SmallRockBehavior {
            damage 9
            knockback 1
        }
        LimitDamage 1
        LimitHeal 0
        StripStatuses 1

        FormChanger {
            default {
            }
            hot {
                name "OBJECT_HOTBOULDER_NAME"
                animation_suffix "Hot"

                passives {
                    InnateElement Fire
                    MeleeRevengeDamage {
                        effects {
                            Burn 2
                        }
                        elements [
                            Fire
                        ]
                    }
                }
            }
            initial_form default
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `LavaBoulder`
**Source:** `inanimate_objects.gon`  

```
LavaBoulder {
    variant_of Boulder

    passives {
        FormChanger {
            initial_form hot
        }
    }
}
```

---

### `AnimatedBoulder`
**Name:** Pet Boulder  
**Source:** `inanimate_objects.gon`  

```
AnimatedBoulder {
    graphics {
        movieclip PetBoulder
        name "OBJECT_PETBOULDER_NAME"

        tooltip "OBJECT_PETBOULDER_DESC"
    }

    properties {
        faction allies
        tag rock
        type object
        takes_turns true
        
        can_be_backstabbed false
        kill_required false
        corpse_health 0
        initiative -80
        movement 1
        ai_scale .25

        health 8
    }

    abilities {
        move DefaultMove
        attack AnimatedRockAttack
        
        spells [
            
        ]
    }

    passives {
        SmallRockBehavior {
            damage 5
            knockback 1
        }
        LimitDamage 1
        LimitHeal 0
        StripStatuses 1

        FormChanger {
            default {

                passives {
                    FormChangeOnElementInfluence {
                        element very_hot
                        exclude water
                        form hot
                    }
                }
            }
            hot {
                name "OBJECT_HOTPETBOULDER_NAME"
                animation_suffix "Hot"

                passives {
                    InnateElement Fire
                    MeleeRevengeDamage {
                        effects {
                            Burn 2
                        }
                        elements [
                            Fire
                        ]
                    }
                    
                    FormChangeOnElementInfluence {
                        element water
                        form default
                        particle FireExtinguish
                        sfx FireExtinguish
                    }
                }
            }
            initial_form default
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default_ignore_selfdamage
        move_weights stay_close
    }
}
```

---

### `AnimatedLavaBoulder`
**Source:** `inanimate_objects.gon`  

```
AnimatedLavaBoulder {
    variant_of AnimatedBoulder

    passives {
        FormChanger {
            initial_form hot
        }
    }
}
```

---

### `Tire`
**Name:** Tire  
**Source:** `inanimate_objects.gon`  

```
Tire {
    graphics {
        movieclip Tire
        name "OBJECT_TIRE_NAME"
        water_mask medium

        tooltip "OBJECT_TIRE_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_TireLand]]
	}

    properties {
        faction none
        type object
        takes_turns false
        inanimate true
        can_be_backstabbed false
        kill_required false

        inanimate_can_receive_specific_statuses [Burn]
    }

    abilities {
        move None
        attack None
    }

    passives {
        FormChanger {
            Down {
                passives {
                    TireBehavior 1
                }
            }
            Up {
                animation_suffix "Up"
                tooltip "OBJECT_TIREUP_DESC"

                passives {
                    UpTireBehavior 5
                }
            }

            initial_form Down
        }

        PassiveWhenAffectedByElement {
            element Fire
            passives {
                TileTrail_Ahead FireTile
            }
        }

        DiesToPiercingAndSpikes {
            deferred true
        }

    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Tire_Up`
**Source:** `inanimate_objects.gon`  

```
Tire_Up {
    variant_of Tire

    passives {
        FormChanger {
            initial_form Up
        }
    }
}
```

---

### `Crate`
**Name:** Crate  
**Source:** `inanimate_objects.gon`  

```
Crate {
    graphics {
        movieclip Crate
        name "OBJECT_CRATE_NAME"
        water_mask square

        tooltip "OBJECT_CRATE_DESC"
    }

    sound {
        alt_sounds [
            [DamageHealthMed SE_CrateDamage]
        ]
    }

    properties {
        faction none
        type object
        tag container
        takes_turns false
        health 10
        corpse_health 0
        can_be_backstabbed false
        held_coins [1 10]
        kill_required false
    }

    abilities {
        move None
        attack None
    }

    passives {

    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Crate_WithItemChance`
**Source:** `inanimate_objects.gon`  

```
Crate_WithItemChance {
    variant_of Crate
    passives {
        BirdRewards {
            statuses {
            }
            ally_rewards {
                Conditional_GoodRoll {
                    odds 33%
                    FindItemFromPool chapter
                }
            }
        }
    }
}
```

---

### `GasCan`
**Name:** Gas Can  
**Source:** `inanimate_objects.gon`  

```
GasCan {
    graphics {
        movieclip GasCan
        name "OBJECT_GASCAN_NAME"
    }

    properties {
        health 10
        can_be_backstabbed false
        faction none
        type object
        takes_turns false
        
        corpse_health 0
        kill_required false
    }
    
    abilities {
        move None
        attack GasCanExplode
    }

    passives {
        GasCanBehavior 1
        ChangeTileOnPop OilTile
    }
    
    ai {
        brain NoBrain
        animate_choice false
    }
}
```

---

### `Poop`
**Name:** Poop  
**Source:** `inanimate_objects.gon`  

```
Poop {
    graphics {
        movieclip Poop
        name "OBJECT_POOP_NAME"
    }
    sound {
		alt_sounds [[HitGround Obj_PoopLand]]
	}

    properties {
        faction none
        type object
        tag poop
        takes_turns false
        health 1
        corpse_health 0
        can_be_backstabbed false
        kill_required false
        held_coins [0 2]
    }

    abilities {
        move None
        attack None
    }

    passives {
        CapReceivedDamage 1
        HPAltStates {
            clipname poopmain
            /*thresholds [
                [3 0] 
                [2 1] 
                [1 2] 
                [0 3] 
            ]*/
            thresholds [
                [1 0] 
                
                
                [0 3] 
            ]
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `FlamingPoop`
**Source:** `inanimate_objects.gon`  

```
FlamingPoop {
    variant_of Poop
    passives {
        Burn 3
    }
}
```

---

### `Hydrant`
**Name:** Fire Hydrant  
**Source:** `inanimate_objects.gon`  

```
Hydrant {
    graphics {
        movieclip Hydrant
        name "OBJECT_FIREHYDRANT_NAME"
    }

    properties {
        faction none
        type object
        takes_turns false
        health 1
        corpse_health 0
        can_be_backstabbed false
        knockback_immune true
        kill_required false
    }

    abilities {
        move None
        attack None
    }

    passives {
        TransformOnDeath HydrantFountain
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `HydrantFountain`
**Name:** Fountain  
**Source:** `inanimate_objects.gon`  

```
HydrantFountain {
    graphics {
        movieclip HydrantFountain
        name "OBJECT_FOUNTAIN_NAME"
        depth_offset .1
        dont_sink true
    }

    properties {
        faction none
        type object
        takes_turns false
        health 1
        inanimate true
        corpse_health 0
        can_be_backstabbed false
        knockback_immune true
        blocking false
        kill_required false
    }

    abilities {
        move None
        attack None
    }

    passives {
        SpreadWater 1
        FlingObjectsOnTop 8
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Dice`
**Name:** D6  
**Source:** `inanimate_objects.gon`  

```
Dice {
    graphics {
        movieclip GambitDice
        name "OBJECT_D6_NAME"
        shadow_size .50
		
		tooltip "OBJECT_D6_DESC"
    }

    properties {
        faction enemies
        type object
        takes_turns false
        inanimate true
        speculative_inanimate false
        can_be_backstabbed false
        kill_required false
        corpse_health 0
    }

    abilities {
        move None
        attack None
    }

    passives {
        DiceBehavior {
            dice_size 6
            knockback_damage 5
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Phylactery`
**Name:** Phylactery  
**Source:** `inanimate_objects.gon`  

```
Phylactery {
    graphics {
        movieclip Tumor
        name "OBJECT_PHYLACTERY_NAME"
        shadow None

        tooltip "OBJECT_PHYLACTERY_DESC"
    }

    properties {
        faction enemies
        type object
        takes_turns false
        health 75
        initial_health 15
        corpse_health 0
        can_be_backstabbed false
        kill_required false
    }

    abilities {
        move None
        attack None
    }

    passives {

    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `BloatyCorpse`
**Name:** Bloated Corpse  
**Source:** `inanimate_objects.gon`  

```
BloatyCorpse {
    graphics {
        movieclip BloatyCorpse
        name "OBJECT_BLOATEDCORPSE_NAME"
        water_mask medmed

        tooltip "OBJECT_BLOATEDCORPSE_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        health 1
        can_be_backstabbed false
        kill_required false
    }

    abilities {
        move None
        attack None

        spells [
            BloatyExplodey
        ]
    }

    passives {
        
        DeathRattle BloatyExplodey

        MultiSpawnOnDeath {
            obj Maggot
            count [0, 2]
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `TNTCrate`
**Name:** TNT  
**Source:** `inanimate_objects.gon`  

```
TNTCrate {
    graphics {
        movieclip TNTCrate
        name "OBJECT_TNT_NAME"
        no_splatter true
        water_mask square

        tooltip "OBJECT_TNT_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        health 1
        can_be_backstabbed false
        kill_required false
    }

    abilities {
        move None
        attack None

        spells [
            TNTExplodey
        ]
    }

    passives {
        DeathRattle TNTExplodey
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `HarpoonTrap`
**Name:** Harpoon Trap  
**Source:** `inanimate_objects.gon`  

```
HarpoonTrap {
    graphics {
        movieclip HarpoonTrap
        name "OBJECT_HARPOONTRAP_NAME"
        no_splatter true
        water_mask square

        tooltip "OBJECT_HARPOONTRAP_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        inanimate true
        can_be_backstabbed false
        kill_required false
        aoe_pierce_mode block
    }

    abilities {
        move None
        attack None

        spells [
            HarpoonTrapPull
        ]
    }

    passives {
        HarpoonTrapPassive HarpoonTrapPull
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `SpikyRock`
**Name:** Spiky Rock  
**Source:** `inanimate_objects.gon`  

```
SpikyRock {
    graphics {
        movieclip SpikyRock
        name "OBJECT_SPIKYROCK_NAME"
        no_splatter true
        water_mask medium

        tooltip "OBJECT_SPIKYROCK_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        inanimate true
        can_be_backstabbed false
        kill_required false
        knockback_immune true
        aoe_pierce_mode block
        visually_spiky true
        corpse_health 0
    }

    abilities {
        move None
        attack None
    }

    passives {
        Thorns 5
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `SpikyCactus`
**Name:** Spiky Cactus  
**Source:** `inanimate_objects.gon`  

```
SpikyCactus {
    variant_of SpikyRock

    graphics {
        movieclip SpikyCactus
        name "OBJECT_SPIKYCACTUS_NAME"
    }

    properties {
        visually_spiky true
    }

    passives {
        Thorns 5
        ChangeTileOnDeath WaterTile
        MeleeRevengeDamage {
            damage 0
            effects {
                Thorns 1
            }
        }
    }
}
```

---

### `SpikyCactus_Tall`
**Name:** Spiky Cactus  
**Source:** `inanimate_objects.gon`  

```
SpikyCactus_Tall {
    variant_of SpikyCactus

    graphics {
        movieclip SpikyCactusTall
        name "OBJECT_SPIKYCACTUS_NAME"
        dont_sink true
    }

    properties {
        tall true
    }

}
```

---

### `SpikyCactus_2x2`
**Name:** Spiky Cactus  
**Source:** `inanimate_objects.gon`  

```
SpikyCactus_2x2 {
    variant_of SpikyCactus

    graphics {
        movieclip SpikyCactus2x2
        name "OBJECT_SPIKYCACTUS_NAME"
        dont_sink true
    }

    properties {
        size 2x2
        tall true
    }
}
```

---

### `Decoy`
**Name:** Decoy  
**Source:** `inanimate_objects.gon`  

```
Decoy {
    graphics {
        movieclip Decoy2
        name "OBJECT_DECOY_NAME"
    }

    sound {
        alt_sounds [[HitGround SE_BuildBot_Land]]
    }

    properties {
        type object
        tag [robot decoy]
        takes_turns false
        health 5
        corpse_health 0
        can_be_backstabbed false
        kill_required false

        faction allies
        inherit_faction true
        ai_scale 1
    }

    abilities {
        move None
        attack None
    }

    passives {
        Robot 1
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `ExplodingDecoy`
**Description:** Explodes when it dies.  
**Source:** `inanimate_objects.gon`  

```
ExplodingDecoy {
    variant_of Decoy

    graphics {
        desc "OBJECT_DECOY_DESC"
    }

    abilities {
        spells [
            DecoyExplode
        ]
    }

    passives {
        DeathRattle DecoyExplode
    }
}
```

---

### `ElectricNail`
**Name:** Electric Nail  
**Source:** `inanimate_objects.gon`  

```
ElectricNail {
    graphics {
        movieclip ElectricNail
        name "OBJECT_ELECTRICNAIL_NAME"
        shadow_size .25

        tooltip "OBJECT_ELECTRICNAIL_DESC"
    }

    properties {
        type object
        tag robot
        takes_turns false
        health 5
        corpse_health 0
        can_be_backstabbed false
        kill_required false

        faction none
        
    }

    abilities {
        move None
        attack None
    }

    passives {
        ElectricArcs 1
        Robot 1
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `RubberFistBot`
**Name:** Rubber Fist Bot  
**Source:** `inanimate_objects.gon`  

```
RubberFistBot {
    graphics {
        movieclip Punchbot
        name "OBJECT_RUBBERFISTBOT_NAME"
        tooltip "OBJECT_RUBBERFISTBOT_DESC"
    }

    sound {
        alt_sounds [[HitGround SE_BuildBot_Land]]
    }

    properties {
        type object
        tag robot
        takes_turns false
        health 3
        corpse_health 0
        can_be_backstabbed false
        kill_required false

        faction none
        inherit_faction true
    }

    abilities {
        move None
        attack RubberFistBotPunch
    }

    passives {
        Robot 1
        /*Trapper {
            ability RubberFistBotPunch
            enemies_only false
            on_self_move true
        }*/
        MovementReaction {
            ability RubberFistBotPunch
            enemies_only false
            on_self_move_too true
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Tombstone_Ghost`
**Name:** Tombstone  
**Source:** `inanimate_objects.gon`  

```
Tombstone_Ghost {
    graphics {
        movieclip Tombstone
        name "OBJECT_TOMBSTONE_NAME"

        tooltip "OBJECT_GHOSTTOMBSTONE_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        health 3
        can_be_backstabbed false
        kill_required false
        corpse_health 0
    }

    abilities {
        move None
        attack None
    }

    passives {
        SpawnOnDeath {
            obj [Spookie Spookie Scary Coin2 Coin3 Coin4]
            faction enemies
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Tombstone_Zombie`
**Name:** Tombstone  
**Source:** `inanimate_objects.gon`  

```
Tombstone_Zombie {
    graphics {
        movieclip Tombstone
        name "OBJECT_TOMBSTONE_NAME"
        piece_alt_frame 3
        tooltip "OBJECT_TOMBSTONE_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        health 3
        can_be_backstabbed false
        kill_required false
        corpse_health 0
    }

    abilities {
        move None
        attack None
    }

    passives {
        AutocastEachRound {
            ability ZombieTombstone
            even_if_stunned true
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Tombstone_ManaIdol`
**Name:** Tombstone  
**Source:** `inanimate_objects.gon`  

```
Tombstone_ManaIdol {
    graphics {
        movieclip Tombstone
        name "OBJECT_TOMBSTONE_NAME"
        piece_alt_frame 5

        tooltip "OBJECT_DRAINTOMBSTONE_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        health 3
        can_be_backstabbed false
        kill_required false
        corpse_health 0
    }

    abilities {
        move None
        attack None
    }

    passives {
        GlobalManaDrainAura -1

        CharacterLightSource {
            color [.3, .7, 1]
            size 3
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Cactus`
**Name:** Cactus  
**Source:** `inanimate_objects.gon`  

```
Cactus {
    graphics {
        movieclip Cactus
        name "OBJECT_CACTUS_NAME"

        tooltip "OBJECT_CACTUS_DESC"
    }

    properties {
        faction none
        type object
		
        takes_turns false
        health 10
        can_be_backstabbed false
        kill_required false
        visually_spiky true
    }

    abilities {
        move None
        attack None
    }

    passives {
        Thorns 5
        ChangeTileOnDeath WaterTile
        MeleeRevengeDamage {
            damage 0
            effects {
                Thorns 1
            }
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Twister`
**Name:** Twister  
**Source:** `inanimate_objects.gon`  

```
Twister {
    graphics {
        movieclip Twister
        name "OBJECT_TWISTER_NAME"
        no_splatter true
		
		tooltip "OBJECT_TWISTER_DESC"
    }

    properties {
        faction enemies
        inherit_faction true
        type object
        takes_turns true
        initiative 10000
        movement 2
        health 1
        inanimate true
        corpse_health 0
        can_be_backstabbed false
        blocking false
        kill_required false
        flying true
        tile_desire_cost 200
    }

    abilities {
        move TwisterMove
        attack None
    }

    passives {
        Phasing 1
        LoopingSoundWhileAlive Twister_loop
        TwisterFling {
            min_dist 3
            max_dist 5

            damage 5
        }
        ReflectProjectiles 100%
        DiesToElement Wind
        HiddenDoomed 2
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_always_move
        animate_choice false
    }
}
```

---

### `NeutralTwister`
**Source:** `inanimate_objects.gon`  

```
NeutralTwister {
    variant_of Twister

    graphics {
		tooltip "OBJECT_NTWISTER_DESC"
    }

    properties {
        faction third_party
        initiative 10
    }
}
```

---

### `MiniNuke`
**Name:** Mini Nuke  
**Source:** `inanimate_objects.gon`  

```
MiniNuke {
    graphics {
        movieclip TNTCrate
        name "OBJECT_MININUKE_NAME"
        no_splatter true
        water_mask square

        tooltip "OBJECT_MININUKE_DESC"
    }

    properties {
        faction none
        tag bomb
        type object
        takes_turns false
        health 1
        can_be_backstabbed false
        kill_required false
    }

    abilities {
        move None
        attack None

        spells [
            MiniNukeExplodey
        ]
    }

    passives {
        DeathRattle MiniNukeExplodey
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `NeutronStar`
**Name:** Neutron Star  
**Source:** `inanimate_objects.gon`  

```
NeutronStar {
    graphics {
        movieclip NeutronStar
        name "OBJECT_NEUTRONSTAR_NAME"
        dont_sink true
		
		tooltip "OBJECT_NEUTRONSTAR_DESC"
    }

    properties {
        tag cosmic
        faction none
        type object
        takes_turns true
        size 2x2
        tall true
        inanimate true
        knockback_immune true
        takes_main_turn false
        round_end_bonus_turns 1
    }

    abilities {
        move None
        attack None

        spells [
            BHoleSuck
            NeutronRumble
            NeutronExplode
        ]
    }

    passives {
        FormChanger {
            NeutronStar {
                ai {
                    brain PatternBrain

                    pattern {
                        do_random [NeutronRumble NeutronExplode]
                    }

                    decision_weights always_cast
                    animate_choice false
                }

                passives {
                    MeleeRevengeDamage {
                        damage 5
                        knockback 3

                        effects {
                            Burn 5
                        }

                        elements [
                            Fire
                        ]
                    }
                }
            }
            BlackHole {
                animation_suffix "BlackHole"
                name "OBJECT_BLACKHOLE_NAME"
				
				tooltip "OBJECT_BLACKHOLE_DESC"

                ai {
                    brain PatternBrain

                    pattern {
                        do BHoleSuck
                    }

                    decision_weights always_cast
                    animate_choice false
                }

                passives {
                    MeleeRevengeDamage {
                        damage 0
                        type none
                        cant_miss true

                        effects {
                            BlackHoleSuck 1
                        }
                    }
                    BlackHolePassive 1
                }
            }
        }

        
    }

    ai {
        brain NoBrain
    }
}
```

---

### `BlackHole`
**Source:** `inanimate_objects.gon`  

```
BlackHole {
    variant_of NeutronStar
    passives {
       FormChanger {
           initial_form BlackHole
       }
    }
}
```

---

### `HellHand`
**Name:** Hell Hand  
**Source:** `inanimate_objects.gon`  

```
HellHand {
    graphics {
        movieclip CoreArm
        name "OBJECT_HELLHAND_NAME"
        shadow none
		no_splatter true
		tooltip "OBJECT_HELLHAND_DESC"
    }

    stats {
        strength 4
        dexterity 2
        constitution 2
        intelligence 2
        speed 5
        charisma 2
    }
    
    properties {
        tag demon
        faction enemies
        kill_required false
        movement 0
        health 13
        weak_threshold 0
        corpse_health 0

        takes_turns false
    }

    abilities {
        move None
        attack HellHandGrab

        spells [
            
        ]
    }

    passives {
        FormChanger {
            Default {
                passives {
                    Trapper {
                        ability HellHandGrab
                        pathfinding_avoidance 250
                    }
                }
            }
            Grappling {
                partial_animation_suffix Grapple
                exit_animations {
                    Default release
                }
            }
        }
        FormChangeWhileHasStatus {
            status Grappling
            form_has Grappling
            form_hasnot Default
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `CloningVat`
**Name:** Cloning Vat  
**Source:** `inanimate_objects.gon`  

```
CloningVat {
    graphics {
        movieclip CloningVat
        name "OBJECT_CLONINGVAT_NAME"
		scale .8
		
		tooltip "OBJECT_CLONINGVAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        faction none
        type object
        kill_required false
        movement 0
        corpse_health 0
        health 3
        takes_turns false
    }

    abilities {
        move None
        attack None

        spells [
            
        ]
    }

    passives {
        SpawnOnDeath {
            obj [Kitten Kitten TomTom TomTom Mangy Mangy CatCaller CatCaller GlassSpitter SpiderCat SharkyCat WolfCat]
            faction enemies
            additional_statuses {
                PermanentMadness 1
            }
        }
    }
    
    ai {
        brain NoBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `GroundedSpear`
**Name:** Spear  
**Source:** `inanimate_objects.gon`  

```
GroundedSpear {
    graphics {
        movieclip GroundedSpear
        name "OBJECT_GROUNDEDSPEAR_NAME"
		
		tooltip "OBJECT_GROUNDEDSPEAR_DESC"
    }

    properties {
        tag spear
        faction none
        type object
        takes_turns false
        health 12
        can_be_backstabbed false
        kill_required false
        
        corpse_health 0
    }

    abilities {
        move None
        attack None
    }

    passives {
        StripStatuses 1
        AddStatusToReceivedDamage {
            Conditional_IsPhysicalAttack {
                RemoveKnockback 1
                KnockUpAndAway {
                    stacks 5
                    distance 3
                    displace true
                    self_damage false
                }
                TempPassiveUntilSettled {
                    MeleeRevengeDamage {
                        effects {
                            Stun 1
                        }
                    }
                }
            } Else {
                Conditional_HasKnockback {
                    RemoveKnockback 1
                    KnockUpAndAway {
                        stacks 5
                        distance 3
                        displace true
                        self_damage false
                    }
                    TempPassiveUntilSettled {
                        MeleeRevengeDamage {
                            effects {
                                Stun 1
                            }
                        }
                    }
                }
            }
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `LabSupportPillar`
**Name:** Support Pillar  
**Source:** `inanimate_objects.gon`  

```
LabSupportPillar {
    graphics {
        movieclip LabSupportPillar
        name "OBJECT_SUPPORTPILLAR_NAME"
        water_mask square
		
		tooltip "OBJECT_SUPPORTPILLAR_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        health 1
        can_be_backstabbed false
        kill_required false
        knockback_immune true
    }

    abilities {
        move None
        attack None

        spells [
            LabPillarDrop
        ]
    }

    passives {
        DeathRattle {
            ability LabPillarDrop
            pop_corpse false
            is_dying_animation true
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `SpewerPill_Normal`
**Name:** Creep Pill  
**Source:** `inanimate_objects.gon`  

```
SpewerPill_Normal {
    graphics {
        movieclip SpewerPill
        name "OBJECT_SPEWERPILL_CREEP_NAME"
        piece_alt_frame 1
		
		tooltip "OBJECT_SPEWERPILL_DESC"
    }

    properties {
        faction none
        type object
        tag pill
        hidden_tag sp_pill_normal
        takes_turns false
        health 6
        corpse_health 0
        can_be_backstabbed false
        kill_required false
        flying true
    }

    abilities {
        move None
        attack None
    }

    passives {
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `SpewerPill_Fire`
**Name:** Lava Pill  
**Source:** `inanimate_objects.gon`  

```
SpewerPill_Fire {
    variant_of SpewerPill_Normal

    graphics {
        name "OBJECT_SPEWERPILL_LAVA_NAME"
        piece_alt_frame 3
    }

    properties {
        hidden_tag sp_pill_fire
    }
}
```

---

### `SpewerPill_Tar`
**Name:** Tar Pill  
**Source:** `inanimate_objects.gon`  

```
SpewerPill_Tar {
    variant_of SpewerPill_Normal

    graphics {
        name "OBJECT_SPEWERPILL_TAR_NAME"
        piece_alt_frame 5
    }

    properties {
        hidden_tag sp_pill_tar
    }
}
```

---

### `SpewerPillTubeL`
**Name:** Pill Tube  
**Source:** `inanimate_objects.gon`  

```
SpewerPillTubeL {
    graphics {
        movieclip SpewerTube
        name "OBJECT_SPEWERTUBE_NAME"
		
		tooltip "OBJECT_SPEWERTUBE_DESC"
    }

    properties {
        faction none
        type object
        takes_turns true
        inanimate true
        can_be_backstabbed false
        kill_required false
        knockback_immune true
        initiative -999999

        lock_orientation [-1 0]
    }

    abilities {
        move None
        attack SpawnSpewerPill

        spells [
            LabPillarDrop
        ]
    }
    
    ai {
        brain GenericBrain
        animate_choice false
    }
}
```

---

### `SpewerPillTubeR`
**Source:** `inanimate_objects.gon`  

```
SpewerPillTubeR {
    variant_of SpewerPillTubeL

    properties {
        lock_orientation [0 -1]
    }
}
```

---

### `MiniVolcano`
**Name:** Mini Volcano  
**Source:** `inanimate_objects.gon`  

```
MiniVolcano {
    graphics {
        movieclip MiniVolcano
        name "OBJECT_MINIVOLCANO_NAME"
		
		tooltip "OBJECT_MINIVOLCANO_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        inanimate true
        can_be_backstabbed false
        kill_required false
        knockback_immune true
        lock_orientation [1 0]
    }

    abilities {
        move None
        attack None

        spells [
            MiniVolcano_Spurt
        ]
    }

    passives {
        MiniVolcanoReaction MiniVolcano_Spurt
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `PunchingBag`
**Name:** Punching Bag  
**Source:** `inanimate_objects.gon`  

```
PunchingBag {
    graphics {
        movieclip Decoy
        name "OBJECT_PUNCHINGBAG_NAME"
        uifloaters_offset 1.5
    }

    properties {
        type object
        takes_turns false
        health 999
        corpse_health 0
        can_be_backstabbed false
        kill_required false

        faction third_party
    }

    abilities {
        move None
        attack None
    }

    passives {
        KineticSpikes 5
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `GasCloud`
**Name:** Gas Cloud  
**Source:** `inanimate_objects.gon`  

```
GasCloud {
    graphics {
        movieclip GasCloud
        name "OBJECT_GASCLOUD_NAME"
        depth_offset -.1
        no_splatter true
		
		tooltip "OBJECT_GASCLOUD_DESC"
    }

    properties {
        faction none
        type object
        takes_turns false
        inanimate true
        layer gas
        flying true
        corpse_health 0
        can_be_backstabbed false
        kill_required false
        tile_desire_cost 100
        
        elements [
            Poison
        ]
    }

    abilities {
        move None
        attack None
    }

    passives {
        
        

        GasCloudBehavior2 2
        StatusOverlappingCharactersAndDie {
            Poison 1
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Grenade`
**Name:** Grenade  
**Source:** `inanimate_objects.gon`  

```
Grenade {
    graphics {
        movieclip Grenade
        name "OBJECT_GRENADE_NAME"
        no_splatter true
        scale .8

        tooltip "OBJECT_GRENADE_DESC"
    }

    sound {
        alt_sounds [[HitGround SE_Obj_GrenadeLand]]
    }

    properties {
        faction none
        tag bomb
        initiative -99
        type object
        health 35
        can_be_backstabbed false
        kill_required false
        corpse_health 0
    }

    abilities {
        move None
        attack None

        spells [
            GrenadeExplode
        ]
    }

    passives {
        DeathRattle GrenadeExplode
        DisplayDangerAOE GrenadeExplode
        MinimumKnockbackFromPhysicalAttacks 1
        BasicAIDangerZone 2
    }
    
    ai {
        brain PatternBrain
        decision_weights always_cast
        pattern {
            do GrenadeExplode
        }
    }
}
```

---

### `SlotMachine`
**Name:** Slot Machine  
**Source:** `inanimate_objects.gon`  

```
SlotMachine {
    graphics {
        movieclip SlotMachine
        name "OBJECT_SLOTMACHINE_NAME"
        no_splatter true
        uifloaters_offset 1.5
		
		tooltip "OBJECT_SLOTMACHINE_DESC"
    }

    properties {
        faction none
        tag [robot container]
        initiative -99
        type object
        health 21
        always_face_forward true
        kill_required false
        corpse_health 0
        takes_turns false
        flying true
    }

    abilities {
        move None
        attack None

        spells [
            SlotMachine_DeathExplode

            SlotResult_Explode
            SlotResult_Nothing
            SlotResult_RandomPickup
            SlotResult_Jackpot_Coins
        ]
    }

    passives {
       Robot {
           alternate_energized_effect {
               FormChange GuaranteedJackpot
           }
       }

       FormChanger {
           Default {
               passives {
                   SlotMachineRollPool {
                       SlotResult_Explode 1
                       SlotResult_Nothing 7
                       SlotResult_RandomPickup 11
                       SlotResult_Jackpot_Coins 1
                   }
               }
           }
           GuaranteedJackpot {
               passives {
                   SlotMachineRollPool {
                       SlotResult_Jackpot_Coins 1
                   }
               }
           }
       }

       DeathRattle SlotMachine_DeathExplode
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `CovenCandle`
**Name:** Candle  
**Source:** `inanimate_objects.gon`  

```
CovenCandle {
    graphics {
        movieclip CovenCandle
        name "OBJECT_CANDLE_NAME"
        uifloaters_offset 1.5
		scale .8
		no_splatter true
    }

    properties {
        faction none
        tag candle
        type object
        takes_turns false
        health 50
        corpse_health 0
        can_be_backstabbed false
        kill_required false
        weak_threshold 0
        knockback_immune true
        can_be_overkilled false
    }

    abilities {
        move None
        attack None
    }

    passives {
        BattlefieldUniqueRandomPassive {
            DemonicGlyph_Bite 1
            DemonicGlyph_Fire 1
            DemonicGlyph_Summon 1
            DemonicGlyph_Movement 1
            DemonicGlyph_Bounce 1
        }
        StripStatuses 1

        FormChanger {
            Lit {
                partial_animation_suffix Lit

                passives {
                    FormChangeOnElementInfluence {
                        element wind
                        exclude fire
                        form Unlit
                        particle FireExtinguish
                        sfx FireExtinguish
                    }
                    FormChangeOnElementInfluence {
                        element water
                        form Unlit
                        particle FireExtinguish
                        sfx FireExtinguish
                    }
                }
            }
            Unlit {
                partial_animation_suffix Unlit

                passives {
                    MuteDemonicGlyphDisplay 1

                    FormChangeOnElementInfluence {
                        element [fire]
                        exclude water
                        form Lit
                    }
                    AddHiddenTag unlit_candle
                }
            }
        }
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `BloatEye`
**Name:** Peeper  
**Source:** `inanimate_objects.gon`  

```
BloatEye {
    graphics {
        movieclip BloatEye
        name "OBJECT_BLOATEYE_NAME"
		
		tooltip "OBJECT_BLOATEYE_DESC"
    }

    properties {
        faction enemies
        hidden_tag bloateye
        type object
        inanimate true
        takes_turns false
        flying true
    }

    abilities {
        move None
        attack None

        spells [
            BloatEyeMovement2
        ]
    }

    passives {
        Trample 3
        BloatEyePassive2 BloatEyeMovement2
        MinimumKnockbackFromPhysicalAttacks 1

    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Pyrophina`
**Name:** Pyrophina  
**Source:** `kaijus.gon`  

```
Pyrophina {
    graphics {
        movieclip Pyrophina
        name "ENEMY_PYROPHINA_NAME"
        shadow_size 2.5
        uifloaters_offset 3.5
        move_speed_sync_frames 50
        water_mask big
		tooltip "ENEMY_PYROPHINASOLO_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag kaiju
        faction enemies
        type boss
        movement 3
        corpse_health indestructible

        size 2x2
        move_block everything_even_when_dead

        evenly_dispersed_bonus_turns 2
        dispersed_bonus_turns_before_cats false
        initiative -100
        
        mana_regen 999
        mana 100
        
        health 600
        weak_threshold 150
    }

    abilities {
        move DefaultMove
        attack PyrophinaSoloAttack
        
        spells [
            
            PyrophinaVSWeatherRoar
            PyrophinaSoloCatThrow
            PyrophinaSoloFlamethrower
            PyrophinaSoloEarthquakeStomp
            PyrophinaSoloRoar

            PyrophinaVSRun
        ]
    }

    passives {
        Trample 3
        KaijuKnockbackImmune 1
        ElementImmune Fire
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveForThrow {
                ability move
                move_for_ability PyrophinaSoloCatThrow
                move_weights util_minmove
            }
            RunFar {
                ability PyrophinaVSRun
                move_weights run_far
            }
        }

        bonusturn_pattern {
            do_priority [*PyrophinaVSWeatherRoar *PyrophinaSoloFlamethrower move]
            do_priority [*PyrophinaVSWeatherRoar *attack *PyrophinaSoloEarthquakeStomp move]
            do_priority [*PyrophinaVSWeatherRoar MoveForThrow *PyrophinaSoloCatThrow]
        }

        pattern {
            do_all [*PyrophinaVSWeatherRoar *PyrophinaSoloRoar RunFar]
        }

        fallback {
            do_priority [*attack RunFar]
        }

        fallback_advances_pattern true
        stun_advances_pattern true

        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `Zaratana`
**Name:** Zaratana  
**Source:** `kaijus.gon`  

```
Zaratana {
    graphics {
        movieclip Zaratana
        name "ENEMY_ZARATANA_NAME"
        shadow_size 2.5
        uifloaters_offset 2
        move_speed_sync_frames 52
        water_mask big
		tooltip "ENEMY_ZARATANASOLO_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [kaiju rock]
        hidden_tag zaratana
        faction enemies
        type boss
        movement 3
        corpse_health indestructible

        size 2x2
        move_block everything_even_when_dead

        evenly_dispersed_bonus_turns 2
        dispersed_bonus_turns_before_cats false
        initiative -100
        
        mana_regen 999
        mana 100
        
        health 600
        weak_threshold 150
    }

    abilities {
        move DefaultMove
        attack ZaratanaSoloBasic
        
        spells [
            ZaratanaSoloMagnet
            ZaratanaSoloBombardment
            ZaratanaSoloTurtle
            ZaratanaSoloRoar
            ZaratanaSoloSpinDash

            ZaratanaVSRevenge
            ZaratanaSoloWeatherRoar
            ZaratanaVSExitTurtle
        ]
    }

    passives {
        Trample 3
        KaijuKnockbackImmune 1

        FormChanger {
            Default {
                passives {
                    ImmediateAbilityReaction {
                        ability ZaratanaVSRevenge
                        ability_damage_only true
                        damage_threshold 10
                    }
                }
            }
            Turtled {
                attack None
                move None
                animation_suffix Turtle

                passives {
                    Brace 10
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do **ZaratanaSoloSpinDash
                        do *ZaratanaVSExitTurtle
                    }
                    reset_pattern_on_formswitch true
                    stun_advances_pattern false
                }
            }
        }
    }
    
    ai {
        
        brain PatternBrain

        bonusturn_pattern {
            do_priority [*ZaratanaSoloWeatherRoar ZaratanaSoloBombardment]
            do_priority [*ZaratanaSoloWeatherRoar attack]
            do_priority [*ZaratanaSoloWeatherRoar ZaratanaSoloMagnet ZaratanaSoloBombardment] 
            do_priority [*ZaratanaSoloWeatherRoar *ZaratanaSoloTurtle]
            do_priority [*ZaratanaSoloWeatherRoar attack]
        }

        fallback {
            do_priority [attack move]
        }

        pattern {
            do_all [*ZaratanaSoloWeatherRoar *ZaratanaSoloRoar]
        }

        decision_weights default
        move_weights stay_close

        fallback_advances_pattern true
        stun_advances_pattern true
    }
}
```

---

### `PyrophinaVS`
**Name:** Pyrophina  
**Source:** `kaijus.gon`  

```
PyrophinaVS {
    graphics {
        movieclip Pyrophina
        name "ENEMY_PYROPHINA_NAME"
        shadow_size 2.5
        uifloaters_offset 3.5
        move_speed_sync_frames 50
        water_mask big
		tooltip "ENEMY_PYROPHINAVS_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag kaiju
        faction kaiju1
        type boss
        movement 3
        corpse_health indestructible

        size 2x2
        move_block everything_even_when_dead

        disperse_main_turns true
        dispersed_bonus_turns_before_cats true
        
        mana_regen 999
        mana 100
        
        health 1000
        weak_threshold 150

        must_start_facing_camera false
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            PyrophinaVSSpinThrow
            PyrophinaVSWeatherRoar
            PyrophinaVSCatThrow
            PyrophinaVSFlamethrower
            PyrophinaVSEarthquakeStomp
            PyrophinaVSRoar

            PyrophinaVSRun
        ]
    }

    passives {
        Trample 3
        Buddy {
            obj ZaratanaVS
            allies_only false
        }
        KaijuKnockbackImmune 1
        KaijuWinCon pyrophina
        ElementImmune Fire

        BonusTurnPattern [ 
            {
                evenly_dispersed_bonus_turns 1
                round_end_bonus_turns 1
                initiative_adjustment 50
            }

            {
                evenly_dispersed_bonus_turns 0
                round_end_bonus_turns 1
                initiative_adjustment -50
            }
        ]
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveForSpin {
                ability PyrophinaVSRun
                move_for_ability PyrophinaVSSpinThrow
                move_weights stay_close
            }

            MoveForThrow {
                ability move
                move_for_ability PyrophinaVSCatThrow
                move_weights util_minmove
            }
        }

        pattern {
            do_all [*PyrophinaVSWeatherRoar PyrophinaVSFlamethrower]
            do_all [*PyrophinaVSWeatherRoar MoveForThrow *PyrophinaVSCatThrow]
            do_all [*PyrophinaVSWeatherRoar PyrophinaVSEarthquakeStomp]
        }
        round_end_bonusturn_pattern {
            do_one [**PyrophinaVSWeatherRoar **PyrophinaVSRoar]
            do_all [*PyrophinaVSWeatherRoar MoveForSpin PyrophinaVSSpinThrow]
        }
        fallback {
            do attack
        }

        fallback_advances_pattern true
        stun_advances_pattern true

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `ZaratanaVS`
**Name:** Zaratana  
**Source:** `kaijus.gon`  

```
ZaratanaVS {
    graphics {
        movieclip Zaratana
        name "ENEMY_ZARATANA_NAME"
        shadow_size 2.5
        uifloaters_offset 2
        move_speed_sync_frames 52
        water_mask big
		tooltip "ENEMY_ZARATANAVS_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [kaiju rock]
        hidden_tag zaratana
        faction kaiju2
        type boss
        movement 3
        corpse_health indestructible

        size 2x2
        move_block everything_even_when_dead

        disperse_main_turns true
        dispersed_bonus_turns_before_cats true
        
        mana_regen 999
        mana 100
        
        health 1000
        weak_threshold 150

        must_start_facing_camera false
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack ZaratanaBasic
        
        spells [
            ZaratanaVSSpinDash
            ZaratanaVSWeatherRoar
            ZaratanaVSMagnet
            ZaratanaVSBombardment
            ZaratanaVSTurtle
            ZaratanaVSExitTurtle
            ZaratanaVSRoar
            ZaratanaVSRevenge

            ZaratanaVSTurtleGuaranteed
        ]
    }

    passives {
        Trample 3
        Buddy {
            obj PyrophinaVS
            allies_only false
        }
        KaijuKnockbackImmune 1
        KaijuWinCon zaratana

        FormChanger {
            Default {
                passives {
                    ImmediateAbilityReaction {
                        ability ZaratanaVSRevenge
                        buddy_damage_only true
                        ability_damage_only true
                    }
                }
            }
            Turtled {
                attack None
                move None
                animation_suffix Turtle

                passives {
                    Brace 10
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do *ZaratanaVSExitTurtle
                    }
                    end_turn_on_formswitch true
                }
            }
        }

        BonusTurnPattern [ 
            {
                evenly_dispersed_bonus_turns 0
                round_end_bonus_turns 1
                initiative_adjustment -50
            }

            {
                evenly_dispersed_bonus_turns 1
                round_end_bonus_turns 1
                initiative_adjustment 50
            }
        ]
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveForBarrage {
                ability move
                move_for_ability ZaratanaVSBombardment
                move_weights stay_far
            }
        }

        pattern {
            do_all [*ZaratanaVSWeatherRoar MoveForBarrage *ZaratanaVSBombardment ZaratanaVSTurtle]
            do_all [*ZaratanaVSWeatherRoar ZaratanaVSMagnet ZaratanaVSTurtle]
            do_all [*ZaratanaVSWeatherRoar attack ZaratanaVSTurtle]
        }
        round_end_bonusturn_pattern {
            do_all [*ZaratanaVSWeatherRoar ZaratanaVSSpinDash ZaratanaVSTurtle]
            do_one [**ZaratanaVSWeatherRoar **ZaratanaVSRoar]
        }
        fallback {
            do_priority [attack ZaratanaVSTurtleGuaranteed]
        }

        decision_weights default
        move_weights keep_distance

        fallback_advances_pattern true
        stun_advances_pattern true
    }
}
```

---

### `PyrophinaFamiliar`
**Name:** Pyrophina (Friendly)  
**Source:** `kaijus.gon`  

```
PyrophinaFamiliar {
    graphics {
        movieclip Pyrophina
        name "ENEMY_PYROPHINAFRIENDLY_NAME"
        shadow_size 2.5
        uifloaters_offset 3.5
        move_speed_sync_frames 50
        water_mask big

        tooltip "ENEMY_KAIJUFRIENDLY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag kaiju
        faction allies
        inherit_faction true
        type boss
        movement 3
        corpse_health indestructible

        size 2x2
        move_block everything_even_when_dead
        initiative -5
        
        mana_regen 999
        mana 100
        
        health 600
        weak_threshold 150
        ai_scale .25
    }

    abilities {
        move DefaultMove
        attack PyrophinaSoloAttack
        
        spells [
            PyrophinaSoloFlamethrower
        ]
    }

    passives {
        Trample 3
        KaijuKnockbackImmune 1
        DissuadeInstakills 1
        ElementImmune Fire

        ChanceToDisableActionsIfNotCharmed 75% 
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_random [attack PyrophinaSoloFlamethrower]
        }

        decision_weights careless
        move_weights chaotic
    }
}
```

---

### `ZaratanaFamiliar`
**Name:** Zaratana (Friendly)  
**Source:** `kaijus.gon`  

```
ZaratanaFamiliar {
    graphics {
        movieclip Zaratana
        name "ENEMY_ZARATANAFRIENDLY_NAME"
        shadow_size 2.5
        uifloaters_offset 2
        move_speed_sync_frames 52
        water_mask big

        tooltip "ENEMY_KAIJUFRIENDLY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [kaiju rock]
        hidden_tag zaratana
        faction allies
        inherit_faction true
        type boss
        movement 3
        corpse_health indestructible

        size 2x2
        move_block everything_even_when_dead
        initiative -5
        
        mana_regen 999
        mana 100
        
        health 600
        weak_threshold 150
        ai_scale .25
    }

    abilities {
        move DefaultMove
        attack ZaratanaSoloBasic
        
        spells [
            ZaratanaSoloBombardment
            ZaratanaVSRevenge
        ]
    }

    passives {
        Trample 3
        KaijuKnockbackImmune 1
        DissuadeInstakills 1

        ChanceToDisableActionsIfNotCharmed 75% 

        ImmediateAbilityReaction {
            ability ZaratanaVSRevenge
            ability_damage_only true
            damage_threshold 10
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_random [attack ZaratanaSoloBombardment]
        }

        decision_weights careless
        move_weights chaotic
    }
}
```

---

### `CanCreeper`
**Name:** Can Creeper  
**Source:** `minibosses.gon`  

```
CanCreeper {
    graphics {
        movieclip CanCreeper
        name "ENEMY_CANCREEPER_NAME"
        water_mask medmed

        tooltip "ENEMY_CANCREEPER_DESC"
    }

    sound {
        alt_sounds [[DamageBlocked DamageBlocked_CanCreeper]]
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        dispersed_bonus_turns 1
        movement 3
        corpse_health 0

        
        mana_regen 999
        mana 100
        
        health 40
        always_triggers_traps true
    }

    abilities {
        move DefaultMove
        attack DoubleDiagonalCreepshot
        
        spells [
            CanCreeperSlide
        ]
    }

    passives {
        TileTrail CreepTile
        CanShield 1
        IgnoreTiles 1
        ChangeTileOnPop CreepTile
        TransformOnDeath CanCreeperOut
        ElementImmune Creep
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveCenter {
                ability move
                move_weights stay_near_map_center
            }
        }

        mainturn_pattern {
            do attack
        }


        bonusturn_pattern {
            do_strict [*CanCreeperSlide, MoveCenter]
        }

        decision_weights default
        move_weights stay_close_always_move
        auto_orient false
    }
}
```

---

### `CanCreeperOut`
**Name:** Can Creeper  
**Source:** `minibosses.gon`  

```
CanCreeperOut {
    graphics {
        movieclip CanCreeperOut
        name "ENEMY_CANCREEPER_NAME"
        projectile_spawn_offset [0 1]

        tooltip "ENEMY_CANCREEPEROUT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 8
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        dispersed_bonus_turns 1
        corpse_health 1

        
        mana_regen 999
        mana 100
        
        health 20
    }

    abilities {
        move Swim
        attack ShortCreepshot
        
        spells [
            MoveOne
        ]
    }

    passives {
        GroundFlopper MoveOne
        WaterWalk 1
        ElementImmune Creep
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `BigSlime`
**Name:** Big Slime  
**Source:** `minibosses.gon`  

```
BigSlime {
    graphics {
        movieclip BigSlime
        name "ENEMY_BIGSLIME_NAME"
        shadow BigSlimeShadow

        tooltip "ENEMY_BIGSLIME_DESC"

        water_mask medium
    }

    stats {
        strength 10
        dexterity 6
        constitution 6
        intelligence 6
        speed 6
        charisma 6
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        movement 4
        dispersed_bonus_turns 1
        corpse_health 0
        
        health 64

        size 2x2
        move_block everything_even_when_dead

        banned_elite_buffs [Shielded1 Shielded2 Shielded3 Shielded4]
    }

    abilities {
        move DefaultMove
        attack BasicBigMelee
        
        spells [
        ]
    }

    passives {
        Trample 3
        Divide4OnDeath MedSlime
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `MedSlime`
**Name:** Medium Slime  
**Source:** `minibosses.gon`  

```
MedSlime {
    graphics {
        movieclip MedSlime
        name "ENEMY_MEDIUMSLIME_NAME"
        shadow MedSlimeShadow

        tooltip "ENEMY_MEDIUMSLIME_DESC"

        water_mask medium
    }

    stats {
        strength 5
        dexterity 3
        constitution 3
        intelligence 3
        speed 3
        charisma 3
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        movement 3
        corpse_health 0
        
        health 16

        banned_elite_buffs [Shielded1 Shielded2 Shielded3 Shielded4]
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
        ]
    }

    passives {
        Divide4OnDeath SmallSlime
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `SmallSlime`
**Name:** Small Slime  
**Source:** `minibosses.gon`  

```
SmallSlime {
    graphics {
        movieclip SmallSlime
        name "ENEMY_SMALLSLIME_NAME"
        shadow SmallSlimeShadow
		tooltip "ENEMY_SMALLSLIME_DESC"
    }

    stats {
        strength 2
        dexterity 1
        constitution 1
        intelligence 1
        speed 1
        charisma 1
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        movement 2
        corpse_health 0
        
        health 4
        held_coins [0 1]

        banned_elite_buffs [Shielded1 Shielded2 Shielded3 Shielded4]
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Gambit`
**Name:** Gambit  
**Source:** `minibosses.gon`  

```
Gambit {
    graphics {
        movieclip Gambit
        name "ENEMY_GAMBIT_NAME"
        uifloaters_offset 1.5
		tooltip "ENEMY_GAMBIT_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 10
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        round_start_bonus_turns 1
        round_end_bonus_turns 1
        
        mana_regen 999
        mana 100
        
        health 110
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            DiceLeap
            RollDice
            D6Fizzle 
            D6Confused 
            D6Poop 
            D6Laser 
            D6Quake 
            D6Storm 
            D6Wrath 
        ]
    }

    passives {
	
		BossRewards {
			common SnakeEyes
			rare GambitsDice
		}
        Buddy {
            obj Dice
            reclaim_if_lost true
            allies_only false
        }
        DicerArt [59 52 65 50 54 63 64]

        
        
    }
    
    ai { 
        brain DicerBrain
        roll_ability RollDice
        dice_abilities [D6Fizzle D6Confused D6Poop D6Laser D6Quake D6Storm D6Wrath]

        decision_weights always_cast
        move_weights keep_distance_always_move

        post_absorb_move_weights minimum_move
    }
}
```

---

### `Flushmaster`
**Name:** Flushmaster  
**Source:** `minibosses.gon`  

```
Flushmaster {
    graphics {
        movieclip Flushmaster
        name "ENEMY_FLUSHMASTER_NAME"
        water_mask medium
        uifloaters_offset 2
        shadow none

        tooltip "ENEMY_FLUSHMASTER_DESC"
    }

    stats {
        strength 6
        dexterity 6
        constitution 6
        intelligence 6
        speed 0
        charisma 6
    }
    
    properties {
        tag [elemental poop]
        faction enemies
        type boss
        movement 6
        corpse_health 0
        initiative -30
        
        health 100

        elements [
            Water
        ]
    }

    abilities {
        move Teleport
        attack Flush
        
        spells [
        ]
    }

    passives {
        TransformOnDeath Dip
        FlushmasterCelebration celebrate
    }
    
    ai {
        brain PatternBrain

        pattern {
            do *Flush
        }

        decision_weights always_cast
        move_weights blind_move_far
        random_orient true
    }
}
```

---

### `MaggotLord`
**Name:** Mama Maggot  
**Source:** `minibosses.gon`  

```
MaggotLord {
    graphics {
        movieclip MamaMaggot
        name "ENEMY_MAMAMAGGOT_NAME"
        projectile_spawn_offset [-1 .5]
        water_mask medium

        tooltip "ENEMY_MAMAMAGGOT_DESC"
    }

    stats {
        strength  5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        faction enemies
        type boss

        mana_regen 999
        mana 100
        movement 3
        health 125
        
        round_start_bonus_turns 1
        round_end_bonus_turns 1

        size 2x2
        move_block everything_even_when_dead
        boss_minions_runaway false
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [
            SpawnMaggots
            MutateAOE
            RallyMaggots
        ]
    }

    passives {
        Trample 3

        SpawnThingOnDamage {
            object Maggot
            good false 
            spawn_on_death_hit false
            chance 33%
        }
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights keep_distance

        virtual_abilities {
            MoveClose {
                ability move
                move_weights stay_close_always_move
            }
        }

        round_start_bonusturn_pattern {
            do_priority [MutateAOE SpawnMaggots]
        }

        mainturn_pattern {
            do_priority [MutateAOE SpawnMaggots]
        }
        
        round_end_bonusturn_pattern {
            do RallyMaggots
        }

        fallback {
            do_priority [MoveClose SpawnMaggots]
        }
        
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `Lenny`
**Name:** Lenny  
**Source:** `minibosses.gon`  

```
Lenny {
    graphics {
        movieclip Lenny
        name "ENEMY_LENNY_NAME"
        uifloaters_offset 2

        tooltip "ENEMY_LENNY_DESC"
    }

    stats {
        strength 8
        dexterity 5
        constitution 5
        intelligence 0
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid]
        faction enemies
        type boss
        movement 4
        corpse_health 1
        dispersed_bonus_turns 2
        
        health 130
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack LennyShove
        
        spells [
            LennyGrab
            LennyHug
            LennyCatSlap

            LennyCatDies
            LennyDrop
            LennyStruggleFail
            LennyGrabDead
        ]
    }

    passives {
        Buddy choose_favorite_cat
        DisplayBuddyCatOnSpawn 3

        FormChanger {
            Default {
                move LennyTrampleMove
                attack LennyShove

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has HasCat
                    }
                    AggroTargetIsBuddy 1
                }

                ai {
                    brain PatternBrain

                    pattern {
                        move_then_do_all [LennyShove, LennyGrabDead, LennyGrab]
                    }

                    decision_weights default
                    move_weights stay_close_lenny
                    end_turn_on_formswitch true
                    reset_pattern_on_formswitch true
                }
            }
            HasCat {
                animation_suffix "Cat"
                attack LennyCatSlap

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot Default
                    }

                    DigestDeadBodies LennyCatDies
                    CounterAttack LennyCatSlap
                }

                ai {
                    brain PatternBrain

                    bonusturn_pattern {
                        do move
                    }
                    mainturn_pattern {
                        do LennyHug
                    }

                    decision_weights default
                    move_weights stay_far_always_move
                    end_turn_on_formswitch true
                    reset_pattern_on_formswitch true
                    auto_orient false
                }
            }
            HasDeadCat {
                animation_suffix "CatDead"
                attack LennyCatSlap

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_hasnot Default
                    }
                    CounterAttack LennyCatSlap
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do attack
                    }

                    decision_weights default
                    move_weights stay_close
                    end_turn_on_formswitch true
                    reset_pattern_on_formswitch true
                }
            }

            initial_form Default
        }
    }
    
    ai {
        brain NoBrain

        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Zodiac`
**Name:** Zodiac  
**Source:** `minibosses.gon`  

```
Zodiac {
    graphics {
        movieclip Zodiac
        name "ENEMY_ZODIAC_NAME"
        uifloaters_offset 1.6
        scale .8
		tooltip "ENEMY_ZODIAC_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag cat
        faction enemies
        type boss
        movement 6
        
        mana_regen 999
        mana 100
        
        health 75
        initiative 1000
    }

    abilities {
        move DefaultMove
        attack ZodiacShoot
        
        spells [
            Reload
        ]
    }

    passives {
        WeaponsDontLoseDurability 1
        Ammo 6

		BossRewards {
			common ZodiacsPoncho
			rare ZodiacsSixshooter
		}

        FormChanger {
            active {
                passives {
                    MovementReaction {
                        ability ZodiacShoot
                        objects_too true
                    }
                }
            }
            passive {
                attack DoNothing
            }

            initial_form active
        }
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do_all [*attack move Reload]
        }

        decision_weights default
        move_weights gunslinger_reposition
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `Cerberubs`
**Name:** Cerberubs  
**Source:** `minibosses.gon`  

```
Cerberubs {
    graphics {
        movieclip Cerberubs
        name "ENEMY_CERBERUBS_NAME"
        water_mask square
        scale .8

        tooltip "ENEMY_CERBERUBS_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [dog demon]
        faction enemies
        type boss
        movement 2
        dispersed_bonus_turns 1
        mana_regen 999
        mana 100
        
        health 200

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack CerberubsJump
        
        spells [
            CerberubsShotgunReaction
            CerberubsStraightReaction
            CerberubsThrow
            CerberubsBarrage
            CerberubsCalm
        ]
    }

    passives {
        Trample 3
        ImmediateAbilityReaction CerberubsStraightReaction
        ElementImmune Fire

        FormChanger {
            Normal {
                passives {
                    RandomizeAIWeightsEachTurn [
                        {
                            decision_weights default
                            move_weights chubs_and_nubs_blind
                        }

                        {
                            decision_weights default
                            move_weights chubs_and_nubs_blind
                        }

                        {
                            decision_weights default
                            move_weights stay_close_always_move
                        }
                    ]
                }

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights blind_move_far
                    auto_orient false
                    reset_pattern_on_formswitch true

                    virtual_abilities {
                        CerberubsJumpBlind {
                            ability CerberubsJump
                            decision_weights nubs_fakeblind
                        }
                        CerberubsJumpNormal {
                            ability CerberubsJump
                            decision_weights default
                        }
                    }

        
                    pattern {
                        move_then_do_random [CerberubsJumpBlind CerberubsJumpNormal]
                        move_then_do CerberubsBarrage
                    }
                }
            }
            Alert {
                partial_animation_suffix Alert

                ai {
                    brain PatternBrain
                    decision_weights default
                    move_weights stay_close

                    pattern {
                        do CerberubsThrow
                    }
                    fallback {
                        move_then_do CerberubsCalm
                    }
                }

                passives {
                    AddMovement 2
                }
            }
        }

        CerberubsAggroTargetBehavior {
            default_form Normal
            alert_form Alert
        }
    }
    
    ai {
        brain NoBrain 
    }
}
```

---

### `AstroZombie`
**Name:** Abandoned One  
**Source:** `minibosses.gon`  

```
AstroZombie {
    graphics {
        movieclip AstroZombie
        name "ENEMY_ASTROZOMBIE_NAME"
        uifloaters_offset 1.8
		tooltip "ENEMY_ASTROZOMBIE_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag [humanoid zombie]
        faction enemies
        type boss
        movement 2
        
        health 40
        disperse_main_turns true
    }

    abilities {
        move DefaultMove
        attack AZ_BreakNeck
        
        spells [
            AZ_Jump
            AZ_BreakLeg
            AZ_BreakArm
            AZ_LoseHead
        ]
    }

    passives {
        Undead 1

        FormChanger {
            Default {

                passives {
                    DeathRattleRevive {
                        ability AZ_LoseHead
                        even_if_stunned true
                    }
                }
            }
            Headless {
                animation_suffix "Headless"

                passives {
                    AddMovement 1
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do attack
                    }

                    decision_weights default
                    move_weights stay_close_always_move
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_random [AZ_BreakNeck AZ_BreakLeg AZ_BreakArm]
        }
        fallback {
            do AZ_Jump
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `AstroZombieHead`
**Name:** Abandoned One  
**Source:** `minibosses.gon`  

```
AstroZombieHead {
    graphics {
        movieclip AstroSkull
        name "ENEMY_ASTROZOMBIE_NAME"
        uifloaters_offset 1.8
		tooltip "ENEMY_ASTROZOMBIEHEAD_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag [humanoid zombie]
        faction enemies
        type boss
        movement 3
        corpse_health 0
        flying true
        
        health 20
        disperse_main_turns false
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            AZ_Scream
        ]
    }

    passives {
        Undead 1
		InnateElement Fire
        ElementImmune Fire
        StatusImmunity [Burn]
		
		AddStatusToBasicAttack {
            Burn 4
        }

        AddElementsToBasicAttack Fire
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [attack, AZ_Scream]
        }

        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `Spewer`
**Name:** Spewer  
**Source:** `minibosses.gon`  

```
Spewer {
    graphics {
        movieclip Spewer
        name "ENEMY_SPEWER_NAME"
        water_mask medmed
        scale .8
		tooltip "ENEMY_SPEWER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        movement 4
        health 100
        dispersed_bonus_turns 2
    }

    abilities {
        move DefaultMove
        attack SpewerLobbed_Normal
        
        spells [
            SpewerTransformNormal
            SpewerTransformFire
            SpewerTransformTar
            SpewerSuckNormal
            SpewerSuckTar
            SpewerSuckLava
            SpewerSuckPill
            SpewerBarf_Normal
            SpewerBarf_Tar
            SpewerBarf_Lava
        ]
    }

    passives {
	
		BossRewards {
			common RedPill
			rare ForbiddenPill
		}
		
        FormChanger {
            Normal {
                attack SpewerLobbed_Normal

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has NormalFull
                        form_hasnot Normal
                    }

                    CounterAttack SpewerSuckNormal
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_all [SpewerSuckPill SpewerBarf_Normal attack move]
                    }

                    decision_weights default
                    move_weights stay_far_move_far
                }
            }
            NormalFull {
                animation_suffix Full
                attack SpewerSpit

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has NormalFull
                        form_hasnot Normal
                    }
                    Trample 3

                    ChanceToSpitOnDamage {
                        flat_chance 100%
                        ability SpewerSpit
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [*SpewerTransformNormal *SpewerTransformFire *SpewerTransformTar attack]
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
            Fire {
                attack SpewerLobbed_Lava

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has FireFull
                        form_hasnot Fire
                    }

                    CounterAttack SpewerSuckLava
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_all [SpewerSuckPill SpewerBarf_Lava attack move]
                    }

                    decision_weights default
                    move_weights stay_far_move_far
                }
            }
            FireFull {
                animation_suffix Full
                attack SpewerSpit

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has FireFull
                        form_hasnot Fire
                    }
                    Trample 3

                    ChanceToSpitOnDamage {
                        flat_chance 100%
                        ability SpewerSpit
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [*SpewerTransformNormal *SpewerTransformFire *SpewerTransformTar attack]
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
            Tar {
                attack SpewerLobbed_Tar

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has TarFull
                        form_hasnot Tar
                    }

                    CounterAttack SpewerSuckTar
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_all [SpewerSuckPill SpewerBarf_Tar attack move]
                    }

                    decision_weights default
                    move_weights stay_far_move_far
                }
            }
            TarFull {
                animation_suffix Full
                attack SpewerSpit

                passives {
                    FormChangeWhileHasStatus {
                        status Consuming
                        form_has TarFull
                        form_hasnot Tar
                    }
                    Trample 3

                    ChanceToSpitOnDamage {
                        flat_chance 100%
                        ability SpewerSpit
                    }
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [*SpewerTransformNormal *SpewerTransformFire *SpewerTransformTar attack]
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
        }

        GoopWalk 1
        GoopImmunity 1

        SpewerAltGraphics {
            Normal 0
            NormalFull 0
            Fire 1
            FireFull 1
            Tar 2
            TarFull 2
        }
    }
    
    ai {
        brain NoBrain 

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `IceElemental`
**Name:** Frostbiter  
**Source:** `minibosses.gon`  

```
IceElemental {
    graphics {
        movieclip IceElemental
        name "ENEMY_FROSTBITER_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_FROSTBITER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [elemental poop]
        faction enemies
        type boss
        movement 4
        corpse_health 0
        round_end_bonus_turns 1

        initiative -999
        dispersed_bonus_turns 1
        takes_main_turn false
        
        health 200

        elements [
            Ice
        ]
    }

    abilities {
        move DefaultMove
        attack IceElementalSpikes
        
        spells [
            IceElementalBlizzard
            IceElementalBreath
        ]
    }

    passives {
        ElementImmune Ice
        ElementWeakness Fire
        TileElementDamageImmunity Ice
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_all [*attack *IceElementalBreath move]
        }

        round_end_bonusturn_pattern {
            do_all [*attack *IceElementalBlizzard move]
        }


        decision_weights default
        move_weights blind_move_far
    }
}
```

---

### `RatKing`
**Name:** Rat King  
**Source:** `minibosses.gon`  

```
RatKing {
    graphics {
        movieclip RatKing_New
        name "ENEMY_RATKING_NAME"
        water_mask square
        shadow_size 2
		tooltip "ENEMY_RATKING_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [rat]
        faction enemies
        type boss
        movement 2
        dispersed_bonus_turns 1
        
        health 100

        size 2x2
        move_block everything_even_when_dead
    }

    abilities {
        move DefaultMove
        attack RatKingToss
        
        spells [
            RatKingSpawn
            RatKing2Spawn
            RatKingTransform
        ]
    }

    passives {
        Trample 3

        FormChanger {
            Normal {
                passives {
                    ImmediateAbilityReaction {
                        ability RatKingTransform
                        health_threshold 70
                    }
                }
            }
            HalfDead {
                animation_suffix "2"
                attack RatKingDash
                
                passives {
                    AddMovement -2
                }

                ai {
                    brain PatternBrain
                    virtual_abilities {
                        MoveForDash {
                            ability move
                            move_for_ability attack
                            move_weights keep_distance
                        }
                    }

                    pattern {
                        do_all [MoveForDash RatKing2Spawn attack]
                    }

                    decision_weights spawn_far
                    move_weights keep_distance
                }
            }

            initial_form Normal
        }
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do attack
        }
        bonusturn_pattern {
            move_then_do RatKingSpawn
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `GirlDino`
**Name:** Pachysaurus [img:female]  
**Source:** `minibosses.gon`  

```
GirlDino {
    graphics {
        movieclip GirlDino
        name "ENEMY_GIRLDINO_NAME"
        water_mask square
        shadow_size 2
        uifloaters_offset 2
		tooltip "ENEMY_DINOLOVER_DESC"
    }

    stats {
        strength 7
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag dinosaur
        hidden_tag dinofamily
        faction enemies
        type boss
        movement 2
        
        
        health 50
        shield 50

        size 2x2
        move_block everything_even_when_dead
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack GirlDinoMelee
        
        spells [
            GirlDinoHeadBash
            GirlDinoCry
            GirlDinoThrow
            GirlDinoPoop
        ]
    }

    passives {
        Trample 3
        Brace 2
        Buddy BoyDino
        AbilityWhenBuddyDies GirlDinoCry

        FormChanger {
            Default {
                passives {
                    SecurityBotProtect {
                        
                        ability GirlDinoHeadBash
                        tag_restriction dinofamily
                        not_on_kill true
                    }
                }
            }
            Rage {
                turns {
                    dispersed_bonus_turns 1
                }
                passives {
                    SpeedUp 2
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do GirlDinoThrow
        }

        decision_weights spawn_far
        move_weights stay_close
    }
}
```

---

### `BoyDino`
**Name:** Pachysaurus [img:male]  
**Source:** `minibosses.gon`  

```
BoyDino {
    graphics {
        movieclip BoyDino
        name "ENEMY_BOYDINO_NAME"
        water_mask square
        shadow_size 2
        uifloaters_offset 2
		tooltip "ENEMY_DINOLOVER_DESC"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 8
        charisma 5
    }
    
    properties {
        tag dinosaur
        hidden_tag dinofamily
        faction enemies
        type boss
        movement 3
        
        
        health 50
        shield 25

        size 2x2
        move_block everything_even_when_dead
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack BoyDinoBasic
        
        spells [
            BoyDinoHeadBash
            BoyDinoCry
        ]
    }

    passives {
        Trample 3
        Brace 1
        Buddy GirlDino
        AbilityWhenBuddyDies BoyDinoCry

        FormChanger {
            Default {
                passives {
                    SecurityBotProtect {
                        
                        ability BoyDinoHeadBash
                        tag_restriction dinofamily
                        not_on_kill true
                    }
                }
            }
            Rage {
                turns {
                    dispersed_bonus_turns 1
                }
                passives {
                    StrengthUp 2
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `TheBloat`
**Name:** The Bloat  
**Source:** `minibosses.gon`  

```
TheBloat {
    graphics {
        movieclip TheBloat
        name "ENEMY_BLOAT_NAME"
        uifloaters_offset 1.8
        water_mask big
		tooltip "ENEMY_BLOAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag [blob]
        faction enemies
        type boss
        movement 1
        
        health 250
        dispersed_bonus_turns 1
    }

    abilities {
        move DefaultMove
        attack BloatFrontLaser
        
        spells [
            BloatSideLaser
            BloatLeap
            BloatLoseFirstEye
            BloatLoseSecondEye
        ]
    }

    passives {
        ElementImmune Creep
        Trample 3

        Trapper {
            ability BloatSideLaser
            range 10
            cancel_movement false
        }

        FormChanger {
            TwoEyes {
                passives {
                    AbilityHealthThreshold {
                        threshold "X*.8"
                        ability BloatLoseFirstEye
                    }
                }
            }
            OneEye {
                animation_suffix "1"

                passives {
                    AbilityHealthThreshold {
                        threshold "X*.4"
                        ability BloatLoseSecondEye
                    }
                }
            }
            NoEyes {
                animation_suffix "0"
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do_priority [attack BloatLeap]
            do_priority [BloatLeap attack]
        }

        decision_weights default
        move_weights keep_far_distance
    }
}
```

---

### `LightningElemental`
**Name:** Zapphauser  
**Source:** `minibosses.gon`  

```
LightningElemental {
    graphics {
        movieclip LightningElemental
        name "ENEMY_ZAPPHAUSER_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_ZAPPHAUSER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 3
        intelligence 5
        speed 20
        charisma 5
    }
    
    properties {
        tag [elemental]
        faction enemies
        type boss
        movement 3
        corpse_health 0
        flying true

        health 125
        dispersed_bonus_turns 3

        /*elements [ 
            Electric
        ]*/

        banned_elite_buffs [Protected]
    }

    abilities {
        move Teleport
        attack LEBurst
        
        spells [
            LELeave
            LEReturn
            LEPortFar
        ]
    }

    passives {
        ElementImmune Electric

        FormChanger {
            Default {
                passives {
                    CherubimReaction {
                        Leave LELeave
                        Return LEReturn
                    }
                }
            }
            OffMap {
                ai {
                    brain PatternBrain

                    pattern {
                        do_priority [LEReturn]
                    }

                    decision_weights default
                    move_weights keep_distance_always_move
                }
            }
        }

        FormChangeOffMap {
            form_offmap OffMap
            form_onmap Default
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do *LEBurst
        }

        decision_weights always_cast
        move_weights keep_distance_always_move
        end_turn_on_formswitch true
    }
}
```

---

### `DrMangler`
**Name:** Dr. Mangler  
**Source:** `minibosses.gon`  

```
DrMangler {
    graphics {
        movieclip DrMangler
        name "ENEMY_DRMANGLER_NAME"
        uifloaters_offset 2
		tooltip "ENEMY_DRMANGLER_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid robot]
        faction enemies
        type boss
        movement 5
        initiative -10

        health 185
        evenly_dispersed_bonus_turns 1
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack ManglerCommand
        
        spells [
            ManglerFumbleEven
            ManglerFumbleOdd
            ManglerEnrage
            ManglerThrowRemote
            ManglerSpin
        ]
    }

    passives {
        Robot 1
        Buddy ManglersMonster
        AbilityWhenBuddyDies ManglerEnrage

        FormChanger {
            Joystick {
                animation_suffix "Joystick"
                passives {
                    ImmediateAbilityReaction [ManglerFumbleEven ManglerFumbleOdd]
                }
            }
            NoStick {
                attack ManglerJab
                ai {
                    brain PatternBrain

                    pattern {
                        do_all [*ManglerSpin attack]
                    }

                    decision_weights default
                    move_weights stay_close_always_move
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do *attack
        }

        decision_weights default
        move_weights drmangler
    }
}
```

---

### `ManglersMonster`
**Name:** Mangler's Monster  
**Source:** `minibosses.gon`  

```
ManglersMonster {
    graphics {
        movieclip ManglersMonster
        name "ENEMY_MANGLERMONSTER_NAME"
        uifloaters_offset 2.5
        water_mask square
        four_way_animations true
		tooltip "ENEMY_MANGLERMONSTER_DESC"
    }

    stats {
        strength 8
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid blob]
        faction enemies
        type boss
        health 250

        size 3x3
        movement 1

        move_block everything_even_when_dead
        takes_turns false
        can_be_backstabbed false
        knockback_immune true
        banned_elite_buffs [Twin]
    }

    abilities {
        move None
        attack ManglerMonsterDashAttack

        spells [
            ManglerMonsterExplode
            ManglerMonsterHeartAttack
        ]
    }

    passives {
        Trample 3
        Buddy DrMangler
        ManglerMonsterPassive ManglerMonsterDashAttack
        OrthogonalAIDangerZone 10
        CCImmunity 1
        FormChanger {
            Default {
                passives {
                    DeathRattle ManglerMonsterExplode
                }
            }
            NoDeathRattle {
            }
        }
        AbilityWhenBuddyDies ManglerMonsterHeartAttack
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `GlowingBear`
**Name:** Glowing Bear  
**Source:** `minibosses.gon`  

```
GlowingBear {
    graphics {
        movieclip WhiteBear
        name "ENEMY_GLOWINGBEAR_NAME"
        shadow_size 2
		tooltip "ENEMY_GLOWINGBEAR_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag animal
        faction enemies
        type boss
        health 100
        movement 2
        weak_threshold 25
        
        evenly_dispersed_bonus_turns 1

        size 2x2
    }

    abilities {
        move DefaultMove
        attack BasicBigMelee
    }

    passives {
        Trample 3
		HealthRegenUp 4
        AddStatusToBasicAttack {
            Bleed 2
        }
		CharacterLightSource {
		    color [1, 1, 1]
            glow [1 1 1 1]
		    size 3
        }
    }
    
    ai {
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Death`
**Name:** Death!  
**Source:** `minibosses.gon`  

```
Death {
    graphics {
        movieclip Reaper
        name "ENEMY_DEATH_NAME"
        uifloaters_offset 1.5
        move_speed_multiplier .66
		scale 1.5
        tooltip "ENEMY_DEATH_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [ghost skeleton]
        faction enemies
        movement 4
        health 60
        corpse_health 0
        flying true
		dispersed_bonus_turns 3
    }

    abilities {
        move FloatMove
        attack ReaperSpin

        spells [
            ReaperRevenge
        ]
    }

    passives {
        MoveTowardsKillers ReaperRevenge
        
        Undead 1
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveClose {
                ability move
                move_for_ability attack
                move_weights stay_close_avoid_allies
            }
        }

        pattern {
            do_all [*attack, MoveClose, move]
        }

        decision_weights reaper
        move_weights stay_close_avoid_allies
    }
}
```

---

### `ShadowCat`
**Name:** Shadow Cat  
**Source:** `nemesis_bosses.gon`  

```
ShadowCat {
    graphics {
        movieclip _CAT
        name "ENEMY_SHADOWCAT_NAME"
        
        tint [0 0 0 1]
    }

    equipment {

    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [cat demon]
        faction enemies
        type boss
        movement 5
        corpse_health 3
        health 50
        disperse_main_turns true

        elements [
            Shadow
        ]
    }

    abilities {
        move DefaultMove
        attack ShadowDagger
        
        spells [
            ShadowstepDodge
        ]
    }

    passives {
        DodgeWhenTargeted {
            ability ShadowstepDodge
        }
        TileTrail ShadowTile
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `static_object_template`
**Name:** STATIC OBJECT  
**Source:** `non_interactive_objects.gon`  

```
static_object_template {
    graphics {
        movieclip Rock
        name "STATIC OBJECT"
        shade_occluded_objects true
        shadow None
        water_mask square
    }

    properties {
        faction none
        type object
        size 1x1
        takes_turns false
        corpse_health 0
        inanimate true
        static true
        knockback_immune true
        can_be_backstabbed false
        layer all
        ignore_mouseover true
        kill_required false
        aoe_pierce_mode block
    }

    abilities {
        move None
        attack None
    }
    
    ai {
        brain NoBrain
    }
}
```

---

### `Static1x1A`
**Source:** `non_interactive_objects.gon`  

```
Static1x1A {
    variant_of static_object_template
    graphics {
        movieclip static_1x1_a
    }
}
```

---

### `Static1x1B`
**Source:** `non_interactive_objects.gon`  

```
Static1x1B {
    variant_of static_object_template
    graphics {
        movieclip static_1x1_b
    }
}
```

---

### `Static1x1C`
**Source:** `non_interactive_objects.gon`  

```
Static1x1C {
    variant_of static_object_template
    graphics {
        movieclip static_1x1_c
    }
}
```

---

### `StaticTallA`
**Source:** `non_interactive_objects.gon`  

```
StaticTallA {
    variant_of static_object_template
    graphics {
        movieclip static_tall_a
        dont_sink true
    }
    properties {
        tall true
    }
}
```

---

### `StaticTallB`
**Source:** `non_interactive_objects.gon`  

```
StaticTallB {
    variant_of static_object_template
    graphics {
        movieclip static_tall_b
        dont_sink true
    }
    properties {
        tall true
    }
}
```

---

### `Static2x2A`
**Source:** `non_interactive_objects.gon`  

```
Static2x2A {
    variant_of static_object_template
    graphics {
        movieclip static_2x2_a
        dont_sink true
    }

    properties {
        size 2x2
        tall true
    }
}
```

---

### `Static2x2B`
**Source:** `non_interactive_objects.gon`  

```
Static2x2B {
    variant_of static_object_template
    graphics {
        movieclip static_2x2_b
        dont_sink true
    }

    properties {
        size 2x2
        tall true
    }
}
```

---

### `CandleSmall`
**Source:** `non_interactive_objects.gon`  

```
CandleSmall {
    variant_of static_object_template
    graphics {
        movieclip BunkerCandlesSmall
    }

    passives {
        CharacterLightSource {
            color [.7, .7, .5]
            size 1
        }
    }
}
```

---

### `CandleBig`
**Source:** `non_interactive_objects.gon`  

```
CandleBig {
    variant_of static_object_template
    graphics {
        movieclip BunkerCandles2x2
        dont_sink true
    }
    properties {
        size 2x2
        tall true
    }

    passives {
        CharacterLightSource {
            color [.7, .7, .5]
            size 3
        }
    }
}
```

---

### `PickupBase`
**Name:** Nothing!  
**Source:** `pickups.gon`  

```
PickupBase {
    graphics {
        movieclip Coin
        name "PICKUP_NOTHING_NAME"
        depth_offset .015
        shadow None
    }

    properties {
        faction none
        type object
        takes_turns false
        inanimate true
        can_be_backstabbed false
        layer pickups
        kill_required false
        tag pickup
    }

    abilities {
        move None
        attack None
    }

    ai {
        brain NoBrain
    }
}
```

---

### `Coin`
**Name:** Coin  
**Source:** `pickups.gon`  

```
Coin {
    variant_of PickupBase

    graphics {
        movieclip Coin
        name "PICKUP_COIN_NAME"

        tooltip "PICKUP_COIN_DESC"
    }
    sound {
	    alt_sounds [[HitGround Obj_CoinLand]]
    }

    properties {
        pickup_type 1
        tag [money pickup]

        elements [
            Metal
        ]
    }

    passives {
        CoinPickup 1
    }
}
```

---

### `Coin2`
**Source:** `pickups.gon`  

```
Coin2 {
    variant_of Coin

    passives {
        CoinPickup 2
    }
}
```

---

### `Coin3`
**Source:** `pickups.gon`  

```
Coin3 {
    variant_of Coin

    passives {
        CoinPickup 3
    }
}
```

---

### `Coin4`
**Source:** `pickups.gon`  

```
Coin4 {
    variant_of Coin

    passives {
        CoinPickup 4
    }
}
```

---

### `Coin5`
**Source:** `pickups.gon`  

```
Coin5 {
    variant_of Coin

    passives {
        CoinPickup 5
    }
}
```

---

### `Coin6`
**Source:** `pickups.gon`  

```
Coin6 {
    variant_of Coin

    passives {
        CoinPickup 6
    }
}
```

---

### `Coin7`
**Source:** `pickups.gon`  

```
Coin7 {
    variant_of Coin

    passives {
        CoinPickup 7
    }
}
```

---

### `Coin8`
**Source:** `pickups.gon`  

```
Coin8 {
    variant_of Coin

    passives {
        CoinPickup 8
    }
}
```

---

### `Coin9`
**Source:** `pickups.gon`  

```
Coin9 {
    variant_of Coin

    passives {
        CoinPickup 9
    }
}
```

---

### `Coin10`
**Source:** `pickups.gon`  

```
Coin10 {
    variant_of Coin

    passives {
        CoinPickup 10
    }
}
```

---

### `FoodBase`
**Name:** Food  
**Source:** `pickups.gon`  

```
FoodBase {
    variant_of PickupBase

    graphics {
        movieclip Food
        name "PICKUP_FOOD_NAME"

        tooltip "PICKUP_FOOD_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_FoodLand]]
	}

    properties {
        tag [food pickup]
    }

    passives {
        HealthPickup {
            stacks 4
            frame_range [1 2]
            stored_food_value 1
        }
    }
}
```

---

### `Food`
**Name:** Food  
**Source:** `pickups.gon`  

```
Food {
    variant_of FoodBase

    graphics {
        name "PICKUP_FOOD_NAME"

        tooltip "PICKUP_FOOD_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_FoodLand]]
	}

    passives {
        HealthPickup {
            stacks 4
            frame_range [1 2]
            stored_food_value 1
        }

        TransformOnElementInfluence {
            element Fire
            object CookedFood
        }
    }
}
```

---

### `BigFood`
**Name:** Medium Food  
**Source:** `pickups.gon`  

```
BigFood {
    variant_of FoodBase

    graphics {
        name "PICKUP_MEDIUMFOOD_NAME"

        tooltip "PICKUP_MEDIUMFOOD_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_FoodLand]]
	}

    passives {
        HealthPickup {
            stacks 7
            frame_range [3 4]
            stored_food_value 2
        }

        TransformOnElementInfluence {
            element Fire
            object CookedBigFood
        }
    }
}
```

---

### `BiggestFood`
**Name:** Big Food  
**Source:** `pickups.gon`  

```
BiggestFood {
    variant_of FoodBase

    graphics {
        name "PICKUP_BIGFOOD_NAME"

        tooltip "PICKUP_BIGFOOD_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_FoodLand]]
	}

    passives {
        HealthPickup {
            stacks 10
            frame_range [5 5]
            stored_food_value 3
        }

        TransformOnElementInfluence {
            element Fire
            object CookedBiggestFood
        }
    }
}
```

---

### `PoisonFood`
**Name:** Poisoned Food  
**Source:** `pickups.gon`  

```
PoisonFood {
    variant_of FoodBase

    graphics {
        name "PICKUP_POISONEDFOOD_NAME"

        tooltip "PICKUP_POISONEDFOOD_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_FoodLand]]
	}

    passives {
        HealthPickup {
            stacks 0
            frame_range [6 7]
            stored_food_value 0
        }

        StatusCollector {
            Poison 2
            Slow 2
        }

        TransformOnElementInfluence {
            element Fire
            object CookedPoisonFood
        }
        TransformOnElementInfluencex {
            element Holy
            object PurifiedPoisonFood
        }
    }
}
```

---

### `Bait`
**Name:** Bait  
**Source:** `pickups.gon`  

```
Bait {
    variant_of FoodBase

    graphics {
        name "PICKUP_BAIT_NAME"

        tooltip "PICKUP_BAIT_DESC"
    }

    passives {
        HealthPickup {
            stacks 1
            frame_range [8 8]
            anything_eats true
            stored_food_value 0
        }
        BaitAura {range 3}
        TransformOnElementInfluence {
            element Fire
            object CookedBait
        }
    }
}
```

---

### `PoisonBait`
**Name:** Poisoned Bait  
**Source:** `pickups.gon`  

```
PoisonBait {
    variant_of FoodBase

    graphics {
        name "PICKUP_POISONBAIT_NAME"

        tooltip "PICKUP_POISONBAIT_DESC"
    }

    passives {
        HealthPickup {
            stacks 0
            frame_range [19 19]
            anything_eats true
            stored_food_value 0
        }
        BaitAura {range 3}

        StatusCollector {
            Poison 2
            Slow 2
        }
        TransformOnElementInfluence {
            element Fire
            object CookedPoisonBait
        }
        TransformOnElementInfluencex {
            element Holy
            object Bait
        }
    }
}
```

---

### `CookedFood`
**Name:** Cooked Food  
**Source:** `pickups.gon`  

```
CookedFood {
    variant_of FoodBase

    graphics {
        name "PICKUP_COOKEDFOOD_NAME"

        tooltip "PICKUP_COOKEDFOOD_DESC"
    }

    passives {
        HealthPickup {
            stacks 4
            frame_range [9 10]
            stored_food_value 2
        }
        StatusCollector {
            StrengthUp 1
        }
    }
}
```

---

### `CookedBigFood`
**Name:** Cooked Medium Food  
**Source:** `pickups.gon`  

```
CookedBigFood {
    variant_of FoodBase

    graphics {
        name "PICKUP_COOKEDMEDIUMFOOD_NAME"

        tooltip "PICKUP_COOKEDMEDIUMFOOD_DESC"
    }

    passives {
        HealthPickup {
            stacks 7
            frame_range [11 12]
            stored_food_value 3
        }
        StatusCollector {
            StrengthUp 1
        }
    }
}
```

---

### `CookedChickenLeg`
**Source:** `pickups.gon`  

```
CookedChickenLeg {
    variant_of CookedBigFood

    passives {
        HealthPickup {
            force_frame 12
        }
    }
}
```

---

### `CookedBiggestFood`
**Name:** Cooked Big Food  
**Source:** `pickups.gon`  

```
CookedBiggestFood {
    variant_of FoodBase

    graphics {
        name "PICKUP_COOKEDBIGFOOD_NAME"

        tooltip "PICKUP_COOKEDBIGFOOD_DESC"
    }

    passives {
        HealthPickup {
            stacks 10
            frame_range [13 13]
            stored_food_value 4
        }
        StatusCollector {
            StrengthUp 1
        }
    }
}
```

---

### `CookedPoisonFood`
**Name:** Cooked Poisoned Food  
**Source:** `pickups.gon`  

```
CookedPoisonFood {
    variant_of FoodBase

    graphics {
        name "PICKUP_COOKEDPOISONEDFOOD_NAME"

        tooltip "PICKUP_COOKEDPOISONEDFOOD_DESC"
    }

    passives {
        HealthPickup {
            stacks 0
            frame_range [14 15]
            stored_food_value 0
        }

        StatusCollector {
            Poison 2
            Slow 2
            StrengthUp 1
        }
        TransformOnElementInfluence {
            element Holy
            object CookedPurifiedPoisonFood
        }
    }
}
```

---

### `PurifiedPoisonFood`
**Name:** Purified Food  
**Source:** `pickups.gon`  

```
PurifiedPoisonFood {
    variant_of FoodBase

    graphics {
        name "PICKUP_PURIFIEDFOOD_NAME"

        tooltip "PICKUP_PURIFIEDFOOD_DESC"
    }

    passives {
        HealthPickup {
            stacks 4
            frame_range [17 18]
            stored_food_value 1
        }
        TransformOnElementInfluence {
            element Fire
            object CookedPurifiedPoisonFood
        }
    }
}
```

---

### `CookedPurifiedPoisonFood`
**Name:** Cooked Purified Food  
**Source:** `pickups.gon`  

```
CookedPurifiedPoisonFood {
    variant_of FoodBase

    graphics {
        name "PICKUP_COOKEDPURIFIEDFOOD_NAME"

        tooltip "PICKUP_COOKEDPURIFIEDFOOD_DESC"
    }

    passives {
        HealthPickup {
            stacks 4
            frame_range [21 22]
            stored_food_value 2
        }
        StatusCollector {
            StrengthUp 1
        }
    }
}
```

---

### `CookedBait`
**Name:** Cooked Bait  
**Source:** `pickups.gon`  

```
CookedBait {
    variant_of FoodBase

    graphics {
        name "PICKUP_COOKEDBAIT_NAME"

        tooltip "PICKUP_COOKEDBAIT_DESC"
    }

    passives {
        HealthPickup {
            stacks 1
            frame_range [16 16]
            anything_eats true
            stored_food_value 0
        }
        BaitAura {range 3}
        StatusCollector {
            StrengthUp 1
        }
    }
}
```

---

### `CookedPoisonBait`
**Name:** Cooked Poisoned Bait  
**Source:** `pickups.gon`  

```
CookedPoisonBait {
    variant_of FoodBase

    graphics {
        name "PICKUP_COOKEDPOISONEDBAIT_NAME"

        tooltip "PICKUP_COOKEDPOISONEDBAIT_DESC"
    }

    passives {
        HealthPickup {
            stacks 0
            frame_range [20 20]
            anything_eats true
            stored_food_value 0
        }
        BaitAura {range 3}

        StatusCollector {
            Poison 2
            Slow 2
            StrengthUp 1
        }
        TransformOnElementInfluence {
            element Holy
            object CookedBait
        }
    }
}
```

---

### `Scrap`
**Name:** Scrap  
**Source:** `pickups.gon`  

```
Scrap {
    variant_of PickupBase

    graphics {
        movieclip ArmorPickup
        name "PICKUP_SCRAP_NAME"

        tooltip "PICKUP_SCRAP_DESC"
    }

    properties {
        tag [scrap pickup]
        elements [
            Metal
        ]
    }

    passives {
        ArmorPickup {
            stacks 2
            frame_range [1 2]
        }
    }
}
```

---

### `MedScrap`
**Name:** Medium Scrap  
**Source:** `pickups.gon`  

```
MedScrap {
    variant_of PickupBase

    graphics {
        movieclip ArmorPickup
        name "PICKUP_MEDIUMSCRAP_NAME"

        tooltip "PICKUP_MEDIUMSCRAP_DESC"
    }

    properties {
        tag [scrap pickup]
        elements [
            Metal
        ]
    }

    passives {
        ArmorPickup {
            stacks 4
            frame_range [3 5]
        }
    }
}
```

---

### `BigScrap`
**Name:** Big Scrap  
**Source:** `pickups.gon`  

```
BigScrap {
    variant_of PickupBase

    graphics {
        movieclip ArmorPickup
        name "PICKUP_BIGSCRAP_NAME"

        tooltip "PICKUP_BIGSCRAP_DESC"
    }

    properties {
        tag [scrap pickup]
        elements [
            Metal
        ]
    }

    passives {
        ArmorPickup {
            stacks 6
            frame_range [6 6]
        }
    }
}
```

---

### `Blessing`
**Name:** Blessing  
**Source:** `pickups.gon`  

```
Blessing {
    variant_of PickupBase

    graphics {
        movieclip HolyPickup
        name "PICKUP_BLESSING_NAME"

        tooltip "PICKUP_BLESSING_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_HolyPickupLand]]
	}

    passives {
        DivineShieldPickup 1
    }
}
```

---

### `Antidote`
**Name:** Antidote  
**Source:** `pickups.gon`  

```
Antidote {
    variant_of PickupBase

    graphics {
        movieclip AntidotePickup
        name "PICKUP_ANTIDOTE_NAME"

        tooltip "PICKUP_ANTIDOTE_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_AntidotePickupLand]]
	}

    passives {
        ModularPickup {
            Cleanse 0
            sound_event EatAntidote
        }
    }
}
```

---

### `Catnip`
**Name:** Catnip  
**Source:** `pickups.gon`  

```
Catnip {
    variant_of PickupBase

    graphics {
        movieclip ManaPickup
        name "PICKUP_CATNIP_NAME"

        tooltip "PICKUP_CATNIP_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_ManaPickupLand]]
	}

    passives {
        ManaPickup {
            stacks 2
            frame_range [1 2]
        }
    }
}
```

---

### `MedCatnip`
**Name:** Medium Catnip  
**Source:** `pickups.gon`  

```
MedCatnip {
    variant_of PickupBase

    graphics {
        movieclip ManaPickup
        name "PICKUP_MEDIUMCATNIP_NAME"

        tooltip "PICKUP_MEDIUMCATNIP_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_ManaPickupLand]]
	}

    passives {
        ManaPickup {
            stacks 4
            frame_range [3 5]
        }
    }
}
```

---

### `BigCatnip`
**Name:** Big Catnip  
**Source:** `pickups.gon`  

```
BigCatnip {
    variant_of PickupBase

    graphics {
        movieclip ManaPickup
        name "PICKUP_BIGCATNIP_NAME"

        tooltip "PICKUP_BIGCATNIP_DESC"
    }
    sound {
		alt_sounds [[HitGround Obj_ManaPickupLand]]
	}

    passives {
        ManaPickup {
            stacks 6
            frame_range [6 6]
        }
    }
}
```

---

### `RandomPickup`
**Source:** `pickups.gon`  

```
RandomPickup {
    alt_spawn_pool {
        Coin 70
        RandomFoodPickup 15
        RandomArmorPickup 4.5
        RandomCatnipPickup 10
        Antidote .5
        Blessing .5
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `RandomNonCoinPickup`
**Source:** `pickups.gon`  

```
RandomNonCoinPickup {
    alt_spawn_pool {
        RandomFoodPickup 40
        RandomArmorPickup 40
        RandomCatnipPickup 30
        Antidote 1
        Blessing 1
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `RandomCatnipPickup`
**Source:** `pickups.gon`  

```
RandomCatnipPickup {
    alt_spawn_pool {
        Catnip 20
        MedCatnip 5
        BigCatnip 1
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `RandomBiggerCatnipPickup`
**Source:** `pickups.gon`  

```
RandomBiggerCatnipPickup {
    alt_spawn_pool {
        MedCatnip 20
        BigCatnip 6
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `RandomFoodPickup`
**Source:** `pickups.gon`  

```
RandomFoodPickup {
    alt_spawn_pool {
        Food 20
        BigFood 5
        BiggestFood 1
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `RandomBiggerFoodPickup`
**Source:** `pickups.gon`  

```
RandomBiggerFoodPickup {
    alt_spawn_pool {
        BigFood 20
        BiggestFood 6
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `RandomArmorPickup`
**Source:** `pickups.gon`  

```
RandomArmorPickup {
    alt_spawn_pool {
        Scrap 20
        MedScrap 5
        BigScrap 1
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `RandomBiggerArmorPickup`
**Source:** `pickups.gon`  

```
RandomBiggerArmorPickup {
    alt_spawn_pool {
        MedScrap 20
        BigScrap 6
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `RandomBiggerPickup`
**Source:** `pickups.gon`  

```
RandomBiggerPickup {
    alt_spawn_pool {
        Coin 70
        RandomBiggerFoodPickup 15
        RandomBiggerArmorPickup 4.5
        RandomBiggerCatnipPickup 10
        Antidote .5
        Blessing .5
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `RandomBiggestPickup`
**Source:** `pickups.gon`  

```
RandomBiggestPickup {
    alt_spawn_pool {
        Coin 70
        BiggestFood 15
        BigScrap 4.5
        BigCatnip 10
        Antidote .5
        Blessing .5
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `SlotMachineNormalPickupReward`
**Source:** `pickups.gon`  

```
SlotMachineNormalPickupReward {
    alt_spawn_pool {
        Coin 1
        Coin2 1
        Coin3 1
        Coin4 1
        Coin10 .1
        BiggestFood 4
        BigScrap 2
        BigCatnip 2
        Antidote 1
        Blessing 1
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `SlotMachineJackpotCoinsReward`
**Source:** `pickups.gon`  

```
SlotMachineJackpotCoinsReward {
    alt_spawn_pool {
        Coin3 1
        Coin4 1
        Coin10 1
    }

    properties {
        layer pickups
        can_be_champion false
    }
}
```

---

### `PlayerCat`
**Name:** {Catname}  
**Source:** `player_cat.gon`  

```
PlayerCat {
    graphics {
        movieclip _CAT
        shadow_size 1
        name "PLAYER_CAT_NAME"
        projectile_spawn_offset [.5 .75]

        tooltip "PLAYER_CAT_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        faction allies
        type cat

        
        base_movement 4
        base_initiative 0
        base_health 0
        base_mana 0
        base_mana_regen 0
        base_health_regen 0
        base_initial_mana 0
        base_crit_chance 0
        mana_matters true
        
        
        weak_threshold 5 

        can_be_overkilled false 
        can_collect_coins true
        can_eat_food true
        access_to_player_inventory true
        corpse_health 3
        is_player_cat true
        can_run false
        exclude_from_hallucinate true
        
        uncapturable true
        
        allow_flying_effect true
    }

    abilities {
        can_get_bonus true
    }

    passives {

    }
    
    ai {
        brain PlayerBrain
        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `CustomEnemyCat`
**Source:** `player_cat.gon`  

```
CustomEnemyCat {
    variant_of PlayerCat

    graphics {
    }

    properties {
        faction enemies

        can_be_overkilled true
        allow_passive_spelltransforming true

        can_collect_coins false
        can_eat_food false
        access_to_player_inventory false
        corpse_health 1
        is_player_cat false
        exclude_from_hallucinate true

        uncapturable false
        capture_as_cat true
    }

    ai {
        brain GenericBrain
    }
}
```

---

### `PlayerCat_Shade`
**Source:** `player_cat.gon`  

```
PlayerCat_Shade {
    variant_of PlayerCat

    graphics {
        tint [0 0 0 1]
    }

    properties {
        corpse_health 0
        can_grant_extra_turns false
    }

    passives {
        FadeInsteadOfDie 1
    }
}
```

---

### `PlayerCat_ThiefShade`
**Source:** `player_cat.gon`  

```
PlayerCat_ThiefShade {
    variant_of PlayerCat

    graphics {
        tint [0 0 0 1]
    }

    properties {
        corpse_health 0
        can_grant_extra_turns false
        takes_turns false
        health 1
        weak_threshold 0
        catdata_ignore_skills true
        is_player_cat false
        move_block nothing
    }

    passives {
        FadeInsteadOfDie 1
        ExpireOnSpawnerTurnEnd 1
        MimicSpawnerAttacks 1
    }
}
```

---

### `PlayerCat_ThiefShade2`
**Source:** `player_cat.gon`  

```
PlayerCat_ThiefShade2 {
    variant_of PlayerCat

    graphics {
        tint [0 0 0 1]
    }

    properties {
        corpse_health 0
        can_grant_extra_turns false
        takes_turns false
        health 1
        weak_threshold 0
        catdata_ignore_skills true
        is_player_cat false
        move_block nothing
    }

    passives {
        FadeInsteadOfDie 1
        MimicSpawnerAttacks 1
    }
}
```

---

### `PlayerCat_MonkShade`
**Source:** `player_cat.gon`  

```
PlayerCat_MonkShade {
    variant_of PlayerCat

    graphics {
        tint yellow
    }

    properties {
        corpse_health 0
        can_grant_extra_turns false
        takes_turns false
        health 1
        weak_threshold 0
        catdata_ignore_skills true
        is_player_cat false
        move_block nothing
    }

    passives {
        FadeInsteadOfDie 1
        ExpireOnSpawnerTurnEnd 1
        MimicSpawnerAttacks -1
    }
}
```

---

### `PlayerCat_MiniMe`
**Name:** Mini-{Catname}  
**Source:** `player_cat.gon`  

```
PlayerCat_MiniMe {
    variant_of PlayerCat

    graphics {
        name "PLAYER_MINIME_NAME" 
        scale .75
    }

    passives {
        BaseStatMultiply .5
    }

    ai {
        brain GenericBrain
    }
}
```

---

### `PlayerCat_MiniMiniMe`
**Name:** Mini-Mini-{Catname}  
**Source:** `player_cat.gon`  

```
PlayerCat_MiniMiniMe {
    variant_of PlayerCat

    graphics {
        name "PLAYER_MINIMINIME_NAME"
        scale .5
    }

    passives {
        BaseStatMultiply .25
    }

    ai {
        brain GenericBrain
    }
}
```

---

### `PlayerCat_MonkMiniMe`
**Source:** `player_cat.gon`  

```
PlayerCat_MonkMiniMe {
    variant_of PlayerCat_MiniMe

    passives {
        DisableSpells 1
    }
}
```

---

### `PlayerCat_FleshGolem`
**Name:** Flesh Golem  
**Source:** `player_cat.gon`  

```
PlayerCat_FleshGolem {
    variant_of PlayerCat
    graphics {
        name "PLAYER_FLESHGOLEM_NAME"
    }
}
```

---

### `PlayerCat_CambionMiniMe`
**Name:** Mini-{Catname}  
**Source:** `player_cat.gon`  

```
PlayerCat_CambionMiniMe {
    variant_of PlayerCat

    graphics {
        name "PLAYER_MINIME_NAME"
        scale .75
    }

    properties {
        tag [cat demon]
    }
    
    passives {
        BaseStatMultiply .666

        CatPartsTransform {
            palette 59
            eye1 1013
            eye2 1013
            ear1 1013
            ear2 1013
        }
    }

    ai {
        brain GenericBrain
    }
}
```

---

### `PlayerCat_NecroShade`
**Source:** `player_cat.gon`  

```
PlayerCat_NecroShade {
    variant_of PlayerCat

    graphics {
        tint [0 0 0 1]
    }

    properties {
        corpse_health 0
        can_grant_extra_turns false
    }

    passives {
        SafeDoomed 1
        InjuryImmunity 1
        FadeInsteadOfDie 1
    }
}
```

---

### `PlayerCat_AncestralShade`
**Source:** `player_cat.gon`  

```
PlayerCat_AncestralShade {
    variant_of PlayerCat
    
    properties {
        corpse_health 0
        can_grant_extra_turns false
    }

    passives {
        SafeDoomed 1
        InjuryImmunity 1
        FadeInsteadOfDie 1
        IllusionTint 1
    }
}
```

---

### `PlayerCat_StevenShade`
**Name:** Steven  
**Source:** `player_cat.gon`  

```
PlayerCat_StevenShade {
    variant_of PlayerCat

    properties {
        corpse_health 0
        can_grant_extra_turns false
    }
    
    graphics {
        name "ITEM_STEVENSCONSUMABLE2_NAME"
        tint [0, 0, 0, 1]
        spawnin_animation poofIntoExistance
    }
    
    passives {
        InjuryImmunity 1
        FadeInsteadOfDie 1
    }
}
```

---

### `PlayerCat_MachineClone`
**Name:** {Catname} Clone  
**Source:** `player_cat.gon`  

```
PlayerCat_MachineClone {
    variant_of PlayerCat

    graphics {
        name "PLAYER_CATCLONE_NAME" 
    }
    
    ai {
        brain GenericBrain
    }
}
```

---

### `PlayerCat_ClotClone`
**Name:** {Catname} Clone  
**Source:** `player_cat.gon`  

```
PlayerCat_ClotClone {
    variant_of PlayerCat

    graphics {
        name "PLAYER_CATCLONE_NAME" 
        scale .75

        tint [.7, .4, .4, 1]
    }

    passives {
        StatusOnSpawnIn {
            SetHealth 50%
        }
    }

    ai {
        brain GenericBrain
    }
}
```

---

### `Bunny`
**Name:** Bunny  
**Source:** `rare_cat_tests.gon`  

```
Bunny {
    graphics {
        movieclip _CAT
        name "Bunny"
        custom_cat_data Bunny
        scale .8
        shadow_size .8

        tooltip "Bunny!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Beaver`
**Name:** Beaver  
**Source:** `rare_cat_tests.gon`  

```
Beaver {
    graphics {
        movieclip _CAT
        name "Beaver"
        custom_cat_data Beaver
        scale .8
        shadow_size .8

        tooltip "Beaver!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Pig`
**Name:** Pig  
**Source:** `rare_cat_tests.gon`  

```
Pig {
    graphics {
        movieclip _CAT
        name "Pig"
        custom_cat_data Pig
        scale 1
        shadow_size 1

        tooltip "Pig!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Dog`
**Name:** Dog  
**Source:** `rare_cat_tests.gon`  

```
Dog {
    graphics {
        movieclip _CAT
        name "Dog"
        custom_cat_data Dog
        scale 1
        shadow_size 1

        tooltip "Dog!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Skunk`
**Name:** Skunk  
**Source:** `rare_cat_tests.gon`  

```
Skunk {
    graphics {
        movieclip _CAT
        name "Skunk"
        custom_cat_data Skunk
        scale .8
        shadow_size .8

        tooltip "Skunk!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Porcupine`
**Name:** Porcupine  
**Source:** `rare_cat_tests.gon`  

```
Porcupine {
    graphics {
        movieclip _CAT
        name "Porcupine"
        custom_cat_data Porcupine
        scale .8
        shadow_size .8

        tooltip "Porcupine!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Isaac`
**Name:** Isaac  
**Source:** `rare_cat_tests.gon`  

```
Isaac {
    graphics {
        movieclip _CAT
        name "Isaac"
        custom_cat_data Isaac
        scale 1
        shadow_size 1

        tooltip "Isaac!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Edmund`
**Name:** Edmund  
**Source:** `rare_cat_tests.gon`  

```
Edmund {
    graphics {
        movieclip _CAT
        name "Edmund"
        custom_cat_data Edmund
        scale 1
        shadow_size 1

        tooltip "Edmund!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Tyler`
**Name:** Tyler  
**Source:** `rare_cat_tests.gon`  

```
Tyler {
    graphics {
        movieclip _CAT
        name "Tyler"
        custom_cat_data Tyler
        scale 1
        shadow_size 1

        tooltip "Tyler!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `FijiMermaid`
**Name:** Fiji Mermaid  
**Source:** `rare_cat_tests.gon`  

```
FijiMermaid {
    graphics {
        movieclip _CAT
        name "Fiji Mermaid"
        custom_cat_data FijiMermaid
        scale 1
        shadow_size 1

        tooltip "The Fiji Mermaid!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `JerseyDevil`
**Name:** Jersey Devil  
**Source:** `rare_cat_tests.gon`  

```
JerseyDevil {
    graphics {
        movieclip _CAT
        name "Jersey Devil"
        custom_cat_data JerseyDevil
        scale 1
        shadow_size 1

        tooltip "The Jersey Devil!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Sonichu`
**Name:** Sonichu  
**Source:** `rare_cat_tests.gon`  

```
Sonichu {
    graphics {
        movieclip _CAT
        name "Sonichu"
        custom_cat_data Sonichu
        scale 1
        shadow_size 1

        tooltip "Sonichu!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Bigfoot`
**Name:** Bigfoot  
**Source:** `rare_cat_tests.gon`  

```
Bigfoot {
    graphics {
        movieclip _CAT
        name "Bigfoot"
        custom_cat_data Bigfoot
        scale 1.3
        shadow_size 1.3

        tooltip "Bigfoot!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Nessie`
**Name:** Nessie  
**Source:** `rare_cat_tests.gon`  

```
Nessie {
    graphics {
        movieclip _CAT
        name "Nessie"
        custom_cat_data Nessie
        scale 1
        shadow_size 1

        tooltip "Nessie!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Grey`
**Name:** Grey Alien  
**Source:** `rare_cat_tests.gon`  

```
Grey {
    graphics {
        movieclip _CAT
        name "Grey Alien"
        custom_cat_data Grey
        scale 1
        shadow_size 1

        tooltip "Grey Alien!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Mothman`
**Name:** Mothman  
**Source:** `rare_cat_tests.gon`  

```
Mothman {
    graphics {
        movieclip _CAT
        name "Mothman"
        custom_cat_data Mothman
        scale 1
        shadow_size 1

        tooltip "Mothman!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Slenderman`
**Name:** Slendermann  
**Source:** `rare_cat_tests.gon`  

```
Slenderman {
    graphics {
        movieclip _CAT
        name "Slendermann"
        custom_cat_data Slenderman
        scale 1
        shadow_size 1

        tooltip "Slenderman!"
    }
    

    stats {
        strength 6
        dexterity 5
        constitution 5
        intelligence 5
        speed 1
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        YOffset .35
        IgnoreTiles 1
        StatusImmunity Webbed
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `OrganZodiac`
**Name:** {organname}  
**Source:** `rifthead.gon`  

```
OrganZodiac {
    graphics {
        movieclip OrganGrinderX
        name "ENEMY_ORGANZODIAC_NAME"
        uifloaters_offset 1.6
        scale .8
		tooltip "ENEMY_ZODIAC_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }
    
    properties {
        tag cat
        hidden_tag riftheadguardian
        faction enemies
        type boss
        movement 6
        
        mana_regen 999
        mana 100

        corpse_health 0
        
        health 80
        initiative 1000

        banned_elite_buffs [Shielded1 Shielded2 Shielded3 Shielded4]
    }

    abilities {
        move DefaultMove
        attack ZodiacShootX
        
        spells [
            Reload
        ]
    }

    passives {
        Ammo 6

        SpawnOnDeath {
            obj RiftKitten
            faction allies
        }
        SpawnOnDeath Maggot
        SpawnOnDeath Maggot
        SpawnOnDeath Maggot
        SpawnOnDeath Maggot

        FormChanger {
            active {
                passives {
                    MovementReaction {
                        ability ZodiacShootX
                        objects_too true
                    }
                }
            }
            passive {
                attack DoNothing
            }

            initial_form active
        }
    }
    
    ai {
        brain PatternBrain

        mainturn_pattern {
            do_all [*attack move Reload]
        }

        decision_weights default
        move_weights gunslinger_reposition
        fallback_advances_pattern true
        stun_advances_pattern false
    }
}
```

---

### `BigSlimeX`
**Name:** Steven  
**Source:** `rifthead.gon`  

```
BigSlimeX {
    graphics {
        movieclip BigSlimeX
        name "ENEMY_STEVENSLIME_NAME"
        shadow BigSlimeShadow

        tooltip "ENEMY_BIGSTEVENSLIME_DESC"

        water_mask medium
    }

    stats {
        strength 10
        dexterity 6
        constitution 6
        intelligence 6
        speed 6
        charisma 6
    }
    
    properties {
        tag blob
        hidden_tag riftheadguardian
        faction enemies
        type boss
        movement 4
        dispersed_bonus_turns 1
        corpse_health 0
        
        health 64

        size 2x2
        move_block everything_even_when_dead

        banned_elite_buffs [Shielded1 Shielded2 Shielded3 Shielded4]
    }

    abilities {
        move DefaultMove
        attack BasicBigMelee
        
        spells [
        ]
    }

    passives {
        Trample 3
        Divide4OnDeath MedSlimeX
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `MedSlimeX`
**Name:** Steven  
**Source:** `rifthead.gon`  

```
MedSlimeX {
    graphics {
        movieclip MedSlimeX
        name "ENEMY_STEVENSLIME_NAME"
        shadow MedSlimeShadow

        tooltip "ENEMY_MIDSTEVENSLIME_DESC"

        water_mask medium
    }

    stats {
        strength 5
        dexterity 3
        constitution 3
        intelligence 3
        speed 3
        charisma 3
    }
    
    properties {
        tag blob
        hidden_tag riftheadguardian
        faction enemies
        type boss
        movement 3
        corpse_health 0
        
        health 16

        banned_elite_buffs [Shielded1 Shielded2 Shielded3 Shielded4]
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
        ]
    }

    passives {
        Divide4OnDeath SmallSlimeX
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `SmallSlimeX`
**Name:** Steven  
**Source:** `rifthead.gon`  

```
SmallSlimeX {
    graphics {
        movieclip SmallSlimeX
        name "ENEMY_STEVENSLIME_NAME"
        shadow SmallSlimeShadow
		tooltip "ENEMY_SMALLSTEVENSLIME_DESC"
    }

    stats {
        strength 2
        dexterity 1
        constitution 1
        intelligence 1
        speed 1
        charisma 1
    }
    
    properties {
        tag blob
        hidden_tag riftheadguardian
        faction enemies
        type boss
        movement 2
        corpse_health 0
        
        health 4
        held_coins [0 1]
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
        ]
    }

    passives {
        ChangeTileOnPop GlitchTile
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Chaos`
**Name:** Soahc  
**Source:** `rifthead.gon`  

```
Chaos {
    graphics {
        movieclip Chaos
        name "ENEMY_CHAOS_NAME"
        uifloaters_offset 4
        shadow_size 2.2
		tooltip "ENEMY_CHAOS_DESC"
		scale 1.1
    }

    stats {
        strength 8
        dexterity 8
        constitution 8
        intelligence 8
        speed 8
        charisma 8
    }
    
    properties {
        tag humanoid
        faction enemies
        type boss
        movement 0
        evenly_dispersed_bonus_turns 1
        initiative -999
        corpse_health 1
        knockback_immune true
        flying true
        
        health 400

        size 2x2
        move_block everything_even_when_dead
        banned_elite_buffs [Twin]
    }

    abilities {
        move None
        attack BasicBigMelee
        
        spells [
            ChaosSwitchSides
            DbgChaosSwitchFormsA
            DbgChaosSwitchFormsP
            ChaosSwitchForms
            SpreadX
            MegablastX
            FlushX
            ThornUpX
            CerberubsShotgunReactionX
            ChaosSpawnIn
        ]
    }

    passives {
        Trample 3
        LockOrientationFaceTile [0 0]
        StartOffMap 1

        FormChanger {
            OffScreen {
                turns {
                    takes_turns false
                }
                passives {
                    ChaosHeadDropIn {
                        tag riftheadguardian
                        ability ChaosSpawnIn
                        new_music chaos_boss_part2
                    }
                }
            }

            Default {
                ai {
                    brain PatternBrain

                    pattern {
                        do_all [ChaosSwitchSides ChaosSwitchForms]
                    }

                    decision_weights default
                    move_weights chaos_always_move
                }
                turns {
                    takes_turns true
                    evenly_dispersed_bonus_turns 1
                }
            }

            
            Johnny {
                ai {
                    brain PatternBrain

                    pattern {
                        do_all [MegablastX ChaosSwitchSides ChaosSwitchForms]
                    }

                    decision_weights default
                    move_weights chaos_always_move
                    end_turn_on_formswitch true
                }
            }
            Throb {
                ai {
                    brain PatternBrain

                    pattern {
                        do SpreadX
                        do_all [ChaosSwitchSides ChaosSwitchForms]
                    }

                    decision_weights default
                    move_weights chaos_always_move
                    reset_pattern_on_formswitch true
                    stun_advances_pattern true
                    clamp_pattern true
                }
            }
            Flush {
                ai {
                    brain PatternBrain

                    pattern {
                        do_all [FlushX ChaosSwitchSides ChaosSwitchForms]
                    }

                    decision_weights default
                    move_weights chaos_always_move
                    end_turn_on_formswitch true
                }
            }

            

            
                JohnnyHost {
                    partial_animation_suffix Host

                    passives {
                        ReflectProjectiles {
                            self_damage 2
                        }

                        MeleeRevengeDamage {
                            type status
                            damage 0
                            knockback 4
                        }
                    }

                    ai {
                        brain PatternBrain

                        pattern {
                            do_all [MegablastX ChaosSwitchSides ChaosSwitchForms]
                        }

                        decision_weights default
                        move_weights chaos_always_move
                        end_turn_on_formswitch true
                    }
                }
                JohnnyNettle {

                    passives {
                        AbilityAfterEnemyCastSpell_Stackable ThornUpX
                        Thorns 1
                        KineticSpikes 1
                    }

                    ai {
                        brain PatternBrain

                        pattern {
                            do_all [MegablastX ChaosSwitchSides ChaosSwitchForms]
                        }

                        decision_weights default
                        move_weights chaos_always_move
                        end_turn_on_formswitch true
                    }
                }
                JohnnyBubs {

                    passives {
                        ImmediateAbilityReaction CerberubsShotgunReactionX
                    }

                    ai {
                        brain PatternBrain

                        pattern {
                            do_all [MegablastX ChaosSwitchSides ChaosSwitchForms]
                        }

                        decision_weights default
                        move_weights chaos_always_move
                        end_turn_on_formswitch true
                    }
                }

            
                ThrobHost {
                    partial_animation_suffix Host

                    passives {
                        ReflectProjectiles {
                            self_damage 2
                        }

                        MeleeRevengeDamage {
                            type status
                            damage 0
                            knockback 4
                        }
                    }

                    ai {
                        brain PatternBrain

                        pattern {
                            do SpreadX
                            do_all [ChaosSwitchSides ChaosSwitchForms]
                        }

                        decision_weights default
                        move_weights chaos_always_move
                        reset_pattern_on_formswitch true
                        stun_advances_pattern true
                        clamp_pattern true
                    }
                }
                ThrobNettle {

                    passives {
                        AbilityAfterEnemyCastSpell_Stackable ThornUpX
                        Thorns 1
                        KineticSpikes 1
                    }

                    ai {
                        brain PatternBrain

                        pattern {
                            do SpreadX
                            do_all [ChaosSwitchSides ChaosSwitchForms]
                        }

                        decision_weights default
                        move_weights chaos_always_move
                        reset_pattern_on_formswitch true
                        stun_advances_pattern true
                        clamp_pattern true
                    }
                }
                ThrobBubs {

                    passives {
                        ImmediateAbilityReaction CerberubsShotgunReactionX
                    }

                    ai {
                        brain PatternBrain

                        pattern {
                            do SpreadX
                            do_all [ChaosSwitchSides ChaosSwitchForms]
                        }

                        decision_weights default
                        move_weights chaos_always_move
                        reset_pattern_on_formswitch true
                        stun_advances_pattern true
                        clamp_pattern true
                    }
                }

            
                FlushHost {
                    partial_animation_suffix Host

                    passives {
                        ReflectProjectiles {
                            self_damage 2
                        }

                        MeleeRevengeDamage {
                            type status
                            damage 0
                            knockback 4
                        }
                    }

                    ai {
                        brain PatternBrain

                        pattern {
                            do_all [FlushX ChaosSwitchSides ChaosSwitchForms]
                        }

                        decision_weights default
                        move_weights chaos_always_move
                        end_turn_on_formswitch true
                    }
                }
                FlushNettle {

                    passives {
                        AbilityAfterEnemyCastSpell_Stackable ThornUpX
                        Thorns 1
                        KineticSpikes 1
                    }

                    ai {
                        brain PatternBrain

                        pattern {
                            do_all [FlushX ChaosSwitchSides ChaosSwitchForms]
                        }

                        decision_weights default
                        move_weights chaos_always_move
                        end_turn_on_formswitch true
                    }
                }
                FlushBubs {

                    passives {
                        ImmediateAbilityReaction CerberubsShotgunReactionX
                    }

                    ai {
                        brain PatternBrain

                        pattern {
                            do_all [FlushX ChaosSwitchSides ChaosSwitchForms]
                        }

                        decision_weights default
                        move_weights chaos_always_move
                        end_turn_on_formswitch true
                    }
                }
        }

        ChaosBossFormChangeGuide {
            active_pieces [Johnny Throb Flush]
            passive_pieces [Host Nettle Bubs]
            passives_health_threshold 50% 
            

        }

        ChaosBossPieces {
            active_pieces [Johnny Throb Flush]
            passive_pieces [Host Nettle Bubs]
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `RiftKitten`
**Name:** Gun  
**Source:** `rifthead.gon`  

```
RiftKitten { 
    graphics {
        movieclip _CAT
        name "FAMILIAR_RIFTKITTEN_NAME"
        custom_cat_data TrailerCat
        scale .8
        shadow_size .8
		tooltip "FAMILIAR_RIFTKITTEN_DESC"
    }

    stats {
        strength 4
        dexterity 4
        constitution 4
        intelligence 4
        speed 4
        charisma 4
        luck 4
    }
    
    properties {
        tag cat
        type cat
        health 16
        faction allies
        mana_matters true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        can_get_bonus true
        
        spells [
            
        ]
    }

    passives {
        ConjureBonusAbility random
    }
    
    ai {
        brain PlayerBrain
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `Fly`
**Name:** Fly  
**Source:** `small_enemies.gon`  

```
Fly {
    graphics {
        movieclip Fly
        name "ENEMY_FLY_NAME"
        shadow_size .4
		tooltip "ENEMY_FLY_DESC"
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag bug
        faction enemies
        
        corpse_health 0
        movement 4
        health 1
        base_mana_regen 999
        flying true
        type small
        deathpoof_size 1
        can_be_backstabbed false
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Maggot`
**Name:** Maggot  
**Source:** `small_enemies.gon`  

```
Maggot {
    graphics {
        movieclip Maggot
        name "ENEMY_MAGGOT_NAME"
        shadow_size .4
		tooltip "ENEMY_MAGGOT_DESC"
    }

    stats {
        strength 2
        dexterity 1
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        health 1
        corpse_health 0
        movement 2
        faction enemies
        type small
        initiative 1
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        CanMutateTo [TumorousMaggot, ChargeyMaggot, SwappyMaggot]
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Flea`
**Name:** Flea  
**Source:** `small_enemies.gon`  

```
Flea {
    graphics {
        movieclip Flea
        name "ENEMY_FLEA_NAME"
        shadow_size .50

        tooltip "ENEMY_FLEA_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag bug
        health 2
        corpse_health 0
        movement 4
        faction enemies
        type small
        deathpoof_size 1
    }

    abilities {
        move DefaultMove
        attack SuicideMelee
        
        spells [

        ]
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Pinky`
**Name:** Pinky  
**Source:** `small_enemies.gon`  

```
Pinky {
    graphics {
        movieclip Pinky
        name "ENEMY_PINKY_NAME"
        shadow_size .6

        tooltip "ENEMY_PINKY_DESC"
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag rat
        health 1
        movement 2
        faction enemies
        type small
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }
    
    ai {
        brain PatternBrain
        pattern {
            move_then_do attack
        }

        decision_weights simple
        move_weights random
    }
}
```

---

### `MeatMinion`
**Name:** Meat Minion  
**Source:** `small_enemies.gon`  

```
MeatMinion {
    graphics {
        movieclip MeatMinion
        name "ENEMY_MEATMINION_NAME"
        shadow_size .20
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        health 2
        corpse_health 0
        movement 3
        faction enemies
        type small
        deathpoof_size 1
    }

    abilities {
        move DefaultMove
        attack MeatMinionMelee
        
        spells [

        ]
    }

    passives {
        SpawnThingOnDeath Food
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Dip`
**Name:** Dip  
**Source:** `small_enemies.gon`  

```
Dip {
    graphics {
        movieclip Dip
        name "ENEMY_DIP_NAME"
        shadow_size .5
		tooltip "ENEMY_DIP_DESC"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag poop
        health 1
        corpse_health 0
        movement 3
        faction enemies
        type small
        inherit_faction true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {

    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `RattleSnake`
**Name:** Rattlesnek  
**Source:** `small_enemies.gon`  

```
RattleSnake {
    graphics {
        movieclip Snake
        name "ENEMY_RATTLESNEK_NAME"
        piece_alt_frame 3
        scale .80
        shadow_size .60

        tooltip "ENEMY_RATTLESNEK_DESC"
    }

    sound {
        animation_prefix RattleSnake
    }

    stats {
        strength 4
        dexterity 2
        constitution 2
        intelligence 2
        speed 5
        charisma 2
    }
    
    properties {
        tag animal
        type small
        faction enemies
        movement 4
        health 3
        weak_threshold 0
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack RattleSnakeAttack

        spells [
            RattleSnakeTrap
        ]
    }

    passives {
        
        Trapper {
            ability RattleSnakeTrap
            pathfinding_avoidance 250
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights rattle_distance
        consider_spells false
    }
}
```

---

### `TinySpider`
**Name:** Spiderling  
**Source:** `small_enemies.gon`  

```
TinySpider {
    graphics {
        movieclip BabySpider
        name "ENEMY_SPIDERLING_NAME"
        shadow_size .5
        move_speed_multiplier 2
        tooltip "ENEMY_SPIDERLING_DESC"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag bug
        health 2
        corpse_health 0
        movement 4
        faction enemies
        type small
        deathpoof_size 1
    }

    abilities {
        move DefaultMove
        attack SpiderSuicideMelee
        
        spells [

        ]
    }

    passives {
        StatusImmunity Webbed
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Wisp`
**Name:** Wisp  
**Source:** `small_enemies.gon`  

```
Wisp {
    graphics {
        movieclip Wisp
        name "ENEMY_WISP_NAME"
        
        uifloaters_offset 1.5
        tooltip "ENEMY_WISP_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag ghost
        faction enemies
        
        corpse_health 0
        movement 4
        health 1
        base_mana_regen 999
        flying true
        type small
        deathpoof_size 1
        can_be_backstabbed false
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    passives {
        WispDodge 1

        AddStatusToBasicAttack {
            Burn 2
        }

        CharacterLightSource {
            color [.7, .3, 1]
            glow [.7, .3, 1, .5]
            size 1
        }
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `MoonWorm`
**Name:** Moon Worm  
**Source:** `small_enemies.gon`  

```
MoonWorm {
    graphics {
        movieclip MoonWorm
        name "ENEMY_MOONWORM_NAME"
        shadow_size .5
		tooltip "ENEMY_MOONWORM_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag worm
        type small
        health 12
        movement 3
        faction enemies
    }

    abilities {
        move Teleport
        attack MoonWormShot
        
        spells [
            MoonWormCurl
        ]
    }

    passives {
        AbilityReaction MoonWormCurl
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `Invader`
**Name:** Schpidenbot  
**Source:** `small_enemies.gon`  

```
Invader {
    graphics {
        movieclip Invader
        name "ENEMY_INVADER_NAME"
        shadow_size .40
        move_speed_multiplier 2
        scale .8
		tooltip "ENEMY_INVADER_DESC"
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [robot bug]
        health 5
        corpse_health 0
        movement 4
        faction enemies
        type small
        deathpoof_size 1
    }

    abilities {
        move DefaultMove
        attack InvaderAttack
        
        spells [

        ]
    }

    passives {
        Brace 2
        StatusImmunity Webbed
        Robot 1
        DeathRattle InvaderExplode
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights stay_close_always_move
    }
}
```

---

### `TinyTumor`
**Name:** Tiny Tumor  
**Source:** `small_enemies.gon`  

```
TinyTumor {
    graphics {
        movieclip [TinyTumorA TinyTumorB TinyTumorC]
        name "ENEMY_TINYTUMOR_NAME"
        shadow_size .5
		tooltip "ENEMY_TINYTUMOR_DESC"
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag tumor
        faction enemies
        type small

        corpse_health 0
        movement 4
        health 4
        flying true
        
        deathpoof_size 1
    }

    abilities {
        move DefaultMove
        attack CancerMelee
        
        spells [

        ]
    }

    passives {
        Brace 2
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Clot`
**Name:** Clot  
**Source:** `small_enemies.gon`  

```
Clot {
    graphics {
        movieclip Clot
        name "ENEMY_CLOT_NAME"
        shadow_size .5
		scale .7
		tooltip "ENEMY_CLOT_DESC"
    }

    stats {
        strength 2
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies
        inherit_faction true
        type small

        corpse_health 0
        movement 4
        health 1
        
        deathpoof_size 1
    }

    abilities {
        move DefaultMove
        attack None
        
        spells [
            ClotEvolve
            ClotFailEvolve
        ]
    }

    passives {
        
    }
    
    ai {
        brain PatternBrain

        pattern {
            move_then_do_random [ClotEvolve ClotFailEvolve]
        }

        decision_weights default
        move_weights stay_far
    }
}
```

---

### `FrankPinky`
**Name:** Frank's Bean  
**Source:** `small_enemies.gon`  

```
FrankPinky {
    graphics {
        movieclip PinkyX
        name "ENEMY_FRANKSBEAN_NAME"
        shadow_size .6
		scale .7

        tooltip "ENEMY_PINKY_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag tumor
        health 8
        movement 2
        faction enemies
        type small
        dispersed_bonus_turns 2
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }
    
    passives {
        Brace 5
    }

    ai {
        brain PatternBrain
        pattern {
            move_then_do attack
        }

        decision_weights simple
        move_weights random
    }
}
```

---

### `Lice`
**Name:** Louse  
**Source:** `small_enemies.gon`  

```
Lice {
    graphics {
        movieclip Flea
        name "ENEMY_LOUSE_NAME"
        shadow_size .50
		scale .5
		no_splatter true
        tooltip "ENEMY_LOUSE_DESC"
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag bug
        health 1
        corpse_health 0
        movement 3
        faction enemies
        type small
        deathpoof_size 1
    }

    abilities {
        move DefaultMove
        attack LiceBite
        
        spells [

        ]
    }
    
    ai {
        brain GenericBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

### `Terminator1`
**Name:** C-800  
**Source:** `terminator.gon`  

```
Terminator1 {
    graphics {
        movieclip _CAT
        name "ENEMY_TERMINATOR1_NAME"
        custom_cat_data TerminatorCat
        scale 1.2
        shadow_size 1.2
        move_speed_multiplier .66

        uifloaters_offset 1.4

        tooltip "ENEMY_TERMINATOR1_DESC"

        alt_animations[[idle catbotIdle] [walk stompwalk]]
    }

    sound {
        alt_sounds [
            [SE_Cat_StompWalk SE_Terminator1_WalkStep]
            [SE_Cat_StompLegMove SE_Terminator1_WalkLeg]
            [SE_Cat_equipWeapon SE_TerminatorSwapWeapon]
            [SE_Cat_WeaponRaise SE_Terminator_WeaponRaise]
            [SE_Cat_WeaponLower SE_Terminator_WeaponLower]
            [SE_CatSwishThrow SE_ThrowGrenade]
            [SE_Cat_bearHug SE_Terminator_bearHug]
        ]
    }

    stats {
        strength 10
        dexterity 8
        constitution 10
        intelligence 6
        speed 6
        charisma 4
        luck 7
    }

    equipment {
        face TerminatorCoolGlasses
    }
    
    properties {
        tag [cat robot]
        type boss
        health 250
        base_mana_regen 999
        faction enemies

        initiative 999
        
        evenly_dispersed_bonus_turns 2
        first_turn_is_main_turn true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [
            T1Pummel
            T1SwapWeapon
            T1ThrowGrenadeA
            T1ThrowGrenadeB

            MoveOne
            T1ChokeReaction
        ]
    }

    passives {
        Robot 1
        Brace 50
        Trample 3
        AggroTargetIsCurrentTurn 1
        StatusOnTookDamage {
            RemoveStatusStacks {
                status Brace
                stacks 1
            }
        }
        TerminatorChase {
            move MoveOne
            ability T1ChokeReaction
        }
        PrioritizePlayerCats 1

        TerminatorSkin {
            status Brace

            groups [
                {
                    stacks 48
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        head 1057
                    }
                }
                {
                    stacks 46
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        ear1 1038
                    }
                }
                {
                    stacks 44
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        leg1 1061
                    } 
                }
                {
                    stacks 42
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        body 1057
                    }
                }
                {
                    stacks 40
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        tail 1058
                    }
                }
                {
                    stacks 38
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        eye2 1071
                    }
                }
                {
                    stacks 36
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        head 1058
                    }
                }
                {
                    stacks 32
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        arm2 1061

                    }
                }
                {
                    stacks 28
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        head 1059
                        body 1057
                        tail 1058
                        leg1 1062
                        leg2 1060
                        arm1 1060
                        arm2 1061
                        ear1 1038
                        mouth 1000
                    }
                }
                {
                    stacks 24
                    ParticleBurst Gibs_terminatorskin
                    TransformEquipment {
                        from TerminatorCoolGlasses 
                        to TerminatorCoolGlasses2
                    }
                    CatPartsTransform {
                        head 1059
                        body 1057
                        tail 1058
                        leg1 1061
                        leg2 1060
                        arm1 1061
                        arm2 1061
                        ear1 1038
                        mouth 1000
                    }
                }
                {
                    stacks 20
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        head 1059
                        body 1058
                        tail 1059
                        leg1 1061
                        leg2 1062
                        arm1 1061
                        arm2 1062
                        ear2 1037
                        ear1 1038
                    }
                }
                {
                    stacks 16
                    ParticleBurst Gibs_terminatorskin
                    DestroyFaceArmor 1
                    CatPartsTransform {
                        head 1059
                        body 1058
                        tail 1059
                        leg1 1061
                        leg2 1062
                        arm1 1061
                        arm2 1062
                        eye1 1071
                    }
                }
                {
                    stacks 12
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        head 1060
                        body 1058
                        tail 1059
                        leg1 1061
                        leg2 1062
                        arm1 1061
                        arm2 1062
                    }
                }
                {
                    stacks 8
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        head 1061
                        body 1058
                        tail 1059
                        leg1 1061
                        leg2 1062
                        arm1 1061
                        arm2 1062
                        mouth 1072
                    }
                }
                {
                    stacks 4
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        head 1062
                        body 1058
                        tail 1059
                        leg1 1061
                        leg2 1062
                        arm1 1062
                        arm2 1062
                        mouth 1072
                    }
                }
                {
                    stacks 0
                    ParticleBurst Gibs_terminatorskin
                    CatPartsTransform {
                        head 1062
                        body 1059
                        tail 1059
                        leg1 1062
                        leg2 1062
                        arm1 1062
                        arm2 1062
                        mouth 1072
                    }
                }
            ]

        }
    }
    
    ai {
        brain PatternBrain

        virtual_abilities {
            MoveSpaced {
                ability move
                move_weights terminator_keep_distance_always_move
            }
        }

        pattern {
            do_all [*weapon *T1ThrowGrenadeA *T1ThrowGrenadeB MoveSpaced T1SwapWeapon]
        }
        bonusturn_pattern {
            do_all [*T1Pummel *weapon MoveSpaced T1SwapWeapon]
        }

        decision_weights terminator
        move_weights terminator_stay_close
    }
}
```

---

### `Terminator2`
**Name:** C-1000  
**Source:** `terminator.gon`  

```
Terminator2 {
    graphics {
        movieclip _CAT
        name "ENEMY_TERMINATOR2_NAME"
        custom_cat_data Terminator2Cat
        scale 1.2
        shadow_size 1.2

        uifloaters_offset 1.4
		tooltip "ENEMY_TERMINATOR2_DESC"

        alt_animations[[dying liquidmetalDying] [dodge liquidmetaldodge]]
        no_splatter true
    }

    sound {
        alt_sounds [
            [SE_CatWalk SE_Terminator2_WalkStep]
            [SE_Cat_StompLegMove SE_Terminator2_WalkLeg]
            [SE_Cat_ShadowStepOut SE_Terminator_ShadowStepOut]
            [SE_Cat_ShadowStepIn SE_Terminator_ShadowStepIn]
        ]
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
   
    
    properties {
        tag [cat robot]
        type boss
        health 500
        faction enemies
        allow_passive_spelltransforming true
        evenly_dispersed_bonus_turns 3
        last_turn_is_main_turn true

        movement 1
        corpse_health 0
        allow_replacebrain false
    }

    abilities {
        move DefaultMove
        attack T2SpearMelee
        
        spells [
            DoNothing 
            DoNothing
            DoNothing
            DoNothing
            DoNothing

            T2Clone
            T2UnClone
            T2GoopRun
        ]
    }

    passives {
        Robot 1
        PrioritizePlayerCats 1
        AggroTargetIsCurrentTurn 1

        FormChanger {
            Default {
                ai {
                    brain PatternBrain
                    end_turn_on_formswitch true

                    pattern {
                        do_all [*T2Clone *attack move]
                    }

                    decision_weights terminator
                    move_weights stay_close
                }

                passives {
                    DodgeChance_Status 100

                    Terminator2Chase move

                    StatusOnEndMove {
                        RemoveStatusStacks {
                            status DodgeChance_Status
                            stacks 10
                        }
                        SpeedUp_WithoutInitiative 1
                    }
                    Terminator2Run {
                        move_ability T2GoopRun
                        move_weights stay_far_always_move
                    }
                }
            }
            Transformed {
                ai {
                    brain PatternBrain
                    end_turn_on_formswitch true

                    pattern {
                        do_best_multiple [attack spell0 spell1 spell2 spell3 spell4 weapon trinket]
                    }

                    decision_weights terminator
                    move_weights keep_distance_always_move
                }

                passives {
                    StatusEachTurnEndIfEnabledAtStartOfTurn {
                        ForceUseAbility T2UnClone
                    }
                }
            }
        }
        FormChangeWhileHasStatus {
            status T2CopyCatInternal
            form_has Transformed
            form_hasnot Default
        }
    }
    
    ai {
        brain NoBrain 
        decision_weights default
        move_weights stay_close
    }
}
```

---

### `TankCat_Terminator`
**Name:** Robo-Maisie  
**Source:** `terminator.gon`  

```
TankCat_Terminator {
    graphics {
        movieclip _CAT
        name "ENEMY_TERMINATOR3_TANK_NAME"
        custom_cat_data TankCat_Terminator 
        spawnin_animation beaminTank

        tooltip "ENEMY_TERMINATOR3_TANK_DESC"
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkA]]
    }

    equipment {
        face MetalPlate_Terminator
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0

        faction enemies
        type boss
        movement 5
        dispersed_bonus_turns 1
        dispersed_bonus_turns_consider_initiative false
    }

    abilities {
        move DefaultMove
        attack BasicTankMelee
        
        spells [
            SwapPositions_TankCat
            T3LickyLicky
        ]
    }

    passives {
        ProtectTargetedAllies {
            ability SwapPositions_TankCat
            target_filter any
        }

        MamaCatAnimations 1

        Robot 1

        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }

    ai {
        brain PatternBrain

        pattern {
            do_priority [T3LickyLicky attack]
        }

        decision_weights default_no_revive
        move_weights keep_distance_always_move
    }
}
```

---

### `MageCat_Terminator`
**Name:** Robo-Lucy  
**Source:** `terminator.gon`  

```
MageCat_Terminator {
    variant_of MageCat
    graphics {
        name "ENEMY_TERMINATOR3_MAGE_NAME"
        custom_cat_data MageCat_Terminator 
        spawnin_animation beaminMage
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkB]]
    }

    equipment {
        neck MageCollar_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `HunterCat_Terminator`
**Name:** Robo-Fenrir  
**Source:** `terminator.gon`  

```
HunterCat_Terminator {
    graphics {
        movieclip _CAT
        name "ENEMY_TERMINATOR3_HUNTER_NAME"
        custom_cat_data HunterCat_Terminator 
        spawnin_animation beaminHunter

        tooltip "ENEMY_TERMINATOR3_HUNTER_DESC"
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkC]]
    }

    equipment {
        face HuntersPatch_Terminator
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25

        faction enemies
        type boss
        dispersed_bonus_turns 1
        corpse_health 0
    }

    abilities {
        move HunterMinibossMove
        attack BasicRanged_Hunter
        
        spells [
            BearTrap_Enemy_Cantrip
            Shove
        ]
    }

    passives {
        CounterAttack Shove
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }

    ai {
        brain PatternBrain

        pattern {
            do BearTrap_Enemy_Cantrip
            do_all [BearTrap_Enemy_Cantrip attack]
        }

        decision_weights default
        move_weights prefer_tall_grass_always_move
    }
}
```

---

### `ThiefCat_Terminator`
**Name:** Robo-Dack  
**Source:** `terminator.gon`  

```
ThiefCat_Terminator {
    variant_of ThiefCat
    graphics {
        name "ENEMY_TERMINATOR3_THIEF_NAME"
        custom_cat_data ThiefCat_Terminator 
        spawnin_animation beaminThief
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkD]]
    }

    equipment {
        head CoinBag_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0
        dispersed_bonus_turns 1
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `MedicCat_Terminator`
**Name:** Robo-Marshmallow  
**Source:** `terminator.gon`  

```
MedicCat_Terminator {
    variant_of MedicCat
    graphics {
        name "ENEMY_TERMINATOR3_CLERIC_NAME"
        custom_cat_data MedicCat_Terminator 
        spawnin_animation beaminMedic
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkE]]
    }

    equipment {
        neck AngelicAura_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        divine_shield 0
        corpse_health 0
        dispersed_bonus_turns 1
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `FighterCat_Terminator`
**Name:** Robo-Magnus  
**Source:** `terminator.gon`  

```
FighterCat_Terminator {
    variant_of FighterCat
    graphics {
        name "ENEMY_TERMINATOR3_FIGHTER_NAME"
        custom_cat_data FighterCat_Terminator 
        spawnin_animation beaminFighter
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkF]]
    }

    equipment {
        neck SamsonsChains_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `Pebbles_Terminator`
**Name:** Robo-Pebbles  
**Source:** `terminator.gon`  

```
Pebbles_Terminator {
    graphics {
        movieclip _CAT
        name "ENEMY_TERMINATOR3_PEBBLES_NAME"
        custom_cat_data Pebbles_Terminator
        spawnin_animation beamin
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkA]]
    }

    equipment {
        head Pebble_Terminator
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma  5
        luck 5
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini

        faction enemies
        type boss
        dispersed_bonus_turns 1
        dispersed_bonus_turns_consider_initiative false
        movement 4

        health 25
        shield 25
        corpse_health 0
    }

    abilities {
        move DefaultMove
        attack ColorlessCat_Push
        
        spells [
            RockToss_ColorlessCat
            RockToss_ColorlessCat_AsCloseAsPossible
            T3Pebbles_BoulderDrop
            T3Pebbles_PrimeBoulderDrop
        ]
    }

    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup

        UseAbilityWhenShieldDepleted T3Pebbles_PrimeBoulderDrop
    }

    ai {
        brain PatternBrain

        pattern {
            do_priority [attack, RockToss_ColorlessCat]
            do_priority [RockToss_ColorlessCat, attack]
        }

        fallback {
            do RockToss_ColorlessCat_AsCloseAsPossible
        }

        decision_weights default
        move_weights keep_distance_always_move
    }
}
```

---

### `NecroCat_Terminator`
**Name:** Robo-Morana  
**Source:** `terminator.gon`  

```
NecroCat_Terminator {
    variant_of NecroCat
    graphics {
        name "ENEMY_TERMINATOR3_NECRO_NAME"
        custom_cat_data NecroCat_Terminator
        spawnin_animation beaminNecro
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkB]]
    }

    equipment {
        face NecromancerMask_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0
        dispersed_bonus_turns 0 
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `TinkererCat_Terminator`
**Name:** Robo-Franklin  
**Source:** `terminator.gon`  

```
TinkererCat_Terminator {
    variant_of TinkererCat
    graphics {
        name "ENEMY_TERMINATOR3_TINKERER_NAME"
        custom_cat_data TinkererCat_Terminator
        spawnin_animation beaminTinkerer
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkC]]
    }

    equipment {
        head TinkererHat_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `ButcherCat_Terminator`
**Name:** Robo-Gein  
**Source:** `terminator.gon`  

```
ButcherCat_Terminator {
    variant_of ButcherCat
    graphics {
        name "ENEMY_TERMINATOR3_BUTCHER_NAME"
        custom_cat_data ButcherCat_Terminator
        spawnin_animation beaminButcher
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkD]]
    }

    equipment {
        face ButcherMask_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `PsychicCat_Terminator`
**Name:** Robo-Alice  
**Source:** `terminator.gon`  

```
PsychicCat_Terminator {
    variant_of PsychicCat
    graphics {
        name "ENEMY_TERMINATOR3_PSYCHIC_NAME"
        custom_cat_data PsychicCat_Terminator
        spawnin_animation beaminPsychic
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkE]]
    }

    equipment {
        face PsychicMask_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `DruidCat_Terminator`
**Name:** Robo-Draven  
**Source:** `terminator.gon`  

```
DruidCat_Terminator {
    graphics {
        movieclip _CAT
        name "ENEMY_TERMINATOR3_DRUID_NAME"
        custom_cat_data DruidCat_Terminator
        spawnin_animation beaminDruid
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkF]]
    }

    equipment {
        neck DruidNeck_Terminator
    }

    stats {
        strength 3
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }

    abilities {
        move DefaultMove
        attack DruidCatBasic
        
        spells [
            DCSquirrelForm
            DCBirthSquirrel
            DCT_SummonCrow
        ]
    }

    properties {
        tags [cat robot]
        hidden_tags [terminator_mini dc_cat]
        faction enemies
        type boss
        dispersed_bonus_turns 1
        health 25
        shield 25
        corpse_health 0
    }
    passives {
        FormChanger {
            Default {
            }
            SquirrelForm {
                attack BasicMelee
                passives {
                    SpeedUp 6
                    AddTemporaryEffectsToBasicAttack {
                        Fury 75
                    }

                }
                ai {
                    brain PatternBrain

                    pattern {
                        do_all [*DCBirthSquirrel attack DCBirthSquirrel]
                    }

                    decision_weights default
                    move_weights keep_distance
                }
            }
        }

        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
    ai {
        brain PatternBrain

        pattern {
            do_all [*DCT_SummonCrow DCSquirrelForm attack]
        }

        decision_weights default
        move_weights keep_distance
    }
}
```

---

### `DruidCrow_Terminator`
**Name:** Robo-Draven's Crow  
**Source:** `terminator.gon`  

```
DruidCrow_Terminator {
    variant_of DruidCrow

    graphics {
        name "ENEMY_TERMINATOR3_DRUIDCROW_NAME"
    }
}
```

---

### `MonkCat_Terminator`
**Name:** Robo-Chan Hung  
**Source:** `terminator.gon`  

```
MonkCat_Terminator {
    variant_of MonkCat
    graphics {
        name "ENEMY_TERMINATOR3_MONK_NAME"
        custom_cat_data MonkCat_Terminator
        spawnin_animation beaminMonk
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkF]]
    }

    equipment {
        head MonkMask_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `JesterCat_Terminator`
**Name:** Robo-Arthur  
**Source:** `terminator.gon`  

```
JesterCat_Terminator {
    variant_of JesterCat
    graphics {
        name "ENEMY_TERMINATOR3_JESTER_NAME"
        custom_cat_data JesterCat_Terminator
        spawnin_animation beaminJester
    }
    sound {
        alt_sounds [[SE_CatWalk SE_TerminatorCatWalkA]]
    }

    equipment {
        head JesterHat_Terminator
    }

    properties {
        tags [cat robot]
        hidden_tags terminator_mini
        health 25
        shield 25
        corpse_health 0
        dispersed_bonus_turns 1
    }
    passives {
        Robot 1
        SpawnOnDeath Antidote
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
        SpawnOnDeath RandomArmorPickup
    }
}
```

---

### `T3Hitler`
**Name:** Hitler  
**Source:** `terminator.gon`  

```
T3Hitler {
    graphics {
        movieclip HitlerMech
        name "ENEMY_TERMINATOR3_HITLER_NAME"
        tooltip ENEMY_TERMINATOR3_HITLER_DESC
        uifloaters_offset 2.5
    }

    stats {
        strength  2
        dexterity 7
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag [humanoid robot]
        faction enemies
        type boss
        movement 4
        corpse_health 0
        takes_turns false
        flying true

        health 100
        shield 100

        banned_elite_buffs [Mad Twin]
    }

    abilities {
        move DoNothing
        attack DoNothing

        spells [
            T3RipAndTear
            T3Counter

            T3Spawn_Tank
            T3Spawn_Mage
            T3Spawn_Hunter
            T3Spawn_Thief
            T3Spawn_Medic
            T3Spawn_Fighter
            T3Spawn_Colorless
            T3Spawn_Necromancer
            T3Spawn_Tinkerer
            T3Spawn_Butcher
            T3Spawn_Psychic
            T3Spawn_Druid
            T3Spawn_Monk
            T3Spawn_Jester

            T3Intro
            T3JoinFight

            HitlerPulp1
            HitlerPulp2
            HitlerPulp3
            HitlerPulp4
            HitlerPulp5
            HitlerPulp6
        ]
    }

    passives {
        Robot 1

        FormChanger {
            InitialPhase {
                move FloatMove
                attack T3Shoot

                turns {
                    takes_turns true
                    takes_main_turn false
                    round_start_bonus_turns 1
                }

                ai {
                    brain PatternBrain
                    pattern {
                        do *T3Intro
                    }
                    decision_weights default
                    move_weights keep_distance
                }

                passives {
                    AddInitiative 999999
                    DebuffImmunity 1
                    DeathRattleRevive {
                        ability HitlerPulp1
                        even_if_stunned true
                    }
                }
            }
            SpawningPhase {
                turns {
                    takes_turns false
                }
                passives {
                    FullBlockEverything 1
        
                    T3HitlerSpawningPhase {
                        spell_use_groups [
                            [
                                T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk 
                                T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk T3Spawn_Monk 
                                T3Spawn_Tank
                                T3Spawn_Mage
                                T3Spawn_Hunter
                                T3Spawn_Thief
                                T3Spawn_Medic
                                T3Spawn_Fighter
                                T3Spawn_Necromancer
                                T3Spawn_Tinkerer
                                T3Spawn_Butcher
                                T3Spawn_Psychic
                                T3Spawn_Druid
                                T3Spawn_Jester
                            ]
                            [                    
                                T3Spawn_Colorless
                            ]
                            [                    
                                T3JoinFight
                            ]
                        ]
                    }

                    FormChangeOffMap {
                        form_offmap SpawningPhase
                        form_onmap FightPhase
                    }
                }
            }
            FightPhase {
                move FloatMove
                attack T3Shoot

                turns {
                    takes_turns true
                    dispersed_bonus_turns 1
                }
                passives {
                    PrioritizeFarAwayTargets 10
                    DeathRattleRevive {
                        ability HitlerPulp1
                        even_if_stunned true
                    }
                    CounterAttack T3Counter
                }

                ai {
                    brain PatternBrain

                    pattern {
                        do_all [*T3RipAndTear *attack attack move]
                    }

                    decision_weights default
                    move_weights keep_distance_always_move
                }
            }
            Pulp2 {
                animation_suffix 2
                uifloaters_offset 1
                attack None
                move None
                tooltip ENEMY_TERMINATOR3_HITLERHEAD_DESC

                turns {
                    takes_turns false
                }

                passives {
                    OverrideMaxHealth 25
                    BackstabImmunity 1
                    MinimumKnockbackFromAllDamage 1
                    DeathRattleRevive {
                        ability HitlerPulp2
                        even_if_stunned true
                    }
                }
            }
            Pulp3 {
                animation_suffix 3
                uifloaters_offset 1
                attack None
                move None
                tooltip ENEMY_TERMINATOR3_HITLERHEAD_DESC

                turns {
                    takes_turns false
                }

                passives {
                    OverrideMaxHealth 25
                    BackstabImmunity 1
                    MinimumKnockbackFromAllDamage 1
                    DeathRattleRevive {
                        ability HitlerPulp3
                        even_if_stunned true
                    }
                }
            }
            Pulp4 {
                animation_suffix 4
                uifloaters_offset 1
                attack None
                move None
                tooltip ENEMY_TERMINATOR3_HITLERHEAD_DESC

                turns {
                    takes_turns false
                }

                passives {
                    OverrideMaxHealth 25
                    BackstabImmunity 1
                    MinimumKnockbackFromAllDamage 1
                    DeathRattleRevive {
                        ability HitlerPulp4
                        even_if_stunned true
                    }
                }
            }
            Pulp5 {
                animation_suffix 5
                uifloaters_offset 1
                attack None
                move None
                tooltip ENEMY_TERMINATOR3_HITLERHEAD_DESC

                turns {
                    takes_turns false
                }

                passives {
                    OverrideMaxHealth 25
                    BackstabImmunity 1
                    MinimumKnockbackFromAllDamage 1
                    DeathRattleRevive {
                        ability HitlerPulp5
                        even_if_stunned true
                    }
                }
            }
            Pulp6 {
                animation_suffix 6
                uifloaters_offset 1
                attack None
                move None
                tooltip ENEMY_TERMINATOR3_HITLERHEAD_DESC

                turns {
                    takes_turns false
                }

                passives {
                    OverrideMaxHealth 25
                    BackstabImmunity 1
                    MinimumKnockbackFromAllDamage 1
                    DeathRattleRevive {
                        ability HitlerPulp6
                        even_if_stunned true
                    }
                }
            }
            Pulp7 {
                animation_suffix 7
                uifloaters_offset 1
                attack None
                move None
                tooltip ENEMY_TERMINATOR3_HITLERHEAD_DESC

                turns {
                    takes_turns false
                }

                passives {
                    OverrideMaxHealth 1
                    BackstabImmunity 1
                }
            }
        }
    }
    
    ai {
        brain PatternBrain

        pattern {
            do none
        }

        decision_weights default_t3hitler
        move_weights keep_distance
    }
}
```

---

### `SpearGuy`
**Name:** Spear Test Guy  
**Source:** `test_enemies.gon`  

```
SpearGuy {
    graphics {
        movieclip SpearTestGuy
        name "Spear Test Guy"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        health 30
        faction enemies
        exclude_from_hallucinate true
    }

    abilities {
        move DefaultMove
        attack SpearPokeTest
        can_get_bonus true
        
        spells [

        ]
    }

    passives {

    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `Dummy`
**Name:** Dummy Cat  
**Source:** `test_enemies.gon`  

```
Dummy {
    graphics {
        movieclip _CAT
        name "Dummy Cat"
    }

    properties {
        tag cat
        type cat
        health 100
        base_mana_regen 999
        faction enemies
        exclude_from_hallucinate true
    }

    abilities {
        move DefaultMove
        attack BasicMelee
        
        spells [

        ]
    }

    ai {
        brain NoBrain
    }
}
```

---

### `Test2x2`
**Name:** Test 2x2  
**Source:** `test_enemies.gon`  

```
Test2x2 {
    graphics {
        movieclip test2x2
        name "Test 2x2"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        health 30
        faction enemies
        exclude_from_hallucinate true
    }

    abilities {
        move DefaultMove
        attack SpearPokeTest
        can_get_bonus true
        
        spells [

        ]
    }

    passives {

    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `ThrobbingKing`
**Name:** Throbbing King  
**Source:** `throbbing_king.gon`  

```
ThrobbingKing {
    graphics {
        movieclip ThrobbingKing
        name "ENEMY_THROBBINGKING_NAME"
        shadow_size 2
        uifloaters_offset 2.5
        water_mask big
        move_speed_sync_frames 28
		tooltip "ENEMY_THROBBINGKING_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        movement 3
        mana_regen 999
        mana 100
        corpse_health 0
        
        health 460

        size 2x2
        move_block everything_even_when_dead

        dispersed_bonus_turns 2
        round_end_bonus_turns 1
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack TKNG_GutBall
        
        spells [
            TKNG_Trash
            TKNG_Spread
            TKNG_Kneel
            TKNG_Roulette
            TKNG_GoAway
            TKNG_DeathExplode
        ]
    }

    passives {
        FormChanger {
            NotPriming {
                turns {
                    takes_main_turn true
                    dispersed_bonus_turns 2
                    round_end_bonus_turns 1
                    wait_till_next_round_to_update_turns true
                }
            }
            Priming {
                turns {
                    takes_main_turn false
                    round_end_bonus_turns 1
                    wait_till_next_round_to_update_turns true
                }

                passives {
                    StunImmunity 1
                }
            }
        }

        FormChangeWhilePrimingAbility {
            priming Priming
            not_priming NotPriming
        }

        Trample 3
        TransformOnDeath ThrobbingKing2
        DeathRattle TKNG_DeathExplode
    }
    
    ai {
        brain PatternBrain
        decision_weights default
        move_weights keep_distance_always_move
        stun_advances_pattern true
        auto_orient false
        
        mainturn_pattern {
            do *TKNG_Trash
        }

        dispersed_bonusturn_pattern {
            do attack
        }
        
        round_end_bonusturn_pattern {
            do_random [TKNG_Spread TKNG_Kneel TKNG_Roulette TKNG_GoAway]
        }
    }
}
```

---

### `ThrobbingKing2`
**Name:** Throbbing King  
**Source:** `throbbing_king.gon`  

```
ThrobbingKing2 {
    graphics {
        movieclip ThrobbingKing2
        name "ENEMY_THROBBINGKING_NAME"
        uifloaters_offset 1.75
        water_mask medmed
		tooltip "ENEMY_THROBBINGKING2_DESC"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
    }
    
    properties {
        tag blob
        faction enemies
        type boss
        movement 5
        mana_regen 999
        mana 100
        dispersed_bonus_turns 2
        corpse_health indestructible
        
        health 150
        banned_elite_buffs [Twin]
    }

    abilities {
        move DefaultMove
        attack TKNG_Laser
        
        spells [
            TKNG_Spawn
            TKNG_Hop
        ]
    }

    passives {
        MoveWhenDamaged TKNG_Hop
    }
    
    ai {
        brain PatternBrain

        pattern {
            do attack
            do TKNG_Spawn
        }

        decision_weights default
        move_weights keep_distance_always_move
        auto_orient false
    }
}
```

---

### `SeducedBoulder`
**Name:** Seduced Boulder  
**Source:** `world_event_specials.gon`  

```
SeducedBoulder {
    graphics {
        movieclip Rock
        name "ENEMY_SEDUCEDBOULDER_NAME"
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 0
        speed 5
        charisma 5
    }

    properties {
        faction allies
        takes_turns true
        corpse_health 0
        can_be_backstabbed false
        movement 4
        health 15
        
        elements [
            Rock
        ]
    }

    abilities {
        move DefaultMove
        attack None
        can_get_bonus true
        
        spells [
            Taunt
        ]
    }
    
    ai {
        brain PlayerBrain
    }
}
```

---

### `EventBountyHunter`
**Name:** Bounty Hunter  
**Source:** `world_event_specials.gon`  

```
EventBountyHunter { 
    graphics {
        movieclip _CAT
        name "ENEMY_EVENTBOUNTYHUNTER_NAME"
        tooltip ENEMY_BOUNTYHUNTER_DESC
        custom_cat_data GunCat
    }
    
    equipment {
        weapon GunslingerPistol
        face MuggerMask
    }

    stats {
        strength 4
        dexterity 5
        constitution 5
        intelligence 5
        speed 2
        charisma 5
        luck 5
    }
    
    properties {
        tag cat
        type cat
        health 17
        faction birds 
        base_mana_regen 999
        movement 2
        kill_required false

        can_collect_coins true
        held_coins [5 10]

        aggro_target_is_enemy true
        can_run false
    }

    abilities {
        move DefaultMove
        attack GuncatShoot
        
        spells [

        ]
    }

    passives {
        WeaponsDontLoseDurability 1
        EventBounterHunterPassive 1
    }
    
    ai {
        brain GenericBrain
        decision_weights default
        move_weights keep_distance_always_move
        consider_spells false
    }
}
```

---

### `DeadPinky`
**Source:** `world_event_specials.gon`  

```
DeadPinky { 
    variant_of Pinky
    graphics {
        tooltip "ENEMY_DEADPINKY_DESC"
    }
    passives {
        StartDead 100%
    }
}
```

---

### `FastFetus`
**Source:** `world_event_specials.gon`  

```
FastFetus { 
    variant_of Fetus

    passives {
        AlphaTurns 1
    }
}
```

---

### `FastRat`
**Source:** `world_event_specials.gon`  

```
FastRat { 
    variant_of Rat

    passives {
        AlphaTurns 1
    }
}
```

---

### `AlienEgg`
**Name:** Strange Egg  
**Source:** `world_event_specials.gon`  

```
AlienEgg {
    graphics {
        movieclip AlienEgg
        name "ENEMY_STRANGEEGG_NAME"
        tooltip ENEMY_STRANGEEGG_DESC
    }

    stats {
        strength 5
        dexterity 5
        constitution 5
        intelligence 5
        speed 5
        charisma 5
        luck 5
    }
    
    properties {
        tag alien
        faction enemies
        inherit_faction true
        kill_required false

        movement 0
        health 1
        corpse_health 0
        can_be_overkilled false
    }

    abilities {
        move None
        attack None

        spells [
            
        ]
    }

    passives {
        TransformInXTurns {
            turns [1 4]
            object [
                YellowBlaster GreyAlien GreenProber 
                Amoeba MoonWorm Waggle 
                KirbyFetus BrainDrain Fetus FetusGusher 
            ]
            animation hatch
        }
    }
    
    ai {
        brain NoBrain
        decision_weights simple
        move_weights stay_close
    }
}
```

---

