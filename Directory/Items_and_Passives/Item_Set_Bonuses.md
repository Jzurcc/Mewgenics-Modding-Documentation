# Items and Passives/Item Set Bonuses Directory

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

## File: `item_setbonuses.gon`

### `Scrap`
**Name:** Scrap Set Bonus!  
**Description:** +1 Thorns.  
**Source:** `item_setbonuses.gon`  

```
Scrap {
    name "SETBONUS_SCRAP_NAME"
    desc "SETBONUS_SCRAP_DESC"
    pieces_required 3

    shield 3
    passives {
        Thorns 1
    }
}
```

---

### `Leather`
**Name:** Leather Set Bonus!  
**Description:** SETBONUS_LEATHER_DESC  
**Source:** `item_setbonuses.gon`  

```
Leather {
    name "SETBONUS_LEATHER_NAME"
    desc "SETBONUS_LEATHER_DESC"
    pieces_required 3

    shield 3
}
```

---

### `Rag`
**Name:** Rags Set Bonus!  
**Description:** SETBONUS_RAG_DESC  
**Source:** `item_setbonuses.gon`  

```
Rag {
    name "SETBONUS_RAG_NAME"
    desc "SETBONUS_RAG_DESC"
    pieces_required 3

    spd 2
}
```

---

### `Rubber`
**Name:** Rubber Set Bonus!  
**Description:** +3 Knockback damage.  
**Source:** `item_setbonuses.gon`  

```
Rubber {
    name "SETBONUS_RUBBER_NAME"
    desc "SETBONUS_RUBBER_DESC"
    pieces_required 3

    passives {
        AddStatusToAllDamage {
            BonusKnockbackDamage 3
        }
    }

}
```

---

### `CatHide`
**Name:** Cathide Set Bonus!  
**Description:** 5% chance to spawn a Flea each turn.
Familiars have +1 Damage and +1 movement range.  
**Source:** `item_setbonuses.gon`  

```
CatHide {
    name "SETBONUS_CATHIDE_NAME"
    desc "SETBONUS_CATHIDE_DESC"
    pieces_required 3

    passives {
        SpawnEachTurn {
            chance 5%
            object CharmedFlea

            stack_key CATHIDE
        }

        GlobalFamiliarDamageBoost 1
        GlobalFamiliarMoveBoost 1
    }
}
```

---

### `Guts`
**Name:** Guts Set Bonus!  
**Description:** +1 Health Regen.  
**Source:** `item_setbonuses.gon`  

```
Guts {
    name "SETBONUS_GUTS_NAME"
    desc "SETBONUS_GUTS_DESC"
    pieces_required 3

    con 3
    passives {
        HealthRegenUp 1
    }
}
```

---

### `Bone`
**Name:** Bone Set Bonus!  
**Description:** Find a random common bone item at the end of each battle.  
**Source:** `item_setbonuses.gon`  

```
Bone {
    name "SETBONUS_BONE_NAME"
    desc "SETBONUS_BONE_DESC"
    pieces_required 3

    shield 4

    passives {
        StatusOnBattleEnd {
            FindItemFromPool common_bones
        }
    }
}
```

---

### `DirtClod`
**Name:** Dirt Clod Set Bonus!  
**Description:** Grow flowers under yourself at the end of each turn.  
**Source:** `item_setbonuses.gon`  

```
DirtClod {
    name "SETBONUS_DIRTCLOD_NAME"
    desc "SETBONUS_DIRTCLOD_DESC"
    pieces_required 3

    passives {
        FlowersOnEndTurn 1
    }
}
```

---

### `Barbed`
**Name:** Barbed Set Bonus!  
**Description:** +3 Thorns.  
**Source:** `item_setbonuses.gon`  

```
Barbed {
    name "SETBONUS_BARBED_NAME"
    desc "SETBONUS_BARBED_DESC"
    pieces_required 3

    con 2

    passives {
        Thorns 3
    }
}
```

---

### `Sludge`
**Name:** Sludge Set Bonus!  
**Description:** Gain +2 [img:shield] at the end of each turn.  
**Source:** `item_setbonuses.gon`  

```
Sludge {
    name "SETBONUS_SLUDGE_NAME"
    desc "SETBONUS_SLUDGE_DESC"
    pieces_required 3

    passives {
        StatusEachTurnEnd {
            Shield 2
        }
    }
}
```

---

### `Cool`
**Name:** Cool Set Bonus!  
**Description:** Cool Set Pieces are no longer Fragile.  
**Source:** `item_setbonuses.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_COOL`: "Cool {Catname}"

```
Cool {
    name "SETBONUS_COOL_NAME"
    desc "SETBONUS_COOL_DESC"
    pieces_required 3

    name_mod "CAT_NAME_MOD_COOL"

    lck 4
    passives {
        SetFragileImmune Cool
    }
}
```

---

### `Paper`
**Name:** Paper Set Bonus!  
**Description:** +1 Bleed Thorns. Paper Set Pieces are no longer Fragile nor Brittle.  
**Source:** `item_setbonuses.gon`  

```
Paper {
    name "SETBONUS_PAPER_NAME"
    desc "SETBONUS_PAPER_DESC"
    pieces_required 3

    passives {
        BleedThorns 1
        SetFragileImmune Paper
        SetBrittleImmune Paper
    }
}
```

---

### `Cardboard`
**Name:** Cardboard Set Bonus!  
**Description:** Cardboard Set Pieces are no longer Fragile.  
**Source:** `item_setbonuses.gon`  

```
Cardboard {
    name "SETBONUS_CARDBOARD_NAME"
    desc "SETBONUS_CARDBOARD_DESC"
    pieces_required 3

    shield 2

    passives {
        SetFragileImmune Cardboard
    }
}
```

---

### `Used`
**Name:** Used Set Bonus!  
**Description:** SETBONUS_USED_DESC  
**Source:** `item_setbonuses.gon`  

```
Used {
    name "SETBONUS_USED_NAME"
    desc "SETBONUS_USED_DESC"
    pieces_required 3

    con 1
}
```

