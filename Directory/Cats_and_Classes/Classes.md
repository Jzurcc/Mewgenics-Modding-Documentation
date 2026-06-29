# Cats and Classes/Classes Directory

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
    <td><a href="../Statuses_and_Injuries/Injuries.md">Injuries</a> • <a href="../Statuses_and_Injuries/Status_Effect_Keywords.md">Status Effect Keywords</a></td>
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

## File: `advanced_classes.gon`

### `Monk`
**Name:** Monk  
**Source:** `advanced_classes.gon`  

**Localization Strings:**
- `CAT_CLASS_MONK_DESC`: "A versatile combat master! Monks can switch between ranged and melee stances and attack twice per turn!"

```
Monk {
    meta {
        name "CAT_CLASS_MONK_NAME"
        description "CAT_CLASS_MONK_DESC"
    }

    graphics {
        palette 66

        alt_animations [
            [idle, MonkIdle]
            [ClassToNeutral,   MonkToNeutral]
            [ClassFromNeutral, MonkFromNeutral]
            [StartTurn, MonkStartTurn]
            [Victory, monkVictory]
        ]

        portrait_face monk_portrait
    }

    innate_items {
        weapon MonkFist
        trinket MonkStyleChanger
    }
    innate_passives {
        MonkStances [BasicMonkMelee BasicMonkRanged]
    }

    attack_pool [
        BasicMonkMelee
    ]

    ability_pool [
        Propell
        Hadouken
        Cartwheel
        StoneFists
        Transcend

        HipToss
        Bruise
        Slapback
        Finisher
        Reverberate

        ComboThrow
        ComboPull
        OneWithTheWind
        Pogo
        TrainArms

        Porcupine
        Anneal
        DeepDive
        HopAndBlock
        TrainMind

        Meditate
        DoomPunch
        KiBurst
        DragonPunch
        TrainLegs

        ReallyFastRun
        DetectWeakness
        HundredHandSlap
        KineticCharge
        AirBurst

        TrainBody
        ReleaseEnergy
        Pummel
        QuickAttack
        PerfectForm

        WarmupStretch
        FlyingFist
        SpiritBomb
        OnePunch
        UnbridledHits

        Kamehameha
        SideStep
        UnimpededLunge
        DoubleDragon
        FistOfFate

        Nirvana
        EmptyMind
        Position
        ChargeFists
        Apprentice
    ]

    starter_abilities [
        Propell
        Pogo
        ComboThrow
        ComboPull
        Bruise
        Anneal
        Hadouken
        ReallyFastRun
		Finisher
		UnbridledHits
    ]

    ability_groups {
        attack [
            Propell
            Hadouken
            HipToss
            Slapback
            Finisher
            ComboThrow
            ComboPull
            DoomPunch
            DragonPunch
            HundredHandSlap
            ReleaseEnergy
            Pummel
            FlyingFist
            SpiritBomb
            OnePunch
            UnbridledHits
            Kamehameha
            UnimpededLunge
        ]
        defense [
            Transcend
            Reverberate
            Porcupine
            Anneal
            DeepDive
            Meditate
            KiBurst
            KineticCharge
            TrainBody
            PerfectForm
            Nirvana
        ]
        move [
            Cartwheel
            OneWithTheWind
            Pogo
            HopAndBlock
            TrainLegs
            ReallyFastRun
            QuickAttack
            SideStep
            FistOfFate
            Position
        ]
        misc [
            StoneFists
            Bruise
            TrainArms
            TrainMind
            DetectWeakness
            AirBurst
            WarmupStretch
            DoubleDragon
            EmptyMind
            ChargeFists
            Apprentice
        ]
    }
    
    passive_pool [
        SafeSwitching
        Mixup
        Turnabout
        MonkeyStyle
        BrickSkin

        JaggedEdges
        MindBreaker
        CobraStyle
        Tenderize
        LongArms

        SpreadThePain
        Harden
        IronSkin
        JetFists
        EnergyFists

        Unstoppable
        UnburdenedMotion
        UnburdenedStrikes
        UnburdenedThoughts
        RunningJab

        PerfectTechnique
        RapidFlow
        CounterBarrage
        FlowState
        DancingLights
    ]

    stat_mods {
        int 2
        cha 2
        str -1
        dex -1
    }

    levelup_stats [int str lck]
}
```

---

### `Butcher`
**Name:** Butcher  
**Source:** `advanced_classes.gon`  

**Localization Strings:**
- `CAT_CLASS_BUTCHER_DESC`: "Meat Meat Meat Meat Meat! Butchers are great at cleaving chunks of meat off of things and have a hook to pull stuff towards them!"

```
Butcher {
    meta {
        name "CAT_CLASS_BUTCHER_NAME"
        description "CAT_CLASS_BUTCHER_DESC"
    }

    graphics {
         palette 64

        alt_animations [
            [idle, ButcherIdle]
            [ClassToNeutral,   ButcherToNeutral]
            [ClassFromNeutral, ButcherFromNeutral]
            [StartTurn, ButcherStartTurn]
            [Victory, butcherVictory]
        ]

        portrait_face butcher_portrait
    }

    innate_items {
        weapon ButcherHook
    }

    attack_pool [
        BasicButcherMelee
    ]

    ability_pool [
        HogRush
        Burp
        SelfMutilate
        ForceFeed
        Fartoom

        Mutilate
        SkullBash
        Shred
        Chomp
        Succ

        Trudge
        BodySlam
        Consume
        BloodMagic
        SmellBlood

        Vurp
        SliceAndDice
        LunchTime
        Tromp
        LightenTheLoad

        Crushinator
        CannonBall
        Monch
        DeathWind
        Spoil

        Grill
        Roast
        BadGas
        ButcherPurge
        Binge

        MyTurn
        Gib
        Swallow
        Track
        Sharpen

        FireFart
        RoughToss
        TaintedOffering
        DeliciousScent
        Cough

        Reflux
        Tryptophan
        HookBind
        Regurge
        Grapnel

        Rehook
        Contaminate
        LodgeHook
        Butcher
        Chonkwalk
    ]

    starter_abilities [
        Succ
        HogRush
        Chomp
        BodySlam
        Vurp
        Tromp
        Spoil
        Grill
		Sharpen
		SliceAndDice
    ]

    ability_groups {
        attack [
            Fartoom
            Mutilate
            SkullBash
            Shred
            Chomp
            BodySlam
            SliceAndDice
            Monch
            DeathWind
            Roast
            Swallow
            FireFart
            RoughToss
            Reflux
            HookBind
            LodgeHook
            Butcher
        ]
        defense [
            Burp
            ForceFeed
            Binge
            Gib
            DeliciousScent
            Tryptophan
            Regurge
        ]
        move [
            HogRush
            Trudge
            LunchTime
            Tromp
            CannonBall
            BadGas
            ButcherPurge
            Track
            TaintedOffering
            Grapnel
            Chonkwalk
        ]
        misc [
            SelfMutilate
            Succ
            Consume
            BloodMagic
            SmellBlood
            Vurp
            LightenTheLoad
            Spoil
            Grill
            MyTurn
            Sharpen
            Cough
            Rehook
            Contaminate
        ]
    }
    
    passive_pool [
        Putrefy
        NeverFull
        MainCourse
        FreshMeat
        Masochist

        Glutton
        Hooked
        Stompy
        Barbed
        GrapplingHook

        PainGain
        WideSwing
        Confrontational
        HeaveHook
        Harpooner

        LordOfTheFlies
        Schadenfreude
        Gurgitator
        LooseMeat
        Hack

        BowlingBall
        Testy
        Indigestion
        Incubator
        DukeOfFlies
    ]

    stat_mods {
        con 3
        str 2
        spd -2
    }

    levelup_stats [con str lck]
}
```

