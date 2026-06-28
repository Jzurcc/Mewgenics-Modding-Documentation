# Abilities/System and Item Abilities Directory

## File: `armor_abilities.gon`

### `set_GrubFamiliarReturn`
**Source:** `armor_abilities.gon`  

```
set_GrubFamiliarReturn {
    template targeted_status
    
    graphics {
        animation attack
    }

    cost {
        mana 0
        move_points 0
        act_points 1
    }

    target {
        min_range 1
        max_range 1
        range_mode cross
        restrictions [must_have_buddy must_have_living_character]
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            GenericBuff 100
            GiveBoundItemToTarget 1
        }
    }

    self_damage {
        damage 0
        type none

        effects {
            DeleteObject 1
        }
    }
}
```

---

### `set_MummySetCurse`
**Source:** `armor_abilities.gon`  

```
set_MummySetCurse {
    template spell

    graphics {
        particle PoisonPoof
    }
    
    target {
        target_mode none
        aoe_mode all
        aoe_restrictions enemies_only
        aoe_considers_character_size false
        knockback_mode zero
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Rot 1
            Weakness 1
        }
    }
}
```

---

### `set_HumanFleshSetCurse`
**Source:** `armor_abilities.gon`  

```
set_HumanFleshSetCurse {
    template spell

    graphics {
        particle PoisonPoof
    }
    
    target {
        target_mode none
        aoe_mode all
        aoe_restrictions enemies_only
        aoe_considers_character_size false
        knockback_mode zero
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Fear 2
        }
    }
}
```

---

### `neck_TentacleArmorCounter`
**Source:** `armor_abilities.gon`  

```
neck_TentacleArmorCounter {
    template spell

    graphics {
        affected_particle fx_tentaclestrangle
        miss_particle fx_tentaclestrangleMiss
		fx_is_placeholder_animation true
        fx_random_flip true
    }
    
    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 4
        type physical_spell
    }
}
```

---

### `set_SpaceArmorJump`
**Source:** `armor_abilities.gon`  

```
set_SpaceArmorJump {
    variant_of BasicJump

    target {
        restrictions none
        always_bounce true
    }

    damage_instance {
        type melee
        damage 4
        
        effects {
            IgnoreSelf 1
            Displace 1
        }
    }
}
```

---

### `set_PlanetSetGravity`
**Source:** `armor_abilities.gon`  

```
set_PlanetSetGravity {
    template spell

    graphics {
        particle none
    }
    
    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 2

        aoe_considers_character_size true
        aoe_excludes_self true
        knockback_mode tile_to_target
    }

    damage_instance {
        type none
        damage 0
        knockback 1

        elements [
            Gravity
        ]
    }
}
```

---

### `head_MiniMoonArmorAsteroid`
**Source:** `armor_abilities.gon`  

```
head_MiniMoonArmorAsteroid {
    variant_of Asteroid
    
    graphics {
        animation none
    }
}
```

---

### `head_MagnetoAttract`
**Source:** `armor_abilities.gon`  

```
head_MagnetoAttract {
    template spell

    graphics {
        particle none
        animation none
    }
    
    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 1

        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode tile_to_character
        restrictions aoe_must_exist
        aoe_restrictions must_have_tag
        target_requires_tag pickup
    }

    damage_instance {
        damage 0
        knockback 1
    }
}
```

---

### `head_CrownOfHorns`
**Source:** `armor_abilities.gon`  

```
head_CrownOfHorns {
    template straightshot_attack

    graphics {
        projectile NeedleProjectile
        animation none
    }
    
    target {
        aoe_mode custom
        aoe_symmetry four_way
        custom_aoe [[1, 1] [1, 0]]
    }

    damage_instance {
        damage 2
    }
}
```

---

### `neck_DarkFriend`
**Source:** `armor_abilities.gon`  

```
neck_DarkFriend {
    template spawn

    tags [summon]
    
    graphics {
        lob true
        animation none
    }
    
    target {
        min_range 1
        max_range 5
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }
    
    spawn {
        object PlayerCat_ThiefShade
        faction self

        catdata clone
        clone_items true
        
        additional_passives {
            HideEquipment neck
            ApplyPassivesToSpawnerWhileAlive {
                HideEquipment neck
            }
        }
    }
    
    damage_instance {
        ai_base_score 1000
        custom_additional_ai_weight tile_close_to_enemy
    }
}
```

---

### `head_EmoSong`
**Source:** `armor_abilities.gon`  

```
head_EmoSong {
    template spell
    
    tags [musical]

    graphics {
        animation sing3
        particle None
    }

    target {
        target_mode none
        max_aoe 2
    }

    damage_instance {
        heal 1
        cant_miss true

        effects {
            TempDamageUp 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `set_WitchJump`
**Source:** `armor_abilities.gon`  

```
set_WitchJump {
    variant_of BasicJump

    target {
        max_range 20
    }
}
```

---

### `face_LeechBrood`
**Source:** `armor_abilities.gon`  

```
face_LeechBrood {
    template lobbed_attack
    
    graphics {
		projectile LeechProjectile
    }
    
    target {
        target_mode none
        aoe_mode all
        aoe_restrictions enemies_only
        aoe_considers_character_size false
        knockback_mode zero
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Leeches 1
        }
    }
}
```

---

### `head_Pestilence`
**Name:** Pestilence  
**Description:** Deal 1 damage to all units.  
**Source:** `armor_abilities.gon`  

```
head_Pestilence {
    template spell

    meta {
        name "ABILITY_CROWNOFPESTILENCE_NAME"
        desc "ABILITY_CROWNOFPESTILENCE_DESC"
        ability_icon Pestilence
        animate_name false
    }

    graphics {
        particle PoisonPoof
		animation evilMagic
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
    }

    damage_instance {
        damage 1
    }
}
```

---

### `neck_ChefsApron`
**Source:** `armor_abilities.gon`  

```
neck_ChefsApron {
    template spawn

    meta {
    }

    tags [summon]
    
    graphics {
        lob true
        animation none
        dont_orient true
    }
    
    target {
        target_mode random_tile
        min_range 1
        max_range 2
    }

    spawn {
        object Food
    }
}
```

---

### `head_HeadBrandJump`
**Source:** `armor_abilities.gon`  

```
head_HeadBrandJump {
    variant_of BasicJump

    target {
        restrictions none
        always_bounce true
    }

    damage_instance {
        damage 1
        
        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `head_ThrobbingCrown`
**Source:** `armor_abilities.gon`  

```
head_ThrobbingCrown {
    template spell

    graphics {
        animation none
        affected_particle fx_tentaclestrangle
        miss_particle fx_tentaclestrangleMiss
        fx_is_placeholder_animation true
        fx_random_flip true
        miss_random_delay [0, 20]
        random_delay [30 50]
    }
    
    target {
        target_mode none
        min_aoe 1
        max_aoe 1
    }

    damage_instance {
        damage 8
    }
}
```

---

### `head_IronJaw`
**Source:** `armor_abilities.gon`  

```
head_IronJaw {
    template melee_attack
    
    graphics {
        animation biteattack
    }

    damage_instance {
        damage 3
        effects {
            Leech 1
        }
    }
}
```

---

### `face_StevenMask2`
**Source:** `armor_abilities.gon`  

```
face_StevenMask2 {
    template spawn

    tags [summon]
    
    graphics {
        lob true
        animation none
    }
    
    cost {
        can_cast_while_dead true
    }

    target {
        target_mode random_tile
        min_range 1
        max_range 5
        max_aoe 0
        aoe_restrictions [exclude_blocking]
    }
    
    spawn {
        object RANDOM_1X1_ENEMY
        faction self
    }
}
```

---

## File: `consumable_item_abilities.gon`

### `cm_Heal`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Heal {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, meat]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        heal item_aux

        effects {
            ClearStarving 1
        }
    }
}
```

---

### `cm_Catnip`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Catnip {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, catnip]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            ManaGain item_aux
        }
    }
}
```

---

### `cm_Shield`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Shield {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, pill]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            Shield item_aux
        }
    }
}
```

---

### `cm_StrBuff`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_StrBuff {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, pill]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            StrengthUp item_aux
        }
    }
}
```

---

### `cm_DexBuff`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_DexBuff {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, pill]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            DexterityUp item_aux
        }
    }
}
```

---

### `cm_ConBuff`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_ConBuff {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, pill]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            ConstitutionUp item_aux
        }
    }
}
```

---

### `cm_IntBuff`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_IntBuff {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, pill]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            IntelligenceUp item_aux
        }
    }
}
```

---

### `cm_SpdBuff`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_SpdBuff {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, pill]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            SpeedUp item_aux
        }
    }
}
```

---

### `cm_ChaBuff`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_ChaBuff {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, pill]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            CharismaUp item_aux
            ManaGain 6
        }
    }
}
```

---

### `cm_LckBuff`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_LckBuff {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, pill]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            LuckUp item_aux
        }
    }
}
```

---

### `cm_Antidote`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Antidote {
    template targeted_status

    meta {
        name "{itemname}"
    }
    tags [consumable]
    
    graphics {
        affected_particle Cleanse
        animation showTrinket
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 0
        max_range 1
    }

    damage_instance {
        effects {
            Cleanse 0
        }
    }
}
```

---

### `cm_Nipple`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Nipple {
    template melee_spell

    meta {
        name "{itemname}"
    }
    tags consumable

    graphics {
        animation showTrinket
        particle fx_statup
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            HealthRegenUp 1
        }
    }
}
```

---

### `cm_ExperimentX`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_ExperimentX {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags consumable

    keyword_tooltips {}
    
    graphics {
        animation drinkTrinket
        particle fx_statup
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            ApplyMultipleTimes {
                stacks 8

                RandomStatusFromPool {
                    Quivered 1
                    MoveQuivered 1
                    Thorns 1
                    Brace 1
                    Shield 1
                    DivineShield 1
                    BleedThorns 1
                    KineticSpikes 1
                    Reflect 1
                    DiminishingHealthRegen 1
                    Charge 1
                    AllStatsUp 1
                    StrengthUp 1
                    DexterityUp 1
                    SpeedUp 1
                    ConstitutionUp 1
                    IntelligenceUp 1
                    CharismaUp 1
                    LuckUp 1
                    PoisonLace 1
                    Lifesteal 1
                    CritChanceUp 1
                    DodgeChance_Status 1
                    HealthRegenUp 1
                    BackflipWhenTargeted 1
                    TempCounterAttack 1
                }
            }
            ApplyMultipleTimes {
                stacks 4

                RandomStatusFromPool {
                    Slow 2
                    Weakness 2
                    MagicWeakness 2
                    Bruise 2
                    Marked 1
                    Ostracized 1
                    Hex 1
                    Tarred 1
                    Scrambled 2
                    DelayedPain 1
                    Rot 1
                    Infested 1
                    Poison 1
                }
            }
        }
    }
}
```

---

### `cm_Steven1`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Steven1 {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags consumable

    graphics {
        animation eatTrinket
        particle fx_statup
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            PermanentUpgradeRandomActiveOrPassive 1
        }
    }
}
```

---

### `cm_Steven2`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Steven2 {
    template spawn

    meta {
        name "{itemname}"
    }
    tags [summon consumable]
    
    graphics {
        animation eatTrinket
    }

    cost {
        mana 0
        cantrip true
        must_not_be_a_summon true
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }
    
    spawn {
        object PlayerCat_StevenShade
        faction self

        catdata clone
        clone_items true // todo: don't clone the consumable (the clone can't use it anyway but it would be better for it not to be there at all)
    }
}
```

---

### `cm_Gizzard`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Gizzard {
    variant_of MockingbirdForm
    
    meta {
        name "{itemname}"
    }
    tags [consumable shapeshift]

    cost {
        mana 0
        cantrip true
        infcantrip false
    }

    damage_instance {
        effects {
            ApplyPassives {
                StatusOnBattleEnd {
                    even_if_dead true
                    RandomTaggedMutation bird
                }
            }
        }
    }
}
```

---

### `cm_JokerCard`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_JokerCard {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            DuplicateRandomEquippedItem 1
        }
    }
}
```

---

### `tk_WaterBottle_Full`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
tk_WaterBottle_Full {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable] //i dont think this technically counts as a consumable?

    graphics {
        animation drinkTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        heal 5

        effects {
            DrinkWater 1
        }

        elements [
            Lesser_Water
        ]
    }
}
```

---

### `tk_WaterBottle_Half`
**Source:** `consumable_item_abilities.gon`  

```
tk_WaterBottle_Half {
    variant_of tk_WaterBottle_Full

    meta {
    }
}
```

---

### `tk_WaterBottle_Empty`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
tk_WaterBottle_Empty {
    template ranged_attack

    meta {
        name "{itemname}"
    }
    //tags [consumable] //i dont think this technically counts as a consumable?

    graphics {
        animation throwobject
    }
    
    cost {
        mana 0
        cantrip true
        durability 0
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    self_damage {
        effects {
            DestroyTrinket 1
        }
    }

    damage_instance {
        damage 1

        effects {
            Confusion 1
        }
    }
}
```

---

### `cm_Kidney`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Kidney {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, meat]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        heal 10
		HealthRegenUp 2
		
        effects {
            Cleanse 0
            ClearStarving 1
        }
    }
}
```

---

### `cm_Enema`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Enema {
    template self_buff
    chain_ability Dump

    meta {
        name "{itemname}"
    }
    tags [consumable]
    
    graphics {
        particle Wave
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            PurgeAll 1
        }

        elements [
            Water
        ]
    }
}
```

---

### `cm_HealPercent`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_HealPercent {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation eatTrinket
    }
    
    target {
        X_is max_health
    }
    
    cost {
        mana 0
        cantrip true
        X_cant_be_zero true
    }

    damage_instance {
        heal "ceil(X*item_aux/100)"
    }
}
```

---

### `cm_HealPercent_Auto`
**Source:** `consumable_item_abilities.gon`  

```
cm_HealPercent_Auto {
    variant_of cm_HealPercent

    meta {
        is_trinket true
    }
    
    self_damage {
        effects {
            DamageTrinket 1
        }
    }
}
```

---

### `cm_Lard`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Lard {
    template spell
    
    meta {
        name "{itemname}"
    }
    graphics {
        animation none
        particle none
    }
    
    target { 
        target_mode none
        max_aoe 1
        knockback_mode tile_to_character
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            FaceAway 1
            ImmediateUseAbility cm_Lard_Impl
        }
    }

    self_damage {
        effects {
            // consume durability here since ImmediateUseAbility seems to bypass the durability loss
            DamageTrinket 1
        }
    }
}
```

---

### `cm_Lard_Impl`
**Source:** `consumable_item_abilities.gon`  

```
cm_Lard_Impl {
    template self_buff
    tags [consumable, meat]
    
    graphics {
        animation gulp
    }

    damage_instance {
        effects {
            FullHeal 1
            ClearStarving 1
        }
    }
}
```

---

### `cm_KiloOfCatnip`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_KiloOfCatnip {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, catnip]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
			FillMana 1
            }
        }
}
```

---

### `cm_SmellingSalts`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_SmellingSalts {
    template targeted_status

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        aoe_restrictions must_have_corpse
        restrictions aoe_must_exist
        min_range 0
        max_range 1
    }
    
    damage_instance {
        effects {
            Revive 1
        }
    }
}
```

---

### `cm_ViperBottle`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_ViperBottle {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation drinkTrinket
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            RandomPermanentStat 1
            Conditional_RandomChance {
                odds 10%
                ApplyPassives {
                    StatusOnBattleEnd {
                        even_if_dead true
                        RandomTaggedMutation melted
                    }
                }
            }
        }
    }

    self_damage {
        damage 5
    }
}
```

---

### `cm_SuperBandage`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_SuperBandage {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation showTrinket
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            HealRandomInjury 1
        }
    }
}
```

---

### `cm_RottenMeat`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_RottenMeat {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, meat]

    graphics {
        animation eatTrinket
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    damage_instance {
        effects {
            Poison 1
            ApplyPassives {
                ReplaceBasicAttack BasicPuke
            }
            ClearStarving 1
        }
    }
}
```

---

### `cm_AllStatsBuff`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_AllStatsBuff {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            AllStatsUp item_aux
        }
    }
}
```

---

### `cm_Star`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Star {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            Temporary {
                status AllDamageImmune
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
            Temporary {
                status Trample
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
            Temporary {
                status Thorns
                stacks 10
                turns 1
                expires_on_begin_turn true
            }
            RefreshMovePoints 1
        }
    }
}
```

---

### `cm_Bullseye`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Bullseye {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            Temporary {
                status MaxAccuracy
                stacks 1
                turns 1
                expires_on_end_turn true
            }
            Temporary {
                status AllDamageCrits
                stacks 1
                turns 1
                expires_on_end_turn true
            }
        }
    }
}
```

---

### `cm_StemCells`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_StemCells {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, meat] // kinda pushing the definition of meat, but it's definitely not vegan

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            HealthRegenUp 3
            ClearStarving 1
        }
    }
}
```

---

### `cm_WitchsEye`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_WitchsEye {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable, meat]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            BackflipWhenTargeted 2
            ClearStarving 1
        }
    }
}
```

---

### `cm_ForbiddenFruit`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_ForbiddenFruit {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            FullHeal 1
            FillMana 1
            AllStatsUp 2

            Conditional_GoodRoll {
                odds 90%
                GainDisorderFromPool_PostCast forbidden_spell_consequences
            } Else {
                GainDisorderFromPool_PostCast forbidden_spell_consequences_crippling
            }
        }
    }
}
```

---

### `cm_PCP`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_PCP {
    template targeted_status

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation drinkTrinket
        affected_particle PoisonPoof
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 0
        max_range 1
    }

    damage_instance {
        effects {
            Madness 3
            Temporary {
                status DamageUp
                stacks 5
                turns 3
                expires_on_end_turn true
            }
        }
    }
}
```

---

### `cm_WishBone`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_WishBone {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            TempLuckUp 99
        }
    }
}
```

---

### `cm_MetalCoat`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_MetalCoat {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
        requires_destructible_weapon true
    }

    damage_instance {
        effects {
            MakeWeaponUnbreakable 1
        }
    }
}
```

---

### `cm_ShoePolish`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_ShoePolish {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            RepairWeapon 99
            RefreshWeaponAbility 1
            RepairWeaponCondition 1
        }
    }
}
```

---

### `cm_Pearl`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_Pearl {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            GainCoinsRange {
                min 10
                max 30
            }
        }
    }
}
```

---

### `cm_TheD6`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_TheD6 {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            PermanentUpgradeRandomActive 1
        }
    }
}
```

---

### `cm_BigToe`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_BigToe {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    graphics {
        affected_particle Cleanse
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        heal 6

        effects {
            Cleanse 0
            HealthRegenUp 1
        }
    }
}
```

---

### `cm_RaptorEgg`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_RaptorEgg {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            FullHeal 1
        }
    }
}
```

---

### `cm_RaptorEggSpawn`
**Source:** `consumable_item_abilities.gon`  

```
cm_RaptorEggSpawn {
    template spawn

    meta {
    }

    tags [summon]
    
    graphics {
        lob true
        animation none
        dont_orient true
    }
    
    target {
        target_mode random_closest_tile
        min_range 1
        max_range 1
    }

    spawn {
        object [CharmedRaptorBaby]
        //additional_passives {
        //    Madness 1
        //}
    }
}
```

---

### `cm_JarOfChaos`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_JarOfChaos {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation drinkTrinket
        particle fx_statup
    }

    cost {
        mana 0
        cantrip true
    }

    self_damage {
        effects {
            TransformEquipment {
                from JarOfChaos
                to JarOfNothing
            }
        }
    }

    damage_instance {
        effects {
            PermanentStrength 2
            PermanentDexterity 2
            PermanentConstitution 2
            PermanentIntelligence 2
            PermanentCharisma 2
            PermanentSpeed 2
            PermanentLuck 2
            PermanentUpgradeRandomActive 4
        }
    }
}
```

---

### `cm_ClassSeal`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_ClassSeal {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation druidTransform
    }
    
    cost {
        mana 0
        cantrip true
    }
}
```

---

### `cm_FighterSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_FighterSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Fighter
        }
    }
}
```

---

### `cm_HunterSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_HunterSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Hunter
        }
    }
}
```

---

### `cm_MageSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_MageSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Mage
        }
    }
}
```

---

### `cm_TankSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_TankSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Tank
        }
    }
}
```

---

### `cm_ClericSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_ClericSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Medic
        }
    }
}
```

---

### `cm_ThiefSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_ThiefSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Thief
        }
    }
}
```

---

### `cm_ButcherSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_ButcherSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Butcher
        }
    }
}
```

---

### `cm_PsychicSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_PsychicSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Psychic
        }
    }
}
```

---

### `cm_DruidSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_DruidSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Druid
        }
    }
}
```

---

### `cm_NecromancerSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_NecromancerSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Necromancer
        }
    }
}
```

---

### `cm_MonkSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_MonkSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Monk
        }
    }
}
```

---

### `cm_TinkererSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_TinkererSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Tinkerer
        }
    }
}
```

---

### `cm_JesterSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_JesterSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Jester
        }
    }
}
```

---

### `cm_ColorlessSeal`
**Source:** `consumable_item_abilities.gon`  

```
cm_ColorlessSeal {
    variant_of cm_ClassSeal
    damage_instance {
        effects {
            ChangeCatClass Colorless
        }
    }
}
```

---

### `cm_EatHummingbird`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_EatHummingbird {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags consumable

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            SpeedUp item_aux
			DodgeChance_Status 50
			SizeScale .6
        }
    }
}
```

---

### `cm_ForbiddenPill`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_ForbiddenPill {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            UpgradeRandomAbility 1
			UpgradeRandomAbility 1
			UpgradeRandomAbility 1
			UpgradeRandomAbility 1
            Conditional_GoodRoll {
                odds 90%
                GainDisorderFromPool_PostCast forbidden_spell_consequences
            } Else {
                GainDisorderFromPool_PostCast forbidden_spell_consequences_crippling
            }
        }
    }
}
```

---

### `cm_RedPill`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_RedPill {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]
    
    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
		damage 0
        type status_spell
        effects {
            Conditional_GoodRoll {
                odds 50%
                GainDisorder Chungus
            }
            Else {
                DoDamage {
                    damage 8
                    type spell
                }
            }
        }
    }
}
```

---

### `cm_UnstableDNA`
**Name:** {itemname}  
**Source:** `consumable_item_abilities.gon`  

```
cm_UnstableDNA {
    template self_buff

    meta {
        name "{itemname}"
    }
    tags [consumable]

    graphics {
        animation eatTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
		damage 0
        type status_spell
        effects {
            RandomStatUp -3
			RandomStatUp 6
            ApplyPassives {
                StatusOnBattleEnd {
                    even_if_dead true
                    RandomMutation 3
                }
            }
		}
    }
}
```

---

## File: `item_abilities.gon`

### `wp_GlassShard`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_GlassShard {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 2
        piercing true
        incidentally_collects_pickups false
        effects {
            Bleed 1
        }
    }
}
```

---

### `wp_RailSpikes`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RailSpikes {
    template ranged_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }
    
    damage_instance {
        damage 5
    }
}
```

---

### `wp_NailBoard`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_NailBoard {
    template melee_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }

    damage_instance {
        damage 8
        incidentally_collects_pickups false
    }
}
```

---

### `wp_LilSlugger`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_LilSlugger {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 0
        knockback 5
        incidentally_collects_pickups false
    }
}
```

---

### `wp_ChumBucket`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ChumBucket {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 5+bonus_range

        max_aoe 1

        can_multihit false
    }

    graphics {
        animation weaponthrowhigh
        single_projectile true
        projectile source_weapon
    }
    
    damage_instance {
        damage 5
        effects {
            SpawnCreep 1
        }
    }
}
```

---

### `wp_MeatHook`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MeatHook {
    template straightshot_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        max_range 10

        knockback_mode pull_to_character
    }

    graphics {
        animation weaponthrowstraight

        projectile HookProjectile
        chain_movieclip ChainLink
        chain_distance .25
    }
    
    damage_instance {
        damage 0

        effects {
            CollectsPickups 1
        }
    }
}
```

