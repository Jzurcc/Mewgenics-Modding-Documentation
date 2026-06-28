# Map Generation and Routing Directory

## File: `alley.gon`

### `levels`
**Source:** `alley.gon`  

```
levels {
    folder alley
    easy [easy]
    hard [easy] //switch this to "hard" in the brackets if we get specific hard levels in!
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `bosses`
**Name:** of  
**Source:** `alley.gon`  

```
bosses {
    radicalrat auto //auto means set subfolder and boss_cutscene to the name of the boss
    queenhippo auto
    /*radicalrat {
        subfolder radicalrat
        boss_cutscene radicalrat
    }
    queenhippo {
        subfolder queenhippo
        boss_cutscene queenhippo
    }*/
}
```

---

### `minibosses`
**Source:** `alley.gon`  

```
minibosses {
    fightercat auto
    huntercat auto
    magecat auto
    tankcat auto
    jestercat auto
}
```

---

### `events`
**Source:** `alley.gon`  

```
events {
    normal [
        common
        alley_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `alley.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [Maggot Fly Flea Pinky]
    medium [Rat Leaper Pooter Kitten TomTom Mangy CatCaller]
    large []
}
```

---

### `item_pools`
**Source:** `alley.gon`  

```
item_pools {
    chapter_item_pool alleyitems
}
```

---

### `nodes`
**Source:** `alley.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map sewers.gon
        locked true
        override_art MapNodeExit_Sewers
    }
    exit1 {
        type exit
        next_map junkyard.gon
        locked true
        override_art MapNodeExit_Junkyard
    }
    exit_desert {
        type exit
        next_map desert.gon
        locked true
        override_art MapNodeExit_Desert
        hidden true
    }
    exit_lab {
        type exit
        next_map lab.gon
        locked true
        override_art MapNodeExit_Lab
        hidden true
    }
    hard_initial {
	    type hard
        locked true
    }

    //special
    boss {
        type boss
        unlockcheck_on_complete map_unlock_junkyard
    }
}
```

---

### `flags`
**Source:** `alley.gon`  

```
flags {
    HardPathUnlocked {
        hard_initial {
            locked false
        }
    }
    SewersUnlocked {
        exit0 {
            locked false
        }
    }
    JunkyardUnlocked {
        exit1 {
            locked false
        }
    }
    /*DesertUnlocked {
        exit_desert {
            locked false
            hidden false
        }
    }
    LabUnlocked {
        exit_lab {
            locked false
            hidden false
        }
    }*/
}
```

---

## File: `boneyard.gon`

### `levels`
**Source:** `boneyard.gon`  

```
levels {
    folder boneyard
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `boneyard.gon`  

```
events {
    normal [
        common
        boneyard_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `boneyard.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [Flea Wisp Fly Maggot]
    medium [ZombieCat SkeletonCat TallSkeletonCat WolfCat Tatters Spookie Scary Reaper TallRobes GraveWorm ButtZombie]
    large [Shambler]
}
```

---

### `item_pools`
**Source:** `boneyard.gon`  

```
item_pools {
    chapter_item_pool boneyarditems
}
```

---

### `minibosses`
**Source:** `boneyard.gon`  

```
minibosses {
    mamamaggot auto
}
```

---

### `nodes`
**Source:** `boneyard.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map meatworld.gon
        hidden true
        override_art MapNodeExit_MeatWorld
    }

    quest_event {
        type special_event
        level Quest_ThrobbingArtery
        override_art MapNode_Veins
    }

    //special
    boss {
        type boss
        is_final_boss true
        boss_cutscene dybbuk
    }
}
```

---

### `flags`
**Source:** `boneyard.gon`  

```
flags {
    ThrobbingArteryDone {
        quest_event {
            level Quest_ThrobbingArtery2
            override_art MapNode_VeinsDrained
        }
    }
    MeatWorldUnlocked {
        quest_event {
            type empty
            override_art MapNode_Empty
        }
        exit0 {
            hidden false
        }
    }
}
```

---

## File: `bunker.gon`

### `levels`
**Source:** `bunker.gon`  

```
levels {
    folder bunker
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `bunker.gon`  

```
events {
    normal [
        common
        bunker_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `bunker.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small []
    medium [AtomicKitten RoboTom CatCultist Cultist CultistZealot CultistMutant CultistBishop BishopHat LoveBot SecurityBot Hive FloatingHive]
    large [KillDozer]
}
```

---

### `item_pools`
**Source:** `bunker.gon`  

```
item_pools {
    chapter_item_pool bunkeritems
}
```

---

### `minibosses`
**Source:** `bunker.gon`  

```
minibosses {
    lenny auto
    bumblefoot auto
}
```

---

### `nodes`
**Source:** `bunker.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map core.gon
        locked true
        override_art MapNodeExit_Core
    }

    //special
    boss {
        type boss
        boss_cutscene johnny
    }
}
```

---

### `flags`
**Source:** `bunker.gon`  

```
flags {
    CoreUnlocked {
        exit0 {
            locked false
        }
    }
}
```

---

## File: `caves.gon`

### `levels`
**Source:** `caves.gon`  

```
levels {
    folder caves
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `caves.gon`  

```
events {
    normal [
        common
        caves_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `caves.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [TinySpider]
    medium [SkullOoze BrainDrain Bat TallSpiderCat SpiderCat Toadie AlbinoTomTom KirbyFetus TenTickles]
    large [MegaFetus]
}
```

---

### `item_pools`
**Source:** `caves.gon`  

```
item_pools {
    chapter_item_pool cavesitems
}
```

---

### `minibosses`
**Source:** `caves.gon`  

```
minibosses {
    slime auto
}
```

---

### `nodes`
**Source:** `caves.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map meatworld.gon
        hidden true
        override_art MapNodeExit_MeatWorld
    }

    quest_event {
        type special_event
        level Quest_WallOfFlesh
        override_art MapNode_FleshHole
    }

    //special
    boss {
        type boss
        is_final_boss true
        boss_cutscene spiderkitten
    }
}
```

---

### `flags`
**Source:** `caves.gon`  

```
flags {
    WallOfFleshDone {
        quest_event {
            level Quest_WallOfFlesh2
            override_art MapNode_FleshWall
        }
    }
    MeatWorldUnlocked {
        quest_event {
            type empty
            override_art MapNode_Empty
        }
        exit0 {
            hidden false
        }
    }
}
```

---

## File: `core.gon`

### `levels`
**Source:** `core.gon`  

```
levels {
    folder core
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `core.gon`  

```
events {
    normal [
        common
        core_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `core.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small []
    medium [CoreFreak PokerDemon Whisperer CloakedDemon BigDemon HeadTumor TallTumor DemonHooker Belcher TumorCat]
    large [MegaTumor]
}
```

---

### `item_pools`
**Source:** `core.gon`  

```
item_pools {
    chapter_item_pool coreitems
}
```

---

### `minibosses`
**Source:** `core.gon`  

```
minibosses {
    cerberubs auto
}
```

---

### `nodes`
**Source:** `core.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map dimensionx.gon
        hidden true
        override_art MapNodeExit_DimensionX
    }

    //special
    boss {
        type boss
        boss_cutscene coven
    }

    quest_event {
        type special_event
        level Quest_CoreObelisk
        override_art MapNode_ObeliskHalf
    }
}
```

---

### `flags`
**Source:** `core.gon`  

```
flags {
    CoreObeliskUnlocked {
        quest_event {
            level Quest_CoreObeliskRaised
            override_art MapNode_ObeliskFull
        }
    }

    BothObelisksUnlocked {
        quest_event {
            level Quest_CoreObeliskGlowing
            override_art MapNode_ObeliskGlowing
        }
    }

    DimensionXUnlocked {
        quest_event {
            level Quest_DimensionXPortal
            override_art MapNode_RiftPortal
        }
    }
}
```

---

## File: `crater.gon`

### `levels`
**Source:** `crater.gon`  

```
levels {
    folder crater
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `crater.gon`  

```
events {
    normal [
        common
        crater_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `crater.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [Amoeba]
    medium [GeoLad BrambleBaby Hemlock Nettle Birthwort Tremblo Infested RockHead NoHead CraterCreeper]
    large [Carnibulb]
}
```

---

### `item_pools`
**Source:** `crater.gon`  

```
item_pools {
    chapter_item_pool crateritems
}
```

---

### `minibosses`
**Source:** `crater.gon`  

```
minibosses {
    rockybobo auto
    infestedduo auto
}
```

---

### `nodes`
**Source:** `crater.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map moon.gon
        locked true
        override_art MapNodeExit_Moon
    }

    //special
    boss {
        type boss
        boss_cutscene alienqueen
    }

    weather_event {
        type special_event
        level CraterWeatherEvent
    }
}
```

---

### `flags`
**Source:** `crater.gon`  

```
flags {
    MoonUnlocked {
        exit0 {
            locked false
        }
    }
}
```

---

## File: `desert.gon`

### `levels`
**Source:** `desert.gon`  

```
levels {
    folder desert
    easy [easy]
    hard [easy] //switch this to "hard" in the brackets if we get specific hard levels in!
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `desert.gon`  

```
events {
    normal [
        common
        desert_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `desert.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [RattleSnake]
    medium [FlySwarm SnakeyBones Carcus Peashy BabyDeathWorm HornyCat GunCat Mangy2 ScorpionCat]
    large [SkeletonShambler Thump DeathWorm]
}
```

---

### `item_pools`
**Source:** `desert.gon`  

```
item_pools {
    chapter_item_pool desertitems
}
```

---

### `bosses`
**Source:** `desert.gon`  

```
bosses {
    zodiac auto
    gambit auto
}
```

---

### `minibosses`
**Source:** `desert.gon`  

```
minibosses {
    thiefcat auto
    clericcat auto
    butchercat auto
    necrocat auto
    jestercat auto
}
```

---

### `nodes`
**Source:** `desert.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map bunker.gon
        locked true
        override_art MapNodeExit_Bunker
    }
    exit1 {
        type exit
        next_map crater.gon
        locked true
        override_art MapNodeExit_Crater
    }

    //special
    boss {
        type boss
    }
    shop_water {
        type shop
        level WaterShop
		override_art cheapwatershop
    }
    shop_cheapwater {
        type shop
        level WaterShopCheap
		override_art cheapwatershop
    }
}
```

---

### `flags`
**Source:** `desert.gon`  

```
flags {
    BunkerUnlocked {
        exit0 {
            locked false
        }
    }
    CraterUnlocked {
        exit1 {
            locked false
        }
    }
}
```

---

## File: `dimensionx.gon`

### `levels`
**Source:** `dimensionx.gon`  

```
levels {
    folder dimensionx
    easy [easy]
    hard [easy] //switch this to "hard" in the brackets if we get specific hard levels in!
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `dimensionx.gon`  

```
events {
    normal [
        common
    ]
}
```

---

### `enemy_pools`
**Source:** `dimensionx.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [FrankPinky]
    medium [JackCat ChaosStacy FrankFetus BeaniesRat]
    large [ButchTinkBoris TracyFetus]
}
```

---

### `item_pools`
**Source:** `dimensionx.gon`  

```
item_pools {
    chapter_item_pool dimensionxitems
}
```

---

### `nodes`
**Source:** `dimensionx.gon`  

```
nodes {
    #include "standard_nodes.gon"

    boss {
        type boss
        boss_cutscene chaos
        override_music chaos_boss
    }

    quest_event {
        type special_event
        level Quest_DimensionXRift
        override_art MapNode_DeadChaos
    }
}
```

---

### `flags`
**Source:** `dimensionx.gon`  

```
flags {
    ChaosAntennaAttached {
        quest_event {
            override_art MapNode_DeadChaosAntenna
        }
    }
}
```

---

## File: `endoftime.gon`

### `levels`
**Source:** `endoftime.gon`  

```
levels {
    folder theinfinite
    easy [easy]
    hard [easy] //switch this to "hard" in the brackets if we get specific hard levels in!
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `endoftime.gon`  

```
events {
    normal [
        common
    ]
}
```

---

### `enemy_pools`
**Source:** `endoftime.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small []
    medium [Cherubim Seraphim Gatekeeper AngelicKitten AngelicCat]
    large []
}
```

---

### `item_pools`
**Source:** `endoftime.gon`  

```
item_pools {
    chapter_item_pool theinfiniteitems
}
```

---

### `nodes`
**Source:** `endoftime.gon`  

```
nodes {
    #include "standard_nodes.gon"

    boss {
        tileset finalboss
        type boss
        boss_cutscene thecreator
        override_music finalboss
    }

    quest_event {
        type special_event
        level Quest_DeadGod
        override_art MapNode_DeadChild
    }
}
```

---

### `flags`
**Source:** `endoftime.gon`  

```
flags {

}
```

---

## File: `eventdebug.gon`

### `levels`
**Source:** `eventdebug.gon`  

```
levels {
    folder alley
    //folder future
    easy [easy]
    hard [hard]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    nemesis [nemesis]
}
```

---

### `events`
**Source:** `eventdebug.gon`  

```
events {
    normal [
        common
        special_events.gon
    ]
}
```

---

### `item_pools`
**Source:** `eventdebug.gon`  

```
item_pools {
    chapter_item_pool alleyitems
}
```

---

### `nemesis`
**Source:** `eventdebug.gon`  

```
nemesis {
    head_start 99
    advance 1
    spawn_node start
    repeat never
}
```

---

### `nodes`
**Source:** `eventdebug.gon`  

```
nodes {
    #include "standard_nodes.gon"

    boss {
        type boss
        boss_cutscene radicalrat
    }
}
```

---

### `generated_nodes`
**Source:** `eventdebug.gon`  

```
generated_nodes {

}
```

---

### `groups`
**Source:** `eventdebug.gon`  

```
groups {

}
```

---

### `flags`
**Source:** `eventdebug.gon`  

```
flags {

}
```

---

## File: `future.gon`

### `levels`
**Source:** `future.gon`  

```
levels {
    folder future
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `future.gon`  

```
events {
    normal [
        common
        future_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `future.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [Invader]
    medium [FatCat FutureBot SoldierBot HangerBot DoctorBot TallBot TVBot JarHead FetusJar FetusNoJar]
    large [FatMan FatWoman]
}
```

---

### `item_pools`
**Source:** `future.gon`  

```
item_pools {
    chapter_item_pool futureitems
}
```

---

### `minibosses`
**Source:** `future.gon`  

```
minibosses {
    lightningelemental auto
    drmangler auto
}
```

---

### `nodes`
**Source:** `future.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map theend.gon
        locked true
        override_art MapNodeExit_TheEnd
    }

    //special
    boss {
        type boss
        boss_cutscene hitler
    }

    time_machine {
        type special_event
        level Quest_TimeMachineFuture
        override_art MapNode_TimeMachine
    }
}
```

---

### `flags`
**Source:** `future.gon`  

```
flags {
    TheEndUnlocked {
        exit0 {
            locked false
        }
    }
}
```

---

## File: `iceage.gon`

### `levels`
**Source:** `iceage.gon`  

```
levels {
    folder iceage
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `iceage.gon`  

```
events {
    normal [
        common
        iceage_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `iceage.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small []
    medium [CaveBaby CaveMan CaveWoman WereMan CaveChief Yeti Yeticat SabertoothCat SabertoothCub MammothBaby Fuzzer]
    large [Mammoth]
}
```

---

### `item_pools`
**Source:** `iceage.gon`  

```
item_pools {
    chapter_item_pool iceageitems
}
```

---

### `minibosses`
**Source:** `iceage.gon`  

```
minibosses {
    iceelemental auto
    cavecatfamily auto
}
```

---

### `nodes`
**Source:** `iceage.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map jurassic.gon
        locked true
        override_art MapNodeExit_Jurassic
    }

    //special
    boss {
        type boss
        boss_cutscene lordbunga
    }

    time_machine {
        type special_event
        level Quest_TimeMachineIceAge
        override_art MapNode_TimeMachine
    }
}
```

---

### `flags`
**Source:** `iceage.gon`  

```
flags {
    JurassicUnlocked {
        exit0 {
            locked false
        }
    }
}
```

---

## File: `junkyard.gon`

### `levels`
**Source:** `junkyard.gon`  

```
levels {
    folder junkyard
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `junkyard.gon`  

```
events {
    normal [
        common
        junkyard_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `junkyard.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [Maggot Fly]
    medium [Lumpy GlassSpitter Siren Jekyll SpikedCat PopeyeCat ChumBag Chummy Host]
    large []
}
```

---

### `item_pools`
**Source:** `junkyard.gon`  

```
item_pools {
    chapter_item_pool junkyarditems
}
```

---

### `minibosses`
**Source:** `junkyard.gon`  

```
minibosses {
    cancreeper auto
    trampy auto
}
```

---

### `nodes`
**Source:** `junkyard.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map boneyard.gon
        locked true
        override_art MapNodeExit_Boneyard
    }

    //special
    boss {
        type boss
        boss_cutscene chubsandnubs
    }
}
```

---

### `flags`
**Source:** `junkyard.gon`  

```
flags {
    BoneyardUnlocked {
        exit0 {
            locked false
        }
    }
}
```

---

## File: `jurassic.gon`

### `levels`
**Source:** `jurassic.gon`  

```
levels {
    folder jurassic
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `jurassic.gon`  

```
events {
    normal [
        common
        jurassic_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `jurassic.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small []
    medium [PrehistoricPooter Pterodactyl Raptor RaptorBaby Ankylosaurus Parasaurolophus Maelestes DinoEggs]
    large [Trex Stegosaurus Triceratops]
}
```

---

### `item_pools`
**Source:** `jurassic.gon`  

```
item_pools {
    chapter_item_pool jurassicitems
}
```

---

### `minibosses`
**Source:** `jurassic.gon`  

```
minibosses {
    dinocouple auto
}
```

---

### `nodes`
**Source:** `jurassic.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map endoftime.gon
        hidden true
        override_art MapNodeExit_Infinite
    }

    //special
    boss {
        type boss
        boss_cutscene megadino
    }

    quest_event {
        type special_event
        level Quest_Volcano
        override_art MapNode_Volcano
    }

    time_machine {
        type special_event
        level Quest_TimeMachineJurassic
        override_art MapNode_TimeMachine
    }
}
```

---

### `flags`
**Source:** `jurassic.gon`  

```
flags {
    VolcanoAntennaAttached {
        quest_event {
            override_art MapNode_VolcanoAntenna
        }
    }
    EndOfTimeUnlocked {
        exit0 {
            hidden false
        }
    }
}
```

---

## File: `lab.gon`

### `levels`
**Source:** `lab.gon`  

```
levels {
    folder lab
    easy [easy]
    hard [easy] //switch this to "hard" in the brackets if we get specific hard levels in!
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `lab.gon`  

```
events {
    normal [
        common
        lab_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `lab.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small []
    medium [RatCat Gamete NubsCat CatHuman HumanCat CopBot DrDitto Drcat Mangy3 Needlecat Stacy2p0]
    large [MegaMutant]
}
```

---

### `item_pools`
**Source:** `lab.gon`  

```
item_pools {
    chapter_item_pool labitems
}
```

---

### `bosses`
**Source:** `lab.gon`  

```
bosses {
    stacy auto
    spewer auto
}
```

---

### `minibosses`
**Source:** `lab.gon`  

```
minibosses {
    druidcat auto
    monkcat auto
    psychiccat auto
    tinkerercat auto
    jestercat auto
}
```

---

### `random_generation_flags`
**Source:** `lab.gon`  

```
random_generation_flags {
    choose_one [GenFlag_Boss_Stacy, GenFlag_Boss_Spewer] //select one of these flags at random to set upon map generation
}
```

---

### `nodes`
**Source:** `lab.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map iceage.gon
        locked true
        override_art MapNodeExit_IceAge
    }
    exit1 {
        type exit
        next_map future.gon
        locked true
        override_art MapNodeExit_Future
    }

    //special
    boss {
        type boss
    }

    miniboss_event {
        type empty
    }

    quest_event {
        type special_event
        level Quest_BrokenTimeMachine
        override_art MapNode_BrokenTimeMachine
    }
}
```

---

### `flags`
**Source:** `lab.gon`  

```
flags {
    IceAgeUnlocked {
        quest_event {
            level Quest_TimeMachine
            override_art MapNode_TimeMachine
        }
    }
    FutureUnlocked {
        quest_event {
            level Quest_TimeMachine
            override_art MapNode_TimeMachine
        }
    }
    GenFlag_Boss_Stacy {
        miniboss_event {
            type special_event
            level StacyMutant1
        }
        boss {
            level stacy
        }
    }
    GenFlag_Boss_Spewer {
        boss {
            level spewer
        }
    }
}
```

---

## File: `meatworld.gon`

### `levels`
**Source:** `meatworld.gon`  

```
levels {
    folder meatworld
    easy [easy]
    hard [easy] //switch this to "hard" in the brackets if we get specific hard levels in!
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `meatworld.gon`  

```
events {
    normal [
        common
    ]
}
```

---

### `enemy_pools`
**Source:** `meatworld.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [Clot Maggot]
    medium [Skinned ThrobbingTurret FleshLad Parasiter MeatSlime StemCat TumorousMaggot ChargeyMaggot SwappyMaggot]
    large []
}
```

---

### `item_pools`
**Source:** `meatworld.gon`  

```
item_pools {
    chapter_item_pool meatworlditems
}
```

---

### `nodes`
**Source:** `meatworld.gon`  

```
nodes {
    #include "standard_nodes.gon"

    mw_altar {
        type special_event
        level Quest_MeatWorldAltar
        override_art MapNode_MeatAltar
    }

    mw_earlyhome {
        type home
    }

    mw_battle1 {
        type battle
        hidden true
    }

    mw_hard1 {
        type hard
        hidden true
        musiclayer boss
    }

    mw_event1 {
        type event
        hidden true
    }

    mw_treasure {
        type treasure
        hidden true
    }

    mw_boss {
        type boss
        boss_cutscene throbbingking
        hidden true
        override_music throbbingking
    }

    mw_quest_event {
        type special_event
        level Quest_DeadKing
        override_art MapNode_DeadKing
        hidden true
    }

    mw_home {
        type home
        hidden true
    }
}
```

---

### `flags`
**Source:** `meatworld.gon`  

```
flags {
    MeatWorldUnlockedFull {
        mw_battle1 {
            hidden false
        }
        mw_hard1 {
            hidden false
        }
        mw_event1 {
            hidden false
        }
        mw_treasure {
            hidden false
        }
        mw_boss {
            hidden false
        }
        mw_quest_event {
            hidden false
        }
        mw_home {
            hidden false
        }
        mw_earlyhome {
            hidden true
        }
        //mw_altar {
        //    type empty
        //}
    }
}
```

---

## File: `moon.gon`

### `levels`
**Source:** `moon.gon`  

```
levels {
    folder moon
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `moon.gon`  

```
events {
    normal [
        common
        moon_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `moon.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [MoonWorm]
    medium [BigAsteroid SmallAsteroid SmallUFO YellowBlaster GreyAlien GreenProber Waggle MoonWorm Rover Astro]
    large [BigUFO]
}
```

---

### `item_pools`
**Source:** `moon.gon`  

```
item_pools {
    chapter_item_pool moonitems
}
```

---

### `minibosses`
**Source:** `moon.gon`  

```
minibosses {
    abandonedones auto
}
```

---

### `nodes`
**Source:** `moon.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map dimensionx.gon
        hidden true
        override_art MapNodeExit_DimensionX
    }

    //special
    boss {
        type boss
        boss_cutscene moonhead
    }

    quest_event {
        type special_event
        level Quest_MoonObelisk
        override_art MapNode_ObeliskHalf
    }
}
```

---

### `flags`
**Source:** `moon.gon`  

```
flags {
    MoonObeliskUnlocked {
        quest_event {
            level Quest_MoonObeliskRaised
            override_art MapNode_ObeliskFull
        }
    }

    BothObelisksUnlocked {
        quest_event {
            level Quest_MoonObeliskGlowing
            override_art MapNode_ObeliskGlowing
        }
    }

    DimensionXUnlocked {
        quest_event {
            level Quest_DimensionXPortal
            override_art MapNode_RiftPortal
        }
    }
}
```

---

## File: `sewers.gon`

### `levels`
**Source:** `sewers.gon`  

```
levels {
    folder sewer
    easy [easy bigsharklevels]
    hard [easy bigsharklevels]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `sewers.gon`  

```
events {
    normal [
        common
        sewer_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `sewers.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [Dip]
    medium [BabyShark GassyCat SharkyCat BoomerCat WaterKitten Pile Floater WaterLeech Fetus FetusGusher]
    large [DaddyShark]
}
```

---

### `item_pools`
**Source:** `sewers.gon`  

```
item_pools {
    chapter_item_pool seweritems
}
```

---

### `minibosses`
**Source:** `sewers.gon`  

```
minibosses {
    flushmaster auto
    ratking auto
    //todo: ice elemental cutscene if its snowing
}
```

---

### `nodes`
**Source:** `sewers.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map caves.gon
        locked true
        override_art MapNodeExit_Caves
    }
    hard_initial {
	    type hard
        locked true
    }

    //special
    boss {
        type boss
        boss_cutscene boris
    }
}
```

---

### `flags`
**Source:** `sewers.gon`  

```
flags {
    HardPathUnlocked {
        hard_initial {
            locked false
        }
    }
    CavesUnlocked {
        exit0 {
            locked false
        }
    }
}
```

---

## File: `standard_nodes.gon`

### `node`
**Source:** `standard_nodes.gon`  

```
node {
	type empty
}
```

---

### `npc`
**Source:** `standard_nodes.gon`  

```
npc {
	type npc
	locked true
}
```

---

### `battle`
**Source:** `standard_nodes.gon`  

```
battle {
	type battle
}
```

---

### `event`
**Source:** `standard_nodes.gon`  

```
event {
	type event
}
```

---

### `optional_event`
**Source:** `standard_nodes.gon`  

```
optional_event {
	type optional_event
}
```

---

### `miniboss`
**Source:** `standard_nodes.gon`  

```
miniboss {
	type miniboss
}
```

---

### `hard`
**Source:** `standard_nodes.gon`  

```
hard {
	type hard
}
```

---

### `c4hard`
**Source:** `standard_nodes.gon`  

```
c4hard {
	type hard
	musiclayer boss
}
```

---

### `treasure`
**Source:** `standard_nodes.gon`  

```
treasure {
	type treasure
}
```

---

### `treasure_hard`
**Source:** `standard_nodes.gon`  

```
treasure_hard {
	type treasure
	level TreasureHard
	override_art Rare_Treasure
}
```

---

### `shop`
**Source:** `standard_nodes.gon`  

```
shop {
	type shop
}
```

---

### `start`
**Source:** `standard_nodes.gon`  

```
start {
	type enter
}
```

---

### `home`
**Source:** `standard_nodes.gon`  

```
home {
	type home
}
```

---

### `battle_testskip`
**Source:** `standard_nodes.gon`  

```
battle_testskip {
	//type battle
	type empty
}
```

---

### `hard_testskip`
**Source:** `standard_nodes.gon`  

```
hard_testskip {
	//type hard
	type empty
}
```

---

### `foodbox`
**Source:** `standard_nodes.gon`  

```
foodbox {
	type foodbox
}
```

---

### `largemeteor`
**Source:** `standard_nodes.gon`  

```
largemeteor {
	type treasure
	level Treasure_LargeMeteor
	override_art MapNode_LargeMetor
}
```

---

### `smallmeteor`
**Source:** `standard_nodes.gon`  

```
smallmeteor {
	type treasure
	level Treasure_SmallMeteor
	override_art MapNode_SmallMeteor
}
```

---

### `furniturebox`
**Source:** `standard_nodes.gon`  

```
furniturebox {
	type treasure
	level Treasure_FurnitureBox
	override_art MapNode_FurnitureBox
}
```

---

### `furniturebox2`
**Source:** `standard_nodes.gon`  

```
furniturebox2 {
	type treasure
	level Treasure_MedFurnitureBox
	override_art MapNode_FurnitureBox2
}
```

---

### `furniturebox3`
**Source:** `standard_nodes.gon`  

```
furniturebox3 {
	type treasure
	level Treasure_RareFurnitureBox
	override_art MapNode_FurnitureBox3
}
```

---

### `abilityneedle`
**Source:** `standard_nodes.gon`  

```
abilityneedle {
	type treasure
	level Treasure_AbilityNeedle
	override_art MapNode_Needle
}
```

---

### `largemoneybag`
**Source:** `standard_nodes.gon`  

```
largemoneybag {
	type treasure
	level Treasure_LargeMoneyBag
	override_art MapNode_BigMoneyBag
}
```

---

### `smallmoneybag`
**Source:** `standard_nodes.gon`  

```
smallmoneybag {
	type treasure
	level Treasure_SmallMoneyBag
	override_art MapNode_SmallMoneyBag
}
```

---

### `treasure_radiated`
**Source:** `standard_nodes.gon`  

```
treasure_radiated {
	type treasure
	level Treasure_IrradiatedObject
	override_art MapNode_CursedTreasure
}
```

---

### `ancestor_bones`
**Source:** `standard_nodes.gon`  

```
ancestor_bones {
	type treasure
	level Treasure_AncestorsSkull
	override_art MapNode_Bones
}
```

---

### `glowing_bones`
**Source:** `standard_nodes.gon`  

```
glowing_bones {
	type treasure
	level Treasure_GlowingBone
	override_art MapNode_GlowingBones
}
```

---

## File: `theend.gon`

### `levels`
**Source:** `theend.gon`  

```
levels {
    folder theend
    easy [easy]
    hard [easy]
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `theend.gon`  

```
events {
    normal [
        common
        theend_events.gon
    ]
}
```

---

### `enemy_pools`
**Source:** `theend.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small []
    medium [BoyShade GirlShade Gasper Floast TumorBarrier Husk ConjoinedHusk CancerCat CollectiveCat ShadeCat]
    large [Slag]
    //extra_large [Gorger] //this one is 3x3 so it probably needs its own pool?
}
```

---

### `item_pools`
**Source:** `theend.gon`  

```
item_pools {
    chapter_item_pool theenditems
}
```

---

### `minibosses`
**Source:** `theend.gon`  

```
minibosses {
    thebloat auto
}
```

---

### `nodes`
**Source:** `theend.gon`  

```
nodes {
    #include "standard_nodes.gon"

    //exits
    exit0 {
        type exit
        next_map endoftime.gon
        hidden true
        override_art MapNodeExit_Infinite
    }

    //special
    boss {
        type boss
        boss_cutscene themother
    }

    quest_event {
        type special_event
        level Quest_Orb
        override_art MapNode_Orb
    }

    time_machine {
        type special_event
        level Quest_TimeMachineTheEnd
        override_art MapNode_TimeMachine
    }
}
```

---

### `flags`
**Source:** `theend.gon`  

```
flags {
    VolcanoAntennaAttached {
        quest_event {
            override_art MapNode_OrbAntenna
        }
    }
    EndOfTimeUnlocked {
        exit0 {
            hidden false
        }
    }
}
```

---

## File: `tutorial.gon`

### `levels`
**Source:** `tutorial.gon`  

```
levels {
    folder tutorial
    easy [easy]
    hard [easy] //switch this to "hard" in the brackets if we get specific hard levels in!
    rare [rare]
    boss [boss]
    miniboss [miniboss]
    special [special]
}
```

---

### `events`
**Source:** `tutorial.gon`  

```
events {
    normal [
        common
    ]
}
```

---

### `enemy_pools`
**Source:** `tutorial.gon`  

```
enemy_pools { //for effects that need to spawn a "chapter enemy" of some sort
    small [Maggot Fly Flea Pinky]
    medium [Rat Leaper Pooter Kitten TomTom Mangy CatCaller]
    large []
}
```

---

### `item_pools`
**Source:** `tutorial.gon`  

```
item_pools {

}
```

---

### `nodes`
**Source:** `tutorial.gon`  

```
nodes {
    start {
	    type enter
    }

    battle {
	    type battle
    }

    treasure {
	    type treasure
        level TreasureTutorial
    }

    event {
	    type event
        level Butch_Tutorial
    }

    //exits
    home {
	    type home
    }

    //special
    boss {
        type boss
        boss_cutscene pebbles
    }
}
```

---

## File: `world.gon`

### `nodes`
**Source:** `world.gon`  

```
nodes {
	alley {}
		sewers {}
		caves {}

		junkyard {}
		boneyard {}

		meatworld {}


	desert {}
		crater {}
		moon {}

		bunker {}
		core {}

		dimensionx {
			spin_cats true
		}

	lab {}
		future {
			spin_cats true
		}
		theend {
			spin_cats true
		}

		iceage {
			spin_cats true
		}
		jurassic {
			spin_cats true
		}

		endoftime {
			spin_cats true
		}
}
```

---