---

### `Druid`
**Name:** Druid  
**Source:** `advanced_classes.gon`  

**Localization Strings:**
- `CAT_CLASS_DRUID_DESC`: "One with nature! Druids are great at summoning animal friends and come with a special Crow counterpart!"

```
Druid {
    meta {
        name "CAT_CLASS_DRUID_NAME"
        description "CAT_CLASS_DRUID_DESC"
    }

    graphics {
        palette 65

        alt_animations [
            [idle, DruidIdle]
            [ClassToNeutral,   DruidToNeutral]
            [ClassFromNeutral, DruidFromNeutral]
            [StartTurn, DruidStartTurn]
            [Victory, druidVictory]
        ]
        
        portrait_face druid_portrait
    }

    attack_pool [
        BasicDruidAbility
    ]

    innate_passives {
        SpawnOnBattleStart Crow
    }

    ability_pool [
        ManaBomb
        SongOfSpring
        GrantLife
        SquirrelSquad
        SummonSquirrel

        DruidSwap
        BattleCry
        SummonSnake
        SummonTurtle
        SummonToad

        SummonBear
        PullToSafety
        BrambleBurst
        FlowerFeet
        ThornyFeet

        Encourage
        Protection
        Promote
        SafetyDance
        WarCry

        TigerForm
        MonkeyForm
        RhinoForm
        SummonCatepillar
        CallTheWind

        InspirationalSong
        DeathMetal
        ChaChaSlide
        BestowWisdom
        RaccoonForm

        SummonCrow
        WeWillRockYou
        TreeForm
        HydroPump
        ControlPlants

        ControlWater
        ControlAir
        Entangle
        Lullaby
        WeAreTheChampions

        Cheerlead
        NaturesBlessing
        ThrowEgg
        SquirrelForm
        PlantMushroom

        Serenade
        WindyStep
        ElkForm
        MockingbirdForm
        FromTheTrees
    ]

    starter_abilities [
        SummonSquirrel 
        SummonToad
        Encourage
        Protection
        SongOfSpring
        BattleCry
        SafetyDance
        TigerForm
		RhinoForm
		InspirationalSong
    ]

    ability_groups {
        attack [
            SquirrelSquad
            SummonSquirrel
            SummonSnake
            SummonToad
            BrambleBurst
            SummonBear
            WarCry
            TigerForm
            SummonCatepillar
            DeathMetal
            ThrowEgg
            FromTheTrees
        ]
        defense [
            SongOfSpring
            SummonTurtle
            PullToSafety
            Protection
            SafetyDance
            RhinoForm
            CallTheWind
            ChaChaSlide
            WeWillRockYou
            TreeForm
            ControlWater
            Entangle
            Lullaby
            NaturesBlessing
            Serenade
        ]
        move [
            DruidSwap
            FlowerFeet
            ThornyFeet
            RaccoonForm
            HydroPump
            ControlAir
            WindyStep
            ElkForm
        ]
        misc [
            ManaBomb
            BattleCry
            Encourage
            GrantLife
            Promote
            MonkeyForm
            InspirationalSong
            BestowWisdom
            SummonCrow
            ControlPlants
            WeAreTheChampions
            Cheerlead
            SquirrelForm
            PlantMushroom
            MockingbirdForm
        ]
    }
    
    passive_pool [
        SuperCrow
        NaturesGuidance
        PoisonIvy
        Pathfinder
        EmptyVessels

        WildAnimals
        BarkSkin
        SoothingSong
        Teamwork
        Bouquet

        GoodVibrations
        VersatileVocalist
        LikeAFish
        Encore
        SpecialFriends

        SneakAttack
        WildStyle
        BuddySystem
        FlowerPower
        SuicideSquad

        Feral
        RapGod
        Animalistic
        Maestro
        MegaMinions
    ]

    stat_mods {
        cha 3
        lck 1
        con -2
    }

    levelup_stats [cha int str]
}
```

---

### `Tinkerer`
**Name:** Tinkerer  
**Source:** `advanced_classes.gon`  

**Localization Strings:**
- `CAT_CLASS_TINKERER_DESC`: "A crafty inventor! Tinkerers are great at crafting temporary weapons and using all sorts of crazy gadgets!"

