# World and Events/House and Environment Directory

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

## File: `house_weather.gon`

### `Forecast`
**Source:** `house_weather.gon`  

```
Forecast [ //the first and last week of each month's odds are blended with the next month
    { //Winter 2 (January)
		None 14
		Snow 1
	}
	{ //Winter 3
		None 14
		Snow 1
	}
	{ //Spring 1 (March)
		None 14
		Rain 1
	}
	{ //Spring 2
		None 14
		Rain 1
	}
	{ //Spring 3
		None 14
		Rain 1
	}
	{ //Summer 1 (June)
		None 14
		Thunderstorm 1
	}
	{ //Summer 2
		None 14
		Thunderstorm 1
	}
	{ //Summer 3
		None 14
		Thunderstorm 1
	}
	{ //Autumn 1 (September)
		None 14
		Windy 1
	}
	{ //Autumn 2
		None 14
		Windy 1
	}
	{ //Autumn 3
		None 14
		Windy 1
	}
	{ //Winter 1 (December)
		None 14
		Snow 1
	}
]
```

---

### `Weather`
**Source:** `house_weather.gon`  

```
Weather {
	Rain {
		adventure_weather Rain
		ambient_sound amb_rain.ogg
		particles [Rain]
		prewarm 5
		skybox_frame day_rain
	}
	Thunderstorm {
		adventure_weather Thunderstorm
		ambient_sound amb_heavyrain.ogg
		particles [Thunderstorm]
		prewarm 5
		lightning_fx true
		skybox_frame day_thunderstorm
	}
	Windy {
		adventure_weather Windy
		ambient_sound amb_windy.ogg
		particles [WindFull]
		prewarm 5
		skybox_frame day_windy
	}
	Snow {
		adventure_weather Snow
		ambient_sound amb_snow.ogg
		particles [Snow]
		prewarm 20
		skybox_frame day_snow
	}
}
```

---

## File: `tiles.gon`

### `editor`
**Name:** Empty  
**Source:** `tiles.gon`  

```
editor {
        image "empty.png"
        name "Empty"
    }
```

---

### `editor`
**Name:** Water  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [blue blue]
        paint true
        name "Water"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Grass  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [green green]
        paint true
        name "Grass"
        tile_layer 0
    }
```

---

### `tile`
**Source:** `tiles.gon`  

```
tile {
        GrassTile 80
        TallGrassTile 15
        BlankTile 5
    }
```

---

### `editor`
**Name:** Tall Grass  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [[0,.5,0], [0,.5,0]]
        paint true
        name "Tall Grass"
        tile_layer 0
    }
```

---

### `tile`
**Source:** `tiles.gon`  

```
tile {
        GrassTile 15
        TallGrassTile 80
        BlankTile 5
    }
```

---

### `editor`
**Name:** Fire  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [red red]
        paint true
        name "Fire"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Ice  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [cyan cyan]
        paint true
        name "Ice"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Lava  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [orange red]
        paint true
        name "Lava"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Metal  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [grey grey]
        paint true
        name "Metal"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Rock  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [brown black]
        paint true
        name "Rock"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Creep  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [purple purple]
        paint true
        name "Creep"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Oil  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [orange yellow]
        paint true
        name "Oil"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Toxic Sludge  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [green yellow]
        paint true
        name "Toxic Sludge"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Shadow  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [black none]
        paint true
        name "Shadow"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Glass Shards  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [none none]
        paint true
        name "Glass Shards"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Snow  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [none cyan]
        paint true
        name "Snow"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Water with current  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png" "north_arrow.png"]
        image_tint [blue blue none]
        paint true
        name "Water with current"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Water with current  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png" "south_arrow.png"]
        image_tint [blue blue none]
        paint true
        name "Water with current"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Water with current  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png" "east_arrow.png"]
        image_tint [blue blue none]
        paint true
        name "Water with current"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Water with current  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png" "west_arrow.png"]
        image_tint [blue blue none]
        paint true
        name "Water with current"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Dirt  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [brown brown]
        paint true
        name "Dirt"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Stalagmites  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [none brown]
        paint true
        name "Stalagmites"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Road Tile  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [grey yellow]
        paint true
        name "Road Tile"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Brambles  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [green black]
        paint true
        name "Brambles"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Flowers  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [green pink]
        paint true
        name "Flowers"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Tall Flower Tile  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [green purple]
        paint true
        name "Tall Flower Tile"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Supercooled Water Tile  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_spots.png"]
        image_tint [blue cyan]
        paint true
        name "Supercooled Water Tile"
        tile_layer 0
    }