---

### `Wood`
**Name:** Wood Set Bonus!  
**Description:** +1 Brace. Wood Set Pieces are no longer Fragile.  
**Source:** `item_setbonuses.gon`  

```
Wood {
    name "SETBONUS_WOOD_NAME"
    desc "SETBONUS_WOOD_DESC"
    pieces_required 3

    passives {
        SetFragileImmune Wood
        Brace 1
    }
}
```

---

### `Recycled`
**Name:** Recycled Set Bonus!  
**Description:** Also find a rare item when a recycled set piece breaks.  
**Source:** `item_setbonuses.gon`  

```
Recycled {
    name "SETBONUS_RECYCLED_NAME"
    desc "SETBONUS_RECYCLED_DESC"
    pieces_required 3

    passives {
        StatusOnSetPieceBreak {
            set Recycled
            FindItemFromPool rare
        }
    }
}
```

---

### `Rotten`
**Name:** Rotten Set Bonus!  
**Description:** All Bugs and Maggots you spawn are upgraded to champions.  
**Source:** `item_setbonuses.gon`  

```
Rotten {
    name "SETBONUS_ROTTEN_NAME"
    desc "SETBONUS_ROTTEN_DESC"
    pieces_required 3

    passives {
        UpgradeTaggedSpawnsToChampions bug
        UpgradeTaggedSpawnsToChampions worm
    }
}
```

---

### `JankAlloy`
**Name:** Jank Alloy Set Bonus!  
**Description:** Jank Alloy Set Pieces are no longer Brittle.  
**Source:** `item_setbonuses.gon`  

```
JankAlloy {
    name "SETBONUS_JANKALLOY_NAME"
    desc "SETBONUS_JANKALLOY_DESC"
    pieces_required 3

    passives {
        SetBrittleImmune JankAlloy
    }
}
```

---

### `Alloy`
**Name:** Alloy Set Bonus!  
**Description:** Alloy Set Pieces are no longer Brittle.  
**Source:** `item_setbonuses.gon`  

```
Alloy {
    name "SETBONUS_ALLOY_NAME"
    desc "SETBONUS_ALLOY_DESC"
    pieces_required 3

    passives {
        SetBrittleImmune Alloy
    }
}
```

---

### `AdvancedAlloy`
**Name:** Advanced Alloy Set Bonus!  
**Description:** Advanced Alloy Set Pieces are no longer Brittle.  
**Source:** `item_setbonuses.gon`  

```
AdvancedAlloy {
    name "SETBONUS_ADVALLOY_NAME"
    desc "SETBONUS_ADVALLOY_DESC"
    pieces_required 3

    passives {
        SetBrittleImmune AdvancedAlloy
    }
}
```

---

### `EliteAlloy`
**Name:** Elite Alloy Set Bonus!  
**Description:** Elite Alloy Set Pieces are no longer Brittle.  
**Source:** `item_setbonuses.gon`  

```
EliteAlloy {
    name "SETBONUS_ELITEALLOY_NAME"
    desc "SETBONUS_ELITEALLOY_DESC"
    pieces_required 3

    passives {
        SetBrittleImmune EliteAlloy
    }
}
```

---

### `Twine`
**Name:** Twine Set Bonus!  
**Description:** +10% Dodge Chance.
Bruise units that contact you.  
**Source:** `item_setbonuses.gon`  

```
Twine {
    name "SETBONUS_TWINE_NAME"
    desc "SETBONUS_TWINE_DESC"
    pieces_required 3

    passives {
        ArmorDodgeChance 10%
        MeleeRevengeDamage {
            damage 0
            effects {
                Bruise 1
            }
        }
    }
}
```

---

### `Rock`
**Name:** Rock Set Bonus!  
**Description:** +1 Brace. Spawn a pet rock familiar whenever you lose [img:shield].  
**Source:** `item_setbonuses.gon`  

```
Rock {
    name "SETBONUS_ROCK_NAME"
    desc "SETBONUS_ROCK_DESC"
    pieces_required 3

    passives {
        Brace 1
		SpawnThingOnDamage {
            object AnimatedSmallRock
            shield_only true
        }
    }
}
```

---

### `Miner`
**Name:** Miner Set Bonus!  
**Description:** 2 more pickups spawn in each battle.  
**Source:** `item_setbonuses.gon`  

```
Miner {
    name "SETBONUS_MINER_NAME"
    desc "SETBONUS_MINER_DESC"
    pieces_required 3

    lck 3
    passives {
        SpawnOnBattleStartRandomEmptyTile {
            object RandomPickup
            number 2
        }
    }
}
```

---

### `Gemstone`
**Name:** Gemstone Set Bonus!  
**Description:** Gain +3 [img:shield] at the end of each turn.  
**Source:** `item_setbonuses.gon`  

```
Gemstone {
    name "SETBONUS_GEMSTONE_NAME"
    desc "SETBONUS_GEMSTONE_DESC"
    pieces_required 3

    cha 1
    passives {
        StatusEachTurnEnd {
            Shield 3
        }
    }
}
```

---

### `Veiny`
**Name:** Veiny Set Bonus!  
**Description:** Your basic attack inflicts Bleed. Whenever you inflict Bleed, trigger Bleed damage immediately.  
**Source:** `item_setbonuses.gon`  

```
Veiny {
    name "SETBONUS_VEINY_NAME"
    desc "SETBONUS_VEINY_DESC"
    pieces_required 3

    passives {
        AddStatusToBasicAttack {
            Bleed 1
        }
        TriggerBleedOnBleed 1
    }
}
```

---

### `Gimp`
**Name:** Gimp Set Bonus!  
**Description:** Gain +1 Random Stat Up whenever you take damage.  
**Source:** `item_setbonuses.gon`  

```
Gimp {
    name "SETBONUS_GIMP_NAME"
    desc "SETBONUS_GIMP_DESC"
    pieces_required 3

    passives {
        StatusOnTookDamage {
            RandomStatUp 1
        }
    }
}
```

---