---

### `wp_MeatHookB`
**Source:** `item_abilities.gon`  

```
wp_MeatHookB {
    variant_of wp_MeatHook

    target {
        target_mode direction8
    }
}
```

---

### `wp_Kebab`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Kebab {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }

    target {
        max_aoe 2
    }

    damage_instance {
        damage 5
        piercing true
        incidentally_collects_pickups false
    }
}
```

---

### `wp_Pipe`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Pipe {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }

    damage_instance {
        damage 3
        incidentally_collects_pickups false
        effects {
            Stun [1, .1]
        }
    }
}
```

---

### `wp_ObsidianChunk`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ObsidianChunk {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponstab
    }

    self_damage {
        effects {
            LateStatusApplication {
                AddWeaponAux 2
            }
        }
    }

    damage_instance {
        damage item_aux
        incidentally_collects_pickups false
    }
}
```

---

### `wp_SoulClaw`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SoulClaw {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponstab
    }

    damage_instance {
        damage durability
        incidentally_collects_pickups false
        effects {
            RepairOnKill 2
        }
    }
}
```

---

### `wp_Bomb`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Bomb {
    template spell

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range

        min_aoe 0
        max_aoe 2
    }

    graphics {
        animation weaponthrowhigh
        use_projectile true
        projectile source_weapon

        particle Explosion
        delay 1
    }
    
    damage_instance {
        damage 10
        knockback 1
        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `wp_SmallBomb`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SmallBomb {
    template spell

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range

        min_aoe 0
        max_aoe 1
    }

    graphics {
        animation weaponthrowhigh
        use_projectile true
        projectile source_weapon

        particle Explosion
        delay 1
    }
    
    damage_instance {
        damage 5
        knockback 1
        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `wp_BoneClub`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BoneClub {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        durability 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }

    damage_instance {
        damage 8
        incidentally_collects_pickups false

        effects {
            ChanceToBreak 15
        }
    }
}
```

---

### `wp_Molars`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Molars {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 5+bonus_range
    }

    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }
    
    damage_instance {
        damage 1
    }
}
```

---

### `wp_Whetstone`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Whetstone {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {

    }
    
    damage_instance {
        effects {
            DamageUp 1
        }
    }
}
```

---

### `wp_HairSpray`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_HairSpray {
    template spell

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        particle Explosion
        delay 10
        animation weaponspell
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 2
    }
    
    damage_instance {
        damage 1

        effects {
            Burn 1
        }
        
        elements [
            Fire
        ]
    }
}
```

---

### `wp_Lighter`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Lighter {
    template spell

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        particle Explosion
        delay 10
        animation weaponspell
    }
    
    target {
        target_mode direction

        aoe_mode line
        min_aoe 1
        max_aoe 1
    }
    
    damage_instance {
        damage 1

        effects {
            Burn 1
        }
        
        elements [
            Fire
            Napalm
        ]
    }
}
```

---

### `wp_SeedBomb`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SeedBomb {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 5
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 0

        effects {
            ChangeTile TallGrassTile
        }
    }
}
```

---

### `wp_Battery`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Battery {
    template spell

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        particle Bolt
        animation weaponspell3
    }
    
    target {
        max_aoe 0
        max_range 3
    }
    
    damage_instance {
        damage 2
        
        effects {
            Stun [1, .1]
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `wp_Hose`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Hose {
    template spell
    
    meta {
        name "{itemname}"
    }

    graphics {
        particle Wave
        animation weaponspell
    }

    sounds {
        ontrigger OldHose_Start_Trigger
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode direction
        
        aoe_mode line
        min_aoe 1
        max_aoe 10
        
        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode orientation
    }

    damage_instance {
        damage 0
        knockback 1

        effects {
            ChangeTile WaterTile
        }

        elements [
            Water
        ]
    }
}
```

---

### `wp_SixPack`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SixPack {
    template spell

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 5+bonus_range

        max_aoe 1

        can_multihit false
    }

    graphics {
        use_projectile true
        animation weaponthrowhigh
        single_projectile true
        projectile source_weapon
        particle Wave
        delay 15
    }
    
    damage_instance {
        damage 6
        
        elements [
            Water
        ]
    }
}
```

---

### `wp_IceCubes`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_IceCubes {
    template spell

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 3+bonus_range

        max_aoe 0
    }

    graphics {
        use_projectile true
        animation weaponthrowhigh
        projectile IcecubeParticle
		particle none
    }
    
    damage_instance {
        damage 0

        effects {
            Freeze 1
        }
        
        elements [
            Ice
        ]
    }
}
```

---

### `wp_DryIce`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_DryIce {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponspell2
    }

    damage_instance {
        damage 2
        incidentally_collects_pickups false

        effects {
            Slow 1
        }
        elements [
            Ice
        ]
    }
}
```

---

### `wp_Bottles`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Bottles {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 4

        effects {
            ChangeTile GlassTile
        }
    }
}
```

---

### `wp_Stick`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Stick {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }

    target {
        max_aoe 2
        aoe_restrictions must_have_line_of_sight_unpurgable
    }

    damage_instance {
        damage 4
        incidentally_collects_pickups false
    }
}
```

---

### `wp_BigStick`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BigStick {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }

    target {
        max_aoe 3
        aoe_restrictions must_have_line_of_sight_unpurgable
    }

    damage_instance {
        damage 6
        incidentally_collects_pickups false
    }
}
```

---

### `wp_BiggestStick`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BiggestStick {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }

    target {
        max_aoe 4
        aoe_restrictions must_have_line_of_sight_unpurgable
    }

    damage_instance {
        damage 8
        incidentally_collects_pickups false
    }
}
```

---

### `wp_Log`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Log {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }

    target {
        aoe_mode custom
        custom_aoe [
                     [1, 1], [2, 1], [3, 1], [4, 1],
                     [1, 0], [2, 0], [3, 0], [4, 0],
                     [1,-1], [2,-1], [3,-1], [4,-1],
                   ]

        knockback_mode orientation
    }

    damage_instance {
        damage 10
        knockback 1
        incidentally_collects_pickups false
        effects {
            Bruise 1
            DoScreenShake {
                time .75
                intensity 10
            }

            QuakeAreaChance {
                radius 0
                chance 50%
            }
        }
    }
}
```

---

### `wp_RubberFist`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RubberFist {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 0
        knockback 1
        incidentally_collects_pickups false

        effects {
            Confusion 1
        }
    }
}
```

---

### `wp_BarbedPaw`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BarbedPaw {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false
        effects {
            Bleed 1
        }
    }
}
```

---

### `wp_GnarledClaw`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_GnarledClaw {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponstab
    }

    damage_instance {
        damage item_aux
        incidentally_collects_pickups false
        effects {
            RepairOnKill 1
            IncreaseItemAuxOnKill 1
        }
    }
}
```

---

### `tr_SelfDestruct`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tr_SelfDestruct {
    template spell

    meta {
        name "{itemname}"
    }

    graphics {
        particle Explosion
        animation blowUp
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode none
        max_aoe 1
    }


    damage_instance {
        damage 50
        piercing true
        cant_miss true
        elements [
            Fire
            Napalm
            Explosion
        ]
        effects {
            Vaporize 1
        }
    }
    splash_damage {
        damage 50
        knockback 1
        elements [
            Fire
            Napalm
            Explosion
        ]
    }
}
```

---

### `wp_Garbage`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Garbage {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 0

        effects {
            Poison 1
        }
    }
}
```

---

### `wp_Shotgun`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Shotgun {
    template straightshot_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode direction
        max_aoe 3+bonus_range
        shotgun_mode true

        aoe_mode custom
        custom_aoe [[3, -2][3, -1][3, 0][3, 1][3, 2]]
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        lob_height 0
        speed 25
    }

    self_damage {
        damage 0
        knockback 1
        effects {
            KnockbackDirectionIsFacingDirection flip
        }
    }
    
    damage_instance {
        damage 5
    }
}
```

---

### `wp_Revolver`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Revolver {
    template straightshot_attack

    meta {
        name "{itemname}"
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        speed 25
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {

    }

    
    
    damage_instance {
        damage 1

        effects {
            Instakill 25
        }
    }
}
```

---

### `wp_Sniper`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Sniper {
    template lobbed_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        max_range 20
        min_range 1
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        lob_height 0
        speed 25
    }
    
    
    damage_instance {
        damage 1

        effects {
            Instakill 25
        }
    }
}
```

---

### `wp_GunslingerPistol`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_GunslingerPistol {
    template straightshot_attack

    meta {
        name "{itemname}"
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        speed 25
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode tile
        min_range 1
        max_range 20
        max_aoe 100
    }

    damage_instance {
        damage 10+bonus_ranged_damage
    }
}
```

---

### `IsaacBasicAttack`
**Name:** Cry  
**Description:** Shoot a tear.  
**Source:** `item_abilities.gon`  

```
IsaacBasicAttack {
    template ranged_attack
	
	graphics {
        projectile spitprojectile
    }
    
    meta {
        name "ABILITY_ISAACBASICATTACK_NAME"
        desc "ABILITY_ISAACBASICATTACK_DESC"
        animate_name false
    }

    target {
        min_range 1
        max_range 3+bonus_range
    }

    damage_instance {
        damage 1+bonus_ranged_damage

        elements [
            Water
        ]
    }
}
```

---

### `wp_MonkFist`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MonkFist {
    class CloneAbility
    cloned_ability attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }
}
```

---

### `tk_MonkStyleChange`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_MonkStyleChange {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation none
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            MonkStanceSwitch 1
        }
        ai_base_score 1
        custom_additional_ai_weight prefer_dont_move
    }
}
```

---

### `wp_Spitball`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Spitball {
    template ranged_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 20
    }

    graphics {
        animation shoot
        projectile source_weapon
    }
    
    damage_instance {
        damage 3
        effects {
            Slow 1
        }
        elements [
            Water
        ]
    }
}
```

---

### `wp_PogoStick`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_PogoStick {
    template jump_attack

    meta {
        name "{itemname}"
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_range 4

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none

        always_bounce true
    }

    damage_instance {
        damage 4

        effects {
            IgnoreSelf 1
           // Displace 1
        }
    }
}
```

---

### `wp_MiniJetpack`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MiniJetpack {
    template jump_attack

    meta {
        name "{itemname}"
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_range 20

        aoe_mode occupied_tiles
        aoe_excludes_self false
        restrictions none

        randomize_target_within_range 2
    }

    damage_instance {
        damage 0
        type none
        cant_miss true

        effects {
            ExplosionIfHitSomething 5
            IgnoreSelf true
        }
    }
}
```

---

### `wp_Taser`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Taser {
    template ranged_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        particle Bolt
        animation weaponshoot
    }

    sounds {
        ontrigger SE_WeaponShoot_Taser
    }
    
    target {
        max_aoe 0
        max_range 4
    }
    
    damage_instance {
        damage 5
        
        effects {
            Stun 1
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `wp_AstroTaser`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_AstroTaser {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }

    sounds {
        ontrigger SE_AstroTaserPoke
    }

    damage_instance {
        damage 3+bonus_melee_damage
        
        effects {
            Stun [1 .70]
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `wp_Deathbot`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Deathbot {
    template spawn

    meta {
        name "{itemname}"
    }

    tags [summon]
    
    graphics {
        fall_from_sky true
        animation weaponspell3
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        min_range 1
        max_range 3
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Deathbot
    }

    damage_instance { //this is here so ThrowWeapon will make an explosion
        damage 5
        
        effects {
            HitExplosion 5
        }
    }
}
```

---

### `wp_Crossbow`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Crossbow {
    template ranged_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 20
    }

    graphics {
        animation weaponshoot
    }

    sounds {
        ontrigger SE_WeaponShoot_Crossbow
    }
    
    damage_instance {
        damage 6
        piercing true
        effects {
            Bleed 1
        }
    }
}
```

---

### `wp_BucketOfAcid`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BucketOfAcid {
    template spell

    meta {
        name "{itemname}"
    }

    keyword_tooltips {}
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 1

        min_aoe 0
        max_aoe 0
    }

    graphics {
        animation weaponslam
		projectile AcidshotProjectile
		particle none
    }

	
    damage_instance {
        damage 6

        effects {
            Burn [1 .25]
            Burn [1 .25]
            Burn [1 .25]
            Burn [1 .25]

            Bruise [1 .25]
            Slow [1 .25]
            Stun [1 .1]
            Poison [1 .2]
            Poison [1 .2]
            Bleed [1 .2]
            RandomStatDown [1 .25]
            RandomStatDown [1 .25]
            RandomStatDown [1 .25]
            Weakness [1 .25]
            Blind [1 .25]
            Charmed [1 .1]
            Fear [1 .1]
            Confusion [1 .2]
            Confusion [1 .2]
			ChangeTile GlassTile
        }
    }
}
```

---

### `wp_StunGun`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_StunGun {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }

    damage_instance {
        damage 5
        incidentally_collects_pickups false
        effects {
            Stun [1, .5]
        }

        elements [
            Electric
        ]
    }
}
```

---

### `wp_SlingShot`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SlingShot {
    template ranged_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 20
    }

    graphics {
        animation weaponshoot
    }

    sounds {
        ontrigger SE_WeaponShoot_Slingshot
    }
    
    damage_instance {
        damage 4
        effects {
            Blind [2 .33]
        }
    }
}
```

---

### `wp_Uzi`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Uzi {
    template straightshot_attack

    meta {
        name "{itemname}"
    }

    graphics {
        projectile Bullet
        animation uziShoot
        speed 25
    }
    
    cost {
        mana 0
        cantrip true
    }


    target {
        multihit 5
    }

    /*temporary_effects {
        CastAgain 4
    }*/
    
    damage_instance {
        damage 2
    }
}
```

---

### `wp_22Rifle`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_22Rifle {
    template lobbed_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        max_range 20
        min_range 1
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        lob_height 0
        speed 25
    }
    
    damage_instance {
        damage 12
    }
}
```

---

### `wp_BagOfRocks`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BagOfRocks {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false
        effects {
            Bruise 1
        }
    }
}
```

---

### `wp_Textbook`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Textbook {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		
    }

    graphics {

    }
    
    damage_instance {
        effects {
            IntelligenceUp 1
        }
    }
}
```

---

### `wp_BucketOfLard`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BucketOfLard {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {

    }
    
    damage_instance {
        heal 4
        effects {
            ConstitutionUp 2
            SpeedUp -1
        }
    }
}
```

---

### `wp_NailGun`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_NailGun {
    template straightshot_attack

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponshoot
    }

    sounds {
        ontrigger SE_WeaponShoot_Nailgun
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {

    }
    
    damage_instance {
        damage 1
        piercing true
        effects {
            Thorns 1
        }
    }
}
```

---

### `wp_StrongMagnet`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_StrongMagnet {
    template spell

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
        particle WaterConduct
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_aoe 0
        max_range 6

        knockback_mode target_to_character
        hint_can_target_pickups true
    }
    
    damage_instance {
        damage 0
        knockback 2

        effects {
            CollectsPickups 1
        }

        elements [
            Electric
        ]
    }
}
```

---

### `wp_SawBlades`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SawBlades {
    template straightshot_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 10
        restrictions none
        upgrade_straight_shot_to_piercing true
    }

    damage_instance {
        damage 3

        effects {
            Bleed 1
        }
    }
}
```

---

### `wp_OddRemote`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_OddRemote {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            Metronome 1
        }
    }
}
```

---

### `wp_OddRemoteEnemy`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_OddRemoteEnemy {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            PoolMetronome {
                pool [Shockwave Ping Telefrag Stasis Reduce Zealot]
            }
        }
    }
}
```

---

### `wp_ButterflyKnife`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ButterflyKnife {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponpoke
    }

    temporary_effects {
        Fury 75
    }
    
    damage_instance {
        damage 1
        piercing true
        incidentally_collects_pickups false
        effects {
            Bleed 1
        }
    }
}
```

---

### `wp_BearTraps`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BearTraps {
    template lobbed_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        projectile DamageTrap
        use_rotation false
        animation weaponthrowhigh
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 5

        restrictions must_be_empty
    }

    damage_instance {
        damage 0
        ai_base_score 10
        custom_additional_ai_weight tile_has_no_known_traps
        
        effects {
            SpawnBearTrap 1
        }
    }
}
```

---

### `wp_RustyRazor`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RustyRazor {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 0
        piercing true
        incidentally_collects_pickups false
        effects {
            Bleed 1
            Poison 1
        }
    }
}
```

---

### `wp_Bricks`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Bricks {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    graphics {
        projectile SmallRock
        animation weaponthrowstraight
        projectile source_weapon
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }
    
    target {
        min_range 1
        max_range 3+bonus_range
    }
    
    damage_instance {
        damage 2

        effects {
            Stun 1
            BounceObject SmallRock
        }

        elements [
            Rock
        ]
    }
}
```

---

### `tk_Pawn`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Pawn {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            ForceMoveTowardsEnemies MoveOne
        }
    }
}
```

---

### `tk_Rook`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Rook {
    template move
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        move_points 0
        cantrip true
    }

    target {
        range_mode cross
        max_range 10
        restrictions [must_be_moveable must_move must_have_line_of_sight]
        straight_shot true
    }
}
```

---

### `tk_Queen`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Queen {
    template move
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        move_points 0
        cantrip true
    }

    target {
        range_mode 8cross
        max_range 10
        restrictions [must_be_moveable must_move must_have_line_of_sight]
        straight_shot true
        allow_diagonals true
    }
}
```

---

### `tk_Knight`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Knight {
    template jump_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        jump_attack_animation land
    }

    target { 
        target_mode tile
        range_mode custom
        custom_range [[1 2]]
        range_symmetry eight_way

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        
        range_display_include_character_size true
        restrictions must_be_moveable
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        type none
        damage 0
    }
}
```

---

### `wp_NecroSoulDagger`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_NecroSoulDagger {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponstab
    }

    damage_instance {
        damage 5

        effects {
            Conditional_Ally {
                ApplyToSourceOnKill {
                    TransformWeapon {
                        from Necro_SoulDagger_Uncharged
                        to Necro_SoulDagger_Charged
                    }
                }
            }
            Conditional_PlayerCat {
                ConjureRandomAbilityFromCat 1
            }
        }
    }
}
```

---

### `wp_NecroSoulDaggerCharged`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_NecroSoulDaggerCharged {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponstab
    }

    damage_instance {
        damage 10

        effects {
            Leech 1

            Conditional_PlayerCat {
                ConjureRandomAbilityFromCat 1
            }
        }
    }
}
```

---

### `wp_SpiderWebber`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SpiderWebber {
    template lobbed_attack

    meta {
        name "{itemname}"
    }
	
    graphics {
        animation weaponshoot
		projectile Webball
    }

    sounds {
        ontrigger SE_WeaponShoot_SpiderWebber
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 3
        restrictions none
        knockback_mode zero
    }

    damage_instance {
        damage 0

        effects {
            Webbed 1
        }
    }
}
```

---

### `wp_SleepDart`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SleepDart {
    template straightshot_attack

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 10
        restrictions none
    }

    damage_instance {
        damage 1

        effects {
            Sleep 1
        }
    }
}
```

---

### `wp_Mjolnir`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Mjolnir {
    template straightshot_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponthrowstraight
        speed 10
        projectile source_weapon
        use_rotation_once true
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        max_aoe 5
        upgrade_straight_shot_to_piercing true
        upgrade_straight_shot_to_boomerang true
    }

    bonus_passives {
        CatchBoomerang 1
    }

    damage_instance {
        damage 5
    }

    splash_damage {
        damage 15

        effects {
            VisualFXTile Bolt
        }

        elements [
            Electric
        ]
    }
}
```

---

### `wp_Blackjack`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Blackjack {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false
        effects {
            Stun [1, .05]
        }
    }
}
```

---

### `wp_Blackjack_Auto`
**Source:** `item_abilities.gon`  

```
wp_Blackjack_Auto {
    variant_of wp_Blackjack

    meta {
        is_weapon true
    }
    
    /*self_damage {
        damage 0
        effects {
            DamageWeapon 1
        }
    }*/
}
```

---

### `wp_BigSpring`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BigSpring {
    template throw_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation knockupatk
    }
    
    target {
        max_range 5
    }
    
    damage_instance {
        damage 1
        blocked_damage 5
    }
}
```

---

### `wp_Grenade`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Grenade {
    template spell

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 20
        aoe_mode circle
        min_aoe 0
        max_aoe 3
    }

    graphics {
        animation weaponthrowhigh
        use_projectile true
        projectile source_weapon

        particle Explosion
        delay 2
    }
    
    damage_instance {
        damage 12
        effects {
            PartialPurge 1
            PartialPurge 1
            PartialPurge 1
            PartialPurge 1
            PartialPurge 1
        }
        elements [
            Explosion
        ]
    }
}
```

---

### `wp_Pinwheel`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Pinwheel {
    template spell

    meta {
        name "{itemname}"
    }
    
    graphics {
        particle fx_windSpell
        animation weaponspell
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode direction

        aoe_mode line
        min_aoe 1
        max_aoe 1
    }
    
    damage_instance {
        damage 1
        knockback 1
        
        elements [
            Wind
        ]
    }
}
```

---

### `wp_CrispPaper`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_CrispPaper {
    template ranged_attack

    meta {
        name "{itemname}"
    }

    keyword_tooltips {Bleed 3} // hide secret interaction with burning units
    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }
    
    damage_instance {
        damage 0
        effects {
            Bleed 3
            Conditional_AffectedByElement {
                element Fire
                Burn 2
            }
        }
        type status_spell
    }
}
```

---

### `wp_PurpleMushroom`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_PurpleMushroom {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 0
        effects {
            VisualFXTile PoisonPoof
            Confusion 2
        }
        type status_spell
    }
}
```

---

### `wp_BlackMushroom`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BlackMushroom {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 0
        effects {
            VisualFXTile PoisonPoof
            Weakness 2
        }
        type status_spell
    }
}
```

---

### `wp_RedMushroom`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RedMushroom {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 0
        effects {
            VisualFXTile PoisonPoof
            Charmed 3
        }
        type status_spell
    }
}
```

---

### `wp_PoisonVial`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_PoisonVial {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 0
        effects {
            VisualFXTile PoisonPoof
            Poison 2
        }
        type status_spell
    }
}
```

---

### `wp_PopCap`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_PopCap {
    template spell

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range
        max_aoe 0
        knockback_mode character_to_tile
    }
    
    graphics {
        animation weaponthrowhigh
        use_projectile true
        projectile source_weapon
        particle Explosion
    }
    
    damage_instance {
        damage 2
        knockback 1
        
        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `wp_CreepyPhoto`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_CreepyPhoto {
    template melee_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponspell
    }
    
    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }

    damage_instance {
        damage 0
        incidentally_collects_pickups false
        effects {
            Fear 1
        }
        type status_spell
    }
}
```

---

### `wp_FingerBone`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_FingerBone {
    template straightshot_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation throwobject
        projectile source_weapon
    }
    
    target {
        max_aoe 3+bonus_range
    }
    
    damage_instance {
        damage 0
        effects {
            Immobile 3
        }
        type status_spell
    }
}
```

---

### `wp_SpringBoard`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SpringBoard {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 2
        incidentally_collects_pickups false
        
        effects {
            KnockUpAndAway {
                stacks 5
                distance 3
            }
        }
    }
}
```

---

### `wp_Shovel`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Shovel {
    template melee_spell
    class AOESpellAbility
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponswingup
        particle Earthquake
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        damage 5
        incidentally_collects_pickups false
        

        effects {
            KnockUpAndAway {
                stacks 5+bonus_melee_ability_damage
                distance 2
            }
            BounceObject chapter_corpse_medium
        }

        elements [
            Earth
        ]
    }
}
```

---

