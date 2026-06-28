# Mewgenics Mod Developer Documentation: Items & Equipment Reference

This file lists all items, trinkets, weapons, and consumables found in the game, categorized by their source file.

## Category: `armor_sets.gon`

### Scrap Metal Hat (`ScrapHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Scrap`
- **Description**: 
- **Mechanics**:
```gon
shield 4
        passives {
            Metal 1
        }
```

### Scrap Metal Mask (`ScrapMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Scrap`
- **Description**: 
- **Mechanics**:
```gon
shield 4
        passives {
            Metal 1
        }
```

### Scrap Metal Armor (`ScrapArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Scrap`
- **Description**: 
- **Mechanics**:
```gon
shield 4
        passives {
            Metal 1
        }
```

### Leather Cap (`LeatherHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Leather`
- **Description**: +1 Brace.
- **Mechanics**:
```gon
shield 1
        passives {
            Brace 1
        }
```

### Leather Mask (`LeatherMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Leather`
- **Description**: +1 Brace.
- **Mechanics**:
```gon
shield 1
        passives {
            Brace 1
        }
```

### Leather Choker (`LeatherArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Leather`
- **Description**: +1 Brace.
- **Mechanics**:
```gon
shield 1
        passives {
            Brace 1
        }
```

### Rag Hood (`RagHood`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Rag`
- **Description**: +15% Dodge Chance.
- **Mechanics**:
```gon
passives {
            ArmorDodgeChance 15%
        }
```

### Rag Mask (`RagMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Rag`
- **Description**: +15% Dodge Chance.
- **Mechanics**:
```gon
passives {
            ArmorDodgeChance 15%
        }
```

### Rags (`RagArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Rag`
- **Description**: +15% Dodge Chance.
- **Mechanics**:
```gon
passives {
            ArmorDodgeChance 15%
        }
```

### Rubber Hat (`RubberHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Rubber`
- **Description**: Units that contact you are knocked back 2 tiles.
- **Mechanics**:
```gon
shield 2
        passives {
            MeleeRevengeDamage {
                knockback 2
            }
        }
```

### Rubber Mask (`RubberMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Rubber`
- **Description**: Units that contact you are knocked back 2 tiles.
- **Mechanics**:
```gon
shield 2
        passives {
            MeleeRevengeDamage {
                knockback 2
            }
        }
```

### Tire (`RubberArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Rubber`
- **Description**: Units that contact you are knocked back 2 tiles.
- **Mechanics**:
```gon
shield 2
        passives {
            MeleeRevengeDamage {
                knockback 2
            }
        }
```

### Cathide Hat (`CatHideHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `CatHide`
- **Description**: +1 Health Regen. 5% chance to spawn a Flea Familiar at the end of your turn.
- **Mechanics**:
```gon
shield 2
        passives {
            HealthRegenUp 1
            SpawnEachTurn {
                chance 5%
                object CharmedFlea
                stack_key CATHIDE
            }
        }
```

### Cathide Mask (`CatHideMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `CatHide`
- **Description**: +1 Health Regen. 5% chance to spawn a Flea Familiar at the end of your turn.
- **Mechanics**:
```gon
shield 2
        passives {
            HealthRegenUp 1
            SpawnEachTurn {
                chance 5%
                object CharmedFlea
                stack_key CATHIDE
            }
        }
```

### Cathide Armor (`CatHideArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `CatHide`
- **Description**: +1 Health Regen. 5% chance to spawn a Flea Familiar at the end of your turn.
- **Mechanics**:
```gon
shield 2
        passives {
            HealthRegenUp 1
            SpawnEachTurn {
                chance 5%
                object CharmedFlea
                stack_key CATHIDE
            }
        }
```

### Thick Hide (`ThickHide`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `CatHide`
- **Description**: +1 Brace. Immunity to Slow and Freeze.
- **Mechanics**:
```gon
shield 3
        passives {
            Brace 1
            StatusImmunity [Freeze, Slow]
        }
```

### Heart (`GutsHeart`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Guts`
- **Description**: +1 Health Regen.
- **Mechanics**:
```gon
con 2
        passives {
            HealthRegenUp 1
        }
```

### Liver (`GutsLiver`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Guts`
- **Description**: +1 Health Regen.
- **Mechanics**:
```gon
con 2
        passives {
            HealthRegenUp 1
        }
```

### Intestines (`GutsIntestines`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Guts`
- **Description**: +1 Health Regen.
- **Mechanics**:
```gon
con 2
        passives {
            HealthRegenUp 1
        }
```

### Skull Cap (`BonesHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Bone`
- **Description**: Breaks when [img:shield] is depleted. When it breaks, gain +1 [img:int] and +3 Health Regen for the rest of the battle.
- **Mechanics**:
```gon
shield 3
        passives {
            BoneArmorPassive 1
            StatusOnBreak {
                HealthRegenUp 3
                IntelligenceUp 1
            }
        }
```

### Jawbone (`BonesMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Bone`
- **Description**: Breaks when [img:shield] is depleted. When it breaks, gain +1 [img:str] and +3 Health Regen for the rest of the battle.
- **Mechanics**:
```gon
shield 3
        passives {
            BoneArmorPassive 1
            StatusOnBreak {
                HealthRegenUp 3
                StrengthUp 1
            }
        }
```

### Bone Necklace (`BonesNeck`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Bone`
- **Description**: Breaks when [img:shield] is depleted. When it breaks, gain +1 [img:dex] and +3 Health Regen for the rest of the battle.
- **Mechanics**:
```gon
shield 3
        passives {
            BoneArmorPassive 1
            StatusOnBreak {
                HealthRegenUp 3
                DexterityUp 1
            }
        }
```

### Dirt Clod Hat (`DirtClodHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `DirtClod`
- **Description**: +2 Mana Regen, +2 Health Regen. Fragile and Brittle while wet.
- **Mechanics**:
```gon
passives {
            AddManaRegen 2
            HealthRegenUp 2
            FragileDuringElement water
            BrittleDuringElement water
        }
```

### Dirt Clod Mask (`DirtClodMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `DirtClod`
- **Description**: +2 Mana Regen, +2 Health Regen. Fragile and Brittle while wet.
- **Mechanics**:
```gon
passives {
            AddManaRegen 2
            HealthRegenUp 2
            FragileDuringElement water
            BrittleDuringElement water
        }
```

### Dirt Clod Necklace (`DirtClodNeck`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `DirtClod`
- **Description**: +2 Mana Regen, +2 Health Regen. Fragile and Brittle while wet.
- **Mechanics**:
```gon
passives {
            AddManaRegen 2
            HealthRegenUp 2
            FragileDuringElement water
            BrittleDuringElement water
        }
```

### Barbed Hat (`BarbedHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Barbed`
- **Description**: +1 Damage, +1 Thorns, -1 max HP.
- **Mechanics**:
```gon
max_health -1
        passives {
            Thorns 1
            DamageUp 1
            Metal 1
        }
```

### Barbed Mask (`BarbedMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Barbed`
- **Description**: +1 Damage, +1 Thorns, -1 max HP.
- **Mechanics**:
```gon
max_health -1
        passives {
            Thorns 1
            DamageUp 1
            Metal 1
        }
```

### Barbed Necklace (`BarbedNeck`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Barbed`
- **Description**: +1 Damage, +1 Thorns, -1 max HP.
- **Mechanics**:
```gon
max_health -1
        passives {
            Thorns 1
            DamageUp 1
            Metal 1
        }
```

### Sludge Hat (`SludgeHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Sludge`
- **Description**: 
- **Mechanics**:
```gon
cursed true
        shield 1
        cha -1
```

### Sludge Mask (`SludgeMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `Sludge`
- **Description**: 
- **Mechanics**:
```gon
cursed true
        shield 1
        cha -1
```

### Sludge Necklace (`SludgeNeck`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `Sludge`
- **Description**: 
- **Mechanics**:
```gon
cursed true
        shield 1
        cha -1
```

### Cool Glasses (`CoolGlasses`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Cool`
- **Description**: Fragile
- **Mechanics**:
```gon
cha 2
        passives {
            Fragile 1
        }
```

### Cool Shirt (`CoolShirt`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Cool`
- **Description**: Fragile
- **Mechanics**:
```gon
cha 2
        passives {
            Fragile 1
        }
```

### Cool Hat (`CoolHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Cool`
- **Description**: Fragile
- **Mechanics**:
```gon
cha 2
        passives {
            Fragile 1
        }
```

### Paper Hat (`PaperHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Paper`
- **Description**: +1 Bleed Thorns. Your basic attack inflicts Bleed. Fragile, Brittle, Flammable, melts in water.
- **Mechanics**:
```gon
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
```

### Paper Mask (`PaperMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Paper`
- **Description**: +1 Bleed Thorns. Your basic attack inflicts Bleed. Fragile, Brittle, Flammable, melts in water.
- **Mechanics**:
```gon
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
```

### Paper Shoulder Pads (`PaperArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Paper`
- **Description**: +1 Bleed Thorns. Your basic attack inflicts Bleed. Fragile, Brittle, Flammable, melts in water.
- **Mechanics**:
```gon
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
```

### Cardboard Hat (`CardboardHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Cardboard`
- **Description**: Fragile, Flammable, Brittle when wet.
- **Mechanics**:
```gon
shield 2
        passives {
            Flammable 1
            Fragile 1
            BrittleDuringElement water
        }
```

### Cardboard Mask (`CardboardMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Cardboard`
- **Description**: Fragile, Flammable, Brittle when wet.
- **Mechanics**:
```gon
shield 2
        passives {
            Flammable 1
            Fragile 1
            BrittleDuringElement water
        }
```

### Cardboard Necklace (`CardboardArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Cardboard`
- **Description**: Fragile, Flammable, Brittle when wet.
- **Mechanics**:
```gon
shield 2
        passives {
            Flammable 1
            Fragile 1
            BrittleDuringElement water
        }
```

### Used Hat (`UsedHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Used`
- **Description**: 
- **Mechanics**:
```gon
shield 1
```

### Used Glasses (`UsedMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Used`
- **Description**: 
- **Mechanics**:
```gon
shield 1
```

### Used Shirt (`UsedArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Used`
- **Description**: 
- **Mechanics**:
```gon
shield 1
```

### Wood Hat (`WoodHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Wood`
- **Description**: +1 Thorns. Fragile, Flammable.
- **Mechanics**:
```gon
shield 2
        passives {
            Thorns 1
            Fragile 1
            Flammable 2
        }
```

### Wood Mask (`WoodMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Wood`
- **Description**: +1 Thorns. Fragile, Flammable.
- **Mechanics**:
```gon
shield 2
        passives {
            Thorns 1
            Fragile 1
            Flammable 2
        }
```

### Wood Shoulder Pads (`WoodArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Wood`
- **Description**: +1 Thorns. Fragile, Flammable.
- **Mechanics**:
```gon
shield 2
        passives {
            Thorns 1
            Fragile 1
            Flammable 2
        }
```

### Recycled Hat (`RecycledHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Recycled`
- **Description**: Brittle. Find a common item when this breaks.
- **Mechanics**:
```gon
shield 2
        passives {
            Brittle 1
            StatusOnBreak {
                FindItemFromPool common
            }
        }
```

### Recycled Mask (`RecycledMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Recycled`
- **Description**: Brittle. Find a common item when this breaks.
- **Mechanics**:
```gon
shield 2
        passives {
            Brittle 1
            StatusOnBreak {
                FindItemFromPool common
            }
        }
```

### Recycled Necklace (`RecycledArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Recycled`
- **Description**: Brittle. Find a common item when this breaks.
- **Mechanics**:
```gon
shield 2
        passives {
            Brittle 1
            StatusOnBreak {
                FindItemFromPool common
            }
            Metal 1
        }
```

### Rotten Meat Hat (`RottenHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Rotten`
- **Description**: Spawn a Charmed Maggot or Fly when you end your turn.
- **Mechanics**:
```gon
cha -1
        passives {
            SpawnEachTurn {
                chance 100%
                object [CharmedFly CharmedMaggot]
            }
        }
```

### Rotten Meat Mask (`RottenMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Rotten`
- **Description**: Spawn a Charmed Maggot or Fly when you end your turn.
- **Mechanics**:
```gon
cha -1
        passives {
            SpawnEachTurn {
                chance 100%
                object [CharmedFly CharmedMaggot]
            }
        }
```

### Rotten Meat Armor (`RottenArmor`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Rotten`
- **Description**: Spawn a Charmed Maggot or Fly when you end your turn.
- **Mechanics**:
```gon
cha -1
        passives {
            SpawnEachTurn {
                chance 100%
                object [CharmedFly CharmedMaggot]
            }
        }
```

### Jank Alloy Armor (`JankAlloyHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `JankAlloy`
- **Description**: +1 Brace. Brittle.
- **Mechanics**:
```gon
shield 2
        passives {
            Brace 1
            Brittle 1
            Metal 1
        }
```

### Jank Alloy Mask (`JankAlloyMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `JankAlloy`
- **Description**: +1 Brace. Brittle.
- **Mechanics**:
```gon
shield 2
        passives {
            Brace 1
            Brittle 1
            Metal 1
        }
```

### Jank Alloy Hat (`JankAlloyArmor`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `JankAlloy`
- **Description**: +1 Brace. Brittle.
- **Mechanics**:
```gon
shield 2
        passives {
            Brace 1
            Brittle 1
            Metal 1
        }
```

### Alloy Mask (`AlloyHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Alloy`
- **Description**: +1 Brace, +2 Thorns. Brittle.
- **Mechanics**:
```gon
shield 3
        passives {
            Brace 1
            Thorns 2
            Brittle 1
            Metal 1
        }
```

### Alloy Mask (`AlloyMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `Alloy`
- **Description**: +1 Brace, +2 Thorns. Brittle.
- **Mechanics**:
```gon
shield 3
        passives {
            Brace 1
            Thorns 2
            Brittle 1
            Metal 1
        }
```

### Alloy Armor (`AlloyArmor`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `Alloy`
- **Description**: +1 Brace, +2 Thorns. Brittle.
- **Mechanics**:
```gon
shield 3
        passives {
            Brace 1
            Thorns 2
            Brittle 1
            Metal 1
        }
```

### Advanced Alloy Hat (`AdvancedAlloyHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `AdvancedAlloy`
- **Description**: +2 Brace, +2 Thorns. Brittle.
- **Mechanics**:
```gon
shield 4
        passives {
            Brace 2
            Thorns 2
            Brittle 1
            Metal 1
        }
```

### Advanced Alloy Mask (`AdvancedAlloyMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `AdvancedAlloy`
- **Description**: +2 Brace, +2 Thorns. Brittle.
- **Mechanics**:
```gon
shield 4
        passives {
            Brace 2
            Thorns 2
            Brittle 1
            Metal 1
        }
```

### Advanced Alloy Armor (`AdvancedAlloyArmor`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `AdvancedAlloy`
- **Description**: +2 Brace, +2 Thorns. Brittle.
- **Mechanics**:
```gon
shield 4
        passives {
            Brace 2
            Thorns 2
            Brittle 1
            Metal 1
        }
```

### Elite Alloy Hat (`EliteAlloyHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `EliteAlloy`
- **Description**: +2 Brace, +3 Thorns, All Stats Up 1. Brittle.
- **Mechanics**:
```gon
shield 5
        passives {
            Brace 2
            Thorns 3
            AllStatsUp 1
            Brittle 1
            Metal 1
        }
```

### Elite Alloy Mask (`EliteAlloyMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `EliteAlloy`
- **Description**: +2 Brace, +3 Thorns, All Stats Up 1. Brittle.
- **Mechanics**:
```gon
shield 5
        passives {
            Brace 2
            Thorns 3
            AllStatsUp 1
            Brittle 1
            Metal 1
        }
```

### Elite Alloy Armor (`EliteAlloyArmor`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `EliteAlloy`
- **Description**: +2 Brace, +3 Thorns, All Stats Up 1. Brittle.
- **Mechanics**:
```gon
shield 5
        passives {
            Brace 2
            Thorns 3
            AllStatsUp 1
            Brittle 1
            Metal 1
        }
```

### Twine Hat (`TwineHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Twine`
- **Description**: +50% chance to Grapple units that contact you. Flammable.
- **Mechanics**:
```gon
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
```

### Twine Mask (`TwineMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Twine`
- **Description**: +50% chance to Grapple units that contact you. Flammable.
- **Mechanics**:
```gon
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
```

### Twine Armor (`TwineArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Twine`
- **Description**: +50% chance to Grapple units that contact you. Flammable.
- **Mechanics**:
```gon
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
```

### Rock Hat (`RockHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Brittle. Your basic attack has +1 Knockback. Gain coins when this breaks.
- **Mechanics**:
```gon
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
```

### Rock Mask (`RockMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Brittle. Your basic attack has +1 Knockback. Gain coins when this breaks.
- **Mechanics**:
```gon
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
```

### Rock Necklace (`RockArmor`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Brittle. Your basic attack has +1 Knockback. Gain coins when this breaks.
- **Mechanics**:
```gon
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
```

### Miner Hat (`MinerHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Miner`
- **Description**: Physical attacks can't miss.
- **Mechanics**:
```gon
shield 4
        passives {
            TrueShot 1
        }
```

### Miner Mask (`MinerMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Miner`
- **Description**: Poison Immunity.
- **Mechanics**:
```gon
shield 4
        passives {
            StatusImmunity Poison
            CantCatchDiseases 1
            CantSpreadDiseases 1
        }
```

### Miner Pack (`MinerArmor`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Miner`
- **Description**: Your basic attack has +1 Knockback. +1 Knockback damage.
- **Mechanics**:
```gon
passives {
            AddKnockbackDamage 1
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
```

### Gemstone Crown (`GemstoneHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Gemstone`
- **Description**: +1 Kinetic Spikes.
- **Mechanics**:
```gon
shield 1
        cha 1
        passives {
            KineticSpikes 1
        }
```

### Gemstone Mask (`GemstoneMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Gemstone`
- **Description**: +1 Kinetic Spikes.
- **Mechanics**:
```gon
shield 1
        cha 1
        passives {
            KineticSpikes 1
        }
```

### Gemstone Necklace (`GemstoneArmor`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Gemstone`
- **Description**: +1 Kinetic Spikes.
- **Mechanics**:
```gon
shield 1
        cha 1
        passives {
            KineticSpikes 1
        }
```

### Veiny Hat (`VeinyHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Veiny`
- **Description**: When you damage a Bleeding unit, gain +1 [img:spd].
- **Mechanics**:
```gon
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
```

### Veiny Mask (`VeinyMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Veiny`
- **Description**: When you damage a Bleeding unit, gain +1 [img:str].
- **Mechanics**:
```gon
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
```

### Veiny Necklace (`VeinyArmor`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Veiny`
- **Description**: When you damage a Bleeding unit, heal 3 HP.
- **Mechanics**:
```gon
passives {
            AddStatusToAllDamage {
                must_do_damage true
                Conditional_HasStatus {
                    status Bleed
                    FlatLeechIfDamaged 3
                }
            }
        }
```

### Leather Hood (`GimpHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Gimp`
- **Description**: Gain +2 Charge when you take damage.
- **Mechanics**:
```gon
passives {
            StatusOnTookDamage {
                Charge 2
            }
        }
```

### Ball Gag (`GimpMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Gimp`
- **Description**: Gain +2 Charge when you take damage.
- **Mechanics**:
```gon
passives {
            StatusOnTookDamage {
                Charge 2
            }
        }
```

### Leather Collar (`GimpArmor`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Gimp`
- **Description**: Gain +2 Charge when you take damage.
- **Mechanics**:
```gon
passives {
            StatusOnTookDamage {
                Charge 2
            }
        }
```

### Bionic Skull Plating (`BionicHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Bionic`
- **Description**: Fragile.
- **Mechanics**:
```gon
spd 3
        passives {
            Fragile 1
            Metal 1
        }
```

### Bionic Face Plating (`BionicMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Bionic`
- **Description**: Fragile.
- **Mechanics**:
```gon
spd 3
        passives {
            Fragile 1
            Metal 1
        }
```

### Bionic Neck Plating (`BionicArmor`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Bionic`
- **Description**: Fragile.
- **Mechanics**:
```gon
spd 3
        passives {
            Fragile 1
            Metal 1
        }
```

### Frontal Lobe Implant (`CyborgHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Cyborg`
- **Description**: 10% chance to teleport to a neighboring tile when targeted by an enemy.
- **Mechanics**:
```gon
int 1
		shield 3
        passives {
            ChanceToBackflip {
                ability ShadowstepDodge
                chance 10%
            }
            Metal 1
        }
```

### Optic Nerve Implant (`CyborgMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Cyborg`
- **Description**: +1 range, +1 reach.
- **Mechanics**:
```gon
int 1
		shield 3
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1
            Metal 1
        }
```

### Cerebellum Implant (`CyborgArmor`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Cyborg`
- **Description**: +10% Crit Chance.
- **Mechanics**:
```gon
int 1
		shield 3
        passives {
            CritChanceUp 10
            Metal 1
        }
```

### Lucky Hat (`LuckyHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Lucky`
- **Description**: Fragile.
- **Mechanics**:
```gon
lck 1
        passives {
            Fragile 1
        }
```

### Lucky Clover (`LuckyMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `[Lucky, Leafy]`
- **Description**: Fragile.
- **Mechanics**:
```gon
lck 1
        passives {
            Fragile 1
        }
```

### Lucky Horseshoe (`LuckyArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Lucky`
- **Description**: Fragile.
- **Mechanics**:
```gon
lck 1
        passives {
            Fragile 1
        }
```

### Fly Hat (`FlyHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Fly`
- **Description**: +10% Dodge Chance.
- **Mechanics**:
```gon
cursed true
        cha -1
        spd 3
        passives {
            AddTag bug
            ArmorDodgeChance 10%
        }
```

### Fly Mask (`FlyMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `Fly`
- **Description**: +10% Dodge Chance.
- **Mechanics**:
```gon
cursed true
        dex 3
        cha -1
        passives {
            AddTag bug
            ArmorDodgeChance 10%
        }
```

### Fly Carapace (`FlyNeck`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `Fly`
- **Description**: +10% Dodge Chance.
- **Mechanics**:
```gon
cursed true
        con 3
        cha -1
        passives {
            AddTag bug
            ArmorDodgeChance 10%
        }
```

### Face Grub (`FaceGrub`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Grub`
- **Description**: When your [img:shield] is depleted, this transforms into a Maggot familiar.
- **Mechanics**:
```gon
shield 3
        passives {
            DropAsFamiliarOnArmorBreak FaceGrubFamiliar
        }
```

### Head Grub (`HeadGrub`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Grub`
- **Description**: When your [img:shield] is depleted, this transforms into a Maggot familiar.
- **Mechanics**:
```gon
shield 3
        passives {
            DropAsFamiliarOnArmorBreak HeadGrubFamiliar
        }
```

### Neck Grub (`NeckGrub`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Grub`
- **Description**: When your [img:shield] is depleted, this transforms into a Maggot familiar.
- **Mechanics**:
```gon
shield 3
        passives {
            DropAsFamiliarOnArmorBreak NeckGrubFamiliar
        }
```

### Crimson Mask (`CrimsonMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Meat`
- **Description**: +1 Damage. Gain +1 Damage when you kill an enemy.
- **Mechanics**:
```gon
passives {
            DamageUp 1
            StatusOnKillEnemy {
                DamageUp 1
            }
        }
```

### CrimsonMask_Cursed (`CrimsonMask_Cursed`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of CrimsonMask
        cursed true
```

### Red Cap (`RedCap`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Meat`
- **Description**: +1 Damage. Gain +1 Damage when you kill an enemy.
- **Mechanics**:
```gon
passives {
            DamageUp 1
            StatusOnKillEnemy {
                DamageUp 1
            }
        }
```

### RedCap_Cursed (`RedCap_Cursed`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of RedCap
        cursed true
```

### Pound of Flesh (`PoundOfFlesh`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Meat`
- **Description**: +1 Damage. Gain +1 Damage when you kill an enemy.
- **Mechanics**:
```gon
passives {
            DamageUp 1
            StatusOnKillEnemy {
                DamageUp 1
            }
        }
```

### PoundOfFlesh_Cursed (`PoundOfFlesh_Cursed`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of PoundOfFlesh
        cursed true
```

### Fecal Mask (`FecalMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Fecal`
- **Description**: Poisonous 1.
- **Mechanics**:
```gon
cha -1
        passives {
            PoisonThorns 1
        }
```

### Fecal Hood (`FecalHood`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Fecal`
- **Description**: Poisonous 1.
- **Mechanics**:
```gon
cha -1
        passives {
            PoisonThorns 1
        }
```

### Fecal Necklace (`FecalNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Fecal`
- **Description**: Poisonous 1.
- **Mechanics**:
```gon
cha -1
        passives {
            PoisonThorns 1
        }
```

### FecalMask_Cursed (`FecalMask_Cursed`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of FecalMask
        cursed true
```

### FecalHood_Cursed (`FecalHood_Cursed`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of FecalHood
        cursed true
```

### FecalNecklace_Cursed (`FecalNecklace_Cursed`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of FecalNecklace
        cursed true
```

### Leafy Mask (`LeafyMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Leafy`
- **Description**: While standing in tall grass, you have +40% Dodge Chance.
- **Mechanics**:
```gon
cha 1
        passives {
            PassiveWhenOnTile {
                tile [TallGrassTile TallFlowerTile]
                passives {
                    DodgeChance_Status 40
                }
            }
        }
```

### Leafy Hat (`LeafyHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Leafy`
- **Description**: While standing in tall grass, you have +3 Mana Regen and +1 Health Regen.
- **Mechanics**:
```gon
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
```

### Leafy Necklace (`LeafyNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Leafy`
- **Description**: While standing in tall grass, you have +3 Health Regen and +1 Mana Regen.
- **Mechanics**:
```gon
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
```

### Cactus Mask (`CactusMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Cactus`
- **Description**: +3 Thorns, Brittle. Gain +2 [img:con] permanently and heal 10 HP when this breaks.
- **Mechanics**:
```gon
passives {
            Thorns 3
            Brittle 1
            StatusOnBreak {
                PermanentConstitution 2
                HealthGain 10
                ChangeTilesUnder WaterTile
            }
        }
```

### Cactus Hat (`CactusHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Cactus`
- **Description**: +3 Thorns, Brittle. Gain +2 [img:con] permanently and heal 10 HP when this breaks.
- **Mechanics**:
```gon
passives {
            Thorns 3
            Brittle 1
            StatusOnBreak {
                PermanentConstitution 2
                HealthGain 10
                ChangeTilesUnder WaterTile
            }
        }
```

### Cactus Necklace (`CactusNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Cactus`
- **Description**: +3 Thorns, Brittle. Gain +2 [img:con] permanently and heal 10 HP when this breaks.
- **Mechanics**:
```gon
passives {
            Thorns 3
            Brittle 1
            StatusOnBreak {
                PermanentConstitution 2
                HealthGain 10
                ChangeTilesUnder WaterTile
            }
        }
```

### Face Wrap (`FaceWrap`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Mummy`
- **Description**: +1 Health Regen. When downed, revive with 15% HP at the end of the round.
- **Mechanics**:
```gon
passives {
            HealthRegenUp 1
            DelayedAutoRevive {
                rounds 1
                health 15%
            }
        }
```

### Head Wrap (`HeadWrap`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Mummy`
- **Description**: +1 Health Regen. When downed, revive with 15% HP at the end of the round.
- **Mechanics**:
```gon
passives {
            HealthRegenUp 1
            DelayedAutoRevive {
                rounds 1
                health 15%
            }
        }
```

### Neck Wrap (`NeckWrap`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Mummy`
- **Description**: +1 Health Regen. When downed, revive with 15% HP at the end of the round.
- **Mechanics**:
```gon
passives {
            HealthRegenUp 1
            DelayedAutoRevive {
                rounds 1
                health 15%
            }
        }
```

### Man's Glasses (`ManGlasses`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Man`
- **Description**: Physical attacks can't miss. Spawn 1-2 extra pickups at the start of each battle.
- **Mechanics**:
```gon
passives {
            TrueShot 1
            SpawnExtraThingsOnBattleStart {
                object RandomPickup
                number [1 2]
            }
        }
```

### Man's Hairpiece (`ManHair`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Man`
- **Description**: 
- **Mechanics**:
```gon
cha 2
        passives {
        }
```

### Man's Tie (`ManTie`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Man`
- **Description**: 
- **Mechanics**:
```gon
lck 2
        passives {
        }
```

### Flower Mask (`FlowerMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Flower`
- **Description**: Your basic attack has a +5% chance to inflict Entangled. Plants flowers on each tile you move through. [s:.7](Stacking this effect plants flowers in a wider area.)[/s]
- **Mechanics**:
```gon
passives {
            StackingFlowerTrail {
                stacks 1
                stack_key FLOWER_SET
            }
            AddStatusToBasicAttack {
                Tangled [1, .05]
            }
        }
```

### Flower Hat (`FlowerHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Flower`
- **Description**: Your basic attack has a +5% chance to inflict Entangled. Plants flowers on each tile you move through. [s:.7](Stacking this effect plants flowers in a wider area.)[/s]
- **Mechanics**:
```gon
passives {
            StackingFlowerTrail {
                stacks 1
                stack_key FLOWER_SET
            }
            AddStatusToBasicAttack {
                Tangled [1, .05]
            }
        }
```

### Flower Necklace (`FlowerNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Flower`
- **Description**: Your basic attack has a +5% chance to inflict Entangled. Plants flowers on each tile you move through. [s:.7](Stacking this effect plants flowers in a wider area.)[/s]
- **Mechanics**:
```gon
passives {
            StackingFlowerTrail {
                stacks 1
                stack_key FLOWER_SET
            }
            AddStatusToBasicAttack {
                Tangled [1, .05]
            }
        }
```

### Human Face (`HumanFleshMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `HumanFlesh`
- **Description**: Your basic attack has a +25% chance to inflict Fear. Spawn a food pickup at the start of each battle.
- **Mechanics**:
```gon
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
```

### Human Scalp (`HumanFleshHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `HumanFlesh`
- **Description**: Your crit hits inflict Fear. Spawn a food pickup at the start of each battle.
- **Mechanics**:
```gon
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
```

### Human Hide (`HumanFleshArmor`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `HumanFlesh`
- **Description**: Units that contact or attack you have a +25% chance to be Feared. Spawn a food pickup at the start of each battle.
- **Mechanics**:
```gon
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
```

### Face Tentacle (`TentacleMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Tentacle`
- **Description**: Your basic attack has a +33% chance to inflict Entangle.
- **Mechanics**:
```gon
shield 2
        passives {
            AddStatusToBasicAttack {
                Tangled [1, .33]
            }
        }
```

### Head Tentacle (`TentacleHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Tentacle`
- **Description**: Your basic attack pulls you towards units or objects it hits.
- **Mechanics**:
```gon
shield 2
        passives {
            AddStatusToBasicAttack {
                PullSourceToTarget 1
            }
        }
```

### Back Tentacles (`TentacleNeck`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Tentacle`
- **Description**: Counterattack ranged attackers with a tentacle slap.
- **Mechanics**:
```gon
shield 2
        passives {
            CounterAttack {
                ranged_only true
                ability neck_TentacleArmorCounter
            }
        }
```

### Obelisk Jewel (`ObeliskMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Obelisk`
- **Description**: Gain +2 [img:int] and +2 [img:cha] when you kill a unit. Stats obtained this way are lost when you take damage.
- **Mechanics**:
```gon
divine_shield 1
        passives {
            StatusOnKill {
                BrittleIntelligenceUp 2
                BrittleCharismaUp 2
            }
        }
```

### Obelisk Helmet (`ObeliskHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Obelisk`
- **Description**: Gain +2 [img:dex] and +2 [img:lck] when you kill a unit. Stats obtained this way are lost when you take damage.
- **Mechanics**:
```gon
divine_shield 1
        passives {
            StatusOnKill {
                BrittleDexterityUp 2
                BrittleLuckUp 2
            }
        }
```

### Obelisk Pauldrons (`ObeliskArmor`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Obelisk`
- **Description**: Gain +2 [img:str], +2 [img:spd] and +2 [img:con] when you kill a unit. Stats obtained this way are lost when you take damage.
- **Mechanics**:
```gon
divine_shield 1
        passives {
            StatusOnKill {
                BrittleStrengthUp 2
                BrittleSpeedUp 2
                BrittleConstitutionUp 2
            }
        }
```