```
Tinkerer {
    meta {
        name "CAT_CLASS_TINKERER_NAME"
        description "CAT_CLASS_TINKERER_DESC"
    }

    graphics {
         palette 63

        alt_animations [
            [idle, TinkererIdle]
            [ClassToNeutral,   TinkererToNeutral]
            [ClassFromNeutral, TinkererFromNeutral]
            [StartTurn, TinkererStartTurn]
            [Victory, tinkererVictory]
        ]

        portrait_face tinkerer_portrait
    }

    attack_pool [
        TinkererCraft
    ]

    innate_passives {
        TinkererBasicAttackSwitching {
            craft_ability TinkererCraft
            throw_ability TinkererThrow
        }
    }

    ability_pool [
        Research
        Discharge
        Repair
        ShoddyJetpack
        SpawnDecoy

        SpringShoes
        AutoPilot
        Recycle
        BuildTurret
        RocketSkates

        DrillDown
        ArmorUp
        FreshOffTheForge
        ElectricNail
        Craft

        Shockwave
        Math
        Reprogram
        Improve
        Catbot

        Bombchu
        RemoteDetonator
        EjectButton
        ShortCircuit
        Electrolyze

        Firecrackers
        Upgrade
        Eureka
        PunchBot
        FastHands

        MechSuit
        UnreliableShield
        UnreliableMissile
        SpareParts
        BatteryNuke

        ExperimentalTeleporter
        ShockTherapy
        BuildNuke
        InstantBarrier
        VoltTackle

        Smash
        ShedScrap
        RepairArmor
        RocketRide
        RoboVac

        NurseBot
        TeslaCoil
        RefineMaterials
        Fabricate
        Sparks
    ]

    starter_abilities [
        Research
        ArmorUp
        ShoddyJetpack
        BuildTurret
        RocketSkates
        Discharge
		Craft
		Catbot
		Electrolyze
		InstantBarrier
    ]

    ability_groups {
        attack [
            Discharge
            Craft
            Recycle
            Shockwave
            Math
            Bombchu
            RemoteDetonator
            Firecrackers
            FastHands
            UnreliableMissile
            BatteryNuke
            Smash
            TeslaCoil
            Sparks
        ]
        defense [
            SpawnDecoy
            ArmorUp
            FreshOffTheForge
            ShortCircuit
            PunchBot
            UnreliableShield
            ShockTherapy
            InstantBarrier
            RepairArmor
            NurseBot
        ]
        move [
            ShoddyJetpack
            SpringShoes
            RocketSkates
            DrillDown
            EjectButton
            ExperimentalTeleporter
            VoltTackle
            RocketRide
        ]
        misc [
            Research
            Repair
            AutoPilot
            BuildTurret
            ElectricNail
            Reprogram
            Improve
            Catbot
            Electrolyze
            Upgrade
            Eureka
            MechSuit
            SpareParts
            BuildNuke
            ShedScrap
            RoboVac
            RefineMaterials
            Fabricate
        ]
    }
    
    passive_pool [
        VersionTwo
        WeaponProficiency
        LivingBattery
        FuzzyFeet
        ArmorSpecialist

        EMP
        MrMega
        EscapeSequence
        ItemProxy
        LightningRod

        ItsAlive
        Energizer
        ReactiveArmor
        Nanobots
        Scrapper

        DemoMan
        DuctTape
        ArmoredPlating
        BoobyTrap
        RobotArms

        Conductor
        Napalm
        Ingenuity
        Shrapnel_Tinkerer
        Blacksmith
    ]
    
    stat_mods {
        int 4
        lck -1
        cha -1
    }

    levelup_stats [dex cha int]
}
```

---

### `Necromancer`
**Name:** Necromancer  
**Source:** `advanced_classes.gon`  

**Localization Strings:**
- `CAT_CLASS_NECROMANCER_DESC`: "Rise from the dead! Necromancers are great at playing with corpses and leeching life from enemies!"

```
Necromancer {
    meta {
        name "CAT_CLASS_NECROMANCER_NAME"
        description "CAT_CLASS_NECROMANCER_DESC"
    }

    graphics {
        palette 68
        hud_palette 11

        alt_animations [
            [idle, NecromancerIdle]
            [ClassToNeutral,   NecromancerToNeutral]
            [ClassFromNeutral, NecromancerFromNeutral]
            [StartTurn, NecromancerStartTurn]
            [Victory, necromancerVictory]
        ]
        
        portrait_face necromancer_portrait
    }

    attack_pool [
        BasicNecroRanged
    ]

    ability_pool [
        MaggotArmy
        Reanimate
        Rebirth
        Pestilence
        Weakness

        SoulSuck
        EvilIncarnate
        SoulLink
        WeAreOne
        BloodRain

        AnimateDead
        DeathBloom
        Scare
        SoulTransfer
        Whisper

        SummonShade
        DarkStep
        Leeches
        Shriek
        FullMoon

        Unearth
        BloodGeyser
        Flatline
        Replace
        SummonBones

        GigaDrain
        Bloodletting
        MassPsychosis
        Debone
        Reap

        CarrionShot
        LifeDrain
        CoffinFlop
        DonateBlood
        Seance

        GoLimp
        DemonicPact
        Curse
        LeechSwarm
        Feed

        Hush
        ReaperStep
        ForbiddenFamine
        FleshGolem
        TradeLife

        AbsorbSoul
        Gravecrawl
        DigUpTheDead
        SpiderEgg
        ClewOfLeeches
    ]

    starter_abilities [
        SoulLink
        Reanimate
        Rebirth
        CarrionShot
        Pestilence
        BloodGeyser
        MaggotArmy 
		Gravecrawl
		FullMoon
		CoffinFlop
    ]

    ability_groups {
        attack [
            Pestilence
            DeathBloom
            Leeches
            BloodGeyser
            GigaDrain
            Debone
            CarrionShot
            LifeDrain
            LeechSwarm
            SpiderEgg
        ]
        defense [
            Weakness
            EvilIncarnate
            BloodRain
            SoulTransfer
            Whisper
            Shriek
            FullMoon
            Flatline
            DonateBlood
            Hush
            TradeLife
        ]
        move [
            Rebirth
            Scare
            DarkStep
            Replace
            Reap
            CoffinFlop
            ReaperStep
            Gravecrawl
            DigUpTheDead
        ]
        misc [
            MaggotArmy
            Reanimate
            SoulSuck
            SoulLink
            WeAreOne
            AnimateDead
            SummonShade
            Unearth
            SummonBones
            Bloodletting
            MassPsychosis
            Seance
            GoLimp
            DemonicPact
            Curse
            Feed
            ForbiddenFamine
            FleshGolem
            AbsorbSoul
            ClewOfLeeches
        ]
    }
    
    passive_pool [
        Vampirism
        OneWithNothing
        BedBugs
        WormLord
        InfiniteRebirth

        SacrificialLamb
        DeathIncarnate
        OffloadPain
        CambionConception
        Leechmother

        Infected
        LastGasp
        RelentlessDead
        ChainsOfGuilt
        DarkPriest

        Undeath
        NumbingLeeches
        EternalHealth
        Torpor
        SoulBound

        Superstition
        ImmortalLeeches
        CorpseConnoisseur
        Parasitic
        SpreadSorrow
    ]

    stat_mods {
        con 2
        cha 1
        str -2
    }

    levelup_stats [dex cha con]
}
```

---

### `Psychic`
**Name:** Psychic  
**Source:** `advanced_classes.gon`  

**Localization Strings:**
- `CAT_CLASS_PSYCHIC_DESC`: "Clear your mind! Psychics are great at manipulating things from afar and moving objects with their minds! Psychics also have +5 starting mana."