```

---

### `editor`
**Name:** Glitch Tile  
**Source:** `tiles.gon`  

```
editor {
        category -100
        subcategory 4
        image ["ground.png" "ground_shards.png"]
        image_tint [black grey]
        paint true
        name "Glitch Tile"
        tile_layer 0
    }
```

---

## File: `weather.gon`

### `None`
**Name:** Clear Skies  
**Description:** There are no weather effects.  
**Source:** `weather.gon`  

```
None {
    name "WEATHER_NONE_NAME"
    desc "WEATHER_NONE_DESC"
}
```

---

### `Fog`
**Name:** Fog  
**Description:** All attacks and abilities have a +10% chance to miss.  
**Source:** `weather.gon`  

```
Fog {
    name "WEATHER_FOG_NAME"
    desc "WEATHER_FOG_DESC"
    
    effects {
        Fog 1
    }
}
```

---

### `Rain`
**Name:** Rain  
**Description:** Persistent Water Element.  
**Source:** `weather.gon`  

```
Rain {
    name "WEATHER_RAIN_NAME"
    desc "WEATHER_RAIN_DESC"

    ambient_sound amb_rain.ogg
   
    hint_persistent_elements [Water]
    effects {
        Rain 1
    }
}
```

---

### `HeavyRain`
**Name:** Heavy Rain  
**Description:** Persistent Water Element. There are extra water tiles in every battle.  
**Source:** `weather.gon`  

```
HeavyRain {
    name "WEATHER_HEAVYRAIN_NAME"
    desc "WEATHER_HEAVYRAIN_DESC"

    ambient_sound amb_heavyrain.ogg
    
    hint_persistent_elements [Water]
    effects {
        Rain 2
        SpawnExtraThingsOnBattleStart {
            tile WaterTile
            number [12 20]
        }
    }
}
```

---

### `Windy`
**Name:** Windy  
**Description:** At the end of each round, wind blows everything 1 space in a random direction.  
**Source:** `weather.gon`  

```
Windy {
    name "WEATHER_WINDY_NAME"
    desc "WEATHER_WINDY_DESC"
    
    ambient_sound amb_windy.ogg

    hint_persistent_elements [Wind]
    effects {
        Windy 1
    }
}
```

---

### `Sandstorm`
**Name:** Sandstorm  
**Description:** At the end of each round, damages everything by 1.  
**Source:** `weather.gon`  

```
Sandstorm {
    name "WEATHER_SANDSTORM_NAME"
    desc "WEATHER_SANDSTORM_DESC"
    
    ambient_sound amb_sandstorm.ogg

    effects {
        Sandstorm 1
    }
}
```

---

### `Overgrowth`
**Name:** Overgrowth  
**Description:** There are extra tall grass and bramble tiles in every battle.  
**Source:** `weather.gon`  

```
Overgrowth {
    name "WEATHER_OVERGROWTH_NAME"
    desc "WEATHER_OVERGROWTH_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            tile BrambleTile
            number [2 5]
        }
        SpawnExtraThingsOnBattleStart {
            tile TallGrassTile
            number [2 5]
        }
    }
}
```

---

### `Earthquake`
**Name:** Earthquake  
**Description:** There was an earthquake! Objects in each battle have been destroyed and there are rocks everywhere!  
**Source:** `weather.gon`  

```
Earthquake {
    name "WEATHER_EARTHQUAKE_NAME"
    desc "WEATHER_EARTHQUAKE_DESC"
    
    effects {
        DeleteInanimateObjectsChance 25%

        SpawnExtraThingsOnBattleStart {
            object SmallRock
            number [3 5]
        }
        SpawnExtraThingsOnBattleStart {
            object Boulder
            number [0 2]
        }
    }
}
```

---

### `Wildfire`
**Name:** Wildfire  
**Description:** There is fire everywhere!  
**Source:** `weather.gon`  

```
Wildfire {
    name "WEATHER_WILDFIRE_NAME"
    desc "WEATHER_WILDFIRE_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            tile FireTile
            number [3 8]
        }
    }
}
```

---

### `HeatWave`
**Name:** Heat Wave  
**Description:** Cats do not heal after battle. All heals are reduced by 1. Can be mitigated with water.  
**Source:** `weather.gon`  

```
HeatWave {
    name "WEATHER_HEATWAVE_NAME"
    desc "WEATHER_HEATWAVE_DESC"
    
    hint_persistent_elements [Heat]
    effects {
        HeatWave 1
    }
}
```

---

### `Snow`
**Name:** Snow  
**Description:** Persistent Ice Element.  
**Source:** `weather.gon`  

```
Snow {
    name "WEATHER_SNOW_NAME"
    desc "WEATHER_SNOW_DESC"

    ambient_sound amb_snow.ogg
    
    hint_persistent_elements [Ice]
    effects {
        Snow 1
    }
}
```

---

### `AcidRain`
**Name:** Acid Rain  
**Description:** At the end of each round, damages everything by 2 with a chance to lower a random stat as well.  
**Source:** `weather.gon`  

```
AcidRain {
    name "WEATHER_ACIDRAIN_NAME"
    desc "WEATHER_ACIDRAIN_DESC"
    
    ambient_sound amb_acidrain.ogg

    effects {
        AcidRain 2
    }
}
```

---

### `MeteorShower`
**Name:** Meteor Shower  
**Description:** After each turn there's a chance for a flaming meteor to fall onto a random tile.  
**Source:** `weather.gon`  

```
MeteorShower {
    name "WEATHER_METEORS_NAME"
    desc "WEATHER_METEORS_DESC"
    
    effects {
        MeteorShower 25%
    }
}
```

---

### `Thunderstorm`
**Name:** Thunderstorm  
**Description:** Persistent Water Element. At the end of each round, wind blows everything 1 space in a random direction. After each turn, there's a chance for a random lightning strike.  
**Source:** `weather.gon`  

```
Thunderstorm {
    name "WEATHER_THUNDERSTORM_NAME"
    desc "WEATHER_THUNDERSTORM_DESC"
    
    ambient_sound amb_thunderstorm.ogg

    hint_persistent_elements [Water Wind]
    effects {
        Rain 1
        RandomLightning 50%
        Windy 1
    }
}
```

---

### `FlashFlood`
**Name:** Flash Flood  
**Description:** Persistent Water Element. There are a ton of extra water tiles in every battle.  
**Source:** `weather.gon`  

```
FlashFlood {
    name "WEATHER_FLASHFLOOD_NAME"
    desc "WEATHER_FLASHFLOOD_DESC"
    
    ambient_sound amb_rain.ogg

    hint_persistent_elements [Water]
    effects {
        Rain 4
        SpawnExtraThingsOnBattleStart {
            tile WaterTile
            number [40 60]
        }
    }
}
```

---

### `TrashDay`
**Name:** Trash Day  
**Description:** There is extra junk in every battle.  
**Source:** `weather.gon`  

```
TrashDay {
    name "WEATHER_TRASHDAY_NAME"
    desc "WEATHER_TRASHDAY_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            object [Junk Junk TrashBag]
            number [3 6]
        }
    }
}
```

---

### `RainingFrogs`
**Name:** Raining Frogs  
**Description:** There are extra neutral frogs in every battle.  
**Source:** `weather.gon`  

```
RainingFrogs {
    name "WEATHER_FROGS_NAME"
    desc "WEATHER_FROGS_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            object NeutralToad
            number [2 4]
        }
    }
}
```

---

### `PipeBlockage`
**Name:** Pipe Blockage  
**Description:** There is extra poop and sewage in every battle.  
**Source:** `weather.gon`  

```
PipeBlockage {
    name "WEATHER_BLOCKAGE_NAME"
    desc "WEATHER_BLOCKAGE_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            object Poop
            number [1 3]
        }
        SpawnExtraThingsOnBattleStart {
            tile CreepTile
            number [3 5]
        }
    }
}
```

---

### `PayDay`
**Name:** Pay Day  
**Description:** There are extra coins in every battle.  
**Source:** `weather.gon`  

```
PayDay {
    name "WEATHER_PAYDAY_NAME"
    desc "WEATHER_PAYDAY_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            object Coin
            number [5 10]
        }
    }
}
```

---

### `HuntingSeason`
**Name:** Hunting Season  
**Description:** There are extra bear traps in every battle.  
**Source:** `weather.gon`  

```
HuntingSeason {
    name "WEATHER_HUNTING_NAME"
    desc "WEATHER_HUNTING_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            trap BearTrap
            number [2 4]
        }
    }
}
```

---

### `RestlessDead`
**Name:** Restless Dead  
**Description:** Zombies spawn at the end of each round.  
**Source:** `weather.gon`  

```
RestlessDead {
    name "WEATHER_RESTLESS_NAME"
    desc "WEATHER_RESTLESS_DESC"
    
    effects {
        GlobalSpawnOnRoundEnd {
            object NeutralZombieKitten
        }
    }
}
```

---

### `FireflySwarm`
**Name:** Firefly Swarm  
**Description:** All allies have +2 luck.  
**Source:** `weather.gon`  

```
FireflySwarm {
    name "WEATHER_FIREFLY_NAME"
    desc "WEATHER_FIREFLY_DESC"
    
    effects {
        FireflySwarm 2
    }
}
```

---

### `ButterflySwarm`
**Name:** Butterfly Swarm  
**Description:** All allies have +2 luck.  
**Source:** `weather.gon`  

```
ButterflySwarm {
    name "WEATHER_BUTTERFLY_NAME"
    desc "WEATHER_BUTTERFLY_DESC"

    ambient_sound amb_butterflyswarm.ogg
    
    effects {
        ButterflySwarm 2
    }
}
```

---

### `FlySwarm`
**Name:** Fly Swarm  
**Description:** At the end of each turn, there's a chance to get bitten for 1 damage and 1 Bleed.  
**Source:** `weather.gon`  

```
FlySwarm {
    name "WEATHER_FLYSWARM_NAME"
    desc "WEATHER_FLYSWARM_DESC"

    ambient_sound amb_flyswarm.ogg
    
    effects {
        FlySwarm 50%
    }
}
```

---

### `VisualFlySwarm`
**Name:** Fly Swarm  
**Description:** There's lots of flies!  
**Source:** `weather.gon`  

```
VisualFlySwarm { //for Tormentor fight
    name "WEATHER_TORFLIES_NAME"
    desc "WEATHER_TORFLIES_DESC"

    ambient_sound amb_flyswarm.ogg
    
    effects {
        VisualFlySwarm 1
    }
}
```

---

### `LowGravity`
**Name:** Low Gravity  
**Description:** Jumps, throws, and projectile abilities have +2 range. All physical abilities have +1 Knockback. Other abilities that cause Knockback have +1 Knockback as well.  
**Source:** `weather.gon`  

```
LowGravity {
    name "WEATHER_LOWGRAV_NAME"
    desc "WEATHER_LOWGRAV_DESC"
    
    effects {
        LowGravityRangeBoost 2
        LowGravityKnockbackBoost 1
        ClearDefaultDebris 1
        AddTilesetObjects {
            FloatingDebris {
                count 20
            }
        }
    }
}
```

---

### `Firestorm`
**Name:** Firestorm  
**Description:** Persistent Fire Element. Fires no longer burn out. Parts of the map are on fire.  
**Source:** `weather.gon`  

```
Firestorm {
    name "WEATHER_FIRESTORM_NAME"
    desc "WEATHER_FIRESTORM_DESC"
    
    hint_persistent_elements [Fire]
    effects {
        FireStorm 0%
        SpawnExtraThingsOnBattleStart {
            tile FireTile
            number [2 5]
        }
    }
}
```

---

### `KaijuFirestorm`
**Name:** Firestorm  
**Description:** Persistent Fire Element. Fireballs occasionally rain down from the sky. Fires no longer burn out.  
**Source:** `weather.gon`  

```
KaijuFirestorm {
    name "WEATHER_KAIJUFIRE_NAME"
    desc "WEATHER_KAIJUFIRE_DESC"
    
    hint_persistent_elements [Fire]
    effects {
        FireStorm 33%
        LowerAmbientLight 50%
    }
}
```

---

### `Meteornado`
**Name:** Meteornado  
**Description:** At the end of each round, damages everything by 1 with a 33% chance to Bruise.  
**Source:** `weather.gon`  

```
Meteornado {
    name "WEATHER_METEORNADO_NAME"
    desc "WEATHER_METEORNADO_DESC"

    effects {
        Meteornado 1
    }
}
```

---

### `KaijuMeteornado`
**Name:** Meteornado  
**Description:** At the end of each round, damages everything by 1 with a 33% chance to Bruise.  
**Source:** `weather.gon`  

```
KaijuMeteornado {
    name "WEATHER_KAIJUMETEORNADO_NAME"
    desc "WEATHER_KAIJUMETEORNADO_DESC"

    effects {
        Meteornado 1
        LowerAmbientLight 33%
        SpecialGodRays {
            Big {
                position [4.5 4.5]
                follow_character_tag zaratana
            }
        }
    }
}
```

---

### `KaijuMeteornadoSolo`
**Name:** Meteornado  
**Description:** At the end of each round, damages everything by 1 with a 33% chance to Bruise.  
**Source:** `weather.gon`  

```
KaijuMeteornadoSolo {
    name "WEATHER_KAIJUMETEORSOLO_NAME"
    desc "WEATHER_KAIJUMETEORSOLO_DESC"

    effects {
        Meteornado 1
        LowerAmbientLight 50%
        SpecialGodRays {
            Big {
                position [4.5 4.5]
                follow_character_tag zaratana
            }
        }
    }
}
```

---

### `RobotUprising`
**Name:** Robot Uprising  
**Description:** 2-4 robots spawn in each battle. All robots have gone rogue!  
**Source:** `weather.gon`  

```
RobotUprising {
    name "WEATHER_ROBOTS_NAME"
    desc "WEATHER_ROBOTS_DESC"

    effects {
        FactionUprising robot

        SpawnExtraThingsOnBattleStart { //todo: would like to cluster these spawns together away from enemies or allies
            object [SecurityBot CopBot_Uprising Rover RoboTom]
            number 1
        }
        SpawnExtraThingsOnBattleStart { //todo: would like to cluster these spawns together away from enemies or allies
            object [Bombchu Deathbot RoboVacuum TinkererTurret]
            number [1 3]
        }
    }
}
```

---

### `HauntedNight`
**Name:** Haunted Night  
**Description:** 2-4 ghosts spawn in each battle. All ghosts have gone rogue!  
**Source:** `weather.gon`  

```
HauntedNight {
    name "WEATHER_HAUNTED_NAME"
    desc "WEATHER_HAUNTED_DESC"
    
    effects {
        FactionUprising ghost
        LowerAmbientLight 33%


        SpawnExtraThingsOnBattleStart { //todo: would like to cluster these spawns together away from enemies or allies
            object [Spookie Scary Tatters Wisp Wisp Wisp]
            number [2 4]
        }
    }
}
```

---

### `BirdMigration`
**Name:** Bird Migration  
**Description:** 1-2 extra birds spawn in each battle.  
**Source:** `weather.gon`  

```
BirdMigration {
    name "WEATHER_MIGRATION_NAME"
    desc "WEATHER_MIGRATION_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            object [Bird]
            number [1 2]
        }
    }
}
```

---

### `CockroachSwarm`
**Name:** Cockroach Infestation  
**Description:** All units have a 25% chance to start each battle with Fear or Poison.  
**Source:** `weather.gon`  

```
CockroachSwarm {
    name "WEATHER_COCKROACHES_NAME"
    desc "WEATHER_COCKROACHES_DESC"
    
    effects {
        CockroachSwarm 1

        CharacterTypeGainsStatusAtBattleStart {
            tag any

            Conditional_Flying {
            } Else { //only to things actually on the ground
                Fear [1 .25]
                Poison [1 .25]
            }
        }
    }
}
```

---

### `JudgementDay`
**Name:** Judgement Day  
**Description:** Some tiles will get Raptured at the end of each round during the battle. More tiles are affected every round.  
**Source:** `weather.gon`  

```
JudgementDay {
    name "WEATHER_JUDGEMENT_NAME"
    desc "WEATHER_JUDGEMENT_DESC"
    
    effects {
        JudgementDay 25
    }
}
```

---

### `Pandemonium`
**Name:** Pandemonium  
**Description:** All units have a 25% chance to have Madness each round.  
**Source:** `weather.gon`  

```
Pandemonium {
    name "WEATHER_PANDEMONIUM_NAME"
    desc "WEATHER_PANDEMONIUM_DESC"
    
    effects {
        StatusCharactersOnRoundStart {
            Madness [1 .25]
        }
    }
}
```

---

### `TheHollowing`
**Name:** The Hollowing  
**Description:** At the end of the round, each corpse has a 25% chance to revive at half health with Madness 5.  
**Source:** `weather.gon`  

```
TheHollowing {
    name "WEATHER_HOLLOWING_NAME"
    desc "WEATHER_HOLLOWING_DESC"
    
    effects {
        StatusCharactersOnRoundEnd {
            Conditional_GoodRoll {
                odds 25%
                Conditional_Corpse {
                    Revive 50%
                    Madness 5
                }
            }
        }
    }
}
```

---

### `OilSpill`
**Name:** Oil Spill  
**Description:** A puddle of tar appears in each battle.  
**Source:** `weather.gon`  

```
OilSpill {
    name "WEATHER_OILSPILL_NAME"
    desc "WEATHER_OILSPILL_DESC"
    
    effects {
        SpawnTilePuddleOnBattleStart {
            tile OilTile
            min_radius 1.5
            max_radius 3.5
        }
    }
}
```

---

### `Blizzard`
**Name:** Blizzard!  
**Description:** Persistent Ice Element. At the end of each round, wind blows everything 1 space in a random direction. After each turn, there's a chance for a random lightning strike.  
**Source:** `weather.gon`  

```
Blizzard {
    name "WEATHER_BLIZZARD_NAME"
    desc "WEATHER_BLIZZARD_DESC"

    ambient_sound amb_blizzard.ogg

    hint_persistent_elements [Ice Wind]
    effects {
        Snow 1
        RandomLightning 50%
        Windy 1
    }
}
```

---

### `Hurricane`
**Name:** Hurricane!  
**Description:** At the end of each round, wind blows everything 10 spaces in a random direction.  
**Source:** `weather.gon`  

```
Hurricane {
    name "WEATHER_HURRICANE_NAME"
    desc "WEATHER_HURRICANE_DESC"

    ambient_sound amb_windy.ogg

    hint_persistent_elements [Wind]
    effects {
        Windy 10
    }
}
```

---

### `StrangeSpikes`
**Name:** Strange Spikes!  
**Description:** At the end of the round, all units gain +1 Thorns.  
**Source:** `weather.gon`  

```
StrangeSpikes {
    name "WEATHER_STRANGESPIKES_NAME"
    desc "WEATHER_STRANGESPIKES_DESC"

    effects {
        StatusCharactersOnRoundEnd {
            Thorns 1
        }
    }
}
```

---

### `BlessedDay`
**Name:** Blessed Day!  
**Description:** All units have +3 Health Regen. Persistent Holy Element.  
**Source:** `weather.gon`  

```
BlessedDay {
    name "WEATHER_BLESSED_NAME"
    desc "WEATHER_BLESSED_DESC"

    hint_persistent_elements [Holy]
    effects {
        PersistentElement Holy
        GlobalHealthRegenAura 3
    }
}
```

---

### `StealthMission`
**Name:** Stealth Mission  
**Description:** All units gain Stealth at the start of the battle.  
**Source:** `weather.gon`  

```
StealthMission {
    name "WEATHER_STEALTH_NAME"
    desc "WEATHER_STEALTH_DESC"
    
    effects {
        CharacterTypeGainsStatusAtBattleStart {
            tag any
            Stealth 1
        }
    }
}
```

---

### `Infestation`
**Name:** Infestation  
**Description:** All non-tiny units explode into a charmed maggot when they die.  
**Source:** `weather.gon`  

```
Infestation {
    name "WEATHER_INFESTATION_NAME"
    desc "WEATHER_INFESTATION_DESC"

    effects {
        StatusAllCharactersOnSpawn {
            Conditional_Tiny {
            } Else {
                AllyInfested {
                    object CharmedMaggot
                    faction allies
                }
            }
        }
    }
}
```

---

### `Eruption`
**Name:** Eruption  
**Description:** A mini volcano spawns in each battle.  
**Source:** `weather.gon`  

```
Eruption {
    name "WEATHER_ERUPTION_NAME"
    desc "WEATHER_ERUPTION_DESC"
    
    effects {
        SpawnVolcanoOnBattleStart {
            object MiniVolcano
            puddle_tile LavaTile
            min_radius .2
            max_radius 2.2
        }
    }
}
```

---

### `Drugs`
**Name:** Drug Awareness Day  
**Description:** There is extra catnip in every battle. Find a random pill after every battle.  
**Source:** `weather.gon`  

```
Drugs {
    name "WEATHER_DRUGS_NAME"
    desc "WEATHER_DRUGS_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            object RandomCatnipPickup
            number [4 6]
        }
        FindExtraItemFromPoolOnBattleEnd pills
    }
}
```

---

### `TrainingDay`
**Name:** Training Day  
**Description:** A punching bag with Kinetic Spikes 5 spawns in each battle.  
**Source:** `weather.gon`  

```
TrainingDay {
    name "WEATHER_TRAININGDAY_NAME"
    desc "WEATHER_TRAININGDAY_DESC"
    
    effects {
        SpawnVolcanoOnBattleStart {
            object PunchingBag
        }
    }
}
```

---

### `Tornado`
**Name:** Tornadoes  
**Description:** Twisters spawn each round.  
**Source:** `weather.gon`  

```
Tornado {
    name "WEATHER_TORNADOES_NAME"
    desc "WEATHER_TORNADOES_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            object NeutralTwister
            number [1 2]
        }
        GlobalSpawnOnRoundEnd {
            object NeutralTwister
            number [1 2]
        }
    }
}
```

---

### `CrazyWeather`
**Name:** Crazy Weather  
**Description:** The weather around here is crazy! It's different every battle!  
**Source:** `weather.gon`  

```
CrazyWeather {
    name "WEATHER_CRAZY_NAME"
    desc "WEATHER_CRAZY_DESC"
    
    effects {
        //TODO: this needs to set ambient sounds correctly also
        RandomWeatherEachFight [Fog Rain Windy Sandstorm HeatWave Snow Thunderstorm Blizzard Tornado] //todo: hailstorm too
    }
}
```

---

### `BountyHunting`
**Name:** Bounty Hunting  
**Description:** A random unit in each battle has a bounty. A Bounty Hunter is here to collect.  
**Source:** `weather.gon`  

```
BountyHunting {
    name "WEATHER_BOUNTY_NAME"
    desc "WEATHER_BOUNTY_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            object EventBountyHunter
        }
    }
}
```

---

### `Minesweeper`
**Name:** Minesweeper  
**Description:** There are extra land mines in every battle.  
**Source:** `weather.gon`  

```
Minesweeper {
    name "WEATHER_MINESWEEPER_NAME"
    desc "WEATHER_MINESWEEPER_DESC"
    
    effects {
        SpawnExtraThingsOnBattleStart {
            trap LandMine
            number [2 4]
        }
    }
}
```

---

### `AlienInvasion`
**Name:** Alien Invasion  
**Description:** 2-4 aliens spawn in each battle. Aliens are invading!  
**Source:** `weather.gon`  

```
AlienInvasion {
    name "WEATHER_ALIENS_NAME"
    desc "WEATHER_ALIENS_DESC"

    effects {
        FactionUprising alien

        SpawnExtraThingsOnBattleStart { //todo: would like to cluster these spawns together away from enemies or allies
            object [SmallUFO SmallUFO SmallUFO YellowBlaster GreyAlien GreenProber]
            number [2 3]
        }
        SpawnExtraThingsOnBattleStart { //todo: would like to cluster these spawns together away from enemies or allies
            object [BigUFO]
            number [-2 1] //33% chance of a big ufo
        }
    }
}
```

---

### `Birdemic`
**Name:** Birdemic  
**Description:** 2-4 birds spawn in each battle. All birds are stronger, and angry!  
**Source:** `weather.gon`  

```
Birdemic {
    name "WEATHER_BIRDEMIC_NAME"
    desc "WEATHER_BIRDEMIC_DESC"

    effects {
        FactionUprising {
            tag bird

            extra_statuses { //cancel the -999 bonus bird initiative
                Conditional_HasTag {
                    tag bonusbird

                    ApplyPassives {
                        AddInitiative 999
                    }
                    AddExtraTurnsBeforeRun 2
                }
                AllStatsUp 2
                HealthGain 8 //fill up the blank max health
            }
        }

        SpawnExtraThingsOnBattleStart {
            object [Bird] //todo: would like to cluster these spawns together away from enemies or allies
            number [2 4]
        }
    }
}
```

---

### `SolarFlare`
**Name:** Solar Flare  
**Description:** A solar flare strikes a large area at the end of each round, Burning and inflicting Blind.  
**Source:** `weather.gon`  

```
SolarFlare {
    name "WEATHER_SOLARFLARE_NAME"
    desc "WEATHER_SOLARFLARE_DESC"

    effects {
        SolarFlare {
            damage 5

            effects {
                Burn 3
                Blind 3
            }
            elements [
                Fire
            ]
        }
    }
}
```

---

### `GeomagneticStorm`
**Name:** Geomagnetic Storm  
**Description:** All rocks levitate at the end of the round. Extra rocks spawn in each battle.  
**Source:** `weather.gon`  

```
GeomagneticStorm {
    name "WEATHER_GEOMAGSTORM_NAME"
    desc "WEATHER_GEOMAGSTORM_DESC"

    effects {
        StatusCharactersOnRoundEnd {
            tag_filter rock
            FloatingRockTrap 1
        }
        SpawnExtraThingsOnBattleStart {
            object SmallRock
            number [1 3]
        }
        SpawnExtraThingsOnBattleStart {
            object Boulder
            number [0 2]
        }
    }
}
```

---

### `TheShimmer`
**Name:** The Shimmer  
**Description:** All units gain a random status effect at the start of each round. Cats gain a random mutation at the end of each battle.  
**Source:** `weather.gon`  

```
TheShimmer {
    name "WEATHER_SHIMMER_NAME"
    desc "WEATHER_SHIMMER_DESC"

    effects {
        AddPostProcessEffect {
            shader shimmervignette
            requires_framebuffer false
        }

        StatusCharactersOnRoundStart {
            Conditional_GoodRoll { //so luck matters
                odds .5

                RandomStatusFromPool {
                    //positive
                        RandomStatUp 1
                        RandomStatUp 1
                        RandomStatUp 1
                        RandomStatUp 1

                        Brace 1
                        Shield 1
                        DivineShield 1
                        SpellDamageUp 1
                        DamageUp 1
                        Thorns 1
                        KineticSpikes 1
                }

            } Else {
                RandomStatusFromPool {
                    //negative
                        RandomStatDown 1
                        RandomStatDown 1
                        RandomStatDown 1
                        RandomStatDown 1

                        Poison 1
                        Bruise 1
                        Bleed 1
                        Weakness 1
                        Blind 1
                        Drowsy 1
                        Slow 1
                }
            }
        }

        StatusAllCharactersOnSpawn {
            Conditional_PartyMember {
                ApplyPassives {
                    StatusOnBattleEnd {
                        RandomMutation 1
                    }
                }
            }
        }
    }
}
```

---

### `StrangeEggs`
**Name:** Strange Eggs  
**Description:** 3-6 strange eggs spawn in each battle. Kill them before they hatch!  
**Source:** `weather.gon`  

```
StrangeEggs {
    name "WEATHER_STRANGEEGGS_NAME"
    desc "WEATHER_STRANGEEGGS_DESC"

    effects {
        SpawnExtraThingsOnBattleStart {
            object AlienEgg
            number [3 6]
        }
    }
}
```

---

### `AlienOvergrowth`
**Name:** Alien Overgrowth  
**Description:** A few bramble patches spawn in each battle, but something is strange about them...  
**Source:** `weather.gon`  

```
AlienOvergrowth {
    name "WEATHER_ALIENOVERGROWTH_NAME"
    desc "WEATHER_ALIENOVERGROWTH_DESC"

    effects {
        SpawnVolcanoOnBattleStart {
            object Sprout
            puddle_tile [BrambleTile TallBrambleTile]
            min_radius 1
            max_radius 2.2

            number [3 5]
        }
    }
}
```

---

