# World and Events/Map Generation and Routing Directory

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

### `innate_weather`
**Source:** `desert.gon`  

```
innate_weather [HeatWave]
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

### `innate_weather`
**Source:** `iceage.gon`  

```
innate_weather [Snow]
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

### `innate_weather`
**Source:** `moon.gon`  

```
innate_weather [LowGravity]
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

## File: `tilesets.gon`

### `alley`
**Source:** `tilesets.gon`  

```
alley {
    combat_background AlleyBGTest
    combat_ui_background UI_Background
    
    static_1x1_a Rubble
    static_1x1_b Bricks
    static_1x1_c Bricks
    
    static_2x2_a Dumpster
    static_2x2_b Dumpster
    
    static_tall_a PowerPole
    static_tall_b PhoneBooth
    
    debris Debris

    event_piece_frame alley

    global_objects {
        Fly {
            count [0 20]
        }
    }

    reverb {
        battle {
            preset Alley
            amount .35
            ReverbDelay .2
            volume_adjustment 1.3
        }
    }
}
```

---

### `junkyard`
**Source:** `tilesets.gon`  

```
junkyard {
    combat_background JunkyardBG
    combat_ui_background UI_Background_Junkyard
    
    static_1x1_a StaticJunkSmall
    static_1x1_b Stump
    static_1x1_c SmallGravelPile
    
    static_2x2_a StaticJunkCube
    static_2x2_b BigGravelPile
    
    static_tall_a Tree
    static_tall_b StaticTires
    
    debris Debris2

    event_piece_frame junkyard

    
    global_objects {
        Fly {
            count [0 20]
        }
    }

    reverb {
        battle {
            preset ParkingLot
            amount .35
            ReverbDelay .25
            DecayTime 1.68
            volume_adjustment 1.35

        }
    }

}
```

---

### `sewers`
**Source:** `tilesets.gon`  

```
sewers {
    combat_background SewerBG
    combat_ui_background UI_Background_Sewers
    background_extra_shader water
    
    static_1x1_a SmallPipes
    static_1x1_b Bricks3
    static_1x1_c Sludge
    
    static_2x2_a BigPipes
    static_2x2_b Dumpster
    
    static_tall_a TallPipe
    static_tall_b PhoneBooth
    
    debris Debris3

    event_piece_frame sewers

    global_particles [CaveDrip]
	
	global_objects {
        Lighting {
            ambient .7
        }
    }

    reverb {
        battle {
            preset StoneRoom
            amount .4
            volume_adjustment 1.5
        }
    }
}
```

---

### `caves`
**Source:** `tilesets.gon`  

```
caves {
    combat_background CavesBG
    combat_ui_background UI_Background_Caves
    
    static_1x1_a CaveRock1
    static_1x1_b CaveRock2
    static_1x1_c CaveRock3
    
    static_2x2_a BigCaveRock1
    static_2x2_b BigCaveRock1
    
    static_tall_a TallCaveRock1
    static_tall_b TallCaveRock2
    
    debris CaveDebris

    event_piece_frame caves

    global_objects {
        Lighting {
            ambient .5
            bigrays [1, 1]
            smallrays [1, 2]
        }
        Firefly {
            count [0 2]
        }
    }
    global_particles [CaveDrip]

    reverb {
        battle {
            preset Cave
            amount .65
            volume_adjustment 1.50
            DecayTime 1.8
        }
    }
}
```

---

### `boneyard`
**Source:** `tilesets.gon`  

```
boneyard {
    combat_background BoneYardBG
    combat_ui_background UI_Background_Graves
    
    static_1x1_a GraveRocks1
    static_1x1_b GraveRocks2
    static_1x1_c GraveRocks2
    
    static_2x2_a BigGraveRocks1
    static_2x2_b BigGraveRocks1
    
    static_tall_a TallGraveRocks1
    static_tall_b TallGraveRocks1
    
    debris GravesDebris

    event_piece_frame graves


    global_objects {
        Lighting {
            ambient .7
            bigrays [0, 0]
            smallrays [0, 0]
        }
    }
    global_particles [Mist]

    reverb {
        battle {
            preset ParkingLot
            amount .35
            ReverbDelay .25
            DecayTime 1.68
            volume_adjustment 1.35

        }
    }
}
```

---

### `desert`
**Source:** `tilesets.gon`  

```
desert {
    combat_background DesertBG
    combat_ui_background DesertUI
    
    static_1x1_a DesertRocks
    static_1x1_b DesertCactus
    static_1x1_c DesertRocks
    
    static_2x2_a Desert2x2
    static_2x2_b Desert2x2
    
    static_tall_a DesertTall
    static_tall_b DesertTall2
    
    debris DesertDebris

    event_piece_frame desert

    global_objects {
        Fly {
            count [0 20]
        }
    }

    reverb {
        battle {
            preset Forest
            amount .35
            ReverbDelay .45
            DecayTime 1.68
            volume_adjustment 1.5
        }
    }
}
```

---

### `bunker`
**Source:** `tilesets.gon`  

```
bunker {
    combat_background BunkerBG
    combat_ui_background UI_Background_Bunker
    
    static_1x1_a BunkerObjects1
    static_1x1_b BunkerObjects2
    static_1x1_c SmallGravelPile
    
    static_2x2_a Bunker2x2
    static_2x2_b BigGravelPile
    
    static_tall_a BunkerTall1
    static_tall_b BunkerTall2
    
    debris Debris7

    event_piece_frame bunker

    global_objects {
        Lighting {
            ambient .4

            smallrays [2, 6]
            bigrays [0, 0]

            smallray_clip Bunkerlight
        }
        
        Cockroach {
            count [0 20]
        }
    }

    reverb {
        battle {
            preset Cave
            amount .65
            volume_adjustment 1.50
            DecayTime 1.8
        }
    }
}
```

---

### `crater`
**Source:** `tilesets.gon`  

```
crater {
    combat_background CraterBG
    combat_ui_background UI_Background_Crater
    
    static_1x1_a CraterObjects1
    static_1x1_b CraterObjects2
    static_1x1_c CraterObjects1
    
    static_2x2_a Crater2x2
    static_2x2_b Desert2x2
    
    static_tall_a CraterTall1
    static_tall_b CraterTall2
    
    debris Debris8

    event_piece_frame crater
    global_objects {
        Fly {
            count [0 20]
        }
    }

    global_particles [CraterLeaves]

    reverb {
        battle {
            preset Forest
            amount .35
            ReverbDelay .45
            DecayTime 1.68
            volume_adjustment 1.5
        }
    }
}
```

---

### `core`
**Source:** `tilesets.gon`  

```
core {
    combat_background CoreBG
    boss_background_alt CoreBossBG
    combat_ui_background CoreUI
    
    static_1x1_a CoreObjects1
    static_1x1_b CoreObjects2
    static_1x1_c CoreObjects3
    
    static_2x2_a Core2x2
    static_2x2_b Desert2x2
    
    static_tall_a CoreTall1
    static_tall_b CoreTall2
    
    debris Debris9
    
    

    event_piece_frame core
    
    global_objects {
        Lighting {
            ambient .6
        }
    }

    global_particles [Embers CoreHeatWave_Distortion]

    reverb {
        battle {
            preset Cave
            amount .65
            volume_adjustment 1.50
            DecayTime 1.8
        }
    }
}
```

---

### `moon`
**Source:** `tilesets.gon`  

```
moon {
    combat_background MoonBG
    combat_ui_background MoonUI
    
    static_1x1_a MoonObjects1
    static_1x1_b MoonObjects2
    static_1x1_c MoonObjects2
    
    static_2x2_a Moon2x2
    static_2x2_b Moon2x22
    
    static_tall_a MoonTall1
    static_tall_b MoonTall2
    
    debris Debris10

    event_piece_frame moon
    global_objects {

    }

    reverb {
        battle {
            preset Forest
            amount .35
            ReverbDelay .45
            DecayTime 1.68
            volume_adjustment 1.5
        }
    }
}
```

---

### `lab`
**Source:** `tilesets.gon`  

```
lab {
    combat_background LabBG
    combat_ui_background LabUI
    
    static_1x1_a LabObjects1
    static_1x1_b Labobjects2
    static_1x1_c LabObjects1
    
    static_2x2_a Lab2x2
    static_2x2_b Moon2x22
    
    static_tall_a Labtall1
    static_tall_b Labtall2
    
    debris Debris11

    event_piece_frame lab
    global_objects {

    }
    
    global_objects {
        Lighting {
            ambient .4

            smallrays [4, 8]
            bigrays [0, 0]

            smallray_clip labligtht
        }
        
        Cockroach {
            count [10 20]
        }
    }

    reverb {
        battle {
            preset Cave
            amount .65
            volume_adjustment 1.50
            DecayTime 1.8
        }
    }
}
```

---

### `house`
**Source:** `tilesets.gon`  

```
house {
    combat_background HouseBG
    combat_ui_background UI_Background2
    
    static_1x1_a Rubble
    static_1x1_b Bricks
    static_1x1_c Bricks
    
    static_2x2_a Dumpster
    static_2x2_b Dumpster
    
    static_tall_a PowerPole
    static_tall_b PhoneBooth
    
    debris Debris

    event_piece_frame house

    global_objects {
        Fly {
            count [0 20]
        }
    }

    reverb {
        battle {
            preset Alley
            amount .35
            ReverbDelay .2
            volume_adjustment 1.3
        }
    }
}
```

---

### `iceage`
**Source:** `tilesets.gon`  

```
iceage {
    combat_background IceageBG
    combat_ui_background UI_Background_Iceage
    
    static_1x1_a Iceageobjects1
    static_1x1_b IceageObjects2
    static_1x1_c Iceageobjects1
    
    static_2x2_a Iceage2x2
    static_2x2_b Dumpster
    
    static_tall_a Iceagetall1
    static_tall_b Iceagetall2
    
    debris Debris12

    event_piece_frame iceage

    global_objects {
        Lighting {
            ambient .8
            bigrays [1, 1]
            smallrays [1, 2]
        }

    }
    global_particles [CaveDrip]

    reverb {
        battle {
            preset Forest
            amount .65
            volume_adjustment 1.50
            DecayTime 1.8
            volume_adjustment 1.5
        }
    }
}
```

---

### `tutorial`
**Source:** `tilesets.gon`  

```
tutorial {
    combat_background thepathBG
    combat_ui_background UI_tutoral
    
    static_1x1_a Pathrubble
    static_1x1_b Bricks
    static_1x1_c Bricks
    
    static_2x2_a thepath2x2
    static_2x2_b Dumpster
    
    static_tall_a PowerPole
    static_tall_b PhoneBooth
    
    debris Debris

    event_piece_frame tutorial

    global_objects {
        Fly {
            count [0 20]
        }
    }
}
```

---

### `jurassic`
**Source:** `tilesets.gon`  

```
jurassic {
    combat_background dinolandBG
    combat_ui_background UI_Background_Dino
    
    static_1x1_a Dinoobjects
    static_1x1_b Dinoobjects
    static_1x1_c Dinoobjects
    
    static_2x2_a dino2x2
    static_2x2_b Dumpster
    
    static_tall_a dinolandtall1
    static_tall_b dinolandtall0
    
    debris dinodebris

    event_piece_frame jurassic

    global_objects {
    }
}
```

---

### `future`
**Source:** `tilesets.gon`  

```
future {
    combat_background futureBG
    combat_ui_background UI_Future
    
    static_1x1_a Futureobjects
    static_1x1_b Futureobjects2
    static_1x1_c Futureobjects
    
    static_2x2_a future2x2
    static_2x2_b Dumpster
    
    static_tall_a futuretall1
    static_tall_b futuretall
    
    debris futuredebris

    event_piece_frame future

    global_objects {
    }
}
```

---

### `theend`
**Source:** `tilesets.gon`  

```
theend {
    combat_background theendBG
    combat_ui_background UI_End
    
    static_1x1_a Endobjects
    static_1x1_b Endobjects
    static_1x1_c Endobjects
    
    static_2x2_a End2x2
    static_2x2_b Dumpster
    
    static_tall_a endtall1
    static_tall_b Endt
    
    debris enddebris

    water_alt_tile BloodTile
    water_alt_shroud BloodShroud
    water_alt_shader blood

    event_piece_frame theend

    global_objects {
        Lighting {
            ambient .7
            bigrays [1, 1]
            smallrays [1, 2]
        }
        Cockroach {
            count [10 20]
        }    
        Fly {
            count [10 20]
        }
    }
    global_particles [CaveDrip]
}
```

---

### `meatworld`
**Source:** `tilesets.gon`  

```
meatworld {
    combat_background meatBGpulsing
    combat_ui_background UI_Meat
    background_extra_shader meatpulse
    background_shader meatpulse_ground
    
    static_1x1_a Meatobjects
    static_1x1_b Meatobjects2
    static_1x1_c Meatobjects
    
    static_2x2_a Meat2x2
    static_2x2_b Dumpster
    
    static_tall_a Meatt
    static_tall_b meattall1

    water_alt_tile BloodTile
    water_alt_shroud BloodShroud
    water_alt_shader blood
    
    debris meatdebris

    event_piece_frame meatworld

    global_objects {
        Lighting {
            ambient .6
        }
    }

    global_particles [MeatCaveDrip, CoreHeatWave_Distortion, Mist]

    reverb {
        battle {
            preset Cave
            amount .65
            volume_adjustment 1.50
            DecayTime 1.8
        }
    }
}
```

---

### `therift`
**Source:** `tilesets.gon`  

```
therift {
    combat_background theriftBG
    combat_ui_background UI_Rift
    //battlefield_postprocess_effect glitchvignette
    
    static_1x1_a Riftobjects
    static_1x1_b Riftobjects
    static_1x1_c Riftobjects
    
    static_2x2_a Rift2x2
    static_2x2_b Dumpster
    
    static_tall_a rifttall1
    static_tall_b Riftt
    
    debris riftdebris

    event_piece_frame therift

    global_particles [GlitchShards]

    global_objects {
    }
}
```

---

### `theinfinite`
**Source:** `tilesets.gon`  

```
theinfinite {
    combat_background infiniteBG
    combat_ui_background UI_Infinite
    
    static_1x1_a Infiniteobjects
    static_1x1_b Infiniteobjects2
    static_1x1_c Infiniteobjects
    
    static_2x2_a Infinite2x2
    static_2x2_b Dumpster
    
    static_tall_a infinitetall1
    static_tall_b infinitetall1
    
    debris infinitedebris

    event_piece_frame theinfinite

    global_particles [AngelClouds]

    global_objects {
    }
}
```

---

### `finalboss`
**Source:** `tilesets.gon`  

```
finalboss {
    combat_background finalbossBG
    combat_ui_background UI_FinalBoss
    background_extra_shader crazyeye
    
    static_1x1_a Infiniteobjects
    static_1x1_b Infiniteobjects2
    static_1x1_c Infiniteobjects
    
    static_2x2_a Infinite2x2
    static_2x2_b Dumpster
    
    static_tall_a infinitetall1
    static_tall_b infinitetall1
    
    debris infinitedebris

    event_piece_frame theinfinite

    global_particles [AngelClouds]

    global_objects {
        Lighting {
            ambient .7
        }
    }
}
```

---