### `wp_Trowel`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Trowel {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 0
        knockback 1
        incidentally_collects_pickups false
        
        effects {
            ObjectOnHitEmpty SmallRock
            LeaveBehindRockOnKnockback 1
        }

        elements [
            Earth
        ]
    }
}
```

---

### `wp_StaffOfFlame`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_StaffOfFlame {
    template spell

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }
    
    graphics {
        particle FireSpin
        palette 6
        animation weaponspell3
    }
    
    target {
        max_aoe 0
        max_range 5
    }
    
    damage_instance {
        effects {
            Burn 5
        }
        
        elements [
            Fire
            Napalm
        ]
    }
}
```

---

### `wp_LacedNeedle`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_LacedNeedle {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 0
        incidentally_collects_pickups false
        
        effects {
            Poison 1
        }
    }
}
```

---

### `wp_BattleAxe`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BattleAxe {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        act_points 1
        mana 0
        move_points 1
        charge 0
    }

    graphics {
        animation weaponSpinAttack
    }

    target {
        target_mode none
        aoe_mode square
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 20
    }
}
```

---

### `wp_AnointingOil`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_AnointingOil {
    template targeted_status

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        affected_particle Cleanse
    }
    
    target { 
        min_range 0
        max_range 1
    }

    damage_instance {
        damage 0

        effects {
            Cleanse 0
        }

        elements [
            Holy
        ]
    }
}
```

---

### `wp_Girder`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Girder {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    graphics {
        animation weaponslam
    }

    target {
        max_aoe 2
    }
    
    damage_instance {
        damage 8
        knockback 10
        incidentally_collects_pickups false
        
        effects {
            OverrideChainKnockback 10
        }
    }
}
```

---

### `wp_LilKitty`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_LilKitty {
    template spawn

    meta {
        name "{itemname}"
    }

    tags [summon]
    
    graphics {
        lob true
        bounce_on_hit true
        animation weaponswing
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        min_range 1
        max_range 4+bonus_range
        restrictions none
    }

    spawn {
        object CharmedFlea
    }
}
```

---

### `wp_TractorBeam`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_TractorBeam {
    template spell

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponshoot
        particle MagicMissleBlast
    }

    sounds {
        ontrigger SE_WeaponShoot_TractorBeam
    }

    target {
        max_aoe 0
        max_range 3
        restrictions must_have_line_of_sight
        knockback_mode pull_to_character
        hint_can_target_pickups true
    }

    damage_instance {
        damage 0

        effects {
            CollectsPickups 1
        }
    }
}
```

---

### `wp_RollOfPennies`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RollOfPennies {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        durability 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false

        effects {
            KnockOutCoin {
                stacks 1
                chance .5
            }
            ChanceToBreak 5
        }
    }
}
```

---

### `wp_GrapplingHook`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_GrapplingHook {
    template straightshot_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponthrowstraight

        //projectile source_weapon
        projectile HookProjectile
        chain_movieclip ChainLink
        chain_distance .25
    }
    
    target {
        max_range 10
        target_mode direction8
        hint_can_target_static true
    }

    damage_instance {
        damage 0

        effects {
            PullSourceToTarget 1
        }
    }
}
```

---

### `wp_Chainsaw`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Chainsaw {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponpoke
    }
    
    sounds {
        ontrigger SE_CatWeaponPoke_Chainsaw
    } 
    
    target {
        multihit_min 5
        multihit_max 8
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false

        effects {
            Cleave {
                chance .25
            }
        }
    }
}
```

---

### `tk_BloodyCoin`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_BloodyCoin {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation coinFlip
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        X_is current_health
    }
    
    damage_instance {
        effects {
            RandomStatusFromPool {
                BonusDamage "ceil(X/2)"
                RefreshActPoints 1
            }
        }
    }
}
```

---

### `tk_GlowingCoin`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_GlowingCoin {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation coinFlip
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        X_is current_mana
    }
    
    damage_instance {
        effects {
            ManaGain 0 //this is just so things can identify this as a ManaGain ability
            RandomStatusFromPool {
                ManaGain X
                ManaGain "-ceil(X/2)"
            }
        }
    }
}
```

---

### `tk_ElectricCoin`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_ElectricCoin {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation coinFlip
    }

    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        effects {
            RandomStatusFromPool {
                Slow 2
                RefreshMovePoints 1
            }
        }
    }
}
```

---

### `tk_CounterfeitCoin`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_CounterfeitCoin {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation coinFlip
    }

    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        effects {
            RandomStatusFromPool {
                GainCoins 5
                GainCoins -5
            }
        }
    }
}
```

---

### `tk_Whistle`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Whistle {
    template spawn
    tags [summon]
    
    graphics {
        animation whistle
        fall_from_sky true
    }
    
    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
        once_per_fight true
    }
    
    spawn {
        object [BuffFamiliarFly BuffFamiliarMaggot BuffFamiliarFlea]
    }
}
```

---

### `tk_Metronome`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Metronome {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    tags [musical]
    
    graphics {
        animation metronome
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    damage_instance {
        effects {
            Metronome 2
        }
    }
}
```

---

### `tk_RageJuice`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_RageJuice {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    tags [consumable]
    
    graphics {
        animation drinkTrinket
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    damage_instance {
        effects {
            StrengthUp 4
            SpeedUp 4
            Brace 2
            Madness 999
        }
    }
}
```

---

### `tk_BagOfSeeds`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_BagOfSeeds {
    template targeted_status
    
    meta {
        name "{itemname}"
    }
    
    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_range 3
    }
    
    damage_instance {
        effects {
            ChangeTile {
                tile [TallGrassTile TallFlowerTile BrambleTile]
            }
        }
    }
}
```

---

### `tk_SpellBook`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_SpellBook {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    graphics {
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            ManaGain 10
            ConjureBonusAbility Mage
        }
    }
}
```

---

### `tk_BagOfBags`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_BagOfBags {
    template spawn
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        lob true
        animation throwobject
    }
    
    target {
        min_range 1
        max_range 1
        restrictions [aoe_must_exist]
    }

    spawn {
        object TrashBag
        layer characters
    }
}
```

---

### `tk_Steroids`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Steroids {
    template self_buff
    
    meta {
        name "{itemname}"
    }
    
    keyword_tooltips {Madness 1}

    graphics {
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            PermanentStrength 1
            MadnessChanceOnTurnBegin 2
            NextBattleStatusStacks {
                fights 9999
                MadnessChanceOnTurnBegin 2
            }
        }
    }
}
```

---

### `tk_HolyWater`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_HolyWater {
    template spell

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 3+bonus_range
        min_aoe 0
        max_aoe 1
    }

    graphics {
        animation weaponthrowhigh
        use_projectile true
        projectile source_trinket

        particle HealMed
        delay 1
    }
    
    damage_instance {
        heal 2
        type status_spell

        elements [
            Holy
        ]
    }
}
```

---

### `tk_TankJuice`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_TankJuice {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    graphics {
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
			SpeedUp -1
            Temporary {
                status ChainKnockback
                data 2
                stacks 2
                turns 1
                expires_on_end_turn true
            }
            Temporary {
                status AddKnockbackToEverything
                data 2
                stacks 2
                turns 1
                expires_on_end_turn true
            }
        }
    }
}
```

---

### `tk_HuntersFlute`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_HuntersFlute {
    template spawn
    tags [summon]
    
    meta {
        name "{itemname}"
    }

    target {
        target_mode none
        max_aoe 1
        min_targets 2
        max_targets 3
    }

    graphics {
        animation whistle
        fall_from_sky true
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }
    
    spawn {
        object [CharmedMaggot CharmedMaggot_Champion CharmedPooter CharmedFly CharmedFlea CharmedFlea_Champion CharmedTinySpider CharmedTomTom]
        faction self
    }
}
```

---

### `tk_FriendshipBracelet`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_FriendshipBracelet {
    template melee_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation showTrinket
    }
    
    damage_instance {
        damage 0
        incidentally_collects_pickups false
        effects {
            Conditional_Enemy {
                Conditional_NotBoss {
                    CaptureFamiliar 1
                    FactionConversion 1
                }
            }
        }
        type status_spell
    }
}
```

---

### `tk_CambionConception`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_CambionConception {
    template spawn

    meta {
        name "{itemname}"
    }

    tags [summon]
    
    graphics {
        lob false
        animation shoot
    }
    
    cost {
        mana 0
        cantrip true
        must_not_be_a_summon true
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0
        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object PlayerCat_CambionMiniMe
        faction self
        catdata clone
        clone_items true
        post_spawn_statuses {
            VisualFXTile PoisonPoof
        }
    }
}
```

---

### `tk_EmptyHand`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_EmptyHand {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation brace
    }
    
    bonus_passives {
        XIsFreeArmorSlots 1
    }

    target {
        X_is custom
    }
    
    damage_instance {
        effects {
            Shield 3*X
        }
    }
}
```

---

### `tk_Fireworks`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Fireworks {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation showTrinket
    }
    
    damage_instance {
        effects {
            RandomMagicMissile 5
        }
    }
}
```

---

### `tk_SackOfMeat`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_SackOfMeat {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    tags [consumable]
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation eatTrinket
    }
    
    damage_instance {
        heal 4
    }
}
```

---

### `tk_DruidsWhistle`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_DruidsWhistle {
    template spawn
    tags [summon]
    
    meta {
        name "{itemname}"
    }
    
    graphics {
        animation whistle
        fall_from_sky true
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }
    
    spawn {
        object RandomDruidFamiliar
        redirect_location_if_blocked true
        faction self
    }
}
```

---

### `wp_BurningCoal`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BurningCoal {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }
    
    damage_instance {
        damage 2
        effects {
            Burn 2
            SpeedUp 2
        }
        
        elements [
            Fire
            Napalm
        ]
    }
}
```

---

### `wp_RainbowRemote`
**Source:** `item_abilities.gon`  

```
wp_RainbowRemote {
    template spell

    meta {
        animate_name false
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 4
        min_aoe 0
        max_aoe 0
    }

    graphics {
        particle none
        animation weaponspell3
    }
    
    damage_instance {
        effects {
            TargetedMetronome 20
        }
    }
}
```

---

### `wp_RubberBat`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RubberBat {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 0
        incidentally_collects_pickups false
        effects {
            KnockbackDirectionIsFacingDirection rotate_right
            FaceAway 1
            Confusion 1
        }
    }
}
```

---

### `wp_RustedRod`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RustedRod {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage "durability"
        incidentally_collects_pickups false
    }
}
```

---

### `wp_MeatCleaver`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MeatCleaver {
    template melee_attack

    meta {
        name "{itemname}"
        icon_damage_display "?"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponslam
    }
    
    damage_instance {
        damage 5
        incidentally_collects_pickups false

        effects {
            Conditional_Boss {
                XIsTargetHealth {
                    BonusDamage "max(0, floor(X/6)-1)"
                }
            } Else {
                XIsTargetHealth {
                    BonusDamage "max(0, floor(X/2)-1)"
                }
            }
            Cleave 1
        }
    }
}
```

---

### `wp_SharpStraw`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SharpStraw {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }

    damage_instance {
        damage 1
        incidentally_collects_pickups false

        effects {
            ApplyToSourceOnKill {
                HealthGain 10
            }
        }
    }
}
```

---

### `wp_BagOfGlass`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BagOfGlass {
    template lobbed_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        durability 0
        cantrip true
    }

    target {
        min_range 1
        max_range 1
    }

    graphics {
        animation throwobject
        projectile GlassBall
    }

    damage_instance {
        damage 1

        effects {
            ChangeTile GlassTile
            ChanceToBreak 5
        }
    }
}
```

---

### `wp_BagOfMeat`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BagOfMeat {
    template spawn
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        durability 0
        cantrip true
    }

    graphics {
        lob true
        animation throwobject
    }
    
    target {
        min_range 1
        max_range 1
        restrictions [aoe_must_exist]
    }

    spawn {
        object Food
        layer pickups
    }

    self_damage {
        effects {
            ChanceToBreak 5
        }
    }
}
```

---

### `wp_BagOfGlitter`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BagOfGlitter {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        durability 0
        cantrip true
    }

    graphics {
        animation throwobject
    }

    damage_instance {
        damage 0
        incidentally_collects_pickups false

        effects {
            Blind 2
            ChanceToBreak 5
        }
    }
}
```

---

### `wp_BagOfStuff`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BagOfStuff {
    template spawn
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        durability 0
        cantrip true
    }

    graphics {
        lob true
        animation throwobject
    }
    
    target {
        min_range 1
        max_range 1
        restrictions [aoe_must_exist]
    }

    spawn {
        object RandomPickup
        layer pickups
    }

    self_damage {
        effects {
            ChanceToBreak 5
        }
    }
}
```

---

### `wp_Pickaxe`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Pickaxe {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }

    damage_instance {
        damage 2
        piercing true
        incidentally_collects_pickups false
        
        effects {
            VaporizeInanimate 1

            Conditional_Object {
                RepairWeapon 1
                Conditional_HasTag {
                    tag rock
                } Else {
                    CanApplyToInanimate {
                        BreakIntoRocks SmallRock
                    }
                }
            }
        }

        elements [
            Earth
        ]
    }
}
```

---

### `tk_Technology`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Technology {
    template laser
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
        delay 5
        
        beam_clip thinlaser
        beam_cap thinlasercap
        mask_center SpearMaskCenter
        mask_extent SpearMaskExtent
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    damage_instance {
        damage 4
    }


}
```

---

### `tk_RedDrink`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_RedDrink {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    tags [consumable]
    
    graphics {
        animation drinkTrinket
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    damage_instance {
        heal 5
    }
}
```

---

### `tk_GreenDrink`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_GreenDrink {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    tags [consumable]
    
    graphics {
        animation drinkTrinket
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    damage_instance {
        effects {
            ManaGain 5
        }
    }
}
```

---

### `tk_PurpleDrink`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_PurpleDrink {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    tags [consumable]
    
    graphics {
        animation drinkTrinket
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    damage_instance {
        heal 2
        effects {
            Shield 1
            ManaGain 2
        }
    }
}
```

---

### `tk_LilBattery`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_LilBattery {
    template targeted_status

    meta {
        name "{itemname}"
    }
    
    graphics {
        affected_particle fx_ManaHeal
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
        once_per_fight true
        can_be_refreshed false
    }

    target {
        min_range 0
        max_range 1
    }

    damage_instance {
        effects {
            RefreshOncePerFightAbilities 1
        }
        elements [
            Electric
        ]
    }
}
```

---

### `tk_CarvingKnife`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_CarvingKnife {
    template self_buff
    
    meta {
        name "{itemname}"
    }
    
    graphics {
        animation selfHarm
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        damage 2
        effects {
            Cleave 1
        }
    }
}
```

---

### `tk_RazorBlade`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_RazorBlade {
    template self_buff
    
    meta {
        name "{itemname}"
    }
    
    graphics {
        animation selfHarm
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        damage 5
        effects {
            StrengthUp 2
            DexterityUp 2
        }
    }
}
```

---

### `tk_Teleport`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Teleport {
    template teleport
    
    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    target {
        max_range 20
    }
}
```

---

### `tk_WeirdEgg_Spawn`
**Source:** `item_abilities.gon`  

```
tk_WeirdEgg_Spawn {
    template spawn

    meta {
    }

    tags [summon]
    
    graphics {
        lob true
        animation none
        dont_orient true
    }
    
    target {
        target_mode random_closest_tile
        min_range 1
        max_range 1
    }

    spawn {
        object [FamiliarFetus FamiliarFetus FamiliarFetus FamiliarFetus FamiliarBrainDrain FamiliarKirbyFetus]
        additional_passives {
            CaptureFamiliar 1
        }
    }

}
```

---

### `tk_CatONineTails`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_CatONineTails {
    template self_buff
    
    meta {
        name "{itemname}"
    }
    
    graphics {
        animation attack
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        damage 1
        effects {
            PartialCleanse 9999
        }
    }
}
```

---

### `tk_Glue`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Glue {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    tags [consumable]
    
    graphics {
        animation drinkTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            IntelligenceUp -1
            Confusion 2
            DodgeChance_Status 20
        }
    }
}
```

---

### `tk_MyShadow`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_MyShadow {
    template move
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        move_points 0
        cantrip true
    }

    target {
        range_mode cross
        max_range 3
        restrictions [must_be_moveable must_move must_have_line_of_sight]
        straight_shot true
    }
    
    temporary_effects {
        AfterImage {
            object PlayerCat_ThiefShade
            skilltemp true
        }
    }
}
```

---

### `tk_EggSack`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_EggSack {
    template spawn

    meta {
        name "{itemname}"
    }

    tags [summon]
    
    graphics {
        lob true
        animation throwobject
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_aoe 2

        min_range 1
        max_range 4+bonus_range

        aoe_chance .33
        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object CharmedTinySpider
    }
}
```

---

### `tk_GorgonsEye`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_GorgonsEye {
    template spell
    
    meta {
        name "{itemname}"
    }
    
    graphics {
        animation showTrinket
		particle none
    }

    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_aoe 4
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0

        effects {
            Petrify 1
        }
    }
}
```

---

### `tk_HotLunch`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_HotLunch {
    template spawn
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        lob true
        animation throwobject
    }
    
    target {
        min_range 1
        max_range 1
        restrictions [aoe_must_exist]
    }

    spawn {
        object Food
        layer pickups
        
        post_spawn_statuses {
            DoDamage {
                damage 0
                type spell
                damage_tiles all

                effects {
                    ChangeTile FireTile
                    VisualFXTile BurnTrigger
                }
                elements [
                    Fire
                ]
            }
        }
    }
}
```

---

### `tk_ButterBean`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_ButterBean {
    template melee_attack

    meta {
        name "{itemname}"
    }

    graphics {
        animation none
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        damage 0
        type none
    }

    self_damage {
        damage 0
        type none

        effects {
            Conditional_GoodRoll {
                odds 10%
                ImmediateUseAbility tk_ButterBean_Mega
            }
            Else {
                ImmediateUseAbility tk_ButterBean_Normal
            }
        }
    }
}
```

---

### `tk_ButterBean_Normal`
**Source:** `item_abilities.gon`  

```
tk_ButterBean_Normal {
    template melee_attack

    meta {
        is_trinket true
    }

    graphics {
        animation poopfart
    }

    damage_instance {
        damage 0
        knockback 1
        type spell
        
        effects {
            Knockback 1
            VisualFXTile PoisonPoof
        }
    }
}
```

---

### `tk_ButterBean_Mega`
**Source:** `item_abilities.gon`  

```
tk_ButterBean_Mega {
    template spell

    meta {
        is_trinket true
    }

    graphics {
        animation fartoom
        particle none
    }

    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 1

        aoe_considers_character_size true
        aoe_excludes_self true
    }

    damage_instance {
        damage 0
        knockback 10

        effects {
            BonusKnockbackDamage 2
        }

        elements [
            Explosion
        ]
    }
}
```

---

### `tk_LunchBox`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_LunchBox {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    tags [consumable]
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation drinkTrinket
    }
    
    damage_instance {
        heal 5
    }
}
```

---

### `tk_Checkers`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Checkers {
    template jump_attack

    meta {
        name "{itemname}"
    }

    graphics {
        jump_attack_animation land
    }
    
    cost {
        mana 0
        move_points 0
        cantrip true
    }

    target {
        range_mode diagcross
        max_range 2
        restrictions [must_be_moveable must_move must_have_line_of_sight]
        straight_shot true
        allow_diagonals true
        
        aoe_mode custom
        custom_aoe [ [-1, -1] ]
        min_aoe 1
        max_aoe 1
        
        aoe_considers_character_size true
        aoe_excludes_self true
    }

    damage_instance {
        damage 4
    }
}
```

---

### `tk_Bishop`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Bishop {
    template move
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        move_points 0
        cantrip true
    }

    target {
        range_mode diagcross
        max_range 10
        restrictions [must_be_moveable must_move must_have_line_of_sight]
        straight_shot true
        allow_diagonals true
    }
}
```

---

### `tk_PetrifiedPinky`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_PetrifiedPinky {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation brace
        particle HealBig
    }
    
    damage_instance {
        effects {
            HealTo 50%
            DestroyTrinket 1
        }
    }
}
```

---

### `tk_EstusFlask`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_EstusFlask {
    template self_buff

    meta {
        name "{itemname}"
    }

    tags [consumable]
    
    graphics {
        animation drinkTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        heal 5
    }
}
```

---

### `wp_RocketLauncher`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RocketLauncher {
    template spell

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 20

        min_aoe 0
        max_aoe 2
    }

    graphics {
        animation weaponshoot
        use_projectile true
        projectile Projectile_Rocket

        rocket_swirl {
            speed [1.5, 2.5] //random range of rotations per second
            radius [.5 1]
        }
        easing 1 // ease in

        lob_height 5

        particle Explosion
    }
    
    damage_instance {
        damage 10
        knockback 1
        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `wp_ThrobbingGristle`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ThrobbingGristle {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }

    damage_instance {
        damage 6
        incidentally_collects_pickups false
        effects {
            SpawnThingIfHitKills Food
        }
    }
}
```

---

### `wp_ScaldingOrb`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ScaldingOrb {
    template spell

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 20

        min_aoe 0
        max_aoe 1

        restrictions [must_have_player_cat must_have_living_character must_target_cat_with_empty_or_destructible_weapon_slot]
    }

    graphics {
        animation weaponthrowhigh
        use_projectile true
        projectile source_weapon
        uncatchable true //on graphics so the Projectile has this data, so CatchProjectiles doesnt block the "transfer weapon" effect

        center_particle None
        area_particle BurnTrigger
        delay 1
        palette 6
    }

    damage_instance {
        damage 0
        cant_miss true
        hit_animation_alt catch
        force_play_hit_animation true

        effects {
            ForceTransferWeapon 1
        }
    }
    
    splash_damage {
        damage 0
        force_play_hit_animation true

        effects {
            Burn 3
        }

        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `wp_BlackShard`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BlackShard {
    template melee_spell
    
    meta {
        name "{itemname}"

        icon_shell_frame "attack"
        icon_damage_display_eq item_aux
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    graphics {
        animation weaponAbsorb
        particle none
    }

    target {
        restrictions [must_have_animate_character must_have_living_character aoe_must_exist]
        aoe_restrictions must_have_low_health_character
        low_health_character_threshold item_aux
    }

    damage_instance {
        damage 0
        incidentally_collects_pickups false

        effects {
            OverrideDamage 0
            Conditional_Corpse {
            } Else {
                Conditional_HealthThreshold {
                    threshold_expr item_aux

                    ApplyToSource {
                        AddWeaponAux 1
                    }
                    Vaporize 1
                }

                Conditional_HasTag {
                    tag the_coven

                    ApplyToSourceOnKill {
                        CompleteItemQuest BlackShard
                        RemoveItem BlackShard
                        RemoveItem BlackShard_Glowing //edge case where this upgrades when you kill it
                    }
                }
            }
        }
    }
}
```

---

### `wp_BlackShard_Glowing`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BlackShard_Glowing {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    graphics {
        animation weaponAbsorb
    }

    damage_instance {
        damage 5
        incidentally_collects_pickups false

        effects {
            Leech 1
            Purge 0
            Burn 5

            Conditional_HasTag {
                tag the_coven

                Vaporize 1
                ApplyToSourceOnKill {
                    CompleteItemQuest BlackShard
                    RemoveItem BlackShard_Glowing
                }
            }
        }
    }
}
```

---

### `wp_PersuasionDevice`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_PersuasionDevice {
    template melee_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    graphics {
        animation weaponslam
    }
    
    damage_instance {
        damage 2
        incidentally_collects_pickups false
        effects {
            Conditional_Enemy {
                Conditional_NotBoss {
                    CaptureFamiliar 1
                    FactionConversion 1
                }
            }
        }
    }
}
```

---

### `tk_SuckStone`
**Source:** `item_abilities.gon`  

```
tk_SuckStone { //this one is triggered automatically and not manually castable
    template targeted_status

    graphics {
        animation showTrinket
    }

    target {
        aoe_mode all
        target_mode none
        aoe_restrictions allies_only
    }
    
    damage_instance {
        effects {
            ManaSteal 5
        }
    }
}
```

---

### `face_FartFace`
**Source:** `item_abilities.gon`  

```
face_FartFace {
    template spell

    graphics {
        animation shoot
        particle PoisonPoof
    }
    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
    }

    damage_instance {
        damage 0
        type status_spell
        effects {
            Poison 1
        }
    }
}
```

---

### `face_FartFaceFixed`
**Source:** `item_abilities.gon`  

```
face_FartFaceFixed {
    variant_of face_FartFace

    target {
        aoe_restrictions exclude_allies
    }
}
```

---

### `head_SpiderInjector`
**Source:** `item_abilities.gon`  

```
head_SpiderInjector {
    template lobbed_attack

    graphics {
        animation throwobject
        projectile Spidershot
    }
    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions allies_only
    }

    damage_instance {
        damage 0
        type status_spell
        effects {
            SpiderInfested 4
        }
    }
}
```

---

### `head_SpiderInjectorFixed`
**Source:** `item_abilities.gon`  

```
head_SpiderInjectorFixed {
    variant_of head_SpiderInjector

    target {
        aoe_restrictions enemies_only
    }

    damage_instance {
        damage 0
        type status_spell
        effects {
            SpiderInfested 1
        }
    }
}
```

---

### `wp_PartyDetonator`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_PartyDetonator {
    template spell
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
        particle none
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    target {
        target_mode random_tile
        min_range 1
        max_aoe 0
        max_range 20

        restrictions [must_have_living_character]
    }

    damage_instance {
        damage 0
        cant_miss true
        effects {
            Conditional_Boss {
                BonusDamage 25
                VisualFX PartyExplosion
                ExplodeCharacter_PartyBoss 5
            } Else {
                Instakill 25
            }
        }
    }
}
```