### Experimental Treatment (`ExperimentalMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Experimental`
- **Description**: 
- **Mechanics**:
```gon
str_aux_initialize random_seed
        passives {
            RandomSeededStatModifier [2 -1] // hard coded in SpawnDatabase::get_item_stats
        }
```

### Experimental Treatment (`ExperimentalHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Experimental`
- **Description**: 
- **Mechanics**:
```gon
str_aux_initialize random_seed
        passives {
            RandomSeededStatModifier [2 -1] // hard coded in SpawnDatabase::get_item_stats
        }
```

### Experimental Treatment (`ExperimentalNeck`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Experimental`
- **Description**: 
- **Mechanics**:
```gon
str_aux_initialize random_seed
        passives {
            RandomSeededStatModifier [2 -1] // hard coded in SpawnDatabase::get_item_stats
        }
```

### Rocky Mask (`RockyMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Breaks when [img:shield] is depleted. When this breaks, gain Bruise 3.
- **Mechanics**:
```gon
shield 10
        passives {
            RockyArmorPassive 1
            StatusOnBreak {
                Bruise 3
            }
        }
```

### Rocky Hat (`RockyHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Breaks when [img:shield] is depleted. When this breaks, gain Bruise 3.
- **Mechanics**:
```gon
shield 10
        passives {
            RockyArmorPassive 1
            StatusOnBreak {
                Bruise 3
            }
        }
```

### Rocky Necklace (`RockyNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Breaks when [img:shield] is depleted. When this breaks, gain Bruise 3.
- **Mechanics**:
```gon
shield 10
        passives {
            RockyArmorPassive 1
            StatusOnBreak {
                Bruise 3
            }
        }
```

### Space Helmet (`SpaceHelmet`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Space`
- **Description**: +1 Brace. 30% chance to block negative status effects.
- **Mechanics**:
```gon
passives {
            Brace 1
            BlockNegativeStatus 30%
        }
```

### Space Antenna (`SpaceAntenna`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Space`
- **Description**: Gain 0-4 mana at start of each turn.
- **Mechanics**:
```gon
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
```

### Space Boosters (`SpaceBoosters`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Space`
- **Description**: Your movement action is Jump.
- **Mechanics**:
```gon
spd 3
        passives {
            Metal 1
            ReplaceBasicMove BasicJump
        }
```

### Tiny Planet (`TinyPlanet`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Planet`
- **Description**: Your basic attack pulls units towards you. Inflict Bruise on units who contact you.
- **Mechanics**:
```gon
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
```

### Mini Moon (`MiniMoon`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Planet`
- **Description**: Your basic attack has a +25% chance to shoot an asteroid at what it hits. +10% chance to Block.
- **Mechanics**:
```gon
passives {
            ChanceToBlock 10%
            AddStatusToBasicAttack {
                ForceUseAbilityOnTarget {
                    chance 25%
                    ability head_MiniMoonArmorAsteroid
                }
            }
        }
```

### Asteroid Belt (`AsteroidBelt`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Planet`
- **Description**: +2 Brace. +10% chance to block damage.
- **Mechanics**:
```gon
passives {
            Brace 2
            ChanceToBlock 10%
        }
```

### Debris Mask (`DebrisMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Debris`
- **Description**: +2 range, +1 Kinetic Spikes.
- **Mechanics**:
```gon
shield 2
        dex -1
        passives {
            Metal 1
            AddBonusRange 2
            KineticSpikes 1
        }
```

### Debris Hat (`DebrisHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Debris`
- **Description**: +2 range, +1 Kinetic Spikes.
- **Mechanics**:
```gon
shield 2
        dex -1
        passives {
            Metal 1
            AddBonusRange 2
            KineticSpikes 1
        }
```

### Debris Armor (`DebrisArmor`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Debris`
- **Description**: +2 range, +1 Kinetic Spikes.
- **Mechanics**:
```gon
shield 2
        dex -1
        passives {
            Metal 1
            AddBonusRange 2
            KineticSpikes 1
        }
```

### Dry Bone Mask (`DryBoneMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Bone`
- **Description**: +1 Thorns. Inflict Bruise 1 on units that contact you.
- **Mechanics**:
```gon
shield 3
        passives {
            Thorns 1
            MeleeRevengeDamage {
                effects {
                    Bruise 1
                }
            }
        }
```

### Dry Bone Helm (`DryBoneHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Bone`
- **Description**: +1 Thorns. Inflict Bruise 1 on units that contact you.
- **Mechanics**:
```gon
shield 3
        passives {
            Thorns 1
            MeleeRevengeDamage {
                effects {
                    Bruise 1
                }
            }
        }
```

### Dry Bone Necklace (`DryBoneNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Bone`
- **Description**: +1 Thorns. Inflict Bruise 1 on units that contact you.
- **Mechanics**:
```gon
shield 3
        passives {
            Thorns 1
            MeleeRevengeDamage {
                effects {
                    Bruise 1
                }
            }
        }
```

### Protection Transmitter (`ProtectionTransmitter`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Transmitter`
- **Description**: Bruise 2. All allies gain Brace 1.
- **Mechanics**:
```gon
passives {
            Metal 1
            Bruise 2
            StatusAlliesOnBattleStart {
                Brace 1
            }
        }
```

### Damage Transmitter (`DamageTransmitter`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Transmitter`
- **Description**: -2 Damage. All allies gain +1 Damage.
- **Mechanics**:
```gon
passives {
            Metal 1
            DamageUp -2
            StatusAlliesOnBattleStart {
                DamageUp 1
            }
        }
```

### Energy Transmitter (`EnergyTransmitter`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Transmitter`
- **Description**: All allies gain +2 [img:spd].
- **Mechanics**:
```gon
spd -4
        passives {
            Metal 1
            StatusAlliesOnBattleStart {
                SpeedUp 2
            }
        }
```

### Thrumming Circlet (`ThrummingCirclet`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Thrumming`
- **Description**: If you end your turn without using your basic attack, gain +1 Damage and +1 Thorns.
- **Mechanics**:
```gon
passives {
            StatusOnTurnEndIfDidntCastAbilityTypes {
                type attack
                DamageUp 1
                Thorns 1
            }
        }
```

### Thrumming Spectacles (`ThrummingSpectacles`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Thrumming`
- **Description**: If you end your turn without using your movement action, gain +1 Health Regen and +1 [img:shield].
- **Mechanics**:
```gon
passives {
            StatusOnTurnEndIfDidntCastAbilityTypes {
                type move
                HealthRegenUp 1
                Shield 1
            }
        }
```

### Thrumming Charm (`ThrummingCharm`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Thrumming`
- **Description**: If you end your turn without casting any spells, gain +1 Magic Damage and +1 Charge.
- **Mechanics**:
```gon
passives {
            StatusOnTurnEndIfDidntCastAbilityTypes {
                type spell
                SpellDamageUp 1
                Charge 1
            }
        }
```

### Witch's Hat (`WitchesHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Witch`
- **Description**: +1 Magic Damage.
- **Mechanics**:
```gon
passives {
            SpellDamageUp 1
        }
```

### Witch's Nose (`WitchesNose`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Witch`
- **Description**: +1 Magic Damage.
- **Mechanics**:
```gon
passives {
            SpellDamageUp 1
        }
```

### Witch's Cape (`WitchesCape`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Witch`
- **Description**: +1 Magic Damage.
- **Mechanics**:
```gon
passives {
            SpellDamageUp 1
        }
```

### Stunning Haircut (`StunningHaircut`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Stunning`
- **Description**: Your face and neck item effects are doubled.
- **Mechanics**:
```gon
passives {
            FaceArmorPassiveMultiplierBonus 1
            NeckArmorPassiveMultiplierBonus 1
        }
```

### Stunning Chain (`StunningChain`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Stunning`
- **Description**: Your head and face item effects are doubled.
- **Mechanics**:
```gon
passives {
            Metal 1
            FaceArmorPassiveMultiplierBonus 1
            HeadArmorPassiveMultiplierBonus 1
        }
```

### Stunning Beard (`StunningBeard`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Stunning`
- **Description**: Your head and neck item effects are doubled.
- **Mechanics**:
```gon
passives {
            NeckArmorPassiveMultiplierBonus 1
            HeadArmorPassiveMultiplierBonus 1
        }
```

### Superhero Hat (`SuperheroHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Superhero`
- **Description**: +2 Health Regen.
- **Mechanics**:
```gon
divine_shield 1
        passives {
            HealthRegenUp 2
        }
```

### Superhero Cape (`SuperheroCape`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Superhero`
- **Description**: Flying.
- **Mechanics**:
```gon
spd 3
        passives {
            Flying 1
        }
```

### Superhero Mask (`SuperheroMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Superhero`
- **Description**: +1 Damage. Your basic attack knocks units into the air, lobbing them back 3 tiles.
- **Mechanics**:
```gon
passives {
            DamageUp 1
		    AddStatusToBasicAttack {
                KnockUpAndAway {
                    stacks 5
                    distance 3
                }
            }
        }
```

### Lead Helmet (`LeadHelmet`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Lead`
- **Description**: 
- **Mechanics**:
```gon
shield 6
        spd -1
        passives {
            Metal 1
        }
```

### Lead Shoulder Pads (`LeadShoulderPads`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Lead`
- **Description**: 
- **Mechanics**:
```gon
shield 6
        spd -1
        passives {
            Metal 1
        }
```

### Lead Mask (`LeadMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Lead`
- **Description**: 
- **Mechanics**:
```gon
shield 6
        spd -1
        passives {
            Metal 1
        }
```

### Scary Baby (`ScaryBaby`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Baby`
- **Description**: Inflict Fear 2 on a random enemy at the start of each battle.
- **Mechanics**:
```gon
passives {
            StatusRandomEnemiesOnBattleStart {
                count 1
                Fear 2
            }
        }
```

### Charming Baby (`CharmingBaby`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Baby`
- **Description**: Inflict Charmed 2 on a random enemy at the start of each battle.
- **Mechanics**:
```gon
passives {
            StatusRandomEnemiesOnBattleStart {
                count 1
                Charmed 2
            }
        }
```

### Freezing Baby (`FreezingBaby`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Baby`
- **Description**: Inflict Freeze 2 on a random enemy at the start of each battle.
- **Mechanics**:
```gon
passives {
            StatusRandomEnemiesOnBattleStart {
                count 1
                Freeze 2
            }
        }
```

### Obi (`Obi`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Ninja`
- **Description**: Start battle with +2 bonus moves.
- **Mechanics**:
```gon
passives {
            MoveQuivered 2
        }
```

### Fukumen (`Fukumen`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Ninja`
- **Description**: Counter the first 2 attacks you receive each battle.
- **Mechanics**:
```gon
passives {
            CounterNextAttacks 2
        }
```

### Zukin (`Zukin`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Ninja`
- **Description**: Start battle with +2 Backflip.
- **Mechanics**:
```gon
passives {
            BackflipWhenTargeted {
                stacks 2
                ability BackflipDodge
            }
        }
```

### Prowler's Cap (`ProwlersCap`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Prowler`
- **Description**: Backstabs have +25% Crit Chance.
- **Mechanics**:
```gon
passives {
            BackstabCritChance .25
        }
```

### Prowler's Mask (`ProwlersMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Prowler`
- **Description**: Backstabs inflict Bleed 1.
- **Mechanics**:
```gon
passives {
            AddStatusToBackstabs {
                Bleed 1
            }
        }
```

### Prowler's Vial (`ProwlersVial`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Prowler`
- **Description**: Backstabs heal you by 2 HP.
- **Mechanics**:
```gon
passives {
            StatusOnBackstab {
                HealthGain 2
            }
        }
```

### Mage's Hat (`MageHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Mage`
- **Description**: Gain +1 Charge each time you cast a spell.
- **Mechanics**:
```gon
int 1
        passives {
            StatusOnCastSpell {
                Charge 1
            }
        }
```

### Mage's Robe (`MageRobe`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Mage`
- **Description**: Gain +1 Charge when you deal damage with your basic attack.
- **Mechanics**:
```gon
int 1
        passives {
            AddStatusToBasicAttack {
                ApplyToSource {
                    Charge 1
                }
            }
        }
```

### Mage's Scarf (`MageScarf`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Mage`
- **Description**: Gain +1 Charge each time an enemy dies.
- **Mechanics**:
```gon
int 1
        passives {
            StatusOnEnemyDeath {
                Charge 1
            }
        }
```

### Thief's Hood (`ThiefHood`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Thief`
- **Description**: +5% Dodge Chance and +5% Crit Chance. Your basic attack inflicts Bleed.
- **Mechanics**:
```gon
passives {
            ArmorDodgeChance 5%
            CritChanceUp 5
            AddStatusToBasicAttack {
                Bleed 1
            }
        }
```

### Thief's Tattoo (`ThiefTattoo`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Thief`
- **Description**: +5% Dodge Chance and +5% Crit Chance. Your basic attack inflicts Poison.
- **Mechanics**:
```gon
passives {
            ArmorDodgeChance 5%
            CritChanceUp 5
            AddStatusToBasicAttack {
                Poison 1
            }
        }
```

### Thief's Cloak (`ThiefCloak`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Thief`
- **Description**: +10% Dodge Chance and +10% Crit Chance.
- **Mechanics**:
```gon
passives {
            ArmorDodgeChance 10%
            CritChanceUp 10
        }
```

### Fighter's Helm (`FighterHelm`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Fighter`
- **Description**: +15% chance to refresh your basic attack, movement, weapon and trinket actions when you get a kill.
- **Mechanics**:
```gon
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
```

### Fighter's Scar (`FighterScar`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Fighter`
- **Description**: +15% chance to refresh your basic attack, movement, weapon and trinket actions when you get a kill.
- **Mechanics**:
```gon
shield 2
        passives {
            StatusOnKill {
                Conditional_GoodRoll {
                    odds 15%
                    ForceUseAbility_NonStack Endeavor_Auto
                }
            }
        }
```

### Fighter's Shoulder Pad (`FighterShoulderPad`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Fighter`
- **Description**: +15% chance to refresh your basic attack, movement, weapon and trinket actions when you get a kill.
- **Mechanics**:
```gon
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
```

### Cleric's Mitre (`ClericHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Cleric`
- **Description**: Your heals heal for 2 extra.
- **Mechanics**:
```gon
shield 2
        passives {
            BoostHeals 2
        }
```

### Cleric's Tears (`ClericTears`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Cleric`
- **Description**: Gain +1 [img:divineshield] each time an ally is downed.
- **Mechanics**:
```gon
divine_shield 1
        passives {
            StatusOnAllyCatDeath {
                DivineShield 1
            }
        }
```

### Cleric's Relic (`ClericRelic`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Cleric`
- **Description**: +1 Brace. +15% chance to inflict Fear on units that contact or attack you.
- **Mechanics**:
```gon
passives {
            Brace 1
            RevengeDamage {
                effects {
                    Fear [1, .15]
                }
            }
        }
```

### Tank's Helmet (`TankHelmet`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Tank`
- **Description**: +1 Knockback damage.
- **Mechanics**:
```gon
shield 1
        passives {
            Metal 1
            AddKnockbackDamage 1
        }
```

### Tank's Tattoo (`TankTattoo`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Tank`
- **Description**: All Knockback inflicted by you is increased by 2.
- **Mechanics**:
```gon
passives {
            AmplifyKnockback 2
        }
```

### Tank's Pads (`TankPads`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Tank`
- **Description**: Your knockback damage has a +10% chance to inflict Stun.
- **Mechanics**:
```gon
shield 2
        passives {
            Metal 1
            AddStatusToKnockbackDamage {
                Stun [1, .1]
            }
        }
```

### Hunter's Cap (`HunterCap`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Hunter`
- **Description**: Your familiars gain All Stats Up.
- **Mechanics**:
```gon
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
```

### Hunter's Monocle (`HunterMonocle`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Hunter`
- **Description**: +2 range.
- **Mechanics**:
```gon
passives {
            AddBonusRange 2
        }
```

### Hunter's Quiver (`HunterQuiver`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Hunter, Leather]`
- **Description**: Start each battle with 2 bonus attacks.
- **Mechanics**:
```gon
passives {
            Quivered 2
        }
```

### Mystic Eye (`MysticEye`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Psychic`
- **Description**: +25% chance to reflect projectiles. Your tile-targeted spells have +2 range.
- **Mechanics**:
```gon
passives {
            IncreaseSpellRange 2
            ReflectProjectiles 25%
        }
```

### Tinfoil Hat (`TinfoilHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `[Psychic, Scrap]`
- **Description**: You are immune to Charm, Madness, Fear and Confusion.
- **Mechanics**:
```gon
shield 2
        passives {
            Metal 1
            CharmImmunity 1 // this covers Charm, Madness and other charm-like effects
            StatusImmunity [Fear Confusion PermanentConfusion]
        }
```

### Diviner's Cloth (`DivinersCloth`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Psychic, Rag]`
- **Description**: Adjacent allies have +25% Dodge Chance. Give +1 Charge to all adjacent allies at the end of your turn.
- **Mechanics**:
```gon
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
```

### Death Mask (`DeathMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Necromancer`
- **Description**: Get downed at the start of each battle, then revive at the end of the first round with full HP and +2 [img:shield].
- **Mechanics**:
```gon
passives {
            StatusOnBattleStart {
                SafeDie 1
                ReviveNextRound {
                    revive_health 100%
                    Shield 2
                }
            }
        }
```

### Spider Hat (`SpiderHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Necromancer`
- **Description**: When you destroy a corpse, spawn 2 Spiderlings.
- **Mechanics**:
```gon
passives {
            SpawnObjectOnPopCorpse {
                object CharmedTinySpider
                count 2
                except_tiny true
            }
        }
```

### Leech Necklace (`LeechNecklace`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Necromancer, Leech]`
- **Description**: Your spells inflict Leech 1 against enemies.
- **Mechanics**:
```gon
passives {
            AddStatusToSpells {
                Conditional_Enemy {
                    Leeches 1
                }
            }
        }
```

### Face Brand (`FaceBrand`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Monk`
- **Description**: Each time you use your basic attack, gain +1 [img:shield]. [s:.7](This counts as an empty armor slot.)[/s]
- **Mechanics**:
```gon
weightless true
        passives {
            AddSelfStatusToBasicAttack {
                Shield 1
            }
        }
```

### Head Brand (`HeadBrand`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Monk`
- **Description**: Your movement action is Jump. If you land on a unit, deal 1 damage to it and bounce to an adjacent tile. [s:.7](This counts as an empty armor slot.)[/s]
- **Mechanics**:
```gon
weightless true
        passives {
            ReplaceBasicMove head_HeadBrandJump
        }
```

### Prayer Beads (`PrayerBeads`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Monk, Twine]`
- **Description**: Each time you take damage, gain +3 Brace until your next turn. [s:.7](This counts as an empty armor slot.)[/s]
- **Mechanics**:
```gon
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
```

### Scrapper's Mask (`ScrappersMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `[Tinkerer, Scrap]`
- **Description**: When you break an item, gain +3 [img:shield].
- **Mechanics**:
```gon
shield 3
        passives {
            Metal 1
            StatusOnBreakItem {
                Shield 3
            }
        }
```

### Scrapper's Hat (`ScrappersHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `[Tinkerer, Scrap]`
- **Description**: When you break an item, spawn 3 random pickups.
- **Mechanics**:
```gon
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
```

### Scrapper's Backpack (`ScrappersBackpack`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Tinkerer, Survivalist]`
- **Description**: When you break an item, recover it at the end of the battle with 1 durability. [s:.7](Excludes temporary items)[/s]
- **Mechanics**:
```gon
passives {
            ReclaimItemOnBreak 1
        }
```

### Iron Jaw (`IronJaw`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `[Butcher, Tinkerer]`
- **Description**: Counterattack melee attackers with a bite that deals 3 damage with Lifesteal.
- **Mechanics**:
```gon
shield 3
        passives {
            Metal 1
            CounterAttack {
                ability head_IronJaw
            }
        }
```

### Flesh Shroud (`FleshShroud`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `[Butcher, HumanFlesh]`
- **Description**: Gain +1 [img:shield] each time you heal. When you kill a unit or destroy a corpse, it becomes meat.
- **Mechanics**:
```gon
passives {
            KillsToMeat Food
            StatusOnHealed {
                Shield 1
            }
        }
```

### Hooked Necklace (`HookedNecklace`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Butcher`
- **Description**: +2 Thorns. Cleave units that contact you.
- **Mechanics**:
```gon
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
```

### Greenman Mask (`GreenmanMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `[Druid, Leafy]`
- **Description**: +3 Brace while standing in tall grass. +3 Mana Regen while standing in water.
- **Mechanics**:
```gon
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
```

### Mushroom Hat (`MushroomHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Druid`
- **Description**: Inflict Confusion 2 on units that contact or attack you. Familiars you spawn inflict Confusion.
- **Mechanics**:
```gon
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
```

### Ring of Mushrooms (`RingOfMushrooms`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Druid, Twine]`
- **Description**: All of your area abilities gain +1 area.
- **Mechanics**:
```gon
passives {
            AOEBonus 1
        }
```

### Ordinary Whiskers (`CatWhiskers`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Collarless`
- **Description**: 
- **Mechanics**:
```gon
str 1
        dex 1
        int 1
        con 1
        spd 1
        lck 1
        cha 1
        passives {
        }
```

### Normal Ears (`CatEars`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Collarless`
- **Description**: 
- **Mechanics**:
```gon
str 1
        dex 1
        int 1
        con 1
        spd 1
        lck 1
        cha 1
        passives {
        }
```

### Mundane Collar (`CatCollar`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Collarless, Leather]`
- **Description**: 
- **Mechanics**:
```gon
str 1
        dex 1
        int 1
        con 1
        spd 1
        lck 1
        cha 1
        passives {
        }
```

### Clown Makeup (`ClownMakeup`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Jester`
- **Description**: Triple the effects of your Head armor.
- **Mechanics**:
```gon
lck -3
        passives {
            HeadArmorPassiveMultiplierBonus 2
        }
```

### Cap and Bells (`CapAndBells`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Jester`
- **Description**: Triple the effects of your Trinket.
- **Mechanics**:
```gon
lck -3
        passives {
            TrinketPassiveMultiplierBonus 2
            TrinketActiveEffectsMultiplierBonus 2
        }
```

### Ruffle (`Ruffle`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Jester`
- **Description**: Triple the effects of your Face armor.
- **Mechanics**:
```gon
lck -3
        passives {
            FaceArmorPassiveMultiplierBonus 2
        }
```

### Feathered Veil (`FeatheredVeil`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Feathered`
- **Description**: Counterattack melee attackers.
- **Mechanics**:
```gon
passives {
            CounterAttack {
                melee_only true
                ability attack
            }
        }
```

### Feathered Cap (`FeatheredCap`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Feathered`
- **Description**: 
- **Mechanics**:
```gon
spd 4
        passives {
        }
```

### Feathered Necklace (`FeatheredNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Feathered`
- **Description**: +15% Dodge Chance.
- **Mechanics**:
```gon
passives {
            ArmorDodgeChance 15%
        }
```

### The Mind (`TheMind`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Godhead`
- **Description**: 
- **Mechanics**:
```gon
int 7
```

### The Body (`TheBody`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Godhead`
- **Description**: 
- **Mechanics**:
```gon
con 7
```

### The Soul (`TheSoul`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Godhead`
- **Description**: 
- **Mechanics**:
```gon
lck 7
```

### Brick Hat (`BrickHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Brick`
- **Description**: Inflict Bruise 1 on units that contact you.
- **Mechanics**:
```gon
shield 4
		spd -1
		passives {
			MeleeRevengeDamage {
				effects {
					Bruise 1
				}
			}
		}
```

### Brick Mask (`BrickMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Brick`
- **Description**: Inflict Bruise 1 on units that contact you.
- **Mechanics**:
```gon
shield 4
		spd -1
		passives {
			MeleeRevengeDamage {
				effects {
					Bruise 1
				}
			}
		}
```

### Brick Necklace (`BrickNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Brick`
- **Description**: Inflict Bruise 1 on units that contact you.
- **Mechanics**:
```gon
shield 4
		spd -1
		passives {
			MeleeRevengeDamage {
				effects {
					Bruise 1
				}
			}
		}
```

### Slimy Hat (`SlimyHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Slimy`
- **Description**: +15% chance to catch projectiles. Inflict Immobile 1 on units that contact you.
- **Mechanics**:
```gon
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
```

### Slimy Mask (`SlimyMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Slimy`
- **Description**: +15% chance to catch projectiles. Inflict Immobile 1 on units that contact you.
- **Mechanics**:
```gon
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
```

### Slimy Necklace (`SlimyNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Slimy`
- **Description**: +15% chance to catch projectiles. Inflict Immobile 1 on units that contact you.
- **Mechanics**:
```gon
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
```

### Rat Hat (`RatHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Rat`
- **Description**: Start battle with a Charmed Pinky.
- **Mechanics**:
```gon
passives {
			SpawnOnBattleStart {
				object CharmedPinky
				number 1
			}
		}
```

### Rat Mask (`RatMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Rat`
- **Description**: Start battle with a Charmed Pinky.
- **Mechanics**:
```gon
passives {
			SpawnOnBattleStart {
				object CharmedPinky
				number 1
			}
		}
```

### Rat Necklace (`RatNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Rat`
- **Description**: Start battle with a Charmed Pinky.
- **Mechanics**:
```gon
passives {
			SpawnOnBattleStart {
				object CharmedPinky
				number 1
			}
		}
```

### Carapace Hat (`CarapaceHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Carapace`
- **Description**: Cleanse 1 stack of a random negative status effect when you end your turn.
- **Mechanics**:
```gon
shield 4
		passives {
			StatusEachTurnEnd {
				PartialCleanse 1
			}
		}
```

### Carapace Mask (`CarapaceMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Carapace`
- **Description**: Cleanse 1 stack of a random negative status effect when you end your turn.
- **Mechanics**:
```gon
shield 4
		passives {
			StatusEachTurnEnd {
				PartialCleanse 1
			}
		}
```

### Carapace Necklace (`CarapaceNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Carapace`
- **Description**: Cleanse 1 stack of a random negative status effect when you end your turn.
- **Mechanics**:
```gon
shield 4
		passives {
			StatusEachTurnEnd {
				PartialCleanse 1
			}
		}
```

### Radioactive Hat (`RadioactiveHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Radioactive`
- **Description**: Adjacent units get All Stats Down.
- **Mechanics**:
```gon
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
```

### Radioactive Mask (`RadioactiveMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Radioactive`
- **Description**: Adjacent units get All Stats Down.
- **Mechanics**:
```gon
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
```

### Radioactive Necklace (`RadioactiveNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Radioactive`
- **Description**: Adjacent units get All Stats Down.
- **Mechanics**:
```gon
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
```

### Molten Hat (`MoltenHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Molten`
- **Description**: Start with Burn 2. Your basic attack inflicts Burn 1. Inflict Burn 1 on units that contact you.
- **Mechanics**:
```gon
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
```

### Molten Mask (`MoltenMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Molten`
- **Description**: Start with Burn 2. Your basic attack inflicts Burn 1. Inflict Burn 1 on units that contact you.
- **Mechanics**:
```gon
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
```

### Molten Necklace (`MoltenNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Molten`
- **Description**: Start with Burn 2. Your basic attack inflicts Burn 1. Inflict Burn 1 on units that contact you.
- **Mechanics**:
```gon
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
```

### Mother's Hat (`MothersHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Mother`
- **Description**: Spawn a Charmed Tiny Tumor at the start of each battle and whenever you're downed.
- **Mechanics**:
```gon
passives {
			SpawnThingOnDeath CharmedTinyTumor
			SpawnOnBattleStart {
				object CharmedTinyTumor
				number 1
			}
		}
```

### Mother's Mask (`MothersMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Mother`
- **Description**: Spawn a Charmed Tiny Tumor at the start of each battle and whenever you're downed.
- **Mechanics**:
```gon
passives {
			SpawnThingOnDeath CharmedTinyTumor
			SpawnOnBattleStart {
				object CharmedTinyTumor
				number 1
			}
		}
```

### Mother's Necklace (`MothersNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Mother`
- **Description**: Spawn a Charmed Tiny Tumor at the start of each battle and whenever you're downed.
- **Mechanics**:
```gon
passives {
			SpawnThingOnDeath CharmedTinyTumor
			SpawnOnBattleStart {
				object CharmedTinyTumor
				number 1
			}
		}
```

### Nurse Hat (`NurseHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Nurse`
- **Description**: +1 Health Regen. Your heals heal for 1 extra.
- **Mechanics**:
```gon
con 1
		passives {
			HealthRegenUp 1
			BoostHeals 1
		}
```

### Nurse Mask (`NurseMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Nurse`
- **Description**: +1 Health Regen. Your heals heal for 1 extra.
- **Mechanics**:
```gon
con 1
		passives {
			HealthRegenUp 1
			BoostHeals 1
		}
```

### Nurse Necklace (`NurseNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Nurse`
- **Description**: +1 Health Regen. Your heals heal for 1 extra.
- **Mechanics**:
```gon
con 1
		passives {
			HealthRegenUp 1
			BoostHeals 1
		}
```

### Hybrid Hat (`HybridHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Hybrid`
- **Description**: Start with a bonus move and Bleed 1.
- **Mechanics**:
```gon
passives {
			Bleed 1
			MoveQuivered 1
		}
```

### Hybrid Mask (`HybridMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `[Hybrid, Rat]`
- **Description**: Start with a bonus attack and Poison 1.
- **Mechanics**:
```gon
passives {
			Poison 1
			Quivered 1
		}
```

### Hybrid Necklace (`HybridNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Hybrid`
- **Description**: Start with +5 Charge and Bruise 1.
- **Mechanics**:
```gon
passives {
			Bruise 1
			Charge 5
		}
```

### Fatty Hat (`FattyHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Fatty`
- **Description**: Brace 1. Your basic attack has +1 Knockback.
- **Mechanics**:
```gon
passives {
			Brace 1
			AddStatusToBasicAttack {
				Knockback 1
			}
		}
```

### Fatty Mask (`FattyMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Fatty`
- **Description**: Brace 1. Your basic attack has +1 Knockback.
- **Mechanics**:
```gon
passives {
			Brace 1
			AddStatusToBasicAttack {
				Knockback 1
			}
		}
```

### Fatty Necklace (`FattyNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Fatty`
- **Description**: Brace 1. Your basic attack has +1 Knockback.
- **Mechanics**:
```gon
passives {
			Brace 1
			AddStatusToBasicAttack {
				Knockback 1
			}
		}
```

### Medical Hat (`MedicalHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Medical`
- **Description**: All of your stats are increased by 1 for each disorder you have.
- **Mechanics**:
```gon
passives {
            AllStatsUpPerDisorder 1
        }
```

### Medical Mask (`MedicalMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Medical`
- **Description**: All of your stats are increased by 1 for each disorder you have.
- **Mechanics**:
```gon
passives {
            AllStatsUpPerDisorder 1
        }
```

### Medical Necklace (`MedicalNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Medical`
- **Description**: All of your stats are increased by 1 for each disorder you have.
- **Mechanics**:
```gon
passives {
            AllStatsUpPerDisorder 1
        }
```

### Ocular Chip (`OcularChip`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Chip`
- **Description**: Your spells cost -1 mana.
- **Mechanics**:
```gon
int -1
		cha -1
		passives {
			ManaCostReduction 1
		}
```

### Cerebral Chip (`CerebralChip`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Chip`
- **Description**: Your spells cost -1 mana.
- **Mechanics**:
```gon
int -1
		cha -1
		passives {
			ManaCostReduction 1
		}
```

### Spinal Chip (`SpinalChip`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Chip`
- **Description**: Your spells cost -1 mana.
- **Mechanics**:
```gon
int -1
		cha -1
		passives {
			ManaCostReduction 1
		}
```

### Demonic Hat (`DemonicHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Demonic`
- **Description**: +3 Thorns. Trample. You can no longer heal.
- **Mechanics**:
```gon
passives {
			Thorns 3
			Trample 3
            HPGainBlock 1
		}
```

### Demonic Mask (`DemonicMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Demonic`
- **Description**: +3 Bleed Thorns. Trample. Bleed 3.
- **Mechanics**:
```gon
passives {
			Bleed 3
			BleedThorns 3
			Trample 3
		}
```

