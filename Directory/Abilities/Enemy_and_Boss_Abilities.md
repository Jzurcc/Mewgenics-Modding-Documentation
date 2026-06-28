# Abilities/Enemy and Boss Abilities Directory

## File: `finalboss_abilities.gon`

### `TheCreator_SpawnCloneTeam`
**Source:** `finalboss_abilities.gon`  

```
TheCreator_SpawnCloneTeam {
    template spawn

    tags [summon]
    
    graphics {
        lob false
        animation summon
        dont_visualize_ai true
    }

    target {
        target_mode none
        min_range 1
        max_range 1
        max_aoe 0

        aoe_mode all
        restructions aoe_must_exist
        aoe_restrictions must_have_special_tag
        special_tile_tag FinalBossCloneSpot
        shuffle_tile_order true
    }

    spawn {
        object PlayerCat_FinalBossClone
        first_turn initiative
        inherit_elite_buffs false

        catdata teamclone
        trigger_battle_start true
        clone_items true //"disallow_items" tag is used to govern this on the spawned clone so hard mode ones can have items minus nuke
        face_camera true
    }
}
```

---

### `TheCreator_Reaction`
**Source:** `finalboss_abilities.gon`  

```
TheCreator_Reaction {
    template spell

    graphics {
        animation reaction
        particle none
    }

    target {
        target_mode none
        min_aoe 0
        max_aoe 20
        aoe_excludes_self true
        aoe_considers_character_size true
    }
    
    damage_instance {
        damage 0
        knockback 10
    }
}
```

---

### `BecomeTheDestroyer`
**Source:** `finalboss_abilities.gon`  

```
BecomeTheDestroyer {
    template self_buff

    graphics {
        animation transform
    }

    damage_instance {
        effects {
            ClearFinalBossBattlefield 1
            PlayBackground 0
            PopAndSpawn TheDestroyer
            SwitchMusic {
                new_song same
                new_layer map
            }
        }
    }
}
```

---

### `DestroyerAttack`
**Source:** `finalboss_abilities.gon`  

```
DestroyerAttack {
    variant_of BasicBigMelee

    graphics {
        animation swipe
    }
}
```

---

### `DestroyerAttack2`
**Source:** `finalboss_abilities.gon`  

```
DestroyerAttack2 {
    variant_of BasicBigMelee

    graphics {
        animation swipe
    }

    target {
        multihit 2
    }
}
```

---

### `DestroyerShieldBash`
**Source:** `finalboss_abilities.gon`  

```
DestroyerShieldBash {
    variant_of BasicBigMelee

    graphics {
        animation bash
    }
    damage_instance {
        damage 0
        knockback 10
    }
}
```

---

### `DestroyerHolyAttack`
**Name:** Holy Blast  
**Source:** `finalboss_abilities.gon`  

```
DestroyerHolyAttack {
    template spell

    meta {
        name "EABILITY_HOLYBLAST_NAME"
    }

    graphics {
        prime_animation chargeholy
        custom_priming_animation priming
        animation holy
        dont_visualize_ai true
        particle Holybeam
        delay 6
    }
    
    cost {
        cantrip true
        prime 1
    }

    target {
        target_mode none
        aoe_considers_character_size true
        aoe_excludes_self true
        min_aoe 1
        max_aoe 4
        prioritize_face_camera true
    }

    self_damage {
        effects {
            RemoveActPoints 1
        }
    }

    damage_instance {
        damage 16
        ai_base_score 9999
    }
}
```

---

### `DestroyerPulse`
**Source:** `finalboss_abilities.gon`  

```
DestroyerPulse {
    template spell

    graphics {
        particle none
        animation pulse
    }

    target {
        target_mode none
        aoe_considers_character_size true
        aoe_excludes_self true
        min_aoe 1
        max_aoe 4
    }

    damage_instance {
        damage 0 
        knockback 1
    }
}
```

---

### `DestroyerThrowShield`
**Source:** `finalboss_abilities.gon`  

```
DestroyerThrowShield {
    template lobbed_attack

    graphics {
        animation throwshield
        projectile FinalBossShieldProjectile
        speed 15
        use_rotation false
        lob_height 1
    }

    target {
        min_range 1
        max_range 20
    }

    bonus_passives {
        AbilityEnabledAtHealthThreshold 50%
    }

    self_damage {
        effects {
            CancelPrimedAbilities 1
            SignalFinalBossShieldBroke 1
            FaceCamera 1

            TimeDelayStatusApplication {
                delay 1.13333

                FormChange DualSword

                SwitchMusic {
                    new_song same
                    new_layer battle
                }

                CreateGlobalModifiers {
                    LowerAmbientLight {
                        amount [50% 60% 60%]
                        speed 4
                    }
                    BloodRain 1
                }
            }
        }
    }

    damage_instance {
        damage 99 

        effects {
            Conditional_HasTag {
                tag the_nuke_bearer
                OverrideDamage 1
            }
        }
    }
}
```

---

### `DestroyerBreakShield`
**Source:** `finalboss_abilities.gon`  

```
DestroyerBreakShield {
    template self_buff

    graphics {
        animation breakshield
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            CancelPrimedAbilities 1
            SignalFinalBossShieldBroke 1
            FormChange DualSword
            FaceCamera 1

            SwitchMusic {
                new_song same
                new_layer battle
            }

            CreateGlobalModifiers {
                LowerAmbientLight {
                    amount [50% 60% 60%]
                    speed 4
                }
                BloodRain 1
            }
        }
    }
}
```

---

### `Destroyer2HolyAttack`
**Source:** `finalboss_abilities.gon`  

```
Destroyer2HolyAttack {
    template spell

    graphics {
        prime_animation chargeholy
        custom_priming_animation priming
        animation holy
        dont_visualize_ai true
        particle Holybeam
        delay 6
    }
    
    cost {
        cantrip true
        prime 1
    }

    target {
        target_mode none
        aoe_considers_character_size true
        aoe_excludes_self true
        min_aoe 1
        max_aoe 4
        prioritize_face_camera true
    }

    self_damage {
        effects {
            RemoveActPoints 1
        }
    }

    damage_instance {
        damage 16
        ai_base_score 9999
    }
}
```

---

### `Destroyer2Pulse`
**Source:** `finalboss_abilities.gon`  

```
Destroyer2Pulse {
    template spell

    graphics {
        particle none
        animation pulse
    }

    target {
        target_mode none
        aoe_considers_character_size true
        aoe_excludes_self true
        min_aoe 1
        max_aoe 4
    }

    damage_instance {
        damage 0 
        knockback 1
    }
}
```

---

### `DestroyerDodge`
**Source:** `finalboss_abilities.gon`  

```
DestroyerDodge {
    template move

    graphics {
        sync_speed 28
        max_tiles_single_loop 6
        ignore_slowtiles true
        move_start_animation none
        animation dodge
        move_end_animation none
        dont_orient true

        use_directional_animations true
        use_super_armor true
    }

    target {
        range_mode cross
        max_range 2
        min_range 2
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_any_orientation true
        range_considers_character_size false
    }
}
```

---

### `DestroyerChargeBackflips`
**Name:** Precognition  
**Source:** `finalboss_abilities.gon`  

```
DestroyerChargeBackflips {
    template self_buff

    meta {
        name "EABILITY_PRECOGNITION_NAME"
    }

    graphics {
        animation chargedodges
    }

    cost {
        cantrip true
    }

    bonus_passives {
        AbilityEnabledIfNotHasStatus BackflipWhenTargeted
    }

    target {
        prioritize_dont_change_direction true
    }

    damage_instance {
        effects {
            BackflipWhenTargeted {
                stacks 4
                ability DestroyerDodge
            }
        }
    }
}
```

---

### `DestroyerDashAttack`
**Name:** Annihilation  
**Source:** `finalboss_abilities.gon`  

```
DestroyerDashAttack {
    template dash_attack

    meta {
        name "EABILITY_ANNIHILATION_NAME"
    }
    
    graphics {
        dash_start_animation dashbegin
        dash_animation dashing
        //dash_end_animation dashend
        dash_attack_animation dashattack
    }
    
    cost {
        mana 0
    }
    
    target {
        max_range 10
        consider_trample false
        multihit 4

        aoe_mode square
        knockback_mode character_to_tile
        max_aoe 1
    }
    
    damage_instance {
        damage 2+bonus_melee_damage
    }
}
```

---

### `DestroyerRaise`
**Name:** Rise  
**Source:** `finalboss_abilities.gon`  

```
DestroyerRaise {
    template spell

    meta {
        name "EABILITY_RISE_NAME"
    }

    graphics {
        animation raise
        particle HealBig
        dont_visualize_ai true
    }

    cost {
        cantrip true
    }

    target {
        target_mode none
        aoe_mode all
        aoe_restrictions [must_have_player_cat must_have_corpse]
        restrictions aoe_must_exist
        prioritize_face_camera true
    }

    damage_instance {
        effects {
            Revive 50%
            FlatAIBonus 999999
        }
    }
}
```

---

### `TheChild_ReleaseBeams`
**Name:** Purity  
**Source:** `finalboss_abilities.gon`  

```
TheChild_ReleaseBeams {
    template spell

    meta {
        name "EABILITY_PURITY_NAME"
    }

    graphics {
        animation holy
        particle Holybeam
        dont_visualize_ai true
        delay 5
    }

    cost {
        cantrip true
    }

    target {
        max_aoe 1
        max_range 20
        min_range 0
        multihit 10 //"FinalBossBeamQueue" governs switching targets during this
    }

    damage_instance {
        damage 10

        effects {
            IgnoreSelf 1
        }
        elements [
            Holy
        ]
    }
}
```

---

### `TheChild_TargetBeam`
**Source:** `finalboss_abilities.gon`  

```
TheChild_TargetBeam {
    template targeted_status

    graphics {
        animation chargeholy
        particle none
    }

    target {
        max_aoe 0
        max_range 20
        min_range 0
    }

    damage_instance {
        layer tiles
        effects {
            FinalBossQueueBeam 1
        }
    }
}
```

---

### `TheChild_TransformHoly`
**Source:** `finalboss_abilities.gon`  

```
TheChild_TransformHoly {
    template self_buff

    graphics {
        animation transform1
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            Cleanse 0
            FormChange Holy
        }
    }
}
```

---

### `TheChild_TransformExplosive`
**Source:** `finalboss_abilities.gon`  

```
TheChild_TransformExplosive {
    template self_buff

    graphics {
        animation transform3
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            Cleanse 0
            FormChange Explosive
        }
    }
}
```

---

### `TheChild_TransformBoris`
**Source:** `finalboss_abilities.gon`  

```
TheChild_TransformBoris {
    template self_buff

    graphics {
        animation transform2
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            Cleanse 0
            FormChange Boris
        }
    }
}
```

---

### `MegaGuppy_TransformHoly`
**Source:** `finalboss_abilities.gon`  

```
MegaGuppy_TransformHoly {
    template self_buff

    graphics {
        animation transform1
    }

    cost {
        cantrip true
        allow_offmap_casts true
    }

    self_damage {
        effects {
            Cleanse 0
            FormChange Holy
            SetCrazyEyeBackgroundWeights {
                weights [1 0 0]
            }
        }
    }
}
```

---

### `MegaGuppy_TransformExplosive`
**Source:** `finalboss_abilities.gon`  

```
MegaGuppy_TransformExplosive {
    template self_buff

    graphics {
        animation transform3
    }

    cost {
        cantrip true
        allow_offmap_casts true
    }

    self_damage {
        effects {
            Cleanse 0
            FormChange Explosive
            SetCrazyEyeBackgroundWeights {
                weights [0 0 1]
            }
        }
    }
}
```

---

### `MegaGuppy_TransformBoris`
**Source:** `finalboss_abilities.gon`  

```
MegaGuppy_TransformBoris {
    template self_buff

    graphics {
        animation transform2
    }

    cost {
        cantrip true
        allow_offmap_casts true
    }

    self_damage {
        effects {
            Cleanse 0
            FormChange Boris
            SetCrazyEyeBackgroundWeights {
                weights [0 1 0]
            }
        }
    }
}
```

---

### `TheChild_Wrath`
**Name:** Wrath  
**Source:** `finalboss_abilities.gon`  

```
TheChild_Wrath {
    template spell

    meta {
        name "EABILITY_WRATH_NAME"
    }

    graphics {
        animation holy
        particle Holybeam
        dont_visualize_ai true
        delay 6
    }

    cost {
        cantrip true
    }

    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_line_of_sight
    }

    self_damage {
        effects {
            ExistUntilIdleUpkeep 1 //mute danger AOE
        }
    }

    damage_instance {
        damage 12

        elements [
            Holy
        ]
    }
}
```

---

### `TheChild_Pulse`
**Name:** Pulse  
**Source:** `finalboss_abilities.gon`  

```
TheChild_Pulse {
    template spell

    meta {
        name "EABILITY_PULSE_NAME"
    }

    graphics {
        animation pulse
        particle none
        dont_visualize_ai true
    }

    cost {
        cantrip true
    }

    target {
        target_mode none
        aoe_mode circle
        min_aoe 0
        max_aoe 20
        aoe_excludes_self true
        aoe_considers_character_size true
        distance_sort_targets true
        aoe_restrictions must_have_animate_character
    }

    damage_instance {
        damage 0
        knockback 10
    }

    self_damage {
        effects {
            DoDistortionRing {
                speed 20
                intensity 1
                radius 5
            }
        }
    }
}
```

---

### `MegaGuppy_SlamRight`
**Name:** Slam  
**Source:** `finalboss_abilities.gon`  

```
MegaGuppy_SlamRight {
    template spell
    chain_ability MegaGuppy_DropTrash

    meta {
        name "EABILITY_SLAM_NAME"
        is_basic_attack true
    }

    graphics {
        animation attackL
        particle none
        dont_visualize_ai true
    }

    cost {
        cantrip true
        allow_offmap_casts true
    }

    target {
        target_mode none
        aoe_mode all
        knockback_mode orientation
        aoe_restrictions must_have_animate_character

        /*visual_delay_but_simultaneous_damage 50
        delay_from_map_edge true
        delay 5*/
    }

    self_damage {
        effects {
            TimeDelayStatusApplication {
                delay .25

                DoScreenShake {
                    time 2
                    intensity 10
                }
            }
        }
    }

    damage_instance {
        damage 0
        knockback 10

        effects {
            OverrideKnockbackDamage 3
            FastKnockback 4
            Conditional_HasTag {
                tag god
                IgnoreDamage 1
            }
            Conditional_HasTag {
                tag angeljunk
                IgnoreDamage 1
            }
        }

        ai_base_score 999999
    }
}
```

---

### `MegaGuppy_SlamLeft`
**Source:** `finalboss_abilities.gon`  

```
MegaGuppy_SlamLeft {
    variant_of MegaGuppy_SlamRight

    graphics {
        animation attackR
    }

    target {
        knockback_mode right_orientation
    }
}
```

---

### `MegaGuppy_DropTrash`
**Source:** `finalboss_abilities.gon`  

```
MegaGuppy_DropTrash {
    template spawn

    graphics {
        fall_from_sky true
        fall_randomize_timing .3
        animation none

        precast_delay .25
    }
    
    cost {
        mana 0
        allow_offmap_casts true
    }
    
    target {
        target_mode none
        aoe_mode all
        max_aoe 20
        max_targets 7
        knockback_mode random
    }

    spawn {
        object Cherub_FinalBoss
        start_dead true
    }
}
```

---

### `MegaGuppy_SummonTheChild`
**Source:** `finalboss_abilities.gon`  

```
MegaGuppy_SummonTheChild {
    template spawn

    graphics {
        lob false
        //fall_from_sky true
        animation spawnChild
    }
    
    cost {
        mana 0
        allow_offmap_casts true
    }
    
    target {
        target_mode tile
        range_mode special_tagged_tiles
        special_tile_tag FinalBossTheChildLocation
        knockback_mode orientation
        restrictions none
        range_excludes_blocking false
        aoe_restrictions none
    }

    spawn {
        object TheChild
    }

    damage_instance {
        damage 0
        ai_base_score 999999
    }
}
```

---

## File: `guillotina_abilities.gon`

### `YeetTowardsBuddy`
**Name:** Toss  
**Source:** `guillotina_abilities.gon`  

```
YeetTowardsBuddy {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        animation throw
        use_placeholder true
        face_toss_target true
    }

    cost {
        mana 0
    }
    
    target {
        max_range 7
        restrictions none
    }
    
    damage_instance {
        damage 1
        blocked_damage 5+bonus_melee_ability_damage

        custom_additional_ai_weight toss_towards_buddy
    }
}
```

---

### `GuillotinaTossCollide`
**Name:** Toss  
**Source:** `guillotina_abilities.gon`  

```
GuillotinaTossCollide {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        animation throw
        use_placeholder true
        face_toss_target true
    }

    cost {
        mana 0
    }
    
    target {
        max_range 7
        restrictions none
    }
    
    damage_instance {
        damage 1
        blocked_damage 5+bonus_melee_ability_damage

        custom_additional_ai_weight toss_far
    }
}
```

---

### `Magnetize_AI`
**Name:** Gasp  
**Source:** `guillotina_abilities.gon`  

```
Magnetize_AI {
    template spell

    meta {
        name "EABILITY_GASP_NAME"
    }
    
    cost {
        mana 0
    }

    graphics {
        particle fx_windSpell
        animation suck
    }
    
    target {
        target_mode direction

        aoe_mode custom
        custom_aoe [
                     [1, 1], [2, 1], [3, 1], [4, 1], [5, 1], [6, 1], [7, 1], [8, 1], [9, 1], [10, 1]
                     [1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0], [8, 0], [9, 0], [10, 0]
                     [1,-1], [2,-1], [3,-1], [4,-1], [5,-1], [6,-1], [7,-1], [8,-1], [9,-1], [10,-1]
                   ]

        knockback_mode perp_towards_facing //have the middle be 0,0 for the purposes of magnetize_favorlineup
        
    }
    
    damage_instance {
        damage 0
        knockback 0 //we don't want the ability to actually consider knockback here even though the real one does
        custom_additional_ai_weight magnetize_favorlineup
        
        elements [
            Wind
        ]
    }
}
```

---

### `Magnetize`
**Name:** Gasp  
**Source:** `guillotina_abilities.gon`  

```
Magnetize {
    template spell
    ai_ability Magnetize_AI

    meta {
        name "EABILITY_GASP_NAME"
    }
    
    cost {
        mana 0
    }

    graphics {
        particle fx_windSpell
        animation suck

        visual_delay_but_simultaneous_damage 10
        delay 2
    }
    
    target {
        target_mode direction

        aoe_mode custom
        custom_aoe [
                     [1, 1], [2, 1], [3, 1], [4, 1], [5, 1], [6, 1], [7, 1], [8, 1], [9, 1], [10, 1]
                     [1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0], [8, 0], [9, 0], [10, 0]
                     [1,-1], [2,-1], [3,-1], [4,-1], [5,-1], [6,-1], [7,-1], [8,-1], [9,-1], [10,-1]
                   ]

        knockback_mode perp_towards_facing_middle_pull
        
    }
    
    damage_instance {
        damage 0
        knockback 1
        custom_additional_ai_weight magnetize_favorlineup
        
        elements [
            Wind
        ]
    }
}
```

---

### `TinaHeadGutSpear`
**Source:** `guillotina_abilities.gon`  

```
TinaHeadGutSpear {
    template melee_attack

    graphics {
        animation attack
        detatched_animation TinaSpear
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
        contact_requires_adjacency false
    }
}
```

---

### `TinaBodySlamMax`
**Source:** `guillotina_abilities.gon`  

```
TinaBodySlamMax {
    template jump_attack

    graphics {
        //jump_start_animation leapattackwindup
        full_jump_animation attack
        full_jump_sync_frames 38
        full_jump_windup_frames 13
    }

    cost {
        act_points 1
    }
    
    target {
        max_range 2
        min_range 2
        range_mode cross
        range_considers_character_size false
        min_aoe 0
        max_aoe 0
    }

    temporary_effects {
        DisableTrample 1
    }

    damage_instance {
        type melee
        damage 5+bonus_melee_damage
        knockback 10

        effects {
            IgnoreSelf 1
            Bruise 1
            Stun [1 .5]
        }
    }
}
```

---

### `TinaBodySlam`
**Source:** `guillotina_abilities.gon`  

```
TinaBodySlam {
    template jump_attack

    graphics {
        //jump_start_animation leapattackwindup
        full_jump_animation attack
        full_jump_sync_frames 38
        full_jump_windup_frames 13
    }

    cost {
        act_points 1
    }
    
    target {
        max_range 2
        min_range 1
        range_mode cross
        range_considers_character_size false
        min_aoe 0
        max_aoe 0
    }

    temporary_effects {
        DisableTrample 1
    }

    damage_instance {
        type melee
        damage 5+bonus_melee_damage
        knockback 10

        effects {
            IgnoreSelf 1
            Bruise 1
            Stun [1 .5]
        }
    }
}
```

---

### `TinaBodySlamRage`
**Source:** `guillotina_abilities.gon`  

```
TinaBodySlamRage {
    template jump_attack

    graphics {
        //jump_start_animation leapattackwindup
        full_jump_animation attack
        full_jump_sync_frames 49
        full_jump_windup_frames 13
    }

    cost {
        act_points 1
    }
    
    target {
        max_range 3
        min_range 1
        range_considers_character_size false
        min_aoe 0
        max_aoe 0
    }

    temporary_effects {
        DisableTrample 1
    }

    damage_instance {
        type melee
        damage 5+bonus_melee_damage
        knockback 10

        effects {
            IgnoreSelf 1
            Bruise 1
            Stun [1 .5]
        }
    }
}
```

---

### `Guillotina2Rage`
**Source:** `guillotina_abilities.gon`  

```
Guillotina2Rage {
    template self_buff

    graphics { 
        dont_orient true
        animation react
        particle Cleanse
    }

    damage_instance {
        heal 100
        effects {
            FormChange {
                form Rage
            }
            Cleanse 0
            MaxHPUp 100
        }
        ai_base_score 9999
    }
}
```

---

### `TinaTantrum`
**Name:** Tantrum  
**Source:** `guillotina_abilities.gon`  

```
TinaTantrum {
    template spawn

    meta {
        name "EABILITY_TANTRUM_NAME"
    }
    
    graphics {
        fall_from_sky true
        fall_randomize_timing .3
        animation tantrum
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        max_targets 15

        multihit 5
        stagger_multihit_targets true
    }

    spawn {
        object Junk
    }
}
```

---

### `Tina2Call`
**Name:** Call  
**Source:** `guillotina_abilities.gon`  

```
Tina2Call {
    template spell

    meta {
        name "EABILITY_CALL_NAME"
    }

    graphics {
        particle none
        animation call
        dont_visualize_ai true
    }
    
    cost {
        mana 0
    }
    
    target {
        max_aoe 0
        max_range 20

        knockback_mode pull_to_character
        restrictions must_have_buddy
    }
    
    damage_instance {
        damage 0
    }
}
```

---

### `TinaSuck`
**Source:** `guillotina_abilities.gon`  

```
TinaSuck {
    template targeted_status

    graphics {
        animation suck1
    }

    cost {
        mana 0
        must_not_be_consuming true
    }

    target {
        max_range 20
        range_mode cross
        restrictions must_have_line_of_sight
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                struggle_ability TinaFlail
                force_contact true
                wet true
            }
            GenericDebuff 1 //for AI
        }
    }
}
```

---

### `TinaSpit`
**Name:** Spit  
**Source:** `guillotina_abilities.gon`  

```
TinaSpit {
    template throw_attack
    
    meta {
        name "EABILITY_SPIT_NAME"
    }

    graphics {
        animation shoot
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        max_range 5
        min_range 3
        range_mode cross
        restrictions none
        prioritize_dont_change_direction true
        throw_consumed_character true
    }
    
    damage_instance {
        damage 1
        blocked_damage 5+bonus_melee_ability_damage
        ai_base_score 9999

        custom_additional_ai_weight toss_far
    }
}
```

---

### `TinaSuck2`
**Source:** `guillotina_abilities.gon`  

```
TinaSuck2 {
    template targeted_status

    graphics {
        animation suck2
    }

    cost {
        mana 0
        must_not_be_consuming true
    }

    target {
        max_range 20
        restrictions must_have_line_of_sight
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                struggle_ability TinaFlailRage
                force_contact true
                wet true
            }
            GenericDebuff 1 //for AI
        }
    }
}
```

---

### `TinaSpit2`
**Name:** Spit  
**Source:** `guillotina_abilities.gon`  

```
TinaSpit2 {
    template throw_attack
    
    meta {
        name "EABILITY_SPIT_NAME"
    }

    graphics {
        animation shoot
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        max_range 5
        min_range 3
        restrictions none
        throw_consumed_character true
        prioritize_dont_change_direction true
        range_mode cross

    }
    
    damage_instance {
        damage 1
        blocked_damage 5+bonus_melee_ability_damage
        ai_base_score 9999

       // custom_additional_ai_weight toss_far
    }
}
```

---

### `BellyPound`
**Name:** Belly Pound  
**Source:** `guillotina_abilities.gon`  

```
BellyPound {
    template self_buff
    class DamageConsumedCharactersAbility

    meta {
        name "EABILITY_BELLYPOUND_NAME"
        animate_name true
    }

    cost {

    }

    graphics {
        animation bellypound
    }
    
    
    target {
        target_mode none
        knockback_mode none
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee
        contact_requires_adjacency false
        ai_base_score 9999
    }
}
```

---

### `Digest`
**Name:** Digest  
**Source:** `guillotina_abilities.gon`  

```
Digest {
    template self_buff
    class DamageConsumedCharactersAbility

    meta {
        name "EABILITY_DIGEST_NAME"
        animate_name true
    }

    cost {

    }

    graphics {
        animation digest
    }
    
    
    target {
        target_mode none
        knockback_mode none
    }

    self_damage {
        heal 25
    }

    damage_instance {
        damage 0
        type melee
        cant_miss true
        ai_base_score 9999
        effects {
            Vaporize 1
        }
    }
}
```

---

### `TinaBasicJump`
**Source:** `guillotina_abilities.gon`  

```
TinaBasicJump {
    template jump_attack

    graphics {
        //jump_start_animation leapattackwindup
        full_jump_animation jumpmove
        full_jump_sync_frames 46
        full_jump_windup_frames 22
    }

    cost {
        move_points 1
        act_points 0
    }
    
    target {
        max_range mov
        min_range 1
        range_considers_character_size false
        range_display_include_character_size true
        aoe_considers_character_size false

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0

        restrictions must_be_moveable
    }

    damage_instance {
        type none
        damage 0
    }
}
```

---

### `TinaJumpAttack`
**Source:** `guillotina_abilities.gon`  

```
TinaJumpAttack {
    template jump_attack

    graphics {
        //jump_start_animation leapattackwindup
        full_jump_animation jumpattack
        full_jump_sync_frames 37
        full_jump_windup_frames 20
    }

    cost {
        act_points 1
    }
    
    target {
        max_range 3
        min_range 1
        range_considers_character_size false
        min_aoe 0
        max_aoe 0
    }

    temporary_effects {
        DisableTrample 1
    }

    damage_instance {
        type melee
        damage 5+bonus_melee_damage
        knockback 4

        effects {
            IgnoreSelf 1
            Bruise 1
        }
    }
}
```

---

### `TinaBasicBigMelee`
**Source:** `guillotina_abilities.gon`  

```
TinaBasicBigMelee {
    template melee_attack

    target { 
        max_aoe 1
    }

    damage_instance {
        knockback 10
    }
}
```

---

### `TinaBasicBigMeleeA`
**Source:** `guillotina_abilities.gon`  

```
TinaBasicBigMeleeA {
    variant_of TinaBasicBigMelee

    graphics {
        animation attackRage
    }
}
```

---

### `Guillotina1Rage`
**Source:** `guillotina_abilities.gon`  

```
Guillotina1Rage {
    template self_buff

    cost {
        requires_hp_threshold 200
    }

    graphics { 
        dont_orient true
        animation enrage
        particle Cleanse
    }

    damage_instance {
        heal 50

        effects {
            FormChange {
                form Rage
            }
            Cleanse 0
            MaxHPUp 100
        }
        ai_base_score 9999
    }
}
```

---

### `TinaThrow`
**Name:** Toss  
**Source:** `guillotina_abilities.gon`  

```
TinaThrow {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        grab_animation grab
        animation throw
        use_placeholder true
    }

    cost {
        mana 0
    }
    
    target {
        max_range 20
        restrictions must_be_empty
    }
    
    damage_instance {
        damage 5+bonus_melee_damage

        custom_additional_ai_weight toss_far
    }
}
```

---

### `G3GrabHead`
**Source:** `guillotina_abilities.gon`  

```
G3GrabHead {
    template targeted_status

    graphics {
        animation grab
        dont_visualize_ai true
    }

    cost {
        mana 0
        must_not_be_consuming true
    }

    target {
        max_range 1
        range_mode cross
    }

    damage_instance {
        type none
        damage 0
        cant_miss true

        effects {
            Conditional_Buddy {
                Consumed {
                    force_contact true
                    instant true
                }
            }
        }

        custom_additional_ai_weight must_target_buddy
    }
}
```

---

### `G3RunToHead`
**Name:** Head Charge  
**Source:** `guillotina_abilities.gon`  

```
G3RunToHead {
    template move
    
    meta {
        name "EABILITY_HEADCHARGE_NAME"
    }

    graphics {
        move_start_animation runStart
        animation run
        speed 2
    }

    target { 
        max_range mov//9999
    }
}
```

---

### `G3TossHead`
**Name:** Toss  
**Source:** `guillotina_abilities.gon`  

```
G3TossHead {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        animation throw
    }

    cost {
        mana 0
    }
    
    target {
        max_range 20
        restrictions none
        damage_collided_only true
        throw_consumed_character true
        always_bounce true
        //always_bounce_randomly true
        reorient_thrown_character true
        //random_bounce true
        //bounce_min_distance 5
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage
        effects {
            Bruise 1
        }

        custom_additional_ai_weight toss_far
    }
}
```

---

### `G3Scream_Debuff`
**Name:** Shriek  
**Source:** `guillotina_abilities.gon`  

```
G3Scream_Debuff {
    template spell

    meta {
        name "EABILITY_SHRIEK_NAME"
    }

    graphics {
        animation scream
        particle none
    }
    
    cost {
        mana 0
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        aoe_excludes_self true
        prioritize_face_camera true

        //aoe_restrictions [enemies_only]
    }

    damage_instance {
        damage 0
        ai_base_score 9999

        effects {
            Conditional_Enemy {
                AllStatsUp -1
            }
            Conditional_Ally {
                AllStatsUp 1
                HealthGain 4
            }
        }
    }
}
```

---

### `G3Scream_Fear`
**Name:** Scream  
**Source:** `guillotina_abilities.gon`  

```
G3Scream_Fear {
    template spell

    meta {
        name "EABILITY_SCREAM_NAME"
    }

    graphics {
        animation scream
        particle none
    }
    
    cost {
        mana 0
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        aoe_excludes_self true
        prioritize_face_camera true

        //aoe_restrictions [enemies_only]
    }

    damage_instance {
        damage 0
        ai_base_score 9999

        effects {
            Conditional_Enemy {
                Fear 1
            }
            Conditional_Ally {
                AllStatsUp 1
                HealthGain 4
            }
        }
    }
}
```

---

### `G3Shake`
**Name:** Shake  
**Source:** `guillotina_abilities.gon`  

```
G3Shake {
    template spawn

    meta {
        name "EABILITY_SHAKE_NAME"
    }

    graphics {
        animation shake
        lob true
    }
    
    cost {
        mana 0
    }

    
    target {
        target_mode none
        max_aoe 2
        aoe_considers_character_size true
        aoe_excludes_self true
        max_targets 1
    }

    self_damage {
        effects {
            Cleanse 0
        }
    }

    spawn {
        object Maggot
        faction self
    }
}
```

---

### `G3CoughFly`
**Name:** Cough  
**Source:** `guillotina_abilities.gon`  

```
G3CoughFly {
    template spawn

    meta {
        name "EABILITY_COUGH_NAME"
    }

    graphics {
        animation shoot
        lob true
    }
    
    cost {
        mana 0
    }

    
    target {
        target_mode direction
        aoe_mode line
        max_aoe 1
        aoe_considers_character_size false
        aoe_excludes_self true

        aoe_mode line //standard, line, cross, custom
        min_aoe 1
        max_aoe 1

        aoe_restrictions none
        redirect_location_if_blocked true
    }

    spawn {
        object Fly
        faction self
    }
}
```

---

### `G3SpawnMama`
**Source:** `guillotina_abilities.gon`  

```
G3SpawnMama {
    template spawn
    chain_ability G3Rage

    graphics {
        dont_orient true
        animation spawnmama
        lob false
    }
    
    cost {
        mana 0
    }

    
    target {
        max_range 5

        aoe_mode custom
        dont_orient_aoe true

        custom_aoe [[0 0] [1 0] [0 1] [1 1]]

        range_excludes_blocking false
        restrictions aoe_must_be_displaceable
        aoe_restrictions none

        range_display_include_aoe true
        mouse_offset [.5 .5]
    }

    self_damage {
        damage 130 //mama maggot health
        non_lethal true
    }

    spawn {
        object MamaMaggotTina
        size 2
        face_camera true
        ai_base_score 999999
    }
}
```

---

### `G3Rage`
**Source:** `guillotina_abilities.gon`  

```
G3Rage {
    template self_buff

    graphics { 
        dont_orient true
        animation enrage
        particle Cleanse
    }

    target {
        X_is current_health
    }

    damage_instance {
        raw_heal "100-X"
        effects {
            FormChange {
                form "Rage"
            }
            Cleanse 0
        }
        ai_base_score 9999
    }
}
```

---

### `G3CallForHelp`
**Source:** `guillotina_abilities.gon`  

```
G3CallForHelp {
    template spell

    graphics { 
        dont_orient true
        animation call
        particle none
    }

    target {
        target_mode none
        aoe_mode all
    }

    damage_instance {
        damage 0
        type status_spell
        cant_miss true

        effects {
            Conditional_Buddy {
                Conditional_InForm {
                    form Normal
                    ForceImmediateMoveAndAttack {
                        ability G3GrabHead
                        even_if_cant_reach true
                    }
                } Else {
                    ForceImmediateMove 1
                }
            }
        }
    }
}
```

---

### `G3PrisonSpit`
**Name:** Prison  
**Source:** `guillotina_abilities.gon`  

```
G3PrisonSpit {
    template lobbed_attack
    
    meta {
        name "EABILITY_PRISON_NAME"
    }
	
    graphics {
        projectile Gutball
    }

    target {
        min_range 1
        max_range 5
        restrictions none
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Imprison Tumor
            Poison 1
        }
    }
}
```

---

### `G3Scream_Hex`
**Name:** Shriek  
**Source:** `guillotina_abilities.gon`  

```
G3Scream_Hex {
    template spell

    meta {
        name "EABILITY_SHRIEK_NAME"
    }

    graphics {
        animation scream
        particle none
    }
    
    cost {
        mana 0
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        aoe_excludes_self true
        prioritize_face_camera true

        //aoe_restrictions [enemies_only]
    }

    damage_instance {
        damage 0
        ai_base_score 9999

        effects {
            Conditional_Enemy {
                Hex 1
                Poison 1
            }
        }
    }
}
```

---

### `G3CoughMaggot`
**Name:** Cough  
**Source:** `guillotina_abilities.gon`  

```
G3CoughMaggot {
    template spawn

    meta {
        name "EABILITY_COUGH_NAME"
    }

    graphics {
        animation shoot
        lob true
    }
    
    cost {
        mana 0
    }

    
    target {
        target_mode direction
        aoe_mode line
        max_aoe 1
        aoe_considers_character_size false
        aoe_excludes_self true

        aoe_mode line //standard, line, cross, custom
        min_aoe 1
        max_aoe 1

        aoe_restrictions none
        redirect_location_if_blocked true
    }

    spawn {
        object [TumorousMaggot, ChargeyMaggot, SwappyMaggot]
        faction self
    }
}
```

---

### `G3RageShake`
**Source:** `guillotina_abilities.gon`  

```
G3RageShake {
    variant_of G3Shake

    spawn {
        object [Maggot, Maggot, Maggot, TumorousMaggot, ChargeyMaggot, SwappyMaggot]
        faction self
    }
}
```

---

## File: `kaiju_abilities.gon`

### `PyrophinaVSSpinThrow`
**Name:** Spin Throw  
**Source:** `kaiju_abilities.gon`  

```
PyrophinaVSSpinThrow {
    template throw_attack
    class KaijuSpinThrowAbility
    
    meta {
        name "EABILITY_SPINTHROW_NAME"
    }

    graphics {
        animation throwboss
        use_placeholder true
        face_toss_target true
        dont_visualize_ai true
        min_throw_height 4
    }

    cost {
        mana 0
    }

    bonus_passives {
        TossTargetIsBuddy 1
    }
    
    target {
        max_range 10
        min_range 3

        max_aoe 2
        aoe_mode circle
        aoe_excludes_self true
        aoe_considers_character_size true
        range_considers_character_size false
        
        restrictions must_fit_2x2
        range_mode cross
        toss_direction_restriction forwards
        spin_steps -16

        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 2
        makes_contact false
        type melee

        custom_additional_ai_weight target_farthest

        effects {
            CollideWithThrowTarget 0
        }
    }

    splash_damage {
        damage 10+bonus_melee_damage
        type knockblock
        makes_contact false
        force_no_knockback true
        knockback 0

        effects {
            CollideWithThrowTarget 0
        }
    }
}
```

---

### `PyrophinaVSWeatherRoar`
**Name:** Firestorm  
**Source:** `kaiju_abilities.gon`  

```
PyrophinaVSWeatherRoar {
    template self_buff

    meta {
        name "EABILITY_FIRESTORM_NAME"
    }

    graphics {
        animation firestorm
        particle none
        dont_visualize_ai true
    }
    
    cost {
        cantrip true
        cantrip_group kaiju_roar
    }

    bonus_passives {
        AbilityEnabledOncePerFightAtHealthThreshold 50%
    }

    target {
        prioritize_face_camera true
    }

    damage_instance {
        ai_base_score 9999
        effects {
            EnableWeather KaijuFirestorm
        }
    }
}
```

---

### `PyrophinaVSRoar`
**Source:** `kaiju_abilities.gon`  

```
PyrophinaVSRoar {
    template spell

    graphics {
        animation roar
        particle none
        dont_visualize_ai true
    }
    
    cost {
        cantrip true
        cantrip_group kaiju_roar
    }

    target {
        prioritize_face_camera true
        target_mode none
        aoe_mode all
    }

    damage_instance {
        type status_spell
        ai_base_score 9999
        cant_miss true

        effects {
            Conditional_NotBoss {
                Fear [1 .3]
            }
        }
    }
}
```

---

### `PyrophinaVSCatThrow`
**Source:** `kaiju_abilities.gon`  

```
PyrophinaVSCatThrow {
    template throw_attack
    
    graphics {
        grab_animation grab
        animation throw
        use_placeholder true
        dont_visualize_ai true

        min_throw_height 1.75
        max_throw_height 1.75
        throw_speed 3
    }

    cost {
        mana 0
    }
    
    target {
        max_range 20
        restrictions must_have_buddy
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        ai_base_score 9999
        custom_additional_ai_weight target_closest
    }
    splash_damage {
        damage 5+bonus_melee_damage
    }
}
```

---

### `PyrophinaVSFlamethrower`
**Name:** Fire Breath  
**Source:** `kaiju_abilities.gon`  

```
PyrophinaVSFlamethrower {
    template spell

    meta {
        name "EABILITY_FIREBREATH_NAME"
    }

    graphics {
        particle FireBlastMushroom
        delay 5
        palette 6
        animation fire
    }
    
    target {
        target_mode direction

        aoe_mode narrow_cone
        aoe_leading_edge_only true
        min_aoe 1
        max_aoe 10

        aoe_considers_character_size true
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 5

        effects {
            Burn 2

            Conditional_HasTag {
                tag rock

                ChangeTilesUnder LavaTile

                Conditional_NotBoss {
                    VaporizeInanimate 1
                } Else {
                    Conditional_HasStatus {
                        status Petrify

                        RemoveStatus Petrify
                        BonusDamage 10
                        Burn 3
                    }
                }
            }
        }
        
        elements [
            Fire
        ]
    }
}
```

---

### `PyrophinaVSEarthquakeStomp`
**Name:** Volcano Stomp  
**Source:** `kaiju_abilities.gon`  

```
PyrophinaVSEarthquakeStomp {
    template spell

    meta {
        name "EABILITY_VOLCANOSTOMP_NAME"
    }

    graphics {
        particle FireBlastMushroom
        palette 6
        animation stomp
    }
    
    target {
        target_mode none

        aoe_mode map_edges
    }

    self_damage {
        effects {
            Cleanse 0
            Burn 3
            StrengthUp 1
        }
    }
    
    damage_instance {
        damage 5
        ai_base_score 9999

        effects {
            Burn 2
        }
        
        elements [
            Fire
            Napalm
        ]
    }
}
```

---

### `PyrophinaVSRun`
**Source:** `kaiju_abilities.gon`  

```
PyrophinaVSRun {
    template move

    graphics {
        animation run
        speed 4
    }
    
    target {
        max_range 8
    }
}
```

---

### `ZaratanaVSSpinDash`
**Name:** Spin Dash  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaVSSpinDash {
    template dash_attack
    class BounceDashAbility
    
    meta {
        name "EABILITY_SPINDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend

        decelerate 5
        dash_decelerating_animation dashslow

        lock_orientation_during_dash true
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode direction8
        max_range 20
        max_bounces -1
        splash_damage_aoe_begin 999 //ability forces splash damage on bonk
        restrictions diagonal_only
    }
    
    damage_instance { //for trample
        damage 5+bonus_melee_ability_damage

        effects {
            SetDistanceDisplace 5
        }
    }
    splash_damage { //for bonk
        damage 10+bonus_melee_ability_damage
        type melee
        knockback 1
        makes_contact true
    }
}
```

---

### `ZaratanaVSWeatherRoar`
**Name:** Meteornado  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaVSWeatherRoar {
    template self_buff

    meta {
        name "EABILITY_METEORNADO_NAME"
    }

    graphics {
        animation meteorshower
        particle none
        dont_visualize_ai true
    }
    
    cost {
        cantrip true
        cantrip_group kaiju_roar
    }

    bonus_passives {
        AbilityEnabledOncePerFightAtHealthThreshold 50%
    }

    target {
        prioritize_face_camera true
    }

    damage_instance {
        ai_base_score 9999

        effects {
            EnableWeather KaijuMeteornado
        }
    }
}
```

---

### `ZaratanaVSRoar`
**Source:** `kaiju_abilities.gon`  

```
ZaratanaVSRoar {
    template spell

    graphics {
        animation roar
        particle none
        dont_visualize_ai true
    }
    
    cost {
        cantrip true
        cantrip_group kaiju_roar
    }

    target {
        prioritize_face_camera true
        target_mode none
        aoe_mode all
        aoe_excludes_self true
    }

    damage_instance {
        type status_spell
        ai_base_score 9999
        cant_miss true

        effects {
            /*Conditional_NotBoss {
                Fear [1 .3]
            }*/
            Conditional_HasTag {
                tag rock
                FloatingRockTrap 1
            }
        }
    }
}
```

---

### `ZaratanaVSTurtle`
**Name:** Turtle  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaVSTurtle {
    template self_buff

    meta {
        name "EABILITY_TURTLE_NAME"
    }

    graphics {
        animation turtlestart
    }

    cost {
        cantrip true
    }

    bonus_passives {
        AbilityEnabledPercentEachTurn 35%
    }

    damage_instance {
        ai_base_score 9999

        effects {
            Cleanse 0
            FormChange {
                form "Turtled"
            }
        }
    }
}
```

---

### `ZaratanaVSTurtleGuaranteed`
**Name:** Turtle  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaVSTurtleGuaranteed {
    template self_buff

    meta {
        name "EABILITY_TURTLE_NAME"
    }

    graphics {
        animation turtlestart
    }

    damage_instance {
        ai_base_score 9999

        effects {
            Cleanse 0
            FormChange {
                form "Turtled"
            }
        }
    }
}
```

---

### `ZaratanaVSExitTurtle`
**Source:** `kaiju_abilities.gon`  

```
ZaratanaVSExitTurtle {
    template melee_attack

    graphics {
        animation exit
    }

    cost {
        cantrip true
    }
   
    target {
        target_mode none
        aoe_mode cross
        knockback_mode character_to_tile
    }

    self_damage {
        ai_base_score 9999
        effects {
            FormChange {
                form "Default"
            }
        }
    }

    damage_instance {
        ai_base_score 9999
        damage 5+bonus_melee_damage
        knockback 2
    }
}
```

---

### `ZaratanaVSMagnet`
**Name:** Magnet Pull  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaVSMagnet {
    template spell

    meta {
        name "EABILITY_MAGNETPULL_NAME"
    }

    graphics {
        animation magnet
        particle none
    }
   
    target {
        target_mode none
        aoe_mode all
        distance_sort_targets 1
        aoe_excludes_self true
    }

    self_damage {
        effects {
            DoDistortionRing {
                speed -30
                intensity -1
                radius 5
            }
        }
    }

    damage_instance {
        damage 0
        ai_base_score 9999

        effects {
            Conditional_NotBig {
                DisplaceTowardsSource 1
            }
            Conditional_HasTag {
                tag rock
                FloatingRockTrap 1
            }
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `ZaratanaVSBombardment`
**Name:** Meteor Bombardment  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaVSBombardment {
    template lobbed_attack
    
    meta {
        name "EABILITY_METEORBOMBARD_NAME"
    }

    graphics {
        animation bombardment
        lob_height 6
    }

    target {
        min_range 2
        max_range 20
        min_aoe 0
        max_aoe 3
        aoe_mode circle
        aoe_excludes_self true

        max_targets 8
        multihit 8
        stagger_multihit_targets true
        shuffle_tile_order true

        restrictions must_have_buddy
    }

    damage_instance {
        damage 10+bonus_ranged_damage
        
        effects {
            HitExplosion 5
        }
    }
}
```

---

### `ZaratanaVSRevenge`
**Source:** `kaiju_abilities.gon`  

```
ZaratanaVSRevenge {
    template straightshot_attack

    graphics {
        projectile SmallRock
        animation revenge
        lob_height 2
        speed 10
    }

    target {
        aoe_mode custom
        custom_aoe      [[0, 1] [0, 1]   [0, -1] [0, -1]]
        custom_aoe_util [[0, 1] [1, 1]   [0,  0] [1,  0]]
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            BounceObject SmallRock
        }
    }
}
```

---

### `ZaratanaBasic`
**Source:** `kaiju_abilities.gon`  

```
ZaratanaBasic {
    template dash_attack
    class FullyAnimatedDashAttackAbility
    
    graphics {
        animation attack
        sync_frames 26
    }
    
    cost {
        mana 0
    }
    
    target {
        max_range 2
        consider_trample true
    }
    
    damage_instance {
        damage 10+bonus_melee_damage
        knockback 2
    }
}
```

---

### `PyrophinaSoloCatThrow`
**Source:** `kaiju_abilities.gon`  

```
PyrophinaSoloCatThrow {
    template throw_attack
    
    graphics {
        grab_animation grab
        animation throw
        use_placeholder true
        dont_visualize_ai true

        min_throw_height 1.75
        max_throw_height 1.75
        throw_speed 3
    }

    cost {
        mana 0
    }
    
    target {
        max_range 10
        restrictions must_be_empty
    }
    
    damage_instance {
        damage 2
        custom_additional_ai_weight pyrophina_throw_to_lava
    }
}
```

---

### `PyrophinaSoloFlamethrower`
**Name:** Fire Breath  
**Source:** `kaiju_abilities.gon`  

```
PyrophinaSoloFlamethrower {
    template spell

    meta {
        name "EABILITY_FIREBREATH_NAME"
    }

    graphics {
        particle FireBlastMushroom
        delay 5
        palette 6
        animation fire
    }
    
    target {
        target_mode direction

        aoe_mode narrow_cone
        aoe_leading_edge_only true
        min_aoe 1
        max_aoe 2

        aoe_considers_character_size true
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 1
        ai_base_score 9999
        custom_additional_ai_weight tile_close_to_enemy_soft

        effects {
            Burn 2

            Conditional_HasTag {
                tag rock

                ChangeTilesUnder LavaTile

                Conditional_NotBoss {
                    VaporizeInanimate 1
                } Else {
                    Conditional_HasStatus {
                        status Petrify

                        RemoveStatus Petrify
                        BonusDamage 10
                        Burn 3
                    }
                }
            }

            ChangeTile {
                tile LavaTile
                chance .25
            }
        }
        
        elements [
            Fire
        ]
    }
}
```

---

### `PyrophinaSoloAttack`
**Source:** `kaiju_abilities.gon`  

```
PyrophinaSoloAttack {
    template melee_attack

    damage_instance {
        knockback 3
    }
}
```

---

### `PyrophinaSoloEarthquakeStomp`
**Name:** Volcano Stomp  
**Source:** `kaiju_abilities.gon`  

```
PyrophinaSoloEarthquakeStomp {
    template spell

    meta {
        name "EABILITY_VOLCANOSTOMP_NAME"
    }

    cost {
        cantrip true
    }

    graphics {
        particle FireBlastMushroom
        palette 6
        animation stomp
    }
    
    target {
        target_mode none

        aoe_mode map_edges
    }

    self_damage {
        effects {
            Cleanse 0
            Burn 3
        }
    }
    
    damage_instance {
        damage 1
        ai_base_score 9999

        effects {
            Burn 2
        }
        
        elements [
            Fire
            Napalm
        ]
    }
}
```

---

### `PyrophinaSoloRoar`
**Source:** `kaiju_abilities.gon`  

```
PyrophinaSoloRoar {
    template spell

    graphics {
        animation roar
        particle none
        dont_visualize_ai true
    }
    
    cost {
        cantrip true
        cantrip_group kaiju_roar
    }

    target {
        prioritize_face_camera true
        target_mode none
        aoe_mode all
    }

    damage_instance {
        type status_spell
        ai_base_score 9999
        cant_miss true

        knockback 10

        effects {
            
        }
    }
}
```

---

### `ZaratanaSoloRoar`
**Source:** `kaiju_abilities.gon`  

```
ZaratanaSoloRoar {
    template spell

    graphics {
        animation roar
        particle none
        dont_visualize_ai true
    }
    
    cost {
        cantrip true
        cantrip_group kaiju_roar
    }

    target {
        prioritize_face_camera true
        target_mode none
        aoe_mode all
        aoe_excludes_self true
    }

    damage_instance {
        type status_spell
        ai_base_score 9999
        cant_miss true

        effects {
            Conditional_HasTag {
                tag rock
                FloatingRockTrap 1
            }
        }
    }
}
```

---

### `ZaratanaSoloMagnet`
**Name:** Magnet Pull  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaSoloMagnet {
    template spell

    meta {
        name "EABILITY_MAGNETPULL_NAME"
    }

    graphics {
        animation magnet
        particle none
    }
   
    target {
        target_mode none
        aoe_mode all
        distance_sort_targets 1
        X_is custom
        prioritize_face_camera true
        aoe_excludes_self true
    }

    cost {
        cant_cast 2-X //if there ARENT ANY ROCKS this is 1, = cant cast (adjusted +1 cause zarartana herself is now a rock)
    }

    bonus_passives {
        XIsLivingCharactersWithTag rock
    }

    self_damage {
        effects {
            DoDistortionRing {
                speed -30
                intensity -1
                radius 5
            }
        }
    }

    damage_instance {
        damage 0
        ai_base_score 9999

        effects {
            Conditional_HasTag {
                tag rock
                DisplaceTowardsSource 1
                FloatingRockTrap 1
            }
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `ZaratanaSoloBombardment`
**Name:** Meteor Bombardment  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaSoloBombardment {
    template lobbed_attack
    
    meta {
        name "EABILITY_METEORBOMBARD_NAME"
    }

    graphics {
        projectile Meteorball
        animation bombardment
        lob_height 6
    }

    target {
        min_range 2
        max_range 20
        min_aoe 0
        max_aoe 3
        aoe_mode circle
        aoe_excludes_self true

        max_targets 5
        multihit 5
        stagger_multihit_targets true
        shuffle_tile_order true
        knockback_mode 0
    }

    damage_instance {
        damage 3+bonus_ranged_damage
        custom_additional_ai_weight tile_exists
        
        effects {
            Displace 1
            BounceRock SmallRock
        }
    }
}
```

---

### `ZaratanaSoloBasic`
**Source:** `kaiju_abilities.gon`  

```
ZaratanaSoloBasic {
    template dash_attack
    class FullyAnimatedDashAttackAbility
    
    graphics {
        animation attack
        sync_frames 26
    }
    
    cost {
        mana 0
    }
    
    target {
        max_range 2
        consider_trample true
    }
    
    damage_instance {
        damage 4+bonus_melee_damage
        knockback 2
        effects {
            Bruise 1
        }
    }
}
```

---

### `ZaratanaSoloSpinDash`
**Name:** Spin Dash  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaSoloSpinDash {
    template dash_attack
    class BounceDashAbility
    
    meta {
        name "EABILITY_SPINDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend

        decelerate 5
        dash_decelerating_animation dashslow

        lock_orientation_during_dash true
    }
    
    cost {
        mana 0
        prime 1
    }
    
    target {
        target_mode direction8
        max_range 20
        max_bounces -1
        splash_damage_aoe_begin 999 //ability forces splash damage on bonk
        restrictions diagonal_only
    }

    self_damage {
        effects {
            RemoveActPoints 1
            RemoveMovePoints 1

            FormChange {
                form "Default"
            }
        }
    }
    
    damage_instance {
        damage 3+bonus_melee_ability_damage
        ai_base_score 9999

        effects {
            SetDistanceDisplace 5
            Bruise 1
        }
    }
}
```

---

### `ZaratanaSoloTurtle`
**Name:** Turtle  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaSoloTurtle {
    template self_buff

    meta {
        name "EABILITY_TURTLE_NAME"
    }

    graphics {
        animation turtlestart
    }

    cost {
        cantrip true
    }

    damage_instance {
        ai_base_score 9999

        effects {
            Cleanse 0
            FormChange {
                form "Turtled"
            }
        }
    }
}
```

---

### `ZaratanaSoloWeatherRoar`
**Name:** Meteornado  
**Source:** `kaiju_abilities.gon`  

```
ZaratanaSoloWeatherRoar {
    template self_buff

    meta {
        name "EABILITY_METEORNADO_NAME"
    }

    graphics {
        animation meteorshower
        particle none
        dont_visualize_ai true
    }
    
    cost {
        cantrip true
        cantrip_group kaiju_roar
    }

    bonus_passives {
        AbilityEnabledOncePerFightAtHealthThreshold 50%
    }

    target {
        prioritize_face_camera true
    }

    damage_instance {
        ai_base_score 9999

        effects {
            EnableWeather KaijuMeteornadoSolo
        }
    }
}
```

---

## File: `rifthead_abilities.gon`

### `ZodiacShootX`
**Source:** `rifthead_abilities.gon`  

```
ZodiacShootX {
    template straightshot_attack

    graphics {
        projectile Bullet
        animation shoot
        empty_animation empty
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

        max_targets -X //-1 means no target limit, if no ammo then X is 0
        X_is enable_if_has_ammo
    }

    empty_self_damage {
        effects {
            FormChange passive
        }
    }

    self_damage {
        effects {
            Ammo -1
        }
    }

    damage_instance {
        damage 7+bonus_ranged_damage
        knockback 1//10
        effects {
            //TempTrampleUntilSettled 3
        }
    }
}
```

---

### `ChaosSwitchSides`
**Source:** `rifthead_abilities.gon`  

```
ChaosSwitchSides {
    template teleport

    graphics {
        animation_out portout
        animation_in portin
        self_damage_mid_port true
        dont_visualize_ai true
    }

    cost {
        cantrip true
    }

    self_damage {
        effects {
            ChaosBossFlipMidTeleport 1
        }
    }

    target {
        target_mode tile
        range_mode special_tagged_tiles
        special_tile_tag ChaosValidPosition
        restrictions [must_move]
    }
}
```

---

### `DbgChaosSwitchFormsA`
**Name:** Dbg Switch Forms (Random Active)  
**Source:** `rifthead_abilities.gon`  

```
DbgChaosSwitchFormsA {
    template self_buff
    
    meta {
        name "Dbg Switch Forms (Random Active)"
        animate_name false
    }

    graphics {
        animation change
    }

    cost {
        infcantrip true
    }

    damage_instance {
        effects {
            RandomStatusFromPool {
                FormChange {
                    form "Johnny"
                }
                FormChange {
                    form "Throb"
                }
                FormChange {
                    form "Flush"
                }
            }
        }
        ai_base_score 9999
    }
}
```

---

### `DbgChaosSwitchFormsP`
**Name:** Dbg Switch Forms (Random Active+Passive)  
**Source:** `rifthead_abilities.gon`  

```
DbgChaosSwitchFormsP {
    template self_buff
    
    meta {
        name "Dbg Switch Forms (Random Active+Passive)"
        animate_name false
    }

    graphics {
        animation change
    }

    cost {
        infcantrip true
    }

    damage_instance {
        effects {
            RandomStatusFromPool {
                FormChange {
                    form "JohnnyHost"
                }
                FormChange {
                    form "JohnnyNettle"
                }
                FormChange {
                    form "JohnnyBubs"
                }
                FormChange {
                    form "ThrobHost"
                }
                FormChange {
                    form "ThrobNettle"
                }
                FormChange {
                    form "ThrobBubs"
                }
                FormChange {
                    form "FlushHost"
                }
                FormChange {
                    form "FlushNettle"
                }
                FormChange {
                    form "FlushBubs"
                }
            }
        }
        ai_base_score 9999
    }
}
```

---

### `FlushX`
**Name:** Hsulf  
**Source:** `rifthead_abilities.gon`  

```
FlushX {
    variant_of Flush

    meta {
        name "EABILITY_HSULF_NAME"
    }

    graphics {
        animation flush
        delay_from_map_edge false
        delay_from_reverse_map_edge true
    }

    damage_instance {
        effects {
            OverrideKnockbackDamage 3
        }
        ai_base_score 999999
    }
}
```

---

### `MegablastX`
**Name:** Tsalb Dnim Agem  
**Source:** `rifthead_abilities.gon`  

```
MegablastX {

    template spell
    
    meta {
        name "EABILITY_TSALBDNIMAGEM_NAME"
    }

    graphics {
        animation megablast
        particle none
    }

    target {
        target_mode none
        aoe_mode circle
        min_aoe 0
        max_aoe 20
        aoe_excludes_self true
        aoe_considers_character_size true
        distance_sort_targets true
        knockback_mode tile_to_character
    }
    
    damage_instance {
        damage 0
        layer characters
        knockback 10

        effects {
           // OverrideKnockbackDamage 3+bonus_basic_spell_damage
           // Stun [1 .1]
            /*Conditional_NotBig {
                KnockUpTowardsAndCollide {
                    stacks 1
                    height 1
                }
            }*/
        }

        ai_base_score 999999
    }

    self_damage {
        effects {
            DoDistortionRing {
                speed -30
                intensity -2
                radius 5
            }
        }
    }
}
```

---

### `SpreadX`
**Name:** Tuo Daerps.  
**Source:** `rifthead_abilities.gon`  

```
SpreadX {
    template spell

    meta {
        name "EABILITY_TUODAERPS_NAME"
    }

    graphics {
        animation order
        dont_visualize_ai true

        affected_particle fx_tentaclestrangle
        miss_particle fx_tentaclestrangleMiss
        fx_is_placeholder_animation true
        fx_random_flip true
        miss_random_delay [0, 60]
        random_delay [70 100]
    }
    
    cost {
        prime 1
        cantrip true
    }

    target {
        target_mode none
        aoe_mode area_around_all_player_cats
        aoe_considers_character_size false
        aoe_excludes_self true
        min_aoe 1
        max_aoe 2
        knockback_mode none
        prioritize_face_camera true
    }

    damage_instance {
        damage 8
        ai_base_score 9999
    }
}
```

---

### `ThornUpX`
**Source:** `rifthead_abilities.gon`  

```
ThornUpX {
    template self_buff

    graphics {
        animation spikes
    }
    
    damage_instance {
        effects {
            Thorns 1
            RandomMagicMissile 1
        }
    }
}
```

---

### `CerberubsShotgunReactionX`
**Source:** `rifthead_abilities.gon`  

```
CerberubsShotgunReactionX {
    template straightshot_attack

    target {
        max_aoe 3+bonus_range
        shotgun_mode true

        aoe_mode custom
        custom_aoe      [[4, 3], [4, 2], [4, 1], [4, 0], [4, -1], [4, -2]]

        custom_aoe_util [[1, 1], [1, 1], [1, 1], [1, 0], [1,  0], [1,  0]]
    }

    graphics {
        animation lava
        projectile Projectile
    }
    
    damage_instance {
        damage 3+bonus_ranged_damage

        effects {
            Burn 2
            ChangeTile LavaTile
        }
        elements [
            Fire
        ]
    }
}
```

---

### `ChaosSwitchForms`
**Source:** `rifthead_abilities.gon`  

```
ChaosSwitchForms {
    template self_buff

    graphics {
        animation change
        dont_visualize_ai true
        bypass_combatspeed true
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            PurgeAll 1
            ChaosBossFormChange 1
        }
        ai_base_score 9999
    }
}
```

---

### `ChaosSpawnIn`
**Source:** `rifthead_abilities.gon`  

```
ChaosSpawnIn {
    template return

    graphics {
        animation intro
    }

    target {
        max_range 20
        aoe_excludes_self true
        restrictions none
    }

    self_damage {
        effects {
            FormChange Default
        }
    }
}
```

---

## File: `special_enemy_abilities.gon`

### `SpawnGas`
**Source:** `special_enemy_abilities.gon`  

```
SpawnGas {
    template spawn

    cost {
        mana 5
    }

    graphics {
        lob true
        lob_height 0
        lob_yoff -.5
        animation spawn
    }

    spawn {
        object GasCloud
        faction default
        first_turn initiative
        layer gas
    }
}
```

---

### `BombExplode`
**Source:** `special_enemy_abilities.gon`  

```
BombExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation explode
        delay 1
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode pierce_cross
        knockback_mode character_to_tile
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 10
    }
    
    damage_instance {
        damage 10
        elements [
            Fire
            Explosion
        ]
        ai_base_score 9999
    }
}
```

---

### `GasCanExplode`
**Source:** `special_enemy_abilities.gon`  

```
GasCanExplode {
    template spell

    graphics { 
        dont_orient true
        particle Explosion
        animation explode
        delay 1
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode cross
        knockback_mode character_to_tile
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 1
    }
    
    damage_instance {
        damage 10
        elements [
            Fire
            Napalm
            Explosion
        ]
        ai_base_score 9999
    }
    splash_damage {
        damage 10
        elements [
            Fire
            Explosion
        ]
        ai_base_score 9999
    }
}
```

---

### `SpawnBomb_AI`
**Source:** `special_enemy_abilities.gon`  

```
SpawnBomb_AI {
    variant_of BombExplode

    target {
        target_mode tile
        max_range 5

        range_excludes_blocking true
    }
}
```

---

### `SpawnBomb`
**Name:** Spawn Bomb  
**Source:** `special_enemy_abilities.gon`  

```
SpawnBomb {
    template spawn
    ai_ability SpawnBomb_AI //steal AOE info from BombExplode for targeting

    meta {
        name "EABILITY_SPAWNBOMB_NAME"
    }
    
    graphics {
        lob true
        animation attack
    }
    
    cost {
        mana 5
    }
    
    target {
        max_range 5
    }

    spawn {
        object Bomb
        first_turn end_of_round
    }
}
```

---

### `SpawnRat`
**Name:** Spawn Rat  
**Source:** `special_enemy_abilities.gon`  

```
SpawnRat {
    template spawn

    meta {
        name "EABILITY_SPAWNRAT_NAME"
    }
    
    graphics {
        lob true
        animation attack
    }
    
    cost {
        mana 5
    }
    
    target {
        max_range 1
    }

    spawn {
        object Rat
        ai_base_score 9999
        faction self
        
        auto_cast_on_spawn Dash_Enemy
    }
}
```

---

### `TurtleUp`
**Name:** Turtle  
**Source:** `special_enemy_abilities.gon`  

```
TurtleUp {
    template self_buff
    
    meta {
        name "EABILITY_TURTLE_NAME"
    }
    
    cost {
        mana 5
    }
    
    damage_instance {
        effects {
            Invulnerable 1
        }
    }
}
```

---

### `BombRatTurtle`
**Name:** Turtle  
**Source:** `special_enemy_abilities.gon`  

```
BombRatTurtle {
    template self_buff
    
    meta {
        name "EABILITY_TURTLE_NAME"
    }

    damage_instance {
        effects {
            BombRatTurtle 1
        }
    }
}
```

---

### `CutterCut`
**Name:** Cut  
**Source:** `special_enemy_abilities.gon`  

```
CutterCut {
    template self_buff
    
    meta {
        name "EABILITY_CUT_NAME"
    }
    
    cost {
        mana 0
    }
    
    damage_instance {
        effects {
            Bleed 1
            StrengthUp 2
        }
    }
}
```

---

### `HealSelf`
**Name:** Heal  
**Source:** `special_enemy_abilities.gon`  

```
HealSelf {
    template self_buff
    
    meta {
        name "EABILITY_HEAL_NAME"
    }
    
    cost {
        mana 5
    }
    
    damage_instance {
        heal 5
    }
}
```

---

### `TrampleDash`
**Name:** Trample Dash  
**Source:** `special_enemy_abilities.gon`  

```
TrampleDash {
    template trample_dash
    
    meta {
        name "EABILITY_TRAMPLEDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
    }
    
    cost {
        mana 5
    }
    
    target {

    }
    
    damage_instance {
        damage 8+bonus_melee_damage
    }
}
```

---

### `SmallTrampleDash`
**Name:** Trample Dash  
**Source:** `special_enemy_abilities.gon`  

```
SmallTrampleDash {
    template trample_dash
    
    meta {
        name "EABILITY_TRAMPLEDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
    }
    
    cost {
        mana 5
    }
    
    target {

    }

    temporary_effects {
        Trample 4
    }
    
    damage_instance {
        damage 4+bonus_melee_damage
    }
}
```

---

### `RageUp`
**Name:** Rage Up  
**Source:** `special_enemy_abilities.gon`  

```
RageUp {
    template self_buff
    
    meta {
        name "EABILITY_RAGEUP_NAME"
    }
    
    graphics {
        animation angry
    }
    
    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            StrengthUp 5
        }
    }
}
```

---

### `DustTeleport`
**Source:** `special_enemy_abilities.gon`  

```
DustTeleport {
    template teleport

    cost {
        cantrip true
        move_points 0
        mana 5
    }

    target {
        max_range 6
    }
}
```

---

### `DustDash`
**Name:** Dust Dash  
**Source:** `special_enemy_abilities.gon`  

```
DustDash {
    template dash_attack
    
    meta {
        name "EABILITY_DUSTDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
        dash_attack_animation spin
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode cross
        knockback_mode character_to_tile

        //target_mode tile
        //range_mode cross
        //min_range 0
        //max_range 10

        restrictions dash_must_move
    }

    temporary_effects {
        LeaveBehind {
            object Twister
        }
    }
    
    damage_instance {
        damage 3+bonus_melee_damage
        custom_additional_ai_weight favor_tile_far_away

        effects {
            TwisterDisplaceWithDamage {
                min_dist 2
                max_dist 3

                damage inherit
                exclude_prefix Twister
            }
        }
    }
}
```

---

### `DustMove`
**Source:** `special_enemy_abilities.gon`  

```
DustMove {
    variant_of DefaultMove

    target {
        restrictions [must_be_moveable must_move must_be_empty]
    }
}
```

---

### `DustMelee`
**Source:** `special_enemy_abilities.gon`  

```
DustMelee {
    template melee_attack

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Bruise 1
        }
    }
}
```

---

### `WizSpellShield`
**Name:** Spell Shield  
**Source:** `special_enemy_abilities.gon`  

```
WizSpellShield {
    template self_buff
    
    meta {
        name "EABILITY_SPELLSHIELD_NAME"
    }
    
    cost {
        mana 5
    }
    
    damage_instance {
        effects {
            SpellShield 1
        }
    }
}
```

---

### `WizFlamethrower`
**Name:** Flamethrower  
**Source:** `special_enemy_abilities.gon`  

```
WizFlamethrower {
    template spell

    meta {
        name "EABILITY_FLAMETHROWER_NAME"
    }
    
    cost {
        mana 5
        prime 1
        cantrip true
    }

    graphics {
        particle Explosion
        delay 10
    }
    
    target {
        target_mode direction

        aoe_mode custom
        custom_aoe [       
                                      [3, 2]
                               [2, 1] [3, 1]
                        [1, 0] [2, 0] [3, 0]
                               [2,-1] [3,-1]
                                      [3,-2]
                   ]
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

### `WizBlizzard`
**Name:** Wiz Blizz  
**Source:** `special_enemy_abilities.gon`  

```
WizBlizzard {
    template spell

    meta {
        name "EABILITY_WIZBLIZZ_NAME"
    }
    
    cost {
        mana 5
        prime 1
        cantrip true
    }

    graphics {
        particle IcePoof
    }
    
    target {
        target_mode direction

        aoe_mode square
        min_aoe 1
        max_aoe 1
    }
    
    damage_instance {
        damage 3
        knockback 1

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

### `WizStorm`
**Name:** xXx_Thunder_xXx  
**Source:** `special_enemy_abilities.gon`  

```
WizStorm {
    template spell

    meta {
        name "EABILITY_WIZSTORM_NAME"
    }
    
    cost {
        mana 5
        prime 1
        cantrip true
    }

    graphics {
        particle Bolt
        delay 5
    }
    
    target {
        max_range 5

        aoe_mode custom
        aoe_symmetry four_way
        custom_aoe [[0, 0] [1, 1] [2, 2]]
    }
    
    damage_instance {
        damage 3

        effects {
            Stun [1, .25]
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `GeminiSwipe`
**Name:** Swipe  
**Source:** `special_enemy_abilities.gon`  

```
GeminiSwipe {
    template melee_attack

    meta {
        name "EABILITY_SWIPE_NAME"
    }
    
    cost {
        mana 5
    }

    graphics {
        animation attack
    }
    
    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }
    
    damage_instance {
        damage 1+bonus_melee_damage
        type melee

        effects {
            Bruise 1
        }
    }
}
```

---

### `GeminiBite`
**Name:** Bite  
**Source:** `special_enemy_abilities.gon`  

```
GeminiBite {
    template melee_attack

    meta {
        name "EABILITY_BITE_NAME"
    }
    
    cost {
        mana 5
    }

    graphics {
        animation bite
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        type melee
    }
}
```

---

### `GeminiSpecial`
**Name:** Geminado  
**Source:** `special_enemy_abilities.gon`  

```
GeminiSpecial {
    template spell

    meta {
        name "EABILITY_GEMINADO_NAME"
    }
    
    cost {
        mana 5
    }

    graphics {
        particle none
        animation special
        delay 1
        delay_from_map_center true
    }
    
    target {
        target_mode direction

        aoe_mode square
        min_aoe 0
        max_aoe 10

        aoe_excludes_self true
        knockback_mode to_map_center
    }
    
    damage_instance {
        damage 0
        knockback 3
       
    }
}
```

---

### `SuicideMelee`
**Name:** Melee Attack  
**Description:** A melee attack that also damages yourself.  
**Source:** `special_enemy_abilities.gon`  

```
SuicideMelee {
    template melee_attack
    
    meta {
        name "EABILITY_SUICIDEMELEE_NAME"
        desc "EABILITY_SUICIDEMELEE_DESC"
        animate_name false
    }

    self_damage {
        damage 5+bonus_melee_damage
        type melee
    }
}
```

---

### `SpiderSuicideMelee`
**Source:** `special_enemy_abilities.gon`  

```
SpiderSuicideMelee {
    template melee_attack

    self_damage {
        damage 0
        type melee

        effects {
            DeleteObject 1
        }
    }

    damage_instance {
        effects {
            Infested 1
        }
    }
}
```

---

### `SpawnMaggot`
**Name:** Spawn Maggot  
**Source:** `special_enemy_abilities.gon`  

```
SpawnMaggot {
    template spawn

    meta {
        name "EABILITY_SPAWNMAGGOT_NAME"
    }
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        mana 0
        charge 0
    }
    
    target {
        max_range 2
        range_mode square
    }

    spawn {
        object Maggot
        ai_base_score 9999
        faction self
    }
}
```

---

### `SpawnFlea`
**Name:** Spawn Flea  
**Source:** `special_enemy_abilities.gon`  

```
SpawnFlea {
    template spawn

    meta {
        name "EABILITY_SPAWNFLEA_NAME"
    }
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        mana 0
        charge 0
    }
    
    target {
        max_range 2
        range_mode square
    }

    spawn {
        object Flea
        ai_base_score 9999
        faction self
    }
}
```

---

### `PoisonShot`
**Source:** `special_enemy_abilities.gon`  

```
PoisonShot {
    template lobbed_attack
	
	graphics {
        projectile Poisonball
    }

    target {
        min_range 2
        max_range 3
        restrictions none
    }

    damage_instance {
        effects {
            Poison [1, .25]
        }
    }
}
```

---

### `WideSwipe`
**Source:** `special_enemy_abilities.gon`  

```
WideSwipe {
    template melee_attack

    graphics {
        animation quarterswipe
    }
    
    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }
}
```

---

### `CreepMelee`
**Source:** `special_enemy_abilities.gon`  

```
CreepMelee {
    template melee_attack

    damage_instance {
        effects {
            SpawnCreep 1
        }
    }
}
```

---

### `RatLeap`
**Name:** Rat Leap  
**Source:** `special_enemy_abilities.gon`  

```
RatLeap {
    template jump_attack

    meta {
        name "EABILITY_RATLEAP_NAME"
    }

    graphics {
        jump_attack_animation land
    }
    
    target {
        max_range 3
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1
    }
}
```

---

### `CatCall`
**Name:** Cat Call  
**Source:** `special_enemy_abilities.gon`  

```
CatCall {
    template spell

    meta {
        name "EABILITY_CATCALL_NAME"
    }
    graphics {
        animation howl
        particle fx_statdown
        affected_animation statDown
    }
    
    cost {
        mana 5
        cantrip true
    }
    
    target {
        min_range 0
        max_range 6
        max_aoe 0
    }

    damage_instance {
        damage 0
        
        effects {
            Slow 2
        }
    }
}
```

---

### `CreepRanged`
**Source:** `special_enemy_abilities.gon`  

```
CreepRanged {
    template lobbed_attack
	
    graphics {
		projectile Creepball
    }

    target {
        min_range 1
        max_range 3
        restrictions none
    }

    damage_instance {
        effects {
            SpawnCreep 1
        }
    }
}
```

---

### `MutateOne`
**Name:** Mutate  
**Source:** `special_enemy_abilities.gon`  

```
MutateOne {
    template spell

    meta {
        name "EABILITY_MUTATE_NAME"
    }
    
    target {
        min_range 0
        max_range 6
        max_aoe 0
    }

    damage_instance {
        damage 0
        
        elements [
            Mutate
        ]
    }
}
```

---

### `MutateAOE`
**Name:** Mutate  
**Source:** `special_enemy_abilities.gon`  

```
MutateAOE {
    template spell

    meta {
        name "EABILITY_MUTATE_NAME"
    }

    graphics {
        use_projectile true
		particle DustPoofLarge
        animation fart
        reverse_orientation true
    }
    
    target {
        min_range 0
        max_range 6
        max_aoe 1
    }

    damage_instance {
        damage 0
        
        elements [
            Mutate
        ]
    }
}
```

---

### `SpawnMaggots`
**Name:** Spawn Maggots  
**Source:** `special_enemy_abilities.gon`  

```
SpawnMaggots {
    template spawn

    meta {
        name "EABILITY_SPAWNMAGGOTS_NAME"
    }
    
    graphics {
        lob true
        animation spawn
        reverse_orientation true
    }
    
    cost {
        mana 5
    }
    
    target {
        min_range 0
        max_range 2
        max_aoe 1
        max_targets 2
    }

    spawn {
        object Maggot
        faction self
    }
}
```

---

### `PrisonShot`
**Name:** Tumor Prison  
**Source:** `special_enemy_abilities.gon`  

```
PrisonShot {
    template ranged_attack
    
    meta {
        name "EABILITY_TUMORPRISON_NAME"
    }

    target {
        min_range 1
        max_range 2
        restrictions none
    }

    damage_instance {
        damage 2+bonus_ranged_damage

        effects {
            Imprison Tumor
        }
    }
}
```

---

### `RallyMaggots`
**Name:** Rally, Maggots!  
**Source:** `special_enemy_abilities.gon`  

```
RallyMaggots {
    template spell

    meta {
        name "EABILITY_RALLYMAGGOTS_NAME"
    }

    graphics {
		
		particle fx_statup
        animation whistle
    }
    
    target {
        min_range 0
        max_range 4
        max_aoe 2
        aoe_excludes_self true
    }

    damage_instance {
        damage 0
        
        effects {
            AlliesTakeExtraTurn 1
        }
    }
}
```

---

### `HammerSmash`
**Source:** `special_enemy_abilities.gon`  

```
HammerSmash {
    template melee_attack

    cost {
        mana 0
    }

    target {
        max_aoe 2
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 10

        effects {
            OverrideKnockbackDamage 5
        }
    }
}
```

---

### `SpearPoke`
**Source:** `special_enemy_abilities.gon`  

```
SpearPoke {
    template melee_attack

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

### `MinorZap`
**Name:** Zap  
**Source:** `special_enemy_abilities.gon`  

```
MinorZap {
    template spell

    meta {
        name "EABILITY_ZAP_NAME"
    }
    
    cost {
        mana 0
    }

    graphics {
        particle Bolt
    }
    
    target {
        max_aoe 0
        max_range 2
    }
    
    damage_instance {
        damage 3
        
        effects {
            Stun [1, .25]
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `SpawnJunk`
**Name:** Tantrum  
**Source:** `special_enemy_abilities.gon`  

```
SpawnJunk {
    template spawn

    meta {
        name "EABILITY_TANTRUM_NAME"
    }
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        max_targets 15
    }

    spawn {
        object Junk
    }
}
```

---

### `FatLeap`
**Name:** Fat Leap  
**Source:** `special_enemy_abilities.gon`  

```
FatLeap {
    template jump_attack

    meta {
        name "EABILITY_FATLEAP_NAME"
    }

    graphics {
        jump_attack_animation land
    }
    
    target {
        max_range 4
    }

    damage_instance {
        damage 3+bonus_melee_damage
        knockback 1
    }
}
```

---

### `XLightning`
**Name:** X Lightning  
**Source:** `special_enemy_abilities.gon`  

```
XLightning {
    template spell

    meta {
        name "EABILITY_XLIGHTNING_NAME"
    }
    
    cost {
        mana 0
    }

    graphics {
        particle Bolt
        delay 7
    }
    
    target {
        target_mode direction
        aoe_mode cross
        max_aoe 10
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 2
        
        effects {
            Stun [1, .25]
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `DoubleDiagonalCreepshot`
**Source:** `special_enemy_abilities.gon`  

```
DoubleDiagonalCreepshot {
    template straightshot_attack

    graphics {
        projectile LobbedProjectile
    }

    target {
        aoe_mode custom
        custom_aoe [[1, 1] [1,-1]]
    }

    damage_instance {
        damage 5+bonus_ranged_damage
        
        effects {
            SpawnCreep 1
        }
    }
}
```

---

### `ShortCreepshot`
**Source:** `special_enemy_abilities.gon`  

```
ShortCreepshot {
    template lobbed_attack

    target {
        min_range 1
        max_range 1
    }

    damage_instance {
        damage 5+bonus_ranged_damage
        
        effects {
            SpawnCreep 1
        }
    }
}
```

---

### `Swim`
**Source:** `special_enemy_abilities.gon`  

```
Swim {
    template teleport

    graphics {
        animation_out enterWater
        animation_in exitWater
    }

    target {
        max_range 10
        range_mode square
        restrictions [must_be_moveable must_have_liquid]
    }
}
```

---

### `CanCreeperSlide`
**Name:** Slide  
**Source:** `special_enemy_abilities.gon`  

```
CanCreeperSlide {
    template trample_dash
    
    meta {
        name "EABILITY_SLIDE_NAME"
    }

    cost {
        mana 0
    }

    graphics {
        dash_start_animation launchStart
        dash_animation launchMid
        dash_end_animation launchStop
    }

    temporary_effects {
        Trample 3
        LeaveBehind {
            object Fly
        }
    }

    target {
        max_range 6
    }

    damage_instance {
        damage 4+bonus_melee_damage
        ai_base_score 9999
    }
}
```

---

### `LickyLicky`
**Source:** `special_enemy_abilities.gon`  

```
LickyLicky {
    template melee_attack

    graphics {
        animation lickAttack
    }
    
    cost {
        mana 0
    }
    
    damage_instance {
        heal 1

        effects {
            StrengthUp 1
            Cleanse 0
        }
    }
}
```

---

### `MCFlamethrower`
**Name:** MC Flamethrower  
**Source:** `special_enemy_abilities.gon`  

```
MCFlamethrower {
    template spell

    meta {
        name "EABILITY_MCFLAMETHROWER_NAME"
    }
    
    cost {
        mana 5
        prime 1
    }

    graphics {
        particle FireBlastMedium
		animation castspell
        palette 6
        delay 10
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 4
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

### `MCBlizzard`
**Name:** MC Blizz  
**Source:** `special_enemy_abilities.gon`  

```
MCBlizzard {
    template spell

    meta {
        name "EABILITY_MCBLIZZ_NAME"
    }
    
    cost {
        mana 5
        prime 1
    }

    graphics {
        particle IcePoof
		animation flex
    }
    
    target {
        target_mode direction

        aoe_mode circle
        min_aoe 1
        max_aoe 2
    }
    
    damage_instance {
        damage 3
        knockback 1

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

### `MCStorm`
**Name:** MC Thunder  
**Source:** `special_enemy_abilities.gon`  

```
MCStorm {
    template spell

    meta {
        name "EABILITY_MCTHUNDER_NAME"
    }
    
    cost {
        mana 5
        prime 1
    }

    graphics {
        particle Bolt
		animation floatingmagic
        delay 5
    }
    
    target {
        max_range 5
        target_mode direction

        aoe_mode custom
        aoe_symmetry four_way
        custom_aoe [[1, 1] [2, 2] [3, 3] [4, 4] [5, 5] [6, 6] [7, 7] [8, 8] [9, 9]]
    }
    
    damage_instance {
        damage 3

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

### `D6Fizzle`
**Name:** 0 : Fizzle  
**Source:** `special_enemy_abilities.gon`  

```
D6Fizzle {
    template spell

    meta {
        name "EABILITY_D6FIZZLE_NAME"
    }

    graphics {
        animation fizzle
		particle none
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        min_aoe 0
        max_aoe 0
    }

    damage_instance {
        damage 6

        effects {
            Confusion 2
        }
    }
}
```

---

### `D6Confused`
**Name:** 1 : Confusion  
**Source:** `special_enemy_abilities.gon`  

```
D6Confused {
    template self_buff

    meta {
        name "EABILITY_D6CONFUSION_NAME"
    }

    graphics {
        animation fizzle
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        min_aoe 0
        max_aoe 0
    }

    damage_instance {
        effects {
            Confusion 2
        }
    }
}
```

---

### `D6Poop`
**Name:** 2 : Poop  
**Source:** `special_enemy_abilities.gon`  

```
D6Poop {
    template spawn

    meta {
        name "EABILITY_D6POOP_NAME"
    }
    
    graphics {
        lob true
        animation poop
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[-1, 0]]
    }

    spawn {
        object Poop
        ai_base_score 9999
    }
}
```

---

### `D6Leech`
**Name:** 2 : Leech  
**Source:** `special_enemy_abilities.gon`  

```
D6Leech {
    template lobbed_attack
    
    meta {
        name "EABILITY_D6LEECH_NAME"
    }

    cost {
        mana 0
    }

    target {
        min_range 1
        max_range 3
    }

    damage_instance {
        damage 5+bonus_ranged_damage
        effects {
            Leech 1
        }
    }
}
```

---

### `D6Laser`
**Name:** 3 : Laser  
**Source:** `special_enemy_abilities.gon`  

```
D6Laser {
    template laser
    
    meta {
        name "EABILITY_D6LASER_NAME"
    }

    graphics {
        animation beam
		
		beam_clip Gambitmouthbeam
        beam_cap Gambitmouthbeamcap
    }

    cost {
        mana 0
    }

    damage_instance {
        damage 5
    }
}
```

---

### `D6Knives`
**Name:** 4 : Knives  
**Source:** `special_enemy_abilities.gon`  

```
D6Knives {
    template straightshot_attack

    meta {
        name "EABILITY_D6KNIVES_NAME"
    }

    graphics {
        spawn_offset [0, .5, 0]
    }

    target {
        aoe_mode custom
        aoe_symmetry four_way
        custom_aoe [[1, 1] [1, 0]]
    }

    damage_instance {
        damage 5+bonus_ranged_damage
        
        effects {
            Bleed 1
        }
    }
}
```

---

### `D6Quake`
**Name:** 4 : Quake  
**Source:** `special_enemy_abilities.gon`  

```
D6Quake {
    template spell

    meta {
        name "EABILITY_D6QUAKE_NAME"
        animate_name true
    }
    
    cost {
        mana 0
    }

    graphics {
        particle Earthquake
        delay 7
        animation groundpound
    }
    
    target {
        target_mode none
        aoe_mode diagcross
        max_aoe 10
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 5
        
        effects {
            Bruise 1
            KnockUpAndAway {
                distance 2
            }
        }
        
        elements [
            Earth
        ]
    }
}
```

---

### `D6Storm`
**Name:** 5 : Storm  
**Source:** `special_enemy_abilities.gon`  

```
D6Storm {
    template spell

    meta {
        name "EABILITY_D6STORM_NAME"
    }
    
    cost {
        mana 0
    }

    graphics {
        animation power
        particle Bolt
        delay 5
    }
    
    target {
        max_aoe 3
        max_range 8
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 5
        
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

### `D6Wrath`
**Name:** 6 : Wrath  
**Source:** `special_enemy_abilities.gon`  

```
D6Wrath {
    template spell

    meta {
        name "EABILITY_D6WRATH_NAME"
    }
    
    cost {
        mana 0
    }

    graphics {
        animation power
        particle Explosion
        random_delay [0, 120]
    }
    
    target {
        target_mode none
        
        aoe_mode square
        min_aoe 0
        max_aoe 10
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 10

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

### `RollDice`
**Name:** Roll!  
**Source:** `special_enemy_abilities.gon`  

```
RollDice {
    template spawn

    meta {
        name "EABILITY_ROLLDICE_NAME"
    }
    
    graphics {
        lob true
        animation throw
    }
    
    cost {
        mana 0
        charge 0
    }
    
    target {
        max_range 3
    }

    spawn {
        object Dice
        ai_base_score 9999
    }
}
```

---

### `DiceLeap`
**Source:** `special_enemy_abilities.gon`  

```
DiceLeap {
    template jump_attack

    graphics {
        full_jump_animation djump
        full_jump_sync_frames 36
        full_jump_windup_frames 14
    }

    cost {
        mana 0
        cantrip true
    }
    
    target {
        range_mode square
        max_range 10
        aoe_mode standard
        max_aoe 0
        min_aoe 0
        aoe_excludes_self false
        restrictions none
    }

    damage_instance {
        damage 0
        effects {
            VaporizeDice 1
        }
    }
}
```

---

### `Shove`
**Name:** Shove  
**Source:** `special_enemy_abilities.gon`  

```
Shove {
    template melee_attack
    
    meta {
        name "EABILITY_SHOVE_NAME"
    }
    cost {
        mana 0
        cantrip true
    }

    damage_instance {
        damage 0
        knockback 2
    }
}
```

---

### `KnockCoinsMelee`
**Source:** `special_enemy_abilities.gon`  

```
KnockCoinsMelee {
    template melee_attack

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        custom_additional_ai_weight no_coins_on_map

        effects {
            ScatterHeldCoin 1
            ScatterHeldCoin [1 .5]
            ScatterHeldCoin [1 .5]
            ScatterHeldCoin [1 .5]
        }
    }
}
```

---

### `PoisonKnife`
**Name:** Poison Knife  
**Source:** `special_enemy_abilities.gon`  

```
PoisonKnife {
    template straightshot_attack

    meta {
        name "EABILITY_POISONKNIFE_NAME"
    }

    cost {
        mana 0
    }

    target {
        aoe_mode custom
        custom_aoe [[1, 0]]
    }

    damage_instance {
        damage 1+bonus_ranged_damage
        
        
        effects {
            Poison 1
        }
    }
}
```

---

### `HealBomb`
**Name:** Heal Bomb  
**Source:** `special_enemy_abilities.gon`  

```
HealBomb {
    template spell
    
    meta {
        name "EABILITY_HEALBOMB_NAME"
    }
    
    cost {
        mana 0
    }

    target {
        max_aoe 1
        min_range 1
        max_range 4
    }
    
    damage_instance {
        heal 8
        type spell

        custom_additional_ai_weight must_heal_most_missing_health

        elements [
            Holy
        ]
    }

    splash_damage {
        damage int
        knockback 1
        type spell
    }
}
```

---

### `MassHeal`
**Name:** Mass Heal  
**Source:** `special_enemy_abilities.gon`  

```
MassHeal {
    template spell

    meta {
        name "EABILITY_MASSHEAL_NAME"
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        
        aoe_mode square
        min_aoe 0
        max_aoe 10
        aoe_excludes_self true
        aoe_restrictions [allies_only]
    }
    
    damage_instance {
        heal 4

        elements [
            Holy
        ]
    }
}
```

---

### `ChainDash`
**Name:** Chain Dash  
**Source:** `special_enemy_abilities.gon`  

```
ChainDash {
    template dash_attack
    
    meta {
        name "EABILITY_CHAINDASH_NAME"
    }

    sounds { 
        ontrigger SE_ChainDash 
    } 
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }
    
    cost {
        mana 0
    }
    
    target {

    }

    temporary_effects {
        DashFury 4
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1
    }
}
```

---

### `ShadowstepDodge`
**Source:** `special_enemy_abilities.gon`  

```
ShadowstepDodge {
    template teleport
    
    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    target {
        max_range 1
    }
}
```

---

### `ShadowDagger`
**Name:** Shadow Dagger  
**Source:** `special_enemy_abilities.gon`  

```
ShadowDagger {
    template straightshot_attack

    meta {
        name "EABILITY_SHADOWDAGGER_NAME"
    }

    cost {
        mana 0
    }

    target {
        aoe_mode custom
        custom_aoe [[1, 0]]
        max_aoe 3
    }

    damage_instance {
        damage 4+bonus_ranged_damage

        effects {
            ShadowCrit 1
            ChangeTile {
                tile ShadowTile
            }
        }
    }
}
```

---

### `SwapPositions_TankCat`
**Source:** `special_enemy_abilities.gon`  

```
SwapPositions_TankCat {
    template swap

    target {
        max_range 20
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn

        mode yeet //yeet or overlay
    }
}
```

---

### `WallMove`
**Source:** `special_enemy_abilities.gon`  

```
WallMove {
    template teleport
    
    cost {
        mana 0
    }

    target {
        target_mode tile
        range_mode custom
        custom_range [[0 -9][0 -8][0 -7][0 -6][0 -5][0 -4][0 -3][0 -2][0 -1][0 0][0 1][0 2][0 3][0 4][0 5][0 6][0 7][0 8][0 9]]
        restrictions must_be_moveable_ignore_wall
    }
}
```

---

### `WallEyeShot`
**Name:** Glare  
**Source:** `special_enemy_abilities.gon`  

```
WallEyeShot {
    template straightshot_attack

    meta {
        name "EABILITY_GLARE_NAME"
    }

    cost {
        mana 0
    }

    target {
        aoe_mode custom
        custom_aoe [[1, 0]]
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Weakness 1
        }
    }
}
```

---

### `WallBlow`
**Name:** Blow  
**Source:** `special_enemy_abilities.gon`  

```
WallBlow {
    template spell
    
    meta {
        name "EABILITY_BLOW_NAME"
    }

    cost {
        mana 0
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
        damage 2
        knockback 5

        elements [
            Wind
        ]
    }
}
```

---

### `RangedHeal_Enemy`
**Name:** Healing Word  
**Source:** `special_enemy_abilities.gon`  

```
RangedHeal_Enemy {
    template spell
    
    meta {
        name "EABILITY_HEALINGWORD_NAME"
    }

    graphics {
        affected_particle HealMed
    }
    
    cost {
        mana 5
    }

    target {
        max_aoe 0
        min_range 0
        max_range 3
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

### `BearTrap_Enemy`
**Name:** Bear Trap  
**Source:** `special_enemy_abilities.gon`  

```
BearTrap_Enemy {
    template lobbed_attack
    
    meta {
        name "EABILITY_BEARTRAP_NAME"
    }

    graphics {
        animation throwobject
        projectile DamageTrap
        use_rotation false
    }

    cost {
        mana 2
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

### `BearTrap_Enemy_Cantrip`
**Source:** `special_enemy_abilities.gon`  

```
BearTrap_Enemy_Cantrip {
    variant_of BearTrap_Enemy
    cost {
        cantrip true
    }
}
```

---

### `Spin_Enemy`
**Name:** Spin  
**Source:** `special_enemy_abilities.gon`  

```
Spin_Enemy {
    class MultiHitMeleeAttackAbility
    template melee_attack
    
    meta {
        name "EABILITY_SPIN_NAME"
    }

    graphics {
        start spinattackstart
        loop spinattackloop
        end spinattackend
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode cross
        knockback_mode character_to_tile
        multihit 3
    }
    
    damage_instance {
        damage 2+bonus_melee_damage
    }
}
```

---

### `Dash_Enemy`
**Name:** Dash  
**Source:** `special_enemy_abilities.gon`  

```
Dash_Enemy {
    template dash_attack
    
    meta {
        name "EABILITY_DASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }
    
    cost {
        mana 5
    }
    
    target {

    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1
    }
}
```

---

### `Lick`
**Name:** Lick  
**Source:** `special_enemy_abilities.gon`  

```
Lick {
    template melee_attack
    
    meta {
        name "EABILITY_LICK_NAME"
    }

    cost {
        mana 5
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Stun [1, .25]
        }
    }
}
```

---

### `SpitGlass`
**Name:** Spit Glass  
**Source:** `special_enemy_abilities.gon`  

```
SpitGlass {
    template lobbed_attack

    meta {
        name "EABILITY_SPITGLASS_NAME"
    }
    
    graphics {
        projectile GlassBall
    }
    
    cost {
        mana 0
    }
    
    target {
        min_range 1
        max_range 5
        max_aoe 1
        max_targets 2

        //restrictions [must_be_empty]
        //aoe_restrictions [must_be_empty, exclude_redundant_tilechanges]
    }

    damage_instance {
        damage 2+bonus_ranged_damage

        effects {
            ChangeTile {
                tile GlassTile
            }
            Bleed 1
        }

        //custom_additional_ai_weight tile_close_to_enemy
    }
}
```

---

### `SirenCall`
**Name:** Siren Call  
**Source:** `special_enemy_abilities.gon`  

```
SirenCall {
    template spell

    meta {
        name "EABILITY_SIRENCALL_NAME"
    }
    graphics {
        animation howl
		particle none
    }
    
    cost {
        mana 5
        cantrip true
    }

    
    target {
        min_range 0
        max_range 6
        max_aoe 0
    }

    damage_instance {
        damage 0
        
        effects {
            ForceMoveTowards 1
        }
    }
}
```

---

### `PopeyeDash`
**Name:** Dash  
**Source:** `special_enemy_abilities.gon`  

```
PopeyeDash {
    template dash_attack
    
    meta {
        name "EABILITY_DASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }
    
    cost {
        mana 5
    }
    
    target {
        max_range 2
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 5
    }
}
```

---

### `FurySwipes_Enemy`
**Name:** Fury Swipes  
**Source:** `special_enemy_abilities.gon`  

```
FurySwipes_Enemy {
    template melee_attack
    
    meta {
        name "EABILITY_FURYSWIPES_NAME"
    }

    graphics {
    }

    cost {
        mana 6
    }

    temporary_effects {
        Fury 75
    }

    damage_instance {
        damage 2+bonus_melee_damage
        type melee
    }
}
```

---

### `FurySwipes_Hitler`
**Name:** Führer Swipes  
**Source:** `special_enemy_abilities.gon`  

```
FurySwipes_Hitler {
    variant_of FurySwipes_Enemy
    
    meta {
        name "EABILITY_HITLERSWIPES_NAME"
    }
}
```

---

### `StickyShot`
**Source:** `special_enemy_abilities.gon`  

```
StickyShot {
    template lobbed_attack

    target {
        min_range 1
        max_range 4
        restrictions none
    }

    damage_instance {
        damage 5+bonus_ranged_damage
            
        effects {
            Slow 2
            ChangeTile {
                tile OilTile
            }
        }
    }
}
```

---

### `ChumShot_Maggot`
**Name:** Chum Shot  
**Source:** `special_enemy_abilities.gon`  

```
ChumShot_Maggot {
    template spawn

    meta {
        name "EABILITY_CHUMSHOT_NAME"
        animate_name true
    }
    
    graphics {
        lob true
        animation shoot
		projectile MaggotBall
    }
    
    cost {
        mana 0
        charge 0
    }
    
    target {
        min_range 3
        max_range 5+bonus_range
    }

    spawn {
        object Maggot
        ai_base_score 9999
        faction self
    }
}
```

---

### `ChumShot_Damage`
**Name:** Chum Shot  
**Source:** `special_enemy_abilities.gon`  

```
ChumShot_Damage {
    template lobbed_attack
    
    meta {
        name "EABILITY_CHUMSHOT_NAME"
        animate_name true
    }

    graphics {
        projectile MaggotBall
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

### `ChumDash`
**Name:** Chum Dash  
**Source:** `special_enemy_abilities.gon`  

```
ChumDash {
    template dash_attack
    
    meta {
        name "EABILITY_CHUMDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashend
    }
    
    cost {
        mana 5
    }
    
    target {

    }

    temporary_effects {
        /*LeaveBehind {
            object Maggot
        }*/
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1
    }
}
```

---

### `HostShove`
**Source:** `special_enemy_abilities.gon`  

```
HostShove {
    template melee_attack
    
    cost {
        mana 0
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 2
    }
}
```

---

### `HostSpit`
**Name:** Spit  
**Source:** `special_enemy_abilities.gon`  

```
HostSpit {
    template straightshot_attack
    
    meta {
        name "EABILITY_SPIT_NAME"
        animate_name true
    }

    graphics {

    }

    target {
        aoe_mode custom
        custom_aoe [[1, 1] [1, 0] [1,-1]]
    }

    damage_instance {
        damage 4+bonus_ranged_damage
    }
}
```

---

### `SimonSays_Scatter`
**Name:** Scatter.  
**Source:** `special_enemy_abilities.gon`  

```
SimonSays_Scatter {
    template spell

    meta {
        name "EABILITY_SCATTER_NAME"
    }

    graphics {

    }
    
    cost {
        prime 1
    }

    target {
        target_mode none
        aoe_mode all_except_random_empty
        aoe_considers_character_size false
        aoe_excludes_self true
        min_aoe 6
        max_aoe 10
    }

    damage_instance {
        damage 15
        ai_base_score 9999
    }
}
```

---

### `SimonSays_ComeHere`
**Name:** Kneel.  
**Source:** `special_enemy_abilities.gon`  

```
SimonSays_ComeHere {
    template spell

    meta {
        name "EABILITY_KNEEL_NAME"
    }

    graphics {

    }
    
    cost {
        prime 1
    }

    
    target {
        target_mode none
        aoe_mode square
        aoe_considers_character_size true
        aoe_excludes_self true
        min_aoe 1+size
        max_aoe 20
    }

    damage_instance {
        damage 15
        ai_base_score 9999
    }
}
```

---

### `SimonSays_GoAway`
**Name:** Hide.  
**Source:** `special_enemy_abilities.gon`  

```
SimonSays_GoAway {
    template spell

    meta {
        name "EABILITY_HIDE_NAME"
    }

    graphics {

    }
    
    cost {
        prime 1
    }

    
    target {
        target_mode none
        aoe_mode all_except_edges
        aoe_considers_character_size false
        aoe_excludes_self true
    }

    damage_instance {
        damage 15
        ai_base_score 9999
    }
}
```

---

### `Simon_Tentacle`
**Name:** Meat Tentacle  
**Source:** `special_enemy_abilities.gon`  

```
Simon_Tentacle {
    template spell

    meta {
        name "EABILITY_MEATTENTACLE_NAME"
    }

    graphics {

    }
    
    cost {
        mana 5
        cantrip true
    }

    
    target {
        min_range 0
        max_range 8
        max_aoe 0
    }

    damage_instance {
        damage 0
        custom_additional_ai_weight favor_enemy_already_moved
        
        effects {
            Bound 3
        }
    }
}
```

---

### `Simon_Trash`
**Name:** Litter  
**Source:** `special_enemy_abilities.gon`  

```
Simon_Trash {
    template spawn

    meta {
        name "EABILITY_LITTER_NAME"
    }
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        max_targets 10
    }

    spawn {
        object [Junk Junk Junk Junk Poop Poop SmallRock SmallRock Tumor Crate]
    }
}
```

---

### `Simon_Shot`
**Source:** `special_enemy_abilities.gon`  

```
Simon_Shot {
    template lobbed_attack

    graphics {

    }

    target {
        min_range 1
        max_range 5
    }

    damage_instance {
        damage 4+bonus_ranged_damage
    }
}
```

---

### `SimonFlopper_WiggleFake`
**Name:** Wiggle  
**Source:** `special_enemy_abilities.gon`  

```
SimonFlopper_WiggleFake {
    template self_buff
    
    meta {
        name "EABILITY_WIGGLE_NAME"
    }

    graphics { 
        dont_orient true
    }

    damage_instance {
        ai_base_score 9999
    }
}
```

---

### `SimonFlopper_WiggleGuaranteed`
**Name:** Wiggle  
**Source:** `special_enemy_abilities.gon`  

```
SimonFlopper_WiggleGuaranteed {
    template self_buff
    
    meta {
        name "EABILITY_WIGGLE_NAME"
    }

    graphics { 
        dont_orient true
    }

    damage_instance {
        effects {
            FormChange {
                form "Normal"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `SimonFlopper_WiggleChance`
**Name:** Wiggle  
**Source:** `special_enemy_abilities.gon`  

```
SimonFlopper_WiggleChance {
    template self_buff
    
    meta {
        name "EABILITY_WIGGLE_NAME"
    }

    graphics { 
        dont_orient true
    }

    damage_instance {
        effects {
            FormChange {
                chance 30%
                form "Normal"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `SimonFlopper_Tentacle`
**Name:** Meat Tentacle  
**Source:** `special_enemy_abilities.gon`  

```
SimonFlopper_Tentacle {
    template spell

    meta {
        name "EABILITY_MEATTENTACLE_NAME"
    }
    graphics {

    }
    
    cost {
        mana 5
        cantrip true
    }

    
    target {
        min_range 0
        max_range 8
        max_aoe 0
    }

    damage_instance {
        damage 0
        custom_additional_ai_weight avoid_redundant_debuffs
        
        effects {
            Bound 3
        }
    }
}
```

---

### `SimonFlopper_SpawnMinion`
**Name:** Meat Minion  
**Source:** `special_enemy_abilities.gon`  

```
SimonFlopper_SpawnMinion {
    template spawn

    meta {
        name "EABILITY_MEATMINION_NAME"
        animate_name true
    }
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        mana 0
        charge 0
    }
    
    target {
        min_range 1
        max_range 2
    }

    spawn {
        object MeatMinion
        ai_base_score 9999
        faction self
    }
}
```

---

### `MeatMinionMelee`
**Source:** `special_enemy_abilities.gon`  

```
MeatMinionMelee {
    template melee_attack

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        elements [
            dont_break_tentacles
        ]
    }
}
```

---

### `GasBlast`
**Source:** `special_enemy_abilities.gon`  

```
GasBlast {
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
        
        effects {
            Poison 3
            VisualFXTile PoisonPoof
        }

    }
    self_damage {
        damage 0
        type spell
        knockback -3

        effects {
            KnockbackDamageImmuneUntilSettled 1
        }
    }
}
```

---

### `SharkDash`
**Source:** `special_enemy_abilities.gon`  

```
SharkDash {
    template dash_attack
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashbite
    }
    
    cost {
        mana 5
    }
    
    target {
        max_range 2
    }
    
    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            Bleed 1
        }
    }
}
```

---

### `WaterTrailMove`
**Source:** `special_enemy_abilities.gon`  

```
WaterTrailMove {
    template move

    temporary_effects {
        TileTrail WaterTile
    }
}
```

---

### `BloatyExplodey`
**Name:** Explode  
**Description:** he explode  
**Source:** `special_enemy_abilities.gon`  

```
BloatyExplodey {
    template spell

    meta {
        name "EABILITY_BLOATYEXPLODE_NAME"
        desc "EABILITY_BLOATYEXPLODE_DESC"
        animate_name false
    }
    
    graphics { 
        dont_orient true
        particle none
        animation explode
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode cross
        knockback_mode character_to_tile
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 1
        max_aoe 1
    }
    
    damage_instance {
        damage 1
        knockback 1

        effects {
            Poison 1
        }

        elements [
            Explosion
        ]

    }
}
```

---

### `GasserExplode`
**Source:** `special_enemy_abilities.gon`  

```
GasserExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle none
        animation explode
    }
    
    cost {
        mana 5
    }
    
    target {
        knockback_mode character_to_tile
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 1
        max_aoe 2
    }
    
    damage_instance {
        damage 5
        knockback 1

        effects {
            DustOnHit {
                object GasCloud
            }
        }

        elements [
            Explosion
        ]

    }
}
```

---

### `BoomerCatExplode`
**Source:** `special_enemy_abilities.gon`  

```
BoomerCatExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation blowUp
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode square
        knockback_mode character_to_tile
        aoe_excludes_self true
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 1
    }
    
    damage_instance {
        damage 5
        knockback 1

        elements [
            Explosion
        ]
    }
}
```

---

### `SpawnDip`
**Name:** Spawn Dip  
**Source:** `special_enemy_abilities.gon`  

```
SpawnDip {
    template spawn

    meta {
        name "EABILITY_SPAWNDIP_NAME"
        animate_name true
    }
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        mana 0
        charge 0
    }
    
    target {
        min_range 1
        max_range 1
    }

    spawn {
        object Dip
        ai_base_score 9999
    }
}
```

---

### `DipShot`
**Source:** `special_enemy_abilities.gon`  

```
DipShot {
    template lobbed_attack

    graphics {
        projectile Dip
    }

    target {
        min_range 2
        max_range 7+bonus_range
    }

    damage_instance {
        damage 2+bonus_ranged_damage

        effects {
            BounceObject Dip
        }
    }
}
```

---

### `FloaterMelee`
**Source:** `special_enemy_abilities.gon`  

```
FloaterMelee {
    template melee_attack

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            RefreshMovePointsIfHit 1
        }
    }
}
```

---

### `TallSpiderMelee`
**Source:** `special_enemy_abilities.gon`  

```
TallSpiderMelee {
    template melee_attack

    graphics {
        animation dashbite
    }

    self_damage {
        effects {
            RefreshMovePoints 1
        }
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Leech 1
        }
    }
}
```

---

### `SmallSpiderMelee`
**Source:** `special_enemy_abilities.gon`  

```
SmallSpiderMelee {
    template melee_attack

    graphics {
        animation dashbite
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Leech 1
        }

        custom_additional_ai_weight enemy_is_webbed
    }
}
```

---

### `LeechDash`
**Name:** Leech Dash  
**Source:** `special_enemy_abilities.gon`  

```
LeechDash {
    template dash_attack
    class PierceDashAbility
    
    meta {
        name "EABILITY_LEECHDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
    }
    
    cost {
        mana 5
    }
    
    target {

    }
    
    damage_instance {
        damage 4+bonus_melee_damage
        piercing true
        force_no_knockback true

        effects {
            Leech 1
        }
    }
}
```

---

### `BumblefootLeap`
**Name:** Bumble Jump  
**Source:** `special_enemy_abilities.gon`  

```
BumblefootLeap {
    template jump_attack

    meta {
        name "EABILITY_BUMBLEJUMP_NAME"
    }

    graphics {
        jump_start_animation leapattackwindup
        full_jump_animation leapattack
        full_jump_sync_frames 40
    }

    cost {
        act_points 1
    }
    
    target {
        min_range 4
        max_range 6

        min_aoe 0
        max_aoe 1
    }

    temporary_effects {
        DisableTrample 1
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1
        ai_base_score 9999

        effects {
            IgnoreSelf 1
        }
    }

    self_damage {
        effects {
            FormChange {
                form Down
            }
        }
    }
}
```

---

### `BumblefootEatCorpse`
**Name:** Feast  
**Source:** `special_enemy_abilities.gon`  

```
BumblefootEatCorpse {
    template teleport
    class TeleportEatAbility
    
    meta {
        name "EABILITY_FEAST_NAME"
        animate_name true
    }

    graphics {
        animation_out digout
        animation_in digin
        use_super_armor true
        dont_visualize_ai true
    }

    cost {
        act_points 1
    }

    target {
        max_range 20
        aoe_restrictions must_have_destructible_corpse
        restrictions [must_be_moveable aoe_must_exist]
        corpse_priority 10
        knockback_mode zero
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true
        ai_base_score 9999
        makes_contact true

        effects {
            Vaporize 20
            IgnoreSelf 1
        }
    }

    splash_damage { //for trample
        type melee
        damage 5+bonus_melee_damage
        makes_contact true
        override_trample_damage true

        effects {
            SetDistanceDisplace 5
            IgnoreSelf 1
        }
    }

    self_damage {
        effects {
            FormChange {
                form Up
            }
        }
    }
}
```

---

### `BumblefootEatCat`
**Name:** Feast  
**Source:** `special_enemy_abilities.gon`  

```
BumblefootEatCat {
    template teleport
    class TeleportEatAbility
    
    meta {
        name "EABILITY_FEAST_NAME"
        animate_name true
    }

    graphics {
        animation_out digout
        animation_in digin
        use_super_armor true
        dont_visualize_ai true
    }

    cost {
        act_points 1
    }

    target {
        max_range 20
        aoe_restrictions must_have_animate_character
        restrictions [must_be_moveable aoe_must_exist]

        ally_priority 1
        corpse_priority 5
        enemy_priority 10
        knockback_mode zero
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true
        makes_contact true

        effects {
            Vaporize 20
            IgnoreSelf 1
        }
    }

    splash_damage { //for trample
        type melee
        damage 5+bonus_melee_damage
        makes_contact true
        override_trample_damage true

        effects {
            SetDistanceDisplace 5
            IgnoreSelf 1
        }
    }

    self_damage {
        effects {
            FormChange {
                form Up
            }
        }
    }
}
```

---

### `BumblefootAttemptEatCat`
**Name:** Feast  
**Source:** `special_enemy_abilities.gon`  

```
BumblefootAttemptEatCat {
    template teleport
    
    meta {
        name "EABILITY_FEAST_NAME"
        animate_name true
    }

    graphics {
        animation_out digout
        animation_in digin
        use_super_armor true
        dont_visualize_ai true
    }

    cost {
        act_points 1
    }

    target {
        max_range 20
        aoe_restrictions must_have_animate_character
        restrictions [must_be_moveable aoe_must_exist]

        knockback_mode zero
    }


    damage_instance {
        type melee
        damage 5+bonus_melee_damage
        makes_contact true
        override_trample_damage true

        effects {
            SetDistanceDisplace 5
            IgnoreSelf 1
        }
    }

    self_damage {
        effects {
            FormChange {
                form Up
            }
        }
    }
}
```

---

### `BumblefootBoneShot`
**Name:** Bone Spurt  
**Source:** `special_enemy_abilities.gon`  

```
BumblefootBoneShot {
    template lobbed_attack
    
    meta {
        name "EABILITY_BONESPURT_NAME"
    }

    graphics {
        lob_height 3
        projectile BoneProjectile
        use_rotation false
    }

    cost {
        act_points 1
    }

    target {
        target_mode none
        max_aoe 2
        aoe_considers_character_size true
        aoe_excludes_self true
        max_targets 6

        can_multihit true
        aoe_restrictions [must_not_have_corpse]
    }

    damage_instance {
        ai_base_score 9999

        effects {
            Bruise 1
        }
    }

    temporary_effects {
        CastAgain 2
    }
}
```

---

### `RockySlam`
**Source:** `special_enemy_abilities.gon`  

```
RockySlam {
    template jump_attack

    graphics {
        //jump_start_animation leapattackwindup
        full_jump_animation attack1
        full_jump_sync_frames 39
        full_jump_windup_frames 20
    }

    cost {
        act_points 1
    }
    
    target {
        max_range 2
        min_range 2
        range_mode cross
        range_considers_character_size false
        min_aoe 0
        max_aoe 1
        prioritize_dont_change_direction true
    }

    temporary_effects {
        DisableTrample 1
    }

    damage_instance {
        type melee
        damage 5+bonus_melee_damage
        knockback 1
        ai_base_score 9999

        effects {
            IgnoreSelf 1
        }
    }

    self_damage {
        damage 0
        effects {
            SpawnRock 1
        }
    }
}
```

---

### `RockSong`
**Name:** Rock Song  
**Source:** `special_enemy_abilities.gon`  

```
RockSong {
    template spell

    meta {
        name "EABILITY_ROCKSONG_NAME"
    }
    
    graphics {
        particle none
        animation attack2
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        aoe_mode all
        prioritize_dont_change_direction true
        aoe_excludes_self true
    }

    damage_instance {
        type none
        damage 0

        effects {
            //RockSeekEnemies 1
            Conditional_HasTag {
                tag rock
                FloatingRockTrap 1
            }
        }
    }
}
```

---

### `ChubsSpin`
**Name:** Chub Spin  
**Source:** `special_enemy_abilities.gon`  

```
ChubsSpin {
    template melee_attack
    
    meta {
        name "EABILITY_CHUBSPIN_NAME"
    }

    graphics {
        animation attack
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode square
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `ChubsSpinRage`
**Name:** Chub Spin  
**Source:** `special_enemy_abilities.gon`  

```
ChubsSpinRage {
    template melee_attack
    
    meta {
        name "EABILITY_CHUBSPIN_NAME"
    }

    graphics {
        animation attack
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode square
        knockback_mode character_to_tile
        multihit 2
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `ChubsGoop`
**Source:** `special_enemy_abilities.gon`  

```
ChubsGoop {
    template straightshot_attack

    cost {
        mana 0
    }
	
    graphics {
        projectile Poisonball
    }
    target {
        max_aoe 10
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Poison 2
        }
    }
}
```

---

### `ChubsRage`
**Source:** `special_enemy_abilities.gon`  

```
ChubsRage {
    template self_buff

    graphics { 
        dont_orient true
        animation rage
    }

    damage_instance {
        effects {
            FormChange {
                form "Rage"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `NubsGoop`
**Source:** `special_enemy_abilities.gon`  

```
NubsGoop {
    template lobbed_attack

    cost {
        mana 0
    }
	
    graphics {
        projectile Creepball
    }
	
    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[3, 0]]
    }

    damage_instance {
        damage 8+bonus_ranged_damage
        effects {
            SpawnCreep 1
            Poison 2
        }
    }
}
```

---

### `NubsNuke`
**Name:** Nuke  
**Source:** `special_enemy_abilities.gon`  

```
NubsNuke {
    template spell

    meta {
        name "EABILITY_NUKE_NAME"
    }

    graphics {
        animation nuke
        particle Explosion
        delay 5
    }

    cost {
        mana 0
        prime 1
    }

    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_piercing_line_of_sight
    }

    self_damage {
        damage 0
        piercing true
        effects {
            DeferVaporize 1
        }

        elements [
            Explosion
        ]
    }

    damage_instance {
        damage 50

        effects {
            CorpseVaporizer 1 //kills any corpses it hits, characters leave no corpses
        }

        elements [
            Explosion
        ]
    }
}
```

---

### `NubsJump`
**Name:** Nub Flub  
**Source:** `special_enemy_abilities.gon`  

```
NubsJump {
    template jump_attack
    ai_ability NubsJump_AI

    meta {
        name "EABILITY_NUBFLUB_NAME"
    }

    graphics {
        full_jump_animation attack
        full_jump_sync_frames 31
        full_jump_windup_frames 15
    }

    cost {
        act_points 1
    }
    
    target {
        min_range 2
        max_range 2
        aoe_mode square
    }

    damage_instance {
        damage 4+bonus_melee_damage
        knockback 1

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `NubsCatJumpReaction`
**Source:** `special_enemy_abilities.gon`  

```
NubsCatJumpReaction {
    variant_of NubsJump
    target {
        range_mode cross
        min_range 0
        max_range 2
        aoe_mode square
    }
}
```

---

### `NubsJump_AI`
**Source:** `special_enemy_abilities.gon`  

```
NubsJump_AI { //nubs jump pretends its targeting like a spawn ability so he can jump towards things while blind sometimes
    template spawn

    target {
        min_range 2
        max_range 2
    }

    spawn {
        object SmallRock
    }
}
```

---

### `TNTExplodey`
**Source:** `special_enemy_abilities.gon`  

```
TNTExplodey {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation explode
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode cross
        knockback_mode character_to_tile
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 1
        max_aoe 1
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

### `HunterMinibossMove`
**Source:** `special_enemy_abilities.gon`  

```
HunterMinibossMove {
    template move

    target {
        bonus_pathing_leniency 4
    }
}
```

---

### `DaddyHungry`
**Source:** `special_enemy_abilities.gon`  

```
DaddyHungry {
    template melee_attack
    class MeleeEatAbility
    ai_ability BasicBigMelee //needed so daddy shark's simple brain can understand this

    graphics {
        animation attack
    }

    target { 
        max_aoe 1
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true

        effects {
            Vaporize 20
            FlatLeech 10
        }
    }
}
```

---

### `BabySharkMelee`
**Source:** `special_enemy_abilities.gon`  

```
BabySharkMelee {
    template melee_attack
    ai_ability BasicMelee //needed so baby shark's simple brain can understand this

    damage_instance {
        damage 0

        effects {
            Bleed 1
        }
    }
}
```

---

### `HarpoonTrapPull`
**Source:** `special_enemy_abilities.gon`  

```
HarpoonTrapPull {
    template straightshot_attack
    
    cost {
        mana 0
        cantrip true
    }

    target {
        max_range 10

        knockback_mode pull_to_character
    }

    graphics {
        animation shoot

        projectile Harpoon
        chain_movieclip ChainLink
        chain_distance .25
    }
    
    damage_instance {
        damage 5+bonus_ranged_damage
    }
}
```

---

### `Flush`
**Name:** Flush  
**Source:** `special_enemy_abilities.gon`  

```
Flush {
    template spell

    meta {
        name "EABILITY_FLUSH_NAME"
    }

    graphics {
        particle Wave
        animation attack

        visual_delay_but_simultaneous_damage 50
        delay_from_map_edge true
        delay 5
    }
    
    cost {
        mana 0
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        aoe_excludes_self true
        knockback_mode orientation
        prioritize_dont_change_direction true
    }

    damage_instance {
        damage 0
        knockback 10

        effects {
            OverrideKnockbackDamage 3
        }

        elements [
            Water
        ]
        ai_base_score 999999
    }
}
```

---

### `TenTicklesAttack`
**Name:** Ten Tickles  
**Source:** `special_enemy_abilities.gon`  

```
TenTicklesAttack {
    template spell
    
    meta {
        name "EABILITY_TENTICKLES_NAME"
    }

    graphics {
        center_particle TenTicklesAttack
        area_particle none
        animation attack
    }
    
    cost {
        mana 0
    }

    target {
        aoe_mode custom
        custom_aoe [[1, 0]]
        knockback_mode orientation

        range_mode square
        min_range 1
        max_range 10

        restrictions [must_have_liquid must_be_empty]

        allow_any_orientation true
    }
    
    damage_instance {
        damage 4+bonus_melee_damage
        type melee
        contact_requires_adjacency false
    }
}
```

---

### `TenTicklesSwim`
**Source:** `special_enemy_abilities.gon`  

```
TenTicklesSwim {
    template teleport

    graphics {
        animation_out portOut
        animation_in portIn
    }

    target {
        max_range 10
        range_mode square
        restrictions [must_be_moveable must_have_liquid]
    }
}
```

---

### `DrinkUp`
**Name:** Bottoms Up  
**Description:** Gain 5HP. Can only be used when standing in water.  
**Source:** `special_enemy_abilities.gon`  

```
DrinkUp {
    template self_buff
    
    meta {
        name "EABILITY_BOTTOMSUP_NAME"
		desc "EABILITY_BOTTOMSUP_DESC"
    }

    graphics {
        animation heal
    }
    
    cost {
        mana 3
    }

    target {
        restrictions must_have_liquid
    }
    
    damage_instance {
        heal 5
    }
}
```

---

### `FetusGush`
**Source:** `special_enemy_abilities.gon`  

```
FetusGush {
    template melee_attack

    graphics {
        detatched_animation WaterGush
        detatched_animation_reach 20
        detatched_animation_cutoff true
    }

    cost {
        mana 0
    }

    target {
        max_aoe 10
        aoe_restrictions must_have_piercing_line_of_sight
    }

    damage_instance {
        type spell
        damage 1
        knockback 3

        elements [
            Water
        ]
    }
}
```

---

### `BasicShortLobbed_Water`
**Name:** Lobbed Water Shot  
**Description:** Lobbed Water attack.  
**Source:** `special_enemy_abilities.gon`  

```
BasicShortLobbed_Water {
    template lobbed_attack
	
    meta {
        name "EABILITY_LOBBEDWATERSHOT_NAME"
		desc "EABILITY_LOBBEDWATERSHOT_DESC"
    }
	
    graphics {
        projectile spitprojectile
    }

    target {
        min_range 1
        max_range 2+bonus_range
    }

    damage_instance {
        elements [
            Water
        ]
    }
}
```

---

### `AnimatedRockAttack`
**Source:** `special_enemy_abilities.gon`  

```
AnimatedRockAttack {
    template self_buff

    graphics {
        animation none
    }

    sounds {
        ontrigger SE_PetRock_Dash
    }

    cost {
        move_points 0
        act_points 1
    }

    target {
        target_mode direction8
        knockback_mode orientation
        dont_orient_aoe true //TODO: allow for ability to handle diagonal orients and get rid of this
    }

    damage_instance {
        type melee
        damage 0
        knockback 10
    }
}
```

---

### `WebShot`
**Source:** `special_enemy_abilities.gon`  

```
WebShot {
    template lobbed_attack

    target {
        min_range 1
        max_range 3
        restrictions none
        knockback_mode zero
    }
	
    graphics {
        projectile Webball
    }
	
    damage_instance {
        damage 0

        effects {
            Webbed 1
        }

        custom_additional_ai_weight avoid_redundant_debuffs
    }
}
```

---

### `Disguise`
**Name:** Disguise  
**Source:** `special_enemy_abilities.gon`  

```
Disguise {
    template self_buff
    
    meta {
        name "EABILITY_DISGUISE_NAME"
    }
    
	graphics {
    particle DustPoofLarge
    }
    
	cost {
        mana 5
        cantrip true
    }
    
    damage_instance {
        effects {
            Disguised 1
        }
    }
}
```

---

### `MoveTwoCantrip`
**Source:** `special_enemy_abilities.gon`  

```
MoveTwoCantrip {
    template move

    target { 
        max_range 2
    }

    cost {
        mana 5
        cantrip true
    }
}
```

---

### `Counterspell`
**Name:** Counterspell  
**Description:** Counter the next spell an enemy casts.
If counterspell isn't triggered by your next turn, absorb it to gain +2 Damage and +2 All Stats Up.  
**Source:** `special_enemy_abilities.gon`  

```
Counterspell {
    template self_buff
	
    meta {
        name "EABILITY_COUNTERSPELL_NAME"
        desc "EABILITY_COUNTERSPELL_DESC"
        animate_name false
    }

    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        effects {
            Counterspell 1
        }
    }
}
```

---

### `BrainDrainMagicMissile`
**Name:** Brain Missile  
**Description:** Shoot an infinite-range projectile that can't miss.  
**Source:** `special_enemy_abilities.gon`  

```
BrainDrainMagicMissile {
    variant_of BasicMagicMissile
	
    meta {
        name "EABILITY_BRAINMISSLE_NAME"
        desc "EABILITY_BRAINMISSLE_DESC"
        animate_name false
        class Colorless
    }

    graphics {
        animation pulse2
    }

    damage_instance {
        damage 3
    }
}
```

---

### `AcidShot`
**Name:** Acid Shot  
**Source:** `special_enemy_abilities.gon`  

```
AcidShot {
    template ranged_attack
    
    meta {
        name "EABILITY_ACIDSHOT_NAME"
    }
	
    graphics {
        projectile AcidshotProjectile
    }
	
    target {
        min_range 1
        max_range 2
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Burn 2
            DissolveRandomArmorPiece 1
        }
    }
}
```

---

### `KirbySuck`
**Name:** Suck  
**Description:** Inhale a unit, then spit it out.  
**Source:** `special_enemy_abilities.gon`  

```
KirbySuck {
    template straightshot_attack

    meta {
        name "EABILITY_SUCK_NAME" //TODO: this one does need to be localized
        desc "EABILITY_SUCK_DESC"
        animate_name false
    }

    graphics {
        animation inhale
        projectile None
    }

    cost {
        mana 0
        must_not_be_consuming true
    }

    target {
        max_aoe 10
        knockback_mode none
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                wet true
                struggle_ability Thrash
            }
        }

        elements [
            Wind
        ]
    }
}
```

---

### `KirbySpitAI`
**Source:** `special_enemy_abilities.gon`  

```
KirbySpitAI {
    template straightshot_attack

    target {
        max_aoe 10
        prioritize_change_direction true
        restrictions require_empty_tile_in_front
    }

    damage_instance {
        type ranged
        damage 20
        ai_base_score 9999
        custom_additional_ai_weight favor_tile_far_away
    }
}
```

---

### `KirbySpit`
**Name:** Suck  
**Description:** Inhale a unit, then spit it out.  
**Source:** `special_enemy_abilities.gon`  

```
KirbySpit {
    template melee_attack
    ai_ability KirbySpitAI

    meta {
        name "EABILITY_SUCK_NAME"
        desc "EABILITY_SUCK_DESC"
        animate_name false
    }

    graphics {
        animation exhale
        dont_visualize_ai true
    }

    target {
        prioritize_change_direction true
        restrictions require_empty_tile_in_front
        uncounterable true //not hit by confusion or deja vu or counterspell
    }

    cost {
        mana 0
        cantrip true
        must_be_consuming true
    }

    damage_instance {
        type none
        damage 0
        knockback 10
        cant_miss true

        effects {
            SpitConsumed 1
            OverrideKnockbackDamage 4
        }

        ai_base_score 9999
    }
}
```

---

### `BatFlurry`
**Source:** `special_enemy_abilities.gon`  

```
BatFlurry {
    template melee_attack

    target {
        multihit 4
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Confusion [1 .5]
        }
    }
}
```

---

### `MegafetusMelee_ai`
**Source:** `special_enemy_abilities.gon`  

```
MegafetusMelee_ai {
    template melee_attack

    target { 
        aoe_considers_character_size true
        aoe_mode cone
        max_aoe 20
        min_aoe 2
        aoe_leading_edge_only true

        //custom_aoe [[2, 1] [3, 1] [2, 0] [3, 0]] //thinks he can hit the full 2x2
    }

    damage_instance {
        contact_requires_adjacency false
    }
}
```

---

### `MegafetusMelee`
**Source:** `special_enemy_abilities.gon`  

```
MegafetusMelee {
    template melee_attack
    ai_ability MegafetusMelee_ai

    target { 
        aoe_considers_character_size false
        aoe_rotate_around_character_center true
        aoe_mode custom

        custom_aoe [[2, 1] [3, 1]]
    }

    damage_instance {
        damage 8+bonus_melee_damage
        contact_requires_adjacency false

        effects {
            DoScreenShake {
                time .5
                intensity 3
            }

            QuakeAreaChance {
                radius 1
                chance 50%
            }
        }

        elements [
            Quake
        ]
    }
}
```

---

### `MegafetusSpin`
**Name:** Spin  
**Source:** `special_enemy_abilities.gon`  

```
MegafetusSpin {
    template melee_attack
    
    meta {
        name "EABILITY_SPIN_NAME"
    }

    graphics {
        animation spin
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode square
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1
    }
}
```

---

### `BadBone`
**Source:** `special_enemy_abilities.gon`  

```
BadBone {
    template straightshot_attack

    graphics {
        animation throwobject
        projectile BoneProjectile
        use_rotation false
    }

    cost {
        mana 0
        charge 1
    }

    target {
        max_aoe 10
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Stun [1 .15]
        }
    }
}
```

---

### `BadBone_copy`
**Source:** `special_enemy_abilities.gon`  

```
BadBone_copy {
    variant_of BadBone
}
```

---

### `GoodBone`
**Source:** `special_enemy_abilities.gon`  

```
GoodBone {
    template straightshot_attack

    graphics {
        animation throwobject
        projectile BoneProjectile
        use_rotation false
    }

    cost {
        mana 0
        charge 1
    }

    target {
        max_range 10
    }

    damage_instance {
        damage 0

        effects {
            Shield 5+bonus_ranged_damage
        }
    }
}
```

---

### `GoodBone_copy`
**Source:** `special_enemy_abilities.gon`  

```
GoodBone_copy {
    variant_of GoodBone
}
```

---

### `ZombieFeast`
**Name:** Feast  
**Source:** `special_enemy_abilities.gon`  

```
ZombieFeast {
    template melee_attack
    
    meta {
        name "EABILITY_FEAST_NAME"
        animate_name true
    }

    graphics {
        animation dashbite
    }

    cost {
        mana 5
    }

    target {
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 10

        effects {
            VaporizeCorpse 1

            ApplyToSource {
                ConstitutionUp 2
                StrengthUp 3
                HealthGain 8
                TakeExtraTurn 1
            }
        }
    }
}
```

---

### `ZombieFeastSmall`
**Name:** Feast  
**Source:** `special_enemy_abilities.gon`  

```
ZombieFeastSmall {
    template melee_attack
    
    meta {
        name "EABILITY_FEAST_NAME"
        animate_name true
    }

    graphics {
        animation dashbite
    }

    cost {
        mana 5
    }

    target {
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 10

        effects {
            VaporizeCorpse 1

            ApplyToSource {
                ConstitutionUp 1
                StrengthUp 1
                HealthGain 4
                //TakeExtraTurn 1
            }
        }
    }
}
```

---

### `WolfDash`
**Source:** `special_enemy_abilities.gon`  

```
WolfDash {
    template dash_attack
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
    }

    sounds {
        ontrigger SE_WolfCatAttack
    }
    
    cost {
        mana 5
        charge 1
    }
    
    target {
        max_range 1
    }
    
    damage_instance {
        damage 7+bonus_melee_damage

        effects {
            //Bleed 2
        }
    }
}
```

---

### `WolfLeap`
**Name:** Wolf Leap  
**Source:** `special_enemy_abilities.gon`  

```
WolfLeap {
    template jump_attack

    meta {
        name "EABILITY_WOLFLEAP_NAME"
    }

    graphics {
        jump_attack_animation land
    }

    sounds {
        ontrigger SE_WolfCatLeap
    }
    
    cost {
        mana 5
        charge 1
    }

    target {
        max_range 4
    }

    damage_instance {
        damage 3+bonus_melee_damage
        effects {
            //Bleed 1
        }
    }
}
```

---

### `FearMelee`
**Source:** `special_enemy_abilities.gon`  

```
FearMelee {
    template melee_attack

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Fear 1
        }
    }
}
```

---

### `ReaperSpin`
**Name:** Spin  
**Source:** `special_enemy_abilities.gon`  

```
ReaperSpin {
    template melee_attack
    
    meta {
        name "EABILITY_SPIN_NAME"
    }

    graphics {
        animation attack
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode square
        knockback_mode character_to_tile
        multihit 3
        max_aoe 1
    }
    
    damage_instance {
        damage 4+bonus_melee_damage
    }
}
```

---

### `TattersFear`
**Source:** `special_enemy_abilities.gon`  

```
TattersFear {
    template targeted_status

    target {
        max_range 20
    }

    graphics {
        animation revenge
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Hex 1
        }
    }
}
```

---

### `SpookieLick`
**Source:** `special_enemy_abilities.gon`  

```
SpookieLick {
    template melee_attack

    self_damage {
        effects {
            RefreshMovePoints 1
        }
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            ManaSteal -1
        }
    }
}
```

---

### `ScaryHaunt`
**Name:** DOOM  
**Source:** `special_enemy_abilities.gon`  

```
ScaryHaunt {
    template melee_attack
    
    meta {
        name "EABILITY_DOOM_NAME"
        animate_name true
    }

    graphics {
        animation haunt
    }

    damage_instance {
        damage 0
        type status_spell
        custom_additional_ai_weight avoid_redundant_debuffs_strict

        effects {
            Doomed 3
        }
    }
}
```

---

### `ScaryFear`
**Source:** `special_enemy_abilities.gon`  

```
ScaryFear {
    template melee_attack

    graphics {
        animation attack
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Fear 1
        }
    }
}
```

---

### `ReaperRevenge`
**Source:** `special_enemy_abilities.gon`  

```
ReaperRevenge {
    template teleport

    self_damage {
        effects {
            AllStatsUp 1
            HealthGain 4
        }
    }

    target { 
        max_range 20
    }
}
```

---

### `TattersSpin`
**Source:** `special_enemy_abilities.gon`  

```
TattersSpin {
    template lobbed_attack

    graphics {
        animation attack
    }
    
    cost {
        mana 5
    }
    
    target {
        target_mode none
        aoe_mode circle
        aoe_excludes_self true
        knockback_mode character_to_tile
        multihit 2
        max_aoe 2

        aoe_restrictions [allies_only]
    }
    
    damage_instance {
        damage 0
        effects {
            Shield 4
        }
    }
}
```

---

### `TattersLeeches`
**Source:** `special_enemy_abilities.gon`  

```
TattersLeeches {
    template lobbed_attack

    graphics {
        animation attack
		projectile LeechProjectile
    }
    
    cost {
        mana 5
    }
    
    target {
        target_mode none
        aoe_mode circle
        aoe_excludes_self true
        knockback_mode character_to_tile
        max_aoe 2

        aoe_restrictions [enemies_only]
    }
    
    damage_instance {
        damage 0
        effects {
            Leeches 1
        }
    }
}
```

---

### `HexShot`
**Name:** Leeches  
**Source:** `special_enemy_abilities.gon`  

```
HexShot {
    template lobbed_attack
    
    meta {
        name "EABILITY_LEECHES_NAME"
        animate_name true
    }
	
	graphics {
        projectile LeechProjectile
    }

    target {
        min_range 1
        max_range 20
        restrictions none
    }

    damage_instance {
        damage 0
        effects {
          //  Hex 1
            Leeches 1
        }
    }
}
```

---

### `RobesBuff`
**Name:** Shriek  
**Source:** `special_enemy_abilities.gon`  

```
RobesBuff {
    template targeted_status
    
    meta {
        name "EABILITY_SHRIEK_NAME"
        animate_name true
    }

    cost {
        cantrip true
    }

    target {
        min_range 1
        max_range 20
        restrictions none
    }

    damage_instance {
        effects {
            DamageUp 2
        }
    }
}
```

---

### `ZombieTombstone`
**Source:** `special_enemy_abilities.gon`  

```
ZombieTombstone {
    template spawn
    
    graphics {
        lob false
        animation none
    }
    
    
    target {
        target_mode none
        aoe_mode cross
        max_aoe 1
        min_targets 1
        max_targets 1
        aoe_restrictions [must_be_empty]
    }

    spawn {
        object ZombieCat
    }
}
```

---

### `Leave`
**Name:** Leave  
**Source:** `special_enemy_abilities.gon`  

```
Leave {
    template leave

    meta {
        name "EABILITY_LEAVE_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true
    }

    cost {
        cantrip true
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `Return`
**Name:** Return  
**Source:** `special_enemy_abilities.gon`  

```
Return {
    template return

    meta {
        name "EABILITY_RETURN_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `ReturnAnywhere`
**Name:** Return  
**Source:** `special_enemy_abilities.gon`  

```
ReturnAnywhere {
    template return

    meta {
        name "EABILITY_RETURN_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true
    }

    target {
        max_range 20
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `ReturnAnywhereIgnoreTrample`
**Name:** Return  
**Source:** `special_enemy_abilities.gon`  

```
ReturnAnywhereIgnoreTrample {
    template return

    meta {
        name "EABILITY_RETURN_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true
    }

    target {
        max_range 20   
        restrictions must_be_movable_ignore_trample
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `SpiderReturn`
**Name:** Return  
**Source:** `special_enemy_abilities.gon`  

```
SpiderReturn {
    template return

    meta {
        name "EABILITY_RETURN_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true
    }

    cost {
        cantrip true
    }

    target {
        max_range 20   
        restrictions must_be_movable_ignore_trample
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `SpiderSpawn`
**Name:** Spider Spawn  
**Source:** `special_enemy_abilities.gon`  

```
SpiderSpawn {
    template spawn

    meta {
        name "EABILITY_SPIDERSPAWN_NAME"
    }

    cost {
        allow_offmap_casts true
        must_be_offmap true
    }

    graphics {
        animation egg
        lob true
    }
    
    
    target {
        max_range 20
        min_range 0
        knockback_mode none
    }

    spawn {
        object SpiderCat
        first_turn initiative
        faction self
    }
}
```

---

### `QueenWeb`
**Name:** Web  
**Source:** `special_enemy_abilities.gon`  

```
QueenWeb {
    template lobbed_attack
    
    meta {
        name "EABILITY_WEB_NAME"
    }

    graphics {
        projectile WebTrap
        use_rotation false
        animation web
    }

    target {
        min_range 1
        max_range 5

        max_aoe 1
        max_targets 4
        multihit 2
        stagger_multihit_targets true
         
        restrictions [must_have_animate_character must_have_living_character]
        //aoe_restrictions [must_be_partially_empty must_not_have_known_trap]
    }

    damage_instance {
        damage 0
        ai_base_score 10
        custom_additional_ai_weight tile_close_to_enemy
        
        effects {
            SpawnNeutralWebTrapOnMiss 1
            Webbed 1
        }
    }
}
```

---

### `QueenMinis`
**Name:** Spawn Spiderlings  
**Source:** `special_enemy_abilities.gon`  

```
QueenMinis {
    template lobbed_attack
    
    meta {
        name "EABILITY_SPAWNSPIDERLING_NAME"
    }

    graphics {
        projectile BabySpider
        use_rotation false
        animation web
    }

    target {
        min_range 1
        max_range 3

        max_aoe 1
        max_targets 2
        multihit 2
        stagger_multihit_targets true

        restrictions aoe_must_exist
        aoe_restrictions [must_be_partially_empty]
    }

    damage_instance {
        damage 0
        ai_base_score 10
        custom_additional_ai_weight tile_close_to_enemy
        
        effects {
            BounceObject TinySpider
        }
    }
}
```

---

### `Spider_GoInsane`
**Name:** Go Insane!  
**Source:** `special_enemy_abilities.gon`  

```
Spider_GoInsane {
    template self_buff
    
    meta {
        name "EABILITY_GOINSANE_NAME"
    }

    graphics { 
        animation insane
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            FormChange {
                form "Insane_Ground"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `Spider_CalmDown`
**Name:** Calm Down!  
**Source:** `special_enemy_abilities.gon`  

```
Spider_CalmDown {
    template self_buff
    
    meta {
        name "EABILITY_CALMDOWN_NAME"
    }

    graphics { 
        animation calmdown
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            FormChange {
                form "Default_Ground"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `ButtWeb`
**Name:** Butt Web  
**Source:** `special_enemy_abilities.gon`  

```
ButtWeb {
    template lobbed_attack
    
    meta {
        name "EABILITY_BUTTWEB_NAME"
    }

    graphics {
        projectile WebTrap
        use_rotation false
        animation revenge
    }

    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[-1 0]]
        knockback_mode none
        aoe_considers_character_size true
        aoe_excludes_self true
        restrictions none
        aoe_restrictions none
    }

    self_damage {
        effects {
            QueueUseAbility Spider_GoInsane
        }
    }

    damage_instance {
        damage 0
        
        effects {
            SpawnNeutralWebTrapOnMiss 1
            Webbed 1
        }
    }
}
```

---

### `ButtWeb_AlreadyEnraged`
**Name:** Butt Web  
**Source:** `special_enemy_abilities.gon`  

```
ButtWeb_AlreadyEnraged {
    template lobbed_attack
    
    meta {
        name "EABILITY_BUTTWEB_NAME"
    }

    graphics {
        projectile WebTrap
        use_rotation false
        animation revenge
    }

    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[-1 0]]
        knockback_mode none
        aoe_considers_character_size true
        aoe_excludes_self true
        restrictions none
        aoe_restrictions none
    }

    damage_instance {
        damage 0
        
        effects {
            SpawnNeutralWebTrapOnMiss 1
            Webbed 1
        }
    }
}
```

---

### `ExtraMove`
**Source:** `special_enemy_abilities.gon`  

```
ExtraMove {
    variant_of DefaultMove

    cost {
        cantrip true
    }
}
```

---

### `ShamblerToss`
**Name:** Toss  
**Source:** `special_enemy_abilities.gon`  

```
ShamblerToss {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        animation throw
        use_placeholder true
        face_toss_target true
    }

    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_range 8
        min_range 5
        restrictions none
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        custom_additional_ai_weight toss_far
    }
}
```

---

### `ShamblerDash`
**Source:** `special_enemy_abilities.gon`  

```
ShamblerDash {
    template dash_attack
    class FullyAnimatedDashAttackAbility
    
    graphics {
        animation attack
        sync_frames 26
    }
    
    cost {
        mana 0
    }
    
    target {
        max_range 2
        consider_trample true
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1
    }
}
```

---

### `ButtFlip`
**Name:** Flip  
**Source:** `special_enemy_abilities.gon`  

```
ButtFlip {
    template self_buff
    
    meta {
        name "EABILITY_FLIP_NAME"
    }

    graphics { 
        animation flip
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            FormChange {
                form "Down"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `TeleportFlipUp`
**Name:** Flip  
**Source:** `special_enemy_abilities.gon`  

```
TeleportFlipUp {
    template teleport

    meta {
        name "EABILITY_FLIP_NAME"
    }

    graphics {
        animation_out portout
        animation_in portin
    }

    target {
        max_range 20
        dont_orient true
    }

    self_damage {
        effects {
            FormChange {
                form Up
            }
        }
    }
}
```

---

### `ButtFart`
**Name:** Fart  
**Source:** `special_enemy_abilities.gon`  

```
ButtFart {
    template spell

    meta {
        name "EABILITY_FART_NAME"
    }

    graphics {
        particle PoisonPoof
        animation attack
    }
    
    cost {
        cantrip true
        mana 4
    }

    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 1

        aoe_considers_character_size true
        aoe_excludes_self true
        dont_orient true
    }
    
    damage_instance {
        damage 0
        knockback 1

        effects {
            Poison 4
        }
        
        elements [
            Poison
        ]
    }
}
```

---

### `BumbleButt`
**Name:** Fart  
**Source:** `special_enemy_abilities.gon`  

```
BumbleButt {
    template spell

    meta {
        name "EABILITY_FART_NAME"
    }

    graphics {
        particle PoisonPoof
        animation revenge
    }
    
    cost {
        cantrip true
        mana 4
    }

    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 1

        aoe_considers_character_size true
        aoe_excludes_self true
        dont_orient true
    }
    
    damage_instance {
        damage 0
        knockback 1

        effects {
            Poison 2
        }
        
        elements [
            Poison
        ]
    }
}
```

---

### `SpawnWisp`
**Name:** Spawn Wisp  
**Source:** `special_enemy_abilities.gon`  

```
SpawnWisp {
    template spawn

    meta {
        name "EABILITY_SPAWNWISP_NAME"
    }
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        cantrip true
    }
    
    target {
        max_range 2
    }

    spawn {
        object Wisp
        ai_base_score 9999
        faction self
    }
}
```

---

### `RockToss_BomberRat`
**Name:** Bomb Toss  
**Source:** `special_enemy_abilities.gon`  

```
RockToss_BomberRat {
    template lobbed_attack

    meta {
        name "EABILITY_BOMBTOSS_NAME"
    }

    graphics {
        projectile Bomb
        animation attack
        use_rotation false
    }
    
    cost {
        mana 5
        cantrip true
    }
    
    target {
        max_range 5
    }
    
    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Stun [1, .10]
            BounceObject Bomb
        }

        elements [
            Rock
        ]
    }
}
```

---

### `ThumpSlam`
**Source:** `special_enemy_abilities.gon`  

```
ThumpSlam {
    template jump_attack

    graphics {
        jump_start_animation none
        full_jump_animation jump
        full_jump_sync_frames 42
        full_jump_windup_frames 6
    }

    cost {
        act_points 1
        move_points 0
    }
    
    target {
        max_range 2
        min_range 2
        range_mode cross
        range_considers_character_size false
        min_aoe 0
        max_aoe 1
    }

    temporary_effects {
        DisableTrample 1
    }

    damage_instance {
        type melee
        damage 5+bonus_melee_damage
        knockback 1

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `ThumpSlam_Mov`
**Source:** `special_enemy_abilities.gon`  

```
ThumpSlam_Mov {
    variant_of ThumpSlam
}
```

---

### `MarshmallowConvert`
**Name:** Convert  
**Source:** `special_enemy_abilities.gon`  

```
MarshmallowConvert {
    template spell
    
    meta {
        name "EABILITY_CONVERT_NAME"
    }

    graphics {
        animation lickAttack
        particle none
    }
    
    cost {
        mana 0
    }

    target {
        min_range 1
        max_range level
        max_aoe 0
    }

    bonus_passives {
        AbilityEnabledOncePerRound 1
    }
    
    damage_instance {
        damage 0
        type spell
        //custom_additional_ai_weight one_charmed_enemy_at_a_time

        effects {
            Charmed 1
            TakeExtraTurn 1
            GenericDebuff 999 //for AI, compensate for TakeExtraTurn being a big buff
        }
    }
}
```

---

### `MarshmallowZealot`
**Name:** Zealot  
**Source:** `special_enemy_abilities.gon`  

```
MarshmallowZealot {
    template self_buff
    
    meta {
        name "EABILITY_ZEALOT_NAME"
    }

    graphics {
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        effects {
            DivineShield 1
        }
    }
}
```

---

### `BasicMelee_2Hits`
**Source:** `special_enemy_abilities.gon`  

```
BasicMelee_2Hits {
    variant_of BasicMelee

    target {
        multihit 2
    }
}
```

---

### `BasicMelee_3Hits`
**Source:** `special_enemy_abilities.gon`  

```
BasicMelee_3Hits {
    variant_of BasicMelee

    target {
        multihit 3
    }
}
```

---

### `BasicMelee_4Hits`
**Source:** `special_enemy_abilities.gon`  

```
BasicMelee_4Hits {
    variant_of BasicMelee

    target {
        multihit 4
    }
}
```

---

### `BasicMelee_5Hits`
**Source:** `special_enemy_abilities.gon`  

```
BasicMelee_5Hits {
    variant_of BasicMelee

    target {
        multihit 5
    }
}
```

---

### `FormGrowTwoSnakey`
**Source:** `special_enemy_abilities.gon`  

```
FormGrowTwoSnakey {
    variant_of FormGrowTwo

    graphics { 
        dont_orient true
    }

    damage_instance {
        effects {
            Shield 1
            EndTurn 1
            DamageUp 1
        }
    }
}
```

---

### `FormGrowThreeSnakey`
**Source:** `special_enemy_abilities.gon`  

```
FormGrowThreeSnakey {
    variant_of FormGrowThree

    graphics { 
        dont_orient true
    }

    damage_instance {
        effects {
            Shield 1
            EndTurn 1
            DamageUp 1
        }
    }
}
```

---

### `FormShrinkTwoSnakey`
**Source:** `special_enemy_abilities.gon`  

```
FormShrinkTwoSnakey {
    variant_of FormShrinkTwo

    damage_instance {
        effects {
            DamageUp -1
        }
    }
}
```

---

### `FormShrinkOneSnakey`
**Source:** `special_enemy_abilities.gon`  

```
FormShrinkOneSnakey {
    variant_of FormShrinkOne

    damage_instance {
        effects {
            DamageUp -1
        }
    }
}
```

---

### `BoneWormShotSmall`
**Name:** Bone Shot  
**Source:** `special_enemy_abilities.gon`  

```
BoneWormShotSmall {
    template lobbed_attack
    
    meta {
        name "EABILITY_BONESHOT_NAME"
    }

    graphics {
        projectile BoneProjectile
        use_rotation false
    }

    cost {
        act_points 1
    }

    target {
        min_range 1
        max_range 4
    }

    damage_instance {
        damage 3+bonus_ranged_damage
    }
}
```

---

### `BoneWormShotMed`
**Name:** Bone Shot  
**Source:** `special_enemy_abilities.gon`  

```
BoneWormShotMed {
    template lobbed_attack
    
    meta {
        name "EABILITY_BONESHOT_NAME"
    }

    graphics {
        projectile BoneProjectile
        use_rotation false
    }

    cost {
        act_points 1
    }

    target {
        min_range 1
        max_range 7
    }

    damage_instance {
        damage 4+bonus_ranged_damage
    }
}
```

---

### `BoneWormShotTall`
**Name:** Bone Shot  
**Source:** `special_enemy_abilities.gon`  

```
BoneWormShotTall {
    template lobbed_attack
    
    meta {
        name "EABILITY_BONESHOT_NAME"
    }

    graphics {
        projectile BoneProjectile
        use_rotation false
    }

    cost {
        act_points 1
    }

    target {
        min_range 1
        max_range 10
    }

    damage_instance {
        damage 4+bonus_ranged_damage
    }
}
```

---

### `CarcusSpawn`
**Source:** `special_enemy_abilities.gon`  

```
CarcusSpawn {
    template spawn
    
    graphics {
        lob true
        animation spawn
        dont_orient true
        dont_visualize_ai true
    }
    
    
    target {
        max_range 1
        allow_any_orientation true
    }

    spawn {
        object [TumorousMaggot, ChargeyMaggot, Maggot]
        first_turn initiative
        faction self
    }
}
```

---

### `GenericRage`
**Source:** `special_enemy_abilities.gon`  

```
GenericRage {
    template self_buff

    graphics { 
        dont_orient true
        animation rage
    }

    damage_instance {
        effects {
            FormChange {
                form "Rage"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `PeashyStab`
**Source:** `special_enemy_abilities.gon`  

```
PeashyStab {
    template melee_attack
    ai_ability BasicMelee //needed so baby shark's simple brain can understand this

    cost {
        act_points 1
    }

    damage_instance {
        damage 3+bonus_melee_damage
        crit_chance 25%

        effects {
            Bleed 3
        }
    }
}
```

---

### `Dash_BabyDeathWorm`
**Name:** Dash  
**Source:** `special_enemy_abilities.gon`  

```
Dash_BabyDeathWorm {
    template dash_attack
    
    meta {
        name "EABILITY_DASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }
    
    cost {
        mana 5
    }
    
    target {

    }
    
    damage_instance {
        damage 4+bonus_melee_damage

        effects {
            FlatLeech 2
        }
    }
}
```

---

### `DeathWormTrampleDash`
**Name:** Sand Rush  
**Source:** `special_enemy_abilities.gon`  

```
DeathWormTrampleDash {
    template trample_dash
    
    meta {
        name "EABILITY_SANDRUSH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
        dash_bonk_animation bonk
    }
    
    cost {
        mana 5
    }
    
    target {

    }

    self_damage {
        effects {
            DeathwormUnderground DeathWormEat
            EndTurn 1
        }
    }
    bonk_damage {
        damage 0

        effects {
            Stun 1
        }
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `DeathWormTrampleDash_Reaction_ai`
**Source:** `special_enemy_abilities.gon`  

```
DeathWormTrampleDash_Reaction_ai { //copy of the megafetusmelee_ai
    template melee_attack

    target { 
        aoe_considers_character_size true
        aoe_mode cone
        max_aoe 20
        min_aoe 2
        aoe_leading_edge_only true
    }

    damage_instance {
        contact_requires_adjacency false
    }
}
```

---

### `DeathWormTrampleDash_Reaction`
**Source:** `special_enemy_abilities.gon`  

```
DeathWormTrampleDash_Reaction {
    variant_of DeathWormTrampleDash
    ai_ability DeathWormTrampleDash_Reaction_ai
}
```

---

### `DeathWormEat`
**Name:** Eat  
**Source:** `special_enemy_abilities.gon`  

```
DeathWormEat {
    template return
    
    meta {
        name "EABILITY_EAT_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true
        animation eat
    }

    temporary_effects {
        DisableTrample 1
    }

    target {
        restrictions aoe_must_be_force_displaceable 
        min_range 0
        max_range 0
    }

    damage_instance {
        ai_base_score 100

        effects {
            Vaporize 1
            IgnoreSelf 1
        }
    }
}
```

---

### `DeathWormReturn`
**Name:** Return  
**Source:** `special_enemy_abilities.gon`  

```
DeathWormReturn {
    template return
    
    meta {
        name "EABILITY_RETURN_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true
        animation appear
    }

    cost {
        move_points 0
        act_points 1
    }

    target {
        restrictions aoe_must_be_force_displaceable 
        min_range 0
        max_range 0
    }
}
```

---

### `RattleSnakeAttack`
**Name:** Poison Attack  
**Source:** `special_enemy_abilities.gon`  

```
RattleSnakeAttack {
    template melee_attack
    
    meta {
        name "EABILITY_POISONATTACK_NAME"
        animate_name false
    }

    graphics {
        animation attack
    }

    self_damage {
        effects {
            RefreshMovePoints 1
        }
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Poison 1
        }
    }
}
```

---

### `RattleSnakeTrap`
**Name:** Poison Attack  
**Source:** `special_enemy_abilities.gon`  

```
RattleSnakeTrap {
    template melee_attack
    
    meta {
        name "EABILITY_POISONATTACK_NAME"
        animate_name false
    }

    graphics {
        animation attack
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Poison 1
        }
    }
}
```

---

### `HornyToadShot`
**Source:** `special_enemy_abilities.gon`  

```
HornyToadShot {
    variant_of BasicStraightShot

    graphics {
        animation shoot
        projectile Projectile
    }

    damage_instance {
        effects {
            Blind 1
        }
    }
}
```

---

### `ScorpionSting`
**Name:** Sting  
**Source:** `special_enemy_abilities.gon`  

```
ScorpionSting {
    variant_of BasicMelee

    meta {
        name "EABILITY_STING_NAME"
        animate_name true
    }

    graphics {
        animation scorpionSting
    }
    sounds {
        ontrigger SE_ScorpionCatAngry
    }

    damage_instance {
        effects {
            Poison 1
        }
    }
}
```

---

### `ScorpionHold`
**Name:** Grapple  
**Source:** `special_enemy_abilities.gon`  

```
ScorpionHold {
    variant_of BasicMelee
    class PlaceholderMeleeAttackAbility

    meta {
        name "EABILITY_GRAPPLE_NAME"
        animate_name true
    }

    graphics {
        animation bearHug
    }

    sounds {
        ontrigger SE_ScorpionCatHug
    }

    target {
        knockback_mode tile_to_character

        aoe_considers_character_size false
        target_mode tile
        restrictions must_have_character
        range_mode standard
        aoe_mode standard
        min_range 1
        max_range 1
        min_aoe 0 
        max_aoe 0 
    }

    damage_instance {
        damage 1+bonus_melee_damage
        effects {
            Grappled 1
            EndTurn 1
        }
    }
}
```

---

### `GuncatShoot`
**Name:** Shoot Gun  
**Source:** `special_enemy_abilities.gon`  

```
GuncatShoot {
    template ranged_attack

    meta {
        name "EABILITY_SHOOTGUN_NAME"
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
        min_range 1
        max_range 20
    }

    damage_instance {
        damage 4+bonus_ranged_damage
    }
}
```

---

### `ZodiacShoot`
**Source:** `special_enemy_abilities.gon`  

```
ZodiacShoot {
    template straightshot_attack

    graphics {
        projectile Bullet
        animation shoot
        empty_animation empty
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

        max_targets -X //-1 means no target limit, if no ammo then X is 0
        X_is enable_if_has_ammo
    }

    empty_self_damage {
        effects {
            FormChange passive
        }
    }

    self_damage {
        effects {
            Ammo -1
        }
    }

    damage_instance {
        damage 7+bonus_ranged_damage
    }
}
```

---

### `Reload`
**Name:** Reload  
**Source:** `special_enemy_abilities.gon`  

```
Reload {
    template self_buff
    
    meta {
        name "EABILITY_RELOAD_NAME"
    }

    graphics {
        animation reload
    }
    
    cost {
        mana 5
    }
    
    damage_instance {
        effects {
            Ammo -99999 //clear existing ammo
            Ammo 6 //then set it to 6
            FormChange active
        }
        ai_base_score 10
        custom_additional_ai_weight avoid_redundant_debuffs_strict
    }
}
```

---

### `RubberFistBotPunch`
**Source:** `special_enemy_abilities.gon`  

```
RubberFistBotPunch {
    template melee_attack

    cost {
        mana 0
    }

    /*self_damage {
        damage 1
    }*/

    damage_instance {
        damage 0
        knockback 10
    }
}
```

---

### `TwisterMove`
**Source:** `special_enemy_abilities.gon`  

```
TwisterMove {
    template move

    target {
        restrictions [must_move]
    }
    sounds {
        ontrigger Twister_move
    }
}
```

---

### `LennyGrab`
**Source:** `special_enemy_abilities.gon`  

```
LennyGrab {
    template targeted_status

    graphics {
        animation grab
    }

    cost {
        mana 0
        must_not_be_consuming true
        cantrip true
    }

    target {
        max_range 1
        range_mode cross
        restrictions [must_have_buddy must_have_living_character]
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                instant true
                mount_mode true
                force_contact true
                drop_on_death false
                do_not_pop_corpse true
                struggle_ability LennyStruggle
            }
            GenericDebuff 1 //for AI
        }

        custom_additional_ai_weight must_target_buddy
    }
}
```

---

### `LennyGrabDead`
**Source:** `special_enemy_abilities.gon`  

```
LennyGrabDead {
    template targeted_status

    graphics {
        animation grabCorpse
    }

    cost {
        mana 0
        must_not_be_consuming true
        cantrip true
    }

    target {
        max_range 1
        range_mode cross
        restrictions [must_have_buddy must_have_corpse]
    }

    self_damage {
        effects {
            FormChange HasDeadCat
        }
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                instant true
                mount_mode true
                force_contact true
                drop_on_death false
                do_not_pop_corpse true
                struggle_ability LennyStruggle
            }
            GenericDebuff 1 //for AI
        }

        custom_additional_ai_weight must_target_buddy
    }
}
```

---

### `LennyCatDies`
**Source:** `special_enemy_abilities.gon`  

```
LennyCatDies {
    template self_buff
    class DamageConsumedCharactersAbility

    cost {

    }

    graphics {
        animation catdying
    }
    
    
    target {
        target_mode none
        knockback_mode none
    }

    self_damage {
        effects {
            FormChange HasDeadCat
        }
    }

    damage_instance {
        damage 0
        type none
    }
}
```

---

### `LennyHug`
**Name:** Hug  
**Source:** `special_enemy_abilities.gon`  

```
LennyHug {
    template self_buff
    class DamageConsumedCharactersAbility

    meta {
        name "EABILITY_HUG_NAME"
        animate_name true
    }

    cost {

    }

    graphics {
        animation hug
    }
    
    
    target {
        target_mode none
        knockback_mode none
        prioritize_dont_change_direction true
    }

    damage_instance {
        damage 1+bonus_melee_damage //should be 4 damage total with 8 str on lenny
        type melee
        contact_requires_adjacency false
        ai_base_score 9999
    }
}
```

---

### `LennyStruggleFail`
**Source:** `special_enemy_abilities.gon`  

```
LennyStruggleFail {
    variant_of LennyHug

    graphics {
        animation struggle
    }
}
```

---

### `LennyDrop`
**Name:** Drop Cat  
**Source:** `special_enemy_abilities.gon`  

```
LennyDrop {
    template throw_attack
    
    meta {
        name "EABILITY_DROPCAT_NAME"
    }

    graphics {
        animation escape
        min_throw_height 0
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        max_range 1
        min_range 1
        restrictions none
        throw_consumed_character true
        prioritize_dont_change_direction true
        reorient_thrown_character true
        range_mode cross

    }
    
    damage_instance {
        damage 0
        ai_base_score 9999
    }
}
```

---

### `LennyCatSlap`
**Name:** Cat Slap  
**Source:** `special_enemy_abilities.gon`  

```
LennyCatSlap {
    template melee_attack
    
    meta {
        name "EABILITY_CATSLAP_NAME"
        animate_name false
    }

    cost {
        mana 0
    }

    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 10

        effects {
            CollideWithConsumed 1+bonus_melee_damage
        }
    }
}
```

---

### `LennyShove`
**Source:** `special_enemy_abilities.gon`  

```
LennyShove {
    template melee_attack

    cost {
        mana 0
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 10

        custom_additional_ai_weight must_not_target_buddy
    }
}
```

---

### `BirdFly`
**Source:** `special_enemy_abilities.gon`  

```
BirdFly {
    template move

    graphics {
        move_start_animation moveStart
        animation moveLoop
        move_end_animation moveEnd
    }

    target {
        as_the_crow_flies true
    }
}
```

---

### `CatSpin`
**Name:** Big Spin  
**Source:** `special_enemy_abilities.gon`  

```
CatSpin {
    template melee_attack
    
    meta {
        name "EABILITY_BIGSPIN_NAME"
    }

    graphics {
        animation singleSpin
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode square
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `CatGoop`
**Source:** `special_enemy_abilities.gon`  

```
CatGoop {
    template straightshot_attack

    graphics {
        animation shoot
    }

    cost {
        mana 0
    }

    target {
        max_aoe 10
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Poison 2
        }
    }
}
```

---

### `AtomicBurst`
**Name:** Radiate  
**Source:** `special_enemy_abilities.gon`  

```
AtomicBurst {
    template spell
    
    meta {
        name "EABILITY_RADIATE_NAME"
    }

    graphics {
        animation radiant
        dont_orient true
		particle fx_magicSplash
    }

    target {
        target_mode none
        min_aoe 1
        max_aoe 2
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 3+bonus_basic_spell_damage
        knockback 3

        elements [
            Mutate
        ]
    }
}
```

---

### `CultistCut`
**Name:** Cut  
**Source:** `special_enemy_abilities.gon`  

```
CultistCut {
    template self_buff
    
    meta {
        name "EABILITY_CUT_NAME"
    }

    graphics {
        animation selfHarm
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        damage 1

        ai_base_score 99999
    }
}
```

---

### `BBTransformMutant`
**Source:** `special_enemy_abilities.gon`  

```
BBTransformMutant {
    template self_buff

    graphics { 
        dont_orient true
        animation becomemutant
    }

    damage_instance {
        effects {
            FormChange {
                form "Mutant"
            }
            Brace 2
        }
        ai_base_score 9999
    }
}
```

---

### `BBTransformZealot`
**Source:** `special_enemy_abilities.gon`  

```
BBTransformZealot {
    template self_buff

    graphics { 
        dont_orient true
        animation becomezealot
    }

    damage_instance {
        effects {
            FormChange {
                form "Zealot"
            }
            FullHeal 1
        }
        ai_base_score 9999
    }
}
```

---

### `BBPickupCrown`
**Source:** `special_enemy_abilities.gon`  

```
BBPickupCrown {
    template melee_attack
    class MeleeEatAbility

    graphics {
        animation pickup
    }

    target { 
        target_mode tile
        min_range 0
        max_range 1
        
        min_aoe 0
        max_aoe 0

        restrictions [must_have_tag]
        target_requires_tag bishop_hat
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true

        effects {
            ApplyToSource {
                FormChange {
                    form "Bishop"
                }
                Cleanse 0
                FullHeal 1
                DivineShield 2
                KineticSpikes 1
            }

            Vaporize 20
            FlatLeech 10
        }

        ai_base_score 9999
    }
}
```

---

### `BBToss`
**Name:** Toss  
**Source:** `special_enemy_abilities.gon`  

```
BBToss {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        animation throw
        use_placeholder true
        face_toss_target true
        dont_visualize_ai true
    }

    cost {
        mana 0
    }
    
    target {
        max_range 4
        min_range 2
        restrictions none
        range_mode cross
        toss_direction_restriction backwards
    }
    
    damage_instance {
        damage 1+bonus_melee_damage
        custom_additional_ai_weight toss_far
    }
}
```

---

### `BBStabby`
**Source:** `special_enemy_abilities.gon`  

```
BBStabby {
    template melee_attack

    target {
        multihit 3
    }

    damage_instance {
        damage 1+bonus_melee_damage
        type melee

        effects {
            Bleed 1
        }
    }
}
```

---

### `BBSpin`
**Name:** Spin  
**Source:** `special_enemy_abilities.gon`  

```
BBSpin {
    template melee_attack
    
    meta {
        name "EABILITY_SPIN_NAME"
    }

    graphics {
        animation spin
    }
    
    cost {
        mana 0
    }
    
    target {
        aoe_mode cross
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 4+bonus_melee_damage
    }
}
```

---

### `BBCut`
**Name:** Cut  
**Source:** `special_enemy_abilities.gon`  

```
BBCut {
    template self_buff
    
    meta {
        name "EABILITY_CUT_NAME"
    }

    graphics {
        animation cut
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        damage 1
        type melee

        effects {
            DamageUp 1
        }
        ai_base_score 9999
    }
}
```

---

### `BBPullBomb`
**Source:** `special_enemy_abilities.gon`  

```
BBPullBomb {
    template self_buff

    graphics { 
        dont_orient true
        animation bomb
    }

    damage_instance {
        effects {
            FormChange {
                form "ZealotBomb"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `BBExplode`
**Source:** `special_enemy_abilities.gon`  

```
BBExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation explode
    }
    
    cost {
        mana 5
    }
    
    target {
        knockback_mode character_to_tile
        aoe_excludes_self true
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 1
    }

    self_damage {
        piercing true
        cant_miss true
        effects {
            DeferVaporize 1
        }
    }
    
    damage_instance {
        damage 7
        knockback 1

        elements [
            Explosion
        ]
    }
}
```

---

### `BBMutantSwipe`
**Source:** `special_enemy_abilities.gon`  

```
BBMutantSwipe {
    template melee_attack

    graphics {
        animation attack
    }
    
    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }

    damage_instance {
        damage 4+bonus_melee_damage

        effects {
            KnockUpAndAway {
                stacks 3
                distance 3
            }
        }
    }
}
```

---

### `BBXLightning`
**Name:** Crackle  
**Source:** `special_enemy_abilities.gon`  

```
BBXLightning {
    template spell

    meta {
        name "EABILITY_CRACKLE_NAME"
        animate_name true
    }
    
    cost {
        mana 0
    }

    graphics {
        particle Bolt
        delay 7
        animation spell
    }
    
    target {
        target_mode none
        aoe_mode diagcross
        max_aoe 10
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 5+bonus_basic_spell_damage
        
        effects {
            Stun [1, .25]
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `BBBless`
**Name:** Bless  
**Source:** `special_enemy_abilities.gon`  

```
BBBless {
    template spell

    meta {
        name "EABILITY_BLESS_NAME"
    }
    
    cost {
        mana 0
    }

    graphics {
        animation bless
        particle HealSmall
    }
    
    target {
        target_mode none
        
        aoe_mode square
        min_aoe 0
        max_aoe 10
        aoe_excludes_self true
        aoe_restrictions [allies_only]
    }
    
    damage_instance {
        heal 5

        effects {
            DamageUp 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `LoveBotHeal`
**Name:** Feel Good Drugs  
**Source:** `special_enemy_abilities.gon`  

```
LoveBotHeal {
    template tile_targeted_melee_attack

    meta {
        name "EABILITY_FEELGOODDRUGS_NAME"
    }
    
    cost {
        mana 0
    }

    graphics {
        animation heal
    }
    
    target {
        restrictions [must_not_have_tag]
        target_requires_tag robot
    }
    
    damage_instance {
        heal 4+bonus_melee_damage

        effects {
            SpeedUp 1
            OverHealToStatuses {
                stack_scale 0
                TakeExtraTurn 1
            }
        }
    }
}
```

---

### `LoveBotCounter`
**Name:** Feel Bad Drugs  
**Source:** `special_enemy_abilities.gon`  

```
LoveBotCounter {
    template melee_attack

    meta {
        name "EABILITY_FEELBADDRUGS_NAME"
    }

    graphics {
        animation attack
    }

    damage_instance {
        damage 4+bonus_melee_damage

        effects {
            RandomStatDown 1
            RandomStatusFromPool {
                Bleed 1
                Bleed 1
                Bleed 1
                Poison 1
                Poison 1
                Poison 1
                Slow 1
                Slow 1
                Slow 1
                Stun 1
                Madness 1
            }
        }
    }
}
```

---

### `SBotAttack`
**Source:** `special_enemy_abilities.gon`  

```
SBotAttack {
    template melee_attack

    target {
        multihit 2
    }

    damage_instance {
        damage 3+bonus_melee_damage
        type melee

        effects {
            Bleed 1
        }
    }
}
```

---

### `SBotAngryMove`
**Source:** `special_enemy_abilities.gon`  

```
SBotAngryMove {
    template move

    graphics {
        animation walkAngry
    }
}
```

---

### `SBotRecharge`
**Name:** Recharge  
**Source:** `special_enemy_abilities.gon`  

```
SBotRecharge {
    template self_buff
    
    meta {
        name "EABILITY_RECHARGE_NAME"
    }

    graphics {
        animation recharge
    }

    target {
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        effects {
            Shield 1
            MovementUp 1
        }
    }
}
```

---

### `SBotAnger`
**Source:** `special_enemy_abilities.gon`  

```
SBotAnger {
    template self_buff

    graphics { 
        dont_orient true
        animation rage
    }

    damage_instance {
        effects {
            FormChange {
                form "Angry"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `KillDoze`
**Name:** Killdoze  
**Source:** `special_enemy_abilities.gon`  

```
KillDoze {
    template trample_dash
    
    meta {
        name "EABILITY_KILLDOZE_NAME"
    }
    
    graphics {
        dash_start_animation ramStart
        dash_animation ramLoop
        dash_end_animation ramEnd
    }
    
    target {
        max_range 2
    }
    
    damage_instance {
        damage 3+bonus_melee_damage
    }
}
```

---

### `GunkShot`
**Source:** `special_enemy_abilities.gon`  

```
GunkShot {
    template lobbed_attack

    target {
        min_range 2
        max_range 3
        restrictions none
    }

    damage_instance {
        effects {
            Slow 1
        }
    }
}
```

---

### `BigGunkShot`
**Name:** Gunk Ball  
**Source:** `special_enemy_abilities.gon`  

```
BigGunkShot {
    template spell

    meta {
        name "EABILITY_GUNKBALL_NAME"
    }

    graphics {
        use_projectile true
        particle PoisonPoof
        delay 0
    }
    
    target {
        min_range 2
        max_range 3
        max_aoe 1
    }

    damage_instance {
        damage 3+bonus_basic_spell_damage
        
        effects {
            Slow 3
        }
    }
    splash_damage {
        damage 3+bonus_basic_spell_damage
        
        effects {
            Slow 1
        }
    }
}
```

---

### `MiniNukeExplodey`
**Source:** `special_enemy_abilities.gon`  

```
MiniNukeExplodey {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation explode
        delay 5
        visual_delay_but_simultaneous_damage 10
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode standard
        knockback_mode character_to_tile
        aoe_restrictions must_have_piercing_line_of_sight
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 3
    }
    
    damage_instance {
        damage 7
        knockback 1

        elements [
            Explosion
            Mutate
        ]
    }
}
```

---

### `JohnnyPush`
**Name:** Telekinesis  
**Source:** `special_enemy_abilities.gon`  

```
JohnnyPush {
    template spell

    meta {
        name "EABILITY_TELEKENESIS_NAME"
    }

    graphics {
        particle MagicMissleBlast
        animation telekinesis
    }
    
    target {
        max_aoe 0
        max_range 20
        knockback_mode character_to_target
    }
    
    damage_instance {
        damage 3+bonus_basic_spell_damage
        knockback 10

        effects {
            OverrideKnockbackDamage 3+bonus_basic_spell_damage
        }
    }
}
```

---

### `JohnnyPull`
**Source:** `special_enemy_abilities.gon`  

```
JohnnyPull {
    variant_of JohnnyPush
    target {
        knockback_mode target_to_character
    }
}
```

---

### `JohnnyMindControl`
**Name:** Mind Control  
**Source:** `special_enemy_abilities.gon`  

```
JohnnyMindControl {
    template spell
    
    meta {
        name "EABILITY_MINDCONTROL_NAME"
    }

    graphics {
        animation mindcontrol
		particle CharmedHearts
    }

    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 0
        type spell
        custom_additional_ai_weight avoid_redundant_debuffs_strict

        effects {
            Charmed 1
        }
    }
}
```

---

### `JohnnyMissile`
**Name:** Magic Missile  
**Source:** `special_enemy_abilities.gon`  

```
JohnnyMissile {
    template spell

    meta {
        name "EABILITY_MAGICMISSLE_NAME"
    }

    graphics {
        particle MagicMissleBlast
        use_projectile true
        projectile MagicMissileProjectile
        lob_height 1
        speed 20

        animation blast1
    }

    target {
        max_aoe 0
        max_range 20
    }

    self_damage {
        effects {
            RandomMagicMissile 1
            RandomMagicMissile 1
            RandomMagicMissile 1
        }
    }
    
    damage_instance {
        damage 3+bonus_basic_spell_damage
    }
}
```

---

### `JohnnyBlast`
**Name:** Mind Blast  
**Source:** `special_enemy_abilities.gon`  

```
JohnnyBlast {
    template spell
    
    meta {
        name "EABILITY_MINDBLAST_NAME"
    }

    graphics {
        animation blast1
        particle none
    }

    target {
        target_mode none
        aoe_mode circle
        min_aoe 0
        max_aoe 2
        aoe_excludes_self true
        aoe_considers_character_size true
    }
    
    damage_instance {
        damage 3+bonus_basic_spell_damage
        knockback 2

        effects {
            Stun [1 .1]
        }

        ai_base_score 999999
    }
}
```

---

### `JohnnyMegaBlast`
**Name:** Mega Mind Blast  
**Source:** `special_enemy_abilities.gon`  

```
JohnnyMegaBlast {
    template spell
    
    meta {
        name "EABILITY_MEGAMINDBLAST_NAME"
    }

    graphics {
        animation blast2
        particle none
    }

    target {
        target_mode none
        aoe_mode circle
        min_aoe 0
        max_aoe 20
        aoe_excludes_self true
        aoe_considers_character_size true
    }
    
    damage_instance {
        damage 3+bonus_basic_spell_damage
        knockback 10

        effects {
            OverrideKnockbackDamage 3+bonus_basic_spell_damage
            Stun [1 .1]
        }

        ai_base_score 999999
    }
}
```

---

### `JohnnyCryOne`
**Source:** `special_enemy_abilities.gon`  

```
JohnnyCryOne {
    template self_buff

    graphics {
        animation cry1
    }

    damage_instance {
        effects {
            JohnnyCriesForWashers 1
        }
    }
}
```

---

### `JohnnyCryTwo`
**Source:** `special_enemy_abilities.gon`  

```
JohnnyCryTwo {
    template self_buff

    graphics {
        animation cry2
    }

    damage_instance {
        effects {
            JohnnyCriesForWashers 2
        }
    }
}
```

---

### `CarnibulbEat`
**Source:** `special_enemy_abilities.gon`  

```
CarnibulbEat {
    template melee_attack
    class MeleeEatAbility
    ai_ability BasicBigMelee //needed so daddy shark's simple brain can understand this

    graphics {
        animation eat
    }

    target { 
        max_aoe 1
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true

        effects {
            Conditional_Boss {
                OverrideDamage 25
            } Else {
                Vaporize 20
            }
        }
    }
}
```

---

### `SproutSpore`
**Source:** `special_enemy_abilities.gon`  

```
SproutSpore {
    template spell

    graphics {
        animation spore
        particle none
        dont_orient true
    }

    target {
        target_mode none
        aoe_excludes_self true
    }

    damage_instance {
        damage 0

        effects {
            Possessed 1
        }

        elements [
            Grass
        ]

    }
}
```

---

### `Sprout`
**Name:** Sprout  
**Source:** `special_enemy_abilities.gon`  

```
Sprout {
    template spawn

    meta {
        name "EABILITY_SPROUT_NAME"
    }
    
    graphics {
        lob false
        animation spawn
        dont_visualize_ai true
        dont_orient true
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        max_targets 1
    }

    spawn {
        object Sprout
        ai_base_score 99999
        faction self
    }
}
```

---

### `QuakeJump`
**Name:** Quake Jump  
**Source:** `special_enemy_abilities.gon`  

```
QuakeJump {
    template jump_attack

    meta {
        name "EABILITY_QUAKEJUMP_NAME"
    }

    graphics {
        full_jump_animation jumpsmash
        full_jump_sync_frames 24
        full_jump_windup_frames 26
        
        aoe_spell_on_land true
        delay 5
        animation earthquakeSlam
        particle Earthquake
        visual_delay_but_simultaneous_damage 7
    }

    cost {
        act_points 1
    }
    
    target {
        min_range 1
        max_range 3
        max_aoe 2
        aoe_mode standard
    }

    damage_instance {
        damage 4+bonus_melee_damage
        knockback 1

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `BrambleBabyEntangle`
**Source:** `special_enemy_abilities.gon`  

```
BrambleBabyEntangle {
    template spell

    graphics {
        animation entangle
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
            Tangled 1
            BramblesOnHit 1
        }

        elements [
            Grass
        ]

        ai_base_score 999
    }
}
```

---

### `BramblePull`
**Source:** `special_enemy_abilities.gon`  

```
BramblePull {
    template straightshot_attack
    
    cost {
        mana 0
        cantrip true
    }

    target {
        max_range 10

        knockback_mode pull_to_character
    }

    graphics {
        animation shoot

        projectile Bramblehook
        chain_movieclip Bramblechain
        chain_distance .38
    }
    
    damage_instance {
        damage 3+bonus_ranged_damage
    }
}
```

---

### `HemBounce`
**Source:** `special_enemy_abilities.gon`  

```
HemBounce {
    template melee_attack

    graphics {
        animation bounce
        dont_orient true
    }

    target {
        target_mode none
        aoe_mode cross
        knockback_mode character_to_tile
    }

    damage_instance {
        damage 0
        type melee
        knockback 3
        makes_contact true
    }
}
```

---

### `HemDeathPop`
**Source:** `special_enemy_abilities.gon`  

```
HemDeathPop {
    template lobbed_attack

    graphics {
        animation dying
        projectile HemlockFetus
        dont_orient true
    }

    target {
        target_mode random_closest_tile
        recalc_target_on_castpoint true
        
        min_range 1
        max_range 20
        restrictions [must_have_enemy must_have_living_character]
    }

    damage_instance {
        effects {
            Possessed 1
            Poison 1
        }
    }
}
```

---

### `HemShot`
**Source:** `special_enemy_abilities.gon`  

```
HemShot {
    template lobbed_attack

    graphics {
        animation shoot
        dont_orient true
    }

    target {
        min_range 1
        max_range 3
        restrictions [must_have_enemy must_have_living_character]
    }

    damage_instance {
        damage 1+bonus_ranged_damage
        effects {
            Poison 1
        }
    }
}
```

---

### `HemHeal`
**Name:** Healing Gas  
**Source:** `special_enemy_abilities.gon`  

```
HemHeal {
    template melee_attack
    
    meta {
        name "EABILITY_HEALINGGAS_NAME"
    }

    graphics {
        animation heal
    }
    
    cost {
        mana 5
    }
    
    target {
        target_mode none
        aoe_mode cross
        knockback_mode character_to_tile
        multihit 3
    }
    
    damage_instance {
        heal 1+bonus_basic_spell_damage
        type spell
        makes_contact false
    }
}
```

---

### `ThornUp`
**Name:** Thorn Up  
**Source:** `special_enemy_abilities.gon`  

```
ThornUp {
    template self_buff
    
    meta {
        name "EABILITY_THORNUP_NAME"
    }

    graphics {
        animation spikes
    }
    
    damage_instance {
        effects {
            Thorns 1
            //KineticSpikes 1
            RandomMagicMissile 1
        }
    }
}
```

---

### `BirthwortReactionShot`
**Name:** Shot  
**Source:** `special_enemy_abilities.gon`  

```
BirthwortReactionShot {
    template straightshot_attack

    meta {
        name "EABILITY_SHOT_NAME"
    }

    graphics {

    }

    target {
        aoe_mode custom
        custom_aoe [[0, 1] [0,-1]]
    }

    damage_instance {
        damage 3+bonus_ranged_damage
        
        effects {
            Rot 1
        }
    }
}
```

---

### `BirthwortTrample`
**Name:** Trample Dash  
**Source:** `special_enemy_abilities.gon`  

```
BirthwortTrample {
    template trample_dash
    
    meta {
        name "EABILITY_TRAMPLEDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend

        speed .5
    }

    cost {
        cantrip true
    }
    
    target {
        max_range 3
    }
    
    temporary_effects {
        Trample 3
    }

    damage_instance {
        damage 3+bonus_melee_damage
    }
}
```

---

### `BirthwortHeal`
**Source:** `special_enemy_abilities.gon`  

```
BirthwortHeal {
    template spell

    graphics {
        animation heal
        particle none
        dont_orient true
    }

    cost {
        cantrip true
    }

    target {
        target_mode none
        aoe_excludes_self false
    }

    damage_instance {
        heal 2

        elements [
            Grass
        ]

    }
}
```

---

### `PickupRock`
**Source:** `special_enemy_abilities.gon`  

```
PickupRock {
    variant_of BasicMelee
    class PlaceholderMeleeAttackAbility

    graphics {
        animation hide
        do_not_clear_placeholder true
    }

    cost {
        mana 0
        must_not_be_consuming true
        cantrip true
    }

    target { 
        target_mode tile
        min_range 0
        max_range 1
        
        min_aoe 0
        max_aoe 0

        restrictions [must_have_tag]
        target_requires_tag rock
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                instant true
                use_placeholder true
                drop_on_death deferred
                struggle_ability Thrash
            }
            ApplyShieldToApplierBasedOnMaxHealth 1
        }
        ai_base_score 99999
    }
}
```

---

### `AmoebaRockBash`
**Source:** `special_enemy_abilities.gon`  

```
AmoebaRockBash {
    template melee_attack

    graphics {
        animation bash
    }

    target {
        X_is custom
    }
    bonus_passives {
        XIsConsumedCharacterMaxHP 3
    }

    damage_instance {
        damage X+bonus_melee_damage

        effects {
            CollideWithConsumed 4+bonus_melee_damage
        }
    }
}
```

---

### `AmoebaAttach`
**Source:** `special_enemy_abilities.gon`  

```
AmoebaAttach {
    template tile_targeted_melee_attack

    graphics {
        animation attach
    }

    self_damage {
        damage 0
        type melee

        effects {
            Vaporize 1
        }
    }

    target {
        restrictions must_have_cat
    }

    damage_instance {
        damage 0
        force_play_hit_animation true

        effects {
            DestroyEquipmentAndAttachParasite {
                pool [AmoebaHat AmoebaNeck AmoebaFace]
            }
            GenericDebuff 100 //for AI
        }
    }
}
```

---

### `TrembloSuck`
**Name:** Suck  
**Source:** `special_enemy_abilities.gon`  

```
TrembloSuck {
    template targeted_status

    meta {
        name "EABILITY_SUCK_NAME"
    }

    graphics {
        animation suck
        projectile None
    }

    cost {
        mana 0
        must_not_be_consuming true
        cantrip true
    }

    target {
        max_range 10
        range_mode cross
        knockback_mode none
        restrictions [must_have_tag]
        target_requires_tag rock
        knockback_mode pull_to_character
    }

    damage_instance {
        damage 0
        cant_miss true

        effects {
            TempTrampleUntilSettled 3
            BypassRockKnockback 1
        }

        elements [
            Wind
        ]
    }
}
```

---

### `TrembloEat`
**Source:** `special_enemy_abilities.gon`  

```
TrembloEat {
    template targeted_status
    class MeleeEatAbility

    graphics {
        animation chewing
    }

    cost {
        cantrip true
    }

    target { 
        max_range 1
        restrictions [must_have_tag]
        target_requires_tag rock
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true
        ai_base_score 99

        effects {
            Vaporize 20
            ApplyToSource {
                Brace 1
                Shield 1
            }
        }
    }
}
```

---

### `TrembloSmash_AI`
**Source:** `special_enemy_abilities.gon`  

```
TrembloSmash_AI {
    template tile_targeted_melee_attack

    graphics {
        animation attack
    }

    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[0, 0]]
    }

    damage_instance {
        damage 4+bonus_melee_damage
        knockback 1

        effects {
            Stun 1
        }

        elements [
            Earth
        ]
    }
}
```

---

### `TrembloSmash`
**Source:** `special_enemy_abilities.gon`  

```
TrembloSmash {
    template tile_targeted_melee_attack
    ai_ability TrembloSmash_AI

    graphics {
        animation attack
    }

    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[0, -1] [0, 0] [0, 1]]
    }

    damage_instance {
        damage 4+bonus_melee_damage
        knockback 1

        effects {
            Stun 1
        }

        elements [
            Earth
        ]
    }
    splash_damage {
        damage 0
        knockback 1

        effects {
            SendRock 1
        }
    }
}
```

---

### `CraterCreeperGush`
**Source:** `special_enemy_abilities.gon`  

```
CraterCreeperGush {
    template melee_attack

    graphics {
        animation shoot
        detatched_animation WaterGush
        detatched_animation_reach 20
        detatched_animation_cutoff true
    }

    cost {
        mana 0
    }

    target {
        max_aoe 10
        aoe_restrictions must_have_piercing_line_of_sight
    }

    damage_instance {
        type spell
        damage 1
        knockback 1

        effects {
            Poison 1
        }

        elements [
            Water
        ]
    }
}
```

---

### `CraterCreeperRockBlast`
**Source:** `special_enemy_abilities.gon`  

```
CraterCreeperRockBlast {
    template melee_attack
    ai_ability RockBlast_AI

    graphics {
        animation shoot
    }

    cost {
        mana 0
    }

    target {
        aoe_restrictions must_be_empty
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 0
        type melee
        incidentally_collects_pickups false

        effects {
            SendRock 1
        }

        elements [
        ]
    }
}
```

---

### `CraterCreeperSlide`
**Name:** Slide  
**Source:** `special_enemy_abilities.gon`  

```
CraterCreeperSlide {
    template trample_dash
    
    meta {
        name "EABILITY_SLIDE_NAME"
    }

    cost {
        mana 0
    }

    graphics {
        dash_start_animation launchStart
        dash_animation launchMid
        dash_end_animation launchStop
    }

    temporary_effects {
        Trample 3
        LeaveBehind {
            object Amoeba
        }
    }

    target {
        max_range 6
    }

    damage_instance {
        damage 3+bonus_melee_damage
        ai_base_score 9999
    }
}
```

---

### `ShortCreepshotCrater`
**Source:** `special_enemy_abilities.gon`  

```
ShortCreepshotCrater {
    template lobbed_attack

    target {
        min_range 1
        max_range 2
    }

    damage_instance {
        damage 4+bonus_ranged_damage
        
        effects {
            SpawnCreep 1
            BounceObject Amoeba
        }
    }
}
```

---

### `AlienBeastGoop`
**Source:** `special_enemy_abilities.gon`  

```
AlienBeastGoop {
    template straightshot_attack

    graphics {
        projectile LobbedProjectile
        animation spit
    }

    target {
        aoe_mode custom
        custom_aoe      [[0,  1], [0, 1], [0, 1],    [0,  -1], [0, -1], [0, -1]]
        custom_aoe_util [[-1, 1], [0, 1], [1, 1],    [-1, -1], [0, -1], [1, -1]]
    }

    self_damage {
        effects {
            IncAuxCounterCycle {
                change 1
                max 3
            }
        }
    }

    damage_instance {
        damage 4+bonus_ranged_damage

        effects {
            Poison 1
        }
    }
}
```

---

### `AlienBeastOpenEyes`
**Source:** `special_enemy_abilities.gon`  

```
AlienBeastOpenEyes {
    template self_buff

    cost {
        cantrip true
    }

    graphics {
        animation none
    }

    damage_instance {
        ai_base_score 999999
        effects {
            RandomStatusFromPool {
                IncAuxCounterClamped {
                    change -1
                    max 3
                }
                IncAuxCounterClamped {
                    change -2
                    max 3
                }
                IncAuxCounterClamped {
                    change -3
                    max 3
                }
            }
        }
    }
}
```

---

### `AlienBeastWideSwipe`
**Source:** `special_enemy_abilities.gon`  

```
AlienBeastWideSwipe {
    template melee_attack

    graphics {
        animation attack
    }

    cost {
        //requires_exact_character_aux 1
    }
    
    target {
        aoe_mode custom
        custom_aoe [ [1, 0], [0, -1], [0, 1], [1, 1], [1, -1] ]
        aoe_leading_edge_only true
        aoe_considers_character_size true
    }
}
```

---

### `AlienBeastEat`
**Name:** Consume!  
**Source:** `special_enemy_abilities.gon`  

```
AlienBeastEat {
    template melee_attack

    meta {
        name "EABILITY_CONSUME_NAME"
    }

    graphics {
        animation eat
    }

    cost {
        requires_exact_character_aux 1
    }
    
    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[2, 0]]
        aoe_considers_character_size false
        prioritize_dont_change_direction true
    }

    damage_instance {
        damage 99999
        cant_miss true
        ai_base_score 999999

        effects {
            Vaporize 1
            VaporizeInanimate 1
        }
    }
}
```

---

### `AlienBeastPuke`
**Name:** Pukewave  
**Source:** `special_enemy_abilities.gon`  

```
AlienBeastPuke {
    template lobbed_attack

    meta {
        name "EABILITY_PUKEWAVE_NAME"
    }

    graphics {
        animation puke
        dont_visualize_ai true
    }

    cost {
        requires_exact_character_aux 2
    }

    target {
        target_mode none
        aoe_mode custom
        aoe_symmetry eight_way

        custom_aoe [ [1 1] [2 2] [3 3] [4 4] [5 5] [6 6] [7 7] [8 8] [9 9]
                     [0 1] [1 2] [2 3] [3 4] [4 5] [5 6] [6 7] [7 8] [8 9] [9 9] ]

        aoe_excludes_self true
        aoe_considers_character_size false
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 5+bonus_ranged_damage
        ai_base_score 999999

        effects {
            Poison 1
            SpawnCreep 1
        }
    }
}
```

---

### `AlienBeastScream`
**Name:** Crater Howl!  
**Source:** `special_enemy_abilities.gon`  

```
AlienBeastScream {
    template spell

    meta {
        name "EABILITY_CRATERHOWL_NAME"
    }

    graphics {
        particle none
        animation howl
        dont_visualize_ai true
    }
    
    cost {
        requires_exact_character_aux 0
    }
    
    target {
        target_mode none
        aoe_mode all
        prioritize_dont_change_direction true
        aoe_excludes_self true
    }

    damage_instance {
        damage 10
        ai_base_score 999999

        effects {
            Stun [1 .5]
            Immobile [1 .5]
        }
    }
}
```

---

### `AlienBeastRampage`
**Name:** Rampage!  
**Source:** `special_enemy_abilities.gon`  

```
AlienBeastRampage {
    template trample_dash
    class BounceDashAbility

    meta {
        name "EABILITY_RAMPAGE_NAME"
    }
    
    graphics {
        dash_start_animation none
        dash_animation rampage
        dash_end_animation none
        speed .5
        dont_visualize_ai true
    }

    cost {
        requires_exact_character_aux 3
    }
    
    target {
        target_mode direction
        max_range 16
        max_bounces 3
        restrictions aoe_must_exist
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 3+bonus_melee_damage
        ai_base_score 999999

        effects {
            Immobile [1 .5]
        }
    }
}
```

---

### `AlienBeastMoveOne`
**Source:** `special_enemy_abilities.gon`  

```
AlienBeastMoveOne {
    variant_of MoveOne

    cost {
        requires_exact_character_aux 2
    }
}
```

---

### `CoreFreakFury`
**Name:** Fury  
**Source:** `special_enemy_abilities.gon`  

```
CoreFreakFury {
    template melee_attack
    
    meta {
        name "EABILITY_FURY_NAME"
    }

    graphics {
        animation fury
    }

    cost {
        cantrip true
    }
    
    target {
        multihit 3
    }
    
    damage_instance {
        damage 3+bonus_melee_damage
    }
}
```

---

### `CoreFreakAttack`
**Source:** `special_enemy_abilities.gon`  

```
CoreFreakAttack {
    template melee_attack
    
    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            Stun 1
        }
    }
}
```

---

### `PokerAttack`
**Source:** `special_enemy_abilities.gon`  

```
PokerAttack {
    template melee_attack
    
    damage_instance {
        damage 4+bonus_melee_damage

        effects {
            Immobile 1
            RefreshMovePointsIfHit 1
        }
    }
}
```

---

### `PokerPokeCat`
**Name:** Hot Poke  
**Source:** `special_enemy_abilities.gon`  

```
PokerPokeCat {
    template melee_attack

    meta {
        name "EABILITY_HOTPOKE_NAME"
    }

    graphics {
        animation poke
    }

    cost {
        cantrip true
    }
    
    damage_instance {
        damage 1+bonus_melee_damage
        knockback 10

        effects {
            Burn 1
            KnockbackDirectionIsFacingDirection 1
        }

        elements [
            Fire
        ]
    }
}
```

---

### `PokerPokeAlly`
**Name:** Hot Poke  
**Source:** `special_enemy_abilities.gon`  

```
PokerPokeAlly {
    template tile_targeted_melee_attack

    meta {
        name "EABILITY_HOTPOKE_NAME"
    }

    graphics {
        animation poke
    }

    target {
        restrictions [must_not_have_tag must_have_ally]
        target_requires_tag poker
    }

    cost {
        cantrip true
    }
    
    damage_instance {
        damage 1+bonus_melee_damage
        ai_base_score 99999

        effects {
            Burn 1
            TakeExtraTurn 1
        }

        //PURPOSELY NOT FIRE ELEMENT because the fire-immune enemies would not receive the buffs from this if it was (adding Burn should keep the elemental effect here for the non-immune enemies)
    }
}
```

---

### `WhispererThrowDamage`
**Name:** Tumor Throw  
**Source:** `special_enemy_abilities.gon`  

```
WhispererThrowDamage {
    template lobbed_attack

    meta {
        name "EABILITY_TUMORTHROW_NAME"
    }

    graphics {
        animation shoot
    }

    target {
        min_range 1
        max_range 3
    }

    damage_instance {
        damage 1+bonus_ranged_damage

        effects {
            SpeedUp -2
            Bruise 2
        }
    }
}
```

---

### `WhispererThrowBuff`
**Name:** Tumor Throw  
**Source:** `special_enemy_abilities.gon`  

```
WhispererThrowBuff {
    template lobbed_attack

    meta {
        name "EABILITY_TUMORTHROW_NAME"
    }

    graphics {
        animation shoot
    }

    target {
        min_range 1
        max_range 3
    }

    damage_instance {
        heal 1+bonus_ranged_damage

        effects {
            SpeedUp 2
            Brace 2
        }
    }
}
```

---

### `WhispererWhisper`
**Name:** Whisper  
**Source:** `special_enemy_abilities.gon`  

```
WhispererWhisper {
    template tile_targeted_melee_attack
    class PlaceholderMeleeAttackAbility

    meta {
        name "EABILITY_WHISPER_NAME"
    }

    graphics {
        animation whisper
    }

    target {
        knockback_mode tile_to_character
        restrictions must_have_character
    }

    damage_instance {
        damage 0
        effects {
            Charmed 1
        }
    }
}
```

---

### `TwistingFlames`
**Name:** Twisting Flames  
**Source:** `special_enemy_abilities.gon`  

```
TwistingFlames {
    template spell

    meta {
        name "EABILITY_TWISTINGFLAMES_NAME"
    }

    graphics {
        particle FireSpin
        palette 6
        animation flames
    }
    
    cost {
        prime 1
    }
    
    target {
        min_range 3
        max_range 4
        min_aoe 0
        max_aoe 2
    }
    
    damage_instance {
        damage 4
        
        effects {
            ContextualHeal 1
            Conditional_Enemy {
                Burn 3
            }
            Conditional_Ally {
                DamageUp 1
            }
        }
        
        elements [
            Fire
        ]
    }
}
```

---

### `CloakerHex`
**Source:** `special_enemy_abilities.gon`  

```
CloakerHex {
    template targeted_status

    target {
        max_range 20
    }

    graphics {
        animation counter
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Hex 1
        }
    }
}
```

---

### `NeckSnap`
**Source:** `special_enemy_abilities.gon`  

```
NeckSnap {
    template tile_targeted_melee_attack
    class PlaceholderMeleeAttackAbility

    graphics {
        animation necksnap
    }

    target {
        knockback_mode tile_to_character
        restrictions must_have_character
    }

    damage_instance {
        damage 0
        effects {
            Conditional_Speculative {
                Conditional_HealthThreshold {
                    threshold_percent 50%
                    DieViolently 1
                }
            } Else {
                DieViolently 1
            }
        }
    }
}
```

---

### `DemonUppercut`
**Source:** `special_enemy_abilities.gon`  

```
DemonUppercut {
    template melee_attack

    graphics {
        animation attack
    }

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            KnockUpAndAway {
                stacks 3
                distance 3
            }
        }
    }
}
```

---

### `DemonRockThrow`
**Source:** `special_enemy_abilities.gon`  

```
DemonRockThrow {
    template lobbed_attack

    graphics {
        projectile SmallRock
        animation shoot
    }
    
    target {
        max_range 20
    }
    
    damage_instance {
        damage 3+bonus_ranged_damage

        effects {
            Stun [1, .2]
            BounceObject SmallRock

            Conditional_Speculative {
                BonusDamageBasedOnDistance 1
            }
        }

        elements [
            Rock
        ]
    }
}
```

---

### `TumorDash`
**Name:** Tumor Dash  
**Source:** `special_enemy_abilities.gon`  

```
TumorDash {
    template trample_dash
    
    meta {
        name "EABILITY_TUMORDASH_NAME"
    }
    
    graphics {
        dash_animation dash
        speed .5
    }
    
    cost {
        mana 5
    }
    
    target {
        max_range mov
        allow_any_orientation true
    }
    
    damage_instance {
        damage 6+bonus_melee_damage

        effects {
            Bruise 1
            Immobile 1
        }
    }
}
```

---

### `TumorPowerup`
**Source:** `special_enemy_abilities.gon`  

```
TumorPowerup {
    template self_buff

    graphics {
        animation powerup
    }
    
    cost {
        cantrip true
    }
    
    damage_instance {
        effects {
            Cleanse 1
            MovementUp 1
        }
    }
}
```

---

### `HeadTumorAttack`
**Source:** `special_enemy_abilities.gon`  

```
HeadTumorAttack {
    template melee_attack

    damage_instance {
        damage 2+bonus_melee_damage
        knockback 3
    }
}
```

---

### `HeadTumorResponse`
**Source:** `special_enemy_abilities.gon`  

```
HeadTumorResponse {
    template melee_spell

    graphics {
        animation fart
        particle fx_windSpell
    }

    target {
        aoe_mode custom
        custom_aoe [[-1 0]]
        knockback_mode back_orientation
    }

    self_damage {
        knockback -2
    }

    damage_instance {
        type spell
        damage 0
        knockback 3

        elements [
            Wind
        ]
    }
}
```

---

### `DH_MeatHook`
**Source:** `special_enemy_abilities.gon`  

```
DH_MeatHook {
    template straightshot_attack

    target {
        max_range 10

        knockback_mode pull_to_character
    }

    cost {
        cantrip true
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
            Conditional_Speculative {
                BonusDamageBasedOnDistance 1
                BonusDamage -1
                CapDamage 1
            }
        }
    }
}
```

---

### `DH_Attack`
**Source:** `special_enemy_abilities.gon`  

```
DH_Attack {
    template melee_attack

    damage_instance {
        damage 4+bonus_melee_damage
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

### `BelcherLavashot`
**Name:** Spit Lava  
**Source:** `special_enemy_abilities.gon`  

```
BelcherLavashot {
    template lobbed_attack

    meta {
        name "EABILITY_SPITLAVA_NAME"
    }
	
    graphics {
        projectile LavaBall
    }
	
    cost {
        mana 0
    }
    
    target {
        min_range 1
        max_range 2
    }

    damage_instance {
        damage 2+bonus_ranged_damage

        effects {
            Burn 2

            ChangeTile {
                tile LavaTile
            }
        }

        elements [
            Fire
        ]

        custom_additional_ai_weight tile_close_to_enemy
    }
}
```

---

### `TC_DashReaction_AI`
**Source:** `special_enemy_abilities.gon`  

```
TC_DashReaction_AI {
    template melee_attack

    target { 
        aoe_considers_character_size true
        aoe_mode cone
        max_aoe 20
        min_aoe 2
        aoe_leading_edge_only true

        //custom_aoe [[2, 1] [3, 1] [2, 0] [3, 0]] //thinks he can hit the full 2x2
    }

    damage_instance {
        contact_requires_adjacency false
    }
}
```

---

### `TC_DashReaction`
**Source:** `special_enemy_abilities.gon`  

```
TC_DashReaction {
    template trample_dash
    ai_ability TC_DashReaction_AI

    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
    }

    temporary_effects {
        Trample 3
    }
    
    damage_instance {
        damage 3+bonus_melee_damage
    }
}
```

---

### `TC_Attack`
**Source:** `special_enemy_abilities.gon`  

```
TC_Attack {
    template melee_attack

    damage_instance {
        damage 4+bonus_melee_damage
        knockback 3
        effects {
            Bruise 1
        }
    }
}
```

---

### `TT_Thrash`
**Source:** `special_enemy_abilities.gon`  

```
TT_Thrash {
    template melee_attack
    
    graphics {
        animation thrash
    }

    
    target {
        aoe_mode square
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 4+bonus_melee_damage
        knockback 1
    }
}
```

---

### `TT_ManaBurn`
**Source:** `special_enemy_abilities.gon`  

```
TT_ManaBurn {
    template spell

    target {
        max_range 20
        max_aoe 0
    }

    graphics {
        animation curse
        particle MagicMissleBlast
    }

    damage_instance {
        damage 0

        effects {
            BonusDamageBasedOnMana 1
            ManaStealToHealth -1
        }
    }
}
```

---

### `BigAsteroidBarrage`
**Source:** `special_enemy_abilities.gon`  

```
BigAsteroidBarrage {
    template lobbed_attack

    graphics {
        animation puke
        lob_height 2
        projectile Boulder
    }
    
    /*target {
        target_mode direction
        aoe_excludes_self true
        aoe_considers_character_size true
        aoe_mode line
        max_aoe 1 //+2 from low gravity boost
        min_aoe 1

        multihit 3
        stagger_multihit_targets true
        multihit_target_distance_sort true
    }*/
    target {
        range_mode cross
        max_range 1 //+2 from low gravity boost
        knockback_mode zero //should prevent the AI from trying to use this for knockback
    }
    
    damage_instance {
        damage 4+bonus_ranged_damage

        effects {
            BounceObject Boulder
            TwisterDisplaceWithDamage {
                damage 1
                max_dist 2 //boost to 4 with low grav
            }

        }
    }
}
```

---

### `SmallAsteroidBarrage`
**Source:** `special_enemy_abilities.gon`  

```
SmallAsteroidBarrage {
    template lobbed_attack

    graphics {
        animation puke
        lob_height 2
        projectile SmallRock
    }
    
    target {
        aoe_excludes_self true
        aoe_considers_character_size true

        max_aoe 2
        min_aoe 0

        min_range 0
        max_range 1 //boost to 3 with low grav

        max_targets 3

        multihit 3
        stagger_multihit_targets true
        knockback_mode zero //should prevent the AI from trying to use this for knockback
    }
    
    damage_instance {
        damage 4+bonus_ranged_damage

        effects {
            BounceObject SmallRock
            TwisterDisplaceWithDamage {
                damage 1
                max_dist 2 //boost to 4 with low grav
            }
        }
    }
}
```

---

### `UFO_SpelunkyDeath`
**Source:** `special_enemy_abilities.gon`  

```
UFO_SpelunkyDeath {
    template jump_attack

    graphics {
        jump_attack_animation land
    }
    
    target {
        target_mode random_tile

        min_range 0
        max_range 1 //buffed to 2 via low gravity

        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
    }

    

    damage_instance {
        damage 0
        type none

        effects {
            HitExplosion 5
        }
    }
}
```

---

### `UFO_CrossLasers`
**Name:** Zorp  
**Source:** `special_enemy_abilities.gon`  

```
UFO_CrossLasers {
    template straightshot_attack

    meta {
        name "EABILITY_ZORP_NAME"
    }

    graphics {
        particle MagicMissleBlast
        animation attack
        projectile MagicMissileProjectile
        lob_height 0
        speed 20
    }
    
    target {
        target_mode none

        aoe_mode custom
        aoe_symmetry four_way
        custom_aoe [[1, 1]]

        upgrade_straight_shot_to_piercing true
    }
    
    damage_instance {
        damage 2+bonus_basic_spell_damage
    }
}
```

---

### `UFO_Detect`
**Name:** Detect  
**Source:** `special_enemy_abilities.gon`  

```
UFO_Detect {
    template targeted_status

    meta {
        name "EABILITY_DETECT_NAME"
    }

    graphics {
        particle none
        animation identify
    }
    
    target {
        target_mode none
        max_aoe 3
        aoe_excludes_self true
    }
    
    damage_instance {
        effects {
            Conditional_Enemy {
                Marked 1
            }
        }
    }
}
```

---

### `UFO_Shield`
**Name:** Shields Up  
**Source:** `special_enemy_abilities.gon`  

```
UFO_Shield {
    template self_buff

    meta {
        name "EABILITY_SHEILDSUP_NAME"
    }

    graphics {
        animation shield
    }
    
    damage_instance {
        effects {
            DivineShield 1
        }
    }
}
```

---

### `UFO_Megalaser`
**Name:** Annihilaser  
**Source:** `special_enemy_abilities.gon`  

```
UFO_Megalaser {
    template spell

    meta {
        name "EABILITY_ANNIHILASER_NAME"
    }

    cost {
        prime 1
        act_points 1
    }

    graphics {
        particle MagicMissleBlast
        animation laserShoot
    }
    
    target {
        target_mode direction
        aoe_mode line
        aoe_considers_character_size true
        max_aoe 10
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0

        effects {
            Conditional_Boss {
                OverrideDamage 25
            } Else {
                Vaporize 1
            }
        }
    }
}
```

---

### `UFO_Dash`
**Name:** M-Dash  
**Source:** `special_enemy_abilities.gon`  

```
UFO_Dash {
    template trample_dash
    
    meta {
        name "EABILITY_MDASH_NAME"
    }

    cost {
        act_points 1
    }
    
    graphics {
        dash_start_animation ramStart
        dash_animation ramLoop
        dash_end_animation ramEnd
    }

    target {

    }
    
    damage_instance {
        damage 4+bonus_melee_damage

        effects {
            Stun 1
        }
    }
}
```

---

### `UFO_Summon`
**Name:** Beam In  
**Source:** `special_enemy_abilities.gon`  

```
UFO_Summon {
    template spawn

    meta {
        name "EABILITY_BEAMIN_NAME"
    }

    cost {
        act_points 1
    }
    
    graphics {
        lob false
        animation spawn
    }

    target {
        max_range 5
    }

    spawn {
        object GreenProber
        ai_base_score 9999
        spawnin_animation summonspawnin
        faction self
    }
}
```

---

### `UFO_BigShield`
**Name:** M-Shield  
**Source:** `special_enemy_abilities.gon`  

```
UFO_BigShield {
    template self_buff

    meta {
        name "EABILITY_MSHEILD_NAME"
    }

    cost {
        act_points 1
    }

    graphics {
        animation shield
    }
    
    damage_instance {
        effects {
            DivineShield 2
        }
    }
}
```

---

### `UFO_BigExplode`
**Source:** `special_enemy_abilities.gon`  

```
UFO_BigExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation dying
    }

    target {
        knockback_mode character_to_tile
        aoe_considers_character_size true
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 2
    }

    damage_instance {
        damage 7
        knockback 1

        effects {
            IgnoreSelf true
        }

        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `YA_Laser`
**Source:** `special_enemy_abilities.gon`  

```
YA_Laser {
    template laser

    graphics {
        use_projectile_spawn_offset true
        animation shoot
        visual_delay_but_simultaneous_damage 0
		
		beam_clip greenlaser
        beam_cap greenlasercap
    }
    
    target {
        target_mode direction
        aoe_mode line
        max_aoe 10
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 1+bonus_basic_spell_damage
    }
}
```

---

### `YA_Charge`
**Source:** `special_enemy_abilities.gon`  

```
YA_Charge {
    template self_buff

    graphics {
        animation charge
    }

    cost {
        cantrip true
    }
    
    damage_instance {
        effects {
            DamageUp 1
        }
    }
}
```

---

### `YA_Jetpack`
**Source:** `special_enemy_abilities.gon`  

```
YA_Jetpack {
    template move

    graphics {
        move_start_animation jetbegin
        animation jetloop
        move_end_animation jetend
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 3
        max_range 4
        straight_shot true
        as_the_crow_flies true
        range_mode normal
    }
}
```

---

### `GA_Telekinesis`
**Source:** `special_enemy_abilities.gon`  

```
GA_Telekinesis {
    template spell

    graphics {
        particle MagicMissleBlast
        animation shoot
    }
    
    target {
        max_aoe 0
        max_range 20
        knockback_mode character_to_target
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 1+bonus_basic_spell_damage
        knockback 3
    }
}
```

---

### `GA_Telekinesis_Big`
**Source:** `special_enemy_abilities.gon`  

```
GA_Telekinesis_Big {
    template spell

    graphics {
        particle MagicMissleBlast
        animation shoot
    }
    
    target {
        max_aoe 0
        max_range 20
        knockback_mode character_to_target
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 1+bonus_basic_spell_damage
        knockback 20

        effects {
            Confusion 1
        }
    }
}
```

---

### `GA_Counterspell`
**Name:** Counterspell  
**Source:** `special_enemy_abilities.gon`  

```
GA_Counterspell {
    template self_buff
    
    meta {
        name "EABILITY_COUNTERSPELL_NAME"
    }

    graphics {
        animation prime
    }
    
    cost {
        cantrip true
    }
    
    damage_instance {
        effects {
            Counterspell 1
            EndTurn 1
        }
    }
}
```

---

### `GA_Megablast`
**Name:** Prime Blast  
**Source:** `special_enemy_abilities.gon`  

```
GA_Megablast {
    template spell
    
    meta {
        name "EABILITY_PRIMEBLAST_NAME"
    }

    graphics {
        animation megablast
        particle none
    }

    target {
        target_mode none
        aoe_mode circle
        min_aoe 0
        max_aoe 20
        aoe_excludes_self true
        aoe_considers_character_size true
        aoe_restrictions [enemies_only]
    }
    
    damage_instance {
        damage 2+bonus_basic_spell_damage
        knockback 10

        effects {
            Confusion 1
        }

        ai_base_score 999999
    }
}
```

---

### `GA_Suggest`
**Source:** `special_enemy_abilities.gon`  

```
GA_Suggest {
    template targeted_status

    target {
        max_range 20
    }

    cost {
        cantrip true
    }

    graphics {
        animation suggest
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            TakeExtraTurn 1
        }
    }
}
```

---

### `GA_PrimeExplode`
**Source:** `special_enemy_abilities.gon`  

```
GA_PrimeExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle MagicMissleBlast
        animation dying
    }

    target {
        knockback_mode character_to_tile
        aoe_considers_character_size true
        aoe_mode circle
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 1
    }

    damage_instance {
        damage 7
        knockback 1

        effects {
            IgnoreSelf true
        }

        elements [
            Explosion
        ]
    }
}
```

---

### `GP_Probe`
**Source:** `special_enemy_abilities.gon`  

```
GP_Probe {
    template melee_attack

    graphics {
        animation probe
    }

    target {
        restrictions [aoe_must_exist]
        aoe_restrictions [must_backstab must_have_cat]
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        force_play_hit_animation true

        effects {
            ProbeCharmed 1
        }

        custom_additional_ai_weight avoid_redundant_debuffs_strict
    }
}
```

---

### `MoonWormShot`
**Source:** `special_enemy_abilities.gon`  

```
MoonWormShot {
    template lobbed_attack
    class MultiTargetRangedAttackAbility

    target {
        target_mode none
        min_aoe 1
        max_aoe 1 //boosted to 3 via low grav
        aoe_restrictions [enemies_only]
    }

    damage_instance {
        damage 2+bonus_ranged_damage
    }
}
```

---

### `MoonWormCurl`
**Source:** `special_enemy_abilities.gon`  

```
MoonWormCurl {
    template self_buff

    graphics {
        animation curlup
    }

    damage_instance {
        effects {
            Brace 1
        }
    }
}
```

---

### `WaggleClone`
**Source:** `special_enemy_abilities.gon`  

```
WaggleClone {
    template lobbed_attack

    target {
        min_range 1
        max_range 3 //boosted to 5 via low gravity
        knockback_mode none
    }

    cost {
        cantrip true
    }

    damage_instance {
        damage 0
        
        effects {
            WaggleClone {
                stacks 5 //will clone onto enemies with 5 or less health as well
                1x1_object cWaggle
                2x2_object cWaggle2x2
                3x3_object cWaggle3x3
            }
        }
    }
}
```

---

### `RoverDash`
**Name:** Chain Dash  
**Source:** `special_enemy_abilities.gon`  

```
RoverDash {
    template dash_attack
    
    meta {
        name "EABILITY_CHAINDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }
    
    cost {
        mana 0
    }
    
    target {

    }

    temporary_effects {
        DashFury 4
    }
    
    damage_instance {
        damage 4+bonus_melee_damage
        knockback 1

        effects {
            ApplyToSource {
                DoDamage {
                    damage 1
                    type generic_physical
                }
            }
        }
    }
}
```

---

### `BHoleSuck`
**Source:** `special_enemy_abilities.gon`  

```
BHoleSuck {
    template spell

    graphics {
        particle none
        animation suck
    }

    target {
        target_mode none
        min_aoe 0
        max_aoe 20
        aoe_excludes_self true
        aoe_considers_character_size true
        knockback_mode tile_to_character
    }
    
    damage_instance {
        damage 0
        knockback 1
        hint_dont_lowgravboost true

        ai_base_score 999999
    }
}
```

---

### `NeutronRumble`
**Source:** `special_enemy_abilities.gon`  

```
NeutronRumble {
    template self_buff

    graphics {
        animation rumble
    }

    //no effects
    damage_instance {
        ai_base_score 999999
    }
}
```

---

### `NeutronExplode`
**Source:** `special_enemy_abilities.gon`  

```
NeutronExplode {
    template spell

    graphics {
        animation explode
        particle MagicMissleBlast
        delay 3
    }
    
    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_line_of_sight
    }

    self_damage {
        effects {
            FormChange {
                form BlackHole
            }
        }
    }
    
    damage_instance {
        damage 10
        ai_base_score 999999

        effects {
            Blind 1
        }
    }
}
```

---

### `HellHandGrab`
**Source:** `special_enemy_abilities.gon`  

```
HellHandGrab {
    template melee_attack

    graphics {
        animation grab
    }

    damage_instance {
        damage 0
        type melee
        cant_miss true

        effects {
            Grappled 1
        }
    }
}
```

---

### `GameteInflate`
**Source:** `special_enemy_abilities.gon`  

```
GameteInflate {
    template self_buff

    graphics { 
        dont_orient true
        animation transform
    }

    damage_instance {
        effects {
            FormChange {
                form "Big"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `GameteSpawn`
**Source:** `special_enemy_abilities.gon`  

```
GameteSpawn {
    template spawn
    
    graphics {
        lob true
        animation birth
    }
    
    cost {
        mana 5
    }
    
    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [ [-1, 0] ]
    }

    self_damage {
        effects {
            FormChange {
                form "Small"
            }
        }
    }

    spawn {
        object RANDOM_SPECIFIC_CHAPTER_ENEMY_MEDIUM
        chapter alley
        ai_base_score 9999
        faction self
    }
}
```

---

### `GametePop`
**Source:** `special_enemy_abilities.gon`  

```
GametePop {
    template spell
    
    graphics { 
        dont_orient true
        particle fx_windSpell
        animation dying
    }

    target {
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 1
        max_aoe 1
    }

    damage_instance {
        damage 1
        knockback 2

        effects {
            IgnoreSelf true
        }

        elements [
            Explosion
            Wind
        ]
    }
}
```

---

### `CHToss`
**Name:** Toss  
**Source:** `special_enemy_abilities.gon`  

```
CHToss {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        animation throw
        use_placeholder true
        face_toss_target true
        dont_visualize_ai true
    }
    
    target {
        max_range 4
        min_range 2
        restrictions none
        range_mode cross
        toss_direction_restriction backwards
    }
    
    damage_instance {
        damage 1+bonus_melee_damage
        custom_additional_ai_weight toss_farthest

        effects {
            RandomInjury 1
        }
    }
}
```

---

### `CHCry`
**Name:** Howl  
**Source:** `special_enemy_abilities.gon`  

```
CHCry {
    template spell
    
    meta {
        name "EABILITY_HOWL_NAME"
    }

    graphics {
        animation cry
		particle none
    }

    target {
        target_mode none
        min_aoe 0
        max_aoe 3
        aoe_excludes_self true
        aoe_considers_character_size true
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Immobile [1, .5]
        }

        ai_base_score 999999
    }
}
```

---

### `CHSpawn`
**Source:** `special_enemy_abilities.gon`  

```
CHSpawn {
    template spawn
    
    graphics {
        lob true
        animation fart
    }
    
    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [ [-1, 0] ]
    }

    spawn {
        object Kitten
        ai_base_score 9999
        faction self
    }
}
```

---

### `HCHumanDie`
**Source:** `special_enemy_abilities.gon`  

```
HCHumanDie {
    template self_buff
    
    graphics { 
        animation humandie
    }

    damage_instance {
        heal 999

        effects {
            FormChange {
                form "HumanDead"
            }
            MovementUp -2
        }
    }
}
```

---

### `HCAttack`
**Source:** `special_enemy_abilities.gon`  

```
HCAttack {
    template melee_attack

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1

        effects {
            Immobile 1
        }
    }
}
```

---

### `HCSpin`
**Source:** `special_enemy_abilities.gon`  

```
HCSpin {
    template melee_attack

    graphics {
        animation attack
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode square
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 5
    }
}
```

---

### `CBShoot`
**Source:** `special_enemy_abilities.gon`  

```
CBShoot {
    template ranged_attack

    graphics {
        projectile Bullet
        animation shoot
        empty_animation empty
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

        max_aoe X-1
        restrictions [aoe_must_exist must_have_line_of_sight]

        X_is enable_if_has_ammo
    }

    self_damage {
        effects {
            Ammo -1
        }
    }

    damage_instance {
        damage 7+bonus_ranged_damage
    }
}
```

---

### `CBShoot_ZodiacStyle`
**Source:** `special_enemy_abilities.gon`  

```
CBShoot_ZodiacStyle {
    template straightshot_attack

    graphics {
        projectile Bullet
        animation shoot
        empty_animation empty
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

        max_targets -X //-1 means no target limit, if no ammo then X is 0
        X_is enable_if_has_ammo
    }

    self_damage {
        effects {
            Ammo -1
        }
    }

    damage_instance {
        damage 7+bonus_ranged_damage
    }
}
```

---

### `CBReload`
**Name:** Reload  
**Source:** `special_enemy_abilities.gon`  

```
CBReload {
    template self_buff
    
    meta {
        name "EABILITY_RELOAD_NAME"
    }

    graphics {
        animation reload
    }
    
    cost {
        cantrip true
    }
    
    damage_instance {
        effects {
            Ammo 1
            FormChange active
        }
        ai_base_score 10
    }
}
```

---

### `DrDGlare`
**Source:** `special_enemy_abilities.gon`  

```
DrDGlare {
    template spell

    graphics {
        animation glare
        particle none
    }

    cost {
        cantrip true
    }

    target {
        target_mode none
        max_aoe 1
        aoe_excludes_self true
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 0
        effects {
            Fear 1
        }
    }
}
```

---

### `DrDRockets_ai`
**Source:** `special_enemy_abilities.gon`  

```
DrDRockets_ai {
    template spell

    target {
        max_aoe 2

        min_range 1
        max_range 3

        max_targets 1
        restrictions none
    }

    damage_instance {
        damage 5
    }
}
```

---

### `DrDRockets`
**Source:** `special_enemy_abilities.gon`  

```
DrDRockets {
    template spell
    ai_ability DrDRockets_ai
    
    graphics {
        animation spell
        particle RocketFromAbove
    }

    cost {
        cantrip true
    }

    target {
        max_aoe 2

        min_range 1
        max_range 3

        max_targets 1
        restrictions none
        can_multihit true
    }

    damage_instance {
        damage 0

        effects {
            HitExplosion 5
        }
    }
}
```

---

### `ParasiteShot`
**Source:** `special_enemy_abilities.gon`  

```
ParasiteShot {
    template lobbed_attack

    target {
        min_range 2
        max_range 3
        restrictions none
    }

    damage_instance {
        effects {
            DestroyEquipmentAndAttachParasite {
                chance .15
                pool parasites
            }
        }
    }
}
```

---

### `StacyCharm`
**Name:** Charm  
**Source:** `special_enemy_abilities.gon`  

```
StacyCharm {
    template melee_attack
    
    meta {
        name "EABILITY_CHARM_NAME"
    }

    graphics {
        animation lickAttack
    }

    damage_instance {
        damage 0
        custom_additional_ai_weight avoid_redundant_debuffs_strict

        effects {
            Charmed 1
        }
    }
}
```

---

### `StacyHeal`
**Source:** `special_enemy_abilities.gon`  

```
StacyHeal {
    template melee_attack
    
    graphics {
        animation lickAttack
    }

    damage_instance {
        heal 5+bonus_melee_damage

        effects {
            AllStatsUp 1
        }
    }
}
```

---

### `CerberubsShotgunReaction`
**Source:** `special_enemy_abilities.gon`  

```
CerberubsShotgunReaction {
    template straightshot_attack

    target {
        max_aoe 3+bonus_range
        shotgun_mode true

        aoe_mode custom
        custom_aoe      [[4, 3], [4, 2], [4, 1], [4, 0], [4, -1], [4, -2]]

        custom_aoe_util [[1, 1], [1, 1], [1, 1], [1, 0], [1,  0], [1,  0]]
    }

    graphics {
        projectile Projectile
        primed_alt_animation "shootPrimed"
    }
    
    damage_instance {
        damage 3+bonus_ranged_damage

        effects {
            Burn 2
            ChangeTile LavaTile
        }
        elements [
            Fire
        ]
    }
}
```

---

### `CerberubsStraightReaction`
**Source:** `special_enemy_abilities.gon`  

```
CerberubsStraightReaction {
    template straightshot_attack

    target {
        max_aoe 5+bonus_range
        //shotgun_mode true

        aoe_mode custom
        custom_aoe      [[1, 0], [1, 0]]

        custom_aoe_util [[1, 1] [1,  0]]
    }

    graphics {
        projectile Projectile
        primed_alt_animation "shootPrimed"
    }
    
    damage_instance {
        damage 3+bonus_ranged_damage

        effects {
            Burn 2
            ChangeTile LavaTile
        }
        elements [
            Fire
        ]
    }
}
```

---

### `CerberubsJump`
**Name:** Cerberub Flub  
**Source:** `special_enemy_abilities.gon`  

```
CerberubsJump {
    template jump_attack
    ai_ability CerberubsJump_AI

    meta {
        name "EABILITY_CERBERUBFLUB_NAME"
    }

    graphics {
        full_jump_animation attack
        full_jump_sync_frames 43
        full_jump_windup_frames 14
    }

    cost {
        act_points 1
    }
    
    target {
        min_range 2
        max_range 2
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `CerberubsJump_AI`
**Source:** `special_enemy_abilities.gon`  

```
CerberubsJump_AI { //jump pretends its targeting like a spawn ability so he can jump towards things while blind sometimes
    template spawn

    target {
        min_range 2
        max_range 2
        aoe_considers_character_size true
        restrictions must_be_moveable
    }

    spawn {
        object SmallRock
    }
}
```

---

### `CerberubsThrow`
**Name:** Maul  
**Source:** `special_enemy_abilities.gon`  

```
CerberubsThrow {
    template throw_attack
    
    meta {
        name "EABILITY_MAUL_NAME"
    }

    graphics {
        animation throw
        use_placeholder true
        face_toss_target true
        dont_visualize_ai true
    }

    cost {
        mana 0
    }

    bonus_passives {
        TossTargetIsAggroTarget 1
    }

    self_damage {
        heal 10
        effects {
            FormChange {
                form "Normal"
            }
        }
        ai_base_score 9999
    }
    
    target {
        max_range 10
        min_range 1
        restrictions none
        range_mode cross
        toss_direction_restriction forwards
    }
    
    damage_instance {
        damage 10+bonus_melee_damage
        custom_additional_ai_weight toss_farthest
    }
}
```

---

### `CerberubsBarrage`
**Source:** `special_enemy_abilities.gon`  

```
CerberubsBarrage {
    template lobbed_attack

    graphics {
        animation shootLava
    }

    
    cost {
        prime 1
    }

    target {
        target_mode direction
        aoe_mode cone
        min_aoe -1
        max_aoe 10
        aoe_considers_character_size true
        restrictions none

        //aoe_chance .33
        max_targets 10
        multihit 5
        stagger_multihit_targets true
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Burn 2
            ChangeTile LavaTile
            HitExplosion 5
        }
        elements [
            Fire
        ]
    }
}
```

---

### `CerberubsCalm`
**Source:** `special_enemy_abilities.gon`  

```
CerberubsCalm {
    template self_buff

    graphics { 
        dont_orient true
        animation none
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            FormChange {
                form "Normal"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `CovenRise1`
**Source:** `special_enemy_abilities.gon`  

```
CovenRise1 {
    template lobbed_attack

    graphics { 
        animation rise
        dont_visualize_ai true
        projectile FireBallProjectile
    }

    target {
        target_mode none
        max_targets 1
        aoe_mode all
        restrictions none
        aoe_restrictions [must_have_tag]
        target_requires_tag unlit_candle
    }

    cost {
        cantrip true
    }

    self_damage {
        effects {
            FormChange {
                form 1
            }
            Brace 1
        }
    }

    damage_instance {
        damage 0
        ai_base_score 999999
        elements [
            Fire
        ]
    }
}
```

---

### `CovenRise2`
**Source:** `special_enemy_abilities.gon`  

```
CovenRise2 {
    variant_of CovenRise1

    self_damage {
        effects {
            FormChange {
                form 2
            }
            Brace 1
        }
    }
}
```

---

### `CovenRise3`
**Source:** `special_enemy_abilities.gon`  

```
CovenRise3 {
    variant_of CovenRise1

    self_damage {
        effects {
            FormChange {
                form 3
            }
            Brace 1
        }
    }
}
```

---

### `CovenRise4`
**Source:** `special_enemy_abilities.gon`  

```
CovenRise4 {
    variant_of CovenRise1

    self_damage {
        effects {
            FormChange {
                form 4
            }
            Brace 1
        }
    }
}
```

---

### `CovenSummon`
**Name:** Death  
**Source:** `special_enemy_abilities.gon`  

```
CovenSummon {
    template self_buff

    meta {
        name "EABILITY_DEATH_NAME"
    }

    graphics { 
        animation summon
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            PopAndSpawn Tormentor
        }
        ai_base_score 9999
    }
}
```

---

### `CovenPestilence`
**Name:** Pestilence  
**Source:** `special_enemy_abilities.gon`  

```
CovenPestilence {
    template spawn

    meta {
        name "EABILITY_PESTILENCE_NAME"
    }
    
    graphics {
        lob true
        animation spell
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        max_targets 4
    }

    spawn {
        object PoisonFrog
        ai_base_score 9999
        first_turn initiative
    }
}
```

---

### `CovenFamine`
**Name:** Famine  
**Source:** `special_enemy_abilities.gon`  

```
CovenFamine {
    template spell

    meta {
        name "EABILITY_FAMINE_NAME"
    }

    graphics {
        particle none
        animation spell
    }
    
    target {
        target_mode none
        aoe_mode square
        aoe_considers_character_size true
        aoe_excludes_self true
        min_aoe 0
        max_aoe 20
    }

    damage_instance {
        damage 0
        ai_base_score 999999

        effects {
            Conditional_Enemy {
                Conditional_FinishedSpawning {
                    Imprison Fly
                }
            }
            EnableWeather VisualFlySwarm
            Conditional_HasTag {
                tag food

                CanApplyToInanimate {
                    Vaporize 1
                    ObjectOnHitCharacter Fly
                }
            }
        }

        ai_base_score 9999
    }
}
```

---

### `CovenWar`
**Name:** War  
**Source:** `special_enemy_abilities.gon`  

```
CovenWar {
    template lobbed_attack

    meta {
        name "EABILITY_WAR_NAME"
    }

    graphics {
        animation spell
    }

    target {
        target_mode none
        aoe_mode square
        aoe_considers_character_size true
        aoe_excludes_self true
        min_aoe 0
        max_aoe 20

        max_targets 20
        //multihit 5
        //stagger_multihit_targets true
    }

    damage_instance {
        ai_base_score 999999
        damage 5+bonus_ranged_damage

        effects {
            Burn 2
            ChangeTile LavaTile
        }
        elements [
            Fire
        ]
    }
}
```

---

### `TormentorMelee`
**Source:** `special_enemy_abilities.gon`  

```
TormentorMelee {
    template melee_attack
}
```

---

### `TormentorBite`
**Name:** Lucifer  
**Source:** `special_enemy_abilities.gon`  

```
TormentorBite {
    template melee_attack

    meta {
        name "EABILITY_LUCIFER_NAME"
    }

    graphics {
        animation bite
    }

    bonus_passives {
        AbilityEnabledIfHasStatus DemonicGlyph_Bite
        AbilityEnabledOncePerRound 1
    }

    damage_instance {
        damage 1+bonus_melee_damage
        type melee

        effects {
            RandomInjury 1
        }
    }
}
```

---

### `TormentorThrow`
**Source:** `special_enemy_abilities.gon`  

```
TormentorThrow {
    template lobbed_attack

    graphics {
        animation throw
    }
    
    target {
        min_range 0
        max_range 2
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            ObjectOnHitEmpty HeadTumor
            Madness 2
        }
    }
}
```

---

### `TormentorThrow_spAI`
**Source:** `special_enemy_abilities.gon`  

```
TormentorThrow_spAI {
    template spawn
    
    target {
        min_range 0
        max_range 2
    }
}
```

---

### `TormentorThrow_sp`
**Source:** `special_enemy_abilities.gon`  

```
TormentorThrow_sp {
    variant_of TormentorThrow
    ai_ability TormentorThrow_spAI
}
```

---

### `TormentorSpawn`
**Name:** Pentagram  
**Source:** `special_enemy_abilities.gon`  

```
TormentorSpawn {
    template spawn

    meta {
        name "EABILITY_PENTAGRAM_NAME"
    }
    
    graphics {
        animation throw
        lob true
    }
    
    target {
        min_range 0
        max_range 2
    }

    bonus_passives {
        AbilityEnabledIfHasStatus DemonicGlyph_Summon
        AbilityEnabledOncePerRound 1
    }

    spawn {
        object HeadTumor
        faction self
    }
}
```

---

### `TormentorSuck`
**Name:** Feast  
**Source:** `special_enemy_abilities.gon`  

```
TormentorSuck {
    template spell

    meta {
        name "EABILITY_FEAST_NAME"
    }
    
    cost {
        prime 1
    }

    graphics {
        animation megabite
        particle none
    }
    
    target {
        target_mode direction

        aoe_considers_character_size true
        aoe_excludes_self true
        aoe_mode cone
        min_aoe -1
        max_aoe 10
    }
    
    damage_instance {
        damage 0
        type status_spell
        custom_additional_ai_weight tile_exists
        ai_base_score 999999

        effects {
            Conditional_HasTag {
                tag kaiju
            } Else {
                Consumed {
                    kill_on_consume true
                    force_contact true
                }

                GenericDebuff 100
            }
        }
    }

    self_damage {
        effects {
            EndTurn 1
        }
    }
}
```

---

### `TormentorRuneAbsorb`
**Name:** Imbue  
**Source:** `special_enemy_abilities.gon`  

```
TormentorRuneAbsorb {
    template spell

    meta {
        name "EABILITY_IMBUE_NAME"
    }
    
    cost {
        prime 1
    }

    graphics {
        animation megabite
        particle none
        dont_visualize_ai true
    }
    
    target {
        target_mode none
        prioritize_face_camera true
        prioritize_dont_change_direction true
        aoe_mode all
    }
    
    damage_instance {
        damage 0
        type status_spell
        ai_base_score 999999
        cant_miss true

        effects {
            StealDemonicGlyph 1
        }
    }
}
```

---

### `AZ_Jump`
**Source:** `special_enemy_abilities.gon`  

```
AZ_Jump {
    template jump_attack
    ai_ability AZ_Jump_AI

    graphics {
        full_jump_animation moonjump
        full_jump_sync_frames 98
        full_jump_windup_frames 19
    }

    cost {
        act_points 1
    }
    
    target {
        min_range 0
        max_range 2 //boosted to 4 via low gravity
        min_aoe 0
        max_aoe 0
    }

    damage_instance {
        damage 0
    }
}
```

---

### `AZ_Jump_AI`
**Source:** `special_enemy_abilities.gon`  

```
AZ_Jump_AI { //jump pretends its targeting like a spawn ability so he can jump towards things
    template spawn

    target {
        min_range 0
        max_range 2
        low_gravity_boostable true
        restrictions must_be_moveable
    }

    spawn {
        object SmallRock
    }
}
```

---

### `AZ_BreakNeck`
**Source:** `special_enemy_abilities.gon`  

```
AZ_BreakNeck {
    template tile_targeted_melee_attack
    class PlaceholderMeleeAttackAbility

    graphics {
        animation breakneck
    }

    target {
        knockback_mode zero
        restrictions must_have_character
    }

    damage_instance {
        damage 15+bonus_melee_damage
        effects {
            SpecificInjury int
        }
    }
}
```

---

### `AZ_BreakLeg`
**Source:** `special_enemy_abilities.gon`  

```
AZ_BreakLeg {
    template tile_targeted_melee_attack
    class PlaceholderMeleeAttackAbility

    graphics {
        animation breakleg
    }

    target {
        knockback_mode zero
        restrictions must_have_character
    }

    damage_instance {
        damage 15+bonus_melee_damage
        effects {
            SpecificInjury spd
        }
    }
}
```

---

### `AZ_BreakArm`
**Source:** `special_enemy_abilities.gon`  

```
AZ_BreakArm {
    template tile_targeted_melee_attack
    class PlaceholderMeleeAttackAbility

    graphics {
        animation breakarm
    }

    target {
        knockback_mode zero
        restrictions must_have_character
    }

    damage_instance {
        damage 15+bonus_melee_damage
        effects {
            SpecificInjury str
        }
    }
}
```

---

### `AZ_LoseHead`
**Source:** `special_enemy_abilities.gon`  

```
AZ_LoseHead {
    template spawn
    
    graphics { 
        animation dying
        lob true
        dont_orient true
    }

    target {
        target_mode random_tile
        min_range 2
        max_range 4
    }

    self_damage {
        //heal 999

        effects {
            TimeDelayStatusApplication {
                delay 3
                Cleanse 0
                FullHeal 1
            }
            FormChange {
                form "Headless"
            }
        }
    }

    spawn {
        object AstroZombieHead
    }
}
```

---

### `AZ_Scream`
**Name:** Scream  
**Source:** `special_enemy_abilities.gon`  

```
AZ_Scream {
    template spell

    meta {
        name "EABILITY_SCREAM_NAME"
    }

    graphics {
        particle none
        animation scream
    }
    
    cost {
        mana 0
        requires_exact_character_aux 0
    }
    
    target {
        target_mode none
        max_aoe 3
        prioritize_dont_change_direction true
        aoe_excludes_self true
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Conditional_Enemy {
                Fear 1
            }
        }
    }
}
```

---

### `SM_Lavashot`
**Source:** `special_enemy_abilities.gon`  

```
SM_Lavashot {
    variant_of BelcherLavashot

    damage_instance {
        damage 2+bonus_ranged_damage

        effects {
            Burn 1
        }
    }
}
```

---

### `SM_Flamethrower`
**Name:** Flamethrower  
**Source:** `special_enemy_abilities.gon`  

```
SM_Flamethrower {
    variant_of MCFlamethrower

    meta {
        name "EABILITY_FLAMETHROWER_NAME"
    }

    cost {
        cantrip true
    }
    damage_instance {
        damage 3+bonus_basic_spell_damage
        ai_base_score 999999

        effects {
            Burn 2
        }
    }
}
```

---

### `SM_MagicMissile`
**Source:** `special_enemy_abilities.gon`  

```
SM_MagicMissile {
    variant_of MagicMissile

    cost {
        cantrip false
        infcantrip false
        mana 0
        act_points 1
    }
}
```

---

### `SM_IceShards`
**Name:** Shards of Ice  
**Source:** `special_enemy_abilities.gon`  

```
SM_IceShards {
    template spell

    meta {
        name "EABILITY_SHARDSOFICE_NAME"
    }
    
    cost {
        prime 1
        cantrip true
    }

    graphics {
        animation ice
        particle Icequake
    }
    
    target {
        target_mode direction

        aoe_mode circle
        min_aoe 1
        max_aoe 2
    }
    
    damage_instance {
        damage 6+bonus_basic_spell_damage
        ai_base_score 999999

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

### `SM_Snow`
**Name:** Snow  
**Source:** `special_enemy_abilities.gon`  

```
SM_Snow {
    template spell

    meta {
        name "EABILITY_SNOW_NAME"
    }

    graphics {
        particle IcePoof
    }
    
    target {
        target_mode none

        aoe_mode all
        aoe_excludes_self true
        knockback_mode none
    }
    
    damage_instance {
        damage 1+bonus_basic_spell_damage

        effects {

        }
        
        elements [
            Ice
        ]
    }
}
```

---

### `SM_IceBreath`
**Name:** Ice Breath  
**Source:** `special_enemy_abilities.gon`  

```
SM_IceBreath {
    template spell

    meta {
        name "EABILITY_ICEBREATH_NAME"
    }

    graphics {
        particle IcePoof
        animation blowFire
        delay 3
        visual_delay_but_simultaneous_damage 20
    }
    
    target {
        target_mode direction

        aoe_mode narrow_cone
        min_aoe 2
        max_aoe 3
        //aoe_restrictions must_have_piercing_line_of_sight
        knockback_mode orientation
    }
    
    damage_instance {
        damage 4+bonus_basic_spell_damage
        knockback 1

        effects {
           // Slow 1
           ChangeTile IceTile
        }
        
        elements [
            Ice
            Wind
        ]
    }
}
```

---

### `SM_LightningDash`
**Name:** Lightning Dash  
**Source:** `special_enemy_abilities.gon`  

```
SM_LightningDash {
    template dash_attack
    class PierceDashAbility
    
    meta {
        name "EABILITY_LIGHTNINGDASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
    }
    
    cost {
        mana 5
    }
    
    target {

    }

    damage_instance {
        damage 6+bonus_basic_spell_damage
        type spell
        makes_contact true
        two_way_contact true

        effects {
            VisualFX WaterConduct
        }

        elements [
            Electric
        ]
    }
}
```

---

### `SM_LightningStorm`
**Name:** Lightning Storm  
**Source:** `special_enemy_abilities.gon`  

```
SM_LightningStorm {
    template spell

    meta {
        name "EABILITY_LIGHTNINGSTORM_NAME"
    }
    
    cost {
        cantrip true
        prime 1
    }

    graphics {
        particle Bolt
        delay 5
    }
    
    target {
        max_range 20
        target_mode none
        aoe_excludes_self true

        aoe_mode all
        knockback_mode none

        aoe_restrictions checker_parity_even
    }
    
    damage_instance {
        damage 3+bonus_basic_spell_damage
        ai_base_score 999999

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

### `SM_BleedCounter`
**Source:** `special_enemy_abilities.gon`  

```
SM_BleedCounter {
    variant_of BasicMelee

    damage_instance {
        effects {
            Bleed 1
        }
    }
}
```

---

### `MM_Slap`
**Source:** `special_enemy_abilities.gon`  

```
MM_Slap {
    template melee_attack

    graphics {
        animation swat
    }

    cost {
        cantrip true
        mana 0
    }

    target {
        max_aoe 1
    }

    damage_instance {
        damage 1+bonus_melee_damage
        knockback 10
    }
}
```

---

### `MM_Quake`
**Name:** Quake  
**Source:** `special_enemy_abilities.gon`  

```
MM_Quake {
    template spell

    meta {
        name "EABILITY_QUAKE_NAME"
    }

    graphics {
        animation slam
        delay 3
        particle Earthquake
    }

    target {
        target_mode direction

        aoe_mode line
        aoe_considers_character_size true
        aoe_excludes_self true
        min_aoe 1
        max_aoe 10
        aoe_leading_edge_only true
    }

    
    damage_instance {
        damage 2

        effects {
            SpawnRock [1, .20]
            Petrify [1, .1]
        }

        elements [
            Earth
        ]
    }
}
```

---

### `MM_Guard`
**Source:** `special_enemy_abilities.gon`  

```
MM_Guard {
    template self_buff

    graphics {
        animation guard
        dont_orient true
    }
    
    cost {
        cantrip true
    }

    damage_instance {
        ai_base_score 999999
        effects {
            FormChange {
                form "Guarding"
            } 
        }
    }
}
```

---

### `MM_Unguard`
**Source:** `special_enemy_abilities.gon`  

```
MM_Unguard {
    template self_buff

    graphics {
        animation unguard
        dont_orient true
    }

    target {
        prioritize_dont_change_direction true
    }
    
    cost {
        cantrip true
    }

    damage_instance {
        ai_base_score 999999
        effects {
            FormChange {
                form "Default"
            } 
        }
    }
}
```

---

### `MM_Grab`
**Source:** `special_enemy_abilities.gon`  

```
MM_Grab { //TODO: this kind of move on 2x2s needs to act more like MeleeEatAbility (select a random target from whats in front)
    template tile_targeted_melee_attack
    class PlaceholderMeleeAttackAbility

    graphics {
        animation grab
    }

    target {
        knockback_mode tile_to_character
        restrictions must_have_character
        aoe_considers_character_size false
    }

    damage_instance {
        damage 0
        effects {
             DieViolently 1
        }
    }
}
```

---

### `MoonHandDash`
**Source:** `special_enemy_abilities.gon`  

```
MoonHandDash {
    template dash_attack
    
    graphics {
        dash_start_animation dashstart2
        dash_animation dash2
        always_play_animations true
        //dash_end_animation dashend
        dash_attack_animation dashEnd2
    }
    
    target {
        target_mode direction8
        consider_trample true
    }

    temporary_effects {
        Trample 3
    }
    
    damage_instance {
        damage 10+bonus_melee_damage
        knockback 10

        effects {
            //Bruise 1
            Conditional_HasTag {
                tag moonhead
                RemoveStatus Brace
                BonusDamage 10
                CrackMoonHead 1
            }
        }
    }
}
```

---

### `MoonHandPunchHead`
**Source:** `special_enemy_abilities.gon`  

```
MoonHandPunchHead {
    variant_of MoonHandDash

    damage_instance {
        custom_additional_ai_weight moonhead_punchself

        effects {
            Conditional_Speculative {
                IgnoreDamage 1
            }
        }
    }
}
```

---

### `MoonHandSlap`
**Source:** `special_enemy_abilities.gon`  

```
MoonHandSlap {
    template melee_attack

    graphics {
        animation dashend
    }

    damage_instance {
        effects {
            Bruise 1
        }
    }
}
```

---

### `MoonHandGrab`
**Source:** `special_enemy_abilities.gon`  

```
MoonHandGrab {
    template targeted_status

    graphics {
        animation grab
    }

    cost {
        mana 0
        must_not_be_consuming true
        cantrip true
    }

    target {
        max_range 1
        range_mode cross
        restrictions [must_have_living_character /*must_have_cat*/]
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                instant true
                mount_mode auto
                force_contact true
                drop_body_ability MoonHandDrop
                do_not_pop_corpse true
                struggle_ability MoonHandFlail
            }
            GenericDebuff 1 //for AI
        }
    }
}
```

---

### `MoonHandSqueeze`
**Source:** `special_enemy_abilities.gon`  

```
MoonHandSqueeze {
    template self_buff
    class DamageConsumedCharactersAbility

    cost {

    }

    graphics {
        animation squeeze
    }
    
    
    target {
        target_mode none
        knockback_mode none
        prioritize_dont_change_direction true
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee
        contact_requires_adjacency false
        ai_base_score 9999

        effects {
            Bruise 1
        }
    }
}
```

---

### `MoonHead_RefreshBrace`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_RefreshBrace {
    template self_buff

    graphics {
        animation uncrack
    }

    cost {
        cantrip true
    }

    damage_instance {
        custom_additional_ai_weight moonhead_use_if_cracked 

        effects {
            RemoveStatus Brace
            Brace 10
            ReformMoonHead 1
        }
    }
}
```

---

### `MoonHandMegaSqueeze`
**Source:** `special_enemy_abilities.gon`  

```
MoonHandMegaSqueeze {
    template self_buff
    class DamageConsumedCharactersAbility

    cost {

    }

    graphics {
        animation squeeze
    }
    
    
    target {
        target_mode none
        knockback_mode none
        prioritize_dont_change_direction true
    }

    damage_instance {
        damage 999
        type melee
        contact_requires_adjacency false
        ai_base_score 9999

        effects {
            Vaporize 1
        }
    }
}
```

---

### `MoonHandThrow`
**Source:** `special_enemy_abilities.gon`  

```
MoonHandThrow {
    template throw_attack

    graphics {
        animation throw
        dont_orient true
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        //target_mode random_tile
        max_range 4 //boosted to 6 via low gravity
        min_range 3
        restrictions none
        throw_consumed_character true
    }

    bonus_passives {
        MoonHeadFinisherEnabler -1
    }
    
    damage_instance {
        damage 1
        blocked_damage 5+bonus_melee_ability_damage

        custom_additional_ai_weight toss_towards_bottomleft

        effects {
            Bruise 1
        }
    }
}
```

---

### `MoonHandDrop`
**Source:** `special_enemy_abilities.gon`  

```
MoonHandDrop {
    variant_of MoonHandThrow

    bonus_passives {
        MoonHeadFinisherEnabler 0
    }

    target {
        target_mode random_tile
        restrictions none
        prioritize_dont_change_direction true
        allow_any_orientation true
    }
}
```

---

### `MoonHandDrop_Deathrattle`
**Source:** `special_enemy_abilities.gon`  

```
MoonHandDrop_Deathrattle {
    variant_of MoonHandDrop

    graphics {
        animation dying
    }
}
```

---

### `MoonHead_BeginCharge`
**Name:** :O  
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_BeginCharge {
    template self_buff
    
    meta {
        name "EABILITY_MOONMANCHARGE_NAME"
    }

    graphics {
        animation openmouth
    }

    damage_instance {
        effects {
            FormChange {
                form "Charging"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `MoonHead_EatCat`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_EatCat {
    template targeted_status

    graphics {
        animation grab
    }

    cost {
        mana 0
        must_not_be_consuming true
        cantrip true
    }

    target {
        max_range 2
        min_range 2

        range_mode cross

        range_considers_character_size false
        aoe_considers_character_size false
        restrictions [must_have_living_character must_match_locked_orientation must_not_have_large_character]
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters
        ai_base_score 99999

        effects {
            
            Conditional_LivingPlayerCat {
                ApplyToSource {
                    FormChange HasCat
                }
                Consumed {
                    //instant true
                    mount_mode true
                    force_contact true
                    drop_on_death false
                    do_not_pop_corpse true
                    struggle_ability MoonHeadFlail
                    wet true
                }

                TempPassiveWhileHasStatus {
                    status Consumed
                    ReplaceSpell {
                        slot 0
                        ability MoonHeadCommandStopHittingYourself
                    }
                    ReplaceSpell {
                        slot 1
                        ability None
                    }
                    ReplaceSpell {
                        slot 2
                        ability None
                    }
                    ReplaceSpell {
                        slot 3
                        ability None
                    }
                }
            } Else {
                ApplyToSource {
                    FormChange Default
                }
                Vaporize 1
            }
            GenericDebuff 1 //for AI
        }
    }
}
```

---

### `MoonHead_SacrificeHand`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_SacrificeHand {
    template targeted_status

    graphics {

    }

    cost {
        mana 0
        cantrip true
    }

    target {
        max_range 20
        target_mode random_tile
        restrictions [must_have_tag must_have_living_character]
        target_requires_tag moonhand
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters
        ai_base_score 999999

        effects {
            Die 1
        }
    }
}
```

---

### `MoonHead_KillHands`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_KillHands {
    template targeted_status

    graphics {
        animation dying
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        aoe_mode all
        target_mode none
        restrictions [must_have_tag must_have_living_character]
        target_requires_tag moonhand
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters
        ai_base_score 999999

        effects {
            Conditional_HasTag {
                tag moonhand
                Die 1
            }
        }
    }
}
```

---

### `MoonHead_CallForHelp`
**Name:** Call for Help  
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_CallForHelp {
    template spawn

    meta {
        name "EABILITY_CALLFORHELP_NAME"
    }
    
    graphics {
        animation yell
        fall_from_sky true
        fall_randomize_timing .3
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    bonus_passives {
        AbilityEnabledOncePerFightAtHealthThreshold 25%
    }

    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        max_targets 4
    }

    spawn {
        object GreenProber
        ai_base_score 999999
        first_turn next_round
    }
}
```

---

### `MoonHead_CommandHeadPunch`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_CommandHeadPunch {
    template targeted_status

    graphics {
        animation none
        particle none
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        aoe_mode all
        restrictions [must_have_tag must_have_living_character]
        target_requires_tag moonhand
    }

    damage_instance {
        type none
        damage 0
        ai_base_score 999999
        cant_miss true

        effects {
            Conditional_HasTag {
                tag moonhand
                Conditional_InForm {
                    form Default
                    UseAbility MoonHandPunchHead
                }
            }
        }
    }
}
```

---

### `MoonHead_SpitCat`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_SpitCat {
    template throw_attack

    graphics {
        animation spit
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        target_mode tile
        max_range 20
        min_range 3
        range_mode standard
        restrictions must_match_locked_orientation
        prioritize_dont_change_direction true
        throw_consumed_character true
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage
        blocked_damage 5+bonus_melee_ability_damage
        ai_base_score 9999

        custom_additional_ai_weight toss_far
    }
}
```

---

### `MoonHead_SpitCat_AndDie`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_SpitCat_AndDie {
    variant_of MoonHead_SpitCat
    self_damage {
        effects {
            SpecialBossMultipartInstakill moonboss
        }
    }
}
```

---

### `MoonHead_ChewCat`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_ChewCat {
    template self_buff
    class DamageConsumedCharactersAbility

    cost {
        must_be_consuming true
    }

    graphics {
        animation chew
    }
    
    
    target {
        target_mode none
        knockback_mode none
        prioritize_dont_change_direction true
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee
        contact_requires_adjacency false
        ai_base_score 9999
    }
}
```

---

### `MoonHead_Barrage`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_Barrage {
    template lobbed_attack

    target {
        range_mode none
        target_mode direction
        aoe_mode cone
        max_aoe 10
        min_aoe 1

        aoe_leading_edge_only true
        aoe_considers_character_size true
        aoe_excludes_self true

        can_multihit false
        restrictions must_match_locked_orientation
    }
    
    self_damage {
        effects {
            FormChange {
                form "Default"
            }
        }
    }

    damage_instance {
        damage 10+bonus_ranged_damage
        ai_base_score 999999

        effects {
            Bruise 1
        }
    }
}
```

---

### `MoonHead_Blow`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_Blow {
    template spell

    graphics {
        particle fx_windSpell
        delay 2
        visual_delay_but_simultaneous_damage 4
    }

    target {
        range_mode none
        target_mode direction
        aoe_mode cone
        max_aoe 10
        min_aoe 1

        aoe_leading_edge_only true
        aoe_considers_character_size true
        aoe_excludes_self true

        can_multihit false
        restrictions must_match_locked_orientation
        knockback_mode orientation
    }
    
    self_damage {
        effects {
            FormChange {
                form "Default"
            }
        }
    }

    damage_instance {
        damage 0
        ai_base_score 999999
        knockback 10

        effects {
            Conditional_HasTag {
                tag moonhand
                IgnoreDamage 1
            }
        }
    }
}
```

---

### `MoonHead_Digest`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_Digest {
    template self_buff
    class DamageConsumedCharactersAbility

    cost {
        must_be_consuming true
    }

    graphics {
        animation digest
    }
    
    target {
        target_mode none
        knockback_mode none
        prioritize_dont_change_direction true
    }

    damage_instance {
        effects {
            Vaporize 1
        }
    }
}
```

---

### `MoonHead_SpawnHand`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_SpawnHand {
    template spawn

    graphics {
        lob false
    }

    cost {
        cantrip true
    }

    target {
        target_mode none
        aoe_mode square
        min_aoe 2
        max_aoe 20
        min_targets 1
        max_targets 1
        aoe_restrictions [must_be_empty]
    }

    spawn {
        object MoonHand
        lob false
        faction enemies
        ai_base_score 999999
    }
}
```

---

### `MoonHead_Finisher`
**Source:** `special_enemy_abilities.gon`  

```
MoonHead_Finisher {
    template spell

    graphics {
        lob false
        particle none
    }

    cost {
        cantrip true
    }

    target {
        target_mode none
        aoe_mode square
        max_aoe 20
    }

    bonus_passives {
        MoonHeadFinisherEnabler 1
    }

    damage_instance {
        damage 0
        type none
        cant_miss true
        makes_contact false
        ai_base_score 999999

        effects {
            Conditional_HasTag {
                tag moonhand
                ImmediateUseAbility MoonHandMegaSqueeze
            }
        }
    }
}
```

---

### `CaveBabyMelee`
**Source:** `special_enemy_abilities.gon`  

```
CaveBabyMelee {
    template melee_attack

    graphics {
        animation attack
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Leech 1
        }
    }
}
```

---

### `CaveBabyGrow`
**Source:** `special_enemy_abilities.gon`  

```
CaveBabyGrow {
    template self_buff

    graphics { 
        dont_orient true
        animation growup
    }

    damage_instance {
        heal 20
        effects {
            FormChange {
                form "CaveManSpear"
            }
            InstantMaxHealthUp 20
        }
        ai_base_score 9999
    }
}
```

---

### `CaveManTransform`
**Source:** `special_enemy_abilities.gon`  

```
CaveManTransform {
    template self_buff

    graphics { 
        dont_orient true
        animation transform
    }

    damage_instance {
        effects {
            FormChange {
                form "WereMan"
            }
            ChangeFaction sabertooths
        }
        ai_base_score 9999
    }
}
```

---

### `CaveManThrowSpear`
**Source:** `special_enemy_abilities.gon`  

```
CaveManThrowSpear {
    template lobbed_attack

    graphics {
        projectile SpearProjectile
        animation throw
    }

    target {
        min_range 1
        max_range 5
    }

    self_damage {
        effects {
            FormChange {
                form "CaveMan"
            }
        }
    }

    damage_instance {
        effects {
            Stun 1
            Displace 1
            BounceObject GroundedSpear
        }
    }
}
```

---

### `CaveManPickupSpear`
**Source:** `special_enemy_abilities.gon`  

```
CaveManPickupSpear {
    template tile_targeted_melee_attack

    graphics {
        animation pickup
    }

    target {
        restrictions must_have_tag
        target_requires_tag spear
    }

    damage_instance {
        damage 0
        type none
        makes_contact false
        cant_miss true
        effects {
            Conditional_HasTag {
                tag spear
                DeleteObject 1
                ApplyToSource {
                    FormChange {
                        form "CaveManSpear"
                    }
                }
            }
        }
        ai_base_score 99999
    }
}
```

---

### `CaveMan3HitCombo`
**Source:** `special_enemy_abilities.gon`  

```
CaveMan3HitCombo {
    template melee_attack

    graphics {
        animation attack
    }

    target {
        multihit 3
    }
    
    damage_instance {
        damage 2+bonus_melee_damage

        effects {
            Conditional_LastHit {
                Bruise 1
                BonusDamage 3
                KnockUpAndAway {
                    stacks 3
                    distance 3
                }
            }
        }
    }
}
```

---

### `CaveManChestPound`
**Name:** Fooga Bunga  
**Source:** `special_enemy_abilities.gon`  

```
CaveManChestPound {
    template spell

    meta {
        name "EABILITY_FOOGABUNGA_NAME"
    }

    graphics {
        particle none
        animation chestpound
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
                tag humanoid
                DamageUp 1
            }
        }
    }
}
```

---

### `CaveWomanGrab`
**Source:** `special_enemy_abilities.gon`  

```
CaveWomanGrab {
    template targeted_status

    graphics {
        animation grab
    }

    cost {
        mana 0
        must_not_be_consuming true
        cantrip true
    }

    target {
        max_range 1
        range_mode cross
        restrictions [must_have_cat must_have_living_character]
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                instant true
                mount_mode true
                force_contact true
                drop_on_death true
                drop_on_self_death true
                do_not_pop_corpse true
                struggle_ability CaveWomanEscape
            }
            GenericDebuff 1 //for AI
        }

        ai_base_score 999999
    }
}
```

---

### `CaveWomanDrop`
**Source:** `special_enemy_abilities.gon`  

```
CaveWomanDrop {
    template throw_attack

    graphics {
        animation drop
        min_throw_height 0
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        max_range 1
        min_range 1
        restrictions none
        throw_consumed_character true
        prioritize_dont_change_direction true
        reorient_thrown_character true
        range_mode cross

    }
    
    damage_instance {
        damage 0
        ai_base_score 9999
    }
}
```

---

### `CaveWomanDropTransform`
**Source:** `special_enemy_abilities.gon`  

```
CaveWomanDropTransform {
    template throw_attack

    graphics {
        animation transform
        dont_orient true
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        target_mode random_tile
        max_range 5
        min_range 3
        restrictions none
        throw_consumed_character true
        prioritize_dont_change_direction true
        reorient_thrown_character true
        range_mode cross
    }

    self_damage {
        effects {
            FormChange {
                form "WereMan"
            }
            ChangeFaction sabertooths
        }
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage
        blocked_damage 5+bonus_melee_ability_damage
    }
}
```

---

### `CaveWomanCatSlap`
**Source:** `special_enemy_abilities.gon`  

```
CaveWomanCatSlap {
    template melee_attack

    cost {
        mana 0
    }

    target {
        max_aoe 2
        aoe_restrictions none
    }

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            CollideWithConsumed 5+bonus_melee_damage
        }
    }
}
```

---

### `CaveWomanKick`
**Source:** `special_enemy_abilities.gon`  

```
CaveWomanKick {
    template melee_attack

    graphics {
        animation kick
    }

    cost {
        mana 0
    }

    damage_instance {
        knockback 3
    }
}
```

---

### `CaveWomanBirth`
**Source:** `special_enemy_abilities.gon`  

```
CaveWomanBirth {
    template spawn
    
    graphics {
        lob true
        animation birth
    }
    
    cost {
        mana 5
    }

    bonus_passives {
        CaveWomanBirthControl 1
    }
    
    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [ [-1, 0] ]
    }

    spawn {
        object CaveBaby
        ai_base_score 9999
        faction self
    }
}
```

---

### `CaveWomanThrow`
**Source:** `special_enemy_abilities.gon`  

```
CaveWomanThrow {
    template throw_attack

    graphics {
        animation throw
        dont_orient true
    }

    cost {
        mana 0
        must_be_consuming true
        must_be_first_nonmove_action true
    }
    
    target {
        max_range 5
        min_range 3
        restrictions none
        throw_consumed_character true
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        blocked_damage 5+bonus_melee_ability_damage
    }
}
```

---

### `WereManFurySwipes`
**Source:** `special_enemy_abilities.gon`  

```
WereManFurySwipes {
    template melee_attack
    class MultiHitMeleeAttackAbility
    
    graphics {
        start attack
        loop attack
        end upswipe
    }

    target {
        multihit_min 2
        multihit_max 5
    }

    damage_instance {
        damage 2+bonus_melee_damage
        type melee

        effects {
            Conditional_LastHit {
                KnockUpAndAway {
                    stacks 3
                    distance 3
                }
            } Else {
                Cleave 1
            }
            TriggerWerewolfTransform [1 .15]
        }
    }
}
```

---

### `WereManTransformSwipe`
**Source:** `special_enemy_abilities.gon`  

```
WereManTransformSwipe {
    template melee_attack
    
    graphics {
        animation attack
    }

    damage_instance {
        damage 2+bonus_melee_damage
        type melee
        non_lethal true

        effects {
            TriggerWerewolfTransform .5
        }
    }
}
```

---

### `WereManPounce`
**Name:** Pounce  
**Source:** `special_enemy_abilities.gon`  

```
WereManPounce {
    template jump_attack

    meta {
        name "EABILITY_POUNCE_NAME"
    }

    graphics {
        full_jump_animation pounce
        full_jump_sync_frames 37
        full_jump_windup_frames 10
    }

    target {
        aoe_excludes_self false
        max_aoe 0
        min_aoe 0

        max_range 5
        restrictions none
    }

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            IgnoreSelf 1
            Leech 1
            Displace 1
            TriggerWerewolfTransform [1 .5]
        }
    }
}
```

---

### `CaveBabyFoodMove`
**Source:** `special_enemy_abilities.gon`  

```
CaveBabyFoodMove {
    template move

    target {
        restrictions [must_be_moveable must_have_tag must_move]
        target_requires_tag food
    }
}
```

---

### `CaveManSpearRun`
**Source:** `special_enemy_abilities.gon`  

```
CaveManSpearRun {
    template move

    temporary_effects {
        Trample 3
    }
}
```

---

### `CaveChiefSlam`
**Source:** `special_enemy_abilities.gon`  

```
CaveChiefSlam {
    template melee_attack

    target {
        max_aoe 2
        aoe_restrictions none
    }

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            Stun 1
        }
    }
}
```

---

### `CaveChiefBat`
**Name:** Gruk Oog Mooga  
**Source:** `special_enemy_abilities.gon`  

```
CaveChiefBat {
    template melee_attack

    graphics {
        animation "bat"
    }

    meta {
        name "EABILITY_GRUKOOGMOOGA_NAME"
    }

    damage_instance {
        damage 0

        effects {
            Conditional_Speculative {
                Conditional_HealthThreshold {
                    threshold_flat 10
                    BonusDamage 20+bonus_melee_damage
                } Else {
                    FlatAIBonus -999999
                }
            } Else {
                Conditional_Displaceable {
                    LaunchOffScreenInstakill 1
                } Else {
                    BonusDamage 20+bonus_melee_damage
                }
            }
        }
    }
}
```

---

### `CaveChiefRally`
**Name:** Atook Thag Kat  
**Source:** `special_enemy_abilities.gon`  

```
CaveChiefRally {
    template targeted_status

    graphics {
        animation "rally"
    }

    meta {
        name "EABILITY_ATOOKTHAGKAT_NAME"
    }

    target {
        max_range 20
        min_range 1
        restrictions must_have_tag
        target_requires_tag humanoid
    }

    damage_instance {
        damage 0

        effects {
            TakeExtraTurn 1
        }
    }
}
```

---

### `CaveChiefFear`
**Name:** Raoog Fooba  
**Source:** `special_enemy_abilities.gon`  

```
CaveChiefFear {
    template spell

    meta {
        name "EABILITY_RAOOGFOOBA_NAME"
    }

    graphics {
        particle none
        animation yell
    }
    
    target {
        target_mode direction

        aoe_mode cone
        aoe_leading_edge_only true
        min_aoe 1
        max_aoe 10

        aoe_considers_character_size true
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0

        effects {
            Fear 1
        }
    }
}
```

---

### `YetiSlam`
**Source:** `special_enemy_abilities.gon`  

```
YetiSlam {
    template melee_attack

    graphics {
        animation slam
        dont_visualize_ai true
    }

    damage_instance {
        damage 3+bonus_melee_damage
    }
}
```

---

### `YetiBite`
**Source:** `special_enemy_abilities.gon`  

```
YetiBite {
    template melee_attack

    graphics {
        animation bite
        dont_visualize_ai true
    }

    damage_instance {
        damage 2+bonus_melee_damage

        effects {
            Bleed 2
            Leech 1
        }
    }
}
```

---

### `YetiKick`
**Source:** `special_enemy_abilities.gon`  

```
YetiKick {
    template melee_attack

    graphics {
        animation kick
        dont_visualize_ai true
    }

    damage_instance {
        damage 2+bonus_melee_damage
        knockback 3
    }
}
```

---

### `YetiIceBreath`
**Name:** Ice Breath  
**Source:** `special_enemy_abilities.gon`  

```
YetiIceBreath {
    template spell

    meta {
        name "EABILITY_ICEBREATH_NAME"
    }

    graphics {
        particle IcePoof
        animation icebreath
        delay 10
    }
    
    cost {
        act_points 3
    }

    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 3
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

### `SabertoothCatTransformSwipe`
**Source:** `special_enemy_abilities.gon`  

```
SabertoothCatTransformSwipe {
    template melee_attack
    
    graphics {
        animation attack
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee
        non_lethal true

        effects {
            TriggerWerewolfTransform .5
        }
    }
}
```

---

### `SabertoothCatPounce`
**Source:** `special_enemy_abilities.gon`  

```
SabertoothCatPounce {
    template jump_attack

    graphics {
        jump_attack_animation land
        jump_height_multiplier .25
        jump_speed_multiplier 1.5
    }

    sounds { 
        ontrigger SE_SabertoothCatPounce 
    }

    target {
        max_range 4

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
            TriggerWerewolfTransform [1 .5]
        }
    }
}
```

---

### `SabertoothCatDoubleSwipe`
**Source:** `special_enemy_abilities.gon`  

```
SabertoothCatDoubleSwipe {
    template melee_attack
    
    graphics {
        animation doubleswat
    }

    sounds { 
        ontrigger SE_SabertoothCatSwipe 
    }

    cost {
        cantrip true
    }

    target {
        multihit 2
    }

    damage_instance {
        damage 3+bonus_melee_damage

        effects {
            Bleed 1
            TriggerWerewolfTransform [1 .20]
        }
    }
}
```

---

### `SabertoothCubDoubleSwipe`
**Source:** `special_enemy_abilities.gon`  

```
SabertoothCubDoubleSwipe {
    template melee_attack
    
    graphics {
        animation doubleswat
    }

    sounds { 
        ontrigger SE_SabertoothCubSwipe 
    }

    cost {
        cantrip true
    }

    target {
        multihit 2
    }

    damage_instance {
        damage 3+bonus_melee_damage

        effects {
            Bleed 1
            TriggerWerewolfTransform [1 .20]
        }
    }
}
```

---

### `YeticatSnowball`
**Source:** `special_enemy_abilities.gon`  

```
YeticatSnowball {
    template lobbed_attack

    graphics {
        animation throwobject
		projectile Snowball
    }

    target {
        min_range 2
        max_range 2
    }

    damage_instance {
        effects {
            Slow 1
            Freeze [1 .25]
        }

        elements [
            Ice
        ]
    }
}
```

---

### `YeticatSnowball_Counter`
**Source:** `special_enemy_abilities.gon`  

```
YeticatSnowball_Counter {
    variant_of YeticatSnowball

    target {
        min_range 1
        max_range 1
    }
}
```

---

### `SabertoothCubLick`
**Source:** `special_enemy_abilities.gon`  

```
SabertoothCubLick {
    template melee_attack

    graphics {
        animation lickAttack
    }

    sounds {
        ontrigger SE_SabertoothCubLick
    }
    
    damage_instance {
        heal 5+bonus_melee_damage
    }
}
```

---

### `MammothBabyThrow`
**Source:** `special_enemy_abilities.gon`  

```
MammothBabyThrow {
    template melee_attack

    graphics {
        animation knockupatk
    }
    
    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            KnockUpAndAway {
                stacks 3
                distance 3
            }
        }
    }
}
```

---

### `MammothBabyStomp`
**Source:** `special_enemy_abilities.gon`  

```
MammothBabyStomp {
    template melee_attack
    
    graphics {
        animation groundpound
    }
    
    cost {
        cantrip true
    }
    
    target {
        target_mode none
        aoe_mode cross
        min_aoe 0
        knockback_mode character_to_tile
        aoe_excludes_self false
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1

        effects {
            IgnoreSelf 1
            Bruise 1
            DoScreenShake {
                time .5
                intensity 3
            }
        }

        elements [
            Earth
        ]
    }
}
```

---

### `FuzzerJump`
**Source:** `special_enemy_abilities.gon`  

```
FuzzerJump {
    variant_of BasicJump

    graphics {
        full_jump_animation fuzzjump
        full_jump_sync_frames 57
        full_jump_windup_frames 8
    }
}
```

---

### `FuzzerJump_post`
**Source:** `special_enemy_abilities.gon`  

```
FuzzerJump_post {
    variant_of FuzzerJump

    graphics {
        dont_visualize_ai true
    }

    cost {
        move_points 0
        cantrip true
    }

    target {
        min_range 3
        max_range 5
        target_mode random_tile
    }

    damage_instance {
        ai_base_score 999
    }
}
```

---

### `FuzzerReact`
**Source:** `special_enemy_abilities.gon`  

```
FuzzerReact {
    template self_buff
    
    graphics {
        animation react
    }

    damage_instance {
        heal 5
    }
}
```

---

### `MammothThrow`
**Source:** `special_enemy_abilities.gon`  

```
MammothThrow {
    template melee_attack

    graphics {
        animation attack
    }
    
    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            KnockUpAndAway {
                stacks 3
                distance 3
                circular_variance 2
            }
        }
    }
}
```

---

### `MammothTrampleDash`
**Name:** Stampede  
**Source:** `special_enemy_abilities.gon`  

```
MammothTrampleDash {
    template trample_dash
    
    meta {
        name "EABILITY_STAMPEDE_NAME"
    }

    cost {
        cantrip true
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
    }

    damage_instance {
        damage 8+bonus_melee_damage
    }
}
```

---

### `MammothStomp`
**Source:** `special_enemy_abilities.gon`  

```
MammothStomp {
    template melee_attack
    
    graphics {
        animation stompy
    }
    
    cost {
        cantrip true
    }
    
    target {
        target_mode none
        aoe_mode square
        min_aoe 0
        max_aoe 1
        knockback_mode character_to_tile
        aoe_excludes_self false
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1

        effects {
            IgnoreSelf 1
            Bruise 1
            DoScreenShake {
                time 2
                intensity 10
            }
        }

        elements [
            Earth
        ]
    }
}
```

---

### `LabPillarDrop`
**Source:** `special_enemy_abilities.gon`  

```
LabPillarDrop {
    template spawn

    graphics {
        fall_from_sky true
        bounce_on_hit true
        animation dying
        dont_orient true
        fall_randomize_timing .3
    }

    target {
        target_mode none
        min_aoe 1
        max_aoe 2

        min_targets 3
        max_targets 5

        aoe_restrictions none

        knockback_mode zero
    }

    spawn {
        object [Pinky Rat SmallRock Junk RandomPickup RandomPickup]
        faction default
    }

    damage_instance {
        damage 5
    }
}
```

---

### `ColorlessCat_Push`
**Name:** Push  
**Source:** `special_enemy_abilities.gon`  

```
ColorlessCat_Push {
    template dash_attack
    
    meta {
        name "EABILITY_PUSH_NAME"
    }

    graphics {
        dash_start_animation headbuttdashStart
        dash_animation headbuttdash
        dash_attack_animation headbuttdashEnd
    }

    cost {
        mana 0
        act_points 1
    }

    target { 
        target_mode direction8
        max_range 1
        max_aoe 1
        aoe_restrictions must_have_line_of_sight_unpurgable
    }

    damage_instance {
        damage 4+bonus_melee_damage
        knockback 10
    }
}
```

---

### `RockToss_ColorlessCat`
**Name:** Rock Toss  
**Source:** `special_enemy_abilities.gon`  

```
RockToss_ColorlessCat {
    template lobbed_attack

    meta {
        name "EABILITY_ROCKTOSS_NAME"
    }

    graphics {
        projectile SmallRock
        animation throwobject
    }
    
    cost {
        mana 0
        act_points 1
    }
    
    target {
        min_range 3
        max_range 5
    }
    
    damage_instance {
        damage 3+bonus_ranged_damage

        effects {
            BounceObject SmallRock
        }

        elements [
            Rock
        ]

        custom_additional_ai_weight dont_target_rock
    }
}
```

---

### `RockToss_ColorlessCat_AsCloseAsPossible`
**Source:** `special_enemy_abilities.gon`  

```
RockToss_ColorlessCat_AsCloseAsPossible {
    variant_of RockToss_ColorlessCat

    damage_instance {
        custom_additional_ai_weight tile_close_to_enemy
    }
}
```

---

### `ColorlessCat_BoulderDrop`
**Name:** Boulder Drop!  
**Source:** `special_enemy_abilities.gon`  

```
ColorlessCat_BoulderDrop {
    template spawn

    meta {
        name "EABILITY_BOULDERDROP_NAME"
    }

    tags [summon]
    
    graphics {
        fall_from_sky true
        bounce_on_hit false
        animation floatingmagic
        dont_orient true
    }
    sounds {
        oncast AbilitySnd_BoulderDrop
    }

    bonus_passives {
        AbilityEnabledOncePerFightAtHealthThreshold 16
    }
    
    target {
        target_mode tile
        min_range 1
        max_range 20
        max_aoe 0

        range_excludes_blocking false
        aoe_restrictions none

        knockback_mode zero
    }

    spawn {
        object Boulder
    }

    damage_instance {
        damage 999
        cant_miss true
        type ranged

        effects {
            AIFavorLowHealth 100
        }

        custom_additional_ai_weight tutorial_boulderdrop_miss_if_one_left
    }
}
```

---

### `BungaEntrance`
**Source:** `special_enemy_abilities.gon`  

```
BungaEntrance {
    template jump_attack

    graphics {
        jump_start_animation enterbattle
        air_animation entrance
        jump_attack_animation entrance_land
        land_animation none

        fixed_jump_height 3.5
        fixed_jump_speed .8
    }

    target {
        target_mode random_farthest_tile
        range_mode custom
        custom_range [ [0 0] [-1 0] [-2 0] [-3 0] [-4 0] ]
        max_range 4
        max_aoe 2
        aoe_mode circle
        aoe_considers_character_size false
        range_considers_character_size false
    }

    temporary_effects {
        JustInCaseTrample 0
        JumpAttackLeaveBehind BungaThrone
    }

    self_damage {
        effects {
            FormChange Standing
            Cleanse 0
        }
    }

    damage_instance {
        damage 0
        effects {
            IgnoreSelf true
            KnockUpAndAway {
                stacks 3
                distance 3
            }
        }
    }
}
```

---

### `BungaEatCat`
**Source:** `special_enemy_abilities.gon`  

```
BungaEatCat {
    template melee_attack
    class MeleeEatAbility
    ai_ability BasicBigMelee //needed so daddy shark's simple brain can understand this

    graphics {
        animation consume
    }

    target { 
        max_aoe 1
        restrictions cant_target_behind
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true

        effects {
            Vaporize 20
        }
    }
}
```

---

### `BungaSwipe_ai`
**Source:** `special_enemy_abilities.gon`  

```
BungaSwipe_ai {
    template melee_attack

    target {
        aoe_leading_edge_only true
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1] [2, 0]]
        restrictions cant_target_behind
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        knockback 3
    }
}
```

---

### `BungaSwipe`
**Source:** `special_enemy_abilities.gon`  

```
BungaSwipe {
    ai_ability BungaSwipe_ai
    template melee_attack

    graphics {
        animation swing
    }
    
    target {
        aoe_leading_edge_only true
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[0, -1] [0, 0] [0, 1] [1, -1] [1, 0] [1, 1] [2, 0]]
        restrictions cant_target_behind
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        knockback 3
    }
}
```

---

### `BungaSmash`
**Source:** `special_enemy_abilities.gon`  

```
BungaSmash {
    template melee_attack

    graphics {
        animation attack
    }
    
    target {
        max_aoe 2
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        knockback 1

        effects {
            Bruise 1
            SpecificInjury int
        }
    }
}
```

---

### `BungaRoar`
**Name:** Booga!  
**Source:** `special_enemy_abilities.gon`  

```
BungaRoar {
    template spell

    meta {
        name "EABILITY_BOOGA_NAME"
    }

    graphics {
        particle none
        animation roar
    }

    target {
        target_mode none
        aoe_mode all
        prioritize_dont_change_direction true
        aoe_excludes_self true
    }

    damage_instance {
        damage 0
        ai_base_score 999999

        effects {
            Slow 2
        }
    }
}
```

---

### `BungaJumpMove`
**Source:** `special_enemy_abilities.gon`  

```
BungaJumpMove {
    variant_of BasicJump

    target {
        max_range mov
        max_aoe 0
        aoe_mode occupied_tiles
        aoe_considers_character_size false
        range_considers_character_size false
    }

    temporary_effects {
        JustInCaseTrample 0
    }
}
```

---

### `SpewerTransformNormal`
**Source:** `special_enemy_abilities.gon`  

```
SpewerTransformNormal {
    template self_buff

    graphics { 
        dont_orient true
        animation transform
        dont_visualize_ai true
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        prioritize_dont_change_direction true
    }

    bonus_passives {
        AbilityEnableIfConsumedCharacterHasTag sp_pill_normal
    }

    damage_instance {
        heal 4

        effects {
            DamageUp 1
            ApplyToConsumed {
                DeleteObject 1
            }
            FormChange {
                form "Normal"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `SpewerTransformFire`
**Source:** `special_enemy_abilities.gon`  

```
SpewerTransformFire {
    template self_buff

    graphics { 
        dont_orient true
        animation transform
        dont_visualize_ai true
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        prioritize_dont_change_direction true
    }

    bonus_passives {
        AbilityEnableIfConsumedCharacterHasTag sp_pill_fire
    }

    damage_instance {
        heal 4

        effects {
            SpeedUp 1
            ApplyToConsumed {
                DeleteObject 1
            }
            FormChange {
                form "Fire"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `SpewerTransformTar`
**Source:** `special_enemy_abilities.gon`  

```
SpewerTransformTar {
    template self_buff

    graphics { 
        dont_orient true
        animation transform
        dont_visualize_ai true
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        prioritize_dont_change_direction true
    }

    bonus_passives {
        AbilityEnableIfConsumedCharacterHasTag sp_pill_tar
    }

    damage_instance {
        heal 4

        effects {
            Brace 1
            ApplyToConsumed {
                DeleteObject 1
            }
            FormChange {
                form "Tar"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `SpewerSuck_base`
**Source:** `special_enemy_abilities.gon`  

```
SpewerSuck_base {
    template straightshot_attack

    graphics {
        animation suck
        projectile None
    }

    cost {
        mana 0
        must_not_be_consuming true
        cantrip true
        cantrip_group spewer_suck
    }

    target {
        max_aoe 10
        knockback_mode none
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                wet true
                struggle_ability Thrash
            }
        }

        elements [
            Wind
        ]
    }
}
```

---

### `SpewerSuckNormal`
**Source:** `special_enemy_abilities.gon`  

```
SpewerSuckNormal {
    variant_of SpewerSuck_base

    damage_instance {
        effects {
            Consumed {
                wet true

                extra_statuses {
                    Poison 1
                }
            }
        }
    }
}
```

---

### `SpewerSuckTar`
**Source:** `special_enemy_abilities.gon`  

```
SpewerSuckTar {
    variant_of SpewerSuck_base

    damage_instance {
        effects {
            Consumed {
                wet false

                extra_statuses {
                    Tarred 2
                }
            }
        }
    }
}
```

---

### `SpewerSuckLava`
**Source:** `special_enemy_abilities.gon`  

```
SpewerSuckLava {
    variant_of SpewerSuck_base

    damage_instance {
        effects {
            Consumed {
                wet false

                extra_statuses {
                    Burn 4
                }
            }
        }
    }
}
```

---

### `SpewerSuckPill`
**Source:** `special_enemy_abilities.gon`  

```
SpewerSuckPill {
    variant_of SpewerSuck_base

    cost {
        act_points 0
        cantrip true
        cantrip_group spewer_suck
    }

    target {
        max_aoe 3
        knockback_mode none
    }

    damage_instance {
        custom_additional_ai_weight pills_only
    }
}
```

---

### `SpewerLobbed_Normal`
**Source:** `special_enemy_abilities.gon`  

```
SpewerLobbed_Normal {
    template lobbed_attack

    graphics {
        animation spit
		projectile Creepball
    }

    target {
        min_range 3
        max_range 5
    }

    damage_instance {
        damage 5+bonus_ranged_damage
        
        effects {
            ChangeTile CreepTile
            Poison 1
        }
    }
}
```

---

### `SpewerLobbed_Tar`
**Source:** `special_enemy_abilities.gon`  

```
SpewerLobbed_Tar {
    template lobbed_attack

    graphics {
        animation spit
		projectile Tarshot
    }

    target {
        min_range 3
        max_range 5
    }

    damage_instance {
        damage 3+bonus_ranged_damage
        
        effects {
            ChangeTile OilTile
            Tarred 2
        }
    }
}
```

---

### `SpewerLobbed_Lava`
**Source:** `special_enemy_abilities.gon`  

```
SpewerLobbed_Lava {
    template lobbed_attack

    graphics {
        animation spit
		projectile LavaBall
    }

    target {
        min_range 3
        max_range 5
    }

    damage_instance {
        damage 2+bonus_ranged_damage
        
        effects {
            ChangeTile LavaTile
            Burn 4
        }
    }
}
```

---

### `SpewerSpit_AI`
**Source:** `special_enemy_abilities.gon`  

```
SpewerSpit_AI {
    template spell

    target {
        max_range 10
        min_range 1
        range_mode cross
        restrictions none

        aoe_mode line
        max_aoe 10

        restrictions must_be_empty
        aoe_restrictions must_have_target_line_of_sight
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 5
        ai_base_score 9999
        custom_additional_ai_weight target_closest
    }
}
```

---

### `SpewerSpit`
**Name:** Spit  
**Source:** `special_enemy_abilities.gon`  

```
SpewerSpit {
    template throw_attack
    ai_ability SpewerSpit_AI
    
    meta {
        name "EABILITY_SPIT_NAME"
    }

    graphics {
        animation spit
        min_throw_height .25
    }

    cost {
        mana 0
        must_be_consuming true
        cantrip true
    }
    
    target {
        max_range 10
        min_range 1
        range_mode cross
        throw_consumed_character true
        restrictions must_be_empty
    }
    
    damage_instance {
        damage 0
        knockback 10
        blocked_damage 5+bonus_melee_ability_damage
        ai_base_score 9999

        custom_additional_ai_weight target_closest

        effects {
            OverrideKnockbackDamage 5
        }
    }
}
```

---

### `SpewerBarf_Normal`
**Source:** `special_enemy_abilities.gon`  

```
SpewerBarf_Normal {
    template lobbed_attack

    graphics {
        animation spit
		projectile Creepball
    }

    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[1 0] [2 -1] [2 0] [2 1] [3 -1] [3 0] [3 1] [4 -1] [4 0] [4 1]]
        max_targets 5
    }

    damage_instance {
        damage 5+bonus_ranged_damage
        
        effects {
            ChangeTile CreepTile
            Poison 1
        }
    }
}
```

---

### `SpewerBarf_Tar`
**Source:** `special_enemy_abilities.gon`  

```
SpewerBarf_Tar {
    template lobbed_attack

    graphics {
        animation spit
		projectile Tarshot
    }

    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[1 0] [2 -1] [2 0] [2 1] [3 -1] [3 0] [3 1] [4 -1] [4 0] [4 1]]
        max_targets 5
    }

    damage_instance {
        damage 3+bonus_ranged_damage
        
        effects {
            ChangeTile OilTile
            Tarred 2
        }
    }
}
```

---

### `SpewerBarf_Lava`
**Source:** `special_enemy_abilities.gon`  

```
SpewerBarf_Lava {
    template lobbed_attack

    graphics {
        animation spit
		projectile LavaBall
    }

    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[1 0] [2 -1] [2 0] [2 1] [3 -1] [3 0] [3 1] [4 -1] [4 0] [4 1]]
        max_targets 5
    }

    damage_instance {
        damage 2+bonus_ranged_damage
        
        effects {
            ChangeTile LavaTile
            Burn 4
        }
    }
}
```

---

### `SpawnSpewerPill`
**Source:** `special_enemy_abilities.gon`  

```
SpawnSpewerPill {
    template spawn

    graphics {
        lob true
        animation shoot
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode random_tile
        min_range 3
        max_range 6
    }

    spawn {
        object [SpewerPill_Normal SpewerPill_Fire SpewerPill_Tar]
        ai_base_score 999999
    }
}
```

---

### `IceElementalBlizzard`
**Name:** Blizzard  
**Source:** `special_enemy_abilities.gon`  

```
IceElementalBlizzard {
    template spell

    meta {
        name "EABILITY_BLIZZARD_NAME"
    }

    graphics {
        animation blizzard
        particle IcePoof
    }

    cost {
        cantrip true
    }
    
    target {
        target_mode none

        aoe_mode all
        aoe_excludes_self true
        knockback_mode character_to_tile
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 0
        knockback 1

        effects {
            SpeedUp -1
        }
        
        elements [
            Ice
        ]

        ai_base_score 999999
    }
}
```

---

### `IceElementalSpikes`
**Source:** `special_enemy_abilities.gon`  

```
IceElementalSpikes {
    template spell

    graphics {
        animation ice
        particle Icequake
    }
    
    target {
        target_mode none

        aoe_mode square
        max_aoe 1
        aoe_excludes_self true
        knockback_mode character_to_tile
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 5
        knockback 1

        effects {
            Freeze 1
            ChangeTile IceShardsSmall
        }
        
        elements [
            Ice
        ]
    }
}
```

---

### `IceElementalBreath`
**Name:** Frost Breath  
**Source:** `special_enemy_abilities.gon`  

```
IceElementalBreath {
    template spell
    ai_ability IceElementalBreath_ai

    meta {
        name "EABILITY_FROSTBREATH_NAME"
    }

    graphics {
        animation freeze
        particle IcePoof
        delay 3
        visual_delay_but_simultaneous_damage 30
    }

    cost {
        cantrip true
    }

    target {
        target_mode direction

        aoe_mode cone
        min_aoe 2
        max_aoe 10
        aoe_excludes_self true
        knockback_mode character_to_tile
        aoe_restrictions must_have_piercing_line_of_sight
    }
    
    damage_instance {
        damage 5
        knockback 1

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

### `IceElementalBreath_ai`
**Source:** `special_enemy_abilities.gon`  

```
IceElementalBreath_ai {
    template spell

    target {
        target_mode direction

        aoe_mode cone
        min_aoe 2
        max_aoe 10
        aoe_excludes_self true
        knockback_mode character_to_tile
    }

    damage_instance {
        damage 5

        elements [
            Ice
        ]
    }
}
```

---

### `TrexEat`
**Source:** `special_enemy_abilities.gon`  

```
TrexEat {
    template melee_attack
    class MeleeEatAbility

    graphics {
        animation eat
        use_placeholder true
    }

    target { 
        max_aoe 1
        aoe_restrictions must_have_aggro_target
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true

        effects {
            Vaporize 20
            FlatLeech 10
        }
        ai_base_score 999999
    }
}
```

---

### `TrexSwitchTarget`
**Source:** `special_enemy_abilities.gon`  

```
TrexSwitchTarget {
    template targeted_status

    graphics {
        preturn_animation alertstart
        animation alertend
    }

    target { 
        max_range 20
    }

    damage_instance {
        cant_miss true

        effects {
            CanApplyToInanimate {
                GetAggroTarget 1
            }
        }
        ai_base_score 999999
    }
}
```

---

### `TrexReacquireTarget`
**Source:** `special_enemy_abilities.gon`  

```
TrexReacquireTarget {
    template targeted_status

    graphics {
        preturn_animation alertstart
        animation alertend
        dont_visualize_ai true
    }

    cost {
        cantrip true
    }

    target { 
        max_range 20

        restrictions [must_have_cat must_have_enemy]
    }

    bonus_passives {
        AbilityEnabledIfNoAggroTarget 1
    }

    damage_instance {
        cant_miss true

        effects {
            CanApplyToInanimate {
                GetAggroTarget 1
            }
        }
        ai_base_score 999999
    }
}
```

---

### `TrexStomp`
**Source:** `special_enemy_abilities.gon`  

```
TrexStomp {
    template melee_attack
    
    graphics {
        animation stomp
    }
    
    cost {
        cantrip true
    }
    
    target {
        target_mode none
        aoe_mode square
        aoe_excludes_self true
        min_aoe 0
        max_aoe 1
        knockback_mode character_to_tile
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            Immobile 1
            DoScreenShake {
                time 2
                intensity 20
            }
        }
    }
}
```

---

### `StegoTailSwipe`
**Source:** `special_enemy_abilities.gon`  

```
StegoTailSwipe {
    template melee_attack
    
    graphics {
        animation counter
    }

    target {
        min_aoe -1
        max_aoe -1
    }
    
    damage_instance {
        damage 6+bonus_melee_damage
        piercing true

        effects {
            Bleed 1
        }

        elements [
            Spikes
        ]
    }
}
```

---

### `StegoEatGrass`
**Source:** `special_enemy_abilities.gon`  

```
StegoEatGrass {
    template melee_attack
    
    graphics {
        animation bite
    }

    target {
        aoe_restrictions tile_must_have_element
        aoe_tile_requires_element Grass
    }

    self_damage {
        heal 5
        effects {
            Cleanse 0
        }
    }
    
    damage_instance {
        layer tiles
        effects {
            ChangeTile BlankTile
        }
        ai_base_score 99999
    }
}
```

---

### `StegoSpin`
**Source:** `special_enemy_abilities.gon`  

```
StegoSpin {
    template melee_attack
    
    graphics {
        animation spin
    }
    
    target {
        target_mode none
        aoe_mode square
        aoe_excludes_self true
        min_aoe 0
        max_aoe 1
        knockback_mode character_to_tile
        prioritize_dont_change_direction true
    }
    
    damage_instance {
        damage 6+bonus_melee_damage
        piercing true

        effects {
            Bleed 1
        }

        elements [
            Spikes
        ]
    }
}
```

---

### `StegoGrassStomp`
**Source:** `special_enemy_abilities.gon`  

```
StegoGrassStomp {
    template move

    graphics {
        animation walk2
    }

    target {
        max_range 20
    }
}
```

---

### `TriceratopsTrample`
**Name:** Trample Dash  
**Source:** `special_enemy_abilities.gon`  

```
TriceratopsTrample {
    template dash_attack
    
    meta {
        name "EABILITY_TRAMPLEDASH_NAME"
    }
    
    graphics {
        //dash_start_animation dashstart
        dash_animation ram
        dash_attack_animation none
    }
    
    cost {
        prime 1
        cantrip true
    }
    
    target {
        consider_trample true
    }
    
    damage_instance {
        damage 8+bonus_melee_damage
        knockback 1
        override_trample_damage true

        effects {
            Conditional_IsTrample { 
                SetKnockback 0
            }
        }
    }
}
```

---

### `TriceratopsGore`
**Source:** `special_enemy_abilities.gon`  

```
TriceratopsGore {
    template melee_attack

    graphics {
        animation attack
    }

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            KnockUpAndAway {
                stacks 3
                distance -3
            }
        }
    }
}
```

---

### `PteroGrab`
**Source:** `special_enemy_abilities.gon`  

```
PteroGrab {
    template targeted_status

    graphics {
        animation grab
    }

    cost {
        mana 0
        must_not_be_consuming true
    }

    target {
        max_range 1
        range_mode cross
        restrictions [must_have_cat must_have_living_character]
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            RefreshMovePointsIfHit 1
            Consumed {
                instant true
                mount_mode true
                force_contact true
                drop_on_death true
                drop_on_self_death true
                do_not_pop_corpse true
                struggle_ability PteroTryEscape
            }
            GenericDebuff 1 //for AI
        }

        //ai_base_score 999999
    }
}
```

---

### `PteroPeck`
**Name:** Peck  
**Source:** `special_enemy_abilities.gon`  

```
PteroPeck {
    template self_buff
    class DamageConsumedCharactersAbility

    meta {
        name "EABILITY_PECK_NAME"
    }

    cost {

    }

    graphics {
        animation peck
    }
    
    
    target {
        target_mode none
        knockback_mode none
        prioritize_dont_change_direction true
        multihit 3
    }

    damage_instance {
        damage 2+bonus_melee_damage //should be 4 damage total with 8 str on lenny
        type melee
        contact_requires_adjacency false
        ai_base_score 9999
    }
}
```

---

### `PteroEscape`
**Source:** `special_enemy_abilities.gon`  

```
PteroEscape {
    template throw_attack

    graphics {
        animation escape
        use_hit_alts false
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        max_range 4
        min_range 1
        restrictions none
        throw_consumed_character true
        prioritize_dont_change_direction true
        reorient_thrown_character true
        range_mode cross

    }
    
    damage_instance {
        damage 0
        blocked_damage 5
        ai_base_score 9999
    }
}
```

---

### `RaptorBabyBite`
**Source:** `special_enemy_abilities.gon`  

```
RaptorBabyBite {
    template melee_attack

    damage_instance {
        damage 5+bonus_melee_damage
        type melee

        effects {
            Bleed 1
            RefreshMovePointsIfHit 1
        }

        custom_additional_ai_weight avoid_redundant_debuffs
    }
}
```

---

### `AnkyloSwipe`
**Source:** `special_enemy_abilities.gon`  

```
AnkyloSwipe {
    template melee_attack

    graphics {
        animation tailwhip
    }

    sounds {
        ontrigger SE_AnkylosaurusAttack
    }
    
    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }

    damage_instance {
        knockback 10
        effects {
            Stun [1 .33]
        }
    }
}
```

---

### `AnkyloSpin`
**Source:** `special_enemy_abilities.gon`  

```
AnkyloSpin {
    template melee_attack

    graphics {
        animation singleSpin
    }

    sounds {
        ontrigger SE_AnkylosaurusAttack
    }
    
    cost {
        cantrip true
    }
    
    target {
        aoe_mode square
        knockback_mode character_to_tile
        prioritize_dont_change_direction 1
    }
    
    damage_instance {
        knockback 2
        effects {
            Bruise 1
        }
    }
}
```

---

### `MaelestesPickup`
**Source:** `special_enemy_abilities.gon`  

```
MaelestesPickup {
    template tile_targeted_melee_attack
    
    cost {
        cantrip true
    }
    
    target {
        restrictions [must_have_tag]
        target_requires_tag pickup
    }
    
    damage_instance {
        layer pickups
        damage 0
        effects {
            CollectsPickups 1
        }
    }
}
```

---

### `MaelestesSteal`
**Source:** `special_enemy_abilities.gon`  

```
MaelestesSteal {
    template melee_attack

    damage_instance {
        
        effects {
            StealEquipment any
        }
    }
}
```

---

### `Parasaurolophus_Push`
**Source:** `special_enemy_abilities.gon`  

```
Parasaurolophus_Push {
    variant_of BasicTankMelee

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            Conditional_AffectedByElement {
                element Water
                BonusCritChance 100
            } Else {
                Conditional_Speculative {
                    IgnoreDamage 1
                }
            }
        }
    }
}
```

---

### `Parasaurolophus_Gore`
**Source:** `special_enemy_abilities.gon`  

```
Parasaurolophus_Gore {
    template melee_attack

    graphics {
        animation headbuttUppercut
    }

    sounds {
        ontrigger SE_ParasaurolophusAttack
    }

    damage_instance {
        damage 3+bonus_melee_damage

        effects {
            KnockUpAndAway {
                stacks 3
                distance -3
            }

            Conditional_AffectedByElement {
                element Water
                BonusCritChance 100
                Conditional_Speculative {
                    IgnoreDamage 1
                }
            }
        }
    }
}
```

---

### `Parasaurolophus_Throw`
**Source:** `special_enemy_abilities.gon`  

```
Parasaurolophus_Throw {
    template throw_attack

    graphics {
        animation knockupatk
    }

    sounds {
        ontrigger SE_ParasaurolophusAttack
    }

    target {
        min_range 1
        max_range 4
        restrictions [must_be_empty aoe_must_exist]
        aoe_restrictions [tile_must_have_element]
        aoe_tile_requires_element Water
    }

    bonus_passives {
        TossTargetIsNotInWater 1
    }

    damage_instance {
        damage 3+bonus_melee_damage
        custom_additional_ai_weight toss_far
    }
}
```

---

### `TarBall`
**Source:** `special_enemy_abilities.gon`  

```
TarBall {
    template lobbed_attack

    target {
        min_range 1
        max_range 4
    }

    damage_instance {
        damage 1+bonus_ranged_damage
            
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

### `PrehistoricPooterShot`
**Source:** `special_enemy_abilities.gon`  

```
PrehistoricPooterShot {
    template lobbed_attack

    target {
        min_range 1
        max_range 2+bonus_range
    }

    damage_instance {
        knockback 3
        effects {
            Stun 1
        }
    }
}
```

---

### `BombFlyExplode`
**Source:** `special_enemy_abilities.gon`  

```
BombFlyExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation dying
    }
    
    cost {
        mana 5
    }
    
    target {
        knockback_mode character_to_tile
        aoe_excludes_self true
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 2
    }

    self_damage {
        piercing true
        cant_miss true
        effects {
            DeferVaporize 1
        }
    }
    
    damage_instance {
        damage 10
        knockback 1

        elements [
            Explosion
        ]
    }
}
```

---

### `MiniVolcano_Spurt`
**Source:** `special_enemy_abilities.gon`  

```
MiniVolcano_Spurt {
    template lobbed_attack

    graphics {
        projectile SmallRock
        animation shoot
        lob_height 2
        speed 5
    }

    target {
        range_mode 8cross
        min_range 0
        max_range 2
    }
    
    damage_instance {
        damage 3+bonus_ranged_damage

        effects {
            BounceObject {
                obj SmallLavaRock
                slide 10
            }
        }

        elements [
            Rock
            Fire
            Napalm
        ]
    }
}
```

---

### `DinoEggsSpawn`
**Source:** `special_enemy_abilities.gon`  

```
DinoEggsSpawn {
    template spawn
    
    graphics {
        lob true
        animation spawn
        dont_orient true
        dont_visualize_ai true
    }

    bonus_passives {
        AbilityEnabledPercentEachTurn 50%
    }
    
    
    target {
        max_range 1
        allow_any_orientation true
    }

    spawn {
        object RaptorBaby
        first_turn initiative
        faction self
    }
}
```

---

### `FatManLunge`
**Source:** `special_enemy_abilities.gon`  

```
FatManLunge {
    template dash_attack
    class FullyAnimatedDashAttackAbility
    
    graphics {
        animation slam
        sync_frames 34
    }
    
    cost {
        mana 0
    }
    
    target {
        max_range 1
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 10
    }
}
```

---

### `InvaderAttack`
**Source:** `special_enemy_abilities.gon`  

```
InvaderAttack {
    template melee_attack
    
    graphics {
        animation attack
    }
    
    target {
        multihit 2
    }
    
    damage_instance {
        damage 2+bonus_melee_damage

        effects {
            Poison 1
        }
    }
}
```

---

### `InvaderExplode`
**Source:** `special_enemy_abilities.gon`  

```
InvaderExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation none
    }
    
    cost {
        mana 5
    }
    
    target {
        knockback_mode character_to_tile
        aoe_excludes_self true
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 1
    }

    self_damage {
        piercing true
        cant_miss true
        effects {
            DeferVaporize 1
        }
    }
    
    damage_instance {
        damage 5
        knockback 1

        elements [
            Explosion
        ]
    }
}
```

---

### `SZBShoot`
**Source:** `special_enemy_abilities.gon`  

```
SZBShoot {
    template straightshot_attack

    graphics {
        projectile Bullet
        animation shoot
        empty_animation empty
        speed 25
        dont_visualize_ai true
    }
    
    cost {
        mana 0
        infcantrip true
        cant_cast 1-X
    }

    target {
        target_mode tile
        min_range 1
        max_range 20
        max_aoe 100

        max_targets -X //-1 means no target limit, if no ammo then X is 0
        X_is enable_if_has_ammo
    }

    self_damage {
        effects {
            Ammo -1
        }
    }

    damage_instance {
        damage 7+bonus_ranged_damage

        effects {
            Conditional_Speculative {
                RandomBonusDamage 25
            }
        }
    }
}
```

---

### `SZBReload`
**Name:** Reload  
**Source:** `special_enemy_abilities.gon`  

```
SZBReload {
    template self_buff
    
    meta {
        name "EABILITY_RELOAD_NAME"
    }

    graphics {
        animation reload
    }
    
    cost {
        cantrip true
    }
    
    damage_instance {
        effects {
            Ammo 3
            BackflipWhenTargeted {
                stacks 1
                ability SZBBackflipDodge
            }
            FormChange active
        }
        ai_base_score 10
    }
}
```

---

### `SZBBackflipDodge`
**Source:** `special_enemy_abilities.gon`  

```
SZBBackflipDodge {
    template jump_move

    graphics {
        full_jump_animation backflip
        full_jump_sync_frames 27
        full_jump_windup_frames 2

        dont_orient true
    }

    target {
        range_mode cross
        max_range 1
        restrictions [must_be_moveable must_move]
        allow_any_orientation true
    }
}
```

---

### `HangerBotAttack`
**Source:** `special_enemy_abilities.gon`  

```
HangerBotAttack {
    template melee_attack
    
    graphics {
        animation attack
    }
    
    damage_instance {
        damage 3+bonus_basic_spell_damage
        type spell
        makes_contact false

        effects {
            ShortCircuit 1
        }
        elements [
            Electric
        ]
    }
}
```

---

### `HangerBotSpawn`
**Source:** `special_enemy_abilities.gon`  

```
HangerBotSpawn {
    template spawn
    
    graphics {
        lob false
        animation spawn
    }

    target {
        max_range 1
    }

    spawn {
        object Invader
        ai_base_score 9999
        faction self
    }
}
```

---

### `HangerBotLeave`
**Source:** `special_enemy_abilities.gon`  

```
HangerBotLeave {
    template leave

    meta {
        is_move true
    }

    graphics {
        dont_visualize_ai true
    }

    cost {
        move_points 1
        act_points 0
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `HangerBotReturn`
**Source:** `special_enemy_abilities.gon`  

```
HangerBotReturn {
    template return

    meta {
        is_move true
    }

    graphics {
        dont_visualize_ai true
    }

    cost {
        move_points 1
        act_points 0
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `DoctorBotHeal`
**Source:** `special_enemy_abilities.gon`  

```
DoctorBotHeal {
    template melee_attack

    graphics {
        animation heal
    }
    
    cost {
        mana 0
    }

    target {
        multihit 3
    }
    
    damage_instance {
        heal 3

        effects {
            Conditional_HasCleansableDebuffs {
                PartialCleanse 1
                RandomStatusFromPool {
                    Brace 1
                    Thorns 1
                    DivineShield 1
                    KineticSpikes 1

                    DamageUp 1
                    DamageUp 1
                    ConstitutionUp 1
                    ConstitutionUp 1
                    SpeedUp 1
                    SpeedUp 1
                }
                GenericBuff 5 //for AI
            }
        }
    }
}
```

---

### `DoctorPickup`
**Source:** `special_enemy_abilities.gon`  

```
DoctorPickup {
    template tile_targeted_melee_attack

    graphics {
        animation loot
    }
    
    target {
        restrictions [must_have_tag]
        target_requires_tag pickup
    }
    
    damage_instance {
        layer pickups
        damage 0
        effects {
            ForceCollectsPickups 1
        }
        ai_base_score 999
    }
}
```

---

### `DoctorSpawn`
**Source:** `special_enemy_abilities.gon`  

```
DoctorSpawn {
    template spawn
    
    graphics {
        lob false
        animation spawn
    }

    target {
        max_range 1
    }

    spawn {
        object Invader
        ai_base_score 9999
        faction self
    }
}
```

---

### `JarHeadOrder`
**Name:** Befehl  
**Source:** `special_enemy_abilities.gon`  

```
JarHeadOrder {
    template tile_targeted_melee_attack

    meta {
        name "EABILITY_BEFEHL_NAME"
    }

    graphics {
        animation order
    }

    damage_instance {
        damage 0

        effects {
            TakeExtraTurn 1
        }
    }
}
```

---

### `JarHeadDeath`
**Source:** `special_enemy_abilities.gon`  

```
JarHeadDeath {
    template spell

    graphics {
        animation dying
        dont_orient true
        particle none
    }

    target {
        aoe_mode cross
        knockback_mode character_to_tile
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 1
    }

    damage_instance {
        damage 0
        type none

        effects {
            ChangeTile WaterTile
        }
    }
    splash_damage {
        damage 0
        type none

        effects {
            ChangeTile GlassTile
        }
    }
}
```

---

### `FetusJarDeath`
**Source:** `special_enemy_abilities.gon`  

```
FetusJarDeath {
    variant_of JarHeadDeath

    damage_instance {
        effects {
            SpeculativeMoveSelfCorpseOffMap 1
            ObjectOnHit FetusNoJar
        }
    }
}
```

---

### `FetusAirstrikeTrigger`
**Source:** `special_enemy_abilities.gon`  

```
FetusAirstrikeTrigger {
    template self_buff 

    graphics {
        animation dying
        dont_orient true
    }

    damage_instance {
        effects {
            DelayCastAbility {
                ability FetusAirstrike
                relative false
                lingering true
            }
        }
    }
}
```

---

### `FetusAirstrike`
**Source:** `special_enemy_abilities.gon`  

```
FetusAirstrike {
    template spell
    
    graphics { 
        dont_orient true

        pseudoprojectile RocketFromAbove
        particle Explosion
        animation RocketFromAbove
        delay 0
        //visual_delay_but_simultaneous_damage 10
    }
    
    cost {
        infcantrip true
        allow_offmap_casts true
        can_cast_while_dead true
    }
    
    target {
        lingering true
        aoe_mode standard
        knockback_mode character_to_tile
        
        target_mode tile
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 3
    }
    
    damage_instance {
        damage 8
        knockback 1

        elements [
            Explosion
            Fire
        ]
    }
}
```

---

### `FetusPullBomb`
**Source:** `special_enemy_abilities.gon`  

```
FetusPullBomb {
    template self_buff

    graphics { 
        dont_orient true
        animation pullremote
    }

    damage_instance {
        effects {
            FormChange {
                form "Bomb"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `FatCatBellyFlop`
**Name:** Lasagnefloppen  
**Source:** `special_enemy_abilities.gon`  

```
FatCatBellyFlop {
    template jump_attack

    meta {
        name "EABILITY_LASAGNEFLOPPEN_NAME"
    }

    graphics {
        jump_start_animation bellyflopStart
        air_animation bellyflop_air
        jump_attack_animation bellyflopEnd
        land_animation none
    }

    target {
        max_range 3

        min_aoe 0
        max_aoe 1
        aoe_mode square
        aoe_excludes_self false
        restrictions none
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `FutureBotPunch`
**Source:** `special_enemy_abilities.gon`  

```
FutureBotPunch {
    template melee_attack

    graphics {
        animation heaviestMelee
    }

    sounds {
        ontrigger SE_FuturebotPunch
    }

    damage_instance {
        damage 10+bonus_melee_damage
        type melee
    }
}
```

---

### `FutureBotPunchAggro`
**Name:** Ausführen  
**Source:** `special_enemy_abilities.gon`  

```
FutureBotPunchAggro {
    variant_of FutureBotPunch

    meta {
        name "EABILITY_FUTUREBOTEXECUTE_NAME"
    }

    target {
        restrictions aoe_must_exist
        aoe_restrictions must_have_aggro_target
    }
}
```

---

### `FutureBotSuplex`
**Name:** Bewegen  
**Source:** `special_enemy_abilities.gon`  

```
FutureBotSuplex {
    template melee_attack
    class SuplexAbility
    
    meta {
        name "EABILITY_BEWEGEN_NAME"
    }

    graphics {
        animation suplex
    }

    sounds {
        ontrigger SE_FuturebotSuplex
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
        damage 3+bonus_melee_ability_damage
        type melee
        blocked_multiplier 2
        makes_contact false
    }
}
```

---

### `TVOff`
**Source:** `special_enemy_abilities.gon`  

```
TVOff {
    template self_buff

    graphics { 
        dont_orient true
        animation turnOff
    }

    damage_instance {
        effects {
            FormChange Off
        }
        ai_base_score 9999
    }
}
```

---

### `TVChangeObey`
**Source:** `special_enemy_abilities.gon`  

```
TVChangeObey {
    template self_buff

    graphics { 
        animation changechannel
    }

    damage_instance {
        effects {
            FormChange Obey
        }
        custom_additional_ai_weight no_redundant_formchange
        ai_base_score 100
    }
}
```

---

### `TVChangeStop`
**Source:** `special_enemy_abilities.gon`  

```
TVChangeStop {
    variant_of TVChangeObey
    damage_instance {
        effects {
            FormChange Stop
        }
    }
}
```

---

### `TVChangeDumb`
**Source:** `special_enemy_abilities.gon`  

```
TVChangeDumb {
    variant_of TVChangeObey
    damage_instance {
        effects {
            FormChange Dumb
        }
    }
}
```

---

### `TVChangeDie`
**Source:** `special_enemy_abilities.gon`  

```
TVChangeDie {
    template spell

    graphics {
        particle none
        animation changechannel
    }

    target {
        target_mode none
        aoe_mode all
        aoe_excludes_self true
    }

    self_damage {
        effects {
            FormChange Die
        }
    }

    damage_instance {
        damage 0
        type status_spell
        cant_miss true

        effects {
            Conditional_Enemy {
                Doomed 1
            }
        }

        ai_base_score 100
    }
}
```

---

### `TallBotSuplex`
**Name:** Bewegen  
**Source:** `special_enemy_abilities.gon`  

```
TallBotSuplex {
    template melee_attack
    class SuplexAbility
    
    meta {
        name "EABILITY_BEWEGEN_NAME"
    }

    graphics {
        animation suplex
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
        damage 3+bonus_melee_ability_damage
        type melee
        blocked_multiplier 2
        makes_contact false

        effects {
            Stun [1 .5]
            Immobile [1 .5]
        }
    }
}
```

---

### `TallBotRocket`
**Name:** Blitzkrieg  
**Source:** `special_enemy_abilities.gon`  

```
TallBotRocket {
    template spell

    graphics {
        animation launch
        pseudoprojectile RocketFromAbove
        particle Explosion
    }

    meta {
        name "EABILITY_BLITZKRIEG_NAME"
    }

    cost {
        cantrip true
        prime 1
    }

    target {
        max_aoe 2

        min_range 1
        max_range 20
    }

    damage_instance {
        damage 8

        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `CancerMelee`
**Source:** `special_enemy_abilities.gon`  

```
CancerMelee {
    variant_of BasicMelee

    damage_instance {
        effects {
			ConstitutionUp -1
            SpreadDisease {
                chance 30%
                disease Cancer
            }
        }
    }
}
```

---

### `ShadeDuplicate`
**Source:** `special_enemy_abilities.gon`  

```
ShadeDuplicate {
    template spawn
    
    graphics {
        animation spawn
    }
    
    cost {
        cantrip true
    }

    target {
        max_range 1
    }

    spawn {
        object BoyShadeClone
        ai_base_score 9999
        faction self
    }
}
```

---

### `ToxGasBlast`
**Source:** `special_enemy_abilities.gon`  

```
ToxGasBlast {
    template spawn

    graphics {
        animation reflex
        lob true
        lob_height 0
        lob_yoff -.5
        animation spawn
    }

    target {
        knockback_mode back_orientation

        target_mode direction
        min_aoe 0
        max_aoe 1
        aoe_mode line
    }

    spawn {
        object GasCloud
        faction default
        first_turn initiative
        layer gas
    }
    self_damage {
        damage 0
        type spell
        knockback 3

        effects {
            KnockbackDamageImmuneUntilSettled 1
        }
    }
}
```

---

### `SpawnGasAOE`
**Source:** `special_enemy_abilities.gon`  

```
SpawnGasAOE {
    template spawn

    cost {
        //prime 1
        cantrip true
    }

    graphics {
        lob true
        lob_height 0
        lob_yoff -.5
        animation spawn
    }

    spawn {
        object GasCloud
        faction default
        first_turn initiative
        layer gas
    }

    target {
        target_mode none
        max_aoe 1
        //aoe_excludes_self true
        prioritize_dont_change_direction true
    }
}
```

---

### `ToxPuff`
**Source:** `special_enemy_abilities.gon`  

```
ToxPuff {
    template self_buff
    
    graphics { 
        animation puff
    }

    damage_instance {
        heal 999

        effects {
            FormChange {
                form "Explody"
            }
        }
    }
}
```

---

### `ToxExplode`
**Source:** `special_enemy_abilities.gon`  

```
ToxExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle none
        animation explode
    }
    
    cost {
        mana 5
    }
    
    target {
        knockback_mode character_to_tile
        prioritize_dont_change_direction true
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 1
        max_aoe 2
    }

    self_damage {
        piercing true
        cant_miss true
        effects {
            DeferVaporize 1
        }
    }

    damage_instance {
        damage 5
        knockback 1

        effects {
            DustOnHit {
                object GasCloud
            }
        }

        elements [
            Explosion
        ]

    }
}
```

---

### `FloastPull`
**Source:** `special_enemy_abilities.gon`  

```
FloastPull {
    template straightshot_attack

    target {
        max_aoe 10

        knockback_mode pull_to_character
    }

    graphics {
        animation shoot

        projectile Froghook
        chain_movieclip Frogchain
        chain_distance .25
    }
    
    damage_instance {
        damage 3+bonus_ranged_damage

        effects {
             PullSourceToKnockbackImmuneTarget 1
        }
    }
}
```

---

### `FloastThrow`
**Name:** Maul  
**Source:** `special_enemy_abilities.gon`  

```
FloastThrow {
    template throw_attack
    
    meta {
        name "EABILITY_MAUL_NAME"
    }

    graphics {
        animation throw
        use_placeholder true
        face_toss_target true
        dont_visualize_ai true
    }

    target {
        max_range 10
        min_range 1
        restrictions none
        range_mode square
        toss_direction_restriction forwards
    }
    
    damage_instance {
        damage 8+bonus_melee_damage
        custom_additional_ai_weight toss_farthest

        effects {
            Bruise 1
            Confusion 1
        }
    }
}
```

---

### `FloastSpawn`
**Source:** `special_enemy_abilities.gon`  

```
FloastSpawn {
    template spawn

    graphics {
        lob true
        animation spawn
    }

    target {
        max_range 3
    }

    spawn {
        object Fly
        faction self
    }
}
```

---

### `CollectiveSpinImpl`
**Source:** `special_enemy_abilities.gon`  

```
CollectiveSpinImpl {
    template melee_attack

    graphics {
        animation singleSpin
    }

    target {
        target_mode none
        max_aoe 1
        aoe_mode standard
    }

    damage_instance {
        damage 4+bonus_melee_damage
    }
}
```

---

### `CollectiveSpin`
**Source:** `special_enemy_abilities.gon`  

```
CollectiveSpin {
    template self_buff
    sub_ability CollectiveSpinImpl
    ai_ability CollectiveSpinImpl
    
    graphics {
        animation none
    }

    target {
        aoe_hint_teamcast true
    }
    
    damage_instance {
        effects {
            TeamCastAbility {
                ability CollectiveSpinImpl
                tag_restriction collective
            }
        }
    }
}
```

---

### `CollectiveCounterImpl_ai`
**Source:** `special_enemy_abilities.gon`  

```
CollectiveCounterImpl_ai {
    template melee_attack

    target { 
        aoe_considers_character_size true
        aoe_mode cone
        max_aoe 20
        min_aoe 2
        aoe_leading_edge_only true
    }
}
```

---

### `CollectiveCounterImpl`
**Source:** `special_enemy_abilities.gon`  

```
CollectiveCounterImpl {
    template melee_attack

    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `CollectiveCounter`
**Source:** `special_enemy_abilities.gon`  

```
CollectiveCounter {
    template self_buff
    sub_ability CollectiveCounterImpl
    ai_ability CollectiveCounterImpl_ai
    
    graphics {
        animation none
    }

    target {
        aoe_hint_teamcast true
    }
    
    damage_instance {
        effects {
            TeamCastAbility {
                ability CollectiveCounterImpl
                tag_restriction collective
                same_orientation true
            }
        }
    }
}
```

---

### `SCSneakUp`
**Source:** `special_enemy_abilities.gon`  

```
SCSneakUp {
    template teleport

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    target {
        target_mode random_tile
        max_range 20
        restrictions [must_be_moveable must_be_directly_behind_enemy]
    }
}
```

---

### `SCAttack`
**Source:** `special_enemy_abilities.gon`  

```
SCAttack {
    variant_of BasicMelee

    damage_instance {
        effects {
            ForceMoveAway 1
            Conditional_Backstab {
                BonusCritChance 100
                Fear 1
            }
        }
    }
}
```

---

### `CancerExplode`
**Source:** `special_enemy_abilities.gon`  

```
CancerExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation blowUp
    }
    
    cost {
        mana 5
    }
    
    target {
        knockback_mode character_to_tile
        aoe_excludes_self true
        
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 1
        max_aoe 2
    }

    self_damage {
        piercing true
        cant_miss true
        effects {
            DeferVaporize 1
            SpeculativeMoveSelfCorpseOffMap 1
            ObjectOnHit Carcus
        }
    }
    
    damage_instance {
        damage 5
        knockback 1

        effects {
            DustOnHit {
                object GasCloud
            }
        }

        elements [
            Explosion
        ]
    }
}
```

---

### `GorgerGorge`
**Source:** `special_enemy_abilities.gon`  

```
GorgerGorge {
    template melee_attack
    class MeleeEatAbility

    graphics {
        animation consume
    }

    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[2, 0]]
        aoe_considers_character_size false
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true

        effects {
            Vaporize 20
            FlatLeech 10
        }
    }
}
```

---

### `GorgerRun`
**Source:** `special_enemy_abilities.gon`  

```
GorgerRun {
    template move

    cost {
        act_points 1
        move_points 1
    }

    graphics {
        animation run
        speed 1.5
    }

    target {
        max_range 6
    }
}
```

---

### `SlagSpawn`
**Source:** `special_enemy_abilities.gon`  

```
SlagSpawn {
    template spawn

    graphics {
        lob true
        animation spawn
    }

    target {
        target_mode direction
        aoe_mode line
        min_aoe 1
        max_aoe 1
        max_targets 1
        restrictions aoe_must_exist
        aoe_considers_character_size true
        aoe_excludes_self true
        range_excludes_blocking false
    }

    spawn {
        object FlySwarm
        faction self
    }
}
```

---

### `SlagBoner`
**Name:** Bone Shot  
**Source:** `special_enemy_abilities.gon`  

```
SlagBoner {
    template lobbed_attack
    
    meta {
        name "EABILITY_BONESHOT_NAME"
    }

    graphics {
        lob_height 3
        projectile BoneProjectile
        use_rotation false
        min_range 1
        max_range 3
    }

    target {
        max_aoe 1
    }

    damage_instance {
        effects {
            Bruise 1
        }
    }
}
```

---

### `QueenHippoAttack`
**Source:** `special_enemy_abilities.gon`  

```
QueenHippoAttack {
    template melee_attack

    damage_instance {
        damage 4+bonus_melee_damage
        knockback 3
        type melee

        effects {
            Bruise 1
            OverrideChainKnockback 3
        }
    }
}
```

---

### `QueenHippoUppercut`
**Source:** `special_enemy_abilities.gon`  

```
QueenHippoUppercut {
    template melee_attack

    graphics {
        animation uppercut
    }

    cost {
        cantrip true
    }

    damage_instance {
        damage 4+bonus_melee_damage
        
        effects {
            //Immobile 1
            KnockUpAndAway {
                distance 2
            }
        }
    }
}
```

---

### `QueenHippoTire`
**Source:** `special_enemy_abilities.gon`  

```
QueenHippoTire {
    template self_buff

    graphics {
        animation breathing
    }

    cost {
        cantrip true
    }

    target {
        prioritize_face_camera true
    }

    damage_instance {
        ai_base_score 999999

        effects {
            RemoveStatusStacks {
                status Brace
                stacks 1
            }
            MovementUp 1
        }
    }
}
```

---

### `QueenHippoHeartAttack`
**Source:** `special_enemy_abilities.gon`  

```
QueenHippoHeartAttack {
    template self_buff

    graphics {
        animation heartattack
    }

    cost {
        cantrip true
    }

    damage_instance {
        ai_base_score 999999

        effects {
            DieViaAbilityInternally 1
        }
    }
}
```

---

### `TrampyDump`
**Name:** Dump  
**Source:** `special_enemy_abilities.gon`  

```
TrampyDump {
    template melee_attack

    meta {
        name "EABILITY_DUMP_NAME"
    }

    graphics {
        animation poop
    }

    target {
        target_mode direction
        
        aoe_mode line
        min_aoe 1
        max_aoe 1
        knockback_mode orientation

        restrictions [aoe_must_be_displaceable aoe_must_exist]
    }

    damage_instance {
        damage 0
        cant_miss true

        effects {
            Displace 1
            Poison 2
            ObjectOnHit {
                object Poop
            }
        }
        ai_base_score 999999
    }

    /*self_damage {
        damage 0
        type spell
        knockback -3
    }*/
}
```

---

### `TrampySpit`
**Name:** Loogie  
**Source:** `special_enemy_abilities.gon`  

```
TrampySpit {
    template lobbed_attack

    meta {
        name "EABILITY_LOOGIE_NAME"
    }

    graphics {
        animation shoot
		projectile spitprojectile
    }

    target {
        min_range 2
        max_range 3
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Blind 2
            Slow 2
        }
    }
}
```

---

### `TrampyFleas`
**Source:** `special_enemy_abilities.gon`  

```
TrampyFleas {
    template spawn

    graphics {
        lob true
        animation scratch
    }

    target {
        target_mode none    
        max_aoe 1
        max_targets 2
        multihit 2
        stagger_multihit_targets true
    }

    spawn {
        object Flea
        faction self
    }
}
```

---

### `TrampySleep`
**Source:** `special_enemy_abilities.gon`  

```
TrampySleep {
    template self_buff

    graphics {
        animation none
    }

    damage_instance {
        heal 15

        effects {
            Sleep 3
        }
    }
}
```

---

### `TrampyDrink`
**Source:** `special_enemy_abilities.gon`  

```
TrampyDrink {
    template lobbed_attack

    graphics {
		projectile Bottleshot
        animation drink
        first_castpoint_is_self_damage_only true
    }

    target {
        multihit 2
    }

    self_damage {
        heal 5
        cant_miss true

        effects {
            Conditional_InForm {
                form Default

                SpeedUp 1
                DamageUp 1
                DodgeChance_Status 20
                CritChanceUp 20

                FormChange Drunker
            } Else {
                SpeedUp 1
                DamageUp 1
                DodgeChance_Status 5
                CritChanceUp 5
            }
        }
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            ChangeTile GlassTile
        }
    }
}
```

---

### `RatKingToss`
**Name:** Toss  
**Source:** `special_enemy_abilities.gon`  

```
RatKingToss {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        animation throw
        use_placeholder true
        face_toss_target true
        dont_visualize_ai true
    }
    
    target {
        max_range 10
        min_range 2
        restrictions none
        range_mode cross
        toss_direction_restriction forwards
    }
    
    damage_instance {
        damage 6+bonus_melee_damage
        custom_additional_ai_weight toss_farthest
    }
}
```

---

### `RatKingSpawn`
**Source:** `special_enemy_abilities.gon`  

```
RatKingSpawn {
    template spawn

    graphics {
        lob true
        animation shoot
    }

    target {
        target_mode direction
        aoe_mode line
        min_aoe 1
        max_aoe 1
        restrictions aoe_must_exist
        aoe_considers_character_size true
        aoe_excludes_self true
        range_excludes_blocking false
    }

    spawn {
        object Rat
        faction self
    }
}
```

---

### `RatKingDash`
**Name:** Dash  
**Source:** `special_enemy_abilities.gon`  

```
RatKingDash {
    template dash_attack
    
    meta {
        name "EABILITY_DASH_NAME"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_attack_animation dashend
    }
    
    cost {
        mana 5
    }
    
    target {

    }
    
    damage_instance {
        damage 7+bonus_melee_damage
        knockback 4
    }
}
```

---

### `RatKing2Spawn`
**Source:** `special_enemy_abilities.gon`  

```
RatKing2Spawn {
    template spawn

    graphics {
        lob true
        animation shoot
    }

    cost {
        cantrip true
    }

    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[-1 0]]
        knockback_mode none
        aoe_considers_character_size true
        aoe_excludes_self true
        range_excludes_blocking false
        restrictions aoe_must_exist
        min_targets 1
        max_targets 2
        prioritize_dont_change_direction true
    }

    spawn {
        object [Pinky Dip Poop]
        faction self
    }
}
```

---

### `RatKingTransform`
**Source:** `special_enemy_abilities.gon`  

```
RatKingTransform {
    template self_buff

    graphics {
        animation transform
    }

    damage_instance {
        effects {
            FormChange HalfDead
            DamageUp 3
            MovementUp 2
            Brace 1
        }
    }
}
```

---

### `DybbukBackflipDodge`
**Source:** `special_enemy_abilities.gon`  

```
DybbukBackflipDodge {
    template jump_move

    graphics {
        full_jump_animation backflip
        full_jump_sync_frames 27

        dont_orient true
    }

    target {
        range_mode cross
        max_range 1
        restrictions [must_be_moveable must_move]
        allow_any_orientation true
    }
}
```

---

### `DybbukEscape`
**Source:** `special_enemy_abilities.gon`  

```
DybbukEscape {
    template jump_move

    graphics {
        full_jump_animation backflip
        full_jump_sync_frames 27

        dont_orient true
    }

    bonus_passives {
        AbilityEnabledOncePerFightAtHealthThreshold 50%
        AbilityEnabledIfMovementTrapped 1
    }

    target {
        min_range 2
        max_range 5
        restrictions [must_be_moveable must_move]
    }
}
```

---

### `DybbukPossess`
**Name:** Possess  
**Source:** `special_enemy_abilities.gon`  

```
DybbukPossess {
    template jump_attack

    meta {
        name "EABILITY_POSSESS_NAME"
    }

    graphics {
        full_jump_animation possess
        full_jump_sync_frames 65
        full_jump_windup_frames 72 
    }

    cost {
        cantrip true
    }

    target {
        remain_off_map true

        aoe_excludes_self false
        max_aoe 0
        min_aoe 0

        max_range 20
        restrictions must_have_cat
    }

    self_damage {
        effects {
            Cleanse 0
            FormChange Possessing
        }
    }

    damage_instance {
        damage 0
        cant_miss true
        type spell
        makes_contact false

        effects {
            IgnoreSelf 1

            Conditional_Speculative {
            } Else { //just dont want the AI considering any of this
                PurgeAll 1
                Revive 100%
                FullHeal 1
                DybbukPossessed {
                    exit_ability DybbukReturn
                    punch_self_ability Dybbuk_StopHittingYourself
                }

                CatPartsTransform {
                    //palette 999
                    mouth 1069
                    eye1 1069
                    eye2 1069
                    eyebrow1 1069
                    eyebrow2 1070
                    palette 86
                }
            }
        }

        custom_additional_ai_weight dybbuk_possession
    }
}
```

---

### `DybbukRePossess`
**Source:** `special_enemy_abilities.gon`  

```
DybbukRePossess { //copy of dybbukposses without the heal
    variant_of DybbukPossess

    damage_instance {
        effects {
            Conditional_Speculative {
            } Else {
                Revive 1
                FullHeal 0
            }
        }
    }
}
```

---

### `DybbukReturn`
**Name:** Return  
**Source:** `special_enemy_abilities.gon`  

```
DybbukReturn {
    template jump_move

    meta {
        name "EABILITY_RETURN_NAME"
    }

    cost {
        allow_offmap_casts true
    }

    graphics {
        full_jump_animation depossess
        full_jump_sync_frames 37
    }

    target {
        max_aoe 0
        min_aoe 0

        max_range 20
        
    }

    self_damage {
        effects {
            Cleanse 0

            Conditional_HasStatus {
                status DybbukManualExitTag
                FormChange Bully
            } Else {
                FormChange LastHit
            }
        }
    }
}
```

---

### `DybbukReanimate`
**Name:** Reanimate  
**Source:** `special_enemy_abilities.gon`  

```
DybbukReanimate {
    template targeted_status
    
    meta {
        name "EABILITY_REANIMATE_NAME"
    }

    graphics {
        animation zombie
    }

    target {
        min_range 1
        max_range 3
        max_aoe 0
        aoe_restrictions must_have_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        effects {
            Reanimate 100%
        }
    }
}
```

---

### `DybbukWisps`
**Source:** `special_enemy_abilities.gon`  

```
DybbukWisps {
    template spawn

    graphics {
        lob true
        animation wisps
    }

    target {
        target_mode none    
        max_aoe 1
        max_targets 2
        multihit 2
        stagger_multihit_targets true
    }

    spawn {
        object Wisp
        faction self
    }
}
```

---

### `DybbukLick`
**Source:** `special_enemy_abilities.gon`  

```
DybbukLick {
    template melee_attack

    damage_instance {
        effects {
            ManaSteal -1
        }
    }
}
```

---

### `HitlerCloneTransform`
**Source:** `special_enemy_abilities.gon`  

```
HitlerCloneTransform {
    template self_buff

    graphics {
        animation transform
    }

    damage_instance {
        effects {
            FormChange Grown
            Cleanse 0
            InstantMaxHealthUp 20
            FullHeal 1
            FaceCamera 1
        }
        ai_base_score 999999
    }
}
```

---

### `HitlerCloneSwipes`
**Name:** Führer Swipes  
**Source:** `special_enemy_abilities.gon`  

```
HitlerCloneSwipes {
    variant_of BasicMelee

    meta {
        name "EABILITY_HITLERSWIPES_NAME"
        animate_name true
    }

    target {
        multihit 5
    }

    damage_instance {
        damage 1+bonus_melee_damage
    }
}
```

---

### `HitlerCloneLick`
**Source:** `special_enemy_abilities.gon`  

```
HitlerCloneLick {
    template self_buff

    graphics {
        animation lick
    }

    damage_instance {
        heal 7

        effects {
            Cleanse 0
        }
    }
}
```

---

### `HitlerShoot`
**Source:** `special_enemy_abilities.gon`  

```
HitlerShoot {
    template lobbed_attack

    target {
        max_range 20
        min_range 1
    }

    graphics {
        projectile Bullet
        animation shoot
        lob_height 0
        speed 25
    }
    
    damage_instance {
        damage 5+bonus_ranged_damage


        effects {
            Conditional_HasTag {
                tag hitler_clone

                MergeDamageInstance {
                    can_instapop false
                    force_no_hit_animation true
                }

                SetAnimationAlts {
                    dying shot
                    dead deadShot
                }
                Instakill 25
            }
        }
    }
}
```

---

### `GooseStep`
**Source:** `special_enemy_abilities.gon`  

```
GooseStep {
    variant_of DefaultMove

    damage_instance {
        damage 3
        override_trample_damage true

        effects {
            SetDistanceDisplace 5
        }
    }
}
```

---

### `HitlerCloneHeil`
**Source:** `special_enemy_abilities.gon`  

```
HitlerCloneHeil {
    template self_buff

    graphics {
        animation heil
    }

    damage_instance {
        effects {
            SpeedUp 1
            DamageUp 1
        }
        ai_base_score 999999
    }
}
```

---

### `HitlerHeil`
**Source:** `special_enemy_abilities.gon`  

```
HitlerHeil {
    template spell

    graphics {
        particle none
        animation heil
        dont_visualize_ai true
    }

    target { 
        target_mode none
        max_aoe 20

        aoe_restrictions [must_have_tag must_have_living_character]
        target_requires_tag hitler_clone
        knockback_mode tile_to_character
    }
    
    damage_instance {
        damage 0
        cant_miss true
        type status_spell

        effects {
            Conditional_HasTag {
                tag grown_hitler_clone
                FaceAway 1
                ImmediateUseAbility HitlerCloneHeil
            }
            Conditional_HasTag {
                tag hitler_clone_fetus
                ImmediateUseAbility HitlerCloneTransform
            }
        }

        ai_base_score 999999
    }
}
```

---

### `HitlerHeadGrowA`
**Source:** `special_enemy_abilities.gon`  

```
HitlerHeadGrowA {
    template spell

    graphics {
        particle none
        animation yell1
        dont_visualize_ai true
    }

    target { 
        target_mode none
        max_aoe 20

        aoe_restrictions [must_have_tag must_have_living_character]
        target_requires_tag hitler_clone_fetus
        max_targets 2
    }
    
    damage_instance {
        damage 0
        cant_miss true
        type status_spell

        effects {
            ImmediateUseAbility HitlerCloneTransform
        }
    }
}
```

---

### `HitlerHeadGrowB`
**Source:** `special_enemy_abilities.gon`  

```
HitlerHeadGrowB {
    variant_of HitlerHeadGrowA
    graphics {
        animation yell2
    }
}
```

---

### `HitlerHeadTransform`
**Source:** `special_enemy_abilities.gon`  

```
HitlerHeadTransform {
    template self_buff
    chain_ability HitlerHeadTransform_Chain

    cost {
        cant_cast X
    }
    target {
        X_is custom
    }
    bonus_passives {
        XIsLivingAlliesWithTag hitler_clone_fetus
    }

    graphics {
        animation yell3
    }
}
```

---

### `HitlerHeadTransform_Chain`
**Source:** `special_enemy_abilities.gon`  

```
HitlerHeadTransform_Chain {
    template self_buff

    graphics {
        animation transform
    }

    damage_instance {
        effects {
            TransformNow Hitler
        }
    }
}
```

---

### `HitlerSuicide`
**Source:** `special_enemy_abilities.gon`  

```
HitlerSuicide {
    template melee_attack

    graphics {
        animation suicide
    }
    target {
        target_mode none
        min_range 0
        max_range 0
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        aoe_mode standard
        multihit 2
    }

    damage_instance {
        damage 0
        type status_spell
        cant_miss true

        effects {
            Conditional_LastHit {
                DelayCastAbility HitlerNuke
            } Else {
                Cleanse 0
                FaceCamera 1
                ShowFakeDamage {
                    stacks 999
                    style [crit]
                }
                SetHealth 1
                SetShield 88
                FormChange Nuke
                RemoveTurnsThisRound 1
            }
        }
    }
}
```

---

### `HitlerNuke`
**Name:** Nuke  
**Source:** `special_enemy_abilities.gon`  

```
HitlerNuke {
    template spell

    meta {
        name "EABILITY_NUKE_NAME"
    }

    graphics {
        animation detonate
        particle Explosion
        delay 5
        dont_visualize_ai true
    }

    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_piercing_line_of_sight
    }

    self_damage {
        damage 0
        piercing true
        effects {
            DeferVaporize 1
        }

        elements [
            Explosion
        ]
    }

    damage_instance {
        damage 50

        effects {
            CorpseVaporizer 1 //kills any corpses it hits, characters leave no corpses
        }

        elements [
            Explosion
        ]
    }
}
```

---

### `HuskSwipes`
**Source:** `special_enemy_abilities.gon`  

```
HuskSwipes {
    class MultiHitMeleeAttackAbility
    template melee_attack

    graphics {
        start attack
        loop attack
        end attack
    }

    target {
        multihit X
        X_is custom
    }

    bonus_passives {
        XIsLivingCharactersWithTag husk
    }
    
    damage_instance {
        damage 3+bonus_melee_damage
    }
}
```

---

### `TumorPrisonDeathrattle`
**Source:** `special_enemy_abilities.gon`  

```
TumorPrisonDeathrattle {
    template ranged_attack

    graphics {
        animation dying
    }

    target {
        min_range 0
        max_range 1
        restrictions none
    }

    self_damage {
        effects {
            Conditional_AbilityTargetIsSelf {
            } Else {
                SpeculativeMoveSelfCorpseOffMap 1
            }
        }
    }

    damage_instance {
        damage 0

        effects {
            Imprison Tumor
        }
    }
}
```

---

### `CHuskGrab`
**Source:** `special_enemy_abilities.gon`  

```
CHuskGrab {
    template targeted_status

    graphics {
        animation grab
    }

    target {
        max_range 1
        range_mode cross
        restrictions [must_have_cat must_have_living_character]
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                instant true
                mount_mode true
                force_contact true
                drop_on_death true
                drop_on_self_death true
                do_not_pop_corpse true
                struggle_ability CHuskStruggle
            }
            GenericDebuff 1 //for AI
        }

        ai_base_score 999999
    }
}
```

---

### `CHuskDrop`
**Source:** `special_enemy_abilities.gon`  

```
CHuskDrop {
    template throw_attack

    graphics {
        animation escape
        use_hit_alts false
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        max_range 7
        min_range 2
        restrictions none
        throw_consumed_character true
        prioritize_dont_change_direction true
        reorient_thrown_character true
        range_mode cross

    }
    
    damage_instance {
        damage 0
        ai_base_score 9999
    }
}
```

---

### `CHuskDropFail`
**Source:** `special_enemy_abilities.gon`  

```
CHuskDropFail {
    template self_buff
    class DamageConsumedCharactersAbility

    cost {

    }

    graphics {
        animation struggle
    }
    
    
    target {
        target_mode none
        knockback_mode none
        prioritize_dont_change_direction true
    }

    damage_instance {
        damage 1+bonus_melee_damage
        type melee
        contact_requires_adjacency false
        ai_base_score 9999
    }
}
```

---

### `CHuskBone`
**Source:** `special_enemy_abilities.gon`  

```
CHuskBone {
    template straightshot_attack

    graphics {
        animation shoot
        projectile BoneProjectile
        use_rotation false
    }

    target {
        max_aoe 4
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Bruise 1
        }
    }
}
```

---

### `CHuskCatShade`
**Source:** `special_enemy_abilities.gon`  

```
CHuskCatShade {
    template spawn

    tags [summon]
    
    graphics {
        lob true
        animation use
    }

    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object PlayerCat_HuskShade
        first_turn next_turn
        faction self

        catdata clone_consumed
        clone_items true

        additional_passives {
            SafeDoomed 1
            InjuryImmunity 1
        }
    }
}
```

---

### `Metronome_Enemy`
**Source:** `special_enemy_abilities.gon`  

```
Metronome_Enemy {
    variant_of Metronome

    cost {
        infcantrip false
        cantrip true
    }
    damage_instance {
        ai_base_score 999999

        effects {
            Metronome {
                stacks 1
                banned_abilities [BatteryNuke WeAreOne Metronome SmartMetronome BecomeEntropy ForbiddenFamine]
            }
        }
    }
}
```

---

### `PsychicChoke_Enemy`
**Source:** `special_enemy_abilities.gon`  

```
PsychicChoke_Enemy {
    variant_of PsychicChoke

    cost {
        infcantrip false
        cantrip true
    }
}
```

---

### `PsychicCatBackflip`
**Name:** Predict  
**Source:** `special_enemy_abilities.gon`  

```
PsychicCatBackflip {
    template self_buff
    
    meta {
        name "EABILITY_PREDICT_NAME"
    }

    cost {
        cantrip true
    }

    damage_instance {
        effects {
            BackflipWhenTargeted {
                stacks 1
                ability Teleport
            }
        }
        ai_base_score 999999
    }
}
```

---

### `DruidCatBasic`
**Name:** Sing  
**Description:** Heal and give +1 Temporary Damage to units in a wide area.  
**Source:** `special_enemy_abilities.gon`  

```
DruidCatBasic {
    template spell
    
    meta {
        name "ABILITY_DRUIDSING_NAME"
        desc "ABILITY_DRUIDSING_DESC"
        animate_name false
        class Druid
    }
    tags [musical]

    graphics {
        animation sing3
        particle None
    }

    target { 
        max_aoe 2
        max_range 5+bonus_range
        aoe_excludes_self true
    }

    damage_instance {
        heal 3
        cant_miss true

        effects {
            DamageUp 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `DCSquirrelForm`
**Name:** Form of the Squirrel  
**Source:** `special_enemy_abilities.gon`  

```
DCSquirrelForm {
    template self_buff
    
    meta {
        name "ABILITY_SQUIRRELFORM_NAME"
    }

    tags [shapeshift summon]

    graphics {
        animation druidTransform
    }
    
    cost {
        cantrip true
        cant_cast X
    }

    target {
        X_is custom
    }

    bonus_passives {
        XIsLivingAlliesWithTag dc_crow
    }
    
    damage_instance {
        effects {
            FormChange SquirrelForm

            CatPartsTransform {
                mouth 1071
                tail 1042
                ear1 1036
                ear2 1036
            }
        }
        ai_base_score 999999
    }
}
```

---

### `DCBirthSquirrel`
**Source:** `special_enemy_abilities.gon`  

```
DCBirthSquirrel {
    variant_of BirthSquirrel

    cost {
        infcantrip false
        cantrip true
    }
}
```

---

### `MCMonkStyleChange`
**Source:** `special_enemy_abilities.gon`  

```
MCMonkStyleChange {
    template self_buff

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
        ai_base_score 999999
    }
}
```

---

### `DCAeroblast`
**Source:** `special_enemy_abilities.gon`  

```
DCAeroblast {
    variant_of CrowFlap

    cost {
        infcantrip false
        cantrip true
    }
}
```

---

### `NCReanimate`
**Source:** `special_enemy_abilities.gon`  

```
NCReanimate {
    variant_of Reanimate
    
    cost {
        infcantrip false
        cantrip false
        act_points 1
    }

    target {
        max_range 3
    }

    damage_instance {
        effects {
            Reanimate 100%
        }
        ai_base_score 999999
    }
}
```

---

### `NCGravecrawl`
**Source:** `special_enemy_abilities.gon`  

```
NCGravecrawl {
    variant_of Gravecrawl
    
    cost {
        infcantrip false
        cantrip false
        act_points 1
    }

    damage_instance {
        ai_base_score 999999
    }
}
```

---

### `GSSuck`
**Source:** `special_enemy_abilities.gon`  

```
GSSuck {
    template straightshot_attack
    chain_ability GSChew

    graphics {
        animation suck
        projectile None
    }

    cost {
        mana 0
        must_not_be_consuming true
    }

    target {
        max_aoe 10
        knockback_mode none
        aoe_restrictions must_have_cat
    }

    damage_instance {
        type none
        damage 0
        cant_miss true
        layer characters

        effects {
            Consumed {
                mount_mode true
                struggle_ability Thrash
            }
        }

        elements [
            Wind
        ]
    }
}
```

---

### `GSChew`
**Source:** `special_enemy_abilities.gon`  

```
GSChew {
    template self_buff
    class DamageConsumedCharactersAbility
    chain_ability GSSpit

    graphics {
        animation chew
    }

    target {
        target_mode none
        knockback_mode none
        prioritize_dont_change_direction true
        multihit 2
    }

    damage_instance {
        damage 2+bonus_melee_damage //should be 4 damage total with 8 str on lenny
        type melee
        contact_requires_adjacency false

        effects {
            Bruise 1
            Bleed 1
        }
    }
}
```

---

### `GSSpit`
**Source:** `special_enemy_abilities.gon`  

```
GSSpit {
    template throw_attack

    graphics {
        animation spit
    }

    cost {
        mana 0
        must_be_consuming true
    }
    
    target {
        target_mode random_farthest_tile
        max_range 10
        min_range 3
        range_mode cross
        restrictions must_match_current_orientation
        throw_consumed_character true
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage
        blocked_damage 5+bonus_melee_ability_damage
        ai_base_score 9999

        custom_additional_ai_weight toss_far
    }
}
```

---

### `GSOpen`
**Source:** `special_enemy_abilities.gon`  

```
GSOpen {
    template self_buff

    graphics {
        animation open
    }

    damage_instance {
        effects {
            FormChange Open
        }
    }
}
```

---

### `GSClosedAttack`
**Source:** `special_enemy_abilities.gon`  

```
GSClosedAttack {
    template melee_attack

    damage_instance {
        knockback 10
        effects {
            Bleed 1
        }
    }
}
```

---

### `GSOpenAttack`
**Source:** `special_enemy_abilities.gon`  

```
GSOpenAttack {
    template melee_attack

    damage_instance {
        //nothing on the counter
    }
}
```

---

### `GSScream`
**Source:** `special_enemy_abilities.gon`  

```
GSScream {
    template spell
    ai_ability MegafetusMelee_ai

    graphics {
        particle none
        animation shriek
    }

    target {
        target_mode direction
        aoe_mode circle
        max_aoe 3
        aoe_excludes_self true
    }

    damage_instance {
        damage 0
        ai_base_score 999999

        effects {
            Fear 1
        }
    }
}
```

---

### `TCMechSuit`
**Source:** `special_enemy_abilities.gon`  

```
TCMechSuit {
    variant_of MechSuit

    damage_instance {
        ai_base_score 999999
    }

    cost {
      //  mana 0
    }

    spawn {
        object TCMechSuit
    }
}
```

---

### `TCCatBot`
**Source:** `special_enemy_abilities.gon`  

```
TCCatBot {
    variant_of Catbot

    cost {
        infcantrip false
        cantrip true
        requires_destructible_weapon true
    }
}
```

---

### `MCMelee`
**Source:** `special_enemy_abilities.gon`  

```
MCMelee {
    template melee_attack
    
    graphics {
        animation monkAttack
    }

    target { 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable //TODO: MAKE THIS WORK PROPERLY IF ENLARGED
    }

    /*temporary_effects {
        CastAgain 1
    }*/

    damage_instance {
        damage "(5+bonus_melee_damage+1)/2"

        effects {
            Bruise 1
        }
    }
}
```

---

### `MCHadouken`
**Source:** `special_enemy_abilities.gon`  

```
MCHadouken {
    variant_of Hadouken

    damage_instance {
        damage 8
    }
}
```

---

### `MCKineticCharge`
**Name:** Kinetic Charge  
**Source:** `special_enemy_abilities.gon`  

```
MCKineticCharge {
    template self_buff
    
    meta {
        name "ABILITY_KINETICCHARGE_NAME"
    }

    graphics {
        animation flex
    }

    damage_instance {
        damage 0

        effects {
            KineticSpikes 1
        }
    }
}
```

---

### `GrenadeExplode`
**Source:** `special_enemy_abilities.gon`  

```
GrenadeExplode {
    template spell
    
    graphics { 
        dont_orient true
        particle Explosion
        animation explode
        delay 2

        animation dying
        dont_visualize_ai true
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode standard
        knockback_mode character_to_tile
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 2
    }

    self_damage {
        piercing true
        cant_miss true
        effects {
            DeferVaporize 1
        }
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

### `SlotResult_Explode`
**Source:** `special_enemy_abilities.gon`  

```
SlotResult_Explode {
    template spell
    
    graphics { 
        particle Explosion
        animation resultExplode
        delay 2
        visual_delay_but_simultaneous_damage 2
    }
    
    target {
        aoe_mode standard
        knockback_mode character_to_tile
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 2
    }

    self_damage {
        piercing true
        cant_miss true
        effects {
            DeferVaporize 1
        }
    }
    
    damage_instance {
        damage 10
        knockback 2

        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `SlotMachine_DeathExplode`
**Source:** `special_enemy_abilities.gon`  

```
SlotMachine_DeathExplode {
    variant_of SlotResult_Explode

    graphics {
        animation dying
    }
}
```

---

### `SlotResult_Nothing`
**Source:** `special_enemy_abilities.gon`  

```
SlotResult_Nothing {
    template self_buff
    
    graphics { 
        animation resultLose
    }
}
```

---

### `SlotResult_RandomPickup`
**Source:** `special_enemy_abilities.gon`  

```
SlotResult_RandomPickup {
    template spawn

    graphics {
        lob true
        animation resultWin
        bounce_on_hit true
    }

    target {
        target_mode direction
        aoe_mode line
        min_aoe 1
        max_aoe 1
        restrictions none
    }

    spawn {
        object SlotMachineNormalPickupReward
    }
}
```

---

### `SlotResult_Jackpot_Coins`
**Source:** `special_enemy_abilities.gon`  

```
SlotResult_Jackpot_Coins {
    template spawn

    graphics {
        lob true
        animation resultJackpot
        bounce_on_hit true
    }

    target {
        target_mode direction
        aoe_mode cone
        min_aoe 1
        max_aoe 4
        restrictions none
        min_targets 7
        max_targets 7
        stagger_multihit_targets true
        multihit 7
    }

    self_damage {
        effects {
            FormChange Default
        }
    }

    spawn {
        object SlotMachineJackpotCoinsReward
    }
}
```

---

### `ClotEvolve`
**Source:** `special_enemy_abilities.gon`  

```
ClotEvolve {
    template self_buff

    graphics {
        animation pulse
    }

    damage_instance {
        ai_base_score 999999
        effects {
            PopAndSpawn StemCat_HalfHealth
        }
    }
}
```

---

### `ClotFailEvolve`
**Source:** `special_enemy_abilities.gon`  

```
ClotFailEvolve {
    template self_buff

    graphics {
        animation pulse
    }

    damage_instance {
        ai_base_score 999999
    }
}
```

---

### `ClotEvolveCatCopy`
**Source:** `special_enemy_abilities.gon`  

```
ClotEvolveCatCopy {
    template self_buff

    graphics {
        animation pulse
    }

    damage_instance {
        ai_base_score 999999
        effects {
            PopAndSpawn {
                object PlayerCat_ClotClone
                clone_referenced_catdata true
                clone_items false
            }
        }
    }
}
```

---

### `SpawnClot`
**Source:** `special_enemy_abilities.gon`  

```
SpawnClot {
    template spawn

    graphics {
        lob true
        animation spawn
    }

    target {
        min_range 1
        max_range 1
    }

    spawn {
        object Clot
        ai_base_score 9999
    }
}
```

---

### `ThrobShot`
**Source:** `special_enemy_abilities.gon`  

```
ThrobShot {
    template lobbed_attack

    graphics {
        animation shoot
		projectile Tumorball
    }

    target {
        min_range 3
        max_range 7+bonus_range
        max_aoe 1
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Bleed 1
            ChangeTile WaterTile
        }

        elements [
            Water
        ]
    }
}
```

---

### `ThrobShot_Reaction`
**Source:** `special_enemy_abilities.gon`  

```
ThrobShot_Reaction {
    variant_of ThrobShot

    target {
        max_range 3
        range_mode 8cross
    }
}
```

---

### `ParasiterSpawn`
**Source:** `special_enemy_abilities.gon`  

```
ParasiterSpawn {
    template spawn

    graphics {
        lob false
        animation spawn
    }
    
    target {
        min_range 1
        max_range 1
    }

    spawn {
        object [TumorousMaggot, ChargeyMaggot, SwappyMaggot, Maggot, Maggot]
        ai_base_score 9999
        faction self
    }
}
```

---

### `ParasiterShoot`
**Source:** `special_enemy_abilities.gon`  

```
ParasiterShoot {
    template lobbed_attack

    graphics {
        projectile Maggot
    }

    target {
        min_range 1
        max_range 2
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            ObjectOnHitEmpty Maggot

            Conditional_DebuffRoll {
                odds 15%
                DestroyEquipmentAndAttachParasite {
                    pool parasites
                }
            } Else {
                ObjectOnHitCharacter Maggot
            }
        }
    }
}
```

---

### `FleshLadDoublehit`
**Name:** Double Hit  
**Description:** A melee attack that hits twice.  
**Source:** `special_enemy_abilities.gon`  

```
FleshLadDoublehit {
    template melee_attack

    meta {
        name "EABILITY_DOUBLEHIT_NAME"
        desc "EABILITY_DOUBLEHIT_DESC"
        animate_name false
    }

    graphics {
        animation doublepunch
        dont_visualize_ai true
    }
    
    target {
        multihit 2
    }
    
    damage_instance {
        damage 1+bonus_melee_damage
    }
}
```

---

### `FleshLadUppercut`
**Name:** Uppercut  
**Description:** Punch a unit, knocking it back 3 tiles and inflicting Bruise.
[s:.7](Castable once per turn.)[/s]  
**Source:** `special_enemy_abilities.gon`  

```
FleshLadUppercut {
    template melee_attack

    meta {
        name "EABILITY_FLESHLAD_UPPERCUT_NAME"
        desc "EABILITY_FLESHLAD_UPPERCUT_DESC"
        animate_name false
    }

    cost {
        cantrip true
    }

    graphics {
        animation attack
        dont_visualize_ai true
    }

    damage_instance {
        damage 1+bonus_melee_damage
        knockback 3

        effects {
            Bruise 1
        }
    }
}
```

---

### `SkinnedTripleDash_AI`
**Source:** `special_enemy_abilities.gon`  

```
SkinnedTripleDash_AI {
    template dash_attack

    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }

    temporary_effects {
        CastAgain 2
    }

    target {
        max_range 1
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 3
    }
}
```

---

### `SkinnedTripleDash`
**Source:** `special_enemy_abilities.gon`  

```
SkinnedTripleDash {
    ai_ability SkinnedTripleDash_AI
    template dash_attack

    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }

    target {
        max_range 1
    }

    temporary_effects {
        CastAgain 2
    }

    damage_instance {
        damage 2+bonus_melee_damage
        knockback 1
    }
}
```

---

### `FleshyMindDisable`
**Name:** Disable  
**Source:** `special_enemy_abilities.gon`  

```
FleshyMindDisable {
    template lobbed_attack

    meta {
        name "EABILITY_DISABLE_NAME"
    }

    graphics {
        animation pulse
        projectile MagicMissileProjectile
        lob_height 1
        speed 20
    }

    target {
        target_mode none
        aoe_mode circle
        aoe_excludes_self true
        knockback_mode character_to_tile
        max_aoe 3

        aoe_restrictions [enemies_only]
    }
    
    damage_instance {
        damage "3+bonus_basic_spell_damage"
        cant_miss true
        type spell

        effects {
            Muted 1
            VisualFXTile MagicMissleBlast
        }
    }
}
```

---

### `FleshyMindConfusion`
**Source:** `special_enemy_abilities.gon`  

```
FleshyMindConfusion {
    template targeted_status

    target {
        max_range 20
    }

    graphics {
        animation attack
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Conditional_HasStatus {
                status Confusion
                Confusion 1
            } Else {
                Confusion 2
            }
        }
    }
}
```

---

### `THC_KnockCoinsRanged`
**Source:** `special_enemy_abilities.gon`  

```
THC_KnockCoinsRanged {
    template straightshot_attack

    graphics {
        animation throwobject
    }

    target {
        max_aoe 3+bonus_range
    }

    damage_instance {
        effects {
            ScatterHeldCoin 1
            ScatterHeldCoin [1 .3]
        }
    }
}
```

---

### `THC_PoisonSwat`
**Source:** `special_enemy_abilities.gon`  

```
THC_PoisonSwat {
    template melee_attack
    
    meta {
        is_basic_attack true
    }

    graphics {
        animation doubleswat
    }

    target { 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable
        multihit 2
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

### `THC_CoinRoll`
**Source:** `special_enemy_abilities.gon`  

```
THC_CoinRoll {
    template move

    graphics {
        sync_speed 22
        max_tiles_single_loop 5
        ignore_slowtiles true
        move_start_animation startroll
        animation roll
        move_end_animation endroll
    }

    cost {
        cantrip true
        cantrip_group THC_CoinRoll
    }

    self_damage {
        effects {
            Conditional_Speculative {
            } Else {
                RemoveMovePoints 1
            }
        }
    }

    target {
        force_ai_target_as_spell true

        range_mode 8cross
        max_range 10
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_diagonals true
    }

    damage_instance {
        type none
        damage 0

        custom_additional_ai_weight thiefcat_coinroll
    }
}
```

---

### `THC_Roll`
**Source:** `special_enemy_abilities.gon`  

```
THC_Roll {
    variant_of THC_CoinRoll

    bonus_passives {
        AbilityEnabledIfBasicAttackUsedThisTurn 1
    }

    damage_instance {
        custom_additional_ai_weight thiefcat_roll
    }
}
```

---

### `Dybbuk_StopHittingYourself`
**Name:** Stop Hitting Yourself  
**Source:** `special_enemy_abilities.gon`  

```
Dybbuk_StopHittingYourself {
    template melee_attack
    
    meta {
        name "EABILITY_STOPHITTINGYOURSELF_NAME"
        is_basic_attack true
    }

    cost {
        cantrip true
        mana 0
    }

    graphics {
        animation punchSelf
    }

    target { 
        target_mode none
        min_aoe 0
        max_aoe 0
        restrictions none
        aoe_excludes_self false
    }

    damage_instance {
        cant_miss true

        effects {
            RemoveStatus DybbukPossessed
        }
    }
}
```

---

### `JackShield`
**Name:** Protect  
**Source:** `special_enemy_abilities.gon`  

```
JackShield {
    template spell

    meta {
        name "EABILITY_PROTECT_NAME"
    }

    graphics {
        affected_particle fx_shield
        animation pray
    }

    target {
        max_aoe 2
        max_range 6
    }
    
    damage_instance {
        heal 0

        effects {
            Shield 5
        }
    }
}
```

---

### `JackAttack`
**Source:** `special_enemy_abilities.gon`  

```
JackAttack {
    template melee_attack

    graphics {
        animation knockswatatk
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee
        knockback 1
    }
}
```

---

### `CherubimReturn`
**Name:** Crash  
**Source:** `special_enemy_abilities.gon`  

```
CherubimReturn {
    template return

    meta {
        name "EABILITY_CRASH_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true

        aoe_spell_on_land true
        delay 5
        animation crash
        area_particle Earthquake
        center_particle none
        visual_delay_but_simultaneous_damage 7
    }

    cost {
        prime 1
        cantrip true
    }

    target {
        aoe_mode standard
        max_range 20   
        restrictions must_be_moveable
        max_aoe 2
        allow_any_orientation true
        prioritize_face_camera true
        force_ai_target_as_spell true
    }
    temporary_effects {
        Trample 3
    }
    self_damage {
        effects {
            DoScreenShake {
                time 1
                intensity 30
            }
        }
    }

    damage_instance {
        damage 15+bonus_melee_damage
        ai_base_score 100
        override_trample_damage true

        effects {
            ForceDisplace 1
            Stun 1
            IgnoreSelf 1
        }
    }
    splash_damage {
        damage "(15+bonus_melee_damage)*.5"
        knockback 3
    }
}
```

---

### `CherubimHeal`
**Name:** Bless  
**Source:** `special_enemy_abilities.gon`  

```
CherubimHeal {
    template spell

    meta {
        name "EABILITY_BLESS_NAME"
    }

    graphics {
        affected_particle HealBig
        animation heal
    }

    target {
        max_aoe 2
        max_range 6
        aoe_excludes_self true
    }
    
    damage_instance {
        heal 4

        effects {
            DivineShield 1
        }

        elements [
            HOLY
        ]
    }
}
```

---

### `CherubimLeave`
**Name:** Leave  
**Source:** `special_enemy_abilities.gon`  

```
CherubimLeave {
    template leave

    meta {
        name "EABILITY_LEAVE_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true
    }

    cost {
        cantrip true
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `SeraphimX`
**Name:** Holy Light  
**Source:** `special_enemy_abilities.gon`  

```
SeraphimX {
    template spell

    meta {
        name "EABILITY_HOLYLIGHT_NAME"
    }
    
    cost {
        mana 0
    }

    graphics {
        particle Holybeam
        delay 2
        animation attack
    }
    
    target {
        target_mode none
        aoe_mode diagcross
        max_aoe 10
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 5+bonus_basic_spell_damage

        elements [
            Holy
        ]
    }
}
```

---

### `SeraphimRevive`
**Name:** Revive  
**Source:** `special_enemy_abilities.gon`  

```
SeraphimRevive {
    template spell

    meta {
        name "EABILITY_REVIVE_NAME"
    }

    graphics {
        animation revive
        affected_particle HealBig
        dont_visualize_ai true
    }

    cost {
        cantrip true
    }

    target {
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_corpse
    }

    damage_instance {
        heal 0

        effects {
            Revive 50%

            Conditional_Ally {
                Conditional_Corpse {
                    FlatAIBonus 100
                }
            }
        }

        elements [
            Holy
        ]
    }
}
```

---

### `CherubAttract`
**Name:** Allure  
**Source:** `special_enemy_abilities.gon`  

```
CherubAttract {
    template targeted_status

    meta {
        name "EABILITY_ALLURE_NAME"
    }

    graphics {
        animation charm
        particle none
    }

    target {
        max_range 5
    }

    damage_instance {
        damage 0

        effects {
            Attraction 1
        }
    }
}
```

---

### `CherubMelee`
**Name:** Poison Kiss  
**Source:** `special_enemy_abilities.gon`  

```
CherubMelee {
    template melee_attack

    meta {
        name "EABILITY_POISONKISS_NAME"
    }

    graphics {
        animation kiss
    }

    damage_instance {
        damage 0

        effects {
            Poison 5
        }
    }
}
```

---

### `CherubDoom`
**Source:** `special_enemy_abilities.gon`  

```
CherubDoom {
    template targeted_status

    graphics {
        animation doom
        particle none
    }

    target {
        max_range 20
    }

    damage_instance {
        damage 0

        effects {
            Doomed 2
        }
    }
}
```

---

### `AngelcatWind`
**Name:** Holy Wind  
**Source:** `special_enemy_abilities.gon`  

```
AngelcatWind {
    template spell

    meta {
        name "EABILITY_HOLYWIND_NAME"
    }

    graphics {
        animation shoot
        particle fx_windSpell
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 2
    }
    
    damage_instance {
        damage 3
        knockback 4

        effects {
            Blind 2
            OverrideKnockbackDamage 5
        }
        
        elements [
            Wind
            Holy
        ]
    }
}
```

---

### `GKLeap`
**Source:** `special_enemy_abilities.gon`  

```
GKLeap {
    template jump_move

    graphics {
        full_jump_animation leap
        full_jump_sync_frames 30
        full_jump_windup_frames 14
    }

    cost {
        cantrip true
    }

    target {
        max_range 20
    }

    self_damage {
        effects {
            RemoveMovePoints 1
        }
    }
}
```

---

### `GKSuck`
**Name:** Absorb Soul  
**Source:** `special_enemy_abilities.gon`  

```
GKSuck {
    template tile_targeted_melee_attack
    class PlaceholderMeleeAttackAbility

    meta {
        name "EABILITY_ABSORBSOUL_NAME"
    }

    graphics {
        animation attack
    }

    target {
        knockback_mode tile_to_character
        restrictions must_have_character
    }

    damage_instance {
        damage 0
        makes_contact false

        effects {
            Die 1
            PermanentConstitution -2
            ApplyToSource {
                ConstitutionUp 2
                HealthGain 8
            }
            GenericDebuff 10
        }
    }
}
```

---

### `GKSpawn`
**Source:** `special_enemy_abilities.gon`  

```
GKSpawn {
    template spawn
    
    graphics {
        lob false
        animation spawn
    }

    target {
        max_range 1
    }

    spawn {
        object [SkeletonCat TallSkeletonCat SnakeyBones]
        first_turn initiative
        faction self
    }
}
```

---

### `ChaosStacyAttack`
**Source:** `special_enemy_abilities.gon`  

```
ChaosStacyAttack {
    template melee_attack
    chain_ability ChaosStacyAttackChain

    graphics {
        animation knockswatatk
    }

    damage_instance {
        damage 0
        effects {
            GenericDebuff 10
            Conditional_PlayerCat {
                Scrambled 1
            } Else {
                Confusion 1
            }
            FaceAway 1

            Conditional_Speculative {
                Knockback 10
            }
        }
    }
}
```

---

### `ChaosStacyAttackChain`
**Source:** `special_enemy_abilities.gon`  

```
ChaosStacyAttackChain {
    template melee_attack

    graphics {
        animation attack
    }

    damage_instance {
        damage 3+bonus_melee_damage
        knockback 10

        effects {
            CharmedForceAttack 1
        }
    }
}
```

---

### `MD_Lift`
**Source:** `special_enemy_abilities.gon`  

```
MD_Lift {
    template self_buff

    graphics {
        animation lift
    }

    damage_instance {
        effects {
            Conditional_InForm {
                form Default
                FormChange Lifted
            }
            SetHealth 100%
            PurgeAll 1
        }
    }
}
```

---

### `MD_Walk`
**Source:** `special_enemy_abilities.gon`  

```
MD_Walk {
    template jump_move

    graphics {
        full_jump_animation walk
        full_jump_sync_frames 38
        full_jump_windup_frames 10
    }

    target {
        aoe_considers_character_size false
        range_considers_character_size false
    }

    self_damage {
        effects {
            DoScreenShake {
                time .5
                intensity 10
            }
        }
    }

    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `MD_WalkOne`
**Source:** `special_enemy_abilities.gon`  

```
MD_WalkOne {
    variant_of MD_Walk
    target {
        max_range 1
    }
}
```

---

### `MD_Stomp`
**Source:** `special_enemy_abilities.gon`  

```
MD_Stomp {
    template spell
    
    graphics {
        animation stomp
        particle Earthquake
        delay 5
    }
    
    cost {
        cantrip true
    }
    
    target {
        target_mode none
        aoe_mode square
        min_aoe 0
        max_aoe 1
        knockback_mode character_to_tile
        aoe_excludes_self true
        prioritize_dont_change_direction true
        aoe_considers_character_size true
    }

    self_damage {
        effects {
            ChangeTilesUnder DirtTile
        }
    }
    
    damage_instance {
        damage 7+bonus_melee_damage
        knockback 1

        effects {
            IgnoreSelf 1
            DoScreenShake {
                time 2
                intensity 10
            }

            Conditional_HasTag {
                tag megadino
                SetKnockback 0
            }
        }

        elements [
            Earth
        ]
    }
}
```

---

### `MD_Kick`
**Source:** `special_enemy_abilities.gon`  

```
MD_Kick {
    template melee_attack

    graphics {
        animation kick
    }
    
    target {
        restrictions must_match_locked_orientation
    }

    damage_instance {
        damage 7+bonus_melee_damage

        effects {
            Conditional_HasTag {
                tag megadino
            } Else {
                KnockUpAndAway {
                    stacks 3
                    distance 3
                }
            }
        }
    }
}
```

---

### `MD_LegLeave`
**Source:** `special_enemy_abilities.gon`  

```
MD_LegLeave {
    template leave
    graphics {
        animation leave
    }
    self_damage {
        effects {
            FormChange OffMap
            SetHealth 100%
            PurgeAll 1
        }
    }
}
```

---

### `MD_LegReturn`
**Source:** `special_enemy_abilities.gon`  

```
MD_LegReturn {
    template return

    target {
        max_range 20
    }

    graphics {
        animation return
    }

    damage_instance {
        damage 3
        effects {
            ForceDisplace 1
            IgnoreSelf 1
        }
    }

    self_damage {
        effects {
            FormChange Default
            SetHealth 100%
            PurgeAll 1
        }
    }
}
```

---

### `MD_HeadLeave`
**Source:** `special_enemy_abilities.gon`  

```
MD_HeadLeave {
    template leave
    graphics {
        animation raise
        dont_visualize_ai true
    }
    self_damage {
        effects {
            FormChange OffMap
            PurgeAll 1
            ReturnDinoLegs 1
        }
    }
    damage_instance {
        ai_base_score 99999
    }
}
```

---

### `MD_HeadDrop`
**Source:** `special_enemy_abilities.gon`  

```
MD_HeadDrop {
    template return

    graphics {
        animation drop

        aoe_spell_on_land true
        delay 5
        area_particle Earthquake
        center_particle none
    }

    target {
        max_range 20
        aoe_excludes_self true
        max_aoe 1
        aoe_mode square
        aoe_considers_character_size true
        restrictions none
    }

    temporary_effects {
        DisableTrample 1
    }

    self_damage {
        damage 100
        effects {
            DoScreenShake {
                time 2
                intensity 30
            }
            Stun 1
            FormChange Default
        }
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 5
        override_trample_damage true

        effects {
            // ForceDisplace 1
            IgnoreSelf 1

            Conditional_HasTag {
                tag megadino
                IgnoreDamage 1
            }
        }

        elements [
            Earth
        ]
    }
    splash_damage {
        damage 5+bonus_melee_damage
        knockback 5
    }
}
```

---

### `MD_Poop`
**Name:** Defecate  
**Source:** `special_enemy_abilities.gon`  

```
MD_Poop {
    template self_buff
    
    meta {
        name "EABILITY_DEFECATE_NAME"
    }

    cost {
        allow_offmap_casts true
        must_be_offmap true
    }

    graphics {
        animation none
        dont_visualize_ai true
    }

    self_damage { //not on map so have to do this via self_damage
        effects {
            DinoLegAnimation poop
            UseAbility MD_PoopChain
        }
    }

    damage_instance {
        ai_base_score 999
    }
}
```

---

### `MD_PoopChain`
**Source:** `special_enemy_abilities.gon`  

```
MD_PoopChain {
    template spawn
    ai_ability MD_PoopChainAI

    cost {
        allow_offmap_casts true
        must_be_offmap true
    }

    graphics {
        do_animation_offscreen true
        animation poop
        fall_from_sky true 
    }
    
    
    target {
        max_range 20
        min_range 0
        knockback_mode none
    }

    spawn {
        object PoopCat
        first_turn initiative
        faction self
    }
}
```

---

### `MD_PoopChainAI`
**Source:** `special_enemy_abilities.gon`  

```
MD_PoopChainAI {
    template spell

    cost {
        allow_offmap_casts true
        must_be_offmap true
    }

    target {
        max_range 20
        min_range 0

        aoe_mode custom
        custom_aoe [[0 0] [5 0] [0 -3] [0 3]]

        aoe_symmetry none
        restrictions must_match_locked_orientation
    }

    damage_instance {
        damage 0
        custom_additional_ai_weight tile_exists
    }
}
```

---

### `PoopCatMelee`
**Source:** `special_enemy_abilities.gon`  

```
PoopCatMelee {
    variant_of BasicMelee
    class PlaceholderMeleeAttackAbility

    graphics {
        animation bearHug
    }

    sounds {
        ontrigger SE_PoopCatHug
    }

    target {
        knockback_mode tile_to_character

        aoe_considers_character_size false
        target_mode tile
        restrictions must_have_character
        range_mode standard
        aoe_mode standard
        min_range 1
        max_range 1
        min_aoe 0 
        max_aoe 0 
    }

    damage_instance {
        damage 1+bonus_melee_damage
        effects {
            Poison 3
            Slow 1
        }
    }
}
```

---

### `GirlDinoMelee`
**Source:** `special_enemy_abilities.gon`  

```
GirlDinoMelee {
    template melee_attack

    damage_instance {
        effects {
            Stun 1
        }
    }
}
```

---

### `GirlDinoHeadBash`
**Source:** `special_enemy_abilities.gon`  

```
GirlDinoHeadBash {
    template melee_attack

    damage_instance {
        effects {
            Stun 1
        }
    }
}
```

---

### `BoyDinoHeadBash`
**Source:** `special_enemy_abilities.gon`  

```
BoyDinoHeadBash {
    template melee_attack

    damage_instance {
        knockback 3
        effects {

        }
    }
}
```

---

### `BoyDinoBasic`
**Source:** `special_enemy_abilities.gon`  

```
BoyDinoBasic {
    template melee_attack
    chain_ability BoyDinoDash

    damage_instance {
        damage 1
        effects {
            KnockUpAndAway {
                distance 2
                stacks 3
                height 2
            }
        }
    }
}
```

---

### `BoyDinoDash`
**Source:** `special_enemy_abilities.gon`  

```
BoyDinoDash {
    template dash_attack
    
    graphics {
        dash_start_animation dashstart
        dash_animation dashing
        //dash_end_animation dashend
        dash_attack_animation dashEnd
    }
    
    cost {
        mana 0
    }
    
    target {
        max_range 10
        consider_trample false
    }
    
    damage_instance {
        damage 5+bonus_melee_damage
        knockback 10

        effects {
            OverrideChainKnockback 10
        }
    }
}
```

---

### `BoyDinoCry`
**Source:** `special_enemy_abilities.gon`  

```
BoyDinoCry {
    template self_buff

    graphics { 
        dont_orient true
        animation cry
    }

    damage_instance {
        effects {
            FormChange {
                form "Rage"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `GirlDinoCry`
**Source:** `special_enemy_abilities.gon`  

```
GirlDinoCry {
    template self_buff

    graphics { 
        dont_orient true
        animation cry
    }

    damage_instance {
        effects {
            FormChange {
                form "Rage"
            }
            UseAbility GirlDinoPoop
        }
        ai_base_score 9999
    }
}
```

---

### `GirlDinoPoop`
**Source:** `special_enemy_abilities.gon`  

```
GirlDinoPoop {
    template spawn

    graphics {
        lob true
        animation spawn
    }

    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[-1, 0][-2, 0]]
        aoe_considers_character_size true
    }

    spawn {
        object [Poop Dip Floater Pile]
        ai_base_score 9999
    }
}
```

---

### `GirlDinoThrow`
**Source:** `special_enemy_abilities.gon`  

```
GirlDinoThrow {
    template throw_attack

    graphics {
        animation throw
        use_placeholder true
        face_toss_target true
        dont_visualize_ai true
    }

    target {
        max_range 10
        min_range 1
        restrictions none
        range_mode cross
    }
    
    damage_instance {
        damage 10+bonus_melee_damage
        custom_additional_ai_weight toss_farthest
    }
}
```

---

### `BloatEyeMovement`
**Source:** `special_enemy_abilities.gon`  

```
BloatEyeMovement {
    template dash_attack
    class BounceDashAbility
    

    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend

        decelerate 5
        dash_decelerating_animation dashslow

        lock_orientation_during_dash true
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode direction8
        max_range 1
        max_bounces -1
        splash_damage_aoe_begin 999 //ability forces splash damage on bonk
        restrictions diagonal_only
        allow_diagonal_passthrough true
        range_display_include_direction true
    }
    
    damage_instance { //for trample
        damage 5+bonus_melee_ability_damage

        effects {
            Displace 1
        }
    }
    splash_damage { //for bonk
        damage 5+bonus_melee_ability_damage
        type melee
        makes_contact true
    }
}
```

---

### `BloatEyeMovement2`
**Source:** `special_enemy_abilities.gon`  

```
BloatEyeMovement2 {
    template move
    
    cost {
        mana 0
    }
    
    target {
        range_mode 8cross
        max_range 1
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_diagonals true
    }
    
    /*damage_instance { //for trample
        damage 3+bonus_melee_ability_damage
        override_trample_damage true

        effects {
            Conditional_HasTag {
                tag bloateye

                RandomDistanceDisplace {
                    stacks 20
                    min_dist 4
                }
            }
        }
    }*/
}
```

---

### `BloatSideLaser`
**Source:** `special_enemy_abilities.gon`  

```
BloatSideLaser {
    template laser

    graphics {
        animation shoot
        beam_clip fx_bloatlaser
        beam_cap fx_bloatlasercap
    }

    target {
        aoe_mode custom
        custom_aoe [[0 1][0 -1]]
        restrictions must_match_current_orientation
    }

    damage_instance {
        damage 5

        effects {
            Bleed 1
        }
    }
}
```

---

### `BloatFrontLaser`
**Source:** `special_enemy_abilities.gon`  

```
BloatFrontLaser {
    template laser

    graphics {
        animation shootForward
        beam_clip fx_bloatlaser
        beam_cap fx_bloatlasercap
    }

    damage_instance {
        damage 5

        effects {
            Bleed 1
        }
    }
}
```

---

### `BloatLeap`
**Name:** Leap  
**Source:** `special_enemy_abilities.gon`  

```
BloatLeap {
    template jump_attack

    meta {
        name "EABILITY_LEAP_NAME"
    }

    graphics {
        jump_start_animation none
        full_jump_animation jump
        full_jump_sync_frames 25
        full_jump_windup_frames 60
        
        aoe_spell_on_land true
        delay 5
        particle Earthquake
    }

    cost {
        act_points 1
    }
    
    target {
        min_range 1
        max_range 7
        min_aoe 0
        max_aoe 2
        aoe_excludes_self false
        aoe_mode standard
        restrictions must_be_moveable
    }

    damage_instance {
        damage 4

        effects {
            IgnoreSelf 1
            ChangeTile WaterTile
        }
    }
}
```

---

### `BloatLoseFirstEye`
**Source:** `special_enemy_abilities.gon`  

```
BloatLoseFirstEye {
    template self_buff

    graphics {
        animation spawn
    }

    damage_instance {
        effects {
            FormChange {
                form "OneEye"
            }
            ObjectOnHitCharacter BloatEye
        }
        ai_base_score 9999
    }
}
```

---

### `BloatLoseSecondEye`
**Source:** `special_enemy_abilities.gon`  

```
BloatLoseSecondEye {
    template self_buff

    graphics {
        animation spawn
    }

    damage_instance {
        effects {
            FormChange {
                form "NoEyes"
            }
            ObjectOnHitCharacter BloatEye
        }
        ai_base_score 9999
    }
}
```

---

### `LELeave`
**Name:** Leave  
**Source:** `special_enemy_abilities.gon`  

```
LELeave {
    template leave

    meta {
        name "EABILITY_LEAVE_NAME"
        is_move true
    }

    graphics {
        dont_visualize_ai true
    }

    cost {
        cantrip true
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `LEPortFar`
**Source:** `special_enemy_abilities.gon`  

```
LEPortFar {
    variant_of Teleport

    target {
        max_range 9
    }
}
```

---

### `LEReturn`
**Name:** Zap  
**Source:** `special_enemy_abilities.gon`  

```
LEReturn {
    template return

    meta {
        name "EABILITY_ZAP_NAME"
        is_move true
    }

    graphics {
        aoe_spell_on_land true
        delay 3
        center_particle none
        area_particle Bolt
    }

    cost {
        prime 1
        cantrip true
    }

    target { //todo: X lighting then teleport away
        aoe_mode standard
        max_range 20   
        restrictions must_be_moveable

        aoe_mode diagcross
        max_aoe 10
        aoe_excludes_self true
        allow_any_orientation true
        prioritize_face_camera true
        force_ai_target_as_spell true
        aoe_spell_on_land true
        knockback_mode none
    }
    temporary_effects {
        Trample 3
    }

    self_damage {
        effects {
            RemoveActPoints 1
            UseMoveAbilityWithAI {
                ability LEPortFar
                move_weights stay_far_move_far
            }
        }
    }

    damage_instance {
        damage 5
        type spell
        ai_base_score 100
        override_trample_damage true

        effects {
            ForceDisplace 1
            Stun [0 .25]
            IgnoreSelf 1
        }
        elements [
            Electric
        ]
    }
    splash_damage {
        damage 5
        type spell

        effects {
            Stun [0 .25]
            IgnoreSelf 1
        }
        elements [
            Electric
        ]
    }
}
```

---

### `LEBurst`
**Name:** Lightning Burst  
**Source:** `special_enemy_abilities.gon`  

```
LEBurst {
    template spell

    meta {
        name "EABILITY_LIGHTNINGBURST_NAME"
    }

    graphics {
        particle Bolt
        animation strike
    }
    
    target {
        target_mode none
        aoe_excludes_self true
        max_aoe 20
        prioritize_face_camera 1
        knockback_mode none
        aoe_restrictions checker_parity_even
    }
    
    damage_instance {
        damage 2

        elements [
            Electric
        ]
    }
}
```

---

### `IDSprout`
**Name:** Sprout  
**Source:** `special_enemy_abilities.gon`  

```
IDSprout {
    template spawn

    meta {
        name "EABILITY_SPROUT_NAME"
    }
    
    graphics {
        lob false
        animation statusReaction
        dont_visualize_ai true
        dont_orient true
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        max_targets 1
    }

    spawn {
        object Sprout
        ai_base_score 99999
        faction self
    }
}
```

---

### `IDBrambleBurst`
**Source:** `special_enemy_abilities.gon`  

```
IDBrambleBurst {
    template spell

    graphics { 
        dont_orient true
        center_particle Explosion
        area_particle none
        animation blowUp
        delay 15
    }
    
    target {
        target_mode none
        min_range 0
        max_range 0
        
        min_aoe 0
        max_aoe 2
    }
    
    damage_instance {
        damage 0
        knockback 0

        effects {
            ChangeTile BrambleTile
            PopAndSpawn Sprout
        }

        elements [
            Explosion
        ]
    }

    splash_damage {
        layer tiles
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

### `IDBrambleShot`
**Name:** Bramble Shot  
**Source:** `special_enemy_abilities.gon`  

```
IDBrambleShot {
    template spell

    meta {
        name "EABILITY_BRAMBLESHOT_NAME"
    }
    
    graphics {
        animation shoot
        use_projectile true
        particle none
        projectile BrambleProjectile
        delay 5
    }
    
    target {
        min_range 1
        max_range 2
        max_aoe 0
    }

    damage_instance {
        damage 2
        
        effects {
            BramblesOnHit 1
        }
        
        elements [
            Grass
        ]

        custom_additional_ai_weight non_bramble_tile_close_to_enemy
    }
}
```

---

### `RockToss_CaveDad`
**Name:** Rock Toss  
**Source:** `special_enemy_abilities.gon`  

```
RockToss_CaveDad {
    template lobbed_attack

    meta {
        name "EABILITY_ROCKTOSS_NAME"
    }

    graphics {
        projectile SmallRock
        animation throwobject
    }
    
    cost {
        mana 0
        act_points 1
    }
    
    target {
        min_range 1
        max_range 20
    }
    
    damage_instance {
        damage 2+bonus_ranged_damage

        effects {
            BounceObject SmallRock
        }

        elements [
            Rock
        ]

        custom_additional_ai_weight dont_target_rock
    }
}
```

---

### `CaveDad_ClubBasic`
**Source:** `special_enemy_abilities.gon`  

```
CaveDad_ClubBasic {
    template melee_attack

    graphics {
        animation weaponswing
    }

    cost {
        must_have_weapon true //if you destroy his club he shouldnt use this anymore
    }
    
    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
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

### `CaveMom_Basic`
**Source:** `special_enemy_abilities.gon`  

```
CaveMom_Basic {
    template lobbed_attack

    graphics {
        lob true
        animation throwobject
        projectile Snowball
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
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

### `CaveMom_TossDad`
**Name:** Toss  
**Source:** `special_enemy_abilities.gon`  

```
CaveMom_TossDad {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        animation knockupatk
        face_toss_target true
    }

    cost {
        cantrip true
        cantrip_group cavemomtoss
    }
    
    target {
        max_range 20
    }
    
    damage_instance {
        damage 1
        blocked_damage 5+bonus_melee_ability_damage

        custom_additional_ai_weight toss_towards_buddy
    }
}
```

---

### `CaveMom_TossElsewhere`
**Name:** Toss  
**Source:** `special_enemy_abilities.gon`  

```
CaveMom_TossElsewhere {
    template throw_attack
    
    meta {
        name "EABILITY_TOSS_NAME"
    }

    graphics {
        animation knockupatk
        face_toss_target true
    }

    cost {
        cantrip true
        cantrip_group cavemomtoss
    }
    
    target {
        max_range 20
        restrictions none
    }
    
    damage_instance {
        damage 1
        blocked_damage 5+bonus_melee_ability_damage
    }
}
```

---

### `CaveMom_Heal`
**Source:** `special_enemy_abilities.gon`  

```
CaveMom_Heal {
    template melee_attack

    graphics {
        animation lickAttack
    }
    
    cost {
        mana 0
    }
    
    damage_instance {
        heal 5

        effects {
            Cleanse 0
        }
    }
}
```

---

### `CaveCatPounce`
**Name:** Pounce  
**Source:** `special_enemy_abilities.gon`  

```
CaveCatPounce {
    template jump_attack

    meta {
        name "EABILITY_POUNCE_NAME"
    }

    graphics {
        jump_attack_animation none
        fixed_jump_height 1
    }

    target {
        aoe_excludes_self false
        max_aoe 0
        min_aoe 0

        max_range 4
        restrictions none
        always_bounce true
    }

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `BearTrap_CaveBaby`
**Name:** Bear Trap  
**Source:** `special_enemy_abilities.gon`  

```
BearTrap_CaveBaby {
    template lobbed_attack
    
    meta {
        name "EABILITY_BEARTRAP_NAME"
    }

    graphics {
        animation throwobject
        projectile DamageTrap
        use_rotation false
    }

    cost {
         cantrip true
    }

    target {
        min_range 1
        max_range 2

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

### `CaveCatEnrageOne`
**Source:** `special_enemy_abilities.gon`  

```
CaveCatEnrageOne {
    template self_buff
    
    graphics { 
        animation fail
    }

    damage_instance {
        effects {
            FormChange {
                form "TwoAlive"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `CaveCatEnrageTwo`
**Source:** `special_enemy_abilities.gon`  

```
CaveCatEnrageTwo {
    template self_buff
    
    graphics { 
        animation fail
    }

    damage_instance {
        effects {
            FormChange {
                form "OneAlive"
            }
        }
        ai_base_score 9999
    }
}
```

---

### `ManglerMonsterDashAttack`
**Source:** `special_enemy_abilities.gon`  

```
ManglerMonsterDashAttack {
    template dash_attack

    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
    }

    target {
        consider_trample true
    }

    damage_instance { //for trample
        damage 10+bonus_melee_damage
        override_trample_damage true
    }
}
```

---

### `ManglerFumbleEven`
**Source:** `special_enemy_abilities.gon`  

```
ManglerFumbleEven {
    template multihit_self_buff
    
    graphics { 
        animation fumble
    }

    target {
        multihit 4
    }

    damage_instance {
        effects {
            ManglerShuffle false
        }
    }
}
```

---

### `ManglerFumbleOdd`
**Source:** `special_enemy_abilities.gon`  

```
ManglerFumbleOdd {
    variant_of ManglerFumbleEven

    graphics { 
        animation fumble2
    }

    target {
        multihit 5
    }
}
```

---

### `ManglerCommand`
**Source:** `special_enemy_abilities.gon`  

```
ManglerCommand {
    template targeted_status

    target {
        max_range 20
    }

    graphics {
        animation controlmonster
        dont_visualize_ai true
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            ManglerAttack 1
        }
        custom_additional_ai_weight must_target_buddy
        ai_base_score 999
    }
}
```

---

### `ManglerEnrage`
**Source:** `special_enemy_abilities.gon`  

```
ManglerEnrage {
    template self_buff
    
    graphics { 
        animation none
    }

    damage_instance {
        effects {
            UseAbility ManglerThrowRemote
        }
    }
}
```

---

### `ManglerThrowRemote`
**Source:** `special_enemy_abilities.gon`  

```
ManglerThrowRemote {
    template lobbed_attack
    
    graphics { 
        animation throw
		projectile Joystick
    }

    target {
        min_range 1
        max_range 20
    }
    self_damage {
        effects {
            FormChange NoStick
        }
    }

    damage_instance {
        damage 5+bonus_ranged_damage
        effects {
            Stun 1
        }
        ai_base_score 999999
    }
}
```

---

### `ManglerJab`
**Source:** `special_enemy_abilities.gon`  

```
ManglerJab {
    template melee_attack

    graphics {
        animation jab
    }

    target {
        multihit 3
    }

    damage_instance {
        damage 1+bonus_melee_damage
        type melee

        effects {
            RandomStatusFromPool {
                RandomStatDown 1
                Weakness 1
                Poison 1
                Bleed 1
                Bruise 1
            }
        }
    }
}
```

---

### `ManglerSpin`
**Source:** `special_enemy_abilities.gon`  

```
ManglerSpin {
    template melee_attack

    graphics {
        animation spin
    }

    cost {
        cantrip true
    }

    target {
        aoe_mode square
        multihit 4
        knockback_mode character_to_tile
    }

    damage_instance {
        damage 2+bonus_melee_damage
        type melee
    }
}
```

---

### `ManglerMonsterExplode`
**Source:** `special_enemy_abilities.gon`  

```
ManglerMonsterExplode {
    template spell
    
    graphics {
        animation explode
        particle none
    }

    target {
        target_mode none
        aoe_mode circle
        min_aoe 0
        max_aoe 20
        aoe_excludes_self true
        aoe_considers_character_size true
    }
    
    damage_instance {
        damage 0
        knockback 10

        ai_base_score 999999
    }
}
```

---

### `ManglerMonsterHeartAttack`
**Source:** `special_enemy_abilities.gon`  

```
ManglerMonsterHeartAttack {
    template self_buff
    
    graphics {
        animation dying
    }

    damage_instance {
        effects {
            FormChange NoDeathrattle
            DieViaAbilityInternally 1
        }
    }
}
```

---

### `SpawnMotherTumor`
**Source:** `special_enemy_abilities.gon`  

```
SpawnMotherTumor {
    template spawn

    graphics {
        lob false
        animation shoot
    }

    cost {
        mana 0
        infcantrip true
    }

    target {
        max_range 20

        range_excludes_blocking false
        aoe_restrictions none
    }

    spawn {
        object MotherTumor
    }
}
```

---

### `MotherTumorForcePass`
**Source:** `special_enemy_abilities.gon`  

```
MotherTumorForcePass {
    template targeted_status

    graphics {
        lob false
        animation pointout
    }

    cost {
        mana 0
        infcantrip true
    }

    target {
        max_range 20
    }

    damage_instance {
        effects {
            MotherTumorDebugForcePass 1
        }
    }
}
```

---

### `MotherTumorForceGrow`
**Source:** `special_enemy_abilities.gon`  

```
MotherTumorForceGrow {
    template targeted_status

    graphics {
        lob false
        animation pointout
    }

    cost {
        mana 0
        infcantrip true
    }

    target {
        max_range 20
    }

    damage_instance {
        effects {
            ForceUseAbility MotherTumorGrow
        }
    }
}
```

---

### `MotherTumorGrow`
**Source:** `special_enemy_abilities.gon`  

```
MotherTumorGrow {
    template self_buff

    graphics { 
        animation grow
        dont_orient true
    }

    damage_instance {
        heal 4
        effects {
            InstantMaxHealthUp 4
            Conditional_InForm {
                form Small
                FormChange Big
            }
            Conditional_InForm {
                form SmallHolding
                FormChange BigHolding
            }
            Conditional_InForm {
                form SmallHoldingCat
                FormChange BigHoldingCat
            }
            
        }
        ai_base_score 9999
    }
}
```

---

### `MotherGrow`
**Source:** `special_enemy_abilities.gon`  

```
MotherGrow {
    template self_buff

    graphics {
        animation pullin
    }

    damage_instance {
        effects {
            TriggerMotherGrow 4
        }
    }
}
```

---

### `MotherConsume`
**Source:** `special_enemy_abilities.gon`  

```
MotherConsume {
    template self_buff
    chain_ability MotherGrow

    cost {
        cantrip true
    }

    graphics {
        animation none
    }

    damage_instance {
        effects {
            TriggerMotherConsume 1
        }
        ai_base_score 99999
    }
}
```

---

### `SpawnMotherSpike`
**Source:** `special_enemy_abilities.gon`  

```
SpawnMotherSpike {
    template spawn

    graphics {
        lob false
        animation spike
    }

    cost {
        mana 0
    }

    target {
        max_range 20

        range_excludes_blocking false
        aoe_restrictions none
        knockback_mode tile_to_character
    }

    spawn {
        object MotherSpike
    }
    damage_instance {
        damage 3
        effects {
            KnockUpAndAway {
                stacks 3
                distance 2
            }
        }
    }
}
```

---

### `Dclaude_Declaw`
**Name:** Declaw  
**Description:** A melee attack that inflicts -1 Damage and Bleed.  
**Source:** `special_enemy_abilities.gon`  

```
Dclaude_Declaw {
    template melee_attack

    meta {
        name "ABILITY_DECLAW_NAME"
        desc "ABILITY_DECLAW_DESC"
    }

    graphics {
        animation sliceOpen
    }

    cost {
        mana 0
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage
        piercing true

        effects {
            Bleed 1
            DamageUp -1
        }
    }
}
```

---

### `LiceBite`
**Source:** `special_enemy_abilities.gon`  

```
LiceBite {
    template melee_attack
	
    self_damage {
        damage 0
        type melee

        effects {
            DeleteObject 1
        }
    }

    damage_instance {
        effects {
            Bruise 1
        }
    }
}
```

---

### `LennyTrampleMove`
**Source:** `special_enemy_abilities.gon`  

```
LennyTrampleMove {
    variant_of TrampleMove

    sounds {
        ontrigger_intentional Lenny_HereKitty
    }
}
```

---

### `TheMother_Birth`
**Name:** Birth  
**Source:** `special_enemy_abilities.gon`  

```
TheMother_Birth {
    template spell

    meta {
        name EABILITY_BIRTH_NAME
    }

    graphics {
        animation spike
        particle none
    }

    cost {
        mana 0
    }

    bonus_passives {
        AbilityEnabledOncePerFightAtHealthThreshold 25%
    }

    target {
        target_mode none
        aoe_mode all
        restrictions aoe_must_exist
        aoe_restrictions [must_have_tag]
        target_requires_tag themotherspike
    }

    damage_instance {
        type none
        damage 0
        cant_miss true

        effects {
            Conditional_HasTag {
                tag themotherspike
                PopAndSpawn {
                    object BoyShade
                    no_splatter false
                }
            }
        }
        ai_base_score 999999
    }
}
```

---

## File: `terminator_abilities.gon`

### `T1ChokeReaction`
**Source:** `terminator_abilities.gon`  

```
T1ChokeReaction {
    variant_of BasicMelee
    class PlaceholderMeleeAttackAbility

    graphics {
        animation bearHug
    }

    target {
        knockback_mode tile_to_character

        aoe_considers_character_size false
        target_mode tile
        restrictions must_have_character
        range_mode standard
        aoe_mode standard
        min_range 1
        max_range 1
        min_aoe 0 
        max_aoe 0 
    }

    damage_instance {
        damage 5+bonus_melee_damage
        effects {
            Stun 1
        }
    }
}
```

---

### `T1SwapWeapon`
**Source:** `terminator_abilities.gon`  

```
T1SwapWeapon {
    template self_buff

    graphics {
        animation equipWeapon
    }

    cost {
        cantrip true
    }
    //sounds {
    //    ontrigger SE_WP_SwapShotgun
    //}

    damage_instance {
        damage 0

        effects {
            SwapWeapon {
                pool [TerminatorShotgun TerminatorSniper TerminatorUzi]
            }
        }
        ai_base_score 9999
    }
}
```

---

### `T1ThrowGrenadeA`
**Name:** Throw Grenade  
**Source:** `terminator_abilities.gon`  

```
T1ThrowGrenadeA {
    template spawn

    meta {
        name "EABILITY_THROWGRENADE_NAME"
    }
    
    graphics {
        lob true
        animation throwobject
    }
    
    cost {
        cantrip true
    }
    
    target {
        range_mode standard
        min_range 3
        max_range 6
    }

    spawn {
        object Grenade
        first_turn end_of_round
    }

    damage_instance {
        custom_additional_ai_weight spread_grenades
    }
}
```

---

### `T1ThrowGrenadeB`
**Source:** `terminator_abilities.gon`  

```
T1ThrowGrenadeB {
    variant_of T1ThrowGrenadeA
}
```

---

### `T1Pummel`
**Source:** `terminator_abilities.gon`  

```
T1Pummel {
    variant_of BasicMelee
    class PlaceholderMeleeAttackAbility

    graphics {
        animation terminatorPunch
        othercat_placeholder_available true
    }

    target {
        //knockback_mode tile_to_character

        aoe_considers_character_size false
        target_mode tile
        restrictions must_have_character
        range_mode standard
        aoe_mode standard
        min_range 1
        max_range 1
        min_aoe 0 
        max_aoe 0 

        multihit 6
    }

    damage_instance {
        damage -3+bonus_melee_damage //10 str, makes this 2x6 damage
        effects {
            IntelligenceUp -1
            FaceAway 1
        }
    }
}
```

---

### `wp_TerminatorSniper`
**Name:** Sniper  
**Source:** `terminator_abilities.gon`  

```
wp_TerminatorSniper {
    variant_of wp_22Rifle

    meta {
        name "EABILITY_SNIPER_NAME"
    }

    target {
        restrictions must_have_line_of_sight
    }
    damage_instance {
        damage 8
    }

}
```

---

### `wp_TerminatorShotgun`
**Source:** `terminator_abilities.gon`  

```
wp_TerminatorShotgun {
    variant_of wp_Shotgun
}
```

---

### `wp_TerminatorUzi`
**Source:** `terminator_abilities.gon`  

```
wp_TerminatorUzi {
    variant_of wp_Uzi
    
}
```

---

### `T2Clone`
**Source:** `terminator_abilities.gon`  

```
T2Clone {
    variant_of BasicMelee

    graphics {
        animation liquidclone
    }

    damage_instance {
        damage 0

        effects {
            Conditional_PlayerCat {
                ApplyToSource {
                    Cleanse 0
                    RemoveStatus DodgeChance_Status
                    RemoveStatus SpeedUp_WithoutInitiative
                }

                T2CopyCat 1
                GenericDebuff 999999
            }
        }
    }
}
```

---

### `T2UnClone`
**Source:** `terminator_abilities.gon`  

```
T2UnClone {
    template self_buff

    graphics {
        animation liquidunclone
    }

    damage_instance {
        damage 0
        effects {
            RemoveStatus T2CopyCatInternal
            Cleanse 0
        }
        ai_base_score 999999
    }
}
```

---

### `T2SpearMelee`
**Source:** `terminator_abilities.gon`  

```
T2SpearMelee {
    template melee_attack

    graphics {
        animation liquidmetalspear
        detatched_animation LiquidMetalSpear
        detatched_animation_reach 3
    }

    target {
        max_aoe 3
    }

    damage_instance {
        damage 10+bonus_melee_damage
        piercing true
    }
}
```

---

### `T2GoopRun`
**Source:** `terminator_abilities.gon`  

```
T2GoopRun {
    template teleport

    graphics {
        animation_out liquidteleportOut
        animation_in liquidteleportIn
    }
}
```

---

### `SpawnTerminatorMini_Base`
**Source:** `terminator_abilities.gon`  

```
SpawnTerminatorMini_Base {
    template spawn

    cost {
        allow_offmap_casts true
        must_be_offmap true
        cantrip true
        once_per_fight true
        cant_cast X-1 //if x is 1 or 0, this is <= 0, can cast. If X is 2, this is 1, = cant cast
    }

    graphics {
        animation beamin
        lob false
    }
    
    target {
        max_range 20
        min_range 0
        knockback_mode orientation
        X_is custom
        allow_any_orientation true
    }

    bonus_passives {
        XIsLivingAlliesWithTag terminator_mini
    }

    spawn {
        object TankCat_Terminator
        first_turn initiative
        inherit_elite_buffs false
    }
    damage_instance {
        custom_additional_ai_weight avoid_target_map_top
    }
}
```

---

### `T3Spawn_Tank`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Tank {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object TankCat_Terminator
    }
}
```

---

### `T3Spawn_Mage`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Mage {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object MageCat_Terminator
    }
}
```

---

### `T3Spawn_Hunter`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Hunter {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object HunterCat_Terminator
    }
}
```

---

### `T3Spawn_Thief`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Thief {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object ThiefCat_Terminator
    }
}
```

---

### `T3Spawn_Medic`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Medic {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object MedicCat_Terminator
    }
}
```

---

### `T3Spawn_Fighter`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Fighter {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object FighterCat_Terminator
    }
}
```

---

### `T3Spawn_Colorless`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Colorless {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object Pebbles_Terminator
    }
}
```

---

### `T3Spawn_Necromancer`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Necromancer {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object NecroCat_Terminator
    }
}
```

---

### `T3Spawn_Tinkerer`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Tinkerer {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object TinkererCat_Terminator
    }
}
```

---

### `T3Spawn_Butcher`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Butcher {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object ButcherCat_Terminator
    }
}
```

---

### `T3Spawn_Psychic`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Psychic {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object PsychicCat_Terminator
    }
}
```

---

### `T3Spawn_Druid`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Druid {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object DruidCat_Terminator
    }
}
```

---

### `T3Spawn_Monk`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Monk {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object MonkCat_Terminator
    }
}
```

---

### `T3Spawn_Jester`
**Source:** `terminator_abilities.gon`  

```
T3Spawn_Jester {
    variant_of SpawnTerminatorMini_Base

    spawn {
        object JesterCat_Terminator
    }
}
```

---

### `DCT_SummonCrow`
**Source:** `terminator_abilities.gon`  

```
DCT_SummonCrow {
    template spawn

    tags [summon]
    
    graphics {
        lob true
        animation throwobject
    }

    cost {
        cantrip true
        cant_cast X
        once_per_fight true
    }

    target {
        X_is custom
    }

    bonus_passives {
        XIsLivingAlliesWithTag dc_crow
    }
    
    target {
        min_range 1
        max_range 2
        min_aoe 0
        max_aoe 0
        max_targets 1

        range_excludes_blocking false
        restrictions aoe_must_exist
        aoe_restrictions [exclude_blocking]
    }

    spawn {
        object DruidCrow_Terminator
        custom_additional_ai_weight tile_exists
        faction self
    }
}
```

---

### `T3Pebbles_PrimeBoulderDrop`
**Name:** Boulder Drop!  
**Source:** `terminator_abilities.gon`  

```
T3Pebbles_PrimeBoulderDrop {
    template self_buff

    graphics { 
        animation none
    }


    meta {
        name "EABILITY_BOULDERDROP_NAME"
    }

    damage_instance {
        effects {
            UseAbility {
                ability T3Pebbles_BoulderDrop
                respect_prime true
            }
        }
    }
}
```

---

### `T3Pebbles_BoulderDrop`
**Name:** Boulder Drop!  
**Source:** `terminator_abilities.gon`  

```
T3Pebbles_BoulderDrop {
    template spawn

    meta {
        name "EABILITY_BOULDERDROP_NAME"
    }

    tags [summon]
    
    graphics {
        prime_animation prouder
        fall_from_sky true
        bounce_on_hit false
        animation floatingmagic
        dont_orient true
        fall_randomize_timing .3
    }
    sounds {
        oncast AbilitySnd_BoulderDrop
    }

    cost {
        prime 1
    }

    target {
        target_mode tile
        min_range 1
        max_range 6
        max_aoe 2

        range_excludes_blocking false
        aoe_restrictions none

        knockback_mode zero
    }

    spawn {
        object Boulder
    }

    damage_instance {
        damage 999
        cant_miss true
        type ranged
    }
}
```

---

### `T3LickyLicky`
**Source:** `terminator_abilities.gon`  

```
T3LickyLicky {
    template melee_attack

    graphics {
        animation lickAttack
    }
    
    cost {
        mana 0
    }
    
    damage_instance {
        heal 5

        effects {
            DamageUp 2
            Cleanse 0
        }
    }
}
```

---

### `HitlerPulpBase`
**Source:** `terminator_abilities.gon`  

```
HitlerPulpBase {
    template self_buff
    
    graphics { 
        animation pulp
    }

    damage_instance {
        effects {
            FormChange Pulp2
            Cleanse 0
            Purge 0
            SetHealth 100%
            SetShield 0
        }
    }
}
```

---

### `HitlerPulp1`
**Source:** `terminator_abilities.gon`  

```
HitlerPulp1 {
    template spell

    graphics {
        animation pulp
        particle none
        dont_visualize_ai true
    }

    target {
        target_mode none
        aoe_mode all
    }

    self_damage {
        effects {
            FormChange Pulp2
            PurgeAll 1
            SetHealth 100%
            SetShield 0
            FaceCamera 1

            SwitchMusic {
                //new_song same (for reference if using this effect elsewhere)
                new_layer battle
                crossfade_speed 1
            }
        }
    }

    damage_instance {
        type status_spell
        ai_base_score 9999
        cant_miss true

        effects {
            Conditional_PlayerCat {
                Cleanse 0
                Adrenaline 10
            }
        }
    }
}
```

---

### `HitlerPulp2`
**Source:** `terminator_abilities.gon`  

```
HitlerPulp2 {
    variant_of HitlerPulpBase
    damage_instance {
        effects {
            FormChange Pulp3
        }
    }
}
```

---

### `HitlerPulp3`
**Source:** `terminator_abilities.gon`  

```
HitlerPulp3 {
    variant_of HitlerPulpBase
    damage_instance {
        effects {
            FormChange Pulp4
        }
    }
}
```

---

### `HitlerPulp4`
**Source:** `terminator_abilities.gon`  

```
HitlerPulp4 {
    variant_of HitlerPulpBase
    damage_instance {
        effects {
            FormChange Pulp5
        }
    }
}
```

---

### `HitlerPulp5`
**Source:** `terminator_abilities.gon`  

```
HitlerPulp5 {
    variant_of HitlerPulp1
    damage_instance {
        effects {
            FormChange Pulp6
        }
    }
}
```

---

### `HitlerPulp6`
**Source:** `terminator_abilities.gon`  

```
HitlerPulp6 {
    variant_of HitlerPulpBase
    damage_instance {
        effects {
            FormChange Pulp7
        }
    }
}
```

---

### `T3RipAndTear`
**Name:** Auseinanderreißen  
**Source:** `terminator_abilities.gon`  

```
T3RipAndTear {
    template melee_attack
    class MeleeEatAbility
    ai_ability BasicBigMelee //needed so daddy shark's simple brain can understand this

    meta {
        name EABILITY_T3RIPANDTEAR_NAME
    }

    graphics {
        animation ripandtear
    }

    target { 
        max_aoe 1
    }

    damage_instance {
        type melee
        damage 0
        piercing true
        cant_miss true

        effects {
            Vaporize 20
        }
    }
}
```

---

### `T3Shoot`
**Source:** `terminator_abilities.gon`  

```
T3Shoot {
    template ranged_attack

    target {
        max_range 20
        min_range 1
    }

    graphics {
        projectile Bullet
        animation shoot
        lob_height 0
        speed 25
    }
    
    damage_instance {
        damage 5+bonus_ranged_damage
    }
}
```

---

### `T3Counter`
**Source:** `terminator_abilities.gon`  

```
T3Counter {
    variant_of BasicMelee

    damage_instance {
        knockback 3
    }
}
```

---

### `T3Intro`
**Source:** `terminator_abilities.gon`  

```
T3Intro {
    template self_buff
    chain_ability T3Leave

    graphics {
        dont_visualize_ai true
        animation yella
    }
    target {
        prioritize_face_camera true
    }

    damage_instance {
        ai_base_score 99999
    }
}
```

---

### `T3Leave`
**Source:** `terminator_abilities.gon`  

```
T3Leave {
    template leave

    graphics {
        dont_visualize_ai true
        animation portout
    }

    damage_instance {
        ai_base_score 99999
    }
    self_damage {
        effects {
            PurgeAll 1
            TurnControlDelay .25
            T3HitlerTriggerInitialSpawns 1
            FormChange SpawningPhase
        }
    }
}
```

---

### `T3JoinFight`
**Source:** `terminator_abilities.gon`  

```
T3JoinFight {
    ai_ability SpawnTerminatorMini_Base
    template return
    chain_ability T3YellB

    meta {
        is_move true
        animation portin
    }

    graphics {
        dont_visualize_ai true
    }

    cost {
        allow_offmap_casts true
        must_be_offmap true
        cantrip true
        once_per_fight true
        cant_cast X //if any living minis, cant cast
    }

    target {
        max_range 20
        min_range 0
        X_is custom
        force_ai_target_as_spell true
        prioritize_face_camera true
        allow_any_orientation true
    }

    bonus_passives {
        XIsLivingAlliesWithTag terminator_mini
    }

    damage_instance {
        ai_base_score 100
    }
}
```

---

### `T3YellB`
**Source:** `terminator_abilities.gon`  

```
T3YellB {
    template self_buff

    graphics {
        dont_visualize_ai true
        animation yellb
    }

    damage_instance {
        ai_base_score 99999
    }
}
```

---

## File: `throbbing_king_abilities.gon`

### `TKNG_Roulette`
**Name:** Roulette.  
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_Roulette {
    template spell

    meta {
        name "EABILITY_ROULETTE_NAME"
    }

    graphics {
        prime_animation command3
        custom_priming_animation idleCommand3
        animation releaseCommand3
        dont_visualize_ai true

        affected_particle fx_tentaclestrangle
        miss_particle fx_tentaclestrangleMiss
        fx_is_placeholder_animation true
        fx_random_flip true
        miss_random_delay [0, 60]
        random_delay [70 100]
    }
    
    cost {
        prime 1
    }

    target {
        target_mode none
        aoe_mode all_except_random_empty
        aoe_considers_character_size false
        aoe_excludes_self true
        min_aoe 6
        max_aoe 10
        knockback_mode none
        prioritize_face_camera true
    }

    damage_instance {
        damage 16
        ai_base_score 9999
    }

    self_damage {
        effects {
            EndTurn 1
        }
    }
}
```

---

### `TKNG_Kneel`
**Name:** Kneel.  
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_Kneel {
    template spell

    meta {
        name "EABILITY_KNEEL_NAME"
    }

    graphics {
        prime_animation command2
        custom_priming_animation idleCommand2
        animation releaseCommand2
        dont_visualize_ai true

        affected_particle fx_tentaclestrangle
        miss_particle fx_tentaclestrangleMiss
        fx_is_placeholder_animation true
        fx_random_flip true
        miss_random_delay [0, 60]
        random_delay [70 100]
    }
    
    cost {
        prime 1
    }

    
    target {
        target_mode none
        aoe_mode square
        aoe_considers_character_size true
        aoe_excludes_self true
        min_aoe 1+size
        max_aoe 20
        knockback_mode none
        prioritize_face_camera true
    }

    damage_instance {
        damage 16
        ai_base_score 9999
    }

    self_damage {
        effects {
            EndTurn 1
        }
    }
}
```

---

### `TKNG_GoAway`
**Name:** Go Away.  
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_GoAway {
    template spell

    meta {
        name "EABILITY_GOAWAY_NAME"
    }

    graphics {
        prime_animation command1
        custom_priming_animation idleCommand1
        animation releaseCommand1
        dont_visualize_ai true

        affected_particle fx_tentaclestrangle
        miss_particle fx_tentaclestrangleMiss
        fx_is_placeholder_animation true
        fx_random_flip true
        miss_random_delay [0, 60]
        random_delay [70 100]
    }
    
    cost {
        prime 1
    }

    
    target {
        target_mode none
        aoe_mode all_except_edges
        aoe_considers_character_size false
        aoe_excludes_self true
        knockback_mode none
        prioritize_face_camera true
    }

    damage_instance {
        damage 16
        ai_base_score 9999
    }

    self_damage {
        effects {
            EndTurn 1
        }
    }
}
```

---

### `TKNG_Spread`
**Name:** Spread Out.  
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_Spread {
    template spell

    meta {
        name "EABILITY_SPREADOUT_NAME"
    }

    graphics {
        prime_animation command4
        custom_priming_animation idleCommand4
        animation releaseCommand4
        dont_visualize_ai true

        affected_particle fx_tentaclestrangle
        miss_particle fx_tentaclestrangleMiss
        fx_is_placeholder_animation true
        fx_random_flip true
        miss_random_delay [0, 60]
        random_delay [70 100]
    }
    
    cost {
        prime 1
    }

    target {
        target_mode none
        aoe_mode area_around_all_player_cats
        aoe_considers_character_size false
        aoe_excludes_self true
        min_aoe 1
        max_aoe 2
        knockback_mode none
        prioritize_face_camera true
    }

    damage_instance {
        damage 16
        ai_base_score 9999
    }

    self_damage {
        effects {
            EndTurn 1
        }
    }
}
```

---

### `TKNG_Trash`
**Name:** Vomit Rain  
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_Trash {
    template spawn

    meta {
        name "EABILITY_VOMITRAIN_NAME"
    }
    
    graphics {
        lob true
        animation vomitrain
        lob_height 4
        lob_speed .5
        dont_visualize_ai true
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        max_targets 14
        multihit 14
        stagger_multihit_targets true
    }

    spawn {
        ai_base_score 9999
        object [Clot Dip Poop SmallRock Tumor RandomFoodPickup RandomFoodPickup PoisonFood Coin]

        post_spawn_statuses {
            DoDamage {
                damage 0
                type spell
                damage_tiles all

                effects {
                    ChangeTile WaterTile
                }
                elements [
                    Water
                ]
            }
        }
    }
}
```

---

### `TKNG_GutBall`
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_GutBall {
    template lobbed_attack

    graphics {
        animation gutball
		projectile Meatball
    }

    target {
        min_range 1
        max_range 5
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Slow 2
            Tangled {
                stacks 1
                alt_art TangledMeat
            }
        }
    }
}
```

---

### `TKNG_DeathExplode`
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_DeathExplode {
    template spell
    
    graphics {
        animation dying
        particle none
    }

    target {
        target_mode none
        aoe_mode circle
        min_aoe 0
        max_aoe 20
        aoe_excludes_self true
        aoe_considers_character_size true
    }
    
    damage_instance {
        damage 0
        knockback 10

        ai_base_score 999999
    }
}
```

---

### `TKNG_Laser`
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_Laser {
    template laser

    graphics {
        animation shoot

        beam_clip fx_kingbloodlaser
        beam_cap fx_kingbloodlasercap
    }

    damage_instance {
        damage 3+bonus_ranged_damage

        effects {
            Bleed 2
        }
    }
}
```

---

### `TKNG_Spawn`
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_Spawn {
    template spawn

    graphics {
        lob true
        animation spawn
    }

    target {
        target_mode direction
        aoe_mode custom
        custom_aoe [[-1, 0]]
    }

    spawn {
        object Clot
        ai_base_score 9999
    }
}
```

---

### `TKNG_Hop`
**Source:** `throbbing_king_abilities.gon`  

```
TKNG_Hop {
    variant_of BasicJump

    graphics {
        full_jump_animation hop
        full_jump_sync_frames 45
        full_jump_windup_frames 18
    }
}
```

---