---

### `wp_PartyDetonatorFixed`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_PartyDetonatorFixed {
    template spell

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
        particle none
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    target {
        target_mode tile
        min_range 1
        max_aoe 3
        max_range 20

        max_targets 1

        restrictions none
        aoe_restrictions must_have_living_character
        aoe_display_exclude_restrictions true
    }

    damage_instance {
        damage 0
        cant_miss true
        effects {
            Conditional_Boss {
                BonusDamage 25
                VisualFX PartyExplosion
                ExplodeCharacter_PartyBoss 5
            } Else {
                ExplodeCharacter_Party 5
            }
        }
    }
}
```

---

### `face_EatNeverstone`
**Name:** Mmmm... Yummy Neverstone  
**Source:** `item_abilities.gon`  

```
face_EatNeverstone {
    template self_buff

    meta {
        name "ABILITY_EATNEVERSTONE_NAME"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation eatTrinket
    }

    bonus_passives {
        AbilityEnabledIfSpecificItemEquipped Neverstone
    }
    
    damage_instance {
        heal 8
        effects {
            AllStatsUp 2
            DestroyTrinket 1
        }
    }
}
```

---

### `wp_FreyedWires`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_FreyedWires {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 4
        type spell
        
        effects {
            ArcLightning {
                stacks 100
                enemies_only false
                ignore_self true
                max_distance 1
            }
            VisualFX WaterConduct
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `wp_OldExtinguisher`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_OldExtinguisher {
    template spell

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    graphics {
        particle fx_windSpell
        delay 10
        animation weaponspell
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 3
    }
    
    damage_instance {
        damage 1

        effects {
            Knockback 5
        }
        
        elements [
            Wind
            Water
        ]
    }
}
```

---

### `wp_TrashCanLid`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_TrashCanLid {
    template melee_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 0
        knockback 1
        incidentally_collects_pickups false
    }
}
```

---

### `wp_MiniNuke`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MiniNuke {
    template spell

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 20
        aoe_mode circle
        min_aoe 0
        max_aoe 4
    }

    graphics {
        animation weaponthrowhigh
        use_projectile true
        projectile source_weapon

        particle Explosion
        delay 1
    }
    
    damage_instance {
        damage 10
        effects {
            Poison 2
            ChangeTile {
                chance 25%
                tile ToxicTile
            }
        }
        elements [
            Fire
            Explosion
            Mutate
            Poison
        ]
    }
}
```

---

### `wp_Kandarian`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Kandarian {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 10
        incidentally_collects_pickups false
        crit_chance 100%

        effects {
            Bleed 10
        }
    }
}
```

---

### `wp_Geode`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Geode {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        durability 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false

        effects {
            ChanceToBreak 5
        }
    }
}
```

---

### `wp_Rocks`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Rocks {
    template lobbed_attack

    meta {
        name "{itemname}"
    }
    
    tags [weapon_throw]

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 2
    }
}
```

---

### `wp_ExtraLimb`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ExtraLimb {
    class CloneAbility
    cloned_ability attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
        can_self_refresh false
    }
}
```

---

### `wp_GripTrainer`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_GripTrainer {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    graphics {
        // TODO: placeholder, need trinket-like animations for weapons
        animation equipWeapon
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            StrengthUp 1
            CatPartsSizeScaleStatus {
                arm1 1.1
                arm2 1.1
            }
        }
    }
}
```

---

### `wp_ShoeHorn`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ShoeHorn {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    graphics {
        animation equipWeapon
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            SpeedUp 2
        }
    }
}
```

---

### `wp_Cheese`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Cheese {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    graphics {
        animation gulp
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        heal 2

        effects {
            ConstitutionUp 1
            CatPartsSizeScaleStatus {
                body 1.1
            }
        }
    }
}
```

---

### `wp_LipFiller`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_LipFiller {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    graphics {
        animation equipWeapon
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            CharismaUp 1
            ManaGain 2
            CatPartsSizeScaleStatus {
                mouth 1.1
            }
        }
    }
}
```

---

### `wp_EnergyDrink`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_EnergyDrink {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    graphics {
        animation none
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            DexterityUp 1
			SpeedUp 1
        }
    }
}
```

---

### `wp_CatPaw`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

**Localization Strings:**
- `COMBAT_POPUP_RELOAD`: "Reload"

```
wp_CatPaw {
    template melee_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 4
        incidentally_collects_pickups false
    }
    
    self_damage {
        damage 0
        effects {
            Conditional_GoodRoll {
                odds 25%
                RefreshWeaponAbility 1
                ShowText "COMBAT_POPUP_RELOAD"
            }
        }
    }
}
```

---

### `wp_FlowerMix`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_FlowerMix {
    template spell

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponpoke
        particle none
    }
    
    target {
        min_range 1
        max_range 3+bonus_range

        min_aoe 0
        max_aoe 2
    }

    damage_instance {
        damage 0
        elements [
            Bloom
        ]
    }
}
```

---

### `wp_PuzzleBox`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_PuzzleBox {
    template straightshot_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        max_range 10
        target_mode none
        //aoe_mode square

        aoe_mode custom
        aoe_symmetry four_way
        custom_aoe [[1, 0] [1, 1]]

        knockback_mode pull_to_character
    }

    graphics {
        animation weaponspell3
        projectile HookProjectile
        chain_movieclip ChainLink
        chain_distance .25
    }
    
    damage_instance {
        damage 0

        effects {
            CollectsPickups 1
            Bleed 1
        }
    }
}
```

---

### `wp_Crowbar`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Crowbar {
    template melee_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 2
        incidentally_collects_pickups false

        effects {
            Conditional_HasTag {
                tag container
                EventBounty 5
                ScatterRandomPickups 5
                Die 1
                VaporizeCorpse 1
            }
        }
    }
}
```

---

### `wp_FireFlower`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_FireFlower {
    template spell

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics { 
        use_projectile true
        animation weaponspell
        projectile FireBallProjectile
        center_particle FireBlastMushroom
        area_particle FireBlastSmall
        palette 6
    }

    target {
        max_aoe 1
        max_range 3
    }
    
    damage_instance {
        damage 3
        
        effects {
            Burn 2
        }
        
        elements [
            Fire
        ]
    }
}
```

---

### `wp_HolyWater`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_HolyWater {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 4+bonus_range
        max_aoe 1
    }

    graphics {
        animation weaponthrowhigh
        single_projectile true
        projectile source_weapon
    }
    
    damage_instance {
        damage 7

        effects {
            ContextualHeal 1
            VisualFXTile HealBig
        }

        elements [
            Holy
            Water
        ]
    }
}
```

---

### `wp_Bible`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Bible {
    template melee_attack

    meta {
        name "{itemname}"
    }

    keyword_tooltips {}

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Conditional_HasStatus {
                status Undead
                Fear 1
            }
            Else {
                PartialCleanse 1
            }
        }
    }
}
```

---

### `wp_CarBattery`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_CarBattery {
    template melee_attack

    meta {
        name "{itemname}"
    }

    target {
        X_is is_at_max_mana
    }
    
    cost {
        mana 0
        cantrip true
        cant_cast 1-X
    }

    graphics {
        particle Bolt
        animation weaponswing
    }
    
    damage_instance {
        damage 5
        
        effects {
            ArcLightning {
                stacks 100
                chance .5
                enemies_only true
                max_distance 3
            }
            VisualFX WaterConduct
        }
        elements [
            Electric
        ]
    }
}
```

---

### `wp_ModelingClay`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ModelingClay {
    template lobbed_attack

    meta {
        name "{itemname}"
    }
    
    tags [weapon_throw]

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 2
    }
}
```

---

### `wp_CaveCatClub`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_CaveCatClub { //for a miniboss enemy
    template melee_attack

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponswing
    }
    
    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        damage 5+bonus_melee_damage
        incidentally_collects_pickups false

        knockback 10

        effects {
            Stun [1 .5]
        }
    }
}
```

---

### `wp_PharaohStaff`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_PharaohStaff {
    template spawn
    tags [summon]
    
    graphics {
        animation weaponspell3
        fall_from_sky true
    }

    meta {
        name "{itemname}"
    }
    
    target {
        target_mode none
        max_aoe 2
        min_targets 2
        max_targets 5
    }

    cost {
        cantrip true
        mana 0
    }
    
    spawn {
        object [CharmedFly]
    }
}
```

---

### `wp_SignalAmplifierSpawnTerminator`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SignalAmplifierSpawnTerminator {
    template spawn
    tags [summon]
    
    graphics {
        animation weaponspell3
        fall_from_sky true
        dont_visualize_ai true
        dont_orient true
    }

    meta {
        name "{itemname}"
    }
    
    target {
        target_mode tile
        max_range 5
        allow_any_orientation true
    }

    cost {
        cantrip true
        mana 0
    }
    
    spawn {
        object [
            TankCat_Terminator 
            MageCat_Terminator 
            HunterCat_Terminator 
            ThiefCat_Terminator 
            MedicCat_Terminator 
            FighterCat_Terminator

            NecroCat_Terminator
            TinkererCat_Terminator
            ButcherCat_Terminator
            PsychicCat_Terminator
            DruidCat_Terminator
            MonkCat_Terminator

            JesterCat_Terminator
            Pebbles_Terminator
        ]

        faction solitary_enemies
        first_turn initiative
        
        additional_passives {
            PermanentMadness 1
        }
        ai_base_score 999999
    }
}
```

---

### `wp_SignalAmplifier`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SignalAmplifier {
    template targeted_status
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
        particle Bolt
    }
    
    cost {
        cantrip true
        mana 0
    }

    target {
        target_mode none
        aoe_mode all
        aoe_restrictions [must_have_tag]
        target_requires_tag robot
        aoe_excludes_self true
        restrictions aoe_must_exist
    }

    self_damage {
        effects {
            AllStatsUp 1
        }
    }
    
    damage_instance {
        damage 5

        elements [
            Electric
        ]
    }
}
```

---

### `wp_InfinityArrow`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_InfinityArrow {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponspell3
    }
    
    damage_instance {
        effects {
            NextAttackBonusRange 5
            NextBasicAttackCritsThisTurn {
                stacks 1
                cant_miss true
                piercing true
            }
        }
    }
}
```

---

### `wp_BentSpoon`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BentSpoon {
    template spell

    meta {
        name "{itemname}"
    }
    
    graphics {
        particle MagicMissleBlast
        animation psyAttack3
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_aoe 0
        max_range 20

        knockback_mode target_to_character
    }
    
    damage_instance {
        damage 1
        knockback 1

        elements [
            Gravity
        ]
    }
}
```

---

### `wp_UnderworldStaff`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_UnderworldStaff {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 1
        knockback 1
        incidentally_collects_pickups false
    }
}
```

---

### `wp_Bo`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Bo {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    temporary_effects {
        Trample 1
    }

    damage_instance {
        damage 1
        effects {
            ApplyToSource {
                KnockUpAndAway {
                    stacks 1
                    distance 2
                    height 0
                }
            }
        }

        incidentally_collects_pickups false
    }
}
```

---

### `wp_BallPeenHammer`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

**Localization Strings:**
- `COMBAT_POPUP_REPAIRED`: "Repaired"

```
wp_BallPeenHammer {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    target {
        min_range 0
    }

    damage_instance {
        damage 1
        effects {
            Conditional_Ally {
                OverrideDamage 0
                RepairAll 1
                ShowText "COMBAT_POPUP_REPAIRED"

                ChanceToBreak 5%
            }
        }
        incidentally_collects_pickups false
    }
}
```

---

### `wp_ButchersCleaver`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ButchersCleaver {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    target { 
        target_mode direction8 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable //TODO: MAKE THIS WORK PROPERLY IF ENLARGED
    }

    damage_instance {
        damage 2
        effects {
            Cleave 1
        }

        incidentally_collects_pickups false
    }
}
```

---

### `tk_TarotDeck`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_TarotDeck {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    graphics {
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            ConjureSingleUseBonusAbility random
        }
    }
}
```

---

### `wp_RainStaff`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RainStaff {
    template spell
    
    meta {
        name "{itemname}"
    }
    
    graphics {
        particle Wave
        animation weaponspell3
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        knockback_mode zero
        max_range 20
        max_aoe 2
        aoe_mode circle
    }
    
    damage_instance {
        effects {
            ChangeTile {
                tile WaterTile
            }
        }
        
        elements [
            Water
        ]
    }
}
```

---

### `wp_SlagMight`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SlagMight {
    template melee_attack

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponswing
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    damage_instance {
        damage 10
        knockback 5

        incidentally_collects_pickups false

        effects {
            Bruise 1
        }
    }
}
```

---

### `wp_MetalRod`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MetalRod {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation headbutt
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        damage 4
        knockback 1
        incidentally_collects_pickups false

        effects {
            Stun [1, .1]
        }
    }
}
```

---

### `wp_MomsToeNail`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MomsToeNail {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponswing
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        damage 2
        incidentally_collects_pickups false
    }
}
```

---

### `wp_AirHorn`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_AirHorn {
    template spell
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell
        particle none
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        knockback_mode tile_to_character
    }
    
    sounds {
        oncastpoint AirHorn
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            FaceAway 1
        }
    }
}
```

---

### `wp_AirHornFixed`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_AirHornFixed {
    template targeted_status

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponspell
    }
    
    target { 
        min_range 0
        max_range 5
        restrictions [must_have_line_of_sight]
    }

    sounds {
        oncastpoint AirHorn
    }


    damage_instance {
        damage 0

        effects {
            Madness 1
        }
    }
}
```

---

### `wp_TheLonerAuto`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_TheLonerAuto {
    class MultiTargetRangedAttackAbility
    template lobbed_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode none
        aoe_mode all
        aoe_excludes_self true
        restrictions aoe_must_exist
        aoe_restrictions [allies_only]
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        lob_height 0
        speed 25
        face_targets true
    }
    
    damage_instance {
        damage 1

        effects {
            Instakill 25
        }
    }
}
```

---

### `wp_TheLoner`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_TheLoner {
    template ranged_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        max_range 20
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        lob_height 0
        speed 25
    }
    
    damage_instance {
        damage 5
    }
}
```

---

### `wp_TheLonerFixed`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_TheLonerFixed {
    template ranged_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        requires_reload true
        start_reloaded true
    }

    target {
        max_range 20
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        lob_height 0
        speed 25
    }

    bonus_passives {
        ReloadOnAllyDies 1
    }
    
    damage_instance {
        damage 5
    }
}
```

---

### `wp_GlassCannon`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_GlassCannon {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponshoot
        projectile GlassBall
    }

    sounds {
        ontrigger SE_WeaponShoot_GlassCannon
    }
    
    damage_instance {
        damage 1

        effects {
            ChangeTile GlassTile
        }
    }
}
```

---

### `wp_GlassCannonFixed`
**Source:** `item_abilities.gon`  

```
wp_GlassCannonFixed {
    variant_of wp_GlassCannon

    target {
        max_range 20
    }
}
```

---

### `wp_BubbleBoyFixed`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BubbleBoyFixed {
    template straightshot_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponspell
        projectile bubbleshot
        speed 2

        rocket_swirl {
            speed [.25, 1.0] //random range of rotations per second
            radius [.25 .5]
        }
    }
    
    target {
        max_aoe 3+bonus_range
    }
    
    damage_instance {
        damage 0
        knockback 1
        effects {
            Confusion 1
        }
        elements [
            Wind
            Water
        ]
    }
}
```

---

### `wp_StopwatchFixed`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_StopwatchFixed {
    template targeted_status

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponspell
    }
    
    target { 
        min_range 0
        max_range 3
    }

    damage_instance {
        damage 0

        effects {
            TakeBonusTurnWithAIControl {
                include_spells true
            }
        }
        ai_base_score -99999 //AI shouldn't cast this lol
    }
}
```

---

### `tk_MadGhost_Spawn`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_MadGhost_Spawn {
    template spawn

    meta {
        name "{itemname}"
    }

    tags [summon]
    
    graphics {
        lob true
        animation none
        dont_orient true
    }
    
    target {
        target_mode random_tile
        min_range 1
        max_aoe 0
        max_range 20
        aoe_restrictions [exclude_blocking]
    }

    spawn {
        object CharmedSpookie
        additional_passives {
            PermanentMadness 1
        }
    }
}
```

---

### `wp_NuclearKnife`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_NuclearKnife {
    template melee_attack

    meta {
        name "{itemname}"
        icon_shell_frame attack
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        raw_damage item_aux

        effects {
            ApplyToSourceOnKill {
                WeaponAuxMultiplier .5
            }
        }
    }
}
```

---

### `wp_NuclearKnifeExplode`
**Source:** `item_abilities.gon`  

```
wp_NuclearKnifeExplode {
    template spell

    graphics {
        particle Explosion
        animation weaponspell3
        delay 5
        visual_delay_but_simultaneous_damage 10
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode none
        max_aoe 2
    }

    damage_instance {
        damage 50
        piercing true
        cant_miss true
        elements [
            Fire
            Explosion
        ]
        effects {
            Vaporize 1
        }
    }
    splash_damage {
        damage 50
        knockback 2
        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `wp_NuclearKnifeFixed`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_NuclearKnifeFixed {
    template spell

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponshoot
        use_projectile true
        projectile Projectile_Rocket
		center_particle NukeBlastLarge
		
        speed 20
        lob_height 3

        particle none
        delay 3
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode tile
        max_aoe 20
        max_range 20
    }

    damage_instance {
        damage 40
        elements [
            Fire
            Explosion
            Mutate
        ]

        effects {
            ChanceToBreak 20
        }
    }
    splash_damage {
        damage 20
        elements [
            Fire
            Explosion
            Mutate
        ]
    }
}
```

---

### `wp_AlienBlaster`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_AlienBlaster {
    template laser

    meta {
        name "{itemname}"
    }
    
    graphics {
        use_projectile_spawn_offset true
        animation weaponshoot
        visual_delay_but_simultaneous_damage 0
		
		beam_clip greenlaser
        beam_cap greenlasercap
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        target_mode direction
        aoe_mode line
        max_aoe 10
        aoe_excludes_self true
    }
    
    self_damage {
        effects {
            LateStatusApplication {
                CurrentWeaponDamageUp 1
            }
        }
    }

    damage_instance {
        damage 1
    }
}
```

---

### `tk_JarOfRadiation`
**Source:** `item_abilities.gon`  

```
tk_JarOfRadiation {
    template spell

    graphics {
        particle none
		animation psyMegaAttack
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
    }

    self_damage {
        effects {
            DoDistortionRing {
                speed 30
                intensity 2
                radius 5
            }
        }
    }

    damage_instance {
        damage 1
    }
}
```

---

### `neck_NukeBonus`
**Name:** Trigger the Nuke  
**Description:** Explode the nuke and mass damage everything.  
**Source:** `item_abilities.gon`  

```
neck_NukeBonus {
    template self_buff
    sub_ability neck_NukeExplode

    meta { //DESCRIPTION IS RELEVANT HERE
        name "ABILITY_NUKEBONUS_NAME"
        desc "ABILITY_NUKEBONUS_DESC"
    }

    graphics {
        animation tinkerSelf
    }

    bonus_passives {
        NukeQuestFinalBossModifications {
            self_damage {
                effects {
                    Conditional_OncePerBattle { //REALLY dont want any possible cases of double-triggering this with item synergies
                        key gamewin
                        TriggerGameEnding 1
                        CompleteItemQuest Nuke
                    }
                }
            }
        }
    }

    damage_instance {
        effects {
            VisualCountDownThenApplyStatus {
                ForceUseAbility neck_NukeExplode
            }
        }
        ai_base_score -999999
    }
}
```

---

### `neck_NukeBonus_remote`
**Source:** `item_abilities.gon`  

```
neck_NukeBonus_remote {
    variant_of neck_NukeBonus

    graphics {
        animation none
    }
}
```

---

### `neck_NukeExplode`
**Source:** `item_abilities.gon`  

```
neck_NukeExplode {
    template spell

    graphics {
        center_particle NukeBlastLarge
        animation none
        area_particle none
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode none
        max_aoe 20
    }

    bonus_passives {
        NukeQuestFinalBossModifications {
            damage_instance {
                effects {
                    Instakill 50 //get an Infinite damage icon on the ability
                    IgnoreDamage 1 //but dont actually kill
                }
            }
            self_damage {
                effects {
                    Conditional_OncePerBattle { //REALLY dont want any possible cases of double-triggering this with item synergies
                        key gamewin
                        TriggerGameEnding 0
                        CompleteItemQuest Nuke
                    }
                }
            }
            splash_damage {
                effects {
                    IgnoreDamage 1 //dont actually kill
                }
            }
        }
    }

    self_damage {
        effects {
            DestroyNeckArmor 1 
        }
    }

    damage_instance {
        damage 50
        piercing true
        cant_miss true
        elements [
            Fire
            Napalm
            Explosion
        ]
        effects {
            Vaporize 1
        }

        ai_base_score -999999
    }
    splash_damage {
        damage 50

        elements [
            Fire
            Explosion
            Mutate
        ]
    }
}
```

---

### `wp_PolymorphRemote`
**Source:** `item_abilities.gon`  

```
wp_PolymorphRemote {
    template spell

    meta {
        animate_name false
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 4
        min_aoe 0
        max_aoe 0
        
        restrictions [must_have_living_character must_have_enemy must_not_have_boss]
    }

    graphics {
        particle MagicMissleBlast
        animation weaponspell3
    }
    
    damage_instance {
        effects {
            RerollEnemy 1
        }
    }
}
```

---

### `tk_SoulJar`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_SoulJar {
    template spawn

    meta {
        name "{itemname}"
    }

    tags [summon]
    
    graphics {
        lob true
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
        must_not_be_a_summon true
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object PlayerCat_Shade

        catdata item_aux_catid
        clone_items true

        additional_passives {
            SafeDoomed 1
            InjuryImmunity 1
        }
    }
}
```

---

### `wp_MelonBaller`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MelonBaller {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false

        effects {
            Blind 3
            Conditional_Object {
            }
            Else {
                ApplyToSource {
                    Craft {
                        pool eyes_nonrare
                        slot trinket
                        temporary false
                    }
                }
            }
        }
    }
}
```

---