```
Psychic {
    meta {
        name "CAT_CLASS_PSYCHIC_NAME"
        description "CAT_CLASS_PSYCHIC_DESC"
    }

    graphics {
        palette 62

        alt_animations [
            [idle, PsychicIdle]
            [ClassToNeutral,   PsychicToNeutral]
            [ClassFromNeutral, PsychicFromNeutral]
            [StartTurn, PsychicStartTurn]
            [Victory, psychicVictory]
        ] 

        portrait_face psychic_portrait
    }

    innate_passives {
        AddStartingMana 5
    }

    attack_pool [
        BasicPsychicPull
    ]

    ability_pool [
        Telekinesis
        Suggestion
        MindControl
        MegaGrav
        PsyFlutter

        MagnetPull
        MindBlast
        PsychicChoke
        SkyShatter
        Supernova

        AlterDNA
        Flicker
        MindMeld
        Vaccuum
        Ping

        FlashForward
        Order
        TemporalShards
        RealityScramble
        Glare

        BlindingFlash
        Snatch
        FutureSight
        MassManaLeech
        BecomeEntropy

        FastForward
        AncestralRecall
        CumulativeBlast
        Hallucinate
        MassHysteria

        ExtraTurnQuestion
        MindCrack
        Reset
        Mimic
        ChaosSwap

        Asteroid
        Stasis
        Pass
        ThinkDeep
        Puppet

        YouSeeNothing
        ForceBlast
        IncreaseGravity
        Manifest
        Flip

        Withdraw
        ForceCone
        Inversion
        Echo
        Slipstream
    ]

    starter_abilities [
        Ping
        Telekinesis
        Suggestion
        SkyShatter
        MindMeld
        Glare
        MindCrack
        FlashForward
		CumulativeBlast
		IncreaseGravity
    ]

    ability_groups {
        attack [
            Telekinesis
            Suggestion
            MindControl
            PsychicChoke
            Supernova
            Ping
            Order
            BecomeEntropy
            CumulativeBlast
            Asteroid
            Puppet
            ForceCone
        ]
        defense [
            MagnetPull
            MindBlast
            Vaccuum
            BlindingFlash
            FutureSight
            Reset
            Stasis
            ForceBlast
            IncreaseGravity
            Flip
        ]
        move [
            PsyFlutter
            Flicker
            FlashForward
            FastForward
            ChaosSwap
            Manifest
            Withdraw
            Inversion
            Echo
            Slipstream
        ]
        misc [
            MegaGrav
            SkyShatter
            AlterDNA
            MindMeld
            TemporalShards
            RealityScramble
            Glare
            Snatch
            MassManaLeech
            AncestralRecall
            Hallucinate
            ExtraTurnQuestion
            MindCrack
            Mimic
            Pass
            ThinkDeep
            YouSeeNothing
        ]
    }
    
    passive_pool [
        Flying
        SoulShatter
        Glow
        Blink
        FullPower

        RealityShatter
        MentalStorm
        Wither
        Flourish
        PsySmack

        Beckon
        MindTempest
        Overflow
        Omniscience
        PsionicRepel

        Enlightened
        MadVisage
        PowerUp
        TrueSight
        Radiation

        GravityWell
        Drag
        Twiddle
        RepressedMemories
        EldritchVisage
    ]

    stat_mods {
        int 1
        cha 1
        spd 1
        con -1
    }

    levelup_stats [int cha spd]
}
```

---

### `Jester`
**Name:** Jester  
**Source:** `advanced_classes.gon`  

**Localization Strings:**
- `CAT_CLASS_JESTER_DESC`: "You can be anything! Jesters have no limits!"

```
Jester {
    meta {
        name "CAT_CLASS_JESTER_NAME"
        description "CAT_CLASS_JESTER_DESC"
    }

    graphics {
        //palette 67
        palette [54 50 55 52 51 53     66 64 63 65 68 62]

        alt_animations [
            [idle, JesterIdle]
            [ClassToNeutral,   JesterToNeutral]
            [ClassFromNeutral, JesterFromNeutral]
            [StartTurn, JesterStartTurn]
            [Victory, jesterVictory]
        ]

        portrait_face jester_portrait
    }

    attack_pool [
        BasicMelee_Fighter
        BasicRanged_Hunter
        BasicMagicShortRanged
        BasicTankMelee
        BasicStraightShot_Thief
        BasicMedicMelee
        BasicButcherMelee
        BasicPsychicPull
        BasicNecroRanged
    ]

    ability_pool [
        SmartMetronome
        RNGCannon
        Bump
        PowerUp
        //hard coded
    ]

    passive_pool [
        SuperLuck
        Goofball
        //hard coded
    ]

    stat_mods {

    }

    levelup_stats [str dex con int spd cha lck]
}
```

---

## File: `classes.gon`

### `Fighter`
**Name:** Fighter  
**Source:** `classes.gon`  

**Localization Strings:**
- `CAT_CLASS_FIGHTER_DESC`: "Punch your way to victory! Fighters are great at doing big strong melee attacks and smashing things to pieces!"

