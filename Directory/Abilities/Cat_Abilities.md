# Abilities/Cat Abilities Directory

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

## File: `butcher_abilities.gon`

### `HogRush`
**Name:** Hog Rush  
**Description:** Trample over to a tile with meat on it.  
**Source:** `butcher_abilities.gon`  

```
HogRush {
    template move
    
    meta {
        name "ABILITY_HOGRUSH_NAME"
        desc "ABILITY_HOGRUSH_DESC"
        animate_name true
        class Butcher
    }

    graphics {
        speed 2
        animation dash
    }

    cost {
        infcantrip true
        mana 7
    }

    temporary_effects {
        Trample 3
    }

    target {
        max_range 100
        restrictions [must_be_moveable must_have_tag must_move]
        target_requires_tag food
        trample_allies_too true
    }
}
```

---

### `HogRush2`
**Description:** Trample over to a tile with meat on it and Cleave all units in your way.  
**Source:** `butcher_abilities.gon`  

```
HogRush2 {
    variant_of HogRush
    
    meta {
        desc "ABILITY_HOGRUSH2_DESC"
    }

    damage_instance {
        damage 3
        override_trample_damage true

        effects {
            Cleave 1
        }
    }
}
```

---

### `Burp`
**Name:** Burp  
**Description:** Inflict Rot on a unit and it moves away from you.  
**Source:** `butcher_abilities.gon`  

```
Burp {
    template melee_attack
    
    meta {
        name "ABILITY_BURP_NAME"
        desc "ABILITY_BURP_DESC"
        class Butcher
    }

    graphics {
        animation burp
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        damage 0
        type status_spell
        incidentally_collects_pickups false

        effects {
            ForceMoveAway 1
            Rot 1
        }
    }
}
```

---

### `Burp2`
**Description:** Inflict Rot 2 and Poison 2 on a unit and it moves away from you.  
**Source:** `butcher_abilities.gon`  

```
Burp2 {
    variant_of Burp

    meta {
        desc "ABILITY_BURP2_DESC"
    }

    damage_instance {
        effects {
            ForceMoveAway 1
            Rot 2
            Poison 2
        }
    }
}
```

---

### `SelfMutilate`
**Name:** Self Harm  
**Description:** Attack yourself with Cleave to gain +2 [img:str].  
**Source:** `butcher_abilities.gon`  

```
SelfMutilate {
    template self_buff
    
    meta {
        name "ABILITY_SELFHARM_NAME"
        desc "ABILITY_SELFHARM_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
        animation selfHarm
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage
        type generic_physical

        effects {
            Cleave 1
            StrengthUp 2
        }
    }
}
```

---

### `SelfMutilate2`
**Description:** Attack yourself at half damage with Cleave to gain +2 [img:str].  
**Source:** `butcher_abilities.gon`  

```
SelfMutilate2 {
    variant_of SelfMutilate

    meta {
        desc "ABILITY_SELFHARM2_DESC"
    }

    damage_instance {
        damage "(5+bonus_melee_ability_damage)*.5"
    }
}
```

---

### `ForceFeed`
**Name:** Force Feed  
**Description:** Heal an adjacent unit and give that unit +1 [img:con] and -1 [img:spd].  
**Source:** `butcher_abilities.gon`  

```
ForceFeed {
    template melee_attack
    
    meta {
        name "ABILITY_FORCEFEED_NAME"
        desc "ABILITY_FORCEFEED_DESC"
        class Butcher
    }

    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        heal 4
        type spell
        incidentally_collects_pickups false

        effects {
            ConstitutionUp 1
            SpeedUp -1
        }
    }
}
```

---

### `ForceFeed2`
**Name:** Force Feed  
**Description:** Heal a unit within range and give that unit +1 [img:con] and -1 [img:spd].  
**Source:** `butcher_abilities.gon`  

```
ForceFeed2 {
    template lobbed_attack
    
    meta {
        name "ABILITY_FORCEFEED_NAME"
        desc "ABILITY_FORCEFEED2_DESC"
        class Butcher
    }

    target {
        min_range 1
        max_range 4
    }

    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        heal 4
        type spell

        effects {
            ConstitutionUp 1
            SpeedUp -1
        }
    }
}
```

---

### `Fartoom`
**Name:** Fartoom!  
**Description:** Lose 25% of your current HP, deal that much damage to adjacent units, and deal Knockback to them.  
**Source:** `butcher_abilities.gon`  

```
Fartoom {
    template spell

    meta {
        name "ABILITY_FARTOOM_NAME"
        desc "ABILITY_FARTOOM_DESC"
        class Butcher
    }

    tags [musical]

    graphics {
        particle none
        animation fartoom
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 1

        aoe_considers_character_size true
        aoe_excludes_self true

        X_is current_health
    }

    self_damage {
        damage "floor(X*.25)"
        piercing true
    }
    
    damage_instance {
        damage "floor(X*.25)"
        knockback "ceil(X*.25/5)"

        elements [
            Explosion
        ]
    }
}
```

---

### `Fartoom2`
**Description:** Lose 25% of your HP, deal that much damage to nearby units, and deal Knockback to them.  
**Source:** `butcher_abilities.gon`  

```
Fartoom2 {
    variant_of Fartoom

    meta {
        desc "ABILITY_FARTOOM2_DESC"
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 2
    }
}
```

---

### `Mutilate`
**Name:** Mutilate  
**Description:** Attack 3-5 times for 1 damage each. These attacks inflict Bleed.  
**Source:** `butcher_abilities.gon`  

```
Mutilate {
    class MultiHitMeleeAttackAbility
    template melee_attack
    
    meta {
        name "ABILITY_MUTILATE_NAME"
        desc "ABILITY_MUTILATE_DESC"
        class Butcher
    }

    graphics {
        start attack
        loop attack
        end attack
    }

    cost {
        infcantrip true
        mana 8
    }

    target {
        multihit_min 3
        multihit_max 5
    }

    damage_instance {
        damage 1

        effects {
            Bleed 1
        }
    }
}
```

---

### `Mutilate2`
**Description:** Attack 3-10 times for 1 damage each. These attacks inflict Bleed.  
**Source:** `butcher_abilities.gon`  

```
Mutilate2 {
    variant_of Mutilate

    meta {
        desc "ABILITY_MUTILATE2_DESC"
    }

    target {
        multihit_min 3
        multihit_max 10
    }
}
```

---

### `SkullBash`
**Name:** Skull Bash  
**Description:** A range 1 dash attack that inflicts Stun and knockback. Also stuns yourself.  
**Source:** `butcher_abilities.gon`  

```
SkullBash {
    template dash_attack
    
    meta {
        name "ABILITY_SKULLBASH_NAME"
        desc "ABILITY_SKULLBASH_DESC"
        class Butcher
        type_icon "defense"
    }
    
    graphics {
        dash_start_animation headbuttdashStart
        dash_animation headbuttdash
        dash_attack_animation headbuttdashEnd
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_range 1
    }
    
    damage_instance {
        damage 2+bonus_melee_ability_damage
        knockback 5

        effects {
            Stun 1
            SelfStun 1
        }
    }
}
```

---

### `SkullBash2`
**Description:** A range 4 dash attack that inflicts Stun and knockback. Has a 50% chance to stun yourself.  
**Source:** `butcher_abilities.gon`  

```
SkullBash2 {
    variant_of SkullBash

    meta {
        desc "ABILITY_SKULLBASH2_DESC"
    }

    target {
        max_range 4
    }

    damage_instance {
        effects {
            SelfStun [1 .5]
        }
    }
}
```

---

### `Shred`
**Name:** Shred  
**Description:** Attack five times for 1 damage each. These attacks inflict all status effects your basic attack does.  
**Source:** `butcher_abilities.gon`  

```
Shred {
    //class MultiHitMeleeAttackAbility
    template melee_attack
    
    meta {
        name "ABILITY_SHRED_NAME"
        desc "ABILITY_SHRED_DESC"
        class Butcher
    }

    graphics {
        animation shred
        //start shred
        //loop shred
        //end shred
    }

    cost {
        infcantrip true
        mana 12
    }

    target {
        multihit 5
    }

    bonus_passives {
        CopyBasicAttackEffects 1
    }

    damage_instance {
        damage 1
    }
}
```

---

### `Shred2`
**Description:** Attack five times with damage that scales with [img:str]. These attacks inflict all status effects your basic attack does.  
**Source:** `butcher_abilities.gon`  

```
Shred2 {
    variant_of Shred

    meta {
        desc "ABILITY_SHRED2_DESC"
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage
    }
}
```

---

### `Chomp`
**Name:** Chomp  
**Description:** A melee attack with Life Steal. If used on an ally, gain +1[img:str]. If used on a pickup, gain double that pickup's effects.  
**Source:** `butcher_abilities.gon`  

```
Chomp {
    template melee_attack
    
    meta {
        name "ABILITY_CHOMP_NAME"
        desc "ABILITY_CHOMP_DESC"
        class Butcher
    }

    graphics {
        animation biteattack
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        hint_can_target_pickups true
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        can_collect_pickups true

        effects {
            Leech 1
            Conditional_Ally {
                ApplyToSource {
                    StrengthUp 1
                }
            }
            CollectsPickups 2
        }
    }
}
```

---

### `Chomp2`
**Description:** A wide melee attack with Life Steal. If used on an ally, gain +1[img:str]. If used on a pickup, gain double that pickup's effects.  
**Source:** `butcher_abilities.gon`  

```
Chomp2 {
    variant_of Chomp

    meta {
        desc "ABILITY_CHOMP2_DESC"
    }

    target {
        aoe_mode custom
        aoe_symmetry none
        custom_aoe [[1, -1] [1, 0] [1, 1]]
    }
}
```

---

### `Succ`
**Name:** SUCC  
**Description:** Collect a pickup within two tiles of you.  
**Source:** `butcher_abilities.gon`  

```
Succ {
    template spell
    
    meta {
        name "ABILITY_SUCC_NAME"
        desc "ABILITY_SUCC_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
        particle fx_windSpell
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    target {
        target_mode tile
        max_aoe 0
        max_range 2
        knockback_mode tile_to_character
        hint_can_target_pickups true
    }
    
    damage_instance {
        damage 0
        type none

        effects {
            CollectsPickups 1
        }

        elements [
            Wind
        ]
    }
}
```

---

### `Succ2`
**Description:** Collect all pickups within two tiles of you.  
**Source:** `butcher_abilities.gon`  

```
Succ2 {
    variant_of Succ

    meta {
        desc "ABILITY_SUCC2_DESC"
    }

    target {
        target_mode none
        max_aoe 2
    }
}
```

---

### `Consume`
**Name:** Consume  
**Description:** Collect all pickups, then become drowsy.  
**Source:** `butcher_abilities.gon`  

```
Consume {
    template spell
    
    meta {
        name "ABILITY_CONSUME_NAME"
        desc "ABILITY_CONSUME_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
		particle DustPoofMedium
        delay 5
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        target_mode none
        max_aoe 20
    }

    self_damage {
        effects {
            Drowsy 1
        }
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

### `Consume2`
**Description:** Collect all pickups, then become drowsy. Gain double the effects of these pickups.  
**Source:** `butcher_abilities.gon`  

```
Consume2 {
    variant_of Consume

    meta {
        desc "ABILITY_CONSUME2_DESC"
    }

    damage_instance {
        effects {
            CollectsPickups 2
        }
    }
}
```

---

### `Trudge`
**Name:** Trudge  
**Description:** Move four tiles. Costs less mana the lower your HP is.  
**Source:** `butcher_abilities.gon`  

```
Trudge {
    template move
    
    meta {
        name "ABILITY_TRUDGE_NAME"
        desc "ABILITY_TRUDGE_DESC"
        animate_name true
        class Butcher
    }

    graphics {

    }

    cost {
        infcantrip true
        mana X
    }

    target {
        max_range 4
        X_is custom
    }
    bonus_passives {
        XIsMultipliedPercentHealth [1 12]
    }
}
```

---

### `Trudge2`
**Description:** Trample over four tiles. Costs less mana the lower your HP is.  
**Source:** `butcher_abilities.gon`  

```
Trudge2 {
    variant_of Trudge

    meta {
        desc "ABILITY_TRUDGE2_DESC"
    }

    temporary_effects {
        Trample 3
    }
}
```

---

### `BodySlam`
**Name:** Body Slam  
**Description:** Jump to a tile within range 2. Damage both yourself and units you land on equal to 25% of your current HP.  
**Source:** `butcher_abilities.gon`  

```
BodySlam {
    template jump_attack

    meta {
        name "ABILITY_BODYSLAM_NAME"
        desc "ABILITY_BODYSLAM_DESC"
        class Butcher
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 6
        infcantrip true
    }
    
    target {
        max_range 2

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none
        X_is current_health
    }

    self_damage {
        damage "floor(X*.25)"
    }

    damage_instance {
        damage "floor(X*.25)"

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `BodySlam2`
**Description:** Jump to a tile within range 2. Damage both yourself and units you land on equal to 25% of your current HP. This attack inflicts Bruise and has a chance to Stun.  
**Source:** `butcher_abilities.gon`  

```
BodySlam2 {
    variant_of BodySlam

    meta {
        desc "ABILITY_BODYSLAM2_DESC"
    }

    damage_instance {
        effects {
            Bruise 1
            Stun [1 .5]
        }
    }
}
```

---

### `BloodMagic`
**Name:** Blood Magic  
**Description:** Take 5 damage and gain 5 mana.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
BloodMagic {
    template self_buff
    
    meta {
        name "ABILITY_BLOODMAGIC_NAME"
        desc "ABILITY_BLOODMAGIC_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
    }
    
    cost {
        mana 0
        act_points 0
        charge 1
    }
    
    damage_instance {
        damage 5
        type none
        cant_miss true

        effects {
            ManaGain 5
        }
    }
}
```

---

### `BloodMagic2`
**Description:** Take 5 damage and gain 10 mana.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
BloodMagic2 {
    variant_of BloodMagic

    meta {
        desc "ABILITY_BLOODMAGIC2_DESC"
    }

    damage_instance {
        effects {
            ManaGain 10
        }
    }
}
```

---

### `SmellBlood`
**Name:** Smell Blood  
**Description:** Until your next turn, if a unit in your attack range takes physical damage from a source that isn't you, you attack that unit.  
**Source:** `butcher_abilities.gon`  

```
SmellBlood {
    template self_buff
    
    meta {
        name "ABILITY_SMELLBLOOD_NAME"
        desc "ABILITY_SMELLBLOOD_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
    }
    
    cost {
        mana 7
        infcantrip true
    }
    
    damage_instance {
        effects {
            SmellBlood 1
        }
    }
}
```

---

### `SmellBlood2`
**Description:** Until your next turn, if a unit in your attack range takes physical damage from a source that isn't you, you attack that unit.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
SmellBlood2 {
    variant_of SmellBlood

    meta {
        desc "ABILITY_SMELLBLOOD2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `Vurp`
**Name:** Vurp  
**Description:** Vomit up the last consumable you ate this battle and equip it.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
Vurp {
    template self_buff
    
    meta {
        name "ABILITY_VURP_NAME"
        desc "ABILITY_VURP_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
		animation pukeatk
    }
    
    cost {
        mana 4
        cantrip true
        requires_empty_trinket true
        requires_consumed_trinket true
        once_per_fight true
    }
    
    damage_instance {
        effects {
            Regurge 1
        }
    }
}
```

---

### `Vurp2`
**Description:** Vomit up the last consumable you ate this battle and equip it.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
Vurp2 {
    variant_of Vurp

    meta {
        desc "ABILITY_VURP2_DESC"
    }

    cost {
        once_per_fight false
    }
}
```

---

### `SliceAndDice`
**Name:** Slice and Dice  
**Description:** Dash forward one tile and do a spin attack with Cleave, then repeat twice more.  
**Source:** `butcher_abilities.gon`  

```
SliceAndDice {
    template dash_attack
    
    meta {
        name "ABILITY_SLICEANDDICE_NAME"
        desc "ABILITY_SLICEANDDICE_DESC"
        class Butcher
    }
    
    graphics {
        dash_start_animation none
        dash_animation spinattackloop
        dash_attack_animation spinattackloop
    }
    
    cost {
        infcantrip true
        mana 9
    }
    
    target {
        aoe_mode cross
        knockback_mode character_to_tile
        max_range 1
    }

    temporary_effects {
        CastAgain 2
    }
    
    damage_instance {
        damage 2+bonus_melee_ability_damage
        effects {
            Cleave 1
        }
    }
}
```

---

### `SliceAndDice2`
**Description:** Dash forward one tile and do a spin attack with Cleave, then repeat four more times.  
**Source:** `butcher_abilities.gon`  

```
SliceAndDice2 {
    variant_of SliceAndDice

    meta {
        desc "ABILITY_SLICEANDDICE2_DESC"
    }

    temporary_effects {
        CastAgain 4
    }
}
```

---

### `LunchTime`
**Name:** Lunch Time  
**Description:** Jump to a food pickup in range 4.  
**Source:** `butcher_abilities.gon`  

```
LunchTime {
    template jump_attack

    meta {
        name "ABILITY_LUNCHTIME_NAME"
        desc "ABILITY_LUNCHTIME_DESC"
        class Butcher
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 3
        infcantrip true
    }
    
    target {
        max_range 4
        min_range 1

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions [aoe_must_be_displaceable must_have_tag must_move]
        target_requires_tag food
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `LunchTime2`
**Description:** Jump to any food pickup.  
**Source:** `butcher_abilities.gon`  

```
LunchTime2 {
    variant_of LunchTime

    meta {
        desc "ABILITY_LUNCHTIME2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `Tromp`
**Name:** Tromp  
**Description:** Trample over one tile. If you trample over a unit, you inflict Bruise on that unit and yourself.  
**Source:** `butcher_abilities.gon`  

```
Tromp {
    template move
    
    meta {
        name "ABILITY_TROMP_NAME"
        desc "ABILITY_TROMP_DESC"
        class Butcher
        animate_name true
    }

    cost {
        infcantrip true
        mana 3
    }

    temporary_effects {
        Trample 3
    }

    target {
        range_mode cross
        max_range 1
        restrictions [must_be_moveable must_move]
        straight_shot true
    }

    damage_instance {
        override_trample_damage true
        damage 3
        effects {
            Bruise 1
            ApplyToSource {
                Bruise 1
            }
        }
    }
}
```

---

### `Tromp2`
**Name:** Tromp  
**Description:** Trample over one tile. If you trample over a unit, you inflict Bruise on that unit.  
**Source:** `butcher_abilities.gon`  

```
Tromp2 {
    template move

    meta {
        name "ABILITY_TROMP_NAME"
        desc "ABILITY_TROMP2_DESC"
        class Butcher
        animate_name true
    }

    cost {
        infcantrip true
        mana 2
    }

    temporary_effects {
        Trample 3
    }

    target {
        range_mode cross
        max_range 1
        restrictions [must_be_moveable must_move]
        straight_shot true
    }

    damage_instance {
        override_trample_damage true
        damage 3
        effects {
            Bruise 1
        }
    }
}
```

---

### `LightenTheLoad`
**Name:** Lighten the Load  
**Description:** Take 25 damage. You take an extra turn after this one.
\[s:.7\](This spell can't be cast on extra turns.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
LightenTheLoad {
    template self_buff
    
    meta {
        name "ABILITY_LIGHTENTHELOAD_NAME"
        desc "ABILITY_LIGHTENTHELOAD_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
		animation selfHarm
    }
    
    cost {
        infcantrip true
        mana 2
        main_turn_only true
    }
    
    damage_instance {
        damage 25
        type melee
        cant_miss true
        crit_chance -999999

        effects {
            TakeExtraTurn 1
        }
    }
}
```

---

### `LightenTheLoad2`
**Description:** Take 15 damage. You take an extra turn after this one.
\[s:.7\](This spell can't be cast on extra turns.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
LightenTheLoad2 {
    variant_of LightenTheLoad

    meta {
        desc "ABILITY_LIGHTENTHELOAD2_DESC"
    }

    damage_instance {
        damage 15
    }
}
```

---

### `Crushinator`
**Name:** Crushinator  
**Description:** This spell only damages Shield. Cleave and inflict Stun on units with Shield. Deals 3 Knockback to units without Shield.  
**Source:** `butcher_abilities.gon`  

```
Crushinator {
    template melee_attack
    
    meta {
        name "ABILITY_CRUSHINATOR_NAME"
        desc "ABILITY_CRUSHINATOR_DESC"
        class Butcher
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 6
    }

    damage_instance {
        damage 20
        damage_shield_only true

        effects {
            Conditional_Shielded {
                Stun 1
                Cleave 1
            }
            Conditional_NotShielded {
                Knockback 3
            }
        }
    }
}
```

---

### `Crushinator2`
**Description:** This spell only damages Shield. Cleave and inflict Stun on units with Shield. Deals 10 Knockback to units without Shield.  
**Source:** `butcher_abilities.gon`  

```
Crushinator2 {
    variant_of Crushinator

    meta {
        desc "ABILITY_CRUSHINATOR2_DESC"
    }

    damage_instance {
        damage 50

        effects {
            Conditional_NotShielded {
                Knockback 10
            }
        }
    }
}
```

---

### `CannonBall`
**Name:** Cannon Ball!  
**Description:** Target any tile. At the beginning of your next turn, jump to that tile. If you land on a unit, stun it.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
CannonBall {
    template jump_attack

    meta {
        name "ABILITY_CANNONBALL_NAME"
        desc "ABILITY_CANNONBALL_DESC"
        class Butcher
    }

    graphics {
        jump_attack_animation land
        //jump_attack_animation cannonBallSplash

        //TODO: jump attack air states- up, up/down, down, and land
    }

    cost {
        mana 4
        cantrip true
    }
    
    target {
        max_range 20
        delayed_trigger true

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none
    }

    damage_instance {
        damage 0

        effects {
            IgnoreSelf 1
            Stun 1
        }
    }
}
```

---

### `CannonBall2`
**Description:** Target any tile. At the beginning of your next turn, jump to that tile. If you land on a unit, damage and stun it.
\[s:.7\](This spell costs less.)\[/s\]
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
CannonBall2 {
    variant_of CannonBall

    meta {
        desc "ABILITY_CANNONBALL2_DESC"
    }

    cost {
        mana 2
    }

    damage_instance {
        damage 10+bonus_melee_ability_damage
    }
}
```

---

### `Monch`
**Name:** Monch  
**Description:** A melee attack with lifesteal. This spell does more damage the less health you have.  
**Source:** `butcher_abilities.gon`  

```
Monch {
    template melee_attack
    
    meta {
        name "ABILITY_MONCH_NAME"
        desc "ABILITY_MONCH_DESC"
        class Butcher
    }

    graphics {
        animation biteattack
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        X_is custom
    }
    bonus_passives {
        XIsMultipliedPercentHealth [14 1]
    }

    damage_instance {
        damage X

        effects {
            Leech 1
        }
    }
}
```

---

### `Monch2`
**Description:** A melee attack with lifesteal. This spell does more damage the less health you have.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
Monch2 {
    variant_of Monch

    meta {
        desc "ABILITY_MONCH2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `DeathWind`
**Name:** Death Wind  
**Description:** Blow wind that inflicts Poison 4 in a cone. The cone is larger the less health you have.  
**Source:** `butcher_abilities.gon`  

```
DeathWind {
    template spell

    meta {
        name "ABILITY_DEATHWIND_NAME"
        desc "ABILITY_DEATHWIND_DESC"
        class Butcher
    }

    graphics {
        delay 4
        particle PoisonPoof
        animation poopfart
        visual_delay_but_simultaneous_damage 8
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe X

        aoe_considers_character_size true
        aoe_excludes_self true
        X_is custom
    }
    bonus_passives {
        XIsMultipliedPercentHealth [6 2]
    }
    
    damage_instance {
        damage 0
        knockback 1
        type status_spell

        effects {
            Poison 4
        }

        elements [
            Wind
        ]
    }
}
```

---

### `DeathWind2`
**Description:** Blow wind that inflicts Poison 4 in a cone. The cone is larger the less health you have.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
DeathWind2 {
    variant_of DeathWind

    meta {
        desc "ABILITY_DEATHWIND2_DESC"
    }

    cost {
        mana 6
    }
}
```

---

### `Spoil`
**Name:** Spoil  
**Description:** Turn all food pickups into Rot Flies.  
**Source:** `butcher_abilities.gon`  

```
Spoil {
    template spell

    meta {
        name "ABILITY_SPOIL_NAME"
        desc "ABILITY_SPOIL_DESC"
        class Butcher
    }

    graphics {
        particle none
    }
    
    cost {
        mana 6
        infcantrip true
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
            Conditional_HasTag {
                tag food

                CanApplyToInanimate {
                    Vaporize 1
                    ObjectOnHitCharacter AllyRotFly
                }
            }
        }
    }
}
```

---

### `Spoil2`
**Description:** Turn all food pickups into Rot Flies.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
Spoil2 {
    variant_of Spoil

    meta {
        desc "ABILITY_SPOIL2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `Grill`
**Name:** Grill  
**Description:** Light a fire under a food pickup on any tile.  
**Source:** `butcher_abilities.gon`  

```
Grill {
    template spell
    
    meta {
        name "ABILITY_GRILL_NAME"
        desc "ABILITY_GRILL_DESC"
        class Butcher
    }

    graphics {
        particle FireSpin
        palette 6
    }

    cost {
        infcantrip true
        mana 2
    }

    target {
        max_aoe 0
        max_range 20
        restrictions [must_have_tag]
        target_requires_tag food
    }

    damage_instance {
        damage 0
        effects {
            ChangeTile FireTile
            Burn 1
        }
        elements [
            Fire
        ]
    }
}
```

---

### `Grill2`
**Description:** Light a fire under any tile.  
**Source:** `butcher_abilities.gon`  

```
Grill2 {
    variant_of Grill
    
    meta {
        desc "ABILITY_GRILL2_DESC"
    }

    target {
        restrictions none
    }
}
```

---

### `Roast`
**Name:** Roast  
**Description:** Breathe a cone of fire.  
**Source:** `butcher_abilities.gon`  

```
Roast {
    template spell

    meta {
        name "ABILITY_ROAST_NAME"
        desc "ABILITY_ROAST_DESC"
        class Butcher
    }

    graphics {
		animation blowFire
        particle FireBlastSmall
        delay 10
        palette 6
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 2

        aoe_considers_character_size true
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 3

        effects {
            Burn 1
        }

        elements [
            Fire
            Wind
        ]
    }
}
```

---

### `Roast2`
**Description:** Breathe a larger cone of fire.  
**Source:** `butcher_abilities.gon`  

```
Roast2 {
    variant_of Roast
    
    meta {
        desc "ABILITY_ROAST2_DESC"
    }

    target {
        max_aoe 4
    }

    damage_instance {
        damage 4

        effects {
            Burn 2
        }
    }
}
```

---

### `BadGas`
**Name:** Bad Gas  
**Description:** Fart on a unit, inflicting Poison 3 and propelling yourself 3 tiles.  
**Source:** `butcher_abilities.gon`  

```
BadGas {
    template melee_attack

    meta {
        name "ABILITY_BADGAS_NAME"
        desc "ABILITY_BADGAS_DESC"
        animate_name false
        class Butcher
    }

    graphics {
        animation poopfartbehind
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        knockback_mode back_orientation
        reverse_target_direction true

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

### `BadGas2`
**Description:** Fart on a unit, inflicting Poison 3 and propelling yourself ten tiles. Units in your path get trampled over.  
**Source:** `butcher_abilities.gon`  

```
BadGas2 {
    variant_of BadGas

    meta {
        desc "ABILITY_BADGAS2_DESC"
    }

    cost {
        infcantrip true
        mana 5
    }

    self_damage {
        knockback -10
        effects {
            KnockbackDamageImmuneUntilSettled 1
            TempTrampleUntilSettled 3
        }
    }
}
```

---

### `ButcherPurge`
**Name:** Purge  
**Description:** Puke on the tile in front of you. You get -1 [img:con] and +2 [img:spd].  
**Source:** `butcher_abilities.gon`  

```
ButcherPurge {
    template lobbed_attack
    
    meta {
        name "ABILITY_PURGE_NAME"
        desc "ABILITY_PURGE_DESC"
        class Butcher
    }

    graphics {
        animation pukeatk
    }
    
    cost {
        infcantrip true
        mana 2
        minimum_con 1
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
    
    self_damage {
        effects {
            ConstitutionUp -1
            SpeedUp 2
        }
    }

    damage_instance {
        damage 1+bonus_ranged_damage

        effects {
            SpawnCreep 1
        }
    }
}
```

---

### `ButcherPurge2`
**Description:** Puke on a tile in range. You get -1 [img:con] and +2 [img:spd].  
**Source:** `butcher_abilities.gon`  

```
ButcherPurge2 {
    variant_of ButcherPurge

    meta {
        desc "ABILITY_PURGE2_DESC"
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
    }
}
```

---

### `Binge`
**Name:** Binge  
**Description:** Gain -1 [img:spd], +1 [img:con], and +1 [img:str].  
**Source:** `butcher_abilities.gon`  

```
Binge {
    template self_buff
    
    meta {
        name "ABILITY_BINGE_NAME"
        desc "ABILITY_BINGE_DESC"
        class Butcher
    }

    graphics {
        animation gulp
    }
    
    cost {
        infcantrip true
        mana 2
        minimum_spd 1
    }
    
    damage_instance {
        effects {
            SpeedUp -1
            ConstitutionUp 1
            StrengthUp 1
        }
    }
}
```

---

### `Binge2`
**Description:** Gain -1 [img:spd], +1 [img:con], +1 [img:str], and heal 4 HP.  
**Source:** `butcher_abilities.gon`  

```
Binge2 {
    variant_of Binge

    meta {
        desc "ABILITY_BINGE2_DESC"
    }

    damage_instance {
        heal 4
    }
}
```

---

### `MyTurn`
**Name:** My Turn!  
**Description:** Steal an allied cat's next turn for yourself.  
**Source:** `butcher_abilities.gon`  

```
MyTurn {
    template targeted_status
    
    meta {
        name "ABILITY_MYTURN_NAME"
        desc "ABILITY_MYTURN_DESC"
        class Butcher
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 1
        max_range 20
        restrictions [must_have_ally must_have_player_cat]
    }
    
    damage_instance {
        damage 0

        effects {
            StealTurn 1
        }
    }
}
```

---

### `MyTurn2`
**Description:** Steal an allied cat's next turn for yourself.
\[s:.7\](This spell costs 1 mana.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
MyTurn2 {
    variant_of MyTurn

    meta {
        desc "ABILITY_MYTURN2_DESC"
    }
    cost {
        mana 1
    }
}
```

---

### `Gib`
**Name:** Gib  
**Description:** Attack a unit in melee range. If this kills it, it becomes 3 food pickups.  
**Source:** `butcher_abilities.gon`  

```
Gib {
    template melee_attack
    
    meta {
        name "ABILITY_GIB_NAME"
        desc "ABILITY_GIB_DESC"
        class Butcher
    }

    graphics {
		animation groundpound
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        damage 3+bonus_melee_ability_damage

        effects {
            SpawnThingIfHitKills Food
            SpawnThingIfHitKills Food
            SpawnThingIfHitKills Food
        }
    }
}
```

---

### `Gib2`
**Description:** Attack a unit in melee range for more damage. If this kills it, it becomes 3 food pickups.  
**Source:** `butcher_abilities.gon`  

```
Gib2 {
    variant_of Gib

    meta {
        desc "ABILITY_GIB2_DESC"
    }

    damage_instance {
        damage 6+bonus_melee_ability_damage
    }
}
```

---

### `Swallow`
**Name:** Swallow  
**Description:** Eat a unit and take damage equal to that unit's remaining HP. You can't swallow bosses or large units.  
**Source:** `butcher_abilities.gon`  

```
Swallow {
    template targeted_status
    
    meta {
        name "ABILITY_SWALLOW_NAME"
        desc "ABILITY_SWALLOW_DESC"
        class Butcher
    }

    graphics {
        animation biteattack
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 1
        min_range 1
    }

    damage_instance {
        damage 0
        can_collect_pickups true

        effects {
            CollectsPickups 1
            SwallowSmallCharacter 100%
        }

        elements [
            Wind
        ]
    }
}
```

---

### `Swallow2`
**Description:** Eat a unit within range 2 and take damage equal to half of that unit's remaining HP. You can't swallow bosses or large units.  
**Source:** `butcher_abilities.gon`  

```
Swallow2 {
    variant_of Swallow

    meta {
        desc "ABILITY_SWALLOW2_DESC"
    }

    target {
        max_range 2
        min_range 1
    }

    damage_instance {
        damage 0
        can_collect_pickups true

        effects {
            SwallowSmallCharacter 50%
        }
    }
}
```

---

### `Track`
**Name:** Track  
**Description:** Trample one tile toward the nearest food pickup.  
**Source:** `butcher_abilities.gon`  

```
Track {
    template self_buff
    
    meta {
        name "ABILITY_TRACK_NAME"
        desc "ABILITY_TRACK_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
        animation none
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            ForceMoveTowardsTaggedObject {
                ability MoveOneTrample
                tag food
            }
        }
    }
}
```

---

### `Track2`
**Description:** Trample two tiles toward the nearest food pickup.  
**Source:** `butcher_abilities.gon`  

```
Track2 {
    variant_of Track

    meta {
        desc "ABILITY_TRACK2_DESC"
    }

    effects {
        ForceMoveTowardsTaggedObject {
            ability MoveTwoTrample
        }
    }
}
```

---

### `Sharpen`
**Name:** Sharpen  
**Description:** Your weapon gains +1 damage for the rest of the battle.  
**Source:** `butcher_abilities.gon`  

```
Sharpen {
    template self_buff
    
    meta {
        name "ABILITY_SHARPEN_NAME"
        desc "ABILITY_SHARPEN_DESC"
        class Butcher
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            CurrentWeaponDamageUp 1
        }
    }
}
```

---

### `Sharpen2`
**Description:** Your weapon gains +1 damage for the rest of the battle and you gain +1 Damage.  
**Source:** `butcher_abilities.gon`  

```
Sharpen2 {
    variant_of Sharpen

    meta {
        desc "ABILITY_SHARPEN2_DESC"
    }

    damage_instance {
        effects {
            DamageUp 1
        }
    }
}
```

---

### `FireFart`
**Name:** Fire Fart  
**Description:** Inflict Poison 2 and Burn 2 on a unit in melee range.  
**Source:** `butcher_abilities.gon`  

```
FireFart {
    template spell

    meta {
        name "ABILITY_FIREFART_NAME"
        desc "ABILITY_FIREFART_DESC"
        class Butcher
    }

    graphics {
        delay 4
        particle FireBlastMushroom
        animation poopfart
        palette 6
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 1

        aoe_considers_character_size true
        aoe_excludes_self true
        X_is custom
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Poison 2
            Burn 2
        }

        elements [
            Fire
        ]
    }
}
```

---

### `FireFart2`
**Description:** Inflict Poison 2 and Burn 2 in a small cone.  
**Source:** `butcher_abilities.gon`  

```
FireFart2 {
    variant_of FireFart

    meta {
        desc "ABILITY_FIREFART2_DESC"
    }

    target {
        max_aoe 2
    }
}
```

---

### `RoughToss`
**Name:** Rough Toss  
**Description:** Throw an adjacent unit to an empty tile, dealing a lot of damage to that unit.  
**Source:** `butcher_abilities.gon`  

```
RoughToss {
    template throw_attack
    
    meta {
        name "ABILITY_ROUGHTOSS_NAME"
        desc "ABILITY_ROUGHTOSS_DESC"
        class Butcher
        type_icon "defense"
    }

    graphics {
        animation knockupatk
    }

    cost {
        mana 6
        infcantrip true
    }
    
    target {
        min_range 3
        max_range 4
    }
    
    damage_instance {
        damage 7+bonus_melee_ability_damage
        blocked_damage 7+bonus_melee_ability_damage
    }
}
```

---

### `RoughToss2`
**Description:** Throw an adjacent unit to another tile (even if it isnt empty), dealing a lot of damage to that unit and whatever it lands on.  
**Source:** `butcher_abilities.gon`  

```
RoughToss2 {
    variant_of RoughToss

    meta {
        desc "ABILITY_ROUGHTOSS2_DESC"
    }

    target {
        max_range 7
        restrictions none
    }
}
```

---

### `Bowl`
**Name:** Bowl  
**Description:** Roll the bowling ball cat. If it hits something, deal 10 damage in a large cone with knockback.  
**Source:** `butcher_abilities.gon`  

```
Bowl {
    template spell

    meta {
        name "ABILITY_BOWL_NAME"
        desc "ABILITY_BOWL_DESC"
        class Butcher
    }

    graphics {
        particle none
        animation knockswatatk
    }
    
    cost {
        cantrip true
        mana 0
    }
    
    target {
        range_mode square
        max_aoe 0
        max_range 1
        knockback_mode character_to_target
        restrictions must_have_tag
        target_requires_tag bowling_ball
    }
    
    damage_instance {
        damage 0
        makes_contact false

        effects {
            ImmediateUseDirectionalAbility BowlDash
        }
    }
}
```

---

### `Bowl2`
**Description:** Roll the bowling ball cat. If it hits something, deal 15 damage and inflict Bruise in a large cone with knockback.  
**Source:** `butcher_abilities.gon`  

```
Bowl2 {
    variant_of Bowl

    meta {
        desc "ABILITY_BOWL2_DESC"
    }

    damage_instance {
        effects {
            ImmediateUseDirectionalAbility BowlDash2
        }
    }
}
```

---

### `BowlDash`
**Source:** `butcher_abilities.gon`  

```
BowlDash { //2nd util ability for Bowl
    template dash_attack

    graphics {
        dash_start_animation none
        dash_animation roll
        dash_attack_animation none
        aoe_spell_on_land true

        speed .5

        delay 3
        particle Earthquake
        visual_delay_but_simultaneous_damage 3
    }
    
    cost {
        mana 0
    }
    
    target {
        target_mode direction8
        max_range 10

        aoe_mode cone8
        knockback_mode character_to_tile
        min_aoe 1
        max_aoe 4
    }
    
    damage_instance {
        type spell
        damage 10
        knockback 10
        force_adjacent_and_diagonal_contact true
        two_way_contact true

        effects {
            DoScreenShake 1
        }
    }
}
```

---

### `BowlDash2`
**Source:** `butcher_abilities.gon`  

```
BowlDash2 {
    variant_of BowlDash

    damage_instance {
        damage 15

        effects {
            Bruise 1
        }
    }
}
```

---

### `TaintedOffering`
**Name:** Tainted Offering  
**Description:** Jump to any open tile and fall asleep. While asleep, inflict Rot 1 and Poison 1 on units that contact you.  
**Source:** `butcher_abilities.gon`  

```
TaintedOffering {
    template jump_attack

    meta {
        name "ABILITY_TAINTEDOFFERING_NAME"
        desc "ABILITY_TAINTEDOFFERING_DESC"
        class Butcher
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 4
        infcantrip true
    }
    
    target {
        max_range 20
        max_aoe 0
        min_aoe 0
    }

    self_damage {
        effects {
            Sleep 1

            Conditional_FirstApplicationThisTurn {
                key TaintedOffering
                TempPassiveWhileHasStatus {
                    status Sleep

                    MeleeRevengeDamage {
                        effects {
                            Poison 1
                            Rot 1
                        }
                    }
                }
            }
        }
    }
}
```

---

### `TaintedOffering2`
**Description:** Jump to any open tile and fall asleep. While asleep, inflict Rot 2 and Poison 2 on units that contact you.  
**Source:** `butcher_abilities.gon`  

```
TaintedOffering2 {
    variant_of TaintedOffering

    meta {
        desc "ABILITY_TAINTEDOFFERING2_DESC"
    }

    self_damage {
        effects {
            Conditional_FirstApplicationThisTurn {
                key TaintedOffering2
                TempPassiveWhileHasStatus {
                    MeleeRevengeDamage {
                        effects {
                            Poison 2
                            Rot 2
                        }
                    }
                }
            }
        }
    }
}
```

---

### `DeliciousScent`
**Name:** Delicious Scent  
**Description:** Inflict Attraction on all enemies within range 4.  
**Source:** `butcher_abilities.gon`  

```
DeliciousScent {
    template spell
    
    meta {
        name "ABILITY_DELICIOUSSCENT_NAME"
        desc "ABILITY_DELICIOUSSCENT_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
        particle none
    }
    
    cost {
        infcantrip true
        mana 10
    }
    
    target {
        target_mode none
        max_aoe 4
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0

        effects {
            Conditional_Enemy {
                Attraction 1
            }
        }
    }
}
```

---

### `DeliciousScent2`
**Name:** Delicious Scent  
**Description:** Jump to a tile, then inflict Attraction on all enemies within range 4.  
**Source:** `butcher_abilities.gon`  

```
DeliciousScent2 {
    template jump_attack

    meta {
        name "ABILITY_DELICIOUSSCENT_NAME"
        desc "ABILITY_DELICIOUSSCENT2_DESC"
        class Butcher
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 10
        infcantrip true
    }
    
    target {
        max_range 4
        max_aoe 4
        aoe_mode standard
        min_aoe 0
        aoe_excludes_self true
    }

    damage_instance {
        damage 0
        type spell

        effects {
            Conditional_Enemy {
                Attraction 1
            }
        }
    }
}
```

---

### `Cough`
**Name:** Cough  
**Description:** Take 2 damage.
Summon a Rot Fly.  
**Source:** `butcher_abilities.gon`  

```
Cough {
    template spawn

    meta {
        name "ABILITY_COUGH_NAME"
        desc "ABILITY_COUGH_DESC"
        class Butcher
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    self_damage {
        damage 2
    }

    spawn {
        object AllyRotFly
    }
}
```

---

### `Cough2`
**Description:** Take 2 damage.
Summon a [img:champion] Rot Fly.  
**Source:** `butcher_abilities.gon`  

```
Cough2 {
    variant_of Cough

    meta {
        desc "ABILITY_COUGH2_DESC"
    }

    self_damage {
        damage 2
    }

    spawn {
        object AllyRotFly_Champion
    }
}
```

---

### `Reflux`
**Name:** Reflux  
**Description:** Take 2 damage and gain Burn 2, then fire a projectile that spawns a lava tile at short range.  
**Source:** `butcher_abilities.gon`  

```
Reflux {
    template lobbed_attack
    
    meta {
        name "ABILITY_REFLUX_NAME"
        desc "ABILITY_REFLUX_DESC"
        class Butcher
    }

    graphics {
        animation pukeatk
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        min_range 1
        max_range 2
        
        knockback_mode character_to_tile
    }
    
    self_damage {
        damage 2
        effects {
            Burn 2
        }
        elements [
            Fire
        ]
    }

    damage_instance {
        damage 1+bonus_ranged_damage

        effects {
            ChangeTile LavaTile
        }

        elements [
            Fire
        ]
    }
}
```

---

### `Reflux2`
**Description:** Take 2 damage and gain Burn 2, then fire a projectile that spawns a lava tile at long range.  
**Source:** `butcher_abilities.gon`  

```
Reflux2 {
    variant_of Reflux

    meta {
        desc "ABILITY_REFLUX2_DESC"
    }

    target {
        max_range 5
    }
}
```

---

### `Tryptophan`
**Name:** Yawn  
**Description:** You and adjacent units fall asleep  
**Source:** `butcher_abilities.gon`  

```
Tryptophan {
    template spell
    
    meta {
        name "ABILITY_TRYPTOPHAN_NAME"
        desc "ABILITY_TRYPTOPHAN_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
        particle none
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        target_mode none
        max_aoe 1
    }
    
    damage_instance {
        damage 0

        effects {
            Sleep 1
        }
    }
}
```

---

### `Tryptophan2`
**Description:** You and adjacent units fall asleep. You gain all stats up and heal 4.  
**Source:** `butcher_abilities.gon`  

```
Tryptophan2 {
    variant_of Tryptophan

    meta {
        desc "ABILITY_TRYPTOPHAN2_DESC"
    }

    self_damage {
        heal 4
        effects {
            AllStatsUp 1
        }
    }
}
```

---

### `HookBind`
**Name:** Hook Bind  
**Description:** Melee attack that immobilizes.  
**Source:** `butcher_abilities.gon`  

```
HookBind {
    template melee_attack
    
    meta {
        name "ABILITY_HOOKBIND_NAME"
        desc "ABILITY_HOOKBIND_DESC"
        class Butcher
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage

        effects {
            Immobile 1
        }
    }
}
```

---

### `HookBind2`
**Description:** Melee attack that immobilizes and inflicts Bleed 2.  
**Source:** `butcher_abilities.gon`  

```
HookBind2 {
    variant_of HookBind

    meta {
        desc "ABILITY_HOOKBIND2_DESC"
    }

    damage_instance {
        effects {
            Bleed 2
        }
    }
}
```

---

### `Regurge`
**Name:** Regurge  
**Description:** Take 2 damage and spawn a food pickup.  
**Source:** `butcher_abilities.gon`  

```
Regurge {
    template spawn

    meta {
        name "ABILITY_REGURGE_NAME"
        desc "ABILITY_REGURGE_DESC"
        class Butcher
        type_icon "misc"
    }
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_range 1
        max_range 3
        restrictions [aoe_must_exist]
    }

    spawn {
        object Food
        layer pickups
    }

    self_damage {
        damage 2
    }
}
```

---

### `Regurge2`
**Description:** Take 2 damage and spawn a big food pickup.  
**Source:** `butcher_abilities.gon`  

```
Regurge2 {
    variant_of Regurge

    meta {
        desc "ABILITY_REGURGE2_DESC"
    }

    target {
        max_range 5
    }

    spawn {
        object BigFood
        layer pickups
    }
}
```

---

### `Grapnel`
**Name:** Grapnel  
**Description:** Lob a hook at an object and pull yourself to it. Trample over tiles in your path.  
**Source:** `butcher_abilities.gon`  

```
Grapnel {
    template lobbed_attack
    
    meta {
        name "ABILITY_GRAPNEL_NAME"
        desc "ABILITY_GRAPNEL_DESC"
        class Butcher
        type_icon "movement"
    }

    graphics {
        animation invthrow

        projectile HookProjectile
        chain_movieclip ChainLink
        chain_distance .25
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        max_range 10
        range_mode 8cross
    }

    damage_instance {
        damage 0

        effects {
            CanApplyToInanimate {
                ApplyToSource {
                    TempTrampleUntilSettled 3
                }
            }
            PullSourceToTarget 1
        }
    }
}
```

---

### `Grapnel2`
**Description:** Lob a hook at an object and pull yourself to it. Trample over tiles in your path.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
Grapnel2 {
    variant_of Grapnel

    meta {
        desc "ABILITY_GRAPNEL2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `Rehook`
**Name:** Rehook  
**Description:** Refresh your weapon ability.  
**Source:** `butcher_abilities.gon`  

```
Rehook {
    template self_buff
    
    meta {
        name "ABILITY_REHOOK_NAME"
        desc "ABILITY_REHOOK_DESC"
        class Butcher
    }
	
    graphics {
		animation equipWeapon
    }
    
    tags [noncopyable]

    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            RefreshWeaponAbility 1
        }
    }
}
```

---

### `Rehook2`
**Description:** Refresh your weapon and movement action.  
**Source:** `butcher_abilities.gon`  

```
Rehook2 {
    variant_of Rehook

    meta {
        desc "ABILITY_REHOOK2_DESC"
    }
    
    damage_instance {
        effects {
            RefreshMovePoints 1
        }
    }
}
```

---

### `Contaminate`
**Name:** Contaminate  
**Description:** Collect an adjacent pickup. Instead of that pickup's normal effects, add Poison 1 to your weapon for the rest of the battle.  
**Source:** `butcher_abilities.gon`  

```
Contaminate {
    template targeted_status
    
    meta {
        name "ABILITY_CONTAMINATE_NAME"
        desc "ABILITY_CONTAMINATE_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
		animation weaponslam
    }

    cost {
        infcantrip true
        mana 2
    }

    target {
        max_range 1

        restrictions must_have_tag
        target_requires_tag pickup
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            CollectsPickupsWithAltEffects {
                CurrentWeaponAddPoison 1
            }
        }
    }
}
```

---

### `Contaminate2`
**Description:** Collect a pickup in range 5. Instead of that pickup's normal effects, add Poison 1 to your weapon for the rest of the battle.  
**Source:** `butcher_abilities.gon`  

```
Contaminate2 {
    variant_of Contaminate

    meta {
        desc "ABILITY_CONTAMINATE2_DESC"
    }

    target {
        max_range 5
    }
}
```

---

### `LodgeHook`
**Name:** Lodge Hook  
**Description:** Inflict Bleed 10 on an adjacent unit. You can't use your weapon for the rest of the battle.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
LodgeHook {
    template melee_attack
    
    meta {
        name "ABILITY_LODGEHOOK_NAME"
        desc "ABILITY_LODGEHOOK_DESC"
        class Butcher
        type_icon "misc"
    }

    graphics {
        animation weaponslam
    }

    cost {
        act_points 0
        must_have_weapon true
        once_per_fight true
        mana 0
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Bleed 10
            ApplyToSource {
                DisableWeapon 1
            }
        }
    }
}
```

---

### `LodgeHook2`
**Description:** Inflict Bleed 10, Immobilize 2, and Bruise 2 on an adjacent unit. You can't use your weapon for the rest of the battle.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `butcher_abilities.gon`  

```
LodgeHook2 {
    variant_of LodgeHook

    meta {
        desc "ABILITY_LODGEHOOK2_DESC"
    }

    damage_instance {
        effects {
            Bleed 10
            Immobile 2
            Bruise 2
        }
    }
}
```

---

### `Butcher`
**Name:** Butcher  
**Description:** Kill every unit with 3 or less health. They become meat.  
**Source:** `butcher_abilities.gon`  

```
Butcher {
    template spell

    meta {
        name "ABILITY_BUTCHER_NAME"
        desc "ABILITY_BUTCHER_DESC"
        class Butcher
    }

    graphics {
        particle none
    }
    
    cost {
        mana 5
        infcantrip true
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
            Conditional_HealthThreshold {
                threshold_flat 3
                SpawnThingIfHitKills Food
                Die 1
            }
        }
    }
}
```

---

### `Butcher2`
**Description:** Kill every unit with 3 or less health. They become meat. Gain 5 health for each unit killed.  
**Source:** `butcher_abilities.gon`  

```
Butcher2 {
    variant_of Butcher

    meta {
        desc "ABILITY_BUTCHER2_DESC"
    }

    damage_instance {
        effects {
            Conditional_HealthThreshold {
                threshold_flat 3
                FlatLeech 5
                SpawnThingIfHitKills Food
                Instakill 999
            }
        }
    }
}
```

---

### `Chonkwalk`
**Name:** Chonkwalk  
**Description:** Deal 5 damage to yourself. Refresh your movement action.  
**Source:** `butcher_abilities.gon`  

```
Chonkwalk {
    template self_buff
    
    meta {
        name "ABILITY_CHONKWALK_NAME"
        desc "ABILITY_CHONKWALK_DESC"
        class Butcher
        type_icon "move"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        damage 5
        type melee
        cant_miss true
        crit_chance -999999

        effects {
            RefreshMovePoints 1
        }
    }
}
```

---

### `Chonkwalk2`
**Description:** Deal 5 damage to yourself. Refresh your movement action.
PASSIVE: You have Trample.  
**Source:** `butcher_abilities.gon`  

```
Chonkwalk2 {
    variant_of Chonkwalk

    meta {
        desc "ABILITY_CHONKWALK2_DESC"
    }

    bonus_passives {
        Trample 3
    }
}
```

---

### `Indigestion_Fart`
**Source:** `butcher_abilities.gon`  

```
Indigestion_Fart { //util ability for Indigestion passive, no icon needed
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
        damage 0

        effects {
            Poison 3
        }
        
        elements [
            Poison
        ]
    }
}
```

---

### `Indigestion_Fart2`
**Source:** `butcher_abilities.gon`  

```
Indigestion_Fart2 { //util ability for Indigestion passive, no icon needed
    variant_of Indigestion_Fart

    graphics {
        particle FireBlastMushroom
        palette 6
    }

    damage_instance {
        effects {
            Poison 3
            Burn 3
        }
        
        elements [
            Poison
            Fire
        ]
    }
}
```

---

## File: `colorless_abilities.gon`

### `Block`
**Name:** Block  
**Description:** Gain +2 [img:shield].  
**Source:** `colorless_abilities.gon`  

```
Block {
    template self_buff
    
    meta {
        name "ABILITY_BLOCK_NAME"
        desc "ABILITY_BLOCK_DESC"
        class Colorless
        type_icon "defense"
    }

    graphics {
        animation block
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            Shield 2
        }
    }
}
```

---

### `Block2`
**Description:** Gain +5 [img:shield].  
**Source:** `colorless_abilities.gon`  

```
Block2 {
    variant_of Block

    meta {
        desc "ABILITY_BLOCK2_DESC"
    }

    damage_instance {
        effects {
            Shield 5
        }
    }
}
```

---

### `Rest`
**Name:** Rest  
**Description:** Heal some HP, then fall asleep.  
**Source:** `colorless_abilities.gon`  

```
Rest {
    template self_buff
    
    meta {
        name "ABILITY_REST_NAME"
        desc "ABILITY_REST_DESC"
        class Colorless
    }

    graphics {
		animation none
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        heal 10

        effects {
            Sleep 1
        }
    }
}
```

---

### `Rest2`
**Description:** Heal a lot of HP, then fall asleep.  
**Source:** `colorless_abilities.gon`  

```
Rest2 {
    variant_of Rest

    meta {
        desc "ABILITY_REST2_DESC"
    }

    damage_instance {
        heal 20

        effects {
            Sleep 1
        }
    }
}
```

---

### `Brace`
**Name:** Brace  
**Description:** Gain +1 temporary Brace until your next turn.  
**Source:** `colorless_abilities.gon`  

```
Brace {
    template self_buff
    
    meta {
        name "ABLITY_BRACE_NAME"
        desc "ABLITY_BRACE_DESC"
        class Colorless
        type_icon "defense"
    }

    graphics {
        animation brace
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            Temporary {
                status Brace
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `Brace2`
**Name:** Brace  
**Description:** Gain +1 temporary Brace and +1 temporary Thorns until your next turn.  
**Source:** `colorless_abilities.gon`  

```
Brace2 {
    template self_buff
    
    meta {
        name "ABLITY_BRACE_NAME"
        desc "ABLITY_BRACE2_DESC"
        class Colorless
        type_icon "defense"
    }

    graphics {
        animation brace
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        effects {
            Temporary {
                status Brace
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
            Temporary {
                status Thorns
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `Groom`
**Name:** Groom  
**Description:** Remove all of the debuffs on yourself or an adjacent unit.  
**Source:** `colorless_abilities.gon`  

```
Groom {
    template spell

    meta {
        name "ABILITY_GROOM_NAME"
        desc "ABILITY_GROOM_DESC"
        class Colorless
        type_icon "heal"
    }
    
    graphics {
        animation lickAttack
        particle none
    }
    
    cost {
        mana 5
        infcantrip true
    }
    
    target {
        max_aoe 0
        max_range 1
        min_range 0
    }
    
    damage_instance {
        heal 0
        makes_contact true
        
        effects {
            Cleanse 0
        }
    }
}
```

---

### `Groom2`
**Description:** Remove all of the debuffs and heal a little HP to yourself or an adjacent unit.  
**Source:** `colorless_abilities.gon`  

```
Groom2 {
    variant_of Groom

    meta {
        desc "ABILITY_GROOM2_DESC"
    }

    damage_instance {
        heal 2
        
        effects {
            Cleanse 0
        }
    }
}
```

---

### `Roll`
**Name:** Roll  
**Description:** Roll up to three tiles in a straight line.  
**Source:** `colorless_abilities.gon`  

```
Roll {
    template move
    
    meta {
        name "ABILITY_ROLL_NAME"
        desc "ABILITY_ROLL_DESC"
        class Colorless
        animate_name true
    }
    
    graphics {
        sync_speed 22
        max_tiles_single_loop 5
        ignore_slowtiles true
        move_start_animation startroll
        animation roll
        move_end_animation endroll
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        range_mode cross
        max_range 3
        restrictions [must_be_moveable must_move]
        straight_shot true
    }
}
```

---

### `Roll2`
**Description:** Roll up to ten tiles in a straight line.  
**Source:** `colorless_abilities.gon`  

```
Roll2 {
    variant_of Roll

    meta {
        desc "ABILITY_ROLL2_DESC"
    }

    target {
        max_range 10
    }
}
```

---

### `SharpenClaws`
**Name:** Sharpen Claws  
**Description:** Gain +1 [img:str].  
**Source:** `colorless_abilities.gon`  

```
SharpenClaws {
    template self_buff
    
    meta {
        name "ABILITY_SHARPENCLAWS_NAME"
        desc "ABILITY_SHARPENCLAWS_DESC"
        class Colorless
    }

    graphics {
		animation fx_statup
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            StrengthUp 1
        }
    }
}
```

---

### `SharpenClaws2`
**Description:** Gain +1 [img:str].
Bonus Passive: Your basic attack inflicts Bleed.  
**Source:** `colorless_abilities.gon`  

```
SharpenClaws2 {
    variant_of SharpenClaws

    meta {
        desc "ABILITY_SHARPENCLAWS2_DESC"
    }

    bonus_passives {
        AddStatusToBasicAttack {
            Bleed 1
        }
    }
}
```

---

### `Reach`
**Name:** Reach  
**Description:** Your next basic attack has +1 range.  
**Source:** `colorless_abilities.gon`  

```
Reach {
    template self_buff
    
    meta {
        name "ABILITY_REACH_NAME"
        desc "ABILITY_REACH_DESC"
        class Colorless
    }

    graphics {
	    particle fx_statup
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            NextAttackBonusRange 1
        }
    }
}
```

---

### `Reach2`
**Description:** Your next basic attack has +3 range.  
**Source:** `colorless_abilities.gon`  

```
Reach2 {
    variant_of Reach

    meta {
        desc "ABILITY_REACH2_DESC"
    }

    damage_instance {
        effects {
            NextAttackBonusRange 3
        }
    }
}
```

---

### `ManaDrain`
**Name:** Borrow Mana  
**Description:** Steal up to 5 mana from an ally.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
ManaDrain {
    template targeted_status
    
    meta {
        name "ABILITY_BORROWMANA_NAME"
        desc "ABILITY_BORROWMANA_DESC"
        class Colorless
    }

    graphics {
    }

    
    cost {
        mana 0
        act_points 0
        charge 1
    }

    target {
        min_range 1
        max_range 20

        restrictions [must_have_ally]
    }
    
    damage_instance {
        effects {
            ManaSteal 5
        }
    }
}
```

---

### `ManaDrain2`
**Description:** Steal all of an ally's mana.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
ManaDrain2 {
    variant_of ManaDrain

    meta {
        desc "ABILITY_BORROWMANA2_DESC"
    }

    damage_instance {
        effects {
            ManaSteal -1
        }
    }
}
```

---

### `SoothingGlow`
**Name:** Soothing Glow  
**Description:** Heal yourself 1.  
**Source:** `colorless_abilities.gon`  

```
SoothingGlow {
    template self_buff
    
    meta {
        name "ABILITY_SOOTHINGGLOW_NAME"
        desc "ABILITY_SOOTHINGGLOW_DESC"
        class Colorless
    }

    graphics {
		particle HealSmall
    }

    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        heal 1

        elements [
            Holy
        ]
    }
}
```

---

### `SoothingGlow2`
**Description:** Heal yourself 1 and gain +1 to a random stat.  
**Source:** `colorless_abilities.gon`  

```
SoothingGlow2 {
    variant_of SoothingGlow

    meta {
        desc "ABILITY_SOOTHINGGLOW2_DESC"
    }

    damage_instance {
        effects {
            RandomStatUp 1
        }
    }
}
```

---

### `Ponder`
**Name:** Ponder  
**Description:** Gain +1 [img:int].  
**Source:** `colorless_abilities.gon`  

```
Ponder {
    template self_buff
    
    meta {
        name "ABILITY_PONDER_NAME"
        desc "ABILITY_PONDER_DESC"
        class Colorless
    }

    graphics {
        animation thinking
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            IntelligenceUp 1
        }
    }
}
```

---

### `Ponder2`
**Description:** Gain +1 [img:int] and conjure a random bonus ability.  
**Source:** `colorless_abilities.gon`  

```
Ponder2 {
    variant_of Ponder

    meta {
        desc "ABILITY_PONDER2_DESC"
    }

    damage_instance {
        effects {
            ConjureBonusAbility random
        }
    }
}
```

---

### `Focus`
**Name:** Focus  
**Description:** Gain +1 [img:dex].  
**Source:** `colorless_abilities.gon`  

```
Focus {
    template self_buff
    
    meta {
        name "ABILITY_FOCUS_NAME"
        desc "ABILITY_FOCUS_DESC"
        class Colorless
    }

    graphics {
		particle fx_statup
		animation backflipLoop
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            DexterityUp 1
        }
    }
}
```

---

### `Focus2`
**Description:** Gain +1 [img:dex].
Bonus Passive: +25% critical hit chance.  
**Source:** `colorless_abilities.gon`  

```
Focus2 {
    variant_of Focus

    meta {
        desc "ABILITY_FOCUS2_DESC"
    }

    bonus_passives {
        CritChanceUp 25
    }
}
```

---

### `Metabolize`
**Name:** Metabolize  
**Description:** Gain +1 [img:con].  
**Source:** `colorless_abilities.gon`  

```
Metabolize {
    template self_buff
    
    meta {
        name "ABILITY_METABOLIZE_NAME"
        desc "ABILITY_METABOLIZE_DESC"
        class Colorless
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            ConstitutionUp 1
        }
    }
}
```

---

### `Metabolize2`
**Description:** Gain +1 [img:con].
Bonus Passive: +3 Health Regeneration.  
**Source:** `colorless_abilities.gon`  

```
Metabolize2 {
    variant_of Metabolize

    meta {
        desc "ABILITY_METABOLIZE2_DESC"
    }

    bonus_passives {
        HealthRegenUp 3
    }
}
```

---

### `Brainstorm`
**Name:** Brainstorm  
**Description:** Reduce the costs of your other spells by 1 mana.  
**Source:** `colorless_abilities.gon`  

```
Brainstorm {
    template self_buff
    
    meta {
        name "ABILITY_BRAINSTORM_NAME"
        desc "ABILITY_BRAINSTORM_DESC"
        class Colorless
    }
    
    graphics {
		animation thinking
    }

    cost {
        infcantrip true
        mana 7
    }
    
    damage_instance {
        effects {
            ReduceManaCostExcludeBrainstorm 1
        }
    }
}
```

---

### `Brainstorm2`
**Name:** Brainstorm  
**Description:** Reduce the cost of ALL of your spells by 1 mana.  
**Source:** `colorless_abilities.gon`  

```
Brainstorm2 {
    template self_buff
    
    meta {
        name "ABILITY_BRAINSTORM_NAME"
        desc "ABILITY_BRAINSTORM2_DESC"
        class Colorless
    }
    
    graphics {
    }

    cost {
        infcantrip true
        mana 7
    }
    
    damage_instance {
        effects {
            ReduceManaCost 1
        }
    }
}
```

---

### `Momentum`
**Name:** Momentum  
**Description:** This turn, every time you move a tile, increase crit chance by 5% until the end of the turn  
**Source:** `colorless_abilities.gon`  

```
Momentum { //REMOVED
    template self_buff
    
    meta {
        name "Momentum"
        desc "This turn, every time you move a tile, increase crit chance by 5% until the end of the turn"
        class Colorless
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            TilesMovedToCritChance 1
        }
    }
}
```

---

### `Momentum2`
**Source:** `colorless_abilities.gon`  

```
Momentum2 {
    variant_of Momentum

    damage_instance {
        effects {
            TilesMovedToStrength 1
        }
    }
}
```

---

### `TapLand`
**Name:** Tap Land  
**Description:** At the end of your turn, gain 1 mana for each tile you moved this turn after casting this ability.  
**Source:** `colorless_abilities.gon`  

```
TapLand { //REMOVED
    template self_buff
    
    meta {
        name "Tap Land"
        desc "At the end of your turn, gain 1 mana for each tile you moved this turn after casting this ability."
        class Colorless
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            TilesMovedToMana 1
        }
    }
}
```

---

### `TapLand2`
**Source:** `colorless_abilities.gon`  

```
TapLand2 {
    variant_of TapLand
}
```

---

### `GainThorns`
**Name:** Claws Out  
**Description:** Gain +1 Thorns.  
**Source:** `colorless_abilities.gon`  

```
GainThorns {
    template self_buff
    
    meta {
        name "ABILITY_CLAWSOUT_NAME"
        desc "ABILITY_CLAWSOUT_DESC"
        class Colorless
    }

    graphics {
		animation showclaws
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            Thorns 1
        }
    }
}
```

---

### `GainThorns2`
**Description:** Gain +1 Thorns.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
GainThorns2 {
    variant_of GainThorns

    meta {
        desc "ABILITY_CLAWSOUT2_DESC"
    }

    cost {
        mana 2
    }
}
```

---

### `HolyStep`
**Name:** Holy Step  
**Description:** At the end of your turn, heal neighbors for 1 health for each tile you moved after casting this ability.  
**Source:** `colorless_abilities.gon`  

```
HolyStep { //REMOVED
    template self_buff
    
    meta {
        name "Holy Step"
        desc "At the end of your turn, heal neighbors for 1 health for each tile you moved after casting this ability."
        class Colorless
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            TilesMovedToNeighborHeal level
        }
    }
}
```

---

### `HolyStep2`
**Source:** `colorless_abilities.gon`  

```
HolyStep2 {
    variant_of HolyStep
}
```

---

### `LoveTap`
**Name:** Love Tap  
**Description:** Your next attack or spell heals instead of doing damage  
**Source:** `colorless_abilities.gon`  

```
LoveTap { //REMOVED
    template self_buff
    
    meta {
        name "Love Tap"
        desc "Your next attack or spell heals instead of doing damage"
        class Colorless
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            NextAbilityHeals 1
        }
    }
}
```

---

### `LoveTap2`
**Source:** `colorless_abilities.gon`  

```
LoveTap2 {
    variant_of LoveTap
}
```

---

### `PrepareToJump`
**Name:** Hop  
**Description:** Hop up to 2 tiles away.  
**Source:** `colorless_abilities.gon`  

```
PrepareToJump {
    template jump_attack
    
    meta {
        name "ABILITY_PREPARETOJUMP_NAME"
        desc "ABILITY_PREPARETOJUMP_DESC"
        class Colorless
        type_icon "movement"
    }

    graphics {
        jump_attack_animation land
    }

    target { 
        target_mode tile

        min_range 1
        max_range 2
        
        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        
        range_display_include_character_size true
        restrictions must_be_moveable
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        type none
        damage 0
    }
}
```

---

### `PrepareToJump2`
**Description:** Hop up to 4 tiles away.  
**Source:** `colorless_abilities.gon`  

```
PrepareToJump2 {
    variant_of PrepareToJump

    meta {
        desc "ABILITY_PREPARETOJUMP2_DESC"
    }

    target { 
        max_range 4
    }
}
```

---

### `MarkJump`
**Source:** `colorless_abilities.gon`  

```
MarkJump { //UTILITY MOVE NEEDED FOR (the old version of) PrepareToJump2
    variant_of BasicJump

    graphics {
    }

    target { 
        min_range 1
        max_range mov
        
        target_mode tile
        
        aoe_mode cross
        min_aoe 1
        max_aoe 1
        
        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode character_to_tile

        range_display_include_character_size true
        restrictions must_be_moveable
    }

    damage_instance {
        type spell
        damage 0
        effects {
            Marked 1
        }
    }
}
```

---

### `BoostSpellRange`
**Name:** Boost  
**Description:** Gain +1 Magic Damage until end of turn.  
**Source:** `colorless_abilities.gon`  

```
BoostSpellRange {
    template self_buff
    
    meta {
        name "ABILITY_SPELLBOOSTRANGE_NAME"
        desc "ABILITY_SPELLBOOSTRANGE_DESC"
        class Colorless
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            TempSpellDamageUp 1
        }
    }
}
```

---

### `BoostSpellRange2`
**Description:** Gain +1 Magic Damage until end of turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BoostSpellRange2 {
    variant_of BoostSpellRange

    meta {
        desc "ABILITY_SPELLBOOSTRANGE2_DESC"
    }

    cost {
        mana 2
    }

    damage_instance {
        effects {
            TempSpellDamageUp 1
        }
    }
}
```

---

### `PushMove`
**Name:** Steam Roller  
**Description:** Trample over 1 tile.  
**Source:** `colorless_abilities.gon`  

```
PushMove {
    template move
    
    meta {
        name "ABILITY_STEAMROLLER_NAME"
        desc "ABILITY_STEAMROLLER_DESC"
        class Colorless
        animate_name true
    }
	
    graphics {
        move_start_animation startroll
        animation roll
        move_end_animation endroll
    }

    cost {
        infcantrip true
        mana 4
    }

    temporary_effects {
        Trample 3
    }

    target {
        range_mode cross
        max_range 1
        restrictions [must_be_moveable must_move]
        straight_shot true
    }

    damage_instance {
        override_trample_damage true
        damage 3
    }
}
```

---

### `PushMove2`
**Description:** Trample over 3 tiles.  
**Source:** `colorless_abilities.gon`  

```
PushMove2 {
    variant_of PushMove

    meta {
        desc "ABILITY_STEAMROLLER2_DESC"
    }

    target {
        range_mode ground_move
        max_range 3
        straight_shot false
    }
}
```

---

### `Gamble`
**Name:** Gamble  
**Description:** Gain +2% critical hit chance. If your next attack is critical, deal +100% more damage and spawn coins.  
**Source:** `colorless_abilities.gon`  

```
Gamble {
    template self_buff
    
    meta {
        name "ABILITY_GAMBLE_NAME"
        desc "ABILITY_GAMBLE_DESC"
        class Colorless
    }

    graphics {
		animation coinFlip
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        effects {
            CritChanceUp 2
            NextAttackSpecialCrit 1
        }
    }
}
```

---

### `Gamble2`
**Description:** Gain +2% critical hit chance. If your next attack is critical, deal +200% more damage and spawn more coins.  
**Source:** `colorless_abilities.gon`  

```
Gamble2 {
    variant_of Gamble

    meta {
        desc "ABILITY_GAMBLE2_DESC"
    }

    damage_instance {
        effects {
            CritChanceUp 2
            NextAttackSpecialCrit {
                extra_coins_per_stack 2
                crit_multiplier_bonus 2
                luck_increase 1
            }
        }
    }
}
```

---

### `SoulReap`
**Name:** Soul Reap  
**Description:** Deal 1 damage to a unit within five tiles. If this kills it, gain 5 mana.  
**Source:** `colorless_abilities.gon`  

```
SoulReap {
    template spell
    
    meta {
        name "ABILITY_SOULREAP_NAME"
        desc "ABILITY_SOULREAP_DESC"
        class Colorless
    }
    
    graphics {
        particle MagicMissleBlast
		animation pointout
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 0
        min_range 1
        max_range 5
    }
    
    damage_instance {
        damage 1
        effects {
            ApplyToSourceOnKill {
                ManaGain 5
            }
        }
    }
}
```

---

### `SoulReap2`
**Description:** Deal 1 damage to any unit. If this kills it, gain 5 mana.  
**Source:** `colorless_abilities.gon`  

```
SoulReap2 {
    variant_of SoulReap

    meta {
        desc "ABILITY_SOULREAP2_DESC"
    }

    target {
        max_aoe 0
        max_range 20
    }

    damage_instance {
        effects {
            ApplyToSourceOnKill {
                ManaGain 5
                AllStatsUp 1
            }
        }
    }
}
```

---

### `Hunt`
**Name:** Hunt  
**Description:** A ranged attack that turns anything it kills into meat.  
**Source:** `colorless_abilities.gon`  

```
Hunt {
    template lobbed_attack
    
    meta {
        name "ABILITY_HUNT_NAME"
        desc "ABILITY_HUNT_DESC"
        class Colorless
    }

    graphics {
		projectile ArrowProjectile
		animation throwArrow
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 4
    }
    
    damage_instance {
        damage 2+bonus_ranged_damage
        effects {
            SpawnThingIfHitKills BigFood
        }
    }
}
```

---

### `Hunt2`
**Description:** A stronger ranged attack that turns anything it kills into meat.  
**Source:** `colorless_abilities.gon`  

```
Hunt2 {
    variant_of Hunt

    meta {
        desc "ABILITY_HUNT2_DESC"
    }

    damage_instance {
        damage 4+bonus_ranged_damage
        effects {
            SpawnThingIfHitKills BiggestFood
        }
    }
}
```

---

### `Flex`
**Name:** Flex  
**Description:** Gain +1 temporary Brace until your next turn and deal 1 knockback to each adjacent unit.  
**Source:** `colorless_abilities.gon`  

```
Flex {
    template self_buff
    
    meta {
        name "ABILITY_FLEX_NAME"
        desc "ABILITY_FLEX_DESC"
        class Colorless
        type_icon "defense"
    }

    graphics {
        animation flex
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        aoe_mode standard
        max_aoe 1
        aoe_excludes_self true
        knockback_mode character_to_tile
    }

    self_damage {
        damage 0
        effects {
            Temporary {
                status Brace
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
        }
    }
    
    damage_instance {
        damage 0
        knockback 1
        layer all
    }
}
```

---

### `Flex2`
**Description:** Gain +1 temporary Brace until your next turn and deal 3 knockback to each adjacent unit.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Flex2 {
    variant_of Flex

    meta {
        desc "ABILITY_FLEX2_DESC"
    }

    cost {
        mana 3
    }

    damage_instance {
        damage 0
        knockback 3
    }
}
```

---

### `HolyBlood`
**Name:** HolyBlood  
**Description:** Reduce the next damage you take, then heal all neignbors by the amount of damage you take.  
**Source:** `colorless_abilities.gon`  

```
HolyBlood { //REMOVED
    template self_buff
    
    meta {
        name "HolyBlood"
        desc "Reduce the next damage you take, then heal all neignbors by the amount of damage you take."
        class Colorless
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            NextDamageReduceAndHealAllies 1
        }
    }
}
```

---

### `HolyBlood2`
**Source:** `colorless_abilities.gon`  

```
HolyBlood2 {
    variant_of HolyBlood
}
```

---

### `Dart`
**Name:** Dart  
**Description:** Throw a nail that ignores shield.  
**Source:** `colorless_abilities.gon`  

```
Dart {
    template straightshot_attack
    
    meta {
        name "ABILITY_DART_NAME"
        desc "ABILITY_DART_DESC"
        class Colorless
    }

    graphics {
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        max_aoe 3+bonus_range
    }
    
    damage_instance {
        damage 2
        piercing true
    }
}
```

---

### `Dart2`
**Description:** Throw a stronger nail that ignores shield.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Dart2 {
    variant_of Dart

     meta {
        desc "ABILITY_DART2_DESC"
    }

    cost {
        mana 4
    }

    damage_instance {
        damage 4
    }
}
```

---

### `Smack`
**Name:** Smack  
**Description:** A weak melee attack.  
**Source:** `colorless_abilities.gon`  

```
Smack {
    template melee_attack
    
    meta {
        name "ABILITY_SMACK_NAME"
        desc "ABILITY_SMACK_DESC"
        class Colorless
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        damage 2
        type melee
    }
}
```

---

### `Smack2`
**Description:** A weak melee attack with a chance to repeat.  
**Source:** `colorless_abilities.gon`  

```
Smack2 {
    variant_of Smack

    meta {
        desc "ABILITY_SMACK2_DESC"
    }

    cost {
        mana 4
    }

    temporary_effects {
        Fury 75
    }
}
```

---

### `Spit`
**Name:** Spit  
**Description:** Spit attack with infinite range that deals 1 damage.  
**Source:** `colorless_abilities.gon`  

```
Spit {
    template lobbed_attack
    
    meta {
        name "ABILITY_SPIT_NAME"
        desc "ABILITY_SPIT_DESC"
        class Colorless
    }

    graphics {
        single_projectile true
		projectile spitprojectile
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 1
        max_range 20
    }

    damage_instance {
        damage 1

        elements [
            Water
        ]
    }
}
```

---

### `Spit2`
**Description:** Spit attack with infinite range that deals 2 damage in an area.  
**Source:** `colorless_abilities.gon`  

```
Spit2 {
    variant_of Spit

    meta {
        desc "ABILITY_SPIT2_DESC"
    }

    target {
        max_aoe 1
    }

    damage_instance {
        damage 2
    }
}
```

---

### `FetusSpit`
**Source:** `colorless_abilities.gon`  

```
FetusSpit {
    variant_of Spit

    meta {
        ability_icon "Spit"
    }
    
    cost {
        infcantrip false
        mana 0
    }
}
```

---

### `MiniHook`
**Name:** Minihook  
**Description:** Pull a unit towards you.  
**Source:** `colorless_abilities.gon`  

```
MiniHook {
    template straightshot_attack

    meta {
        name "ABILITY_MINIHOOK_NAME"
        desc "ABILITY_MINIHOOK_DESC"
        class Colorless
        type_icon "ranged"
    }
    
    cost {
        mana 3
        infcantrip true
    }

    target {
        max_aoe 3

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

### `MiniHook2`
**Description:** Pull a unit towards you. Deal 1 damage and inflict 1 Bleed on them.  
**Source:** `colorless_abilities.gon`  

```
MiniHook2 {
    variant_of MiniHook

    meta {
        desc "ABILITY_MINIHOOK2_DESC"
    }

    target {
        max_aoe 5
    }

    damage_instance {
        damage 1
        effects {
            Bleed 1
        }
    }
}
```

---

### `MiniDistract`
**Name:** Over There!  
**Description:** Adjacent units turn away from you.  
**Source:** `colorless_abilities.gon`  

```
MiniDistract {
    template spell

    meta {
        name "ABILITY_OVERTHERE_NAME"
        desc "ABILITY_OVERTHERE_DESC"
        class Colorless
        type_icon "misc"
    }

    graphics {
	    particle none
	    animation pointout
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 1

        aoe_considers_character_size true
        aoe_excludes_self true
        knockback_mode character_to_tile_4snap
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

### `MiniDistract2`
**Description:** Units within three tiles of you turn away from you.  
**Source:** `colorless_abilities.gon`  

```
MiniDistract2 {
    variant_of MiniDistract

    meta {
        desc "ABILITY_OVERTHERE2_DESC"
    }

    target {
        max_aoe 3
    }
}
```

---

### `ButtScoot`
**Name:** Butt Scoot  
**Description:** Move 1 tile, leaving a maggot familiar behind you.  
**Source:** `colorless_abilities.gon`  

```
ButtScoot {
    template move
    
    meta {
        name "ABILITY_BUTTSCOOT_NAME"
        desc "ABILITY_BUTTSCOOT_DESC"
        class Colorless
    }

    graphics {
        //sync_speed 150
        max_tiles_single_loop 1
        ignore_slowtiles true
        move_start_animation buttScootStart
        animation buttScootLoop
        move_end_animation buttScootEnd
    }

    cost {
        infcantrip true
        move_points 0
        mana 4
    }

    temporary_effects {
        LeaveBehind {
            object CharmedMaggot
        }
    }

    target {
        max_range 1
    }
}
```

---

### `ButtScoot2`
**Description:** Move up to 3 tiles, leaving a maggot familiar behind you.  
**Source:** `colorless_abilities.gon`  

```
ButtScoot2 {
    variant_of ButtScoot

    meta {
        desc "ABILITY_BUTTSCOOT2_DESC"
    }

    cost {
        mana 3
    }

    target {
        max_range 3
    }
}
```

---

### `Confusion`
**Name:** Confusion  
**Description:** Inflict Confusion 2 on a unit.  
**Source:** `colorless_abilities.gon`  

```
Confusion {
    template spell

    meta {
        name "ABILITY_CONFUSION_NAME"
        desc "ABILITY_CONFUSION_DESC"
        class Colorless
    }

    graphics {
		particle confusionStars
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_aoe 0
        max_range 3
    }
    
    damage_instance {
        damage 0

        effects {
            Confusion 2
        }
    }
}
```

---

### `Confusion2`
**Description:** Inflict Confusion 4 on units in an area.  
**Source:** `colorless_abilities.gon`  

```
Confusion2 {
    variant_of Confusion

    meta {
        desc "ABILITY_CONFUSION2_DESC"
    }

    target {
        max_aoe 1
    }
    
    damage_instance {
        effects {
            Confusion 4
        }
    }
}
```

---

### `PlayDead`
**Name:** Play Dead  
**Description:** Down yourself. You don't get injured.  
**Source:** `colorless_abilities.gon`  

```
PlayDead {
    template self_buff
    
    meta {
        name "ABILITY_PLAYDEAD_NAME"
        desc "ABILITY_PLAYDEAD_DESC"
        class Colorless
        type_icon "defense"
    }

    graphics {
		animation none
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            SafeDie 1
        }
    }
}
```

---

### `PlayDead2`
**Description:** Down yourself. You don't get injured. Revive at the end of the next round at full HP.  
**Source:** `colorless_abilities.gon`  

```
PlayDead2 {
    variant_of PlayDead

    meta {
        desc "ABILITY_PLAYDEAD2_DESC"
    }

    damage_instance {
        effects {
            ReviveNextRound 2
        }
    }
}
```

---

### `Reflect`
**Name:** Reflect  
**Description:** Reflect the next projectile that hits you back at the attacker.  
**Source:** `colorless_abilities.gon`  

```
Reflect {
    template self_buff
    
    meta {
        name "ABILITY_REFLECT_NAME"
        desc "ABILITY_REFLECT_DESC"
        class Colorless
        type_icon "defense"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            Reflect 1
        }
    }
}
```

---

### `Reflect2`
**Description:** You or another unit reflects the next projectile that hits them back at the attacker.  
**Source:** `colorless_abilities.gon`  

```
Reflect2 {
    variant_of Reflect

    meta {
        desc "ABILITY_REFLECT2_DESC"
    }

    graphics {
    }
    
    target {
        target_mode tile
        min_range 0
        max_range 4
    }

    cost {
        mana 4
    }
}
```

---

### `HealBolt`
**Name:** Healing Bolt  
**Description:** A lightning bolt that heals and has a chance to Stun.  
**Source:** `colorless_abilities.gon`  

```
HealBolt {
    template spell

    meta {
        name "ABILITY_HEALINGBOLT_NAME"
        desc "ABILITY_HEALINGBOLT_DESC"
        class Colorless
    }

    graphics {
        particle Bolt
        animation castspell
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        max_aoe 0
        max_range 3
    }
    
    damage_instance {
        heal 5
        
        effects {
            Stun [1, .25]
        }
        
        elements [
            Electric
            Holy
        ]
    }
}
```

---

### `HealBolt2`
**Name:** Healing Bolt  
**Description:** A lightning bolt that heals allies and has a chance to Stun enemies.  
**Source:** `colorless_abilities.gon`  

```
HealBolt2 {
    template spell

    meta {
        name "ABILITY_HEALINGBOLT_NAME"
        desc "ABILITY_HEALINGBOLT2_DESC"
        class Colorless
    }

    graphics {
        particle Bolt
        animation castspell
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        max_aoe 0
        max_range 3
    }
    
    damage_instance {
        heal 5
        
        effects {
            Conditional_Enemy {
                Stun [1, .25]
            }
            DontHealEnemies 1
        }
        
        elements [
            Electric
            Holy
        ]
    }
}
```

---

### `SlipThrough`
**Name:** Slip Through  
**Description:** Roll up to two tiles in a diagonal line.  
**Source:** `colorless_abilities.gon`  

```
SlipThrough {
    template move
    
    meta {
        name "ABILITY_SLIPTHROUGH_NAME"
        desc "ABILITY_SLIPTHROUGH_DESC"
        class Colorless
    }

    graphics {
        sync_speed 22
        max_tiles_single_loop 5
        ignore_slowtiles true
        move_start_animation startroll
        animation roll
        move_end_animation endroll
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        range_mode diagcross
        max_range 2
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_diagonals true
    }
}
```

---

### `SlipThrough2`
**Description:** Roll any number of tiles in a diagonal line.  
**Source:** `colorless_abilities.gon`  

```
SlipThrough2 {
    variant_of SlipThrough

    meta {
        desc "ABILITY_SLIPTHROUGH2_DESC"
    }

    target {
        max_range 10
    }
}
```

---

### `Dump`
**Name:** Dump  
**Description:** Spawn a poop on an adjacent tile.  
**Source:** `colorless_abilities.gon`  

```
Dump {
    template melee_attack

    meta {
        name "ABILITY_DUMP_NAME"
        desc "ABILITY_DUMP_DESC"
        class Colorless
        type_icon "defense"
    }

    graphics {
        animation poopfart
    }

    cost {
        mana 3
        infcantrip true
    }
    
    target {
        target_mode direction
        
        aoe_mode line
        min_aoe 1
        max_aoe 1

        restrictions [aoe_must_be_displaceable aoe_must_exist]
    }

    damage_instance {
        damage 0
        cant_miss true
        incidentally_collects_pickups false

        effects {
            Displace 1
            ObjectOnHit {
                object Poop
            }
        }
    }
}
```

---

### `Dump2`
**Description:** Spawn a poop on an adjacent tile. Inflict Poison 3 and a 15% chance to Stun if you poop on a unit.  
**Source:** `colorless_abilities.gon`  

```
Dump2 {
    variant_of Dump

    meta {
        desc "ABILITY_DUMP2_DESC"
    }

    damage_instance {
        effects {
            Poison 3
            Stun [1 .15]
        }
    }
}
```

---

### `Snacks`
**Name:** Snacks  
**Description:** Heal yourself or another unit within four tiles 1 HP.  
**Source:** `colorless_abilities.gon`  

```
Snacks {
    template spell
    
    meta {
        name "ABILITY_SNACK_NAME"
        desc "ABILITY_SNACK_DESC"
        class Colorless
    }

    graphics {
        affected_particle HealMed
        use_projectile true
        animation throwobject
		projectile Fishball
    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 0
        min_range 0
        max_range 4
    }
    
    damage_instance {
        heal 1
        type spell
    }
}
```

---

### `Snacks2`
**Description:** Heal yourself or another unit 1 HP. 50% chance to also give +1 [img:con].  
**Source:** `colorless_abilities.gon`  

```
Snacks2 {
    variant_of Snacks

    meta {
        desc "ABILITY_SNACK2_DESC"
    }

    target {
        max_range 20
    }
    
    damage_instance {
        effects {
            ConstitutionUp [1 .5]
        }
    }
}
```

---

### `FeatherFeet`
**Name:** Feather Feet  
**Description:** Gain +1 [img:spd].  
**Source:** `colorless_abilities.gon`  

```
FeatherFeet {
    template self_buff
    
    meta {
        name "ABILITY_FEATHERFEET_NAME"
        desc "ABILITY_FEATHERFEET_DESC"
        class Colorless
    }

    graphics {
		particle fx_statup
		animation hopinplace
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            SpeedUp 1
        }
    }
}
```

---

### `FeatherFeet2`
**Description:** Gain +1 [img:spd].
Bonus Passive: You're unaffected by tile effects.  
**Source:** `colorless_abilities.gon`  

```
FeatherFeet2 {
    variant_of FeatherFeet

    meta {
        desc "ABILITY_FEATHERFEET2_DESC"
    }

    bonus_passives {
        IgnoreTiles 1
    }
}
```

---

### `Reduce`
**Name:** Reduce  
**Description:** Gain +20% dodge chance, +4 [img:spd], and -2 Damage.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Reduce {
    template self_buff
    
    meta {
        name "ABILITY_REDUCE_NAME"
        desc "ABILITY_REDUCE_DESC"
        class Colorless
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 5
        once_per_fight true
    }
    
    damage_instance {
        effects {
            SpeedUp 4
            DamageUp -2
            DodgeChance_Status 20
            SizeScale .6
        }
    }
}
```

---

### `Reduce2`
**Description:** Gain +20% dodge chance, +4 [img:spd], and -2 Damage.
\[s:.7\](This spell costs 0 mana. Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Reduce2 {
    variant_of Reduce

    meta {
        desc "ABILITY_REDUCE2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `Nerf`
**Name:** Nerf  
**Description:** Inflict -1 Damage on a unit.  
**Source:** `colorless_abilities.gon`  

```
Nerf {
    template spell

    meta {
        name "ABILITY_NERF_NAME"
        desc "ABILITY_NERF_DESC"
        class Colorless
    }

    graphics {
	    particle fx_statdown
		animation pointout
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_range 3
        max_aoe 0
    }

    damage_instance {
        damage 0
        
        effects {
            DamageUp -1
        }
    }
}
```

---

### `Nerf2`
**Description:** Inflict -1 Damage and -1 [img:con] on a unit.  
**Source:** `colorless_abilities.gon`  

```
Nerf2 {
    variant_of Nerf

    meta {
        desc "ABILITY_NERF2_DESC"
    }

    damage_instance {
        effects {
            ConstitutionUp -1
        }
    }
}
```

---

### `Trip`
**Name:** Trip  
**Description:** Immobilize an adjacent unit.
[s:.7]This only has a 25% chance to work on boss units and large enemies.\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Trip {
    template melee_attack
    
    meta {
        name "ABILITY_TRIP_NAME"
        desc "ABILITY_TRIP_DESC"
        class Colorless
        type_icon "debuff"
    }

    graphics {
        animation trip
    }

    cost {
        infcantrip true
        mana 4
    }

    damage_instance {
        damage 0
        type melee

        effects {
            Conditional_BossOrBig {
                Immobile [1 .25]
            }
            Conditional_NotBossOrBig {
                Immobile 1
            }
        }
    }
}
```

---

### `Trip2`
**Name:** Trip  
**Description:** Immobilize a unit in range 4.
[s:.7]This only has a 25% chance to work on boss units and large enemies.\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Trip2 {
    template lobbed_attack
    
    meta {
        name "ABILITY_TRIP_NAME"
        desc "ABILITY_TRIP2_DESC"
        class Colorless
        type_icon "debuff"
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        range_min 1
        range_max 4
    }

    damage_instance {
        damage 0
        type ranged

        effects {
            Conditional_BossOrBig {
                Immobile [1 .25]
            }
            Conditional_NotBossOrBig {
                Immobile 1
            }
        }
    }
}
```

---

### `Copycat`
**Name:** Copycat  
**Description:** This spell is a copy of the most recent spell an allied cat cast.  
**Source:** `colorless_abilities.gon`  

```
Copycat {
    template self_buff
    
    meta {
        name "ABILITY_COPYCAT_NAME"
        desc "ABILITY_COPYCAT_DESC"
        class Colorless
        type_icon "misc"
    }

    tags [noncopyable]
    
    graphics {
        animation thumbsup
    }

    cost {
        cant_cast true
        mana 5
    }

    bonus_passives {
        CopyCatPassive_Initializer 1
    }
}
```

---

### `Copycat2`
**Description:** This spell is an upgraded copy of the most recent spell an allied cat cast.  
**Source:** `colorless_abilities.gon`  

```
Copycat2 {
    variant_of Copycat
    
    meta {
        desc "ABILITY_COPYCAT2_DESC"
    }

    bonus_passives {
        CopyCatPassive_Initializer 2
    }
}
```

---

### `Metronome`
**Name:** Metronome  
**Description:** Cast a random spell.  
**Source:** `colorless_abilities.gon`  

```
Metronome {
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

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        effects {
            Metronome 1
        }
    }
}
```

---

### `Metronome2`
**Description:** Cast a random upgraded spell.  
**Source:** `colorless_abilities.gon`  

```
Metronome2 {
    variant_of Metronome
    
    meta {
        desc "ABILITY_METRONOME2_DESC"
    }

    damage_instance {
        effects {
            Metronome 2
        }
    }
}
```

---

### `DollUp`
**Name:** Doll Up  
**Description:** Gain +1 [img:cha].  
**Source:** `colorless_abilities.gon`  

```
DollUp {
    template self_buff
    
    meta {
        name "ABILITY_DOLLUP_NAME"
        desc "ABILITY_DOLLUP_DESC"
        class Colorless
    }

    graphics {
		particle fx_statup
		animation blowKiss
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        effects {
            CharismaUp 1
        }
    }
}
```

---

### `DollUp2`
**Description:** Gain +1 [img:cha].
Bonus Passive: You have a chance to inflict Charm on units that contact or attack you. This chance increases with your [img:cha].  
**Source:** `colorless_abilities.gon`  

```
DollUp2 {
    variant_of DollUp

    meta {
        desc "ABILITY_DOLLUP2_DESC"
    }

    bonus_passives {
        RevengeDamage {
            effects {
                Charmed [1, .1+.02*cha]
            }
        }
    }
}
```

---

### `StackTheDeck`
**Name:** Stack the Deck  
**Description:** Gain +1 [img:lck].  
**Source:** `colorless_abilities.gon`  

```
StackTheDeck {
    template self_buff
    
    meta {
        name "ABILITY_STACKTHEDECK_NAME"
        desc "ABILITY_STACKTHEDECK_DESC"
        class Colorless
    }

    graphics {
        animation cheat
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            LuckUp 1
        }
    }
}
```

---

### `StackTheDeck2`
**Description:** Gain +1 [img:lck]. You have +99 [img:lck] during your next action.  
**Source:** `colorless_abilities.gon`  

```
StackTheDeck2 {
    variant_of StackTheDeck

    meta {
        desc "ABILITY_STACKTHEDECK2_DESC"
    }

    damage_instance {
        effects {
            LuckUp 1
            NextActionLuckUp 99
        }
    }
}
```

---

### `Infiltrate`
**Name:** Tunnel  
**Description:** Dig to any open tile.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Infiltrate {
    template teleport
    
    meta {
        name "ABILITY_INFILTRATE_NAME"
        desc "ABILITY_INFILTRATE_DESC"
        animate_name true
        class Colorless
    }

    graphics {
        animation_out digDown
        animation_in digUp
    }

    cost {
        infcantrip true
        mana 3
        once_per_fight true
    }

    target {
        max_range 20
    }
}
```

---

### `Infiltrate2`
**Description:** Dig to any open tile.
\[s:.7\](Castable once per battle. This spell costs 0 mana.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Infiltrate2 {
    variant_of Infiltrate

    meta {
        desc "ABILITY_INFILTRATE2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `Burst`
**Name:** Burst  
**Description:** Fire a magical blast.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Burst {
    template spell

    meta {
        name "ABILITY_BURST_NAME"
        desc "ABILITY_BURST_DESC"
        class Colorless
    }

    graphics {
        particle BigMagicMissileBlast
        use_projectile true
        projectile MagicMissileProjectile
        lob_height 1
        speed 20
        animation castspell
    }
    
    cost {
        infcantrip true
        mana 7
        once_per_fight true
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

### `Burst2`
**Description:** Fire a magical blast.
\[s:.7\](This spell costs 0 mana. Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Burst2 {
    variant_of Burst

    meta {
        desc "ABILITY_BURST2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `Suppress`
**Name:** Stun  
**Description:** Chuck a rock at a unit, inflicting Stun on that unit.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Suppress {
    template lobbed_attack

    meta {
        name "ABILITY_SUPPRESS_NAME"
        desc "ABILITY_SUPPRESS_DESC"
        class Colorless
    }

    graphics {
        projectile SmallRock
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 5
        once_per_fight true
    }
    
    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 1+bonus_ranged_damage

        effects {
            Stun 1
            BounceObject SmallRock
        }
    }
}
```

---

### `Suppress2`
**Description:** Chuck a rock at a unit, inflicting Stun on that unit.
\[s:.7\](This spell costs 0 mana. Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Suppress2 {
    variant_of Suppress

    meta {
        desc "ABILITY_SUPPRESS2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `Endeavor`
**Name:** Second Wind  
**Description:** Refresh your basic attack, movement, weapon, and trinket action.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Endeavor {
    template self_buff

    meta {
        name "ABILITY_SECONDWIND_NAME"
        desc "ABILITY_SECONDWIND_DESC"
        class Colorless
    }
	
    tags [noncopyable]

    graphics {
        animation proud
    }

    cost {
        infcantrip true
        mana 8
        once_per_fight true
    }

    damage_instance {
        effects {
            RefreshMovePoints 1
            RefreshActPoints 1
            RefreshItemAbilities 1
        }
    }
}
```

---

### `Endeavor2`
**Description:** Refresh your basic attack, movement, weapon, and trinket action.
\[s:.7\](This spell costs 0 mana. Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Endeavor2 {
    variant_of Endeavor

    meta {
        desc "ABILITY_SECONDWIND2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `Endeavor_Auto`
**Source:** `colorless_abilities.gon`  

```
Endeavor_Auto {
    variant_of Endeavor
    damage_instance {
        effects {
            CanceledQueuedInput 1
        }
    }
}
```

---

### `LotteryShottery`
**Name:** Rat Roulette  
**Description:** Deal 1 damage to a random unit. If you kill that unit, take an extra turn.  
**Source:** `colorless_abilities.gon`  

```
LotteryShottery {
    template lobbed_attack
    
    meta {
        name "ABILITY_RATROULETTE_NAME"
        desc "ABILITY_RATROULETTE_DESC"
        class Colorless
    }
    
    graphics {
        particle MagicMissleBlast
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        target_mode random_tile
        min_range 0
        max_range 20

        restrictions must_have_animate_character
    }
    
    damage_instance {
        damage 1
        effects {
            ApplyToSourceOnKill {
                TakeExtraTurn 1
            }
        }
    }
}
```

---

### `LotteryShottery2`
**Description:** Deal 2 damage to a random unit. If you kill that unit, take an extra turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
LotteryShottery2 {
    variant_of LotteryShottery

    meta {
        desc "ABILITY_RATROULETTE2_DESC"
    }

    cost {
        mana 5
    }

    damage_instance {
        damage 2
    }
}
```

---

### `CatNap`
**Name:** Cat Nap  
**Description:** Remove all of your debuffs, then fall asleep.  
**Source:** `colorless_abilities.gon`  

```
CatNap {
    template self_buff
    
    meta {
        name "ABILITY_CATNAP_NAME"
        desc "ABILITY_CATNAP_DESC"
        class Colorless
    }

    graphics {

    }

    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        effects {
            Cleanse 0 //0 = no divine shield per removed buff
            Sleep 1
        }
    }
}
```

---

### `CatNap2`
**Description:** Remove all of your debuffs, gain All Stats Up, then fall asleep.  
**Source:** `colorless_abilities.gon`  

```
CatNap2 {
    variant_of CatNap

    meta {
        desc "ABILITY_CATNAP2_DESC"
    }

    damage_instance {
        effects {
            AllStatsUp 1
        }
    }
}
```

---

### `PissYourself`
**Name:** Number One  
**Description:** Spawn "water" tiles in an area around yourself.  
**Source:** `colorless_abilities.gon`  

```
PissYourself {
    template spell

    meta {
        name "ABILITY_PISSYOURSELF_NAME"
        desc "ABILITY_PISSYOURSELF_DESC"
        class Colorless
        type_icon "misc"
    }
    
    graphics {
        animation pissYourself
        particle none
    }
    
    cost {
        mana 2
        infcantrip true
    }
    
    target {
        target_mode none
        max_aoe 1
        aoe_excludes_self false
    }
    
    damage_instance {
        heal 0
        type status_spell
        
        effects {
            ChangeTile WaterTile
        }
    }
}
```

---

### `PissYourself2`
**Description:** Spawn "water" tiles in a larger area around yourself.  
**Source:** `colorless_abilities.gon`  

```
PissYourself2 {
    variant_of PissYourself

    meta {
        desc "ABILITY_PISSYOURSELF2_DESC"
    }

    target {
        max_aoe 2
    }
}
```

---

### `FindARock`
**Name:** Find a Rock  
**Description:** Dig up a small rock.  
**Source:** `colorless_abilities.gon`  

```
FindARock {
    template spawn

    meta {
        name "ABILITY_FINDAROCK_NAME"
        desc "ABILITY_FINDAROCK_DESC"
        class Colorless
        type_icon "misc"
    }

    graphics {
        animation dig
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_range 1
    }
    
    spawn {
        object SmallRock
        lob false
    }
}
```

---

### `FindARock2`
**Description:** Dig up a small rock.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
FindARock2 {
    variant_of FindARock

    meta {
        desc "ABILITY_FINDAROCK2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `Gassy_AssBlast`
**Name:** Ass Blast  
**Description:** Knock back all adjacent units.  
**Source:** `colorless_abilities.gon`  

```
Gassy_AssBlast { //util ability used for Gassy passive
    template melee_attack
    
    meta {
        name "ABILITY_GASSYASSBLAST_NAME"
        desc "ABILITY_GASSYASSBLAST_DESC"
        class Colorless
    }

    graphics {
        animation poopfart
    }
    
    cost {
        mana 4
        infcantrip true
    }
    
    target {
        aoe_mode standard
        max_aoe 1
        aoe_excludes_self true
        knockback_mode character_to_tile
    }
    
    damage_instance {
        type spell
        damage 0
        knockback 1
        incidentally_collects_pickups false
    }
}
```

---

### `Gassy_AssBlast2`
**Description:** Knock back all adjacent units 3 tiles and inflict Poison 1.  
**Source:** `colorless_abilities.gon`  

```
Gassy_AssBlast2 {
    variant_of Gassy_AssBlast

    meta {
        desc "ABILITY_GASSYASSBLAST2_DESC"
    }

    damage_instance {
        type spell
        damage 0
        knockback 3
        incidentally_collects_pickups false

        effects {
            Poison 1
        }
    }
}
```

---

### `BurgeoningBlast`
**Name:** Burgeoning Blast  
**Description:** A spell that deals {v0} damage. Increase this spell's damage by 2 at the end of each turn.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BurgeoningBlast {
    template spell

    meta {
        name "ABILITY_BURGEONINGBLAST_NAME"
        desc "ABILITY_BURGEONINGBLAST_DESC"
        class Colorless
        tooltip_values ["max((X-1)*2, 0)"]
    }

    graphics {
        particle BigMagicMissileBlast
		animation createmagic
    }
    
    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }
    
    target {
        max_aoe 0
        max_range 3
        X_is turn_count
    }
    
    damage_instance {
        raw_damage "max((X-1)*2, 0)"
    }
}
```

---

### `BurgeoningBlast2`
**Description:** A spell that deals {v0} damage. Increase this spell's damage by 3 at the end of each turn.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BurgeoningBlast2 {
    variant_of BurgeoningBlast

    meta {
        desc "ABILITY_BURGEONINGBLAST2_DESC"
        tooltip_values ["max(X*3, 0)"]
    }

    damage_instance {
        damage "max(X*3, 0)"
    }
}
```

---

### `BurgeoningBarrier`
**Name:** Burgeoning Barrier  
**Description:** Gain {v0} [img:shield]. Increase this spell's [img:shield] by 2 at the end of each turn.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BurgeoningBarrier {
    template self_buff

    meta {
        name "ABILITY_BURGEONINGBARRIER_NAME"
        desc "ABILITY_BURGEONINGBARRIER_DESC"
        class Colorless
        tooltip_values ["max((X-1)*2, 0)"]
    }

    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }
    
    target {
        X_is turn_count
    }
    
    damage_instance {
        effects {
            Shield "max((X-1)*2, 0)"
        }
    }
}
```

---

### `BurgeoningBarrier2`
**Description:** Gain {v0} [img:shield]. Increase this spell's [img:shield] by 3 at the end of each turn.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BurgeoningBarrier2 {
    variant_of BurgeoningBarrier

    meta {
        desc "ABILITY_BURGEONINGBARRIER2_DESC"
        tooltip_values ["max(X*3, 0)"]
    }

    damage_instance {
        effects {
            Shield "max(X*3, 0)"
        }
    }
}
```

---

### `BurgeoningBattery`
**Name:** Burgeoning Battery  
**Description:** Gain {v0} mana. Increase this spell's mana gain by 2 at the end of each turn.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BurgeoningBattery {
    template self_buff

    meta {
        name "ABILITY_BURGEONINGBATTERY_NAME"
        desc "ABILITY_BURGEONINGBATTERY_DESC"
        class Colorless
        tooltip_values ["max((X-1)*2, 0)"]
    }

    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }
    
    target {
        X_is turn_count
    }
    
    damage_instance {
        effects {
            ManaGain "max((X-1)*2, 0)"
        }
    }
}
```

---

### `BurgeoningBattery2`
**Description:** Gain {v0} mana. Increase this spell's mana gain by 3 at the end of each turn.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BurgeoningBattery2 {
    variant_of BurgeoningBattery

    meta {
        desc "ABILITY_BURGEONINGBATTERY2_DESC"
        tooltip_values ["max(X*3, 0)"]
    }

    damage_instance {
        effects {
            ManaGain "max(X*3, 0)"
        }
    }
}
```

---

### `HoseOff`
**Name:** Hose Off  
**Description:** Spray a unit with water, cleansing its debuffs and making a puddle.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
HoseOff {
    template spell
    
    meta {
        name "ABILITY_HOSEOFF_NAME"
        desc "ABILITY_HOSEOFF_DESC"
        class Colorless
    }

    graphics {
        particle Wave
		animation pointout
    }
    
    cost {
        infcantrip true
        mana 5
        once_per_fight true
    }

    target {
        min_range 0
        max_range 20
        max_aoe 0
        knockback_mode none
    }
    
    damage_instance {
        effects {
            Cleanse 0
            ChangeTile WaterTile
        }

        elements [
            Water
        ]
    }
}
```

---

### `HoseOff2`
**Description:** Spray a unit with water, cleansing its debuffs and making a puddle.
\[s:.7\](This spell costs 0 mana. Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
HoseOff2 {
    variant_of HoseOff

    meta {
        desc "ABILITY_HOSEOFF2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `Taint`
**Name:** Proliferate  
**Description:** Double a unit's Poison, Bleed, and Burn.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Taint {
    template targeted_status
    
    meta {
        name "ABILITY_PROLIFERATE_NAME"
        desc "ABILITY_PROLIFERATE_DESC"
        class Colorless
    }
	
    graphics {
        particle PoisonPoof
		animation pointout
    }

    cost {
        infcantrip true
        mana 8
        once_per_fight true
    }

    target {
        min_range 1
        max_range 1
    }
    
    damage_instance {
        effects {
            DoubleStatus Poison
            DoubleStatus Bleed
            DoubleStatus Burn
        }
    }
}
```

---

### `Taint2`
**Description:** Double a unit's Poison, Bleed, and Burn.
\[s:.7\](This spell costs 0 mana. Castable once per battle.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Taint2 {
    variant_of Taint

    meta {
        desc "ABILITY_PROLIFERATE2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `PokeWound`
**Name:** Sudden Affliction  
**Description:** Trigger the Poison, Bleed, and Burn effects on a unit.  
**Source:** `colorless_abilities.gon`  

```
PokeWound {
    template targeted_status
	
    graphics {
        animation pointout
    }
    
    meta {
        name "ABILITY_SUDDENAFFLICTION_NAME"
        desc "ABILITY_SUDDENAFFLICTION_DESC"
        class Colorless
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 1
    }
    
    damage_instance {
        makes_contact true
        effects {
            TriggerDOTStatuses 0
        }
    }
}
```

---

### `PokeWound2`
**Description:** Trigger the Poison, Bleed, and Burn effects on a unit. If that unit isn't Poisoned, Bleeding, or Burning, they gain 1 of each.  
**Source:** `colorless_abilities.gon`  

```
PokeWound2 {
    variant_of PokeWound

    meta {
        desc "ABILITY_SUDDENAFFLICTION2_DESC"
    }

    damage_instance {
        effects {
            TriggerDOTStatuses 1
        }
    }
}
```

---

### `WasteTime`
**Name:** Waste Time  
**Description:** Do nothing.  
**Source:** `colorless_abilities.gon`  

```
WasteTime {
    template self_buff
    
    meta {
        name "ABILITY_WASTETIME_NAME"
        desc "ABILITY_WASTETIME_DESC"
        class Colorless
    }

    graphics {
        animation thinking
    }

    cost {
        infcantrip true
        mana 1
    }

    damage_instance {

    }
}
```

---

### `WasteTime2`
**Description:** Gain 1 Charge.  
**Source:** `colorless_abilities.gon`  

```
WasteTime2 {
    variant_of WasteTime
    
    meta {
        desc "ABILITY_WASTETIME2_DESC"
    }

    damage_instance {
        effects {
            Charge 1
        }
    }
}
```

---

### `Desecrate`
**Name:** Desecrate  
**Description:** Destroy a body.  
**Source:** `colorless_abilities.gon`  

```
Desecrate {
    template targeted_status
    
    meta {
        name "ABILITY_DESECRATE_NAME"
        desc "ABILITY_DESECRATE_DESC"
        class Colorless
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 0
    }

    target {
        max_range 20

        restrictions must_have_destructible_corpse
    }
    
    damage_instance {
        damage 0
        cant_miss true

        effects {
            VaporizeCorpse 1
        }
    }
}
```

---

### `Desecrate2`
**Description:** Destroy a body and gain 2 mana.  
**Source:** `colorless_abilities.gon`  

```
Desecrate2 {
    variant_of Desecrate

    meta {
        desc "ABILITY_DESECRATE2_DESC"
    }

    damage_instance {
        effects {
            ApplyToSource {
                ManaGain 2
            }
        }
    }
}
```

---

### `Contort`
**Name:** Invert  
**Description:** Swap your highest and lowest stats.
\[s:.7\](Ties are chosen at random)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Contort {
    template self_buff
    
    meta {
        name "ABILITY_INVERT_NAME"
        desc "ABILITY_INVERT_DESC"
        class Colorless
    }

    cost {
        infcantrip true
        mana 2
    }

    damage_instance {
        effects {
            SwapHighestAndLowestStat 1
        }
    }
}
```

---

### `Contort2`
**Description:** Swap a unit's highest and lowest stats.
\[s:.7\](Ties are chosen at random)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Contort2 {
    variant_of Contort
    
    meta {
        desc "ABILITY_INVERT2_DESC"
    }

    target {
        target_mode tile
        min_range 0
        max_range 20
    }
}
```

---

### `RussianRoulette`
**Name:** Russian Shorthair Roulette  
**Description:** There is a 1 in 6 chance this will kill you. If it doesn't, gain +1 to a random stat and 1-2 coins.  
**Source:** `colorless_abilities.gon`  

```
RussianRoulette {
    template self_buff
    
    meta {
        name "ABILITY_RUSSIANSHORTHAIRROULETTE_NAME"
        desc "ABILITY_RUSSIANSHORTHAIRROULETTE_DESC"
        class Colorless
    }

    cost {
        infcantrip true
        mana 2
    }

    damage_instance {
        effects {
            Conditional_BadRoll {
                odds .16666666

                DieViolently 1
            } Else {
                RandomStatUp 1
                GainCoinsRange {
                    min 1 
                    max 2
                }
            }
        }
    }
}
```

---

### `RussianRoulette2`
**Description:** There is a 1 in 6 chance this will kill you. If it doesn't, gain +2 to a random stat and 2-4 coins.  
**Source:** `colorless_abilities.gon`  

```
RussianRoulette2 {
    variant_of RussianRoulette
    
    meta {
        desc "ABILITY_RUSSIANSHORTHAIRROULETTE2_DESC"
    }

    damage_instance {
        effects {
            Conditional_BadRoll {
                odds .16666666

                Instakill 25
            } Else {
                RandomStatUp 2
                GainCoinsRange {
                    min 2
                    max 4
                }
            }
        }
    }
}
```

---

### `Step`
**Name:** Step  
**Description:** Move one tile.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Step {
    template move
    
    meta {
        name "ABILITY_STEP_NAME"
        desc "ABILITY_STEP_DESC"
        animate_name true
        class Colorless
    }

    cost {
        cantrip true
        mana 0
    }

    target {
        max_range 1
    }
}
```

---

### `Step2`
**Description:** Move two tiles.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Step2 {
    variant_of Step
    
    meta {
        desc "ABILITY_STEP2_DESC"
    }

    target {
        max_range 2
    }
}
```

---

### `Interchange`
**Name:** Interchange  
**Description:** Exchange your movement action for an additional basic attack, and vice versa.  
**Source:** `colorless_abilities.gon`  

```
Interchange {
    template self_buff
    
    meta {
        name "ABILITY_INTERCHANGE_NAME"
        desc "ABILITY_INTERCHANGE_DESC"
        animate_name true
        class Colorless
    }
	
	graphics {
		animation runincircles
    }

    cost {
        infcantrip true
        mana 3
    }

    bonus_passives {
        InterchangeDisabler 1
    }

    damage_instance {
        effects {
            InterchangeMoveActPoints 1
        }
    }
}
```

---

### `Interchange2`
**Description:** Exchange your movement action for an additional basic attack, and vice versa.
\[s:.7\](This spell costs 0 mana the first time you cast it each turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Interchange2 {
    variant_of Interchange

    meta {
        desc "ABILITY_INTERCHANGE2_DESC"
    }
    cost {
        mana 3
    }
    bonus_passives {
        FreeFirstCast 1
    }
}
```

---

### `LookAtMe`
**Name:** Look at me!  
**Description:** Each unit turns to face you.  
**Source:** `colorless_abilities.gon`  

```
LookAtMe {
    template spell
    
    meta {
        name "ABILITY_LOOKATME_NAME"
        desc "ABILITY_LOOKATME_DESC"
        class Colorless
    }

    graphics {
        animation tauntwiggle
		particle none
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        knockback_mode tile_to_character
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

### `LookAtMe2`
**Description:** Each unit turns to face you. 20% chance to Confuse enemies.  
**Source:** `colorless_abilities.gon`  

```
LookAtMe2 {
    variant_of LookAtMe

    meta {
        desc "ABILITY_LOOKATME2_DESC"
    }

    damage_instance {
        effects {
            FaceAway 1
            Conditional_Enemy {
                Confusion [1 .2]
            }
        }
    }
}
```

---

### `Rouse`
**Name:** Rouse  
**Description:** Give an adjacent unit +2 Charge.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Rouse {
    template targeted_status
    
    meta {
        name "ABILITY_ROUSE_NAME"
        desc "ABILITY_ROUSE_DESC"
        class Colorless
    }

    cost {
        cantrip true
        mana 0
    }

    target {
        min_range 1
        max_range 1
    }

    damage_instance {
        effects {
            Charge 2
        }
    }
}
```

---

### `Rouse2`
**Description:** Give any unit +2 Charge.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Rouse2 {
    variant_of Rouse

    meta {
        desc "ABILITY_ROUSE2_DESC"
    }

    target {
        max_range 4
    }
}
```

---

### `Shift`
**Name:** Shift  
**Description:** Swap positions with an adjacent unit.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Shift {
    template swap
    
    meta {
        name "ABILITY_SHIFT_NAME"
        desc "ABILITY_SHIFT_DESC"
        animate_name true
        class Colorless
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
        mode yeet
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        max_range 1
    }
}
```

---

### `Shift2`
**Description:** Swap positions with any unit.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Shift2 {
    variant_of Shift

    meta {
        desc "ABILITY_SHIFT2_DESC"
    }

    target {
        max_range 3
    }
}
```

---

### `Donate`
**Name:** Make a Wish  
**Description:** Spend a coin to spawn a random pickup on a random tile.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Donate {
    template spawn

    meta {
        name "ABILITY_MAKEAWISH_NAME"
        desc "ABILITY_MAKEAWISH_DESC"
        class Colorless
        type_icon "misc"
    }
    
    graphics {
        lob true
    }
    sounds {
        ontrigger Spawn_Donate
    }

    
    cost {
        mana 0
        coins 1
        cantrip true
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        min_targets 1
        max_targets 1
        aoe_restrictions [must_be_empty]
    }

    spawn {
        object RandomPickup
        layer pickups
    }
}
```

---

### `Donate2`
**Description:** Spend a coin to spawn a random pickup on an empty tile of your choice.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Donate2 {
    variant_of Donate

    meta {
        desc "ABILITY_MAKEAWISH2_DESC"
    }

    target {
        target_mode tile
        max_aoe 0
        max_range 20
        restrictions aoe_must_exist
        aoe_restrictions [must_be_empty]
    }
}
```

---

### `Magnet`
**Name:** Magnet  
**Description:** Pull a pickup one tile toward you.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Magnet {
    template spell

    meta {
        name "ABILITY_MAGNET_NAME"
        desc "ABILITY_MAGNET_DESC"
        animate_name false
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
        restrictions must_have_tag
        target_requires_tag pickup
    }
    
    damage_instance {
        damage 0
        knockback 1
    }
}
```

---

### `Magnet2`
**Description:** Pull a pickup all the way toward you.
\[s:.7\](Castable once per turn)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Magnet2 {
    variant_of Magnet

    meta {
        desc "ABILITY_MAGNET2_DESC"
    }

    target {
        knockback_mode pull_to_character_plus1
    }

    damage_instance {
        damage 0
        knockback 1
    }
}
```

---

### `ScuffItOff`
**Name:** Shrug It Off  
**Description:** Heal yourself HP equal to half your [img:str], rounded up.  
**Source:** `colorless_abilities.gon`  

```
ScuffItOff {
    template self_buff
    
    meta {
        name "ABILITY_SHRUGITOFF_NAME"
        desc "ABILITY_SHRUGITOFF_DESC"
        class Colorless
        icon_shell_frame attack
    }

    graphics {
		animation flex
    }

    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        raw_heal "(str+1)/2"

    }
}
```

---

### `ScuffItOff2`
**Description:** Heal yourself HP equal to half your [img:str], rounded up.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
ScuffItOff2 {
    variant_of ScuffItOff

    meta {
        desc "ABILITY_SHRUGITOFF2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `BarfBall`
**Name:** Barf Ball  
**Description:** A ranged attack that deals damage equal to half your [img:con], rounded up.  
**Source:** `colorless_abilities.gon`  

```
BarfBall {
    template lobbed_attack

    meta {
        name "ABILITY_BARFBALL_NAME"
        desc "ABILITY_BARFBALL_DESC"
        class Colorless
        icon_shell_frame attack
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 5
    }
    
    damage_instance {
        raw_damage "(con+1)/2"
    }
}
```

---

### `BarfBall2`
**Description:** A ranged attack that deals damage equal to half your [img:con], rounded up.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BarfBall2 {
    variant_of BarfBall

    meta {
        desc "ABILITY_BARFBALL2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `DexterousHit`
**Name:** Dexterous Hit  
**Description:** A melee attack that deals damage equal to half your [img:dex], rounded up.  
**Source:** `colorless_abilities.gon`  

```
DexterousHit {
    template melee_attack
    
    meta {
        name "ABILITY_DEXTEROUSHIT_NAME"
        desc "ABILITY_DEXTEROUSHIT_DESC"
        class Colorless
    }

    graphics {
		animation karateKid
    }

    cost {
        infcantrip true
        mana 6
    }

    damage_instance {
        damage "(dex+1)/2"
    }
}
```

---

### `DexterousHit2`
**Description:** A melee attack that deals damage equal to half your [img:dex], rounded up.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
DexterousHit2 {
    variant_of DexterousHit

    meta {
        desc "ABILITY_DEXTEROUSHIT2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `Till`
**Name:** Randomize  
**Description:** Spawn a random tile anywhere.  
**Source:** `colorless_abilities.gon`  

```
Till {
    template targeted_status
    
    meta {
        name "ABILITY_RANDOMIZE_NAME"
        desc "ABILITY_RANDOMIZE_DESC"
        class Colorless
    }

    graphics {
		animation pointout
    }
    
    cost {
        infcantrip true
        mana 2
    }

    target {
        max_range 5
    }
    
    damage_instance {
        effects {
            ChangeTile RandomDifferentTile
        }
    }
}
```

---

### `Till2`
**Description:** Tiles in an area become random tiles.  
**Source:** `colorless_abilities.gon`  

```
Till2 {
    variant_of Till

    meta {
        desc "ABILITY_RANDOMIZE2_DESC"
    }

    target {
        max_range 6
        max_aoe 2
    }
}
```

---

### `PathOfTheMage`
**Name:** Path of the Mage  
**Description:** Transform this spell into a random Mage spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheMage {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEMAGE_NAME"
        desc "ABILITY_PATHOFTHEMAGE_DESC"
        class Colorless
    }

    tags [noncopyable]
    
    graphics {
		animation floatingmagic
    }

    cost {
        cantrip true
        mana 12
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool Mage
        }
    }
}
```

---

### `PathOfTheMage2`
**Description:** Transform this spell into a random upgraded Mage spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheMage2 {
    variant_of PathOfTheMage
    
    meta {
        desc "ABILITY_PATHOFTHEMAGE2_DESC"
    }

    cost {
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Mage
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheHunter`
**Name:** Path of the Hunter  
**Description:** A lobbed attack that deals 1 damage. If this kills an enemy, this spell becomes a random Hunter spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheHunter {
    template lobbed_attack
    
    meta {
        name "ABILITY_PATHOFTHEHUNTER_NAME"
        desc "ABILITY_PATHOFTHEHUNTER_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
		animation throwArrow
		projectile ArrowProjectile
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 1

        effects {
            Conditional_Enemy {
                ApplyToSourceOnKill {
                    EvolveAbilityFromPool Hunter
                }
            }
        }
    }
}
```

---

### `PathOfTheHunter2`
**Name:** Path of the Hunter  
**Description:** Transform this spell into a random upgraded Hunter spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheHunter2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEHUNTER_NAME"
        desc "ABILITY_PATHOFTHEHUNTER2_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Hunter
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheThief`
**Name:** Path of the Thief  
**Description:** A straight shot attack that deals 1 damage. If this makes a critical hit, this spell becomes a random Thief spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheThief {
    template straightshot_attack
    
    meta {
        name "ABILITY_PATHOFTHETHIEF_NAME"
        desc "ABILITY_PATHOFTHETHIEF_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
        animation throwobject
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_aoe 3+bonus_range
    }

    damage_instance {
        damage 1

        effects {
            ApplyStatusIfCrit {
                ApplyToSource {
                    EvolveAbilityFromPool Thief
                }
            }
        }
    }
}
```

---

### `PathOfTheThief2`
**Name:** Path of the Thief  
**Description:** Transform this spell into a random upgraded Thief spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheThief2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHETHIEF_NAME"
        desc "ABILITY_PATHOFTHETHIEF2_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Thief
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheFighter`
**Name:** Path of the Fighter  
**Description:** Your [img:int] becomes 0 until the end of the battle, then this spell becomes a random Fighter spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheFighter {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEFIGHTER_NAME"
        desc "ABILITY_PATHOFTHEFIGHTER_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
		animation angry
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool Fighter
            IntelligenceUp -int
        }
    }
}
```

---

### `PathOfTheFighter2`
**Name:** Path of the Fighter  
**Description:** Transform this spell into a random upgraded Fighter spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheFighter2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEFIGHTER_NAME"
        desc "ABILITY_PATHOFTHEFIGHTER2_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
        animation angry
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Fighter
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheTank`
**Name:** Path of the Tank  
**Description:** Transform this spell into a random Tank spell permanently. Castable only if you have 5 or less health.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheTank {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHETANK_NAME"
        desc "ABILITY_PATHOFTHETANK_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
    }

    cost {
        cantrip true
        mana 0
        cant_cast X-5
    }

    target {
        X_is current_health
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool Tank
        }
    }
}
```

---

### `PathOfTheTank2`
**Description:** Transform this spell into a random upgraded Tank spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheTank2 {
    variant_of PathOfTheTank
    
    meta {
        desc "ABILITY_PATHOFTHETANK2_DESC"
    }

    cost {
        cant_cast false
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Tank
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheCleric`
**Name:** Path of the Cleric  
**Description:** Give an enemy All Stats Up and fully heal it, then this spell becomes a random Cleric spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheCleric {
    template targeted_status
    
    meta {
        name "ABILITY_PATHOFTHECLERIC_NAME"
        desc "ABILITY_PATHOFTHECLERIC_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
        animation pray
    }

    cost {
        cantrip true
        mana 0
    }

    target {
        max_range 1
        restrictions must_have_enemy
    }

    damage_instance {
        effects {
            Revive 100%
            AllStatsUp 1
            FullHeal 1
            ApplyToSource {
                EvolveAbilityFromPool Medic
            }
        }
    }
}
```

---

### `PathOfTheCleric2`
**Name:** Path of the Cleric  
**Description:** Transform this spell into a random upgraded Cleric spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheCleric2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHECLERIC_NAME"
        desc "ABILITY_PATHOFTHECLERIC2_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Medic
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheButcher`
**Name:** Path of the Butcher  
**Description:** Collect an adjacent food pickup, then this spell becomes a random Butcher spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheButcher {
    template targeted_status
    
    meta {
        name "ABILITY_PATHOFTHEBUTCHER_NAME"
        desc "ABILITY_PATHOFTHEBUTCHER_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
        animation attack
    }

    cost {
        cantrip true
        mana 1
    }

    target {
        max_range 1

        restrictions must_have_tag
        target_requires_tag food
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            CollectsPickups 1
            CanApplyToInanimate {
                ApplyToSource {
                    EvolveAbilityFromPool Butcher
                }
            }
        }
    }
}
```

---

### `PathOfTheButcher2`
**Name:** Path of the Butcher  
**Description:** Transform this spell into a random upgraded Butcher spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheButcher2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEBUTCHER_NAME"
        desc "ABILITY_PATHOFTHEBUTCHER2_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Butcher
                upgraded true
            }
        }
    }
}
```

---

### `PathOfThePsychic`
**Name:** Path of the Psychic  
**Description:** This spell becomes a random Psychic spell permanently. Castable only if you have full mana.  
**Source:** `colorless_abilities.gon`  

```
PathOfThePsychic {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEPSYCHIC_NAME"
        desc "ABILITY_PATHOFTHEPSYCHIC_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
		animation psyAttack1
    }

    cost {
        cantrip true
        mana 0
        cant_cast 1-X
    }

    target {
        X_is is_at_max_mana
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool Psychic
        }
    }
}
```

---

### `PathOfThePsychic2`
**Description:** Transform this spell into a random upgraded Psychic spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfThePsychic2 {
    variant_of PathOfThePsychic
    
    meta {
        desc "ABILITY_PATHOFTHEPSYCHIC2_DESC"
    }

    cost {
        cant_cast false
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Psychic
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheTinkerer`
**Name:** Path of the Tinkerer  
**Description:** Destroy your weapon, then this spell becomes a random Tinkerer spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheTinkerer {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHETINKERER_NAME"
        desc "ABILITY_PATHOFTHETINKERER_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {

    }
    
    cost {
        cantrip true
        mana 0
        requires_destructible_weapon true
    }
    
    damage_instance {
        effects {
            DestroyWeapon 1
            EvolveAbilityFromPool Tinkerer
        }
    }
}
```

---

### `PathOfTheTinkerer2`
**Name:** Path of the Tinkerer  
**Description:** Transform this spell into a random upgraded Tinkerer spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheTinkerer2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHETINKERER_NAME"
        desc "ABILITY_PATHOFTHETINKERER2_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Tinkerer
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheMonk`
**Name:** Path of the Monk  
**Description:** Gain All Stats Down, then this spell becomes a random Monk spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheMonk {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEMONK_NAME"
        desc "ABILITY_PATHOFTHEMONK_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
		animation meditate
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool Monk
            AllStatsUp -1
        }
    }
}
```

---

### `PathOfTheMonk2`
**Name:** Path of the Monk  
**Description:** This spell becomes a random upgraded Monk spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheMonk2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEMONK_NAME"
        desc "ABILITY_PATHOFTHEMONK2_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Monk
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheDruid`
**Name:** Path of the Druid  
**Description:** Plant flowers on the tile you're standing on, then this spell becomes a random Druid spell permanently. Castable only if you're standing on a grass tile.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheDruid {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEDRUID_NAME"
        desc "ABILITY_PATHOFTHEDRUID_DESC"
        class Colorless
    }

    tags [noncopyable, musical]

    graphics {
        animation sing1
    }

    cost {
        cantrip true
        mana 2
    }

    target {
        restrictions [must_have_element]
        target_requires_element [grass]
    }

    damage_instance {
        layer all
        effects {
            EvolveAbilityFromPool Druid
            FlowersOnHit 1
        }
    }
}
```

---

### `PathOfTheDruid2`
**Name:** Path of the Druid  
**Description:** Transform this spell into a random upgraded Druid spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheDruid2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEDRUID_NAME"
        desc "ABILITY_PATHOFTHEDRUID2_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Druid
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheNecromancer`
**Name:** Path of the Necromancer  
**Description:** Destroy a corpse, then this spell becomes a random Necromancer spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheNecromancer {
    template melee_attack
    
    meta {
        name "ABILITY_PATHOFTHENECROMANCER_NAME"
        desc "ABILITY_PATHOFTHENECROMANCER_DESC"
        class Colorless
    }

    tags [noncopyable]

    cost {
        cantrip true
        mana 0
    }

    target {
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 0
        incidentally_collects_pickups false

        effects {
            VaporizeCorpse 1
            ApplyToSource {
                EvolveAbilityFromPool Necromancer
            }
        }
    }
}
```

---

### `PathOfTheNecromancer2`
**Name:** Path of the Necromancer  
**Description:** Transform this spell into a random Necromancer spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheNecromancer2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHENECROMANCER_NAME"
        desc "ABILITY_PATHOFTHENECROMANCER2_DESC"
        class Colorless
    }

    tags [noncopyable]

    graphics {
    }

    cost {
        cantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool Necromancer
                upgraded true
            }
        }
    }
}
```

---

### `Itch`
**Name:** Itch  
**Description:** Deal 1 damage to yourself. 50% chance to spawn a friendly flea.  
**Source:** `colorless_abilities.gon`  

```
Itch {
    template self_buff
    
    meta {
        name "ABILITY_ITCH_NAME"
        desc "ABILITY_ITCH_DESC"
        class Colorless
    }

    graphics {
        animation scratchear
    }

    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        damage 1
        type melee
        cant_miss true
        crit_chance -999999

        effects {
            ObjectOnHitCharacter {
                object CharmedFlea
                chance .5
            }
        }
    }
}
```

---

### `Itch2`
**Description:** Deal 1 damage to yourself. Spawn a friendly flea.  
**Source:** `colorless_abilities.gon`  

```
Itch2 {
    variant_of Itch
    
    meta {
        desc "ABILITY_ITCH2_DESC"
    }

    damage_instance {
        effects {
            ObjectOnHitCharacter {
                object CharmedFlea
                chance 1
            }
        }
    }
}
```

---

### `Meow`
**Name:** Meow  
**Description:** Your closest ally moves toward you.  
**Source:** `colorless_abilities.gon`  

```
Meow {
    template self_buff
    
    meta {
        name "ABILITY_MEOW_NAME"
        desc "ABILITY_MEOW_DESC"
        class Colorless
    }

	tags [musical]

    graphics {
        animation howl
    }

    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        effects {
            ApplyToRandomClosestAlly {
                ForceMoveTowards 1
            }
        }
    }
}
```

---

### `Meow2`
**Name:** Meow  
**Description:** A target ally moves toward you.  
**Source:** `colorless_abilities.gon`  

```
Meow2 {
    template targeted_status
    
    meta {
        name "ABILITY_MEOW_NAME"
        desc "ABILITY_MEOW2_DESC"
        class Colorless
    }

    tags [musical]

    graphics {
        animation howl
    }

    target {
        max_range 20
        restrictions must_have_ally
    }

    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        effects {
            ForceMoveTowards 1
        }
    }
}
```

---

### `Swat`
**Name:** Swat  
**Description:** Knockback a unit 3 tiles.  
**Source:** `colorless_abilities.gon`  

```
Swat {
    template melee_attack
    
    meta {
        name "ABILITY_SWAT_NAME"
        desc "ABILITY_SWAT_DESC"
        class Colorless
    }

    graphics {
        animation knockswatatk
    }

    cost {
        infcantrip true
        mana 3
    }

    damage_instance {
        damage 0
        knockback 3
    }
}
```

---

### `Swat2`
**Description:** Knockback a unit 10 tiles.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
Swat2 {
    variant_of Swat

    meta {
        desc "ABILITY_SWAT2_DESC"
    }

    cost {
        mana 2
    }

    damage_instance {
        knockback 10
    }
}
```

---

### `LickHeal`
**Name:** Lick  
**Description:** Heal an adjacent unit by 2 HP.  
**Source:** `colorless_abilities.gon`  

```
LickHeal {
    template melee_attack

    meta {
        name "ABILITY_LICK_NAME"
        desc "ABILITY_LICK_DESC"
        class Colorless
        type_icon "heal"
    }
    
    graphics {
        animation lickAttack
    }
    
    cost {
        mana 4
        infcantrip true
    }
    
    damage_instance {
        heal 2

        elements [
            Water
            Holy
        ]
    }
}
```

---

### `LickHeal2`
**Description:** Heal an adjacent unit by 2 HP. Healed enemies gain Confusion 3.  
**Source:** `colorless_abilities.gon`  

```
LickHeal2 {
    variant_of LickHeal

    meta {
        desc "ABILITY_LICK2_DESC"
    }

    damage_instance {
        effects {
            Conditional_Enemy {
                Confusion 3
            }
        }
    }
}
```

---

### `Purr`
**Name:** Purr  
**Description:** Remove 1 stack of a random debuff from yourself and all adjacent units.  
**Source:** `colorless_abilities.gon`  

```
Purr {
    template self_buff
    
    meta {
        name "ABILITY_PURR_NAME"
        desc "ABILITY_PURR_DESC"
        class Colorless
    }

    target {
        max_aoe 1
    }

    graphics {
        animation knead
    }

    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            PartialCleanse 1
        }
    }
}
```

---

### `Purr2`
**Description:** Remove 1 stack of a random debuff from and heal 1 HP to yourself and all adjacent units.  
**Source:** `colorless_abilities.gon`  

```
Purr2 {
    variant_of Purr

    meta {
        desc "ABILITY_PURR2_DESC"
    }

    cost {
        mana 3
    }

    target {
        max_aoe 1
    }

    damage_instance {
        heal 1
        layer all
    }
}
```

---

### `Hiss`
**Name:** Hiss  
**Description:** Adjacent units move away from you. You have a 25% chance to inflict Fear on them.  
**Source:** `colorless_abilities.gon`  

```
Hiss {
    template spell

    meta {
        name "ABILITY_HISS_NAME"
        desc "ABILITY_HISS_DESC"
        class Colorless
    }

    graphics {
        animation hiss
        particle none
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 1
    }
    
    damage_instance {
        damage 0

        effects {
            ForceMoveAway 1
            Fear [1 .25]
        }
    }
}
```

---

### `Hiss2`
**Description:** Adjacent units move away from you. Inflict fear on them.  
**Source:** `colorless_abilities.gon`  

```
Hiss2 {
    variant_of Hiss

    meta {
        desc "ABILITY_HISS2_DESC"
    }

    damage_instance {
        effects {
            Fear 1
        }
    }
}
```

---

### `Knead`
**Name:** Knead  
**Description:** Knead another unit. Allies gain +1 Damage, enemies gain Weakness 1.  
**Source:** `colorless_abilities.gon`  

```
Knead {
    template melee_attack

    meta {
        name "ABILITY_KNEAD_NAME"
        desc "ABILITY_KNEAD_DESC"
        class Colorless
        type_icon buff
    }
    
    graphics {
        animation knead
    }
    
    cost {
        mana 5
        infcantrip true
    }
    
    damage_instance {
        damage 0

        effects {
            Conditional_Ally {
                DamageUp 1
            }
            Conditional_Enemy {
                Weakness 1
            }
        }
    }
}
```

---

### `Knead2`
**Description:** Knead another unit. Allies gain +2 Damage, enemies gain Weakness 2.  
**Source:** `colorless_abilities.gon`  

```
Knead2 {
    variant_of Knead

    meta {
        desc "ABILITY_KNEAD2_DESC"
    }

    damage_instance {
        effects {
            Conditional_Ally {
                DamageUp 2
            }
            Conditional_Enemy {
                Weakness 2
            }
        }
    }
}
```

---

### `BuyCatnip`
**Name:** Buy Catnip  
**Description:** Spend 5 coins, gain 10 mana.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BuyCatnip {
    template self_buff
    
    meta {
        name "ABILITY_BUYCATNIP_NAME"
        desc "ABILITY_BUYCATNIP_DESC"
        class Colorless
    }

    graphics {
	    animation statusReaction
	    particle none
    }
    
    cost {
        cantrip true
        mana 0
        coins 5
    }
    
    damage_instance {
        effects {
            ManaGain 10
        }
    }
}
```

---

### `BuyCatnip2`
**Description:** Spend 5 coins, gain 15 mana.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
BuyCatnip2 {
    variant_of BuyCatnip

    meta {
        desc "ABILITY_BUYCATNIP2_DESC"
    }

    damage_instance {
        effects {
            ManaGain 15
        }
    }
}
```

---

### `VetVisit`
**Name:** Vet Visit  
**Description:** Spend 5 coins, heal 10 HP.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
VetVisit {
    template self_buff
    
    meta {
        name "ABILITY_VETVISIT_NAME"
        desc "ABILITY_VETVISIT_DESC"
        class Colorless
    }

    graphics {
    }
    
    cost {
        cantrip true
        mana 0
        coins 5
    }
    
    damage_instance {
        heal 10
    }
}
```

---

### `VetVisit2`
**Description:** Spend 5 coins, heal 15 HP.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
VetVisit2 {
    variant_of VetVisit

    meta {
        desc "ABILITY_VETVISIT2_DESC"
    }

    damage_instance {
        heal 15
    }
}
```

---

### `HireHitman`
**Name:** Hire Hitman  
**Description:** Spend 7 coins, summon a bounty hunter.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
HireHitman {
    template spawn

    meta {
        name "ABILITY_HIREHITMAN_NAME"
        desc "ABILITY_HIREHITMAN_DESC"
        class Colorless
    }

    graphics {
        lob false
    }

    cost {
        cantrip true
        mana 0
        coins 7
    }
    
    target {
        max_range 1
    }
    
    spawn {
        object GunCat
        faction self
    }
}
```

---

### `HireHitman2`
**Description:** Spend 7 coins, summon a bounty hunter with All Stats Up 2.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
HireHitman2 {
    variant_of HireHitman

    meta {
        desc "ABILITY_HIREHITMAN2_DESC"
    }

    spawn {
        additional_passives {
            AllStatsUp 2
            HealthGain 8
        }
    }
}
```

---

### `SubwayRide`
**Name:** Subway Ride  
**Description:** Spend 5 coins, teleport to any tile.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
SubwayRide {
    template teleport
    
    meta {
        name "ABILITY_SUBWAYRIDE_NAME"
        desc "ABILITY_SUBWAYRIDE_DESC"
        animate_name true
        class Colorless
    }

    graphics {
        animation_out digDown
        animation_in digUp
    }

    cost {
        cantrip true
        mana 0
        coins 5
    }

    target {
        max_range 20
    }
}
```

---

### `SubwayRide2`
**Description:** Spend 2 coins, teleport to any tile.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
SubwayRide2 {
    variant_of SubwayRide

    meta {
        desc "ABILITY_SUBWAYRIDE2_DESC"
    }

    cost {
        coins 2
    }
}
```

---

### `GymMembership`
**Name:** Gym Membership  
**Description:** Spend 5 coins, gain All Stats Up.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
GymMembership {
    template self_buff
    
    meta {
        name "ABILITY_GYMMEMBERSHIP_NAME"
        desc "ABILITY_GYMMEMBERSHIP_DESC"
        class Colorless
    }

    graphics {
		particle fx_statup
    }
    
    cost {
        cantrip true
        mana 0
        coins 5
    }
    
    damage_instance {
        effects {
            AllStatsUp 1
        }
    }
}
```

---

### `GymMembership2`
**Description:** Spend 5 coins, gain All Stats Up and refresh your basic attack and movement actions.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
GymMembership2 {
    variant_of GymMembership

    meta {
        desc "ABILITY_GYMMEMBERSHIP2_DESC"
    }

    damage_instance {
        effects {
            AllStatsUp 1
            RefreshActPoints 1
            RefreshMovePoints 1
        }
    }
}
```

---

### `SuperCrateBox`
**Name:** Super Crate Box  
**Description:** Spawn a crate on an adjacent tile.  
**Source:** `colorless_abilities.gon`  

```
SuperCrateBox {
    template spawn

    meta {
        name "ABILITY_SUPERCRATEBOX_NAME"
        desc "ABILITY_SUPERCRATEBOX_DESC"
        class Colorless
    }

    graphics {
        lob true
    }

    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_range 1
    }
    
    spawn {
        object Crate
    }
}
```

---

### `SuperCrateBox2`
**Description:** Spawn a crate within range 5.  
**Source:** `colorless_abilities.gon`  

```
SuperCrateBox2 {
    variant_of SuperCrateBox

    meta {
        desc "ABILITY_SUPERCRATEBOX2_DESC"
    }

    target {
        max_range 5
    }
}
```

---

### `BBQ`
**Name:** BBQ  
**Description:** Spawn a cooked meat pickup.  
**Source:** `colorless_abilities.gon`  

```
BBQ {
    template spawn

    meta {
        name "ABILITY_BBQ_NAME"
        desc "ABILITY_BBQ_DESC"
        class Colorless
    }

    graphics {
        lob true
    }

    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_range 2
    }
    
    spawn {
        object CookedFood
    }
}
```

---

### `BBQ2`
**Description:** Spawn a big cooked meat pickup.  
**Source:** `colorless_abilities.gon`  

```
BBQ2 {
    variant_of BBQ

    meta {
        desc "ABILITY_BBQ2_DESC"
    }

    spawn {
        object CookedBiggestFood
    }
}
```

---

### `CPR`
**Name:** CPR  
**Description:** Revive an adjacent body to 1 HP.  
**Source:** `colorless_abilities.gon`  

```
CPR {
    template melee_spell
    
    meta {
        name "ABILITY_CPR_NAME"
        desc "ABILITY_CPR_DESC"
        class Colorless
        type_icon "heal"
    }

    graphics {
        affected_particle HealBig
        animation knead
    }

    target {
        aoe_restrictions must_have_corpse
        restrictions aoe_must_exist
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        heal 1
        type spell
        can_revive true
    }
}
```

---

### `CPR2`
**Description:** Revive an adjacent body to 5 HP.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
CPR2 {
    variant_of CPR

    meta {
        desc "ABILITY_CPR2_DESC"
    }

    cost {
        mana 2
    }

    damage_instance {
        heal 5
    }
}
```

---

### `Blow`
**Name:** Blow  
**Description:** Blow units in a cone back 1 tile.  
**Source:** `colorless_abilities.gon`  

```
Blow {
    template spell

    meta {
        name "ABILITY_BLOW_NAME"
        desc "ABILITY_BLOW_DESC"
        class Colorless
    }

    graphics {
        particle fx_windSpell
		animation blowFire
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 2

        aoe_considers_character_size true
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0
        knockback 1

        elements [
            Wind
        ]
    }
}
```

---

### `Blow2`
**Description:** Blow units in a larger cone back 1 tile.  
**Source:** `colorless_abilities.gon`  

```
Blow2 {
    variant_of Blow

    meta {
        desc "ABILITY_BLOW2_DESC"
    }

    target {
        max_aoe 4
    }
}
```

---

### `Toast`
**Name:** Toast  
**Description:** Inflict Burn 1 on an adjacent unit.  
**Source:** `colorless_abilities.gon`  

```
Toast {
    template spell

    meta {
        name "ABILITY_TOAST_NAME"
        desc "ABILITY_TOAST_DESC"
        class Colorless
    }

    graphics {
        particle BurnTrigger
        animation createmagic
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        max_aoe 0
        min_range 1
        max_range 1
    }
    
    damage_instance {
        damage 0

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

### `Toast2`
**Description:** Inflict Burn 1 on a unit in range 5.  
**Source:** `colorless_abilities.gon`  

```
Toast2 {
    variant_of Toast

    meta {
        desc "ABILITY_TOAST2_DESC"
    }

    target {
        max_range 5
    }
}
```

---

### `Landscape`
**Name:** Landscape  
**Description:** Turn an adjacent tile into a small grass tile.  
**Source:** `colorless_abilities.gon`  

```
Landscape {
    template targeted_status
    
    meta {
        name "ABILITY_LANDSCAPE_NAME"
        desc "ABILITY_LANDSCAPE_DESC"
        class Colorless
    }

    graphics {
		animation knead
    }
    
    cost {
        infcantrip true
        mana 1
    }

    target {
        max_range 1
    }
    
    damage_instance {
        effects {
            ChangeTile GrassTile
        }

        elements [
            Grass
        ]
    }
}
```

---

### `Landscape2`
**Description:** Turn any tile into a small grass tile.  
**Source:** `colorless_abilities.gon`  

```
Landscape2 {
    variant_of Landscape

    meta {
        desc "ABILITY_LANDSCAPE2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `Zap`
**Name:** Zap  
**Description:** Deal 1 electric damage at infinite range.  
**Source:** `colorless_abilities.gon`  

```
Zap {
    template spell

    meta {
        name "ABILITY_ZAP_NAME"
        desc "ABILITY_ZAP_DESC"
        class Colorless
    }

    graphics {
        particle Bolt
        animation castspell
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 1

        elements [
            Electric
        ]
    }
}
```

---

### `Zap2`
**Description:** Deal 1 electric damage with a 25% chance to Stun at infinite range.  
**Source:** `colorless_abilities.gon`  

```
Zap2 {
    variant_of Zap

    meta {
        desc "ABILITY_ZAP2_DESC"
    }

    damage_instance {
        effects {
            Stun [1 .25]
        }
    }
}
```

---

### `Sunburn`
**Name:** Sunburn  
**Description:** Inflicts Burn 1 and Blind 1 at infinite range.  
**Source:** `colorless_abilities.gon`  

```
Sunburn {
    template spell

    meta {
        name "ABILITY_SUNBURN_NAME"
        desc "ABILITY_SUNBURN_DESC"
        class Colorless
    }

    graphics {
        particle FireSpin
        palette 6
        animation castspell
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 0

        effects {
            Burn 1
            Blind 1
        }

        elements [
            Fire
        ]
    }
}
```

---

### `Sunburn2`
**Description:** Inflict Burn 1 and Blind 1 in an area at infinite range.  
**Source:** `colorless_abilities.gon`  

```
Sunburn2 {
    variant_of Sunburn

    meta {
        desc "ABILITY_SUNBURN2_DESC"
    }

    target {
        max_aoe 2
    }
}
```

---

### `ColdShoulder`
**Name:** Cold Shoulder  
**Description:** Deal 1 ice damage and inflict Slow 1 at infinite range.  
**Source:** `colorless_abilities.gon`  

```
ColdShoulder {
    template spell

    meta {
        name "ABILITY_COLDSHOULDER_NAME"
        desc "ABILITY_COLDSHOULDER_DESC"
        class Colorless
    }

    graphics {
        particle IcePoof
        animation castspell
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 1

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

### `ColdShoulder2`
**Description:** Deal 1 ice damage and inflict Slow 1 at infinite range.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
ColdShoulder2 {
    variant_of ColdShoulder

    meta {
        desc "ABILITY_COLDSHOULDER2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `BlowKiss`
**Name:** Blow Kiss  
**Description:** Heal another unit by 1 HP at infinite range.  
**Source:** `colorless_abilities.gon`  

```
BlowKiss {
    template spell

    meta {
        name "ABILITY_BLOWKISS_NAME"
        desc "ABILITY_BLOWKISS_DESC"
        class Colorless
    }

    graphics {
        particle fx_windSpell
        animation blowKiss
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        max_aoe 0
        min_range 1
        max_range 20
    }
    
    damage_instance {
        heal 1

        elements [
            Holy
            Wind
        ]
    }
}
```

---

### `BlowKiss2`
**Description:** Heal another unit by 2 HP at infinite range.  
**Source:** `colorless_abilities.gon`  

```
BlowKiss2 {
    variant_of BlowKiss

    meta {
        desc "ABILITY_BLOWKISS2_DESC"
    }

    damage_instance {
        heal 2
    }
}
```

---

### `ForbiddenFart`
**Name:** Forbidden Fart  
**Description:** Damage, Inflict Poison 4 and Knock Up nearby units.
There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
ForbiddenFart {
    template spell

    meta {
        name "ABILITY_FORRBIDDENFART_NAME"
        desc "ABILITY_FORRBIDDENFART_DESC"
        class Colorless
    }

    graphics {
        particle none
        animation fartoom
    }
    
    cost {
        cantrip true
        mana 0
    }

    
    target {
        target_mode none
        aoe_mode circle
        max_aoe 2
        aoe_excludes_self true
    }

    self_damage {
        effects {
            Conditional_GoodRoll {
                odds 90%
                GainDisorderFromPool_PostCast forbidden_spell_consequences
            } Else {
                GainDisorderFromPool_PostCast forbidden_spell_consequences_crippling
            }
        }
    }

    damage_instance {
        damage 4

        effects {
            Poison 4
            KnockUpAndAway {
                distance 3
            }
        }
        
        elements [
            Poison
        ]
    }
}
```

---

### `ForbiddenFart2`
**Description:** Damage, Inflict Poison 6 and Knock Up nearby units in a larger area.
There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `colorless_abilities.gon`  

```
ForbiddenFart2 {
    variant_of ForbiddenFart

    meta {
        desc "ABILITY_FORRBIDDENFART2_DESC"
    }

    target {
        max_aoe 3
    }

    damage_instance {
        damage 6

        effects {
            Poison 6
        }
    }
}
```

---

### `WetHairball`
**Name:** Wet Hairball  
**Description:** Shoot a wet hairball that deals damage in an area.  
**Source:** `colorless_abilities.gon`  

```
WetHairball {
    template spell

    meta {
        name "ABILITY_WETHAIRBALL_NAME"
        desc "ABILITY_WETHAIRBALL_DESC"
    }

    cost {
        mana 7
        infcantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range

        max_aoe 1

        can_multihit false
    }

    graphics {
        use_projectile true
        single_projectile true
        particle Wave
        delay 15
		animation pukeatk
    }
    
    damage_instance {
        damage 2
        
        elements [
            Water
        ]
    }
}
```

---

### `WetHairball2`
**Description:** Shoot a wet hairball that deals more damage in an area.  
**Source:** `colorless_abilities.gon`  

```
WetHairball2 {
    variant_of WetHairball

    meta {
        desc "ABILITY_WETHAIRBALL2_DESC"
    }


    target {
        max_range 7+bonus_range
    }

    damage_instance {
        damage 5
    }
}
```

---

### `PathOfTheVoid`
**Name:** Path Of The Void  
**Description:** Conjure a random Collarless spell into your bonus spell slot.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheVoid {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEVOID_NAME"
        desc "ABILITY_PATHOFTHEVOID_DESC"
        class Colorless
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 1
    }
    
    damage_instance {
        effects {
            ConjureBonusAbility Colorless
        }
    }
}
```

---

### `PathOfTheVoid2`
**Description:** Conjure a random upgraded Collarless spell into your bonus spell slot.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheVoid2 {
    variant_of PathOfTheVoid

    meta {
        desc "ABILITY_PATHOFTHEVOID2_DESC"
    }

    damage_instance {
        effects {
            ConjureBonusAbility {
                ability Colorless
                upgraded true
            }
        }
    }
}
```

---

### `PathOfTheJester`
**Name:** Path of the Jester  
**Description:** Gain 10 random stat ups and 5 random stat downs, then transform this spell into a random class spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheJester {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEJESTER_NAME"
        desc "ABILITY_PATHOFTHEJESTER_DESC"
        class Colorless
    }

    tags [noncopyable]

    cost {
        cantrip true
        mana 0
    }

    damage_instance {
        effects {
            EvolveAbilityFromPool JesterMinusColorless
            RandomStatUp 10
            RandomStatUp -5
        }
    }
}
```

---

### `PathOfTheJester2`
**Name:** Path of the Jester  
**Description:** Gain 10 random stat ups, then transform this spell into a random upgraded class spell permanently.  
**Source:** `colorless_abilities.gon`  

```
PathOfTheJester2 {
    template self_buff
    
    meta {
        name "ABILITY_PATHOFTHEJESTER_NAME"
        desc "ABILITY_PATHOFTHEJESTER2_DESC"
        class Colorless
    }

    tags [noncopyable]

    cost {
        cantrip true
        mana 0
    }

    damage_instance {
        effects {
            EvolveAbilityFromPool {
                pool JesterMinusColorless
                upgraded true
            }
            RandomStatUp 10
        }
    }
}
```

---

## File: `druid_abilities.gon`

### `CrowFlutter`
**Name:** Flutter  
**Description:** Fly over 3 tiles.  
**Source:** `druid_abilities.gon`  

```
CrowFlutter {
    template move
    
    meta {
        name "ABILITY_CROWFLUTTER_NAME"
        desc "ABILITY_CROWFLUTTER_DESC"
        animate_name true
        class Druid
    }

    graphics {
        animation fast
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 3
        max_range 3
        straight_shot true
        as_the_crow_flies true
        range_mode normal
    }
}
```

---

### `CrowFlutter2`
**Description:** Fly over 3-4 tiles.  
**Source:** `druid_abilities.gon`  

```
CrowFlutter2 {
    variant_of CrowFlutter

    meta {
        desc "ABILITY_CROWFLUTTER2_DESC"
    }

    target {
        max_range 4
    }
}
```

---

### `CrowFlutter3`
**Description:** Fly over 2-5 tiles.  
**Source:** `druid_abilities.gon`  

```
CrowFlutter3 {
    variant_of CrowFlutter

    meta {
        desc "ABILITY_CROWFLUTTER3_DESC"
    }

    target {
        min_range 2
        max_range 5
    }
}
```

---

### `CrowFlap`
**Name:** Aeroblast  
**Description:** A wind gust that deals 1 damage and 1 Knockback in a line.  
**Source:** `druid_abilities.gon`  

```
CrowFlap {
    template spell
    
    meta {
        name "ABILITY_AEROBLAST_NAME"
        desc "ABILITY_AEROBLAST_DESC"
        class Druid
    }

    graphics {
        particle fx_windSpell
        animation wind
    }

    cost {
        mana 5
        infcantrip true
    }

    target {
        target_mode direction
        
        aoe_mode line
        min_aoe 1
        max_aoe 3+bonus_range
        
        aoe_considers_character_size true
        aoe_excludes_self true

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

### `CrowFlap2`
**Description:** A wind gust that deals 2 damage and 2 Knockback in a line.  
**Source:** `druid_abilities.gon`  

```
CrowFlap2 {
    variant_of CrowFlap
    meta {
        desc "ABILITY_AEROBLAST2_DESC"
    }

    target {
        max_aoe 10
    }

    damage_instance {
        damage 2
        knockback 2
    }
}
```

---

### `CrowFlap3`
**Description:** A wind gust that deals 3 damage and 10 Knockback in a line.  
**Source:** `druid_abilities.gon`  

```
CrowFlap3 {
    variant_of CrowFlap
    meta {
        desc "ABILITY_AEROBLAST3_DESC"
    }

    target {
        max_aoe 10
    }

    damage_instance {
        damage 3
        knockback 10
    }
}
```

---

### `ManaBomb`
**Name:** Bloom  
**Description:** Give 5 mana to allies in an area.  
**Source:** `druid_abilities.gon`  

```
ManaBomb {
    template spell
    
    meta {
        name "ABILITY_BLOOM_NAME"
        desc "ABILITY_BLOOM_DESC"
        class Druid
        type_icon "misc"
    }

    tags [musical]

    graphics {
        affected_particle fx_ManaHeal
        animation sing2
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 0
        max_range 3
        max_aoe 1
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0
        type spell

        effects {
            ManaGain 5
        }
    }
}
```

---

### `ManaBomb2`
**Description:** Give 5 mana to allies in a large area.  
**Source:** `druid_abilities.gon`  

```
ManaBomb2 {
    variant_of ManaBomb
    
    meta {
        desc "ABILITY_BLOOM2_DESC"
    }

    target {
        min_range 0
        max_range 6
        max_aoe 2
    }
}
```

---

### `SongOfSpring`
**Name:** Song of Spring  
**Description:** Spawn flower tiles in an area.  
**Source:** `druid_abilities.gon`  

```
SongOfSpring {
    template spell
    
    meta {
        name "ABILITY_SONGOFSPRING_NAME"
        desc "ABILITY_SONGOFSPRING_DESC"
        class Druid
        type_icon "misc"
    }

    tags [musical]

    graphics {
        animation sing1
		particle none 
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        min_range 0
        max_range 5
        max_aoe 1
    }
    
    damage_instance {
        damage 0
        type spell

        effects {
            FlowersOnHit 1
        }

        elements [
            Grass
            Bloom
        ]
    }
}
```

---

### `SongOfSpring2`
**Description:** Spawn flower tiles in a large area.  
**Source:** `druid_abilities.gon`  

```
SongOfSpring2 {
    variant_of SongOfSpring
    
    meta {
        desc "ABILITY_SONGOFSPRING2_DESC"
    }

    target {
        max_aoe 2
    }
}
```

---

### `GrantLife`
**Name:** Grant Life  
**Description:** Give a unit All Stats Up. You get All Stats Down.  
**Source:** `druid_abilities.gon`  

```
GrantLife {
    template targeted_status
    
    meta {
        name "ABILITY_GRANTLIFE_NAME"
        desc "ABILITY_GRANTLIFE_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing1
    }
    
    cost {
        infcantrip true
        mana 2
    }

    target {
        min_range 1
        max_range 5
        max_aoe 0
    }

    self_damage {
        effects {
            AllStatsUp -1
        }
    }
    
    damage_instance {
        damage 0
        type spell

        effects {
            AllStatsUp 1
        }
    }
}
```

---

### `GrantLife2`
**Description:** Give a unit All Stats Up, Charge 2, and heal them 2. You get All Stats Down.  
**Source:** `druid_abilities.gon`  

```
GrantLife2 {
    variant_of GrantLife
    
    meta {
        desc "ABILITY_GRANTLIFE2_DESC"
    }

    
    damage_instance {
        heal 2

        effects {
            AllStatsUp 1
            Charge 2
        }
    }
}
```

---

### `SquirrelSquad`
**Name:** Squirrel Squad  
**Description:** Summon 5 baby squirrels.  
**Source:** `druid_abilities.gon`  

```
SquirrelSquad {
    template spawn

    meta {
        name "ABILITY_SQUIRRELSQUAD_NAME"
        desc "ABILITY_SQUIRRELSQUAD_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 13
    }
    
    target {
        min_range 0
        max_range 3
        max_aoe 1

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object BabySquirrel
    }
}
```

---

### `SquirrelSquad2`
**Description:** Summon 5 adult squirrels.  
**Source:** `druid_abilities.gon`  

```
SquirrelSquad2 {
    variant_of SquirrelSquad

    meta {
        desc "ABILITY_SQUIRRELSQUAD2_DESC"
    }
    spawn {
        object Squirrel
    }
}
```

---

### `SquirrelFurySwipes`
**Name:** Squirrel Swipes  
**Description:** A melee attack that hits 1-3 times.  
**Source:** `druid_abilities.gon`  

```
SquirrelFurySwipes {
    class MultiHitMeleeAttackAbility
    template melee_attack
    
    meta {
        name "ABILITY_SQUIRRELSWIPES_NAME"
        desc "ABILITY_SQUIRRELSWIPES_DESC"
        class Druid
        animate_name false
    }

    graphics {
        start attack
        loop attack
        end attack
    }

    target {
        multihit_min 1
        multihit_max 3
    }

    cost {
        move_points 0
        act_points 1
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee
    }
}
```

---

### `BearFurySwipes`
**Name:** Bear Swipes  
**Source:** `druid_abilities.gon`  

```
BearFurySwipes {
    variant_of SquirrelFurySwipes
    meta {
        name "ABILITY_BEARSWIPES_NAME"
    }
}
```

---

### `SummonSquirrel`
**Name:** Summon Squirrel  
**Description:** Summon a squirrel.  
**Source:** `druid_abilities.gon`  

```
SummonSquirrel {
    template spawn

    meta {
        name "ABILITY_SUMMONSQUIRREL_NAME"
        desc "ABILITY_SUMMONSQUIRREL_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Squirrel
    }
}
```

---

### `SummonSquirrel2`
**Description:** Summon a squirrel to any tile.  
**Source:** `druid_abilities.gon`  

```
SummonSquirrel2 {
    variant_of SummonSquirrel

    meta {
        desc "ABILITY_SUMMONSQUIRREL2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `SummonSnake`
**Name:** Summon Snake  
**Description:** Summon a snake.  
**Source:** `druid_abilities.gon`  

```
SummonSnake {
    template spawn

    meta {
        name "ABILITY_SUMMONSNAKE_NAME"
        desc "ABILITY_SUMMONSNAKE_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Snake
    }
}
```

---

### `SummonSnake2`
**Description:** Summon a slippery snake!
(It has a 66% dodge chance.)  
**Source:** `druid_abilities.gon`  

```
SummonSnake2 {
    variant_of SummonSnake

    meta {
        desc "ABILITY_SUMMONSNAKE2_DESC"
    }

    spawn {
        object Snake2
    }
}
```

---

### `SummonTurtle`
**Name:** Summon Turtle  
**Description:** Summon a turtle.  
**Source:** `druid_abilities.gon`  

```
SummonTurtle {
    template spawn

    meta {
        name "ABILITY_SUMMONTURTLE_NAME"
        desc "ABILITY_SUMMONTURTLE_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Turtle
    }
}
```

---

### `SummonTurtle2`
**Description:** Summon a turtle to any tile in range 6.  
**Source:** `druid_abilities.gon`  

```
SummonTurtle2 {
    variant_of SummonTurtle

    meta {
        desc "ABILITY_SUMMONTURTLE2_DESC"
    }

    target {
        max_range 6
    }
}
```

---

### `SummonToad`
**Name:** Summon Toad  
**Description:** Summon a toad.  
**Source:** `druid_abilities.gon`  

```
SummonToad {
    template spawn

    meta {
        name "ABILITY_SUMMONTOAD_NAME"
        desc "ABILITY_SUMMONTOAD_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Toad
    }
}
```

---

### `SummonToad2`
**Description:** Summon a super toad!
(It has more damage, health, and can move an extra time each turn)  
**Source:** `druid_abilities.gon`  

```
SummonToad2 {
    variant_of SummonToad

    meta {
        desc "ABILITY_SUMMONTOAD2_DESC"
    }

    spawn {
        object Toad2
    }
}
```

---

### `SummonBear`
**Name:** Summon Bear  
**Description:** Summon a bear.  
**Source:** `druid_abilities.gon`  

```
SummonBear {
    template spawn

    meta {
        name "ABILITY_SUMMONBEAR_NAME"
        desc "ABILITY_SUMMONBEAR_DESC"
        class Druid
    }
    
    tags [summon]

    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 12
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

    spawn {
        object Bear
        size 2
    }
}
```

---

### `SummonBear2`
**Description:** Summon a furious bear!
(It has Fury Swipes.)  
**Source:** `druid_abilities.gon`  

```
SummonBear2 {
    variant_of SummonBear

    meta {
        desc "ABILITY_SUMMONBEAR2_DESC"
    }

    spawn {
        object Bear2
    }
}
```

---

### `DruidSwap`
**Name:** Step In  
**Description:** Swap positions with a familiar.  
**Source:** `druid_abilities.gon`  

```
DruidSwap {
    template swap
    
    meta {
        name "ABILITY_STEPIN_NAME"
        desc "ABILITY_STEPIN_DESC"
        animate_name true
        class Druid
    }

    graphics {
    }

    cost {
        mana 3
        infcantrip true
    }

    target {
        max_range 20
        restrictions [must_be_swappable aoe_must_exist]
        aoe_restrictions [familiars_only]
    }
}
```

---

### `DruidSwap2`
**Description:** Swap positions with any unit.  
**Source:** `druid_abilities.gon`  

```
DruidSwap2 {
    variant_of DruidSwap

    meta {
        desc "ABILITY_STEPIN2_DESC"
    }

    target {
        aoe_restrictions none
    }
}
```

---

### `BattleCry`
**Name:** Battle Cry  
**Description:** Give all familiars in an area +2 Damage.  
**Source:** `druid_abilities.gon`  

```
BattleCry {
    template targeted_status
    
    meta {
        name "ABILITY_BATTLECRY_NAME"
        desc "ABILITY_BATTLECRY_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing2
    }
    
    cost {
        infcantrip true
        mana 8
    }

    target {
        min_range 0
        max_range 4
        max_aoe 2
        //aoe_restrictions familiars_only
    }
    
    damage_instance {
        damage 0

        effects {
            Conditional_Familiar {
                DamageUp 2
            }
        }
    }
}
```

---

### `BattleCry2`
**Description:** Give all familiars +3 Damage.  
**Source:** `druid_abilities.gon`  

```
BattleCry2 {
    variant_of BattleCry
    
    meta {
        desc "ABILITY_BATTLECRY2_DESC"
    }

    target {
        target_mode none
        aoe_mode all
    }
	
	damage_instance {
        damage 0

        effects {
            Conditional_Familiar {
                DamageUp 3
            }
        }
    }
}
```

---

### `PullToSafety`
**Name:** Stand By Me  
**Description:** Teleport an ally to you.  
**Source:** `druid_abilities.gon`  

```
PullToSafety {
    template targeted_status
    
    meta {
        name "ABILITY_STANDBYME_NAME"
        desc "ABILITY_STANDBYME_DESC"
        class Druid
        type_icon "defense"
    }

    tags [musical]

    graphics {
        animation sing3
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 0
        max_range 20
        restrictions must_have_ally
    }
    
    damage_instance {
        damage 0

        effects {
            DisplaceTowardsSource 1
        }
    }
}
```

---

### `PullToSafety2`
**Description:** Teleport any unit to you.  
**Source:** `druid_abilities.gon`  

```
PullToSafety2 {
    variant_of PullToSafety
    
    meta {
        desc "ABILITY_STANDBYME2_DESC"
    }

    target {
        restrictions [must_have_character aoe_must_be_force_displaceable]
    }
}
```

---

### `BrambleBurst`
**Name:** Bramble Burst  
**Description:** Explode a familiar causing damage to all adjacent units and spawning brambles.  
**Source:** `druid_abilities.gon`  

```
BrambleBurst {
    template spell
    
    meta {
        name "ABILITY_BRAMBLEBURST_NAME"
        desc "ABILITY_BRAMBLEBURST_DESC"
        class Druid
    }

    graphics {
	    projectile BrambleProjectile
	    particle Explosion
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 0
        max_range 20

        max_aoe 1
        restrictions must_have_familiar
    }
    
    damage_instance {
        damage 5
        cant_miss true

        effects {
            VaporizeTarget 1
            ChangeTile BrambleTile
        }

        elements [
            Explosion
            Grass
        ]
    }
}
```

---

### `BrambleBurst2`
**Description:** Explode a familiar causing damage to all units in range 2 and spawning brambles.  
**Source:** `druid_abilities.gon`  

```
BrambleBurst2 {
    variant_of BrambleBurst
    
    meta {
        desc "ABILITY_BRAMBLEBURST2_DESC"
    }

    target {
        max_aoe 2
    }
}
```

---

### `FlowerFeet`
**Name:** Flower Feet  
**Description:** Move 3 tiles. Plant flowers as you move.  
**Source:** `druid_abilities.gon`  

```
FlowerFeet {
    template move
    
    meta {
        name "ABILITY_FLOWERFEET_NAME"
        desc "ABILITY_FLOWERFEET_DESC"
        animate_name true
        class Druid
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        max_range 3
    }

    temporary_effects {
        TileTrail FlowerTile
    }
}
```

---

### `FlowerFeet2`
**Description:** Move 5 tiles. Plant flowers as you move and where you end up.  
**Source:** `druid_abilities.gon`  

```
FlowerFeet2 {
    variant_of FlowerFeet
    
    meta {
        desc "ABILITY_FLOWERFEET2_DESC"
    }

    target {
        max_range 5
    }

    temporary_effects {
        TileTrail_Ahead FlowerTile
    }
}
```

---

### `ThornyFeet`
**Name:** Thorny Feet  
**Description:** Move 3 tiles. Plant brambles as you move.  
**Source:** `druid_abilities.gon`  

```
ThornyFeet {
    template move
    
    meta {
        name "ABILITY_THORNYFEET_NAME"
        desc "ABILITY_THORNYFEET_DESC"
        animate_name true
        class Druid
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        max_range 3
    }

    temporary_effects {
        TileTrail BrambleTile
    }
}
```

---

### `ThornyFeet2`
**Description:** Move 3 tiles. Plant brambles as you move.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
ThornyFeet2 {
    variant_of ThornyFeet
    
    meta {
        desc "ABILITY_THORNYFEET2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `Encourage`
**Name:** Encourage  
**Description:** Give a familiar an extra turn after this one.  
**Source:** `druid_abilities.gon`  

```
Encourage {
    template targeted_status
    
    meta {
        name "ABILITY_ENCOURAGE_NAME"
        desc "ABILITY_ENCOURAGE_DESC"
        class Druid
        type_icon "misc"
    }

    tags [musical]

    graphics {
        animation sing3
    }
    
    cost {
        infcantrip true
        mana 8
    }

    target {
        min_range 0
        max_range 3
        restrictions must_have_familiar
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

### `Encourage2`
**Description:** Give a familiar an extra turn after this one.
\[s:.7\](This spell costs less and has increased range.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
Encourage2 {
    variant_of Encourage
    
    meta {
        desc "ABILITY_ENCOURAGE2_DESC"
    }

    cost {
        mana 6
    }

    target {
        max_range 6
    }
}
```

---

### `Protection`
**Name:** Protection  
**Description:** Give a familiar +1 [img:divineshield].  
**Source:** `druid_abilities.gon`  

```
Protection {
    template targeted_status
    
    meta {
        name "ABILITY_PROTECTION_NAME"
        desc "ABILITY_PROTECTION_DESC"
        class Druid
        type_icon "defense"
    }

    tags [musical]

    graphics {
        animation sing3
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 0
        max_range 4
        max_aoe 0
        restrictions aoe_must_exist
        aoe_restrictions familiars_only
    }
    
    damage_instance {
        damage 0

        effects {
            DivineShield 1
        }
    }
}
```

---

### `Protection2`
**Name:** Protection  
**Description:** Give familiars in a large area +1 [img:divineshield].  
**Source:** `druid_abilities.gon`  

```
Protection2 {
    template targeted_status
    
    meta {
        name "ABILITY_PROTECTION_NAME"
        desc "ABILITY_PROTECTION2_DESC"
        class Druid
        type_icon "defense"
    }

    tags [musical]

    graphics {
        animation sing3
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 0
        max_range 4
        max_aoe 4
    }

    damage_instance {
        damage 0

        effects {
            Conditional_Familiar {
                DivineShield 1
            }
        }
    }
}
```

---

### `Promote`
**Name:** Promote  
**Description:** The next familiar you spawn becomes a [img:champion] champion.  
**Source:** `druid_abilities.gon`  

```
Promote {
    template self_buff
    
    meta {
        name "ABILITY_PROMOTE_NAME"
        desc "ABILITY_PROMOTE_DESC"
        class Druid
        type_icon "buff"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            ChampionUpgradeNextMinion 1
        }
    }
}
```

---

### `Promote2`
**Name:** Promote  
**Description:** The next familiar you spawn becomes an [img:elite] elite.  
**Source:** `druid_abilities.gon`  

```
Promote2 {
    template self_buff
    
    meta {
        name "ABILITY_PROMOTE_NAME"
        desc "ABILITY_PROMOTE2_DESC"
        class Druid
        type_icon "buff"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            EliteUpgradeNextMinion 1
        }
    }
}
```

---

### `SafetyDance`
**Name:** Safety Dance  
**Description:** Give all allies +1 [img:shield].  
**Source:** `druid_abilities.gon`  

```
SafetyDance {
    template spell

    meta {
        name "ABILITY_SAFETYDANCE_NAME"
        desc "ABILITY_SAFETYDANCE_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        particle fx_shield
        animation sing2
    }
    
    cost {
        mana 5
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_excludes_self true
        aoe_restrictions [allies_only]
    }

    damage_instance {
        damage 0
        effects {
            Shield 1
        }
    }
}
```

---

### `SafetyDance2`
**Description:** Give all allies +2 [img:shield].  
**Source:** `druid_abilities.gon`  

```
SafetyDance2 {
    variant_of SafetyDance

    meta {
        desc "ABILITY_SAFETYDANCE2_DESC"
    }

    damage_instance {
        effects {
            Shield 2
        }
    }
}
```

---

### `WarCry`
**Name:** War Cry  
**Description:** Each familiar attacks their closest enemy immediately if they can.  
**Source:** `druid_abilities.gon`  

```
WarCry {
    template spell

    meta {
        name "ABILITY_WARCRY_NAME"
        desc "ABILITY_WARCRY_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation howl
		particle none
    }
    
    cost {
        mana 5
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_excludes_self true
        aoe_restrictions familiars_only
    }

    damage_instance {
        damage 0
        effects {
            ForceAttack 1
        }
    }
}
```

---

### `WarCry2`
**Description:** Your allies and familiars all attack their closest enemy immediately if they can.  
**Source:** `druid_abilities.gon`  

```
WarCry2 {
    variant_of WarCry

    meta {
        desc "ABILITY_WARCRY2_DESC"
    }

    target {
        aoe_restrictions allies_only
    }
}
```

---

### `TigerForm`
**Name:** Form of the Wolf  
**Description:** Enter Wolf Form, gaining +2 [img:str], +2 [img:spd], -2 [img:lck], and -2 [img:int]. Your basic attack becomes Wolf Claws and this becomes Pounce.  
**Source:** `druid_abilities.gon`  

```
TigerForm {
    template self_buff
    
    meta {
        name "ABILITY_FORMOFTHEWOLF_NAME"
        desc "ABILITY_FORMOFTHEWOLF_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack TigerSwipes
            TransformAbility Pounce
            SpeedUp 2
            StrengthUp 2
            LuckUp -2
            IntelligenceUp -2

            CatPartsTransform {
                tail 4
                body 31
                head 12
                arm1 1013
                arm2 1013
                leg1 41
                leg2 41
                ear1 23
                ear2 23
            }
        }
    }
}
```

---

### `TigerForm2`
**Description:** Enter Wolf Form, gaining +2 [img:str], +2 [img:spd], -2 [img:lck], and -2 [img:int]. Your basic attack becomes Wolf Claws+ and this becomes Pounce+.  
**Source:** `druid_abilities.gon`  

```
TigerForm2 {
    variant_of TigerForm
    
    meta {
        desc "ABILITY_FORMOFTHEWOLF2_DESC"
    }

    damage_instance {
        effects {
            TransformBasicAttack TigerSwipes2
            TransformAbility Pounce2
        }
    }
}
```

---

### `TigerSwipes`
**Name:** Wolf Claws  
**Description:** A 2-hit melee attack.  
**Source:** `druid_abilities.gon`  

```
TigerSwipes { //alt basic for TigerForm
    template melee_attack
    
    meta {
        name "ABILITY_WOLFCLAWS_NAME"
        desc "ABILITY_WOLFCLAWS_DESC"
        class Druid
        animate_name false
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
        damage "(5+bonus_melee_damage+1)/2"
    }
}
```

---

### `TigerSwipes2`
**Description:** A 2-hit melee attack that inflicts bleed.  
**Source:** `druid_abilities.gon`  

```
TigerSwipes2 {
    variant_of TigerSwipes

    meta {
        desc "ABILITY_WOLFCLAWS2_DESC"
    }

    damage_instance {
        effects {
            Bleed 1
        }
    }
}
```

---

### `Pounce`
**Name:** Pounce  
**Description:** Jump on a unit, damaging and displacing it.  
**Source:** `druid_abilities.gon`  

```
Pounce { //alt ability for TigerForm
    template jump_attack

    meta {
        name "ABILITY_WOLFPOUNCE_NAME"
        desc "ABILITY_WOLFPOUNCE_DESC"
        class Druid
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 6
        infcantrip true
    }
    
    target {
        max_range 4

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions [must_have_character]
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `Pounce2`
**Description:** Jump on a unit, damaging, displacing and inflicting Bleed 1 to it.  
**Source:** `druid_abilities.gon`  

```
Pounce2 {
    variant_of Pounce

    meta {
        desc "ABILITY_WOLFPOUNCE2_DESC"
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage

        effects {
            Bleed 1
        }
    }
}
```

---

### `MonkeyForm`
**Name:** Form of the Monkey  
**Description:** Enter Monkey Form, gaining +2 [img:dex], +2 [img:lck], -2 [img:con], and -2 [img:cha]. Your basic attack becomes Throw Poop and this becomes Monkey Toss.  
**Source:** `druid_abilities.gon`  

```
MonkeyForm {
    template self_buff
    
    meta {
        name "ABILITY_FORMOFTHEMONKEY_NAME"
        desc "ABILITY_FORMOFTHEMONKEY_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack ThrowPoop
            TransformAbility MonkeyThrow
            DexterityUp 2
            LuckUp 2
            ConstitutionUp -2
            CharismaUp -2

            CatPartsTransform {
                tail 1502
                ear1 1501
                ear2 1501
                mouth 1501
                arm1 1501
                arm2 1501
                leg1 1501
                leg2 1501
            }
        }
    }
}
```

---

### `MonkeyForm2`
**Name:** Form of the Monkey  
**Description:** Enter Monkey Form, gaining +2 [img:dex] and +2 [img:lck]. Your basic attack becomes Throw Poop and this becomes Monkey Toss+.  
**Source:** `druid_abilities.gon`  

```
MonkeyForm2 {
    template self_buff
    
    meta {
        name "ABILITY_FORMOFTHEMONKEY_NAME"
        desc "ABILITY_FORMOFTHEMONKEY2_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack ThrowPoop
            TransformAbility MonkeyThrow2
            DexterityUp 2
            LuckUp 2

            CatPartsTransform {
                tail 1502
                ear1 1501
                ear2 1501
                mouth 1501
                arm1 1501
                arm2 1501
                leg1 1501
                leg2 1501
            }
        }
    }
}
```

---

### `ThrowPoop`
**Name:** Throw Poop  
**Description:** Throw poop.  
**Source:** `druid_abilities.gon`  

```
ThrowPoop { //alt basic attack for Monkey Form
    template lobbed_attack
    
    meta {
        name "ABILITY_THROWPOOP_NAME"
        desc "ABILITY_THROWPOOP_DESC"
        class Druid
        animate_name false
    }

    graphics {
        projectile Dip
        animation throwobject
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 4+bonus_ranged_damage

        effects {
            BounceObject CharmedDip
        }
    }
}
```

---

### `MonkeyThrow`
**Name:** Monkey Toss  
**Description:** Throw an adjacent unit to another tile. It takes damage if it's thrown onto something.  
**Source:** `druid_abilities.gon`  

```
MonkeyThrow { //bonus ability for Monkey Form
    template throw_attack
    
    meta {
        name "ABILITY_MONKEYTOSS_NAME"
        desc "ABILITY_MONKEYTOSS_DESC"
        class Druid
        type_icon "defense"
        icon_shell_frame attack
    }

    graphics {
        animation knockupatk
    }

    cost {
        mana 6
        infcantrip true
    }
    
    target {
        max_range 5
        restrictions none
    }
    
    damage_instance {
        damage 0

        blocked_damage 3+bonus_melee_ability_damage
    }
}
```

---

### `MonkeyThrow2`
**Description:** Throw an adjacent unit to another tile. It takes damage if it's thrown onto something.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
MonkeyThrow2 {
    variant_of MonkeyThrow

    meta {
        desc "ABILITY_MONKEYTOSS2_DESC"
    }
    cost {
        mana 3
    }
}
```

---

### `RhinoForm`
**Name:** Form of the Turtle  
**Description:** Enter Turtle Form, getting +2 [img:con], +10 [img:shield], -2 [img:int], and -2 [img:spd]. Your basic attack becomes Head Bash and this becomes Harden Shell.  
**Source:** `druid_abilities.gon`  

```
RhinoForm {
    template self_buff
    
    meta {
        name "ABILITY_FORMOFTHETURTLE_NAME"
        desc "ABILITY_FORMOFTHETURTLE_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack HornCharge
            TransformAbility HardenSkin
            ConstitutionUp 2
            Shield 10
            IntelligenceUp -2
            SpeedUp -2

            CatPartsTransform {
                tail 1503
                body 1029
                mouth 1005
            }
        }
    }
}
```

---

### `RhinoForm2`
**Name:** Form of the Turtle  
**Description:** Enter Turtle Form, getting +2 [img:con], +10 [img:shield], and -2 [img:int]. Your basic attack becomes Head Bash and this becomes Harden Shell+.  
**Source:** `druid_abilities.gon`  

```
RhinoForm2 {
    template self_buff
    
    meta {
        name "ABILITY_FORMOFTHETURTLE_NAME"
        desc "ABILITY_FORMOFTHETURTLE2_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack HornCharge
            TransformAbility HardenSkin2
            ConstitutionUp 2
            Shield 10
            IntelligenceUp -2
        }
    }
}
```

---

### `HardenSkin`
**Name:** Harden Shell  
**Description:** Gain +1 [img:shield], +1 Thorns, and +1 temporary Brace.  
**Source:** `druid_abilities.gon`  

```
HardenSkin {
    template self_buff
    
    meta {
        name "ABILITY_HARDENSHELL_NAME"
        desc "ABILITY_HARDENSHELL_DESC"
        class Druid
        type_icon "buff"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            Shield 1
            Thorns 1
            Temporary {
                status Brace
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `HardenSkin2`
**Description:** Gain +1 [img:shield], +1 Thorns, and +1 temporary Brace.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
HardenSkin2 {
    variant_of HardenSkin

    meta {
        desc "ABILITY_HARDENSHELL2_DESC"
    }
    cost {
        mana 3
    }
}
```

---

### `HornCharge`
**Name:** Head Bash  
**Description:** Dash forward one tile, then attack. This attack deals Knockback and has a chance to inflict Stun.  
**Source:** `druid_abilities.gon`  

```
HornCharge { //bonus ability for Rhino Form
    template dash_attack
    
    meta {
        name "ABILITY_HEADBASH_NAME"
        desc "ABILITY_HEADBASH_DESC"
        class Druid
        animate_name false
    }

    graphics {
        dash_start_animation headbuttdashStart
        dash_animation headbuttdash
        dash_attack_animation headbuttdashEnd
    }

    target { 
        max_range 1+bonus_melee_range
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1

        effects {
            Stun [1 .2]
        }
    }
}
```

---

### `SummonCatepillar`
**Name:** Summon Caterpillar  
**Description:** Summon a caterpillar. It gains All Stats Up at the end of each turn. It becomes a moth at All Stats Up 5.  
**Source:** `druid_abilities.gon`  

```
SummonCatepillar {
    template spawn

    meta {
        name "ABILITY_SUMMONCATERPILLAR_NAME"
        desc "ABILITY_SUMMONCATERPILLAR_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Catepillar
    }
}
```

---

### `SummonCatepillar2`
**Description:** Summon a caterpillar with All Stats Up 2. It gains All Stats Up at the end of each turn. It becomes a moth at All Stats Up 5.  
**Source:** `druid_abilities.gon`  

```
SummonCatepillar2 {
    variant_of SummonCatepillar

    meta {
        desc "ABILITY_SUMMONCATERPILLAR2_DESC"
    }

    spawn {
        additional_passives {
            AllStatsUp 2
        }
    }
}
```

---

### `SleepPowder`
**Name:** Sleep Powder  
**Description:** Inflict Sleep on a unit.  
**Source:** `druid_abilities.gon`  

```
SleepPowder {
    template lobbed_attack
    
    meta {
        name "ABILITY_SLEEPPOWDER_NAME"
        desc "ABILITY_SLEEPPOWDER_DESC"
        class Druid
    }

    graphics {
        animation powder
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        min_range 1
        max_range 3
        max_aoe 0
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Sleep 1
        }
    }
}
```

---

### `CallTheWind`
**Name:** Call the Wind  
**Description:** Blow all units back one tile.  
**Source:** `druid_abilities.gon`  

```
CallTheWind {
    template spell

    meta {
        name "ABILITY_CALLTHEWIND_NAME"
        desc "ABILITY_CALLTHEWIND_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing3
        particle fx_windSpell
    }
    
    cost {
        mana 4
        infcantrip true
    }

    
    target {
        target_mode direction
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode orientation
    }

    damage_instance {
        damage 0
        knockback 1

        elements [
            Wind
        ]
    }
}
```

---

### `CallTheWind2`
**Description:** Blow all units back three tiles.
Allies are immune to knockback damage during this.  
**Source:** `druid_abilities.gon`  

```
CallTheWind2 {
    variant_of CallTheWind

    meta {
        desc "ABILITY_CALLTHEWIND2_DESC"
    }

    damage_instance {
        damage 0
        knockback 3

        effects {
            Conditional_Ally {
                KnockbackDamageImmuneUntilSettled 1
            }
        }
    }
}
```

---

### `InspirationalSong`
**Name:** Inspirational Song  
**Description:** Heal all allies and give them +1 Temporary Damage.  
**Source:** `druid_abilities.gon`  

```
InspirationalSong {
    template spell

    meta {
        name "ABILITY_INSPIRATIONALSONG_NAME"
        desc "ABILITY_INSPIRATIONALSONG_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing3
		particle fx_statup
    }
    
    cost {
        mana 4
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_excludes_self true
        aoe_restrictions [allies_only]
    }

    damage_instance {
        heal 1
        effects {
            TempDamageUp 1
        }
    }
}
```

---

### `InspirationalSong2`
**Description:** Heal all allies and give them +2 Temporary Damage.  
**Source:** `druid_abilities.gon`  

```
InspirationalSong2 {
    variant_of InspirationalSong

    meta {
        desc "ABILITY_INSPIRATIONALSONG2_DESC"
    }

    damage_instance {
        heal 2
        effects {
            TempDamageUp 2
        }
    }
}
```

---

### `DeathMetal`
**Name:** Death Metal  
**Description:** A song that explodes a random enemy. If this hits a boss, it instead inflicts Fear.  
**Source:** `druid_abilities.gon`  

```
DeathMetal {//TODO: makevoice very low for this
    template spell

    meta {
        name "ABILITY_DEATHMETAL_NAME"
        desc "ABILITY_DEATHMETAL_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing3
		particle None
    }
    
    cost {
        mana 13
        infcantrip true
    }

    
    target {
        target_mode random_tile
        max_aoe 0
        max_range 20

        restrictions [must_have_living_character must_have_enemy]
    }

    damage_instance {
        damage 0

        effects {
            Conditional_Boss {
                Fear 1
                VisualFX Explosion
                ExplodeCharacter_NoDie 5
            } Else {
                ExplodeCharacter 5
            }
        }
    }
}
```

---

### `DeathMetal2`
**Description:** A song that explodes a random enemy. If this hits a boss, it instead inflicts Fear. Inflict Madness on each other enemy.  
**Source:** `druid_abilities.gon`  

```
DeathMetal2 {
    variant_of DeathMetal

    meta {
        desc "ABILITY_DEATHMETAL2_DESC"
    }

    target {
        max_aoe 20
    }

    splash_damage {
        damage 0

        effects {
            Conditional_Enemy {
                Madness 1
            }
        }
    }
}
```

---

### `ChaChaSlide`
**Name:** Cha Cha Slide  
**Description:** Deal 10 Knockback to all units in a random direction. Allies are immune to Thorns, tile and Knockback damage during this effect.  
**Source:** `druid_abilities.gon`  

```
ChaChaSlide {
    template spell

    meta {
        name "ABILITY_CHACHASLIDE_NAME"
        desc "ABILITY_CHACHASLIDE_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing3
        particle none
    }
    
    cost {
        mana 5
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
    }

    damage_instance {
        damage 0
        knockback 10

        effects {
            RandomKnockbackDirection 4

            KnockbackDamageImmuneUntilSettled 1
            ThornsDamageImmuneUntilSettled 1
            TileDamageImmuneUntilSettled 1
        }
    }
}
```

---

### `ChaChaSlide2`
**Description:** Deal 10 Knockback to all units in a random direction. Allies gain +3 temporary Thorns and are immune to Thorns, tile and Knockback damage during this effect.  
**Source:** `druid_abilities.gon`  

```
ChaChaSlide2 {
    variant_of ChaChaSlide

    meta {
        desc "ABILITY_CHACHASLIDE2_DESC"
    }

    damage_instance {
        effects {
            Conditional_Ally {
                Temporary {
                    status Thorns
                    stacks 3
                    turns 1
                    expires_on_begin_turn true
                }

                KnockbackDamageImmuneUntilSettled 1
                ThornsDamageImmuneUntilSettled 1
                TileDamageImmuneUntilSettled 1
            }
        }
    }
}
```

---

### `BestowWisdom`
**Name:** Bestow Wisdom  
**Description:** Give +1 [img:int] to a unit.  
**Source:** `druid_abilities.gon`  

```
BestowWisdom {
    template targeted_status
    
    meta {
        name "ABILITY_BESTOWWISDOM_NAME"
        desc "ABILITY_BESTOWWISDOM_DESC"
        class Druid
        type_icon "misc"
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        min_range 1
        max_range 5
    }
    
    damage_instance {
        effects {
            IntelligenceUp 1
        }
    }
}
```

---

### `BestowWisdom2`
**Description:** Give +1 [img:int] and +2 mana to a unit.  
**Source:** `druid_abilities.gon`  

```
BestowWisdom2 {
    variant_of BestowWisdom
    
    meta {
        desc "ABILITY_BESTOWWISDOM2_DESC"
    }

    damage_instance {
        effects {
            CharismaUp 1
            ManaGain 2
        }
    }
}
```

---

### `RaccoonForm`
**Name:** Form of the Raccoon  
**Description:** Enter Raccoon Form, gaining +2 [img:int], and -2 [img:str]. Your basic attack becomes Pilfer and this becomes Scavenge.  
**Source:** `druid_abilities.gon`  

```
RaccoonForm {
    template self_buff
    
    meta {
        name "ABILITY_FORMOFTHERACCOON_NAME"
        desc "ABILITY_FORMOFTHERACCOON_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack Pilfer
            TransformAbility Scavenge
            IntelligenceUp 2
            StrengthUp -2
            
            CatPartsTransform {
                tail 1504
                head 1504
                texture 1008
            }
        }
    }
}
```

---

### `RaccoonForm2`
**Name:** Form of the Raccoon  
**Description:** Enter Raccoon Form, gaining +2 [img:int], and +2 [img:lck]. Your basic attack becomes Pilfer and this becomes Scavenge+.  
**Source:** `druid_abilities.gon`  

```
RaccoonForm2 {
    template self_buff
    
    meta {
        name "ABILITY_FORMOFTHERACCOON_NAME"
        desc "ABILITY_FORMOFTHERACCOON2_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack Pilfer
            TransformAbility Scavenge2
            IntelligenceUp 2
            LuckUp 2
            
            CatPartsTransform {
                tail 1504
                head 1504
                texture 1008
            }
        }
    }
}
```

---

### `Pilfer`
**Name:** Pilfer  
**Description:** A melee attack that scatters two random pickups when it hits.  
**Source:** `druid_abilities.gon`  

```
Pilfer { //alt basic for RaccoonForm
    template melee_attack
    
    meta {
        name "ABILITY_PILFER_NAME"
        desc "ABILITY_PILFER_DESC"
        class Druid
        animate_name false
    }

    damage_instance {
        damage 2+bonus_melee_damage

        effects {
            ScatterRandomPickups 2
        }
    }
}
```

---

### `Scavenge`
**Name:** Scavenge  
**Description:** Run to any pickup and collect it.  
**Source:** `druid_abilities.gon`  

```
Scavenge {
    template move
    
    meta {
        name "ABILITY_SCAVENGE_NAME"
        desc "ABILITY_SCAVENGE_DESC"
        animate_name true
        class Druid
    }

    graphics {
        speed 1.5
        animation dash
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 100
        restrictions [must_be_moveable must_have_tag must_move]
        target_requires_tag pickup
    }
}
```

---

### `Scavenge2`
**Description:** Run to any pickup and collect it. The effects of that pickup are doubled.  
**Source:** `druid_abilities.gon`  

```
Scavenge2 {
    variant_of Scavenge
    
    meta {
        desc "ABILITY_SCAVENGE2_DESC"
    }

    temporary_effects {
        DoubleLoot 1
    }
}
```

---

### `SummonCrow`
**Name:** Resummon Crow  
**Description:** Summon a new crow. Castable only if your crow is dead.  
**Source:** `druid_abilities.gon`  

```
SummonCrow {
    template spawn

    meta {
        name "ABILITY_SUMMONCROW_NAME"
        desc "ABILITY_SUMMONCROW_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 11
    }

    bonus_passives {
        AbilityDisableIfLivingCrow 1
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Crow
    }
}
```

---

### `SummonCrow2`
**Name:** Resummon Crow  
**Description:** Summon a crow.  
**Source:** `druid_abilities.gon`  

```
SummonCrow2 {
    template spawn

    meta {
        name "ABILITY_SUMMONCROW_NAME"
        desc "ABILITY_SUMMONCROW2_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 11
    }

    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Crow
    }
}
```

---

### `WeWillRockYou`
**Name:** We Will Rock You  
**Description:** Inflict Petrify on a familiar and give it +6 [img:shield].  
**Source:** `druid_abilities.gon`  

```
WeWillRockYou {
    template targeted_status
    
    meta {
        name "ABILITY_WEWILLROCKYOU_NAME"
        desc "ABILITY_WEWILLROCKYOU_DESC"
        class Druid
        type_icon "defense"
    }

    tags [musical]

    graphics {
        animation sing3
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 0
        max_range 7
        max_aoe 0
        restrictions aoe_must_exist
        aoe_restrictions familiars_only
    }
    
    damage_instance {
        damage 0

        effects {
            Shield 6
            Petrify 1
        }
    }
}
```

---

### `WeWillRockYou2`
**Description:** Inflict Petrify on a familiar and give it +6 [img:shield] and +2 Thorns.  
**Source:** `druid_abilities.gon`  

```
WeWillRockYou2 {
    variant_of WeWillRockYou

    meta {
        desc "ABILITY_WEWILLROCKYOU2_DESC"
    }

    damage_instance {
        effects {
            Thorns 2
        }
    }
}
```

---

### `TreeForm`
**Name:** Form of the Tree  
**Description:** Enter Tree Form, gaining -2 [img:int], +5 [img:shield], and Brace 2. You become immobile and immune to Knockback. Your basic attack becomes Timber and this becomes Synthesize.  
**Source:** `druid_abilities.gon`  

```
TreeForm {
    template self_buff
    
    meta {
        name "ABILITY_FORMOFTHETREE_NAME"
        desc "ABILITY_FORMOFTHETREE_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack Timber
            TransformAbility Synthesize
            IntelligenceUp -2
            PermanentImmobile 1
            Brace 2
            Shield 5
            ApplyPassives {
                KnockbackImmunity 1
                AddTag plant
                Plant 1
                ElementImmune Creep
            }
            
            CatPartsTransform {
                texture 322
                ear1 325
                arm2 324
            }
        }
    }
}
```

---

### `TreeForm2`
**Description:** Enter Tree Form, gaining -2 [img:int], +5 [img:shield], and Brace 4. You become immobile and immune to Knockback. Your basic attack becomes Timber and this becomes Synthesize+.  
**Source:** `druid_abilities.gon`  

```
TreeForm2 {
    variant_of TreeForm

    meta {
        desc "ABILITY_FORMOFTHETREE2_DESC"
    }

    damage_instance {
        effects {
            TransformAbility Synthesize2
            FullHeal 1
            Brace 4
        }
    }
}
```

---

### `Timber`
**Name:** Timber  
**Description:** Fall into an adjacent tile, dealing massive damage to units you displace.  
**Source:** `druid_abilities.gon`  

```
Timber { //alt basic for TreeForm
    template trample_dash
    
    meta {
        name "ABILITY_TIMBER_NAME"
        desc "ABILITY_TIMBER_DESC"
        class Druid
        type_icon "melee"
    }
    
    graphics {
        dash_start_animation timberStart
        dash_animation timberDash
        dash_end_animation timberEnd
    }
    
    cost {
        act_points 1
        move_points 0
    }
    
    target {
        max_range 1+bonus_range
    }

    temporary_effects {
        Trample 3
    }
    
    damage_instance {
        override_trample_damage true
        damage 10+bonus_melee_damage
    }
}
```

---

### `Synthesize`
**Name:** Synthesize  
**Description:** Heal 2 HP and gain Charge 2.  
**Source:** `druid_abilities.gon`  

```
Synthesize {
    template self_buff
    
    meta {
        name "ABILITY_SYNTHESIZE_NAME"
        desc "ABILITY_SYNTHESIZE_DESC"
        class Druid
        type_icon "buff"
    }

    graphics {
		particle HealSmall
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        heal 2
        effects {
            Charge 2
        }
    }
}
```

---

### `Synthesize2`
**Description:** You and allies within 3 tiles gain 2 HP and 2 Charge.  
**Source:** `druid_abilities.gon`  

```
Synthesize2 {
    variant_of Synthesize

    meta {
        desc "ABILITY_SYNTHESIZE2_DESC"
    }

    target {
        max_aoe 3
        aoe_restrictions [allies_only]
    }
}
```

---

### `HydroPump`
**Name:** Hydro Pump  
**Description:** Shoot a blast of water that deals 3 Knockback. This spell has recoil.  
**Source:** `druid_abilities.gon`  

```
HydroPump {
    template spell
    
    meta {
        name "ABILITY_HYDROPUMP_NAME"
        desc "ABILITY_HYDROPUMP_DESC"
        class Druid
    }

    graphics {
        particle Wave
        animation shoot
    }

    cost {
        mana 4
        infcantrip true
    }

    target {
        target_mode direction
        
        aoe_mode line
        min_aoe 1
        max_aoe 3
        
        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode orientation
    }

    self_damage {
        knockback -3

        effects {
            KnockbackDamageImmuneUntilSettled 1
        }

        elements [
            Water
        ]
    }

    damage_instance {
        damage 0
        knockback 3

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

### `HydroPump2`
**Description:** Shoot a long blast of water that deals 10 Knockback. This spell has recoil.  
**Source:** `druid_abilities.gon`  

```
HydroPump2 {
    variant_of HydroPump

    meta {
        desc "ABILITY_HYDROPUMP2_DESC"
    }

    target {
        max_aoe 10
    }

    self_damage {
        knockback -10
    }

    damage_instance {
        knockback 10
    }
}
```

---

### `ControlPlants`
**Name:** Control Plants  
**Description:** Create a tall grass tile, then all enemies on grass element tiles take 1 damage.  
**Source:** `druid_abilities.gon`  

```
ControlPlants {
    template spell
    chain_ability ControlPlantsPartTwo
    
    meta {
        name "ABILITY_CONTROLPLANTS_NAME"
        desc "ABILITY_CONTROLPLANTS_DESC"
        class Druid
        type_icon "misc"
    }
	
	graphics {
        particle VineWhip
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 1
        max_range 4
        max_aoe 0
    }
    
    damage_instance {
        damage 1
        type spell

        effects {
            ChangeTile TallGrassTile
            OverrideDamage 0
        }

        elements [
            Grass
        ]
    }
}
```

---

### `ControlPlants2`
**Description:** Create a tall grass tile, then all enemies on grass element tiles take 1 damage and gain Poison 1.  
**Source:** `druid_abilities.gon`  

```
ControlPlants2 {
    variant_of ControlPlants
    chain_ability ControlPlantsPartTwo2
    
    meta {
        desc "ABILITY_CONTROLPLANTS2_DESC"
    }

    target {
        max_range 6
    }
}
```

---

### `ControlPlantsPartTwo`
**Source:** `druid_abilities.gon`  

```
ControlPlantsPartTwo {
    template spell

    graphics {
        animation none
		particle VineWhip
    }

    target {
        target_mode none
        aoe_mode all
        
        aoe_restrictions [enemies_only character_must_be_affected_by_tile_with_element]
        aoe_tile_requires_element Grass
    }

    damage_instance {
        damage 1
    }
}
```

---

### `ControlPlantsPartTwo2`
**Source:** `druid_abilities.gon`  

```
ControlPlantsPartTwo2 {
    variant_of ControlPlantsPartTwo

    damage_instance {
        effects {
            Poison 1
        }
    }
}
```

---

### `ControlWater`
**Name:** Control Water  
**Description:** Create a water tile, then all allies on water element tiles heal 2 HP.  
**Source:** `druid_abilities.gon`  

```
ControlWater {
    template spell
    chain_ability ControlWaterPartTwo
	
	graphics {
        particle Wave
    }
    
    meta {
        name "ABILITY_CONTROLWATER_NAME"
        desc "ABILITY_CONTROLWATER_DESC"
        class Druid
        type_icon "misc"
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 1
        max_range 4
        max_aoe 0
    }
    
    damage_instance {
        heal 2
        type spell

        effects {
            ChangeTile WaterTile
            OverrideDamage 0
        }

        elements [
            Water
        ]
    }
}
```

---

### `ControlWater2`
**Description:** Create a water tile, then all allies on water element tiles heal 2 HP and have their debuffs cleansed.  
**Source:** `druid_abilities.gon`  

```
ControlWater2 {
    variant_of ControlWater
    chain_ability ControlWaterPartTwo2
    
    meta {
        desc "ABILITY_CONTROLWATER2_DESC"
    }

    target {
        max_range 6
    }
}
```

---

### `ControlWaterPartTwo`
**Source:** `druid_abilities.gon`  

```
ControlWaterPartTwo {
    template spell

    graphics {
        animation none
		particle none
    }

    target {
        target_mode none
        aoe_mode all
        
        aoe_restrictions [allies_only character_must_be_affected_by_tile_with_element]
        aoe_tile_requires_element Water
    }

    damage_instance {
        heal 2
    }
}
```

---

### `ControlWaterPartTwo2`
**Source:** `druid_abilities.gon`  

```
ControlWaterPartTwo2 {
    variant_of ControlWaterPartTwo

    damage_instance {
        effects {
            Cleanse 0
        }
    }
}
```

---

### `ControlAir`
**Name:** Control Air  
**Description:** Blow a unit ten tiles away from you. This doesn't deal Knockback damage.  
**Source:** `druid_abilities.gon`  

```
ControlAir {
    template spell

    meta {
        name "ABILITY_CONTROLAIR_NAME"
        desc "ABILITY_CONTROLAIR_DESC"
        class Druid
        type_icon "magic"
    }

    graphics {
        particle fx_windSpell
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_aoe 0
        min_range 1
        max_range 4
        knockback_mode character_to_target
    }
    
    damage_instance {
        damage 0
        knockback 10

        effects {
            OverrideKnockbackDamage 0
        }

        elements [
            Wind
        ]
    }
}
```

---

### `ControlAir2`
**Description:** Blow a unit ten tiles away from you. This doesn't deal Knockback damage.
\[s:.7\](This spell costs less and has infinite range.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
ControlAir2 {
    variant_of ControlAir

    meta {
        desc "ABILITY_CONTROLAIR2_DESC"
    }

    cost {
        mana 3
    }

    target {
        max_range 20
    }
}
```

---

### `FamiliarSelfDestruct`
**Name:** Self-destruct  
**Description:** Explode.  
**Source:** `druid_abilities.gon`  

```
FamiliarSelfDestruct {
    template spell

    meta {
        name "ABILITY_SELFDESTRUCTFAMILIAR_NAME"
        desc "ABILITY_SELFDESTRUCTFAMILIAR_DESC"
        class Druid
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
        aoe_considers_character_size true
    }


    damage_instance {
        ai_base_score -999999
        damage 7
        knockback 1
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
        damage 8
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

### `FamiliarSelfDestruct2`
**Source:** `druid_abilities.gon`  

```
FamiliarSelfDestruct2 {
    variant_of FamiliarSelfDestruct

    damage_instance {
        damage 12
    }
    splash_damage {
        damage 12
    }
}
```

---

### `FeralMelee`
**Name:** Feral Attack  
**Description:** A melee attack.
\[s:.7\](This spell costs 0 mana. Castable once per turn.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
FeralMelee {
    template melee_attack
    
    meta {
        name "ABILITY_FERALMELEE_NAME"
        desc "ABILITY_FERALMELEE_DESC"
        animate_name false
        class Druid
    }

    cost {
        mana 0
        cantrip true
    }

    target { 
        max_aoe 1+bonus_melee_range
        aoe_restrictions must_have_line_of_sight_unpurgable
    }
}
```

---

### `Entangle`
**Name:** Entangle  
**Description:** Entangle units in an area.  
**Source:** `druid_abilities.gon`  

```
Entangle {
    template lobbed_attack
	
	graphics {
        projectile SpiderBall
    }
    
    meta {
        name "ABILITY_ENTANGLE_NAME"
        desc "ABILITY_ENTANGLE_DESC"
        class Druid
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 0
        max_range 4
        max_aoe 1
    }
    
    damage_instance {
        damage 0

        effects {
            Tangled 1
        }
    }
}
```

---

### `Entangle2`
**Description:** Entangle units in an area and spawn bramble tiles.  
**Source:** `druid_abilities.gon`  

```
Entangle2 {
    variant_of Entangle

    meta {
        desc "ABILITY_ENTANGLE2_DESC"
    }

    damage_instance {
        effects {
            ChangeTile BrambleTile
        }
    }
}
```

---

### `Lullaby`
**Name:** Lullaby  
**Description:** Inflicts Sleep on units in an area.  
**Source:** `druid_abilities.gon`  

```
Lullaby {
    template spell
    
    meta {
        name "ABILITY_LULLABY_NAME"
        desc "ABILITY_LULLABY_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing2
		particle none
    }

    cost {
        infcantrip true
        mana 12
    }

    target {
        min_range 0
        max_range 4
        max_aoe 2
    }
    
    damage_instance {
        damage 0

        effects {
            Sleep 1
        }
    }
}
```

---

### `Lullaby2`
**Description:** Inflicts Sleep on units in an area.
\[s:.7\](This spell costs less and has increased range.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
Lullaby2 {
    variant_of Lullaby

    meta {
        desc "ABILITY_LULLABY2_DESC"
    }

    cost {
        mana 9
    }

    target {
        max_range 6
    }
}
```

---

### `WeAreTheChampions`
**Name:** We Are the Champions  
**Description:** Each familiar gains All Stats Up 2 and heals to full.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
WeAreTheChampions {
    template targeted_status
    
    meta {
        name "ABILITY_WEARETHECHAMPIONS_NAME"
        desc "ABILITY_WEARETHECHAMPIONS_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing2
    }
    
    cost {
        infcantrip true
        mana 7
        once_per_fight true
    }

    target {
        target_mode none
        aoe_mode all
        aoe_restrictions familiars_only
    }
    
    damage_instance {
        heal 0

        effects {
            AllStatsUp 2
            FullHeal 1
        }
    }
}
```

---

### `WeAreTheChampions2`
**Description:** Each familiar gains All Stats Up 2 and heals to full.
\[s:.7\](This spell costs 0 mana. Castable once per battle.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
WeAreTheChampions2 {
    variant_of WeAreTheChampions
    
    meta {
        desc "ABILITY_WEARETHECHAMPIONS2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `Cheerlead`
**Name:** Cheerlead  
**Description:** Make a target unit The Alpha.
PASSIVE: The first spell the Alpha casts each turn is cast twice.  
**Source:** `druid_abilities.gon`  

```
Cheerlead {
    template targeted_status
    
    meta {
        name "ABILITY_CHEERLEAD_NAME"
        desc "ABILITY_CHEERLEAD_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing1
    }
    
    cost {
        infcantrip true
        mana 10
    }

    target {
        min_range 1
        max_range 5
    }

    bonus_passives {
        AlphaStatusOnTurnBegin {
            DoubleCastSpellThisTurn 1
        }
    }
    
    damage_instance {
        effects {
            AlphaCat 1
        }
    }
}
```

---

### `Cheerlead2`
**Description:** Make a target unit The Alpha.
PASSIVE: The first spell the Alpha casts each turn is cast twice.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
Cheerlead2 {
    variant_of Cheerlead

    meta {
        desc "ABILITY_CHEERLEAD2_DESC"
    }

    cost {
        mana 5
    }
}
```

---

### `NaturesBlessing`
**Name:** Nature's Blessing  
**Description:** Grow tall grass tiles in an area and give units in that area +3 Diminishing Health Regeneration  
**Source:** `druid_abilities.gon`  

```
NaturesBlessing {
    template spell
	
    graphics {
        particle none
        animation createmagic
    }
    
    meta {
        name "ABILITY_NATURESBLESSING_NAME"
        desc "ABILITY_NATURESBLESSING_DESC"
        class Druid
    }

    cost {
        infcantrip true
        mana 9
    }

    target {
        min_range 0
        max_range 4
        max_aoe 2
    }
    
    damage_instance {
        damage 0

        effects {
            ChangeTile TallGrassTile
            DiminishingHealthRegen 3
        }

        elements [
            Grass
        ]
    }
}
```

---

### `NaturesBlessing2`
**Description:** Grow tall grass tiles in an area and give units in that area +3 Diminishing Health Regeneration
\[s:.7\](This spell costs less and has infinite range.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
NaturesBlessing2 {
    variant_of NaturesBlessing

    meta {
        desc "ABILITY_NATURESBLESSING2_DESC"
    }

    cost {
        mana 7
    }

    target {
        max_range 20
    }
}
```

---

### `ThrowEgg`
**Name:** Throw Egg  
**Description:** Throw an egg. If the egg lands in an empty tile, it hatches into a random animal friend at the start of its second turn.  
**Source:** `druid_abilities.gon`  

```
ThrowEgg {
    template lobbed_attack
    
    meta {
        name "ABILITY_THROWEGGDRUID_NAME"
        desc "ABILITY_THROWEGGDRUID_DESC"
        class Druid
    }

    tags [summon]

    graphics {
        projectile AnimalEgg
        animation throwobject
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        min_range 1
        max_range 5+bonus_range
    }

    damage_instance {
        damage 4+bonus_ranged_damage

        effects {
            ObjectOnHitEmpty AnimalEgg
        }
    }
}
```

---

### `ThrowEgg2`
**Description:** Throw an egg. If the egg lands in an empty tile, it hatches into a random animal friend at the start of its first turn.  
**Source:** `druid_abilities.gon`  

```
ThrowEgg2 {
    variant_of ThrowEgg

    meta {
        desc "ABILITY_THROWEGGDRUID2_DESC"
    }

    damage_instance {
        effects {
            ObjectOnHitEmpty AnimalEgg2
        }
    }
}
```

---

### `SquirrelForm`
**Name:** Form of the Squirrel  
**Description:** Spawn squirrels on each adjacent tile, then enter Squirrel Form.
Your basic attack becomes Chitter and this becomes Birth Squirrel.  
**Source:** `druid_abilities.gon`  

```
SquirrelForm {
    template spawn
    
    meta {
        name "ABILITY_SQUIRRELFORM_NAME"
        desc "ABILITY_SQUIRRELFORM_DESC"
        class Druid
    }

    tags [shapeshift summon]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 10
    }

    target {
        target_mode none
        max_aoe 1
    }
    
    self_damage {
        effects {
            TransformBasicAttack Chitter
            TransformAbility BirthSquirrel
            ApplyPassives {
                AddTag squirrel
            }
            CatPartsTransform {
                mouth 1071
                tail 1042
                ear1 1036
                ear2 1036
            }
        }
    }

    spawn {
        object Squirrel
    }
}
```

---

### `SquirrelForm2`
**Description:** Spawn squirrels on each adjacent tile, then enter Squirrel Form.
Your basic attack becomes Chitter and this becomes Birth Squirrel+.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
SquirrelForm2 {
    variant_of SquirrelForm

    meta {
        desc "ABILITY_SQUIRRELFORM2_DESC"
    }

    cost {
        mana 7
    }

    self_damage {
        effects {
            TransformAbility BirthSquirrel2
        }
    }
}
```

---

### `BirthSquirrel`
**Name:** Birth Squirrel  
**Description:** Summon a squirrel.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
BirthSquirrel {
    template spawn

    meta {
        name "ABILITY_BIRTHSQUIRREL_NAME"
        desc "ABILITY_BIRTHSQUIRREL_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
        animation poopfart
    }
    
    cost {
        cantrip true
        mana 2
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Squirrel
    }
}
```

---

### `BirthSquirrel2`
**Source:** `druid_abilities.gon`  

```
BirthSquirrel2 {
    variant_of BirthSquirrel

    cost {
        mana 0
    }
}
```

---

### `Chitter`
**Name:** Chitter  
**Description:** Each squirrel gains +2 Damage and +2 [img:spd].  
**Source:** `druid_abilities.gon`  

```
Chitter {
    template spell
    
    meta {
        name "ABILITY_CHITTER_NAME"
        desc "ABILITY_CHITTER_DESC"
        animate_name false
        class Druid
    }
    tags [musical]

    graphics {
        animation sing3//howl
		particle fx_statup
    }

    target { 
        target_mode none
        max_aoe 20

        aoe_restrictions must_have_tag
        target_requires_tag squirrel
    }

    damage_instance {
        damage 0
        cant_miss true

        effects {
            DamageUp 2
            SpeedUp 2
        }
    }
}
```

---

### `GlowingMushroomGiveMana`
**Source:** `druid_abilities.gon`  

```
GlowingMushroomGiveMana { //util ability for Glowing Mushroom, does not need icon
    template spell

    graphics {
        animation puff
		particle DustPoofMedium
    }

    target { 
        target_mode none
        max_aoe 3
        aoe_excludes_self true
    }

    damage_instance {
        damage 0
        cant_miss true

        effects {
            ManaGain 1
        }
    }
}
```

---

### `GlowingMushroomGiveMana2`
**Source:** `druid_abilities.gon`  

```
GlowingMushroomGiveMana2 {
    variant_of GlowingMushroomGiveMana

    damage_instance {
        heal 1
        cant_miss true

        effects {
            ManaGain 1
        }
    }
}
```

---

### `PlantMushroom`
**Name:** Plant Mushroom  
**Description:** Spawn a glowing mushroom that restores mana to nearby units on its turn.  
**Source:** `druid_abilities.gon`  

```
PlantMushroom {
    template spawn

    meta {
        name "ABILITY_PLANTMUSHROOM_NAME"
        desc "ABILITY_PLANTMUSHROOM_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        lob true
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object GlowingMushroom
    }
}
```

---

### `PlantMushroom2`
**Description:** Spawn a glowing mushroom anywhere that restores mana and health to nearby units on its turn.  
**Source:** `druid_abilities.gon`  

```
PlantMushroom2 {
    variant_of PlantMushroom

    meta {
        desc "ABILITY_PLANTMUSHROOM2_DESC"
    }

    target {
        max_range 20
    }

    spawn {
        object GlowingMushroom2
    }
}
```

---

### `Serenade`
**Name:** Serenade  
**Description:** Give Health Regeneration 1 to units in an area.  
**Source:** `druid_abilities.gon`  

```
Serenade {
    template targeted_status
    
    meta {
        name "ABILITY_SERENADE_NAME"
        desc "ABILITY_SERENADE_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation sing2
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 0
        max_range 4
        max_aoe 1
    }
    
    damage_instance {
        damage 0

        effects {
            HealthRegenUp 1
        }
    }
}
```

---

### `Serenade2`
**Description:** Give Health Regeneration 1 to units in a larger area.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
Serenade2 {
    variant_of Serenade

    meta {
        desc "ABILITY_SERENADE2_DESC"
    }

    cost {
        mana 4
    }

    target {
        max_aoe 2
    }
}
```

---

### `WindyStep`
**Name:** Windy Step  
**Description:** Give a unit +1 Bonus Move.  
**Source:** `druid_abilities.gon`  

```
WindyStep {
    template targeted_status
    
    meta {
        name "ABILITY_WINDYSTEP_NAME"
        desc "ABILITY_WINDYSTEP_DESC"
        class Druid
        type_icon "misc"
    }

    graphics {
        particle fx_windSpell
		animation castspell
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 1
        max_range 5
    }
    
    damage_instance {
        effects {
            MoveQuivered 1
        }

        elements [
            Wind
        ]
    }
}
```

---

### `WindyStep2`
**Description:** Give a unit +1 Bonus Move and +1 [img:spd]. They take their next turn earlier.  
**Source:** `druid_abilities.gon`  

```
WindyStep2 {
    variant_of WindyStep

    meta {
        desc "ABILITY_WINDYSTEP2_DESC"
    }

    damage_instance {
        effects {
            MoveQuivered 1
            SpeedUp 1
            TempInitiativeChange 100
        }
    }
}
```

---

### `ElkForm`
**Name:** Form of the Elk  
**Description:** Enter Elk Form, gaining +8 [img:spd], -2 [img:int], -2 [img:con], and Trample 3. You ignore tile effects while moving.
Your basic attack becomes Antler Swipe and this becomes Prance.  
**Source:** `druid_abilities.gon`  

```
ElkForm {
    template self_buff
    
    meta {
        name "ABILITY_ELKFORM_NAME"
        desc "ABILITY_ELKFORM_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack AntlerSwipe
            TransformAbility Prance

            SpeedUp 8
            IntelligenceUp -2
            ConstitutionUp -2
            Trample 3

            ApplyPassives {
                IgnoreTiles 1
                YOffset .25
            }

            CatPartsTransform {
                leg1 338
                leg2 338
                arm1 338
                arm2 338
                ear1 343
                ear2 343
            }
        }
    }
}
```

---

### `ElkForm2`
**Name:** Form of the Elk  
**Description:** Enter Elk Form, gaining +8 [img:spd] and Trample 3. You ignore tile effects while moving.
Your basic attack becomes Antler Swipe+ and this becomes Prance+.  
**Source:** `druid_abilities.gon`  

```
ElkForm2 {
    template self_buff
    
    meta {
        name "ABILITY_ELKFORM_NAME"
        desc "ABILITY_ELKFORM2_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack AntlerSwipe2
            TransformAbility Prance2

            SpeedUp 8
            Trample 3

            ApplyPassives {
                IgnoreTiles 1
                YOffset .25
            }

            CatPartsTransform {
                leg1 338
                leg2 338
                arm1 338
                arm2 338
                ear1 343
                ear2 343
            }
        }
    }
}
```

---

### `AntlerSwipe`
**Name:** Antler Swipe  
**Description:** Toss a unit up to four tiles away. Inflict Bruise on it and any unit it lands on.  
**Source:** `druid_abilities.gon`  

```
AntlerSwipe { //basic attack for Elk Form
    template throw_attack
    
    meta {
        name "ABILITY_ANTLERSWIPE_NAME"
        desc "ABILITY_ANTLERSWIPE_DESC"
        class Druid
    }

    graphics {
        animation headbuttUppercut
    }

    target {
        max_range 4
        restrictions none
    }
    
    damage_instance {
        damage 0
		force_play_hit_animation true

        effects {
            Bruise 1
        }
    }
}
```

---

### `AntlerSwipe2`
**Description:** Toss a unit up to four tiles away. Deal damage to and inflict Bruise on it and any unit it lands on.  
**Source:** `druid_abilities.gon`  

```
AntlerSwipe2 { //basic attack for Elk Form
    variant_of AntlerSwipe

    meta {
        desc "ABILITY_ANTLERSWIPE2_DESC"
    }

    damage_instance {
        damage 5+bonus_melee_damage
        blocked_damage 5+bonus_melee_damage
    }
}
```

---

### `Prance`
**Name:** Prance  
**Description:** Refresh your movement action.  
**Source:** `druid_abilities.gon`  

```
Prance { //bonus ability for Elk Form
    template self_buff
    
    meta {
        name "ABILITY_PRANCE_NAME"
        desc "ABILITY_PRANCE_DESC"
        class Druid
        type_icon "movement"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
    }

    damage_instance {
        effects {
            RefreshMovePoints 1
        }
    }
}
```

---

### `Prance2`
**Description:** Refresh your movement action.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
Prance2 { 
    variant_of Prance 

    meta {
        desc "ABILITY_PRANCE2_DESC"
    }

    cost {
        mana 2
    }
}
```

---

### `MockingbirdForm`
**Name:** Form of the Mockingbird  
**Description:** Enter Mockingbird Form, gaining flying movement, +2 [img:lck], and -2 [img:str].
Your basic attack becomes Mock Song and this becomes Tease.  
**Source:** `druid_abilities.gon`  

```
MockingbirdForm {
    template self_buff
    
    meta {
        name "ABILITY_MOCKINGBIRDFORM_NAME"
        desc "ABILITY_MOCKINGBIRDFORM_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack MockSong
            TransformAbility Tease

            LuckUp 2
            StrengthUp -2

            ApplyPassives {
                Flying 1
            }

            CatPartsTransform {
                tail 337
                mouth 320
                arm1 339
                arm2 339
                ear1 1005
                ear2 1005
            }
        }
    }
}
```

---

### `MockingbirdForm2`
**Name:** Form of the Mockingbird  
**Description:** Enter Mockingbird Form, gaining flying movement and +2 [img:lck].
Your basic attack becomes Mock Song+ and this becomes Tease+.  
**Source:** `druid_abilities.gon`  

```
MockingbirdForm2 {
    template self_buff
    
    meta {
        name "ABILITY_MOCKINGBIRDFORM_NAME"
        desc "ABILITY_MOCKINGBIRDFORM2_DESC"
        class Druid
        type_icon "buff"
    }

    tags [shapeshift]

    graphics {
        animation druidTransform
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicAttack MockSong2
            TransformAbility Tease2

            LuckUp 2

            ApplyPassives {
                Flying 1
            }

            CatPartsTransform {
                tail 337
                mouth 320
                arm1 339
                arm2 339
                ear1 1005
                ear2 1005
            }
        }
    }
}
```

---

### `MockSong`
**Name:** Mock Song  
**Description:** Give each unit within an area All Stats Down 2 until the end of their next turn.  
**Source:** `druid_abilities.gon`  

```
MockSong { //basic attack for mockingbird form
    template spell
    
    meta {
        name "ABILITY_MOCKSONG_NAME"
        desc "ABILITY_MOCKSONG_DESC"
        animate_name false
        class Druid
    }
    tags [musical]

    graphics {
        animation sing3//howl
		affected_particle fx_statdown
    }

    target { 
        max_aoe 2
        max_range 5+bonus_range
    }

    damage_instance {
        damage 0
        cant_miss true

        effects {
            Temporary {
                status AllStatsUp
                stacks -2
                turns 1
                expires_on_end_turn true
            }
        }
    }
}
```

---

### `MockSong2`
**Name:** Mock Song  
**Description:** Give enemies within an area All Stats Down 2 (and allies All Stats Up 2) until the the end of their next turn.  
**Source:** `druid_abilities.gon`  

```
MockSong2 { //basic attack for mockingbird form
    template spell
    
    meta {
        name "ABILITY_MOCKSONG_NAME"
        desc "ABILITY_MOCKSONG2_DESC"
        animate_name false
        class Druid
    }
    tags [musical]

    graphics {
        animation sing3
		particle none//needs visual for enemies and allys
    }

    target { 
        max_aoe 2
        max_range 5+bonus_range
    }

    damage_instance {
        damage 0
        cant_miss true

        effects {
            Conditional_Ally {
                Temporary {
                    status AllStatsUp
                    stacks 2
                    turns 1
                    expires_on_end_turn true
                }
            } Else {
                Temporary {
                    status AllStatsUp
                    stacks -2
                    turns 1
                    expires_on_end_turn true
                }
            }
        }
    }
}
```

---

### `Tease`
**Name:** Tease  
**Description:** Inflict Madness 1 on a unit.  
**Source:** `druid_abilities.gon`  

```
Tease { //special ability for mockingbird form
    template targeted_status
    
    meta {
        name "ABILITY_TEASE_NAME"
        desc "ABILITY_TEASE_DESC"
        class Druid
    }

    tags [musical]

    graphics {
        animation howl
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 1
        max_range 5
        max_aoe 0
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

### `Tease2`
**Description:** Inflict Madness 1 on a unit. It immediately attacks a unit if it can.  
**Source:** `druid_abilities.gon`  

```
Tease2 {
    variant_of Tease

    meta {
        desc "ABILITY_TEASE2_DESC"
    }

    damage_instance {
        effects {
            ForceAttack 1
        }
    }
}
```

---

### `FromTheTrees`
**Name:** From the Trees!  
**Description:** Summon a random animal that falls from the sky onto a random enemy, dealing damage.  
**Source:** `druid_abilities.gon`  

```
FromTheTrees {
    template spawn

    meta {
        name "ABILITY_FROMTHETREES_NAME"
        desc "ABILITY_FROMTHETREES_DESC"
        class Druid
    }

    tags [summon]
    
    graphics {
        fall_from_sky true
        bounce_on_hit true
        animation howl
        dont_orient true
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        target_mode random_tile
        min_range 1
        max_range 20
        max_aoe 0

        range_excludes_blocking false
        restrictions [aoe_must_exist must_have_enemy]
        aoe_restrictions none

        knockback_mode zero
    }

    spawn {
        object [Squirrel Turtle Snake Toad Catepillar Crow]
    }

    damage_instance {
        damage 5
    }
}
```

---

### `FromTheTrees2`
**Description:** Summon a random animal that falls from the sky onto a random enemy, dealing more damage.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `druid_abilities.gon`  

```
FromTheTrees2 {
    variant_of FromTheTrees

    meta {
        desc "ABILITY_FROMTHETREES2_DESC"
    }

    cost {
        mana 6
    }
    damage_instance {
        damage 7
    }
}
```

---

## File: `fighter_abilities.gon`

### `Dash`
**Name:** Bull Rush  
**Description:** Dash forward and attack with knockback.  
**Source:** `fighter_abilities.gon`  

```
Dash {
    template dash_attack
    
    meta {
        name "ABILITY_BULLRUSH_NAME"
        desc "ABILITY_BULLRUSH_DESC"
        class Fighter
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }

    sounds { 
        ontrigger SE_BullRushDash 
    } 
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {

    }
    
    damage_instance {
        damage 3+bonus_melee_ability_damage
        knockback 1
    }
}
```

---

### `Dash2`
**Description:** Dash forward and attack with knockback. Repeat this if you hit something.  
**Source:** `fighter_abilities.gon`  

```
Dash2 {
    variant_of Dash

    meta {
        desc "ABILITY_BULLRUSH2_DESC"
    }

    

    temporary_effects {
        DashFury 4
    }
}
```

---

### `Spin`
**Name:** Spin  
**Description:** Attack everything around you 3 times.  
**Source:** `fighter_abilities.gon`  

```
Spin {
    class MultiHitMeleeAttackAbility
    template melee_attack
    
    meta {
        name "ABILITY_SPIN_NAME"
        desc "ABILITY_SPIN_DESC"
        class Fighter
    }

    graphics {
        start spinattackstart
        loop spinattackloop
        end spinattackend
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        target_mode none
        aoe_mode cross
        knockback_mode character_to_tile
        multihit 3
    }
    
    damage_instance {
        damage 1+bonus_melee_ability_damage
    }
}
```

---

### `Spin2`
**Description:** Attack everything around you in a wide area 3 times.  
**Source:** `fighter_abilities.gon`  

```
Spin2 {
    variant_of Spin

    meta {
        desc "ABILITY_SPIN2_DESC"
    }

    target {
        aoe_mode square
    }
}
```

---

### `FirePunch`
**Name:** Fire Punch  
**Description:** A melee attack that inflicts Burn 3.  
**Source:** `fighter_abilities.gon`  

```
FirePunch {
    template melee_attack
    
    meta {
        name "ABILITY_FIREPUNCH_NAME"
        desc "ABILITY_FIREPUNCH_DESC"
        class Fighter
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 7
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        type melee

        effects {
            Burn 3
			VisualFXTile FireBlastSmall
        }

        elements [
            Fire
        ]
    }
}
```

---

### `FirePunch2`
**Description:** A melee attack that inflicts more Burn the more [img:str] you have.  
**Source:** `fighter_abilities.gon`  

```
FirePunch2 {
    variant_of FirePunch

    meta {
        desc "ABILITY_FIREPUNCH2_DESC"
    }

    damage_instance {
        effects {
            Burn 3+bonus_melee_ability_damage
        }
    }
}
```

---

### `IcePunch`
**Name:** Ice Punch  
**Description:** A melee attack that inflicts Freeze.  
**Source:** `fighter_abilities.gon`  

```
IcePunch {
    template melee_attack
    
    meta {
        name "ABILITY_ICEPUNCH_NAME"
        desc "ABILITY_ICEPUNCH_DESC"
        class Fighter
    }

    graphics {
		particle IcePoof
    }

    cost {
        infcantrip true
        mana 7
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        type melee

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

### `IcePunch2`
**Description:** A much stronger melee attack that inflicts Freeze.  
**Source:** `fighter_abilities.gon`  

```
IcePunch2 {
    variant_of IcePunch

    meta {
        desc "ABILITY_ICEPUNCH2_DESC"
    }

    damage_instance {
        damage 10+bonus_melee_ability_damage
    }
}
```

---

### `ThunderPunch`
**Name:** Thunder Punch  
**Description:** A melee attack that has a 25% chance to inflict Stun.  
**Source:** `fighter_abilities.gon`  

```
ThunderPunch {
    template melee_attack
    
    meta {
        name "ABILITY_THUNDERPUNCH_NAME"
        desc "ABILITY_THUNDERPUNCH_DESC"
        class Fighter
    }

    graphics {
		animation angryfail
    }

    cost {
        infcantrip true
        mana 7
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        type melee

        effects {
            Stun [1, .25]
			VisualFXTile WaterConduct
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `ThunderPunch2`
**Description:** A melee attack that inflicts Stun.  
**Source:** `fighter_abilities.gon`  

```
ThunderPunch2 {
    variant_of ThunderPunch

    meta {
        desc "ABILITY_THUNDERPUNCH2_DESC"
    }

    damage_instance {
        effects {
            Stun 1
        }
    }
}
```

---

### `FurySwipes`
**Name:** Fury Swipes  
**Description:** A weak melee attack that has a chance to hit multiple times.  
**Source:** `fighter_abilities.gon`  

```
FurySwipes {
    template melee_attack
    
    meta {
        name "ABILITY_FURYSWIPES_NAME"
        desc "ABILITY_FURYSWIPES_DESC"
        class Fighter
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 6
    }

    temporary_effects {
        Fury 75
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage
        type melee
    }
}
```

---

### `FurySwipes2`
**Description:** A melee attack that has a chance to hit multiple times.  
**Source:** `fighter_abilities.gon`  

```
FurySwipes2 {
    variant_of FurySwipes

    meta {
        desc "ABILITY_FURYSWIPES2_DESC"
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        type melee
    }
}
```

---

### `SideSlash`
**Name:** Side Slash  
**Description:** An attack that hits a half circle around you.  
**Source:** `fighter_abilities.gon`  

```
SideSlash {
    template melee_attack
    
    meta {
        name "ABILITY_SIDESLASH_NAME"
        desc "ABILITY_SIDESLASH_DESC"
        class Fighter
    }

    graphics {
		animation quarterswipe
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        aoe_mode custom
        custom_aoe [ [1, 0], [0, -1], [0, 1], [1, 1], [1, -1] ]

        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage
    }
}
```

---

### `SideSlash2`
**Description:** An attack that hits a half circle around you and inflicts Bruise.  
**Source:** `fighter_abilities.gon`  

```
SideSlash2 {
    variant_of SideSlash

    meta {
        desc "ABILITY_SIDESLASH2_DESC"
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        effects {
            Bruise 2
        }
    }
}
```

---

### `FighterLeap`
**Name:** Leap  
**Description:** Jump to an open tile within range, then inflict Bruise on all adjacent units.  
**Source:** `fighter_abilities.gon`  

```
FighterLeap {
    template jump_attack

    meta {
        name "ABILITY_LEAP_NAME"
        desc "ABILITY_LEAP_DESC"
        class Fighter
        type_icon "movement"
    }

    graphics {
        jump_attack_animation land
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        max_range 4
    }

    temporary_effects {
        JustInCaseTrample 0
    }

    damage_instance {
        damage 0
        makes_contact false

        effects {
            Bruise 1
        }
    }
}
```

---

### `FighterLeap2`
**Description:** Jump to an open tile within range, then damage and inflict Bruise on all adjacent units.  
**Source:** `fighter_abilities.gon`  

```
FighterLeap2 {
    variant_of FighterLeap

    meta {
        desc "ABILITY_LEAP2_DESC"
        type_icon "attack"
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        makes_contact true
    }
}
```

---

### `Uppercut`
**Name:** Uppercut  
**Description:** Punch a unit into the air, lobbing it back 3 tiles.  
**Source:** `fighter_abilities.gon`  

```
Uppercut {
    template melee_attack
    
    meta {
        name "ABILITY_UPPERCUT_NAME"
        desc "ABILITY_UPPERCUT_DESC"
        class Fighter
    }

    graphics {
        animation uppercutatk
    }

    cost {
        infcantrip true
        mana 7
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        type melee

        effects {
            KnockUpAndAway {
                stacks 5+bonus_melee_ability_damage
                distance 3
            }
        }
    }
}
```

---

### `Uppercut2`
**Description:** Punch a unit into the air, lobbing it back 3 tiles.
Refresh your movement action.  
**Source:** `fighter_abilities.gon`  

```
Uppercut2 {
    variant_of Uppercut

    meta {
        desc "ABILITY_UPPERCUT2_DESC"
    }

    damage_instance {
        effects {
            RefreshMovePointsIfHit 1
        }
    }
}
```

---

### `Counter`
**Name:** Counter  
**Description:** Counterattack all attacks until your next turn.  
**Source:** `fighter_abilities.gon`  

```
Counter {
    template self_buff
    
    meta {
        name "ABILITY_COUNTER_NAME"
        desc "ABILITY_COUNTER_DESC"
        class Fighter
        type_icon "defense"
    }

    graphics {
		animation bruise
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            TempCounterAttack 1
        }
    }
}
```

---

### `Counter2`
**Name:** Counter  
**Description:** Preemptively counterattack all attacks until your next turn.  
**Source:** `fighter_abilities.gon`  

```
Counter2 {
    template self_buff
    
    meta {
        name "ABILITY_COUNTER_NAME"
        desc "ABILITY_COUNTER2_DESC"
        class Fighter
        type_icon "defense"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            TempPreEmptiveCounterAttack 1
        }
    }
}
```

---

### `TailWhip`
**Name:** Tail Whip  
**Description:** An attack that hits 2 tiles in front of and behind you.  
**Source:** `fighter_abilities.gon`  

```
TailWhip {
    template melee_attack
    
    meta {
        name "ABILITY_TAILWHIP_NAME"
        desc "ABILITY_TAILWHIP_DESC"
        class Fighter
    }

    graphics {
        animation tailwhip
    }

    target {
        aoe_mode custom
        custom_aoe [[1, 0] [2, 0], [-1, 0], [-2, 0]]
        max_aoe 2
    }

    cost {
        infcantrip true
        mana 6
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        type melee
    }
}
```

---

### `TailWhip2`
**Description:** An attack that hits 4 tiles in front of and behind you.  
**Source:** `fighter_abilities.gon`  

```
TailWhip2 {
    variant_of TailWhip

    meta {
        desc "ABILITY_TAILWHIP2_DESC"
    }

    target {
        aoe_mode custom
        custom_aoe [[1, 0] [2, 0] [3, 0] [4, 0] [-1, 0] [-2, 0] [-3, 0] [-4, 0]]
    }
}
```

---

### `Poke`
**Name:** Poke  
**Description:** A melee attack that deals 1 damage.  
**Source:** `fighter_abilities.gon`  

```
Poke {
    template melee_attack
    
    meta {
        name "ABILITY_POKE_NAME"
        desc "ABILITY_POKE_DESC"
        class Fighter
    }

    graphics {
        animation tinyPunch
    }

    cost {
        infcantrip true
        mana 2
    }

    damage_instance {
        damage 1
        type melee
    }
}
```

---

### `Poke2`
**Description:** A melee attack that deals 1 damage.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
Poke2 {
    variant_of Poke

    meta {
        desc "ABILITY_POKE2_DESC"
    }

    cost {
        infcantrip true
        mana 1
    }
}
```

---

### `Nip`
**Name:** Nip  
**Description:** Inflict Bruise on a unit.  
**Source:** `fighter_abilities.gon`  

```
Nip {
    template melee_attack
    
    meta {
        name "ABILITY_NIP_NAME"
        desc "ABILITY_NIP_DESC"
        class Fighter
        type_icon "debuff"
    }

    graphics {
		animation dashbite
    }

    cost {
        infcantrip true
        mana 2
    }

    damage_instance {
        damage 0
        type melee

        effects {
            Bruise 1
        }
    }
}
```

---

### `Nip2`
**Description:** Deal 1 damage and inflict Bruise on a unit.  
**Source:** `fighter_abilities.gon`  

```
Nip2 {
    variant_of Nip

    meta {
        desc "ABILITY_NIP2_DESC"
    }

    damage_instance {
        damage 1
    }
}
```

---

### `Push`
**Name:** Push  
**Description:** Knockback a unit 2 tiles.  
**Source:** `fighter_abilities.gon`  

```
Push {
    template melee_attack
    
    meta {
        name "ABILITY_PUSH_NAME"
        desc "ABILITY_PUSH_DESC"
        class Fighter
        type_icon "melee"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 2
    }

    damage_instance {
        damage 0
        type melee
        knockback 2
    }
}
```

---

### `Push2`
**Description:** Turn an adjacent unit around and knock it back 2 tiles.  
**Source:** `fighter_abilities.gon`  

```
Push2 {
    variant_of Push

    meta {
        desc "ABILITY_PUSH2_DESC"
    }

    damage_instance {
        effects {
            FaceAway 1
        }
    }
}
```

---

### `FalconPunch`
**Name:** Falcon Punch  
**Description:** Charge up a mega punch.
\[s:.7\](This punch will be unleashed on your next turn.)\[/s\]
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
FalconPunch {
    template melee_attack
    
    meta {
        name "ABILITY_FALCONPUNCH_NAME"
        desc "ABILITY_FALCONPUNCH_DESC"
        class Fighter
    }

    graphics {
        animation falconPunch
    }

    cost {
        cantrip true
        mana 2
    }

    target {
        delayed_trigger true
    }

    damage_instance {
        damage 25+bonus_melee_ability_damage
        knockback 10
    }
}
```

---

### `FalconPunch2`
**Name:** Falcon Punch  
**Description:** Charge up a mega dash attack.
\[s:.7\](This punch will be unleashed on your next turn.)\[/s\]
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
FalconPunch2 {
    template dash_attack
    
    meta {
        name "ABILITY_FALCONPUNCH_NAME"
        desc "ABILITY_FALCONPUNCH2_DESC"
        class Fighter
    }

    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }

    cost {
        cantrip true
        mana 2
    }

    target {
        max_range 4
        delayed_trigger true
    }

    damage_instance {
        damage 25+bonus_melee_ability_damage
        knockback 10
    }
}
```

---

### `Exert`
**Name:** Exert  
**Description:** Refresh your basic attack and movement action.
Fall asleep at the end of the turn.  
**Source:** `fighter_abilities.gon`  

```
Exert {
    template self_buff
    
    meta {
        name "ABILITY_EXERT_NAME"
        desc "ABILITY_EXERT_DESC"
        class Fighter
        type_icon "misc"
    }

    graphics {
        animation jitter
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    damage_instance {
        effects {
            Drowsy 1
            RefreshMovePoints 1
            RefreshActPoints 1
        }
    }
}
```

---

### `Exert2`
**Name:** Exert  
**Description:** Refresh your basic attack and movement action.
Gain +2 [img:str] and +4 [img:spd] until end of turn.
Fall asleep at the end of the turn.  
**Source:** `fighter_abilities.gon`  

```
Exert2 {
    template self_buff

    meta {
        name "ABILITY_EXERT_NAME"
        desc "ABILITY_EXERT2_DESC"
        class Fighter
    }

    cost {
        infcantrip true
        mana 6
    }

    damage_instance {
        effects {
            Drowsy 1
            RefreshMovePoints 1
            RefreshActPoints 1
            Temporary {
                status StrengthUp
                stacks 2
                turns 1
            }
            Temporary {
                status SpeedUp
                stacks 4
                turns 1
            }
        }
    }
}
```

---

### `Enrage`
**Name:** Enrage  
**Description:** Give a unit +4 [img:str] and Confusion 2.  
**Source:** `fighter_abilities.gon`  

```
Enrage {
    template targeted_status

    meta {
        name "ABILITY_ENRAGE_NAME"
        desc "ABILITY_ENRAGE_DESC"
        class Fighter
    }

    graphics {
        particle fx_statup
		animation pointout
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        max_aoe 0
        min_range 0
        max_range 3
    }
    
    damage_instance {
        damage 0
        
        effects {
            StrengthUp 4
            Confusion 2
        }
    }
}
```

---

### `Enrage2`
**Description:** Give a unit on any tile +4 [img:str] and Confusion 2.  
**Source:** `fighter_abilities.gon`  

```
Enrage2 {
    variant_of Enrage

    meta {
        desc "ABILITY_ENRAGE2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `Tumble`
**Name:** Tumble  
**Description:** Move one tile diagonally.  
**Source:** `fighter_abilities.gon`  

```
Tumble {
    template move
    
    meta {
        name "ABILITY_TUMBLE_NAME"
        desc "ABILITY_TUMBLE_DESC"
        class Fighter
        animate_name true
    }

    graphics {
        sync_speed 22
        max_tiles_single_loop 5
        ignore_slowtiles true
        move_start_animation startroll
        animation roll
        move_end_animation endroll
    }

    cost {
        infcantrip true
        mana 2
    }

    target {
        range_mode diagcross
        max_range level
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_diagonals true
    }
}
```

---

### `Tumble2`
**Description:** Move two tiles diagonally.  
**Source:** `fighter_abilities.gon`  

```
Tumble2 {
    variant_of Tumble

    meta {
        desc "ABILITY_TUMBLE2_DESC"
    }
}
```

---

### `Confront`
**Name:** Confront  
**Description:** Move in front of an enemy.  
**Source:** `fighter_abilities.gon`  

```
Confront {
    template move
    
    meta {
        name "ABILITY_CONFRONT_NAME"
        desc "ABILITY_CONFRONT_DESC"
        animate_name true
        class Fighter
    }

    graphics {

    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        max_range 100

        restrictions [must_be_moveable must_be_directly_in_front_of_enemy must_move]
    }
}
```

---

### `Confront2`
**Description:** Move in front of an enemy.
Your next action has +30% critical chance.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
Confront2 {
    variant_of Confront

    meta {
        desc "ABILITY_CONFRONT2_DESC"
    }

    cost {
        mana 5
    }

    self_damage {
        effects {
            TempCritChanceUp 30
        }
    }
}
```

---

### `Juiced`
**Name:** Juiced  
**Description:** Your movement range is doubled until the end of the turn.  
**Source:** `fighter_abilities.gon`  

```
Juiced {
    template self_buff
    
    meta {
        name "ABILITY_JUICED_NAME"
        desc "ABILITY_JUICED_DESC"
        class Fighter
        type_icon "movement"
    }

    graphics {
		animation runincircles
		particle fx_statup
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            TempMovement mov
        }
    }
}
```

---

### `Juiced2`
**Description:** Your movement range is doubled and you get +4 [img:str] until the end of the turn.  
**Source:** `fighter_abilities.gon`  

```
Juiced2 {
    variant_of Juiced

    meta {
        desc "ABILITY_JUICED2_DESC"
    }

    damage_instance {
        effects {
            Temporary {
                status StrengthUp
                stacks 4
                turns 1
            }
        }
    }
}
```

---

### `CosmicPunch`
**Name:** Cosmic Punch  
**Description:** Punch a unit into SPACE!
[s:.7]They will fall back down at the end of the round.\[/s\]  
**Source:** `fighter_abilities.gon`  

```
CosmicPunch {
    template melee_attack
    
    meta {
        name "ABILITY_COSMICPUNCH_NAME"
        desc "ABILITY_COSMICPUNCH_DESC"
        class Fighter
        type_icon "melee"

        icon_shell_frame attack
        icon_damage_display_eq "10+bonus_melee_ability_damage"
    }

    graphics {
        animation uppercutatk
        darken_screen true
        darken_screen_exclude_characters_on_tile true
        darken_screen_exclude_self true
        darken_screen_start_early true
    }

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        damage 0
        type melee

        effects {
            Conditional_Displaceable {
                LaunchOffScreen 10+bonus_melee_ability_damage
                TempInitiativeChange -100
            } Else {
                BonusDamage 1
            }
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `CosmicPunch2`
**Description:** Punch a unit into SPACE!
[s:.7]They will fall back down at the end of the round.
(This spell costs less.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
CosmicPunch2 {
    variant_of CosmicPunch

    meta {
        desc "ABILITY_COSMICPUNCH2_DESC"
    }

    cost {
        mana 1
    }
}
```

---

### `FighterTaunt`
**Name:** Taunt!  
**Description:** All enemies within 3 tiles move toward you.  
**Source:** `fighter_abilities.gon`  

```
FighterTaunt {
    template spell
    
    meta {
        name "ABILITY_TAUNT_NAME"
        desc "ABILITY_TAUNT_DESC"
        class Fighter
    }

    graphics {
	    animation tauntwiggle
	    particle none
    }

    cost {
        mana 4
        infcantrip true
    }

    target {
        target_mode none
        
        max_aoe 3
        min_aoe 1
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Conditional_Enemy {
                ForceMoveTowards 1
            }
        }
    }
}
```

---

### `FighterTaunt2`
**Description:** All enemies within 5 tiles move toward you.  
**Source:** `fighter_abilities.gon`  

```
FighterTaunt2 {
    variant_of FighterTaunt

    meta {
        desc "ABILITY_TAUNT2_DESC"
    }

    target {
        max_aoe 5
    }

    cost {
        mana 3
    }
}
```

---

### `GravitySlam`
**Name:** Gravity Slam  
**Description:** Jump to a tile and pull enemies toward you when you land.  
**Source:** `fighter_abilities.gon`  

```
GravitySlam {
    template jump_attack

    meta {
        name "ABILITY_GRAVITYSLAM_NAME"
        desc "ABILITY_GRAVITYSLAM_DESC"
        class Fighter
        type_icon "movement"
    }

    graphics {
        jump_start_animation gravitySlamStart
        air_animation gravitySlam_air
        jump_attack_animation gravitySlamEnd
        land_animation none

        apex_distance 0.875
        apex_time .35
        hang_time .6
        fixed_jump_height 3.5
        fixed_jump_speed 1
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        max_range 4
        max_aoe 4
        aoe_mode standard
        distance_sort_targets 1
    }

    temporary_effects {
        JustInCaseTrample 0
    }

    self_damage {
        effects {
            DoScreenShake 1
            DoDistortionRing {
                speed -30
                intensity -1
                radius 4
            }
        }
    }

    damage_instance {
        damage 0
        makes_contact false
        type spell
        effects {
            Conditional_Enemy {
                DisplaceToAbilityTarget 1
            }
        }
        elements [
            Gravity
        ]
    }
}
```

---

### `GravitySlam2`
**Description:** Jump to a tile and pull enemies toward you when you land.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
GravitySlam2 {
    variant_of GravitySlam

    meta {
        desc "ABILITY_GRAVITYSLAM2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `Berserk`
**Name:** Berserk  
**Description:** Gain +5 [img:str] and Bruise 5. This ability becomes Berserker Dash.  
**Source:** `fighter_abilities.gon`  

```
Berserk {
    template self_buff
    
    meta {
        name "ABILITY_BERSERK_NAME"
        desc "ABILITY_BERSERK_DESC"
        class Fighter
        type_icon "misc"
    }

    graphics {
        animation angry
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            StrengthUp 5
            Bruise 5
            TransformAbility BerserkDash
            AlternateIdleAnimation berserkIdle
            SetDefaultFace insane
        }
    }
}
```

---

### `Berserk2`
**Description:** Gain +7 [img:str] and Bruise 3. This ability becomes Berserker Dash+.  
**Source:** `fighter_abilities.gon`  

```
Berserk2 {
    variant_of Berserk

    meta {
        desc "ABILITY_BERSERK2_DESC"
    }

    damage_instance {
        effects {
            StrengthUp 7
            Bruise 3
            TransformAbility BerserkDash2
        }
    }
}
```

---

### `BerserkDash`
**Name:** Berserker Dash  
**Description:** A short range dash attack.  
**Source:** `fighter_abilities.gon`  

```
BerserkDash { //util ability for Bezerk
    template dash_attack
    
    meta {
        name "ABILITY_BERSERKERDASH_NAME"
        desc "ABILITY_BERSERKERDASH_DESC"
        class Fighter
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    target {
        max_range 2
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage
    }
}
```

---

### `BerserkDash2`
**Description:** A dash attack with infinite range.  
**Source:** `fighter_abilities.gon`  

```
BerserkDash2 { 
    variant_of BerserkDash

    meta {
        desc "ABILITY_BERSERKERDASH2_DESC"
    }
    target {
        max_range 10
    }
}
```

---

### `Challenge`
**Name:** Mock  
**Description:** Force a unit to move towards you.
RELOAD: Kill something.  
**Source:** `fighter_abilities.gon`  

```
Challenge {
    template spell

    meta {
        name "ABILITY_MOCK_NAME"
        desc "ABILITY_MOCK_DESC"
        class Fighter
        type_icon "misc"
    }
    graphics {
        animation howl
		particle none
    }
    
    cost {
        mana 0
        requires_reload true
    }

    bonus_passives {
        ReloadOnKill 1
    }
    
    target {
        min_range 1
        max_range 4
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

### `Challenge2`
**Description:** Force a unit to move towards you.
RELOAD: Kill something.
Bonus Ability: Slap.  
**Source:** `fighter_abilities.gon`  

```
Challenge2 {
    variant_of Challenge

    meta {
        desc "ABILITY_MOCK2_DESC"
    }

    bonus_passives {
        BonusAbility_DelayedApplication Slap
    }
}
```

---

### `Slap`
**Name:** Slap  
**Description:** A weak melee attack.
RELOAD: Kill something.  
**Source:** `fighter_abilities.gon`  

```
Slap { //util ability for Challenge
    template melee_attack
    
    meta {
        name "ABILITY_SLAP_NAME"
        desc "ABILITY_SLAP_DESC"
        class Fighter
    }

    graphics {
    }

    cost {
        requires_reload true
        mana 0
    }

    bonus_passives {
        ReloadOnKill 1
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage
    }
}
```

---

### `Stoopzerk`
**Name:** Stoopzerk  
**Description:** Your [img:int] becomes 0. You can attack an extra time each turn for the rest of the battle.
This ability becomes MORE ANGRIER!!!  
**Source:** `fighter_abilities.gon`  

```
Stoopzerk {
    template self_buff
    
    meta {
        name "ABILITY_STOOPZERK_NAME"
        desc "ABILITY_STOOPZERK_DESC"
        class Fighter
        type_icon "misc"
    }

    graphics {
        animation angry
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            ExtraBasicAttacks_Status 1
            IntelligenceUp "min(-int, 0)"
            TransformAbility LastThought
        }
    }
}
```

---

### `Stoopzerk2`
**Description:** Your [img:int] becomes 0. You can attack an extra time each turn for the rest of the battle.
This ability becomes MORE ANGRIER!!!+  
**Source:** `fighter_abilities.gon`  

```
Stoopzerk2 {
    variant_of Stoopzerk

    meta {
        desc "ABILITY_STOOPZERK2_DESC"
    }

    cost {
        mana 4
    }

    damage_instance {
        effects {
            StrengthUp "max(int, 0)"
            TransformAbility LastThought2
        }
    }
}
```

---

### `LastThought`
**Name:** MORE ANGRIER!!!  
**Description:** Lose all of your mana and gain that much [img:str] until the end of the turn.  
**Source:** `fighter_abilities.gon`  

```
LastThought {
    template self_buff
    
    meta {
        name "ABILITY_MOREANGRIER_NAME"
        desc "ABILITY_MOREANGRIER_DESC"
        class Fighter
        type_icon "misc"
    }

    graphics {
		animation angry
		particle fx_statup
    }
    
    cost {
        mana X
        infcantrip true
        X_cant_be_zero true
        disallow_cost_modification true
    }

    target {
        X_is current_mana
    }
    
    damage_instance {
        effects {
            TempStrengthUp X
        }
    }
}
```

---

### `LastThought2`
**Description:** Lose all of your mana and gain that much [img:str], [img:dex], and [img:spd] until the end of the turn.  
**Source:** `fighter_abilities.gon`  

```
LastThought2 {
    variant_of LastThought
    
    meta {
        desc "ABILITY_MOREANGRIER2_DESC"
    }

    damage_instance {
        effects {
            TempStrengthUp X
            TempDexterityUp X
            TempSpeedUp X
        }
    }
}
```

---

### `SleeperHold`
**Name:** Sleeper Hold  
**Description:** Inflict Sleep on an adjacent unit.  
**Source:** `fighter_abilities.gon`  

```
SleeperHold {
    template melee_attack
    
    meta {
        name "ABILITY_SLEEPERHOLD_NAME"
        desc "ABILITY_SLEEPERHOLD_DESC"
        class Fighter
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        damage 0
        type melee
        effects {
            Sleep 1
        }
    }
}
```

---

### `SleeperHold2`
**Description:** Inflict Sleep and Bruise on an adjacent unit.  
**Source:** `fighter_abilities.gon`  

```
SleeperHold2 {
    variant_of SleeperHold

    meta {
        desc "ABILITY_SLEEPERHOLD2_DESC"
    }

    cost {
        infcantrip true
        mana 4
    }

    damage_instance {
        effects {
            Sleep 1
            Bruise 1
        }
    }
}
```

---

### `Grapple`
**Name:** Grapple  
**Description:** Immobilize an adjacent unit for as long as you remain adjacent.  
**Source:** `fighter_abilities.gon`  

```
Grapple {
    template tile_targeted_melee_attack
    class PlaceholderMeleeAttackAbility
    
    meta {
        name "ABILITY_GRAPPLE_NAME"
        desc "ABILITY_GRAPPLE_DESC"
        class Fighter
    }

    graphics {
        animation bearHug
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        knockback_mode tile_to_character
    }

    damage_instance {
        damage 0
        type melee
        effects {
            Grappled 1
        }
    }
}
```

---

### `Grapple2`
**Description:** Immobilize an adjacent unit for as long as you remain adjacent.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
Grapple2 {
    variant_of Grapple

    meta {
        desc "ABILITY_GRAPPLE2_DESC"
    }

    cost {
        mana 2
    }
}
```

---

### `ThinkTooHard`
**Name:** Think Too Hard  
**Description:** Take damage equal to your [img:int].
The next spell you cast this turn is free.  
**Source:** `fighter_abilities.gon`  

```
ThinkTooHard {
    template self_buff
    
    meta {
        name "ABILITY_THINKTOOHARD_NAME"
        desc "ABILITY_THINKTOOHARD_DESC"
        class Fighter
        type_icon "misc"
    }

    graphics {
        animation thinking
    }
    
    cost {
        mana 2
        infcantrip true
        manacost_cant_be_zero true
    }

    damage_instance {
        raw_damage int

        effects {
            FreeSpell 1
        }
    }
}
```

---

### `ThinkTooHard2`
**Description:** Take damage equal to your [img:int], then your [img:int] becomes 0.
The next spell you cast this turn is free.  
**Source:** `fighter_abilities.gon`  

```
ThinkTooHard2 {
    variant_of ThinkTooHard
    
    meta { 
        desc "ABILITY_THINKTOOHARD2_DESC"
    }

    damage_instance {
        effects {
            IntelligenceUp "min(-int, 0)"
        }
    }
}
```

---

### `Zoomzerk`
**Name:** Zoomzerk  
**Description:** Your movement action becomes a dash attack.
This ability becomes Reposition.  
**Source:** `fighter_abilities.gon`  

```
Zoomzerk {
    template self_buff
    
    meta {
        name "ABILITY_ZOOMZERK_NAME"
        desc "ABILITY_ZOOMZERK_DESC"
        class Fighter
        type_icon "misc"
    }

    graphics {
        animation angry
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformBasicMove BasicDashAttackMove_NoKnockback
            TransformAbility Reposition
        }
    }
}
```

---

### `Zoomzerk2`
**Description:** Your movement action becomes a dash attack. Restore all your mana.
This ability becomes Reposition+.  
**Source:** `fighter_abilities.gon`  

```
Zoomzerk2 {
    variant_of Zoomzerk

    meta {
        desc "ABILITY_ZOOMZERK2_DESC"
    }

    damage_instance {
        effects {
            FillMana 1
            TransformAbility Reposition2
        }
    }
}
```

---

### `Reposition`
**Name:** Reposition  
**Description:** Move up to two tiles.  
**Source:** `fighter_abilities.gon`  

```
Reposition {
    template move
    
    meta {
        name "ABILITY_REPOSITION_NAME"
        desc "ABILITY_REPOSITION_DESC"
        animate_name true
        class Fighter
    }
    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 2
    }
}
```

---

### `Reposition2`
**Description:** Move up to two tiles.  
**Source:** `fighter_abilities.gon`  

```
Reposition2 {
    variant_of Reposition
    
    meta {
        desc "ABILITY_REPOSITION2_DESC"
    }
    cost {
        infcantrip true
        mana 3
    }
}
```

---

### `FighterBonusThrow`
**Name:** Throw Weapon  
**Description:** Throw your weapon at a unit. The weapon breaks.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
FighterBonusThrow {
    template ranged_attack
    
    meta {
        name "ABILITY_FIGHTERTHROW_NAME"
        desc "ABILITY_FIGHTERTHROW_DESC"
        animate_name false
    }

    tags [weapon_throw]

    graphics {
        animation weaponthrowstraight
    }

    cost {
        requires_destructible_weapon true
        mana 0
        cantrip true
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    bonus_passives {
        AbilityInheritsWeaponEffects 1
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

### `Bloodzerk`
**Name:** Bloodzerk  
**Description:** Drop to 1 HP.
Damage you deal to bleeding units has Lifesteal.
This spell becomes Lacerate.  
**Source:** `fighter_abilities.gon`  

```
Bloodzerk {
    template self_buff
    
    meta {
        name "ABILITY_BLOODZERK_NAME"
        desc "ABILITY_BLOODZERK_DESC"
        class Fighter
        type_icon "misc"
    }

    graphics {
        animation angry
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            SetHealth 1
            Bloodzerked 1
            TransformAbility Lacerate
        }
    }
}
```

---

### `Bloodzerk2`
**Description:** Drop to 1 HP.
Damage you deal to bleeding units has Lifesteal.
This spell becomes Lacerate+.
\[s:.7\](This spell costs 0 mana.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
Bloodzerk2 {
    variant_of Bloodzerk

    meta {
        desc "ABILITY_BLOODZERK2_DESC"
    }

    cost {
        infcantrip true
        mana 0
    }

    damage_instance {
        effects {
            TransformAbility Lacerate2
        }
    }
}
```

---

### `Lacerate`
**Name:** Lacerate  
**Description:** A melee attack that inflicts Bleed 2.  
**Source:** `fighter_abilities.gon`  

```
Lacerate {
    template melee_attack
    
    meta {
        name "ABILITY_LACERATE_NAME"
        desc "ABILITY_LACERATE_DESC"
        class Fighter
    }

    graphics {
        animation sliceOpen
    }

    cost {
        infcantrip true
        mana 4
    }

    damage_instance {
        damage 3+bonus_melee_ability_damage

        effects {
            Bleed 2
        }
    }
}
```

---

### `Lacerate2`
**Description:** A stronger melee attack that inflicts Bleed 2.  
**Source:** `fighter_abilities.gon`  

```
Lacerate2 {
    variant_of Lacerate

    meta {
        desc "ABILITY_LACERATE2_DESC"
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
    }
}
```

---

### `ExhaustingBlow`
**Name:** Exhausting Blow  
**Description:** Dash forward one tile and attack with knockback.
\[s:.7\](This spell's mana cost increases by 2 at the end of each of your turns.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
ExhaustingBlow {
    template dash_attack
    
    meta {
        name "ABILITY_EXHAUSTINGBLOW_NAME"
        desc "ABILITY_EXHAUSTINGBLOW_DESC"
        class Fighter
    }

    graphics {
        dash_start_animation headbuttdashStart
        dash_animation headbuttdash
        dash_attack_animation headbuttdashEnd
    }

    cost {
        mana 2+X*2
        infcantrip true
    }

    target { 
        max_range 1+bonus_range
        max_aoe 1
        aoe_restrictions must_have_line_of_sight_unpurgable

        X_is custom
    }
    bonus_passives {
        XIsIncreaseEachTurn 1
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        knockback 1
    }
}
```

---

### `ExhaustingBlow2`
**Description:** Dash forward any number of tiles and attack with knockback.
\[s:.7\](This spell's mana cost increases by 2 at the end of each of your turns.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
ExhaustingBlow2 {
    variant_of ExhaustingBlow

    meta {
        desc "ABILITY_EXHAUSTINGBLOW2_DESC"
    }

    target { 
        max_range 10
    }
}
```

---

### `ChaosRampage`
**Name:** Chaos Rampage  
**Description:** Take an extra turn. You have Madness 1 and Confusion 1 on that turn.
\[s:.7\](This spell can't be cast on extra turns.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
ChaosRampage {
    template self_buff
    
    meta {
        name "ABILITY_CHAOSRAMPAGE_NAME"
        desc "ABILITY_CHAOSRAMPAGE_DESC"
        class Fighter
        type_icon "misc"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
        main_turn_only true
    }
    
    damage_instance {
        effects {
            TakeBonusTurnWithStatus {
                Madness 1
                Confusion 1
            }
        }
    }
}
```

---

### `ChaosRampage2`
**Name:** Chaos Rampage  
**Description:** Take an extra turn. You have Madness 1 on that turn.
\[s:.7\](This spell can't be cast on extra turns.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
ChaosRampage2 {
    template self_buff
    
    meta {
        name "ABILITY_CHAOSRAMPAGE_NAME"
        desc "ABILITY_CHAOSRAMPAGE2_DESC"
        class Fighter
        type_icon "misc"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
        main_turn_only true
    }
    
    damage_instance {
        effects {
            TakeBonusTurnWithStatus {
                Madness 1
            }
        }
    }
}
```

---

### `MeteorSlam`
**Name:** Meteor Slam  
**Description:** Jump up to 2 tiles.
Damage, knockback, and inflict Burn 3 on the unit you land on and all adjacent units.
\[s:.7\](Adjacent units take half damage.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
MeteorSlam {
    template jump_attack

    meta {
        name "ABILITY_METEORSLAM_NAME"
        desc "ABILITY_METEORSLAM_DESC"
        class Fighter
    }

    graphics {
        aoe_spell_on_land true
        jump_attack_animation land
        do_damage_immediately true
        particle Explosion
        palette 6
        delay 3
        visual_delay_but_simultaneous_damage 0
        jump_height_multiplier 2
    }

    cost {
        infcantrip true
        mana 10
    }
    
    target {
        min_range 1
        max_range 2
        max_aoe 1
        aoe_mode square
        restrictions none
    }

    splash_damage {
        damage "(5+bonus_melee_ability_damage)/2"
        knockback 2
        type spell

        effects {
            Burn 3
            IgnoreSelf 1
        }

        elements [
            Fire
            Explosion
        ]
    }
    damage_instance {
        damage 5+bonus_melee_ability_damage
        knockback 2

        effects {
            Burn 3
            IgnoreSelf 1
        }

        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `MeteorSlam2`
**Description:** Jump up to 5 tiles.
Damage, knockback, and inflict Burn 3 on the unit you land on and all adjacent units.  
**Source:** `fighter_abilities.gon`  

```
MeteorSlam2 {
    variant_of MeteorSlam

    meta {
        desc "ABILITY_METEORSLAM2_DESC"
    }

    target {
        max_range 5
    }

    splash_damage {
        damage 5+bonus_melee_ability_damage
    }
    damage_instance {
        damage 5+bonus_melee_ability_damage
    }
}
```

---

### `MuscleMemory`
**Name:** Muscle Memory  
**Description:** A melee attack that deals 8 damage.
\[s:.7\](This spell's damage is reduced by 1 and mana cost is reduced by 2 each time it's cast.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
MuscleMemory {
    template melee_attack
    
    meta {
        name "ABILITY_MUSCLEMEMORY_NAME"
        desc "ABILITY_MUSCLEMEMORY_DESC"
        class Fighter
    }

    graphics {
	animation heaviestMelee
    }

    target {
        X_is cast_count
    }

    cost {
        infcantrip true
        mana "max(8-2*X,0)"
        damage_cant_be_zero true
    }

    damage_instance {
        raw_damage "8-X"
    }
}
```

---

### `MuscleMemory2`
**Description:** A melee attack that deals 8 damage and inflicts Bruise.
\[s:.7\](This spell's damage is reduced by 1 and mana cost is reduced by 2 each time it's cast.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
MuscleMemory2 {
    variant_of MuscleMemory
    
    meta {
        desc "ABILITY_MUSCLEMEMORY2_DESC"
    }

    cost {
        mana "max(7-2*X,0)"
    }

    damage_instance {
        effects {
            Bruise 1
        }
    }
}
```

---

### `Inhale`
**Name:** Inhale  
**Description:** Suck all units in a straight line 1 tile toward you.  
**Source:** `fighter_abilities.gon`  

```
Inhale {
    template spell
    
    meta {
        name "ABILITY_INHALE_NAME"
        desc "ABILITY_INHALE_DESC"
        class Fighter
    }

    graphics {
        particle fx_windSpell
    }

    cost {
        mana 3
        infcantrip true
    }

    target {
        target_mode direction
        
        aoe_mode line
        min_aoe 1
        max_aoe 10
        
        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode back_orientation
    }

    damage_instance {
        damage 0
        knockback 1

        elements [
            Wind
        ]
    }
}
```

---

### `Inhale2`
**Description:** Suck all units in a straight line 3 tiles toward you.  
**Source:** `fighter_abilities.gon`  

```
Inhale2 {
    variant_of Inhale

    meta {
        desc "ABILITY_INHALE2_DESC"
    }

    damage_instance {
        knockback 3
    }
}
```

---

### `OneTwoPunch`
**Name:** One-Two Punch  
**Description:** A melee attack that hits twice. Each punch inflicts Bruise 1.  
**Source:** `fighter_abilities.gon`  

```
OneTwoPunch {
    template melee_attack
    
    meta {
        name "ABILITY_ONETWOPUNCH_NAME"
        desc "ABILITY_ONETWOPUNCH_DESC"
        class Fighter
    }

    graphics {
        animation bigdoubleswat
    }

    cost {
        infcantrip true
        mana 8
    }

    target {
        multihit 2
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage
        type melee

        effects {
            Bruise 1
        }
    }
}
```

---

### `OneTwoPunch2`
**Description:** A melee attack that hits thrice! Each punch inflicts Bruise 1.  
**Source:** `fighter_abilities.gon`  

```
OneTwoPunch2 {
    variant_of OneTwoPunch

    meta {
        desc "ABILITY_ONETWOPUNCH2_DESC"
    }

    graphics {
        animation tripleswat
    }

    target {
        multihit 3
    }
}
```

---

### `TeamSpin`
**Name:** Synchro Spin  
**Description:** You and each allied cat do a spin attack at the same time.  
**Source:** `fighter_abilities.gon`  

```
TeamSpin {
    template self_buff
    sub_ability Spin
    
    meta {
        name "ABILITY_SYNCHROSPIN_NAME"
        desc "ABILITY_SYNCHROSPIN_DESC"
        class Fighter
    }

    graphics {
        animation prouder
    }
    
    cost {
        infcantrip true
        mana 8
    }

    target {
        aoe_hint_teamcast true
    }
    
    damage_instance {
        effects {
            TeamCastAbility Spin
        }
    }
}
```

---

### `TeamSpin2`
**Description:** You and each allied cat do a spin attack at the same time.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
TeamSpin2 {
    variant_of TeamSpin

    meta {
        desc "ABILITY_SYNCHROSPIN2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `TeamFlex`
**Name:** Flex Off  
**Description:** You and each allied cat gain +2 [img:shield] and knockback adjacent units 2 tiles.  
**Source:** `fighter_abilities.gon`  

```
TeamFlex {
    template self_buff
    sub_ability TeamFlex_Impl
    
    meta {
        name "ABILITY_FLEXOFF_NAME"
        desc "ABILITY_FLEXOFF_DESC"
        class Fighter
    }

    graphics {
		particle none
    }
    
    cost {
        infcantrip true
        mana 8
    }

    target {
        aoe_hint_teamcast true
    }
    
    damage_instance {
        effects {
            TeamCastAbility TeamFlex_Impl
        }
    }
}
```

---

### `TeamFlex2`
**Description:** You and each allied cat gain +2 [img:shield], +2 temporary Brace, and knockback adjacent units 2 tiles.  
**Source:** `fighter_abilities.gon`  

```
TeamFlex2 {
    variant_of TeamFlex

    meta {
        desc "ABILITY_FLEXOFF2_DESC"
    }

    damage_instance {
        effects {
            TeamCastAbility TeamFlex_Impl2
        }
    }
}
```

---

### `TeamFlex_Impl`
**Source:** `fighter_abilities.gon`  

```
TeamFlex_Impl { //this is a sub ability for TeamFlex and does not need an icon
    template spell

    graphics {
        animation flex
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

    self_damage {
        effects {
            Shield 2
        }
    }
    damage_instance {
        damage 0
        knockback 2
    }
}
```

---

### `TeamFlex_Impl2`
**Source:** `fighter_abilities.gon`  

```
TeamFlex_Impl2 {
    variant_of TeamFlex_Impl

    self_damage {
        effects {
            Shield 2
            Temporary {
                status Brace
                stacks 2
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `Huddle`
**Name:** Huddle  
**Description:** You and each allied cat give adjacent units +1 Damage and +2 [img:spd].  
**Source:** `fighter_abilities.gon`  

```
Huddle {
    template self_buff
    sub_ability Huddle_Impl
    
    meta {
        name "ABILITY_HUDDLE_NAME"
        desc "ABILITY_HUDDLE_DESC"
        class Fighter
    }

    graphics {
        animation none
		particle none
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        aoe_hint_teamcast true
    }
    
    damage_instance {
        effects {
            TeamCastAbility Huddle_Impl
        }
    }
}
```

---

### `Huddle2`
**Description:** You and each allied cat give adjacent units +1 Damage and +2 [img:spd].
\[s:.7\](This spell is free the first time it's cast each battle.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
Huddle2 {
    variant_of Huddle

    meta {
        desc "ABILITY_HUDDLE2_DESC"
    }

    cost {
        mana 6
    }
    bonus_passives {
        FreeFirstCastEachMatch 1
    }
}
```

---

### `Huddle_Impl`
**Source:** `fighter_abilities.gon`  

```
Huddle_Impl { //this is a sub ability for TeamFlex and does not need an icon
    template spell

    graphics {
        animation celebrate
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
        effects {
            DamageUp 1
            SpeedUp 2
        }
    }
}
```

---

### `RagePunch`
**Name:** Rage Punch  
**Description:** A melee attack that increases its damage by 1 each time you take damage.  
**Source:** `fighter_abilities.gon`  

```
RagePunch {
    template melee_attack
    
    meta {
        name "ABILITY_RAGEPUNCH_NAME"
        desc "ABILITY_RAGEPUNCH_DESC"
        class Fighter
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        X_is custom
    }
    bonus_passives {
        XIsTimesDamageTaken 1
    }


    damage_instance {
        damage 1+X
    }
}
```

---

### `RagePunch2`
**Description:** A melee attack that increases its damage by 1 each time you take damage.
\[s:.7\](This spell starts at 5 damage.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
RagePunch2 {
    variant_of RagePunch

    meta {
        desc "ABILITY_RAGEPUNCH2_DESC"
    }

    damage_instance {
        damage 5+X
    }
}
```

---

### `BreakingPoint`
**Name:** Breaking Point  
**Description:** Deal damage, knockback, and knockback damage equal to your [img:str].
Reduce this spell's mana cost by 1 each time you take damage.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
BreakingPoint {
    template melee_attack
    
    meta {
        name "ABILITY_BREAKINGPOINT_NAME"
        desc "ABILITY_BREAKINGPOINT_DESC"
        class Fighter
    }

    graphics {
		animation shoulder
    }

    cost {
        cantrip true
        mana 15-X
    }

    target {
        X_is custom
    }
    bonus_passives {
        XIsTimesDamageTaken 1
    }


    damage_instance {
        damage str
        knockback str

        effects {
            OverrideKnockbackDamage str
        }
    }
}
```

---

### `BreakingPoint2`
**Description:** Deal damage, knockback, and knockback damage equal to your [img:str].
Reduce this spell's mana cost by 2 each time you take damage.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
BreakingPoint2 {
    variant_of BreakingPoint

    meta {
        desc "ABILITY_BREAKINGPOINT2_DESC"
    }

    cost {
        mana 15-X*2
    }
}
```

---

### `AssertDominance`
**Name:** Assert Dominance  
**Description:** A weak melee attack. If this kills anything, you become the Alpha. If you are the Alpha, this spell deals 5 additional damage and inflicts Bruise.  
**Source:** `fighter_abilities.gon`  

```
AssertDominance {
    template melee_attack
    
    meta {
        name "ABILITY_ASSERTDOMINANCE_NAME"
        desc "ABILITY_ASSERTDOMINANCE_DESC"
        class Fighter
    }

    graphics {
		animation splashatk
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        X_is you_are_the_alpha
    }

    damage_instance {
        damage "1+bonus_melee_ability_damage+X*5"

        effects {
            ApplyToSourceOnKill {
                AlphaCat 1
            }
            Conditional_SourceHasStatus {
                status AlphaCat
                Bruise 1
            }
        }
    }
}
```

---

### `AssertDominance2`
**Description:** A weak melee attack. If this kills anything, you become the Alpha and gain +2 [img:str]. If you are the Alpha, this spell deals 5 additional damage and inflicts Bruise.  
**Source:** `fighter_abilities.gon`  

```
AssertDominance2 {
    variant_of AssertDominance

    meta {
        desc "ABILITY_ASSERTDOMINANCE2_DESC"
    }

    damage_instance {
        effects {
            ApplyToSourceOnKill {
                AlphaCat 1
                StrengthUp 2
            }
        }
    }
}
```

---

### `DumbMove`
**Name:** 1D Chess  
**Description:** Move toward the closest enemy. The dumber you are, the farther you move.  
**Source:** `fighter_abilities.gon`  

```
DumbMove {
    template self_buff

    meta {
        name "ABILITY_DUMBMOVE_NAME"
        desc "ABILITY_DUMBMOVE_DESC"
        class Fighter
        type_icon movement
    }
    
    cost {
        infcantrip true
        mana 3
    }

    graphics {

    }
    
    damage_instance {
        effects {
            ForceMoveTowardsEnemies DumbMove_Impl
        }
    }
}
```

---

### `DumbMove2`
**Description:** Move toward the closest enemy. The dumber you are, the farther you move.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
DumbMove2 {
    variant_of DumbMove

    meta {
        desc "ABILITY_DUMBMOVE2_DESC"
    }
    
    cost {
        mana 1
    }
}
```

---

### `DumbMove_Impl`
**Source:** `fighter_abilities.gon`  

```
DumbMove_Impl { //this is a sub ability for DumbMove and does not need an icon
    template move

    target { 
        max_range "max(5-int, 1)"
    }
}
```

---

### `ReflexPunchJab`
**Source:** `fighter_abilities.gon`  

```
ReflexPunchJab { //this is a sub ability for Reflex Punch passive and does not need an icon
    template melee_attack

    damage_instance {
        damage 1

        effects {
            Bruise 1
        }
    }
}
```

---

### `ReflexPunchJab2`
**Source:** `fighter_abilities.gon`  

```
ReflexPunchJab2 { //this is a sub ability for Reflex Punch passive and does not need an icon
    template melee_attack

    damage_instance {
        damage 5+bonus_melee_damage

        effects {
            Bruise 1
        }
    }
}
```

---

### `SuckerPunch`
**Name:** Sucker Punch  
**Description:** The next time an enemy moves through an adjacent tile, cancel its movement and attack it.  
**Source:** `fighter_abilities.gon`  

```
SuckerPunch {
    template self_buff

    meta {
        name "ABILITY_SUCKERPUNCH_NAME"
        desc "ABILITY_SUCKERPUNCH_DESC"
        class Fighter
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            Trapper_Status 1
        }
    }
}
```

---

### `SuckerPunch2`
**Description:** The next time an enemy moves through an adjacent tile, cancel its movement and attack it.
Bonus Passive: While it's not your turn, your basic attack inflicts Bruise 2.  
**Source:** `fighter_abilities.gon`  

```
SuckerPunch2 {
    variant_of SuckerPunch

    meta {
        desc "ABILITY_SUCKERPUNCH2_DESC"
    }

    bonus_passives {
        PassiveWhileNotTakingTurn {
            AddStatusToBasicAttack {
                Bruise 2
            }
        }
    }
}
```

---

### `Stick`
**Name:** Stick!  
**Description:** Equip a temporary Stick!
\[s:.7\](Your weapon slot must be empty.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
Stick {
    template self_buff
    
    meta {
        name "ABILITY_STICK_NAME"
        desc "ABILITY_STICK_DESC"
        type_icon "misc"
        class Fighter
    }

    target {
        restrictions aoe_must_exist
        aoe_restrictions must_have_cat_with_empty_weapon_slot
    }

    graphics {
        animation equipWeapon
    }

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        damage 0

        effects {
            Craft {
                pool stick //should expand to stick_0, stick_1, stick_2, stick_3
                slot weapon
                works_with_tech true
            }
        }
    }
}
```

---

### `Stick2`
**Description:** Equip a temporary Stick! Maybe even a big one?
\[s:.7\](Your weapon slot must be empty.)\[/s\]
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
Stick2 {
    variant_of Stick

    meta {
        desc "ABILITY_STICK2_DESC"
    }

    cost {
        mana 3
    }

    damage_instance {
        effects {
            Craft {
                pool allsticks
            }
        }
    }
}
```

---

### `Hurl`
**Name:** Hurl  
**Description:** Toss an adjacent unit at a random unit.  
**Source:** `fighter_abilities.gon`  

```
Hurl {
    template throw_attack
    
    meta {
        name "ABILITY_HURL_NAME"
        desc "ABILITY_HURL_DESC"
        class Fighter
    }

    graphics {
        animation knockupatk
    }

    cost {
        mana 5
        infcantrip true
    }
    
    target {
        target_mode random_tile
        min_range 2
        max_range 20
        restrictions must_have_enemy
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage

        blocked_damage 5+bonus_melee_ability_damage
    }
}
```

---

### `Hurl2`
**Description:** Toss an adjacent unit at a random unit.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `fighter_abilities.gon`  

```
Hurl2 {
    variant_of Hurl

    meta {
        desc "ABILITY_HURL2_DESC"
    }

    cost {
        mana 2
    }
}
```

---

### `BigPunch`
**Name:** Big Punch  
**Description:** A melee attack.
This spell's mana cost increases by 2 each time it's cast.  
**Source:** `fighter_abilities.gon`  

```
BigPunch {
    template melee_attack
    
    meta {
        name "ABILITY_BIGPUNCH_NAME"
        desc "ABILITY_BIGPUNCH_DESC"
        class Fighter
    }

    graphics {
        animation heavyMelee
    }

    target {
        X_is cast_count
    }

    cost {
        infcantrip true
        mana 3+X*2
    }

    damage_instance {
        damage 10+bonus_melee_ability_damage
    }
}
```

---

### `BigPunch2`
**Description:** A melee attack.
This spell's mana cost increases by 1 each time it's cast.  
**Source:** `fighter_abilities.gon`  

```
BigPunch2 {
    variant_of BigPunch

    meta {
        desc "ABILITY_BIGPUNCH2_DESC"
    }

    cost {
        mana 3+X*1
    }
}
```

---

### `Pawbreaker`
**Name:** Paw Breaker  
**Description:** A huge punch that breaks your paw... (You get -1 [img:str] permanently.)  
**Source:** `fighter_abilities.gon`  

```
Pawbreaker {
    template melee_attack
    
    meta {
        name "ABILITY_PAWBREAKER_NAME"
        desc "ABILITY_PAWBREAKER_DESC"
        class Fighter
    }

    graphics {
        animation heaviestMelee
    }

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        damage 15+bonus_melee_ability_damage

        effects {
            CanApplyToInanimate {
                ApplyToSource {
                    SpecificInjury str
                }
            }
        }
    }
}
```

---

### `Pawbreaker2`
**Description:** A huge punch that inflicts Bruise and Stun, and breaks your paw... (You get -1 [img:str] permanently.)  
**Source:** `fighter_abilities.gon`  

```
Pawbreaker2 {
    variant_of Pawbreaker

    meta {
        desc "ABILITY_PAWBREAKER2_DESC"
    }

    damage_instance {
        damage 15+bonus_melee_ability_damage

        effects {
            Bruise 1
            Stun 1
        }
    }
}
```

---

### `Ram`
**Name:** Ram  
**Description:** Knock back a unit 4 tiles, then dash forward and attack it.  
**Source:** `fighter_abilities.gon`  

```
Ram {
    template melee_attack
    
    meta {
        name "ABILITY_RAM_NAME"
        desc "ABILITY_RAM_DESC"
        class Fighter
        icon_damage_display_eq "3+bonus_melee_ability_damage"
        icon_shell_frame attack
    }

    cost {
        infcantrip true
        mana 6
    }

    damage_instance {
        damage 0
        type melee
        knockback 4

        effects {
            ApplyToSource {
                ForceUseAbility Ram_chained
            }
        }
    }
}
```

---

### `Ram_chained`
**Source:** `fighter_abilities.gon`  

```
Ram_chained {
    template dash_attack

    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }

    damage_instance {
        damage 3+bonus_melee_ability_damage
    }
}
```

---

### `Ram2`
**Description:** Knock back a unit 10 tiles, then dash forward and attack it.  
**Source:** `fighter_abilities.gon`  

```
Ram2 {
    variant_of Ram

    meta {
        desc "ABILITY_RAM2_DESC"
        icon_damage_display_suffix "x2"
        icon_shell_frame multihit_attack
    }

    damage_instance {
        damage 3+bonus_melee_ability_damage
        knockback 10
    }
}
```

---

## File: `hunter_abilities.gon`

### `LineShot`
**Name:** Line Shot  
**Description:** An attack that hits all units in a straight line.  
**Source:** `hunter_abilities.gon`  

```
LineShot {
    template spell
    
    meta {
        name "ABILITY_LINESHOT_NAME"
        desc "ABILITY_LINESHOT_DESC"
        class Hunter
    }

    graphics {
        particle ArrowFromAbove
        delay 10
        animation majormagic
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        target_mode direction  //tile, direction, none
        
        aoe_mode line //standard, line, cross, custom
        min_aoe 2+size
        max_aoe 10
        
        aoe_considers_character_size true
        aoe_excludes_self true

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

### `LineShot2`
**Description:** A stronger attack that hits all units in a straight line.  
**Source:** `hunter_abilities.gon`  

```
LineShot2 {
    variant_of LineShot

    meta {
        desc "ABILITY_LINESHOT2_DESC"
    }

    target {
        min_aoe 0
    }

    damage_instance {
        damage 9+bonus_ranged_damage
    }
}
```

---

### `HailOfNails`
**Name:** Hail of Nails  
**Description:** An attack that hits all units in a perpendicular line.  
**Source:** `hunter_abilities.gon`  

```
HailOfNails {
    template spell
    
    meta {
        name "ABILITY_HAILOFNAILS_NAME"
        desc "ABILITY_HAILOFNAILS_DESC"
        class Hunter
    }

    graphics {
        particle ArrowFromAbove
        delay 10
        animation majormagic
    }

    cost {
        infcantrip true
        mana 9
    }

    target {
        target_mode tile

        range_mode cross
        min_range 3
        max_range 10
        
        aoe_mode perpline
        min_aoe -10
        max_aoe 10

        knockback_mode zero
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

### `HailOfNails2`
**Description:** An attack that hits and Immobilizes all units in a perpendicular line.  
**Source:** `hunter_abilities.gon`  

```
HailOfNails2 {
    variant_of HailOfNails

    meta {
        desc "ABILITY_HAILOFNAILS2_DESC"
    }

    damage_instance {
        effects {
            Immobile 1
        }
    }
}
```

---

### `SpawnMaggotFriend`
**Name:** Spawn Maggot Friend  
**Description:** Spawn a maggot familiar.  
**Source:** `hunter_abilities.gon`  

```
SpawnMaggotFriend {
    template spawn

    meta {
        name "ABILITY_SPAWNMAGGOTFRIEND_NAME"
        desc "ABILITY_SPAWNMAGGOTFRIEND_DESC"
        class Hunter
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_range 3
        max_range 4
    }

    spawn {
        object CharmedMaggot
    }
}
```

---

### `SpawnMaggotFriend2`
**Description:** Spawn a [img:champion] maggot familiar.  
**Source:** `hunter_abilities.gon`  

```
SpawnMaggotFriend2 {
    variant_of SpawnMaggotFriend

    meta {
        desc "ABILITY_SPAWNMAGGOTFRIEND2_DESC"
    }

    spawn {
        object CharmedMaggot_Champion
    }
}
```

---

### `SpawnPooterFriend`
**Name:** Spawn Pooter Friend  
**Description:** Spawn a pooter familiar.  
**Source:** `hunter_abilities.gon`  

```
SpawnPooterFriend {
    template spawn

    meta {
        name "ABILITY_SPAWNPOOTERFRIEND_NAME"
        desc "ABILITY_SPAWNPOOTERFRIEND_DESC"
        class Hunter
    }

    tags [summon]
    
    graphics {
        lob true
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        min_range 1
        max_range 2
    }

    spawn {
        object CharmedPooter
    }
}
```

---

### `SpawnPooterFriend2`
**Description:** Spawn 2 pooter familiars.  
**Source:** `hunter_abilities.gon`  

```
SpawnPooterFriend2 {
    variant_of SpawnPooterFriend

    meta {
        desc "ABILITY_SPAWNPOOTERFRIEND2_DESC"
    }

    target {
        min_range 1
        max_range 3

        max_aoe 1
        max_targets 2
    }
}
```

---

### `Marked`
**Name:** Marked  
**Description:** Inflict Marked on a unit.  
**Source:** `hunter_abilities.gon`  

```
Marked {
    template targeted_status

    meta {
        name "ABILITY_MARKED_NAME"
        desc "ABILITY_MARKED_DESC"
        class Hunter
    }

    graphics {
        affected_particle TakeAim
        animation pointout
    }
    
    cost {
        mana 5
        infcantrip true
    }
    
    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        effects {
            Marked 1
        }
    }
}
```

---

### `Marked2`
**Name:** Marked  
**Description:** Inflict Marked on a unit and all other units of the same type.  
**Source:** `hunter_abilities.gon`  

```
Marked2 {
    template targeted_status

    meta {
        name "ABILITY_MARKED_NAME"
        desc "ABILITY_MARKED2_DESC"
        class Hunter
    }

    graphics {
        affected_particle TakeAim
        animation pointout
    }
    
    cost {
        mana 5
        infcantrip true
    }
    
    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        effects {
            Marked 1
            ApplyToOthersWithSharedTagAndFaction {
                Marked 1
            }
        }
    }
}
```

---

### `ScatterShot`
**Name:** Scatter Shot  
**Description:** Fire a bunch of shots randomly in an area.  
**Source:** `hunter_abilities.gon`  

```
ScatterShot {
    template lobbed_attack
    
    meta {
        name "ABILITY_SCATTERSHOT_NAME"
        desc "ABILITY_SCATTERSHOT_DESC"
        class Hunter
    }

    graphics {
        
    }

    cost {
        infcantrip true
        mana 10
    }

    target {
        max_aoe 3

        min_range 3
        max_range 6+bonus_range

        aoe_chance .5
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

### `ScatterShot2`
**Description:** Fire a bunch of shots randomly in a large area.  
**Source:** `hunter_abilities.gon`  

```
ScatterShot2 {
    variant_of ScatterShot

    meta {
        desc "ABILITY_SCATTERSHOT2_DESC"
    }

    target {
        max_aoe 4
    }
}
```

---

### `BrambleShot`
**Name:** Bramble Shot  
**Description:** Fire a shot that spawns brambles in an area.  
**Source:** `hunter_abilities.gon`  

```
BrambleShot {
    template spell

    meta {
        name "ABILITY_BRAMBLESHOT_NAME"
        desc "ABILITY_BRAMBLESHOT_DESC"
        class Hunter
    }

    graphics {
		animation throwArrow
        use_projectile true
        particle none
        projectile BrambleProjectile
        delay 5
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        max_aoe level
        min_range 3
        max_range 5+bonus_range
    }
    
    damage_instance {
        damage 2
        
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

### `BrambleShot2`
**Description:** Fire a shot that spawns brambles in a large area.  
**Source:** `hunter_abilities.gon`  

```
BrambleShot2 {
    variant_of BrambleShot

    meta {
        desc "ABILITY_BRAMBLESHOT2_DESC"
    }

    target {
        max_aoe level
        min_range 0
        max_range 20
    }
}
```

---

### `BearTrap`
**Name:** Bear Trap  
**Description:** Set a trap within 5 tiles that damages and immobilizes units that walk over it.  
**Source:** `hunter_abilities.gon`  

```
BearTrap {
    template lobbed_attack
    
    meta {
        name "ABILITY_BEARTRAP_NAME"
        desc "ABILITY_BEARTRAP_DESC"
        class Hunter
        type_icon "misc"
    }

    graphics {
        projectile DamageTrap
        use_rotation false
        animation throwobject
    }

    cost {
        mana 5
        infcantrip true
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

### `BearTrap2`
**Description:** Set a trap on any tile that damages and immobilizes units that walk over it.  
**Source:** `hunter_abilities.gon`  

```
BearTrap2 {
    variant_of BearTrap

    meta {
        desc "ABILITY_BEARTRAP2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `Harpoon`
**Name:** Harpoon  
**Description:** Hook onto something in a straight line and drag yourself to it.  
**Source:** `hunter_abilities.gon`  

```
Harpoon { //CUT
    template straightshot_attack
    
    meta {
        name "ABILITY_HARPOON_NAME"
        desc "ABILITY_HARPOON_DESC"
        class Hunter
        type_icon "movement"
    }

    graphics {
        animation invthrow

        projectile HookProjectile
        chain_movieclip ChainLink
        chain_distance .25
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        max_aoe 10
    }

    damage_instance {
        damage 1

        effects {
            PullSourceToTarget 1
        }
    }
}
```

---

### `Harpoon2`
**Description:** Hook onto something in a straight line and drag yourself to it.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
Harpoon2 {
    variant_of Harpoon

    meta {
        desc "ABILITY_HARPOON2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `TwinShot`
**Name:** Twin Shot  
**Description:** Shoot twice.  
**Source:** `hunter_abilities.gon`  

```
TwinShot {
    template lobbed_attack
    
    meta {
        name "ABILITY_TWINSHOT_NAME"
        desc "ABILITY_TWINSHOT_DESC"
        class Hunter
    }

    graphics {
        animation throwArrow
        projectile ArrowProjectile
    }

    cost {
        infcantrip true
        mana 9
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 4+bonus_ranged_damage
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `TwinShot2`
**Description:** Shoot thrice.  
**Source:** `hunter_abilities.gon`  

```
TwinShot2 {
    variant_of TwinShot

    meta {
        desc "ABILITY_TWINSHOT2_DESC"
    }

    temporary_effects {
        CastAgain 2
    }
}
```

---

### `CrossShot`
**Name:** Cross Shot  
**Description:** Shoot four projectiles in an X shape.  
**Source:** `hunter_abilities.gon`  

```
CrossShot {
    template straightshot_attack
    
    meta {
        name "ABILITY_CROSSSHOT_NAME"
        desc "ABILITY_CROSSSHOT_DESC"
        class Hunter
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        target_mode none
        aoe_mode custom
        aoe_symmetry four_way
        custom_aoe [[1, 1]]
    }

    damage_instance {
        damage 4+bonus_ranged_damage
    }
}
```

---

### `CrossShot2`
**Description:** Shoot four penetrating projectiles in an X shape.  
**Source:** `hunter_abilities.gon`  

```
CrossShot2 {
    variant_of CrossShot

    meta {
        desc "ABILITY_CROSSSHOT2_DESC"
    }

    target {
        upgrade_straight_shot_to_piercing true
    }
}
```

---

### `SpawnBaitTrap`
**Name:** Bait Trap  
**Description:** Set a bait trap that attracts enemies.  
**Source:** `hunter_abilities.gon`  

```
SpawnBaitTrap {
    template spawn

    meta {
        name "ABILITY_BAITTRAP_NAME"
        desc "ABILITY_BAITTRAP_DESC"
        class Hunter
        type_icon "misc"
    }
    
    graphics {
        lob true
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        min_range 1
        max_range 5
        restrictions [must_be_empty aoe_must_exist]
    }

    spawn {
        object Bait
        layer pickups
    }
}
```

---

### `SpawnBaitTrap2`
**Description:** Set a bait trap that attracts enemies and inflicts Poison and Slow when eaten.  
**Source:** `hunter_abilities.gon`  

```
SpawnBaitTrap2 {
    variant_of SpawnBaitTrap

    meta {
        desc "ABILITY_BAITTRAP2_DESC"
    }

    spawn {
        object PoisonBait
        layer pickups
    }
}
```

---

### `BombShot`
**Name:** Bomb Shot  
**Description:** Toss a bomb that explodes and knocks units away.  
**Source:** `hunter_abilities.gon`  

```
BombShot {
    template spell
    
    meta {
        name "ABILITY_BOMBSHOT_NAME"
        desc "ABILITY_BOMBSHOT_DESC"
        class Hunter
    }

    graphics {
        animation shoot
        center_particle Explosion
        area_particle none
        use_projectile true
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        max_aoe 1
        min_range 3
        max_range 5+bonus_range
    }
    
    damage_instance {
        damage 5
        type spell
        knockback 1

        elements [
            Explosion
        ]
    }
}
```

---

### `BombShot2`
**Description:** Toss a large bomb that explodes and knocks units away.  
**Source:** `hunter_abilities.gon`  

```
BombShot2 {
    variant_of BombShot

    meta {
        desc "ABILITY_BOMBSHOT2_DESC"
    }

    target {
        max_aoe 2
    }
}
```

---

### `SummonBrambles`
**Name:** Summon Brambles  
**Description:** Spawn brambles on any tile.  
**Source:** `hunter_abilities.gon`  

```
SummonBrambles {
    template spell

    meta {
        name "ABILITY_SUMMONBRAMBLES_NAME"
        desc "ABILITY_SUMMONBRAMBLES_DESC"
        class Hunter
        type_icon "magic"
    }

    graphics {
	particle none
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_aoe level-1
        min_range 1
        max_range 20
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

### `SummonBrambles2`
**Description:** Spawn brambles in an area.  
**Source:** `hunter_abilities.gon`  

```
SummonBrambles2 {
    variant_of SummonBrambles

    meta {
        desc "ABILITY_SUMMONBRAMBLES2_DESC"
    }
}
```

---

### `FireShot`
**Name:** Fire Shot  
**Description:** Shoot a projectile that inflicts Burn 2 and lights fires.  
**Source:** `hunter_abilities.gon`  

```
FireShot {
    template spell
    
    meta {
        name "ABILITY_FIRESHOT_NAME"
        desc "ABILITY_FIRESHOT_DESC"
        class Hunter
    }

    graphics {
        animation throwArrow
        center_particle none
        area_particle none
        use_projectile true
		projectile FireProjectile
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        max_aoe 1
        min_range 3
        max_range 5+bonus_range
    }
    
    damage_instance {
        damage 2+bonus_ranged_damage
        type ranged

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

### `FireShot2`
**Description:** Shoot a projectile with infinite range that inflicts Burn 4 and lights fires.  
**Source:** `hunter_abilities.gon`  

```
FireShot2 {
    variant_of FireShot

    meta {
        desc "ABILITY_FIRESHOT2_DESC"
    }

    target {
        max_range 20
    }

    damage_instance {
        effects {
            Burn 4
        }
    }
}
```

---

### `TrailBlazer`
**Name:** Trail Blazer  
**Description:** Increase your movement. You're unaffected by tile effects until the end of the turn.  
**Source:** `hunter_abilities.gon`  

```
TrailBlazer { //CUT
    template self_buff
    
    meta {
        name "ABILITY_TRAILBLAZER_NAME"
        desc "ABILITY_TRAILBLAZER_DESC"
        class Hunter
        type_icon "movement"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            TrailBlazer 1
        }
    }
}
```

---

### `TrailBlazer2`
**Description:** Double your movement.  You're unaffected by tile effects until the end of the turn.  
**Source:** `hunter_abilities.gon`  

```
TrailBlazer2 {
    variant_of TrailBlazer

    meta {
        desc "ABILITY_TRAILBLAZER2_DESC"
    }

    damage_instance {
        effects {
            TrailBlazer mov
        }
    }
}
```

---

### `FocusShot`
**Name:** Focus Shot  
**Description:** Aim at a unit. On your next turn, shoot a projectile that always crits and ignores shield at that unit.  
**Source:** `hunter_abilities.gon`  

```
FocusShot {
    template lobbed_attack
    
    meta {
        name "ABILITY_FOCUSSHOT_NAME"
        desc "ABILITY_FOCUSSHOT_DESC"
        class Hunter
    }

    graphics {
        lob_height 1
        speed 20
        animation throwArrow
        projectile ArrowProjectile

        darken_screen true
        darken_screen_exclude_characters_on_tile true
        darken_screen_exclude_self true
        darken_screen_start_early true
    }

    cost {
        cantrip true
        mana 7
    }

    target {
        delayed_trigger true

        min_range 3
        max_range 5+bonus_range
        track_target true
        hint_can_target_empty false
    }

    damage_instance {
        damage 4+bonus_ranged_damage
        piercing true
        crit_chance 100%
        cant_miss true
    }
}
```

---

### `FocusShot2`
**Description:** Shoot a projectile that always crits and ignores shield.  
**Source:** `hunter_abilities.gon`  

```
FocusShot2 {
    variant_of FocusShot

    meta {
        desc "ABILITY_FOCUSSHOT2_DESC"
    }

    cost {
        infcantrip true
    }

    target {
        delayed_trigger false
    }
}
```

---

### `Shards`
**Name:** Shards  
**Description:** Shoot a projectile that spawns glass.  
**Source:** `hunter_abilities.gon`  

```
Shards {
    template lobbed_attack
    
    meta {
        name "ABILITY_SHARDS_NAME"
        desc "ABILITY_SHARDS_DESC"
        class Hunter
    }

    graphics {
        animation throwArrow
        projectile GlassBall
    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }
    
    damage_instance {
        damage 1
        type ranged

        effects {
            ChangeTile GlassTile
        }
    }
}
```

---

### `Shards2`
**Description:** Shoot a projectile that spawns glass in an area and inflicts Bleed 2.  
**Source:** `hunter_abilities.gon`  

```
Shards2 {
    variant_of Shards

    meta {
        desc "ABILITY_SHARDS2_DESC"
    }

    damage_instance {
        damage 2
        type ranged

        effects {
            ChangeTile {
                tile GlassTile
                aoe 1
            }
            Bleed 2
        }
    }
}
```

---

### `TerrainWalk`
**Name:** Terrain Walk  
**Description:** Teleport to any grass or water tile.  
**Source:** `hunter_abilities.gon`  

```
TerrainWalk {
    template teleport
    
    meta {
        name "ABILITY_TERRAINWALK_NAME"
        desc "ABILITY_TERRAINWALK_DESC"
        animate_name true
        class Hunter
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 20

        restrictions [must_be_moveable must_have_element]
        target_requires_element [grass water]
    }
}
```

---

### `TerrainWalk2`
**Description:** Teleport to any grass or water tile. Gain Stealth.  
**Source:** `hunter_abilities.gon`  

```
TerrainWalk2 {
    variant_of TerrainWalk

    meta {
        desc "ABILITY_TERRAINWALK2_DESC"
    }

    cost {
        mana 4
    }

    self_damage {
        effects {
            Stealth 1
        }
    }
}
```

---

### `Extend`
**Name:** Extend  
**Description:** Give a unit +3 range and reach until the end of their next turn.  
**Source:** `hunter_abilities.gon`  

```
Extend {
    template spell
    
    meta {
        name "ABILITY_EXTEND_NAME"
        desc "ABILITY_EXTEND_DESC"
        class Hunter
        type_icon "buff"
    }

    graphics {
		particle fx_statup
		animation pointout
    }

    cost {
        mana 3
        infcantrip true
    }

    target {
        min_range 1
        max_range 4
        max_aoe 0
    }

    damage_instance {
        damage 0

        effects {
            TempRangeUp 3

            Temporary   {
                status MeleeRangeUp
                stacks 3
                turns 1
            }
        }
    }
}
```

---

### `Extend2`
**Name:** Extend  
**Description:** Give a unit +20 range and reach until the end of their next turn.  
**Source:** `hunter_abilities.gon`  

```
Extend2 {
    template spell
    
    meta {
        name "ABILITY_EXTEND_NAME"
        desc "ABILITY_EXTEND2_DESC"
        class Hunter
    }

    graphics {
		particle fx_statup
    }

    cost {
        mana 3
        infcantrip true
    }

    target {
        min_range 1
        max_range 4
        max_aoe 0
    }

    damage_instance {
        damage 0

        effects {
            TempRangeUp 20

            Temporary   {
                status MeleeRangeUp
                stacks 20
                turns 1
            }
        }
    }
}
```

---

### `ChaosShot`
**Name:** Chaos Shot  
**Description:** Shoot a random unit within range.  
**Source:** `hunter_abilities.gon`  

```
ChaosShot {
    template lobbed_attack
    
    meta {
        name "ABILITY_CHAOSSHOT_NAME"
        desc "ABILITY_CHAOSSHOT_DESC"
        class Hunter
    }

    graphics {
        animation throwArrow
        projectile ArrowProjectile
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        target_mode random_tile
        min_range 3
        max_range 5+bonus_range

        restrictions must_have_animate_character
    }

    damage_instance {
        damage 4+bonus_ranged_damage
    }
}
```

---

### `ChaosShot2`
**Description:** Shoot a random unit within range, twice!  
**Source:** `hunter_abilities.gon`  

```
ChaosShot2 {
    variant_of ChaosShot

    meta {
        desc "ABILITY_CHAOSSHOT2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `NeedleShot`
**Name:** Needle Shot  
**Description:** Shoot a needle that deals damage, gives Thorns, and ignores shield.  
**Source:** `hunter_abilities.gon`  

```
NeedleShot {
    template lobbed_attack
    
    meta {
        name "ABILITY_NEEDLESHOT_NAME"
        desc "ABILITY_NEEDLESHOT_DESC"
        class Hunter
    }

    graphics {
        projectile NeedleProjectile
        animation throwArrow
    }

    cost {
        infcantrip true
        mana 2
    }

    target {
        min_range 3
        max_range 5+bonus_range
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

### `NeedleShot2`
**Description:** Shoot a needle that deals damage, gives Thorns, and ignores shield. This deals extra damage to enemies and gives extra Thorns to allies.  
**Source:** `hunter_abilities.gon`  

```
NeedleShot2 {
    variant_of NeedleShot

    meta {
        desc "ABILITY_NEEDLESHOT2_DESC"
    }

    damage_instance {
        effects {
            Conditional_Enemy {
                BonusDamage 1
            }
            Conditional_Ally {
                Thorns 1
            }
        }
    }
}
```

---

### `SpikeTrap`
**Name:** Spike Trap  
**Description:** Set a trap that deals 8 damage.  
**Source:** `hunter_abilities.gon`  

```
SpikeTrap {
    template lobbed_attack
    
    meta {
        name "ABILITY_SPIKETRAP_NAME"
        desc "ABILITY_SPIKETRAP_DESC"
        class Hunter
        type_icon "misc"
    }

    graphics {
        projectile SpikeTrap
        animation throwobject
        use_rotation false
    }

    cost {
        mana 6
        infcantrip true
    }

    target {
        min_range 1
        max_range 5

        restrictions must_be_empty
    }

    damage_instance {
        damage 8
        ai_base_score 10
        custom_additional_ai_weight tile_has_no_known_traps
        
        effects {
            SpawnCustomTrap SpikeTrap
        }
    }
}
```

---

### `SpikeTrap2`
**Description:** Set a trap that deals 13 damage.  
**Source:** `hunter_abilities.gon`  

```
SpikeTrap2 {
    variant_of SpikeTrap

    meta {
        desc "ABILITY_SPIKETRAP2_DESC"
    }

    target {
        max_range 6
    }

    damage_instance {
        damage 13
    }
}
```

---

### `FleaShot`
**Name:** Flea Shot  
**Description:** Shoot a flea at a unit.  
**Source:** `hunter_abilities.gon`  

```
FleaShot {
    template lobbed_attack
    
    meta {
        name "ABILITY_FLEASHOT_NAME"
        desc "ABILITY_FLEASHOT_DESC"
        type_icon "spawn"
        class Hunter
    }

    tags [summon]

    graphics {
        projectile Flea
    }

    cost {
        mana 6
        infcantrip true
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 2

        effects {
            BounceObject CharmedFlea
        }
    }
}
```

---

### `FleaShot2`
**Description:** Shoot a [img:champion] flea at a unit.  
**Source:** `hunter_abilities.gon`  

```
FleaShot2 {
    variant_of FleaShot
    
    meta {
        desc "ABILITY_FLEASHOT2_DESC"
    }

    damage_instance {
        damage 4

        effects {
            BounceObject CharmedFlea_Champion
        }
    }
}
```

---

### `WebTrap`
**Name:** Web Trap  
**Description:** Set a trap that webs non-bug units that walk through it.  
**Source:** `hunter_abilities.gon`  

```
WebTrap {
    template lobbed_attack

    keyword_tooltips {Webbed 1}
    
    meta {
        name "ABILITY_WEBTRAP_NAME"
        desc "ABILITY_WEBTRAP_DESC"
        class Hunter
        type_icon "misc"
    }

    graphics {
        projectile WebTrap
        animation throwobject
        use_rotation false
    }

    cost {
        mana 4
        infcantrip true
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
            SpawnWebTrap 1
        }
    }
}
```

---

### `WebTrap2`
**Description:** Set a web trap on any tile that webs non-bug units that walk through it.  
**Source:** `hunter_abilities.gon`  

```
WebTrap2 {
    variant_of WebTrap

    meta {
        desc "ABILITY_WEBTRAP2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `LastHit`
**Name:** Last Hit  
**Description:** Deal 1 damage to a unit. If this kills it, refresh your basic attack.  
**Source:** `hunter_abilities.gon`  

```
LastHit {
    template lobbed_attack
    
    meta {
        name "ABILITY_LASTHIT_NAME"
        desc "ABILITY_LASTHIT_DESC"
        class Hunter
    }

    graphics {
        animation throwArrow
        projectile ArrowProjectile
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 1
        
        effects {
            ApplyToSourceOnKill {
                RefreshActPoints 1
            }
        }
    }
}
```

---

### `LastHit2`
**Description:** Deal 1 damage to a unit. If this kills it, refresh your basic attack. This ignores shield and can't miss.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
LastHit2 {
    variant_of LastHit

    meta {
        desc "ABILITY_LASTHIT2_DESC"
    }

    cost {
        mana 2
    }

    damage_instance {
        piercing true
        cant_miss true
    }
}
```

---

### `CupidsArrow`
**Name:** Cupid's Arrow  
**Description:** A shot that damages and inflicts Charm.  
**Source:** `hunter_abilities.gon`  

```
CupidsArrow {
    template lobbed_attack
    
    meta {
        name "ABILITY_CUPIDSARROW_NAME"
        desc "ABILITY_CUPIDSARROW_DESC"
        class Hunter
    }

    graphics {
        projectile CupidsArrowProjectile
        animation throwArrow
    }

    cost {
        infcantrip true
        mana 12
    }

    target {
        min_range 3
        max_range 8+bonus_range
    }

    damage_instance {
        damage 6+bonus_ranged_damage
        effects {
            Charmed level
        }
    }
}
```

---

### `CupidsArrow2`
**Description:** A shot that damages and inflicts Charm 2.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
CupidsArrow2 {
    variant_of CupidsArrow

    cost {
        infcantrip true
        mana 8
    }

    meta {
        desc "ABILITY_CUPIDSARROW2_DESC"
    }
}
```

---

### `ArrowFlurry`
**Name:** Arrow Flurry  
**Description:** Shoot 5 weak shots, each one has a 50% chance to miss.  
**Source:** `hunter_abilities.gon`  

```
ArrowFlurry {
    template lobbed_attack
    
    meta {
        name "ABILITY_ARROWFLURRY_NAME"
        desc "ABILITY_ARROWFLURRY_DESC"
        class Hunter
    }

    graphics {
		animation throwArrow
		projectile ArrowProjectile
    }

    cost {
        infcantrip true
        mana 8
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 2+bonus_ranged_damage
        accuracy .5
    }

    temporary_effects {
        CastAgain 4
    }
}
```

---

### `ArrowFlurry2`
**Description:** Shoot 5 weak shots, each one has a 50% chance to miss and 50% chance to crit!  
**Source:** `hunter_abilities.gon`  

```
ArrowFlurry2 {
    variant_of ArrowFlurry

    meta {
        desc "ABILITY_ARROWFLURRY2_DESC"
    }

    damage_instance {
        damage 3+bonus_ranged_damage
        accuracy .5
        crit_chance .5
    }
}
```

---

### `HeavyShot`
**Name:** Heavy Shot  
**Description:** Shoot a high damage shot with a 50% chance to miss.  
**Source:** `hunter_abilities.gon`  

```
HeavyShot {
    template lobbed_attack
    
    meta {
        name "ABILITY_HEAVYSHOT_NAME"
        desc "ABILITY_HEAVYSHOT_DESC"
        class Hunter
    }

    graphics {
        lob_height 4
        animation throwArrow
        projectile ArrowProjectile
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 8+bonus_ranged_damage
        accuracy .5
    }
}
```

---

### `HeavyShot2`
**Description:** Shoot a high damage shot with a 50% chance to miss and a 50% chance to crit.
\[s:.7\](This spell has increased range.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
HeavyShot2 {
    variant_of HeavyShot

    meta {
        desc "ABILITY_HEAVYSHOT2_DESC"
    }

    target {
        min_range 3
        max_range 8+bonus_range
    }

    damage_instance {
        crit_chance .5
    }
}
```

---

### `StakeOut`
**Name:** Stake Out  
**Description:** End your turn. On your next turn, your ranged abilities deal double damage.
\[s:.7\](Castable only if you haven't taken any other actions this turn.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
StakeOut {
    template self_buff
    
    meta {
        name "ABILITY_STAKEOUT_NAME"
        desc "ABILITY_STAKEOUT_DESC"
        class Hunter
    }

    graphics {
		animation statup
    }
    
    cost {
        infcantrip true
        mana 3
        must_be_first_action true
    }
    
    damage_instance {
        effects {
            EndTurn 1
            NextTurnDoubleRangedDamage 1
        }
    }
}
```

---

### `StakeOut2`
**Description:** End your turn. On your next turn, your ranged abilities deal double damage.
\[s:.7\](Costs 0 mana. Castable only if you haven't taken any other actions this turn other than your movement action.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
StakeOut2 {
    variant_of StakeOut

    meta {
        desc "ABILITY_STAKEOUT2_DESC"
    }

    cost {
        infcantrip true
        mana 0
        must_be_first_action false
        must_be_first_nonmove_action true
    }
}
```

---

### `BallOfSpiders`
**Name:** Ball of Spiders  
**Description:** Throw a spider egg that spawns 3 spiderlings on impact.  
**Source:** `hunter_abilities.gon`  

```
BallOfSpiders {
    template lobbed_attack
    
    meta {
        name "ABILITY_BALLOFSPIDERS_NAME"
        desc "ABILITY_BALLOFSPIDERS_DESC"
        type_icon "spawn"
        class Hunter
    }

    tags [summon]

    graphics {
        animation throwobject
        projectile SpiderBall
    }

    cost {
        mana 9
        infcantrip true
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 2

        effects {
            BounceObject CharmedTinySpider
            BounceObject CharmedTinySpider
            BounceObject CharmedTinySpider
        }
    }
}
```

---

### `BallOfSpiders2`
**Description:** Throw a stronger spider egg that spawns 3 spiderlings on impact.  
**Source:** `hunter_abilities.gon`  

```
BallOfSpiders2 {
    variant_of BallOfSpiders

    meta {
        desc "ABILITY_BALLOFSPIDERS2_DESC"
    }

    damage_instance {
        damage 6
    }
}
```

---

### `Snipe`
**Name:** Snipe  
**Description:** Fire a shot exactly 6 tiles away that ignores shield and can't miss.  
**Source:** `hunter_abilities.gon`  

```
Snipe {
    template lobbed_attack
    
    meta {
        name "ABILITY_SNIPE_NAME"
        desc "ABILITY_SNIPE_DESC"
        class Hunter
    }

    graphics {
		animation throwArrow
		projectile ArrowProjectile
    }


    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 6
        max_range 6
    }

    damage_instance {
        damage 5+bonus_ranged_damage
        cant_miss true
        piercing true
    }
}
```

---

### `Snipe2`
**Description:** Fire a stronger shot exactly 6 tiles away that ignores shield, can't miss, and has a 50% chance to crit.  
**Source:** `hunter_abilities.gon`  

```
Snipe2 {
    variant_of Snipe

    meta {
        desc "ABILITY_SNIPE2_DESC"
    }

    damage_instance {
        damage 8+bonus_ranged_damage
        crit_chance .5
    }
}
```

---

### `Diversion`
**Name:** Diversion  
**Description:** Shoot a pebble. All enemies within 3 tiles move toward it.  
**Source:** `hunter_abilities.gon`  

```
Diversion {
    template lobbed_attack
    
    meta {
        name "ABILITY_DIVERSION_NAME"
        desc "ABILITY_DIVERSION_DESC"
        class Hunter
    }

    graphics {
        single_projectile true
		projectile Pebble
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 3
        max_range 5+bonus_range
        max_aoe 3
        aoe_restrictions exclude_allies
    }

    damage_instance {
        damage 1

        effects {
            ForceMoveNonAlliesInRangeTowardsTile 3
        }
    }

    splash_damage {
        damage 0
        type status_spell
    }
}
```

---

### `Diversion2`
**Description:** Shoot a pebble. All enemies within 3 tiles move toward it and gain Confusion.  
**Source:** `hunter_abilities.gon`  

```
Diversion2 {
    variant_of Diversion

    meta {
        desc "ABILITY_DIVERSION2_DESC"
    }

    target {
        max_aoe 4
    }

    damage_instance {
        effects {
            ForceMoveNonAlliesInRangeTowardsTile 4
            Confusion 1
        }
    }

    splash_damage {
        effects {
            Conditional_NotAlly {
                Confusion 1
            }
        }
    }
}
```

---

### `ArrowSmith`
**Name:** Arrowsmith  
**Description:** Gain +1 Bonus Attack at the start of your next turn.  
**Source:** `hunter_abilities.gon`  

```
ArrowSmith {
    template self_buff
    
    meta {
        name "ABILITY_ARROWSMITH_NAME"
        desc "ABILITY_ARROWSMITH_DESC"
        class Hunter
    }
	
    graphics {
        particle none
		animation Quiver
    }
	
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            ApplyStatusesNextTurnBegin {
                Quivered 1
            }
        }
    }
}
```

---

### `ArrowSmith2`
**Description:** You or another unit gains +1 Bonus Attack at the start of their next turn.  
**Source:** `hunter_abilities.gon`  

```
ArrowSmith2 {
    variant_of ArrowSmith

    meta {
        desc "ABILITY_ARROWSMITH2_DESC"
    }

    target {
        target_mode tile
        min_range 0
        max_range 5+bonus_range
    }
}
```

---

### `TacticalRetreat`
**Name:** Tactical Retreat  
**Description:** Teleport up to 5 tiles away. Set a bear trap on the tile you teleported from.  
**Source:** `hunter_abilities.gon`  

```
TacticalRetreat {
    template teleport
    
    meta {
        name "ABILITY_TACTICALRETREAT_NAME"
        desc "ABILITY_TACTICALRETREAT_DESC"
        class Hunter
        animate_name true
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 5
    }

    temporary_effects {
        BearTrapTrail 1
    }
}
```

---

### `TacticalRetreat2`
**Description:** Teleport up to 5 tiles away. Set a baited bear trap on the tile you teleported from.  
**Source:** `hunter_abilities.gon`  

```
TacticalRetreat2 {
    variant_of TacticalRetreat
    meta {
        desc "ABILITY_TACTICALRETREAT2_DESC"
    }

    temporary_effects {
        BearTrapTrail 1
        LeaveBehind Bait
    }
}
```

---

### `Infest`
**Name:** Infest  
**Description:** Toss a spider egg that deals low damage and inflicts Infested.  
**Source:** `hunter_abilities.gon`  

```
Infest {
    template lobbed_attack
    
    meta {
        name "ABILITY_INFEST_NAME"
        desc "ABILITY_INFEST_DESC"
        class Hunter
    }
	
    graphics {
        animation throwobject
		projectile SpiderBall
    }

    cost {
        mana 4
        infcantrip true
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 1+bonus_ranged_damage

        effects {
            SpiderInfested 1
        }
    }
}
```

---

### `Infest2`
**Description:** Toss a spider egg that deals low damage and inflicts Infested 2.  
**Source:** `hunter_abilities.gon`  

```
Infest2 {
    variant_of Infest

    meta {
        desc "ABILITY_INFEST2_DESC"
    }

    damage_instance {
        effects {
            SpiderInfested 2
        }
    }
}
```

---

### `CollectPelt`
**Name:** Collect Pelt  
**Description:** Destroy a body. Equip a piece of Cat Hide armor to an empty armor slot.  
**Source:** `hunter_abilities.gon`  

```
CollectPelt {
    template melee_attack
    
    meta {
        name "ABILITY_COLLECTPELT_NAME"
        desc "ABILITY_COLLECTPELT_DESC"
        class Hunter
        type_icon "misc"
    }

    graphics {
        animation sliceOpen
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 0
        type melee
        incidentally_collects_pickups false

        effects {
            VaporizeCorpse 1
            ApplyToSource {
                Craft {
                    slot random_empty_armor
                    pool pelts
                    temporary false
                }
            }
        }
    }
}
```

---

### `CollectPelt2`
**Description:** Destroy a body. Create a big food pickup and equip a piece of Cat Hide armor to an empty armor slot.  
**Source:** `hunter_abilities.gon`  

```
CollectPelt2 {
    variant_of CollectPelt

    meta {
        desc "ABILITY_COLLECTPELT2_DESC"
    }

    cost {
        mana 2
    }

    damage_instance {
        effects {
            ObjectOnHit BiggestFood
        }
    }
}
```

---

### `SentryMode`
**Name:** Sentry Mode  
**Description:** The next time an enemy ends movement in your basic attack range, attack it.  
**Source:** `hunter_abilities.gon`  

```
SentryMode {
    template self_buff
    
    meta {
        name "ABILITY_SENTRYMODE_NAME"
        desc "ABILITY_SENTRYMODE_DESC"
        class Hunter
    }

    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            TowerDefenseStatus 1
        }
    }
}
```

---

### `SentryMode2`
**Name:** Sentry Mode  
**Description:** Until your next turn, whenever an enemy ends movement in your basic attack range, attack it.  
**Source:** `hunter_abilities.gon`  

```
SentryMode2 {
    template self_buff
    
    meta {
        name "ABILITY_SENTRYMODE_NAME"
        desc "ABILITY_SENTRYMODE2_DESC"
        class Hunter
    }

    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            TowerDefenseStatus2 1
        }
    }
}
```

---

### `Pheromones`
**Name:** Pheromones  
**Description:** Inflict Charm on a unit. If it's an enemy, it takes an extra turn immediately.  
**Source:** `hunter_abilities.gon`  

```
Pheromones {
    template lobbed_attack
    
    meta {
        name "ABILITY_PHEROMONES_NAME"
        desc "ABILITY_PHEROMONES_DESC"
        class Hunter
    }

    graphics {
        projectile CupidsArrowProjectile
        animation throwArrow
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 0
        effects {
            Charmed 1
            Conditional_Enemy {
                TakeExtraTurn 1
            }
        }
    }
}
```

---

### `Pheromones2`
**Name:** Pheromones  
**Description:** Inflict Charm on a unit. It takes an extra turn immediately.  
**Source:** `hunter_abilities.gon`  

```
Pheromones2 {
    template lobbed_attack
    
    meta {
        name "ABILITY_PHEROMONES_NAME"
        desc "ABILITY_PHEROMONES2_DESC"
        class Hunter
    }

    graphics {
        animation throwArrow
        projectile CupidsArrowProjectile
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        damage 0
        effects {
            Charmed 1
            TakeExtraTurn 1
        }
    }
}
```

---

### `SpawnTomTomFriend`
**Name:** Call of the Wild  
**Description:** Spawn a charmed Tom Tom.  
**Source:** `hunter_abilities.gon`  

```
SpawnTomTomFriend {
    template spawn

    meta {
        name "ABILITY_CALLOFTHEWILD_NAME"
        desc "ABILITY_CALLOFTHEWILD_DESC"
        class Hunter
    }

    tags [summon]
    
    graphics {
        lob true
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 9
    }
    
    target {
        min_range 1
        max_range 1
    }

    spawn {
        object CharmedTomTom
    }
}
```

---

### `SpawnTomTomFriend2`
**Description:** Spawn a charmed Tom Tom on any tile.  
**Source:** `hunter_abilities.gon`  

```
SpawnTomTomFriend2 {//todo needs a buff
    variant_of SpawnTomTomFriend

    meta {
        desc "ABILITY_CALLOFTHEWILD2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `ScoutMe`
**Name:** Scout Me  
**Description:** Until next turn, allied cats gain a bonus ability that can let you shoot a tile of their choice.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
ScoutMe {
    template self_buff
    
    meta {
        name "ABILITY_SCOUTME_NAME"
        desc "ABILITY_SCOUTME_DESC"
        class Hunter
    }
	
    graphics {
        animation ColorlessStartTurn
    }

    cost {
        cantrip true
        mana 7
    }
    
    damage_instance {
        effects {
            ShootHereReceiver 1
            TeamBonusAbility ShootHere
        }
    }
}
```

---

### `ScoutMe2`
**Description:** Until next turn, allied cats gain a bonus ability that can let you shoot a tile of their choice.
\[s:.7\](Castable once per turn. This spell costs 0 mana.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
ScoutMe2 {
    variant_of ScoutMe
    
    meta {
        desc "ABILITY_SCOUTME2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `ShootHere`
**Name:** Shoot Here!  
**Description:** Instructs your friend to shoot an adjacent tile!
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
ShootHere {
    template targeted_status

    meta {
        name "ABILITY_SHOOTHERE_NAME"
        desc "ABILITY_SHOOTHERE_DESC"
        class Hunter
    }

    graphics {
        animation pointout
    }

    cost {
        cantrip true
        mana 0
    }

    target {
        max_range 1
        min_range 1
    }

    damage_instance {
        effects {
            ShootHereCommand 1
        }
    }
}
```

---

### `CraftArrow`
**Name:** Craft Arrow  
**Description:** Collect an adjacent pickup and gain +1 Bonus Attack instead of its normal effects.  
**Source:** `hunter_abilities.gon`  

```
CraftArrow {
    template targeted_status
    
    meta {
        name "ABILITY_CRAFTARROW_NAME"
        desc "ABILITY_CRAFTARROW_DESC"
        class Hunter
        type_icon "misc"
    }

    graphics {
		animation Quiver
    }

    cost {
        infcantrip true
        mana 2
    }

    target {
        max_range 1
        
        restrictions must_have_tag
        target_requires_tag pickup
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            CollectsPickupsWithAltEffects {
                Quivered 1
            }
        }
    }
}
```

---

### `CraftArrow2`
**Description:** Collect all pickups within two tiles of you. Gain +1 Bonus Attack for each pickup instead of their normal effects.
\[s:.7\](This spell costs 1 mana.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
CraftArrow2 {
    variant_of CraftArrow
    
    meta {
        desc "ABILITY_CRAFTARROW2_DESC"
    }

    target {
        target_mode none
        max_aoe 2
        restrictions aoe_must_exist
        aoe_restrictions must_have_tag
    }

    cost {
        mana 1
    }
}
```

---

### `CharmTrap`
**Name:** Charm Trap  
**Description:** Spawn a trap that deals damage and inflicts Charm 1.  
**Source:** `hunter_abilities.gon`  

```
CharmTrap {
    template lobbed_attack

    keyword_tooltips {Charmed 1}
    
    meta {
        name "ABILITY_CHARMTRAP_NAME"
        desc "ABILITY_CHARMTRAP_DESC"
        class Hunter
        type_icon "misc"
    }

    graphics {
        projectile CharmTrap
        animation throwobject
        use_rotation false
    }

    cost {
        mana 6
        infcantrip true
    }

    target {
        min_range 1
        max_range 5

        restrictions must_be_empty
    }

    damage_instance {
        damage 2
        ai_base_score 10
        custom_additional_ai_weight tile_has_no_known_traps
        
        effects {
            SpawnCustomTrap CharmTrap
            Charmed 1
            Immobile 0 // immobile 0 is just "cancel movement"
        }
    }
}
```

---

### `CharmTrap2`
**Description:** Spawn a trap that deals damage and inflicts Charm 1.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
CharmTrap2 {
    variant_of CharmTrap

    meta {
        desc "ABILITY_CHARMTRAP2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `BounceShot`
**Name:** Bounce Shot  
**Description:** Shoot a projectile that bounces everything adjacent to it back 3 tiles.  
**Source:** `hunter_abilities.gon`  

```
BounceShot {
    template spell
    
    meta {
        name "ABILITY_BOUNCESHOT_NAME"
        desc "ABILITY_BOUNCESHOT_DESC"
        class Hunter
    }

    graphics {
        animation throwArrow
        area_particle none
        use_projectile true
		particle none
		projectile bounceshot
    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 1
        min_aoe 1
        min_range 0
        max_range 5+bonus_range
    }
    
    damage_instance {
        damage 0
        type spell

        effects {
            KnockUpAndAway {
                distance 3
                stacks 1
            }
        }
    }
}
```

---

### `BounceShot2`
**Description:** Shoot a projectile that bounces everything adjacent to it back 3 tiles. They take 5 damage if they collide with something.  
**Source:** `hunter_abilities.gon`  

```
BounceShot2 {
    variant_of BounceShot

    meta {
        desc "ABILITY_BOUNCESHOT2_DESC"
    }

    damage_instance {
        effects {
            KnockUpAndAway {
                stacks 5
            }
        }
    }
}
```

---

### `Picnic`
**Name:** Picnic  
**Description:** You and adjacent units each heal 5 HP.  
**Source:** `hunter_abilities.gon`  

```
Picnic {
    template spell

    meta {
        name "ABILITY_PICNIC_NAME"
        desc "ABILITY_PICNIC_DESC"
        class Hunter
    }

    graphics {
        affected_particle HealSmall
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        target_mode none
        max_aoe 1
    }
    
    damage_instance {
        heal 5
    }
}
```

---

### `Picnic2`
**Description:** You and adjacent units each heal 5 HP and gain +1 Damage.  
**Source:** `hunter_abilities.gon`  

```
Picnic2 {
    variant_of Picnic

    meta {
        desc "ABILITY_PICNIC2_DESC"
    }

    damage_instance {
        heal 5

        effects {
            DamageUp 1
        }
    }
}
```

---

### `SoothingShot`
**Name:** Soothing Shot  
**Description:** A ranged shot that heals and inflicts Charmed 1.  
**Source:** `hunter_abilities.gon`  

```
SoothingShot {
    template lobbed_attack
    
    meta {
        name "ABILITY_SOOTHINGSHOT_NAME"
        desc "ABILITY_SOOTHINGSHOT_DESC"
        class Hunter
    }

    graphics {
        projectile CupidsArrowProjectile
        animation throwArrow
		particle CharmedOverlay
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        heal 10+bonus_ranged_damage

        effects {
            Charmed 1
        }
    }
}
```

---

### `SoothingShot2`
**Name:** Soothing Shot  
**Description:** A ranged shot that heals and inflicts Charmed 2.
Against allies this cleanses debuffs and inflicts Charmed 1 instead.  
**Source:** `hunter_abilities.gon`  

```
SoothingShot2 {
    template lobbed_attack
    
    meta {
        name "ABILITY_SOOTHINGSHOT_NAME"
        desc "ABILITY_SOOTHINGSHOT2_DESC"
        class Hunter
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        heal 10+bonus_ranged_damage

        effects {
            Conditional_Ally {
                Cleanse 0
                Charmed 1
            } Else {
                Charmed 2
            }
        }
    }
}
```

---

### `Vivisect`
**Name:** Vivisect  
**Description:** A melee attack that spawns a baited bear trap if it kills a unit or destroys a body.  
**Source:** `hunter_abilities.gon`  

```
Vivisect {
    template melee_attack
    
    meta {
        name "ABILITY_VIVISECT_NAME"
        desc "ABILITY_VIVISECT_DESC"
        class Hunter
    }

    graphics {
        animation sliceOpen
    }

    cost {
        infcantrip true
        mana 4
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        
        effects {
            Conditional_DestructibleCorpse {
                VaporizeCorpse 1

                ApplyToTile {
                    ObjectOnHit Bait
                    SpawnBearTrap 1
                }
            } Else {
                SpawnBearTrapIfHitKills 1
                SpawnThingIfHitKills Bait
            }
        }
    }
}
```

---

### `Vivisect2`
**Name:** Vivisect  
**Description:** A lobbed attack that spawns a baited bear trap if it kills a unit or destroys a body.  
**Source:** `hunter_abilities.gon`  

```
Vivisect2 {
    template lobbed_attack
    
    meta {
        name "ABILITY_VIVISECT_NAME"
        desc "ABILITY_VIVISECT2_DESC"
        class Hunter
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 1
        max_range 5+bonus_range
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        
        effects {
            Conditional_DestructibleCorpse {
                VaporizeCorpse 1

                ApplyToTile {
                    ObjectOnHit Bait
                    SpawnBearTrap 1
                }
            } Else {
                SpawnBearTrapIfHitKills 1
                SpawnThingIfHitKills Bait
            }
        }
    }
}
```

---

### `PoisonLace`
**Name:** Poison Lace  
**Description:** Give yourself or an adjacent unit +1 Poison Lace.  
**Source:** `hunter_abilities.gon`  

```
PoisonLace {
    template targeted_status
    
    meta {
        name "ABILITY_POISONLACE_NAME"
        desc "ABILITY_POISONLACE_DESC"
        class Hunter
        type_icon "buff"
    }

    graphics {
    }

    cost {
        mana 5
        infcantrip true
    }

    target {
        min_range 0
        max_range 1
        max_aoe 0
    }

    damage_instance {
        effects {
            PoisonLace 1
        }
    }
}
```

---

### `PoisonLace2`
**Description:** Give yourself or any other unit +1 Poison Lace.  
**Source:** `hunter_abilities.gon`  

```
PoisonLace2 {
    variant_of PoisonLace

    meta {
        desc "ABILITY_POISONLACE2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `SlopThePigs`
**Name:** Slop the Pigs  
**Description:** Each familiar in an area gains All Stats Up and heals 4 HP. Other units in the area gain +1 [img:con] and heal 2 HP.  
**Source:** `hunter_abilities.gon`  

```
SlopThePigs {
    template lobbed_attack
    
    meta {
        name "ABILITY_SLOPTHEPIGS_NAME"
        desc "ABILITY_SLOPTHEPIGS_DESC"
        class Hunter
    }
    graphics {
        animation throwobject
		projectile Foodball
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 5+bonus_range
        max_aoe 1
    }

    damage_instance {
        heal 2
        
        effects {
            Conditional_Familiar {
                BonusDamage -2
                AllStatsUp 1
            } Else {
                ConstitutionUp 1
            }
        }
    }
}
```

---

### `SlopThePigs2`
**Description:** Each familiar in an area gains All Stats Up and heals 4 HP. Other units in the area gain +1 [img:con] and heal 2 HP.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `hunter_abilities.gon`  

```
SlopThePigs2 {
    variant_of SlopThePigs

    meta {
        desc "ABILITY_SLOPTHEPIGS2_DESC"
    }

    cost {
        mana 5
    }

    target {
        max_aoe 2
    }
}
```

---

### `SpiderInjector`
**Name:** Egg Sac Trap  
**Description:** Spawn a spider egg trap that inflicts Infested 4.  
**Source:** `hunter_abilities.gon`  

```
SpiderInjector {
    template lobbed_attack
    
    meta {
        name "ABILITY_EGGSACTRAP_NAME"
        desc "ABILITY_EGGSACTRAP_DESC"
        class Hunter
        type_icon "misc"
    }

    graphics {
        animation throwobject
        projectile EggSackTrap
        use_rotation false
    }

    cost {
        mana 4
        infcantrip true
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
            SpawnCustomTrap EggSackTrap
            SpiderInfested 4
        }
    }
}
```

---

### `SpiderInjector2`
**Description:** Spawn a spider egg trap that deals damage and inflicts Infested 4.  
**Source:** `hunter_abilities.gon`  

```
SpiderInjector2 {
    variant_of SpiderInjector

    meta {
        desc "ABILITY_EGGSACTRAP2_DESC"
    }

    damage_instance {
        damage 4
    }
}
```

---

### `PersistentHunt`
**Name:** Persistent Hunt  
**Description:** Inflict Marked 5 on a unit. 
RELOAD: Kill an enemy.  
**Source:** `hunter_abilities.gon`  

```
PersistentHunt {
    template targeted_status

    meta {
        name "ABILITY_PERSISTENTHUNT_NAME"
        desc "ABILITY_PERSISTENTHUNT_DESC"
        class Hunter
    }

    graphics {
        affected_particle TakeAim
        animation pointout
    }
    
    cost {
        mana 0
        requires_reload true
    }
    
    bonus_passives {
        ReloadOnKillEnemy 1
    }

    target {
        min_range 3
        max_range 5+bonus_range
    }

    damage_instance {
        effects {
            Marked 5
        }
    }
}
```

---

### `PersistentHunt2`
**Description:** Inflict Marked 5 on a unit.
RELOAD: Kill an enemy.
This spell starts reloaded.  
**Source:** `hunter_abilities.gon`  

```
PersistentHunt2 {
    variant_of PersistentHunt

    meta {
        desc "ABILITY_PERSISTENTHUNT2_DESC"
    }

    cost {
        start_reloaded true
    }
}
```

---

### `Bunker`
**Name:** Hedge In  
**Description:** Spawn bear traps on each adjacent tile.  
**Source:** `hunter_abilities.gon`  

```
Bunker {
    template lobbed_attack
    
    meta {
        name "ABILITY_HEDGEIN_NAME"
        desc "ABILITY_HEDGEIN_DESC"
        class Hunter
        type_icon "misc"
    }

    graphics {
        projectile DamageTrap
        use_rotation false
        animation throwobject
    }

    cost {
        mana 4
        infcantrip true
    }

    target {
        target_mode none
        min_aoe 1
        max_aoe 1

        aoe_restrictions must_be_empty
        low_gravity_boostable false
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

### `Bunker2`
**Description:** Spawn bear traps on each tile exactly 2 tiles away.  
**Source:** `hunter_abilities.gon`  

```
Bunker2 {
    variant_of Bunker

    meta {
        desc "ABILITY_HEDGEIN2_DESC"
    }

    target {
        min_aoe 2
        max_aoe 2
    }
}
```

---

## File: `jester_abilities.gon`

### `SmartMetronome`
**Name:** Smart Metronome  
**Description:** Cast any random spell. The spell is usually good.  
**Source:** `jester_abilities.gon`  

```
SmartMetronome {
    template self_buff
    
    meta {
        name "ABILITY_SMARTMETRONOME_NAME"
        desc "ABILITY_SMARTMETRONOME_DESC"
        class Jester
        type_icon "unknown"
    }
	
    graphics {
		animation metronome
    }
    

    tags [musical]

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        effects {
            SmartMetronome 20
        }
    }
}
```

---

### `SmartMetronome2`
**Description:** Cast any random upgraded spell. The spell is usually good.  
**Source:** `jester_abilities.gon`  

```
SmartMetronome2 {
    variant_of SmartMetronome

    meta {
        desc "ABILITY_SMARTMETRONOME2_DESC"
    }

    damage_instance {
        effects {
            SmartMetronome {
                stacks 20
                upgraded true
            }
        }
    }
}
```

---

### `RNGCannon`
**Name:** RNG Cannon  
**Description:** Deals a random amount of damage. Requires line of sight  
**Source:** `jester_abilities.gon`  

```
RNGCannon {
    template spell

    meta {
        name "ABILITY_RNGCANNON_NAME"
        desc "ABILITY_RNGCANNON_DESC"
        class Jester

        type_icon magic
        icon_shell_frame attack
        icon_damage_display "?"
    }

    graphics {
        particle BigMagicMissileBlast
		animation hadouken
        use_projectile true
        projectile MagicMissileProjectile
        lob_height 0
        speed 20
    }
    
    cost {
        infcantrip true
        mana 10
    }
    
    target {
        max_aoe 0
        max_range 5
        restrictions must_have_line_of_sight
    }

    damage_instance {
        damage 0
        show_damage_on_0 true

        effects {
            RNGCannonRandomDamage 100
        }
    }
}
```

---

### `RNGCannon2`
**Description:** Deals a random amount of damage and inflicts random debuffs. Requires line of sight  
**Source:** `jester_abilities.gon`  

```
RNGCannon2 {
    variant_of RNGCannon
    keyword_tooltips {}

    meta {
        desc "ABILITY_RNGCANNON2_DESC"
    }

    damage_instance {
        effects {
            RandomStatusFromPool {
                Poison 1
                Burn 1
                Bleed 1
                Blind 1
                Bruise 1
                Stun 1
                Immobile 1
                Freeze 1
                Weakness 1
                Petrify 1
                MagicWeakness 1
                Marked 1
                Sleep 1
                Charmed 1
                Slow 1
                Madness 1
                Fear 1
                Confusion 1
                Tarred 1
                Rot 1
            }

            Poison [1 .1]
            Burn [1 .1]
            Bleed [1 .1]
            Blind [1 .1]
            Bruise [1 .1]
            Stun [1 .1]
            Immobile [1 .1]
            Freeze [1 .1]
            Weakness [1 .1]
            Petrify [1 .1]
            MagicWeakness [1 .1]
            Marked [1 .1]
            Sleep [1 .1]
            Charmed [1 .1]
            Slow [1 .1]
            Madness [1 .1]
            Fear [1 .1]
            Confusion [1 .1]
            Tarred [1 .1]
            Rot [1 .1]

            Poison [1 .1]
            Burn [1 .1]
            Bleed [1 .1]
            Blind [1 .1]
            Bruise [1 .1]
            Stun [1 .1]
            Immobile [1 .1]
            Freeze [1 .1]
            Weakness [1 .1]
            Petrify [1 .1]
            MagicWeakness [1 .1]
            Marked [1 .1]
            Sleep [1 .1]
            Charmed [1 .1]
            Slow [1 .1]
            Madness [1 .1]
            Fear [1 .1]
            Confusion [1 .1]
            Tarred [1 .1]
            Rot [1 .1]
        }
    }
}
```

---

### `Bump`
**Name:** Bump  
**Description:** Displace a target unit to a random location.  
**Source:** `jester_abilities.gon`  

```
Bump {
    template targeted_status

    meta {
        name "ABILITY_BUMP_NAME"
        desc "ABILITY_BUMP_DESC"
        class Jester
        type_icon "movement"
    }

    graphics {
        animation earthquakeSlam
        particle Earthquake
    }

    cost {
        mana 1
        infcantrip true
    }

    target {
        min_range 0
        max_range 20
        range_excludes_self false
        knockback_mode none
        restrictions aoe_must_be_displaceable
    }

    damage_instance {
        damage 0

        effects {
            RandomDistanceDisplace 20
        }

        elements [
            Earth
        ]
    }
}
```

---

### `Bump2`
**Description:** Displace a target unit to a random location. If its an enemy, deal 1 damage to it.  
**Source:** `jester_abilities.gon`  

```
Bump2 {
    variant_of Bump

    meta {
        desc "ABILITY_BUMP2_DESC"
    }

    damage_instance {
        raw_damage 1

        effects {
            Conditional_Enemy {
            } Else {
                OverrideDamage 0
            }
        }
    }
}
```

---

### `PowerUp`
**Name:** Power Up  
**Description:** Spend all of your mana and gain that many random buffs.  
**Source:** `jester_abilities.gon`  

```
PowerUp {
    template self_buff
    keyword_tooltips {}
    
    meta {
        name "ABILITY_POWERUP_NAME"
        desc "ABILITY_POWERUP_DESC"
        class Jester
    }

    graphics {
		animation floatingmagic
		particle fx_statup
    }
    
    cost {
        mana X
        infcantrip true
        X_cant_be_zero true
        disallow_cost_modification true
    }

    target {
        X_is current_mana
    }
    
    damage_instance {
        effects {
            ApplyMultipleTimes {
                stacks X

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
        }
    }
}
```

---

### `PowerUp2`
**Description:** Spend all of your mana and give that many random buffs to yourself or another unit.  
**Source:** `jester_abilities.gon`  

```
PowerUp2 {
    variant_of PowerUp

    target {
        target_mode tile
        min_range 0
        max_range 20
    }

    meta {
        desc "ABILITY_POWERUP2_DESC"
    }
}
```

---

## File: `mage_abilities.gon`

### `Surf`
**Name:** Surf  
**Description:** A water spell that deals damage and knockback in a large area.  
**Source:** `mage_abilities.gon`  

```
Surf {
    template spell

    meta {
        name "ABILITY_SURF_NAME"
        desc "ABILITY_SURF_DESC"
        class Mage
    }

    graphics {
        particle Wave

        visual_delay_but_simultaneous_damage 20
        delay 10
        animation majormagic
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        max_aoe 2
        max_range 4
    }
    
    damage_instance {
        damage 3
        knockback 2

        elements [
            Water
        ]
    }
}
```

---

### `Surf2`
**Description:** A water spell that deals more damage and knockback in a larger area.  
**Source:** `mage_abilities.gon`  

```
Surf2 {
    variant_of Surf

    meta {
        desc "ABILITY_SURF2_DESC"
    }

    target {
        max_aoe 3
        max_range 6
    }
    
    damage_instance {
        damage 5
        
        elements [
            Water
        ]
    }
}
```

---

### `Bolt`
**Name:** Bolt  
**Description:** A lightning bolt that has a 25% chance to Stun.  
**Source:** `mage_abilities.gon`  

```
Bolt {
    template spell

    meta {
        name "ABILITY_BOLT_NAME"
        desc "ABILITY_BOLT_DESC"
        class Mage
    }

    graphics {
        particle Bolt
        animation castspell
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        max_aoe 0
        max_range 5
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

### `Bolt2`
**Description:** A stronger lightning bolt that has a 50% chance to Stun.  
**Source:** `mage_abilities.gon`  

```
Bolt2 {
    variant_of Bolt

    meta {
        desc "ABILITY_BOLT2_DESC"
    }

    damage_instance {
        damage 6

        effects {
            Stun [1, .5]
        }
    }
}
```

---

### `Fireball`
**Name:** Fire Blast  
**Description:** A fireblast that inflicts Burn 2 in an area.  
**Source:** `mage_abilities.gon`  

```
Fireball {
    template spell

    meta {
        name "ABILITY_FIREBLAST_NAME"
        desc "ABILITY_FIREBLAST_DESC"
        class Mage
    }

    graphics {
        center_particle FireBlastMushroom
        area_particle FireBlastSmall
        delay 5
        palette 6
        animation castspell
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        max_aoe 1
        max_range 5
    }
    
    damage_instance {
        damage 3
        
        effects {
            Burn 2
        }
        
        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `Fireball2`
**Description:** A more damaging fireblast that inflicts Burn 3 in an area.  
**Source:** `mage_abilities.gon`  

```
Fireball2 {
    variant_of Fireball

    meta {
        desc "ABILITY_FIREBLAST2_DESC"
    }

    damage_instance {
        damage 5

        effects {
            Burn 3
        }
    }
}
```

---

### `FreezeRay`
**Name:** Frost Blast  
**Description:** Shoot a blast of ice in a line that freezes the first unit it hits.  
**Source:** `mage_abilities.gon`  

```
FreezeRay {
    template spell

    meta {
        name "ABILITY_FROSTBLAST_NAME"
        desc "ABILITY_FROSTBLAST_DESC"
        class Mage
        type_icon "magic"
    }

    graphics {
		animation mouthbeam
        particle IceBlast
        delay 10
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        target_mode direction
        aoe_mode line
        
        max_aoe 5
        
        aoe_considers_character_size true
        aoe_excludes_self true
        knockback_mode character_to_tile
        aoe_restrictions must_have_line_of_sight_unpurgable
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

### `FreezeRay2`
**Description:** Shoot a blast of ice in a line that freezes every unit it hits.  
**Source:** `mage_abilities.gon`  

```
FreezeRay2 {
    variant_of FreezeRay

    meta {
        desc "ABILITY_FROSTBLAST2_DESC"
    }

    target {
        aoe_restrictions none
    }
}
```

---

### `Blast`
**Name:** Energy Blast  
**Description:** A high damage spell that hits a single target.  
**Source:** `mage_abilities.gon`  

```
Blast {
    template spell

    meta {
        name "ABILITY_ENERGYBLAST_NAME"
        desc "ABILITY_ENERGYBLAST_DESC"
        class Mage
    }

    graphics {
        particle BigMagicMissileBlast
		animation createmagic
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        max_aoe 0
        max_range 3
    }
    
    damage_instance {
        damage 10
    }
}
```

---

### `Blast2`
**Description:** A high damage spell that hits a single target and deals extra damage equal to your [img:int].  
**Source:** `mage_abilities.gon`  

```
Blast2 {
    variant_of Blast

    meta {
        desc "ABILITY_ENERGYBLAST2_DESC"
    }

    damage_instance {
        damage "10+int"
    }
}
```

---

### `MagicMissile`
**Name:** Magic Missile  
**Description:** Shoot an infinite-range projectile that can't miss.  
**Source:** `mage_abilities.gon`  

```
MagicMissile {
    template spell

    meta {
        name "ABILITY_MAGICMISSILE_NAME"
        desc "ABILITY_MAGICMISSILE_DESC"
        class Mage
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
        infcantrip true
        mana 5
    }
    
    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 3
        cant_miss true
    }
}
```

---

### `MagicMissile2`
**Description:** Shoot an infinite-range projectile that can't miss. Emit 3 Sparkles.  
**Source:** `mage_abilities.gon`  

```
MagicMissile2 {
    variant_of MagicMissile

    meta {
        desc "ABILITY_MAGICMISSILE2_DESC"
    }

    self_damage {
        effects {
            RandomMagicMissile 1
            RandomMagicMissile 1
            RandomMagicMissile 1
        }
    }
}
```

---

### `WallOfFire`
**Name:** Wall of Fire  
**Description:** A fire spell that inflicts Burn 1 and spawns fires in a perpendicular line.  
**Source:** `mage_abilities.gon`  

```
WallOfFire {
    template spell

    meta {
        name "ABILITY_WALLOFFIRE_NAME"
        desc "ABILITY_WALLOFFIRE_DESC"
        class Mage
        type_icon "magic"
    }

    graphics {
        particle FireSpin
        palette 6
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        range_mode cross
        max_range 10
        
        aoe_mode perpline
        min_aoe -10
        max_aoe 10
    }
    
    damage_instance {
        damage 0
        
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

### `WallOfFire2`
**Description:** A fire spell that damages, inflicts Burn 3 and spawns fires in a perpendicular line.  
**Source:** `mage_abilities.gon`  

```
WallOfFire2 {
    variant_of WallOfFire

    meta {
        desc "ABILITY_WALLOFFIRE2_DESC"
    }

    damage_instance {
        damage 2
        effects {
            Burn 3
        }
    }
}
```

---

### `HyperBeam`
**Name:** Hyper Beam  
**Description:** Target a tile. At the start of your next turn, unleash an extremely high damage mega beam on that tile.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
HyperBeam {
    template spell

    meta {
        name "ABILITY_HYPERBEAM_NAME"
        desc "ABILITY_HYPERBEAM_DESC"
        class Mage
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
        mana 3
    }
    
    target {
        delayed_trigger true
        max_aoe 0
        max_range 6
    }
    
    damage_instance {
        damage 25
    }
}
```

---

### `HyperBeam2`
**Description:** Target a tile. At the start of your next turn, unleash an extremely high damage mega beam on that tile.  
**Source:** `mage_abilities.gon`  

```
HyperBeam2 {
    variant_of HyperBeam

    meta {
        desc "ABILITY_HYPERBEAM2_DESC"
    }

    cost {
        infcantrip true
    }
}
```

---

### `MeteorStorm`
**Name:** Meteor Storm  
**Description:** Summon meteors that hit random tiles in a large area. These meteors have a chance to stun, spawn fires, or leave rocks behind.  
**Source:** `mage_abilities.gon`  

```
MeteorStorm {
    template spell
    
    meta {
        name "ABILITY_METEORSTORM_NAME"
        desc "ABILITY_METEORSTORM_DESC"
        class Mage
    }

    graphics {
        particle MeteorFall
		animation floatingmagic
        random_delay [0, 120]
    }

    cost {
        infcantrip true
        mana 10
    }

    target {
        max_aoe 3
        max_range 5+level

        aoe_chance .4+.2*level
        knockback_mode zero

        can_multihit true
    }

    damage_instance {
        damage 10

        effects {
            Stun [1, .10+.1*level]
            SpawnFlames [1, .20+.1*level]
            BounceRock [1 .2]
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `MeteorStorm2`
**Description:** Summon meteors that hit random tiles in a larger area. These meteors have a chance to stun, spawn fires, or leave rocks behind.  
**Source:** `mage_abilities.gon`  

```
MeteorStorm2 {
    variant_of MeteorStorm

    meta {
        desc "ABILITY_METEORSTORM2_DESC"
    }

    target {
        max_aoe 4
    }
}
```

---

### `MegaBlast`
**Name:** Mega Blast  
**Description:** Deal high damage in a cone.  
**Source:** `mage_abilities.gon`  

```
MegaBlast {
    template spell

    meta {
        name "ABILITY_MEGABLAST_NAME"
        desc "ABILITY_MEGABLAST_DESC"
        class Mage
    }

    graphics {
		animation floatingmagic
        particle BigMagicMissileBlast
        delay 10
    }
    
    cost {
        infcantrip true
        mana 13
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 3

        aoe_considers_character_size true
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 15
    }
}
```

---

### `MegaBlast2`
**Description:** Deal high damage in a larger cone.  
**Source:** `mage_abilities.gon`  

```
MegaBlast2 {
    variant_of MegaBlast
    
    meta {
        desc "ABILITY_MEGABLAST2_DESC"
    }

    target {
        max_aoe 6
    }
}
```

---

### `Slow`
**Name:** Chill  
**Description:** Inflict Slow on a unit.  
**Source:** `mage_abilities.gon`  

```
Slow {
    template spell

    meta {
        name "ABILITY_CHILL_NAME"
        desc "ABILITY_CHILL_DESC"
        class Mage
        type_icon "debuff"
    }

    graphics {
        particle IcePoof
		animation blowFire
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_range 1
        max_range 5+2*level
        max_aoe 0
    }

    damage_instance {
        damage 0
        
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

### `Slow2`
**Description:** Inflict Slow on units in an area.  
**Source:** `mage_abilities.gon`  

```
Slow2 {
    variant_of Slow

    meta {
        desc "ABILITY_CHILL2_DESC"
    }

    target {
        max_aoe 1
    }
}
```

---

### `Enlarge`
**Name:** Enlarge  
**Description:** Get big.  
**Source:** `mage_abilities.gon`  

```
Enlarge { //REMOVED (spell is still here in case we want to add it back later, its just real fuckin annoying to make abilities when I constantly have to consider how they interact with Enlarge)
    template spell

    meta {
        name "ABILITY_ENLARGE_NAME"
        desc "ABILITY_ENLARGE_DESC"
        class Mage
    }

    graphics {
        particle none
    }
    
    cost {
        mana 10
        infcantrip true
        require_default_size true
    }
    
    target {
        range_mode custom
        custom_range [ [1, 1] [1, -1] [-1, 1] [-1, -1] ]

        aoe_mode corner_square
        restrictions aoe_must_be_displaceable
        aoe_excludes_self true
    }

    self_damage {
        type none
        damage 0

        effects {
            Enlarge 3
        }
    }

    damage_instance {
        damage 3
        cant_miss true

        effects {
            Displace 1
            IgnoreSelf 1
        }
    }
}
```

---

### `Enlarge2`
**Description:** Get big.  
**Source:** `mage_abilities.gon`  

```
Enlarge2 {
    variant_of Enlarge

    meta {
        desc "ABILITY_ENLARGE2_DESC"
    }

    cost {
        mana 1
    }
}
```

---

### `WindSlash`
**Name:** Wind Slash  
**Description:** A wind spell that hits an entire line with Knockback 1.  
**Source:** `mage_abilities.gon`  

```
WindSlash {
    template spell
    
    meta {
        name "ABILITY_WINDSLASH_NAME"
        desc "ABILITY_WINDSLASH_DESC"
        class Mage
    }

    graphics {
        particle fx_windSpell
		animation blowFire
    }

    cost {
        mana 4
        infcantrip true
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
        damage level
        knockback level

        elements [
            Wind
        ]
    }
}
```

---

### `WindSlash2`
**Description:** A wind spell that hits a wide line with Knockback 2.  
**Source:** `mage_abilities.gon`  

```
WindSlash2 {
    variant_of WindSlash

    meta {
        desc "ABILITY_WINDSLASH2_DESC"
    }

    target {
        aoe_mode custom
        custom_aoe [
                     [1, 1], [2, 1], [3, 1], [4, 1], [5, 1], [6, 1], [7, 1], [8, 1], [9, 1], [10, 1]
                     [1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0], [8, 0], [9, 0], [10, 0]
                     [1,-1], [2,-1], [3,-1], [4,-1], [5,-1], [6,-1], [7,-1], [8,-1], [9,-1], [10,-1]
                   ]
    }
}
```

---

### `Warp`
**Name:** Warp  
**Description:** Teleport diagonally any distance.  
**Source:** `mage_abilities.gon`  

```
Warp {
    template teleport
    
    meta {
        name "ABILITY_WARP_NAME"
        desc "ABILITY_WARP_DESC"
        animate_name true
        class Mage
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 20
        range_mode diagcross
        range_considers_character_size false
    }
}
```

---

### `Warp2`
**Description:** Teleport diagonally any distance.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
Warp2 {
    variant_of Warp

    meta {
        desc "ABILITY_WARP2_DESC"
    }

    cost {
        infcantrip true
        mana 2
    }
}
```

---

### `MageTeleport`
**Name:** Teleport  
**Description:** Teleport to any tile.  
**Source:** `mage_abilities.gon`  

```
MageTeleport {
    template teleport
    
    meta {
        name "ABILITY_TELEPORTMAGE_NAME"
        desc "ABILITY_TELEPORTMAGE_DESC"
        animate_name true
        class Mage
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        max_range 20
    }
}
```

---

### `MageTeleport2`
**Description:** Teleport to any tile.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
MageTeleport2 {
    variant_of MageTeleport

    meta {
        desc "ABILITY_TELEPORTMAGE2_DESC"
    }

    cost {
        infcantrip true
        mana 4
    }
}
```

---

### `MageSwap`
**Name:** Switch  
**Description:** Switch positions with any unit.  
**Source:** `mage_abilities.gon`  

```
MageSwap {
    template swap
    
    meta {
        name "ABILITY_SWITCH_NAME"
        desc "ABILITY_SWITCH_DESC"
        animate_name true
        class Mage
    }

    graphics {
    }

    cost {
        mana 5
        infcantrip true
    }

    target {
        max_range 20
    }
}
```

---

### `MageSwap2`
**Description:** Switch positions with any unit.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
MageSwap2 {
    variant_of MageSwap

    meta {
        desc "ABILITY_SWITCH2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `Absorb`
**Name:** Absorb  
**Description:** Spend all of your mana and heal that much HP.  
**Source:** `mage_abilities.gon`  

```
Absorb {
    template self_buff
    
    meta {
        name "ABILITY_ABSORB_NAME"
        desc "ABILITY_ABSORB_DESC"
        class Mage
        type_icon "heal"
    }

    graphics {
		animation bodypulse
		particle HealMed
    }
    
    cost {
        mana X
        infcantrip true
        X_cant_be_zero true
        disallow_cost_modification true
    }

    target {
        X_is current_mana
    }
    
    damage_instance {
        heal X

        elements [
            Holy
        ]
    }
}
```

---

### `Absorb2`
**Description:** Spend all of your mana and heal that much HP. Excess healing is converted into [img:shield].  
**Source:** `mage_abilities.gon`  

```
Absorb2 {
    variant_of Absorb

    meta {
        desc "ABILITY_ABSORB2_DESC"
    }

    damage_instance {
        effects {
            OverHealToShield 1
        }
    }
}
```

---

### `IceArmor`
**Name:** Ice Armor  
**Description:** -  
**Source:** `mage_abilities.gon`  

```
IceArmor { //CUT
    template self_buff
    
    meta {
        name "ABILITY_ICEARMOR_NAME"
        desc "ABILITY_ICEARMOR_DESC"
        class Mage
        type_icon "defense"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            IceArmor 1
        }
    }
}
```

---

### `IceArmor2`
**Description:** -  
**Source:** `mage_abilities.gon`  

```
IceArmor2 {
    variant_of IceArmor

    meta {
        desc "ABILITY_ICEARMOR2_DESC"
    }

    damage_instance {
        effects {
            NonStackingDivineShield 1
        }
    }
}
```

---

### `FireArmor`
**Name:** Fire Armor  
**Description:** -  
**Source:** `mage_abilities.gon`  

```
FireArmor { //CUT
    template self_buff
    
    meta {
        name "ABILITY_FIREARMOR_NAME"
        desc "ABILITY_FIREARMOR_DESC"
        class Mage
        type_icon "defense"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            FireArmor 1
        }
    }
}
```

---

### `FireArmor2`
**Name:** Fire Armor  
**Description:** -  
**Source:** `mage_abilities.gon`  

```
FireArmor2 {
    template self_buff
    
    meta {
        name "ABILITY_FIREARMOR_NAME"
        desc "ABILITY_FIREARMOR2_DESC"
        class Mage
        type_icon "defense"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            FireArmor2 1
            Shield 3
        }
    }
}
```

---

### `ManaMeld`
**Name:** Mana Meld  
**Description:** Give all of your mana to a unit in range 3.  
**Source:** `mage_abilities.gon`  

```
ManaMeld {
    template spell
    
    meta {
        name "ABILITY_MANAMELD_NAME"
        desc "ABILITY_MANAMELD_DESC"
        class Mage
        type_icon "misc"
    }

    graphics {
	    particle none
	    animation createmagic
    }
    
    cost {
        mana X
        infcantrip true
        X_cant_be_zero true
        disallow_cost_modification true
    }

    target {
        min_range 1
        max_range 3
        max_aoe 0
        X_is current_mana
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0
        effects {
            ManaGain X
        }
    }
}
```

---

### `ManaMeld2`
**Description:** Give all of your mana plus 2 to a unit.  
**Source:** `mage_abilities.gon`  

```
ManaMeld2 {
    variant_of ManaMeld

    meta {
        desc "ABILITY_MANAMELD2_DESC"
    }

    target {
        max_range 20
    }

    damage_instance {
        effects {
            ManaGain X+2
        }
    }
}
```

---

### `Inspire`
**Name:** Inspire  
**Description:** Give 2 mana to a unit.  
**Source:** `mage_abilities.gon`  

```
Inspire {
    template spell
    
    meta {
        name "ABILITY_INSPIRE_NAME"
        desc "ABILITY_INSPIRE_DESC"
        class Mage
        type_icon "misc"
    }

    graphics {
		particle none
    }
    
    cost {
        mana 3
        infcantrip true
    }

    target {
        min_range 1
        max_range 6
        max_aoe 0
    }
    
    damage_instance {
        damage 0
        effects {
            ManaGain 2
        }
    }
}
```

---

### `Inspire2`
**Description:** Give 4 mana to a unit.  
**Source:** `mage_abilities.gon`  

```
Inspire2 {
    variant_of Inspire

    meta {
        desc "ABILITY_INSPIRE2_DESC"
    }

    damage_instance {
        effects {
            ManaGain 4
        }
    }
}
```

---

### `Telefrag`
**Name:** Telefrag  
**Description:** Teleport onto a unit, dealing damage to yourself and that unit.  
**Source:** `mage_abilities.gon`  

```
Telefrag {
    template teleport
    
    meta {
        name "ABILITY_TELEFRAG_NAME"
        desc "ABILITY_TELEFRAG_DESC"
        animate_name true
        class Mage
        type_icon "magic"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 6
    }

    self_damage {
        damage 5
    }

    damage_instance {
        damage 5
        type spell
        makes_contact true

        effects {
            IgnoreSelf 1
        }
    }

    target {
        max_range 20
        restrictions [aoe_must_be_displaceable must_have_animate_character]
    }
}
```

---

### `Telefrag2`
**Description:** Teleport onto a unit, dealing damage to that unit.  
**Source:** `mage_abilities.gon`  

```
Telefrag2 {
    variant_of Telefrag

    meta {
        desc "ABILITY_TELEFRAG2_DESC"
    }

    self_damage {
        damage 0
    }

    damage_instance {
        damage 5
    }
}
```

---

### `ChaosTeleport`
**Name:** Chaos Teleport  
**Description:** Teleport to a random tile.  
**Source:** `mage_abilities.gon`  

```
ChaosTeleport {
    template teleport
    
    meta {
        name "ABILITY_CHAOSTELEPORT_NAME"
        desc "ABILITY_CHAOSTELEPORT_DESC"
        animate_name true
        class Mage
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 1
    }

    target {
        target_mode random_tile
        max_range 20
    }
}
```

---

### `ChaosTeleport2`
**Description:** Teleport to a random tile. Deal damage to units adjacent to the tile you teleport to.  
**Source:** `mage_abilities.gon`  

```
ChaosTeleport2 {
    variant_of ChaosTeleport

    meta {
        desc "ABILITY_CHAOSTELEPORT2_DESC"
    }

    self_damage {
        effects {
            SplashDamage 1
        }
    }
}
```

---

### `CryoHeal`
**Name:** Cryo-Heal  
**Description:** Heal and inflict Freeze 1 on a unit in range 3.  
**Source:** `mage_abilities.gon`  

```
CryoHeal {
    template spell
    
    meta {
        name "ABILITY_CRYOHEAL_NAME"
        desc "ABILITY_CRYOHEAL_DESC"
        class Mage
    }

    graphics {
        affected_particle HealMed
		particle IcePoof
        animation slowPawMagic
    }
    
    cost {
        infcantrip true
        mana 8
    }

    target {
        max_aoe 0
        min_range 0
        max_range 3
    }
    
    damage_instance {
        heal 10
        type spell

        effects {
            Freeze 1
        }

        elements [
            Ice
            Holy
        ]
    }
}
```

---

### `CryoHeal2`
**Description:** Heal and inflict Freeze 1 on any unit.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
CryoHeal2 {
    variant_of CryoHeal

    meta {
        desc "ABILITY_CRYOHEAL2_DESC"
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        max_aoe 0
        min_range 0
        max_range 20
    }
}
```

---

### `Gust`
**Name:** Gust  
**Description:** Knock back each unit adjacent to a chosen tile 1 space.  
**Source:** `mage_abilities.gon`  

```
Gust {
    template spell

    meta {
        name "ABILITY_GUST_NAME"
        desc "ABILITY_GUST_DESC"
        class Mage
        type_icon "magic"
    }

    graphics {
        particle fx_windSpell
	    animation blowFire
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_aoe 1
        max_aoe 1
        max_range 5
    }
    
    damage_instance {
        damage 0
        knockback 1
        
        elements [
            Wind
        ]
    }
}
```

---

### `Gust2`
**Description:** Knock back each unit adjacent to a chosen tile 3 spaces, at infinite range.  
**Source:** `mage_abilities.gon`  

```
Gust2 {
    variant_of Gust

    meta {
        desc "ABILITY_GUST2_DESC"
    }

    target {
        max_range 20
    }
    
    damage_instance {
        damage 0
        knockback 3
        
        elements [
            Wind
        ]
    }
}
```

---

### `Blizzard`
**Name:** Blizzard  
**Description:** Deal ice damage in a wide line with Knockback 1 that inflicts Freeze.  
**Source:** `mage_abilities.gon`  

```
Blizzard {
    template spell
    
    meta {
        name "ABILITY_BLIZZARD_NAME"
        desc "ABILITY_BLIZZARD_DESC"
        class Mage
    }

    graphics {
        particle IcePoof
        animation slowPawMagic
    }

    cost {
        mana 12
        infcantrip true
    }

    target {
        target_mode direction
        
        aoe_mode custom
        custom_aoe [
                     [1, 1], [2, 1], [3, 1], [4, 1], [5, 1], [6, 1], [7, 1], [8, 1], [9, 1], [10, 1]
                     [1, 0], [2, 0], [3, 0], [4, 0], [5, 0], [6, 0], [7, 0], [8, 0], [9, 0], [10, 0]
                     [1,-1], [2,-1], [3,-1], [4,-1], [5,-1], [6,-1], [7,-1], [8,-1], [9,-1], [10,-1]
                   ]
        
        aoe_considers_character_size true
        aoe_excludes_self true

        knockback_mode orientation
    }

    damage_instance {
        damage 16
        knockback 1

        effects {
            Freeze 1
        }

        elements [
            Wind
            Ice
        ]
    }
}
```

---

### `Blizzard2`
**Description:** Deal more ice damage in a wide line with Knockback 10 that inflicts Freeze.  
**Source:** `mage_abilities.gon`  

```
Blizzard2 {
    variant_of Blizzard

    meta {
        desc "ABILITY_BLIZZARD2_DESC"
    }

    damage_instance {
        damage 24
        knockback 10
    }
}
```

---

### `Inferno`
**Name:** Inferno  
**Description:** Deal fire damage and inflict Burn 8 to all units in a large circle around you.  
**Source:** `mage_abilities.gon`  

```
Inferno {
    template spell
    
    meta {
        name "ABILITY_INFERNO_NAME"
        desc "ABILITY_INFERNO_DESC"
        class Mage
    }

    graphics {
		animation floatingmagic
        particle FireBlastMedium
        palette 6
        delay 3
    }

    cost {
        mana 12
        infcantrip true
    }

    target {
        target_mode none
        
        aoe_mode circle
        max_aoe 2
        min_aoe 1
    }

    damage_instance {
        damage 8

        effects {
            Burn 8
        }

        elements [
            Fire
        ]
    }
}
```

---

### `Inferno2`
**Description:** Deal more fire damage and inflict Burn 10 to all units in a large circle around you.  
**Source:** `mage_abilities.gon`  

```
Inferno2 {
    variant_of Inferno

    meta {
        desc "ABILITY_INFERNO2_DESC"
    }

    damage_instance {
        damage 12

        effects {
            Burn 10
        }
    }
}
```

---

### `Thunderburst`
**Name:** Thunderburst  
**Description:** Shoot lightning bolts in eight directions with a 50% chance to Stun.  
**Source:** `mage_abilities.gon`  

```
Thunderburst {
    template spell
    
    meta {
        name "ABILITY_THUNDERBURST_NAME"
        desc "ABILITY_THUNDERBURST_DESC"
        class Mage
    }

    graphics {
        particle Bolt
        delay 5
    }

    cost {
        mana 12
        infcantrip true
    }

    target {
        target_mode none
        
        aoe_mode 8cross
        max_aoe 10
        min_aoe 1
    }

    damage_instance {
        damage 12

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

### `Thunderburst2`
**Description:** Shoot stronger lightning bolts in eight directions with a 100% chance to Stun.  
**Source:** `mage_abilities.gon`  

```
Thunderburst2 {
    variant_of Thunderburst

    meta {
        desc "ABILITY_THUNDERBURST2_DESC"
    }

    damage_instance {
        damage 16

        effects {
            Stun 1
        }
    }
}
```

---

### `DealWithTheDevil`
**Name:** Deal with the Devil  
**Description:** Injure yourself, then restore 15 mana.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
DealWithTheDevil {
    template self_buff
    
    meta {
        name "ABILITY_DEALWITHTHEDEVIL_NAME"
        desc "ABILITY_DEALWITHTHEDEVIL_DESC"
        class Mage
        type_icon "misc"
    }

    graphics {
        animation selfHarm
    }
    
    cost {
        cantrip true
        mana 0
        once_per_fight true
    }
    
    damage_instance {
        damage 0
        type spell_cost
        cant_miss true

        effects {
            RandomInjury 1
            ManaGain 15
        }
    }
}
```

---

### `DealWithTheDevil2`
**Name:** Deal with the Devil  
**Description:** Injure yourself, then restore all your mana.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
DealWithTheDevil2 {
    template self_buff
    
    meta {
        name "ABILITY_DEALWITHTHEDEVIL_NAME"
        desc "ABILITY_DEALWITHTHEDEVIL2_DESC"
        class Mage
        type_icon "misc"
    }

    graphics {
        animation selfHarm
    }
    
    cost {
        cantrip true
        mana 0
        once_per_fight true
    }
    
    damage_instance {
        damage 0
        type spell_cost
        cant_miss true

        effects {
            RandomInjury 1
            FillMana 1
        }
    }
}
```

---

### `ForbiddenFlame`
**Name:** Forbidden Flame  
**Description:** Damage and inflict Burn 7 on all enemies and light the map on fire. There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
ForbiddenFlame {
    template spell

    meta {
        name "ABILITY_FORBIDDENFLAME_NAME"
        desc "ABILITY_FORBIDDENFLAME_DESC"
        class Mage
    }

    graphics {
        particle FireBlastMedium
        palette 6
        delay 3
        animation floatingmagic
    }
    
    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions exclude_allies
    }

    self_damage {
        effects {
            Conditional_GoodRoll {
                odds 90%
                GainDisorderFromPool_PostCast forbidden_spell_consequences
            } Else {
                GainDisorderFromPool_PostCast forbidden_spell_consequences_crippling
            }
            Burn 4
        }
    }

    damage_instance {
        damage 7

        effects {
            Burn 7
        }
        
        elements [
            Fire
            Napalm
        ]
    }
}
```

---

### `ForbiddenFlame2`
**Description:** Heavily damage and inflict Burn 10 on all enemies and light the map on fire. There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
ForbiddenFlame2 {
    variant_of ForbiddenFlame

    meta {
         desc "ABILITY_FORBIDDENFLAME2_DESC"
    }

    damage_instance {
        damage 15

        effects {
            Burn 10
        }
    }
}
```

---

### `ForbiddenFlood`
**Name:** Forbidden Flood  
**Description:** Knock back and damage all enemies, then flood the entire map. There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
ForbiddenFlood {
    template spell

    meta {
        name "ABILITY_FORBIDDENFLOOD_NAME"
        desc "ABILITY_FORBIDDENFLOOD_DESC"
        class Mage
    }

    graphics {
        particle Wave
        animation attack

        visual_delay_but_simultaneous_damage 50
        delay_from_map_edge true
        delay 5
    }
    
    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }

    self_damage {
        effects {
            Conditional_GoodRoll {
                odds 90%
                GainDisorderFromPool_PostCast forbidden_spell_consequences
            } Else {
                GainDisorderFromPool_PostCast forbidden_spell_consequences_crippling
            }
        }
    }

    target {
        target_mode direction
        aoe_mode all
        aoe_considers_character_size false
        aoe_excludes_self false
        knockback_mode orientation
        prioritize_dont_change_direction true
    }

    damage_instance {
        damage 15
        knockback 10

        effects {
            ChangeTile WaterTile
            Conditional_Ally {
                KnockbackDamageImmuneUntilSettled 1
                OverrideDamage 0
            }
        }

        elements [
            Water
        ]
    }
}
```

---

### `ForbiddenFlood2`
**Description:** Knock back and damage all enemies, heal all allies, then flood the entire map. There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
ForbiddenFlood2 {
    variant_of ForbiddenFlood

    meta {
         desc "ABILITY_FORBIDDENFLOOD2_DESC"
    }

    damage_instance {
       damage 15
       knockback 10

       effects {
           Conditional_Ally {
               OverrideDamage -10
           }
       }
    }
}
```

---

### `WaterSphere`
**Name:** Whirlpool  
**Description:** Create a whirlpool that spins units and inflicts Confusion on them.  
**Source:** `mage_abilities.gon`  

```
WaterSphere {
    template spell

    meta {
        name "ABILITY_WATERSPHERE_NAME"
        desc "ABILITY_WATERSPHERE_DESC"
        class Mage
    }

    graphics {
        particle Wave
        animation majormagic
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        max_aoe 2
        max_range 4

        knockback_mode target_to_tile
        knockback_modifier rotate_cw
    }
    
    damage_instance {
        damage 0
        knockback 1

        effects {
            Confusion 1
            ChangeTile WaterTile_Current
            TurnRight 1
        }

        elements [
            Water
        ]
    }
}
```

---

### `WaterSphere2`
**Description:** Create a larger whirlpool that spins units and inflicts Confusion on them.  
**Source:** `mage_abilities.gon`  

```
WaterSphere2 {
    variant_of WaterSphere

    target {
        max_aoe 3
        max_range 6
    }

    meta {
        desc "ABILITY_WATERSPHERE2_DESC"
    }
}
```

---

### `ChainLightning`
**Name:** Chain Lightning  
**Description:** Shoot lightning that chains randomly to other nearby units up to 2 tiles away.  
**Source:** `mage_abilities.gon`  

```
ChainLightning {
    template spell

    meta {
        name "ABILITY_CHAINLIGHTNING_NAME"
        desc "ABILITY_CHAINLIGHTNING_DESC"
        class Mage
    }

    graphics {
        particle none
        use_projectile true
        projectile LightningBallProjectile
        lob_height 1
        speed 20
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        max_aoe 0
        max_range 4
    }
    
    damage_instance {
        damage 4
        
        effects {
            ArcLightning {
                stacks 100
                enemies_only false
                max_distance 2
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

### `ChainLightning2`
**Description:** Shoot lightning that chains randomly to other nearby enemies up to 3 tiles away.  
**Source:** `mage_abilities.gon`  

```
ChainLightning2 {
    variant_of ChainLightning

    meta {
        desc "ABILITY_CHAINLIGHTNING2_DESC"
    }

    damage_instance {
        damage 4
        
        effects {
            ArcLightning {
                stacks 100
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

### `Shatter`
**Name:** Shatter  
**Description:** A melee attack that instantly kills frozen units. If used on a boss, it instead removes Frozen to deal 15 damage and inflict Slow 2.  
**Source:** `mage_abilities.gon`  

```
Shatter {
    template melee_attack

    meta {
        name "ABILITY_SHATTER_NAME"
        desc "ABILITY_SHATTER_DESC"
        class Mage
    }

    graphics {
    }

    cost {
        mana 3
        infcantrip true
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage

        effects {
            Conditional_Boss {
                Conditional_HasStatus {
                    status Freeze
                    Slow 2
                }
            }
            Shatter 15
        }
    }
}
```

---

### `Shatter2`
**Name:** Shatter  
**Description:** A spell that instantly kills frozen units in an area. If used on a boss, it instead removes Frozen to deal 15 damage and inflict Slow 2.  
**Source:** `mage_abilities.gon`  

```
Shatter2 {
    template spell

    meta {
        name "ABILITY_SHATTER_NAME"
        desc "ABILITY_SHATTER2_DESC"
        class Mage
    }

    graphics {
		particle none
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        max_aoe 1
        max_range 3
    }
    
    damage_instance {
        damage 2
        
        effects {
            Conditional_Boss {
                Conditional_HasStatus {
                    status Freeze
                    Slow 2
                }
            }
            Shatter 15
        }
    }
}
```

---

### `ForbiddenFulmination`
**Name:** Forbidden Fulmination  
**Description:** Strike all enemies with lightning, inflicting Stun. There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
ForbiddenFulmination {
    template spell

    meta {
        name "ABILITY_FORBIDDENFULMINATION_NAME"
        desc "ABILITY_FORBIDDENFULMINATION_DESC"
        class Mage
    }

    graphics {
        particle Bolt
    }
    
    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions enemies_only
    }

    self_damage {
        effects {
            Conditional_GoodRoll {
                odds 90%
                GainDisorderFromPool_PostCast forbidden_spell_consequences
            } Else {
                GainDisorderFromPool_PostCast forbidden_spell_consequences_crippling
            }
        }
    }

    damage_instance {
        damage 10

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

### `ForbiddenFulmination2`
**Description:** Strike all enemies with lightning, inflicting Stun 2. There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
ForbiddenFulmination2 {
    variant_of ForbiddenFulmination

    meta {
        desc "ABILITY_FORBIDDENFULMINATION2_DESC"
    }

    damage_instance {
        effects {
            Stun 2
        }
    }
}
```

---

### `FireBolt`
**Name:** Firebolt  
**Description:** Cast a fire/electric spell that inflicts Burn 1 and has a 15% chance to inflict Stun in an X shaped area.  
**Source:** `mage_abilities.gon`  

```
FireBolt {
    template spell

    meta {
        name "ABILITY_FIREBOLT_NAME"
        desc "ABILITY_FIREBOLT_DESC"
        class Mage
    }

    graphics {
        particle Bolt
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        max_aoe 1
        max_range 5
        aoe_mode diagcross
    }
    
    damage_instance {
        damage 4
        
        effects {
            Burn 1
            Stun [1 .15]
        }
        
        elements [
            Fire
            Electric
        ]
    }
}
```

---

### `FireBolt2`
**Description:** Cast a fire/electric spell that inflicts Burn 2 and has a 30% chance to inflict Stun in an X shaped area.  
**Source:** `mage_abilities.gon`  

```
FireBolt2 {
    variant_of FireBolt

    meta {
        desc "ABILITY_FIREBOLT2_DESC"
    }

    target {
        max_aoe 2
    }

    damage_instance {
        damage 5
        
        effects {
            Burn 2
            Stun [1 .30]
        }
    }
}
```

---

### `IcicleTaser`
**Name:** Icicle Zapper  
**Description:** Shoot an ice/electric bolt in a straight line. It inflicts Slow 2, has a 25% chance to Stun and a 25% chance to Freeze.  
**Source:** `mage_abilities.gon`  

```
IcicleTaser {
    template straightshot_attack
    
    meta {
        name "ABILITY_ICICLETASER_NAME"
        desc "ABILITY_ICICLETASER_DESC"
        class Mage
    }

    graphics {
        animation throwobject
		projectile MagicSpikeProjectile
    }
    
    cost {
        infcantrip true
        mana 8
    }

    target {
        max_aoe 10
    }
    
    damage_instance {
        damage 4
        type spell

        effects {
            Slow 2
            Stun [1 .25]
            Freeze [1 .25]
        }

        elements [
            Ice
            Electric
        ]
    }
}
```

---

### `IcicleTaser2`
**Description:** Shoot 2 ice/electric bolts in a straight line. They inflict Slow 2, have a 25% chance to Stun and a 25% chance to Freeze.  
**Source:** `mage_abilities.gon`  

```
IcicleTaser2 {
    variant_of IcicleTaser

    meta {
        desc "ABILITY_ICICLETASER2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `FreezerBurn`
**Name:** Freezer Burn  
**Description:** Cast a fire/ice spell that inflicts Burn 2, Slow 2 and Knockback 2 on all units around you.  
**Source:** `mage_abilities.gon`  

```
FreezerBurn {
    template spell

    meta {
        name "ABILITY_FREEZERBURN_NAME"
        desc "ABILITY_FREEZERBURN_DESC"
        class Mage
    }

    graphics {
        particle IcePoof
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        target_mode none
        max_aoe 3
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 2
        knockback 2
        
        effects {
            Burn 2
            Slow 2
        }
        
        elements [
            Fire
            Ice
        ]
    }
}
```

---

### `FreezerBurn2`
**Description:** Cast a fire/ice spell that inflicts Burn 3, Slow 3 and Knockback 3 on all units around you in a larger area.  
**Source:** `mage_abilities.gon`  

```
FreezerBurn2 {
    variant_of FreezerBurn

    meta {
        desc "ABILITY_FREEZERBURN2_DESC"
    }

    target {
        max_aoe 4
    }

    damage_instance {
        damage 3
        
        effects {
            Burn 3
            Slow 3
        }
    }
}
```

---

### `Corrupt`
**Name:** Corrupt  
**Description:** Injure yourself, then gain +3 Magic Damage.  
**Source:** `mage_abilities.gon`  

```
Corrupt {
    template self_buff
    
    meta {
        name "ABILITY_CORRUPT_NAME"
        desc "ABILITY_CORRUPT_DESC"
        class Mage
    }

    graphics {
        animation selfHarm
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        damage 0
        type spell_cost
        cant_miss true

        effects {
            RandomInjury 1
            SpellDamageUp 3
        }
    }
}
```

---

### `Corrupt2`
**Description:** Injure yourself, then gain +3 Magic Damage and emit a Sparkle.  
**Source:** `mage_abilities.gon`  

```
Corrupt2 {
    variant_of Corrupt
    
    meta {
        desc "ABILITY_CORRUPT2_DESC"
    }
    
    damage_instance {
        effects {
            RandomMagicMissile 1
        }
    }
}
```

---

### `Jolt`
**Name:** Jolt  
**Description:** Shoot a lightning bolt that deals 1 damage and knocks the unit it hits 3 tiles in the direction it's facing.  
**Source:** `mage_abilities.gon`  

```
Jolt {
    template spell

    meta {
        name "ABILITY_JOLT_NAME"
        desc "ABILITY_JOLT_DESC"
        class Mage
    }

    graphics {
        particle Bolt
		animation castspell
    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 0
        min_range 1
        max_range 5
    }
    
    damage_instance {
        damage 1
        knockback 3
        
        effects {
            KnockbackDirectionIsFacingDirection 1
        }
        
        elements [
            Electric
        ]
    }
}
```

---

### `Jolt2`
**Description:** Shoot a lightning bolt that deals 2 damage and knocks the unit it hits 6 tiles in the direction it's facing.  
**Source:** `mage_abilities.gon`  

```
Jolt2 {
    variant_of Jolt

    meta {
        desc "ABILITY_JOLT2_DESC"
    }

    target {
        max_aoe 0
        max_range 20
    }

    damage_instance {
        damage 2
        knockback 6
    }
}
```

---

### `Smolder`
**Name:** Smolder  
**Description:** Inflict Burn 1 and +1 [img:spd] to a unit in range.  
**Source:** `mage_abilities.gon`  

```
Smolder {
    template spell

    meta {
        name "ABILITY_SMOLDER_NAME"
        desc "ABILITY_SMOLDER_DESC"
        class Mage
    }

    graphics {
        particle BurnTrigger
		animation castspell
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        max_aoe 0
        max_range 5
    }
    
    damage_instance {
        damage 0
        
        effects {
            Burn 1
            SpeedUp 1
        }
        
        elements [
            Fire
        ]
    }
}
```

---

### `Smolder2`
**Description:** Inflict Burn 1 and +1 [img:spd] to any unit.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
Smolder2 {
    variant_of Smolder

    meta {
        desc "ABILITY_SMOLDER2_DESC"
    }

    cost {
        mana 2
    }

    target {
        max_range 20
    }
}
```

---

### `FireSurge`
**Name:** Fire Surge  
**Description:** A fire spell that increases its range, area, damage, and Burn by 1 every turn.  
**Source:** `mage_abilities.gon`  

```
FireSurge {
    template spell

    meta {
        name "ABILITY_FIRESURGE_NAME"
        desc "ABILITY_FIRESURGE_DESC"
        class Mage
        type_icon "magic"
        icon_shell_frame attack
    }

    graphics {
        particle FireBlastSmall
    }
    
    cost {
        infcantrip true
        mana 5
    }

    bonus_passives {
        XIsRampAndReset 0
    }
    
    target {
        max_aoe "X/2"
        max_range X
        X_is turn_count
    }
    
    damage_instance {
        raw_damage X
        
        effects {
            Conditional_FormulaIsPositive {
                formula X
                Burn X
            }
        }
        
        elements [
            Fire
        ]
    }
}
```

---

### `FireSurge2`
**Description:** A fire spell that increases its range, area, damage, and Burn by 1 every turn. Starts stronger.  
**Source:** `mage_abilities.gon`  

```
FireSurge2 {
    variant_of FireSurge

    meta {
        desc "ABILITY_FIRESURGE2_DESC"
    }

    target {
        max_aoe "(X+1)/2"
        max_range X+1
        X_is turn_count
    }
    
    damage_instance {
        raw_damage X+1
        
        effects {
            Conditional_FormulaIsPositive {
                formula X+1
                Burn X+1
            }
        }
    }
}
```

---

### `IceSurge`
**Name:** Ice Surge  
**Description:** An ice spell that increases its range and Slow every turn. At 2 turns, it gains Immobilize 1. At 3 turns, it gains Freeze 1.
\[s:.7\](Current turns: {v0})\[/s\]  
**Source:** `mage_abilities.gon`  

```
IceSurge {
    template spell

    meta {
        name "ABILITY_ICESURGE_NAME"
        desc "ABILITY_ICESURGE_DESC"
        class Mage
        type_icon "magic"
        tooltip_values ["X"]
    }

    graphics {
        particle IcePoof
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_aoe 0
        max_range X
        X_is turn_count
    }
    
    damage_instance {
        raw_damage 0
        
        effects {
            Conditional_FormulaIsPositive {
                formula X
                Slow X
            }
            Conditional_FormulaIsPositive {
                formula X-1
                Immobile 1
            }
            Conditional_FormulaIsPositive {
                formula X-2
                Freeze 1
            }
        }

        
        elements [
            Ice
        ]
    }
}
```

---

### `IceSurge2`
**Description:** An ice spell that increases its range, damage, and Slow every turn. At 2 turns, it gains Immobilize 1. At 3 turns, it gains Freeze 1.
\[s:.7\](Current turns: {v0})\[/s\]  
**Source:** `mage_abilities.gon`  

```
IceSurge2 {
    variant_of IceSurge

    meta {
        desc "ABILITY_ICESURGE2_DESC"
    }

    damage_instance {
        raw_damage X
    }
}
```

---

### `LightningSurge`
**Name:** Lightning Surge  
**Description:** An electric spell that increases its range and damage by 2 every turn, and its stun chance by 10%.  
**Source:** `mage_abilities.gon`  

```
LightningSurge {
    template spell

    meta {
        name "ABILITY_LIGHTNINGSURGE_NAME"
        desc "ABILITY_LIGHTNINGSURGE_DESC"
        class Mage
        type_icon "magic"
        icon_shell_frame attack
        tooltip_values ["X"]
    }

    graphics {
        particle Bolt
		animation castspell
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        max_aoe 0
        max_range X*2
        X_is turn_count
    }
    
    damage_instance {
        raw_damage X*2
        
        effects {
            Stun [1 X*.1]
        }

        elements [
            Electric
        ]
    }
}
```

---

### `LightningSurge2`
**Description:** An electric spell that increases its range and damage by 3 every turn, and its stun chance by 10%.  
**Source:** `mage_abilities.gon`  

```
LightningSurge2 {
    variant_of LightningSurge

    meta {
        desc "ABILITY_LIGHTNINGSURGE2_DESC"
    }

    target {
        max_range X*3
    }

    damage_instance {
        raw_damage X*3
    }
}
```

---

### `Creshendo`
**Name:** Crescendo  
**Description:** This spell gains +1 damage, range and area, and -1 mana cost each time you cast a spell.
This spell resets after you cast it.  
**Source:** `mage_abilities.gon`  

```
Creshendo {
    template lobbed_attack

    meta {
        name "ABILITY_CRESHENDO_NAME"
        desc "ABILITY_CRESHENDO_DESC"
        class Mage
        type_icon "magic"
        icon_shell_frame attack
        tooltip_values ["X"]
    }

    graphics {
        projectile MagicMissileProjectileSmall
        lob_height 1
        speed 20
    }
    
    cost {
        infcantrip true
        mana 6-X
        X_cant_be_zero true
    }

    bonus_passives {
        XIsSpellStormRampAndReset 0
    }
    
    target {
        max_aoe X*.5
        max_range X
        min_range 0
        X_is custom
    }
    
    damage_instance {
        raw_damage X
        type spell

        effects {
            VisualFXTile MagicMissleBlast
        }
    }
}
```

---

### `Creshendo2`
**Description:** This spell gains +1 damage, range and area, and -1 mana cost each time you cast a spell.
This spell loses half its boosts after you cast it.  
**Source:** `mage_abilities.gon`  

```
Creshendo2 {
    variant_of Creshendo

    meta {
        desc "ABILITY_CRESHENDO2_DESC"
    }

    bonus_passives {
        XIsSpellStormRampAndReset {
            stacks 0
            reset_percent 50%
        }
    }
}
```

---

### `Divide`
**Name:** Divide  
**Description:** Lose Damage equal to half of your basic attack's damage, rounded up. For the rest of the battle, you can attack an extra time each turn.
\[s:.7\](This can't be cast if your basic attack's damage is 1 or less.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
Divide {
    template self_buff

    keyword_tooltips {DamageUp -1}
    
    meta {
        name "ABILITY_DIVIDE_NAME"
        desc "ABILITY_DIVIDE_DESC"
        class Mage
    }

    graphics {
		animation thinking
    }
    
    cost {
        infcantrip true
        mana 3
        requires_attack_damage_threshold 2
    }

    target {
        X_is basic_attack_damage
    }
    
    damage_instance {
        effects {
            ExtraBasicAttacks_Status 1
            DamageUp "(-ceil(abs(X/2)))"
        }
    }
}
```

---

### `Divide2`
**Description:** Lose Damage equal to 1/3rd of your basic attack's damage, rounded up. For the rest of the battle, you can attack an extra time each turn.
\[s:.7\](This can't be cast if your basic attack's damage is 1 or less.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
Divide2 {
    variant_of Divide

    meta {
        desc "ABILITY_DIVIDE2_DESC"
    }

    damage_instance {
        effects {
            DamageUp "(-ceil(abs(X/3)))"
        }
    }
}
```

---

### `ForbiddenFrost`
**Name:** Forbidden Frost  
**Description:** Apply Freeze 2 to each unit except for yourself and 1 other chosen unit.
Deal 10 Damage to enemies and heal each ally 10 HP.
There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
ForbiddenFrost {
    template spell

    meta {
        name "ABILITY_FORBIDDENFROST_NAME"
        desc "ABILITY_FORBIDDENFROST_DESC"
        class Mage
    }

    graphics {
        particle IcePoof
		animation floatingmagic
    }
    
    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }

    
    target {
        target_mode tile
        max_range 20
        min_range 1
        max_aoe 20
        min_aoe 1
        aoe_considers_character_size false
        knockback_mode zero
        aoe_excludes_self true
        aoe_restrictions exclude_direct_target
    }

    self_damage {
        effects {
            Conditional_GoodRoll {
                odds 90%
                GainDisorderFromPool_PostCast forbidden_spell_consequences
            } Else {
                GainDisorderFromPool_PostCast forbidden_spell_consequences_crippling
            }
        }
    }

    damage_instance {
        damage 10

        effects {
            Conditional_Ally { //this is a weird hack so that the FullHeal of the upgrade can apply before Freeze (conditional statuses get appended onto the end of the status application list so this hack maintains intended order)
            }
            StatusGroup {
                Freeze 2
                DamageOrHealConditionally 1
            }
        }
        
        elements [
            Ice
        ]
    }
}
```

---

### `ForbiddenFrost2`
**Description:** Apply Freeze 2 to each unit except for yourself and 1 other chosen unit.
Deal 15 Damage to enemies and fully heal each ally.
There will be permanent consequences for casting this spell…
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
ForbiddenFrost2 {
    variant_of ForbiddenFrost

    meta {
        desc "ABILITY_FORBIDDENFROST2_DESC"
    }

    damage_instance {
        damage 15

        effects {
            Conditional_Ally {
                OverrideDamage 0
                FullHeal 1
            }
        }
    }
}
```

---

### `BlackMagic`
**Name:** Black Magic  
**Description:** Drop to 1 HP. Gain mana equal to the HP lost.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
BlackMagic {
    template self_buff
    
    meta {
        name "ABILITY_BLACKMAGIC_NAME"
        desc "ABILITY_BLACKMAGIC_DESC"
        class Mage
    }

    graphics {
		animation selfHarm
		particle none
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        X_is current_health
    }
    
    damage_instance {
        raw_damage X-1
        piercing true

        effects {
            ManaGain X-1
        }
    }
}
```

---

### `BlackMagic2`
**Name:** Black Magic  
**Description:** Drop to 1 HP. Gain mana equal to the HP lost and gain All Stats Up 2.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
BlackMagic2 { //not implemented as a variant cause the all stats up has to be before the mana gain...
    template self_buff
    
    meta {
        name "ABILITY_BLACKMAGIC_NAME"
        desc "ABILITY_BLACKMAGIC2_DESC"
        class Mage
    }

    graphics {
    }
    
    cost {
        mana 0
        cantrip true
    }

    target {
        X_is current_health
    }
    
    damage_instance {
        raw_damage X-1
        piercing true

        effects {
            AllStatsUp 2
            ManaGain X-1
        }
    }
}
```

---

### `Teach`
**Name:** Teach  
**Description:** Reduce the cost of another unit's spells by 1 until the end of their turn.  
**Source:** `mage_abilities.gon`  

```
Teach {
    template targeted_status
    
    meta {
        name "ABILITY_TEACH_NAME"
        desc "ABILITY_TEACH_DESC"
        class Mage
    }

    graphics {
		animation thumbsup
    }
    
    cost {
        mana 5
        infcantrip true
    }

    target {
        min_range 1
        max_range 5
    }
    
    damage_instance {
        effects {
            TempManaCostReduction 1
        }
    }
}
```

---

### `Teach2`
**Description:** Reduce the cost of a unit's spells by 1 until the end of their turn. This can target yourself.  
**Source:** `mage_abilities.gon`  

```
Teach2 {
    variant_of Teach

    meta {
        desc "ABILITY_TEACH2_DESC"
    }

    target {
        min_range 0
    }
}
```

---

### `HomingBlasts`
**Name:** Homing Blasts  
**Description:** Shoot 3 Magic Missiles at random enemies.  
**Source:** `mage_abilities.gon`  

```
HomingBlasts {
    template self_buff
    sub_ability HomingBlasts_sub

    meta {
        name "ABILITY_HOMINGBLASTS_NAME"
        desc "ABILITY_HOMINGBLASTS_DESC"
        class Mage
    }

    keyword_tooltips {}

    graphics {
        animation castspell
    }

    cost {
        infcantrip true
        mana 7
    }

    damage_instance {
        effects {
            RandomMagicMissile {
                stacks 3
                full_size true
            }
        }
    }
}
```

---

### `HomingBlasts2`
**Description:** Shoot 4 Magic Missiles at random enemies.  
**Source:** `mage_abilities.gon`  

```
HomingBlasts2 {
    variant_of HomingBlasts
    sub_ability HomingBlasts2_sub

    meta {
        desc "ABILITY_HOMINGBLASTS2_DESC"
    }

    cost {
        mana 6
    }

    damage_instance {
        effects {
            RandomMagicMissile {
                stacks 4
                full_size true
            }
        }
    }
}
```

---

### `HomingBlasts_sub`
**Source:** `mage_abilities.gon`  

```
HomingBlasts_sub { //util used to show "3x3" with magic damage modifications on homing blasts
    template spell
    target {
        multihit 3
    }
    damage_instance {
        damage 3
    }
}
```

---

### `HomingBlasts2_sub`
**Source:** `mage_abilities.gon`  

```
HomingBlasts2_sub { //util used to show "3x3" with magic damage modifications on homing blasts
    template spell
    target {
        multihit 4
    }
    damage_instance {
        damage 3
    }
}
```

---

### `Replicate`
**Name:** Replicate  
**Description:** The next spell you cast is cast twice.  
**Source:** `mage_abilities.gon`  

```
Replicate {
    template self_buff

    meta {
        name "ABILITY_REPLICATE_NAME"
        desc "ABILITY_REPLICATE_DESC"
        class Mage
    }

    graphics {
        animation thumbsup
    }

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        effects {
            DoubleCastSpell 1
        }
    }
}
```

---

### `Replicate2`
**Name:** Replicate  
**Description:** The next spell you or another unit casts is cast twice.  
**Source:** `mage_abilities.gon`  

```
Replicate2 {
    template targeted_status

    meta {
        name "ABILITY_REPLICATE_NAME"
        desc "ABILITY_REPLICATE2_DESC"
        class Mage
    }

    graphics {
        animation jitter
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 0
        max_range 5
    }

    damage_instance {
        effects {
            DoubleCastSpell 1
        }
    }
}
```

---

### `Magnify`
**Name:** Magnify  
**Description:** Your basic attack gains +1 range and area until the end of the turn.  
**Source:** `mage_abilities.gon`  

```
Magnify {
    template self_buff

    meta {
        name "ABILITY_MAGNIFY_NAME"
        desc "ABILITY_MAGNIFY_DESC"
        class Mage
    }

    graphics {
        animation thinking
    }

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        effects {
            TempRangeUp 1
            TempBasicAttackBonusAOE 1
        }
    }
}
```

---

### `Magnify2`
**Description:** Your basic attack gains +2 range and +1 area until the end of the turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `mage_abilities.gon`  

```
Magnify2 {
    variant_of Magnify

    meta {
        desc "ABILITY_MAGNIFY2_DESC"
    }

    cost {
        mana 4
    }

    damage_instance {
        effects {
            TempRangeUp 2
        }
    }
}
```

---

### `TriAttack`
**Name:** Tri-Attack  
**Description:** A Fire / Ice / Electric spell that inflicts Burn 1, Slow 1, and has a 5% chance to inflict Stun.  
**Source:** `mage_abilities.gon`  

```
TriAttack {
    template spell

    meta {
        name "ABILITY_TRIATTACK_NAME"
        desc "ABILITY_TRIATTACK_DESC"
        class Mage
    }

    graphics {
        particle WaterConduct
        animation castspell
    }
    
    cost {
        infcantrip true
        mana 7
    }

    target {
        max_aoe 0
        max_range 5
    }
    
    damage_instance {
        damage 4
        
        effects {
            Burn 1
            Slow 1
            Stun [1 .05]
        }
        
        elements [
            Electric
            Fire
            Ice
        ]
    }
}
```

---

### `TriAttack2`
**Description:** A Fire / Ice / Electric spell that inflicts Burn 1, Slow 1, and has a 5% chance to inflict Stun in an area.  
**Source:** `mage_abilities.gon`  

```
TriAttack2 {
    variant_of TriAttack

    meta {
        desc "ABILITY_TRIATTACK2_DESC"
    }

    target {
        max_aoe 1
        max_range 7
    }
}
```

---

## File: `medic_abilities.gon`

### `RangedHeal`
**Name:** Healing Word  
**Description:** Heal a unit at range.  
**Source:** `medic_abilities.gon`  

```
RangedHeal {
    template spell
    
    meta {
        name "ABILITY_HEALINGWORD_NAME"
        desc "ABILITY_HEALINGWORD_DESC"
        class Medic
    }

    tags [musical]

    graphics {
        animation sing1
        affected_particle HealMed
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        max_aoe 0
        min_range 1
        max_range 3
        aoe_excludes_self true
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

### `RangedHeal2`
**Description:** Heal other units in an area at range.  
**Source:** `medic_abilities.gon`  

```
RangedHeal2 {
    variant_of RangedHeal

    meta {
        desc "ABILITY_HEALINGWORD2_DESC"
    }

    target {
        min_range 1
        max_range 6

        max_aoe 1
    }
}
```

---

### `MeleeHeal`
**Name:** Cure Wounds  
**Description:** Heal an adjacent unit.  
**Source:** `medic_abilities.gon`  

```
MeleeHeal {
    template melee_spell
    
    meta {
        name "ABILITY_CUREWOUNDS_NAME"
        desc "ABILITY_CUREWOUNDS_DESC"
        class Medic
    }

    graphics {
        affected_particle HealBig
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        heal 10
        type spell
        incidentally_collects_pickups false

        elements [
            Holy
        ]
    }
}
```

---

### `MeleeHeal2`
**Description:** Heal all adjacent units.  
**Source:** `medic_abilities.gon`  

```
MeleeHeal2 {
    variant_of MeleeHeal

    meta {
        desc "ABILITY_CUREWOUNDS2_DESC"
    }

    target {
        aoe_mode cross
    }
}
```

---

### `Malaise`
**Name:** Malaise  
**Description:** Inflict Weakness on units in an area.  
**Source:** `medic_abilities.gon`  

```
Malaise {
    template spell

    meta {
        name "ABILITY_MALAISE_NAME"
        desc "ABILITY_MALAISE_DESC"
        class Medic
    }

    graphics {
        particle PoisonPoof
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_aoe 1
        max_range 4
    }
    
    damage_instance {
        damage 0
        
        effects {
            Weakness 2
        }

        elements [
            Poison
        ]
    }
}
```

---

### `Malaise2`
**Description:** Inflict Weakness and Poison on units in an area.  
**Source:** `medic_abilities.gon`  

```
Malaise2 {
    variant_of Malaise

    meta {
        desc "ABILITY_MALAISE2_DESC"
    }

    damage_instance {
        effects {
            Weakness 3
            Poison 3
        }
    }
}
```

---

### `OpenWounds`
**Name:** Open Wounds  
**Description:** A spell that deals more damage the less health the target unit has.
\[s:.7\](based on their health percent)\[/s\]  
**Source:** `medic_abilities.gon`  

```
OpenWounds {
    template melee_spell
    
    meta {
        name "ABILITY_OPENWOUNDS_NAME"
        desc "ABILITY_OPENWOUNDS_DESC"
        class Medic
        type_icon magic
        icon_shell_frame big_damage
        icon_damage_display "0-25"
    }

    graphics {
        animation floatingmagic
        particle Slash
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    damage_instance {
        damage 0
        show_damage_on_0 true
        type spell

        effects {
            DamageBasedOnMissingHealth 25
        }
    }
}
```

---

### `OpenWounds2`
**Description:** A spell that deals even more damage the less health the target unit has.
\[s:.7\](based on their health percent)\[/s\]  
**Source:** `medic_abilities.gon`  

```
OpenWounds2 {
    variant_of OpenWounds

    meta {
        desc "ABILITY_OPENWOUNDS2_DESC"
        icon_damage_display "0-50"
    }

    damage_instance {
        effects {
            DamageBasedOnMissingHealth 50
        }
    }
}
```

---

### `Prayer`
**Name:** Prayer  
**Description:** Heal units in an area.  
**Source:** `medic_abilities.gon`  

```
Prayer {
    template spell

    meta {
        name "ABILITY_PRAYER_NAME"
        desc "ABILITY_PRAYER_DESC"
        class Medic
    }

    graphics {
        affected_particle HealSmall
        animation pray
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_aoe 2
        max_range 6
    }
    
    damage_instance {
        heal 2

        elements [
            Holy
        ]
    }
}
```

---

### `Prayer2`
**Description:** Heal units in a larger area. Infinite range.  
**Source:** `medic_abilities.gon`  

```
Prayer2 {
    variant_of Prayer

    meta {
        desc "ABILITY_PRAYER2_DESC"
    }

    target {
        max_aoe 3
        max_range 20
    }
    
    damage_instance {
        heal 2
    }
}
```

---

### `Convert`
**Name:** Convert  
**Description:** Inflict Charm 2 on an adjacent unit.  
**Source:** `medic_abilities.gon`  

```
Convert {
    template spell
    
    meta {
        name "ABILITY_CONVERT_NAME"
        desc "ABILITY_CONVERT_DESC"
        class Medic
    }

    graphics {
		particle CharmedHearts
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range level
        max_aoe 0
    }
    
    damage_instance {
        damage 0
        type spell

        effects {
            Charmed 2
        }
    }
}
```

---

### `Convert2`
**Description:** Inflict Charm 2 on an adjacent unit. Non-boss enemies with less than 25% health join your party.  
**Source:** `medic_abilities.gon`  

```
Convert2 {
    variant_of Convert

    meta {
        desc "ABILITY_CONVERT2_DESC"
    }

    damage_instance {
        effects {
            Conditional_Enemy {
                Conditional_NotBoss {
                    Conditional_HealthThreshold {
                        threshold_flat 5
                        threshold_percent 25%

                        CaptureFamiliar 1
                        FactionConversion 1
                        FullHeal 1
                    }
                }
            }
        }
    }
}
```

---

### `Cleanse`
**Name:** Cleanse  
**Description:** Remove all debuffs from a unit.  
**Source:** `medic_abilities.gon`  

```
Cleanse {
    template spell

    meta {
        name "ABILITY_CLEANSE_NAME"
        desc "ABILITY_CLEANSE_DESC"
        class Medic
        type_icon "heal"
    }

    graphics {
        affected_particle Cleanse
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        max_aoe 0
        max_range 5
    }
    
    damage_instance {
        damage 0
        
        effects {
            Cleanse 0 //0 = no divine shield per removed buff
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Cleanse2`
**Description:** Remove all debuffs from units in an area.  
**Source:** `medic_abilities.gon`  

```
Cleanse2 {
    variant_of Cleanse

    meta {
        desc "ABILITY_CLEANSE2_DESC"
    }

    target {
        max_aoe 2
        max_range 7
    }

    damage_instance {
        effects {
            Cleanse 0 //1 divine shield for each removed buff
        }
    }
}
```

---

### `Purge`
**Name:** Purge  
**Description:** Remove all buffs from a unit.  
**Source:** `medic_abilities.gon`  

```
Purge { //CUT
    template spell

    meta {
        name "ABILITY_PURGEMEDIC_NAME"
        desc "ABILITY_PURGEMEDIC_DESC"
        class Medic
        type_icon "misc"
    }

    graphics {
        affected_particle Purge
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        max_aoe 0
        max_range 4
    }
    
    damage_instance {
        damage 0
        
        effects {
            Purge 0 //0 damage for each removal
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Purge2`
**Description:** Remove all buffs from a unit. Deal 3 damage to that unit for each unique status effect removed.  
**Source:** `medic_abilities.gon`  

```
Purge2 {
    variant_of Purge

    meta {
        desc "ABILITY_PURGEMEDIC2_DESC"
    }

    damage_instance {
        damage 0
        
        effects {
            Purge 3 //3 damage for each removal
        }
    }
}
```

---

### `HereticMark`
**Name:** Heretic Mark  
**Description:** Inflict Ostracized 2 on a unit.  
**Source:** `medic_abilities.gon`  

```
HereticMark {
    template spell

    meta {
        name "ABILITY_HERETICMARK_NAME"
        desc "ABILITY_HERETICMARK_DESC"
        class Medic
        type_icon "misc"
    }

    graphics {
        affected_particle fx_heretic
        animation pointout
    }
    
    cost {
        infcantrip true
        mana 10
    }
    
    target {
        max_range 7
        max_aoe 0
    }

    damage_instance {
        damage 0
        
        effects {
            Ostracized 2
        }
    }
}
```

---

### `HereticMark2`
**Description:** Inflict Ostracized 4 on a unit.  
**Source:** `medic_abilities.gon`  

```
HereticMark2 {
    variant_of HereticMark

    meta {
        desc "ABILITY_HERETICMARK2_DESC"
    }

    damage_instance {
        effects {
            Ostracized 4
        }
    }
}
```

---

### `Zealot`
**Name:** Zealot  
**Description:** Gain +1 [img:divineshield].  
**Source:** `medic_abilities.gon`  

```
Zealot {
    template self_buff
    
    meta {
        name "ABILITY_ZEALOT_NAME"
        desc "ABILITY_ZEALOT_DESC"
        class Medic
        type_icon "defense"
    }

    graphics {
		animation pray
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    damage_instance {
        effects {
            DivineShield 1
        }
    }
}
```

---

### `Zealot2`
**Description:** Gain +1 [img:divineshield].
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
Zealot2 {
    variant_of Zealot

    meta {
        desc "ABILITY_ZEALOT2_DESC"
    }

    cost {
        mana 5
    }
}
```

---

### `Haste`
**Name:** Haste  
**Description:** Give a unit +10 [img:spd] until the end of its next turn.  
**Source:** `medic_abilities.gon`  

```
Haste {
    template spell

    meta {
        name "ABILITY_HASTE_NAME"
        desc "ABILITY_HASTE_DESC"
        class Medic
    }

    graphics {
        affected_particle fx_haste
		animation pointout
    }
    
    cost {
        mana 3
        infcantrip true
    }
    
    target {
        min_range 1
        max_range 5+2*level
        max_aoe 0
    }

    damage_instance {
        damage 0
        
        effects {
            TempSpeedUp 10
        }
    }
}
```

---

### `Haste2`
**Description:** Give units in an area +10 [img:spd] until the end of their next turns.  
**Source:** `medic_abilities.gon`  

```
Haste2 {
    variant_of Haste

    meta {
        desc "ABILITY_HASTE2_DESC"
    }

    target {
        max_aoe 1
    }
}
```

---

### `Rally`
**Name:** Rally  
**Description:** Force a unit to attack one of its enemies.  
**Source:** `medic_abilities.gon`  

```
Rally {
    template spell
    
    meta {
        name "ABILITY_RALLY_NAME"
        desc "ABILITY_RALLY_DESC"
        class Medic
        type_icon "misc"
    }

    graphics {
        animation pointout
        particle none
    }
    
    cost {
        infcantrip true
        mana 8
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

### `Rally2`
**Description:** Force units in an area to each attack one of their enemies.  
**Source:** `medic_abilities.gon`  

```
Rally2 {
    variant_of Rally

    meta {
        desc "ABILITY_RALLY2_DESC"
    }

    target {
        max_aoe 1
    }
}
```

---

### `BuddyUp`
**Name:** Buddy Up  
**Description:** Jump to an open tile next to an ally.  
**Source:** `medic_abilities.gon`  

```
BuddyUp {
    template jump_attack

    meta {
        name "ABILITY_BUDDYUP_NAME"
        desc "ABILITY_BUDDYUP_DESC"
        class Medic
        type_icon "movement"
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 4
        infcantrip true
    }
    
    target {
        max_range 20

        min_aoe 0
        max_aoe 0
        aoe_excludes_self true
        restrictions [must_be_moveable must_be_adjacent_to_ally]
    }

    damage_instance {
        damage 0
        type none
    }
}
```

---

### `BuddyUp2`
**Description:** Jump to an open tile next to an ally.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
BuddyUp2 {
    variant_of BuddyUp

    meta {
        desc "ABILITY_BUDDYUP2_DESC"
    }

    cost {
        mana 3
        infcantrip true
    }
}
```

---

### `HealingFall`
**Name:** Healing Fall  
**Description:** Jump to an open tile, then heal each adjacent unit.  
**Source:** `medic_abilities.gon`  

```
HealingFall {
    template jump_attack

    meta {
        name "ABILITY_HEALINGFALL_NAME"
        desc "ABILITY_HEALINGFALL_DESC"
        class Medic
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 8
        infcantrip true
    }
    
    target {
        max_range 4

        restrictions [must_be_moveable]
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

### `HealingFall2`
**Description:** Jump to an open tile, then heal each adjacent unit.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
HealingFall2 {
    variant_of HealingFall

    meta {
        desc "ABILITY_HEALINGFALL2_DESC"
    }

    cost {
        mana 5
        infcantrip true
    }
}
```

---

### `RallyCharge`
**Name:** Holy Dash  
**Description:** Dash forward, heal a unit and give it a random stat up.  
**Source:** `medic_abilities.gon`  

```
RallyCharge {
    template dash_attack
    
    meta {
        name "ABILITY_RALLYCHARGE_NAME"
        desc "ABILITY_RALLYCHARGE_DESC"
        class Medic
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation dashatk
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {

    }
    
    damage_instance {
        heal 5
        type spell

        effects {
            RandomStatUp 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `RallyCharge2`
**Description:** Dash forward, heal a unit and give it 3 random stat ups.  
**Source:** `medic_abilities.gon`  

```
RallyCharge2 {
    variant_of RallyCharge

    meta {
        desc "ABILITY_RALLYCHARGE2_DESC"
    }

    cost {
        mana 5
    }

    damage_instance {
        effects {
            RandomStatUp 3
        }
    }
}
```

---

### `ReverseDamage`
**Name:** Reverse Damage  
**Description:** Reverse the last damage an adjacent unit took.  
**Source:** `medic_abilities.gon`  

```
ReverseDamage {
    template melee_spell
    
    meta {
        name "ABILITY_REVERSEDAMAGE_NAME"
        desc "ABILITY_REVERSEDAMAGE_DESC"
        class Medic
        type_icon "heal"
    }

    graphics {
        affected_particle HealBig
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        heal 0
        type spell

        effects {
            UndoDamage 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `ReverseDamage2`
**Description:** Reverse the last damage a unit within range took.  
**Source:** `medic_abilities.gon`  

```
ReverseDamage2 {
    variant_of ReverseDamage

    meta {
        desc "ABILITY_REVERSEDAMAGE2_DESC"
    }

    target {
        target_mode tile
        aoe_mode standard
        min_range 1
        max_range 4
        
        min_aoe 0
        max_aoe 0
    }
}
```

---

### `Rebuke`
**Name:** Rebuke  
**Description:** Deal damage to a unit equal to the damage that unit last dealt.  
**Source:** `medic_abilities.gon`  

```
Rebuke {
    template spell
    
    meta {
        name "ABILITY_REBUKE_NAME"
        desc "ABILITY_REBUKE_DESC"
        class Medic
        type_icon "magic"
        icon_shell_frame attack
        icon_damage_display "?"
    }

    graphics {
		particle rebuke
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 1
        max_range 20

        min_aoe 0
        max_aoe 0
    }
    
    damage_instance {
        damage 0
        type spell
        show_damage_on_0 true

        effects {
            RebukeDamage 1
        }
    }
}
```

---

### `Rebuke2`
**Description:** Deal damage to a unit equal to twice the damage that unit last dealt.  
**Source:** `medic_abilities.gon`  

```
Rebuke2 {
    variant_of Rebuke

    meta {
        desc "ABILITY_REBUKE2_DESC"
    }

    damage_instance {
        effects {
            RebukeDamage 2
        }
    }
}
```

---

### `Wish`
**Name:** Wish  
**Description:** Target an area. At the beginning of your next turn, heal all units in that area.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
Wish {
    template spell
    
    meta {
        name "ABILITY_WISH_NAME"
        desc "ABILITY_WISH_DESC"
        class Medic
    }

    graphics {
        affected_particle HealBig
    }
    
    cost {
        cantrip true
        mana 3
    }

    target {
        delayed_trigger true
        max_aoe 1
        min_range 1
        max_range 20
    }
    
    damage_instance {
        heal 10
        type spell

        elements [
            Holy
        ]
    }
}
```

---

### `Wish2`
**Description:** Target an area. At the beginning of your next turn, heal all units in that area. This spell tracks its target if you directly targeted a unit.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
Wish2 {
    variant_of Wish

    meta {
        desc "ABILITY_WISH2_DESC"
    }

    target {
        track_target true
    }
}
```

---

### `WitchHunt`
**Name:** Witch Hunt  
**Description:** Put a bounty on a unit. When that unit dies, its killer gains All Stats Up.  
**Source:** `medic_abilities.gon`  

```
WitchHunt {
    template spell

    meta {
        name "ABILITY_WITCHHUNT_NAME"
        desc "ABILITY_WITCHHUNT_DESC"
        class Medic
        type_icon "buff"
    }

    graphics {
		animation pointout
		particle none
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_range 20
        max_aoe 0
    }

    damage_instance {
        damage 0
        
        effects {
            StatBounty 1
        }
    }
}
```

---

### `WitchHunt2`
**Description:** Put a bounty on a unit. When that unit dies, it becomes meat and its killer gains All Stats Up.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
WitchHunt2 {
    variant_of WitchHunt

    meta {
        desc "ABILITY_WITCHHUNT2_DESC"
    }

    cost {
        mana 2
    }
    damage_instance {
        effects {
            Meaty 1
        }
    }
}
```

---

### `FriendOrFoe`
**Name:** Friend or Foe  
**Description:** A ranged spell that heals allies and damages enemies.  
**Source:** `medic_abilities.gon`  

```
FriendOrFoe {
    template spell
    
    meta {
        name "ABIITY_FRIENDORFOE_NAME"
        desc "ABIITY_FRIENDORFOE_DESC"
        class Medic
    }

    graphics {
        affected_particle HealMed
		animation pointout
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        max_aoe 0
        min_range 1
        max_range 4
    }
    
    damage_instance {
        damage 3
        type spell

        effects {
            DamageOrHealConditionally 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `FriendOrFoe2`
**Description:** An infinitely ranged spell that heals allies and damages enemies.  
**Source:** `medic_abilities.gon`  

```
FriendOrFoe2 {
    variant_of FriendOrFoe

    meta {
        desc "ABIITY_FRIENDORFOE2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `Revive`
**Name:** Revive  
**Description:** Revive a body to 50% HP and cure one of its injuries.  
**Source:** `medic_abilities.gon`  

```
Revive {
    template melee_spell
    
    meta {
        name "ABILITY_REVIVE_NAME"
        desc "ABILITY_REVIVE_DESC"
        class Medic
        type_icon "heal"
    }

    graphics {
        affected_particle HealBig
        animation pray
    }

    target {
        aoe_restrictions must_have_corpse
        restrictions aoe_must_exist
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    damage_instance {
        heal 0
        type spell
        can_revive true

        effects {
            Conditional_Corpse {
                Revive 50%
                HealRandomInjury 1
            }
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Revive2`
**Description:** Revive a body to 100% HP and cure one of its injuries. If it was an enemy, it gets charmed.  
**Source:** `medic_abilities.gon`  

```
Revive2 {
    variant_of Revive

    meta {
        desc "ABILITY_REVIVE2_DESC"
    }

    damage_instance {
        effects {
            Conditional_Corpse {
                Revive 100%
                Conditional_Enemy {
                    PermanentCharm 1
                }
            }
        }
    }
}
```

---

### `HolyLight`
**Name:** Holy Light  
**Description:** Heal allies and damage enemies in an area. This spell has half effect outside its center.  
**Source:** `medic_abilities.gon`  

```
HolyLight {
    template spell
    
    meta {
        name "ABILITY_HOLYLIGHT_NAME"
        desc "ABILITY_HOLYLIGHT_DESC"
        class Medic
    }

    graphics {
        center_particle Holybeam
        area_particle Holybeam
        animation pray
    }
    
    cost {
        infcantrip true
        mana 12
    }

    target {
        max_aoe 1
        min_range 1
        max_range 5
    }
    
    damage_instance {
        damage 10
        type spell

        effects {
            DamageOrHealConditionally 1
        }

        elements [
            Holy
        ]
    }
    splash_damage {
        damage 5
        type spell

        effects {
            DamageOrHealConditionally 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `HolyLight2`
**Description:** Heal allies and damage enemies in an area. This spell has half effect outside its center.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
HolyLight2 {
    variant_of HolyLight

    meta {
        desc "ABILITY_HOLYLIGHT2_DESC"
    }

    cost {
        mana 8
    }
}
```

---

### `Ethereal`
**Name:** Ethereal  
**Description:** Gain 4 [img:divineshield], 3 [img:shield], heal 2 HP, and Brace 1.  
**Source:** `medic_abilities.gon`  

```
Ethereal {
    template self_buff
    
    meta {
        name "ABILITY_ETHEREAL_NAME"
        desc "ABILITY_ETHEREAL_DESC"
        class Medic
        type_icon "defense"
    }

    graphics {
		animation proud
    }
    
    cost {
        infcantrip true
        mana 16
    }
    
    damage_instance {
        heal 2

        effects {
            DivineShield 4
            Shield 3
            Brace 1
        }
    }
}
```

---

### `Ethereal2`
**Description:** Gain Thorns 6, Reflect 5, 4 [img:divineshield],
3 [img:shield], heal 2 HP and Brace 1.  
**Source:** `medic_abilities.gon`  

```
Ethereal2 {
    variant_of Ethereal

    meta {
        desc "ABILITY_ETHEREAL2_DESC"
    }

    damage_instance {
        heal 2

        effects {
            Thorns 6
            Reflect 5
            DivineShield 4
            Shield 3
            Brace 1
        }
    }
}
```

---

### `BornAgain`
**Name:** Born Again  
**Description:** Revive a body to 100% HP and give it All Stats Up, then you fall asleep.  
**Source:** `medic_abilities.gon`  

```
BornAgain {
    template targeted_status
    
    meta {
        name "ABILITY_BORNAGAIN_NAME"
        desc "ABILITY_BORNAGAIN_DESC"
        class Medic
        type_icon "heal"
    }

    graphics {
        affected_particle HealBig
    }

    target {
        aoe_restrictions must_have_corpse
        restrictions aoe_must_exist

        max_range 7
    }
    
    cost {
        infcantrip true
        mana 10
    }

    self_damage {
        effects {
            Sleep 4
        }
    }
    
    damage_instance {
        heal 0
        type spell
        can_revive true

        effects {
            Conditional_Corpse {
                Revive 100%
                AllStatsUp 1
            }
        }

        elements [
            Holy
        ]
    }
}
```

---

### `BornAgain2`
**Name:** Born Again  
**Description:** Revive a body to 100% HP and give it All Stats Up.  
**Source:** `medic_abilities.gon`  

```
BornAgain2 {
    template targeted_status
    
    meta {
        name "ABILITY_BORNAGAIN_NAME"
        desc "ABILITY_BORNAGAIN2_DESC"
        class Medic
        type_icon "heal"
    }

    graphics {
        affected_particle HealBig
    }

    target {
        aoe_restrictions must_have_corpse
        restrictions aoe_must_exist

        max_range 7
    }
    
    cost {
        infcantrip true
        mana 10
    }
    
    damage_instance {
        heal 0
        type spell
        can_revive true

        effects {
            Conditional_Corpse {
                Revive 100%
                AllStatsUp 1
            }
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Benediction`
**Name:** Benediction  
**Description:** Heal EVERYTHING for 2 HP.  
**Source:** `medic_abilities.gon`  

```
Benediction {
    template spell

    meta {
        name "ABILITY_BENEDICTION_NAME"
        desc "ABILITY_BENEDICTION_DESC"
        class Medic
    }

    graphics {
        particle HealSmall
    }
    
    cost {
        mana 5
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
    }

    damage_instance {
        heal 2

        elements [
            Holy
        ]
    }
}
```

---

### `Benediction2`
**Description:** Heal EVERYTHING for 2 HP.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
Benediction2 {
    variant_of Benediction

    meta {
        desc "ABILITY_BENEDICTION2_DESC"
    }

    cost {
        mana 3
        infcantrip true
    }
}
```

---

### `Crusade`
**Name:** Crusade  
**Description:** You and your allies move toward the nearest enemy.  
**Source:** `medic_abilities.gon`  

```
Crusade {
    template spell

    meta {
        name "ABILITY_CRUSADE_NAME"
        desc "ABILITY_CRUSADE_DESC"
        class Medic
    }

    graphics {
        animation pointout
		particle none
    }
    
    cost {
        mana 3
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero

        aoe_restrictions [allies_only]
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            ForceMoveTowardsEnemies 1
        }
    }
}
```

---

### `Crusade2`
**Description:** You and your allies move toward the nearest enemy and gain +1 [img:str].  
**Source:** `medic_abilities.gon`  

```
Crusade2 {
    variant_of Crusade

    meta {
        desc "ABILITY_CRUSADE2_DESC"
    }

    damage_instance {
        effects {
            StrengthUp 1
        }
    }
}
```

---

### `HallowedGround`
**Name:** Hallowed Ground  
**Description:** Spawn a blessing pickup on an empty tile in range.  
**Source:** `medic_abilities.gon`  

```
HallowedGround {
    template spawn

    meta {
        name "ABILITY_HALLOWEDGROUND_NAME"
        desc "ABILITY_HALLOWEDGROUND_DESC"
        class Medic
        type_icon "misc"
    }
    
    graphics {
        lob true
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        min_range 1
        max_range 4
        restrictions [must_be_empty aoe_must_exist]
    }

    spawn {
        object Blessing
        layer pickups
    }
}
```

---

### `HallowedGround2`
**Description:** Spawn a blessing pickup on any empty tile.  
**Source:** `medic_abilities.gon`  

```
HallowedGround2 {
    variant_of HallowedGround

    meta {
        desc "ABILITY_HALLOWEDGROUND2_DESC"
    }

    cost {
        mana 4
    }
    
    target {
        max_range 20
    }
}
```

---

### `Enlighten`
**Name:** Enlighten  
**Description:** Another unit's next spell is free.  
**Source:** `medic_abilities.gon`  

```
Enlighten {
    template targeted_status
    
    meta {
        name "ABILITY_ENLIGHTEN_NAME"
        desc "ABILITY_ENLIGHTEN_DESC"
        class Medic
    }

    graphics {
        animation pointout
        affected_particle HealBig
    }

    target {
        max_range 5
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    damage_instance {
        type status_spell
        effects {
            FreeSpell 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Enlighten2`
**Description:** Another unit's next spell is free. Infinite range.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
Enlighten2 {
    variant_of Enlighten

    meta {
        desc "ABILITY_ENLIGHTEN2_DESC"
    }

    cost {
        mana 6
    }

    target {
        min_range 1
        max_range 20
    }
}
```

---

### `Anoint`
**Name:** Anoint  
**Description:** Give +2 Diminishing Health Regeneration and +1 to a random stat to an adjacent unit.  
**Source:** `medic_abilities.gon`  

```
Anoint {
    template melee_spell
    
    meta {
        name "ABILITY_ANOINT_NAME"
        desc "ABILITY_ANOINT_DESC"
        class Medic
        type_icon "heal"
    }

    graphics {
        animation pointout
        affected_particle HealBig
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        heal 0
        type spell

        effects {
            DiminishingHealthRegen 2
            RandomStatUp 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Anoint2`
**Description:** Give +2 Diminishing Health Regeneration and +1 to 2 random stats to any unit.  
**Source:** `medic_abilities.gon`  

```
Anoint2 {
    variant_of Anoint

    meta {
        desc "ABILITY_ANOINT2_DESC"
    }

    target {
        target_mode tile
        aoe_mode standard
        min_range 1
        max_range 4
        
        min_aoe 0
        max_aoe 0
    }

    damage_instance {
        heal 0
        type spell

        effects {
            RandomStatUp 2
        }
    }
}
```

---

### `EyeForAnEye`
**Name:** An Eye for an Eye  
**Description:** A melee attack that inflicts Blind 5 and Bleed 1.  
**Source:** `medic_abilities.gon`  

```
EyeForAnEye {
    template melee_attack
    
    meta {
        name "ABILITY_EYEFORANEYE_NAME"
        desc "ABILITY_EYEFORANEYE_DESC"
        class Medic
    }

    graphics {
        animation sliceOpen
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        damage 2+bonus_melee_ability_damage

        effects {
            Blind 5
            Bleed 1

            ApplyStatusIfCrit {
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

### `EyeForAnEye2`
**Description:** A melee attack that inflicts Blind 5, Bleed 1, and Madness 1.  
**Source:** `medic_abilities.gon`  

```
EyeForAnEye2 {
    variant_of EyeForAnEye

    meta {
        desc "ABILITY_EYEFORANEYE2_DESC"
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage

        effects {
            Madness 1
        }
    }
}
```

---

### `WrathOfGod`
**Name:** Wrath of God  
**Description:** Deal holy damage and inflict Blind to everything except for a safe circle around you. This vaporizes units it kills.  
**Source:** `medic_abilities.gon`  

```
WrathOfGod {
    template spell
    
    meta {
        name "ABILITY_WRATHOFGOD_NAME"
        desc "ABILITY_WRATHOFGOD_DESC"
        class Medic
    }

    graphics {
		animation floatingmagic
        particle Holybeam
        delay 6
    }

    cost {
        mana 10
        infcantrip true
    }

    target {
        target_mode none

        max_aoe 20
        min_aoe 4
    }

    damage_instance {
        damage 6

        effects {
            Blind 1
            CorpseVaporizer 1 
        }

        elements [
            Holy
        ]
    }
}
```

---

### `WrathOfGod2`
**Description:** Deal holy damage and inflict Blind to all enemies. This vaporizes units it kills.  
**Source:** `medic_abilities.gon`  

```
WrathOfGod2 {
    variant_of WrathOfGod

    meta {
        desc "ABILITY_WRATHOFGOD2_DESC"
    }

    target {
        min_aoe 1
        aoe_restrictions exclude_allies
    }
}
```

---

### `Adoubement`
**Name:** Adoubment  
**Description:** Heal a unit and remove its debuffs. That unit gets +1 to a random stat and becomes the Alpha.
If there is an Alpha, this spell has infinite range and must target it.  
**Source:** `medic_abilities.gon`  

```
Adoubement {
    template spell
    
    meta {
        name "ABILITY_ADOUBMENT_NAME"
        desc "ABILITY_ADOUBMENT_DESC"
        class Medic
    }

    graphics {
        affected_particle HealMed
        animation pointout
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        max_aoe 0
        min_range 1
        max_range 2
        restrictions must_target_alpha_if_exists
        range_bonuses include_alpha
    }
    
    damage_instance {
        heal 4

        effects {
            Cleanse 0
            AlphaCat 1
            RandomStatUp 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Adoubement2`
**Description:** Heal or revive a unit and remove its debuffs. That unit gets +1 to 3 random stats and becomes the Alpha.
If there is an Alpha, this spell has infinite range and must target it.  
**Source:** `medic_abilities.gon`  

```
Adoubement2 {
    variant_of Adoubement

    meta {
        desc "ABILITY_ADOUBMENT2_DESC"
    }

    damage_instance {
        heal 6
        can_revive true

        effects {
            RandomStatUp 3
        }
    }
}
```

---

### `DivineProtection`
**Name:** Divine Protection  
**Description:** Give a unit +1 [img:divineshield] and +1 Kinetic Spikes. That unit becomes the Alpha.
If there is an Alpha, this spell costs less and must target it.  
**Source:** `medic_abilities.gon`  

```
DivineProtection {
    template targeted_status
    
    meta {
        name "ABILITY_DIVINEPROTECTION_NAME"
        desc "ABILITY_DIVINEPROTECTION_DESC"
        class Medic
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 10-X*6
    }

    target {
        min_range 1
        max_range 4
        restrictions must_target_alpha_if_exists
        X_is alpha_exists
    }
    
    damage_instance {
        effects {
            DivineShield 1
            KineticSpikes 1
            AlphaCat 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `DivineProtection2`
**Description:** Give a unit anywhere +1 [img:divineshield] and +2 Kinetic Spikes. That unit becomes the Alpha.
If there is an Alpha, this spell costs less and must target it.  
**Source:** `medic_abilities.gon`  

```
DivineProtection2 {
    variant_of DivineProtection

    meta {
        desc "ABILITY_DIVINEPROTECTION2_DESC"
    }

    target {
        min_range 1
        max_range 20
    }

    damage_instance {
        effects {
            KineticSpikes 2
        }
    }
}
```

---

### `ChosenWarrior`
**Name:** Chosen Warrior  
**Description:** Give a unit +1 Damage. That unit becomes the Alpha.
If there is an Alpha, this spell must target it and it gives +1 bonus attack.  
**Source:** `medic_abilities.gon`  

```
ChosenWarrior {
    template targeted_status
    
    meta {
        name "ABILITY_CHOSENWARRIOR_NAME"
        desc "ABILITY_CHOSENWARRIOR_DESC"
        class Medic
    }

    graphics {
		animation pointout
		particle fx_statup
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 5
        restrictions must_target_alpha_if_exists
    }
    
    damage_instance {
        effects {
            DamageUp 1
            Conditional_HasStatus {
                status AlphaCat
                Quivered 1
            }
            AlphaCat 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `ChosenWarrior2`
**Description:** Give a unit +1 Damage and +1 Magic Damage. That unit becomes the Alpha.
If there is an Alpha, this spell must target it and it gives +1 bonus attack.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
ChosenWarrior2 {
    variant_of ChosenWarrior

    meta {
        desc "ABILITY_CHOSENWARRIOR2_DESC"
    }

    cost {
        infcantrip true
        mana 4
    }

    damage_instance {
        effects {
            SpellDamageUp 1
        }
    }
}
```

---

### `SwiftSanctify`
**Name:** Swift Servant  
**Description:** Give a unit +1 Bonus Move. That unit becomes the Alpha.
If there is an Alpha, this spell must target it and it gives you +1 Bonus Move too.  
**Source:** `medic_abilities.gon`  

```
SwiftSanctify {
    template targeted_status
    
    meta {
        name "ABILITY_SWIFTSERVANT_NAME"
        desc "ABILITY_SWIFTSERVANT_DESC"
        class Medic
    }

    graphics {
	    animation pointout
	    particle fx_statup
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 1
        max_range 4
        restrictions must_target_alpha_if_exists
    }
    
    damage_instance {
        effects {
            MoveQuivered 1
            Conditional_HasStatus {
                status AlphaCat

                ApplyToSource {
                    MoveQuivered 1
                }
            }
            AlphaCat 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `SwiftSanctify2`
**Description:** Give a unit +1 Bonus Move. That unit becomes the Alpha.
If there is an Alpha, this spell has infinite range, costs less and must target it, and it gives you +1 Bonus Move too.  
**Source:** `medic_abilities.gon`  

```
SwiftSanctify2 {
    variant_of SwiftSanctify

    meta {
        desc "ABILITY_SWIFTSERVANT2_DESC"
    }

    cost {
        mana 4-X
    }

    target {
        range_bonuses include_alpha
        X_is alpha_exists
    }
}
```

---

### `DivineGift`
**Name:** Divine Gift  
**Description:** Gain All Stats Up. This spell costs 1 mana less for each HP you healed other units this turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
DivineGift { //todo: track X globally for this
    template self_buff
    
    meta {
        name "ABILITY_DIVINEGIFT_NAME"
        desc "ABILITY_DIVINEGIFT_DESC"
        class Medic
    }

    graphics {
    }
    
    cost {
        cantrip true
        mana 10-X
    }
    
    target {
        X_is custom
    }
    bonus_passives {
        XIsOtherHealsThisTurn 1
    }

    damage_instance {
        effects {
            AllStatsUp 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `DivineGift2`
**Description:** Gain All Stats Up and +1 [img:divineshield]. This spell costs 1 mana less for each HP you healed other units this turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
DivineGift2 {
    variant_of DivineGift

    meta {
        desc "ABILITY_DIVINEGIFT2_DESC"
    }

    damage_instance {
        effects {
            AllStatsUp 1
            DivineShield 1
        }
    }
}
```

---

### `HolyWeapon`
**Name:** Holy Weapon  
**Description:** A dash attack with range, damage, and knockback equal to the amount of HP you healed other units this turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
HolyWeapon {
    template dash_attack
    
    meta {
        name "ABILITY_HOLYWEAPON_NAME"
        desc "ABILITY_HOLYWEAPON_DESC"
        class Medic
        type_icon melee
        icon_shell_frame attack
    }

    graphics {
        dash_attack_animation knockswatatk
    }
    
    cost {
        cantrip true
        mana 0
    }

    target {
        X_is custom
        max_range X
    }
    bonus_passives {
        XIsOtherHealsThisTurn 1
    }
    
    damage_instance {
        raw_damage X
        knockback X
        show_damage_on_0 true

        effects {
            VisualFX Holyatk
        }

        elements [
            Holy
        ]
    }
}
```

---

### `HolyWeapon2`
**Description:** A dash attack with range, damage, and knockback equal to twice the amount of HP you healed other units this turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
HolyWeapon2 {
    variant_of HolyWeapon

    meta {
        desc "ABILITY_HOLYWEAPON2_DESC"
    }

    target {
        max_range X*2
    }

    damage_instance {
        raw_damage X*2
        knockback X*2
    }
}
```

---

### `GetDown`
**Name:** Stand In  
**Description:** Swap positions with any unit. That unit becomes the Alpha.
If there is an Alpha, this spell must target it.  
**Source:** `medic_abilities.gon`  

```
GetDown {
    template swap
    
    meta {
        name "ABILITY_STANDIN_NAME"
        desc "ABILITY_STANDIN_DESC"
        animate_name true
        class Medic
    }

    graphics {
        mode yeet
    }

    cost {
        mana 2
        infcantrip true
    }

    target {
        max_range 20
        restrictions [must_be_swappable aoe_must_exist must_target_alpha_if_exists must_have_animate_character]
    }

    damage_instance {
        type status_spell
        cant_miss true

        effects {
            AlphaCat 1
        }
    }
}
```

---

### `GetDown2`
**Description:** Swap positions with any unit and heal it by 1 HP. That unit becomes the Alpha.
If there is an Alpha, this spell must target it.  
**Source:** `medic_abilities.gon`  

```
GetDown2 {
    variant_of GetDown

    meta {
        desc "ABILITY_STANDIN2_DESC"
    }

    damage_instance {
        heal 1

        elements [
            Holy
        ]
    }
}
```

---

### `MedicObey`
**Name:** Obey  
**Source:** `medic_abilities.gon`  

```
MedicObey { //for ThouShaltObey passive, does not need an icon
    template spell
    
    meta {
        name "ABILITY_OBEY_NAME"
    }

    graphics {
		animate_name pointout
		particle none
    }


    target {
        target_mode random_closest_tile
        max_aoe 0
        max_range 1

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

### `MedicObey2`
**Source:** `medic_abilities.gon`  

```
MedicObey2 { //for ThouShaltObey passive, does not need an icon
    variant_of MedicObey

    target {
        max_range 20
    }
}
```

---

### `Awaken`
**Name:** Awaken  
**Description:** Revive a body to 1 HP.  
**Source:** `medic_abilities.gon`  

```
Awaken {
    template spell
    
    meta {
        name "ABILITY_AWAKEN_NAME"
        desc "ABILITY_AWAKEN_DESC"
        class Medic
        type_icon "heal"
    }

    graphics {
        affected_particle HealBig
    }

    target {
        aoe_restrictions must_have_corpse_or_sleeping
        restrictions aoe_must_exist
        max_range 5
        max_aoe 0
    }
    
    cost {
        infcantrip true
        mana 1
    }
    
    damage_instance {
        heal 1
        type spell
        can_revive true

        effects {
            RemoveStatus Sleep
            RemoveStatus SleepParalysis
            RemoveStatus Drowsy
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Awaken2`
**Description:** Revive a body to 1 HP. Give that unit +1 [img:divineshield] and All Stats Up.  
**Source:** `medic_abilities.gon`  

```
Awaken2 {
    variant_of Awaken

    meta {
        desc "ABILITY_AWAKEN2_DESC"
    }

    damage_instance {
        effects {
            DivineShield 1
            AllStatsUp 1
        }
    }
}
```

---

### `Baptism`
**Name:** Fury Heal  
**Description:** Heal an adjacent unit 2 to 6 times.  
**Source:** `medic_abilities.gon`  

```
Baptism {
    class MultiHitMeleeAttackAbility
    template melee_attack
    
    meta {
        name "ABILITY_BAPTISM_NAME"
        desc "ABILITY_BAPTISM_DESC"
        class Medic
    }

    graphics {
        start lickAttack
        loop lickAttack
        end lickAttack
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        multihit_min 2
        multihit_max 6
    }

    damage_instance {
        heal 2
        type spell
        incidentally_collects_pickups false

        elements [
            Holy
            Water
        ]
    }
}
```

---

### `Baptism2`
**Description:** Heal an adjacent unit 2 to 6 times. Each heal gives +1 to a random stat.  
**Source:** `medic_abilities.gon`  

```
Baptism2 {
    variant_of Baptism
    
    meta {
        desc "ABILITY_BAPTISM2_DESC"
    }

    damage_instance {
        effects {
            RandomStatUp 1
        }
    }
}
```

---

### `Pray`
**Name:** Pray  
**Description:** Give another unit +5 [img:lck] until the end of its next turn.  
**Source:** `medic_abilities.gon`  

```
Pray {
    template spell
	
    graphics {
        particle fx_statup
        animation pray
    }

    meta {
        name "ABILITY_PRAY_NAME"
        desc "ABILITY_PRAY_DESC"
        class Medic
    }

    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_aoe 0
        max_range 6
    }
    
    damage_instance {
        damage 0
        
        effects {
            Temporary {
                status LuckUp
                stacks 5
                turns 1
                expires_on_end_turn true
            }
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Pray2`
**Name:** Pray  
**Description:** Give allies +5 [img:lck] and enemies -5 [img:lck] until the end of their next turns, in an area.  
**Source:** `medic_abilities.gon`  

```
Pray2 {
    template spell

    meta {
        name "ABILITY_PRAY_NAME"
        desc "ABILITY_PRAY2_DESC"
        class Medic
    }

    graphics {
        particle fx_statup
        animation pray
    }

    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_aoe 1
        max_range 6
    }
    
    damage_instance {
        damage 0
        
        effects {
            Conditional_Ally {
                Temporary {
                    status LuckUp
                    stacks 5
                    turns 1
                    expires_on_end_turn true
                }
            }
            Conditional_Enemy {
                Temporary {
                    status LuckUp
                    stacks -5
                    turns 1
                    expires_on_end_turn true
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

### `Emergency`
**Name:** Emergency  
**Description:** Run next to the ally with the most missing health. Trample all in the way.  
**Source:** `medic_abilities.gon`  

```
Emergency {
    template move
    
    meta {
        name "ABILITY_EMERGENCY_NAME"
        desc "ABILITY_EMERGENCY_DESC"
        animate_name true
        class Medic
    }

    graphics {
        speed 2
        animation dash
    }

    cost {
        infcantrip true
        mana 5
    }

    temporary_effects {
        Trample 3
    }

    target {
        target_mode random_closest_tile
        max_range 100
        restrictions [must_be_moveable must_move must_be_adjacent_to_most_hurt_ally]
        trample_allies_too true
    }
}
```

---

### `Emergency2`
**Description:** Run next to the ally with the most missing health. Trample all in the way.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
Emergency2 {
    variant_of Emergency

    meta {
        desc "ABILITY_EMERGENCY2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `GuardianAngel`
**Name:** Guardian Angel  
**Description:** Make a unit The Alpha.
Bonus Passive: The Alpha has +50% dodge chance.  
**Source:** `medic_abilities.gon`  

```
GuardianAngel {
    template targeted_status
    
    meta {
        name "ABILITY_GUARDIANANGEL_NAME"
        desc "ABILITY_GUARDIANANGEL_DESC"
        class Medic
    }

    graphics {
	    animation pray
	    particle fx_statup
    }
    
    cost {
        infcantrip true
        mana 8
    }

    target {
        min_range 1
        max_range 4
    }

    bonus_passives {
        AlphaDodgeChance 50%
    }
    
    damage_instance {
        effects {
            AlphaCat 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `GuardianAngel2`
**Description:** Make a unit anywhere The Alpha.
\[s:.7\](This spell costs less.)\[/s\]
Bonus Passive: The Alpha has +50% dodge chance.  
**Source:** `medic_abilities.gon`  

```
GuardianAngel2 {
    variant_of GuardianAngel

    meta {
        desc "ABILITY_GUARDIANANGEL2_DESC"
    }

    cost {
        mana 6
    }

    target {
        max_range 20
    }

    damage_instance {
        effects {
            Cleanse 0
        }
    }
}
```

---

### `Booster`
**Name:** Booster  
**Description:** Heal an adjacent unit. Excess healing is converted to an equal amount of random stat ups.  
**Source:** `medic_abilities.gon`  

```
Booster {
    template spell
    
    meta {
        name "ABILITY_BOOSTER_NAME"
        desc "ABILITY_BOOSTER_DESC"
        class Medic
    }

    graphics {
        animation pray
        affected_particle HealBig
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        max_aoe 0
        max_range 1
        min_range 1
    }
    
    damage_instance {
        heal 4
        type spell
        incidentally_collects_pickups false

        effects {
            OverHealToStatuses {
                RandomStatUp 1
            }
        }

        elements [
            Holy
        ]
    }
}
```

---

### `Booster2`
**Description:** Heal a unit at range. Excess healing is converted to an equal amount of random stat ups.  
**Source:** `medic_abilities.gon`  

```
Booster2 {
    variant_of Booster

    meta {
        desc "ABILITY_BOOSTER2_DESC"
    }

    target {
        max_range 4
    }

    cost {
        mana 5
    }
}
```

---

### `Stimulants`
**Name:** Stimulants  
**Description:** You and adjacent units gain +2 [img:spd].  
**Source:** `medic_abilities.gon`  

```
Stimulants {
    template spell
	
	graphics {
        particle fx_statup
		animation hopinplace
    }
    
    meta {
        name "ABILITY_STIMULANTS_NAME"
        desc "ABILITY_STIMULANTS_DESC"
        class Medic
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        target_mode none
        max_aoe 1
    }
    
    damage_instance {
        damage 0

        effects {
            SpeedUp 2
        }
    }
}
```

---

### `Stimulants2`
**Description:** You and adjacent units gain +2 [img:spd] and +1 [img:int].  
**Source:** `medic_abilities.gon`  

```
Stimulants2 {
    variant_of Stimulants

    meta {
        desc "ABILITY_STIMULANTS2_DESC"
    }

    damage_instance {
        effects {
            IntelligenceUp 1
        }
    }
}
```

---

### `BlindingLight`
**Name:** Blinding Lights  
**Description:** Inflict Blind 1 on each unit in an area.  
**Source:** `medic_abilities.gon`  

```
BlindingLight {
    template spell
    
    meta {
        name "ABILITY_BLINDINGLIGHT_NAME"
        desc "ABILITY_BLINDINGLIGHT_DESC"
        class Medic
    }

    graphics {
        particle Holybeam
		animation majormagic
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_range 5
        max_aoe 2
    }
    
    damage_instance {
        damage 0

        effects {
            Blind 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `BlindingLight2`
**Description:** Inflict Blind 2 on each unit in a larger area.  
**Source:** `medic_abilities.gon`  

```
BlindingLight2 {
    variant_of BlindingLight

    meta {
        desc "ABILITY_BLINDINGLIGHT2_DESC"
    }

    target {
        max_range 8
        max_aoe 3
    }

    damage_instance {
        effects {
            Blind 2
        }
    }
}
```

---

### `CircleOfProtection`
**Name:** Circle of Protection  
**Description:** Give +1 [img:divineshield] to each unit within 2 tiles of you.  
**Source:** `medic_abilities.gon`  

```
CircleOfProtection {
    template spell
    
    meta {
        name "ABILITY_CIRCLEOFPROTECTION_NAME"
        desc "ABILITY_CIRCLEOFPROTECTION_DESC"
        class Medic
    }

    graphics {
        animation pray
        particle none
    }

    cost {
        infcantrip true
        mana 8
    }
    
    target {
        max_aoe 2
        target_mode none
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0

        effects {
            DivineShield 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `CircleOfProtection2`
**Description:** Give +1 [img:divineshield] and +1 Health Regeneration to each unit within 2 tiles of you.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `medic_abilities.gon`  

```
CircleOfProtection2 {
    variant_of CircleOfProtection

    meta {
        desc "ABILITY_CIRCLEOFPROTECTION2_DESC"
    }

    cost {
        mana 6
    }

    damage_instance {
        effects {
            DivineShield 1
            HealthRegenUp 1
        }
    }
}
```

---

### `CallOver`
**Name:** Call Over  
**Description:** Make an ally move toward you.  
**Source:** `medic_abilities.gon`  

```
CallOver {
    template targeted_status

    meta {
        name "ABILITY_CALLOVER_NAME"
        desc "ABILITY_CALLOVER_DESC"
        class Medic
        type_icon "misc"
    }
    graphics {
        animation howl
        particle none
    }
    
    cost {
        mana 2
        infcantrip true
    }

    
    target {
        min_range 1
        max_range 5
        max_aoe 0

        restrictions must_have_ally
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

### `CallOver2`
**Description:** Make an ally move toward you. Infinite range.  
**Source:** `medic_abilities.gon`  

```
CallOver2 {
    variant_of CallOver

    meta {
        desc "ABILITY_CALLOVER2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `Grace`
**Name:** Grace  
**Description:** You or an adjacent unit gains a random positive effect.  
**Source:** `medic_abilities.gon`  

```
Grace {
    template targeted_status

    keyword_tooltips {}
    meta {
        name "ABILITY_GRACE_NAME"
        desc "ABILITY_GRACE_DESC"
        class Medic
        type_icon "buff"
    }
    graphics {
        animation pray
        particle fx_statup
    }
    
    cost {
        mana 3
        infcantrip true
    }

    
    target {
        min_range 0
        max_range 1
    }

    damage_instance {
        heal 0
        
        effects {
            Conditional_CanBeHealed {
                RandomStatusFromPool {
                    BonusDamage -5
                    BonusDamage -4
                    BonusDamage -3
                    DivineShield 1
                    GainCoins 1
                    Shield 2
                    RandomStatUp 1
                    RandomStatUp 1
                }
            } Else {
                RandomStatusFromPool {
                    DivineShield 1
                    GainCoins 1
                    Shield 2
                    RandomStatUp 1
                    RandomStatUp 1
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

### `Grace2`
**Name:** Grace  
**Description:** You or an adjacent unit heals a random amount of HP, gains +1 to a random stat, and gains a random positive effect.  
**Source:** `medic_abilities.gon`  

```
Grace2 {
    template targeted_status

    keyword_tooltips {}
    meta {
        name "ABILITY_GRACE_NAME"
        desc "ABILITY_GRACE2_DESC"
        class Medic
        type_icon "buff"

        icon_shell_frame big_damage
        icon_damage_display "1-5"
    }
    graphics {
        animation pray
        particle HealSmall
    }
    
    cost {
        mana 3
        infcantrip true
    }

    
    target {
        min_range 0
        max_range 1

        X_is random_0_to_N
        N 4
    }

    damage_instance {
        heal X+1
        
        effects {
            RandomStatUp 1

            RandomStatusFromPool {
                DivineShield 1
                GainCoins 1
                Shield 2
                Quivered 1
                MoveQuivered 1
                KineticSpikes 1
                SpellDamageUp 1
                DamageUp 1
            }
        }

        elements [
            Holy
        ]
    }
}
```

---

### `TurnFoe`
**Name:** Turn Foe  
**Description:** Force a nearby unit to move away from you.  
**Source:** `medic_abilities.gon`  

```
TurnFoe {
    template targeted_status

    meta {
        name "ABILITY_TURNFOE_NAME"
        desc "ABILITY_TURNFOE_DESC"
        class Medic
        type_icon "misc"
    }
    graphics {
        animation pointout
        particle none
    }
    
    cost {
        mana 2
        infcantrip true
    }

    
    target {
        min_range 1
        max_range 2
        max_aoe 0
    }

    damage_instance {
        damage 0
        
        effects {
            ForceMoveAway 1
        }
    }
}
```

---

### `TurnFoe2`
**Description:** Force a nearby unit to move away from you. If it was an enemy, inflict Madness 1 and Confusion 1.  
**Source:** `medic_abilities.gon`  

```
TurnFoe2 {
    variant_of TurnFoe

    meta {
        desc "ABILITY_TURNFOE2_DESC"
    }

    damage_instance {
        effects {
            Conditional_Enemy {
                Madness 1
                Confusion 1
            }
        }
    }
}
```

---

### `HealingSalve`
**Name:** Healing Salve  
**Description:** You or an adjacent unit gains +1 Health Regeneration.  
**Source:** `medic_abilities.gon`  

```
HealingSalve {
    template targeted_status

    meta {
        name "ABILITY_HEALINGSALVE_NAME"
        desc "ABILITY_HEALINGSALVE_DESC"
        class Medic
        type_icon "buff"
    }
    graphics {
        animation knead
        particle none
    }
    
    cost {
        mana 4
        infcantrip true
    }

    
    target {
        min_range 0
        max_range 1
    }

    damage_instance {
        heal 0
        
        effects {
            HealthRegenUp 1
        }

        elements [
            Holy
        ]
    }
}
```

---

### `HealingSalve2`
**Description:** You or an adjacent unit gains +2 Health Regeneration.  
**Source:** `medic_abilities.gon`  

```
HealingSalve2 {
    variant_of HealingSalve

    meta {
        desc "ABILITY_HEALINGSALVE2_DESC"
    }

    damage_instance {
        effects {
            HealthRegenUp 2
        }
    }
}
```

---

### `Heathens`
**Name:** Heathens!  
**Source:** `medic_abilities.gon`  

```
Heathens { //util ability for Heathens passive, does not need an icon
    template spell

    meta {
        name "ABILITY_HEATHENS_NAME"
        class Medic
    }

    graphics {
        animation howl
        particle fx_statdown
    }

    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions enemies_only
    }

    damage_instance {
        damage 0
        type status_spell
        effects {
            Weakness 3
        }
    }
}
```

---

### `Heathens2`
**Source:** `medic_abilities.gon`  

```
Heathens2 { //util ability for Heathens passive, does not need an icon
    variant_of Heathens

    damage_instance {
        effects {
            Weakness 4
            MagicWeakness 4
        }
    }
}
```

---

## File: `monk_abilities.gon`

### `Propell`
**Name:** Propel  
**Description:** Dash forward one tile and attack.  
**Source:** `monk_abilities.gon`  

```
Propell {
    template dash_attack
    
    meta {
        name "ABILITY_PROPELL_NAME"
        desc "ABILITY_PROPELL_DESC"
        class Monk
    }
    
    graphics {
        dash_start_animation propelStart
        dash_animation propelLoop
        dash_attack_animation propelEnd
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_range 1
    }
    
    damage_instance {
        damage 3+bonus_melee_ability_damage
    }
}
```

---

### `Propell2`
**Description:** Dash forward one tile and attack, twice!  
**Source:** `monk_abilities.gon`  

```
Propell2 {
    variant_of Propell

    meta {
        desc "ABILITY_PROPELL2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `Hadouken`
**Name:** Hadouken  
**Description:** Shoot an energy blast in a straight line.  
**Source:** `monk_abilities.gon`  

```
Hadouken {
    template straightshot_attack
    
    meta {
        name "ABILITY_HADOKEN_NAME"
        desc "ABILITY_HADOKEN_DESC"
        class Monk
    }

    graphics {
        animation hadouken
        projectile MagicMissileProjectile
    }
    
    cost {
        infcantrip true
        mana 9
    }

    target {
        max_aoe 10
    }

    damage_instance {
        damage 10
        type spell

        effects {
            VisualFX MagicMissleBlast
        }
    }
}
```

---

### `Hadouken2`
**Description:** Shoot a high damage energy blast in a straight line.  
**Source:** `monk_abilities.gon`  

```
Hadouken2 {
    variant_of Hadouken

    meta {
        desc "ABILITY_HADOKEN2_DESC"
    }

     damage_instance {
        damage 15
     }
}
```

---

### `Cartwheel`
**Name:** Cartwheel  
**Description:** Roll up to 4 tiles diagonally.  
**Source:** `monk_abilities.gon`  

```
Cartwheel {
    template move
    
    meta {
        name "ABILITY_CARTWHEEL_NAME"
        desc "ABILITY_CARTWHEEL_DESC"
        class Monk
        animate_name true
    }

    graphics {
        sync_speed 30
        //max_tiles_single_loop 1
        ignore_slowtiles true
        move_start_animation cartwheelStart
        animation cartwheelLoop
        move_end_animation cartwheelEnd
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        range_mode diagcross
        max_range 4
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_diagonals true
    }
}
```

---

### `Cartwheel2`
**Description:** Roll up to 4 tiles diagonally or in a straight line.  
**Source:** `monk_abilities.gon`  

```
Cartwheel2 {
    variant_of Cartwheel

    meta {
        desc "ABILITY_CARTWHEEL2_DESC"
    }

    target {
        range_mode 8cross
    }
}
```

---

### `StoneFists`
**Name:** Stone Fists  
**Description:** Gain [img:str] and [img:dex] equal to your [img:shield] until the end of your turn.  
**Source:** `monk_abilities.gon`  

```
StoneFists {
    template self_buff
    
    meta {
        name "ABILITY_STONEFISTS_NAME"
        desc "ABILITY_STONEFISTS_DESC"
        class Monk
        type_icon "buff"
    }

    graphics {
        animation stoneFists
    }

    target {
        X_is current_shield
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            TempStrengthUp X
            TempDexterityUp X
        }
    }
}
```

---

### `StoneFists2`
**Name:** Stone Fists  
**Description:** Convert your [img:shield] to [img:str] and [img:dex] for the rest of the battle.  
**Source:** `monk_abilities.gon`  

```
StoneFists2 {
    template self_buff
    
    meta {
        name "ABILITY_STONEFISTS_NAME"
        desc "ABILITY_STONEFISTS2_DESC"
        class Monk
        type_icon "buff"
    }

    graphics {

    }

    target {
        X_is current_shield
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            StrengthUp X
            DexterityUp X
            Shield -X
        }
    }
}
```

---

### `Transcend`
**Name:** Transcend  
**Description:** Cleanse your debuffs and gain +1 [img:shield].  
**Source:** `monk_abilities.gon`  

```
Transcend {
    template self_buff
    
    meta {
        name "ABILITY_TRANSCEND_NAME"
        desc "ABILITY_TRANSCEND_DESC"
        class Monk
        type_icon "defense"
    }

    graphics {

    }

    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            Cleanse 0 //0 = no divine shield per removed buff
            Shield 1
        }
    }
}
```

---

### `Transcend2`
**Description:** Cleanse your debuffs and gain +1 [img:shield]. At the end of each round, automatically cast this spell for free.  
**Source:** `monk_abilities.gon`  

```
Transcend2 {
    variant_of Transcend
    
    meta {
        desc "ABILITY_TRANSCEND2_DESC"
    }

    bonus_passives {
        AutocastEachRound {
            ability Transcend2
            even_if_stunned true
        }
    }
}
```

---

### `HipToss`
**Name:** Hip Toss  
**Description:** Throw a random adjacent unit two tiles away, dealing damage to it.  
**Source:** `monk_abilities.gon`  

```
HipToss {
    template throw_attack
    
    meta {
        name "ABILITY_HIPTOSS_NAME"
        desc "ABILITY_HIPTOSS_DESC"
        class Monk
    }

    graphics {
        animation knockupatk
    }

    cost {
        mana 3
        infcantrip true
    }
    
    target {
        max_range 2
        min_range 2
        restrictions none
    }
    
    damage_instance {
        damage 3+bonus_melee_ability_damage
    }
}
```

---

### `HipToss2`
**Description:** Throw a random adjacent unit two tiles away, dealing damage to it. This deals double damage if it's thrown onto another unit.  
**Source:** `monk_abilities.gon`  

```
HipToss2 {
    variant_of HipToss

    meta {
        desc "ABILITY_HIPTOSS2_DESC"
    }

    damage_instance {
        blocked_damage "(3+bonus_melee_ability_damage)*2"
    }
}
```

---

### `Bruise`
**Name:** Bruise  
**Description:** Your basic attack inflicts Bruise until the end of the turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
Bruise {
    template self_buff
    
    meta {
        name "ABILITY_BRUISE_NAME"
        desc "ABILITY_BRUISE_DESC"
        class Monk
        type_icon "buff"
    }

    graphics {
        animation bruise
    }

    cost {
        mana 6
        cantrip true
    }
    
    damage_instance {
        effects {
            HeavyHits 1
        }
    }
}
```

---

### `Bruise2`
**Description:** Your basic attack inflicts Bruise until the end of the turn.  
**Source:** `monk_abilities.gon`  

```
Bruise2 {
    variant_of Bruise
    
    meta {
        desc "ABILITY_BRUISE2_DESC"
    }

    cost {
        infcantrip true
    }
}
```

---

### `Slapback`
**Name:** Slapback  
**Description:** A melee attack with a high critical hit chance.
RELOAD: Take damage.  
**Source:** `monk_abilities.gon`  

```
Slapback {
    template melee_attack
    
    meta {
        name "ABILITY_SLAPBACK_NAME"
        desc "ABILITY_SLAPBACK_DESC"
        class Monk
    }

    graphics {
    }

    cost {
        requires_reload true
        mana 0
    }

    bonus_passives {
        ReloadOnAnyDamage 1
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage
        crit_chance 50%

        type melee
    }
}
```

---

### `Slapback2`
**Description:** A melee attack with a 100% critical hit chance.
RELOAD: Take damage.  
**Source:** `monk_abilities.gon`  

```
Slapback2 {
    variant_of Slapback

    meta {
        desc "ABILITY_SLAPBACK2_DESC"
    }

    damage_instance {
        crit_chance 100%
    }
}
```

---

### `Finisher`
**Name:** Finisher  
**Description:** Dash forward three tiles and attack. This deals 2 damage for each action you've taken this turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
Finisher {
    template dash_attack
    
    meta {
        name "ABILITY_FINISHER_NAME"
        desc "ABILITY_FINISHER_DESC"
        class Monk
        icon_shell_frame attack
        type_icon attack
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_attack_animation heaviestMelee
    }
    
    cost {
        cantrip true
        mana 6
    }
    
    target {
        max_range 3
        X_is storm_count
    }
    
    damage_instance {
        raw_damage X*2 //raw_damage lets this go down to 0
        show_damage_on_0 true
    }
}
```

---

### `Finisher2`
**Description:** Dash forward three tiles and attack. This deals 2 damage for each action you've taken this turn.
\[s:.7\](This spell costs 0 mana. Castable once per turn.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
Finisher2 {
    variant_of Finisher

    meta {
        desc "ABILITY_FINISHER2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `Reverberate`
**Name:** Reverberate  
**Description:** Gain +8 [img:shield] and knock back adjacent units two tiles. This spell costs 3 mana less for each action you've taken this turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
Reverberate {
    template melee_attack
    
    meta {
        name "ABILITY_REVERBERATE_NAME"
        desc "ABILITY_REVERBERATE_DESC"
        class Monk
        type_icon "defense"
    }

    tags [musical]

    graphics {
        animation block
    }

    cost {
        mana 22-X*3
        cantrip true
    }

    target {
        target_mode none
        aoe_mode cross
        X_is storm_count
    }

    self_damage {
        effects {
            Shield 8
        }
    }
    
    damage_instance {
        damage 0
        type spell
        knockback 2
        incidentally_collects_pickups false
    }
}
```

---

### `Reverberate2`
**Description:** Gain +8 [img:shield] and knock back adjacent units two tiles. This spell costs 3 mana less and grants 1 extra [img:shield] for each action you've taken this turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
Reverberate2 {
    variant_of Reverberate

    meta {
        desc "ABILITY_REVERBERATE2_DESC"
    }

    self_damage {
        effects {
            Shield 8+X
        }
    }
}
```

---

### `ComboThrow`
**Name:** Combo Throw  
**Description:** A melee attack with Knockback 3. When this hits, switch into ranged stance and refresh your basic attack.  
**Source:** `monk_abilities.gon`  

```
ComboThrow {
    template melee_attack
    
    meta {
        name "ABILITY_COMBOTHROW_NAME"
        desc "ABILITY_COMBOTHROW_DESC"
        class Monk
    }

    graphics {
		animation knockswatatk
    }

    cost {
        infcantrip true
        mana 6
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage
        type melee
        knockback 3

        effects {
            ApplyToSource {
                StanceSwitchToRanged 1
                RefreshActPoints 1
            }
        }
    }
}
```

---

### `ComboThrow2`
**Description:** A melee attack with Knockback 3. When this hits, switch into ranged stance and refresh your basic attack.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
ComboThrow2 {
    variant_of ComboThrow

    meta {
        desc "ABILITY_COMBOTHROW2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `ComboPull`
**Name:** Combo Pull  
**Description:** A ranged attack that pulls the unit it hits toward you. When this hits, switch into melee stance and refresh your basic attack.  
**Source:** `monk_abilities.gon`  

```
ComboPull {
    template lobbed_attack
    
    meta {
        name "ABILITY_COMBOPULL_NAME"
        desc "ABILITY_COMBOPULL_DESC"
        class Monk
    }

    target {
        min_range 2
        max_range 4+bonus_range
    }

    cost {
        infcantrip true
        mana 6
    }

    damage_instance {
        damage 1+bonus_ranged_damage

        effects {
            ApplyToSource {
                StanceSwitchToMelee 1
                RefreshActPoints 1
            }
            DisplaceTowardsSource 1
        }
    }
}
```

---

### `ComboPull2`
**Description:** A ranged attack that pulls the unit it hits toward you. When this hits, switch into melee stance and refresh your basic attack.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
ComboPull2 {
    variant_of ComboPull

    meta {
        desc "ABILITY_COMBOPULL2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `OneWithTheWind`
**Name:** One With the Wind  
**Description:** Gain +20 Movement Range until the end of the turn.  
**Source:** `monk_abilities.gon`  

```
OneWithTheWind {
    template self_buff
    
    meta {
        name "ABILITY_ONEWITHTHEWIND_NAME"
        desc "ABILITY_ONEWITHTHEWIND_DESC"
        class Monk
        type_icon "movement"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            TempMovement 20
        }
    }
}
```

---

### `OneWithTheWind2`
**Description:** Gain +20 Movement Range until the end of the turn and refresh your movement action.  
**Source:** `monk_abilities.gon`  

```
OneWithTheWind2 {
    variant_of OneWithTheWind

    meta {
        desc "ABILITY_ONEWITHTHEWIND2_DESC"
    }

    damage_instance {
        effects {
            RefreshMovePoints 1
        }
    }
}
```

---

### `Pogo`
**Name:** Pogo  
**Description:** Jump to a tile. Bounce off any unit you land on, damaging that unit.  
**Source:** `monk_abilities.gon`  

```
Pogo {
    template jump_attack

    meta {
        name "ABILITY_POGO_NAME"
        desc "ABILITY_POGO_DESC"
        class Monk
        type_icon "movement"
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 5
        infcantrip true
    }
    
    target {
        max_range 3

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none

        always_bounce true
    }

    damage_instance {
        damage 3+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `Pogo2`
**Description:** Jump to a tile. Bounce off any unit you land on, damaging and Bruising that unit.  
**Source:** `monk_abilities.gon`  

```
Pogo2 {
    variant_of Pogo

    meta {
        desc "ABILITY_POGO2_DESC"
    }

    target {
        max_range 5
    }

    damage_instance {
        effects {
            Bruise 1
        }
    }
}
```

---

### `TrainArms`
**Name:** Way of the Mantis  
**Description:** For the rest of the battle, you can attack an extra time each turn.  
**Source:** `monk_abilities.gon`  

```
TrainArms {
    template self_buff
    
    meta {
        name "ABILITY_WAYOFTHEMANTIS_NAME"
        desc "ABILITY_WAYOFTHEMANTIS_DESC"
        class Monk
        type_icon "buff"
    }

    graphics {
		animation stoneFists
    }
    
    cost {
        infcantrip true
        mana 12
    }
    
    damage_instance {
        effects {
            ExtraBasicAttacks_Status 1
        }
    }
}
```

---

### `TrainArms2`
**Description:** For the rest of the battle, you can attack an extra time each turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
TrainArms2 {
    variant_of TrainArms

    meta {
        desc "ABILITY_WAYOFTHEMANTIS2_DESC"
    }

    cost {
        mana 9
    }
}
```

---

### `Porcupine`
**Name:** Porcupine  
**Description:** Gain +2 temporary Brace and +2 temporary Thorns until your next turn.  
**Source:** `monk_abilities.gon`  

```
Porcupine {
    template self_buff
    
    meta {
        name "ABILITY_PORCUPINE_NAME"
        desc "ABILITY_PORCUPINE_DESC"
        class Monk
        type_icon "defense"
    }

    graphics {
		animation bruise
    }

    cost {
        mana 5
        infcantrip true
    }

    damage_instance {
        damage 0

        effects {
            Temporary {
                status Thorns
                stacks 2
                turns 1
                expires_on_begin_turn true
            }
            Temporary {
                status Brace
                stacks 2
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `Porcupine2`
**Description:** Gain +2 temporary Brace and +2 temporary Thorns until your next turn. Also reflect the next projectile you're hit by.  
**Source:** `monk_abilities.gon`  

```
Porcupine2 {
    variant_of Porcupine

    meta {
        desc "ABILITY_PORCUPINE2_DESC"
    }

    damage_instance {
        effects {
            Reflect 1
        }
    }
}
```

---

### `Anneal`
**Name:** Anneal  
**Description:** Gain +1 [img:shield]. This spell costs 0 mana the first time you cast it each turn.  
**Source:** `monk_abilities.gon`  

```
Anneal {
    template self_buff
    
    meta {
        name "ABILITY_ANNEAL_NAME"
        desc "ABILITY_ANNEAL_DESC"
        class Monk
        type_icon "defense"
    }

    graphics {
        animation block
    }

    cost {
        infcantrip true
        mana 3
    }

    bonus_passives {
        FreeFirstCast 1
    }
    
    damage_instance {
        effects {
            Shield 1
        }
    }
}
```

---

### `Anneal2`
**Name:** Anneal  
**Description:** Gain +1 [img:shield]. This spell costs 0 mana the first time you cast it each turn, and after each time you spend mana on another spell.  
**Source:** `monk_abilities.gon`  

```
Anneal2 {
    template self_buff
    
    meta {
        name "ABILITY_ANNEAL_NAME"
        desc "ABILITY_ANNEAL2_DESC"
        class Monk
        type_icon "defense"
    }

    graphics {
        animation block
    }

    cost {
        infcantrip true
        mana 3
    }

    bonus_passives {
        FreeFirstCastAndAfterSpendMana 1
    }
    
    damage_instance {
        effects {
            Shield 1
        }
    }
}
```

---

### `DeepDive`
**Name:** Deep Dive  
**Description:** Become downed. You don't get injured. At the end of the next round, you're revived with 1 HP, 15 [img:shield], and All Stats Up.  
**Source:** `monk_abilities.gon`  

```
DeepDive {
    template self_buff
    
    meta {
        name "ABILITY_DEEPDIVE_NAME"
        desc "ABILITY_DEEPDIVE_DESC"
        class Monk
        type_icon "defense"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            SafeDie 1
            ReviveNextRound {
                stacks 2
                revive_health 1

                Shield 15
                AllStatsUp 1
            }
        }
    }
}
```

---

### `DeepDive2`
**Description:** Become downed. You don't get injured. At the end of the next round, you're revived with 50% HP, 20 [img:shield], 2 [img:divineshield], and All Stats Up 2.  
**Source:** `monk_abilities.gon`  

```
DeepDive2 {
    variant_of DeepDive
    
    meta {
        desc "ABILITY_DEEPDIVE2_DESC"
    }

    damage_instance {
        effects {
            ReviveNextRound {
                stacks 2
                revive_health 50%
                Shield 20
                DivineShield 2
                AllStatsUp 2
            }
        }
    }
}
```

---

### `HopAndBlock`
**Name:** Hop n' Block  
**Description:** Jump to a tile, then gain +2 [img:shield] for each enemy adjacent to the tile you land on.  
**Source:** `monk_abilities.gon`  

```
HopAndBlock {
    template jump_attack

    meta {
        name "ABILITY_HOPNBLOCK_NAME"
        desc "ABILITY_HOPNBLOCK_DESC"
        class Monk
        type_icon "movement"
    }

    graphics {
        jump_attack_animation block
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        max_range 4
    }

    temporary_effects {
        JustInCaseTrample 0
    }

    damage_instance {
        damage 0
        type none
        cant_miss true
        makes_contact false
        effects {
            Conditional_Enemy {
                ApplyToSource {
                    Shield 2
                }
            }
        }
    }
}
```

---

### `HopAndBlock2`
**Description:** Jump to any tile, then gain +2 [img:shield] for each enemy adjacent to the tile you land on.  
**Source:** `monk_abilities.gon`  

```
HopAndBlock2 {
    variant_of HopAndBlock

    meta {
        desc "ABILITY_HOPNBLOCK2_DESC"
    }

    target {
        max_range 10
    }
}
```

---

### `TrainMind`
**Name:** Way of the Owl  
**Description:** For the rest of the battle, the first spell you cast each turn is cast twice.  
**Source:** `monk_abilities.gon`  

```
TrainMind {
    template self_buff
    
    meta {
        name "ABILITY_WAYOFTHEOWL_NAME"
        desc "ABILITY_WAYOFTHEOWL_DESC"
        class Monk
        type_icon "buff"
    }

    graphics {
		animation meditate
    }
    
    cost {
        infcantrip true
        mana 13
    }
    
    damage_instance {
        effects {
            DoubleCastSpellsEachTurn_Status 1
        }
    }
}
```

---

### `TrainMind2`
**Description:** For the rest of the battle, the first spell you cast each turn is cast twice.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
TrainMind2 {
    variant_of TrainMind

    meta {
        desc "ABILITY_WAYOFTHEOWL2_DESC"
    }

    cost {
        mana 10
    }
}
```

---

### `Meditate`
**Name:** Meditate  
**Description:** Heal yourself for 8 HP and gain +8 Shield, All Stats Up 2, and Sleep 8.  
**Source:** `monk_abilities.gon`  

```
Meditate {
    template self_buff
    
    meta {
        name "ABILITY_MEDITATE_NAME"
        desc "ABILITY_MEDITATE_DESC"
        class Monk
        type_icon "buff"
    }

    graphics {
        animation meditate
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    damage_instance {
        heal 8

        effects {
            Sleep 8
            Shield 8
            AllStatsUp 2
        }
    }
}
```

---

### `Meditate2`
**Name:** Meditate  
**Description:** Heal yourself for 8 HP and gain +8 Shield, All Stats Up 2, and Drowsy 8.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
Meditate2 {
    template self_buff
    
    meta {
        name "ABILITY_MEDITATE_NAME"
        desc "ABILITY_MEDITATE2_DESC"
        class Monk
        type_icon "buff"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        heal 8

        effects {
            Drowsy 8
            Shield 8
            AllStatsUp 2
        }
    }
}
```

---

### `DoomPunch`
**Name:** Five Point Palm Exploding Heart Technique  
**Description:** A melee attack that causes a unit to die at the end of its next turn. Bosses fall asleep at the end of their next turn instead.  
**Source:** `monk_abilities.gon`  

```
DoomPunch {
    template melee_attack
    
    meta {
        name "ABILITY_DOOMPUNCH_NAME"
        desc "ABILITY_DOOMPUNCH_DESC"
        class Monk
    }

    graphics {
        animation tinyPunch
    }

    cost {
        infcantrip true
        mana 7
    }

    damage_instance {
        damage 0

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

### `DoomPunch2`
**Description:** A melee attack that causes a unit to die at the end of its next turn. Bosses fall asleep at the end of their next turn instead.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
DoomPunch2 {
    variant_of DoomPunch

    meta {
        desc "ABILITY_DOOMPUNCH2_DESC"
    }

    cost {
        mana 5
    }
}
```

---

### `KiBurst`
**Name:** Ki Burst  
**Description:** Deal 1 damage and knockback adjacent units. Gain +1 [img:shield].  
**Source:** `monk_abilities.gon`  

```
KiBurst {
    template spell

    meta {
        name "ABILITY_KIBURST_NAME"
        desc "ABILITY_KIBURST_DESC"
        class Monk
    }

    graphics {
        particle fx_magicSplash
    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        target_mode none

        aoe_mode standard
        min_aoe 1
        max_aoe 1

        aoe_considers_character_size true
        aoe_excludes_self true
    }

    self_damage {
        effects {
            Shield 1
        }
    }
    damage_instance {
        damage 1
        knockback 1
    }
}
```

---

### `KiBurst2`
**Description:** Deal 2 damage and knockback adjacent units 2 tiles. Gain +2 [img:shield].  
**Source:** `monk_abilities.gon`  

```
KiBurst2 {
    variant_of KiBurst

    meta {
        desc "ABILITY_KIBURST2_DESC"
    }
    self_damage {
        effects {
            Shield 2
        }
    }
    damage_instance {
        damage 2
        knockback 2
    }
}
```

---

### `DragonPunch`
**Name:** Dragon Punch  
**Description:** A magic damage melee attack with knockback 3 that inflicts Confusion.  
**Source:** `monk_abilities.gon`  

```
DragonPunch {
    template melee_attack
    
    meta {
        name "ABILITY_DRAGONPUNCH_NAME"
        desc "ABILITY_DRAGONPUNCH_DESC"
        class Monk
    }

    graphics {
		animation uppercutatk
    }

    cost {
        infcantrip true
        mana 7
    }

    damage_instance {
        damage 5
        type spell
        knockback 3
        makes_contact false

        effects {
            Confusion 1
            VisualFX MagicMissleBlast
        }
    }
}
```

---

### `DragonPunch2`
**Description:** A strong magic damage melee attack with knockback 10 that inflicts Confusion.  
**Source:** `monk_abilities.gon`  

```
DragonPunch2 {
    variant_of DragonPunch

    meta {
        desc "ABILITY_DRAGONPUNCH2_DESC"
    }

    damage_instance {
        damage 8
        knockback 10

        effects {
            VisualFX BigMagicMissileBlast
        }
    }
}
```

---

### `TrainLegs`
**Name:** Way of the Hare  
**Description:** For the rest of the battle, you can move an extra time each turn.  
**Source:** `monk_abilities.gon`  

```
TrainLegs {
    template self_buff
    
    meta {
        name "ABILITY_WAYOFTHEHARE_NAME"
        desc "ABILITY_WAYOFTHEHARE_DESC"
        class Monk
        type_icon "buff"
    }

    graphics {
		animation backflipLoop
    }
    
    cost {
        infcantrip true
        mana 9
    }
    
    damage_instance {
        effects {
            ExtraBasicMoves_Status 1
        }
    }
}
```

---

### `TrainLegs2`
**Description:** For the rest of the battle, you can move an extra time each turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
TrainLegs2 {
    variant_of TrainLegs

    meta {
        desc "ABILITY_WAYOFTHEHARE2_DESC"
    }

    cost {
        mana 6
    }
}
```

---

### `ReallyFastRun`
**Name:** Really Fast Run  
**Description:** Run in a straight line up to 4 tiles, through objects. Wind blows over tiles you run through.  
**Source:** `monk_abilities.gon`  

```
ReallyFastRun {
    template move
    
    meta {
        name "ABILITY_REALLYFASTRUN_NAME"
        desc "ABILITY_REALLYFASTRUN_DESC"
        class Monk
        animate_name true

        icon_damage_display_eq 1+bonus_spell_damage_display
        icon_shell_frame attack
        icon_damage_type magic
    }
    
    graphics {
        speed 6
        ignore_slowtiles true
        //move_start_animation startroll
        animation dash
        //move_end_animation endroll
    }

    cost {
        infcantrip true
        mana 6
    }

    temporary_effects {
        //DisableTrample 1
        DelayedWindTrail 1
    }

    target {
        range_mode cross
        max_range 4
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_diagonals true
    }
}
```

---

### `ReallyFastRun2`
**Description:** Run diagonally or in a straight line any distance, through objects. Wind blows over tiles you run through.  
**Source:** `monk_abilities.gon`  

```
ReallyFastRun2 {
    variant_of ReallyFastRun

    meta {
        desc "ABILITY_REALLYFASTRUN2_DESC"
    }

    target {
        range_mode 8cross
        max_range 10
    }
}
```

---

### `DetectWeakness`
**Name:** Ocular Pat Down  
**Description:** Inflict Marked and Magic Weakness 1 on a unit.  
**Source:** `monk_abilities.gon`  

```
DetectWeakness {
    template targeted_status

    meta {
        name "ABILITY_OCULARPATDOWN_NAME"
        desc "ABILITY_OCULARPATDOWN_DESC"
        class Monk
    }

    graphics {
        affected_particle TakeAim
    }
    
    cost {
        mana 7
        infcantrip true
    }
    
    target {
        min_range 1
        max_range 4+bonus_range
    }

    damage_instance {
        effects {
            Marked 1
            MagicWeakness 1
        }
    }
}
```

---

### `DetectWeakness2`
**Description:** Inflict Marked 3 and Magic Weakness 3 on a unit.  
**Source:** `monk_abilities.gon`  

```
DetectWeakness2 {
    variant_of DetectWeakness

    meta {
        desc "ABILITY_OCULARPATDOWN2_DESC"
    }

    damage_instance {
        effects {
            Marked 3
            MagicWeakness 3
        }
    }
}
```

---

### `HundredHandSlap`
**Name:** Hundred Hand Slap  
**Description:** A ten-hit multi-strike melee attack with Knockback 10 at the end of the combo.  
**Source:** `monk_abilities.gon`  

```
HundredHandSlap {
    template melee_attack
    class PlaceholderMeleeAttackAbility
    
    meta {
        name "ABILITY_100HANDSLAP_NAME"
        desc "ABILITY_100HANDSLAP_DESC"
        class Monk
    }

    graphics {
        animation megaslap

        darken_screen true
        darken_screen_exclude_characters_on_tile true
        darken_screen_exclude_self true
        darken_screen_start_early true
    }

    cost {
        infcantrip true
        mana 15
    }

    target {
        aoe_considers_character_size false
        target_mode tile
        restrictions must_have_character
        range_mode standard
        aoe_mode standard
        min_range 1
        max_range 1
        min_aoe 0 
        max_aoe 0 

        multihit 10
        randomize_knockback_direction_except_for_finisher true
    }

    damage_instance {
        damage "1+bonus_melee_ability_damage/5"
        type melee
        knockback 10
    }
}
```

---

### `HundredHandSlap2`
**Description:** A ten-hit multi-strike melee attack with Knockback 10 at the end of the combo. Each hit has a 10% chance to inflict Bruise. The final hit deals extra damage.  
**Source:** `monk_abilities.gon`  

```
HundredHandSlap2 {
    variant_of HundredHandSlap

    meta {
        desc "ABILITY_100HANDSLAP2_DESC"
    }

    damage_instance {
        effects {
            Bruise [1 .1]
        }

        final_hit_bonus_damage 5+bonus_melee_ability_damage
    }
}
```

---

### `KineticCharge`
**Name:** Kinetic Charge  
**Description:** Gain +1 temporary Kinetic Spikes.  
**Source:** `monk_abilities.gon`  

```
KineticCharge {
    template self_buff
    
    meta {
        name "ABILITY_KINETICCHARGE_NAME"
        desc "ABILITY_KINETICCHARGE_DESC"
        class Monk
        type_icon "defense"
    }

    graphics {
        animation meditate
    }

    cost {
        mana 3
        infcantrip true
    }

    damage_instance {
        damage 0

        effects {
            Temporary {
                status KineticSpikes
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `KineticCharge2`
**Description:** Gain +2 temporary Kinetic Spikes.  
**Source:** `monk_abilities.gon`  

```
KineticCharge2 {
    variant_of KineticCharge

    meta {
        desc "ABILITY_KINETICCHARGE2_DESC"
    }

    damage_instance {
        effects {
            Temporary {
                stacks 2
            }
        }
    }
}
```

---

### `AirBurst`
**Name:** Air Burst  
**Description:** A burst of air that knocks back units diagonally from the target.  
**Source:** `monk_abilities.gon`  

```
AirBurst {
    template spell

    meta {
        name "ABILITY_AIRBURST_NAME"
        desc "ABILITY_AIRBURST_DESC"
        class Monk
        type_icon "magic"
    }

    graphics {
        particle fx_windSpell
        animation attack
        use_projectile true
        projectile MagicMissileProjectile
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_aoe 1
        max_aoe 1
        max_range 5+bonus_range

        aoe_mode diagcross
    }
    
    damage_instance {
        damage 0
        knockback 1
        
        elements [
            Wind
        ]
    }
}
```

---

### `AirBurst2`
**Description:** A large burst of air that knocks back units diagonally from the target.  
**Source:** `monk_abilities.gon`  

```
AirBurst2 {
    variant_of AirBurst

    meta {
        desc "ABILITY_AIRBURST2_DESC"
    }

    target {
        max_aoe 3
        max_range 7+bonus_range
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

### `TrainBody`
**Name:** Way of the Turtle  
**Description:** Gain +1 Brace.  
**Source:** `monk_abilities.gon`  

```
TrainBody {
    template self_buff
    
    meta {
        name "ABILITY_WAYOFTHETURTLE_NAME"
        desc "ABILITY_WAYOFTHETURTLE_DESC"
        class Monk
        type_icon "buff"
    }

    graphics {
		animation block
    }
    
    cost {
        infcantrip true
        mana 9
    }
    
    damage_instance {
        effects {
            Brace 1
        }
    }
}
```

---

### `TrainBody2`
**Description:** Gain +1 Brace.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
TrainBody2 {
    variant_of TrainBody

    meta {
        desc "ABILITY_WAYOFTHETURTLE2_DESC"
    }

    cost {
        mana 6
    }
}
```

---

### `ReleaseEnergy`
**Name:** Release Energy  
**Description:** Emit 10 Sparkles.  
**Source:** `monk_abilities.gon`  

```
ReleaseEnergy {
    template self_buff
    
    meta {
        name "ABILITY_RELEASEENERGY_NAME"
        desc "ABILITY_RELEASEENERGY_DESC"
        class Monk
        type_icon "magic"

        icon_damage_display_eq 1+bonus_spell_damage_display
        icon_damage_display_suffix "x10"
        icon_shell_frame multihit_attack
        icon_damage_type magic
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 12
    }
    
    damage_instance {
        effects {
            RandomMagicMissile 10
        }
    }
}
```

---

### `ReleaseEnergy2`
**Description:** Emit 10 Sparkles.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
ReleaseEnergy2 {
    variant_of ReleaseEnergy
    
    meta {
        desc "ABILITY_RELEASEENERGY2_DESC"
    }

    cost {
        mana 9
    }
}
```

---

### `Pummel`
**Name:** Pummel  
**Description:** A melee attack that does 3 more damage each time you use it on the same turn. This attack inflicts all status effects your basic attack does.  
**Source:** `monk_abilities.gon`  

```
Pummel {
    template melee_attack
    
    meta {
        name "ABILITY_PUMMEL_NAME"
        desc "ABILITY_PUMMEL_DESC"
        class Monk
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        X_is this_ability_storm_count
    }

    bonus_passives {
        CopyBasicAttackEffects 1
    }

    damage_instance {
        damage 1+X*3
    }
}
```

---

### `Pummel2`
**Description:** A melee attack that does 4 more damage each time you use it on the same turn. This attack inflicts all status effects your basic attack does.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
Pummel2 {
    variant_of Pummel

    meta {
        desc "ABILITY_PUMMEL2_DESC"
    }

    cost {
        mana 4
    }

    damage_instance {
        damage 1+X*4
    }
}
```

---

### `QuickAttack`
**Name:** Quick Attack  
**Description:** Teleport, then use your basic attack on an enemy within range. This spell's range is increased by 2 for each empty armor slot you have.  
**Source:** `monk_abilities.gon`  

```
QuickAttack {
    template teleport
    
    meta {
        name "ABILITY_QUICKATTACK_NAME"
        desc "ABILITY_QUICKATTACK_DESC"
        animate_name true
        class Monk
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 7
    }

    bonus_passives {
        XIsFreeArmorSlots 1
    }

    target {
        max_range 1+X*2
        min_range 1
        X_is custom
    }

    self_damage {
        effects {
            ForceAttack 1
        }
    }
}
```

---

### `QuickAttack2`
**Description:** Teleport, then use your basic attack on an enemy within range. This spell's range is increased by 2 for each empty armor slot you have.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
QuickAttack2 {
    variant_of QuickAttack

    meta {
        desc "ABILITY_QUICKATTACK2_DESC"
    }

    cost {
        mana 5
    }
}
```

---

### `PerfectForm`
**Name:** Perfect Form  
**Description:** Gain +1 [img:shield] for each empty armor slot you have, then switch stances.  
**Source:** `monk_abilities.gon`  

```
PerfectForm {
    template self_buff
    
    meta {
        name "ABILITY_PERFECTFORM_NAME"
        desc "ABILITY_PERFECTFORM_DESC"
        class Monk
    }

    graphics {
		animation cartwheelLoop
    }
    
    cost {
        infcantrip true
        mana 4
    }

    bonus_passives {
        XIsFreeArmorSlots 1
    }

    target {
        X_is custom
    }
    
    damage_instance {
        effects {
            Shield X
            MonkStanceSwitch 1
        }
    }
}
```

---

### `PerfectForm2`
**Description:** Gain +1 [img:shield] and heal 1 HP for each empty armor slot you have, then switch stances.  
**Source:** `monk_abilities.gon`  

```
PerfectForm2 {
    variant_of PerfectForm
    
    meta {
        desc "ABILITY_PERFECTFORM2_DESC"
    }

    damage_instance {
        heal X
        effects {
            Shield X
            MonkStanceSwitch 1
        }
    }
}
```

---

### `WarmupStretch`
**Name:** Warm Up Stretch  
**Description:** Gain +1 [img:dex], and +1 [img:spd]. This spell costs 2 mana less for each empty armor slot you have.  
**Source:** `monk_abilities.gon`  

```
WarmupStretch {
    template self_buff
    
    meta {
        name "ABILITY_WARMUPSTRETCH_NAME"
        desc "ABILITY_WARMUPSTRETCH_DESC"
        class Monk
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 8-X*2
    }

    bonus_passives {
        XIsFreeArmorSlots 1
    }

    target {
        X_is custom
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

### `WarmupStretch2`
**Description:** Gain +1 [img:dex], +1 [img:spd] and +1 [img:str]. This spell costs 2 mana less for each empty armor slot you have.  
**Source:** `monk_abilities.gon`  

```
WarmupStretch2 {
    variant_of WarmupStretch
    
    meta {
        desc "ABILITY_WARMUPSTRETCH2_DESC"
    }

    damage_instance {
        effects {
            StrengthUp 1
        }
    }
}
```

---

### `FlyingFist`
**Name:** Flying Fist  
**Description:** A melee attack with knockback that hits two tiles away from you. This spell's range is increased by 1 each time you use it on the same turn.  
**Source:** `monk_abilities.gon`  

```
FlyingFist {
    template melee_spell
    
    meta {
        name "ABILITY_FLYINGFIST_NAME"
        desc "ABILITY_FLYINGFIST_DESC"
        class Monk
    }

    graphics {
        animation attack
        particle fx_windSpell
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_aoe 2+X
        max_aoe 2+X

        X_is this_ability_storm_count
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        type physical_spell
        knockback 1

        elements [
            Wind
        ]
    }
}
```

---

### `FlyingFist2`
**Description:** A melee attack with knockback that hits two tiles away from you. This spell's range is increased by 1 and mana cost decreased by 1 each time you use it on the same turn.  
**Source:** `monk_abilities.gon`  

```
FlyingFist2 {
    variant_of FlyingFist

    meta {
        desc "ABILITY_FLYINGFIST2_DESC"
    }

    cost {
        mana "max(4-X, 0)"
    }
}
```

---

### `RapidFlowSpin`
**Source:** `monk_abilities.gon`  

```
RapidFlowSpin { //util ability for RapidFlow passive, does not need an icon
    template melee_attack

    graphics {
        animation singleSpin
    }

    target {
        target_mode none
        aoe_mode cross
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 1+bonus_melee_ability_damage
    }
}
```

---

### `RapidFlowSpin2`
**Source:** `monk_abilities.gon`  

```
RapidFlowSpin2 { //util ability for RapidFlow passive, does not need an icon
    variant_of RapidFlowSpin
    class MultiHitMeleeAttackAbility

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

### `SpiritBomb`
**Name:** Charge Spirit Bomb  
**Description:** Begin charging a spirit bomb. This ability becomes Throw Spirit Bomb.
Allies gain the bonus ability Donate Energy until you throw it.  
**Source:** `monk_abilities.gon`  

```
SpiritBomb {
    template self_buff

    keyword_tooltips {
        BonusAbility ThrowSpiritBomb
        BonusAbility DonateEnergy
    }
    
    meta {
        name "ABILITY_CHARGESPIRITBOMB_NAME"
        desc "ABILITY_CHARGESPIRITBOMB_DESC"
        class Monk
        type_icon "buff"
    }

    cost {
        infcantrip true
        mana 0
    }
    
    damage_instance {
        effects {
            TransformAbility ThrowSpiritBomb
        }
    }
}
```

---

### `SpiritBomb2`
**Description:** Begin charging a spirit bomb. This ability becomes Throw Spirit Bomb.
Allies gain the bonus ability Donate Energy+ until you throw it.  
**Source:** `monk_abilities.gon`  

```
SpiritBomb2 {
    variant_of SpiritBomb

    keyword_tooltips {
        BonusAbility ThrowSpiritBomb2
        BonusAbility DonateEnergy2
    }
    
    meta {
        desc "ABILITY_CHARGESPIRITBOMB2_DESC"
    }

    damage_instance {
        effects {
            TransformAbility ThrowSpiritBomb2
        }
    }
}
```

---

### `ThrowSpiritBomb`
**Name:** Throw Spirit Bomb  
**Description:** Throw the Spirit Bomb, then this ability becomes Charge Spirit Bomb.
\[s:.7\](Cannot be thrown with 0 charges.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
ThrowSpiritBomb {
    template spell

    meta {
        name "ABILITY_THROWSPIRITBOMB_NAME"
        desc "ABILITY_THROWSPIRITBOMB_DESC"
        class Monk
        icon_shell_frame attack
    }

    graphics {
        area_particle MagicMissleBlast
        center_particle BigMagicMissileBlast
        use_projectile true
        projectile MagicMissileProjectile
        lob_height 1
        speed 20
        animation castspell
        delay 5
    }
    
    cost {
        infcantrip true
        mana 0
        X_cant_be_zero true
    }

    bonus_passives {
        ChargeSpiritBombAura DonateEnergy
    }
    
    target {
        max_aoe 2
        max_range 20
        X_is custom
    }
    
    self_damage {
        effects {
            TransformAbility SpiritBomb
        }
    }

    damage_instance {
        raw_damage X

        elements [
            Explosion
        ]
    }
}
```

---

### `ThrowSpiritBomb2`
**Source:** `monk_abilities.gon`  

```
ThrowSpiritBomb2 {
    variant_of ThrowSpiritBomb

    bonus_passives {
        ChargeSpiritBombAura DonateEnergy2
    }

    self_damage {
        effects {
            TransformAbility SpiritBomb2
        }
    }
}
```

---

### `DonateEnergy`
**Name:** Donate Energy  
**Description:** Give +1 damage to the Spirit Bomb!  
**Source:** `monk_abilities.gon`  

```
DonateEnergy {
    template self_buff
    
    meta {
        name "ABILITY_DONATEENERGY_NAME"
        desc "ABILITY_DONATEENERGY_DESC"
        class Monk
        type_icon "buff"
    }

    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        effects {
            AddSpiritBombCharges 1
        }
    }
}
```

---

### `DonateEnergy2`
**Description:** Give +2 damage to the Spirit Bomb!  
**Source:** `monk_abilities.gon`  

```
DonateEnergy2 {
    variant_of DonateEnergy

    meta {
        desc "ABILITY_DONATEENERGY2_DESC"
    }
    
    damage_instance {
        effects {
            AddSpiritBombCharges 2
        }
    }
}
```

---

### `OnePunch`
**Name:** One Punch  
**Description:** A one-hit kill punch. Gain All Stats Down on use.
This deals 25 damage to bosses instead of killing them.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
OnePunch {
    template melee_attack
    
    meta {
        name "ABILITY_ONEPUNCH_NAME"
        desc "ABILITY_ONEPUNCH_DESC"
        class Monk
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }

    self_damage {
        effects {
            AllStatsUp -1
        }
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

### `OnePunch2`
**Name:** One Punch  
**Description:** A one-hit kill punch. It causes a cone of wind that deals 5 damage. Gain All Stats Down on use.
This deals 25 damage to bosses instead of killing them.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
OnePunch2 {
    variant_of OnePunch

    meta {
        name "ABILITY_ONEPUNCH_NAME"
        desc "ABILITY_ONEPUNCH2_DESC"
    }

    damage_instance {
        effects {
            DelayedWindCone {
                damage 5
                distance 10
            }
        }
    }
}
```

---

### `UnbridledHits`
**Name:** Unbridled Hits  
**Description:** A weak melee attack that hits an extra time for each empty armor slot you have.  
**Source:** `monk_abilities.gon`  

```
UnbridledHits {
    class MultiHitMeleeAttackAbility
    template melee_attack
    
    meta {
        name "ABILITY_UNBRIDLEDHITS_NAME"
        desc "ABILITY_UNBRIDLEDHITS_DESC"
        class Monk
    }

    graphics {
        start monkAttack
        loop monkAttack
        end monkAttack
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        X_is custom
        multihit X+1
    }

    bonus_passives {
        XIsFreeArmorSlots 1
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage
    }
}
```

---

### `UnbridledHits2`
**Description:** A weak melee attack that hits two extra times for each empty armor slot you have.  
**Source:** `monk_abilities.gon`  

```
UnbridledHits2 {
    variant_of UnbridledHits

    meta {
        desc "ABILITY_UNBRIDLEDHITS2_DESC"
    }

    target {
        multihit X*2+1
    }
}
```

---

### `Kamehameha`
**Name:** Kamehameha  
**Description:** Fire a magic blast at a unit within 5 tiles. Requires line of sight.
\[s:.7\](Castable once per battle. If all your armor slots are empty, castable once per turn.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
Kamehameha {
    template spell

    meta {
        name "ABILITY_KAMEHAMEHA_NAME"
        desc "ABILITY_KAMEHAMEHA_DESC"
        class Monk
        icon_shell_frame attack
    }

    graphics {
        particle BigMagicMissileBlast
        use_projectile true
        projectile MagicMissileProjectile
        lob_height 0
        speed 20
        animation hadouken
    }
    
    cost {
        cantrip true
        mana 0
        once_per_fight 3-X
    }

    bonus_passives {
        XIsFreeArmorSlots 1
    }
    
    target {
        max_aoe 0
        max_range 5
        X_is custom
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 14
    }
}
```

---

### `Kamehameha2`
**Description:** Fire a magic blast at a unit anywhere within your line of sight.
\[s:.7\](Castable once per battle. If all your armor slots are empty, castable once per turn.)\[/s\]  
**Source:** `monk_abilities.gon`  

```
Kamehameha2 {
    variant_of Kamehameha

    meta {
        desc "ABILITY_KAMEHAMEHA2_DESC"
    }

    target {
        max_range 20
    }

    damage_instance {
        damage 20
    }
}
```

---

### `SideStep`
**Name:** Sidestep  
**Description:** Move one tile and gain +1 [img:shield].  
**Source:** `monk_abilities.gon`  

```
SideStep {
    template move
    
    meta {
        name "ABILITY_SIDESTEP_NAME"
        desc "ABILITY_SIDESTEP_DESC"
        animate_name true
        class Monk
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 1
    }

    self_damage {
        effects {
            Shield 1
        }
    }
}
```

---

### `SideStep2`
**Description:** Move one tile and gain +1 [img:shield].
This spell costs 0 mana the first time you cast it each turn.  
**Source:** `monk_abilities.gon`  

```
SideStep2 {
    variant_of SideStep

    meta {
        desc "ABILITY_SIDESTEP2_DESC"
    }

    cost {
        mana 4
    }

    bonus_passives {
        FreeFirstCast 1
    }
}
```

---

### `UnimpededLunge`
**Name:** Unimpeded Lunge  
**Description:** Dash forward X spaces, gain +X [img:shield], deal X damage, and deal X knockback.
X is equal to the number of empty armor slots you have plus one.  
**Source:** `monk_abilities.gon`  

```
UnimpededLunge {
    template dash_attack
    
    meta {
        name "ABILITY_UNIMPEDEDLUNGE_NAME"
        desc "ABILITY_UNIMPEDEDLUNGE_DESC"
        class Monk
    }
    
    graphics {
        dash_start_animation propelStart
        dash_animation propelLoop
        dash_attack_animation propelEnd
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        max_range X+1
        X_is custom
    }

    bonus_passives {
        XIsFreeArmorSlots 1
    }
    
    self_damage {
        effects {
            Shield X+1
        }
    }

    damage_instance {
        damage X+1
        knockback X+1
    }
}
```

---

### `UnimpededLunge2`
**Description:** Dash forward X spaces, gain +X [img:shield], deal X damage, and deal X knockback.
X is equal to twice the number of empty armor slots you have.  
**Source:** `monk_abilities.gon`  

```
UnimpededLunge2 {
    variant_of UnimpededLunge

    meta {
        desc "ABILITY_UNIMPEDEDLUNGE2_DESC"
        icon_shell_frame attack
    }

    target {
        max_range 2*X
    }
    
    self_damage {
        effects {
            Shield 2*X
        }
    }

    damage_instance {
        raw_damage 2*X
        knockback 2*X
    }
}
```

---

### `DoubleDragon`
**Name:** Double Dragon  
**Description:** Summon a 1 HP illusion of yourself within three tiles that mimics your basic attack, but in the opposite direction of you. It dies at the end of your turn.  
**Source:** `monk_abilities.gon`  

```
DoubleDragon {
    template spawn

    meta {
        name "ABILITY_DOUBLEDRAGON_NAME"
        desc "ABILITY_DOUBLEDRAGON_DESC"
        class Monk
    }

    tags [summon]
    
    graphics {
        lob false
        animation MonkStartTurn
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        min_range 1
        max_range 3
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object PlayerCat_MonkShade
        faction self

        catdata clone
        clone_items true
    }
}
```

---

### `DoubleDragon2`
**Description:** Summon a 1 HP illusion of yourself on any tile that mimics your basic attack, but in the opposite direction of you. It dies at the end of your turn.  
**Source:** `monk_abilities.gon`  

```
DoubleDragon2 {
    variant_of DoubleDragon

    meta {
        desc "ABILITY_DOUBLEDRAGON2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `FistOfFate`
**Name:** Fist of Fate  
**Description:** Teleport next to a random enemy, then switch to melee stance and automatically attack it.  
**Source:** `monk_abilities.gon`  

```
FistOfFate {
    template teleport
    
    meta {
        name "ABILITY_FISTOFFATE_NAME"
        desc "ABILITY_FISTOFFATE_DESC"
        animate_name true
        class Monk
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        target_mode random_tile
        max_range 20
        min_range 1
        restrictions [must_be_moveable must_be_adjacent_to_enemy_fistoffate]
    }

    self_damage {
        effects {
            StanceSwitchToMelee 1
            DelayedFury 0
            ForceAttack {
                immediate true
            }
        }
    }
}
```

---

### `FistOfFate2`
**Description:** Teleport next to a random enemy, then switch to melee stance and automatically attack it. This has a chance to repeat multiple times on different targets.  
**Source:** `monk_abilities.gon`  

```
FistOfFate2 {
    variant_of FistOfFate

    meta {
        desc "ABILITY_FISTOFFATE2_DESC"
    }

    bonus_passives {
        FistOfFateUniqueEnemyTracker 1
    }

    self_damage {
        effects {
            StanceSwitchToMelee 1
            DelayedFury 75
            ForceAttack {
                immediate true
            }
        }
    }
}
```

---

### `Nirvana`
**Name:** Nirvana  
**Description:** Gain +1 [img:int] and +1 [img:shield].
If you have 7 or more [img:shield], this spell costs 1 mana less.  
**Source:** `monk_abilities.gon`  

```
Nirvana {
    template self_buff
    
    meta {
        name "ABILITY_NIRVANA_NAME"
        desc "ABILITY_NIRVANA_DESC"
        class Monk
        type_icon "buff"
    }
	
    graphics {
        animation meditate
    }

    target {
        X_is current_shield
    }
    
    cost {
        infcantrip true
        mana "4-clamp(floor(X/7), 0, 1)"
    }
    
    damage_instance {
        effects {
            Shield 1
            IntelligenceUp 1
        }
    }
}
```

---

### `Nirvana2`
**Description:** Gain +1 [img:int] and +2 [img:shield].
If you have 7 or more [img:shield], this spell costs 1 mana less.  
**Source:** `monk_abilities.gon`  

```
Nirvana2 {
    variant_of Nirvana
    
    meta {
        desc "ABILITY_NIRVANA2_DESC"
    }
    
    damage_instance {
        effects {
            Shield 2
            IntelligenceUp 1
        }
    }
}
```

---

### `EmptyMind`
**Name:** Empty Mind  
**Description:** You can't cast spells for the rest of the battle.
For the rest of the battle, whenever you kill an enemy, take an extra turn.  
**Source:** `monk_abilities.gon`  

```
EmptyMind {
    template self_buff
    
    meta {
        name "ABILITY_EMPTYMIND_NAME"
        desc "ABILITY_EMPTYMIND_DESC"
        class Monk
        type_icon "buff"
    }
	
	graphics {
        animation psyAttack1
    }

    cost {
        infcantrip true
        once_per_fight true
        mana 0
    }
    
    damage_instance {
        effects {
            EmptyMind 1
        }
    }
}
```

---

### `EmptyMind2`
**Description:** You can't cast spells for the rest of the battle.
For the rest of the battle, whenever you kill an enemy, take an extra turn.
Get an extra turn when you cast this.  
**Source:** `monk_abilities.gon`  

```
EmptyMind2 {
    variant_of EmptyMind
    
    meta {
        desc "ABILITY_EMPTYMIND2_DESC"
    }

    damage_instance {
        effects {
            TakeExtraTurn 1
        }
    }
}
```

---

### `Position`
**Name:** Position  
**Description:** Teleport exactly two tiles away, then switch stances.  
**Source:** `monk_abilities.gon`  

```
Position {
    template teleport
    
    meta {
        name "ABILITY_POSITION_NAME"
        desc "ABILITY_POSITION_DESC"
        animate_name true
        class Monk
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        max_range 2
        min_range 2
    }

    self_damage {
        effects {
            MonkStanceSwitch 1
        }
    }
}
```

---

### `Position2`
**Description:** Teleport two to four tiles away, then switch stances.  
**Source:** `monk_abilities.gon`  

```
Position2 {
    variant_of Position
    
    meta {
        desc "ABILITY_POSITION2_DESC"
    }

    target {
        max_range 4
        min_range 2
    }
}
```

---

### `ChargeFists`
**Name:** Charge Fists  
**Description:** Until end of turn, your basic attack emits +1 Sparkle.  
**Source:** `monk_abilities.gon`  

```
ChargeFists {
    template self_buff

    keyword_tooltips {RandomMagicMissile 1}
    
    meta {
        name "ABILITY_CHARGEFISTS_NAME"
        desc "ABILITY_CHARGEFISTS_DESC"
        class Monk
        type_icon "buff"
    }

    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            ChargeFists 1
        }
    }
}
```

---

### `ChargeFists2`
**Description:** Until end of turn, your basic attack emits +1 Sparkle.
Refresh your basic attack.  
**Source:** `monk_abilities.gon`  

```
ChargeFists2 {
    variant_of ChargeFists

    meta {
        desc "ABILITY_CHARGEFISTS2_DESC"
    }

    damage_instance {
        effects {
            RefreshActPoints 1
        }
    }
}
```

---

### `Apprentice`
**Name:** Summon Apprentice  
**Description:** Summon a half-sized copy of yourself with half your stats. It's AI-controlled and can't use spells.  
**Source:** `monk_abilities.gon`  

```
Apprentice {
    template spawn

    meta {
        name "ABILITY_SUMMONAPPRENTICE_NAME"
        desc "ABILITY_SUMMONAPPRENTICE_DESC"
        class Monk
    }

    tags [summon]
    
    graphics {
        lob false
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 9
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
        object PlayerCat_MonkMiniMe
        faction self

        catdata clone
        clone_items true
    }
}
```

---

### `Apprentice2`
**Description:** Summon a half-sized copy of yourself with half your stats. It's AI-controlled and CAN use spells.  
**Source:** `monk_abilities.gon`  

```
Apprentice2 {
    variant_of Apprentice

    meta {
        desc "ABILITY_SUMMONAPPRENTICE2_DESC"
    }

    spawn {
        object PlayerCat_MiniMe
    }
}
```

---

## File: `necromancer_abilities.gon`

### `MaggotArmy`
**Name:** Decompose  
**Description:** Explode a body and spawn 3 Leeches.  
**Source:** `necromancer_abilities.gon`  

```
MaggotArmy {
    template spell
	
	graphics {
        animation floatingmagic
        particle none
    }
    
    meta {
        name "ABILITY_DECOMPOSE_NAME"
        desc "ABILITY_DECOMPOSE_DESC"
        class Necromancer
        type_icon "spawn"
    }

    tags [summon]

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 1
        max_range 4
        max_aoe 0
        restrictions must_have_destructible_corpse
    }

    damage_instance {
        damage 0

        effects {
            VaporizeCorpse 1
            CanApplyToInanimate {
                ObjectOnHitCharacter CharmedLeech
                ObjectOnHitCharacter CharmedLeech
                ObjectOnHitCharacter CharmedLeech
            }
        }
    }
}
```

---

### `MaggotArmy2`
**Name:** Decompose  
**Description:** Explode a body and spawn 5 Leeches.  
**Source:** `necromancer_abilities.gon`  

```
MaggotArmy2 {
    template spell

    meta {
        name "ABILITY_DECOMPOSE_NAME"
        desc "ABILITY_DECOMPOSE2_DESC"
        class Necromancer
        type_icon "spawn"
    }

	graphics {
        animation floatingmagic
        particle none
    }

    tags [summon]

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 1
        max_range 4
        max_aoe 0
        restrictions must_have_destructible_corpse
    }

    damage_instance {
        damage 0

        effects {
            VaporizeCorpse 1
            CanApplyToInanimate {
                ObjectOnHitCharacter CharmedLeech
                ObjectOnHitCharacter CharmedLeech
                ObjectOnHitCharacter CharmedLeech
                ObjectOnHitCharacter CharmedLeech
                ObjectOnHitCharacter CharmedLeech
            }
        }
    }
}
```

---

### `Reanimate`
**Name:** Reanimate  
**Description:** Resurrect a body to half HP. It becomes a Zombie and joins your team.  
**Source:** `necromancer_abilities.gon`  

```
Reanimate {
    template targeted_status
    
    meta {
        name "ABILITY_REANIMATE_NAME"
        desc "ABILITY_REANIMATE_DESC"
        class Necromancer
        type_icon "misc"
    }

    graphics {
        animation floatingmagic
        affected_particle HealBig
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 1
        max_range 4
        max_aoe 0
        aoe_restrictions must_have_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        effects {
            Reanimate 50%
        }
    }
}
```

---

### `Reanimate2`
**Description:** Resurrect a body to full HP. It becomes a Zombie and joins your team.  
**Source:** `necromancer_abilities.gon`  

```
Reanimate2 {
    variant_of Reanimate

    meta {
        desc "ABILITY_REANIMATE2_DESC"
    }

    target {
        max_range 20
    }

    damage_instance {
        effects {
            Reanimate 100%
        }
    }
}
```

---

### `Rebirth`
**Name:** Rebirth  
**Description:** Teleport into a body, destroying it to heal 4 HP, gain +1 [img:int] and +1 [img:con].  
**Source:** `necromancer_abilities.gon`  

```
Rebirth {
    template teleport
    
    meta {
        name "ABILITY_REBIRTH_NAME"
        desc "ABILITY_REBIRTH_DESC"
        animate_name true
        class Necromancer
        type_icon "misc"
    }

    graphics {
        animation_out digDown
        animation_in digUp
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        max_range 20
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    self_damage {
        damage 0

        effects {
            ConstitutionUp 1
            IntelligenceUp 1
            HealthGain 4
        }
    }

    damage_instance {
        damage 0
        makes_contact true

        effects {
            VaporizeCorpse 1
        }
    }
}
```

---

### `Rebirth2`
**Name:** Rebirth  
**Description:** Teleport into a body, destroying it to heal 4 HP and gain All Stats Up.  
**Source:** `necromancer_abilities.gon`  

```
Rebirth2 {
    template teleport
    
    meta {
        name "ABILITY_REBIRTH_NAME"
        desc "ABILITY_REBIRTH2_DESC"
        animate_name true
        class Necromancer
        type_icon "misc"
    }

    graphics {
        animation_out digDown
        animation_in digUp
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        max_range 20
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    self_damage {
        damage 0

        effects {
            AllStatsUp 1
            HealthGain 4
        }
    }

    damage_instance {
        damage 0
        makes_contact true

        effects {
            VaporizeCorpse 1
        }
    }
}
```

---

### `Pestilence`
**Name:** Pestilence  
**Description:** Deal 1 damage to all units.  
**Source:** `necromancer_abilities.gon`  

```
Pestilence {
    template spell

    meta {
        name "ABILITY_PESTILENCE_NAME"
        desc "ABILITY_PESTILENCE_DESC"
        class Necromancer
    }

    graphics {
        particle PoisonPoof
		animation evilMagic
    }
    
    cost {
        mana 4
        infcantrip true
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

### `Pestilence2`
**Description:** Deal 1 damage to all units.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Pestilence2 {
    variant_of Pestilence

    meta {
        desc "ABILITY_PESTILENCE2_DESC"
    }

    
    cost {
        mana 3
    }
}
```

---

### `Weakness`
**Name:** Weakness  
**Description:** Inflict Weakness 5 on a unit.  
**Source:** `necromancer_abilities.gon`  

```
Weakness {
    template targeted_status
    
    meta {
        name "ABILITY_WEAKNESS_NAME"
        desc "ABILITY_WEAKNESS_DESC"
        class Necromancer
    }

    graphics {
        particle PoisonPoof
		animation evilMagic
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        max_aoe 0
        min_range 1
        max_range 4
    }
    
    damage_instance {
        damage 0
        effects {
            Weakness 5
        }
    }
}
```

---

### `Weakness2`
**Description:** Give a unit Weakness 5 and All Stats Down.  
**Source:** `necromancer_abilities.gon`  

```
Weakness2 {
    variant_of Weakness

    meta {
        desc "ABILITY_WEAKNESS2_DESC"
    }
    
    damage_instance {
        effects {
            AllStatsUp -1
        }
    }
}
```

---

### `SoulSuck`
**Name:** Dark Ritual  
**Description:** Destroy an adjacent body. The next spell you cast costs 0 mana.  
**Source:** `necromancer_abilities.gon`  

```
SoulSuck {
    template melee_attack
    
    meta {
        name "ABILITY_DARKRITUAL_NAME"
        desc "ABILITY_DARKRITUAL_DESC"
        class Necromancer
        type_icon "misc"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 2
    }

    target {
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 0
        type melee
        incidentally_collects_pickups false

        effects {
            VaporizeCorpse 1
            ApplyToSource {
                FreeSpell 1
            }
        }
    }
}
```

---

### `SoulSuck2`
**Description:** Destroy an adjacent body. The next 2 spells you cast cost 0 mana.  
**Source:** `necromancer_abilities.gon`  

```
SoulSuck2 {
    variant_of SoulSuck

    meta {
        desc "ABILITY_DARKRITUAL2_DESC"
    }

    damage_instance {
        effects {
            ApplyToSource {
                FreeSpell 2
            }
        }
    }
}
```

---

### `EvilIncarnate`
**Name:** Evil Incarnate  
**Description:** Inflict Fear on all enemies.  
**Source:** `necromancer_abilities.gon`  

```
EvilIncarnate {
    template spell

    meta {
        name "ABILITY_EVILINCARNATE_NAME"
        desc "ABILITY_EVILINCARNATE_DESC"
        class Necromancer
    }

    graphics {
        darken_screen true
        darken_screen_exclude_characters_on_tile false
        darken_screen_exclude_self true
        darken_screen_start_early true
		particle FearEffect
    }
    
    cost {
        mana 12
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions enemies_only
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

### `EvilIncarnate2`
**Description:** Inflict Fear 1 and Weakness 2 on all enemies.  
**Source:** `necromancer_abilities.gon`  

```
EvilIncarnate2 {
    variant_of EvilIncarnate

    meta {
        desc "ABILITY_EVILINCARNATE2_DESC"
    }

    cost {
        mana 12
    }

    damage_instance {
        effects {
            Weakness 2
        }
    }
}
```

---

### `SoulLink`
**Name:** Soul Link  
**Description:** Inflict Soul Link on units in an area.  
**Source:** `necromancer_abilities.gon`  

```
SoulLink {
    template targeted_status
    
    meta {
        name "ABILITY_SOULLINK_NAME"
        desc "ABILITY_SOULLINK_DESC"
        class Necromancer
    }

    graphics {
        particle PoisonPoof
		animation castspell
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        max_aoe 1
        min_range 0
        max_range 4
    }
    
    damage_instance {
        effects {
            SoulLink 1
        }
    }
}
```

---

### `SoulLink2`
**Description:** Inflict Soul Link on units in a large area.  
**Source:** `necromancer_abilities.gon`  

```
SoulLink2 {
    variant_of SoulLink

    meta {
        desc "ABILITY_SOULLINK2_DESC"
    }

    target {
        max_range 6
        max_aoe 2
    }
}
```

---

### `WeAreOne`
**Name:** We Are One  
**Description:** Inflict Soul Link on yourself and every enemy.  
**Source:** `necromancer_abilities.gon`  

```
WeAreOne {
    template spell

    meta {
        name "ABILITY_WEAREONE_NAME"
        desc "ABILITY_WEAREONE_DESC"
        class Necromancer
        type_icon "debuff"
    }
    
    cost {
        mana 15
        infcantrip true
    }

    graphics {
        particle PoisonPoof
		animation floatingmagic
    }
    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions enemies_only
    }

    self_damage {
        effects {
            SoulLink 1
        }
    }

    damage_instance {
        damage 0
        effects {
            SoulLink 1
        }
    }
}
```

---

### `WeAreOne2`
**Description:** Inflict Soul Link on yourself and every enemy. Gain +2 [img:con] and heal 8 HP.  
**Source:** `necromancer_abilities.gon`  

```
WeAreOne2 {
    variant_of WeAreOne

    meta {
        desc "ABILITY_WEAREONE2_DESC"
    }

    self_damage {
        heal 8
        effects {
            ConstitutionUp 2
        }
    }
}
```

---

### `BloodRain`
**Name:** Blood Rain  
**Description:** Take 1 damage and heal all allies 1 HP.  
**Source:** `necromancer_abilities.gon`  

```
BloodRain {
    template spell

    meta {
        name "ABILITY_BLOODRAIN_NAME"
        desc "ABILITY_BLOODRAIN_DESC"
        class Necromancer
    }

    graphics {
		particle none
		animation selfHarm
    }
    
    cost {
        mana 3
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions allies_only
        aoe_excludes_self true
    }

    self_damage {
        damage 1
    }

    damage_instance {
        heal 1
    }
}
```

---

### `BloodRain2`
**Description:** Take 1 damage, heal all allies 1 HP and give them +1 mana.  
**Source:** `necromancer_abilities.gon`  

```
BloodRain2 {
    variant_of BloodRain

    meta {
        desc "ABILITY_BLOODRAIN2_DESC"
    }

    damage_instance {
        effects {
            ManaGain 1
        }
    }
}
```

---

### `AnimateDead`
**Name:** Eternal Servitude  
**Description:** Resurrect an enemy body to full HP. It joins your team.  
**Source:** `necromancer_abilities.gon`  

```
AnimateDead {
    template spell
    
    meta {
        name "ABILITY_ETERNALSERVITUDE_NAME"
        desc "ABILITY_ETERNALSERVITUDE_DESC"
        class Necromancer
        type_icon "misc"
    }

    graphics {
        animation floatingmagic
        particle none
    }

    cost {
        infcantrip true
        mana 12
    }

    target {
        min_range 1
        max_range 4
        max_aoe 0
        aoe_restrictions [must_have_corpse enemies_only]
        restrictions aoe_must_exist
    }

    damage_instance {
        heal 0
        type spell
        can_revive true

        effects {
            HealPercentMaxHP 100
            FactionConversion 1
            CaptureFamiliar 1
        }
    }
}
```

---

### `AnimateDead2`
**Description:** Resurrect an enemy body to full HP. It joins your team and takes an extra turn after this one.  
**Source:** `necromancer_abilities.gon`  

```
AnimateDead2 {
    variant_of AnimateDead

    meta {
        desc "ABILITY_ETERNALSERVITUDE2_DESC"
    }

    damage_instance {
        effects {
            TakeExtraTurn 1
        }
    }
}
```

---

### `DeathBloom`
**Name:** Death Bloom  
**Description:** Explode a body, dealing damage and Knockback to adjacent units.  
**Source:** `necromancer_abilities.gon`  

```
DeathBloom {
    template targeted_status
    
    meta {
        name "ABILITY_DEATHBLOOM_NAME"
        desc "ABILITY_DEATHBLOOM_DESC"
        class Necromancer
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 0
    }

    target {
        max_range 20

        splash_damage_aoe_begin 1
        restrictions must_have_destructible_corpse
    }
    
    damage_instance {
        damage 0
        cant_miss true

        effects {
            ExplodeCharacter_DeathBloom 5
        }
    }
}
```

---

### `DeathBloom2`
**Name:** Death Bloom  
**Description:** Explode a body, dealing damage and Knockback to units in a large area.  
**Source:** `necromancer_abilities.gon`  

```
DeathBloom2 {
    template targeted_status

    meta {
        name "ABILITY_DEATHBLOOM_NAME"
        desc "ABILITY_DEATHBLOOM2_DESC"
        class Necromancer
    }

    cost {
        infcantrip true
        mana 0
    }

    target {
        max_range 20

        splash_damage_aoe_begin 1
        restrictions must_have_destructible_corpse
    }
    
    damage_instance {
        damage 0
        cant_miss true

        effects {
            ExplodeCharacter_DeathBloom2 5
        }
    }
}
```

---

### `Scare`
**Name:** Scare  
**Description:** Teleport in front of an enemy then Knockback each adjacent unit 4 tiles.  
**Source:** `necromancer_abilities.gon`  

```
Scare {
    template teleport
    
    meta {
        name "ABILITY_SCARE_NAME"
        desc "ABILITY_SCARE_DESC"
        animate_name true
        class Necromancer
        type_icon "movement"
    }

    graphics {
        animation_out teleportOut
        animation_in teleportIn
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        aoe_mode normal
        min_range 1
        max_range 20
        max_aoe 1
        restrictions [must_be_moveable must_be_directly_in_front_of_enemy]
        knockback_mode character_to_tile
    }

    damage_instance {
        damage 0
        knockback 4
        type spell

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `Scare2`
**Description:** Teleport in front of an enemy then inflict Knockback 4 and Fear on each adjacent unit.  
**Source:** `necromancer_abilities.gon`  

```
Scare2 {
    variant_of Scare

    meta {
        desc "ABILITY_SCARE2_DESC"
    }

    damage_instance {
        effects {
            Fear 1
        }
    }
}
```

---

### `SoulTransfer`
**Name:** Soul Transfer  
**Description:** Give a unit +1 [img:con] and heal it 4 HP. You gain -1 [img:con] and lose 4 health.  
**Source:** `necromancer_abilities.gon`  

```
SoulTransfer {
    template targeted_status
    
    meta {
        name "ABILITY_SOULTRANSFER_NAME"
        desc "ABILITY_SOULTRANSFER_DESC"
        class Necromancer
        type_icon "heal"
    }

    graphics {
        particle PoisonPoof
    }
    
    cost {
        infcantrip true
        mana 1
    }

    target {
        max_aoe 0
        min_range 1
        max_range 4

        X_is max_health
    }

    self_damage {
        damage 4
        piercing true
        cant_miss true

        effects {
            ConstitutionUp -1
        }
    }
    
    damage_instance {
        heal 4
        piercing true
        cant_miss true

        effects {
            ConstitutionUp 1
        }
    }
}
```

---

### `SoulTransfer2`
**Description:** Give a unit +1 [img:con] and heal it 4 HP. You gain -1 [img:con] and lose 4 health.
This spell can revive units. If the unit revived was an enemy it gets charmed for the battle.  
**Source:** `necromancer_abilities.gon`  

```
SoulTransfer2 {
    variant_of SoulTransfer

    meta {
        desc "ABILITY_SOULTRANSFER2_DESC"
    }

    damage_instance {
        can_revive true

        effects {
            Conditional_Corpse {
                PermanentCharm 1
            }
        }
    }
}
```

---

### `RandomReap`
**Source:** `necromancer_abilities.gon`  

```
RandomReap { //for death incarnate passive
    template spell
    
    graphics {
        animation floatingmagic
	    particle sytheCut

        darken_screen true
        darken_screen_exclude_characters_on_tile true
    }

    cost {
        infcantrip true
        mana 15
    }

    target {
        target_mode random_tile
        max_aoe 0
        max_range 20

        restrictions [must_have_living_character must_not_have_boss must_have_enemy]
    }

    damage_instance {
        damage 1
        cant_miss true
        can_instapop false
        effects {
            Instakill 25
        }
    }
}
```

---

### `RandomReap2`
**Source:** `necromancer_abilities.gon`  

```
RandomReap2 { //for death incarnate passive
    template spell

    graphics {
        animation floatingmagic
        particle sytheCut

        darken_screen true
        darken_screen_exclude_characters_on_tile true
    }

    cost {
        infcantrip true
        mana 15
    }

    target {
        target_mode random_tile
        max_aoe 0
        max_range 20

        restrictions [must_have_living_character must_have_enemy]
    }

    damage_instance {
        damage 1
        cant_miss true
        can_instapop false
        effects {
            Instakill 50
        }
    }
}
```

---

### `SlitWrists`
**Name:** Slit Wrists  
**Description:** Deal 2 damage to yourself.  
**Source:** `necromancer_abilities.gon`  

```
SlitWrists { //bonus ability for OneWithNothing passive
    template self_buff

    meta {
        name "ABILITY_SLITWRISTS_NAME"
        desc "ABILITY_SLITWRISTS_DESC"
        class Necromancer
    }

    graphics {
		animation selfHarm
    }
    
    cost {
        mana 1
        infcantrip true
    }

    damage_instance {
        damage 2
        type melee
    }
}
```

---

### `Whisper`
**Name:** Whisper  
**Description:** Inflict Fear and Madness on an adjacent unit.  
**Source:** `necromancer_abilities.gon`  

```
Whisper {
    template melee_spell
    
    meta {
        name "ABILITY_WHISPER_NAME"
        desc "ABILITY_WHISPER_DESC"
        class Necromancer
        type_icon "defense"
    }

    graphics {
        animation angry
		particle FearEffect
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        damage 0
        type status_spell
        incidentally_collects_pickups false

        effects {
            Fear 1
            Madness level
        }
    }
}
```

---

### `Whisper2`
**Description:** Inflict Fear 1 and Madness 2 on a unit in range 4.  
**Source:** `necromancer_abilities.gon`  

```
Whisper2 {
    variant_of Whisper

    meta {
        desc "ABILITY_WHISPER2_DESC"
    }

    target {
        target_mode tile
        aoe_mode standard
        max_range 4
        min_range 1
        min_aoe 0 
        max_aoe 0 
        aoe_considers_character_size false
    }
}
```

---

### `SummonShade`
**Name:** Summon Shade  
**Description:** Spawn a shadow copy of yourself that fades after its first turn.
\[s:.7\](The copy can't cast this ability or give extra turns to units.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
SummonShade {
    template spawn

    meta {
        name "ABILITY_SUMMONSHADE_NAME"
        desc "ABILITY_SUMMONSHADE_DESC"
        class Necromancer
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 13
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
        faction self

        catdata clone
        clone_items true

        additional_passives {
            SafeDoomed 1
            InjuryImmunity 1
        }
    }
}
```

---

### `SummonShade2`
**Description:** Spawn a shadow copy of yourself that fades after its second turn.
\[s:.7\](The copy can't cast this ability or give extra turns to units.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
SummonShade2 {
    variant_of SummonShade

    meta {
        desc "ABILITY_SUMMONSHADE2_DESC"
    }

    spawn {
        additional_passives {
            SafeDoomed 2
        }
    }
}
```

---

### `DarkStep`
**Name:** Dark Step  
**Description:** Teleport to an open tile.  
**Source:** `necromancer_abilities.gon`  

```
DarkStep {
    template teleport
    
    meta {
        name "ABILITY_DARKSTEP_NAME"
        desc "ABILITY_DARKSTEP_DESC"
        animate_name true
        class Necromancer
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 4
        //restrictions [aoe_must_be_displaceable]
    }
}
```

---

### `DarkStep2`
**Description:** Teleport to a tile. If you teleport into a unit you both take 5 damage, then inflict Fear on it.  
**Source:** `necromancer_abilities.gon`  

```
DarkStep2 {
    variant_of DarkStep

    meta {
        desc "ABILITY_DARKSTEP2_DESC"
    }

    target {
        restrictions [aoe_must_be_displaceable]
    }

    damage_instance {
        damage 5
        makes_contact true

        effects {
            IgnoreSelf 1
            Fear 1

            ApplyToSource {
                DoDamage {
                    damage 5
                    type melee
                }
            }
        }
    }
}
```

---

### `Leeches`
**Name:** Leeches  
**Description:** Inflict Leech 1 on a unit.  
**Source:** `necromancer_abilities.gon`  

```
Leeches {
    template lobbed_attack
    
    meta {
        name "ABILITY_LEECHES_NAME"
        desc "ABILITY_LEECHES_DESC"
        class Necromancer
    }

    graphics {
        projectile LeechProjectile
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        min_range 1
        max_range 3+bonus_range
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

### `Leeches2`
**Description:** Inflict Leech 1 and Mana Leech 1 on a unit.  
**Source:** `necromancer_abilities.gon`  

```
Leeches2 {
    variant_of Leeches

    meta {
        desc "ABILITY_LEECHES2_DESC"
    }

    damage_instance {
        effects {
            Leeches 1
            ManaLeeches 1
        }
    }
}
```

---

### `Shriek`
**Name:** Shriek  
**Description:** Inflict Fear 1, Confusion 2, and Madness 2 on units within a cone.  
**Source:** `necromancer_abilities.gon`  

```
Shriek {
    template spell

    meta {
        name "ABILITY_SHRIEK_NAME"
        desc "ABILITY_SHRIEK_DESC"
        class Necromancer
    }

    tags [musical]

    graphics {
	    animation sing3
	    particle FearEffect
    }
    
    cost {
        infcantrip true
        mana 9
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 3

        aoe_considers_character_size true
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0
        effects {
            Fear 1
            Confusion 2
            Madness 2
        }
    }
}
```

---

### `Shriek2`
**Description:** Inflict Fear 1, Confusion 2, Madness 2 and drain 2 HP from units within a cone.  
**Source:** `necromancer_abilities.gon`  

```
Shriek2 {
    variant_of Shriek
    
    meta {
        desc "ABILITY_SHRIEK2_DESC"
    }

    damage_instance {
        damage 2
        piercing true
        effects {
            Leech 1
        }
    }
}
```

---

### `LastGasp`
**Source:** `necromancer_abilities.gon`  

```
LastGasp { //util deathrattle for Last Gasp passive
    template spell

    graphics {
        particle PoisonPoof
        animation none
    }
    
    cost {
        mana 5
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_excludes_self true
        aoe_restrictions must_have_animate_character
    }

    damage_instance {
        damage 6

        effects {
            ContextualHeal 1
        }
    }
}
```

---

### `LastGasp2`
**Source:** `necromancer_abilities.gon`  

```
LastGasp2 {
    variant_of LastGasp

    damage_instance {
        damage 10

        effects {
            ContextualHeal 1
        }
    }
}
```

---

### `Seppuku`
**Name:** Seppuku  
**Description:** Down yourself.  
**Source:** `necromancer_abilities.gon`  

```
Seppuku { //bonus ability for Last Gasp passive
    template self_buff

    meta {
        name "ABILITY_SEPPUKU_NAME"
        desc "ABILITY_SEPPUKU_DESC"
        class Necromancer
    }

    graphics {
		animation selfHarm
        particle PoisonPoof
    }
    
    cost {
        mana 5
        infcantrip true
    }

    damage_instance {
        effects {
            Die 1
        }
    }
}
```

---

### `RaiseTheDead`
**Source:** `necromancer_abilities.gon`  

```
RaiseTheDead { //util ability for RelentlessDead passive
    template spawn

    tags [summon]
    
    graphics {
        lob false
        animation none
    }
    
    cost {
        mana 4
        infcantrip true
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        min_targets 1
        max_targets 1
        aoe_restrictions [must_be_empty]
    }

    spawn {
        object ZombieCatFamiliar
        lob false
    }
}
```

---

### `RaiseTheDead2`
**Source:** `necromancer_abilities.gon`  

```
RaiseTheDead2 { //util ability for RelentlessDead passive
    variant_of RaiseTheDead

    target {
        min_targets 2
        max_targets 2
    }
}
```

---

### `FullMoon`
**Name:** Full Moon  
**Description:** Give Lifesteal 1 to units in an area.  
**Source:** `necromancer_abilities.gon`  

```
FullMoon {
    template spell

    meta {
        name "ABILITY_BESTOWLEECHES_NAME"
        desc "ABILITY_BESTOWLEECHES_DESC"
        class Necromancer
    }

    graphics {
        animation floatingmagic
        particle Holybeam
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        max_aoe 1
        max_range 5
    }
    
    damage_instance {
        damage 0
        
        effects {
            Lifesteal 1
        }
    }
}
```

---

### `FullMoon2`
**Description:** Give Lifesteal 3 to units in an area.  
**Source:** `necromancer_abilities.gon`  

```
FullMoon2 {
    variant_of FullMoon

    meta {
        desc "ABILITY_BESTOWLEECHES2_DESC"
    }

    target {
        max_range 7
    }

    damage_instance {
        effects {
            Lifesteal 3
        }
    }
}
```

---

### `Unearth`
**Name:** Unearth  
**Description:** Dig up a body. It reanimates at the end of the round.  
**Source:** `necromancer_abilities.gon`  

```
Unearth {
    template spawn

    meta {
        name "ABILITY_UNEARTH_NAME"
        desc "ABILITY_UNEARTH_DESC"
        class Necromancer
    }

    tags [summon]

    graphics {
        animation dig
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_range 1
    }
    
    spawn {
        object ZombieCatFamiliar
        lob false
        start_dead true

        additional_passives {
            ReviveNextRound {
                revive_health 100%
            }
        }
    }
}
```

---

### `Unearth2`
**Description:** Dig up a body. It reanimates at the end of the round.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Unearth2 {
    variant_of Unearth

    meta {
        desc "ABILITY_UNEARTH2_DESC"
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 5
    }
}
```

---

### `BloodGeyser`
**Name:** Blood Geyser  
**Description:** Take damage equal to half of your max HP, then deal that much damage and inflict Fear 2 on another unit.  
**Source:** `necromancer_abilities.gon`  

```
BloodGeyser {
    template spell
    
    meta {
        name "ABILITY_BLOODGEYSER_NAME"
        desc "ABILITY_BLOODGEYSER_DESC"
        class Necromancer
    }

    graphics {
        particle bloodywave
    }
    
    cost {
        infcantrip true
        mana 6
    }

    target {
        max_aoe 0
        min_range 1
        max_range 4

        X_is max_health
    }

    self_damage {
        damage "ceil(X/2)"
        piercing true
        cant_miss true
    }
    
    damage_instance {
        damage "ceil(X/2)"

        effects {
            Fear 2
        }
    }
}
```

---

### `BloodGeyser2`
**Description:** Take damage equal to half of your max HP, then deal that much damage and inflict Fear 2 on units in an area.  
**Source:** `necromancer_abilities.gon`  

```
BloodGeyser2 {
    variant_of BloodGeyser

    meta {
        desc "ABILITY_BLOODGEYSER2_DESC"
    }

    target {
        max_aoe 2
        max_range 6
    }
}
```

---

### `Flatline`
**Name:** Flatline  
**Description:** Down yourself. You don't get injured. Spawn a shadow copy of yourself that fades after its first turn.
[s:.7]The copy can't cast this ability or give extra turns to units.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Flatline {
    template spawn

    meta {
        name "ABILITY_FLATLINE_NAME"
        desc "ABILITY_FLATLINE_DESC"
        class Necromancer
    }

    tags [summon]
    
    graphics {
        lob true
        animation none
    }
    
    cost {
        infcantrip true
        mana 3
        must_not_be_a_summon true
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    self_damage {
        effects {
            SafeDie 1
        }
    }

    spawn {
        object PlayerCat_Shade
        faction self

        catdata clone
        clone_items true

        additional_passives {
            SafeDoomed level
            InjuryImmunity 1
        }
    }
}
```

---

### `Flatline2`
**Description:** Down yourself. You don't get injured. Spawn a shadow copy of yourself that fades after its first turn.
[s:.7]The copy can't cast this ability or give extra turns to units.\[/s\]
\[s:.7\](This spell costs 0 mana.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Flatline2 {
    variant_of Flatline

    meta {
        desc "ABILITY_FLATLINE2_DESC"
    }

    cost {
        mana 0
    }

    spawn {
        additional_passives {
            FillMana 1
        }
    }
}
```

---

### `Replace`
**Name:** Replace  
**Description:** Teleport into a familiar and destroy it. Refresh your basic attack.  
**Source:** `necromancer_abilities.gon`  

```
Replace {
    template teleport
    
    meta {
        name "ABILITY_REPLACE_NAME"
        desc "ABILITY_REPLACE_DESC"
        animate_name true
        class Necromancer
        type_icon "movement"
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        min_range 1
        max_range 20

        restrictions aoe_must_exist
        aoe_restrictions familiars_only
    }

    self_damage {
        effects {
             RefreshActPoints 1
        }
    }

    damage_instance {
        damage 0

        effects {
            IgnoreSelf 1
            VaporizeTarget 1
        }
    }
}
```

---

### `Replace2`
**Description:** Teleport into a familiar and destroy it. Refresh your basic attack and heal 5 HP.  
**Source:** `necromancer_abilities.gon`  

```
Replace2 {
    variant_of Replace

    meta {
        desc "ABILITY_REPLACE2_DESC"
    }

    self_damage {
        effects {
             HealthGain 5
        }
    }
}
```

---

### `SummonBones`
**Name:** Summon Bones  
**Description:** Summon a skeleton from a body.  
**Source:** `necromancer_abilities.gon`  

```
SummonBones {
    template spell
    
    graphics {
        animation floatingmagic
        particle none
    }
	
    meta {
        name "ABILITY_SUMMONBONES_NAME"
        desc "ABILITY_SUMMONBONES_DESC"
        class Necromancer
        type_icon "spawn"
    }

    tags [summon]

    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 4
        max_aoe 0
        restrictions must_have_destructible_corpse
    }

    damage_instance {
        damage 0

        effects {
            VaporizeCorpse 1
            ObjectOnHitCharacter SkeletonCatFamiliar
        }
    }
}
```

---

### `SummonBones2`
**Description:** Summon a skeleton from a body, anywhere.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
SummonBones2 {
    variant_of SummonBones

    meta {
        desc "ABILITY_SUMMONBONES2_DESC"
    }

    cost {
        mana 4
    }

    target {
        max_range 20
    }
}
```

---

### `GigaDrain`
**Name:** Giga Drain  
**Description:** Spend all of your mana, then drain that much HP from an adjacent unit. Ignores shield.  
**Source:** `necromancer_abilities.gon`  

```
GigaDrain {
    template melee_attack

    meta {
        name "ABILITY_GIGADRAIN_NAME"
        desc "ABILITY_GIGADRAIN_DESC"
        class Necromancer
        type_icon "magic"
    }

    graphics {
        animation floatingmagic
    }
    
    cost {
        mana X
        infcantrip true
        X_cant_be_zero true
        disallow_cost_modification true
    }

    target {
        X_is current_mana
    }
    
    damage_instance {
        damage X
        type spell
        piercing true

        effects {
            Leech 1
        }
    }
}
```

---

### `GigaDrain2`
**Description:** Spend all of your mana, then drain that much HP from a unit in range 3. Ignores shield.  
**Source:** `necromancer_abilities.gon`  

```
GigaDrain2 {
    variant_of GigaDrain

    meta {
        desc "ABILITY_GIGADRAIN2_DESC"
    }

    target {
        target_mode tile
        max_range 3
        min_aoe 0
        max_aoe 0
        restrictions none
    }
}
```

---

### `Bloodletting`
**Name:** Bloodletting  
**Description:** Remove all status effects from another unit, then inflict Bleed 5 on it.  
**Source:** `necromancer_abilities.gon`  

```
Bloodletting {
    template targeted_status
    
    meta {
        name "ABILITY_BLOODLETTING_NAME"
        desc "ABILITY_BLOODLETTING_DESC"
        class Necromancer
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 8
    }

    target {
        max_aoe 0
        min_range 1
        max_range 3
    }
    
    damage_instance {
        damage 0
        effects {
            Cleanse 0
            Purge 0
            Bleed 5
        }
    }
}
```

---

### `Bloodletting2`
**Description:** Remove all status effects from another unit, then inflict Bleed 5 on it.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Bloodletting2 {
    variant_of Bloodletting

    meta {
        desc "ABILITY_BLOODLETTING2_DESC"
    }

    cost {
        infcantrip true
        mana 4
    }
}
```

---

### `MassPsychosis`
**Name:** Mass Psychosis  
**Description:** Inflict Madness on all enemies.  
**Source:** `necromancer_abilities.gon`  

```
MassPsychosis {
    template spell

    meta {
        name "ABILITY_MASSPSYCHOSIS_NAME"
        desc "ABILITY_MASSPSYCHOSIS_DESC"
        class Necromancer
    }

    graphics {
        darken_screen true
        darken_screen_exclude_characters_on_tile false
        darken_screen_exclude_self true
        darken_screen_start_early true
        particle FearEffect
        animation floatingmagic
    }
    
    cost {
        mana 15
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions enemies_only
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

### `MassPsychosis2`
**Description:** Inflict Madness on all enemies.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
MassPsychosis2 {
    variant_of MassPsychosis

    meta {
        desc "ABILITY_MASSPSYCHOSIS2_DESC"
    }

    cost {
        mana 11
    }
}
```

---

### `Debone`
**Name:** Debone  
**Description:** Deal damage and inflict Weakness on an adjacent unit. If you have no weapon, equip a bone.  
**Source:** `necromancer_abilities.gon`  

```
Debone {
    template melee_attack

    meta {
        name "ABILITY_DEBONE_NAME"
        desc "ABILITY_DEBONE_DESC"
        class Necromancer
    }

    graphics {
        animation sliceOpen
    }
    
    cost {
        mana 7
        infcantrip true
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage

        effects {
            Weakness 1
            ApplyToSource {
                EquipPermanentItem BoneClub
            }
        }
    }
}
```

---

### `Debone2`
**Description:** Deal damage, inflict Weakness and Immobile on an adjacent unit. If you have no weapon, equip a bone.  
**Source:** `necromancer_abilities.gon`  

```
Debone2 {
    variant_of Debone

    meta {
        desc "ABILITY_DEBONE2_DESC"
    }
    damage_instance {
        effects {
            Immobile 1
        }
    }
}
```

---

### `Reap`
**Name:** Reap  
**Description:** Teleport into a unit with 5 or less health and destroy it.  
**Source:** `necromancer_abilities.gon`  

```
Reap {
    template teleport
    
    meta {
        name "ABILITY_REAP_NAME"
        desc "ABILITY_REAP_DESC"
        animate_name true
        class Necromancer
        type_icon "movement"
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
		particle sytheCut
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        min_range 1
        max_range 20

        restrictions aoe_must_exist
        aoe_restrictions must_have_low_health_character
        low_health_character_threshold 5
    }

    damage_instance {
        damage 0

        effects {
            IgnoreSelf 1
            VaporizeTarget 1
            VisualFXTile sytheCut
        }
    }
}
```

---

### `Reap2`
**Description:** Teleport into a unit with 10 or less health and destroy it.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Reap2 {
    variant_of Reap

    meta {
        desc "ABILITY_REAP2_DESC"
    }

    cost {
        mana 5
    }

    target {
        low_health_character_threshold 10
    }
}
```

---

### `Haunt`
**Name:** Haunt  
**Description:** Damage any unit and inflict Fear.
[s:.7]Castable while downed.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Haunt {
    template spell

    meta {
        name "ABILITY_HAUNT_NAME"
        desc "ABILITY_HAUNT_DESC"
    }

    graphics {
        particle MagicMissleBlast
        animation none
		particle FearEffect
    }
    
    cost {
        move_points 0
        act_points 1
        can_cast_while_dead true
    }
    
    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 5+bonus_basic_spell_damage
        effects {
            Fear 1
        }
    }
}
```

---

### `Spook`
**Name:** Spook  
**Description:** Deal damage to any unit. This has a 25% chance to inflict Fear.
[s:.7]Castable while downed.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Spook {
    template spell

    meta {
        name "ABILITY_SPOOK_NAME"
        desc "ABILITY_SPOOK_DESC"
    }

    graphics {
        particle MagicMissleBlast
        animation none
		particle FearEffect
    }
    
    cost {
        cantrip true
        can_cast_while_dead true
    }
    
    target {
        max_aoe 0
        max_range 20
    }
    
    damage_instance {
        damage 3+bonus_basic_spell_damage
        effects {
            Fear [1 .25]
        }
    }
}
```

---

### `CarrionShot`
**Name:** Carrion Shot  
**Description:** Deal 1 damage and inflict Leech 1.
[s:.7]This spell is stronger and castable while you're downed.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
CarrionShot {
    template lobbed_attack
    
    meta {
        name "ABILITY_CARRIONSHOT_NAME"
        desc "ABILITY_CARRIONSHOT_DESC"
        class Necromancer
    }

    graphics {
		projectile LeechProjectile
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 3+bonus_range
    }

    bonus_passives {
        DeadAltAbility CarrionShot_Afterlife
    }

    damage_instance {
        damage 1

        effects {
            Leeches 1
        }
    }
}
```

---

### `CarrionShot_Afterlife`
**Name:** Carrion Shot  
**Description:** Deal 1 damage and inflict Leech 1.
[s:.7]This spell is stronger and castable while you're downed.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
CarrionShot_Afterlife {
    template lobbed_attack
    
    meta { //SAME TOOLTIP AND NAME AS THE LIVING VERSION, USE THE SAME LOCALIZATION KEY
        name "ABILITY_CARRIONSHOT_NAME"
        desc "ABILITY_CARRIONSHOT_DESC"
        class Necromancer
    }

    graphics {
        animation none
    }

    cost {
        cantrip true
        mana 0
        can_cast_while_dead true
    }

    target {
        min_range 1
        max_range 20
    }

    damage_instance {
        damage 5+bonus_ranged_damage

        effects {
            Leeches 1
        }
    }
}
```

---

### `CarrionShot2`
**Description:** Deal 2 damage and inflict Leech 2.
[s:.7]This spell is stronger and castable while you're downed.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
CarrionShot2 {
    variant_of CarrionShot

    meta {
        desc "ABILITY_CARRIONSHOT2_DESC"
    }

    bonus_passives {
        DeadAltAbility CarrionShot_Afterlife2
    }
    
    damage_instance {
        damage 2

        effects {
            Leeches 2
        }
    }
}
```

---

### `CarrionShot_Afterlife2`
**Description:** Deal 2 damage and inflict Leech 2.
[s:.7]This spell is stronger and castable while you're downed.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
CarrionShot_Afterlife2 {
    variant_of CarrionShot_Afterlife

    meta { //SAME TOOLTIP AND NAME AS THE LIVING VERSION, USE THE SAME LOCALIZATION KEY
        desc "ABILITY_CARRIONSHOT2_DESC"
    }

    damage_instance {
        damage 8+bonus_ranged_damage

        effects {
            Leeches 2
        }
    }
}
```

---

### `LifeDrain`
**Name:** Lifedrain  
**Description:** Drain 2 HP at melee range.
[s:.7]This spell is much stronger and castable while you're downed. If this kills a unit, revive with 50% hp.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
LifeDrain {
    template spell
    
    meta {
        name "ABILITY_LIFEDRAIN_NAME"
        desc "ABILITY_LIFEDRAIN_DESC"
        class Necromancer
    }

    graphics {
        animation floatingmagic
		particle none
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 1
        max_aoe 0
    }

    bonus_passives {
        DeadAltAbility LifeDrain_Afterlife
    }

    damage_instance {
        damage 2

        effects {
            Leech 1
        }
    }
}
```

---

### `LifeDrain_Afterlife`
**Name:** Lifedrain  
**Description:** Drain 2 HP at melee range.
[s:.7]This spell is much stronger and castable while you're downed. If this kills a unit, revive with 50% hp.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
LifeDrain_Afterlife {
    template spell
    
    meta {
        name "ABILITY_LIFEDRAIN_NAME" //SAME TOOLTIP AND NAME AS THE LIVING VERSION, USE THE SAME LOCALIZATION KEY
        desc "ABILITY_LIFEDRAIN_DESC"
        class Necromancer
    }

    graphics {
        animation none
		particle SpookyDarkness
    }

    cost {
        cantrip true
        mana 0
        can_cast_while_dead true
    }

    target {
        min_range 1
        max_range 1
        max_aoe 0
    }

    damage_instance {
        damage 10

        effects {
            ApplyToSourceOnKill {
                Revive 50%
            }
            Leech 1
        }
    }
}
```

---

### `LifeDrain2`
**Description:** Drain 2 HP at melee range.
[s:.7]This spell is much stronger and castable while you're downed. If this kills a unit, revive with max hp.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
LifeDrain2 {
    variant_of LifeDrain

    meta {
        desc "ABILITY_LIFEDRAIN2_DESC"
    }

    target {
        max_range 2
    }

    bonus_passives {
        DeadAltAbility LifeDrain_Afterlife2
    }
}
```

---

### `LifeDrain_Afterlife2`
**Description:** Drain 2 HP at melee range.
[s:.7]This spell is much stronger and castable while you're downed. If this kills a unit, revive with max hp.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
LifeDrain_Afterlife2 {
    variant_of LifeDrain_Afterlife

    meta {
        desc "ABILITY_LIFEDRAIN2_DESC"
    }

    target {
        max_range 2
    }

    damage_instance {
        damage 10

        effects {
            ApplyToSourceOnKill {
                Revive 100%
            }
            Leech 1
        }
    }
}
```

---

### `CoffinFlop`
**Name:** Coffin Flop  
**Description:** Jump to an open tile in range 2.
[s:.7]This spell is stronger and castable while you're downed. When downed you can land on units dealing damage and inflicting Madness. \[/s\]  
**Source:** `necromancer_abilities.gon`  

```
CoffinFlop {
    template jump_attack

    meta {
        name "ABILITY_COFFINFLOP_NAME"
        desc "ABILITY_COFFINFLOP_DESC"
        class Necromancer
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 6
        infcantrip true
    }

    bonus_passives {
        DeadAltAbility CoffinFlop_Afterlife
    }
    
    target {
        max_range 2

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
    }

    damage_instance {
        type none
        damage 0
    }
}
```

---

### `CoffinFlop_Afterlife`
**Name:** Coffin Flop  
**Description:** Jump to an open tile in range 2.
[s:.7]This spell is stronger and castable while you're downed. When downed you can land on units dealing damage and inflicting Madness. \[/s\]  
**Source:** `necromancer_abilities.gon`  

```
CoffinFlop_Afterlife {
    template jump_attack

    meta {
        name "ABILITY_COFFINFLOP_NAME"
        desc "ABILITY_COFFINFLOP_DESC"
        class Necromancer
    }

    graphics {
        jump_start_animation none
        jump_attack_animation none
        land_animation none
    }

    cost {
        cantrip true
        mana 0
        can_cast_while_dead true
    }
    
    target {
        max_range 5

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
            Madness 1
        }
    }
}
```

---

### `CoffinFlop2`
**Description:** Jump to an open tile in range 3.
[s:.7]This spell is stronger and castable while you're downed. When downed you can land on units anywhere dealing damage and inflicting Madness 2. \[/s\]  
**Source:** `necromancer_abilities.gon`  

```
CoffinFlop2 {
    variant_of CoffinFlop

    meta {
        desc "ABILITY_COFFINFLOP2_DESC"
    }

    target {
        max_range 3
    }

    bonus_passives {
        DeadAltAbility CoffinFlop_Afterlife2
    }
}
```

---

### `CoffinFlop_Afterlife2`
**Description:** Jump to an open tile in range 3.
[s:.7]This spell is stronger and castable while you're downed. When downed you can land on units anywhere dealing damage and inflicting Madness 2. \[/s\]  
**Source:** `necromancer_abilities.gon`  

```
CoffinFlop_Afterlife2 {
    variant_of CoffinFlop_Afterlife

    meta {
        desc "ABILITY_COFFINFLOP2_DESC"
    }

    target {
        max_range 20
    }

    damage_instance {
        damage 4+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
            Madness 2
        }
    }
}
```

---

### `DonateBlood`
**Name:** Donate Blood  
**Description:** Heal a unit 5 HP, then take 10 damage.
[s:.7]Castable while you're downed. If you do, take no damage and give what you heal All Stats Up.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
DonateBlood {
    template spell

    meta {
        name "ABILITY_DONATEBLOOD_NAME"
        desc "ABILITY_DONATEBLOOD_DESC"
        class Necromancer
    }

    graphics {
        particle none
		animation selfHarm
    }
    
    cost {
        mana 6
        infcantrip true
    }

    
    target {
        min_range 1
        max_range 3
        max_aoe 0
    }

    bonus_passives {
        DeadAltAbility DonateBlood_Afterlife
    }

    self_damage {
        damage 10
    }

    damage_instance {
        heal 5
    }
}
```

---

### `DonateBlood_Afterlife`
**Name:** Donate Blood  
**Description:** Heal a unit 5 HP, then take 10 damage.
[s:.7]Castable while you're downed. If you do, take no damage and give what you heal All Stats Up.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
DonateBlood_Afterlife {
    template spell

    meta {
        name "ABILITY_DONATEBLOOD_NAME"
        desc "ABILITY_DONATEBLOOD_DESC"
        class Necromancer
    }

    graphics {
        animation none
		particle none
    }
    
    cost {
        cantrip true
        mana 0
        can_cast_while_dead true
    }

    target {
        min_range 1
        max_range 3
        max_aoe 0
    }

    damage_instance {
        heal 5

        effects {
            AllStatsUp 1
        }
    }
}
```

---

### `DonateBlood2`
**Description:** Heal all units in an area 5 HP, then take 10 damage.
[s:.7]Castable while you're downed. If you do, take no damage and give what you heal All Stats Up.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
DonateBlood2 {
    variant_of DonateBlood

    meta {
        desc "ABILITY_DONATEBLOOD2_DESC"
    }

    bonus_passives {
        DeadAltAbility DonateBlood_Afterlife2
    }

    target {
        max_range 5
        max_aoe 1
    }
}
```

---

### `DonateBlood_Afterlife2`
**Description:** Heal all units in an area 5 HP, then take 10 damage.
[s:.7]Castable while you're downed. If you do, take no damage and give what you heal All Stats Up.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
DonateBlood_Afterlife2 {
    variant_of DonateBlood_Afterlife

    meta {
        desc "ABILITY_DONATEBLOOD2_DESC"
    }

    target {
        max_range 5
        max_aoe 1
    }
}
```

---

### `Seance`
**Name:** Seance  
**Description:** Spawn a ghost Familiar that fades after its first turn.
[s:.7]Castable while you're downed. If you do, spawn a shadow copy of yourself instead.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Seance {
    template spawn

    meta {
        name "ABILITY_SEANCE_NAME"
        desc "ABILITY_SEANCE_DESC"
        class Necromancer
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    bonus_passives {
        DeadAltAbility Seance_Afterlife
    }

    spawn {
        object Spookie
        faction self

        additional_passives {
            SafeDoomed 1
        }
    }
}
```

---

### `Seance_Afterlife`
**Name:** Seance  
**Description:** Spawn a ghost Familiar that fades after its first turn.
[s:.7]Castable while you're downed. If you do, spawn a shadow copy of yourself instead.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Seance_Afterlife {
    template spawn

    meta {
        name "ABILITY_SEANCE_NAME"
        desc "ABILITY_SEANCE_DESC"
        class Necromancer
    }

    tags [summon]
    
    graphics {
        lob true
        animation none
    }
    
    cost {
        cantrip true
        mana 0
        can_cast_while_dead true
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
        faction self

        catdata clone
        clone_items true

        additional_passives {
            SafeDoomed 1
            InjuryImmunity 1
        }
    }
}
```

---

### `Seance2`
**Description:** Spawn a ghost Familiar that fades after its second turn.
[s:.7]Castable while you're downed. If you do, spawn a shadow copy of yourself instead.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Seance2 {
    variant_of Seance

    meta {
        desc "ABILITY_SEANCE2_DESC"
    }

    bonus_passives {
        DeadAltAbility Seance_Afterlife2
    }

    spawn {
        additional_passives {
            SafeDoomed 2
        }
    }
}
```

---

### `Seance_Afterlife2`
**Description:** Spawn a ghost Familiar that fades after its second turn.
[s:.7]Castable while you're downed. If you do, spawn a shadow copy of yourself instead.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Seance_Afterlife2 {
    variant_of Seance_Afterlife

    meta {
        desc "ABILITY_SEANCE2_DESC"
    }

    spawn {
        additional_passives {
            SafeDoomed 2
        }
    }
}
```

---

### `GoLimp`
**Name:** Go Limp  
**Description:** Until your next turn, you won't get injured if you're downed.  
**Source:** `necromancer_abilities.gon`  

```
GoLimp {
    template self_buff

    meta {
        name "ABILITY_GOLIMP_NAME"
        desc "ABILITY_GOLIMP_DESC"
        class Necromancer
    }
	
    graphics {
        animation hithard
    }

    cost {
        mana 4
        infcantrip true
    }

    damage_instance {
        effects {
            TempInjuryImmunity 1
        }
    }
}
```

---

### `GoLimp2`
**Description:** Until your next turn, you won't get injured if you're downed.
When downed, inflict Confusion 10 on the unit that downed you.  
**Source:** `necromancer_abilities.gon`  

```
GoLimp2 {
    variant_of GoLimp

    meta {
        desc "ABILITY_GOLIMP2_DESC"
    }

    bonus_passives {
         StatusKillers {
             Confusion 10
         }
    }
}
```

---

### `DemonicPact`
**Name:** Demonic Pact  
**Description:** Injure yourself and take an extra turn.
\[s:.7\](This spell can't be cast on extra turns.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
DemonicPact {
    template self_buff
    
    meta {
        name "ABILITY_DEMONICPACT_NAME"
        desc "ABILITY_DEMONICPACT_DESC"
        class Necromancer
        type_icon "misc"
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 10
        main_turn_only true
    }
    
    damage_instance {
        effects {
            RandomInjury 1
            TakeExtraTurn 1
        }
    }
}
```

---

### `DemonicPact2`
**Description:** Injure yourself and take an extra turn.
\[s:.7\](This spell costs less. This spell can't be cast on extra turns.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
DemonicPact2 {
    variant_of DemonicPact

    meta {
        desc "ABILITY_DEMONICPACT2_DESC"
    }

    cost {
        mana 7
    }
}
```

---

### `RandomSoulLink`
**Source:** `necromancer_abilities.gon`  

```
RandomSoulLink { //for soul bind passive, does not need an icon
    template spell

	graphics {
        particle PoisonPoof
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
            SoulLink 1
        }
    }
}
```

---

### `RandomDualSoulLink`
**Source:** `necromancer_abilities.gon`  

```
RandomDualSoulLink { //for Raven Feather item, does not need an icon
    template spell

	graphics {
        particle PoisonPoof
    }

    target {
        target_mode none
        aoe_mode all
		aoe_restrictions enemies_only
		max_targets 2
    }

    damage_instance {
        damage 0
        cant_miss true
        effects {
            SoulLink 1
        }
    }
}
```

---

### `Curse`
**Name:** Curse  
**Description:** Give a unit -4 [img:lck].  
**Source:** `necromancer_abilities.gon`  

```
Curse {
    template targeted_status
    
    meta {
        name "ABILITY_CURSE_NAME"
        desc "ABILITY_CURSE_DESC"
        class Necromancer
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        min_range 1
        max_range 3
    }

    damage_instance {
        effects {
            LuckUp -4
        }
    }
}
```

---

### `Curse2`
**Description:** Give a unit -4 [img:lck].
\[s:.7\](This spell has increased range)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Curse2 {
    variant_of Curse
    
    meta {
        desc "ABILITY_CURSE2_DESC"
    }

    target {
        max_range 8
    }
}
```

---

### `LeechSwarm`
**Name:** Leech Swarm  
**Description:** Inflict Leech 3 on all units, except yourself.  
**Source:** `necromancer_abilities.gon`  

```
LeechSwarm {
    template lobbed_attack

    meta {
        name "ABILITY_LEECHSWARM_NAME"
        desc "ABILITY_LEECHSWARM_DESC"
        class Necromancer
    }

    graphics {
	projectile LeechProjectile
    }
    
    cost {
        mana 12
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        aoe_excludes_self true
        knockback_mode zero
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            Leeches 3
        }
    }
}
```

---

### `LeechSwarm2`
**Description:** Inflict Leech 1 on each allied unit and Leech 3 on all other units, except yourself.  
**Source:** `necromancer_abilities.gon`  

```
LeechSwarm2 {
    variant_of LeechSwarm

    meta {
        desc "ABILITY_LEECHSWARM2_DESC"
    }

    damage_instance {
        effects {
            Leeches 1

            Conditional_Ally {
            } Else {
                Leeches 2
            }
        }
    }
}
```

---

### `Feed`
**Name:** Feed  
**Description:** Destroy an adjacent body. Your basic attack inflicts +1 Leech for the rest of the battle.  
**Source:** `necromancer_abilities.gon`  

```
Feed {
    template melee_attack
    
    meta {
        name "ABILITY_FEED_NAME"
        desc "ABILITY_FEED_DESC"
        class Necromancer
        type_icon "misc"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 2
    }

    target {
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 0
        incidentally_collects_pickups false

        effects {
            VaporizeCorpse 1
            ApplyToSource {
                AddLeechesStatus 1
            }
        }
    }
}
```

---

### `Feed2`
**Name:** Feed  
**Description:** Destroy a body at range. Your basic attack inflicts +1 Leech for the rest of the battle.  
**Source:** `necromancer_abilities.gon`  

```
Feed2 {
    template targeted_status
    
    meta {
        name "ABILITY_FEED_NAME"
        desc "ABILITY_FEED2_DESC"
        class Necromancer
        type_icon "misc"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 2
    }

    target {
        max_range 5
        aoe_restrictions must_have_destructible_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 0
        incidentally_collects_pickups false

        effects {
            VaporizeCorpse 1
            ApplyToSource {
                AddLeechesStatus 1
            }
        }
    }
}
```

---

### `Hush`
**Name:** Hush  
**Description:** Inflict Sleep 1 on an adjacent unit.  
**Source:** `necromancer_abilities.gon`  

```
Hush {
    template targeted_status
    
    meta {
        name "ABILITY_HUSH_NAME"
        desc "ABILITY_HUSH_DESC"
        class Necromancer
        type_icon "misc"
    }

    tags [musical]

    graphics {
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        max_range 1
    }

    damage_instance {
        effects {
            Sleep 1
        }
    }
}
```

---

### `Hush2`
**Description:** Inflict Sleep 1 on a unit in range 4.  
**Source:** `necromancer_abilities.gon`  

```
Hush2 {
    variant_of Hush

    meta {
        desc "ABILITY_HUSH2_DESC"
    }

    target {
        max_range 4
    }
}
```

---

### `ReaperStep`
**Name:** Reaper Step  
**Description:** Teleport to an open tile in range 1. Whenever a unit dies, this spell's range increases by 1.  
**Source:** `necromancer_abilities.gon`  

```
ReaperStep {
    template teleport
    
    meta {
        name "ABILITY_REAPERSTEP_NAME"
        desc "ABILITY_REAPERSTEP_DESC"
        animate_name true
        class Necromancer
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 6
    }

    bonus_passives {
        XIsCountDeaths 1
    }

    target {
        max_range 1+X
        X_is custom
    }
}
```

---

### `ReaperStep2`
**Description:** Teleport to a tile in range 1, dealing damage to units you land on. Whenever a unit dies, this spell's range and damage increase by 1.  
**Source:** `necromancer_abilities.gon`  

```
ReaperStep2 {
    variant_of ReaperStep

    meta {
        desc "ABILITY_REAPERSTEP2_DESC"
    }

    target {
        restrictions [aoe_must_be_displaceable]
    }

    damage_instance {
        damage 1+X
        makes_contact true

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `ForbiddenFamine`
**Name:** Forbidden Famine  
**Description:** Inflict Weakness 5, Poison 2, and Madness 2 on all enemies.
There are permanent consequences for casting this spell… but maybe not for you. 
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
ForbiddenFamine {
    template spell

    meta {
        name "ABILITY_FORBIDDENFAMINE_NAME"
        desc "ABILITY_FORBIDDENFAMINE_DESC"
        class Necromancer
    }

    graphics {
        animation floatingmagic
        particle PoisonPoof
    }
    
    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions enemies_only
    }

    self_damage {
        effects {
            Conditional_GoodRoll {
                odds 90%
                ApplyToRandomPartyMemberIfPossible {
                    GainDisorderFromPool_PostCast forbidden_spell_consequences
                }
            } Else {
                ApplyToRandomPartyMemberIfPossible {
                    GainDisorderFromPool_PostCast forbidden_spell_consequences_crippling
                }
            }
        }
    }

    damage_instance {
        damage 0

        effects {
            Weakness 5
            Poison 2
            Madness 2
        }
    }
}
```

---

### `ForbiddenFamine2`
**Description:** Inflict Leech 2, Weakness 5, Poison 2, and Madness 2 on all enemies.
There are permanent consequences for casting this spell… but maybe not for you. 
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
ForbiddenFamine2 {
    variant_of ForbiddenFamine

    meta {
        desc "ABILITY_FORBIDDENFAMINE2_DESC"
    }

    damage_instance {
        damage 0

        effects {
            Weakness 5
            Poison 5
            Madness 2
            Leeches 2
        }
    }
}
```

---

### `FleshGolem`
**Name:** Flesh Golem  
**Description:** You and all allies lose 7 HP. Summon a flesh golem with one random spell from each of those units.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
FleshGolem {
    template spawn

    meta {
        name "ABILITY_FLESHGOLEM_NAME"
        desc "ABILITY_FLESHGOLEM_DESC"
        class Necromancer
    }

    tags [summon]
    
    graphics {
        lob true
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    self_damage {
        effects {
            DrainAllyCatsForFleshGolem 7
        }
    }

    spawn {
        object PlayerCat_FleshGolem
        catdata fleshgolem
        appearance GolemCat
        faction self
    }
}
```

---

### `FleshGolem2`
**Description:** You and all allies lose 7 HP. Summon a flesh golem with one random spell and random passives from each of those units.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
FleshGolem2 {
    variant_of FleshGolem

    meta {
        desc "ABILITY_FLESHGOLEM2_DESC"
    }

    spawn {
        include_passives true
    }
}
```

---

### `TradeLife`
**Name:** Trade Life  
**Description:** Swap HP with an ally in range 3.
[s:.7]Castable while you're downed. If this spell downs you or the ally, neither are injured.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
TradeLife {
    template spell
    
    meta {
        name "ABILITY_TRADELIFE_NAME"
        desc "ABILITY_TRADELIFE_DESC"
        class Necromancer
    }

    graphics {
        animation floatingmagic
        particle none
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 1
        max_range 3
        max_aoe 0

        restrictions [must_have_ally must_not_have_boss]
    }

    bonus_passives {
        DeadAltAbility TradeLife_Afterlife
    }

    damage_instance {
        damage 0

        effects {
            TradeLife 1
        }
    }
}
```

---

### `TradeLife2`
**Description:** Swap HP with any ally.
[s:.7]Castable while you're downed. If this spell downs you or the ally, neither are injured.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
TradeLife2 {
    variant_of TradeLife

    meta {
        desc "ABILITY_TRADELIFE2_DESC"
    }

    bonus_passives {
        DeadAltAbility TradeLife_Afterlife2
    }

    target {
        max_range 20
    }
}
```

---

### `TradeLife_Afterlife`
**Name:** Trade Life  
**Description:** Swap HP with an ally in range 3.
[s:.7]Castable while you're downed. If this spell downs you or the ally, neither are injured.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
TradeLife_Afterlife {
    template spell
    
    meta {
        name "ABILITY_TRADELIFE_NAME" //SAME TOOLTIP AND NAME AS THE LIVING VERSION, USE THE SAME LOCALIZATION KEY
        desc "ABILITY_TRADELIFE_DESC"
        class Necromancer
    }

    graphics {
        animation none
        particle none
    }

    cost {
        cantrip true
        mana 0
        can_cast_while_dead true
    }

    target {
        min_range 1
        max_range 3
        max_aoe 0

        restrictions [must_have_ally must_not_have_boss]
    }

    damage_instance {
        damage 0

        effects {
            TradeLife 1
        }
    }
}
```

---

### `TradeLife_Afterlife2`
**Description:** Swap HP with any ally.
[s:.7]Castable while you're downed. If this spell downs you or the ally, neither are injured.\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
TradeLife_Afterlife2 {
    variant_of TradeLife_Afterlife

    meta {
        desc "ABILITY_TRADELIFE2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `AbsorbSoul`
**Name:** Absorb Soul  
**Description:** Down an ally in range 5 and steal their mana. It doesn't get injured.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
AbsorbSoul {
    template spell
    
    meta {
        name "ABILITY_ABSORBSOUL_NAME"
        desc "ABILITY_ABSORBSOUL_DESC"
        class Necromancer
    }

    graphics {
        animation floatingmagic
        particle none
    }

    cost {
        cantrip true
        mana 0
    }

    target {
        min_range 1
        max_range 5
        max_aoe 0

        restrictions [must_have_ally must_not_have_boss must_have_living_character]
    }

    damage_instance {
        damage 0

        effects {
            ManaSteal -1
            SafeDie 1
        }
    }
}
```

---

### `AbsorbSoul2`
**Description:** Down any ally and steal their mana. It doesn't get injured.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
AbsorbSoul2 {
    variant_of AbsorbSoul

    meta {
        desc "ABILITY_ABSORBSOUL2_DESC"
    }

    target {
        max_range 20
    }

    damage_instance {
        damage 0

        effects {
            Leech 1
            ManaSteal -1
            SafeDie 1
        }
    }
}
```

---

### `Gravecrawl`
**Name:** Gravecrawl  
**Description:** Dig to any tile and unearth a body.  
**Source:** `necromancer_abilities.gon`  

```
Gravecrawl {
    template teleport
    
    meta {
        name "ABILITY_GRAVECRAWL_NAME"
        desc "ABILITY_GRAVECRAWL_DESC"
        animate_name true
        class Necromancer
    }

    graphics {
        animation_out digDown
        animation_in digUp
    }

    cost {
        infcantrip true
        mana 8
    }

    target {
        max_range 20
    }

    self_damage {
        damage 0

        effects {
            BounceObject chapter_corpse_medium
        }
    }
}
```

---

### `Gravecrawl2`
**Name:** Gravecrawl  
**Description:** Dig to any tile and unearth 1-3 bodies.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
Gravecrawl2 {
    template teleport
    
    meta {
        name "ABILITY_GRAVECRAWL_NAME"
        desc "ABILITY_GRAVECRAWL2_DESC"
        animate_name true
        class Necromancer
    }

    graphics {
        animation_out digDown
        animation_in digUp
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        max_range 20
    }

    self_damage {
        damage 0

        effects {
            BounceObject chapter_corpse_medium
            BounceObject {
                chance .5
                obj chapter_corpse_medium
            }
            BounceObject {
                chance .25
                obj chapter_corpse_medium
            }
        }
    }
}
```

---

### `DigUpTheDead`
**Name:** Dig Up the Dead  
**Description:** Dig to any tile and unearth 4 zombies.  
**Source:** `necromancer_abilities.gon`  

```
DigUpTheDead {
    template teleport
    
    meta {
        name "ABILITY_DIGUPTHEDEAD_NAME"
        desc "ABILITY_DIGUPTHEDEAD_DESC"
        animate_name true
        class Necromancer
        type_icon spawn
    }

    tags [summon]

    graphics {
        animation_out digDown
        animation_in digUp
    }

    cost {
        infcantrip true
        mana 16
    }

    target {
        max_range 20
    }

    self_damage {
        damage 0

        effects {
            BounceObject ZombieCatFamiliar
            BounceObject ZombieCatFamiliar
            BounceObject ZombieCatFamiliar
            BounceObject ZombieCatFamiliar
        }
    }
}
```

---

### `DigUpTheDead2`
**Description:** Dig to any tile and unearth 4 zombies.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `necromancer_abilities.gon`  

```
DigUpTheDead2 {
    variant_of DigUpTheDead

    meta {
        desc "ABILITY_DIGUPTHEDEAD2_DESC"
    }

    cost {
        mana 9
    }
}
```

---

### `SpiderEgg`
**Name:** Spider Egg  
**Description:** Inflict Infested 1 on a unit in range 3.  
**Source:** `necromancer_abilities.gon`  

```
SpiderEgg {
    template lobbed_attack
    
    meta {
        name "ABILITY_SPIDEREGG_NAME"
        desc "ABILITY_SPIDEREGG_DESC"
        class Necromancer
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        min_range 1
        max_range 3+bonus_range
    }

    damage_instance {
        damage 0

        effects {
            SpiderInfested 1
        }
    }
}
```

---

### `SpiderEgg2`
**Description:** Deal 1 damage and inflict Infested 1 on any unit.  
**Source:** `necromancer_abilities.gon`  

```
SpiderEgg2 {
    variant_of SpiderEgg

    meta {
        desc "ABILITY_SPIDEREGG2_DESC"
    }

    target {
        max_range 20
    }

    damage_instance {
        damage 1
    }
}
```

---

### `ClewOfLeeches`
**Name:** Clew of Leeches  
**Description:** Surround a unit with leeches.  
**Source:** `necromancer_abilities.gon`  

```
ClewOfLeeches {
    template lobbed_attack
    
    meta {
        name "ABILITY_CLEWOFLEECHES_NAME"
        desc "ABILITY_CLEWOFLEECHES_DESC"
        class Necromancer
    }

    graphics {
		projectile LeechProjectile
    }

    cost {
        infcantrip true
        mana 8
    }

    target {
        min_range 1
        max_range 5+bonus_range

        restrictions [must_have_animate_character]
    }

    damage_instance {
        damage 0

        effects {
            Imprison CharmedLeech
        }
    }
}
```

---

### `ClewOfLeeches2`
**Description:** Surround a unit with beefy leeches.  
**Source:** `necromancer_abilities.gon`  

```
ClewOfLeeches2 {
    variant_of ClewOfLeeches

    meta {
        desc "ABILITY_CLEWOFLEECHES2_DESC"
    }

    damage_instance {
        effects {
            Imprison BeefyCharmedLeech
        }
    }
}
```

---

## File: `psychic_abilities.gon`

### `Telekinesis`
**Name:** Telekinesis  
**Description:** Push a unit within your line of sight away from you 10 tiles.  
**Source:** `psychic_abilities.gon`  

```
Telekinesis {
    template spell

    meta {
        name "ABILITY_TELEKINESIS_NAME"
        desc "ABILITY_TELEKINESIS_DESC"
        class Psychic
        type_icon "magic"
    }

    graphics {
        particle MagicMissleBlast
        animation psyAttack1
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        max_aoe 0
        max_range 20
        knockback_mode character_to_target
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0
        knockback 10

        effects {
            //OverrideKnockbackDamage 3
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `Telekinesis2`
**Description:** Push a unit within your line of sight away from you 10 tiles with Chain Knockback.  
**Source:** `psychic_abilities.gon`  

```
Telekinesis2 {
    variant_of Telekinesis

    meta {
        desc "ABILITY_TELEKINESIS2_DESC"
    }

    target {
        max_aoe 0
        max_range 20
    }

    damage_instance {
        effects {
            OverrideChainKnockback 10
            //OverrideChainKnockbackDamage 3
        }
    }
}
```

---

### `Suggestion`
**Name:** Suggestion  
**Description:** Cause an enemy within your line of sight to attack another enemy if it can.  
**Source:** `psychic_abilities.gon`  

```
Suggestion { //TODO: fix the percieved bugginess when it doesnt do anything
    template spell
    
    meta {
        name "ABILITY_SUGGESTION_NAME"
        desc "ABILITY_SUGGESTION_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
        animation slowPawMagic
		particle ExclamationPointEnemy
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        min_range 0
        max_range 20
        max_aoe 0
        aoe_excludes_self true
        restrictions [aoe_must_exist must_have_line_of_sight]
        aoe_restrictions [enemies_only must_have_living_character]
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            CharmedForceAttack 1
        }
    }
}
```

---

### `Suggestion2`
**Description:** Cause enemies in a target area within your line of sight to each attack another enemy if they can.  
**Source:** `psychic_abilities.gon`  

```
Suggestion2 {
    variant_of Suggestion

    meta {
        desc "ABILITY_SUGGESTION2_DESC"
    }

    target {
        max_aoe 2
    }
}
```

---

### `MindControl`
**Name:** Mind Control  
**Description:** Charm an enemy within your line of sight for the rest of the battle.  
**Source:** `psychic_abilities.gon`  

```
MindControl {
    template spell
    
    meta {
        name "ABILITY_MINDCONTROL_NAME"
        desc "ABILITY_MINDCONTROL_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
        animation slowPawMagic
		particle ExclamationPointEnemy
    }
    
    cost {
        infcantrip true
        mana 15
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0
        aoe_excludes_self true

        restrictions [aoe_must_exist must_have_line_of_sight]
        aoe_restrictions [enemies_only]
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Conditional_Boss {
                Charmed 1
            }
            Conditional_NotBoss {
                PermanentCharm 1
            }
        }
    }
}
```

---

### `MindControl2`
**Description:** Charm an enemy within your line of sight for the rest of the battle. That unit immediately takes an extra turn.  
**Source:** `psychic_abilities.gon`  

```
MindControl2 {
    variant_of MindControl

    meta {
        desc "ABILITY_MINDCONTROL2_DESC"
    }

    effects {
        TakeExtraTurn 1
    }
}
```

---

### `MegaGrav`
**Name:** Mega Grav  
**Description:** Damage and throw each unit near you to random tiles.  
**Source:** `psychic_abilities.gon`  

```
MegaGrav {
    template spell
    
    meta {
        name "ABILITY_MEGAGRAV_NAME"
        desc "ABILITY_MEGAGRAV_DESC"
        class Psychic
        type_icon "magic"
    }

    graphics {
        animation psyAttack2
		particle none
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        target_mode none
        max_aoe 3
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 2

        effects {
            TwisterDisplaceWithDamage {
                min_dist 3
                max_dist 20
                damage inherit
            }
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `MegaGrav2`
**Description:** Damage and throw each unit in a target area to random tiles.  
**Source:** `psychic_abilities.gon`  

```
MegaGrav2 {
    variant_of MegaGrav

    meta {
        desc "ABILITY_MEGAGRAV2_DESC"
    }

    cost {
        mana 3
    }

    target {
        target_mode tile
        max_range 20
    }
}
```

---

### `PsyFlutter`
**Name:** Psyflutter  
**Description:** Teleport exactly three tiles away.  
**Source:** `psychic_abilities.gon`  

```
PsyFlutter {
    template teleport
    
    meta {
        name "ABILITY_PSYFLUTTER_NAME"
        desc "ABILITY_PSYFLUTTER_DESC"
        animate_name true
        class Psychic
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 3
        max_range 3
        range_mode normal
    }
}
```

---

### `PsyFlutter2`
**Description:** Teleport exactly three tiles away.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
PsyFlutter2 {
    variant_of PsyFlutter

    meta {
        desc "ABILITY_PSYFLUTTER2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `MagnetPull`
**Name:** Gravity Pull  
**Description:** Pull units toward a tile within range 5.  
**Source:** `psychic_abilities.gon`  

```
MagnetPull {
    template spell

    meta {
        name "ABILITY_MAGNETPULL_NAME"
        desc "ABILITY_MAGNETPULL_DESC"
        class Psychic
        type_icon "magic"
    }

    graphics {
        animation psyAttack3
		particle none
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_aoe 1
        max_aoe 1
        max_range 5

        knockback_mode tile_to_target
    }
    
    damage_instance {
        damage 0
        knockback 1
        
        elements [
            Gravity
        ]
    }
}
```

---

### `MagnetPull2`
**Description:** Pull units in a larger area toward a tile at infinite range.  
**Source:** `psychic_abilities.gon`  

```
MagnetPull2 {
    variant_of MagnetPull

    meta {
        desc "ABILITY_MAGNETPULL2_DESC"
    }

    target {
        max_range 20
        max_aoe 2
    }
}
```

---

### `MindBlast`
**Name:** Mindblast  
**Description:** Push away each unit near you. This inflicts Madness and has a small chance to inflict Stun.  
**Source:** `psychic_abilities.gon`  

```
MindBlast {
    template spell
    
    meta {
        name "ABILITY_MINDBLAST_NAME"
        desc "ABILITY_MINDBLAST_DESC"
        class Psychic
        type_icon "magic"
    }

    graphics {
        animation psyAttack2
		particle none
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        target_mode none
        min_aoe 1
        max_aoe 3
    }
    
    damage_instance {
        damage 0
        knockback 3

        effects {
            Stun [1 .1]
            Madness 1
        }

        elements [
            Explosion
            Gravity
        ]
    }
}
```

---

### `MindBlast2`
**Description:** Push away each unit near a target area. This inflicts Madness and has a small chance to inflict Stun.  
**Source:** `psychic_abilities.gon`  

```
MindBlast2 {
    variant_of MindBlast

    meta {
        desc "ABILITY_MINDBLAST2_DESC"
    }

    target {
        target_mode tile
        max_range 20
        knockback_mode target_to_tile
    }
}
```

---

### `BlinkDodge`
**Source:** `psychic_abilities.gon`  

```
BlinkDodge { //used for a passive, does not need an upgrade
    template teleport

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    target {
        max_range 20
    }
}
```

---

### `PsychicChoke`
**Name:** Psychic Choke  
**Description:** Deal damage to and inflict Bruise on a unit within your line of sight.  
**Source:** `psychic_abilities.gon`  

```
PsychicChoke {
    template spell

    meta {
        name "ABILITY_PSYCHICCHOKE_NAME"
        desc "ABILITY_PSYCHICCHOKE_DESC"
        class Psychic
    }

    graphics {
        affected_particle fx_GravitySlam
        fx_is_placeholder_animation true
        animation slowPawMagic
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_aoe 0
        max_range 20
        knockback_mode zero
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 2

        effects {
            Bruise 1
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `PsychicChoke2`
**Description:** Deal damage to and inflict Bruise on a unit within your line of sight. This damage counts as physical damage and scales with [img:str].  
**Source:** `psychic_abilities.gon`  

```
PsychicChoke2 {
    variant_of PsychicChoke

    meta {
        desc "ABILITY_PSYCHICCHOKE2_DESC"
    }

    cost {
        mana 4
    }

    damage_instance {
        damage 2+bonus_melee_ability_damage
        type physical_spell
    }
}
```

---

### `SkyShatter`
**Name:** Shatter the Sky  
**Description:** Create floating glass shards on a tile within your line of sight.  
**Source:** `psychic_abilities.gon`  

```
SkyShatter {
    template spell

    meta {
        name "ABILITY_SKYSHATTER_NAME"
        desc "ABILITY_SKYSHATTER_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
		animation psyAttack1
		particle none

    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        max_aoe 1
        max_range 20
        max_aoe 0
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0

        effects {
            ChangeTile FloatingGlassTile
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `SkyShatter2`
**Description:** Create floating glass shards in an area within your line of sight.  
**Source:** `psychic_abilities.gon`  

```
SkyShatter2 {
    variant_of SkyShatter

    meta {
        desc "ABILITY_SKYSHATTER2_DESC"
    }

    target {
        max_aoe 1
    }
}
```

---

### `Supernova`
**Name:** Supernova  
**Description:** Deal damage to and inflict Blind on every unit within your line of sight.  
**Source:** `psychic_abilities.gon`  

```
Supernova {
    template spell
    
    meta {
        name "ABILITY_SUPERNOVA_NAME"
        desc "ABILITY_SUPERNOVA_DESC"
        class Psychic
    }

    graphics {
        animation psyMegaAttack
        particle MagicMissleBlast
        delay 3
    }
    
    cost {
        infcantrip true
        mana 10
    }
    
    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 12

        effects {
            Blind 3
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `Supernova2`
**Description:** Deal damage to and inflict Blind on every unit within your line of sight, excluding your allies.  
**Source:** `psychic_abilities.gon`  

```
Supernova2 {
    variant_of Supernova

    meta {
        desc "ABILITY_SUPERNOVA2_DESC"
    }

    target {
        aoe_restrictions [must_have_line_of_sight exclude_allies]
    }

    damage_instance {
        effects {
            Burn 3
        }
    }
}
```

---

### `ReadMind`
**Name:** Read Mind  
**Description:** Replace your spells with the spells of an ally cat until the end of the turn.  
**Source:** `psychic_abilities.gon`  

```
ReadMind { //CUT
    template spell
    
    meta {
        name "ABILITY_READMIND_NAME"
        desc "ABILITY_READMIND_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
        animation slowPawMagic
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0
        aoe_excludes_self true

        restrictions [aoe_must_exist]
        aoe_restrictions [must_have_player_cat]
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            CopySpells 1
        }
    }
}
```

---

### `ReadMind2`
**Description:** Replace your spells with upgraded versions of the spells of an ally cat until the end of the turn.  
**Source:** `psychic_abilities.gon`  

```
ReadMind2 {
    variant_of ReadMind

    meta {
        desc "ABILITY_READMIND2_DESC"
    }

    damage_instance {
        effects {
            CopySpells {
                stacks 1
                upgraded true
            }
        }
    }
}
```

---

### `AlterDNA`
**Name:** Alter DNA  
**Description:** Spend all your mana. Give a unit within your line of sight a random stat up for every 3 mana spent (rounded up). Give enemies random stat downs instead.  
**Source:** `psychic_abilities.gon`  

```
AlterDNA {
    template spell
    
    meta {
        name "ABILITY_ALTERDNA_NAME"
        desc "ABILITY_ALTERDNA_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
        animation slowPawMagic
		particle SparklingClean
    }
    
    cost {
        infcantrip true
        mana X
        X_cant_be_zero true
        disallow_cost_modification true
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0
        X_is current_mana
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Conditional_Ally {
                RandomStatUp "ceil(X/3)"
            } Else {
                RandomStatDown "ceil(X/3)"
            }
        }
    }
}
```

---

### `AlterDNA2`
**Description:** Spend all your mana. Give a unit within your line of sight a random stat up for every 2 mana spent (rounded up). Give enemies random stat downs instead.  
**Source:** `psychic_abilities.gon`  

```
AlterDNA2 {
    variant_of AlterDNA

    meta {
        desc "ABILITY_ALTERDNA2_DESC"
    }

    target {
        min_range 0
    }

    damage_instance {
        effects {
            Conditional_Ally {
                RandomStatUp "ceil(X/2)"
            } Else {
                RandomStatDown "ceil(X/2)"
            }
        }
    }
}
```

---

### `Flicker`
**Name:** Flicker  
**Description:** Teleport two tiles away. Displace any units you teleport into.  
**Source:** `psychic_abilities.gon`  

```
Flicker { //todo: blind when hit
    template teleport
    
    meta {
        name "ABILITY_FLICKER_NAME"
        desc "ABILITY_FLICKER_DESC"
        animate_name true
        class Psychic
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 2
        max_range 2
        range_mode normal

        restrictions [aoe_must_be_displaceable]
    }

    damage_instance {
        damage 0
        makes_contact true

        effects {
            IgnoreSelf 1
            Displace 1
        }
    }
}
```

---

### `Flicker2`
**Description:** Teleport two tiles away. Displace any units you teleport into and inflict them with Confusion 2 and Blind 2.  
**Source:** `psychic_abilities.gon`  

```
Flicker2 {
    variant_of Flicker

    meta {
        desc "ABILITY_FLICKER2_DESC"
    }


    damage_instance {
        damage 0
        makes_contact true

        effects {
            Confusion 2
            Blind 2
        }
    }
}
```

---

### `MindMeld`
**Name:** Mind Meld  
**Description:** Give another unit an extra turn after this one.
This spell can't be cast during extra turns.  
**Source:** `psychic_abilities.gon`  

```
MindMeld {
    template spell
    
    meta {
        name "ABILITY_MINDMELD_NAME"
        desc "ABILITY_MINDMELD_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
		animation pointout
		particle clockanim
    }
    
    cost {
        infcantrip true
        mana 10
        main_turn_only true
    }
    
    target {
        min_range 1
        max_range 3
        max_aoe 0
        aoe_excludes_self true
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

### `MindMeld2`
**Description:** Give another unit +10 mana and an extra turn after this one.
This spell can't be cast during extra turns.  
**Source:** `psychic_abilities.gon`  

```
MindMeld2 {
    variant_of MindMeld

    meta {
        desc "ABILITY_MINDMELD2_DESC"
    }

    damage_instance {
        effects {
            ManaGain 10
        }
    }
}
```

---

### `Vaccuum`
**Name:** Vacuum  
**Description:** Teleport all enemies within an area as close to the center of that area as possible.  
**Source:** `psychic_abilities.gon`  

```
Vaccuum {
    template spell
    
    meta {
        name "ABILITY_VACUUM_NAME"
        desc "ABILITY_VACUUM_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
        delay 1
        animation psyAttack1
		particle none
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        target_mode tile
        max_range 20
        max_aoe 4
        shuffle_tile_order true
    }
    
    damage_instance {
        damage 0

        effects {
            Conditional_Enemy {
                DisplaceToAbilityTarget 1
            }
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `Vaccuum2`
**Description:** Teleport all enemies within a large area as close to the center of that area as possible and inflict Confusion on those units.  
**Source:** `psychic_abilities.gon`  

```
Vaccuum2 {
    variant_of Vaccuum

    meta {
        desc "ABILITY_VACUUM2_DESC"
    }

    target {
        max_aoe 6
    }

    damage_instance {
        damage 0

        effects {
            Conditional_Enemy {
                DisplaceToAbilityTarget 1
                Confusion 1
            }
        }
    }
}
```

---

### `GrowHead`
**Name:** Grow Head  
**Description:** Gain +1 [img:int] and -1 [img:cha].  
**Source:** `psychic_abilities.gon`  

```
GrowHead { //bonus ability for FullPower passive
    template self_buff

    meta {
        name "ABILITY_GROWHEAD_NAME"
        desc "ABILITY_GROWHEAD_DESC"
        class Psychic
    }

    graphics {

    }
    
    cost {
        mana 3
        infcantrip true
    }


    damage_instance {
        effects {
            IntelligenceUp 1
            CharismaUp -1
        }
    }
}
```

---

### `Ping`
**Name:** Ping  
**Description:** Deal 1 damage to any unit within your line of sight.
RELOAD: Spend mana  
**Source:** `psychic_abilities.gon`  

```
Ping {
    template spell

    meta {
        name "ABILITY_PING_NAME"
        desc "ABILITY_PING_DESC"
        class Psychic
    }

    graphics {
        particle fx_magicSplash
        animation psyAttack3
    }
    
    cost {
        requires_reload true
        mana 0
    }
    
    target {
        max_aoe 0
        max_range 20
        restrictions must_have_line_of_sight
    }

    bonus_passives {
        ReloadOnSpendMana 1
    }
    
    damage_instance {
        damage 1
    }
}
```

---

### `Ping2`
**Description:** Deal 1 damage to any unit within your line of sight.
RELOAD: Spend mana
Bonus Passive: +2 [img:int].  
**Source:** `psychic_abilities.gon`  

```
Ping2 {
    variant_of Ping

    meta {
        desc "ABILITY_PING2_DESC"
    }

    bonus_passives {
        IntelligenceUp 2
    }
}
```

---

### `FlashForward`
**Name:** Flash Forward  
**Description:** Teleport to any tile. At the end of your turn, teleport back to your original tile and deal 10 damage to any unit you teleport into.  
**Source:** `psychic_abilities.gon`  

```
FlashForward {
    template teleport
    
    meta {
        name "ABILITY_FLASHFORWARD_NAME"
        desc "ABILITY_FLASHFORWARD_DESC"
        animate_name true
        class Psychic
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        min_range 1
        max_range 20
        range_mode normal
    }

    self_damage {
        damage 0
        effects {
            TeleportBackAtTurnEnd FlashBack
        }
    }
}
```

---

### `FlashForward2`
**Description:** Teleport to any tile. At the end of your turn, teleport back to your original tile and deal 10 damage to any unit you teleport into.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
FlashForward2 {
    variant_of FlashForward

    meta {
        desc "ABILITY_FLASHFORWARD2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `FlashBack`
**Name:** Flashback  
**Description:** Teleport back.  
**Source:** `psychic_abilities.gon`  

```
FlashBack { //utility ability for FlashForward
    template teleport
    
    meta {
        name "ABILITY_FLASHBACK_NAME"
        desc "ABILITY_FLASHBACK_DESC"
        animate_name true
        class Psychic
    }

    cost {
        infcantrip true
        mana 10
    }

    target {
        min_range 1
        max_range 20
        range_mode normal

        restrictions [aoe_must_be_force_displaceable]
    }

    damage_instance {
        damage 10
        makes_contact true

        effects {
            IgnoreSelf 1
            Displace 1
        }
    }
}
```

---

### `Order`
**Name:** Order  
**Description:** Force a unit within your line of sight to move and attack one of its enemies.  
**Source:** `psychic_abilities.gon`  

```
Order {
    template spell
    
    meta {
        name "ABILITY_ORDER_NAME"
        desc "ABILITY_ORDER_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
        animation pointout
		particle ExclamationPoint
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0
        aoe_excludes_self true
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            ForceMoveAndAttack 1
        }
    }
}
```

---

### `Order2`
**Description:** Give a unit within your line of sight All Stats Up and force it to move and attack one of its enemies.  
**Source:** `psychic_abilities.gon`  

```
Order2 {
    variant_of Order

    meta {
        desc "ABILITY_ORDER2_DESC"
    }

    damage_instance {
        effects {
            AllStatsUp 1
        }
    }
}
```

---

### `TemporalShards`
**Name:** Temporal Shards  
**Description:** Give a unit within your line of sight +3 temporary Bleed Thorns until the end of its turn.  
**Source:** `psychic_abilities.gon`  

```
TemporalShards {
    template spell
    
    meta {
        name "ABILITY_TEMPORALSHARDS_NAME"
        desc "ABILITY_TEMPORALSHARDS_DESC"
        class Psychic
        type_icon "buff"
    }
	
    graphics {
        animation pointout
		particle Glasspop
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        min_range 0
        max_range 20
        max_aoe 0
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Temporary {
                status BleedThorns
                stacks 3
                turns 1
            }
        }
    }
}
```

---

### `TemporalShards2`
**Name:** Temporal Shards  
**Description:** Give a unit within your line of sight +3 temporary Bleed Thorns until the end of its turn. If its was an ally, the bleed thorns last for the rest of the battle.  
**Source:** `psychic_abilities.gon`  

```
TemporalShards2 {
    template spell

    meta {
        name "ABILITY_TEMPORALSHARDS_NAME"
        desc "ABILITY_TEMPORALSHARDS2_DESC"
        class Psychic
        type_icon "buff"
    }
	
    graphics {
        animation pointout
		particle Glasspop
    }

    cost {
        infcantrip true
        mana 7
    }
    
    target {
        min_range 0
        max_range 20
        max_aoe 0
        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Conditional_Ally {
                BleedThorns 3
            }
            Conditional_NotAlly {
                Temporary {
                    status BleedThorns
                    stacks 3
                    turns 1
                }
            }
        }
    }
}
```

---

### `RealityScramble`
**Name:** Reality Scramble  
**Description:** Randomize the positions of all units. Enemies get Confused.  
**Source:** `psychic_abilities.gon`  

```
RealityScramble {
    template spell

    meta {
        name "ABILITY_REALITYSCRAMBLE_NAME"
        desc "ABILITY_REALITYSCRAMBLE_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
        particle none
        animation psyAttack1
    }
    
    cost {
        mana 6
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
    }

    self_damage {
        effects {
            ScrambleEverything 0
        }
    }

    damage_instance {
        damage 0
        type status_spell
        cant_miss true
    }
}
```

---

### `RealityScramble2`
**Description:** Randomize the positions of all units. Enemies get Confused. Non-boss enemies have a 10% chance to be erased from existence.  
**Source:** `psychic_abilities.gon`  

```
RealityScramble2 {
    variant_of RealityScramble

    meta {
        desc "ABILITY_REALITYSCRAMBLE2_DESC"
    }

    self_damage {
        effects {
            ScrambleEverything 10%
        }
    }
}
```

---

### `Glare`
**Name:** Glare  
**Description:** Inflict Madness on a unit in your line of sight.  
**Source:** `psychic_abilities.gon`  

```
Glare {
    template spell
    
    meta {
        name "ABILITY_GLARE_NAME"
        desc "ABILITY_GLARE_DESC"
        class Psychic
        type_icon "buff"
    }

    graphics {
        animation glare
		particle ExclamationPointEnemy
    }

    cost {
        infcantrip true
        mana 7
    }
    
    target {
        min_range 0
        max_range 20
        max_aoe 0

        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Madness 1
        }
    }
}
```

---

### `Glare2`
**Description:** Inflict Madness and Confusion on a unit in your line of sight.  
**Source:** `psychic_abilities.gon`  

```
Glare2 {
    variant_of Glare

    meta {
        desc "ABILITY_GLARE2_DESC"
    }

    damage_instance {
        effects {
            Confusion 1
        }
    }
}
```

---

### `BlindingFlash`
**Name:** Blinding Flash  
**Description:** Inflict Blind 2 on each unit near you in your line of sight.  
**Source:** `psychic_abilities.gon`  

```
BlindingFlash {
    template spell
    
    meta {
        name "ABILITY_BLINDINGFLASH_NAME"
        desc "ABILITY_BLINDINGFLASH_DESC"
        class Psychic
    }

    graphics {
        particle MagicMissleBlast
		animation flex
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_aoe 3
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0

        effects {
            Blind 2
        }
    }
}
```

---

### `BlindingFlash2`
**Description:** Inflict Blind 2 on each enemy within five tiles of you in your line of sight.  
**Source:** `psychic_abilities.gon`  

```
BlindingFlash2 {
    variant_of BlindingFlash

    meta {
        desc "ABILITY_BLINDINGFLASH2_DESC"
    }

    target {
        aoe_restrictions [must_have_line_of_sight exclude_allies]
        max_aoe 5
    }
}
```

---

### `Snatch`
**Name:** Snatch  
**Description:** Collect any pickup within your line of sight.  
**Source:** `psychic_abilities.gon`  

```
Snatch {
    template spell

    meta {
        name "ABILITY_SNATCH_NAME"
        desc "ABILITY_SNATCH_DESC"
        class Psychic
        type_icon "magic"
    }

    graphics {
        animation psyAttack1
		particle none
    }
    
    cost {
        infcantrip true
        mana 1
    }
    
    target {
        max_aoe 0
        max_range 20
        restrictions [must_have_tag must_have_line_of_sight]
        target_requires_tag pickup
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

### `Snatch2`
**Description:** Collect any pickup within your line of sight.
Gain +1 [img:lck].  
**Source:** `psychic_abilities.gon`  

```
Snatch2 {
    variant_of Snatch

    meta {
        desc "ABILITY_SNATCH2_DESC"
    }

    self_damage {
        effects {
            LuckUp 1
        }
    }
}
```

---

### `FutureSight`
**Name:** Future Sight  
**Description:** A unit within your line of sight backflips out of the way the next time they're targeted by an enemy.  
**Source:** `psychic_abilities.gon`  

```
FutureSight {
    template spell
    
    meta {
        name "ABILITY_FUTURESIGHT_NAME"
        desc "ABILITY_FUTURESIGHT_DESC"
        class Psychic
        type_icon "buff"
    }
	
    graphics {
        animation pointout
		particle ExclamationPoint
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0

        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            BackflipWhenTargeted 1
        }
    }
}
```

---

### `FutureSight2`
**Description:** A unit within your line of sight backflips out of the way the next time they're targeted by an enemy.
 \[s:.7\](This spell costs less.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
FutureSight2 {
    variant_of FutureSight

    meta {
        desc "ABILITY_FUTURESIGHT2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `MassManaLeech`
**Name:** Mass Mana Leech  
**Description:** Inflict Mana Leech 2 and Weakness 2 on all units within 3 tiles of you.  
**Source:** `psychic_abilities.gon`  

```
MassManaLeech {
    template spell
	
    graphics {
	    particle none
	    animation floatingmagic
    }
    
    meta {
        name "ABILITY_MASSMANALEECH_NAME"
        desc "ABILITY_MASSMANALEECH_DESC"
        class Psychic
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_aoe 3
        target_mode none
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            ManaLeeches 2
            Weakness 2
        }
    }
}
```

---

### `MassManaLeech2`
**Description:** Inflict Mana Leech 2 and Weakness 2 on all units within 5 tiles of you.  
**Source:** `psychic_abilities.gon`  

```
MassManaLeech2 {
    variant_of MassManaLeech

    meta {
        desc "ABILITY_MASSMANALEECH2_DESC"
    }

    target {
        max_aoe 5
    }
}
```

---

### `BecomeEntropy`
**Name:** Become Entropy  
**Description:** Vaporize everything on a tile within your line of sight. Against a boss, this deals 10 damage and inflicts Stun instead.  
**Source:** `psychic_abilities.gon`  

```
BecomeEntropy {
    template spell

    meta {
        name "ABILITY_BECOMEENTROPY_NAME"
        desc "ABILITY_BECOMEENTROPY_DESC"
        class Psychic
    }

    graphics {
        particle BigMagicMissileBlast
    }
    
    cost {
        infcantrip true
        mana 14
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0

        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0

        effects {
            Conditional_NotBoss {
                CanApplyToInanimate {
                    PreventDeathTransforms 1
                    Vaporize 1
                }
            }
            Conditional_Boss {
                Stun 1
                OverrideDamage 10
            }
            ChangeTile BlankTile
            DeleteTraps 1
        }
    }
}
```

---

### `BecomeEntropy2`
**Description:** Vaporize everything on a tile within your line of sight. Against a boss, this deals 25 damage and inflicts Stun instead.  
**Source:** `psychic_abilities.gon`  

```
BecomeEntropy2 {
    variant_of BecomeEntropy

    meta {
        desc "ABILITY_BECOMEENTROPY2_DESC"
    }

    damage_instance {
        damage 0

        effects {
            Conditional_Boss {
                Stun 1
                OverrideDamage 25
            }
        }
    }
}
```

---

### `FastForward`
**Name:** Fast Forward  
**Description:** Every ally that hasn't taken their turn yet takes their turn right after yours. You go first next round.  
**Source:** `psychic_abilities.gon`  

```
FastForward {
    template spell

    meta {
        name "ABILITY_FASTFORWARD_NAME"
        desc "ABILITY_FASTFORWARD_DESC"
        class Psychic
    }

    graphics {
        affected_particle fx_haste
    }
    
    cost {
        mana 4
        infcantrip true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_excludes_self false
        aoe_restrictions [allies_only character_has_turns_left]
    }

    damage_instance {
        type status_spell
        effects {
            TempInitiativeChange 9999
        }
    }
}
```

---

### `FastForward2`
**Description:** Every ally that hasn't taken their turn yet takes their turn right after yours. Those units get +4 temporary [img:spd]. You go first next round.  
**Source:** `psychic_abilities.gon`  

```
FastForward2 {
    variant_of FastForward

    meta {
        desc "ABILITY_FASTFORWARD2_DESC"
    }

    damage_instance {
        effects {
            TempSpeedUp 4
        }
    }
}
```

---

### `AncestralRecall`
**Name:** Ancestral Recall  
**Description:** Upgrade one of your spells at random for the rest of the battle.  
**Source:** `psychic_abilities.gon`  

```
AncestralRecall {
    template self_buff

    meta {
        name "ABILITY_ANCESTRALRECALL_NAME"
        desc "ABILITY_ANCESTRALRECALL_DESC"
        class Psychic
    }

    graphics {
		animation thinking
    }
    
    cost {
        mana 8
        infcantrip true
    }

    damage_instance {
        effects {
            UpgradeRandomAbility 1
            Conditional_Enemy {
                AllStatsUp 1
            }
        }
    }
}
```

---

### `AncestralRecall2`
**Description:** Target yourself or a unit within your line of sight and upgrade one of their spells at random for the rest of the battle.  
**Source:** `psychic_abilities.gon`  

```
AncestralRecall2 {
    variant_of AncestralRecall

    meta {
        desc "ABILITY_ANCESTRALRECALL2_DESC"
    }
    
    target {
        min_range 0
        max_range 20
        max_aoe 0
        restrictions must_have_line_of_sight
        target_mode tile
    }
}
```

---

### `CumulativeBlast`
**Name:** Cumulative Blast  
**Description:** Deal damage to a unit in your line of sight, then increase this spell's damage by 1 for the rest of the battle.  
**Source:** `psychic_abilities.gon`  

```
CumulativeBlast {
    template spell

    meta {
        name "ABILITY_CUMULATIVEBLAST_NAME"
        desc "ABILITY_CUMULATIVEBLAST_DESC"
        class Psychic
    }

    graphics {
        particle fx_magicSplash
        animation psyAttack3
    }
    
    cost {
        mana 6
        infcantrip true
    }
    
    target {
        max_aoe 0
        max_range 20
        restrictions must_have_line_of_sight
        X_is custom
    }
    
    self_damage {
        effects {
            IncreaseCumulativeBlastDamage 1
        }
    }

    damage_instance {
        damage 1+X
    }
}
```

---

### `CumulativeBlast2`
**Description:** Deal damage to a unit in your line of sight, then increase this spell's damage by 1 for the rest of the battle.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
CumulativeBlast2 {
    variant_of CumulativeBlast

    meta {
        desc "ABILITY_CUMULATIVEBLAST2_DESC"
    }

    cost {
        mana 5
    }
}
```

---

### `Hallucinate`
**Name:** Hallucinate  
**Description:** Spawn a friendly illusion of a random unit that fades away after one turn.  
**Source:** `psychic_abilities.gon`  

```
Hallucinate {
    template spawn

    meta {
        name "ABILITY_HALLUCINATE_NAME"
        desc "ABILITY_HALLUCINATE_DESC"
        class Psychic
    }

    tags [summon]
    
    graphics {
        animation thinking
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0
        restrictions must_have_line_of_sight
        aoe_restrictions [exclude_blocking]
    }

    spawn {
        object RANDOM_1X1_ENEMY
        faction self

        additional_passives {
            SafeDoomed 1
            InjuryImmunity 1
            FadeInsteadOfDie 1
            IllusionTint 1
        }
    }
}
```

---

### `Hallucinate2`
**Description:** Spawn a friendly illusion of a random unit that fades away after one turn. The illusion gets +4 [img:spd] and +2 Damage.  
**Source:** `psychic_abilities.gon`  

```
Hallucinate2 {
    variant_of Hallucinate

    meta {
        desc "ABILITY_HALLUCINATE2_DESC"
    }

    target {
        max_range 20
    }

    spawn {
        additional_passives {
            SpeedUp 4
            DamageUp 2
        }
    }
}
```

---

### `MassHysteria`
**Name:** Mass Hysteria  
**Description:** Every enemy in your line of sight takes an extra turn. They are charmed on that turn.  
**Source:** `psychic_abilities.gon`  

```
MassHysteria {
    template spell
    
    meta {
        name "ABILITY_MASSHYSTERIA_NAME"
        desc "ABILITY_MASSHYSTERIA_DESC"
        class Psychic
    }

    graphics {
		affected_particle ExclamationPointEnemy
    }
    
    cost {
        infcantrip true
        mana 10
    }
    
    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        aoe_restrictions [must_have_line_of_sight exclude_allies]
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Conditional_Enemy {
                Charmed 1
                TakeExtraTurn 1
            }
        }
    }
}
```

---

### `MassHysteria2`
**Description:** Every enemy in your line of sight takes an extra turn. They are charmed on that turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
MassHysteria2 {
    variant_of MassHysteria

    meta {
        desc "ABILITY_MASSHYSTERIA2_DESC"
    }

    cost {
        mana 7
    }
}
```

---

### `ExtraTurnQuestion`
**Name:** Extra Turn?  
**Description:** Take an extra turn. You're stunned and don't regenerate mana on that turn.
\[s:.7\](This spell can't be cast on extra turns.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
ExtraTurnQuestion {
    template self_buff
    
    meta {
        name "ABILITY_EXTRATURNQ_NAME"
        desc "ABILITY_EXTRATURNQ_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
		animation doublevision
    }
    
    cost {
        infcantrip true
        mana 4
        main_turn_only true
    }
    
    damage_instance {
        effects {
            TakeBonusTurnWithStatus {
                Stun 1
                TempNoManaRegen 1
            }
        }
    }
}
```

---

### `ExtraTurnQuestion2`
**Description:** Take an extra turn. You have a 75% chance to be stunned and don't regenerate mana on that turn.
\[s:.7\](This spell can't be cast on extra turns.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
ExtraTurnQuestion2 {
    variant_of ExtraTurnQuestion

    meta {
        desc "ABILITY_EXTRATURNQ2_DESC"
    }

    damage_instance {
        effects {
            TakeBonusTurnWithStatus {
                Stun [1 .75]
                TempNoManaRegen 1
            }
        }
    }
}
```

---

### `MindCrack`
**Name:** Mindcrack  
**Description:** Inflict Magic Weakness 2 on all units in your line of sight.  
**Source:** `psychic_abilities.gon`  

```
MindCrack {
    template spell
    
    meta {
        name "ABILITY_MINDCRACK_NAME"
        desc "ABILITY_MINDCRACK_DESC"
        class Psychic
    }

    graphics {
        animation psyMegaAttack
        particle none
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_line_of_sight
    }
    
    damage_instance {
        type status_spell

        effects {
            MagicWeakness 2
        }
    }
}
```

---

### `MindCrack2`
**Description:** Inflict Magic Weakness 2 and Confusion 1 on all non-allied units in your line of sight.  
**Source:** `psychic_abilities.gon`  

```
MindCrack2 {
    variant_of MindCrack

    meta {
        desc "ABILITY_MINDCRACK2_DESC"
    }

    target {
        aoe_restrictions [must_have_line_of_sight exclude_allies]
    }

    damage_instance {
        effects {
            MagicWeakness 2
            Confusion 1
        }
    }
}
```

---

### `Reset`
**Name:** Reset  
**Description:** Revive all bodies, fully heal all units, and clear all status effects.
\[s:.7\](This spell can be cast only once per battle.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
Reset {
    template spell
    
    meta {
        name "ABILITY_RESET_NAME"
        desc "ABILITY_RESET_DESC"
        class Psychic
    }

    graphics {
        animation psyMegaAttack
        particle none
    }
    
    cost {
        infcantrip true
        mana 16
        once_per_fight true
    }
    
    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self false
        aoe_restrictions none
    }
    
    damage_instance {
        type status_spell

        effects {
            PurgeAll 1
            Revive 100%
            PurgeAll 1
            FullHeal 1
        }
    }
}
```

---

### `Reset2`
**Description:** Revive all bodies, fully heal all units, and clear all status effects.
Castable while you're downed. It costs 0 mana if you're downed.
\[s:.7\](This spell can be cast only once per battle.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
Reset2 {
    variant_of Reset
    
    meta {
        desc "ABILITY_RESET2_DESC"
    }

    graphics {
        animation psyMegaAttack
        particle none
    }
    
    cost {
        infcantrip true
        mana 16-X*16
        once_per_fight true
        can_cast_while_dead true
    }
    
    target {
        X_is is_dead
    }
}
```

---

### `Mimic`
**Name:** Mimic  
**Description:** Target an allied cat within your line of sight. Cast one of their spells at random for free (or use their basic attack if theres no good spells).  
**Source:** `psychic_abilities.gon`  

```
Mimic {
    template targeted_status
    
    meta {
        name "ABILITY_MIMIC_NAME"
        desc "ABILITY_MIMIC_DESC"
        class Psychic
        type_icon "unknown"
    }
	
    graphics {
        animation thinking
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0

        restrictions [must_have_line_of_sight must_have_player_cat]
    }
    
    damage_instance {
        effects {
            MimicMetronome 1
        }
    }
}
```

---

### `Mimic2`
**Description:** Target an allied cat within your line of sight. Cast one of their spells at random for free (or use their basic attack if theres no good spells).
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
Mimic2 {
    variant_of Mimic

    meta {
        desc "ABILITY_MIMIC2_DESC"
    }

    cost {
        infcantrip true
        mana 5
    }
}
```

---

### `ChaosSwap`
**Name:** Chaos Swap  
**Description:** Swap positions with a random unit.  
**Source:** `psychic_abilities.gon`  

```
ChaosSwap {
    template swap
    
    meta {
        name "ABILITY_CHAOSSWAP_NAME"
        desc "ABILITY_CHAOSSWAP_DESC"
        animate_name false
        class Psychic
    }

    graphics {
    }

    cost {
        mana 2
        infcantrip true
    }

    target {
        target_mode random_tile
        max_range 20
    }
}
```

---

### `ChaosSwap2`
**Description:** Swap positions with a random unit. If that unit was an enemy, you inflict Confusion on it.  
**Source:** `psychic_abilities.gon`  

```
ChaosSwap2 {
    variant_of ChaosSwap

    meta {
        desc "ABILITY_CHAOSSWAP2_DESC"
    }

    damage_instance {
        effects {
            Conditional_Enemy {
                Confusion 1
            }
        }
    }
}
```

---

### `Asteroid`
**Name:** Asteroid  
**Description:** Make an asteroid fall onto a tile within your line of sight. The asteroid deals damage and leaves a rock.  
**Source:** `psychic_abilities.gon`  

```
Asteroid {
    template spell
    
    meta {
        name "ABILITY_ASTEROID_NAME"
        desc "ABILITY_ASTEROID_DESC"
        class Psychic
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
        min_range 1
        max_range 20
        max_aoe 0

        restrictions must_have_line_of_sight
        knockback_mode zero
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

### `Asteroid2`
**Description:** Make an asteroid fall onto a tile within your line of sight. The asteroid deals damage, bruises and leaves a boulder.  
**Source:** `psychic_abilities.gon`  

```
Asteroid2 {
    variant_of Asteroid

    meta {
        desc "ABILITY_ASTEROID2_DESC"
    }

    damage_instance {
        damage 8

        effects {
            Bruise 1
            Displace 1
            BounceRock LavaBoulder
        }
    }
}
```

---

### `Stasis`
**Name:** Stasis  
**Description:** Inflict Freeze on a unit within your line of sight.  
**Source:** `psychic_abilities.gon`  

```
Stasis {
    template targeted_status
    
    meta {
        name "ABILITY_STASIS_NAME"
        desc "ABILITY_STASIS_DESC"
        class Psychic
    }
	
	graphics {
        particle IcePoof
		animation psyAttack1
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0

        restrictions must_have_line_of_sight
    }
    
    damage_instance {
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

### `Stasis2`
**Description:** Inflict Freeze 1, Blind 2, and Confusion 2 on a unit within your line of sight.  
**Source:** `psychic_abilities.gon`  

```
Stasis2 {
    variant_of Stasis
    
    meta {
        desc "ABILITY_STASIS2_DESC"
    }

    damage_instance {
        effects {
            Freeze 1
            Blind 2
            Confusion 2
        }
    }
}
```

---

### `Pass`
**Name:** Pass  
**Description:** Give a unit within your line of sight an extra turn immediately, then end your turn. 
Castable only if you haven't taken any actions this turn.
\[s:.7\](This can't be cast on extra turns.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
Pass {
    template targeted_status
    
    meta {
        name "ABILITY_PASS_NAME"
        desc "ABILITY_PASS_DESC"
        class Psychic
    }

    graphics {
		animation pointout
    }
    
    cost {
        infcantrip true
        mana 3
        must_be_first_action true
        main_turn_only true
    }

    target {
        min_range 1
        max_range 20
        max_aoe 0

        restrictions must_have_line_of_sight
    }
    
    self_damage {
        effects {
            EndTurn 1
        }
    }

    damage_instance {
        effects {
            TakeExtraTurn 1
        }
    }
}
```

---

### `Pass2`
**Description:** Give a unit within your line of sight an extra turn immediately, then end your turn.
Castable only if you haven't taken any actions this turn other than your movement action.
\[s:.7\](This can't be cast on extra turns.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
Pass2 {
    variant_of Pass

    meta {
        desc "ABILITY_PASS2_DESC"
    }

    cost {
        infcantrip true
        must_be_first_action false
        must_be_first_nonmove_action true
    }
}
```

---

### `ThinkDeep`
**Name:** Think Deep  
**Description:** Restore all of your mana and fall asleep.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
ThinkDeep {
    template self_buff

    meta {
        name "ABILITY_THINKDEEP_NAME"
        desc "ABILITY_THINKDEEP_DESC"
        class Psychic
    }

    graphics {

    }
    
    cost {
        mana 5
        cantrip true
    }


    damage_instance {
        effects {
            FillMana 1
            Sleep 1
        }
    }
}
```

---

### `ThinkDeep2`
**Description:** Restore all of your mana and fall asleep.
\[s:.7\](Castable once per turn. This spell costs 0 mana.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
ThinkDeep2 {
    variant_of ThinkDeep

    meta {
        desc "ABILITY_THINKDEEP2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `Puppet`
**Name:** Puppet  
**Description:** Force an enemy within your line of sight to attack in the direction it's facing.  
**Source:** `psychic_abilities.gon`  

```
Puppet {
    template targeted_status
    
    meta {
        name "ABILITY_PUPPET_NAME"
        desc "ABILITY_PUPPET_DESC"
        class Psychic
        type_icon "misc"
    }

    graphics {
		animation pointout
		particle ExclamationPointEnemy
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0
        aoe_excludes_self true
        restrictions [aoe_must_exist must_have_line_of_sight]
        aoe_restrictions [enemies_only]
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            CharmedFacingForceAttack 1
        }
    }
}
```

---

### `Puppet2`
**Description:** Force a unit within your line of sight to attack in the direction it's facing.  
**Source:** `psychic_abilities.gon`  

```
Puppet2 {
    variant_of Puppet

    meta {
        desc "ABILITY_PUPPET2_DESC"
    }

    target {
        restrictions must_have_line_of_sight
        aoe_restrictions none
    }
}
```

---

### `YouSeeNothing`
**Name:** Look Away  
**Description:** Every unit within your line of sight turns away from you.  
**Source:** `psychic_abilities.gon`  

```
YouSeeNothing {
    template spell
    
    meta {
        name "ABILITY_LOOKAWAY_NAME"
        desc "ABILITY_LOOKAWAY_DESC"
        class Psychic
    }

    graphics {
        particle none
		animation psyAttack1
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        aoe_restrictions must_have_line_of_sight
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

### `YouSeeNothing2`
**Description:** Every unit within your line of sight turns away from you and is inflicted with Blind 1.  
**Source:** `psychic_abilities.gon`  

```
YouSeeNothing2 {
    variant_of YouSeeNothing
    
    meta {
        desc "ABILITY_LOOKAWAY2_DESC"
    }
    
    damage_instance {
        effects {
            Blind 1
        }
    }
}
```

---

### `ForceBlast`
**Name:** Gravity Blast  
**Description:** Deal 10 Knockback to adjacent units. If you cast this from full mana, the units take 10 damage on collision.  
**Source:** `psychic_abilities.gon`  

```
ForceBlast {
    template spell
    
    meta {
        name "ABILITY_GRAVITYBLAST_NAME"
        desc "ABILITY_GRAVITYBLAST_DESC"
        class Psychic
        icon_shell_frame attack
        icon_damage_display_eq X*10
        icon_damage_type physical
    }

    graphics {
		animation flex
        particle none
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        target_mode none
        max_aoe 1
        aoe_excludes_self true
        X_is is_at_max_mana
    }
    
    damage_instance {
        damage 0
        knockback 10

        effects {
            Conditional_FormulaIsPositive {
                formula X*10
                OverrideKnockbackDamage X*10
            }
        }

        elements [
            Gravity
            Explosion
        ]
    }
}
```

---

### `ForceBlast2`
**Description:** Deal 10 Knockback to adjacent units. If you cast this from full mana, the units take 10 damage on collision and get stunned.  
**Source:** `psychic_abilities.gon`  

```
ForceBlast2 {
    variant_of ForceBlast

    meta {
        desc "ABILITY_GRAVITYBLAST2_DESC"
    }

    damage_instance {
        effects {
            Conditional_FormulaIsPositive {
                Stun 1
            }
        }
    }
}
```

---

### `IncreaseGravity`
**Name:** Increase Gravity  
**Description:** Inflict Slow 1 on a unit within your line of sight. If you cast this from full mana, instead inflict Immobilize 1 and deal 6 damage.  
**Source:** `psychic_abilities.gon`  

```
IncreaseGravity {
    template spell
    
    meta {
        name "ABILITY_INCREASEGRAVITY_NAME"
        desc "ABILITY_INCREASEGRAVITY_DESC"
        class Psychic
        icon_shell_frame attack
    }

    graphics {
		animation pointout
		particle fx_statdown
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        min_range 1
        max_range 20
        max_aoe 0
        aoe_excludes_self true
        restrictions must_have_line_of_sight
        X_is is_at_max_mana
    }
    
    damage_instance {
        raw_damage X*6

        effects {
            Conditional_FormulaIsPositive {
                formula X
                Immobile 1
            } Else {
                Slow 1
            }
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `IncreaseGravity2`
**Description:** Inflict Slow 1 on each unit in an area around a tile within your line of sight. If you cast this from full mana, instead inflict Immobilize 1 and deal 6 damage.  
**Source:** `psychic_abilities.gon`  

```
IncreaseGravity2 {
    variant_of IncreaseGravity

    meta {
        desc "ABILITY_INCREASEGRAVITY2_DESC"
    }

    target {
        max_aoe 2
    }
}
```

---

### `Manifest`
**Name:** Manifest  
**Description:** Teleport in a straight line into a unit within your line of sight. Deal damage and displace it.  
**Source:** `psychic_abilities.gon`  

```
Manifest {
    template teleport
    
    meta {
        name "ABILITY_MANIFEST_NAME"
        desc "ABILITY_MANIFEST_DESC"
        animate_name true
        class Psychic
        type_icon "magic"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 6
    }

    target {
        range_mode cross
        max_range 20
        restrictions [aoe_must_be_displaceable must_have_animate_character must_have_line_of_sight]
    }

    damage_instance {
        damage 5
        type spell
        makes_contact true

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `Manifest2`
**Description:** Teleport into a unit within your line of sight. Deal damage and displace it.  
**Source:** `psychic_abilities.gon`  

```
Manifest2 {
    variant_of Manifest

    meta {
        desc "ABILITY_MANIFEST2_DESC"
    }

    target {
        range_mode normal
    }
}
```

---

### `Flip`
**Name:** Flip  
**Description:** Turn a unit within your line of sight 180 degrees. Inflict Confusion 1 on that unit.  
**Source:** `psychic_abilities.gon`  

```
Flip {
    template spell
	
	graphics {
		animation thinking
		particle confusionStars
    }
    
    meta {
        name "ABILITY_FLIP_NAME"
        desc "ABILITY_FLIP_DESC"
        class Psychic
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        min_range 0
        max_range 20
        max_aoe 0

        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0
        type status_spell

        effects {
            Confusion 1
            TurnAround 1
        }
    }
}
```

---

### `Flip2`
**Description:** Turn a unit within your line of sight 180 degrees. Inflict Confusion 2 and Magic Weakness 1 on that unit.  
**Source:** `psychic_abilities.gon`  

```
Flip2 {
    variant_of Flip

    meta {
        desc "ABILITY_FLIP2_DESC"
    }

    damage_instance {
        effects {
            Confusion 2
            MagicWeakness 1
        }
    }
}
```

---

### `Withdraw`
**Name:** Withdraw  
**Description:** Pull any unit within your line of sight to a tile adjacent to you.  
**Source:** `psychic_abilities.gon`  

```
Withdraw {
    template targeted_status
    
    meta {
        name "ABILITY_WITHDRAW_NAME"
        desc "ABILITY_WITHDRAW_DESC"
        class Psychic
    }
	
	graphics {
		animation psyAttack1
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        min_range 0
        max_range 20
        max_aoe 0

        restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0

        effects {
            DisplaceTowardsSource 1
        }
    }
}
```

---

### `Withdraw2`
**Description:** Pull any unit within your line of sight to a tile adjacent to you.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
Withdraw2 {
    variant_of Withdraw

    meta {
        desc "ABILITY_WITHDRAW2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `ForceCone`
**Name:** Gravity Wave  
**Description:** Deal damage with Knockback 4 and Chain Knockback in a cone.  
**Source:** `psychic_abilities.gon`  

```
ForceCone {
    template spell

    meta {
        name "ABILITY_GRAVITYWAVE_NAME"
        desc "ABILITY_GRAVITYWAVE_DESC"
        class Psychic
    }

    graphics {
		animation psyAttack1
        particle BigMagicMissileBlast
        delay 0
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 3

        aoe_considers_character_size true
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 2
        knockback 4

        effects {
            OverrideChainKnockback 1
        }

        elements [
            Gravity
        ]
    }
}
```

---

### `ForceCone2`
**Description:** Deal damage with Knockback 4, Chain Knockback and inflict Bruise 1 in a cone.  
**Source:** `psychic_abilities.gon`  

```
ForceCone2 {
    variant_of ForceCone

    meta {
        desc "ABILITY_GRAVITYWAVE2_DESC"
    }

    target {
        max_aoe 4
    }

    damage_instance {
        effects {
            Bruise 1
        }
    }
}
```

---

### `Inversion`
**Name:** Inversion  
**Description:** Swap positions with a unit in your line of sight.  
**Source:** `psychic_abilities.gon`  

```
Inversion {
    template swap
    
    meta {
        name "ABILITY_INVERSION_NAME"
        desc "ABILITY_INVERSION_DESC"
        animate_name true
        class Psychic
    }

    graphics {
    }

    cost {
        mana 4
        infcantrip true
    }

    target {
        max_range 20
        restrictions [must_be_swappable must_have_line_of_sight]
    }
}
```

---

### `Inversion2`
**Description:** Swap positions with a unit in your line of sight.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `psychic_abilities.gon`  

```
Inversion2 {
    variant_of Inversion
    
    meta {
        desc "ABILITY_INVERSION2_DESC"
    }

    cost {
        mana 2
    }
}
```

---

### `Echo`
**Name:** Echo  
**Description:** Teleport to the last tile you targeted with an ability if it's empty.  
**Source:** `psychic_abilities.gon`  

```
Echo {
    template teleport
    
    meta {
        name "ABILITY_ECHO_NAME"
        desc "ABILITY_ECHO_DESC"
        animate_name true
        class Psychic
    }

    cost {
        infcantrip true
        mana 1
    }

    target {
        target_mode random_tile
        min_range 1
        max_range 20
        range_mode last_targeted_tile
    }
}
```

---

### `Echo2`
**Description:** Teleport to the last tile you targeted with an ability. Displace and damage any units on that tile.  
**Source:** `psychic_abilities.gon`  

```
Echo2 {
    variant_of Echo

    meta {
        desc "ABILITY_ECHO2_DESC"
    }

    target {
        restrictions [aoe_must_be_force_displaceable]
    }

    damage_instance {
        damage 5
        makes_contact true

        effects {
            IgnoreSelf 1
            Displace 1
        }
    }
}
```

---

### `Slipstream`
**Name:** Slipstream  
**Description:** Dash up to three tiles in a straight line or diagonally. Leave floating glass shards on tiles you pass through.  
**Source:** `psychic_abilities.gon`  

```
Slipstream {
    template move
    
    meta {
        name "ABILITY_SLIPSTEAM_NAME"
        desc "ABILITY_SLIPSTEAM_DESC"
        class Psychic
        animate_name true
    }
    
    graphics {
        speed 6
        ignore_slowtiles true
        //move_start_animation startroll
        //animation roll
        //move_end_animation endroll
    }

    cost {
        infcantrip true
        mana 5
    }

    temporary_effects {
        TileTrail FloatingGlassTile
    }

    target {
        range_mode 8cross
        max_range 3
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_diagonals true
    }
}
```

---

### `Slipstream2`
**Description:** Dash up to five tiles in a straight line or diagonally. Leave floating glass shards on tiles you pass through.  
**Source:** `psychic_abilities.gon`  

```
Slipstream2 {
    variant_of Slipstream

    meta {
        desc "ABILITY_SLIPSTEAM2_DESC"
    }

    target {
        max_range 5
    }
}
```

---

### `MindCrack_EldritchVisage`
**Source:** `psychic_abilities.gon`  

```
MindCrack_EldritchVisage { //util for eldritch visage passive, does not need an icon
    template spell

    graphics {
        animation psyMegaAttack
        particle none
    }

    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
        aoe_restrictions [must_have_line_of_sight exclude_allies]
    }
    
    damage_instance {
        type status_spell

        effects {
            MagicWeakness 1
        }
    }
}
```

---

### `MindCrack_EldritchVisage2`
**Source:** `psychic_abilities.gon`  

```
MindCrack_EldritchVisage2 { //util for eldritch visage passive, does not need an icon
    variant_of MindCrack_EldritchVisage

    target {
        aoe_restrictions [must_have_line_of_sight exclude_allies]
    }
    
    damage_instance {
        type status_spell

        effects {
            MagicWeakness 1
            Marked 1
        }
    }
}
```

---

## File: `tank_abilities.gon`

### `Taunt`
**Name:** Taunt  
**Description:** Enemies will attack you if possible  
**Source:** `tank_abilities.gon`  

```
Taunt { //CUT
    template self_buff
    
    meta {
        name "Taunt"
        desc "Enemies will attack you if possible"
        class Tank
        type_icon "misc"
    }

    graphics {
        animation tauntwiggle
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            Taunting 1
        }
    }
}
```

---

### `Taunt2`
**Description:** Enemies will attack you if possible (lower mana)  
**Source:** `tank_abilities.gon`  

```
Taunt2 {
    variant_of Taunt

    meta {
        desc "Enemies will attack you if possible (lower mana)"
    }

    cost {
        mana 1
    }
}
```

---

### `HeadButt`
**Name:** Headbutt  
**Description:** A melee attack that inflicts Stun.  
**Source:** `tank_abilities.gon`  

```
HeadButt {
    template melee_attack
    
    meta {
        name "ABILITY_HEADBUTT_NAME"
        desc "ABILITY_HEADBUTT_DESC"
        class Tank
        type_icon "defense"
    }

    graphics {
        animation headbutt
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    damage_instance {
        damage 1

        effects {
            Stun 1
        }
    }
}
```

---

### `HeadButt2`
**Description:** A melee attack that inflicts Stun.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
HeadButt2 {
    variant_of HeadButt

    meta {
        desc "ABILITY_HEADBUTT2_DESC"
    }

    cost {
        mana 6
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage

        effects {
            Stun 1
        }
    }
}
```

---

### `ThrowShield`
**Name:** Throw Scrap  
**Description:** Give +3 [img:shield] to a unit or spawn a scrap pickup on an empty tile.  
**Source:** `tank_abilities.gon`  

```
ThrowShield {
    template lobbed_attack
    
    meta {
        name "ABILITY_THROWSCRAP_NAME"
        desc "ABILITY_THROWSCRAP_DESC"
        class Tank
        type_icon "defense"
    }

    graphics {
        projectile ArmorPickup
        animation throwobject
    }

    cost {
        mana 5
        infcantrip true
    }

    target {
        min_range 1
        max_range 2+level
    }

    damage_instance {
        damage 0

        effects {
            Shield 3
            ObjectOnHitFullyEmpty RandomArmorPickup
        }
    }
}
```

---

### `ThrowShield2`
**Description:** Give +3 [img:shield] to units in an area and spawn scrap pickups on the empty tiles in that area.  
**Source:** `tank_abilities.gon`  

```
ThrowShield2 {
    variant_of ThrowShield

    meta {
        desc "ABILITY_THROWSCRAP2_DESC"
    }

    target {
        min_range 0
        max_aoe 1
    }
}
```

---

### `ChewCud`
**Name:** Chew Cud  
**Description:** Heal yourself.  
**Source:** `tank_abilities.gon`  

```
ChewCud {
    template self_buff
    
    meta {
        name "ABILITY_CHEWCUD_NAME"
        desc "ABILITY_CHEWCUD_DESC"
        class Tank
    }

    graphics {
        animation gulp
    }
    
    cost {
        mana 3
        infcantrip true
    }
    
    damage_instance {
        heal 3
    }
}
```

---

### `ChewCud2`
**Description:** Heal yourself more.  
**Source:** `tank_abilities.gon`  

```
ChewCud2 {
    variant_of ChewCud

    meta {
        desc "ABILITY_CHEWCUD2_DESC"
    }

    damage_instance {
        heal 6
    }
}
```

---

### `AssBlast`
**Name:** Ass Blast  
**Description:** Knock back units in an area near you 4 tiles.  
**Source:** `tank_abilities.gon`  

```
AssBlast {
    template melee_attack
    
    meta {
        name "ABILITY_ASSBLAST_NAME"
        desc "ABILITY_ASSBLAST_DESC"
        class Tank
        type_icon "defense"
    }

    graphics {
        animation poopfart
    }
    
    cost {
        mana 3
        infcantrip true
    }
    
    target {
        aoe_mode standard
        max_aoe 2
        aoe_excludes_self true
        knockback_mode character_to_tile
    }
    
    damage_instance {
        type spell
        damage 0
        knockback 4
        incidentally_collects_pickups false

        elements [
            Explosion
        ]
    }
}
```

---

### `AssBlast2`
**Description:** Knock back units in a larger area near you 10 tiles.  
**Source:** `tank_abilities.gon`  

```
AssBlast2 {
    variant_of AssBlast

    meta {
        desc "ABILITY_ASSBLAST2_DESC"
    }

    target {
        max_aoe 3
    }

    damage_instance {
        knockback 10
    }
}
```

---

### `Chew`
**Name:** Chew  
**Description:** A melee attack with Lifesteal.  
**Source:** `tank_abilities.gon`  

```
Chew {
    template melee_attack
    
    meta {
        name "ABILITY_CHEW_NAME"
        desc "ABILITY_CHEW_DESC"
        class Tank
    }

    graphics {
	    animation dashbite
    }

    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        type melee

        effects {
            Leech 1
        }
    }
}
```

---

### `Chew2`
**Description:** A melee attack with Lifesteal that inflicts Bleed 2 and ignores shield.  
**Source:** `tank_abilities.gon`  

```
Chew2 {
    variant_of Chew

    meta {
        desc "ABILITY_CHEW2_DESC"
    }

    damage_instance {
        piercing true

        effects {
            Bleed 2
        }
    }
}
```

---

### `BatterUp`
**Name:** Batter Up  
**Description:** Knock a unit back 10 tiles.  
**Source:** `tank_abilities.gon`  

```
BatterUp {
    template melee_attack
    
    meta {
        name "ABILITY_BATTERUP_NAME"
        desc "ABILITY_BATTERUP_DESC"
        class Tank
        type_icon "melee"
        icon_damage_display_eq 3+bonus_melee_ability_damage
        icon_shell_frame attack
    }

    graphics {
        animation knockswatatk
    }

    cost {
        infcantrip true
        mana 5
    }
    sounds {
        oncastpoint Batterup_Swing_Castpoint
    }

    damage_instance {
        damage 0
        type melee
        knockback 10

        effects {
            OverrideKnockbackDamage 3+bonus_melee_ability_damage
            SoundEventOnHit Batterup_Connect
        }
    }
}
```

---

### `BatterUp2`
**Description:** Knock a unit back 10 tiles with Chain Knockback.  
**Source:** `tank_abilities.gon`  

```
BatterUp2 {
    variant_of BatterUp

    meta {
        desc "ABILITY_BATTERUP2_DESC"
    }
    damage_instance {
        effects {
            OverrideChainKnockback 10
            OverrideChainKnockbackDamage 3+bonus_melee_ability_damage
        }
    }
}
```

---

### `BackBreaker`
**Name:** Backbreaker  
**Description:** A melee attack that Immobilizes.  
**Source:** `tank_abilities.gon`  

```
BackBreaker {
    template melee_attack
    
    meta {
        name "ABILITY_BACKBREAKER_NAME"
        desc "ABILITY_BACKBREAKER_DESC"
        class Tank
    }

    graphics {
        animation throwbigelement
    }

    cost {
        infcantrip true
        mana 6
    }

    damage_instance {
        damage 3+bonus_melee_ability_damage
        type melee

        effects {
            Immobile 1
        }
    }
}
```

---

### `BackBreaker2`
**Description:** A melee attack that Immobilizes and gives -2 [img:spd].  
**Source:** `tank_abilities.gon`  

```
BackBreaker2 {
    variant_of BackBreaker

    meta {
        desc "ABILITY_BACKBREAKER2_DESC"
    }

    damage_instance {
        damage 3+bonus_melee_ability_damage
        effects {
            Immobile 1
            SpeedUp -2
        }
    }
}
```

---

### `Suplex`
**Name:** Suplex  
**Description:** Grab a unit in front of you and slam it into the tile behind you.  
**Source:** `tank_abilities.gon`  

```
Suplex {
    template melee_attack
    class SuplexAbility
    
    meta {
        name "ABILITY_SUPLEX_NAME"
        desc "ABILITY_SUPLEX_DESC"
        class Tank
    }

    graphics {
        animation suplex
    }

    cost {
        infcantrip true
        mana 5
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

### `Suplex2`
**Description:** Grab a unit in front of you and slam it into the tile behind you, inflicting Bruise 3 and Immobile.  
**Source:** `tank_abilities.gon`  

```
Suplex2 {
    variant_of Suplex

    meta {
        desc "ABILITY_SUPLEX2_DESC"
    }

    damage_instance {
        effects {
            Bruise 3
            Immobile 1
        }
    }
}
```

---

### `Intimidate`
**Name:** Intimidate  
**Description:** Inflict Fear on an adjacent unit.  
**Source:** `tank_abilities.gon`  

```
Intimidate {
    template melee_attack
    
    meta {
        name "ABILITY_INTIMIDATE_NAME"
        desc "ABILITY_INTIMIDATE_DESC"
        class Tank
        type_icon "defense"
    }

    graphics {
        animation angry
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        damage 0
        type status_spell
        makes_contact false
        incidentally_collects_pickups false

        effects {
            Fear 1
        }
    }
}
```

---

### `Intimidate2`
**Description:** Inflict Fear on a unit up to five tiles away.  
**Source:** `tank_abilities.gon`  

```
Intimidate2 {
    variant_of Intimidate

    meta {
        desc "ABILITY_INTIMIDATE2_DESC"
    }

    target {
        target_mode tile
        max_range 5
    }
}
```

---

### `Toss`
**Name:** Toss  
**Description:** Throw an adjacent unit to an open tile.  
**Source:** `tank_abilities.gon`  

```
Toss {
    template throw_attack
    
    meta {
        name "ABILITY_TOSS_NAME"
        desc "ABILITY_TOSS_DESC"
        class Tank
        type_icon "defense"
    }

    graphics {
        animation knockupatk
    }

    cost {
        mana 3
        infcantrip true
    }
    
    target {
        max_range 3+2*level
    }
    
    damage_instance {
        damage 1

        blocked_damage 5+bonus_melee_ability_damage
    }
}
```

---

### `Toss2`
**Description:** Throw an adjacent unit to a tile, dealing bonus damage if it collides with something.  
**Source:** `tank_abilities.gon`  

```
Toss2 {
    variant_of Toss

    meta {
        desc "ABILITY_TOSS2_DESC"
    }

    target {
        restrictions none
    }
}
```

---

### `BonusToss`
**Name:** Toss  
**Description:** Throw an adjacent unit to an open tile.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
BonusToss { //bonus ability for Wrestlemania
    template throw_attack
    
    meta {
        name "ABILITY_TOSS_NAME"
        desc "ABILITY_WRESTLETOSS_DESC"
        class Tank
        type_icon "defense"
        ability_icon "Toss"
    }

    graphics {
        animation knockupatk
    }

    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_range 5
    }
    
    damage_instance {
        damage 1

        blocked_damage 5+bonus_melee_ability_damage
    }
}
```

---

### `BonusToss2`
**Description:** Throw an adjacent unit to a tile, dealing bonus damage if it collides with something.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
BonusToss2 { //bonus ability for Wrestlemania
    variant_of BonusToss

    meta {
        desc "ABILITY_WRESTLETOSS2_DESC"
    }

    target {
        restrictions none
    }
    
    damage_instance {
        damage 1

        blocked_damage 5+bonus_melee_ability_damage
    }
}
```

---

### `NubbyToss`
**Name:** Toss  
**Description:** Throw your crippled friend to any tile.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
NubbyToss { //bonus ability for MyLeg
    template throw_attack
    
    meta {
        name "ABILITY_TOSS_NAME"
        desc "ABILITY_NUBBYTOSS_DESC"
        class Tank
        type_icon "defense"
        ability_icon "Toss"
    }

    graphics {
        animation knockupatk
    }

    cost {
        mana 0
        cantrip true
    }
    
    target {
        max_range 20
        restrictions none
        force_no_contact true
        prioritize_throw_target_with_passive NubbyTossPriority
    }
    
    damage_instance {
        damage 1
    }
}
```

---

### `BellyFlop`
**Name:** Belly Flop  
**Description:** Jump to a tile and Immobilize anything you land on.  
**Source:** `tank_abilities.gon`  

```
BellyFlop {
    template jump_attack

    meta {
        name "ABILITY_BELLYFLOP_NAME"
        desc "ABILITY_BELLYFLOP_DESC"
        class Tank
    }

    graphics {
        jump_start_animation bellyflopStart
        air_animation bellyflop_air
        jump_attack_animation bellyflopEnd
        land_animation none
    }

    cost {
        mana 6
        infcantrip true
    }
    
    target {
        max_range 3

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
            Immobile 1
        }
    }
}
```

---

### `BellyFlop2`
**Description:** Jump to a tile and Immobilize units in an area.  
**Source:** `tank_abilities.gon`  

```
BellyFlop2 {
    variant_of BellyFlop

    meta {
        desc "ABILITY_BELLYFLOP2_DESC"
    }

    target {
        max_range 5
        max_aoe 1
    }

    splash_damage {
        damage 1+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
            Immobile 1
        }
    }
}
```

---

### `ToadJump_BasicMove`
**Name:** Jump  
**Description:** Jump to a tile and damage what you land on.  
**Source:** `tank_abilities.gon`  

```
ToadJump_BasicMove {
    template jump_attack

    meta {
        name "ABILITY_JUMP_NAME"
        desc "ABILITY_TOADJUMP_DESC"
        animate_name false
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        move_points 1
        act_points 0
    }
    
    target {
        min_range 1
        max_range mov
        
        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `BellyFlop_BasicMove`
**Name:** Jump  
**Description:** Jump to a tile and damage what you land on.  
**Source:** `tank_abilities.gon`  

```
BellyFlop_BasicMove {
    template jump_attack

    meta {
        name "ABILITY_JUMP_NAME"
        desc "ABILITY_BELLYJUMP_DESC"
        animate_name false
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        move_points 1
        act_points 0
    }
    
    target {
        min_range 1
        max_range mov
        
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
        }
    }
}
```

---

### `TankTrample`
**Name:** Trample Dash  
**Description:** Dash forward with Trample, then spawn a rock.  
**Source:** `tank_abilities.gon`  

```
TankTrample {
    template trample_dash
    
    meta {
        name "ABILITY_TRAMPLEDASH_NAME"
        desc "ABILITY_TRAMPLEDASH_DESC"
        class Tank
        type_icon "melee"
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_end_animation dashend
    }
    
    cost {
        mana 6
        infcantrip true
    }
    
    target {

    }

    temporary_effects {
        Trample 3
    }
    
    damage_instance {
        damage 3
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

### `TankTrample2`
**Description:** Dash forward with Trample, then spawn a rock. Deals more damage and has a 20% chance to inflict Stun.  
**Source:** `tank_abilities.gon`  

```
TankTrample2 {
    variant_of TankTrample

    meta {
        desc "ABILITY_TRAMPLEDASH2_DESC"
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage

        effects {
            Stun [1, .2]
        }
    }
}
```

---

### `TankSwap`
**Name:** Swap  
**Description:** Swap positions with any ally.  
**Source:** `tank_abilities.gon`  

```
TankSwap {
    template swap
    
    meta {
        name "ABILITY_TANKSWAP_NAME"
        desc "ABILITY_TANKSWAP_DESC"
        animate_name true
        class Tank
    }

    graphics {
    }

    cost {
        mana 5
        infcantrip true
    }

    target {
        max_range 20
        restrictions [must_be_swappable aoe_must_exist]
        aoe_restrictions [allies_only]
    }
}
```

---

### `TankSwap2`
**Description:** Swap positions with any unit.  
**Source:** `tank_abilities.gon`  

```
TankSwap2 {
    variant_of TankSwap

    meta {
        desc "ABILITY_TANKSWAP2_DESC"
    }

    cost {
        mana 3
    }
    target {
        aoe_restrictions none
    }
}
```

---

### `ToTheRescue`
**Name:** To the Rescue!  
**Description:** Jump to a tile adjacent to an ally. Damage and displace any units you land on.  
**Source:** `tank_abilities.gon`  

```
ToTheRescue {
    template jump_attack

    meta {
        name "ABILITY_TOTHERESCUE_NAME"
        desc "ABILITY_TOTHERESCUE_DESC"
        class Tank
        type_icon "movement"
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 5
        infcantrip true
    }
    
    target {
        max_range 20

        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions [must_be_adjacent_to_ally]
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `ToTheRescue2`
**Description:** Jump to a tile adjacent to an ally. Damage and displace any units you land on, or are adjacent to.  
**Source:** `tank_abilities.gon`  

```
ToTheRescue2 {
    variant_of ToTheRescue

    meta {
        desc "ABILITY_TOTHERESCUE2_DESC"
    }

    cost {
        mana 3
        infcantrip true
    }

    target {
        max_aoe 1
        aoe_restrictions [exclude_allies]
    }

    splash_damage {
        damage 5+bonus_melee_ability_damage

        knockback 1
    }
}
```

---

### `TankTantrum`
**Name:** Tantrum  
**Description:** Hit all adjacent units, then spawn a rock.  
**Source:** `tank_abilities.gon`  

```
TankTantrum {
    template melee_attack
    
    meta {
        name "ABILITY_TANKTANTRUM_NAME"
        desc "ABILITY_TANKTANTRUM_DESC"
        class Tank
    }

    graphics {
        animation spinAttack
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        target_mode none
        aoe_mode cross
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 1+bonus_melee_ability_damage

        elements [
            Earth
        ]
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

### `TankTantrum2`
**Description:** Hit all adjacent and diagonally adjacent units, then spawn a rock.  
**Source:** `tank_abilities.gon`  

```
TankTantrum2 {
    variant_of TankTantrum

    meta {
        desc "ABILITY_TANKTANTRUM2_DESC"
    }

    target {
        aoe_mode square
    }
    damage_instance {
        damage 3+bonus_melee_ability_damage
    }
}
```

---

### `Earthquake`
**Name:** Earthquake  
**Description:** Deal damage in a cone with a 10% chance to Petrify. Has a chance to spawn rocks.
\[s:.7\](This spell spawns rocks.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
Earthquake {
    template spell

    meta {
        name "ABILITY_EARTHQUAKE_NAME"
        desc "ABILITY_EARTHQUAKE_DESC"
        class Tank
    }

    graphics {
        animation earthquakeSlam
        delay 3
        particle Earthquake
    }
    
    cost {
        mana 7
        infcantrip true
    }

    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 4
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

### `Earthquake2`
**Description:** Deal more damage in a cone with a 20% chance to Petrify. Has a chance to spawn rocks.
\[s:.7\](This spell spawns rocks.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
Earthquake2 {
    meta {
        desc "ABILITY_EARTHQUAKE2_DESC"
    }

    variant_of Earthquake
    damage_instance {
        damage 5

        effects {
            Petrify [1, .20]
        }
    }
}
```

---

### `RockToss`
**Name:** Rock Toss  
**Description:** Throw a rock with a 10% chance to Stun.  
**Source:** `tank_abilities.gon`  

```
RockToss {
    template lobbed_attack

    meta {
        name "ABILITY_ROCKTOSS_NAME"
        desc "ABILITY_ROCKTOSS_DESC"
        class Tank
    }

    graphics {
        projectile SmallRock
        animation throwobject
    }
    
    cost {
        mana 5
        infcantrip true
    }
    
    target {
        min_range 1
        max_range 3+bonus_range
    }
    
    damage_instance {
        damage 2+bonus_ranged_damage

        effects {
            Stun [1, .10]
            BounceObject SmallRock
        }

        elements [
            Rock
        ]
    }
}
```

---

### `RockToss2`
**Description:** Throw a rock with a 33% chance to Stun.  
**Source:** `tank_abilities.gon`  

```
RockToss2 {
    variant_of RockToss

    graphics {
        lob_height -1
    }

    meta {
        desc "ABILITY_ROCKTOSS2_DESC"
    }

    target {
        min_range 1
        max_range 5+bonus_range
        restrictions none
    }

    damage_instance {
        damage 4+bonus_ranged_damage

        effects {
            Stun [1, .33]
        }
    }
}
```

---

### `BarbedWire`
**Name:** Barbed Wire  
**Description:** Give a unit +5 Thorns until your next turn.
\[s:.7\](You can target yourself.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
BarbedWire {
    template lobbed_attack
    
    meta {
        name "ABILITY_BARBEDWIRE_NAME"
        desc "ABILITY_BARBEDWIRE_DESC"
        class Tank
        type_icon "buff"
    }

    graphics {
        projectile barbedwire
        animation throwobject
    }

    cost {
        mana 3
        infcantrip true
    }

    target {
        min_range 0
        max_range 5
        max_aoe 0
    }

    damage_instance {
        damage 0

        effects {
            Temporary {
                status Thorns
                stacks 5
                turns 1
                expires_on_appliers_turn true
            }
        }
    }
}
```

---

### `BarbedWire2`
**Name:** Barbed Wire  
**Description:** Give a unit or object +5 Thorns until your next turn.
\[s:.7\](You can target yourself.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
BarbedWire2 {
    template spell
    
    meta {
        name "ABILITY_BARBEDWIRE_NAME"
        desc "ABILITY_BARBEDWIRE2_DESC"
        class Tank
        type_icon "buff"
    }

    graphics {
		particle none
    }

    cost {
        mana 3
        infcantrip true
    }

    target {
        min_range 0
        max_range 20
        max_aoe 0
    }

    damage_instance {
        damage 0

        effects {
            CanApplyToInanimate {
                Temporary {
                    status Thorns
                    stacks 5
                    turns 1
                    expires_on_appliers_turn true
                }
            }
        }
    }
}
```

---

### `DrawAttention`
**Name:** Goad  
**Description:** Force an enemy to move towards you.  
**Source:** `tank_abilities.gon`  

```
DrawAttention {
    template spell

    meta {
        name "ABILITY_TANKMOCK_NAME"
        desc "ABILITY_TANKMOCK_DESC"
        class Tank
        type_icon "misc"
    }
    graphics {
        animation howl
        particle none
    }
    
    cost {
        mana 3
        infcantrip true
    }

    
    target {
        min_range 1
        max_range 6
        max_aoe 0

        restrictions must_have_enemy
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

### `DrawAttention2`
**Description:** Force an enemy anywhere to move towards you.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
DrawAttention2 {
    variant_of DrawAttention

    meta {
        desc "ABILITY_TANKMOCK2_DESC"
    }

    cost {
        mana 2
    }

    target {
        max_range 20
    }
}
```

---

### `BowlOver`
**Name:** Bowl Over  
**Description:** Trample over one tile diagonally.  
**Source:** `tank_abilities.gon`  

```
BowlOver {
    template move
    
    meta {
        name "ABILITY_BOWLOVER_NAME"
        desc "ABILITY_BOWLOVER_DESC"
        class Tank
        animate_name true
    }

    graphics {
        sync_speed 22
        max_tiles_single_loop 5
        ignore_slowtiles true
        move_start_animation startroll
        animation roll
        move_end_animation endroll
    }

    cost {
        infcantrip true
        mana 2
    }

    temporary_effects {
        Trample 3
    }

    target {
        range_mode diagcross
        max_range 1
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_diagonals true
    }
}
```

---

### `BowlOver2`
**Description:** Trample over two tiles diagonally with a 10% chance to inflict Stun.  
**Source:** `tank_abilities.gon`  

```
BowlOver2 {
    variant_of BowlOver

    meta {
        desc "ABILITY_BOWLOVER2_DESC"
    }

    target {
        max_range 2
    }

    damage_instance {
        override_trample_damage true
        damage 3
        effects {
            Stun [1 .1]
        }
    }
}
```

---

### `Clap`
**Name:** Clap  
**Description:** Knock 2 enemies in front of you together.  
**Source:** `tank_abilities.gon`  

```
Clap {
    template melee_attack
    
    meta {
        name "ABILITY_CLAP_NAME"
        desc "ABILITY_CLAP_DESC"
        class Tank
        type_icon "melee"
    }

    tags [musical]

    graphics {
        animation clapTogether
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    target {
        aoe_mode custom
        custom_aoe [ [1, 1], [1, -1] ]
        range_display_include_direction true

        knockback_mode perp_towards_facing
    }
    
    damage_instance {
        damage 0
        knockback 1
    }
}
```

---

### `Clap2`
**Description:** Knock 2 enemies in front of you together with +2 knockback damage.  
**Source:** `tank_abilities.gon`  

```
Clap2 {
    variant_of Clap

    meta {
        desc "ABILITY_CLAP2_DESC"
    }

    damage_instance {
        effects {
            BonusKnockbackDamage 2
        }
    }
}
```

---

### `TankRockSong`
**Name:** Rock Song  
**Description:** Levitate all rocks. They will automatically fling towards enemies that end movement in line with them.  
**Source:** `tank_abilities.gon`  

```
TankRockSong {
    template spell

    meta {
        name "ABILITY_ROCKSONG_NAME"
        desc "ABILITY_ROCKSONG_DESC"
        class Tank
        type_icon "misc"
    }

    tags [musical]
    
    graphics {
        particle none
        animation howl
    }
    
    cost {
        mana 6
        infcantrip true
    }
    
    target {
        target_mode none
        aoe_mode all
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

### `TankRockSong2`
**Description:** Levitate all rocks. They will automatically fling towards enemies that end movement in line with them.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
TankRockSong2 {
    variant_of TankRockSong

    meta {
        desc "ABILITY_ROCKSONG2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `RockCrusher`
**Name:** Rock Crusher  
**Description:** Jump on top of a rock, exploding it. Deal damage and knock back all adjacent units.  
**Source:** `tank_abilities.gon`  

```
RockCrusher {
    template jump_attack

    meta {
        name "ABILITY_ROCKCRUSHER_NAME"
        desc "ABILITY_ROCKCRUSHER_DESC"
        class Tank
    }

    keyword_tooltips {}

    graphics {
        jump_start_animation bellyflopStart
        air_animation bellyflop_air
        jump_attack_animation bellyflopEnd
        land_animation none
    }

    cost {
        mana 4
        infcantrip true
    }
    
    target {
        max_range 20
        min_range 1

        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions [must_have_tag]
        target_requires_tag rock
    }

    damage_instance {
        damage 0
        override_trample_damage true

        effects {
            IgnoreSelf 1

            Conditional_HasTag {
                tag rock

                Conditional_NotBoss {
                    ExplodeCharacter_RockCrusher 5
                }
                Conditional_Boss {
                    RemoveStatus Petrify

                    Conditional_HasStatus {
                        status Petrify
                        BonusDamage 20
                    } Else {
                        BonusDamage 5
                    }

                    ExplodeCharacter_RockCrusher_PetrifyBreak 5
                }
            }
        }

        elements [
            Earth,
        ]
    }
}
```

---

### `RockCrusher2`
**Description:** Jump on top of a rock, exploding it. Deal high damage and knock back all adjacent units.  
**Source:** `tank_abilities.gon`  

```
RockCrusher2 {
    variant_of RockCrusher

    meta {
        desc "ABILITY_ROCKCRUSHER2_DESC"
    }

    damage_instance {
        effects {
            Conditional_HasTag {
                Conditional_NotBoss {
                    ExplodeCharacter_RockCrusher 9
                }
                Conditional_Boss {
                    RemoveStatus Petrify

                    Conditional_HasStatus {
                        status Petrify
                        BonusDamage 20
                    } Else {
                        BonusDamage 5
                    }

                    ExplodeCharacter_RockCrusher_PetrifyBreak 9
                }
            }
        }
    }
}
```

---

### `BodyGuard`
**Name:** Body Guard  
**Description:** The next time an ally is targeted by an enemy, switch places with that ally.  
**Source:** `tank_abilities.gon`  

```
BodyGuard {
    template self_buff
    
    meta {
        name "ABILITY_BODYGUARD_NAME"
        desc "ABILITY_BODYGUARD_DESC"
        class Tank
    }

    graphics {
    }
    
    cost {
        mana 2
        infcantrip true
    }
    
    damage_instance {
        effects {
            BodyGuard {
                stacks 1
                ability BodyGuardSwap
            }
        }
    }
}
```

---

### `BodyGuard2`
**Description:** The next time an ally is targeted by an enemy, switch places with that ally and gain +4 [img:shield].  
**Source:** `tank_abilities.gon`  

```
BodyGuard2 {
    variant_of BodyGuard

    meta {
        desc "ABILITY_BODYGUARD2_DESC"
    }

    damage_instance {
        effects {
            BodyGuard {
                stacks 1
                ability BodyGuardSwap2
            }
        }
    }
}
```

---

### `BodyGuardSwap`
**Name:** Swap  
**Description:** {he} swap  
**Source:** `tank_abilities.gon`  

```
BodyGuardSwap { //util ability for BodyGuard
    template swap
    
    meta {
        name "ABILITY_SWAP_NAME"
        desc "ABILITY_SWAP_DESC"
        animate_name true
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn

        mode yeet //yeet or overlay
    }
}
```

---

### `BodyGuardSwap2`
**Name:** Swap  
**Description:** {he} swap  
**Source:** `tank_abilities.gon`  

```
BodyGuardSwap2 { //util ability for BodyGuard2
    template swap
    
    meta {
        name "ABILITY_SWAP_NAME"
        desc "ABILITY_SWAP_DESC"
        animate_name true
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn

        mode yeet //yeet or overlay
    }

    
    self_damage {
        effects {
            Shield 4
        }
    }
}
```

---

### `Gore`
**Name:** Gore  
**Description:** Dash 3 tiles, damage, inflict Bruise and throw what you hit towards your original tile.  
**Source:** `tank_abilities.gon`  

```
Gore {
    template dash_attack
    
    meta {
        name "ABILITY_GORE_NAME"
        desc "ABILITY_GORE_DESC"
        class Tank
    }
    
    graphics {
        dash_start_animation headbuttdashStart
        dash_animation headbuttdash
        dash_attack_animation headbuttUppercut
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_range 3
    }
    
    damage_instance {
        damage 2+bonus_melee_ability_damage
        makes_contact true

        effects {
            DisplaceToOriginalPosition 1
            Bruise 1
        }
    }
}
```

---

### `Gore2`
**Description:** Dash 10 tiles, damage, inflict Bruise and throw what you hit towards your original tile.  
**Source:** `tank_abilities.gon`  

```
Gore2 {
    variant_of Gore

    meta {
        desc "ABILITY_GORE2_DESC"
    }

    target {
        max_range 10
    }

    damage_instance {
        damage 4+bonus_melee_ability_damage
        makes_contact true

        effects {
            DisplaceToOriginalPosition 1
            Bruise 1
        }
    }
}
```

---

### `RockBlast_AI`
**Source:** `tank_abilities.gon`  

```
RockBlast_AI {
    template melee_attack
    
    target { 
        max_aoe 10
        aoe_restrictions must_have_line_of_sight
    }
    damage_instance {
        damage 5
    }
}
```

---

### `RockBlast`
**Name:** Rock Blast  
**Description:** Shoot a rock forward.  
**Source:** `tank_abilities.gon`  

```
RockBlast { //TODO: make less janky
    template melee_attack
    ai_ability RockBlast_AI
    
    meta {
        name "ABILITY_ROCKBLAST_NAME"
        desc "ABILITY_ROCKBLAST_DESC"
        class Tank
        type_icon "melee"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 6
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

### `RockBlast2`
**Description:** Shoot a rock forward with Chain Knockback.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
RockBlast2 {
    variant_of RockBlast

    meta {
        desc "ABILITY_ROCKBLAST2_DESC"
    }

    cost {
        mana 3
    }

    damage_instance {
        effects {
            OverrideChainKnockback 1
        }
    }
}
```

---

### `RockTomb`
**Name:** Rock Tomb  
**Description:** Damage and Petrify a unit within 3 tiles of you.  
**Source:** `tank_abilities.gon`  

```
RockTomb {
    template spell
    
    meta {
        name "ABILITY_ROCKTOMB_NAME"
        desc "ABILITY_ROCKTOMB_DESC"
        class Tank
    }

    graphics {
        animation floatingmagic
        particle Earthquake
        //affected_particle PetrifyCube
        //fx_is_placeholder_animation true
    }

    cost {
        mana 8
        infcantrip true
    }

    target {
        min_range 0
        max_range 3
        max_aoe 0
    }

    damage_instance {
        damage 3

        effects {
            Petrify 1
        }
    }
}
```

---

### `RockTomb2`
**Description:** Damage and Petrify a unit within 5 tiles of you.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
RockTomb2 {
    variant_of RockTomb

    meta {
       desc "ABILITY_ROCKTOMB2_DESC"
    }

    cost {
        mana 6
    }
    target {
        max_range 5
    }
}
```

---

### `SwapPositions_WideLoad`
**Source:** `tank_abilities.gon`  

```
SwapPositions_WideLoad { //util ability for WideLoad
    template swap

    target {
        max_range 1
        restrictions [must_be_swappable aoe_must_exist]
    }
}
```

---

### `SwapPositions_WideLoad2`
**Source:** `tank_abilities.gon`  

```
SwapPositions_WideLoad2 {
    variant_of TankSwap

    target {
        max_range 3
    }

    self_damage {
        effects {
            Temporary {
                status Thorns
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
            Temporary {
                status Brace
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `BearHug`
**Name:** Grab  
**Description:** Pull a unit within 2 tiles towards you, knocking it into you.  
**Source:** `tank_abilities.gon`  

```
BearHug {
    template melee_attack
    
    meta {
        name "ABILITY_GRAB_NAME"
        desc "ABILITY_GRAB_DESC"
        class Tank
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 2
        knockback_mode tile_to_character
        aoe_restrictions must_have_line_of_sight_unpurgable
    }

    temporary_effects {
        KnockbackImmunity 1
    }
    
    damage_instance {
        damage 0
        knockback 10
    }
}
```

---

### `BearHug2`
**Description:** Pull a unit within 4 tiles towards you, knocking it into you and inflicting Grappled.  
**Source:** `tank_abilities.gon`  

```
BearHug2 {
    variant_of BearHug

    meta {
        desc "ABILITY_GRAB2_DESC"
    }

    target {
       max_aoe 4
    }
    
    damage_instance {
        effects {
            Grappled 1
        }
    }
}
```

---

### `Fissure`
**Name:** Fissure  
**Description:** Pull all units in a wide line towards the center of that line. This has a 10% chance to Petrify.  
**Source:** `tank_abilities.gon`  

```
Fissure {
    template spell

    meta {
        name "ABILITY_FISSURE_NAME"
        desc "ABILITY_FISSURE_DESC"
        class Tank
    }
    
    cost {
        infcantrip true
        mana 5
    }

    graphics {
		animation groundpound
        particle Earthquake
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
        
        effects {
            Petrify [1 .1]
        }

        elements [
            Earth
        ]
    }
}
```

---

### `Fissure2`
**Description:** Pull all units in a wide line towards the center of that line. This has a 15% chance to Petrify and spawns rocks.  
**Source:** `tank_abilities.gon`  

```
Fissure2 {
    variant_of Fissure

    meta {
        desc "ABILITY_FISSURE2_DESC"
    }

    damage_instance {
        effects {
            Petrify [1 .15]
            LeaveBehindRockOnKnockback 1
        }
    }
}
```

---

### `BigRock`
**Name:** Big Rock  
**Description:** Drop a boulder on an adjacent tile, damaging and displacing units it lands on.  
**Source:** `tank_abilities.gon`  

```
BigRock {
    template spawn

    meta {
        name "ABILITY_BIGROCK_NAME"
        desc "ABILITY_BIGROCK_DESC"
        class Tank
        type_icon "melee"
        icon_shell_frame damage
    }
    
    graphics {
        lob true
        animation shoot
    }

    cost {
        infcantrip true
        mana 7
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_be_displaceable
        aoe_restrictions none
    }

    spawn {
        object Boulder
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        type melee
        force_no_contact true
    }
}
```

---

### `BigRock2`
**Description:** Drop a boulder on an adjacent tile, damaging, Stunning and displacing units it lands on.  
**Source:** `tank_abilities.gon`  

```
BigRock2 {
    variant_of BigRock

    meta {
        desc "ABILITY_BIGROCK2_DESC"
    }

    damage_instance {
        effects {
            Stun 1
        }
    }
}
```

---

### `FlipFlop`
**Name:** Flip Flop  
**Description:** Jump up to 3 tiles away, damage units you land on, then gain -1 [img:spd].
\[s:.7\](This spell's mana cost is equal to your [img:spd].
At 0 [img:spd], this spell is Castable once per turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
FlipFlop {
    template jump_attack

    meta {
        name "ABILITY_FLIPFLOP_NAME"
        desc "ABILITY_FLIPFLOP_DESC"
        class Tank
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana spd
        move_points 0
        act_points 0
        charge "1-clamp(spd,0,1)"
        initial_charge 1
    }
    
    target {
        max_range 3

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none
    }

    self_damage {
        effects {
            SpeedUp -1
        }
    }

    damage_instance {
        damage 3+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `FlipFlop2`
**Description:** Jump up to 4 tiles away, damage units you land on, then gain -1 [img:spd].
If your [img:spd] is 0, this has increased range and damage.
\[s:.7\](This spell's mana cost is equal to your [img:spd].
At 0 [img:spd], this spell is Castable once per turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
FlipFlop2 {
    variant_of FlipFlop

    meta {
        desc "ABILITY_FLIPFLOP2_DESC"
    }

    target {
        max_range "4+(1-clamp(spd,0,1))*2"
    }

    damage_instance {
        damage "4+(1-clamp(spd,0,1))*2+bonus_melee_ability_damage"

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `Lunge`
**Name:** Lunge  
**Description:** Dash forward one tile and attack with Knockback.
This spell uses up your movement action.  
**Source:** `tank_abilities.gon`  

```
Lunge {
    template dash_attack
    
    meta {
        name "ABILITY_LUNGE_NAME"
        desc "ABILITY_LUNGE_DESC"
        class Tank
    }

    graphics {
        dash_start_animation headbuttdashStart
        dash_animation headbuttdash
        dash_attack_animation headbuttdashEnd
    }

    cost {
        mana 0
        act_points 0
        move_points 1
        charge 0
    }

    target { 
        max_range 1+bonus_range
        max_aoe 1
        aoe_restrictions must_have_line_of_sight_unpurgable
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 1
    }
}
```

---

### `Lunge2`
**Description:** Dash forward one tile, attack with Knockback and inflict Stun.
This spell uses up your movement action.  
**Source:** `tank_abilities.gon`  

```
Lunge2 {
    variant_of Lunge

    meta {
        desc "ABILITY_LUNGE2_DESC"
    }

    damage_instance {
        effects {
            Stun 1
        }
    }
}
```

---

### `Nudge`
**Name:** Nudge  
**Description:** Push a unit back 1 tile.
\[s:.7\](This spell costs 0 mana the first time it's used each turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
Nudge {
    template melee_attack
    
    meta {
        name "ABILITY_NUDGE_NAME"
        desc "ABILITY_NUDGE_DESC"
        class Tank
        type_icon "melee"
    }

    graphics {
        animation bigkick
    }

    cost {
        infcantrip true
        mana 3
    }
    bonus_passives {
        FreeFirstCast 1
    }

    damage_instance {
        damage 0
        type melee
        knockback 1
    }
}
```

---

### `Nudge2`
**Description:** Push a unit back 10 tiles.
\[s:.7\](This spell costs 0 mana the first time it's used each turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
Nudge2 {
    variant_of Nudge

    meta {
        desc "ABILITY_NUDGE2_DESC"
    }

    damage_instance {
        knockback 10
    }
}
```

---

### `StoneGaze`
**Name:** Stone Breath  
**Description:** Inflict Petrify on the first unit in a line.  
**Source:** `tank_abilities.gon`  

```
StoneGaze {
    template spell

    meta {
        name "ABILITY_STONEBREATH_NAME"
        desc "ABILITY_STONEBREATH_DESC"
        class Tank
        type_icon "magic" //needs wind element
    }

    graphics {
        particle fx_windSpell
        //affected_particle Earthquake
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        target_mode direction
        aoe_mode line
        
        max_aoe 10
        
        aoe_considers_character_size true
        aoe_excludes_self true
        knockback_mode character_to_tile
        aoe_restrictions must_have_line_of_sight
    }
    
    damage_instance {
        damage 0
        
        effects {
            Petrify 1
        }
	    elements [
            Wind,
        ]
    }
}
```

---

### `StoneGaze2`
**Description:** Inflict Petrify and Knockback on the first unit in a line.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
StoneGaze2 {
    variant_of StoneGaze

    meta {
        desc "ABILITY_STONEBREATH2_DESC"
    }

    cost {
        mana 4
    }

    damage_instance {
        knockback 10
        effects {
            OverrideKnockbackDamage 5 //hack since Petrify is supposed to make things deal 5 knockback damage
        }
    }
}
```

---

### `Medusa`
**Name:** Gorgon Glare  
**Description:** Inflict Petrify on all units in your line of sight.  
**Source:** `tank_abilities.gon`  

```
Medusa {
    template spell
    
    meta {
        name "ABILITY_MEDUSA_NAME"
        desc "ABILITY_MEDUSA_DESC"
        class Tank
    }

    graphics {
        particle none
    }
    
    cost {
        infcantrip true
        mana 10
    }
    
    target {
        aoe_mode all
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

### `Medusa2`
**Description:** Inflict Petrify on all units in your line of sight.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
Medusa2 {
    variant_of Medusa

    meta {
        desc "ABILITY_MEDUSA2_DESC"
    }

    cost {
        mana 8
    }
}
```

---

### `Anchor`
**Name:** Anchor  
**Description:** Gain +4 Brace until the next time you move.  
**Source:** `tank_abilities.gon`  

```
Anchor {
    template self_buff
    
    meta {
        name "ABILITY_ANCHOR_NAME"
        desc "ABILITY_ANCHOR_DESC"
        class Tank
    }

    graphics {
	    animation block
    }
    
    cost {
        mana 6
        infcantrip true
    }
    
    damage_instance {
        effects {
            Temporary {
                status Brace
                stacks 4
                turns 1
                expires_on_move true
            }
        }
    }
}
```

---

### `Anchor2`
**Description:** Gain +4 Brace until the next time you move.
Bonus Passive: Knockback immunity.  
**Source:** `tank_abilities.gon`  

```
Anchor2 {
    variant_of Anchor

    meta {
        desc "ABILITY_ANCHOR2_DESC"
    }

    bonus_passives {
        KnockbackImmunity 1
    }
}
```

---

### `EatRock`
**Name:** Eat Rock  
**Description:** Eat a rock to gain +5 [img:shield] and +1 [img:str].  
**Source:** `tank_abilities.gon`  

```
EatRock {
    template tile_targeted_melee_attack

    meta {
        name "ABILITY_EATROCK_NAME"
        desc "ABILITY_EATROCK_DESC"
        class Tank
    }

    keyword_tooltips {Shield 5}

    graphics {
        animation biteattack
    }

    cost {
        mana 1
        infcantrip true
    }
    
    target {
        restrictions [must_have_tag]
        target_requires_tag rock
    }

    damage_instance {
        damage 0

        effects {
            IgnoreSelf 1

            Conditional_HasTag {
                tag rock

                Conditional_NotBoss {
                    Vaporize 1
                }
                Conditional_Boss {
                    RemoveStatus Petrify

                    Conditional_HasStatus {
                        status Petrify
                        BonusDamage 20
                    } Else {
                        BonusDamage 5
                    }
                }

                ApplyToSource {
                    Shield 5
                    StrengthUp 1
                }
            }
        }
    }
}
```

---

### `EatRock2`
**Name:** Eat Rock  
**Description:** Eat a rock to gain +5 [img:shield] and All Stats Up.  
**Source:** `tank_abilities.gon`  

```
EatRock2 {
    template tile_targeted_melee_attack

    meta {
        name "ABILITY_EATROCK_NAME"
        desc "ABILITY_EATROCK2_DESC"
        class Tank
    }

    keyword_tooltips {Shield 5}

    graphics {
        animation biteattack
    }

    cost {
        mana 1
        infcantrip true
    }
    
    target {
        restrictions [must_have_tag]
        target_requires_tag rock
    }

    damage_instance {
        damage 0

        effects {
            IgnoreSelf 1

            Conditional_HasTag {
                tag rock

                Conditional_NotBoss {
                    Vaporize 1
                }
                Conditional_Boss {
                    RemoveStatus Petrify

                    Conditional_HasStatus {
                        status Petrify
                        BonusDamage 20
                    } Else {
                        BonusDamage 5
                    }
                }

                ApplyToSource {
                    Shield 5
                    AllStatsUp 1
                }
            }
        }
    }
}
```

---

### `PlantFeet`
**Name:** Plant Your Feet  
**Description:** Gain +5 [img:shield] and -1 [img:spd]. 
If you are at 0 [img:spd], instead cleanse all of your debuffs.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
PlantFeet {
    template self_buff
    
    meta {
        name "ABILITY_PLANTFEET_NAME"
        desc "ABILITY_PLANTFEET_DESC"
        class Tank
    }

    graphics {
	    animation bruise
    }
    
    cost {
        mana 0
        cantrip true
    }
    
    damage_instance {
        effects {
            Conditional_FormulaIsPositive {
                formula spd
                SpeedUp -1
                Shield 5
            } Else {
                Cleanse 0
            }
        }
    }
}
```

---

### `PlantFeet2`
**Description:** Gain +6 [img:shield] and -1 [img:spd].
If you are at 0 [img:spd], instead cleanse all of your debuffs and gain All Stats Up.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
PlantFeet2 {
    variant_of PlantFeet

    meta {
        desc "ABILITY_PLANTFEET2_DESC"
    }

    damage_instance {
        effects {
            Conditional_FormulaIsPositive {
                Shield 6
            } Else {
                AllStatsUp 1
            }
        }
    }
}
```

---

### `IronHead`
**Name:** Iron Head  
**Description:** Dash forward up to 3 tiles, gain +4 [img:shield] then damage and knock back adjacent units.  
**Source:** `tank_abilities.gon`  

```
IronHead {   //todo: this is a weird one, lets update it later
    template dash_attack
    
    meta {
        name "ABILITY_IRONHEAD_NAME"
        desc "ABILITY_IRONHEAD_DESC"
        class Tank
    }

    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_attack_animation block
    }

    cost {
        mana 6
        infcantrip true
    }

    target { 
        max_range 3
        min_range 1

        target_mode tile
        range_mode cross

        aoe_mode standard
        min_aoe 1
        max_aoe 1
        knockback_mode character_to_tile

        aoe_considers_character_size true
        aoe_excludes_self true
    }

    self_damage {
        effects {
            Shield 4
        }
    }
    damage_instance {
        damage 0
        knockback 1
    }
}
```

---

### `IronHead2`
**Description:** Dash forward up to 10 tiles, gain +4 [img:shield] then damage and knock back adjacent units with +5 knockback damage.  
**Source:** `tank_abilities.gon`  

```
IronHead2 {
    variant_of IronHead
    
    meta {
        desc "ABILITY_IRONHEAD2_DESC"
    }

    target { 
        max_range 10
    }

    damage_instance {
        effects {
            OverrideKnockbackDamage 5
        }
    }
}
```

---

### `GangUp`
**Name:** Gang Up  
**Description:** Toss a unit to an empty tile within 3 tiles of you, then your allies attack it if they can.  
**Source:** `tank_abilities.gon`  

```
GangUp {
    template throw_attack
    
    meta {
        name "ABILITY_GANGUP_NAME"
        desc "ABILITY_GANGUP_DESC"
        class Tank
        type_icon "attack"
    }

    graphics {
        animation knockupatk
    }

    cost {
        mana 9
        infcantrip true
    }
    
    target {
        max_range 3
    }
    
    damage_instance {
        damage 0

        effects {
            MassAttackThis 1
        }
    }
}
```

---

### `GangUp2`
**Description:** Toss a unit to an empty tile within 6 tiles of you and inflict Bruise, then your allies attack it if they can.  
**Source:** `tank_abilities.gon`  

```
GangUp2 {
    variant_of GangUp

    meta {
        desc "ABILITY_GANGUP2_DESC"
    }

    target {
        max_range 6
    }

    damage_instance {
        effects {
            Bruise 1
        }
    }
}
```

---

### `Aftershock`
**Name:** Aftershock  
**Description:** All units on dirt tiles get tossed to random nearby tiles and take damage when they land.  
**Source:** `tank_abilities.gon`  

```
Aftershock {
    template spell

    meta {
        name "ABILITY_AFTERSHOCK_NAME"
        desc "ABILITY_AFTERSHOCK_DESC"
        class Tank
    }

    graphics {
        animation earthquakeSlam
        particle Earthquake
        delay 3
    }

    cost {
        mana 4
        infcantrip true
    }

    target {
        target_mode none
        aoe_mode all
        
        aoe_restrictions [tile_must_have_element]
        aoe_tile_requires_element Earth
    }

    damage_instance {
        damage 5

        effects {
            TwisterDisplaceWithDamage {
                damage inherit
                max_dist 2
            }
        }

        elements [
            Earth
        ]
    }
}
```

---

### `Aftershock2`
**Description:** All units on dirt tiles get tossed to random tiles and take damage when they land.
Bonus Passive: All of your spells have Earth element.  
**Source:** `tank_abilities.gon`  

```
Aftershock2 {
    variant_of Aftershock

    meta {
        desc "ABILITY_AFTERSHOCK2_DESC"
    }

    bonus_passives {
        AddElementsToSpells Earth
    }
}
```

---

### `SteelSkin`
**Name:** Steelskin  
**Description:** Gain +99 Brace until your next turn, then disable this spell until you take a total of 25 damage.  
**Source:** `tank_abilities.gon`  

```
SteelSkin {
    template self_buff

    meta {
        name "ABILITY_STEELSKIN_NAME"
        desc "ABILITY_STEELSKIN_DESC"
        class Tank
    }
	
    keyword_tooltips { Brace 1 } //disable Reload tooltip

    graphics {
        animation earthquakeSlam
        particle Earthquake
    }
    
    cost {
        mana 0
        requires_reload true
        start_reloaded true
    }

    bonus_passives {
        ReloadOnTotalDamageReceived 25
    }
    
    target {
        min_range 1
        max_range 4
        max_aoe 0
    }

    damage_instance {
        damage 0
        
        effects {
            Temporary {
                status Brace
                stacks 99
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `SteelSkin2`
**Description:** Gain +99 Brace until your next turn, then disable this spell until you take a total of 15 damage.  
**Source:** `tank_abilities.gon`  

```
SteelSkin2 {
    variant_of SteelSkin

    meta {
        desc "ABILITY_STEELSKIN2_DESC"
    }
    
    cost {
        mana 0
    }

    bonus_passives {
        ReloadOnTotalDamageReceived 15
    }
}
```

---

### `FaultLine`
**Name:** Fault Line  
**Description:** Fling all units in a straight line onto nearby tiles.  
**Source:** `tank_abilities.gon`  

```
FaultLine {
    template spell

    meta {
        name "ABILITY_FAULTLINE_NAME"
        desc "ABILITY_FAULTLINE_DESC"
        class Tank
    }

    graphics {
        animation earthquakeSlam
        particle Earthquake
        delay 3
    }
    
    cost {
        mana 5
        infcantrip true
    }

    target {
        target_mode direction

        aoe_mode line
        min_aoe 1
        max_aoe 10
    }
    
    damage_instance {
        damage 2

        effects {
            TwisterDisplaceWithDamage {
                damage inherit
                max_dist 2
            }
        }

        elements [
            Earth
        ]
    }
}
```

---

### `FaultLine2`
**Description:** Fling all units in a straight line onto nearby tiles, dealing more damage.  
**Source:** `tank_abilities.gon`  

```
FaultLine2 {
    variant_of FaultLine

    meta {
        desc "ABILITY_FAULTLINE2_DESC"
    }

    damage_instance {
        damage 5
    }
}
```

---

### `Demolish`
**Name:** Demolish  
**Description:** Turn a tile into a dirt tile, smashing any inanimate objects into rocks.  
**Source:** `tank_abilities.gon`  

```
Demolish {
    template melee_attack

    meta {
        name "ABILITY_DEMOLISH_NAME"
        desc "ABILITY_DEMOLISH_DESC"
        class Tank
    }
	
    graphics {
        animation earthquakeSlam
        particle Earthquake
    }

    target {
        knockback_mode zero
    }

    cost {
        mana 3
        infcantrip true
    }

    damage_instance {
        damage 0

        effects {
            ChangeTile DirtTile
            VaporizeInanimate 1

            Conditional_Object {
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

### `Demolish2`
**Description:** Turn 3 tiles into dirt tiles, smashing any inanimate objects into rocks.  
**Source:** `tank_abilities.gon`  

```
Demolish2 {
    variant_of Demolish

    meta {
        desc "ABILITY_DEMOLISH2_DESC"
    }

    target {
        aoe_mode custom
        custom_aoe [ [1, 1], [1, 0], [1, -1] ]
    }

    damage_instance {
        effects {
            Conditional_Object {
                Conditional_HasTag {
                    tag rock
                } Else {
                    CanApplyToInanimate {
                        BreakIntoRocks SmallRock
                    }
                }
            } Else {
                Immobile 1
            }
        }
    }
}
```

---

### `FollowUpDash`
**Source:** `tank_abilities.gon`  

```
FollowUpDash { //util ability for Follow Up passive, does not need an icon
    template dash_attack

    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_attack_animation none
    }

    cost {
        mana 0
        act_points 0
        move_points 1
    }

    target { 
        max_range 10
        max_aoe 0
        aoe_restrictions must_have_line_of_sight_unpurgable
        consider_trample true
    }

    damage_instance {
        damage 0
        type none
    }
}
```

---

### `FollowUpDash2`
**Source:** `tank_abilities.gon`  

```
FollowUpDash2 {
    variant_of FollowUpDash

    graphics {
        dash_attack_animation dashatk
    }

    target { 
        max_aoe 1
    }

    damage_instance {
        damage 5+bonus_melee_damage
        type melee
    }
}
```

---

### `CatapultJump`
**Name:** Cat-A-Pult!  
**Description:** Get flung to a tile and deal damage to anything you land on.
This doesn't use up your movement action.  
**Source:** `tank_abilities.gon`  

```
CatapultJump {
    variant_of BasicJump

    meta {
        name "ABILITY_CATAPULT_NAME"
        desc "ABILITY_CATAPULT_DESC"
        animate_name false
        is_move true
    }

    cost {
        mana 0
        cantrip true
    }

    target { 
        min_range 1
        max_range 4
        aoe_excludes_self false
        restrictions []
    }
    damage_instance {
        damage 5+bonus_melee_ability_damage

        effects {
            IgnoreSelf 1
        }
    }
}
```

---

### `CatapultJump2`
**Description:** Get flung to a tile and deal damage to anything you land on.
This doesn't use up your movement action.  
**Source:** `tank_abilities.gon`  

```
CatapultJump2 {
    variant_of CatapultJump

    meta {
        desc "ABILITY_CATAPULT2_DESC"
    }

    target {
        max_range 20
    }
}
```

---

### `PushThrough`
**Name:** Push Through  
**Description:** Trample over 2 tiles in a straight line destroying any inanimate objects.  
**Source:** `tank_abilities.gon`  

```
PushThrough {
    template move
    
    meta {
        name "ABILITY_PUSHTHROUGH_NAME"
        desc "ABILITY_PUSHTHROUGH_DESC"
        class Tank
        animate_name true
    }
    
    cost {
        mana 4
        infcantrip true
    }
    
    target {
        range_mode cross
        max_range 2
        restrictions [must_move must_not_be_knockback_immune_animate_character]
        straight_shot true
    }

    temporary_effects {
        Trample 3
    }
    
    damage_instance {
        damage 3
        override_trample_damage true

        effects {
            VaporizeInanimate 1
        }
    }
}
```

---

### `PushThrough2`
**Description:** Trample over 4 tiles in a straight line destroying any inanimate objects and inflicting Bruise 1 on units you trample.  
**Source:** `tank_abilities.gon`  

```
PushThrough2 {
    variant_of PushThrough

    meta {
        desc "ABILITY_PUSHTHROUGH2_DESC"
    }

    target {
        max_range 4
    }

    damage_instance {
        effects {
            Bruise 1
        }
    }
}
```

---

### `Spur`
**Name:** Pincushion  
**Description:** Gain +3 Thorns. 
This spell uses up your movement action.  
**Source:** `tank_abilities.gon`  

```
Spur {
    template self_buff
    
    meta {
        name "ABILITY_PINCUSHION_NAME"
        desc "ABILITY_PINCUSHION_DESC"
        class Tank
    }

    cost {
        mana 0
        act_points 0
        move_points 1
        charge 0
    }

    damage_instance {
        effects {
            Thorns 3
        }
    }
}
```

---

### `Spur2`
**Description:** Gain +3 Thorns and +1 Brace.
This spell uses up your movement action.  
**Source:** `tank_abilities.gon`  

```
Spur2 {
    variant_of Spur

    meta {
        desc "ABILITY_PINCUSHION2_DESC"
    }

    damage_instance {
        effects {
            Thorns 3
            Brace 1
        }
    }
}
```

---

### `Supper`
**Name:** Supper  
**Description:** Heal 15 HP and gain -2 [img:spd].
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
Supper {
    template self_buff
    
    meta {
        name "ABILITY_SUPPER_NAME"
        desc "ABILITY_SUPPER_DESC"
        class Tank
    }

    graphics {
        animation gulp
    }
    
    cost {
        infcantrip true
        mana 0
        once_per_fight true
    }
    
    damage_instance {
        heal 15
        effects {
            SpeedUp -2
        }
    }
}
```

---

### `Supper2`
**Description:** Heal 15 HP, gain -2 [img:spd] and +5 Health Regeneration.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
Supper2 {
    variant_of Supper

    meta {
        desc "ABILITY_SUPPER2_DESC"
    }

    damage_instance {
        effects {
            HealthRegenUp 5
        }
    }
}
```

---

### `FullForce`
**Name:** Full Force  
**Description:** Deal damage equal to your [img:con] and inflict Stun. Also stuns yourself.  
**Source:** `tank_abilities.gon`  

```
FullForce {
    template jump_attack

    meta {
        name "ABILITY_FULLFORCE_NAME"
        desc "ABILITY_FULLFORCE_DESC"
        class Tank
    }

    graphics {
        jump_start_animation bellyflopStart
        air_animation bellyflop_air
        jump_attack_animation bellyflopEnd
        land_animation none
        fixed_jump_height 1
        fixed_jump_speed 2
    }

    cost {
        mana 8
        infcantrip true
    }
    
    target {
        max_range 1

        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        aoe_excludes_self false
        restrictions none
    }

    temporary_effects {
        DisableTrample 1
    }

    damage_instance {
        damage con

        effects {
            Stun 1
            Conditional_IsSelf {
                OverrideDamage 0
            } Else {
            }
        }
    }
}
```

---

### `FullForce2`
**Description:** Deal damage equal to your [img:con] and inflict Stun and Bruise 4. Also stuns yourself.  
**Source:** `tank_abilities.gon`  

```
FullForce2 {
    variant_of FullForce

    meta {
        desc "ABILITY_FULLFORCE2_DESC"
    }

    damage_instance {
        effects {
            Conditional_IsSelf {
            } Else {
                Bruise 4
            }
        }
    }
}
```

---

### `Sandstorm`
**Name:** Sandstorm  
**Description:** Start a sandstorm.
(Sandstorm deals 1 damage to all units at the end of round.)
If a sandstorm was already active, increase its damage by 1.  
**Source:** `tank_abilities.gon`  

```
Sandstorm {
    template self_buff

    meta {
        name "ABILITY_SANDSTORM_NAME"
        desc "ABILITY_SANDSTORM_DESC"
        class Tank
    }

    cost {
        mana 4
        infcantrip true
    }

    damage_instance {
        effects {
            StackingSandstorm 1
        }
    }
}
```

---

### `Sandstorm2`
**Description:** Start a sandstorm.
(Sandstorm deals 1 damage to all units at the end of round.)
If a sandstorm was already active, increase its damage by 1.
\[s:.7\](This spell costs 0 mana the first time you cast it each turn.)\[/s\]  
**Source:** `tank_abilities.gon`  

```
Sandstorm2 {
    variant_of Sandstorm

    meta {
        desc "ABILITY_SANDSTORM2_DESC"
    }

    cost {
        mana 4
    }
    bonus_passives {
        FreeFirstCast 4
    }
}
```

---

### `Thicken`
**Name:** Thicken  
**Description:** Gain +1 knockback damage and +1 knockback range until the end of the turn.  
**Source:** `tank_abilities.gon`  

```
Thicken {
    template self_buff

    meta {
        name "ABILITY_THICKEN_NAME"
        desc "ABILITY_THICKEN_DESC"
        class Tank
    }

    graphics {
		animation gulp
    }

    cost {
        mana 2
        infcantrip true
    }

    damage_instance {
        effects {
            TempBonusKnockback 1
            TempBonusKnockbackDamage 1
        }
    }
}
```

---

### `Thicken2`
**Description:** Gain +1 [img:con].
Gain +1 knockback damage and +1 knockback range until the end of the turn.  
**Source:** `tank_abilities.gon`  

```
Thicken2 {
    variant_of Thicken

    meta {
        desc "ABILITY_THICKEN2_DESC"
    }

    damage_instance {
        effects {
            ConstitutionUp 1
        }
    }
}
```

---

## File: `thief_abilities.gon`

### `Assassinate`
**Name:** Assassinate  
**Description:** A melee attack that can only hit from behind. This attack ignores shield and has 50% crit chance.  
**Source:** `thief_abilities.gon`  

```
Assassinate {
    template melee_spell
    class AOESpellAbility //its a melee attack but I want a spell effect animation
    
    meta {
        name "ABILITY_ASSASSINATE_NAME"
        desc "ABILITY_ASSASSINATE_DESC"
        class Thief
    }

    graphics {
        animation attack
        particle Slash
        darken_screen true
        darken_screen_exclude_characters_on_tile true
        darken_screen_exclude_self true
        darken_screen_start_early true
        delay 0
    }

    sounds {
        oncast AbilitySnd_Assassinate
    }

    cost {
        infcantrip true
        mana 8
    }

    target {
        restrictions [aoe_must_exist]
        aoe_restrictions [must_backstab]
    }
    
    damage_instance {
        type melee
        damage 10+bonus_melee_ability_damage
        crit_chance 50%
        piercing true
        incidentally_collects_pickups true
    }
}
```

---

### `Assassinate2`
**Description:** A melee attack that can only hit from behind. This attack ignores shield and has 100% crit chance.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
Assassinate2 {
    variant_of Assassinate

    meta {
        desc "ABILITY_ASSASSINATE2_DESC"
    }

    cost {
        mana 6
    }

    damage_instance {
        damage 10+bonus_melee_ability_damage
        crit_chance 100%
    }
}
```

---

### `BoostBackstab`
**Name:** Boost Backstab  
**Description:** Until end of turn, your backstabs do +75% more damage and ignore shield.  
**Source:** `thief_abilities.gon`  

```
BoostBackstab {
    template self_buff
    
    meta {
        name "ABILITY_BOOSTBACKSTAB_NAME"
        desc "ABILITY_BOOSTBACKSTAB_DESC"
        class Thief
    }

    graphics {
		animation tailwag
		particle fx_statup
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            TempBackstab 75
            TempBackstabPiercing 1
        }
    }
}
```

---

### `BoostBackstab2`
**Description:** Until end of turn, your backstabs do +75% more damage, ignore shield, and inflict Bleed and Poison.  
**Source:** `thief_abilities.gon`  

```
BoostBackstab2 {
    variant_of BoostBackstab

    meta {
        desc "ABILITY_BOOSTBACKSTAB2_DESC"
    }

    damage_instance {
        effects {
            TempBackstabBleed 1
            TempBackstabPoison 1
        }
    }
}
```

---

### `PoisonGas`
**Name:** Poison Gas  
**Description:** Inflict Poison 2 on all units adjacent to you.  
**Source:** `thief_abilities.gon`  

```
PoisonGas {
    template spell

    meta {
        name "ABILITY_POISONGAS_NAME"
        desc "ABILITY_POISONGAS_DESC"
        class Thief
    }

    graphics {
        particle PoisonPoof
		animation runincircles
    }
    
    cost {
        infcantrip true
        mana 4
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

### `PoisonGas2`
**Description:** Inflict Poison 4 on all units adjacent to you (even diagonally).  
**Source:** `thief_abilities.gon`  

```
PoisonGas2 {
    variant_of PoisonGas

    meta {
        desc "ABILITY_POISONGAS2_DESC"
    }

    target {
        aoe_mode square
    }
	
    damage_instance {
        effects {
            Poison 4
        }
    }

}
```

---

### `PoisonNail`
**Name:** Poison Nail  
**Description:** Throw a nail that inflicts Poison and ignores shield.  
**Source:** `thief_abilities.gon`  

```
PoisonNail {
    template straightshot_attack
    
    meta {
        name "ABILITY_POISONNAIL_NAME"
        desc "ABILITY_POISONNAIL_DESC"
        class Thief
    }

    graphics {
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 3+bonus_range
    }

    damage_instance {
        damage 1+bonus_ranged_damage
        piercing true
        effects {
            Poison 1
        }
    }
}
```

---

### `PoisonNail2`
**Description:** Throw 2 nails that inflict Poison and ignore shield.  
**Source:** `thief_abilities.gon`  

```
PoisonNail2 {
    variant_of PoisonNail

    meta {
        desc "ABILITY_POISONNAIL2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `WeakeningNail`
**Name:** Weakening Nail  
**Description:** Throw a nail that inflicts Weakness and ignores shield.  
**Source:** `thief_abilities.gon`  

```
WeakeningNail {
    template straightshot_attack
    
    meta {
        name "ABILITY_WEAKENINGNAIL_NAME"
        desc "ABILITY_WEAKENINGNAIL_DESC"
        class Thief
    }

    graphics {
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 3+bonus_range
    }
    
    damage_instance {
        damage 1+bonus_ranged_damage
        piercing true
        effects {
            Weakness 1
        }
    }
}
```

---

### `WeakeningNail2`
**Description:** Throw 2 nails that inflict Weakness and ignore shield.  
**Source:** `thief_abilities.gon`  

```
WeakeningNail2 {
    variant_of WeakeningNail

    meta {
        desc "ABILITY_WEAKENINGNAIL2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `SharpNail`
**Name:** Sharp Nail  
**Description:** Throw a nail that inflicts Bleed and ignores shield.  
**Source:** `thief_abilities.gon`  

```
SharpNail {
    template straightshot_attack
    
    meta {
        name "ABILITY_SHARPNAIL_NAME"
        desc "ABILITY_SHARPNAIL_DESC"
        class Thief
    }

    graphics {
		projectile knifeprojectile
		animation throwobject
    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 3+bonus_range
    }
    
    damage_instance {
        damage 1+bonus_ranged_damage
        piercing true
        effects {
            Bleed 1
        }
    }
}
```

---

### `SharpNail2`
**Description:** Throw 2 nails that inflict Bleed and ignore shield.  
**Source:** `thief_abilities.gon`  

```
SharpNail2 {
    variant_of SharpNail

    meta {
        desc "ABILITY_SHARPNAIL2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `Double`
**Name:** Double  
**Description:** -  
**Source:** `thief_abilities.gon`  

```
Double { //CUT
    template self_buff
    
    meta {
        name "ABILITY_DOUBLE_NAME"
        desc "ABILITY_DOUBLE_DESC"
        class Thief
    }

    graphics {
        animation jitter
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    damage_instance {
        effects {
            DoubleCast 1
        }
    }
}
```

---

### `Double2`
**Description:** -  
**Source:** `thief_abilities.gon`  

```
Double2 {
    variant_of Double

    meta {
        desc "ABILITY_DOUBLE2_DESC"
    }

    cost {
        mana 6
    }
}
```

---

### `CoinToss`
**Name:** Coin Toss  
**Description:** Throw a coin that deals damage.
RELOAD: Collect a coin.
[s:.7]This spell costs more mana each additional time you use it on the same turn.\[/s\]  
**Source:** `thief_abilities.gon`  

```
CoinToss {
    template straightshot_attack
    
    meta {
        name "ABILITY_COINTOSS_NAME"
        desc "ABILITY_COINTOSS_DESC"
        class Thief
    }

    graphics {
        animation invthrow
        projectile CoinProjectile
    }

    cost {
        requires_reload true
        mana X
        coins 1
    }

    target {
        max_aoe 5
        X_is this_ability_storm_count
    }

    bonus_passives {
        ReloadOnGainCoins 1
    }

    damage_instance {
        damage 10+bonus_ranged_damage

        effects {
            CoinTossBounce X
        }
    }
}
```

---

### `CoinToss2`
**Description:** Throw a coin at infinite range with +50% crit chance that ignores shield.
RELOAD: Collect a coin.
[s:.7]This spell costs more mana each additional time you use it on the same turn.\[/s\]  
**Source:** `thief_abilities.gon`  

```
CoinToss2 {
    variant_of CoinToss

    meta {
        desc "ABILITY_COINTOSS2_DESC"
    }

    target {
        max_aoe 10
    }

    damage_instance {
        crit_chance 50%
        piercing true
    }
}
```

---

### `MoveAgain`
**Name:** Move Again  
**Description:** Refresh your movement action.  
**Source:** `thief_abilities.gon`  

```
MoveAgain { //TODO: disable ability until you are actually out of move points
    template self_buff
    
    meta {
        name "ABILITY_MOVEAGAIN_NAME"
        desc "ABILITY_MOVEAGAIN_DESC"
        class Thief
        type_icon "movement"
    }

    graphics {
		animation hopinplace
    }
    
    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        effects {
            RefreshMovePoints 1
        }
    }
}
```

---

### `MoveAgain2`
**Description:** Refresh your movement action.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
MoveAgain2 {
    variant_of MoveAgain

    meta {
        desc "ABILITY_MOVEAGAIN2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `AttackAgain`
**Name:** Rearm  
**Description:** Refresh your basic attack.  
**Source:** `thief_abilities.gon`  

```
AttackAgain { //TODO: disable ability until you are actually out of act points
    template self_buff
    
    meta {
        name "ABILITY_REARM_NAME"
        desc "ABILITY_REARM_DESC"
        class Thief
        type_icon "melee"
    }

    graphics {
	animation celebrate
    }
    
    cost {
        infcantrip true
        mana 7
    }

    damage_instance {
        effects {
            RefreshActPoints 1
        }
    }
}
```

---

### `AttackAgain2`
**Description:** Refresh your basic attack.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
AttackAgain2 {
    variant_of AttackAgain

    meta {
        desc "ABILITY_REARM2_DESC"
    }

    cost {
        mana 5
    }
}
```

---

### `Camouflage`
**Name:** Camouflage  
**Description:** Gain Stealth.  
**Source:** `thief_abilities.gon`  

```
Camouflage { //CUT
    template self_buff
    
    meta {
        name "ABILITY_CAMOFLAUGE_NAME"
        desc "ABILITY_CAMOFLAUGE_DESC"
        class Thief
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            Stealth 1
        }
    }
}
```

---

### `Camouflage2`
**Description:** Gain Stealth. Attacking while stealthed has a 100% critical hit chance.  
**Source:** `thief_abilities.gon`  

```
Camouflage2 {
    variant_of Camouflage

    meta {
        desc "ABILITY_CAMOFLAUGE2_DESC"
    }

    damage_instance {
        effects {
            Stealth 1
            StealthCritChance 100
        }
    }
}
```

---

### `Shadow`
**Name:** Shadow  
**Description:** Teleport behind a unit.
[s:.7]Nothin' personnel, kid.\[/s\]  
**Source:** `thief_abilities.gon`  

```
Shadow {
    template teleport
    
    meta {
        name "ABILITY_SHADOW_NAME"
        desc "ABILITY_SHADOW_DESC"
        animate_name true
        class Thief
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 4

        restrictions [must_be_moveable must_be_directly_behind_character]
    }
}
```

---

### `Shadow2`
**Description:** Teleport behind a unit. Your next action has +100% crit chance.
[s:.7]Nothin' personnel, kid.\[/s\]  
**Source:** `thief_abilities.gon`  

```
Shadow2 {
    variant_of Shadow

    meta {
        desc "ABILITY_SHADOW2_DESC"
    }

    target {
        max_range 6
    }

    self_damage {
        effects {
            TempCritChanceUp 100
        }
    }
}
```

---

### `TimeWalk`
**Name:** Time Walk  
**Description:** Take an extra turn at the end of the round.
\[s:.7\](This spell can't be cast on extra turns.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
TimeWalk {
    template self_buff
    
    meta {
        name "ABILITY_TIMEWALK_NAME"
        desc "ABILITY_TIMEWALK_DESC"
        class Thief
        type_icon "misc"
    }

    graphics {
        animation doublevision
    }
    
    cost {
        infcantrip true
        mana 10
        main_turn_only true
    }
    
    damage_instance {
        effects {
            TakeExtraTurnEndOfRound 1
        }
    }
}
```

---

### `TimeWalk2`
**Description:** Take an extra turn at the end of the round.
\[s:.7\](This spell can't be cast on extra turns. This spell costs less.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
TimeWalk2 {
    variant_of TimeWalk

    meta {
        desc "ABILITY_TIMEWALK2_DESC"
    }

    cost {
        mana 7
    }
}
```

---

### `DoubleLoot`
**Name:** Double Loot  
**Description:** -  
**Source:** `thief_abilities.gon`  

```
DoubleLoot { //CUT
    template self_buff
    
    meta {
        name "ABILITY_DOUBLELOOT_NAME"
        desc "ABILITY_DOUBLELOOT_DESC"
        class Thief
        type_icon "misc"
    }

    graphics {
        animation jitter
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            DoubleLoot 1
        }
    }
}
```

---

### `DoubleLoot2`
**Description:** -  
**Source:** `thief_abilities.gon`  

```
DoubleLoot2 {
    variant_of DoubleLoot

    meta {
        desc "ABILITY_DOUBLELOOT2_DESC"
    }

    damage_instance {
        effects {
            DoubleLoot 2
        }
    }
}
```

---

### `Distract`
**Name:** Distract  
**Description:** Make a unit face away from you.  
**Source:** `thief_abilities.gon`  

```
Distract {
    template spell

    meta {
        name "ABILITY_DISTRACT_NAME"
        desc "ABILITY_DISTRACT_DESC"
        class Thief
        type_icon "misc"
    }

    graphics {
		particle none
		animation pointout
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    target {
        max_aoe 0
        max_range 4
        min_range 1

        knockback_mode character_to_tile_4snap
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

### `Distract2`
**Description:** Make any unit look away from you. This has a 33% chance to inflict Confusion.  
**Source:** `thief_abilities.gon`  

```
Distract2 {
    variant_of Distract

    meta {
        desc "ABILITY_DISTRACT2_DESC"
    }

    target {
        max_range 6
    }

    damage_instance {
        effects {
            Confusion [1 .33]
        }
    }
}
```

---

### `Rebound`
**Name:** Rebound  
**Description:** A melee attack that rebounds you backwards 10 tiles.  
**Source:** `thief_abilities.gon`  

```
Rebound {
    template melee_attack

    meta {
        name "ABILITY_REBOUND_NAME"
        desc "ABILITY_REBOUND_DESC"
        class Thief
    }

    graphics {
		animation bigkick
    }

    cost {
        mana 3
        infcantrip true
    }

    target {
        restrictions [aoe_must_exist]
        aoe_restrictions [must_have_character]
        knockback_mode orientation
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
    }
    self_damage {
        damage 0
        type melee
        knockback -10

        effects {
            OverrideKnockbackDamage 2
            KnockbackDamageImmuneUntilSettled 1
        }
    }
}
```

---

### `Rebound2`
**Description:** A melee attack that rebounds you backwards 10 tiles. Deal damage to any unit you collide with.  
**Source:** `thief_abilities.gon`  

```
Rebound2 {
    variant_of Rebound

    meta {
        desc "ABILITY_REBOUND2_DESC"
    }

    self_damage {
        effects {
            OverrideKnockbackDamage "max(5+bonus_melee_ability_damage, 1)"
        }
    }
}
```

---

### `CutPurse`
**Name:** Cut Purse  
**Description:** Throw a nail that knocks coins out of units it hits and ignores shield.  
**Source:** `thief_abilities.gon`  

```
CutPurse {
    template straightshot_attack
    
    meta {
        name "ABILITY_CUTPURSE_NAME"
        desc "ABILITY_CUTPURSE_DESC"
        class Thief
    }

    graphics {
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        max_aoe 3+bonus_range
    }

    damage_instance {
        damage 1+bonus_ranged_damage
        piercing true
        effects {
            KnockOutCoin 1
        }
    }
}
```

---

### `CutPurse2`
**Description:** Throw 2 nails that knock coins out of units they hit and ignore shield.  
**Source:** `thief_abilities.gon`  

```
CutPurse2 {
    variant_of CutPurse

    meta {
        desc "ABILITY_CUTPURSE2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `EagleEye`
**Name:** Eagle Eye  
**Description:** Spawn 2-3 coins on random tiles.  
**Source:** `thief_abilities.gon`  

```
EagleEye {
    template spawn

    meta {
        name "ABILITY_EAGLEEYE_NAME"
        desc "ABILITY_EAGLEEYE_DESC"
        class Thief
        type_icon "misc"
    }
    
    graphics {
        lob false
    }
    
    cost {
        mana 4
        infcantrip true
    }
    
    target {
        target_mode none
        aoe_mode square
        max_aoe 20
        min_targets 2
        max_targets 3
        aoe_restrictions [must_be_empty]
    }

    spawn {
        object Coin
        layer pickups
    }
}
```

---

### `EagleEye2`
**Description:** Spawn 3-7 coins on random tiles.  
**Source:** `thief_abilities.gon`  

```
EagleEye2 {
    variant_of EagleEye

    meta {
        desc "ABILITY_EAGLEEYE2_DESC"
    }

    target {
        min_targets 3
        max_targets 7
    }
}
```

---

### `PickPocket`
**Name:** Pickpocket  
**Description:** Steal 1-3 coins from a unit and give it -1 Damage.  
**Source:** `thief_abilities.gon`  

```
PickPocket {
    template melee_attack

    meta {
        name "ABILITY_PICKPOCKET_NAME"
        desc "ABILITY_PICKPOCKET_DESC"
        class Thief
    }

    graphics {
    }

    cost {
        mana 3
        infcantrip true
    }

    damage_instance {
        damage 0

        effects {
            BurgleCoin 1
            BurgleCoin [1 .5]
            BurgleCoin [1 .5]
            DamageUp -1
        }
    }
}
```

---

### `PickPocket2`
**Description:** Steal 3-5 coins from a unit, give it -1 Damage, and apply some extra debuffs at random.  
**Source:** `thief_abilities.gon`  

```
PickPocket2 {
    variant_of PickPocket

    keyword_tooltips {DamageUp -1}

    meta {
        desc "ABILITY_PICKPOCKET2_DESC"
    }

    damage_instance {
        effects {
            BurgleCoin 3
            Poison [1 .2]
            Bleed [1 .2]
            Weakness [1 .2]
            Bruise [1 .2]
            Burn [1 .2]
            Slow [1 .2]
        }
    }
}
```

---

### `Backflip`
**Name:** Backflip  
**Description:** Backflip out of the way the next time you're targeted by an enemy.  
**Source:** `thief_abilities.gon`  

```
Backflip {
    template self_buff
    
    meta {
        name "ABILITY_BACKFLIP_NAME"
        desc "ABILITY_BACKFLIP_DESC"
        class Thief
        type_icon "defense"
    }

    graphics {
		animation backflipLoop
    }

    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            BackflipWhenTargeted {
                stacks 1
                ability BackflipDodge
            }
        }
    }
}
```

---

### `Backflip2`
**Description:** Backflip out of the way the next time you're targeted by an enemy.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
Backflip2 {
    variant_of Backflip

    meta {
        desc "ABILITY_BACKFLIP2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `BackflipDodge`
**Source:** `thief_abilities.gon`  

```
BackflipDodge {
    template move

    graphics {
        sync_speed 17
        max_tiles_single_loop 5
        ignore_slowtiles true
        move_start_animation backflipStart
        animation backflipLoop
        move_end_animation backflipEnd
        dont_orient true
    }

    target {
        range_mode cross
        max_range 1
        restrictions [must_be_moveable must_move]
        straight_shot true
        allow_any_orientation true
    }
}
```

---

### `Blur`
**Name:** Blur  
**Description:** Gain +10% dodge chance.
Disable this spell if you have more than 65% dodge chance.  
**Source:** `thief_abilities.gon`  

```
Blur {
    template self_buff
    
    meta {
        name "ABILITY_BLUR_NAME"
        desc "ABILITY_BLUR_DESC"
        class Thief
        type_icon "defense"
    }

    graphics {
        animation hopinplace
    }

    cost {
        infcantrip true
        mana 4
        cant_cast X-65
    }

    bonus_passives {
        XIsCountStatusStacks DodgeChance_Status
    }

    target {
        X_is custom
    }
    
    damage_instance {
        effects {
            DodgeChance_Status 10
        }
    }
}
```

---

### `Blur2`
**Description:** Gain +15% dodge chance. 
Disable this spell if you have more than 80% dodge chance.  
**Source:** `thief_abilities.gon`  

```
Blur2 {
    variant_of Blur

    meta {
        desc "ABILITY_BLUR2_DESC"
    }

    cost {
        cant_cast X-75
    }

    damage_instance {
        effects {
            DodgeChance_Status 15
        }
    }
}
```

---

### `GreedStep`
**Name:** Greedstep  
**Description:** Teleport to a tile with coins on it.  
**Source:** `thief_abilities.gon`  

```
GreedStep {
    template teleport
    
    meta {
        name "ABILITY_GREEDSTEP_NAME"
        desc "ABILITY_GREEDSTEP_DESC"
        animate_name true
        class Thief
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 20
        restrictions [must_be_moveable must_have_tag]
        target_requires_tag money
    }
}
```

---

### `GreedStep2`
**Description:** Teleport to a tile with coins on it, then spawn 1-2 coins on random tiles.  
**Source:** `thief_abilities.gon`  

```
GreedStep2 {
    variant_of GreedStep

    meta {
        desc "ABILITY_GREEDSTEP2_DESC"
    }

    self_damage {
        effects {
            SpawnCoinAnywhere 1
            SpawnCoinAnywhere [1 .5]
        }
    }
}
```

---

### `Stalk`
**Name:** Stalk  
**Description:** Target any enemy. Teleport behind it at the start of your next turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
Stalk {
    template teleport
    
    meta {
        name "ABILITY_STALK_NAME"
        desc "ABILITY_STALK_DESC"
        animate_name true
        class Thief
    }

    graphics {
		prime_animation angry
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        cantrip true
        mana 3
    }

    target {
        max_range 20
        track_target true
        delayed_trigger true
        adjust_target stalk

        restrictions [must_have_enemy]
    }
}
```

---

### `Stalk2`
**Description:** Target any enemy. Teleport behind it at the start of your next turn.
\[s:.7\](Castable once per turn. Costs 0 mana.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
Stalk2 {
    variant_of Stalk

    meta {
        desc "ABILITY_STALK2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `NailFlurry`
**Name:** Nail Flurry  
**Description:** Throw 10 1-damage nails that ignore shield.  
**Source:** `thief_abilities.gon`  

```
NailFlurry {
    template straightshot_attack
    
    meta {
        name "ABILITY_NAILFLURRY_NAME"
        desc "ABILITY_NAILFLURRY_DESC"
        class Thief
    }

    graphics {
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 10
    }

    target {
        max_aoe 10
    }

    temporary_effects {
        CastAgain 9
    }
    
    damage_instance {
        damage 1
        piercing true
    }
}
```

---

### `NailFlurry2`
**Description:** Throw 10 1-damage nails that ignore shield. Throw extra nails equal to your [img:dex].  
**Source:** `thief_abilities.gon`  

```
NailFlurry2 {
    variant_of NailFlurry

    meta {
        desc "ABILITY_NAILFLURRY2_DESC"
    }

    target {
        X_is custom
    }

    bonus_passives {
        XIsFormulaLockedUntilComplete dex
    }

    temporary_effects {
        CastAgain 9+X
    }
}
```

---

### `Declaw`
**Name:** Declaw  
**Description:** A melee attack that inflicts -1 Damage and Bleed.  
**Source:** `thief_abilities.gon`  

```
Declaw {
    template melee_attack

    meta {
        name "ABILITY_DECLAW_NAME"
        desc "ABILITY_DECLAW_DESC"
        class Thief
    }

    graphics {
        animation sliceOpen
    }

    cost {
        mana 3
        infcantrip true
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage

        effects {
            Bleed 1
            DamageUp -1
        }
    }
}
```

---

### `Declaw2`
**Description:** A 2-hit melee attack that inflicts -1 Damage and Bleed.  
**Source:** `thief_abilities.gon`  

```
Declaw2 {
    variant_of Declaw

    meta {
        desc "ABILITY_DECLAW2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `QuickRoll`
**Name:** Quick Roll  
**Description:** Roll in a straight line up to three tiles.
RELOAD: Backstab a unit.  
**Source:** `thief_abilities.gon`  

```
QuickRoll {
    template move
    
    meta {
        name "ABILITY_QUICKROLL_NAME"
        desc "ABILITY_QUICKROLL_DESC"
        class Thief
        animate_name true
    }
    
    graphics {
        sync_speed 22
        max_tiles_single_loop 5
        ignore_slowtiles true
        move_start_animation startroll
        animation roll
        move_end_animation endroll
    }

    cost {
        requires_reload true
        mana 0
    }

    bonus_passives {
        ReloadOnBackstab 1
    }

    target {
        range_mode cross
        max_range 3
        restrictions [must_be_moveable must_move]
        straight_shot true
    }
}
```

---

### `QuickRoll2`
**Description:** Roll in a straight or diagonal line up to five tiles.
RELOAD: Backstab a unit.  
**Source:** `thief_abilities.gon`  

```
QuickRoll2 {
    variant_of QuickRoll

    meta {
        desc "ABILITY_QUICKROLL2_DESC"
    }

    target {
        range_mode 8cross
        max_range 5
        allow_diagonals true
    }
}
```

---

### `Slice`
**Name:** Slice  
**Description:** A melee attack that has all effects of your basic attack and ignores shield.  
**Source:** `thief_abilities.gon`  

```
Slice {
    template melee_attack

    meta {
        name "ABILITY_SLICE_NAME"
        desc "ABILITY_SLICE_DESC"
        class Thief
    }

    graphics {
        animation sliceOpen
    }

    cost {
        mana 6
        infcantrip true
    }

    bonus_passives {
        CopyBasicAttackEffects 1
    }

    damage_instance {
        damage 5+bonus_melee_ability_damage
        piercing true
    }
}
```

---

### `Slice2`
**Description:** A melee attack that has all effects of your basic attack and ignores shield.
\[s:.7\](This spell is free the 1st time you use it each turn.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
Slice2 {
    variant_of Slice

    meta {
        desc "ABILITY_SLICE2_DESC"
    }

    cost {
        mana 6
    }
    bonus_passives {
        FreeFirstCast 1
    }
}
```

---

### `PocketSand`
**Name:** Pocket Sand  
**Description:** Inflict Blind on all units in a small cone.  
**Source:** `thief_abilities.gon`  

```
PocketSand {
    template spell
	
    graphics {
		delay 4
	    particle fx_sandBlows
		animation kicksand
    }

    meta {
        name "ABILITY_POCKETSAND_NAME"
        desc "ABILITY_POCKETSAND_DESC"
        class Thief
    }

    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        target_mode direction

        aoe_mode cone
        min_aoe 1
        max_aoe 2

        aoe_considers_character_size true
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 0
        type status_spell
		
        elements [
            Wind
        ]
		
        effects {
            Blind 1
        }
    }
}
```

---

### `PocketSand2`
**Description:** Inflict Blind 2 on all units in a larger cone.  
**Source:** `thief_abilities.gon`  

```
PocketSand2 {
    variant_of PocketSand

    meta {
        desc "ABILITY_POCKETSAND2_DESC"
    }

    target {
        max_aoe 3
    }

    damage_instance {
        effects {
            Blind 2
        }
    }
}
```

---

### `Nightshade`
**Name:** Nightshade  
**Description:** Inflict Poison 4 on an adjacent unit.  
**Source:** `thief_abilities.gon`  

```
Nightshade {
    template melee_spell
    
    meta {
        name "ABILITY_NIGHTSHADE_NAME"
        desc "ABILITY_NIGHTSHADE_DESC"
        class Thief
    }

    graphics {
		affected_particle PoisonPoof
		animation swatupatk
    }

    cost {
        infcantrip true
        mana 7
    }

    damage_instance {
        damage 0
        type melee

        effects {
            Poison 4
        }
    }
}
```

---

### `Nightshade2`
**Description:** Inflict Poison 4 on an adjacent unit.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
Nightshade2 {
    variant_of Nightshade

    meta {
        desc "ABILITY_NIGHTSHADE2_DESC"
    }

    cost {
        mana 5
    }
}
```

---

### `Shadowshift`
**Name:** Shadow Shift  
**Description:** Teleport exactly 2 tiles away, leaving behind a shadow that mimics your basic attack.
\[s:.7\](The shadow fades at the end of your turn.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
Shadowshift {
    template teleport
    
    meta {
        name "ABILITY_SHADOWSHIFT_NAME"
        desc "ABILITY_SHADOWSHIFT_DESC"
        animate_name true
        class Thief
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 5
    }

    temporary_effects {
        AfterImage {
            object PlayerCat_ThiefShade
            skilltemp true
        }
    }

    target {
        max_range 2
        min_range 2
    }
}
```

---

### `Shadowshift2`
**Description:** Teleport up to 3 tiles away, leaving behind a shadow that mimics your basic attack.
\[s:.7\](The shadow fades at the end of your turn.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
Shadowshift2 {
    variant_of Shadowshift

    meta {
        desc "ABILITY_SHADOWSHIFT2_DESC"
    }

    target {
        max_range 3
        min_range 1
    }
}
```

---

### `SlingShade`
**Name:** Slingshade  
**Description:** Spawn a shadow up to 3 tiles away that mimics your basic attack.
\[s:.7\](The shadow fades at the end of your turn.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
SlingShade {
    template spawn

    meta {
        name "ABILITY_SLINGSHADE_NAME"
        desc "ABILITY_SLINGSHADE_DESC"
        class Thief
    }

    tags [summon]
    
    graphics {
        lob false
        animation shoot
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        min_range 1
        max_range 3
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object PlayerCat_ThiefShade
        faction self

        catdata clone
        clone_items true
    }
}
```

---

### `SlingShade2`
**Description:** Spawn a shadow up to 5 tiles away that mimics your basic attack.
\[s:.7\](The shadow fades at the end of your turn.)\[/s\]
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
SlingShade2 {
    variant_of SlingShade

    meta {
        desc "ABILITY_SLINGSHADE2_DESC"
    }

    target {
        max_range 5
    }

    cost {
        mana 4
    }
}
```

---

### `Caltrops`
**Name:** Caltrops  
**Description:** Move up to 4 tiles, spreading glass shards on the tiles you walk through.  
**Source:** `thief_abilities.gon`  

```
Caltrops {
    template move
    
    meta {
        name "ABILITY_CALTROPS_NAME"
        desc "ABILITY_CALTROPS_DESC"
        animate_name true
        class Thief
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 4
    }

    temporary_effects {
        TileTrail GlassTile
    }
}
```

---

### `Caltrops2`
**Description:** Move up to 10 tiles, spreading glass shards on the tiles you walk through.  
**Source:** `thief_abilities.gon`  

```
Caltrops2 {
    variant_of Caltrops
    
    meta {
        desc "ABILITY_CALTROPS2_DESC"
    }

    target {
        max_range 10
    }
}
```

---

### `PierceShot`
**Name:** Pierce Shot  
**Description:** Throw a nail that passes through units and ignores shield.  
**Source:** `thief_abilities.gon`  

```
PierceShot {
    template straightshot_attack
    
    meta {
        name "ABILITY_PIERCESHOT_NAME"
        desc "ABILITY_PIERCESHOT_DESC"
        class Thief
    }

    graphics {
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        max_aoe 3+bonus_range
        upgrade_straight_shot_to_piercing true
    }
    
    damage_instance {
        damage 3+bonus_ranged_damage
        piercing true
    }
}
```

---

### `PierceShot2`
**Description:** Throw an infinite range nail that passes through units and ignores shield.  
**Source:** `thief_abilities.gon`  

```
PierceShot2 {
    variant_of PierceShot

    meta {
        desc "ABILITY_PIERCESHOT2_DESC"
    }

    target {
        max_aoe 10+bonus_range
    }
}
```

---

### `Cheat`
**Name:** Cheat  
**Description:** Gain temporary +5 [img:lck] until your next turn.  
**Source:** `thief_abilities.gon`  

```
Cheat {
    template self_buff
    
    meta {
        name "ABILITY_CHEAT_NAME"
        desc "ABILITY_CHEAT_DESC"
        class Thief
    }

    graphics {
        animation cheat
    }

    cost {
        mana 5
        infcantrip true
    }

    damage_instance {
        damage 0

        effects {
            Temporary {
                status LuckUp
                stacks 5
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `Cheat2`
**Description:** Gain temporary +10 [img:lck] until your next turn.  
**Source:** `thief_abilities.gon`  

```
Cheat2 {
    variant_of Cheat

    meta {
        desc "ABILITY_CHEAT2_DESC"
    }

    damage_instance {
        damage 0

        effects {
            Temporary {
                status LuckUp
                stacks 10
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `VenomBarrage`
**Name:** Venom Barrage  
**Description:** Throw a nail that inflicts Poison 1 and ignores shield at each enemy in your line of sight.  
**Source:** `thief_abilities.gon`  

```
VenomBarrage {
    template ranged_attack
    
    meta {
        name "ABILITY_VENOMBARRAGE_NAME"
        desc "ABILITY_VENOMBARRAGE_DESC"
        class Thief
    }

    graphics {
        animation throwobject
        projectile SpikeProjectile
        lob_height 0
        speed 20
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        target_mode none
        max_aoe 20
        aoe_restrictions [must_have_line_of_sight enemies_only]
    }
    
    damage_instance {
        damage 1+bonus_ranged_damage
        piercing true
        effects {
            Poison 1
        }
    }
}
```

---

### `VenomBarrage2`
**Description:** Throw 2 nails that inflict Poison 1 and ignore shield at each enemy in your line of sight.  
**Source:** `thief_abilities.gon`  

```
VenomBarrage2 {
    variant_of VenomBarrage

    meta {
        desc "ABILITY_VENOMBARRAGE2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `LootCorpse`
**Name:** Loot Corpse  
**Description:** Loot 1-3 coins from a body... and possibly something else?
\[s:.7\](This might destroy the body)\[/s\]  
**Source:** `thief_abilities.gon`  

```
LootCorpse {
    template melee_attack
    
    meta {
        name "ABILITY_LOOTCORPSE_NAME"
        desc "ABILITY_LOOTCORPSE_DESC"
        class Thief
        type_icon "misc"
    }

    graphics {
        animation pickpocket
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        aoe_restrictions must_have_corpse
        restrictions aoe_must_exist
    }

    damage_instance {
        damage 0
        type melee
        incidentally_collects_pickups false

        effects {
            VaporizeCorpseFlipAdvantage [1 .33]
            ApplyToSource {
                GainCoinsRange {
                    min 1
                    max 3
                }
                FindItemFromPool {
                    pool chapter
                    chance .02
                }
            }
        }
    }
}
```

---

### `LootCorpse2`
**Description:** Loot 1-3 coins from a body... and possibly something else?
\[s:.7\](This might not destroy the body)\[/s\]
\[s:.7\](Your chance of finding "something else" is significantly increased.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
LootCorpse2 {
    variant_of LootCorpse
    
    meta {
        desc "ABILITY_LOOTCORPSE2_DESC"
    }

    damage_instance {
        effects {
            ApplyToSource {
                FindItemFromPool {
                    chance .15
                }
            }
        }
    }
}
```

---

### `SeverArtery`
**Name:** Sever Artery  
**Description:** A weak melee attack. If this crits, inflict Bleed 5.  
**Source:** `thief_abilities.gon`  

```
SeverArtery {
    template melee_attack

    meta {
        name "ABILITY_SEVERARTERY_NAME"
        desc "ABILITY_SEVERARTERY_DESC"
        class Thief
    }

    graphics {
        animation sliceOpen
    }

    cost {
        mana 4
        infcantrip true
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage

        effects {
            ApplyStatusIfCrit {
                Bleed 5
            }
        }
    }
}
```

---

### `SeverArtery2`
**Description:** A weak melee attack. If this crits inflict Bleed 5 and you gain All Stats Up.  
**Source:** `thief_abilities.gon`  

```
SeverArtery2 {
    variant_of SeverArtery
    
    meta {
        desc "ABILITY_SEVERARTERY2_DESC"
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage

        effects {
            ApplyStatusIfCrit {
                Bleed 5

                ApplyToSource {
                    AllStatsUp 1
                }
            }
        }
    }
}
```

---

### `Fade`
**Name:** Fade  
**Description:** Gain Stealth 1.  
**Source:** `thief_abilities.gon`  

```
Fade {
    template self_buff
    
    meta {
        name "ABILITY_FADE_NAME"
        desc "ABILITY_FADE_DESC"
        class Thief
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 10
    }
    
    damage_instance {
        effects {
            Stealth 1
        }
    }
}
```

---

### `Fade2`
**Description:** Gain Stealth 2.  
**Source:** `thief_abilities.gon`  

```
Fade2 {
    variant_of Fade

    meta {
        desc "ABILITY_FADE2_DESC"
    }

    damage_instance {
        effects {
            Stealth 2
        }
    }
}
```

---

### `SharpenNail`
**Name:** Sharpen Nail  
**Description:** Gain +1 [img:dex] and +1 Range until the end of the battle.  
**Source:** `thief_abilities.gon`  

```
SharpenNail {
    template self_buff
    
    meta {
        name "ABILITY_SHARPENNAIL_NAME"
        desc "ABILITY_SHARPENNAIL_DESC"
        class Thief
    }

    graphics {
		particle fx_statup
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            DexterityUp 1
            RangeUp 1
        }
    }
}
```

---

### `SharpenNail2`
**Description:** Gain +1 [img:dex] and +1 Range until the end of the battle.
[s:.7]Automatically cast this spell at the end of each round for free.\[/s\]  
**Source:** `thief_abilities.gon`  

```
SharpenNail2 {
    variant_of SharpenNail

    meta {
        desc "ABILITY_SHARPENNAIL2_DESC"
    }

    bonus_passives {
        AutocastEachRound {
            ability SharpenNail2
        }
    }
}
```

---

### `SneakUp`
**Name:** Sneak Up  
**Description:** Teleport directly behind a random enemy.  
**Source:** `thief_abilities.gon`  

```
SneakUp {
    template teleport
    
    meta {
        name "ABILITY_SNEAKUP_NAME"
        desc "ABILITY_SNEAKUP_DESC"
        animate_name true
        class Thief
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        target_mode random_tile
        max_range 20
        restrictions [must_be_moveable must_be_directly_behind_enemy]
    }
}
```

---

### `SneakUp2`
**Description:** Teleport directly behind a random enemy.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
SneakUp2 {
    variant_of SneakUp

    meta {
        desc "ABILITY_SNEAKUP2_DESC"
    }

    cost {
        mana 2
    }
}
```

---

### `Shank`
**Name:** Shank  
**Description:** An attack that hits 2 times from behind.  
**Source:** `thief_abilities.gon`  

```
Shank { //alt basic attack for Shank passive
    template melee_attack
    
    meta {
        name "ABILITY_SHANKALT_NAME"
        desc "ABILITY_SHANKALT_DESC"
        animate_name false
    }

    graphics {
        animation doubleswat
    }

    target { 
        max_aoe 1+bonus_melee_range
        aoe_restrictions [must_have_line_of_sight_unpurgable enemies_only must_backstab]
        restrictions aoe_must_exist
        multihit 2
    }
}
```

---

### `Shank2`
**Description:** An attack that hits 3 times from behind.  
**Source:** `thief_abilities.gon`  

```
Shank2 {
    variant_of Shank

    meta {
        desc "ABILITY_SHANKALT2_DESC"
    }

    target { 
        multihit 3
    }
}
```

---

### `StealKidney`
**Name:** Steal Kidney  
**Description:** A melee attack with increased critical hit chance. If this crits and your trinket slot is empty, gain a kidney, then inflict Bleed 1.  
**Source:** `thief_abilities.gon`  

```
StealKidney {
    template melee_attack

    meta {
        name "ABILITY_STEALKIDNEY_NAME"
        desc "ABILITY_STEALKIDNEY_DESC"
        class Thief
    }

    graphics {
        animation sliceOpen
    }

    cost {
        mana 4
        infcantrip true
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage
        crit_chance 20%

        effects {
            ApplyStatusIfCrit {
                ApplyToSource {
                    EquipPermanentItem Kidney
                }
                Bleed 1
            }
        }
    }
}
```

---

### `StealKidney2`
**Description:** A melee attack with increased critical hit chance that inflicts Bleed and Bruise 1. If this crits and your trinket slot is empty, gain a kidney, then inflict Bleed 1.  
**Source:** `thief_abilities.gon`  

```
StealKidney2 {
    variant_of StealKidney

    meta {
        desc "ABILITY_STEALKIDNEY2_DESC"
    }

    damage_instance {
        effects {
            Bleed 1
            Bruise 1
        }
    }
}
```

---

### `StealLuck`
**Name:** Steal Luck  
**Description:** A weak melee attack. If this crits, inflict -1 [img:lck] and you gain +1 [img:lck].  
**Source:** `thief_abilities.gon`  

```
StealLuck {
    template melee_attack

    meta {
        name "ABILITY_STEALLUCK_NAME"
        desc "ABILITY_STEALLUCK_DESC"
        class Thief
    }

    graphics {
    }

    cost {
        mana 3
        infcantrip true
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage

        effects {
            ApplyStatusIfCrit {
                LuckUp -1
                ApplyToSource {
                    LuckUp 1
                }
            }
        }
    }
}
```

---

### `StealLuck2`
**Name:** Steal Luck  
**Description:** A weak melee attack that inflicts -1 [img:lck] and you gain +1 [img:lck].  
**Source:** `thief_abilities.gon`  

```
StealLuck2 {
    template melee_attack

    meta {
        name "ABILITY_STEALLUCK_NAME"
        desc "ABILITY_STEALLUCK2_DESC"
        class Thief
    }

    graphics {
    }

    cost {
        mana 3
        infcantrip true
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage

        effects {
            LuckUp -1
            ApplyToSource {
                LuckUp 1
            }
        }
    }
}
```

---

### `ThiefSwap`
**Name:** Over Here, Over There  
**Description:** Swap positions with an ally. Swap back at the end of your turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
ThiefSwap {
    template swap
    
    meta {
        name "ABILITY_THIEFSWAP_NAME"
        desc "ABILITY_THIEFSWAP_DESC"
        animate_name true
        class Thief
    }

    graphics {
        animation_in shadowStepIn
        animation_out shadowStepOut
    }

    cost {
        mana 0
        cantrip true
    }

    target {
        max_range 20
        restrictions [must_be_swappable aoe_must_exist]
        aoe_restrictions [allies_only]
    }

    damage_instance {
        effects {
            SourceSwapsBackEndOfTurn ThiefSwapBack
        }
    }
}
```

---

### `ThiefSwap2`
**Description:** Swap positions with any unit. Swap back at the end of your turn. If the unit was an enemy, inflict Confusion 1.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
ThiefSwap2 {
    variant_of ThiefSwap
    
    meta {
        desc "ABILITY_THIEFSWAP2_DESC"
    }

    target {
        aoe_restrictions none
    }

    damage_instance {
        effects {
            Conditional_Enemy {
                Confusion 1
            }
        }
    }
}
```

---

### `ThiefSwapBack`
**Source:** `thief_abilities.gon`  

```
ThiefSwapBack { //util ability for ThiefSwap, does not need an icon
    template swap

    graphics {
        animation_in shadowStepIn
        animation_out shadowStepOut
    }

    target {
        max_range 20
        restrictions [must_be_swappable aoe_must_exist]
    }
}
```

---

### `Pierce`
**Name:** Pierce  
**Description:** Gain +2 Range. Your attacks pass through units and ignore shield for the rest of the turn.  
**Source:** `thief_abilities.gon`  

```
Pierce {
    template self_buff
    
    meta {
        name "ABILITY_PIERCE_NAME"
        desc "ABILITY_PIERCE_DESC"
        class Thief
    }

    graphics {
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            TempPenetrate 1
            TempRangeUp 2
        }
    }
}
```

---

### `Pierce2`
**Description:** Gain +4 Range. Your attacks pass through units and ignore shield for the rest of the turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
Pierce2 {
    variant_of Pierce

    meta {
        desc "ABILITY_PIERCE2_DESC"
    }
    
    cost {
        mana 2
    }
    
    damage_instance {
        effects {
            TempRangeUp 4
        }
    }
}
```

---

### `WindUp`
**Name:** Wind Up  
**Description:** Gain +1 Range for the rest of the turn.  
**Source:** `thief_abilities.gon`  

```
WindUp {
    template self_buff
    
    meta {
        name "ABILITY_WINDUP_NAME"
        desc "ABILITY_WINDUP_DESC"
        class Thief
    }

    graphics {
        animation hopinplace
	    particle fx_statup
    }
    
    cost {
        infcantrip true
        mana 1
    }
    
    damage_instance {
        effects {
            TempRangeUp 1
        }
    }
}
```

---

### `WindUp2`
**Description:** Gain +1 Range.  
**Source:** `thief_abilities.gon`  

```
WindUp2 {
    variant_of WindUp
    
    meta {
        desc "ABILITY_WINDUP2_DESC"
    }

    damage_instance {
        effects {
            RangeUp 1
        }
    }
}
```

---

### `TripleNails`
**Name:** Triple Nails  
**Description:** Throw 3 nails straight and diagonally in front of you. These nails have the effects of your basic attack and ignore shield.  
**Source:** `thief_abilities.gon`  

```
TripleNails {
    template straightshot_attack
    
    meta {
        name "ABILITY_TRIPLENAILS_NAME"
        desc "ABILITY_TRIPLENAILS_DESC"
        class Thief
    }

    graphics {
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 10

        aoe_mode custom
        custom_aoe [[1, 1] [1, 0] [1,-1]]
    }

    bonus_passives {
        CopyBasicAttackEffects 1
    }
    
    damage_instance {
        damage 1+bonus_ranged_damage
        piercing true
    }
}
```

---

### `TripleNails2`
**Description:** Throw 3 nails straight and diagonally in front of you 2 times. These nails have the effects of your basic attack and ignore shield.  
**Source:** `thief_abilities.gon`  

```
TripleNails2 {
    variant_of TripleNails

    meta {
        desc "ABILITY_TRIPLENAILS2_DESC"
    }

    temporary_effects {
        CastAgain 1
    }
}
```

---

### `SkinDisguise`
**Name:** Skin Disguise  
**Description:** Destroy an adjacent body. Enemies won't attack you until your next turn.
\[s:.7\](Castable once per turn.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
SkinDisguise {
    template targeted_status
    
    meta {
        name "ABILITY_SKINDISGUISE_NAME"
        desc "ABILITY_SKINDISGUISE_DESC"
        class Thief
        type_icon "misc"
    }

    graphics {
        animation sliceOpen
    }

    cost {
        cantrip true
        mana 3
    }

    target {
        aoe_restrictions [must_have_destructible_corpse enemies_only]
        restrictions aoe_must_exist

        max_range 1
        min_range 1
    }

    damage_instance {
        damage 0
        type melee
        incidentally_collects_pickups false

        effects {
            FactionDisguiseSource 1
            VaporizeCorpse 1
        }
    }
}
```

---

### `SkinDisguise2`
**Description:** Destroy a body in range 3. Enemies won't attack you until your next turn.
\[s:.7\](This spell is free. Castable once per turn.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
SkinDisguise2 {
    variant_of SkinDisguise

    meta {
        desc "ABILITY_SKINDISGUISE2_DESC"
    }

    cost {
        mana 0
    }
    target {
        max_range 3
    }
}
```

---

### `Chakram`
**Name:** Chakram  
**Description:** Throw a projectile that passes through units and then returns to you. This can collect pickups.  
**Source:** `thief_abilities.gon`  

```
Chakram {
    template straightshot_attack
    
    meta {
        name "ABILITY_CHAKRAM_NAME"
        desc "ABILITY_CHAKRAM_DESC"
        class Thief
    }

    graphics {
        animation throwobject
        speed 10
        projectile ChakramProjectile
        use_rotation false
    }
    
    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 3+bonus_range
        upgrade_straight_shot_to_piercing true
        upgrade_straight_shot_to_boomerang true
    }

    bonus_passives {
        CatchBoomerang 1
    }

    damage_instance {
        damage 1+bonus_ranged_damage

        effects {
            CollectsPickups 1
        }
    }
}
```

---

### `Chakram2`
**Description:** Throw a projectile that passes through units and then returns to you. At its apex, it deals increased damage and always crits. This can collect pickups.  
**Source:** `thief_abilities.gon`  

```
Chakram2 {
    variant_of Chakram

    meta {
        desc "ABILITY_CHAKRAM2_DESC"
    }

    splash_damage {
        damage 4+bonus_ranged_damage

        crit_chance 100
        effects {
            CollectsPickups 1
        }
    }
}
```

---

### `Jitter`
**Name:** Jitter  
**Description:** Inflict Confusion 1 on each adjacent unit.  
**Source:** `thief_abilities.gon`  

```
Jitter {
    template spell

    meta {
        name "ABILITY_JITTER_NAME"
        desc "ABILITY_JITTER_DESC"
        class Thief
    }

    graphics {
        particle none
        animation hopinplace
    }
    
    cost {
        infcantrip true
        mana 3
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

        effects {
            Confusion 1
        }
    }
}
```

---

### `Jitter2`
**Description:** Inflict Confusion 1 on each unit within 3 tiles of you.  
**Source:** `thief_abilities.gon`  

```
Jitter2 {
    variant_of Jitter

    meta {
        desc "ABILITY_JITTER2_DESC"
    }

    target {
        max_aoe 3
    }
}
```

---

### `StealTime`
**Name:** Steal Time  
**Description:** A melee attack. If this crits, refresh your basic attack and movement actions.  
**Source:** `thief_abilities.gon`  

```
StealTime {
    template melee_attack

    meta {
        name "ABILITY_STEALTIME_NAME"
        desc "ABILITY_STEALTIME_DESC"
        class Thief
    }

    graphics {
    }

    cost {
        mana 4
        infcantrip true
    }

    damage_instance {
        damage 1+bonus_melee_ability_damage

        effects {
            ApplyStatusIfCrit {
                ApplyToSource {
                    RefreshActPoints 1
                    RefreshMovePoints 1
                }
            }
        }
    }
}
```

---

### `StealTime2`
**Description:** A melee attack with +30% crit chance. If this crits, refresh your basic attack and movement actions.  
**Source:** `thief_abilities.gon`  

```
StealTime2 {
    variant_of StealTime

    meta {
        desc "ABILITY_STEALTIME2_DESC"
    }

    damage_instance {
        crit_chance 30%
    }
}
```

---

### `Outskirts`
**Name:** Outskirts  
**Description:** Teleport to a tile on the edge of the map.  
**Source:** `thief_abilities.gon`  

```
Outskirts {
    template teleport
    
    meta {
        name "ABILITY_OUTSKIRTS_NAME"
        desc "ABILITY_OUTSKIRTS_DESC"
        animate_name true
        class Thief
    }

    graphics {
        animation_out shadowStepOut
        animation_in shadowStepIn
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        range_mode map_edges
    }
}
```

---

### `Outskirts2`
**Description:** Teleport to a tile on the edge of the map. Gain +2 Damage for the rest of the turn.  
**Source:** `thief_abilities.gon`  

```
Outskirts2 {
    variant_of Outskirts

    meta {
        desc "ABILITY_OUTSKIRTS2_DESC"
    }

    self_damage {
        effects {
            TempDamageUp 2
        }
    }
}
```

---

### `PoisonDip`
**Name:** Poison Dip  
**Description:** Spend all your mana. For every 5 mana spent, your basic attack inflicts +1 Poison.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
PoisonDip {
    template self_buff

    meta {
        name "ABILITY_POISONDIP_NAME"
        desc "ABILITY_POISONDIP_DESC"
        class Thief
    }

    cost {
        infcantrip true
        
        mana X
        cant_cast 5-X //effectively makes the ability uncastable until you have 5+ mana

        X_cant_be_zero true
        disallow_cost_modification true
        once_per_fight true
    }

    target {
        X_is current_mana
    }
    
    damage_instance {
        damage 0

        effects {
            PoisonLace "X/5" 
        }
    }
}
```

---

### `PoisonDip2`
**Description:** Spend all your mana. For every 3 mana spent, your basic attack inflicts +1 Poison.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `thief_abilities.gon`  

```
PoisonDip2 {
    variant_of PoisonDip

    meta {
        desc "ABILITY_POISONDIP2_DESC"
    }

    cost {
        cant_cast 3-X
    }

    damage_instance {
        effects {
            PoisonLace "X/3" 
        }
    }
}
```

---

### `LuckyPenny`
**Name:** Lucky Penny  
**Description:** Collect an adjacent pickup and gain +2 [img:lck] instead of its normal effects.  
**Source:** `thief_abilities.gon`  

```
LuckyPenny {
    template targeted_status
    
    meta {
        name "ABILITY_LUCKYPENNY_NAME"
        desc "ABILITY_LUCKYPENNY_DESC"
        class Thief
        type_icon "misc"
    }

    graphics {
		animation coinFlip
    }

    cost {
        infcantrip true
        mana 1
    }
    
    target {
        max_range 1

        restrictions must_have_tag
        target_requires_tag pickup
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            CollectsPickupsWithAltEffects {
                LuckUp 2
            }
        }
    }
}
```

---

### `LuckyPenny2`
**Description:** Collect a pickup within four tiles of you. Gain +2 [img:lck] instead of its normal effects.  
**Source:** `thief_abilities.gon`  

```
LuckyPenny2 {
    variant_of LuckyPenny

    meta {
        desc "ABILITY_LUCKYPENNY2_DESC"
    }

    target {
        max_range 4
    }
}
```

---

## File: `tinkerer_abilities.gon`

### `Research`
**Name:** Research  
**Description:** Gain +1 Tech.  
**Source:** `tinkerer_abilities.gon`  

```
Research {
    template self_buff
    
    meta {
        name "ABILITY_RESEARCH_NAME"
        desc "ABILITY_RESEARCH_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {
		animation idea
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            Tech 1
        }
    }
}
```

---

### `Research2`
**Description:** Gain +1 Tech.
Bonus Passive: Crafting subtracts 1 Tech instead of all of it.  
**Source:** `tinkerer_abilities.gon`  

```
Research2 {
    variant_of Research

    meta {
        desc "ABILITY_RESEARCH2_DESC"
    }

    bonus_passives {
        CapTechSpent 1
    }

    damage_instance {
        effects {
            Tech 1
        }
    }
}
```

---

### `Discharge`
**Name:** Discharge  
**Description:** Spend all of your mana, then deal that much electric damage to an adjacent unit.  
**Source:** `tinkerer_abilities.gon`  

```
Discharge {
    template spell

    meta {
        name "ABILITY_DISCHARGE_NAME"
        desc "ABILITY_DISCHARGE_DESC"
        class Tinkerer
        type_icon "magic"
    }

    graphics {
        particle WaterConduct
		animation tapatk
    }
    
    cost {
        mana X
        infcantrip true
        X_cant_be_zero true
        disallow_cost_modification true
    }

    target {
        max_aoe 0
        max_range 1
        min_range 1
        X_is current_mana
    }
    
    damage_instance {
        damage X

        elements [
            Electric
        ]
    }
}
```

---

### `Discharge2`
**Description:** Spend all of your mana, then deal that much electric damage to an adjacent unit with a 10% Stun chance for each point of mana spent.  
**Source:** `tinkerer_abilities.gon`  

```
Discharge2 {
    variant_of Discharge

    meta {
        desc "ABILITY_DISCHARGE2_DESC"
    }

    damage_instance {
        effects {
            Stun [1 X*.1]
        }
    }
}
```

---

### `Repair`
**Name:** Repair  
**Description:** Repair 1 use to all of your or an adjacent unit's equipment.  
**Source:** `tinkerer_abilities.gon`  

```
Repair {
    template spell

    meta {
        name "ABILITY_REPAIR_NAME"
        desc "ABILITY_REPAIR_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {
        animation tinkerAdjacent
        //animation tinkerSelf
        //TODO: switch animation depending on target
		particle none

    }
    
    cost {
        mana 5
        infcantrip true
    }

    target {
        max_aoe 0
        max_range 1
        min_range 0
    }
    
    damage_instance {
        damage 0
        type status_spell
        cant_miss true

        effects {
            RepairAll 1
            RepairAllCondition 1
        }
    }
}
```

---

### `Repair2`
**Description:** Repair all uses to all of your or an adjacent unit's equipment.  
**Source:** `tinkerer_abilities.gon`  

```
Repair2 {
    variant_of Repair

    meta {
        desc "ABILITY_REPAIR2_DESC"
    }

    damage_instance {
        effects {
            RepairAll 10
        }
    }
}
```

---

### `ShoddyJetpack`
**Name:** Shoddy Jetpack  
**Description:** Fly to a random tile in a large area. If you land on a unit, explode dealing 5 damage in an area (including to yourself).  
**Source:** `tinkerer_abilities.gon`  

```
ShoddyJetpack {
    template jump_attack

    meta {
        name "ABILITY_SHODDYJETPACK_NAME"
        desc "ABILITY_SHODDYJETPACK_DESC"
        class Tinkerer
        type_icon "movement"
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 6
        infcantrip true
    }
    
    target {
        max_range 20

        aoe_mode occupied_tiles
        aoe_excludes_self false
        restrictions none

        randomize_target_within_range 3
    }

    damage_instance {
        damage 0
        type none
        cant_miss true

        effects {
            IgnoreSelf true
            ExplosionIfHitSomething 5
        }
    }
}
```

---

### `ShoddyJetpack2`
**Description:** Fly to any tile. If you land on a unit, explode dealing 5 damage in an area (including to yourself).  
**Source:** `tinkerer_abilities.gon`  

```
ShoddyJetpack2 {
    variant_of ShoddyJetpack

    meta {
        desc "ABILITY_SHODDYJETPACK2_DESC"
    }

    target {
        randomize_target_within_range 0
    }
}
```

---

### `SpawnDecoy`
**Name:** Spawn Decoy  
**Description:** Spawn a decoy that explodes when it dies.  
**Source:** `tinkerer_abilities.gon`  

```
SpawnDecoy {
    template spawn

    meta {
        name "ABILITY_SPAWNDECOY_NAME"
        desc "ABILITY_SPAWNDECOY_DESC"
        class Tinkerer
        type_icon "defense"
    }

    tags [summon]
    
    graphics {
        lob true
        animation tinker
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        min_range 1
        max_range 3
    }

    spawn {
        object ExplodingDecoy
    }
}
```

---

### `SpawnDecoy2`
**Description:** Spawn a decoy that explodes when it dies. When an enemy targets you, swap places with the decoy.  
**Source:** `tinkerer_abilities.gon`  

```
SpawnDecoy2 {
    variant_of SpawnDecoy

    meta {
        desc "ABILITY_SPAWNDECOY2_DESC"
    }

    self_damage {
        effects {
            DecoySwapper 1
        }
    }

    spawn {
        object ExplodingDecoy
    }
}
```

---

### `DecoySwap`
**Source:** `tinkerer_abilities.gon`  

```
DecoySwap {
    template swap

    graphics {
    }

    cost {
        mana 5
        infcantrip true
    }

    target {
        max_range 20
    }
}
```

---

### `DecoyExplode`
**Source:** `tinkerer_abilities.gon`  

```
DecoyExplode {
    template spell

    graphics { 
        dont_orient true
        particle Explosion
    }
    
    cost {
        mana 0
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

### `Switcheroo`
**Name:** Switcheroo  
**Description:** Your next attack breaks your weapon, then craft a new one.  
**Source:** `tinkerer_abilities.gon`  

```
Switcheroo { //CUT
    template self_buff
    
    meta {
        name "ABILITY_SWITCHEROO_NAME"
        desc "ABILITY_SWITCHEROO_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {
		animation idea
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    damage_instance {
        effects {
            Switcheroo 1
        }
    }
}
```

---

### `Switcheroo2`
**Description:** Your next attack breaks your weapon, then gain +1 Tech and craft a weapon.  
**Source:** `tinkerer_abilities.gon`  

```
Switcheroo2 {
    variant_of Switcheroo

    meta {
        desc "ABILITY_SWITCHEROO2_DESC"
    }

    damage_instance {
        effects {
            Tech 1
        }
    }
}
```

---

### `SpringShoes`
**Name:** Spring Shoes  
**Description:** Jump up to 2 tiles away.  
**Source:** `tinkerer_abilities.gon`  

```
SpringShoes {
    template jump_attack

    meta {
        name "ABILITY_SPRINGSHOES_NAME"
        desc "ABILITY_SPRINGSHOES_DESC"
        class Tinkerer
        type_icon "movement"
    }

    graphics {
        jump_attack_animation land
    }

    cost {
        mana 2
        infcantrip true
    }
    
    target { 
        target_mode tile

        min_range 1
        max_range 2
        
        aoe_mode occupied_tiles
        min_aoe 0
        max_aoe 0
        
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

### `SpringShoes2`
**Description:** Jump up to 5 tiles away.  
**Source:** `tinkerer_abilities.gon`  

```
SpringShoes2 {
    variant_of SpringShoes

    meta {
        desc "ABILITY_SPRINGSHOES2_DESC"
    }

    target {
        max_range 5
    }
}
```

---

### `Flamethrower`
**Name:** Flamethrower  
**Description:** Shoot a flame that inflicts Burn.  
**Source:** `tinkerer_abilities.gon`  

```
Flamethrower { //used as Deathbot's basic attack
    template spell

    meta {
        name "ABILITY_FLAMETHROWER_NAME"
        desc "ABILITY_FLAMETHROWER_DESC"
    }

    graphics {
        animation attack
        particle FireBlastSmall
        delay 10
        palette 6
    }
    
    cost {
        move_points 0
        act_points 1
    }
    
    target {
        target_mode direction
        aoe_mode line
        
        max_aoe 3
        
        aoe_considers_character_size true
        aoe_excludes_self true
        knockback_mode character_to_tile
    }
    
    damage_instance {
        damage 5
        
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

### `TurretShot`
**Source:** `tinkerer_abilities.gon`  

```
TurretShot { //used as Turret's basic attack
    template lobbed_attack
    
    target {
        min_range 1
        max_range 6
    }

    damage_instance {
        damage 3+bonus_ranged_damage
    }
}
```

---

### `RocketTurretShot`
**Source:** `tinkerer_abilities.gon`  

```
RocketTurretShot { //used as Rocket Turret's basic attack
    template spell

    target {
        min_range 1
        max_range 6

        min_aoe 0
        max_aoe 1
    }

    graphics {
        animation shoot
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

### `AutoPilot`
**Name:** Autopilot  
**Description:** Take an extra turn after this one. You are AI controlled on that turn.  
**Source:** `tinkerer_abilities.gon`  

```
AutoPilot {
    template self_buff
    
    meta {
        name "ABILITY_AUTOPILOT_NAME"
        desc "ABILITY_AUTOPILOT_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 10
    }
    
    damage_instance {
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

### `AutoPilot2`
**Description:** You or another unit takes an extra turn after this one. That unit is AI controlled on that turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
AutoPilot2 {
    variant_of AutoPilot

    meta {
        desc "ABILITY_AUTOPILOT2_DESC"
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        target_mode tile
        min_range 0
        max_range 4
    }
}
```

---

### `Recycle`
**Name:** Recycle  
**Description:** Destroy your weapon to gain +1 Tech and refresh your basic action.  
**Source:** `tinkerer_abilities.gon`  

```
Recycle {
    template self_buff
    
    meta {
        name "ABILITY_RECYCLE_NAME"
        desc "ABILITY_RECYCLE_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {
		animation idea
    }
    
    cost {
        infcantrip true
        mana 5
        requires_destructible_weapon true
    }

    bonus_passives {
        DownRankAIIfWeaponUsable .001
    }
    
    damage_instance {
        effects {
            DestroyWeapon 1
            Tech 1
            RefreshActPoints 1
        }
    }
}
```

---

### `Recycle2`
**Description:** Destroy your weapon to gain +1 Tech and refresh your basic action. This spell costs 1 mana if you haven't used your weapon this turn.  
**Source:** `tinkerer_abilities.gon`  

```
Recycle2 {
    variant_of Recycle

    meta {
        desc "ABILITY_RECYCLE2_DESC"
    }

    cost {
        mana X
    }
    target {
        X_is custom
    }
    bonus_passives {
        XIsRecycleCostReduction 5
    }
}
```

---

### `BuildTurret`
**Name:** Build Turret  
**Description:** Summon a turret.  
**Source:** `tinkerer_abilities.gon`  

```
BuildTurret {
    template spawn

    meta {
        name "ABILITY_BUILDTURRET_NAME"
        desc "ABILITY_BUILDTURRET_DESC"
        class Tinkerer
    }

    tags [summon]
    
    graphics {
        lob true
        animation buildRobot//Projectile
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object TinkererTurret
    }
}
```

---

### `BuildTurret2`
**Description:** Summon a rocket turret.  
**Source:** `tinkerer_abilities.gon`  

```
BuildTurret2 {
    variant_of BuildTurret

    meta {
        desc "ABILITY_BUILDTURRET2_DESC"
    }

    spawn {
        object RocketTurret
    }
}
```

---

### `RocketSkates`
**Name:** Rocket Skates  
**Description:** Dash forward in a straight line then explode dealing damage in an area (including to yourself).  
**Source:** `tinkerer_abilities.gon`  

```
RocketSkates {
    template dash_attack
    
    meta {
        name "ABILITY_ROCKETSKATES_NAME"
        desc "ABILITY_ROCKETSKATES_DESC"
        class Tinkerer
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        //dash_end_animation dashend
        dash_attack_animation none
    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    target {
        aoe_mode standard
        min_aoe 0
        max_aoe 1
        knockback_mode character_to_tile
        aoe_excludes_self false
    }
    
    damage_instance {
        damage 5
        knockback 1
        type spell
        incidentally_collects_pickups false

        effects {
            VisualFXTile Explosion
        }

        elements [
            Explosion
            Fire
        ]
    }
}
```

---

### `RocketSkates2`
**Description:** Dash forward in a straight line then explode dealing damage in an larger area (including to yourself).  
**Source:** `tinkerer_abilities.gon`  

```
RocketSkates2 {
    variant_of RocketSkates

    meta {
        desc "ABILITY_ROCKETSKATES2_DESC"
    }

    target {
        max_aoe 2
    }
}
```

---

### `RocketSkates_Bombchu`
**Name:** Bombchu Dash  
**Description:** Dash forward in a straight line then explode.  
**Source:** `tinkerer_abilities.gon`  

```
RocketSkates_Bombchu {
    template dash_attack
    
    meta {
        name "ABILITY_BOMBCHUDASH_NAME"
        desc "ABILITY_BOMBCHUDASH_DESC"
        animate_name false
    }
    
    graphics {
        dash_start_animation dashstart
        dash_animation dash
        dash_attack_animation none
    }
    
    cost {
        mana 5
    }
    
    target {
        aoe_mode standard
        min_aoe 0
        max_aoe 1
        knockback_mode character_to_tile
        aoe_excludes_self false
    }

    self_damage {
        effects {
            Vaporize 1
        }
    }
    
    damage_instance {
        damage 5
        knockback 1
        type spell
        incidentally_collects_pickups false

        effects {
            VisualFXTile Explosion
        }

        elements [
            Explosion
            Fire
        ]
    }
}
```

---

### `DrillDown`
**Name:** Drill Down  
**Description:** Dig to an open tile in a straight line.  
**Source:** `tinkerer_abilities.gon`  

```
DrillDown {
    template teleport
    
    meta {
        name "ABILITY_DRILLDOWN_NAME"
        desc "ABILITY_DRILLDOWN_DESC"
        animate_name true
        class Tinkerer
    }

    graphics {
        animation_out digDown
        animation_in digUp
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        range_mode cross
        max_range 10
    }
}
```

---

### `DrillDown2`
**Description:** Dig to a tile in a straight line. If you dig into a unit, explode dealing 5 damage in an area (including to yourself).  
**Source:** `tinkerer_abilities.gon`  

```
DrillDown2 {
    variant_of DrillDown

    meta {
        desc "ABILITY_DRILLDOWN2_DESC"
    }

    target {
        restrictions [aoe_must_be_displaceable]
    }

    damage_instance {
        makes_contact true

        effects {
            IgnoreSelf 1
            ExplosionIfHitSomething 5
        }
    }
}
```

---

### `ArmorUp`
**Name:** Armor Up  
**Description:** Craft a Tinkerer armor piece into one of your empty armor slots.  
**Source:** `tinkerer_abilities.gon`  

```
ArmorUp {
    template self_buff
    
    meta {
        name "ABILITY_ARMORUP_NAME"
        desc "ABILITY_ARMORUP_DESC"
        class Tinkerer
        type_icon "defense"
    }

    graphics {
		animation tinkerSelf
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            Craft {
                pool tinkerer_default
                slot random_empty_armor
            }
        }
    }
}
```

---

### `ArmorUp2`
**Description:** Craft a Tinkerer armor piece into one of your or an adjacent unit's empty armor slots.  
**Source:** `tinkerer_abilities.gon`  

```
ArmorUp2 {
    variant_of ArmorUp

    meta {
        desc "ABILITY_ARMORUP2_DESC"
    }

    target {
        target_mode tile
        min_range 0
        max_range 1
    }
}
```

---

### `FreshOffTheForge`
**Name:** Fresh off the Forge  
**Description:** Gain +7 [img:shield] and Burn 3.  
**Source:** `tinkerer_abilities.gon`  

```
FreshOffTheForge {
    template self_buff
    
    meta {
        name "ABILITY_FRESHOFFTHEFORGE_NAME"
        desc "ABILITY_FRESHOFFTHEFORGE_DESC"
        class Tinkerer
        type_icon "defense"
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            Shield 7
            Burn 3
        }

        elements [
            Fire
        ]
    }
}
```

---

### `FreshOffTheForge2`
**Description:** Give +7 [img:shield] and Burn 3 to yourself or an adjacent unit.  
**Source:** `tinkerer_abilities.gon`  

```
FreshOffTheForge2 {
    variant_of FreshOffTheForge

    meta {
        desc "ABILITY_FRESHOFFTHEFORGE2_DESC"
    }

    target {
        target_mode tile
        min_range 0
        max_range 1
    }
}
```

---

### `ElectricNail`
**Name:** Electric Nail  
**Description:** Summon a nail that arcs electricity to neighboring tiles whenever any unit spends mana.  
**Source:** `tinkerer_abilities.gon`  

```
ElectricNail {
    template spawn

    meta {
        name "ABILITY_ELECTRICNAIL_NAME"
        desc "ABILITY_ELECTRICNAIL_DESC"
        class Tinkerer
    }

    tags [summon]
    
    graphics {
        lob true
        animation buildRobotProjectile
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        min_range 1
        max_range 4
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object ElectricNail
    }
}
```

---

### `ElectricNail2`
**Description:** Summon a nail that arcs electricity to neighboring tiles whenever any unit spends mana.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
ElectricNail2 {
    variant_of ElectricNail

    meta {
        desc "ABILITY_ELECTRICNAIL2_DESC"
    }

    cost {
        mana 3
    }

    target {
        max_range 8
    }

    spawn {
        object ElectricNail
    }
}
```

---

### `Craft`
**Name:** Craft  
**Description:** Craft and equip a random temporary weapon.  
**Source:** `tinkerer_abilities.gon`  

```
Craft {
    template self_buff
    
    meta {
        name "ABILITY_CRAFT_NAME"
        desc "ABILITY_CRAFT_DESC"
        type_icon "misc"
        class Tinkerer
    }

    graphics {
        animation tinker
    }

    target {
        restrictions aoe_must_exist
        aoe_restrictions must_have_cat_with_empty_weapon_slot
    }

    cost {
        infcantrip true
        mana 4
    }

    damage_instance {
        damage 0

        effects {
            Craft {
                pool tinkerer_default
                slot weapon
            }
        }
        ai_base_score 9999
        custom_additional_ai_weight prefer_dont_move
    }
}
```

---

### `Craft2`
**Description:** Craft and equip a random temporary weapon for yourself or an ally in range 3 (if they have an empty weapon slot).  
**Source:** `tinkerer_abilities.gon`  

```
Craft2 {
    variant_of Craft
    
    meta {
        desc "ABILITY_CRAFT2_DESC"
    }

    target {
        target_mode tile
        max_range 3
        min_range 0
    }
}
```

---

### `Shockwave`
**Name:** Shockwave  
**Description:** Deal damage to all units. The closer a unit is to you the more damage it takes.  
**Source:** `tinkerer_abilities.gon`  

```
Shockwave {
    template spell
    
    meta {
        name "ABILITY_SHOCKWAVE_NAME"
        desc "ABILITY_SHOCKWAVE_DESC"
        class Tinkerer
    }

    graphics {
        particle WaterConduct
        animation shocking
        delay 3
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        aoe_mode all
        target_mode none
        aoe_excludes_self true
    }
    
    damage_instance {
        damage 10

        effects {
            DamageDistanceAOEFalloff 1
        }

        elements [
            Electric
            Conducted //this prevents it from conducting, since it hits everything already conduction damage is irrelevant
        ]
    }
}
```

---

### `Shockwave2`
**Description:** Deal damage to all units. The closer a unit is to you the more damage it takes.
\[s:.7\](Deals more damage to closer units and less damage to further units.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
Shockwave2 {
    variant_of Shockwave

    meta {
        desc "ABILITY_SHOCKWAVE2_DESC"
    }

    damage_instance {
        damage 15

        effects {
            DamageDistanceAOEFalloff 2
        }
    }
}
```

---

### `Math`
**Name:** Math!  
**Description:** Deal 1 damage to a unit for each unique divisor in its current HP value. If its HP was a prime number, stun it.  
**Source:** `tinkerer_abilities.gon`  

```
Math {
    template spell

    meta {
        name "ABILITY_MATH_NAME"
        desc "ABILITY_MATH_DESC"
        class Tinkerer
        type_icon magic
        icon_shell_frame attack
        icon_damage_display "?"
    }

    graphics {
        particle Bolt
		animation pointout
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        max_aoe 0
        max_range 5
    }
    
    damage_instance {
        raw_damage 0
        show_damage_on_0 true

        effects {
            Math {
                stacks 1
                Stun 1
            }
        }

        elements [
            Electric
        ]
    }
}
```

---

### `Math2`
**Description:** Deal 1 damage to a unit for each unique divisor in its current HP value. If its HP was a prime number, stun it and gain +1 Tech.  
**Source:** `tinkerer_abilities.gon`  

```
Math2 {
    variant_of Math

    meta {
        desc "ABILITY_MATH2_DESC"
    }

    damage_instance {
         effects {
            Math {
                stacks 1
                Stun 1
                ApplyToSource {
                    Tech 1
                }
            }
        }
    }
}
```

---

### `Reprogram`
**Name:** Reprogram  
**Description:** Conjure a random spell of your class as a bonus ability.  
**Source:** `tinkerer_abilities.gon`  

```
Reprogram {
    template self_buff
    
    meta {
        name "ABILITY_REPROGRAM_NAME"
        desc "ABILITY_REPROGRAM_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            ConjureBonusAbility Class
        }
    }
}
```

---

### `Reprogram2`
**Description:** Conjure a random upgraded spell of your class as a bonus ability.  
**Source:** `tinkerer_abilities.gon`  

```
Reprogram2 {
    variant_of Reprogram

    meta {
        desc "ABILITY_REPROGRAM2_DESC"
    }

    damage_instance {
        effects {
            ConjureBonusAbility {
                ability Class
                upgraded true
            }
        }
    }
}
```

---

### `Improve`
**Name:** Improve  
**Description:** Gain +1 to a random stat.  
**Source:** `tinkerer_abilities.gon`  

```
Improve {
    template self_buff
    
    meta {
        name "ABILITY_IMPROVE_NAME"
        desc "ABILITY_IMPROVE_DESC"
        class Tinkerer
        type_icon "buff"
    }

    graphics {
        animation tinkerSelf
    }
    
    cost {
        infcantrip true
        mana 2
    }
    
    damage_instance {
        effects {
            RandomStatUp 1
        }
    }
}
```

---

### `Improve2`
**Description:** You or an adjacent unit gain +1 to 2 random stats.  
**Source:** `tinkerer_abilities.gon`  

```
Improve2 {
    variant_of Improve

    meta {
        desc "ABILITY_IMPROVE2_DESC"
    }

    damage_instance {
        effects {
            RandomStatUp 2
        }
    }

    target {
        target_mode tile
        max_range 1
        min_range 0
    }
}
```

---

### `Catbot`
**Name:** Catbot  
**Description:** Spawn a Catbot and give it your current weapon.
\[s:.7\](You will not get the weapon back)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
Catbot {
    template spawn

    meta {
        name "ABILITY_CATBOT_NAME"
        desc "ABILITY_CATBOT_DESC"
        class Tinkerer
    }

    tags [summon]
    
    graphics {
        lob true
        animation tinker
    }
    
    cost {
        infcantrip true
        mana 8
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Catbot
    }
}
```

---

### `Catbot2`
**Description:** Spawn a Catbot and give it your current weapon. Gain +1 Tech and refresh your basic action.
\[s:.7\](You will not get the weapon back)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
Catbot2 {
    variant_of Catbot

    meta {
        desc "ABILITY_CATBOT2_DESC"
    }

    self_damage {
        effects {
            Tech 1
            RefreshActPoints 1
        }
    }
}
```

---

### `Bombchu`
**Name:** Bombchu  
**Description:** Spawn a Bombchu bot.  
**Source:** `tinkerer_abilities.gon`  

```
Bombchu {
    template spawn

    meta {
        name "ABILITY_BOMBCHU_NAME"
        desc "ABILITY_BOMBCHU_DESC"
        class Tinkerer
    }
    
    tags [summon]

    graphics {
        lob true
        animation buildRobot
    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object Bombchu
    }
}
```

---

### `Bombchu2`
**Description:** Spawn a Bombchu bot in range 4.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
Bombchu2 {
    variant_of Bombchu

    meta {
        desc "ABILITY_BOMBCHU2_DESC"
    }

    graphics {
        animation buildRobotProjectile
    }

    cost {
        mana 4
    }

    target {
        max_range 4
    }
}
```

---

### `RemoteDetonator`
**Name:** Remote Detonator  
**Description:** Explode a familiar, dealing 5 damage with knockback in an area.  
**Source:** `tinkerer_abilities.gon`  

```
RemoteDetonator {
    template targeted_status
    
    meta {
        name "ABILITY_REMOTEDETONATOR_NAME"
        desc "ABILITY_REMOTEDETONATOR_DESC"
        class Tinkerer
    }

    graphics {
        particle none
		animation pointout
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        max_range 20

        restrictions must_have_familiar
    }
    
    damage_instance {
        damage 0
        cant_miss true

        effects {
            ExplodeCharacter 5
        }
    }
}
```

---

### `RemoteDetonator2`
**Description:** Explode a familiar, dealing 5 damage with knockback in an area.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
RemoteDetonator2 {
    variant_of RemoteDetonator

    meta {
        desc "ABILITY_REMOTEDETONATOR2_DESC"
    }

    cost {
        mana 2
    }
}
```

---

### `ShortCircuit`
**Name:** Short Circuit  
**Description:** Deal 1 electric damage with a random amount of knockback (up to 3) to all adjacent units.  
**Source:** `tinkerer_abilities.gon`  

```
ShortCircuit {
    template spell

    meta {
        name "ABILITY_SHORTCIRCUIT_NAME"
        desc "ABILITY_SHORTCIRCUIT_DESC"
        class Tinkerer
    }

    graphics {
        particle WaterConduct
    }
    
    cost {
        infcantrip true
        mana 3
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
        knockback 0

        effects {
            RandomKnockback {
                min 1
                max 3
            }
        }

        elements [
            Electric
        ]
    }
}
```

---

### `ShortCircuit2`
**Description:** Deal 2 electric damage with a random amount of knockback (up to 10) to all adjacent units.  
**Source:** `tinkerer_abilities.gon`  

```
ShortCircuit2 {
    variant_of ShortCircuit

    meta {
        desc "ABILITY_SHORTCIRCUIT2_DESC"
    }
    damage_instance {
        damage 2

        effects {
            RandomKnockback {
                min 1
                max 10
            }
        }
    }
}
```

---

### `Electrolyze`
**Name:** Electrolyze  
**Description:** Give your weapon +3 electric damage.  
**Source:** `tinkerer_abilities.gon`  

```
Electrolyze {
    template self_buff
    
    meta {
        name "ABILITY_ELECTROLYZE_NAME"
        desc "ABILITY_ELECTROLYZE_DESC"
        class Tinkerer
        type_icon "buff"
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 5
    }
    
    damage_instance {
        effects {
            CurrentWeaponDamageUp 3
            CurrentWeaponAddElectricElement 1
        }
    }
}
```

---

### `Electrolyze2`
**Description:** Give your weapon +3 electric damage.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
Electrolyze2 {
    variant_of Electrolyze

    meta {
        desc "ABILITY_ELECTROLYZE2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `EjectButton`
**Name:** Eject Button  
**Description:** Explode and fly to a random tile at least four tiles away. This explosion damages you.  
**Source:** `tinkerer_abilities.gon`  

```
EjectButton {
    template self_buff
    
    meta {
        name "ABILITY_EJECTBUTTON_NAME"
        desc "ABILITY_EJECTBUTTON_DESC"
        class Tinkerer
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 3
    }
    
    damage_instance {
        effects {
            ExplosionIfHitSomething 5
            RandomDistanceDisplace {
                stacks 20
                min_dist 4
            }
        }
    }
}
```

---

### `EjectButton2`
**Description:** Explode and fly to a random tile at least four tiles away. This explosion damages you.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
EjectButton2 {
    variant_of EjectButton

    meta {
        desc "ABILITY_EJECTBUTTON2_DESC"
    }

    cost {
        mana 1
    }
}
```

---

### `Firecrackers`
**Name:** Firecracker  
**Description:** Throw 3 small 1-damage explosives at random tiles in an area.  
**Source:** `tinkerer_abilities.gon`  

```
Firecrackers {
    template lobbed_attack
    
    meta {
        name "ABILITY_FIRECRACKERS_NAME"
        desc "ABILITY_FIRECRACKERS_DESC"
        class Tinkerer
    }

    graphics {
        animation throwobject
		projectile Firecracker
    }

    cost {
        infcantrip true
        mana 3
    }

    target {
        max_aoe 2

        min_range 1
        max_range 5+bonus_range

        max_targets 3
        restrictions none

        can_multihit true
    }

    damage_instance {
        damage 0
        type ranged

        effects {
            SmallHitExplosion 1
        }
    }
}
```

---

### `Firecrackers2`
**Description:** Throw small 1-damage explosives at all tiles in an area.  
**Source:** `tinkerer_abilities.gon`  

```
Firecrackers2 {
    variant_of Firecrackers

    meta {
        desc "ABILITY_FIRECRACKERS2_DESC"
    }

    target {
        max_range 6+bonus_range
        max_targets -1
    }
}
```

---

### `Upgrade`
**Name:** Upgrade  
**Description:** Fully heal a familiar and give it All Stats Up.  
**Source:** `tinkerer_abilities.gon`  

```
Upgrade {
    template targeted_status
    
    meta {
        name "ABILITY_UPGRADE_NAME"
        desc "ABILITY_UPGRADE_DESC"
        class Tinkerer
    }


    graphics {
        animation sing3
    }
    
    cost {
        infcantrip true
        mana 4
    }

    target {
        min_range 0
        max_range 3
        max_aoe 0
        restrictions aoe_must_exist
        aoe_restrictions familiars_only
    }
    
    damage_instance {
        damage 0

        effects {
            AllStatsUp 1
            FullHeal 1
        }
    }
}
```

---

### `Upgrade2`
**Description:** Fully heal a familiar and give it All Stats Up and +1 [img:divineshield].  
**Source:** `tinkerer_abilities.gon`  

```
Upgrade2 {
    variant_of Upgrade
    
    meta {
        desc "ABILITY_UPGRADE2_DESC"
    }

    damage_instance {
        effects {
            AllStatsUp 1
            FullHeal 1
            DivineShield 1
        }
    }
}
```

---

### `Eureka`
**Name:** Eureka!  
**Description:** Gain +3 Tech and Madness 1.
\[s:.7\](This spell can only be cast once per battle.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
Eureka {
    template self_buff
    
    meta {
        name "ABILITY_EUREKA_NAME"
        desc "ABILITY_EUREKA_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {
		animation idea
    }
    
    cost {
        infcantrip true
        mana 5
        once_per_fight true
    }
    
    damage_instance {
        effects {
            Tech 3
            Madness {
                stacks 1
                tickdown_this_turn true
            }
        }
    }
}
```

---

### `Eureka2`
**Name:** Eureka!  
**Description:** Gain +3 Tech.
\[s:.7\](This spell can only be cast once per battle.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
Eureka2 {
    template self_buff
    
    meta {
        name "ABILITY_EUREKA_NAME"
        desc "ABILITY_EUREKA2_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 5
        once_per_fight true
    }
    
    damage_instance {
        effects {
            Tech 3
        }
    }
}
```

---

### `PunchBot`
**Name:** Punchbot  
**Description:** Spawn a Rubber Fist Bot.  
**Source:** `tinkerer_abilities.gon`  

```
PunchBot {
    template spawn

    meta {
        name "ABILITY_PUNCHBOT_NAME"
        desc "ABILITY_PUNCHBOT_DESC"
        class Tinkerer
    }
    
    tags [summon]

    graphics {
        lob true
        animation buildRobotProjectile
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        min_range 1
        max_range 2
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object RubberFistBot
    }
}
```

---

### `PunchBot2`
**Description:** Spawn a Rubber Fist Bot within a large range.  
**Source:** `tinkerer_abilities.gon`  

```
PunchBot2 {
    variant_of PunchBot

    meta {
        desc "ABILITY_PUNCHBOT2_DESC"
    }

    cost {
        mana 6
    }

    target {
        max_range 6
    }
}
```

---

### `FastHands`
**Name:** Fast Hands  
**Description:** Refresh your weapon and trinket actions (unless they gain you mana).  
**Source:** `tinkerer_abilities.gon`  

```
FastHands {
    template self_buff
    
    meta {
        name "ABILITY_FASTHANDS_NAME"
        desc "ABILITY_FASTHANDS_DESC"
        class Tinkerer
    }

    tags [noncopyable]

    graphics {
		animation thumbsup
    }
    
    cost {
        infcantrip true
        mana 8
    }

    damage_instance {
        effects {
            RefreshNonManaItemAbilities 1
        }
    }
}
```

---

### `FastHands2`
**Description:** Refresh your weapon and trinket actions (unless they gain you mana). Repair 1 use to all of your equipment.  
**Source:** `tinkerer_abilities.gon`  

```
FastHands2 {
    variant_of FastHands

    meta {
        desc "ABILITY_FASTHANDS2_DESC"
    }

    damage_instance {
        effects {
            RepairAll 1
        }
    }
}
```

---

### `MechSuitPunch`
**Name:** Mech Punch  
**Description:** Dash-punch with Knockback 3.  
**Source:** `tinkerer_abilities.gon`  

```
MechSuitPunch {
    template dash_attack

    meta {
        name "ABILITY_MECHPUNCH_NAME"
        desc "ABILITY_MECHPUNCH_DESC"
    }
    
    graphics {
        dash_start_animation ramStart
        dash_animation ramLoop
        dash_attack_animation ramEnd
        always_play_animations true
    }

    target { 
        max_range 1+bonus_range
        max_aoe 1+bonus_melee_range
    }

    damage_instance {
        damage 5+bonus_melee_damage
        knockback 3
    }
}
```

---

### `MechSuitEject`
**Name:** Eject!  
**Description:** Launch yourself out of the mech. Deal damage to units you land on and yourself.  
**Source:** `tinkerer_abilities.gon`  

```
MechSuitEject {
    template throw_attack
    
    meta {
        name "ABILITY_MECHSUITEJECT_NAME"
        desc "ABILITY_MECHSUITEJECT_DESC"
    }

    graphics {
        animation eject
    }

    cost {
        mana 3
        must_be_consuming true
        infcantrip true
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
        custom_additional_ai_weight toss_far

        effects {
            EndTurn 1
        }
        ai_base_score -999999
    }
}
```

---

### `MechSuitBarrage`
**Name:** Barrage  
**Description:** Fire the machine guns!  
**Source:** `tinkerer_abilities.gon`  

```
MechSuitBarrage {
    template straightshot_attack
    
    meta {
        name "ABILITY_MECHSUITBARRAGE_NAME"
        desc "ABILITY_MECHSUITBARRAGE_DESC"
    }

    graphics {
        projectile Bullet
        animation shoot
        speed 25
        use_origin_offsets false
    }

    cost {
        mana 5
        must_be_consuming true
        infcantrip true
    }
    
    target {
        target_mode direction
        max_aoe 10
        min_aoe 1
        multihit 6
        stagger_multihit_targets true

        aoe_mode custom
        custom_aoe      [[1  0] [1  0]  [1, 0] [1, 0]  [1, 0] [1, 0]]
        custom_aoe_util [[1, 0] [1, 1]  [1, 0] [1, 1]  [1, 0] [1, 1]]

        custom_aoe_mirror      [[1  0] [1  0]  [1, 0] [1, 0]  [1, 0] [1, 0]]
        custom_aoe_util_mirror [[1, 1] [1, 0]  [1, 1] [1, 0]  [1, 1] [1, 0]]

        mirror_custom_aoe true
    }
    
    damage_instance {
        damage 4+bonus_ranged_damage

        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `MechSuitDash`
**Name:** Thrusters  
**Description:** Dash forward and light fires in your path.  
**Source:** `tinkerer_abilities.gon`  

```
MechSuitDash {
    template trample_dash
    
    meta {
        name "ABILITY_MECHDASH_NAME"
        desc "ABILITY_MECHDASH_DESC"
    }
    
    graphics {
        dash_start_animation thrustersStart
        dash_animation thrustersLoop
        dash_end_animation thrustersEnd

        speed .5
    }
    
    cost {
        mana 5
        infcantrip true
    }

    temporary_effects {
        TileTrail FireTile
    }
    
    damage_instance {
        damage 3+bonus_melee_damage
    }
}
```

---

### `MechExplode`
**Source:** `tinkerer_abilities.gon`  

```
MechExplode {
    template throw_attack

    graphics {
        animation dying
        dont_orient true
    }

    cost {
        mana 0
        infcantrip true
    }
    
    target {
        target_mode random_tile
        min_range 5
        max_range 7
        restrictions none
        throw_consumed_character true
        allow_any_orientation true
    }

    self_damage {
        effects {
            ApplyToConsumed {
                Die 1
            }
            ExplodeCharacter_NoDie 1
        }
    }
    
    damage_instance {
        damage 5+bonus_melee_ability_damage
        blocked_damage 5+bonus_melee_ability_damage
    }
}
```

---

### `MechSuit`
**Name:** Mech Suit  
**Description:** Summon a mech suit that can be piloted.
\[s:.7\](Castable once per battle.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
MechSuit {
    template spawn

    meta {
        name "ABILITY_MECHSUIT_NAME"
        desc "ABILITY_MECHSUIT_DESC"
        class Tinkerer
    }
    
    tags [summon]

    graphics {
        lob false
        animation portout
    }
    
    cost {
        infcantrip true
        mana 15
        once_per_fight true
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

    spawn {
        object MechSuit
        size 2

        post_spawn_statuses {
            EnterMount enter
        }
    }
}
```

---

### `MechSuit2`
**Description:** Summon a mech suit that can be piloted.
\[s:.7\](Costs 0 mana. Castable once per battle.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
MechSuit2 {
    variant_of MechSuit

    meta {
        desc "ABILITY_MECHSUIT2_DESC"
    }

    cost {
        mana 0
    }
}
```

---

### `UnreliableShield`
**Name:** Unreliable Shield Generator  
**Description:** Gain +6 [img:shield] and +1 temporary Brace. This spell has a 75% chance to be disabled on each turn.  
**Source:** `tinkerer_abilities.gon`  

```
UnreliableShield {
    template self_buff
    
    meta {
        name "ABILITY_UNRELIABLESHIELD_NAME"
        desc "ABILITY_UNRELIABLESHIELD_DESC"
        class Tinkerer
        type_icon "defense"
    }

    graphics {

    }

    bonus_passives {
        AbilityEnabledPercentEachTurn 25%
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    damage_instance {
        effects {
            Shield 6
            Temporary {
                status Brace
                stacks 1
                turns 1
                expires_on_begin_turn true
            }
        }
    }
}
```

---

### `UnreliableShield2`
**Description:** Get +6 [img:shield] and +1 temporary Brace. This spell has a 66% chance to be disabled on each turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
UnreliableShield2 {
    variant_of UnreliableShield

    meta {
        desc "ABILITY_UNRELIABLESHIELD2_DESC"
    }

    bonus_passives {
        AbilityEnabledPercentEachTurn 33%
    }

    cost {
        mana 3
    }
}
```

---

### `UnreliableMissile`
**Name:** Unreliable Missile Launcher  
**Description:** Shoot an explosive homing missile at a random enemy. This spell has a 75% chance to be disabled on each turn.  
**Source:** `tinkerer_abilities.gon`  

```
UnreliableMissile {
    template spell
    
    meta {
        name "ABILITY_UNRELIABLEMISSILE_NAME"
        desc "ABILITY_UNRELIABLEMISSILE_DESC"
        class Tinkerer
    }

    graphics {
        use_projectile true
        projectile Projectile_Rocket
        particle Explosion
        animation throwobject

        rocket_swirl {
            speed [1.5, 2.5] //random range of rotations per second
            radius [.5 1]
        }
        easing 1 // ease in
        lob_height 5
    }

    cost {
        infcantrip true
        mana 4
    }

    target {
        target_mode random_tile
        min_range 1
        max_range 20

        restrictions must_have_enemy
    }

    bonus_passives {
        AbilityEnabledPercentEachTurn 25%
    }

    damage_instance {
        damage 5
        knockback 1

        elements [
            Explosion
            Fire
        ]
    }
}
```

---

### `UnreliableMissile2`
**Description:** Shoot an explosive homing missile at a random enemy. This spell has a 66% chance to be disabled on each turn.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
UnreliableMissile2 {
    variant_of UnreliableMissile

    meta {
        desc "ABILITY_UNRELIABLEMISSILE2_DESC"
    }

    bonus_passives {
        AbilityEnabledPercentEachTurn 33%
    }

    cost {
        mana 3
    }
}
```

---

### `SpareParts`
**Name:** Spare Parts  
**Description:** Destroy your weapon and gain one of the following: +2 [img:shield], +4 Charge, +1 Thorns, or 1 coin.  
**Source:** `tinkerer_abilities.gon`  

```
SpareParts {
    template self_buff
    
    meta {
        name "ABILITY_SPAREPARTS_NAME"
        desc "ABILITY_SPAREPARTS_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {

    }
    
    cost {
        infcantrip true
        mana 1
        requires_destructible_weapon true
    }

    bonus_passives {
        DownRankAIIfWeaponUsable .001
    }
    
    damage_instance {
        effects {
            DestroyWeapon 1
            
            RandomStatusFromPool {
                Shield 2
                Charge 4
                Thorns 1
                GainCoins 1
            }
        }
    }
}
```

---

### `SpareParts2`
**Description:** Destroy your weapon and gain one of the following: +4 [img:shield], +8 Charge, +2 Thorns, or 2 coins.  
**Source:** `tinkerer_abilities.gon`  

```
SpareParts2 {
    variant_of SpareParts

    meta {
        desc "ABILITY_SPAREPARTS2_DESC"
    }

    damage_instance {
        effects {
            RandomStatusFromPool {
                Shield 4
                Charge 8
                Thorns 2
                GainCoins 2
            }
        }
    }
}
```

---

### `BatteryNuke`
**Name:** Split the Atom  
**Description:** Deal 50 damage to and inflict Burn 10 on all enemies. You can pay for this spell over multiple turns.
\[s:.7\](This spell's mana cost can't be modified.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
BatteryNuke {
    template spell

    meta {
        name "ABILITY_SPLITTHEATOM_NAME"
        desc "ABILITY_SPLITTHEATOM_DESC"
        class Tinkerer
    }

    graphics {
        particle Explosion
        delay 3
    }
    
    cost {
        infcantrip true
        mana 50
        can_pay_over_multiple_turns true
        disallow_cost_modification true
    }

    
    target {
        target_mode none
        aoe_mode all
        aoe_considers_character_size false
        knockback_mode zero
        aoe_restrictions exclude_allies
    }

    damage_instance {
        damage 50

        effects {
            Burn 10
        }
        
        elements [
            Fire
            Explosion
        ]
    }
}
```

---

### `BatteryNuke2`
**Description:** Deal 50 damage to and inflict Burn 10 on all enemies. You can pay for this spell over multiple turns.
This spell absorbs the mana you spend casting other spells.
\[s:.7\](This spell's mana cost can't be modified.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
BatteryNuke2 {
    variant_of BatteryNuke

    meta {
        desc "ABILITY_SPLITTHEATOM2_DESC"
    }

    bonus_passives {
        AbsorbManaFromOtherSpells 1
    }
}
```

---

### `ExperimentalTeleporter`
**Name:** Experimental Teleporter  
**Description:** Teleport to any tile. You have a 15% chance to equip a piece of Fly armor that breaks any armor pieces it replaces.  
**Source:** `tinkerer_abilities.gon`  

```
ExperimentalTeleporter {
    template teleport
    
    meta {
        name "ABILITY_EXPERIMENTALTELEPORTER_NAME"
        desc "ABILITY_EXPERIMENTALTELEPORTER_DESC"
        animate_name true
        class Tinkerer
    }

    graphics {
        self_damage_mid_port true
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        max_range 20
    }

    self_damage {
        effects {
            Conditional_ActiveWeather_Any {
                weather [FlySwarm FireflySwarm ButterflySwarm]

                DestroyEquipmentAndAttachParasite {
                    chance 1
                    pool [FlyHat FlyMask FlyNeck]
                }
            } Else {
                DestroyEquipmentAndAttachParasite {
                    chance .15
                    pool [FlyHat FlyMask FlyNeck]
                }
            }
        }
    }
}
```

---

### `ExperimentalTeleporter2`
**Description:** Teleport to any tile. You have a 15% chance to equip a piece of Fly armor that breaks any armor pieces it replaces.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
ExperimentalTeleporter2 {
    variant_of ExperimentalTeleporter

    meta {
        desc "ABILITY_EXPERIMENTALTELEPORTER2_DESC"
    }

    cost {
        mana 3
    }
}
```

---

### `ShockTherapy`
**Name:** Shock Therapy  
**Description:** Deal 1 electric damage to yourself or an adjacent unit. Cleanse debuffs from that unit, give it a random stat up, and a 25% chance to be Stunned.  
**Source:** `tinkerer_abilities.gon`  

```
ShockTherapy {
    template spell

    meta {
        name "ABILITY_SHOCKTHERAPY_NAME"
        desc "ABILITY_SHOCKTHERAPY_DESC"
        class Tinkerer
        type_icon "magic"
    }

    graphics {
        particle WaterConduct
    }
    
    cost {
        mana 5
        infcantrip true
    }

    target {
        max_aoe 0
        max_range 1
        min_range 0
    }
    
    damage_instance {
        damage 1

        effects {
            Cleanse 0
            RandomStatUp 1
            Stun [1 .25]
        }

        elements [
            Electric
        ]
    }
}
```

---

### `ShockTherapy2`
**Description:** Deal 1 electric damage to yourself or a unit in range 5. Cleanse debuffs from that unit, give it a random stat up, and a 25% chance to be Stunned.  
**Source:** `tinkerer_abilities.gon`  

```
ShockTherapy2 {
    variant_of ShockTherapy

    meta {
        desc "ABILITY_SHOCKTHERAPY2_DESC"
    }

    target {
        max_range 5
    }
}
```

---

### `BuildNuke`
**Name:** Build Nuke  
**Description:** Spawn a mini-nuke that makes a HUGE explosion when it dies.  
**Source:** `tinkerer_abilities.gon`  

```
BuildNuke {
    template spawn

    meta {
        name "ABILITY_BUILDNUKE_NAME"
        desc "ABILITY_BUILDNUKE_DESC"
        class Tinkerer
    }

    tags [summon]
    
    graphics {
        lob true
        animation buildRobot
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object MiniNuke
    }
}
```

---

### `BuildNuke2`
**Description:** Spawn a mini-nuke in range 4 that makes a HUGE explosion when it dies.  
**Source:** `tinkerer_abilities.gon`  

```
BuildNuke2 {
    variant_of BuildNuke

    meta {
        desc "ABILITY_BUILDNUKE2_DESC"
    }

    graphics {
        animation buildRobotProjectile
    }

    target {
        max_range 4
    }
}
```

---

### `InstantBarrier`
**Name:** Instant Barrier  
**Description:** Gain +6 [img:shield].
Castable only if you have no [img:shield].  
**Source:** `tinkerer_abilities.gon`  

```
InstantBarrier {
    template self_buff
    
    meta {
        name "ABILITY_INSTANTBARRIER_NAME"
        desc "ABILITY_INSTANTBARRIER_DESC"
        class Tinkerer
        type_icon "defense"
    }

    graphics {

    }

    target {
        X_is current_shield
    }
    
    cost {
        infcantrip true
        mana 1
        enabled_formula 1-X
    }
    
    damage_instance {
        effects {
            Shield 6
        }
    }
}
```

---

### `InstantBarrier2`
**Description:** Gain +6 [img:shield].
This spell's mana cost is equal to your current [img:shield].  
**Source:** `tinkerer_abilities.gon`  

```
InstantBarrier2 {
    variant_of InstantBarrier

    meta {
        desc "ABILITY_INSTANTBARRIER2_DESC"
    }

    cost {
        infcantrip true
        mana X
        enabled_formula 1
    }
}
```

---

### `VoltTackle`
**Name:** Volt Tackle  
**Description:** Teleport to anything that's electrically conductive. Displace units you teleport onto and deal electric damage to them.  
**Source:** `tinkerer_abilities.gon`  

```
VoltTackle {
    template teleport
    
    meta {
        name "ABILITY_VOLTTACKLE_NAME"
        desc "ABILITY_VOLTTACKLE_DESC"
        class Tinkerer
        type_icon "defense"
    }

    graphics {

    }

    cost {
        infcantrip true
        mana 7
    }
    target {
        max_range 20
        restrictions [aoe_must_be_displaceable must_move must_be_conductive]
    }
    
    damage_instance {
        damage 5
        type spell

        effects {
            IgnoreSelf 1
            VisualFXTile WaterConduct
        }

        elements [
            Electric
        ]
    }
}
```

---

### `VoltTackle2`
**Description:** Teleport to anything that's electrically conductive. Displace units you teleport onto and deal electric damage to them with a 50% chance to inflict Stun.  
**Source:** `tinkerer_abilities.gon`  

```
VoltTackle2 {
    variant_of VoltTackle

    meta {
        desc "ABILITY_VOLTTACKLE2_DESC"
    }

    damage_instance {
        effects {
            Stun [1 .5]
        }
    }
}
```

---

### `Smash`
**Name:** Smash  
**Description:** Smash your weapon onto an adjacent unit, destroying it and dealing double its damage.  
**Source:** `tinkerer_abilities.gon`  

```
Smash {
    template melee_attack
    
    meta {
        name "ABILITY_SMASHTINKERER_NAME"
        desc "ABILITY_SMASHTINKERER_DESC"
        class Tinkerer
    }

    tags [weapon_throw noncopyable]

    graphics {
        animation weaponslam
    }

    cost {
        requires_destructible_weapon true
        infcantrip true
        mana 5
    }

    target {
        min_range 1
        max_range 4+bonus_range
    }

    bonus_passives {
        AbilityInheritsWeaponEffects 2
        DownRankAIIfWeaponUsable .001
    }

    self_damage {
        effects {
            DestroyWeaponThrow 1
        }
    }

    damage_instance {
        damage 0
    }
}
```

---

### `Smash2`
**Description:** Smash your weapon onto an adjacent unit, destroying it and dealing double its damage.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
Smash2 {
    variant_of Smash

    meta {
        desc "ABILITY_SMASHTINKERER2_DESC"
    }

    cost {
        mana 2
    }
}
```

---

### `ShedScrap`
**Name:** Shed Scrap  
**Description:** Lose 1 [img:shield]. Spawn a junk pile.  
**Source:** `tinkerer_abilities.gon`  

```
ShedScrap {
    template spawn

    meta {
        name "ABILITY_SHEDSCRAP_NAME"
        desc "ABILITY_SHEDSCRAP_DESC"
        class Tinkerer
    }
    
    graphics {
        lob true
        animation throwobject
    }
    
    cost {
        infcantrip true
        mana 1
        enabled_formula X
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0
        X_is current_shield

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    self_damage {
        effects {
            Shield -1
        }
    }

    spawn {
        object Junk
    }
}
```

---

### `ShedScrap2`
**Description:** Lose 1 [img:shield]. Spawn a junk pile in range 2.  
**Source:** `tinkerer_abilities.gon`  

```
ShedScrap2 {
    variant_of ShedScrap

    meta {
        desc "ABILITY_SHEDSCRAP2_DESC"
    }

    target {
        max_range 2
    }
}
```

---

### `RepairArmor`
**Name:** Repair Armor  
**Description:** Lose all [img:shield], then gain [img:shield] equal to your equipment's starting [img:shield].  
**Source:** `tinkerer_abilities.gon`  

```
RepairArmor {
    template self_buff

    meta {
        name "ABILITY_REPAIRARMOR_NAME"
        desc "ABILITY_REPAIRARMOR_DESC"
        class Tinkerer
    }
    
    cost {
        infcantrip true
        mana 5
    }

    damage_instance {
        effects {
            ResetArmorShield 1
            RepairArmorCondition 1
        }
    }
}
```

---

### `RepairArmor2`
**Name:** Repair Armor  
**Description:** Lose all [img:shield], then give [img:shield] equal to your equipment's starting [img:shield] to yourself or another ally.  
**Source:** `tinkerer_abilities.gon`  

```
RepairArmor2 {
    template targeted_status

    meta {
        name "ABILITY_REPAIRARMOR_NAME"
        desc "ABILITY_REPAIRARMOR2_DESC"
        class Tinkerer
    }
    
    cost {
        infcantrip true
        mana 5
    }

    target {
        max_range 20
        restrictions must_have_ally
        min_range 0
    }

    damage_instance {
        effects {
            ResetArmorShield 1
            RepairArmorCondition 1
        }
    }
}
```

---

### `RocketRide`
**Name:** Rocket Ride  
**Description:** Jump to any open tile. Explode when you land. (This explosion also damages you.)  
**Source:** `tinkerer_abilities.gon`  

```
RocketRide {
    template jump_attack
    
    meta {
        name "ABILITY_ROCKETRIDE_NAME"
        desc "ABILITY_ROCKETRIDE_DESC"
        class Tinkerer
    }
    
    graphics {
        jump_attack_animation land
        do_damage_immediately true
    }
    
    cost {
        infcantrip true
        mana 6
    }
    
    target {
        aoe_mode standard
        min_aoe 0
        max_aoe 1
        max_range 20
        knockback_mode character_to_tile
        aoe_excludes_self false
    }
    
    damage_instance {
        damage 8
        knockback 1
        type spell
        incidentally_collects_pickups false

        effects {
            VisualFXTile Explosion
        }

        elements [
            Explosion
            Fire
        ]
    }
}
```

---

### `RocketRide2`
**Description:** Jump to any open tile. Explode when you land. (This explosion also damages you.)
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
RocketRide2 {
    variant_of RocketRide

    meta {
        desc "ABILITY_ROCKETRIDE2_DESC"
    }

    cost {
        mana 4
    }
}
```

---

### `Roomba_Bump`
**Source:** `tinkerer_abilities.gon`  

```
Roomba_Bump { //basic attack for roomba
    template dash_attack

    graphics {
        dash_start_animation ramStart
        dash_animation ramLoop
        dash_attack_animation ramEnd
    }

    target { 
        max_range 1
        max_aoe 1
    }

    damage_instance {
        damage 5+bonus_melee_damage
    }
}
```

---

### `RoboVac`
**Name:** Robo-Vac  
**Description:** Spawn a vacuum bot that collects pickups and shares their effects with you.  
**Source:** `tinkerer_abilities.gon`  

```
RoboVac {
    template spawn

    meta {
        name "ABILITY_ROBOVAC_NAME"
        desc "ABILITY_ROBOVAC_DESC"
        class Tinkerer
    }
    
    tags [summon]

    graphics {
        lob true
        animation buildRobot
    }
    
    cost {
        infcantrip true
        mana 4
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object RoboVacuum
    }
}
```

---

### `RoboVac2`
**Description:** Spawn a vacuum bot that collects pickups and shares their effects with your whole team.  
**Source:** `tinkerer_abilities.gon`  

```
RoboVac2 {
    variant_of RoboVac

    meta {
        desc "ABILITY_ROBOVAC2_DESC"
    }

    spawn {
        object RoboVacuum2
    }
}
```

---

### `NurseBotHeal`
**Name:** Give drugs!  
**Source:** `tinkerer_abilities.gon`  

```
NurseBotHeal { //basic attack for nurse bot, does not need an icon
    template tile_targeted_melee_attack

    meta {
        name "ABILITY_FEELGOODDRUGS_NAME"
    }

    graphics {
        animation heal
    }

    damage_instance {
        heal 5+bonus_melee_damage
    }
}
```

---

### `NurseBotHealCat`
**Source:** `tinkerer_abilities.gon`  

```
NurseBotHealCat {
    variant_of NurseBotHeal
    target {
        restrictions [must_not_have_tag]
        target_requires_tag robot
    }
}
```

---

### `NurseBot`
**Name:** Nurse Bot  
**Description:** Spawn a nurse bot that heals allies.  
**Source:** `tinkerer_abilities.gon`  

```
NurseBot {
    template spawn

    meta {
        name "ABILITY_NURSEBOT_NAME"
        desc "ABILITY_NURSEBOT_DESC"
        class Tinkerer
    }
    
    tags [summon]

    graphics {
        lob true
        animation buildRobot
    }
    
    cost {
        infcantrip true
        mana 9
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object NurseBot
    }
}
```

---

### `NurseBot2`
**Description:** Spawn a nurse bot that heals allies.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
NurseBot2 {
    variant_of NurseBot

    meta {
        desc "ABILITY_NURSEBOT2_DESC"
    }

    cost {
        mana 6
    }
}
```

---

### `TeslaBolt`
**Source:** `tinkerer_abilities.gon`  

```
TeslaBolt { //basic attack for tesla coil, does not need an icon
    template spell

    graphics {
        particle Bolt
        animation none
        dont_visualize_ai true
        dont_orient true
    }

    target {
        max_aoe 0
        max_range 3
        min_range 1
    }
    
    damage_instance {
        damage 3
        custom_additional_ai_weight teslacoil_priorities
        
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

### `TeslaCoil`
**Name:** Tesla Coil  
**Description:** Spawn a tesla coil that shoots lightning bolts at random units with a small chance to inflict Stun.  
**Source:** `tinkerer_abilities.gon`  

```
TeslaCoil {
    template spawn

    meta {
        name "ABILITY_TESLACOIL_NAME"
        desc "ABILITY_TESLACOIL_DESC"
        class Tinkerer
    }
    
    tags [summon]

    graphics {
        lob true
        animation buildRobot
    }
    
    cost {
        infcantrip true
        mana 7
    }
    
    target {
        min_range 1
        max_range 1
        max_aoe 0

        range_excludes_blocking false
        restrictions aoe_must_exist
    }

    spawn {
        object TeslaCoil
    }
}
```

---

### `TeslaCoil2`
**Description:** Spawn a tesla coil in range 7 that shoots lightning bolts at random units with a small chance to inflict Stun.  
**Source:** `tinkerer_abilities.gon`  

```
TeslaCoil2 {
    variant_of TeslaCoil

    meta {
        desc "ABILITY_TESLACOIL2_DESC"
    }

    graphics {
        animation buildRobotProjectile
    }

    target {
        max_range 7
    }
}
```

---

### `RefineMaterials`
**Name:** Refine Materials  
**Description:** Collect a pickup in range 3. Instead of its normal effect, gain +1 Tech.  
**Source:** `tinkerer_abilities.gon`  

```
RefineMaterials {
    template targeted_status
    
    meta {
        name "ABILITY_REFINEMATERIALS_NAME"
        desc "ABILITY_REFINEMATERIALS_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 1
    }

    target {
        max_range 3

        restrictions must_have_tag
        target_requires_tag pickup
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            CollectsPickupsWithAltEffects {
                Tech 1
            }
        }
    }
}
```

---

### `RefineMaterials2`
**Description:** Collect a pickup in range 3. Instead of its normal effect, gain +1 Tech, +1 [img:shield], and +1 to a random stat.  
**Source:** `tinkerer_abilities.gon`  

```
RefineMaterials2 {
    variant_of RefineMaterials
    
    meta {
        desc "ABILITY_REFINEMATERIALS2_DESC"
    }

    damage_instance {
        effects {
            CollectsPickupsWithAltEffects {
                Tech 1
                Shield 1
                RandomStatUp 1
            }
        }
    }
}
```

---

### `Fabricate`
**Name:** Fabricate  
**Description:** Give an ally in range 3 a temporary copy of your weapon, if they don't have a weapon.  
**Source:** `tinkerer_abilities.gon`  

```
Fabricate {
    template targeted_status
    
    meta {
        name "ABILITY_FABRICATE_NAME"
        desc "ABILITY_FABRICATE_DESC"
        class Tinkerer
        type_icon "misc"
    }

    graphics {
    }

    cost {
        infcantrip true
        mana 5
    }

    target {
        max_range 3
        min_range 1
        restrictions aoe_must_exist
        aoe_restrictions must_have_cat_with_empty_weapon_slot
    }

    damage_instance {
        damage 0
        type status_spell

        effects {
            CloneWeaponTemp 1
        }
    }
}
```

---

### `Fabricate2`
**Description:** Give an ally in range 3 a temporary copy of your weapon, if they don't have a weapon.
\[s:.7\](This spell costs less.)\[/s\]  
**Source:** `tinkerer_abilities.gon`  

```
Fabricate2 {
    variant_of Fabricate

    meta {
        desc "ABILITY_FABRICATE2_DESC"
    }

    cost {
        mana 4
    }

    target {
        max_range 20
    }
}
```

---

### `Sparks`
**Name:** Sparks  
**Description:** Shoot electric bolts at up to 3 random enemies or robots.  
**Source:** `tinkerer_abilities.gon`  

```
Sparks {
    template lobbed_attack
    
    meta {
        name "ABILITY_SPARKS_NAME"
        desc "ABILITY_SPARKS_DESC"
        class Tinkerer
    }

    graphics {
        animation castspell
        projectile LightningBallProjectile
        lob_height 1
        speed 20
    }

    cost {
        infcantrip true
        mana 7
    }

    target {
        target_mode none
        aoe_excludes_self true
        max_aoe 20

        max_targets 3
        aoe_restrictions [must_have_enemy_or_robot must_have_living_character]
    }

    damage_instance {
        damage 3
        type spell

        effects {
            VisualFXTile WaterConduct
        }

        elements [
            Electric
        ]
    }
}
```

---

### `Sparks2`
**Description:** Shoot electric bolts at up to 5 random enemies or robots.  
**Source:** `tinkerer_abilities.gon`  

```
Sparks2 {
    variant_of Sparks 

    meta {
        desc "ABILITY_SPARKS2_DESC"
    }

    target {
        max_targets 5
    }
}
```

---

### `Hone`
**Name:** Hone  
**Description:** Repair 1 use to your weapon and give it +1 damage for the rest of the battle.  
**Source:** `tinkerer_abilities.gon`  

```
Hone { //alternate basic attack for Blacksmith passive
    template self_buff

    meta {
        name "ABILITY_HONE_NAME"
        desc "ABILITY_HONE_DESC"
        class Tinkerer
        type_icon "misc"
    }

    tags [noncopyable]
    
    graphics {
        animation tinkerSelf

    }
    
    cost {
        requires_weapon true
    }

    damage_instance {
        damage 0

        effects {
            RepairWeapon 1
            CurrentWeaponDamageUp 1
            RepairWeaponCondition 1
        }
    }
}
```

---

### `Hone2`
**Description:** Repair 1 use to your weapon and give it +1 damage for the rest of the battle. Refresh your weapon action.  
**Source:** `tinkerer_abilities.gon`  

```
Hone2 { //alternate basic attack for Blacksmith passive
    variant_of Hone

    meta {
        desc "ABILITY_HONE2_DESC"
    }

    damage_instance {
        effects {
            RefreshWeaponAbility 1
        }
    }
}
```

---