### `wp_EtherSoakedRag`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_EtherSoakedRag {
    template targeted_status

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponspell
    }
    
    target {
        min_range 0
        max_range 1
    }
    
    damage_instance {
        damage 0
        incidentally_collects_pickups false
        effects {
            Conditional_FirstApplicationThisTurn {
                key EtherSoakedRag
                TempPassiveWhileHasStatus {
                    status Sleep
                    AddManaRegen 5
                    HealthRegenUp 5
                }
            }
            Sleep 3
        }
        type status_spell
    }
}
```

---

### `wp_DeathsScythe`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_DeathsScythe {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponSpinAttack
    }

    target {
        target_mode none
        aoe_mode square
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 13
    }
    
    self_damage {
        effects {
            Doomed 1
        }
    }
}
```

---

### `wp_MomsKnife`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MomsKnife {
    template straightshot_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponthrowstraight
        speed 10
        projectile source_weapon
        use_rotation_once true
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        max_aoe 3
        upgrade_straight_shot_to_piercing true
        upgrade_straight_shot_to_boomerang true
    }

    bonus_passives {
        CatchBoomerang 1
    }

    damage_instance {
        damage 2
    }
}
```

---

### `wp_Necronomicon`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Necronomicon {
    template spawn

    keyword_tooltips {PermanentMadness 1}

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        target_mode none
        max_aoe 5
        
        min_targets 5
        max_targets 5
    }

    spawn {
        object [ZombieCatFamiliar ZombieCatFamiliar FeralZombieKitten]
        faction default
    }
}
```

---

### `wp_Jitte`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Jitte {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage "ceil(str/2)"
        incidentally_collects_pickups false

        effects {
            Weakness 1
            ApplyToSource {
                StrengthUp 1
                HealthGain 1
            }
        }
    }
}
```

---

### `wp_AnarchistCookbook`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_AnarchistCookbook {
    template spawn

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
        fall_from_sky true
        fall_randomize_timing .3
    }

    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        target_mode none
        max_aoe 5
        
        min_targets 3
        max_targets 5
    }

    spawn {
        object Grenade
    }
}
```

---

### `wp_Ocarina`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Ocarina {
    template self_buff

    meta {
        name "{itemname}"
        animate_name false
    }

    graphics {
        animation none
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            TagMetronome musical
        }
    }
}
```

---

### `wp_HeavyMace`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_HeavyMace {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }
    
    damage_instance {
        damage str
        incidentally_collects_pickups false

        effects {
            Conditional_Shielded {
                BonusDamage str
                Cleave 1
            }
        }
    }
}
```

---

### `wp_UraniumRod`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_UraniumRod {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 2
        incidentally_collects_pickups false

        effects {
            Poison 2
            Weakness 1
            ConstitutionUp -1
        }

        elements [
            Fire
            Mutate
        ]
    }
}
```

---

### `wp_MysteriousBone`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MysteriousBone {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false

        effects {
            Charmed [1, .25]
        }
    }
}
```

---

### `wp_HolyGrail`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_HolyGrail {
    template spell
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation pray
        affected_particle HealMed
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        max_aoe 0
        min_range 0
        max_range 1
    }
    
    damage_instance {
        heal 5
        type spell

        elements [
            Holy
        ]
    }
}
```

---

### `wp_SpearOfDestiny`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SpearOfDestiny {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        requires_reload true
        start_reloaded true
    }

    graphics {
        animation weaponpoke
    }

    target {
        max_aoe 2
    }

    bonus_passives {
        ReloadOnElementalDamageReceived Holy
        ReloadOnGainDivineShield 1
    }

    damage_instance {
        damage 7
        piercing true
        incidentally_collects_pickups false
    }
}
```

---

### `wp_USAShield`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_USAShield {
    template ranged_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }
    
    cost {
        cantrip true
        mana 0
		once_per_fight true
    }

    target {
        min_range 1
        max_range 20
    }

    damage_instance {
        damage 4
        effects {
            Stun 1
        }
    }
}
```

---

### `wp_TeslaCannon`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_TeslaCannon {
    template straightshot_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponshoot
        projectile LightningBallProjectile
    }

    sounds {
        ontrigger SE_WeaponShoot_TeslaCannon
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 10
        restrictions none
        upgrade_straight_shot_to_piercing true
    }

    damage_instance {
        damage 10

        effects {
            Stun [1 .5]
        }

        elements [
            Electric
        ]
    }
}
```

---

### `wp_BloodyButterflyKnife`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BloodyButterflyKnife {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        animation weaponpoke
    }

    temporary_effects {
        Fury 75
    }
    
    damage_instance {
        damage 1
        piercing true
        incidentally_collects_pickups false
        effects {
            Bleed 1
            Leech 1
        }
    }
}
```

---

### `wp_BloodyBagOfGlass`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BloodyBagOfGlass {
    template lobbed_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 10
    }

    graphics {
        animation throwobject
        projectile GlassBall
    }

    damage_instance {
        damage 1

        effects {
            ChangeTile GlassTile
        }
    }
}
```

---

### `wp_MeatSlugger`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MeatSlugger {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 2
        knockback 10
        incidentally_collects_pickups false

        effects {
            Bruise 1
	    }
    }
}
```

---

### `wp_BloodyMeatHook`
**Source:** `item_abilities.gon`  

```
wp_BloodyMeatHook {
    variant_of wp_MeatHook

    target {
        target_mode direction8
    }

    damage_instance {
        damage 1
		effects {
			Cleave 1
			Bleed 1
		}
	}
	
}
```

---

### `wp_BloodySoulClaw`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BloodySoulClaw {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponstab
    }

    damage_instance {
        damage durability
        incidentally_collects_pickups false
        effects {
            RepairOnKill 2
            ApplyToSourceOnKill {
			    HealthGain 5
            }
        }
    }
}
```

---

### `wp_BloodBottles`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BloodBottles {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4
		
		max_aoe 1
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 3

        effects {
            ChangeTile GlassTile
        }
    }
}
```

---

### `wp_BlessedAnointingOil`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BlessedAnointingOil {
    template targeted_status

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        affected_particle Cleanse
    }
    
    target { 
        min_range 0
        max_range 1
    }

    damage_instance {
        damage 0
		heal 4

        effects {
            Cleanse 0
        }

        elements [
            Holy
        ]
    }
}
```

---

### `wp_HarpyClaw`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_HarpyClaw {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 1
        piercing true
        incidentally_collects_pickups false
        effects {
            Bleed 1
            Poison 1
			Confusion 1
			Slow 1
			Weakness 1
        }
    }
}
```

---

### `tk_BloodyRazor`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_BloodyRazor {
    template self_buff
    
    meta {
        name "{itemname}"
    }
    
    graphics {
        animation selfHarm
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        damage 5
        effects {
            DamageUp 3
			SpellDamageUp 1
        }
    }
}
```

---

### `tk_Pentagram`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Pentagram {
    template self_buff
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation selfHarm
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
		damage 5
        effects {
            RefreshMovePoints 1
            RefreshActPoints 1
        }
    }
}
```

---

### `head_HitlersToupe`
**Source:** `item_abilities.gon`  

```
head_HitlersToupe { 
    template spell

	graphics {
		animation showTrinket
		particle none
    }

    target {
        target_mode random_tile
        max_aoe 0
        max_range 20

        restrictions [must_have_living_character must_have_enemy]
    }

    damage_instance {
        damage 0
        cant_miss true
        effects {
            Madness 1
        }
    }
}
```

---

### `tk_DybbuksRib`
**Source:** `item_abilities.gon`  

```
tk_DybbuksRib { 
    template spell

	graphics {
		animation showTrinket
		particle none
    }

    target {
        target_mode random_tile
        max_aoe 0
        max_range 20

        restrictions [must_have_living_character must_have_enemy]
    }

    damage_instance {
        damage 0
        cant_miss true
        effects {
            Charmed 1
        }
    }
}
```

---

### `wp_GambitsDice`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_GambitsDice {
    template straightshot_attack
    
    meta {
        name "{itemname}"
        icon_damage_display "1-6"
    }

    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }

    cost {
        requires_reload true
        start_reloaded true
        mana 0
        cantrip true
		once_per_fight true
    }

    target {
        min_range 1
        max_range 10
        restrictions none

        X_is random_0_to_N
        N 5
    }

    bonus_passives {
        ReloadOnUseAbilityWithManaCost 6
    }

    damage_instance {
        damage 1+X
    }
}
```

---

### `wp_Stoolatk`
**Source:** `item_abilities.gon`  

```
wp_Stoolatk {
    template melee_attack

    meta {
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 2
        knockback 2
        incidentally_collects_pickups false
    }
}
```

---

### `AlienBeam`
**Source:** `item_abilities.gon`  

```
AlienBeam {
    template spell

    meta {
    }

    graphics {
        particle HyperBeam
        darken_screen true
        darken_screen_exclude_characters_on_tile true
        particle_mat shadow_occluded_spelldissolve
        animation majormagic
		prime_animation pointout
    }
    
    cost {
        cantrip true
        mana 0
		once_per_fight true
    }
    
    target {
        delayed_trigger true
        max_aoe 1
        max_range 5
    }
    
    damage_instance {
        damage 20
    }
}
```

---

### `wp_SpawnStacy`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SpawnStacy {
    template spawn

    meta {
        name "{itemname}"
    }

    tags [summon]
    
    graphics {
        lob true
        bounce_on_hit true
        animation weaponswing
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }
    
    target {
        min_range 1
        max_range 1+bonus_range
        restrictions none
    }

    spawn {
        object CharmedStacy
	}
}
```

---

### `wp_BungaClub`
**Source:** `item_abilities.gon`  

```
wp_BungaClub {
    template melee_attack
    
    meta {
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }

    damage_instance {
        damage 8
		knockback 5
        incidentally_collects_pickups false
    }
}
```

---

### `wp_Lugar`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Lugar {
    template straightshot_attack

    meta {
        name "{itemname}"
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        speed 25
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {

    }

    
    
    damage_instance {
        damage 10
    }
}
```

---

### `wp_SpawnCultist`
**Source:** `item_abilities.gon`  

```
wp_SpawnCultist {
    template spawn

    meta {
    }

    tags [summon]
    
    graphics {
        lob true
        bounce_on_hit true
        animation thumbsup
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        min_range 1
        max_range 2+bonus_range
        restrictions none
    }

    spawn {
        object CharmedCultist
	}
}
```

---

### `tk_Asteroid`
**Source:** `item_abilities.gon`  

```
tk_Asteroid {
    template spell
    
    meta {
    }

    graphics {
        particle MeteorFall
		animation psyAttack1
    }
    
    cost {
        infcantrip true
        mana 9
    }
    
    target {
        target_mode random_tile
        max_aoe 0
        max_range 20

        restrictions [must_have_living_character must_not_have_boss must_have_enemy]
    }
    
    damage_instance {
        damage 5

        effects {
            Burn 1
            BounceRock SmallLavaRock
        }

        elements [
            Gravity
            Fire
            Napalm
        ]
    }
}
```

---

### `tk_RoboSucc`
**Source:** `item_abilities.gon`  

```
tk_RoboSucc {
    template spell
    
    meta {

    }

    graphics {
		particle none
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    target {
        target_mode tile
        max_aoe 1
        max_range 0
        hint_can_target_pickups true
    }
    
    damage_instance {
        damage 0
        type none

        effects {
            CollectsPickups 1
        }
    }
}
```

---

### `head_CatChestPound`
**Source:** `item_abilities.gon`  

```
head_CatChestPound {
    template spell

    meta {
    }

    graphics {
        particle none
    }
    
    cost {
        mana 0
        requires_exact_character_aux 0
    }
    
    target {
        target_mode none
        max_aoe 3
        prioritize_dont_change_direction true
        aoe_excludes_self false
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Conditional_HasTag {
                tag cat
                DamageUp 1
            }
        }
    }
}
```

---

### `wp_Manhole`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Manhole {
    template straightshot_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponthrowstraight
        speed 10
        projectile source_weapon
        use_rotation_once true
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        max_aoe 4
        upgrade_straight_shot_to_piercing true
        upgrade_straight_shot_to_boomerang true
    }

    bonus_passives {
        CatchBoomerang 1
    }

    damage_instance {
        damage 5
		knockback 2
    }
}
```

---

### `wp_GoldPickaxe`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_GoldPickaxe {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }

    damage_instance {
        damage 4
        piercing true
        incidentally_collects_pickups false
        
        effects {
            Conditional_HasTag {
                tag pickup
            } Else {
                VaporizeInanimate 1

                Conditional_Object {
                    CanApplyToInanimate {
                        BreakIntoRocks Coin
                    }
                }
            }
        }

        elements [
            Earth
        ]
    }
}
```

---

### `wp_ChumShot`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ChumShot {
    template spawn

    meta {
        name "{itemname}"
    }
    
    graphics {
        lob true
        animation shoot
		projectile MaggotBall
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        min_range 3
        max_range 5+bonus_range
    }

    spawn {
        object CharmedMaggot
        ai_base_score 9999
    }
}
```

---

### `wp_DemonDoom`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_DemonDoom {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    graphics {
        animation weaponslam
    }

    damage_instance {
        damage 0
        type status_spell
        custom_additional_ai_weight avoid_redundant_debuffs_strict

        effects {
            Conditional_NotBoss {
                Doomed 1
            }
            Conditional_Boss {
                Drowsy 1
            }
        }
    }
}
```

---

### `wp_MegaAlienBlaster`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MegaAlienBlaster {
    template laser

    meta {
        name "{itemname}"
    }
    
    graphics {
        use_projectile_spawn_offset true
        animation weaponshoot
        visual_delay_but_simultaneous_damage 0
		
		beam_clip greenmegalaser
        beam_cap greenmegalasercap
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    target {
        target_mode direction
        aoe_mode line
        max_aoe 10
        aoe_excludes_self true
    }
    
    self_damage {
        damage 5
        effects {
            LateStatusApplication {
                CurrentWeaponDamageUp 5
            }
        }
    }

    damage_instance {
        damage 1
    }
}
```

---

### `wp_BookofBelial`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BookofBelial {
    template self_buff

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
		requires_reload true
    }

    bonus_passives {
        ReloadOnKillEnemy 1
    }

    graphics {
		animation weaponspell3
    }
    
    damage_instance {
        effects {
            DamageUp 3
        }
    }
}
```

---

### `wp_Rally`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Rally {
    template spell
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
        particle none
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }
    
    target {
        min_range 1
        max_range 4
        max_aoe 0
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            ForceAttack 1
        }
    }
}
```

---

### `wp_TuskThrow`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_TuskThrow {
    template melee_attack

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponswing
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    damage_instance {
        damage 15
		
		effects {
		    Bruise 2
		    Confusion 1
		}
	}	

	self_damage {
		effects {
			Drowsy 1
		}
	}
}
```

---

### `wp_Fate`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Fate {
    template spell
    
    meta {
        name "{itemname}"
    }

    graphics {
        particle MeteorFall
		animation weaponspell3
        random_delay [0, 120]
    }

    cost {
        mana 0
		cantrip true
    }

    target {
		target_mode none
        max_aoe 20
        aoe_chance .5
        knockback_mode zero

        can_multihit true
    }

    damage_instance {
        damage 10

        effects {
            Stun [1, .10]
            SpawnFlames [1, .20]
            BounceRock [1 .2]
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `tw_TriachnidSpawn`
**Source:** `item_abilities.gon`  

```
tw_TriachnidSpawn {
    template spawn
    
    graphics {
        lob false
        animation walk
    }

    target {
        max_range 2
    }

    spawn {
        object CharmedTinySpider
        ai_base_score 9999
    }
}
```

---

### `tk_LegWhistle`
**Source:** `item_abilities.gon`  

```
tk_LegWhistle {
    template spawn
    tags [summon]
    
    graphics {
        animation whistle
        fall_from_sky true
    }
    
    target {
        range_mode custom
        custom_range [[-2 0] [-2 -1] [-1 -2] [0 -2] [-1 1] [0 1] [1 0] [1 -1]]

        aoe_mode custom
        dont_orient_aoe true

        custom_aoe [[0 0] [1 0] [0 1] [1 1]]

        range_excludes_blocking false
        restrictions must_fit_2x2_character
        aoe_restrictions none

        range_display_include_aoe true
        mouse_offset [.5 .5]
    }
    
    cost {
        mana 0
        cantrip true
        once_per_fight true
    }
    
    spawn {
        object CharmedMegaDino
        size 2
    }
}
```

---

### `wp_ShotgunSteven`
**Source:** `item_abilities.gon`  

```
wp_ShotgunSteven {
    template straightshot_attack

    meta {

    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode direction
        max_aoe 3+bonus_range
        shotgun_mode true

        aoe_mode custom
        custom_aoe [[3, -2][3, -1][3, 0][3, 1][3, 2]]
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        lob_height 0
        speed 25
    }

    self_damage {
        damage 0
        knockback 10
        effects {
            KnockbackDirectionIsFacingDirection flip
			Confusion 2
        }
    }
    
    damage_instance {
        damage 7
    }
}
```

---

### `wp_StevensBagOfRocks`
**Source:** `item_abilities.gon`  

```
wp_StevensBagOfRocks {
    template melee_attack

    meta {

    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }
	
    temporary_effects {
        Fury 75
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false
        effects {
            Bruise 1
        }
    }
}
```

---

### `wp_StevensBottles`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_StevensBottles {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    damage_instance {
        damage 4

        effects {
            Tarred 2
            ChangeTile {
                tile OilTile
			}
		}
	}
}
```

---

### `wp_StevenWeapon1`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_StevenWeapon1 {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        requires_reload true
        start_reloaded true
    }

    graphics {
        animation weaponswing
    }
	
    bonus_passives {
        ReloadOnAllyCatDies 1
    }

    damage_instance {
        damage 1
        incidentally_collects_pickups false

        effects {
            Conditional_Ally {
                Conditional_PlayerCat {
                    KnockOutClone PlayerCat_MiniMiniMe
                }
                // todo: make this work with non-player ally cats? (i.e. kitten and tom-tom familiars)
            }
        }
    }
}
```

---

### `wp_StevenWeapon2`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_StevenWeapon2 {
    template lobbed_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        requires_reload true
        start_reloaded true
    }

    target {
        min_range 1
        max_range 20
    }

    graphics {
        animation weaponthrowhigh
        projectile source_weapon
    }
    
    bonus_passives {
        ReloadOnKillTagged rock
    }

    damage_instance {
        damage 0

        effects {
            Petrify 1
		}
	}
}
```

---

### `wp_BangGun`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_BangGun {
    template melee_attack

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }
	
    graphics {
        animation weaponshoot
    }

    damage_instance {
        damage 3
        knockback 10
        force_no_contact true
        effects {
            OverrideChainKnockback 10
            Bruise 1
        }
    }
}
```

---

### `wp_TinaScream`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_TinaScream {
    variant_of EvilIncarnate

    meta {
        name "{itemname}"
    }

    tags [musical]
	
    graphics {
        darken_screen false
        particle none
        animation weaponTina
    }
	
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }
}
```

---

### `wp_FuryArm`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_FuryArm {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponslam
    }
	
    cost {
        mana 0
        cantrip true
    }

    temporary_effects {
        Fury 55
    }
	
    self_damage {
        effects {
            LateStatusApplication {
                CurrentWeaponDamageUp 1
            }
        }
    }

    damage_instance {
        damage 1
        incidentally_collects_pickups false
    }
}
```

---

### `neck_Brambles`
**Source:** `item_abilities.gon`  

```
neck_Brambles {
    template spell

    graphics {
        animation none
        particle none
        dont_orient true
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode none
        aoe_excludes_self true
    }

    damage_instance {
        damage 0

        effects {
            BramblesOnHit 1
        }

        elements [
            Grass
        ]
    }
}
```

---

### `wp_RatBomb`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_RatBomb {
    variant_of SpawnBomb

    meta {
        name "{itemname}"
    }

    graphics {
        animation throwobject
    }

    cost {
        mana 0
        cantrip true
    }
}
```

---

### `wp_MoneyBag`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_MoneyBag {
    template melee_attack
    
    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponslam
    }

    target {
        X_is random_0_to_N
        N 2
    }

    damage_instance {
        damage 7
        incidentally_collects_pickups false
        effects {
            Conditional_SourceAbilityHasTag {
                tag weapon_throw
                ScatterCoins {
                    stacks item_aux
                    stackable true
                }
                ApplyToSource {
                    AddWeaponAux -item_aux
                }
            } Else {
                ScatterCoins {
                    stacks "max(min(X+1, item_aux), 0)"
                    stackable true
                }
                ApplyToSource {
                    AddWeaponAux "-max(min(X+1, item_aux), 0)"
                }
            }
        }
    }
}
```

---

### `wp_MoneyBag_Small`
**Source:** `item_abilities.gon`  

```
wp_MoneyBag_Small {
    variant_of wp_MoneyBag

    target {
        N 2 //1 to 3 coins scattered
    }
    damage_instance {
        damage 1
    }
}
```

---

### `wp_MoneyBag_Medium`
**Source:** `item_abilities.gon`  

```
wp_MoneyBag_Medium {
    variant_of wp_MoneyBag

    target {
        N 3 //1 to 4 coins scattered
    }
    damage_instance {
        damage 3
    }
}
```

---

### `wp_MoneyBag_Large`
**Source:** `item_abilities.gon`  

```
wp_MoneyBag_Large {
    variant_of wp_MoneyBag

    target {
        N 4 //1 to 5 coins scattered
    }
    damage_instance {
        damage 5
    }
}
```

---

### `wp_MoneyBag_Huge`
**Source:** `item_abilities.gon`  

```
wp_MoneyBag_Huge {
    variant_of wp_MoneyBag

    target {
        N 5 //1 to 6 coins scattered
    }
    damage_instance {
        damage 7
    }
}
```

---

### `wp_ZodiacsSixshooter`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ZodiacsSixshooter {
    template ranged_attack

    meta {
        name "{itemname}"
    }

    graphics {
        projectile Bullet
        animation weaponshoot
        speed 25
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode tile
        min_range 1
        max_range 20
    }

    damage_instance {
        damage 2
    }
}
```

---

### `wp_ZodiacsSixshooter_Auto`
**Source:** `item_abilities.gon`  

```
wp_ZodiacsSixshooter_Auto {
    variant_of wp_ZodiacsSixshooter
    
    meta {
        is_weapon true
    }

    self_damage {
        damage 0
        effects {
            DamageWeapon 1
        }
    }
}
```

---

### `wp_IrradiatedObject`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
        once_per_fight true
    }

    graphics {
        animation weaponswing
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false
    }
}
```

---

### `wp_IrradiatedObject_Burn`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Burn {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Burn 1
        }
    }
}
```

---

### `wp_IrradiatedObject_Poison`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Poison {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Poison 1
        }
    }
}
```

---

### `wp_IrradiatedObject_Bleed`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Bleed {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Bleed 1
        }
    }
}
```

---

### `wp_IrradiatedObject_Fear`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Fear {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Fear 1
        }
    }
}
```

---

### `wp_IrradiatedObject_Confusion`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Confusion {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Confusion 1
        }
    }
}
```

---

### `wp_IrradiatedObject_Sleep`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Sleep {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Sleep 1
        }
    }
}
```

---

### `wp_IrradiatedObject_Charmed`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Charmed {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Charmed 1
        }
    }
}
```

---

### `wp_IrradiatedObject_Weakness`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Weakness {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Weakness 1
        }
    }
}
```

---

### `wp_IrradiatedObject_Stun`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Stun {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Stun 1
        }
    }
}
```

---

### `wp_IrradiatedObject_Bruise`
**Source:** `item_abilities.gon`  

```
wp_IrradiatedObject_Bruise {
    variant_of wp_IrradiatedObject
    damage_instance {
        effects {
            Bruise 1
        }
    }
}
```

---

### `wp_Pliers`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Pliers {
    template melee_attack

    meta {
        name "{itemname}"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponpoke
    }
    
    damage_instance {
        damage 1
        incidentally_collects_pickups false

        effects {
            Weakness 3
            Conditional_Object {
            }
            Else {
				Conditional_GoodRoll {
                    ApplyToSource {
                        FindItem Molars
                    }
					odds 20%
				}
            }
        }
    }
}
```

---