```
Fighter {
    meta {
        name "CAT_CLASS_FIGHTER_NAME"
        description "CAT_CLASS_FIGHTER_DESC"
    }

    graphics {
        palette 54

        alt_animations [
            [idle, FighterIdle]
            [ClassToNeutral,   FighterToNeutral]
            [ClassFromNeutral, FighterFromNeutral]
            [StartTurn, FighterStartTurn]
            [Victory, fighterVictory]
        ]

        default_face happy
        portrait_face fighter_portrait
    }

    attack_pool [
        BasicMelee_Fighter
    ]

    ability_pool [
        Spin
        Dash
        FirePunch
        IcePunch
        ThunderPunch

        FurySwipes
        SideSlash
        FighterLeap
        Uppercut
        Counter

        TailWhip
        Poke
        Nip
        Push
        FalconPunch

        Exert
        Enrage
        Tumble
        Confront
        Juiced

        CosmicPunch
        FighterTaunt
        GravitySlam
        Berserk
        Challenge

        Stoopzerk
        SleeperHold
        Grapple
        ThinkTooHard
        Zoomzerk

        Bloodzerk
        ExhaustingBlow
        ChaosRampage
        MeteorSlam
        MuscleMemory

        Inhale
        OneTwoPunch
        TeamSpin
        TeamFlex
        Huddle

        RagePunch
        BreakingPoint
        AssertDominance
        DumbMove
        SuckerPunch

        Stick
        Hurl
        BigPunch
        Pawbreaker
        Ram
    ]

    complicated_abilities [
        FalconPunch
        Exert
        Challenge
        Stoopzerk
        Grapple
        ThinkTooHard
        Zoomzerk
        Bloodzerk
        ExhaustingBlow
        ChaosRampage
        MeteorSlam
        MuscleMemory
        Huddle
        BreakingPoint
        AssertDominance
    ]

    starter_abilities [
        FurySwipes
        Dash
        Spin
        Confront
        FirePunch
        SideSlash
        Exert
        Berserk
		Stick
		Counter
    ]

    ability_groups {
        attack [
            Spin
            FirePunch
            IcePunch
            ThunderPunch
            FurySwipes
            SideSlash
            Uppercut
            TailWhip
            Poke
            FalconPunch
            CosmicPunch
            ExhaustingBlow
            MeteorSlam
            MuscleMemory
            OneTwoPunch
            TeamSpin
            RagePunch
            BreakingPoint
            AssertDominance
            Hurl
            BigPunch
            Pawbreaker
        ]
        /*defense [
            
        ]*/
        move [
            Dash
            FighterLeap
            Tumble
            Confront
            Juiced
            GravitySlam
            Zoomzerk
            DumbMove
            Ram
        ]
        misc [
            Nip
            Exert
            Enrage
            FighterTaunt
            Berserk
            Challenge
            Stoopzerk
            SleeperHold
            Grapple
            ThinkTooHard
            ChaosRampage
            Inhale
            Huddle
            Stick

            //moved from def
            Counter
            Push
            Bloodzerk
            TeamFlex
            SuckerPunch
        ]
    }
    
    passive_pool [
        BloodLust
        Avenger
        Scars
        FasterWhenHit
        KillsHeal

        Vengeful
        HamsterStyle
        WeaponMaster
        ShoulderCheck
        SkullSmash

        TurtleStyle
        Overpowered
        FightMe
        HighAsYouCanCount
        DumbMuscle

        ThickSkull
        MostValuableCat
        RatStyle
        Boned
        DualWield

        ReflexPunch
        HitMe
        Smash
        PunchFace
        Recoil
    ]

    complicated_passives [
        ShoulderCheck
        DumbMuscle
        ThickSkull
        MostValuableCat
        HitMe
    ]

    stat_mods {
        str 2
        spd 1
        int -1
    }

    levelup_stats [str con spd]
}
```

---

### `Hunter`
**Name:** Hunter  
**Source:** `classes.gon`  

**Localization Strings:**
- `CAT_CLASS_HUNTER_DESC`: "Shoot things from afar! Hunters are great at hitting things from a distance while staying out of danger themselves!"

```
Hunter {
    meta {
        name "CAT_CLASS_HUNTER_NAME"
        description "CAT_CLASS_HUNTER_DESC"
    }

    graphics {
        palette 50
    
        alt_animations [
            [idle, HunterIdle]
            [ClassToNeutral,   HunterToNeutral]
            [ClassFromNeutral, HunterFromNeutral]
            [StartTurn, HunterStartTurn]
            [Victory, hunterVictory]
        ]

        portrait_face hunter_portrait
    }

    attack_pool [
        BasicRanged_Hunter
    ]

    ability_pool [
        LineShot
        SpawnMaggotFriend
        SpawnPooterFriend
        Marked
        HailOfNails

        ScatterShot
        BrambleShot
        BearTrap
        TwinShot
        CrossShot

        SpawnBaitTrap
        BombShot
        SummonBrambles
        FireShot
        FocusShot

        Shards
        TerrainWalk
        Extend
        ChaosShot
        NeedleShot

        SpikeTrap
        FleaShot
        WebTrap
        LastHit
        CupidsArrow

        ArrowFlurry
        HeavyShot
        StakeOut
        BallOfSpiders
        Snipe

        Diversion
        ArrowSmith
        TacticalRetreat
        Infest
        CollectPelt

        SentryMode
        Pheromones
        SpawnTomTomFriend
        ScoutMe
        CraftArrow

        CharmTrap
        BounceShot
        Picnic
        SoothingShot
        Vivisect

        PoisonLace
        SlopThePigs
        SpiderInjector
        PersistentHunt
        Bunker
    ]

    complicated_abilities [
        Extend
        LastHit
        StakeOut
        Diversion
        ScoutMe
        CraftArrow
        BounceShot
        Vivisect
        SlopThePigs
        SpiderInjector
        PersistentHunt
    ]

    starter_abilities [
        SpawnPooterFriend 
        BrambleShot 
        SpawnBaitTrap 
        BearTrap 
        TerrainWalk
        NeedleShot
        ScatterShot
        Marked
		FleaShot
	    HeavyShot
    ]

    ability_groups {
        attack [
            LineShot
            HailOfNails
            ScatterShot
            BrambleShot
            TwinShot
            CrossShot
            BombShot
            FireShot
            FocusShot
            ChaosShot
            SpikeTrap
            FleaShot
            ArrowFlurry
            HeavyShot
            BallOfSpiders
            Snipe
            Infest
            ScoutMe
            Vivisect
        ]
        defense [
            SpawnMaggotFriend
            SpawnPooterFriend
            BearTrap
            SpawnBaitTrap
            SummonBrambles
            WebTrap
            CupidsArrow
            Diversion
            SentryMode
            SpawnTomTomFriend
            CharmTrap
            Picnic
            SoothingShot
            SlopThePigs
            Bunker
        ]
        move [
            
        ]
        misc [
            Marked
            Shards
            Extend
            NeedleShot
            LastHit
            TerrainWalk //move
            StakeOut
            ArrowSmith
            TacticalRetreat //move
            CollectPelt
            Pheromones
            CraftArrow
            BounceShot
            PoisonLace
            SpiderInjector
            PersistentHunt
        ]
    }
    
    passive_pool [
        TakeAim
        HuntersBoon
        BroodMother
        TaintedMother
        Quiver

        SplitShot
        Hazardous
        ThornArrows
        Traps
        CatchProjectiles

        TowerDefense
        TrickyTraps
        GravityFalls
        HawkEye
        Spotters

        LuckSwing
        Host
        Sniper
        RubberArrows
        TalkToAnimals

        AnimalControl
        SleepDarts
        Survivalist
        Fleabag
        ThrillOfTheHunt
    ]

    complicated_passives [ 
        Hazardous
        Traps
        CatchProjectiles
        Host
        SleepDarts
        Survivalist
    ]

    stat_mods {
        dex 3
        lck 2
        con -1
        spd -2
    }

    levelup_stats [dex spd int]
}
```

---

### `Mage`
**Name:** Mage  
**Source:** `classes.gon`  

**Localization Strings:**
- `CAT_CLASS_MAGE_DESC`: "Blast your foes! Mages are great at casting all sorts of crazy spells and dealing elemental damage!"