### `Bionic`
**Name:** Bionic Set Bonus!  
**Description:** Your movement action becomes an infinite range Teleport.
Bionic Set Pieces are no longer Fragile.  
**Source:** `item_setbonuses.gon`  

```
Bionic {
    name "SETBONUS_BIONIC_NAME"
    desc "SETBONUS_BIONIC_DESC"
    pieces_required 3

    passives {
        SetFragileImmune Bionic
        ReplaceBasicMove MaxTeleport
    }
}
```

---

### `Cyborg`
**Name:** Cyborg Set Bonus!  
**Description:** Take an AI controlled bonus turn at the end of the first round.  
**Source:** `item_setbonuses.gon`  

```
Cyborg {
    name "SETBONUS_CYBORG_NAME"
    desc "SETBONUS_CYBORG_DESC"
    pieces_required 3

    passives {
        CyborgTurns {
            stacks 1
            TakeBonusTurnWithAIControl {
                end_of_round true
                include_spells true
            }
        }
        Robot {
            allow_energize_self true
        }
    }
}
```

---

### `Lucky`
**Name:** Lucky Set Bonus!  
**Description:** Spawn 5-10 extra coins on each map.
Lucky Set Pieces are no longer Fragile.  
**Source:** `item_setbonuses.gon`  

```
Lucky {
    name "SETBONUS_LUCKY_NAME"
    desc "SETBONUS_LUCKY_DESC"
    pieces_required 3

    lck 1
    passives {
        SetFragileImmune Lucky
        SpawnOnBattleStartRandomEmptyTile {
            object Coin
            number [5 10]
        }
    }
}
```

---

### `Fly`
**Name:** Fly Set Bonus!  
**Description:** Flying. You do not take extra damage from backstabs.
50% Chance to spawn a Fly each turn.  
**Source:** `item_setbonuses.gon`  

```
Fly {
    name "SETBONUS_FLY_NAME"
    desc "SETBONUS_FLY_DESC"
    pieces_required 3

    passives {
        BackstabImmunity 1
        Flying 1

        SpawnEachTurn {
            chance 50%
            object CharmedFly
        }
    }
}
```

---

### `Amoeba`
**Name:** Amoeba Set Bonus!  
**Description:** Permanent Madness.  
**Source:** `item_setbonuses.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_AMOEBA`: "{Catname}?|1"

```
Amoeba {
    name "SETBONUS_AMOEBA_NAME"
    desc "SETBONUS_AMOEBA_DESC"
    pieces_required 3

    name_mod "CAT_NAME_MOD_AMOEBA"

    passives {
        PermanentMadness 1
    }
}
```

---

### `Mage`
**Name:** Mage Set Bonus!  
**Description:** +5 starting mana.  
**Source:** `item_setbonuses.gon`  

```
Mage {
    name "SETBONUS_MAGE_NAME"
    desc "SETBONUS_MAGE_DESC"
    pieces_required 3
    
    passives {
        AddStartingMana 5
    }
}
```

---

### `Thief`
**Name:** Thief Set Bonus!  
**Description:** +5% Dodge Chance and +5% Crit Chance.  
**Source:** `item_setbonuses.gon`  

```
Thief {
    name "SETBONUS_THIEF_NAME"
    desc "SETBONUS_THIEF_DESC"
    pieces_required 3
    
    passives {
        ArmorDodgeChance 5%
        CritChanceUp 5
    }
}
```

---

### `Fighter`
**Name:** Fighter Set Bonus!  
**Description:** +15% chance to refresh your basic attack, movement, weapon and trinket actions when you get a kill.  
**Source:** `item_setbonuses.gon`  

```
Fighter {
    name "SETBONUS_FIGHTER_NAME"
    desc "SETBONUS_FIGHTER_DESC"
    pieces_required 3
    
    shield 4

    passives {
        StatusOnKill {
            Conditional_GoodRoll {
                odds 15%
                ForceUseAbility_NonStack Endeavor_Auto
            }
        }
    }
}
```

---

### `Cleric`
**Name:** Cleric Set Bonus!  
**Description:** If an attack would down you, instead lower your HP to 1. While at 1 HP, this has no effect.  
**Source:** `item_setbonuses.gon`  

```
Cleric {
    name "SETBONUS_CLERIC_NAME"
    desc "SETBONUS_CLERIC_DESC"
    pieces_required 3
    
    passives {
        PassiveAtHealthThreshold {
            threshold 1
            mode greater
            
            passives {
                DeathRattleRevive DoNothing
            }
        }
    }
}
```

---

### `Tank`
**Name:** Tank Set Bonus!  
**Description:** +1 Knockback damage.  
**Source:** `item_setbonuses.gon`  

```
Tank {
    name "SETBONUS_TANK_NAME"
    desc "SETBONUS_TANK_DESC"
    pieces_required 3
    
    passives {
        AddKnockbackDamage 1
    }
}
```

---

### `Hunter`
**Name:** Hunter Set Bonus!  
**Description:** +50% Crit Chance while standing in tall grass.  
**Source:** `item_setbonuses.gon`  

```
Hunter {
    name "SETBONUS_HUNTER_NAME"
    desc "SETBONUS_HUNTER_DESC"
    pieces_required 3
    
    passives {
        PassiveWhenOnTile {
            tile [TallGrassTile TallFlowerTile]
            passives {
                CritChanceUp 50
            }
        }
    }
}
```

---

### `Psychic`
**Name:** Psychic Set Bonus!  
**Description:** When you gain excess mana, reduce the cost of all your spells by that amount until you cast them.  
**Source:** `item_setbonuses.gon`  

```
Psychic {
    name "SETBONUS_PSYCHIC_NAME"
    desc "SETBONUS_PSYCHIC_DESC"
    pieces_required 3
    
    passives {
        OverManaReducesManaCosts 1
    }
}
```

---

### `Necromancer`
**Name:** Necromancer Set Bonus!  
**Description:** When downed, spawn a shadow copy of yourself that fades away after one turn.  
**Source:** `item_setbonuses.gon`  

