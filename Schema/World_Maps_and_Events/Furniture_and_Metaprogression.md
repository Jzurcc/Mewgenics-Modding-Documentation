---
title: "Furniture & Metaprogression Schema"
description: "Placeable furniture and permanent upgrades."
---

# Furniture & Metaprogression Schema

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
| [`set`](../Reference_and_Meta/Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. | 985 | `80s`<br>`90s`<br>`AdvancedAlloy` |
| `Comfort` | Integer | The amount of comfort provided by the furniture piece to the room. | 406 | `-1`<br>`-2`<br>`-3` |
| `Appeal` | Integer | The amount of appeal provided by the furniture piece to the room. | 338 | `-1`<br>`-2`<br>`-4` |
| [`{Logic Keys}`](../Engine_Scripts_and_Logic/Engine_LogicKeys.md#valid-property-keys) | Variable | Placeholder for logic keys used within the Conditional_Shielded object; no specific examples provided. | 155 | Default<br>FormChange<br>Druid |
| `Stimulation` | Integer | The amount of stimulation provided by the furniture piece to the room. | 268 | `-1`<br>`-2`<br>`1` |
| `Health` | Integer | The amount of health provided by the furniture piece to the room. | 67 | `-1`<br>`-2`<br>`-5` |
| `Evolution` | Integer | The amount of evolution provided by the furniture piece to the room. | 53 | `1`<br>`2`<br>`4` |
| `special` | Boolean | An array or boolean indicating that an item or entry is a special container or category. | 29 | `[special]`<br>`true` |
| `can_be_rare` | Boolean | If false, this item cannot appear with a rare quality. | 10 | `false` |
| `BreedSuppression` | Integer | The amount of breeding suppression provided by the furniture piece. | 1 | `1` |
| `FightBonusRewards` | Integer | The number of bonus rewards earned from fights due to the furniture piece. | 1 | `1` |
| `FightRisk` | Integer | The increased risk level of fights triggered by the furniture piece. | 1 | `2` |
| `FoodStorage` | Integer | The amount of food storage capacity added by the furniture piece. | 1 | `40` |
| `removed` | Boolean | If true, this autofeeder item is disabled and not available. | 1 | `true` |

</details>


---