### `wp_FeatherDarts`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_FeatherDarts {
    template ranged_attack

    meta {
        name "{itemname}"
    }

    tags [weapon_throw]
    
    cost {
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 20
    }

    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }
    
    damage_instance {
        damage 1
    }
}
```

---

### `wp_FeatheredWing`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_FeatheredWing {
    template spell

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
    }

    graphics {
        animation weaponswing
        particle fx_windSpell
    }
    
    target {
        target_mode direction
        knockback_mode orientation

        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }

    damage_instance {
        damage 1
        incidentally_collects_pickups false

        knockback 3
        elements [
            Wind
        ]
    }
}
```

---

### `wp_SteelBall`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_SteelBall {
    template spawn

    meta {
        name "{itemname}"
    }

    tags [summon]
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }

    graphics {
        lob true
        animation throwobject
    }
    
    target {
        min_range 1
        max_range 3
    }

    spawn {
        object SteelFly
    }
}
```

---

### `tk_SpawnTheLost`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_SpawnTheLost {
    template spawn

    meta {
        name "{itemname}"
    }

    tags [summon]
    
    graphics {
        lob true
        bounce_on_hit true
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
		once_per_fight true
    }
    
    target {
        min_range 1
        max_range 1+bonus_range
        restrictions none
    }

    spawn {
        object TheLost
	}
}
```

---

### `wp_Probe`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_Probe {
    template melee_attack

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponpoke
    }

    cost {
        mana 0
        cantrip true
    }
	
    target {
        restrictions [aoe_must_exist]
        aoe_restrictions must_backstab
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        force_play_hit_animation true

        effects {
            Charmed 3
        }

        custom_additional_ai_weight avoid_redundant_debuffs_strict
    }
}
```

---

### `wp_ThePact`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
wp_ThePact {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation weaponspell3
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            PermanentConstitution -1
			StrengthUp 1
			DexterityUp 2
			SpeedUp 2
        }
    }
}
```

---

### `tk_Reset`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Reset {
    variant_of Reset

    meta {
        name "{itemname}"
    }

    cost {
        mana 0
        cantrip true
        once_per_fight true
    }
}
```

---

### `tk_TheBlackBox`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_TheBlackBox {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
    }

    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            Craft {
                pool any_chapter
                slot random_empty
                temporary false
            }
        }
    }
}
```

---

### `tk_Glitch`
**Name:** {itemname}  
**Source:** `item_abilities.gon`  

```
tk_Glitch {
    template self_buff

    meta {
        name "{itemname}"
    }

    graphics {
        animation showTrinket
    }
    
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        effects {
            ScrambleLastUsedSpell {
                permanent true
            }
        }
    }
}
```

---

## File: `disorder_abilities.gon`

### `ViolentOutburst`
**Source:** `disorder_abilities.gon`  

```
ViolentOutburst {
    template dash_attack

    graphics {
        dash_start_animation headbuttdashStart
        dash_animation headbuttdash
        dash_attack_animation headbuttdashEnd
    }

    target { 
        max_range 2
    }

    damage_instance {
        damage 1
        knockback 1
    }
    self_damage {
        damage 1
    }
}
```

---

### `BasicDashAttackMove`
**Name:** Dash Attack  
**Description:** Dash forward, then attack with knockback.  
**Source:** `disorder_abilities.gon`  

```
BasicDashAttackMove {
    template dash_attack
    
    meta {
        name "ABILITY_BASICDASHATTACKMOVE_NAME"
        desc "ABILITY_BASICDASHATTACKMOVE_DESC"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }
    
    cost {
        move_points 1
        act_points 0
    }
    
    damage_instance {
        damage 3+bonus_melee_ability_damage
        knockback 1
    }
}
```

---

### `BasicDashAttackMove_NoKnockback`
**Name:** Dash Attack  
**Description:** Dash forward and attack  
**Source:** `disorder_abilities.gon`  

```
BasicDashAttackMove_NoKnockback {
    template dash_attack
    
    meta {
        name "ABILITY_BASICDASHATTACKMOVE_NOKNOCKBACK_NAME"
        desc "ABILITY_BASICDASHATTACKMOVE_NOKNOCKBACK_DESC"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }
    
    cost {
        move_points 1
        act_points 0
    }
    
    damage_instance {
        damage 3+bonus_melee_ability_damage
    }
}
```

---

### `PoxScratch`
**Source:** `disorder_abilities.gon`  

```
PoxScratch {
    template self_buff
    
    graphics {
        animation scratchear
    }
    
    damage_instance {
        damage 1
        
        effects {
            EndTurn 1
        }
    }
}
```

---

### `MegaFart`
**Name:** Mega Fart  
**Source:** `disorder_abilities.gon`  

```
MegaFart {
    template spell

    meta {
        name "ABILITY_MEGAFART_NAME"
    }

    graphics {
        particle none
        animation fartoom
    }

    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 3

        aoe_considers_character_size true
        aoe_excludes_self true

        delayed_trigger true
    }

    damage_instance {
        damage 10
        knockback 10

        effects {
            Poison 2
        }

        elements [
            Explosion
        ]
    }
}
```

---

### `ParanoiaBasicMelee`
**Source:** `disorder_abilities.gon`  

```
ParanoiaBasicMelee {
    variant_of BasicMelee

    meta {
        is_basic_attack true
    }

    self_damage {
        effects {
            Fear 1
        }
    }
}
```

---

### `MiniFart`
**Source:** `disorder_abilities.gon`  

```
MiniFart {
    template spell

    graphics {
        particle PoisonPoof
        animation poopfartbehind
    }

    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 1

        aoe_considers_character_size true
        aoe_excludes_self true
    }

    damage_instance {
        damage 1

        effects {
            Poison 1
        }
    }
}
```

---

### `KidneyStone`
**Source:** `disorder_abilities.gon`  

```
KidneyStone {
    template spell

    graphics {
        particle None
        animation poopfartbehind
    }

    target {
        target_mode none

        aoe_mode custom
        custom_aoe [[-1, 0]]

        aoe_considers_character_size true
        aoe_excludes_self true
    }
	
    self_damage {
        damage 1
    }

    damage_instance {
        damage 5

        effects {
            ChangeTile WaterTile
            ObjectOnHitCharacter SmallRock
            SendRock 1
        }
    }
}
```

---

### `EatShit`
**Name:** Eat Poop  
**Source:** `disorder_abilities.gon`  

```
EatShit {
    template tile_targeted_melee_attack

    meta {
        name "ABILITY_EATSHIT_NAME"
    }

    graphics {
        animation biteattack
    }

    cost {
        mana 0
        cantrip true
    }
    
    target {
        restrictions [must_have_tag]
        target_requires_tag poop
    }

    damage_instance {
        damage 0
        ai_base_score 999999

        effects {
            IgnoreSelf 1

            Conditional_HasTag {
                tag poop
                Vaporize 1
                //FlatLeech 5 //this effect is added by the disorder
            }
        }
    }
}
```

---

### `Cannibalize`
**Name:** Cannibalize  
**Source:** `disorder_abilities.gon`  

```
Cannibalize {
    template melee_attack
    
    meta {
        name "ABILITY_CANNIBALIZE_NAME"
    }

    graphics {
        animation dashbite
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 0
        ai_base_score 999999

        effects {
            VaporizeCorpse 1

            ApplyToSource {
                AllStatsUp 1
                HealthGain 4
            }
        }
    }
}
```

---

### `CrohnsPoop`
**Source:** `disorder_abilities.gon`  

```
CrohnsPoop {
    template spawn

    graphics {
        animation fartoom
        lob true
    }

    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 2

        aoe_considers_character_size true
        aoe_excludes_self true
        aoe_restrictions must_be_displaceable
    }

    spawn {
        object Poop
    }

    damage_instance {
        damage 5
        effects {
            Poison 1
        }
    }
}
```

---

### `Hallucinate_Disorder`
**Source:** `disorder_abilities.gon`  

```
Hallucinate_Disorder {
    template spawn

    tags [summon]
    
    graphics {
        animation thinking
    }

    target {
        target_mode random_tile
        min_range 1
        max_range 20
        max_aoe 0
        aoe_restrictions [exclude_blocking]
    }

    spawn {
        object RANDOM_1X1_ENEMY
        faction solitary_enemies
        first_turn next_turn

        additional_passives {
            SafeDoomed 1
            InjuryImmunity 1
            FadeInsteadOfDie 1
            IllusionTint 1
            //PermanentMadness 1
            SchizoIllusionAIModifier 1
        }
    }
}
```

---

### `SpontaneouslyCombust`
**Source:** `disorder_abilities.gon`  

```
SpontaneouslyCombust {
    template spell

    graphics {
        center_particle FireBlastMushroom
        area_particle FireBlastSmall
        delay 5
        palette 6
        animation meow
    }
    
    target {
        target_mode none
        max_aoe 1
    }
    
    damage_instance {
        damage 0
        
        effects {
            Burn 5
        }
        
        elements [
            Fire
        ]
    }
}
```

---

### `DysenteryPoop`
**Source:** `disorder_abilities.gon`  

```
DysenteryPoop {
    template spawn

    graphics {
        animation poopfartbehind
        lob true
    }

    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[-1, 0]]
        aoe_restrictions none
    }

    spawn {
        object FlamingPoop
    }

    self_damage {
        damage 1
    }

    damage_instance {
        damage 3
        effects {
            Burn 3
        }
        elements [
            Fire
        ]
    }
}
```

---

### `DarkOneStrike`
**Source:** `disorder_abilities.gon`  

```
DarkOneStrike {
    template spell

    graphics {
        particle PoisonPoof
		animation evilMagic
    }
    
    cost {
        infcantrip true
    }
    
    target {
        target_mode tile
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        restrictions [must_have_living_character]
    }

    damage_instance {
        damage 1

        effects {
            Leech 1
            IgnoreSelf 1
        }
    }
}
```

---

### `SkunkTail`
**Source:** `disorder_abilities.gon`  

```
SkunkTail {
    template melee_attack

    graphics {
        animation poopfartbehind
    }

    target {
        knockback_mode back_orientation

        aoe_mode custom
        custom_aoe [ [-1, 0] ]
    }

    damage_instance {
        damage 0
        type spell
        knockback 4
        
        effects {
            Poison 4
            VisualFXTile PoisonPoof
        }
    }
}
```

---

## File: `event_abilities.gon`

### `FlowerEventSleep`
**Source:** `event_abilities.gon`  

```
FlowerEventSleep {
    template spell

    graphics {
        animation none
        particle none
    }
    
    target {
        target_mode none
        max_aoe 1
    }
    
    damage_instance {
        damage 0
        cant_miss true
        
        effects {
            ChangeTile TallFlowerTile
            Sleep 1
        }
    }
}
```

---

### `GrassEvent`
**Source:** `event_abilities.gon`  

```
GrassEvent {
    template spell

    graphics {
        animation none
        particle none
    }
    
    target {
        target_mode none
        max_aoe 1
    }
    
    damage_instance {
        damage 0
        
        effects {
            ChangeTile TallGrassTile
        }
    }
}
```

---

### `BrambleRandomTileEvent`
**Source:** `event_abilities.gon`  

```
BrambleRandomTileEvent {
    template spell

    target {
        max_aoe 0
        min_range 0
        max_range 20
        target_mode random_tile
    }

    graphics {
        center_particle none
        area_particle none
        animation none
    }

    damage_instance {
        damage 0
        
        effects {
            BramblesOnHit 1
        }

        elements [
            Grass
        ]
    }
}
```

---

### `RocksFallEvent`
**Source:** `event_abilities.gon`  

```
RocksFallEvent {
    template spell

    graphics {
        animation none
        particle none
    }
    
    target {
        target_mode none
        max_aoe 0
    }
    
    damage_instance {
        damage 0
        
        effects {
            BounceObject SmallRock
        }
    }
}
```

---

## File: `basic_attacks.gon`

### `BasicMelee`
**Name:** Melee Attack  
**Description:** Attack an adjacent unit.  
**Source:** `basic_attacks.gon`  

```
BasicMelee {
    template melee_attack

    graphics {
        animation Default

        damage_threshold_altanimations {
            heavyMelee 10
            heaviestMelee 20
        }
    }
    
    meta {
        name "ABILITY_MELEEATTACK_NAME"
        desc "ABILITY_MELEEATTACK_DESC"
        animate_name false
    }

    target { 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable //TODO: MAKE THIS WORK PROPERLY IF ENLARGED
    }
}
```

---

### `BasicMelee_Fighter`
**Source:** `basic_attacks.gon`  

```
BasicMelee_Fighter {
    variant_of BasicMelee
    meta {
        ability_icon BasicMelee
        class Fighter
    }
}
```

---

### `BasicBigMelee`
**Name:** Melee Attack  
**Description:** Attack an adjacent unit.  
**Source:** `basic_attacks.gon`  

```
BasicBigMelee {
    template melee_attack
    
    meta {
        name "ABILITY_BIGMELEEATTACK_NAME"
        desc "ABILITY_BIGMELEEATTACK_DESC"
        animate_name false
    }

    target { 
        max_aoe 1+bonus_melee_range
    }
}
```

---

### `BasicRanged`
**Name:** Lobbed Shot  
**Description:** Lob a shot over units and obstacles.  
**Source:** `basic_attacks.gon`  

```
BasicRanged {
    template lobbed_attack
    
    meta {
        name "ABILITY_LOBBEDSHOT_NAME"
        desc "ABILITY_LOBBEDSHOT_DESC"
        animate_name false
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 4+bonus_ranged_damage
    }
}
```

---

### `BasicRanged_Hunter`
**Source:** `basic_attacks.gon`  

```
BasicRanged_Hunter {
    variant_of BasicRanged
    meta {
        ability_icon BasicRanged
        class Hunter
    }
}
```

---

### `BasicRanged_1DMG`
**Name:** Lobbed Shot  
**Description:** Lob a shot over units and obstacles.  
**Source:** `basic_attacks.gon`  

```
BasicRanged_1DMG {
    template lobbed_attack
    
    meta {
        name "ABILITY_LOBBEDSHOT1DMG_NAME"
        desc "ABILITY_LOBBEDSHOT1DMG_DESC"
        animate_name false
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 1
    }
}
```

---

### `BasicShortRanged`
**Name:** Short Shot  
**Description:** Shoot a unit in your line of sight.  
**Source:** `basic_attacks.gon`  

```
BasicShortRanged {
    template ranged_attack
    
    meta {
        name "ABILITY_SHORTSHOT_NAME"
        desc "ABILITY_SHORTSHOT_DESC"
        animate_name false
    }

    target {
        min_range 1
        max_range 3+bonus_range
    }
}
```

---

### `BasicMagicShortRanged`
**Name:** Magic Dart  
**Description:** Shoot a charged projectile within your line of sight. This attack counts as both magical and physical.  
**Source:** `basic_attacks.gon`  

```
BasicMagicShortRanged {
    template ranged_attack
    
    meta {
        name "ABILITY_BASICMAGICSHORTRANGED_NAME"
        desc "ABILITY_BASICMAGICSHORTRANGED_DESC"
        animate_name false
        class Mage
    }

    graphics {
        projectile MagicSpikeProjectile//MagicMissileProjectileSmall
        animation createmagic
    }

    target {
        min_range 1
        max_range 5+bonus_range
    }

    damage_instance {
        damage 5+bonus_ranged_damage
        type physical_spell
        ranged true
    }
}
```

---

### `BasicShortLobbed`
**Name:** Short Lobbed Shot  
**Description:** Lob a shot over units and obstacles.  
**Source:** `basic_attacks.gon`  

```
BasicShortLobbed {
    template lobbed_attack
    
    meta {
        name "ABILITY_SHORTLOBBEDSHOT_NAME"
        desc "ABILITY_SHORTLOBBEDSHOT_DESC"
        animate_name false
    }

    target {
        min_range 1
        max_range 3+bonus_range
    }
}
```

---

### `BasicStraightShot`
**Name:** Nail Throw  
**Description:** Attack a unit in a straight line.  
**Source:** `basic_attacks.gon`  

```
BasicStraightShot {
    template straightshot_attack
    
    meta {
        name "ABILITY_NAILTHROW_NAME"
        desc "ABILITY_NAILTHROW_DESC"
        animate_name false
    }

    graphics {
        animation throwobject
    }

    target {
        max_aoe 3+bonus_range
    }

    damage_instance {
        damage 5+bonus_ranged_damage
    }
}
```

---

### `BasicStraightShot_Thief`
**Source:** `basic_attacks.gon`  

```
BasicStraightShot_Thief {
    variant_of BasicStraightShot
    meta {
        ability_icon BasicStraightShot
        class Thief
    }
}
```

---

### `BasicMedicMelee`
**Name:** Melee Attack / Heal  
**Description:** Heals allies but damages enemies.  
**Source:** `basic_attacks.gon`  