```
Necromancer {
    name "SETBONUS_NECROMANCER_NAME"
    desc "SETBONUS_NECROMANCER_DESC"
    pieces_required 3
    
    passives {
        SpawnCatCopyWhenDowned {
            object PlayerCat_NecroShade
            prevent_chain_tag necroset_shade
        }
    }
}
```

---

### `Monk`
**Name:** Monk Set Bonus!  
**Description:** Gain +2 [img:shield] at the end of each turn.  
**Source:** `item_setbonuses.gon`  

```
Monk {
    name "SETBONUS_MONK_NAME"
    desc "SETBONUS_MONK_DESC"
    pieces_required 3
    
    passives {
        StatusEachTurnEnd {
			Shield 2
		}
    }
}
```

---

### `Tinkerer`
**Name:** Tinkerer Set Bonus!  
**Description:** Spawn 4 Scrap pickups at the start of each battle.  
**Source:** `item_setbonuses.gon`  

```
Tinkerer {
    name "SETBONUS_TINKERER_NAME"
    desc "SETBONUS_TINKERER_DESC"
    pieces_required 3
    
	passives {
		SpawnOnBattleStart {
			object Scrap
			number 4
		}
	}	
}
```

---

### `Butcher`
**Name:** Butcher Set Bonus!  
**Description:** Food and scrap pickups you spawn are bigger.  
**Source:** `item_setbonuses.gon`  

```
Butcher {
    name "SETBONUS_BUTCHER_NAME"
    desc "SETBONUS_BUTCHER_DESC"
    pieces_required 3
    
	passives {
		UpgradeSpawnedPickups 1
	}
}
```

---

### `Druid`
**Name:** Druid Set Bonus!  
**Description:** Your Familiars gain +4 HP and +1 Damage.  
**Source:** `item_setbonuses.gon`  

```
Druid {
    name "SETBONUS_DRUID_NAME"
    desc "SETBONUS_DRUID_DESC"
    pieces_required 3
    
    passives {
		AddPassivesToMinions {
            DamageUp 1
            AddMaxHealth 4
            HealthGain 4
		}
    }
}
```

---

### `Collarless`
**Name:** Collarless Set Bonus!  
**Description:** Collarless spells cost -1 mana to cast.  
**Source:** `item_setbonuses.gon`  

```
Collarless {
    name "SETBONUS_COLLARLESS_NAME"
    desc "SETBONUS_COLLARLESS_DESC"
    pieces_required 3

    passives {
        ClassManaCostReduction {
            class Colorless
            reduction 1
        }
    }
}
```

---

### `Grub`
**Name:** Grub Set Bonus!  
**Description:** Grubs spawned by items gain +5 HP.  
**Source:** `item_setbonuses.gon`  

```
Grub {
    name "SETBONUS_GRUB_NAME"
    desc "SETBONUS_GRUB_DESC"
    pieces_required 3
    
    passives {
        AddPassivesToMinions {
            tag_filter grub_familiar
            Buddy spawner
            ReturnBoundItemOnBattleEnd 1
            DamageUp 1
            AddMaxHealth 5
            HealthGain 5 //fill up the blank max health
        }
    }
}
```

---

### `Fecal`
**Name:** Fecal Set Bonus!  
**Description:** Poisonous 1.
Your basic attack inflicts Poison.  
**Source:** `item_setbonuses.gon`  

```
Fecal {
    name "SETBONUS_FECAL_NAME"
    desc "SETBONUS_FECAL_DESC"
    pieces_required 3
    
    passives {
        PoisonThorns 1
        AddStatusToBasicAttack {
            Poison 1
        }
    }
}
```

---

### `Meat`
**Name:** Meat Set Bonus!  
**Description:** +1 Damage.
Gain +1 Damage when you get a kill.
After three kills, gains +2 [img:con], +4 Health Regen and Madness for the rest of the battle.  
**Source:** `item_setbonuses.gon`  

```
Meat {
    name "SETBONUS_MEAT_NAME"
    desc "SETBONUS_MEAT_DESC"
    pieces_required 3
    
    passives {
        DamageUp 1
        StatusOnKillEnemy {
            DamageUp 1
        }
        PassiveAfterXKills {
            stacks 3

            passives {
                AddConstitution 2
                HealthRegenUp 4
                PermanentMadness 1
            }
        }
    }
}
```

---

### `Leafy`
**Name:** Leafy Set Bonus!  
**Description:** If you end your turn with unused movement actions, heal 3 HP and gain +3 Charge.  
**Source:** `item_setbonuses.gon`  

```
Leafy {
    name "SETBONUS_LEAFY_NAME"
    desc "SETBONUS_LEAFY_DESC"
    pieces_required 3
    
    passives {
        StatusIfUnusedMovePoints {
            HealthGain 3
            Charge 3
        }
    }
}
```

---

### `Cactus`
**Name:** Cactus Set Bonus!  
**Description:** +2 Thorns.
Whenever any Cactus armor breaks, increase all your stats by 1, permanently.  
**Source:** `item_setbonuses.gon`  

```
Cactus {
    name "SETBONUS_CACTUS_NAME"
    desc "SETBONUS_CACTUS_DESC"
    pieces_required 3
    
    passives {
        Thorns 2
        StatusOnSetPieceBreak {
            PermanentCharisma 1
            PermanentDexterity 1
            PermanentIntelligence 1
            PermanentLuck 1
            PermanentSpeed 1
            PermanentStrength 1
            PermanentConstitution 1
        }
    }
}
```

---

### `Mummy`
**Name:** Mummy Set Bonus!  
**Description:** When downed, inflict Rot 1 and Weakness 1 on all enemies.
When downed, revive with +30% HP at the end of the round.  
**Source:** `item_setbonuses.gon`  

```
Mummy {
    name "SETBONUS_MUMMY_NAME"
    desc "SETBONUS_MUMMY_DESC"
    pieces_required 3
    
    passives {
        DeathRattle {
            pop_corpse false
            ability set_MummySetCurse
        }
        DelayedAutoRevive {
            rounds 1
            health 30%
        }
    }
}
```

