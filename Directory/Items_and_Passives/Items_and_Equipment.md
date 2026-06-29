# Items and Passives/Items and Equipment Directory

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

## File: `armor_sets.gon`

### `ScrapHat`
**Name:** Scrap Metal Hat  
**Description:** ARMOR_SCRAPMETALHAT_DESC  
**Source:** `armor_sets.gon`  

```
ScrapHat {
        name "ARMOR_SCRAPMETALHAT_NAME"
        desc "ARMOR_SCRAPMETALHAT_DESC"
        rarity common
        kind head
        frame 12
        set Scrap

        shield 4

        passives {
            Metal 1
        }
    }
```

---

### `ScrapMask`
**Name:** Scrap Metal Mask  
**Description:** ARMOR_SCRAPMETALMASK_DESC  
**Source:** `armor_sets.gon`  

```
ScrapMask {
        name "ARMOR_SCRAPMETALMASK_NAME"
        desc "ARMOR_SCRAPMETALMASK_DESC"
        rarity common
        kind face
        frame 12
        set Scrap

        shield 4

        passives {
            Metal 1
        }
    }
```

---

### `ScrapArmor`
**Name:** Scrap Metal Armor  
**Description:** ARMOR_SCRAPMETALARMOR_DESC  
**Source:** `armor_sets.gon`  

```
ScrapArmor {
        name "ARMOR_SCRAPMETALARMOR_NAME"
        desc "ARMOR_SCRAPMETALARMOR_DESC"
        rarity common
        kind neck
        frame 2
        set Scrap

        shield 4

        passives {
            Metal 1
        }
    }
```

---

### `LeatherHat`
**Name:** Leather Cap  
**Description:** +1 Brace.  
**Source:** `armor_sets.gon`  

```
LeatherHat {
        name "ARMOR_LEATHERHAT_NAME"
        desc "ARMOR_LEATHERHAT_DESC"
        rarity common
        kind head
        frame 23
        set Leather

		shield 1

        passives {
            Brace 1
        }
    }
```

---

### `LeatherMask`
**Name:** Leather Mask  
**Description:** +1 Brace.  
**Source:** `armor_sets.gon`  

```
LeatherMask {
        name "ARMOR_LEATHERMASK_NAME"
        desc "ARMOR_LEATHERMASK_DESC"
        rarity common
        kind face
        frame 32
        set Leather

		shield 1

        passives {
            Brace 1
        }
    }
```

---

### `LeatherArmor`
**Name:** Leather Choker  
**Description:** +1 Brace.  
**Source:** `armor_sets.gon`  

```
LeatherArmor {
        name "ARMOR_LEATHERARMOR_NAME"
        desc "ARMOR_LEATHERARMOR_DESC"
        rarity common
        kind neck
        frame 26
        set Leather

		shield 1

        passives {
            Brace 1
        }
    }
```

---

### `RagHood`
**Name:** Rag Hood  
**Description:** +15% Dodge Chance.  
**Source:** `armor_sets.gon`  

```
RagHood {
        name "ARMOR_RAGHAT_NAME"
        desc "ARMOR_RAGHAT_DESC"
        rarity common
        kind head
        frame 6
        set Rag

        passives {
            ArmorDodgeChance 15%
        }
    }
```

---

### `RagMask`
**Name:** Rag Mask  
**Description:** +15% Dodge Chance.  
**Source:** `armor_sets.gon`  

```
RagMask {
        name "ARMOR_RAGMASK_NAME"
        desc "ARMOR_RAGMASK_DESC"
        rarity common
        kind face
        frame 13
        set Rag

        passives {
            ArmorDodgeChance 15%
        }
    }
```

---

### `RagArmor`
**Name:** Rags  
**Description:** +15% Dodge Chance.  
**Source:** `armor_sets.gon`  

```
RagArmor {
        name "ARMOR_RAGARMOR_NAME"
        desc "ARMOR_RAGARMOR_DESC"
        rarity common
        kind neck
        frame 3
        set Rag

        passives {
            ArmorDodgeChance 15%
        }
    }
```

---

### `RubberHat`
**Name:** Rubber Hat  
**Description:** Units that contact you are knocked back 2 tiles.  
**Source:** `armor_sets.gon`  

```
RubberHat {
        name "ARMOR_RUBBERHAT_NAME"
        desc "ARMOR_RUBBERHAT_DESC"
        rarity common
        kind head
        frame 10
        set Rubber

        shield 2
        passives {
            MeleeRevengeDamage {
                knockback 2
            }
        }
    }
```

---

### `RubberMask`
**Name:** Rubber Mask  
**Description:** Units that contact you are knocked back 2 tiles.  
**Source:** `armor_sets.gon`  

```
RubberMask {
        name "ARMOR_RUBBERMASK_NAME"
        desc "ARMOR_RUBBERMASK_DESC"
        rarity common
        kind face
        frame 14
        set Rubber

        shield 2
        passives {
            MeleeRevengeDamage {
                knockback 2
            }
        }
    }
```

---

### `RubberArmor`
**Name:** Tire  
**Description:** Units that contact you are knocked back 2 tiles.  
**Source:** `armor_sets.gon`  

```
RubberArmor {
        name "ARMOR_RUBBERARMOR_NAME"
        desc "ARMOR_RUBBERARMOR_DESC"
        rarity common
        kind neck
        frame 4
        set Rubber

        shield 2
        passives {
            MeleeRevengeDamage {
                knockback 2
            }
        }
    }
```

---

### `CatHideHat`
**Name:** Cathide Hat  
**Description:** +1 Health Regen.
5% chance to spawn a Flea Familiar at the end of your turn.  
**Source:** `armor_sets.gon`  

```
CatHideHat {
        name "ARMOR_CATHIDEHAT_NAME"
        desc "ARMOR_CATHIDEHAT_DESC"
        rarity common
        kind head
        frame 11
        set CatHide

        shield 2
    
        passives {
            HealthRegenUp 1
            SpawnEachTurn {
                chance 5%
                object CharmedFlea

                stack_key CATHIDE
            }
        }
    }
```

---

### `CatHideMask`
**Name:** Cathide Mask  
**Description:** +1 Health Regen.
5% chance to spawn a Flea Familiar at the end of your turn.  
**Source:** `armor_sets.gon`  

```
CatHideMask {
        name "ARMOR_CATHIDEMASK_NAME"
        desc "ARMOR_CATHIDEMASK_DESC"
        rarity common
        kind face
        frame 15
        set CatHide

        shield 2
    
        passives {
            HealthRegenUp 1
            SpawnEachTurn {
                chance 5%
                object CharmedFlea

                stack_key CATHIDE
            }
        }
    }
```

---

### `CatHideArmor`
**Name:** Cathide Armor  
**Description:** +1 Health Regen.
5% chance to spawn a Flea Familiar at the end of your turn.  
**Source:** `armor_sets.gon`  

```
CatHideArmor {
        name "ARMOR_CATHIDEARMOR_NAME"
        desc "ARMOR_CATHIDEARMOR_DESC"
        rarity common
        kind neck
        frame 5
        set CatHide

        shield 2
    
        passives {
            HealthRegenUp 1
            SpawnEachTurn {
                chance 5%
                object CharmedFlea

                stack_key CATHIDE
            }
        }
    }
```

---

### `ThickHide`
**Name:** Thick Hide  
**Description:** +1 Brace. Immunity to Slow and Freeze.  
**Source:** `armor_sets.gon`  

```
ThickHide { //Aquired from DeadMammoth event
        name "ARMOR_THICKHIDE_NAME"
        desc "ARMOR_THICKHIDE_DESC"
        rarity rare
        kind neck
        frame 161
        set CatHide
        
        shield 3

        passives {
            Brace 1
            StatusImmunity [Freeze, Slow]
        }
    }
```

---

### `GutsHeart`
**Name:** Heart  
**Description:** +1 Health Regen.  
**Source:** `armor_sets.gon`  

```
GutsHeart {
        name "ARMOR_GUTSHEART_NAME"
        desc "ARMOR_GUTSHEART_DESC"
        rarity uncommon
        kind neck
        frame 19
        set Guts

        con 2
    
        passives {
            HealthRegenUp 1
        }
    }
```

---

### `GutsLiver`
**Name:** Liver  
**Description:** +1 Health Regen.  
**Source:** `armor_sets.gon`  

```
GutsLiver {
        name "ARMOR_GUTSLIVER_NAME"
        desc "ARMOR_GUTSLIVER_DESC"
        rarity uncommon
        kind head
        frame 20
        set Guts

        con 2
    
        passives {
            HealthRegenUp 1
        }
    }
```

---

### `GutsIntestines`
**Name:** Intestines  
**Description:** +1 Health Regen.  
**Source:** `armor_sets.gon`  

```
GutsIntestines {
        name "ARMOR_GUTSINTESTINES_NAME"
        desc "ARMOR_GUTSINTESTINES_DESC"
        rarity uncommon
        kind face
        frame 25
        set Guts

        con 2
    
        passives {
            HealthRegenUp 1
        }
    }
```

---

### `BonesHat`
**Name:** Skull Cap  
**Description:** Breaks when [img:shield] is depleted.
When it breaks, gain +1 [img:int] and +3 Health Regen for the rest of the battle.  
**Source:** `armor_sets.gon`  

```
BonesHat {
        name "ARMOR_BONESHAT_NAME"
        desc "ARMOR_BONESHAT_DESC"
        rarity common
        kind head
        frame 5
        set Bone

        shield 3
    
        passives {
            BoneArmorPassive 1
            StatusOnBreak {
                HealthRegenUp 3
                IntelligenceUp 1
            }
        }
    }
```

---

### `BonesMask`
**Name:** Jawbone  
**Description:** Breaks when [img:shield] is depleted.
When it breaks, gain +1 [img:str] and +3 Health Regen for the rest of the battle.  
**Source:** `armor_sets.gon`  

```
BonesMask {
        name "ARMOR_BONESMASK_NAME"
        desc "ARMOR_BONESMASK_DESC"
        rarity common
        kind face
        frame 24
        set Bone

        shield 3
    
        passives {
            BoneArmorPassive 1
            StatusOnBreak {
                HealthRegenUp 3
                StrengthUp 1
            }
        }
    }
```

---

### `BonesNeck`
**Name:** Bone Necklace  
**Description:** Breaks when [img:shield] is depleted.
When it breaks, gain +1 [img:dex] and +3 Health Regen for the rest of the battle.  
**Source:** `armor_sets.gon`  

```
BonesNeck {
        name "ARMOR_BONESARMOR_NAME"
        desc "ARMOR_BONESARMOR_DESC"
        rarity common
        kind neck
        frame 18
        set Bone

        shield 3
    
        passives {
            BoneArmorPassive 1
            StatusOnBreak {
                HealthRegenUp 3
                DexterityUp 1
            }
        }
    }
```

---

### `DirtClodHat`
**Name:** Dirt Clod Hat  
**Description:** +2 Mana Regen, +2 Health Regen.
Fragile and Brittle while wet.  
**Source:** `armor_sets.gon`  

```
DirtClodHat {
        name "ARMOR_DIRTHAT_NAME"
        desc "ARMOR_DIRTHAT_DESC"
        rarity uncommon
        kind head
        frame 22
        set DirtClod

        passives {
            AddManaRegen 2
            HealthRegenUp 2
            FragileDuringElement water
            BrittleDuringElement water
        }
    }
```

---

### `DirtClodMask`
**Name:** Dirt Clod Mask  
**Description:** +2 Mana Regen, +2 Health Regen.
Fragile and Brittle while wet.  
**Source:** `armor_sets.gon`  

```
DirtClodMask {
        name "ARMOR_DIRTMASK_NAME"
        desc "ARMOR_DIRTMASK_DESC"
        rarity uncommon
        kind face
        frame 31
        set DirtClod

        passives {
            AddManaRegen 2
            HealthRegenUp 2
            FragileDuringElement water
            BrittleDuringElement water
        }
    }
```

---

### `DirtClodNeck`
**Name:** Dirt Clod Necklace  
**Description:** +2 Mana Regen, +2 Health Regen.
Fragile and Brittle while wet.  
**Source:** `armor_sets.gon`  

```
DirtClodNeck {
        name "ARMOR_DIRTARMOR_NAME"
        desc "ARMOR_DIRTARMOR_DESC"
        rarity uncommon
        kind neck
        frame 25
        set DirtClod

        passives {
            AddManaRegen 2
            HealthRegenUp 2
            FragileDuringElement water
            BrittleDuringElement water
        }
    }
```

---

### `BarbedHat`
**Name:** Barbed Hat  
**Description:** +1 Damage, +1 Thorns, -1 max HP.  
**Source:** `armor_sets.gon`  

```
BarbedHat {
        name "ARMOR_BARBEDHAT_NAME"
        desc "ARMOR_BARBEDHAT_DESC"
        rarity common
        kind head
        frame 21
        set Barbed

        max_health -1

        passives {
            Thorns 1
            DamageUp 1
            Metal 1
        }
    }
```

---

### `BarbedMask`
**Name:** Barbed Mask  
**Description:** +1 Damage, +1 Thorns, -1 max HP.  
**Source:** `armor_sets.gon`  

```
BarbedMask {
        name "ARMOR_BARBEDMASK_NAME"
        desc "ARMOR_BARBEDMASK_DESC"
        rarity common
        kind face
        frame 26
        set Barbed

        max_health -1

        passives {
            Thorns 1
            DamageUp 1
            Metal 1
        }
    }
```

---

### `BarbedNeck`
**Name:** Barbed Necklace  
**Description:** +1 Damage, +1 Thorns, -1 max HP.  
**Source:** `armor_sets.gon`  

```
BarbedNeck {
        name "ARMOR_BARBEDARMOR_NAME"
        desc "ARMOR_BARBEDARMOR_DESC"
        rarity common
        kind neck
        frame 20
        set Barbed

        max_health -1

        passives {
            Thorns 1
            DamageUp 1
            Metal 1
        }
    }
```

---

### `SludgeHat`
**Name:** Sludge Hat  
**Description:** ARMOR_SLUDGEHAT_DESC  
**Source:** `armor_sets.gon`  

```
SludgeHat {
        name "ARMOR_SLUDGEHAT_NAME"
        desc "ARMOR_SLUDGEHAT_DESC"
        kind head
        frame 14
        set Sludge
        cursed true

        shield 1
        cha -1
    }
```

---

### `SludgeMask`
**Name:** Sludge Mask  
**Description:** ARMOR_SLUDGEMASK_DESC  
**Source:** `armor_sets.gon`  

```
SludgeMask {
        name "ARMOR_SLUDGEMASK_NAME"
        desc "ARMOR_SLUDGEMASK_DESC"
        kind face
        frame 23
        set Sludge
        cursed true

        shield 1
        cha -1
    }
```

---

### `SludgeNeck`
**Name:** Sludge Necklace  
**Description:** ARMOR_SLUDGEARMOR_DESC  
**Source:** `armor_sets.gon`  

```
SludgeNeck {
        name "ARMOR_SLUDGEARMOR_NAME"
        desc "ARMOR_SLUDGEARMOR_DESC"
        kind neck
        frame 14
        set Sludge
        cursed true

        shield 1
        cha -1
    }
```

---

### `CoolGlasses`
**Name:** Cool Glasses  
**Description:** Fragile  
**Source:** `armor_sets.gon`  

```
CoolGlasses {
        name "ARMOR_COOLMASK_NAME"
        desc "ARMOR_COOLMASK_DESC"
        rarity common
        kind face
        frame 10
        set Cool

        cha 2

        passives {
            Fragile 1
        }
    }
```

---

### `CoolShirt`
**Name:** Cool Shirt  
**Description:** Fragile  
**Source:** `armor_sets.gon`  

```
CoolShirt {
        name "ARMOR_COOLARMOR_NAME"
        desc "ARMOR_COOLARMOR_DESC"
        rarity common
        kind neck
        frame 36
        set Cool

        cha 2

        passives {
            Fragile 1
        }
    }
```

---

### `CoolHat`
**Name:** Cool Hat  
**Description:** Fragile  
**Source:** `armor_sets.gon`  

```
CoolHat {
        name "ARMOR_COOLHAT_NAME"
        desc "ARMOR_COOLHAT_DESC"
        rarity common
        kind head
        frame 39
        set Cool

        cha 2

        passives {
            Fragile 1
        }
    }
```

---

### `PaperHat`
**Name:** Paper Hat  
**Description:** +1 Bleed Thorns.
Your basic attack inflicts Bleed.
Fragile, Brittle, Flammable, melts in water.  
**Source:** `armor_sets.gon`  

```
PaperHat {
        name "ARMOR_PAPERHAT_NAME"
        desc "ARMOR_PAPERHAT_DESC"
        rarity common
        kind head
        frame 40
        set Paper

        passives {
            BleedThorns 1
            AddStatusToBasicAttack {
                Bleed 1
            }
            Flammable 1
            BreakOnElement water
            Fragile 1
            Brittle 1
        }
    }
```

---

### `PaperMask`
**Name:** Paper Mask  
**Description:** +1 Bleed Thorns.
Your basic attack inflicts Bleed.
Fragile, Brittle, Flammable, melts in water.  
**Source:** `armor_sets.gon`  

```
PaperMask {
        name "ARMOR_PAPERMASK_NAME"
        desc "ARMOR_PAPERMASK_DESC"
        rarity common
        kind face
        frame 46
        set Paper

        passives {
            BleedThorns 1
            AddStatusToBasicAttack {
                Bleed 1
            }
            Flammable 1
            BreakOnElement water
            Fragile 1
            Brittle 1
        }
    }
```

---

### `PaperArmor`
**Name:** Paper Shoulder Pads  
**Description:** +1 Bleed Thorns.
Your basic attack inflicts Bleed.
Fragile, Brittle, Flammable, melts in water.  
**Source:** `armor_sets.gon`  

```
PaperArmor {
        name "ARMOR_PAPERARMOR_NAME"
        desc "ARMOR_PAPERARMOR_DESC"
        rarity common
        kind neck
        frame 37
        set Paper

        passives {
            BleedThorns 1
            AddStatusToBasicAttack {
                Bleed 1
            }
            Flammable 1
            BreakOnElement water
            Fragile 1
            Brittle 1
        }
    }
```

---

### `CardboardHat`
**Name:** Cardboard Hat  
**Description:** Fragile, Flammable, Brittle when wet.  
**Source:** `armor_sets.gon`  

```
CardboardHat {
        name "ARMOR_CARDBOARDHAT_NAME"
        desc "ARMOR_CARDBOARDHAT_DESC"
        rarity common
        kind head
        frame 41
        set Cardboard

        shield 2

        passives {
            Flammable 1
            Fragile 1
            BrittleDuringElement water
        }
    }
```

---

### `CardboardMask`
**Name:** Cardboard Mask  
**Description:** Fragile, Flammable, Brittle when wet.  
**Source:** `armor_sets.gon`  

```
CardboardMask {
        name "ARMOR_CARDBOARDMASK_NAME"
        desc "ARMOR_CARDBOARDMASK_DESC"
        rarity common
        kind face
        frame 47
        set Cardboard

        shield 2

        passives {
            Flammable 1
            Fragile 1
            BrittleDuringElement water
        }
    }
```

---

### `CardboardArmor`
**Name:** Cardboard Necklace  
**Description:** Fragile, Flammable, Brittle when wet.  
**Source:** `armor_sets.gon`  

```
CardboardArmor {
        name "ARMOR_CARDBOARDARMOR_NAME"
        desc "ARMOR_CARDBOARDARMOR_DESC"
        rarity common
        kind neck
        frame 38
        set Cardboard

        shield 2

        passives {
            Flammable 1
            Fragile 1
            BrittleDuringElement water
        }
    }
```

---

### `UsedHat`
**Name:** Used Hat  
**Description:** ARMOR_USEDHAT_DESC  
**Source:** `armor_sets.gon`  

```
UsedHat {
        name "ARMOR_USEDHAT_NAME"
        desc "ARMOR_USEDHAT_DESC"
        rarity common
        kind head
        frame 31
        set Used

        shield 1
    }
```

---

### `UsedMask`
**Name:** Used Glasses  
**Description:** ARMOR_USEDMASK_DESC  
**Source:** `armor_sets.gon`  

```
UsedMask {
        name "ARMOR_USEDMASK_NAME"
        desc "ARMOR_USEDMASK_DESC"
        rarity common
        kind face
        frame 38
        set Used

        shield 1
    }
```

---

### `UsedArmor`
**Name:** Used Shirt  
**Description:** ARMOR_USEDARMOR_DESC  
**Source:** `armor_sets.gon`  

```
UsedArmor {
        name "ARMOR_USEDARMOR_NAME"
        desc "ARMOR_USEDARMOR_DESC"
        rarity common
        kind neck
        frame 27
        set Used

        shield 1
    }
```

---

### `WoodHat`
**Name:** Wood Hat  
**Description:** +1 Thorns.
Fragile, Flammable.  
**Source:** `armor_sets.gon`  

```
WoodHat {
        name "ARMOR_WOODHAT_NAME"
        desc "ARMOR_WOODHAT_DESC"
        rarity common
        kind head
        frame 33
        set Wood

        shield 2

        passives {
            Thorns 1
            Fragile 1
            Flammable 2
        }
    }
```

---

### `WoodMask`
**Name:** Wood Mask  
**Description:** +1 Thorns.
Fragile, Flammable.  
**Source:** `armor_sets.gon`  

```
WoodMask {
        name "ARMOR_WOODMASK_NAME"
        desc "ARMOR_WOODMASK_DESC"
        rarity common
        kind face
        frame 40
        set Wood

        shield 2

        passives {
            Thorns 1
            Fragile 1
            Flammable 2
        }
    }
```

---

### `WoodArmor`
**Name:** Wood Shoulder Pads  
**Description:** +1 Thorns.
Fragile, Flammable.  
**Source:** `armor_sets.gon`  

```
WoodArmor {
        name "ARMOR_WOODARMOR_NAME"
        desc "ARMOR_WOODARMOR_DESC"
        rarity common
        kind neck
        frame 29
        set Wood

        shield 2

        passives {
            Thorns 1
            Fragile 1
            Flammable 2
        }
    }
```

---

### `RecycledHat`
**Name:** Recycled Hat  
**Description:** Brittle. Find a common item when this breaks.  
**Source:** `armor_sets.gon`  

```
RecycledHat {
        name "ARMOR_RECYCLEDHAT_NAME"
        desc "ARMOR_RECYCLEDHAT_DESC"
        rarity common
        kind head
        frame 34
        set Recycled

        shield 2

        passives {
            Brittle 1
            StatusOnBreak {
                FindItemFromPool common
            }
        }
    }
```

---

### `RecycledMask`
**Name:** Recycled Mask  
**Description:** Brittle. Find a common item when this breaks.  
**Source:** `armor_sets.gon`  

```
RecycledMask {
        name "ARMOR_RECYCLEDMASK_NAME"
        desc "ARMOR_RECYCLEDMASK_DESC"
        rarity common
        kind face
        frame 41
        set Recycled

        shield 2

        passives {
            Brittle 1
            StatusOnBreak {
                FindItemFromPool common
            }
        }
    }
```

---

### `RecycledArmor`
**Name:** Recycled Necklace  
**Description:** Brittle. Find a common item when this breaks.  
**Source:** `armor_sets.gon`  

```
RecycledArmor {
        name "ARMOR_RECYCLEDARMOR_NAME"
        desc "ARMOR_RECYCLEDARMOR_DESC"
        rarity common
        kind neck
        frame 30
        set Recycled

        shield 2

        passives {
            Brittle 1
            StatusOnBreak {
                FindItemFromPool common
            }
            Metal 1
        }
    }
```

---

### `RottenHat`
**Name:** Rotten Meat Hat  
**Description:** Spawn a Charmed Maggot or Fly when you end your turn.  
**Source:** `armor_sets.gon`  

```
RottenHat {
        name "ARMOR_ROTTENHAT_NAME"
        desc "ARMOR_ROTTENHAT_DESC"
        rarity uncommon
        kind head
        frame 35
        set Rotten

        cha -1

        passives {
            SpawnEachTurn {
                chance 100%
                object [CharmedFly CharmedMaggot]
            }
        }
    }
```

---

### `RottenMask`
**Name:** Rotten Meat Mask  
**Description:** Spawn a Charmed Maggot or Fly when you end your turn.  
**Source:** `armor_sets.gon`  

```
RottenMask {
        name "ARMOR_ROTTENMASK_NAME"
        desc "ARMOR_ROTTENMASK_DESC"
        rarity uncommon
        kind face
        frame 42
        set Rotten

        cha -1

        passives {
            SpawnEachTurn {
                chance 100%
                object [CharmedFly CharmedMaggot]
            }
        }
    }
```

---

### `RottenArmor`
**Name:** Rotten Meat Armor  
**Description:** Spawn a Charmed Maggot or Fly when you end your turn.  
**Source:** `armor_sets.gon`  

```
RottenArmor {
        name "ARMOR_ROTTENARMOR_NAME"
        desc "ARMOR_ROTTENARMOR_DESC"
        rarity uncommon
        kind neck
        frame 31
        set Rotten

        cha -1

        passives {
            SpawnEachTurn {
                chance 100%
                object [CharmedFly CharmedMaggot]
            }
        }
    }
```

---

### `JankAlloyHat`
**Name:** Jank Alloy Armor  
**Description:** +1 Brace.
Brittle.  
**Source:** `armor_sets.gon`  

```
JankAlloyHat {
        name "ARMOR_JANKARMOR_NAME"
        desc "ARMOR_JANKARMOR_DESC"
        kind head
        frame 42
        set JankAlloy

        shield 2

        passives {
            Brace 1
            Brittle 1
            Metal 1
        }
    }
```

---

### `JankAlloyMask`
**Name:** Jank Alloy Mask  
**Description:** +1 Brace.
Brittle.  
**Source:** `armor_sets.gon`  

```
JankAlloyMask {
        name "ARMOR_JANKMASK_NAME"
        desc "ARMOR_JANKMASK_DESC"
        kind face
        frame 48
        set JankAlloy

        shield 2

        passives {
            Brace 1
            Brittle 1
            Metal 1
        }
    }
```

---

### `JankAlloyArmor`
**Name:** Jank Alloy Hat  
**Description:** +1 Brace.
Brittle.  
**Source:** `armor_sets.gon`  

```
JankAlloyArmor {
        name "ARMOR_JANKHAT_NAME"
        desc "ARMOR_JANKHAT_DESC"
        kind neck
        frame 39
        set JankAlloy

        shield 2

        passives {
            Brace 1
            Brittle 1
            Metal 1
        }
    }
```

---

### `AlloyHat`
**Name:** Alloy Mask  
**Description:** +1 Brace, +2 Thorns.
Brittle.  
**Source:** `armor_sets.gon`  

```
AlloyHat {
        name "ARMOR_ALLOYMASK_NAME"
        desc "ARMOR_ALLOYMASK_DESC"
        kind head
        frame 43
        set Alloy

        shield 3

        passives {
            Brace 1
            Thorns 2
            Brittle 1
            Metal 1
        }
    }
```

---

### `AlloyMask`
**Name:** Alloy Mask  
**Description:** +1 Brace, +2 Thorns.
Brittle.  
**Source:** `armor_sets.gon`  

```
AlloyMask {
        name "ARMOR_ALLOYMASK_NAME"
        desc "ARMOR_ALLOYMASK_DESC"
        kind face
        frame 49
        set Alloy

        shield 3

        passives {
            Brace 1
            Thorns 2
            Brittle 1
            Metal 1
        }
    }
```

---

### `AlloyArmor`
**Name:** Alloy Armor  
**Description:** +1 Brace, +2 Thorns.
Brittle.  
**Source:** `armor_sets.gon`  

```
AlloyArmor {
        name "ARMOR_ALLOYARMOR_NAME"
        desc "ARMOR_ALLOYARMOR_DESC"
        kind neck
        frame 40
        set Alloy

        shield 3

        passives {
            Brace 1
            Thorns 2
            Brittle 1
            Metal 1
        }
    }
```

---

### `AdvancedAlloyHat`
**Name:** Advanced Alloy Hat  
**Description:** +2 Brace, +2 Thorns.
Brittle.  
**Source:** `armor_sets.gon`  

```
AdvancedAlloyHat {
        name "ARMOR_ADVANCEDHAT_NAME"
        desc "ARMOR_ADVANCEDHAT_DESC"
        kind head
        frame 44
        set AdvancedAlloy

        shield 4

        passives {
            Brace 2
            Thorns 2
            Brittle 1
            Metal 1
        }
    }
```

---

### `AdvancedAlloyMask`
**Name:** Advanced Alloy Mask  
**Description:** +2 Brace, +2 Thorns.
Brittle.  
**Source:** `armor_sets.gon`  

```
AdvancedAlloyMask {
        name "ARMOR_ADVANCEDMASK_NAME"
        desc "ARMOR_ADVANCEDMASK_DESC"
        kind face
        frame 50
        set AdvancedAlloy

        shield 4

        passives {
            Brace 2
            Thorns 2
            Brittle 1
            Metal 1
        }
    }
```

---

### `AdvancedAlloyArmor`
**Name:** Advanced Alloy Armor  
**Description:** +2 Brace, +2 Thorns.
Brittle.  
**Source:** `armor_sets.gon`  

```
AdvancedAlloyArmor {
        name "ARMOR_ADVANCEDARMOR_NAME"
        desc "ARMOR_ADVANCEDARMOR_DESC"
        kind neck
        frame 41
        set AdvancedAlloy

        shield 4

        passives {
            Brace 2
            Thorns 2
            Brittle 1
            Metal 1
        }
    }
```

---

### `EliteAlloyHat`
**Name:** Elite Alloy Hat  
**Description:** +2 Brace, +3 Thorns, All Stats Up 1.
Brittle.  
**Source:** `armor_sets.gon`  

```
EliteAlloyHat {
        name "ARMOR_ELITEHAT_NAME"
        desc "ARMOR_ELITEHAT_DESC"
        kind head
        frame 45
        set EliteAlloy

        shield 5

        passives {
            Brace 2
            Thorns 3
            AllStatsUp 1
            Brittle 1
            Metal 1
        }
    }
```

---

### `EliteAlloyMask`
**Name:** Elite Alloy Mask  
**Description:** +2 Brace, +3 Thorns, All Stats Up 1.
Brittle.  
**Source:** `armor_sets.gon`  

```
EliteAlloyMask {
        name "ARMOR_ELITEMASK_NAME"
        desc "ARMOR_ELITEMASK_DESC"
        kind face
        frame 51
        set EliteAlloy

        shield 5

        passives {
            Brace 2
            Thorns 3
            AllStatsUp 1
            Brittle 1
            Metal 1
        }
    }
```

---

### `EliteAlloyArmor`
**Name:** Elite Alloy Armor  
**Description:** +2 Brace, +3 Thorns, All Stats Up 1.
Brittle.  
**Source:** `armor_sets.gon`  

```
EliteAlloyArmor {
        name "ARMOR_ELITEARMOR_NAME"
        desc "ARMOR_ELITEARMOR_DESC"
        kind neck
        frame 42
        set EliteAlloy

        shield 5

        passives {
            Brace 2
            Thorns 3
            AllStatsUp 1
            Brittle 1
            Metal 1
        }
    }
```

---

### `TwineHat`
**Name:** Twine Hat  
**Description:** +50% chance to Grapple units that contact you.
Flammable.  
**Source:** `armor_sets.gon`  

```
TwineHat {
        name "ARMOR_TWINEHAT_NAME"
        desc "ARMOR_TWINEHAT_DESC"
        rarity common
        kind head
        frame 32
        set Twine

		shield 3

        passives {
            Flammable 1
            MeleeRevengeDamage {
                damage 0
                effects {
                    Grappled [1, .50]
                }
            }
        }
    }
```

---

### `TwineMask`
**Name:** Twine Mask  
**Description:** +50% chance to Grapple units that contact you.
Flammable.  
**Source:** `armor_sets.gon`  

```
TwineMask {
        name "ARMOR_TWINEMASK_NAME"
        desc "ARMOR_TWINEMASK_DESC"
        rarity common
        kind face
        frame 39
        set Twine

		shield 1

        passives {
            Flammable 1
            MeleeRevengeDamage {
                damage 0
                effects {
                    Grappled [1, .50]
                }
            }
        }
    }
```

---

### `TwineArmor`
**Name:** Twine Armor  
**Description:** +50% chance to Grapple units that contact you.
Flammable.  
**Source:** `armor_sets.gon`  

```
TwineArmor {
        name "ARMOR_TWINEARMOR_NAME"
        desc "ARMOR_TWINEARMOR_DESC"
        rarity common
        kind neck
        frame 28
        set Twine
		
		shield 1

        passives {
            Flammable 1
            MeleeRevengeDamage {
                damage 0
                effects {
                    Grappled [1, .50]
                }
            }
        }
    }
```

---

### `RockHat`
**Name:** Rock Hat  
**Description:** Brittle. Your basic attack has +1 Knockback. Gain coins when this breaks.  
**Source:** `armor_sets.gon`  

```
RockHat {
        name "ARMOR_ROCKHAT_NAME"
        desc "ARMOR_ROCKHAT_DESC"
        rarity uncommon
        kind head
        frame 46
        set Rock

        shield 6
        spd -1
        passives { 
		    Brittle 1
		    AddStatusToBasicAttack {
                Knockback 1
            }
            StatusOnBreak {
                GainCoinsRange {
                    min 1
                    max 25
                }
            }
        }
    }
```

---

### `RockMask`
**Name:** Rock Mask  
**Description:** Brittle. Your basic attack has +1 Knockback. Gain coins when this breaks.  
**Source:** `armor_sets.gon`  

```
RockMask {
        name "ARMOR_ROCKMASK_NAME"
        desc "ARMOR_ROCKMASK_DESC"
        rarity uncommon
        kind face
        frame 53
        set Rock

        shield 6
        spd -1
        passives {
		    Brittle 1
		    AddStatusToBasicAttack {
                Knockback 1
            }
            StatusOnBreak {
                GainCoinsRange {
                    min 1
                    max 25
                }
            }
        }
    }
```

---

### `RockArmor`
**Name:** Rock Necklace  
**Description:** Brittle. Your basic attack has +1 Knockback. Gain coins when this breaks.  
**Source:** `armor_sets.gon`  

```
RockArmor {
        name "ARMOR_ROCKARMOR_NAME"
        desc "ARMOR_ROCKARMOR_DESC"
        rarity uncommon
        kind neck
        frame 44
        set Rock

        shield 6
        spd -1
        passives {
		    Brittle 1
		    AddStatusToBasicAttack {
                Knockback 1
            }
            StatusOnBreak {
                GainCoinsRange {
                    min 1
                    max 25
                }
            }
        }
    }
```

---

### `MinerHat`
**Name:** Miner Hat  
**Description:** Physical attacks can't miss.  
**Source:** `armor_sets.gon`  

```
MinerHat {
        name "ARMOR_MINERHAT_NAME"
        desc "ARMOR_MINERHAT_DESC"
        rarity uncommon
        kind head
        frame 48
        set Miner

        shield 4
        passives {
            TrueShot 1
        }
    }
```

---

### `MinerMask`
**Name:** Miner Mask  
**Description:** Poison Immunity.  
**Source:** `armor_sets.gon`  

```
MinerMask {
        name "ARMOR_MINERMASK_NAME"
        desc "ARMOR_MINERMASK_DESC"
        rarity uncommon
        kind face
        frame 55
        set Miner
		
		shield 4

        passives {
            StatusImmunity Poison
            CantCatchDiseases 1
            CantSpreadDiseases 1
        }
    }
```

---

### `MinerArmor`
**Name:** Miner Pack  
**Description:** Your basic attack has +1 Knockback.
+1 Knockback damage.  
**Source:** `armor_sets.gon`  

```
MinerArmor {
        name "ARMOR_MINERARMOR_NAME"
        desc "ARMOR_MINERARMOR_DESC"
        rarity uncommon
        kind neck
        frame 46
        set Miner

        passives {
            AddKnockbackDamage 1
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }
```

---

### `GemstoneHat`
**Name:** Gemstone Crown  
**Description:** +1 Kinetic Spikes.  
**Source:** `armor_sets.gon`  

```
GemstoneHat {
        name "ARMOR_GEMSTONEHAT_NAME"
        desc "ARMOR_GEMSTONEHAT_DESC"
        rarity uncommon
        kind head
        frame 47
        set Gemstone

        shield 1
        cha 1
        passives {
            KineticSpikes 1
        }
    }
```

---

### `GemstoneMask`
**Name:** Gemstone Mask  
**Description:** +1 Kinetic Spikes.  
**Source:** `armor_sets.gon`  

```
GemstoneMask {
        name "ARMOR_GEMSTONEMASK_NAME"
        desc "ARMOR_GEMSTONEMASK_DESC"
        rarity uncommon
        kind face
        frame 54
        set Gemstone

        shield 1
        cha 1
        passives {
            KineticSpikes 1
        }
    }
```

---

### `GemstoneArmor`
**Name:** Gemstone Necklace  
**Description:** +1 Kinetic Spikes.  
**Source:** `armor_sets.gon`  

```
GemstoneArmor {
        name "ARMOR_GEMSTONEARMOR_NAME"
        desc "ARMOR_GEMSTONEARMOR_DESC"
        rarity uncommon
        kind neck
        frame 45
        set Gemstone

        shield 1
        cha 1
        passives {
            KineticSpikes 1
        }
    }
```

---

### `VeinyHat`
**Name:** Veiny Hat  
**Description:** When you damage a Bleeding unit, gain +1 [img:spd].  
**Source:** `armor_sets.gon`  

```
VeinyHat {
        name "ARMOR_VEINYHAT_NAME"
        desc "ARMOR_VEINYHAT_DESC"
        rarity rare
        kind head
        frame 49
        set Veiny

        passives {
            AddStatusToAllDamage {
                must_do_damage true
                Conditional_HasStatus {
                    status Bleed
                    ApplyToSource {
                        SpeedUp 1
                    }
                }
            }
        }
    }
```

---

### `VeinyMask`
**Name:** Veiny Mask  
**Description:** When you damage a Bleeding unit, gain +1 [img:str].  
**Source:** `armor_sets.gon`  

```
VeinyMask {
        name "ARMOR_VEINYMASK_NAME"
        desc "ARMOR_VEINYMASK_DESC"
        rarity rare
        kind face
        frame 56
        set Veiny

        passives {
            AddStatusToAllDamage {
                must_do_damage true
                Conditional_HasStatus {
                    status Bleed
                    ApplyToSource {
                        StrengthUp 1
                    }
                }
            }
        }
    }
```

---

### `VeinyArmor`
**Name:** Veiny Necklace  
**Description:** When you damage a Bleeding unit, heal 3 HP.  
**Source:** `armor_sets.gon`  

```
VeinyArmor {
        name "ARMOR_VEINYARMOR_NAME"
        desc "ARMOR_VEINYARMOR_DESC"
        rarity rare
        kind neck
        frame 47
        set Veiny

        passives {
            AddStatusToAllDamage {
                must_do_damage true
                Conditional_HasStatus {
                    status Bleed
                    FlatLeechIfDamaged 3
                }
            }
        }
    }
```

---

### `GimpHat`
**Name:** Leather Hood  
**Description:** Gain +2 Charge when you take damage.  
**Source:** `armor_sets.gon`  

```
GimpHat {
        name "ARMOR_GIMPHAT_NAME"
        desc "ARMOR_GIMPHAT_DESC"
        rarity uncommon
        kind head
        frame 28
        set Gimp

        passives {
            StatusOnTookDamage {
                Charge 2
            }
        }
    }
```

---

### `GimpMask`
**Name:** Ball Gag  
**Description:** Gain +2 Charge when you take damage.  
**Source:** `armor_sets.gon`  

```
GimpMask {
        name "ARMOR_GIMPMASK_NAME"
        desc "ARMOR_GIMPMASK_DESC"
        rarity uncommon
        kind face
        frame 37
        set Gimp

        passives {
            StatusOnTookDamage {
                Charge 2
            }
        }
    }
```

---

### `GimpArmor`
**Name:** Leather Collar  
**Description:** Gain +2 Charge when you take damage.  
**Source:** `armor_sets.gon`  

```
GimpArmor {
        name "ARMOR_GIMPCOLLAR_NAME"
        desc "ARMOR_GIMPCOLLAR_DESC"
        rarity uncommon
        kind neck
        frame 33
        set Gimp

        passives {
            StatusOnTookDamage {
                Charge 2
            }
        }
    }
```

---

### `BionicHat`
**Name:** Bionic Skull Plating  
**Description:** Fragile.  
**Source:** `armor_sets.gon`  

```
BionicHat {
        name "ARMOR_BIONICHAT_NAME"
        desc "ARMOR_BIONICHAT_DESC"
        rarity uncommon
        kind head
        frame 25
        set Bionic

        spd 3

        passives {
            Fragile 1
            Metal 1
        }
    }
```

---

### `BionicMask`
**Name:** Bionic Face Plating  
**Description:** Fragile.  
**Source:** `armor_sets.gon`  

```
BionicMask {
        name "ARMOR_BIONICMASK_NAME"
        desc "ARMOR_BIONICMASK_DESC"
        rarity uncommon
        kind face
        frame 34
        set Bionic

        spd 3

        passives {
            Fragile 1
            Metal 1
        }
    }
```

---

### `BionicArmor`
**Name:** Bionic Neck Plating  
**Description:** Fragile.  
**Source:** `armor_sets.gon`  

```
BionicArmor {
        name "ARMOR_BIONICARMOR_NAME"
        desc "ARMOR_BIONICARMOR_DESC"
        rarity uncommon
        kind neck
        frame 34
        set Bionic

        spd 3

        passives {
            Fragile 1
            Metal 1
        }
    }
```

---

### `CyborgHat`
**Name:** Frontal Lobe Implant  
**Description:** 10% chance to teleport to a neighboring tile when targeted by an enemy.  
**Source:** `armor_sets.gon`  

```
CyborgHat {
        name "ARMOR_CYBORGHAT_NAME"
        desc "ARMOR_CYBORGHAT_DESC"
        rarity rare
        kind head
        frame 26
        set Cyborg

        int 1
		shield 3
		
        passives {
            ChanceToBackflip {
                ability ShadowstepDodge
                chance 10%
            }
            Metal 1
        }
    }
```

---

### `CyborgMask`
**Name:** Optic Nerve Implant  
**Description:** +1 range, +1 reach.  
**Source:** `armor_sets.gon`  

```
CyborgMask {
        name "ARMOR_CYBORGMASK_NAME"
        desc "ARMOR_CYBORGMASK_DESC"
        rarity rare
        kind face
        frame 35
        set Cyborg

        int 1
		shield 3

        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1
            Metal 1
        }
    }
```

---

### `CyborgArmor`
**Name:** Cerebellum Implant  
**Description:** +10% Crit Chance.  
**Source:** `armor_sets.gon`  

```
CyborgArmor {
        name "ARMOR_CYBORGARMOR_NAME"
        desc "ARMOR_CYBORGARMOR_DESC"
        rarity rare
        kind neck
        frame 35
        set Cyborg

        int 1
		shield 3

        passives {
            CritChanceUp 10
            Metal 1
        }
    }
```

---

### `LuckyHat`
**Name:** Lucky Hat  
**Description:** Fragile.  
**Source:** `armor_sets.gon`  

```
LuckyHat {
        name "ARMOR_LUCKYHAT_NAME"
        desc "ARMOR_LUCKYHAT_DESC"
        rarity common
        kind head
        frame 27
        set Lucky

        lck 1

        passives {
            Fragile 1
        }
    }
```

---

### `LuckyMask`
**Name:** Lucky Clover  
**Description:** Fragile.  
**Source:** `armor_sets.gon`  

```
LuckyMask {
        name "ARMOR_LUCKYMASK_NAME"
        desc "ARMOR_LUCKYMASK_DESC"
        rarity common
        kind face
        frame 36
        set [Lucky, Leafy]

        lck 1

        passives {
            Fragile 1
        }
    }
```

---

### `LuckyArmor`
**Name:** Lucky Horseshoe  
**Description:** Fragile.  
**Source:** `armor_sets.gon`  

```
LuckyArmor {
        name "ARMOR_LUCKYARMOR_NAME"
        desc "ARMOR_LUCKYARMOR_DESC"
        rarity common
        kind neck
        frame 32
        set Lucky

        lck 1

        passives {
            Fragile 1
        }
    }
```

---

### `FlyHat`
**Name:** Fly Hat  
**Description:** +10% Dodge Chance.  
**Source:** `armor_sets.gon`  

```
FlyHat {
        name "ARMOR_FLYHAT_NAME"
        desc "ARMOR_FLYHAT_DESC"
        kind head
        frame 73
        set Fly
        cursed true

        cha -1
        spd 3

        passives {
            AddTag bug
            ArmorDodgeChance 10%
        }
    }
```

---

### `FlyMask`
**Name:** Fly Mask  
**Description:** +10% Dodge Chance.  
**Source:** `armor_sets.gon`  

```
FlyMask {
        name "ARMOR_FLYMASK_NAME"
        desc "ARMOR_FLYMASK_DESC"
        kind face
        frame 75
        set Fly
        cursed true

        dex 3
        cha -1

        passives {
            AddTag bug
            ArmorDodgeChance 10%
           
        }
    }
```

---

### `FlyNeck`
**Name:** Fly Carapace  
**Description:** +10% Dodge Chance.  
**Source:** `armor_sets.gon`  

```
FlyNeck {
        name "ARMOR_FLYARMOR_NAME"
        desc "ARMOR_FLYARMOR_DESC"
        kind neck
        frame 59
        set Fly
        cursed true

        con 3
        cha -1

        passives {
            AddTag bug
            ArmorDodgeChance 10%
        }
    }
```

---

### `FaceGrub`
**Name:** Face Grub  
**Description:** When your [img:shield] is depleted, this transforms into a Maggot familiar.  
**Source:** `armor_sets.gon`  

```
FaceGrub {//todo needs a huge buff, maybe just spawn maggots on damage and not break
        name "ARMOR_FACEGRUB_NAME"
        desc "ARMOR_FACEGRUB_DESC"
        rarity uncommon
        kind face
        frame 21
        set Grub

        shield 3

        passives {
            DropAsFamiliarOnArmorBreak FaceGrubFamiliar
        }
    }
```

---

### `HeadGrub`
**Name:** Head Grub  
**Description:** When your [img:shield] is depleted, this transforms into a Maggot familiar.  
**Source:** `armor_sets.gon`  

```
HeadGrub {
        name "ARMOR_HEADGRUB_NAME"
        desc "ARMOR_HEADGRUB_DESC"
        rarity uncommon
        kind head
        frame 17
        set Grub

        shield 3

        passives {
            DropAsFamiliarOnArmorBreak HeadGrubFamiliar
        }
    }
```

---

### `NeckGrub`
**Name:** Neck Grub  
**Description:** When your [img:shield] is depleted, this transforms into a Maggot familiar.  
**Source:** `armor_sets.gon`  

```
NeckGrub {
        name "ARMOR_NECKGRUB_NAME"
        desc "ARMOR_NECKGRUB_DESC"
        rarity uncommon
        kind neck
        frame 16
        set Grub

        shield 3

        passives {
            DropAsFamiliarOnArmorBreak NeckGrubFamiliar
        }
    }
```

---

### `CrimsonMask`
**Name:** Crimson Mask  
**Description:** +1 Damage.
Gain +1 Damage when you kill an enemy.  
**Source:** `armor_sets.gon`  

```
CrimsonMask {
        name "ARMOR_CRIMSONMASK_NAME"
        desc "ARMOR_CRIMSONMASK_DESC"
        rarity rare
        kind face
        frame 57
        set Meat

        passives {
            DamageUp 1
            StatusOnKillEnemy {
                DamageUp 1
            }
        }
    }
```

---

### `CrimsonMask_Cursed`
**Source:** `armor_sets.gon`  

```
CrimsonMask_Cursed {
        variant_of CrimsonMask
        cursed true
    }
```

---

### `RedCap`
**Name:** Red Cap  
**Description:** +1 Damage.
Gain +1 Damage when you kill an enemy.  
**Source:** `armor_sets.gon`  

```
RedCap {
        name "ARMOR_REDCAP_NAME"
        desc "ARMOR_REDCAP_DESC"
        rarity rare
        kind head
        frame 50
        set Meat

        passives {
            DamageUp 1
            StatusOnKillEnemy {
                DamageUp 1
            }
        }
    }
```

---

### `RedCap_Cursed`
**Source:** `armor_sets.gon`  

```
RedCap_Cursed {
        variant_of RedCap
        cursed true
    }
```

---

### `PoundOfFlesh`
**Name:** Pound of Flesh  
**Description:** +1 Damage.
Gain +1 Damage when you kill an enemy.  
**Source:** `armor_sets.gon`  

```
PoundOfFlesh {
        name "ARMOR_POUNDOFFLESH_NAME"
        desc "ARMOR_POUNDOFFLESH_DESC"
        rarity rare
        kind neck
        frame 48
        set Meat

        passives {
            DamageUp 1
            StatusOnKillEnemy {
                DamageUp 1
            }
        }
    }
```

---

### `PoundOfFlesh_Cursed`
**Source:** `armor_sets.gon`  

```
PoundOfFlesh_Cursed {
        variant_of PoundOfFlesh
        cursed true
    }
```

---

### `FecalMask`
**Name:** Fecal Mask  
**Description:** Poisonous 1.  
**Source:** `armor_sets.gon`  

```
FecalMask {
        name "ARMOR_FECALMASK_NAME"
        desc "ARMOR_FECALMASK_DESC"
        rarity common
        kind face
        frame 60
        set Fecal

        cha -1

        passives {
            PoisonThorns 1
        }
    }
```

---

### `FecalHood`
**Name:** Fecal Hood  
**Description:** Poisonous 1.  
**Source:** `armor_sets.gon`  

```
FecalHood {
        name "ARMOR_FECALHOOD_NAME"
        desc "ARMOR_FECALHOOD_DESC"
        rarity common
        kind head
        frame 57
        set Fecal

        cha -1

        passives {
            PoisonThorns 1
        }
    }
```

---

### `FecalNecklace`
**Name:** Fecal Necklace  
**Description:** Poisonous 1.  
**Source:** `armor_sets.gon`  

```
FecalNecklace {
        name "ARMOR_FECALNECKLACE_NAME"
        desc "ARMOR_FECALNECKLACE_DESC"
        rarity common
        kind neck
        frame 52
        set Fecal

        cha -1

        passives {
            PoisonThorns 1
        }
    }
```

---

### `FecalMask_Cursed`
**Source:** `armor_sets.gon`  

```
FecalMask_Cursed {
        variant_of FecalMask
        cursed true
    }
```

---

### `FecalHood_Cursed`
**Source:** `armor_sets.gon`  

```
FecalHood_Cursed {
        variant_of FecalHood
        cursed true
    }
```

---

### `FecalNecklace_Cursed`
**Source:** `armor_sets.gon`  

```
FecalNecklace_Cursed {
        variant_of FecalNecklace
        cursed true
    }
```

---

### `LeafyMask`
**Name:** Leafy Mask  
**Description:** While standing in tall grass, you have +40% Dodge Chance.  
**Source:** `armor_sets.gon`  

```
LeafyMask {
        name "ARMOR_LEAFYMASK_NAME"
        desc "ARMOR_LEAFYMASK_DESC"
        rarity common
        kind face
        frame 70
        set Leafy

        cha 1

        passives {
            PassiveWhenOnTile {
                tile [TallGrassTile TallFlowerTile]
                passives {
                    DodgeChance_Status 40
                }
            }
        }
    }
```

---

### `LeafyHat`
**Name:** Leafy Hat  
**Description:** While standing in tall grass, you have +3 Mana Regen and +1 Health Regen.  
**Source:** `armor_sets.gon`  

```
LeafyHat {
        name "ARMOR_LEAFYHAT_NAME"
        desc "ARMOR_LEAFYHAT_DESC"
        rarity common
        kind head
        frame 68
        set Leafy

        cha 1

        passives {
            PassiveWhenOnTile {
                tile [TallGrassTile TallFlowerTile]
                passives {
                    AddManaRegen 3
                    HealthRegenUp 1
                }
            }
        }
    }
```

---

### `LeafyNecklace`
**Name:** Leafy Necklace  
**Description:** While standing in tall grass, you have +3 Health Regen and +1 Mana Regen.  
**Source:** `armor_sets.gon`  

```
LeafyNecklace {
        name "ARMOR_LEAFYNECKLACE_NAME"
        desc "ARMOR_LEAFYNECKLACE_DESC"
        rarity common
        kind neck
        frame 56
        set Leafy

        cha 1

        passives {
            PassiveWhenOnTile {
                tile [TallGrassTile TallFlowerTile]
                passives {
                    AddManaRegen 1
                    HealthRegenUp 3
                }
            }
        }
    }
```

---

### `CactusMask`
**Name:** Cactus Mask  
**Description:** +3 Thorns, Brittle.
Gain +2 [img:con] permanently and heal 10 HP when this breaks.  
**Source:** `armor_sets.gon`  

```
CactusMask {
        name "ARMOR_CACTUSMASK_NAME"
        desc "ARMOR_CACTUSMASK_DESC"
        rarity uncommon
        kind face
        frame 74
        set Cactus

        passives {
            Thorns 3
            Brittle 1
            StatusOnBreak {
                PermanentConstitution 2
                HealthGain 10
                ChangeTilesUnder WaterTile
            }
        }
    }
```

---

### `CactusHat`
**Name:** Cactus Hat  
**Description:** +3 Thorns, Brittle.
Gain +2 [img:con] permanently and heal 10 HP when this breaks.  
**Source:** `armor_sets.gon`  

```
CactusHat {
        name "ARMOR_CACTUSHAT_NAME"
        desc "ARMOR_CACTUSHAT_DESC"
        rarity uncommon
        kind head
        frame 72
        set Cactus

        passives {
            Thorns 3
            Brittle 1
            StatusOnBreak {
                PermanentConstitution 2
                HealthGain 10
                ChangeTilesUnder WaterTile
            }
        }
    }
```

---

### `CactusNecklace`
**Name:** Cactus Necklace  
**Description:** +3 Thorns, Brittle.
Gain +2 [img:con] permanently and heal 10 HP when this breaks.  
**Source:** `armor_sets.gon`  

```
CactusNecklace {
        name "ARMOR_CACTUSNECKLACE_NAME"
        desc "ARMOR_CACTUSNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 58
        set Cactus

        passives {
            Thorns 3
            Brittle 1
            StatusOnBreak {
                PermanentConstitution 2
                HealthGain 10
                ChangeTilesUnder WaterTile
            }
        }
    }
```

---

### `FaceWrap`
**Name:** Face Wrap  
**Description:** +1 Health Regen.
When downed, revive with 15% HP at the end of the round.  
**Source:** `armor_sets.gon`  

```
FaceWrap {
        name ARMOR_FACEWRAP_NAME
        desc ARMOR_FACEWRAP_DESC
        rarity uncommon
        kind face
        frame 76
        set Mummy
        passives {
            HealthRegenUp 1
            DelayedAutoRevive {
                rounds 1
                health 15%
            }
        }
    }
```

---

### `HeadWrap`
**Name:** Head Wrap  
**Description:** +1 Health Regen.
When downed, revive with 15% HP at the end of the round.  
**Source:** `armor_sets.gon`  

```
HeadWrap {
        name ARMOR_HEADWRAP_NAME
        desc ARMOR_HEADWRAP_DESC
        rarity uncommon
        kind head
        frame 74
        set Mummy
        passives {
            HealthRegenUp 1
            DelayedAutoRevive {
                rounds 1
                health 15%
            }
        }
    }
```

---

### `NeckWrap`
**Name:** Neck Wrap  
**Description:** +1 Health Regen.
When downed, revive with 15% HP at the end of the round.  
**Source:** `armor_sets.gon`  

```
NeckWrap {
        name ARMOR_NECKWRAP_NAME
        desc ARMOR_NECKWRAP_DESC
        rarity uncommon
        kind neck
        frame 60
        set Mummy
        passives {
            HealthRegenUp 1
            DelayedAutoRevive {
                rounds 1
                health 15%
            }
        }
    }
```

---

### `ManGlasses`
**Name:** Man's Glasses  
**Description:** Physical attacks can't miss.
Spawn 1-2 extra pickups at the start of each battle.  
**Source:** `armor_sets.gon`  

```
ManGlasses {
        name ARMOR_MANGLASSES_NAME
        desc ARMOR_MANGLASSES_DESC
        rarity uncommon
        kind face
        frame 77
        set Man

        passives {
            TrueShot 1
            SpawnExtraThingsOnBattleStart {
                object RandomPickup
                number [1 2]
            }
        }
    }
```

---

### `ManHair`
**Name:** Man's Hairpiece  
**Description:** ARMOR_MANHAIR_DESC  
**Source:** `armor_sets.gon`  

```
ManHair {
        name ARMOR_MANHAIR_NAME
        desc ARMOR_MANHAIR_DESC
        rarity uncommon
        kind head
        frame 75
        set Man

        cha 2

        passives {
        }
    }
```

---

### `ManTie`
**Name:** Man's Tie  
**Description:** ARMOR_MANTIE_DESC  
**Source:** `armor_sets.gon`  

```
ManTie {
        name ARMOR_MANTIE_NAME
        desc ARMOR_MANTIE_DESC
        rarity uncommon
        kind neck
        frame 61
        set Man

        lck 2

        passives {
        }
    }
```

---

### `FlowerMask`
**Name:** Flower Mask  
**Description:** Your basic attack has a +5% chance to inflict Entangled.
Plants flowers on each tile you move through.
\[s:.7\](Stacking this effect plants flowers in a wider area.)\[/s\]  
**Source:** `armor_sets.gon`  

```
FlowerMask {//todo needs rework
        name ARMOR_FLOWERMASK_NAME
        desc ARMOR_FLOWERMASK_DESC
        rarity uncommon
        kind face
        frame 78
        set Flower

        passives {
            StackingFlowerTrail {
                stacks 1
                stack_key FLOWER_SET
            }
            AddStatusToBasicAttack {
                Tangled [1, .05]
            }
        }
    }
```

---

### `FlowerHat`
**Name:** Flower Hat  
**Description:** Your basic attack has a +5% chance to inflict Entangled.
Plants flowers on each tile you move through.
\[s:.7\](Stacking this effect plants flowers in a wider area.)\[/s\]  
**Source:** `armor_sets.gon`  

```
FlowerHat {
        name ARMOR_FLOWERHAT_NAME
        desc ARMOR_FLOWERHAT_DESC
        rarity uncommon
        kind head
        frame 76
        set Flower

        passives {
            StackingFlowerTrail {
                stacks 1
                stack_key FLOWER_SET
            }
            AddStatusToBasicAttack {
                Tangled [1, .05]
            }
        }
    }
```

---

### `FlowerNecklace`
**Name:** Flower Necklace  
**Description:** Your basic attack has a +5% chance to inflict Entangled.
Plants flowers on each tile you move through.
\[s:.7\](Stacking this effect plants flowers in a wider area.)\[/s\]  
**Source:** `armor_sets.gon`  

```
FlowerNecklace {
        name ARMOR_FLOWERNECKLACE_NAME
        desc ARMOR_FLOWERNECKLACE_DESC
        rarity uncommon
        kind neck
        frame 62
        set Flower

        passives {
            StackingFlowerTrail {
                stacks 1
                stack_key FLOWER_SET
            }
            AddStatusToBasicAttack {
                Tangled [1, .05]
            }
        }
    }
```

---

### `HumanFleshMask`
**Name:** Human Face  
**Description:** Your basic attack has a +25% chance to inflict Fear.
Spawn a food pickup at the start of each battle.  
**Source:** `armor_sets.gon`  

```
HumanFleshMask {
        name ARMOR_HUMANFLESHMASK_NAME
        desc ARMOR_HUMANFLESHMASK_DESC
        rarity rare
        kind face
        frame 79
        set HumanFlesh

        cha -1
        con 2

        passives {
            AddStatusToBasicAttack {
                Fear [1, .25]
            }
            SpawnOnBattleStart {
                object Food
            }
        }
    }
```

---

### `HumanFleshHat`
**Name:** Human Scalp  
**Description:** Your crit hits inflict Fear.
Spawn a food pickup at the start of each battle.  
**Source:** `armor_sets.gon`  

```
HumanFleshHat {
        name ARMOR_HUMANFLESHHAT_NAME
        desc ARMOR_HUMANFLESHHAT_DESC
        rarity rare
        kind head
        frame 77
        set HumanFlesh

        cha -1
        str 2

        passives {
            CritsApplyStatus {
                Fear 1
            }
            SpawnOnBattleStart {
                object Food
            }
        }
    }
```

---

### `HumanFleshArmor`
**Name:** Human Hide  
**Description:** Units that contact or attack you have a +25% chance to be Feared.
Spawn a food pickup at the start of each battle.  
**Source:** `armor_sets.gon`  

```
HumanFleshArmor {
        name ARMOR_HUMANFLESHARMOR_NAME
        desc ARMOR_HUMANFLESHARMOR_DESC
        rarity rare
        kind neck
        frame 63
        set HumanFlesh
		
		cha -1
		lck 2

        passives {
            RevengeDamage {
                effects {
                    Fear [1, .25]
                }
            }
            SpawnOnBattleStart {
                object Food
            }
        }
    }
```

---

### `TentacleMask`
**Name:** Face Tentacle  
**Description:** Your basic attack has a +33% chance to inflict Entangle.  
**Source:** `armor_sets.gon`  

```
TentacleMask {
        name ARMOR_TENTACLEMASK_NAME
        desc ARMOR_TENTACLEMASK_DESC
        rarity uncommon
        kind face
        frame 80
        set Tentacle

        shield 2

        passives {
            AddStatusToBasicAttack {
                Tangled [1, .33]
            }
        }
    }
```

---

### `TentacleHat`
**Name:** Head Tentacle  
**Description:** Your basic attack pulls you towards units or objects it hits.  
**Source:** `armor_sets.gon`  

```
TentacleHat {
        name ARMOR_TENTACLEHAT_NAME
        desc ARMOR_TENTACLEHAT_DESC
        rarity uncommon
        kind head
        frame 78
        set Tentacle

        shield 2

        passives {
            AddStatusToBasicAttack {
                PullSourceToTarget 1
            }
        }
    }
```

---

### `TentacleNeck`
**Name:** Back Tentacles  
**Description:** Counterattack ranged attackers with a tentacle slap.  
**Source:** `armor_sets.gon`  

```
TentacleNeck {
        name ARMOR_TENTACLENECK_NAME
        desc ARMOR_TENTACLENECK_DESC
        rarity uncommon
        kind neck
        frame 64
        set Tentacle

        shield 2

        passives {
            CounterAttack {
                ranged_only true
                ability neck_TentacleArmorCounter
            }
        }
    }
```

---

### `ObeliskMask`
**Name:** Obelisk Jewel  
**Description:** Gain +2 [img:int] and +2 [img:cha] when you kill a unit.
Stats obtained this way are lost when you take damage.  
**Source:** `armor_sets.gon`  

```
ObeliskMask {
        name ARMOR_OBELISKMASK_NAME
        desc ARMOR_OBELISKMASK_DESC
        rarity rare
        kind face
        frame 81
        set Obelisk

        divine_shield 1

        passives {
            StatusOnKill {
                BrittleIntelligenceUp 2
                BrittleCharismaUp 2
            }
        }
    }
```

---

### `ObeliskHat`
**Name:** Obelisk Helmet  
**Description:** Gain +2 [img:dex] and +2 [img:lck] when you kill a unit.
Stats obtained this way are lost when you take damage.  
**Source:** `armor_sets.gon`  

```
ObeliskHat {
        name ARMOR_OBELISKHAT_NAME
        desc ARMOR_OBELISKHAT_DESC
        rarity rare
        kind head
        frame 79
        set Obelisk

        divine_shield 1
        
        passives {
            StatusOnKill {
                BrittleDexterityUp 2
                BrittleLuckUp 2
            }
        }
    }
```

---

### `ObeliskArmor`
**Name:** Obelisk Pauldrons  
**Description:** Gain +2 [img:str], +2 [img:spd] and +2 [img:con] when you kill a unit.
Stats obtained this way are lost when you take damage.  
**Source:** `armor_sets.gon`  

```
ObeliskArmor {
        name ARMOR_OBELISKARMOR_NAME
        desc ARMOR_OBELISKARMOR_DESC
        rarity rare
        kind neck
        frame 65
        set Obelisk

        divine_shield 1
        
        passives {
            StatusOnKill {
                BrittleStrengthUp 2
                BrittleSpeedUp 2
                BrittleConstitutionUp 2
            }
        }
    }
```

---

### `ExperimentalMask`
**Name:** Experimental Treatment  
**Description:** ARMOR_EXPERIMENTALMASK_DESC  
**Source:** `armor_sets.gon`  

```
ExperimentalMask {
        name ARMOR_EXPERIMENTALMASK_NAME
        desc ARMOR_EXPERIMENTALMASK_DESC
        rarity common
        kind face
        frame 82
        set Experimental

        str_aux_initialize random_seed

        passives {
            RandomSeededStatModifier [2 -1] // hard coded in SpawnDatabase::get_item_stats
        }
    }
```

---

### `ExperimentalHat`
**Name:** Experimental Treatment  
**Description:** ARMOR_EXPERIMENTALHAT_DESC  
**Source:** `armor_sets.gon`  

```
ExperimentalHat {
        name ARMOR_EXPERIMENTALHAT_NAME
        desc ARMOR_EXPERIMENTALHAT_DESC
        rarity common
        kind head
        frame 80
        set Experimental

        str_aux_initialize random_seed

        passives {
            RandomSeededStatModifier [2 -1] // hard coded in SpawnDatabase::get_item_stats
        }
    }
```

---

### `ExperimentalNeck`
**Name:** Experimental Treatment  
**Description:** ARMOR_EXPERIMENTALNECK_DESC  
**Source:** `armor_sets.gon`  

```
ExperimentalNeck {
        name ARMOR_EXPERIMENTALNECK_NAME
        desc ARMOR_EXPERIMENTALNECK_DESC
        rarity common
        kind neck
        frame 66
        set Experimental

        str_aux_initialize random_seed

        passives {
            RandomSeededStatModifier [2 -1] // hard coded in SpawnDatabase::get_item_stats
        }
    }
```

---

### `RockyMask`
**Name:** Rocky Mask  
**Description:** Breaks when [img:shield] is depleted.
When this breaks, gain Bruise 3.  
**Source:** `armor_sets.gon`  

```
RockyMask {
        name ARMOR_ROCKYMASK_NAME
        desc ARMOR_ROCKYMASK_DESC
        rarity uncommon
        kind face
        frame 83
        set Rock

        shield 10

        passives {
            RockyArmorPassive 1
            StatusOnBreak {
                Bruise 3
            }
        }
    }
```

---

### `RockyHat`
**Name:** Rocky Hat  
**Description:** Breaks when [img:shield] is depleted.
When this breaks, gain Bruise 3.  
**Source:** `armor_sets.gon`  

```
RockyHat {
        name ARMOR_ROCKYHAT_NAME
        desc ARMOR_ROCKYHAT_DESC
        rarity uncommon
        kind head
        frame 81
        set Rock

        shield 10

        passives {
            RockyArmorPassive 1
            StatusOnBreak {
                Bruise 3
            }
        }
    }
```

---

### `RockyNecklace`
**Name:** Rocky Necklace  
**Description:** Breaks when [img:shield] is depleted.
When this breaks, gain Bruise 3.  
**Source:** `armor_sets.gon`  

```
RockyNecklace {
        name ARMOR_ROCKYNECKLACE_NAME
        desc ARMOR_ROCKYNECKLACE_DESC
        rarity uncommon
        kind neck
        frame 67
        set Rock
        
        shield 10

        passives {
            RockyArmorPassive 1
            StatusOnBreak {
                Bruise 3
            }
        }
    }
```

---

### `SpaceHelmet`
**Name:** Space Helmet  
**Description:** +1 Brace.
30% chance to block negative status effects.  
**Source:** `armor_sets.gon`  

```
SpaceHelmet {
        name ARMOR_SPACEHELMET_NAME
        desc ARMOR_SPACEHELMET_DESC
        rarity uncommon
        kind face
        frame 84
        set Space

        passives {
            Brace 1
            BlockNegativeStatus 30%
        }
    }
```

---

### `SpaceAntenna`
**Name:** Space Antenna  
**Description:** Gain 0-4 mana at start of each turn.  
**Source:** `armor_sets.gon`  

```
SpaceAntenna {
        name ARMOR_SPACEANTENNA_NAME
        desc ARMOR_SPACEANTENNA_DESC
        rarity uncommon
        kind head
        frame 82
        set Space

		shield 3

        passives {
            Metal 1
            StatusEachTurnBegin {
                ManaGainRange {
                    min 0
                    max 4
                }
            }
        }
    }
```

---

### `SpaceBoosters`
**Name:** Space Boosters  
**Description:** Your movement action is Jump.  
**Source:** `armor_sets.gon`  

```
SpaceBoosters {
        name ARMOR_SPACEBOOSTERS_NAME
        desc ARMOR_SPACEBOOSTERS_DESC
        rarity uncommon
        kind neck
        frame 68
        set Space
		
		spd 3

        passives {
            Metal 1
            ReplaceBasicMove BasicJump
        }
    }
```

---

### `TinyPlanet`
**Name:** Tiny Planet  
**Description:** Your basic attack pulls units towards you.
Inflict Bruise on units who contact you.  
**Source:** `armor_sets.gon`  

```
TinyPlanet {
        name ARMOR_TINYPLANET_NAME
        desc ARMOR_TINYPLANET_DESC
        rarity uncommon
        kind face
        frame 85
        set Planet

        shield 1
        int -1

        passives {
            MakeBasicAttackPull 1
            MeleeRevengeDamage {
                effects {
                    Bruise 1
                }
            }
        }
    }
```

---

### `MiniMoon`
**Name:** Mini Moon  
**Description:** Your basic attack has a +25% chance to shoot an asteroid at what it hits.
+10% chance to Block.  
**Source:** `armor_sets.gon`  

```
MiniMoon {
        name ARMOR_MINIMOON_NAME
        desc ARMOR_MINIMOON_DESC
        rarity uncommon
        kind head
        frame 83
        set Planet

        passives {
            ChanceToBlock 10%
            AddStatusToBasicAttack {
                ForceUseAbilityOnTarget {
                    chance 25%
                    ability head_MiniMoonArmorAsteroid
                }
            }
        }
    }
```

---

### `AsteroidBelt`
**Name:** Asteroid Belt  
**Description:** +2 Brace.
+10% chance to block damage.  
**Source:** `armor_sets.gon`  

```
AsteroidBelt {
        name ARMOR_ASTEROIDBELT_NAME
        desc ARMOR_ASTEROIDBELT_DESC
        rarity uncommon
        kind neck
        frame 69
        set Planet

        passives {
            Brace 2
            ChanceToBlock 10%
        }
    }
```

---

### `DebrisMask`
**Name:** Debris Mask  
**Description:** +2 range, +1 Kinetic Spikes.  
**Source:** `armor_sets.gon`  

```
DebrisMask {//todo: instea of passivce kenetic spikes maybe just shoot them end of turn so its unique.
        name ARMOR_DEBRISMASK_NAME
        desc ARMOR_DEBRISMASK_DESC
        rarity common
        kind face
        frame 86
        set Debris

        shield 2
        dex -1

        passives {
            Metal 1
            AddBonusRange 2
            KineticSpikes 1
        }
    }
```

---

### `DebrisHat`
**Name:** Debris Hat  
**Description:** +2 range, +1 Kinetic Spikes.  
**Source:** `armor_sets.gon`  

```
DebrisHat {
        name ARMOR_DEBRISHAT_NAME
        desc ARMOR_DEBRISHAT_DESC
        rarity common
        kind head
        frame 84
        set Debris

        shield 2
        dex -1

        passives {
            Metal 1
            AddBonusRange 2
            KineticSpikes 1
        }
    }
```

---

### `DebrisArmor`
**Name:** Debris Armor  
**Description:** +2 range, +1 Kinetic Spikes.  
**Source:** `armor_sets.gon`  

```
DebrisArmor {
        name ARMOR_DEBRISARMOR_NAME
        desc ARMOR_DEBRISARMOR_DESC
        rarity common
        kind neck
        frame 70
        set Debris

        shield 2
        dex -1

        passives {
            Metal 1
            AddBonusRange 2
            KineticSpikes 1
        }
    }
```

---

### `DryBoneMask`
**Name:** Dry Bone Mask  
**Description:** +1 Thorns.
Inflict Bruise 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
DryBoneMask {
        name ARMOR_DRYBONEMASK_NAME
        desc ARMOR_DRYBONEMASK_DESC
        rarity uncommon
        kind face
        frame 87
        set Bone

        shield 3

        passives {
            Thorns 1
            MeleeRevengeDamage {
                effects {
                    Bruise 1
                }
            }
        }
    }
```

---

### `DryBoneHat`
**Name:** Dry Bone Helm  
**Description:** +1 Thorns.
Inflict Bruise 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
DryBoneHat {
        name ARMOR_DRYBONEHAT_NAME
        desc ARMOR_DRYBONEHAT_DESC
        rarity uncommon
        kind head
        frame 85
        set Bone

        shield 3

        passives {
            Thorns 1
            MeleeRevengeDamage {
                effects {
                    Bruise 1
                }
            }
        }
    }
```

---

### `DryBoneNecklace`
**Name:** Dry Bone Necklace  
**Description:** +1 Thorns.
Inflict Bruise 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
DryBoneNecklace {
        name ARMOR_DRYBONENECKLACE_NAME
        desc ARMOR_DRYBONENECKLACE_DESC
        rarity uncommon
        kind neck
        frame 71
        set Bone

        shield 3

        passives {
            Thorns 1
            MeleeRevengeDamage {
                effects {
                    Bruise 1
                }
            }
        }
    }
```

---

### `ProtectionTransmitter`
**Name:** Protection Transmitter  
**Description:** Bruise 2.
All allies gain Brace 1.  
**Source:** `armor_sets.gon`  

```
ProtectionTransmitter {
        name "ARMOR_PROTECTIONTRANSMITTER_NAME"
        desc "ARMOR_PROTECTIONTRANSMITTER_DESC"
        rarity rare
        kind head
        frame 148
        set Transmitter

        passives {
            Metal 1
            Bruise 2
            StatusAlliesOnBattleStart {
                Brace 1
            }
        }
    }
```

---

### `DamageTransmitter`
**Name:** Damage Transmitter  
**Description:** -2 Damage.
All allies gain +1 Damage.  
**Source:** `armor_sets.gon`  

```
DamageTransmitter {
        name "ARMOR_DAMAGETRANSMITTER_NAME"
        desc "ARMOR_DAMAGETRANSMITTER_DESC"
        rarity rare
        kind neck
        frame 98
        set Transmitter

        passives {
            Metal 1
            DamageUp -2
            StatusAlliesOnBattleStart {
                DamageUp 1
            }
        }
    }
```

---

### `EnergyTransmitter`
**Name:** Energy Transmitter  
**Description:** All allies gain +2 [img:spd].  
**Source:** `armor_sets.gon`  

```
EnergyTransmitter {
        name "ARMOR_ENERGYTRANSMITTER_NAME"
        desc "ARMOR_ENERGYTRANSMITTER_DESC"
        rarity rare
        kind face
        frame 133
        set Transmitter

        spd -4

        passives {
            Metal 1
            StatusAlliesOnBattleStart {
                SpeedUp 2
            }
        }
    }
```

---

### `ThrummingCirclet`
**Name:** Thrumming Circlet  
**Description:** If you end your turn without using your basic attack, gain +1 Damage and +1 Thorns.  
**Source:** `armor_sets.gon`  

```
ThrummingCirclet {
        name "ARMOR_THRUMMINGCIRCLET_NAME"
        desc "ARMOR_THRUMMINGCIRCLET_DESC"
        rarity rare
        kind head
        frame 149
        set Thrumming

        passives {
            StatusOnTurnEndIfDidntCastAbilityTypes {
                type attack
                DamageUp 1
                Thorns 1
            }
        }
    }
```

---

### `ThrummingSpectacles`
**Name:** Thrumming Spectacles  
**Description:** If you end your turn without using your movement action, gain +1 Health Regen and +1 [img:shield].  
**Source:** `armor_sets.gon`  

```
ThrummingSpectacles {
        name "ARMOR_THRUMMINGSPECTACLES_NAME"
        desc "ARMOR_THRUMMINGSPECTACLES_DESC"
        rarity rare
        kind face
        frame 134
        set Thrumming

        passives {
            StatusOnTurnEndIfDidntCastAbilityTypes {
                type move
                HealthRegenUp 1
                Shield 1
            }
        }
    }
```

---

### `ThrummingCharm`
**Name:** Thrumming Charm  
**Description:** If you end your turn without casting any spells, gain +1 Magic Damage and +1 Charge.  
**Source:** `armor_sets.gon`  

```
ThrummingCharm {
        name "ARMOR_THRUMMINGCHARM_NAME"
        desc "ARMOR_THRUMMINGCHARM_DESC"
        rarity rare
        kind neck
        frame 124
        set Thrumming

        passives {
            StatusOnTurnEndIfDidntCastAbilityTypes {
                type spell
                SpellDamageUp 1
                Charge 1
            }
        }
    }
```

---

### `WitchesHat`
**Name:** Witch's Hat  
**Description:** +1 Magic Damage.  
**Source:** `armor_sets.gon`  

```
WitchesHat {
        name "ARMOR_WITCHESHAT_NAME"
        desc "ARMOR_WITCHESHAT_DESC"
        rarity rare
        kind head
        frame 146
        set Witch

        passives {
            SpellDamageUp 1
        }
    }
```

---

### `WitchesNose`
**Name:** Witch's Nose  
**Description:** +1 Magic Damage.  
**Source:** `armor_sets.gon`  

```
WitchesNose {
        name "ARMOR_WITCHESNOSE_NAME"
        desc "ARMOR_WITCHESNOSE_DESC"
        rarity rare
        kind face
        frame 131
        set Witch
        
        passives {
            SpellDamageUp 1
        }
    }
```

---

### `WitchesCape`
**Name:** Witch's Cape  
**Description:** +1 Magic Damage.  
**Source:** `armor_sets.gon`  

```
WitchesCape {
        name "ARMOR_WITCHESCAPE_NAME"
        desc "ARMOR_WITCHESCAPE_DESC"
        rarity rare
        kind neck
        frame 122
        set Witch

        passives {
            SpellDamageUp 1
        }
    }
```

---

### `StunningHaircut`
**Name:** Stunning Haircut  
**Description:** Your face and neck item effects are doubled.  
**Source:** `armor_sets.gon`  

```
StunningHaircut {
        name "ARMOR_STUNNINGHAIRCUT_NAME"
        desc "ARMOR_STUNNINGHAIRCUT_DESC"
        rarity very_rare
        kind head
        frame 152
        set Stunning

        passives {
            FaceArmorPassiveMultiplierBonus 1
            NeckArmorPassiveMultiplierBonus 1
        }
    }
```

---

### `StunningChain`
**Name:** Stunning Chain  
**Description:** Your head and face item effects are doubled.  
**Source:** `armor_sets.gon`  

```
StunningChain {
        name "ARMOR_STUNNINGCHAIN_NAME"
        desc "ARMOR_STUNNINGCHAIN_DESC"
        rarity very_rare
        kind neck
        frame 136
        set Stunning

        passives {
            Metal 1
            FaceArmorPassiveMultiplierBonus 1
            HeadArmorPassiveMultiplierBonus 1
        }
    }
```

---

### `StunningBeard`
**Name:** Stunning Beard  
**Description:** Your head and neck item effects are doubled.  
**Source:** `armor_sets.gon`  

```
StunningBeard {
        name "ARMOR_STUNNINGBEARD_NAME"
        desc "ARMOR_STUNNINGBEARD_DESC"
        rarity very_rare
        kind face
        frame 137
        set Stunning

        passives {
            NeckArmorPassiveMultiplierBonus 1
            HeadArmorPassiveMultiplierBonus 1
        }
    }
```

---

### `SuperheroHat`
**Name:** Superhero Hat  
**Description:** +2 Health Regen.  
**Source:** `armor_sets.gon`  

```
SuperheroHat {
        name "ARMOR_SUPERHEROHAT_NAME"
        desc "ARMOR_SUPERHEROHAT_DESC"
        rarity rare
        kind head
        frame 154
        set Superhero

        divine_shield 1

        passives {
            HealthRegenUp 2
        }
    }
```

---

### `SuperheroCape`
**Name:** Superhero Cape  
**Description:** Flying.  
**Source:** `armor_sets.gon`  

```
SuperheroCape {
        name "ARMOR_SUPERHEROCAPE_NAME"
        desc "ARMOR_SUPERHEROCAPE_DESC"
        rarity rare
        kind neck
        frame 130
        set Superhero

        spd 3

        passives {
            Flying 1
        }
    }
```

---

### `SuperheroMask`
**Name:** Superhero Mask  
**Description:** +1 Damage. Your basic attack knocks units into the air, lobbing them back 3 tiles.  
**Source:** `armor_sets.gon`  

```
SuperheroMask {
        name "ARMOR_SUPERHEROMASK_NAME"
        desc "ARMOR_SUPERHEROMASK_DESC"
        rarity rare
        kind face
        frame 139
        set Superhero

        passives {
            DamageUp 1
            
		    AddStatusToBasicAttack {
                KnockUpAndAway {
                    stacks 5
                    distance 3
                }
            }
        }
    }
```

---

### `LeadHelmet`
**Name:** Lead Helmet  
**Description:** ARMOR_LEADHELMET_DESC  
**Source:** `armor_sets.gon`  

```
LeadHelmet {
        name "ARMOR_LEADHELMET_NAME"
        desc "ARMOR_LEADHELMET_DESC"
        rarity uncommon
        kind head
        frame 156
        set Lead
        
        shield 6
        spd -1

        passives {
            Metal 1
        }
    }
```

---

### `LeadShoulderPads`
**Name:** Lead Shoulder Pads  
**Description:** ARMOR_LEADSHOULDERPADS_DESC  
**Source:** `armor_sets.gon`  

```
LeadShoulderPads {
        name "ARMOR_LEADSHOULDERPADS_NAME"
        desc "ARMOR_LEADSHOULDERPADS_DESC"
        rarity uncommon
        kind neck
        frame 129
        set Lead

        shield 6
        spd -1

        passives {
            Metal 1
        }
    }
```

---

### `LeadMask`
**Name:** Lead Mask  
**Description:** ARMOR_LEADMASK_DESC  
**Source:** `armor_sets.gon`  

```
LeadMask {
        name "ARMOR_LEADMASK_NAME"
        desc "ARMOR_LEADMASK_DESC"
        rarity uncommon
        kind face
        frame 141
        set Lead

        shield 6
        spd -1

        passives {
            Metal 1
        }
    }
```

---

### `ScaryBaby`
**Name:** Scary Baby  
**Description:** Inflict Fear 2 on a random enemy at the start of each battle.  
**Source:** `armor_sets.gon`  

```
ScaryBaby {
        name "ARMOR_SCARYBABY_NAME"
        desc "ARMOR_SCARYBABY_DESC"
        rarity rare
        kind face
        frame 180
        set Baby

        passives {
            StatusRandomEnemiesOnBattleStart {
                count 1
                Fear 2
            }
        }
    }
```

---

### `CharmingBaby`
**Name:** Charming Baby  
**Description:** Inflict Charmed 2 on a random enemy at the start of each battle.  
**Source:** `armor_sets.gon`  

```
CharmingBaby {
        name "ARMOR_CHARMINGBABY_NAME"
        desc "ARMOR_CHARMINGBABY_DESC"
        rarity rare
        kind head
        frame 188
        set Baby

        passives {
            StatusRandomEnemiesOnBattleStart {
                count 1
                Charmed 2
            }
        }
    }
```

---

### `FreezingBaby`
**Name:** Freezing Baby  
**Description:** Inflict Freeze 2 on a random enemy at the start of each battle.  
**Source:** `armor_sets.gon`  

```
FreezingBaby {
        name "ARMOR_FREEZINGBABY_NAME"
        desc "ARMOR_FREEZINGBABY_DESC"
        rarity rare
        kind neck
        frame 166
        set Baby

        passives {
            StatusRandomEnemiesOnBattleStart {
                count 1
                Freeze 2
            }
        }
    }
```

---

### `Obi`
**Name:** Obi  
**Description:** Start battle with +2 bonus moves.  
**Source:** `armor_sets.gon`  

```
Obi {
        name "ARMOR_OBI_NAME"
        desc "ARMOR_OBI_DESC"
        rarity uncommon
        kind neck
        frame 148
        set Ninja

        passives {
            MoveQuivered 2
        }
    }
```

---

### `Fukumen`
**Name:** Fukumen  
**Description:** Counter the first 2 attacks you receive each battle.  
**Source:** `armor_sets.gon`  

```
Fukumen {
        name "ARMOR_FUKUMEN_NAME"
        desc "ARMOR_FUKUMEN_DESC"
        rarity uncommon
        kind face
        frame 175
        set Ninja

        passives {
            CounterNextAttacks 2
        }
    }
```

---

### `Zukin`
**Name:** Zukin  
**Description:** Start battle with +2 Backflip.  
**Source:** `armor_sets.gon`  

```
Zukin {
        name "ARMOR_ZUKIN_NAME"
        desc "ARMOR_ZUKIN_DESC"
        rarity uncommon
        kind head
        frame 184
        set Ninja

        passives {
            BackflipWhenTargeted {
                stacks 2
                ability BackflipDodge
            }
        }
    }
```

---

### `ProwlersCap`
**Name:** Prowler's Cap  
**Description:** Backstabs have +25% Crit Chance.  
**Source:** `armor_sets.gon`  

```
ProwlersCap {
        name "ARMOR_PROWLERSCAP_NAME"
        desc "ARMOR_PROWLERSCAP_DESC"
        rarity uncommon
        kind head
        frame 186
        set Prowler

        passives {
            BackstabCritChance .25
        }
    }
```

---

### `ProwlersMask`
**Name:** Prowler's Mask  
**Description:** Backstabs inflict Bleed 1.  
**Source:** `armor_sets.gon`  

```
ProwlersMask {
        name "ARMOR_PROWLERSMASK_NAME"
        desc "ARMOR_PROWLERSMASK_DESC"
        rarity uncommon
        kind face
        frame 177
        set Prowler

        passives {
            AddStatusToBackstabs {
                Bleed 1
            }
        }
    }
```

---

### `ProwlersVial`
**Name:** Prowler's Vial  
**Description:** Backstabs heal you by 2 HP.  
**Source:** `armor_sets.gon`  

```
ProwlersVial {
        name "ARMOR_PROWLERSVIAL_NAME"
        desc "ARMOR_PROWLERSVIAL_DESC"
        rarity uncommon
        kind neck
        frame 164
        set Prowler

        passives {
            StatusOnBackstab {
                HealthGain 2
            }
        }
    }
```

---

### `MageHat`
**Name:** Mage's Hat  
**Description:** Gain +1 Charge each time you cast a spell.  
**Source:** `armor_sets.gon`  

```
MageHat {
        name "ARMOR_MAGEHAT_NAME"
        desc "ARMOR_MAGEHAT_DESC"
        rarity rare
        kind head
        frame 101
        set Mage
        
        int 1
        
        passives {
            StatusOnCastSpell {
                Charge 1
            }
        }
    }
```

---

### `MageRobe`
**Name:** Mage's Robe  
**Description:** Gain +1 Charge when you deal damage with your basic attack.  
**Source:** `armor_sets.gon`  

```
MageRobe {
        name "ARMOR_MAGEROBE_NAME"
        desc "ARMOR_MAGEROBE_DESC"
        rarity rare
        kind face
        frame 101
        set Mage

        int 1
        
        passives {
            AddStatusToBasicAttack {
                ApplyToSource {
                    Charge 1
                }
            }
        }
    }
```

---

### `MageScarf`
**Name:** Mage's Scarf  
**Description:** Gain +1 Charge each time an enemy dies.  
**Source:** `armor_sets.gon`  

```
MageScarf {
        name "ARMOR_MAGESCARF_NAME"
        desc "ARMOR_MAGESCARF_DESC"
        rarity rare
        kind neck
        frame 101
        set Mage

        int 1
        
        passives {
            StatusOnEnemyDeath {
                Charge 1
            }
        }
    }
```

---

### `ThiefHood`
**Name:** Thief's Hood  
**Description:** +5% Dodge Chance and +5% Crit Chance.
Your basic attack inflicts Bleed.  
**Source:** `armor_sets.gon`  

```
ThiefHood {
        name "ARMOR_THIEFHOOD_NAME"
        desc "ARMOR_THIEFHOOD_DESC"
        rarity rare
        kind head
        frame 102
        set Thief
        
        passives {
            ArmorDodgeChance 5%
            CritChanceUp 5
            AddStatusToBasicAttack {
                Bleed 1
            }
        }
    }
```

---

### `ThiefTattoo`
**Name:** Thief's Tattoo  
**Description:** +5% Dodge Chance and +5% Crit Chance.
Your basic attack inflicts Poison.  
**Source:** `armor_sets.gon`  

```
ThiefTattoo {
        name "ARMOR_THIEFTATTOO_NAME"
        desc "ARMOR_THIEFTATTOO_DESC"
        rarity rare
        kind face
        frame 102
        set Thief

        passives {
            ArmorDodgeChance 5%
            CritChanceUp 5
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }
```

---

### `ThiefCloak`
**Name:** Thief's Cloak  
**Description:** +10% Dodge Chance and +10% Crit Chance.  
**Source:** `armor_sets.gon`  

```
ThiefCloak {
        name "ARMOR_THIEFCLOAK_NAME"
        desc "ARMOR_THIEFCLOAK_DESC"
        rarity rare
        kind neck
        frame 102
        set Thief
        
        passives {
            ArmorDodgeChance 10%
            CritChanceUp 10
        }
    }
```

---

### `FighterHelm`
**Name:** Fighter's Helm  
**Description:** +15% chance to refresh your basic attack, movement, weapon and trinket actions when you get a kill.  
**Source:** `armor_sets.gon`  

```
FighterHelm {
        name "ARMOR_FIGHTERHELM_NAME"
        desc "ARMOR_FIGHTERHELM_DESC"
        rarity rare
        kind head
        frame 103
        set Fighter
        
        shield 2

        passives {
            Metal 1
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

### `FighterScar`
**Name:** Fighter's Scar  
**Description:** +15% chance to refresh your basic attack, movement, weapon and trinket actions when you get a kill.  
**Source:** `armor_sets.gon`  

```
FighterScar {
        name "ARMOR_FIGHTERSCAR_NAME"
        desc "ARMOR_FIGHTERSCAR_DESC"
        rarity rare
        kind face
        frame 103
        set Fighter
        
        shield 2

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

### `FighterShoulderPad`
**Name:** Fighter's Shoulder Pad  
**Description:** +15% chance to refresh your basic attack, movement, weapon and trinket actions when you get a kill.  
**Source:** `armor_sets.gon`  

```
FighterShoulderPad {
        name "ARMOR_FIGHTERSHOULDERPAD_NAME"
        desc "ARMOR_FIGHTERSHOULDERPAD_DESC"
        rarity rare
        kind neck
        frame 103
        set Fighter
        
        shield 2

        passives {
            Metal 1
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

### `ClericHat`
**Name:** Cleric's Mitre  
**Description:** Your heals heal for 2 extra.  
**Source:** `armor_sets.gon`  

```
ClericHat {
        name "ARMOR_CLERICHAT_NAME"
        desc "ARMOR_CLERICHAT_DESC"
        rarity rare
        kind head
        frame 104
        set Cleric
        
        shield 2

        passives {
            BoostHeals 2
        }
    }
```

---

### `ClericTears`
**Name:** Cleric's Tears  
**Description:** Gain +1 [img:divineshield] each time an ally is downed.  
**Source:** `armor_sets.gon`  

```
ClericTears {
        name "ARMOR_CLERICTEARS_NAME"
        desc "ARMOR_CLERICTEARS_DESC"
        rarity rare
        kind face
        frame 104
        set Cleric
        
        divine_shield 1

        passives {
            StatusOnAllyCatDeath {
                DivineShield 1
            }
        }
    }
```

---

### `ClericRelic`
**Name:** Cleric's Relic  
**Description:** +1 Brace.
+15% chance to inflict Fear on units that contact or attack you.  
**Source:** `armor_sets.gon`  

```
ClericRelic {
        name "ARMOR_CLERICRELIC_NAME"
        desc "ARMOR_CLERICRELIC_DESC"
        rarity rare
        kind neck
        frame 104
        set Cleric
        
        passives {
            Brace 1
            RevengeDamage {
                effects {
                    Fear [1, .15]
                }
            }
        }
    }
```

---

### `TankHelmet`
**Name:** Tank's Helmet  
**Description:** +1 Knockback damage.  
**Source:** `armor_sets.gon`  

```
TankHelmet {
        name "ARMOR_TANKHELMET_NAME"
        desc "ARMOR_TANKHELMET_DESC"
        rarity rare
        kind head
        frame 105
        set Tank
        
        shield 1

        passives {
            Metal 1
            AddKnockbackDamage 1
        }
    }
```

---

### `TankTattoo`
**Name:** Tank's Tattoo  
**Description:** All Knockback inflicted by you is increased by 2.  
**Source:** `armor_sets.gon`  

```
TankTattoo {
        name "ARMOR_TANKTATTOO_NAME"
        desc "ARMOR_TANKTATTOO_DESC"
        rarity rare
        kind face
        frame 105
        set Tank
        
        passives {
            AmplifyKnockback 2
        }
    }
```

---

### `TankPads`
**Name:** Tank's Pads  
**Description:** Your knockback damage has a +10% chance to inflict Stun.  
**Source:** `armor_sets.gon`  

```
TankPads {
        name "ARMOR_TANKPADS_NAME"
        desc "ARMOR_TANKPADS_DESC"
        rarity rare
        kind neck
        frame 105
        set Tank
        
        shield 2

        passives {
            Metal 1
            AddStatusToKnockbackDamage {
                Stun [1, .1]
            }
        }
    }
```

---

### `HunterCap`
**Name:** Hunter's Cap  
**Description:** Your familiars gain All Stats Up.  
**Source:** `armor_sets.gon`  

```
HunterCap {
        name "ARMOR_HUNTERCAP_NAME"
        desc "ARMOR_HUNTERCAP_DESC"
        rarity rare
        kind head
        frame 106
        set Hunter

        lck 1
        
        passives {
            AddPassivesToMinions {
                AllStatsUp 1
                HealthGain 4
            }
            AddPassivesToCharmed {
                AllStatsUp 1
            }
        }
    }
```

---

### `HunterMonocle`
**Name:** Hunter's Monocle  
**Description:** +2 range.  
**Source:** `armor_sets.gon`  

```
HunterMonocle {
        name "ARMOR_HUNTERMONOCLE_NAME"
        desc "ARMOR_HUNTERMONOCLE_DESC"
        rarity rare
        kind face
        frame 106
        set Hunter
        
        passives {
            AddBonusRange 2
        }
    }
```

---

### `HunterQuiver`
**Name:** Hunter's Quiver  
**Description:** Start each battle with 2 bonus attacks.  
**Source:** `armor_sets.gon`  

```
HunterQuiver {
        name "ARMOR_HUNTERQUIVER_NAME"
        desc "ARMOR_HUNTERQUIVER_DESC"
        rarity rare
        kind neck
        frame 106
        set [Hunter, Leather]
        
        passives {
            Quivered 2
        }
    }
```

---

### `MysticEye`
**Name:** Mystic Eye  
**Description:** +25% chance to reflect projectiles. Your tile-targeted spells have +2 range.  
**Source:** `armor_sets.gon`  

```
MysticEye {
        name ARMOR_MYSTICEYE_NAME
        desc ARMOR_MYSTICEYE_DESC
        rarity rare
        kind face
        frame 107
        set Psychic

        passives {
            IncreaseSpellRange 2
            ReflectProjectiles 25%
        }
    }
```

---

### `TinfoilHat`
**Name:** Tinfoil Hat  
**Description:** You are immune to Charm, Madness, Fear and Confusion.  
**Source:** `armor_sets.gon`  

```
TinfoilHat {
        name ARMOR_TINFOILHAT_NAME
        desc ARMOR_TINFOILHAT_DESC
        rarity rare
        kind head
        frame 107
        set [Psychic, Scrap]

        shield 2

        passives {
            Metal 1
            CharmImmunity 1 // this covers Charm, Madness and other charm-like effects
            StatusImmunity [Fear Confusion PermanentConfusion]
        }
    }
```

---

### `DivinersCloth`
**Name:** Diviner's Cloth  
**Description:** Adjacent allies have +25% Dodge Chance.
Give +1 Charge to all adjacent allies at the end of your turn.  
**Source:** `armor_sets.gon`  

```
DivinersCloth {
        name ARMOR_DIVINERSCLOTH_NAME
        desc ARMOR_DIVINERSCLOTH_DESC
        rarity rare
        kind neck
        frame 107
        set [Psychic, Rag]

        passives {
            StatusAlliesEachTurn {
                Conditional_Adjacent {
                    Conditional_PlayerCat {
                        Charge 1
                    }
                }
            }
            AllyDodgeChanceAura {
                chance 25%
                range 1
            }
        }
    }
```

---

### `DeathMask`
**Name:** Death Mask  
**Description:** Get downed at the start of each battle, then revive at the end of the first round with full HP and +2 [img:shield].  
**Source:** `armor_sets.gon`  

```
DeathMask {
        name ARMOR_DEATHMASK_NAME
        desc ARMOR_DEATHMASK_DESC
        rarity rare
        kind face
        frame 108
        set Necromancer

        passives {
            StatusOnBattleStart {
                SafeDie 1
                ReviveNextRound {
                    revive_health 100%
                    Shield 2
                }
            }
        }
    }
```

---

### `SpiderHat`
**Name:** Spider Hat  
**Description:** When you destroy a corpse, spawn 2 Spiderlings.  
**Source:** `armor_sets.gon`  

```
SpiderHat {
        name ARMOR_SPIDERHAT_NAME
        desc ARMOR_SPIDERHAT_DESC
        rarity rare
        kind head
        frame 108
        set Necromancer
        passives {
            SpawnObjectOnPopCorpse {
                object CharmedTinySpider
                count 2
                except_tiny true
            }
        }
    }
```

---

### `LeechNecklace`
**Name:** Leech Necklace  
**Description:** Your spells inflict Leech 1 against enemies.  
**Source:** `armor_sets.gon`  

```
LeechNecklace {
        name ARMOR_LEECHNECKLACE_NAME
        desc ARMOR_LEECHNECKLACE_DESC
        rarity rare
        kind neck
        frame 108
        set [Necromancer, Leech]

        passives {
            AddStatusToSpells {
                Conditional_Enemy {
                    Leeches 1
                }
            }
        }
    }
```

---

### `FaceBrand`
**Name:** Face Brand  
**Description:** Each time you use your basic attack, gain +1 [img:shield].
\[s:.7\](This counts as an empty armor slot.)\[/s\]  
**Source:** `armor_sets.gon`  

```
FaceBrand {
        name ARMOR_FACEBRAND_NAME
        desc ARMOR_FACEBRAND_DESC
        rarity rare
        kind face
        frame 109
        set Monk
        weightless true

        passives {
            AddSelfStatusToBasicAttack {
                Shield 1
            }
        }
    }
```

---

### `HeadBrand`
**Name:** Head Brand  
**Description:** Your movement action is Jump.
If you land on a unit, deal 1 damage to it and bounce to an adjacent tile.
\[s:.7\](This counts as an empty armor slot.)\[/s\]  
**Source:** `armor_sets.gon`  

```
HeadBrand {
        name ARMOR_HEADBRAND_NAME
        desc ARMOR_HEADBRAND_DESC
        rarity rare
        kind head
        frame 109
        set Monk
        weightless true

        passives {
            ReplaceBasicMove head_HeadBrandJump
        }
    }
```

---

### `PrayerBeads`
**Name:** Prayer Beads  
**Description:** Each time you take damage, gain +3 Brace until your next turn.
\[s:.7\](This counts as an empty armor slot.)\[/s\]  
**Source:** `armor_sets.gon`  

```
PrayerBeads {
        name ARMOR_PRAYERBEADS_NAME
        desc ARMOR_PRAYERBEADS_DESC
        rarity rare
        kind neck
        frame 109
        set [Monk, Twine]
        weightless true

        passives {
            StatusOnTookDamage {
                Temporary {
                    status Brace
                    stacks 3
                    turns 1
                    expires_on_begin_turn true
                }
            }
        }
    }
```

---

### `ScrappersMask`
**Name:** Scrapper's Mask  
**Description:** When you break an item, gain +3 [img:shield].  
**Source:** `armor_sets.gon`  

```
ScrappersMask {
        name ARMOR_SCRAPPERSMASK_NAME
        desc ARMOR_SCRAPPERSMASK_DESC
        rarity rare
        kind face
        frame 110
        set [Tinkerer, Scrap]

        shield 3

        passives {
            Metal 1
            StatusOnBreakItem {
                Shield 3
            }
        }
    }
```

---

### `ScrappersHat`
**Name:** Scrapper's Hat  
**Description:** When you break an item, spawn 3 random pickups.  
**Source:** `armor_sets.gon`  

```
ScrappersHat {
        name ARMOR_SCRAPPERSHAT_NAME
        desc ARMOR_SCRAPPERSHAT_DESC
        rarity rare
        kind head
        frame 110
        set [Tinkerer, Scrap]

        shield 3

        passives {
            Metal 1
            StatusOnBreakItem {
                DoDamage {
                    damage 0
                    type spell
                    damage_tiles all

                    effects {
                        BounceObject RandomPickup
                        BounceObject RandomPickup
                        BounceObject RandomPickup
                    }
                }
            }
        }
    }
```

---

### `ScrappersBackpack`
**Name:** Scrapper's Backpack  
**Description:** When you break an item, recover it at the end of the battle with 1 durability.
\[s:.7\](Excludes temporary items)\[/s\]  
**Source:** `armor_sets.gon`  

```
ScrappersBackpack {
        name ARMOR_SCRAPPERSBACKPACK_NAME
        desc ARMOR_SCRAPPERSBACKPACK_DESC
        rarity rare
        kind neck
        frame 110
        set [Tinkerer, Survivalist]

        passives {
            ReclaimItemOnBreak 1
        }
    }
```

---

### `IronJaw`
**Name:** Iron Jaw  
**Description:** Counterattack melee attackers with a bite that deals 3 damage with Lifesteal.  
**Source:** `armor_sets.gon`  

```
IronJaw {
        name ARMOR_IRONJAW_NAME
        desc ARMOR_IRONJAW_DESC
        rarity rare
        kind face
        frame 111
        set [Butcher, Tinkerer]

        shield 3

        passives {
            Metal 1
            CounterAttack {
                ability head_IronJaw
            }
        }
    }
```

---

### `FleshShroud`
**Name:** Flesh Shroud  
**Description:** Gain +1 [img:shield] each time you heal.
When you kill a unit or destroy a corpse, it becomes meat.  
**Source:** `armor_sets.gon`  

```
FleshShroud {
        name ARMOR_FLESHSHROUD_NAME
        desc ARMOR_FLESHSHROUD_DESC
        rarity rare
        kind head
        frame 111
        set [Butcher, HumanFlesh]

        passives {
            KillsToMeat Food
            StatusOnHealed {
                Shield 1
            }
        }
    }
```

---

### `HookedNecklace`
**Name:** Hooked Necklace  
**Description:** +2 Thorns. Cleave units that contact you.  
**Source:** `armor_sets.gon`  

```
HookedNecklace {
        name ARMOR_HOOKEDNECKLACE_NAME
        desc ARMOR_HOOKEDNECKLACE_DESC
        rarity rare
        kind neck
        frame 111
        set Butcher

        shield 2

        passives {
            Metal 1
            Thorns 2
            MeleeRevengeDamage {
                effects {
                    Cleave 1
                }
            }
        }
    }
```

---

### `GreenmanMask`
**Name:** Greenman Mask  
**Description:** +3 Brace while standing in tall grass.
+3 Mana Regen while standing in water.  
**Source:** `armor_sets.gon`  

```
GreenmanMask {
        name ARMOR_GREENMANMASK_NAME
        desc ARMOR_GREENMANMASK_DESC
        rarity rare
        kind face
        frame 112
        set [Druid, Leafy]

        passives {
            PassiveWhenOnTile {
                tile [TallGrassTile TallFlowerTile]
                passives {
                    Brace 3
                }
            }
            PassiveWhenOnTile {
                tile [WaterTile]
                passives {
                    AddManaRegen 3
                }
            }
        }
    }
```

---

### `MushroomHat`
**Name:** Mushroom Hat  
**Description:** Inflict Confusion 2 on units that contact or attack you.
Familiars you spawn inflict Confusion.  
**Source:** `armor_sets.gon`  

```
MushroomHat {
        name ARMOR_MUSHROOMHAT_NAME
        desc ARMOR_MUSHROOMHAT_DESC
        rarity rare
        kind head
        frame 112
        set Druid

        passives {
            RevengeDamage {
                effects {
                    Confusion 2
                }
            }
            AddPassivesToMinions {
                AddStatusToBasicAttack {
                    Confusion 1
                }
            }
        }
    }
```

---

### `RingOfMushrooms`
**Name:** Ring of Mushrooms  
**Description:** All of your area abilities gain +1 area.  
**Source:** `armor_sets.gon`  

```
RingOfMushrooms {
        name ARMOR_RINGOFMUSHROOMS_NAME
        desc ARMOR_RINGOFMUSHROOMS_DESC
        rarity rare
        kind neck
        frame 112
        set [Druid, Twine]

        passives {
            AOEBonus 1
        }
    }
```

---

### `CatWhiskers`
**Name:** Ordinary Whiskers  
**Description:** ARMOR_CATWHISKERS_DESC  
**Source:** `armor_sets.gon`  

```
CatWhiskers {
        name ARMOR_CATWHISKERS_NAME
        desc ARMOR_CATWHISKERS_DESC
        rarity rare
        kind face
        frame 119
        set Collarless
        
        str 1
        dex 1
        int 1
        con 1
        spd 1
        lck 1
        cha 1

        passives {
        }
    }
```

---

### `CatEars`
**Name:** Normal Ears  
**Description:** ARMOR_CATEARS_DESC  
**Source:** `armor_sets.gon`  

```
CatEars {
        name ARMOR_CATEARS_NAME
        desc ARMOR_CATEARS_DESC
        rarity rare
        kind head
        frame 132
        set Collarless

        str 1
        dex 1
        int 1
        con 1
        spd 1
        lck 1
        cha 1

        passives {
        }
    }
```

---

### `CatCollar`
**Name:** Mundane Collar  
**Description:** ARMOR_CATCOLLAR_DESC  
**Source:** `armor_sets.gon`  

```
CatCollar {
        name ARMOR_CATCOLLAR_NAME
        desc ARMOR_CATCOLLAR_DESC
        rarity rare
        kind neck
        frame 87
        set [Collarless, Leather]

        str 1
        dex 1
        int 1
        con 1
        spd 1
        lck 1
        cha 1

        passives {
        }
    }
```

---

### `ClownMakeup`
**Name:** Clown Makeup  
**Description:** Triple the effects of your Head armor.  
**Source:** `armor_sets.gon`  

```
ClownMakeup {
        name "ARMOR_CLOWNMAKEUP_NAME"
        desc "ARMOR_CLOWNMAKEUP_DESC"
        rarity very_rare
        kind face
        frame 171
        set Jester
        
        lck -3

        passives {
            HeadArmorPassiveMultiplierBonus 2
        }
    }
```

---

### `CapAndBells`
**Name:** Cap and Bells  
**Description:** Triple the effects of your Trinket.  
**Source:** `armor_sets.gon`  

```
CapAndBells {
        name "ARMOR_CAPANDBELLS_NAME"
        desc "ARMOR_CAPANDBELLS_DESC"
        rarity very_rare
        kind head
        frame 180
        set Jester

        lck -3

        passives {
            TrinketPassiveMultiplierBonus 2
            TrinketActiveEffectsMultiplierBonus 2
        }
    }
```

---

### `Ruffle`
**Name:** Ruffle  
**Description:** Triple the effects of your Face armor.  
**Source:** `armor_sets.gon`  

```
Ruffle {
        name "ARMOR_RUFFLE_NAME"
        desc "ARMOR_RUFFLE_DESC"
        rarity very_rare
        kind neck
        frame 163
        set Jester
        
        lck -3

        passives {
            FaceArmorPassiveMultiplierBonus 2
        }
    }
```

---

### `FeatheredVeil`
**Name:** Feathered Veil  
**Description:** Counterattack melee attackers.  
**Source:** `armor_sets.gon`  

```
FeatheredVeil {
        name "ARMOR_FEATHEREDVEIL_NAME"
        desc "ARMOR_FEATHEREDVEIL_DESC"
        rarity rare
        kind face
        frame 92
        set Feathered

        passives {
            CounterAttack {
                melee_only true
                ability attack
            }
        }
    }
```

---

### `FeatheredCap`
**Name:** Feathered Cap  
**Description:** ARMOR_FEATHEREDCAP_DESC  
**Source:** `armor_sets.gon`  

```
FeatheredCap {
        name "ARMOR_FEATHEREDCAP_NAME"
        desc "ARMOR_FEATHEREDCAP_DESC"
        rarity uncommon
        kind head
        frame 89
        set Feathered

        spd 4

        passives {
        }
    }
```

---

### `FeatheredNecklace`
**Name:** Feathered Necklace  
**Description:** +15% Dodge Chance.  
**Source:** `armor_sets.gon`  

```
FeatheredNecklace {
        name "ARMOR_FEATHEREDNECKLACE_NAME"
        desc "ARMOR_FEATHEREDNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 75
        set Feathered

        passives {
            ArmorDodgeChance 15%
        }
    }
```

---

### `TheMind`
**Name:** The Mind  
**Description:** ARMOR_THEMIND_DESC  
**Source:** `armor_sets.gon`  

```
TheMind {
        name "ARMOR_THEMIND_NAME"
        desc "ARMOR_THEMIND_DESC"
        rarity very_rare
        kind head
        frame 205
        set Godhead

        int 7

    }
```

---

### `TheBody`
**Name:** The Body  
**Description:** ARMOR_THEBODY_DESC  
**Source:** `armor_sets.gon`  

```
TheBody {
        name "ARMOR_THEBODY_NAME"
        desc "ARMOR_THEBODY_DESC"
        rarity very_rare
        kind face
        frame 193
        set Godhead

        con 7
    }
```

---

### `TheSoul`
**Name:** The Soul  
**Description:** ARMOR_THESOUL_DESC  
**Source:** `armor_sets.gon`  

```
TheSoul {
        name "ARMOR_THESOUL_NAME"
        desc "ARMOR_THESOUL_DESC"
        rarity very_rare
        kind neck
        frame 177
        set Godhead

        lck 7
    }
```

---

### `BrickHat`
**Name:** Brick Hat  
**Description:** Inflict Bruise 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
BrickHat {
        name "ARMOR_BRICKHAT_NAME"
        desc "ARMOR_BRICKHAT_DESC"
        rarity common
        kind head
        frame 122
        set Brick
	
		shield 4
		spd -1
		
		passives {
			MeleeRevengeDamage {
				effects {
					Bruise 1
				}
			}
		}
    }
```

---

### `BrickMask`
**Name:** Brick Mask  
**Description:** Inflict Bruise 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
BrickMask {
        name "ARMOR_BRICKMASK_NAME"
        desc "ARMOR_BRICKMASK_DESC"
        rarity common
        kind face
        frame 124
        set Brick
		
		shield 4
		spd -1
		
		passives {
			MeleeRevengeDamage {
				effects {
					Bruise 1
				}
			}
		}
    }
```

---

### `BrickNecklace`
**Name:** Brick Necklace  
**Description:** Inflict Bruise 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
BrickNecklace {
        name "ARMOR_BRICKNECKLACE_NAME"
        desc "ARMOR_BRICKNECKLACE_DESC"
        rarity common
        kind neck
        frame 113
        set Brick
		
		shield 4
		spd -1
		
		passives {
			MeleeRevengeDamage {
				effects {
					Bruise 1
				}
			}
		}
    }
```

---

### `SlimyHat`
**Name:** Slimy Hat  
**Description:** +15% chance to catch projectiles. Inflict Immobile 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
SlimyHat {
        name "ARMOR_SLIMYHAT_NAME"
        desc "ARMOR_SLIMYHAT_DESC"
        rarity uncommon
        kind head
        frame 123
        set Slimy

        keyword_tooltips {Immobile 1}
		
		cha -1
		passives {
			CatchProjectiles {
				chance 15%
				ally_chance 15%
				Quivered 1
            }
			MeleeRevengeDamage {
				effects {
					Immobile 1
				}
			}
		}
    }
```

---

### `SlimyMask`
**Name:** Slimy Mask  
**Description:** +15% chance to catch projectiles. Inflict Immobile 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
SlimyMask {
        name "ARMOR_SLIMYMASK_NAME"
        desc "ARMOR_SLIMYMASK_DESC"
        rarity uncommon
        kind face
        frame 125
        set Slimy
		
		cha -1
		passives {
			CatchProjectiles {
				chance 15%
				ally_chance 15%
				Quivered 1
            }
			MeleeRevengeDamage {
				effects {
					Immobile 1
				}
			}
		}
    }
```

---

### `SlimyNecklace`
**Name:** Slimy Necklace  
**Description:** +15% chance to catch projectiles. Inflict Immobile 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
SlimyNecklace {
        name "ARMOR_SLIMYNECKLACE_NAME"
        desc "ARMOR_SLIMYNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 114
        set Slimy
		
		cha -1
		passives {
			CatchProjectiles {
				chance 15%
				ally_chance 15%
				Quivered 1
            }
			MeleeRevengeDamage {
				effects {
					Immobile 1
				}
			}
		}
    }
```

---

### `RatHat`
**Name:** Rat Hat  
**Description:** Start battle with a Charmed Pinky.  
**Source:** `armor_sets.gon`  

```
RatHat {
        name "ARMOR_RATHAT_NAME"
        desc "ARMOR_RATHAT_DESC"
        rarity common
        kind head
        frame 124
        set Rat
		passives {
			SpawnOnBattleStart {
				object CharmedPinky 
				number 1
			}
		}
    }
```

---

### `RatMask`
**Name:** Rat Mask  
**Description:** Start battle with a Charmed Pinky.  
**Source:** `armor_sets.gon`  

```
RatMask {
        name "ARMOR_RATMASK_NAME"
        desc "ARMOR_RATMASK_DESC"
        rarity common
        kind face
        frame 126
        set Rat

		passives {
			SpawnOnBattleStart {
				object CharmedPinky 
				number 1
			}
		}
    }
```

---

### `RatNecklace`
**Name:** Rat Necklace  
**Description:** Start battle with a Charmed Pinky.  
**Source:** `armor_sets.gon`  

```
RatNecklace {
        name "ARMOR_RATNECKLACE_NAME"
        desc "ARMOR_RATNECKLACE_DESC"
        rarity common
        kind neck
        frame 115
        set Rat

		passives {
			SpawnOnBattleStart {
				object CharmedPinky 
				number 1
			}
		}
    }
```

---

### `CarapaceHat`
**Name:** Carapace Hat  
**Description:** Cleanse 1 stack of a random negative status effect when you end your turn.  
**Source:** `armor_sets.gon`  

```
CarapaceHat {
        name "ARMOR_CARAPACEHAT_NAME"
        desc "ARMOR_CARAPACEHAT_DESC"
        rarity uncommon
        kind head
        frame 73
        set Carapace
		
		shield 4
		
		passives {
			StatusEachTurnEnd {
				PartialCleanse 1 
			}
		}
    }
```

---

### `CarapaceMask`
**Name:** Carapace Mask  
**Description:** Cleanse 1 stack of a random negative status effect when you end your turn.  
**Source:** `armor_sets.gon`  

```
CarapaceMask {
        name "ARMOR_CARAPACEMASK_NAME"
        desc "ARMOR_CARAPACEMASK_DESC"
        rarity uncommon
        kind face
        frame 75
        set Carapace
		
		shield 4
		
		passives {
			StatusEachTurnEnd {
				PartialCleanse 1
			}
		}
    }
```

---

### `CarapaceNecklace`
**Name:** Carapace Necklace  
**Description:** Cleanse 1 stack of a random negative status effect when you end your turn.  
**Source:** `armor_sets.gon`  

```
CarapaceNecklace {
        name "ARMOR_CARAPACENECKLACE_NAME"
        desc "ARMOR_CARAPACENECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 59
        set Carapace
		
		shield 4
		
		passives {
			StatusEachTurnEnd {
				PartialCleanse 1
			}
		}
    }
```

---

### `RadioactiveHat`
**Name:** Radioactive Hat  
**Description:** Adjacent units get All Stats Down.  
**Source:** `armor_sets.gon`  

```
RadioactiveHat {
        name "ARMOR_RADIOACTIVEHAT_NAME"
        desc "ARMOR_RADIOACTIVEHAT_DESC"
        rarity uncommon
        kind head
        frame 86
        set Radioactive
		
		shield 2
		
		passives {
            Metal 1
			DepressionAura 1
			StatusOnBattleEnd {
				Conditional_GoodRoll {
					RandomMutation 1
					odds 1%
				}	
			}
		}
    }
```

---

### `RadioactiveMask`
**Name:** Radioactive Mask  
**Description:** Adjacent units get All Stats Down.  
**Source:** `armor_sets.gon`  

```
RadioactiveMask {
        name "ARMOR_RADIOACTIVEMASK_NAME"
        desc "ARMOR_RADIOACTIVEMASK_DESC"
        rarity uncommon
        kind face
        frame 88
        set Radioactive
		
		shield 2

		passives {
            Metal 1
			DepressionAura 1
			StatusOnBattleEnd {
				Conditional_GoodRoll {
					RandomMutation 1
					odds 1%
				}	
			}
		}
    }
```

---

### `RadioactiveNecklace`
**Name:** Radioactive Necklace  
**Description:** Adjacent units get All Stats Down.  
**Source:** `armor_sets.gon`  

```
RadioactiveNecklace {
        name "ARMOR_RADIOACTIVENECKLACE_NAME"
        desc "ARMOR_RADIOACTIVENECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 72
        set Radioactive
		
		shield 2

		passives {
            Metal 1
			DepressionAura 1
			StatusOnBattleEnd {
				Conditional_GoodRoll {
					RandomMutation 1
					odds 1%
				}	
			}
		}
    }
```

---

### `MoltenHat`
**Name:** Molten Hat  
**Description:** Start with Burn 2. Your basic attack inflicts Burn 1. Inflict Burn 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
MoltenHat {
        name "ARMOR_MOLTENHAT_NAME"
        desc "ARMOR_MOLTENHAT_DESC"
        rarity uncommon
        kind head
        frame 87
        set Molten
		
		passives {
			Burn 2
			AddStatusToBasicAttack {
				Burn 1
			}
			MeleeRevengeDamage {
				effects {
					Burn 1
				}
			}
		}
	}
```

---

### `MoltenMask`
**Name:** Molten Mask  
**Description:** Start with Burn 2. Your basic attack inflicts Burn 1. Inflict Burn 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
MoltenMask {
        name "ARMOR_MOLTENMASK_NAME"
        desc "ARMOR_MOLTENMASK_DESC"
        rarity uncommon
        kind face
        frame 89
        set Molten

		passives {
			Burn 2
			AddStatusToBasicAttack {
				Burn 1
			}
			MeleeRevengeDamage {
				effects {
					Burn 1
				}
			}
		}
    }
```

---

### `MoltenNecklace`
**Name:** Molten Necklace  
**Description:** Start with Burn 2. Your basic attack inflicts Burn 1. Inflict Burn 1 on units that contact you.  
**Source:** `armor_sets.gon`  

```
MoltenNecklace {
        name "ARMOR_MOLTENNECKLACE_NAME"
        desc "ARMOR_MOLTENNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 73
        set Molten

		passives {
			Burn 2
			AddStatusToBasicAttack {
				Burn 1
	        }
			MeleeRevengeDamage {
				effects {
					Burn 1
				}
			}
		}
    }
```

---

### `MothersHat`
**Name:** Mother's Hat  
**Description:** Spawn a Charmed Tiny Tumor at the start of each battle and whenever you're downed.  
**Source:** `armor_sets.gon`  

```
MothersHat {
        name "ARMOR_MOTHERSHAT_NAME"
        desc "ARMOR_MOTHERSHAT_DESC"
        rarity uncommon
        kind head
        frame 88
        set Mother
		
		passives {
			SpawnThingOnDeath CharmedTinyTumor
			SpawnOnBattleStart {
				object CharmedTinyTumor
				number 1
			}
		}
    }
```

---

### `MothersMask`
**Name:** Mother's Mask  
**Description:** Spawn a Charmed Tiny Tumor at the start of each battle and whenever you're downed.  
**Source:** `armor_sets.gon`  

```
MothersMask {
        name "ARMOR_MOTHERSMASK_NAME"
        desc "ARMOR_MOTHERSMASK_DESC"
        rarity uncommon
        kind face
        frame 90
        set Mother

		passives {
			SpawnThingOnDeath CharmedTinyTumor
			SpawnOnBattleStart {
				object CharmedTinyTumor
				number 1
			}
		}
    }
```

---

### `MothersNecklace`
**Name:** Mother's Necklace  
**Description:** Spawn a Charmed Tiny Tumor at the start of each battle and whenever you're downed.  
**Source:** `armor_sets.gon`  

```
MothersNecklace {
        name "ARMOR_MOTHERSNECKLACE_NAME"
        desc "ARMOR_MOTHERSNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 74
        set Mother

		passives {
			SpawnThingOnDeath CharmedTinyTumor
			SpawnOnBattleStart {
				object CharmedTinyTumor
				number 1
			}
		}
    }
```

---

### `NurseHat`
**Name:** Nurse Hat  
**Description:** +1 Health Regen. Your heals heal for 1 extra.  
**Source:** `armor_sets.gon`  

```
NurseHat {
        name "ARMOR_NURSEHAT_NAME"
        desc "ARMOR_NURSEHAT_DESC"
        rarity common
        kind head
        frame 125
        set Nurse
		
		con 1
		
		passives {
			HealthRegenUp 1
			BoostHeals 1
		}
    }
```

---

### `NurseMask`
**Name:** Nurse Mask  
**Description:** +1 Health Regen. Your heals heal for 1 extra.  
**Source:** `armor_sets.gon`  

```
NurseMask {
        name "ARMOR_NURSEMASK_NAME"
        desc "ARMOR_NURSEMASK_DESC"
        rarity common
        kind face
        frame 127
        set Nurse
		
		con 1
		
		passives {
			HealthRegenUp 1
			BoostHeals 1
		}
    }
```

---

### `NurseNecklace`
**Name:** Nurse Necklace  
**Description:** +1 Health Regen. Your heals heal for 1 extra.  
**Source:** `armor_sets.gon`  

```
NurseNecklace {
        name "ARMOR_NURSENECKLACE_NAME"
        desc "ARMOR_NURSENECKLACE_DESC"
        rarity common
        kind neck
        frame 116
        set Nurse
		
		con 1
		
		passives {
			HealthRegenUp 1
			BoostHeals 1
		}
    }
```

---

### `HybridHat`
**Name:** Hybrid Hat  
**Description:** Start with a bonus move and Bleed 1.  
**Source:** `armor_sets.gon`  

```
HybridHat {
        name "ARMOR_HYBRIDHAT_NAME"
        desc "ARMOR_HYBRIDHAT_DESC"
        rarity common
        kind head
        frame 126
        set Hybrid
		
		passives {
			Bleed 1
			MoveQuivered 1
		}	
    }
```

---

### `HybridMask`
**Name:** Hybrid Mask  
**Description:** Start with a bonus attack and Poison 1.  
**Source:** `armor_sets.gon`  

```
HybridMask {
        name "ARMOR_HYBRIDMASK_NAME"
        desc "ARMOR_HYBRIDMASK_DESC"
        rarity common
        kind face
        frame 128
        set [Hybrid, Rat]

		passives {
			Poison 1
			Quivered 1
		}
    }
```

---

### `HybridNecklace`
**Name:** Hybrid Necklace  
**Description:** Start with +5 Charge and Bruise 1.  
**Source:** `armor_sets.gon`  

```
HybridNecklace {
        name "ARMOR_HYBRIDNECKLACE_NAME"
        desc "ARMOR_HYBRIDNECKLACE_DESC"
        rarity common
        kind neck
        frame 117
        set Hybrid
		
		passives {
			Bruise 1
			Charge 5
		}
    }
```

---

### `FattyHat`
**Name:** Fatty Hat  
**Description:** Brace 1. Your basic attack has +1 Knockback.  
**Source:** `armor_sets.gon`  

```
FattyHat {
        name "ARMOR_FATTYHAT_NAME"
        desc "ARMOR_FATTYHAT_DESC"
        rarity common
        kind head
        frame 116
        set Fatty

		passives {
			Brace 1
			AddStatusToBasicAttack {
				Knockback 1
			}
		}
    }
```

---

### `FattyMask`
**Name:** Fatty Mask  
**Description:** Brace 1. Your basic attack has +1 Knockback.  
**Source:** `armor_sets.gon`  

```
FattyMask {
        name "ARMOR_FATTYMASK_NAME"
        desc "ARMOR_FATTYMASK_DESC"
        rarity common
        kind face
        frame 98
        set Fatty
		
		passives {
			Brace 1
			AddStatusToBasicAttack {
				Knockback 1
			}
		}
    }
```

---

### `FattyNecklace`
**Name:** Fatty Necklace  
**Description:** Brace 1. Your basic attack has +1 Knockback.  
**Source:** `armor_sets.gon`  

```
FattyNecklace {
        name "ARMOR_FATTYNECKLACE_NAME"
        desc "ARMOR_FATTYNECKLACE_DESC"
        rarity common
        kind neck
        frame 80
        set Fatty
		
		passives {
			Brace 1
			AddStatusToBasicAttack {
				Knockback 1
			}
		}
    }
```

---

### `MedicalHat`
**Name:** Medical Hat  
**Description:** All of your stats are increased by 1 for each disorder you have.  
**Source:** `armor_sets.gon`  

```
MedicalHat {
        name "ARMOR_MEDICALHAT_NAME"
        desc "ARMOR_MEDICALHAT_DESC"
        rarity uncommon
        kind head
        frame 117
        set Medical

        passives {
            AllStatsUpPerDisorder 1
        }
    }
```

---

### `MedicalMask`
**Name:** Medical Mask  
**Description:** All of your stats are increased by 1 for each disorder you have.  
**Source:** `armor_sets.gon`  

```
MedicalMask {
        name "ARMOR_MEDICALMASK_NAME"
        desc "ARMOR_MEDICALMASK_DESC"
        rarity uncommon
        kind face
        frame 99
        set Medical

        passives {
            AllStatsUpPerDisorder 1
        }
    }
```

---

### `MedicalNecklace`
**Name:** Medical Necklace  
**Description:** All of your stats are increased by 1 for each disorder you have.  
**Source:** `armor_sets.gon`  

```
MedicalNecklace {
        name "ARMOR_MEDICALNECKLACE_NAME"
        desc "ARMOR_MEDICALNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 81
        set Medical

        passives {
            AllStatsUpPerDisorder 1
        }
    }
```

---

### `OcularChip`
**Name:** Ocular Chip  
**Description:** Your spells cost -1 mana.  
**Source:** `armor_sets.gon`  

```
OcularChip {
        name "ARMOR_OCULARCHIP_NAME"
        desc "ARMOR_OCULARCHIP_DESC"
        rarity uncommon
        kind head
        frame 118
        set Chip
		
		int -1
		cha -1
		
		passives {
			ManaCostReduction 1
		}
    }
```

---

### `CerebralChip`
**Name:** Cerebral Chip  
**Description:** Your spells cost -1 mana.  
**Source:** `armor_sets.gon`  

```
CerebralChip {
        name "ARMOR_CEREBRALCHIP_NAME"
        desc "ARMOR_CEREBRALCHIP_DESC"
        rarity uncommon
        kind face
        frame 114
        set Chip

		int -1
		cha -1
		
		passives {
			ManaCostReduction 1
		}
    }
```

---

### `SpinalChip`
**Name:** Spinal Chip  
**Description:** Your spells cost -1 mana.  
**Source:** `armor_sets.gon`  

```
SpinalChip {
        name "ARMOR_SPINALCHIP_NAME"
        desc "ARMOR_SPINALCHIP_DESC"
        rarity uncommon
        kind neck
        frame 82
        set Chip

		int -1
		cha -1
		
		passives {
			ManaCostReduction 1
		}
    }
```

---

### `DemonicHat`
**Name:** Demonic Hat  
**Description:** +3 Thorns. Trample.
You can no longer heal.  
**Source:** `armor_sets.gon`  

```
DemonicHat {
        name "ARMOR_DEMONICHAT_NAME"
        desc "ARMOR_DEMONICHAT_DESC"
        rarity uncommon
        kind head
        frame 127
        set Demonic

		passives {
			Thorns 3
			Trample 3
            HPGainBlock 1
		}
    }
```

---

### `DemonicMask`
**Name:** Demonic Mask  
**Description:** +3 Bleed Thorns.
Trample. Bleed 3.  
**Source:** `armor_sets.gon`  

```
DemonicMask {
        name "ARMOR_DEMONICMASK_NAME"
        desc "ARMOR_DEMONICMASK_DESC"
        rarity uncommon
        kind face
        frame 129
        set Demonic
		
		passives {
			Bleed 3
			BleedThorns 3
			Trample 3
		}
    }
```

---

### `DemonicNecklace`
**Name:** Demonic Necklace  
**Description:** Bruise 1. When you take damage, gain +2 Damage.  
**Source:** `armor_sets.gon`  

```
DemonicNecklace {
        name "ARMOR_DEMONICNECKLACE_NAME"
        desc "ARMOR_DEMONICNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 118
        set Demonic
		
		passives {
			Bruise 1
            StatusOnTookDamage {
                DamageUp 2
            }
        }
    }
```

---

### `FrozenHat`
**Name:** Frozen Hat  
**Description:** Your basic attack inflicts Slow and has a +10% chance to Freeze units. Units that contact you gain Slow and have a 10% chance to become Frozen.  
**Source:** `armor_sets.gon`  

```
FrozenHat {
        name "ARMOR_FROZENHAT_NAME"
        desc "ARMOR_FROZENHAT_DESC"
        rarity common
        kind head
        frame 128
        set Frozen
		
		shield 1
		
		passives {
			AddStatusToBasicAttack {
				Slow 1
				Conditional_GoodRoll {
					Freeze 1
					odds 10%
				}	
			}
			MeleeRevengeDamage {
				effects {
					Slow 1
					Conditional_GoodRoll {
						Freeze 1
						odds 10%
				    }	
				}
			}
		}
    }
```

---

### `FrozenMask`
**Name:** Frozen Mask  
**Description:** Your basic attack inflicts Slow and has a +10% chance to Freeze units. Units that contact you gain Slow and have a 10% chance to become Frozen.  
**Source:** `armor_sets.gon`  

```
FrozenMask {
        name "ARMOR_FROZENMASK_NAME"
        desc "ARMOR_FROZENMASK_DESC"
        rarity common
        kind face
        frame 130
        set Frozen

		shield 1
		
		passives {
			AddStatusToBasicAttack {
				Slow 1
				Conditional_GoodRoll {
					Freeze 1
					odds 10%
				}	
			}
			MeleeRevengeDamage {
				effects {
					Slow 1
					Conditional_GoodRoll {
						Freeze 1
						odds 10%
				    }	
				}
			}
		}
    }
```

---

### `FrozenNecklace`
**Name:** Frozen Necklace  
**Description:** Your basic attack inflicts Slow and has a +10% chance to Freeze units. Units that contact you gain Slow and have a 10% chance to become Frozen.  
**Source:** `armor_sets.gon`  

```
FrozenNecklace {
        name "ARMOR_FROZENNECKLACE_NAME"
        desc "ARMOR_FROZENNECKLACE_DESC"
        rarity common
        kind neck
        frame 119
        set Frozen
		
		shield 1
		
		passives {
			AddStatusToBasicAttack {
				Slow 1
				Conditional_GoodRoll {
					Freeze 1
					odds 10%
				}	
			}
			MeleeRevengeDamage {
				effects {
					Slow 1
					Conditional_GoodRoll {
						Freeze 1
						odds 10%
				    }	
				}
			}
		}
    }
```

---

### `SaberToothedHat`
**Name:** Sabertooth Hat  
**Description:** +2 Thorns. Ice immunity.  
**Source:** `armor_sets.gon`  

```
SaberToothedHat {
        name "ARMOR_SABERTOOTHEDHAT_NAME"
		desc "ARMOR_SABERTOOTHEDHAT_DESC"
        rarity common
        kind head
        frame 114
        set Wooly

		shield 3

		passives {
			Thorns 2
			ElementImmune Ice
			StatusImmunity [Freeze, Slow]
		}

    }
```

---

### `CavemanBeard`
**Name:** Wooly Beard  
**Description:** Brace 2. Ice immunity.  
**Source:** `armor_sets.gon`  

```
CavemanBeard {
        name "ARMOR_CAVEMANBEARD_NAME"
        desc "ARMOR_CAVEMANBEARD_DESC"
        rarity common
        kind face
        frame 96
        set [Wooly, Caveman]

		shield 3

		passives {
			Brace 2
			ElementImmune Ice
			StatusImmunity [Freeze, Slow]
		}
    }
```

---

### `SaberToothedPelt`
**Name:** Sabertooth Pelt  
**Description:** +2 Health Regen. Ice immunity.  
**Source:** `armor_sets.gon`  

```
SaberToothedPelt {
        name "ARMOR_SABERTOOTHEDPELT_NAME"
        desc "ARMOR_SABERTOOTHEDPELT_DESC"
        rarity common
        kind neck
        frame 78
        set Wooly

		shield 3
	
		passives {
		    HealthRegenUp 2
		    ElementImmune Ice
		    StatusImmunity [Freeze, Slow]
		}
    }
```

---

### `RuneofJera`
**Name:** Rune of Jera  
**Description:** Your trinket effects are doubled.  
**Source:** `armor_sets.gon`  

```
RuneofJera {
        name "ARMOR_RUNEOFJERA_NAME"
        desc "ARMOR_RUNEOFJERA_DESC"
        rarity rare
        kind head
        frame 119
        set Rune
		
		passives {
			TrinketPassiveMultiplierBonus 1
            TrinketActiveEffectsMultiplierBonus 1
		}
    }
```

---

### `RuneofHagalaz`
**Name:** Rune of Hagalaz  
**Description:** Your Weapons hit twice.  
**Source:** `armor_sets.gon`  

```
RuneofHagalaz {
        name "ARMOR_RUNEOFHAGALAZ_NAME"
        desc "ARMOR_RUNEOFHAGALAZ_DESC"
        rarity rare
        kind face
        frame 115
        set Rune

		passives {
			DoubleCastWeapons 1
		}
    }
```

---

### `RuneofPerthro`
**Name:** Rune of Perthro  
**Description:** This item counts for all item sets.  
**Source:** `armor_sets.gon`  

```
RuneofPerthro {
        name "ARMOR_RUNEOFPERTHRO_NAME"
        desc "ARMOR_RUNEOFPERTHRO_DESC"
        rarity rare
        kind neck
        frame 83
        set [Rune *]

		shield 4
    }
```

---

### `CavemanWig`
**Name:** Caveman Wig  
**Description:** Spawn 1-3 Charmed Lice at the start of each battle.  
**Source:** `armor_sets.gon`  

```
CavemanWig {
        name "ARMOR_CAVEMANWIG_NAME"
        desc "ARMOR_CAVEMANWIG_DESC"
        rarity uncommon
        kind head
        frame 115
        set Caveman

		int -1
		str 2
		
		passives {
			SpawnOnBattleStart {
				object CharmedLice
				number [1, 3]
			}
		}
    }
```

---

### `CavemanEyebrows`
**Name:** Caveman Eyebrows  
**Description:** Your weapons deal double damage.  
**Source:** `armor_sets.gon`  

```
CavemanEyebrows {
        name "ARMOR_CAVEMANEYEBROWS_NAME"
        desc "ARMOR_CAVEMANEYEBROWS_DESC"
        rarity uncommon
        kind face
        frame 97
        set Caveman

		int -1
		con 2

		passives {
			WeaponDamageMultiplierBonus 1
		}
    }
```

---

### `CavemanNecklace`
**Name:** Caveman Necklace  
**Description:** +33% crit damage.  
**Source:** `armor_sets.gon`  

```
CavemanNecklace {
        name "ARMOR_CAVEMANNECKLACE_NAME"
        desc "ARMOR_CAVEMANNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 79
        set Caveman

		int -1
		lck 2
		
		passives {
			AddCritMultiplier 33%
		}
    }
```

---

### `DinoHat`
**Name:** Dino Hat  
**Description:** Allies gain +1 [img:str] at the start of each battle.  
**Source:** `armor_sets.gon`  

```
DinoHat { //TODO: these should be an aura and not a "at the start of combat" thing
        name "ARMOR_DINOHAT_NAME"
        desc "ARMOR_DINOHAT_DESC"
        rarity uncommon
        kind head
        frame 131
        set [Dino, Bone]

		int -1
		
		shield 5
		
		passives {
            StatusAlliesOnBattleStart {
                StrengthUp 1
            }
        }
    }
```

---

### `DinoMask`
**Name:** Dino Mask  
**Description:** Allies gain +1 [img:con] at the start of each battle.  
**Source:** `armor_sets.gon`  

```
DinoMask { //TODO: these should be an aura and not a "at the start of combat" thing
        name "ARMOR_DINOMASK_NAME"
        desc "ARMOR_DINOMASK_DESC"
        rarity uncommon
        kind face
        frame 118
        set [Dino, Bone]
		
		int -1
		
		shield 5
		
		passives {
            StatusAlliesOnBattleStart {
                ConstitutionUp 1
            }
        }
    }
```

---

### `DinoNecklace`
**Name:** Dino Necklace  
**Description:** Allies gain +1 [img:spd] at the start of each battle.  
**Source:** `armor_sets.gon`  

```
DinoNecklace { //TODO: these should be an aura and not a "at the start of combat" thing
        name "ARMOR_DINONECKLACE_NAME"
        desc "ARMOR_DINONECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 86
        set [Dino, Bone]
		
		int -1
		
		shield 5
		
		passives {
            StatusAlliesOnBattleStart {
                SpeedUp 1
            }
        }
    }
```

---

### `BigRockHat`
**Name:** Big Rock Hat  
**Description:** Brace 2.  
**Source:** `armor_sets.gon`  

```
BigRockHat {
        name "ARMOR_BIGROCKHAT_NAME"
        desc "ARMOR_BIGROCKHAT_DESC"
        rarity uncommon
        kind head
        frame 129
        set Rock
		
		spd -2
		shield 6

		passives {
			Brace 2
		}
    }
```

---

### `BigRockMask`
**Name:** Big Rock Mask  
**Description:** Brace 2.  
**Source:** `armor_sets.gon`  

```
BigRockMask {
        name "ARMOR_BIGROCKMASK_NAME"
        desc "ARMOR_BIGROCKMASK_DESC"
        rarity uncommon
        kind face
        frame 116
        set Rock
		spd -2
		shield 6

		passives {
			Brace 2
		}

    }
```

---

### `BigRockNecklace`
**Name:** Big Rock Necklace  
**Description:** Brace 2.  
**Source:** `armor_sets.gon`  

```
BigRockNecklace {
        name "ARMOR_BIGROCKNECKLACE_NAME"
        desc "ARMOR_BIGROCKNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 84
        set Rock

		spd -2
		shield 6

		passives {
			Brace 2
		}
    }
```

---

### `PhoenixHat`
**Name:** Phoenix Hat  
**Description:** +10% Dodge Chance. Each time you end movement, gain +1 [img:spd] and Charge 2.  
**Source:** `armor_sets.gon`  

```
PhoenixHat {
        name "ARMOR_PHOENIXHAT_NAME"
        desc "ARMOR_PHOENIXHAT_DESC"
        rarity uncommon
        kind head
        frame 130
        set [Phoenix, Feathered]

		passives {
			ArmorDodgeChance 10%
		    StatusOnEndMove {
				SpeedUp 1
				Charge 2
			}
		}
    }
```

---

### `PhoenixMask`
**Name:** Phoenix Mask  
**Description:** +10% Dodge Chance. Each time you end movement, gain +1 [img:spd] and Charge 2.  
**Source:** `armor_sets.gon`  

```
PhoenixMask {
        name "ARMOR_PHOENIXMASK_NAME"
        desc "ARMOR_PHOENIXMASK_DESC"
        rarity uncommon
        kind face
        frame 117
        set [Phoenix, Feathered]

		passives {
			ArmorDodgeChance 10%
		    StatusOnEndMove {
				SpeedUp 1
				Charge 2
			}
		}
    }
```

---

### `PhoenixNecklace`
**Name:** Phoenix Necklace  
**Description:** +10% Dodge Chance. Each time you end movement, gain +1 [img:spd] and Charge 2.  
**Source:** `armor_sets.gon`  

```
PhoenixNecklace {
        name "ARMOR_PHOENIXNECKLACE_NAME"
        desc "ARMOR_PHOENIXNECKLACE_DESC"
        rarity uncommon
        kind neck
        frame 85
        set [Phoenix, Feathered]

		passives {
			ArmorDodgeChance 10%
		    StatusOnEndMove {
				SpeedUp 1
				Charge 2
			}
		}
    }
```

---

### `AncestorsSkull`
**Name:** Ancestor's Skull  
**Description:** - {str_aux_passive_name} -
{str_aux_passive_desc}  
**Source:** `armor_sets.gon`  

```
AncestorsSkull {
        name "ARMOR_ANCESTORSSKULL_NAME"
        desc "ARMOR_ANCESTORSSKULL_DESC"
        rarity rare
        kind head
        frame 171
        set [Ancestor, Bone]
        
        str_aux_initialize random_class_passive
        str_aux_is_copy_passive true
    }
```

---

### `AncestorsJaw`
**Name:** Ancestor's Jaw  
**Description:** - {str_aux_passive_name} -
{str_aux_passive_desc}  
**Source:** `armor_sets.gon`  

```
AncestorsJaw {
        name "ARMOR_ANCESTORSJAW_NAME"
        desc "ARMOR_ANCESTORSJAW_DESC"
        rarity rare
        kind face
        frame 155
        set [Ancestor, Bone]
        
        str_aux_initialize random_class_passive
        str_aux_is_copy_passive true
    }
```

---

### `AncestorsBones`
**Name:** Ancestor's Bones  
**Description:** - {str_aux_passive_name} -
{str_aux_passive_desc}  
**Source:** `armor_sets.gon`  

```
AncestorsBones {
        name "ARMOR_ANCESTORSBONES_NAME"
        desc "ARMOR_ANCESTORSBONES_DESC"
        rarity rare
        kind neck
        frame 141
        set [Ancestor, Bone]
        
        str_aux_initialize random_class_passive
        str_aux_is_copy_passive true
    }
```

---

### `CopycatHat`
**Name:** Copycat Hat  
**Description:** Copies your trinket's passive effects.  
**Source:** `armor_sets.gon`  

```
CopycatHat {
        name "ARMOR_COPYCATHAT_NAME"
        desc "ARMOR_COPYCATHAT_DESC"
        rarity rare
        kind head
        frame 90
        set Copycat

        passives {
            TrinketPassiveMultiplierBonus 1
        }
    }
```

---

### `CopycatMask`
**Name:** Copycat Mask  
**Description:** Copies your trinket's passive effects.  
**Source:** `armor_sets.gon`  

```
CopycatMask {
        name "ARMOR_COPYCATMASK_NAME"
        desc "ARMOR_COPYCATMASK_DESC"
        rarity rare
        kind face
        frame 93
        set Copycat

        passives {
            TrinketPassiveMultiplierBonus 1
        }
    }
```

---

### `CopycatScarf`
**Name:** Copycat Scarf  
**Description:** Copies your trinket's passive effects.  
**Source:** `armor_sets.gon`  

```
CopycatScarf {
        name "ARMOR_COPYCATSCARF_NAME"
        desc "ARMOR_COPYCATSCARF_DESC"
        rarity rare
        kind neck
        frame 76
        set Copycat

        passives {
            TrinketPassiveMultiplierBonus 1
        }
    }
```

---

## File: `beanies_quest_items.gon`

### `PersuasionDevice`
**Name:** Persuasion Device  
**Description:** Side Quest Item. Use to permanently charm a non-boss enemy. It joins your party.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `beanies_quest_items.gon`  

```
PersuasionDevice {
	name "ITEM_PERSUASIONDEVICE_NAME"
    desc "ITEM_PERSUASIONDEVICE_DESC"
    kind weapon
    frame 168
    quest_item true
    rarity sidequest
    quest_reward_item PersuasionDevice_Fixed

    ability wp_PersuasionDevice

    spd -2
}
```

---

### `PersuasionDevice_Fixed`
**Description:** Use to permanently charm a non-boss enemy. It joins your party.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `beanies_quest_items.gon`  

```
PersuasionDevice_Fixed {
    variant_of PersuasionDevice
    desc "ITEM_PERSUASIONDEVICE_FIXED_DESC"
    kind weapon
    frame 169
	rarity rare
    quest_item false
}
```

---

### `ChaosDevice`
**Name:** Chaos Device  
**Description:** Side Quest Item. When any cat levels up they are offered abilities from all classes.  
**Source:** `beanies_quest_items.gon`  

```
ChaosDevice {
    name "ARMOR_CHAOSDEVICE_NAME"
    desc "ARMOR_CHAOSDEVICE_DESC"
    kind head
    frame 160
	set Experimental
    quest_item true
    rarity sidequest
    quest_reward_item ChaosDevice_Fixed

    global_tags [all_cats_are_jester]
}
```

---

### `ChaosDevice_Fixed`
**Name:** Chaos Controller  
**Description:** Abilities from all classes are offered when you level up. You can reroll your levelup options thrice.  
**Source:** `beanies_quest_items.gon`  

```
ChaosDevice_Fixed {
    name "ARMOR_CHAOSDEVICE_FIXED_NAME"
    desc "ARMOR_CHAOSDEVICE_FIXED_DESC"
    kind head
    frame 161
	set Experimental
    rarity rare

    passives {
        LevelUpClassOverride Jester
        AddLevelUpRerolls 3
    }
}
```

---

### `MagicMirror`
**Name:** Magic Mirror (Broken)  
**Description:** Side Quest Item. Your team has very bad luck during events. +2 Thorns.  
**Source:** `beanies_quest_items.gon`  

```
MagicMirror {
    name "ARMOR_MAGICMIRROR_NAME"
    desc "ARMOR_MAGICMIRROR_DESC"
    kind face
    frame 147
    quest_item true
    cursed true
    rarity sidequest
    quest_reward_item MagicMirror_Fixed
	
	passives {
		Thorns 2
	}

    global_tags [fail_all_events]
}
```

---

### `MagicMirror_Fixed`
**Name:** Magic Mirror  
**Description:** +20% chance to reflect projectiles. Spawn a friendly Spookie when downed.  
**Source:** `beanies_quest_items.gon`  

```
MagicMirror_Fixed { //TODO: Soul Mirror that absorbed the previous cat, on die re-summon the other cat
    name "ARMOR_MAGICMIRROR_FIXED_NAME"
    desc "ARMOR_MAGICMIRROR_FIXED_DESC"
    kind face
    frame 148
    rarity rare

    passives {
        ReflectProjectiles 20%
        SpawnOnDowned CharmedSpookie
    }
}
```

---

### `MeStone`
**Name:** Me Stone  
**Description:** Side Quest Item. This cat always levels up, and can level up even if it was downed.  
**Source:** `beanies_quest_items.gon`  

```
MeStone {
    name "ITEM_MESTONE_NAME"
    desc "ITEM_MESTONE_DESC"
    kind trinket
    frame 227
	set Rock
    quest_item true
    cursed true
    rarity sidequest
    quest_reward_item MeStone_Fixed

    passives {
        CanLevelUpWhenDead 1
        AlwaysChosenForLevelUp 1
    }
}
```

---

### `MeStone_Fixed`
**Name:** Suck Stone  
**Description:** At the end of your turn, drain up to 5 mana from each of your allies.  
**Source:** `beanies_quest_items.gon`  

```
MeStone_Fixed {
    name "ITEM_MESTONE_FIXED_NAME"
    desc "ITEM_MESTONE_FIXED_DESC"
    kind trinket
    frame 228
	set Rock
    rarity rare

    passives {
        StatusEachTurnEnd {
            ForceUseAbility tk_SuckStone
        }
    }
}
```

---

### `AngryFace`
**Name:** Angry Face  
**Description:** Side Quest Item. Equipped cat is an enemy, must be downed to win the battle, and can still receive level ups. Can't be equipped to a Collarless cat.  
**Source:** `beanies_quest_items.gon`  

```
AngryFace {
    name "ARMOR_ANGRYFACE_NAME"
    desc "ARMOR_ANGRYFACE_DESC"
    kind face
    frame 143
	set Paper
    quest_item true
    cursed true
    rarity sidequest
    quest_reward_item AngryFace_Fixed
    cant_equip_to_colorless true

    passives {
        SetFaction enemies
        CanLevelUpWhenDead 1
        SpawnNearEnemies 1
        MoveAndUseAbilityEachTurnBeginIfPossible face_EatNeverstone
        AddEndOfCombatRegen 999999
    }
}
```

---

### `AngryFace_Fixed`
**Name:** Happy Face  
**Description:** Spawn near enemies and take an AI controlled bonus turn at the start of every battle.  
**Source:** `beanies_quest_items.gon`  

```
AngryFace_Fixed {
    name "ARMOR_ANGRYFACE_FIXED_NAME"
    desc "ARMOR_ANGRYFACE_FIXED_DESC"
    kind face
    frame 144
	set Paper
    rarity rare

    passives {
        SpawnNearEnemies 1
        AlphaTurns 1
        AIControlNextTurn {
            stacks 1
            include_spells true
        }
    }
}
```

---

### `FartFace`
**Name:** Fart Face  
**Description:** Side Quest Item. Apply Poison 1 to everything at the start of the battle.  
**Source:** `beanies_quest_items.gon`  

```
FartFace {
    name "ARMOR_FARTFACE_NAME"
    desc "ARMOR_FARTFACE_DESC"
    kind face
    frame 145
	set HumanFlesh
    quest_item true
    rarity sidequest
    quest_reward_item FartFace_Fixed

    passives {
        AbilityOnBattleStart face_FartFace
    }
}
```

---

### `FartFace_Fixed`
**Name:** Robo Fart Face  
**Description:** Apply Poison 1 to all enemies at the start of the battle.  
**Source:** `beanies_quest_items.gon`  

```
FartFace_Fixed {
    name "ARMOR_FARTFACE_FIXED_NAME"
    desc "ARMOR_FARTFACE_FIXED_DESC"
    kind face
    frame 146
	set Bionic
    rarity rare

    passives {
        AbilityOnBattleStart face_FartFaceFixed
    }
}
```

---

### `SpiderInjector`
**Name:** Spider Injector  
**Description:** Side Quest Item. Apply Infested 4 to all allies at the start of each battle.  
**Source:** `beanies_quest_items.gon`  

```
SpiderInjector {
    name "ARMOR_SPIDERINJECTOR_NAME"
    desc "ARMOR_SPIDERINJECTOR_DESC"
    kind head
    frame 162
    quest_item true
    rarity sidequest
    quest_reward_item SpiderInjector_Fixed

    passives {
        AbilityOnBattleStart head_SpiderInjector
    }
}
```

---

### `SpiderInjector_Fixed`
**Name:** Spider Baby  
**Description:** Apply Infested 1 to all enemies at the start of each battle.  
**Source:** `beanies_quest_items.gon`  

```
SpiderInjector_Fixed {
    name "ARMOR_SPIDERINJECTOR_FIXED_NAME"
    desc "ARMOR_SPIDERINJECTOR_FIXED_DESC"
    kind head
    frame 163
    rarity rare

    passives {
        AbilityOnBattleStart head_SpiderInjectorFixed
    }
}
```

---

### `PartyDetonator`
**Name:** Party Detonator  
**Description:** Side Quest Item. All units explode when they die.
Use: Explode a random other unit, once per battle.  
**Source:** `beanies_quest_items.gon`  

```
PartyDetonator {
    name "ITEM_PARTYDETONATOR_NAME"
    desc "ITEM_PARTYDETONATOR_DESC"
    kind weapon
    frame 170
    quest_item true
    rarity sidequest
    quest_reward_item PartyDetonator_Fixed

    ability wp_PartyDetonator

    passives {
        AllUnitsExplodeOnDeath 5
    }
}
```

---

### `PartyDetonator_Fixed`
**Name:** Party Detonator (Fixed)  
**Description:** Use: Explode a random unit within a target radius.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `beanies_quest_items.gon`  

```
PartyDetonator_Fixed {
    name "ITEM_PARTYDETONATOR_FIXED_NAME"
    desc "ITEM_PARTYDETONATOR_FIXED_DESC"
    kind weapon
    frame 171
    rarity rare

    ability wp_PartyDetonatorFixed
}
```

---

### `AirHorn`
**Name:** Air Horn  
**Description:** Side Quest Item. You are Ambushed every battle. Use to make some noise!  
**Source:** `beanies_quest_items.gon`  

```
AirHorn {
    name "ITEM_AIRHORN_NAME"
    desc "ITEM_AIRHORN_DESC"
    kind weapon
    frame 200
    quest_item true
    rarity sidequest
    quest_reward_item AirHorn_Fixed

    ability wp_AirHorn

    global_tags [always_ambushed]
}
```

---

### `AirHorn_Fixed`
**Name:** Amplified Air Horn  
**Description:** Use: Apply Madness to a unit within 5 tiles in your line of sight.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `beanies_quest_items.gon`  

```
AirHorn_Fixed {
    name "ITEM_AIRHORN_FIXED_NAME"
    desc "ITEM_AIRHORN_FIXED_DESC"
    kind weapon
    frame 206
    rarity rare

    ability wp_AirHornFixed
}
```

---

### `TheLoner`
**Name:** The Loner  
**Description:** Side Quest Item. Kill all of your allies at the start of each battle.  
**Source:** `beanies_quest_items.gon`  

```
TheLoner {
    name "ITEM_THELONER_NAME"
    desc "ITEM_THELONER_DESC"
    kind weapon
    frame 204
	set Cool
    quest_item true
    rarity sidequest
    quest_reward_item TheLoner_Fixed

    ability wp_TheLoner

    passives {
        AbilityOnBattleStart wp_TheLonerAuto
    }
}
```

---

### `TheLoner_Fixed`
**Name:** The Loner Mark 2  
**Description:** Use: Deals 5 damage to anything in your line of sight.
RELOAD: Any ally dies.  
**Source:** `beanies_quest_items.gon`  

```
TheLoner_Fixed {
    name "ITEM_THELONER_FIXED_NAME"
    desc "ITEM_THELONER_FIXED_DESC"
    kind weapon
    frame 209
	set [Cool, Used]
    rarity rare

    ability wp_TheLonerFixed
}
```

---

### `GlassCannon`
**Name:** Glass Cannon  
**Description:** Side Quest Item. Fill the map with glass at the start of each battle.
Use: Shoot a glass ball.  
**Source:** `beanies_quest_items.gon`  

```
GlassCannon {
    name "ITEM_GLASSCANNON_NAME"
    desc "ITEM_GLASSCANNON_DESC"
    kind weapon
    frame 205
    quest_item true
    rarity sidequest
    quest_reward_item GlassCannon_Fixed

    ability wp_GlassCannon

    passives {
        ReplaceBlankTilesOnBattleStart GlassTile
    }
}
```

---

### `GlassCannon_Fixed`
**Name:** Glass Cannon (Fixed)  
**Description:** Use: Shoot a glass ball anywhere.  
**Source:** `beanies_quest_items.gon`  

```
GlassCannon_Fixed {
    name "ITEM_GLASSCANNON_FIXED_NAME"
    desc "ITEM_GLASSCANNON_FIXED_DESC"
    kind weapon
    frame 210
    rarity rare

    ability wp_GlassCannonFixed
}
```

---

### `PrincessHat`
**Name:** Princess Hat  
**Description:** Side Quest Item. Fragile. Equipped cat cannot use any actions except Move.  
**Source:** `beanies_quest_items.gon`  

```
PrincessHat {
    name "ARMOR_PRINCESSHAT_NAME"
    desc "ARMOR_PRINCESSHAT_DESC"
    kind head
    frame 201
    quest_item true
    rarity sidequest
    quest_reward_item PrincessHat_Fixed

    shield 10

    passives {
        Fragile 1
        DisableAbilities all_items
        DisableAbilities all_spells
        DisableAbilities basic_attack
    }
}
```

---

### `PrincessHat_Fixed`
**Name:** Used Princess Hat  
**Description:** ARMOR_PRINCESSHAT_FIXED_DESC  
**Source:** `beanies_quest_items.gon`  

```
PrincessHat_Fixed {
    name "ARMOR_PRINCESSHAT_FIXED_NAME"
    desc "ARMOR_PRINCESSHAT_FIXED_DESC"
    kind head
    frame 203
    rarity rare
    set Used

    shield 6
}
```

---

### `HardPill`
**Name:** Unidentified Pills  
**Description:** Side Quest Item. The adventure is harder!  
**Source:** `beanies_quest_items.gon`  

```
HardPill {
    name "ITEM_HARDPILL_NAME"
    desc "ITEM_HARDPILL_DESC"
    kind trinket
    frame 252
    quest_item true
    rarity sidequest
    quest_reward_item HardPill_Fixed
	
	shield 8

    global_tags [increase_difficulty]
}
```

---

### `HardPill_Fixed`
**Name:** Truck Stop Pills  
**Description:** +3 Brace. You count as a rock.  
**Source:** `beanies_quest_items.gon`  

```
HardPill_Fixed {
    name "ITEM_HARDPILL_FIXED_NAME"
    desc "ITEM_HARDPILL_FIXED_DESC"
    kind trinket
    frame 257
    rarity rare

    passives {
        Brace 3
        AddTag rock
    }
}
```

---

### `BubbleBoy`
**Name:** Bubble Boy  
**Description:** Side Quest Item. All units rebound with Knockback 5 on contact.  
**Source:** `beanies_quest_items.gon`  

```
BubbleBoy {
    name "ARMOR_BUBBLEBOY_NAME"
    desc "ARMOR_BUBBLEBOY_DESC"
    kind neck
    frame 153
    quest_item true
    rarity sidequest
    quest_reward_item BubbleBoy_Fixed
    
    passives {
        GlobalMeleeRevengeDamage {
            knockback 5
        }
    }
}
```

---

### `BubbleBoy_Fixed`
**Name:** Bubbles  
**Description:** Use: Throw a bubble with Wind and Water Element that inflicts Confusion.  
**Source:** `beanies_quest_items.gon`  

```
BubbleBoy_Fixed {
    name "ITEM_BUBBLEBOY_FIXED_NAME"
    desc "ITEM_BUBBLEBOY_FIXED_DESC"
    kind weapon
    frame 216
    rarity rare

    ability wp_BubbleBoyFixed
}
```

---

### `Redacted`
**Name:** Redacted  
**Description:** Side Quest Item. Health bars and status icons are hidden in battle.  
**Source:** `beanies_quest_items.gon`  

```
Redacted {
    name "ARMOR_REDACTED_NAME"
    desc "ARMOR_REDACTED_DESC"
    kind face
    frame 164
    quest_item true
    rarity sidequest
    quest_reward_item Redacted_Fixed

    passives {
        HideSomeHudStuff 1
    }
}
```

---

### `Redacted_Fixed`
**Name:** Paper Bag  
**Description:** Your [img:cha] is equal to your highest other stat.  
**Source:** `beanies_quest_items.gon`  

```
Redacted_Fixed {
    name "ARMOR_REDACTED_FIXED_NAME"
    desc "ARMOR_REDACTED_FIXED_DESC"
    kind face
    frame 168
    rarity rare

    passives {
        CharismaIsMaxStat 1
    }
}
```

---

### `Stopwatch`
**Name:** Stopwatch  
**Description:** Side Quest Item. You have 5 seconds to make decisions in battle, otherwise cats will act randomly.  
**Source:** `beanies_quest_items.gon`  

```
Stopwatch {
    name "ITEM_STOPWATCH_NAME"
    desc "ITEM_STOPWATCH_DESC"
    kind trinket
    frame 249
    quest_item true
    rarity sidequest
    quest_reward_item Stopwatch_Fixed

    global_passives {
        RealTimePressure 5
    }
}
```

---

### `Stopwatch_Fixed`
**Name:** Stopwatch (Fixed)  
**Description:** Use: You or a target unit takes an AI controlled bonus turn.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `beanies_quest_items.gon`  

```
Stopwatch_Fixed {
    name "ITEM_STOPWATCH_FIXED_NAME"
    desc "ITEM_STOPWATCH_FIXED_DESC"
    kind weapon
    frame 213
    rarity rare

    ability wp_StopwatchFixed
}
```

---

### `StorageLocker`
**Name:** Storage Locker  
**Description:** Side Quest Item. Your team's active ability level ups offer rare items instead.  
**Source:** `beanies_quest_items.gon`  

```
StorageLocker {
    name "ARMOR_STORAGELOCKER_NAME"
    desc "ARMOR_STORAGELOCKER_DESC"
    kind neck
    frame 150
    quest_item true
    rarity sidequest
    quest_reward_item StorageLocker_Fixed

    global_tags [item_levelup_quest]
    
    passives {
        Metal 1
    }
}
```

---

### `StorageLocker_Fixed`
**Name:** Armory Key  
**Description:** Find an extra item after each battle.  
**Source:** `beanies_quest_items.gon`  

```
StorageLocker_Fixed {
    name "ARMOR_STORAGELOCKER_FIXED_NAME"
    desc "ARMOR_STORAGELOCKER_FIXED_DESC"
    kind neck
    frame 157
    rarity rare

    passives {
        Metal 1
        FindExtraItemFromPoolOnBattleEnd combat_reward_easy
    }
}
```

---

### `MysteriousDice`
**Name:** Mysterious Dice  
**Description:** Side Quest Item. Your team's level up options are complete chaos!  
**Source:** `beanies_quest_items.gon`  

```
MysteriousDice {
    name "ITEM_MYSTERIOUSDICE_NAME"
    desc "ITEM_MYSTERIOUSDICE_DESC"
    kind trinket
    frame 255
    quest_item true
    rarity sidequest
    quest_reward_item MysteriousDice_Fixed

    global_tags [superchaos_levelups]
}
```

---

### `MysteriousDice_Fixed`
**Name:** The D6  
**Description:** Use: Permanently upgrade one of your active abilities at random.  
**Source:** `beanies_quest_items.gon`  

```
MysteriousDice_Fixed {
    name "ITEM_MYSTERIOUSDICE_FIXED_NAME"
    desc "ITEM_MYSTERIOUSDICE_FIXED_DESC"
    kind trinket
    frame 259
    rarity rare
    consumable true

    durability 1

    ability cm_TheD6
}
```

---

### `ExperimentalTreatment`
**Name:** Experimental Treatment  
**Description:** Side Quest Item. Your team's passive ability level ups offer disorders instead.  
**Source:** `beanies_quest_items.gon`  

```
ExperimentalTreatment {
    name "ARMOR_EXPERIMENTALTREATMENT_NAME"
    desc "ARMOR_EXPERIMENTALTREATMENT_DESC"
    kind face
    frame 162
	set Experimental
    quest_item true
    rarity sidequest
    quest_reward_item ExperimentalTreatment_Fixed

    global_tags [disorder_levelup_quest]
}
```

---

### `ExperimentalTreatment_Fixed`
**Name:** Disorder Decoder  
**Description:** Your spells cost 1 less for each disorder you have.  
**Source:** `beanies_quest_items.gon`  

```
ExperimentalTreatment_Fixed {
    name "ARMOR_EXPERIMENTALTREATMENT_FIXED_NAME"
    desc "ARMOR_EXPERIMENTALTREATMENT_FIXED_DESC"
    kind face
    frame 167
	set Experimental
    rarity rare

    passives {
        ReduceSpellCostsPerDisorder 1
    }
}
```

---

### `UltraVision3000`
**Name:** Ultra Vision 3000  
**Description:** Side Quest Item. Events are harder. All normal events trigger 2 extra events.  
**Source:** `beanies_quest_items.gon`  

```
UltraVision3000 {
    name "ARMOR_ULTRAVISION3000_NAME"
    desc "ARMOR_ULTRAVISION3000_DESC"
    kind face
    frame 166
	set Bionic
    quest_item true
    rarity sidequest
    quest_reward_item UltraVision3000_Fixed

    global_tags [
        increase_event_difficulty 
        increase_event_difficulty 
        trigger_extra_event
        trigger_extra_event
    ]
}
```

---

### `UltraVision3000_Fixed`
**Name:** Ultra Vision 3000 v1.1  
**Description:** Your basic attack inflicts Marked.  
**Source:** `beanies_quest_items.gon`  

```
UltraVision3000_Fixed {
    name "ARMOR_ULTRAVISION3000_FIXED_NAME"
    desc "ARMOR_ULTRAVISION3000_FIXED_DESC"
    kind face
    frame 169
	set Bionic
    rarity rare
    cursed true

    lck 4

    passives {
        AddStatusToBasicAttack {
            Marked 1
        }
    }
}
```

---

### `NuclearKnife`
**Name:** Nuclear Knife  
**Description:** Side Quest Item. Use: Melee Attack with damage = charges ({aux}). Permanently gains 1 charge at the end of each turn.
If charges go above 10, this weapon explodes.
Loses half of its charges when it gets a kill.  
**Source:** `beanies_quest_items.gon`  

```
NuclearKnife {
    name "ITEM_NUCLEARKNIFE_NAME"
    desc "ITEM_NUCLEARKNIFE_DESC"
    kind weapon
    frame 201
	set Radioactive
    quest_item true
    rarity sidequest
    quest_reward_item NuclearKnife_Fixed
    
    ability wp_NuclearKnife

    passives {
        StatusEachTurnEnd {
            AddWeaponAux 1
        }
        ItemAuxTransform {
            ge [10 NuclearKnife_Glowing]
        }
    }
}
```

---

### `NuclearKnife_Glowing`
**Name:** Nuclear Knife (Glowing)  
**Description:** Side Quest Item. It's about to explode! Get a kill with this now to quench it.  
**Source:** `beanies_quest_items.gon`  

```
NuclearKnife_Glowing {
    name "ITEM_NUCLEARKNIFE_GLOWING_NAME"
    desc "ITEM_NUCLEARKNIFE_GLOWING_DESC"
    kind weapon
    frame 202
	set Radioactive
    quest_item true
    rarity sidequest
    quest_reward_item NuclearKnife_Fixed
    quest_item_alias NuclearKnife
    
    ability wp_NuclearKnife

    aux 10

    passives { 
        StatusEachTurnEnd {
            ImmediateUseAbility {
                ability wp_NuclearKnifeExplode
                even_if_stunned true
            }
        }

        ItemAuxTransform {
            lt [10 NuclearKnife]
        }
    }
}
```

---

### `NuclearKnife_Fixed`
**Name:** Nuclear Gun  
**Description:** Use: Deals 40 damage to a target and 20 damage to EVERYTHING ELSE. 20% chance to break on use.  
**Source:** `beanies_quest_items.gon`  

```
NuclearKnife_Fixed {
    name "ITEM_NUCLEARKNIFE_FIXED_NAME"
    desc "ITEM_NUCLEARKNIFE_FIXED_DESC"
    kind weapon
    frame 207
	set Radioactive
    rarity rare

    ability wp_NuclearKnifeFixed
}
```

---

## File: `consumables.gon`

### `FoodMedium`
**Name:** A Snack  
**Description:** Use: Heal {aux} HP.  
**Source:** `consumables.gon`  

```
FoodMedium {
    name "ITEM_ASNACK_NAME"
    desc "ITEM_ASNACK_DESC"
    rarity consumable_common
    kind trinket
    frame 21
    durability 1
    consumable true

    ability cm_Heal
    aux 12
}
```

---

### `FoodBig`
**Name:** Cat Food  
**Description:** Use: Heal {aux} HP.  
**Source:** `consumables.gon`  

```
FoodBig {
    name "ITEM_CATFOOD_NAME"
    desc "ITEM_CATFOOD_DESC"
    rarity consumable_common
    kind trinket
    frame 2
    durability 1
    consumable true

    ability cm_Heal
    aux 24
}
```

---

### `Chicken`
**Name:** Rotisserie Chicken  
**Description:** Use: Heal {aux} HP.  
**Source:** `consumables.gon`  

```
Chicken {
    name "ITEM_ROTISSERIECHICKEN_NAME"
    desc "ITEM_ROTISSERIECHICKEN_DESC"
    rarity consumable_rare
    kind trinket
    frame 59
    durability 3
    consumable true

    ability cm_Heal
    aux 15
}
```

---

### `Catnip`
**Name:** Small Catnip Baggy  
**Description:** Use: Gain {aux} mana.  
**Source:** `consumables.gon`  

```
Catnip {
    name "ITEM_SMALLCATNIPBAGGY_NAME"
    desc "ITEM_SMALLCATNIPBAGGY_DESC"
    rarity consumable_common
    kind trinket
    frame 22
    durability 1
    consumable true

    ability cm_Catnip
    aux 7
}
```

---

### `CatnipBig`
**Name:** Large Catnip Baggy  
**Description:** Use: Gain {aux} mana.  
**Source:** `consumables.gon`  

```
CatnipBig {
    name "ITEM_LARGECATNIPBAGGY_NAME"
    desc "ITEM_LARGECATNIPBAGGY_DESC"
    rarity consumable_common
    kind trinket
    frame 3
    durability 1
    consumable true

    ability cm_Catnip
    aux 12
}
```

---

### `RoidRage`
**Name:** Roid Rage  
**Description:** Use: Gain +{aux} [img:str] for the rest of the battle.  
**Source:** `consumables.gon`  

```
RoidRage {
    name "ITEM_ROIDRAGE_NAME"
    desc "ITEM_ROIDRAGE_DESC"
    rarity consumable_common
    kind trinket
    frame 23
    durability 1
    consumable true

    ability cm_StrBuff
    aux 5
}
```

---

### `SpeedBall`
**Name:** Speedball  
**Description:** Use: Gain +{aux} [img:dex] for the rest of the battle.  
**Source:** `consumables.gon`  

```
SpeedBall {
    name "ITEM_SPEEDBALL_NAME"
    desc "ITEM_SPEEDBALL_DESC"
    rarity consumable_common
    kind trinket
    frame 24
    durability 1
    consumable true

    ability cm_DexBuff
    aux 5
}
```

---

### `BrainCandy`
**Name:** Brain Candy  
**Description:** Use: Gain +{aux} [img:int] for the rest of the battle.  
**Source:** `consumables.gon`  

```
BrainCandy {
    name "ITEM_BRAINCANDY_NAME"
    desc "ITEM_BRAINCANDY_DESC"
    rarity consumable_common
    kind trinket
    frame 25
    durability 1
    consumable true

    ability cm_IntBuff
    aux 5
}
```

---

### `DiscoBiscuit`
**Name:** Disco Biscuit  
**Description:** Use: Gain +{aux} [img:cha] for the rest of the battle and gain 6 mana.  
**Source:** `consumables.gon`  

```
DiscoBiscuit {
    name "ITEM_DISCOBISCUIT_NAME"
    desc "ITEM_DISCOBISCUIT_DESC"
    rarity consumable_common
    kind trinket
    frame 26
    durability 1
    consumable true

    ability cm_ChaBuff
    aux 5
}
```

---

### `Clover`
**Name:** Clover  
**Description:** Use: Gain +{aux} [img:lck] for the rest of the battle.  
**Source:** `consumables.gon`  

```
Clover {
    name "ITEM_CLOVER_NAME"
    desc "ITEM_CLOVER_DESC"
    rarity consumable_common
    kind trinket
    frame 27
    durability 1
    consumable true

    ability cm_LckBuff
    aux 5
}
```

---

### `Upper`
**Name:** Upper  
**Description:** Use: Gain +{aux} [img:spd] for the rest of the battle.  
**Source:** `consumables.gon`  

```
Upper {
    name "ITEM_UPPER_NAME"
    desc "ITEM_UPPER_DESC"
    rarity consumable_common
    kind trinket
    frame 28
    durability 1
    consumable true

    ability cm_SpdBuff
    aux 5
}
```

---

### `Percs`
**Name:** Percs  
**Description:** Use: Gain +{aux} [img:shield].  
**Source:** `consumables.gon`  

```
Percs {
    name "ITEM_PERCS_NAME"
    desc "ITEM_PERCS_DESC"
    rarity consumable_common
    kind trinket
    frame 29
    durability 1
    consumable true

    ability cm_Shield
    aux 10
}
```

---

### `Antidote`
**Name:** Antidote  
**Description:** Use: Cleanse all debuffs.
This can be used on adjacent units.  
**Source:** `consumables.gon`  

```
Antidote {
    name "ITEM_ANTIDOTE_NAME"
    desc "ITEM_ANTIDOTE_DESC"
    rarity consumable_common
    kind trinket
    frame 103
    durability 2
    consumable true

    ability cm_Antidote
}
```

---

### `Kidney`
**Name:** Kidney  
**Description:** Use: Use to heal 10, gain +2 Health Regen, and cleanse debuffs.  
**Source:** `consumables.gon`  

```
Kidney {
    name "ITEM_KIDNEY_NAME"
    desc "ITEM_KIDNEY_DESC"
    kind trinket
    frame 189
    durability 1
    consumable true

    ability cm_Kidney
}
```

---

### `Enema`
**Name:** Enema  
**Description:** Use: Cleanse all buffs and debuffs.  
**Source:** `consumables.gon`  

```
Enema {
    name "ITEM_ENEMA_NAME"
    desc "ITEM_ENEMA_DESC"
    rarity consumable_uncommon
    kind trinket
    frame 100
    durability 5
    consumable true

    ability cm_Enema
}
```

---

### `SitrusBerry`
**Name:** Citrus Berry  
**Description:** Use: Heal 25% HP.
Automatically eaten if your HP drops below 50%.  
**Source:** `consumables.gon`  

```
SitrusBerry {
    name "ITEM_SITRUSBERRY_NAME"
    desc "ITEM_SITRUSBERRY_DESC"
    rarity consumable_uncommon
    kind trinket
    frame 101
    durability 1
    consumable true

    ability cm_HealPercent
    aux 25
    
    passives {
        AbilityHealthThreshold {
            threshold "max(X*.5, 1)"
            immediate true
            even_if_stunned true
            ability cm_HealPercent_Auto
            aux 25
        }
    }
}
```

---

### `SmellingSalts`
**Name:** Smelling Salts  
**Description:** Use: Revive an adjacent unit at 1 HP.
Automatically used on yourself at the end of the round if you're downed.  
**Source:** `consumables.gon`  

```
SmellingSalts {
    name "ITEM_SMELLINGSALTS_NAME"
    desc "ITEM_SMELLINGSALTS_DESC"
    rarity consumable_uncommon
    kind trinket
    frame 111
    durability 3
    consumable true
    
    ability cm_SmellingSalts
    
    passives {
        PassiveWhenDead {
            StatusEachTurnBegin {
                Revive 1
                DestroyTrinket 1
            }
        }
    }
}
```

---

### `Lard`
**Name:** Big Bucket of Lard  
**Description:** Use: Heal yourself and all adjacent units to full HP.  
**Source:** `consumables.gon`  

```
Lard {
    name "ITEM_LARD_NAME"
    desc "ITEM_LARD_DESC"
    rarity consumable_rare
    kind trinket
    frame 75
    durability 1
    consumable true

    ability cm_Lard
}
```

---

### `KiloOfCatnip`
**Name:** Kilo of Catnip  
**Description:** Use: Restore all your mana.  
**Source:** `consumables.gon`  

```
KiloOfCatnip {
    name "ITEM_KILOOFCATNIP_NAME"
    desc "ITEM_KILOOFCATNIP_DESC"
    rarity consumable_rare
    kind trinket
    frame 121
    durability 1
    consumable true

    ability cm_KiloOfCatnip
}
```

---

### `BagOfGrass`
**Name:** Bag of Grass  
**Description:** Use: Gain {aux} mana.  
**Source:** `consumables.gon`  

```
BagOfGrass {
    name "ITEM_BAGOFGRASS_NAME"
    desc "ITEM_BAGOFGRASS_DESC"
    rarity consumable_rare
    kind trinket
    frame 69
    durability 5
    consumable true

    ability cm_Catnip
    aux 10
}
```

---

### `ViperBottle`
**Name:** Viper Bottle  
**Description:** Use: Take 5 damage and gain +1 to a random stat permanently.
May have side effects...  
**Source:** `consumables.gon`  

```
ViperBottle {
    name "ITEM_VIPERBOTTLE_NAME"
    desc "ITEM_VIPERBOTTLE_DESC"
    rarity consumable_rare
    kind trinket
    frame 72
    durability [2 4]
    consumable true
    
    ability cm_ViperBottle
}
```

---

### `SuperBandage`
**Name:** Super Bandage  
**Description:** Use: Cure a random injury.  
**Source:** `consumables.gon`  

```
SuperBandage {
    name "ITEM_SUPERBANDAGE_NAME"
    desc "ITEM_SUPERBANDAGE_DESC"
    rarity consumable_rare
    kind trinket
    frame 102
    durability 4
    consumable true
	set Nurse
    
    ability cm_SuperBandage
}
```

---

### `RottenMeat`
**Name:** Rotten Meat  
**Description:** Use: Gain Poison 1, then your basic attack becomes Puke Shot.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `consumables.gon`  

```
RottenMeat {
    name "ITEM_ROTTENMEAT_NAME"
    desc "ITEM_ROTTENMEAT_DESC"
    rarity consumable_rare
    kind trinket
    frame 112
    consumable true
	set [Rotten, Meat]
    
    ability cm_RottenMeat
}
```

---

### `Mushrooms`
**Name:** Mushrooms  
**Description:** Use: Gain All Stats Up 2.  
**Source:** `consumables.gon`  

```
Mushrooms {
    name "ITEM_MUSHROOMS_NAME"
    desc "ITEM_MUSHROOMS_DESC"
    rarity consumable_uncommon
    kind trinket
    frame 116
    durability [2 4]
    consumable true
	set Druid
    
    ability cm_AllStatsBuff
    aux 2
}
```

---

### `Star`
**Name:** Star  
**Description:** Use: Gain Invincibility, +10 Thorns, and Trample until the start of your next turn. Refresh your movement action.  
**Source:** `consumables.gon`  

```
Star {
    name "ITEM_STAR_NAME"
    desc "ITEM_STAR_DESC"
    rarity consumable_very_rare
    kind trinket
    frame 119
    durability 1
    consumable true
    
    ability cm_Star
}
```

---

### `Bullseye`
**Name:** Bullseye  
**Description:** Use: All damage you deal until the end of the turn is critical and can't miss.  
**Source:** `consumables.gon`  

```
Bullseye {
    name "ITEM_BULLSEYE_NAME"
    desc "ITEM_BULLSEYE_DESC"
    rarity consumable_uncommon
    kind trinket
    frame 120
    durability 4
    consumable true
	set Paper
    
    ability cm_Bullseye
}
```

---

### `StemCells`
**Name:** Stem Cells  
**Description:** Use: Gain +3 Health Regen until the end of the battle.  
**Source:** `consumables.gon`  

```
StemCells {
    name "ITEM_STEMCELLS_NAME"
    desc "ITEM_STEMCELLS_DESC"
    rarity consumable_uncommon
    kind trinket
    frame 122
    durability 2
    consumable true
    
    ability cm_StemCells
}
```

---

### `Eyeball`
**Name:** Eyeball  
**Description:** Use: Heal {aux} HP.  
**Source:** `consumables.gon`  

```
Eyeball {
    name "ITEM_EYEBALL_NAME"
    desc "ITEM_EYEBALL_DESC"
    rarity consumable_common
    kind trinket
    frame 131
    durability 1
    consumable true
	set Guts
    
    ability cm_Heal
    aux 8
}
```

---

### `WitchsEye`
**Name:** Witch's Eye  
**Description:** Use: Gain Backflip 2.  
**Source:** `consumables.gon`  

```
WitchsEye {
    name "ITEM_WITCHSEYE_NAME"
    desc "ITEM_WITCHSEYE_DESC"
    rarity consumable_uncommon
    kind trinket
    frame 132
    durability [2 6]
    consumable true
    
    ability cm_WitchsEye
}
```

---

### `ForbiddenFruit`
**Name:** Forbidden Fruit  
**Description:** Use: Heal to full, restore all your mana, and gain All Stats Up 2.
There will be permanent consequences for eating this fruit...  
**Source:** `consumables.gon`  

```
ForbiddenFruit {
    name "ITEM_FORBIDDENFRUIT_NAME"
    desc "ITEM_FORBIDDENFRUIT_DESC"
    rarity consumable_very_rare
    kind trinket
    frame 136
    durability [1 3]
    consumable true
    
    ability cm_ForbiddenFruit
}
```

---

### `PCP`
**Name:** PCP  
**Description:** Use: Gain +5 Damage and Madness 3.
This can be used on adjacent units.  
**Source:** `consumables.gon`  

```
PCP {
    name "ITEM_PCP_NAME"
    desc "ITEM_PCP_DESC"
    rarity consumable_uncommon
    kind trinket
    frame 138
    durability 3
    consumable true
    
    ability cm_PCP
}
```

---

### `WishBone`
**Name:** Wish Bone  
**Description:** Use: Gain +99 [img:lck] until the end of the turn.  
**Source:** `consumables.gon`  

```
WishBone {
    name "ITEM_WISHBONE_NAME"
    desc "ITEM_WISHBONE_DESC"
    rarity consumable_very_rare
    kind trinket
    frame 193
    durability 1
    consumable true
	set Bone
    
    ability cm_WishBone
}
```

---

### `MetalCoat`
**Name:** Metal Coat  
**Description:** Use: Make your weapon unbreakable for the rest of the adventure.  
**Source:** `consumables.gon`  

```
MetalCoat {
    name "ITEM_METALCOAT_NAME"
    desc "ITEM_METALCOAT_DESC"
    rarity very_rare //this one is not consumables_very_rare cause I moved it to the general pool now and not the consumable pool
    kind trinket
    frame 43
    durability 1
    consumable true
    
    ability cm_MetalCoat
}
```

---

### `ShoePolish`
**Name:** Shoe Polish  
**Description:** Use: Fully repair your weapon. Refresh your weapon action.  
**Source:** `consumables.gon`  

```
ShoePolish {
    name "ITEM_SHOEPOLISH_NAME"
    desc "ITEM_SHOEPOLISH_DESC"
    rarity rare
    kind trinket
    frame 44
    durability 1
    consumable true
    
    ability cm_ShoePolish
}
```

---

### `Pearl`
**Name:** Pearl  
**Description:** Use: Gain 10-30 coins.  
**Source:** `consumables.gon`  

```
Pearl {
    name "ITEM_PEARL_NAME"
    desc "ITEM_PEARL_DESC"
    kind trinket
    frame 57
    durability 1
    consumable true
    
    lck 2

    ability cm_Pearl
}
```

---

### `BigToe`
**Name:** Big Toe  
**Description:** Use: Heal 6, gain +1 Health Regen and cleanse your debuffs.  
**Source:** `consumables.gon`  

```
BigToe { //Aquired from Big Toe event
    name "ITEM_BIGTOE_NAME"
    desc "ITEM_BIGTOE_DESC"
    kind trinket
    frame 265
    durability 1
    consumable true
	set HumanFlesh

    ability cm_BigToe
}
```

---

### `RaptorEgg`
**Name:** Raptor Egg  
**Description:** Use: Heal to full.
10% chance at the end of each turn to break and summon a Charmed Raptor Kitten.  
**Source:** `consumables.gon`  

```
RaptorEgg { //Aquired from Nest of Eggs event
    name "ITEM_RAPTOREGG_NAME"
    desc "ITEM_RAPTOREGG_DESC"
    kind trinket
    frame 263
    durability 1
    consumable true

    ability cm_RaptorEgg
    
    passives {
        StatusEachTurnEnd {
            Conditional_GoodRoll {
                odds 10%
                ForceUseAbility cm_RaptorEggSpawn
                DestroyTrinket 1
            }
        }
    }
}
```

---

### `FighterSeal`
**Name:** Fighter Seal  
**Description:** Use: Permanently turn into a Fighter.  
**Source:** `consumables.gon`  

```
FighterSeal {
    name "ITEM_FIGHTERSEAL_NAME"
    desc "ITEM_FIGHTERSEAL_DESC"
    kind trinket
    rarity rare
    frame 160
    durability 1
    consumable true
	set Fighter
    
    ability cm_FighterSeal
}
```

---

### `HunterSeal`
**Name:** Hunter Seal  
**Description:** Use: Permanently turn into a Hunter.  
**Source:** `consumables.gon`  

```
HunterSeal {
    name "ITEM_HUNTERSEAL_NAME"
    desc "ITEM_HUNTERSEAL_DESC"
    kind trinket
    rarity rare
    frame 161
    durability 1
    consumable true
	set Hunter
    
    ability cm_HunterSeal
}
```

---

### `TankSeal`
**Name:** Tank Seal  
**Description:** Use: Permanently turn into a Tank.  
**Source:** `consumables.gon`  

```
TankSeal {
    name "ITEM_TANKSEAL_NAME"
    desc "ITEM_TANKSEAL_DESC"
    kind trinket
    rarity rare
    frame 162
    durability 1
    consumable true
	set Tank
    
    ability cm_TankSeal
}
```

---

### `ClericSeal`
**Name:** Cleric Seal  
**Description:** Use: Permanently turn into a Cleric.  
**Source:** `consumables.gon`  

```
ClericSeal {
    name "ITEM_CLERICSEAL_NAME"
    desc "ITEM_CLERICSEAL_DESC"
    kind trinket
    rarity rare
    frame 163
    durability 1
    consumable true
	set Cleric
    
    ability cm_ClericSeal
}
```

---

### `ThiefSeal`
**Name:** Thief Seal  
**Description:** Use: Permanently turn into a Thief.  
**Source:** `consumables.gon`  

```
ThiefSeal {
    name "ITEM_THIEFSEAL_NAME"
    desc "ITEM_THIEFSEAL_DESC"
    kind trinket
    rarity rare
    frame 164
    durability 1
    consumable true
	set Thief
    
    ability cm_ThiefSeal
}
```

---

### `MageSeal`
**Name:** Mage Seal  
**Description:** Use: Permanently turn into a Mage.  
**Source:** `consumables.gon`  

```
MageSeal {
    name "ITEM_MAGESEAL_NAME"
    desc "ITEM_MAGESEAL_DESC"
    kind trinket
    rarity rare
    frame 165
    durability 1
    consumable true
	set Mage
    
    ability cm_MageSeal
}
```

---

### `ColorlessSeal`
**Name:** Void Seal  
**Description:** Use: Permanently turn into a Collarless cat.  
**Source:** `consumables.gon`  

```
ColorlessSeal {
    name "ITEM_COLORLESSSEAL_NAME"
    desc "ITEM_COLORLESSSEAL_DESC"
    kind trinket
    rarity rare
    frame 166
    durability 1
    consumable true
    
    ability cm_ColorlessSeal
}
```

---

### `PsychicSeal`
**Name:** Psychic Seal  
**Description:** Use: Permanently turn into a Psychic.  
**Source:** `consumables.gon`  

```
PsychicSeal {
    name "ITEM_PSYCHICSEAL_NAME"
    desc "ITEM_PSYCHICSEAL_DESC"
    kind trinket
    rarity rare
    frame 167
    durability 1
    consumable true
	set Psychic
    
    ability cm_PsychicSeal
}
```

---

### `JesterSeal`
**Name:** Jester Seal  
**Description:** Use: Permanently turn into a Jester.  
**Source:** `consumables.gon`  

```
JesterSeal {
    name "ITEM_JESTERSEAL_NAME"
    desc "ITEM_JESTERSEAL_DESC"
    kind trinket
    rarity rare
    frame 168
    durability 1
    consumable true
	set Jester
    
    ability cm_JesterSeal
}
```

---

### `TinkererSeal`
**Name:** Tinkerer Seal  
**Description:** Use: Permanently turn into a Tinkerer.  
**Source:** `consumables.gon`  

```
TinkererSeal {
    name "ITEM_TINKERERSEAL_NAME"
    desc "ITEM_TINKERERSEAL_DESC"
    kind trinket
    rarity rare
    frame 169
    durability 1
    consumable true
	set Tinkerer
    
    ability cm_TinkererSeal
}
```

---

### `ButcherSeal`
**Name:** Butcher Seal  
**Description:** Use: Permanently turn into a Butcher.  
**Source:** `consumables.gon`  

```
ButcherSeal {
    name "ITEM_BUTCHERSEAL_NAME"
    desc "ITEM_BUTCHERSEAL_DESC"
    kind trinket
    rarity rare
    frame 170
    durability 1
    consumable true
	set Butcher
    
    ability cm_ButcherSeal
}
```

---

### `DruidSeal`
**Name:** Druid Seal  
**Description:** Use: Permanently turn into a Druid.  
**Source:** `consumables.gon`  

```
DruidSeal {
    name "ITEM_DRUIDSEAL_NAME"
    desc "ITEM_DRUIDSEAL_DESC"
    kind trinket
    rarity rare
    frame 171
    durability 1
    consumable true
	set Druid
    
    ability cm_DruidSeal
}
```

---

### `MonkSeal`
**Name:** Monk Seal  
**Description:** Use: Permanently turn into a Monk.  
**Source:** `consumables.gon`  

```
MonkSeal {
    name "ITEM_MONKSEAL_NAME"
    desc "ITEM_MONKSEAL_DESC"
    kind trinket
    rarity rare
    frame 172
    durability 1
    consumable true
	Set Monk
    
    ability cm_MonkSeal
}
```

---

### `NecromancerSeal`
**Name:** Necromancer Seal  
**Description:** Use: Permanently turn into a Necromancer.  
**Source:** `consumables.gon`  

```
NecromancerSeal {
    name "ITEM_NECROMANCERSEAL_NAME"
    desc "ITEM_NECROMANCERSEAL_DESC"
    kind trinket
    rarity rare
    frame 173
    durability 1
    consumable true
	set Necromancer
    
    ability cm_NecromancerSeal
}
```

---

### `Turkey`
**Name:** Whole Turkey  
**Description:** Use: Heal {aux} HP.  
**Source:** `consumables.gon`  

```
Turkey {
    name "ITEM_TURKEY_NAME"
    desc "ITEM_TURKEY_DESC"
    rarity consumable_rare
    kind trinket
    frame 244
    durability 7
    consumable true

    ability cm_Heal
    aux 15
}
```

---

### `DeadHummingbird`
**Name:** Dead Hummingbird  
**Description:** Use: Gain +20 [img:spd] and +50% Dodge Chance.  
**Source:** `consumables.gon`  

```
DeadHummingbird {
    name "ITEM_DEADHUMMINGBIRD_NAME"
    desc "ITEM_DEADHUMMINGBIRD_DESC"
    rarity consumable_very_rare
    kind trinket
    frame 245
    durability 2
    consumable true
	set Feathered

    ability cm_EatHummingbird
    aux 20
}
```

---

### `UnstableDNA`
**Name:** Unstable DNA  
**Description:** Use: Gain 6 random stat ups and 3 random stat downs, then gain 3 Mutations at the end of combat.  
**Source:** `consumables.gon`  

```
UnstableDNA {
    name "ITEM_UNSTABLEDNA_NAME"
    desc "ITEM_UNSTABLEDNA_DESC"
    rarity consumable_rare
    kind trinket
    frame 277
    durability [1 3]
    consumable true
	
	ability cm_UnstableDNA
}
```

---

### `RedPill`
**Name:** Red Pill  
**Description:** Use: 50% chance to get Chungus (+4 [img:con]), otherwise take 8 damage.  
**Source:** `consumables.gon`  

```
RedPill {
    name "ITEM_REDPILL_NAME"
    desc "ITEM_REDPILL_DESC"
    rarity consumable_rare
    kind trinket
    frame 278
    durability 1
    consumable true
	
	ability cm_RedPill
}
```

---

### `ForbiddenPill`
**Name:** Forbidden Pill  
**Description:** Use: Temporarily upgrade all of your active abilities.
There will be permanent consequences for taking this pill.  
**Source:** `consumables.gon`  

```
ForbiddenPill {
    name "ITEM_FORBIDDENPILL_NAME"
    desc "ITEM_FORBIDDENPILL_DESC"
    rarity consumable_very_rare
    kind trinket
    frame 279
    durability 1
    consumable true
	
	ability cm_ForbiddenPill
}
```

---

### `MissingNipple`
**Name:** Missing Nipple  
**Description:** Use: Give an adjacent unit +1 Health Regen.  
**Source:** `consumables.gon`  

```
MissingNipple {
    name "ITEM_MISSINGNIPPLE_NAME"
    desc "ITEM_MISSINGNIPPLE_DESC"
    rarity consumable_rare
    kind trinket
    frame 272
	durability 6
	consumable true
    
	ability cm_Nipple
}
```

---

### `Experimentx`
**Name:** Experiment X  
**Description:** Use: ???  
**Source:** `consumables.gon`  

```
Experimentx {
    name "ITEM_EXPERIMENTX_NAME"
    desc "ITEM_EXPERIMENTX_DESC"
    rarity rare
    kind trinket
    frame 285
	durability 1
	consumable true
	set Experimental
    
    ability cm_ExperimentX
}
```

---

### `StevensConsumable1`
**Name:** Steven  
**Description:** Use: Permanently upgrade a random spell or passive ability.  
**Source:** `consumables.gon`  

```
StevensConsumable1 {
    name "ITEM_STEVENSCONSUMABLE1_NAME"
    desc "ITEM_STEVENSCONSUMABLE1_DESC"
    rarity rare
    kind trinket
    frame 235
	durability 1
	consumable true
	set Steven
    
    ability cm_Steven1
}
```

---

### `StevensConsumable2`
**Name:** Steven  
**Description:** Use: Spawn a controllable copy of yourself.  
**Source:** `consumables.gon`  

```
StevensConsumable2 {
    name "ITEM_STEVENSCONSUMABLE2_NAME"
    desc "ITEM_STEVENSCONSUMABLE2_DESC"
    rarity rare
    kind trinket
    frame 237
	durability 1
	consumable true
	set Steven
    
    ability cm_Steven2
}
```

---

### `JokerCard`
**Name:** Joker Card  
**Description:** Use: Duplicate one of your equipped items.  
**Source:** `consumables.gon`  

```
JokerCard {
    name "ITEM_JOKERCARD_NAME"
    desc "ITEM_JOKERCARD_DESC"
    rarity very_rare
    kind trinket
    frame 268
	durability 1
	consumable true
	set [Jester, Paper]
    
    ability cm_JokerCard
}
```

---

### `Gizzard`
**Name:** Gizzard  
**Description:** Use: Enter Mockingbird Form. Gain a random bird mutation at the end of the battle.  
**Source:** `consumables.gon`  

```
Gizzard {
    name "ITEM_GIZZARD_NAME"
    desc "ITEM_GIZZARD_DESC"
    rarity consumable_rare
    kind trinket
    frame 194
	durability 1
	consumable true
	set Guts
    
    ability cm_Gizzard
}
```

---

## File: `cursed_items.gon`

### `AlluringDoodie`
**Name:** Alluring Doodie  
**Description:** 10% chance to eat poop and gain Poison 1 each turn.  
**Source:** `cursed_items.gon`  

```
AlluringDoodie {
    name "ITEM_ALLURINGDOODIE_NAME"
    desc "ITEM_ALLURINGDOODIE_DESC"
    kind head
    frame 15
    cursed true
    durability 5
	set Fecal

    passives {
        AlluringDoodieEater {
            chance 10%

            damage_instance {
                damage 0
                type status

                effects {
                    Poison 1
                }
            }
        }
    }
}
```

---

### `ChildSkull`
**Name:** Child's Skull  
**Description:** Your basic attack is a weak tear shot. You can use your basic attack an extra time each turn.  
**Source:** `cursed_items.gon`  

```
ChildSkull {
    name "ITEM_CHILDSSKULL_NAME"
    desc "ITEM_CHILDSSKULL_DESC"
    kind head
    frame 18
    cursed true
    set Bone

    attack IsaacBasicAttack
    shield 3
    passives {
        ExtraBasicAttacks 1
        OverrideBasicAttack IsaacBasicAttack
    }
}
```

---

### `PawShards`
**Name:** Paw Shards  
**Description:** Your basic attack inflicts Bleed 1. Gain +1 Bleed each time you use your basic attack.  
**Source:** `cursed_items.gon`  

```
PawShards {
    name "ITEM_PAWSHARDS_NAME"
    desc "ITEM_PAWSHARDS_DESC"
    kind weapon
    frame 23
    cursed true

    passives {
        AddStatusToBasicAttack {
            Bleed 1
        }
        AddSelfStatusToBasicAttack {
            Bleed 1
        }
    }
}
```

---

### `Splinters`
**Name:** Splinters  
**Description:** ITEM_SPLINTERS_DESC  
**Source:** `cursed_items.gon`  

```
Splinters {
    name "ITEM_SPLINTERS_NAME"
    desc "ITEM_SPLINTERS_DESC"
    kind weapon
    frame 22
    cursed true

    con -1
    str 1
}
```

---

### `FaceShards`
**Name:** Face Shards  
**Description:** +2 Thorns.
Gain +1 Bleed each time you take damage.  
**Source:** `cursed_items.gon`  

```
FaceShards {
    name "ITEM_FACESHARDS_NAME"
    desc "ITEM_FACESHARDS_DESC"
    kind face
    frame 22
    cursed true

    passives {
        Thorns 2
        StatusOnTookDamage {
            Bleed 1
        }
    }
}
```

---

### `BadSplinters`
**Name:** Bad Splinters  
**Description:** +2 Thorns.  
**Source:** `cursed_items.gon`  

```
BadSplinters {
    name "ITEM_BADSPLINTERS_NAME"
    desc "ITEM_BADSPLINTERS_DESC"
    kind neck
    frame 17
    cursed true

    con -2

    passives {
        Thorns 2
    }
}
```

---

### `CursedHairball`
**Name:** Cursed Hairball  
**Description:** Your basic attack inflicts Poison 2. Start each battle with Poison 3.  
**Source:** `cursed_items.gon`  

```
CursedHairball {
    name "ITEM_CURSEDHAIRBALL_NAME"
    desc "ITEM_CURSEDHAIRBALL_DESC"
    kind trinket
    frame 79
    cursed true

    passives {
        Poison 3
        AddStatusToBasicAttack {
            Poison 2
        }
    }
}
```

---

### `MarkOfTheBeast`
**Name:** Mark of the Beast  
**Description:** +6 Damage. Holy Element heals damage you instead.
When downed, your body is destroyed.  
**Source:** `cursed_items.gon`  

```
MarkOfTheBeast { //Unique item given from Baphomet event
    name "ITEM_MARKOFTHEBEAST_NAME"
    desc "ITEM_MARKOFTHEBEAST_DESC"
    kind face
    frame 63
    cursed true

    passives {
        DamageUp 6
        Undead 1
        AddCorpseHealth -999999
    }
}
```

---

### `PutridPile`
**Name:** Putrid Pile  
**Description:** Adjacent units move away from you at the end of their turns.
Your basic attack inflicts Poison.  
**Source:** `cursed_items.gon`  

```
PutridPile {
    name "ITEM_PUTRIDPILE_NAME"
    desc "ITEM_PUTRIDPILE_DESC"
    kind trinket
    rarity uncommon
    cursed true
    frame 70
    
    cha -1

    passives {
	    AddStatusToBasicAttack {
            Poison 1
		}
        StatusAdjacentOnTheirTurnEnd {
            ForceMoveAway 1
        }
    }
}
```

---

### `VibratingMeteorite`
**Name:** Vibrating Meteorite  
**Description:** This item loses 1 of each stat at the end of each battle, permanently.
\[s:.7\](This can go negative.)\[/s\]  
**Source:** `cursed_items.gon`  

```
VibratingMeteorite {
    name "ITEM_VIBRATINGMETEORITE_NAME"
    desc "ITEM_VIBRATINGMETEORITE_DESC"
    rarity rare
    kind trinket
    cursed true
    frame 202
    aux 3
    
    str aux
    dex aux
    con aux
    int aux
    spd aux
    cha aux
    lck aux
    
    passives {
        StatusOnBattleEnd {
            SetItemAux {
                slot trinket
                value item_aux-1
            }
            even_if_dead true
        }
    }
}
```

---

### `CursedRock`
**Name:** Cursed Rock  
**Description:** ITEM_CURSEDROCK_DESC  
**Source:** `cursed_items.gon`  

```
CursedRock {
    name "ITEM_CURSEDROCK_NAME"
    desc "ITEM_CURSEDROCK_DESC"
    kind trinket
    frame 56
    cursed true

    shield 6
    str -2
}
```

---

### `Clam`
**Name:** Clam  
**Description:** 5% chance to break when you take damage.
When this breaks, find a Pearl.  
**Source:** `cursed_items.gon`  

```
Clam {
    name "ARMOR_CLAM_NAME"
    desc "ARMOR_CLAM_DESC"
    kind face
    frame 59
    cursed true

    cha -1

    passives {
        ArmorBreakOnHit {
            durability_loss 0
            chance_to_break 5%
        }
        StatusOnBreak {
            FindItem Pearl
        }
    }
}
```

---

### `BirdPoopHat`
**Name:** Bird Poop  
**Description:** +50% chance for an extra bird to spawn at the start of each battle.  
**Source:** `cursed_items.gon`  

```
BirdPoopHat {
    name "ARMOR_BIRDPOOPHAT_NAME"
    desc "ARMOR_BIRDPOOPHAT_DESC"
    kind head
    frame 30
    cursed true
	set Fecal //Bird

    cha -1	
    passives {
        SpawnOnBattleStartRandomEmptyTile {
            object Bird
            number [0 1]
        }
    }
}
```

---

### `Callus`
**Name:** Callus  
**Description:** Permanently gain +2 [img:shield] each time you end a battle with 1 or more [img:shield].  
**Source:** `cursed_items.gon`  

```
Callus {
    name "ARMOR_CALLUS_NAME"
    desc "ARMOR_CALLUS_DESC"
    rarity uncommon
    kind face
    frame 140
    cursed true

    aux 2
    shield aux

    passives {
        StatusOnBattleEnd {
            Conditional_Shielded {
                SetItemAux {
                    slot face
                    value item_aux+2
                }
            }
        }
    }
}
```

---

### `SlagTight`
**Name:** Slag Tight  
**Description:** Brace 1. Your basic attack inflicts Bruise 1.  
**Source:** `cursed_items.gon`  

```
SlagTight { //Unique item given from Jagged Pathway event
    name "ITEM_SLAGTIGHT_NAME"
    desc "ITEM_SLAGTIGHT_DESC"
    kind head
    frame 170
    cursed true

    int -4
    shield 5
    passives {
        Brace 1
        AddStatusToBasicAttack {
            Bruise 1
        }
    }
}
```

---

### `MetalRod`
**Name:** Metal Rod  
**Description:** Use: A melee attack with Knockback 1 and a 10% chance to inflict Stun.  
**Source:** `cursed_items.gon`  

```
MetalRod { //Unique item given from Wall of Cats event
    name "ITEM_METALROD_NAME"
    desc "ITEM_METALRODHAT_DESC"
    kind head
    frame 64
    cursed true

    int -1
    con -1
    ability wp_MetalRod
}
```

---

### `BigToeCursed`
**Name:** Big Toe  
**Description:** After your 3rd turn, spawn a Charmed Spookie with Madness on a random tile.  
**Source:** `cursed_items.gon`  

```
BigToeCursed { //Aquired from Big Toe event
    name "ITEM_BIGTOECURSED_NAME"
    desc "ITEM_BIGTOECURSED_DESC"
    kind trinket
    frame 266
    cursed true
    
    passives {
        StatusAfterXTurns {
            stacks 3
            ForceUseAbility tk_MadGhost_Spawn
        }
    }
}
```

---

### `GoldenIdol`
**Name:** Golden Idol  
**Description:** Becomes {aux} coins when you return home.  
**Source:** `cursed_items.gon`  

```
GoldenIdol { //Aquired from PitOfSnakes event
    name "ITEM_GOLDENIDOL_NAME"
    desc "ITEM_GOLDENIDOL_DESC"
    kind trinket
    frame 266
    cursed true
	on_store become_aux_coins
    aux 500

    lck -2
}
```

---

## File: `enemy_items.gon`

### `MageCollar`
**Source:** `enemy_items.gon`  

```
MageCollar {
    name ""
    desc ""
    kind neck
    frame 6
	int 2
}
```

---

### `MetalPlate`
**Source:** `enemy_items.gon`  

```
MetalPlate {
    name ""
    desc ""
    kind face
    frame 18
	con 2

    passives {
        Metal 1
    }
}
```

---

### `HuntersPatch`
**Source:** `enemy_items.gon`  

```
HuntersPatch {
    name ""
    desc ""
    kind face
    frame 19
	dex 2
}
```

---

### `AngelicAura`
**Source:** `enemy_items.gon`  

```
AngelicAura {
    name ""
    desc ""
    kind neck
    frame 7
	int 1
	con 1
}
```

---

### `CoinBag`
**Source:** `enemy_items.gon`  

```
CoinBag {
    name ""
    desc ""
    kind head
    frame 13
	speed 1
}
```

---

### `SamsonsChains`
**Source:** `enemy_items.gon`  

```
SamsonsChains {
    name ""
    desc ""
    kind neck
    frame 8
	str 2

    passive {
        Metal 1
    }
}
```

---

### `Banana`
**Source:** `enemy_items.gon`  

```
Banana {
    name ""
    desc ""
    kind head
    frame 14
	cha -1
}
```

---

### `Slime`
**Source:** `enemy_items.gon`  

```
Slime {
    name ""
    desc ""
    kind neck
    frame 14
	cha -1
}
```

---

### `GunslingerPistol`
**Name:** Gunslinger Pistol  
**Source:** `enemy_items.gon`  

```
GunslingerPistol {
    name "ITEM_GUNSLINGERPISTOL_NAME"
    desc ""
    kind weapon
    frame 51
    durability 6

    ability wp_GunslingerPistol
}
```

---

### `WesternHat`
**Source:** `enemy_items.gon`  

```
WesternHat {
    name ""
    desc ""
    kind face
    frame 52
}
```

---

### `Poncho`
**Source:** `enemy_items.gon`  

```
Poncho {
    name ""
    desc ""
    kind neck
    frame 43
}
```

---

### `AtomicMark`
**Source:** `enemy_items.gon`  

```
AtomicMark {
    name ""
    desc ""
    kind face
    frame 64

    int 2
}
```

---

### `AstroTaser`
**Name:** Astro Zapper  
**Source:** `enemy_items.gon`  

```
AstroTaser {
    name "ITEM_ASTROTASER_NAME"
    desc ""
    kind weapon
    frame 84
    
    ability wp_AstroTaser
}
```

---

### `OddRemote_Enemy`
**Name:** Odd Remote  
**Description:** Use: Cast a random spell.  
**Source:** `enemy_items.gon`  

```
OddRemote_Enemy {
    name "ITEM_ODDREMOTE_NAME"
    desc "ITEM_ODDREMOTE_DESC"
    kind weapon
    frame 95

    ability wp_OddRemoteEnemy
}
```

---

### `Pebble`
**Source:** `enemy_items.gon`  

```
Pebble {
    name ""
    desc ""
    kind head
    frame 92

    shield 2
}
```

---

### `Dreadlocks`
**Source:** `enemy_items.gon`  

```
Dreadlocks {
    name ""
    desc ""
    kind head
    frame 93

}
```

---

### `BabyHair`
**Source:** `enemy_items.gon`  

```
BabyHair {
    name ""
    desc ""
    kind head
    frame 94

}
```

---

### `BulbHead`
**Source:** `enemy_items.gon`  

```
BulbHead {
    name ""
    desc ""
    kind head
    frame 95

}
```

---

### `MuggerMask`
**Source:** `enemy_items.gon`  

```
MuggerMask {
    name ""
    desc ""
    kind face
    frame 113

}
```

---

### `NecromancerMask`
**Source:** `enemy_items.gon`  

```
NecromancerMask {
    name ""
    desc ""
    kind face
    frame 120
}
```

---

### `TinkererHat`
**Source:** `enemy_items.gon`  

```
TinkererHat {
    name ""
    desc ""
    kind head
    frame 120
}
```

---

### `ButcherMask`
**Source:** `enemy_items.gon`  

```
ButcherMask {
    name ""
    desc ""
    kind face
    frame 122
}
```

---

### `PsychicMask`
**Source:** `enemy_items.gon`  

```
PsychicMask {
    name ""
    desc ""
    kind face
    frame 121
}
```

---

### `JesterHat`
**Source:** `enemy_items.gon`  

```
JesterHat {
    name ""
    desc ""
    kind head
    frame 121
}
```

---

### `MonkMask`
**Source:** `enemy_items.gon`  

```
MonkMask {
    name ""
    desc ""
    kind face
    frame 123
}
```

---

### `DruidNeck`
**Source:** `enemy_items.gon`  

```
DruidNeck {
    name ""
    desc ""
    kind neck
    frame 120
}
```

---

### `TerminatorShotgun`
**Name:** Shotgun  
**Source:** `enemy_items.gon`  

```
TerminatorShotgun {
    name "ITEM_SHOTGUN_NAME"
    desc ""
    kind weapon
    frame 50
    
    ability wp_TerminatorShotgun

}
```

---

### `TerminatorSniper`
**Name:** Sniper Rifle  
**Source:** `enemy_items.gon`  

```
TerminatorSniper {
    name "ITEM_SNIPERRIFLE_NAME"
    desc ""
    kind weapon
    frame 52
    
    ability wp_TerminatorSniper
}
```

---

### `TerminatorUzi`
**Name:** Submachine Gun  
**Source:** `enemy_items.gon`  

```
TerminatorUzi {
    name "ITEM_UZI_NAME"
    desc ""
    kind weapon
    frame 137
    
    ability wp_TerminatorUzi

}
```

---

### `TerminatorCoolGlasses`
**Name:** Cool Glasses  
**Source:** `enemy_items.gon`  

```
TerminatorCoolGlasses {
    name "ARMOR_COOLMASK_NAME"
    desc ""
    kind face
    frame 10
}
```

---

### `TerminatorCoolGlasses2`
**Source:** `enemy_items.gon`  

```
TerminatorCoolGlasses2 {
    name ""
    desc ""
    kind face
    frame 94
}
```

---

### `CaveCatClub`
**Name:** Club  
**Source:** `enemy_items.gon`  

```
CaveCatClub {
    name "ITEM_CAVECATCLUB_NAME"
    desc ""
    kind weapon
    frame 1
    ability wp_CaveCatClub
}
```

---

### `SuperDunceCap`
**Source:** `enemy_items.gon`  

```
SuperDunceCap { //test item
    name ""
	desc ""
    kind head
    frame 91

    int -10
}
```

---

### `MageCollar_Terminator`
**Source:** `enemy_items.gon`  

```
MageCollar_Terminator {
    name ""
	desc ""
    kind neck
    frame 137
	int 2
}
```

---

### `MetalPlate_Terminator`
**Source:** `enemy_items.gon`  

```
MetalPlate_Terminator {
    name ""
	desc ""
    kind face
    frame 153
	con 2

    passives {
        Metal 1
    }
}
```

---

### `HuntersPatch_Terminator`
**Source:** `enemy_items.gon`  

```
HuntersPatch_Terminator {
    name ""
	desc ""
    kind face
    frame 149
	dex 2
}
```

---

### `AngelicAura_Terminator`
**Source:** `enemy_items.gon`  

```
AngelicAura_Terminator {
    name ""
	desc ""
    kind neck
    frame 139
	int 1
	con 1
}
```

---

### `CoinBag_Terminator`
**Source:** `enemy_items.gon`  

```
CoinBag_Terminator {
    name ""
	desc ""
    kind head
    frame 164
	speed 1
}
```

---

### `SamsonsChains_Terminator`
**Source:** `enemy_items.gon`  

```
SamsonsChains_Terminator {
    name ""
	desc ""
    kind neck
    frame 138
	str 2

    passive {
        Metal 1
    }
}
```

---

### `NecromancerMask_Terminator`
**Source:** `enemy_items.gon`  

```
NecromancerMask_Terminator {
    name ""
	desc ""
    kind face
    frame 150
}
```

---

### `TinkererHat_Terminator`
**Source:** `enemy_items.gon`  

```
TinkererHat_Terminator {
    name ""
	desc ""
    kind head
    frame 166
}
```

---

### `ButcherMask_Terminator`
**Source:** `enemy_items.gon`  

```
ButcherMask_Terminator {
    name ""
	desc ""
    kind face
    frame 152
}
```

---

### `PsychicMask_Terminator`
**Source:** `enemy_items.gon`  

```
PsychicMask_Terminator {
    name ""
	desc ""
    kind face
    frame 151
}
```

---

### `JesterHat_Terminator`
**Source:** `enemy_items.gon`  

```
JesterHat_Terminator {
    name ""
	desc ""
    kind head
    frame 167
}
```

---

### `MonkMask_Terminator`
**Source:** `enemy_items.gon`  

```
MonkMask_Terminator {
    name ""
	desc ""
    kind head
    frame 165
}
```

---

### `DruidNeck_Terminator`
**Source:** `enemy_items.gon`  

```
DruidNeck_Terminator {
    name ""
	desc ""
    kind neck
    frame 140
}
```

---

### `Pebble_Terminator`
**Source:** `enemy_items.gon`  

```
Pebble_Terminator {
    name ""
	desc ""
    kind head
    frame 169

    shield 2
}
```

---

### `LoansharksFedora`
**Source:** `enemy_items.gon`  

```
LoansharksFedora {
    name ""
	desc ""
    rarity very_rare
    kind head
    frame 192

    passives {
		CritChanceUp 100
    }
}
```

---

### `Rabiesface`
**Source:** `enemy_items.gon`  

```
Rabiesface {
	name ""
	desc ""
	kind face
	frame 11

	passives {

	}
}
```

---

## File: `face_items.gon`

### `Mustache`
**Name:** Mustache  
**Description:** ARMOR_MUSTACHE_DESC  
**Source:** `face_items.gon`  

```
Mustache {
    name "ARMOR_MUSTACHE_NAME"
    desc "ARMOR_MUSTACHE_DESC"
    rarity common
    kind face
    frame 5
	set Man

    cha 1
    //TODO: cat becomes male
}
```

---

### `Glasses`
**Name:** Glasses  
**Description:** ARMOR_GLASSES_DESC  
**Source:** `face_items.gon`  

```
Glasses {
    name "ARMOR_GLASSES_NAME"
    desc "ARMOR_GLASSES_DESC"
    rarity uncommon
    kind face
    frame 1

    int 2
    con -1
}
```

---

### `Muzzle`
**Name:** Muzzle  
**Description:** ARMOR_MUZZLE_DESC  
**Source:** `face_items.gon`  

```
Muzzle {
    name "ARMOR_MUZZLE_NAME"
    desc "ARMOR_MUZZLE_DESC"
    rarity uncommon
    kind face
    frame 4
	set Gimp

    str -2
    cha 1
    int 1

    shield 2
}
```

---

### `FaceCovering`
**Name:** Face Covering  
**Description:** ARMOR_FACECOVERING_DESC  
**Source:** `face_items.gon`  

```
FaceCovering {
    name "ARMOR_FACECOVERING_NAME"
    desc "ARMOR_FACECOVERING_DESC"
    rarity common
    kind face
    frame 6
	set [Medical, Nurse]

    con 1

    passives {
        CantCatchDiseases 1
        CantSpreadDiseases 1
    }
}
```

---

### `Bozo`
**Name:** Bozo  
**Description:** Your basic attack has a +15% chance to inflict Fear.  
**Source:** `face_items.gon`  

```
Bozo {
    name "ARMOR_BOZO_NAME"
    desc "ARMOR_BOZO_DESC"
    rarity uncommon
    kind face
    frame 7
	set Jester

    int -1
    cha 2

    passives {
        AddStatusToBasicAttack {
            Fear [1 .15]
        }
    }
}
```

---

### `Bandage`
**Name:** Bandage  
**Description:** +2 Health Regen.  
**Source:** `face_items.gon`  

```
Bandage {
    name "ARMOR_BANDAGE_NAME"
    desc "ARMOR_BANDAGE_DESC"
    rarity uncommon
    kind face
    frame 9
	set Nurse

    con -1

    passives {
        HealthRegenUp 2
    }
}
```

---

### `MysticalBlindfold`
**Name:** Mystical Blindfold  
**Description:** Your physical attacks and abilities always miss.  
**Source:** `face_items.gon`  

```
MysticalBlindfold {
    name "ARMOR_MYSTICALBLINDFOLD_NAME"
    desc "ARMOR_MYSTICALBLINDFOLD_DESC"
    rarity rare
    kind face
    frame 28
	set Rag

    int 4
    cha 2

    passives {
        PhysicalAttacksMiss 1
    }
}
```

---

### `ThirdEye`
**Name:** Third Eye  
**Description:** +1 range.
Your ranged attacks can't miss.  
**Source:** `face_items.gon`  

```
ThirdEye {
    name "ARMOR_THIRDEYE_NAME"
    desc "ARMOR_THIRDEYE_DESC"
    rarity rare
    kind face
    frame 29
    set [Psychic, Hybrid]

    passives {
        RangedTrueShot 1
        AddBonusRange 1
    }
}
```

---

### `Flower`
**Name:** Flower  
**Description:** Spawn flowers under you when you end your turn.
+1 Health Regen.  
**Source:** `face_items.gon`  

```
Flower {
    name "ARMOR_FLOWER_NAME"
    desc "ARMOR_FLOWER_DESC"
    rarity uncommon
    kind face
    frame 30
	set Flower

    passives {
        FlowersOnEndTurn 1
		HealthRegenUp 1
    }
}
```

---

### `HockeyMask`
**Name:** Hockey Mask  
**Description:** While downed, you have a 25% chance to revive with 1 HP at the end of the round.  
**Source:** `face_items.gon`  

```
HockeyMask {
    name "ARMOR_HOCKEYMASK_NAME"
    desc "ARMOR_HOCKEYMASK_DESC"
    rarity uncommon
    kind face
    frame 27
	
	shield 5

    passives {
        ChanceToRevive 25
    }
}
```

---

### `BanditMask`
**Name:** Bandit Mask  
**Description:** Your basic attack spawns 1 coin when it deals damage.  
**Source:** `face_items.gon`  

```
BanditMask {
    name "ARMOR_BANDITMASK_NAME"
    desc "ARMOR_BANDITMASK_DESC"
    rarity common
    kind face
    frame 3
	set Thief

    passives {
        AddStatusToBasicAttack {
            KnockOutCoin 1
        }
    }
}
```

---

### `InfamousMask`
**Name:** Infamous Mask  
**Description:** Block attacks from the front.  
**Source:** `face_items.gon`  

```
InfamousMask {
    name "ARMOR_INFAMOUSMASK_NAME"
    desc "ARMOR_INFAMOUSMASK_DESC"
    rarity rare
    kind face
	set Lead
    frame 2

    spd -2

    passives {
        FaceShield 1
    }
}
```

---

### `BearTrapMask`
**Name:** Bear Trap Mask  
**Description:** +1 Bleed Thorns.  
**Source:** `face_items.gon`  

```
BearTrapMask {
    name "ARMOR_BEARTRAPMASK_NAME"
    desc "ARMOR_BEARTRAPMASK_DESC"
    rarity uncommon
    kind face
	set Lead
    frame 62

    shield 4

    passives {
        Metal 1
        BleedThorns 1
    }
}
```

---

### `PinsAndNeedles`
**Name:** Pins and Needles  
**Description:** +1 Thorns.
Gain +1 Charge when you take damage.  
**Source:** `face_items.gon`  

```
PinsAndNeedles {
    name "ARMOR_PINSANDNEEDLES_NAME"
    desc "ARMOR_PINSANDNEEDLES_DESC"
    rarity uncommon
    kind face
    frame 65
	set Gimp

    passives {
        Metal 1
        Thorns 1
        StatusOnTookDamage {
            Charge 1
        }
    }
}
```

---

### `NinjaBandana`
**Name:** Ninja Bandana  
**Description:** You have a 10% chance to gain a bonus attack when you use your basic attack.  
**Source:** `face_items.gon`  

```
NinjaBandana {
    name "ARMOR_NINJABANDANA_NAME"
    desc "ARMOR_NINJABANDANA_DESC"
    rarity uncommon
    kind face
    frame 66
    set Ninja

    passives {
        AddSelfStatusToBasicAttack {
            Quivered [1 .10]
        }
    }
}
```

---

### `Monocle`
**Name:** Monocle  
**Description:** Your physical attacks can't miss.  
**Source:** `face_items.gon`  

```
Monocle {
    name "ARMOR_MONOCLE_NAME"
    desc "ARMOR_MONOCLE_DESC"
    rarity uncommon
    kind face
    frame 67

    cha 1

    passives {
        TrueShot 1
    }
}
```

---

### `PhantomMask`
**Name:** Phantom Mask  
**Description:** +10% chance to Block attacks.
When you take damage, this becomes an invincible familiar.  
**Source:** `face_items.gon`  

```
PhantomMask {
    name "ARMOR_PHANTOMMASK_NAME"
    desc "ARMOR_PHANTOMMASK_DESC"
    rarity very_rare
    kind face
    frame 69

    shield 3

    passives {
        ChanceToBlock 10%
        DropAsFamiliarOnTookDamage PhantomMaskRock
    }
}
```

---

### `WhiteBelt`
**Name:** White Belt  
**Description:** +1 Brace.  
**Source:** `face_items.gon`  

```
WhiteBelt {
    name "ARMOR_WHITEBELT_NAME"
    desc "ARMOR_WHITEBELT_DESC"
    rarity common
    kind face
    frame 71

    passives {
        Brace 1
    }
}
```

---

### `BrownBelt`
**Name:** Brown Belt  
**Description:** +1 Damage.
If you end your turn with unused basic attacks, gain that many Backflips.  
**Source:** `face_items.gon`  

```
BrownBelt {
    name "ARMOR_BROWNBELT_NAME"
    desc "ARMOR_BROWNBELT_DESC"
    rarity uncommon
    kind face
    frame 72

    passives {
        DamageUp 1
        StatusIfUnusedActPoints {
            BackflipWhenTargeted X
        }
    }
}
```

---

### `BlackBelt`
**Name:** Black Belt  
**Description:** 25% chance to block attacks and counter attack.  
**Source:** `face_items.gon`  

```
BlackBelt {
    name "ARMOR_BLACKBELT_NAME"
    desc "ARMOR_BLACKBELT_DESC"
    rarity rare
    kind face
    frame 73

    passives {
        ChanceToBlockAndCounter 25%
    }
}
```

---

### `EyeOfRa`
**Name:** Eye of Ra  
**Description:** Your basic attack inflicts Burn 1 and Blind 1.
Inflict Burn 1 and Blind 1 on units that contact or attack you.  
**Source:** `face_items.gon`  

```
EyeOfRa { //Unique item from looting the Mysterious Tomb.
    name "ARMOR_EYEOFRA_NAME"
    desc "ARMOR_EYEOFRA_DESC"
    rarity very_rare
    kind face
    frame 154
    
    passives {
        AddStatusToBasicAttack {
            Burn 1
            Blind 1
        }
        RevengeDamage {
            effects {
                Burn 1
                Blind 1
            }
        }
    }
}
```

---

### `Bandages`
**Name:** Bandages  
**Description:** Heals heal you for twice as much.  
**Source:** `face_items.gon`  

```
Bandages {
    name "ARMOR_BANDAGES_NAME"
    desc "ARMOR_BANDAGES_DESC"
    rarity rare
    kind face
    frame 132
	set Nurse

    passives {
        MultiplyReceivedHealing 2
    }
}
```

---

### `HorseBlinders`
**Name:** Horse Blinders  
**Description:** Your abilities have 100% accuracy and +50% Crit Chance.
You are unable to hit any unit that isn't in a straight line directly in front of you.  
**Source:** `face_items.gon`  

```
HorseBlinders {
    name "ARMOR_HORSEBLINDERS_NAME"
    desc "ARMOR_HORSEBLINDERS_DESC"
    rarity rare
    kind face
    frame 138
	set [Leather, Gimp]

    passives {
        TunnelVision {
            crit_chance 50%
        }
    }
}
```

---

### `SurvivalistMask`
**Name:** Survivalist's Mask  
**Description:** Bodies you destroy spawn food, catnip and a coin.  
**Source:** `face_items.gon`  

```
SurvivalistMask {
    name "ARMOR_SURVIVALISTMASK_NAME"
    desc "ARMOR_SURVIVALISTMASK_DESC"
    rarity uncommon
    kind face
    frame 135
	set Survivalist 

    passives {
        SpawnObjectOnPopCorpse Food
        SpawnObjectOnPopCorpse Coin
        SpawnObjectOnPopCorpse Catnip
    }
}
```

---

### `LeechBrood`
**Name:** Leech Brood  
**Description:** Inflict Leech 1 to all enemies at the start of each battle.
Start each battle at 50% health.  
**Source:** `face_items.gon`  

```
LeechBrood {
    name "ARMOR_LEECHBROOD_NAME"
    desc "ARMOR_LEECHBROOD_DESC"
    rarity rare
    kind face
    frame 136
	set Leech

    passives {
        AbilityOnBattleStart face_LeechBrood
        StatusOnBattleStart {
            SetHealth 50%
        }
    }
}
```

---

### `GlyphOfProtection`
**Name:** Glyph of Protection  
**Description:** Gain +1 [img:shield] each time you cast a spell.  
**Source:** `face_items.gon`  

```
GlyphOfProtection {
    name "ARMOR_GLYPHOFPROTECTION_NAME"
    desc "ARMOR_GLYPHOFPROTECTION_DESC"
    rarity very_rare
    kind face
    frame 142
	set Cleric

    passives {
        StatusOnCastSpell {
            Shield 1
        }
    }
}
```

---

### `FeatheredMask`
**Name:** Feathered Mask  
**Description:** +10% Dodge Chance.  
**Source:** `face_items.gon`  

```
FeatheredMask {
    name "ARMOR_FEATHEREDMASK_NAME"
    desc "ARMOR_FEATHEREDMASK_DESC"
    rarity common
    kind face
    frame 183
	set Feathered

    passives {
        ArmorDodgeChance 10%
    }
}
```

---

### `Debris`
**Name:** Debris  
**Description:** +1 Brace.  
**Source:** `face_items.gon`  

```
Debris {
    name "ARMOR_DEBRIS_NAME"
    desc "ARMOR_DEBRIS_DESC"
    rarity common
    kind face
    frame 182
	set [Debris, Scrap]

    passives {
        Metal 1
        Brace 1
    }
}
```

---

### `MudMask`
**Name:** Mud Mask  
**Description:** Fragile and Brittle while wet.  
**Source:** `face_items.gon`  

```
MudMask {
    name "ARMOR_MUDMASK_NAME"
    desc "ARMOR_MUDMASK_DESC"
    rarity common
    kind face
    frame 181
	set DirtClod

	shield 3

    passives {
        FragileDuringElement water
        BrittleDuringElement water
    }
}
```

---

### `VisionPlugin`
**Name:** Vision Plugin  
**Description:** +1 range.  
**Source:** `face_items.gon`  

```
VisionPlugin {
    name "ARMOR_VISIONPLUGIN_NAME"
    desc "ARMOR_VISIONPLUGIN_DESC"
    rarity common
    kind face
    frame 173
	set [Cyborg, Bionic, Chip]

    passives {
        Metal 1
        AddBonusRange 1
    }
}
```

---

### `RubberBand`
**Name:** Rubber Band  
**Description:** +1 reach.  
**Source:** `face_items.gon`  

```
RubberBand {
    name "ARMOR_RUBBERBAND_NAME"
    desc "ARMOR_RUBBERBAND_DESC"
    rarity uncommon
    kind face
    frame 174
	set Rubber

    passives {
        AddBonusMeleeRange 1
    }
}
```

---

### `MuertosMask`
**Name:** Muertos Mask  
**Description:** +6 Corpse Health.  
**Source:** `face_items.gon`  

```
MuertosMask {
    name "ARMOR_MUERTOSMASK_NAME"
    desc "ARMOR_MUERTOSMASK_DESC"
    rarity common
    kind face
    frame 176
	set Necromancer
	
	shield 2

    passives {
        AddCorpseHealth 6
    }
}
```

---

### `RhinestoneStickers`
**Name:** Rhinestone Stickers  
**Description:** Emit 4 Sparkles at the start of each battle.  
**Source:** `face_items.gon`  

```
RhinestoneStickers {
    name "ARMOR_RHINESTONESTICKERS_NAME"
    desc "ARMOR_RHINESTONESTICKERS_DESC"
    rarity common
    kind face
    frame 179
	set Gemstone

    passives {
		StatusOnBattleStart {
			RandomMagicMissile 4
		}	
	}	
}
```

---

### `BlessedAshes`
**Name:** Blessed Ashes  
**Description:** Gain +3 [img:shield] once per battle when your HP is 3 or less.  
**Source:** `face_items.gon`  

```
BlessedAshes {
    name "ARMOR_BLESSEDASHES_NAME"
    desc "ARMOR_BLESSEDASHES_DESC"
    rarity uncommon
    kind face
    frame 172
	set Cleric

    shield 3

    passives {
        StatusOnTookDamage {
            Conditional_HealthThreshold {
                threshold_flat 3
                Conditional_OncePerBattle {
                    Shield 3
                }
            }
        }
    }
}
```

---

### `AttractiveHairClip`
**Name:** Attractive Hair Clip  
**Description:** After you're downed, the next time an allied cat takes a turn, they take an extra turn.  
**Source:** `face_items.gon`  

```
AttractiveHairClip {
    name "ARMOR_ATTRACTIVEHAIRCLIP_NAME"
    desc "ARMOR_ATTRACTIVEHAIRCLIP_DESC"
    rarity uncommon
    kind face
    frame 178
	set Used

    passives {
        StatusOnDie {
            CreateGlobalModifiers {
                NextPlayerCatTakesExtraTurn 1
            }
        }
    }
}
```

---

### `ChampionsMask`
**Name:** Champion's Mask  
**Description:** Gain +1 [img:{str_aux}] until the end of the battle each time you kill a unit.  
**Source:** `face_items.gon`  

```
ChampionsMask {
    name "ARMOR_CHAMPIONSMASK_NAME"
    desc "ARMOR_CHAMPIONSMASK_DESC"
    rarity uncommon
    kind face
    frame 184

    shield 3
    str_aux_initialize random_stat

    passives {
        // can't help but feel like there's gotta be a better way to do this but this will have to do for now
        PassiveIfStrAuxEquals {
            value str
            passives {
                StatusOnKill {
                    StrengthUp 1
                }
            }
        }
        PassiveIfStrAuxEquals {
            value dex
            passives {
                StatusOnKill {
                    DexterityUp 1
                }
            }
        }
        PassiveIfStrAuxEquals {
            value con
            passives {
                StatusOnKill {
                    ConstitutionUp 1
                }
            }
        }
        PassiveIfStrAuxEquals {
            value spd
            passives {
                StatusOnKill {
                    SpeedUp 1
                }
            }
        }
        PassiveIfStrAuxEquals {
            value int
            passives {
                StatusOnKill {
                    IntelligenceUp 1
                }
            }
        }
        PassiveIfStrAuxEquals {
            value cha
            passives {
                StatusOnKill {
                    CharismaUp 1
                }
            }
        }
        PassiveIfStrAuxEquals {
            value lck
            passives {
                StatusOnKill {
                    LuckUp 1
                }
            }
        }
    }
}
```

---

### `BarbedScrap`
**Name:** Barbed Scrap  
**Description:** +1 Thorns, +1 Damage.  
**Source:** `face_items.gon`  

```
BarbedScrap {
	name "ARMOR_BARBEDSCRAP_NAME"
	desc "ARMOR_BARBEDSCRAP_DESC"
	rarity very_rare
	kind face
	frame 185
	set [Barbed, Scrap]

	shield 4

	passives {
		Thorns 1
		DamageUp 1
		Metal 1
    }
}
```

---

### `LeatherHideMask`
**Name:** Leather Hide Mask  
**Description:** +1 Brace, +1 Health Regen, 5% chance to spawn a Charmed Flea each turn.  
**Source:** `face_items.gon`  

```
LeatherHideMask {
	name "ARMOR_LEATHERHIDEMASK_NAME"
	desc "ARMOR_LEATHERHIDEMASK_DESC"
	rarity very_rare
	kind face
	frame 186
	set [CatHide, Leather]

	shield 4

	passives {
		HealthRegenUp 1
		Brace 1
		SpawnEachTurn {
			chance 5%
			object CharmedFlea
			
			stack_key CATHIDE
		}
	}
}
```

---

### `RecycledGimpMask`
**Name:** Recycled Ball Gag  
**Description:** Gain +2 Charge when you take damage.
Find a common item when you are downed.  
**Source:** `face_items.gon`  

```
RecycledGimpMask {
	name "ARMOR_RECYCLEDGIMPMASK_NAME"
	desc "ARMOR_RECYCLEDGIMPMASK_DESC"
	rarity very_rare
	kind face
	frame 187
	set [Gimp, Recycled]
	
	shield 2

	passives {
	    StatusOnDie {
            FindItemFromPool chapter_common
        }
		StatusOnTookDamage {
			Charge 2
		}
	}
}
```

---

### `GemstoneBones`
**Name:** Gemstone Bones  
**Description:** +1 Kinetic Spikes. When you take damage, gain +1 [img:str]. When you are downed, emit 6 Sparkles.  
**Source:** `face_items.gon`  

```
GemstoneBones {
	name "ARMOR_GEMSTONEBONES_NAME"
	desc "ARMOR_GEMSTONEBONES_DESC"
	rarity very_rare
	kind face
	frame 188
	set [Bone, Gemstone]

	shield 4
	cha 1

	passives {
		KineticSpikes 1
		StatusOnTookDamage {
			StrengthUp 1
		}
		StatusOnDie {
			RandomMagicMissile 6
		}
	}
}
```

---

### `CoolRocks`
**Name:** Cool Rocks  
**Description:** Your basic attack has +1 Knockback.
When you are downed, gain coins.  
**Source:** `face_items.gon`  

```
CoolRocks {
	name "ARMOR_COOLROCKS_NAME"
	desc "ARMOR_COOLROCKS_DESC"
	rarity very_rare
	kind face
	frame 189
	set [Cool, Rock]

	cha 2

	shield 6
	spd -1
	
	passives {
		AddStatusToBasicAttack {
			Knockback 1
		}
		StatusOnDie {
			GainCoinsRange {
				min 1
				max 25
			}
		}
	}
}
```

---

### `MinerImplant`
**Name:** Miner Implant  
**Description:** +1 range, +1 reach.
Poison Immunity.  
**Source:** `face_items.gon`  

```
MinerImplant {
	name "ARMOR_MINERIMPLANT_NAME"
	desc "ARMOR_MINERIMPLANT_DESC"
	rarity very_rare
	kind face
	frame 190
	set [Miner, Cyborg]
	
	shield 7
	int 1

	passives {
		StatusImmunity Poison
		CantCatchDiseases 1
		CantSpreadDiseases 1
		AddBonusRange 1
        AddBonusMeleeRange 1
        Metal 1
	}
}
```

---

### `HolyTears`
**Name:** Holy Tears  
**Description:** Allies gain 2 [img:divineshield] when you are downed.
Your spells cost -1 mana.  
**Source:** `face_items.gon`  

```
HolyTears {
	name "ARMOR_HOLYTEARS_NAME"
	desc "ARMOR_HOLYTEARS_DESC"
	rarity very_rare
	kind face
	frame 191
	set Cleric
	
	divine_shield 2

	passives {
		ManaCostReduction 1
		StatusAlliesOnDeath {
			DivineShield 2
		}
	}
}
```

---

### `EyeOfGod`
**Name:** Eye Of God  
**Description:** +10 range. 
Your ranged attacks can't miss.  
**Source:** `face_items.gon`  

```
EyeOfGod {
    name "ARMOR_EYEOFGOD_NAME"
    desc "ARMOR_EYEOFGOD_DESC"
    rarity very_rare
    kind face
    frame 192
	set Hybrid
	
	divine_shield 1

    passives {
        RangedTrueShot 1
        AddBonusRange 10
    }
}
```

---

### `PeaceSymbolFacePaint`
**Name:** Peace Symbol Face Paint  
**Description:** Damage you deal to allies is reduced to 0.  
**Source:** `face_items.gon`  

```
PeaceSymbolFacePaint {
    name "ARMOR_PEACESYMBOLFACEPAINT_NAME"
    desc "ARMOR_PEACESYMBOLFACEPAINT_DESC"
    rarity rare
    kind face
    frame 194
	set Hippie

	passives {
		AllyDamageReduction 0
	}
}
```

---

### `HitlersMustache`
**Name:** Hitler's Mustache  
**Description:** Permanent Madness.
Take 2 extra turns at the start of each round.  
**Source:** `face_items.gon`  

```
HitlersMustache {
    name "ARMOR_HITLERSMUSTACHE_NAME"
    desc "ARMOR_HITLERSMUSTACHE_DESC"
    rarity very_rare
    kind face
    frame 196
	set [Man, Used]

	passives {
		PermanentMadness 1
		AlphaTurns -1
		AlphaTurns -1
	}
}
```

---

### `RadGlasses`
**Name:** Rad Glasses  
**Description:** Your explosions deal +1 damage and have +1 area.  
**Source:** `face_items.gon`  

```
RadGlasses {
    name "ARMOR_RADGLASSES_NAME"
    desc "ARMOR_RADGLASSES_DESC"
    rarity very_rare
    kind face
    frame 195
	set Cool
	
	cha 2

	passives {
		IncreaseExplosionSize 1
		IncreaseExplosionDamage 1
	}
}
```

---

### `FleshKid`
**Name:** Flesh Kid  
**Description:** You can't get injuries.
When you're downed, revive at the end of the round.
Your movement action is Jump.  
**Source:** `face_items.gon`  

```
FleshKid {
    name "ARMOR_FLESHKID_NAME"
    desc "ARMOR_FLESHKID_DESC"
    rarity very_rare
    kind face
    frame 198
	set [Meat, HumanFlesh]

	spd 4

	passives {
		InjuryImmunity 1
		ChanceToRevive 100
		ReplaceBasicMove BasicJump
	}
}
```

---

### `LilTumor`
**Name:** Lil' Tumor  
**Description:** At the end of each battle, gain -1 to three random stats, then gain a mutation.  
**Source:** `face_items.gon`  

```
LilTumor {
    name "ARMOR_LILTUMOR_NAME"
    desc "ARMOR_LILTUMOR_DESC"
    rarity rare
    kind face
    frame 199
	set Mother

    passives {
        StatusOnBattleEnd {
            even_if_dead true
            
            RandomPermanentStat -3
            RandomMutation 1
        }
    }
}
```

---

### `ConjoinedAmeoba`
**Name:** Conjoined Ameoba  
**Description:** Brace 2. +2 Health Regen. Units that contact you are knocked back 2 tiles.
20% chance to spawn a Charmed Ameoba at the end of the turn.  
**Source:** `face_items.gon`  

```
ConjoinedAmeoba {
    name "ARMOR_CONJOINEDAMEOBA_NAME"
    desc "ARMOR_CONJOINEDAMEOBA_DESC"
    rarity rare
    kind face
    frame 200
	set Amoeba

	int -2

    passives {
        Brace 2
		HealthRegenUp 2
		MeleeRevengeDamage {
            knockback 2
        }
		SpawnEachTurn {
			chance .2
			object CharmedAmoeba
		}
    }
}
```

---

### `MinersBeard`
**Name:** Miner's Beard  
**Description:** When you take damage, spawn scrap.
When you end turn, spawn a coin on a random tile.  
**Source:** `face_items.gon`  

```
MinersBeard {
    name "ARMOR_MINERSBEARD_NAME"
    desc "ARMOR_MINERSBEARD_DESC"
    rarity rare
    kind face
    frame 201
	set [Miner, Man]

	passives {
        SpawnThingOnDamage {
			object Scrap
		}
		StatusEachTurnEnd {
			SpawnCoinAnywhere 1
		}
    }
}
```

---

### `EtherealEyes`
**Name:** Ethereal Eyes  
**Description:** +15% Dodge Chance.
Gain +5% Dodge Chance each time you take damage.  
**Source:** `face_items.gon`  

```
EtherealEyes {
    name "ARMOR_ETHEREALEYES_NAME"
    desc "ARMOR_ETHEREALEYES_DESC"
    rarity rare
    kind face
    frame 202

	passives {
		DodgeChance_Status 15
		StatusOnTookDamage {
            DodgeChance_Status 5
        }
	}
}
```

---

### `DoodieMask`
**Name:** Doodie Mask  
**Description:** Spawn a Charmed Fly at the end of your turn.  
**Source:** `face_items.gon`  

```
DoodieMask {
    name "ARMOR_DOODIEMASK_NAME"
    desc "ARMOR_DOODIEMASK_DESC"
    rarity rare
    kind face
    frame 203
	set Fecal

	cha -2
	
	passives {
		SpawnEachTurn {
			object CharmedFly
        }
	}
}
```

---

### `TinasFriend`
**Name:** Tina's Best Friend  
**Description:** Spawn a large Charmed Fly at the start of each battle.  
**Source:** `face_items.gon`  

```
TinasFriend {
    name "ARMOR_TINASFRIEND_NAME"
    desc "ARMOR_TINASFRIEND_DESC"
    rarity very_rare
    kind face
    frame 161
	set Fly

    passives {
        SpawnOnBattleStart {
            object CharmedTinaFly
            number 1
        }
    }
}
```

---

### `StevensFartFace`
**Name:** Steven's Fart Face  
**Description:** At the end of your turn, inflict Poison 1 on all units. Repeat for each turn you've taken this battle.  
**Source:** `face_items.gon`  

```
StevensFartFace {
    name "ARMOR_STEVENSFARTFACE_NAME"
    desc "ARMOR_STEVENSFARTFACE_DESC"
    rarity very_rare
    kind face
    frame 156
	set Steven

	passives {
		StatusEachTurnEndForEachTurn {
			ForceUseAbility face_FartFace
		}
	}
}
```

---

### `StevensMustache`
**Name:** Steven's Mustache  
**Description:** ARMOR_STEVENSMUSTACHE_DESC  
**Source:** `face_items.gon`  

```
StevensMustache {//todo become ? gender
    name "ARMOR_STEVENSMUSTACHE_NAME"
    desc "ARMOR_STEVENSMUSTACHE_DESC"
    rarity very_rare
    kind face
    frame 157
	set Steven

	cha 5
	lck -2

}
```

---

### `StevenMask1`
**Name:** Steven  
**Description:** Your musical abilities are always double cast.  
**Source:** `face_items.gon`  

```
StevenMask1 {
    name "ARMOR_STEVENMASK1_NAME"
    desc "ARMOR_STEVENMASK1_DESC"
    rarity very_rare
    kind face
    frame 158
	set Steven

	passives {
        DoubleCastTaggedSpells musical
	}
}
```

---

### `StevenMask2`
**Name:** Steven  
**Description:** While you're downed, spawn a random charmed enemy familiar at the end of each round.  
**Source:** `face_items.gon`  

```
StevenMask2 {
    name "ARMOR_STEVENMASK2_NAME"
    desc "ARMOR_STEVENMASK2_DESC"
    rarity very_rare
    kind face
    frame 159
	set Steven

	passives {
        PassiveWhenDead {
            AutocastEachRound {
                ability face_StevenMask2
                even_if_stunned true
            }
        }
	}
}
```

---

### `Intruder`
**Name:** Intruder  
**Description:** Is it your baby?  
**Source:** `face_items.gon`  

```
Intruder {
    name "ARMOR_INVADER_NAME"
    desc "ARMOR_INVADER_DESC"
    rarity very_rare
    kind face
    frame 206
	parasite true

	passives {
		SpawnThingOnDeath TheIntruder
	}
}
```

---

### `ChildOfTheGlowingOne2`
**Name:** Child of the Glowing One  
**Description:** Gain +1 Damage and heal 1 HP every time you use your basic attack.  
**Source:** `face_items.gon`  

```
ChildOfTheGlowingOne2 {
    name "ARMOR_CHILDOFTHEGLOWINGONE2_NAME"
    desc "ARMOR_CHILDOFTHEGLOWINGONE2_DESC"
    rarity very_rare
    kind face
    frame 205
	//allsets
	
	passives {
		StatusOnUseBasicAttack {
			DamageUp 1
			HealthGain 1
		}
	}
}
```

---

## File: `head_items.gon`

### `Antenna`
**Name:** Antenna  
**Description:** Units that contact or attack you get hit with a lightning bolt that has a 10% chance to Stun.  
**Source:** `head_items.gon`  

```
Antenna {
    name "ARMOR_ANTENNA_NAME"
    desc "ARMOR_ANTENNA_DESC"
    rarity uncommon
    kind head
    frame 1
    
    passives {
        RevengeDamage {
            damage 1

            effects {
                Stun [1, .1]
                VisualFX Bolt
            }
            
            elements [
                Electric
            ]
        }
        Metal 1
    }
}
```

---

### `Horns`
**Name:** Horns  
**Description:** +1 Thorns.  
**Source:** `head_items.gon`  

```
Horns {
    name "ARMOR_HORNS_NAME"
    desc "ARMOR_HORNS_DESC"
    rarity uncommon
    kind head
    frame 2
    
    str 1
    passives {
        Thorns 1
    }
}
```

---

### `HappyHelmet`
**Name:** Happy Helmet  
**Description:** Fragile. Gain Psychosis when this breaks.  
**Source:** `head_items.gon`  

```
HappyHelmet {
    name "ARMOR_HAPPYHELMET_NAME"
    desc "ARMOR_HAPPYHELMET_DESC"
    rarity rare
    kind head
    frame 55
	set [Bionic, Cyborg]
    
    shield 10
    passives {
        SetDefaultFacePassive euphoric
        Fragile 1
        StatusOnBreak {
            GainDisorder Psychosis
        }
    }
}
```

---

### `HeadSpring`
**Name:** Head Spring  
**Description:** Units that contact you are knocked back 10 tiles.  
**Source:** `head_items.gon`  

```
HeadSpring {
    name "ARMOR_HEADSPRING_NAME"
    desc "ARMOR_HEADSPRING_DESC"
    rarity common
    kind head
    frame 54
	set Scrap
    
    passives {
        MeleeRevengeDamage {
            knockback 10
        }
        Metal 1
    }
}
```

---

### `Wig`
**Name:** Wig  
**Description:** ARMOR_WIG_DESC  
**Source:** `head_items.gon`  

```
Wig {
    name "ARMOR_WIG_NAME"
    desc "ARMOR_WIG_DESC"
    rarity common
    kind head
    frame 56
	set Used
    
    cha 2
}
```

---

### `HeadCheese`
**Name:** Head Cheese  
**Description:** +2 Health Regen.  
**Source:** `head_items.gon`  

```
HeadCheese {
    name "ARMOR_HEADCHEESE_NAME"
    desc "ARMOR_HEADCHEESE_DESC"
    rarity uncommon
    kind head
    frame 53
    
    passives {
        HealthRegenUp 2
    }
}
```

---

### `DunceCap`
**Name:** Dunce Cap  
**Description:** Your spells cost -1 mana.  
**Source:** `head_items.gon`  

```
DunceCap {
    name "ARMOR_DUNCECAP_NAME"
    desc "ARMOR_DUNCECAP_DESC"
    rarity rare
    kind head
    frame 91
	set Paper

    int -2

    passives {
        ManaCostReduction 1
    }
}
```

---

### `PoopHat`
**Name:** Crown of Feculence  
**Description:** Poops you spawn are alive!  
**Source:** `head_items.gon`  

```
PoopHat {
    name "ARMOR_POOPHAT_NAME"
    desc "ARMOR_POOPHAT_DESC"
    rarity rare
    kind head
    frame 96
	set Fecal

    passives {
        ReplaceSpawnedObjects [Poop RandomLivingPoop]
        ReplaceSpawnedObjects [FlamingPoop RandomLivingPoop]
    }
}
```

---

### `Magneto`
**Name:** Magneto  
**Description:** When you end your movement, pull all adjacent pickups towards you.
When you gain coins, gain that much [img:shield].  
**Source:** `head_items.gon`  

```
Magneto {
    name "ARMOR_MAGNETO_NAME"
    desc "ARMOR_MAGNETO_DESC"
    rarity rare
    kind head
    frame 29

    shield 1

    passives {
        Metal 1
        StatusOnEndMove {
            ImmediateUseAbility head_MagnetoAttract
        }
        StatusOnGainCoins {
            Shield X
        }
    }
}
```

---

### `BlackCandle`
**Name:** Black Candle  
**Description:** You can remove cursed items equipped on you, except this one.  
**Source:** `head_items.gon`  

```
BlackCandle { //TODO: make sure this can't be replaced by a parasite or cursed item
    name "ARMOR_BLACKCANDLE_NAME"
    desc "ARMOR_BLACKCANDLE_DESC"
    rarity rare
    kind head
    frame 58
    cursed true
    force_sticky true
	set Demonic
    
    shield 1

    passives {
        CanRemoveCursedItems 1
        ExcludeFromEvents Tragedy
    }
}
```

---

### `CamoHat`
**Name:** Survivalist Hat  
**Description:** +25% chance to ambush when entering battle.
10% chance to gain Stealth 1 at the end of each turn.  
**Source:** `head_items.gon`  

```
CamoHat {
    name "ARMOR_CAMOHAT_NAME"
    desc "ARMOR_CAMOHAT_DESC"
    rarity rare
    kind head
    frame 59
	set Survivalist 

    passives {
        ChanceToAmbush 25%
        StatusEachTurnEnd {
            Stealth [1 .1]
        }
    }
}
```

---

### `JesterCap`
**Name:** Jester Cap  
**Description:** You can reroll your options twice when you level up.
Abilities from all classes are offered after rerolling.  
**Source:** `head_items.gon`  

```
JesterCap {
    name "ARMOR_JESTERCAP_NAME"
    desc "ARMOR_JESTERCAP_DESC"
    rarity rare
    kind head
    frame 60
	set Jester

    cha 1

    passives {
        AddLevelUpRerolls 2
        JesterLevelUpRerolls 1
    }
}
```

---

### `Halo`
**Name:** Halo  
**Description:** +33% chance to gain +1 [img:divineshield] when you take damage.  
**Source:** `head_items.gon`  

```
Halo {
    name "ARMOR_HALO_NAME"
    desc "ARMOR_HALO_DESC"
    rarity rare
    kind head
    frame 61
	set Cleric

    divine_shield 1

    passives {
        StatusOnTakeHealthOrShieldDamage {
            DivineShield [1 .33]
        }
    }
}
```

---

### `PropellerCap`
**Name:** Propeller Cap  
**Description:** Flying.  
**Source:** `head_items.gon`  

```
PropellerCap {
    name "ARMOR_PROPELLERCAP_NAME"
    desc "ARMOR_PROPELLERCAP_DESC"
    rarity uncommon
    kind head
    frame 62

    shield 2

    passives {
        Flying 1
    }
}
```

---

### `BrainInAJar`
**Name:** Brain In A Jar  
**Description:** The first spell you cast each turn is free.  
**Source:** `head_items.gon`  

```
BrainInAJar {
    name "ITEM_BRAININAJAR_NAME"
    desc "ITEM_BRAININAJAR_DESC"
    rarity rare
    kind head
    cursed true
    frame 168
	set Guts
    
    int -5
    
    passives {
        StatusEachTurnBegin {
            Temporary {
                status FreeSpell
                stacks 1
                expires_on_end_turn true
            }
        }
    }
}
```

---

### `MangyWig`
**Name:** Mangy Wig  
**Description:** Spawn a Spiderling for every 4 [img:lck] you have at the start of each battle.  
**Source:** `head_items.gon`  

```
MangyWig {
    name "ARMOR_MANGYWIG_NAME"
    desc "ARMOR_MANGYWIG_DESC"
    rarity uncommon
    kind head
    frame 133
	set Used

    passives {
        StatusOnBattleStart {
            ObjectOnHitCharacter {
                stacks "floor(lck/4)"
                object CharmedTinySpider
            }
        }
    }
}
```

---

### `RisingSunBandana`
**Name:** Nisshōki Bandana  
**Description:** While at 5 or less health, you have +3 Damage and can move an extra time each turn.  
**Source:** `head_items.gon`  

```
RisingSunBandana {
    name "ARMOR_RISINGSUNBANDANA_NAME"
    desc "ARMOR_RISINGSUNBANDANA_DESC"
    rarity rare
    kind head
    frame 135

    passives {
        PassiveAtHealthThreshold {
            threshold 5
            mode less_or_equal
            
            passives {
                ExtraMovePoints 1
                DamageUp 3
            }
        }
    }
}
```

---

### `JewelOfDrog`
**Name:** Jewel of Drog  
**Description:** The first time you reach full mana each battle, gain +1 Magic Damage and reduce the cost of your spells by 1.  
**Source:** `head_items.gon`  

**Localization Strings:**
- `COMBAT_POPUP_BRAINSTORM`: "Brainstorm!"

```
JewelOfDrog {
    name "ARMOR_JEWELOFDROG_NAME"
    desc "ARMOR_JEWELOFDROG_DESC"
    rarity rare
    kind head
    frame 137
	set Gemstone

    passives {
        StatusOnFullMana {
            Conditional_OncePerBattle {
                key JewelOfDrog
                ReduceManaCost 1
                SpellDamageUp 1
                ShowText "COMBAT_POPUP_BRAINSTORM"
            }
        }
    }
}
```

---

### `LeakyBrain`
**Name:** Leaky Brain  
**Description:** When you spend mana, adjacent allies gain that amount of mana.  
**Source:** `head_items.gon`  

```
LeakyBrain {
    name "ARMOR_LEAKYBRAIN_NAME"
    desc "ARMOR_LEAKYBRAIN_DESC"
    rarity rare
    kind head
    frame 143
	set Guts

    int -2

    passives {
        ScaledStatusAlliesOnSpendMana {
            Conditional_Adjacent {
                Conditional_Ally {
                    ManaGain 1
                }
            }
        }
    }
}
```

---

### `FryingPan`
**Name:** Frying Pan  
**Description:** Block and counter Backstabs.  
**Source:** `head_items.gon`  

```
FryingPan {
    name "ARMOR_FRYINGPAN_NAME"
    desc "ARMOR_FRYINGPAN_DESC"
    rarity uncommon
    kind head
    frame 151
	set Lead

    passives {
        Metal 1
        ChanceToBlockAndCounter {
            chance 100%
            backstab_only true
        }
    }
}
```

---

### `CrownOfHorns`
**Name:** Crown of Horns  
**Description:** +4 Thorns. When you take damage while you have Thorns, lose 1 Thorns, then shoot needles that deal 2 damage in eight directions.  
**Source:** `head_items.gon`  

```
CrownOfHorns {
    name "ARMOR_CROWNOFHORNS_NAME"
    desc "ARMOR_CROWNOFHORNS_DESC"
    rarity rare
    kind head
    frame 155
	set [Demonic, Barbed]

    passives {
        Thorns 4
        StatusOnTookDamage {
            Conditional_HasStatus {
                status Thorns
                ImmediateUseAbility_Instant head_CrownOfHorns
                RemoveStatusStacks {
                    status Thorns
                    stacks 1
                }
            }
        }
    }
}
```

---

### `TheRelic`
**Name:** The Relic  
**Description:** When you lose [img:divineshield], emit a Sparkle for every point of damage blocked.  
**Source:** `head_items.gon`  

```
TheRelic {
    name "ARMOR_THERELIC_NAME"
    desc "ARMOR_THERELIC_DESC"
    rarity uncommon
    kind head
    frame 158
	set Cleric

    divine_shield 1

    passives {
        ScaledStatusOnHolyShieldBlock {
            RandomMagicMissile 1
        }
    }
}
```

---

### `FocusBand`
**Name:** Focus Band  
**Description:** Your crits knock units back 10 tiles with Chain Knockback.  
**Source:** `head_items.gon`  

```
FocusBand {
    name "ARMOR_FOCUSBAND_NAME"
    desc "ARMOR_FOCUSBAND_DESC"
    rarity uncommon
    kind head
    frame 136

    passives {
        AddStatusToAllDamage {
            KnockbackIfCrit {
                knockback 10
                override_chain_knockback 10
            }
        }
    }
}
```

---

### `MedicHat`
**Name:** Medic Hat  
**Description:** -1 Damage. Your basic attack heals allies.  
**Source:** `head_items.gon`  

```
MedicHat {
    name "ARMOR_MEDICHAT_NAME"
    desc "ARMOR_MEDICHAT_DESC"
    rarity uncommon
    kind head
    frame 140
	set [Nurse, Medical]

    passives {
        DamageUp -1
        AddStatusToBasicAttack {
            DamageOrHealConditionally 1
        }
    }
}
```

---

### `KingsCrown`
**Name:** King's Crown  
**Description:** Become the Alpha at the start of each battle.
The Alpha has All Stats Up.
Lose Alpha status when you take damage.  
**Source:** `head_items.gon`  

```
KingsCrown {
    name "ARMOR_KINGSCROWN_NAME"
    desc "ARMOR_KINGSCROWN_DESC"
    rarity uncommon
    kind head
    frame 141

    passives {
        Metal 1
        AlphaCat 1
        AlphaAllStatsUp 1
        StatusOnTookDamage {
            RemoveStatus AlphaCat
        }
    }
}
```

---

### `EmoWig`
**Name:** Emo Wig  
**Description:** Adjacent units get All Stats Down 2.
When you take damage, all units within 2 tiles heal 1 HP and gain a temporary +1 Damage.  
**Source:** `head_items.gon`  

```
EmoWig {
    name "ARMOR_EMOWIG_NAME"
    desc "ARMOR_EMOWIG_DESC"
    rarity rare
    kind head
    frame 142
	set [Necromancer, Used]

    str -1
    dex -1
    con -1
    int -1
    spd -1
    cha -1
    lck -1

    passives {
        DepressionAura 2
        AbilityReaction head_EmoSong
    }
}
```

---

### `ToxicCanister`
**Name:** Toxic Canister  
**Description:** Inflict Poison 1 on all units at the start of the battle.
Your basic attack inflicts Poison 1.
Inflict Poison 1 on units that contact you.  
**Source:** `head_items.gon`  

```
ToxicCanister {
    name "ARMOR_TOXICCANISTER_NAME"
    desc "ARMOR_TOXICCANISTER_DESC"
    rarity rare
    kind head
    frame 147
	set Radioactive

    passives {
        Metal 1
        StatusAllCharactersOnSpawn {
            Poison 1
        }
        AddStatusToBasicAttack {
            Poison 1
        }
        MeleeRevengeDamage {
            effects {
                Poison 1
            }
        }
        StatusOnDie {
            Conditional_RandomChance {
                odds 20%
                ApplyPassives {
                    StatusOnBattleEnd {
                        even_if_dead true
                        RandomMutation 1
                    }
                }
            }
        }
    }
}
```

---

### `BrokenMirrorHat`
**Name:** Broken Mirror  
**Description:** +3 Bleed Thorns. Your basic attack inflicts +1 Bleed and spawns glass.  
**Source:** `head_items.gon`  

```
BrokenMirrorHat {
    name "ARMOR_BROKENMIRROR_NAME"
    desc "ARMOR_BROKENMIRROR_DESC"
    rarity rare
    kind head
    frame 134
	set Used

    shield 4
    lck -7

    passives {
        BleedThorns 3
        AddStatusToBasicAttack {
            ChangeTile GlassTile
            Bleed 1
        }
    }
}
```

---

### `TopHat`
**Name:** Top Hat  
**Description:** Start with a bomb if you have no weapon equipped.
Your explosions have +1 area.  
**Source:** `head_items.gon`  

```
TopHat {
    name "ARMOR_TOPHAT_NAME"
    desc "ARMOR_TOPHAT_DESC"
    rarity uncommon
    kind head
    frame 138
	set Cool

    passives {
        StatusOnBattleStart {
            Craft {
                pool bombs //should expand to bombs_0, bombs_1, bombs_2, bombs_3
                slot weapon
                works_with_tech true
            }
        }
        IncreaseExplosionSize 1
    }
}
```

---

### `Helmet`
**Name:** Helmet  
**Description:** ARMOR_HELMET_DESC  
**Source:** `head_items.gon`  

```
Helmet {
    name "ARMOR_HELMET_NAME"
    desc "ARMOR_HELMET_DESC"
    rarity common
    kind head
    frame 139

    shield 4

    passives {
        Metal 1
        PreventSpecificInjury int
        // TODO: prevent Head Trauma disorder?
    }
}
```

---

### `ConfusingHat`
**Name:** Confusing Hat  
**Description:** Apply Confusion 2 to yourself and all enemies at the start of each battle.  
**Source:** `head_items.gon`  

```
ConfusingHat {
    name "ARMOR_CONFUSINGHAT_NAME"
    desc "ARMOR_CONFUSINGHAT_DESC"
    rarity rare
    kind head
    frame 144

    passives {
        Confusion 2
        StatusRandomEnemiesOnBattleStart {
            count 99
            Confusion 2
        }
    }
}
```

---

### `NightmareHat`
**Name:** Nightmare Hat  
**Description:** After you kill 3 units, you can attack an extra time each turn.  
**Source:** `head_items.gon`  

```
NightmareHat {
    name "ARMOR_NIGHTMAREHAT_NAME"
    desc "ARMOR_NIGHTMAREHAT_DESC"
    rarity uncommon
    kind head
    frame 145
	set Leather

    passives {
        PassiveAfterXKills {
            stacks 3

            passives {
                ExtraBasicAttacks 1
            }
        }
    }
}
```

---

### `CrownOfPestilence`
**Name:** Crown of Pestilence  
**Description:** Your basic attack becomes Pestilence.  
**Source:** `head_items.gon`  

```
CrownOfPestilence {
    name "ARMOR_CROWNOFPESTILENCE_NAME"
    desc "ARMOR_CROWNOFPESTILENCE_DESC"
    rarity rare
    kind head
    frame 150
	set Necromancer

    passives {
        ReplaceBasicAttack head_Pestilence
    }
}
```

---

### `RainHat`
**Name:** Rain Hat  
**Description:** You have All Stats Up while wet.  
**Source:** `head_items.gon`  

```
RainHat {
    name "ARMOR_RAINHAT_NAME"
    desc "ARMOR_RAINHAT_DESC"
    rarity uncommon
    kind head
    frame 153

    passives {
        PassiveWhenAffectedByElement {
            element water
            passives {
                AllStatsUp 1
            }
        }
    }
}
```

---

### `SplinteredCrown`
**Name:** Splintered Crown  
**Description:** Gain +1 Thorns when you take damage.  
**Source:** `head_items.gon`  

```
SplinteredCrown {
    name "ARMOR_SPLINTEREDCROWN_NAME"
    desc "ARMOR_SPLINTEREDCROWN_DESC"
    rarity uncommon
    kind head
    frame 157
    set Wood

    passives {
        StatusOnTookDamage {
            Thorns 1
        }
    }
}
```

---

### `MedievalHelmet`
**Name:** Medieval Helmet  
**Description:** +2 Brace.  
**Source:** `head_items.gon`  

```
MedievalHelmet {
    name "ARMOR_MEDIEVALHELMET_NAME"
    desc "ARMOR_MEDIEVALHELMET_DESC"
    rarity uncommon
    kind head
    frame 159
	set Fighter

    passives {
        Metal 1
        Brace 2
    }
}
```

---

### `ConjoinedEye`
**Name:** Conjoined Eye  
**Description:** +10% Dodge Chance.  
**Source:** `head_items.gon`  

```
ConjoinedEye {
    name "ARMOR_CONJOINEDEYE_NAME"
    desc "ARMOR_CONJOINEDEYE_DESC"
    rarity common
    kind head
    frame 191
	set Hybrid

    passives {
        ArmorDodgeChance 10%
    }
}
```

---

### `StoneHelmet`
**Name:** Stone Helmet  
**Description:** +1 Brace.  
**Source:** `head_items.gon`  

```
StoneHelmet {
    name "ARMOR_STONEHELMET_NAME"
    desc "ARMOR_STONEHELMET_DESC"
    rarity common
    kind head
    frame 190
	set Rock

    passives {
        Brace 1
    }
}
```

---

### `OakHelmet`
**Name:** Oak Helmet  
**Description:** Flammable.  
**Source:** `head_items.gon`  

```
OakHelmet {
    name "ARMOR_OAKHELMET_NAME"
    desc "ARMOR_OAKHELMET_DESC"
    rarity common
    kind head
    frame 189
	set Wood

	shield 3

    passives {
        Flammable 1
    }
}
```

---

### `RustingHelmet`
**Name:** Rusting Helmet  
**Description:** Gain +1 [img:shield] at the end of each turn.  
**Source:** `head_items.gon`  

```
RustingHelmet {
    name "ARMOR_RUSTINGHELMET_NAME"
    desc "ARMOR_RUSTINGHELMET_DESC"
    rarity common
    kind head
    frame 183
	set Used

	shield 1
	
    passives {
        Metal 1
        StatusEachTurnEnd {
			Shield 1
		}
    }
}
```

---

### `TrainingBand`
**Name:** Training Band  
**Description:** +20% Crit Chance.  
**Source:** `head_items.gon`  

```
TrainingBand {
    name "ARMOR_TRAININGBAND_NAME"
    desc "ARMOR_TRAININGBAND_DESC"
    rarity common
    kind head
    frame 182

    passives {
		CritChanceUp 20
    }
}
```

---

### `SkullClamp`
**Name:** Skull Clamp  
**Description:** Brace 2 
+25% chance to inflict Stun on units that contact you.  
**Source:** `head_items.gon`  

```
SkullClamp {
    name "ARMOR_SKULLCLAMP_NAME"
    desc "ARMOR_SKULLCLAMP_DESC"
    rarity rare
    kind head
    frame 70

    int -6
    shield 10

    passives {
        Metal 1
        Brace 2
        MeleeRevengeDamage {
            effects {
                Stun [1, .25]
            }
        }
    }
}
```

---

### `BrainChip`
**Name:** Brain Chip  
**Description:** Become AI controlled.  
**Source:** `head_items.gon`  

```
BrainChip {
    name "ARMOR_BRAINCHIP_NAME"
    desc "ARMOR_BRAINCHIP_DESC"
    rarity uncommon
    kind head
    frame 69
	set Chip

    str 1
    dex 1
    con 1
    int 1
    cha 1
    spd 1
    lck 1

    passives {
        Metal 1
        Uncontrollable 1
    }
}
```

---

### `SpareParts`
**Name:** Spare Parts  
**Description:** When you move, spawn a scrap pickup where you moved from.  
**Source:** `head_items.gon`  

```
SpareParts {
    name "ARMOR_SPAREPARTS_NAME"
    desc "ARMOR_SPAREPARTS_DESC"
    rarity uncommon
    kind head
    frame 181
	set [Tinkerer, Scrap]

    passives {
        Metal 1
        LeaveBehindOnceEachMove Scrap
    }
}
```

---

### `SnakeskinHat`
**Name:** Snakeskin Hat  
**Description:** Spawn a Charmed Rattlesnek at the start of each battle.  
**Source:** `head_items.gon`  

```
SnakeskinHat {
    name "ARMOR_SNAKESKINHAT_NAME"
    desc "ARMOR_SNAKESKINHAT_DESC"
    rarity uncommon
    kind head
    frame 185
	set Leather

    passives {
        SpawnOnBattleStart {
            object CharmedRattleSnake
        }
    }
}
```

---

### `DeathShroud`
**Name:** Death Shroud  
**Description:** When you're downed, permanently gain +1 to a random stat.  
**Source:** `head_items.gon`  

```
DeathShroud {
    name "ARMOR_DEATHSHROUD_NAME"
    desc "ARMOR_DEATHSHROUD_DESC"
    rarity rare
    kind head
    frame 187
	set Rag

    passives {
        StatusOnDie {
            RandomStatusFromPool {
                PermanentStrength 1
                PermanentDexterity 1
                PermanentConstitution 1
                PermanentIntelligence 1
                PermanentCharisma 1
                PermanentSpeed 1
                PermanentLuck 1
            }
        }
    }
}
```

---

### `BlessedHalo`
**Name:** Blessed Halo  
**Description:** 50% chance to gain +1 [img:divineshield] when you take damage.  
**Source:** `head_items.gon`  

```
BlessedHalo {
    name "ARMOR_BLESSEDHALO_NAME"
    desc "ARMOR_BLESSEDHALO_DESC"
    rarity very_rare
    kind head
    frame 206

    divine_shield 3

    passives {
        StatusOnTakeHealthOrShieldDamage {
            DivineShield [1 .5]
        }
    }
}
```

---

### `CrownOfThorns`
**Name:** Crown Of Thorns  
**Description:** +1 Thorns. Gain +1 Thorns whenever you take damage.  
**Source:** `head_items.gon`  

```
CrownOfThorns {
    name "ARMOR_CROWNOFTHORNS_NAME"
    desc "ARMOR_CROWNOFTHORNS_DESC"
    rarity very_rare
    kind head
    frame 65
	set Cleric
	divine_shield 2


	passives {
		Thorns 1

		StatusOnTookDamage {
			Thorns 1
		}
    }
}
```

---

### `RottenGuts`
**Name:** Rotten Guts  
**Description:** +2 Health Regen. Spawn a Charmed Maggot or Fly when you end your turn.  
**Source:** `head_items.gon`  

```
RottenGuts {
	name "ARMOR_ROTTENGUTS_NAME"
	desc "ARMOR_ROTTENGUTS_DESC"
	rarity very_rare
	kind head
	frame 207
	set [Guts, Rotten]

	con 2
	cha -1

	passives {
		HealthRegenUp 2
		SpawnEachTurn {
			chance 100%
			object [CharmedFly CharmedMaggot]
		}
	}
}
```

---

### `PaperRags`
**Name:** Paper Rags  
**Description:** +20% Dodge Chance.
+1 Bleed Thorns.
Your basic attack inflicts Bleed.  
**Source:** `head_items.gon`  

```
PaperRags {
	name "ARMOR_PAPERRAGS_NAME"
	desc "ARMOR_PAPERRAGS_DESC"
	rarity very_rare
	kind head
	frame 208
	set [Paper, Rag]

	passives {
		ArmorDodgeChance 20%
		BleedThorns 1
		AddStatusToBasicAttack {
			Bleed 1
		}
	}
}
```

---

### `TieDyeBandana`
**Name:** Tie Dye Bandana  
**Description:** Spawn a Catnip pickup when you take damage.  
**Source:** `head_items.gon`  

```
TieDyeBandana {
    name "ARMOR_TIEDYEBANDANA_NAME"
    desc "ARMOR_TIEDYEBANDANA_DESC"
    rarity rare
    kind head
    frame 209
	set Hippie

	passives {
		SpawnThingOnDamage {
			object Catnip
			good false //good relative to the thing attacking, for luck calculations
		}
	}
}
```

---

### `BungasCrown`
**Name:** Bunga's Crown  
**Description:** Your weapons always crit.
Equip a Bone Club weapon when you kill a unit.  
**Source:** `head_items.gon`  

```
BungasCrown {
    name "ARMOR_BUNGASCROWN_NAME"
    desc "ARMOR_BUNGASCROWN_DESC"
    rarity very_rare
    kind head
    frame 217
	
	str 2
	spd -4
	con 1

	passives {
		BoostWeaponDamage {
            damage 0
            crit_chance 1
        }
		StatusOnKill {
			EquipPermanentItem BoneClub
		}
	}
}
```

---

### `Asteroid`
**Name:** Asteroid  
**Description:** 20% chance to call down a Meteor on a random enemy when you take damage.  
**Source:** `head_items.gon`  

```
Asteroid {
    name "ARMOR_ASTEROID_NAME"
    desc "ARMOR_ASTEROID_DESC"
    rarity very_rare
    kind head
    frame 216
	shield 4
	set Planet

	passives {
		StatusOnTakeHealthOrShieldDamage{
			Conditional_GoodRoll {
                odds 20%
                ForceUseAbility tk_Asteroid
			}
        }
	}
}
```

---

### `AlienStalk`
**Name:** Alien Stalk  
**Description:** Cast a random spell each time you take damage.  
**Source:** `head_items.gon`  

```
AlienStalk {
    name "ARMOR_ALIENSTALK_NAME"
    desc "ARMOR_ALIENSTALK_DESC"
    rarity very_rare
    kind head
    frame 215
	set [Space, Amoeba]

	passives {
		StatusOnTakeHealthOrShieldDamage {
			Metronome 1
		}
	}
}
```

---

### `FriendlyAmoeba`
**Name:** Friendly Amoeba  
**Description:** Brace 1, +2 Health Regen, Shield 3. Units that contact you get knocked back 1.  
**Source:** `head_items.gon`  

```
FriendlyAmoeba {
    name "ARMOR_FRIENDLYAMOEBA_NAME"
    desc "ARMOR_FRIENDLYAMOEBA_DESC"
    kind head
	rarity rare
    frame 214
    set Amoeba
	
	int -1
	shield 3

    passives {
        Brace 1
		HealthRegenUp 2
		MeleeRevengeDamage {
            knockback 1
        }
    }
}
```

---

### `SpiderBaby`
**Name:** Spider Baby  
**Description:** Spawn a Spiderling when you take damage.  
**Source:** `head_items.gon`  

```
SpiderBaby {
    name "ARMOR_SPIDERBABY_NAME"
    desc "ARMOR_SPIDERBABY_DESC"
    rarity very_rare
    kind head
    frame 213
	set Necromancer

	passives {
        SpawnThingOnDamage {
            object CharmedTinySpider
        }
	}
}
```

---

### `BorisBrain`
**Name:** Boris' Brain  
**Description:** Trample. When you take damage, move 1 tile towards what damaged you.  
**Source:** `head_items.gon`  

```
BorisBrain {
    name "ARMOR_BORISBRAIN_NAME"
    desc "ARMOR_BORISBRAIN_DESC"
    rarity very_rare
    kind head
    frame 212
	set Guts

	passives {
		Trample 3
		MoveTowardsDamageSource MoveOne
	}
}
```

---

### `JohnnysUndies`
**Name:** Johnny's Undies  
**Description:** Spawn a Charmed Cultist at the start of each battle.  
**Source:** `head_items.gon`  

```
JohnnysUndies {
    name "ARMOR_JOHNNYSUNDIES_NAME"
    desc "ARMOR_JOHNNYSUNDIES_DESC"
    rarity very_rare
    kind head
    frame 211
	set Used

	passives {
		SpawnOnBattleStart CharmedCultist
	}
}
```

---

### `QueensCrown`
**Name:** Queen's Crown  
**Description:** Your basic attack has Knockback and Chain Knockback.  
**Source:** `head_items.gon`  

```
QueensCrown {
    name "ARMOR_QUEENSCROWN_NAME"
    desc "ARMOR_QUEENSCROWN_DESC"
    rarity very_rare
    kind head
    frame 210
	shield 4

	passives {
        Metal 1
		AddStatusToBasicAttack {
			Knockback 1
            OverrideChainKnockback 1
		}
	}
}
```

---

### `DustDevilsHorn`
**Name:** Dust Devil's Horn  
**Description:** +1 Thorns. After you use your basic attack, do a dash attack that leaves a tornado behind.  
**Source:** `head_items.gon`  

```
DustDevilsHorn {
    name "ARMOR_DUSTDEVILSHORN_NAME"
    desc "ARMOR_DUSTDEVILSHORN_DESC"
    rarity very_rare
    kind head
    frame 219

	shield 1

	passives {
		Thorns 1
		AddSelfStatusToBasicAttack {
			ForceUseAbility DustDash
        }
	}
}
```

---

### `ChildOfTheGlowingOne`
**Name:** Child of the Glowing One  
**Description:** Gain +1 [img:divineshield] every time you end your movement.  
**Source:** `head_items.gon`  

```
ChildOfTheGlowingOne {
    name "ARMOR_CHILDOFTHEGLOWINGONE_NAME"
    desc "ARMOR_CHILDOFTHEGLOWINGONE_DESC"
    rarity very_rare
    kind head
    frame 220
	//allsets
	
	passives {
		StatusOnEndMove {
			DivineShield 1
		}
	}
}
```

---

### `SabertoothTigerPelt`
**Name:** Pale Sabertooth Pelt  
**Description:** When you kill a unit, all nearby cats gain +1 Damage.  
**Source:** `head_items.gon`  

```
SabertoothTigerPelt {
    name "ARMOR_SABERTOOTHTIGERPELT_NAME"
    desc "ARMOR_SABERTOOTHTIGERPELT_DESC"
    rarity rare
    kind head
    frame 221
	set Wooly

	cha 2

	passives {
		StatusOnKillEnemy {
			ForceUseAbility head_CatChestPound
		}
	}
}
```

---

### `CowSkull`
**Name:** Cow Skull  
**Description:** +2 Thorns. Your basic attack is Push Attack.  
**Source:** `head_items.gon`  

```
CowSkull {
    name "ARMOR_COWSKULL_NAME"
    desc "ARMOR_COWSKULL_DESC"
    rarity very_rare
    kind head
    frame 222
	set Bone
	
	attack BasicTankMelee
    shield 3
	str 2

	passives {
		Thorns 2
        OverrideBasicAttack BasicTankMelee
	}
}
```

---

### `TrashCan`
**Name:** TrashCan  
**Description:** Brace 4. Blind.  
**Source:** `head_items.gon`  

```
TrashCan {
    name "ARMOR_TRASHCAN_NAME"
    desc "ARMOR_TRASHCAN_DESC"
    rarity very_rare
    kind head
    frame 223

	shield 10

	passives {
        Metal 1
		Brace 4
		Blind -1
	}
}
```

---

### `ThrobbingCrown`
**Name:** Throbbing Crown  
**Description:** Tentacles attack all adjacent tiles at the end of your turn.  
**Source:** `head_items.gon`  

```
ThrobbingCrown {
    name "ARMOR_THROBBINGCROWN_NAME"
    desc "ARMOR_THROBBINGCROWN_DESC"
    rarity very_rare
    kind head
    frame 172

    passives {
        Metal 1
        StatusEachTurnEnd {
            ImmediateUseAbility head_ThrobbingCrown
        }
    }
}
```

---

### `CrownOfChaos`
**Name:** Crown of Chaos  
**Description:** +2 level up Rerolls. Abilities from all classes are offered when you level up.  
**Source:** `head_items.gon`  

```
CrownOfChaos {
    name "ARMOR_CROWNOFCHAOS_NAME"
    desc "ARMOR_CROWNOFCHAOS_DESC"
    rarity very_rare
    kind head
    frame 173
	set Hybrid

    passives {
		AddLevelUpRerolls 2
		LevelUpClassOverride Jester
    }
}
```

---

### `ChildsCrown`
**Name:** Child's Crown  
**Description:** Your basic attack becomes holy and can heal allies.  
**Source:** `head_items.gon`  

```
ChildsCrown {
    name "ARMOR_CHILDSCROWN_NAME"
    desc "ARMOR_CHILDSCROWN_DESC"
    rarity very_rare
    kind head
    frame 174

    passives {
        Metal 1
        AddElementsToBasicAttack Holy
        AddStatusToBasicAttack {
            DamageOrHealConditionally 1
        }
    }
}
```

---

### `TinasBellyButton`
**Name:** Tina's Belly Button  
**Description:** When you get a kill, gain +1 Health Regen.  
**Source:** `head_items.gon`  

```
TinasBellyButton {
    name "ARMOR_TINASBELLYBUTTON_NAME"
    desc "ARMOR_TINASBELLYBUTTON_DESC"
    rarity very_rare
    kind head
    frame 175

    passives {
		StatusOnKill {
			HealthRegenUp 1
		}
    }
}
```

---

### `HitlersToupe`
**Name:** Hitler's Toupe  
**Description:** Permanent Madness. Give Madness to a random enemy at the end of your turn.  
**Source:** `head_items.gon`  

```
HitlersToupe {
    name "ARMOR_HITLERSTOUPE_NAME"
    desc "ARMOR_HITLERSTOUPE_DESC"
    rarity very_rare
    kind head
    frame 225
	set [Man, Used]

	str 2
	dex 2

    passives {
		PermanentMadness 1
		StatusEachTurnEnd {
			ForceUseAbility head_HitlersToupe
		}
    }
}
```

---

### `StevensHat`
**Name:** Steven's Hat  
**Description:** Your spells cost 0. You can only cast each of your spells once per turn.  
**Source:** `head_items.gon`  

```
StevensHat {
    name "ARMOR_STEVENSHAT_NAME"
    desc "ARMOR_STEVENSHAT_DESC"
    rarity very_rare
    kind head
    frame 177
	set Steven

    int -9
	cha -9

	passives {
		SetSpellCosts 0
		MakeSpellsRequireCharge 1
	}
}
```

---

### `StevensHelmet`
**Name:** Steven's Helmet  
**Description:** When you are downed, give another allied cat 2 random disorders, or to yourself if you're alone.  
**Source:** `head_items.gon`  

```
StevensHelmet {
    name "ARMOR_STEVENSHELMET_NAME"
    desc "ARMOR_STEVENSHELMET_DESC"
    rarity very_rare
    kind head
    frame 176
	set Steven

    shield 20
	
    passives {
        SetDefaultFacePassive euphoric
        Fragile 1
        StatusOnBreak {
            ApplyToRandomPartyMemberIfPossible {
                GainDisorderFromPool all_disorders
                GainDisorderFromPool all_disorders
            }
        }
    }
}
```

---

### `StevenHat1`
**Name:** Steven  
**Description:** Your explosions are much, much bigger!
You have explosion immunity.  
**Source:** `head_items.gon`  

```
StevenHat1 {
    name "ARMOR_STEVENHAT1_NAME"
    desc "ARMOR_STEVENHAT1_DESC"
    rarity very_rare
    kind head
    frame 178
	set Steven
    
    passives {
		ExplosionImmunity 1
		IncreaseExplosionSize 7
        IncreaseExplosionDamage 2
    }
}
```

---

### `StevenHat2`
**Name:** Steven  
**Description:** Each time you cast a spell, gain +1 range and +1 reach until the end of the turn.  
**Source:** `head_items.gon`  

```
StevenHat2 {
    name "ARMOR_STEVENHAT2_NAME"
    desc "ARMOR_STEVENHAT2_DESC"
    rarity very_rare
    kind head
    frame 179
	set Steven
	
	passives {
		StatusAfterCastSpell {
			TempRangeUp 1
            TempMeleeRangeUp 1
		}
	}
}
```

---

## File: `legacy_quest_items.gon`

### `ThrobbingGristle`
**Name:** Throbbing Gristle  
**Description:** Take it to the Wall of Flesh in the Caves.
All units die when they get downed.
Use: A melee attack that turns things it kills into Meat.  
**Source:** `legacy_quest_items.gon`  

```
ThrobbingGristle {
	name "ITEM_THROBBINGGRISTLE_NAME"
    desc "ITEM_THROBBINGGRISTLE_DESC"
    kind weapon
    frame 162
    quest_item true
    legacy_quest true
    hint_destination caves
    rarity quest
    indestructible true
	set Meat

    ability wp_ThrobbingGristle

    global_passives {
        NoCorpses 1
    }
}
```

---

### `PutridLeech`
**Name:** Putrid Leech  
**Description:** Take it to the Throbbing Artery in the Boneyard.
You never level up and die when downed. You have Lifesteal on all of your attacks and abilities.  
**Source:** `legacy_quest_items.gon`  

```
PutridLeech {
	name "ARMOR_PUTRIDLEECH_NAME"
    desc "ARMOR_PUTRIDLEECH_DESC"
    kind head
    frame 97
    quest_item true
    legacy_quest true
    hint_destination boneyard
    rarity quest
    indestructible true
    cursed true
    parasite true
	set Leech

    prevent_level_up true
    passives {
        AddStatusToBasicAttack {
            Leech 1
        }
        AddStatusToSpells {
            Leech 1
        }
        AddStatusToWeapons {
            Leech 1
        }
        AddCorpseHealth -999999
        SpawnOnDeath {
            obj BeefyCharmedLeech
            faction solitary_enemies
        }
    }
}
```

---

### `GuillotinasHead`
**Name:** Guillotina's Head  
**Description:** Take it to the Meat Altar in the Throbbing Domain.
All battles are Hard battles. Enemies will attack you instead of your allies if they can. Units that contact or attack you have a chance to be Feared. Your basic attack has a +10% chance to inflict Fear.  
**Source:** `legacy_quest_items.gon`  

```
GuillotinasHead {
	name "ARMOR_GUILLOTINASHEAD_NAME"
    desc "ARMOR_GUILLOTINASHEAD_DESC"
    kind face
    frame 95
    quest_item true
    legacy_quest true
    hint_destination meatworld
    hint_prerequisite_flag mapflag_MeatWorldUnlocked
    rarity quest
    indestructible true
    cursed true
	set [Meat, Guts]

    global_tags [upgrade_basic_combats_to_hard]

    passives {
        TauntAlways 1

        RevengeDamage {
            effects {
                Fear [1, .5]
            }
        }

        AddStatusToBasicAttack {
            Fear [1 .1]
        }
    }
}
```

---

### `ScaldingOrb`
**Name:** Scalding Orb  
**Description:** Feed it to the Man in the Moon.
Toss it to allies with open weapon slots to avoid taking Burn 3 each turn!
Applies Burn 3 to units adjacent to allies that catch it.  
**Source:** `legacy_quest_items.gon`  

```
ScaldingOrb {
	name "ITEM_SCALDINGORB_NAME"
    desc "ITEM_SCALDINGORB_DESC"
    kind weapon
    frame 163
    quest_item true
    legacy_quest true
    hint_destination moon
    rarity quest
    indestructible true
	set Molten
    
    ability wp_ScaldingOrb
	
	spd 3

    passives {
        StatusEachTurnEnd {
            Burn 3
        }
        ScaldingOrbMoonBossOneShot {
            CompleteItemQuest ScaldingOrb
            RemoveItem ScaldingOrb
        }
    }
}
```

---

### `BlackShard`
**Name:** Black Shard  
**Description:** Use: Absorb a unit with {aux} or less health to power this item up.
Transforms after 20 absorptions.
\[s:.7\](Saves its power across multiple runs.)\[/s\]
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `legacy_quest_items.gon`  

```
BlackShard {
	name "ITEM_BLACKSHARD_NAME"
    desc "ITEM_BLACKSHARD_DESC"
    kind weapon
    frame 164
    quest_item true
    legacy_quest true
    hint_destination core
    rarity quest
    indestructible true
	set Obelisk

    aux 1
    
    ability wp_BlackShard

    passives {
        ItemAuxTransform {
            ge [20 BlackShard_Glowing]
        }
    }
}
```

---

### `BlackShard_Glowing`
**Name:** Glowing Black Shard  
**Description:** Stab it into The Coven! 
Use: Deal 5 damage with Lifesteal, inflict Burn 5, and purge all buffs. Instantly kills The Coven.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `legacy_quest_items.gon`  

```
BlackShard_Glowing {
	name "ITEM_BLACKSHARD_GLOWING_NAME"
    desc "ITEM_BLACKSHARD_GLOWING_DESC"
    kind weapon
    frame 166
    quest_item true
    legacy_quest true
    hint_destination core
    rarity quest
    quest_item_alias BlackShard //this is the BlackShard, for the purposes of all the quest item code that is keyed on the item name
    indestructible true
	set Obelisk

    ability wp_BlackShard_Glowing
}
```

---

### `PyrophinasCollar`
**Name:** Pyrophina's Collar  
**Description:** Pyrophina joins you on your journey. She wishes to activate an obelisk on the moon.  
**Source:** `legacy_quest_items.gon`  

```
PyrophinasCollar {
	name "ITEM_PYROPHINASCOLLAR_NAME"
    desc "ITEM_PYROPHINASCOLLAR_DESC"
    kind trinket
    frame 219
    quest_item true
    legacy_quest true
    hint_destination moon
    hint_prerequisite_flag mapflag_BothObelisksUnlocked
    rarity quest
    indestructible true
	set Used

    global_tags [pyrophina_following]

    passives {
        SpawnItemLinkedFamiliar {
            object PyrophinaFamiliar
            break_on_pop_only true
        }
    }
}
```

---

### `ZaratanasCollar`
**Name:** Zaratana's Collar  
**Description:** Zaratana joins you on your journey. She wishes to activate an obelisk in the Core.  
**Source:** `legacy_quest_items.gon`  

```
ZaratanasCollar {
	name "ITEM_ZARATANASCOLLAR_NAME"
    desc "ITEM_ZARATANASCOLLAR_DESC"
    kind trinket
    frame 220
    quest_item true
    legacy_quest true
    hint_destination core
    hint_prerequisite_flag mapflag_BothObelisksUnlocked
    rarity quest
    indestructible true
	set Used

    global_tags [zaratana_following]

    passives {
        SpawnItemLinkedFamiliar {
            object ZaratanaFamiliar
            break_on_pop_only true
        }
    }
}
```

---

### `CryogenicTimeChamber_Empty`
**Name:** Cryogenic Time Chamber  
**Description:** Put the Throbbing King's heart inside it.
All enemy bodies revive to 30% health at the end of each round (except bosses). Find a random pill at the end of each battle.  
**Source:** `legacy_quest_items.gon`  

```
CryogenicTimeChamber_Empty {
	name "ITEM_CRYOGENICTIMECHAMBER_EMPTY_NAME"
    desc "ITEM_CRYOGENICTIMECHAMBER_EMPTY_DESC"
    kind trinket
    frame 224
    quest_item true
    legacy_quest true
    hint_destination meatworld
    hint_prerequisite_flag mapflag_MeatWorldUnlockedFull
    rarity quest
    indestructible true

    passives {
        StatusOnBattleEnd {
            FindItemFromPool pills
        }
    }

    global_passives {
        GlobalEnemyAutoRevive 30%
    }
}
```

---

### `CryogenicTimeChamber_Full`
**Name:** Cryogenic Time Chamber (Throbbing)  
**Description:** Use it on the time machine in the Lab.
All enemy bodies revive to full health at the end of each round (except bosses). +2 Health Regen.  
**Source:** `legacy_quest_items.gon`  

```
CryogenicTimeChamber_Full {
    name "ITEM_CRYOGENICTIMECHAMBER_FULL_NAME"
    desc "ITEM_CRYOGENICTIMECHAMBER_FULL_DESC"
    kind trinket
    frame 225
    quest_item true
    legacy_quest true
    hint_destination lab
    rarity quest
    indestructible true

    passives {
        HealthRegenUp 2
    }

    global_passives {
        GlobalEnemyAutoRevive 100%
    }
}
```

---

### `ReceiverAntenna`
**Name:** Receiver Antenna  
**Description:** Place it far in the past.
All events cause special happenings.
Gain +2 Charge whenever an ally spends mana.  
**Source:** `legacy_quest_items.gon`  

```
ReceiverAntenna {
    name "ARMOR_RECEIVERANTENNA_NAME"
    desc "ARMOR_RECEIVERANTENNA_DESC"
    kind head
    frame 98
    quest_item true
    legacy_quest true
    hint_destination jurassic
    rarity quest
    indestructible true
	set [Bionic, Cyborg]

    global_tags [all_normal_events_are_weather]

	shield 8

    passives {
        Metal 1
        StatusWhenAllySpendsMana {
            Charge 2
        }
    }
    
}
```

---

### `TransmitterAntenna`
**Name:** Transmitter Antenna  
**Description:** Place it far in the future.
Your spells cost -2 mana. Every time you or another cat casts a spell, scramble that spell for the rest of the battle.  
**Source:** `legacy_quest_items.gon`  

```
TransmitterAntenna {
    name "ARMOR_TRANSMITTERANTENNA_NAME"
    desc "ARMOR_TRANSMITTERANTENNA_DESC"
    kind head
    frame 99
    quest_item true
    legacy_quest true
    hint_destination theend
    rarity quest
    indestructible true
	set [Bionic, Cyborg]

    passives {
        Metal 1
        AlliesScrambleSpellAfterCast 1
		ReduceManaCost 2
    }
}
```

---

### `SignalAmplifier`
**Name:** Signal Amplifier  
**Description:** Place it on a floating head inside The Rift.
Spawn a random robot miniboss with Madness at the end of the first round.
Use: Energize all robots and give yourself All Stats Up.  
**Source:** `legacy_quest_items.gon`  

```
SignalAmplifier {
    name "ITEM_SIGNALAMPLIFIER_NAME"
    desc "ITEM_SIGNALAMPLIFIER_DESC"
    kind weapon
    frame 165
    quest_item true
    legacy_quest true
    hint_destination dimensionx
    hint_prerequisite_flag mapflag_DimensionXUnlocked
    rarity quest
    indestructible true
	set [Bionic, Cyborg]

    ability wp_SignalAmplifier

    passives {
        AbilityOnRoundEndOnce {
            ability wp_SignalAmplifierSpawnTerminator
            even_of_stunned true
        }
    }
}
```

---

### `JarOfRadiation`
**Name:** Jar of Radiation  
**Description:** Fill it with the blood of the Throbbing King.
At the end of your turn, deal 1 damage to EVERYTHING. At the end of each battle, gain +1 to a random stat and -1 to a random stat, permanently.  
**Source:** `legacy_quest_items.gon`  

```
JarOfRadiation { //end of turn: deal 1 damage to everything (pestillence). take it to throbbing king corpse
    name "ITEM_JAROFRADIATION_NAME"
    desc "ITEM_JAROFRADIATION_DESC"
    kind trinket
    frame 222
    quest_item true
    legacy_quest true
    hint_destination meatworld
    rarity quest
    indestructible true
	set Radioactive

    failable true

    passives {
        StatusEachTurnEnd {
            ForceUseAbility tk_JarOfRadiation
        }

        StatusOnBattleEnd {
            even_if_dead true

            RandomPermanentStat 1
            RandomPermanentStat -1
        }
    }
}
```

---

### `JarOfRadiatedBlood`
**Name:** Jar of Radiated Blood  
**Description:** Add a bit of Chaos to it from The Rift.
Whenever you take damage, spawn a friendly Clot that can grow into a copy of yourself. At the end of each battle, gain +2 to a random stat and -2 to a random stat, permanently.  
**Source:** `legacy_quest_items.gon`  

```
JarOfRadiatedBlood { //when the cat holding the jar takes damage, spawn a clot. the clot evolves into a mini me of the cat that holding the jar
    name "ITEM_JAROFRADIATEDBLOOD_NAME"
    desc "ITEM_JAROFRADIATEDBLOOD_DESC"
    kind trinket
    frame 223
    quest_item true
    legacy_quest true
    hint_destination dimensionx
    rarity quest
    indestructible true
	set Radioactive

    failable true

    passives {
        SpawnThingOnDamage {
            object CatCopyClot
            good false //from the perspective of the thing attacking
            spawn_on_death_hit false
        }

        StatusOnBattleEnd {
            even_if_dead true

            RandomPermanentStat 2
            RandomPermanentStat -2
        }
    }
}
```

---

### `JarOfChaos`
**Name:** Jar Of Chaos  
**Description:** Bring it to Dr. Beanies.
...or drink it to permanently gain All Stats Up 2 and upgrade all of your spells.  
**Source:** `legacy_quest_items.gon`  

```
JarOfChaos { 
    name "ITEM_JAROFCHAOS_NAME"
    desc "ITEM_JAROFCHAOS_DESC"
    kind trinket
    frame 239
    quest_item true
    legacy_quest true
    indestructible true
    rarity quest
    consumable true
    durability 1
    dont_destroy_on_0 true
	set Radioactive

    failable true

    ability cm_JarOfChaos

    passives {
        DurabilityTransform {
            eq [0 JarOfNothing]
        }
    }
}
```

---

### `JarOfNothing`
**Name:** Jar Of Nothing  
**Description:** It's trash now.  
**Source:** `legacy_quest_items.gon`  

```
JarOfNothing { 
    name "ITEM_JAROFNOTHING_NAME"
    desc "ITEM_JAROFNOTHING_DESC"
    kind trinket
    frame 242
    rarity common
    dont_destroy_on_0 true
}
```

---

### `Nuke`
**Name:** Nuke  
**Description:** Take it to The Infinite and wait for the signal from Dr. Beanies to set it off.
+2 Brace. If this cat dies, it explodes and damages everything for 50.
Bonus Ability: Trigger the Nuke.  
**Source:** `legacy_quest_items.gon`  

```
Nuke {
    name "ARMOR_NUKE_NAME"
    desc "ARMOR_NUKE_DESC"
    kind neck
    frame 77
    quest_item true
    legacy_quest true
    hint_destination endoftime
    rarity quest
    indestructible true
	set Radioactive

    shield 10
    spd -2

    failable true

    passives {
        Metal 1
        AddHiddenTag the_nuke_bearer
        BonusAbility neck_NukeBonus
        DeathRattle neck_NukeExplode
        Brace 2
    }
}
```

---

## File: `legendary_items.gon`

### `TinksBow`
**Name:** Fancy Bow  
**Description:** It's fancy.  
**Source:** `legendary_items.gon`  

```
TinksBow {
    name "ARMOR_TINKSBOW_NAME"
    desc "ARMOR_TINKSBOW_DESC"
    rarity very_rare
    kind head
    frame 113
    degrade_after_adventure false
}
```

---

## File: `modifiers.gon`

### `LearnPassive`
**Name:** {str_aux_passive_name} Syringe  
**Description:** Use to immediately teach a cat the passive ability: {str_aux_passive_name}

{str_aux_passive_desc}  
**Source:** `modifiers.gon`  

```
LearnPassive {
    name "ITEM_LEARNPASSIVE_NAME"
    desc "ITEM_LEARNPASSIVE_DESC"
    kind modifier

    str_aux_initialize random_class_passive
    icon_hint passive_syringe

    frame 12
}
```

---

### `LearnDisorder`
**Name:** {str_aux_passive_name} Syringe  
**Description:** Use to immediately give a cat the disorder: {str_aux_passive_name}

{str_aux_passive_desc}  
**Source:** `modifiers.gon`  

```
LearnDisorder {
    name "ITEM_LEARNDISORDER_NAME"
    desc "ITEM_LEARNDISORDER_DESC"
    kind modifier

    str_aux_initialize random_disorder
    icon_hint passive_syringe

    frame 12
}
```

---

### `LearnAbility`
**Name:** {str_aux_active_name} Syringe  
**Description:** Use to immediately teach a cat the active ability: {str_aux_active_name}

{str_aux_active_desc}  
**Source:** `modifiers.gon`  

```
LearnAbility {
    name "ITEM_LEARNABILITY_NAME"
    desc "ITEM_LEARNABILITY_DESC"
    kind modifier

    str_aux_initialize random_class_ability
    icon_hint ability_syringe

    frame 13
}
```

---

## File: `neck_items.gon`

### `LionMane`
**Name:** Lion Mane  
**Description:** ARMOR_LIONMANE_DESC  
**Source:** `neck_items.gon`  

```
LionMane {
    name "ARMOR_LIONMANE_NAME"
    desc "ARMOR_LIONMANE_DESC"
    rarity uncommon
    kind neck
    frame 1

    str 1
    con 1
    cha 1
	int -1
	spd -1
}
```

---

### `Gobbler`
**Name:** Gobbler  
**Description:** Units that contact you are knocked back 2 tiles.  
**Source:** `neck_items.gon`  

```
Gobbler {
    name "ARMOR_GOBBLER_NAME"
    desc "ARMOR_GOBBLER_DESC"
    rarity uncommon
    kind neck
    frame 22
	set Fatty

    con 4
    spd -2

    passives {
        MeleeRevengeDamage {
            knockback 2
        }
    }
}
```

---

### `SpikedCollar`
**Name:** Spiked Collar  
**Description:** +2 Thorns.  
**Source:** `neck_items.gon`  

```
SpikedCollar {
    name "ARMOR_SPIKEDCOLLAR_NAME"
    desc "ARMOR_SPIKEDCOLLAR_DESC"
    rarity uncommon
    kind neck
    frame 24

    passives {
        Thorns 2
        Metal 1
    }
}
```

---

### `FrankBolts`
**Name:** Frank Bolts  
**Description:** Electric immunity.
Electric damage revives you when downed.  
**Source:** `neck_items.gon`  

```
FrankBolts {
    name "ARMOR_FRANKBOLTS_NAME"
    desc "ARMOR_FRANKBOLTS_DESC"
    rarity uncommon
    kind neck
    frame 21
	set [Bionic, Cyborg]

	shield 2
	
    passives {
        FrankBolts 1
        Metal 1
    }
}
```

---

### `FortuneNecklace`
**Name:** Fortune Necklace  
**Description:** Spawn 3-6 coins at the start of each battle.
Fragile.  
**Source:** `neck_items.gon`  

```
FortuneNecklace {
    name "ARMOR_FORTUNENECKLACE_NAME"
    desc "ARMOR_FORTUNENECKLACE_DESC"
    rarity common
    kind neck
    frame 23

    passives {
        Fragile 1
        SpawnOnBattleStartRandomEmptyTile {
            object Coin
            number [3 6]
        }
    }
}
```

---

### `Scarf`
**Name:** Scarf  
**Description:** Ice immunity.  
**Source:** `neck_items.gon`  

```
Scarf {
    name "ARMOR_SCARF_NAME"
    desc "ARMOR_SCARF_DESC"
    rarity common
    kind neck
    frame 50

    cha 1

    passives {
        ElementImmune Ice
        StatusImmunity [Freeze, Slow]
    }
}
```

---

### `BulletproofVest`
**Name:** Bulletproof Vest  
**Description:** Injury immunity.  
**Source:** `neck_items.gon`  

```
BulletproofVest {
    name "ARMOR_BULLETPROOFVEST_NAME"
    desc "ARMOR_BULLETPROOFVEST_DESC"
    rarity uncommon
    kind neck
    frame 51

    spd -1
    dex -1

    passives {
        InjuryImmunity 1
    }
}
```

---

### `LuckyToe`
**Name:** Lucky Toe  
**Description:** ARMOR_LUCKYTOE_DESC  
**Source:** `neck_items.gon`  

```
LuckyToe {
    name "ARMOR_LUCKYTOE_NAME"
    desc "ARMOR_LUCKYTOE_DESC" //intentionally blank description
    rarity uncommon
    kind neck
    frame 53
	set [HumanFlesh, Lucky, Twine]

    lck 2

    passives {
        ChanceToForceEvent {
            chance 25%
            event Blessing
        }
    }
}
```

---

### `Bling`
**Name:** Bling  
**Description:** ARMOR_BLING_DESC  
**Source:** `neck_items.gon`  

```
Bling {
    name "ARMOR_BLING_NAME"
    desc "ARMOR_BLING_DESC"
    rarity uncommon
    kind neck
    frame 54

    shield 4
    spd -2
    cha 2

    passives {
        Metal 1
    }
}
```

---

### `OddMedallion`
**Name:** Odd Medallion  
**Description:** Deal 1 electric damage to units that contact or attack you.
25% chance to poop every time you take damage.  
**Source:** `neck_items.gon`  

```
OddMedallion {
    name "ARMOR_ODDMEDALLION_NAME"
    desc "ARMOR_ODDMEDALLION_DESC"
    rarity very_rare
    kind neck
    frame 55
	set [Used, Twine, Demonic]
    cursed true

    spd 6

    passives {
        PoopWhenHit {
            chance 25%
            object Poop
        }
        RevengeDamage {
            damage 1
            effects {
                VisualFXTile WaterConduct
            }
            elements [
                Electric
            ]
        }
    }
}
```

---

### `FishNecklace`
**Name:** Fish Necklace  
**Description:** Poisonous 1.
Damage you deal inflicts Rot 1.
Allied flies have +2 Damage.  
**Source:** `neck_items.gon`  

```
FishNecklace {
    name "ARMOR_FISHNECKLACE_NAME"
    desc "ARMOR_FISHNECKLACE_DESC"
    rarity rare
    kind neck
    frame 57
	set [Rotten, Twine]

    cha -6
    shield 3

    passives {
        AddStatusToAllDamage {
            Rot 1
        }
        PoisonThorns 1
        FlyDamageIncrease {
            stacks 2
            allies_only true
        }
    }
}
```

---

### `TwoOfSpades`
**Name:** Two of Spades  
**Description:** Double cast spells that cost 1 or 2 mana.  
**Source:** `neck_items.gon`  

```
TwoOfSpades {
    name "ARMOR_TWOOFSPADES_NAME"
    desc "ARMOR_TWOOFSPADES_DESC"
    rarity uncommon
    kind neck
	set Twine
    frame 88

    passives {
        DoubleCastSpellIfManaCostUnderThreshold 3
    }
}
```

---

### `ColostomyBag`
**Name:** Colostomy Bag  
**Description:** Spawn Charmed Dips randomly when you move over tiles.
While downed, spawn a Charmed Dip at the end of each round.  
**Source:** `neck_items.gon`  

```
ColostomyBag {
    name "ARMOR_COLOSTOMYBAG_NAME"
    desc "ARMOR_COLOSTOMYBAG_DESC"
    rarity uncommon
    kind neck
    frame 89
	set [Fecal, Used]

    passives {
        ObjectDetector {
            object CharmedDip
            chance 10%
        }

        PassiveWhenDead {
            StatusEachRoundEnd {
                DoDamage {
                    damage 0
                    type spell
                    damage_tiles all

                    effects {
                        BounceObject CharmedDip
                    }
                }
            }
        }
    }
}
```

---

### `SurvivalistGaiter`
**Name:** Survivalist's Gaiter  
**Description:** +40% Dodge Chance while standing in tall grass.
Start each battle with Stealth 1. Lose this stealth when you use your basic attack.  
**Source:** `neck_items.gon`  

```
SurvivalistGaiter {
    name "ARMOR_SURVIVALISTGAITER_NAME"
    desc "ARMOR_SURVIVALISTGAITER_DESC"
    rarity uncommon
    kind neck
    frame 90
	set Survivalist 

    passives {
        StatusOnBattleStart {
            StealthUntilBasicAttack 1
        }
        PassiveWhenOnTile {
            tile [TallGrassTile TallFlowerTile]
            passives {
                DodgeChance_Status 40
            }
        }
    }
}
```

---

### `PeaceSymbol`
**Name:** Peace Symbol  
**Description:** If you end your turn without dealing damage, gain +1 [img:divineshield].  
**Source:** `neck_items.gon`  

```
PeaceSymbol {
    name "ARMOR_PEACESYMBOL_NAME"
    desc "ARMOR_PEACESYMBOL_DESC"
    rarity uncommon
    kind neck
    frame 91
	set [Hippie, Twine]

    keyword_tooltips { DivineShield 1 }

    passives {
        StatusEachTurnBegin {
            BlessingOfPeace 1
        }
    }
}
```

---

### `EmptyGenerator`
**Name:** Empty Generator  
**Description:** When you spend 12 or more mana in a turn, refresh your basic attack.  
**Source:** `neck_items.gon`  

```
EmptyGenerator {
    name "ARMOR_EMPTYGENERATOR_NAME"
    desc "ARMOR_EMPTYGENERATOR_DESC"
    rarity uncommon
    kind neck
    frame 92

    shield 2

    passives {
        Metal 1
        ScaledStatusOnSpendMana {
            StatusAfterXStacks {
                stack_key EMPTY_GENERATOR
                threshold 12
                expires_on_end_turn true

                RefreshActPoints 1
            }
        }
    }
}
```

---

### `DarkFriend`
**Name:** Dark Friend  
**Description:** At the start of your turn, spawn a Shadow copy that mimics your basic attack and fades at the end of the turn.
Units that contact or attack you have a 15% chance to be Feared.  
**Source:** `neck_items.gon`  

```
DarkFriend {
    name "ARMOR_DARKFRIEND_NAME"
    desc "ARMOR_DARKFRIEND_DESC"
    rarity rare
    kind neck
    frame 93
	set Demonic

    passives {
        RevengeDamage {
            effects {
                Fear [1, .15]
            }
        }
        StatusEachTurnBegin {
            UseAbility neck_DarkFriend
        }
    }
}
```

---

### `FannyPack`
**Name:** Fanny Pack  
**Description:** Spawn 1-2 extra pickups at the start of each battle.
After you collect your 3rd pickup, you can move an extra time each turn.  
**Source:** `neck_items.gon`  

```
FannyPack {
    name "ARMOR_FANNYPACK_NAME"
    desc "ARMOR_FANNYPACK_DESC"
    rarity common
    kind neck
	set [Leather, Survivalist]
    frame 125

    passives {
        SpawnExtraThingsOnBattleStart {
            object RandomPickup
            number [1 2]
        }
        StatusOnCollectPickup {
            StatusAfterXStacks {
                stack_key FANNY_PACK
                threshold 3

                ExtraBasicMoves_Status 1
            }
        }
    }
}
```

---

### `MorphineDrip`
**Name:** Morphine Drip  
**Description:** Damage you take is reduced by 3.
Damage prevented this way is delayed and taken at the end of your turn, all at once.  
**Source:** `neck_items.gon`  

```
MorphineDrip {
    name "ARMOR_MORPHINEDRIP_NAME"
    desc "ARMOR_MORPHINEDRIP_DESC"
    rarity rare
    kind neck
    frame 128
	set [Medical, Nurse]

    passives {
        ConvertDamageToScaledStatus {
            stacks 3
            DelayedPain 1
        }
    }
}
```

---

### `LeatherJacket`
**Name:** Leather Jacket  
**Description:** If you would take exactly 1 damage, take 0 instead.  
**Source:** `neck_items.gon`  

```
LeatherJacket {
    name "ARMOR_LEATHERJACKET_NAME"
    desc "ARMOR_LEATHERJACKET_DESC"
    rarity rare
    kind neck
    frame 132
    set [Leather, Cool]

    shield 3

    passives {
        BlockDamageUnderThreshold 1
    }
}
```

---

### `HealingGauze`
**Name:** Healing Gauze  
**Description:** You have +3 Health Regen as long as you have [img:shield].  
**Source:** `neck_items.gon`  

```
HealingGauze {
    name "ARMOR_HEALINGGAUZE_NAME"
    desc "ARMOR_HEALINGGAUZE_DESC"
    rarity uncommon
    kind neck
    frame 134
	set [Mummy, Nurse]

    passives {
        PassiveWhileShielded {
            HealthRegenUp 3
        }
    }
}
```

---

### `MarkIV`
**Name:** Mark IV  
**Description:** After every fourth spell you cast, gain +2 [img:int].  
**Source:** `neck_items.gon`  

```
MarkIV {
    name "ARMOR_MARKIV_NAME"
    desc "ARMOR_MARKIV_DESC"
    rarity uncommon
    kind neck
    frame 94

    passives {
        Metal 1
        StatusEveryXSpellCasts {
            stacks 4
            IntelligenceUp 2
        }
    }
}
```

---

### `MamaLeech`
**Name:** Mama Leech  
**Description:** After every third spell you cast, spawn a Leech familiar.  
**Source:** `neck_items.gon`  

```
MamaLeech {
    name "ARMOR_MAMALEECH_NAME"
    desc "ARMOR_MAMALEECH_DESC"
    rarity uncommon
    kind neck
    frame 95
	set [Leech, Mother]

    passives {
        StatusEveryXSpellCasts {
            stacks 3
            ObjectOnHitCharacter {
                stacks 1
                object CharmedLeech
            }
        }
    }
}
```

---

### `FuryDice`
**Name:** Furry Dice  
**Description:** You can reroll your options when you level up.  
**Source:** `neck_items.gon`  

```
FuryDice {
    name "ARMOR_FURYDICE_NAME"
    desc "ARMOR_FURYDICE_DESC"
    rarity uncommon
    kind neck
    frame 97
	set [Lucky, Twine]

    lck 1

    passives {
        AddLevelUpRerolls 1
    }
}
```

---

### `DNAMultiplier`
**Name:** DNA Multiplier  
**Description:** Double all status effects that get applied to you.  
**Source:** `neck_items.gon`  

```
DNAMultiplier {
    name "ARMOR_DNAMULTIPLIER_NAME"
    desc "ARMOR_DNAMULTIPLIER_DESC"
    rarity rare
    kind neck
    frame 99

    passives {
        Metal 1
        DoubleReceivedNegativeStatus 1
        DoubleReceivedPositiveStatus 1
    }
}
```

---

### `PackOfBlades`
**Name:** Pack of Blades  
**Description:** Whenever you backstab, gain +1 Serrated Claws.  
**Source:** `neck_items.gon`  

```
PackOfBlades {
    name "ARMOR_PACKOFBLADES_NAME"
    desc "ARMOR_PACKOFBLADES_DESC"
    rarity uncommon
    kind neck
    frame 121

    passives {
        Metal 1
        StatusOnBackstab {
            SerratedClaws 1
        }
    }
}
```

---

### `Backpack`
**Name:** Backpack  
**Description:** 50% chance to find an extra consumable item at the end of each battle.
When you use up a consumable or trinket, equip a new consumable from your inventory if you have any.  
**Source:** `neck_items.gon`  

```
Backpack {
    name "ARMOR_BACKPACK_NAME"
    desc "ARMOR_BACKPACK_DESC"
    rarity uncommon
    kind neck
    frame 123
	set Survivalist

    passives {
        StatusOnBattleEnd {
            Conditional_GoodRoll {
                odds 50%
                FindItemFromPool consumables
            }
        }
        AutoEquipConsumables 1
    }
}
```

---

### `StoneOrbit`
**Name:** Stone Orbit  
**Description:** Spawn a small rock when you take damage.  
**Source:** `neck_items.gon`  

```
StoneOrbit {
    name "ARMOR_STONEORBIT_NAME"
    desc "ARMOR_STONEORBIT_DESC"
    rarity uncommon
    kind neck
    frame 126
    set [Rock, Planet]

    shield 2

    passives {
        SpawnThingOnDamage {
            object SmallRock
        }
    }
}
```

---

### `AngelicProtection`
**Name:** Angelic Protection  
**Description:** 33% chance to teleport to a random tile when targeted by an enemy.  
**Source:** `neck_items.gon`  

```
AngelicProtection {
    name "ARMOR_ANGELICPROTECTION_NAME"
    desc "ARMOR_ANGELICPROTECTION_DESC"
    rarity rare
    kind neck
    frame 127
	set Cleric

    passives {
        ChanceToBackflip {
            ability BlinkDodge
            chance 33%
        }
    }
}
```

---

### `ChefsApron`
**Name:** Chef's Apron  
**Description:** At the end of each turn, gain +1 [img:con] and spawn a random food pickup within 2 tiles.  
**Source:** `neck_items.gon`  

```
ChefsApron {
    name "ARMOR_CHEFSAPRON_NAME"
    desc "ARMOR_CHEFSAPRON_DESC"
    rarity uncommon
    kind neck
    frame 131
	set Butcher

    passives {
        StatusEachTurnEnd {
            ConstitutionUp 1
            ForceUseAbility neck_ChefsApron
        }
    }
}
```

---

### `RadarDish`
**Name:** Radar Dish  
**Description:** One random enemy becomes Marked at the start of each turn.  
**Source:** `neck_items.gon`  

```
RadarDish {
    name "ARMOR_RADARDISH_NAME"
    desc "ARMOR_RADARDISH_DESC"
    rarity uncommon
    kind neck
    frame 133
	set [Cyborg, Bionic, Space]

    passives {
        Metal 1
        ApplyStatusesToRandomEnemiesEachTurn {
            count 1
            Marked 1
        }
    }
}
```

---

### `ExtraSetOfEyes`
**Name:** Extra Set of Eyes  
**Description:** At the end of each turn, gain +1 Preemptive Counterattack.  
**Source:** `neck_items.gon`  

```
ExtraSetOfEyes {
    name "ARMOR_EXTRASETOFEYES_NAME"
    desc "ARMOR_EXTRASETOFEYES_DESC"
    rarity rare
    kind neck
    frame 135
	set Space

    passives {
        StatusEachTurnEnd {
            PreEmptiveCounterNextAttacks 1
        }
    }
}
```

---

### `SharkTooth`
**Name:** Large Shark Tooth  
**Description:** Your basic attack inflicts +1 Bleed. Take an extra turn at the end of the round for each Bleeding enemy. You are uncontrollable during these turns.  
**Source:** `neck_items.gon`  

```
SharkTooth { //Aquired from Giant Sleeping Shark event.
    name "ARMOR_SHARKTOOTH_NAME"
    desc "ARMOR_SHARKTOOTH_DESC"
    rarity rare
    kind neck
    frame 162
	set Twine

    passives {
        SharkySmellsBlood 1
        AddStatusToBasicAttack {
            Bleed 1
        }
    }
}
```

---

### `SmallRune`
**Name:** Small Rune  
**Description:** +10% Dodge Chance.  
**Source:** `neck_items.gon`  

```
SmallRune {
    name "ARMOR_SMALLRUNE_NAME"
    desc "ARMOR_SMALLRUNE_DESC"
    rarity common
    kind neck
    frame 169
	set [Rune, Twine]

    passives {
        ArmorDodgeChance 10%
    }
}
```

---

### `QuartzNecklace`
**Name:** Quartz Necklace  
**Description:** +1 Brace.  
**Source:** `neck_items.gon`  

```
QuartzNecklace {
    name "ARMOR_QUARTZNECKLACE_NAME"
    desc "ARMOR_QUARTZNECKLACE_DESC"
    rarity common
    kind neck
    frame 168
	set [Gemstone, Twine]

    passives {
        Brace 1
    }
}
```

---

### `CinderBlock`
**Name:** Cinder Block  
**Description:** ARMOR_CINDERBLOCK_DESC  
**Source:** `neck_items.gon`  

```
CinderBlock {
    name "ARMOR_CINDERBLOCK_NAME"
    desc "ARMOR_CINDERBLOCK_DESC"
    rarity common
    kind neck
    frame 167
	set Rock

	shield 3
}
```

---

### `BoxingCharm`
**Name:** Boxing Charm  
**Description:** Start with +1 bonus attack.  
**Source:** `neck_items.gon`  

```
BoxingCharm {
    name "ARMOR_BOXINGCHARM_NAME"
    desc "ARMOR_BOXINGCHARM_DESC"
    rarity common
    kind neck
    frame 165
	set [Fighter, Twine]

    passives {
        Quivered 1
    }
}
```

---

### `Crucifix`
**Name:** Crucifix  
**Description:** ARMOR_CRUCIFIX_DESC  
**Source:** `neck_items.gon`  

```
Crucifix {
    name "ARMOR_CRUCIFIX_NAME"
    desc "ARMOR_CRUCIFIX_DESC"
    rarity common
    kind neck
    frame 173
	set Cleric

    divine_shield 1
}
```

---

### `TatteredScrap`
**Name:** Tattered Scrap  
**Description:** When you take damage, spawn a scrap pickup.  
**Source:** `neck_items.gon`  

```
TatteredScrap {
    name "ARMOR_TATTEREDSCRAP_NAME"
    desc "ARMOR_TATTEREDSCRAP_DESC"
    rarity common
    kind neck
    frame 171
	set [Tinkerer, Scrap]

    passives {
        Metal 1
        SpawnThingOnDamage {
            object Scrap
			good false //good relative to the thing attacking, for luck calculations
        }
    }
}
```

---

### `MeekStone`
**Name:** Meek Stone  
**Description:** You have All Stats Up while at 10 or less health.  
**Source:** `neck_items.gon`  

```
MeekStone {
    name "ARMOR_MEEKSTONE_NAME"
    desc "ARMOR_MEEKSTONE_DESC"
    rarity common
    kind neck
    frame 172
	set Gemstone

    passives {
        PassiveAtHealthThreshold {
            threshold 10
            mode less_or_equal
            
            passives {
                AllStatsUp 1
            }
        }
    }
}
```

---

### `Stomach`
**Name:** Stomach  
**Description:** Consumables you use have double the effect.  
**Source:** `neck_items.gon`  

```
Stomach {
    name "ARMOR_STOMACH_NAME"
    desc "ARMOR_STOMACH_DESC"
    rarity uncommon
    kind neck
    frame 174
    set Guts

    passives {
        ConsumableEffectsMultiplierBonus 1
    }
}
```

---

### `WaterFeeder`
**Name:** Water Feeder  
**Description:** +1 Health Regen.
Become wet at the start of your turn.  
**Source:** `neck_items.gon`  

```
WaterFeeder {
    name "ARMOR_WATERFEEDER_NAME"
    desc "ARMOR_WATERFEEDER_DESC"
    rarity common
    kind neck
    frame 170

    passives {
        HealthRegenUp 1
        StatusEachTurnBegin {
            DrinkWater 1
            Wet 1
        }
    }
}
```

---

### `Scrubs`
**Name:** Scrubs  
**Description:** Heals heal you for 2 extra.  
**Source:** `neck_items.gon`  

```
Scrubs {
    name "ARMOR_SCRUBS_NAME"
    desc "ARMOR_SCRUBS_DESC"
    rarity uncommon
    kind neck
    frame 149
	set [Nurse, Medical]

    passives {
        BoostReceivedHealing 2
    }
}
```

---

### `Scapular`
**Name:** Scapular  
**Description:** ARMOR_SCAPULAR_DESC  
**Source:** `neck_items.gon`  

```
Scapular {
    name "ARMOR_SCAPULAR_NAME"
    desc "ARMOR_SCAPULAR_DESC"
    rarity very_rare
    kind neck
    frame 178
	set Cleric

	divine_shield 1

    str 1
    dex 1
    con 1
    cha 1
	int 1
	spd 1
	lck 1
}
```

---

### `DirtyBionicArmor`
**Name:** Dirty Bionic Armor  
**Description:** +2 Mana Regen, +2 Health Regen.  
**Source:** `neck_items.gon`  

```
DirtyBionicArmor {
	name "ARMOR_DIRTYBIONICARMOR_NAME"
	desc "ARMOR_DIRTYBIONICARMOR_DESC"
	rarity very_rare
	kind neck
	frame 175
	set [DirtClod, Bionic] 

	spd 4

	passives {
		AddManaRegen 2
		HealthRegenUp 2
		Metal 1
	}
}
```

---

### `LuckyTwine`
**Name:** Lucky Twine  
**Description:** 75% chance to Grapple units that make contact with you.  
**Source:** `neck_items.gon`  

```
LuckyTwine {
	name "ARMOR_LUCKYTWINE_NAME"
	desc "ARMOR_LUCKYTWINE_DESC"
	rarity very_rare
	kind neck
	frame 176
	set [Twine, Lucky]
	
	shield 2
	lck 1

	passives {
		MeleeRevengeDamage {
			damage 0
			effects {
				Grappled [1, .75]
			}
		}
	}
}
```

---

### `RavenFeather`
**Name:** Raven Feather  
**Description:** Inflict Soul Link on 2 random enemies at the start of each battle.  
**Source:** `neck_items.gon`  

```
RavenFeather {
    name "ARMOR_RAVENFEATHER_NAME"
    desc "ARMOR_RAVENFEATHER_DESC"
	rarity rare
	kind neck
	frame 179
	set Feathered
    
    passives {
		AbilityOnBattleStart RandomDualSoulLink
    }
}
```

---

### `LostSoul`
**Name:** Lost Soul  
**Description:** The first time you are downed each battle, revive to full HP.  
**Source:** `neck_items.gon`  

```
LostSoul {
    name "ARMOR_LOSTSOUL_NAME"
    desc "ARMOR_LOSTSOUL_DESC"
	rarity very_rare
	kind neck
	frame 180
    
    passives {
        Eternal {
            stacks 1
            health_percent 100%
        }
    }
}
```

---

### `MothersTeeth`
**Name:** Mother's Teeth  
**Description:** +6 Bleed Thorns, +6 Thorns, +6 Bleed.  
**Source:** `neck_items.gon`  

```
MothersTeeth {
    name "ARMOR_MOTHERSTEETH_NAME"
    desc "ARMOR_MOTHERSTEETH_DESC"
	rarity very_rare
	kind neck
	frame 187
	set Mother
    
    passives {
		BleedThorns 6
		Thorns 6
		Bleed 6
    }
}
```

---

### `MegaPoop`
**Name:** Mega Poop  
**Description:** Leave poop behind when you move.
Spawn 2-3 pickups whenever you destroy a poop.  
**Source:** `neck_items.gon`  

```
MegaPoop {
    name "ARMOR_MEGAPOOP_NAME"
    desc "ARMOR_MEGAPOOP_DESC"
	rarity rare
	kind neck
	frame 186
	set Fecal
    
	cha -1
	shield 4
	
    passives {
		LeaveBehindOnceEachMove Poop
        SpawnRandomPickupsOnTaggedUnitKilled {
            tag poop
            count [2 3]
        }
    }
}
```

---

### `ZodiacsPoncho`
**Name:** Zodiacs Poncho  
**Description:** +1 Range. During your turn, one random enemy has a Bounty.  
**Source:** `neck_items.gon`  

```
ZodiacsPoncho {
    name "ARMOR_ZODIACSPONCHO_NAME"
    desc "ARMOR_ZODIACSPONCHO_DESC"
	rarity rare
	kind neck
	frame 185
	set Rag
    
	passives {
		AddBonusRange 1
		ApplyStatusesToRandomEnemiesEachTurn {
			Bounty 1
		}
	}
}
```

---

### `CoffinArmor`
**Name:** Coffin Armor  
**Description:** +1 Thorns.  
**Source:** `neck_items.gon`  

```
CoffinArmor {
    name "ARMOR_COFFINARMOR_NAME"
    desc "ARMOR_COFFINARMOR_DESC"
	rarity rare
	kind neck
	frame 184
	set Wood

	shield 3
	divine_shield 1

	passives {
		Thorns 1
	}
}
```

---

### `NubsCollar`
**Name:** Nubs Collar  
**Description:** Your movement action is Belly Flop.  
**Source:** `neck_items.gon`  

```
NubsCollar {
    name "ARMOR_NUBSCOLLAR_NAME"
    desc "ARMOR_NUBSCOLLAR_DESC"
	rarity very_rare
	kind neck
	frame 183
	set Leather
	
	passives {
		ReplaceBasicMove BellyFlop_BasicMove
	}
}
```

---

### `ChubsCollar`
**Name:** Chub's Collar  
**Description:** Your basic attack is Spin Attack.  
**Source:** `neck_items.gon`  

```
ChubsCollar {
    name "ARMOR_CHUBSCOLLAR_NAME"
    desc "ARMOR_CHUBSCOLLAR_DESC"
	rarity rare
	kind neck
	frame 182
	set Leather
	
	str 1

    attack BasicSpin

	passives {
		OverrideBasicAttack BasicSpin 
	}
}
```

---

### `Blubber`
**Name:** Blubber  
**Description:** ARMOR_BLUBBER_DESC  
**Source:** `neck_items.gon`  

```
Blubber {
    name "ARMOR_BLUBBER_NAME"
    desc "ARMOR_BLUBBER_DESC"
	rarity rare
	kind neck
	frame 181
	set Fatty
    
	con 7
	spd -5
	cha -2
	
    passives {

    }
}
```

---

### `EtherealRings`
**Name:** Ethereal Rings  
**Description:** Kinetic Spikes 3. Emit 3 Sparkles when you use your basic attack.  
**Source:** `neck_items.gon`  

```
EtherealRings {
    name "ARMOR_ETHEREALRINGS_NAME"
    desc "ARMOR_ETHEREALRINGS_DESC"
	rarity very_rare
	kind neck
	frame 198
	
	shield 3
	
    passives {
		KineticSpikes 3
        AddSelfStatusToBasicAttack {
            RandomMagicMissile 3
        }
    }
}
```

---

### `WhiteRabbitPaw`
**Name:** White Rabbit Paw  
**Description:** ARMOR_WHITERABBITPAW_DESC  
**Source:** `neck_items.gon`  

```
WhiteRabbitPaw {
    name "ARMOR_WHITERABBITPAW_NAME"
    desc "ARMOR_WHITERABBITPAW_DESC"
	rarity very_rare
	kind neck
	frame 197
	set [Lucky, Twine]
	
	lck 5
	
    passives {

    }
}
```

---

### `GlowingPelt`
**Name:** Glowing Pelt  
**Description:** +5 Health Regen.
When you're downed, revive at the end of the round.  
**Source:** `neck_items.gon`  

```
GlowingPelt {
    name "ARMOR_GLOWINGPELT_NAME"
    desc "ARMOR_GLOWINGPELT_DESC"
	rarity very_rare
	kind neck
	frame 196
	
    passives {
		HealthRegenUp 5
        ChanceToRevive 100
    }
}
```

---

### `Polyp`
**Name:** Polyp  
**Description:** +1 Health Regen. 25% chance to spawn a Charmed Clot when you take damage.  
**Source:** `neck_items.gon`  

```
Polyp {
    name "ARMOR_POLYP_NAME"
    desc "ARMOR_POLYP_DESC"
	rarity rare
	kind neck
	frame 195
	set [Meat, HumanFlesh]
	
	passives {
		HealthRegenUp 1
		SpawnThingOnDamage {
			object CharmedClot
			number 1
			chance .25
		}
	}
}
```

---

### `RoboArm`
**Name:** Robo Arm  
**Description:** Start with +1 bonus attack. Collect all adjacent pickups when you end your turn.  
**Source:** `neck_items.gon`  

```
RoboArm {
    name "ARMOR_ROBOARM_NAME"
    desc "ARMOR_ROBOARM_DESC"
	rarity rare
	kind neck
	frame 194
	set [Bionic, Cyborg]
	
    passives {
        Metal 1
		Quivered 1
        StatusEachTurnEnd {
            ForceUseAbility tk_RoboSucc
        }
    }
}
```

---

### `Brambles`
**Name:** Brambles  
**Description:** +1 Thorns. Spawn brambles in adjacent tiles when you end your turn.
You are immune to tile effects.  
**Source:** `neck_items.gon`  

```
Brambles {
    name "ARMOR_BRAMBLES_NAME"
    desc "ARMOR_BRAMBLES_DESC"
	rarity very_rare
	kind neck
	frame 193
	set Leafy
	
	passives {
		Thorns 1
		IgnoreTiles 1
        StatusEachTurnEnd {
            ForceUseAbility neck_Brambles
        }
    }
}
```

---

### `CrustySock`
**Name:** Crusty Sock  
**Description:** Spawn a Gamete familiar at the start of each battle.  
**Source:** `neck_items.gon`  

```
CrustySock {
    name "ARMOR_CRUSTYSOCK_NAME"
    desc "ARMOR_CRUSTYSOCK_DESC"
	rarity rare
	kind neck
	frame 192
	set Used
	
	passives {
		SpawnOnBattleStart CharmedGamete
	}
}
```

---

### `Tombstone`
**Name:** Tombstone  
**Description:** Your basic attack has +2 Knockback and a +10% chance to Stun.  
**Source:** `neck_items.gon`  

```
Tombstone {
    name "ARMOR_TOMBSTONE_NAME"
    desc "ARMOR_TOMBSTONE_DESC"
	rarity rare
	kind neck
	frame 191
	set Rock
	
	shield 6
	spd -2
	
	passives {
		AddStatusToBasicAttack {
			Knockback 2
            Stun [1, .1]
		}
	}
}
```

---

### `BrokenWindow`
**Name:** Broken Window  
**Description:** +3 Bleed Thorns. Bleed 1.  
**Source:** `neck_items.gon`  

```
BrokenWindow {
    name "ARMOR_BROKENWINDOW_NAME"
    desc "ARMOR_BROKENWINDOW_DESC"
	rarity rare
	kind neck
	frame 190
	set Wood
	
    passives {
		BleedThorns 3
		Bleed 1
		//CounterAttack wp_BagOfGlass
    }
}
```

---

### `PyrophinasToenail`
**Name:** Pyrophina's Toenail  
**Description:** Fire Immunity.  
**Source:** `neck_items.gon`  

```
PyrophinasToenail {
    name "ARMOR_PYROPHINASTOENAIL_NAME"
    desc "ARMOR_PYROPHINASTOENAIL_DESC"
	rarity very_rare
	kind neck
	frame 146
	
	shield 8
	
    passives {
		ElementImmune Fire
        StatusImmunity [Burn]
    }
}
```

---

### `ZaratanaTurd`
**Name:** Zaratana's Turd  
**Description:** Knockback immunity.  
**Source:** `neck_items.gon`  

```
ZaratanaTurd {
    name "ARMOR_ZARATANATURD_NAME"
    desc "ARMOR_ZARATANATURD_DESC"
	rarity very_rare
	kind neck
	frame 147
	set [Fecal, Rock]
	
	shield 8
	
    passives {
		KnockbackImmunity 1
    }
}
```

---

### `StevensGobbler`
**Name:** Steven's Gobbler  
**Description:** Units that contact you get knocked back. Knockback you deal is increased by 10 and inflicts Bruise 1.  
**Source:** `neck_items.gon`  

```
StevensGobbler {
    name "ARMOR_STEVENSGOBBLER_NAME"
    desc "ARMOR_STEVENSGOBBLER_DESC"
	rarity very_rare
	kind neck
	frame 142
	set Steven
	
    con 6
    spd -99

	passives {
		MeleeRevengeDamage {
		    knockback 1
        }
		AmplifyKnockback 10
		AddStatusToKnockbackDamage {
			Bruise 1
		}
	}
}
```

---

### `StevensFriend`
**Name:** Steven's Friend  
**Description:** Each time you cast a spell, spawn a Shadow copy of yourself that mimics your basic attack and fades at the end of your turn.  
**Source:** `neck_items.gon`  

```
StevensFriend {
    name "ARMOR_STEVENSFRIEND_NAME"
    desc "ARMOR_STEVENSFRIEND_DESC"
	rarity very_rare
	kind neck
	frame 143
	set Steven
	
	
	passives {
		StatusAfterCastSpell {
			UseAbility neck_DarkFriend
		}
	}
}
```

---

### `StevenNeck1`
**Name:** Steven  
**Description:** Your Holy Element spells cost -1 mana.  
**Source:** `neck_items.gon`  

```
StevenNeck1 {
    name "ARMOR_STEVENNECK1_NAME"
    desc "ARMOR_STEVENNECK1_DESC"
	rarity very_rare
	kind neck
	frame 144
	set Steven
	
    passives {
        ElementalManaCostReduction {
            element [Holy]
            reduction 1
        }
    }
}
```

---

### `StevenNeck2`
**Name:** Steven  
**Description:** While you're downed, receiving any damage revives you.  
**Source:** `neck_items.gon`  

```
StevenNeck2 {
    name "ARMOR_STEVENNECK2_NAME"
    desc "ARMOR_STEVENNECK2_DESC"
	rarity very_rare
	kind neck
	frame 145
	set Steven
	
    passives {
        StevenBolts 1
    }
}
```

---

### `AFriendsFoot`
**Name:** A Friends Foot  
**Description:** Gain +1 [img:lck] when you get a kill.  
**Source:** `neck_items.gon`  

```
AFriendsFoot {
    name "ARMOR_AFRIENDSFOOT_NAME"
    desc "ARMOR_AFRIENDSFOOT_DESC"
	rarity very_rare
	kind neck
	frame 200
	set HumanFlesh
	
	lck 1
	
    passives {
		StatusOnKillEnemy {
			LuckUp 1
		}
    }
}
```

---

## File: `parasites.gon`

### `Tapeworm`
**Name:** Tapeworm  
**Description:** Your basic attack inflicts Poison 1.  
**Source:** `parasites.gon`  

```
Tapeworm {
    name "PARASITE_TAPEWORM_NAME"
    desc "PARASITE_TAPEWORM_DESC"
    kind trinket
    frame 12
    cursed true
    parasite true
    con -2

    passives {
        AddStatusToBasicAttack {
            Poison 1
        }
    }
}
```

---

### `Pinworm`
**Name:** Pinworm  
**Description:** Spawns a Maggot familiar when you take damage.  
**Source:** `parasites.gon`  

```
Pinworm {
    name "PARASITE_PINWORM_NAME"
    desc "PARASITE_PINWORM_DESC"
    kind neck
    frame 15
    cursed true
    parasite true
	set Parasite

    con -1
    str -1

    passives {
        SpawnThingOnDamage {
            object CharmedMaggot
            good false //good relative to the thing attacking, for luck calculations
        }
    }
}
```

---

### `Ringworm`
**Name:** Ringworm  
**Description:** Your basic attack inflicts Weakness 3.  
**Source:** `parasites.gon`  

```
Ringworm {
    name "PARASITE_RINGWORM_NAME"
    desc "PARASITE_RINGWORM_DESC"
    kind face
    frame 20
    cursed true
    parasite true
	set Parasite

    cha -3

    passives {
        AddStatusToBasicAttack {
            Weakness 3
        }
    }
}
```

---

### `Heartworm`
**Name:** Heartworm  
**Description:** When downed, your body is destroyed.  
**Source:** `parasites.gon`  

```
Heartworm {
    name "PARASITE_HEARTWORM_NAME"
    desc "PARASITE_HEARTWORM_DESC"
    kind trinket
    frame 14
    cursed true
    parasite true

    durability 1

    lck 3

    passives {
        AddCorpseHealth -999999
    }
}
```

---

### `BotflyLarva`
**Name:** Botfly Larva  
**Description:** Spawns 2 Pooter familiars when you're downed.  
**Source:** `parasites.gon`  

```
BotflyLarva {
    name "PARASITE_BOTFLYLARVA_NAME"
    desc "PARASITE_BOTFLYLARVA_DESC"
    kind trinket
    frame 13
    cursed true
    parasite true

    spd -1
    cha -1

    passives {
        SpawnThingOnDeath CharmedPooter
        SpawnThingOnDeath CharmedPooter
    }
}
```

---

### `BrainMaggot`
**Name:** Brain Maggot  
**Description:** Revive with 50% HP 2 rounds after you are downed.  
**Source:** `parasites.gon`  

```
BrainMaggot {
    name "PARASITE_BRAINMAGGOT_NAME"
    desc "PARASITE_BRAINMAGGOT_DESC"
    kind head
    frame 16
    cursed true
    parasite true
	set Parasite

    int -3

    passives {
        DelayedAutoRevive {
            rounds 2
            health 50%
        }
    }
}
```

---

### `SpiderEgg`
**Name:** Spider Egg  
**Description:** Your basic attack inflicts Infested.  
**Source:** `parasites.gon`  

```
SpiderEgg {
    name "PARASITE_SPIDEREGG_NAME"
    desc "PARASITE_SPIDEREGG_DESC"
    kind trinket
    frame 98
    cursed true
    parasite true

    passives {
        AddStatusToBasicAttack {
            SpiderInfested 1
        }
    }
}
```

---

### `SpiderWebber`
**Name:** Spider Webber  
**Description:** Use: A ranged attack that inflicts Webbed.  
**Source:** `parasites.gon`  

```
SpiderWebber {
    name "PARASITE_SPIDERWEBBER_NAME"
    desc "PARASITE_SPIDERWEBBER_DESC"
    kind weapon
    frame 159
    cursed true
    parasite true

    ability wp_SpiderWebber
}
```

---

### `AmoebaHat`
**Name:** Amoeba  
**Description:** +1 Brace. +10% Miss Chance.  
**Source:** `parasites.gon`  

```
AmoebaHat {
    name "PARASITE_AMOEBAHEAD_NAME"
    desc "PARASITE_AMOEBAHEAD_DESC"
    kind head
    frame 100
    set Amoeba
    cursed true
    parasite true
    
    shield 4
    int -1

    passives {
        Brace 1
		MissChance 10
    }
}
```

---

### `AmoebaNeck`
**Name:** Amoeba  
**Description:** +1 Brace. +10% Miss Chance.  
**Source:** `parasites.gon`  

```
AmoebaNeck {
    name "PARASITE_AMOEBANECK_NAME"
    desc "PARASITE_AMOEBANECK_DESC"
    kind neck
    frame 100
    set Amoeba
    cursed true
    parasite true

	shield 4
    con -1

    passives {
        Brace 1
		MissChance 10
    }
}
```

---

### `AmoebaFace`
**Name:** Amoeba  
**Description:** +1 Brace. +10% Miss Chance.  
**Source:** `parasites.gon`  

```
AmoebaFace {
    name "PARASITE_AMOEBAFACE_NAME"
    desc "PARASITE_AMOEBAFACE_DESC"
    kind face
    frame 100
    set Amoeba
    cursed true
    parasite true

	shield 4
	cha -1

    passives {
        Brace 1
        MissChance 10
    }
}
```

---

### `SoulSucker`
**Name:** Soul Sucker  
**Description:** Restore 2 mana when you kill an enemy.  
**Source:** `parasites.gon`  

```
SoulSucker {
    name "ARMOR_SOULSUCKER_NAME"
    desc "ARMOR_SOULSUCKER_DESC"
    kind face
    frame 58
    cursed true
    parasite true
	set Parasite

    con -1

    passives {
        StatusOnKillEnemy {
            ManaGain 2
        }
    }
}
```

---

### `BestBud`
**Name:** Best Bud  
**Description:** 10% chance to break when you take damage.
When this breaks, gain a permanent Leech familiar.  
**Source:** `parasites.gon`  

```
BestBud {
    name "ARMOR_BESTBUD_NAME"
    desc "ARMOR_BESTBUD_DESC"
    kind head
    frame 51
    cursed true
    parasite true
	set Parasite

    con -1

    passives {
        ArmorBreakOnHit {
            durability_loss 0
            chance_to_break 10%
        }
        StatusOnBreak {
            ObjectOnHitCharacter BestBud
        }
    }
}
```

---

### `AngryWorm`
**Name:** Angry Worm  
**Description:** Your basic attack hits an extra time for 1 damage.  
**Source:** `parasites.gon`  

```
AngryWorm {
    name "ARMOR_ANGRYWORM_NAME"
    desc "ARMOR_ANGRYWORM_DESC"
    kind head
    frame 52
    cursed true
    parasite true
	set Parasite

    con -1

    passives {
        AddTemporaryEffectsToBasicAttack {
            CastAgainWithStatus {
                stacks 1
                OverrideDamage 1
            }
        }
    }
}
```

---

### `HealWorm`
**Name:** Heal Worm  
**Description:** +2 Health Regen.  
**Source:** `parasites.gon`  

```
HealWorm {
    name "ARMOR_HEALWORM_NAME"
    desc "ARMOR_HEALWORM_DESC"
    kind neck
    frame 49
    cursed true
    parasite true
	set Parasite

    con -1

    passives {
        HealthRegenUp 2
    }
}
```

---

### `CymothoaExigua`
**Name:** Cymothoa Exigua  
**Description:** ARMOR_CYMOTHOAEXIGUA_DESC  
**Source:** `parasites.gon`  

```
CymothoaExigua {
    name "ARMOR_CYMOTHOAEXIGUA_NAME"
    desc "ARMOR_CYMOTHOAEXIGUA_DESC"
    kind face
    frame 43
    cursed true
    parasite true
	set Parasite

    cha -2
    str 2
    dex 2

    passives {
    }
}
```

---

### `EyeWorm`
**Name:** Eye Worm  
**Description:** +10% Miss Chance. 75% chance to equip a piece of Grub armor at the start of each battle.
This will destroy any armor it replaces.  
**Source:** `parasites.gon`  

```
EyeWorm {
    name "ARMOR_EYEWORM_NAME"
    desc "ARMOR_EYEWORM_DESC"
    kind face
    frame 44
    cursed true
    parasite true
	set Parasite

    passives {
        MissChance 10

        StatusOnBattleStart {
            DestroyEquipmentAndAttachParasite {
                chance .75
                pool [FaceGrub HeadGrub NeckGrub]
            }
        }
    }
}
```

---

### `Scabies`
**Name:** Scabies  
**Description:** Bruise 2. Spawn a charmed Flea when you take damage.  
**Source:** `parasites.gon`  

```
Scabies {
    name "ARMOR_SCABIES_NAME"
    desc "ARMOR_SCABIES_DESC"
    kind face
    frame 45
    cursed true
    parasite true
	set Parasite

    passives {
        Bruise 2
        SpawnThingOnDamage {
            object CharmedFlea
            spawn_on_death_hit false
        }
    }
}
```

---

### `BeanParasite`
**Name:** Bean Parasite  
**Description:** Confusion 99.  
**Source:** `parasites.gon`  

```
BeanParasite {
    name "ARMOR_BEANPARASITE_NAME"
    desc "ARMOR_BEANPARASITE_DESC"
    kind head
    frame 67
    cursed true
    parasite true
	set Parasite

    int 5

    passives {
        Confusion 99
    }
}
```

---

### `Cordyceps`
**Name:** Cordyceps  
**Description:** 30% chance to gain +2 [img:spd] and become AI controlled at the start of your turn.  
**Source:** `parasites.gon`  

```
Cordyceps {
    name "ARMOR_CORDYCEPS_NAME"
    desc "ARMOR_CORDYCEPS_DESC"
    kind head
    frame 36
    cursed true
    parasite true
	set Parasite

    passives {
        StatusEachTurnBegin {
            Conditional_BadRoll {
                odds .3

                Temporary {
                    status SpeedUp
                    stacks 2
                    turns 1
                    expires_on_end_turn true
                }
                Temporary {
                    status Uncontrollable
                    stacks 1
                    turns 1
                    expires_on_end_turn true
                }
            }
        }
    }
}
```

---

### `NaegleriaFowleri`
**Name:** Naegleria Fowleri  
**Description:** Brace {aux}.
Gain -1 [img:int] at the end of each battle, permanently.
This gains +2 [img:shield] and +1 Brace at the end of each battle. 
If your [img:int] is 0 or less, you are uncontrollable.  
**Source:** `parasites.gon`  

```
NaegleriaFowleri {
    name "ARMOR_NAEGLERIAFOWLERI_NAME"
    desc "ARMOR_NAEGLERIAFOWLERI_DESC"
    kind head
    frame 37
    cursed true
    parasite true
	set Parasite

    // kinda convenient that this gives Brace equal to aux
    // might need to implement tooltip_values for items later
    aux 1

    shield "max((aux-1)*2, 0)"

    passives {
        StatusOnBattleStart {
            Brace item_aux
        }
        StatusOnBattleEnd {
            PermanentIntelligence -1
            SetItemAux {
                slot head
                value item_aux+1
            }
            even_if_dead true
        }
        CatPartsSizeScale {
            head 1.3
        }
        
        PassiveAtStatThreshold {
            mode less_or_equal
            threshold {
                int 0
            }
            passives {
				Uncontrollable 1
            }
        }
    }
}
```

---

### `Malaria`
**Name:** Malaria  
**Description:** At the end of each battle, all your [img:con] is permanently reduced by 1.
Spawn 2 Charmed Fly Swarms when you're downed.
If your [img:con] is 0 or less, start each battle downed.  
**Source:** `parasites.gon`  

```
Malaria {
    name "ARMOR_MALARIA_NAME"
    desc "ARMOR_MALARIA_DESC"
    kind head
    frame 38
    cursed true
    parasite true
	set Parasite

    passives {
		SpawnThingOnDeath CharmedFlySwarm
		SpawnThingOnDeath CharmedFlySwarm
        StatusOnBattleEnd {
            PermanentConstitution -1
            even_if_dead true
        }
        
        PassiveAtStatThreshold {
            mode less_or_equal
            threshold {
                con 0
            }
            passives {
                StatusOnBattleStart {
                    SafeDie 1
                }
            }
        }
    }
}
```

---

### `TheTick`
**Name:** The Tick  
**Description:** Inflict All Stats Down on bosses and minibosses at the start of each battle.
Heal +12 HP at the end of each battle.  
**Source:** `parasites.gon`  

```
TheTick {
    name "ARMOR_THETICK_NAME"
    desc "ARMOR_THETICK_DESC"
    rarity uncommon
    kind neck
    frame 96
    cursed true
    parasite true
	set Parasite

    con -1

    passives {
        AddEndOfCombatRegen 12
        StatusAllCharactersOnSpawn {
            Conditional_Boss {
                AllStatsUp -1
            }
        }
    }
}
```

---

### `Parousworm`
**Name:** Parous Worm  
**Description:** 66% chance to find a random parasite at the end of each battle.  
**Source:** `parasites.gon`  

```
Parousworm {
    name "ITEM_PAROUSWORM_NAME"
    desc "ITEM_PAROUSWORM_DESC"
    kind trinket
    frame 271
    cursed true
    parasite true
	//set Worm
    con -1

    passives {
        StatusOnBattleEnd {
            Conditional_GoodRoll {
                odds 66%
                FindItemFromPool parasites
			}
        }
    }
}
```

---

### `Hookworm`
**Name:** Hookworm  
**Description:** Spawn a Charmed Leech when you take damage.  
**Source:** `parasites.gon`  

```
Hookworm {
    name "ARMOR_HOOKWORM_NAME"
    desc "ARMOR_HOOKWORM_DESC"
    kind neck
    frame 188
    cursed true
    parasite true
	
	con -1
	spd -1

	passives {
        SpawnThingOnDamage {
            object CharmedLeech
        }
	}
}
```

---

### `Cooties`
**Name:** Cooties  
**Description:** Your basic attack inflicts Weakness, Rot and Infested.  
**Source:** `parasites.gon`  

```
Cooties {
    name "ARMOR_COOTIES_NAME"
    desc "ARMOR_COOTIES_DESC"
    kind neck
    frame 189
    cursed true
    parasite true
	
	con -1
	str -1
	dex -1
	lck -1
	int -1
    spd -1
	cha -1

    passives {
		AddStatusToBasicAttack {
            Weakness 1
			Rot 1
			SpiderInfested 1
        }
    }
}
```

---

### `Lice`
**Name:** Lice  
**Description:** Bruise 1. Spawn a charmed Louse when you take damage.  
**Source:** `parasites.gon`  

```
Lice {
    name "ARMOR_LICE_NAME"
    desc "ARMOR_LICE_DESC"
    kind head
    frame 218
    cursed true
    parasite true

	passives {
		Bruise 1
        SpawnThingOnDamage {
            object CharmedLice
        }
	}
}
```

---

### `SacculinaCarcini`
**Name:** Sacculina Carcini  
**Description:** ARMOR_SACCULINACARCINI_DESC  
**Source:** `parasites.gon`  

```
SacculinaCarcini {
    name "ARMOR_SACCULINACARCINI_NAME"
    desc "ARMOR_SACCULINACARCINI_DESC"
    kind face
    frame 197
    cursed true
    parasite true

	spd -1
	shield 5

    passives {

    }
}
```

---

### `Roundworm`
**Name:** Roundworm  
**Description:** Units that contact you get knocked back 5 tiles.  
**Source:** `parasites.gon`  

```
Roundworm {
    name "ITEM_ROUNDWORM_NAME"
    desc "ITEM_ROUNDWORM_DESC"
    kind trinket
    frame 283
    cursed true
    parasite true

	con -1

    passives {
        MeleeRevengeDamage {
            knockback 5
        }
    }
}
```

---

### `EuhaplorchisCaliforniensis`
**Name:** Euhaplorchis Californiensis  
**Description:** Start with Confusion 3.  
**Source:** `parasites.gon`  

```
EuhaplorchisCaliforniensis {
    name "ITEM_EUHAPLORCHISCALIFORNIENSIS_NAME"
    desc "ITEM_EUHAPLORCHISCALIFORNIENSIS_DESC"
    kind trinket
    frame 282
    cursed true
    parasite true
	
	spd 4

    passives {
		Confusion 3
    }
}
```

---

### `Beepis`
**Name:** Beepis  
**Description:** Your passives are duplicated during battle.
Your spells cost +2 mana and can only be used once per turn.  
**Source:** `parasites.gon`  

```
Beepis { 
    name "ARMOR_BEEPIS_NAME"
    desc "ARMOR_BEEPIS_DESC"
    kind head
    frame 224
    cursed true
    parasite true

    passives {
        ManaCostReduction -2
        AllSpellsCostCharge 1
        CopyPassiveSlot 0
        CopyPassiveSlot 1
    }
}
```

---

### `Feebis`
**Name:** Feebis  
**Description:** Your spells cost -2 mana and the first one you cast each turn is double cast.
Your basic attack is Poke and your movement range is 1.  
**Source:** `parasites.gon`  

```
Feebis { 
    name "ARMOR_FEEBIS_NAME"
    desc "ARMOR_FEEBIS_DESC"
    kind face
    frame 204
    cursed true
    parasite true

    attack BasicPoke
    passives {
        ManaCostReduction 2
        StatusEachTurnBegin {
            DoubleCastSpellThisTurn 1
        }
        CapMovementAbilityRange 1
        MoveSpeedMultiplier .5
        ReplaceBasicAttack BasicPoke
    }
}
```

---

### `Cunch`
**Name:** Cunch  
**Description:** You can use your basic attack and movement action an extra time each turn.
Your passives are disabled during battle.  
**Source:** `parasites.gon`  

```
Cunch {
    name "ARMOR_CUNCH_NAME"
    desc "ARMOR_CUNCH_DESC"
    kind neck
    frame 199
    cursed true
    parasite true

    passives {
        ExtraBasicAttacks_Status 1
        ExtraBasicMoves_Status 1
        DisablePassiveSlot 0
        DisablePassiveSlot 1
    }
}
```

---

## File: `special_class_items.gon`

### `MonkFist`
**Name:** Monk Fist  
**Description:** Use: another basic attack! (innate, can't be removed or replaced)  
**Source:** `special_class_items.gon`  

**Localization Strings:**
- `ITEM_MONKFIST_DESC`: "You can use your basic attack an extra time each turn. <br/> Innate"

```
MonkFist {
    name "ITEM_MONKFIST_NAME"
    // desc "Use: another basic attack! (innate, can't be removed or replaced)"
    desc "ITEM_MONKFIST_DESC"
    kind weapon
    frame 71
    
    sticky true
    fragile true
    indestructible true
    
    //ability wp_MonkFist
    passives {
        ExtraBasicAttacks 1
    }
}
```

---

### `MonkStyleChanger`
**Name:** Stance Switcher  
**Description:** Use: Switch between melee and ranged stances.
You have Brace 1 while in melee stance.
Innate  
**Source:** `special_class_items.gon`  

```
MonkStyleChanger {
    name "ITEM_STANCESWITCHER_NAME"
    desc "ITEM_STANCESWITCHER_DESC"
    kind trinket
    frame 80

    sticky true
    fragile true
    indestructible true
    
    ability tk_MonkStyleChange

    passives {
        PassiveWhileInMonkMeleeStance {
            Brace 1
        }
    }
}
```

---

### `ButcherHook`
**Name:** Meat Hook  
**Description:** Use: Pull a unit toward you.
Innate  
**Source:** `special_class_items.gon`  

```
ButcherHook {
    name "ITEM_MEATHOOK_NAME"
    desc "ITEM_MEATHOOK_DESC"
    kind weapon
    frame 6

    sticky true
    fragile true
    indestructible true
    
    ability wp_MeatHookB
}
```

---

### `ButcherHook_Temporary`
**Name:** Meat Hook  
**Description:** Use: Pull a unit toward you.  
**Source:** `special_class_items.gon`  

```
ButcherHook_Temporary {
    name "ITEM_MEATHOOK_NAME"
    desc "ITEM_MEATHOOKTEMP_DESC"
    kind weapon
    frame 6
    
    ability wp_MeatHookB
}
```

---

### `Necro_SoulDagger_Uncharged`
**Name:** Soul Dagger  
**Description:** Use: A melee attack. If this weapon damages an allied cat, gain one of their spells at random in your bonus ability slot.
If this weapon downs an ally it becomes Charged for the rest of the battle.  
**Source:** `special_class_items.gon`  

```
Necro_SoulDagger_Uncharged {
    name "ITEM_SOULDAGGER_NAME"
    desc "ITEM_SOULDAGGER_DESC"
    kind weapon
    frame 118
    
    ability wp_NecroSoulDagger
}
```

---

### `Necro_SoulDagger_Charged`
**Name:** Charged Soul Dagger  
**Description:** Use: A melee attack with Lifesteal. If this weapon damages an allied cat, gain one of their spells at random in your bonus ability slot.
Loses its charge at the end of the battle.  
**Source:** `special_class_items.gon`  

```
Necro_SoulDagger_Charged {
    name "ITEM_SOULDAGGERCHARGED_NAME"
    desc "ITEM_SOULDAGGERCHARGED_DESC"
    kind weapon
    frame 119

    passives {
        StatusOnBattleEnd {
            even_if_dead true
            TransformWeapon {
                from Necro_SoulDagger_Charged
                to Necro_SoulDagger_Uncharged
            }
        }
    }
    
    ability wp_NecroSoulDaggerCharged
}
```

---

### `SleepDart`
**Name:** Sleep Dart  
**Description:** Use: A straight ranged attack that inflicts Sleep 1.  
**Source:** `special_class_items.gon`  

```
SleepDart {
    name "ITEM_SLEEPDART_NAME"
    desc "ITEM_SLEEPDART_DESC"
    kind weapon
    frame 151
    durability 1 
    
    ability wp_SleepDart
}
```

---

### `SleepDart2`
**Name:** Sleep Dart  
**Description:** Use: A straight ranged attack that inflicts Sleep 1.  
**Source:** `special_class_items.gon`  

```
SleepDart2 {
    name "ITEM_SLEEPDART_NAME"
    desc "ITEM_SLEEPDART_DESC"
    kind weapon
    frame 151
    durability 2
    
    ability wp_SleepDart
}
```

---

## File: `trinkets.gon`

### `RatTail`
**Name:** Rat Tail  
**Description:** ITEM_RATTAIL_DESC  
**Source:** `trinkets.gon`  

```
RatTail {
    name "ITEM_RATTAIL_NAME"
    desc "ITEM_RATTAIL_DESC"
    kind trinket
    frame 4
    rarity common
	set Rat

    lck 1
}
```

---

### `RatHeart`
**Name:** Rat Heart  
**Description:** ITEM_RATHEART_DESC  
**Source:** `trinkets.gon`  

```
RatHeart {
    name "ITEM_RATHEART_NAME"
    desc "ITEM_RATHEART_DESC"
    kind trinket
    frame 5
    rarity common
	set [Rat, Guts]

    con 1
}
```

---

### `RatBeezer`
**Name:** Rat Bezoar  
**Description:** Poisonous 1.  
**Source:** `trinkets.gon`  

```
RatBeezer {
    name "ITEM_RATBEZOAR_NAME"
    desc "ITEM_RATBEZOAR_DESC"
    kind trinket
    rarity common
	set Rat

    frame 6

    passives {
        PoisonThorns 1
    }
}
```

---

### `Book`
**Name:** Book  
**Description:** ITEM_BOOK_DESC  
**Source:** `trinkets.gon`  

```
Book {
    name "ITEM_BOOK_NAME"
    desc "ITEM_BOOK_DESC"
    rarity common
    kind trinket
    frame 90
	set Paper

    int 1
}
```

---

### `Dumbell`
**Name:** Dumbbell  
**Description:** ITEM_DUMBELL_DESC  
**Source:** `trinkets.gon`  

```
Dumbell {
    name "ITEM_DUMBELL_NAME"
    desc "ITEM_DUMBELL_DESC"
    rarity common
    kind trinket
    frame 91
	set Lead

    str 1
}
```

---

### `Jazzercise`
**Name:** Jazzercise VHS Tape  
**Description:** ITEM_JAZZERCISEVHSTAPE_DESC  
**Source:** `trinkets.gon`  

```
Jazzercise {
    name "ITEM_JAZZERCISEVHSTAPE_NAME"
    desc "ITEM_JAZZERCISEVHSTAPE_DESC"
    rarity common
    kind trinket
    frame 92

    dex 1
}
```

---

### `OldShoe`
**Name:** Old Shoe  
**Description:** ITEM_OLDSHOE_DESC  
**Source:** `trinkets.gon`  

```
OldShoe {
    name "ITEM_OLDSHOE_NAME"
    desc "ITEM_OLDSHOE_DESC"
    rarity common
    kind trinket
    frame 93
	set [Used, Leather]

    spd 1
}
```

---

### `BodySpray`
**Name:** Body Spray  
**Description:** ITEM_BODYSPRAY_DESC  
**Source:** `trinkets.gon`  

```
BodySpray {
    name "ITEM_BODYSPRAY_NAME"
    desc "ITEM_BODYSPRAY_DESC"
    rarity common
    kind trinket
    frame 94

    cha 1
}
```

---

### `LuckyPenny`
**Name:** Lucky Penny  
**Description:** ITEM_LUCKYPENNY_DESC  
**Source:** `trinkets.gon`  

```
LuckyPenny {
    name "ITEM_LUCKYPENNY_NAME"
    desc "ITEM_LUCKYPENNY_DESC"
    rarity common
    kind trinket
    frame 95
	set Lucky

    lck 1
}
```

---

### `WizCheese`
**Name:** Wiz Cheese  
**Description:** ITEM_WIZCHEESE_DESC  
**Source:** `trinkets.gon`  

```
WizCheese {
    name "ITEM_WIZCHEESE_NAME"
    desc "ITEM_WIZCHEESE_DESC"
    rarity common
    kind trinket
    frame 96

    con 1
}
```

---

### `SnaggleTooth`
**Name:** Snaggle Tooth  
**Description:** Your basic attack inflicts Bleed 1.  
**Source:** `trinkets.gon`  

```
SnaggleTooth {
    name "ITEM_SNAGGLETOOTH_NAME"
    desc "ITEM_SNAGGLETOOTH_DESC"
    rarity rare
    kind trinket
    frame 8
	set Bone

    passives {
        AddStatusToBasicAttack {
            Bleed 1
        }
    }
}
```

---

### `JarOfLeeches`
**Name:** Jar of Leeches  
**Description:** Your basic attack inflicts Leech 1.  
**Source:** `trinkets.gon`  

```
JarOfLeeches {
    name "ITEM_JAROFLEECHES_NAME"
    desc "ITEM_JAROFLEECHES_DESC"
    rarity rare
    kind trinket
    frame 81
	set Leech

    passives {
        AddStatusToBasicAttack {
            Leeches 1
        }
    }
}
```

---

### `BrassKnuckles`
**Name:** Brass Knuckles  
**Description:** Your basic attack inflicts Bruise 1.  
**Source:** `trinkets.gon`  

```
BrassKnuckles {
    name "ITEM_BRASSKNUCKLES_NAME"
    desc "ITEM_BRASSKNUCKLES_DESC"
    rarity rare
    kind trinket
    frame 82
	set Fighter

    passives {
        AddStatusToBasicAttack {
            Bruise 1
        }
    }
}
```

---

### `FlyLarva`
**Name:** Fly Larva  
**Description:** Your basic attack inflicts Rot 1.  
**Source:** `trinkets.gon`  

```
FlyLarva {
    name "ITEM_FLYLARVA_NAME"
    desc "ITEM_FLYLARVA_DESC"
    rarity uncommon
    kind trinket
    frame 83
	set Fly

    passives {
        AddStatusToBasicAttack {
            Rot 1
        }
    }
}
```

---

### `StrangeMarble`
**Name:** Strange Marble  
**Description:** Your basic attack inflicts Mana Leech 1.  
**Source:** `trinkets.gon`  

```
StrangeMarble {
    name "ITEM_STRANGEMARBLE_NAME"
    desc "ITEM_STRANGEMARBLE_DESC"
    rarity uncommon
    kind trinket
    frame 84

    passives {
        AddStatusToBasicAttack {
            ManaLeeches 1
        }
    }
}
```

---

### `VibratingSkull`
**Name:** Vibrating Skull  
**Description:** Your basic attack inflicts Magic Weakness 1.  
**Source:** `trinkets.gon`  

```
VibratingSkull {
    name "ITEM_VIBRATINGSKULL_NAME"
    desc "ITEM_VIBRATINGSKULL_DESC"
    rarity uncommon
    kind trinket
    frame 85
	set [Bone, Space]

    passives {
        AddStatusToBasicAttack {
            MagicWeakness 1
        }
    }
}
```

---

### `BoneMarrow`
**Name:** Bone Marrow  
**Description:** Heal to full at the end of each battle.  
**Source:** `trinkets.gon`  

```
BoneMarrow {
    name "ITEM_BONEMARROW_NAME"
    desc "ITEM_BONEMARROW_DESC"
    rarity rare
    kind trinket
    frame 9
	set [Meat, Bone]

    passives {
        AddEndOfCombatRegen 999999
    }
}
```

---

### `Feather`
**Name:** Feather  
**Description:** Take your turn earlier.  
**Source:** `trinkets.gon`  

```
Feather {
    name "ITEM_FEATHER_NAME"
    desc "ITEM_FEATHER_DESC"
    rarity uncommon
    kind trinket
    frame 31
	set Feathered
	
	spd 1

    passives {
        AddInitiative 100
    }
}
```

---

### `Weight`
**Name:** Weight  
**Description:** Trample. Take your turn later.  
**Source:** `trinkets.gon`  

```
Weight {
    name "ITEM_WEIGHT_NAME"
    desc "ITEM_WEIGHT_DESC"
    rarity uncommon
    kind trinket
    frame 30
	set Lead

    passives {
        AddInitiative -20
		Trample 3
    }
}
```

---

### `MatchStick`
**Name:** Match Stick  
**Description:** Your basic attack inflicts Burn 1.  
**Source:** `trinkets.gon`  

```
MatchStick {
    name "ITEM_MATCHSTICK_NAME"
    desc "ITEM_MATCHSTICK_DESC"
    rarity rare
    kind trinket
    frame 32

    passives {
        AddStatusToBasicAttack {
            Burn 1
        }
    }
}
```

---

### `BeeStinger`
**Name:** Bee Stinger  
**Description:** Your basic attack inflicts Poison 1.  
**Source:** `trinkets.gon`  

```
BeeStinger {
    name "ITEM_BEESTINGER_NAME"
    desc "ITEM_BEESTINGER_DESC"
    rarity rare
    kind trinket
    frame 33

    passives {
        AddStatusToBasicAttack {
            Poison 1
        }
    }
}
```

---

### `PullTab`
**Name:** Pull Tab  
**Description:** ITEM_PULLTAB_DESC  
**Source:** `trinkets.gon`  

```
PullTab {
    name "ITEM_PULLTAB_NAME"
    desc "ITEM_PULLTAB_DESC"
    rarity common
    kind trinket
    frame 15
	set Scrap

    shield 4
}
```

---

### `SelfDestructButton`
**Name:** Self-Destruct Button  
**Description:** Use: Vaporize yourself and deal 50 damage to adjacent units.  
**Source:** `trinkets.gon`  

```
SelfDestructButton {
    name "ITEM_SELFDESTRUCTBUTTON_NAME"
    desc "ITEM_SELFDESTRUCTBUTTON_DESC"
    rarity very_rare
    kind trinket
    frame 42

    ability tr_SelfDestruct
}
```

---

### `EmptySyringe`
**Name:** Empty Syringe  
**Description:** When you inflict Bleed or Poison, inflict +1 Bleed or Poison.  
**Source:** `trinkets.gon`  

```
EmptySyringe {
    name "ITEM_EMPTYSYRINGE_NAME"
    desc "ITEM_EMPTYSYRINGE_DESC"
    rarity rare
    kind trinket
    frame 66
	set Medical

    passives {
        AmplifyStatus Bleed
		AmplifyStatus Poison
    }
}
```

---

### `LiquidNitrogen`
**Name:** Liquid Nitrogen  
**Description:** Your Ice Element damage is increased by 2.  
**Source:** `trinkets.gon`  

```
LiquidNitrogen {
    name "ITEM_LIQUIDNITROGEN_NAME"
    desc "ITEM_LIQUIDNITROGEN_DESC"
    rarity uncommon
    kind trinket
    frame 60
	set Frozen

    passives {
        AddDamageToElementDamage {
            element Ice
            damage 2
        }
    }
}
```

---

### `Ember`
**Name:** Ember  
**Description:** Your Fire Element damage is increased by 1 and inflicts +1 Burn.  
**Source:** `trinkets.gon`  

```
Ember {
    name "ITEM_EMBER_NAME"
    desc "ITEM_EMBER_DESC"
    rarity uncommon
    kind trinket
    frame 61
	set Molten

    passives {
        AddStatusToElementDamage {
            element Fire
            Burn 1
        }
        AddDamageToElementDamage {
            element Fire
            damage 1
        }
    }
}
```

---

### `Conductor`
**Name:** Conductor  
**Description:** Your Electric Element damage is increased by 1 and has +10% chance to Stun.  
**Source:** `trinkets.gon`  

```
Conductor {
    name "ITEM_CONDUCTOR_NAME"
    desc "ITEM_CONDUCTOR_DESC"
    rarity uncommon
    kind trinket
    frame 62

    passives {
        AddStatusToElementDamage {
            element Electric
            Stun [1 .1]
        }
        AddDamageToElementDamage {
            element Electric
            damage 1
        }
    }
}
```

---

### `FeedBag`
**Name:** Feed Bag  
**Description:** Familiars you spawn gain +2 max HP.  
**Source:** `trinkets.gon`  

```
FeedBag {
    name "ITEM_FEEDBAG_NAME"
    desc "ITEM_FEEDBAG_DESC"
    rarity uncommon
    kind trinket
    frame 64
	set [Druid, Hunter]

    passives {
        AddPassivesToMinions {
            AddMaxHealth 2
            HealthGain 2 //fill up the blank max health
        }
    }
}
```

---

### `Nightshade`
**Name:** Nightshade  
**Description:** When you inflict Poison, inflict +2 Poison.
Start with Poison 2.  
**Source:** `trinkets.gon`  

```
Nightshade {
    name "ITEM_NIGHTSHADE_NAME"
    desc "ITEM_NIGHTSHADE_DESC"
    rarity rare
    kind trinket
    frame 63
	set Flower


    passives {
	    Poison 2
        AmplifyStatus Poison
		AmplifyStatus Poison
    }
}
```

---

### `Neverstone`
**Name:** Neverstone  
**Description:** Never level up.  
**Source:** `trinkets.gon`  

```
Neverstone {
    name "ITEM_NEVERSTONE_NAME"
    desc "ITEM_NEVERSTONE_DESC"
    rarity rare
    kind trinket
    frame 97
	set [Rock, Gemstone]

    prevent_level_up true
}
```

---

### `Pawn`
**Name:** Pawn  
**Description:** Use: Move 1 tile toward the closest enemy.  
**Source:** `trinkets.gon`  

```
Pawn {
    name "ITEM_PAWN_NAME"
    desc "ITEM_PAWN_DESC"
    rarity common
    kind trinket
    frame 35

    durability 10

    ability tk_Pawn
}
```

---

### `Knight`
**Name:** Knight  
**Description:** Use: Jump in an L shape.  
**Source:** `trinkets.gon`  

```
Knight {
    name "ITEM_KNIGHT_NAME"
    desc "ITEM_KNIGHT_DESC"
    rarity uncommon
    kind trinket
    frame 114

    durability 6

    ability tk_Knight
}
```

---

### `Rook`
**Name:** Rook  
**Description:** Use: Move any number of tiles in a straight line.  
**Source:** `trinkets.gon`  

```
Rook {
    name "ITEM_ROOK_NAME"
    desc "ITEM_ROOK_DESC"
    rarity rare
    kind trinket
    frame 36

    durability 6

    ability tk_Rook
}
```

---

### `Queen`
**Name:** Queen  
**Description:** Use: Move any number of tiles in a straight or diagonal line.  
**Source:** `trinkets.gon`  

```
Queen {
    name "ITEM_QUEEN_NAME"
    desc "ITEM_QUEEN_DESC"
    rarity very_rare
    kind trinket
    frame 37

    durability 8

    ability tk_Queen
}
```

---

### `PetrifiedPoop`
**Name:** Petrified Poop  
**Description:** Familiars you spawn gain +2 [img:shield].  
**Source:** `trinkets.gon`  

```
PetrifiedPoop {
    name "ITEM_PETRIFIEDPOOP_NAME"
    desc "ITEM_PETRIFIEDPOOP_DESC"
    rarity uncommon
    kind trinket
    frame 45
	set [Rock, Fecal]

    shield 2
	
	passives {
        AddPassivesToMinions {
            Shield 2
        }
    }
}
```

---

### `FishHook`
**Name:** Fish Hook  
**Description:** If you would knockback a unit, instead deal extra damage to it equal to the knockback.  
**Source:** `trinkets.gon`  

```
FishHook {
    name "ITEM_FISHHOOK_NAME"
    desc "ITEM_FISHHOOK_DESC"
    rarity uncommon
    kind trinket
    frame 55
	set Barbed

    passives {
        StripKnockback 1
    }
}
```

---

### `HumanHand`
**Name:** Human Hand  
**Description:** ITEM_HUMANHAND_DESC  
**Source:** `trinkets.gon`  

```
HumanHand {
    name "ITEM_HUMANHAND_NAME"
    desc "ITEM_HUMANHAND_DESC"
    rarity uncommon
    kind trinket
    frame 105
	set HumanFlesh

    str 2
}
```

---

### `HumanBrain`
**Name:** Human Brain  
**Description:** ITEM_HUMANBRAIN_DESC  
**Source:** `trinkets.gon`  

```
HumanBrain {
    name "ITEM_HUMANBRAIN_NAME"
    desc "ITEM_HUMANBRAIN_DESC"
    rarity uncommon
    kind trinket
    frame 106
	set [HumanFlesh, Guts]

    int 2
}
```

---

### `HumanLeg`
**Name:** Human Leg Bone  
**Description:** ITEM_HUMANLEGBONE_DESC  
**Source:** `trinkets.gon`  

```
HumanLeg {
    name "ITEM_HUMANLEGBONE_NAME"
    desc "ITEM_HUMANLEGBONE_DESC"
    rarity uncommon
    kind trinket
    frame 107
	set Bone

    dex 2
}
```

---

### `HumanToe`
**Name:** Human Toe  
**Description:** ITEM_HUMANTOE_DESC  
**Source:** `trinkets.gon`  

```
HumanToe {
    name "ITEM_HUMANTOE_NAME"
    desc "ITEM_HUMANTOE_DESC"
    rarity uncommon
    kind trinket
    frame 108
	set HumanFlesh

    lck 2
}
```

---

### `HumanHeart`
**Name:** Human Heart  
**Description:** ITEM_HUMANHEART_DESC  
**Source:** `trinkets.gon`  

```
HumanHeart {
    name "ITEM_HUMANHEART_NAME"
    desc "ITEM_HUMANHEART_DESC"
    rarity uncommon
    kind trinket
    frame 109
	set [HumanFlesh, Guts]

    con 2
}
```

---

### `HumanFoot`
**Name:** Human Foot  
**Description:** ITEM_HUMANFOOT_DESC  
**Source:** `trinkets.gon`  

```
HumanFoot {
    name "ITEM_HUMANFOOT_NAME"
    desc "ITEM_HUMANFOOT_DESC"
    rarity uncommon
    kind trinket
    frame 110
	set HumanFlesh

    spd 2
}
```

---

### `MysteriousEye`
**Name:** Human Eye  
**Description:** ITEM_HUMANEYE_DESC  
**Source:** `trinkets.gon`  

```
MysteriousEye {
    name "ITEM_HUMANEYE_NAME"
    desc "ITEM_HUMANEYE_DESC"
    rarity uncommon
    kind trinket
    frame 20
	set [HumanFlesh, Guts]

    cha 2
}
```

---

### `D6`
**Name:** D6  
**Description:** You can reroll your options when you level up.  
**Source:** `trinkets.gon`  

```
D6 {
    name "ITEM_D6_NAME"
    desc "ITEM_D6_DESC"
    rarity common
    kind trinket
    frame 89

    passives {
        AddLevelUpRerolls 1
    }
}
```

---

### `MetalSquare`
**Name:** Metal Plate  
**Description:** Gain +1 Brace when you kill an enemy.  
**Source:** `trinkets.gon`  

```
MetalSquare {
    name "ITEM_METALPLATE_NAME"
    desc "ITEM_METALPLATE_DESC"
    rarity uncommon
    kind trinket
    frame 86
	set Scrap

    passives {
        StatusOnKillEnemy {
            Brace 1
        }
    }
}
```

---

### `BlinkingEyeball`
**Name:** Blinking Eyeball  
**Description:** Your line of sight restrictions are ignored.  
**Source:** `trinkets.gon`  

```
BlinkingEyeball {
    name "ITEM_BLINKINGEYEBALL_NAME"
    desc "ITEM_BLINKINGEYEBALL_DESC"
    kind trinket
    frame 10
	set Guts

    passives {
        RemoveLineOfSightRestrictions 1
    }
}
```

---

### `GoldenTooth`
**Name:** Golden Tooth  
**Description:** Becomes {aux} coins when you return home.  
**Source:** `trinkets.gon`  

```
GoldenTooth {
    name "ITEM_GOLDENTOOTH_NAME"
    desc "ITEM_GOLDENTOOTH_DESC"
    kind trinket
    frame 11

    lck 4

    on_store become_aux_coins
    aux 125
}
```

---

### `WaterBottle_Full`
**Name:** Water Bottle  
**Description:** Use: Heal +5 HP and gain Heatwave immunity.
Refills when affected by Water Element effects.  
**Source:** `trinkets.gon`  

```
WaterBottle_Full {
    name "ITEM_WATERBOTTLEFULL_NAME"
    desc "ITEM_WATERBOTTLEFULL_DESC"
    kind trinket
    frame 128

    durability 2
    max_durability 2
    dont_destroy_on_0 true

    ability tk_WaterBottle_Full

    passives {
        DurabilityTransform {
            eq [1 WaterBottle_Half]
            eq [0 WaterBottle_Empty]
        }
    }
}
```

---

### `WaterBottle_Half`
**Name:** Water Bottle  
**Description:** Use: Heal +5 HP and gain Heatwave immunity.
Refills when affected by Water Element effects.  
**Source:** `trinkets.gon`  

```
WaterBottle_Half {
    name "ITEM_WATERBOTTLEHALF_NAME"
    desc "ITEM_WATERBOTTLEHALF_DESC"
    kind trinket
    frame 129

    durability 1
    max_durability 2
    dont_destroy_on_0 true

    ability tk_WaterBottle_Half

    passives {
        TransformItemOnElementInfluence {
            element Greater_Water
            item WaterBottle_Full
            full_repair true
        }
        DurabilityTransform {
            ge [2 WaterBottle_Full]
            eq [0 WaterBottle_Empty]
        }
    }
}
```

---

### `WaterBottle_Empty`
**Name:** Empty Water Bottle  
**Description:** Use: Throw it at something.
Refills when affected by Water Element effects.  
**Source:** `trinkets.gon`  

```
WaterBottle_Empty {
    name "ITEM_WATERBOTTLEEMPTY_NAME"
    desc "ITEM_WATERBOTTLEMPTY_DESC"
    kind trinket
    frame 130

    durability 0
    max_durability 2
    dont_destroy_on_0 true

    ability tk_WaterBottle_Empty

    passives {
        TransformItemOnElementInfluence {
            element Greater_Water
            item WaterBottle_Full
            full_repair true
        }
        DurabilityTransform {
            ge [2 WaterBottle_Full]
            eq [1 WaterBottle_Half]
        }
    }
}
```

---

### `BloodyCoin`
**Name:** Bloody Coin  
**Description:** Use: Flip a coin.
Heads: Refresh your basic attack.
Tails: Lose 50% of your HP.  
**Source:** `trinkets.gon`  

```
BloodyCoin {
    name "ITEM_BLOODYCOIN_NAME"
    desc "ITEM_BLOODYCOIN_DESC"
    kind trinket
    rarity uncommon
    frame 38
	//set Bloody
    
    ability tk_BloodyCoin
}
```

---

### `GlowingCoin`
**Name:** Glowing Coin  
**Description:** Use: Flip a coin.
Heads: Double your mana.
Tails: Lose 50% of your mana.  
**Source:** `trinkets.gon`  

```
GlowingCoin {
    name "ITEM_GLOWINGCOIN_NAME"
    desc "ITEM_GLOWINGCOIN_DESC"
    kind trinket
    rarity uncommon
    frame 39
    
    ability tk_GlowingCoin
}
```

---

### `ElectricCoin`
**Name:** Electric Coin  
**Description:** Use: Flip a coin.
Heads: Refresh your movement action.
Tails: Gain Slow 2.  
**Source:** `trinkets.gon`  

```
ElectricCoin {
    name "ITEM_ELECTRICCOIN_NAME"
    desc "ITEM_ELECTRICCOIN_DESC"
    kind trinket
    rarity uncommon
    frame 40
    
    ability tk_ElectricCoin
}
```

---

### `CounterfeitCoin`
**Name:** Counterfeit Coin  
**Description:** Use: Flip a coin.
Heads: Gain 5 coins.
Tails: Lose 5 coins.  
**Source:** `trinkets.gon`  

```
CounterfeitCoin {
    name "ITEM_COUNTERFEITCOIN_NAME"
    desc "ITEM_COUNTERFEITCOIN_DESC"
    kind trinket
    rarity uncommon
    frame 41
    
    ability tk_CounterfeitCoin
}
```

---

### `Whistle`
**Name:** Whistle  
**Description:** Use: Summon a Fly, Maggot or Flea familiar.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
Whistle {//refresh when a familiar dies
    name "ITEM_WHISTLE_NAME"
    desc "ITEM_WHISTLE_DESC"
    kind trinket
    rarity common
    frame 16
	set [Druid, Hunter]
    
    ability tk_Whistle
}
```

---

### `Metronome`
**Name:** Metronome  
**Description:** Use: Cast a random upgraded spell.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
Metronome {
    name "ITEM_METRONOME_NAME"
    desc "ITEM_METRONOME_DESC"
    kind trinket
    rarity rare
    frame 17
	set Jester
    
    ability tk_Metronome
}
```

---

### `TinkerTools`
**Name:** Tinker Tools  
**Description:** Repair 1 use to your items at the end of each battle.  
**Source:** `trinkets.gon`  

```
TinkerTools {
    name "ITEM_TINKERTOOLS_NAME"
    desc "ITEM_TINKERTOOLS_DESC"
    kind trinket
    rarity rare
    frame 18
	set Tinkerer
    
    passives {
        StatusOnBattleEnd {
            RepairAll 1
        }
    }
}
```

---

### `RingOfFrost`
**Name:** Ring of Frost  
**Description:** Freezes tiles you walk over. +25% chance to inflict Freeze on units that contact or attack you.
Your Ice Element damage is increased by 1.  
**Source:** `trinkets.gon`  

```
RingOfFrost {
    name "ITEM_RINGOFFROST_NAME"
    desc "ITEM_RINGOFFROST_DESC"
    kind trinket
    rarity rare
    frame 177
	set [Mage, Frozen]
    
    passives {
        AddDamageToElementDamage {
            element Ice
            damage 1
        }
        RevengeDamage {
            damage 0
            effects {
                Freeze [1, .25]
            }
        }
        InnateElement Ice
    }
}
```

---

### `LuckyCoinPurse`
**Name:** Lucky Coin Purse  
**Description:** Gain +2 [img:lck] each time you gain a coin.  
**Source:** `trinkets.gon`  

```
LuckyCoinPurse {
    name "ITEM_LUCKYCOINPURSE_NAME"
    desc "ITEM_LUCKYCOINPURSE_DESC"
    kind trinket
    rarity rare
    frame 178
	set [Thief, Lucky]
    
    passives {
        StatusOnGainCoins {
            LuckUp 2
        }
    }
}
```

---

### `RageJuice`
**Name:** Rage Juice  
**Description:** Use: Gain +4 [img:str], +4 [img:spd], Brace 2 and Madness for the rest of the battle.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
RageJuice {
    name "ITEM_RAGEJUICE_NAME"
    desc "ITEM_RAGEJUICE_DESC"
    kind trinket
    rarity rare
    frame 179
	set Fighter
    
    ability tk_RageJuice
}
```

---

### `PrayerCard`
**Name:** Prayer Card  
**Description:** 33% chance to gain +1 [img:divineshield] each time you take damage.  
**Source:** `trinkets.gon`  

```
PrayerCard {
    name "ITEM_PRAYERCARD_NAME"
    desc "ITEM_PRAYERCARD_DESC"
    kind trinket
    rarity rare
    frame 180
	set [Cleric, Cardboard, Paper]
    
    passives {
        StatusOnTookDamage {
            DivineShield [1, .33]
        }
    }
}
```

---

### `TankToy`
**Name:** Tank Toy  
**Description:** Trample.  
**Source:** `trinkets.gon`  

```
TankToy {
    name "ITEM_TANKTOY_NAME"
    desc "ITEM_TANKTOY_DESC"
    kind trinket
    rarity rare
    frame 181
	set Tank
	
	shield 5
    
    passives {
        Trample 3
    }
}
```

---

### `BagOfSeeds`
**Name:** Bag of Seeds  
**Description:** Use: Spawn grass, flowers, or brambles on an adjacent tile.  
**Source:** `trinkets.gon`  

```
BagOfSeeds {
    name "ITEM_BAGOFSEEDS_NAME"
    desc "ITEM_BAGOFSEEDS_DESC"
    kind trinket
    rarity rare
    frame 182
	set Druid
    
    ability tk_BagOfSeeds
}
```

---

### `Libra`
**Name:** Libra  
**Description:** Balances all stats. This applies after all stat modifiers.  
**Source:** `trinkets.gon`  

```
Libra {
    name "ITEM_LIBRA_NAME"
    desc "ITEM_LIBRA_DESC"
    kind trinket
    rarity rare
    frame 174
	set Space

    passives {
        BalanceStats 1
    }
}
```

---

### `BallOfBandages`
**Name:** Ball of Bandages  
**Description:** Cleanse one stack of a random debuff at the end of each turn.
+1 Health Regen.  
**Source:** `trinkets.gon`  

```
BallOfBandages {
    name "ITEM_BALLOFBANDAGES_NAME"
    desc "ITEM_BALLOFBANDAGES_DESC"
    kind trinket
    rarity uncommon
    frame 99
	set Nurse

    passives {
        StatusEachTurnEnd {
            PartialCleanse 1
        }
        HealthRegenUp 1
    }
}
```

---

### `Natural20`
**Name:** Natural 20  
**Description:** Your weapons have +50% Crit Chance.
Your basic attack has +10% Crit Chance.  
**Source:** `trinkets.gon`  

```
Natural20 {
    name "ITEM_NATURAL20_NAME"
    desc "ITEM_NATURAL20_DESC"
    kind trinket
    rarity uncommon
    frame 34

    passives {
        BoostWeaponDamage {
            damage 0
            crit_chance .5
        }
        BasicAttackCritChance .1
    }
}
```

---

### `Technology`
**Name:** Technology  
**Description:** Use: Shoot a laser beam.
\[s:.7\](Usable once per battle.)\[/s\]
Refreshes when affected by Electricity.  
**Source:** `trinkets.gon`  

**Localization Strings:**
- `COMBAT_POPUP_RECHARGED`: "Recharged!"

```
Technology {
    name "ITEM_TECHNOLOGY_NAME"
    desc "ITEM_TECHNOLOGY_DESC"
    kind trinket
    rarity rare
    frame 46
	set [Cyborg, Bionic]
    
    ability tk_Technology

    passives {
        RefreshEquipmentAbilityOnElement {
            element Electric
            text "COMBAT_POPUP_RECHARGED"
        }
    }
}
```

---

### `Spring`
**Name:** Spring  
**Description:** Your movement action is Jump.  
**Source:** `trinkets.gon`  

```
Spring {
    name "ITEM_SPRING_NAME"
    desc "ITEM_SPRING_DESC"
    kind trinket
    rarity uncommon
    frame 47
	set Scrap
	
	spd 2
    
    passives {
        ReplaceBasicMove BasicJump
    }
}
```

---

### `RedDrink`
**Name:** Red Drink  
**Description:** Use: Heal 5 HP.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
RedDrink {
    name "ITEM_REDDRINK_NAME"
    desc "ITEM_REDDRINK_DESC"
    kind trinket
    rarity uncommon
    frame 48
    
    ability tk_RedDrink
}
```

---

### `GreenDrink`
**Name:** Green Drink  
**Description:** Use: Gain 5 mana.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
GreenDrink {
    name "ITEM_GREENDRINK_NAME"
    desc "ITEM_GREENDRINK_DESC"
    kind trinket
    rarity uncommon
    frame 49
    
    ability tk_GreenDrink
}
```

---

### `PurpleDrink`
**Name:** Purple Drink  
**Description:** Use: Heal 2 HP, gain 2 mana and +1 [img:shield].
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
PurpleDrink {
    name "ITEM_PURPLEDRINK_NAME"
    desc "ITEM_PURPLEDRINK_DESC"
    kind trinket
    rarity uncommon
    frame 50
    
    ability tk_PurpleDrink
}
```

---

### `LilBattery`
**Name:** Lil' Battery  
**Description:** Use: Refresh all items and spells with a once per battle restriction.
Can be used on allies.
\[s:.7\](Usable once per battle. Can't be refreshed.)\[/s\]  
**Source:** `trinkets.gon`  

```
LilBattery {
    name "ITEM_LILBATTERY_NAME"
    desc "ITEM_LILBATTERY_DESC"
    kind trinket
    rarity rare
    frame 51
    
    ability tk_LilBattery
}
```

---

### `CarvingKnife`
**Name:** Carving Knife  
**Description:** Use: Take 2 damage and spawn a Meat pickup.  
**Source:** `trinkets.gon`  

```
CarvingKnife {
    name "ITEM_CARVINGKNIFE_NAME"
    desc "ITEM_CARVINGKNIFE_DESC"
    kind trinket
    rarity uncommon
    
    frame 52
    ability tk_CarvingKnife
}
```

---

### `RazorBlade`
**Name:** Razor Blade  
**Description:** Use: Take 5 damage and gain +2 [img:str] and +2 [img:dex].  
**Source:** `trinkets.gon`  

```
RazorBlade {
    name "ITEM_RAZORBLADE_NAME"
    desc "ITEM_RAZORBLADE_DESC"
    kind trinket
    rarity rare
    frame 53
    
    ability tk_RazorBlade
}
```

---

### `Teleport`
**Name:** Teleport!  
**Description:** Use: Teleport to any open tile.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
Teleport {
    name "ITEM_TELEPORT_NAME"
    desc "ITEM_TELEPORT_DESC"
    kind trinket
    rarity rare
    frame 54
	set Experimental
    
    ability tk_Teleport
}
```

---

### `SmallEye`
**Name:** Small Eye  
**Description:** +15% Dodge Chance.
Your basic attack has a +10% chance to inflict Fear.  
**Source:** `trinkets.gon`  

```
SmallEye {
    name "ITEM_SMALLEYE_NAME"
    desc "ITEM_SMALLEYE_DESC"
    kind trinket
    rarity uncommon
    frame 58
	set Guts
    
    passives {
        DodgeChance 15%
        AddStatusToBasicAttack {
            Fear [1 .1]
        }
    }
}
```

---

### `Stickman`
**Name:** Stickman  
**Description:** Gain All Stats Up when you deal damage to a party member.  
**Source:** `trinkets.gon`  

```
Stickman {
    name "ITEM_STICKMAN_NAME"
    desc "ITEM_STICKMAN_DESC"
    kind trinket
    rarity rare
    frame 67
	set [Wood, Demonic]
    
    passives {
        ExtraStatusWhenDealingDamage {
            Conditional_PartyMember {
                Conditional_IsSelf {
                } Else {
                    ApplyToSource {
                        AllStatsUp 1
                    }
                }
            }
        }
    }
}
```

---

### `CursedStickman`
**Name:** Cursed Stickman  
**Description:** Gain All Stats Up when you deal damage to a party member.
10% chance to gain Madness at the start of your turn.  
**Source:** `trinkets.gon`  

```
CursedStickman {
    name "ITEM_CURSEDSTICKMAN_NAME"
    desc "ITEM_CURSEDSTICKMAN_DESC"
    kind trinket
    rarity rare
    cursed true
    frame 68
	set [Wood, Demonic]
    
    passives {
        StatusEachTurnBegin {
            Conditional_BadRoll {
                odds .1
                
                Temporary {
                    status Madness
                    stacks 1
                    turns 1
                    expires_on_end_turn true
                }
            }
        }
        ExtraStatusWhenDealingDamage {
            Conditional_PartyMember {
                Conditional_IsSelf {
                } Else {
                    ApplyToSource {
                        AllStatsUp 1
                    }
                }
            }
        }
    }
}
```

---

### `GlowingSeed`
**Name:** Glowing Seed  
**Description:** Your basic attack spawns tall grass.  
**Source:** `trinkets.gon`  

```
GlowingSeed {
    name "ITEM_GLOWINGSEED_NAME"
    desc "ITEM_GLOWINGSEED_DESC"
    kind trinket
    rarity uncommon
    frame 71
    
    passives {
        AddStatusToBasicAttack {
            ChangeTile TallGrassTile
        }
    }
}
```

---

### `MagicSeed`
**Name:** Magic Seed  
**Description:** Your basic attack spawns brambles.  
**Source:** `trinkets.gon`  

```
MagicSeed {
    name "ITEM_MAGICSEED_NAME"
    desc "ITEM_MAGICSEED_DESC"
    kind trinket
    rarity uncommon
    frame 113
    
    passives {
        AddStatusToBasicAttack {
            ChangeTile BrambleTile
        }
    }
}
```

---

### `WeirdEgg`
**Name:** Weird Egg  
**Description:** 10% chance to spawn a controllable Fetus familiar at the end of each turn. It joins your party.  
**Source:** `trinkets.gon`  

```
WeirdEgg {
    name "ITEM_WEIRDEGG_NAME"
    desc "ITEM_WEIRDEGG_DESC"
    kind trinket
    rarity uncommon
    frame 73
	set Baby

    passives {
        StatusEachTurnEnd {
            Conditional_GoodRoll {
                odds 10%
                ForceUseAbility tk_WeirdEgg_Spawn
            }
        }
    }
}
```

---

### `SpottedMushroom`
**Name:** Spotted Mushroom  
**Description:** ITEM_SPOTTEDMUSHROOM_DESC  
**Source:** `trinkets.gon`  

```
SpottedMushroom {
    name "ITEM_SPOTTEDMUSHROOM_NAME"
    desc "ITEM_SPOTTEDMUSHROOM_DESC"
    kind trinket
    rarity common
    frame 74
	set Druid
    
    str_aux_initialize random_seed

    passives {
        RandomSeededStatModifier [2 -1] // hard coded in SpawnDatabase::get_item_stats
    }
}
```

---

### `MundaneStone`
**Name:** Mundane Stone  
**Description:** Your basic attack's damage is increased by your lowest stat minus 2.  
**Source:** `trinkets.gon`  

```
MundaneStone {
    name "ITEM_MUNDANESTONE_NAME"
    desc "ITEM_MUNDANESTONE_DESC"
    kind trinket
    rarity rare
    frame 88
	set Rock
    
    passives {
        StatDependentPassive {
            AddDamageToBasicAttack "min(min(min(min(min(min(str,dex),int),con),lck),spd),cha)-2"
        }
    }
}
```

---

### `EmptySack`
**Name:** Empty Sack  
**Description:** Spawn 3 pickups at the start of each battle.
Find an extra common item at the end of each battle.  
**Source:** `trinkets.gon`  

```
EmptySack {
    name "ITEM_EMPTYSACK_NAME"
    desc "ITEM_EMPTYSACK_DESC"
    kind trinket
    rarity uncommon
    frame 115
    set [Leather, HumanFlesh]
	
    passives {
        StatusOnBattleStart {
            FindItemFromPool common
        }
        SpawnExtraThingsOnBattleStart {
            object RandomPickup
            number 3
        }
    }
}
```

---

### `AAABattery`
**Name:** AAA Battery  
**Description:** Every time you cast 3 spells, gain +3 Charge.  
**Source:** `trinkets.gon`  

```
AAABattery {
    name "ITEM_AAABATTERY_NAME"
    desc "ITEM_AAABATTERY_DESC"
    kind trinket
    rarity uncommon
    frame 117
    
    passives {
        StatusEveryXSpellCasts {
            stacks 3
            Charge 3
        }
    }
}
```

---

### `ToolBox`
**Name:** Tool Box  
**Description:** Your items lose Brittle and Fragile.
Your weapons have a 25% chance to repair 1 use when used.  
**Source:** `trinkets.gon`  

```
ToolBox {
    name "ITEM_TOOLBOX_NAME"
    desc "ITEM_TOOLBOX_DESC"
    kind trinket
    rarity uncommon
    frame 118
	set Tinkerer
    
    passives {
        SetBrittleImmune ""
        SetFragileImmune ""
        AddSelfStatusToWeapons {
            RepairWeapon [1 .25]
        }
    }
}
```

---

### `RubberCement`
**Name:** Rubber Cement  
**Description:** Your projectiles bounce to another enemy within 2 tiles.  
**Source:** `trinkets.gon`  

```
RubberCement {
    name "ITEM_RUBBERCEMENT_NAME"
    desc "ITEM_RUBBERCEMENT_DESC"
    kind trinket
    rarity rare
    frame 124
	set [Rubber, Slimy]
    
    passives {
        BouncyProjectiles {
            max_bounces 1
            max_range 2
        }
    }
}
```

---

### `CoinPurse`
**Name:** Coin Purse  
**Description:** When you collect a coin pickup, gain +1 coin.
Find an extra coin at the end of each battle.  
**Source:** `trinkets.gon`  

```
CoinPurse {
    name "ITEM_COINPURSE_NAME"
    desc "ITEM_COINPURSE_DESC"
    kind trinket
    rarity uncommon
    frame 125
	set Mother
    
    passives {
        StatusOnPickupCoins {
            GainCoins 1
        }
        StatusOnBattleEnd {
            GainCoins 1
        }
    }
}
```

---

### `Fork`
**Name:** Fork  
**Description:** Heal 5 HP when you kill a unit or destroy a corpse.  
**Source:** `trinkets.gon`  

```
Fork {
    name "ITEM_FORK_NAME"
    desc "ITEM_FORK_DESC"
    kind trinket
    rarity uncommon
    frame 126
    
    passives {
        StatusOnKill {
            HealthGain 5
        }
        StatusOnPopCorpse {
            HealthGain 5
        }
    }
}
```

---

### `CatONineTails`
**Name:** Cat o' Nine Tails  
**Description:** Use: Take 1 damage and cleanse one random debuff.  
**Source:** `trinkets.gon`  

```
CatONineTails {
    name "ITEM_CATONINETAILS_NAME"
    desc "ITEM_CATONINETAILS_DESC"
    kind trinket
    rarity uncommon
    frame 127
	set Gimp
    
    ability tk_CatONineTails
}
```

---

### `Glue`
**Name:** Glue  
**Description:** Use: Gain +20% Dodge Chance, -1 [img:int] and Confusion 2.  
**Source:** `trinkets.gon`  

```
Glue {
    name "ITEM_GLUE_NAME"
    desc "ITEM_GLUE_DESC"
    rarity uncommon
    kind trinket
    frame 137
    durability [5 8]
	set Slimy
    
    ability tk_Glue
}
```

---

### `MyShadow`
**Name:** My Shadow  
**Description:** Use: Move 3 tiles, leaving a shadow copy behind that mimics your basic attack.
The shadow fades at the end of the turn.  
**Source:** `trinkets.gon`  

```
MyShadow {
    name "ITEM_MYSHADOW_NAME"
    desc "ITEM_MYSHADOW_DESC"
    rarity rare
    kind trinket
    frame 133
	set Demonic

    durability 6

    ability tk_MyShadow
}
```

---

### `EggSack`
**Name:** Egg Sack  
**Description:** Use: Spawns Spiderlings in an area.  
**Source:** `trinkets.gon`  

```
EggSack {
    name "ITEM_EGGSACK_NAME"
    desc "ITEM_EGGSACK_DESC"
    rarity uncommon
    kind trinket
    frame 134
    durability [4 6]
    
    ability tk_EggSack
}
```

---

### `GorgonsEye`
**Name:** Gorgon's Eye  
**Description:** Use: Petrify all nearby units in your line of sight.  
**Source:** `trinkets.gon`  

```
GorgonsEye {
    name "ITEM_GORGONSEYE_NAME"
    desc "ITEM_GORGONSEYE_DESC"
    rarity uncommon
    kind trinket
    frame 135
    durability [5 7]
	set [Guts, Rock]
    
    ability tk_GorgonsEye
}
```

---

### `HotLunch`
**Name:** Hot Lunch  
**Description:** Spawn a Flaming Meat pickup.  
**Source:** `trinkets.gon`  

```
HotLunch {
    name "ITEM_HOTLUNCH_NAME"
    desc "ITEM_HOTLUNCH_DESC"
    rarity uncommon
    kind trinket
    frame 139
    durability [5 8]
	set Paper
    
    ability tk_HotLunch
}
```

---

### `ButterBean`
**Name:** Butter Bean  
**Description:** Use: Fart at an adjacent unit, knocking it back 1 tile.  
**Source:** `trinkets.gon`  

```
ButterBean {
    name "ITEM_BUTTERBEAN_NAME"
    desc "ITEM_BUTTERBEAN_DESC"
    rarity common
    kind trinket
    frame 140
    
    ability tk_ButterBean
}
```

---

### `MomsRing`
**Name:** Mom's Ring  
**Description:** +1 Damage. Find a pill at the end of each battle.  
**Source:** `trinkets.gon`  

```
MomsRing {
    name "ITEM_MOMSRING_NAME"
    desc "ITEM_MOMSRING_DESC"
    rarity rare
    kind trinket
    frame 142
	set Mother
    
    passives {
        DamageUp 1
        StatusOnBattleEnd {
            FindItemFromPool pills
        }
    }
}
```

---

### `MindStone`
**Name:** Mind Stone  
**Description:** Your collarless spells cost -2 mana.  
**Source:** `trinkets.gon`  

```
MindStone {
    name "ITEM_MINDSTONE_NAME"
    desc "ITEM_MINDSTONE_DESC"
    rarity rare
    kind trinket
    frame 146
	set Rock
    
    passives {
        ClassManaCostReduction {
            class Colorless
            reduction 2
        }
    }
}
```

---

### `SkillStone`
**Name:** Skill Stone  
**Description:** Spells that match your class cost -1 mana.  
**Source:** `trinkets.gon`  

```
SkillStone {
    name "ITEM_SKILLSTONE_NAME"
    desc "ITEM_SKILLSTONE_DESC"
    rarity rare
    kind trinket
    frame 147
	set Rock
    
    passives {
        ClassManaCostReduction {
            reduction 1
        }
    }
}
```

---

### `Multiplier`
**Name:** Multiplier  
**Description:** You can use your weapon an extra time each turn.  
**Source:** `trinkets.gon`  

```
Multiplier {
    name "ITEM_MULTIPLIER_NAME"
    desc "ITEM_MULTIPLIER_DESC"
    rarity rare
    kind trinket
    frame 148
    
    passives {
        ExtraWeaponAttacks 1
    }
}
```

---

### `SacredHeart`
**Name:** Sacred Heart  
**Description:** +1 Damage. Emit 2 Sparkles when you use your basic attack.  
**Source:** `trinkets.gon`  

```
SacredHeart {
    name "ITEM_SACREDHEART_NAME"
    desc "ITEM_SACREDHEART_DESC"
    rarity rare
    kind trinket
    frame 153
	set Cleric
    
    passives {
        DamageUp 1
        AddSelfStatusToBasicAttack {
            RandomMagicMissile 2
        }
    }
}
```

---

### `FetusInAJar`
**Name:** Fetus in a Jar  
**Description:** At the the start of each battle, equip a temporary Bomb if your weapon slot is open.
At the end of each turn, if you didn't use your basic attack, equip another Bomb.  
**Source:** `trinkets.gon`  

```
FetusInAJar {
    name "ITEM_FETUSINAJAR_NAME"
    desc "ITEM_FETUSINAJAR_DESC"
    rarity rare
    kind trinket
    frame 155
	set Baby
    
    passives {
        StatusOnBattleStart {
            Craft {
                pool bombs //should expand to bombs_0, bombs_1, bombs_2, bombs_3
                slot weapon
                works_with_tech true
            }
        }
        StatusIfUnusedActPoints {
            Craft {
                pool bombs //should expand to bombs_0, bombs_1, bombs_2, bombs_3
                slot weapon
                works_with_tech true
            }
        }
    }
}
```

---

### `Breakfast`
**Name:** Breakfast  
**Description:** +2 Health Regen.  
**Source:** `trinkets.gon`  

```
Breakfast {
    name "ITEM_BREAKFAST_NAME"
    desc "ITEM_BREAKFAST_DESC"
    rarity uncommon
    kind trinket
    frame 157
	set Cardboard
    
    passives {
        HealthRegenUp 2
    }
}
```

---

### `DreamCatcher`
**Name:** Dream Catcher  
**Description:** Whenever you fall asleep, gain All Stats Up, restore all your mana, and heal a random injury.  
**Source:** `trinkets.gon`  

```
DreamCatcher {
    name "ITEM_DREAMCATCHER_NAME"
    desc "ITEM_DREAMCATCHER_DESC"
    rarity rare
    kind trinket
    frame 158
	set Twine
    
    passives {
        StatusOnFallAsleep {
            AllStatsUp 1
            FillMana 1
			HealRandomInjury 1
        }
    }
}
```

---

### `EnchantingPoop`
**Name:** Enchanting Poop  
**Description:** Spawn a poop at the start of each battle.  
**Source:** `trinkets.gon`  

```
EnchantingPoop { //Aquired from various Poop events
    name "ITEM_ENCHANTINGPOOP_NAME"
    desc "ITEM_ENCHANTINGPOOP_DESC"
    kind trinket
    frame 159
	set Fecal
    
    passives {
        SpawnOnBattleStart {
            object Poop
        }
    }
}
```

---

### `EnchantingPoop_Cursed`
**Source:** `trinkets.gon`  

```
EnchantingPoop_Cursed {
    variant_of EnchantingPoop
    cursed true
}
```

---

### `LunchBox`
**Name:** Lunch Box  
**Description:** Use: Heal 5 HP.
Whenever you collect a food pickup, instead of its normal effects, add +1 use to this item.  
**Source:** `trinkets.gon`  

```
LunchBox {
    name "ITEM_LUNCHBOX_NAME"
    desc "ITEM_LUNCHBOX_DESC"
    rarity uncommon
    kind trinket
    frame 176
    
    durability 0
    max_durability 9
    dont_destroy_on_0 true

    passives {
        StatusOnEatFood {
            TempPassiveUntilSettled {
                LimitHeal 0
            }
            RepairTrinket 1
        }
    }
    
    ability tk_LunchBox
}
```

---

### `SatanicBible`
**Name:** Satanic Bible  
**Description:** Heal 3 HP and gain +3 Charge each time you damage a party member.  
**Source:** `trinkets.gon`  

```
SatanicBible {
    name "ITEM_SATANICBIBLE_NAME"
    desc "ITEM_SATANICBIBLE_DESC"
    rarity rare
    kind trinket
    frame 184
	set [Demonic, Paper]
    
    passives {
        ExtraStatusWhenDealingDamage {
            Conditional_PartyMember {
                Conditional_IsSelf {
                } Else {
                    ApplyToSource {
                        HealthGain 3
                        Charge 3
                    }
                }
            }
        }
    }
}
```

---

### `TinyPebble`
**Name:** Tiny Pebble  
**Description:** +10% Dodge Chance.
Gain +2% Dodge Chance when you dodge an attack.  
**Source:** `trinkets.gon`  

```
TinyPebble {
    name "ITEM_TINYPEBBLE_NAME"
    desc "ITEM_TINYPEBBLE_DESC"
    rarity uncommon
    kind trinket
    frame 185
	set Rock
    
    passives {
        DodgeChance_Status 10
        StatusOnDodge {
            DodgeChance_Status 2
        }
    }
}
```

---

### `ScrapBag`
**Name:** Scrap Bag  
**Description:** Craft a temporary weapon at the start of the battle if you don't have a weapon.  
**Source:** `trinkets.gon`  

```
ScrapBag {
    name "ITEM_SCRAPBAG_NAME"
    desc "ITEM_SCRAPBAG_DESC"
    rarity uncommon
    kind trinket
    frame 186
	set [Scrap, Tinkerer]
    
    passives {
        StatusOnBattleStart {
            Craft {
                pool tinkerer_default
                slot weapon
            }
        }
    }
}
```

---

### `Cookbook`
**Name:** Cookbook  
**Description:** When you kill a unit or destroy a corpse, it becomes meat.  
**Source:** `trinkets.gon`  

```
Cookbook {
    name "ITEM_COOKBOOK_NAME"
    desc "ITEM_COOKBOOK_DESC"
    rarity uncommon
    kind trinket
    frame 187
	set [Butcher, Paper]
    
    passives {
        KillsToMeat Food
    }
}
```

---

### `TarotDeck`
**Name:** Tarot Deck  
**Description:** Use: Conjure a random, single-use spell as a bonus ability.  
**Source:** `trinkets.gon`  

```
TarotDeck {
    name "ITEM_TAROTDECK_NAME"
    desc "ITEM_TAROTDECK_DESC"
    rarity uncommon
    kind trinket
    frame 183
	set [Psychic, Cardboard, Paper]
    
    ability tk_TarotDeck

    passives {
    }
}
```

---

### `TinyCage`
**Name:** Tiny Cage  
**Description:** Spawn a random animal familiar at the start of each battle.  
**Source:** `trinkets.gon`  

```
TinyCage {
    name "ITEM_TINYCAGE_NAME"
    desc "ITEM_TINYCAGE_DESC"
    rarity uncommon
    kind trinket
    frame 188
	set Druid

    passives {
        SpawnOnBattleStart {
            object RandomDruidFamiliar
            number 1
        }
    }
}
```

---

### `SpellBook`
**Name:** Spell Book  
**Description:** Use: Gain 10 mana and conjure a random Mage spell as a bonus ability.  
**Source:** `trinkets.gon`  

```
SpellBook {
    name "ITEM_SPELLBOOK_NAME"
    desc "ITEM_SPELLBOOK_DESC"
    rarity rare
    kind trinket
    frame 207
	set [Mage, Paper]

    durability 2
    ability tk_SpellBook

    passives {
    }
}
```

---

### `BagOfBags`
**Name:** Bag o' Bags  
**Description:** Use: Throw a trash bag on an adjacent tile.  
**Source:** `trinkets.gon`  

```
BagOfBags {
    name "ITEM_BAGOFBAGS_NAME"
    desc "ITEM_BAGOFBAGS_DESC"
    rarity uncommon
    kind trinket
    frame 208

    durability 13
    ability tk_BagOfBags

    passives {
    }
}
```

---

### `Steroids`
**Name:** Steroids  
**Description:** Use: Gain +1 [img:str], permanently. For the rest of the adventure, you have a +2% chance to gain Madness at the start of each turn.  
**Source:** `trinkets.gon`  

```
Steroids {
    name "ITEM_STEROIDS_NAME"
    desc "ITEM_STEROIDS_DESC"
    rarity rare
    kind trinket
    frame 209
	set Fighter

    durability 9

    ability tk_Steroids

    passives {
    }
}
```

---

### `HolyWater`
**Name:** Holy Water  
**Description:** Heal 2 HP in an area.  
**Source:** `trinkets.gon`  

```
HolyWater {
    name "ITEM_HOLYWATER_NAME"
    desc "ITEM_HOLYWATER_DESC"
    rarity uncommon
    kind trinket
    frame 210
	set Cleric

    ability tk_HolyWater

    passives {
    }
}
```

---

### `TankJuice`
**Name:** Tank Juice  
**Description:** Use: Gain -1 [img:spd], then, for the rest of the turn, all damage you deal has Knockback 2 and Chain Knockback.  
**Source:** `trinkets.gon`  

```
TankJuice {
    name "ITEM_TANKJUICE_NAME"
    desc "ITEM_TANKJUICE_DESC"
    rarity uncommon
    kind trinket
    frame 211
	set Tank
    
    ability tk_TankJuice

    passives {
    }
}
```

---

### `HuntersFlute`
**Name:** Hunter's Flute  
**Description:** Spawn 2-3 random familiars on adjacent tiles.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
HuntersFlute {
    name "ITEM_HUNTERSFLUTE_NAME"
    desc "ITEM_HUNTERSFLUTE_DESC"
    rarity rare
    kind trinket
    frame 212
	set Hunter

    ability tk_HuntersFlute

    passives {
    }
}
```

---

### `FriendshipBracelet`
**Name:** Friendship Bracelet  
**Description:** Use: Permanently charm a non-boss enemy. It joins your party.  
**Source:** `trinkets.gon`  

```
FriendshipBracelet {
    name "ITEM_FRIENDSHIPBRACELET_NAME"
    desc "ITEM_FRIENDSHIPBRACELET_DESC"
    rarity rare
    kind trinket
    frame 213
	set Druid

    durability 3
    ability tk_FriendshipBracelet

    passives {
    }
}
```

---

### `CambionConception`
**Name:** Cambion Conception  
**Description:** Use: Summon a half-sized copy of yourself that has 66% of your stats and is AI controlled.  
**Source:** `trinkets.gon`  

```
CambionConception {
    name "ITEM_CAMBIONCONCEPTION_NAME"
    desc "ITEM_CAMBIONCONCEPTION_DESC"
    rarity rare
    kind trinket
    frame 214
	set [Necromancer, Demonic, Baby]

    durability 2
    ability tk_CambionConception

    passives {
    }
}
```

---

### `EmptyHand`
**Name:** Empty Hand  
**Description:** Use: Gain +3 [img:shield] for each empty armor slot you have.
When this breaks, gain +1 [img:con] permanently.  
**Source:** `trinkets.gon`  

```
EmptyHand {
    name "ITEM_EMPTYHAND_NAME"
    desc "ITEM_EMPTYHAND_DESC"
    rarity rare
    kind trinket
    frame 215
	set Monk

    durability 4
    ability tk_EmptyHand

    passives {
        StatusOnBreak {
            ConstitutionUp 1
        }
    }
}
```

---

### `Fireworks`
**Name:** Fireworks  
**Description:** Use: Emit 5 Sparkles.
If you end your turn with 0 mana, this gains +1 use.  
**Source:** `trinkets.gon`  

```
Fireworks {
    name "ITEM_FIREWORKS_NAME"
    desc "ITEM_FIREWORKS_DESC"
    rarity rare
    kind trinket
    frame 216
	set Tinkerer

    durability 3
    ability tk_Fireworks

    passives {
        StatusEachTurnEnd {
            Conditional_ManaThreshold {
                threshold_flat 0
                RepairTrinket 1
            }
        }
    }
}
```

---

### `SackOfMeat`
**Name:** Sack o' Meat  
**Description:** Use: Heal 4 HP.
This gains +1 use each time you destroy a corpse.  
**Source:** `trinkets.gon`  

```
SackOfMeat {
    name "ITEM_SACKOFMEAT_NAME"
    desc "ITEM_SACKOFMEAT_DESC"
    rarity rare
    kind trinket
    frame 217
	set Butcher

    durability 2
    ability tk_SackOfMeat

    passives {
	    ExtraTrinketUses 10
        StatusOnPopCorpse {
            RepairTrinket 1
        }
    }
}
```

---

### `DruidsWhistle`
**Name:** Druid's Whistle  
**Description:** Use: Spawn a random animal familiar on an adjacent tile.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
DruidsWhistle {
    name "ITEM_DRUIDSWHISTLE_NAME"
    desc "ITEM_DRUIDSWHISTLE_DESC"
    rarity rare
    kind trinket
    frame 218
	set Druid
    
    ability tk_DruidsWhistle

    passives {
    }
}
```

---

### `BallOfYarn`
**Name:** Ball of Yarn  
**Description:** Spawn a Charmed Kitten with All Stats Up 2 at the start of each battle.  
**Source:** `trinkets.gon`  

```
BallOfYarn {
    name "ITEM_BALLOFYARN_NAME"
    desc "ITEM_BALLOFYARN_DESC"
    rarity uncommon
    kind trinket
    frame 226
	set Twine

    passives {
        SpawnOnBattleStart BuffCharmedKitten
    }
}
```

---

### `BirdHead`
**Name:** Bird Head  
**Description:** Your basic attack inflicts Soul Link.  
**Source:** `trinkets.gon`  

```
BirdHead {
    name "ITEM_BIRDHEAD_NAME"
    desc "ITEM_BIRDHEAD_DESC"
    rarity rare
    kind trinket
    frame 192
	set Feathered
    
    passives {
        AddStatusToBasicAttack {
            SoulLink 1
        }
    }
}
```

---

### `BrokenMirror`
**Name:** Broken Mirror  
**Description:** ITEM_BROKENMIRROR_DESC  
**Source:** `trinkets.gon`  

```
BrokenMirror {
    name "ITEM_BROKENMIRROR_NAME"
    desc "ITEM_BROKENMIRROR_DESC"
    rarity rare
    kind trinket
    frame 196
	set Used
    
    lck -99

    passives {
    }
}
```

---

### `Binoculars`
**Name:** Binoculars  
**Description:** +2 range.  
**Source:** `trinkets.gon`  

```
Binoculars {
    name "ITEM_BINOCULARS_NAME"
    desc "ITEM_BINOCULARS_DESC"
    rarity uncommon
    kind trinket
    frame 198
    
    passives {
        AddBonusRange 2
    }
}
```

---

### `Bishop`
**Name:** Bishop  
**Description:** Use: Move any number of tiles in a diagonal line.  
**Source:** `trinkets.gon`  

```
Bishop {
    name "ITEM_BISHOP_NAME"
    desc "ITEM_BISHOP_DESC"
    rarity uncommon
    kind trinket
    frame 201

    durability 6
    
    ability tk_Bishop
}
```

---

### `GoldenEgg`
**Name:** Golden Egg  
**Description:** Find 3-5 extra coins at the end of each battle.  
**Source:** `trinkets.gon`  

```
GoldenEgg {
    name "ITEM_GOLDENEGG_NAME"
    desc "ITEM_GOLDENEGG_DESC"
    rarity uncommon
    kind trinket
    frame 190
    
    passives {
        StatusOnBattleEnd {
            GainCoins [3 5]
        }
    }
}
```

---

### `BirdFeed`
**Name:** Bird Feed  
**Description:** +50% chance for an extra bird to spawn at the start of each battle.  
**Source:** `trinkets.gon`  

```
BirdFeed {
    name "ITEM_BIRDFEED_NAME"
    desc "ITEM_BIRDFEED_DESC"
    rarity uncommon
    kind trinket
    frame 191
    
    passives {
        SpawnOnBattleStartRandomEmptyTile {
            object Bird
            number [0 1]
        }
    }
}
```

---

### `AngelWing`
**Name:** Angel Wing  
**Description:** If an attack would down you, instead lower your HP to 1. While at 1 HP, this has no effect.  
**Source:** `trinkets.gon`  

```
AngelWing {
    name "ITEM_ANGELWING_NAME"
    desc "ITEM_ANGELWING_DESC"
    rarity rare
    kind trinket
    frame 195
	set Feathered
    
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

### `SoulJar`
**Name:** Soul Jar  
**Description:** When your body is destroyed, this item is recovered and permanently gains the ability to summon a ghost copy of you.  
**Source:** `trinkets.gon`  

```
SoulJar {
    name "ITEM_SOULJAR_NAME"
    desc "ITEM_SOULJAR_DESC"
    rarity rare
    kind trinket
    frame 175

    passives {
        DropSoulJarOnDeath SoulJar_Full
    }
}
```

---

### `SoulJar_Full`
**Name:** Soul Jar  
**Description:** Use: Summon a ghost copy of {aux_cat_name}.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
SoulJar_Full {
    name "ITEM_SOULJAR_FULL_NAME"
    desc "ITEM_SOULJAR_FULL_DESC"
    rarity very_rare
    kind trinket
    frame 206
    aux -1
    aux_is_catid true
    
    ability tk_SoulJar
}
```

---

### `PetrifiedPinky`
**Name:** Petrified Pinky  
**Description:** If an attack would down you, instead this breaks and you regain 50% of your max HP.  
**Source:** `trinkets.gon`  

```
PetrifiedPinky {
    name "ITEM_PETRIFIEDPINKY_NAME"
    desc "ITEM_PETRIFIEDPINKY_DESC"
    rarity uncommon
    kind trinket
    frame 7
	set [Rat, Rock]
    
    passives {
        DeathRattleRevive tk_PetrifiedPinky
    }
}
```

---

### `CatRib`
**Name:** Cat Rib  
**Description:** When your body is destroyed, you are reborn as a kitten!  
**Source:** `trinkets.gon`  

```
CatRib {
    name "ITEM_CATRIB_NAME"
    desc "ITEM_CATRIB_DESC"
    rarity rare
    kind trinket
    frame 19
	set Bone
    
    passives {
        SpawnCatCloneOnCorpsePopped 1
    }
}
```

---

### `EstusFlask_Full`
**Name:** Glowing Flask  
**Description:** Use: Heal 5 HP. This refills at the end of each battle.  
**Source:** `trinkets.gon`  

```
EstusFlask_Full {
    name "ITEM_ESTUSFLASK_NAME"
    desc "ITEM_ESTUSFLASK_DESC"
    rarity rare
    kind trinket
    frame 87

    durability 3
    max_durability 3
    dont_destroy_on_0 true

    ability tk_EstusFlask

    passives {
        DurabilityTransform {
            eq [2 EstusFlask_Half]
            eq [1 EstusFlask_Half]
            eq [0 EstusFlask_Empty]
        }
    }
}
```

---

### `EstusFlask_Half`
**Name:** Glowing Flask  
**Description:** Use: Heal 5 HP. This refills at the end of each battle.  
**Source:** `trinkets.gon`  

```
EstusFlask_Half {
    name "ITEM_ESTUSFLASK_NAME"
    desc "ITEM_ESTUSFLASK_DESC"
    rarity rare
    kind trinket
    frame 203

    durability 2
    max_durability 3
    dont_destroy_on_0 true

    ability tk_EstusFlask

    passives {
        DurabilityTransform {
            ge [3 EstusFlask_Full]
            eq [0 EstusFlask_Empty]
        }
        StatusOnBattleEnd {
            RepairTrinket 99
        }
        TransformItemOnElementInfluence {
            element Fire
            item EstusFlask_Full
            full_repair true
        }
    }
}
```

---

### `EstusFlask_Empty`
**Name:** Glowing Flask  
**Description:** Use: Heal 5 HP. This refills at the end of each battle.  
**Source:** `trinkets.gon`  

```
EstusFlask_Empty {
    name "ITEM_ESTUSFLASK_NAME"
    desc "ITEM_ESTUSFLASK_DESC"
    rarity rare
    kind trinket
    frame 204

    durability 0
    max_durability 3
    dont_destroy_on_0 true

    passives {
        DurabilityTransform {
            ge [3 EstusFlask_Full]
            eq [2 EstusFlask_Half]
            eq [1 EstusFlask_Half]
        }
        StatusOnBattleEnd {
            RepairTrinket 99
        }
        TransformItemOnElementInfluence {
            element Fire
            item EstusFlask_Full
            full_repair true
        }
    }
}
```

---

### `LuckyCoin`
**Name:** Lucky Coin  
**Description:** Coins that spawn at the start of each battle are doubled.  
**Source:** `trinkets.gon`  

```
LuckyCoin {
    name "ITEM_LUCKYCOIN_NAME"
    desc "ITEM_LUCKYCOIN_DESC"
    rarity uncommon
    kind trinket
    frame 145
	set Lucky

    lck 2

    passives {
        MultiplyCoinsOnBattleStart 2
    }
}
```

---

### `HeavyRock`
**Name:** Heavy Rock  
**Description:** Rocks you knock back deal +5 damage and have Chain Knockback.  
**Source:** `trinkets.gon`  

```
HeavyRock {
    name "ITEM_HEAVYROCK_NAME"
    desc "ITEM_HEAVYROCK_DESC"
    rarity uncommon
    kind trinket
    frame 65
	set Rock

    passives {
        AddStatusToAllDamage {
            Conditional_HasTag {
                tag rock
                BonusKnockbackDamage 5
                OverrideChainKnockback 0
            }
        }
    }
}
```

---

### `Ipecac`
**Name:** Ipecac  
**Description:** Your basic attack is Explosive Shot.  
**Source:** `trinkets.gon`  

```
Ipecac {
    name "ITEM_IPECAC_NAME"
    desc "ITEM_IPECAC_DESC"
    rarity rare
    kind trinket
    frame 149
	set Medical

    attack BasicExplosiveShot
    passives {
        OverrideBasicAttack BasicExplosiveShot
    }
}
```

---

### `MeatCube`
**Name:** Meat Cube  
**Description:** Start with a Flesh Lad familiar.  
**Source:** `trinkets.gon`  

```
MeatCube {
    name "ITEM_MEATCUBE_NAME"
    desc "ITEM_MEATCUBE_DESC"
    rarity rare
    kind trinket
    frame 143
	set Meat

    passives {
        SpawnOnBattleStart {
            object FamiliarFleshLad
        }
    }
}
```

---

### `SoyMilk`
**Name:** Soy Milk  
**Description:** Your basic attack cannot deal more than 1 damage.
You can attack 2 extra times each turn.  
**Source:** `trinkets.gon`  

```
SoyMilk {
    name "ITEM_SOYMILK_NAME"
    desc "ITEM_SOYMILK_DESC"
    rarity rare
    kind trinket
    frame 150

    passives {
        CapBasicAttackDamage 1
        ExtraBasicAttacks 2
    }
}
```

---

### `SpoonBender`
**Name:** Spoon Bender  
**Description:** Your basic attack can't miss and emits a Sparkle when used.  
**Source:** `trinkets.gon`  

```
SpoonBender {
    name "ITEM_SPOONBENDER_NAME"
    desc "ITEM_SPOONBENDER_DESC"
    rarity rare
    kind trinket
    frame 151
	set Psychic

    passives {
        BasicAttackCantMiss 1
        AddSelfStatusToBasicAttack {
            RandomMagicMissile 1
        }
    }
}
```

---

### `Cancer`
**Name:** Cancer  
**Description:** At the end of each battle, gain -1 to three random stats, then gain a mutation.  
**Source:** `trinkets.gon`  

```
Cancer {
    name "ITEM_CANCER_NAME"
    desc "ITEM_CANCER_DESC"
    rarity rare
    kind trinket
    frame 152
	set Mother

    passives {
        StatusOnBattleEnd {
            even_if_dead true
            
            RandomPermanentStat -3
            RandomMutation 1
        }
    }
}
```

---

### `Wafer`
**Name:** Wafer  
**Description:** ITEM_WAFER_DESC  
**Source:** `trinkets.gon`  

```
Wafer {
    name "ITEM_WAFER_NAME"
    desc "ITEM_WAFER_DESC"
    rarity rare
    kind trinket
    frame 156
	set Cleric

    divine_shield 2

    passives {
    }
}
```

---

### `LargeMeteor`
**Name:** Large Meteor  
**Description:** - {str_aux_passive_name} -
{str_aux_passive_desc}  
**Source:** `trinkets.gon`  

```
LargeMeteor {
    name "ITEM_LARGEMETEOR_NAME"
    desc "ITEM_LARGEMETEOR_DESC"
    rarity uncommon
    kind trinket
    frame 243
    randomize_piece_frames true
	set Planet 
    
    str_aux_initialize random_copyable_colorless_passive
    str_aux_is_copy_passive true
}
```

---

### `BloodyRazor`
**Name:** Bloody Razor  
**Description:** Use: Deal 5 damage to yourself to gain +3 Damage and +1 Magic Damage.  
**Source:** `trinkets.gon`  

```
BloodyRazor {
    name "ITEM_BLOODYRAZOR_NAME"
    desc "ITEM_BLOODYRAZOR_DESC"
    kind trinket
    rarity very_rare
    frame 270
	//set Bloody
    
    ability tk_BloodyRazor
}
```

---

### `ImmaculateHeart`
**Name:** Immaculate Heart  
**Description:** +2 Damage, +1 Magic Damage. Emit 3 Sparkles when you use your basic attack.  
**Source:** `trinkets.gon`  

```
ImmaculateHeart {
    name "ITEM_IMMACULATEHEART_NAME"
    desc "ITEM_IMMACULATEHEART_DESC"
    rarity very_rare
    kind trinket
    frame 246
    
    passives {
        DamageUp 2
		SpellDamageUp 1
        AddSelfStatusToBasicAttack {
            RandomMagicMissile 3
        }
    }
}
```

---

### `DybbuksRib`
**Name:** Dybbuk's Rib  
**Description:** Charm a random enemy at the start of each battle.  
**Source:** `trinkets.gon`  

```
DybbuksRib {
    name "ITEM_DYBBUKSRIB_NAME"
    desc "ITEM_DYBBUKSRIB_DESC"
    rarity very_rare
    kind trinket
    frame 273
	set Bone
	
	passives {
		StatusOnBattleStart {
			ForceUseAbility tk_DybbuksRib
		}
	}
}
```

---

### `SnakeEyes`
**Name:** Snake Eyes  
**Description:** While you are at exactly 2 HP, you have +222 [img:lck]  
**Source:** `trinkets.gon`  

```
SnakeEyes {
    name "ITEM_SNAKEEYES_NAME"
    desc "ITEM_SNAKEEYES_DESC"
    rarity rare
    kind trinket
    frame 274
    
    passives {
        PassiveAtHealthThreshold {
            threshold 2
            mode equal
            
            passives {
                LuckUp 222
            }
		}
    }
}
```

---

### `GreenWhistle`
**Name:** Green Whistle  
**Description:** Use: Summon a really big Leg.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
GreenWhistle {
    name "ITEM_GREENWHISTLE_NAME"
    desc "ITEM_GREENWHISTLE_DESC"
    rarity very_rare
    kind trinket
    frame 280
    
	ability tk_LegWhistle
}
```

---

### `MothersLove`
**Name:** Mother's Love  
**Description:** +6 Health Regen.  
**Source:** `trinkets.gon`  

```
MothersLove {
    name "ITEM_MOTHERSLOVE_NAME"
    desc "ITEM_MOTHERSLOVE_DESC"
    rarity very_rare
    kind trinket
    frame 281
	set Mother

	shield 6
    lck 6
    
    passives {
		HealthRegenUp 6
    }
}
```

---

### `PentagramSigil`
**Name:** Pentagram Sigil  
**Description:** Use: Take 5 damage and refresh your basic attack and movement actions.  
**Source:** `trinkets.gon`  

```
PentagramSigil {
    name "ITEM_PENTAGRAMSIGIL_NAME"
    desc "ITEM_PENTAGRAMSIGIL_DESC"
    rarity very_rare
    kind trinket
    frame 276
    cursed true
	set Demonic
    
    durability 5

    ability tk_Pentagram
}
```

---

### `LuciferSigil`
**Name:** Lucifer Sigil  
**Description:** Summon a Charmed Brute at the start of each battle.  
**Source:** `trinkets.gon`  

```
LuciferSigil {
    name "ITEM_LUCIFERSIGIL_NAME"
    desc "ITEM_LUCIFERSIGIL_DESC"
    rarity rare
    kind trinket
    frame 275
    cursed true
	set Demonic
    
    passives {
        SpawnOnBattleStart {
            object CharmedBigDemon
            number 1
        }
    }
}
```

---

### `HexagramSigil`
**Name:** Hexagram Sigil  
**Description:** +3 Magic Damage.
You are immune to buffs and debuffs.
When you die, you don't leave a corpse.  
**Source:** `trinkets.gon`  

```
HexagramSigil {
    name "ITEM_HEXAGRAMSIGIL_NAME"
    desc "ITEM_HEXAGRAMSIGIL_DESC"
    rarity rare
    kind trinket
    frame 284
	cursed true
	set Demonic
	
	str 3
	dex 3

    passives {
		SpellDamageUp 3
		DebuffImmunity 1

        BuffImmunity {
            exclude SpellDamageUp
        }

        AddCorpseHealth -999999
    }
}
```

---

### `ChupacabraTongue`
**Name:** Chupacabra Tongue  
**Description:** Your basic attack has Lifesteal.  
**Source:** `trinkets.gon`  

```
ChupacabraTongue {
    name "ITEM_CHUPACABRATONGUE_NAME"
    desc "ITEM_CHUPACABRATONGUE_DESC"
    rarity rare
    kind trinket
    frame 286
	set Guts
    
    passives {
		Lifesteal 1
    }
}
```

---

### `CharonsObal`
**Name:** Charon's Obol  
**Description:** +6 corpse health. Spawn a Charmed Reaper when you are downed.  
**Source:** `trinkets.gon`  

```
CharonsObal {
    name "ITEM_CHARONSOBAL_NAME"
    desc "ITEM_CHARONSOBAL_DESC"
    rarity very_rare
    kind trinket
    frame 287
	set Necromancer
    
    passives {
		SpawnThingOnDeath CharmedReaper
		AddCorpseHealth 6
    }
}
```

---

### `HumanHead`
**Name:** Human Head  
**Description:** ITEM_HUMANHEAD_DESC  
**Source:** `trinkets.gon`  

```
HumanHead {
    name "ITEM_HUMANHEAD_NAME"
    desc "ITEM_HUMANHEAD_DESC"
    rarity very_rare
    kind trinket
    frame 288
	set HumanFlesh
	
    str 1
	dex 1
	con 1
    int 1
	spd 1
	cha 1
	lck 1
}
```

---

### `Glitch`
**Name:** Glitch  
**Description:** Use: Scramble the last spell you used. Permanently.  
**Source:** `trinkets.gon`  

```
Glitch {
    name "ITEM_GLITCH_NAME"
    desc "ITEM_GLITCH_DESC"
    rarity rare
    kind trinket
    frame 289
    
    ability tk_Glitch
}
```

---

### `VideoGameCart`
**Name:** Video Game Cart  
**Description:** It's broken.  
**Source:** `trinkets.gon`  

```
VideoGameCart {//this item will have no effect till dlc.. figure it out later. 
    name "ITEM_VIDEOGAMECART_NAME"
    desc "ITEM_VIDEOGAMECART_DESC"
    rarity very_rare
    kind trinket
    frame 290
	set Used
    
    passives {

    }
}
```

---

### `TV`
**Name:** TV  
**Description:** Your bonus ability is Waste Time.  
**Source:** `trinkets.gon`  

```
TV {
    name "ITEM_TV_NAME"
    desc "ITEM_TV_DESC"
    rarity very_rare
    kind trinket
    frame 291
    
    passives {
		BonusAbility WasteTime
    }
}
```

---

### `Triachnid`
**Name:** Triachnid  
**Description:** Spawn Triachnid at the start of each battle.  
**Source:** `trinkets.gon`  

```
Triachnid {
    name "ITEM_TRIACHNID_NAME"
    desc "ITEM_TRIACHNID_DESC"
    rarity very_rare
    kind trinket
    frame 292
    
    passives {
        SpawnOnBattleStart {
            object Triachnid
            number 1
        }
    }
}
```

---

### `GallonOfWater`
**Name:** Gallon of Water  
**Description:** Use: Heal +5 HP and gain Heatwave immunity.
Refills when affected by Water Element effects.  
**Source:** `trinkets.gon`  

```
GallonOfWater {//todo make it become empty and you can throw it like bottles but with a big glass aoe and more damage.
    name "ITEM_GALLONOFWATER_NAME"
    desc "ITEM_GALLONOFWATER_DESC"
    kind trinket
    frame 293
    rarity rare

    durability 8
    max_durability 8
    dont_destroy_on_0 true

    ability tk_WaterBottle_Half

    passives {
        TransformItemOnElementInfluence {
            element Greater_Water
            item GallonOfWater
            full_repair true
        }
    }
}
```

---

### `ScorchedEarth`
**Name:** Scorched Earth  
**Description:** Your Earth and Fire Element spells cost -1 mana.  
**Source:** `trinkets.gon`  

```
ScorchedEarth {
    name "ITEM_SCORCHEDEARTH_NAME"
    desc "ITEM_SCORCHEDEARTH_DESC"
    rarity very_rare
    kind trinket
    frame 238
	set DirtClod
    
    passives {
        ElementalManaCostReduction {
            element [Fire Earth]
            reduction 1
        }
    }
}
```

---

### `LiquidMetal`
**Name:** Liquid Metal  
**Description:** +25% Dodge Chance.  
**Source:** `trinkets.gon`  

```
LiquidMetal {
    name "ITEM_LIQUIDMETAL_NAME"
    desc "ITEM_LIQUIDMETAL_DESC"
    rarity very_rare
    kind trinket
    frame 231
    
    passives {
		DodgeChance 25%
    }
}
```

---

### `StevenStone`
**Name:** Steven Stone  
**Description:** Your collarless spells cost -2 mana.  
**Source:** `trinkets.gon`  

```
StevenStone {
    name "ITEM_STEVENSTONE_NAME"
    desc "ITEM_STEVENSTONE_DESC"
    rarity very_rare
    kind trinket
    frame 232
	set Steven
	
	cha 2
    
    passives {
        ClassManaCostReduction {
			class Colorless
            reduction 2
        }
    }
}
```

---

### `StevenMarrow`
**Name:** Steven Marrow  
**Description:** Any [img:shield] you gain is increased by 4.  
**Source:** `trinkets.gon`  

```
StevenMarrow {
    name "ITEM_STEVENMARROW_NAME"
    desc "ITEM_STEVENMARROW_DESC"
    rarity very_rare
    kind trinket
    frame 233
	set Steven
    
	shield 4
	con -3
	
	passives {
		GainExtraShield 4
	}
}
```

---

### `StevenTrinket1`
**Name:** Steven  
**Description:** Your basic attack inflicts Slow and has a +10% chance to Freeze.
You can damage frozen units.  
**Source:** `trinkets.gon`  

```
StevenTrinket1 {
    name "ITEM_STEVENTRINKET1_NAME"
    desc "ITEM_STEVENTRINKET1_DESC"
    rarity very_rare
    kind trinket
    frame 234
	set Steven
    
    passives {
		FreezePiercing 1
        AddStatusToBasicAttack {
            Slow 1
			Freeze [1 .1]
        }
    }
}
```

---

### `StevenTrinket2`
**Name:** Steven  
**Description:** Your basic attack inflicts Confusion.  
**Source:** `trinkets.gon`  

```
StevenTrinket2 {
    name "ITEM_STEVENTRINKET2_NAME"
    desc "ITEM_STEVENTRINKET2_DESC"
    rarity very_rare
    kind trinket
    frame 236
	set Steven
    
    passives {
        AddStatusToBasicAttack {
            Confusion 1
        }
    }
}
```

---

### `NinnyStick`
**Name:** Ninny Stick  
**Description:** Reroll your other equipped items at the end of each battle.
You can reroll your options when you level up.  
**Source:** `trinkets.gon`  

```
NinnyStick {
    name "ITEM_NINNYSTICK_NAME"
    desc "ITEM_NINNYSTICK_DESC"
    rarity very_rare
    kind trinket
    frame 267
	set Jester
    
    passives {
        RerollItemsOnBattleEnd 1
        AddLevelUpRerolls 1
    }
}
```

---

### `SkillSplit`
**Name:** Skill Split  
**Description:** Gain a temporary copy of your first passive ability at the start of each battle.  
**Source:** `trinkets.gon`  

```
SkillSplit {
    name "ITEM_SKILLSPLIT_NAME"
    desc "ITEM_SKILLSPLIT_DESC"
    rarity very_rare
    kind trinket
    frame 269
    
    passives {
        CopyPassiveSlot 0
    }
}
```

---

### `FurnitureBox`
**Name:** Furniture Box  
**Description:** Breaks when [img:shield] is depleted.
Becomes a random piece of furniture when you return home.  
**Source:** `trinkets.gon`  

```
FurnitureBox {
    name "ITEM_FURNITUREBOX_NAME"
    desc "ITEM_FURNITUREBOX_DESC"
    rarity rare
    kind trinket
    frame 294
    on_store become_furniture

    spd -5
    shield 8

    passives {
        BreakWhenNoShield 1
    }
}
```

---

### `FurnitureBox_Rare`
**Name:** Rare Furniture Box  
**Description:** Breaks when [img:shield] is depleted.
Becomes a random piece of rare furniture when you return home.  
**Source:** `trinkets.gon`  

```
FurnitureBox_Rare {
    name "ITEM_FURNITUREBOX_RARE_NAME"
    desc "ITEM_FURNITUREBOX_RARE_DESC"
    rarity very_rare
    kind trinket
    frame 295
    on_store become_rare_furniture

    spd -5
    lck 5
    shield 4

    passives {
        BreakWhenNoShield 1
    }
}
```

---

### `Ankh`
**Name:** Ankh  
**Description:** While you're downed, you have a 50% chance to revive with 33% HP at the end of each round.  
**Source:** `trinkets.gon`  

```
Ankh {
    name "ITEM_ANKH_NAME"
    desc "ITEM_ANKH_DESC"
    rarity rare
    kind trinket
    frame 199

    passives {
        ChanceToRevive {
            stacks 50
            health 34%
        }
    }
}
```

---

### `TheBoxCardboard`
**Name:** The Box  
**Description:** Find an extra chapter item at the end of each battle.  
**Source:** `trinkets.gon`  

```
TheBoxCardboard {
    name "ITEM_THEBOXCARDBOARD_NAME"
    desc "ITEM_THEBOXCARDBOARD_DESC"
    rarity rare
    kind trinket
    frame 296
	set Cardboard

    passives {
	    StatusOnBattleEnd {
            FindItemFromPool chapter_specific_item
        }
    }
}
```

---

### `TheBoxChest`
**Name:** The bOx  
**Description:** Use: Spawn A lost Spirit. This gains +1 use whenever an allied cat dies.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
TheBoxChest {
    name "ITEM_THEBOXCHEST_NAME"
    desc "ITEM_THEBOXCHEST_DESC"
    rarity rare
    kind trinket
    frame 297
	set Wood

    durability 1
    max_durability 4
    dont_destroy_on_0 true

    passives {
        StatusOnAllyCatDeath {
            RepairTrinket 1
        }
    }
    
	ability tk_SpawnTheLost
}
```

---

### `TheBox`
**Name:** The boX  
**Description:** Use: Revive all bodies, fully heal all units, and clear all status effects.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `trinkets.gon`  

```
TheBox {
    name "ITEM_THEBOX_NAME"
    desc "ITEM_THEBOX_DESC"
    rarity rare
    kind trinket
    frame 298
	set Steven
	
	durability 4

	ability tk_Reset
}
```

---

### `TheBlackBox`
**Name:** the box  
**Description:** Use: Find and equip a random item into one of your empty item slots.  
**Source:** `trinkets.gon`  

```
TheBlackBox {
    name "ITEM_THEBLACKBOX_NAME"
    desc "ITEM_THEBLACKBOX_DESC"
    rarity very_rare
    kind trinket
    frame 300
	set Steven

	ability tk_TheBlackBox
}
```

---

### `SkullOfGlorg`
**Name:** Skull Of Glorg  
**Description:** Your spells cost -1 mana for each parasite you have equipped.  
**Source:** `trinkets.gon`  

```
SkullOfGlorg {
    name "ITEM_SKULLOFGLORG_NAME"
    desc "ITEM_SKULLOFGLORG_DESC"
    rarity rare
    kind trinket
    frame 299
	parasite true
	set Bone

    passives {
		ReduceSpellCostsPerParasite 1
    }
}
```

---

## File: `weapons.gon`

### `GlassShard`
**Name:** Shard of Glass  
**Description:** Use: A melee attack that inflicts Bleed.  
**Source:** `weapons.gon`  

```
GlassShard {
    name "ITEM_SHARDOFGLASS_NAME"
    desc "ITEM_SHARDOFGLASS_DESC"
    rarity common
    kind weapon
    frame 2
    durability [7, 12]
    
    ability wp_GlassShard
}
```

---

### `TinkererGlassShard`
**Source:** `weapons.gon`  

```
TinkererGlassShard {
    variant_of GlassShard
    durability [4 9]
}
```

---

### `RailSpikes`
**Name:** Railroad Spikes  
**Description:** Use: A ranged attack.  
**Source:** `weapons.gon`  

```
RailSpikes {
    name "ITEM_RAILROADSPIKE_NAME"
    desc "ITEM_RAILROADSPIKE_DESC"
    rarity common
    kind weapon
    frame 3
    durability 8
	set Lead
    
    ability wp_RailSpikes
}
```

---

### `NailBoard`
**Name:** Nail Board  
**Description:** Use: A wide melee attack.  
**Source:** `weapons.gon`  

```
NailBoard {
    name "ITEM_NAILBOARD_NAME" 
    desc "ITEM_NAILBOARD_DESC" 
    rarity uncommon
    kind weapon
    frame 4
    durability 4
	set Wood
    
    ability wp_NailBoard 
}
```

---

### `LilSlugger`
**Name:** Lil' Slugger  
**Description:** Use: Knock back a unit 5 tiles.  
**Source:** `weapons.gon`  

```
LilSlugger {
    name "ITEM_LILSLUGGER_NAME"
    desc "ITEM_LILSLUGGER_DESC"
    rarity common
    kind weapon
    frame 1
	set Wood

    
    ability wp_LilSlugger
}
```

---

### `ChumBucket`
**Name:** Chum Bucket  
**Description:** Use: A lobbed attack that creates a creep puddle.  
**Source:** `weapons.gon`  

```
ChumBucket {
    name "ITEM_CHUMBUCKET_NAME"
    desc "ITEM_CHUMBUCKET_DESC"
    rarity common
    kind weapon
    frame 5
    durability 6
	set [Guts, Meat]
    
    ability wp_ChumBucket
}
```

---

### `MeatHook`
**Name:** Meat Hook  
**Description:** Use: Pull a unit toward you.  
**Source:** `weapons.gon`  

```
MeatHook {
    name "ITEM_MEATHOOK_NAME"
    desc "ITEM_MEATHOOKTEMP_DESC"
    rarity rare
    kind weapon
    frame 6
	set [Barbed, Butcher]
    
    ability wp_MeatHook
}
```

---

### `Kebab`
**Name:** Kebab  
**Description:** Use: A melee attack with +1 reach that penetrates through units.  
**Source:** `weapons.gon`  

```
Kebab {
    name "ITEM_KEBAB_NAME"
    desc "ITEM_KEBAB_DESC"
    rarity uncommon
    kind weapon
    frame 7
    durability 8
    
    ability wp_Kebab
}
```

---

### `Pipe`
**Name:** Pipe  
**Description:** Use: A melee attack with a 10% chance to inflict Stun.  
**Source:** `weapons.gon`  

```
Pipe {
    name "ITEM_PIPE_NAME"
    desc "ITEM_PIPE_DESC"
    rarity uncommon
    kind weapon
    frame 8
	set Lead
    
    ability wp_Pipe
}
```

---

### `ObsidianChunk`
**Name:** Obsidian Chunk  
**Description:** Use: A melee attack.
This weapon gains +2 damage each time it's used.
Damage resets at the end of the adventure.  
**Source:** `weapons.gon`  

```
ObsidianChunk {
    name "ITEM_OBSIDIANCHUNK_NAME"
    desc "ITEM_OBSIDIANCHUNK_DESC"
    rarity rare
    kind weapon
    frame 9
    durability 9
    aux 1
	set Obelisk
    
    reset_aux_on_store 1

    ability wp_ObsidianChunk
}
```

---

### `SoulClaw`
**Name:** Soul Claw  
**Description:** Use: A melee attack that deals damage equal to the number of uses this has left.
When this weapon kills a unit, it gains +2 uses.  
**Source:** `weapons.gon`  

```
SoulClaw {
    name "ITEM_SOULCLAW_NAME"
    desc "ITEM_SOULCLAW_DESC"
    rarity rare
    kind weapon
    frame 10
    durability 7
	set Demonic
    
    ability wp_SoulClaw
}
```

---

### `Bomb`
**Name:** Bomb  
**Description:** Use: Throw a bomb that explodes.  
**Source:** `weapons.gon`  

```
Bomb {
    name "ITEM_BOMB_NAME"
    desc "ITEM_BOMB_DESC"
    rarity uncommon
    kind weapon
    frame 11
    durability 1
    
    ability wp_Bomb
}
```

---

### `BoneClub`
**Name:** Bone Club  
**Description:** Use: A melee attack.
This weapon has a 15% chance to break each time it's used.  
**Source:** `weapons.gon`  

```
BoneClub {
    name "ITEM_BONECLUB_NAME"
    desc "ITEM_BONECLUB_DESC"
    rarity uncommon
    kind weapon
    frame 13
	set Bone
    
    ability wp_BoneClub
}
```

---

### `Molars`
**Name:** Molars  
**Description:** Use: A low-damage lobbed attack.  
**Source:** `weapons.gon`  

```
Molars {
    name "ITEM_MOLAR_NAME"
    desc "ITEM_MOLAR_DESC"
    rarity common
    kind weapon
    frame 14
    durability [10 20]
	set Bone
    
    ability wp_Molars
}
```

---

### `Whetstone`
**Name:** Whetstone  
**Description:** Use: Gain +1 Damage for the rest of the battle.  
**Source:** `weapons.gon`  

```
Whetstone {
    name "ITEM_WHETSTONE_NAME"
    desc "ITEM_WHETSTONE_DESC"
    rarity rare
    kind weapon
    frame 15
	set Rock
    
    ability wp_Whetstone
}
```

---

### `Hairspray`
**Name:** Modded Hairspray  
**Description:** Use: Deal fire damage in a cone.  
**Source:** `weapons.gon`  

```
Hairspray {
    name "ITEM_MODDEDHAIRSPRAY_NAME"
    desc "ITEM_MODDEDHAIRSPRAY_DESC"
    rarity uncommon
    kind weapon
    frame 25
    durability [8 12]
    
    ability wp_HairSpray
}
```

---

### `Lighter`
**Name:** Lighter  
**Description:** Use: Inflict Burn 1 on an adjacent unit.  
**Source:** `weapons.gon`  

```
Lighter {
    name "ITEM_LIGHTER_NAME"
    desc "ITEM_LIGHTER_DESC"
    rarity common
    kind weapon
    frame 26
    durability [8 12]
	set Cool
    
    ability wp_Lighter
}
```

---

### `SeedBombs`
**Name:** Seed Bombs  
**Description:** Use: A lobbed projectile that spawns tall grass.  
**Source:** `weapons.gon`  

```
SeedBombs {
    name "ITEM_SEEDBOMBS_NAME"
    desc "ITEM_SEEDBOMBS_DESC"
    rarity uncommon
    kind weapon
    frame 27
    
    ability wp_SeedBomb
}
```

---

### `Battery`
**Name:** Battery  
**Description:** Use: A ranged lightning attack with a 10% chance to Stun.  
**Source:** `weapons.gon`  

```
Battery {
    name "ITEM_BATTERY_NAME"
    desc "ITEM_BATTERY_DESC"
    rarity uncommon
    kind weapon
    frame 30
    durability [3 6]
    
    ability wp_Battery
}
```

---

### `TinkererBattery`
**Source:** `weapons.gon`  

```
TinkererBattery {
    variant_of Battery
    durability [2 3]
}
```

---

### `OldHose`
**Name:** Old Hose  
**Description:** Use: A water attack that hits an entire line with Knockback 1.  
**Source:** `weapons.gon`  

```
OldHose {
    name "ITEM_OLDHOSE_NAME"
    desc "ITEM_OLDHOSE_DESC"
    rarity common
    kind weapon
    frame 31
	set Rubber
    
    ability wp_Hose
}
```

---

### `SixPack`
**Name:** Six Pack  
**Description:** Use: A lobbed water attack that deals splash damage.  
**Source:** `weapons.gon`  

```
SixPack {
    name "ITEM_SIXPACK_NAME"
    desc "ITEM_SIXPACK_DESC"
    rarity uncommon
    kind weapon
    frame 32
    durability 6
    
    ability wp_SixPack
}
```

---

### `IceCubes`
**Name:** Ice Cubes  
**Description:** Use: A lobbed attack that Freezes units.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IceCubes {
    name "ITEM_ICECUBES_NAME"
    desc "ITEM_ICECUBES_DESC"
    rarity uncommon
    kind weapon
    frame 35
	set Frozen
    
    ability wp_IceCubes
}
```

---

### `DryIce`
**Name:** Dry Ice  
**Description:** Use: An Ice Element melee attack that inflicts Slow.  
**Source:** `weapons.gon`  

```
DryIce {
    name "ITEM_DRYICE_NAME"
    desc "ITEM_DRYICE_DESC"
    rarity uncommon
    kind weapon
    frame 36
	set Frozen
    
    ability wp_DryIce
}
```

---

### `Bottles`
**Name:** Bottles  
**Description:** Use: A lobbed attack that spawns a glass tile.  
**Source:** `weapons.gon`  

```
Bottles {
    name "ITEM_BOTTLES_NAME"
    desc "ITEM_BOTTLES_DESC"
    rarity common
    kind weapon
    frame 17
    durability 6

    ability wp_Bottles
}
```

---

### `TinkererBottles`
**Source:** `weapons.gon`  

```
TinkererBottles {
    variant_of Bottles
    durability 4
}
```

---

### `Stick`
**Name:** Stick  
**Description:** Use: A melee attack with +1 reach.  
**Source:** `weapons.gon`  

```
Stick {
    name "ITEM_STICK_NAME"
    desc "ITEM_STICK_DESC"
    rarity common
    kind weapon
    frame 16
    durability 4
	set Wood

    ability wp_Stick
}
```

---

### `TinkererStick`
**Source:** `weapons.gon`  

```
TinkererStick {
    variant_of Stick
    durability [2 4]
}
```

---

### `TutorialStick`
**Source:** `weapons.gon`  

```
TutorialStick {
    variant_of Stick
    durability 4
}
```

---

### `RubberFist`
**Name:** Rubber Fist  
**Description:** Use: A melee attack with Knockback 1 that inflicts Confusion.  
**Source:** `weapons.gon`  

```
RubberFist {
    name "ITEM_RUBBERFIST_NAME"
    desc "ITEM_RUBBERFIST_DESC" 
    rarity uncommon
    kind weapon
    frame 19
	set Rubber

    ability wp_RubberFist
}
```

---

### `BarbedPaw`
**Name:** Barbed Paw  
**Description:** Use: A melee attack that inflicts Bleed 1.
Passive: +1 Thorns.  
**Source:** `weapons.gon`  

```
BarbedPaw {
    name "ITEM_BARBEDPAW_NAME"
    desc "ITEM_BARBEDPAW_DESC" 
    rarity uncommon
    kind weapon
    frame 24
	set Barbed

    con -1

    passives {
        Thorns 1
    }

    ability wp_BarbedPaw
}
```

---

### `GnarledClaw`
**Name:** Gnarled Claw  
**Description:** Use: A melee attack.
This weapon gains +1 damage and +1 use when it gets a kill.
Damage resets at the end of the adventure.  
**Source:** `weapons.gon`  

```
GnarledClaw {
    name "ITEM_GNARLEDCLAW_NAME"
    desc "ITEM_GNARLEDCLAW_DESC"
    rarity rare
    kind weapon
    frame 21
    aux 1
    durability 13

    reset_aux_on_store 1

    ability wp_GnarledClaw
}
```

---

### `Garbage`
**Name:** Garbage  
**Description:** Use: A lobbed attack that inflicts Poison 1.  
**Source:** `weapons.gon`  

```
Garbage {
    name "ITEM_GARBAGE_NAME"
    desc "ITEM_GARBAGE_DESC"
    kind weapon
    frame 39
    durability 1
	set Recycled
	
    ability wp_Garbage
}
```

---

### `Shotgun`
**Name:** Shotgun  
**Description:** Use: Fires 5 projectiles in a cone.  
**Source:** `weapons.gon`  

```
Shotgun {
    name "ITEM_SHOTGUN_NAME"
    desc "ITEM_SHOTGUN_DESC"
    rarity very_rare
    kind weapon
    frame 50
    durability 2

    ability wp_Shotgun
}
```

---

### `Revolver`
**Name:** Revolver  
**Description:** Use: Fire a shot in a straight line that instakills units and deals 25 damage to bosses.  
**Source:** `weapons.gon`  

```
Revolver {
    name "ITEM_REVOLVER_NAME"
    desc "ITEM_REVOLVER_DESC"
    rarity very_rare
    kind weapon
    frame 51
    durability 6

    ability wp_Revolver
}
```

---

### `Sniper`
**Name:** Sniper Rifle  
**Description:** Use: Fire a shot that instakills units and deals 25 damage to bosses.  
**Source:** `weapons.gon`  

```
Sniper {
    name "ITEM_SNIPERRIFLE_NAME"
    desc "ITEM_SNIPERRIFLE_DESC"
    rarity very_rare
    kind weapon
    frame 52
    durability [2 4]

    ability wp_Sniper
}
```

---

### `SmallBomb`
**Name:** Small Bomb  
**Description:** Use: Throw a bomb that explodes.  
**Source:** `weapons.gon`  

```
SmallBomb {
    name "ITEM_SMALLBOMB_NAME"
    desc "ITEM_SMALLBOMB_DESC"
    rarity common
    kind weapon
    frame 74
    durability 1
    
    ability wp_SmallBomb
}
```

---

### `PogoStick`
**Name:** Pogo Stick  
**Description:** Use: Jump to a tile and damage units you land on.  
**Source:** `weapons.gon`  

```
PogoStick {
    name "ITEM_POGOSTICK_NAME"
    desc "ITEM_POGOSTICK_DESC"
    rarity uncommon
    kind weapon
    frame 72
    durability [3 7]
    
    ability wp_PogoStick
}
```

---

### `Spitball`
**Name:** Spitball  
**Description:** Use: A ranged attack that inflicts Slow.  
**Source:** `weapons.gon`  

```
Spitball {
    name "ITEM_SPITBALL_NAME"
    desc "ITEM_SPITBALL_DESC"
    rarity uncommon
    kind weapon
    frame 73
    durability [4 8]
    
    ability wp_Spitball
}
```

---

### `MiniJetpack`
**Name:** Mini Jetpack  
**Description:** Use: Fly to a random tile within a target area. If you land on a unit, explode dealing 5 damage in an area (including to yourself).  
**Source:** `weapons.gon`  

```
MiniJetpack {
    name "ITEM_MINIJETPACK_NAME"
    desc "ITEM_MINIJETPACK_DESC"
    rarity rare
    kind weapon
    frame 77
    durability [3 6]
	set Experimental
    
    ability wp_MiniJetpack
}
```

---

### `BigStick`
**Name:** Big Stick  
**Description:** Use: A melee attack with +2 reach.  
**Source:** `weapons.gon`  

```
BigStick {
    name "ITEM_BIGSTICK_NAME"
    desc "ITEM_BIGSTICK_DESC"
    rarity uncommon
    kind weapon
    frame 75
    durability [8 12]
	set Wood
    
    ability wp_BigStick
}
```

---

### `TinkererBigStick`
**Source:** `weapons.gon`  

```
TinkererBigStick {
    variant_of BigStick
    durability [5 8]
}
```

---

### `BiggestStick`
**Name:** Biggest Stick  
**Description:** Use: A melee attack with +3 reach.  
**Source:** `weapons.gon`  

```
BiggestStick {
    name "ITEM_BIGGESTSTICK_NAME"
    desc "ITEM_BIGGESTSTICK_DESC"
    rarity rare
    kind weapon
    frame 82
    durability [8 12]
	set Wood
    
    ability wp_BiggestStick
}
```

---

### `TinkererBiggestStick`
**Source:** `weapons.gon`  

```
TinkererBiggestStick {
    variant_of BiggestStick
    durability [5 8]
}
```

---

### `Log`
**Name:** Log  
**Description:** Use: A wide attack that hits all units in an area.  
**Source:** `weapons.gon`  

```
Log {
    name "ITEM_LOG_NAME"
    desc "ITEM_LOG_DESC"
    rarity very_rare
    kind weapon
    frame 76
    durability 8
	set Wood
    
    ability wp_Log
}
```

---

### `TinkererLog`
**Source:** `weapons.gon`  

```
TinkererLog {
    variant_of Log
    durability 4
}
```

---

### `Taser`
**Name:** Zapper  
**Description:** Use: A ranged electric attack that inflicts Stun.  
**Source:** `weapons.gon`  

```
Taser {
    name "ITEM_TASER_NAME"
    desc "ITEM_TASER_DESC"
    rarity rare
    kind weapon
    frame 84
    durability 4
    
    ability wp_Taser
}
```

---

### `TinkererTaser`
**Source:** `weapons.gon`  

```
TinkererTaser {
    variant_of Taser
    durability 3
}
```

---

### `Deathbot`
**Name:** Deathbot  
**Description:** Use: Spawn a Deathbot with a flamethrower.  
**Source:** `weapons.gon`  

```
Deathbot {
    name "ITEM_DEATHBOT_NAME"
    desc "ITEM_DEATHBOT_DESC"
    rarity rare
    kind weapon
    frame 81
    durability 1
	set Tinkerer
    
    ability wp_Deathbot
}
```

---

### `Crossbow`
**Name:** Crossbow  
**Description:** Use: A ranged attack that ignores shield and inflicts Bleed 1.  
**Source:** `weapons.gon`  

```
Crossbow {
    name "ITEM_CROSSBOW_NAME"
    desc "ITEM_CROSSBOW_DESC"
    rarity rare
    kind weapon
    frame 80
    durability 6
	set Wood
    
    ability wp_Crossbow
}
```

---

### `TinkererCrossbow`
**Source:** `weapons.gon`  

```
TinkererCrossbow {
    variant_of Crossbow
    durability 4
}
```

---

### `BucketOfAcid`
**Name:** Vial of Acid  
**Description:** Use: A melee attack that inflicts random status effects.  
**Source:** `weapons.gon`  

```
BucketOfAcid {
    name "ITEM_BUCKETOFACID_NAME"
    desc "ITEM_BUCKETOFACID_DESC"
    rarity rare
    kind weapon
    frame 78
    durability 1
    
    ability wp_BucketOfAcid
}
```

---

### `StunGun`
**Name:** Stun Gun  
**Description:** Use: An electric melee attack with a 50% chance to inflict Stun.  
**Source:** `weapons.gon`  

```
StunGun {
    name "ITEM_STUNGUN_NAME"
    desc "ITEM_STUNGUN_DESC"
    rarity uncommon
    kind weapon
    frame 79
    durability [2 4]
    
    ability wp_StunGun
}
```

---

### `SlingShot`
**Name:** Slingshot  
**Description:** Use: A ranged attack with a 33% chance to inflict Blind 2.  
**Source:** `weapons.gon`  

```
SlingShot {
    name "ITEM_SLINGSHOT_NAME"
    desc "ITEM_SLINGSHOT_DESC"
    rarity uncommon
    kind weapon
    frame 83
    durability [5 9]
	set Wood
    
    ability wp_SlingShot
}
```

---

### `TinkererSlingShot`
**Source:** `weapons.gon`  

```
TinkererSlingShot {
    variant_of SlingShot
    durability [4 7]
}
```

---

### `Uzi`
**Name:** Submachine Gun  
**Description:** Use: Fire 5 shots in a straight line.  
**Source:** `weapons.gon`  

```
Uzi {
    name "ITEM_UZI_NAME"
    desc "ITEM_UZI_DESC"
    rarity rare
    kind weapon
    frame 137
    durability 3

    ability wp_Uzi
}
```

---

### `durability`
**Source:** `weapons.gon`  

```
durability [2 4]
```

---

### `BagOfRocks`
**Name:** Bag of Rocks  
**Description:** Use: A melee attack that inflicts Bruise.  
**Source:** `weapons.gon`  

```
BagOfRocks {
    name "ITEM_BAGOFROCKS_NAME"
    desc "ITEM_BAGOFROCKS_DESC"
    rarity rare
    kind weapon
    frame 86
	set Rock

    ability wp_BagOfRocks
}
```

---

### `Textbook`
**Name:** Textbook  
**Description:** Use: Gain +1 [img:int] for the rest of the battle.  
**Source:** `weapons.gon`  

```
Textbook {
    name "ITEM_TEXTBOOK_NAME"
    desc "ITEM_TEXTBOOK_DESC"
    rarity rare
    kind weapon
    frame 90
	set Paper

    ability wp_Textbook
}
```

---

### `BucketOfLard`
**Name:** Bucket of Lard  
**Description:** Use: Gain +2 [img:con] and -1 [img:spd], then heal 4 HP.  
**Source:** `weapons.gon`  

```
BucketOfLard {
    name "ITEM_BUCKETOFLARD_NAME"
    desc "ITEM_BUCKETOFLARD_DESC"
    rarity uncommon
    kind weapon
    frame 91
    durability [4 7]
	set Fatty

    ability wp_BucketOfLard
}
```

---

### `NailGun`
**Name:** Nail Gun  
**Description:** Use: Fire a shot in a straight line that inflicts +1 Thorns.  
**Source:** `weapons.gon`  

```
NailGun {
    name "ITEM_NAILGUN_NAME"
    desc "ITEM_NAILGUN_DESC"
    rarity uncommon
    kind weapon
    frame 92

    ability wp_NailGun
}
```

---

### `StrongMagnet`
**Name:** Strong Magnet  
**Description:** Use: Pull a unit 2 tiles toward you.  
**Source:** `weapons.gon`  

```
StrongMagnet {
    name "ITEM_STRONGMAGNET_NAME"
    desc "ITEM_STRONGMAGNET_DESC"
    rarity uncommon
    kind weapon
    frame 93

    ability wp_StrongMagnet
}
```

---

### `SawBlades`
**Name:** Sawblades  
**Description:** Use: Throw a blade in a straight line that inflicts Bleed 1 and passes through units.  
**Source:** `weapons.gon`  

```
SawBlades {
    name "ITEM_SAWBLADES_NAME"
    desc "ITEM_SAWBLADES_DESC"
    rarity rare
    kind weapon
    frame 94
    durability [9 16]

    ability wp_SawBlades
}
```

---

### `OddRemote`
**Name:** Odd Remote  
**Description:** Use: Cast a random spell.  
**Source:** `weapons.gon`  

```
OddRemote {
    name "ITEM_ODDREMOTE_NAME"
    desc "ITEM_ODDREMOTE_DESC" 
    rarity uncommon
    kind weapon
    frame 95
	durability [6 8]
	set Experimental

    ability wp_OddRemote
}
```

---

### `ButterflyKnife`
**Name:** Butterfly Knife  
**Description:** Use: A multi-hit melee attack that inflicts Bleed.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
ButterflyKnife {
    name "ITEM_BUTTERFLYKNIFE_NAME"
    desc "ITEM_BUTTERFLYKNIFE_DESC" 
    rarity rare
    kind weapon
    frame 97
	set Cool

    ability wp_ButterflyKnife
}
```

---

### `BearTraps`
**Name:** Bear Traps  
**Description:** Use: Place a Bear Trap.  
**Source:** `weapons.gon`  

```
BearTraps {
    name "ITEM_BEARTRAPS_NAME"
    desc "ITEM_BEARTRAPS_DESC"
    rarity uncommon
    kind weapon
    frame 99
    durability 6
	set [Hunter, Survivalist]

    ability wp_BearTraps
}
```

---

### `RustyRazor`
**Name:** Rusty Razor  
**Description:** Use: A melee attack that inflicts Poison 1 and Bleed 1.  
**Source:** `weapons.gon`  

```
RustyRazor {
    name "ITEM_RUSTYRAZOR_NAME"
    desc "ITEM_RUSTYRAZOR_DESC"
    rarity uncommon
    kind weapon
    frame 89
    durability [6 9]

    ability wp_RustyRazor
}
```

---

### `Bricks`
**Name:** Bricks  
**Description:** Use: A lobbed attack that inflicts Stun.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
Bricks {
    name "ITEM_BRICKS_NAME"
    desc "ITEM_BRICKS_DESC" 
    rarity rare
    kind weapon
    frame 18
	set Brick

    ability wp_Bricks
}
```

---

### `Mjolnir`
**Name:** Mjolnir  
**Description:** Use: A ranged attack that passes through units and returns to you after you throw it. At its apex, it deals electric damage.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
Mjolnir {
    name "ITEM_MJOLNIR_NAME"
    desc "ITEM_MJOLNIR_DESC"
    rarity very_rare
    kind weapon
    frame 12
	set Superhero
    
    ability wp_Mjolnir
}
```

---

### `Blackjack`
**Name:** Blackjack  
**Description:** Use: A melee attack with a 5% chance to Stun.
Automatically use this when you stop next to an enemy or an enemy stops next to you.  
**Source:** `weapons.gon`  

```
Blackjack {
    name "ITEM_BLACKJACK_NAME"
    desc "ITEM_BLACKJACK_DESC"
    rarity uncommon
    kind weapon
    frame 85
	set [Thief, Prowler]

    ability wp_Blackjack
    passives {
        MovementReaction {
            ability wp_Blackjack_Auto
            enemies_only true
            on_self_move_too true
            create_temp_ability true
        }
    }
}
```

---

### `BigSpring`
**Name:** Big Spring  
**Description:** Use: Throw an adjacent unit to a tile.  
**Source:** `weapons.gon`  

```
BigSpring {
    name "ITEM_BIGSPRING_NAME"
    desc "ITEM_BIGSPRING_DESC"
    rarity uncommon
    kind weapon
    frame 87
	set Scrap

    ability wp_BigSpring
}
```

---

### `Grenade`
**Name:** Grenade  
**Description:** Use: Throw a grenade that explodes and shreds 5 stacks of random buffs off of whatever it hits.  
**Source:** `weapons.gon`  

```
Grenade {
    name "ITEM_GRENADE_NAME"
    desc "ITEM_GRENADE_DESC"
    rarity rare
    kind weapon
    frame 98
    durability 1

    ability wp_Grenade
}
```

---

### `Pinwheel`
**Name:** Pinwheel  
**Description:** Use: A melee wind attack with Knockback 1.
Can be used 3 times per turn.  
**Source:** `weapons.gon`  

```
Pinwheel {
    name "ITEM_PINWHEEL_NAME"
    desc "ITEM_PINWHEEL_DESC"
    rarity common
    kind weapon
    frame 34
    durability [10 16]
	set Paper

    ability wp_Pinwheel
    passives {
        ExtraWeaponAttacks 2
    }
}
```

---

### `CrispPaper`
**Name:** Crisp Paper  
**Description:** Use: A ranged attack that inflicts Bleed 3.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
CrispPaper {
    name "ITEM_CRISPPAPER_NAME"
    desc "ITEM_CRISPPAPER_DESC"
    rarity uncommon
    kind weapon
    frame 56
	set Paper

    ability wp_CrispPaper
}
```

---

### `PurpleMushroom`
**Name:** Purple Mushroom  
**Description:** Use: A ranged attack that inflicts Confusion 2.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
PurpleMushroom {
    name "ITEM_PURPLEMUSHROOM_NAME"
    desc "ITEM_PURPLEMUSHROOM_DESC"
    rarity common
    kind weapon
    frame 57
    durability [2 4]
	set Druid

    ability wp_PurpleMushroom
}
```

---

### `BlackMushroom`
**Name:** Black Mushroom  
**Description:** Use: A ranged attack that inflicts Weakness 2.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
BlackMushroom {
    name "ITEM_BLACKMUSHROOM_NAME"
    desc "ITEM_BLACKMUSHROOM_DESC"
    rarity common
    kind weapon
    frame 58
	set Druid

    ability wp_BlackMushroom
}
```

---

### `RedMushroom`
**Name:** Red Mushroom  
**Description:** Use: A ranged attack that inflicts Charm 3.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
RedMushroom {
    name "ITEM_REDMUSHROOM_NAME"
    desc "ITEM_REDMUSHROOM_DESC"
    rarity rare
    kind weapon
    frame 59
	set Druid

    ability wp_RedMushroom
}
```

---

### `PoisonVial`
**Name:** Les Toxin  
**Description:** Use: A ranged attack that inflicts Poison 2.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
PoisonVial {
    name "ITEM_POISONVIAL_NAME"
    desc "ITEM_POISONVIAL_DESC"
    rarity common
    kind weapon
    frame 60
	set Thief

    ability wp_PoisonVial
}
```

---

### `PopCap`
**Name:** Pop Cap  
**Description:** Use: A lobbed attack with Knockback 1.  
**Source:** `weapons.gon`  

```
PopCap {
    name "ITEM_POPCAP_NAME"
    desc "ITEM_POPCAP_DESC"
    rarity common
    kind weapon
    frame 42
    durability [6 10]

    ability wp_PopCap
}
```

---

### `CreepyPhoto`
**Name:** Creepy Photo  
**Description:** Use: A melee attack that inflicts Fear 1.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
CreepyPhoto {
    name "ITEM_CREEPYPHOTO_NAME"
    desc "ITEM_CREEPYPHOTO_DESC"
    rarity uncommon
    kind weapon
    frame 62

    ability wp_CreepyPhoto
}
```

---

### `FingerBone`
**Name:** Finger Bone  
**Description:** Use: A straight ranged attack that inflicts Immobile 3.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
FingerBone {
    name "ITEM_FINGERBONE_NAME"
    desc "ITEM_FINGERBONE_DESC"
    rarity rare
    kind weapon
    frame 63
	set Bone

    ability wp_FingerBone
}
```

---

### `SpringBoard`
**Name:** Spring Board  
**Description:** Use: A melee attack that lobs a unit back 3 tiles.  
**Source:** `weapons.gon`  

```
SpringBoard {
    name "ITEM_SPRINGBOARD_NAME"
    desc "ITEM_SPRINGBOARD_DESC"
    rarity common
    kind weapon
    frame 45
	set Wood

    ability wp_SpringBoard
}
```

---

### `Shovel`
**Name:** Shovel  
**Description:** Use: A melee attack that lobs a unit back 2 tiles and digs up a corpse.  
**Source:** `weapons.gon`  

```
Shovel {
    name "ITEM_SHOVEL_NAME"
    desc "ITEM_SHOVEL_DESC"
    rarity rare
    kind weapon
    frame 37

    ability wp_Shovel
}
```

---

### `Trowel`
**Name:** Trowel  
**Description:** Use: A melee attack with Knockback 1 that spawns a rock.  
**Source:** `weapons.gon`  

```
Trowel {
    name "ITEM_TROWEL_NAME"
    desc "ITEM_TROWEL_DESC"
    rarity common
    kind weapon
    frame 38
    durability [6 8]

    ability wp_Trowel
}
```

---

### `StaffOfFlame`
**Name:** Staff of Flame  
**Description:** Use: A fire attack that inflicts Burn 5.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
StaffOfFlame {
    name "ITEM_STAFFOFFLAME_NAME"
    desc "ITEM_STAFFOFFLAME_DESC"
    rarity rare
    kind weapon
    frame 139
	set Mage

    ability wp_StaffOfFlame
}
```

---

### `LacedNeedle`
**Name:** Laced Needle  
**Description:** Use: A melee attack that inflicts Poison 1.
Can be used 3 times per turn.  
**Source:** `weapons.gon`  

```
LacedNeedle {
    name "ITEM_LACEDNEEDLE_NAME"
    desc "ITEM_LACEDNEEDLE_DESC"
    rarity uncommon
    kind weapon
    frame 140
    durability [10 14]
	set Thief
    
    ability wp_LacedNeedle
    passives {
        ExtraWeaponAttacks 2
    }
}
```

---

### `BattleAxe`
**Name:** Battle Axe  
**Description:** Use: A melee spin attack.
This uses up both your movement and attack action.  
**Source:** `weapons.gon`  

```
BattleAxe {
    name "ITEM_BATTLEAXE_NAME"
    desc "ITEM_BATTLEAXE_DESC"
    rarity rare
    kind weapon
    frame 141
	set Fighter
    
    ability wp_BattleAxe
}
```

---

### `AnointingOil`
**Name:** Anointing Oil  
**Description:** Use: Cleanse debuffs from an adjacent unit or yourself.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
AnointingOil {
    name "ITEM_ANOINTINGOIL_NAME"
    desc "ITEM_ANOINTINGOIL_DESC"
    rarity rare
    kind weapon
    frame 142
	set Cleric
    
    ability wp_AnointingOil
}
```

---

### `Girder`
**Name:** Girder  
**Description:** Use: A melee attack with Knockback 10 and Chain Knockback.
\[s:.7\](Usable once per battle.)\[/s\]
Passive: +1 Brace while this weapon is usable.  
**Source:** `weapons.gon`  

```
Girder {
    name "ITEM_GIRDER_NAME"
    desc "ITEM_GIRDER_DESC"
    rarity rare
    kind weapon
    frame 143
	set Tank
    
    ability wp_Girder
    passives {
        PassiveIfWeaponIsUsable {
            Brace 1
        }
    }
}
```

---

### `InfinityArrow`
**Name:** Arrow of Infinity  
**Description:** Use: Your next basic attack has +5 range, +100% Crit Chance, ignores shield and can't miss.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
InfinityArrow {
    name "ITEM_INFINITYARROW_NAME"
    desc "ITEM_INFINITYARROW_DESC"
    rarity rare
    kind weapon
    frame 144
	set Hunter

    ability wp_InfinityArrow
    passives {
    }
}
```

---

### `BentSpoon`
**Name:** Bent Spoon  
**Description:** Use: Pull any unit 1 tile toward you and deal 1 damage to it.  
**Source:** `weapons.gon`  

```
BentSpoon {
    name "ITEM_BENTSPOON_NAME"
    desc "ITEM_BENTSPOON_DESC"
    rarity rare
    kind weapon
    frame 145
	set Psychic

    ability wp_BentSpoon
    passives {
    }
}
```

---

### `UnderworldStaff`
**Name:** Staff of the Underworld  
**Description:** Use: A melee attack with Knockback 1.
Passive: Start each battle with a Zombie Cat familiar.  
**Source:** `weapons.gon`  

```
UnderworldStaff {
    name "ITEM_UNDERWORLDSTAFF_NAME"
    desc "ITEM_UNDERWORLDSTAFF_DESC"
    rarity rare
    kind weapon
    frame 146
	set [Necromancer, Bone]

    ability wp_UnderworldStaff
    passives {
        SpawnOnBattleStart ZombieCatFamiliar
    }
}
```

---

### `Bo`
**Name:** Bo  
**Description:** Use: A melee attack. On hit, jump forward 2 tiles.  
**Source:** `weapons.gon`  

```
Bo {
    name "ITEM_BO_NAME"
    desc "ITEM_BO_DESC"
    rarity rare
    kind weapon
    frame 147
	set [Monk, Wood]

    ability wp_Bo
    passives {
    }
}
```

---

### `BallPeenHammer`
**Name:** Ball-Peen Hammer  
**Description:** Use: A melee attack. If used on an ally, give +1 use to all of their items instead of dealing damage.
5% chance to break when used to repair items.  
**Source:** `weapons.gon`  

```
BallPeenHammer {
    name "ITEM_BALLPEENHAMMER_NAME"
    desc "ITEM_BALLPEENHAMMER_DESC"
    rarity rare
    kind weapon
    frame 148
	set Tinkerer

    ability wp_BallPeenHammer
    passives {
    }
}
```

---

### `ButchersCleaver`
**Name:** Butcher's Cleaver  
**Description:** Use: A melee attack with Cleave that can hit diagonally.  
**Source:** `weapons.gon`  

```
ButchersCleaver {
    name "ITEM_BUTCHERSCLEAVER_NAME"
    desc "ITEM_BUTCHERSCLEAVER_DESC"
    rarity rare
    kind weapon
    frame 149
	set Butcher

    ability wp_ButchersCleaver
    passives {
    }
}
```

---

### `RainStaff`
**Name:** Rain Staff  
**Description:** Use: Spawn a large puddle of water anywhere.  
**Source:** `weapons.gon`  

```
RainStaff {
    name "ITEM_RAINSTAFF_NAME"
    desc "ITEM_RAINSTAFF_DESC"
    rarity rare
    kind weapon
    frame 150
	set [Druid, Wood]

    ability wp_RainStaff
    passives {
    }
}
```

---

### `LilKitty`
**Name:** Lil' Kitty  
**Description:** Use: Spawn a Flea familiar.  
**Source:** `weapons.gon`  

```
LilKitty {
    name "ITEM_LILKITTY_NAME"
    desc "ITEM_LILKITTY_DESC"
    rarity rare
    kind weapon
    frame 167
    
    ability wp_LilKitty
    passives {
    }
}
```

---

### `TractorBeam`
**Name:** Tractor Beam  
**Description:** Use: Pull a unit within 3 tiles all the way towards you. Requires line of sight.  
**Source:** `weapons.gon`  

```
TractorBeam {
    name "ITEM_TRACTORBEAM_NAME"
    desc "ITEM_TRACTORBEAM_DESC"
    rarity uncommon
    kind weapon
    frame 106
	set Space
    
    ability wp_TractorBeam
}
```

---

### `RollOfPennies`
**Name:** Roll of Pennies  
**Description:** Use: A weak melee attack that has a 50% chance to spawn a coin. 
5% chance to break when used.
Gain a lot of coins when it breaks.  
**Source:** `weapons.gon`  

```
RollOfPennies {
    name "ITEM_ROLLOFPENNIES_NAME"
    desc "ITEM_ROLLOFPENNIES_DESC"
    rarity uncommon
    kind weapon
    frame 107
    
    ability wp_RollOfPennies
    
    passives {
        StatusOnBreak {
            GainCoinsRange {
                min 30
                max 60
            }
        }
    }
}
```

---

### `GrapplingHook`
**Name:** Grappling Hook  
**Description:** Use: Pull yourself toward a unit or object.  
**Source:** `weapons.gon`  

```
GrapplingHook {
    name "ITEM_GRAPPLINGHOOK_NAME"
    desc "ITEM_GRAPPLINGHOOK_DESC"
    rarity rare
    kind weapon
    frame 108
	set [Barbed, Ninja]
    
    ability wp_GrapplingHook
}
```

---

### `Chainsaw`
**Name:** Chainsaw  
**Description:** Use: A multi-hit melee attack with a 25% chance to Cleave.
\[s:.7\](Usable once per battle.)\[/s\]
Passive: +2 Thorns.  
**Source:** `weapons.gon`  

```
Chainsaw {
    name "ITEM_CHAINSAW_NAME"
    desc "ITEM_CHAINSAW_DESC"
    rarity rare
    kind weapon
    frame 109
	set Cool
    
    equip_sound SE_CatWeaponPoke_Chainsaw

    ability wp_Chainsaw
    passives {
        Thorns 2
    }
}
```

---

### `BurningCoal`
**Name:** Burning Coals  
**Description:** Use: A lobbed attack that inflicts Burn 2 and +2 [img:spd].
Passive: Gain Burn 1 and +2 [img:spd] at the start of each turn.  
**Source:** `weapons.gon`  

```
BurningCoal {
    name "ITEM_BURNINGCOAL_NAME"
    desc "ITEM_BURNINGCOAL_DESC"
    rarity rare
    kind weapon
    frame 69
	set Molten
    
    ability wp_BurningCoal
    passives {
        StatusEachTurnBegin {
            Burn 1
			SpeedUp 2
        }
    }
}
```

---

### `RainbowRemote`
**Name:** Rainbow Remote  
**Description:** Use: Cast a targeted random spell.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
RainbowRemote {
    name "ITEM_RAINBOWREMOTE_NAME"
    desc "ITEM_RAINBOWREMOTE_DESC"
    rarity rare
    kind weapon
    frame 66
	set Experimental
    
    ability wp_RainbowRemote
}
```

---

### `RubberBat`
**Name:** Rubber Bat  
**Description:** Use: A melee attack that inflicts Confusion 1 and turns the unit to the right.  
**Source:** `weapons.gon`  

```
RubberBat {
    name "ITEM_RUBBERBAT_NAME"
    desc "ITEM_RUBBERBAT_DESC"
    rarity uncommon
    kind weapon
    frame 40
    set Rubber
	
    ability wp_RubberBat
}
```

---

### `RustedRod`
**Name:** Rusted Rod  
**Description:** Use: A melee attack with damage equal to uses.  
**Source:** `weapons.gon`  

```
RustedRod {
    name "ITEM_RUSTEDROD_NAME"
    desc "ITEM_RUSTEDROD_DESC"
    rarity uncommon
    kind weapon
    frame 41
    durability 9
    
    ability wp_RustedRod
}
```

---

### `MeatCleaver`
**Name:** Meat Cleaver  
**Description:** Use: A melee attack with Cleave that deals damage equal to half the target's current HP.
Bosses take 1/6th of their current HP in damage instead.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
MeatCleaver {
    name "ITEM_MEATCLEAVER_NAME"
    desc "ITEM_MEATCLEAVER_DESC"
    rarity rare
    kind weapon
    frame 43
	set Butcher
    
    ability wp_MeatCleaver
}
```

---

### `SharpStraw`
**Name:** Sharp Straw  
**Description:** Use: A weak melee attack.
If it kills a unit, heal 10 HP.  
**Source:** `weapons.gon`  

```
SharpStraw {
    name "ITEM_SHARPSTRAW_NAME"
    desc "ITEM_SHARPSTRAW_DESC"
    rarity uncommon
    kind weapon
    frame 44
    
    ability wp_SharpStraw
}
```

---

### `BagOfGlass`
**Name:** Bag o' Glass  
**Description:** Use: Spawn Glass on an adjacent tile.
5% chance to break when used.  
**Source:** `weapons.gon`  

```
BagOfGlass {
    name "ITEM_BAGOFGLASS_NAME"
    desc "ITEM_BAGOFGLASS_DESC"
    rarity uncommon
    kind weapon
    frame 46
    
    ability wp_BagOfGlass
}
```

---

### `BagOfMeat`
**Name:** Bag o' Meat  
**Description:** Use: Spawn Meat on an adjacent tile.
5% chance to break when used.  
**Source:** `weapons.gon`  

```
BagOfMeat {
    name "ITEM_BAGOFMEAT_NAME"
    desc "ITEM_BAGOFMEAT_DESC"
    rarity uncommon
    kind weapon
    frame 47
	set Meat
    
    ability wp_BagOfMeat
}
```

---

### `BagOfGlitter`
**Name:** Bag o' Glitter  
**Description:** Use: Inflict Blind 2 on an adjacent unit.
5% chance to break when used.  
**Source:** `weapons.gon`  

```
BagOfGlitter {
    name "ITEM_BAGOFGLITTER_NAME"
    desc "ITEM_BAGOFGLITTER_DESC"
    rarity uncommon
    kind weapon
    frame 48
	set Stunning
    
    ability wp_BagOfGlitter
}
```

---

### `BagOfStuff`
**Name:** Bag o' Stuff  
**Description:** Use: Spawn a random pickup on an adjacent tile.
5% chance to break when used.  
**Source:** `weapons.gon`  

```
BagOfStuff {
    name "ITEM_BAGOFSTUFF_NAME"
    desc "ITEM_BAGOFSTUFF_DESC"
    rarity common
    kind weapon
    frame 49
    
    ability wp_BagOfStuff
}
```

---

### `Pickaxe`
**Name:** Pickaxe  
**Description:** Use: A melee attack that ignores shield.
If used on static or inanimate objects it destroys them and spawns a Rock. Restore 1 use when used this way.  
**Source:** `weapons.gon`  

```
Pickaxe {
    name "ITEM_PICKAXE_NAME"
    desc "ITEM_PICKAXE_DESC"
    rarity rare
    kind weapon
    frame 88
	set Miner
    
    ability wp_Pickaxe
}
```

---

### `RocketLauncher`
**Name:** Rocket Launcher  
**Description:** Use: Fire a rocket anywhere that explodes.  
**Source:** `weapons.gon`  

```
RocketLauncher {
    name "ITEM_ROCKETLAUNCHER_NAME"
    desc "ITEM_ROCKETLAUNCHER_DESC"
    kind weapon
    rarity very_rare
    frame 160
    durability 5

    ability wp_RocketLauncher
}
```

---

### `FreyedWires`
**Name:** Frayed Wires  
**Description:** Use: An electric melee attack that can chain through adjacent units.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
FreyedWires {
    name "ITEM_FREYEDWIRES_NAME" 
    desc "ITEM_FREYEDWIRES_DESC" 
    rarity uncommon
    kind weapon
    frame 29
    
    ability wp_FreyedWires
}
```

---

### `OldExtinguisher`
**Name:** Old Extinguisher  
**Description:** Use: Extinguishes fires in a cone with Knockback 5.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
OldExtinguisher {
    name "ITEM_OLDEXTINGUISHER_NAME" 
    desc "ITEM_OLDEXTINGUISHER_DESC" 
    rarity uncommon
    kind weapon
    frame 33
    
    ability wp_OldExtinguisher
}
```

---

### `TrashCanLid`
**Name:** Trash Can Lid  
**Description:** Use: A melee attack with Knockback 1.  
**Source:** `weapons.gon`  

```
TrashCanLid {
    name "ITEM_TRASHCANLID_NAME" 
    desc "ITEM_TRASHCANLID_DESC" 
    rarity uncommon
    kind weapon
    frame 54
    
    shield 5

    ability wp_TrashCanLid
}
```

---

### `MiniNuke`
**Name:** Mini Nuke  
**Description:** Use: Throw a mini nuke that makes a HUGE explosion that spawns toxic sludge.  
**Source:** `weapons.gon`  

```
MiniNuke {
    name "ITEM_MININUKE_NAME" 
    desc "ITEM_MININUKE_DESC" 
    rarity rare
    kind weapon
    frame 96
    durability 1
	set Radioactive
    
    ability wp_MiniNuke
}
```

---

### `Kandarian`
**Name:** The Kandarian  
**Description:** Use: A melee attack that always crits and inflicts Bleed 10.  
**Source:** `weapons.gon`  

```
Kandarian {
    name "ITEM_KANDARIAN_NAME" 
    desc "ITEM_KANDARIAN_DESC" 
    rarity rare
    kind weapon
    frame 135
    durability 1
	set [Demonic, Bone]
    
    ability wp_Kandarian
}
```

---

### `Geode`
**Name:** Geode  
**Description:** Use: A melee attack with a 5% chance to break when used.
When it breaks, gain 15-30 coins.  
**Source:** `weapons.gon`  

```
Geode {
    name "ITEM_GEODE_NAME"
    desc "ITEM_GEODE_DESC"
    rarity common
    kind weapon
    frame 100
	set [Rock, Gemstone]
    
    ability wp_Geode
    
    passives {
        StatusOnBreak {
            GainCoinsRange {
                min 15
                max 30
            }
        }
    }
}
```

---

### `Rocks`
**Name:** Rocks  
**Description:** Use: A lobbed attack.  
**Source:** `weapons.gon`  

```
Rocks {
    name "ITEM_ROCKS_NAME"
    desc "ITEM_ROCKS_DESC"
    rarity common
    kind weapon
    frame 55
    durability 8
    set Rock
	
    ability wp_Rocks
}
```

---

### `ExtraLimb`
**Name:** Extra Limb  
**Description:** Use: An attack that copies your basic attack.  
**Source:** `weapons.gon`  

```
ExtraLimb {
    name "ITEM_EXTRALIMB_NAME"
    desc "ITEM_EXTRALIMB_DESC"
    rarity rare
    kind weapon
    frame 65
    durability 6
	set Hybrid
    
    ability wp_ExtraLimb
}
```

---

### `GripTrainer`
**Name:** Grip Trainer  
**Description:** Use: Gain +1 [img:str].  
**Source:** `weapons.gon`  

```
GripTrainer {
    name "ITEM_GRIPTRAINER_NAME"
    desc "ITEM_GRIPTRAINER_DESC"
    rarity rare
    kind weapon
    frame 101
	set Fighter
    
    ability wp_GripTrainer
}
```

---

### `ShoeHorn`
**Name:** Shoe Horn  
**Description:** Use: Gain +2 [img:spd].  
**Source:** `weapons.gon`  

```
ShoeHorn {
    name "ITEM_SHOEHORN_NAME"
    desc "ITEM_SHOEHORN_DESC"
    rarity rare
    kind weapon
    frame 102
    
    ability wp_ShoeHorn
}
```

---

### `Cheese`
**Name:** Cheese  
**Description:** Use: Gain +1 [img:con] and heal 2 HP.  
**Source:** `weapons.gon`  

```
Cheese {
    name "ITEM_CHEESE_NAME"
    desc "ITEM_CHEESE_DESC"
    rarity rare
    kind weapon
    frame 103
    
    ability wp_Cheese
}
```

---

### `LipFiller`
**Name:** Lip Filler  
**Description:** Use: Gain +1 [img:cha] and 2 mana.  
**Source:** `weapons.gon`  

```
LipFiller {
    name "ITEM_LIPFILLER_NAME"
    desc "ITEM_LIPFILLER_DESC"
    rarity rare
    kind weapon
    frame 104
    
    ability wp_LipFiller
}
```

---

### `EnergyDrink`
**Name:** Energy Drink  
**Description:** Use: Gain +1 [img:dex] and +1 [img:spd].  
**Source:** `weapons.gon`  

```
EnergyDrink {
    name "ITEM_ENERGYDRINK_NAME"
    desc "ITEM_ENERGYDRINK_DESC"
    rarity rare
    kind weapon
    frame 105
    
    ability wp_EnergyDrink
}
```

---

### `CatPaw`
**Name:** Cat Paw  
**Description:** Use: A melee attack that has a 25% chance to refresh itself when used.  
**Source:** `weapons.gon`  

```
CatPaw {
    name "ITEM_CATPAW_NAME"
    desc "ITEM_CATPAW_DESC"
    rarity rare
    kind weapon
    frame 20
	set Hybrid

    lck 2

    ability wp_CatPaw
}
```

---

### `FlowerMix`
**Name:** Flower Mix  
**Description:** Use: Plant flowers in a large area. 
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
FlowerMix {
    name "ITEM_FLOWERMIX_NAME"
    desc "ITEM_FLOWERMIX_DESC"
    rarity uncommon
    kind weapon
    frame 28
	set Flower

    ability wp_FlowerMix
}
```

---

### `PuzzleBox`
**Name:** Puzzle Box  
**Description:** Use: Shoot hooks in 8 directions that inflict Bleed 1 and pull units towards you.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
PuzzleBox {
    name "ITEM_PUZZLEBOX_NAME"
    desc "ITEM_PUZZLEBOX_DESC"
    rarity rare
    kind weapon
    frame 111
	set [Gimp, Demonic]
    
    ability wp_PuzzleBox
}
```

---

### `Crowbar`
**Name:** Crowbar  
**Description:** Use: A melee attack that destroys trash bags and crates, scattering extra pickups.  
**Source:** `weapons.gon`  

```
Crowbar {
    name "ITEM_CROWBAR_NAME"
    desc "ITEM_CROWBAR_DESC"
    rarity rare
    kind weapon
    frame 110

    ability wp_Crowbar

    passives {
        AddAdvantageToEvent { //TODO: this doesn't actually do anything yet
            type treasure_box
            options [smash bash open]
            add 5
        }
    }
}
```

---

### `FireFlower`
**Name:** Fire Flower  
**Description:** Use: Shoot a fireball that inflicts Burn 2 in an area.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
FireFlower {
    name "ITEM_FIREFLOWER_NAME"
    desc "ITEM_FIREFLOWER_DESC"
    rarity rare
    kind weapon
    frame 112
	set Flower

    ability wp_FireFlower
}
```

---

### `Bible`
**Name:** The Bible  
**Description:** Use: Cleanse one stack of a random debuff from a unit at melee range. 
Passive: Your heals heal for 1 extra.  
**Source:** `weapons.gon`  

```
Bible {
    name "ITEM_BIBLE_NAME"
    desc "ITEM_BIBLE_DESC"
    rarity uncommon
    kind weapon
    frame 114
	set Cleric

    ability wp_Bible

    passives {
        BoostHeals 1
    }
}
```

---

### `CarBattery`
**Name:** Car Battery  
**Description:** Use: An electric melee attack that has a 50% chance to chain to another enemy within 3 tiles. Can only be used while at full mana.  
**Source:** `weapons.gon`  

```
CarBattery {
    name "ITEM_CARBATTERY_NAME"
    desc "ITEM_CARBATTERY_DESC"
    rarity uncommon
    kind weapon
    frame 115

    ability wp_CarBattery
}
```

---

### `ModelingClay`
**Name:** Modeling Clay  
**Description:** {str_aux_item_desc}
\[s:.7\](This changes into a different weapon each time it's used.)\[/s\]  
**Source:** `weapons.gon`  

```
ModelingClay { //TODO: test interactions with weapons that have a chance to break on use (they probably shouldn't cause this item to break)
    name "ITEM_MODELINGCLAY_NAME"
    desc "ITEM_MODELINGCLAY_DESC"
    rarity rare
    kind weapon
    frame 68
	set DirtClod

    str_aux ModelingClay_Default
    reset_str_aux_on_store ModelingClay_Default
    str_aux_is_copy_item_active true
    str_aux_is_copy_item_passive true
    str_aux_is_copy_item_icon true
    passives {
        ModelingClayPassive 1
        TintItem {
            ignore_if_str_aux_equals ModelingClay_Default
            add [0.05 0.05 0.05]
            mul [0.45 0.3 0.25]
        }
    }
}
```

---

### `ModelingClay_Default`
**Name:** Modeling Clay  
**Description:** Use: A lobbed attack.  
**Source:** `weapons.gon`  

```
ModelingClay_Default {
    name "ITEM_MODELINGCLAY_NAME"
    desc "ITEM_MODELINGCLAY_DEFAULT_DESC"
    kind weapon
    frame 68

    ability wp_ModelingClay
}
```

---

### `PharaohStaff`
**Name:** Pharaoh's Staff  
**Description:** Use: Summon a swarm of charmed flies.
When you destroy a corpse, restore this weapon's use.  
**Source:** `weapons.gon`  

```
PharaohStaff { //Unique item from looting the Mysterious Tomb.
    name "ITEM_PHARAOHSTAFF_NAME"
    desc "ITEM_PHARAOHSTAFF_DESC"
    rarity very_rare
    kind weapon
    frame 172

    durability 1
    max_durability 1
    dont_destroy_on_0 true

    ability wp_PharaohStaff
    passives {
        StatusOnPopCorpse {
            RepairWeapon 1
        }
    }
}
```

---

### `SlagMight`
**Name:** Slag Might  
**Description:** Use: A melee attack with Bruise 1 and Knockback 5.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
SlagMight { //Unique from Jagged Pathway event
    name "ITEM_SLAGMIGHT_NAME"
    desc "ITEM_SLAGMIGHT_DESC"
    rarity very_rare
    kind weapon
    frame 173
	set Rock
        
    ability wp_SlagMight
}
```

---

### `MomsToeNail`
**Name:** Mom's Toenail  
**Description:** Use: A melee attack.  
**Source:** `weapons.gon`  

```
MomsToeNail { //Unique from BigToe event
    name "ITEM_MOMSTOENAIL_NAME"
    desc "ITEM_MOMSTOENAIL_DESC"
    kind weapon
    frame 219
	set Mother
    
    ability wp_MomsToeNail
}
```

---

### `AlienBlaster`
**Name:** Alien Blaster  
**Description:** Use: A laser attack. Gains +1 damage for the rest of the battle each time it's used.  
**Source:** `weapons.gon`  

```
AlienBlaster { //Unique from CrashedObject event
    name "ITEM_ALIENBLASTER_NAME"
    desc "ITEM_ALIENBLASTER_DESC"
    kind weapon
    frame 218
	set Space

    ability wp_AlienBlaster
}
```

---

### `PolymorphRemote`
**Name:** Polymorph Remote  
**Description:** Use: Transform a non-boss enemy into another random enemy from the same chapter.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
PolymorphRemote {
    name "ITEM_POLYMORPHREMOTE_NAME"
    desc "ITEM_POLYMORPHREMOTE_DESC"
    rarity rare
    kind weapon
    frame 67
    
    ability wp_PolymorphRemote
}
```

---

### `MelonBaller`
**Name:** Melon Baller  
**Description:** Use: A melee attack that inflicts Blind 3 and gives you a random eye trinket if you don't have a trinket equipped.  
**Source:** `weapons.gon`  

```
MelonBaller {
    name "ITEM_MELONBALLER_NAME"
    desc "ITEM_MELONBALLER_DESC"
    rarity uncommon
    kind weapon
    frame 120
    durability [4, 6]

    ability wp_MelonBaller
}
```

---

### `EtherSoakedRag`
**Name:** Ether Soaked Rag  
**Description:** Use: Put an adjacent unit or yourself to sleep. That unit gets +5 Health Regen and +5 Mana Regen until it wakes up.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
EtherSoakedRag {
    name "ITEM_ETHERSOAKEDRAG_NAME"
    desc "ITEM_ETHERSOAKEDRAG_DESC"
    rarity uncommon
    kind weapon
    frame 121
	set Rag

    ability wp_EtherSoakedRag
}
```

---

### `DeathsScythe`
**Name:** Death's Scythe  
**Description:** Use: A spin attack. After using this, die at the end of your turn.  
**Source:** `weapons.gon`  

```
DeathsScythe {
    name "ITEM_DEATHSSCYTHE_NAME"
    desc "ITEM_DEATHSSCYTHE_DESC"
    rarity rare
    kind weapon
    frame 122

    ability wp_DeathsScythe
}
```

---

### `Necronomicon`
**Name:** Necronomicon  
**Description:** Use: Unearth 5 zombies. These zombies have a 33% chance of having Madness.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
Necronomicon {
    name "ITEM_NECRONOMICON_NAME"
    desc "ITEM_NECRONOMICON_DESC"
    rarity uncommon
    kind weapon
    frame 123
	set [Necromancer, Demonic]

    ability wp_Necronomicon
}
```

---

### `Jitte`
**Name:** Jitte  
**Description:** Use: A melee attack that deals damage equal to half your [img:str] rounded up, inflicts Weakness 1, and gives you +1 [img:str] and +1 HP on hit.  
**Source:** `weapons.gon`  

```
Jitte {
    name "ITEM_JITTE_NAME"
    desc "ITEM_JITTE_DESC"
    rarity uncommon
    kind weapon
    frame 124
	set Ninja

    ability wp_Jitte
}
```

---

### `AnarchistCookbook`
**Name:** Anarchist Cookbook  
**Description:** Use: Summon 3-5 grenades that explode at the end of the round or when destroyed.  
**Source:** `weapons.gon`  

```
AnarchistCookbook {
    name "ITEM_ANARCHISTCOOKBOOK_NAME"
    desc "ITEM_ANARCHISTCOOKBOOK_DESC"
    rarity uncommon
    kind weapon
    frame 125
	set Paper

    ability wp_AnarchistCookbook
}
```

---

### `MomsKnife`
**Name:** Mom's Knife  
**Description:** Use: Throw a penetrating projectile that returns to you.  
**Source:** `weapons.gon`  

```
MomsKnife {
    name "ITEM_MOMSKNIFE_NAME"
    desc "ITEM_MOMSKNIFE_DESC"
    rarity very_rare
    kind weapon
    frame 126
	set Mother

    ability wp_MomsKnife
}
```

---

### `MysteriousBone`
**Name:** Mysterious Bone  
**Description:** Use: A melee attack with a 25% chance to inflict Charm.  
**Source:** `weapons.gon`  

```
MysteriousBone {
    name "ITEM_MYSTERIOUSBONE_NAME"
    desc "ITEM_MYSTERIOUSBONE_DESC"
    rarity very_rare
    kind weapon
    frame 127
	set Bone
    
    ability wp_MysteriousBone
}
```

---

### `HolyGrail`
**Name:** Holy Grail  
**Description:** Use: Heal an adjacent unit or yourself for 5 HP.  
**Source:** `weapons.gon`  

```
HolyGrail {
    name "ITEM_HOLYGRAIL_NAME"
    desc "ITEM_HOLYGRAIL_DESC"
    rarity very_rare
    kind weapon
    frame 128
	set Cleric

    ability wp_HolyGrail
}
```

---

### `SpearOfDestiny`
**Name:** Spear of Destiny  
**Description:** Use: A melee attack with +1 reach that penetrates through units.
RELOAD: Collect a blessing pickup or get hit by a Holy Element spell.  
**Source:** `weapons.gon`  

```
SpearOfDestiny {
    name "ITEM_SPEAROFDESTINY_NAME"
    desc "ITEM_SPEAROFDESTINY_DESC"
    rarity very_rare
    kind weapon
    frame 129

    ability wp_SpearOfDestiny
}
```

---

### `HeavyMace`
**Name:** Heavy Mace  
**Description:** Use: A melee attack with Knockback 2 that deals damage equal to your [img:str].
Cleaves and deals double damage to units with [img:shield].  
**Source:** `weapons.gon`  

```
HeavyMace {
    name "ITEM_HEAVYMACE_NAME"
    desc "ITEM_HEAVYMACE_DESC"
    rarity very_rare
    kind weapon
    frame 131
	set Fighter

    spd -6

    ability wp_HeavyMace
}
```

---

### `UraniumRod`
**Name:** Uranium Rod  
**Description:** Use: A melee attack that inflicts -1 [img:con], Poison 2 and Weakness 1.
At the end of each battle, if you are downed, gain a random mutation.  
**Source:** `weapons.gon`  

```
UraniumRod {
    name "ITEM_URANIUMROD_NAME"
    desc "ITEM_URANIUMROD_DESC"
    rarity rare
    kind weapon
    frame 132
	set Radioactive

    con -6

    ability wp_UraniumRod
    
    passives {
        StatusOnBattleEnd {
            even_if_dead true
            Conditional_Corpse {
                RandomMutation 1
            }
        }
    }
}
```

---

### `Ocarina`
**Name:** Ocarina  
**Description:** Use: Cast a random musical spell.  
**Source:** `weapons.gon`  

```
Ocarina {
    name "ITEM_OCARINA_NAME"
    desc "ITEM_OCARINA_DESC"
    rarity uncommon
    kind weapon
    frame 134

    ability wp_Ocarina
}
```

---

### `SmallMeteor`
**Name:** Small Meteor  
**Description:** - {str_aux_active_name} -
{str_aux_active_desc}  
**Source:** `weapons.gon`  

```
SmallMeteor {
    name "ITEM_SMALLMETEOR_NAME"
    desc "ITEM_SMALLMETEOR_DESC"
    rarity rare
    kind weapon
    frame 175
    randomize_piece_frames true
	set Planet

    str_aux_initialize random_copyable_colorless_ability
    str_aux_is_copy_ability {
        bonus_passives {
            ModifyAbility {
                meta {
                    is_basic_attack false
                    is_weapon true
                }
                cost {
                    mana 0
                    charge 1
                }
            }
        }
    }

    ability None
}
```

---

### `GlowingBone`
**Name:** Glowing Bone  
**Description:** - {str_aux_active_name} -
{str_aux_active_desc}  
**Source:** `weapons.gon`  

```
GlowingBone {
    name "ITEM_GLOWINGBONE_NAME"
    desc "ITEM_GLOWINGBONE_DESC"
    rarity rare
    kind weapon
    frame 174
    randomize_piece_frames true
	set Bone

    str_aux_initialize random_copyable_class_ability
    str_aux_is_copy_ability {
        bonus_passives {
            ModifyAbility {
                meta {
                    is_basic_attack false
                    is_weapon true
                }
                cost {
                    mana 0
                    charge 1
                }
            }
        }
    }

    ability None
}
```

---

### `IrradiatedObject`
**Name:** Irradiated Object  
**Description:** {str_aux_item_desc}  
**Source:** `weapons.gon`  

```
IrradiatedObject {
    name "ITEM_IRRADIATEDOBJECT_NAME"
    desc "ITEM_IRRADIATEDOBJECT_DESC"
    rarity rare
    kind weapon
    frame 176
    randomize_piece_frames true
	set Radioactive

    str_aux_initialize random_passive_trinket
    str_aux_is_copy_item_passive true

    ability wp_IrradiatedObject
}
```

---

### `IrradiatedObject_Burn`
**Description:** Use: A melee attack that inflicts Burn 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Burn {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_BURN_DESC"
    ability wp_IrradiatedObject_Burn
}
```

---

### `IrradiatedObject_Stun`
**Description:** Use: A melee attack that inflicts Stun 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Stun {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_STUN_DESC"
    ability wp_IrradiatedObject_Stun
}
```

---

### `IrradiatedObject_Bleed`
**Description:** Use: A melee attack that inflicts Bleed 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Bleed {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_BLEED_DESC"
    ability wp_IrradiatedObject_Bleed
}
```

---

### `IrradiatedObject_Bruise`
**Description:** Use: A melee attack that inflicts Bruise 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Bruise {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_BRUISE_DESC"
    ability wp_IrradiatedObject_Bruise
}
```

---

### `IrradiatedObject_Poison`
**Description:** Use: A melee attack that inflicts Poison 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Poison {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_POISON_DESC"
    ability wp_IrradiatedObject_Poison
}
```

---

### `IrradiatedObject_Sleep`
**Description:** Use: A melee attack that inflicts Sleep 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Sleep {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_SLEEP_DESC"
    ability wp_IrradiatedObject_Sleep
}
```

---

### `IrradiatedObject_Fear`
**Description:** Use: A melee attack that inflicts Fear 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Fear {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_FEAR_DESC"
    ability wp_IrradiatedObject_Fear
}
```

---

### `IrradiatedObject_Charmed`
**Description:** Use: A melee attack that inflicts Charmed 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Charmed {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_CHARMED_DESC"
    ability wp_IrradiatedObject_Charmed
}
```

---

### `IrradiatedObject_Weakness`
**Description:** Use: A melee attack that inflicts Weakness 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Weakness {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_WEAKNESS_DESC"
    ability wp_IrradiatedObject_Weakness
}
```

---

### `IrradiatedObject_Confusion`
**Description:** Use: A melee attack that inflicts Confusion 1.
{str_aux_item_desc}
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
IrradiatedObject_Confusion {
    variant_of IrradiatedObject
    desc "ITEM_IRRADIATEDOBJECT_CONFUSION_DESC"
    ability wp_IrradiatedObject_Confusion
}
```

---

### `SteelBall`
**Name:** Steel Ball  
**Description:** Use: Summon an invulnerable Fly familiar.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
SteelBall {
    name "ITEM_STEELBALL_NAME"
    desc "ITEM_STEELBALL_DESC"
    rarity rare
    kind weapon
    frame 157

    ability wp_SteelBall
}
```

---

### `USAShield`
**Name:** USA Shield  
**Description:** Use: A ranged attack that inflicts Stun.
\[s:.7\](Usable once per battle.)\[/s\]
Passive: +2 Brace while this weapon is usable.  
**Source:** `weapons.gon`  

```
USAShield {
    name "ITEM_USASHIELD_NAME"
    desc "ITEM_USASHIELD_DESC"
    rarity rare
    kind weapon
    frame 158
	set Superhero

    passives {
        PassiveIfWeaponIsUsable {
            Brace 2
        }
    }
    ability wp_USAShield
}
```

---

### `TeslaCannon`
**Name:** Tesla Cannon  
**Description:** Use: Fire a ranged electric shot that passes through units in a straight line with a 50% chance to Stun.  
**Source:** `weapons.gon`  

```
TeslaCannon { //this is a Tinkerer Tech 3 item
    name "ITEM_TESLACANNON_NAME"
    desc "ITEM_TESLACANNON_DESC"
    rarity very_rare
    kind weapon
    frame 185
    durability 3
	set Experimental

    ability wp_TeslaCannon
}
```

---

### `MeatBomb`
**Name:** Meat Bomb  
**Description:** Use: Throw a bomb that explodes.  
**Source:** `weapons.gon`  

```
MeatBomb {
    name "ITEM_MEATBOMB_NAME"
    desc "ITEM_MEATBOMB_DESC"
    rarity very_rare
    kind weapon
    frame 191
    set Meat
	
    ability wp_SmallBomb
}
```

---

### `BloodyStick`
**Name:** Bloody Stick  
**Description:** +1 Health Regen.
Use: A melee attack with +1 reach.  
**Source:** `weapons.gon`  

```
BloodyStick {
    name "ITEM_BLOODYSTICK_NAME"
    desc "ITEM_BLOODYSTICK_DESC"
    rarity very_rare
    kind weapon
    frame 192
	set Wood
	
    passives {
        HealthRegenUp 1
    }

    ability wp_Stick
}
```

---

### `BucketOfBlood`
**Name:** Bucket of Blood  
**Description:** Use: Gain +2 [img:con] and -1 [img:spd], then heal 4 HP.  
**Source:** `weapons.gon`  

```
BucketOfBlood {
    name "ITEM_BUCKETOFBLOOD_NAME"
    desc "ITEM_BUCKETOFBLOOD_DESC"
    rarity very_rare
    kind weapon
    frame 196

    ability wp_BucketOfLard
}
```

---

### `BloodyButterflyKnife`
**Name:** Bloody Knife  
**Description:** Use: A multi-hit melee attack with Lifesteal that inflicts Bleed.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
BloodyButterflyKnife {
    name "ITEM_BLOODYBUTTERFLYKNIFE_NAME"
    desc "ITEM_BLOODYBUTTERFLYKNIFE_DESC" 
    rarity very_rare
    kind weapon
    frame 197

    ability wp_BloodyButterflyKnife
}
```

---

### `BloodyBearTraps`
**Name:** Bloody Bear Traps  
**Description:** Use: Place a Bear Trap.  
**Source:** `weapons.gon`  

```
BloodyBearTraps {
    name "ITEM_BLOODYBEARTRAPS_NAME"
    desc "ITEM_BLOODYBEARTRAPS_DESC"
    rarity very_rare
    kind weapon
    frame 198
	set [Hunter, Survivalist]

    ability wp_BearTraps
}
```

---

### `BloodyBagOfGlass`
**Name:** Bloody Bag of Glass  
**Description:** Use: Throw a projectile that creates glass.  
**Source:** `weapons.gon`  

```
BloodyBagOfGlass {
    name "ITEM_BLOODYBAGOFGLASS_NAME"
    desc "ITEM_BLOODYBAGOFGLASS_DESC"
    rarity very_rare
    kind weapon
    frame 194
    
    ability wp_BloodyBagOfGlass
}
```

---

### `MeatSlugger`
**Name:** Meat Slugger  
**Description:** Use: A melee attack with Knockback 10 that inflicts Bruise.  
**Source:** `weapons.gon`  

```
MeatSlugger {
    name "ITEM_MEATSLUGGER_NAME"
    desc "ITEM_MEATSLUGGER_DESC"
    rarity very_rare
    kind weapon
    frame 186

    ability wp_MeatSlugger
}
```

---

### `BloodyMeatHook`
**Name:** Bloody Meat Hook  
**Description:** Use: Pull a unit towards you, Cleaving and inflicting Bleed 1.  
**Source:** `weapons.gon`  

```
BloodyMeatHook {
    name "ITEM_BLOODYMEATHOOK_NAME"
    desc "ITEM_BLOODYMEATHOOK_DESC"
    rarity very_rare
    kind weapon
    frame 189
	set [Butcher, Barbed]
    
    ability wp_BloodyMeatHook
}
```

---

### `BloodySoulClaw`
**Name:** Bloody Soul Claw  
**Description:** Use: A melee attack that deals damage equal to the number of uses this has left.
When this weapon kills a unit, it gains +2 uses and you heal 5 HP.  
**Source:** `weapons.gon`  

```
BloodySoulClaw {
    name "ITEM_BLOODYSOULCLAW_NAME"
    desc "ITEM_BLOODYSOULCLAW_DESC"
    rarity very_rare
    kind weapon
    frame 190
	durability 8
    
    ability wp_BloodySoulClaw 
}
```

---

### `BloodBucket`
**Name:** Blood Bucket  
**Description:** Use: A lobbed attack that creates a creep puddle.  
**Source:** `weapons.gon`  

```
BloodBucket {
    name "ITEM_BLOODBUCKET_NAME"
    desc "ITEM_BLOODBUCKET_DESC"
    rarity very_rare
    kind weapon
    frame 188
    
    ability wp_ChumBucket
}
```

---

### `BloodySpikes`
**Name:** Bloody Spikes  
**Description:** +1 Thorns.
Use: A ranged attack.  
**Source:** `weapons.gon`  

```
BloodySpikes {
    name "ITEM_BLOODYSPIKES_NAME"
    desc "ITEM_BLOODYSPIKES_DESC"
    rarity very_rare
    kind weapon
    frame 187
	
    passives {
        Thorns 1
    }
    
    ability wp_RailSpikes
}
```

---

### `BottlesOfBlood`
**Name:** Bottles of Blood  
**Description:** Use: A lobbed attack that creates glass tiles in an area.  
**Source:** `weapons.gon`  

```
BottlesOfBlood {
    name "ITEM_BOTTLESOFBLOOD_NAME"
    desc "ITEM_BOTTLESOFBLOOD_DESC"
    rarity very_rare
    kind weapon
    frame 193

    ability wp_BloodBottles
}
```

---

### `BlessedAnointingOil`
**Name:** Blessed Anointing Oil  
**Description:** Use: Cleanse debuffs and heal an adjacent unit or yourself.  
**Source:** `weapons.gon`  

```
BlessedAnointingOil {
    name "ITEM_BLESSEDANOINTINGOIL_NAME"
    desc "ITEM_BLESSEDANOINTINGOIL_DESC"
    rarity very_rare
    kind weapon
    frame 221
	set Cleric
    
    ability wp_BlessedAnointingOil
}
```

---

### `HarpysClaw`
**Name:** Harpy's Claw  
**Description:** Use: A melee attack that inflicts Poison 1, Bleed 1, Confusion 1, Weakness 1, and Slow 1.  
**Source:** `weapons.gon`  

```
HarpysClaw {
    name "ITEM_HARPYSCLAW_NAME"
    desc "ITEM_HARPYSCLAW_DESC"
    rarity very_rare
    kind weapon
    frame 199

    ability wp_HarpyClaw
}
```

---

### `RatBomb`
**Name:** Rat Bomb  
**Description:** Use: Toss a Bomb that explodes at the end of the round.  
**Source:** `weapons.gon`  

```
RatBomb {
    name "ITEM_RATBOMB_NAME"
    desc "ITEM_RATBOMB_DESC"
    rarity rare
    kind weapon
    frame 222
	durability 5
	set Rat

	ability wp_RatBomb
}
```

---

### `Spinnerets`
**Name:** Spinnerets  
**Description:** Use: A ranged attack that inflicts Webbed.  
**Source:** `weapons.gon`  

```
Spinnerets {
    name "ITEM_SPINNERETS_NAME"
    desc "ITEM_SPINNERETS_DESC"
    rarity rare
    kind weapon
    frame 223
	durability 6

	ability wp_SpiderWebber
}
```

---

### `ZodiacsSixshooter`
**Name:** Zodiac's Six Shooter  
**Description:** Use: Fire a shot anywhere within your line of sight.
Automatically use this whenever an enemy ends movement within your line of sight.
Reloads at the end of each battle.  
**Source:** `weapons.gon`  

```
ZodiacsSixshooter {
    name "ITEM_ZODIACSSIXSHOOTER_NAME"
    desc "ITEM_ZODIACSSIXSHOOTER_DESC"
    rarity very_rare
    kind weapon
    frame 224
    durability 6
    max_durability 6
    dont_destroy_on_0 true
	set Cool

    ability wp_ZodiacsSixshooter
    passives {
        StatusOnBattleEnd {
            even_if_dead true
            RepairWeapon 6
        }
        PassiveWhileHasDurability {
            MovementReaction {
                ability wp_ZodiacsSixshooter_Auto
                enemies_only true
                create_temp_ability true
            }
        }
    }
}
```

---

### `GambitsDice`
**Name:** Gambit's Dice  
**Description:** Use: Throw a projectile that deals 1-6 damage at random.
RELOAD: Cast a spell that costs exactly 6 mana.  
**Source:** `weapons.gon`  

```
GambitsDice {
    name "ITEM_GAMBITSDICE_NAME"
    desc "ITEM_GAMBITSDICE_DESC"
    rarity very_rare
    kind weapon
    frame 225

	ability wp_GambitsDice
}
```

---

### `JohnnysStool`
**Name:** Johnny's Stool  
**Description:** Use: A melee attack with Knockback 2.
If you end your turn with a unused movement actions, heal 3 HP and gain 3 Charge.  
**Source:** `weapons.gon`  

```
JohnnysStool {
    name "ITEM_JOHNNYSSTOOL_NAME"
    desc "ITEM_JOHNNYSSTOOL_DESC"
    rarity rare
    kind weapon
    frame 226
	set Wood

	ability wp_Stoolatk

    passives {
		StatusIfUnusedMovePoints {
			HealthGain 3
			Charge 3
		}
    }
}
```

---

### `AlienTech`
**Name:** Alien Tech  
**Description:** Use: Target an area. Unleash a hyper beam attack in that area at the start of your next turn.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
AlienTech {
    name "ITEM_ALIENTECH_NAME"
    desc "ITEM_ALIENTECH_DESC"
    rarity rare
    kind weapon
    frame 227
	set Space

	ability AlienBeam
}
```

---

### `Stacy100`
**Name:** Stacy 100  
**Description:** Use: Spawn a Stacy.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
Stacy100 {
    name "ITEM_STACY100_NAME"
    desc "ITEM_STACY100_DESC"
    rarity very_rare
    kind weapon
    frame 228

	ability wp_SpawnStacy
}
```

---

### `BungasBone`
**Name:** Bunga's Bone  
**Description:** Use: A melee attack with Knockback 5.  
**Source:** `weapons.gon`  

```
BungasBone {
    name "ITEM_BUNGASBONE_NAME"
    desc "ITEM_BUNGASBONE_DESC"
    rarity rare
    kind weapon
    frame 229
	set Bone

	ability wp_BungaClub
}
```

---

### `HitlersPistol`
**Name:** Hitler's Pistol  
**Description:** Use: Fire a shot in a straight line.  
**Source:** `weapons.gon`  

```
HitlersPistol {
    name "ITEM_HITLERSPISTOL_NAME"
    desc "ITEM_HITLERSPISTOL_DESC"
    rarity rare
    kind weapon
    frame 230
	durability 8

	ability wp_Lugar
}
```

---

### `Bug`
**Name:** Bug  
**Description:** Your basic attack is Metronome.
Use: Cast a random spell.  
**Source:** `weapons.gon`  

```
Bug {
    name "ITEM_BUG_NAME"
    desc "ITEM_BUG_DESC"
    rarity rare
    kind weapon
    frame 231
	
	attack BasicMetronome

	ability wp_OddRemote
	
	passives {
        OverrideBasicAttack BasicMetronome
	}
}
```

---

### `Fate`
**Name:** Fate  
**Description:** Use: Summon meteors that hit random tiles everywhere. These meteors have a chance to stun, spawn fires, or leave rocks behind.  
**Source:** `weapons.gon`  

```
Fate {
    name "ITEM_FATE_NAME"
    desc "ITEM_FATE_DESC"
    rarity rare
    kind weapon
    frame 232
	
	ability wp_Fate
}
```

---

### `MammothTusk`
**Name:** Mammoth Tusk  
**Description:** Use: A melee attack that inflicts Bruise 2 and Confusion. Become Drowsy after use.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
MammothTusk {
    name "ITEM_MAMMOTHTUSK_NAME"
    desc "ITEM_MAMMOTHTUSK_DESC"
    rarity very_rare
    kind weapon
    frame 233
	set Wooly
	
	ability wp_TuskThrow

}
```

---

### `AmericanFlag`
**Name:** American Flag  
**Description:** Use: Force a unit to attack one of its enemies.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
AmericanFlag {
    name "ITEM_AMERICANFLAG_NAME"
    desc "ITEM_AMERICANFLAG_DESC"
    rarity rare
    kind weapon
    frame 234
	
	str 1
	dex 1
    con 1
	spd 1
	int 1
	lck 1
	cha 1

	ability wp_Rally
}
```

---

### `BookOfBelial`
**Name:** Book Of Belial  
**Description:** Use: Gain +3 Damage.
RELOAD: Kill an enemy.  
**Source:** `weapons.gon`  

```
BookOfBelial {
    name "ITEM_BOOKOFBELIAL_NAME"
    desc "ITEM_BOOKOFBELIAL_DESC"
    rarity rare
    kind weapon
    frame 235
	set [Demonic, Paper]
	
	ability wp_BookofBelial
}
```

---

### `MegaAlienBlaster`
**Name:** Mega Alien Blaster  
**Description:** Use: A laser attack. Gains +5 damage for the rest of the battle each time it's used.
Take 5 damage when used.  
**Source:** `weapons.gon`  

```
MegaAlienBlaster {
    name "ITEM_MEGAALIENBLASTER_NAME"
    desc "ITEM_MEGAALIENBLASTER_DESC"
    rarity rare
    kind weapon
    frame 236
	set Space

	ability wp_MegaAlienBlaster
}
```

---

### `HellHook`
**Name:** Hell Hook  
**Description:** Use: Pull a unit toward you.  
**Source:** `weapons.gon`  

```
HellHook {
    name "ITEM_HELLHOOK_NAME"
    desc "ITEM_HELLHOOK_DESC"
    rarity very_rare
    kind weapon
    frame 237
	set [Demonic, Barbed, Butcher]
	
	ability wp_MeatHookB
}
```

---

### `DemonCore`
**Name:** Demon Core  
**Description:** Start each battle with Poison 5. Inflict All Stats Down 2 on bosses and minibosses at the start of the battle.
Use: A melee attack that causes a unit to die at the end of its next turn. Bosses fall asleep at the end of their next turn instead.  
**Source:** `weapons.gon`  

```
DemonCore {
    name "ITEM_DEMONCORE_NAME"
    desc "ITEM_DEMONCORE_DESC"
    rarity rare
    kind weapon
    frame 238
	set Radioactive
	
	ability wp_DemonDoom

    passives {
        Poison 5
        StatusAllCharactersOnSpawn {
            Conditional_Boss {
                AllStatsUp -2
            }
        }
    }
}
```

---

### `BagOfChum`
**Name:** Bag Of Chum  
**Description:** Use: Spawn a Charmed Maggot.  
**Source:** `weapons.gon`  

```
BagOfChum {
    name "ITEM_BAGOFCHUM_NAME"
    desc "ITEM_BAGOFCHUM_DESC"
    rarity rare
    kind weapon
    frame 240
	set Guts

	ability wp_ChumShot
}
```

---

### `GoldenPickaxe`
**Name:** Golden Pickaxe  
**Description:** Use: A melee attack that ignores shield.
If used on static or inanimate objects it destroys them and spawns a Coin.
Spawn a coin on a random tile at the end of each turn.  
**Source:** `weapons.gon`  

```
GoldenPickaxe {
    name "ITEM_GOLDENPICKAXE_NAME"
    desc "ITEM_GOLDENPICKAXE_DESC"
    rarity very_rare
    kind weapon
    frame 241
	set Miner
	
	ability wp_GoldPickaxe
	
	passives {
		StatusEachTurnEnd {
			SpawnCoinAnywhere 1
		}
    }
}
```

---

### `ManholeCover`
**Name:** Manhole Cover  
**Description:** Brace 2.
Use: A ranged attack with Knockback 2 that passes through units and returns to you.  
**Source:** `weapons.gon`  

```
ManholeCover {
    name "ITEM_MANHOLECOVER_NAME"
    desc "ITEM_MANHOLECOVER_DESC"
    rarity very_rare
    kind weapon
    frame 242
	
	ability wp_Manhole	

	passives {
		Brace 2
    }
}
```

---

### `TinasLarynx`
**Name:** Tina's Larynx  
**Description:** Use: Inflict Fear on all enemies.
\[s:.7\](Usable once per battle.)\[/s\]  
**Source:** `weapons.gon`  

```
TinasLarynx {
    name "ITEM_TINASLARYNX_NAME"
    desc "ITEM_TINASLARYNX_DESC"
    rarity very_rare
    kind weapon
    frame 183
	set Guts
	
    ability wp_TinaScream
}
```

---

### `RoboticArm`
**Name:** Robotic Arm  
**Description:** Use: A melee attack with a chance to repeat. Gains 1 damage for the rest of the battle each time it's used. Refreshes when affected by Electric element.  
**Source:** `weapons.gon`  

**Localization Strings:**
- `COMBAT_POPUP_RECHARGED`: "Recharged!"

```
RoboticArm {
    name "ITEM_ROBOTICARM_NAME"
    desc "ITEM_ROBOTICARM_DESC"
    rarity very_rare
    kind weapon
    frame 184
	set Cyborg

	ability wp_FuryArm
    
    passives {
        RefreshEquipmentAbilityOnElement {
            element Electric
            text "COMBAT_POPUP_RECHARGED"
        }
    }
}
```

---

### `StevensShotgun`
**Name:** Steven's Shotgun  
**Description:** Use: Fires 5 projectiles in a cone. Using this recoils you 10 tiles backwards and Confuses you.  
**Source:** `weapons.gon`  

```
StevensShotgun {
    name "ITEM_STEVENSSHOTGUN_NAME"
    desc "ITEM_STEVENSSHOTGUN_DESC"
    rarity very_rare
    kind weapon
    frame 177
	
    ability wp_ShotgunSteven
}
```

---

### `StevensGristle`
**Name:** Steven's Gristle  
**Description:** Units don't leave corpses.
Use: A melee attack.
This weapon gains +1 damage and +1 use when it gets a kill.
Damage resets at the end of the adventure.  
**Source:** `weapons.gon`  

```
StevensGristle {
    name "ITEM_STEVENSGRISTLE_NAME"
    desc "ITEM_STEVENSGRISTLE_DESC"
    rarity very_rare
    kind weapon
    frame 178
	durability 99
    aux 1
	set Steven

    reset_aux_on_store 1

    ability wp_GnarledClaw

    passives {
        CreateGlobalModifiers {
            NoCorpses 1
        }
    }
}
```

---

### `StevensBagofRocks`
**Name:** Steven's Bag of Rocks  
**Description:** Use: A melee attack with a chance to repeat that inflicts Bruise.  
**Source:** `weapons.gon`  

```
StevensBagofRocks {
    name "ITEM_STEVENSBAGOFROCKS_NAME"
    desc "ITEM_STEVENSBAGOFROCKS_DESC"
    rarity very_rare
    kind weapon
    frame 179
	set Steven
	
	ability wp_StevensBagOfRocks
}
```

---

### `StevensBottle`
**Name:** Steven's Bottle  
**Description:** Use: A ranged attack that creates a Tar tile.  
**Source:** `weapons.gon`  

```
StevensBottle {
    name "ITEM_STEVENSBOTTLE_NAME"
    desc "ITEM_STEVENSBOTTLE_DESC"
    rarity very_rare
    kind weapon
    frame 180
	set Steven

	ability wp_StevensBottles
}
```

---

### `StevenWeapon1`
**Name:** Steven  
**Description:** Use: A melee attack. If this hits an allied cat, spawn a quarter-sized copy of them with 25% of their stats. The copy is AI controlled.
RELOAD: An allied cat dies.  
**Source:** `weapons.gon`  

```
StevenWeapon1 {
    name "ITEM_STEVENWEAPON1_NAME"
    desc "ITEM_STEVENWEAPON1_DESC"
    rarity very_rare
    kind weapon
    frame 181
	set Steven

    ability wp_StevenWeapon1
}
```

---

### `StevenWeapon2`
**Name:** Steven  
**Description:** Use: A lobbed attack that inflicts Petrify.
RELOAD: Kill a rock.  
**Source:** `weapons.gon`  

```
StevenWeapon2 {
    name "ITEM_STEVENWEAPON2_NAME"
    desc "ITEM_STEVENWEAPON2_DESC"
    rarity very_rare
    kind weapon
    frame 182
	set Steven
	
    ability wp_StevenWeapon2
}
```

---

### `ToyGun`
**Name:** Toy Gun  
**Description:** Use: A melee attack with Knockback 10 and Chain Knockback that inflicts Bruise.  
**Source:** `weapons.gon`  

```
ToyGun {
    name "ITEM_TOYGUN_NAME"
    desc "ITEM_TOYGUN_DESC"
    rarity very_rare
    kind weapon
    frame 220
	set Jester
	
	ability wp_BangGun
}
```

---

### `Pliers`
**Name:** Pliers  
**Description:** Use: A melee attack that inflicts Weakness 3.  
**Source:** `weapons.gon`  

```
Pliers {
    name "ITEM_PLIERS_NAME"
    desc "ITEM_PLIERS_DESC"
    rarity rare
    kind weapon
    frame 133

	ability wp_Pliers
}
```

---

### `FeatherDarts`
**Name:** Feather Darts  
**Description:** Use: A ranged attack that can hit any unit in your line of sight.
Can be used 3 times per turn.  
**Source:** `weapons.gon`  

```
FeatherDarts {
    name "ITEM_FEATHERDARTS_NAME"
    desc "ITEM_FEATHERDARTS_DESC"
    rarity rare
    kind weapon
    frame 153
	set Feathered

    durability 99

    ability wp_FeatherDarts
    passives {
        ExtraWeaponAttacks 2
    }
}
```

---

### `FeatheredWing`
**Name:** Feathered Wing  
**Description:** Use: A wide wind attack with Knockback 3.  
**Source:** `weapons.gon`  

```
FeatheredWing {
    name "ITEM_FEATHEREDWING_NAME"
    desc "ITEM_FEATHEREDWING_DESC"
    kind weapon
    frame 155
	set Feathered

    durability 20

    ability wp_FeatheredWing
}
```

---

### `MoneyBag_Small`
**Name:** Money Bag  
**Description:** Becomes {aux} coins when you return home.
Use: A melee attack.  
**Source:** `weapons.gon`  

```
MoneyBag_Small {
    name "ITEM_MONEYBAG_SMALL_NAME"
    desc "ITEM_MONEYBAG_SMALL_DESC"
    rarity common
    kind weapon
    frame 243
    on_store become_aux_coins
    aux 10

    ability wp_MoneyBag_Small

    passives {
        BreakAtAux 0
    }
}
```

---

### `MoneyBag_Medium`
**Name:** Money Bag  
**Description:** Becomes {aux} coins when you return home.
Use: A melee attack.  
**Source:** `weapons.gon`  

```
MoneyBag_Medium {
    name "ITEM_MONEYBAG_MEDIUM_NAME"
    desc "ITEM_MONEYBAG_MEDIUM_DESC"
    rarity uncommon
    kind weapon
    frame 244
    on_store become_aux_coins
    aux 25

    ability wp_MoneyBag_Medium

    passives {
        ItemAuxTransform {
            le [10 MoneyBag_Small]
        }
        BreakAtAux 0
    }
}
```

---

### `MoneyBag_Large`
**Name:** Money Bag  
**Description:** Becomes {aux} coins when you return home.
Use: A melee attack.  
**Source:** `weapons.gon`  

```
MoneyBag_Large {
    name "ITEM_MONEYBAG_LARGE_NAME"
    desc "ITEM_MONEYBAG_LARGE_DESC"
    rarity rare
    kind weapon
    frame 245
    on_store become_aux_coins
    aux 50

    ability wp_MoneyBag_Large

    passives {
        ItemAuxTransform {
            le [10 MoneyBag_Small]
            le [25 MoneyBag_Medium]
        }
        BreakAtAux 0
    }
}
```

---

### `MoneyBag_Huge`
**Name:** Money Bag  
**Description:** Becomes {aux} coins when you return home.
Use: A melee attack.  
**Source:** `weapons.gon`  

```
MoneyBag_Huge {
    name "ITEM_MONEYBAG_HUGE_NAME"
    desc "ITEM_MONEYBAG_HUGE_DESC"
    rarity very_rare
    kind weapon
    frame 246
    on_store become_aux_coins
    aux 100

    ability wp_MoneyBag_Huge

    passives {
        ItemAuxTransform {
            le [10 MoneyBag_Small]
            le [25 MoneyBag_Medium]
            le [50 MoneyBag_Large]
        }
        BreakAtAux 0
    }
}
```

---

### `ThePact`
**Name:** The Pact  
**Description:** Use: Permanently lose 1 [img:con] to gain +1 [img:str], +2 [img:dex] and +2 [img:spd] for the rest of the battle.  
**Source:** `weapons.gon`  

```
ThePact {
    name "ITEM_THEPACT_NAME"
    desc "ITEM_THEPACT_DESC"
    rarity very_rare
    kind weapon
    frame 247
	set Demonic
	
	ability wp_ThePact
}
```

---

### `Probe`
**Name:** Probe  
**Description:** Use: Inflict Charm 3. Can only hit from behind.  
**Source:** `weapons.gon`  

```
Probe {
    name "ITEM_PROBE_NAME"
    desc "ITEM_PROBE_DESC"
    rarity very_rare
    kind weapon
    frame 248
	set Space
	
	ability wp_Probe
}
```

---

