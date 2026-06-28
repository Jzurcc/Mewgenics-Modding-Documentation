# Enemies and Combat/Combat Rewards Directory

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

## File: `combat_reward_table.gon`

### `acts`
**Source:** `combat_reward_table.gon`  

```
acts {
	0 { //tutorial, everything hardcoded
	}

	1 { //alley and such
		food_bonus 1
		coins_bonus .5

		chapters {
			1 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [2 5]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [5 8]
					item_chance 1
					consumable_chance .5
				}
			}
			2 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [4 8]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [6 12]
					item_chance 1
					consumable_chance .5
				}
			}
			3 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
			4 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
		}
	}

	2 { //desert and such
		food_bonus 1.75
		coins_bonus .75

		chapters {
			1 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [2 5]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [5 8]
					item_chance 1
					consumable_chance .5
				}
			}
			2 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [4 8]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [6 12]
					item_chance 1
					consumable_chance .5
				}
			}
			3 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
			4 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
		}
	}

	3 { //lab and such
		food_bonus 2.5
		coins_bonus 1

		chapters {
			1 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [2 5]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [5 8]
					item_chance 1
					consumable_chance .5
				}
			}
			2 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [4 8]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [6 12]
					item_chance 1
					consumable_chance .5
				}
			}
			3 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
			4 {
				food_bonus 1 //food rewards get multiplied by this (quick way to "overall balance" an area)
				coins_bonus 1 //coin rewards get multiplied by this (quick way to "overall balance" an area)

				normal {
					coins [1 6]
					food [1 3]
					item_chance .25
					consumable_chance .25
				}
				hard {
					coins [1 6]
					food [4 7]
					item_chance .25
					consumable_chance .25
				}
				miniboss {
					coins [10 20]
					food [5 10]
					item_chance .5
					consumable_chance .3
				}
				boss {
					coins [10 20]
					food [10 15]
					item_chance 1
					consumable_chance .5
				}
			}
		}
	}
}
```

---