---

### `Man`
**Name:** Man Set Bonus!  
**Description:** Gain 1-9 coins at the end of each battle.  
**Source:** `item_setbonuses.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_MAN`: "Mr. {Catname}|1"

```
Man {
    name "SETBONUS_MAN_NAME"
    desc "SETBONUS_MAN_DESC"
    pieces_required 3

    name_mod "CAT_NAME_MOD_MAN"
    
    passives {
        StatusOnBattleEnd {
            GainCoinsRange {
                min 1
                max 9
            }
        }
    }
}
```

---

### `Flower`
**Name:** Flower Set Bonus!  
**Description:** Enemies have a 10% chance to become Entangled when walking through flower tiles.  
**Source:** `item_setbonuses.gon`  

```
Flower {
    name "SETBONUS_FLOWER_NAME"
    desc "SETBONUS_FLOWER_DESC"
    pieces_required 3
    
    passives {
        GlobalFlowerTrapperAura {
            Tangled [1, .1]
        }
    }
}
```

---

### `HumanFlesh`
**Name:** Human Flesh Set Bonus!  
**Description:** +50% Crit Chance on humanoid enemies.
When downed, inflict Fear 2 on all enemies.  
**Source:** `item_setbonuses.gon`  

```
HumanFlesh {
    name "SETBONUS_HUMANFLESH_NAME"
    desc "SETBONUS_HUMANFLESH_DESC"
    pieces_required 3
    
    passives {
        DeathRattle {
            pop_corpse false
            ability set_HumanFleshSetCurse
        }
        AddStatusToAllDamage {
            Conditional_HasTag {
                tag humanoid
                BonusCritChance 50
            }
        }
    }
}
```

---

### `Tentacle`
**Name:** Tentacle Set Bonus!  
**Description:** Cleanse all your debuffs at the end of each turn.  
**Source:** `item_setbonuses.gon`  

```
Tentacle {
    name "SETBONUS_TENTACLE_NAME"
    desc "SETBONUS_TENTACLE_DESC"
    pieces_required 3
    
    passives {
        StatusEachTurnEnd {
            Conditional_HasCleansableDebuffs {
                VisualFX Cleanse
            }
            Cleanse 0
        }
    }
}
```

---

### `Obelisk`
**Name:** Obelisk Set Bonus!  
**Description:** If you end your turn with unused movement actions, gain +1 [img:divineshield].  
**Source:** `item_setbonuses.gon`  

```
Obelisk {
    name "SETBONUS_OBELISK_NAME"
    desc "SETBONUS_OBELISK_DESC"
    pieces_required 3
    
    divine_shield 1

    passives {
        StatusIfUnusedMovePoints {
            DivineShield 1
        }
    }
}
```

---

### `Experimental`
**Name:** Experimental Set Bonus!  
**Description:** Find a pill at the end of each battle.
Whenever you eat a pill, gain a random stat and lose another random stat, permanently.  
**Source:** `item_setbonuses.gon`  

```
Experimental {
    name "SETBONUS_EXPERIMENTAL_NAME"
    desc "SETBONUS_EXPERIMENTAL_DESC"
    pieces_required 3
    
    passives {
        FindExtraItemFromPoolOnBattleEnd pills
        StatusOnEatPill {
            RandomPermanentStatsDistinct {
                stats [1 -1]
            }
        }
    }
}
```

---

### `Rocky`
**Name:** Rocky Set Bonus!  
**Description:** Spawn a pet rock familiar whenever you lose [img:shield].
Broken Rocky equipment pieces have a 75% chance of being recovered at the end of the battle.  
**Source:** `item_setbonuses.gon`  

```
Rocky {
    name "SETBONUS_ROCKY_NAME"
    desc "SETBONUS_ROCKY_DESC"
    pieces_required 3
    
    passives {
        RockyArmorSalvage .75
        SpawnThingOnDamage {
            object AnimatedSmallRock
            shield_only true
        }
    }
}
```

---

### `Space`
**Name:** Space Set Bonus!  
**Description:** Your movement action is Jump. Units you land on take damage.  
**Source:** `item_setbonuses.gon`  

```
Space {
    name "SETBONUS_SPACE_NAME"
    desc "SETBONUS_SPACE_DESC"
    pieces_required 3
    
    passives {
        ReplaceBasicMove set_SpaceArmorJump
    }
}
```

---

### `Planet`
**Name:** Planet Set Bonus!  
**Description:** Flying. Inflict Bruise 1 on units you make contact with.
Pull every unit within 2 tiles toward you at the end of each round.  
**Source:** `item_setbonuses.gon`  

```
Planet {
    name "SETBONUS_PLANET_NAME"
    desc "SETBONUS_PLANET_DESC"
    pieces_required 3
    
    passives {
        MeleeRevengeDamage {
            effects {
                Bruise 1
            }
        }
        Flying 1
        AutocastEachRound {
            ability set_PlanetSetGravity
            even_if_stunned true
        }
    }
}
```

---

### `Debris`
**Name:** Debris Set Bonus!  
**Description:** Your basic attack deals electric damage and has a +10% chance to Stun.  
**Source:** `item_setbonuses.gon`  

```
Debris {
    name "SETBONUS_DEBRIS_NAME"
    desc "SETBONUS_DEBRIS_DESC"
    pieces_required 3
    
    passives {
        AddElementsToBasicAttack Electric
        AddStatusToBasicAttack {
            Stun [1 .1]
        }
    }
}
```

---

### `DryBone`
**Name:** Dry Bone Set Bonus!  
**Description:** Find a bone club at the end of each battle.  
**Source:** `item_setbonuses.gon`  

```
DryBone {
    name "SETBONUS_DRYBONE_NAME"
    desc "SETBONUS_DRYBONE_DESC"
    pieces_required 3
    
    passives {
        StatusOnBattleEnd {
            FindItem BoneClub
        }
    }
}
```

---