### Demonic Necklace (`DemonicNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Demonic`
- **Description**: Bruise 1. When you take damage, gain +2 Damage.
- **Mechanics**:
```gon
passives {
			Bruise 1
            StatusOnTookDamage {
                DamageUp 2
            }
        }
```

### Frozen Hat (`FrozenHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Frozen`
- **Description**: Your basic attack inflicts Slow and has a +10% chance to Freeze units. Units that contact you gain Slow and have a 10% chance to become Frozen.
- **Mechanics**:
```gon
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
```

### Frozen Mask (`FrozenMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Frozen`
- **Description**: Your basic attack inflicts Slow and has a +10% chance to Freeze units. Units that contact you gain Slow and have a 10% chance to become Frozen.
- **Mechanics**:
```gon
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
```

### Frozen Necklace (`FrozenNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Frozen`
- **Description**: Your basic attack inflicts Slow and has a +10% chance to Freeze units. Units that contact you gain Slow and have a 10% chance to become Frozen.
- **Mechanics**:
```gon
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
```

### Sabertooth Hat (`SaberToothedHat`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Wooly`
- **Description**: +2 Thorns. Ice immunity.
- **Mechanics**:
```gon
shield 3
		passives {
			Thorns 2
			ElementImmune Ice
			StatusImmunity [Freeze, Slow]
		}
```

### Wooly Beard (`CavemanBeard`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `[Wooly, Caveman]`
- **Description**: Brace 2. Ice immunity.
- **Mechanics**:
```gon
shield 3
		passives {
			Brace 2
			ElementImmune Ice
			StatusImmunity [Freeze, Slow]
		}
```

### Sabertooth Pelt (`SaberToothedPelt`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Wooly`
- **Description**: +2 Health Regen. Ice immunity.
- **Mechanics**:
```gon
shield 3
		passives {
		    HealthRegenUp 2
		    ElementImmune Ice
		    StatusImmunity [Freeze, Slow]
		}
```

### Rune of Jera (`RuneofJera`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Rune`
- **Description**: Your trinket effects are doubled.
- **Mechanics**:
```gon
passives {
			TrinketPassiveMultiplierBonus 1
            TrinketActiveEffectsMultiplierBonus 1
		}
```

### Rune of Hagalaz (`RuneofHagalaz`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Rune`
- **Description**: Your Weapons hit twice.
- **Mechanics**:
```gon
passives {
			DoubleCastWeapons 1
		}
```

### Rune of Perthro (`RuneofPerthro`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Rune *]`
- **Description**: This item counts for all item sets.
- **Mechanics**:
```gon
shield 4
```

### Caveman Wig (`CavemanWig`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Caveman`
- **Description**: Spawn 1-3 Charmed Lice at the start of each battle.
- **Mechanics**:
```gon
int -1
		str 2
		passives {
			SpawnOnBattleStart {
				object CharmedLice
				number [1, 3]
			}
		}
```

### Caveman Eyebrows (`CavemanEyebrows`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Caveman`
- **Description**: Your weapons deal double damage.
- **Mechanics**:
```gon
int -1
		con 2
		passives {
			WeaponDamageMultiplierBonus 1
		}
```

### Caveman Necklace (`CavemanNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Caveman`
- **Description**: +33% crit damage.
- **Mechanics**:
```gon
int -1
		lck 2
		passives {
			AddCritMultiplier 33%
		}
```

### Dino Hat (`DinoHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `[Dino, Bone]`
- **Description**: Allies gain +1 [img:str] at the start of each battle.
- **Mechanics**:
```gon
int -1
		shield 5
		passives {
            StatusAlliesOnBattleStart {
                StrengthUp 1
            }
        }
```

### Dino Mask (`DinoMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `[Dino, Bone]`
- **Description**: Allies gain +1 [img:con] at the start of each battle.
- **Mechanics**:
```gon
int -1
		shield 5
		passives {
            StatusAlliesOnBattleStart {
                ConstitutionUp 1
            }
        }
```

### Dino Necklace (`DinoNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Dino, Bone]`
- **Description**: Allies gain +1 [img:spd] at the start of each battle.
- **Mechanics**:
```gon
int -1
		shield 5
		passives {
            StatusAlliesOnBattleStart {
                SpeedUp 1
            }
        }
```

### Big Rock Hat (`BigRockHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Brace 2.
- **Mechanics**:
```gon
spd -2
		shield 6
		passives {
			Brace 2
		}
```

### Big Rock Mask (`BigRockMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Brace 2.
- **Mechanics**:
```gon
spd -2
		shield 6
		passives {
			Brace 2
		}
```

### Big Rock Necklace (`BigRockNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Brace 2.
- **Mechanics**:
```gon
spd -2
		shield 6
		passives {
			Brace 2
		}
```

### Phoenix Hat (`PhoenixHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `[Phoenix, Feathered]`
- **Description**: +10% Dodge Chance. Each time you end movement, gain +1 [img:spd] and Charge 2.
- **Mechanics**:
```gon
passives {
			ArmorDodgeChance 10%
		    StatusOnEndMove {
				SpeedUp 1
				Charge 2
			}
		}
```

### Phoenix Mask (`PhoenixMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `[Phoenix, Feathered]`
- **Description**: +10% Dodge Chance. Each time you end movement, gain +1 [img:spd] and Charge 2.
- **Mechanics**:
```gon
passives {
			ArmorDodgeChance 10%
		    StatusOnEndMove {
				SpeedUp 1
				Charge 2
			}
		}
```

### Phoenix Necklace (`PhoenixNecklace`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Phoenix, Feathered]`
- **Description**: +10% Dodge Chance. Each time you end movement, gain +1 [img:spd] and Charge 2.
- **Mechanics**:
```gon
passives {
			ArmorDodgeChance 10%
		    StatusOnEndMove {
				SpeedUp 1
				Charge 2
			}
		}
```

### Ancestor's Skull (`AncestorsSkull`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `[Ancestor, Bone]`
- **Description**: - {str_aux_passive_name} - {str_aux_passive_desc}
- **Mechanics**:
```gon
str_aux_initialize random_class_passive
        str_aux_is_copy_passive true
```

### Ancestor's Jaw (`AncestorsJaw`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `[Ancestor, Bone]`
- **Description**: - {str_aux_passive_name} - {str_aux_passive_desc}
- **Mechanics**:
```gon
str_aux_initialize random_class_passive
        str_aux_is_copy_passive true
```

### Ancestor's Bones (`AncestorsBones`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Ancestor, Bone]`
- **Description**: - {str_aux_passive_name} - {str_aux_passive_desc}
- **Mechanics**:
```gon
str_aux_initialize random_class_passive
        str_aux_is_copy_passive true
```

### Copycat Hat (`CopycatHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Copycat`
- **Description**: Copies your trinket's passive effects.
- **Mechanics**:
```gon
passives {
            TrinketPassiveMultiplierBonus 1
        }
```

### Copycat Mask (`CopycatMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Copycat`
- **Description**: Copies your trinket's passive effects.
- **Mechanics**:
```gon
passives {
            TrinketPassiveMultiplierBonus 1
        }
```

### Copycat Scarf (`CopycatScarf`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Copycat`
- **Description**: Copies your trinket's passive effects.
- **Mechanics**:
```gon
passives {
            TrinketPassiveMultiplierBonus 1
        }
```

## Category: `beanies_quest_items.gon`

### Persuasion Device (`PersuasionDevice`)
- **Kind**: `weapon` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. Use to permanently charm a non-boss enemy. It joins your party. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
quest_item true
    quest_reward_item PersuasionDevice_Fixed
    ability wp_PersuasionDevice
    spd -2
```

### PersuasionDevice_Fixed (`PersuasionDevice_Fixed`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use to permanently charm a non-boss enemy. It joins your party. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of PersuasionDevice
    quest_item false
```

### Chaos Device (`ChaosDevice`)
- **Kind**: `head` | **Rarity**: `sidequest` | **Set**: `Experimental`
- **Description**: Side Quest Item. When any cat levels up they are offered abilities from all classes.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item ChaosDevice_Fixed
    global_tags [all_cats_are_jester]
```

### Chaos Controller (`ChaosDevice_Fixed`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Experimental`
- **Description**: Abilities from all classes are offered when you level up. You can reroll your levelup options thrice.
- **Mechanics**:
```gon
passives {
        LevelUpClassOverride Jester
        AddLevelUpRerolls 3
    }
```

### Magic Mirror (Broken) (`MagicMirror`)
- **Kind**: `face` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. Your team has very bad luck during events. +2 Thorns.
- **Mechanics**:
```gon
quest_item true
    cursed true
    quest_reward_item MagicMirror_Fixed
	passives {
		Thorns 2
	}
    global_tags [fail_all_events]
```

### Magic Mirror (`MagicMirror_Fixed`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `None`
- **Description**: +20% chance to reflect projectiles. Spawn a friendly Spookie when downed.
- **Mechanics**:
```gon
passives {
        ReflectProjectiles 20%
        SpawnOnDowned CharmedSpookie
    }
```

### Me Stone (`MeStone`)
- **Kind**: `trinket` | **Rarity**: `sidequest` | **Set**: `Rock`
- **Description**: Side Quest Item. This cat always levels up, and can level up even if it was downed.
- **Mechanics**:
```gon
quest_item true
    cursed true
    quest_reward_item MeStone_Fixed
    passives {
        CanLevelUpWhenDead 1
        AlwaysChosenForLevelUp 1
    }
```

### Suck Stone (`MeStone_Fixed`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Rock`
- **Description**: At the end of your turn, drain up to 5 mana from each of your allies.
- **Mechanics**:
```gon
passives {
        StatusEachTurnEnd {
            ForceUseAbility tk_SuckStone
        }
    }
```

### Angry Face (`AngryFace`)
- **Kind**: `face` | **Rarity**: `sidequest` | **Set**: `Paper`
- **Description**: Side Quest Item. Equipped cat is an enemy, must be downed to win the battle, and can still receive level ups. Can't be equipped to a Collarless cat.
- **Mechanics**:
```gon
quest_item true
    cursed true
    quest_reward_item AngryFace_Fixed
    cant_equip_to_colorless true
    passives {
        SetFaction enemies
        CanLevelUpWhenDead 1
        SpawnNearEnemies 1
        MoveAndUseAbilityEachTurnBeginIfPossible face_EatNeverstone
        AddEndOfCombatRegen 999999
    }
```

### Happy Face (`AngryFace_Fixed`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Paper`
- **Description**: Spawn near enemies and take an AI controlled bonus turn at the start of every battle.
- **Mechanics**:
```gon
passives {
        SpawnNearEnemies 1
        AlphaTurns 1
        AIControlNextTurn {
            stacks 1
            include_spells true
        }
    }
```

### Fart Face (`FartFace`)
- **Kind**: `face` | **Rarity**: `sidequest` | **Set**: `HumanFlesh`
- **Description**: Side Quest Item. Apply Poison 1 to everything at the start of the battle.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item FartFace_Fixed
    passives {
        AbilityOnBattleStart face_FartFace
    }
```

### Robo Fart Face (`FartFace_Fixed`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Bionic`
- **Description**: Apply Poison 1 to all enemies at the start of the battle.
- **Mechanics**:
```gon
passives {
        AbilityOnBattleStart face_FartFaceFixed
    }
```

### Spider Injector (`SpiderInjector`)
- **Kind**: `head` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. Apply Infested 4 to all allies at the start of each battle.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item SpiderInjector_Fixed
    passives {
        AbilityOnBattleStart head_SpiderInjector
    }
```

### Spider Baby (`SpiderInjector_Fixed`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Apply Infested 1 to all enemies at the start of each battle.
- **Mechanics**:
```gon
passives {
        AbilityOnBattleStart head_SpiderInjectorFixed
    }
```

### Party Detonator (`PartyDetonator`)
- **Kind**: `weapon` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. All units explode when they die. Use: Explode a random other unit, once per battle.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item PartyDetonator_Fixed
    ability wp_PartyDetonator
    passives {
        AllUnitsExplodeOnDeath 5
    }
```

### Party Detonator (Fixed) (`PartyDetonator_Fixed`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Explode a random unit within a target radius. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_PartyDetonatorFixed
```

### Air Horn (`AirHorn`)
- **Kind**: `weapon` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. You are Ambushed every battle. Use to make some noise!
- **Mechanics**:
```gon
quest_item true
    quest_reward_item AirHorn_Fixed
    ability wp_AirHorn
    global_tags [always_ambushed]
```

### Amplified Air Horn (`AirHorn_Fixed`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Apply Madness to a unit within 5 tiles in your line of sight. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_AirHornFixed
```

### The Loner (`TheLoner`)
- **Kind**: `weapon` | **Rarity**: `sidequest` | **Set**: `Cool`
- **Description**: Side Quest Item. Kill all of your allies at the start of each battle.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item TheLoner_Fixed
    ability wp_TheLoner
    passives {
        AbilityOnBattleStart wp_TheLonerAuto
    }
```

### The Loner Mark 2 (`TheLoner_Fixed`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `[Cool, Used]`
- **Description**: Use: Deals 5 damage to anything in your line of sight. RELOAD: Any ally dies.
- **Mechanics**:
```gon
ability wp_TheLonerFixed
```

### Glass Cannon (`GlassCannon`)
- **Kind**: `weapon` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. Fill the map with glass at the start of each battle. Use: Shoot a glass ball.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item GlassCannon_Fixed
    ability wp_GlassCannon
    passives {
        ReplaceBlankTilesOnBattleStart GlassTile
    }
```

### Glass Cannon (Fixed) (`GlassCannon_Fixed`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Shoot a glass ball anywhere.
- **Mechanics**:
```gon
ability wp_GlassCannonFixed
```

### Princess Hat (`PrincessHat`)
- **Kind**: `head` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. Fragile. Equipped cat cannot use any actions except Move.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item PrincessHat_Fixed
    shield 10
    passives {
        Fragile 1
        DisableAbilities all_items
        DisableAbilities all_spells
        DisableAbilities basic_attack
    }
```

### Used Princess Hat (`PrincessHat_Fixed`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Used`
- **Description**: 
- **Mechanics**:
```gon
shield 6
```

### Unidentified Pills (`HardPill`)
- **Kind**: `trinket` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. The adventure is harder!
- **Mechanics**:
```gon
quest_item true
    quest_reward_item HardPill_Fixed
	shield 8
    global_tags [increase_difficulty]
```

### Truck Stop Pills (`HardPill_Fixed`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: +3 Brace. You count as a rock.
- **Mechanics**:
```gon
passives {
        Brace 3
        AddTag rock
    }
```

### Bubble Boy (`BubbleBoy`)
- **Kind**: `neck` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. All units rebound with Knockback 5 on contact.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item BubbleBoy_Fixed
    passives {
        GlobalMeleeRevengeDamage {
            knockback 5
        }
    }
```

### Bubbles (`BubbleBoy_Fixed`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Throw a bubble with Wind and Water Element that inflicts Confusion.
- **Mechanics**:
```gon
ability wp_BubbleBoyFixed
```

### Redacted (`Redacted`)
- **Kind**: `face` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. Health bars and status icons are hidden in battle.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item Redacted_Fixed
    passives {
        HideSomeHudStuff 1
    }
```

### Paper Bag (`Redacted_Fixed`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Your [img:cha] is equal to your highest other stat.
- **Mechanics**:
```gon
passives {
        CharismaIsMaxStat 1
    }
```

### Stopwatch (`Stopwatch`)
- **Kind**: `trinket` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. You have 5 seconds to make decisions in battle, otherwise cats will act randomly.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item Stopwatch_Fixed
    global_passives {
        RealTimePressure 5
    }
```

### Stopwatch (Fixed) (`Stopwatch_Fixed`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: You or a target unit takes an AI controlled bonus turn. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_StopwatchFixed
```

### Storage Locker (`StorageLocker`)
- **Kind**: `neck` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. Your team's active ability level ups offer rare items instead.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item StorageLocker_Fixed
    global_tags [item_levelup_quest]
    passives {
        Metal 1
    }
```

### Armory Key (`StorageLocker_Fixed`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Find an extra item after each battle.
- **Mechanics**:
```gon
passives {
        Metal 1
        FindExtraItemFromPoolOnBattleEnd combat_reward_easy
    }
```

### Mysterious Dice (`MysteriousDice`)
- **Kind**: `trinket` | **Rarity**: `sidequest` | **Set**: `None`
- **Description**: Side Quest Item. Your team's level up options are complete chaos!
- **Mechanics**:
```gon
quest_item true
    quest_reward_item MysteriousDice_Fixed
    global_tags [superchaos_levelups]
```

### The D6 (`MysteriousDice_Fixed`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Permanently upgrade one of your active abilities at random.
- **Mechanics**:
```gon
consumable true
    durability 1
    ability cm_TheD6
```

### Experimental Treatment (`ExperimentalTreatment`)
- **Kind**: `face` | **Rarity**: `sidequest` | **Set**: `Experimental`
- **Description**: Side Quest Item. Your team's passive ability level ups offer disorders instead.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item ExperimentalTreatment_Fixed
    global_tags [disorder_levelup_quest]
```

### Disorder Decoder (`ExperimentalTreatment_Fixed`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Experimental`
- **Description**: Your spells cost 1 less for each disorder you have.
- **Mechanics**:
```gon
passives {
        ReduceSpellCostsPerDisorder 1
    }
```

### Ultra Vision 3000 (`UltraVision3000`)
- **Kind**: `face` | **Rarity**: `sidequest` | **Set**: `Bionic`
- **Description**: Side Quest Item. Events are harder. All normal events trigger 2 extra events.
- **Mechanics**:
```gon
quest_item true
    quest_reward_item UltraVision3000_Fixed
    global_tags [
        increase_event_difficulty
        increase_event_difficulty
        trigger_extra_event
        trigger_extra_event
    ]
```

### Ultra Vision 3000 v1.1 (`UltraVision3000_Fixed`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Bionic`
- **Description**: Your basic attack inflicts Marked.
- **Mechanics**:
```gon
cursed true
    lck 4
    passives {
        AddStatusToBasicAttack {
            Marked 1
        }
    }
```

### Nuclear Knife (`NuclearKnife`)
- **Kind**: `weapon` | **Rarity**: `sidequest` | **Set**: `Radioactive`
- **Description**: Side Quest Item. Use: Melee Attack with damage = charges ({aux}). Permanently gains 1 charge at the end of each turn. If charges go above 10, this weapon explodes. Loses half of its charges when it gets a kill.
- **Mechanics**:
```gon
quest_item true
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
```

### Nuclear Knife (Glowing) (`NuclearKnife_Glowing`)
- **Kind**: `weapon` | **Rarity**: `sidequest` | **Set**: `Radioactive`
- **Description**: Side Quest Item. It's about to explode! Get a kill with this now to quench it.
- **Mechanics**:
```gon
quest_item true
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
```

### Nuclear Gun (`NuclearKnife_Fixed`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Radioactive`
- **Description**: Use: Deals 40 damage to a target and 20 damage to EVERYTHING ELSE. 20% chance to break on use.
- **Mechanics**:
```gon
ability wp_NuclearKnifeFixed
```

## Category: `consumables.gon`

### A Snack (`FoodMedium`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Heal {aux} HP.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_Heal
    aux 12
```

### Cat Food (`FoodBig`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Heal {aux} HP.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_Heal
    aux 24
```

### Rotisserie Chicken (`Chicken`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `None`
- **Description**: Use: Heal {aux} HP.
- **Mechanics**:
```gon
durability 3
    consumable true
    ability cm_Heal
    aux 15
```

### Small Catnip Baggy (`Catnip`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Gain {aux} mana.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_Catnip
    aux 7
```

### Large Catnip Baggy (`CatnipBig`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Gain {aux} mana.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_Catnip
    aux 12
```

### Roid Rage (`RoidRage`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Gain +{aux} [img:str] for the rest of the battle.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_StrBuff
    aux 5
```

### Speedball (`SpeedBall`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Gain +{aux} [img:dex] for the rest of the battle.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_DexBuff
    aux 5
```

### Brain Candy (`BrainCandy`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Gain +{aux} [img:int] for the rest of the battle.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_IntBuff
    aux 5
```

### Disco Biscuit (`DiscoBiscuit`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Gain +{aux} [img:cha] for the rest of the battle and gain 6 mana.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_ChaBuff
    aux 5
```

### Clover (`Clover`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Gain +{aux} [img:lck] for the rest of the battle.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_LckBuff
    aux 5
```

### Upper (`Upper`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Gain +{aux} [img:spd] for the rest of the battle.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_SpdBuff
    aux 5
```

### Percs (`Percs`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Gain +{aux} [img:shield].
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_Shield
    aux 10
```

### Antidote (`Antidote`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `None`
- **Description**: Use: Cleanse all debuffs. This can be used on adjacent units.
- **Mechanics**:
```gon
durability 2
    consumable true
    ability cm_Antidote
```

### Kidney (`Kidney`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Use to heal 10, gain +2 Health Regen, and cleanse debuffs.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_Kidney
```

### Enema (`Enema`)
- **Kind**: `trinket` | **Rarity**: `consumable_uncommon` | **Set**: `None`
- **Description**: Use: Cleanse all buffs and debuffs.
- **Mechanics**:
```gon
durability 5
    consumable true
    ability cm_Enema
```

### Citrus Berry (`SitrusBerry`)
- **Kind**: `trinket` | **Rarity**: `consumable_uncommon` | **Set**: `None`
- **Description**: Use: Heal 25% HP. Automatically eaten if your HP drops below 50%.
- **Mechanics**:
```gon
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
```

### Smelling Salts (`SmellingSalts`)
- **Kind**: `trinket` | **Rarity**: `consumable_uncommon` | **Set**: `None`
- **Description**: Use: Revive an adjacent unit at 1 HP. Automatically used on yourself at the end of the round if you're downed.
- **Mechanics**:
```gon
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
```

### Big Bucket of Lard (`Lard`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `None`
- **Description**: Use: Heal yourself and all adjacent units to full HP.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_Lard
```

### Kilo of Catnip (`KiloOfCatnip`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `None`
- **Description**: Use: Restore all your mana.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_KiloOfCatnip
```

### Bag of Grass (`BagOfGrass`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `None`
- **Description**: Use: Gain {aux} mana.
- **Mechanics**:
```gon
durability 5
    consumable true
    ability cm_Catnip
    aux 10
```

### Viper Bottle (`ViperBottle`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `None`
- **Description**: Use: Take 5 damage and gain +1 to a random stat permanently. May have side effects...
- **Mechanics**:
```gon
durability [2 4]
    consumable true
    ability cm_ViperBottle
```

### Super Bandage (`SuperBandage`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `Nurse`
- **Description**: Use: Cure a random injury.
- **Mechanics**:
```gon
durability 4
    consumable true
    ability cm_SuperBandage
```

### Rotten Meat (`RottenMeat`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `[Rotten, Meat]`
- **Description**: Use: Gain Poison 1, then your basic attack becomes Puke Shot. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
consumable true
    ability cm_RottenMeat
```

### Mushrooms (`Mushrooms`)
- **Kind**: `trinket` | **Rarity**: `consumable_uncommon` | **Set**: `Druid`
- **Description**: Use: Gain All Stats Up 2.
- **Mechanics**:
```gon
durability [2 4]
    consumable true
    ability cm_AllStatsBuff
    aux 2
```

### Star (`Star`)
- **Kind**: `trinket` | **Rarity**: `consumable_very_rare` | **Set**: `None`
- **Description**: Use: Gain Invincibility, +10 Thorns, and Trample until the start of your next turn. Refresh your movement action.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_Star
```

### Bullseye (`Bullseye`)
- **Kind**: `trinket` | **Rarity**: `consumable_uncommon` | **Set**: `Paper`
- **Description**: Use: All damage you deal until the end of the turn is critical and can't miss.
- **Mechanics**:
```gon
durability 4
    consumable true
    ability cm_Bullseye
```

### Stem Cells (`StemCells`)
- **Kind**: `trinket` | **Rarity**: `consumable_uncommon` | **Set**: `None`
- **Description**: Use: Gain +3 Health Regen until the end of the battle.
- **Mechanics**:
```gon
durability 2
    consumable true
    ability cm_StemCells
```

### Eyeball (`Eyeball`)
- **Kind**: `trinket` | **Rarity**: `consumable_common` | **Set**: `Guts`
- **Description**: Use: Heal {aux} HP.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_Heal
    aux 8
```

### Witch's Eye (`WitchsEye`)
- **Kind**: `trinket` | **Rarity**: `consumable_uncommon` | **Set**: `None`
- **Description**: Use: Gain Backflip 2.
- **Mechanics**:
```gon
durability [2 6]
    consumable true
    ability cm_WitchsEye
```

### Forbidden Fruit (`ForbiddenFruit`)
- **Kind**: `trinket` | **Rarity**: `consumable_very_rare` | **Set**: `None`
- **Description**: Use: Heal to full, restore all your mana, and gain All Stats Up 2. There will be permanent consequences for eating this fruit...
- **Mechanics**:
```gon
durability [1 3]
    consumable true
    ability cm_ForbiddenFruit
```

### PCP (`PCP`)
- **Kind**: `trinket` | **Rarity**: `consumable_uncommon` | **Set**: `None`
- **Description**: Use: Gain +5 Damage and Madness 3. This can be used on adjacent units.
- **Mechanics**:
```gon
durability 3
    consumable true
    ability cm_PCP
```

### Wish Bone (`WishBone`)
- **Kind**: `trinket` | **Rarity**: `consumable_very_rare` | **Set**: `Bone`
- **Description**: Use: Gain +99 [img:lck] until the end of the turn.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_WishBone
```

### Metal Coat (`MetalCoat`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Make your weapon unbreakable for the rest of the adventure.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_MetalCoat
```

### Shoe Polish (`ShoePolish`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Fully repair your weapon. Refresh your weapon action.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_ShoePolish
```

### Pearl (`Pearl`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Gain 10-30 coins.
- **Mechanics**:
```gon
durability 1
    consumable true
    lck 2
    ability cm_Pearl
```

### Big Toe (`BigToe`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `HumanFlesh`
- **Description**: Use: Heal 6, gain +1 Health Regen and cleanse your debuffs.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_BigToe
```

### Raptor Egg (`RaptorEgg`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Heal to full. 10% chance at the end of each turn to break and summon a Charmed Raptor Kitten.
- **Mechanics**:
```gon
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
```

### Fighter Seal (`FighterSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Fighter`
- **Description**: Use: Permanently turn into a Fighter.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_FighterSeal
```

### Hunter Seal (`HunterSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Hunter`
- **Description**: Use: Permanently turn into a Hunter.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_HunterSeal
```

### Tank Seal (`TankSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Tank`
- **Description**: Use: Permanently turn into a Tank.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_TankSeal
```

### Cleric Seal (`ClericSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Cleric`
- **Description**: Use: Permanently turn into a Cleric.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_ClericSeal
```

### Thief Seal (`ThiefSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Thief`
- **Description**: Use: Permanently turn into a Thief.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_ThiefSeal
```

### Mage Seal (`MageSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Mage`
- **Description**: Use: Permanently turn into a Mage.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_MageSeal
```

### Void Seal (`ColorlessSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Permanently turn into a Collarless cat.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_ColorlessSeal
```

### Psychic Seal (`PsychicSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Psychic`
- **Description**: Use: Permanently turn into a Psychic.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_PsychicSeal
```

### Jester Seal (`JesterSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Jester`
- **Description**: Use: Permanently turn into a Jester.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_JesterSeal
```

### Tinkerer Seal (`TinkererSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Tinkerer`
- **Description**: Use: Permanently turn into a Tinkerer.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_TinkererSeal
```

### Butcher Seal (`ButcherSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Butcher`
- **Description**: Use: Permanently turn into a Butcher.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_ButcherSeal
```

### Druid Seal (`DruidSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Druid`
- **Description**: Use: Permanently turn into a Druid.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_DruidSeal
```

### Monk Seal (`MonkSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Permanently turn into a Monk.
- **Mechanics**:
```gon
durability 1
    consumable true
	Set Monk
    ability cm_MonkSeal
```

### Necromancer Seal (`NecromancerSeal`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Necromancer`
- **Description**: Use: Permanently turn into a Necromancer.
- **Mechanics**:
```gon
durability 1
    consumable true
    ability cm_NecromancerSeal
```

### Whole Turkey (`Turkey`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `None`
- **Description**: Use: Heal {aux} HP.
- **Mechanics**:
```gon
durability 7
    consumable true
    ability cm_Heal
    aux 15
```

### Dead Hummingbird (`DeadHummingbird`)
- **Kind**: `trinket` | **Rarity**: `consumable_very_rare` | **Set**: `Feathered`
- **Description**: Use: Gain +20 [img:spd] and +50% Dodge Chance.
- **Mechanics**:
```gon
durability 2
    consumable true
    ability cm_EatHummingbird
    aux 20
```

### Unstable DNA (`UnstableDNA`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `None`
- **Description**: Use: Gain 6 random stat ups and 3 random stat downs, then gain 3 Mutations at the end of combat.
- **Mechanics**:
```gon
durability [1 3]
    consumable true
	ability cm_UnstableDNA
```

### Red Pill (`RedPill`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `None`
- **Description**: Use: 50% chance to get Chungus (+4 [img:con]), otherwise take 8 damage.
- **Mechanics**:
```gon
durability 1
    consumable true
	ability cm_RedPill
```

### Forbidden Pill (`ForbiddenPill`)
- **Kind**: `trinket` | **Rarity**: `consumable_very_rare` | **Set**: `None`
- **Description**: Use: Temporarily upgrade all of your active abilities. There will be permanent consequences for taking this pill.
- **Mechanics**:
```gon
durability 1
    consumable true
	ability cm_ForbiddenPill
```

### Missing Nipple (`MissingNipple`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `None`
- **Description**: Use: Give an adjacent unit +1 Health Regen.
- **Mechanics**:
```gon
durability 6
	consumable true
	ability cm_Nipple
```

### Experiment X (`Experimentx`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Experimental`
- **Description**: Use: ???
- **Mechanics**:
```gon
durability 1
	consumable true
    ability cm_ExperimentX
```

### Steven (`StevensConsumable1`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Steven`
- **Description**: Use: Permanently upgrade a random spell or passive ability.
- **Mechanics**:
```gon
durability 1
	consumable true
    ability cm_Steven1
```

### Steven (`StevensConsumable2`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Steven`
- **Description**: Use: Spawn a controllable copy of yourself.
- **Mechanics**:
```gon
durability 1
	consumable true
    ability cm_Steven2
```

### Joker Card (`JokerCard`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `[Jester, Paper]`
- **Description**: Use: Duplicate one of your equipped items.
- **Mechanics**:
```gon
durability 1
	consumable true
    ability cm_JokerCard
```

### Gizzard (`Gizzard`)
- **Kind**: `trinket` | **Rarity**: `consumable_rare` | **Set**: `Guts`
- **Description**: Use: Enter Mockingbird Form. Gain a random bird mutation at the end of the battle.
- **Mechanics**:
```gon
durability 1
	consumable true
    ability cm_Gizzard
```

## Category: `cursed_items.gon`

### Alluring Doodie (`AlluringDoodie`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Fecal`
- **Description**: 10% chance to eat poop and gain Poison 1 each turn.
- **Mechanics**:
```gon
cursed true
    durability 5
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
```

### Child's Skull (`ChildSkull`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Bone`
- **Description**: Your basic attack is a weak tear shot. You can use your basic attack an extra time each turn.
- **Mechanics**:
```gon
cursed true
    attack IsaacBasicAttack
    shield 3
    passives {
        ExtraBasicAttacks 1
        OverrideBasicAttack IsaacBasicAttack
    }
```

### Paw Shards (`PawShards`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Your basic attack inflicts Bleed 1. Gain +1 Bleed each time you use your basic attack.
- **Mechanics**:
```gon
cursed true
    passives {
        AddStatusToBasicAttack {
            Bleed 1
        }
        AddSelfStatusToBasicAttack {
            Bleed 1
        }
    }
```

### Splinters (`Splinters`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
cursed true
    con -1
    str 1
```

### Face Shards (`FaceShards`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: +2 Thorns. Gain +1 Bleed each time you take damage.
- **Mechanics**:
```gon
cursed true
    passives {
        Thorns 2
        StatusOnTookDamage {
            Bleed 1
        }
    }
