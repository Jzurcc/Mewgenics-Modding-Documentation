---
title: "Furniture & Metaprogression Schema"
description: "Placeable furniture and permanent upgrades."
---

# Furniture & Metaprogression Schema


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

## Overview
> [!NOTE]
> This schema controls cosmetic and functional objects you can buy and place inside your house to grant global meta-progression bonuses.

## Usage Example
Here is a real example of this object being defined in the game's data:
```gon
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

## Associated Directory Files
To see extracted instances of this schema in the base game, refer to:
- [`Furniture_and_Metaprogression.md`](../../Directory/World_and_Events/Furniture_and_Metaprogression.md)

---



This document is an exhaustive, auto-generated dictionary of `.gon` properties relevant to this subsystem. While the overview above provides high-level context, you may still need to infer exact engine execution rules through testing or context clues.

## Furniture & Metaprogression

> **Associated Files:** `data/furniture_effects.gon`


### Object: `ROOT`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 634

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Comfort` | Integer | The amount of comfort provided by the furniture piece to the room. | 406 | `-1`<br>`-2`<br>`-3` |
| `Appeal` | Integer | The amount of appeal provided by the furniture piece to the room. | 338 | `-1`<br>`-2`<br>`-4` |
| `Stimulation` | Integer | The amount of stimulation provided by the furniture piece to the room. | 268 | `-1`<br>`-2`<br>`1` |
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 220 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `Health` | Integer | The amount of health provided by the furniture piece to the room. | 67 | `-1`<br>`-2`<br>`-5` |
| `Evolution` | Integer | The amount of evolution provided by the furniture piece to the room. | 53 | `1`<br>`2`<br>`4` |
| `special` | Boolean | An array or boolean indicating that an item or entry is a special container or category. | 10 | `[special]`<br>`true` |
| `can_be_rare` | Boolean | If false, this item cannot appear with a rare quality. | 10 | `false` |
| `BreedSuppression` | Integer | The amount of breeding suppression provided by the furniture piece. | 1 | `1` |
| `FightBonusRewards` | Integer | The number of bonus rewards earned from fights due to the furniture piece. | 1 | `1` |
| `FightRisk` | Integer | The increased risk level of fights triggered by the furniture piece. | 1 | `2` |
| `FoodStorage` | Integer | The amount of food storage capacity added by the furniture piece. | 1 | `40` |
| `removed` | Boolean | If true, this autofeeder item is disabled and not available. | 1 | `true` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 0 | Default<br>FormChange<br>Druid |
| [{Status and Passive Keys}](../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md) | Object | Inherits standard status effect and passive mechanics. | 0 | `{ . . . }` |

</details>


---