### `Molten`
**Name:** Molten Set Bonus!  
**Description:** Fire immunity.  
**Source:** `item_setbonuses.gon`  

```
Molten {
    name "SETBONUS_MOLTEN_NAME"
    desc "SETBONUS_MOLTEN_DESC"
    pieces_required 3
    
    passives {
		InnateElement Fire
		ElementImmune Fire
		StatusImmunity [Burn]
    }
}
```

---

### `Mother`
**Name:** Mother Set Bonus!  
**Description:** Familiars you spawn gain +2 Damage and +2 HP.  
**Source:** `item_setbonuses.gon`  

```
Mother {
    name "SETBONUS_MOTHER_NAME"
    desc "SETBONUS_MOTHER_DESC"
    pieces_required 3
    
    passives {
		AddPassivesToMinions {
		    DamageUp 2
		    AddMaxHealth 2
		    HealthGain 2
		}
    }
}
```

---

### `Feathered`
**Name:** Feathered Set Bonus!  
**Description:** Flying.  
**Source:** `item_setbonuses.gon`  

```
Feathered {
    name "SETBONUS_FEATHERED_NAME"
    desc "SETBONUS_FEATHERED_DESC"
    pieces_required 3
	
	spd 2
    
    passives {
		Flying 1
    }
}
```

---

### `Copycat`
**Name:** Copycat Set Bonus!  
**Description:** Copies your trinket's passive effects.  
**Source:** `item_setbonuses.gon`  

```
Copycat {
    name "SETBONUS_COPYCAT_NAME"
    desc "SETBONUS_COPYCAT_DESC"
    pieces_required 3
    
    passives {
        TrinketPassiveMultiplierBonus 1
    }
}
```

---

### `Transmitter`
**Name:** Transmitter Set Bonus!  
**Description:** All allies gain +1 [img:int] and +1 [img:lck].  
**Source:** `item_setbonuses.gon`  

```
Transmitter {
    name "SETBONUS_TRANSMITTER_NAME"
    desc "SETBONUS_TRANSMITTER_DESC"
    pieces_required 3
    
    int -2

    passives {
        StatusAlliesOnBattleStart {
            IntelligenceUp 1
            LuckUp 1
        }
    }
}
```

---

### `Thrumming`
**Name:** Thrumming Set Bonus!  
**Description:** If you end your turn without using your basic attack, movement action, or casting a spell, gain All Stats Up.  
**Source:** `item_setbonuses.gon`  

```
Thrumming {
    name "SETBONUS_THRUMMING_NAME"
    desc "SETBONUS_THRUMMING_DESC"
    pieces_required 3
    
    passives {
        StatusOnTurnEndIfDidntCastAbilityTypes {
            type [attack move spell]
            AllStatsUp 1
        }
    }
}
```

---

### `Witch`
**Name:** Witch Set Bonus!  
**Description:** Your movement action becomes a Jump with infinite range.
Your tile-targeted spells have infinite range.  
**Source:** `item_setbonuses.gon`  

```
Witch {
    name "SETBONUS_WITCH_NAME"
    desc "SETBONUS_WITCH_DESC"
    pieces_required 3

    passives {
        ReplaceBasicMove set_WitchJump
        IncreaseSpellRange 20
    }
}
```

---

### `Stunning`
**Name:** Stunning Set Bonus!  
**Description:** Your weapon and trinket's passive and active effects are tripled.  
**Source:** `item_setbonuses.gon`  

```
Stunning {
    name "SETBONUS_STUNNING_NAME"
    desc "SETBONUS_STUNNING_DESC"
    pieces_required 3

    passives {
        TrinketPassiveMultiplierBonus 2
        TrinketActiveEffectsMultiplierBonus 2
        WeaponPassiveMultiplierBonus 2
        WeaponActiveEffectsMultiplierBonus 2
    }
}
```

---

### `Superhero`
**Name:** Superhero Set Bonus!  
**Description:** The first spell you cast each turn inflicts Webbed.  
**Source:** `item_setbonuses.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_SUPER`: "Super-{Catname}"

```
Superhero {
    name "SETBONUS_SUPERHERO_NAME"
    desc "SETBONUS_SUPERHERO_DESC"
    pieces_required 3

    name_mod "CAT_NAME_MOD_SUPER"

    passives {
        AddStatusToFirstSpellEachTurn {
            Conditional_IsSelf {}
            Else {
                Webbed 1
            }
        }
    }
}
```

---

### `Lead`
**Name:** Lead Set Bonus!  
**Description:** Trample 9.  
**Source:** `item_setbonuses.gon`  

```
Lead {
    name "SETBONUS_LEAD_NAME"
    desc "SETBONUS_LEAD_DESC"
    pieces_required 3

    shield 4
    spd -1

    passives {
        Trample 9
    }
}
```

---

### `Baby`
**Name:** Baby Set Bonus!  
**Description:** Start battle with a baby version of yourself.  
**Source:** `item_setbonuses.gon`  

```
Baby {
    name "SETBONUS_BABY_NAME"
    desc "SETBONUS_BABY_DESC"
    pieces_required 3

	passives {
		SpawnCatCopyOnBattleStart {
			object PlayerCat_MiniMiniMe
			prevent_chain_tag minime_clone
		}
	}
}
```

---

### `Ninja`
**Name:** Ninja Set Bonus!  
**Description:** Start battle with a bonus attack.  
**Source:** `item_setbonuses.gon`  

```
Ninja {
    name "SETBONUS_NINJA_NAME"
    desc "SETBONUS_NINJA_DESC"
    pieces_required 3

    passives {
        Quivered 1
    }
}
```

---

### `Prowler`
**Name:** Prowler Set Bonus!  
**Description:** Backstabs are always critical.  
**Source:** `item_setbonuses.gon`  

```
Prowler {
    name "SETBONUS_PROWLER_NAME"
    desc "SETBONUS_PROWLER_DESC"
    pieces_required 3

	passives {
		BackstabCritChance 1
	}
}
```

---