```
Mage {
    meta {
        name "CAT_CLASS_MAGE_NAME"
        description "CAT_CLASS_MAGE_DESC"
    }

    graphics {
        palette 55
    
        alt_animations [
            [idle, MageIdle]
            [ClassToNeutral,   MageToNeutral]
            [ClassFromNeutral, MageFromNeutral]
            [StartTurn, MageStartTurn]
            [Victory, mageVictory]
        ]

        portrait_face mage_portrait
    }

    attack_pool [
        BasicMagicShortRanged
    ]

    ability_pool [
        Surf
        Bolt
        Fireball
        FreezeRay
        MagicMissile

        Blast
        WallOfFire
        HyperBeam
        MeteorStorm
        MegaBlast

        Slow
        WindSlash
        MageTeleport
        MageSwap
        Absorb

        Warp
        ManaMeld
        Inspire
        Telefrag
        ChaosTeleport

        CryoHeal
        Gust
        Blizzard
        Inferno
        Thunderburst

        DealWithTheDevil
        ForbiddenFlame
        ForbiddenFlood
        WaterSphere
        ChainLightning

        Shatter
        ForbiddenFulmination
        FireBolt
        IcicleTaser
        FreezerBurn

        Corrupt
        Jolt
        Smolder
        FireSurge
        IceSurge

        LightningSurge
        Creshendo
        Divide
        ForbiddenFrost
        BlackMagic

        Teach
        HomingBlasts
        Replicate
        Magnify
        TriAttack
    ]

    complicated_abilities [
        DealWithTheDevil
        ForbiddenFlame
        ForbiddenFlood
        ForbiddenFulmination
        Corrupt
        FireSurge
        IceSurge
        LightningSurge
        Creshendo
        Divide
        ForbiddenFrost
        Teach
        TriAttack
    ]

    starter_abilities [
        MagicMissile
        Fireball
        FreezeRay
        Warp
        Surf
        WindSlash
        Absorb
        Bolt
		Inspire
		MegaBlast
    ]

    ability_groups {
        attack [
            Surf
            Bolt
            Fireball
            MagicMissile
            Blast
            HyperBeam
            MeteorStorm
            MegaBlast
            WindSlash
            Blizzard
            Inferno
            Thunderburst
            ForbiddenFlame
            ForbiddenFlood
            WaterSphere
            ChainLightning
            ForbiddenFulmination
            FireBolt
            IcicleTaser
            FreezerBurn
            FireSurge
            LightningSurge
            Creshendo
            HomingBlasts
            TriAttack
        ]
        defense [
            FreezeRay
            WallOfFire
            Slow
            Absorb
            CryoHeal
            Gust
            IceSurge
            ForbiddenFrost
        ]
        move [
            MageTeleport
            MageSwap
            Warp
            Telefrag
            ChaosTeleport
            Jolt
        ]
        misc [
            ManaMeld
            Inspire
            DealWithTheDevil
            Shatter
            Corrupt
            Smolder
            Divide
            BlackMagic
            Teach
            Replicate
            Magnify
        ]
    }
    
    passive_pool [
        Micronaps
        HolyMantel
        Shrapnel
        BurningPaws
        LightningPaws

        IcePaws
        PawMissile
        Overload
        ChargeUp
        Recharged

        EnergyStorm
        FireArmor
        IceArmor
        Resonance
        LearnFromMe

        LightningArmor
        LongCast
        LightUpTheStage
        ElementalAttunement
        LatentEnergy

        Five
        MagicGuru
        One
        Two
        Four
    ]

    complicated_passives [
        ElementalAttunement
        LatentEnergy
        MagicGuru
        One
        Two
        Four
        Five
    ]

    stat_mods {
        int 2
        cha 2
        con -1
        str -1
    }

    levelup_stats [int cha dex]
}
```

---

### `Medic`
**Name:** Cleric  
**Source:** `classes.gon`  

**Localization Strings:**
- `CAT_CLASS_MEDIC_DESC`: "Be the best friend! Clerics are great at keeping your team alive and helping them recover from taking hits!"

```
Medic {
    meta {
        name "CAT_CLASS_MEDIC_NAME"
        description "CAT_CLASS_MEDIC_DESC"
    }

    graphics {
        palette 52

        alt_animations [
            [idle, HealerIdle]
            [ClassToNeutral,   HealerToNeutral]
            [ClassFromNeutral, HealerFromNeutral]
            [StartTurn, HealerStartTurn]
            [Victory, clericVictory]
        ]

        portrait_face medic_portrait
    }

    attack_pool [
        BasicMedicMelee
    ]

    ability_pool [
        RangedHeal
        MeleeHeal
        Malaise
        OpenWounds
        Prayer

        Convert
        Cleanse
        HereticMark
        Zealot
        Haste

        Rally
        BuddyUp
        HealingFall
        RallyCharge
        ReverseDamage

        Rebuke
        Wish
        WitchHunt
        FriendOrFoe
        Revive

        HolyLight
        Ethereal
        BornAgain
        Benediction
        Crusade

        Enlighten
        HallowedGround
        Anoint
        EyeForAnEye
        WrathOfGod

        Adoubement
        DivineProtection
        ChosenWarrior
        SwiftSanctify
        GetDown

        DivineGift
        HolyWeapon
        Awaken
        Baptism
        Pray

        Emergency
        GuardianAngel
        Booster
        Stimulants
        BlindingLight

        CircleOfProtection
        CallOver
        Grace
        TurnFoe
        HealingSalve
    ]

    complicated_abilities [
        OpenWounds
        WitchHunt
        Adoubement
        DivineProtection
        ChosenWarrior
        SwiftSanctify
        DivineGift
        HolyWeapon
        GetDown
        Rebuke
        ReverseDamage
    ]

    starter_abilities [
        RangedHeal
        Rally
        Prayer
        FriendOrFoe
        HolyWeapon
        Zealot
        OpenWounds
        RallyCharge
		HallowedGround
		Cleanse
    ]

    ability_groups {
        attack [
            OpenWounds
            HereticMark
            Rally
            Rebuke
            FriendOrFoe
            HolyLight
            EyeForAnEye
            WrathOfGod
            HolyWeapon
        ]
        defense [
            RangedHeal
            MeleeHeal
            Prayer
            Cleanse
            Zealot
            ReverseDamage
            Wish
            Ethereal
            Benediction
            Adoubement
            DivineProtection
            DivineGift
            Baptism
            GuardianAngel
            Booster
            CircleOfProtection
            HealingSalve
        ]
        move [
            BuddyUp
            HealingFall
            RallyCharge
            Crusade
            SwiftSanctify
            GetDown
            Emergency
            Stimulants
            CallOver
            TurnFoe
        ]
        misc [
            Haste
            WitchHunt
            Revive
            BornAgain
            ChosenWarrior
            Awaken
            Pray
            Grace
            BlindingLight
            Convert
            Malaise
        ]
    }
    
    passive_pool [
        HealingAura
        NaturalHealer
        Eternal
        Blessed
        EvilPatron

        AngelicInspiration
        TopOff
        SharingIsCaring
        Caretaker
        MoraleBoost

        RangedMedic
        Godspeed
        GodWarrior
        BreathOfLife
        ThouShaltNotKill

        ThouShaltNotCovet
        BlessingOfHolyFire
        AlmsForThePoor
        Purifier
        VeneratedTouch

        ProtectTheWeak
        ThouShaltObey
        EnchantedRelic
        BlessingOfSpirit
        Heathens
    ]

    complicated_passives [
        RangedMedic //not complicated but dont want it showing up the first time you play Cleric
        ThouShaltNotKill
        BlessingOfHolyFire
        BlessingOfSpirit
    ]

    stat_mods {
        cha 2
        con 2
        spd -1
        dex -1
    }

    levelup_stats [cha int con]
}
```