```
BasicMedicMelee {
    template melee_attack
    
    meta {
        name "ABILITY_MELEEHEAL_NAME"
        desc "ABILITY_MELEEHEAL_DESC"
        animate_name false
        class Medic
    }

    graphics {
        ally_animation lickAttack
        animation Default
    }

    target { 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable
    }

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            ContextualHeal 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `BasicMedicRanged`
**Name:** Ranged Attack / Heal  
**Description:** Heals allies but damages enemies.  
**Source:** `basic_attacks.gon`  

```
BasicMedicRanged {
    template lobbed_attack
    
    meta {
        name "ABILITY_RANGEDHEAL_NAME"
        desc "ABILITY_RANGEDHEAL_DESC"
        animate_name false
        class Medic
    }


    target { 
        min_range 1
        max_range 4+bonus_range
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            ContextualHeal 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `BasicTankMelee`
**Name:** Push Attack  
**Description:** Dash forward one space, then melee attack with Knockback.  
**Source:** `basic_attacks.gon`  

```
BasicTankMelee {
    template dash_attack
    
    meta {
        name "ABILITY_PUSHATTACK_NAME"
        desc "ABILITY_PUSHATTACK_DESC"
        animate_name false
        class Tank
    }

    graphics {
        dash_start_animation headbuttdashStart
        dash_animation headbuttdash
        dash_attack_animation headbuttdashEnd
    }

    target { 
        max_range 1+bonus_range
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1
    }
}
```

---

### `BasicMonkMelee`
**Name:** Melee Attack  
**Description:** Attack an adjacent unit.  
**Source:** `basic_attacks.gon`  

```
BasicMonkMelee {
    template melee_attack
    
    meta {
        name "ABILITY_MONKMELEE_NAME"
        desc "ABILITY_MONKMELEE_DESC"
        animate_name false
        class Monk
    }

    graphics {
        animation monkAttack
    }

    target { 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable //TODO: MAKE THIS WORK PROPERLY IF ENLARGED
    }

    damage_instance {
        damage "(5+bonus_melee_damage+1)/2"
    }
}
```

---

### `BasicMonkRanged`
**Name:** Lobbed Shot  
**Description:** Lob a shot over units and obstacles.  
**Source:** `basic_attacks.gon`  

```
BasicMonkRanged {
    template lobbed_attack
    
    meta {
        name "ABILITY_MONKLOBBED_NAME"
        desc "ABILITY_MONKLOBBED_DESC"
        animate_name false
        class Monk
    }

    target {
        min_range 2
        max_range 4+bonus_range
    }

    damage_instance {
        damage "(4+bonus_ranged_damage+1)/2"
    }
}
```

---

### `BasicButcherMelee`
**Name:** Cleave  
**Description:** Attack a unit adjacent or diagonally with Cleave.  
**Source:** `basic_attacks.gon`  

```
BasicButcherMelee {
    template melee_attack
    
    meta {
        name "ABILITY_BUTCHERMELEE_NAME"
        desc "ABILITY_BUTCHERMELEE_DESC"
        animate_name false
        class Butcher
    }

    graphics {
        animation butcherAttack
    }

    target { 
        target_mode direction8 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable //TODO: MAKE THIS WORK PROPERLY IF ENLARGED
    }

    damage_instance {
        damage 5+bonus_melee_damage
        effects {
            Cleave 1
        }
    }
}
```

---

### `BasicButcherMeleeWide`
**Name:** Wide Cleave  
**Description:** Attack a wide area with Cleave.  
**Source:** `basic_attacks.gon`  

```
BasicButcherMeleeWide {
    template melee_attack
    
    meta {
        name "ABILITY_BUTCHERWIDE_NAME"
        desc "ABILITY_BUTCHERWIDE_DESC"
        animate_name false
        class Butcher
    }

    target { //TODO: have "wide melee" aoe mode that works with range increasing stuff
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }

    damage_instance {
        damage 5+bonus_melee_damage
        effects {
            Cleave 1
        }
    }
}
```

---

### `BasicButcherMeleeWideSpin`
**Name:** Spin Cleave  
**Description:** Attack everything around you with Cleave.  
**Source:** `basic_attacks.gon`  

```
BasicButcherMeleeWideSpin {
    template melee_attack
    
    meta {
        name "ABILITY_BUTCHERSPIN_NAME"
        desc "ABILITY_BUTCHERSPIN_DESC"
        animate_name false
        class Butcher
    }

    graphics {
        animation singleSpin
    }

    target { //TODO: have "wide melee" aoe mode that works with range increasing stuff
        target_mode none
        max_aoe 1+bonus_melee_range
        aoe_mode square
    }

    damage_instance {
        damage 5+bonus_melee_damage
        effects {
            Cleave 1
        }
    }
}
```

---

### `BasicButcherMeleeWideDoubleSpin`
**Source:** `basic_attacks.gon`  

```
BasicButcherMeleeWideDoubleSpin {
    variant_of BasicButcherMeleeWideSpin
    class MultiHitMeleeAttackAbility

    meta {
        ability_icon BasicButcherMeleeWideSpin
    }

    graphics {
        start spinattackstart
        loop spinattackloop
        end spinattackend
    }
    target {
        multihit 2
    }
}
```

---

### `BasicDruidAbility`
**Name:** Sing  
**Description:** Heal and give +1 Temporary Damage to units in a wide area.  
**Source:** `basic_attacks.gon`  

```
BasicDruidAbility {
    template spell
    
    meta {
        name "ABILITY_DRUIDSING_NAME"
        desc "ABILITY_DRUIDSING_DESC"
        animate_name false
        class Druid
    }
    tags [musical]

    graphics {
        animation sing3//howl
        particle None
    }

    target { 
        max_aoe 2
        max_range 5+bonus_range
    }

    damage_instance {
        //damage 0
        heal 1
        cant_miss true

        effects {
            //ContextualHeal 1

            //Conditional_Ally {
                TempDamageUp 1
            //}
        }

        elements [
            Holy
        ]
    }
}
```

---

### `BasicDruidAbilityVersatile`
**Name:** Sing  
**Description:** Heal and give +1 Temporary Damage to units in a wide area.  
**Source:** `basic_attacks.gon`  

```
BasicDruidAbilityVersatile {
    template spell
    
    meta {
        name "ABILITY_DRUIDVERSATILE_NAME"
        desc "ABILITY_DRUIDVERSATILE_DESC"
        animate_name false
        class Druid
    }

    tags [musical]

    graphics {
        animation sing3//howl
        particle None
    }

    target { 
        max_aoe 2
        max_range 5+bonus_range
    }

    damage_instance {
        damage 1
        cant_miss true

        effects {
            ContextualHeal 1

            Conditional_Ally {
                TempDamageUp 1
            }
            Conditional_Enemy {
                TempDamageUp -1
            }
        }

        elements [
            Holy
        ]
    }
}
```

---

### `TinkererCraft`
**Name:** Craft Weapon  
**Description:** Craft and equip a random temporary weapon.  
**Source:** `basic_attacks.gon`  

```
TinkererCraft {
    template self_buff

    keyword_tooltips {TemporaryItem 1 BonusAbility TinkererThrow}
    
    meta {
        name "ABILITY_CRAFTWEAPON_NAME"
        desc "ABILITY_CRAFTWEAPON_DESC"
        animate_name false
        class Tinkerer
    }

    graphics {
        animation tinker
    }

    target {
        restrictions aoe_must_exist
        aoe_restrictions must_have_cat_with_empty_weapon_slot
    }

    damage_instance {
        damage 0

        effects {
            Craft {
                pool tinkerer_default
                slot weapon
            }
            IgnoreDebuffs 1
        }
        ai_base_score 9999
        custom_additional_ai_weight prefer_dont_move
    }
}
```

---

### `TinkererThrow`
**Name:** Throw Weapon  
**Description:** Throw your weapon at a unit.
[s:.7]This breaks the weapon.[/s]  
**Source:** `basic_attacks.gon`  

```
TinkererThrow {
    template ranged_attack
    
    meta {
        name "ABILITY_THROWWEAPON_NAME"
        desc "ABILITY_THROWWEAPON_DESC"
        animate_name false
        class Tinkerer
    }

    tags [weapon_throw]

    graphics {
        animation weaponthrowstraight
        projectile source_weapon
    }

    cost {
        infcantrip true
        requires_destructible_weapon true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    bonus_passives {
        AbilityInheritsWeaponEffects 1
        DownRankAIIfWeaponUsable .001
    }

    self_damage {
        effects {
            DestroyWeaponThrow 1
        }
    }

    damage_instance {
        damage 5+bonus_ranged_damage
    }
}
```

---

### `BasicPsychicPull`
**Name:** Psychic Pull  
**Description:** Pull a unit toward you from anywhere dealing low damage.  
**Source:** `basic_attacks.gon`  

```
BasicPsychicPull {
    template spell

    meta {
        name "ABILITY_PSYCHICPULL_NAME"
        desc "ABILITY_PSYCHICPULL_DESC"
        animate_name false
        class Psychic
    }

    graphics {
        particle MagicMissleBlast
        animation psyAttack3
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target {
        max_aoe 0
        max_range 20

        knockback_mode target_to_character
    }
    
    damage_instance {
        damage 2+bonus_basic_spell_damage
        knockback 1

        elements [
            Gravity
        ]
    }
}
```

---

### `BasicNecroRanged`
**Name:** Leech Shot  
**Description:** A lobbed attack that inflicts Leech 1.  
**Source:** `basic_attacks.gon`  

```
BasicNecroRanged {
    template lobbed_attack
    
    meta {
        name "ABILITY_LEECHSHOT_NAME"
        desc "ABILITY_LEECHSHOT_DESC"
        animate_name false
        class Necromancer
    }

    graphics {
        projectile LeechProjectile
    }

    target {
        min_range 1
        max_range 3+bonus_range
    }

    damage_instance {
        damage 3+bonus_ranged_damage

        effects {
            Leeches 1
        }
    }
}
```

---

### `BasicDrainMelee`
**Name:** Drain Attack  
**Description:** A melee attack with Lifesteal.  
**Source:** `basic_attacks.gon`  

```
BasicDrainMelee {
    template melee_attack
    
    meta {
        name "ABILITY_DRAINATTACK_NAME"
        desc "ABILITY_DRAINATTACK_DESC"
        animate_name false
    }

    graphics {
        animation dashbite
    }

    target { 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable //TODO: MAKE THIS WORK PROPERLY IF ENLARGED
    }

    damage_instance {
        damage 5+bonus_melee_damage
    
        effects {
            Leech 1
        }
    }
}
```

---

### `BasicHook`
**Name:** Hook  
**Description:** Pull an enemy to you.  
**Source:** `basic_attacks.gon`  

```
BasicHook {
    template straightshot_attack

    meta {
        name "ABILITY_HOOK_NAME"
        desc "ABILITY_HOOK_DESC"
        animate_name false
    }

    target {
        max_aoe 3+bonus_range

        knockback_mode pull_to_character
    }

    graphics {
        animation throwobject

        projectile Froghook
        chain_movieclip Frogchain
        chain_distance .25
    }
    
    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
             PullSourceToKnockbackImmuneTarget 1
             CollectsPickups 1
        }
    }
}
```

---

### `BasicMagicMissile`
**Name:** Magic Missile  
**Description:** Shoot an infinite-range projectile that can't miss.
[s:.7](This attack's damage scales with your [img:int])[/s]  
**Source:** `basic_attacks.gon`  

```
BasicMagicMissile {
    template spell

    meta {
        name "ABILITY_BASICMAGICMISSILE_NAME"
        desc "ABILITY_BASICMAGICMISSILE_DESC"
        class Mage
        animate_name false
    }

    graphics {
        particle MagicMissleBlast
        use_projectile true
        projectile MagicMissileProjectile
        lob_height 1
        speed 20
        animation castspell
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage "3+bonus_basic_spell_damage+((int-5)*.5)"
        cant_miss true
    }
}
```

---

### `BasicSuplex`
**Name:** Suplex  
**Description:** Grab a unit in front of you and slam it into the tile behind you.  
**Source:** `basic_attacks.gon`  

```
BasicSuplex {
    template melee_attack
    class SuplexAbility
    
    meta {
        name "ABILITY_SUPLEX_NAME"
        desc "ABILITY_SUPLEX_DESC"
        class Tank
        animate_name false
    }

    tags [cant_be_simulcast] //for MimicBasicAttacks passive

    graphics {
        animation suplex
    }

    cost {
        move_points 0
        act_points 1
    }

    target {
       knockback_mode zero
       aoe_considers_character_size false

       target_mode tile
       restrictions [aoe_must_be_displaceable must_have_character]
       range_mode standard
       aoe_mode standard
       min_range 1
       max_range 1
       min_aoe 0 
       max_aoe 0 
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee
        blocked_multiplier 2
        makes_contact false
    }
}
```

---

### `BasicTwoHitMelee`
**Name:** Two-Hit Melee Attack  
**Description:** Hits twice  
**Source:** `basic_attacks.gon`  

```
BasicTwoHitMelee {
    template melee_attack
    
    meta {
        name "ABILITY_BASICTWOHITMELEE_NAME"
        desc "ABILITY_BASICTWOHITMELEE_DESC"
        animate_name false
    }

    graphics {
        animation doubleswat
    }

    target { 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable //TODO: MAKE THIS WORK PROPERLY IF ENLARGED
        multihit 2
    }
}
```

---

### `BasicPuke`
**Name:** Puke Shot  
**Description:** Lob projectiles in an area.  
**Source:** `basic_attacks.gon`  

```
BasicPuke {
    template lobbed_attack
    
    meta {
        name "ABILITY_PUKESHOT_NAME"
        desc "ABILITY_PUKESHOT_DESC"
        animate_name false
    }
    
    graphics {
        animation pukeatk
    }

    target {
        min_range 1
        max_range 4+bonus_range
        max_aoe 1
    }

    damage_instance {
        damage "(4+bonus_ranged_damage+1)/2"
		elements [
            Water
        ]
    }
}
```

---

### `BasicExplosiveShot`
**Name:** Explosive Shot  
**Description:** Lob a puke projectile that does splash damage to neighboring units.  
**Source:** `basic_attacks.gon`  

```
BasicExplosiveShot {
    template spell
    
    meta {
        name "ABILITY_EXPLOSIVESHOT_NAME"
        desc "ABILITY_EXPLOSIVESHOT_DESC"
        animate_name false
    }
    
    graphics {
        animation pukeatk
        use_projectile true
        projectile PukeBall
        particle Explosion
        delay 2
    }

    target {
        min_range 3
        max_range 4+bonus_range
        max_aoe 1
    }

    damage_instance {
        damage 4+bonus_ranged_damage
        type ranged
		elements [
            Explosion
        ]
    }
}
```

---

### `BasicPoke`
**Name:** Poke  
**Description:** A melee attack that deals 1 damage.  
**Source:** `basic_attacks.gon`  

```
BasicPoke {
    template melee_attack
    
    meta {
        name "ABILITY_POKE_NAME"
        desc "ABILITY_POKE_DESC"
        ability_icon Poke
        animate_name false
    }

    graphics {
        animation tinyPunch
    }

    damage_instance {
        damage 1
        type melee
    }
}
```

---

### `GerdShot`
**Name:** Gerd Shot  
**Description:** Lob a puke projectile that does splash damage to neighboring units. Damages you for 2 on use.  
**Source:** `basic_attacks.gon`  

```
GerdShot {
    template spell
    
    meta {
        name "ABILITY_GERDSHOT_NAME"
        desc "ABILITY_GERDSHOT_DESC"
        animate_name false
    }
    
    graphics {
        use_projectile true
        projectile PukeBall
        animation pukeatk
        particle Wave
        center_particle none
    }

    target {
        min_range 1
        max_range 4+bonus_range
        max_aoe 1
    }

    self_damage {
        damage 2
    }

    damage_instance {
        damage "4+bonus_ranged_damage"
        type ranged
        elements [
            Water
        ]
    }
    splash_damage {
        damage 4
        type spell
        knockback 1
        elements [
            Water
        ]
    }
}
```

---

### `BasicSpin`
**Name:** Spin Attack  
**Description:** Attack all adjacent units.  
**Source:** `basic_attacks.gon`  

```
BasicSpin {
    template melee_attack
    
    meta {
	    name "ABILITY_BASICSPIN_NAME"
        desc "ABILITY_BASICSPIN_DESC"
        animate_name false
    }
	
    graphics {
        animation singleSpin
    }

    target {
        target_mode none
        aoe_mode cross
        knockback_mode character_to_tile
    }

    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `BasicMetronome`
**Name:** Metronome  
**Description:** Cast a random spell.  
**Source:** `basic_attacks.gon`  

```
BasicMetronome {
    template self_buff
    
    meta {
        name "ABILITY_METRONOME_NAME"
        desc "ABILITY_METRONOME_DESC"
        class Colorless
        type_icon "unknown"
    }

    tags [musical]
    
    graphics {
        animation metronome
    }

    damage_instance {
        effects {
            Metronome 1
        }
    }
}
```

---

## File: `basic_movement.gon`

### `DefaultMove`
**Name:** Move  
**Description:** {he} go  
**Source:** `basic_movement.gon`  

```
DefaultMove {
    template move
    
    meta {
        name "ABILITY_MOVE_NAME"
        desc "ABILITY_MOVE_DESC"
        animate_name false
    }
}
```

---

### `BasicJump`
**Name:** Jump  
**Description:** {he} jump  
**Source:** `basic_movement.gon`  

```
BasicJump {
    template jump_attack
    
    meta {
        name "ABILITY_JUMP_NAME"
        desc "ABILITY_JUMP_DESC"
        animate_name false
        is_move true
    }

    cost {
        move_points 1
        act_points 0
    }

    graphics {
        jump_attack_animation land
    }

    target { 
        target_mode tile

        min_range 1
        max_range mov
        
        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        
        aoe_considers_character_size false
        range_display_include_character_size true
        restrictions must_be_moveable
    }

    damage_instance {
        type none
        damage 0
    }
}
```

---

### `Teleport`
**Name:** Teleport  
**Description:** {he} teleport  
**Source:** `basic_movement.gon`  

```
Teleport {
    template teleport
    
    meta {
        name "ABILITY_TELEPORT_NAME"
        desc "ABILITY_TELEPORT_DESC"
        animate_name false
    }
}
```

---

### `BasicDig`
**Name:** Dig  
**Description:** {he} dig  
**Source:** `basic_movement.gon`  

```
BasicDig {
    template teleport
    
    meta {
        name "ABILITY_DIG_NAME"
        desc "ABILITY_DIG_DESC"
        animate_name false
    }

    graphics {
        animation_out digDown
        animation_in digUp
    }
}
```

---

### `Shadowstep`
**Name:** Shadowstep  
**Description:** {he} teleport  
**Source:** `basic_movement.gon`  

```
Shadowstep {
    template teleport
    
    meta {
        name "ABILITY_SHADOWSTEP_NAME"
        desc "ABILITY_SHADOWSTEP_DESC"
        animate_name false
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }
}
```

---

### `SwapPositions`
**Name:** Swap  
**Description:** {he} swap  
**Source:** `basic_movement.gon`  

```
SwapPositions {
    template swap
    
    meta {
        name "ABILITY_SWAP_NAME"
        desc "ABILITY_SWAP_DESC"
        animate_name true
    }
}
```

---

### `SwimmerMove`
**Name:** Move  
**Description:** {he} go  
**Source:** `basic_movement.gon`  

```
SwimmerMove {
    template move
    
    meta {
        name "ABILITY_SWIMMERMOVE_NAME"
        desc "ABILITY_SWIMMERMOVE_DESC"
        animate_name false
    }

    target {
        range_mode water_move
    }
}
```

---

### `TrampleMove`
**Name:** Move  
**Description:** {he} go  
**Source:** `basic_movement.gon`  

```
TrampleMove {
    template move
    
    meta {
        name "ABILITY_TRAMPLEMOVE_NAME"
        desc "ABILITY_TRAMPLEMOVE_DESC"
        animate_name false
    }

    temporary_effects {
        Trample 3
    }
    
    damage_instance {
        damage 3
    }
}
```

---

### `TrampleMoveOne`
**Name:** Move  
**Description:** {he} go  
**Source:** `basic_movement.gon`  

```
TrampleMoveOne {
    template move
    
    meta {
        name "ABILITY_MOVEONETILE_NAME"
        desc "ABILITY_MOVEONETILE_DESC"
        animate_name false
    }

    target { 
        max_range 1
    }

    temporary_effects {
        Trample 3
    }
    
    damage_instance {
        damage 3
    }
}
```

---

### `MaxTeleport`
**Name:** Teleport  
**Description:** {he} teleport  
**Source:** `basic_movement.gon`  

```
MaxTeleport {
    template teleport
    
    meta {
        name "ABILITY_MAXTELEPORT_NAME"
        desc "ABILITY_MAXTELEPORT_DESC"
        animate_name false
    }

    target { 
        max_range 20
    }
}
```

---

### `FloatMove`
**Name:** Move  
**Description:** {he} go  
**Source:** `basic_movement.gon`  

```
FloatMove {
    template move
    
    meta {
        name "ABILITY_FLOAT_NAME"
        desc "ABILITY_FLOAT_DESC"
        animate_name false
    }

    target {
        as_the_crow_flies true
    }
}
```

---

## File: `contextual_abilities.gon`

### `BreakWeb`
**Name:** Break Free  
**Description:** Break out of what you're tangled in.  
**Source:** `contextual_abilities.gon`  

```
BreakWeb {
    template self_buff
    
    meta {
        name "ABILITY_BREAKWEB_NAME"
        desc "ABILITY_BREAKWEB_DESC"
        class Colorless
    }

    tags [contextual]

    graphics {
        animation attack
    }
    sounds {
        ontrigger Spiderweb_Break
    }
    target {
        prioritize_dont_change_direction true
    }


    cost {
        move_points 0
        act_points 1
    }
    
    damage_instance {
        damage 0
        disallow_modifications true

        elements [
            Break_Web
        ]

        ai_base_score 9999
    }
}
```

---

### `BreakShortCircuit`
**Name:** Break Circuit  
**Description:** Break out of short circuit  
**Source:** `contextual_abilities.gon`  

```
BreakShortCircuit {
    template self_buff
    
    meta {
        name "ABILITY_BREAKSHORTCIRCUIT_NAME"
        desc "ABILITY_BREAKSHORTCIRCUIT_DESC"
        class Colorless
        ability_icon "BreakShortCircuit"
    }

    tags [contextual]

    graphics {
        animation attack
    }
    target {
        prioritize_dont_change_direction true
    }


    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        damage 0
        disallow_modifications true

        effects {
            TickDownStatus ShortCircuit
        }

        ai_base_score 9999
    }
}
```

---

### `BreakShortCircuit_Familiar`
**Source:** `contextual_abilities.gon`  

```
BreakShortCircuit_Familiar {
    variant_of BreakShortCircuit

    graphics {
        animation none
    }
}
```

---

### `BreakShortCircuit_Manaless`
**Source:** `contextual_abilities.gon`  

```
BreakShortCircuit_Manaless {
    variant_of BreakShortCircuit

    cost {
        infcantrip false
        act_points 1
        mana 0
    }

    graphics {
        animation none
    }
}
```

---

### `EnterMech`
**Name:** Enter Mech  
**Description:** Get in the mech suit.  
**Source:** `contextual_abilities.gon`  

```
EnterMech {
    template targeted_status
    
    meta {
        name "ABILITY_ENTERMECH_NAME"
        desc "ABILITY_ENTERMECH_DESC"
        class Colorless
    }

    tags [contextual]

    graphics {
        animation portout
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        target_mode random_closest_tile
        recalc_target_on_castpoint true
        min_range 1
        max_range 1

        restrictions [must_have_tag]
        target_requires_tag mount
    }
    
    damage_instance {
        damage 0
        
        effects {
            EnterMount enter
        }
    }
}
```

---

### `StruggleBase`
**Name:** Struggle  
**Description:** 25% chance to break free. If you fail, take damage.  
**Source:** `contextual_abilities.gon`  

```
StruggleBase {
    template melee_attack

    meta {
        name "ABILITY_STRUGGLE_NAME"
        desc "ABILITY_STRUGGLE_DESC"
        animate_name true
        ability_icon "Struggle"
    }

    cost {
        allow_offmap_casts true
        must_be_offmap true
    }

    graphics {
        animation none
    }
    
    
    target {
        target_mode none
        knockback_mode none
        aoe_mode hit_consumer
        aoe_considers_character_size false
    }

    damage_instance {
        damage 0
        type none

        effects {
            ChanceToBreakFree {
                stacks 25
                ability XXX
                fail_ability XXX
            }
        }
    }
}
```

---

### `LennyStruggle`
**Source:** `contextual_abilities.gon`  

```
LennyStruggle {
    variant_of StruggleBase

    damage_instance {
        effects {
            ChanceToBreakFree {
                ability LennyDrop
                fail_ability LennyStruggleFail
            }
        }
    }
}
```

---

### `CHuskStruggle`
**Source:** `contextual_abilities.gon`  

```
CHuskStruggle {
    variant_of StruggleBase

    damage_instance {
        effects {
            ChanceToBreakFree {
                ability CHuskDrop
                fail_ability CHuskDropFail
            }
        }
    }
}
```

---

### `FlailBase`
**Name:** Flail  
**Description:** Attack the unit restraining you. 25% chance to break free.  
**Source:** `contextual_abilities.gon`  

```
FlailBase {
    template melee_attack

    meta {
        name "ABILITY_FLAIL_NAME"
        desc "ABILITY_FLAIL_DESC"
        animate_name true
        ability_icon "Flail"
    }

    cost {
        allow_offmap_casts true
        must_be_offmap true
    }

    graphics {
        animation none
    }
    
    
    target {
        target_mode none
        knockback_mode none
        aoe_mode hit_consumer
        aoe_considers_character_size false
    }

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            ChanceToBreakFree {
                stacks 25
                ability XXX
            }
        }
    }
}
```

---

### `TinaFlail`
**Source:** `contextual_abilities.gon`  

```
TinaFlail { //for Guillotina
    variant_of FlailBase

    damage_instance {
        effects {
            ChanceToBreakFree {
                ability TinaSpit
            }
        }
    }
}
```

---

### `TinaFlailRage`
**Source:** `contextual_abilities.gon`  

```
TinaFlailRage { //for Guillotina
    variant_of FlailBase

    damage_instance {
        effects {
            ChanceToBreakFree {
                ability TinaSpit2
            }
        }
    }
}
```

---

### `MoonHandFlail`
**Source:** `contextual_abilities.gon`  

```
MoonHandFlail {
    variant_of FlailBase

    damage_instance {
        effects {
            ChanceToBreakFree {
                ability MoonHandDrop
            }
        }
    }
}
```

---

### `MoonHeadFlail`
**Source:** `contextual_abilities.gon`  

```
MoonHeadFlail {
    variant_of FlailBase

    damage_instance {
        effects {
            ChanceToBreakFree {
                ability MoonHead_SpitCat
                //fail_ability MoonHead_ChewCat
            }
        }
    }
}
```

---

### `EscapeBase`
**Name:** Escape?  
**Description:** 25% chance to break free.  
**Source:** `contextual_abilities.gon`  

```
EscapeBase {
    template melee_attack

    meta {
        name "ABILITY_ESCAPE_NAME"
        desc "ABILITY_ESCAPE_DESC"
        animate_name true
        ability_icon "Escape"
    }

    cost {
        allow_offmap_casts true
        must_be_offmap true
    }

    graphics {
        animation none
    }
    
    
    target {
        target_mode none
        knockback_mode none
        aoe_mode hit_consumer
        aoe_considers_character_size false
    }

    damage_instance {
        damage 0
        type none

        effects {
            ChanceToBreakFree {
                stacks 25
                ability XXX
            }
        }
    }
}
```

---

### `CaveWomanEscape`
**Source:** `contextual_abilities.gon`  

```
CaveWomanEscape {
    variant_of EscapeBase

    damage_instance {
        effects {
            ChanceToBreakFree {
                ability CaveWomanDrop
            }
        }
    }
}
```

---

### `PteroTryEscape`
**Source:** `contextual_abilities.gon`  

```
PteroTryEscape {
    variant_of EscapeBase

    damage_instance {
        effects {
            ChanceToBreakFree {
                ability PteroEscape
            }
        }
    }
}
```

---

### `Thrash`
**Name:** Thrash  
**Description:** Attack the unit restraining you.  
**Source:** `contextual_abilities.gon`  

```
Thrash {
    template melee_attack

    meta {
        name "ABILITY_THRASH_NAME"
        desc "ABILITY_THRASH_DESC"
        animate_name true
        ability_icon "Thrash"
    }

    cost {
        allow_offmap_casts true
        must_be_offmap true
    }

    graphics {
        animation none
    }
    
    
    target {
        target_mode none
        knockback_mode none
        aoe_mode hit_consumer
        aoe_considers_character_size false
    }

    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `MoonHeadCommandStopHittingYourself`
**Name:** Stop Hitting Yourself  
**Description:** Command all the moon hands to attack the face.  
**Source:** `contextual_abilities.gon`  

```
MoonHeadCommandStopHittingYourself {
    template melee_attack

    meta {
        name "ABILITY_MOONHEADCOMMANDSTOPHITTINGYOURSELF_NAME"
        desc "ABILITY_MOONHEADCOMMANDSTOPHITTINGYOURSELF_DESC"
        animate_name true
    }

    cost {
        allow_offmap_casts true
        must_be_offmap true
        mana 10
        infcantrip true
    }

    graphics {
        animation none
    }
    
    
    target {
        target_mode none
        knockback_mode none
        aoe_mode hit_consumer
        aoe_considers_character_size false
    }

    damage_instance {
        damage 0
        type none
        cant_miss true
        makes_contact false

        effects {
            Conditional_HasTag {
                tag moonhead
                UseAbility MoonHead_CommandHeadPunch
            }
        }
    }
}
```

---

## File: `misc_abilities.gon`

### `MoveOne`
**Source:** `misc_abilities.gon`  

```
MoveOne {
    template move

    target { 
        max_range 1
    }
}
```

---

### `MoveTwo`
**Source:** `misc_abilities.gon`  

```
MoveTwo {
    template move

    target { 
        max_range 2
    }
}
```

---

### `MoveThree`
**Source:** `misc_abilities.gon`  

```
MoveThree {
    template move

    target { 
        max_range 3
    }
}
```

---

### `MoveFour`
**Source:** `misc_abilities.gon`  

```
MoveFour {
    template move

    target { 
        max_range 4
    }
}
```

---

### `DoubleDistanceMove`
**Source:** `misc_abilities.gon`  

```
DoubleDistanceMove {
    template move

    target { 
        max_range mov*2
    }
}
```

---

### `MoveOneTrample`
**Source:** `misc_abilities.gon`  

```
MoveOneTrample {
    template move

    target { 
        max_range 1
    }

    temporary_effects {
        Trample 3
    }
}
```

---

### `MoveTwoTrample`
**Source:** `misc_abilities.gon`  

```
MoveTwoTrample {
    template move

    target { 
        max_range 2
    }

    temporary_effects {
        Trample 3
    }
}
```

---

### `MoveThreeTrample`
**Source:** `misc_abilities.gon`  

```
MoveThreeTrample {
    template move

    target { 
        max_range 3
    }

    temporary_effects {
        Trample 3
    }
}
```

---

### `MoveFourTrample`
**Source:** `misc_abilities.gon`  

```
MoveFourTrample {
    template move

    target { 
        max_range 4
    }

    temporary_effects {
        Trample 3
    }
}
```

---

### `FormShrinkFour`
**Source:** `misc_abilities.gon`  

```
FormShrinkFour {
    template self_buff
    
    meta {
        dont_visualize_ai true
    }

    graphics {
        animation shrink
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            FormChange {
                form 4
            }
        }
    }
}
```

---

### `FormShrinkThree`
**Source:** `misc_abilities.gon`  

```
FormShrinkThree {
    variant_of FormShrinkFour

    damage_instance {
        effects {
            FormChange {
                form 3
            }
        }
    }
}
```

---

### `FormShrinkTwo`
**Source:** `misc_abilities.gon`  

```
FormShrinkTwo {
    variant_of FormShrinkFour

    damage_instance {
        effects {
            FormChange {
                form 2
            }
        }
    }
}
```

---

### `FormShrinkOne`
**Source:** `misc_abilities.gon`  

```
FormShrinkOne {
    variant_of FormShrinkFour

    damage_instance {
        effects {
            FormChange {
                form 1
            }
        }
    }
}
```

---

### `FormGrowTwo`
**Source:** `misc_abilities.gon`  

```
FormGrowTwo {
    template self_buff
    
    meta {
        dont_visualize_ai true
    }

    graphics {
        animation grow
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            FormChange {
                form 2
            }
        }
    }
}
```

---

### `FormGrowThree`
**Source:** `misc_abilities.gon`  

```
FormGrowThree {
    variant_of FormGrowTwo

    damage_instance {
        effects {
            FormChange {
                form 3
            }
        }
    }
}
```

---

### `DoNothing`
**Source:** `misc_abilities.gon`  

```
DoNothing {
    template placeholder
    
    cost {
        cant_cast true
    }

    graphics {
        animation none
    }

    target {
        target_mode none
        aoe_mode none
        range_mode none
    }
}
```

---

## File: `test_abilities.gon`

### `BlockingRanged`
**Name:** Long Ranged Attack  
**Description:** he shoot  
**Source:** `test_abilities.gon`  

```
BlockingRanged {
    template ranged_attack
    
    meta {
        name "Long Ranged Attack"
        desc "he shoot"
        animate_name false
    }

    target {
        min_range 0
        max_range 10
        restrictions must_have_line_of_sight_unpurgable
    }
}
```

---

### `BigWind`
**Name:** Big Wind  
**Description:** hewind  
**Source:** `test_abilities.gon`  

```
BigWind {
    template spell

    meta {
        name "Big Wind"
        desc "hewind"
    }

    graphics {
        particle fx_windSpell
    }
    
    cost {
        mana 0
        infcantrip true
    }

    
    target {
        target_mode direction
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode orientation
    }

    damage_instance {
        damage 1
        knockback 1

        elements [
            Wind
        ]
    }
}
```

---

### `LookTowardsCenter`
**Name:** FaceCenter  
**Description:** hewind  
**Source:** `test_abilities.gon`  

```
LookTowardsCenter {
    template spell

    meta {
        name "FaceCenter"
        desc "hewind"
    }

    graphics {
        particle none
    }
    
    cost {
        mana 0
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode to_map_center
    }

    damage_instance {
        damage 0

        effects {
            FaceAway 1
        }
    }
}
```

---

### `LookTowardsMe`
**Name:** FaceMe  
**Description:** hewind  
**Source:** `test_abilities.gon`  

```
LookTowardsMe {
    template spell

    meta {
        name "FaceMe"
        desc "hewind"
    }

    graphics {
        particle none
    }
    
    cost {
        mana 0
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode tile_to_character_4snap
    }

    damage_instance {
        damage 0

        effects {
            FaceAway 1
        }
    }
}
```

---

### `LookTowardsMeOne`
**Name:** FaceMe  
**Description:** hewind  
**Source:** `test_abilities.gon`  

```
LookTowardsMeOne {
    template spell

    meta {
        name "FaceMe"
        desc "hewind"
    }

    graphics {
        particle none
    }
    
    cost {
        mana 0
        infcantrip true
    }

    
    target {
        target_mode tile
        max_aoe 0
        max_range 20
        aoe_considers_character_size false
        knockback_mode tile_to_character_4snap
    }

    damage_instance {
        damage 0

        effects {
            FaceAway 1
        }
    }
}
```

---

### `PierceShotTest`
**Name:** Pierce Shot Test  
**Description:** range 5 straight shot, upgraded to piercing  
**Source:** `test_abilities.gon`  

```
PierceShotTest {
    template straightshot_attack
    
    meta {
        name "Pierce Shot Test"
        desc "range 5 straight shot, upgraded to piercing"
        class Thief
    }

    graphics {
        animation invthrow
    }

    cost {
        infcantrip true
        mana 0
    }

    target {
        max_aoe 5
        upgrade_straight_shot_to_piercing true
    }

    damage_instance {
        damage 5+bonus_ranged_damage
    }
}
```

---

### `SleepTalk`
**Name:** Sleep Talk  
**Description:** High damage magical blast with infinite range. You can cast this while dead.  
**Source:** `test_abilities.gon`  

```
SleepTalk {
    template spell

    meta {
        name "Sleep Talk"
        desc "High damage magical blast with infinite range. You can cast this while dead."
        class Necromancer
    }

    graphics {
        particle BigMagicMissileBlast
        use_projectile true
        projectile MagicMissileProjectile
        lob_height 1
        speed 20
    }
    
    cost {
        infcantrip true
        mana 7
        can_cast_while_dead true
    }
    
    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 10
    }
}
```

---

### `SpearPokeTest`
**Source:** `test_abilities.gon`  

```
SpearPokeTest {
    template melee_attack

    graphics {
        detatched_animation SpearGuyAttack
        detatched_animation_reach 4
    }

    cost {
        mana 0
    }

    target {
        max_aoe 4
    }

    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `DiagonalDashTest`
**Name:** Diagonal Dash  
**Source:** `test_abilities.gon`  

```
DiagonalDashTest {
    template dash_attack
    
    meta {
        name "Diagonal Dash"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_attack_animation dashatk
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode direction8
    }
    
    damage_instance {
        damage 3+bonus_melee_ability_damage
        knockback 1
    }
}
```

---

### `DiagonalBasicMelee`
**Name:** Diagonal Melee  
**Source:** `test_abilities.gon`  

```
DiagonalBasicMelee {
    template melee_attack
    
    meta {
        name "Diagonal Melee"
    }

    cost {
        mana 0
    }
    
    target {
        target_mode direction8
        max_aoe 2
    }
    
    damage_instance {
        damage 3+bonus_melee_ability_damage
        knockback 1
    }
}
```

---

### `DiagonalSpell`
**Name:** Diagonal Spell  
**Description:** fire cone attack  
**Source:** `test_abilities.gon`  

```
DiagonalSpell {
    template spell

    meta {
        name "Diagonal Spell"
        desc "fire cone attack"
    }
    
    cost {
        mana 0
        cantrip true
    }

    graphics {
        particle Explosion
        delay 10
        animation weaponspell
    }
    
    target {
        target_mode direction8

        aoe_mode cone
        min_aoe 1
        max_aoe 2
    }
    
    damage_instance {
        damage 1

        effects {
            Burn 1
        }
        
        elements [
            Fire
        ]
    }
}
```

---

### `BounceDashTest`
**Name:** Bounce Dash  
**Source:** `test_abilities.gon`  

```
BounceDashTest {
    template dash_attack
    class BounceDashAbility
    
    meta {
        name "Bounce Dash"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_attack_animation dashatk
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode direction8
        max_range -1
        max_bounces 10
    }
    
    damage_instance { //for trample
        damage 3+bonus_melee_ability_damage
    }
    splash_damage { //for bonk
        damage 3+bonus_melee_ability_damage
        knockback 0
        makes_contact true
    }
}
```

---

### `LaserTest`
**Name:** Laser Test  
**Description:** laser  
**Source:** `test_abilities.gon`  

```
LaserTest {
    template laser
    
    meta {
        name "Laser Test"
        desc "laser"
    }

    graphics {
        animation shoot
        delay 5

        beam_clip thinlaser
        beam_cap thinlasercap
        mask_center SpearMaskCenter
        mask_extent SpearMaskExtent

        //use_projectile_spawn_offset true
    }

    cost {
        mana 1
        infcantrip true
    }

    damage_instance {
        damage 1
        knockback 0
    }
}
```

---

### `LaserBombTest`
**Name:** Laser Bomb Test  
**Description:** laser  
**Source:** `test_abilities.gon`  

```
LaserBombTest {
    template laser
    
    meta {
        name "Laser Bomb Test"
        desc "laser"
    }

    graphics {
        delay 5
    }

    target {
        target_mode tile

        max_range 5

        aoe_mode custom 
        custom_aoe [[1, 0]]
        aoe_symmetry four_way
    }

    cost {
        mana 1
        infcantrip true
    }

    damage_instance {
        damage 1
        knockback 0
    }
}
```

---

### `BackgroundTransitionTest`
**Source:** `test_abilities.gon`  

```
BackgroundTransitionTest {
    template self_buff
    
    cost {
        mana 0
        infcantrip true
    }

    damage_instance {
        effects {
            GlobalSpawnCharacter MegaGuppy
            PlayBackground 1
            SwitchMusic {
                new_song same
                new_layer event
            }
        }
    }
}
```

---

### `DbgBackgroundTransitionTest`
**Source:** `test_abilities.gon`  

```
DbgBackgroundTransitionTest {
    template self_buff

    graphics {
        dont_visualize_ai true
    }
    
    cost {
        mana 0
        infcantrip true
        allow_offmap_casts true
    }

    self_damage {
        effects {
            PlayBackground 1

            TimeDelayStatusApplication {
                delay .1
                GlobalSpawnCharacter MegaGuppy
                PlayBackground 1
                RemoveAmbientLightEffects .5
                SwitchMusic {
                    new_song same
                    new_layer event
                }
                Vaporize 1
            }
        }
    }
    damage_instance {
        ai_base_score 999999
    }
}
```

---

### `TestGameEndingSequence`
**Source:** `test_abilities.gon`  

```
TestGameEndingSequence {
    template self_buff

    cost {
        mana 0
        infcantrip true
        allow_offmap_casts true
    }

    self_damage {
        effects {
            TriggerGameEnding 1
        }
    }
}
```

---

## File: `util_abilities.gon`

### `STARTER_PLACEHOLDER_Fighter`
**Name:** ???  
**Description:** Becomes a random Fighter starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Fighter {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_FIGHTER_DESC"
        class Fighter
    }
}
```

---

### `STARTER_PLACEHOLDER_Thief`
**Name:** ???  
**Description:** Becomes a random Thief starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Thief {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_THIEF_DESC"
        class Thief
    }
}
```

---

### `STARTER_PLACEHOLDER_Tank`
**Name:** ???  
**Description:** Becomes a random Tank starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Tank {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_TANK_DESC"
        class Tank
    }
}
```