### `Godhead`
**Name:** Godhead Set Bonus!  
**Description:** Eternal Life  
**Source:** `item_setbonuses.gon`  

```
Godhead {
    name "SETBONUS_GODHEAD_NAME"
    desc "SETBONUS_GODHEAD_DESC"
    pieces_required 3

    passives {
		ChanceToRevive {
			stacks 100
			health 50%
		}
    }
}
```

---

### `Hippie`
**Name:** Hippie Set Bonus!  
**Description:** Spawn 5 Catnip pickups at the start of each battle.  
**Source:** `item_setbonuses.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_HIPPIE`: "{Catname} Moonbeam"

```
Hippie {
    name "SETBONUS_HIPPIE_NAME"
    desc "SETBONUS_HIPPIE_DESC"
    pieces_required 3

    name_mod "CAT_NAME_MOD_HIPPIE"

	passives {
		SpawnOnBattleStart {
			object Catnip
			number 5
		}
	}	
}
```

---

### `Parasite`
**Name:** Parasite Set Bonus!  
**Description:** At the end of each battle, lose a random stat permanently and gain a random mutation.  
**Source:** `item_setbonuses.gon`  

```
Parasite {
    name "SETBONUS_PARASITE_NAME"
    desc "SETBONUS_PARASITE_DESC"
    pieces_required 3

	passives {
        StatusOnBattleEnd {
            even_if_dead true
            
            RandomPermanentStat -1
            RandomMutation 1
        }
	}	
}
```

---

### `Brick`
**Name:** Brick Set Bonus!  
**Description:** Knockback immunity.  
**Source:** `item_setbonuses.gon`  

```
Brick {
    name "SETBONUS_BRICK_NAME"
    desc "SETBONUS_BRICK_DESC"
    pieces_required 3
	
	shield 4

	passives {
		KnockbackImmunity 1
	}
}
```

---

### `Slimy`
**Name:** Slimy Set Bonus!  
**Description:** Poisonous 2.  
**Source:** `item_setbonuses.gon`  

```
Slimy {
    name "SETBONUS_SLIMY_NAME"
    desc "SETBONUS_SLIMY_DESC"
    pieces_required 3

	passives {
		PoisonThorns 2
	}
}
```

---

### `Rat`
**Name:** Rat Set Bonus!  
**Description:** Start battle with 2 Charmed Rats.  
**Source:** `item_setbonuses.gon`  

```
Rat {
    name "SETBONUS_RAT_NAME"
    desc "SETBONUS_RAT_DESC"
    pieces_required 3
	
	passives {
		SpawnOnBattleStart {
			object CharmedRat 
			number 2
		}
	}
}
```

---

### `Carapace`
**Name:** Carapace Set Bonus!  
**Description:** Gain 3 random stat ups at the end of your turn.  
**Source:** `item_setbonuses.gon`  

```
Carapace {
    name "SETBONUS_CARAPACE_NAME"
    desc "SETBONUS_CARAPACE_DESC"
    pieces_required 3
	
	passives {
		StatusEachTurnEnd {
			RandomStatUp 3
		}
	}
}
```

---

### `Radioactive`
**Name:** Radioactive Set Bonus!  
**Description:** Gain a random mutation at the end of each battle.
Explode when downed. This explosion doesn't damage you.  
**Source:** `item_setbonuses.gon`  

```
Radioactive {
    name "SETBONUS_RADIOACTIVE_NAME"
    desc "SETBONUS_RADIOACTIVE_DESC"
    pieces_required 3

	passives {
		StatusOnBattleEnd {
			RandomMutation 1
		}
        DeathRattle {
            pop_corpse false
            ability MiniNukeExplodey
        }
	}
}
```

---

### `Nurse`
**Name:** Nurse Set Bonus!  
**Description:** Your basic attack becomes holy and can heal allies.  
**Source:** `item_setbonuses.gon`  

```
Nurse {
    name "SETBONUS_NURSE_NAME"
    desc "SETBONUS_NURSE_DESC"
    pieces_required 3

	passives {
        AddElementsToBasicAttack Holy
        AddStatusToBasicAttack {
            DamageOrHealConditionally 1
        }
	}
}
```

---

### `Hybrid`
**Name:** Hybrid Set Bonus!  
**Description:** Bruise 1. Poison 1. Bleed 1.
The first spell you cast each turn is cast twice.  
**Source:** `item_setbonuses.gon`  

```
Hybrid {
    name "SETBONUS_HYBRID_NAME"
    desc "SETBONUS_HYBRID_DESC"
    pieces_required 3

	passives {
		Poison 1
		Bleed 1
		Bruise 1
        DoubleCastSpellsEachTurn_Status 1
	}
}
```

---

### `Fatty`
**Name:** Fatty Set Bonus!  
**Description:** SETBONUS_FATTY_DESC  
**Source:** `item_setbonuses.gon`  

```
Fatty {
    name "SETBONUS_FATTY_NAME"
    desc "SETBONUS_FATTY_DESC"
    pieces_required 3

	con 3
	
}
```

---

### `Medical`
**Name:** Medical Set Bonus!  
**Description:** You have +1 Health Regen for each disorder you have.  
**Source:** `item_setbonuses.gon`  

```
Medical {
    name "SETBONUS_MEDICAL_NAME"
    desc "SETBONUS_MEDICAL_DESC"
    pieces_required 3

	passives {
        BonusHealthRegenPerDisorder 1
	}
}
```

---

### `Chip`
**Name:** Chip Set Bonus!  
**Description:** When you end your turn, if you cast exactly 5 spells, double cast your next spell.  
**Source:** `item_setbonuses.gon`  

```
Chip {
    name "SETBONUS_CHIP_NAME"
    desc "SETBONUS_CHIP_DESC"
    pieces_required 3

    passives {
        StatusOnTurnEndIfCastNSpells {
            spells 5

            DoubleCastSpell 1
        }
	}
}
```

---

### `Demonic`
**Name:** Demonic Set Bonus!  
**Description:** When you get a kill, gain +6 Shield.  
**Source:** `item_setbonuses.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_DEMONIC`: "Evil {Catname}"