```

### Bad Splinters (`BadSplinters`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: +2 Thorns.
- **Mechanics**:
```gon
cursed true
    con -2
    passives {
        Thorns 2
    }
```

### Cursed Hairball (`CursedHairball`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Your basic attack inflicts Poison 2. Start each battle with Poison 3.
- **Mechanics**:
```gon
cursed true
    passives {
        Poison 3
        AddStatusToBasicAttack {
            Poison 2
        }
    }
```

### Mark of the Beast (`MarkOfTheBeast`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: +6 Damage. Holy Element heals damage you instead. When downed, your body is destroyed.
- **Mechanics**:
```gon
cursed true
    passives {
        DamageUp 6
        Undead 1
        AddCorpseHealth -999999
    }
```

### Putrid Pile (`PutridPile`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Adjacent units move away from you at the end of their turns. Your basic attack inflicts Poison.
- **Mechanics**:
```gon
cursed true
    cha -1
    passives {
	    AddStatusToBasicAttack {
            Poison 1
		}
        StatusAdjacentOnTheirTurnEnd {
            ForceMoveAway 1
        }
    }
```

### Vibrating Meteorite (`VibratingMeteorite`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: This item loses 1 of each stat at the end of each battle, permanently. [s:.7](This can go negative.)[/s]
- **Mechanics**:
```gon
cursed true
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
```

### Cursed Rock (`CursedRock`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
cursed true
    shield 6
    str -2
```

### Clam (`Clam`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: 5% chance to break when you take damage. When this breaks, find a Pearl.
- **Mechanics**:
```gon
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
```

### Bird Poop (`BirdPoopHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Fecal //Bird`
- **Description**: +50% chance for an extra bird to spawn at the start of each battle.
- **Mechanics**:
```gon
cursed true
    cha -1
    passives {
        SpawnOnBattleStartRandomEmptyTile {
            object Bird
            number [0 1]
        }
    }
```

### Callus (`Callus`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Permanently gain +2 [img:shield] each time you end a battle with 1 or more [img:shield].
- **Mechanics**:
```gon
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
```

### Slag Tight (`SlagTight`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Brace 1. Your basic attack inflicts Bruise 1.
- **Mechanics**:
```gon
cursed true
    int -4
    shield 5
    passives {
        Brace 1
        AddStatusToBasicAttack {
            Bruise 1
        }
    }
```

### Metal Rod (`MetalRod`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack with Knockback 1 and a 10% chance to inflict Stun.
- **Mechanics**:
```gon
cursed true
    int -1
    con -1
    ability wp_MetalRod
```

### Big Toe (`BigToeCursed`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: After your 3rd turn, spawn a Charmed Spookie with Madness on a random tile.
- **Mechanics**:
```gon
cursed true
    passives {
        StatusAfterXTurns {
            stacks 3
            ForceUseAbility tk_MadGhost_Spawn
        }
    }
```

### Golden Idol (`GoldenIdol`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Becomes {aux} coins when you return home.
- **Mechanics**:
```gon
cursed true
	on_store become_aux_coins
    aux 500
    lck -2
```

## Category: `enemy_items.gon`

### MageCollar (`MageCollar`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
	int 2
```

### MetalPlate (`MetalPlate`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
	con 2
    passives {
        Metal 1
    }
```

### HuntersPatch (`HuntersPatch`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
	dex 2
```

### AngelicAura (`AngelicAura`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
	int 1
	con 1
```

### CoinBag (`CoinBag`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
	speed 1
```

### SamsonsChains (`SamsonsChains`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
	str 2
    passive {
        Metal 1
    }
```

### Banana (`Banana`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
	cha -1
```

### Slime (`Slime`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
	cha -1
```

### Gunslinger Pistol (`GunslingerPistol`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
desc ""
    durability 6
    ability wp_GunslingerPistol
```

### WesternHat (`WesternHat`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### Poncho (`Poncho`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### AtomicMark (`AtomicMark`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
    int 2
```

### Astro Zapper (`AstroTaser`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
desc ""
    ability wp_AstroTaser
```

### Odd Remote (`OddRemote_Enemy`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Cast a random spell.
- **Mechanics**:
```gon
ability wp_OddRemoteEnemy
```

### Pebble (`Pebble`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
    shield 2
```

### Dreadlocks (`Dreadlocks`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### BabyHair (`BabyHair`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### BulbHead (`BulbHead`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### MuggerMask (`MuggerMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### NecromancerMask (`NecromancerMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### TinkererHat (`TinkererHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### ButcherMask (`ButcherMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### PsychicMask (`PsychicMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### JesterHat (`JesterHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### MonkMask (`MonkMask`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### DruidNeck (`DruidNeck`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### Shotgun (`TerminatorShotgun`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
desc ""
    ability wp_TerminatorShotgun
```

### Sniper Rifle (`TerminatorSniper`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
desc ""
    ability wp_TerminatorSniper
```

### Submachine Gun (`TerminatorUzi`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
desc ""
    ability wp_TerminatorUzi
```

### Cool Glasses (`TerminatorCoolGlasses`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
desc ""
```

### TerminatorCoolGlasses2 (`TerminatorCoolGlasses2`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
    desc ""
```

### Club (`CaveCatClub`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
desc ""
    ability wp_CaveCatClub
```

### SuperDunceCap (`SuperDunceCap`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
    int -10
```

### MageCollar_Terminator (`MageCollar_Terminator`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
	int 2
```

### MetalPlate_Terminator (`MetalPlate_Terminator`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
	con 2
    passives {
        Metal 1
    }
```

### HuntersPatch_Terminator (`HuntersPatch_Terminator`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
	dex 2
```

### AngelicAura_Terminator (`AngelicAura_Terminator`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
	int 1
	con 1
```

### CoinBag_Terminator (`CoinBag_Terminator`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
	speed 1
```

### SamsonsChains_Terminator (`SamsonsChains_Terminator`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
	str 2
    passive {
        Metal 1
    }
```

### NecromancerMask_Terminator (`NecromancerMask_Terminator`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
```

### TinkererHat_Terminator (`TinkererHat_Terminator`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
```

### ButcherMask_Terminator (`ButcherMask_Terminator`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
```

### PsychicMask_Terminator (`PsychicMask_Terminator`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
```

### JesterHat_Terminator (`JesterHat_Terminator`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
```

### MonkMask_Terminator (`MonkMask_Terminator`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
```

### DruidNeck_Terminator (`DruidNeck_Terminator`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
```

### Pebble_Terminator (`Pebble_Terminator`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
    shield 2
```

### LoansharksFedora (`LoansharksFedora`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
    passives {
		CritChanceUp 100
    }
```

### Rabiesface (`Rabiesface`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
name ""
	desc ""
	passives {
	}
```

## Category: `face_items.gon`

### Mustache (`Mustache`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Man`
- **Description**: 
- **Mechanics**:
```gon
cha 1
```

### Glasses (`Glasses`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
int 2
    con -1
```

### Muzzle (`Muzzle`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Gimp`
- **Description**: 
- **Mechanics**:
```gon
str -2
    cha 1
    int 1
    shield 2
```

### Face Covering (`FaceCovering`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `[Medical, Nurse]`
- **Description**: 
- **Mechanics**:
```gon
con 1
    passives {
        CantCatchDiseases 1
        CantSpreadDiseases 1
    }
```

### Bozo (`Bozo`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Jester`
- **Description**: Your basic attack has a +15% chance to inflict Fear.
- **Mechanics**:
```gon
int -1
    cha 2
    passives {
        AddStatusToBasicAttack {
            Fear [1 .15]
        }
    }
```

### Bandage (`Bandage`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Nurse`
- **Description**: +2 Health Regen.
- **Mechanics**:
```gon
con -1
    passives {
        HealthRegenUp 2
    }
```

### Mystical Blindfold (`MysticalBlindfold`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Rag`
- **Description**: Your physical attacks and abilities always miss.
- **Mechanics**:
```gon
int 4
    cha 2
    passives {
        PhysicalAttacksMiss 1
    }
```

### Third Eye (`ThirdEye`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `[Psychic, Hybrid]`
- **Description**: +1 range. Your ranged attacks can't miss.
- **Mechanics**:
```gon
passives {
        RangedTrueShot 1
        AddBonusRange 1
    }
```

### Flower (`Flower`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Flower`
- **Description**: Spawn flowers under you when you end your turn. +1 Health Regen.
- **Mechanics**:
```gon
passives {
        FlowersOnEndTurn 1
		HealthRegenUp 1
    }
```

### Hockey Mask (`HockeyMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: While downed, you have a 25% chance to revive with 1 HP at the end of the round.
- **Mechanics**:
```gon
shield 5
    passives {
        ChanceToRevive 25
    }
```

### Bandit Mask (`BanditMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Thief`
- **Description**: Your basic attack spawns 1 coin when it deals damage.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            KnockOutCoin 1
        }
    }
```

### Infamous Mask (`InfamousMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Lead`
- **Description**: Block attacks from the front.
- **Mechanics**:
```gon
spd -2
    passives {
        FaceShield 1
    }
```

### Bear Trap Mask (`BearTrapMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Lead`
- **Description**: +1 Bleed Thorns.
- **Mechanics**:
```gon
shield 4
    passives {
        Metal 1
        BleedThorns 1
    }
```

### Pins and Needles (`PinsAndNeedles`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Gimp`
- **Description**: +1 Thorns. Gain +1 Charge when you take damage.
- **Mechanics**:
```gon
passives {
        Metal 1
        Thorns 1
        StatusOnTookDamage {
            Charge 1
        }
    }
```

### Ninja Bandana (`NinjaBandana`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Ninja`
- **Description**: You have a 10% chance to gain a bonus attack when you use your basic attack.
- **Mechanics**:
```gon
passives {
        AddSelfStatusToBasicAttack {
            Quivered [1 .10]
        }
    }
```

### Monocle (`Monocle`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Your physical attacks can't miss.
- **Mechanics**:
```gon
cha 1
    passives {
        TrueShot 1
    }
```

### Phantom Mask (`PhantomMask`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: +10% chance to Block attacks. When you take damage, this becomes an invincible familiar.
- **Mechanics**:
```gon
shield 3
    passives {
        ChanceToBlock 10%
        DropAsFamiliarOnTookDamage PhantomMaskRock
    }
```

### White Belt (`WhiteBelt`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `None`
- **Description**: +1 Brace.
- **Mechanics**:
```gon
passives {
        Brace 1
    }
```

### Brown Belt (`BrownBelt`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: +1 Damage. If you end your turn with unused basic attacks, gain that many Backflips.
- **Mechanics**:
```gon
passives {
        DamageUp 1
        StatusIfUnusedActPoints {
            BackflipWhenTargeted X
        }
    }
```

### Black Belt (`BlackBelt`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `None`
- **Description**: 25% chance to block attacks and counter attack.
- **Mechanics**:
```gon
passives {
        ChanceToBlockAndCounter 25%
    }
```

### Eye of Ra (`EyeOfRa`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Your basic attack inflicts Burn 1 and Blind 1. Inflict Burn 1 and Blind 1 on units that contact or attack you.
- **Mechanics**:
```gon
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
```

### Bandages (`Bandages`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Nurse`
- **Description**: Heals heal you for twice as much.
- **Mechanics**:
```gon
passives {
        MultiplyReceivedHealing 2
    }
```

### Horse Blinders (`HorseBlinders`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `[Leather, Gimp]`
- **Description**: Your abilities have 100% accuracy and +50% Crit Chance. You are unable to hit any unit that isn't in a straight line directly in front of you.
- **Mechanics**:
```gon
passives {
        TunnelVision {
            crit_chance 50%
        }
    }
```

### Survivalist's Mask (`SurvivalistMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Survivalist`
- **Description**: Bodies you destroy spawn food, catnip and a coin.
- **Mechanics**:
```gon
passives {
        SpawnObjectOnPopCorpse Food
        SpawnObjectOnPopCorpse Coin
        SpawnObjectOnPopCorpse Catnip
    }
```

### Leech Brood (`LeechBrood`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Leech`
- **Description**: Inflict Leech 1 to all enemies at the start of each battle. Start each battle at 50% health.
- **Mechanics**:
```gon
passives {
        AbilityOnBattleStart face_LeechBrood
        StatusOnBattleStart {
            SetHealth 50%
        }
    }
```

### Glyph of Protection (`GlyphOfProtection`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Cleric`
- **Description**: Gain +1 [img:shield] each time you cast a spell.
- **Mechanics**:
```gon
passives {
        StatusOnCastSpell {
            Shield 1
        }
    }
```

### Feathered Mask (`FeatheredMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Feathered`
- **Description**: +10% Dodge Chance.
- **Mechanics**:
```gon
passives {
        ArmorDodgeChance 10%
    }
```

### Debris (`Debris`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `[Debris, Scrap]`
- **Description**: +1 Brace.
- **Mechanics**:
```gon
passives {
        Metal 1
        Brace 1
    }
```

### Mud Mask (`MudMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `DirtClod`
- **Description**: Fragile and Brittle while wet.
- **Mechanics**:
```gon
shield 3
    passives {
        FragileDuringElement water
        BrittleDuringElement water
    }
```

### Vision Plugin (`VisionPlugin`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `[Cyborg, Bionic, Chip]`
- **Description**: +1 range.
- **Mechanics**:
```gon
passives {
        Metal 1
        AddBonusRange 1
    }
```

### Rubber Band (`RubberBand`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Rubber`
- **Description**: +1 reach.
- **Mechanics**:
```gon
passives {
        AddBonusMeleeRange 1
    }
```

### Muertos Mask (`MuertosMask`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Necromancer`
- **Description**: +6 Corpse Health.
- **Mechanics**:
```gon
shield 2
    passives {
        AddCorpseHealth 6
    }
```

### Rhinestone Stickers (`RhinestoneStickers`)
- **Kind**: `face` | **Rarity**: `common` | **Set**: `Gemstone`
- **Description**: Emit 4 Sparkles at the start of each battle.
- **Mechanics**:
```gon
passives {
		StatusOnBattleStart {
			RandomMagicMissile 4
		}
	}
```

### Blessed Ashes (`BlessedAshes`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Cleric`
- **Description**: Gain +3 [img:shield] once per battle when your HP is 3 or less.
- **Mechanics**:
```gon
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
```

### Attractive Hair Clip (`AttractiveHairClip`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `Used`
- **Description**: After you're downed, the next time an allied cat takes a turn, they take an extra turn.
- **Mechanics**:
```gon
passives {
        StatusOnDie {
            CreateGlobalModifiers {
                NextPlayerCatTakesExtraTurn 1
            }
        }
    }
```

### Champion's Mask (`ChampionsMask`)
- **Kind**: `face` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Gain +1 [img:{str_aux}] until the end of the battle each time you kill a unit.
- **Mechanics**:
```gon
shield 3
    str_aux_initialize random_stat
    passives {
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
```

### Barbed Scrap (`BarbedScrap`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `[Barbed, Scrap]`
- **Description**: +1 Thorns, +1 Damage.
- **Mechanics**:
```gon
shield 4
	passives {
		Thorns 1
		DamageUp 1
		Metal 1
    }
```

### Leather Hide Mask (`LeatherHideMask`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `[CatHide, Leather]`
- **Description**: +1 Brace, +1 Health Regen, 5% chance to spawn a Charmed Flea each turn.
- **Mechanics**:
```gon
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
```

### Recycled Ball Gag (`RecycledGimpMask`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `[Gimp, Recycled]`
- **Description**: Gain +2 Charge when you take damage. Find a common item when you are downed.
- **Mechanics**:
```gon
shield 2
	passives {
	    StatusOnDie {
            FindItemFromPool chapter_common
        }
		StatusOnTookDamage {
			Charge 2
		}
	}
```

### Gemstone Bones (`GemstoneBones`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `[Bone, Gemstone]`
- **Description**: +1 Kinetic Spikes. When you take damage, gain +1 [img:str]. When you are downed, emit 6 Sparkles.
- **Mechanics**:
```gon
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
```

### Cool Rocks (`CoolRocks`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `[Cool, Rock]`
- **Description**: Your basic attack has +1 Knockback. When you are downed, gain coins.
- **Mechanics**:
```gon
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
```

### Miner Implant (`MinerImplant`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `[Miner, Cyborg]`
- **Description**: +1 range, +1 reach. Poison Immunity.
- **Mechanics**:
```gon
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
```

### Holy Tears (`HolyTears`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Cleric`
- **Description**: Allies gain 2 [img:divineshield] when you are downed. Your spells cost -1 mana.
- **Mechanics**:
```gon
divine_shield 2
	passives {
		ManaCostReduction 1
		StatusAlliesOnDeath {
			DivineShield 2
		}
	}
```

### Eye Of God (`EyeOfGod`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Hybrid`
- **Description**: +10 range.  Your ranged attacks can't miss.
- **Mechanics**:
```gon
divine_shield 1
    passives {
        RangedTrueShot 1
        AddBonusRange 10
    }
```

### Peace Symbol Face Paint (`PeaceSymbolFacePaint`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Hippie`
- **Description**: Damage you deal to allies is reduced to 0.
- **Mechanics**:
```gon
passives {
		AllyDamageReduction 0
	}
```

### Hitler's Mustache (`HitlersMustache`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `[Man, Used]`
- **Description**: Permanent Madness. Take 2 extra turns at the start of each round.
- **Mechanics**:
```gon
passives {
		PermanentMadness 1
		AlphaTurns -1
		AlphaTurns -1
	}
```

### Rad Glasses (`RadGlasses`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Cool`
- **Description**: Your explosions deal +1 damage and have +1 area.
- **Mechanics**:
```gon
cha 2
	passives {
		IncreaseExplosionSize 1
		IncreaseExplosionDamage 1
	}
```

### Flesh Kid (`FleshKid`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `[Meat, HumanFlesh]`
- **Description**: You can't get injuries. When you're downed, revive at the end of the round. Your movement action is Jump.
- **Mechanics**:
```gon
spd 4
	passives {
		InjuryImmunity 1
		ChanceToRevive 100
		ReplaceBasicMove BasicJump
	}
```

### Lil' Tumor (`LilTumor`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Mother`
- **Description**: At the end of each battle, gain -1 to three random stats, then gain a mutation.
- **Mechanics**:
```gon
passives {
        StatusOnBattleEnd {
            even_if_dead true
            RandomPermanentStat -3
            RandomMutation 1
        }
    }
```

### Conjoined Ameoba (`ConjoinedAmeoba`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Amoeba`
- **Description**: Brace 2. +2 Health Regen. Units that contact you are knocked back 2 tiles. 20% chance to spawn a Charmed Ameoba at the end of the turn.
- **Mechanics**:
```gon
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
```

### Miner's Beard (`MinersBeard`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `[Miner, Man]`
- **Description**: When you take damage, spawn scrap. When you end turn, spawn a coin on a random tile.
- **Mechanics**:
```gon
passives {
        SpawnThingOnDamage {
			object Scrap
		}
		StatusEachTurnEnd {
			SpawnCoinAnywhere 1
		}
    }
```

### Ethereal Eyes (`EtherealEyes`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `None`
- **Description**: +15% Dodge Chance. Gain +5% Dodge Chance each time you take damage.
- **Mechanics**:
```gon
passives {
		DodgeChance_Status 15
		StatusOnTookDamage {
            DodgeChance_Status 5
        }
	}
```

### Doodie Mask (`DoodieMask`)
- **Kind**: `face` | **Rarity**: `rare` | **Set**: `Fecal`
- **Description**: Spawn a Charmed Fly at the end of your turn.
- **Mechanics**:
```gon
cha -2
	passives {
		SpawnEachTurn {
			object CharmedFly
        }
	}
```

### Tina's Best Friend (`TinasFriend`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Fly`
- **Description**: Spawn a large Charmed Fly at the start of each battle.
- **Mechanics**:
```gon
passives {
        SpawnOnBattleStart {
            object CharmedTinaFly
            number 1
        }
    }
```

### Steven's Fart Face (`StevensFartFace`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: At the end of your turn, inflict Poison 1 on all units. Repeat for each turn you've taken this battle.
- **Mechanics**:
```gon
passives {
		StatusEachTurnEndForEachTurn {
			ForceUseAbility face_FartFace
		}
	}
```

### Steven's Mustache (`StevensMustache`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: 
- **Mechanics**:
```gon
cha 5
	lck -2
```

### Steven (`StevenMask1`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Your musical abilities are always double cast.
- **Mechanics**:
```gon
passives {
        DoubleCastTaggedSpells musical
	}
```

### Steven (`StevenMask2`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: While you're downed, spawn a random charmed enemy familiar at the end of each round.
- **Mechanics**:
```gon
passives {
        PassiveWhenDead {
            AutocastEachRound {
                ability face_StevenMask2
                even_if_stunned true
            }
        }
	}
```

### Intruder (`Intruder`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Is it your baby?
- **Mechanics**:
```gon
parasite true
	passives {
		SpawnThingOnDeath TheIntruder
	}
```

### Child of the Glowing One (`ChildOfTheGlowingOne2`)
- **Kind**: `face` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Gain +1 Damage and heal 1 HP every time you use your basic attack.
- **Mechanics**:
```gon
passives {
		StatusOnUseBasicAttack {
			DamageUp 1
			HealthGain 1
		}
	}
```

## Category: `head_items.gon`

### Antenna (`Antenna`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Units that contact or attack you get hit with a lightning bolt that has a 10% chance to Stun.
- **Mechanics**:
```gon
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
```

### Horns (`Horns`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: +1 Thorns.
- **Mechanics**:
```gon
str 1
    passives {
        Thorns 1
    }
```

### Happy Helmet (`HappyHelmet`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `[Bionic, Cyborg]`
- **Description**: Fragile. Gain Psychosis when this breaks.
- **Mechanics**:
```gon
shield 10
    passives {
        SetDefaultFacePassive euphoric
        Fragile 1
        StatusOnBreak {
            GainDisorder Psychosis
        }
    }
```

### Head Spring (`HeadSpring`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Scrap`
- **Description**: Units that contact you are knocked back 10 tiles.
- **Mechanics**:
```gon
passives {
        MeleeRevengeDamage {
            knockback 10
        }
        Metal 1
    }
```

### Wig (`Wig`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Used`
- **Description**: 
- **Mechanics**:
```gon
cha 2
```

### Head Cheese (`HeadCheese`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: +2 Health Regen.
- **Mechanics**:
```gon
passives {
        HealthRegenUp 2
    }
```

### Dunce Cap (`DunceCap`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Paper`
- **Description**: Your spells cost -1 mana.
- **Mechanics**:
```gon
int -2
    passives {
        ManaCostReduction 1
    }
```

### Crown of Feculence (`PoopHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Fecal`
- **Description**: Poops you spawn are alive!
- **Mechanics**:
```gon
passives {
        ReplaceSpawnedObjects [Poop RandomLivingPoop]
        ReplaceSpawnedObjects [FlamingPoop RandomLivingPoop]
    }
```

### Magneto (`Magneto`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `None`
- **Description**: When you end your movement, pull all adjacent pickups towards you. When you gain coins, gain that much [img:shield].
- **Mechanics**:
```gon
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
```

### Black Candle (`BlackCandle`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Demonic`
- **Description**: You can remove cursed items equipped on you, except this one.
- **Mechanics**:
```gon
cursed true
    force_sticky true
    shield 1
    passives {
        CanRemoveCursedItems 1
        ExcludeFromEvents Tragedy
    }
```

### Survivalist Hat (`CamoHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Survivalist`
- **Description**: +25% chance to ambush when entering battle. 10% chance to gain Stealth 1 at the end of each turn.
- **Mechanics**:
```gon
passives {
        ChanceToAmbush 25%
        StatusEachTurnEnd {
            Stealth [1 .1]
        }
    }
```

### Jester Cap (`JesterCap`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Jester`
- **Description**: You can reroll your options twice when you level up. Abilities from all classes are offered after rerolling.
- **Mechanics**:
```gon
cha 1
    passives {
        AddLevelUpRerolls 2
        JesterLevelUpRerolls 1
    }
```

### Halo (`Halo`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Cleric`
- **Description**: +33% chance to gain +1 [img:divineshield] when you take damage.
- **Mechanics**:
```gon
divine_shield 1
    passives {
        StatusOnTakeHealthOrShieldDamage {
            DivineShield [1 .33]
        }
    }
```

### Propeller Cap (`PropellerCap`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Flying.
- **Mechanics**:
```gon
shield 2
    passives {
        Flying 1
    }
```

### Brain In A Jar (`BrainInAJar`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Guts`
- **Description**: The first spell you cast each turn is free.
- **Mechanics**:
```gon
cursed true
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
```

### Mangy Wig (`MangyWig`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Used`
- **Description**: Spawn a Spiderling for every 4 [img:lck] you have at the start of each battle.
- **Mechanics**:
```gon
passives {
        StatusOnBattleStart {
            ObjectOnHitCharacter {
                stacks "floor(lck/4)"
                object CharmedTinySpider
            }
        }
    }
```

### Nisshōki Bandana (`RisingSunBandana`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `None`
- **Description**: While at 5 or less health, you have +3 Damage and can move an extra time each turn.
- **Mechanics**:
```gon
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
```

### Jewel of Drog (`JewelOfDrog`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Gemstone`
- **Description**: The first time you reach full mana each battle, gain +1 Magic Damage and reduce the cost of your spells by 1.
- **Mechanics**:
```gon
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
```

### Leaky Brain (`LeakyBrain`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Guts`
- **Description**: When you spend mana, adjacent allies gain that amount of mana.
- **Mechanics**:
```gon
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
```

### Frying Pan (`FryingPan`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Lead`
- **Description**: Block and counter Backstabs.
- **Mechanics**:
```gon
passives {
        Metal 1
        ChanceToBlockAndCounter {
            chance 100%
            backstab_only true
        }
    }
```

### Crown of Horns (`CrownOfHorns`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `[Demonic, Barbed]`
- **Description**: +4 Thorns. When you take damage while you have Thorns, lose 1 Thorns, then shoot needles that deal 2 damage in eight directions.
- **Mechanics**:
```gon
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
```

### The Relic (`TheRelic`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Cleric`
- **Description**: When you lose [img:divineshield], emit a Sparkle for every point of damage blocked.
- **Mechanics**:
```gon
divine_shield 1
    passives {
        ScaledStatusOnHolyShieldBlock {
            RandomMagicMissile 1
        }
    }
```

### Focus Band (`FocusBand`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Your crits knock units back 10 tiles with Chain Knockback.
- **Mechanics**:
```gon
passives {
        AddStatusToAllDamage {
            KnockbackIfCrit {
                knockback 10
                override_chain_knockback 10
            }
        }
    }
```

### Medic Hat (`MedicHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `[Nurse, Medical]`
- **Description**: -1 Damage. Your basic attack heals allies.
- **Mechanics**:
```gon
passives {
        DamageUp -1
        AddStatusToBasicAttack {
            DamageOrHealConditionally 1
        }
    }
```

### King's Crown (`KingsCrown`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Become the Alpha at the start of each battle. The Alpha has All Stats Up. Lose Alpha status when you take damage.
- **Mechanics**:
```gon
passives {
        Metal 1
        AlphaCat 1
        AlphaAllStatsUp 1
        StatusOnTookDamage {
            RemoveStatus AlphaCat
        }
    }
```

### Emo Wig (`EmoWig`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `[Necromancer, Used]`
- **Description**: Adjacent units get All Stats Down 2. When you take damage, all units within 2 tiles heal 1 HP and gain a temporary +1 Damage.
- **Mechanics**:
```gon
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
```

### Toxic Canister (`ToxicCanister`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Radioactive`
- **Description**: Inflict Poison 1 on all units at the start of the battle. Your basic attack inflicts Poison 1. Inflict Poison 1 on units that contact you.
- **Mechanics**:
```gon
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
```

### Broken Mirror (`BrokenMirrorHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Used`
- **Description**: +3 Bleed Thorns. Your basic attack inflicts +1 Bleed and spawns glass.
- **Mechanics**:
```gon
shield 4
    lck -7
    passives {
        BleedThorns 3
        AddStatusToBasicAttack {
            ChangeTile GlassTile
            Bleed 1
        }
    }
```

### Top Hat (`TopHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Cool`
- **Description**: Start with a bomb if you have no weapon equipped. Your explosions have +1 area.
- **Mechanics**:
```gon
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
```

### Helmet (`Helmet`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
shield 4
    passives {
        Metal 1
        PreventSpecificInjury int
    }
```

### Confusing Hat (`ConfusingHat`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Apply Confusion 2 to yourself and all enemies at the start of each battle.
- **Mechanics**:
```gon
passives {
        Confusion 2
        StatusRandomEnemiesOnBattleStart {
            count 99
            Confusion 2
        }
    }
```

### Nightmare Hat (`NightmareHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Leather`
- **Description**: After you kill 3 units, you can attack an extra time each turn.
- **Mechanics**:
```gon
passives {
        PassiveAfterXKills {
            stacks 3
            passives {
                ExtraBasicAttacks 1
            }
        }
    }
```

### Crown of Pestilence (`CrownOfPestilence`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Necromancer`
- **Description**: Your basic attack becomes Pestilence.
- **Mechanics**:
```gon
passives {
        ReplaceBasicAttack head_Pestilence
    }
```

### Rain Hat (`RainHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: You have All Stats Up while wet.
- **Mechanics**:
```gon
passives {
        PassiveWhenAffectedByElement {
            element water
            passives {
                AllStatsUp 1
            }
        }
    }
```

### Splintered Crown (`SplinteredCrown`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Wood`
- **Description**: Gain +1 Thorns when you take damage.
- **Mechanics**:
```gon
passives {
        StatusOnTookDamage {
            Thorns 1
        }
    }
```

### Medieval Helmet (`MedievalHelmet`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Fighter`
- **Description**: +2 Brace.
- **Mechanics**:
```gon
passives {
        Metal 1
        Brace 2
    }
```

### Conjoined Eye (`ConjoinedEye`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Hybrid`
- **Description**: +10% Dodge Chance.
- **Mechanics**:
```gon
passives {
        ArmorDodgeChance 10%
    }
```

### Stone Helmet (`StoneHelmet`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Rock`
- **Description**: +1 Brace.
- **Mechanics**:
```gon
passives {
        Brace 1
    }
```

### Oak Helmet (`OakHelmet`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Wood`
- **Description**: Flammable.
- **Mechanics**:
```gon
shield 3
    passives {
        Flammable 1
    }
```

### Rusting Helmet (`RustingHelmet`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `Used`
- **Description**: Gain +1 [img:shield] at the end of each turn.
- **Mechanics**:
```gon
shield 1
    passives {
        Metal 1
        StatusEachTurnEnd {
			Shield 1
		}
    }
```

### Training Band (`TrainingBand`)
- **Kind**: `head` | **Rarity**: `common` | **Set**: `None`
- **Description**: +20% Crit Chance.
- **Mechanics**:
```gon
passives {
		CritChanceUp 20
    }
```

### Skull Clamp (`SkullClamp`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Brace 2  +25% chance to inflict Stun on units that contact you.
- **Mechanics**:
```gon
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
```

### Brain Chip (`BrainChip`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Chip`
- **Description**: Become AI controlled.
- **Mechanics**:
```gon
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
```

### Spare Parts (`SpareParts`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `[Tinkerer, Scrap]`
- **Description**: When you move, spawn a scrap pickup where you moved from.
- **Mechanics**:
```gon
passives {
        Metal 1
        LeaveBehindOnceEachMove Scrap
    }
```

### Snakeskin Hat (`SnakeskinHat`)
- **Kind**: `head` | **Rarity**: `uncommon` | **Set**: `Leather`
- **Description**: Spawn a Charmed Rattlesnek at the start of each battle.
- **Mechanics**:
```gon
passives {
        SpawnOnBattleStart {
            object CharmedRattleSnake
        }
    }
```

### Death Shroud (`DeathShroud`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Rag`
- **Description**: When you're downed, permanently gain +1 to a random stat.
- **Mechanics**:
```gon
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
```

### Blessed Halo (`BlessedHalo`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: 50% chance to gain +1 [img:divineshield] when you take damage.
- **Mechanics**:
```gon
divine_shield 3
    passives {
        StatusOnTakeHealthOrShieldDamage {
            DivineShield [1 .5]
        }
    }
```

### Crown Of Thorns (`CrownOfThorns`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Cleric`
- **Description**: +1 Thorns. Gain +1 Thorns whenever you take damage.
- **Mechanics**:
```gon
divine_shield 2
	passives {
		Thorns 1
		StatusOnTookDamage {
			Thorns 1
		}
    }
```