---

### `STARTER_PLACEHOLDER_Mage`
**Name:** ???  
**Description:** Becomes a random Mage starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Mage {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_MAGE_DESC"
        class Mage
    }
}
```

---

### `STARTER_PLACEHOLDER_Medic`
**Name:** ???  
**Description:** Becomes a random Cleric starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Medic {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_MEDIC_DESC"
        class Medic
    }
}
```

---

### `STARTER_PLACEHOLDER_Hunter`
**Name:** ???  
**Description:** Becomes a random Hunter starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Hunter {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_HUNTER_DESC"
        class Hunter
    }
}
```

---

### `STARTER_PLACEHOLDER_Necromancer`
**Name:** ???  
**Description:** Becomes a random Necromancer starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Necromancer {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_NECROMANCER_DESC"
        class Necromancer
    }
}
```

---

### `STARTER_PLACEHOLDER_Butcher`
**Name:** ???  
**Description:** Becomes a random Butcher starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Butcher {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_BUTCHER_DESC"
        class Butcher
    }
}
```

---

### `STARTER_PLACEHOLDER_Monk`
**Name:** ???  
**Description:** Becomes a random Monk starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Monk {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_MONK_DESC"
        class Monk
    }
}
```

---

### `STARTER_PLACEHOLDER_Druid`
**Name:** ???  
**Description:** Becomes a random Druid starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Druid {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_DRUID_DESC"
        class Druid
    }
}
```

---

### `STARTER_PLACEHOLDER_Psychic`
**Name:** ???  
**Description:** Becomes a random Psychic starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Psychic {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_PSYCHIC_DESC"
        class Psychic
    }
}
```

---

### `STARTER_PLACEHOLDER_Tinkerer`
**Name:** ???  
**Description:** Becomes a random Tinkerer starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Tinkerer {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_TINKERER_DESC"
        class Tinkerer
    }
}
```

---

### `STARTER_PLACEHOLDER_Colorless`
**Name:** ???  
**Description:** Becomes a random Collarless starter ability when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Colorless {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_COLORLESS_DESC"
        class Colorless
    }
}
```

---

### `STARTER_PLACEHOLDER_Jester`
**Name:** ???  
**Description:** Becomes a random ability from any class when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
STARTER_PLACEHOLDER_Jester {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_STARTER_PLACEHOLDER_JESTER_DESC"
        class Colorless
    }
}
```

---

### `ATTACK_PLACEHOLDER_JesterBasic`
**Name:** ???  
**Description:** Becomes a random class basic attack when you lock in your team's collars.  
**Source:** `util_abilities.gon`  

```
ATTACK_PLACEHOLDER_JesterBasic {
    template placeholder
    
    meta {
        name "ABILITY_STARTER_PLACEHOLDER_NAME"
        desc "ABILITY_ATTACK_PLACEHOLDER_JESTERBASIC_DESC"
        class Colorless
    }
}
```

---

## File: `abilities.gon`

### `None`
**Name:** None  
**Description:** nothing  
**Source:** `abilities.gon`  

```
None {
    template melee_attack
    
    meta {
        name "None"
        desc "nothing"
    }

    damage {
        damage 0
        type none
    }
}
```

---

## File: `ability_templates.gon`

### `template_move`
**Source:** `ability_templates.gon`  

```
template_move {
    class MoveAbility

    meta {
        type_icon "movement"
        is_move true
    }
    
    cost {
        move_points 1
        act_points 0
    }

    graphics {
        use_super_armor false
    }
    
    target { 
        target_mode tile  //tile, direction, none
        
        range_mode ground_move
        min_range 0
        max_range mov
        
        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        
        range_display_include_character_size true
        
        restrictions [must_be_moveable must_move]
    }
    
}
```

---

### `template_teleport`
**Source:** `ability_templates.gon`  

```
template_teleport {
    class TeleportAbility

    meta {
        type_icon "movement"
        is_move auto
    }
    
    cost {
        move_points 1
        act_points 0
    }

    graphics {
        use_super_armor false
    }

    target { 
        target_mode tile  //tile, direction, none
        
        range_mode standard
        min_range 1
        max_range mov
        
        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        
        range_display_include_character_size true
        
        restrictions must_be_moveable
    }
}
```

---

### `template_swap`
**Source:** `ability_templates.gon`  

```
template_swap {
    class SwapperAbility

    meta {
        type_icon "movement"
    }
    
    cost {
        move_points 1
        act_points 0
    }

    graphics {
        use_super_armor false
    }
    
    target { 
        target_mode tile  //tile, direction, none
        
        range_mode standard
        min_range 1
        max_range mov
        
        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        
        range_display_include_character_size true
        
        restrictions must_be_swappable
    }
    
}
```

---

### `template_melee_attack`
**Source:** `ability_templates.gon`  

```
template_melee_attack {
    class MeleeAttackAbility
    graphics {
        animation Default
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode direction  //tile, direction, none
        
        aoe_mode line //standard, line, cross, custom
        min_aoe 1
        max_aoe 1
        
        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        type melee
        incidentally_collects_pickups true
    }
}
```

---

### `template_ranged_attack`
**Source:** `ability_templates.gon`  

```
template_ranged_attack {
    class RangedAttackAbility
    graphics {
        animation shoot
        projectile Default
        lob_height 0
        speed 15
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode tile  //tile, direction, none
        min_range 1
        max_range 4+bonus_range
        
        min_aoe 0
        max_aoe 0

        knockback_mode character_to_tile
        restrictions must_have_line_of_sight

        can_multihit true
    }
    
    damage_instance {
        damage 5+bonus_ranged_damage
        type ranged
    }
}
```

---

### `template_lobbed_attack`
**Source:** `ability_templates.gon`  

```
template_lobbed_attack {
    class RangedAttackAbility
    graphics {
        animation shoot
        projectile LobbedProjectile
        speed 7
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode tile  //tile, direction, none
        min_range 1
        max_range 4+bonus_range
        
        min_aoe 0
        max_aoe 0

        knockback_mode character_to_tile
        restrictions none

        can_multihit true
    }
    
    damage_instance {
        damage 5+bonus_ranged_damage
        type ranged
    }
}
```

---

### `template_spell`
**Source:** `ability_templates.gon`  

```
template_spell {
    class AOESpellAbility
    graphics {
        animation meow
        particle Spike
        delay 0
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode tile  //tile, direction, none
        min_range 0
        max_range 4
        
        min_aoe 0
        max_aoe 1

        knockback_mode target_to_tile
    }
    
    damage_instance {
        type spell
    }
}
```

---

### `template_melee_spell`
**Source:** `ability_templates.gon`  

```
template_melee_spell {
    class AOESpellAbility
    graphics {
        animation attack
        particle Spike
        delay 0
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode direction  //tile, direction, none
        
        aoe_mode line //standard, line, cross, custom
        min_aoe 1
        max_aoe 1
        
        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode character_to_tile
    }
    
    damage_instance {
        type spell
    }
}
```

---

### `template_dash_attack`
**Source:** `ability_templates.gon`  

```
template_dash_attack {
    class DashAttackAbility
    graphics {
        animation attack
    }

    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode direction  //tile, direction, none
        
        aoe_mode line //standard, line, cross, custom
        min_aoe 1
        max_aoe 1
        max_range 10
        
        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode orientation
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        type melee
        incidentally_collects_pickups true
    }
}
```

---

### `template_trample_dash`
**Source:** `ability_templates.gon`  

```
template_trample_dash {
    class TrampleDashAbility
    graphics {

    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode direction  //tile, direction, none
        
        aoe_mode line //standard, line, cross, custom
        min_aoe 1
        max_aoe 1
        max_range 10

        knockback_mode zero
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        type trample
    }
}
```

---

### `template_spawn`
**Source:** `ability_templates.gon`  

```
template_spawn {
    class SpawnAbility
    meta {
        type_icon "spawn"
        icon_shell_frame nodamage
    }

    graphics {
        animation throwobject
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode tile  //tile, direction, none
        min_range 1
        max_range 1
        
        min_aoe 0
        max_aoe 0

        range_excludes_blocking true
        aoe_restrictions [exclude_blocking]

        hint_can_target_empty true
    }
    
    damage_instance {
        type spawn
        damage 5 //doesnt actually do damage, this is just "how much the spawn is worth" for the AI
        layer characters
        faction auto
    }
}
```

---

### `template_self_buff`
**Source:** `ability_templates.gon`  

```
template_self_buff {
    class AOESpellAbility
    graphics {
        animation meow
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode none  //tile, direction, none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 0
    }
    
    damage_instance {
        type status_spell
        damage 0
        layer self
        cant_miss true
    }
}
```

---

### `template_targeted_status`
**Source:** `ability_templates.gon`  

```
template_targeted_status {
    class AOESpellAbility
    graphics {
        animation meow
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode tile  //tile, direction, none
        min_range 1
        max_range 4
        
        min_aoe 0
        max_aoe 0
    }
    
    damage_instance {
        type status_spell
        damage 0
        cant_miss true
    }
}
```

---

### `template_jump_attack`
**Source:** `ability_templates.gon`  

```
template_jump_attack {
    class JumpAttackAbility
    meta {
        is_move auto
    }

    graphics {
        animation Default
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode tile  //tile, direction, none
        
        aoe_mode cross //standard, line, cross, custom
        min_aoe 1
        max_aoe 1
        
        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode character_to_tile

        range_display_include_character_size true
        restrictions must_be_moveable
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        type melee
    }
}
```

---

### `template_jump_move`
**Source:** `ability_templates.gon`  

```
template_jump_move {
    class JumpAttackAbility
    meta {
        is_move true
    }

    graphics {
        animation Default
    }
    
    cost {
        move_points 1
        act_points 0
    }
    
    target { 
        target_mode tile  //tile, direction, none

        min_range 1
        max_range mov
        
        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        
        aoe_considers_character_size false
        aoe_excludes_self true

        knockback_mode character_to_tile

        range_display_include_character_size true
        range_considers_character_size false
        restrictions must_be_moveable
    }
    
    damage_instance {
        type none
        damage 0
    }
}
```

---

### `template_throw_attack`
**Source:** `ability_templates.gon`  

```
template_throw_attack {
    class ThrowAbility
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode tile  //tile, direction, none
        min_range 1
        max_range 5
        
        min_aoe 0
        max_aoe 0

        knockback_mode character_to_target
        restrictions must_be_empty
    }
    
    damage_instance {
        damage 1
        type knockblock
        makes_contact false
    }
}
```

---

### `template_straightshot_attack`
**Source:** `ability_templates.gon`  

```
template_straightshot_attack {
    class StraightShotRanged
    graphics {
        animation shoot
        projectile SpikeProjectile
        lob_height 0
        speed 20
    }

    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode direction  //tile, direction, none
        min_aoe 0
        max_aoe 10

        knockback_mode character_to_tile

        can_multihit true
    }
    
    damage_instance {
        damage 5+bonus_ranged_damage
        type ranged
    }
}
```

---

### `template_leave`
**Source:** `ability_templates.gon`  

```
template_leave {
    class GoOffMapAbility

    meta {
        type_icon "movement"
        animate_name false
    }
    
    cost {
        move_points 0
        act_points 1
    }

    target { 
        target_mode none

    }
}
```

---

### `template_return`
**Source:** `ability_templates.gon`  

```
template_return {
    class ReturnToMapAbility

    meta {
        type_icon "movement"
        animate_name false
    }
    
    cost {
        move_points 0
        act_points 1
        allow_offmap_casts true
        must_be_offmap true
    }
    
    target { 
        target_mode tile  //tile, direction, none
        
        range_mode standard
        min_range 0
        max_range mov
        
        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        
        range_display_include_character_size true
        range_considers_character_size false
        
        restrictions must_be_moveable 
        allow_any_orientation true
    }
}
```

---

### `template_placeholder`
**Source:** `ability_templates.gon`  

```
template_placeholder {
    class MeleeAttackAbility
    graphics {
        animation Default
    }
    
    cost {
        move_points 0
        act_points 1
        mana 0
    }

    damage_instance {
        damage 0
        type  none
    }
}
```

---

### `template_tile_targeted_melee_attack`
**Source:** `ability_templates.gon`  

```
template_tile_targeted_melee_attack {
    class MeleeAttackAbility
    graphics {
        animation Default
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode tile  //tile, direction, none
        min_range 1
        max_range 1

        min_aoe 0
        max_aoe 0

        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        type melee
        incidentally_collects_pickups true
    }
}
```

---

### `template_laser`
**Source:** `ability_templates.gon`  

```
template_laser {
    class LaserAbility

    graphics {
        animation meow

        beam_clip thinlaser
        beam_cap thinlasercap
    }

    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode direction  //tile, direction, none
        min_aoe 1
        max_aoe 10

        knockback_mode target_to_tile
        upgrade_straight_shot_to_piercing true
    }
    
    damage_instance {
        damage 5
        type spell
    }
}
```

---

### `template_multihit_self_buff`
**Source:** `ability_templates.gon`  

```
template_multihit_self_buff {
    class MeleeAttackAbility
    graphics {
        animation meow
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target { 
        target_mode none  //tile, direction, none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 0
    }
    
    damage_instance {
        type status_spell
        damage 0
        layer self
        cant_miss true
    }
}
```

---