```
Demonic {
    name "SETBONUS_DEMONIC_NAME"
    desc "SETBONUS_DEMONIC_DESC"
    pieces_required 3

    name_mod CAT_NAME_MOD_DEMONIC

	passives {
		StatusOnKill {
			Shield 6
		}
	}
}
```

---

### `Frozen`
**Name:** Frozen Set Bonus!  
**Description:** You can damage Frozen units.  
**Source:** `item_setbonuses.gon`  

```
Frozen {
    name "SETBONUS_FROZEN_NAME"
    desc "SETBONUS_FROZEN_DESC"
    pieces_required 3

	shield 4

	passives {
		FreezePiercing 1
	}
}
```

---

### `Wooly`
**Name:** Wooly Set Bonus!  
**Description:** Start with a Charmed Mammoth Baby.  
**Source:** `item_setbonuses.gon`  

```
Wooly {
    name "SETBONUS_WOOLLY_NAME"
    desc "SETBONUS_WOOLLY_DESC"
    pieces_required 3

	passives {
		SpawnOnBattleStart {
			object CharmedMammothBaby
			number 1
		}
	}
}
```

---

### `Rune`
**Name:** Rune Set Bonus!  
**Description:** SETBONUS_RUNE_DESC  
**Source:** `item_setbonuses.gon`  

```
Rune {
    name "SETBONUS_RUNE_NAME"
    desc "SETBONUS_RUNE_DESC"
    pieces_required 3

	divine_shield 2
}
```

---

### `Caveman`
**Name:** Caveman Set Bonus!  
**Description:** If your [img:int] is 1 or less, gain Brace 5.  
**Source:** `item_setbonuses.gon`  

```
Caveman {
    name "SETBONUS_CAVEMAN_NAME"
    desc "SETBONUS_CAVEMAN_DESC"
    pieces_required 3

	passives {
		PassiveAtStatThreshold {
		mode less_or_equal
			threshold {
				int 1
			}
			passives {
				Brace 5
			}
		}
	}
}
```

---

### `Dino`
**Name:** Dino Set Bonus!  
**Description:** Allies gain +5 [img:shield] at the start of each battle.  
**Source:** `item_setbonuses.gon`  

```
Dino {
    name "SETBONUS_DINO_NAME"
    desc "SETBONUS_DINO_DESC"
    pieces_required 3

	passives {
		StatusAlliesOnBattleStart {
			Shield 5
		}
	}
}
```

---

### `BigRock`
**Name:** Big Rock Set Bonus!  
**Description:** Spawn 2 Charmed Geolads at the start of each battle.  
**Source:** `item_setbonuses.gon`  

```
BigRock {
    name "SETBONUS_BIGROCK_NAME"
    desc "SETBONUS_BIGROCK_DESC"
    pieces_required 3


	passives {
		SpawnOnBattleStart {
			object GeoLad
			number 2
		}
	}
}
```

---

### `Phoenix`
**Name:** Phoenix Set Bonus!  
**Description:** Flying. You can move an extra time each turn.  
**Source:** `item_setbonuses.gon`  

```
Phoenix {
    name "SETBONUS_PHOENIX_NAME"
    desc "SETBONUS_PHOENIX_DESC"
    pieces_required 3

	passives {
		Flying 1
		ExtraBasicMoves_Status 1
	}
}
```

---

### `Jester`
**Name:** Jester Set Bonus!  
**Description:** +3 Rerolls when leveling up.  
**Source:** `item_setbonuses.gon`  

```
Jester {
    name "SETBONUS_JESTER_NAME"
    desc "SETBONUS_JESTER_DESC"
    pieces_required 3
    
    passives {
        AddLevelUpRerolls 3
    }
}
```

---

### `Ancestor`
**Name:** Ancestor Set Bonus!  
**Description:** Spawn a spectral copy of yourself when you die.
The copy dies at the end of its turn.  
**Source:** `item_setbonuses.gon`  

```
Ancestor {
    name "SETBONUS_ANCESTOR_NAME"
    desc "SETBONUS_ANCESTOR_DESC"
    pieces_required 3
    
    passives {
        SpawnCatCopyWhenDowned {
            object PlayerCat_AncestralShade
            prevent_chain_tag ancestorset_shade
        }
    }
}
```

---

### `Survivalist`
**Name:** Survivalist Set Bonus!  
**Description:** Find a consumable item at the end of each battle.
When you use up a consumable or trinket, equip a new consumable from your inventory if you have any.  
**Source:** `item_setbonuses.gon`  

```
Survivalist {
    name "SETBONUS_SURVIVALIST_NAME"
    desc "SETBONUS_SURVIVALIST_DESC"
    pieces_required 3
    
    passives {
        StatusOnBattleEnd {
            Conditional_GoodRoll {
                odds 100%
                FindItemFromPool consumables
            }
        }
        AutoEquipConsumables 1
    }
}
```

---

### `Leech`
**Name:** Leech Set Bonus!  
**Description:** Start battle with 4 beefy Leech familiars.  
**Source:** `item_setbonuses.gon`  

```
Leech {
    name "SETBONUS_LEECH_NAME"
    desc "SETBONUS_LEECH_DESC"
    pieces_required 3
    
	passives {
		SpawnOnBattleStart BeefyCharmedLeech
		SpawnOnBattleStart BeefyCharmedLeech
		SpawnOnBattleStart BeefyCharmedLeech
		SpawnOnBattleStart BeefyCharmedLeech
	}
}
```

---

### `Steven`
**Name:** Steven Set Bonus!  
**Description:** Your name is now Steven! Hello Steven!  
**Source:** `item_setbonuses.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_STEVEN`: "Steven|-999"

```
Steven {//change the cats name to "Steven"
    name "SETBONUS_STEVEN_NAME"
    desc "SETBONUS_STEVEN_DESC"
    pieces_required 3

    name_mod "CAT_NAME_MOD_STEVEN"
    
    passives {
    }
}
```

---