---

### `Tank`
**Name:** Tank  
**Source:** `classes.gon`  

**Localization Strings:**
- `CAT_CLASS_TANK_DESC`: "Get in the way! Tanks are great at absorbing damage and pushing enemies around!"

```
Tank {
    meta {
        name "CAT_CLASS_TANK_NAME"
        description "CAT_CLASS_TANK_DESC"
    }

    graphics {
        palette 51
    
        alt_animations [
            [idle, TankIdle]
            [ClassToNeutral,   TankToNeutral]
            [ClassFromNeutral, TankFromNeutral]
            [StartTurn, TankStartTurn]
            [Victory, tankVictory]
        ]

        portrait_face tank_portrait
    }

    attack_pool [
        BasicTankMelee
    ]

    ability_pool [
        HeadButt
        ThrowShield
        ChewCud
        AssBlast
        Chew

        BatterUp
        BackBreaker
        Suplex
        Intimidate
        Toss

        BellyFlop
        TankTrample
        TankSwap
        ToTheRescue
        TankTantrum

        Earthquake
        RockToss
        BarbedWire
        DrawAttention
        BowlOver

        Clap
        TankRockSong
        RockCrusher
        BodyGuard
        Gore

        RockBlast
        RockTomb
        BearHug
        Fissure
        BigRock

        FlipFlop
        Lunge
        Nudge
        StoneGaze
        Medusa

        Anchor
        EatRock
        PlantFeet
        IronHead
        GangUp

        Aftershock
        SteelSkin
        FaultLine
        Demolish
        PushThrough

        Spur
        Supper
        FullForce
        Sandstorm
        Thicken
    ]

    complicated_abilities [
        TankRockSong
        FlipFlop
        Lunge
        PlantFeet
        IronHead
        Aftershock
        Demolish
        FullForce
        Thicken
        Spur
    ]

    starter_abilities [
        TankSwap
        Toss
        BellyFlop
        BatterUp
        Chew
        ThrowShield
        DrawAttention
        BodyGuard
		Earthquake
		Spur
    ]

    ability_groups {
        attack [
            Chew
            BatterUp
            Suplex
            TankTantrum
            Earthquake
            RockToss
            RockBlast
            BigRock
            Lunge
            GangUp
            Aftershock
            FaultLine
            FullForce
        ]
        defense [
            HeadButt
            ThrowShield
            ChewCud
            AssBlast
            BackBreaker
            Intimidate
            Toss
            BodyGuard
            Nudge
            StoneGaze
            Medusa
            Anchor
            PlantFeet
            IronHead
            SteelSkin
            Supper
        ]
        move [
            BellyFlop
            TankTrample
            TankSwap
            ToTheRescue
            BowlOver
            RockCrusher
            Gore
            FlipFlop
            PushThrough
        ]
        misc [
            BarbedWire
            DrawAttention
            Clap
            TankRockSong
            BearHug
            Fissure
            EatRock
            Demolish
            Spur
            Sandstorm
            Thicken
        ]
    }
    
    passive_pool [
        Thorns
        HeavyHanded
        SlackOff
        Scabs
        ThunderThighs

        Plow
        PetRocks
        ToadStyle
        ChainKnockback
        ProtectiveAura

        Wrestlemaniac
        MountainForm
        HomeRun
        RockAspect
        WideLoad

        HardHead
        MyLeg
        Hardy
        SlowAndSteady
        FollowUp

        CatAPult
        ShovingMatch
        Stoic
        PriorityTarget
        Bouncer
    ]

    complicated_passives [
        Plow
        ChainKnockback
        Wrestlemaniac
        MyLeg
        SlowAndSteady
        ShovingMatch
    ]

    stat_mods {
        con 4
        int -1
        dex -1
    }

    levelup_stats [con str spd]
}
```

---

### `Thief`
**Name:** Thief  
**Source:** `classes.gon`  

**Localization Strings:**
- `CAT_CLASS_THIEF_DESC`: "Attack from the shadows! Thiefs are great at evading hits, collecting coins, and striking from behind!"