### Rotten Guts (`RottenGuts`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `[Guts, Rotten]`
- **Description**: +2 Health Regen. Spawn a Charmed Maggot or Fly when you end your turn.
- **Mechanics**:
```gon
con 2
	cha -1
	passives {
		HealthRegenUp 2
		SpawnEachTurn {
			chance 100%
			object [CharmedFly CharmedMaggot]
		}
	}
```

### Paper Rags (`PaperRags`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `[Paper, Rag]`
- **Description**: +20% Dodge Chance. +1 Bleed Thorns. Your basic attack inflicts Bleed.
- **Mechanics**:
```gon
passives {
		ArmorDodgeChance 20%
		BleedThorns 1
		AddStatusToBasicAttack {
			Bleed 1
		}
	}
```

### Tie Dye Bandana (`TieDyeBandana`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Hippie`
- **Description**: Spawn a Catnip pickup when you take damage.
- **Mechanics**:
```gon
passives {
		SpawnThingOnDamage {
			object Catnip
			good false //good relative to the thing attacking, for luck calculations
		}
	}
```

### Bunga's Crown (`BungasCrown`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Your weapons always crit. Equip a Bone Club weapon when you kill a unit.
- **Mechanics**:
```gon
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
```

### Asteroid (`Asteroid`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Planet`
- **Description**: 20% chance to call down a Meteor on a random enemy when you take damage.
- **Mechanics**:
```gon
shield 4
	passives {
		StatusOnTakeHealthOrShieldDamage{
			Conditional_GoodRoll {
                odds 20%
                ForceUseAbility tk_Asteroid
			}
        }
	}
```

### Alien Stalk (`AlienStalk`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `[Space, Amoeba]`
- **Description**: Cast a random spell each time you take damage.
- **Mechanics**:
```gon
passives {
		StatusOnTakeHealthOrShieldDamage {
			Metronome 1
		}
	}
```

### Friendly Amoeba (`FriendlyAmoeba`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Amoeba`
- **Description**: Brace 1, +2 Health Regen, Shield 3. Units that contact you get knocked back 1.
- **Mechanics**:
```gon
int -1
	shield 3
    passives {
        Brace 1
		HealthRegenUp 2
		MeleeRevengeDamage {
            knockback 1
        }
    }
```

### Spider Baby (`SpiderBaby`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Necromancer`
- **Description**: Spawn a Spiderling when you take damage.
- **Mechanics**:
```gon
passives {
        SpawnThingOnDamage {
            object CharmedTinySpider
        }
	}
```

### Boris' Brain (`BorisBrain`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Guts`
- **Description**: Trample. When you take damage, move 1 tile towards what damaged you.
- **Mechanics**:
```gon
passives {
		Trample 3
		MoveTowardsDamageSource MoveOne
	}
```

### Johnny's Undies (`JohnnysUndies`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Used`
- **Description**: Spawn a Charmed Cultist at the start of each battle.
- **Mechanics**:
```gon
passives {
		SpawnOnBattleStart CharmedCultist
	}
```

### Queen's Crown (`QueensCrown`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Your basic attack has Knockback and Chain Knockback.
- **Mechanics**:
```gon
shield 4
	passives {
        Metal 1
		AddStatusToBasicAttack {
			Knockback 1
            OverrideChainKnockback 1
		}
	}
```

### Dust Devil's Horn (`DustDevilsHorn`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: +1 Thorns. After you use your basic attack, do a dash attack that leaves a tornado behind.
- **Mechanics**:
```gon
shield 1
	passives {
		Thorns 1
		AddSelfStatusToBasicAttack {
			ForceUseAbility DustDash
        }
	}
```

### Child of the Glowing One (`ChildOfTheGlowingOne`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Gain +1 [img:divineshield] every time you end your movement.
- **Mechanics**:
```gon
passives {
		StatusOnEndMove {
			DivineShield 1
		}
	}
```

### Pale Sabertooth Pelt (`SabertoothTigerPelt`)
- **Kind**: `head` | **Rarity**: `rare` | **Set**: `Wooly`
- **Description**: When you kill a unit, all nearby cats gain +1 Damage.
- **Mechanics**:
```gon
cha 2
	passives {
		StatusOnKillEnemy {
			ForceUseAbility head_CatChestPound
		}
	}
```

### Cow Skull (`CowSkull`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Bone`
- **Description**: +2 Thorns. Your basic attack is Push Attack.
- **Mechanics**:
```gon
attack BasicTankMelee
    shield 3
	str 2
	passives {
		Thorns 2
        OverrideBasicAttack BasicTankMelee
	}
```

### TrashCan (`TrashCan`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Brace 4. Blind.
- **Mechanics**:
```gon
shield 10
	passives {
        Metal 1
		Brace 4
		Blind -1
	}
```

### Throbbing Crown (`ThrobbingCrown`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Tentacles attack all adjacent tiles at the end of your turn.
- **Mechanics**:
```gon
passives {
        Metal 1
        StatusEachTurnEnd {
            ImmediateUseAbility head_ThrobbingCrown
        }
    }
```

### Crown of Chaos (`CrownOfChaos`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Hybrid`
- **Description**: +2 level up Rerolls. Abilities from all classes are offered when you level up.
- **Mechanics**:
```gon
passives {
		AddLevelUpRerolls 2
		LevelUpClassOverride Jester
    }
```

### Child's Crown (`ChildsCrown`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Your basic attack becomes holy and can heal allies.
- **Mechanics**:
```gon
passives {
        Metal 1
        AddElementsToBasicAttack Holy
        AddStatusToBasicAttack {
            DamageOrHealConditionally 1
        }
    }
```

### Tina's Belly Button (`TinasBellyButton`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: When you get a kill, gain +1 Health Regen.
- **Mechanics**:
```gon
passives {
		StatusOnKill {
			HealthRegenUp 1
		}
    }
```

### Hitler's Toupe (`HitlersToupe`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `[Man, Used]`
- **Description**: Permanent Madness. Give Madness to a random enemy at the end of your turn.
- **Mechanics**:
```gon
str 2
	dex 2
    passives {
		PermanentMadness 1
		StatusEachTurnEnd {
			ForceUseAbility head_HitlersToupe
		}
    }
```

### Steven's Hat (`StevensHat`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Your spells cost 0. You can only cast each of your spells once per turn.
- **Mechanics**:
```gon
int -9
	cha -9
	passives {
		SetSpellCosts 0
		MakeSpellsRequireCharge 1
	}
```

### Steven's Helmet (`StevensHelmet`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: When you are downed, give another allied cat 2 random disorders, or to yourself if you're alone.
- **Mechanics**:
```gon
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
```

### Steven (`StevenHat1`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Your explosions are much, much bigger! You have explosion immunity.
- **Mechanics**:
```gon
passives {
		ExplosionImmunity 1
		IncreaseExplosionSize 7
        IncreaseExplosionDamage 2
    }
```

### Steven (`StevenHat2`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Each time you cast a spell, gain +1 range and +1 reach until the end of the turn.
- **Mechanics**:
```gon
passives {
		StatusAfterCastSpell {
			TempRangeUp 1
            TempMeleeRangeUp 1
		}
	}
```

## Category: `legacy_quest_items.gon`

### Throbbing Gristle (`ThrobbingGristle`)
- **Kind**: `weapon` | **Rarity**: `quest` | **Set**: `Meat`
- **Description**: Take it to the Wall of Flesh in the Caves. All units die when they get downed. Use: A melee attack that turns things it kills into Meat.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination caves
    indestructible true
    ability wp_ThrobbingGristle
    global_passives {
        NoCorpses 1
    }
```

### Putrid Leech (`PutridLeech`)
- **Kind**: `head` | **Rarity**: `quest` | **Set**: `Leech`
- **Description**: Take it to the Throbbing Artery in the Boneyard. You never level up and die when downed. You have Lifesteal on all of your attacks and abilities.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination boneyard
    indestructible true
    cursed true
    parasite true
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
```

### Guillotina's Head (`GuillotinasHead`)
- **Kind**: `face` | **Rarity**: `quest` | **Set**: `[Meat, Guts]`
- **Description**: Take it to the Meat Altar in the Throbbing Domain. All battles are Hard battles. Enemies will attack you instead of your allies if they can. Units that contact or attack you have a chance to be Feared. Your basic attack has a +10% chance to inflict Fear.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination meatworld
    hint_prerequisite_flag mapflag_MeatWorldUnlocked
    indestructible true
    cursed true
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
```

### Scalding Orb (`ScaldingOrb`)
- **Kind**: `weapon` | **Rarity**: `quest` | **Set**: `Molten`
- **Description**: Feed it to the Man in the Moon. Toss it to allies with open weapon slots to avoid taking Burn 3 each turn! Applies Burn 3 to units adjacent to allies that catch it.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination moon
    indestructible true
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
```

### Black Shard (`BlackShard`)
- **Kind**: `weapon` | **Rarity**: `quest` | **Set**: `Obelisk`
- **Description**: Use: Absorb a unit with {aux} or less health to power this item up. Transforms after 20 absorptions. [s:.7](Saves its power across multiple runs.)[/s] [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination core
    indestructible true
    aux 1
    ability wp_BlackShard
    passives {
        ItemAuxTransform {
            ge [20 BlackShard_Glowing]
        }
    }
```

### Glowing Black Shard (`BlackShard_Glowing`)
- **Kind**: `weapon` | **Rarity**: `quest` | **Set**: `Obelisk`
- **Description**: Stab it into The Coven!  Use: Deal 5 damage with Lifesteal, inflict Burn 5, and purge all buffs. Instantly kills The Coven. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination core
    quest_item_alias BlackShard //this is the BlackShard, for the purposes of all the quest item code that is keyed on the item name
    indestructible true
    ability wp_BlackShard_Glowing
```

### Pyrophina's Collar (`PyrophinasCollar`)
- **Kind**: `trinket` | **Rarity**: `quest` | **Set**: `Used`
- **Description**: Pyrophina joins you on your journey. She wishes to activate an obelisk on the moon.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination moon
    hint_prerequisite_flag mapflag_BothObelisksUnlocked
    indestructible true
    global_tags [pyrophina_following]
    passives {
        SpawnItemLinkedFamiliar {
            object PyrophinaFamiliar
            break_on_pop_only true
        }
    }
```

### Zaratana's Collar (`ZaratanasCollar`)
- **Kind**: `trinket` | **Rarity**: `quest` | **Set**: `Used`
- **Description**: Zaratana joins you on your journey. She wishes to activate an obelisk in the Core.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination core
    hint_prerequisite_flag mapflag_BothObelisksUnlocked
    indestructible true
    global_tags [zaratana_following]
    passives {
        SpawnItemLinkedFamiliar {
            object ZaratanaFamiliar
            break_on_pop_only true
        }
    }
```

### Cryogenic Time Chamber (`CryogenicTimeChamber_Empty`)
- **Kind**: `trinket` | **Rarity**: `quest` | **Set**: `None`
- **Description**: Put the Throbbing King's heart inside it. All enemy bodies revive to 30% health at the end of each round (except bosses). Find a random pill at the end of each battle.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination meatworld
    hint_prerequisite_flag mapflag_MeatWorldUnlockedFull
    indestructible true
    passives {
        StatusOnBattleEnd {
            FindItemFromPool pills
        }
    }
    global_passives {
        GlobalEnemyAutoRevive 30%
    }
```

### Cryogenic Time Chamber (Throbbing) (`CryogenicTimeChamber_Full`)
- **Kind**: `trinket` | **Rarity**: `quest` | **Set**: `None`
- **Description**: Use it on the time machine in the Lab. All enemy bodies revive to full health at the end of each round (except bosses). +2 Health Regen.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination lab
    indestructible true
    passives {
        HealthRegenUp 2
    }
    global_passives {
        GlobalEnemyAutoRevive 100%
    }
```

### Receiver Antenna (`ReceiverAntenna`)
- **Kind**: `head` | **Rarity**: `quest` | **Set**: `[Bionic, Cyborg]`
- **Description**: Place it far in the past. All events cause special happenings. Gain +2 Charge whenever an ally spends mana.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination jurassic
    indestructible true
    global_tags [all_normal_events_are_weather]
	shield 8
    passives {
        Metal 1
        StatusWhenAllySpendsMana {
            Charge 2
        }
    }
```

### Transmitter Antenna (`TransmitterAntenna`)
- **Kind**: `head` | **Rarity**: `quest` | **Set**: `[Bionic, Cyborg]`
- **Description**: Place it far in the future. Your spells cost -2 mana. Every time you or another cat casts a spell, scramble that spell for the rest of the battle.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination theend
    indestructible true
    passives {
        Metal 1
        AlliesScrambleSpellAfterCast 1
		ReduceManaCost 2
    }
```

### Signal Amplifier (`SignalAmplifier`)
- **Kind**: `weapon` | **Rarity**: `quest` | **Set**: `[Bionic, Cyborg]`
- **Description**: Place it on a floating head inside The Rift. Spawn a random robot miniboss with Madness at the end of the first round. Use: Energize all robots and give yourself All Stats Up.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination dimensionx
    hint_prerequisite_flag mapflag_DimensionXUnlocked
    indestructible true
    ability wp_SignalAmplifier
    passives {
        AbilityOnRoundEndOnce {
            ability wp_SignalAmplifierSpawnTerminator
            even_of_stunned true
        }
    }
```

### Jar of Radiation (`JarOfRadiation`)
- **Kind**: `trinket` | **Rarity**: `quest` | **Set**: `Radioactive`
- **Description**: Fill it with the blood of the Throbbing King. At the end of your turn, deal 1 damage to EVERYTHING. At the end of each battle, gain +1 to a random stat and -1 to a random stat, permanently.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination meatworld
    indestructible true
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
```

### Jar of Radiated Blood (`JarOfRadiatedBlood`)
- **Kind**: `trinket` | **Rarity**: `quest` | **Set**: `Radioactive`
- **Description**: Add a bit of Chaos to it from The Rift. Whenever you take damage, spawn a friendly Clot that can grow into a copy of yourself. At the end of each battle, gain +2 to a random stat and -2 to a random stat, permanently.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination dimensionx
    indestructible true
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
```

### Jar Of Chaos (`JarOfChaos`)
- **Kind**: `trinket` | **Rarity**: `quest` | **Set**: `Radioactive`
- **Description**: Bring it to Dr. Beanies. ...or drink it to permanently gain All Stats Up 2 and upgrade all of your spells.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    indestructible true
    consumable true
    durability 1
    dont_destroy_on_0 true
    failable true
    ability cm_JarOfChaos
    passives {
        DurabilityTransform {
            eq [0 JarOfNothing]
        }
    }
```

### Jar Of Nothing (`JarOfNothing`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `None`
- **Description**: It's trash now.
- **Mechanics**:
```gon
dont_destroy_on_0 true
```

### Nuke (`Nuke`)
- **Kind**: `neck` | **Rarity**: `quest` | **Set**: `Radioactive`
- **Description**: Take it to The Infinite and wait for the signal from Dr. Beanies to set it off. +2 Brace. If this cat dies, it explodes and damages everything for 50. Bonus Ability: Trigger the Nuke.
- **Mechanics**:
```gon
quest_item true
    legacy_quest true
    hint_destination endoftime
    indestructible true
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
```

## Category: `legendary_items.gon`

### Fancy Bow (`TinksBow`)
- **Kind**: `head` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: It's fancy.
- **Mechanics**:
```gon
degrade_after_adventure false
```

## Category: `modifiers.gon`

### {str_aux_passive_name} Syringe (`LearnPassive`)
- **Kind**: `modifier` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use to immediately teach a cat the passive ability: {str_aux_passive_name}  {str_aux_passive_desc}
- **Mechanics**:
```gon
str_aux_initialize random_class_passive
    icon_hint passive_syringe
```

### {str_aux_passive_name} Syringe (`LearnDisorder`)
- **Kind**: `modifier` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use to immediately give a cat the disorder: {str_aux_passive_name}  {str_aux_passive_desc}
- **Mechanics**:
```gon
str_aux_initialize random_disorder
    icon_hint passive_syringe
```

### {str_aux_active_name} Syringe (`LearnAbility`)
- **Kind**: `modifier` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use to immediately teach a cat the active ability: {str_aux_active_name}  {str_aux_active_desc}
- **Mechanics**:
```gon
str_aux_initialize random_class_ability
    icon_hint ability_syringe
```

### [U] (`Upgrade`)
- **Kind**: `modifier` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: [U]

### [S] (`StatUp`)
- **Kind**: `modifier` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: [U]

### [S] (`StatShuffle`)
- **Kind**: `modifier` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: [U]

### [H] (`InstantHeal`)
- **Kind**: `modifier` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: [U]

### [C] (`CureDisorder`)
- **Kind**: `modifier` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: [U]

### [T] (`TemporaryBuff`)
- **Kind**: `modifier` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: [U]

## Category: `neck_items.gon`

### Lion Mane (`LionMane`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
str 1
    con 1
    cha 1
	int -1
	spd -1
```

### Gobbler (`Gobbler`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Fatty`
- **Description**: Units that contact you are knocked back 2 tiles.
- **Mechanics**:
```gon
con 4
    spd -2
    passives {
        MeleeRevengeDamage {
            knockback 2
        }
    }
```

### Spiked Collar (`SpikedCollar`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: +2 Thorns.
- **Mechanics**:
```gon
passives {
        Thorns 2
        Metal 1
    }
```

### Frank Bolts (`FrankBolts`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Bionic, Cyborg]`
- **Description**: Electric immunity. Electric damage revives you when downed.
- **Mechanics**:
```gon
shield 2
    passives {
        FrankBolts 1
        Metal 1
    }
```

### Fortune Necklace (`FortuneNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `None`
- **Description**: Spawn 3-6 coins at the start of each battle. Fragile.
- **Mechanics**:
```gon
passives {
        Fragile 1
        SpawnOnBattleStartRandomEmptyTile {
            object Coin
            number [3 6]
        }
    }
```

### Scarf (`Scarf`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `None`
- **Description**: Ice immunity.
- **Mechanics**:
```gon
cha 1
    passives {
        ElementImmune Ice
        StatusImmunity [Freeze, Slow]
    }
```

### Bulletproof Vest (`BulletproofVest`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Injury immunity.
- **Mechanics**:
```gon
spd -1
    dex -1
    passives {
        InjuryImmunity 1
    }
```

### Lucky Toe (`LuckyToe`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[HumanFlesh, Lucky, Twine]`
- **Description**: 
- **Mechanics**:
```gon
lck 2
    passives {
        ChanceToForceEvent {
            chance 25%
            event Blessing
        }
    }
```

### Bling (`Bling`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
shield 4
    spd -2
    cha 2
    passives {
        Metal 1
    }
```

### Odd Medallion (`OddMedallion`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `[Used, Twine, Demonic]`
- **Description**: Deal 1 electric damage to units that contact or attack you. 25% chance to poop every time you take damage.
- **Mechanics**:
```gon
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
```

### Fish Necklace (`FishNecklace`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Rotten, Twine]`
- **Description**: Poisonous 1. Damage you deal inflicts Rot 1. Allied flies have +2 Damage.
- **Mechanics**:
```gon
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
```

### Two of Spades (`TwoOfSpades`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Twine`
- **Description**: Double cast spells that cost 1 or 2 mana.
- **Mechanics**:
```gon
passives {
        DoubleCastSpellIfManaCostUnderThreshold 3
    }
```

### Colostomy Bag (`ColostomyBag`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Fecal, Used]`
- **Description**: Spawn Charmed Dips randomly when you move over tiles. While downed, spawn a Charmed Dip at the end of each round.
- **Mechanics**:
```gon
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
```

### Survivalist's Gaiter (`SurvivalistGaiter`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Survivalist`
- **Description**: +40% Dodge Chance while standing in tall grass. Start each battle with Stealth 1. Lose this stealth when you use your basic attack.
- **Mechanics**:
```gon
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
```

### Peace Symbol (`PeaceSymbol`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Hippie, Twine]`
- **Description**: If you end your turn without dealing damage, gain +1 [img:divineshield].
- **Mechanics**:
```gon
keyword_tooltips { DivineShield 1 }
    passives {
        StatusEachTurnBegin {
            BlessingOfPeace 1
        }
    }
```

### Empty Generator (`EmptyGenerator`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: When you spend 12 or more mana in a turn, refresh your basic attack.
- **Mechanics**:
```gon
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
```

### Dark Friend (`DarkFriend`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Demonic`
- **Description**: At the start of your turn, spawn a Shadow copy that mimics your basic attack and fades at the end of the turn. Units that contact or attack you have a 15% chance to be Feared.
- **Mechanics**:
```gon
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
```

### Fanny Pack (`FannyPack`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `[Leather, Survivalist]`
- **Description**: Spawn 1-2 extra pickups at the start of each battle. After you collect your 3rd pickup, you can move an extra time each turn.
- **Mechanics**:
```gon
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
```

### Morphine Drip (`MorphineDrip`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Medical, Nurse]`
- **Description**: Damage you take is reduced by 3. Damage prevented this way is delayed and taken at the end of your turn, all at once.
- **Mechanics**:
```gon
passives {
        ConvertDamageToScaledStatus {
            stacks 3
            DelayedPain 1
        }
    }
```

### Leather Jacket (`LeatherJacket`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Leather, Cool]`
- **Description**: If you would take exactly 1 damage, take 0 instead.
- **Mechanics**:
```gon
shield 3
    passives {
        BlockDamageUnderThreshold 1
    }
```

### Healing Gauze (`HealingGauze`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Mummy, Nurse]`
- **Description**: You have +3 Health Regen as long as you have [img:shield].
- **Mechanics**:
```gon
passives {
        PassiveWhileShielded {
            HealthRegenUp 3
        }
    }
```

### Mark IV (`MarkIV`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: After every fourth spell you cast, gain +2 [img:int].
- **Mechanics**:
```gon
passives {
        Metal 1
        StatusEveryXSpellCasts {
            stacks 4
            IntelligenceUp 2
        }
    }
```

### Mama Leech (`MamaLeech`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Leech, Mother]`
- **Description**: After every third spell you cast, spawn a Leech familiar.
- **Mechanics**:
```gon
passives {
        StatusEveryXSpellCasts {
            stacks 3
            ObjectOnHitCharacter {
                stacks 1
                object CharmedLeech
            }
        }
    }
```

### Furry Dice (`FuryDice`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Lucky, Twine]`
- **Description**: You can reroll your options when you level up.
- **Mechanics**:
```gon
lck 1
    passives {
        AddLevelUpRerolls 1
    }
```

### DNA Multiplier (`DNAMultiplier`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Double all status effects that get applied to you.
- **Mechanics**:
```gon
passives {
        Metal 1
        DoubleReceivedNegativeStatus 1
        DoubleReceivedPositiveStatus 1
    }
```

### Pack of Blades (`PackOfBlades`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Whenever you backstab, gain +1 Serrated Claws.
- **Mechanics**:
```gon
passives {
        Metal 1
        StatusOnBackstab {
            SerratedClaws 1
        }
    }
```

### Backpack (`Backpack`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Survivalist`
- **Description**: 50% chance to find an extra consumable item at the end of each battle. When you use up a consumable or trinket, equip a new consumable from your inventory if you have any.
- **Mechanics**:
```gon
passives {
        StatusOnBattleEnd {
            Conditional_GoodRoll {
                odds 50%
                FindItemFromPool consumables
            }
        }
        AutoEquipConsumables 1
    }
```

### Stone Orbit (`StoneOrbit`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Rock, Planet]`
- **Description**: Spawn a small rock when you take damage.
- **Mechanics**:
```gon
shield 2
    passives {
        SpawnThingOnDamage {
            object SmallRock
        }
    }
```

### Angelic Protection (`AngelicProtection`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Cleric`
- **Description**: 33% chance to teleport to a random tile when targeted by an enemy.
- **Mechanics**:
```gon
passives {
        ChanceToBackflip {
            ability BlinkDodge
            chance 33%
        }
    }
```

### Chef's Apron (`ChefsApron`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Butcher`
- **Description**: At the end of each turn, gain +1 [img:con] and spawn a random food pickup within 2 tiles.
- **Mechanics**:
```gon
passives {
        StatusEachTurnEnd {
            ConstitutionUp 1
            ForceUseAbility neck_ChefsApron
        }
    }
```

### Radar Dish (`RadarDish`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Cyborg, Bionic, Space]`
- **Description**: One random enemy becomes Marked at the start of each turn.
- **Mechanics**:
```gon
passives {
        Metal 1
        ApplyStatusesToRandomEnemiesEachTurn {
            count 1
            Marked 1
        }
    }
```

### Extra Set of Eyes (`ExtraSetOfEyes`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Space`
- **Description**: At the end of each turn, gain +1 Preemptive Counterattack.
- **Mechanics**:
```gon
passives {
        StatusEachTurnEnd {
            PreEmptiveCounterNextAttacks 1
        }
    }
```

### Large Shark Tooth (`SharkTooth`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Twine`
- **Description**: Your basic attack inflicts +1 Bleed. Take an extra turn at the end of the round for each Bleeding enemy. You are uncontrollable during these turns.
- **Mechanics**:
```gon
passives {
        SharkySmellsBlood 1
        AddStatusToBasicAttack {
            Bleed 1
        }
    }
```

### Small Rune (`SmallRune`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `[Rune, Twine]`
- **Description**: +10% Dodge Chance.
- **Mechanics**:
```gon
passives {
        ArmorDodgeChance 10%
    }
```

### Quartz Necklace (`QuartzNecklace`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `[Gemstone, Twine]`
- **Description**: +1 Brace.
- **Mechanics**:
```gon
passives {
        Brace 1
    }
```

### Cinder Block (`CinderBlock`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Rock`
- **Description**: 
- **Mechanics**:
```gon
shield 3
```

### Boxing Charm (`BoxingCharm`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `[Fighter, Twine]`
- **Description**: Start with +1 bonus attack.
- **Mechanics**:
```gon
passives {
        Quivered 1
    }
```

### Crucifix (`Crucifix`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Cleric`
- **Description**: 
- **Mechanics**:
```gon
divine_shield 1
```

### Tattered Scrap (`TatteredScrap`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `[Tinkerer, Scrap]`
- **Description**: When you take damage, spawn a scrap pickup.
- **Mechanics**:
```gon
passives {
        Metal 1
        SpawnThingOnDamage {
            object Scrap
			good false //good relative to the thing attacking, for luck calculations
        }
    }
```

### Meek Stone (`MeekStone`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `Gemstone`
- **Description**: You have All Stats Up while at 10 or less health.
- **Mechanics**:
```gon
passives {
        PassiveAtHealthThreshold {
            threshold 10
            mode less_or_equal
            passives {
                AllStatsUp 1
            }
        }
    }
```

### Stomach (`Stomach`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Guts`
- **Description**: Consumables you use have double the effect.
- **Mechanics**:
```gon
passives {
        ConsumableEffectsMultiplierBonus 1
    }
```

### Water Feeder (`WaterFeeder`)
- **Kind**: `neck` | **Rarity**: `common` | **Set**: `None`
- **Description**: +1 Health Regen. Become wet at the start of your turn.
- **Mechanics**:
```gon
passives {
        HealthRegenUp 1
        StatusEachTurnBegin {
            DrinkWater 1
            Wet 1
        }
    }
```

### Scrubs (`Scrubs`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `[Nurse, Medical]`
- **Description**: Heals heal you for 2 extra.
- **Mechanics**:
```gon
passives {
        BoostReceivedHealing 2
    }
```

### Scapular (`Scapular`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Cleric`
- **Description**: 
- **Mechanics**:
```gon
divine_shield 1
    str 1
    dex 1
    con 1
    cha 1
	int 1
	spd 1
	lck 1
```

### Dirty Bionic Armor (`DirtyBionicArmor`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `[DirtClod, Bionic]`
- **Description**: +2 Mana Regen, +2 Health Regen.
- **Mechanics**:
```gon
spd 4
	passives {
		AddManaRegen 2
		HealthRegenUp 2
		Metal 1
	}
```

### Lucky Twine (`LuckyTwine`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `[Twine, Lucky]`
- **Description**: 75% chance to Grapple units that make contact with you.
- **Mechanics**:
```gon
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
```

### Raven Feather (`RavenFeather`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Feathered`
- **Description**: Inflict Soul Link on 2 random enemies at the start of each battle.
- **Mechanics**:
```gon
passives {
		AbilityOnBattleStart RandomDualSoulLink
    }
```

### Lost Soul (`LostSoul`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: The first time you are downed each battle, revive to full HP.
- **Mechanics**:
```gon
passives {
        Eternal {
            stacks 1
            health_percent 100%
        }
    }
```

### Mother's Teeth (`MothersTeeth`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Mother`
- **Description**: +6 Bleed Thorns, +6 Thorns, +6 Bleed.
- **Mechanics**:
```gon
passives {
		BleedThorns 6
		Thorns 6
		Bleed 6
    }
```

### Mega Poop (`MegaPoop`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Fecal`
- **Description**: Leave poop behind when you move. Spawn 2-3 pickups whenever you destroy a poop.
- **Mechanics**:
```gon
cha -1
	shield 4
    passives {
		LeaveBehindOnceEachMove Poop
        SpawnRandomPickupsOnTaggedUnitKilled {
            tag poop
            count [2 3]
        }
    }
```

### Zodiacs Poncho (`ZodiacsPoncho`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Rag`
- **Description**: +1 Range. During your turn, one random enemy has a Bounty.
- **Mechanics**:
```gon
passives {
		AddBonusRange 1
		ApplyStatusesToRandomEnemiesEachTurn {
			Bounty 1
		}
	}
```

### Coffin Armor (`CoffinArmor`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Wood`
- **Description**: +1 Thorns.
- **Mechanics**:
```gon
shield 3
	divine_shield 1
	passives {
		Thorns 1
	}
```

### Nubs Collar (`NubsCollar`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Leather`
- **Description**: Your movement action is Belly Flop.
- **Mechanics**:
```gon
passives {
		ReplaceBasicMove BellyFlop_BasicMove
	}
```

### Chub's Collar (`ChubsCollar`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Leather`
- **Description**: Your basic attack is Spin Attack.
- **Mechanics**:
```gon
str 1
    attack BasicSpin
	passives {
		OverrideBasicAttack BasicSpin
	}
```

### Blubber (`Blubber`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Fatty`
- **Description**: 
- **Mechanics**:
```gon
con 7
	spd -5
	cha -2
    passives {
    }
```

### Ethereal Rings (`EtherealRings`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Kinetic Spikes 3. Emit 3 Sparkles when you use your basic attack.
- **Mechanics**:
```gon
shield 3
    passives {
		KineticSpikes 3
        AddSelfStatusToBasicAttack {
            RandomMagicMissile 3
        }
    }
```

### White Rabbit Paw (`WhiteRabbitPaw`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `[Lucky, Twine]`
- **Description**: 
- **Mechanics**:
```gon
lck 5
    passives {
    }
```

### Glowing Pelt (`GlowingPelt`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: +5 Health Regen. When you're downed, revive at the end of the round.
- **Mechanics**:
```gon
passives {
		HealthRegenUp 5
        ChanceToRevive 100
    }
```

### Polyp (`Polyp`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Meat, HumanFlesh]`
- **Description**: +1 Health Regen. 25% chance to spawn a Charmed Clot when you take damage.
- **Mechanics**:
```gon
passives {
		HealthRegenUp 1
		SpawnThingOnDamage {
			object CharmedClot
			number 1
			chance .25
		}
	}
```

### Robo Arm (`RoboArm`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `[Bionic, Cyborg]`
- **Description**: Start with +1 bonus attack. Collect all adjacent pickups when you end your turn.
- **Mechanics**:
```gon
passives {
        Metal 1
		Quivered 1
        StatusEachTurnEnd {
            ForceUseAbility tk_RoboSucc
        }
    }
```

### Brambles (`Brambles`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Leafy`
- **Description**: +1 Thorns. Spawn brambles in adjacent tiles when you end your turn. You are immune to tile effects.
- **Mechanics**:
```gon
passives {
		Thorns 1
		IgnoreTiles 1
        StatusEachTurnEnd {
            ForceUseAbility neck_Brambles
        }
    }
```

### Crusty Sock (`CrustySock`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Used`
- **Description**: Spawn a Gamete familiar at the start of each battle.
- **Mechanics**:
```gon
passives {
		SpawnOnBattleStart CharmedGamete
	}
```

### Tombstone (`Tombstone`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Rock`
- **Description**: Your basic attack has +2 Knockback and a +10% chance to Stun.
- **Mechanics**:
```gon
shield 6
	spd -2
	passives {
		AddStatusToBasicAttack {
			Knockback 2
            Stun [1, .1]
		}
	}
```

### Broken Window (`BrokenWindow`)
- **Kind**: `neck` | **Rarity**: `rare` | **Set**: `Wood`
- **Description**: +3 Bleed Thorns. Bleed 1.
- **Mechanics**:
```gon
passives {
		BleedThorns 3
		Bleed 1
    }
```

### Pyrophina's Toenail (`PyrophinasToenail`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Fire Immunity.
- **Mechanics**:
```gon
shield 8
    passives {
		ElementImmune Fire
        StatusImmunity [Burn]
    }
```

### Zaratana's Turd (`ZaratanaTurd`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `[Fecal, Rock]`
- **Description**: Knockback immunity.
- **Mechanics**:
```gon
shield 8
    passives {
		KnockbackImmunity 1
    }
```

### Steven's Gobbler (`StevensGobbler`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Units that contact you get knocked back. Knockback you deal is increased by 10 and inflicts Bruise 1.
- **Mechanics**:
```gon
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
```

### Steven's Friend (`StevensFriend`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Each time you cast a spell, spawn a Shadow copy of yourself that mimics your basic attack and fades at the end of your turn.
- **Mechanics**:
```gon
passives {
		StatusAfterCastSpell {
			UseAbility neck_DarkFriend
		}
	}
```

### Steven (`StevenNeck1`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Your Holy Element spells cost -1 mana.
- **Mechanics**:
```gon
passives {
        ElementalManaCostReduction {
            element [Holy]
            reduction 1
        }
    }
```

### Steven (`StevenNeck2`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: While you're downed, receiving any damage revives you.
- **Mechanics**:
```gon
passives {
        StevenBolts 1
    }
```

### A Friends Foot (`AFriendsFoot`)
- **Kind**: `neck` | **Rarity**: `very_rare` | **Set**: `HumanFlesh`
- **Description**: Gain +1 [img:lck] when you get a kill.
- **Mechanics**:
```gon
lck 1
    passives {
		StatusOnKillEnemy {
			LuckUp 1
		}
    }
```

## Category: `parasites.gon`

### Tapeworm (`Tapeworm`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Your basic attack inflicts Poison 1.
- **Mechanics**:
```gon
cursed true
    parasite true
    con -2
    passives {
        AddStatusToBasicAttack {
            Poison 1
        }
    }
```

### Pinworm (`Pinworm`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: Spawns a Maggot familiar when you take damage.
- **Mechanics**:
```gon
cursed true
    parasite true
    con -1
    str -1
    passives {
        SpawnThingOnDamage {
            object CharmedMaggot
            good false //good relative to the thing attacking, for luck calculations
        }
    }
```

### Ringworm (`Ringworm`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: Your basic attack inflicts Weakness 3.
- **Mechanics**:
```gon
cursed true
    parasite true
    cha -3
    passives {
        AddStatusToBasicAttack {
            Weakness 3
        }
    }
```

### Heartworm (`Heartworm`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: When downed, your body is destroyed.
- **Mechanics**:
```gon
cursed true
    parasite true
    durability 1
    lck 3
    passives {
        AddCorpseHealth -999999
    }
```

### Botfly Larva (`BotflyLarva`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Spawns 2 Pooter familiars when you're downed.
- **Mechanics**:
```gon
cursed true
    parasite true
    spd -1
    cha -1
    passives {
        SpawnThingOnDeath CharmedPooter
        SpawnThingOnDeath CharmedPooter
    }
```

### Brain Maggot (`BrainMaggot`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: Revive with 50% HP 2 rounds after you are downed.
- **Mechanics**:
```gon
cursed true
    parasite true
    int -3
    passives {
        DelayedAutoRevive {
            rounds 2
            health 50%
        }
    }
```

### Spider Egg (`SpiderEgg`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Your basic attack inflicts Infested.
- **Mechanics**:
```gon
cursed true
    parasite true
    passives {
        AddStatusToBasicAttack {
            SpiderInfested 1
        }
    }
```

### Spider Webber (`SpiderWebber`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A ranged attack that inflicts Webbed.
- **Mechanics**:
```gon
cursed true
    parasite true
    ability wp_SpiderWebber
```

### Amoeba (`AmoebaHat`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Amoeba`
- **Description**: +1 Brace. +10% Miss Chance.
- **Mechanics**:
```gon
cursed true
    parasite true
    shield 4
    int -1
    passives {
        Brace 1
		MissChance 10
    }
```

### Amoeba (`AmoebaNeck`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `Amoeba`
- **Description**: +1 Brace. +10% Miss Chance.
- **Mechanics**:
```gon
cursed true
    parasite true
	shield 4
    con -1
    passives {
        Brace 1
		MissChance 10
    }
```

### Amoeba (`AmoebaFace`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `Amoeba`
- **Description**: +1 Brace. +10% Miss Chance.
- **Mechanics**:
```gon
cursed true
    parasite true
	shield 4
	cha -1
    passives {
        Brace 1
        MissChance 10
    }
```

### Soul Sucker (`SoulSucker`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: Restore 2 mana when you kill an enemy.
- **Mechanics**:
```gon
cursed true
    parasite true
    con -1
    passives {
        StatusOnKillEnemy {
            ManaGain 2
        }
    }
```

### Best Bud (`BestBud`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: 10% chance to break when you take damage. When this breaks, gain a permanent Leech familiar.
- **Mechanics**:
```gon
cursed true
    parasite true
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
```

### Angry Worm (`AngryWorm`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: Your basic attack hits an extra time for 1 damage.
- **Mechanics**:
```gon
cursed true
    parasite true
    con -1
    passives {
        AddTemporaryEffectsToBasicAttack {
            CastAgainWithStatus {
                stacks 1
                OverrideDamage 1
            }
        }
    }
```

### Heal Worm (`HealWorm`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: +2 Health Regen.
- **Mechanics**:
```gon
cursed true
    parasite true
    con -1
    passives {
        HealthRegenUp 2
    }
```

### Cymothoa Exigua (`CymothoaExigua`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: 
- **Mechanics**:
```gon
cursed true
    parasite true
    cha -2
    str 2
    dex 2
    passives {
    }
```

### Eye Worm (`EyeWorm`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: +10% Miss Chance. 75% chance to equip a piece of Grub armor at the start of each battle. This will destroy any armor it replaces.
- **Mechanics**:
```gon
cursed true
    parasite true
    passives {
        MissChance 10
        StatusOnBattleStart {
            DestroyEquipmentAndAttachParasite {
                chance .75
                pool [FaceGrub HeadGrub NeckGrub]
            }
        }
    }
```

### Scabies (`Scabies`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: Bruise 2. Spawn a charmed Flea when you take damage.
- **Mechanics**:
```gon
cursed true
    parasite true
    passives {
        Bruise 2
        SpawnThingOnDamage {
            object CharmedFlea
            spawn_on_death_hit false
        }
    }
```

### Bean Parasite (`BeanParasite`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: Confusion 99.
- **Mechanics**:
```gon
cursed true
    parasite true
    int 5
    passives {
        Confusion 99
    }
```

### Cordyceps (`Cordyceps`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: 30% chance to gain +2 [img:spd] and become AI controlled at the start of your turn.
- **Mechanics**:
```gon
cursed true
    parasite true
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
```

### Naegleria Fowleri (`NaegleriaFowleri`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: Brace {aux}. Gain -1 [img:int] at the end of each battle, permanently. This gains +2 [img:shield] and +1 Brace at the end of each battle.  If your [img:int] is 0 or less, you are uncontrollable.
- **Mechanics**:
```gon
cursed true
    parasite true
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
```

### Malaria (`Malaria`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `Parasite`
- **Description**: At the end of each battle, all your [img:con] is permanently reduced by 1. Spawn 2 Charmed Fly Swarms when you're downed. If your [img:con] is 0 or less, start each battle downed.
- **Mechanics**:
```gon
cursed true
    parasite true
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
```

### The Tick (`TheTick`)
- **Kind**: `neck` | **Rarity**: `uncommon` | **Set**: `Parasite`
- **Description**: Inflict All Stats Down on bosses and minibosses at the start of each battle. Heal +12 HP at the end of each battle.
- **Mechanics**:
```gon
cursed true
    parasite true
    con -1
    passives {
        AddEndOfCombatRegen 12
        StatusAllCharactersOnSpawn {
            Conditional_Boss {
                AllStatsUp -1
            }
        }
    }
```

### Parous Worm (`Parousworm`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: 66% chance to find a random parasite at the end of each battle.
- **Mechanics**:
```gon
cursed true
    parasite true
    con -1
    passives {
        StatusOnBattleEnd {
            Conditional_GoodRoll {
                odds 66%
                FindItemFromPool parasites
			}
        }
    }
```

### Hookworm (`Hookworm`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Spawn a Charmed Leech when you take damage.
- **Mechanics**:
```gon
cursed true
    parasite true
	con -1
	spd -1
	passives {
        SpawnThingOnDamage {
            object CharmedLeech
        }
	}
```

### Cooties (`Cooties`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Your basic attack inflicts Weakness, Rot and Infested.
- **Mechanics**:
```gon
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
```

### Lice (`Lice`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Bruise 1. Spawn a charmed Louse when you take damage.
- **Mechanics**:
```gon
cursed true
    parasite true
	passives {
		Bruise 1
        SpawnThingOnDamage {
            object CharmedLice
        }
	}
```

### Sacculina Carcini (`SacculinaCarcini`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
cursed true
    parasite true
	spd -1
	shield 5
    passives {
    }
```

### Roundworm (`Roundworm`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Units that contact you get knocked back 5 tiles.
- **Mechanics**:
```gon
cursed true
    parasite true
	con -1
    passives {
        MeleeRevengeDamage {
            knockback 5
        }
    }
```

### Euhaplorchis Californiensis (`EuhaplorchisCaliforniensis`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Start with Confusion 3.
- **Mechanics**:
```gon
cursed true
    parasite true
	spd 4
    passives {
		Confusion 3
    }
```

### Beepis (`Beepis`)
- **Kind**: `head` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Your passives are duplicated during battle. Your spells cost +2 mana and can only be used once per turn.
- **Mechanics**:
```gon
cursed true
    parasite true
    passives {
        ManaCostReduction -2
        AllSpellsCostCharge 1
        CopyPassiveSlot 0
        CopyPassiveSlot 1
    }
```

### Feebis (`Feebis`)
- **Kind**: `face` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Your spells cost -2 mana and the first one you cast each turn is double cast. Your basic attack is Poke and your movement range is 1.
- **Mechanics**:
```gon
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
```

### Cunch (`Cunch`)
- **Kind**: `neck` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: You can use your basic attack and movement action an extra time each turn. Your passives are disabled during battle.
- **Mechanics**:
```gon
cursed true
    parasite true
    passives {
        ExtraBasicAttacks_Status 1
        ExtraBasicMoves_Status 1
        DisablePassiveSlot 0
        DisablePassiveSlot 1
    }
```

## Category: `special_class_items.gon`

### Monk Fist (`MonkFist`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: You can use your basic attack an extra time each turn. Innate
- **Mechanics**:
```gon
sticky true
    fragile true
    indestructible true
    passives {
        ExtraBasicAttacks 1
    }
```

### Stance Switcher (`MonkStyleChanger`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Switch between melee and ranged stances. You have Brace 1 while in melee stance. Innate
- **Mechanics**:
```gon
sticky true
    fragile true
    indestructible true
    ability tk_MonkStyleChange
    passives {
        PassiveWhileInMonkMeleeStance {
            Brace 1
        }
    }
```

### Meat Hook (`ButcherHook`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Pull a unit toward you. Innate
- **Mechanics**:
```gon
sticky true
    fragile true
    indestructible true
    ability wp_MeatHookB
```

### Meat Hook (`ButcherHook_Temporary`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Pull a unit toward you.
- **Mechanics**:
```gon
ability wp_MeatHookB
```

### Soul Dagger (`Necro_SoulDagger_Uncharged`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack. If this weapon damages an allied cat, gain one of their spells at random in your bonus ability slot. If this weapon downs an ally it becomes Charged for the rest of the battle.
- **Mechanics**:
```gon
ability wp_NecroSoulDagger
```

### Charged Soul Dagger (`Necro_SoulDagger_Charged`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack with Lifesteal. If this weapon damages an allied cat, gain one of their spells at random in your bonus ability slot. Loses its charge at the end of the battle.
- **Mechanics**:
```gon
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
```

### Sleep Dart (`SleepDart`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A straight ranged attack that inflicts Sleep 1.
- **Mechanics**:
```gon
durability 1
    ability wp_SleepDart
```

### Sleep Dart (`SleepDart2`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A straight ranged attack that inflicts Sleep 1.
- **Mechanics**:
```gon
durability 2
    ability wp_SleepDart
```

## Category: `trinkets.gon`

### Rat Tail (`RatTail`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `Rat`
- **Description**: 
- **Mechanics**:
```gon
lck 1
```

### Rat Heart (`RatHeart`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `[Rat, Guts]`
- **Description**: 
- **Mechanics**:
```gon
con 1
```

### Rat Bezoar (`RatBeezer`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `Rat`
- **Description**: Poisonous 1.
- **Mechanics**:
```gon
passives {
        PoisonThorns 1
    }
```

### Book (`Book`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `Paper`
- **Description**: 
- **Mechanics**:
```gon
int 1
```

### Dumbbell (`Dumbell`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `Lead`
- **Description**: 
- **Mechanics**:
```gon
str 1
```

### Jazzercise VHS Tape (`Jazzercise`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
dex 1
```

### Old Shoe (`OldShoe`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `[Used, Leather]`
- **Description**: 
- **Mechanics**:
```gon
spd 1
```

### Body Spray (`BodySpray`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
cha 1
```

### Lucky Penny (`LuckyPenny`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `Lucky`
- **Description**: 
- **Mechanics**:
```gon
lck 1
```

### Wiz Cheese (`WizCheese`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `None`
- **Description**: 
- **Mechanics**:
```gon
con 1
```

### Snaggle Tooth (`SnaggleTooth`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Bone`
- **Description**: Your basic attack inflicts Bleed 1.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            Bleed 1
        }
    }
