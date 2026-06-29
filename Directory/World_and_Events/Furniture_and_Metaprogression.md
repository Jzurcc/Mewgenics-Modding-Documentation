# World and Events/Furniture and Metaprogression Directory

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

## File: `house.gon`

### `rooms`
**Source:** `house.gon`  

```
rooms {
	Floor1_Large {
		width 16
		height 7

		movieclip RoomBackgroundLargeF1
		interstitial_bg_frame room1

		reverb_empty {
			preset STONEROOM
			amount .65
            volume_adjustment 2
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
	Floor1_Small {
		width 16
		height 7

		movieclip RoomBackgroundSmallF1
		interstitial_bg_frame room2

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
	SmallAttic {
		id Attic
		width 18
		height 5

		movieclip RoomBackgroundSmallAttic
		interstitial_bg_frame attic

		extra_bound_planes [
			{
				p [0 0]  
				n [1 -2]
			}
			{
				p [18 0] 
				n [-1 -2]
			}
		]

		//0: empty, 1: solid, 2: attachable solid, 6: out of bounds, 7: semi out of bounds (cat can be here, furniture cant)
		built_in_collision [ //this is 2 larger than specified dimensions cause theres normally a blue (2) border added
							 [6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6]
							 [6 6 6 6 6 6 6 6 6 8 8 6 6 6 6 6 6 6 6 6]
						     [6 6 6 6 6 6 6 8 7 0 0 7 8 6 6 6 6 6 6 6]
							 [6 6 6 6 6 8 7 0 0 0 0 0 0 7 8 6 6 6 6 6]
							 [6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6]
							 [6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6]
							 [6 8 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 8 6]
		                   ]

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
	LargeAttic {
		id Attic
		width 35
		height 9

		movieclip RoomBackgroundAttic
		interstitial_bg_frame attic

		extra_bound_planes [
			{
				p [0 0]  
				n [1 -2]
			}
			{
				p [35 0] 
				n [-1 -2]
			}
		]

		//0: empty, 1: solid, 2: attachable solid, 6: out of bounds, 8: out of bounds but still visualize it
		built_in_collision [ //this is 2 larger than specified dimensions cause theres normally a blue (2) border added
							 [6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6]
							 [6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 8 7 8 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6]
							 [6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 8 7 0 0 0 7 8 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6]
							 [6 6 6 6 6 6 6 6 6 6 6 6 6 8 7 0 0 0 0 0 0 0 7 8 6 6 6 6 6 6 6 6 6 6 6 6 6]
							 [6 6 6 6 6 6 6 6 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 6 6 6 6 6 6 6 6]
							 [6 6 6 6 6 6 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 6 6 6 6 6 6]
						     [6 6 6 6 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 6 6 6 6]
							 [6 6 6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6 6 6]
							 [6 6 6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6 6 6]
							 [6 8 7 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 7 8 6]
							 [6 8 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 8 6]
		                   ]

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
	Floor2_Large {
		width 16
		height 7

		movieclip RoomBackgroundLargeF2
		interstitial_bg_frame room3

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
	Floor2_Small {
		width 16
		height 7

		movieclip RoomBackgroundSmallF2
		interstitial_bg_frame room4

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}

	Basement0 { //basement
		width 33
		height 5

		movieclip RoomBackgroundBasement0
		//bounds_ignored_for_zoomout true

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
	Basement1 { //caves
		width 33
		height 5

		movieclip RoomBackgroundBasement1
		//bounds_ignored_for_zoomout true

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
	Basement2 { //depths
		width 33
		height 5

		movieclip RoomBackgroundBasement2
		//bounds_ignored_for_zoomout true

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
	Basement3 { //womb
		width 33
		height 5

		movieclip RoomBackgroundBasement3
		//bounds_ignored_for_zoomout true

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
	Basement4 { //sheol
		width 33
		height 5

		movieclip RoomBackgroundBasement4
		//bounds_ignored_for_zoomout true

		reverb_empty {
			preset AUDITORIUM
			amount .65
            volume_adjustment 1.50
		}
		reverb_full {
			preset LIVINGROOM
			amount .25
		}
	}
}
```

---

### `houses`
**Source:** `house.gon`  

```
houses {
	House1 {
		movieclip_bg HouseBackground1
		movieclip_fg HouseForeground1
		bg_placements_frame small
		zoomout_catvolume .8

		room_positions {
			Floor1_Large [1, 1]
			SmallAttic [0, 9]
		}

		aux_positions {
			ButchBox [21, 0]
			StraySpawn [-3 0]
			HousePipe [-2 0]

			Roof_LeftEdge [-3.388 8.138]
			Roof_Top [8.983 14.4]
			Roof_RightEdge [21.548 8.175]
		}
	}

	House2 {
		movieclip_bg HouseBackground2
		movieclip_fg HouseForeground2
		bg_placements_frame large
		zoomout_catvolume .7

		room_positions {
			Floor1_Large [1, 1]
			Floor1_Small [18, 1]
			LargeAttic [0, 9]

			Basement0 [1 -6]
			Basement1 [1 -12]
			Basement2 [1 -18]
			Basement3 [1 -24]
			Basement4 [1 -30]
		}

		aux_positions {
			ButchBox [38, 0]
			StraySpawn [-3 0]
			HousePipe [-2 0]

			Roof_LeftEdge [-3.617 8.112]
			Roof_Top [17.563 18.677]
			Roof_RightEdge [38.518 8.207]
		}
	}

	House3 {
		movieclip_bg HouseBackground3
		movieclip_fg HouseForeground3
		bg_placements_frame large
		zoomout_catvolume .6

		room_positions {
			Floor1_Large [1, 1]
			Floor1_Small [18, 1]
			Floor2_Small [1, 9]
			Floor2_Large [18, 9]
			LargeAttic [0, 17]

			Basement0 [1 -6]
			Basement1 [1 -12]
			Basement2 [1 -18]
			Basement3 [1 -24]
			Basement4 [1 -30]
		}

		aux_positions {
			ButchBox [38, 0]
			StraySpawn [-3 0]
			HousePipe [-2 0]

			Roof_LeftEdge [-3.482 16.11]
			Roof_Top [17.562 26.715]
			Roof_RightEdge [38.408 16.185]
		}
	}
}
```

---

### `upgrades`
**Source:** `house.gon`  

```
upgrades {
	Default {
		unlock_room Floor1_Large
		set_house House1
	}

	SmallHouse_Attic {
		prereq Default
		unlock_room Attic
	}

	MediumHouse {
		prereq Default
		set_house House2
	}

	MediumHouse_SmallRoom {
		prereq MediumHouse
		unlock_room Floor1_Small
	}

	LargeHouse {
		prereq MediumHouse
		set_house House3
	}

	LargeHouse_Floor2Large {
		prereq LargeHouse
		unlock_room Floor2_Large
	}

	LargeHouse_Floor2Small {
		prereq LargeHouse
		unlock_room Floor2_Small
	}


	BasementUpgrade {
		prereq MediumHouse
		unlock_room Basement0
	}
	BasementUpgrade2 {
		prereq BasementUpgrade
		unlock_room Basement1
	}
	BasementUpgrade3 {
		prereq BasementUpgrade2
		unlock_room Basement2
	}
	BasementUpgrade4 {
		prereq BasementUpgrade3
		unlock_room Basement3
	}
	BasementUpgrade5 {
		prereq BasementUpgrade4
		unlock_room Basement4
	}
}
```

---

## File: `furniture_effects.gon`

### `poop`
**Name:** Poop  
**Description:** FURNITURE_DESC_POOP  
**Source:** `furniture_effects.gon`  

```
poop {
    name FURNITURE_NAME_POOP
    desc FURNITURE_DESC_POOP
    special true
    can_be_rare false

    Comfort -2
    Health -2
}
```

---

### `autofeeder`
**Name:** Autofeeder  
**Description:** This item got removed from the game and has no effect. Its a waste of space to keep in your house.  
**Source:** `furniture_effects.gon`  

```
autofeeder {
    name FURNITURE_NAME_AUTOFEEDER
    desc FURNITURE_DESC_AUTOFEEDER
    special true
    removed true //deleted from the game
    can_be_rare false
    
   // AutoFeedCat 1
}
```

---

### `special_foodbox`
**Name:** Food Storage Box  
**Description:** +40 Max Food  
**Source:** `furniture_effects.gon`  

```
special_foodbox {
    name FURNITURE_NAME_SPECIAL_FOODBOX
    desc FURNITURE_DESC_SPECIAL_FOODBOX
    special true
    can_be_rare false
    
    FoodStorage 40
}
```

---

### `special_comfortidol`
**Name:** Idol of Comfort  
**Description:** FURNITURE_DESC_SPECIAL_COMFORTIDOL  
**Source:** `furniture_effects.gon`  

```
special_comfortidol {
    name FURNITURE_NAME_SPECIAL_COMFORTIDOL
    desc FURNITURE_DESC_SPECIAL_COMFORTIDOL
    special true
    can_be_rare false
    
    Comfort 5
}
```

---

### `special_appealidol`
**Name:** Idol of Appeal  
**Description:** FURNITURE_DESC_SPECIAL_APPEALIDOL  
**Source:** `furniture_effects.gon`  

```
special_appealidol {
    name FURNITURE_NAME_SPECIAL_APPEALIDOL
    desc FURNITURE_DESC_SPECIAL_APPEALIDOL
    special true
    can_be_rare false
    
    Appeal 5
}
```

---

### `special_healthidol`
**Name:** Idol of Health  
**Description:** FURNITURE_DESC_SPECIAL_HEALTHIDOL  
**Source:** `furniture_effects.gon`  

```
special_healthidol {
    name FURNITURE_NAME_SPECIAL_HEALTHIDOL
    desc FURNITURE_DESC_SPECIAL_HEALTHIDOL
    special true
    can_be_rare false
    
    Health 5
}
```

---

### `special_evolutionidol`
**Name:** Idol of Evolution  
**Description:** FURNITURE_DESC_SPECIAL_EVOLUTIONIDOL  
**Source:** `furniture_effects.gon`  

```
special_evolutionidol {
    name FURNITURE_NAME_SPECIAL_EVOLUTIONIDOL
    desc FURNITURE_DESC_SPECIAL_EVOLUTIONIDOL
    special true
    can_be_rare false
    
    Evolution 5
}
```

---

### `special_stimulationidol`
**Name:** Idol of Stimulation  
**Description:** FURNITURE_DESC_SPECIAL_STIMULATIONIDOL  
**Source:** `furniture_effects.gon`  

```
special_stimulationidol {
    name FURNITURE_NAME_SPECIAL_STIMULATIONIDOL
    desc FURNITURE_DESC_SPECIAL_STIMULATIONIDOL
    special true
    can_be_rare false
    
    Stimulation 5
}
```

---

### `special_fightidol`
**Name:** Idol of Chaos  
**Description:** Fights are deadlier but the winning cat gets double the stat rewards.  
**Source:** `furniture_effects.gon`  

```
special_fightidol {
    name FURNITURE_NAME_SPECIAL_FIGHTIDOL
    desc FURNITURE_DESC_SPECIAL_FIGHTIDOL
    special true
    can_be_rare false
    
    Comfort -5
    FightBonusRewards 1
    FightRisk 2
}
```

---

### `special_suppressoridol`
**Name:** Idol of Chastity  
**Description:** Cats will not breed.  
**Source:** `furniture_effects.gon`  

```
special_suppressoridol {
    name FURNITURE_NAME_SPECIAL_SUPPRESSORIDOL
    desc FURNITURE_DESC_SPECIAL_SUPPRESSORIDOL
    special true
    can_be_rare false
    
    Comfort 5
    BreedSuppression 1
}
```

---

### `set_spider_candelabra`
**Name:** Spider Candelabra  
**Description:** FURNITURE_DESC_SET_SPIDER_CANDELABRA  
**Source:** `furniture_effects.gon`  

```
set_spider_candelabra { //frame 0
    name FURNITURE_NAME_SET_SPIDER_CANDELABRA
    desc FURNITURE_DESC_SET_SPIDER_CANDELABRA
    set spider
    
    Appeal 2
}
```

---

### `set_spider_vanity`
**Name:** Spider Vanity  
**Description:** FURNITURE_DESC_SET_SPIDER_VANITY  
**Source:** `furniture_effects.gon`  

```
set_spider_vanity { //frame 1
    name FURNITURE_NAME_SET_SPIDER_VANITY
    desc FURNITURE_DESC_SET_SPIDER_VANITY
    set spider
    
    Appeal 2    
}
```

---

### `set_spider_chair`
**Name:** Spider Chair  
**Description:** FURNITURE_DESC_SET_SPIDER_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_spider_chair { //frame 2
    name FURNITURE_NAME_SET_SPIDER_CHAIR
    desc FURNITURE_DESC_SET_SPIDER_CHAIR
    set spider
    
    Appeal 2 
}
```

---

### `set_spider_table`
**Name:** Spider Table  
**Description:** FURNITURE_DESC_SET_SPIDER_TABLE  
**Source:** `furniture_effects.gon`  

```
set_spider_table { //frame 3
    name FURNITURE_NAME_SET_SPIDER_TABLE
    desc FURNITURE_DESC_SET_SPIDER_TABLE
    set spider
    
    Appeal 2 
}
```

---

### `set_spider_dresser`
**Name:** Spider Dresser  
**Description:** FURNITURE_DESC_SET_SPIDER_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_spider_dresser { //frame 4
    name FURNITURE_NAME_SET_SPIDER_DRESSER
    desc FURNITURE_DESC_SET_SPIDER_DRESSER
    set spider
    
    Appeal 2 
}
```

---

### `set_spider_tv`
**Name:** Spider TV  
**Description:** FURNITURE_DESC_SET_SPIDER_TV  
**Source:** `furniture_effects.gon`  

```
set_spider_tv { //frame 5
    name FURNITURE_NAME_SET_SPIDER_TV
    desc FURNITURE_DESC_SET_SPIDER_TV
    set spider
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_spider_toilet`
**Name:** Spider Toilet  
**Description:** FURNITURE_DESC_SET_SPIDER_TOILET  
**Source:** `furniture_effects.gon`  

```
set_spider_toilet { //frame 6
    name FURNITURE_NAME_SET_SPIDER_TOILET
    desc FURNITURE_DESC_SET_SPIDER_TOILET
    set spider
    
    Appeal 2 
}
```

---

### `set_spider_shelf`
**Name:** Spider Shelf  
**Description:** FURNITURE_DESC_SET_SPIDER_SHELF  
**Source:** `furniture_effects.gon`  

```
set_spider_shelf { //frame 7
    name FURNITURE_NAME_SET_SPIDER_SHELF
    desc FURNITURE_DESC_SET_SPIDER_SHELF
    set spider
    
    Appeal 2 
}
```

---

### `set_spider_bed`
**Name:** Spider Bed  
**Description:** FURNITURE_DESC_SET_SPIDER_BED  
**Source:** `furniture_effects.gon`  

```
set_spider_bed { //frame 8
    name FURNITURE_NAME_SET_SPIDER_BED
    desc FURNITURE_DESC_SET_SPIDER_BED
    set spider
    
    Appeal 1
    Comfort 1    
}
```

---

### `set_spider_sidetable`
**Name:** Spider Side Table  
**Description:** FURNITURE_DESC_SET_SPIDER_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_spider_sidetable { //frame 9
    name FURNITURE_NAME_SET_SPIDER_SIDETABLE
    desc FURNITURE_DESC_SET_SPIDER_SIDETABLE
    set spider
    
    Appeal 2 
}
```

---

### `set_junk_sidetable`
**Name:** Junk Side Table  
**Description:** FURNITURE_DESC_SET_JUNK_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_junk_sidetable { //frame 10
    name FURNITURE_NAME_SET_JUNK_SIDETABLE
    desc FURNITURE_DESC_SET_JUNK_SIDETABLE
    set junk

    Comfort 1
    Stimulation 1
}
```

---

### `set_junk_chair`
**Name:** Junk Chair  
**Description:** FURNITURE_DESC_SET_JUNK_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_junk_chair { //frame 11
    name FURNITURE_NAME_SET_JUNK_CHAIR
    desc FURNITURE_DESC_SET_JUNK_CHAIR
    set junk

    Comfort 1
    Stimulation 1
}
```

---

### `set_junk_shelf`
**Name:** Junk Shelf  
**Description:** FURNITURE_DESC_SET_JUNK_SHELF  
**Source:** `furniture_effects.gon`  

```
set_junk_shelf { //frame 12
    name FURNITURE_NAME_SET_JUNK_SHELF
    desc FURNITURE_DESC_SET_JUNK_SHELF
    set junk

    Comfort 1
    Stimulation 1
}
```

---

### `set_junk_bed`
**Name:** Junk Bed  
**Description:** FURNITURE_DESC_SET_JUNK_BED  
**Source:** `furniture_effects.gon`  

```
set_junk_bed { //frame 13
    name FURNITURE_NAME_SET_JUNK_BED
    desc FURNITURE_DESC_SET_JUNK_BED
    set junk

    Comfort 1
    Stimulation 1
}
```

---

### `set_junk_cabinet`
**Name:** Junk Cabinet  
**Description:** FURNITURE_DESC_SET_JUNK_CABINET  
**Source:** `furniture_effects.gon`  

```
set_junk_cabinet { //frame 14
    name FURNITURE_NAME_SET_JUNK_CABINET
    desc FURNITURE_DESC_SET_JUNK_CABINET
    set junk

    Comfort 1
    Stimulation 1
}
```

---

### `set_junk_tv`
**Name:** Junk TV  
**Description:** FURNITURE_DESC_SET_JUNK_TV  
**Source:** `furniture_effects.gon`  

```
set_junk_tv { //frame 15
    name FURNITURE_NAME_SET_JUNK_TV
    desc FURNITURE_DESC_SET_JUNK_TV
    set junk

    Stimulation 2
}
```

---

### `set_junk_suspendedshelf`
**Name:** Suspended Junk Shelf  
**Description:** FURNITURE_DESC_SET_JUNK_SUSPENDEDSHELF  
**Source:** `furniture_effects.gon`  

```
set_junk_suspendedshelf { //frame 16
    name FURNITURE_NAME_SET_JUNK_SUSPENDEDSHELF
    desc FURNITURE_DESC_SET_JUNK_SUSPENDEDSHELF
    set junk

    Comfort 1
    Stimulation 1
}
```

---

### `set_junk_lamp`
**Name:** Junk Lamp  
**Description:** FURNITURE_DESC_SET_JUNK_LAMP  
**Source:** `furniture_effects.gon`  

```
set_junk_lamp { //frame 17
    name FURNITURE_NAME_SET_JUNK_LAMP
    desc FURNITURE_DESC_SET_JUNK_LAMP
    set junk

    Comfort 1
    Stimulation 1
}
```

---

### `set_junk_dresser`
**Name:** Junk Dresser  
**Description:** FURNITURE_DESC_SET_JUNK_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_junk_dresser { //frame 18
    name FURNITURE_NAME_SET_JUNK_DRESSER
    desc FURNITURE_DESC_SET_JUNK_DRESSER
    set junk

    Comfort 1
    Stimulation 1
}
```

---

### `set_junk_toilet`
**Name:** Junk Toilet  
**Description:** FURNITURE_DESC_SET_JUNK_TOILET  
**Source:** `furniture_effects.gon`  

```
set_junk_toilet { //frame 19
    name FURNITURE_NAME_SET_JUNK_TOILET
    desc FURNITURE_DESC_SET_JUNK_TOILET
    set junk

    Comfort 1
    Stimulation 1
}
```

---

### `set_sewn_dresser`
**Name:** Sewn Dresser  
**Description:** FURNITURE_DESC_SET_SEWN_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_sewn_dresser { //frame 20
    name FURNITURE_NAME_SET_SEWN_DRESSER
    desc FURNITURE_DESC_SET_SEWN_DRESSER
    set sewn
    
    Appeal 1
    Comfort 1
}
```

---

### `set_sewn_sidetable`
**Name:** Sewn Side Table  
**Description:** FURNITURE_DESC_SET_SEWN_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_sewn_sidetable { //frame 21
    name FURNITURE_NAME_SET_SEWN_SIDETABLE
    desc FURNITURE_DESC_SET_SEWN_SIDETABLE
    set sewn
    
    Appeal 1
    Comfort 1
}
```

---

### `set_sewn_table`
**Name:** Sewn Table  
**Description:** FURNITURE_DESC_SET_SEWN_TABLE  
**Source:** `furniture_effects.gon`  

```
set_sewn_table { //frame 22
    name FURNITURE_NAME_SET_SEWN_TABLE
    desc FURNITURE_DESC_SET_SEWN_TABLE
    set sewn
    
    Appeal 1
    Comfort 1 
}
```

---

### `set_sewn_couch`
**Name:** Sewn Couch  
**Description:** FURNITURE_DESC_SET_SEWN_COUCH  
**Source:** `furniture_effects.gon`  

```
set_sewn_couch { //frame 23
    name FURNITURE_NAME_SET_SEWN_COUCH
    desc FURNITURE_DESC_SET_SEWN_COUCH
    set sewn
    
    Comfort 2
}
```

---