```
Thief {
    meta {
        name "CAT_CLASS_THIEF_NAME"
        description "CAT_CLASS_THIEF_DESC"
    }

    graphics {
        palette 53
    
        alt_animations [
            [idle, ThiefIdle] 
            [ClassToNeutral,   ThiefToNeutral]
            [ClassFromNeutral, ThiefFromNeutral]
            [StartTurn, ThiefStartTurn]
            [Victory, thiefVictory]
        ]

        portrait_face thief_portrait
    }

    attack_pool [
        BasicStraightShot_Thief
    ]

    ability_pool [
        MoveAgain
        Assassinate
        BoostBackstab
        PoisonGas
        PoisonNail

        WeakeningNail
        SharpNail
        CoinToss
        Shadow
        TimeWalk

        Distract
        Rebound
        CutPurse
        EagleEye
        PickPocket

        Blur
        GreedStep
        Stalk
        Backflip
        AttackAgain

        NailFlurry
        Declaw
        QuickRoll
        Slice
        PocketSand

        Nightshade
        Shadowshift
        SlingShade
        Caltrops
        PierceShot

        Cheat
        VenomBarrage
        LootCorpse
        SeverArtery
        Fade

        SharpenNail
        SneakUp
        StealKidney
        StealLuck
        ThiefSwap

        Pierce
        WindUp
        TripleNails
        SkinDisguise
        Jitter

        Chakram
        StealTime
        Outskirts
        PoisonDip
        LuckyPenny
    ]

    complicated_abilities [
        QuickRoll
        Shadowshift
        SlingShade
        ThiefSwap
        Pierce
        TripleNails
        SkinDisguise
        PoisonDip
    ]

    starter_abilities [
        Shadow
        PoisonNail
        MoveAgain
        Backflip
        Distract
        Rebound
        Stalk
        Assassinate
		CutPurse
		SeverArtery
    ]

    ability_groups {
        attack [
            Assassinate
            PoisonGas
            PoisonNail
            WeakeningNail
            SharpNail
            CoinToss
            Rebound
            AttackAgain
            Declaw
            Slice
            CutPurse
            NailFlurry
            Nightshade
            SlingShade
            PierceShot
            VenomBarrage
            SeverArtery
            StealKidney
            StealLuck
            TripleNails
            Chakram
            StealTime
        ]
        /*defense [ //moved to misc
            
        ]*/
        move [
            MoveAgain
            Shadow
            GreedStep
            Stalk
            QuickRoll
            Shadowshift
            Caltrops
            SneakUp
            ThiefSwap
            Outskirts
        ]
        misc [
            TimeWalk
            Distract
            EagleEye
            PickPocket
            Blur //def
            Backflip //def
            PocketSand //def
            BoostBackstab
            Cheat
            LootCorpse
            Fade //def
            SharpenNail
            Pierce
            WindUp
            SkinDisguise //def
            Jitter //def
            PoisonDip
            LuckyPenny
        ]
    }
    
    passive_pool [
        Backstabber
        GoldenClaws
        Shadow
        PoisonTips
        Burgle

        SwiftKiller
        DoubleThrow
        BountyHunter
        RazorClaws
        Looter

        AlphaStrike
        Zip
        WeakSpot
        Penetrate
        AfterImage

        Shiv
        Critical
        LootHoarder
        Cripple
        Agile

        Shank
        FlipACoin
        ShakeDown
        SweetSpot
        Pinpoint
    ]

    complicated_passives [
        BountyHunter
        AfterImage
        Agile
        FlipACoin
    ]

    stat_mods {
        spd 4
        lck 1
        str -1
        con -1 //possibly -2 to balance the stats more
    }

    levelup_stats [spd dex lck]
}
```

---

### `Colorless`
**Name:** Collarless  
**Source:** `classes.gon`  

**Localization Strings:**
- `CAT_CLASS_COLORLESS_DESC`: "It's a cat!"

```
Colorless {
    meta {
        name "CAT_CLASS_COLORLESS_NAME"
        description "CAT_CLASS_COLORLESS_DESC"
    }

    graphics {
        alt_animations [
            [StartTurn, ColorlessStartTurn]
        ]
    }

    attack_pool [
        BasicMelee
        BasicMelee
        BasicShortRanged
        BasicShortLobbed
    ]

    move_pool [
        DefaultMove
    ]

    ability_pool [
        Block
        Rest
        Brace
        Roll
        SharpenClaws

        Reach
        ManaDrain
        SoothingGlow
        Ponder
        Brainstorm

        Focus
        Metabolize
        GainThorns
        PrepareToJump
        BoostSpellRange

        PushMove
        Gamble
        SoulReap
        Hunt
        Flex

        Dart
        Smack
        Spit
        MiniHook
        MiniDistract

        ButtScoot
        Confusion
        Reflect
        PlayDead
        HealBolt

        SlipThrough
        Dump
        Snacks
        FeatherFeet
        Reduce

        Nerf
        Trip
        Copycat
        Metronome
        DollUp

        StackTheDeck
        Infiltrate
        Burst
        Suppress
        Endeavor

        LotteryShottery
        CatNap
        PissYourself
        FindARock
        BurgeoningBlast

        BurgeoningBarrier
        BurgeoningBattery
        HoseOff
        Taint
        PokeWound

        WasteTime
        Desecrate
        Contort
        RussianRoulette
        Step

        Interchange
        LookAtMe
        Rouse
        Shift
        Donate

        Magnet
        ScuffItOff
        BarfBall
        DexterousHit
        Till

        PathOfTheMage
        PathOfTheHunter
        PathOfTheThief
        PathOfTheFighter
        PathOfTheTank

        PathOfTheCleric
        PathOfTheButcher
        PathOfThePsychic
        PathOfTheTinkerer
        PathOfTheMonk

        PathOfTheDruid
        PathOfTheNecromancer
        Itch
        Meow
        Swat

        LickHeal
        Purr
        Hiss
        Knead
        BuyCatnip

        VetVisit
        HireHitman
        SubwayRide
        GymMembership
        SuperCrateBox

        BBQ
        CPR
        Blow
        Toast
        Landscape

        Zap
        Sunburn
        ColdShoulder
        BlowKiss
        ForbiddenFart

        WetHairball
        PathOfTheVoid
        PathOfTheJester
    ]

    passive_pool [
        SelfAssured
        LuckDrain
        Infested
        Worms
        Amped

        Furious
        MetalDetector
        DeathProof
        Leader
        Mange

        ETank
        Careful
        DirtyClaws
        LateBloomer
        Study

        SkillShare
        NaturalHealing
        LongShot
        FastFooted
        Slugger

        Pulp
        Amplify
        DeathBoon
        SantaSangre
        Untouched

        Daunt
        AnimalHandler
        WhipCracker
        PressurePoints
        Gassy

        Dealer
        Patience
        Wiggly
        MiniMe
        BareMinimum

        Unrestricted
        DeathsDoor
        OverConfident
        SerialKiller
        StrengthInNumbers

        FightersSoul
        MagesSoul
        TanksSoul
        HuntersSoul
        ThiefsSoul

        ClericsSoul
        NecromancersSoul
        TinkerersSoul
        DruidsSoul
        MonksSoul

        ButchersSoul
        PsychicsSoul
        Charming
        FirstImpression
        Scavenger

        ZenkaiBoost
        Protection
        Rockin
        Mania
        Lucky
        
        OneEighty
        JestersSoul
        HotBlooded
        VoidSoul
    ]
    
    tutorial_levelup_active_pool [
        Block
        LickHeal
        //Sunburn //hard coded to guarantee this in slot 2 in LevelUpScreen.cpp, so its removed from the pool
        Dump
    ]
    tutorial_levelup_active_pool_2 [
        GainThorns
        ButtScoot
        Burst
        HireHitman
    ]
    tutorial_levelup_passive_pool [
        Furious
        PressurePoints
        LateBloomer
        ZenkaiBoost
    ]

    levelup_stats [str dex con int spd cha lck]
}
```

---