```

### Jar of Leeches (`JarOfLeeches`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Leech`
- **Description**: Your basic attack inflicts Leech 1.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            Leeches 1
        }
    }
```

### Brass Knuckles (`BrassKnuckles`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Fighter`
- **Description**: Your basic attack inflicts Bruise 1.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            Bruise 1
        }
    }
```

### Fly Larva (`FlyLarva`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Fly`
- **Description**: Your basic attack inflicts Rot 1.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            Rot 1
        }
    }
```

### Strange Marble (`StrangeMarble`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Your basic attack inflicts Mana Leech 1.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            ManaLeeches 1
        }
    }
```

### Vibrating Skull (`VibratingSkull`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[Bone, Space]`
- **Description**: Your basic attack inflicts Magic Weakness 1.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            MagicWeakness 1
        }
    }
```

### Bone Marrow (`BoneMarrow`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Meat, Bone]`
- **Description**: Heal to full at the end of each battle.
- **Mechanics**:
```gon
passives {
        AddEndOfCombatRegen 999999
    }
```

### Feather (`Feather`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Feathered`
- **Description**: Take your turn earlier.
- **Mechanics**:
```gon
spd 1
    passives {
        AddInitiative 100
    }
```

### Weight (`Weight`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Lead`
- **Description**: Trample. Take your turn later.
- **Mechanics**:
```gon
passives {
        AddInitiative -20
		Trample 3
    }
```

### Match Stick (`MatchStick`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Your basic attack inflicts Burn 1.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            Burn 1
        }
    }
```

### Bee Stinger (`BeeStinger`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Your basic attack inflicts Poison 1.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            Poison 1
        }
    }
```

### Pull Tab (`PullTab`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `Scrap`
- **Description**: 
- **Mechanics**:
```gon
shield 4
```

### Self-Destruct Button (`SelfDestructButton`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Vaporize yourself and deal 50 damage to adjacent units.
- **Mechanics**:
```gon
ability tr_SelfDestruct
```

### Empty Syringe (`EmptySyringe`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Medical`
- **Description**: When you inflict Bleed or Poison, inflict +1 Bleed or Poison.
- **Mechanics**:
```gon
passives {
        AmplifyStatus Bleed
		AmplifyStatus Poison
    }
```

### Liquid Nitrogen (`LiquidNitrogen`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Frozen`
- **Description**: Your Ice Element damage is increased by 2.
- **Mechanics**:
```gon
passives {
        AddDamageToElementDamage {
            element Ice
            damage 2
        }
    }
```

### Ember (`Ember`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Molten`
- **Description**: Your Fire Element damage is increased by 1 and inflicts +1 Burn.
- **Mechanics**:
```gon
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
```

### Conductor (`Conductor`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Your Electric Element damage is increased by 1 and has +10% chance to Stun.
- **Mechanics**:
```gon
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
```

### Feed Bag (`FeedBag`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[Druid, Hunter]`
- **Description**: Familiars you spawn gain +2 max HP.
- **Mechanics**:
```gon
passives {
        AddPassivesToMinions {
            AddMaxHealth 2
            HealthGain 2 //fill up the blank max health
        }
    }
```

### Nightshade (`Nightshade`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Flower`
- **Description**: When you inflict Poison, inflict +2 Poison. Start with Poison 2.
- **Mechanics**:
```gon
passives {
	    Poison 2
        AmplifyStatus Poison
		AmplifyStatus Poison
    }
```

### Neverstone (`Neverstone`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Rock, Gemstone]`
- **Description**: Never level up.
- **Mechanics**:
```gon
prevent_level_up true
```

### Pawn (`Pawn`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `None`
- **Description**: Use: Move 1 tile toward the closest enemy.
- **Mechanics**:
```gon
durability 10
    ability tk_Pawn
```

### Knight (`Knight`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Jump in an L shape.
- **Mechanics**:
```gon
durability 6
    ability tk_Knight
```

### Rook (`Rook`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Move any number of tiles in a straight line.
- **Mechanics**:
```gon
durability 6
    ability tk_Rook
```

### Queen (`Queen`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Move any number of tiles in a straight or diagonal line.
- **Mechanics**:
```gon
durability 8
    ability tk_Queen
```

### Petrified Poop (`PetrifiedPoop`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[Rock, Fecal]`
- **Description**: Familiars you spawn gain +2 [img:shield].
- **Mechanics**:
```gon
shield 2
	passives {
        AddPassivesToMinions {
            Shield 2
        }
    }
```

### Fish Hook (`FishHook`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Barbed`
- **Description**: If you would knockback a unit, instead deal extra damage to it equal to the knockback.
- **Mechanics**:
```gon
passives {
        StripKnockback 1
    }
```

### Human Hand (`HumanHand`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `HumanFlesh`
- **Description**: 
- **Mechanics**:
```gon
str 2
```

### Human Brain (`HumanBrain`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[HumanFlesh, Guts]`
- **Description**: 
- **Mechanics**:
```gon
int 2
```

### Human Leg Bone (`HumanLeg`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Bone`
- **Description**: 
- **Mechanics**:
```gon
dex 2
```

### Human Toe (`HumanToe`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `HumanFlesh`
- **Description**: 
- **Mechanics**:
```gon
lck 2
```

### Human Heart (`HumanHeart`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[HumanFlesh, Guts]`
- **Description**: 
- **Mechanics**:
```gon
con 2
```

### Human Foot (`HumanFoot`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `HumanFlesh`
- **Description**: 
- **Mechanics**:
```gon
spd 2
```

### Human Eye (`MysteriousEye`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[HumanFlesh, Guts]`
- **Description**: 
- **Mechanics**:
```gon
cha 2
```

### D6 (`D6`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `None`
- **Description**: You can reroll your options when you level up.
- **Mechanics**:
```gon
passives {
        AddLevelUpRerolls 1
    }
```

### Metal Plate (`MetalSquare`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Scrap`
- **Description**: Gain +1 Brace when you kill an enemy.
- **Mechanics**:
```gon
passives {
        StatusOnKillEnemy {
            Brace 1
        }
    }
```

### Blinking Eyeball (`BlinkingEyeball`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `Guts`
- **Description**: Your line of sight restrictions are ignored.
- **Mechanics**:
```gon
passives {
        RemoveLineOfSightRestrictions 1
    }
```

### Golden Tooth (`GoldenTooth`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Becomes {aux} coins when you return home.
- **Mechanics**:
```gon
lck 4
    on_store become_aux_coins
    aux 125
```

### Water Bottle (`WaterBottle_Full`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Heal +5 HP and gain Heatwave immunity. Refills when affected by Water Element effects.
- **Mechanics**:
```gon
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
```

### Water Bottle (`WaterBottle_Half`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Heal +5 HP and gain Heatwave immunity. Refills when affected by Water Element effects.
- **Mechanics**:
```gon
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
```

### Empty Water Bottle (`WaterBottle_Empty`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: Throw it at something. Refills when affected by Water Element effects.
- **Mechanics**:
```gon
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
```

### Bloody Coin (`BloodyCoin`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Flip a coin. Heads: Refresh your basic attack. Tails: Lose 50% of your HP.
- **Mechanics**:
```gon
ability tk_BloodyCoin
```

### Glowing Coin (`GlowingCoin`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Flip a coin. Heads: Double your mana. Tails: Lose 50% of your mana.
- **Mechanics**:
```gon
ability tk_GlowingCoin
```

### Electric Coin (`ElectricCoin`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Flip a coin. Heads: Refresh your movement action. Tails: Gain Slow 2.
- **Mechanics**:
```gon
ability tk_ElectricCoin
```

### Counterfeit Coin (`CounterfeitCoin`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Flip a coin. Heads: Gain 5 coins. Tails: Lose 5 coins.
- **Mechanics**:
```gon
ability tk_CounterfeitCoin
```

### Whistle (`Whistle`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `[Druid, Hunter]`
- **Description**: Use: Summon a Fly, Maggot or Flea familiar. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_Whistle
```

### Metronome (`Metronome`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Jester`
- **Description**: Use: Cast a random upgraded spell. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_Metronome
```

### Tinker Tools (`TinkerTools`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Tinkerer`
- **Description**: Repair 1 use to your items at the end of each battle.
- **Mechanics**:
```gon
passives {
        StatusOnBattleEnd {
            RepairAll 1
        }
    }
```

### Ring of Frost (`RingOfFrost`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Mage, Frozen]`
- **Description**: Freezes tiles you walk over. +25% chance to inflict Freeze on units that contact or attack you. Your Ice Element damage is increased by 1.
- **Mechanics**:
```gon
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
```

### Lucky Coin Purse (`LuckyCoinPurse`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Thief, Lucky]`
- **Description**: Gain +2 [img:lck] each time you gain a coin.
- **Mechanics**:
```gon
passives {
        StatusOnGainCoins {
            LuckUp 2
        }
    }
```

### Rage Juice (`RageJuice`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Fighter`
- **Description**: Use: Gain +4 [img:str], +4 [img:spd], Brace 2 and Madness for the rest of the battle. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_RageJuice
```

### Prayer Card (`PrayerCard`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Cleric, Cardboard, Paper]`
- **Description**: 33% chance to gain +1 [img:divineshield] each time you take damage.
- **Mechanics**:
```gon
passives {
        StatusOnTookDamage {
            DivineShield [1, .33]
        }
    }
```

### Tank Toy (`TankToy`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Tank`
- **Description**: Trample.
- **Mechanics**:
```gon
shield 5
    passives {
        Trample 3
    }
```

### Bag of Seeds (`BagOfSeeds`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Druid`
- **Description**: Use: Spawn grass, flowers, or brambles on an adjacent tile.
- **Mechanics**:
```gon
ability tk_BagOfSeeds
```

### Libra (`Libra`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Space`
- **Description**: Balances all stats. This applies after all stat modifiers.
- **Mechanics**:
```gon
passives {
        BalanceStats 1
    }
```

### Ball of Bandages (`BallOfBandages`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Nurse`
- **Description**: Cleanse one stack of a random debuff at the end of each turn. +1 Health Regen.
- **Mechanics**:
```gon
passives {
        StatusEachTurnEnd {
            PartialCleanse 1
        }
        HealthRegenUp 1
    }
```

### [ITEM_ROSARY_NAME] (`Rosary`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: [ITEM_ROSARY_DESC]
- **Mechanics**:
```gon
passives {
    }
```

### [ITEM_WEATHERVANE_NAME] (`WeatherVane`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: [ITEM_WEATHERVANE_DESC]
- **Mechanics**:
```gon
passives {
    }
```

### Natural 20 (`Natural20`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Your weapons have +50% Crit Chance. Your basic attack has +10% Crit Chance.
- **Mechanics**:
```gon
passives {
        BoostWeaponDamage {
            damage 0
            crit_chance .5
        }
        BasicAttackCritChance .1
    }
```

### Technology (`Technology`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Cyborg, Bionic]`
- **Description**: Use: Shoot a laser beam. [s:.7](Usable once per battle.)[/s] Refreshes when affected by Electricity.
- **Mechanics**:
```gon
ability tk_Technology
    passives {
        RefreshEquipmentAbilityOnElement {
            element Electric
            text "COMBAT_POPUP_RECHARGED"
        }
    }
```

### Spring (`Spring`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Scrap`
- **Description**: Your movement action is Jump.
- **Mechanics**:
```gon
spd 2
    passives {
        ReplaceBasicMove BasicJump
    }
```

### Red Drink (`RedDrink`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Heal 5 HP. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_RedDrink
```

### Green Drink (`GreenDrink`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Gain 5 mana. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_GreenDrink
```

### Purple Drink (`PurpleDrink`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Heal 2 HP, gain 2 mana and +1 [img:shield]. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_PurpleDrink
```

### Lil' Battery (`LilBattery`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Refresh all items and spells with a once per battle restriction. Can be used on allies. [s:.7](Usable once per battle. Can't be refreshed.)[/s]
- **Mechanics**:
```gon
ability tk_LilBattery
```

### Carving Knife (`CarvingKnife`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Take 2 damage and spawn a Meat pickup.
- **Mechanics**:
```gon
ability tk_CarvingKnife
```

### Razor Blade (`RazorBlade`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Take 5 damage and gain +2 [img:str] and +2 [img:dex].
- **Mechanics**:
```gon
ability tk_RazorBlade
```

### Teleport! (`Teleport`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Experimental`
- **Description**: Use: Teleport to any open tile. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_Teleport
```

### Small Eye (`SmallEye`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Guts`
- **Description**: +15% Dodge Chance. Your basic attack has a +10% chance to inflict Fear.
- **Mechanics**:
```gon
passives {
        DodgeChance 15%
        AddStatusToBasicAttack {
            Fear [1 .1]
        }
    }
```

### Stickman (`Stickman`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Wood, Demonic]`
- **Description**: Gain All Stats Up when you deal damage to a party member.
- **Mechanics**:
```gon
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
```

### Cursed Stickman (`CursedStickman`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Wood, Demonic]`
- **Description**: Gain All Stats Up when you deal damage to a party member. 10% chance to gain Madness at the start of your turn.
- **Mechanics**:
```gon
cursed true
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
```

### Glowing Seed (`GlowingSeed`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Your basic attack spawns tall grass.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            ChangeTile TallGrassTile
        }
    }
```

### Magic Seed (`MagicSeed`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Your basic attack spawns brambles.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            ChangeTile BrambleTile
        }
    }
```

### Weird Egg (`WeirdEgg`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Baby`
- **Description**: 10% chance to spawn a controllable Fetus familiar at the end of each turn. It joins your party.
- **Mechanics**:
```gon
passives {
        StatusEachTurnEnd {
            Conditional_GoodRoll {
                odds 10%
                ForceUseAbility tk_WeirdEgg_Spawn
            }
        }
    }
```

### Spotted Mushroom (`SpottedMushroom`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `Druid`
- **Description**: 
- **Mechanics**:
```gon
str_aux_initialize random_seed
    passives {
        RandomSeededStatModifier [2 -1] // hard coded in SpawnDatabase::get_item_stats
    }
```

### Mundane Stone (`MundaneStone`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Rock`
- **Description**: Your basic attack's damage is increased by your lowest stat minus 2.
- **Mechanics**:
```gon
passives {
        StatDependentPassive {
            AddDamageToBasicAttack "min(min(min(min(min(min(str,dex),int),con),lck),spd),cha)-2"
        }
    }
```

### Empty Sack (`EmptySack`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[Leather, HumanFlesh]`
- **Description**: Spawn 3 pickups at the start of each battle. Find an extra common item at the end of each battle.
- **Mechanics**:
```gon
passives {
        StatusOnBattleStart {
            FindItemFromPool common
        }
        SpawnExtraThingsOnBattleStart {
            object RandomPickup
            number 3
        }
    }
```

### AAA Battery (`AAABattery`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Every time you cast 3 spells, gain +3 Charge.
- **Mechanics**:
```gon
passives {
        StatusEveryXSpellCasts {
            stacks 3
            Charge 3
        }
    }
```

### Tool Box (`ToolBox`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Tinkerer`
- **Description**: Your items lose Brittle and Fragile. Your weapons have a 25% chance to repair 1 use when used.
- **Mechanics**:
```gon
passives {
        SetBrittleImmune ""
        SetFragileImmune ""
        AddSelfStatusToWeapons {
            RepairWeapon [1 .25]
        }
    }
```

### Rubber Cement (`RubberCement`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Rubber, Slimy]`
- **Description**: Your projectiles bounce to another enemy within 2 tiles.
- **Mechanics**:
```gon
passives {
        BouncyProjectiles {
            max_bounces 1
            max_range 2
        }
    }
```

### Coin Purse (`CoinPurse`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Mother`
- **Description**: When you collect a coin pickup, gain +1 coin. Find an extra coin at the end of each battle.
- **Mechanics**:
```gon
passives {
        StatusOnPickupCoins {
            GainCoins 1
        }
        StatusOnBattleEnd {
            GainCoins 1
        }
    }
```

### Fork (`Fork`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Heal 5 HP when you kill a unit or destroy a corpse.
- **Mechanics**:
```gon
passives {
        StatusOnKill {
            HealthGain 5
        }
        StatusOnPopCorpse {
            HealthGain 5
        }
    }
```

### Cat o' Nine Tails (`CatONineTails`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Gimp`
- **Description**: Use: Take 1 damage and cleanse one random debuff.
- **Mechanics**:
```gon
ability tk_CatONineTails
```

### Glue (`Glue`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Slimy`
- **Description**: Use: Gain +20% Dodge Chance, -1 [img:int] and Confusion 2.
- **Mechanics**:
```gon
durability [5 8]
    ability tk_Glue
```

### My Shadow (`MyShadow`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Demonic`
- **Description**: Use: Move 3 tiles, leaving a shadow copy behind that mimics your basic attack. The shadow fades at the end of the turn.
- **Mechanics**:
```gon
durability 6
    ability tk_MyShadow
```

### Egg Sack (`EggSack`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Spawns Spiderlings in an area.
- **Mechanics**:
```gon
durability [4 6]
    ability tk_EggSack
```

### Gorgon's Eye (`GorgonsEye`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[Guts, Rock]`
- **Description**: Use: Petrify all nearby units in your line of sight.
- **Mechanics**:
```gon
durability [5 7]
    ability tk_GorgonsEye
```

### Hot Lunch (`HotLunch`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Paper`
- **Description**: Spawn a Flaming Meat pickup.
- **Mechanics**:
```gon
durability [5 8]
    ability tk_HotLunch
```

### Butter Bean (`ButterBean`)
- **Kind**: `trinket` | **Rarity**: `common` | **Set**: `None`
- **Description**: Use: Fart at an adjacent unit, knocking it back 1 tile.
- **Mechanics**:
```gon
ability tk_ButterBean
```

### Mom's Ring (`MomsRing`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Mother`
- **Description**: +1 Damage. Find a pill at the end of each battle.
- **Mechanics**:
```gon
passives {
        DamageUp 1
        StatusOnBattleEnd {
            FindItemFromPool pills
        }
    }
```