### `set_sewn_chair`
**Name:** Sewn Chair  
**Description:** FURNITURE_DESC_SET_SEWN_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_sewn_chair { //frame 24
    name FURNITURE_NAME_SET_SEWN_CHAIR
    desc FURNITURE_DESC_SET_SEWN_CHAIR
    set sewn
    
    Comfort 2
}
```

---

### `set_sewn_stool1`
**Name:** Sewn Stool A  
**Description:** FURNITURE_DESC_SET_SEWN_STOOL1  
**Source:** `furniture_effects.gon`  

```
set_sewn_stool1 { //frame 25
    name FURNITURE_NAME_SET_SEWN_STOOL1
    desc FURNITURE_DESC_SET_SEWN_STOOL1
    set sewn
    
    Comfort 2
}
```

---

### `set_sewn_toilet`
**Name:** Sewn Toilet  
**Description:** FURNITURE_DESC_SET_SEWN_TOILET  
**Source:** `furniture_effects.gon`  

```
set_sewn_toilet { //frame 26
    name FURNITURE_NAME_SET_SEWN_TOILET
    desc FURNITURE_DESC_SET_SEWN_TOILET
    set sewn
    
    Comfort 2
}
```

---

### `set_sewn_tv`
**Name:** Sewn TV  
**Description:** FURNITURE_DESC_SET_SEWN_TV  
**Source:** `furniture_effects.gon`  

```
set_sewn_tv { //frame 27
    name FURNITURE_NAME_SET_SEWN_TV
    desc FURNITURE_DESC_SET_SEWN_TV
    set sewn
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_sewn_doll`
**Name:** Sewn Doll  
**Description:** FURNITURE_DESC_SET_SEWN_DOLL  
**Source:** `furniture_effects.gon`  

```
set_sewn_doll { //frame 28
    name FURNITURE_NAME_SET_SEWN_DOLL
    desc FURNITURE_DESC_SET_SEWN_DOLL
    set sewn
    
    Comfort 1
    Appeal 1
}
```

---

### `set_sewn_stool2`
**Name:** Sewn Stool B  
**Description:** FURNITURE_DESC_SET_SEWN_STOOL2  
**Source:** `furniture_effects.gon`  

```
set_sewn_stool2 { //frame 29
    name FURNITURE_NAME_SET_SEWN_STOOL2
    desc FURNITURE_DESC_SET_SEWN_STOOL2
    set sewn
    
    Comfort 2
}
```

---

### `set_cat_shelf`
**Name:** Cat Shelf  
**Description:** FURNITURE_DESC_SET_CAT_SHELF  
**Source:** `furniture_effects.gon`  

```
set_cat_shelf { //frame 30
    name FURNITURE_NAME_SET_CAT_SHELF
    desc FURNITURE_DESC_SET_CAT_SHELF
    set cat
    
    Appeal 2
}
```

---

### `set_cat_couch`
**Name:** Cat Couch  
**Description:** FURNITURE_DESC_SET_CAT_COUCH  
**Source:** `furniture_effects.gon`  

```
set_cat_couch { //frame 31
    name FURNITURE_NAME_SET_CAT_COUCH
    desc FURNITURE_DESC_SET_CAT_COUCH
    set cat
    
    Appeal 2
}
```

---

### `set_cat_chair`
**Name:** Cat Chair  
**Description:** FURNITURE_DESC_SET_CAT_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_cat_chair { //frame 32
    name FURNITURE_NAME_SET_CAT_CHAIR
    desc FURNITURE_DESC_SET_CAT_CHAIR
    set cat
    
    Appeal 2
}
```

---

### `set_cat_bed`
**Name:** Cat Bed  
**Description:** FURNITURE_DESC_SET_CAT_BED  
**Source:** `furniture_effects.gon`  

```
set_cat_bed { //frame 33
    name FURNITURE_NAME_SET_CAT_BED
    desc FURNITURE_DESC_SET_CAT_BED
    set cat
    
    Appeal 2
}
```

---

### `set_cat_table`
**Name:** Cat Table A  
**Description:** FURNITURE_DESC_SET_CAT_TABLE  
**Source:** `furniture_effects.gon`  

```
set_cat_table { //frame 34
    name FURNITURE_NAME_SET_CAT_TABLE
    desc FURNITURE_DESC_SET_CAT_TABLE
    set cat
    
    Appeal 2
}
```

---

### `set_cat_tv`
**Name:** Cat TV  
**Description:** FURNITURE_DESC_SET_CAT_TV  
**Source:** `furniture_effects.gon`  

```
set_cat_tv { //frame 35
    name FURNITURE_NAME_SET_CAT_TV
    desc FURNITURE_DESC_SET_CAT_TV
    set cat
    
    Appeal 2
}
```

---

### `set_cat_bench`
**Name:** Cat Bench  
**Description:** FURNITURE_DESC_SET_CAT_BENCH  
**Source:** `furniture_effects.gon`  

```
set_cat_bench { //frame 36
    name FURNITURE_NAME_SET_CAT_BENCH
    desc FURNITURE_DESC_SET_CAT_BENCH
    set cat
    
    Appeal 2
}
```

---

### `set_cat_dresser`
**Name:** Cat Dresser  
**Description:** FURNITURE_DESC_SET_CAT_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_cat_dresser { //frame 37
    name FURNITURE_NAME_SET_CAT_DRESSER
    desc FURNITURE_DESC_SET_CAT_DRESSER
    set cat
    
    Appeal 2
}
```

---

### `set_cat_suspended_shelf`
**Name:** Suspended Cat Shelf  
**Description:** FURNITURE_DESC_SET_CAT_SUSPENDED_SHELF  
**Source:** `furniture_effects.gon`  

```
set_cat_suspended_shelf { //frame 38
    name FURNITURE_NAME_SET_CAT_SUSPENDED_SHELF
    desc FURNITURE_DESC_SET_CAT_SUSPENDED_SHELF
    set cat
    
    Appeal 2
}
```

---

### `set_cat_table2`
**Name:** Cat Table B  
**Description:** FURNITURE_DESC_SET_CAT_TABLE2  
**Source:** `furniture_effects.gon`  

```
set_cat_table2 { //frame 39
    name FURNITURE_NAME_SET_CAT_TABLE2
    desc FURNITURE_DESC_SET_CAT_TABLE2
    set cat
    
    Appeal 2
}
```

---

### `set_wooden_shelf`
**Name:** Wooden Shelf A  
**Description:** FURNITURE_DESC_SET_WOODEN_SHELF  
**Source:** `furniture_effects.gon`  

```
set_wooden_shelf { //frame 40
    name FURNITURE_NAME_SET_WOODEN_SHELF
    desc FURNITURE_DESC_SET_WOODEN_SHELF
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_wooden_dresser`
**Name:** Wooden Dresser  
**Description:** FURNITURE_DESC_SET_WOODEN_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_wooden_dresser { //frame 41
    name FURNITURE_NAME_SET_WOODEN_DRESSER
    desc FURNITURE_DESC_SET_WOODEN_DRESSER
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_wooden_chair`
**Name:** Wooden Chair  
**Description:** FURNITURE_DESC_SET_WOODEN_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_wooden_chair { //frame 42
    name FURNITURE_NAME_SET_WOODEN_CHAIR
    desc FURNITURE_DESC_SET_WOODEN_CHAIR
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_wooden_toilet`
**Name:** Wooden Toilet  
**Description:** FURNITURE_DESC_SET_WOODEN_TOILET  
**Source:** `furniture_effects.gon`  

```
set_wooden_toilet { //frame 43
    name FURNITURE_NAME_SET_WOODEN_TOILET
    desc FURNITURE_DESC_SET_WOODEN_TOILET
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_wooden_table`
**Name:** Wooden Table  
**Description:** FURNITURE_DESC_SET_WOODEN_TABLE  
**Source:** `furniture_effects.gon`  

```
set_wooden_table { //frame 44
    name FURNITURE_NAME_SET_WOODEN_TABLE
    desc FURNITURE_DESC_SET_WOODEN_TABLE
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_wooden_sink`
**Name:** Wooden Sink  
**Description:** FURNITURE_DESC_SET_WOODEN_SINK  
**Source:** `furniture_effects.gon`  

```
set_wooden_sink { //frame 45
    name FURNITURE_NAME_SET_WOODEN_SINK
    desc FURNITURE_DESC_SET_WOODEN_SINK
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_wooden_lamp`
**Name:** Wooden Lamp  
**Description:** FURNITURE_DESC_SET_WOODEN_LAMP  
**Source:** `furniture_effects.gon`  

```
set_wooden_lamp { //frame 46
    name FURNITURE_NAME_SET_WOODEN_LAMP
    desc FURNITURE_DESC_SET_WOODEN_LAMP
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_wooden_tv`
**Name:** Wooden TV  
**Description:** FURNITURE_DESC_SET_WOODEN_TV  
**Source:** `furniture_effects.gon`  

```
set_wooden_tv { //frame 47
    name FURNITURE_NAME_SET_WOODEN_TV
    desc FURNITURE_DESC_SET_WOODEN_TV
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_wooden_suspendedshelf`
**Name:** Suspended Wooden Shelf  
**Description:** FURNITURE_DESC_SET_WOODEN_SUSPENDEDSHELF  
**Source:** `furniture_effects.gon`  

```
set_wooden_suspendedshelf { //frame 48
    name FURNITURE_NAME_SET_WOODEN_SUSPENDEDSHELF
    desc FURNITURE_DESC_SET_WOODEN_SUSPENDEDSHELF
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_wooden_shelf2`
**Name:** Wooden Shelf B  
**Description:** FURNITURE_DESC_SET_WOODEN_SHELF2  
**Source:** `furniture_effects.gon`  

```
set_wooden_shelf2 { //frame 49
    name FURNITURE_NAME_SET_WOODEN_SHELF2
    desc FURNITURE_DESC_SET_WOODEN_SHELF2
    set wooden
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_sewer_sink`
**Name:** Sewer Sink  
**Description:** FURNITURE_DESC_SET_SEWER_SINK  
**Source:** `furniture_effects.gon`  

```
set_sewer_sink { //frame 50
    name FURNITURE_NAME_SET_SEWER_SINK
    desc FURNITURE_DESC_SET_SEWER_SINK
    set sewer
    
    Stimulation 1
    Appeal 1
	Health -1
	Evolution 1
	
}
```

---

### `set_sewer_shelf`
**Name:** Sewer Shelf  
**Description:** FURNITURE_DESC_SET_SEWER_SHELF  
**Source:** `furniture_effects.gon`  

```
set_sewer_shelf { //frame 51
    name FURNITURE_NAME_SET_SEWER_SHELF
    desc FURNITURE_DESC_SET_SEWER_SHELF
    set sewer
    
    Stimulation 4
    Appeal -1
    Comfort -1
	Health -1
	Evolution 1
}
```

---

### `set_sewer_table`
**Name:** Sewer Table  
**Description:** FURNITURE_DESC_SET_SEWER_TABLE  
**Source:** `furniture_effects.gon`  

```
set_sewer_table { //frame 52
    name FURNITURE_NAME_SET_SEWER_TABLE
    desc FURNITURE_DESC_SET_SEWER_TABLE
    set sewer
    
    Stimulation 4
    Appeal -1
    Comfort -1
	Health -1
	Evolution 1
}
```

---

### `set_sewer_dresser`
**Name:** Sewer Dresser  
**Description:** FURNITURE_DESC_SET_SEWER_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_sewer_dresser { //frame 53
    name FURNITURE_NAME_SET_SEWER_DRESSER
    desc FURNITURE_DESC_SET_SEWER_DRESSER
    set sewer
    
    Stimulation 4
    Appeal -1
    Comfort -1
	Health -1
	Evolution 1
}
```

---

### `set_sewer_chair`
**Name:** Sewer Chair  
**Description:** FURNITURE_DESC_SET_SEWER_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_sewer_chair { //frame 54
    name FURNITURE_NAME_SET_SEWER_CHAIR
    desc FURNITURE_DESC_SET_SEWER_CHAIR
    set sewer
    
    Stimulation 4
    Appeal -1
    Comfort -1
	Health -1
	Evolution 1
}
```

---

### `set_sewer_suspendedshelf`
**Name:** Suspended Sewer Shelf  
**Description:** FURNITURE_DESC_SET_SEWER_SUSPENDEDSHELF  
**Source:** `furniture_effects.gon`  

```
set_sewer_suspendedshelf { //frame 55
    name FURNITURE_NAME_SET_SEWER_SUSPENDEDSHELF
    desc FURNITURE_DESC_SET_SEWER_SUSPENDEDSHELF
    set sewer
    
    Stimulation 4
    Appeal -1
    Comfort -1
	Health -1
	Evolution 1
}
```

---

### `set_sewer_tv`
**Name:** Sewer TV  
**Description:** FURNITURE_DESC_SET_SEWER_TV  
**Source:** `furniture_effects.gon`  

```
set_sewer_tv { //frame 56
    name FURNITURE_NAME_SET_SEWER_TV
    desc FURNITURE_DESC_SET_SEWER_TV
    set sewer
    
    Stimulation 4
    Appeal -1
    Comfort -1
	Health -1
	Evolution 1
}
```

---

### `set_sewer_small_table`
**Name:** Sewer Small Table  
**Description:** FURNITURE_DESC_SET_SEWER_SMALL_TABLE  
**Source:** `furniture_effects.gon`  

```
set_sewer_small_table { //frame 57
    name FURNITURE_NAME_SET_SEWER_SMALL_TABLE
    desc FURNITURE_DESC_SET_SEWER_SMALL_TABLE
    set sewer
    
    Stimulation 4
    Appeal -1
    Comfort -1
	Health -1
	Evolution 1
}
```

---

### `set_sewer_stool`
**Name:** Sewer Stool  
**Description:** FURNITURE_DESC_SET_SEWER_STOOL  
**Source:** `furniture_effects.gon`  

```
set_sewer_stool { //frame 58
    name FURNITURE_NAME_SET_SEWER_STOOL
    desc FURNITURE_DESC_SET_SEWER_STOOL
    set sewer
    
    Stimulation 4
    Appeal -1
    Comfort -1
	Health -1
	Evolution 1
}
```

---

### `set_sewer_lamp`
**Name:** Sewer Lamp  
**Description:** FURNITURE_DESC_SET_SEWER_LAMP  
**Source:** `furniture_effects.gon`  

```
set_sewer_lamp { //frame 59
    name FURNITURE_NAME_SET_SEWER_LAMP
    desc FURNITURE_DESC_SET_SEWER_LAMP
    set sewer
    
    Stimulation 4
    Appeal -1
    Comfort -1
	Health -1
	Evolution 1
}
```

---

### `set_bone_shelf`
**Name:** Bone Shelf  
**Description:** FURNITURE_DESC_SET_BONE_SHELF  
**Source:** `furniture_effects.gon`  

```
set_bone_shelf { //frame 60
    name FURNITURE_NAME_SET_BONE_SHELF
    desc FURNITURE_DESC_SET_BONE_SHELF
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_bone_sink`
**Name:** Bone Sink  
**Description:** FURNITURE_DESC_SET_BONE_SINK  
**Source:** `furniture_effects.gon`  

```
set_bone_sink { //frame 61
    name FURNITURE_NAME_SET_BONE_SINK
    desc FURNITURE_DESC_SET_BONE_SINK
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_bone_sidetable`
**Name:** Bone Side Table  
**Description:** FURNITURE_DESC_SET_BONE_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_bone_sidetable { //frame 62
    name FURNITURE_NAME_SET_BONE_SIDETABLE
    desc FURNITURE_DESC_SET_BONE_SIDETABLE
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_bone_table`
**Name:** Bone Table  
**Description:** FURNITURE_DESC_SET_BONE_TABLE  
**Source:** `furniture_effects.gon`  

```
set_bone_table { //frame 63
    name FURNITURE_NAME_SET_BONE_TABLE
    desc FURNITURE_DESC_SET_BONE_TABLE
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_bone_couch`
**Name:** Bone Couch  
**Description:** FURNITURE_DESC_SET_BONE_COUCH  
**Source:** `furniture_effects.gon`  

```
set_bone_couch { //frame 64
    name FURNITURE_NAME_SET_BONE_COUCH
    desc FURNITURE_DESC_SET_BONE_COUCH
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_bone_tv`
**Name:** Bone TV  
**Description:** FURNITURE_DESC_SET_BONE_TV  
**Source:** `furniture_effects.gon`  

```
set_bone_tv { //frame 65
    name FURNITURE_NAME_SET_BONE_TV
    desc FURNITURE_DESC_SET_BONE_TV
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_bone_chandelier`
**Name:** Bone Chandelier  
**Description:** FURNITURE_DESC_SET_BONE_CHANDELIER  
**Source:** `furniture_effects.gon`  

```
set_bone_chandelier { //frame 66
    name FURNITURE_NAME_SET_BONE_CHANDELIER
    desc FURNITURE_DESC_SET_BONE_CHANDELIER
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_bone_lamp`
**Name:** Bone Lamp  
**Description:** FURNITURE_DESC_SET_BONE_LAMP  
**Source:** `furniture_effects.gon`  

```
set_bone_lamp { //frame 67
    name FURNITURE_NAME_SET_BONE_LAMP
    desc FURNITURE_DESC_SET_BONE_LAMP
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_bone_chair`
**Name:** Bone Chair  
**Description:** FURNITURE_DESC_SET_BONE_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_bone_chair { //frame 68
    name FURNITURE_NAME_SET_BONE_CHAIR
    desc FURNITURE_DESC_SET_BONE_CHAIR
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_bone_pile`
**Name:** Bone Pile  
**Description:** FURNITURE_DESC_SET_BONE_PILE  
**Source:** `furniture_effects.gon`  

```
set_bone_pile { //frame 69
    name FURNITURE_NAME_SET_BONE_PILE
    desc FURNITURE_DESC_SET_BONE_PILE
    set bone
    
    Stimulation 1
    Appeal 2
    Comfort -1
}
```

---

### `set_robo_shelf`
**Name:** Robo Shelf  
**Description:** FURNITURE_DESC_SET_ROBO_SHELF  
**Source:** `furniture_effects.gon`  

```
set_robo_shelf { //frame 70
    name FURNITURE_NAME_SET_ROBO_SHELF
    desc FURNITURE_DESC_SET_ROBO_SHELF
    set robo
    
    Stimulation 3
    Comfort -1
}
```

---

### `set_robo_sink`
**Name:** Robo Sink  
**Description:** FURNITURE_DESC_SET_ROBO_SINK  
**Source:** `furniture_effects.gon`  

```
set_robo_sink { //frame 71
    name FURNITURE_NAME_SET_ROBO_SINK
    desc FURNITURE_DESC_SET_ROBO_SINK
    set robo

    Stimulation 3
    Comfort -1
}
```

---

### `set_robo_desk`
**Name:** Robo Desk  
**Description:** FURNITURE_DESC_SET_ROBO_DESK  
**Source:** `furniture_effects.gon`  

```
set_robo_desk { //frame 72
    name FURNITURE_NAME_SET_ROBO_DESK
    desc FURNITURE_DESC_SET_ROBO_DESK
    set robo
    
    Stimulation 3
    Comfort -1
}
```

---

### `set_robo_table`
**Name:** Robo Table  
**Description:** FURNITURE_DESC_SET_ROBO_TABLE  
**Source:** `furniture_effects.gon`  

```
set_robo_table { //frame 73
    name FURNITURE_NAME_SET_ROBO_TABLE
    desc FURNITURE_DESC_SET_ROBO_TABLE
    set robo
    
    Stimulation 3
    Comfort -1
}
```

---

### `set_robo_dresser`
**Name:** Robo Dresser  
**Description:** FURNITURE_DESC_SET_ROBO_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_robo_dresser { //frame 74
    name FURNITURE_NAME_SET_ROBO_DRESSER
    desc FURNITURE_DESC_SET_ROBO_DRESSER
    set robo
    
    Stimulation 3
    Comfort -1
}
```

---

### `set_robo_tv`
**Name:** Robo TV  
**Description:** FURNITURE_DESC_SET_ROBO_TV  
**Source:** `furniture_effects.gon`  

```
set_robo_tv { //frame 75
    name FURNITURE_NAME_SET_ROBO_TV
    desc FURNITURE_DESC_SET_ROBO_TV
    set robo
    
    Stimulation 3
    Comfort -1
}
```

---

### `set_robo_robobody`
**Name:** Robo Body  
**Description:** FURNITURE_DESC_SET_ROBO_ROBOBODY  
**Source:** `furniture_effects.gon`  

```
set_robo_robobody { //frame 76
    name FURNITURE_NAME_SET_ROBO_ROBOBODY
    desc FURNITURE_DESC_SET_ROBO_ROBOBODY
    set robo
    
    Stimulation 3
    Comfort -1
}
```

---

### `set_robo_robochest`
**Name:** Robo Chest  
**Description:** FURNITURE_DESC_SET_ROBO_ROBOCHEST  
**Source:** `furniture_effects.gon`  

```
set_robo_robochest { //frame 77
    name FURNITURE_NAME_SET_ROBO_ROBOCHEST
    desc FURNITURE_DESC_SET_ROBO_ROBOCHEST
    set robo
    
    Stimulation 3
    Comfort -1
}
```

---

### `set_robo_roboarms`
**Name:** Robo Arms  
**Description:** FURNITURE_DESC_SET_ROBO_ROBOARMS  
**Source:** `furniture_effects.gon`  

```
set_robo_roboarms { //frame 78
    name FURNITURE_NAME_SET_ROBO_ROBOARMS
    desc FURNITURE_DESC_SET_ROBO_ROBOARMS
    set robo
    
    Stimulation 3
    Comfort -1
}
```

---

### `set_robo_head`
**Name:** Robo Head  
**Description:** FURNITURE_DESC_SET_ROBO_HEAD  
**Source:** `furniture_effects.gon`  

```
set_robo_head { //frame 79
    name FURNITURE_NAME_SET_ROBO_HEAD
    desc FURNITURE_DESC_SET_ROBO_HEAD
    set robo
    
    Stimulation 3
    Comfort -1
}
```

---

### `set_guts_shelf`
**Name:** Guts Shelf  
**Description:** FURNITURE_DESC_SET_GUTS_SHELF  
**Source:** `furniture_effects.gon`  

```
set_guts_shelf { //frame 80
    name FURNITURE_NAME_SET_GUTS_SHELF
    desc FURNITURE_DESC_SET_GUTS_SHELF
    set guts
    
    Appeal -1
    Stimulation 1
    Comfort 2
}
```

---

### `set_guts_table`
**Name:** Guts Table  
**Description:** FURNITURE_DESC_SET_GUTS_TABLE  
**Source:** `furniture_effects.gon`  

```
set_guts_table { //frame 81
    name FURNITURE_NAME_SET_GUTS_TABLE
    desc FURNITURE_DESC_SET_GUTS_TABLE
    set guts
    
    Appeal -1
    Stimulation 1
    Comfort 2
}
```

---

### `set_guts_sidetable`
**Name:** Guts Side Table A  
**Description:** FURNITURE_DESC_SET_GUTS_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_guts_sidetable { //frame 82
    name FURNITURE_NAME_SET_GUTS_SIDETABLE
    desc FURNITURE_DESC_SET_GUTS_SIDETABLE
    set guts
    
    Appeal -1
    Stimulation 1
    Comfort 2
}
```

---

### `set_guts_sink`
**Name:** Guts Sink  
**Description:** FURNITURE_DESC_SET_GUTS_SINK  
**Source:** `furniture_effects.gon`  

```
set_guts_sink { //frame 83
    name FURNITURE_NAME_SET_GUTS_SINK
    desc FURNITURE_DESC_SET_GUTS_SINK
    set guts
    
    Appeal -1
    Stimulation 1
    Comfort 2
}
```

---

### `set_guts_sidetable2`
**Name:** Guts Side Table B  
**Description:** FURNITURE_DESC_SET_GUTS_SIDETABLE2  
**Source:** `furniture_effects.gon`  

```
set_guts_sidetable2 { //frame 84
    name FURNITURE_NAME_SET_GUTS_SIDETABLE2
    desc FURNITURE_DESC_SET_GUTS_SIDETABLE2
    set guts
    
    Appeal -1
    Stimulation 1
    Comfort 2
}
```

---

### `set_guts_toilet`
**Name:** Guts Toilet  
**Description:** FURNITURE_DESC_SET_GUTS_TOILET  
**Source:** `furniture_effects.gon`  

```
set_guts_toilet { //frame 85
    name FURNITURE_NAME_SET_GUTS_TOILET
    desc FURNITURE_DESC_SET_GUTS_TOILET
    set guts
    
    Appeal -1
    Stimulation 1
    Comfort 2
}
```

---

### `set_guts_lamp`
**Name:** Guts Lamp A  
**Description:** FURNITURE_DESC_SET_GUTS_LAMP  
**Source:** `furniture_effects.gon`  

```
set_guts_lamp { //frame 86
    name FURNITURE_NAME_SET_GUTS_LAMP
    desc FURNITURE_DESC_SET_GUTS_LAMP
    set guts
    
    Appeal -1
    Stimulation 1
    Comfort 2
}
```

---

### `set_guts_lamp2`
**Name:** Guts Lamp B  
**Description:** FURNITURE_DESC_SET_GUTS_LAMP2  
**Source:** `furniture_effects.gon`  

```
set_guts_lamp2 { //frame 87
    name FURNITURE_NAME_SET_GUTS_LAMP2
    desc FURNITURE_DESC_SET_GUTS_LAMP2
    set guts
    
    Appeal -1
    Stimulation 1
    Comfort 2
}
```

---

### `set_guts_suspendedshelf`
**Name:** Suspended Guts Shelf  
**Description:** FURNITURE_DESC_SET_GUTS_SUSPENDEDSHELF  
**Source:** `furniture_effects.gon`  

```
set_guts_suspendedshelf { //frame 88
    name FURNITURE_NAME_SET_GUTS_SUSPENDEDSHELF
    desc FURNITURE_DESC_SET_GUTS_SUSPENDEDSHELF
    set guts
    
    Appeal -1
    Stimulation 1
    Comfort 2
}
```

---

### `set_guts_tv`
**Name:** Guts TV  
**Description:** FURNITURE_DESC_SET_GUTS_TV  
**Source:** `furniture_effects.gon`  

```
set_guts_tv { //frame 89
    name FURNITURE_NAME_SET_GUTS_TV
    desc FURNITURE_DESC_SET_GUTS_TV
    set guts
    
    Appeal -1
    Stimulation 2
    Comfort 1  
}
```

---

### `set_crystal_toilet`
**Name:** Crystal Toilet  
**Description:** FURNITURE_DESC_SET_CRYSTAL_TOILET  
**Source:** `furniture_effects.gon`  

```
set_crystal_toilet { //frame 90
    name FURNITURE_NAME_SET_CRYSTAL_TOILET
    desc FURNITURE_DESC_SET_CRYSTAL_TOILET
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_crystal_dresser`
**Name:** Crystal Dresser A  
**Description:** FURNITURE_DESC_SET_CRYSTAL_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_crystal_dresser { //frame 91
    name FURNITURE_NAME_SET_CRYSTAL_DRESSER
    desc FURNITURE_DESC_SET_CRYSTAL_DRESSER
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_crystal_lamp`
**Name:** Crystal Lamp  
**Description:** FURNITURE_DESC_SET_CRYSTAL_LAMP  
**Source:** `furniture_effects.gon`  

```
set_crystal_lamp { //frame 92
    name FURNITURE_NAME_SET_CRYSTAL_LAMP
    desc FURNITURE_DESC_SET_CRYSTAL_LAMP
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_crystal_table`
**Name:** Crystal Table  
**Description:** FURNITURE_DESC_SET_CRYSTAL_TABLE  
**Source:** `furniture_effects.gon`  

```
set_crystal_table { //frame 93
    name FURNITURE_NAME_SET_CRYSTAL_TABLE
    desc FURNITURE_DESC_SET_CRYSTAL_TABLE
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_crystal_chandelier`
**Name:** Crystal Chandelier  
**Description:** FURNITURE_DESC_SET_CRYSTAL_CHANDELIER  
**Source:** `furniture_effects.gon`  

```
set_crystal_chandelier { //frame 94
    name FURNITURE_NAME_SET_CRYSTAL_CHANDELIER
    desc FURNITURE_DESC_SET_CRYSTAL_CHANDELIER
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_crystal_dresser2`
**Name:** Crystal Dresser B  
**Description:** FURNITURE_DESC_SET_CRYSTAL_DRESSER2  
**Source:** `furniture_effects.gon`  

```
set_crystal_dresser2 { //frame 95
    name FURNITURE_NAME_SET_CRYSTAL_DRESSER2
    desc FURNITURE_DESC_SET_CRYSTAL_DRESSER2
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_crystal_sidetable`
**Name:** Crystal Side Table  
**Description:** FURNITURE_DESC_SET_CRYSTAL_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_crystal_sidetable { //frame 96
    name FURNITURE_NAME_SET_CRYSTAL_SIDETABLE
    desc FURNITURE_DESC_SET_CRYSTAL_SIDETABLE
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_crystal_couch`
**Name:** Crystal Couch  
**Description:** FURNITURE_DESC_SET_CRYSTAL_COUCH  
**Source:** `furniture_effects.gon`  

```
set_crystal_couch { //frame 97
    name FURNITURE_NAME_SET_CRYSTAL_COUCH
    desc FURNITURE_DESC_SET_CRYSTAL_COUCH
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_crystal_chair`
**Name:** Crystal Chair  
**Description:** FURNITURE_DESC_SET_CRYSTAL_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_crystal_chair { //frame 98
    name FURNITURE_NAME_SET_CRYSTAL_CHAIR
    desc FURNITURE_DESC_SET_CRYSTAL_CHAIR
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_crystal_shelf`
**Name:** Crystal Shelf  
**Description:** FURNITURE_DESC_SET_CRYSTAL_SHELF  
**Source:** `furniture_effects.gon`  

```
set_crystal_shelf { //frame 99
    name FURNITURE_NAME_SET_CRYSTAL_SHELF
    desc FURNITURE_DESC_SET_CRYSTAL_SHELF
    set crystal
    
    Appeal 4
    Comfort -2
}
```

---

### `set_block_L`
**Name:** "L" Block  
**Description:** FURNITURE_DESC_SET_BLOCK_L  
**Source:** `furniture_effects.gon`  

```
set_block_L { //frame 100
    name FURNITURE_NAME_SET_BLOCK_L
    desc FURNITURE_DESC_SET_BLOCK_L
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_block_t`
**Name:** "T" Block  
**Description:** FURNITURE_DESC_SET_BLOCK_T  
**Source:** `furniture_effects.gon`  

```
set_block_t { //frame 101
    name FURNITURE_NAME_SET_BLOCK_T
    desc FURNITURE_DESC_SET_BLOCK_T
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_block_square`
**Name:** "O" Block  
**Description:** FURNITURE_DESC_SET_BLOCK_SQUARE  
**Source:** `furniture_effects.gon`  

```
set_block_square { //frame 102
    name FURNITURE_NAME_SET_BLOCK_SQUARE
    desc FURNITURE_DESC_SET_BLOCK_SQUARE
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_block_7`
**Name:** Flipped "L" Block  
**Description:** FURNITURE_DESC_SET_BLOCK_7  
**Source:** `furniture_effects.gon`  

```
set_block_7 { //frame 103
    name FURNITURE_NAME_SET_BLOCK_7
    desc FURNITURE_DESC_SET_BLOCK_7
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_block_square2`
**Name:** "O"Block  
**Description:** FURNITURE_DESC_SET_BLOCK_SQUARE2  
**Source:** `furniture_effects.gon`  

```
set_block_square2 { //frame 104
    name FURNITURE_NAME_SET_BLOCK_SQUARE2
    desc FURNITURE_DESC_SET_BLOCK_SQUARE2
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_block_layingl`
**Name:** Laying "L" Block  
**Description:** FURNITURE_DESC_SET_BLOCK_LAYINGL  
**Source:** `furniture_effects.gon`  

```
set_block_layingl { //frame 105
    name FURNITURE_NAME_SET_BLOCK_LAYINGL
    desc FURNITURE_DESC_SET_BLOCK_LAYINGL
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_block_i`
**Name:** "I" Block  
**Description:** FURNITURE_DESC_SET_BLOCK_I  
**Source:** `furniture_effects.gon`  

```
set_block_i { //frame 106
    name FURNITURE_NAME_SET_BLOCK_I
    desc FURNITURE_DESC_SET_BLOCK_I
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_block_sidet`
**Name:** Sideways "T" Block  
**Description:** FURNITURE_DESC_SET_BLOCK_SIDET  
**Source:** `furniture_effects.gon`  

```
set_block_sidet { //frame 107
    name FURNITURE_NAME_SET_BLOCK_SIDET
    desc FURNITURE_DESC_SET_BLOCK_SIDET
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_block_downl`
**Name:** Laying "L" Block  
**Description:** FURNITURE_DESC_SET_BLOCK_DOWNL  
**Source:** `furniture_effects.gon`  

```
set_block_downl { //frame 108
    name FURNITURE_NAME_SET_BLOCK_DOWNL
    desc FURNITURE_DESC_SET_BLOCK_DOWNL
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_block_sidei`
**Name:** Laying "I" Block  
**Description:** FURNITURE_DESC_SET_BLOCK_SIDEI  
**Source:** `furniture_effects.gon`  

```
set_block_sidei { //frame 109
    name FURNITURE_NAME_SET_BLOCK_SIDEI
    desc FURNITURE_DESC_SET_BLOCK_SIDEI
    set block
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_monster_shelf`
**Name:** Monster Shelf  
**Description:** FURNITURE_DESC_SET_MONSTER_SHELF  
**Source:** `furniture_effects.gon`  

```
set_monster_shelf { //frame 110
    name FURNITURE_NAME_SET_MONSTER_SHELF
    desc FURNITURE_DESC_SET_MONSTER_SHELF
    set monster
    
    Appeal -1
    Stimulation 2
    Comfort 1
}
```

---

### `set_monster_dresser`
**Name:** Monster Dresser  
**Description:** FURNITURE_DESC_SET_MONSTER_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_monster_dresser { //frame 111
    name FURNITURE_NAME_SET_MONSTER_DRESSER
    desc FURNITURE_DESC_SET_MONSTER_DRESSER
    set monster
    
    Appeal -2
    Stimulation 1
    Comfort 1
	Evolution 1
}
```

---

### `set_monster_table`
**Name:** Monster Table A  
**Description:** FURNITURE_DESC_SET_MONSTER_TABLE  
**Source:** `furniture_effects.gon`  

```
set_monster_table { //frame 112
    name FURNITURE_NAME_SET_MONSTER_TABLE
    desc FURNITURE_DESC_SET_MONSTER_TABLE
    set monster
    
    Appeal -2
    Stimulation 1
    Comfort 1
	Evolution 1
}
```

---

### `set_monster_suspendedshelf`
**Name:** Suspended Monster Shelf A  
**Description:** FURNITURE_DESC_SET_MONSTER_SUSPENDEDSHELF  
**Source:** `furniture_effects.gon`  

```
set_monster_suspendedshelf { //frame 113
    name FURNITURE_NAME_SET_MONSTER_SUSPENDEDSHELF
    desc FURNITURE_DESC_SET_MONSTER_SUSPENDEDSHELF
    set monster
    
    Appeal -2
    Stimulation 1
    Comfort 1
	Evolution 1
}
```

---

### `set_monster_sidetable`
**Name:** Monster Side Table  
**Description:** FURNITURE_DESC_SET_MONSTER_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_monster_sidetable { //frame 114
    name FURNITURE_NAME_SET_MONSTER_SIDETABLE
    desc FURNITURE_DESC_SET_MONSTER_SIDETABLE
    set monster
    
    Appeal -2
    Stimulation 1
    Comfort 1
	Evolution 1
}
```

---

### `set_monster_suspendedshelf2`
**Name:** Suspended Monster Shelf B  
**Description:** FURNITURE_DESC_SET_MONSTER_SUSPENDEDSHELF2  
**Source:** `furniture_effects.gon`  

```
set_monster_suspendedshelf2 { //frame 115
    name FURNITURE_NAME_SET_MONSTER_SUSPENDEDSHELF2
    desc FURNITURE_DESC_SET_MONSTER_SUSPENDEDSHELF2
    set monster
    
    Appeal -2
    Stimulation 1
    Comfort 1
	Evolution 1
}
```

---

### `set_monster_chair`
**Name:** Monster Chair  
**Description:** FURNITURE_DESC_SET_MONSTER_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_monster_chair { //frame 116
    name FURNITURE_NAME_SET_MONSTER_CHAIR
    desc FURNITURE_DESC_SET_MONSTER_CHAIR
    set monster
    
    Appeal -2
    Stimulation 1
    Comfort 1
	Evolution 1
}
```

---

### `set_monster_table2`
**Name:** Monster Table B  
**Description:** FURNITURE_DESC_SET_MONSTER_TABLE2  
**Source:** `furniture_effects.gon`  

```
set_monster_table2 { //frame 117
    name FURNITURE_NAME_SET_MONSTER_TABLE2
    desc FURNITURE_DESC_SET_MONSTER_TABLE2
    set monster
    
    Appeal -2
    Stimulation 1
    Comfort 1
	Evolution 1
}
```

---

### `set_monster_tv`
**Name:** Monster TV  
**Description:** FURNITURE_DESC_SET_MONSTER_TV  
**Source:** `furniture_effects.gon`  

```
set_monster_tv { //frame 118
    name FURNITURE_NAME_SET_MONSTER_TV
    desc FURNITURE_DESC_SET_MONSTER_TV
    set monster
    
    Appeal -2
    Stimulation 1
    Comfort 1
	Evolution 1
}
```

---

### `set_monster_lamp`
**Name:** Monster Lamp  
**Description:** FURNITURE_DESC_SET_MONSTER_LAMP  
**Source:** `furniture_effects.gon`  

```
set_monster_lamp { //frame 119
    name FURNITURE_NAME_SET_MONSTER_LAMP
    desc FURNITURE_DESC_SET_MONSTER_LAMP
    set monster
    
    Appeal -2
    Stimulation 1
    Comfort 1
	Evolution 1
}
```

---

### `set_angelic_bed`
**Name:** Angelic Bed  
**Description:** FURNITURE_DESC_SET_ANGELIC_BED  
**Source:** `furniture_effects.gon`  

```
set_angelic_bed { //frame 120
    name FURNITURE_NAME_SET_ANGELIC_BED
    desc FURNITURE_DESC_SET_ANGELIC_BED
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_angelic_shelf`
**Name:** Angelic Shelf  
**Description:** FURNITURE_DESC_SET_ANGELIC_SHELF  
**Source:** `furniture_effects.gon`  

```
set_angelic_shelf { //frame 121
    name FURNITURE_NAME_SET_ANGELIC_SHELF
    desc FURNITURE_DESC_SET_ANGELIC_SHELF
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_angelic_chair`
**Name:** Angelic Chair  
**Description:** FURNITURE_DESC_SET_ANGELIC_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_angelic_chair { //frame 122
    name FURNITURE_NAME_SET_ANGELIC_CHAIR
    desc FURNITURE_DESC_SET_ANGELIC_CHAIR
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_angelic_dresser`
**Name:** Angelic Dresser  
**Description:** FURNITURE_DESC_SET_ANGELIC_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_angelic_dresser { //frame 123
    name FURNITURE_NAME_SET_ANGELIC_DRESSER
    desc FURNITURE_DESC_SET_ANGELIC_DRESSER
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_angelic_sidetable`
**Name:** Angelic Side Table  
**Description:** FURNITURE_DESC_SET_ANGELIC_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_angelic_sidetable { //frame 124
    name FURNITURE_NAME_SET_ANGELIC_SIDETABLE
    desc FURNITURE_DESC_SET_ANGELIC_SIDETABLE
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_angelic_toilet`
**Name:** Angelic Toilet  
**Description:** FURNITURE_DESC_SET_ANGELIC_TOILET  
**Source:** `furniture_effects.gon`  

```
set_angelic_toilet { //frame 125
    name FURNITURE_NAME_SET_ANGELIC_TOILET
    desc FURNITURE_DESC_SET_ANGELIC_TOILET
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_angelic_table`
**Name:** Angelic Table A  
**Description:** FURNITURE_DESC_SET_ANGELIC_TABLE  
**Source:** `furniture_effects.gon`  

```
set_angelic_table { //frame 126
    name FURNITURE_NAME_SET_ANGELIC_TABLE
    desc FURNITURE_DESC_SET_ANGELIC_TABLE
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_angelic_table2`
**Name:** Angelic Table B  
**Description:** FURNITURE_DESC_SET_ANGELIC_TABLE2  
**Source:** `furniture_effects.gon`  

```
set_angelic_table2 { //frame 127
    name FURNITURE_NAME_SET_ANGELIC_TABLE2
    desc FURNITURE_DESC_SET_ANGELIC_TABLE2
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_angelic_suspendedshelf`
**Name:** Suspended Angelic Shelf  
**Description:** FURNITURE_DESC_SET_ANGELIC_SUSPENDEDSHELF  
**Source:** `furniture_effects.gon`  

```
set_angelic_suspendedshelf { //frame 128
    name FURNITURE_NAME_SET_ANGELIC_SUSPENDEDSHELF
    desc FURNITURE_DESC_SET_ANGELIC_SUSPENDEDSHELF
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_angelic_lamp`
**Name:** Angelic Lamp  
**Description:** FURNITURE_DESC_SET_ANGELIC_LAMP  
**Source:** `furniture_effects.gon`  

```
set_angelic_lamp { //frame 129
    name FURNITURE_NAME_SET_ANGELIC_LAMP
    desc FURNITURE_DESC_SET_ANGELIC_LAMP
    set angelic
    
    Appeal 2
    Comfort 1
    Stimulation -2
	Health 1
}
```

---

### `set_atomic_stove`
**Name:** Atomic Stove  
**Description:** FURNITURE_DESC_SET_ATOMIC_STOVE  
**Source:** `furniture_effects.gon`  

```
set_atomic_stove { //frame 130
    name FURNITURE_NAME_SET_ATOMIC_STOVE
    desc FURNITURE_DESC_SET_ATOMIC_STOVE
    set atomic
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_atomic_frige`
**Name:** Atomic Fridge  
**Description:** FURNITURE_DESC_SET_ATOMIC_FRIGE  
**Source:** `furniture_effects.gon`  

```
set_atomic_frige { //frame 131
    name FURNITURE_NAME_SET_ATOMIC_FRIGE
    desc FURNITURE_DESC_SET_ATOMIC_FRIGE
    set atomic
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_atomic_couch`
**Name:** Atomic Couch  
**Description:** FURNITURE_DESC_SET_ATOMIC_COUCH  
**Source:** `furniture_effects.gon`  

```
set_atomic_couch { //frame 132
    name FURNITURE_NAME_SET_ATOMIC_COUCH
    desc FURNITURE_DESC_SET_ATOMIC_COUCH
    set atomic
    
    Appeal 1
    Comfort 1
}
```

---

### `set_atomic_tv`
**Name:** Atomic TV  
**Description:** FURNITURE_DESC_SET_ATOMIC_TV  
**Source:** `furniture_effects.gon`  

```
set_atomic_tv { //frame 133
    name FURNITURE_NAME_SET_ATOMIC_TV
    desc FURNITURE_DESC_SET_ATOMIC_TV
    set atomic
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_atomic_table`
**Name:** Atomic Table  
**Description:** FURNITURE_DESC_SET_ATOMIC_TABLE  
**Source:** `furniture_effects.gon`  

```
set_atomic_table { //frame 134
    name FURNITURE_NAME_SET_ATOMIC_TABLE
    desc FURNITURE_DESC_SET_ATOMIC_TABLE
    set atomic
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_atomic_sidetable`
**Name:** Atomic Side Table  
**Description:** FURNITURE_DESC_SET_ATOMIC_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_atomic_sidetable { //frame 135
    name FURNITURE_NAME_SET_ATOMIC_SIDETABLE
    desc FURNITURE_DESC_SET_ATOMIC_SIDETABLE
    set atomic
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_atomic_radio`
**Name:** Atomic Radio  
**Description:** FURNITURE_DESC_SET_ATOMIC_RADIO  
**Source:** `furniture_effects.gon`  

```
set_atomic_radio { //frame 136
    name FURNITURE_NAME_SET_ATOMIC_RADIO
    desc FURNITURE_DESC_SET_ATOMIC_RADIO
    set atomic
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_atomic_lamp`
**Name:** Atomic Lamp  
**Description:** FURNITURE_DESC_SET_ATOMIC_LAMP  
**Source:** `furniture_effects.gon`  

```
set_atomic_lamp { //frame 137
    name FURNITURE_NAME_SET_ATOMIC_LAMP
    desc FURNITURE_DESC_SET_ATOMIC_LAMP
    set atomic
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_atomic_shelf`
**Name:** Atomic Shelf  
**Description:** FURNITURE_DESC_SET_ATOMIC_SHELF  
**Source:** `furniture_effects.gon`  

```
set_atomic_shelf { //frame 138
    name FURNITURE_NAME_SET_ATOMIC_SHELF
    desc FURNITURE_DESC_SET_ATOMIC_SHELF
    set atomic
    
    Appeal 1
    Stimulation 1
}
```

---

### `set_atomic_chair`
**Name:** Atomic Chair  
**Description:** FURNITURE_DESC_SET_ATOMIC_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_atomic_chair { //frame 139
    name FURNITURE_NAME_SET_ATOMIC_CHAIR
    desc FURNITURE_DESC_SET_ATOMIC_CHAIR
    set atomic
    
    Appeal 1
    Comfort 1
}
```

---

### `set_elegant_table`
**Name:** Elegant Table  
**Description:** FURNITURE_DESC_SET_ELEGANT_TABLE  
**Source:** `furniture_effects.gon`  

```
set_elegant_table { //frame 140
    name FURNITURE_NAME_SET_ELEGANT_TABLE
    desc FURNITURE_DESC_SET_ELEGANT_TABLE
    set elegant
    
    Appeal 2
}
```

---

### `set_elegant_bed`
**Name:** Elegant Bed  
**Description:** FURNITURE_DESC_SET_ELEGANT_BED  
**Source:** `furniture_effects.gon`  

```
set_elegant_bed { //frame 141
    name FURNITURE_NAME_SET_ELEGANT_BED
    desc FURNITURE_DESC_SET_ELEGANT_BED
    set elegant
    
    Appeal 1
    Comfort 1
}
```

---

### `set_elegant_desk`
**Name:** Elegant Desk  
**Description:** FURNITURE_DESC_SET_ELEGANT_DESK  
**Source:** `furniture_effects.gon`  

```
set_elegant_desk { //frame 142
    name FURNITURE_NAME_SET_ELEGANT_DESK
    desc FURNITURE_DESC_SET_ELEGANT_DESK
    set elegant
    
    Appeal 2
}
```

---

### `set_elegant_dresser`
**Name:** Elegant Dresser A  
**Description:** FURNITURE_DESC_SET_ELEGANT_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_elegant_dresser { //frame 143
    name FURNITURE_NAME_SET_ELEGANT_DRESSER
    desc FURNITURE_DESC_SET_ELEGANT_DRESSER
    set elegant
    
    Appeal 2
}
```

---

### `set_elegant_dresser2`
**Name:** Elegant Dresser B  
**Description:** FURNITURE_DESC_SET_ELEGANT_DRESSER2  
**Source:** `furniture_effects.gon`  

```
set_elegant_dresser2 { //frame 144
    name FURNITURE_NAME_SET_ELEGANT_DRESSER2
    desc FURNITURE_DESC_SET_ELEGANT_DRESSER2
    set elegant
    
    Appeal 2
}
```

---

### `set_elegant_sidetable`
**Name:** Elegant Side Table A  
**Description:** FURNITURE_DESC_SET_ELEGANT_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_elegant_sidetable { //frame 145
    name FURNITURE_NAME_SET_ELEGANT_SIDETABLE
    desc FURNITURE_DESC_SET_ELEGANT_SIDETABLE
    set elegant
    
    Appeal 2
}
```

---

### `set_elegant_sidetable2`
**Name:** Elegant Side Table B  
**Description:** FURNITURE_DESC_SET_ELEGANT_SIDETABLE2  
**Source:** `furniture_effects.gon`  

```
set_elegant_sidetable2 { //frame 146
    name FURNITURE_NAME_SET_ELEGANT_SIDETABLE2
    desc FURNITURE_DESC_SET_ELEGANT_SIDETABLE2
    set elegant
    
    Appeal 2
}
```

---

### `set_elegant_chair`
**Name:** Elegant Chair  
**Description:** FURNITURE_DESC_SET_ELEGANT_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_elegant_chair { //frame 147
    name FURNITURE_NAME_SET_ELEGANT_CHAIR
    desc FURNITURE_DESC_SET_ELEGANT_CHAIR
    set elegant
    
    Appeal 1
    Comfort 1
}
```

---

### `set_elegant_shelf`
**Name:** Elegant Shelf  
**Description:** FURNITURE_DESC_SET_ELEGANT_SHELF  
**Source:** `furniture_effects.gon`  

```
set_elegant_shelf { //frame 148
    name FURNITURE_NAME_SET_ELEGANT_SHELF
    desc FURNITURE_DESC_SET_ELEGANT_SHELF
    set elegant
    
    Appeal 2
}
```

---

### `set_elegant_lamp`
**Name:** Elegant Lamp  
**Description:** FURNITURE_DESC_SET_ELEGANT_LAMP  
**Source:** `furniture_effects.gon`  

```
set_elegant_lamp { //frame 149
    name FURNITURE_NAME_SET_ELEGANT_LAMP
    desc FURNITURE_DESC_SET_ELEGANT_LAMP
    set elegant
    
    Appeal 2
}
```

---

### `set_modern_bed`
**Name:** Modern Bed  
**Description:** FURNITURE_DESC_SET_MODERN_BED  
**Source:** `furniture_effects.gon`  

```
set_modern_bed { //frame 150
    name FURNITURE_NAME_SET_MODERN_BED
    desc FURNITURE_DESC_SET_MODERN_BED
    set modern
    
    Comfort 2
}
```

---

### `set_modern_frige`
**Name:** Modern Fridge  
**Description:** FURNITURE_DESC_SET_MODERN_FRIGE  
**Source:** `furniture_effects.gon`  

```
set_modern_frige { //frame 151
    name FURNITURE_NAME_SET_MODERN_FRIGE
    desc FURNITURE_DESC_SET_MODERN_FRIGE
    set modern
    
    Comfort 1
    Appeal 1
}
```

---

### `set_modern_stove`
**Name:** Modern Stove  
**Description:** FURNITURE_DESC_SET_MODERN_STOVE  
**Source:** `furniture_effects.gon`  

```
set_modern_stove { //frame 152
    name FURNITURE_NAME_SET_MODERN_STOVE
    desc FURNITURE_DESC_SET_MODERN_STOVE
    set modern
    
    Comfort 1
    Appeal 1
}
```

---

### `set_modern_couch`
**Name:** Modern Couch  
**Description:** FURNITURE_DESC_SET_MODERN_COUCH  
**Source:** `furniture_effects.gon`  

```
set_modern_couch { //frame 153
    name FURNITURE_NAME_SET_MODERN_COUCH
    desc FURNITURE_DESC_SET_MODERN_COUCH
    set modern
    
    Comfort 1
    Appeal 1
}
```

---

### `set_modern_chair`
**Name:** Modern Chair  
**Description:** FURNITURE_DESC_SET_MODERN_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_modern_chair { //frame 154
    name FURNITURE_NAME_SET_MODERN_CHAIR
    desc FURNITURE_DESC_SET_MODERN_CHAIR
    set modern
    
    Comfort 1
    Appeal 1
}
```

---

### `set_modern_dresser`
**Name:** Modern Dresser  
**Description:** FURNITURE_DESC_SET_MODERN_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_modern_dresser { //frame 155
    name FURNITURE_NAME_SET_MODERN_DRESSER
    desc FURNITURE_DESC_SET_MODERN_DRESSER
    set modern
    
    Comfort 1
    Appeal 1
}
```

---

### `set_modern_sidetable`
**Name:** Modern Side Table  
**Description:** FURNITURE_DESC_SET_MODERN_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_modern_sidetable { //frame 156
    name FURNITURE_NAME_SET_MODERN_SIDETABLE
    desc FURNITURE_DESC_SET_MODERN_SIDETABLE
    set modern
    
    Comfort 1
    Appeal 1
}
```

---

### `set_modern_table`
**Name:** Modern Table  
**Description:** FURNITURE_DESC_SET_MODERN_TABLE  
**Source:** `furniture_effects.gon`  

```
set_modern_table { //frame 157
    name FURNITURE_NAME_SET_MODERN_TABLE
    desc FURNITURE_DESC_SET_MODERN_TABLE
    set modern
    
    Comfort 1
    Appeal 1
}
```

---

### `set_modern_desk`
**Name:** Modern Desk  
**Description:** FURNITURE_DESC_SET_MODERN_DESK  
**Source:** `furniture_effects.gon`  

```
set_modern_desk { //frame 158
    name FURNITURE_NAME_SET_MODERN_DESK
    desc FURNITURE_DESC_SET_MODERN_DESK
    set modern
    
    Comfort 1
    Appeal 1
}
```

---

### `set_modern_tv`
**Name:** Modern TV  
**Description:** FURNITURE_DESC_SET_MODERN_TV  
**Source:** `furniture_effects.gon`  

```
set_modern_tv { //frame 159
    name FURNITURE_NAME_SET_MODERN_TV
    desc FURNITURE_DESC_SET_MODERN_TV
    set modern
    
    Stimulation 1
    Appeal 1
}
```

---

### `set_80s_couch`
**Name:** 80s Couch  
**Description:** FURNITURE_DESC_SET_80S_COUCH  
**Source:** `furniture_effects.gon`  

```
set_80s_couch { //frame 160
    name FURNITURE_NAME_SET_80S_COUCH
    desc FURNITURE_DESC_SET_80S_COUCH
    set 80s
    
    Comfort 2
}
```

---

### `set_80s_bed`
**Name:** 80s Bed  
**Description:** FURNITURE_DESC_SET_80S_BED  
**Source:** `furniture_effects.gon`  

```
set_80s_bed { //frame 161
    name FURNITURE_NAME_SET_80S_BED
    desc FURNITURE_DESC_SET_80S_BED
    set 80s
    
    Comfort 2
}
```

---

### `set_80s_dresser`
**Name:** 80s Dresser  
**Description:** FURNITURE_DESC_SET_80S_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_80s_dresser { //frame 162
    name FURNITURE_NAME_SET_80S_DRESSER
    desc FURNITURE_DESC_SET_80S_DRESSER
    set 80s
    
    Comfort 2
}
```

---

### `set_80s_chair`
**Name:** 80s Chair  
**Description:** FURNITURE_DESC_SET_80S_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_80s_chair { //frame 163
    name FURNITURE_NAME_SET_80S_CHAIR
    desc FURNITURE_DESC_SET_80S_CHAIR
    set 80s
    
    Comfort 2
}
```

---

### `set_80s_stove`
**Name:** 80s Stove  
**Description:** FURNITURE_DESC_SET_80S_STOVE  
**Source:** `furniture_effects.gon`  

```
set_80s_stove { //frame 164
    name FURNITURE_NAME_SET_80S_STOVE
    desc FURNITURE_DESC_SET_80S_STOVE
    set 80s
    
    Comfort 2
}
```

---

### `set_80s_frige`
**Name:** 80s Fridge  
**Description:** FURNITURE_DESC_SET_80S_FRIGE  
**Source:** `furniture_effects.gon`  

```
set_80s_frige { //frame 165
    name FURNITURE_NAME_SET_80S_FRIGE
    desc FURNITURE_DESC_SET_80S_FRIGE
    set 80s
    
    Comfort 2
}
```

---

### `set_80s_shelf`
**Name:** 80s Shelf  
**Description:** FURNITURE_DESC_SET_80S_SHELF  
**Source:** `furniture_effects.gon`  

```
set_80s_shelf { //frame 166
    name FURNITURE_NAME_SET_80S_SHELF
    desc FURNITURE_DESC_SET_80S_SHELF
    set 80s
    
    Comfort 2
}
```

---

### `set_80s_tv`
**Name:** 80s TV  
**Description:** FURNITURE_DESC_SET_80S_TV  
**Source:** `furniture_effects.gon`  

```
set_80s_tv { //frame 167
    name FURNITURE_NAME_SET_80S_TV
    desc FURNITURE_DESC_SET_80S_TV
    set 80s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_80s_table`
**Name:** 80s Table  
**Description:** FURNITURE_DESC_SET_80S_TABLE  
**Source:** `furniture_effects.gon`  

```
set_80s_table { //frame 168
    name FURNITURE_NAME_SET_80S_TABLE
    desc FURNITURE_DESC_SET_80S_TABLE
    set 80s
    
    Comfort 2
}
```

---

### `set_80s_sidetable`
**Name:** 80s Side Table  
**Description:** FURNITURE_DESC_SET_80S_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_80s_sidetable { //frame 169
    name FURNITURE_NAME_SET_80S_SIDETABLE
    desc FURNITURE_DESC_SET_80S_SIDETABLE
    set 80s
    
    Comfort 2
}
```

---

### `set_retro_bed`
**Name:** Art Deco Bed  
**Description:** FURNITURE_DESC_SET_RETRO_BED  
**Source:** `furniture_effects.gon`  

```
set_retro_bed { //frame 170
    name FURNITURE_NAME_SET_RETRO_BED
    desc FURNITURE_DESC_SET_RETRO_BED
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_retro_stove`
**Name:** Art Deco Stove  
**Description:** FURNITURE_DESC_SET_RETRO_STOVE  
**Source:** `furniture_effects.gon`  

```
set_retro_stove { //frame 171
    name FURNITURE_NAME_SET_RETRO_STOVE
    desc FURNITURE_DESC_SET_RETRO_STOVE
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_retro_frige`
**Name:** Art Deco Fridge  
**Description:** FURNITURE_DESC_SET_RETRO_FRIGE  
**Source:** `furniture_effects.gon`  

```
set_retro_frige { //frame 172
    name FURNITURE_NAME_SET_RETRO_FRIGE
    desc FURNITURE_DESC_SET_RETRO_FRIGE
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_retro_couch`
**Name:** Art Deco Couch  
**Description:** FURNITURE_DESC_SET_RETRO_COUCH  
**Source:** `furniture_effects.gon`  

```
set_retro_couch { //frame 173
    name FURNITURE_NAME_SET_RETRO_COUCH
    desc FURNITURE_DESC_SET_RETRO_COUCH
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_retro_chair`
**Name:** Art Deco Chair  
**Description:** FURNITURE_DESC_SET_RETRO_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_retro_chair { //frame 174
    name FURNITURE_NAME_SET_RETRO_CHAIR
    desc FURNITURE_DESC_SET_RETRO_CHAIR
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_retro_dresser`
**Name:** Art Deco Dresser  
**Description:** FURNITURE_DESC_SET_RETRO_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_retro_dresser { //frame 175
    name FURNITURE_NAME_SET_RETRO_DRESSER
    desc FURNITURE_DESC_SET_RETRO_DRESSER
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_retro_dresser2`
**Name:** Art Deco Vanity  
**Description:** FURNITURE_DESC_SET_RETRO_DRESSER2  
**Source:** `furniture_effects.gon`  

```
set_retro_dresser2 { //frame 176
    name FURNITURE_NAME_SET_RETRO_DRESSER2
    desc FURNITURE_DESC_SET_RETRO_DRESSER2
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_retro_dresser3`
**Name:** Art Deco Armoire  
**Description:** FURNITURE_DESC_SET_RETRO_DRESSER3  
**Source:** `furniture_effects.gon`  

```
set_retro_dresser3 { //frame 177
    name FURNITURE_NAME_SET_RETRO_DRESSER3
    desc FURNITURE_DESC_SET_RETRO_DRESSER3
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_retro_sidetable`
**Name:** Art Deco Side Table  
**Description:** FURNITURE_DESC_SET_RETRO_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_retro_sidetable { //frame 178
    name FURNITURE_NAME_SET_RETRO_SIDETABLE
    desc FURNITURE_DESC_SET_RETRO_SIDETABLE
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_retro_lamp`
**Name:** Art Deco Lamp  
**Description:** FURNITURE_DESC_SET_RETRO_LAMP  
**Source:** `furniture_effects.gon`  

```
set_retro_lamp { //frame 179
    name FURNITURE_NAME_SET_RETRO_LAMP
    desc FURNITURE_DESC_SET_RETRO_LAMP
    set retro
    
    Comfort 1
    Appeal 1
}
```

---

### `set_90s_bed`
**Name:** 90s Bed  
**Description:** FURNITURE_DESC_SET_90S_BED  
**Source:** `furniture_effects.gon`  

```
set_90s_bed { //frame 180
    name FURNITURE_NAME_SET_90S_BED
    desc FURNITURE_DESC_SET_90S_BED
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_90s_cabinet`
**Name:** Suspended 90s Cabinet  
**Description:** FURNITURE_DESC_SET_90S_CABINET  
**Source:** `furniture_effects.gon`  

```
set_90s_cabinet { //frame 181
    name FURNITURE_NAME_SET_90S_CABINET
    desc FURNITURE_DESC_SET_90S_CABINET
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_90s_cabinet2`
**Name:** 90s Cabinet  
**Description:** FURNITURE_DESC_SET_90S_CABINET2  
**Source:** `furniture_effects.gon`  

```
set_90s_cabinet2 { //frame 182
    name FURNITURE_NAME_SET_90S_CABINET2
    desc FURNITURE_DESC_SET_90S_CABINET2
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_90s_sink`
**Name:** 90s Sink  
**Description:** FURNITURE_DESC_SET_90S_SINK  
**Source:** `furniture_effects.gon`  

```
set_90s_sink { //frame 183
    name FURNITURE_NAME_SET_90S_SINK
    desc FURNITURE_DESC_SET_90S_SINK
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_90s_stove`
**Name:** 90s Stove  
**Description:** FURNITURE_DESC_SET_90S_STOVE  
**Source:** `furniture_effects.gon`  

```
set_90s_stove { //frame 184
    name FURNITURE_NAME_SET_90S_STOVE
    desc FURNITURE_DESC_SET_90S_STOVE
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_90s_frige`
**Name:** 90s Fridge  
**Description:** FURNITURE_DESC_SET_90S_FRIGE  
**Source:** `furniture_effects.gon`  

```
set_90s_frige { //frame 185
    name FURNITURE_NAME_SET_90S_FRIGE
    desc FURNITURE_DESC_SET_90S_FRIGE
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_90s_shelf`
**Name:** 90s Shelf  
**Description:** FURNITURE_DESC_SET_90S_SHELF  
**Source:** `furniture_effects.gon`  

```
set_90s_shelf { //frame 186
    name FURNITURE_NAME_SET_90S_SHELF
    desc FURNITURE_DESC_SET_90S_SHELF
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_90s_suspendedshelf`
**Name:** Suspended 90s Shelf  
**Description:** FURNITURE_DESC_SET_90S_SUSPENDEDSHELF  
**Source:** `furniture_effects.gon`  

```
set_90s_suspendedshelf { //frame 187
    name FURNITURE_NAME_SET_90S_SUSPENDEDSHELF
    desc FURNITURE_DESC_SET_90S_SUSPENDEDSHELF
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_90s_chair`
**Name:** 90s Chair  
**Description:** FURNITURE_DESC_SET_90S_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_90s_chair { //frame 188
    name FURNITURE_NAME_SET_90S_CHAIR
    desc FURNITURE_DESC_SET_90S_CHAIR
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_90s_stool`
**Name:** 90s Stool  
**Description:** FURNITURE_DESC_SET_90S_STOOL  
**Source:** `furniture_effects.gon`  

```
set_90s_stool { //frame 189
    name FURNITURE_NAME_SET_90S_STOOL
    desc FURNITURE_DESC_SET_90S_STOOL
    set 90s
    
    Comfort 1
    Stimulation 1
}
```

---

### `set_mushroom_table1`
**Name:** Mushroom Table A  
**Description:** FURNITURE_DESC_SET_MUSHROOM_TABLE1  
**Source:** `furniture_effects.gon`  

```
set_mushroom_table1 { //frame 190
    name FURNITURE_NAME_SET_MUSHROOM_TABLE1
    desc FURNITURE_DESC_SET_MUSHROOM_TABLE1
    set mushroom
    
    Comfort 3
    Stimulation -1
}
```

---

### `set_mushroom_stool`
**Name:** Mushroom Stool A  
**Description:** FURNITURE_DESC_SET_MUSHROOM_STOOL  
**Source:** `furniture_effects.gon`  

```
set_mushroom_stool { //frame 191
    name FURNITURE_NAME_SET_MUSHROOM_STOOL
    desc FURNITURE_DESC_SET_MUSHROOM_STOOL
    set mushroom
    
    Comfort 3
    Stimulation -1
}
```

---

### `set_mushroom_stool2`
**Name:** Mushroom Stool B  
**Description:** FURNITURE_DESC_SET_MUSHROOM_STOOL2  
**Source:** `furniture_effects.gon`  

```
set_mushroom_stool2 { //frame 192
    name FURNITURE_NAME_SET_MUSHROOM_STOOL2
    desc FURNITURE_DESC_SET_MUSHROOM_STOOL2
    set mushroom
	
	Comfort 3
    Stimulation -1
}
```

---

### `set_mushroom_chair`
**Name:** Mushroom Chair  
**Description:** FURNITURE_DESC_SET_MUSHROOM_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_mushroom_chair { //frame 193
    name FURNITURE_NAME_SET_MUSHROOM_CHAIR
    desc FURNITURE_DESC_SET_MUSHROOM_CHAIR
    set mushroom
    
    Comfort 3
    Stimulation -1
}
```

---

### `set_mushroom_table`
**Name:** Mushroom Table B  
**Description:** FURNITURE_DESC_SET_MUSHROOM_TABLE  
**Source:** `furniture_effects.gon`  

```
set_mushroom_table { //frame 194
    name FURNITURE_NAME_SET_MUSHROOM_TABLE
    desc FURNITURE_DESC_SET_MUSHROOM_TABLE
    set mushroom
    
    Comfort 3
    Stimulation -1
}
```

---

### `set_mushroom_toilet`
**Name:** Mushroom Toilet  
**Description:** FURNITURE_DESC_SET_MUSHROOM_TOILET  
**Source:** `furniture_effects.gon`  

```
set_mushroom_toilet { //frame 195
    name FURNITURE_NAME_SET_MUSHROOM_TOILET
    desc FURNITURE_DESC_SET_MUSHROOM_TOILET
    set mushroom
    
    Comfort 3
    Stimulation -1
}
```

---

### `set_mushroom_shelf`
**Name:** Mushroom Shelf  
**Description:** FURNITURE_DESC_SET_MUSHROOM_SHELF  
**Source:** `furniture_effects.gon`  

```
set_mushroom_shelf { //frame 196
    name FURNITURE_NAME_SET_MUSHROOM_SHELF
    desc FURNITURE_DESC_SET_MUSHROOM_SHELF
    set mushroom
    
    Comfort 3
    Stimulation -1
}
```

---

### `set_mushroom_suspendedshelf`
**Name:** Suspended Mushroom Shelf A  
**Description:** FURNITURE_DESC_SET_MUSHROOM_SUSPENDEDSHELF  
**Source:** `furniture_effects.gon`  

```
set_mushroom_suspendedshelf { //frame 197
    name FURNITURE_NAME_SET_MUSHROOM_SUSPENDEDSHELF
    desc FURNITURE_DESC_SET_MUSHROOM_SUSPENDEDSHELF
    set mushroom
    
    Comfort 3
    Stimulation -1
}
```

---

### `set_mushroom_suspendedshelf2`
**Name:** Suspended Mushroom Shelf B  
**Description:** FURNITURE_DESC_SET_MUSHROOM_SUSPENDEDSHELF2  
**Source:** `furniture_effects.gon`  

```
set_mushroom_suspendedshelf2 { //frame 198
    name FURNITURE_NAME_SET_MUSHROOM_SUSPENDEDSHELF2
    desc FURNITURE_DESC_SET_MUSHROOM_SUSPENDEDSHELF2
    set mushroom
    
    Comfort 3
    Stimulation -1
}
```

---

### `set_mushroom_stool3`
**Name:** Mushroom Stool C  
**Description:** FURNITURE_DESC_SET_MUSHROOM_STOOL3  
**Source:** `furniture_effects.gon`  

```
set_mushroom_stool3 { //frame 199
    name FURNITURE_NAME_SET_MUSHROOM_STOOL3
    desc FURNITURE_DESC_SET_MUSHROOM_STOOL3
    set mushroom
    
    Comfort 3
    Stimulation -1
}
```

---

### `set_rustic_dresser`
**Name:** Rustic Dresser  
**Description:** FURNITURE_DESC_SET_RUSTIC_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_rustic_dresser { //frame 200
    name FURNITURE_NAME_SET_RUSTIC_DRESSER
    desc FURNITURE_DESC_SET_RUSTIC_DRESSER
    set rustic
    
    Appeal 2
}
```

---

### `set_rustic_shelf`
**Name:** Suspended Rustic Shelf A  
**Description:** FURNITURE_DESC_SET_RUSTIC_SHELF  
**Source:** `furniture_effects.gon`  

```
set_rustic_shelf { //frame 201
    name FURNITURE_NAME_SET_RUSTIC_SHELF
    desc FURNITURE_DESC_SET_RUSTIC_SHELF
    set rustic
    
    Appeal 2
}
```

---

### `set_rustic_suspendedshelf`
**Name:** Suspended Rustic Shelf B  
**Description:** FURNITURE_DESC_SET_RUSTIC_SUSPENDEDSHELF  
**Source:** `furniture_effects.gon`  

```
set_rustic_suspendedshelf { //frame 202
    name FURNITURE_NAME_SET_RUSTIC_SUSPENDEDSHELF
    desc FURNITURE_DESC_SET_RUSTIC_SUSPENDEDSHELF
    set rustic
    
    Appeal 2
}
```

---

### `set_rustic_sidetable`
**Name:** Rustic Side Table  
**Description:** FURNITURE_DESC_SET_RUSTIC_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_rustic_sidetable { //frame 203
    name FURNITURE_NAME_SET_RUSTIC_SIDETABLE
    desc FURNITURE_DESC_SET_RUSTIC_SIDETABLE
    set rustic
    
    Appeal 2
}
```

---

### `set_rustic_suspendedshelf2`
**Name:** Suspended Rustic Spice Rack  
**Description:** FURNITURE_DESC_SET_RUSTIC_SUSPENDEDSHELF2  
**Source:** `furniture_effects.gon`  

```
set_rustic_suspendedshelf2 { //frame 204
    name FURNITURE_NAME_SET_RUSTIC_SUSPENDEDSHELF2
    desc FURNITURE_DESC_SET_RUSTIC_SUSPENDEDSHELF2
    set rustic
    
    Appeal 2
}
```

---

### `set_rustic_chair`
**Name:** Rustic Chair  
**Description:** FURNITURE_DESC_SET_RUSTIC_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_rustic_chair { //frame 205
    name FURNITURE_NAME_SET_RUSTIC_CHAIR
    desc FURNITURE_DESC_SET_RUSTIC_CHAIR
    set rustic
    
    Appeal 2
}
```

---

### `set_rustic_desk`
**Name:** Rustic Desk  
**Description:** FURNITURE_DESC_SET_RUSTIC_DESK  
**Source:** `furniture_effects.gon`  

```
set_rustic_desk { //frame 206
    name FURNITURE_NAME_SET_RUSTIC_DESK
    desc FURNITURE_DESC_SET_RUSTIC_DESK
    set rustic
    
    Appeal 2
}
```

---

### `set_rustic_bench`
**Name:** Rustic Bench  
**Description:** FURNITURE_DESC_SET_RUSTIC_BENCH  
**Source:** `furniture_effects.gon`  

```
set_rustic_bench { //frame 207
    name FURNITURE_NAME_SET_RUSTIC_BENCH
    desc FURNITURE_DESC_SET_RUSTIC_BENCH
    set rustic
    
    Appeal 2
}
```

---

### `set_rustic_table`
**Name:** Rustic Table  
**Description:** FURNITURE_DESC_SET_RUSTIC_TABLE  
**Source:** `furniture_effects.gon`  

```
set_rustic_table { //frame 208
    name FURNITURE_NAME_SET_RUSTIC_TABLE
    desc FURNITURE_DESC_SET_RUSTIC_TABLE
    set rustic
    
    Appeal 2
}
```

---

### `set_rustic_stool`
**Name:** Rustic Stool  
**Description:** FURNITURE_DESC_SET_RUSTIC_STOOL  
**Source:** `furniture_effects.gon`  

```
set_rustic_stool { //frame 209
    name FURNITURE_NAME_SET_RUSTIC_STOOL
    desc FURNITURE_DESC_SET_RUSTIC_STOOL
    set rustic
    
    Appeal 2
}
```

---

### `set_cute_dresser`
**Name:** Cute Dresser  
**Description:** FURNITURE_DESC_SET_CUTE_DRESSER  
**Source:** `furniture_effects.gon`  

```
set_cute_dresser { //frame 210
    name FURNITURE_NAME_SET_CUTE_DRESSER
    desc FURNITURE_DESC_SET_CUTE_DRESSER
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `set_cute_sidetable`
**Name:** Cute Side Table A  
**Description:** FURNITURE_DESC_SET_CUTE_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
set_cute_sidetable { //frame 211
    name FURNITURE_NAME_SET_CUTE_SIDETABLE
    desc FURNITURE_DESC_SET_CUTE_SIDETABLE
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `set_cute_shelf`
**Name:** Cute Shelf  
**Description:** FURNITURE_DESC_SET_CUTE_SHELF  
**Source:** `furniture_effects.gon`  

```
set_cute_shelf { //frame 212
    name FURNITURE_NAME_SET_CUTE_SHELF
    desc FURNITURE_DESC_SET_CUTE_SHELF
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `set_cute_dresser2`
**Name:** Cute Armoire  
**Description:** FURNITURE_DESC_SET_CUTE_DRESSER2  
**Source:** `furniture_effects.gon`  

```
set_cute_dresser2 { //frame 213
    name FURNITURE_NAME_SET_CUTE_DRESSER2
    desc FURNITURE_DESC_SET_CUTE_DRESSER2
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `set_cute_couch`
**Name:** Cute Couch  
**Description:** FURNITURE_DESC_SET_CUTE_COUCH  
**Source:** `furniture_effects.gon`  

```
set_cute_couch { //frame 214
    name FURNITURE_NAME_SET_CUTE_COUCH
    desc FURNITURE_DESC_SET_CUTE_COUCH
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `set_cute_bed`
**Name:** Cute Bed  
**Description:** FURNITURE_DESC_SET_CUTE_BED  
**Source:** `furniture_effects.gon`  

```
set_cute_bed { //frame 215
    name FURNITURE_NAME_SET_CUTE_BED
    desc FURNITURE_DESC_SET_CUTE_BED
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `set_cute_chair`
**Name:** Cute Chair  
**Description:** FURNITURE_DESC_SET_CUTE_CHAIR  
**Source:** `furniture_effects.gon`  

```
set_cute_chair { //frame 216
    name FURNITURE_NAME_SET_CUTE_CHAIR
    desc FURNITURE_DESC_SET_CUTE_CHAIR
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `set_cute_stool`
**Name:** Cute Stool  
**Description:** FURNITURE_DESC_SET_CUTE_STOOL  
**Source:** `furniture_effects.gon`  

```
set_cute_stool { //frame 217
    name FURNITURE_NAME_SET_CUTE_STOOL
    desc FURNITURE_DESC_SET_CUTE_STOOL
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `set_cute_table2`
**Name:** Cute Coffee Table  
**Description:** FURNITURE_DESC_SET_CUTE_TABLE2  
**Source:** `furniture_effects.gon`  

```
set_cute_table2 { //frame 218
    name FURNITURE_NAME_SET_CUTE_TABLE2
    desc FURNITURE_DESC_SET_CUTE_TABLE2
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `set_cute_sidetable2`
**Name:** Cute Side Table B  
**Description:** FURNITURE_DESC_SET_CUTE_SIDETABLE2  
**Source:** `furniture_effects.gon`  

```
set_cute_sidetable2 { //frame 219
    name FURNITURE_NAME_SET_CUTE_SIDETABLE2
    desc FURNITURE_DESC_SET_CUTE_SIDETABLE2
    set cute
    
    Appeal 1
    Comfort 1
}
```

---

### `object_wood_table`
**Name:** Wood Table  
**Description:** FURNITURE_DESC_OBJECT_WOOD_TABLE  
**Source:** `furniture_effects.gon`  

```
object_wood_table { //frame 221
    name FURNITURE_NAME_OBJECT_WOOD_TABLE
    desc FURNITURE_DESC_OBJECT_WOOD_TABLE
	
	Comfort 2
}
```

---

### `object_statue_lion`
**Name:** Guardian Lion Statue  
**Description:** FURNITURE_DESC_OBJECT_STATUE_LION  
**Source:** `furniture_effects.gon`  

```
object_statue_lion { //frame 449
    name FURNITURE_NAME_OBJECT_STATUE_LION
    desc FURNITURE_DESC_OBJECT_STATUE_LION
    
    Appeal 2
    Stimulation 2
    Comfort -2
}
```

---

### `object_statue_Jesus`
**Name:** Christ the Redeemer Statue  
**Description:** FURNITURE_DESC_OBJECT_STATUE_JESUS  
**Source:** `furniture_effects.gon`  

```
object_statue_Jesus { //frame 450
    name FURNITURE_NAME_OBJECT_STATUE_JESUS
    desc FURNITURE_DESC_OBJECT_STATUE_JESUS
    
    Appeal 2
    Health 2
    Comfort -2
}
```

---

### `object_statue_devil`
**Name:** Baphomet Statue  
**Description:** FURNITURE_DESC_OBJECT_STATUE_DEVIL  
**Source:** `furniture_effects.gon`  

```
object_statue_devil { //frame 451
    name FURNITURE_NAME_OBJECT_STATUE_DEVIL
    desc FURNITURE_DESC_OBJECT_STATUE_DEVIL
    
    Appeal 6
    Comfort -6
}
```

---

### `object_statue_mermaid`
**Name:** The Little Mermaid Statue  
**Description:** FURNITURE_DESC_OBJECT_STATUE_MERMAID  
**Source:** `furniture_effects.gon`  

```
object_statue_mermaid { //frame 452
    name FURNITURE_NAME_OBJECT_STATUE_MERMAID
    desc FURNITURE_DESC_OBJECT_STATUE_MERMAID
    
    Appeal 2
    Stimulation 2
    Comfort -2
}
```

---

### `object_statue_lotus`
**Name:** Lord Shiva Statue  
**Description:** FURNITURE_DESC_OBJECT_STATUE_LOTUS  
**Source:** `furniture_effects.gon`  

```
object_statue_lotus { //frame 453
    name FURNITURE_NAME_OBJECT_STATUE_LOTUS
    desc FURNITURE_DESC_OBJECT_STATUE_LOTUS
    
    Appeal 2
    Stimulation 2
    Comfort -2
}
```

---

### `object_statue_buddah`
**Name:** Laughing Buddha Statue  
**Description:** FURNITURE_DESC_OBJECT_STATUE_BUDDAH  
**Source:** `furniture_effects.gon`  

```
object_statue_buddah { //frame 454
    name FURNITURE_NAME_OBJECT_STATUE_BUDDAH
    desc FURNITURE_DESC_OBJECT_STATUE_BUDDAH
    
    Appeal 2
    Stimulation 2
    Comfort -2
}
```

---

### `object_statue_luckycat`
**Name:** Maneki Neko Statue  
**Description:** FURNITURE_DESC_OBJECT_STATUE_LUCKYCAT  
**Source:** `furniture_effects.gon`  

```
object_statue_luckycat { //frame 455
    name FURNITURE_NAME_OBJECT_STATUE_LUCKYCAT
    desc FURNITURE_DESC_OBJECT_STATUE_LUCKYCAT
    
    Appeal 1
    Stimulation 1
    Comfort -1
}
```

---

### `object_statue_bast`
**Name:** Bastet Statue  
**Description:** FURNITURE_DESC_OBJECT_STATUE_BAST  
**Source:** `furniture_effects.gon`  

```
object_statue_bast { //frame 456
    name FURNITURE_NAME_OBJECT_STATUE_BAST
    desc FURNITURE_DESC_OBJECT_STATUE_BAST
    
    Appeal 1
    Stimulation 1
    Comfort -1
}
```

---

### `object_statue_daruma`
**Name:** Daruma Statue  
**Description:** FURNITURE_DESC_OBJECT_STATUE_DARUMA  
**Source:** `furniture_effects.gon`  

```
object_statue_daruma { //frame 457
    name FURNITURE_NAME_OBJECT_STATUE_DARUMA
    desc FURNITURE_DESC_OBJECT_STATUE_DARUMA
    
    Appeal 1
    Stimulation 1
    Comfort -1
}
```

---

### `object_statue_easterislandsmall`
**Name:** Small Easter Island Head  
**Description:** FURNITURE_DESC_OBJECT_STATUE_EASTERISLANDSMALL  
**Source:** `furniture_effects.gon`  

```
object_statue_easterislandsmall { //frame 458
    name FURNITURE_NAME_OBJECT_STATUE_EASTERISLANDSMALL
    desc FURNITURE_DESC_OBJECT_STATUE_EASTERISLANDSMALL
    
    Appeal 1
    Stimulation 1
    Comfort -1
}
```

---

### `object_statue_easterislandmedium`
**Name:** Medium Easter Island Head  
**Description:** FURNITURE_DESC_OBJECT_STATUE_EASTERISLANDMEDIUM  
**Source:** `furniture_effects.gon`  

```
object_statue_easterislandmedium { //frame 459
    name FURNITURE_NAME_OBJECT_STATUE_EASTERISLANDMEDIUM
    desc FURNITURE_DESC_OBJECT_STATUE_EASTERISLANDMEDIUM

    Appeal 2
    Stimulation 2
    Comfort -2    
}
```

---

### `object_statue_easterislandlarge`
**Name:** Large Easter Island Head  
**Description:** FURNITURE_DESC_OBJECT_STATUE_EASTERISLANDLARGE  
**Source:** `furniture_effects.gon`  

```
object_statue_easterislandlarge { //frame 460
    name FURNITURE_NAME_OBJECT_STATUE_EASTERISLANDLARGE
    desc FURNITURE_DESC_OBJECT_STATUE_EASTERISLANDLARGE
    
    Appeal 3
    Stimulation 3
    Comfort -4
}
```

---

### `object_vase_large`
**Name:** Large Empty Vase  
**Description:** FURNITURE_DESC_OBJECT_VASE_LARGE  
**Source:** `furniture_effects.gon`  

```
object_vase_large { //frame 461
    name FURNITURE_NAME_OBJECT_VASE_LARGE
    desc FURNITURE_DESC_OBJECT_VASE_LARGE
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_tentacle`
**Name:** Potted Tentacle  
**Description:** FURNITURE_DESC_OBJECT_PLANT_TENTACLE  
**Source:** `furniture_effects.gon`  

```
object_plant_tentacle { //frame 462
    name FURNITURE_NAME_OBJECT_PLANT_TENTACLE
    desc FURNITURE_DESC_OBJECT_PLANT_TENTACLE
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_monstera`
**Name:** Potted Monstera  
**Description:** FURNITURE_DESC_OBJECT_PLANT_MONSTERA  
**Source:** `furniture_effects.gon`  

```
object_plant_monstera { //frame 463
    name FURNITURE_NAME_OBJECT_PLANT_MONSTERA
    desc FURNITURE_DESC_OBJECT_PLANT_MONSTERA
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_spikey`
**Name:** Potted Dracaena  
**Description:** FURNITURE_DESC_OBJECT_PLANT_SPIKEY  
**Source:** `furniture_effects.gon`  

```
object_plant_spikey { //frame 464
    name FURNITURE_NAME_OBJECT_PLANT_SPIKEY
    desc FURNITURE_DESC_OBJECT_PLANT_SPIKEY
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_bush`
**Name:** Potted Boxwood  
**Description:** FURNITURE_DESC_OBJECT_PLANT_BUSH  
**Source:** `furniture_effects.gon`  

```
object_plant_bush { //frame 465
    name FURNITURE_NAME_OBJECT_PLANT_BUSH
    desc FURNITURE_DESC_OBJECT_PLANT_BUSH
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_potato`
**Name:** Potted Potato  
**Description:** FURNITURE_DESC_OBJECT_PLANT_POTATO  
**Source:** `furniture_effects.gon`  

```
object_plant_potato { //frame 466
    name FURNITURE_NAME_OBJECT_PLANT_POTATO
    desc FURNITURE_DESC_OBJECT_PLANT_POTATO
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_flowers`
**Name:** Vase of Daisies  
**Description:** FURNITURE_DESC_OBJECT_PLANT_FLOWERS  
**Source:** `furniture_effects.gon`  

```
object_plant_flowers { //frame 467
    name FURNITURE_NAME_OBJECT_PLANT_FLOWERS
    desc FURNITURE_DESC_OBJECT_PLANT_FLOWERS
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_orchid`
**Name:** Potted Orchid  
**Description:** FURNITURE_DESC_OBJECT_PLANT_ORCHID  
**Source:** `furniture_effects.gon`  

```
object_plant_orchid { //frame 468
    name FURNITURE_NAME_OBJECT_PLANT_ORCHID
    desc FURNITURE_DESC_OBJECT_PLANT_ORCHID
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_daisy`
**Name:** Potted Daisy  
**Description:** FURNITURE_DESC_OBJECT_PLANT_DAISY  
**Source:** `furniture_effects.gon`  

```
object_plant_daisy { //frame 469
    name FURNITURE_NAME_OBJECT_PLANT_DAISY
    desc FURNITURE_DESC_OBJECT_PLANT_DAISY
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_rafflesia`
**Name:** Potted Rafflesia  
**Description:** FURNITURE_DESC_OBJECT_PLANT_RAFFLESIA  
**Source:** `furniture_effects.gon`  

```
object_plant_rafflesia { //frame 470
    name FURNITURE_NAME_OBJECT_PLANT_RAFFLESIA
    desc FURNITURE_DESC_OBJECT_PLANT_RAFFLESIA
    
    Appeal 1
    Comfort 1
    Stimulation -1
}
```

---

### `object_plant_piranhasplant`
**Name:** Potted Piranha Plant  
**Description:** FURNITURE_DESC_OBJECT_PLANT_PIRANHASPLANT  
**Source:** `furniture_effects.gon`  

```
object_plant_piranhasplant { //frame 471
    name FURNITURE_NAME_OBJECT_PLANT_PIRANHASPLANT
    desc FURNITURE_DESC_OBJECT_PLANT_PIRANHASPLANT
    
    Appeal 1
    Comfort -1
    Stimulation 1
}
```

---

### `object_plant_cactus`
**Name:** Potted Cactuar  
**Description:** FURNITURE_DESC_OBJECT_PLANT_CACTUS  
**Source:** `furniture_effects.gon`  

```
object_plant_cactus { //frame 472
    name FURNITURE_NAME_OBJECT_PLANT_CACTUS
    desc FURNITURE_DESC_OBJECT_PLANT_CACTUS
    
    Appeal 1
    Comfort -1
    Stimulation 1
}
```

---

### `object_fishtank_blowfish`
**Name:** Blowfish Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_BLOWFISH  
**Source:** `furniture_effects.gon`  

```
object_fishtank_blowfish { //frame 473
    name FURNITURE_NAME_OBJECT_FISHTANK_BLOWFISH
    desc FURNITURE_DESC_OBJECT_FISHTANK_BLOWFISH
    
    Stimulation 1
    Appeal 1
    Comfort -1
}
```

---

### `object_fishtank_catfish`
**Name:** Catfish Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_CATFISH  
**Source:** `furniture_effects.gon`  

```
object_fishtank_catfish { //frame 474
    name FURNITURE_NAME_OBJECT_FISHTANK_CATFISH
    desc FURNITURE_DESC_OBJECT_FISHTANK_CATFISH
    
    Stimulation 1
    Appeal 1
    Comfort -1
}
```

---

### `object_fishtank_booze`
**Name:** Booze Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_BOOZE  
**Source:** `furniture_effects.gon`  

```
object_fishtank_booze { //frame 475
    name FURNITURE_NAME_OBJECT_FISHTANK_BOOZE
    desc FURNITURE_DESC_OBJECT_FISHTANK_BOOZE
    
    Stimulation 1
    Appeal 1
    Comfort -1
}
```

---

### `object_fishtank_tadpoles`
**Name:** Tadpole Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_TADPOLES  
**Source:** `furniture_effects.gon`  

```
object_fishtank_tadpoles { //frame 476
    name FURNITURE_NAME_OBJECT_FISHTANK_TADPOLES
    desc FURNITURE_DESC_OBJECT_FISHTANK_TADPOLES
    
    Stimulation 1
    Appeal 1
    Comfort -1
}
```

---

### `object_fishtank_mermaid`
**Name:** Fiji Mermaid Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_MERMAID  
**Source:** `furniture_effects.gon`  

```
object_fishtank_mermaid { //frame 477
    name FURNITURE_NAME_OBJECT_FISHTANK_MERMAID
    desc FURNITURE_DESC_OBJECT_FISHTANK_MERMAID
    
    Stimulation 1
    Comfort -3
	Evolution 1
}
```

---

### `object_fishtank_whale`
**Name:** Baby Whale Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_WHALE  
**Source:** `furniture_effects.gon`  

```
object_fishtank_whale { //frame 478
    name FURNITURE_NAME_OBJECT_FISHTANK_WHALE
    desc FURNITURE_DESC_OBJECT_FISHTANK_WHALE
    
    Stimulation 1
    Appeal 1
    Comfort -1
}
```

---

### `object_fishtank_small_tadpoles`
**Name:** Small Tadpole Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_SMALL_TADPOLES  
**Source:** `furniture_effects.gon`  

```
object_fishtank_small_tadpoles { //frame 479
    name FURNITURE_NAME_OBJECT_FISHTANK_SMALL_TADPOLES
    desc FURNITURE_DESC_OBJECT_FISHTANK_SMALL_TADPOLES
    
    Stimulation 1
}
```

---

### `object_fishtank_small_poop`
**Name:** Small Poop Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_SMALL_POOP  
**Source:** `furniture_effects.gon`  

```
object_fishtank_small_poop { //frame 480
    name FURNITURE_NAME_OBJECT_FISHTANK_SMALL_POOP
    desc FURNITURE_DESC_OBJECT_FISHTANK_SMALL_POOP
    
    Stimulation 1
}
```

---

### `object_fishtank_small_skull`
**Name:** Small Skull Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_SMALL_SKULL  
**Source:** `furniture_effects.gon`  

```
object_fishtank_small_skull { //frame 481
    name FURNITURE_NAME_OBJECT_FISHTANK_SMALL_SKULL
    desc FURNITURE_DESC_OBJECT_FISHTANK_SMALL_SKULL
    
    Stimulation 1
}
```

---

### `object_fishtank_small_fish`
**Name:** Small Goldfish Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_SMALL_FISH  
**Source:** `furniture_effects.gon`  

```
object_fishtank_small_fish { //frame 482
    name FURNITURE_NAME_OBJECT_FISHTANK_SMALL_FISH
    desc FURNITURE_DESC_OBJECT_FISHTANK_SMALL_FISH
    
    Stimulation 1
}
```

---

### `object_fishtank_small_lilfish`
**Name:** Small Minnow Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_SMALL_LILFISH  
**Source:** `furniture_effects.gon`  

```
object_fishtank_small_lilfish { //frame 483
    name FURNITURE_NAME_OBJECT_FISHTANK_SMALL_LILFISH
    desc FURNITURE_DESC_OBJECT_FISHTANK_SMALL_LILFISH
    
    Stimulation 1
}
```

---

### `object_fishtank_small_lilfishes`
**Name:** Small Minnow Family Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_SMALL_LILFISHES  
**Source:** `furniture_effects.gon`  

```
object_fishtank_small_lilfishes { //frame 484
    name FURNITURE_NAME_OBJECT_FISHTANK_SMALL_LILFISHES
    desc FURNITURE_DESC_OBJECT_FISHTANK_SMALL_LILFISHES
    
    Stimulation 1
}
```

---

### `object_radio_30s`
**Name:** 30s Radio  
**Description:** FURNITURE_DESC_OBJECT_RADIO_30S  
**Source:** `furniture_effects.gon`  

```
object_radio_30s { //frame 485
    name FURNITURE_NAME_OBJECT_RADIO_30S
    desc FURNITURE_DESC_OBJECT_RADIO_30S
    
    Stimulation 2
    Comfort -1
}
```

---

### `object_radio_40s`
**Name:** 40s Radio  
**Description:** FURNITURE_DESC_OBJECT_RADIO_40S  
**Source:** `furniture_effects.gon`  

```
object_radio_40s { //frame 486
    name FURNITURE_NAME_OBJECT_RADIO_40S
    desc FURNITURE_DESC_OBJECT_RADIO_40S
    
    Stimulation 2
    Comfort -1
}
```

---

### `object_radio_50s`
**Name:** 50s Radio  
**Description:** FURNITURE_DESC_OBJECT_RADIO_50S  
**Source:** `furniture_effects.gon`  

```
object_radio_50s { //frame 487
    name FURNITURE_NAME_OBJECT_RADIO_50S
    desc FURNITURE_DESC_OBJECT_RADIO_50S
    
    Stimulation 2
    Comfort -1
}
```

---

### `object_radio_80s`
**Name:** 80s Radio  
**Description:** FURNITURE_DESC_OBJECT_RADIO_80S  
**Source:** `furniture_effects.gon`  

```
object_radio_80s { //frame 488
    name FURNITURE_NAME_OBJECT_RADIO_80S
    desc FURNITURE_DESC_OBJECT_RADIO_80S
    
    Stimulation 2
    Comfort -1
}
```

---

### `object_radio_atomic`
**Name:** Atomic Radio  
**Description:** FURNITURE_DESC_OBJECT_RADIO_ATOMIC  
**Source:** `furniture_effects.gon`  

```
object_radio_atomic { //frame 489
    name FURNITURE_NAME_OBJECT_RADIO_ATOMIC
    desc FURNITURE_DESC_OBJECT_RADIO_ATOMIC
    
    Stimulation 2
    Comfort -1
}
```

---

### `object_radio_70s`
**Name:** 70s Radio  
**Description:** FURNITURE_DESC_OBJECT_RADIO_70S  
**Source:** `furniture_effects.gon`  

```
object_radio_70s { //frame 490
    name FURNITURE_NAME_OBJECT_RADIO_70S
    desc FURNITURE_DESC_OBJECT_RADIO_70S
    
    Stimulation 2
    Comfort -1
}
```

---

### `object_radio_90s`
**Name:** 90s Radio  
**Description:** FURNITURE_DESC_OBJECT_RADIO_90S  
**Source:** `furniture_effects.gon`  

```
object_radio_90s { //frame 491
    name FURNITURE_NAME_OBJECT_RADIO_90S
    desc FURNITURE_DESC_OBJECT_RADIO_90S
    
    Stimulation 2
    Comfort -1
}
```

---

### `object_radio_60s`
**Name:** 60s Radio  
**Description:** FURNITURE_DESC_OBJECT_RADIO_60S  
**Source:** `furniture_effects.gon`  

```
object_radio_60s { //frame 492
    name FURNITURE_NAME_OBJECT_RADIO_60S
    desc FURNITURE_DESC_OBJECT_RADIO_60S
    
    Stimulation 2
    Comfort -1
}
```

---

### `object_taxidermy_pig`
**Name:** Taxidermy Pig  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_PIG  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_pig { //frame 493
    name FURNITURE_NAME_OBJECT_TAXIDERMY_PIG
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_PIG
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_bat`
**Name:** Taxidermy Bat  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_BAT  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_bat { //frame 494
    name FURNITURE_NAME_OBJECT_TAXIDERMY_BAT
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_BAT
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_fish`
**Name:** Taxidermy Cod  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_FISH  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_fish { //frame 495
    name FURNITURE_NAME_OBJECT_TAXIDERMY_FISH
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_FISH
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_bird`
**Name:** Taxidermy Pigeon  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_BIRD  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_bird { //frame 496
    name FURNITURE_NAME_OBJECT_TAXIDERMY_BIRD
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_BIRD
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_turtle`
**Name:** Taxidermy Turtle  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_TURTLE  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_turtle { //frame 497
    name FURNITURE_NAME_OBJECT_TAXIDERMY_TURTLE
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_TURTLE
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_lizard`
**Name:** Taxidermy Iguana  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_LIZARD  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_lizard { //frame 498
    name FURNITURE_NAME_OBJECT_TAXIDERMY_LIZARD
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_LIZARD
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_snake`
**Name:** Taxidermy Snake  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_SNAKE  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_snake { //frame 499
    name FURNITURE_NAME_OBJECT_TAXIDERMY_SNAKE
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_SNAKE
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_squirrel`
**Name:** Taxidermy Squirrel  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_SQUIRREL  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_squirrel { //frame 500
    name FURNITURE_NAME_OBJECT_TAXIDERMY_SQUIRREL
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_SQUIRREL
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_mouse`
**Name:** Taxidermy Mouse  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_MOUSE  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_mouse { //frame 501
    name FURNITURE_NAME_OBJECT_TAXIDERMY_MOUSE
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_MOUSE
    
    Appeal -1
    Health -2
	Evolution 1
	Stimulation 1
}
```

---

### `object_taxidermy_gopher`
**Name:** Taxidermy Gopher  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_GOPHER  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_gopher { //frame 502
    name FURNITURE_NAME_OBJECT_TAXIDERMY_GOPHER
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_GOPHER
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_crow`
**Name:** Taxidermy Crow  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_CROW  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_crow { //frame 503
    name FURNITURE_NAME_OBJECT_TAXIDERMY_CROW
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_CROW
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_taxidermy_rat`
**Name:** Taxidermy Rat  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_RAT  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_rat { //frame 504
    name FURNITURE_NAME_OBJECT_TAXIDERMY_RAT
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_RAT
    
    Appeal -1
    Health -2
	Evolution 1
}
```

---

### `object_electronics_monitor`
**Name:** PC Monitor  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_MONITOR  
**Source:** `furniture_effects.gon`  

```
object_electronics_monitor { //frame 505
    name FURNITURE_NAME_OBJECT_ELECTRONICS_MONITOR
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_MONITOR
    
    Stimulation 1
}
```

---

### `object_electronics_pc`
**Name:** PC  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_PC  
**Source:** `furniture_effects.gon`  

```
object_electronics_pc { //frame 506
    name FURNITURE_NAME_OBJECT_ELECTRONICS_PC
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_PC
    
    Stimulation 1
}
```

---

### `object_electronics_printer`
**Name:** Printer  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_PRINTER  
**Source:** `furniture_effects.gon`  

```
object_electronics_printer { //frame 507
    name FURNITURE_NAME_OBJECT_ELECTRONICS_PRINTER
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_PRINTER
    
    Stimulation 1
}
```

---

### `object_electronics_laptop`
**Name:** Laptop  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_LAPTOP  
**Source:** `furniture_effects.gon`  

```
object_electronics_laptop { //frame 508
    name FURNITURE_NAME_OBJECT_ELECTRONICS_LAPTOP
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_LAPTOP
    
    Stimulation 1
}
```

---

### `object_electronics_vhs`
**Name:** VHS Player  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_VHS  
**Source:** `furniture_effects.gon`  

```
object_electronics_vhs { //frame 509
    name FURNITURE_NAME_OBJECT_ELECTRONICS_VHS
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_VHS
    
    Stimulation 1
}
```

---

### `object_electronics_dvdplayer`
**Name:** DVD Player  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_DVDPLAYER  
**Source:** `furniture_effects.gon`  

```
object_electronics_dvdplayer { //frame 510
    name FURNITURE_NAME_OBJECT_ELECTRONICS_DVDPLAYER
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_DVDPLAYER
    
    Stimulation 1
}
```

---

### `object_electronics_speaker`
**Name:** Speaker  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_SPEAKER  
**Source:** `furniture_effects.gon`  

```
object_electronics_speaker { //frame 511
    name FURNITURE_NAME_OBJECT_ELECTRONICS_SPEAKER
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_SPEAKER
    
    Stimulation 1
}
```

---

### `object_books1`
**Name:** Books A  
**Description:** FURNITURE_DESC_OBJECT_BOOKS1  
**Source:** `furniture_effects.gon`  

```
object_books1 { //frame 512
    name FURNITURE_NAME_OBJECT_BOOKS1
    desc FURNITURE_DESC_OBJECT_BOOKS1
    
    Stimulation 2
    Appeal -1    
}
```

---

### `object_books2`
**Name:** Books B  
**Description:** FURNITURE_DESC_OBJECT_BOOKS2  
**Source:** `furniture_effects.gon`  

```
object_books2 { //frame 513
    name FURNITURE_NAME_OBJECT_BOOKS2
    desc FURNITURE_DESC_OBJECT_BOOKS2
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books3`
**Name:** Books C  
**Description:** FURNITURE_DESC_OBJECT_BOOKS3  
**Source:** `furniture_effects.gon`  

```
object_books3 { //frame 514
    name FURNITURE_NAME_OBJECT_BOOKS3
    desc FURNITURE_DESC_OBJECT_BOOKS3
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books4`
**Name:** Books D  
**Description:** FURNITURE_DESC_OBJECT_BOOKS4  
**Source:** `furniture_effects.gon`  

```
object_books4 { //frame 515
    name FURNITURE_NAME_OBJECT_BOOKS4
    desc FURNITURE_DESC_OBJECT_BOOKS4
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books5`
**Name:** Books E  
**Description:** FURNITURE_DESC_OBJECT_BOOKS5  
**Source:** `furniture_effects.gon`  

```
object_books5 { //frame 516
    name FURNITURE_NAME_OBJECT_BOOKS5
    desc FURNITURE_DESC_OBJECT_BOOKS5
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books6`
**Name:** Books F  
**Description:** FURNITURE_DESC_OBJECT_BOOKS6  
**Source:** `furniture_effects.gon`  

```
object_books6 { //frame 517
    name FURNITURE_NAME_OBJECT_BOOKS6
    desc FURNITURE_DESC_OBJECT_BOOKS6
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books7`
**Name:** Books G  
**Description:** FURNITURE_DESC_OBJECT_BOOKS7  
**Source:** `furniture_effects.gon`  

```
object_books7 { //frame 518
    name FURNITURE_NAME_OBJECT_BOOKS7
    desc FURNITURE_DESC_OBJECT_BOOKS7
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books8`
**Name:** Books H  
**Description:** FURNITURE_DESC_OBJECT_BOOKS8  
**Source:** `furniture_effects.gon`  

```
object_books8 { //frame 519
    name FURNITURE_NAME_OBJECT_BOOKS8
    desc FURNITURE_DESC_OBJECT_BOOKS8
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books9`
**Name:** Books I  
**Description:** FURNITURE_DESC_OBJECT_BOOKS9  
**Source:** `furniture_effects.gon`  

```
object_books9 { //frame 520
    name FURNITURE_NAME_OBJECT_BOOKS9
    desc FURNITURE_DESC_OBJECT_BOOKS9
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books10`
**Name:** Book  
**Description:** FURNITURE_DESC_OBJECT_BOOKS10  
**Source:** `furniture_effects.gon`  

```
object_books10 { //frame 521
    name FURNITURE_NAME_OBJECT_BOOKS10
    desc FURNITURE_DESC_OBJECT_BOOKS10
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books11`
**Name:** Books J  
**Description:** FURNITURE_DESC_OBJECT_BOOKS11  
**Source:** `furniture_effects.gon`  

```
object_books11 { //frame 522
    name FURNITURE_NAME_OBJECT_BOOKS11
    desc FURNITURE_DESC_OBJECT_BOOKS11
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_books12`
**Name:** Books K  
**Description:** FURNITURE_DESC_OBJECT_BOOKS12  
**Source:** `furniture_effects.gon`  

```
object_books12 { //frame 523
    name FURNITURE_NAME_OBJECT_BOOKS12
    desc FURNITURE_DESC_OBJECT_BOOKS12
    
    Stimulation 2
    Appeal -1  
}
```

---

### `object_plant_cutecactus`
**Name:** Potted Cactus  
**Description:** FURNITURE_DESC_OBJECT_PLANT_CUTECACTUS  
**Source:** `furniture_effects.gon`  

```
object_plant_cutecactus { //frame 524
    name FURNITURE_NAME_OBJECT_PLANT_CUTECACTUS
    desc FURNITURE_DESC_OBJECT_PLANT_CUTECACTUS
    
    Appeal 1
}
```

---

### `object_plant_sunflower`
**Name:** Potted Sunflower  
**Description:** FURNITURE_DESC_OBJECT_PLANT_SUNFLOWER  
**Source:** `furniture_effects.gon`  

```
object_plant_sunflower { //frame 525
    name FURNITURE_NAME_OBJECT_PLANT_SUNFLOWER
    desc FURNITURE_DESC_OBJECT_PLANT_SUNFLOWER
    
    Appeal 1
}
```

---

### `object_plant_mushroom`
**Name:** Potted Mushroom  
**Description:** FURNITURE_DESC_OBJECT_PLANT_MUSHROOM  
**Source:** `furniture_effects.gon`  

```
object_plant_mushroom { //frame 526
    name FURNITURE_NAME_OBJECT_PLANT_MUSHROOM
    desc FURNITURE_DESC_OBJECT_PLANT_MUSHROOM
    
    Appeal 1
}
```

---

### `object_plant_mushrooms`
**Name:** Potted Mushrooms  
**Description:** FURNITURE_DESC_OBJECT_PLANT_MUSHROOMS  
**Source:** `furniture_effects.gon`  

```
object_plant_mushrooms { //frame 527
    name FURNITURE_NAME_OBJECT_PLANT_MUSHROOMS
    desc FURNITURE_DESC_OBJECT_PLANT_MUSHROOMS
    
    Appeal 1
}
```

---

### `object_plant_bulb1`
**Name:** Potted Green Bulb  
**Description:** FURNITURE_DESC_OBJECT_PLANT_BULB1  
**Source:** `furniture_effects.gon`  

```
object_plant_bulb1 { //frame 528
    name FURNITURE_NAME_OBJECT_PLANT_BULB1
    desc FURNITURE_DESC_OBJECT_PLANT_BULB1
    
    Appeal 1
}
```

---

### `object_plant_bulb2`
**Name:** Potted Blue Bulb  
**Description:** FURNITURE_DESC_OBJECT_PLANT_BULB2  
**Source:** `furniture_effects.gon`  

```
object_plant_bulb2 { //frame 529
    name FURNITURE_NAME_OBJECT_PLANT_BULB2
    desc FURNITURE_DESC_OBJECT_PLANT_BULB2
    
    Appeal 1
}
```

---

### `object_plant_bulb3`
**Name:** Potted Yellow Bulb  
**Description:** FURNITURE_DESC_OBJECT_PLANT_BULB3  
**Source:** `furniture_effects.gon`  

```
object_plant_bulb3 { //frame 530
    name FURNITURE_NAME_OBJECT_PLANT_BULB3
    desc FURNITURE_DESC_OBJECT_PLANT_BULB3
    
    Appeal 1
}
```

---

### `object_plant_flytrap`
**Name:** Venus Flytrap  
**Description:** FURNITURE_DESC_OBJECT_PLANT_FLYTRAP  
**Source:** `furniture_effects.gon`  

```
object_plant_flytrap { //frame 531
    name FURNITURE_NAME_OBJECT_PLANT_FLYTRAP
    desc FURNITURE_DESC_OBJECT_PLANT_FLYTRAP
    
    Appeal 1
}
```

---

### `object_vase_dasiy`
**Name:** Flower Vase  
**Description:** FURNITURE_DESC_OBJECT_VASE_DASIY  
**Source:** `furniture_effects.gon`  

```
object_vase_dasiy { //frame 532
    name FURNITURE_NAME_OBJECT_VASE_DASIY
    desc FURNITURE_DESC_OBJECT_VASE_DASIY
    
    Appeal 1
}
```

---

### `object_vase_sticks`
**Name:** Branch Vase  
**Description:** FURNITURE_DESC_OBJECT_VASE_STICKS  
**Source:** `furniture_effects.gon`  

```
object_vase_sticks { //frame 533
    name FURNITURE_NAME_OBJECT_VASE_STICKS
    desc FURNITURE_DESC_OBJECT_VASE_STICKS
    
    Appeal 1
}
```

---

### `object_telephone_10s`
**Name:** Antique Telephone  
**Description:** FURNITURE_DESC_OBJECT_TELEPHONE_10S  
**Source:** `furniture_effects.gon`  

```
object_telephone_10s { //frame 534
    name FURNITURE_NAME_OBJECT_TELEPHONE_10S
    desc FURNITURE_DESC_OBJECT_TELEPHONE_10S
    
    Stimulation 1
}
```

---

### `object_coffen`
**Name:** Coffin  
**Description:** FURNITURE_DESC_OBJECT_COFFEN  
**Source:** `furniture_effects.gon`  

```
object_coffen { //frame 535
    name FURNITURE_NAME_OBJECT_COFFEN
    desc FURNITURE_DESC_OBJECT_COFFEN
    
	Health -2
}
```

---

### `object_barrel`
**Name:** Barrel  
**Description:** FURNITURE_DESC_OBJECT_BARREL  
**Source:** `furniture_effects.gon`  

```
object_barrel { //frame 536
    name FURNITURE_NAME_OBJECT_BARREL
    desc FURNITURE_DESC_OBJECT_BARREL
    
    Appeal 1
}
```

---

### `object_toxicwaste`
**Name:** Toxic Waste  
**Description:** FURNITURE_DESC_OBJECT_TOXICWASTE  
**Source:** `furniture_effects.gon`  

```
object_toxicwaste { //frame 537
    name FURNITURE_NAME_OBJECT_TOXICWASTE
    desc FURNITURE_DESC_OBJECT_TOXICWASTE
    
    Comfort -4
	Evolution 2
}
```

---

### `object_crate`
**Name:** Crate  
**Description:** FURNITURE_DESC_OBJECT_CRATE  
**Source:** `furniture_effects.gon`  

```
object_crate { //frame 538
    name FURNITURE_NAME_OBJECT_CRATE
    desc FURNITURE_DESC_OBJECT_CRATE
    
    Comfort 1
}
```

---

### `object_chest`
**Name:** Chest  
**Description:** FURNITURE_DESC_OBJECT_CHEST  
**Source:** `furniture_effects.gon`  

```
object_chest { //frame 539
    name FURNITURE_NAME_OBJECT_CHEST
    desc FURNITURE_DESC_OBJECT_CHEST
    
    Comfort 1
}
```

---

### `object_box`
**Name:** Cardboard Box  
**Description:** FURNITURE_DESC_OBJECT_BOX  
**Source:** `furniture_effects.gon`  

```
object_box { //frame 540
    name FURNITURE_NAME_OBJECT_BOX
    desc FURNITURE_DESC_OBJECT_BOX
    
    Comfort 1
}
```

---

### `object_electronics_microwave`
**Name:** Microwave A  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_MICROWAVE  
**Source:** `furniture_effects.gon`  

```
object_electronics_microwave { //frame 541
    name FURNITURE_NAME_OBJECT_ELECTRONICS_MICROWAVE
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_MICROWAVE
    
    Comfort 1
}
```

---

### `object_electronics_microwave2`
**Name:** Microwave B  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_MICROWAVE2  
**Source:** `furniture_effects.gon`  

```
object_electronics_microwave2 { //frame 542
    name FURNITURE_NAME_OBJECT_ELECTRONICS_MICROWAVE2
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_MICROWAVE2
    
    Comfort 1
}
```

---

### `object_electronics_microwave3`
**Name:** Microwave C  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_MICROWAVE3  
**Source:** `furniture_effects.gon`  

```
object_electronics_microwave3 { //frame 543
    name FURNITURE_NAME_OBJECT_ELECTRONICS_MICROWAVE3
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_MICROWAVE3
    
    Comfort 1
}
```

---

### `object_cinderblock1`
**Name:** Cinderblock  
**Description:** FURNITURE_DESC_OBJECT_CINDERBLOCK1  
**Source:** `furniture_effects.gon`  

```
object_cinderblock1 { //frame 544
    name FURNITURE_NAME_OBJECT_CINDERBLOCK1
    desc FURNITURE_DESC_OBJECT_CINDERBLOCK1
    
    Comfort 1
}
```

---

### `object_cinderblock2`
**Name:** Small Cinderblock  
**Description:** FURNITURE_DESC_OBJECT_CINDERBLOCK2  
**Source:** `furniture_effects.gon`  

```
object_cinderblock2 { //frame 545
    name FURNITURE_NAME_OBJECT_CINDERBLOCK2
    desc FURNITURE_DESC_OBJECT_CINDERBLOCK2
    
    Comfort 1
}
```

---

### `object_rock`
**Name:** Rock  
**Description:** FURNITURE_DESC_OBJECT_ROCK  
**Source:** `furniture_effects.gon`  

```
object_rock { //frame 546
    name FURNITURE_NAME_OBJECT_ROCK
    desc FURNITURE_DESC_OBJECT_ROCK
    
    Appeal 1
}
```

---

### `object_smallrock`
**Name:** Small Rock  
**Description:** FURNITURE_DESC_OBJECT_SMALLROCK  
**Source:** `furniture_effects.gon`  

```
object_smallrock { //frame 547
    name FURNITURE_NAME_OBJECT_SMALLROCK
    desc FURNITURE_DESC_OBJECT_SMALLROCK
    
    Appeal 1
}
```

---

### `object_diamond`
**Name:** Diamond  
**Description:** FURNITURE_DESC_OBJECT_DIAMOND  
**Source:** `furniture_effects.gon`  

```
object_diamond { //frame 548
    name FURNITURE_NAME_OBJECT_DIAMOND
    desc FURNITURE_DESC_OBJECT_DIAMOND
    
    Appeal 1
}
```

---

### `object_electronics_orb`
**Name:** Plasma Orb  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_ORB  
**Source:** `furniture_effects.gon`  

```
object_electronics_orb { //frame 549
    name FURNITURE_NAME_OBJECT_ELECTRONICS_ORB
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_ORB
    
    Stimulation 1
}
```

---

### `object_crystalball`
**Name:** Crystal Ball  
**Description:** FURNITURE_DESC_OBJECT_CRYSTALBALL  
**Source:** `furniture_effects.gon`  

```
object_crystalball { //frame 550
    name FURNITURE_NAME_OBJECT_CRYSTALBALL
    desc FURNITURE_DESC_OBJECT_CRYSTALBALL
    
    Stimulation 1
}
```

---

### `object_electronics_lavalamp`
**Name:** Lava Lamp  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_LAVALAMP  
**Source:** `furniture_effects.gon`  

```
object_electronics_lavalamp { //frame 551
    name FURNITURE_NAME_OBJECT_ELECTRONICS_LAVALAMP
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_LAVALAMP
    
    Appeal 1
}
```

---

### `object_electronics_fan`
**Name:** Small Fan  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_FAN  
**Source:** `furniture_effects.gon`  

```
object_electronics_fan { //frame 552
    name FURNITURE_NAME_OBJECT_ELECTRONICS_FAN
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_FAN
    
    Comfort 1
}
```

---

### `object_jar_empty`
**Name:** Broken Jar  
**Description:** FURNITURE_DESC_OBJECT_JAR_EMPTY  
**Source:** `furniture_effects.gon`  

```
object_jar_empty { //frame 553
    name FURNITURE_NAME_OBJECT_JAR_EMPTY
    desc FURNITURE_DESC_OBJECT_JAR_EMPTY
    
    Comfort 1
}
```

---

### `object_jar_head1`
**Name:** Head In Jar A  
**Description:** FURNITURE_DESC_OBJECT_JAR_HEAD1  
**Source:** `furniture_effects.gon`  

```
object_jar_head1 { //frame 554
    name FURNITURE_NAME_OBJECT_JAR_HEAD1
    desc FURNITURE_DESC_OBJECT_JAR_HEAD1
    
    Stimulation 1
}
```

---

### `object_jar_head2`
**Name:** Head In Jar B  
**Description:** FURNITURE_DESC_OBJECT_JAR_HEAD2  
**Source:** `furniture_effects.gon`  

```
object_jar_head2 { //frame 555
    name FURNITURE_NAME_OBJECT_JAR_HEAD2
    desc FURNITURE_DESC_OBJECT_JAR_HEAD2
    
    Stimulation 1
}
```

---

### `object_jar_eggs`
**Name:** Jar of Eggs  
**Description:** FURNITURE_DESC_OBJECT_JAR_EGGS  
**Source:** `furniture_effects.gon`  

```
object_jar_eggs { //frame 556
    name FURNITURE_NAME_OBJECT_JAR_EGGS
    desc FURNITURE_DESC_OBJECT_JAR_EGGS
    
    Comfort 1    
}
```

---

### `object_jar_cat`
**Name:** Conjoined Cat in Jar  
**Description:** FURNITURE_DESC_OBJECT_JAR_CAT  
**Source:** `furniture_effects.gon`  

```
object_jar_cat { //frame 557
    name FURNITURE_NAME_OBJECT_JAR_CAT
    desc FURNITURE_DESC_OBJECT_JAR_CAT
    
    Appeal 1
}
```

---

### `object_jar_fetus`
**Name:** Fetus in a Jar  
**Description:** FURNITURE_DESC_OBJECT_JAR_FETUS  
**Source:** `furniture_effects.gon`  

```
object_jar_fetus { //frame 558
    name FURNITURE_NAME_OBJECT_JAR_FETUS
    desc FURNITURE_DESC_OBJECT_JAR_FETUS
    
    Stimulation 1
}
```

---

### `object_log`
**Name:** Log  
**Description:** FURNITURE_DESC_OBJECT_LOG  
**Source:** `furniture_effects.gon`  

```
object_log { //frame 559
    name FURNITURE_NAME_OBJECT_LOG
    desc FURNITURE_DESC_OBJECT_LOG
    
    Comfort 1
}
```

---

### `object_food_ham`
**Name:** Ham  
**Description:** FURNITURE_DESC_OBJECT_FOOD_HAM  
**Source:** `furniture_effects.gon`  

```
object_food_ham { //frame 560
    name FURNITURE_NAME_OBJECT_FOOD_HAM
    desc FURNITURE_DESC_OBJECT_FOOD_HAM
    
    Comfort 1
}
```

---

### `object_food_turkey`
**Name:** Turkey  
**Description:** FURNITURE_DESC_OBJECT_FOOD_TURKEY  
**Source:** `furniture_effects.gon`  

```
object_food_turkey { //frame 561
    name FURNITURE_NAME_OBJECT_FOOD_TURKEY
    desc FURNITURE_DESC_OBJECT_FOOD_TURKEY
    
    Comfort 1
}
```

---

### `object_bug_cenipede`
**Name:** Centipede  
**Description:** FURNITURE_DESC_OBJECT_BUG_CENIPEDE  
**Source:** `furniture_effects.gon`  

```
object_bug_cenipede { //frame 562
    name FURNITURE_NAME_OBJECT_BUG_CENIPEDE
    desc FURNITURE_DESC_OBJECT_BUG_CENIPEDE
    
    Stimulation 1
    Appeal 1
    Comfort -1
}
```

---

### `object_bug_pillbug`
**Name:** Pillbug  
**Description:** FURNITURE_DESC_OBJECT_BUG_PILLBUG  
**Source:** `furniture_effects.gon`  

```
object_bug_pillbug { //frame 563
    name FURNITURE_NAME_OBJECT_BUG_PILLBUG
    desc FURNITURE_DESC_OBJECT_BUG_PILLBUG
    
    Stimulation 1
    Appeal 1
    Comfort -1
}
```

---

### `object_bug_spider`
**Name:** Black Widow  
**Description:** FURNITURE_DESC_OBJECT_BUG_SPIDER  
**Source:** `furniture_effects.gon`  

```
object_bug_spider { //frame 564
    name FURNITURE_NAME_OBJECT_BUG_SPIDER
    desc FURNITURE_DESC_OBJECT_BUG_SPIDER
    
    Stimulation 1
    Appeal 1
    Comfort -1
}
```

---

### `object_fishtank_chameleon`
**Name:** Chameleon  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_CHAMELEON  
**Source:** `furniture_effects.gon`  

```
object_fishtank_chameleon { //frame 565
    name FURNITURE_NAME_OBJECT_FISHTANK_CHAMELEON
    desc FURNITURE_DESC_OBJECT_FISHTANK_CHAMELEON
    
    Stimulation 1
    Appeal 1
    Comfort -1
}
```

---

### `object_gastank`
**Name:** Gas Tank  
**Description:** FURNITURE_DESC_OBJECT_GASTANK  
**Source:** `furniture_effects.gon`  

```
object_gastank { //frame 566
    name FURNITURE_NAME_OBJECT_GASTANK
    desc FURNITURE_DESC_OBJECT_GASTANK
    
    Stimulation 1
}
```

---

### `object_electronics_arcade1`
**Name:** Arcade Machine  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_ARCADE1  
**Source:** `furniture_effects.gon`  

```
object_electronics_arcade1 { //frame 567
    name FURNITURE_NAME_OBJECT_ELECTRONICS_ARCADE1
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_ARCADE1
    
    Appeal 1
    Stimulation 1
}
```

---

### `object_electronics_arcade2`
**Name:** Indie Arcade  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_ARCADE2  
**Source:** `furniture_effects.gon`  

```
object_electronics_arcade2 { //frame 568
    name FURNITURE_NAME_OBJECT_ELECTRONICS_ARCADE2
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_ARCADE2
    
    Appeal 1
    Stimulation 1
}
```

---

### `object_fortuneteller`
**Name:** Fortuneteller  
**Description:** FURNITURE_DESC_OBJECT_FORTUNETELLER  
**Source:** `furniture_effects.gon`  

```
object_fortuneteller { //frame 569
    name FURNITURE_NAME_OBJECT_FORTUNETELLER
    desc FURNITURE_DESC_OBJECT_FORTUNETELLER
    
    Appeal 1
    Stimulation 1
}
```

---

### `object_electronics_cranegame`
**Name:** Crane Game  
**Description:** FURNITURE_DESC_OBJECT_ELECTRONICS_CRANEGAME  
**Source:** `furniture_effects.gon`  

```
object_electronics_cranegame { //frame 570
    name FURNITURE_NAME_OBJECT_ELECTRONICS_CRANEGAME
    desc FURNITURE_DESC_OBJECT_ELECTRONICS_CRANEGAME
    
    Appeal 1
    Stimulation 1
}
```

---

### `object_outhouse`
**Name:** Outhouse  
**Description:** FURNITURE_DESC_OBJECT_OUTHOUSE  
**Source:** `furniture_effects.gon`  

```
object_outhouse { //frame 571
    name FURNITURE_NAME_OBJECT_OUTHOUSE
    desc FURNITURE_DESC_OBJECT_OUTHOUSE
    
    Comfort 3
    Appeal -1
}
```

---

### `object_potopotty`
**Name:** Pot O' Potty  
**Description:** FURNITURE_DESC_OBJECT_POTOPOTTY  
**Source:** `furniture_effects.gon`  

```
object_potopotty { //frame 572
    name FURNITURE_NAME_OBJECT_POTOPOTTY
    desc FURNITURE_DESC_OBJECT_POTOPOTTY
    
    Comfort 3
    Appeal -1
}
```

---

### `object_icechest`
**Name:** Ice Chest  
**Description:** FURNITURE_DESC_OBJECT_ICECHEST  
**Source:** `furniture_effects.gon`  

```
object_icechest { //frame 573
    name FURNITURE_NAME_OBJECT_ICECHEST
    desc FURNITURE_DESC_OBJECT_ICECHEST
    
    Comfort 1
}
```

---

### `object_fishtank_octocat`
**Name:** Octocat Aquarium  
**Description:** FURNITURE_DESC_OBJECT_FISHTANK_OCTOCAT  
**Source:** `furniture_effects.gon`  

```
object_fishtank_octocat { //frame 574
    name FURNITURE_NAME_OBJECT_FISHTANK_OCTOCAT
    desc FURNITURE_DESC_OBJECT_FISHTANK_OCTOCAT
    
    Appeal 3
    Stimulation 2
    Comfort -1
}
```

---

### `object_taxidermy_bear`
**Name:** Taxidermy Bear  
**Description:** FURNITURE_DESC_OBJECT_TAXIDERMY_BEAR  
**Source:** `furniture_effects.gon`  

```
object_taxidermy_bear { //frame 575
    name FURNITURE_NAME_OBJECT_TAXIDERMY_BEAR
    desc FURNITURE_DESC_OBJECT_TAXIDERMY_BEAR
    
    Appeal 1
    Health -2
	Evolution 2
}
```

---

### `object_bath1`
**Name:** Antique Bath  
**Description:** FURNITURE_DESC_OBJECT_BATH1  
**Source:** `furniture_effects.gon`  

```
object_bath1 { //frame 576
    name FURNITURE_NAME_OBJECT_BATH1
    desc FURNITURE_DESC_OBJECT_BATH1
    
    Comfort 2
}
```

---

### `object_bath2`
**Name:** Retro Bath  
**Description:** FURNITURE_DESC_OBJECT_BATH2  
**Source:** `furniture_effects.gon`  

```
object_bath2 { //frame 577
    name FURNITURE_NAME_OBJECT_BATH2
    desc FURNITURE_DESC_OBJECT_BATH2
    
    Comfort 2
}
```

---

### `object_shower`
**Name:** Shower  
**Description:** FURNITURE_DESC_OBJECT_SHOWER  
**Source:** `furniture_effects.gon`  

```
object_shower { //frame 578
    name FURNITURE_NAME_OBJECT_SHOWER
    desc FURNITURE_DESC_OBJECT_SHOWER
    
    Comfort 2
}
```

---

### `object_bbq`
**Name:** BBQ  
**Description:** FURNITURE_DESC_OBJECT_BBQ  
**Source:** `furniture_effects.gon`  

```
object_bbq { //frame 579
    name FURNITURE_NAME_OBJECT_BBQ
    desc FURNITURE_DESC_OBJECT_BBQ
    
    Comfort 2
}
```

---

### `object_oldstove`
**Name:** Antique Stove  
**Description:** FURNITURE_DESC_OBJECT_OLDSTOVE  
**Source:** `furniture_effects.gon`  

```
object_oldstove { //frame 580
    name FURNITURE_NAME_OBJECT_OLDSTOVE
    desc FURNITURE_DESC_OBJECT_OLDSTOVE
    
    Comfort 2
}
```

---

### `object_easel`
**Name:** Easel  
**Description:** FURNITURE_DESC_OBJECT_EASEL  
**Source:** `furniture_effects.gon`  

```
object_easel { //frame 581
    name FURNITURE_NAME_OBJECT_EASEL
    desc FURNITURE_DESC_OBJECT_EASEL
    
    Comfort 1
}
```

---

### `object_birdcage`
**Name:** Birdcage  
**Description:** FURNITURE_DESC_OBJECT_BIRDCAGE  
**Source:** `furniture_effects.gon`  

```
object_birdcage { //frame 582
    name FURNITURE_NAME_OBJECT_BIRDCAGE
    desc FURNITURE_DESC_OBJECT_BIRDCAGE
    
    Stimulation 1
}
```

---

### `object_dollhouse`
**Name:** Dollhouse  
**Description:** FURNITURE_DESC_OBJECT_DOLLHOUSE  
**Source:** `furniture_effects.gon`  

```
object_dollhouse { //frame 583
    name FURNITURE_NAME_OBJECT_DOLLHOUSE
    desc FURNITURE_DESC_OBJECT_DOLLHOUSE
    
    Stimulation 1
}
```

---

### `object_safe`
**Name:** Safe  
**Description:** FURNITURE_DESC_OBJECT_SAFE  
**Source:** `furniture_effects.gon`  

```
object_safe { //frame 584
    name FURNITURE_NAME_OBJECT_SAFE
    desc FURNITURE_DESC_OBJECT_SAFE
    
    Appeal 1
}
```

---

### `object_bed`
**Name:** Mattress  
**Description:** FURNITURE_DESC_OBJECT_BED  
**Source:** `furniture_effects.gon`  

```
object_bed { //frame 585
    name FURNITURE_NAME_OBJECT_BED
    desc FURNITURE_DESC_OBJECT_BED
    
    Comfort 1
}
```

---

### `object_watertower`
**Name:** Water Cooler  
**Description:** FURNITURE_DESC_OBJECT_WATERTOWER  
**Source:** `furniture_effects.gon`  

```
object_watertower { //frame 586
    name FURNITURE_NAME_OBJECT_WATERTOWER
    desc FURNITURE_DESC_OBJECT_WATERTOWER
    
    Comfort 1
}
```

---

### `object_visibleman`
**Name:** Visible Man  
**Description:** FURNITURE_DESC_OBJECT_VISIBLEMAN  
**Source:** `furniture_effects.gon`  

```
object_visibleman { //frame 587
    name FURNITURE_NAME_OBJECT_VISIBLEMAN
    desc FURNITURE_DESC_OBJECT_VISIBLEMAN
    
    Stimulation 1
}
```

---

### `object_statue_stonehead`
**Name:** Olmec Head  
**Description:** FURNITURE_DESC_OBJECT_STATUE_STONEHEAD  
**Source:** `furniture_effects.gon`  

```
object_statue_stonehead { //frame 588
    name FURNITURE_NAME_OBJECT_STATUE_STONEHEAD
    desc FURNITURE_DESC_OBJECT_STATUE_STONEHEAD
    
    Appeal 2
}
```

---

### `object_clock`
**Name:** Grandfather Clock  
**Description:** FURNITURE_DESC_OBJECT_CLOCK  
**Source:** `furniture_effects.gon`  

```
object_clock { //frame 589
    name FURNITURE_NAME_OBJECT_CLOCK
    desc FURNITURE_DESC_OBJECT_CLOCK
    
    Comfort 1
}
```

---

### `object_iv`
**Name:** IV  
**Description:** FURNITURE_DESC_OBJECT_IV  
**Source:** `furniture_effects.gon`  

```
object_iv { //frame 590
    name FURNITURE_NAME_OBJECT_IV
    desc FURNITURE_DESC_OBJECT_IV
    
	Health 1
}
```

---

### `object_fireplace`
**Name:** Fireplace  
**Description:** FURNITURE_DESC_OBJECT_FIREPLACE  
**Source:** `furniture_effects.gon`  

```
object_fireplace { //frame 591
    name FURNITURE_NAME_OBJECT_FIREPLACE
    desc FURNITURE_DESC_OBJECT_FIREPLACE
    
    Comfort 2
}
```

---

### `object_dryer`
**Name:** Dryer  
**Description:** FURNITURE_DESC_OBJECT_DRYER  
**Source:** `furniture_effects.gon`  

```
object_dryer { //frame 592
    name FURNITURE_NAME_OBJECT_DRYER
    desc FURNITURE_DESC_OBJECT_DRYER
    
    Comfort 2
}
```

---

### `object_washer`
**Name:** Washer  
**Description:** FURNITURE_DESC_OBJECT_WASHER  
**Source:** `furniture_effects.gon`  

```
object_washer { //frame 593
    name FURNITURE_NAME_OBJECT_WASHER
    desc FURNITURE_DESC_OBJECT_WASHER
    
    Comfort 2
}
```

---

### `object_filingcabinet`
**Name:** Filing Cabinet  
**Description:** FURNITURE_DESC_OBJECT_FILINGCABINET  
**Source:** `furniture_effects.gon`  

```
object_filingcabinet { //frame 594
    name FURNITURE_NAME_OBJECT_FILINGCABINET
    desc FURNITURE_DESC_OBJECT_FILINGCABINET
    
    Comfort 1
    Stimulation 1
}
```

---

### `object_cattree1`
**Name:** Cat Tree A  
**Description:** FURNITURE_DESC_OBJECT_CATTREE1  
**Source:** `furniture_effects.gon`  

```
object_cattree1 { //frame 595
    name FURNITURE_NAME_OBJECT_CATTREE1
    desc FURNITURE_DESC_OBJECT_CATTREE1
    
    Stimulation 1
}
```

---

### `object_cattree2`
**Name:** Cat Tree B  
**Description:** FURNITURE_DESC_OBJECT_CATTREE2  
**Source:** `furniture_effects.gon`  

```
object_cattree2 { //frame 596
    name FURNITURE_NAME_OBJECT_CATTREE2
    desc FURNITURE_DESC_OBJECT_CATTREE2
    
    Stimulation 1
}
```

---

### `object_cattree3`
**Name:** Cat Tree C  
**Description:** FURNITURE_DESC_OBJECT_CATTREE3  
**Source:** `furniture_effects.gon`  

```
object_cattree3 { //frame 597
    name FURNITURE_NAME_OBJECT_CATTREE3
    desc FURNITURE_DESC_OBJECT_CATTREE3
    
    Stimulation 1
}
```

---

### `object_punchy`
**Name:** Boxing Bill  
**Description:** FURNITURE_DESC_OBJECT_PUNCHY  
**Source:** `furniture_effects.gon`  

```
object_punchy { //frame 598
    name FURNITURE_NAME_OBJECT_PUNCHY
    desc FURNITURE_DESC_OBJECT_PUNCHY
    
    Stimulation 1
}
```

---

### `object_sink`
**Name:** Sink  
**Description:** FURNITURE_DESC_OBJECT_SINK  
**Source:** `furniture_effects.gon`  

```
object_sink { //frame 599
    name FURNITURE_NAME_OBJECT_SINK
    desc FURNITURE_DESC_OBJECT_SINK
    
    Comfort 1
}
```

---

### `object_toolchest`
**Name:** Tool Chest  
**Description:** FURNITURE_DESC_OBJECT_TOOLCHEST  
**Source:** `furniture_effects.gon`  

```
object_toolchest { //frame 600
    name FURNITURE_NAME_OBJECT_TOOLCHEST
    desc FURNITURE_DESC_OBJECT_TOOLCHEST
    
    Stimulation 1
}
```

---

### `object_ironingboard`
**Name:** Ironing Board  
**Description:** FURNITURE_DESC_OBJECT_IRONINGBOARD  
**Source:** `furniture_effects.gon`  

```
object_ironingboard { //frame 601
    name FURNITURE_NAME_OBJECT_IRONINGBOARD
    desc FURNITURE_DESC_OBJECT_IRONINGBOARD
    
    Comfort 1
}
```

---

### `object_broom`
**Name:** Broom  
**Description:** FURNITURE_DESC_OBJECT_BROOM  
**Source:** `furniture_effects.gon`  

```
object_broom { //frame 602
    name FURNITURE_NAME_OBJECT_BROOM
    desc FURNITURE_DESC_OBJECT_BROOM
    
    Comfort 1
}
```

---

### `object_vacuum`
**Name:** Vacuum  
**Description:** FURNITURE_DESC_OBJECT_VACUUM  
**Source:** `furniture_effects.gon`  

```
object_vacuum { //frame 603
    name FURNITURE_NAME_OBJECT_VACUUM
    desc FURNITURE_DESC_OBJECT_VACUUM
    
    Comfort 1
}
```

---

### `object_gnome`
**Name:** Gnome  
**Description:** FURNITURE_DESC_OBJECT_GNOME  
**Source:** `furniture_effects.gon`  

```
object_gnome { //frame 604
    name FURNITURE_NAME_OBJECT_GNOME
    desc FURNITURE_DESC_OBJECT_GNOME
    
    Comfort 1
    Appeal 1
}
```

---

### `wallmounted_picture_blueboy`
**Name:** Framed Blue Boy  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_BLUEBOY  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_blueboy { //frame 650
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_BLUEBOY
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_BLUEBOY
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_frida`
**Name:** Framed Frida  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_FRIDA  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_frida { //frame 651
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_FRIDA
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_FRIDA
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_god`
**Name:** Framed Creation of Adam  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_GOD  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_god { //frame 652
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_GOD
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_GOD
    
    Appeal 2
    Comfort 1
	Health 1
}
```

---

### `wallmounted_picture_lisa`
**Name:** Framed Mona Lisa  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_LISA  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_lisa { //frame 653
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_LISA
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_LISA
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_scream`
**Name:** Framed The Scream  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_SCREAM  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_scream { //frame 654
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_SCREAM
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_SCREAM
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_night`
**Name:** Framed Starry Night  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_NIGHT  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_night { //frame 655
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_NIGHT
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_NIGHT
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_gothic`
**Name:** Framed American Gothic  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_GOTHIC  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_gothic { //frame 656
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_GOTHIC
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_GOTHIC
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_picasso`
**Name:** Framed Picasso  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_PICASSO  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_picasso { //frame 657
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_PICASSO
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_PICASSO
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_keith`
**Name:** Framed Keith Haring  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_KEITH  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_keith { //frame 658
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_KEITH
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_KEITH
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_pearl`
**Name:** Framed The Pearl  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_PEARL  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_pearl { //frame 659
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_PEARL
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_PEARL
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_rosie`
**Name:** Rosie Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_ROSIE  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_rosie { //frame 660
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_ROSIE
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_ROSIE
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_ufo`
**Name:** UFO Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_UFO  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_ufo { //frame 661
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_UFO
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_UFO
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_che`
**Name:** Che Purvara Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_CHE  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_che { //frame 662
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_CHE
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_CHE
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_obey`
**Name:** Meowbey Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_OBEY  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_obey { //frame 663
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_OBEY
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_OBEY
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_hang`
**Name:** Hang in There Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_HANG  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_hang { //frame 664
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_HANG
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_HANG
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_jaws`
**Name:** Paws Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_JAWS  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_jaws { //frame 665
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_JAWS
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_JAWS
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_scarface`
**Name:** Catface Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_SCARFACE  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_scarface { //frame 666
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_SCARFACE
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_SCARFACE
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_lambs`
**Name:** Silence of the Mice Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_LAMBS  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_lambs { //frame 667
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_LAMBS
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_LAMBS
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_orange`
**Name:** Catwork Orange Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_ORANGE  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_orange { //frame 668
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_ORANGE
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_ORANGE
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_picture_eraser`
**Name:** Litterhead Poster  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_ERASER  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_eraser { //frame 669
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_ERASER
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_ERASER
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_sewn_clock`
**Name:** Sewn Clock  
**Description:** FURNITURE_DESC_WALLMOUNTED_SEWN_CLOCK  
**Source:** `furniture_effects.gon`  

```
wallmounted_sewn_clock { //frame 670
    name FURNITURE_NAME_WALLMOUNTED_SEWN_CLOCK
    desc FURNITURE_DESC_WALLMOUNTED_SEWN_CLOCK
    
    Appeal 1
    Comfort 1
}
```

---

### `wallmounted_clock`
**Name:** Cat Clock  
**Description:** FURNITURE_DESC_WALLMOUNTED_CLOCK  
**Source:** `furniture_effects.gon`  

```
wallmounted_clock { //frame 671
    name FURNITURE_NAME_WALLMOUNTED_CLOCK
    desc FURNITURE_DESC_WALLMOUNTED_CLOCK
    
    Appeal 1
}
```

---

### `wallmounted_wooden_clock`
**Name:** Wooden Clock  
**Description:** FURNITURE_DESC_WALLMOUNTED_WOODEN_CLOCK  
**Source:** `furniture_effects.gon`  

```
wallmounted_wooden_clock { //frame 672
    name FURNITURE_NAME_WALLMOUNTED_WOODEN_CLOCK
    desc FURNITURE_DESC_WALLMOUNTED_WOODEN_CLOCK
    
    Appeal 1
}
```

---

### `wallmounted_atomic_clock`
**Name:** Atomic Clock  
**Description:** FURNITURE_DESC_WALLMOUNTED_ATOMIC_CLOCK  
**Source:** `furniture_effects.gon`  

```
wallmounted_atomic_clock { //frame 673
    name FURNITURE_NAME_WALLMOUNTED_ATOMIC_CLOCK
    desc FURNITURE_DESC_WALLMOUNTED_ATOMIC_CLOCK
    
    Appeal 1
}
```

---

### `wallmounted_ghost1`
**Name:** Blinky  
**Description:** FURNITURE_DESC_WALLMOUNTED_GHOST1  
**Source:** `furniture_effects.gon`  

```
wallmounted_ghost1 { //frame 674
    name FURNITURE_NAME_WALLMOUNTED_GHOST1
    desc FURNITURE_DESC_WALLMOUNTED_GHOST1
    
    Appeal 1
    Stimulation 1
    Comfort -1
}
```

---

### `wallmounted_ghost2`
**Name:** Pinky  
**Description:** FURNITURE_DESC_WALLMOUNTED_GHOST2  
**Source:** `furniture_effects.gon`  

```
wallmounted_ghost2 { //frame 675
    name FURNITURE_NAME_WALLMOUNTED_GHOST2
    desc FURNITURE_DESC_WALLMOUNTED_GHOST2
    
    Appeal 1
    Stimulation 1
    Comfort -1
}
```

---

### `wallmounted_ghost3`
**Name:** Clyde  
**Description:** FURNITURE_DESC_WALLMOUNTED_GHOST3  
**Source:** `furniture_effects.gon`  

```
wallmounted_ghost3 { //frame 676
    name FURNITURE_NAME_WALLMOUNTED_GHOST3
    desc FURNITURE_DESC_WALLMOUNTED_GHOST3
    
    Appeal 1
    Stimulation 1
    Comfort -1
}
```

---

### `wallmounted_mask_bunny`
**Name:** Bunny Mask  
**Description:** FURNITURE_DESC_WALLMOUNTED_MASK_BUNNY  
**Source:** `furniture_effects.gon`  

```
wallmounted_mask_bunny { //frame 677
    name FURNITURE_NAME_WALLMOUNTED_MASK_BUNNY
    desc FURNITURE_DESC_WALLMOUNTED_MASK_BUNNY
    
    Appeal 1
}
```

---

### `wallmounted_mask_tonetta`
**Name:** Tonetta Mask  
**Description:** FURNITURE_DESC_WALLMOUNTED_MASK_TONETTA  
**Source:** `furniture_effects.gon`  

```
wallmounted_mask_tonetta { //frame 678
    name FURNITURE_NAME_WALLMOUNTED_MASK_TONETTA
    desc FURNITURE_DESC_WALLMOUNTED_MASK_TONETTA
    
    Appeal 1
}
```

---

### `wallmounted_mask_hocky`
**Name:** Hockey Mask  
**Description:** FURNITURE_DESC_WALLMOUNTED_MASK_HOCKY  
**Source:** `furniture_effects.gon`  

```
wallmounted_mask_hocky { //frame 679
    name FURNITURE_NAME_WALLMOUNTED_MASK_HOCKY
    desc FURNITURE_DESC_WALLMOUNTED_MASK_HOCKY
    
    Appeal 1
}
```

---

### `wallmounted_picture_sailboat`
**Name:** Framed Sailboat  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_SAILBOAT  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_sailboat { //frame 680
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_SAILBOAT
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_SAILBOAT
    
    Appeal 1
}
```

---

### `wallmounted_picture_magazine`
**Name:** Centerfold  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_MAGAZINE  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_magazine { //frame 681
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_MAGAZINE
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_MAGAZINE
    
    Comfort 1
}
```

---

### `wallmounted_picture_poem`
**Name:** Poem  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_POEM  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_poem { //frame 682
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_POEM
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_POEM
    
    Comfort 1
}
```

---

### `wallmounted_picture_photo`
**Name:** Photo A  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_PHOTO  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_photo { //frame 683
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_PHOTO
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_PHOTO
    
    Comfort 1
}
```

---

### `wallmounted_picture_photo2`
**Name:** Photo B  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_PHOTO2  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_photo2 { //frame 684
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_PHOTO2
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_PHOTO2
    
    Comfort 1
}
```

---

### `wallmounted_picture_photo3`
**Name:** Photos  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_PHOTO3  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_photo3 { //frame 685
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_PHOTO3
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_PHOTO3
    
    Comfort 1
}
```

---

### `wallmounted_wooden_boards1`
**Name:** Wooden Boards A  
**Description:** FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS1  
**Source:** `furniture_effects.gon`  

```
wallmounted_wooden_boards1 { //frame 686
    name FURNITURE_NAME_WALLMOUNTED_WOODEN_BOARDS1
    desc FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS1
    
    Comfort 1
}
```

---

### `wallmounted_wooden_boards2`
**Name:** Wooden Boards B  
**Description:** FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS2  
**Source:** `furniture_effects.gon`  

```
wallmounted_wooden_boards2 { //frame 687
    name FURNITURE_NAME_WALLMOUNTED_WOODEN_BOARDS2
    desc FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS2
    
    Comfort 1
}
```

---

### `wallmounted_wooden_boards3`
**Name:** Wooden Boards C  
**Description:** FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS3  
**Source:** `furniture_effects.gon`  

```
wallmounted_wooden_boards3 { //frame 688
    name FURNITURE_NAME_WALLMOUNTED_WOODEN_BOARDS3
    desc FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS3
    
    Comfort 1
}
```

---

### `wallmounted_wooden_boards4`
**Name:** Wooden Boards D  
**Description:** FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS4  
**Source:** `furniture_effects.gon`  

```
wallmounted_wooden_boards4 { //frame 689
    name FURNITURE_NAME_WALLMOUNTED_WOODEN_BOARDS4
    desc FURNITURE_DESC_WALLMOUNTED_WOODEN_BOARDS4
    
    Comfort 1
}
```

---

### `wallmounted_switch`
**Name:** Light Switch  
**Description:** FURNITURE_DESC_WALLMOUNTED_SWITCH  
**Source:** `furniture_effects.gon`  

```
wallmounted_switch { //frame 690
    name FURNITURE_NAME_WALLMOUNTED_SWITCH
    desc FURNITURE_DESC_WALLMOUNTED_SWITCH
    
    Comfort 1
}
```

---

### `wallmounted_outlet`
**Name:** Outlet  
**Description:** FURNITURE_DESC_WALLMOUNTED_OUTLET  
**Source:** `furniture_effects.gon`  

```
wallmounted_outlet { //frame 691
    name FURNITURE_NAME_WALLMOUNTED_OUTLET
    desc FURNITURE_DESC_WALLMOUNTED_OUTLET
    
    Comfort 1
}
```

---

### `wallmounted_robo_plate1`
**Name:** Metal Plate A  
**Description:** FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE1  
**Source:** `furniture_effects.gon`  

```
wallmounted_robo_plate1 { //frame 692
    name FURNITURE_NAME_WALLMOUNTED_ROBO_PLATE1
    desc FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE1
    
    Stimulation 1
}
```

---

### `wallmounted_robo_plate2`
**Name:** Metal Plate B  
**Description:** FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE2  
**Source:** `furniture_effects.gon`  

```
wallmounted_robo_plate2 { //frame 693
    name FURNITURE_NAME_WALLMOUNTED_ROBO_PLATE2
    desc FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE2
    
    Stimulation 1
}
```

---

### `wallmounted_robo_plate3`
**Name:** Metal Plate C  
**Description:** FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE3  
**Source:** `furniture_effects.gon`  

```
wallmounted_robo_plate3 { //frame 694
    name FURNITURE_NAME_WALLMOUNTED_ROBO_PLATE3
    desc FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE3
    
    Stimulation 1
}
```

---

### `wallmounted_furnace`
**Name:** Furnace  
**Description:** FURNITURE_DESC_WALLMOUNTED_FURNACE  
**Source:** `furniture_effects.gon`  

```
wallmounted_furnace { //frame 695
    name FURNITURE_NAME_WALLMOUNTED_FURNACE
    desc FURNITURE_DESC_WALLMOUNTED_FURNACE
    
    Comfort 1
}
```

---

### `wallmounted_robo_plate4`
**Name:** Robo Plate  
**Description:** FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE4  
**Source:** `furniture_effects.gon`  

```
wallmounted_robo_plate4 { //frame 696
    name FURNITURE_NAME_WALLMOUNTED_ROBO_PLATE4
    desc FURNITURE_DESC_WALLMOUNTED_ROBO_PLATE4
    
    Stimulation 1
}
```

---

### `wallmounted_tv`
**Name:** Wall-Mounted TV  
**Description:** FURNITURE_DESC_WALLMOUNTED_TV  
**Source:** `furniture_effects.gon`  

```
wallmounted_tv { //frame 697
    name FURNITURE_NAME_WALLMOUNTED_TV
    desc FURNITURE_DESC_WALLMOUNTED_TV
    
    Stimulation 1
}
```

---

### `wallmounted_balloon`
**Name:** Balloon A  
**Description:** FURNITURE_DESC_WALLMOUNTED_BALLOON  
**Source:** `furniture_effects.gon`  

```
wallmounted_balloon { //frame 698
    name FURNITURE_NAME_WALLMOUNTED_BALLOON
    desc FURNITURE_DESC_WALLMOUNTED_BALLOON
    
    Comfort 1
}
```

---

### `wallmounted_balloon2`
**Name:** Balloon B  
**Description:** FURNITURE_DESC_WALLMOUNTED_BALLOON2  
**Source:** `furniture_effects.gon`  

```
wallmounted_balloon2 { //frame 699
    name FURNITURE_NAME_WALLMOUNTED_BALLOON2
    desc FURNITURE_DESC_WALLMOUNTED_BALLOON2
    
    Comfort 1
}
```

---

### `wallmounted_balloon3`
**Name:** Balloon C  
**Description:** FURNITURE_DESC_WALLMOUNTED_BALLOON3  
**Source:** `furniture_effects.gon`  

```
wallmounted_balloon3 { //frame 700
    name FURNITURE_NAME_WALLMOUNTED_BALLOON3
    desc FURNITURE_DESC_WALLMOUNTED_BALLOON3
    
    Comfort 1
}
```

---

### `wallmounted_sewer_pipes1`
**Name:** Sewer Pipes A  
**Description:** FURNITURE_DESC_WALLMOUNTED_SEWER_PIPES1  
**Source:** `furniture_effects.gon`  

```
wallmounted_sewer_pipes1 { //frame 701
    name FURNITURE_NAME_WALLMOUNTED_SEWER_PIPES1
    desc FURNITURE_DESC_WALLMOUNTED_SEWER_PIPES1
    
    Comfort 1
}
```

---

### `wallmounted_sewer_pipes2`
**Name:** Sewer Pipes B  
**Description:** FURNITURE_DESC_WALLMOUNTED_SEWER_PIPES2  
**Source:** `furniture_effects.gon`  

```
wallmounted_sewer_pipes2 { //frame 702
    name FURNITURE_NAME_WALLMOUNTED_SEWER_PIPES2
    desc FURNITURE_DESC_WALLMOUNTED_SEWER_PIPES2
    
    Comfort 1
}
```

---

### `wallmounted_sewer_pipes3`
**Name:** Sewer Pipes C  
**Description:** FURNITURE_DESC_WALLMOUNTED_SEWER_PIPES3  
**Source:** `furniture_effects.gon`  

```
wallmounted_sewer_pipes3 { //frame 703
    name FURNITURE_NAME_WALLMOUNTED_SEWER_PIPES3
    desc FURNITURE_DESC_WALLMOUNTED_SEWER_PIPES3
    
    Comfort 1
}
```

---

### `wallmounted_balloon4`
**Name:** Heart Balloon  
**Description:** FURNITURE_DESC_WALLMOUNTED_BALLOON4  
**Source:** `furniture_effects.gon`  

```
wallmounted_balloon4 { //frame 704
    name FURNITURE_NAME_WALLMOUNTED_BALLOON4
    desc FURNITURE_DESC_WALLMOUNTED_BALLOON4
    
    Comfort 1
}
```

---

### `wallmounted_mirror`
**Name:** Mirror  
**Description:** FURNITURE_DESC_WALLMOUNTED_MIRROR  
**Source:** `furniture_effects.gon`  

```
wallmounted_mirror { //frame 705
    name FURNITURE_NAME_WALLMOUNTED_MIRROR
    desc FURNITURE_DESC_WALLMOUNTED_MIRROR
    
    Comfort 1
}
```

---

### `wallmounted_junk_paper1`
**Name:** Newspapers A  
**Description:** FURNITURE_DESC_WALLMOUNTED_JUNK_PAPER1  
**Source:** `furniture_effects.gon`  

```
wallmounted_junk_paper1 { //frame 706
    name FURNITURE_NAME_WALLMOUNTED_JUNK_PAPER1
    desc FURNITURE_DESC_WALLMOUNTED_JUNK_PAPER1
    
    Appeal 1
}
```

---

### `wallmounted_picture_drawing`
**Name:** Drawing  
**Description:** FURNITURE_DESC_WALLMOUNTED_PICTURE_DRAWING  
**Source:** `furniture_effects.gon`  

```
wallmounted_picture_drawing { //frame 707
    name FURNITURE_NAME_WALLMOUNTED_PICTURE_DRAWING
    desc FURNITURE_DESC_WALLMOUNTED_PICTURE_DRAWING
    
    Appeal 1
}
```

---

### `wallmounted_cowskull`
**Name:** Wallmounted Cow Skull  
**Description:** FURNITURE_DESC_WALLMOUNTED_COWSKULL  
**Source:** `furniture_effects.gon`  

```
wallmounted_cowskull { //frame 708
    name FURNITURE_NAME_WALLMOUNTED_COWSKULL
    desc FURNITURE_DESC_WALLMOUNTED_COWSKULL
    
    Appeal 1
}
```

---

### `wallmounted_taxidermy_deerhead`
**Name:** Taxidermy Deer  
**Description:** FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_DEERHEAD  
**Source:** `furniture_effects.gon`  

```
wallmounted_taxidermy_deerhead { //frame 709
    name FURNITURE_NAME_WALLMOUNTED_TAXIDERMY_DEERHEAD
    desc FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_DEERHEAD
    
    Appeal -1
    Health -1
	Evolution 1
}
```

---

### `wallmounted_taxidermy_guppy`
**Name:** Taxidermy Guppy  
**Description:** FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_GUPPY  
**Source:** `furniture_effects.gon`  

```
wallmounted_taxidermy_guppy { //frame 710
    name FURNITURE_NAME_WALLMOUNTED_TAXIDERMY_GUPPY
    desc FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_GUPPY
    
    Appeal 1
	Evolution 1
}
```

---

### `wallmounted_jollyroger`
**Name:** Jolly Roger  
**Description:** FURNITURE_DESC_WALLMOUNTED_JOLLYROGER  
**Source:** `furniture_effects.gon`  

```
wallmounted_jollyroger { //frame 711
    name FURNITURE_NAME_WALLMOUNTED_JOLLYROGER
    desc FURNITURE_DESC_WALLMOUNTED_JOLLYROGER
    
    Appeal 1
}
```

---

### `wallmounted_taxidermy_bugs`
**Name:** Taxidermy Bugs  
**Description:** FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_BUGS  
**Source:** `furniture_effects.gon`  

```
wallmounted_taxidermy_bugs { //frame 712
    name FURNITURE_NAME_WALLMOUNTED_TAXIDERMY_BUGS
    desc FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_BUGS
    
    Appeal 1
}
```

---

### `wallmounted_taxidermy_fish`
**Name:** Taxidermy Bass  
**Description:** FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_FISH  
**Source:** `furniture_effects.gon`  

```
wallmounted_taxidermy_fish { //frame 713
    name FURNITURE_NAME_WALLMOUNTED_TAXIDERMY_FISH
    desc FURNITURE_DESC_WALLMOUNTED_TAXIDERMY_FISH
    
    Appeal 1
}
```

---

### `wallmounted_mask_infamy`
**Name:** Infamous Mask  
**Description:** FURNITURE_DESC_WALLMOUNTED_MASK_INFAMY  
**Source:** `furniture_effects.gon`  

```
wallmounted_mask_infamy { //frame 714
    name FURNITURE_NAME_WALLMOUNTED_MASK_INFAMY
    desc FURNITURE_DESC_WALLMOUNTED_MASK_INFAMY
    
    Appeal 1
}
```

---

### `wallmounted_safe`
**Name:** Wall Safe  
**Description:** FURNITURE_DESC_WALLMOUNTED_SAFE  
**Source:** `furniture_effects.gon`  

```
wallmounted_safe { //frame 715
    name FURNITURE_NAME_WALLMOUNTED_SAFE
    desc FURNITURE_DESC_WALLMOUNTED_SAFE
    
    Appeal 1
}
```

---

### `wallmounted_bricks1`
**Name:** Bricks A  
**Description:** FURNITURE_DESC_WALLMOUNTED_BRICKS1  
**Source:** `furniture_effects.gon`  

```
wallmounted_bricks1 { //frame 716
    name FURNITURE_NAME_WALLMOUNTED_BRICKS1
    desc FURNITURE_DESC_WALLMOUNTED_BRICKS1
    
    Comfort 1
}
```

---

### `wallmounted_bricks2`
**Name:** Bricks B  
**Description:** FURNITURE_DESC_WALLMOUNTED_BRICKS2  
**Source:** `furniture_effects.gon`  

```
wallmounted_bricks2 { //frame 717
    name FURNITURE_NAME_WALLMOUNTED_BRICKS2
    desc FURNITURE_DESC_WALLMOUNTED_BRICKS2
    
    Comfort 1
}
```

---

### `wallmounted_bricks3`
**Name:** Bricks C  
**Description:** FURNITURE_DESC_WALLMOUNTED_BRICKS3  
**Source:** `furniture_effects.gon`  

```
wallmounted_bricks3 { //frame 718
    name FURNITURE_NAME_WALLMOUNTED_BRICKS3
    desc FURNITURE_DESC_WALLMOUNTED_BRICKS3
    
    Comfort 1
}
```

---

### `wallmounted_bricks4`
**Name:** Bricks D  
**Description:** FURNITURE_DESC_WALLMOUNTED_BRICKS4  
**Source:** `furniture_effects.gon`  

```
wallmounted_bricks4 { //frame 719
    name FURNITURE_NAME_WALLMOUNTED_BRICKS4
    desc FURNITURE_DESC_WALLMOUNTED_BRICKS4
    
    Comfort 1
}
```

---

### `wallmounted_junk_paper2`
**Name:** Newspapers B  
**Description:** FURNITURE_DESC_WALLMOUNTED_JUNK_PAPER2  
**Source:** `furniture_effects.gon`  

```
wallmounted_junk_paper2 { //frame 720
    name FURNITURE_NAME_WALLMOUNTED_JUNK_PAPER2
    desc FURNITURE_DESC_WALLMOUNTED_JUNK_PAPER2
    
    Comfort 1
}
```

---

### `wallmounted_crack`
**Name:** A Crack  
**Description:** FURNITURE_DESC_WALLMOUNTED_CRACK  
**Source:** `furniture_effects.gon`  

```
wallmounted_crack { //frame 721
    name FURNITURE_NAME_WALLMOUNTED_CRACK
    desc FURNITURE_DESC_WALLMOUNTED_CRACK
    
    Comfort 1
}
```

---

### `wallmounted_torch`
**Name:** Torch  
**Description:** FURNITURE_DESC_WALLMOUNTED_TORCH  
**Source:** `furniture_effects.gon`  

```
wallmounted_torch { //frame 722
    name FURNITURE_NAME_WALLMOUNTED_TORCH
    desc FURNITURE_DESC_WALLMOUNTED_TORCH
    
    Comfort 1
}
```

---

### `wallmounted_shrunkinhead`
**Name:** Shrunken Cat Head  
**Description:** FURNITURE_DESC_WALLMOUNTED_SHRUNKINHEAD  
**Source:** `furniture_effects.gon`  

```
wallmounted_shrunkinhead { //frame 723
    name FURNITURE_NAME_WALLMOUNTED_SHRUNKINHEAD
    desc FURNITURE_DESC_WALLMOUNTED_SHRUNKINHEAD
    
    Health -5
	Evolution 1
}
```

---

### `wallmounted_cloud`
**Name:** Cloud  
**Description:** FURNITURE_DESC_WALLMOUNTED_CLOUD  
**Source:** `furniture_effects.gon`  

```
wallmounted_cloud { //frame 724
    name FURNITURE_NAME_WALLMOUNTED_CLOUD
    desc FURNITURE_DESC_WALLMOUNTED_CLOUD
    
    Comfort 1
}
```

---

### `wallmounted_block1`
**Name:** Block  
**Description:** FURNITURE_DESC_WALLMOUNTED_BLOCK1  
**Source:** `furniture_effects.gon`  

```
wallmounted_block1 { //frame 725
    name FURNITURE_NAME_WALLMOUNTED_BLOCK1
    desc FURNITURE_DESC_WALLMOUNTED_BLOCK1
    
    Comfort 1
}
```

---

### `wallmounted_block2`
**Name:** Question Block  
**Description:** FURNITURE_DESC_WALLMOUNTED_BLOCK2  
**Source:** `furniture_effects.gon`  

```
wallmounted_block2 { //frame 726
    name FURNITURE_NAME_WALLMOUNTED_BLOCK2
    desc FURNITURE_DESC_WALLMOUNTED_BLOCK2
    
    Comfort 1
}
```

---

### `wallmounted_block3`
**Name:** Brick Block  
**Description:** FURNITURE_DESC_WALLMOUNTED_BLOCK3  
**Source:** `furniture_effects.gon`  

```
wallmounted_block3 { //frame 727
    name FURNITURE_NAME_WALLMOUNTED_BLOCK3
    desc FURNITURE_DESC_WALLMOUNTED_BLOCK3
    
    Comfort 1
}
```

---

### `wallmounted_balloon5`
**Name:** Balloon D  
**Description:** FURNITURE_DESC_WALLMOUNTED_BALLOON5  
**Source:** `furniture_effects.gon`  

```
wallmounted_balloon5 { //frame 728
    name FURNITURE_NAME_WALLMOUNTED_BALLOON5
    desc FURNITURE_DESC_WALLMOUNTED_BALLOON5
    
    Comfort 1
}
```

---

### `wallmounted_balloon6`
**Name:** Balloon E  
**Description:** FURNITURE_DESC_WALLMOUNTED_BALLOON6  
**Source:** `furniture_effects.gon`  

```
wallmounted_balloon6 { //frame 729
    name FURNITURE_NAME_WALLMOUNTED_BALLOON6
    desc FURNITURE_DESC_WALLMOUNTED_BALLOON6
    
    Comfort 1
}
```

---

### `wallmounted_balloon7`
**Name:** Balloon F  
**Description:** FURNITURE_DESC_WALLMOUNTED_BALLOON7  
**Source:** `furniture_effects.gon`  

```
wallmounted_balloon7 { //frame 730
    name FURNITURE_NAME_WALLMOUNTED_BALLOON7
    desc FURNITURE_DESC_WALLMOUNTED_BALLOON7
    
    Comfort 1
}
```

---

### `hanging_fish`
**Name:** Hanging Air Fouler  
**Description:** FURNITURE_DESC_HANGING_FISH  
**Source:** `furniture_effects.gon`  

```
hanging_fish { //frame 800
    name FURNITURE_NAME_HANGING_FISH
    desc FURNITURE_DESC_HANGING_FISH
    
    Comfort 1
}
```

---

### `hanging_cathead`
**Name:** Hanging Airfreshener A  
**Description:** FURNITURE_DESC_HANGING_CATHEAD  
**Source:** `furniture_effects.gon`  

```
hanging_cathead { //frame 801
    name FURNITURE_NAME_HANGING_CATHEAD
    desc FURNITURE_DESC_HANGING_CATHEAD
    
    Comfort 1
}
```

---

### `hanging_airfreshiner`
**Name:** Hanging Airfreshener B  
**Description:** FURNITURE_DESC_HANGING_AIRFRESHINER  
**Source:** `furniture_effects.gon`  

```
hanging_airfreshiner { //frame 802
    name FURNITURE_NAME_HANGING_AIRFRESHINER
    desc FURNITURE_DESC_HANGING_AIRFRESHINER
    
    Comfort 1
}
```

---

### `ceiling_fan`
**Name:** Ceiling Fan  
**Description:** FURNITURE_DESC_CEILING_FAN  
**Source:** `furniture_effects.gon`  

```
ceiling_fan { //frame 803
    name FURNITURE_NAME_CEILING_FAN
    desc FURNITURE_DESC_CEILING_FAN
    
    Comfort 1
}
```

---

### `ceiling_discoball`
**Name:** Disco Ball  
**Description:** FURNITURE_DESC_CEILING_DISCOBALL  
**Source:** `furniture_effects.gon`  

```
ceiling_discoball { //frame 804
    name FURNITURE_NAME_CEILING_DISCOBALL
    desc FURNITURE_DESC_CEILING_DISCOBALL
    
    Comfort 1
}
```

---

### `ceiling_cage`
**Name:** Hanging Cage  
**Description:** FURNITURE_DESC_CEILING_CAGE  
**Source:** `furniture_effects.gon`  

```
ceiling_cage { //frame 805
    name FURNITURE_NAME_CEILING_CAGE
    desc FURNITURE_DESC_CEILING_CAGE
    
    Stimulation 1
}
```

---

### `small_candle_black1`
**Name:** Red Candle A  
**Description:** FURNITURE_DESC_SMALL_CANDLE_BLACK1  
**Source:** `furniture_effects.gon`  

```
small_candle_black1 { //frame 950
    name FURNITURE_NAME_SMALL_CANDLE_BLACK1
    desc FURNITURE_DESC_SMALL_CANDLE_BLACK1
    
    Comfort 1
}
```

---

### `small_candle_black2`
**Name:** Red Candle B  
**Description:** FURNITURE_DESC_SMALL_CANDLE_BLACK2  
**Source:** `furniture_effects.gon`  

```
small_candle_black2 { //frame 951
    name FURNITURE_NAME_SMALL_CANDLE_BLACK2
    desc FURNITURE_DESC_SMALL_CANDLE_BLACK2
    
    Comfort 1
}
```

---

### `small_candle_black3`
**Name:** Small Red Candle A  
**Description:** FURNITURE_DESC_SMALL_CANDLE_BLACK3  
**Source:** `furniture_effects.gon`  

```
small_candle_black3 { //frame 952
    name FURNITURE_NAME_SMALL_CANDLE_BLACK3
    desc FURNITURE_DESC_SMALL_CANDLE_BLACK3
    
    Comfort 1
}
```

---

### `Small_candle_black4`
**Name:** Small Red Candle B  
**Description:** FURNITURE_DESC_SMALL_CANDLE_BLACK4  
**Source:** `furniture_effects.gon`  

```
Small_candle_black4 { //frame 953
    name FURNITURE_NAME_SMALL_CANDLE_BLACK4
    desc FURNITURE_DESC_SMALL_CANDLE_BLACK4
    
    Comfort 1
}
```

---

### `Small_candle_white1`
**Name:** Small White Candle A  
**Description:** FURNITURE_DESC_SMALL_CANDLE_WHITE1  
**Source:** `furniture_effects.gon`  

```
Small_candle_white1 { //frame 954
    name FURNITURE_NAME_SMALL_CANDLE_WHITE1
    desc FURNITURE_DESC_SMALL_CANDLE_WHITE1
    
    Comfort 1
}
```

---

### `Small_candle_white2`
**Name:** Small White Candle B  
**Description:** FURNITURE_DESC_SMALL_CANDLE_WHITE2  
**Source:** `furniture_effects.gon`  

```
Small_candle_white2 { //frame 955
    name FURNITURE_NAME_SMALL_CANDLE_WHITE2
    desc FURNITURE_DESC_SMALL_CANDLE_WHITE2
    
    Comfort 1
}
```

---

### `Small_candle_white3`
**Name:** White Candle A  
**Description:** FURNITURE_DESC_SMALL_CANDLE_WHITE3  
**Source:** `furniture_effects.gon`  

```
Small_candle_white3 { //frame 956
    name FURNITURE_NAME_SMALL_CANDLE_WHITE3
    desc FURNITURE_DESC_SMALL_CANDLE_WHITE3
    
    Comfort 1
}
```

---

### `Small_candle_white4`
**Name:** White Candle B  
**Description:** FURNITURE_DESC_SMALL_CANDLE_WHITE4  
**Source:** `furniture_effects.gon`  

```
Small_candle_white4 { //frame 957
    name FURNITURE_NAME_SMALL_CANDLE_WHITE4
    desc FURNITURE_DESC_SMALL_CANDLE_WHITE4
    
    Comfort 1
}
```

---

### `small_vase1`
**Name:** Small Vase A  
**Description:** FURNITURE_DESC_SMALL_VASE1  
**Source:** `furniture_effects.gon`  

```
small_vase1 { //frame 958
    name FURNITURE_NAME_SMALL_VASE1
    desc FURNITURE_DESC_SMALL_VASE1
    
    Comfort 1
}
```

---

### `small_vase2`
**Name:** Small Vase B  
**Description:** FURNITURE_DESC_SMALL_VASE2  
**Source:** `furniture_effects.gon`  

```
small_vase2 { //frame 959
    name FURNITURE_NAME_SMALL_VASE2
    desc FURNITURE_DESC_SMALL_VASE2
    
    Comfort 1
}
```

---

### `small_vase3`
**Name:** Small Vase C  
**Description:** FURNITURE_DESC_SMALL_VASE3  
**Source:** `furniture_effects.gon`  

```
small_vase3 { //frame 960
    name FURNITURE_NAME_SMALL_VASE3
    desc FURNITURE_DESC_SMALL_VASE3
    
    Comfort 1
}
```

---

### `small_trash_eggs`
**Name:** Egg Shells  
**Description:** FURNITURE_DESC_SMALL_TRASH_EGGS  
**Source:** `furniture_effects.gon`  

```
small_trash_eggs { //frame 961
    name FURNITURE_NAME_SMALL_TRASH_EGGS
    desc FURNITURE_DESC_SMALL_TRASH_EGGS
    
    Comfort 1
}
```

---

### `small_trash_apple`
**Name:** Apple Core  
**Description:** FURNITURE_DESC_SMALL_TRASH_APPLE  
**Source:** `furniture_effects.gon`  

```
small_trash_apple { //frame 962
    name FURNITURE_NAME_SMALL_TRASH_APPLE
    desc FURNITURE_DESC_SMALL_TRASH_APPLE
    
    Comfort 1
}
```

---

### `small_trash_bone`
**Name:** Bone  
**Description:** FURNITURE_DESC_SMALL_TRASH_BONE  
**Source:** `furniture_effects.gon`  

```
small_trash_bone { //frame 963
    name FURNITURE_NAME_SMALL_TRASH_BONE
    desc FURNITURE_DESC_SMALL_TRASH_BONE
    
    Comfort 1
}
```

---

### `small_trash_banana`
**Name:** Banana Peel  
**Description:** FURNITURE_DESC_SMALL_TRASH_BANANA  
**Source:** `furniture_effects.gon`  

```
small_trash_banana { //frame 964
    name FURNITURE_NAME_SMALL_TRASH_BANANA
    desc FURNITURE_DESC_SMALL_TRASH_BANANA
    
    Comfort 1
}
```

---

### `small_trash_cans`
**Name:** Soda Cans  
**Description:** FURNITURE_DESC_SMALL_TRASH_CANS  
**Source:** `furniture_effects.gon`  

```
small_trash_cans { //frame 965
    name FURNITURE_NAME_SMALL_TRASH_CANS
    desc FURNITURE_DESC_SMALL_TRASH_CANS
    
    Comfort 1
}
```

---

### `small_trash_bread`
**Name:** Old Toast  
**Description:** FURNITURE_DESC_SMALL_TRASH_BREAD  
**Source:** `furniture_effects.gon`  

```
small_trash_bread { //frame 966
    name FURNITURE_NAME_SMALL_TRASH_BREAD
    desc FURNITURE_DESC_SMALL_TRASH_BREAD
    
    Comfort -1
	Health 1
}
```

---

### `small_trash_cup`
**Name:** Soup Cup  
**Description:** FURNITURE_DESC_SMALL_TRASH_CUP  
**Source:** `furniture_effects.gon`  

```
small_trash_cup { //frame 967
    name FURNITURE_NAME_SMALL_TRASH_CUP
    desc FURNITURE_DESC_SMALL_TRASH_CUP

    Comfort 1
}
```

---

### `small_trash_cheese`
**Name:** Cheese  
**Description:** FURNITURE_DESC_SMALL_TRASH_CHEESE  
**Source:** `furniture_effects.gon`  

```
small_trash_cheese { //frame 968
    name FURNITURE_NAME_SMALL_TRASH_CHEESE
    desc FURNITURE_DESC_SMALL_TRASH_CHEESE
    
    Comfort -1
	Health 1
}
```

---

### `small_trash_brokenbottle`
**Name:** Small Broken Bottle  
**Description:** FURNITURE_DESC_SMALL_TRASH_BROKENBOTTLE  
**Source:** `furniture_effects.gon`  

```
small_trash_brokenbottle { //frame 969
    name FURNITURE_NAME_SMALL_TRASH_BROKENBOTTLE
    desc FURNITURE_DESC_SMALL_TRASH_BROKENBOTTLE
    
    Comfort 1
}
```

---

### `small_trash_milk`
**Name:** Empty Milk Carton  
**Description:** FURNITURE_DESC_SMALL_TRASH_MILK  
**Source:** `furniture_effects.gon`  

```
small_trash_milk { //frame 970
    name FURNITURE_NAME_SMALL_TRASH_MILK
    desc FURNITURE_DESC_SMALL_TRASH_MILK
    
    Comfort 1
}
```

---

### `small_trash_can2`
**Name:** Soda Can  
**Description:** FURNITURE_DESC_SMALL_TRASH_CAN2  
**Source:** `furniture_effects.gon`  

```
small_trash_can2 { //frame 971
    name FURNITURE_NAME_SMALL_TRASH_CAN2
    desc FURNITURE_DESC_SMALL_TRASH_CAN2
    
    Comfort 1
}
```

---

### `small_meds_mysterybottle`
**Name:** Glass Bottle  
**Description:** FURNITURE_DESC_SMALL_MEDS_MYSTERYBOTTLE  
**Source:** `furniture_effects.gon`  

```
small_meds_mysterybottle { //frame 972
    name FURNITURE_NAME_SMALL_MEDS_MYSTERYBOTTLE
    desc FURNITURE_DESC_SMALL_MEDS_MYSTERYBOTTLE
    
    Comfort -1
    Stimulation 1
    Appeal -1
	Evolution 1
}
```

---

### `small_meds_coughsyrup`
**Name:** Cough Syrup  
**Description:** FURNITURE_DESC_SMALL_MEDS_COUGHSYRUP  
**Source:** `furniture_effects.gon`  

```
small_meds_coughsyrup { //frame 973
    name FURNITURE_NAME_SMALL_MEDS_COUGHSYRUP
    desc FURNITURE_DESC_SMALL_MEDS_COUGHSYRUP
    
    Comfort 1
    Appeal -1
	Health 1
}
```

---

### `small_meds_pills1`
**Name:** Pill Bottle  
**Description:** FURNITURE_DESC_SMALL_MEDS_PILLS1  
**Source:** `furniture_effects.gon`  

```
small_meds_pills1 { //frame 974
    name FURNITURE_NAME_SMALL_MEDS_PILLS1
    desc FURNITURE_DESC_SMALL_MEDS_PILLS1
    
    Comfort 1
	Health 1
    Appeal -1
}
```

---

### `small_meds_pills2`
**Name:** Small Pill Bottle  
**Description:** FURNITURE_DESC_SMALL_MEDS_PILLS2  
**Source:** `furniture_effects.gon`  

```
small_meds_pills2 { //frame 975
    name FURNITURE_NAME_SMALL_MEDS_PILLS2
    desc FURNITURE_DESC_SMALL_MEDS_PILLS2
    
    Comfort 1
    Health 1
    Appeal -1
}
```

---

### `small_meds_mystery2`
**Name:** Mystery Medicine  
**Description:** FURNITURE_DESC_SMALL_MEDS_MYSTERY2  
**Source:** `furniture_effects.gon`  

```
small_meds_mystery2 { //frame 976
    name FURNITURE_NAME_SMALL_MEDS_MYSTERY2
    desc FURNITURE_DESC_SMALL_MEDS_MYSTERY2
    
    Comfort 1
    Stimulation 1
    Appeal -1
}
```

---

### `small_meds_fishoil`
**Name:** Fish Oil  
**Description:** FURNITURE_DESC_SMALL_MEDS_FISHOIL  
**Source:** `furniture_effects.gon`  

```
small_meds_fishoil { //frame 977
    name FURNITURE_NAME_SMALL_MEDS_FISHOIL
    desc FURNITURE_DESC_SMALL_MEDS_FISHOIL
    
    Comfort 1
    Health 1
    Appeal -1
}
```

---

### `small_meds_cathearts`
**Name:** Can of Cat Hearts  
**Description:** FURNITURE_DESC_SMALL_MEDS_CATHEARTS  
**Source:** `furniture_effects.gon`  

```
small_meds_cathearts { //frame 978
    name FURNITURE_NAME_SMALL_MEDS_CATHEARTS
    desc FURNITURE_DESC_SMALL_MEDS_CATHEARTS
    
    Comfort 1
    Stimulation 1
    Appeal -1
}
```

---

### `small_bottle_empty`
**Name:** Empty Bottle  
**Description:** FURNITURE_DESC_SMALL_BOTTLE_EMPTY  
**Source:** `furniture_effects.gon`  

```
small_bottle_empty { //frame 979
    name FURNITURE_NAME_SMALL_BOTTLE_EMPTY
    desc FURNITURE_DESC_SMALL_BOTTLE_EMPTY
    
    Comfort 1
    Stimulation 1
    Appeal -1
}
```

---

### `small_bottle_full`
**Name:** Bottle  
**Description:** FURNITURE_DESC_SMALL_BOTTLE_FULL  
**Source:** `furniture_effects.gon`  

```
small_bottle_full { //frame 980
    name FURNITURE_NAME_SMALL_BOTTLE_FULL
    desc FURNITURE_DESC_SMALL_BOTTLE_FULL
    
    Comfort 1
    Stimulation 1
    Appeal -1
}
```

---

### `small_bottle_2bottles`
**Name:** Glowing Bottle  
**Description:** FURNITURE_DESC_SMALL_BOTTLE_2BOTTLES  
**Source:** `furniture_effects.gon`  

```
small_bottle_2bottles { //frame 981
    name FURNITURE_NAME_SMALL_BOTTLE_2BOTTLES
    desc FURNITURE_DESC_SMALL_BOTTLE_2BOTTLES
    
    Comfort 1
    Stimulation 1
    Appeal -1
}
```

---

### `small_bobble_darkcat`
**Name:** Basic Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_DARKCAT  
**Source:** `furniture_effects.gon`  

```
small_bobble_darkcat { //frame 982
    name FURNITURE_NAME_SMALL_BOBBLE_DARKCAT
    desc FURNITURE_DESC_SMALL_BOBBLE_DARKCAT
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_guppy`
**Name:** Guppy Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_GUPPY  
**Source:** `furniture_effects.gon`  

```
small_bobble_guppy { //frame 983
    name FURNITURE_NAME_SMALL_BOBBLE_GUPPY
    desc FURNITURE_DESC_SMALL_BOBBLE_GUPPY
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_mad`
**Name:** Angry Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_MAD  
**Source:** `furniture_effects.gon`  

```
small_bobble_mad { //frame 984
    name FURNITURE_NAME_SMALL_BOBBLE_MAD
    desc FURNITURE_DESC_SMALL_BOBBLE_MAD
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_money`
**Name:** Lucky Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_MONEY  
**Source:** `furniture_effects.gon`  

```
small_bobble_money { //frame 985
    name FURNITURE_NAME_SMALL_BOBBLE_MONEY
    desc FURNITURE_DESC_SMALL_BOBBLE_MONEY
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_happy`
**Name:** Happy Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_HAPPY  
**Source:** `furniture_effects.gon`  

```
small_bobble_happy { //frame 986
    name FURNITURE_NAME_SMALL_BOBBLE_HAPPY
    desc FURNITURE_DESC_SMALL_BOBBLE_HAPPY
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_dan`
**Name:** Synj Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_DAN  
**Source:** `furniture_effects.gon`  

```
small_bobble_dan { //frame 987
    name FURNITURE_NAME_SMALL_BOBBLE_DAN
    desc FURNITURE_DESC_SMALL_BOBBLE_DAN
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_zombie`
**Name:** Zombie Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_ZOMBIE  
**Source:** `furniture_effects.gon`  

```
small_bobble_zombie { //frame 988
    name FURNITURE_NAME_SMALL_BOBBLE_ZOMBIE
    desc FURNITURE_DESC_SMALL_BOBBLE_ZOMBIE
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_grump`
**Name:** Irritable Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_GRUMP  
**Source:** `furniture_effects.gon`  

```
small_bobble_grump { //frame 989
    name FURNITURE_NAME_SMALL_BOBBLE_GRUMP
    desc FURNITURE_DESC_SMALL_BOBBLE_GRUMP
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_alone`
**Name:** Lonely Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_ALONE  
**Source:** `furniture_effects.gon`  

```
small_bobble_alone { //frame 990
    name FURNITURE_NAME_SMALL_BOBBLE_ALONE
    desc FURNITURE_DESC_SMALL_BOBBLE_ALONE
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_spots`
**Name:** Spotty Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_SPOTS  
**Source:** `furniture_effects.gon`  

```
small_bobble_spots { //frame 991
    name FURNITURE_NAME_SMALL_BOBBLE_SPOTS
    desc FURNITURE_DESC_SMALL_BOBBLE_SPOTS
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_bobble_devil`
**Name:** Devil Cat Bobble  
**Description:** FURNITURE_DESC_SMALL_BOBBLE_DEVIL  
**Source:** `furniture_effects.gon`  

```
small_bobble_devil { //frame 992
    name FURNITURE_NAME_SMALL_BOBBLE_DEVIL
    desc FURNITURE_DESC_SMALL_BOBBLE_DEVIL
    
    Comfort 1
    Stimulation -1
    Appeal 1
}
```

---

### `small_lab_tank1`
**Name:** Lab Tank A  
**Description:** FURNITURE_DESC_SMALL_LAB_TANK1  
**Source:** `furniture_effects.gon`  

```
small_lab_tank1 { //frame 993
    name FURNITURE_NAME_SMALL_LAB_TANK1
    desc FURNITURE_DESC_SMALL_LAB_TANK1
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_lab_tank2`
**Name:** Lab Tank B  
**Description:** FURNITURE_DESC_SMALL_LAB_TANK2  
**Source:** `furniture_effects.gon`  

```
small_lab_tank2 { //frame 994
    name FURNITURE_NAME_SMALL_LAB_TANK2
    desc FURNITURE_DESC_SMALL_LAB_TANK2
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_lab_jug1`
**Name:** Lab Jug A  
**Description:** FURNITURE_DESC_SMALL_LAB_JUG1  
**Source:** `furniture_effects.gon`  

```
small_lab_jug1 { //frame 995
    name FURNITURE_NAME_SMALL_LAB_JUG1
    desc FURNITURE_DESC_SMALL_LAB_JUG1
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_lab_jug2`
**Name:** Lab Jug B  
**Description:** FURNITURE_DESC_SMALL_LAB_JUG2  
**Source:** `furniture_effects.gon`  

```
small_lab_jug2 { //frame 996
    name FURNITURE_NAME_SMALL_LAB_JUG2
    desc FURNITURE_DESC_SMALL_LAB_JUG2
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_lab_jug3`
**Name:** Bleach Jug  
**Description:** FURNITURE_DESC_SMALL_LAB_JUG3  
**Source:** `furniture_effects.gon`  

```
small_lab_jug3 { //frame 997
    name FURNITURE_NAME_SMALL_LAB_JUG3
    desc FURNITURE_DESC_SMALL_LAB_JUG3
    
    Comfort -1
    Stimulation 3
    Appeal -1
}
```

---

### `small_lab_testtube`
**Name:** Test Tube  
**Description:** FURNITURE_DESC_SMALL_LAB_TESTTUBE  
**Source:** `furniture_effects.gon`  

```
small_lab_testtube { //frame 998
    name FURNITURE_NAME_SMALL_LAB_TESTTUBE
    desc FURNITURE_DESC_SMALL_LAB_TESTTUBE
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_lab_testtube2`
**Name:** Test Tubes  
**Description:** FURNITURE_DESC_SMALL_LAB_TESTTUBE2  
**Source:** `furniture_effects.gon`  

```
small_lab_testtube2 { //frame 999
    name FURNITURE_NAME_SMALL_LAB_TESTTUBE2
    desc FURNITURE_DESC_SMALL_LAB_TESTTUBE2
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_lab_flask`
**Name:** Boiling Flask  
**Description:** FURNITURE_DESC_SMALL_LAB_FLASK  
**Source:** `furniture_effects.gon`  

```
small_lab_flask { //frame 1000
    name FURNITURE_NAME_SMALL_LAB_FLASK
    desc FURNITURE_DESC_SMALL_LAB_FLASK
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_lab_flask2`
**Name:** Erlenmeyer Flask  
**Description:** FURNITURE_DESC_SMALL_LAB_FLASK2  
**Source:** `furniture_effects.gon`  

```
small_lab_flask2 { //frame 1001
    name FURNITURE_NAME_SMALL_LAB_FLASK2
    desc FURNITURE_DESC_SMALL_LAB_FLASK2
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_lab_flask3`
**Name:** Small Beaker  
**Description:** FURNITURE_DESC_SMALL_LAB_FLASK3  
**Source:** `furniture_effects.gon`  

```
small_lab_flask3 { //frame 1002
    name FURNITURE_NAME_SMALL_LAB_FLASK3
    desc FURNITURE_DESC_SMALL_LAB_FLASK3
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_lab_flask4`
**Name:** Round Bottom Flask  
**Description:** FURNITURE_DESC_SMALL_LAB_FLASK4  
**Source:** `furniture_effects.gon`  

```
small_lab_flask4 { //frame 1003
    name FURNITURE_NAME_SMALL_LAB_FLASK4
    desc FURNITURE_DESC_SMALL_LAB_FLASK4
    
    Comfort -1
    Evolution 1
    Appeal -1
}
```

---

### `small_food_root`
**Name:** Mandrake Root  
**Description:** FURNITURE_DESC_SMALL_FOOD_ROOT  
**Source:** `furniture_effects.gon`  

```
small_food_root { //frame 1004
    name FURNITURE_NAME_SMALL_FOOD_ROOT
    desc FURNITURE_DESC_SMALL_FOOD_ROOT
    
    Health 1
}
```

---

### `small_food_lemon`
**Name:** Lemon  
**Description:** FURNITURE_DESC_SMALL_FOOD_LEMON  
**Source:** `furniture_effects.gon`  

```
small_food_lemon { //frame 1005
    name FURNITURE_NAME_SMALL_FOOD_LEMON
    desc FURNITURE_DESC_SMALL_FOOD_LEMON
    
    Health 1
}
```

---

### `small_food_orange`
**Name:** Orange  
**Description:** FURNITURE_DESC_SMALL_FOOD_ORANGE  
**Source:** `furniture_effects.gon`  

```
small_food_orange { //frame 1006
    name FURNITURE_NAME_SMALL_FOOD_ORANGE
    desc FURNITURE_DESC_SMALL_FOOD_ORANGE
    
    Health 1
}
```

---

### `small_food_radish`
**Name:** Radish  
**Description:** FURNITURE_DESC_SMALL_FOOD_RADISH  
**Source:** `furniture_effects.gon`  

```
small_food_radish { //frame 1007
    name FURNITURE_NAME_SMALL_FOOD_RADISH
    desc FURNITURE_DESC_SMALL_FOOD_RADISH
    
    Health 1
}
```

---

### `small_food_onion`
**Name:** Onion  
**Description:** FURNITURE_DESC_SMALL_FOOD_ONION  
**Source:** `furniture_effects.gon`  

```
small_food_onion { //frame 1008
    name FURNITURE_NAME_SMALL_FOOD_ONION
    desc FURNITURE_DESC_SMALL_FOOD_ONION
    
    Health 1
}
```

---

### `small_food_apple`
**Name:** Apple  
**Description:** FURNITURE_DESC_SMALL_FOOD_APPLE  
**Source:** `furniture_effects.gon`  

```
small_food_apple { //frame 1009
    name FURNITURE_NAME_SMALL_FOOD_APPLE
    desc FURNITURE_DESC_SMALL_FOOD_APPLE
    
    Health 1
}
```

---

### `small_food_squash`
**Name:** Squash  
**Description:** FURNITURE_DESC_SMALL_FOOD_SQUASH  
**Source:** `furniture_effects.gon`  

```
small_food_squash { //frame 1010
    name FURNITURE_NAME_SMALL_FOOD_SQUASH
    desc FURNITURE_DESC_SMALL_FOOD_SQUASH
    
    Health 1
}
```

---

### `small_food_eggplant`
**Name:** Eggplant  
**Description:** FURNITURE_DESC_SMALL_FOOD_EGGPLANT  
**Source:** `furniture_effects.gon`  

```
small_food_eggplant { //frame 1011
    name FURNITURE_NAME_SMALL_FOOD_EGGPLANT
    desc FURNITURE_DESC_SMALL_FOOD_EGGPLANT
    
    Health 1
}
```

---

### `small_food_broccoli`
**Name:** Broccoli  
**Description:** FURNITURE_DESC_SMALL_FOOD_BROCCOLI  
**Source:** `furniture_effects.gon`  

```
small_food_broccoli { //frame 1012
    name FURNITURE_NAME_SMALL_FOOD_BROCCOLI
    desc FURNITURE_DESC_SMALL_FOOD_BROCCOLI
    
    Health 1
}
```

---

### `small_food_pumpkin`
**Name:** Pumpkin  
**Description:** FURNITURE_DESC_SMALL_FOOD_PUMPKIN  
**Source:** `furniture_effects.gon`  

```
small_food_pumpkin { //frame 1013
    name FURNITURE_NAME_SMALL_FOOD_PUMPKIN
    desc FURNITURE_DESC_SMALL_FOOD_PUMPKIN
    
    Health 1
}
```

---

### `small_food_pineapple`
**Name:** Pineapple  
**Description:** FURNITURE_DESC_SMALL_FOOD_PINEAPPLE  
**Source:** `furniture_effects.gon`  

```
small_food_pineapple { //frame 1014
    name FURNITURE_NAME_SMALL_FOOD_PINEAPPLE
    desc FURNITURE_DESC_SMALL_FOOD_PINEAPPLE
    
    Health 1
}
```

---

### `small_food_potato`
**Name:** Potato  
**Description:** FURNITURE_DESC_SMALL_FOOD_POTATO  
**Source:** `furniture_effects.gon`  

```
small_food_potato { //frame 1015
    name FURNITURE_NAME_SMALL_FOOD_POTATO
    desc FURNITURE_DESC_SMALL_FOOD_POTATO
    
    Health 1
}
```

---

### `small_doll_stacy`
**Name:** Stacy Plush  
**Description:** FURNITURE_DESC_SMALL_DOLL_STACY  
**Source:** `furniture_effects.gon`  

```
small_doll_stacy { //frame 1016
    name FURNITURE_NAME_SMALL_DOLL_STACY
    desc FURNITURE_DESC_SMALL_DOLL_STACY
    
    Comfort 1
}
```

---

### `small_doll_aether`
**Name:** Aether Plush  
**Description:** FURNITURE_DESC_SMALL_DOLL_AETHER  
**Source:** `furniture_effects.gon`  

```
small_doll_aether { //frame 1017
    name FURNITURE_NAME_SMALL_DOLL_AETHER
    desc FURNITURE_DESC_SMALL_DOLL_AETHER
    
    Comfort 1
}
```

---

### `small_doll_duke`
**Name:** Duke of Flies Plush  
**Description:** FURNITURE_DESC_SMALL_DOLL_DUKE  
**Source:** `furniture_effects.gon`  

```
small_doll_duke { //frame 1018
    name FURNITURE_NAME_SMALL_DOLL_DUKE
    desc FURNITURE_DESC_SMALL_DOLL_DUKE
    
    Comfort 1
}
```

---

### `small_doll_guppy`
**Name:** Guppy Plush  
**Description:** FURNITURE_DESC_SMALL_DOLL_GUPPY  
**Source:** `furniture_effects.gon`  

```
small_doll_guppy { //frame 1019
    name FURNITURE_NAME_SMALL_DOLL_GUPPY
    desc FURNITURE_DESC_SMALL_DOLL_GUPPY
    
    Comfort 1
}
```

---

### `small_doll_gish`
**Name:** Gish Plush  
**Description:** FURNITURE_DESC_SMALL_DOLL_GISH  
**Source:** `furniture_effects.gon`  

```
small_doll_gish { //frame 1020
    name FURNITURE_NAME_SMALL_DOLL_GISH
    desc FURNITURE_DESC_SMALL_DOLL_GISH
    
    Comfort 1
}
```

---

### `small_doll_isaac`
**Name:** Isaac Plush  
**Description:** FURNITURE_DESC_SMALL_DOLL_ISAAC  
**Source:** `furniture_effects.gon`  

```
small_doll_isaac { //frame 1021
    name FURNITURE_NAME_SMALL_DOLL_ISAAC
    desc FURNITURE_DESC_SMALL_DOLL_ISAAC
    
    Comfort 1
}
```

---

### `small_doll_steven`
**Name:** Steven Plush  
**Description:** FURNITURE_DESC_SMALL_DOLL_STEVEN  
**Source:** `furniture_effects.gon`  

```
small_doll_steven { //frame 1022
    name FURNITURE_NAME_SMALL_DOLL_STEVEN
    desc FURNITURE_DESC_SMALL_DOLL_STEVEN
    
    Comfort 1
}
```

---

### `small_electronics_gamesystem`
**Name:** Game System  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_GAMESYSTEM  
**Source:** `furniture_effects.gon`  

```
small_electronics_gamesystem { //frame 1023
    name FURNITURE_NAME_SMALL_ELECTRONICS_GAMESYSTEM
    desc FURNITURE_DESC_SMALL_ELECTRONICS_GAMESYSTEM
    
    Stimulation 1
}
```

---

### `small_electronics_gamepad`
**Name:** Gamepad  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_GAMEPAD  
**Source:** `furniture_effects.gon`  

```
small_electronics_gamepad { //frame 1024
    name FURNITURE_NAME_SMALL_ELECTRONICS_GAMEPAD
    desc FURNITURE_DESC_SMALL_ELECTRONICS_GAMEPAD
    
    Stimulation 1
}
```

---

### `small_electronics_speaker`
**Name:** Small Speaker  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_SPEAKER  
**Source:** `furniture_effects.gon`  

```
small_electronics_speaker { //frame 1025
    name FURNITURE_NAME_SMALL_ELECTRONICS_SPEAKER
    desc FURNITURE_DESC_SMALL_ELECTRONICS_SPEAKER
    
    Stimulation 1
}
```

---

### `small_electronics_mouse`
**Name:** Mouse  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_MOUSE  
**Source:** `furniture_effects.gon`  

```
small_electronics_mouse { //frame 1026
    name FURNITURE_NAME_SMALL_ELECTRONICS_MOUSE
    desc FURNITURE_DESC_SMALL_ELECTRONICS_MOUSE
    
    Stimulation 1
}
```

---

### `small_electronics_phone1`
**Name:** Retro Phone A  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_PHONE1  
**Source:** `furniture_effects.gon`  

```
small_electronics_phone1 { //frame 1027
    name FURNITURE_NAME_SMALL_ELECTRONICS_PHONE1
    desc FURNITURE_DESC_SMALL_ELECTRONICS_PHONE1
    
    Stimulation 1
}
```

---

### `small_electronics_phone2`
**Name:** Rotary Phone B  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_PHONE2  
**Source:** `furniture_effects.gon`  

```
small_electronics_phone2 { //frame 1028
    name FURNITURE_NAME_SMALL_ELECTRONICS_PHONE2
    desc FURNITURE_DESC_SMALL_ELECTRONICS_PHONE2
    
    Stimulation 1
}
```

---

### `small_electronics_phone3`
**Name:** Rotary Phone C  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_PHONE3  
**Source:** `furniture_effects.gon`  

```
small_electronics_phone3 { //frame 1029
    name FURNITURE_NAME_SMALL_ELECTRONICS_PHONE3
    desc FURNITURE_DESC_SMALL_ELECTRONICS_PHONE3
    
    Stimulation 1
}
```

---

### `small_electronics_oldphone`
**Name:** Antique Phone A  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_OLDPHONE  
**Source:** `furniture_effects.gon`  

```
small_electronics_oldphone { //frame 1030
    name FURNITURE_NAME_SMALL_ELECTRONICS_OLDPHONE
    desc FURNITURE_DESC_SMALL_ELECTRONICS_OLDPHONE
    
    Stimulation 1
}
```

---

### `small_electronics_oldphone2`
**Name:** Antique Phone B  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_OLDPHONE2  
**Source:** `furniture_effects.gon`  

```
small_electronics_oldphone2 { //frame 1031
    name FURNITURE_NAME_SMALL_ELECTRONICS_OLDPHONE2
    desc FURNITURE_DESC_SMALL_ELECTRONICS_OLDPHONE2
    
    Stimulation 1
}
```

---

### `small_electronics_oldphone3`
**Name:** Antique Phone C  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_OLDPHONE3  
**Source:** `furniture_effects.gon`  

```
small_electronics_oldphone3 { //frame 1032
    name FURNITURE_NAME_SMALL_ELECTRONICS_OLDPHONE3
    desc FURNITURE_DESC_SMALL_ELECTRONICS_OLDPHONE3
    
    Stimulation 1
}
```

---

### `small_electronics_lipphone`
**Name:** Lips Phone  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_LIPPHONE  
**Source:** `furniture_effects.gon`  

```
small_electronics_lipphone { //frame 1033
    name FURNITURE_NAME_SMALL_ELECTRONICS_LIPPHONE
    desc FURNITURE_DESC_SMALL_ELECTRONICS_LIPPHONE
    
    Stimulation 1
}
```

---

### `small_electronics_duckphone`
**Name:** Duck Phone  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_DUCKPHONE  
**Source:** `furniture_effects.gon`  

```
small_electronics_duckphone { //frame 1034
    name FURNITURE_NAME_SMALL_ELECTRONICS_DUCKPHONE
    desc FURNITURE_DESC_SMALL_ELECTRONICS_DUCKPHONE
    
    Stimulation 1
}
```

---

### `small_electronics_cellphone`
**Name:** 90s Cell Phone  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_CELLPHONE  
**Source:** `furniture_effects.gon`  

```
small_electronics_cellphone { //frame 1035
    name FURNITURE_NAME_SMALL_ELECTRONICS_CELLPHONE
    desc FURNITURE_DESC_SMALL_ELECTRONICS_CELLPHONE
    
    Stimulation 1
}
```

---

### `small_electronics_handradio`
**Name:** Retro Hand Radio  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_HANDRADIO  
**Source:** `furniture_effects.gon`  

```
small_electronics_handradio { //frame 1036
    name FURNITURE_NAME_SMALL_ELECTRONICS_HANDRADIO
    desc FURNITURE_DESC_SMALL_ELECTRONICS_HANDRADIO
    
    Stimulation 1
}
```

---

### `small_electronics_handradio2`
**Name:** Antique Hand Radio  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_HANDRADIO2  
**Source:** `furniture_effects.gon`  

```
small_electronics_handradio2 { //frame 1037
    name FURNITURE_NAME_SMALL_ELECTRONICS_HANDRADIO2
    desc FURNITURE_DESC_SMALL_ELECTRONICS_HANDRADIO2
    
    Stimulation 1
}
```

---

### `small_electronics_walkytalky`
**Name:** Walky-Talkie  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_WALKYTALKY  
**Source:** `furniture_effects.gon`  

```
small_electronics_walkytalky { //frame 1038
    name FURNITURE_NAME_SMALL_ELECTRONICS_WALKYTALKY
    desc FURNITURE_DESC_SMALL_ELECTRONICS_WALKYTALKY
    
    Stimulation 1
}
```

---

### `small_electronics_brain`
**Name:** Brain of Glorg  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_BRAIN  
**Source:** `furniture_effects.gon`  

```
small_electronics_brain { //frame 1039
    name FURNITURE_NAME_SMALL_ELECTRONICS_BRAIN
    desc FURNITURE_DESC_SMALL_ELECTRONICS_BRAIN
    
    Evolution 4
    Appeal -4
}
```

---

### `small_electronics_mysteriousskull`
**Name:** Ethereal Skull  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_MYSTERIOUSSKULL  
**Source:** `furniture_effects.gon`  

```
small_electronics_mysteriousskull { //frame 1040
    name FURNITURE_NAME_SMALL_ELECTRONICS_MYSTERIOUSSKULL
    desc FURNITURE_DESC_SMALL_ELECTRONICS_MYSTERIOUSSKULL
    
    Evolution 4
    Appeal -4
}
```

---

### `small_electronics_moon`
**Name:** Small Asteroid  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_MOON  
**Source:** `furniture_effects.gon`  

```
small_electronics_moon { //frame 1041
    name FURNITURE_NAME_SMALL_ELECTRONICS_MOON
    desc FURNITURE_DESC_SMALL_ELECTRONICS_MOON
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_electronics_ooze`
**Name:** Ooze Canister  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_OOZE  
**Source:** `furniture_effects.gon`  

```
small_electronics_ooze { //frame 1042
    name FURNITURE_NAME_SMALL_ELECTRONICS_OOZE
    desc FURNITURE_DESC_SMALL_ELECTRONICS_OOZE

    Health -1
	Evolution 2
    Appeal -1
}
```

---

### `small_jar_diseases`
**Name:** Jar of Diseases  
**Description:** FURNITURE_DESC_SMALL_JAR_DISEASES  
**Source:** `furniture_effects.gon`  

```
small_jar_diseases { //frame 1043
    name FURNITURE_NAME_SMALL_JAR_DISEASES
    desc FURNITURE_DESC_SMALL_JAR_DISEASES
    
    Stimulation 2
    Health -6
}
```

---

### `small_jar_eyeballs`
**Name:** Jar of Eyeballs  
**Description:** FURNITURE_DESC_SMALL_JAR_EYEBALLS  
**Source:** `furniture_effects.gon`  

```
small_jar_eyeballs { //frame 1044
    name FURNITURE_NAME_SMALL_JAR_EYEBALLS
    desc FURNITURE_DESC_SMALL_JAR_EYEBALLS
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_jar_heart`
**Name:** Heart in a Jar  
**Description:** FURNITURE_DESC_SMALL_JAR_HEART  
**Source:** `furniture_effects.gon`  

```
small_jar_heart { //frame 1045
    name FURNITURE_NAME_SMALL_JAR_HEART
    desc FURNITURE_DESC_SMALL_JAR_HEART
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_jar_spider`
**Name:** Daddy Long Legs  
**Description:** FURNITURE_DESC_SMALL_JAR_SPIDER  
**Source:** `furniture_effects.gon`  

```
small_jar_spider { //frame 1046
    name FURNITURE_NAME_SMALL_JAR_SPIDER
    desc FURNITURE_DESC_SMALL_JAR_SPIDER
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_jar_fish`
**Name:** Jar of Guppies  
**Description:** FURNITURE_DESC_SMALL_JAR_FISH  
**Source:** `furniture_effects.gon`  

```
small_jar_fish { //frame 1047
    name FURNITURE_NAME_SMALL_JAR_FISH
    desc FURNITURE_DESC_SMALL_JAR_FISH
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_jar_flys`
**Name:** Jar of Flies  
**Description:** FURNITURE_DESC_SMALL_JAR_FLYS  
**Source:** `furniture_effects.gon`  

```
small_jar_flys { //frame 1048
    name FURNITURE_NAME_SMALL_JAR_FLYS
    desc FURNITURE_DESC_SMALL_JAR_FLYS
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_jar_fairy`
**Name:** Fairy in a Jar  
**Description:** FURNITURE_DESC_SMALL_JAR_FAIRY  
**Source:** `furniture_effects.gon`  

```
small_jar_fairy { //frame 1049
    name FURNITURE_NAME_SMALL_JAR_FAIRY
    desc FURNITURE_DESC_SMALL_JAR_FAIRY
    
    Health 2
    Comfort 1
}
```

---

### `small_jar_coins`
**Name:** Jar of Pennies  
**Description:** FURNITURE_DESC_SMALL_JAR_COINS  
**Source:** `furniture_effects.gon`  

```
small_jar_coins { //frame 1050
    name FURNITURE_NAME_SMALL_JAR_COINS
    desc FURNITURE_DESC_SMALL_JAR_COINS
    
    Comfort 1
}
```

---

### `small_jar_nails`
**Name:** Jar of Nails  
**Description:** FURNITURE_DESC_SMALL_JAR_NAILS  
**Source:** `furniture_effects.gon`  

```
small_jar_nails { //frame 1051
    name FURNITURE_NAME_SMALL_JAR_NAILS
    desc FURNITURE_DESC_SMALL_JAR_NAILS
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_jar_ghost`
**Name:** Inky  
**Description:** FURNITURE_DESC_SMALL_JAR_GHOST  
**Source:** `furniture_effects.gon`  

```
small_jar_ghost { //frame 1052
    name FURNITURE_NAME_SMALL_JAR_GHOST
    desc FURNITURE_DESC_SMALL_JAR_GHOST
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_jar_empty`
**Name:** Mason Jar  
**Description:** FURNITURE_DESC_SMALL_JAR_EMPTY  
**Source:** `furniture_effects.gon`  

```
small_jar_empty { //frame 1053
    name FURNITURE_NAME_SMALL_JAR_EMPTY
    desc FURNITURE_DESC_SMALL_JAR_EMPTY
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_jar_empty2`
**Name:** Medical Jar  
**Description:** FURNITURE_DESC_SMALL_JAR_EMPTY2  
**Source:** `furniture_effects.gon`  

```
small_jar_empty2 { //frame 1054
    name FURNITURE_NAME_SMALL_JAR_EMPTY2
    desc FURNITURE_DESC_SMALL_JAR_EMPTY2
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_jar_empty3`
**Name:** Pint Jar  
**Description:** FURNITURE_DESC_SMALL_JAR_EMPTY3  
**Source:** `furniture_effects.gon`  

```
small_jar_empty3 { //frame 1055
    name FURNITURE_NAME_SMALL_JAR_EMPTY3
    desc FURNITURE_DESC_SMALL_JAR_EMPTY3
    
    Stimulation 2
    Appeal -1
}
```

---

### `small_gem`
**Name:** Small Gem  
**Description:** FURNITURE_DESC_SMALL_GEM  
**Source:** `furniture_effects.gon`  

```
small_gem { //frame 1056
    name FURNITURE_NAME_SMALL_GEM
    desc FURNITURE_DESC_SMALL_GEM
    
    Appeal 2
}
```

---

### `small_lotion`
**Name:** Lotion  
**Description:** FURNITURE_DESC_SMALL_LOTION  
**Source:** `furniture_effects.gon`  

```
small_lotion { //frame 1057
    name FURNITURE_NAME_SMALL_LOTION
    desc FURNITURE_DESC_SMALL_LOTION
    
    Comfort 1
}
```

---

### `small_tissues`
**Name:** Tissues  
**Description:** FURNITURE_DESC_SMALL_TISSUES  
**Source:** `furniture_effects.gon`  

```
small_tissues { //frame 1058
    name FURNITURE_NAME_SMALL_TISSUES
    desc FURNITURE_DESC_SMALL_TISSUES
    
    Comfort 1
}
```

---

### `small_picture_spoon`
**Name:** Small Picture Frame A  
**Description:** FURNITURE_DESC_SMALL_PICTURE_SPOON  
**Source:** `furniture_effects.gon`  

```
small_picture_spoon { //frame 1059
    name FURNITURE_NAME_SMALL_PICTURE_SPOON
    desc FURNITURE_DESC_SMALL_PICTURE_SPOON
    
    Comfort 1
}
```

---

### `small_picture_cat`
**Name:** Small Picture Frame B  
**Description:** FURNITURE_DESC_SMALL_PICTURE_CAT  
**Source:** `furniture_effects.gon`  

```
small_picture_cat { //frame 1060
    name FURNITURE_NAME_SMALL_PICTURE_CAT
    desc FURNITURE_DESC_SMALL_PICTURE_CAT
    
    Comfort 1
}
```

---

### `small_picture_can`
**Name:** Small Picture Frame C  
**Description:** FURNITURE_DESC_SMALL_PICTURE_CAN  
**Source:** `furniture_effects.gon`  

```
small_picture_can { //frame 1061
    name FURNITURE_NAME_SMALL_PICTURE_CAN
    desc FURNITURE_DESC_SMALL_PICTURE_CAN
    
    Comfort 1
}
```

---

### `small_alarmclock1`
**Name:** Digital Alarm Clock  
**Description:** FURNITURE_DESC_SMALL_ALARMCLOCK1  
**Source:** `furniture_effects.gon`  

```
small_alarmclock1 { //frame 1062
    name FURNITURE_NAME_SMALL_ALARMCLOCK1
    desc FURNITURE_DESC_SMALL_ALARMCLOCK1
    
    Comfort 1
}
```

---

### `small_alarmclock2`
**Name:** Alarm Clock  
**Description:** FURNITURE_DESC_SMALL_ALARMCLOCK2  
**Source:** `furniture_effects.gon`  

```
small_alarmclock2 { //frame 1063
    name FURNITURE_NAME_SMALL_ALARMCLOCK2
    desc FURNITURE_DESC_SMALL_ALARMCLOCK2
    
    Comfort 1
}
```

---

### `small_pillbottle`
**Name:** Small Pill Bottle  
**Description:** FURNITURE_DESC_SMALL_PILLBOTTLE  
**Source:** `furniture_effects.gon`  

```
small_pillbottle { //frame 1064
    name FURNITURE_NAME_SMALL_PILLBOTTLE
    desc FURNITURE_DESC_SMALL_PILLBOTTLE
    
    Health 1
}
```

---

### `small_waterbottle`
**Name:** Water Bottle  
**Description:** FURNITURE_DESC_SMALL_WATERBOTTLE  
**Source:** `furniture_effects.gon`  

```
small_waterbottle { //frame 1065
    name FURNITURE_NAME_SMALL_WATERBOTTLE
    desc FURNITURE_DESC_SMALL_WATERBOTTLE
    
    Health 1
}
```

---

### `small_milk`
**Name:** Milk Jug  
**Description:** FURNITURE_DESC_SMALL_MILK  
**Source:** `furniture_effects.gon`  

```
small_milk { //frame 1066
    name FURNITURE_NAME_SMALL_MILK
    desc FURNITURE_DESC_SMALL_MILK
    
    Health 1
}
```

---

### `small_kettle`
**Name:** Kettle  
**Description:** FURNITURE_DESC_SMALL_KETTLE  
**Source:** `furniture_effects.gon`  

```
small_kettle { //frame 1067
    name FURNITURE_NAME_SMALL_KETTLE
    desc FURNITURE_DESC_SMALL_KETTLE
    
    Comfort 1
}
```

---

### `small_bowlingball`
**Name:** Bowling Ball  
**Description:** FURNITURE_DESC_SMALL_BOWLINGBALL  
**Source:** `furniture_effects.gon`  

```
small_bowlingball { //frame 1068
    name FURNITURE_NAME_SMALL_BOWLINGBALL
    desc FURNITURE_DESC_SMALL_BOWLINGBALL
    
    Appeal 1
}
```

---

### `small_pin`
**Name:** Bowling Pin  
**Description:** FURNITURE_DESC_SMALL_PIN  
**Source:** `furniture_effects.gon`  

```
small_pin { //frame 1069
    name FURNITURE_NAME_SMALL_PIN
    desc FURNITURE_DESC_SMALL_PIN
    
    Appeal 1
}
```

---

### `small_mug`
**Name:** Mug  
**Description:** FURNITURE_DESC_SMALL_MUG  
**Source:** `furniture_effects.gon`  

```
small_mug { //frame 1070
    name FURNITURE_NAME_SMALL_MUG
    desc FURNITURE_DESC_SMALL_MUG
    
    Comfort 1
}
```

---

### `small_pencup`
**Name:** Pen Cup  
**Description:** FURNITURE_DESC_SMALL_PENCUP  
**Source:** `furniture_effects.gon`  

```
small_pencup { //frame 1071
    name FURNITURE_NAME_SMALL_PENCUP
    desc FURNITURE_DESC_SMALL_PENCUP
    
    Comfort 1
}
```

---

### `small_food_sausage`
**Name:** Sausage  
**Description:** FURNITURE_DESC_SMALL_FOOD_SAUSAGE  
**Source:** `furniture_effects.gon`  

```
small_food_sausage { //frame 1072
    name FURNITURE_NAME_SMALL_FOOD_SAUSAGE
    desc FURNITURE_DESC_SMALL_FOOD_SAUSAGE
    
    Comfort 1
	Health 1
}
```

---

### `small_deadrat`
**Name:** Dead Rat  
**Description:** FURNITURE_DESC_SMALL_DEADRAT  
**Source:** `furniture_effects.gon`  

```
small_deadrat { //frame 1073
    name FURNITURE_NAME_SMALL_DEADRAT
    desc FURNITURE_DESC_SMALL_DEADRAT
    
    Stimulation 3
	Health -1
    
}
```

---

### `small_blackbox`
**Name:** Black Box  
**Description:** FURNITURE_DESC_SMALL_BLACKBOX  
**Source:** `furniture_effects.gon`  

```
small_blackbox { //frame 1074
    name FURNITURE_NAME_SMALL_BLACKBOX
    desc FURNITURE_DESC_SMALL_BLACKBOX
    
    Evolution 1
}
```

---

### `small_eyeball`
**Name:** Eyeball  
**Description:** FURNITURE_DESC_SMALL_EYEBALL  
**Source:** `furniture_effects.gon`  

```
small_eyeball { //frame 1075
    name FURNITURE_NAME_SMALL_EYEBALL
    desc FURNITURE_DESC_SMALL_EYEBALL
    
    Comfort 1
}
```

---

### `small_perfume`
**Name:** Perfume  
**Description:** FURNITURE_DESC_SMALL_PERFUME  
**Source:** `furniture_effects.gon`  

```
small_perfume { //frame 1076
    name FURNITURE_NAME_SMALL_PERFUME
    desc FURNITURE_DESC_SMALL_PERFUME
    
    Comfort 1
}
```

---

### `small_jar_tadpole`
**Name:** Tadpole in a Jar  
**Description:** FURNITURE_DESC_SMALL_JAR_TADPOLE  
**Source:** `furniture_effects.gon`  

```
small_jar_tadpole { //frame 1077
    name FURNITURE_NAME_SMALL_JAR_TADPOLE
    desc FURNITURE_DESC_SMALL_JAR_TADPOLE
    
    Comfort 1
}
```

---

### `small_jug`
**Name:** Jug  
**Description:** FURNITURE_DESC_SMALL_JUG  
**Source:** `furniture_effects.gon`  

```
small_jug { //frame 1078
    name FURNITURE_NAME_SMALL_JUG
    desc FURNITURE_DESC_SMALL_JUG
    
    Comfort 1
}
```

---

### `small_couch`
**Name:** Toy Couch  
**Description:** FURNITURE_DESC_SMALL_COUCH  
**Source:** `furniture_effects.gon`  

```
small_couch { //frame 1079
    name FURNITURE_NAME_SMALL_COUCH
    desc FURNITURE_DESC_SMALL_COUCH
    
    Comfort 1
}
```

---

### `small_frige`
**Name:** Toy Fridge  
**Description:** FURNITURE_DESC_SMALL_FRIGE  
**Source:** `furniture_effects.gon`  

```
small_frige { //frame 1080
    name FURNITURE_NAME_SMALL_FRIGE
    desc FURNITURE_DESC_SMALL_FRIGE
    Comfort 1
}
```

---

### `small_sink`
**Name:** Toy Sink  
**Description:** FURNITURE_DESC_SMALL_SINK  
**Source:** `furniture_effects.gon`  

```
small_sink { //frame 1081
    name FURNITURE_NAME_SMALL_SINK
    desc FURNITURE_DESC_SMALL_SINK
    
    Comfort 1
}
```

---

### `small_stove`
**Name:** Toy Stove  
**Description:** FURNITURE_DESC_SMALL_STOVE  
**Source:** `furniture_effects.gon`  

```
small_stove { //frame 1082
    name FURNITURE_NAME_SMALL_STOVE
    desc FURNITURE_DESC_SMALL_STOVE
    
    Comfort 1
}
```

---

### `small_crate`
**Name:** Toy Crate  
**Description:** FURNITURE_DESC_SMALL_CRATE  
**Source:** `furniture_effects.gon`  

```
small_crate { //frame 1083
    name FURNITURE_NAME_SMALL_CRATE
    desc FURNITURE_DESC_SMALL_CRATE
    
    Comfort 1
}
```

---

### `small_bed`
**Name:** Toy Bed  
**Description:** FURNITURE_DESC_SMALL_BED  
**Source:** `furniture_effects.gon`  

```
small_bed { //frame 1084
    name FURNITURE_NAME_SMALL_BED
    desc FURNITURE_DESC_SMALL_BED
    
    Comfort 1
}
```

---

### `small_sidetable`
**Name:** Toy Table  
**Description:** FURNITURE_DESC_SMALL_SIDETABLE  
**Source:** `furniture_effects.gon`  

```
small_sidetable { //frame 1085
    name FURNITURE_NAME_SMALL_SIDETABLE
    desc FURNITURE_DESC_SMALL_SIDETABLE
    
    Comfort 1
}
```

---

### `small_shelf`
**Name:** Toy Shelf  
**Description:** FURNITURE_DESC_SMALL_SHELF  
**Source:** `furniture_effects.gon`  

```
small_shelf { //frame 1086
    name FURNITURE_NAME_SMALL_SHELF
    desc FURNITURE_DESC_SMALL_SHELF
    
    Comfort 1
}
```

---

### `small_piggybank`
**Name:** Piggy Bank  
**Description:** FURNITURE_DESC_SMALL_PIGGYBANK  
**Source:** `furniture_effects.gon`  

```
small_piggybank { //frame 1087
    name FURNITURE_NAME_SMALL_PIGGYBANK
    desc FURNITURE_DESC_SMALL_PIGGYBANK
    
    Comfort 1
}
```

---

### `small_food_cupcake`
**Name:** Cupcake  
**Description:** FURNITURE_DESC_SMALL_FOOD_CUPCAKE  
**Source:** `furniture_effects.gon`  

```
small_food_cupcake { //frame 1088
    name FURNITURE_NAME_SMALL_FOOD_CUPCAKE
    desc FURNITURE_DESC_SMALL_FOOD_CUPCAKE
    
    Comfort 1
}
```

---

### `small_food_cupcake2`
**Name:** Chocolate Cupcake  
**Description:** FURNITURE_DESC_SMALL_FOOD_CUPCAKE2  
**Source:** `furniture_effects.gon`  

```
small_food_cupcake2 { //frame 1089
    name FURNITURE_NAME_SMALL_FOOD_CUPCAKE2
    desc FURNITURE_DESC_SMALL_FOOD_CUPCAKE2
    
    Comfort 1
}
```

---

### `small_mug2`
**Name:** Tall Mug  
**Description:** FURNITURE_DESC_SMALL_MUG2  
**Source:** `furniture_effects.gon`  

```
small_mug2 { //frame 1090
    name FURNITURE_NAME_SMALL_MUG2
    desc FURNITURE_DESC_SMALL_MUG2
    
    Comfort 1
}
```

---

### `small_electronics_joystick`
**Name:** Joystick  
**Description:** FURNITURE_DESC_SMALL_ELECTRONICS_JOYSTICK  
**Source:** `furniture_effects.gon`  

```
small_electronics_joystick { //frame 1091
    name FURNITURE_NAME_SMALL_ELECTRONICS_JOYSTICK
    desc FURNITURE_DESC_SMALL_ELECTRONICS_JOYSTICK
    
    Stimulation 1
}
```

---

### `small_bell`
**Name:** Ring Bell  
**Description:** FURNITURE_DESC_SMALL_BELL  
**Source:** `furniture_effects.gon`  

```
small_bell { //frame 1092
    name FURNITURE_NAME_SMALL_BELL
    desc FURNITURE_DESC_SMALL_BELL
    
    Stimulation 1
}
```

---

### `small_iron`
**Name:** Iron  
**Description:** FURNITURE_DESC_SMALL_IRON  
**Source:** `furniture_effects.gon`  

```
small_iron { //frame 1093
    name FURNITURE_NAME_SMALL_IRON
    desc FURNITURE_DESC_SMALL_IRON
    
    Comfort 1
}
```

---

### `small_snowglobe`
**Name:** Small Snowglobe  
**Description:** FURNITURE_DESC_SMALL_SNOWGLOBE  
**Source:** `furniture_effects.gon`  

```
small_snowglobe { //frame 1094
    name FURNITURE_NAME_SMALL_SNOWGLOBE
    desc FURNITURE_DESC_SMALL_SNOWGLOBE
    
    Comfort 1
}
```

---

### `small_shell`
**Name:** Conch Shell  
**Description:** FURNITURE_DESC_SMALL_SHELL  
**Source:** `furniture_effects.gon`  

```
small_shell { //frame 1095
    name FURNITURE_NAME_SMALL_SHELL
    desc FURNITURE_DESC_SMALL_SHELL
    
    Comfort 1
}
```

---

### `small_bigegg`
**Name:** Big Egg  
**Description:** FURNITURE_DESC_SMALL_BIGEGG  
**Source:** `furniture_effects.gon`  

```
small_bigegg { //frame 1096
    name FURNITURE_NAME_SMALL_BIGEGG
    desc FURNITURE_DESC_SMALL_BIGEGG
    
    Comfort 1
}
```

---

### `small_letterblock1`
**Name:** Letter Block  
**Description:** FURNITURE_DESC_SMALL_LETTERBLOCK1  
**Source:** `furniture_effects.gon`  

```
small_letterblock1 { //frame 1097
    name FURNITURE_NAME_SMALL_LETTERBLOCK1
    desc FURNITURE_DESC_SMALL_LETTERBLOCK1
    
    Comfort 1
}
```

---

### `small_letterblock2`
**Name:** Letter Block  
**Description:** FURNITURE_DESC_SMALL_LETTERBLOCK2  
**Source:** `furniture_effects.gon`  

```
small_letterblock2 { //frame 1098
    name FURNITURE_NAME_SMALL_LETTERBLOCK2
    desc FURNITURE_DESC_SMALL_LETTERBLOCK2
    
    Comfort 1
}
```

---

### `small_letterblock3`
**Name:** Letter Block  
**Description:** FURNITURE_DESC_SMALL_LETTERBLOCK3  
**Source:** `furniture_effects.gon`  

```
small_letterblock3 { //frame 1099
    name FURNITURE_NAME_SMALL_LETTERBLOCK3
    desc FURNITURE_DESC_SMALL_LETTERBLOCK3
    
    Comfort 1
}
```

---

### `small_letterblock4`
**Name:** Letter Block  
**Description:** FURNITURE_DESC_SMALL_LETTERBLOCK4  
**Source:** `furniture_effects.gon`  

```
small_letterblock4 { //frame 1100
    name FURNITURE_NAME_SMALL_LETTERBLOCK4
    desc FURNITURE_DESC_SMALL_LETTERBLOCK4
    
    Comfort 1
}
```

---

### `small_letterblock5`
**Name:** Letter Block  
**Description:** FURNITURE_DESC_SMALL_LETTERBLOCK5  
**Source:** `furniture_effects.gon`  

```
small_letterblock5 { //frame 1101
    name FURNITURE_NAME_SMALL_LETTERBLOCK5
    desc FURNITURE_DESC_SMALL_LETTERBLOCK5
    
    Comfort 1
}
```

---

### `small_letterblock6`
**Name:** Letter Block  
**Description:** FURNITURE_DESC_SMALL_LETTERBLOCK6  
**Source:** `furniture_effects.gon`  

```
small_letterblock6 { //frame 1102
    name FURNITURE_NAME_SMALL_LETTERBLOCK6
    desc FURNITURE_DESC_SMALL_LETTERBLOCK6
    
    Comfort 1
}
```

---

### `small_letterblock7`
**Name:** Letter Block  
**Description:** FURNITURE_DESC_SMALL_LETTERBLOCK7  
**Source:** `furniture_effects.gon`  

```
small_letterblock7 { //frame 1103
    name FURNITURE_NAME_SMALL_LETTERBLOCK7
    desc FURNITURE_DESC_SMALL_LETTERBLOCK7
    
    Comfort 1
}
```

---

### `small_letterblock8`
**Name:** Letter Block  
**Description:** FURNITURE_DESC_SMALL_LETTERBLOCK8  
**Source:** `furniture_effects.gon`  

```
small_letterblock8 { //frame 1104
    name FURNITURE_NAME_SMALL_LETTERBLOCK8
    desc FURNITURE_DESC_SMALL_LETTERBLOCK8
    
    Comfort 1
}
```

---

### `small_rubberduck`
**Name:** Rubber Duck  
**Description:** FURNITURE_DESC_SMALL_RUBBERDUCK  
**Source:** `furniture_effects.gon`  

```
small_rubberduck { //frame 1105
    name FURNITURE_NAME_SMALL_RUBBERDUCK
    desc FURNITURE_DESC_SMALL_RUBBERDUCK
    
    Comfort 1
}
```

---

### `small_wobblebird`
**Name:** Wobble Bird  
**Description:** FURNITURE_DESC_SMALL_WOBBLEBIRD  
**Source:** `furniture_effects.gon`  

```
small_wobblebird { //frame 1106
    name FURNITURE_NAME_SMALL_WOBBLEBIRD
    desc FURNITURE_DESC_SMALL_WOBBLEBIRD
    
    Comfort 1
}
```

---

### `small_90sphone`
**Name:** 90s Phone A  
**Description:** FURNITURE_DESC_SMALL_90SPHONE  
**Source:** `furniture_effects.gon`  

```
small_90sphone { //frame 1107
    name FURNITURE_NAME_SMALL_90SPHONE
    desc FURNITURE_DESC_SMALL_90SPHONE
    
    Comfort 1
}
```

---

### `small_90sphone2`
**Name:** 90s Phone B  
**Description:** FURNITURE_DESC_SMALL_90SPHONE2  
**Source:** `furniture_effects.gon`  

```
small_90sphone2 { //frame 1108
    name FURNITURE_NAME_SMALL_90SPHONE2
    desc FURNITURE_DESC_SMALL_90SPHONE2
    
    Comfort 1
}
```

---

### `small_knocker`
**Name:** Knocker  
**Description:** FURNITURE_DESC_SMALL_KNOCKER  
**Source:** `furniture_effects.gon`  

```
small_knocker { //frame 1109
    name FURNITURE_NAME_SMALL_KNOCKER
    desc FURNITURE_DESC_SMALL_KNOCKER
    
    Comfort 1
}
```

---