### Mind Stone (`MindStone`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Rock`
- **Description**: Your collarless spells cost -2 mana.
- **Mechanics**:
```gon
passives {
        ClassManaCostReduction {
            class Colorless
            reduction 2
        }
    }
```

### Skill Stone (`SkillStone`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Rock`
- **Description**: Spells that match your class cost -1 mana.
- **Mechanics**:
```gon
passives {
        ClassManaCostReduction {
            reduction 1
        }
    }
```

### Multiplier (`Multiplier`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: You can use your weapon an extra time each turn.
- **Mechanics**:
```gon
passives {
        ExtraWeaponAttacks 1
    }
```

### Sacred Heart (`SacredHeart`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Cleric`
- **Description**: +1 Damage. Emit 2 Sparkles when you use your basic attack.
- **Mechanics**:
```gon
passives {
        DamageUp 1
        AddSelfStatusToBasicAttack {
            RandomMagicMissile 2
        }
    }
```

### Fetus in a Jar (`FetusInAJar`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Baby`
- **Description**: At the the start of each battle, equip a temporary Bomb if your weapon slot is open. At the end of each turn, if you didn't use your basic attack, equip another Bomb.
- **Mechanics**:
```gon
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
```

### Breakfast (`Breakfast`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Cardboard`
- **Description**: +2 Health Regen.
- **Mechanics**:
```gon
passives {
        HealthRegenUp 2
    }
```

### Dream Catcher (`DreamCatcher`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Twine`
- **Description**: Whenever you fall asleep, gain All Stats Up, restore all your mana, and heal a random injury.
- **Mechanics**:
```gon
passives {
        StatusOnFallAsleep {
            AllStatsUp 1
            FillMana 1
			HealRandomInjury 1
        }
    }
```

### Enchanting Poop (`EnchantingPoop`)
- **Kind**: `trinket` | **Rarity**: `Unknown` | **Set**: `Fecal`
- **Description**: Spawn a poop at the start of each battle.
- **Mechanics**:
```gon
passives {
        SpawnOnBattleStart {
            object Poop
        }
    }
```

### EnchantingPoop_Cursed (`EnchantingPoop_Cursed`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of EnchantingPoop
    cursed true
```

### Lunch Box (`LunchBox`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Heal 5 HP. Whenever you collect a food pickup, instead of its normal effects, add +1 use to this item.
- **Mechanics**:
```gon
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
```

### Satanic Bible (`SatanicBible`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Demonic, Paper]`
- **Description**: Heal 3 HP and gain +3 Charge each time you damage a party member.
- **Mechanics**:
```gon
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
```

### Tiny Pebble (`TinyPebble`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: +10% Dodge Chance. Gain +2% Dodge Chance when you dodge an attack.
- **Mechanics**:
```gon
passives {
        DodgeChance_Status 10
        StatusOnDodge {
            DodgeChance_Status 2
        }
    }
```

### Scrap Bag (`ScrapBag`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[Scrap, Tinkerer]`
- **Description**: Craft a temporary weapon at the start of the battle if you don't have a weapon.
- **Mechanics**:
```gon
passives {
        StatusOnBattleStart {
            Craft {
                pool tinkerer_default
                slot weapon
            }
        }
    }
```

### Cookbook (`Cookbook`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[Butcher, Paper]`
- **Description**: When you kill a unit or destroy a corpse, it becomes meat.
- **Mechanics**:
```gon
passives {
        KillsToMeat Food
    }
```

### Tarot Deck (`TarotDeck`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[Psychic, Cardboard, Paper]`
- **Description**: Use: Conjure a random, single-use spell as a bonus ability.
- **Mechanics**:
```gon
ability tk_TarotDeck
    passives {
    }
```

### Tiny Cage (`TinyCage`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Druid`
- **Description**: Spawn a random animal familiar at the start of each battle.
- **Mechanics**:
```gon
passives {
        SpawnOnBattleStart {
            object RandomDruidFamiliar
            number 1
        }
    }
```

### Spell Book (`SpellBook`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Mage, Paper]`
- **Description**: Use: Gain 10 mana and conjure a random Mage spell as a bonus ability.
- **Mechanics**:
```gon
durability 2
    ability tk_SpellBook
    passives {
    }
```

### Bag o' Bags (`BagOfBags`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Throw a trash bag on an adjacent tile.
- **Mechanics**:
```gon
durability 13
    ability tk_BagOfBags
    passives {
    }
```

### Steroids (`Steroids`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Fighter`
- **Description**: Use: Gain +1 [img:str], permanently. For the rest of the adventure, you have a +2% chance to gain Madness at the start of each turn.
- **Mechanics**:
```gon
durability 9
    ability tk_Steroids
    passives {
    }
```

### Holy Water (`HolyWater`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Cleric`
- **Description**: Heal 2 HP in an area.
- **Mechanics**:
```gon
ability tk_HolyWater
    passives {
    }
```

### Tank Juice (`TankJuice`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Tank`
- **Description**: Use: Gain -1 [img:spd], then, for the rest of the turn, all damage you deal has Knockback 2 and Chain Knockback.
- **Mechanics**:
```gon
ability tk_TankJuice
    passives {
    }
```

### Hunter's Flute (`HuntersFlute`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Hunter`
- **Description**: Spawn 2-3 random familiars on adjacent tiles. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_HuntersFlute
    passives {
    }
```

### Friendship Bracelet (`FriendshipBracelet`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Druid`
- **Description**: Use: Permanently charm a non-boss enemy. It joins your party.
- **Mechanics**:
```gon
durability 3
    ability tk_FriendshipBracelet
    passives {
    }
```

### Cambion Conception (`CambionConception`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `[Necromancer, Demonic, Baby]`
- **Description**: Use: Summon a half-sized copy of yourself that has 66% of your stats and is AI controlled.
- **Mechanics**:
```gon
durability 2
    ability tk_CambionConception
    passives {
    }
```

### Empty Hand (`EmptyHand`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Monk`
- **Description**: Use: Gain +3 [img:shield] for each empty armor slot you have. When this breaks, gain +1 [img:con] permanently.
- **Mechanics**:
```gon
durability 4
    ability tk_EmptyHand
    passives {
        StatusOnBreak {
            ConstitutionUp 1
        }
    }
```

### Fireworks (`Fireworks`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Tinkerer`
- **Description**: Use: Emit 5 Sparkles. If you end your turn with 0 mana, this gains +1 use.
- **Mechanics**:
```gon
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
```

### Sack o' Meat (`SackOfMeat`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Butcher`
- **Description**: Use: Heal 4 HP. This gains +1 use each time you destroy a corpse.
- **Mechanics**:
```gon
durability 2
    ability tk_SackOfMeat
    passives {
	    ExtraTrinketUses 10
        StatusOnPopCorpse {
            RepairTrinket 1
        }
    }
```

### Druid's Whistle (`DruidsWhistle`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Druid`
- **Description**: Use: Spawn a random animal familiar on an adjacent tile. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_DruidsWhistle
    passives {
    }
```

### Ball of Yarn (`BallOfYarn`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Twine`
- **Description**: Spawn a Charmed Kitten with All Stats Up 2 at the start of each battle.
- **Mechanics**:
```gon
passives {
        SpawnOnBattleStart BuffCharmedKitten
    }
```

### Bird Head (`BirdHead`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Feathered`
- **Description**: Your basic attack inflicts Soul Link.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            SoulLink 1
        }
    }
```

### Broken Mirror (`BrokenMirror`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Used`
- **Description**: 
- **Mechanics**:
```gon
lck -99
    passives {
    }
```

### Binoculars (`Binoculars`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: +2 range.
- **Mechanics**:
```gon
passives {
        AddBonusRange 2
    }
```

### Bishop (`Bishop`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Move any number of tiles in a diagonal line.
- **Mechanics**:
```gon
durability 6
    ability tk_Bishop
```

### Golden Egg (`GoldenEgg`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Find 3-5 extra coins at the end of each battle.
- **Mechanics**:
```gon
passives {
        StatusOnBattleEnd {
            GainCoins [3 5]
        }
    }
```

### Bird Feed (`BirdFeed`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: +50% chance for an extra bird to spawn at the start of each battle.
- **Mechanics**:
```gon
passives {
        SpawnOnBattleStartRandomEmptyTile {
            object Bird
            number [0 1]
        }
    }
```

### Angel Wing (`AngelWing`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Feathered`
- **Description**: If an attack would down you, instead lower your HP to 1. While at 1 HP, this has no effect.
- **Mechanics**:
```gon
passives {
        PassiveAtHealthThreshold {
            threshold 1
            mode greater
            passives {
                DeathRattleRevive DoNothing
            }
        }
    }
```

### Soul Jar (`SoulJar`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: When your body is destroyed, this item is recovered and permanently gains the ability to summon a ghost copy of you.
- **Mechanics**:
```gon
passives {
        DropSoulJarOnDeath SoulJar_Full
    }
```

### Soul Jar (`SoulJar_Full`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Summon a ghost copy of {aux_cat_name}. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
aux -1
    aux_is_catid true
    ability tk_SoulJar
```

### Petrified Pinky (`PetrifiedPinky`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `[Rat, Rock]`
- **Description**: If an attack would down you, instead this breaks and you regain 50% of your max HP.
- **Mechanics**:
```gon
passives {
        DeathRattleRevive tk_PetrifiedPinky
    }
```

### Cat Rib (`CatRib`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Bone`
- **Description**: When your body is destroyed, you are reborn as a kitten!
- **Mechanics**:
```gon
passives {
        SpawnCatCloneOnCorpsePopped 1
    }
```

### Glowing Flask (`EstusFlask_Full`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Heal 5 HP. This refills at the end of each battle.
- **Mechanics**:
```gon
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
```

### Glowing Flask (`EstusFlask_Half`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Heal 5 HP. This refills at the end of each battle.
- **Mechanics**:
```gon
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
```

### Glowing Flask (`EstusFlask_Empty`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Heal 5 HP. This refills at the end of each battle.
- **Mechanics**:
```gon
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
```

### Lucky Coin (`LuckyCoin`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Lucky`
- **Description**: Coins that spawn at the start of each battle are doubled.
- **Mechanics**:
```gon
lck 2
    passives {
        MultiplyCoinsOnBattleStart 2
    }
```

### Heavy Rock (`HeavyRock`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Rock`
- **Description**: Rocks you knock back deal +5 damage and have Chain Knockback.
- **Mechanics**:
```gon
passives {
        AddStatusToAllDamage {
            Conditional_HasTag {
                tag rock
                BonusKnockbackDamage 5
                OverrideChainKnockback 0
            }
        }
    }
```

### Ipecac (`Ipecac`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Medical`
- **Description**: Your basic attack is Explosive Shot.
- **Mechanics**:
```gon
attack BasicExplosiveShot
    passives {
        OverrideBasicAttack BasicExplosiveShot
    }
```

### Meat Cube (`MeatCube`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Meat`
- **Description**: Start with a Flesh Lad familiar.
- **Mechanics**:
```gon
passives {
        SpawnOnBattleStart {
            object FamiliarFleshLad
        }
    }
```

### Soy Milk (`SoyMilk`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Your basic attack cannot deal more than 1 damage. You can attack 2 extra times each turn.
- **Mechanics**:
```gon
passives {
        CapBasicAttackDamage 1
        ExtraBasicAttacks 2
    }
```

### Spoon Bender (`SpoonBender`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Psychic`
- **Description**: Your basic attack can't miss and emits a Sparkle when used.
- **Mechanics**:
```gon
passives {
        BasicAttackCantMiss 1
        AddSelfStatusToBasicAttack {
            RandomMagicMissile 1
        }
    }
```

### Cancer (`Cancer`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Mother`
- **Description**: At the end of each battle, gain -1 to three random stats, then gain a mutation.
- **Mechanics**:
```gon
passives {
        StatusOnBattleEnd {
            even_if_dead true
            RandomPermanentStat -3
            RandomMutation 1
        }
    }
```

### Wafer (`Wafer`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Cleric`
- **Description**: 
- **Mechanics**:
```gon
divine_shield 2
    passives {
    }
```

### Large Meteor (`LargeMeteor`)
- **Kind**: `trinket` | **Rarity**: `uncommon` | **Set**: `Planet`
- **Description**: - {str_aux_passive_name} - {str_aux_passive_desc}
- **Mechanics**:
```gon
randomize_piece_frames true
    str_aux_initialize random_copyable_colorless_passive
    str_aux_is_copy_passive true
```

### Bloody Razor (`BloodyRazor`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Deal 5 damage to yourself to gain +3 Damage and +1 Magic Damage.
- **Mechanics**:
```gon
ability tk_BloodyRazor
```

### Immaculate Heart (`ImmaculateHeart`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: +2 Damage, +1 Magic Damage. Emit 3 Sparkles when you use your basic attack.
- **Mechanics**:
```gon
passives {
        DamageUp 2
		SpellDamageUp 1
        AddSelfStatusToBasicAttack {
            RandomMagicMissile 3
        }
    }
```

### Dybbuk's Rib (`DybbuksRib`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Bone`
- **Description**: Charm a random enemy at the start of each battle.
- **Mechanics**:
```gon
passives {
		StatusOnBattleStart {
			ForceUseAbility tk_DybbuksRib
		}
	}
```

### Snake Eyes (`SnakeEyes`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: While you are at exactly 2 HP, you have +222 [img:lck]
- **Mechanics**:
```gon
passives {
        PassiveAtHealthThreshold {
            threshold 2
            mode equal
            passives {
                LuckUp 222
            }
		}
    }
```

### Green Whistle (`GreenWhistle`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Summon a really big Leg. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability tk_LegWhistle
```

### Mother's Love (`MothersLove`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Mother`
- **Description**: +6 Health Regen.
- **Mechanics**:
```gon
shield 6
    lck 6
    passives {
		HealthRegenUp 6
    }
```

### Pentagram Sigil (`PentagramSigil`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Demonic`
- **Description**: Use: Take 5 damage and refresh your basic attack and movement actions.
- **Mechanics**:
```gon
cursed true
    durability 5
    ability tk_Pentagram
```

### Lucifer Sigil (`LuciferSigil`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Demonic`
- **Description**: Summon a Charmed Brute at the start of each battle.
- **Mechanics**:
```gon
cursed true
    passives {
        SpawnOnBattleStart {
            object CharmedBigDemon
            number 1
        }
    }
```

### Hexagram Sigil (`HexagramSigil`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Demonic`
- **Description**: +3 Magic Damage. You are immune to buffs and debuffs. When you die, you don't leave a corpse.
- **Mechanics**:
```gon
cursed true
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
```

### Chupacabra Tongue (`ChupacabraTongue`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Guts`
- **Description**: Your basic attack has Lifesteal.
- **Mechanics**:
```gon
passives {
		Lifesteal 1
    }
```

### Charon's Obol (`CharonsObal`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Necromancer`
- **Description**: +6 corpse health. Spawn a Charmed Reaper when you are downed.
- **Mechanics**:
```gon
passives {
		SpawnThingOnDeath CharmedReaper
		AddCorpseHealth 6
    }
```

### Human Head (`HumanHead`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `HumanFlesh`
- **Description**: 
- **Mechanics**:
```gon
str 1
	dex 1
	con 1
    int 1
	spd 1
	cha 1
	lck 1
```

### Glitch (`Glitch`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Scramble the last spell you used. Permanently.
- **Mechanics**:
```gon
ability tk_Glitch
```

### Video Game Cart (`VideoGameCart`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Used`
- **Description**: It's broken.
- **Mechanics**:
```gon
passives {
    }
```

### TV (`TV`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Your bonus ability is Waste Time.
- **Mechanics**:
```gon
passives {
		BonusAbility WasteTime
    }
```

### Triachnid (`Triachnid`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Spawn Triachnid at the start of each battle.
- **Mechanics**:
```gon
passives {
        SpawnOnBattleStart {
            object Triachnid
            number 1
        }
    }
```

### Gallon of Water (`GallonOfWater`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Heal +5 HP and gain Heatwave immunity. Refills when affected by Water Element effects.
- **Mechanics**:
```gon
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
```

### Scorched Earth (`ScorchedEarth`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `DirtClod`
- **Description**: Your Earth and Fire Element spells cost -1 mana.
- **Mechanics**:
```gon
passives {
        ElementalManaCostReduction {
            element [Fire Earth]
            reduction 1
        }
    }
```

### Liquid Metal (`LiquidMetal`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: +25% Dodge Chance.
- **Mechanics**:
```gon
passives {
		DodgeChance 25%
    }
```

### Steven Stone (`StevenStone`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Your collarless spells cost -2 mana.
- **Mechanics**:
```gon
cha 2
    passives {
        ClassManaCostReduction {
			class Colorless
            reduction 2
        }
    }
```

### Steven Marrow (`StevenMarrow`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Any [img:shield] you gain is increased by 4.
- **Mechanics**:
```gon
shield 4
	con -3
	passives {
		GainExtraShield 4
	}
```

### Steven (`StevenTrinket1`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Your basic attack inflicts Slow and has a +10% chance to Freeze. You can damage frozen units.
- **Mechanics**:
```gon
passives {
		FreezePiercing 1
        AddStatusToBasicAttack {
            Slow 1
			Freeze [1 .1]
        }
    }
```

### Steven (`StevenTrinket2`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Your basic attack inflicts Confusion.
- **Mechanics**:
```gon
passives {
        AddStatusToBasicAttack {
            Confusion 1
        }
    }
```

### Ninny Stick (`NinnyStick`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Jester`
- **Description**: Reroll your other equipped items at the end of each battle. You can reroll your options when you level up.
- **Mechanics**:
```gon
passives {
        RerollItemsOnBattleEnd 1
        AddLevelUpRerolls 1
    }
```

### Skill Split (`SkillSplit`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Gain a temporary copy of your first passive ability at the start of each battle.
- **Mechanics**:
```gon
passives {
        CopyPassiveSlot 0
    }
```

### Furniture Box (`FurnitureBox`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Breaks when [img:shield] is depleted. Becomes a random piece of furniture when you return home.
- **Mechanics**:
```gon
on_store become_furniture
    spd -5
    shield 8
    passives {
        BreakWhenNoShield 1
    }
```

### Rare Furniture Box (`FurnitureBox_Rare`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Breaks when [img:shield] is depleted. Becomes a random piece of rare furniture when you return home.
- **Mechanics**:
```gon
on_store become_rare_furniture
    spd -5
    lck 5
    shield 4
    passives {
        BreakWhenNoShield 1
    }
```

### Ankh (`Ankh`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: While you're downed, you have a 50% chance to revive with 33% HP at the end of each round.
- **Mechanics**:
```gon
passives {
        ChanceToRevive {
            stacks 50
            health 34%
        }
    }
```

### The Box (`TheBoxCardboard`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Cardboard`
- **Description**: Find an extra chapter item at the end of each battle.
- **Mechanics**:
```gon
passives {
	    StatusOnBattleEnd {
            FindItemFromPool chapter_specific_item
        }
    }
```

### The bOx (`TheBoxChest`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Wood`
- **Description**: Use: Spawn A lost Spirit. This gains +1 use whenever an allied cat dies. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
durability 1
    max_durability 4
    dont_destroy_on_0 true
    passives {
        StatusOnAllyCatDeath {
            RepairTrinket 1
        }
    }
	ability tk_SpawnTheLost
```

### The boX (`TheBox`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Steven`
- **Description**: Use: Revive all bodies, fully heal all units, and clear all status effects. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
durability 4
	ability tk_Reset
```

### the box (`TheBlackBox`)
- **Kind**: `trinket` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Use: Find and equip a random item into one of your empty item slots.
- **Mechanics**:
```gon
ability tk_TheBlackBox
```

### Skull Of Glorg (`SkullOfGlorg`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `Bone`
- **Description**: Your spells cost -1 mana for each parasite you have equipped.
- **Mechanics**:
```gon
parasite true
    passives {
		ReduceSpellCostsPerParasite 1
    }
```

### [C] (`Checkers`)
- **Kind**: `trinket` | **Rarity**: `rare` | **Set**: `None`
- **Description**: [U]

## Category: `weapons.gon`

### Shard of Glass (`GlassShard`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Bleed.
- **Mechanics**:
```gon
durability [7, 12]
    ability wp_GlassShard
```

### TinkererGlassShard (`TinkererGlassShard`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of GlassShard
    durability [4 9]
```

### Railroad Spikes (`RailSpikes`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Lead`
- **Description**: Use: A ranged attack.
- **Mechanics**:
```gon
durability 8
    ability wp_RailSpikes
```

### Nail Board (`NailBoard`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Wood`
- **Description**: Use: A wide melee attack.
- **Mechanics**:
```gon
durability 4
    ability wp_NailBoard
```

### Lil' Slugger (`LilSlugger`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Wood`
- **Description**: Use: Knock back a unit 5 tiles.
- **Mechanics**:
```gon
ability wp_LilSlugger
```

### Chum Bucket (`ChumBucket`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `[Guts, Meat]`
- **Description**: Use: A lobbed attack that creates a creep puddle.
- **Mechanics**:
```gon
durability 6
    ability wp_ChumBucket
```

### Meat Hook (`MeatHook`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `[Barbed, Butcher]`
- **Description**: Use: Pull a unit toward you.
- **Mechanics**:
```gon
ability wp_MeatHook
```

### Kebab (`Kebab`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A melee attack with +1 reach that penetrates through units.
- **Mechanics**:
```gon
durability 8
    ability wp_Kebab
```

### Pipe (`Pipe`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Lead`
- **Description**: Use: A melee attack with a 10% chance to inflict Stun.
- **Mechanics**:
```gon
ability wp_Pipe
```

### Obsidian Chunk (`ObsidianChunk`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Obelisk`
- **Description**: Use: A melee attack. This weapon gains +2 damage each time it's used. Damage resets at the end of the adventure.
- **Mechanics**:
```gon
durability 9
    aux 1
    reset_aux_on_store 1
    ability wp_ObsidianChunk
```

### Soul Claw (`SoulClaw`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Demonic`
- **Description**: Use: A melee attack that deals damage equal to the number of uses this has left. When this weapon kills a unit, it gains +2 uses.
- **Mechanics**:
```gon
durability 7
    ability wp_SoulClaw
```

### Bomb (`Bomb`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Throw a bomb that explodes.
- **Mechanics**:
```gon
durability 1
    ability wp_Bomb
```

### Bone Club (`BoneClub`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Bone`
- **Description**: Use: A melee attack. This weapon has a 15% chance to break each time it's used.
- **Mechanics**:
```gon
ability wp_BoneClub
```

### Molars (`Molars`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Bone`
- **Description**: Use: A low-damage lobbed attack.
- **Mechanics**:
```gon
durability [10 20]
    ability wp_Molars
```

### Whetstone (`Whetstone`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Rock`
- **Description**: Use: Gain +1 Damage for the rest of the battle.
- **Mechanics**:
```gon
ability wp_Whetstone
```

### Modded Hairspray (`Hairspray`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Deal fire damage in a cone.
- **Mechanics**:
```gon
durability [8 12]
    ability wp_HairSpray
```

### Lighter (`Lighter`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Cool`
- **Description**: Use: Inflict Burn 1 on an adjacent unit.
- **Mechanics**:
```gon
durability [8 12]
    ability wp_Lighter
```

### Seed Bombs (`SeedBombs`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A lobbed projectile that spawns tall grass.
- **Mechanics**:
```gon
ability wp_SeedBomb
```

### Battery (`Battery`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A ranged lightning attack with a 10% chance to Stun.
- **Mechanics**:
```gon
durability [3 6]
    ability wp_Battery
```

### TinkererBattery (`TinkererBattery`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of Battery
    durability [2 3]
```

### Old Hose (`OldHose`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Rubber`
- **Description**: Use: A water attack that hits an entire line with Knockback 1.
- **Mechanics**:
```gon
ability wp_Hose
```

### Six Pack (`SixPack`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A lobbed water attack that deals splash damage.
- **Mechanics**:
```gon
durability 6
    ability wp_SixPack
```

### Ice Cubes (`IceCubes`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Frozen`
- **Description**: Use: A lobbed attack that Freezes units. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_IceCubes
```

### Dry Ice (`DryIce`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Frozen`
- **Description**: Use: An Ice Element melee attack that inflicts Slow.
- **Mechanics**:
```gon
ability wp_DryIce
```

### Bottles (`Bottles`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `None`
- **Description**: Use: A lobbed attack that spawns a glass tile.
- **Mechanics**:
```gon
durability 6
    ability wp_Bottles
```

### TinkererBottles (`TinkererBottles`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of Bottles
    durability 4
```

### Stick (`Stick`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Wood`
- **Description**: Use: A melee attack with +1 reach.
- **Mechanics**:
```gon
durability 4
    ability wp_Stick
```

### TinkererStick (`TinkererStick`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of Stick
    durability [2 4]
```

### TutorialStick (`TutorialStick`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of Stick
    durability 4
```

### Rubber Fist (`RubberFist`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Rubber`
- **Description**: Use: A melee attack with Knockback 1 that inflicts Confusion.
- **Mechanics**:
```gon
ability wp_RubberFist
```

### Barbed Paw (`BarbedPaw`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Barbed`
- **Description**: Use: A melee attack that inflicts Bleed 1. Passive: +1 Thorns.
- **Mechanics**:
```gon
con -1
    passives {
        Thorns 1
    }
    ability wp_BarbedPaw
```

### Gnarled Claw (`GnarledClaw`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: A melee attack. This weapon gains +1 damage and +1 use when it gets a kill. Damage resets at the end of the adventure.
- **Mechanics**:
```gon
aux 1
    durability 13
    reset_aux_on_store 1
    ability wp_GnarledClaw
```

### Garbage (`Garbage`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `Recycled`
- **Description**: Use: A lobbed attack that inflicts Poison 1.
- **Mechanics**:
```gon
durability 1
    ability wp_Garbage
```

### Shotgun (`Shotgun`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Fires 5 projectiles in a cone.
- **Mechanics**:
```gon
durability 2
    ability wp_Shotgun
```

### Revolver (`Revolver`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Fire a shot in a straight line that instakills units and deals 25 damage to bosses.
- **Mechanics**:
```gon
durability 6
    ability wp_Revolver
```

### Sniper Rifle (`Sniper`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Fire a shot that instakills units and deals 25 damage to bosses.
- **Mechanics**:
```gon
durability [2 4]
    ability wp_Sniper
```

### Small Bomb (`SmallBomb`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `None`
- **Description**: Use: Throw a bomb that explodes.
- **Mechanics**:
```gon
durability 1
    ability wp_SmallBomb
```

### Pogo Stick (`PogoStick`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Jump to a tile and damage units you land on.
- **Mechanics**:
```gon
durability [3 7]
    ability wp_PogoStick
```

### Spitball (`Spitball`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A ranged attack that inflicts Slow.
- **Mechanics**:
```gon
durability [4 8]
    ability wp_Spitball
```

### Mini Jetpack (`MiniJetpack`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Experimental`
- **Description**: Use: Fly to a random tile within a target area. If you land on a unit, explode dealing 5 damage in an area (including to yourself).
- **Mechanics**:
```gon
durability [3 6]
    ability wp_MiniJetpack
```

### Big Stick (`BigStick`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Wood`
- **Description**: Use: A melee attack with +2 reach.
- **Mechanics**:
```gon
durability [8 12]
    ability wp_BigStick
```

### TinkererBigStick (`TinkererBigStick`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of BigStick
    durability [5 8]
```

### Biggest Stick (`BiggestStick`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Wood`
- **Description**: Use: A melee attack with +3 reach.
- **Mechanics**:
```gon
durability [8 12]
    ability wp_BiggestStick
```

### TinkererBiggestStick (`TinkererBiggestStick`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of BiggestStick
    durability [5 8]
```

### Log (`Log`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Wood`
- **Description**: Use: A wide attack that hits all units in an area.
- **Mechanics**:
```gon
durability 8
    ability wp_Log
```

### TinkererLog (`TinkererLog`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of Log
    durability 4
```

### Zapper (`Taser`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: A ranged electric attack that inflicts Stun.
- **Mechanics**:
```gon
durability 4
    ability wp_Taser
```

### TinkererTaser (`TinkererTaser`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of Taser
    durability 3
```

### Deathbot (`Deathbot`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Tinkerer`
- **Description**: Use: Spawn a Deathbot with a flamethrower.
- **Mechanics**:
```gon
durability 1
    ability wp_Deathbot
```

### Crossbow (`Crossbow`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Wood`
- **Description**: Use: A ranged attack that ignores shield and inflicts Bleed 1.
- **Mechanics**:
```gon
durability 6
    ability wp_Crossbow
```

### TinkererCrossbow (`TinkererCrossbow`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of Crossbow
    durability 4
```

### Vial of Acid (`BucketOfAcid`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts random status effects.
- **Mechanics**:
```gon
durability 1
    ability wp_BucketOfAcid
```

### Stun Gun (`StunGun`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: An electric melee attack with a 50% chance to inflict Stun.
- **Mechanics**:
```gon
durability [2 4]
    ability wp_StunGun
```

### Slingshot (`SlingShot`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Wood`
- **Description**: Use: A ranged attack with a 33% chance to inflict Blind 2.
- **Mechanics**:
```gon
durability [5 9]
    ability wp_SlingShot
```

### TinkererSlingShot (`TinkererSlingShot`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: No description.
- **Mechanics**:
```gon
variant_of SlingShot
    durability [4 7]
```

### Submachine Gun (`Uzi`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Fire 5 shots in a straight line.
- **Mechanics**:
```gon
durability 3
    ability wp_Uzi
```

### .22 Rifle (`22Rifle`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Fire a shot anywhere within your line of sight.
- **Mechanics**:
```gon
durability [2 4]
    ability wp_22Rifle
```

### Bag of Rocks (`BagOfRocks`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Rock`
- **Description**: Use: A melee attack that inflicts Bruise.
- **Mechanics**:
```gon
ability wp_BagOfRocks
```

### Textbook (`Textbook`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Paper`
- **Description**: Use: Gain +1 [img:int] for the rest of the battle.
- **Mechanics**:
```gon
ability wp_Textbook
```

### Bucket of Lard (`BucketOfLard`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Fatty`
- **Description**: Use: Gain +2 [img:con] and -1 [img:spd], then heal 4 HP.
- **Mechanics**:
```gon
durability [4 7]
    ability wp_BucketOfLard
```

### Nail Gun (`NailGun`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Fire a shot in a straight line that inflicts +1 Thorns.
- **Mechanics**:
```gon
ability wp_NailGun
```

### Strong Magnet (`StrongMagnet`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Pull a unit 2 tiles toward you.
- **Mechanics**:
```gon
ability wp_StrongMagnet
```

### Sawblades (`SawBlades`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Throw a blade in a straight line that inflicts Bleed 1 and passes through units.
- **Mechanics**:
```gon
durability [9 16]
    ability wp_SawBlades
```

### Odd Remote (`OddRemote`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Experimental`
- **Description**: Use: Cast a random spell.
- **Mechanics**:
```gon
durability [6 8]
    ability wp_OddRemote
```

### Butterfly Knife (`ButterflyKnife`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Cool`
- **Description**: Use: A multi-hit melee attack that inflicts Bleed. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_ButterflyKnife
```

### Bear Traps (`BearTraps`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `[Hunter, Survivalist]`
- **Description**: Use: Place a Bear Trap.
- **Mechanics**:
```gon
durability 6
    ability wp_BearTraps
```

### Rusty Razor (`RustyRazor`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Poison 1 and Bleed 1.
- **Mechanics**:
```gon
durability [6 9]
    ability wp_RustyRazor
```

### Bricks (`Bricks`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Brick`
- **Description**: Use: A lobbed attack that inflicts Stun. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_Bricks
```

### Mjolnir (`Mjolnir`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Superhero`
- **Description**: Use: A ranged attack that passes through units and returns to you after you throw it. At its apex, it deals electric damage. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_Mjolnir
```

### Blackjack (`Blackjack`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `[Thief, Prowler]`
- **Description**: Use: A melee attack with a 5% chance to Stun. Automatically use this when you stop next to an enemy or an enemy stops next to you.
- **Mechanics**:
```gon
ability wp_Blackjack
    passives {
        MovementReaction {
            ability wp_Blackjack_Auto
            enemies_only true
            on_self_move_too true
            create_temp_ability true
        }
    }
```

### Big Spring (`BigSpring`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Scrap`
- **Description**: Use: Throw an adjacent unit to a tile.
- **Mechanics**:
```gon
ability wp_BigSpring
```

### Grenade (`Grenade`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Throw a grenade that explodes and shreds 5 stacks of random buffs off of whatever it hits.
- **Mechanics**:
```gon
durability 1
    ability wp_Grenade
```

### Pinwheel (`Pinwheel`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Paper`
- **Description**: Use: A melee wind attack with Knockback 1. Can be used 3 times per turn.
- **Mechanics**:
```gon
durability [10 16]
    ability wp_Pinwheel
    passives {
        ExtraWeaponAttacks 2
    }
```

### Crisp Paper (`CrispPaper`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Paper`
- **Description**: Use: A ranged attack that inflicts Bleed 3. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_CrispPaper
```

### Purple Mushroom (`PurpleMushroom`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Druid`
- **Description**: Use: A ranged attack that inflicts Confusion 2. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
durability [2 4]
    ability wp_PurpleMushroom
```

### Black Mushroom (`BlackMushroom`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Druid`
- **Description**: Use: A ranged attack that inflicts Weakness 2. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_BlackMushroom
```

### Red Mushroom (`RedMushroom`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Druid`
- **Description**: Use: A ranged attack that inflicts Charm 3. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_RedMushroom
```

### Les Toxin (`PoisonVial`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Thief`
- **Description**: Use: A ranged attack that inflicts Poison 2. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_PoisonVial
```

### Pop Cap (`PopCap`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `None`
- **Description**: Use: A lobbed attack with Knockback 1.
- **Mechanics**:
```gon
durability [6 10]
    ability wp_PopCap
```

### Creepy Photo (`CreepyPhoto`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Fear 1. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_CreepyPhoto
```

### Finger Bone (`FingerBone`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Bone`
- **Description**: Use: A straight ranged attack that inflicts Immobile 3. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_FingerBone
```

### Spring Board (`SpringBoard`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Wood`
- **Description**: Use: A melee attack that lobs a unit back 3 tiles.
- **Mechanics**:
```gon
ability wp_SpringBoard
```

### Shovel (`Shovel`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: A melee attack that lobs a unit back 2 tiles and digs up a corpse.
- **Mechanics**:
```gon
ability wp_Shovel
```

### Trowel (`Trowel`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `None`
- **Description**: Use: A melee attack with Knockback 1 that spawns a rock.
- **Mechanics**:
```gon
durability [6 8]
    ability wp_Trowel
```

### Staff of Flame (`StaffOfFlame`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Mage`
- **Description**: Use: A fire attack that inflicts Burn 5. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_StaffOfFlame
```

### Laced Needle (`LacedNeedle`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Thief`
- **Description**: Use: A melee attack that inflicts Poison 1. Can be used 3 times per turn.
- **Mechanics**:
```gon
durability [10 14]
    ability wp_LacedNeedle
    passives {
        ExtraWeaponAttacks 2
    }
```

### Battle Axe (`BattleAxe`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Fighter`
- **Description**: Use: A melee spin attack. This uses up both your movement and attack action.
- **Mechanics**:
```gon
ability wp_BattleAxe
```

### Anointing Oil (`AnointingOil`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Cleric`
- **Description**: Use: Cleanse debuffs from an adjacent unit or yourself. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_AnointingOil
```

### Girder (`Girder`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Tank`
- **Description**: Use: A melee attack with Knockback 10 and Chain Knockback. [s:.7](Usable once per battle.)[/s] Passive: +1 Brace while this weapon is usable.
- **Mechanics**:
```gon
ability wp_Girder
    passives {
        PassiveIfWeaponIsUsable {
            Brace 1
        }
    }
```

### Arrow of Infinity (`InfinityArrow`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Hunter`
- **Description**: Use: Your next basic attack has +5 range, +100% Crit Chance, ignores shield and can't miss. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_InfinityArrow
    passives {
    }
```

### Bent Spoon (`BentSpoon`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Psychic`
- **Description**: Use: Pull any unit 1 tile toward you and deal 1 damage to it.
- **Mechanics**:
```gon
ability wp_BentSpoon
    passives {
    }
```

### Staff of the Underworld (`UnderworldStaff`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `[Necromancer, Bone]`
- **Description**: Use: A melee attack with Knockback 1. Passive: Start each battle with a Zombie Cat familiar.
- **Mechanics**:
```gon
ability wp_UnderworldStaff
    passives {
        SpawnOnBattleStart ZombieCatFamiliar
    }
```

### Bo (`Bo`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `[Monk, Wood]`
- **Description**: Use: A melee attack. On hit, jump forward 2 tiles.
- **Mechanics**:
```gon
ability wp_Bo
    passives {
    }
```

### Ball-Peen Hammer (`BallPeenHammer`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Tinkerer`
- **Description**: Use: A melee attack. If used on an ally, give +1 use to all of their items instead of dealing damage. 5% chance to break when used to repair items.
- **Mechanics**:
```gon
ability wp_BallPeenHammer
    passives {
    }
```

### Butcher's Cleaver (`ButchersCleaver`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Butcher`
- **Description**: Use: A melee attack with Cleave that can hit diagonally.
- **Mechanics**:
```gon
ability wp_ButchersCleaver
    passives {
    }
```

### Rain Staff (`RainStaff`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `[Druid, Wood]`
- **Description**: Use: Spawn a large puddle of water anywhere.
- **Mechanics**:
```gon
ability wp_RainStaff
    passives {
    }
```

### Lil' Kitty (`LilKitty`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Spawn a Flea familiar.
- **Mechanics**:
```gon
ability wp_LilKitty
    passives {
    }
```

### Tractor Beam (`TractorBeam`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Space`
- **Description**: Use: Pull a unit within 3 tiles all the way towards you. Requires line of sight.
- **Mechanics**:
```gon
ability wp_TractorBeam
```

### Roll of Pennies (`RollOfPennies`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A weak melee attack that has a 50% chance to spawn a coin.  5% chance to break when used. Gain a lot of coins when it breaks.
- **Mechanics**:
```gon
ability wp_RollOfPennies
    passives {
        StatusOnBreak {
            GainCoinsRange {
                min 30
                max 60
            }
        }
    }
```

### Grappling Hook (`GrapplingHook`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `[Barbed, Ninja]`
- **Description**: Use: Pull yourself toward a unit or object.
- **Mechanics**:
```gon
ability wp_GrapplingHook
```

### Chainsaw (`Chainsaw`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Cool`
- **Description**: Use: A multi-hit melee attack with a 25% chance to Cleave. [s:.7](Usable once per battle.)[/s] Passive: +2 Thorns.
- **Mechanics**:
```gon
equip_sound SE_CatWeaponPoke_Chainsaw
    ability wp_Chainsaw
    passives {
        Thorns 2
    }
```

### Burning Coals (`BurningCoal`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Molten`
- **Description**: Use: A lobbed attack that inflicts Burn 2 and +2 [img:spd]. Passive: Gain Burn 1 and +2 [img:spd] at the start of each turn.
- **Mechanics**:
```gon
ability wp_BurningCoal
    passives {
        StatusEachTurnBegin {
            Burn 1
			SpeedUp 2
        }
    }
```

### Rainbow Remote (`RainbowRemote`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Experimental`
- **Description**: Use: Cast a targeted random spell. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_RainbowRemote
```

### Rubber Bat (`RubberBat`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Rubber`
- **Description**: Use: A melee attack that inflicts Confusion 1 and turns the unit to the right.
- **Mechanics**:
```gon
ability wp_RubberBat
```

### Rusted Rod (`RustedRod`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A melee attack with damage equal to uses.
- **Mechanics**:
```gon
durability 9
    ability wp_RustedRod
```

### Meat Cleaver (`MeatCleaver`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Butcher`
- **Description**: Use: A melee attack with Cleave that deals damage equal to half the target's current HP. Bosses take 1/6th of their current HP in damage instead. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_MeatCleaver
```

### Sharp Straw (`SharpStraw`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A weak melee attack. If it kills a unit, heal 10 HP.
- **Mechanics**:
```gon
ability wp_SharpStraw
```

### Bag o' Glass (`BagOfGlass`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Spawn Glass on an adjacent tile. 5% chance to break when used.
- **Mechanics**:
```gon
ability wp_BagOfGlass
```

### Bag o' Meat (`BagOfMeat`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Meat`
- **Description**: Use: Spawn Meat on an adjacent tile. 5% chance to break when used.
- **Mechanics**:
```gon
ability wp_BagOfMeat
```

### Bag o' Glitter (`BagOfGlitter`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Stunning`
- **Description**: Use: Inflict Blind 2 on an adjacent unit. 5% chance to break when used.
- **Mechanics**:
```gon
ability wp_BagOfGlitter
```

### Bag o' Stuff (`BagOfStuff`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `None`
- **Description**: Use: Spawn a random pickup on an adjacent tile. 5% chance to break when used.
- **Mechanics**:
```gon
ability wp_BagOfStuff
```

### Pickaxe (`Pickaxe`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Miner`
- **Description**: Use: A melee attack that ignores shield. If used on static or inanimate objects it destroys them and spawns a Rock. Restore 1 use when used this way.
- **Mechanics**:
```gon
ability wp_Pickaxe
```

### Rocket Launcher (`RocketLauncher`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Fire a rocket anywhere that explodes.
- **Mechanics**:
```gon
durability 5
    ability wp_RocketLauncher
```

### Frayed Wires (`FreyedWires`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: An electric melee attack that can chain through adjacent units. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_FreyedWires
```

### Old Extinguisher (`OldExtinguisher`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Extinguishes fires in a cone with Knockback 5. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_OldExtinguisher
```

### Trash Can Lid (`TrashCanLid`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A melee attack with Knockback 1.
- **Mechanics**:
```gon
shield 5
    ability wp_TrashCanLid
```

### Mini Nuke (`MiniNuke`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Radioactive`
- **Description**: Use: Throw a mini nuke that makes a HUGE explosion that spawns toxic sludge.
- **Mechanics**:
```gon
durability 1
    ability wp_MiniNuke
```

### The Kandarian (`Kandarian`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `[Demonic, Bone]`
- **Description**: Use: A melee attack that always crits and inflicts Bleed 10.
- **Mechanics**:
```gon
durability 1
    ability wp_Kandarian
```

### Geode (`Geode`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `[Rock, Gemstone]`
- **Description**: Use: A melee attack with a 5% chance to break when used. When it breaks, gain 15-30 coins.
- **Mechanics**:
```gon
ability wp_Geode
    passives {
        StatusOnBreak {
            GainCoinsRange {
                min 15
                max 30
            }
        }
    }
```

### Rocks (`Rocks`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `Rock`
- **Description**: Use: A lobbed attack.
- **Mechanics**:
```gon
durability 8
    ability wp_Rocks
```

### Extra Limb (`ExtraLimb`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Hybrid`
- **Description**: Use: An attack that copies your basic attack.
- **Mechanics**:
```gon
durability 6
    ability wp_ExtraLimb
```

### Grip Trainer (`GripTrainer`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Fighter`
- **Description**: Use: Gain +1 [img:str].
- **Mechanics**:
```gon
ability wp_GripTrainer
```

### Shoe Horn (`ShoeHorn`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Gain +2 [img:spd].
- **Mechanics**:
```gon
ability wp_ShoeHorn
```

### Cheese (`Cheese`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Gain +1 [img:con] and heal 2 HP.
- **Mechanics**:
```gon
ability wp_Cheese
```

### Lip Filler (`LipFiller`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Gain +1 [img:cha] and 2 mana.
- **Mechanics**:
```gon
ability wp_LipFiller
```

### Energy Drink (`EnergyDrink`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Gain +1 [img:dex] and +1 [img:spd].
- **Mechanics**:
```gon
ability wp_EnergyDrink
```

### Cat Paw (`CatPaw`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Hybrid`
- **Description**: Use: A melee attack that has a 25% chance to refresh itself when used.
- **Mechanics**:
```gon
lck 2
    ability wp_CatPaw
```

### Flower Mix (`FlowerMix`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Flower`
- **Description**: Use: Plant flowers in a large area.  [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_FlowerMix
```

### Puzzle Box (`PuzzleBox`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `[Gimp, Demonic]`
- **Description**: Use: Shoot hooks in 8 directions that inflict Bleed 1 and pull units towards you. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_PuzzleBox
```

### Crowbar (`Crowbar`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: A melee attack that destroys trash bags and crates, scattering extra pickups.
- **Mechanics**:
```gon
ability wp_Crowbar
    passives {
        AddAdvantageToEvent { //TODO: this doesn't actually do anything yet
            type treasure_box
            options [smash bash open]
            add 5
        }
    }
```

### Fire Flower (`FireFlower`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Flower`
- **Description**: Use: Shoot a fireball that inflicts Burn 2 in an area. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_FireFlower
```

### The Bible (`Bible`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Cleric`
- **Description**: Use: Cleanse one stack of a random debuff from a unit at melee range.  Passive: Your heals heal for 1 extra.
- **Mechanics**:
```gon
ability wp_Bible
    passives {
        BoostHeals 1
    }
```

### Car Battery (`CarBattery`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: An electric melee attack that has a 50% chance to chain to another enemy within 3 tiles. Can only be used while at full mana.
- **Mechanics**:
```gon
ability wp_CarBattery
```

### Modeling Clay (`ModelingClay`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `DirtClod`
- **Description**: {str_aux_item_desc} [s:.7](This changes into a different weapon each time it's used.)[/s]
- **Mechanics**:
```gon
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
```

### Modeling Clay (`ModelingClay_Default`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A lobbed attack.
- **Mechanics**:
```gon
ability wp_ModelingClay
```

### Pharaoh's Staff (`PharaohStaff`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Summon a swarm of charmed flies. When you destroy a corpse, restore this weapon's use.
- **Mechanics**:
```gon
durability 1
    max_durability 1
    dont_destroy_on_0 true
    ability wp_PharaohStaff
    passives {
        StatusOnPopCorpse {
            RepairWeapon 1
        }
    }
```

### Slag Might (`SlagMight`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Rock`
- **Description**: Use: A melee attack with Bruise 1 and Knockback 5. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_SlagMight
```

### Mom's Toenail (`MomsToeNail`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `Mother`
- **Description**: Use: A melee attack.
- **Mechanics**:
```gon
ability wp_MomsToeNail
```

### Alien Blaster (`AlienBlaster`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `Space`
- **Description**: Use: A laser attack. Gains +1 damage for the rest of the battle each time it's used.
- **Mechanics**:
```gon
ability wp_AlienBlaster
```

### Polymorph Remote (`PolymorphRemote`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Transform a non-boss enemy into another random enemy from the same chapter. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_PolymorphRemote
```

### Melon Baller (`MelonBaller`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Blind 3 and gives you a random eye trinket if you don't have a trinket equipped.
- **Mechanics**:
```gon
durability [4, 6]
    ability wp_MelonBaller
```

### Ether Soaked Rag (`EtherSoakedRag`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Rag`
- **Description**: Use: Put an adjacent unit or yourself to sleep. That unit gets +5 Health Regen and +5 Mana Regen until it wakes up. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_EtherSoakedRag
```

### Death's Scythe (`DeathsScythe`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: A spin attack. After using this, die at the end of your turn.
- **Mechanics**:
```gon
ability wp_DeathsScythe
```

### Necronomicon (`Necronomicon`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `[Necromancer, Demonic]`
- **Description**: Use: Unearth 5 zombies. These zombies have a 33% chance of having Madness. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_Necronomicon
```

### Jitte (`Jitte`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Ninja`
- **Description**: Use: A melee attack that deals damage equal to half your [img:str] rounded up, inflicts Weakness 1, and gives you +1 [img:str] and +1 HP on hit.
- **Mechanics**:
```gon
ability wp_Jitte
```

### Anarchist Cookbook (`AnarchistCookbook`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `Paper`
- **Description**: Use: Summon 3-5 grenades that explode at the end of the round or when destroyed.
- **Mechanics**:
```gon
ability wp_AnarchistCookbook
```

### Mom's Knife (`MomsKnife`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Mother`
- **Description**: Use: Throw a penetrating projectile that returns to you.
- **Mechanics**:
```gon
ability wp_MomsKnife
```

### Mysterious Bone (`MysteriousBone`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Bone`
- **Description**: Use: A melee attack with a 25% chance to inflict Charm.
- **Mechanics**:
```gon
ability wp_MysteriousBone
```

### Holy Grail (`HolyGrail`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Cleric`
- **Description**: Use: Heal an adjacent unit or yourself for 5 HP.
- **Mechanics**:
```gon
ability wp_HolyGrail
```

### Spear of Destiny (`SpearOfDestiny`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: A melee attack with +1 reach that penetrates through units. RELOAD: Collect a blessing pickup or get hit by a Holy Element spell.
- **Mechanics**:
```gon
ability wp_SpearOfDestiny
```

### Heavy Mace (`HeavyMace`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Fighter`
- **Description**: Use: A melee attack with Knockback 2 that deals damage equal to your [img:str]. Cleaves and deals double damage to units with [img:shield].
- **Mechanics**:
```gon
spd -6
    ability wp_HeavyMace
```

### Uranium Rod (`UraniumRod`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Radioactive`
- **Description**: Use: A melee attack that inflicts -1 [img:con], Poison 2 and Weakness 1. At the end of each battle, if you are downed, gain a random mutation.
- **Mechanics**:
```gon
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
```

### Ocarina (`Ocarina`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Use: Cast a random musical spell.
- **Mechanics**:
```gon
ability wp_Ocarina
```

### Small Meteor (`SmallMeteor`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Planet`
- **Description**: - {str_aux_active_name} - {str_aux_active_desc}
- **Mechanics**:
```gon
randomize_piece_frames true
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
```

### Glowing Bone (`GlowingBone`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Bone`
- **Description**: - {str_aux_active_name} - {str_aux_active_desc}
- **Mechanics**:
```gon
randomize_piece_frames true
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
```

### Irradiated Object (`IrradiatedObject`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Radioactive`
- **Description**: {str_aux_item_desc}
- **Mechanics**:
```gon
randomize_piece_frames true
    str_aux_initialize random_passive_trinket
    str_aux_is_copy_item_passive true
    ability wp_IrradiatedObject
```

### IrradiatedObject_Burn (`IrradiatedObject_Burn`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Burn 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Burn
```

### IrradiatedObject_Stun (`IrradiatedObject_Stun`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Stun 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Stun
```

### IrradiatedObject_Bleed (`IrradiatedObject_Bleed`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Bleed 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Bleed
```

### IrradiatedObject_Bruise (`IrradiatedObject_Bruise`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Bruise 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Bruise
```

### IrradiatedObject_Poison (`IrradiatedObject_Poison`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Poison 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Poison
```

### IrradiatedObject_Sleep (`IrradiatedObject_Sleep`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Sleep 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Sleep
```

### IrradiatedObject_Fear (`IrradiatedObject_Fear`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Fear 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Fear
```

### IrradiatedObject_Charmed (`IrradiatedObject_Charmed`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Charmed 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Charmed
```

### IrradiatedObject_Weakness (`IrradiatedObject_Weakness`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Weakness 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Weakness
```

### IrradiatedObject_Confusion (`IrradiatedObject_Confusion`)
- **Kind**: `Unknown` | **Rarity**: `Unknown` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Confusion 1. {str_aux_item_desc} [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
variant_of IrradiatedObject
    ability wp_IrradiatedObject_Confusion
```

### Steel Ball (`SteelBall`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Summon an invulnerable Fly familiar. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_SteelBall
```

### USA Shield (`USAShield`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Superhero`
- **Description**: Use: A ranged attack that inflicts Stun. [s:.7](Usable once per battle.)[/s] Passive: +2 Brace while this weapon is usable.
- **Mechanics**:
```gon
passives {
        PassiveIfWeaponIsUsable {
            Brace 2
        }
    }
    ability wp_USAShield
```

### Tesla Cannon (`TeslaCannon`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Experimental`
- **Description**: Use: Fire a ranged electric shot that passes through units in a straight line with a 50% chance to Stun.
- **Mechanics**:
```gon
durability 3
    ability wp_TeslaCannon
```

### Meat Bomb (`MeatBomb`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Meat`
- **Description**: Use: Throw a bomb that explodes.
- **Mechanics**:
```gon
ability wp_SmallBomb
```

### Bloody Stick (`BloodyStick`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Wood`
- **Description**: +1 Health Regen. Use: A melee attack with +1 reach.
- **Mechanics**:
```gon
passives {
        HealthRegenUp 1
    }
    ability wp_Stick
```

### Bucket of Blood (`BucketOfBlood`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Gain +2 [img:con] and -1 [img:spd], then heal 4 HP.
- **Mechanics**:
```gon
ability wp_BucketOfLard
```

### Bloody Knife (`BloodyButterflyKnife`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: A multi-hit melee attack with Lifesteal that inflicts Bleed. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_BloodyButterflyKnife
```

### Bloody Bear Traps (`BloodyBearTraps`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `[Hunter, Survivalist]`
- **Description**: Use: Place a Bear Trap.
- **Mechanics**:
```gon
ability wp_BearTraps
```

### Bloody Bag of Glass (`BloodyBagOfGlass`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Throw a projectile that creates glass.
- **Mechanics**:
```gon
ability wp_BloodyBagOfGlass
```

### Meat Slugger (`MeatSlugger`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: A melee attack with Knockback 10 that inflicts Bruise.
- **Mechanics**:
```gon
ability wp_MeatSlugger
```

### Bloody Meat Hook (`BloodyMeatHook`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `[Butcher, Barbed]`
- **Description**: Use: Pull a unit towards you, Cleaving and inflicting Bleed 1.
- **Mechanics**:
```gon
ability wp_BloodyMeatHook
```

### Bloody Soul Claw (`BloodySoulClaw`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: A melee attack that deals damage equal to the number of uses this has left. When this weapon kills a unit, it gains +2 uses and you heal 5 HP.
- **Mechanics**:
```gon
durability 8
    ability wp_BloodySoulClaw
```

### Blood Bucket (`BloodBucket`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: A lobbed attack that creates a creep puddle.
- **Mechanics**:
```gon
ability wp_ChumBucket
```

### Bloody Spikes (`BloodySpikes`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: +1 Thorns. Use: A ranged attack.
- **Mechanics**:
```gon
passives {
        Thorns 1
    }
    ability wp_RailSpikes
```

### Bottles of Blood (`BottlesOfBlood`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: A lobbed attack that creates glass tiles in an area.
- **Mechanics**:
```gon
ability wp_BloodBottles
```

### Blessed Anointing Oil (`BlessedAnointingOil`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Cleric`
- **Description**: Use: Cleanse debuffs and heal an adjacent unit or yourself.
- **Mechanics**:
```gon
ability wp_BlessedAnointingOil
```

### Harpy's Claw (`HarpysClaw`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Poison 1, Bleed 1, Confusion 1, Weakness 1, and Slow 1.
- **Mechanics**:
```gon
ability wp_HarpyClaw
```

### Rat Bomb (`RatBomb`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Rat`
- **Description**: Use: Toss a Bomb that explodes at the end of the round.
- **Mechanics**:
```gon
durability 5
	ability wp_RatBomb
```

### Spinnerets (`Spinnerets`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: A ranged attack that inflicts Webbed.
- **Mechanics**:
```gon
durability 6
	ability wp_SpiderWebber
```

### Zodiac's Six Shooter (`ZodiacsSixshooter`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Cool`
- **Description**: Use: Fire a shot anywhere within your line of sight. Automatically use this whenever an enemy ends movement within your line of sight. Reloads at the end of each battle.
- **Mechanics**:
```gon
durability 6
    max_durability 6
    dont_destroy_on_0 true
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
```

### Gambit's Dice (`GambitsDice`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Throw a projectile that deals 1-6 damage at random. RELOAD: Cast a spell that costs exactly 6 mana.
- **Mechanics**:
```gon
ability wp_GambitsDice
```

### Johnny's Stool (`JohnnysStool`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Wood`
- **Description**: Use: A melee attack with Knockback 2. If you end your turn with a unused movement actions, heal 3 HP and gain 3 Charge.
- **Mechanics**:
```gon
ability wp_Stoolatk
    passives {
		StatusIfUnusedMovePoints {
			HealthGain 3
			Charge 3
		}
    }
```

### Alien Tech (`AlienTech`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Space`
- **Description**: Use: Target an area. Unleash a hyper beam attack in that area at the start of your next turn. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability AlienBeam
```

### Stacy 100 (`Stacy100`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Spawn a Stacy. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_SpawnStacy
```

### Bunga's Bone (`BungasBone`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Bone`
- **Description**: Use: A melee attack with Knockback 5.
- **Mechanics**:
```gon
ability wp_BungaClub
```

### Hitler's Pistol (`HitlersPistol`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Fire a shot in a straight line.
- **Mechanics**:
```gon
durability 8
	ability wp_Lugar
```

### Bug (`Bug`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Your basic attack is Metronome. Use: Cast a random spell.
- **Mechanics**:
```gon
attack BasicMetronome
	ability wp_OddRemote
	passives {
        OverrideBasicAttack BasicMetronome
	}
```

### Fate (`Fate`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Summon meteors that hit random tiles everywhere. These meteors have a chance to stun, spawn fires, or leave rocks behind.
- **Mechanics**:
```gon
ability wp_Fate
```

### Mammoth Tusk (`MammothTusk`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Wooly`
- **Description**: Use: A melee attack that inflicts Bruise 2 and Confusion. Become Drowsy after use. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_TuskThrow
```

### American Flag (`AmericanFlag`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: Force a unit to attack one of its enemies. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
str 1
	dex 1
    con 1
	spd 1
	int 1
	lck 1
	cha 1
	ability wp_Rally
```

### Book Of Belial (`BookOfBelial`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `[Demonic, Paper]`
- **Description**: Use: Gain +3 Damage. RELOAD: Kill an enemy.
- **Mechanics**:
```gon
ability wp_BookofBelial
```

### Mega Alien Blaster (`MegaAlienBlaster`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Space`
- **Description**: Use: A laser attack. Gains +5 damage for the rest of the battle each time it's used. Take 5 damage when used.
- **Mechanics**:
```gon
ability wp_MegaAlienBlaster
```

### Hell Hook (`HellHook`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `[Demonic, Barbed, Butcher]`
- **Description**: Use: Pull a unit toward you.
- **Mechanics**:
```gon
ability wp_MeatHookB
```

### Demon Core (`DemonCore`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Radioactive`
- **Description**: Start each battle with Poison 5. Inflict All Stats Down 2 on bosses and minibosses at the start of the battle. Use: A melee attack that causes a unit to die at the end of its next turn. Bosses fall asleep at the end of their next turn instead.
- **Mechanics**:
```gon
ability wp_DemonDoom
    passives {
        Poison 5
        StatusAllCharactersOnSpawn {
            Conditional_Boss {
                AllStatsUp -2
            }
        }
    }
```

### Bag Of Chum (`BagOfChum`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Guts`
- **Description**: Use: Spawn a Charmed Maggot.
- **Mechanics**:
```gon
ability wp_ChumShot
```

### Golden Pickaxe (`GoldenPickaxe`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Miner`
- **Description**: Use: A melee attack that ignores shield. If used on static or inanimate objects it destroys them and spawns a Coin. Spawn a coin on a random tile at the end of each turn.
- **Mechanics**:
```gon
ability wp_GoldPickaxe
	passives {
		StatusEachTurnEnd {
			SpawnCoinAnywhere 1
		}
    }
```

### Manhole Cover (`ManholeCover`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Brace 2. Use: A ranged attack with Knockback 2 that passes through units and returns to you.
- **Mechanics**:
```gon
ability wp_Manhole
	passives {
		Brace 2
    }
```

### Tina's Larynx (`TinasLarynx`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Guts`
- **Description**: Use: Inflict Fear on all enemies. [s:.7](Usable once per battle.)[/s]
- **Mechanics**:
```gon
ability wp_TinaScream
```

### Robotic Arm (`RoboticArm`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Cyborg`
- **Description**: Use: A melee attack with a chance to repeat. Gains 1 damage for the rest of the battle each time it's used. Refreshes when affected by Electric element.
- **Mechanics**:
```gon
ability wp_FuryArm
    passives {
        RefreshEquipmentAbilityOnElement {
            element Electric
            text "COMBAT_POPUP_RECHARGED"
        }
    }
```

### Steven's Shotgun (`StevensShotgun`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Use: Fires 5 projectiles in a cone. Using this recoils you 10 tiles backwards and Confuses you.
- **Mechanics**:
```gon
ability wp_ShotgunSteven
```

### Steven's Gristle (`StevensGristle`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Units don't leave corpses. Use: A melee attack. This weapon gains +1 damage and +1 use when it gets a kill. Damage resets at the end of the adventure.
- **Mechanics**:
```gon
durability 99
    aux 1
    reset_aux_on_store 1
    ability wp_GnarledClaw
    passives {
        CreateGlobalModifiers {
            NoCorpses 1
        }
    }
```

### Steven's Bag of Rocks (`StevensBagofRocks`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Use: A melee attack with a chance to repeat that inflicts Bruise.
- **Mechanics**:
```gon
ability wp_StevensBagOfRocks
```

### Steven's Bottle (`StevensBottle`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Use: A ranged attack that creates a Tar tile.
- **Mechanics**:
```gon
ability wp_StevensBottles
```

### Steven (`StevenWeapon1`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Use: A melee attack. If this hits an allied cat, spawn a quarter-sized copy of them with 25% of their stats. The copy is AI controlled. RELOAD: An allied cat dies.
- **Mechanics**:
```gon
ability wp_StevenWeapon1
```

### Steven (`StevenWeapon2`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Steven`
- **Description**: Use: A lobbed attack that inflicts Petrify. RELOAD: Kill a rock.
- **Mechanics**:
```gon
ability wp_StevenWeapon2
```

### Toy Gun (`ToyGun`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Jester`
- **Description**: Use: A melee attack with Knockback 10 and Chain Knockback that inflicts Bruise.
- **Mechanics**:
```gon
ability wp_BangGun
```

### Pliers (`Pliers`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Use: A melee attack that inflicts Weakness 3.
- **Mechanics**:
```gon
ability wp_Pliers
```

### Feather Darts (`FeatherDarts`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `Feathered`
- **Description**: Use: A ranged attack that can hit any unit in your line of sight. Can be used 3 times per turn.
- **Mechanics**:
```gon
durability 99
    ability wp_FeatherDarts
    passives {
        ExtraWeaponAttacks 2
    }
```

### Feathered Wing (`FeatheredWing`)
- **Kind**: `weapon` | **Rarity**: `Unknown` | **Set**: `Feathered`
- **Description**: Use: A wide wind attack with Knockback 3.
- **Mechanics**:
```gon
durability 20
    ability wp_FeatheredWing
```

### Money Bag (`MoneyBag_Small`)
- **Kind**: `weapon` | **Rarity**: `common` | **Set**: `None`
- **Description**: Becomes {aux} coins when you return home. Use: A melee attack.
- **Mechanics**:
```gon
on_store become_aux_coins
    aux 10
    ability wp_MoneyBag_Small
    passives {
        BreakAtAux 0
    }
```

### Money Bag (`MoneyBag_Medium`)
- **Kind**: `weapon` | **Rarity**: `uncommon` | **Set**: `None`
- **Description**: Becomes {aux} coins when you return home. Use: A melee attack.
- **Mechanics**:
```gon
on_store become_aux_coins
    aux 25
    ability wp_MoneyBag_Medium
    passives {
        ItemAuxTransform {
            le [10 MoneyBag_Small]
        }
        BreakAtAux 0
    }
```

### Money Bag (`MoneyBag_Large`)
- **Kind**: `weapon` | **Rarity**: `rare` | **Set**: `None`
- **Description**: Becomes {aux} coins when you return home. Use: A melee attack.
- **Mechanics**:
```gon
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
```

### Money Bag (`MoneyBag_Huge`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `None`
- **Description**: Becomes {aux} coins when you return home. Use: A melee attack.
- **Mechanics**:
```gon
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
```

### The Pact (`ThePact`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Demonic`
- **Description**: Use: Permanently lose 1 [img:con] to gain +1 [img:str], +2 [img:dex] and +2 [img:spd] for the rest of the battle.
- **Mechanics**:
```gon
ability wp_ThePact
```

### Probe (`Probe`)
- **Kind**: `weapon` | **Rarity**: `very_rare` | **Set**: `Space`
- **Description**: Use: Inflict Charm 3. Can only hit from behind.
- **Mechanics**:
```gon
ability wp_Probe
```

