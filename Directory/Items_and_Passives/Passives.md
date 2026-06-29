# Items and Passives/Passives Directory

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

## File: `butcher_passives.gon`

### `Putrefy`
**Name:** Putrefy  
**Description:** Your basic attack inflicts Rot 1.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_PUTREFY2_DESCRIPTION`: "Your basic attack inflicts permanent Rot."

```
Putrefy {
    name "PASSIVE_PUTREFY_NAME"
    desc "PASSIVE_PUTREFY_DESCRIPTION"
    class Butcher

    1 {
        passives {
            AddStatusToBasicAttack {
                Rot 1
            }
        }
    }
    2 {
        desc "PASSIVE_PUTREFY2_DESCRIPTION"
        passives {
            AddStatusToBasicAttack {
                Rot -999999
            }
        }
    }
}
```

---

### `NeverFull`
**Name:** Never Full  
**Description:** You can heal over your max HP.
Excess HP is lost between battles.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_NEVERFULL2_DESC`: "You can heal over your max HP. <br/> Excess HP is lost between battles. <br/> Gain +1 [img:str] for every 5 HP you have over max HP."

```
NeverFull {
    name "PASSIVE_NEVERFULL_NAME"
    desc "PASSIVE_NEVERFULL_DESC"
    class Butcher

    1 {
        passives {
            UncappedHP 1
        }
    }
    2 {
        desc "PASSIVE_NEVERFULL2_DESC"
        passives {
            UncappedHP 1
            UncappedHPBonusStr 5
        }
    }
}
```

---

### `MainCourse`
**Name:** Supersize Me!  
**Description:** Food and scrap pickups you spawn are bigger.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_MAINCOURSE2_DESC`: "Food and scrap pickups you spawn are max size."

```
MainCourse {
    name "PASSIVE_MAINCOURSE_NAME"
    desc "PASSIVE_MAINCOURSE_DESC"
    class Butcher

    1 {
        passives {
            UpgradeSpawnedPickups 1
        }
    }
    2 {
        desc "PASSIVE_MAINCOURSE2_DESC"
        passives {
            UpgradeSpawnedPickups 2
        }
    }
}
```

---

### `FreshMeat`
**Name:** Fresh Meat  
**Description:** When you eat food, gain +1 [img:str].  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_FRESHMEAT2_DESC`: "When you eat food, gain +1 [img:str] and +1 to a random stat."

```
FreshMeat {
    name "PASSIVE_FRESHMEAT_NAME"
    desc "PASSIVE_FRESHMEAT_DESC"
    class Butcher

    1 {
        passives {
            StatusOnEatFood {
                StrengthUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_FRESHMEAT2_DESC"
        passives {
            StatusOnEatFood {
                StrengthUp 1
                RandomStatUp 1
            }
        }
    }
}
```

---

### `Masochist`
**Name:** Masochist  
**Description:** When you take damage, gain +1 [img:str], [img:con], or [img:spd] at random.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_MASOCHIST2_DESC`: "When you take damage, you get +1 [img:str], [img:con], and [img:spd]."

```
Masochist {
    name "PASSIVE_MASOCHIST_NAME"
    desc "PASSIVE_MASOCHIST_DESC"
    class Butcher

    1 {
        passives {
            StatusOnTookDamage {
                RandomStatusFromPool {
                    StrengthUp 1
                    ConstitutionUp 1
                    SpeedUp 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_MASOCHIST2_DESC"
        passives {
            StatusOnTookDamage {
                StrengthUp 1
                ConstitutionUp 1
                SpeedUp 1
            }
        }
    }
}
```

---

### `Glutton`
**Name:** Glutton  
**Description:** When a food pickup spawns within 2 tiles of you, move to it.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_GLUTTON2_DESC`: "When a food pickup spawns within 2 tiles of you, move to it with trample."

```
Glutton {
    name "PASSIVE_GLUTTON_NAME"
    desc "PASSIVE_GLUTTON_DESC"
    class Butcher

    1 {
        passives {
            AbilityWhenTaggedCharacterMovesNear {
                ability move
                tag food
                range 2
            }
        }
    }
    2 {
        desc "PASSIVE_GLUTTON2_DESC"
        passives {
            AbilityWhenTaggedCharacterMovesNear {
                ability move
                tag food
                range global
            }
            Trample 3
        }
    }
}
```

---

### `Hooked`
**Name:** Hooked  
**Description:** You can use your hook 2 additional times on your turn.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_HOOKED_MULTICLASS_DESC`: "You can use your weapon 2 additional times on your turn."
- `PASSIVE_HOOKED2_DESC`: "You can use your hook 2 additional times on your turn. <br/> Your hook deals +1 damage and has Cleave."
- `PASSIVE_HOOKED2_MULTICLASS_DESC`: "You can use your weapon 2 additional times on your turn. <br/> Your weapon deals +1 damage and has Cleave."

```
Hooked {
    name "PASSIVE_HOOKED_NAME"
    desc "PASSIVE_HOOKED_DESC"
    desc_multiclass "PASSIVE_HOOKED_MULTICLASS_DESC"
    class Butcher

    1 {
        passives {
            ExtraWeaponAttacks 2
        }
    }
    2 {
        desc "PASSIVE_HOOKED2_DESC"
        desc_multiclass "PASSIVE_HOOKED2_MULTICLASS_DESC"
        passives {
            ExtraWeaponAttacks 2

            BoostWeaponDamage 1
            AddStatusToWeapons {
                Cleave 1
            }
        }
    }
}
```

---

### `Stompy`
**Name:** Stompy!  
**Description:** You have Trample.
Trample damage you deal has Cleave.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_STOMPY2_DESC`: "You have Trample and +2 Bonus Moves. <br/> Trample damage you deal has Cleave."

```
Stompy {
    name "PASSIVE_STOMPY_NAME"
    desc "PASSIVE_STOMPY_DESC"
    class Butcher

    1 {
        passives {
            Trample 3

            AddStatusToTrampleDamage {
                Cleave 1
            }
        }
    }
    2 {
        desc "PASSIVE_STOMPY2_DESC"
        passives {
            Trample 3
            MoveQuivered 2

            AddStatusToTrampleDamage {
                Cleave 1
            }
        }
    }
}
```

---

### `Barbed`
**Name:** Barbed  
**Description:** Your hook deals +1 damage and inflicts Bleed.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_BARBED_MULTICLASS_DESC`: "Your weapon deals +1 damage and inflicts Bleed."
- `PASSIVE_BARBED2_DESC`: "Your hook deals +5 damage and inflicts Bleed."
- `PASSIVE_BARBED2_MULTICLASS_DESC`: "Your weapon deals +5 damage and inflicts Bleed."

```
Barbed {
    name "PASSIVE_BARBED_NAME"
    desc "PASSIVE_BARBED_DESC"
    desc_multiclass "PASSIVE_BARBED_MULTICLASS_DESC"
    class Butcher

    1 {
        passives {
            BoostWeaponDamage 1
            AddStatusToWeapons {
                Bleed 1
            }
        }
    }
    2 {
        desc "PASSIVE_BARBED2_DESC"
        desc_multiclass "PASSIVE_BARBED2_MULTICLASS_DESC"
        passives {
            BoostWeaponDamage 5
            AddStatusToWeapons {
                Bleed 1
            }
        }
    }
}
```

---

### `GrapplingHook`
**Name:** Grappling Hook  
**Description:** Your hook pulls you toward knockback-immune objects.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_GRAPPLINGHOOK_MULTICLASS_DESC`: "Your weapon pulls you toward knockback-immune objects."
- `PASSIVE_GRAPPLINGHOOK2_DESC`: "Your hook pulls you toward knockback-immune objects. Refresh your movement action when you use your hook."
- `PASSIVE_GRAPPLINGHOOK2_MULTICLASS_DESC`: "Your weapon pulls you toward knockback-immune objects. Refresh your movement action when you use your weapon."

```
GrapplingHook {
    name "PASSIVE_GRAPPLINGHOOK_NAME"
    desc "PASSIVE_GRAPPLINGHOOK_DESC"
    desc_multiclass "PASSIVE_GRAPPLINGHOOK_MULTICLASS_DESC"
    class Butcher

    1 {
        passives {
            AddStatusToWeapons {
                PullSourceToKnockbackImmuneTarget 1
            }
        }
    }
    2 {
        desc "PASSIVE_GRAPPLINGHOOK2_DESC"
        desc_multiclass "PASSIVE_GRAPPLINGHOOK2_MULTICLASS_DESC"
        passives {
            AddStatusToWeapons {
                PullSourceToKnockbackImmuneTarget 1
            }
            RefreshMoveOnWeaponConnect 1
        }
    }
}
```

---

### `PainGain`
**Name:** Rankle  
**Description:** When you take damage, gain +2 Temp Damage.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_PAINGAIN2_DESC`: "When you take damage, gain +1 Damage and +1 Temp Damage."

```
PainGain {
    name "PASSIVE_PAINGAIN_NAME"
    desc "PASSIVE_PAINGAIN_DESC"
    class Butcher

    1 {
        passives {
            StatusOnTookDamage {
                TempDamageUp 2
            }
        }
    }
    2 {
        desc "PASSIVE_PAINGAIN2_DESC"
        passives {
            StatusOnTookDamage {
                TempDamageUp 1
                DamageUp 1
            }
        }
    }
}
```

---

### `WideSwing`
**Name:** Spin to Win  
**Description:** Your basic attack is a 3x3 tile spin attack with Cleave.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_WIDESWING2_DESC`: "Your basic attack is a 3x3 tile double spin attack with Cleave."

```
WideSwing {
    name "PASSIVE_WIDESWING_NAME"
    desc "PASSIVE_WIDESWING_DESC"
    class Butcher

    1 {
        override_basic_attack BasicButcherMeleeWideSpin 
        passives {
            ReplaceBasicAttack BasicButcherMeleeWideSpin
        }
    }
    2 {
        desc "PASSIVE_WIDESWING2_DESC"

        override_basic_attack BasicButcherMeleeWideDoubleSpin 
        passives {
            ReplaceBasicAttack BasicButcherMeleeWideDoubleSpin
        }
    }
}
```

---

### `Confrontational`
**Name:** Confrontational  
**Description:** When you take damage, trample one tile towards the source of damage.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_CONFRONTATIONAL2_DESC`: "When you take damage, trample all the way to the source of damage."

```
Confrontational {
    name "PASSIVE_CONFRONTATIONAL_NAME"
    desc "PASSIVE_CONFRONTATIONAL_DESC"
    class Butcher

    1 {
        passives {
            MoveTowardsDamageSource {
                move_ability TrampleMoveOne
                move_far false
            }
        }
    }
    2 {
        desc "PASSIVE_CONFRONTATIONAL2_DESC"

        passives {
            MoveTowardsDamageSource {
                move_ability TrampleMove
                move_far false
            }
        }
    }
}
```

---

### `HeaveHook`
**Name:** Heave Hook  
**Description:** Your hook can target tiles.
Units pulled by your hook gain trample while being hooked.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_HEAVEHOOK_MULTICLASS_DESC`: "Your hook can target tiles. <br/> Units pulled by your hook gain trample while being hooked. <br/> \[s:.7\](Equips a temporary hook if you dont have one)\[/s\]"
- `PASSIVE_HEAVEHOOK2_DESC`: "Your hook can target tiles. <br/> Units pulled by your hook gain trample while being hooked, this trample damage is doubled."
- `PASSIVE_HEAVEHOOK2_MULTICLASS_DESC`: "Your hook can target tiles. <br/> Units pulled by your hook gain trample while being hooked, this trample damage is doubled. <br/> \[s:.7\](Equips a temporary hook if you dont have one)\[/s\]"

```
HeaveHook {
    name "PASSIVE_HEAVEHOOK_NAME"
    desc "PASSIVE_HEAVEHOOK_DESC"
    desc_multiclass "PASSIVE_HEAVEHOOK_MULTICLASS_DESC"
    class Butcher

    1 {
        passives {
            LobbedHook 1
            EquipTemporaryItem ButcherHook_Temporary //equips a hook for classes that don't innately have one
        }
    }
    2 {
        desc "PASSIVE_HEAVEHOOK2_DESC"
        desc_multiclass "PASSIVE_HEAVEHOOK2_MULTICLASS_DESC"

        passives {
            LobbedHook 2
            EquipTemporaryItem ButcherHook_Temporary //equips a hook for classes that don't innately have one
        }
    }
}
```

---

### `Harpooner`
**Name:** Harpooner  
**Description:** When an enemy moves in range, hook it.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_HARPOONER_MULTICLASS_DESC`: "When an enemy moves in range, attack it with your weapon."
- `PASSIVE_HARPOONER2_DESC`: "When an enemy moves in range, hook it. Your hook deals +2 Damage."
- `PASSIVE_HARPOONER2_MULTICLASS_DESC`: "When an enemy moves in range, attack it with your weapon. Your weapon deals +2 Damage."

```
Harpooner {
    name "PASSIVE_HARPOONER_NAME"
    desc "PASSIVE_HARPOONER_DESC"
    desc_multiclass "PASSIVE_HARPOONER_MULTICLASS_DESC"
    class Butcher

    1 {
        passives {
            MovementReaction {
                ability weapon
                enemies_only true
            }
        }
    }
    2 {
        desc "PASSIVE_HARPOONER2_DESC"
        desc_multiclass "PASSIVE_HARPOONER2_MULTICLASS_DESC"

        passives {
            MovementReaction {
                ability weapon
                enemies_only true
            }
            BoostWeaponDamage 2
        }
    }
}
```

---

### `LordOfTheFlies`
**Name:** Lord of the Flies  
**Description:** All flies are Charmed and get +1 Damage.
Whenever you inflict Rot, you inflict +1 Rot.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_LORDOFTHEFLIES2_DESC`: "All flies are Charmed and get +4 Damage. <br/> Whenever you inflict Rot, you inflict +1 Rot."

```
LordOfTheFlies {
    name "PASSIVE_LORDOFTHEFLIES_NAME"
    desc "PASSIVE_LORDOFTHEFLIES_DESC"
    class Butcher

    1 {
        passives {
            CharmAllFlies 1
            FlyDamageIncrease 1
            AmplifyStatus Rot
        }
    }
    2 {
        desc "PASSIVE_LORDOFTHEFLIES2_DESC"

        passives {
            CharmAllFlies 1
            FlyDamageIncrease 4
            AmplifyStatus Rot
        }
    }
}
```

---

### `Schadenfreude`
**Name:** Schadenfreude  
**Description:** Your [img:str] and [img:con] are increased by 2 for each disorder your party has.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_SCHADENFREUDE2_DESC`: "All of your stats are increased by 2 for each disorder your party has."

```
Schadenfreude {
    name "PASSIVE_SCHADENFREUDE_NAME"
    desc "PASSIVE_SCHADENFREUDE_DESC"
    class Butcher

    tags [noncopyable]
    
    1 {
        schadenfreude_scaled_stats { //hard coded in CatData::get_bonus_stats and Character::recompute_item_effects
            str 2
            con 2
        }
    }
    2 {
        desc "PASSIVE_SCHADENFREUDE2_DESC"

        schadenfreude_scaled_stats { //hard coded in CatData::get_bonus_stats and Character::recompute_item_effects
            str 2
            dex 2
            con 2
            int 2
            cha 2
            spd 2
            lck 2
        }
    }
}
```

---

### `Gurgitator`
**Name:** Gurgitator  
**Description:** Whenever you heal over your max HP, gain +1 [img:str].  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_GURGITATOR2_DESC`: "Whenever you heal over your max HP, gain +1 [img:str] and +1 Weapon Damage."

```
Gurgitator {
    name "PASSIVE_GURGITATOR_NAME"
    desc "PASSIVE_GURGITATOR_DESC"
    class Butcher

    1 {
        passives {
            StatusOnOverHealed {
                StrengthUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_GURGITATOR2_DESC"
        passives {
            StatusOnOverHealed {
                StrengthUp 1
                CurrentWeaponDamageUp 1
            }
        }
    }
}
```

---

### `LooseMeat`
**Name:** Loose Meat  
**Description:** When you take damage, spawn a food pickup.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_LOOSEMEAT2_DESC`: "When you take damage or move, spawn a food pickup."

```
LooseMeat {
    name "PASSIVE_LOOSEMEAT_NAME"
    desc "PASSIVE_LOOSEMEAT_DESC"
    class Butcher

    1 {
        passives {
            SpawnThingOnDamage {
                object Food
            }
        }
    }
    2 {
        desc "PASSIVE_LOOSEMEAT2_DESC"
        passives {
            SpawnThingOnDamage {
                object Food
            }
            SpawnMeatOnMove Food
        }
    }
}
```

---

### `Hack`
**Name:** Hack  
**Description:** Your basic attack is always critical against enemies with [img:shield].
Your basic attack's critical hits remove buffs from units.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_HACK2_DESC`: "Your basic attack is always critical against enemies with [img:shield]. <br/> Your basic attack's critical hits remove buffs from units. <br/> Your critical hits deal +100% damage."

```
Hack {
    name "PASSIVE_HACK_NAME"
    desc "PASSIVE_HACK_DESC"
    class Butcher

    1 {
        passives {
            AddStatusToBasicAttack {
                Conditional_Shielded {
                    BonusCritChance 100
                }
                ApplyStatusIfCrit {
                    Purge 0
                }
            }
        }
    }
    2 {
        desc "PASSIVE_HACK2_DESC"
        passives {
            AddStatusToBasicAttack {
                Conditional_Shielded {
                    BonusCritChance 100
                }
                ApplyStatusIfCrit {
                    Purge 0
                }
            }

            AddCritMultiplier 100%
        }
    }
}
```

---

### `BowlingBall`
**Name:** Bowling Ball  
**Description:** Adjacent and diagonal allied cats get the bonus ability Bowl.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_BOWLINGBALL2_DESC`: "Adjacent and diagonal allied cats get the bonus ability Bowl+."

```
BowlingBall {
    name "PASSIVE_BOWLINGBALL_NAME"
    desc "PASSIVE_BOWLINGBALL_DESC"
    class Butcher

    1 {
        passives {
            AllyBonusAbilityAura {
                ability Bowl
                square true
            }
            AddHiddenTag bowling_ball
        }
    }
    2 {
        desc "PASSIVE_BOWLINGBALL2_DESC"
        passives {
            AllyBonusAbilityAura {
                ability Bowl2
                square true
            }
            AddHiddenTag bowling_ball
        }
    }
}
```

---

### `Testy`
**Name:** Testy  
**Description:** When you take damage, gain +1 movement range until the end of your turn.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_TESTY2_DESC`: "When you take damage, gain +1 movement range."

```
Testy {
    name "PASSIVE_TESTY_NAME"
    desc "PASSIVE_TESTY_DESC"
    class Butcher

    1 {
        passives {
            StatusOnTookDamage {
                TempMovement 1
            }
        }
    }
    2 {
        desc "PASSIVE_TESTY2_DESC"
        passives {
            StatusOnTookDamage {
                MovementUp 1
            }
        }
    }
}
```

---

### `Indigestion`
**Name:** Indigestion  
**Description:** Whenever you heal over your max HP, fart and inflict Poison 3 on adjacent units.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_INDIGESTION2_DESC`: "Whenever you heal over your max HP, fart and inflict Poison 3 and Burn 3 on adjacent units."

```
Indigestion {
    name "PASSIVE_INDIGESTION_NAME"
    desc "PASSIVE_INDIGESTION_DESC"
    class Butcher

    1 {
        passives {
            StatusOnOverHealed {
                ForceUseAbility_NonStack Indigestion_Fart
            }
        }
    }
    2 {
        desc "PASSIVE_INDIGESTION2_DESC"
        passives {
            StatusOnOverHealed {
                ForceUseAbility_NonStack Indigestion_Fart2
            }
        }
    }
}
```

---

### `Incubator`
**Name:** Incubator  
**Description:** Whenever you heal over your max HP, spawn a rot fly.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_INCUBATOR2_DESC`: "Whenever you heal over your max HP, spawn a rot fly with HP and damage equal to the excess healing."

```
Incubator {
    name "PASSIVE_INCUBATOR_NAME"
    desc "PASSIVE_INCUBATOR_DESC"
    class Butcher

    1 {
        passives {
            StatusOnOverHealed {
                SpawnScaledRotFly 0
            }
        }
    }
    2 {
        desc "PASSIVE_INCUBATOR2_DESC"
        passives {
            ScaledStatusOnOverHealed {
                SpawnScaledRotFly 1
            }
        }
    }
}
```

---

### `DukeOfFlies`
**Name:** Duke of Flies  
**Description:** At the end of the battle, all food pickups become allied flies.
Allied flies stay with you between battles.  
**Source:** `butcher_passives.gon`  

**Localization Strings:**
- `PASSIVE_DUKEOFFLIES2_DESC`: "At the end of the battle, all food pickups become allied flies. <br/> Allied flies stay with you between battles. <br/> Your basic attack spawns flies."

```
DukeOfFlies {
    name "PASSIVE_DUKEOFFLIES_NAME"
    desc "PASSIVE_DUKEOFFLIES_DESC"
    class Butcher

    1 {
        passives {
            DukeOfFlies 1
        }
    }
    2 {
        desc "PASSIVE_DUKEOFFLIES2_DESC"
        passives {
            DukeOfFlies 1

            AddStatusToBasicAttack {
                BounceObject AllyRotFly
            }
        }
    }
}
```

---

## File: `colorless_passives.gon`

### `SelfAssured`
**Name:** Self-Assured  
**Description:** Gain a random stat up whenever you down a unit.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_SELFASSURED2_DESC`: "Gain All Stats Up whenever you down a unit."

```
SelfAssured {
    name "PASSIVE_SELFASSURED_NAME"
    desc "PASSIVE_SELFASSURED_DESC"
    class Colorless

    1 {
        passives {
            StatusOnKill {
                RandomStatUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_SELFASSURED2_DESC"
        passives {
            StatusOnKill {
                AllStatsUp 1
            }
        }
    }
}
```

---

### `LuckDrain`
**Name:** Luck Drain  
**Description:** Gain +1 [img:lck] whenever a unit is downed.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_LUCKDRAIN2_DESC`: "Gain +1 [img:lck] whenever a unit is downed. <br/> Gain an extra +2 [img:lck] whenever YOU down a unit."

```
LuckDrain {
    name "PASSIVE_LUCKDRAIN_NAME"
    desc "PASSIVE_LUCKDRAIN_DESC"
    class Colorless

    1 {
        passives {
            StatusOnAnyDeath {
                LuckUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_LUCKDRAIN2_DESC"
        passives {
            StatusOnAnyDeath {
                LuckUp 1
            }
            StatusOnKill {
                LuckUp 2
            }
        }
    }
}
```

---

### `Infested`
**Name:** Infested  
**Description:** 50% chance to spawn a flea familiar when you end your turn.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_INFESTED2_DESC`: "Spawn 2-3 fleas at the start of each battle. <br/> 50% chance to spawn a flea familiar when you end your turn."

```
Infested {
    name "PASSIVE_INFESTED_NAME"
    desc "PASSIVE_INFESTED_DESC"
    class Colorless

    1 {
        passives {
            SpawnEachTurn {
                object CharmedFlea
                number 1
                chance .5
            }
        }
    }
    2 {
        desc "PASSIVE_INFESTED2_DESC"
        passives {
            SpawnEachTurn {
                object CharmedFlea
                number 1
            }
            SpawnOnBattleStart {
                object CharmedFlea
                number [2 3]
            }
        }
    }
}
```

---

### `Worms`
**Name:** Worms  
**Description:** 50% chance to spawn a maggot familiar when you end your turn.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_WORMS2_DESC`: "50% chance to spawn a mutated maggot familiar when you end your turn."

```
Worms {
    name "PASSIVE_WORMS_NAME"
    desc "PASSIVE_WORMS_DESC"
    class Colorless

    1 {
        passives {
            SpawnEachTurn {
                chance .5
                object CharmedMaggot
            }
        }
    }
    2 {
        desc "PASSIVE_WORMS2_DESC"
        passives {
            SpawnEachTurn {
                chance .5
                object [CharmedTumorousMaggot CharmedChargeyMaggot CharmedSwappyMaggot]
            }
        }
    }
}
```

---

### `Amped`
**Name:** Amped  
**Description:** Gain +1 [img:spd] at the end of your turn.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_AMPED2_DESC`: "Gain +1 [img:spd] at the end of your turn. <br/> You can move an extra time each turn."

```
Amped {
    name "PASSIVE_AMPED_NAME"
    desc "PASSIVE_AMPED_DESC"
    class Colorless

    1 {
        passives {
            StatusEachTurnEnd {
                SpeedUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_AMPED2_DESC"
        passives {
            StatusEachTurnEnd {
                SpeedUp 1
            }
            ExtraMovePoints 1
        }
    }
}
```

---

### `Furious`
**Name:** Furious  
**Description:** Gain +1 Damage each time you land a critical hit.
+5% critical hit chance.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_FURIOUS2_DESC`: "Gain +1 Damage and +5% critical hit chance each time you land a critical hit. <br/> +5% critical hit chance."

```
Furious {
    name "PASSIVE_FURIOUS_NAME"
    desc "PASSIVE_FURIOUS_DESC"
    class Colorless

    1 {
        passives {
            StatusOnCrit {
                DamageUp 1
            }
            CritChanceUp 5
        }
    }
    2 {
        desc "PASSIVE_FURIOUS2_DESC"
        passives {
            StatusOnCrit {
                DamageUp 1
                CritChanceUp 5
            }
            CritChanceUp 5
        }
    }
}
```

---

### `Deathless`
**Name:** Deathless  
**Description:** +3 Corpse HP  
**Source:** `colorless_passives.gon`  

```
Deathless {
    name "PASSIVE_DEATHLESS_NAME"
    desc "PASSIVE_DEATHLESS_DESC"
    class Colorless

    1 {
        passives {
            AddCorpseHealth 3
        }
    }
    2 {
        passives {
            AddCorpseHealth 96
        }
    }
}
```

---

### `MetalDetector`
**Name:** Metal Detector  
**Description:** 5% chance to spawn a coin when you move over a tile.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_METALDETECTOR2_DESC`: "10% chance to spawn a coin when you move over a tile."

```
MetalDetector {
    name "PASSIVE_METALDETECTOR_NAME"
    desc "PASSIVE_METALDETECTOR_DESC"
    class Colorless

    1 {
        passives {
            MetalDetector 5
        }
    }
    2 {
        desc "PASSIVE_METALDETECTOR2_DESC"
        passives {
            MetalDetector 10
            //TODO: find random equipment after each battle
        }
    }
}
```

---

### `DeathProof`
**Name:** Deathproof  
**Description:** While downed, you have a 25% chance to revive with 1 HP at the end of each round.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_DEATHPROOF2_DESC`: "While downed, you have a 33% chance to revive with 10 HP and All Stats Up at the end of each round."

```
DeathProof {
    name "PASSIVE_DEATHPROOF_NAME"
    desc "PASSIVE_DEATHPROOF_DESC"
    class Colorless

    1 {
        passives {
            ChanceToRevive 25
        }
    }
    2 {
        desc "PASSIVE_DEATHPROOF2_DESC"
        passives {
            ChanceToRevive {
                stacks 33

                statuses {
                    AllStatsUp 1
                    HealthGain 10
                }
            }
        }
    }
}
```

---

### `Leader`
**Name:** Leader  
**Description:** Adjacent allies have +1 Damage and +1 Range.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_LEADER2_DESC`: "All allies have +1 Damage and +1 Range."

```
Leader {
    name "PASSIVE_LEADER_NAME"
    desc "PASSIVE_LEADER_DESC"
    class Colorless

    1 {
        passives {
            BoostDamageAura 1
            BoostRangeAura 1
        }
    }
    2 {
        desc "PASSIVE_LEADER2_DESC"
        passives {
            BoostDamageGlobalAura 1
            BoostRangeGlobalAura 1
        }
    }
}
```

---

### `Mange`
**Name:** Mange  
**Description:** Inflict Poison 1 on units that contact you.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_MANGE2_DESC`: "Inflict 1 Poison, Bleed, Bruise, Weakness, and Leech on units that contact you."

```
Mange {
    name "PASSIVE_MANGE_NAME"
    desc "PASSIVE_MANGE_DESC"
    class Colorless

    1 {
        passives {
            MeleeRevengeDamage {
                effects {
                    Poison 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_MANGE2_DESC"
        passives {
            MeleeRevengeDamage {
                effects {
                    Poison 1
                    Bleed 1
                    Bruise 1
                    Weakness 1
                    Leeches 1
                }
            }
        }
    }
}
```

---

### `ETank`
**Name:** E-Tank  
**Description:** Start each battle with +20 unfilled max health.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_ETANK2_DESC`: "Start each battle with +50 unfilled max health."

```
ETank {
    name "PASSIVE_ETANK_NAME"
    desc "PASSIVE_ETANK_DESC"
    class Colorless

    1 {
        passives {
            AddUnfilledMaxHealth 20
        }
    }
    2 {
        desc "PASSIVE_ETANK2_DESC"
        passives {
            AddUnfilledMaxHealth 50
        }
    }
}
```

---

### `Careful`
**Name:** Careful  
**Description:** Damage you deal to other allies is reduced to 0.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_CAREFUL2_DESC`: "Damage you deal to other allies is reduced to 0. You cannot inflict debuffs on other allies. <br/> You are careful in many other ways too."

```
Careful {
    name "PASSIVE_CAREFUL_NAME"
    desc "PASSIVE_CAREFUL_DESC"
    class Colorless

    1 {
        passives {
            AllyDamageReduction 0
        }
    }
    2 {
        desc "PASSIVE_CAREFUL2_DESC"
        passives {
            AllyDamageReduction 0
            WeaponsDontLoseDurability 0
            DodgeChance 25%
            BackstabImmunity 1
            IgnoreTiles 1
            StatusCarefulness 1
        }
    }
}
```

---

### `DirtyClaws`
**Name:** Dirty Claws  
**Description:** Your physical attacks on Poisoned or Bleeding enemies inflict +1 Poison and/or Bleed.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_DIRTYCLAWS2_DESC`: "Your basic attack inflicts Poison 1 and Bleed 1.  <br/> Your physical attacks on Poisoned or Bleeding enemies inflict +1 Poison and/or Bleed."

```
DirtyClaws {
    name "PASSIVE_DIRTYCLAWS_NAME"
    desc "PASSIVE_DIRTYCLAWS_DESC"
    class Colorless

    1 {
        passives {
            DirtyClaws 1
        }
    }
    2 {
        desc "PASSIVE_DIRTYCLAWS2_DESC"
        passives {
            DirtyClaws 1
            AddStatusToBasicAttack {
                Poison 1
                Bleed 1
            }
        }
    }
}
```

---

### `LateBloomer`
**Name:** Late Bloomer  
**Description:** On your 5th turn, you gain All Stats Up 3.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_LATEBLOOMER2_DESC`: "On your 3rd turn, you gain All Stats Up 3."

```
LateBloomer {
    name "PASSIVE_LATEBLOOMER_NAME"
    desc "PASSIVE_LATEBLOOMER_DESC"
    class Colorless

    1 {
        passives {
            LateBloomer {
                stacks 5
                AllStatsUp 3
            }
        }
    }
    2 {
        desc "PASSIVE_LATEBLOOMER2_DESC"
        passives {
            LateBloomer {
                stacks 3
                AllStatsUp 3
            }
        }
    }
}
```

---

### `Study`
**Name:** Study  
**Description:** Gain +1 [img:int] whenever you hit a new type of unit with an attack or ability.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_STUDY2_DESC`: "Gain +1 [img:int] whenever you hit a new type of unit with an attack or ability. All enemies of that type become Marked."

```
Study {
    name "PASSIVE_STUDY_NAME"
    desc "PASSIVE_STUDY_DESC"
    class Colorless

    1 {
        passives {
            Study 1
        }
    }
    2 {
        desc "PASSIVE_STUDY2_DESC"
        passives {
            Study {
                stacks 1
                marked 2
            }
        }
    }
}
```

---

### `SkillShare`
**Name:** Skill Share  
**Description:** Your other passive ability is shared with the other cats in your party at the start of each battle.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_SKILLSHARE2_DESC`: "Your other passive ability is shared with the other cats in your party at the start of each battle. When breeding, your children will always inherit your other passive."

```
SkillShare {
    name "PASSIVE_SKILLSHARE_NAME"
    desc "PASSIVE_SKILLSHARE_DESC"
    class Colorless

    tags [noncopyable]

    1 {
        //hard coded
    }
    2 {
        desc "PASSIVE_SKILLSHARE2_DESC"
        //hard coded
    }
}
```

---

### `NaturalHealing`
**Name:** Natural Healing  
**Description:** You have +1 Health Regeneration  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_NATURALHEALING2_DESC`: "You have +2 Health Regeneration <br/> Adjacent allies gain +1 Health Regeneration"

```
NaturalHealing {
    name "PASSIVE_NATURALHEALING_NAME"
    desc "PASSIVE_NATURALHEALING_DESC"
    class Colorless

    1 {
        passives {
            HealthRegenUp 1
        }
    }
    2 {
        desc "PASSIVE_NATURALHEALING2_DESC"
        passives {
            HealthRegenUp 2
            HealingAura 1
        }
    }
}
```

---

### `LongShot`
**Name:** Longshot  
**Description:** +1 Range.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_LONGSHOT2_DESC`: "+2 Range. <br/> Your ranged attacks have +25% critical hit chance."

```
LongShot {
    name "PASSIVE_LONGSHOT_NAME"
    desc "PASSIVE_LONGSHOT_DESC"
    class Colorless

    1 {
        passives {
            AddBonusRange 1
        }
    }
    2 {
        desc "PASSIVE_LONGSHOT2_DESC"
        passives {
            AddBonusRange 2
            AddRangedCritChance 25%
        }
    }
}
```

---

### `FastFooted`
**Name:** Fast Footsies  
**Description:** You are immune to negative tile effects.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_FASTFOOTED2_DESC`: "You are immune to negative tile effects. <br/> You can move through units and objects."

```
FastFooted {
    name "PASSIVE_FASTFOOTED_NAME"
    desc "PASSIVE_FASTFOOTED_DESC"
    class Colorless

    1 {
        passives {
            IgnoreTiles 1
        }
        stats {
            spd 1
        }
    }
    2 {
        desc "PASSIVE_FASTFOOTED2_DESC"
        passives {
            IgnoreTiles 1
            Phasing 1
        }
        stats {
            spd 3
        }
    }
}
```

---

### `Slugger`
**Name:** Slugger  
**Description:** +1 Damage.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_SLUGGER2_DESC`: "+3 Damage."

```
Slugger {
    name "PASSIVE_SLUGGER_NAME"
    desc "PASSIVE_SLUGGER_DESC"
    class Colorless

    1 {
        passives {
            DamageUp 1
        }
    }
    2 {
        desc "PASSIVE_SLUGGER2_DESC"
        passives {
            DamageUp 3
        }
    }
}
```

---

### `Pulp`
**Name:** Pulp  
**Description:** When you kill a unit or destroy a corpse, it becomes meat.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_PULP2_DESC`: "+4 Damage. <br/> When you kill a unit or destroy a corpse, it becomes meat."

```
Pulp {
    name "PASSIVE_PULP_NAME"
    desc "PASSIVE_PULP_DESC"
    class Colorless

    1 {
        passives {
            KillsToMeat Food
        }
    }
    2 {
        desc "PASSIVE_PULP2_DESC"
        passives {
            KillsToMeat Food
            DamageUp 4
        }
    }
}
```

---

### `Amplify`
**Name:** Amplify  
**Description:** +1 Magic Damage.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_AMPLIFY2_DESC`: "+1 Magic Damage for every 3 [img:cha] you have."

```
Amplify {
    name "PASSIVE_AMPLIFY_NAME"
    desc "PASSIVE_AMPLIFY_DESC"
    class Colorless

    1 {
        passives {
            AddSpellDamage 1
        }
    }
    2 {
        desc "PASSIVE_AMPLIFY2_DESC"
        passives {
            AddChaScalingSpellDamage 3
        }
    }
}
```

---

### `DeathBoon`
**Name:** Death Boon  
**Description:** When you're downed, all allies gain All Stats Up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_DEATHBOON2_DESC`: "When you're downed, all allies gain All Stats Up 2."

```
DeathBoon {
    name "PASSIVE_DEATHBOON_NAME"
    desc "PASSIVE_DEATHBOON_DESC"
    class Colorless

    1 {
        passives {
            BoostAllyStatsOnDeath 1
        }
    }
    2 {
        desc "PASSIVE_DEATHBOON2_DESC"
        passives {
            BoostAllyStatsOnDeath 2
        }
    }
}
```

---

### `SantaSangre`
**Name:** Santa Sangre  
**Description:** When you're downed, allies heal 12 HP. Excess healing is converted to Shield.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_SANTASANGRE2_DESC`: "When you're downed, allies heal 20 HP. Excess healing is converted to Shield."

```
SantaSangre {
    name "PASSIVE_SANTASANGRE_NAME"
    desc "PASSIVE_SANTASANGRE_DESC"
    class Colorless

    1 {
        passives {
            StatusAlliesOnDeath {
                HealAndOverhealToShield 12
            }
        }
    }
    2 {
        desc "PASSIVE_SANTASANGRE2_DESC"
        passives {
            StatusAlliesOnDeath {
                HealAndOverhealToShield 20
            }
        }
    }
}
```

---

### `Untouched`
**Name:** Unscarred  
**Description:** While at full hp you have 100% critical hit chance.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_UNSCARRED2_DESC`: "While at full hp you have 100% critical hit chance, +5 Mana Regeneration  and +1 All Stats Up."

```
Untouched {
    name "PASSIVE_UNSCARRED_NAME"
    desc "PASSIVE_UNSCARRED_DESC"
    class Colorless

    1 {
        passives {
            FullHealthCritChance 100
        }
    }
    2 {
        desc "PASSIVE_UNSCARRED2_DESC"
        passives {
            FullHealthCritChance 100
            FullHealthAllStatsUp 1
            FullHealthManaRegen 5
        }
    }
}
```

---

### `Daunt`
**Name:** Daunt  
**Description:** Small enemies won't attack you.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_DAUNT2_DESC`: "Small enemies won't attack you. <br/> Inflict Fear 1 on units that contact or attack you."

```
Daunt {
    name "PASSIVE_DAUNT_NAME"
    desc "PASSIVE_DAUNT_DESC"
    class Colorless

    1 {
        passives {
            SmallEnemiesIgnoreYou 1
        }
    }
    2 {
        desc "PASSIVE_DAUNT2_DESC"
        passives {
            SmallEnemiesIgnoreYou 1
            RevengeDamage {
                effects {
                    Fear 1
                }
            }
        }
    }
}
```

---

### `AnimalHandler`
**Name:** Animal Handler  
**Description:** You start each battle with a random vermin familiar with boosted damage and health.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_ANIMALHANDLER2_DESC`: "You start each battle with 3 random vermin familiars with boosted damage and health."

```
AnimalHandler {
    name "PASSIVE_ANIMALHANDLER_NAME"
    desc "PASSIVE_ANIMALHANDLER_DESC"
    class Colorless

    1 {
        passives {
            SpawnOnBattleStart {
                object [BuffFamiliarMaggot BuffFamiliarPooter BuffFamiliarFlea BuffFamiliarFly]
                number 1
            }
        }
    }
    2 {
        desc "PASSIVE_ANIMALHANDLER2_DESC"
        passives {
            SpawnOnBattleStart {
                object [BuffFamiliarMaggot BuffFamiliarPooter BuffFamiliarFlea BuffFamiliarFly]
                number 3
            }
        }
    }
}
```

---

### `WhipCracker`
**Name:** Whipcracker  
**Description:** When you damage an ally they gain +1 Damage.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_WHIPCRACKER2_DESC`: "When you damage an ally they gain +1 Damage and +1 [img:spd]."

```
WhipCracker {
    name "PASSIVE_WHIPCRACKER_NAME"
    desc "PASSIVE_WHIPCRACKER_DESC"
    class Colorless

    1 {
        passives {
            ExtraStatusWhenDealingDamage {
                Conditional_Ally {
                    DamageUp 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_WHIPCRACKER2_DESC"
        passives {
            ExtraStatusWhenDealingDamage {
                Conditional_Ally {
                    DamageUp 1
                    SpeedUp 1
                }
            }
        }
    }
}
```

---

### `PressurePoints`
**Name:** Might of the Meek  
**Description:** Damage you deal that's 2 or less is always critical.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_PRESSUREPOINTS2_DESC`: "Damage you deal that's 3 or less is always critical. +50% Crit Damage."

```
PressurePoints {
    name "PASSIVE_PRESSUREPOINTS_NAME"
    desc "PASSIVE_PRESSUREPOINTS_DESC"
    class Colorless

    1 {
        passives {
            AutoCritLowDamage 2
        }
    }
    2 {
        desc "PASSIVE_PRESSUREPOINTS2_DESC"
        passives {
            AutoCritLowDamage 3
            AddCritMultiplier 50%
        }
    }
}
```

---

### `Gassy`
**Name:** Gassy  
**Description:** Whenever you take damage, knock back all adjacent units.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_GASSY2_DESC`: "Whenever you take damage, poison all adjacent units and knock them back 10 tiles."

```
Gassy {
    name "PASSIVE_GASSY_NAME"
    desc "PASSIVE_GASSY_DESC"
    class Colorless

    1 {
        passives {
            AbilityReaction Gassy_AssBlast
        }
    }
    2 {
        desc "PASSIVE_GASSY2_DESC"
        passives {
            AbilityReaction Gassy_AssBlast2
        }
    }
}
```

---

### `Dealer`
**Name:** Dealer  
**Description:** You can use consumables on other units.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_DEALER2_DESC`: "You can use consumables on other units. <br/> Consumables you use have double the effect."

```
Dealer { //TODO: fix this being able to target meat onto vegan cats
    name "PASSIVE_DEALER_NAME"
    desc "PASSIVE_DEALER_DESC"
    class Colorless

    1 {
        passives {
            ConsumablesInfiniteRange 1
        }
    }
    2 {
        desc "PASSIVE_DEALER2_DESC"
        passives {
            ConsumablesInfiniteRange 1
            ConsumableEffectsMultiplierBonus 1
        }
    }
}
```

---

### `Patience`
**Name:** Patience  
**Description:** If you end your turn without taking any actions, gain an extra turn at the end of the round. You don't regenerate mana on your main turn if you pass it.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_PATIENCE2_DESC`: "If you end your turn without taking any actions, gain an extra turn at the end of the round."

```
Patience {
    name "PASSIVE_PATIENCE_NAME"
    desc "PASSIVE_PATIENCE_DESC"
    class Colorless

    1 {
        passives {
            AllowPassTurn 0
        }
    }
    2 {
        desc "PASSIVE_PATIENCE2_DESC"
        passives {
            AllowPassTurn 1
        }
    }
}
```

---

### `Wiggly`
**Name:** Wiggly  
**Description:** +25% dodge chance.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_WIGGLY2_DESC`: "+25% dodge chance and +25% critical hit chance."

```
Wiggly {
    name "PASSIVE_WIGGLY_NAME"
    desc "PASSIVE_WIGGLY_DESC"
    class Colorless

    1 {
        passives {
            DodgeChance 25%
        }
    }
    2 {
        desc "PASSIVE_WIGGLY2_DESC"
        passives {
            DodgeChance 25%
            CritChanceUp 25
        }
    }
}
```

---

### `MiniMe`
**Name:** Mini-Me  
**Description:** Gain a half-sized copy of yourself that has 50% of your stats. The copy is AI controlled.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_MINIME2_DESC`: "Gain a half-sized copy of yourself that has 50% of your stats and quarter-sized copy that has 25% of your stats. The copies are AI controlled."

```
MiniMe {
    name "PASSIVE_MINIME_NAME"
    desc "PASSIVE_MINIME_DESC"
    class Colorless

    1 {
        passives {
            SpawnCatCopyOnBattleStart {
                object PlayerCat_MiniMe
			    prevent_chain_tag minime_clone
            }
        }
    }
    2 {
        desc "PASSIVE_MINIME2_DESC"

        passives {
            SpawnCatCopyOnBattleStart {
                object PlayerCat_MiniMe
			    prevent_chain_tag minime_clone
            }
            SpawnCatCopyOnBattleStart {
                object PlayerCat_MiniMiniMe
			    prevent_chain_tag minime_clone
            }
        }
    }
}
```

---

### `BareMinimum`
**Name:** Bare Minimum  
**Description:** Your stats can't go below 5.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_BAREMINIMUM2_DESC`: "Your stats can't go below 7."

```
BareMinimum {
    name "PASSIVE_BAREMINIMUM_NAME"
    desc "PASSIVE_BAREMINIMUM_DESC"
    class Colorless

    1 {
        passives {
            StatMinimum 5
        }
    }
    2 {
        desc "PASSIVE_BAREMINIMUM2_DESC"

        passives {
            StatMinimum 7
        }
    }
}
```

---

### `Unrestricted`
**Name:** Unrestricted  
**Description:** Actions with a once per battle restriction can be cast once per turn instead.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_UNRESTRICTED2_DESC`: "Actions with a once per battle restriction can be cast once per turn instead. <br/> Actions with a once per turn restriction have a 50% chance to be castable again."

```
Unrestricted {
    name "PASSIVE_UNRESTRICTED_NAME"
    desc "PASSIVE_UNRESTRICTED_DESC"
    class Colorless

    1 {
        passives {
            RemoveOncePerFightRestriction 1
        }
    }
    2 {
        desc "PASSIVE_UNRESTRICTED2_DESC"

        passives {
            RemoveOncePerFightRestriction 1
            AbilityChargeRefundChance {
                chance 50%
                advantage_softcap 3.5
            }
        }
    }
}
```

---

### `DeathsDoor`
**Name:** Death's Door  
**Description:** While you're at 1 HP, your spells cost 1 mana, but can only be cast once per turn.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_DEATHSDOOR2_DESC`: "While you're at 5 or fewer HP, your spells cost 1 mana, but can only be cast once per turn."

```
DeathsDoor {
    name "PASSIVE_DEATHSDOOR_NAME"
    desc "PASSIVE_DEATHSDOOR_DESC"
    class Colorless

    1 {
        passives {
            PassiveAtHealthThreshold {
                threshold 1
                mode equal

                passives {
                    SetSpellCosts 1
                    MakeSpellsRequireCharge 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_DEATHSDOOR2_DESC"

        passives {
            PassiveAtHealthThreshold {
                threshold 5
                mode less_or_equal

                passives {
                    SetSpellCosts 1
                    MakeSpellsRequireCharge 1
                }
            }
        }
    }
}
```

---

### `OverConfident`
**Name:** Overconfident  
**Description:** While at full HP, reduce the cost of your spells by 2, but take double damage. This can't reduce mana costs to less than 1.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_OVERCONFIDENT2_DESC`: "While at full HP, reduce the cost of your spells by 2, but take double damage.  This can't reduce mana costs to less than 1. When you cast a spell, heal 1 HP."

```
OverConfident {
    name "PASSIVE_OVERCONFIDENT_NAME"
    desc "PASSIVE_OVERCONFIDENT_DESC"
    class Colorless

    1 {
        passives {
            PassiveAtFullHealth {
                ManaCostReduction 2
                TakeExtraDamage 200%
            }
        }
    }
    2 {
        desc "PASSIVE_OVERCONFIDENT2_DESC"

        passives {
            PassiveAtFullHealth {
                ManaCostReduction 2
                TakeExtraDamage 200%
            }
            StatusOnCastSpell {
                HealthGain 1
            }
        }
    }
}
```

---

### `SerialKiller`
**Name:** Serial Killer  
**Description:** After you kill 3 units, gain +6 [img:spd] and backstabs have 100% crit chance.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_SERIALKILLER2_DESC`: "After you kill 3 units, gain +6 [img:spd], backstabs have 100% crit chance, and gain an extra basic attack each turn."

```
SerialKiller {
    name "PASSIVE_SERIALKILLER_NAME"
    desc "PASSIVE_SERIALKILLER_DESC"
    class Colorless

    1 {
        passives {
            PassiveAfterXKills {
                stacks 3

                passives {
                    SpeedUp 6
                    BackstabCritChance 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_SERIALKILLER2_DESC"

        passives {
            PassiveAfterXKills {
                stacks 3

                passives {
                    SpeedUp 6
                    BackstabCritChance 1
                    ExtraBasicAttacks 1
                }
            }
        }
    }
}
```

---

### `StrengthInNumbers`
**Name:** Strength in Numbers  
**Description:** Your familiars have +1 Damage for each other familiar you have.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_STRENGTHINNUMBERS2_DESC`: "You and your familiars have +1 Damage for each other familiar you have."

```
StrengthInNumbers {
    name "PASSIVE_STRENGTHINNUMBERS_NAME"
    desc "PASSIVE_STRENGTHINNUMBERS_DESC"
    class Colorless

    1 {
        passives {
            StrengthInNumbersAura 1
        }
    }
    2 {
        desc "PASSIVE_STRENGTHINNUMBERS2_DESC"

        passives {
            StrengthInNumbersAura {
                stacks 1
                count_self true
            }
        }
    }
}
```

---

### `FightersSoul`
**Name:** Fighter's Soul  
**Description:** Fighter abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_FIGHTERSOUL2_DESC`: "Fighter abilities are offered when you level up."

```
FightersSoul {
    name "PASSIVE_FIGHTERSOUL_NAME"
    desc "PASSIVE_FIGHTERSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Fighter
        }

        stats {
            str 2
            spd 1
            int -1
        }
    }
    2 {
        desc "PASSIVE_FIGHTERSOUL2_DESC"

        passives {
            MulticlassLevelUp Fighter
        }

        stats {
            str 4
            spd 2
            int -2
        }
    }
}
```

---

### `HuntersSoul`
**Name:** Hunter's Soul  
**Description:** Hunter abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_HUNTERSOUL2_DESC`: "Hunter abilities are offered when you level up."

```
HuntersSoul {
    name "PASSIVE_HUNTERSOUL_NAME"
    desc "PASSIVE_HUNTERSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Hunter
        }

        stats {
            dex 3
            lck 2
            con -1
            spd -2
        }
    }
    2 {
        desc "PASSIVE_HUNTERSOUL2_DESC"

        passives {
            MulticlassLevelUp Hunter
        }

        stats {
            dex 6
            lck 4
            con -2
            spd -4
        }
    }
}
```

---

### `MagesSoul`
**Name:** Mage's Soul  
**Description:** Mage abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_MAGESOUL2_DESC`: "Mage abilities are offered when you level up."

```
MagesSoul {
    name "PASSIVE_MAGESOUL_NAME"
    desc "PASSIVE_MAGESOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Mage
        }

        stats {
            int 2
            cha 2
            con -1
            str -1
        }
    }
    2 {
        desc "PASSIVE_MAGESOUL2_DESC"

        passives {
            MulticlassLevelUp Mage
        }

        stats {
            int 4
            cha 4
            con -2
            str -2
        }
    }
}
```

---

### `ClericsSoul`
**Name:** Cleric's Soul  
**Description:** Cleric abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_CLERICSOUL2_DESC`: "Cleric abilities are offered when you level up."

```
ClericsSoul {
    name "PASSIVE_CLERICSOUL_NAME"
    desc "PASSIVE_CLERICSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Medic
        }

        stats {
            cha 2
            con 2
            spd -1
            dex -1
        }
    }
    2 {
        desc "PASSIVE_CLERICSOUL2_DESC"

        passives {
            MulticlassLevelUp Medic
        }

        stats {
            cha 4
            con 4
            spd -2
            dex -2
        }
    }
}
```

---

### `TanksSoul`
**Name:** Tank's Soul  
**Description:** Tank abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_TANKSOUL2_DESC`: "Tank abilities are offered when you level up."

```
TanksSoul {
    name "PASSIVE_TANKSOUL_NAME"
    desc "PASSIVE_TANKSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Tank
        }

        stats {
            con 4
            int -1
            dex -1
        }
    }
    2 {
        desc "PASSIVE_TANKSOUL2_DESC"

        passives {
            MulticlassLevelUp Tank
        }

        stats {
            con 8
            int -2
            dex -2
        }
    }
}
```

---

### `ThiefsSoul`
**Name:** Thief's Soul  
**Description:** Thief abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_THIEFSOUL2_DESC`: "Thief abilities are offered when you level up."

```
ThiefsSoul {
    name "PASSIVE_THIEFSOUL_NAME"
    desc "PASSIVE_THIEFSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Thief
        }

        stats {
            spd 4
            lck 1
            str -1
            con -1
        }
    }
    2 {
        desc "PASSIVE_THIEFSOUL2_DESC"

        passives {
            MulticlassLevelUp Thief
        }

        stats {
            spd 8
            lck 2
            str -2
            con -2
        }
    }
}
```

---

### `MonksSoul`
**Name:** Monk's Soul  
**Description:** Monk abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_MONKSOUL2_DESC`: "Monk abilities are offered when you level up."

```
MonksSoul {
    name "PASSIVE_MONKSOUL_NAME"
    desc "PASSIVE_MONKSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Monk
        }

        stats {
            int 2
            cha 2
            str -1
            dex -1
        }
    }
    2 {
        desc "PASSIVE_MONKSOUL2_DESC"

        passives {
            MulticlassLevelUp Monk
        }

        stats {
            int 4
            cha 4
            str -2
            dex -2
        }
    }
}
```

---

### `ButchersSoul`
**Name:** Butcher's Soul  
**Description:** Butcher abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_BUTCHERSOUL2_DESC`: "Butcher abilities are offered when you level up."

```
ButchersSoul {
    name "PASSIVE_BUTCHERSOUL_NAME"
    desc "PASSIVE_BUTCHERSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Butcher
        }

        stats {
            con 3
            str 2
            spd -2
        }
    }
    2 {
        desc "PASSIVE_BUTCHERSOUL2_DESC"

        passives {
            MulticlassLevelUp Butcher
        }

        stats {
            con 6
            str 4
            spd -4
        }
    }
}
```

---

### `DruidsSoul`
**Name:** Druid's Soul  
**Description:** Druid abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_DRUIDSOUL2_DESC`: "Druid abilities are offered when you level up."

```
DruidsSoul {
    name "PASSIVE_DRUIDSOUL_NAME"
    desc "PASSIVE_DRUIDSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Druid
        }

        stats {
            cha 3
            lck 1
            con -2
        }
    }
    2 {
        desc "PASSIVE_DRUIDSOUL2_DESC"

        passives {
            MulticlassLevelUp Druid
        }

        stats {
            cha 6
            lck 2
            con -4
        }
    }
}
```

---

### `TinkerersSoul`
**Name:** Tinkerer's Soul  
**Description:** Tinkerer abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_TINKERERSOUL2_DESC`: "Tinkerer abilities are offered when you level up."

```
TinkerersSoul {
    name "PASSIVE_TINKERERSOUL_NAME"
    desc "PASSIVE_TINKERERSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Tinkerer
        }

        stats {
            int 4
            lck -1
            cha -1
        }
    }
    2 {
        desc "PASSIVE_TINKERERSOUL2_DESC"

        passives {
            MulticlassLevelUp Tinkerer
        }

        stats {
            int 8
            lck -2
            cha -2
        }
    }
}
```

---

### `NecromancersSoul`
**Name:** Necromancer's Soul  
**Description:** Necromancer abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_NECROMANCERSOUL2_DESC`: "Necromancer abilities are offered when you level up."

```
NecromancersSoul {
    name "PASSIVE_NECROMANCERSOUL_NAME"
    desc "PASSIVE_NECROMANCERSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Necromancer
        }

        stats {
            con 2
            cha 1
            str -2
        }
    }
    2 {
        desc "PASSIVE_NECROMANCERSOUL2_DESC"

        passives {
            MulticlassLevelUp Necromancer
        }

        stats {
            con 4
            cha 2
            str -4
        }
    }
}
```

---

### `PsychicsSoul`
**Name:** Psychic's Soul  
**Description:** Psychic abilities are offered when you level up.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_PSYCHICSOUL2_DESC`: "Psychic abilities are offered when you level up."

```
PsychicsSoul {
    name "PASSIVE_PSYCHICSOUL_NAME"
    desc "PASSIVE_PSYCHICSOUL_DESC"
    class Colorless

    1 {
        passives {
            MulticlassLevelUp Psychic
        }

        stats {
            int 1
            cha 1
            spd 1
            con -1
        }
    }
    2 {
        desc "PASSIVE_PSYCHICSOUL2_DESC"

        passives {
            MulticlassLevelUp Psychic
        }

        stats {
            int 2
            cha 2
            spd 2
            con -2
        }
    }
}
```

---

### `Charming`
**Name:** Charming  
**Description:** You have a 25% chance to inflict Charm on units that damage you.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_CHARMING2_DESC`: "You have a 40% chance to inflict Charm on units that damage you."

```
Charming {
    name "PASSIVE_CHARMING_NAME"
    desc "PASSIVE_CHARMING_DESC"
    class Colorless

    1 {
        passives {
            RevengeDamage {
                effects {
                    Charmed [1, .25]
                }
            }
        }

        stats {
            cha 1
        }
    }
    2 {
        desc "PASSIVE_CHARMING2_DESC"

        passives {
            RevengeDamage {
                effects {
                    Charmed [1, .40]
                }
            }
        }

        stats {
            cha 2
        }
    }
}
```

---

### `FirstImpression`
**Name:** First Impression  
**Description:** Start each battle with +1 Bonus Attack.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_FIRSTIMPRESSION2_DESC`: "Start each battle with +2 Bonus Attacks and +2 Bonus Moves."

```
FirstImpression {
    name "PASSIVE_FIRSTIMPRESSION_NAME"
    desc "PASSIVE_FIRSTIMPRESSION_DESC"
    class Colorless

    1 {
        passives {
            Quivered 1
        }
    }
    2 {
        desc "PASSIVE_FIRSTIMPRESSION2_DESC"

        passives {
            Quivered 2
            MoveQuivered 2
        }
    }
}
```

---

### `Scavenger`
**Name:** Scavenger  
**Description:** If your trinket slot is empty, equip a small consumable food item at the start of each battle.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_SCAVENGER2_DESC`: "If your trinket slot is empty, equip a big consumable food item at the start of each battle."

```
Scavenger {
    name "PASSIVE_SCAVENGER_NAME"
    desc "PASSIVE_SCAVENGER_DESC"
    class Colorless

    tags [noncopyable]

    1 {
        passives {
            EquipTemporaryItem FoodMedium
        }
    }
    2 {
        desc "PASSIVE_SCAVENGER2_DESC"

        passives {
            EquipTemporaryItem FoodBig
        }
    }
}
```

---

### `ZenkaiBoost`
**Name:** Zenkai Boost  
**Description:** If you end battle with 1 HP, gain +1 to a random stat permanently and start the next battle at full HP with All Stats Up 3.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_ZENKAIBOOST2_DESC`: "If you end battle with 1 HP, gain +1 to 3 random stats permanently and start the next battle at full HP with All Stats Up 3."

```
ZenkaiBoost {
    name "PASSIVE_ZENKAIBOOST_NAME"
    desc "PASSIVE_ZENKAIBOOST_DESC"
    class Colorless

    1 {
        passives {
            PassiveAtHealthThreshold {
                mode equal
                threshold 1

                passives {
                    StatusOnBattleEnd {
                        RandomPermanentStat 1

                        NextBattleStatus {
                            AllStatsUp 3
                            FullHeal 1
                        }
                    }
                }
            }
        }
    }
    2 {
        desc "PASSIVE_ZENKAIBOOST2_DESC"

        passives {
            PassiveAtHealthThreshold {
                mode equal
                threshold 1

                passives {
                    StatusOnBattleEnd {
                        RandomPermanentStat 3

                        NextBattleStatus {
                            AllStatsUp 3
                            FullHeal 1
                        }
                    }
                }
            }
        }
    }
}
```

---

### `Protection`
**Name:** Protection  
**Description:** PASSIVE_PROTECTION_DESC  
**Source:** `colorless_passives.gon`  

```
Protection {
    name "PASSIVE_PROTECTION_NAME"
    desc "PASSIVE_PROTECTION_DESC"
    class Colorless

    1 {
        divine_shield 1
    }
    2 {
        desc "PASSIVE_PROTECTION2_DESC"

        divine_shield 3
    }
}
```

---

### `Rockin`
**Name:** Rockin'  
**Description:** Spawn 4 small rocks at the start of each battle.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_ROCKIN2_DESC`: "Spawn 4 small rocks and 4 boulders at the start of each battle."

```
Rockin {
    name "PASSIVE_ROCKIN_NAME"
    desc "PASSIVE_ROCKIN_DESC"
    class Colorless

    1 {
        passives {
            SpawnOnBattleStart {
                object SmallRock
                number 4
            }
        }
    }
    2 {
        desc "PASSIVE_ROCKIN2_DESC"

        passives {
            SpawnOnBattleStart {
                object SmallRock
                number 4
            }
            SpawnOnBattleStart {
                object Boulder
                number 4
            }
        }
    }
}
```

---

### `Mania`
**Name:** Mania  
**Description:** 10% chance to restore all your mana at the start of your turn.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_MANIA2_DESC`: "25% chance to restore all your mana at the start of your turn."

```
Mania {
    name "PASSIVE_MANIA_NAME"
    desc "PASSIVE_MANIA_DESC"
    class Colorless

    1 {
        passives {
            StatusEachTurnBegin {
                FillMana [1 .10]
            }
        }
    }
    2 {
        desc "PASSIVE_MANIA2_DESC"

        passives {
            StatusEachTurnBegin {
                FillMana [1 .25]
            }
        }
    }
}
```

---

### `Lucky`
**Name:** Lucky  
**Description:** PASSIVE_LUCKY_DESC  
**Source:** `colorless_passives.gon`  

```
Lucky {
    name "PASSIVE_LUCKY_NAME"
    desc "PASSIVE_LUCKY_DESC"
    class Colorless

    1 {
        stats {
            lck 4
        }
    }
    2 {
        desc "PASSIVE_LUCKY2_DESC"

        stats {
            lck 7
        }
    }
}
```

---

### `OneEighty`
**Name:** 180  
**Description:** When you use your basic attack, turn around and use it again.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_1802_DESC`: "When you use your basic attack, turn around and use it again. <br/> Your basic attack inflicts Confusion 1."

```
OneEighty { //moved from Fighter
    name "PASSIVE_180_NAME"
    desc "PASSIVE_180_DESC"
    class Colorless

    1 {
        passives {
            StatusOnUseBasicAttack {
                FlippedFacingForceAttack 1
            }
        }
    }
    2 {
        desc "PASSIVE_1802_DESC"
        passives {
            StatusOnUseBasicAttack {
                FlippedFacingForceAttack 1
            }
            AddStatusToBasicAttack {
                Confusion 1
            }
        }
    }
}
```

---

### `JestersSoul`
**Name:** Jester's Soul  
**Description:** Abilities from any class are offered when you level up.
You can reroll your level up options twice.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_JESTERSSOUL2_DESC`: "Abilities from any class are offered when you level up. <br/> You can reroll your level up options twice."

```
JestersSoul {
    name "PASSIVE_JESTERSSOUL_NAME"
    desc "PASSIVE_JESTERSSOUL_DESC"
    class Colorless

    1 {
        passives {
            LevelUpClassOverride Jester
            AddLevelUpRerolls 2
        }
    }
    2 {
        desc "PASSIVE_JESTERSSOUL2_DESC"

        passives {
            LevelUpClassOverride Jester
            AddLevelUpRerolls 2
        }

        stats {
            str 2
            dex 2
            con 2
            int 2
            cha 2
            spd 2
            lck 2
        }
    }
}
```

---

### `HotBlooded`
**Name:** Hot-Blooded  
**Description:** Burn you inflict is increased by 1.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_HOTBLOODED2_DESC`: "Burn you inflict is increased by 2."

```
HotBlooded { 
    name "PASSIVE_HOTBLOODED_NAME"
    desc "PASSIVE_HOTBLOODED_DESC"
    class Colorless

    1 {
        passives {
            AmplifyStatus Burn
        }
    }
    2 {
        desc "PASSIVE_HOTBLOODED2_DESC"

        passives {
            AmplifyStatus {
                status Burn
                addstacks 2
            }
        }
    }
}
```

---

### `ToxicBlooded`
**Name:** Toxic-Blooded  
**Description:** Poison you inflict is increased by 1.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_TOXICBLOODED2_DESC`: "Poison you inflict is increased by 2."

```
ToxicBlooded { 
    name "PASSIVE_TOXICBLOODED_NAME"
    desc "PASSIVE_TOXICBLOODED_DESC"
    class Colorless

    1 {
        passives {
            AmplifyStatus Poison
        }
    }
    2 {
        desc "PASSIVE_TOXICBLOODED2_DESC"

        passives {
            AmplifyStatus {
                status Poison
                addstacks 2
            }
        }
    }
}
```

---

### `BloodBlooded`
**Name:** Blood-Blooded  
**Description:** Bleed you inflict is increased by 1.  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_BLOODBLOODED2_DESC`: "Bleed you inflict is increased by 2."

```
BloodBlooded { 
    name "PASSIVE_BLOODBLOODED_NAME"
    desc "PASSIVE_BLOODBLOODED_DESC"
    class Colorless

    1 {
        passives {
            AmplifyStatus Bleed
        }
    }
    2 {
        desc "PASSIVE_BLOODBLOODED2_DESC"

        passives {
            AmplifyStatus {
                status Bleed
                addstacks 2
            }
        }
    }
}
```

---

### `VoidSoul`
**Name:** Void Soul  
**Description:** Only upgraded Collarless abilities are offered when you level up  
**Source:** `colorless_passives.gon`  

**Localization Strings:**
- `PASSIVE_VOIDSOUL2_DESC`: "Only upgraded Collarless abilities are offered when you level up. Collarless spells cost 1 less mana."

```
VoidSoul {
    name "PASSIVE_VOIDSOUL_NAME"
    desc "PASSIVE_VOIDSOUL_DESC"

    1 {
        passives {
            LevelUpClassOverride Colorless
            UpgradeLevelUpClassActives Colorless
            UpgradeLevelUpClassPassives Colorless
        }
    }

    2 {
        desc "PASSIVE_VOIDSOUL2_DESC"

        passives {
            LevelUpClassOverride Colorless
            UpgradeLevelUpClassActives Colorless
            UpgradeLevelUpClassPassives Colorless

            ClassManaCostReduction {
			    class Colorless
                reduction 1
            }
        }
    }
}
```

---

## File: `disorders.gon`

### `Rabies`
**Name:** Rabies  
**Description:** Your basic attack is a melee attack. You can't equip face armor.
After each battle, gain +2 [img:str] and -1 [img:int].
If your [img:int] is 0 or less, you have Madness.  
**Source:** `disorders.gon`  

```
Rabies {
    name "DISORDER_RABIES_NAME"
    desc "DISORDER_RABIES_DESC"
    class Disorder

    lock_item_slot {
        slot face
        frame 11
    }

    override_basic_attack BasicMelee 

    passives {
        StatusOnBattleEnd {
            PermanentStrength 2
            PermanentIntelligence -1
            even_if_dead true
        }

        PassiveAtStatThreshold {
            mode less_or_equal
            threshold {
                int 0
            }
            passives {
                PermanentMadness 1
            }
        }

        AddStatusToBasicMeleeAttack {
            SpreadDisease {
                chance 25%
                disease Rabies
            }
        }

        OverrideBasicAttack BasicMelee
    }
}
```

---

### `Boils`
**Name:** Boils  
**Description:** +1 Brace.
You spawn a puddle of creep whenever you get hit. You can't equip face armor.  
**Source:** `disorders.gon`  

```
Boils {
    name "DISORDER_BOILS_NAME"
    desc "DISORDER_BOILS_DESC"
    class Disorder

    lock_item_slot {
        slot face
        frame 16
    }

    stats {
        cha -2
    }

    passives {
        SpawnCreepOnHit 1
        Brace 1
    }
}
```

---

### `Depression`
**Name:** Depression  
**Description:** Adjacent units get All Stats Down 2.  
**Source:** `disorders.gon`  

```
Depression {
    name "DISORDER_DEPRESSION_NAME"
    desc "DISORDER_DEPRESSION_DESC"
    class Disorder

    stats {
        str -1
        dex -1
        con -1
        int -1
        spd -1
        cha -1
        lck -1
    }

    passives {
        AllStatsUp -1
        DepressionAura 2
    }
}
```

---

### `BrokenLimb`
**Name:** Broken Limb  
**Description:** You can't equip trinkets or consumables. +2 Thorns.  
**Source:** `disorders.gon`  

```
BrokenLimb {
    name "DISORDER_BROKENLIMB_NAME"
    desc "DISORDER_BROKENLIMB_DESC"
    class Disorder

    lock_item_slot {
        slot trinket
    }

    stats {
        spd -2
    }
	
	passives {
		Thorns 2
    }
}
```

---

### `WrenchedNeck`
**Name:** Wrenched Neck  
**Description:** You can't equip neck armor. Double the effects of your head armor.  
**Source:** `disorders.gon`  

```
WrenchedNeck {
    name "DISORDER_WRENCHEDNECK_NAME"
    desc "DISORDER_WRENCHEDNECK_DESC"
    class Disorder

    lock_item_slot {
        slot neck
    }

    stats {
        con -1
        dex -1
    }
	
	passives {
		HeadArmorPassiveMultiplierBonus 1
	}
}
```

---

### `Declawed`
**Name:** Declawed  
**Description:** You can't equip weapons.  
**Source:** `disorders.gon`  

```
Declawed {
    name "DISORDER_DECLAWED_NAME"
    desc "DISORDER_DECLAWED_DESC"
    class Disorder

    lock_item_slot {
        slot weapon
    }

    stats {
        str -3
        cha 2
    }
}
```

---

### `HeadTrauma`
**Name:** Head Trauma  
**Description:** You can't equip head armor. Your Collarless spells cost -2 mana.  
**Source:** `disorders.gon`  

```
HeadTrauma {
    name "DISORDER_HEADTRAUMA_NAME"
    desc "DISORDER_HEADTRAUMA_DESC"
    class Disorder

    lock_item_slot {
        slot head
    }

    stats {
        int -3
    }
	
    passives {
        ClassManaCostReduction {
            class Colorless
            reduction 2
        }
    }
}
```

---

### `DeepCut`
**Name:** Deep Cut  
**Description:** Bleed 1.
You can't equip trinkets or consumables. 
Bonus ability: Bloodzerk.  
**Source:** `disorders.gon`  

```
DeepCut {
    name "DISORDER_DEEPCUT_NAME"
    desc "DISORDER_DEEPCUT_DESC"
    class Disorder

    lock_item_slot {
        slot trinket
    }

    stats {
        con -2
    }

    passives {
        Bleed 1
        BonusAbility Bloodzerk
    }
}
```

---

### `PuncturedEye`
**Name:** Punctured Eye  
**Description:** +10% miss chance.
You can't equip face armor. Gain an eyeball trinket.  
**Source:** `disorders.gon`  

```
PuncturedEye {
    name "DISORDER_PUNCTUREDEYE_NAME"
    desc "DISORDER_PUNCTUREDEYE_DESC"
    class Disorder

    lock_item_slot {
        slot face
    }

    bonus_items [Eyeball]

    passives {
        MissChance 10
    }
}
```

---

### `OCD`
**Name:** Obsessive Compulsive Disorder  
**Description:** Bonus Ability: Groom
At the end of your turn, if you didn't use Groom, take 2 damage.  
**Source:** `disorders.gon`  

```
OCD {
    name "DISORDER_OCD_NAME"
    desc "DISORDER_OCD_DESC"
    class Disorder

    passives {
        DamageIfDidntUseSpecificAbility {
            ability Groom
            damage 2
        }
        BonusAbility Groom
    }
}
```

---

### `Distemper`
**Name:** Distemper  
**Description:** At the end of each battle gain +10% crit chance, +25% crit damage, and +5% miss chance. Permanently.
You can't equip face armor.  
**Source:** `disorders.gon`  

**Localization Strings:**
- `DISORDER_DISTEMPERMAX_DESC`: "+50% Miss Chance, +100% Crit Chance, +250% Crit Damage. <br/> Your movement action is used randomly each turn."

```
Distemper {
    name "DISORDER_DISTEMPER_NAME"
    desc "DISORDER_DISTEMPER_DESC"
    auto_plus_signs_on_name false
    class Disorder

    lock_item_slot {
        slot face
        frame 17
    }

    1 {
        passives {
            MissChance 5
            CritChanceUp 10
			AddCritMultiplier 25%
            PassiveLevelUpAtCombatEnd 1
        }
    }

    2 {
        passives {
            MissChance 10
            CritChanceUp 20
			AddCritMultiplier 50%
            PassiveLevelUpAtCombatEnd 1
        }
    }

    3 {
        passives {
            MissChance 15
            CritChanceUp 30
			AddCritMultiplier 75%
            PassiveLevelUpAtCombatEnd 1
        }
    }

    4 {
        passives {
            MissChance 20
            CritChanceUp 40
			AddCritMultiplier 100%
            PassiveLevelUpAtCombatEnd 1
        }
    }

    5 {
        passives {
            MissChance 25
            CritChanceUp 50
			AddCritMultiplier 125%
            PassiveLevelUpAtCombatEnd 1
        }
    }

    6 {
        passives {
            MissChance 30
            CritChanceUp 60
			AddCritMultiplier 150%
            PassiveLevelUpAtCombatEnd 1
        }
    }

    7 {
        passives {
            MissChance 35
            CritChanceUp 70
			AddCritMultiplier 175%
            PassiveLevelUpAtCombatEnd 1
        }
    }

    8 {
        passives {
            MissChance 40
            CritChanceUp 80
			AddCritMultiplier 200%
            PassiveLevelUpAtCombatEnd 1
        }
    }

    9 {
        passives {
            MissChance 45
            CritChanceUp 90
			AddCritMultiplier 225%
            PassiveLevelUpAtCombatEnd 1
        }
    }

    10 {
        desc "DISORDER_DISTEMPERMAX_DESC"

        passives {
            MissChance 50
            CritChanceUp 100
			AddCritMultiplier 250%
            MoveRandomly 1
        }
    }
}
```

---

### `BrainDamage`
**Name:** Brain Damage  
**Description:** You can't use item actions. +2 Brace.  
**Source:** `disorders.gon`  

```
BrainDamage {
    name "DISORDER_BRAINDAMAGE_NAME"
    desc "DISORDER_BRAINDAMAGE_DESC"
    class Disorder

    passives {
        DisableAbilities all_items
		Brace 2
    }
}
```

---

### `SeveredThumb`
**Name:** Severed Thumb  
**Description:** You can't equip weapons. Spawn a Food pickup at the start of each battle.  
**Source:** `disorders.gon`  

```
SeveredThumb {
    name "DISORDER_SEVEREDTHUMB_NAME"
    desc "DISORDER_SEVEREDTHUMB_DESC"
    class Disorder

    lock_item_slot {
        slot weapon
    }
	
    passives {
		AbilityOnBattleStart neck_ChefsApron
    }
}
```

---

### `PTSD`
**Name:** Post-Traumatic Stress Disorder  
**Description:** When you take damage, gain Fear and +2 Damage.  
**Source:** `disorders.gon`  

```
PTSD {
    name "DISORDER_PTSD_NAME"
    desc "DISORDER_PTSD_DESC"
    class Disorder

    passives {
        StatusOnTookDamage {
            Conditional_HasStatus {
                status Fear
            } Else {
                Fear 1
            }
            DamageUp 2
        }
    }
}
```

---

### `IBS`
**Name:** Irritable Bowel Syndrome  
**Description:** When you take damage, poop.  
**Source:** `disorders.gon`  

```
IBS {
    name "DISORDER_IBS_NAME"
    desc "DISORDER_IBS_DESC"
    class Disorder

    passives {
        PoopWhenHit Poop
    }
}
```

---

### `Dyskinesia`
**Name:** Dyskinesia  
**Description:** When you end your movement, knockback all adjacent units 1 tile.  
**Source:** `disorders.gon`  

```
Dyskinesia {
    name "DISORDER_DYSKINESIA_NAME"
    desc "DISORDER_DYSKINESIA_DESC"
    class Disorder

    passives {
        DamageNeighborsOnEndMove {
            type status
            damage 0
            knockback 1
        }
    }
}
```

---

### `Anemia`
**Name:** Anemia  
**Description:** When you take damage, you have a 10% chance to gain Bleed 1.
Gain 2 Charge for each damage you take from Bleed.  
**Source:** `disorders.gon`  

```
Anemia {
    name "DISORDER_ANEMIA_NAME"
    desc "DISORDER_ANEMIA_DESC"
    class Disorder

    passives {
        AddStatusToReceivedDamage_ExcludeStatuses {
            Conditional_DoesDamage {
                Bleed [1 .1]
            }
        }
        ScaledStatusOnBleedDamage {
            Charge 2
        }
    }
}
```

---

### `Empath`
**Name:** Empath  
**Description:** Take 1 damage when you deal damage.
Your heals heal for 1 extra.  
**Source:** `disorders.gon`  

```
Empath {
    name "DISORDER_EMPATH_NAME"
    desc "DISORDER_EMPATH_DESC"
    class Disorder

    passives {
        SelfDamageWhenDealDamage {
            type status
            damage 1
        }
        BoostHeals 1
    }
}
```

---

### `Infestation`
**Name:** Infestation  
**Description:** At the start of your turn, you have a 50% chance to spawn a Maggot Familiar and 15% chance to spawn an enemy Flea.  
**Source:** `disorders.gon`  

```
Infestation {
    name "DISORDER_INFESTATION_NAME"
    desc "DISORDER_INFESTATION_DESC"
    class Disorder

    passives {
        SpawnEachTurn {
            chance 15%
            object Flea
            good false
        }
        SpawnEachTurn {
            chance 50%
            object CharmedMaggot
        }
    }
}
```

---

### `Leprosy`
**Name:** Leprosy  
**Description:** Bruise 2. When you get hit, spawn a food pickup.  
**Source:** `disorders.gon`  

```
Leprosy {
    name "DISORDER_LEPROSY_NAME"
    desc "DISORDER_LEPROSY_DESC"
    class Disorder

    passives {
        Bruise 2
        SpawnThingOnDamage {
            object Food
            good true
        }
    }
}
```

---

### `ASRFight`
**Name:** Acute Stress Reaction: Fight  
**Description:** Gain +6 [img:str] while you have 5 or fewer HP.  
**Source:** `disorders.gon`  

```
ASRFight {
    name "DISORDER_ASRFIGHT_NAME"
    desc "DISORDER_ASRFIGHT_DESC"
    class Disorder

    stats {
        spd -2
    }

    passives {
        StatsAtLowHealth {
            threshold 5
            strength 6
        }
    }
}
```

---

### `ASRFlight`
**Name:** Acute Stress Reaction: Flight  
**Description:** Gain +6 [img:spd] while you have 5 or fewer HP.  
**Source:** `disorders.gon`  

```
ASRFlight {
    name "DISORDER_ASRFLIGHT_NAME"
    desc "DISORDER_ASRFLIGHT_DESC"
    class Disorder

    stats {
        str -2
    }

    passives {
        StatsAtLowHealth {
			threshold 5
            speed 6
        }
    }
}
```

---

### `BloodFrenzy`
**Name:** Blood Frenzy  
**Description:** When you kill a unit, take an extra turn with Madness.  
**Source:** `disorders.gon`  

```
BloodFrenzy {
    name "DISORDER_BLOODFRENZY_NAME"
    desc "DISORDER_BLOODFRENZY_DESC"
    class Disorder

    passives {
        StatusOnKill {
            TakeBonusTurnWithStatus {
                Madness 1
            }
        }
    }
}
```

---

### `Shunned`
**Name:** Shunned  
**Description:** Take your turn last.
Your heals heal for 2 less. +15% dodge chance.  
**Source:** `disorders.gon`  

```
Shunned {
    name "DISORDER_SHUNNED_NAME"
    desc "DISORDER_SHUNNED_DESC"
    class Disorder

    passives {
        AddInitiative -100
        BoostHeals -2
        DodgeChance 15%
    }
}
```

---

### `Dysentery`
**Name:** Dysentery  
**Description:** 50% chance to make a burning poop directly behind you when you end your turn.  
**Source:** `disorders.gon`  

```
Dysentery {
    name "DISORDER_DYSENTERY_NAME"
    desc "DISORDER_DYSENTERY_DESC"
    class Disorder

    passives {
        //PoopOnTurnEnd 50%
        StatusEachTurnEnd {
            ForceUseAbility {
                chance .5
                ability DysenteryPoop
            }
        }
    }
}
```

---

### `Anxiety`
**Name:** Anxiety  
**Description:** +10% Dodge chance. When you take damage, run away from the source.  
**Source:** `disorders.gon`  

```
Anxiety {
    name "DISORDER_ANXIETY_NAME"
    desc "DISORDER_ANXIETY_DESC"
    class Disorder

    passives {
		DodgeChance 10%
        MoveWhenDamaged {
            weights stay_far_always_move
        }
    }
}
```

---

### `Kamikazee`
**Name:** Kamikaze  
**Description:** You explode when you are downed.  
**Source:** `disorders.gon`  

```
Kamikazee {
    name "DISORDER_KAMIKAZE_NAME"
    desc "DISORDER_KAMIKAZE_DESC"
    class Disorder

    passives {
        DeathRattle BoomerCatExplode
    }
}
```

---

### `Traumatophobia`
**Name:** Traumatophobia  
**Description:** Whenever you take damage, move 1 tile away from the source.  
**Source:** `disorders.gon`  

```
Traumatophobia {
    name "DISORDER_TRAUMATOPHOBIA_NAME"
    desc "DISORDER_TRAUMATOPHOBIA_DESC"
    class Disorder

    passives {
        MoveAwayFromDamageSource MoveOne
    }
}
```

---

### `StockholmSyndrome`
**Name:** Stockholm Syndrome  
**Description:** Whenever you take damage, move toward the source.  
**Source:** `disorders.gon`  

```
StockholmSyndrome {
    name "DISORDER_STOCKHOLMSYNDROME_NAME"
    desc "DISORDER_STOCKHOLMSYNDROME_DESC"
    class Disorder

    passives {
        MoveTowardsDamageSource {
            move_ability move
            move_far false
        }
    }
}
```

---

### `ViolentOutbursts`
**Name:** Violent Outbursts  
**Description:** When you end your turn, dash forward 2 tiles, attack with Knockback, and take 1 damage.  
**Source:** `disorders.gon`  

```
ViolentOutbursts {
    name "DISORDER_VIOLENTOUTBURSTS_NAME"
    desc "DISORDER_VIOLENTOUTBURSTS_DESC"
    class Disorder

    passives {
        AutocastEachTurn ViolentOutburst
    }
}
```

---

### `GamblingAddict`
**Name:** Gambling Addiction  
**Description:** +33% miss chance.
100% critical hit chance.  
**Source:** `disorders.gon`  

```
GamblingAddict {
    name "DISORDER_GAMBLINGADDICT_NAME"
    desc "DISORDER_GAMBLINGADDICT_DESC"
    class Disorder

    passives {
        MissChance 33
        CritChanceUp 100
    }
}
```

---

### `Scleroderma`
**Name:** Scleroderma  
**Description:** At the start of each battle, you lose all but 1 HP, but gain that much [img:shield].  
**Source:** `disorders.gon`  

```
Scleroderma {
    name "DISORDER_SCLERODERMA_NAME"
    desc "DISORDER_SCLERODERMA_DESC"
    class Disorder

    passives {
        Scleroderma 1
    }
}
```

---

### `Pacifist`
**Name:** Pacifist  
**Description:** You can't kill units. If you end your turn without using your basic attack gain 7 mana.  
**Source:** `disorders.gon`  

```
Pacifist {
    name "DISORDER_PACIFIST_NAME"
    desc "DISORDER_PACIFIST_DESC"
    class Disorder

    passives {
        AddStatusToAllDamage {
            NonLethal 1
        }
		
		StatusOnTurnEndIfDidntCastAbilityTypes {
			type attack
			ManaGain 7
		}
    }
}
```

---

### `Gigachad`
**Name:** GIGACHAD  
**Description:** DISORDER_GIGACHAD_DESC  
**Source:** `disorders.gon`  

```
Gigachad {
    name "DISORDER_GIGACHAD_NAME"
    desc "DISORDER_GIGACHAD_DESC"
    class Disorder

    stats {
        cha 8
        int -5
    }
}
```

---

### `ImposterSyndrome`
**Name:** Impostor Syndrome  
**Description:** You're quite suspicious…  
**Source:** `disorders.gon`  

```
ImposterSyndrome {
    name "DISORDER_IMPOSTERSYNDROME_NAME"
    desc "DISORDER_IMPOSTERSYNDROME_DESC"
    class Disorder

    passives {
        InvertBrainFaction 1
    }
}
```

---

### `Vegan`
**Name:** Vegan  
**Description:** You don't eat meat.  
**Source:** `disorders.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_VEGAN`: "{Catname} (Vegan)|999"

```
Vegan {
    name "DISORDER_VEGAN_NAME"
    desc "DISORDER_VEGAN_DESC"
    class Disorder

    name_mod "CAT_NAME_MOD_VEGAN"

    passives {
        Vegan 1
        HouseFoodRequirementMultiplier 0
        DisableAbilitiesWithTag meat
        BlacklistPickupType food
    }
}
```

---

### `FrozenKnee`
**Name:** The Zoomies  
**Description:** Your movement action is a dash attack.  
**Source:** `disorders.gon`  

```
FrozenKnee {
    name "DISORDER_ZOOMIES_NAME"
    desc "DISORDER_ZOOMIES_DESC"
    class Disorder

    passives {
        ReplaceBasicMove BasicDashAttackMove
    }
}
```

---

### `SchrodingerDisorder`
**Name:** Schrödinger's Syndrome  
**Description:** 50% chance to start each battle dead, or alive with max hp and All Stats Up 2 and an extra turn at the start of the battle.  
**Source:** `disorders.gon`  

```
SchrodingerDisorder {
    name "DISORDER_SCHRODINGERDISORDER_NAME"
    desc "DISORDER_SCHRODINGERDISORDER_DESC"
    class Disorder

    passives {
	    AllStatsUp 2
		AlphaTurns 1
        SchrodingerDisorder 50%
    }
}
```

---

### `ScalyScabs`
**Name:** Scaly Scabs  
**Description:** DISORDER_SCALYSCABS_DESC  
**Source:** `disorders.gon`  

```
ScalyScabs {
    name "DISORDER_SCALYSCABS_NAME"
    desc "DISORDER_SCALYSCABS_DESC"
    class Disorder

    shield 8
    stats {
        con -2
    }
}
```

---

### `FattyLiver`
**Name:** Fatty Liver  
**Description:** Whenever you lose HP, you permanently lose 1 [img:con].  
**Source:** `disorders.gon`  

```
FattyLiver {
    name "DISORDER_FATTYLIVER_NAME"
    desc "DISORDER_FATTYLIVER_DESC"
    class Disorder

    stats {
        con 8
    }
    passives {
        StatusOnTakeHealthDamage {
            PermanentConstitution -1
        }
    }
}
```

---

### `CommonCold`
**Name:** The Common Cold  
**Description:** Start each battle with All Stats Down. 30% chance of recovering at the end of each round. Contagious.  
**Source:** `disorders.gon`  

```
CommonCold {
    name "DISORDER_COMMONCOLD_NAME"
    desc "DISORDER_COMMONCOLD_DESC"
    class Disorder

    passives {
        AllStatsUp -1

        StatusOnBattleEnd {
            even_if_dead true
            CureDisease {
                chance 30%
                disease CommonCold
            }
        }

        DamageNeighborsOnEndMove {
            type status
            cant_miss true
            damage 0
            
            effects {
                SpreadDisease {
                    chance 50%
                    disease CommonCold
                    can_apply_to_anything true
                }
            }
        }

        AddStatusToBasicAttack {
            SpreadDisease {
                chance 50%
                disease CommonCold
                can_apply_to_anything true
            }
        }
    }
}
```

---

### `Pox`
**Name:** Pox  
**Description:** 10% chance to skip your turn to scratch yourself. Your basic attack has a 50% chance to inflict Poison 1. 5% chance of recovering at the end of each round. Contagious.  
**Source:** `disorders.gon`  

```
Pox {
    name "DISORDER_POX_NAME"
    desc "DISORDER_POX_DESC"
    class Disorder

    passives {
        AutocastEachTurnBegin {
            ability PoxScratch
            chance 10%
            advantage_polarity -1
        }

        StatusOnBattleEnd {
            even_if_dead true
            CureDisease {
                chance 5%
                disease Pox
            }
        }

        DamageNeighborsOnEndMove {
            type status
            cant_miss true
            damage 0
            
            effects {
                SpreadDisease {
                    chance 50%
                    disease Pox
                }
            }
        }

        AddStatusToBasicAttack {
            Poison [1 .5]
        }
    }
}
```

---

### `Psychosis`
**Name:** Psychosis  
**Description:** After your first turn, you have permanent madness.  
**Source:** `disorders.gon`  

```
Psychosis {
    name "DISORDER_PSYCHOSIS_NAME"
    desc "DISORDER_PSYCHOSIS_DESC"
    class Disorder

    stats {
        str 1
        int 1
        dex 1
        cha 1
        con 1
        lck 1
        spd 1
    }

    passives {
        SetDefaultFacePassive insane
        StatusEachTurnEnd {
            PermanentMadness 1
        }
        StatusIfBattleAlreadyBegan {
            PermanentMadness 1
        }
    }
}
```

---

### `Necrosis`
**Name:** Necrosis  
**Description:** When you take damage, you get -1 [img:con], -1 [img:str], and spawn poisoned food.  
**Source:** `disorders.gon`  

```
Necrosis {
    name "DISORDER_NECROSIS_NAME"
    desc "DISORDER_NECROSIS_DESC"
    class Disorder

    stats {
        str 2
        con 2
    }

    passives {
        SpawnThingOnDamage {
            object PoisonFood
            consider_all_layers true
        }
        StatusOnTookDamage {
            StrengthUp -1
            ConstitutionUp -1
        }
    }
}
```

---

### `Touched`
**Name:** Touched  
**Description:** You can no longer heal HP.  
**Source:** `disorders.gon`  

```
Touched {
    name "DISORDER_TOUCHED_NAME"
    desc "DISORDER_TOUCHED_DESC"
    class Disorder

    stats {
        str 3
        int 3
        dex 3
        cha 3
        con 3
        lck 3
        spd 3
    }

    passives {
        HPGainBlock 1
    }
}
```

---

### `Charred`
**Name:** Charred  
**Description:** Bruise 1. You cannot be Burned.  
**Source:** `disorders.gon`  

```
Charred {
    name "DISORDER_CHARRED_NAME"
    desc "DISORDER_CHARRED_DESC"
    class Disorder

    shield 4

    passives {
	    StatusImmunity Burn
        Bruise 1
    }
}
```

---

### `Invincible`
**Name:** Immortal  
**Description:** All damage you take is reduced to 1.
When you take damage, suffer a random injury.  
**Source:** `disorders.gon`  

```
Invincible {
    name "DISORDER_IMMORTAL_NAME"
    desc "DISORDER_IMMORTAL_DESC"
    class Disorder

    passives {
        LimitDamage 1
        StatusOnTookDamage {
            RandomInjury 1
        }
    }
}
```

---

### `ExplosiveGas`
**Name:** Bad Gas  
**Description:** On the first round, take your turn last. At the start of that turn, do a Mega Fart attack that inflicts Poison 2.  
**Source:** `disorders.gon`  

```
ExplosiveGas {
    name "DISORDER_BADGAS_NAME"
    desc "DISORDER_BADGAS_DESC"
    class Disorder

    passives {
        AbilityOnBattleStart MegaFart
        TempInitiativeChange -999
    }
}
```

---

### `Toxoplasmosis`
**Name:** Toxoplasmosis  
**Description:** Start each battle with a Rat Familiar. Your basic attack charms Rat enemies.  
**Source:** `disorders.gon`  

```
Toxoplasmosis {
    name "DISORDER_TOXOPLASMOSIS_NAME"
    desc "DISORDER_TOXOPLASMOSIS_DESC"
    class Disorder

    stats {
        con -1
        int -1
    }

    passives {
		SpawnOnBattleStart {
            object CharmedRat
        }
        AddStatusToBasicAttack {
            Conditional_HasTag {
                tag rat
                Charmed 1
            }
            SpreadDisease {
                disease Toxoplasmosis
            }
        }
    }
    //TODO: make this spread to enemy cats.
}
```

---

### `Ebola`
**Name:** Ebola  
**Description:** Start each battle with Bleed 3. Your basic attack inflicts Bleed 2.
5% chance of recovering at the end of each round. Contagious.  
**Source:** `disorders.gon`  

```
Ebola {
    name "DISORDER_EBOLA_NAME"
    desc "DISORDER_EBOLA_DESC"
    class Disorder

    passives {
        Bleed 3
        AddStatusToBasicAttack {
            Bleed 2
        }

        StatusOnBattleEnd {
            even_if_dead true
            CureDisease {
                chance 5%
                disease Ebola
            }
        }

        DamageNeighborsOnEndMove {
            type status
            cant_miss true
            damage 0
            
            effects {
                SpreadDisease {
                    chance 25%
                    disease Ebola
                    can_apply_to_anything true
                }
            }
        }
        MeleeRevengeDamage {
            effects {
                SpreadDisease {
                    chance 100%
                    disease Ebola
                    can_apply_to_anything true
                }
            }
        }
    }
}
```

---

### `Fidgety`
**Name:** Fidgety  
**Description:** When you end your turn, automatically use your weapon on a random unit in range, for free.  
**Source:** `disorders.gon`  

```
Fidgety {
    name "DISORDER_FIDGETY_NAME"
    desc "DISORDER_FIDGETY_DESC"
    class Disorder

    passives {
        StatusEachTurnEnd {
            UseAbility_Madness weapon
        }
    }
}
```

---

### `Narcolepsy`
**Name:** Narcolepsy  
**Description:** At the end of your turn, fall asleep, heal 10 HP and gain 7 mana.  
**Source:** `disorders.gon`  

```
Narcolepsy {
    name "DISORDER_NARCOLEPSY_NAME"
    desc "DISORDER_NARCOLEPSY_DESC"
    class Disorder

    passives {
		AddManaRegen 7
        StatusEachTurnEnd {
            ForceUseAbility Rest
        }
    }
}
```

---

### `Paranoia`
**Name:** Paranoia  
**Description:** When a unit ends its movement directly behind you, attack it and gain Fear.  
**Source:** `disorders.gon`  

```
Paranoia {
    name "DISORDER_PARANOIA_NAME"
    desc "DISORDER_PARANOIA_DESC"
    class Disorder

    passives {
        Paranoia ParanoiaBasicMelee
    }
}
```

---

### `EatingDisorder`
**Name:** Eating Disorder  
**Description:** Double the effects of your consumables but you are confused on how to eat them.  
**Source:** `disorders.gon`  

```
EatingDisorder {
    name "DISORDER_EATINGDISORDER_NAME"
    desc "DISORDER_EATINGDISORDER_DESC"
    class Disorder

    passives {
        ConsumableEffectsMultiplierBonus 1
        ConfusionEffectOnTaggedAbilities consumable
    }
}
```

---

### `Gastritis`
**Name:** Gastritis  
**Description:** At the end of your turn, fart and Poison all adjacent units.  
**Source:** `disorders.gon`  

```
Gastritis {
    name "DISORDER_GASTRITIS_NAME"
    desc "DISORDER_GASTRITIS_DESC"
    class Disorder

    passives {
        StatusEachTurnEnd {
            ForceUseAbility MiniFart
        }
    }
}
```

---

### `Hypomania`
**Name:** Hypomania  
**Description:** Start each battle with 3 bonus turns, then never take a turn.  
**Source:** `disorders.gon`  

```
Hypomania {
    name "DISORDER_HYPOMANIA_NAME"
    desc "DISORDER_HYPOMANIA_DESC"
    class Disorder

    passives {
        Hypomania 3
    }
}
```

---

### `Hypersomnia`
**Name:** Hypersomnia  
**Description:** Start each battle asleep and with full health.  
**Source:** `disorders.gon`  

```
Hypersomnia {
    name "DISORDER_HYPERSOMNIA_NAME"
    desc "DISORDER_HYPERSOMNIA_DESC"
    class Disorder

    passives {
        StatusOnBattleStart {
            Sleep 1
        }
        FullHeal 1
    }
}
```

---

### `KidneyStones`
**Name:** Kidney Stone  
**Description:** When you end your turn take 1 damage and pass a kidney stone.  
**Source:** `disorders.gon`  

```
KidneyStones {
    name "DISORDER_KIDNEYSTONE_NAME"
    desc "DISORDER_KIDNEYSTONE_DESC"
    class Disorder

    passives {
        StatusEachTurnEnd {
            ForceUseAbility KidneyStone
        }
    }
}
```

---

### `Cancer`
**Name:** Cancer  
**Description:** At the end of each battle, lose 3 random stats permanently and gain a random mutation.  
**Source:** `disorders.gon`  

```
Cancer {
    name "DISORDER_CANCER_NAME"
    desc "DISORDER_CANCER_DESC"
    class Disorder

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

### `Stinky`
**Name:** Stinky  
**Description:** Adjacent units move away from you at the start of their turns.  
**Source:** `disorders.gon`  

```
Stinky {
    name "DISORDER_STINKY_NAME"
    desc "DISORDER_STINKY_DESC"
    class Disorder

    passives {
        StatusAdjacentOnTheirTurnBegin {
            ForceMoveAway {
                free false //consume the move point
            }
        }
    }
}
```

---

### `Incontinence`
**Name:** Incontinence  
**Description:** When you take damage, pee yourself.  
**Source:** `disorders.gon`  

```
Incontinence {
    name "DISORDER_INCONTINENCE_NAME"
    desc "DISORDER_INCONTINENCE_DESC"
    class Disorder

    passives {
        AbilityReaction PissYourself
    }
}
```

---

### `Fossilized`
**Name:** Fossilized  
**Description:** +2 Brace. Slide like a rock whenever you get hit.  
**Source:** `disorders.gon`  

```
Fossilized {
    name "DISORDER_FOSSILIZED_NAME"
    desc "DISORDER_FOSSILIZED_DESC"
    class Disorder

    passives {
        Brace 2
        SmallRockBehavior 5
        LimitSelfKnockbackDamage 1
        AddTag rock
    }
}
```

---

### `Triskaidekaphobia`
**Name:** Triskaidekaphobia  
**Description:** Your spells cost 0 mana. The 13th spell you cast on an adventure kills you and destroys your body.  
**Source:** `disorders.gon`  

```
Triskaidekaphobia {
    name "DISORDER_TRISKAIDEKAPHOBIA_NAME"
    desc "DISORDER_TRISKAIDEKAPHOBIA_DESC"
    auto_plus_signs_on_name false
    class Disorder

    passives {
        SetSpellCosts 0
        Triskaidekaphobia 13
    }
}
```

---

### `Autism`
**Name:** Autism  
**Description:** Spells you were born with cost -2 mana. Other spells cost +1 mana.  
**Source:** `disorders.gon`  

```
Autism {
    name "DISORDER_AUTISM_NAME"
    desc "DISORDER_AUTISM_DESC"
    class Disorder

    stats {
        cha -2
        int 2
    }
    passives {
        Autism {
            innate -2
            learned 1
        }
    }
}
```

---

### `Tourettes`
**Name:** Tourette's Syndrome  
**Description:** At the start of your turn, you have a 33% chance to cast one of your spells at a random target for free.  
**Source:** `disorders.gon`  

```
Tourettes {
    name "DISORDER_TOURETTES_NAME"
    desc "DISORDER_TOURETTES_DESC"
    class Disorder

    passives {
        TourettesMeows {
            cooldown [8 15]
            pool [Hit Hiss Normal]
        }

        StatusEachTurnBegin {
            Conditional_GoodRoll {
                odds 33%
                UseRandomSpell_Madness 1
            }
        }
    }
}
```

---

### `Albinism`
**Name:** Albinism  
**Description:** Fire damage you take inflicts +3 Burn.
Your basic attack has a 25% chance to inflict Fear.  
**Source:** `disorders.gon`  

```
Albinism {
    name "DISORDER_ALBINISM_NAME"
    desc "DISORDER_ALBINISM_DESC"
    class Disorder

    passives {
        OverridePalette 87

        AddStatusToBasicAttack {
            Fear [1 .25]
        }
        AddStatusesToReceivedElementalDamage {
            elements [Heat Fire]
            Burn 3
        }
        AddStatusesIfPersistentWeatherElement {
            elements [Heat Fire]
            Burn 3
        }
    }
}
```

---

### `SleepParalysis`
**Name:** Sleep Paralysis  
**Description:** When you fall asleep, a Sleep Paralysis Demon with Madness spawns! You can't wake up until it's killed.
Learn the spell Rest (if you have a free spell slot).  
**Source:** `disorders.gon`  

```
SleepParalysis {
    name "DISORDER_SLEEPPARALYSIS_NAME"
    desc "DISORDER_SLEEPPARALYSIS_DESC"
    class Disorder

    grant_ability Rest

    passives {
        ReceivedStatusReplacement [Sleep SleepParalysis]
    }
}
```

---

### `Diabetes`
**Name:** Diabetes  
**Description:** When you end your turn, if you haven't eaten food, gain All Stats Down and Confusion 1. Each time you eat food, cleanse all your debuffs and gain +1 [img:int].  
**Source:** `disorders.gon`  

```
Diabetes {
    name "DISORDER_DIABETES_NAME"
    desc "DISORDER_DIABETES_DESC"
    class Disorder

    passives {
        Diabetes {
            AllStatsUp -1
            Confusion 1
        }
        StatusOnEatFood {
            Cleanse 0
			IntelligenceUp 1
        }
    }
}
```

---

### `Bipolar`
**Name:** Bipolar Disorder  
**Description:** Start each battle with either
 +5 [img:int], +5 [img:cha], and +5 [img:spd]
or 
All Stats Down 2.  
**Source:** `disorders.gon`  

```
Bipolar {
    name "DISORDER_BIPOLARDISORDER_NAME"
    desc "DISORDER_BIPOLARDISORDER_DESC"
    class Disorder

    passives {
        RandomPassivePool {
            PassiveGroup {
                IntelligenceUp 5
                CharismaUp 5
                SpeedUp 5
                SetDefaultFace happy
            }
            PassiveGroup {
                AllStatsUp -2
                SetDefaultFace sad
            }
        }
    }
}
```

---

### `Soulless`
**Name:** Soulless  
**Description:** You are immune to buffs and debuffs. When you die, you don't leave a corpse.  
**Source:** `disorders.gon`  

```
Soulless {
    name "DISORDER_SOULLESS_NAME"
    desc "DISORDER_SOULLESS_DESC"
    class Disorder

    passives {
        DebuffImmunity 1
        BuffImmunity 1
        AddCorpseHealth -999999
    }
}
```

---

### `Premonitions`
**Name:** The Shining  
**Description:** Your attacks can't miss.
+15% dodge chance and +15% chance to gain Fear at the start of each turn.  
**Source:** `disorders.gon`  

```
Premonitions {
    name "DISORDER_THESHINING_NAME"
    desc "DISORDER_THESHINING_DESC"
    class Disorder

    passives {
        MaxAccuracy 1
        DodgeChance 15%
        StatusEachTurnBegin {
            Fear [1 .15]
        }
    }
}
```

---

### `PillPopper`
**Name:** Addict  
**Description:** Start each battle with All Stats Down 2.
Gain All Stats Up 3 whenever you eat a pill.
You have a 50% chance to find a pill at the end of each battle.  
**Source:** `disorders.gon`  

```
PillPopper {
    name "DISORDER_PILLPOPPER_NAME"
    desc "DISORDER_PILLPOPPER_DESC"
    class Disorder

    passives {
        AllStatsUp -2
        StatusOnBattleEnd {
            FindItemFromPool {
                chance .5
                pool pills
            }
        }
        StatusOnEatPill {
            AllStatsUp 3
        }
    }
}
```

---

### `BorrowedTime`
**Name:** Borrowed Time  
**Description:** +50% dodge chance. Doomed 3.  
**Source:** `disorders.gon`  

```
BorrowedTime {
    name "DISORDER_BORROWEDTIME_NAME"
    desc "DISORDER_BORROWEDTIME_DESC"
    class Disorder

    passives {
        DodgeChance 50%
        Doomed 3
    }
}
```

---

### `Brave`
**Name:** Brave  
**Description:** Take your turn earlier.
Immune to Fear and Madness.
Attacks against you never miss.  
**Source:** `disorders.gon`  

```
Brave {
    name "DISORDER_BRAVE_NAME"
    desc "DISORDER_BRAVE_DESC"
    class Disorder

    passives {
        AddInitiative 999
        StatusImmunity [Fear Madness PermanentMadness]
        CantDodge 1
    }
}
```

---

### `Scatological`
**Name:** Scatological  
**Description:** Heal 5 HP when you damage poop.
At the start of your turn, if you're near poop, you automatically move toward it and eat it.  
**Source:** `disorders.gon`  

```
Scatological {
    name "DISORDER_SCATOLOGICAL_NAME"
    desc "DISORDER_SCATOLOGICAL_DESC"
    class Disorder

    passives {
        MoveAndUseAbilityEachTurnBeginIfPossible EatShit
        AddStatusToAllDamage {
            Conditional_HasTag {
                tag poop
                FlatLeechIfDamaged 5
            }
        }
    }
}
```

---

### `Cannibal`
**Name:** Necrophage  
**Description:** At the start of your turn, if there's a dead body near you, move towards it and eat it to gain All Stats Up and heal 4 HP.  
**Source:** `disorders.gon`  

```
Cannibal {
    name "DISORDER_NECROPHAGE_NAME"
    desc "DISORDER_NECROPHAGE_DESC"
    class Disorder

    passives {
        MoveAndUseAbilityEachTurnBeginIfPossible Cannibalize
    }
}
```

---

### `CrohnsDisease`
**Name:** Crohn's Disease  
**Description:** At the end of your turn, you have a 20% chance to poop all over the place!  
**Source:** `disorders.gon`  

```
CrohnsDisease {
    name "DISORDER_CROHNSDISEASE_NAME"
    desc "DISORDER_CROHNSDISEASE_DESC"
    class Disorder

    passives {
        StatusEachTurnEnd {
            ForceUseAbility {
                chance .2
                ability CrohnsPoop
            }
        }
    }
}
```

---

### `Pica`
**Name:** Pica  
**Description:** When you collect a coin or scrap pickup, heal instead of gaining the pickup's normal effect.  
**Source:** `disorders.gon`  

```
Pica {
    name "DISORDER_PICA_NAME"
    desc "DISORDER_PICA_DESC"
    class Disorder

    passives {
        TaggedPickupEffectReplacement {
            tag money

            HealthGain 3*X //3 health per coin
        }
        TaggedPickupEffectReplacement {
            tag scrap

            HealthGain 2*X //2 health per shield
        }
    }
}
```

---

### `FelineAids`
**Name:** Feline Aids  
**Description:** Your basic attack inflicts Poison 3 and Weakness 1.
Inflict Poison 3 and Weakness 1 on units that contact you.
Gain -1 [img:con] and -1 [img:spd] at the end of each battle permanently.  
**Source:** `disorders.gon`  

```
FelineAids {
    name "DISORDER_FELINEAIDS_NAME"
    desc "DISORDER_FELINEAIDS_DESC"
    class Disorder

    passives {
        AddStatusToBasicAttack {
            Poison 3
            Weakness 1

            SpreadDisease {
                chance 5%
                disease FelineAids
            }
        }
        MeleeRevengeDamage {
            Poison 3
            Weakness 1

            SpreadDisease {
                chance 5%
                disease FelineAids
            }
        }
        StatusOnBattleEnd {
            even_if_dead true
            
            PermanentConstitution -1
            PermanentSpeed -1
        }
    }
}
```

---

### `Dyslexia`
**Name:** Dyslexia  
**Description:** Swap 3's and 5's in the mana costs and damage values of your spells while in a battle. 6's and 9's are also swapped.  
**Source:** `disorders.gon`  

```
Dyslexia {
    name "DISORDER_DYSLEXIA_NAME"
    desc "DISORDER_DYSLEXIA_DESC"
    class Disorder

    passives {
        Dyslexia [3 5]
        Dyslexia [6 9]
    }
}
```

---

### `Covid`
**Name:** Covid  
**Description:** Start each battle with All Stats Down, Poison 1, and Weakness 1.
Your basic attack inflicts Poison 1 and Weakness 1.
15% chance of recovering at the end of each round. Contagious.  
**Source:** `disorders.gon`  

```
Covid {
    name "DISORDER_COVID_NAME"
    desc "DISORDER_COVID_DESC"
    class Disorder

    passives {
        AllStatsUp -1
        Poison 1
        Weakness 1

        StatusOnBattleEnd {
            even_if_dead true
            CureDisease {
                chance 15%
                disease Covid
                can_apply_to_anything true
            }
        }

        DamageNeighborsOnEndMove {
            type status
            cant_miss true
            damage 0
            
            effects {
                SpreadDisease {
                    chance 75%
                    disease Covid
                    can_apply_to_anything true
                }
            }
        }

        AddStatusToBasicAttack {
            Poison 1
            Weakness 1
        }
    }
}
```

---

### `Flu`
**Name:** The Flu  
**Description:** Start each battle with Slow 5 and Weakness 5.
Your basic attack inflicts Slow 1 and Weakness 1.
20% chance of recovering at the end of each round. Contagious.  
**Source:** `disorders.gon`  

```
Flu {
    name "DISORDER_THEFLU_NAME"
    desc "DISORDER_THEFLU_DESC"
    class Disorder

    passives {
        Slow 5
        Weakness 5

        StatusOnBattleEnd {
            even_if_dead true
            CureDisease {
                chance 20%
                disease Flu
            }
        }

        DamageNeighborsOnEndMove {
            type status
            cant_miss true
            damage 0
            
            effects {
                SpreadDisease {
                    chance 50%
                    disease Flu
                    can_apply_to_anything true
                }
            }
        }

        AddStatusToBasicAttack {
            Weakness 1
            Slow 1
        }
    }
}
```

---

### `BirdFlu`
**Name:** Bird Flu  
**Description:** Start each battle in Mockingbird Form.
You have a 20% chance to recover at the end of each battle.
Contagious.  
**Source:** `disorders.gon`  

```
BirdFlu {
    name "DISORDER_BIRDFLU_NAME"
    desc "DISORDER_BIRDFLU_DESC"
    class Disorder

    passives {
        //AbilityOnBattleStart MockingbirdForm
        ForceUseAbility MockingbirdForm

        StatusOnBattleEnd {
            even_if_dead true
            CureDisease {
                chance 20%
                disease BirdFlu
            }
        }

        DamageNeighborsOnEndMove {
            type status
            cant_miss true
            damage 0
            
            effects {
                SpreadDisease {
                    chance 50%
                    disease BirdFlu
                }
            }
        }
    }
}
```

---

### `Nudist`
**Name:** Nudist  
**Description:** +50% dodge chance.
You can't wear armor.  
**Source:** `disorders.gon`  

```
Nudist {
    name "DISORDER_NUDIST_NAME"
    desc "DISORDER_NUDIST_DESC"
    class Disorder

    lock_item_slot {
        slot [face head neck]
    }

    stats {
        spd 5
    }

    passives {
        DodgeChance 50%
    }
}
```

---

### `Elephantiasis`
**Name:** Elephantiasis  
**Description:** At the end of each battle, gain -1 [img:spd] and +2 starting [img:shield] permanently. After 8 battles, gain Trample.  
**Source:** `disorders.gon`  

```
Elephantiasis {
    name "DISORDER_ELEPHANTIASIS_NAME"
    desc "DISORDER_ELEPHANTIASIS_DESC"
    class Disorder
    auto_plus_signs_on_name false

    passives {
        StatusOnBattleEnd {
            even_if_dead true
            PermanentSpeed -1
        }
        PassiveLevelUpAtCombatEnd 1

        PassiveLevelScaledStatus {
            Shield "2*(X-1)"
            SizeScalePercent "sqrt(1.0+(.05*(X-1)))*100"

            Trample [3, X-8] //if X is 11 then the chance here switches from 0 to 1
        }
    }
}
```

---

### `Gigantism`
**Name:** Gigantism  
**Description:** Trample.  
**Source:** `disorders.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_GIGANTISM`: "Big {Catname}|2"

```
Gigantism {
    name "DISORDER_GIGANTISM_NAME"
    desc "DISORDER_GIGANTISM_DESC"
    class Disorder

    name_mod "CAT_NAME_MOD_GIGANTISM"

    stats {
        con 2
        str 2
        dex -2
        lck -2
        spd -2
    }

    passives {
        Trample 3
        SizeScale 1.3
    }
}
```

---

### `Dwarfism`
**Name:** Dwarfism  
**Description:** +10% dodge chance.  
**Source:** `disorders.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_DWARF`: "Little {Catname}|3"

```
Dwarfism {
    name "DISORDER_DWARFISM_NAME"
    desc "DISORDER_DWARFISM_DESC"
    class Disorder

    name_mod "CAT_NAME_MOD_DWARF"

    stats {
        con -2
        str -2
        dex 2
        lck 2
        spd 2
    }

    passives {
        DodgeChance 10%
        SizeScale .7
    }
}
```

---

### `PrimordialDwarf`
**Name:** Primordial Dwarf  
**Description:** DISORDER_PRIMORDIALDWARF_DESC  
**Source:** `disorders.gon`  

**Localization Strings:**
- `CAT_NAME_MOD_PDWARF`: "Lil' {Catname}|3"

```
PrimordialDwarf {
    name "DISORDER_PRIMORDIALDWARF_NAME"
    desc "DISORDER_PRIMORDIALDWARF_DESC"
    class Disorder

    name_mod "CAT_NAME_MOD_PDWARF"

    stats {
        lck 12
        str -2
        dex -2
        con -2
        spd -2
        int -2
        cha -2
    }

    passives {
        SizeScale .4
    }
}
```

---

### `Sociopathy`
**Name:** Sociopathy  
**Description:** You have Madness on your first turn.  
**Source:** `disorders.gon`  

```
Sociopathy {
    name "DISORDER_SOCIOPATHY_NAME"
    desc "DISORDER_SOCIOPATHY_DESC"
    class Disorder

    stats {
        cha 5
		int 5
    }

    passives {
        Madness 1
    }
}
```

---

### `SkillShare_Disorder`
**Name:** Munchausen by Proxy  
**Description:** If you have a 2nd disorder, all other cats in your party gain it at the start of each battle.  
**Source:** `disorders.gon`  

```
SkillShare_Disorder { //todo: this one needs to synergize with butcher Schaendefreude and fix how it works with dyslexia
    name "DISORDER_SKILLSHAREDISORDER_NAME"
    desc "DISORDER_SKILLSHAREDISORDER_DESC"
    class Disorder

    passives {
        //hard coded just like skill share
    }
}
```

---

### `Schizophrenia`
**Name:** Schizophrenia  
**Description:** At the end of your turn, spawn a hallucination. It has Madness, attacks any unit except you, and fades after its turn.  
**Source:** `disorders.gon`  

```
Schizophrenia {
    name "DISORDER_SCHIZOPHRENIA_NAME"
    desc "DISORDER_SCHIZOPHRENIA_DESC"
    class Disorder

    passives {
        StatusEachTurnEnd {
            ForceUseAbility Hallucinate_Disorder
        }
    }
}
```

---

### `Lycanthropy`
**Name:** Lycanthropy  
**Description:** 33% chance to enter Wolf Form at the start of your turn.  
**Source:** `disorders.gon`  

```
Lycanthropy {
    name "DISORDER_LYCANTHROPY_NAME"
    desc "DISORDER_LYCANTHROPY_DESC"
    class Disorder

    passives {
        StatusEachTurnBegin {
            ForceUseAbility {
                ability TigerForm
                chance 33%
            }
        }
    }
}
```

---

### `WobblyCat`
**Name:** Wobbly Cat Syndrome  
**Description:** 25% chance to block attacks and get knocked back 10 tiles instead.  
**Source:** `disorders.gon`  

```
WobblyCat {
    name "DISORDER_WOBBLYCATSYNDROME_NAME"
    desc "DISORDER_WOBBLYCATSYNDROME_DESC"
    class Disorder

    stats {
        dex -3
    }

    passives {
        WobblyCat 25%
    }
}
```

---

### `Singleton`
**Name:** Singleton  
**Description:** Your max HP and mana are reduced to 1.
Damage you take is reduced to 1.
Your spells cost 1 mana.  
**Source:** `disorders.gon`  

```
Singleton {
    name "DISORDER_SINGLETON_NAME"
    desc "DISORDER_SINGLETON_DESC"
    class Disorder

    passives {
        OverrideMaxHealth 1
        OverrideMaxMana 1
        StrictLimitDamage 1
        LimitHeal 1
        SetSpellCosts 1
    }
}
```

---

### `Insomnia`
**Name:** Insomnia  
**Description:** You can't fall asleep.
You can move an extra time each turn. Exhaustion sets in on round 3.  
**Source:** `disorders.gon`  

```
Insomnia {
    name "DISORDER_INSOMNIA_NAME"
    desc "DISORDER_INSOMNIA_DESC"
    class Disorder

    passives {
		ExtraBasicMoves_Status 1
        StatusImmunity [Sleep SleepParalysis]
        ExhaustionRoundChange 3
    }
}
```

---

### `Phony`
**Name:** Phony  
**Description:** Start each battle with full mana.
You can't regenerate mana.  
**Source:** `disorders.gon`  

```
Phony {
    name "DISORDER_PHONY_NAME"
    desc "DISORDER_PHONY_DESC"
    class Disorder

    stats {
        cha 2
    }

    passives {
        NoManaRegen 1
        MaxStartingMana 1
    }
}
```

---

### `AcidReflux`
**Name:** Acid Reflux  
**Description:** Your basic attack becomes a lobbed shot with splash damage but deals 2 damage to you.  
**Source:** `disorders.gon`  

```
AcidReflux {
    name "DISORDER_ACIDREFLUX_NAME"
    desc "DISORDER_ACIDREFLUX_DESC"
    class Disorder

    override_basic_attack GerdShot

    passives {
        OverrideBasicAttack GerdShot
    }
}
```

---

### `SpontaneousCombustion`
**Name:** Spontaneous Combustion  
**Description:** When you take damage from an ability, you have a 15% chance to inflict Burn 5 on yourself and adjacent units.  
**Source:** `disorders.gon`  

```
SpontaneousCombustion {
    name "DISORDER_SPONTANEOUSCOMBUSTION_NAME"
    desc "DISORDER_SPONTANEOUSCOMBUSTION_DESC"
    class Disorder

    passives {
        AbilityReaction {
            chance 15%
            ability_damage_only true
            ability SpontaneouslyCombust
        }
    }
}
```

---

### `TheHunger`
**Name:** The Hunger  
**Description:** Your basic attack has lifesteal.
If you don't deal damage to a unit on your turn, gain Madness 1.  
**Source:** `disorders.gon`  

```
TheHunger {
    name "DISORDER_THEHUNGER_NAME"
    desc "DISORDER_THEHUNGER_DESC"
    class Disorder

    passives {
        AddStatusToBasicAttack {
            Leech 1
        }
        TheHunger {
            Madness 1
        }
    }
}
```

---

### `Paralyzed`
**Name:** Paraplegic  
**Description:** The range of all your movement, dash, and jump abilities are capped at 1 unless they teleport.
Enemies won't prioritize attacking you.  
**Source:** `disorders.gon`  

```
Paralyzed {
    name "DISORDER_PARAPELEGIC_NAME"
    desc "DISORDER_PARAPELEGIC_DESC"
    class Disorder

    stats {
        int 2
    }

    passives {
        CapMovementAbilityRange 1
        ChangeTauntPriority -1
        MoveSpeedMultiplier .5
		
    }
}
```

---

### `GlassBones`
**Name:** Osteogenesis Imperfecta  
**Description:** +2 Bruise, +2 Bleed Thorns, and +2 Thorns.
When you're downed, you get injured an extra time.  
**Source:** `disorders.gon`  

```
GlassBones {
    name "DISORDER_OSTEOGENESISIMPERFECTA_NAME"
    desc "DISORDER_OSTEOGENESISIMPERFECTA_DESC"
    class Disorder

    passives {
        BleedThorns 2
        Thorns 2
        Bruise 2
        ExtraInjuryOnDeath 1
    }
}
```

---

### `Gargantuan`
**Name:** Gargantuan  
**Description:** You are permanently immobile.  
**Source:** `disorders.gon`  

```
Gargantuan { //Given by a MonkeyPaw event wish.
    name "DISORDER_GARGANTUAN_NAME"
    desc "DISORDER_GARGANTUAN_DESC"
    class Disorder

    stats {
        con 5
        str 10
        spd -10
    }

    passives {
        SizeScale 1.65
        PermanentImmobile 1
    }
}
```

---

### `BrainDead`
**Name:** Brain Dead  
**Description:** Gain twice as many stats when you level up. +1 Reroll when leveling up.  
**Source:** `disorders.gon`  

```
BrainDead { //Given by a MonkeyPaw event wish.
    name "DISORDER_BRAINDEAD_NAME"
    desc "DISORDER_BRAINDEAD_DESC"
    class Disorder
    
    stats {
        cha -5
        int -10
    }

    passives {
        AddLevelUpRerolls 1
        AddLevelUpStatMultiplier 1
    }
}
```

---

### `TamperedGenes`
**Name:** Tainted Genes  
**Description:** At the end of each battle gain a random mutation. When you're downed, your corpse is destroyed.  
**Source:** `disorders.gon`  

```
TamperedGenes { //Given by a MonkeyPaw event wish.
    name "DISORDER_TAMPEREDGENES_NAME"
    desc "DISORDER_TAMPEREDGENES_DESC"
    class Disorder

    passives {
        AddCorpseHealth -999999
        SpawnThingOnDeath ZombieCatFamiliar
        StatusOnBattleEnd {
            RandomMutation 1
        }
    }
}
```

---

### `SensoryOverloadFace`
**Name:** Sensory Overload  
**Description:** All but your face slot is locked. Your face item's effects are tripled!  
**Source:** `disorders.gon`  

```
SensoryOverloadFace { //Given by a MonkeyPaw event wish.
    name "DISORDER_SENSORYOVERLOAD_NAME"
    desc "DISORDER_SENSORYOVERLOADFACE_DESC"
    class Disorder

    lock_item_slot {
        slot [head neck trinket weapon]
    }
    
    passives {
        FaceArmorPassiveMultiplierBonus 2
    }
}
```

---

### `SensoryOverloadTrinket`
**Name:** Sensory Overload  
**Description:** All but your trinket slot is locked. Your trinket's effects are tripled!  
**Source:** `disorders.gon`  

```
SensoryOverloadTrinket { //Given by a MonkeyPaw event wish.
    name "DISORDER_SENSORYOVERLOAD_NAME"
    desc "DISORDER_SENSORYOVERLOADTRINKET_DESC"
    class Disorder

    lock_item_slot {
        slot [face head neck weapon]
    }
    
    passives {
        TrinketPassiveMultiplierBonus 2
        TrinketActiveEffectsMultiplierBonus 2
    }
}
```

---

### `SensoryOverloadHead`
**Name:** Sensory Overload  
**Description:** All but your head slot is locked. Your head item's effects are tripled!  
**Source:** `disorders.gon`  

```
SensoryOverloadHead { //Given by a MonkeyPaw event wish.
    name "DISORDER_SENSORYOVERLOAD_NAME"
    desc "DISORDER_SENSORYOVERLOADHEAD_DESC"
    class Disorder

    lock_item_slot {
        slot [face trinket neck weapon]
    }
    
    passives {
        HeadArmorPassiveMultiplierBonus 2
    }
}
```

---

### `SensoryOverloadNeck`
**Name:** Sensory Overload  
**Description:** All but your neck slot is locked. Your neck item's effects are tripled!  
**Source:** `disorders.gon`  

```
SensoryOverloadNeck { //Given by a MonkeyPaw event wish.
    name "DISORDER_SENSORYOVERLOAD_NAME"
    desc "DISORDER_SENSORYOVERLOADNECK_DESC"
    class Disorder

    lock_item_slot {
        slot [face head trinket weapon]
    }
    
    passives {
        NeckArmorPassiveMultiplierBonus 2
    }
}
```

---

### `SensoryOverloadWeapon`
**Name:** Sensory Overload  
**Description:** All but your weapon slot is locked. Your weapon's effects are tripled!  
**Source:** `disorders.gon`  

```
SensoryOverloadWeapon { //Given by a MonkeyPaw event wish.
    name "DISORDER_SENSORYOVERLOAD_NAME"
    desc "DISORDER_SENSORYOVERLOADWEAPON_DESC"
    class Disorder

    lock_item_slot {
        slot [face head neck trinket]
    }
    
    passives {
        WeaponPassiveMultiplierBonus 2
        WeaponActiveEffectsMultiplierBonus 2
    }
}
```

---

### `EternalYouth`
**Name:** Eternal Youth  
**Description:** You are a kitten... forever!
+1 [img:comfort], +1 [img:stimulation], +1 [img:appeal]  
**Source:** `disorders.gon`  

```
EternalYouth { //Given by the fountain event
    name "DISORDER_ETERNALYOUTH_NAME"
    desc "DISORDER_ETERNALYOUTH_DESC"
    class Disorder

    passives {
        PermanentKitten 1
        ChangeTauntPriority -1

        FurnitureStats {
            Comfort 1
            Stimulation 1
            Appeal 1
        }
    }
}
```

---

### `DejaVu`
**Name:** Deja Vu  
**Description:** 10% chance to cancel actions.
[s:.7]Deja Vu will go away when this cat returns to the house.\[/s\]  
**Source:** `disorders.gon`  

**Localization Strings:**
- `DISORDER_SEVEREDEJAVU_NAME`: "Severe Deja Vu"
- `DISORDER_SEVEREDEJAVU_DESC`: "Steven has control of you now. <br/> [s:.7]Deja Vu will go away when this cat returns to the house.\[/s\]"

```
DejaVu {
    name "DISORDER_DEJAVU_NAME"
    auto_plus_signs_on_name false
    class Disorder

    1 {
        desc "DISORDER_DEJAVU_DESC"
        passives {
            DejaVu 10%
        }
    }
    2 {
        desc "DISORDER_DEJAVU_DESC"
        icon DejaVu2

        passives {
            DejaVu 10%
        }
    }
    3 {
        name "DISORDER_SEVEREDEJAVU_NAME"
        desc "DISORDER_SEVEREDEJAVU_DESC"
        icon DejaVu3

        passives {
            ReplaceBrain {
                brain GenericBrain
                decision_weights default
                move_weights keep_distance
            }
        }
    }
}
```

---

### `DownsSyndrome`
**Name:** Down's Syndrome  
**Description:** DISORDER_DOWNSSYNDROME_DESC  
**Source:** `disorders.gon`  

```
DownsSyndrome {//might be cool to make the head larger but keep the face the same size
    name "DISORDER_DOWNSSYNDROME_NAME"
    desc "DISORDER_DOWNSSYNDROME_DESC"
    class Disorder

    stats {
        con 3
        int -8
        cha 7
    }
}
```

---

### `Tachysensia`
**Name:** Tachysensia  
**Description:** DISORDER_TACHYSENSIA_DESC  
**Source:** `disorders.gon`  

```
Tachysensia {
    name "DISORDER_TACHYSENSIA_NAME"
    desc "DISORDER_TACHYSENSIA_DESC"
    class Disorder
		
	stats {
		str -3
		dex -3
		spd 8
	}
}
```

---

### `SavantSyndrome`
**Name:** Savant Syndrome  
**Description:** DISORDER_SAVANTSYNDROME_DESC  
**Source:** `disorders.gon`  

```
SavantSyndrome {
    name "DISORDER_SAVANTSYNDROME_NAME"
    desc "DISORDER_SAVANTSYNDROME_DESC"
    class Disorder

    stats {
        int 12
        str -2
        dex -2
        con -2
        spd -2
        cha -2
        lck -2
    }
}
```

---

### `WilliamsSyndrome`
**Name:** Williams Syndrome  
**Description:** Your attacks may Charm.  
**Source:** `disorders.gon`  

```
WilliamsSyndrome {//might be cool to make the mouth larger
    name "DISORDER_WILLIAMSSYNDROME_NAME"
    desc "DISORDER_WILLIAMSSYNDROME_DESC"
    class Disorder

    stats {
        int -5
        cha 10
	}
	
	passives {
        AddStatusToBasicAttack {
            Charmed [1 .25]
        }
	}
}
```

---

### `SpinaBifida`
**Name:** Spina Bifida  
**Description:** DISORDER_SPINABIFIDA_DESC  
**Source:** `disorders.gon`  

```
SpinaBifida {
    name "DISORDER_SPINABIFIDA_NAME"
    desc "DISORDER_SPINABIFIDA_DESC"
    class Disorder

    stats {
        dex 5
        spd -5
    }
}
```

---

### `DarkOne`
**Name:** Dark One  
**Description:** At end of your turn, deal 1 damage to all units and heal for the damage dealt. Whenever you down an ally gain All Stats Up.  
**Source:** `disorders.gon`  

```
DarkOne { //Aquired from Core event 'Demonic Idol'
    name "DISORDER_DARKONE_NAME"
    desc "DISORDER_DARKONE_DESC"
    class Disorder

    passives {
        AutocastEachTurn DarkOneStrike
        StatusKilledCharacters {
            Conditional_Ally {
                ApplyToSource {
                    AllStatsUp 1
                }
            }
        }
    }
}
```

---

### `ADHD`
**Name:** ADHD  
**Description:** You have 5 seconds to make decisions, or else this cat acts on its own.  
**Source:** `disorders.gon`  

```
ADHD {
    name "DISORDER_ADHD_NAME"
    desc "DISORDER_ADHD_DESC"
    class Disorder

    stats {
        spd 2
        int 1
    }

    passives {
        RealTimePressure_OneUnit 5
    }
}
```

---

### `FlamingFists`
**Name:** Flaming Fists  
**Description:** Your basic attacks inflict Burn 1. Start with Burn 1.  
**Source:** `disorders.gon`  

```
FlamingFists {
    name "DISORDER_FLAMINGFISTS_NAME"
    desc "DISORDER_FLAMINGFISTS_DESC"
    class Disorder

    passives {
        Burn 1
        AddStatusToBasicAttack {
            Burn 1
        }
    }
}
```

---

### `IntestinalProlapse`
**Name:** Intestinal Prolapse  
**Description:** You receive double damage from behind.  
**Source:** `disorders.gon`  

```
IntestinalProlapse {
    name "DISORDER_INTESTINALRPOLAPSE_NAME"
    desc "DISORDER_INTESTINALPROLAPSE_DESC"
    class Disorder

    passives {
        BackstabWeakness 0.75
    }
}
```

---

### `BlessingOfGlorg`
**Name:** Blessing of Glorg  
**Description:** You can unequip cursed items.  
**Source:** `disorders.gon`  

```
BlessingOfGlorg {
    name "DISORDER_BLESSINGOFGLORG_NAME"
    desc "DISORDER_BLESSINGOFGLORG_DESC"
    class Disorder

    stats {
        con -2
    }

    passives {
        CanRemoveCursedItems 1
    }
}
```

---

### `BlackFetin`
**Name:** Black Fetin  
**Description:** You have a 10% to be AI controlled each turn.
When an ally cat is downed, restore all your mana.  
**Source:** `disorders.gon`  

```
BlackFetin {
    name "DISORDER_BLACKFETIN_NAME"
    desc "DISORDER_BLACKFETIN_DESC"
    class Disorder

    passives {
		StatusOnAllyCatDeath {
			FillMana 1
		}
        StatusEachTurnBegin {
            Conditional_BadRoll {
                odds .1

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

### `OrangeFetin`
**Name:** Orange Fetin  
**Description:** You have a 10% to be AI controlled each turn.
When you kill an enemy, gain 3 mana and heal 2 hp.  
**Source:** `disorders.gon`  

```
OrangeFetin {
    name "DISORDER_ORANGEFETIN_NAME"
    desc "DISORDER_ORANGEFETIN_DESC"
    class Disorder

    passives {
		StatusOnKillEnemy {
			ManaGain 3
			HealthGain 2
		}
		StatusEachTurnBegin {
            Conditional_BadRoll {
                odds .1

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

### `PurpleFetin`
**Name:** Purple Fetin  
**Description:** You have a 10% to be AI controlled each turn.
You can reroll your level up options 3 times.  
**Source:** `disorders.gon`  

```
PurpleFetin {
    name "DISORDER_PURPLEFETIN_NAME"
    desc "DISORDER_PURPLEFETIN_DESC"
    class Disorder

    passives {
		AddLevelUpRerolls 3
        StatusEachTurnBegin {
            Conditional_BadRoll {
                odds .1

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

### `Chungus`
**Name:** Chungus  
**Description:** DISORDER_CHUNGUS_DESC  
**Source:** `disorders.gon`  

```
Chungus {
    name "DISORDER_CHUNGUS_NAME"
    desc "DISORDER_CHUNGUS_DESC"
    class Disorder

    stats {
        con 4
    }

    passives {
    }
}
```

---

## File: `druid_passives.gon`

### `SuperCrow`
**Name:** Super Crow!  
**Description:** Your crow has its abilities upgraded.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_SUPERCROW2_DESC`: "Your crow has its abilities upgraded… Twice!"

```
SuperCrow {
    name "PASSIVE_SUPERCROW_NAME"
    desc "PASSIVE_SUPERCROW_DESC"
    class Druid

    1 {
        passives {
            ReplaceSpawnedObjects [Crow2 Crow3] //in case you get it twice it should get you to crow3
            ReplaceSpawnedObjects [Crow Crow2]
        }
    }
    2 {
        desc "PASSIVE_SUPERCROW2_DESC"
        passives {
            ReplaceSpawnedObjects [Crow2 Crow3]
            ReplaceSpawnedObjects [Crow Crow3]
        }
    }
}
```

---

### `NaturesGuidance`
**Name:** Nature's Guidance  
**Description:** Allied familiars are immune to damage from tiles, knockback, thorns, and trample.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_NATUREGUIDANCE2_DESC`: "Allied familiars are immune to damage from tiles, knockback, thorns, and trample. <br/> Familiars you spawn gain +1 Holy Shield."

```
NaturesGuidance {
    name "PASSIVE_NATUREGUIDANCE_NAME"
    desc "PASSIVE_NATUREGUIDANCE_DESC"
    class Druid

    1 {
        passives {
            FamiliarSecondaryDamageImmunity 1
        }
    }
    2 {
        desc "PASSIVE_NATUREGUIDANCE2_DESC"
        passives {
            FamiliarSecondaryDamageImmunity 1
            AddPassivesToMinions {
                DivineShield 1
            }
        }
    }
}
```

---

### `PoisonIvy`
**Name:** Poison Ivy  
**Description:** You and familiar you spawn are Poisonous.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_POISONIVY2_DESC`: "You and familiar you spawn have Poisonous 2."

```
PoisonIvy {
    name "PASSIVE_POISONIVY_NAME"
    desc "PASSIVE_POISONIVY_DESC"
    class Druid

    1 {
        passives {
            PoisonThorns 1
            AddPassivesToMinions {
                PoisonThorns 1
            }
        }
    }
    2 {
        desc "PASSIVE_POISONIVY2_DESC"
        passives {
            PoisonThorns 2
            AddPassivesToMinions {
                PoisonThorns 2
            }
        }
        stats {
            con 2
        }
    }
}
```

---

### `Pathfinder`
**Name:** Pathfinder  
**Description:** Grass tiles are free to move through for you and familiars you spawn. Plant grass as you walk.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_PATHFINDER2_DESC`: "Grass tiles are free to move through for you and familiars you spawn. Gain +1 HP when moving through grass tiles. Plant grass as you walk."

```
Pathfinder {
    name "PASSIVE_PATHFINDER_NAME"
    desc "PASSIVE_PATHFINDER_DESC"
    class Druid

    1 {
        passives {
            FreePathfindElement Grass
            TileTrail GrassTile
            AddPassivesToMinions {
                FreePathfindElement Grass
            }
        }
    }
    2 {
        desc "PASSIVE_PATHFINDER2_DESC"
        passives {
            FreePathfindElement Grass
            GrassTileHealing 1
            TileTrail GrassTile
            AddPassivesToMinions {
                FreePathfindElement Grass
                GrassTileHealing 1
            }
        }
    }
}
```

---

### `EmptyVessels`
**Name:** Empty Vessels  
**Description:** Familiars you spawn have +3 Health Regeneration and +10 max health.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_EMPTYVESSEL2_DESC`: "Familiars you spawn have +3 Health Regeneration and uncapped HP."

```
EmptyVessels {
    name "PASSIVE_EMPTYVESSEL_NAME"
    desc "PASSIVE_EMPTYVESSEL_DESC"
    class Druid

    1 {
        passives {
            AddPassivesToMinions {
                HealthRegenUp 3
                AddUnfilledMaxHealth 10
            }
        }
    }
    2 {
        desc "PASSIVE_EMPTYVESSEL2_DESC"
        passives {
            AddPassivesToMinions {
                HealthRegenUp 3
                UncappedHP 1
            }
        }
    }
}
```

---

### `WildAnimals`
**Name:** Wild Animals  
**Description:** Familiars you spawn attack a random enemy within their range when they are spawned.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_WILDANIMALS2_DESC`: "Familiars you spawn attack a random enemy within their range when they're spawned, then they take an extra turn."

```
WildAnimals {
    name "PASSIVE_WILDANIMALS_NAME"
    desc "PASSIVE_WILDANIMALS_DESC"
    class Druid

    1 {
        passives {
            AddPassivesToMinions {
                ForceAttack 1
            }
        }
    }
    2 {
        desc "PASSIVE_WILDANIMALS2_DESC"
        passives {
            AddPassivesToMinions {
                ForceAttack 1
                TakeExtraTurn 1
            }
        }
    }
}
```

---

### `BarkSkin`
**Name:** Bark Skin  
**Description:** +1 Brace.
When you take damage, you get +1 temporary Brace until the start of your next turn.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_BARKSKIN2_DESC`: "+1 Brace. <br/> When you take damage, gain +2 temporary Brace and +2 temporary Thorns until the start of your next turn."

```
BarkSkin {
    name "PASSIVE_BARKSKIN_NAME"
    desc "PASSIVE_BARKSKIN_DESC"
    class Druid

    1 {
        passives {
            Brace 1
            StatusOnTookDamage {
                Temporary {
                    status Brace 
                    stacks 1
                    expires_on_begin_turn true
                }
            }
        }
    }
    2 {
        desc "PASSIVE_BARKSKIN2_DESC"
        passives {
            Brace 1
            StatusOnTookDamage {
                Temporary {
                    status Brace 
                    stacks 2
                    expires_on_begin_turn true
                }
                Temporary {
                    status Thorns 
                    stacks 2
                    expires_on_begin_turn true
                }
            }
        }
    }
}
```

---

### `SoothingSong`
**Name:** Love Song  
**Description:** Your basic action has +2 area, and heals 1 additional HP.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_LOVESONG2_DESC`: "Your basic action has +2 area, and heals 2 additional HP. The Damage your basic action grants lasts until the end of the battle."

```
SoothingSong {
    name "PASSIVE_LOVESONG_NAME"
    desc "PASSIVE_LOVESONG_DESC"
    class Druid

    1 {
        passives {
            BasicAttackAOEBonus 2
            AddDamageToBasicAttack 1
        }
    }
    2 {
        desc "PASSIVE_LOVESONG2_DESC"
        passives {
            BasicAttackAOEBonus 2
            AddDamageToBasicAttack 2

            BasicAttackStatusSwap [TempDamageUp DamageUp]
        }
    }
}
```

---

### `Teamwork`
**Name:** Teamwork  
**Description:** When one of your familiars kills something, all allies get +1 Damage.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_TEAMWORK2_DESC`: "When one of your familiars kills something, all allies get +1 Damage and heal 5 health."

```
Teamwork {
    name "PASSIVE_TEAMWORK_NAME"
    desc "PASSIVE_TEAMWORK_DESC"
    class Druid

    1 {
        passives {
            AddPassivesToMinions {
                StatusAlliesOnKill {
                    DamageUp 1
                }
                StatusOnKill {
                    DamageUp 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_TEAMWORK2_DESC"
        passives {
            AddPassivesToMinions {
                StatusAlliesOnKill {
                    DamageUp 1
                    HealthGain 5
                }
                StatusOnKill {
                    DamageUp 1
                    HealthGain 5
                }
            }
        }
    }
}
```

---

### `Bouquet`
**Name:** Bouquet  
**Description:** Spawn a tall flower tile under you at the end of your turn.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_BOUQUET2_DESC`: "Spawn tall flower tiles under and around you at the end of your turn."

```
Bouquet {
    name "PASSIVE_BOUQUET_NAME"
    desc "PASSIVE_BOUQUET_DESC"
    class Druid

    1 {
        passives {
            FlowersOnEndTurn 3
        }
    }
    2 {
        desc "PASSIVE_BOUQUET2_DESC"
        passives {
            FlowersOnEndTurn 4
        }
    }
}
```

---

### `GoodVibrations`
**Name:** Good Vibrations  
**Description:** Allies have +1 Health Regeneration and +1 Mana Regeneration.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_GOODVIBRATIONS2_DESC`: "Allies have +2 Health Regeneration and +2 Mana Regeneration."

```
GoodVibrations {
    name "PASSIVE_GOODVIBRATIONS_NAME"
    desc "PASSIVE_GOODVIBRATIONS_DESC"
    class Druid

    1 {
        passives {
            AllyHealthRegenAura {
                stacks 1
                range global
            }
            AllyManaRegenAura {
                stacks 1
                range global
            }
        }
    }
    2 {
        desc "PASSIVE_GOODVIBRATIONS2_DESC"
        passives {
            AllyHealthRegenAura {
                stacks 2
                range global
            }
            AllyManaRegenAura {
                stacks 2
                range global
            }
        }
    }
}
```

---

### `VersatileVocalist`
**Name:** Versatile Vocalist  
**Description:** Your basic action deals 1 damage to enemies, and inflicts temporary -1 Damage. Your basic attack wont apply debuffs to allies or buffs to enemies.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_VERSATILEVOLCALIST2_DESC`: "Your basic action has +1 area, deals 1 damage to enemies, and inflicts temporary -1 Damage. Your basic attack wont apply debuffs to allies or buffs to enemies."

```
VersatileVocalist { //TODO: do this in a way that isnt an ability swap
    name "PASSIVE_VERSATILEVOLCALIST_NAME"
    desc "PASSIVE_VERSATILEVOLCALIST_DESC"
    class Druid

    1 {
        override_basic_attack BasicDruidAbilityVersatile 
        passives {
            BasicAttackStatusCarefulness 1
            ReplaceBasicAttack BasicDruidAbilityVersatile
        }
    }
    2 {
        desc "PASSIVE_VERSATILEVOLCALIST2_DESC"

        override_basic_attack BasicDruidAbilityVersatile 
        passives {
            BasicAttackAOEBonus 1
            BasicAttackStatusCarefulness 1
            ReplaceBasicAttack BasicDruidAbilityVersatile
        }
    }
}
```

---

### `LikeAFish`
**Name:** Like a Fish  
**Description:** Water tiles don't slow you down.
Gain +1 Holy Shield at the end of the turn if you're wet and have no Holy Shield.
Familiars you spawn also have this passive.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_LIKEAFISH2_DESC`: "Water tiles don't slow you down. <br/> Gain +1 Holy Shield at the end of the turn if you're wet and have no Holy Shield.  Gain +1 Health Regeneration. <br/> Familiars you spawn also have this passive."

```
LikeAFish {
    name "PASSIVE_LIKEAFISH_NAME"
    desc "PASSIVE_LIKEAFISH_DESC"
    class Druid

    1 {
        passives {
            WaterWalk 1
            PassiveWhenAffectedByElement {
                element water
                passives {
                    StatusEachTurnEnd {
                        NonStackingDivineShield 1
                    }
                }
            }

            AddPassivesToMinions {
                WaterWalk 1
                PassiveWhenAffectedByElement {
                    element water
                    passives {
                        StatusEachTurnEnd {
                            NonStackingDivineShield 1
                        }
                    }
                }
            }
        }
    }
    2 {
        desc "PASSIVE_LIKEAFISH2_DESC"

        passives {
            WaterWalk 1
            FreePathfindElement Water
            PassiveWhenAffectedByElement {
                element water
                passives {
                    StatusEachTurnEnd {
                        NonStackingDivineShield 1
                    }
                    HealthRegenUp 1
                    AddManaRegen 1
                }
            }

            AddPassivesToMinions {
                WaterWalk 1
                FreePathfindElement Water
                PassiveWhenAffectedByElement {
                    element water
                    passives {
                        StatusEachTurnEnd {
                            NonStackingDivineShield 1
                        }
                        HealthRegenUp 1
                        AddManaRegen 1
                    }
                }
            }
        }
    }
}
```

---

### `Encore`
**Name:** Encore  
**Description:** When you use a musical ability, refresh your basic action.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_ENCORE2_DESC`: "Your musical spells cost 1 less mana. When you use a musical ability, refresh your basic action."

```
Encore {
    name "PASSIVE_ENCORE_NAME"
    desc "PASSIVE_ENCORE_DESC"
    class Druid

    1 {
        passives {
            StatusOnUseAbilityWithTag {
                tag musical
                exclude_basicattack true

                RefreshActPoints 1
            }
        }
    }
    2 {
        desc "PASSIVE_ENCORE2_DESC"

        passives {
            StatusOnUseAbilityWithTag {
                tag musical
                exclude_basicattack true

                RefreshActPoints 1
            }

            ManaCostReductionTagged {
                tag musical
                reduction 1
            }
        }
        stats {
            cha 2
        }
    }
}
```

---

### `SpecialFriends`
**Name:** Super Friends  
**Description:** Familiars spawned by spells gain All Stats Up 2, but that spell gets disabled until the spawned familiars die.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_SUPERFRIENDS2_DESC`: "Familiars spawned by spells gain All Stats Up 2, but that spell gets disabled until the spawned familiars die. <br/> Your spawning spells cost 50% less mana."

```
SpecialFriends {
    name "PASSIVE_SUPERFRIENDS_NAME"
    desc "PASSIVE_SUPERFRIENDS_DESC"
    class Druid

    1 {
        passives {
            SpecialFriends {
                AllStatsUp 2
                HealthGain 8 //fill up the blank max health
            }
        }
    }
    2 {
        desc "PASSIVE_SUPERFRIENDS2_DESC"

        passives {
            SpecialFriends {
                AllStatsUp 2
                HealthGain 8 //fill up the blank max health
            }

            ManaCostReductionTagged {
                tag summon
                reduction 50%
            }
        }
    }
}
```

---

### `SneakAttack`
**Name:** Sneak Attack  
**Description:** Your spells that spawn familiars cost -3 mana.
Familiars spawned by your spells gain +2 Damage and +2 Movement, but die after their first turn.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_SNEAKATTACK2_DESC`: "Your spells that spawn familiars cost -3 mana. <br/> Familiars spawned by your spells gain +4 Damage and +4 Movement, but die after their first turn."

```
SneakAttack {
    name "PASSIVE_SNEAKATTACK_NAME"
    desc "PASSIVE_SNEAKATTACK_DESC"
    class Druid

    1 {
        passives {
            AddPassivesToSummonAbilityMinions {
                DamageUp 2
                MovementUp 2
                Doomed 1
            }
            ManaCostReductionTagged {
                tag summon
                reduction 3
            }
        }
    }
    2 {
        desc "PASSIVE_SNEAKATTACK2_DESC"

        passives {
            AddPassivesToSummonAbilityMinions {
                DamageUp 4
                MovementUp 4
                Doomed 1
            }
            ManaCostReductionTagged {
                tag summon
                reduction 3
            }
        }
    }
}
```

---

### `WildStyle`
**Name:** Wild Style  
**Description:** The first time you shapeshift each turn, gain an extra turn.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_WILDSTYLE2_DESC`: "The first time you shapeshift each turn, gain All Stats Up and an extra turn."

```
WildStyle {
    name "PASSIVE_WILDSTYLE_NAME"
    desc "PASSIVE_WILDSTYLE_DESC"
    class Druid

    1 {
        passives {
            StatusOnUseAbilityWithTag {
                tag shapeshift

                Conditional_FirstApplicationThisTurn {
                    TakeExtraTurn 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_WILDSTYLE2_DESC"

        passives {
            StatusOnUseAbilityWithTag {
                tag shapeshift

                Conditional_FirstApplicationThisTurn {
                    TakeExtraTurn 1
                    AllStatsUp 1
                }
            }
        }
    }
}
```

---

### `BuddySystem`
**Name:** Buddy System  
**Description:** When you lose [img:divineshield], your crow gains +1 [img:divineshield]. When your crow loses [img:divineshield], gain +1 [img:divineshield].  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_BUDDYSYSTEM2_DESC`: "When you lose [img:divineshield], all your familiars gain +1 [img:divineshield]. When your crow loses [img:divineshield], gain +1 [img:divineshield]."

```
BuddySystem {
    name "PASSIVE_BUDDYSYSTEM_NAME"
    desc "PASSIVE_BUDDYSYSTEM_DESC"
    class Druid

    1 {
        divine_shield 1

        passives {
            HolyShieldTransferToTaggedMinions crow

            AddPassivesToMinions {
                tag_filter crow

                HolyShieldTransferToSpawner 1
            }
        }
    }
    2 {
        desc "PASSIVE_BUDDYSYSTEM2_DESC"

        divine_shield 1

        passives {
            HolyShieldTransferToTaggedMinions any

            AddPassivesToMinions {
                tag_filter crow

                HolyShieldTransferToSpawner 1
            }
        }
    }
}
```

---

### `FlowerPower`
**Name:** Flower Power  
**Description:** Units on flower tiles have +2 [img:str] and +2 Brace. When you move, plant flowers on the tile you moved from.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_FLOWERPOWER2_DESC`: "Units on flower tiles have +2 [img:str] and +2 Brace. When you move, plant flowers on all tiles you move through."

```
FlowerPower {
    name "PASSIVE_FLOWERPOWER_NAME"
    desc "PASSIVE_FLOWERPOWER_DESC"
    class Druid

    1 {
        passives {
            FlowerPowerAuraStrength 1
            FlowerPowerAuraBrace 1

            LimitedTileTrail FlowerTile
        }
    }
    2 {
        desc "PASSIVE_FLOWERPOWER2_DESC"

        passives {
            FlowerPowerAuraStrength 1
            FlowerPowerAuraBrace 1

            TileTrail FlowerTile
        }
    }
}
```

---

### `SuicideSquad`
**Name:** Suicide Squad  
**Description:** Your controllable familiars gain Self Destruct as their bonus ability.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_SUICIDESQUAD2_DESC`: "Your controllable familiars gain Self Destruct+ as their bonus ability."

```
SuicideSquad {
    name "PASSIVE_SUICIDESQUAD_NAME"
    desc "PASSIVE_SUICIDESQUAD_DESC"
    class Druid

    1 {
        passives {
            AddPassivesToMinions {
                FamiliarBonusAbility FamiliarSelfDestruct
            }
        }
    }
    2 {
        desc "PASSIVE_SUICIDESQUAD2_DESC"
        passives {
            AddPassivesToMinions {
                FamiliarBonusAbility FamiliarSelfDestruct2
            }
        }
    }
}
```

---

### `Feral`
**Name:** Feral  
**Description:** Your bonus ability is Feral Attack.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_FERAL2_DESC`: "Your bonus ability is Feral Attack."

```
Feral {
    name "PASSIVE_FERAL_NAME"
    desc "PASSIVE_FERAL_DESC"
    class Druid

    1 {
        passives {
            BonusAbility FeralMelee
        }
        stats {
            str 3
            con 1
        }
    }
    2 {
        desc "PASSIVE_FERAL2_DESC"
        passives {
            BonusAbility FeralMelee
        }
        stats {
            str 4
            con 2
            spd 2
        }
    }
}
```

---

### `RapGod`
**Name:** Rap God  
**Description:** Your basic action also gives temporary +4 [img:spd].  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_RAPGOD2_DESC`: "Your basic action also gives temporary +4 [img:spd], enemies gain Confusion 2 instead."

```
RapGod {
    name "PASSIVE_RAPGOD_NAME"
    desc "PASSIVE_RAPGOD_DESC"
    class Druid

    1 {
        passives {
            AddStatusToBasicAttack {
                Conditional_SourceHasTag {
                    tag crow

                    Conditional_Ally {
                        TempSpeedUp 4
                    }
                } Else {
                    TempSpeedUp 4
                }
            }
        }
    }
    2 {
        desc "PASSIVE_RAPGOD2_DESC"
        passives {
            AddStatusToBasicAttack {
                Conditional_Ally {
                    TempSpeedUp 4
                }
                Conditional_Enemy {
                    Confusion 2
                }
            }
        }
    }
}
```

---

### `Animalistic`
**Name:** Animalistic  
**Description:** Familiars you spawn gain +2 Damage.
When you shapeshift, gain +1 Damage.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_ANIMALISTIC2_DESC`: "Familiars you spawn gain +2 Damage and a Bonus Attack. <br/> When you shapeshift, gain +1 Damage and refresh your basic attack."

```
Animalistic {
    name "PASSIVE_ANIMALISTIC_NAME"
    desc "PASSIVE_ANIMALISTIC_DESC"
    class Druid

    1 {
        passives {
            AddPassivesToMinions {
                DamageUp 2
            }
            StatusOnUseAbilityWithTag {
                tag shapeshift

                DamageUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_ANIMALISTIC2_DESC"
        passives {
            AddPassivesToMinions {
                DamageUp 2
                Quivered 1
            }
            StatusOnUseAbilityWithTag {
                tag shapeshift

                DamageUp 1
                RefreshActPoints 1
            }
        }
    }
}
```

---

### `Maestro`
**Name:** Maestro  
**Description:** Your musical spells cost 50% less mana.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_MAESTRO2_DESC`: "Your musical spells cost 50% less mana. <br/> When you use a musical spell, heal 1 HP and gain +1 to a random stat."

```
Maestro {
    name "PASSIVE_MAESTRO_NAME"
    desc "PASSIVE_MAESTRO_DESC"
    class Druid

    1 {
        passives {
            ManaCostReductionTagged {
                tag musical
                reduction 50%
            }
        }
    }
    2 {
        desc "PASSIVE_MAESTRO2_DESC"

        passives {
            ManaCostReductionTagged {
                tag musical
                reduction 50%
            }
            StatusOnUseAbilityWithTag {
                tag musical

                RandomStatUp 1
                HealthGain 1
            }
        }
    }
}
```

---

### `MegaMinions`
**Name:** Mega Minions  
**Description:** Every 3rd familiar you spawn is upgraded into a Champion.  
**Source:** `druid_passives.gon`  

**Localization Strings:**
- `PASSIVE_MEGAMINIONS2_DESC`: "The 1st and every 3rd familiar you spawn are upgraded into a Champion. <br/> \[s:.7\](The first familiar you spawn is likely your Crow.)\[/s\]"

```
MegaMinions {
    name "PASSIVE_MEGAMINIONS_NAME"
    desc "PASSIVE_MEGAMINIONS_DESC"
    class Druid

    1 {
        passives {
            MegaMinions 3
        }
    }
    2 {
        desc "PASSIVE_MEGAMINIONS2_DESC"

        passives {
            MegaMinions {
                stacks 3
                cycle_start 3
            }
        }
    }
}
```

---

## File: `fighter_passives.gon`

### `BloodLust`
**Name:** Frenzy  
**Description:** When you down a unit, gain +2 [img:str].  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_FRENZY2_DESC`: "When you down a unit, gain +2 [img:str] and +2 [img:spd]."

```
BloodLust {
    name "PASSIVE_FRENZY_NAME"
    desc "PASSIVE_FRENZY_DESC"
    class Fighter

    1 {
        passives {
            StatusOnKill {
                StrengthUp 2
            }
        }
    }
    2 {
        desc "PASSIVE_FRENZY2_DESC"
        passives {
            StatusOnKill {
                StrengthUp 2
                SpeedUp 2
            }
        }
    }
}
```

---

### `Avenger`
**Name:** Avenger  
**Description:** When an allied cat is downed, gain All Stats Up 2 and heal 8.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_AVENGER2_DESC`: "When an allied cat is downed, gain All Stats Up 2, heal 50% of your max HP, and take an extra turn."

```
Avenger {
    name "PASSIVE_AVENGER_NAME"
    desc "PASSIVE_AVENGER_DESC"
    class Fighter

    1 {
        passives {
            StatusOnAllyCatDeath {
                AllStatsUp 2
                HealthGain 8
            }
        }
    }
    2 {
        desc "PASSIVE_AVENGER2_DESC"
        passives {
            StatusOnAllyCatDeath {
                AllStatsUp 2
                PercentHeal 50
                TakeExtraTurn 1
            }
        }
    }
}
```

---

### `Scars`
**Name:** Scars  
**Description:** +1 Brace.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_SCARS2_DESC`: "+3 Brace."

```
Scars {
    name "PASSIVE_SCARS_NAME"
    desc "PASSIVE_SCARS_DESC"
    class Fighter

    1 {
        passives {
            Brace 1
        }
    }
    2 {
        desc "PASSIVE_SCARS2_DESC"
        passives {
            Brace 3
        }
    }
}
```

---

### `FasterWhenHit`
**Name:** Hulk Up  
**Description:** When you take damage, gain +2 [img:spd].  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_HULKUP2_DESC`: "When you take damage, gain +2 [img:spd] and +10% dodge. This caps at 50%."

```
FasterWhenHit {
    name "PASSIVE_HULKUP_NAME"
    desc "PASSIVE_HULKUP_DESC"
    class Fighter

    1 {
        passives {
            StatusOnTookDamage {
                SpeedUp 2
            }
        }
    }
    2 {
        desc "PASSIVE_HULKUP2_DESC"
        passives {
            StatusOnTookDamage {
                SpeedUp 2
            }
            StackingDodgeChanceOnTookDamage {
                amount 10%
                cap 50%
            }
        }
        stats {
            spd 2
        }
    }
}
```

---

### `KillsHeal`
**Name:** Fervor  
**Description:** When you down a unit, you heal 5 HP.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_FERVOR2_DESC`: "When you down a unit, you heal 50% of your HP."

```
KillsHeal {
    name "PASSIVE_FERVOR_NAME"
    desc "PASSIVE_FERVOR_DESC"
    class Fighter

    1 {
        passives {
            KillsHeal 5
        }
    }
    2 {
        desc "PASSIVE_FERVOR2_DESC"
        passives {
            KillsHeal 50%
        }
    }
}
```

---

### `Vengeful`
**Name:** Vengeful  
**Description:** Your basic attack is always critical on enemies that have damaged you.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_VENGEFUL2_DESC`: "Your basic attack is always critical on enemies units that have damaged you. <br/> Inflict Marked on units that contact or attack you."

```
Vengeful {
    name "PASSIVE_VENGEFUL_NAME"
    desc "PASSIVE_VENGEFUL_DESC"
    class Fighter

    1 {
        passives {
            Vengeful 1
        }
    }
    2 {
        desc "PASSIVE_VENGEFUL2_DESC"
        passives {
            Vengeful 1
            RevengeDamage {
                effects {
                    Marked 1
                }
            }
        }
    }
}
```

---

### `HamsterStyle`
**Name:** Hamster Style  
**Description:** +1 Health Regeneration.
Start with 2 Bonus Moves.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_HAMSTERSTYLE2_DESC`: "+2 Health Regeneration. <br/> Start with 2 Bonus Moves. <br/> Your basic attack has a chance to attack multiple times."

```
HamsterStyle {
    name "PASSIVE_HAMSTERSTYLE_NAME"
    desc "PASSIVE_HAMSTERSTYLE_DESC"
    class Fighter

    1 {
        passives {
            HealthRegenUp 1
            SizeScale .8
            MoveQuivered 2
        }
        stats {
            str -1
            con -1
            int 1
        }
    }
    2 {
        desc "PASSIVE_HAMSTERSTYLE2_DESC"
        passives {
            HealthRegenUp 2
            SizeScale .6
            AddTemporaryEffectsToBasicAttack {
                Fury 75
            }
            MoveQuivered 2
        }
        stats {
            str -1
            con -1
            int 1
        }
    }
}
```

---

### `WeaponMaster`
**Name:** Weapon Master  
**Description:** Your weapon and item abilities deal +2 Damage and get +25% critical chance. A pipe is added to your inventory.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_WEAPONMASTER2_DESC`: "Your weapon and item abilities deal +3 Damage and get +50% critical chance. <br/> If you don't have a weapon, gain a random temporary weapon at the beginning of the battle."

```
WeaponMaster {
    name "PASSIVE_WEAPONMASTER_NAME"
    desc "PASSIVE_WEAPONMASTER_DESC"
    class Fighter

    1 {
        passives {
            BoostWeaponDamage {
                damage 2
                crit_chance .25
            }
        }
        bonus_items [Pipe]
    }
    2 {
        desc "PASSIVE_WEAPONMASTER2_DESC"
        passives {
            BoostWeaponDamage {
                damage 3
                crit_chance .5
            }

            EquipRandomTemporaryItemFromPool weapons
        }
    }
}
```

---

### `ShoulderCheck`
**Name:** Shoulder Check  
**Description:** If you're facing a unit after you move, automatically attack it at 33% damage.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_SHOULDERCHECK2_DESC`: "If you're facing a unit after you move, automatically attack the unit."

```
ShoulderCheck {
    name "PASSIVE_SHOULDERCHECK_NAME"
    desc "PASSIVE_SHOULDERCHECK_DESC"
    class Fighter

    1 {
        passives {
            ShoulderCheck 33%
        }
    }
    2 {
        desc "PASSIVE_SHOULDERCHECK2_DESC"
        passives {
            ShoulderCheck 100%
        }
    }
}
```

---

### `SkullSmash`
**Name:** Skullcrack  
**Description:** Your basic attack inflicts Bruise.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_SKULLSMASH2_DESC`: "Your basic attack inflicts Bruise 2."

```
SkullSmash {
    name "PASSIVE_SKULLSMASH_NAME"
    desc "PASSIVE_SKULLSMASH_DESC"
    class Fighter

    1 {
        passives {
            AddStatusToBasicAttack {
                Bruise 1
            }
        }
    }
    2 {
        desc "PASSIVE_SKULLSMASH2_DESC"
        passives {
            AddStatusToBasicAttack {
                Bruise 2
            }
        }
    }
}
```

---

### `TurtleStyle`
**Name:** Turtle Style  
**Description:** PASSIVE_TURTLESTYLE_DESC  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_TURTLESTYLE2_DESC`: "+2 Brace"

```
TurtleStyle {
    name "PASSIVE_TURTLESTYLE_NAME"
    desc "PASSIVE_TURTLESTYLE_DESC"
    class Fighter

    1 {
        shield 4
        stats {
            con 2
            spd -1
        }
    }
    2 {
        desc "PASSIVE_TURTLESTYLE2_DESC"
        shield 4
        stats {
            con 2
            spd -1
        }
        passives {
            Brace 2
        }
    }
}
```

---

### `Overpowered`
**Name:** OVERPOWERED!!!  
**Description:** Excess damage you deal to units makes them explode, dealing the excess damage to units around it, except for you.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_OVERPOWERED2_DESC`: "Excess damage you deal to units makes them explode, dealing the excess damage to units within 2 tiles of it, except for you."

```
Overpowered {
    name "PASSIVE_OVERPOWERED_NAME"
    desc "PASSIVE_OVERPOWERED_DESC"
    class Fighter

    1 {
        passives {
            ExplodeOverkilledEnemies 1
        }
    }
    2 {
        desc "PASSIVE_OVERPOWERED2_DESC"

        passives {
            ExplodeOverkilledEnemies 2
        }
    }
}
```

---

### `FightMe`
**Name:** Underdog  
**Description:** You have +2 [img:str] and +1 Brace for each enemy adjacent to you.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_FIGHTME2_DESC`: "You have +3 [img:str] and +2 Brace for each enemy adjacent to you."

```
FightMe {
    name "PASSIVE_FIGHTME_NAME"
    desc "PASSIVE_FIGHTME_DESC"
    class Fighter

    1 {
        passives {
            StrengthForEachNeighboringEnemy 2
            BraceForEachNeighboringEnemy 1
        }
    }
    2 {
        desc "PASSIVE_FIGHTME2_DESC"

        passives {
            StrengthForEachNeighboringEnemy 3
            BraceForEachNeighboringEnemy 2
        }
    }
}
```

---

### `HighAsYouCanCount`
**Name:** Math?  
**Description:** Your spells cost 3 mana to cast, but each can be cast only once per turn.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_MATHQ2_DESC`: "Your spells cost 0 mana to cast, but each can be cast only once per turn."

```
HighAsYouCanCount {
    name "PASSIVE_MATHQ_NAME"
    desc "PASSIVE_MATHQ_DESC"
    class Fighter

    1 {
        passives {
            SetSpellCosts 3
            MakeSpellsRequireCharge 1
        }
    }
    2 {
        desc "PASSIVE_MATHQ2_DESC"

        passives {
            SetSpellCosts 0
            MakeSpellsRequireCharge 1
        }
    }
}
```

---

### `DumbMuscle`
**Name:** Dumb Muscle  
**Description:** Lose 1 [img:int] each time you take damage.
If you have 4 or less [img:int], gain +2 [img:str] and your basic attack inflicts Bruise. at 0 [img:int], gain +100% critical hit chance.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_DUMBMUSCLE2_DESC`: "Lose 2 [img:int] each time you take damage. <br/> If you have 4 or less [img:int], gain +2 [img:str] and your basic attack inflicts Bruise. At 0 [img:int], gain +100% critical hit chance. At -10 [img:int], you can use your basic move and attack an additional time each turn."

```
DumbMuscle {
    name "PASSIVE_DUMBMUSCLE_NAME"
    desc "PASSIVE_DUMBMUSCLE_DESC"
    class Fighter

    1 {
        passives {
            StatusOnTookDamage {
                IntelligenceUp -1
            }
            PassiveAtStatThreshold {
                mode less_or_equal
                threshold {
                    int 4
                }
                passives {
                    StrengthUp 2
                    AddStatusToBasicAttack {
                        Bruise 1
                    }
                }
            }
            PassiveAtStatThreshold {
                mode less_or_equal
                threshold {
                    int 0
                }
                passives {
                    BasicAttackCritChance 100%
                }
            }
        }
    }
    2 {
        desc "PASSIVE_DUMBMUSCLE2_DESC"

        passives {
            StatusOnTookDamage {
                IntelligenceUp -2
            }
            PassiveAtStatThreshold {
                mode less_or_equal
                threshold {
                    int 4
                }
                passives {
                    StrengthUp 2
                    AddStatusToBasicAttack {
                        Bruise 1
                    }
                }
            }
            PassiveAtStatThreshold {
                mode less_or_equal
                threshold {
                    int 0
                }
                passives {
                    BasicAttackCritChance 100%
                }
            }
            PassiveAtStatThreshold {
                mode less_or_equal
                threshold {
                    int -10
                }
                passives {
                    ExtraMovePoints 1
                    ExtraBasicAttacks 1
                }
            }
        }
    }
}
```

---

### `ThickSkull`
**Name:** Thick Skull  
**Description:** All injuries you get are Concussions.
You get +3 [img:shield] for each concussion you have. This caps at 30 [img:shield].  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_THICKSKULL2_DESC`: "All injuries you get are Concussions. <br/> You get +3 [img:shield] and +1 [img:str] for each concussion you have. This caps at 30 [img:shield] and 10 [img:str]."

```
ThickSkull {
    name "PASSIVE_THICKSKULL_NAME"
    desc "PASSIVE_THICKSKULL_DESC"
    class Fighter

    1 {
        passives {
            ForceSpecificInjury int
            StatusPerInjury {
                injury int
                cap 10

                Shield 3
            }
        }
    }
    2 {
        desc "PASSIVE_THICKSKULL2_DESC"

        passives {
            ForceSpecificInjury int
            StatusPerInjury {
                injury int
                cap 10

                Shield 3
                StrengthUp 1
            }
        }
    }
}
```

---

### `MostValuableCat`
**Name:** Most Valuable Cat  
**Description:** When you or an ally downs another unit, they become the Alpha.
If you're the Alpha, take an extra turn at the end of each round.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_MOSTVALUABLECAT2_DESC`: "You start the battle as the Alpha. <br/> Whenever you or an ally downs another unit, they become the Alpha. <br/> If you're the Alpha, take an extra turn at the end of each round."

```
MostValuableCat {
    name "PASSIVE_MOSTVALUABLECAT_NAME"
    desc "PASSIVE_MOSTVALUABLECAT_DESC"
    class Fighter

    1 {
        passives {
            StatusAnyCatAllyWhoKills {
                AlphaCat 1
            }
            PassiveWhenTheAlpha {
                TogglableRoundEndExtraTurn 1
            }
        }
    }
    2 {
        desc "PASSIVE_MOSTVALUABLECAT2_DESC"

        passives {
            AlphaCat 1
            StatusAnyCatAllyWhoKills {
                AlphaCat 1
            }
            PassiveWhenTheAlpha {
                TogglableRoundEndExtraTurn 1
            }
        }
    }
}
```

---

### `RatStyle`
**Name:** Rat Style  
**Description:** +10% dodge chance.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_RATSTYLE2_DESC`: "+30% dodge chance."

```
RatStyle {
    name "PASSIVE_RATSTYLE_NAME"
    desc "PASSIVE_RATSTYLE_DESC"
    class Fighter

    1 {
        passives {
            DodgeChance 10%
        }
        stats {
            spd 2
        }
    }
    2 {
        desc "PASSIVE_RATSTYLE2_DESC"
        passives {
            DodgeChance 30%
        }
        stats {
            spd 4
        }
    }
}
```

---

### `Boned`
**Name:** Boned  
**Description:** When you kill a unit, if you don't have a weapon, gain a Bone Club.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_BONED2_DESC`: "When you kill a unit, if you don't have a weapon, gain a Bone Club. <br/> Bonus Ability: Throw Weapon."

```
Boned {
    name "PASSIVE_BONED_NAME"
    desc "PASSIVE_BONED_DESC"
    class Fighter

    1 {
        passives {
            StatusOnKill {
                EquipPermanentItem BoneClub
            }
        }
    }
    2 {
        desc "PASSIVE_BONED2_DESC"
        passives {
            StatusOnKill {
                EquipPermanentItem BoneClub
            }
            BonusAbility FighterBonusThrow
        }
    }
}
```

---

### `DualWield`
**Name:** Dual Wield  
**Description:** When you use your weapon, automatically use it again for free.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_DUALWIELD2_DESC`: "When you use your weapon, automatically use it again for free, and then again! for free!"

```
DualWield {
    name "PASSIVE_DUALWIELD_NAME"
    desc "PASSIVE_DUALWIELD_DESC"
    class Fighter

    1 {
        passives {
            //DualWield 1
            DoubleCastWeapons 1
        }
    }
    2 {
        desc "PASSIVE_DUALWIELD2_DESC"
        passives {
            //DualWield 1
            //WeaponsDontLoseDurability 0
            DoubleCastWeapons 2
        }
    }
}
```

---

### `ReflexPunch`
**Name:** Patellar Reflex  
**Description:** When a unit damages you, counter-attack dealing 1 damage and inflicting Bruise.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_PATELLARREFLEX2_DESC`: "When a unit damages you, counter-attack with your basic attack and inflict Bruise."

```
ReflexPunch {
    name "PASSIVE_PATELLARREFLEX_NAME"
    desc "PASSIVE_PATELLARREFLEX_DESC"
    class Fighter

    1 {
        passives {
            CounterAttack ReflexPunchJab
        }
    }
    2 {
        desc "PASSIVE_PATELLARREFLEX2_DESC"
        passives {
            CounterAttack ReflexPunchJab2
        }
    }
}
```

---

### `HitMe`
**Name:** Hit Me  
**Description:** When you take damage from an ally, basic attack in the direction you're facing.
Damage you take from allies is reduced to 1.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_HITME2_DESC`: "When you take damage from an ally, basic attack in the direction you're facing. <br/> Damage you take from allies is reduced to 1. <br/> Whenever you take damage, gain +1 to a random stat."

```
HitMe {
    name "PASSIVE_HITME_NAME"
    desc "PASSIVE_HITME_DESC"
    class Fighter

    1 {
        passives {
            AllyDamageReaction attack
            CapDamageFromAllies 1
        }
    }
    2 {
        desc "PASSIVE_HITME2_DESC"
        passives {
            AllyDamageReaction attack
            CapDamageFromAllies 1

            StatusOnTookDamage {
                RandomStatUp 1
            }
        }
    }
}
```

---

### `Smash`
**Name:** Smash!  
**Description:** Your weapons deal triple damage, but they always break when you use them.
Three Sticks are added to your inventory.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_SMASH2_DESC`: "Your weapons deal triple damage, but they have a 50% chance to break when you use them. <br/> Three more Sticks are added to your inventory."

```
Smash {
    name "PASSIVE_SMASH_NAME"
    desc "PASSIVE_SMASH_DESC"
    class Fighter

    1 {
        passives {
            WeaponDamageMultiplierBonus 2
            AddSelfStatusToWeapons {
                ChanceToBreak 100
            }
        }

        bonus_items [Stick Stick Stick]
    }
    2 {
        desc "PASSIVE_SMASH2_DESC"
        passives {
            WeaponDamageMultiplierBonus 2
            AddSelfStatusToWeapons {
                ChanceToBreak 50
            }
        }

        bonus_items [Stick Stick Stick]
    }
}
```

---

### `PunchFace`
**Name:** Punch Face  
**Description:** Your basic attacks are critical if they hit the front of a unit.  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_PUNCHFACE2_DESC`: "Your physical attacks are critical if they hit the front of a unit."

```
PunchFace {
    name "PASSIVE_PUNCHFACE_NAME"
    desc "PASSIVE_PUNCHFACE_DESC"
    class Fighter

    1 {
        passives {
            FrontstabBasicAttackCritChance 100%
        }
    }
    2 {
        desc "PASSIVE_PUNCHFACE2_DESC"

        passives {
            FrontstabCritChance 100%
        }
    }
}
```

---

### `Recoil`
**Name:** Merciless  
**Description:** When you deal 10 or more damage in a single hit, gain +2 [img:shield] and refresh your movement action.
\[s:.7\](This doesn't trigger during your movement action.)\[/s\]  
**Source:** `fighter_passives.gon`  

**Localization Strings:**
- `PASSIVE_MERCILESS2_DESC`: "When you deal 10 or more damage in a single hit, gain +2 [img:shield], All Stats Up, and refresh your movement action. <br/> \[s:.7\](This doesn't trigger during your movement action.)\[/s\]"

```
Recoil {
    name "PASSIVE_MERCILESS_NAME"
    desc "PASSIVE_MERCILESS_DESC"
    class Fighter

    1 {
        passives {
            StatusOnDealtDamageThreshold {
                threshold 10
                count_overkill true
                ignore_during_movement true
                RefreshMovePoints 1
                Shield 2
            }
        }
    }
    2 {
        desc "PASSIVE_MERCILESS2_DESC"
        passives {
            StatusOnDealtDamageThreshold {
                threshold 10
                count_overkill true
                ignore_during_movement true
                RefreshMovePoints 1
                Shield 2
                AllStatsUp 1
            }
        }
    }
}
```

---

## File: `hunter_passives.gon`

### `TakeAim`
**Name:** Take Aim  
**Description:** Gain +1 range and damage at the start of each turn. You lose this when you move.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_TAKEAIM2_DESC`: "Gain +2 range and damage at the start of each turn. You lose this when you move."

```
TakeAim {
    name "PASSIVE_TAKEAIM_NAME"
    desc "PASSIVE_TAKEAIM_DESC"
    class Hunter

    1 {
        passives {
            TowerDefense {
                range 1
                damage 1
            }
        }
    }
    2 {
        desc "PASSIVE_TAKEAIM2_DESC"
        passives {
            TowerDefense {
                range 2
                damage 2
            }
        }
    }
}
```

---

### `TowerDefense`
**Name:** Tower Defense  
**Description:** When an enemy comes within range, shoot them for 1 damage.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_TOWERDEFENSE2_DESC`: "When an enemy comes within range, use your basic attack on them."

```
TowerDefense {
    name "PASSIVE_TOWERDEFENSE_NAME"
    desc "PASSIVE_TOWERDEFENSE_DESC"
    class Hunter

    1 {
        passives {
            TowerDefenseReflex BasicRanged_1DMG
        }
    }
    2 {
        desc "PASSIVE_TOWERDEFENSE2_DESC"
        passives {
            TowerDefenseReflex attack
        }
    }
}
```

---

### `HuntersBoon`
**Name:** Hunter's Boon  
**Description:** The first time you kill a unit each turn, gain 5 mana.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_HUNTERSBOON2_DESC`: "The first time you kill a unit each turn, restore all your mana."

```
HuntersBoon {
    name "PASSIVE_HUNTERSBOON_NAME"
    desc "PASSIVE_HUNTERSBOON_DESC"
    class Hunter

    1 {
        passives {
            StatusOnKill {
                Conditional_FirstApplicationThisTurn {
                    ManaGain 5
                }
            }
        }
    }
    2 {
        desc "PASSIVE_HUNTERSBOON2_DESC"
        passives {
            StatusOnKill {
                Conditional_FirstApplicationThisTurn {
                    FillMana 1
                }
            }
        }
    }
}
```

---

### `BroodMother`
**Name:** Brood Mother  
**Description:** Your familiars and units you charm gain +2 Damage and +5 HP.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_BROODMOTHER2_DESC`: "Your familiars and units you charm gain +3 Damage, +10 HP, and inflict Poison."

```
BroodMother {
    name "PASSIVE_BROODMOTHER_NAME"
    desc "PASSIVE_BROODMOTHER_DESC"
    class Hunter

    1 {
        passives {
            AddPassivesToMinions {
                DamageUp 2
                AddMaxHealth 5
                HealthGain 5 //fill up the blank max health
            }
            AddPassivesToCharmed {
                DamageUp 2
                AddMaxHealth 5
            }
        }
    }
    2 {
        desc "PASSIVE_BROODMOTHER2_DESC"
        passives {
            AddPassivesToMinions {
                DamageUp 3
                AddMaxHealth 10
                HealthGain 10 //fill up the blank max health

                AddStatusToBasicAttack {
                    Poison 1
                }
            }

            AddPassivesToCharmed {
                DamageUp 3
                AddMaxHealth 10
                AddStatusToBasicAttack {
                    Poison 1
                }
            }
        }
    }
}
```

---

### `TaintedMother`
**Name:** Tainted Mother  
**Description:** Your familiars and units you charm gain +4 [img:spd] and inflict Poison and Bleed.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_TAINTEDMOTHER2_DESC`: "Your familiars and units you charm gain +4 [img:spd] and inflict Poison and Bleed. <br/> Start each battle with 4 fly familiars."

```
TaintedMother {
    name "PASSIVE_TAINTEDMOTHER_NAME"
    desc "PASSIVE_TAINTEDMOTHER_DESC"
    class Hunter

    1 {
        passives {
            AddPassivesToMinions {
                AddSpeed 4
                AddStatusToBasicAttack {
                    Poison 1
                }
                AddStatusToBasicAttack {
                    Bleed 1
                }
            }

            AddPassivesToCharmed {
                AddSpeed 4
                AddStatusToBasicAttack {
                    Poison 1
                }
                AddStatusToBasicAttack {
                    Bleed 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_TAINTEDMOTHER2_DESC"
        passives {
            AddPassivesToMinions {
                AddSpeed 4
                AddStatusToBasicAttack {
                    Poison 2
                }
                AddStatusToBasicAttack {
                    Bleed 2
                }
            }

            AddPassivesToCharmed {
                AddSpeed 4
                AddStatusToBasicAttack {
                    Poison 2
                }
                AddStatusToBasicAttack {
                    Bleed 2
                }
            }

            SpawnOnBattleStart {
                object CharmedFly
                number 3
            }
        }
    }
}
```

---

### `Quiver`
**Name:** Quiver  
**Description:** Save unused basic attacks for future turns.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_QUIVER2_DESC`: "Save unused basic attacks for future turns. <br/> If you haven't attacked this battle, the number you save is doubled."

```
Quiver {
    name "PASSIVE_QUIVER_NAME"
    desc "PASSIVE_QUIVER_DESC"
    class Hunter

    1 {
        passives {
            Quiver 1
        }
    }
    2 {
        desc "PASSIVE_QUIVER2_DESC"
        passives {
            Quiver 2
        }
    }
}
```

---

### `SplitShot`
**Name:** Split Shot  
**Description:** Your basic attack has +1 area but deals 50% less damage.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_SPLITSHOT2_DESC`: "Your basic attack has +2 area but deals 50% less damage."

```
SplitShot {
    name "PASSIVE_SPLITSHOT_NAME"
    desc "PASSIVE_SPLITSHOT_DESC"
    class Hunter

    1 {
        passives {
            BasicAttackAOEBonus 1
            BasicAttackDamageMultiplier 50%
        }
    }
    2 {
        desc "PASSIVE_SPLITSHOT2_DESC"
        passives {
            BasicAttackAOEBonus 2
            BasicAttackDamageMultiplier 50%
        }
    }
}
```

---

### `Hazardous`
**Name:** Hazardous  
**Description:** Tile damage and effects are doubled.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_HAZARDOUS2_DESC`: "Tile damage and effects are doubled. <br/> Allies are immune to tile damage and effects."

```
Hazardous {
    name "PASSIVE_HAZARDOUS_NAME"
    desc "PASSIVE_HAZARDOUS_DESC"
    class Hunter

    1 {
        passives {
            TileDamageMultiplier 2
        }
    }
    2 {
        desc "PASSIVE_HAZARDOUS2_DESC"
        passives {
            TileDamageMultiplier {
                multiplier 2
                ally_multiplier 0
            }
        }
    }
}
```

---

### `ThornArrows`
**Name:** Thorn Arrows  
**Description:** Your basic attack spawns brambles.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_THORNARROWS2_DESC`: "Your basic attack spawns brambles in an area."

```
ThornArrows {
    name "PASSIVE_THORNARROWS_NAME"
    desc "PASSIVE_THORNARROWS_DESC"
    class Hunter

    1 {
        passives {
            AddStatusToBasicAttack {
                ChangeTile BrambleTile
            }
        }
    }
    2 {
        desc "PASSIVE_THORNARROWS2_DESC"
        passives {
            AddStatusToBasicAttack {
                ChangeTile {
                    tile BrambleTile
                    aoe 1
                }
            }
        }
    }
}
```

---

### `Traps`
**Name:** Traps  
**Description:** Your basic attack spawns a bear trap if you shoot an empty tile.
Whenever one of your traps triggers, gain +2 [img:dex].  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_TRAPS2_DESC`: "Your basic attack spawns a bear trap if you shoot an empty tile. <br/> Whenever one of your traps triggers, gain +2 [img:dex] and +1 Bonus Attack."

```
Traps {
    name "PASSIVE_TRAPS_NAME"
    desc "PASSIVE_TRAPS_DESC"
    class Hunter

    1 {
        passives {
            AddStatusToBasicAttack {
                SpawnBearTrapOnMiss 1
            }
            StatusOnTriggerTrap {
                DexterityUp 2
            }
        }
    }
    2 {
        desc "PASSIVE_TRAPS2_DESC"
        passives {
            AddStatusToBasicAttack {
                SpawnBearTrapOnMiss 1
            }
            StatusOnTriggerTrap {
                Quivered 1
                DexterityUp 2
            }
        }
    }
}
```

---

### `CatchProjectiles`
**Name:** Catch Projectiles  
**Description:** 33% chance to block enemy projectiles and a 100% chance to block allied projectiles. If you block a projectile, gain +1 Bonus Attack.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_CATCHPROJECTILES2_DESC`: "50% chance to block enemy projectiles and a 100% chance to block allied projectiles. If you block a projectile, gain +1 Bonus Attack and +1 All Stats Up."

```
CatchProjectiles {
    name "PASSIVE_CATCHPROJECTILES_NAME"
    desc "PASSIVE_CATCHPROJECTILES_DESC"
    class Hunter

    1 {
        passives {
            CatchProjectiles {
                chance 33%
                ally_chance 100%
                Quivered 1
            }
        }
    }
    2 {
        desc "PASSIVE_CATCHPROJECTILES2_DESC"
        passives {
            CatchProjectiles {
                chance 50%
                ally_chance 100%
                Quivered 1
                AllStatsUp 1
            }
        }
    }
}
```

---

### `TrickyTraps`
**Name:** Tricky Traps  
**Description:** Damage and effects from your traps are doubled.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_TRICKYTRAPS2_DESC`: "Damage and effects from your traps are doubled. <br/> Allies don't trigger your traps."

```
TrickyTraps {
    name "PASSIVE_TRICKYTRAPS_NAME"
    desc "PASSIVE_TRICKYTRAPS_DESC"
    class Hunter

    1 {
        passives {
            TrapEffectsMultiplier 2
        }
    }
    2 {
        desc "PASSIVE_TRICKYTRAPS2_DESC"
        passives {
            TrapEffectsMultiplier 2
            AlliesAvoidTraps 1
        }
    }
}
```

---

### `GravityFalls`
**Name:** Gravity Falls  
**Description:** Your basic attack deals +1 damage for each tile you shoot beyond range 3.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_GRAVITYFALLS2_DESC`: "+2 range. <br/> Your basic attack deals +1 damage for each tile you shoot beyond range 3."

```
GravityFalls {
    name "PASSIVE_GRAVITYFALLS_NAME"
    desc "PASSIVE_GRAVITYFALLS_DESC"
    class Hunter

    1 {
        passives {
            AddStatusToBasicAttack {
                DistanceBonusDamage {
                    stacks 1
                    min_range 3
                }
            }
        }
    }
    2 {
        desc "PASSIVE_GRAVITYFALLS2_DESC"
        passives {
            AddStatusToBasicAttack {
                DistanceBonusDamage {
                    stacks 1
                    min_range 3
                }
            }
            AddBonusRange 2
        }
    }
}
```

---

### `HawkEye`
**Name:** Bullseye  
**Description:** Your ranged attacks never miss.
+25% critical hit chance.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_BULLSEYE2_DESC`: "Your ranged attacks never miss. <br/> +25% critical hit chance. <br/> Gain +1 [img:lck] each time you make a critical hit."

```
HawkEye {
    name "PASSIVE_BULLSEYE_NAME"
    desc "PASSIVE_BULLSEYE_DESC"
    class Hunter

    1 {
        passives {
            RangedTrueShot 1
            CritChanceUp 25
        }
    }
    2 {
        desc "PASSIVE_BULLSEYE2_DESC"
        passives {
            RangedTrueShot 1
            CritChanceUp 25
            StatusOnCrit {
                LuckUp 1
            }
        }
    }
}
```

---

### `Spotters`
**Name:** Spotters  
**Description:** Your basic attack can target tiles adjacent to allies.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_SPOTTERS2_DESC`: "Your basic attack and spells can target tiles adjacent to allies."

```
Spotters {
    name "PASSIVE_SPOTTERS_NAME"
    desc "PASSIVE_SPOTTERS_DESC"
    class Hunter

    1 {
        passives {
            AddAllyNeighborsToAttackRange 1
        }
    }
    2 {
        desc "PASSIVE_SPOTTERS2_DESC"
        passives {
            AddAllyNeighborsToAbilityRange 1
        }
    }
}
```

---

### `LuckSwing`
**Name:** Luck Swing  
**Description:** +50% critical hit chance but +25% chance to miss.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_LUCKSWING2_DESC`: "+50% critical hit chance but +25% chance to miss."

```
LuckSwing {
    name "PASSIVE_LUCKSWING_NAME"
    desc "PASSIVE_LUCKSWING_DESC"
    class Hunter

    1 {
        passives {
            CritChanceUp 50
            MissChance 25
        }
    }
    2 {
        desc "PASSIVE_LUCKSWING2_DESC"
        stats {
            lck 3
        }
        passives {
            CritChanceUp 50
            MissChance 25
        }
    }
}
```

---

### `Host`
**Name:** Host  
**Description:** Start each battle with 2 tiny spider familiars. A spider egg parasite is added to your inventory. You can unequip parasites freely.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_HOST2_DESC`: "Start each battle with 2 tiny spider familiars. A spider webber parasite is added to your inventory. You can unequip parasites freely."

```
Host {
    name "PASSIVE_HOST_NAME"
    desc "PASSIVE_HOST_DESC"
    class Hunter

    1 {
        passives {
            ParasitesArentCursed 1
            SpawnOnBattleStart CharmedTinySpider
            SpawnOnBattleStart CharmedTinySpider
        }

        bonus_items [SpiderEgg]
    }
    2 {
        desc "PASSIVE_HOST2_DESC"

        passives {
            ParasitesArentCursed 1
            SpawnOnBattleStart CharmedTinySpider
            SpawnOnBattleStart CharmedTinySpider
            SpawnOnBattleStart CharmedTinySpider
        }

        bonus_items [SpiderWebber]
    }
}
```

---

### `Sniper`
**Name:** Sniper  
**Description:** Critical hits deal +100% more damage and have a 25% chance to inflict Stun.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_SNIPER2_DESC`: "Critical hits deal +200% more damage and have a 33% chance to inflict Stun."

```
Sniper {
    name "PASSIVE_SNIPER_NAME"
    desc "PASSIVE_SNIPER_DESC"
    class Hunter

    1 {
        passives {
            AddCritMultiplier 100%
            CritsApplyStatus {
                Stun [1 .25]
            }
        }
    }
    2 {
        desc "PASSIVE_SNIPER2_DESC"

        passives {
            AddCritMultiplier 200%
            CritsApplyStatus {
                Stun [1 .33]
            }
        }
    }
}
```

---

### `RubberArrows`
**Name:** Rubber Arrows  
**Description:** Your projectiles bounce to another enemy within 3 tiles.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_RUBBERARROWS2_DESC`: "Your projectiles bounce to another enemy within 4 tiles, twice!"

```
RubberArrows {
    name "PASSIVE_RUBBERARROWS_NAME"
    desc "PASSIVE_RUBBERARROWS_DESC"
    class Hunter

    1 {
        passives {
            BouncyProjectiles {
                max_bounces 1
                max_range 3
            }
        }
    }
    2 {
        desc "PASSIVE_RUBBERARROWS2_DESC"

        passives {
            BouncyProjectiles {
                max_bounces 2
                max_range 4
            }
        }
    }
}
```

---

### `TalkToAnimals`
**Name:** Talk to Animals  
**Description:** Your basic attack inflicts Charm 5 the first time you use it each battle.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_TALKTOANIMALS2_DESC`: "Your basic attack inflicts Charm 5 the first time you use it each battle. <br/> Your basic attack has a 25% chance to inflict Charm 1."

```
TalkToAnimals {
    name "PASSIVE_TALKTOANIMALS_NAME"
    desc "PASSIVE_TALKTOANIMALS_DESC"
    class Hunter

    1 {
        passives {
            AddStatusToFirstBasicAttack {
                Charmed 5
            }
        }
    }
    2 {
        desc "PASSIVE_TALKTOANIMALS2_DESC"

        passives {
            AddStatusToFirstBasicAttack {
                Charmed 5
            }
            AddStatusToBasicAttack {
                Charmed [1 .25]
            }
        }
    }
}
```

---

### `AnimalControl`
**Name:** Animal Control  
**Description:** Your basic attack causes units to immediately attack an enemy in range.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_ANIMALCONTROL2_DESC`: "Your basic attack causes units to immediately attack an enemy in range. Your basic attack can heal allies."

```
AnimalControl {
    name "PASSIVE_ANIMALCONTROL_NAME"
    desc "PASSIVE_ANIMALCONTROL_DESC"
    class Hunter

    1 {
        passives {
            AddStatusToBasicAttackWithCooldown {
                CharmedForceAttack 1
            }
        }
    }
    2 {
        desc "PASSIVE_ANIMALCONTROL2_DESC"

        passives {
            AddStatusToBasicAttackWithCooldown {
                CharmedForceAttack 1
            }
            AddStatusToBasicAttack {
                DamageOrHealConditionally 1
            }
        }
    }
}
```

---

### `SleepDarts`
**Name:** Sleep Darts  
**Description:** At the start of each battle, you and all allies that don't have weapons gains a temporary Sleep Dart.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_SLEEPDARTS2_DESC`: "At the start of each battle, you and all allies that don't have weapons gains a temporary Sleep Dart with 2 uses."

```
SleepDarts {
    name "PASSIVE_SLEEPDARTS_NAME"
    desc "PASSIVE_SLEEPDARTS_DESC"
    class Hunter

    1 {
        passives {
            EquipTemporaryItem SleepDart
            StatusAlliesOnBattleStart {
                EquipTemporaryItem SleepDart
            }
        }
    }
    2 {
        desc "PASSIVE_SLEEPDARTS2_DESC"

        passives {
            EquipTemporaryItem SleepDart2
            StatusAlliesOnBattleStart {
                EquipTemporaryItem SleepDart2
            }
        }
    }
}
```

---

### `Survivalist`
**Name:** Survivalist  
**Description:** 6 healing consumables and a full water bottle are added to your inventory.
You can use consumables on allies.
Store +2 food at the end of each battle.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_SURVIVALIST2_DESC`: "4 large healing consumables are added to your inventory. <br/> You can use consumables on allies. <br/> Store +20 food at the end of each battle."

```
Survivalist {
    name "PASSIVE_SURVIVALIST_NAME"
    desc "PASSIVE_SURVIVALIST_DESC" //NOTE: the +2 food each fight is the "house resource" food
    class Hunter

    1 {
        passives {
            ConsumablesMeleeRange 1
            BonusFoodEachBattle 2
        }

        bonus_items [FoodMedium FoodMedium FoodMedium FoodMedium FoodMedium FoodMedium WaterBottle_Full]
    }
    2 {
        desc "PASSIVE_SURVIVALIST2_DESC"

        passives {
            ConsumablesInfiniteRange 1
            BonusFoodEachBattle 20
        }

        bonus_items [FoodBig FoodBig FoodBig FoodBig]
    }
}
```

---

### `Fleabag`
**Name:** Fleabag  
**Description:** At the end of your turn, spawn Flea familiars equal to the number of enemies you've killed this battle.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_FLEABAG2_DESC`: "At the end of your turn, spawn Flea familiars equal to the number of enemies you've killed this battle plus two."

```
Fleabag {
    name "PASSIVE_FLEABAG_NAME"
    desc "PASSIVE_FLEABAG_DESC"
    class Hunter

    1 {
        passives {
            StatusEachTurnEndPerEnemyKill {
                ObjectOnHitCharacter {
                    stacks 1
                    object CharmedFlea
                }
            }
        }
    }
    2 {
        desc "PASSIVE_FLEABAG2_DESC"

        passives {
            StatusEachTurnEnd {
                ObjectOnHitCharacter {
                    stacks 2
                    object CharmedFlea
                }
            }
            StatusEachTurnEndPerEnemyKill {
                ObjectOnHitCharacter {
                    stacks 1
                    object CharmedFlea
                }
            }
        }
    }
}
```

---

### `ThrillOfTheHunt`
**Name:** Thrill of the Hunt  
**Description:** At the end of each battle, if you killed at least 3 enemies, gain +1 [img:dex] permanently and find a random consumable item.  
**Source:** `hunter_passives.gon`  

**Localization Strings:**
- `PASSIVE_THRILLOFTHEHUNT2_DESC`: "At the end of each battle, if you killed at least 3 enemies, gain +1 [img:dex] permanently and find a random consumable item. +1 Range and +1 Health Regeneration for every 5 [img:dex] you have."

```
ThrillOfTheHunt {
    name "PASSIVE_THRILLOFTHEHUNT_NAME"
    desc "PASSIVE_THRILLOFTHEHUNT_DESC"
    class Hunter

    1 {
        passives {
            StatusOnBattleEndIfKillThresholdMet {
                kills 3

                statuses {
                    PermanentDexterity 1
                    FindItemFromPool consumables
                }
            }
        }
    }
    2 {
        desc "PASSIVE_THRILLOFTHEHUNT2_DESC"

        passives {
            StatusOnBattleEndIfKillThresholdMet {
                kills 3

                statuses {
                    PermanentDexterity 1
                    FindItemFromPool chapter
                }
            }
            BonusRangeBasedOnDex 5
            BonusHealthRegenBasedOnDex 5
        }
    }
}
```

---

## File: `jester_passives.gon`

### `SuperLuck`
**Name:** Super Luck  
**Description:** PASSIVE_SUPERLUCK_DESC  
**Source:** `jester_passives.gon`  

```
SuperLuck {
    name "PASSIVE_SUPERLUCK_NAME"
    desc "PASSIVE_SUPERLUCK_DESC"
    class Jester

    1 {
        stats {
            lck 21
        }
    }
    2 {
        desc "PASSIVE_SUPERLUCK2_DESC"
        stats {
            lck 77
        }
    }
}
```

---

### `Goofball`
**Name:** Goofball  
**Description:** Take an extra turn at the start of each round.  
**Source:** `jester_passives.gon`  

**Localization Strings:**
- `PASSIVE_GOOFBALL2_DESC`: "Take 2 extra turns at the start of each round."

```
Goofball {
    name "PASSIVE_GOOFBALL_NAME"
    desc "PASSIVE_GOOFBALL_DESC"
    class Jester

    1 {
        passives {
            AlphaTurns -1
        }
    }
    2 {
        desc "PASSIVE_GOOFBALL2_DESC"
        passives {
            AlphaTurns -1
            AlphaTurns -1
        }
    }
}
```

---

## File: `mage_passives.gon`

### `Micronaps`
**Name:** Synthesize  
**Description:** Gain +1 [img:int] at the start of each turn.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_SYNTHESIZE2_DESC`: "Gain +1 [img:int] at the start of each turn. <br/> Your spells cost 25% less mana."

```
Micronaps {
    name "PASSIVE_SYNTHESIZE_NAME"
    desc "PASSIVE_SYNTHESIZE_DESC"
    class Mage

    1 {
        passives {
            StatusEachTurnBegin {
                IntelligenceUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_SYNTHESIZE2_DESC"
        passives {
            StatusEachTurnBegin {
                IntelligenceUp 1
            }
            ManaCostReduction 25%
        }
    }
}
```

---

### `HolyMantel`
**Name:** Force Field  
**Description:** At the start of every third turn, gain +1 [img:divineshield].  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_FORCEFIELD2_DESC`: "At the start of every other turn, gain +1 [img:divineshield]."

```
HolyMantel {
    name "PASSIVE_FORCEFIELD_NAME"
    desc "PASSIVE_FORCEFIELD_DESC"
    class Mage

    1 {
        divine_shield 1
        passives {
            StatusEveryXTurnBegins {
                turns 3
                DivineShield 1
            }
        }
    }
    2 {
        desc "PASSIVE_FORCEFIELD2_DESC"

        divine_shield 1
        passives {
            StatusEveryXTurnBegins {
                turns 2
                DivineShield 1
            }
        }
    }
}
```

---

### `Shrapnel`
**Name:** Splash Damage  
**Description:** Your basic attack deals 2 Magic splash damage.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_SHRAPNEL2_DESC`: "+2 Range. Your basic attack deals 2 Magic splash damage in a wide area."

```
Shrapnel {
    name "PASSIVE_SHRAPNEL_NAME"
    desc "PASSIVE_SHRAPNEL_DESC"
    class Mage

    1 {
        passives {
            AddStatusToBasicAttack {
                SplashDamage 2
            }
        }
    }
    2 {
        desc "PASSIVE_SHRAPNEL2_DESC"
        passives {
            AddStatusToBasicAttack {
                BigSplashDamage 2
            }
            AddBonusRange 2
            AddBonusMeleeRange 2
        }
    }
}
```

---

### `BurningPaws`
**Name:** Burning Paws  
**Description:** Your basic action inflicts Burn 2.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_BURNINGPAWS2_DESC`: "Your basic action inflicts Burn 5."

```
BurningPaws {
    name "PASSIVE_BURNINGPAWS_NAME"
    desc "PASSIVE_BURNINGPAWS_DESC"
    class Mage

    1 {
        passives {
            AddStatusToBasicAttack {
                Burn 2
            }

            AddElementsToBasicAttack Fire
        }
    }
    2 {
        desc "PASSIVE_BURNINGPAWS2_DESC"
        passives {
            AddStatusToBasicAttack {
                Burn 5
            }

            AddElementsToBasicAttack Fire
        }
    }
}
```

---

### `LightningPaws`
**Name:** Lightning Paws  
**Description:** Your basic attack deals +2 Electric Damage and has a 15% chance to Stun.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_LIGHTNINGPAWS2_DESC`: "Your basic attack deals +4 Electric Damage and has a 40% chance to Stun."

```
LightningPaws {
    name "PASSIVE_LIGHTNINGPAWS_NAME"
    desc "PASSIVE_LIGHTNINGPAWS_DESC"
    class Mage

    1 {
        passives {
            AddStatusToBasicAttack {
                Stun [1 .15]
            }
            AddDamageToBasicAttack 2
            AddElementsToBasicAttack Electric
        }
    }
    2 {
        desc "PASSIVE_LIGHTNINGPAWS2_DESC"
        passives {
            AddStatusToBasicAttack {
                Stun [1 .40]
            }
            AddDamageToBasicAttack 4
            AddElementsToBasicAttack Electric
        }
    }
}
```

---

### `IcePaws`
**Name:** Ice Paws  
**Description:** Your basic attack deals Ice Damage, inflicts Slow 2, and has a 20% chance to Freeze. You can damage frozen units.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_ICEPAWS2_DESC`: "Your basic attack deals Ice Damage, inflicts Slow 5, and has a 50% chance to Freeze. You can damage frozen units."

```
IcePaws {
    name "PASSIVE_ICEPAWS_NAME"
    desc "PASSIVE_ICEPAWS_DESC"
    class Mage

    1 {
        passives {
			FreezePiercing 1
            AddStatusToBasicAttack {
                Freeze [1 .20]
                Slow 2
            }
            AddElementsToBasicAttack Ice
        }
    }
    2 {
        desc "PASSIVE_ICEPAWS2_DESC"
        passives {
			FreezePiercing 1
            AddStatusToBasicAttack {
                Freeze [1 .5]
                Slow 5
            }
            AddElementsToBasicAttack Ice
        }
    }
}
```

---

### `PawMissile`
**Name:** Paw Missile  
**Description:** Your basic attack is Magic Missile.
(its damage scales with [img:int]).  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_PAWMISSILE2_DESC`: "Your basic attack is Magic Missile. <br/> (its damage scales with [img:int]). <br/> Emit 4 Sparkles when you use your basic attack."

```
PawMissile {
    name "PASSIVE_PAWMISSILE_NAME"
    desc "PASSIVE_PAWMISSILE_DESC"
    class Mage

    1 {
        override_basic_attack BasicMagicMissile 
        passives {
            ReplaceBasicAttack BasicMagicMissile
        }
    }
    2 {
        desc "PASSIVE_PAWMISSILE2_DESC"
        override_basic_attack BasicMagicMissile 
        passives {
            ReplaceBasicAttack BasicMagicMissile
            AddSelfStatusToBasicAttack {
                RandomMagicMissile 1
                RandomMagicMissile 1
                RandomMagicMissile 1
                RandomMagicMissile 1
            }
        }
    }
}
```

---

### `Overload`
**Name:** Overload  
**Description:** When you cast a spell, deal 3 random elemental damage to adjacent tiles.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_OVERLOAD2_DESC`: "When you cast a spell, deal 6 tri-elemental damage to adjacent tiles."

```
Overload {
    name "PASSIVE_OVERLOAD_NAME"
    desc "PASSIVE_OVERLOAD_DESC"
    class Mage

    1 {
        passives {
            DamageNeighborTilesWhenCastSpell {
                fire {
                    type spell
                    damage 3

                    effects {
                        Burn 1
                        VisualFXTile BurnTrigger
                    }
                    elements [
                        Fire
                    ]
                }
                ice {
                    type spell
                    damage 3

                    effects {
                        Freeze [1, .05]
                        VisualFXTile IcePoof
                    }
                    elements [
                        Ice
                    ]
                }
                lightning {
                    type spell
                    damage 3

                    effects {
                        Stun [1, .05]
                        VisualFXTile WaterConduct
                    }
                    elements [
                        Electric
                    ]
                }
            }
        }
    }
    2 {
        desc "PASSIVE_OVERLOAD2_DESC"
        passives {
            DamageNeighborTilesWhenCastSpell {
                triattack {
                    type spell
                    damage 6

                    effects {
                        Burn 1
                        //Freeze [1, .05] //this just conflicts with Burn
                        Stun [1, .05]

                        VisualFXTile IcePoof
                        VisualFXTile BurnTrigger
                        VisualFXTile WaterConduct
                    }
                    elements [
                        Fire
                        Ice
                        Electric
                    ]
                }
            }
        }
    }
}
```

---

### `ChargeUp`
**Name:** Charge Up  
**Description:** If you end your turn with 0 mana, the next spell you cast is free  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_CHARGEUP2_DESC`: "If you end your turn with 0 mana, gain +1 Magic Damage and the next spell you cast is free."

```
ChargeUp {
    name "PASSIVE_CHARGEUP_NAME"
    desc "PASSIVE_CHARGEUP_DESC"
    class Mage

    1 {
        passives {
            StatusOnTurnEndIfManaExact {
                mana 0
                FreeSpell 1
            }
        }
    }
    2 {
        desc "PASSIVE_CHARGEUP2_DESC"
        passives {
            StatusOnTurnEndIfManaExact {
                mana 0
                FreeSpell 1
                SpellDamageUp 1
            }
        }
    }
}
```

---

### `DeathChill`
**Name:** Death Chill  
**Description:** When downed, Freeze all enemies and the rest of the map.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_DEATHCHILL2_DESC`: "When downed, Freeze all enemies and the rest of the map, and full heal all allies."

```
DeathChill { //CUT
    name "PASSIVE_DEATHCHILL_NAME"
    desc "PASSIVE_DEATHCHILL_DESC"
    class Mage

    1 {
        passives {
            StatusEnemiesOnDeath {
                Freeze 2
                AllStatsUp -1
            }
            DeathChill 1
        }
    }
    2 {
        desc "PASSIVE_DEATHCHILL2_DESC"
        passives {
            StatusEnemiesOnDeath {
                Freeze 2
                AllStatsUp -2
            }
            StatusAlliesOnDeath {
                FullHeal 1
                Freeze 1
            }
            DeathChill 1
        }
    }
}
```

---

### `Recharged`
**Name:** Epiphany  
**Description:** +5 starting mana. +5 Mana Regeneration.
Lose all unspent mana at the end of each of your turns  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_RECHARGED2_DESC`: "+20 starting mana. +5 Mana Regeneration. <br/> Lose all unspent mana at the end of each of your turns"

```
Recharged {
    name "PASSIVE_RECHARGED_NAME"
    desc "PASSIVE_RECHARGED_DESC"
    class Mage

    1 {
        passives {
            AddStartingMana 5
            AddManaRegen 5
            StatusEachTurnEnd {
                EmptyMana 1
            }
        }
    }
    2 {
        desc "PASSIVE_RECHARGED2_DESC"
        passives {
            AddStartingMana 20
            AddManaRegen 5
            StatusEachTurnEnd {
                EmptyMana 1
            }
        }
    }
}
```

---

### `EnergyStorm`
**Name:** Three  
**Description:** Every 3rd spell you cast in a turn is cast twice.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_ENERGYSTORM2_DESC`: "The first spell and every 3rd spell you cast is cast twice."

```
EnergyStorm {
    name "PASSIVE_ENERGYSTORM_NAME"
    desc "PASSIVE_ENERGYSTORM_DESC"
    class Mage

    1 {
        passives {
            EnergyStorm 3
        }
    }
    2 {
        desc "PASSIVE_ENERGYSTORM2_DESC"
        passives {
            EnergyStorm {
                period 3
                cycle_start 2
            }
        }
    }
}
```

---

### `FireArmor`
**Name:** Fire Aspect  
**Description:** Fire immunity.
Inflict Burn 1 on units that contact you.
Your Fire element damage is increased by 1 and inflicts +1 Burn.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_FIREASPECT2_DESC`: "Fire immunity. <br/> Inflict Burn 3 on units that contact you. <br/> Your Fire element damage is increased by 2 and inflicts +3 Burn."

```
FireArmor {
    name "PASSIVE_FIREASPECT_NAME"
    desc "PASSIVE_FIREASPECT_DESC"
    class Mage

    1 {
        passives {
            MeleeRevengeDamage {
                damage 0

                effects {
                    //Burn 1 //burn gets added here with the other effect
                    VisualFXTile BurnTrigger
                }
            
                elements [
                    Fire
                ]
            }
            InnateElement Fire
            ElementImmune Fire
            StatusImmunity [Burn]

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
    2 {
        desc "PASSIVE_FIREASPECT2_DESC"
        passives {
            MeleeRevengeDamage {
                damage 0

                effects {
                    //Burn 1 //burn gets added here with the other effect
                    VisualFXTile BurnTrigger
                }
            
                elements [
                    Fire
                ]
            }
            InnateElement Fire
            ElementImmune Fire
            StatusImmunity [Burn]

            AddStatusToElementDamage {
                element Fire
                Burn 3
            }
            AddDamageToElementDamage {
                element Fire
                damage 2
            }
        }
    }
}
```

---

### `IceArmor`
**Name:** Ice Aspect  
**Description:** Ice immunity. You can damage frozen units.
Units that contact you take 1 Ice Damage, Slow 2, and have a 5% chance to Freeze.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_ICEASPECT2_DESC`: "+2 Brace. Ice immunity. You can damage frozen units. <br/> Units that contact you take 3 Ice Damage, Slow 2, and have a 15% chance to Freeze."

```
IceArmor {
    name "PASSIVE_ICEASPECT_NAME"
    desc "PASSIVE_ICEASPECT_DESC"
    class Mage

    1 {
        passives {
            MeleeRevengeDamage {
                damage 1

                effects {
                    Slow 2
                    Freeze [1, .05]

                    VisualFXTile IcePoof
                }
            
                elements [
                    Ice
                ]
            }
            InnateElement Ice
            ElementImmune Ice
            StatusImmunity [Freeze, Slow]

            FreezePiercing 1
        }
    }
    2 {
        desc "PASSIVE_ICEASPECT2_DESC"
        passives {
            MeleeRevengeDamage {
                damage 3

                effects {
                    Slow 2
                    Freeze [1, .15]

                    VisualFXTile IcePoof
                }
            
                elements [
                    Ice
                ]
            }
            InnateElement Ice
            ElementImmune Ice
            StatusImmunity [Freeze, Slow]

            FreezePiercing 1
            Brace 2
        }
    }
}
```

---

### `Resonance`
**Name:** Resonance  
**Description:** When you cast a spell gain +1 Magic Damage for the rest of the turn.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_RESONANCE2_DESC`: "When you cast a spell gain +1 Magic Damage and +1 Damage for the rest of the turn."

```
Resonance {
    name "PASSIVE_RESONANCE_NAME"
    desc "PASSIVE_RESONANCE_DESC"
    class Mage

    1 {
        passives {
            StatusAfterCastSpell {
                TempSpellDamageUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_RESONANCE2_DESC"
        passives {
            StatusAfterCastSpell {
                TempSpellDamageUp 1
                TempDamageUp 1
            }
        }
    }
}
```

---

### `LearnFromMe`
**Name:** Learn From Me  
**Description:** When you cast a spell, all allied cats gain that spell in their bonus slot.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_LEARNFROMME2_DESC`: "When you cast a spell, all allied cats gain the upgraded version of that spell in their bonus slot."

```
LearnFromMe {
    name "PASSIVE_LEARNFROMME_NAME"
    desc "PASSIVE_LEARNFROMME_DESC"
    class Mage

    1 {
        passives {
            ConjureCastSpellsForAllies 1
        }
    }
    2 {
        desc "PASSIVE_LEARNFROMME2_DESC"
        passives {
            ConjureCastSpellsForAllies 2
        }
    }
}
```

---

### `LightningArmor`
**Name:** Lightning Aspect  
**Description:** Electric immunity.
When you deal Electric Damage, gain +1 Charge.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_LIGHTNINGASPECT2_DESC`: "Electric immunity. <br/> When you deal Electric Damage, gain +1 Charge for each point of damage dealt."

```
LightningArmor {
    name "PASSIVE_LIGHTNINGASPECT_NAME"
    desc "PASSIVE_LIGHTNINGASPECT_DESC"
    class Mage

    1 {
        passives {
            InnateElement Electric
            ElementImmune Electric
            LightningAspectCharge 0
        }
    }
    2 {
        desc "PASSIVE_LIGHTNINGASPECT2_DESC"
        passives {
            InnateElement Electric
            ElementImmune Electric
            LightningAspectCharge 1
        }
    }
}
```

---

### `LongCast`
**Name:** Long Cast  
**Description:** Tile-targeted spells gain +5 Range.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_LONGCAST2_DESC`: "+2 Magic Damage. Tile-targeted spells gain +10 Range."

```
LongCast {
    name "PASSIVE_LONGCAST_NAME"
    desc "PASSIVE_LONGCAST_DESC"
    class Mage

    1 {
        passives {
            IncreaseSpellRange 5
        }
    }
    2 {
        desc "PASSIVE_LONGCAST2_DESC"
        passives {
            IncreaseSpellRange 10
            AddSpellDamage 1
        }
    }
}
```

---

### `LightUpTheStage`
**Name:** Light Up the Stage  
**Description:** At the end of your turn, emit 2 Sparkles for each turn you've taken.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_LIGHTUPTHESTAGE2_DESC`: "At the end of your turn, emit 4 Sparkles for each turn you've taken and gain +1 Kinetic Spikes ."

```
LightUpTheStage {
    name "PASSIVE_LIGHTUPTHESTAGE_NAME"
    desc "PASSIVE_LIGHTUPTHESTAGE_DESC"
    class Mage

    1 {
        passives {
            StatusEachTurnEndForEachTurn {
                RandomMagicMissile 2
            }
        }
    }
    2 {
        desc "PASSIVE_LIGHTUPTHESTAGE2_DESC"
        passives {
            StatusEachTurnEndForEachTurn {
                RandomMagicMissile 4
            }
            StatusEachTurnEnd {
                KineticSpikes 1
            }
        }
    }
}
```

---

### `ElementalAttunement`
**Name:** Elemental Attunement  
**Description:** Casting elemental spells imbues your basic attack with those elements and relevant effects for the rest of the battle.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_ELEMENTALATTUNEMENT2_DESC`: "Casting elemental spells imbues your basic attack with those elements and relevant effects for the rest of the battle. <br/> Elemental spells cost -2 mana."

```
ElementalAttunement {
    name "PASSIVE_ELEMENTALATTUNEMENT_NAME"
    desc "PASSIVE_ELEMENTALATTUNEMENT_DESC"
    class Mage

    1 {
        passives {
            ElementalAttunement {
                Fire {
                    Burn X
                }
                Ice {
                    Slow X
                }
                Electric {
                    Stun [1 .1*X]
                }
                Earth {
                    damage X
                }
                Wind {
                    knockback X
                }
                Water {
                    AOEPuddle X-1
                }
                Grass {
                    Poison X
                }
                Holy {
                    FlatLeech X
                }
                /*Explosion { //Fireball has Explosion element so it makes the combo weird, explosion isnt really an element anyway
                    HitExplosion X
                }
                Musical {(cause that shows as an element icon on spells)
                }*/
                Gravity {
                    Weakness X
                }
                Shadow { //do we even have shadow spells?
                    crit_chance .05*X
                }
            }
        }
    }
    2 {
        desc "PASSIVE_ELEMENTALATTUNEMENT2_DESC"
        
        passives {
            ElementalAttunement {
                Fire {
                    Burn X
                }
                Ice {
                    Slow X
                }
                Electric {
                    Stun [1 .1*X]
                }
                Earth {
                    damage X
                }
                Wind {
                    knockback X
                }
                Water {
                    AOEPuddle X-1
                }
                Grass {
                    Poison X
                }
                Holy {
                    FlatLeech X
                }
                /*Explosion { //Fireball has Explosion element so it makes the combo weird, explosion isnt really an element anyway
                    HitExplosion X
                }
                Musical {(cause that shows as an element icon on spells)
                }*/
                Gravity {
                    Weakness X
                }
                Shadow { //do we even have shadow spells?
                    crit_chance .05*X
                }
            }
            ElementalManaCostReduction {
                element [Fire Ice Electric Earth Wind Water Grass Holy Gravity]
                reduction 2
            }
        }
    }
}
```

---

### `LatentEnergy`
**Name:** Latent Energy  
**Description:** When an ally spends mana, Gain +2 Magic Damage until the next time you use magic.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_LATENTENERGY2_DESC`: "When an ally spends mana, Gain +2 Magic Damage until the next time you use magic, and gain +2 mana."

```
LatentEnergy {
    name "PASSIVE_LATENTENERGY_NAME"
    desc "PASSIVE_LATENTENERGY_DESC"
    class Mage

    1 {
        passives {
            StatusWhenAllySpendsMana {
                OneUseSpellDamageUp 2
            }
        }
    }
    2 {
        desc "PASSIVE_LATENTENERGY2_DESC"
        passives {
            StatusWhenAllySpendsMana {
                OneUseSpellDamageUp 2
                ManaGain 2
            }
        }
    }
}
```

---

### `Five`
**Name:** Five  
**Description:** When you end your turn with exactly 5 mana or HP, gain +5 [img:shield] and temporarily gain +5 Kinetic Spikes until the end of your next turn .  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_FIVE2_DESC`: "When you end your turn with exactly 5 mana or HP, gain +5 [img:shield], heal 5 HP and temporarily gain +5 Kinetic Spikes and +5 Damage until the end of your next turn."

```
Five {
    name "PASSIVE_FIVE_NAME"
    desc "PASSIVE_FIVE_DESC"
    class Mage

    1 {
        passives {
            StatusOnTurnEndIfManaOrHealthExact {
                mana 5

                Shield 5
                Temporary {
                    status KineticSpikes
                    stacks 5
                    turns 1
                    expires_on_end_turn true
                }
            }
        }
    }
    2 {
        desc "PASSIVE_FIVE2_DESC"
        passives {
            StatusOnTurnEndIfManaOrHealthExact {
                mana 5

                Shield 5
                HealthGain 5
                Temporary {
                    status KineticSpikes
                    stacks 5
                    turns 1
                    expires_on_end_turn true
                }
                Temporary {
                    status DamageUp
                    stacks 5
                    turns 1
                    expires_on_end_turn true
                }
            }
        }
    }
}
```

---

### `MagicGuru`
**Name:** Magic Guru  
**Description:** Your allies have +1 Mana Regeneration. When an ally spends 7+ mana to cast a spell, they gain All Stats Up.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_MAGICGURU2_DESC`: "Your allies have +1 Mana Regeneration. When an ally spends 7+ mana to cast a spell, they gain All Stats Up. When you spend mana, each ally gains +1 mana."

```
MagicGuru {
    name "PASSIVE_MAGICGURU_NAME"
    desc "PASSIVE_MAGICGURU_DESC"
    class Mage

    1 {
        passives {
            AllyManaRegenAura {
                stacks 1
                range global
            }
            StatusAllyWhenAllySpendsMana {
                threshold 7
                AllStatsUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_MAGICGURU2_DESC"
        passives {
            AllyManaRegenAura {
                stacks 1
                range global
            }
            StatusAllyWhenAllySpendsMana {
                threshold 7
                AllStatsUp 1
            }
            StatusAlliesOnSpendMana {
                ManaGain 1
            }
        }
    }
}
```

---

### `One`
**Name:** One  
**Description:** When you end your turn, if you cast exactly 1 spell, double cast your next spell.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_ONE2_DESC`: "When you end your turn, if you cast exactly 1 spell, double cast your next 2 spells."

```
One {
    name "PASSIVE_ONE_NAME"
    desc "PASSIVE_ONE_DESC"
    class Mage

    1 {
        passives {
            StatusOnTurnEndIfCastNSpells {
                spells 1

                DoubleCastSpell 1
            }
        }
    }
    2 {
        desc "PASSIVE_ONE2_DESC"
        passives {
            StatusOnTurnEndIfCastNSpells {
                spells 1

                DoubleCastSpell 2
            }
        }
    }
}
```

---

### `Two`
**Name:** Two  
**Description:** When you end your turn, if you cast exactly 2 spells, gain +1 Bonus Attack.
When you end your turn, if you have exactly 2 mana, gain +1 Bonus Attack.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_TWO2_DESC`: "When you end your turn, if you cast exactly 2 spells, gain +1 Bonus Attack and Movement. <br/> When you end your turn, if you have exactly 2 mana, gain +1 Bonus Attack and Movement."

```
Two {
    name "PASSIVE_TWO_NAME"
    desc "PASSIVE_TWO_DESC"
    class Mage

    1 {
        passives {
            StatusOnTurnEndIfManaExact {
                mana 2

                Quivered 1
            }
            StatusOnTurnEndIfCastNSpells {
                spells 2

                Quivered 1
            }
        }
    }
    2 {
        desc "PASSIVE_TWO2_DESC"
        passives {
            StatusOnTurnEndIfManaExact {
                mana 2

                Quivered 1
                MoveQuivered 1
            }
            StatusOnTurnEndIfCastNSpells {
                spells 2

                Quivered 1
                MoveQuivered 1
            }
        }
    }
}
```

---

### `Four`
**Name:** Four  
**Description:** When you end your turn with exactly 4 mana or HP, gain +1 [img:int] and +1 Magic Damage.  
**Source:** `mage_passives.gon`  

**Localization Strings:**
- `PASSIVE_FOUR2_DESC`: "When you end your turn with exactly 4 mana or HP, gain +1 [img:int], +1 Magic Damage, +1 Kinetic Spikes, and +1 Holy Shield."

```
Four {
    name "PASSIVE_FOUR_NAME"
    desc "PASSIVE_FOUR_DESC"
    class Mage

    1 {
        passives {
            StatusOnTurnEndIfManaOrHealthExact {
                mana 4

                IntelligenceUp 1
                SpellDamageUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_FOUR2_DESC"
        passives {
            StatusOnTurnEndIfManaOrHealthExact {
                mana 4

                IntelligenceUp 1
                SpellDamageUp 1
                KineticSpikes 1
                DivineShield 1
            }
        }
    }
}
```

---

## File: `medic_passives.gon`

### `HealingAura`
**Name:** Healing Aura  
**Description:** +1 Health Regeneration
Your Health Regeneration also applies to your allies.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_HEALINGAURA2_DESC`: "+2 Health Regeneration <br/> Your Health Regeneration also applies to your allies. <br/> You and your allies have uncapped HP."

```
HealingAura {
    name "PASSIVE_HEALINGAURA_NAME"
    desc "PASSIVE_HEALINGAURA_DESC"
    class Medic

    1 {
        passives {
            ShareHealthRegen 1
            HealthRegenUp 1
        }
    }
    2 {
        desc "PASSIVE_HEALINGAURA2_DESC"
        passives {
            ShareHealthRegen 1
            HealthRegenUp 2
            AllyUncappedHPAura 1
        }
    }
}
```

---

### `NaturalHealer`
**Name:** Natural Healer  
**Description:** Your heals heal for 2 extra.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_NATURALHEALER2_DESC`: "Your heals heal for 4 extra. <br/> Start each battle at full HP."

```
NaturalHealer {
    name "PASSIVE_NATURALHEALER_NAME"
    desc "PASSIVE_NATURALHEALER_DESC"
    class Medic

    1 {
        passives {
            BoostHeals 2
        }
    }
    2 {
        desc "PASSIVE_NATURALHEALER2_DESC"
        passives {
            BoostHeals 4
            HealAtStart 100%
        }
    }
}
```

---

### `Eternal`
**Name:** Eternal  
**Description:** When you are downed for the 1st time each battle, take no injuries and revive with half HP.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_ETERNAL2_DESC`: "When you are downed for the 1st time each battle, take no injuries and revive with half HP, All Stats Up 2, and immediately take an extra turn."

```
Eternal {
    name "PASSIVE_ETERNAL_NAME"
    desc "PASSIVE_ETERNAL_DESC"
    class Medic

    1 {
        passives {
            Eternal {
                stacks 1
                health_percent 50%
            }
        }
    }
    2 {
        desc "PASSIVE_ETERNAL2_DESC"
        passives {
            Eternal {
                stacks 1
                health_percent 50%
                AllStatsUp 2
                TakeExtraTurn 1
            }
        }
    }
}
```

---

### `Blessed`
**Name:** Blessed  
**Description:** Gain +1 to 2 random stats at the start of each turn.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_BLESSED2_DESC`: "+3 Health Regeneration Gain +1 to 3 random stats at the start of each turn."

```
Blessed {
    name "PASSIVE_BLESSED_NAME"
    desc "PASSIVE_BLESSED_DESC"
    class Medic

    1 {
        passives {
            StatusEachTurnBegin {
                RandomStatUp 2
            }
        }
    }
    2 {
        desc "PASSIVE_BLESSED2_DESC"
        passives {
            StatusEachTurnBegin {
                RandomStatUp 3
            }
            HealthRegenUp 3
        }
    }
}
```

---

### `EvilPatron`
**Name:** Evil Patron  
**Description:** Your healing abilities deal damage to enemies.
Gain +2 range on tile-targeted healing spells.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_EVILPATRON2_DESC`: "Your healing abilities deal damage to enemies. <br/> Holy element damage you deal is doubled. <br/> Gain +2 range on tile-targeted healing spells."

```
EvilPatron {
    name "PASSIVE_EVILPATRON_NAME"
    desc "PASSIVE_EVILPATRON_DESC"
    class Medic

    1 {
        passives {
            HealDamagesEnemies 1
            IncreaseHealingSpellRange 2
        }
    }
    2 {
        desc "PASSIVE_EVILPATRON2_DESC"
        passives {
            HolyDamageMultiplierBonus 1
            HealDamagesEnemies 1
            IncreaseHealingSpellRange 2
        }
    }
}
```

---

### `AngelicInspiration`
**Name:** Angelic Inspiration  
**Description:** When you heal an ally, they also gain +2 mana.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_ANGELICINSPIRATION2_DESC`: "When you heal an ally, they also gain mana equal to half the amount healed."

```
AngelicInspiration {
    name "PASSIVE_ANGELICINSPIRATION_NAME"
    desc "PASSIVE_ANGELICINSPIRATION_DESC"
    class Medic

    1 {
        passives {
            HealsAlsoRegenMana 2
        }
    }
    2 {
        desc "PASSIVE_ANGELICINSPIRATION2_DESC"
        passives {
            HealsAlsoRegenMana 50%
        }
        stats {
            cha 1
            int 1
        }
    }
}
```

---

### `TopOff`
**Name:** Top Off  
**Description:** When you heal another unit over their max HP, you both gain +1 [img:shield].  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_TOPOFF2_DESC`: "When you heal another unit over their max HP, you both gain +2 [img:shield]."

```
TopOff {
    name "PASSIVE_TOPOFF_NAME"
    desc "PASSIVE_TOPOFF_DESC"
    class Medic

    1 {
        passives {
            OverhealGainsBothShield 1
        }
    }
    2 {
        desc "PASSIVE_TOPOFF2_DESC"
        passives {
            OverhealGainsBothShield 2
        }
    }
}
```

---

### `SharingIsCaring`
**Name:** Sharing is Caring  
**Description:** When you pick up a non-coin pickup, allies gain the same effects.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_SHARINGISCARING2_DESC`: "When you pick up a non-coin pickup, allies gain the same effects. <br/> Start each battle with pickups nearby."

```
SharingIsCaring {
    name "PASSIVE_SHARINGISCARING_NAME"
    desc "PASSIVE_SHARINGISCARING_DESC"
    class Medic

    1 {
        passives {
            SharePickups 1
        }
        stats {
            spd 2
        }
    }
    2 {
        desc "PASSIVE_SHARINGISCARING2_DESC"
        passives {
            SharePickups 1
            SpawnOnBattleStart {
                object RandomNonCoinPickup
                number [2 4]
            }
        }
        stats {
            spd 4
        }
    }
}
```

---

### `Caretaker`
**Name:** Caretaker  
**Description:** When you heal another unit, heal yourself for half that amount.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_CARETAKER2_DESC`: "When you heal another unit, heal yourself for the same amount."

```
Caretaker {
    name "PASSIVE_CARETAKER_NAME"
    desc "PASSIVE_CARETAKER_DESC"
    class Medic

    1 {
        passives {
            Empath 50%
        }
    }
    2 {
        desc "PASSIVE_CARETAKER2_DESC"
        passives {
            Empath 100%
        }
    }
}
```

---

### `MoraleBoost`
**Name:** Morale Boost  
**Description:** Allies gain All Stats Up whenever you kill something.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_MORALEBOOST2_DESC`: "Allies gain All Stats Up whenever you kill something. <br/> When you kill something, refresh your basic attack."

```
MoraleBoost {
    name "PASSIVE_MORALEBOOST_NAME"
    desc "PASSIVE_MORALEBOOST_DESC"
    class Medic

    1 {
        passives {
            StatusAlliesOnKill {
                AllStatsUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_MORALEBOOST2_DESC"
        passives {
            StatusAlliesOnKill {
                AllStatsUp 1
            }
            StatusOnKill {
                RefreshActPoints 1
            }
        }
    }
}
```

---

### `RangedMedic`
**Name:** Ranged Medic  
**Description:** Your basic attack is a ranged lobbed attack that heals allies and damages enemies.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_RANGEDMEDIC2_DESC`: "+2 Range. Your basic attack is a ranged lobbed attack that heals allies and damages enemies."

```
RangedMedic {
    name "PASSIVE_RANGEDMEDIC_NAME"
    desc "PASSIVE_RANGEDMEDIC_DESC"
    class Medic

    1 {
        override_basic_attack BasicMedicRanged 
        stats {
            dex 2
        }
        passives {
            ReplaceBasicAttack BasicMedicRanged
        }
    }
    2 {
        desc "PASSIVE_RANGEDMEDIC2_DESC"

        override_basic_attack BasicMedicRanged 
        stats {
            dex 4
        }
        passives {
            AddBonusRange 2
            ReplaceBasicAttack BasicMedicRanged
        }
    }
}
```

---

### `Godspeed`
**Name:** Godspeed  
**Description:** When you heal something, gain +2 [img:spd].  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_GODSPEED2_DESC`: "When you heal something, gain +4 [img:spd] and +1 to a random stat."

```
Godspeed {
    name "PASSIVE_GODSPEED_NAME"
    desc "PASSIVE_GODSPEED_DESC"
    class Medic

    1 {
        passives {
            StatusOnHeal {
                SpeedUp 2
            }
        }
    }
    2 {
        desc "PASSIVE_GODSPEED2_DESC"

        passives {
            StatusOnHeal {
                SpeedUp 4
                RandomStatUp 1
            }
        }
    }
}
```

---

### `GodWarrior`
**Name:** God Warrior  
**Description:** When you kill an enemy, gain +1 [img:divineshield].  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_GODWARRIOR2_DESC`: "When you kill an enemy, gain +1 [img:divineshield] and refresh your movement action."

```
GodWarrior {
    name "PASSIVE_GODWARRIOR_NAME"
    desc "PASSIVE_GODWARRIOR_DESC"
    class Medic

    1 {
        passives {
            StatusOnKillEnemy {
                DivineShield 1
            }
        }
    }
    2 {
        desc "PASSIVE_GODWARRIOR2_DESC"
		stats {
			str 2
		}
        passives {
            StatusOnKillEnemy {
                DivineShield 1
                RefreshMovePoints 1
            }
        }
    }
}
```

---

### `BreathOfLife`
**Name:** Breath of Life  
**Description:** When you heal a downed unit, revive it.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_BREATHOFLIFE2_DESC`: "When you heal a downed unit, revive it and heal it for 3 times the number you healed."

```
BreathOfLife {
    name "PASSIVE_BREATHOFLIFE_NAME"
    desc "PASSIVE_BREATHOFLIFE_DESC"
    class Medic

    1 {
        passives {
            HealsCanRevive 1
        }
    }
    2 {
        desc "PASSIVE_BREATHOFLIFE2_DESC"

        passives {
            HealsCanRevive 3
        }
    }
}
```

---

### `ThouShaltNotKill`
**Name:** Thou Shalt Not Kill  
**Description:** When an enemy downs another unit, they take 10 holy damage.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_THOUSHALTNOTKILL2_DESC`: "When an enemy downs another unit, they take 10 holy damage and become Stunned."

```
ThouShaltNotKill {
    name "PASSIVE_THOUSHALTNOTKILL_NAME"
    desc "PASSIVE_THOUSHALTNOTKILL_DESC"
    class Medic

    1 {
        passives {
            SmiteEnemiesWhoKill {
                type spell
                damage 10

                elements [
                    Holy
                ]
            }
        }
    }
    2 {
        desc "PASSIVE_THOUSHALTNOTKILL2_DESC"

        passives {
            SmiteEnemiesWhoKill {
                type spell
                damage 10

                effects {
                    Stun 1
                }

                elements [
                    Holy
                ]
            }
        }
    }
}
```

---

### `ThouShaltNotCovet`
**Name:** Thou Shalt Not Covet  
**Description:** When an enemy takes damage from an ability, it drops a random pickup.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_THOUSHALTNOTCOVET2_DESC`: "When an enemy takes damage from an ability, it drops 2 random pickups."

```
ThouShaltNotCovet {
    name "PASSIVE_THOUSHALTNOTCOVET_NAME"
    desc "PASSIVE_THOUSHALTNOTCOVET_DESC"
    class Medic

    1 {
        passives {
            EnemiesGetPickupsKnockedOut 1
        }
    }
    2 {
        desc "PASSIVE_THOUSHALTNOTCOVET2_DESC"

        passives {
            EnemiesGetPickupsKnockedOut 2
        }
    }
}
```

---

### `BlessingOfHolyFire`
**Name:** Blessing of Holy Fire  
**Description:** Holy-element spells deal double damage to enemies instead of healing and inflict Burn 2. 
This blessing is lost when you kill a unit.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_BLESSINGOFHOLYFIRE2_DESC`: "Holy-element spells deal triple damage to enemies instead of healing and inflict Burn 3.  <br/> This blessing is lost when you kill a unit."

```
BlessingOfHolyFire {
    name "PASSIVE_BLESSINGOFHOLYFIRE_NAME"
    desc "PASSIVE_BLESSINGOFHOLYFIRE_DESC"
    class Medic

    1 {
        passives {
            PassiveUntilGetKill {
                HolyDamageBlessing {
                    damage_multiplier 2
                    Burn 2
                }
            }
        }
    }
    2 {
        desc "PASSIVE_BLESSINGOFHOLYFIRE2_DESC"
        passives {
            PassiveUntilGetKill {
                HolyDamageBlessing {
                    damage_multiplier 3
                    Burn 3
                }
            }
        }
    }
}
```

---

### `AlmsForThePoor`
**Name:** Alms for the Poor  
**Description:** When you gain coins, all allies heal +1 HP and gain +1 [img:lck].  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_ALMSFORTHEPOOR2_DESC`: "When you gain coins, you gain +1 [img:divineshield] and all allies heal HP and gain [img:lck] equal to the number of coins gained."

```
AlmsForThePoor {
    name "PASSIVE_ALMSFORTHEPOOR_NAME"
    desc "PASSIVE_ALMSFORTHEPOOR_DESC"
    class Medic

    1 {
        passives {
            StatusAlliesOnGainCoins {
                LuckUp 1
                HealthGain 1
            }
        }
    }
    2 {
        desc "PASSIVE_ALMSFORTHEPOOR2_DESC"
        passives {
            StatusAlliesOnGainCoins {
                scaled true
                LuckUp 1
                HealthGain 1
            }
            StatusOnGainCoins {
                DivineShield 1
            }
        }
    }
}
```

---

### `Purifier`
**Name:** Purifier  
**Description:** Your basic attack removes debuffs from allies.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_PURIFIER2_DESC`: "Your basic attack removes debuffs from allies and gives them All Stats Up."

```
Purifier {
    name "PASSIVE_PURIFIER_NAME"
    desc "PASSIVE_PURIFIER_DESC"
    class Medic

    1 {
        passives {
            AddStatusToBasicAttack {
                Conditional_Ally {
                    Cleanse 0
                }
            }
        }
    }
    2 {
        desc "PASSIVE_PURIFIER2_DESC"
        passives {
            AddStatusToBasicAttack {
                Conditional_Ally {
                    Cleanse 0
                    AllStatsUp 1
                }
            }
        }
    }
}
```

---

### `VeneratedTouch`
**Name:** Venerated Touch  
**Description:** Your basic attack inflicts Confusion 2 on enemies and gives +2 [img:shield] to allies.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_VENERATEDTOUCH2_DESC`: "Your basic attack inflicts Confusion 3 on enemies and has a 50% chance to Stun. It also gives +3 [img:shield] to allies and a 50% chance for All Stats Up."

```
VeneratedTouch {
    name "PASSIVE_VENERATEDTOUCH_NAME"
    desc "PASSIVE_VENERATEDTOUCH_DESC"
    class Medic

    1 {
        passives {
            AddStatusToBasicAttack {
                Conditional_Enemy {
                    Confusion 2
                }
                Conditional_Ally {
                    Shield 2
                }
            }
        }
    }
    2 {
        desc "PASSIVE_VENERATEDTOUCH2_DESC"
        passives {
            AddStatusToBasicAttack {
                Conditional_Enemy {
                    Confusion 3
                    Stun [1 .5]
                }
                Conditional_Ally {
                    Shield 3
                    AllStatsUp [1 .5]
                }
            }
        }
    }
}
```

---

### `ProtectTheWeak`
**Name:** Protect the Weak  
**Description:** Allies with 5 or fewer HP gain +50% dodge chance.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_PROTECTTHEWEAK2_DESC`: "Allies with 10 or fewer HP gain +50% dodge chance."

```
ProtectTheWeak {
    name "PASSIVE_PROTECTTHEWEAK_NAME"
    desc "PASSIVE_PROTECTTHEWEAK_DESC"
    class Medic

    1 {
        passives {
            LowHealthAllyDodgeChanceAura {
                theshold 5
                chance 50%
            }
        }
    }
    2 {
        desc "PASSIVE_PROTECTTHEWEAK2_DESC"
        passives {
            LowHealthAllyDodgeChanceAura {
                theshold 5
                chance 50%
            }
        }
    }
}
```

---

### `ThouShaltObey`
**Name:** Thou Shalt Obey  
**Description:** At the end of each round, inflict Charm on a random adjacent enemy.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_THOUSHALTOBEY2_DESC`: "At the end of each round, inflict Charm on the closest enemy."

```
ThouShaltObey {
    name "PASSIVE_THOUSHALTOBEY_NAME"
    desc "PASSIVE_THOUSHALTOBEY_DESC"
    class Medic

    1 {
        passives {
            AutocastEachRound {
                ability MedicObey
                force_display_name true
                //even_if_stunned true
            }
        }
    }
    2 {
        desc "PASSIVE_THOUSHALTOBEY2_DESC"
        passives {
            AutocastEachRound {
                ability MedicObey2
                force_display_name true
                //even_if_stunned true
            }
        }
    }
}
```

---

### `EnchantedRelic`
**Name:** Enchanted Relic  
**Description:** Your trinket's passive and active effects are doubled.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_ENCHANTEDRELIC2_DESC`: "Your trinket's passive and active effects are tripled."

```
EnchantedRelic {
    name "PASSIVE_ENCHANTEDRELIC_NAME"
    desc "PASSIVE_ENCHANTEDRELIC_DESC"
    class Medic

    1 {
        passives {
            TrinketPassiveMultiplierBonus 1
            TrinketActiveEffectsMultiplierBonus 1
        }
    }
    2 {
        desc "PASSIVE_ENCHANTEDRELIC2_DESC"
        passives {
            TrinketPassiveMultiplierBonus 2
            TrinketActiveEffectsMultiplierBonus 2
        }
    }
}
```

---

### `BlessingOfSpirit`
**Name:** Blessing of Spirit  
**Description:** When you end your turn, you and all allies heal 2 HP and gain 2 mana. This blessing is lost when you cast a spell.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_BLESSINGOFSPIRIT2_DESC`: "When you end your turn, you and all allies heal 3 HP, gain 3 mana and gain +1 to 3 random stats. This blessing is lost when you cast a spell."

```
BlessingOfSpirit {
    name "PASSIVE_BLESSINGOFSPIRIT_NAME"
    desc "PASSIVE_BLESSINGOFSPIRIT_DESC"
    class Medic

    1 {
        passives {
            PassiveUntilCastSpell {
                HealAlliesEachTurn {
                    stacks 2
                    mana 2
                    exclude_self false
                }
            }
        }
    }
    2 {
        desc "PASSIVE_BLESSINGOFSPIRIT2_DESC"
        passives {
            PassiveUntilCastSpell {
                HealAlliesEachTurn {
                    stacks 3
                    mana 3
                    exclude_self false
                }
                StatusAlliesEachTurn {
                    exclude_self false
                    RandomStatUp 3
                }
            }
        }
    }
}
```

---

### `Heathens`
**Name:** Heathens!  
**Description:** At the start of the battle, inflict Weakness 3 on all enemies.  
**Source:** `medic_passives.gon`  

**Localization Strings:**
- `PASSIVE_HEATHENS2_DESC`: "At the start of the battle, inflict Weakness 4 and Magic Weakness 4 on all enemies."

```
Heathens {
    name "PASSIVE_HEATHENS_NAME"
    desc "PASSIVE_HEATHENS_DESC"
    class Medic

    1 {
        keyword_tooltips {Weakness 1}

        passives {
            AbilityOnBattleStart Heathens
        }
    }
    2 {
        keyword_tooltips {Weakness 1 MagicWeakness 1}

        desc "PASSIVE_HEATHENS2_DESC"
        passives {
            AbilityOnBattleStart Heathens2
        }
    }
}
```

---

## File: `monk_passives.gon`

### `SafeSwitching`
**Name:** Safe Switching  
**Description:** When you switch stances, gain +2 [img:shield].  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_SAFESWITCHING2_DESC`: "When you switch stances, gain +3 [img:shield] and cleanse one stack of a random debuff."

```
SafeSwitching {
    name "PASSIVE_SAFESWITCHING_NAME"
    desc "PASSIVE_SAFESWITCHING_DESC"
    class Monk

    1 {
        passives {
            StatusOnStanceSwitch {
                Shield 2
            }
        }
    }
    2 {
        desc "PASSIVE_SAFESWITCHING2_DESC"
        passives {
            StatusOnStanceSwitch {
                Shield 3
                PartialCleanse 1
            }
        }
    }
}
```

---

### `Mixup`
**Name:** Mixup  
**Description:** When you switch stances, your next basic attack this turn is critical.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_MIXUP2_DESC`: "When you switch stances, your next basic attack this turn is critical. <br/> Critical hits you land inflict Confusion 1."

```
Mixup {
    name "PASSIVE_MIXUP_NAME"
    desc "PASSIVE_MIXUP_DESC"
    class Monk

    1 {
        passives {
            StatusOnStanceSwitch {
                NextBasicAttackCritsThisTurn 1
            }
        }
    }
    2 {
        desc "PASSIVE_MIXUP2_DESC"
        passives {
            StatusOnStanceSwitch {
                NextBasicAttackCritsThisTurn 1
            }
            CritsApplyStatus {
                Confusion 1
            }
        }
    }
}
```

---

### `Turnabout`
**Name:** Turnabout  
**Description:** Your basic melee attacks inflict Confusion 1 and make units face away from you.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_TURNABOUT2_DESC`: "Your basic melee attacks inflict Confusion 1, make units face away from you, and have a 20% chance to inflict Stun 1."

```
Turnabout {
    name "PASSIVE_TURNABOUT_NAME"
    desc "PASSIVE_TURNABOUT_DESC"
    class Monk

    1 {
        passives {
            AddStatusToBasicMeleeAttack {
                FaceAway 1
                Confusion 1
            }
        }
    }
    2 {
        desc "PASSIVE_TURNABOUT2_DESC"
        passives {
            AddStatusToBasicMeleeAttack {
                FaceAway 1
                Confusion 1
                Stun [1 .2]
            }
        }
    }
}
```

---

### `MonkeyStyle`
**Name:** Monkey Style  
**Description:** 15% chance to block damage and counter-attack.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_MONKEYSTYLE2_DESC`: "33% chance to block damage and counter-attack."

```
MonkeyStyle {
    name "PASSIVE_MONKEYSTYLE_NAME"
    desc "PASSIVE_MONKEYSTYLE_DESC"
    class Monk

    1 {
        passives {
            ChanceToBlockAndCounter 15%
        }
    }
    2 {
        desc "PASSIVE_MONKEYSTYLE2_DESC"
        passives {
            ChanceToBlockAndCounter 33%
        }
    }
}
```

---

### `BrickSkin`
**Name:** Brick Skin  
**Description:** Any [img:shield] you gain is increased by 2.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_BRICKSKIN2_DESC`: "Any [img:shield] you gain is increased by 2."

```
BrickSkin {
    name "PASSIVE_BRICKSKIN_NAME"
    desc "PASSIVE_BRICKSKIN_DESC"
    class Monk

    1 {
        passives {
            GainExtraShield 2
        }
    }
    2 {
        desc "PASSIVE_BRICKSKIN2_DESC"
        passives {
            GainExtraShield 2
        }
        shield 8
    }
}
```

---

### `JaggedEdges`
**Name:** Jagged Edges  
**Description:** When you lose [img:shield], gain +1 Thorns.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_JAGGEDEDGE2_DESC`: "When you lose [img:shield], gain that many Thorns."

```
JaggedEdges {
    name "PASSIVE_JAGGEDEDGE_NAME"
    desc "PASSIVE_JAGGEDEDGE_DESC"
    class Monk

    1 {
        passives {
            StatusOnLoseShield {
                Thorns 1
            }
        }
        shield 2
    }
    2 {
        desc "PASSIVE_JAGGEDEDGE2_DESC"
        passives {
            ScaledStatusOnLoseShield {
                Thorns 1
            }
        }
        shield 4
    }
}
```

---

### `MindBreaker`
**Name:** Mind Breaker  
**Description:** Your basic attack inflicts Magic Weakness 1.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_MINDBREAKER2_DESC`: "Your basic attack inflicts Magic Weakness 2."

```
MindBreaker {
    name "PASSIVE_MINDBREAKER_NAME"
    desc "PASSIVE_MINDBREAKER_DESC"
    class Monk

    1 {
        passives {
            AddStatusToBasicAttack {
                MagicWeakness 1
            }
        }
    }
    2 {
        desc "PASSIVE_MINDBREAKER2_DESC"
        passives {
            AddStatusToBasicAttack {
                MagicWeakness 2
            }
        }
    }
}
```

---

### `CobraStyle`
**Name:** Cobra Style  
**Description:** When an enemy moves into an adjacent tile, perform a weak melee attack on it.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_COBRASTYLE2_DESC`: "When an enemy moves into an adjacent tile, perform a weak melee attack on it, twice!"

```
CobraStyle {
    name "PASSIVE_COBRASTYLE_NAME"
    desc "PASSIVE_COBRASTYLE_DESC"
    class Monk

    1 {
        passives {
            CobraReflex BasicMonkMelee
        }
    }
    2 {
        desc "PASSIVE_COBRASTYLE2_DESC"
        passives {
            CobraReflex BasicMonkMelee
            CobraReflex BasicMonkMelee
        }
    }
}
```

---

### `Tenderize`
**Name:** Tenderize  
**Description:** Your basic melee attacks inflict Bruise 1.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_TENDERIZE2_DESC`: "Your basic melee attacks inflict Bruise 1 and have a 15% chance to inflict Stun 1."

```
Tenderize {
    name "PASSIVE_TENDERIZE_NAME"
    desc "PASSIVE_TENDERIZE_DESC"
    class Monk

    1 {
        passives {
            AddStatusToBasicMeleeAttack {
                Bruise 1
            }
        }
    }
    2 {
        desc "PASSIVE_TENDERIZE2_DESC"
        passives {
            AddStatusToBasicMeleeAttack {
                Bruise 1
                Confusion 1
                Stun [1 .15]
            }
        }
    }
}
```

---

### `LongArms`
**Name:** Long Arms  
**Description:** +1 Range and +1 Reach.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_LONGARMS2_DESC`: "+1 Range and +1 Reach."

```
LongArms {
    name "PASSIVE_LONGARMS_NAME"
    desc "PASSIVE_LONGARMS_DESC"
    class Monk

    1 {
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1
        }
    }
    2 {
        desc "PASSIVE_LONGARMS2_DESC"
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1
        }
        stats {
            str 2
            dex 2
        }
    }
}
```

---

### `SpreadThePain`
**Name:** Spread the Pain  
**Description:** Deal 2 extra damage the first time you damage each unit each turn.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_SPREADTHEPAIN2_DESC`: "Deal 2 extra damage with 100% crit chance the first time you damage each unit each turn."

```
SpreadThePain {
    name "PASSIVE_SPREADTHEPAIN_NAME"
    desc "PASSIVE_SPREADTHEPAIN_DESC"
    class Monk

    1 {
        passives {
            SpreadPainBonus 2
        }
    }
    2 {
        desc "PASSIVE_SPREADTHEPAIN2_DESC"
        passives {
            SpreadPainBonus 2
            SpreadPainBonusCrit 1
        }
    }
}
```

---

### `Harden`
**Name:** Harden  
**Description:** When you gain [img:shield], also gain temporary Brace 1.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_HARDEN2_DESC`: "When you gain [img:shield], also gain temporary Brace 1. <br/> Gain +1 [img:shield] when you hit a unit with your basic attack."

```
Harden {
    name "PASSIVE_HARDEN_NAME"
    desc "PASSIVE_HARDEN_DESC"
    class Monk

    1 {
        passives {
            StatusOnGainShield {
                Temporary {
                    status Brace
                    stacks 1
                    turns 1
                    expires_on_begin_turn true
                }
            }
        }
    }
    2 {
        desc "PASSIVE_HARDEN2_DESC"
        passives {
            StatusOnGainShield {
                Temporary {
                    status Brace
                    stacks 1
                    turns 1
                    expires_on_begin_turn true
                }
            }
            AddStatusToBasicAttack {
                ApplyToSource {
                    Shield 1
                }
            }
        }
    }
}
```

---

### `IronSkin`
**Name:** Iron Skin Technique  
**Description:** Gain +2 [img:shield] when you land a critical hit. +10% critical chance.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_IRONSKINTECHNIQUE2_DESC`: "Gain +3 [img:shield] when you land a critical hit. +25% critical chance."

```
IronSkin {
    name "PASSIVE_IRONSKINTECHNIQUE_NAME"
    desc "PASSIVE_IRONSKINTECHNIQUE_DESC"
    class Monk

    1 {
        passives {
            StatusOnCrit {
                Shield 2
            }
            CritChanceUp 10
        }
    }
    2 {
        desc "PASSIVE_IRONSKINTECHNIQUE2_DESC"
        passives {
            StatusOnCrit {
                Shield 3
            }
            CritChanceUp 25
        }
    }
}
```

---

### `JetFists`
**Name:** Jet Fists  
**Description:** Your melee attacks and abilities blow wind through the tiles they hit.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_JETFISTS2_DESC`: "Your melee attacks and abilities blow wind through the tiles they hit in a large cone."

```
JetFists {
    name "PASSIVE_JETFISTS_NAME"
    desc "PASSIVE_JETFISTS_DESC"
    class Monk

    1 {
        passives {
            AddStatusToMeleeDamage {
                DelayedWind {
                    distance 2
                }
            }
        }
    }
    2 {
        desc "PASSIVE_JETFISTS2_DESC"
        passives {
            AddStatusToMeleeDamage {
                DelayedWindCone {
                    distance 10
                }
            }
        }
    }
}
```

---

### `EnergyFists`
**Name:** Energy Fists  
**Description:** Emit a Sparkle when you use your basic attack.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_ENERGYFISTS2_DESC`: "Emit two Sparkles when you use your basic attack."

```
EnergyFists {
    name "PASSIVE_ENERGYFISTS_NAME"
    desc "PASSIVE_ENERGYFISTS_DESC"
    class Monk

    1 {
        passives {
            AddSelfStatusToBasicAttack {
                RandomMagicMissile 1
            }
        }
    }
    2 {
        desc "PASSIVE_ENERGYFISTS2_DESC"
        passives {
            AddSelfStatusToBasicAttack {
                RandomMagicMissile 1
                RandomMagicMissile 1
            }
        }
    }
}
```

---

### `Unstoppable`
**Name:** Unstoppable!  
**Description:** You're immune to knockback, Stun, Slow, and other mobility debuffs.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_UNSTOPPABLE2_DESC`: "You're immune to knockback and debuffs."

```
Unstoppable {
    name "PASSIVE_UNSTOPPABLE_NAME"
    desc "PASSIVE_UNSTOPPABLE_DESC"
    class Monk

    1 {
        passives {
            CCImmunity 1
            KnockbackImmunity 1
        }
    }
    2 {
        desc "PASSIVE_UNSTOPPABLE2_DESC"
        passives {
            CCImmunity 1
            DebuffImmunity 1
            KnockbackImmunity 1
        }
    }
}
```

---

### `UnburdenedMotion`
**Name:** Unburdened Motion  
**Description:** +1 [img:spd] and +10% dodge chance for each empty armor slot. If all of your armor slots are empty, you can use your movement action an extra time.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_UNBURDENEDMOTION2_DESC`: "+2 [img:spd] and +15% dodge chance for each empty armor slot. If all of your armor slots are empty, you gain flying and can use your movement action an extra time."

```
UnburdenedMotion {
    name "PASSIVE_UNBURDENEDMOTION_NAME"
    desc "PASSIVE_UNBURDENEDMOTION_DESC"
    class Monk

    1 {
        empty_armor_scaled_stats { //hard coded in CatData::get_bonus_stats and Character::recompute_item_effects
            spd 1
        }

        passives {
            PassiveIfEmptyHead {
                DodgeChance 10%
            }
            PassiveIfEmptyNeck {
                DodgeChance 10%
            }
            PassiveIfEmptyFace {
                DodgeChance 10%
            }
            PassiveIfAllArmorEmpty {
                ExtraMovePoints 1
            }
        }
    }
    2 {
        desc "PASSIVE_UNBURDENEDMOTION2_DESC"

        empty_armor_scaled_stats { //hard coded in CatData::get_bonus_stats and Character::recompute_item_effects
            spd 2
        }

        passives {
            PassiveIfEmptyHead {
                DodgeChance 15%
            }
            PassiveIfEmptyNeck {
                DodgeChance 15%
            }
            PassiveIfEmptyFace {
                DodgeChance 15%
            }
            PassiveIfAllArmorEmpty {
                ExtraMovePoints 1
                Flying 1
            }
        }
    }
}
```

---

### `UnburdenedStrikes`
**Name:** Unburdened Strikes  
**Description:** +10% critical hit chance and +25% critical hit damage for each empty armor slot. If all of your armor slots are empty, counter-attack whenever you get hit.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_UNBURDENEDSTRIKES2_DESC`: "+10% critical hit chance and +25% critical hit damage for each empty armor slot. If all of your armor slots are empty your critical hits inflict bruise, and counter-attack whenever you get hit."

```
UnburdenedStrikes {
    name "PASSIVE_UNBURDENEDSTRIKES_NAME"
    desc "PASSIVE_UNBURDENEDSTRIKES_DESC"
    class Monk

    1 {
        passives {
            PassiveIfEmptyHead {
                CritChanceUp 10
                AddCritMultiplier 25%
            }
            PassiveIfEmptyNeck {
                CritChanceUp 10
                AddCritMultiplier 25%
            }
            PassiveIfEmptyFace {
                CritChanceUp 10
                AddCritMultiplier 25%
            }
            PassiveIfAllArmorEmpty {
                CounterAttack attack
            }
        }
    }
    2 {
        desc "PASSIVE_UNBURDENEDSTRIKES2_DESC"

        passives {
            PassiveIfEmptyHead {
                CritChanceUp 10
                AddCritMultiplier 40%
            }
            PassiveIfEmptyNeck {
                CritChanceUp 10
                AddCritMultiplier 40%
            }
            PassiveIfEmptyFace {
                CritChanceUp 10
                AddCritMultiplier 40%
            }
            PassiveIfAllArmorEmpty {
                CounterAttack attack
                CritsApplyStatus {
                    Bruise 1
                }
            }
        }
    }
}
```

---

### `UnburdenedThoughts`
**Name:** Unburdened Thoughts  
**Description:** +1 [img:int] and +1 [img:cha] for each empty armor slot. If all of your armor slots are empty, your spells cost 1 less mana.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_UNBURDENEDTHOUGHTS2_DESC`: "+1 [img:int], +1 [img:cha], and +1 Kinetic Spikes for each empty armor slot. If all of your armor slots are empty, you have +2 Magic Damage and your spells cost 1 less mana."

```
UnburdenedThoughts {
    name "PASSIVE_UNBURDENEDTHOUGHTS_NAME"
    desc "PASSIVE_UNBURDENEDTHOUGHTS_DESC"
    class Monk

    1 {
        empty_armor_scaled_stats { //hard coded in CatData::get_bonus_stats and Character::recompute_item_effects
            int 1
            cha 1
        }

        passives {
            PassiveIfAllArmorEmpty {
                ManaCostReduction 1
            }
        }
    }
    2 {
        desc "PASSIVE_UNBURDENEDTHOUGHTS2_DESC"

        empty_armor_scaled_stats { //hard coded in CatData::get_bonus_stats and Character::recompute_item_effects
            int 1
            cha 1
        }

        passives {
            PassiveIfEmptyHead {
                KineticSpikes 1
            }
            PassiveIfEmptyNeck {
                KineticSpikes 1
            }
            PassiveIfEmptyFace {
                KineticSpikes 1
            }
            PassiveIfAllArmorEmpty {
                ManaCostReduction 1
                AddSpellDamage 2
            }
        }
    }
}
```

---

### `RunningJab`
**Name:** Running Jab  
**Description:** When you end your movement, automatically use your basic attack if an enemy is in range.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_RUNNINGJAB2_DESC`: "When you end your movement, automatically use your basic attack if an enemy is in range. You can move an extra time each turn."

```
RunningJab {
    name "PASSIVE_RUNNINGJAB_NAME"
    desc "PASSIVE_RUNNINGJAB_DESC"
    class Monk

    1 {
        passives {
            StatusOnEndMove {
                ForceAttack 1
            }
        }
    }
    2 {
        desc "PASSIVE_RUNNINGJAB2_DESC"

        passives {
            StatusOnEndMove {
                ForceAttack 1
            }
            ExtraMovePoints 1
        }
    }
}
```

---

### `PerfectTechnique`
**Name:** Perfect Technique  
**Description:** While in ranged stance, You have +1 Range and +2 Magic Damage. While in melee stance, you have +1 Brace.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_PERFECTTECHNIQUE2_DESC`: "While in ranged stance, You have +1 Range, +2 Kinetic Spikes, and +2 Magic Damage. While in melee stance, you have +2 Brace and +2 Health Regeneration."

```
PerfectTechnique {
    name "PASSIVE_PERFECTTECHNIQUE_NAME"
    desc "PASSIVE_PERFECTTECHNIQUE_DESC"
    class Monk

    1 {
        passives {
            PassiveWhileInMonkRangedStance {
                AddBonusRange 1
                AddSpellDamage 2
            }
            PassiveWhilePreviewingMonkRangedStance {
                AddBonusRange 1
            }
            PassiveWhileInMonkMeleeStance {
                Brace 1
            }
        }
    }
    2 {
        desc "PASSIVE_PERFECTTECHNIQUE2_DESC"

        passives {
            PassiveWhileInMonkRangedStance {
                AddBonusRange 2
                KineticSpikes 2
                AddSpellDamage 2
            }
            PassiveWhilePreviewingMonkRangedStance {
                AddBonusRange 2
            }
            PassiveWhileInMonkMeleeStance {
                Brace 2
                HealthRegenUp 2
            }
        }
    }
}
```

---

### `RapidFlow`
**Name:** Rapid Flow  
**Description:** When you switch stances, do a spin attack that hits all adjacent units.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_RAPIDFLOW2_DESC`: "When you switch stances, do a double spin attack that hits all adjacent units."

```
RapidFlow {
    name "PASSIVE_RAPIDFLOW_NAME"
    desc "PASSIVE_RAPIDFLOW_DESC"
    class Monk

    1 {
        passives {
            StatusOnStanceSwitch {
                ForceUseAbility RapidFlowSpin
            }
        }
    }
    2 {
        desc "PASSIVE_RAPIDFLOW2_DESC"
        passives {
            StatusOnStanceSwitch {
                ForceUseAbility RapidFlowSpin2
            }
        }
    }
}
```

---

### `CounterBarrage`
**Name:** Counter Barrage  
**Description:** When you take damage from an enemy attack, gain +1 Bonus Attack.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_COUNTERBARRAGE2_DESC`: "When you take damage from an enemy attack, gain +1 Bonus Attack and +1 Bonus Move."

```
CounterBarrage {
    name "PASSIVE_COUNTERBARRAGE_NAME"
    desc "PASSIVE_COUNTERBARRAGE_DESC"
    class Monk

    1 {
        passives {
            StatusOnTookDamageFromEnemyAbility {
                Quivered 1
            }
        }
    }
    2 {
        desc "PASSIVE_COUNTERBARRAGE2_DESC"
        passives {
            StatusOnTookDamageFromEnemyAbility {
                Quivered 1
                MoveQuivered 1
            }
        }
    }
}
```

---

### `FlowState`
**Name:** Flow State  
**Description:** When you deal damage to another unit, gain +1 [img:str] and +2 [img:dex] until the end of the turn.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_FLOWSTATE2_DESC`: "When you deal damage to another unit, gain +2 [img:str], +2 [img:dex], and +2 [img:lck] until the end of the turn."

```
FlowState {
    name "PASSIVE_FLOWSTATE_NAME"
    desc "PASSIVE_FLOWSTATE_DESC"
    class Monk

    1 {
        passives {
            StatusOnDealtDamage {
                TempStrengthUp 1
                TempDexterityUp 2
            }
        }
    }
    2 {
        desc "PASSIVE_FLOWSTATE2_DESC"
        passives {
            StatusOnDealtDamage {
                TempStrengthUp 2
                TempDexterityUp 2
                TempLuckUp 2
            }
        }
    }
}
```

---

### `DancingLights`
**Name:** Dancing Lights  
**Description:** When you switch stances, for each empty armor slot, emit a Sparkle. If all slots are empty gain +1 to a random stat.  
**Source:** `monk_passives.gon`  

**Localization Strings:**
- `PASSIVE_DANCINGLIGHTS2_DESC`: "When you switch stances, for each empty armor slot, emit a Sparkle. If all slots are empty gain +1 to a random stat. <br/> While all armor slots are empty, you have +1 Magic Damage."

```
DancingLights {
    name "PASSIVE_DANCINGLIGHTS_NAME"
    desc "PASSIVE_DANCINGLIGHTS_DESC"
    class Monk

    1 {
        passives {
            PassiveIfEmptyHead {
                StatusOnStanceSwitch {
                    RandomMagicMissile 1
                }
            }
            PassiveIfEmptyNeck {
                StatusOnStanceSwitch {
                    RandomMagicMissile 1
                }
            }
            PassiveIfEmptyFace {
                StatusOnStanceSwitch {
                    RandomMagicMissile 1
                }
            }
            PassiveIfAllArmorEmpty {
                StatusOnStanceSwitch {
                    RandomStatUp 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_DANCINGLIGHTS2_DESC"

        passives {
            PassiveIfEmptyHead {
                StatusOnStanceSwitch {
                    RandomMagicMissile 1
                }
            }
            PassiveIfEmptyNeck {
                StatusOnStanceSwitch {
                    RandomMagicMissile 1
                }
            }
            PassiveIfEmptyFace {
                StatusOnStanceSwitch {
                    RandomMagicMissile 1
                }
            }
            PassiveIfAllArmorEmpty {
                StatusOnStanceSwitch {
                    RandomStatUp 1
                }
                AddSpellDamage 1
            }
        }
    }
}
```

---

## File: `necromancer_passives.gon`

### `Vampirism`
**Name:** Vampirism  
**Description:** Your basic attack has lifesteal.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_VAMPIRISM2_DESC`: "Your basic attack has lifesteal. <br/> Your spells have 50% lifesteal."

```
Vampirism {
    name "PASSIVE_VAMPIRISM_NAME"
    desc "PASSIVE_VAMPIRISM_DESC"
    class Necromancer

    1 {
        passives {
            AddStatusToBasicAttack {
                Leech 1
            }
            NoReflection 1
        }
    }
    2 {
        desc "PASSIVE_VAMPIRISM2_DESC"
        passives {
            AddStatusToBasicAttack {
                Leech 1
            }
            AddStatusToSpells {
                LeechPercent 50
            }
            AddStatusToWeapons {
                LeechPercent 50
            }
            NoReflection 1
        }
    }
}
```

---

### `OneWithNothing`
**Name:** One With Nothing  
**Description:** If you end your turn with 0 mana, your Mana Regeneration is doubled.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_ONEWITHNOTHING2_DESC`: "If you end your turn with 0 mana, your Mana Regeneration is doubled. <br/> Bonus ability: Slit Wrists"

```
OneWithNothing {
    name "PASSIVE_ONEWITHNOTHING_NAME"
    desc "PASSIVE_ONEWITHNOTHING_DESC"
    class Necromancer

    1 {
        passives {
            ManaRegenMultiplierIfManaEmpty 2
        }
    }
    2 {
        desc "PASSIVE_ONEWITHNOTHING2_DESC"
        passives {
            ManaRegenMultiplierIfManaEmpty 2
            BonusAbility SlitWrists
        }
    }
}
```

---

### `BedBugs`
**Name:** Bed Bugs  
**Description:** You start battles with 2 beefy leech familiars.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_BEDBUGS2_DESC`: "You start battles with 4 beefy leech familiars."

```
BedBugs {
    name "PASSIVE_BEDBUGS_NAME"
    desc "PASSIVE_BEDBUGS_DESC"
    class Necromancer

    1 {
        passives {
            SpawnOnBattleStart BeefyCharmedLeech
            SpawnOnBattleStart BeefyCharmedLeech
        }
    }
    2 {
        desc "PASSIVE_BEDBUGS2_DESC"
        passives {
            SpawnOnBattleStart {
                object BeefyCharmedLeech
                number 4
            }
        }
    }
}
```

---

### `WormLord`
**Name:** Worm Lord  
**Description:** When you take damage, spawn a leech familiar.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_WORMLORD2_DESC`: "When you take damage, spawn a leech familiar. <br/> Your basic attack spawns leech familiars."

```
WormLord {
    name "PASSIVE_WORMLORD_NAME"
    desc "PASSIVE_WORMLORD_DESC"
    class Necromancer

    1 {
        passives {
            SpawnThingOnDamage {
                object CharmedLeech
                good false //its bad from the perspective of the thing attacking you, for luck calculations (this is how it works I dont know why I did it like this)
                spawn_on_death_hit false
            }
        }
    }
    2 {
        desc "PASSIVE_WORMLORD2_DESC"
        passives {
            SpawnThingOnDamage {
                object CharmedLeech
                good false //its bad from the perspective of the thing attacking you, for luck calculations (this is how it works I dont know why I did it like this)
                spawn_on_death_hit false
            }
            AddStatusToBasicAttack {
                BounceObject CharmedLeech
            }
        }
    }
}
```

---

### `InfiniteRebirth`
**Name:** Infinite Rebirth  
**Description:** At the end of each round, if there is a body on the map and you're downed, you respawn on that tile with 1 HP and +10 temporary Speed. If that body was a party member, you spawn with full HP instead.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_INFINITEREBIRTH2_DESC`: "At the end of each round, if there is a body on the map and you're downed, you respawn on that tile with 25% HP and +10 temporary Speed. If that body was a party member, you spawn with full HP instead."

```
InfiniteRebirth {
    name "PASSIVE_INFINITEREBIRTH_NAME"
    desc "PASSIVE_INFINITEREBIRTH_DESC"
    class Necromancer

    1 {
        passives {
            InfiniteRebirth {
                health 1
                playercat_health 100%
                TempSpeedUp 10
            }
        }
    }
    2 {
        desc "PASSIVE_INFINITEREBIRTH2_DESC"
        passives {
            InfiniteRebirth {
                health 25%
                playercat_health 100%
                TempSpeedUp 10
            }
        }
    }
}
```

---

### `SacrificialLamb`
**Name:** Sacrificial Lamb  
**Description:** When you're downed, allies gain All Stats Up and take an extra turn.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_SACRIFICIALLAMB2_DESC`: "When you're downed, allies gain All Stats Up and take an extra turn. <br/> You can't get injuries."

```
SacrificialLamb {
    name "PASSIVE_SACRIFICIALLAMB_NAME"
    desc "PASSIVE_SACRIFICIALLAMB_DESC"
    class Necromancer

    1 {
        passives {
            StatusAlliesOnDeath {
                AllStatsUp 1
                TakeExtraTurn 1
            }
        }
    }
    2 {
        desc "PASSIVE_SACRIFICIALLAMB2_DESC"

        passives {
            StatusAlliesOnDeath {
                AllStatsUp 1
                TakeExtraTurn 1
            }
            InjuryImmunity 1
        }
    }
}
```

---

### `DeathIncarnate`
**Name:** Servus Mortem  
**Description:** Destroy a random non-boss enemy at the start of each battle.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_SERVUSMORTEM2_DESC`: "Destroy a random enemy at the start of each battle. If this hits a boss, deal 50 damage instead."

```
DeathIncarnate {
    name "PASSIVE_SERVUSMORTEM_NAME"
    desc "PASSIVE_SERVUSMORTEM_DESC"
    class Necromancer

    1 {
        passives {
            AbilityOnBattleStart RandomReap
        }
    }
    2 {
        desc "PASSIVE_SERVUSMORTEM2_DESC"

        passives {
            AbilityOnBattleStart RandomReap2
        }
    }
}
```

---

### `OffloadPain`
**Name:** Offload Pain  
**Description:** When you heal, deal 1 damage to each enemy.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_OFFLOADPAIN2_DESC`: "When you heal, deal 2 damage to each enemy and you gain +1 Thorns."

```
OffloadPain {
    name "PASSIVE_OFFLOADPAIN_NAME"
    desc "PASSIVE_OFFLOADPAIN_DESC"
    class Necromancer

    1 {
        passives {
            DamageEnemiesOnHeal 1
        }
    }
    2 {
        desc "PASSIVE_OFFLOADPAIN2_DESC"

        passives {
            DamageEnemiesOnHeal 2

            StatusOnHealed {
                Thorns 1
            }
        }
    }
}
```

---

### `CambionConception`
**Name:** Cambion Conception  
**Description:** When you're downed, spawn a demon kitten familiar.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_CAMBIONCONCEPTION2_DESC`: "When you're downed, spawn 2 demon kitten familiars."

```
CambionConception {
    name "PASSIVE_CAMBIONCONCEPTION_NAME"
    desc "PASSIVE_CAMBIONCONCEPTION_DESC"
    class Necromancer

    1 {
        passives {
            SpawnThingOnDeath CharmedDemonKitten
        }
    }
    2 {
        desc "PASSIVE_CAMBIONCONCEPTION2_DESC"

        passives {
            SpawnThingOnDeath CharmedDemonKitten
            SpawnThingOnDeath CharmedDemonKitten
        }
    }
}
```

---

### `Leechmother`
**Name:** Leech Mother  
**Description:** Your basic attack spawns a leech familiar.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_LEECHMOTHER2_DESC`: "Your basic attack spawns a beefy leech familiar."

```
Leechmother {
    name "PASSIVE_LEECHMOTHER_NAME"
    desc "PASSIVE_LEECHMOTHER_DESC"
    class Necromancer

    1 {
        passives {
            AddStatusToBasicAttack {
                BounceObject CharmedLeech
            }
        }
    }
    2 {
        desc "PASSIVE_LEECHMOTHER2_DESC"
        passives {
            AddStatusToBasicAttack {
                BounceObject BeefyCharmedLeech
            }
        }
    }
}
```

---

### `Infected`
**Name:** Infected  
**Description:** When you down a unit, reanimate it with 50% HP.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_INFECTED2_DESC`: "When you down a unit, reanimate it with full HP."

```
Infected {
    name "PASSIVE_INFECTED_NAME"
    desc "PASSIVE_INFECTED_DESC"
    class Necromancer

    1 {
        passives {
            StatusKilledCharacters {
                AutoReanimate 50%
            }
        }
    }
    2 {
        desc "PASSIVE_INFECTED2_DESC"
        passives {
            StatusKilledCharacters {
                AutoReanimate 100%
            }
        }
    }
}
```

---

### `LastGasp`
**Name:** Last Grasp  
**Description:** When you're downed, deal 6 damage to each enemy and heal 6 HP to all allies.
Bonus ability: Seppuku  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_LASTGRASP2_DESC`: "When you're downed, deal 10 damage to each enemy and heal 10 HP to all allies. <br/> Bonus ability: Seppuku"

```
LastGasp {
    name "PASSIVE_LASTGRASP_NAME"
    desc "PASSIVE_LASTGRASP_DESC"
    class Necromancer

    1 {
        passives {
            DeathRattle {
                ability LastGasp
                pop_corpse false
            }
            BonusAbility Seppuku
        }
    }
    2 {
        desc "PASSIVE_LASTGRASP2_DESC"
        passives {
            DeathRattle {
                ability LastGasp2
                pop_corpse false
            }
            BonusAbility Seppuku
        }
    }
}
```

---

### `RelentlessDead`
**Name:** Relentless Dead  
**Description:** At the end of each round, spawn a zombie kitten familiar onto a random tile.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_RELENTLESSDEAD2_DESC`: "At the end of each round, spawn 2 zombie kitten familiars onto random tiles."

```
RelentlessDead {
    name "PASSIVE_RELENTLESSDEAD_NAME"
    desc "PASSIVE_RELENTLESSDEAD_DESC"
    class Necromancer

    1 {
        passives {
            AutocastEachRound {
                ability RaiseTheDead
                even_if_stunned true
            }
        }
    }
    2 {
        desc "PASSIVE_RELENTLESSDEAD2_DESC"
        passives {
            AutocastEachRound {
                ability RaiseTheDead2
                even_if_stunned true
            }
        }
    }
}
```

---

### `ChainsOfGuilt`
**Name:** Chains of Guilt  
**Description:** When an enemy downs you and it wasn't a boss, it joins your party permanently.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_CHAINSOFGUILT2_DESC`: "When an enemy downs you and it wasn't a boss, it joins your party permanently. If it was a boss, inflict Stun 3 on it."

```
ChainsOfGuilt {
    name "PASSIVE_CHAINSOFGUILT_NAME"
    desc "PASSIVE_CHAINSOFGUILT_DESC"
    class Necromancer

    1 {
        passives {
            StatusKillers {
                Conditional_Boss {
                    Charmed 1
                }
                Conditional_NotBoss {
                    Conditional_Enemy {
                        Conditional_PartyMember {
                            Charmed 5
                        } Else {
                            PermanentCharm 1
                            FactionConversion 1
                            CaptureFamiliar 1
                        }
                    }
                }
            }
        }
    }
    2 {
        desc "PASSIVE_CHAINSOFGUILT2_DESC"
        passives {
            StatusKillers {
                Conditional_Boss {
                    Stun 3
                }
                Conditional_NotBoss {
                    Conditional_Enemy {
                        Conditional_PartyMember {
                            Charmed 5
                        } Else {
                            PermanentCharm 1
                            FactionConversion 1
                            CaptureFamiliar 1
                        }
                    }
                }
            }
        }
    }
}
```

---

### `DarkPriest`
**Name:** Dark Priest  
**Description:** At the start of each battle, if you don't have a weapon, gain a temporary Soul Dagger weapon.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_DARKPRIEST2_DESC`: "At the start of each battle, if you don't have a weapon, gain a temporary Soul Dagger weapon. You can use your weapon action an extra time each turn."

```
DarkPriest {
    name "PASSIVE_DARKPRIEST_NAME"
    desc "PASSIVE_DARKPRIEST_DESC"
    class Necromancer

    1 {
        passives {
            EquipTemporaryItem Necro_SoulDagger_Uncharged
        }
    }
    2 {
        desc "PASSIVE_DARKPRIEST2_DESC"
        passives {
            EquipTemporaryItem Necro_SoulDagger_Uncharged
            ExtraWeaponAttacks 1
        }
    }
}
```

---

### `Undeath`
**Name:** Undeath  
**Description:** When you're downed, reanimate each ally to 33% HP. (Once per battle.)  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_UNDEATH2_DESC`: "When you're downed, reanimate each ally to max HP. (Once per battle.)"

```
Undeath {
    name "PASSIVE_UNDEATH_NAME"
    desc "PASSIVE_UNDEATH_DESC"
    class Necromancer

    1 {
        passives {
            StatusAlliesOnDeath {
                triggers_limit 1
                Reanimate 33%
            }
        }
    }
    2 {
        desc "PASSIVE_UNDEATH2_DESC"

        passives {
            StatusAlliesOnDeath {
                triggers_limit 1
                Reanimate 100%
            }
        }
    }
}
```

---

### `NumbingLeeches`
**Name:** Numbing Leeches  
**Description:** Your basic attack deals 0 damage but its status and hit effects are tripled.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_NUMBINGLEECHES2_DESC`: "Your basic attack deals 0 damage, but its status and hit effects are tripled. <br/> Your basic attack inflicts Mana Leech."

```
NumbingLeeches {
    name "PASSIVE_NUMBINGLEECHES_NAME"
    desc "PASSIVE_NUMBINGLEECHES_DESC"
    class Necromancer

    1 {
        passives {
            NumbingLeeches 3
        }
    }
    2 {
        desc "PASSIVE_NUMBINGLEECHES2_DESC"

        passives {
            NumbingLeeches 3
            AddStatusToBasicAttack {
                ManaLeeches 1
            }
        }
    }
}
```

---

### `EternalHealth`
**Name:** Eternal Health  
**Description:** Suffer only Jinxed when downed. When your party wins a battle, if you were downed, heal to full.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_ETERNALHEALTH2_DESC`: "Suffer only Jinxed when downed. When your party wins a battle, if you were downed, heal to full. Your body is indestructible. When you're downed, allies get +1 [img:lck] for each Jinxed injury you have."

```
EternalHealth {
    name "PASSIVE_ETERNALHEALTH_NAME"
    desc "PASSIVE_ETERNALHEALTH_DESC"
    class Necromancer

    1 {
        passives {
            ForceSpecificInjury lck
            ReviveOnWin 100%
        }
    }
    2 {
        desc "PASSIVE_ETERNALHEALTH2_DESC"

        passives {
            ForceSpecificInjury lck
            ReviveOnWin 100%
            AddCorpseHealth 999999
            StatusAlliesScaledByCursedOnDeath {
                //max 10
                LuckUp 1
            }
        }
    }
}
```

---

### `Torpor`
**Name:** Torpor  
**Description:** While you're downed, your basic attack is Haunt. Your body gains +6 corpse HP.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_TORPOR2_DESC`: "While you're downed, your basic attack is Haunt and your spells are Spook. Your body gains +6 corpse HP."

```
Torpor {
    name "PASSIVE_TORPOR_NAME"
    desc "PASSIVE_TORPOR_DESC"
    class Necromancer

    1 {
        passives {
            ReplaceBasicAttackWhenDead Haunt
            AddCorpseHealth 6
        }
    }
    2 {
        desc "PASSIVE_TORPOR2_DESC"

        passives {
            ReplaceBasicAttackWhenDead Haunt
            ReplaceSpellsWhenDead Spook
            AddCorpseHealth 6
        }
    }
}
```

---

### `SoulBound`
**Name:** Soul Bond  
**Description:** Your basic attack inflicts Soul Link.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_SOULBOND2_DESC`: "Your basic attack inflicts Soul Link. Inflict Soul Link on a random enemy at the start of the battle."

```
SoulBound {
    name "PASSIVE_SOULBOND_NAME"
    desc "PASSIVE_SOULBOND_DESC"
    class Necromancer

    1 {
        passives {
            AddStatusToBasicAttack {
                SoulLink 1
            }
        }
    }
    2 {
        desc "PASSIVE_SOULBOND2_DESC"

        passives {
            AddStatusToBasicAttack {
                SoulLink 1
            }
            AbilityOnBattleStart RandomSoulLink
        }
    }
}
```

---

### `Superstition`
**Name:** Superstition  
**Description:** Your basic attack inflicts -1[img:lck]. 
When a unit damages you, inflict -1[img:lck] on it.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_SUPERSTITION2_DESC`: "Your basic attack inflicts -1[img:lck] and has a 15% chance to inflict Fear. <br/> When a unit damages you, inflict -1[img:lck] and a 15% to Fear on it."

```
Superstition {
    name "PASSIVE_SUPERSTITION_NAME"
    desc "PASSIVE_SUPERSTITION_DESC"
    class Necromancer

    1 {
        passives {
            AddStatusToBasicAttack {
                LuckUp -1
            }
            StatusDamagers {
                LuckUp -1
            }
        }
    }
    2 {
        desc "PASSIVE_SUPERSTITION2_DESC"

        passives {
            AddStatusToBasicAttack {
                LuckUp -1
                Fear [1 .25]
            }
            StatusDamagers {
                LuckUp -1
                Fear [1 .25]
            }
        }
    }
}
```

---

### `ImmortalLeeches`
**Name:** Immortal Leeches  
**Description:** When a unit you inflicted Leeches on dies or loses its leeches, your next basic attack inflicts that many additional leeches.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_IMMORTALLEECHES2_DESC`: "When a unit you inflicted Leeches on dies or loses its leeches, your next basic attack inflicts that many additional leeches. <br/> Your basic attack inflicts +1 leech."

```
ImmortalLeeches {
    name "PASSIVE_IMMORTALLEECHES_NAME"
    desc "PASSIVE_IMMORTALLEECHES_DESC"
    class Necromancer

    1 {
        passives {
            ImmortalLeeches 1
        }
    }
    2 {
        desc "PASSIVE_IMMORTALLEECHES2_DESC"

        passives {
            ImmortalLeeches 1
            AddStatusToBasicAttack {
                Leeches 1
            }
        }
    }
}
```

---

### `CorpseConnoisseur`
**Name:** Corpse Connoisseur  
**Description:** Start each battle with 2-3 corpses near you.
When you destroy a corpse, heal 2 HP and spawn a food pickup.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_CORPSECONNOISSEUR2_DESC`: "Start each battle with 3-4 corpses near you. <br/> When you destroy a corpse, heal 8 HP and spawn a food pickup."

```
CorpseConnoisseur  {
    name "PASSIVE_CORPSECONNOISSEUR_NAME"
    desc "PASSIVE_CORPSECONNOISSEUR_DESC"
    class Necromancer

    1 {
        passives {
            SpawnOnBattleStart {
                number [2 3]
                object chapter_corpse_medium
            }
            SpawnObjectOnPopCorpse Food
            StatusOnPopCorpse {
                HealthGain 2
            }
        }
    }
    2 {
        desc "PASSIVE_CORPSECONNOISSEUR2_DESC"

        passives {
            SpawnOnBattleStart {
                number [3 4]
                object chapter_corpse_medium
            }
            SpawnObjectOnPopCorpse Food
            StatusOnPopCorpse {
                HealthGain 8
            }
        }
    }
}
```

---

### `Parasitic`
**Name:** Parasitic  
**Description:** When you gain health, spawn a leech familiar.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_PARASITIC2_DESC`: "When you gain health, spawn a leech familiar. 50% of the time, spawn a beefy leech instead."

```
Parasitic {
    name "PASSIVE_PARASITIC_NAME"
    desc "PASSIVE_PARASITIC_DESC"
    class Necromancer

    1 {
        passives {
            StatusOnHealed {
                ObjectOnHitCharacter CharmedLeech
            }
        }
    }
    2 {
        desc "PASSIVE_PARASITIC2_DESC"

        passives {
            StatusOnHealed {
                RandomStatusFromPool {
                    ObjectOnHitCharacter CharmedLeech
                    ObjectOnHitCharacter BeefyCharmedLeech
                }
            }
        }
    }
}
```

---

### `SpreadSorrow`
**Name:** Spread Sorrow  
**Description:** When you inflict a debuff to an enemy, inflict that same debuff on another random enemy.  
**Source:** `necromancer_passives.gon`  

**Localization Strings:**
- `PASSIVE_SPREADSORROW2_DESC`: "When you inflict a debuff to an enemy, inflict that same debuff on 2 other random enemies."

```
SpreadSorrow {
    name "PASSIVE_SPREADSORROW_NAME"
    desc "PASSIVE_SPREADSORROW_DESC"
    class Necromancer

    1 {
        passives {
            SpreadExtraDebuffs 1
        }
    }
    2 {
        desc "PASSIVE_SPREADSORROW2_DESC"

        passives {
            SpreadExtraDebuffs 2
        }
    }
}
```

---

## File: `psychic_passives.gon`

### `Flying`
**Name:** Antigravity  
**Description:** You have Flying Movement. When you use a Gravity element ability gain +1 [img:spd].
Gravity element spells cost -1 mana.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_FLYING2_DESC`: "You have Flying Movement. When you use a Gravity element ability gain +2 [img:spd]. <br/> Gravity element spells cost -2 mana."

```
Flying {
    name "PASSIVE_FLYING_NAME"
    desc "PASSIVE_FLYING_DESC"
    class Psychic

    1 {
        passives {
            Flying 1
            StatusOnUseElementAbility {
                element Gravity
                SpeedUp 1
            }
            ElementalManaCostReduction {
                element Gravity
                reduction 1
            }
        }
    }
    2 {
        desc "PASSIVE_FLYING2_DESC"
        passives {
            Flying 1
            ExtraMovePoints 1
            StatusOnUseElementAbility {
                element Gravity
                SpeedUp 2
            }
            ElementalManaCostReduction {
                element Gravity
                reduction 2
            }
        }
    }
}
```

---

### `SoulShatter`
**Name:** Soul Shatter  
**Description:** When you kill a unit, deal 1 damage to all enemies.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_SOULSHATTER2_DESC`: "When you kill a unit, deal 2 damage to all enemies."

```
SoulShatter {
    name "PASSIVE_SOULSHATTER_NAME"
    desc "PASSIVE_SOULSHATTER_DESC"
    class Psychic

    1 {
        passives {
            DamageEnemiesOnKill 1
        }
    }
    2 {
        desc "PASSIVE_SOULSHATTER2_DESC"
        passives {
            DamageEnemiesOnKill 2
        }
    }
}
```

---

### `Glow`
**Name:** Glow  
**Description:** Your basic attack inflicts Blind.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_GLOW2_DESC`: "All damage you deal inflicts Blind."

```
Glow {
    name "PASSIVE_GLOW_NAME"
    desc "PASSIVE_GLOW_DESC"
    class Psychic

    1 {
        passives {
            AddStatusToBasicAttack {
                Blind 1
            }
        }
    }
    2 {
        desc "PASSIVE_GLOW2_DESC"
        passives {
            AddStatusToAllDamage {
                Blind 1
            }
        }
    }
}
```

---

### `Blink`
**Name:** Blink  
**Description:** 33% chance to teleport to a random tile when targeted by an enemy.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_BLINK2_DESC`: "50% chance to teleport to a random tile when targeted by an enemy."

```
Blink {
    name "PASSIVE_BLINK_NAME"
    desc "PASSIVE_BLINK_DESC"
    class Psychic

    1 {
        passives {
            ChanceToBackflip {
                ability BlinkDodge
                chance 33%
            }
        }
    }
    2 {
        desc "PASSIVE_BLINK2_DESC"
        passives {
            ChanceToBackflip {
                ability BlinkDodge
                chance 50%
            }
        }
    }
}
```

---

### `FullPower`
**Name:** Full Power  
**Description:** While at full mana, your basic attack deals triple damage and has +3 Knockback.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_FULLPOWER2_DESC`: "While at full mana, your basic attack deals triple damage and has +3 Knockback. <br/> Bonus Ability: Grow Head."

```
FullPower {
    name "PASSIVE_FULLPOWER_NAME"
    desc "PASSIVE_FULLPOWER_DESC"
    class Psychic

    1 {
        passives {
            FullPower 3
        }
    }
    2 {
        desc "PASSIVE_FULLPOWER2_DESC"
        passives {
            FullPower 3
            BonusAbility GrowHead
        }
    }
}
```

---

### `RealityShatter`
**Name:** Reality Shatter  
**Description:** Gravity element abilities spawn Floating Glass.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_REALITYSHATTER2_DESC`: "Gravity element abilities spawn Floating Glass and inflict Bleed 1."

```
RealityShatter {
    name "PASSIVE_REALITYSHATTER_NAME"
    desc "PASSIVE_REALITYSHATTER_DESC"
    class Psychic

    1 {
        passives {
            AddStatusToElementAbilities {
                element Gravity
                ChangeTile FloatingGlassTile
            }
        }
    }
    2 {
        desc "PASSIVE_REALITYSHATTER2_DESC"
        passives {
            AddStatusToElementAbilities {
                element Gravity
                ChangeTile FloatingGlassTile
                Bleed 1
            }
        }
    }
}
```

---

### `MentalStorm`
**Name:** Mental Storm  
**Description:** Gain +1 Charge when you cast a spell.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_MENTALSTORM2_DESC`: "Gain +2 Charge when you cast a spell."

```
MentalStorm {
    name "PASSIVE_MENTALSTORM_NAME"
    desc "PASSIVE_MENTALSTORM_DESC"
    class Psychic

    1 {
        passives {
            StatusOnCastSpell {
                Charge 1
            }
        }
    }
    2 {
        desc "PASSIVE_MENTALSTORM2_DESC"
        passives {
            StatusOnCastSpell {
                Charge 2
            }
        }
    }
}
```

---

### `Wither`
**Name:** Wither  
**Description:** Gravity element abilities inflict a random negative status effect when used on enemies.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_WITHER2_DESC`: "Gravity element abilities inflict a random negative status effect when used on enemies. When you inflict a negative status effect, inflict +1 of that status effect."

```
Wither {
    name "PASSIVE_WITHER_NAME"
    desc "PASSIVE_WITHER_DESC"
    class Psychic

    1 {
        keyword_tooltips {} //empty keyword tooltips field should prevent them from being automatically scanned
        passives {
            AddStatusToElementAbilities {
                element Gravity
                Conditional_Enemy {
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
                    }
                }
            }
        }
    }
    2 {
        desc "PASSIVE_WITHER2_DESC"
        keyword_tooltips {}
        passives {
            AmplifyNegativeStatus 1

            AddStatusToElementAbilities {
                element Gravity
                Conditional_Enemy {
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
                        AllStatsUp -1
                    }
                }
            }
        }
    }
}
```

---

### `Flourish`
**Name:** Flourish  
**Description:** Gravity element abilities do not harm allies. Gravity element abilities give a random positive status effect when used on allies. When you inflict a positive status effect, inflict +1 of that status effect.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_FLOURISH2_DESC`: "Gravity element abilities do not harm allies. Gravity element abilities give a random positive status effect when used on allies. When you inflict a positive status effect, inflict +2 of that status effect."

```
Flourish {
    name "PASSIVE_FLOURISH_NAME"
    desc "PASSIVE_FLOURISH_DESC"
    class Psychic

    1 {
        keyword_tooltips {}
        passives {
            AddStatusToElementAbilities {
                element Gravity
                Conditional_Ally {
                    ClearNegativeEffects 1
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
                    }
                }
            }

            AmplifyPositiveStatus 1
        }
    }
    2 {
        desc "PASSIVE_FLOURISH2_DESC"
        keyword_tooltips {}
        passives {
            AddStatusToElementAbilities {
                element Gravity
                Conditional_Ally {
                    ClearNegativeEffects 1
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
                    }
                }
            }

            AmplifyPositiveStatus 2
        }
    }
}
```

---

### `PsySmack`
**Name:** Psy Smack  
**Description:** Knockback damage you and your allies deal is doubled.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_PSYSMACK2_DESC`: "Knockback damage and distance you and your allies deal is doubled and has Chain Knockback."

```
PsySmack {
    name "PASSIVE_PSYSMACK_NAME"
    desc "PASSIVE_PSYSMACK_DESC"
    class Psychic

    1 {
        passives {
            AllyMultiplyKnockbackDamage 2
        }
    }
    2 {
        desc "PASSIVE_PSYSMACK2_DESC"
        passives {
            AllyMultiplyKnockbackDamage 2
            AllyMultiplyKnockbackDistance 2
            AllyChainKnockback 1
        }
    }
}
```

---

### `Beckon`
**Name:** Beckon  
**Description:** Your basic attack has +4 Knockback.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_BECKON2_DESC`: "Your basic attack has +4 Knockback and Chain Knockback."

```
Beckon { //todo: do something with gravity spells as well
    name "PASSIVE_BECKON_NAME"
    desc "PASSIVE_BECKON_DESC"
    class Psychic

    1 {
        passives {
            AddStatusToBasicAttack {
                Knockback 4
            }
        }
    }
    2 {
        desc "PASSIVE_BECKON2_DESC"
        passives {
            AddStatusToBasicAttack {
                Knockback 4
                OverrideChainKnockback 0
                OverrideChainKnockbackDamage 0
            }
        }
    }
}
```

---

### `MindTempest`
**Name:** Mind Tempest  
**Description:** After every sixth spell you cast, gain All Stats Up and +1 Magic Damage.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_MINDTEMPEST2_DESC`: "After every sixth spell you cast, gain All Stats Up, +1 Magic Damage, and reduce the cost of your spells by 1 mana."

```
MindTempest {
    name "PASSIVE_MINDTEMPEST_NAME"
    desc "PASSIVE_MINDTEMPEST_DESC"
    class Psychic

    1 {
        passives {
            StatusEveryXSpellCasts {
                stacks 6
                AllStatsUp 1
                SpellDamageUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_MINDTEMPEST2_DESC"
        passives {
            StatusEveryXSpellCasts {
                stacks 6
                AllStatsUp 1
                ReduceManaCost 1
                SpellDamageUp 1
            }
        }
    }
}
```

---

### `Overflow`
**Name:** Overflow  
**Description:** While at full mana, gain +2 Brace and Flying Movement. Your mana is uncapped.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_OVERFLOW2_DESC`: "While at full mana, gain +2 Brace and Teleportation. Your mana is uncapped."

```
Overflow {
    name "PASSIVE_OVERFLOW_NAME"
    desc "PASSIVE_OVERFLOW_DESC"
    class Psychic

    1 {
        passives {
            PassiveWhenAtFullMana {
                Brace 2
                Flying 1
            }
            UncappedMana 1
        }
    }
    2 {
        desc "PASSIVE_OVERFLOW2_DESC"
        passives {
            PassiveWhenAtFullMana {
                Brace 3
                Flying 1
                AddMovement 20
                ReplaceBasicMove Teleport
            }
            UncappedMana 1
        }
    }
}
```

---

### `Omniscience`
**Name:** Omniscience  
**Description:** You can see EVERYTHING. Line of sight restrictions are ignored.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_OMNISCIENCE2_DESC`: "You can see EVERYTHING. Line of sight restrictions are ignored."

```
Omniscience {
    name "PASSIVE_OMNISCIENCE_NAME"
    desc "PASSIVE_OMNISCIENCE_DESC"
    class Psychic

    1 {
        passives {
            RemoveLineOfSightRestrictions 1
            ShowHiddenThings 1
        }
    }
    2 {
        desc "PASSIVE_OMNISCIENCE2_DESC"
        passives {
            RemoveLineOfSightRestrictions 1
            ShowHiddenThings 1
        }
        stats {
            int 4
        }
    }
}
```

---

### `PsionicRepel`
**Name:** Psionic Repel  
**Description:** Units that attack or contact you get knocked back 10 tiles.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_PSIONICREPEL2_DESC`: "Units that attack or contact you get knocked back 10 tiles and are Immobilized."

```
PsionicRepel {
    name "PASSIVE_PSIONICREPEL_NAME"
    desc "PASSIVE_PSIONICREPEL_DESC"
    class Psychic

    1 {
        passives {
            RevengeDamage {
                knockback 10
            }
        }
    }
    2 {
        desc "PASSIVE_PSIONICREPEL2_DESC"
        passives {
            RevengeDamage {
                knockback 10

                effects {
                    Immobile 1
                }
            }
        }
    }
}
```

---

### `Enlightened`
**Name:** Enlightened  
**Description:** While at full mana, the first spell you cast each turn is free.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_ENLIGHTENED2_DESC`: "While at full mana, all of your spells are free to cast once a turn."

```
Enlightened {
    name "PASSIVE_ENLIGHTENED_NAME"
    desc "PASSIVE_ENLIGHTENED_DESC"
    class Psychic

    1 {
        passives {
            FreeSpellsAtFullMana 1
        }
    }
    2 {
        desc "PASSIVE_ENLIGHTENED2_DESC"
        passives {
            EachSpellFreeAtFullMana 1
        }
    }
}
```

---

### `MadVisage`
**Name:** Mad Visage  
**Description:** All injuries you get are Disfigured.
While at full mana, your basic action inflicts Madness.
While you have 0 or less [img:cha] you can attack an additional time each turn.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_MADVISAGE2_DESC`: "All injuries you get are Disfigured. <br/> Units that contact or attack you get Madness. <br/> While at full mana, your basic attack inflicts Madness. <br/> While at 0 [img:cha] you can attack 2 additional times each turn."

```
MadVisage {
    name "PASSIVE_MADVISAGE_NAME"
    desc "PASSIVE_MADVISAGE_DESC"
    class Psychic

    1 {
        passives {
            ForceSpecificInjury cha

            PassiveWhenAtFullMana {
                AddStatusToBasicAttack {
                    Madness 1
                }
            }
            PassiveAtStatThreshold {
                mode less_or_equal
                threshold {
                    cha 0
                }
                passives {
                    ExtraBasicAttacks 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_MADVISAGE2_DESC"

        passives {
            ForceSpecificInjury cha

            PassiveWhenAtFullMana {
                AddStatusToBasicAttack {
                    Madness 1
                }
            }
            PassiveAtStatThreshold {
                mode less_or_equal
                threshold {
                    cha 0
                }
                passives {
                    ExtraBasicAttacks 2
                }
            }
            RevengeDamage {
                effects {
                    Madness 1
                }
            }
        }
    }
}
```

---

### `PowerUp`
**Name:** Power Up  
**Description:** When you gain excess mana, gain +1 Magic Damage and +1 [img:int].  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_POWERUP2_DESC`: "When you gain excess mana, gain +1 Magic Damage, +1 [img:int]. and +1 [img:divineshield]."

```
PowerUp {
    name "PASSIVE_POWERUP_NAME"
    desc "PASSIVE_POWERUP_DESC"
    class Psychic

    1 {
        passives {
            StatusOnOverMana {
                SpellDamageUp 1
                IntelligenceUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_POWERUP2_DESC"

        passives {
            StatusOnOverMana {
                SpellDamageUp 1
                IntelligenceUp 1
                DivineShield 1
            }
        }
    }
}
```

---

### `TrueSight`
**Name:** True Sight  
**Description:** You and your allies can't miss enemies within your line of sight.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_TRUESIGHT2_DESC`: "You and your allies can't miss enemies within your line of sight. Allied physical attacks gain +50% critical hit chance against those enemies."

```
TrueSight {
    name "PASSIVE_TRUESIGHT_NAME"
    desc "PASSIVE_TRUESIGHT_DESC"
    class Psychic

    1 {
        passives {
            LineOfSightTrueSightAura 0
        }
    }
    2 {
        desc "PASSIVE_TRUESIGHT2_DESC"
        passives {
            LineOfSightTrueSightAura .5
        }
    }
}
```

---

### `Radiation`
**Name:** Braingeyser  
**Description:** When you gain excess mana, emit that many Sparkles.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_BRAINGEYSER2_DESC`: "When you gain excess mana, emit that many Sparkles and remove all your debuffs."

```
Radiation {
    name "PASSIVE_BRAINGEYSER_NAME"
    desc "PASSIVE_BRAINGEYSER_DESC"
    class Psychic

    1 {
        passives {
            ScaledStatusOnOverMana {
                RandomMagicMissile 1
            }
        }
    }
    2 {
        desc "PASSIVE_BRAINGEYSER2_DESC"
        passives {
            ScaledStatusOnOverMana {
                RandomMagicMissile 1
                Cleanse 0
            }
        }
    }
}
```

---

### `GravityWell`
**Name:** Gravity Well  
**Description:** When a unit is knocked through a tile adjacent to you, stop it and inflict Stun.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_GRAVITYWELL2_DESC`: "When a unit is knocked through a tile adjacent to you, stop it, inflict Stun and deal 5 damage to it."

```
GravityWell {
    name "PASSIVE_GRAVITYWELL_NAME"
    desc "PASSIVE_GRAVITYWELL_DESC"
    class Psychic

    1 {
        passives {
            GravityWell {
                damage 0
                cant_miss true
                type status

                effects {
                    Stun 1
                }
                elements [
                    Gravity
                ]
            }
        }
    }
    2 {
        desc "PASSIVE_GRAVITYWELL2_DESC"
        passives {
            GravityWell {
                damage 5
                cant_miss true
                type status

                effects {
                    Stun 1
                }
                elements [
                    Gravity
                ]
            }
        }
    }
}
```

---

### `Drag`
**Name:** Drag  
**Description:** Units that you knockback take 1 damage for each tile they pass through.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_DRAG2_DESC`: "Units that you knockback take 2 damage for each tile they pass through."

```
Drag {
    name "PASSIVE_DRAG_NAME"
    desc "PASSIVE_DRAG_DESC"
    class Psychic

    1 {
        passives {
            StatusThingsKnockedBack {
                Drag 1
            }
        }
    }
    2 {
        desc "PASSIVE_DRAG2_DESC"
        passives {
            StatusThingsKnockedBack {
                Drag 2
            }
        }
    }
}
```

---

### `Twiddle`
**Name:** Twiddle  
**Description:** Your basic attack deals 0 damage, but you can use it 2 additional times each turn.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_TWIDDLE2_DESC`: "Start each battle with +5 Bonus Attacks. Your basic attack deals 0 damage, but you can use it 2 additional times each turn."

```
Twiddle {
    name "PASSIVE_TWIDDLE_NAME"
    desc "PASSIVE_TWIDDLE_DESC"
    class Psychic

    1 {
        passives {
            BasicAttackDamageMultiplier 0
            ExtraBasicAttacks 2
        }
    }
    2 {
        desc "PASSIVE_TWIDDLE2_DESC"
        passives {
            BasicAttackDamageMultiplier 0
            ExtraBasicAttacks 2
            Quivered 5
        }
    }
}
```

---

### `RepressedMemories`
**Name:** Repressed Memories  
**Description:** When you spend mana, cast a random Psychic spell that costs less than the mana spent.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_REPRESSEDMEMORIES2_DESC`: "When you spend mana, cast a random spell from any class that costs less than the mana spent."

```
RepressedMemories {
    name "PASSIVE_REPRESSEDMEMORIES_NAME"
    desc "PASSIVE_REPRESSEDMEMORIES_DESC"
    class Psychic

    1 {
        passives {
            ScaledStatusOnSpendMana {
                RepressedMemoriesMetronome {
                    stacks 1
                    pool Psychic
                }
            }
        }
    }
    2 {
        desc "PASSIVE_REPRESSEDMEMORIES2_DESC"
        passives {
            ScaledStatusOnSpendMana {
                RepressedMemoriesMetronome {
                    stacks 1
                    pool Jester
                }
            }
        }
    }
}
```

---

### `EldritchVisage`
**Name:** Eldritch Visage  
**Description:** At the start of your turn, inflict Magic Weakness 1 on all enemies in your line of sight.  
**Source:** `psychic_passives.gon`  

**Localization Strings:**
- `PASSIVE_ELDRITCHVISAGE2_DESC`: "At the start of your turn, inflict Magic Weakness 1 and Marked on all enemies in your line of sight."

```
EldritchVisage {
    name "PASSIVE_ELDRITCHVISAGE_NAME"
    desc "PASSIVE_ELDRITCHVISAGE_DESC"
    class Psychic

    1 {
        passives {
            AutocastEachTurnBegin MindCrack_EldritchVisage
        }
    }
    2 {
        desc "PASSIVE_ELDRITCHVISAGE2_DESC"
        passives {
            AutocastEachTurnBegin MindCrack_EldritchVisage2
        }
    }
}
```

---

## File: `tank_passives.gon`

### `Thorns`
**Name:** Thorns  
**Description:** Thorns 2.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_THORNS2_DESC`: "Thorns 4. <br/> Gain +1 Thorns when you take damage."

```
Thorns {
    name "PASSIVE_THORNS_NAME"
    desc "PASSIVE_THORNS_DESC"
    class Tank

    1 {
        passives {
            Thorns 2
        }
    }
    2 {
        desc "PASSIVE_THORNS2_DESC"
        passives {
            Thorns 4
            StatusOnTookDamage {
                Thorns 1
            }
        }
    }
}
```

---

### `HeavyHanded`
**Name:** Heavy Handed  
**Description:** +2 Knockback Damage.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_HEAVYHANDED2_DESC`: "+3 Knockback Damage. <br/> Your basic attack gains +3 Knockback."

```
HeavyHanded {
    name "PASSIVE_HEAVYHANDED_NAME"
    desc "PASSIVE_HEAVYHANDED_DESC"
    class Tank

    1 {
        passives {
            AddKnockbackDamage 2
        }
    }
    2 {
        desc "PASSIVE_HEAVYHANDED2_DESC"
        passives {
            AddKnockbackDamage 3
            AddStatusToBasicAttack {
                Knockback 3
            }
        }
    }
}
```

---

### `SlackOff`
**Name:** Slack Off  
**Description:** If you end your turn with unused movement actions, gain 8 HP.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_SLACKOFF2_DESC`: "If you end your turn with unused movement actions, gain +2 [img:con], 8 HP and 5 mana."

```
SlackOff {
    name "PASSIVE_SLACKOFF_NAME"
    desc "PASSIVE_SLACKOFF_DESC"
    class Tank

    1 {
        passives {
            StatusIfUnusedMovePoints {
                HealthGain 8
            }
        }
    }
    2 {
        desc "PASSIVE_SLACKOFF2_DESC"
        passives {
            StatusIfUnusedMovePoints {
                ConstitutionUp 2
                HealthGain 8
                ManaGain 5
            }
        }
    }
}
```

---

### `Scabs`
**Name:** Scabs  
**Description:** Gain +2 Shield when you take damage from an ability.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_SCABS2_DESC`: "Gain +2 Shield when you take damage from any source."

```
Scabs {
    name "PASSIVE_SCABS_NAME"
    desc "PASSIVE_SCABS_DESC"
    class Tank

    1 {
        passives {
            StatusOnTookDamageFromAbility {
                Shield 2
            }
        }
    }
    2 {
        desc "PASSIVE_SCABS2_DESC"
        passives {
            StatusOnTookDamage {
                Shield 2
            }
        }
    }
}
```

---

### `EyeCatchin`
**Name:** Eye Catchin'  
**Description:** taunt while at full health  
**Source:** `tank_passives.gon`  

```
EyeCatchin { //CUT
    name "Eye Catchin'"
    desc "taunt while at full health"
    class Tank

    1 {
        passives {
            TauntAtFullHealth 1
        }
    }
    2 {
        desc "taunt always"
        passives {
            TauntAlways 1
        }
    }
}
```

---

### `ThunderThighs`
**Name:** Thunder Thighs  
**Description:** Trample.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_THUNDERTHIGHS2_DESC`: "Trample 9."

```
ThunderThighs {
    name "PASSIVE_THUNDERTHIGHS_NAME"
    desc "PASSIVE_THUNDERTHIGHS_DESC"
    class Tank

    1 {
        passives {
            Trample 3
        }
    }
    2 {
        desc "PASSIVE_THUNDERTHIGHS2_DESC"
        passives {
            Trample 9
        }
        stats {
            con 1
        }
    }
}
```

---

### `Plow`
**Name:** Plow  
**Description:** When you knock back a unit, leave a rock where that unit was.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_PLOW2_DESC`: "When you knock back a unit, leave a rock where that unit was. <br/> All damage you deal has +1 Knockback."

```
Plow {
    name "PASSIVE_PLOW_NAME"
    desc "PASSIVE_PLOW_DESC"
    class Tank

    1 {
        passives {
            AddStatusToAllDamage {
                LeaveBehindRockOnKnockback 1
            }
        }
    }
    2 {
        desc "PASSIVE_PLOW2_DESC"
        passives {
            AddStatusToAllDamage {
                LeaveBehindRockOnKnockback 1
            }
            AddKnockbackToEverything 1
        }
    }
}
```

---

### `PetRocks`
**Name:** Pet Rocks  
**Description:** Rocks you spawn are alive!!
...and have +3 HP. Spawn a rock at the start of the battle.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_PETROCKS2_DESC`: "Rocks you spawn are alive, and hot!! <br/> ...and have +7 HP. Spawn a boulder at the start of the battle."

```
PetRocks {
    name "PASSIVE_PETROCKS_NAME"
    desc "PASSIVE_PETROCKS_DESC"
    class Tank

    1 {
        passives {
            ReplaceSpawnedObjects [SmallRock AnimatedSmallRock]
            ReplaceSpawnedObjects [Boulder AnimatedBoulder]
            ReplaceSpawnedObjects [SmallLavaRock AnimatedSmallLavaRock]
            ReplaceSpawnedObjects [LavaBoulder AnimatedLavaBoulder]

            AddPassiveToSpawnedRocks {
                JoinSpawnerFaction 1
                AddFilledMaxHealth 3
            }

            SpawnOnBattleStart {
                object SmallRock
                number 1
            }

            StatusReplacement [Petrify PetrifyCharmed]
        }
    }
    2 {
        desc "PASSIVE_PETROCKS2_DESC"
        passives {
            ReplaceSpawnedObjects [SmallRock AnimatedSmallLavaRock]
            ReplaceSpawnedObjects [Boulder AnimatedLavaBoulder]
            ReplaceSpawnedObjects [SmallLavaRock AnimatedSmallLavaRock]
            ReplaceSpawnedObjects [LavaBoulder AnimatedLavaBoulder]

            AddPassiveToSpawnedRocks {
                JoinSpawnerFaction 1
                AddFilledMaxHealth 7
            }

            SpawnOnBattleStart {
                object Boulder
                number 1
            }

            StatusReplacement [Petrify PetrifyCharmed]
        }
    }
}
```

---

### `ToadStyle`
**Name:** Toad Style  
**Description:** Your movement action is a jump. Landing on a unit deals damage and displaces it.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_TOADSTYLE2_DESC`: "Your movement action is a jump. Landing on a unit deals damage and displaces it."

```
ToadStyle {
    name "PASSIVE_TOADSTYLE_NAME"
    desc "PASSIVE_TOADSTYLE_DESC"
    class Tank
	
    1 {
        stats {
            spd 4
        }
        passives {
            ReplaceBasicMove ToadJump_BasicMove
        }
    }
    2 {
        desc "PASSIVE_TOADSTYLE2_DESC"
        stats {
            spd 8
        }
        passives {
            ReplaceBasicMove BellyFlop_BasicMove
        }
    }
}
```

---

### `ChainKnockback`
**Name:** Chain Knockback  
**Description:** Your basic attack gains +1 Knockback.
Units you knockback will Knockback other units.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_CHAINKNOCKBACK2_DESC`: "Your basic attack gains +1 Knockback. <br/> All knockback you deal is increased by 2 and deals +1 extra damage. <br/> Units you knockback will Knockback other units further."

```
ChainKnockback {
    name "PASSIVE_CHAINKNOCKBACK_NAME"
    desc "PASSIVE_CHAINKNOCKBACK_DESC"
    class Tank

    1 {
        passives {
            ChainKnockback 1
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }
    2 {
        desc "PASSIVE_CHAINKNOCKBACK2_DESC"
        passives {
            ChainKnockback 1
            AddStatusToBasicAttack {
                Knockback 1
            }
            AddKnockbackDamage 1
            AmplifyKnockback 2
        }
    }
}
```

---

### `ProtectiveAura`
**Name:** Protective  
**Description:** Your allies have Brace 1.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_PROTECTIVE2_DESC`: "Your allies have Brace 2."

```
ProtectiveAura {
    name "PASSIVE_PROTECTIVE_NAME"
    desc "PASSIVE_PROTECTIVE_DESC"
    class Tank

    1 {
        passives {
            DamageReductionAura {
                range global
                allies_only true
                stacks 1
            }
        }
    }
    2 {
        desc "PASSIVE_PROTECTIVE2_DESC"
        passives {
            DamageReductionAura {
                range global
                allies_only true
                stacks 2
            }
        }
    }
}
```

---

### `Wrestlemaniac`
**Name:** Wrestlemaniac  
**Description:** Your basic attack becomes Suplex when adjacent to enemies.
You gain the ability Toss.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_WRESTLEMANIAC2_DESC`: "Your basic attack is Suplex while you're next to a unit that can be suplexed and Your basic attack becomes Suplex when adjacent to enemies. +1 Bonus Move. <br/> You gain the ability Toss+."

```
Wrestlemaniac {
    name "PASSIVE_WRESTLEMANIAC_NAME"
    desc "PASSIVE_WRESTLEMANIAC_DESC"
    class Tank

    1 {
        passives {
            BonusAbility BonusToss
            ReplaceBasicAttackWhenCastable BasicSuplex
        }
        stats {
            spd 2
        }
    }
    2 {
        desc "PASSIVE_WRESTLEMANIAC2_DESC"

        passives {
            BonusAbility BonusToss2
            ReplaceBasicAttackWhenCastable BasicSuplex
            ExtraMovePoints 1
        }
        stats {
            spd 2
        }
    }
}
```

---

### `MountainForm`
**Name:** Mountain Form  
**Description:** Knockback immunity.
Tiles you walk over become dirt and may spawn rocks.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_MOUNTAINFORM2_DESC`: "Trample. Knockback and Fire immunity. <br/> Tiles you walk over become dirt and may spawn rocks."

```
MountainForm {
    name "PASSIVE_MOUNTAINFORM_NAME"
    desc "PASSIVE_MOUNTAINFORM_DESC"
    class Tank

    1 {
        passives {
            InnateElement Earth
            //ElementImmune Fire
            //StatusImmunity [Burn]
            KnockbackImmunity 1
            RockDetector 10
            SizeScale 1.2
        }
    }
    2 {
        desc "PASSIVE_MOUNTAINFORM2_DESC"

        passives {
            InnateElement Earth
            ElementImmune Fire
            StatusImmunity [Burn]
            KnockbackImmunity 1
            RockDetector 10
            SizeScale 1.3
            Trample 3
            //Brace 1
            //Thorns 2
        }
    }
}
```

---

### `HomeRun`
**Name:** Home Run  
**Description:** Knockback you deal is increased by 10.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_HOMERUN2_DESC`: "Knockback you deal is increased by 10 and inflicts Bruise 1."

```
HomeRun {
    name "PASSIVE_HOMERUN_NAME"
    desc "PASSIVE_HOMERUN_DESC"
    class Tank

    1 {
        passives {
            AmplifyKnockback 10
        }
    }
    2 {
        desc "PASSIVE_HOMERUN2_DESC"

        passives {
            AmplifyKnockback 10
            AddStatusToKnockbackDamage {
                Bruise 1
            }
        }
    }
}
```

---

### `RockAspect`
**Name:** Rock Aspect  
**Description:** Units that attack or contact you have a 10% chance to get Petrified.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_ROCKASPECT2_DESC`: "Units that attack or contact you have a 20% chance to get Petrified."

```
RockAspect {
    name "PASSIVE_ROCKASPECT_NAME"
    desc "PASSIVE_ROCKASPECT_DESC"
    class Tank

    1 {
        shield 4
        passives {
            RevengeDamage {
                effects {
                    Petrify [1, .1]
                }
            }
            AddTag rock
        }
    }
    2 {
        desc "PASSIVE_ROCKASPECT2_DESC"

        shield 8
        passives {
            RevengeDamage {
                effects {
                    Petrify [1, .2]
                }
            }
            AddTag rock
        }
    }
}
```

---

### `WideLoad`
**Name:** Wide Load  
**Description:** When an adjacent ally is targeted by an enemy, swap places with the ally.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_WIDELOAD2_DESC`: "When an adjacent ally is targeted by an enemy, gain +1 temp Thorns and temp Brace, then swap places with the ally."

```
WideLoad {
    name "PASSIVE_WIDELOAD_NAME"
    desc "PASSIVE_WIDELOAD_DESC"
    class Tank

    1 {
        passives {
            ProtectTargetedAllies SwapPositions_WideLoad
        }
        stats {
            con 1
        }
    }
    2 {
        desc "PASSIVE_WIDELOAD2_DESC"

        passives {
            ProtectTargetedAllies SwapPositions_WideLoad2
        }
        stats {
            con 1
        }
    }
}
```

---

### `HardHead`
**Name:** Hard Head  
**Description:** You block attacks from the front.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_HARDHEAD2_DESC`: "You block attacks from the front. Your basic attack inflicts Bruise."

```
HardHead { //TODO: add cant be stunned (maybe)
    name "PASSIVE_HARDHEAD_NAME"
    desc "PASSIVE_HARDHEAD_DESC"
    class Tank

    1 {
        passives {
            FaceShield 0
        }
    }
    2 {
        desc "PASSIVE_HARDHEAD2_DESC"

        passives {
            FaceShield 0
            AddStatusToBasicAttack {
                Bruise 1
            }
        }
    }
}
```

---

### `MyLeg`
**Name:** My Leg!  
**Description:** All injuries you get are Broken Legs.
If you have four broken legs, gain +4 Thorns, Trample, and adjacent allies have Toss as a bonus ability.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_MYLEG2_DESC`: "All injuries you get are Broken Legs. <br/> If you have four broken legs, gain +4 Thorns, +4 Brace, Trample, and adjacent allies have Toss as a bonus ability."

```
MyLeg {
    name "PASSIVE_MYLEG_NAME"
    desc "PASSIVE_MYLEG_DESC"
    class Tank

    1 {
        passives {
            ForceSpecificInjury spd
            PassiveAtInjuryThreshold {
                mode greater_or_equal

                injury spd
                threshold 4

                passives {
                    Thorns 4
                    Trample 3
                    AllyBonusAbilityAura NubbyToss
                    NubbyTossPriority 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_MYLEG2_DESC"

        passives {
            ForceSpecificInjury spd
            PassiveAtInjuryThreshold {
                mode greater_or_equal

                injury spd
                threshold 4

                passives {
                    Thorns 4
                    Trample 3
                    Brace 4
                    AllyBonusAbilityAura NubbyToss
                    NubbyTossPriority 1
                }
            }
        }
    }
}
```

---

### `Hardy`
**Name:** Hardy  
**Description:** Heal to full HP at the start of each battle.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_HARDY2_DESC`: "Heal to full HP at the start of each battle. +3 Health Regeneration."

```
Hardy {
    name "PASSIVE_HARDY_NAME"
    desc "PASSIVE_HARDY_DESC"
    class Tank

    1 {
        passives {
            StatusOnBattleStart {
                FullHeal 1
            }
        }
    }
    2 {
        desc "PASSIVE_HARDY2_DESC"

        passives {
            StatusOnBattleStart {
                FullHeal 1
            }
            HealthRegenUp 4
        }
    }
}
```

---

### `SlowAndSteady`
**Name:** Slow and Steady  
**Description:** Gain -2 [img:spd] and +1 Range at the end of each turn. If your [img:spd] is 0, you can attack an extra time each turn.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_SLOWANDSTEADY2_DESC`: "Gain -2 [img:spd], +1 Range, +1 [img:str], and +1 [img:int] at the end of each turn. If your [img:spd] is 0, you can attack an extra time each turn."

```
SlowAndSteady {
    name "PASSIVE_SLOWANDSTEADY_NAME"
    desc "PASSIVE_SLOWANDSTEADY_DESC"
    class Tank

    1 {
        passives {
            StatusEachTurnEnd {
                SpeedUp -2
                RangeUp 1
            }
            PassiveAtStatThreshold {
                mode less_or_equal
                threshold {
                    spd 0
                }
                passives {
                    ExtraBasicAttacks 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_SLOWANDSTEADY2_DESC"

        passives {
            StatusEachTurnEnd {
                SpeedUp -2
                RangeUp 1
                StrengthUp 1
                IntelligenceUp 1
            }
            PassiveAtStatThreshold {
                mode less_or_equal
                threshold {
                    spd 0
                }
                passives {
                    ExtraBasicAttacks 1
                }
            }
        }
    }
}
```

---

### `FollowUp`
**Name:** Follow Up  
**Description:** After you use your basic attack, dash forward as far as you can.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_FOLLOWUP2_DESC`: "After you use your basic attack, dash forward as far as you can and do a melee attack."

```
FollowUp {
    name "PASSIVE_FOLLOWUP_NAME"
    desc "PASSIVE_FOLLOWUP_DESC"
    class Tank

    1 {
        passives {
            FollowUp FollowUpDash
        }
    }
    2 {
        desc "PASSIVE_FOLLOWUP2_DESC"
        passives {
            FollowUp FollowUpDash2
        }
    }
}
```

---

### `CatAPult`
**Name:** Cat-A-Pult  
**Description:** You can throw adjacent allies up to 4 tiles on their turns without using their movement action.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_CATAPULT2_DESC`: "You can throw adjacent allies to any tile on their turns without using their movement action."

```
CatAPult {
    name "PASSIVE_CATAPULT_NAME"
    desc "PASSIVE_CATAPULT_DESC"
    class Tank

    1 {
        passives {
            AllyMoveAbilityAura CatapultJump
            CatAPultAnimation {
                ability CatapultJump
                animation knockupatk
            }
        }
    }
    2 {
        desc "PASSIVE_CATAPULT2_DESC"
        passives {
            AllyMoveAbilityAura CatapultJump2
            CatAPultAnimation {
                ability CatapultJump2
                animation knockupatk
            }
        }
    }
}
```

---

### `ShovingMatch`
**Name:** Shoving Match  
**Description:** When you knock a unit into an ally, or knock an ally into an enemy, that ally uses their basic attack on the other unit.
Your basic attack has +1 Knockback.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_SHOVINGMATCH2_DESC`: "When you knock a unit into an ally, or knock an ally into an enemy, that ally uses their basic attack on the other unit. <br/> Your basic attack has +2 Knockback. You deal no damage to allies."

```
ShovingMatch {
    name "PASSIVE_SHOVINGMATCH_NAME"
    desc "PASSIVE_SHOVINGMATCH_DESC"
    class Tank

    1 {
        passives {
            ShovingMatch attack
            AddStatusToBasicAttack {
                Knockback 1
            }
        }
    }
    2 {
        desc "PASSIVE_SHOVINGMATCH2_DESC"
        passives {
            ShovingMatch attack
            AllyDamageReduction 0
            AddStatusToBasicAttack {
                Knockback 2
            }
        }
    }
}
```

---

### `Stoic`
**Name:** Stoic  
**Description:** If you end your turn with unused movement actions, gain +2 Bonus Moves.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_STOIC2_DESC`: "If you end your turn with unused movement actions, gain +2 Bonus Moves, +2 [img:shield] and +1 Brace."

```
Stoic {
    name "PASSIVE_STOIC_NAME"
    desc "PASSIVE_STOIC_DESC"
    class Tank

    1 {
        passives {
            StatusIfUnusedMovePoints {
                MoveQuivered 2
            }
        }
    }
    2 {
        desc "PASSIVE_STOIC2_DESC"
        passives {
            StatusIfUnusedMovePoints {
                MoveQuivered 2
                Brace 1
                Shield 2
            }
        }
    }
}
```

---

### `PriorityTarget`
**Name:** Priority Target  
**Description:** Enemies will attack you instead of your allies if they can.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_PRIORITYTARGET2_DESC`: "+2 Thorns, +2 Brace, and +2 Health Regeneration. Enemies will attack you instead of your allies if they can."

```
PriorityTarget {
    name "PASSIVE_PRIORITYTARGET_NAME"
    desc "PASSIVE_PRIORITYTARGET_DESC"
    class Tank

    1 {
        passives {
            TauntAlways 1
        }
        stats {
            con 1
        }
    }
    2 {
        desc "PASSIVE_PRIORITYTARGET2_DESC"
        passives {
            TauntAlways 1
            Brace 2
            Thorns 2
            HealthRegenUp 2
        }
        stats {
            con 2
        }
    }
}
```

---

### `Bouncer`
**Name:** Bouncer  
**Description:** When an ally takes damage, move 3 tiles toward the source of the damage and attack it if you can.  
**Source:** `tank_passives.gon`  

**Localization Strings:**
- `PASSIVE_BOUNCER2_DESC`: "When an ally takes damage, full move toward the source of the damage and attack it if you can."

```
Bouncer {
    name "PASSIVE_BOUNCER_NAME"
    desc "PASSIVE_BOUNCER_DESC"
    class Tank

    1 {
        passives {
            SecurityBotProtect {
                ability attack
                move MoveThree
            }
        }
    }
    2 {
        desc "PASSIVE_BOUNCER2_DESC"
        passives {
            SecurityBotProtect {
                ability attack
                move move
            }
        }
    }
}
```

---

## File: `thief_passives.gon`

### `Backstabber`
**Name:** Backstabber  
**Description:** Your backstabs are always critical.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_BACKSTABBER2_DESC`: "Your backstabs are always critical. <br/> When you land a critical hit, gain a random stat up."

```
Backstabber {
    name "PASSIVE_BACKSTABBER_NAME"
    desc "PASSIVE_BACKSTABBER_DESC"
    class Thief

    1 {
        passives {
            BackstabCritChance 1
        }
    }
    2 {
        desc "PASSIVE_BACKSTABBER2_DESC"
        passives {
            BackstabCritChance 1
            StatusOnCrit {
                RandomStatUp 1
            }
        }
    }
}
```

---

### `GoldenClaws`
**Name:** Golden Claws  
**Description:** Gain +1 Damage for each coin you collect.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_GOLDENCLAWS2_DESC`: "Gain +2 Damage for each coin you collect."

```
GoldenClaws {
    name "PASSIVE_GOLDENCLAWS_NAME"
    desc "PASSIVE_GOLDENCLAWS_DESC"
    class Thief

    1 {
        passives {
            CoinsAddDamage 1
        }
    }
    2 {
        desc "PASSIVE_GOLDENCLAWS2_DESC"
        passives {
            CoinsAddDamage 2
        }
    }
}
```

---

### `Shadow`
**Name:** Stealthed  
**Description:** Start each battle with Stealth.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_STEALTHED2_DESC`: "Start each battle with Stealth. Gain Stealth when you get a kill."

```
Shadow {
    name "PASSIVE_STEALTHED_NAME"
    desc "PASSIVE_STEALTHED_DESC"
    class Thief

    1 {
        passives {
            Stealth 1
        }
    }
    2 {
        desc "PASSIVE_STEALTHED2_DESC"
        passives {
            Stealth 1

            StatusOnKill {
                Stealth 1
            }
        }
    }
}
```

---

### `PoisonTips`
**Name:** Poison Tips  
**Description:** Your basic attack inflicts Poison 1.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_POISONTIPS2_DESC`: "Your basic attack inflicts Poison 1. <br/> Poison you inflict is doubled."

```
PoisonTips {
    name "PASSIVE_POISONTIPS_NAME"
    desc "PASSIVE_POISONTIPS_DESC"
    class Thief

    1 {
        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
        }
    }
    2 {
        desc "PASSIVE_POISONTIPS2_DESC"
        passives {
            AddStatusToBasicAttack {
                Poison 1
            }
            PoisonMultiplier 2
        }
    }
}
```

---

### `Burgle`
**Name:** Burgle  
**Description:** Your basic attack gains you 1 coin when it deals damage.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_BURGLE2_DESC`: "Your basic attack gains you 1 coin and spawns a coin pickup when it deals damage."

```
Burgle {
    name "PASSIVE_BURGLE_NAME"
    desc "PASSIVE_BURGLE_DESC"
    class Thief

    1 {
        passives {
            AddStatusToBasicAttack {
                BurgleCoin 1
            }
        }
    }
    2 {
        desc "PASSIVE_BURGLE2_DESC"
        passives {
            AddStatusToBasicAttack {
                BurgleCoin 1
                KnockOutCoin 1
                KnockOutCoin [1 .5]
            }
        }
    }
}
```

---

### `SwiftKiller`
**Name:** More!  
**Description:** When you kill a unit, refresh your movement action.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_SWIFTKILLER2_DESC`: "When you kill a unit, refresh your movement and basic attack."

```
SwiftKiller {
    name "PASSIVE_SWIFTKILLER_NAME"
    desc "PASSIVE_SWIFTKILLER_DESC"
    class Thief

    1 {
        passives {
            StatusOnKill {
                RefreshMovePoints 1
            }
        }
    }
    2 {
        desc "PASSIVE_SWIFTKILLER2_DESC"
        passives {
            StatusOnKill {
                RefreshMovePoints 1
                RefreshActPoints 1
            }
        }
    }
}
```

---

### `LongStrider`
**Name:** Long Stride  
**Description:** +1 movement range.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_LONGSTRIDER2_DESC`: "+2 movement range. <br/> +10% dodge chance."

```
LongStrider { //CUT
    name "PASSIVE_LONGSTRIDER_NAME"
    desc "PASSIVE_LONGSTRIDER_DESC"
    class Thief

    1 {
        passives {
            AddMovement 1
        }
    }
    2 {
        desc "PASSIVE_LONGSTRIDER2_DESC"
        passives {
            AddMovement 2
            ArmorDodgeChance 10%
        }
    }
}
```

---

### `DoubleThrow`
**Name:** Double Throw  
**Description:** Your basic attack hits twice for half damage.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_DOUBLETHROW2_DESC`: "Your basic attack hits thrice for 1/3rd damage."

```
DoubleThrow {
    name "PASSIVE_DOUBLETHROW_NAME"
    desc "PASSIVE_DOUBLETHROW_DESC"
    class Thief

    1 {
        passives {
            AddTemporaryEffectsToBasicAttack {
                CastAgain 1
            }
            BasicAttackDamageMultiplier 50%
        }
    }
    2 {
        desc "PASSIVE_DOUBLETHROW2_DESC"
        passives {
            AddTemporaryEffectsToBasicAttack {
                CastAgain 2
            }
            BasicAttackDamageMultiplier 33.333334%

            //BasicAttackMultiplicity 1
        }
        
    }
}
```

---

### `BountyHunter`
**Name:** Bounty Hunter  
**Description:** During your turn, one random enemy has a Bounty.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_BOUNTYHUNTER2_DESC`: "During your turn, 2 random enemies have a large Bounty."

```
BountyHunter {
    name "PASSIVE_BOUNTYHUNTER_NAME"
    desc "PASSIVE_BOUNTYHUNTER_DESC"
    class Thief

    1 {
        passives {
            ApplyStatusesToRandomEnemiesEachTurn {
                Bounty 1
            }
        }
    }
    2 {
        desc "PASSIVE_BOUNTYHUNTER2_DESC"
        passives {
            ApplyStatusesToRandomEnemiesEachTurn {
                count 2

                Bounty 3
            }
        }
    }
}
```

---

### `RazorClaws`
**Name:** Razor Claws  
**Description:** Your basic attack inflicts Bleed 1.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_RAZORCLAWS2_DESC`: "All of your damaging abilities inflict Bleed 1."

```
RazorClaws {
    name "PASSIVE_RAZORCLAWS_NAME"
    desc "PASSIVE_RAZORCLAWS_DESC"
    class Thief

    1 {
        passives {
            AddStatusToBasicAttack {
                Bleed 1
            }
        }
    }
    2 {
        desc "PASSIVE_RAZORCLAWS2_DESC"
        passives {
            AddStatusToBasicAttack {
                Bleed 1
            }
            AddStatusToAllDamageAbilities {
                Bleed 1
            }
        }
    }
}
```

---

### `Looter`
**Name:** Swift Looter  
**Description:** When you collect a coin pickup, refresh your movement action.
1-2 extra coins spawn in each battle.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_SWIFTLOOTER2_DESC`: "When you collect a coin pickup, refresh your movement action and gain +1 [img:dex] and +1 [img:spd]. <br/> 2-3 extra coins spawn in each battle."

```
Looter {
    name "PASSIVE_SWIFTLOOTER_NAME"
    desc "PASSIVE_SWIFTLOOTER_DESC"
    class Thief

    1 {
        passives {
            StatusOnPickupCoins {
                RefreshMovePoints 1
            }
            SpawnOnBattleStartRandomEmptyTile {
                object Coin
                number [1 2]
            }
        }
    }
    2 {
        desc "PASSIVE_SWIFTLOOTER2_DESC"
        passives {
            StatusOnPickupCoins {
                RefreshMovePoints 1
                DexterityUp 1
                SpeedUp 1
            }
            SpawnOnBattleStartRandomEmptyTile {
                object Coin
                number [2 3]
            }
        }
    }
}
```

---

### `AlphaStrike`
**Name:** First Strike  
**Description:** Gain an extra turn at the start of the battle.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_ALPHASTRIKE2_DESC`: "Gain an extra turn at the start of the battle. Damage you deal on this turn is always critical."

```
AlphaStrike {
    name "PASSIVE_ALPHASTRIKE_NAME"
    desc "PASSIVE_ALPHASTRIKE_DESC"
    class Thief

    1 {
        passives {
            AlphaTurns 1
        }
    }
    2 {
        desc "PASSIVE_ALPHASTRIKE2_DESC"
        passives {
            AlphaTurns 1
            AllDamageCrits 1
        }
    }
}
```

---

### `Zip`
**Name:** ZIP!  
**Description:** Your movement action is Shadowstep.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_ZIP2_DESC`: "Your movement action is Shadowstep. <br/> You can use your movement action an extra time each turn."

```
Zip {
    name "PASSIVE_ZIP_NAME"
    desc "PASSIVE_ZIP_DESC"
    class Thief

    1 {
        passives {
            ReplaceBasicMove Shadowstep
        }
    }
    2 {
        desc "PASSIVE_ZIP2_DESC"
        passives {
            ReplaceBasicMove Shadowstep
            ExtraMovePoints 1
        }
    }
}
```

---

### `WeakSpot`
**Name:** Weak Spot  
**Description:** Your basic attack ignores shield and inflicts Weakness 1.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_WEAKSPOT2_DESC`: "All of your damaging abilities ignore shield and inflict Weakness 2. +25% crit chance."

```
WeakSpot {
    name "PASSIVE_WEAKSPOT_NAME"
    desc "PASSIVE_WEAKSPOT_DESC"
    class Thief

    1 {
        passives {
            AddStatusToBasicAttack {
                Weakness 1
                Piercing 1
            }
        }
    }
    2 {
        desc "PASSIVE_WEAKSPOT2_DESC"
        passives {
            CritChanceUp 25
			AddStatusToAllDamageAbilities {
				Weakness 2
				Piercing 1
			}
        }
    }
}
```

---

### `Penetrate`
**Name:** Penetrate  
**Description:** Your basic attack passes through units and ignores shield. +1 Range.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_PENETRATE2_DESC`: "Your basic attack passes through units and ignores shield. +10 Range."

```
Penetrate {
    name "PASSIVE_PENETRATE_NAME"
    desc "PASSIVE_PENETRATE_DESC"
    class Thief

    1 {
        passives {
            AddBonusRange 1
            AddBonusMeleeRange 1
            MakeBasicAttackPassThroughThings 1
            AddStatusToBasicAttack {
                Piercing 1
            }
        }
    }
    2 {
        desc "PASSIVE_PENETRATE2_DESC"
        passives {
            AddBonusRange 10
            AddBonusMeleeRange 10
            MakeBasicAttackPassThroughThings 1
            AddStatusToBasicAttack {
                Piercing 1
            }
        }
    }
}
```

---

### `AfterImage`
**Name:** After Image  
**Description:** When you move, spawn a shadow where you moved from. The shadow mimics your basic action but fades away at the end of your turn.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_AFTERIMAGE2_DESC`: "When you move, spawn a shadow where you moved from. The shadow mimics your basic action."

```
AfterImage {
    name "PASSIVE_AFTERIMAGE_NAME"
    desc "PASSIVE_AFTERIMAGE_DESC"
    class Thief

    1 {
        passives {
            AfterImage PlayerCat_ThiefShade
        }
    }
    2 {
        desc "PASSIVE_AFTERIMAGE2_DESC"
        passives {
            AfterImage PlayerCat_ThiefShade2
            ReplaceSpawnedObjects [PlayerCat_ThiefShade PlayerCat_ThiefShade2]
        }
    }
}
```

---

### `Shiv`
**Name:** Shiv  
**Description:** Your basic attack has +2 damage, +25% critical chance, and inflicts Bleed 1 when attacking a unit in melee range.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_SHIV2_DESC`: "Your basic attack has +2 damage, +50% critical chance, and inflicts Bleed 2 when attacking a unit in melee range."

```
Shiv {
    name "PASSIVE_SHIV_NAME"
    desc "PASSIVE_SHIV_DESC"
    class Thief

    1 {
        passives {
            AddStatusToBasicAttack {
                Conditional_Adjacent {
                    BonusDamage 2
                    Bleed 1
                    BonusCritChance 25
                }
            }
        }
    }
    2 {
        desc "PASSIVE_SHIV2_DESC"
        passives {
            AddStatusToBasicAttack {
                Conditional_Adjacent {
                    BonusDamage 3
                    Bleed 2
                    BonusCritChance 50
                }
            }
        }
    }
}
```

---

### `Critical`
**Name:** Critical  
**Description:** Your critical hits deal +100% more damage. Gain +1 [img:lck] whenever you make a critical hit.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_CRITICAL2_DESC`: "Your critical hits deal +100% more damage and inflict Bleed and Weakness 1.  Gain +1 [img:lck] whenever you make a critical hit."

```
Critical {
    name "PASSIVE_CRITICAL_NAME"
    desc "PASSIVE_CRITICAL_DESC"
    class Thief

    1 {
        passives {
            AddCritMultiplier 100%
            StatusOnCrit {
                LuckUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_CRITICAL2_DESC"

        passives {
            AddCritMultiplier 100%
            StatusOnCrit {
                LuckUp 1
            }

            CritsApplyStatus {
                Bleed 1
                Weakness 1
            }
        }
    }
}
```

---

### `LootHoarder`
**Name:** Loot Hoarder  
**Description:** Automatically collect all pickups at the end of the battle if you're not downed.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_LOOTHOARDER2_DESC`: "Automatically destroy all enemy bodies and collect all pickups at the end of the battle if you're not downed."

```
LootHoarder {
    name "PASSIVE_LOOTHOARDER_NAME"
    desc "PASSIVE_LOOTHOARDER_DESC"
    class Thief

    1 {
        passives {
            CollectPickupsOnBattleEnd 1
        }
    }
    2 {
        desc "PASSIVE_LOOTHOARDER2_DESC"

        passives {
            CollectPickupsOnBattleEnd {
                pop_corpses true
            }
        }
    }
}
```

---

### `Cripple`
**Name:** Cripple  
**Description:** Your critical hits inflict Immobilize and Weakness 2.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_CRIPPLE2_DESC`: "Your critical hits inflict Stun and Weakness 2."

```
Cripple {
    name "PASSIVE_CRIPPLE_NAME"
    desc "PASSIVE_CRIPPLE_DESC"
    class Thief

    1 {
        passives {
            CritsApplyStatus {
                Immobile 1
                Weakness 2
            }
        }
    }
    2 {
        desc "PASSIVE_CRIPPLE2_DESC"

        passives {
            CritsApplyStatus {
                Stun 1
                Weakness 2
            }
        }
    }
}
```

---

### `Agile`
**Name:** Agile  
**Description:** +2 Movement Range. If you move fewer tiles than your full movement range, you can move a 2nd time for the rest of your movement range.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_AGILE2_DESC`: "+4 Movement Range. If you move fewer tiles than your full movement range, you can move a 2nd, 3rd and 4th time for the rest of your movement range."

```
Agile {
    name "PASSIVE_AGILE_NAME"
    desc "PASSIVE_AGILE_DESC"
    class Thief

    1 {
        passives {
            SplittableMove 1
            AddMovement 2
        }
    }
    2 {
        desc "PASSIVE_AGILE2_DESC"

        passives {
            SplittableMove 3
            AddMovement 4
        }
    }
}
```

---

### `Shank`
**Name:** Shank  
**Description:** When behind and adjacent to an enemy, your basic attack is a melee attack that hits twice.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_SHANK2_DESC`: "When behind and adjacent to an enemy, your basic attack is a melee attack that hits thrice!"

```
Shank {
    name "PASSIVE_SHANK_NAME"
    desc "PASSIVE_SHANK_DESC"
    class Thief

    1 {
        passives {
            ReplaceBasicAttackWhenCastable Shank
        }
    }
    2 {
        desc "PASSIVE_SHANK2_DESC"

        passives {
            ReplaceBasicAttackWhenCastable Shank2
        }
    }
}
```

---

### `FlipACoin`
**Name:** Flip a Coin  
**Description:** When you gain a coin, you have a 50% chance to spawn a coin on a random tile and a 50% chance to gain +2 [img:spd] and +2 [img:lck].  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_FLIPACOIN2_DESC`: "When you gain a coin, you have a 50% chance to spawn 2 coins on random tiles and a 50% chance to gain +2 [img:spd], +2 [img:lck] and +2 [img:dex]."

```
FlipACoin {
    name "PASSIVE_FLIPACOIN_NAME"
    desc "PASSIVE_FLIPACOIN_DESC"
    class Thief

    1 {
        passives {
            StatusOnGainCoins {
                RandomStatusFromPool {
                    SpawnCoinAnywhere 1
                    StatusGroup {
                        SpeedUp 2
                        LuckUp 2
                    }
                }
            }
        }
    }
    2 {
        desc "PASSIVE_FLIPACOIN2_DESC"

        passives {
            StatusOnGainCoins {
                RandomStatusFromPool {
                    StatusGroup {
                        SpawnCoinAnywhere 1
                        SpawnCoinAnywhere 1
                    }
                    StatusGroup {
                        SpeedUp 2
                        LuckUp 2
                        DexterityUp 2
                    }
                }
            }
        }
    }
}
```

---

### `ShakeDown`
**Name:** Shake Down  
**Description:** Your critical hits spawn a coin and a random pickup.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_SHAKEDOWN2_DESC`: "+25% critical hit chance. Your critical hits spawn a coin and two random pickups."

```
ShakeDown {
    name "PASSIVE_SHAKEDOWN_NAME"
    desc "PASSIVE_SHAKEDOWN_DESC"
    class Thief

    1 {
        passives {
            CritsApplyStatus {
                ObjectOnHitCharacter Coin
                ObjectOnHitCharacter RandomPickup
            }
        }
    }
    2 {
        desc "PASSIVE_SHAKEDOWN2_DESC"

        passives {
            CritChanceUp 25

            CritsApplyStatus {
                ObjectOnHitCharacter Coin
                ObjectOnHitCharacter RandomPickup
                ObjectOnHitCharacter RandomPickup
            }
        }
    }
}
```

---

### `SweetSpot`
**Name:** Sweetspot  
**Description:** +1 Range. Your basic attack deals more damage the farther away you are from the target.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_SWEETSPOT2_DESC`: "+6 Range. Your basic attack deals more damage the farther away you are from the target."

```
SweetSpot {
    name "PASSIVE_SWEETSPOT_NAME"
    desc "PASSIVE_SWEETSPOT_DESC"
    class Thief

    1 {
        passives {
            AddBonusRange 1

            AddStatusToBasicAttack {
                DistanceBonusDamage {
                    stacks 1
                    min_range 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_SWEETSPOT2_DESC"

        passives {
            AddBonusRange 6

            AddStatusToBasicAttack {
                DistanceBonusDamage {
                    stacks 1
                    min_range 1
                }
            }
        }
    }
}
```

---

### `Pinpoint`
**Name:** Pinpoint  
**Description:** Your critical hits inflict Marked.  
**Source:** `thief_passives.gon`  

**Localization Strings:**
- `PASSIVE_PINPOINT2_DESC`: "Your critical hits inflict Marked. <br/> Your critical hits deal 100% more damage."

```
Pinpoint {
    name "PASSIVE_PINPOINT_NAME"
    desc "PASSIVE_PINPOINT_DESC"
    class Thief

    1 {
        passives {
            CritsApplyStatus {
                Conditional_HasStatus {
                    status Marked
                } Else {
                    Marked 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_PINPOINT2_DESC"

        passives {
            CritsApplyStatus {
                Conditional_HasStatus {
                    status Marked
                } Else {
                    Marked 1
                }
            }

            AddCritMultiplier 100%
        }
    }
}
```

---

## File: `tinkerer_passives.gon`

### `VersionTwo`
**Name:** v2.0  
**Description:** Start with 1 Tech.
Your Tech can't drop below 1.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_VERSIONTWO2_DESC`: "Start with 1 Tech. <br/> Your Tech can't drop below 1. <br/> Your Tech isn't removed when you craft."

```
VersionTwo {
    name "PASSIVE_VERSIONTWO_NAME"
    desc "PASSIVE_VERSIONTWO_DESC"
    class Tinkerer

    1 {
        passives {
            Tech 1
            MinimumTech 1
        }
    }
    2 {
        desc "PASSIVE_VERSIONTWO2_DESC"
        passives {
            Tech 1
            MinimumTech 1
            CapTechSpent 0
        }
    }
}
```

---

### `WeaponProficiency`
**Name:** Weapon Proficiency  
**Description:** Your weapon damage scales with your stats and counts as a basic attack.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_WEAPONPROFICIENCY2_DESC`: "Your weapon damage scales with your stats and counts as a basic attack. <br/> You can use your weapon an extra time each turn."

```
WeaponProficiency {
    name "PASSIVE_WEAPONPROFICIENCY_NAME"
    desc "PASSIVE_WEAPONPROFICIENCY_DESC"
    class Tinkerer

    1 {
        passives {
            AddWeaponScaling 1
            WeaponCountsAsBasicAttack 1
        }
    }
    2 {
        desc "PASSIVE_WEAPONPROFICIENCY2_DESC"
        passives {
            AddWeaponScaling 1
            WeaponCountsAsBasicAttack 1
            ExtraWeaponAttacks 1
        }
    }
}
```

---

### `LivingBattery`
**Name:** Living Battery  
**Description:** When an adjacent ally spends mana, gain that much mana.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_LIVINGBATTERY2_DESC`: "When an adjacent ally spends mana, gain that much mana. You have no mana cap."

```
LivingBattery {
    name "PASSIVE_LIVINGBATTERY_NAME"
    desc "PASSIVE_LIVINGBATTERY_DESC"
    class Tinkerer

    1 {
        passives {
            AbsorbManaAura 1
        }
    }
    2 {
        desc "PASSIVE_LIVINGBATTERY2_DESC"
        passives {
            AbsorbManaAura 1
            UncappedMana 1
        }
    }
}
```

---

### `FuzzyFeet`
**Name:** Fuzzy Feet  
**Description:** When you end your movement, deal 1 Electric Damage to all adjacent units for each tile you moved.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_FUZZYFEET2_DESC`: "When you end your movement, deal 1 Electric Damage to all adjacent units for each tile you moved. This damage has a chance to inflict Stun."

```
FuzzyFeet {
    name "PASSIVE_FUZZYFEET_NAME"
    desc "PASSIVE_FUZZYFEET_DESC"
    class Tinkerer

    1 {
        passives {
            DamageNeighborsAfterMove {
                type spell
                damage X

                effects {
                    VisualFXTile WaterConduct
                }
                elements [
                    Electric
                ]
            }
        }
    }
    2 {
        desc "PASSIVE_FUZZYFEET2_DESC"
        passives {
            DamageNeighborsAfterMove {
                type spell
                damage X

                effects {
                    Stun [1, .05*X]
                    VisualFXTile WaterConduct
                }
                elements [
                    Electric
                ]
            }
        }
    }
}
```

---

### `ArmorSpecialist`
**Name:** Armor Specialist  
**Description:** Your equipment passive effects are doubled.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_ARMORSPECIALIST2_DESC`: "Your equipment passive and active effects are doubled."

```
ArmorSpecialist {
    //PART OF THIS IS HARD CODED
    name "PASSIVE_ARMORSPECIALIST_NAME"
    desc "PASSIVE_ARMORSPECIALIST_DESC"
    class Tinkerer

    1 {
        passives {
            EquipmentPassiveMultiplierBonus 1
        }
    }
    2 {
        desc "PASSIVE_ARMORSPECIALIST2_DESC"
        passives {
            EquipmentPassiveMultiplierBonus 1
            AddTemporaryEffectsToEquipment {
                CastAgain 1
            }
        }
    }
}
```

---

### `EMP`
**Name:** EMP  
**Description:** Your explosions are Electric element and deal +2 damage.
Instead of knockback, explosions have a chance to inflict Stun.
+2 Blast Resistance.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_EMP2_DESC`: "Your explosions are Electric element and deal +4 damage. <br/> Instead of knockback, explosions have a chance to inflict Stun. Your explosions don't affect allies. <br/> +4 Blast Resistance."

```
EMP {
    name "PASSIVE_EMP_NAME"
    desc "PASSIVE_EMP_DESC"
    class Tinkerer

    1 {
        passives {
            EMP {
                spell_graphics_override {
                    particle WaterConduct
                    center_particle WaterConduct
                    area_particle WaterConduct
                    palette -1
                }
                status_explosion_override WaterConduct
            }
            IncreaseExplosionDamage 2
            BlastResistance 2

            AddPassivesToMinions {
                EMP {
                    spell_graphics_override {
                        particle WaterConduct
                        center_particle WaterConduct
                        area_particle WaterConduct
                        palette -1
                    }
                    status_explosion_override WaterConduct
                }
                IncreaseExplosionDamage 2
            }
        }
    }
    2 {
        desc "PASSIVE_EMP2_DESC"
        passives {
            EMP {
                spell_graphics_override {
                    particle WaterConduct
                    center_particle WaterConduct
                    area_particle WaterConduct
                    palette -1
                }
                status_explosion_override WaterConduct
            }
            SafeExplosions 1
            IncreaseExplosionDamage 4
            BlastResistance 4

            AddPassivesToMinions {
                EMP {
                    spell_graphics_override {
                        particle WaterConduct
                        center_particle WaterConduct
                        area_particle WaterConduct
                        palette -1
                    }
                    status_explosion_override WaterConduct
                }
                SafeExplosions 1
                IncreaseExplosionDamage 4
            }
        }
    }
}
```

---

### `MrMega`
**Name:** Mr. Mega  
**Description:** Your explosions are larger and deal +3 damage.
+3 Blast Resistance.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_MRMEGA2_DESC`: "Your explosions are larger and deal +6 damage. <br/> You have explosion immunity."

```
MrMega {
    name "PASSIVE_MRMEGA_NAME"
    desc "PASSIVE_MRMEGA_DESC"
    class Tinkerer

    1 {
        passives {
            IncreaseExplosionSize 2
            IncreaseExplosionDamage 3
            BlastResistance 3

            AddPassivesToMinions {
                IncreaseExplosionSize 2
                IncreaseExplosionDamage 3
            }
        }
    }
    2 {
        desc "PASSIVE_MRMEGA2_DESC"
        passives {
            IncreaseExplosionSize 2
            ExplosionImmunity 1
            IncreaseExplosionDamage 6

            AddPassivesToMinions {
                IncreaseExplosionSize 2
                IncreaseExplosionDamage 6
            }
        }
    }
}
```

---

### `EscapeSequence`
**Name:** Escape Sequence  
**Description:** When you take damage, explode and get launched to a random tile. This explosion doesn't damage you.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_ESCAPESEQUENCE2_DESC`: "When you take damage, explode with a large blast radius and get launched to a random tile. This explosion doesn't damage you."

```
EscapeSequence {
    name "PASSIVE_ESCAPESEQUENCE_NAME"
    desc "PASSIVE_ESCAPESEQUENCE_DESC"
    class Tinkerer

    1 {
        passives {
            EscapeSequence {
                SafeExplosionIfHitSomething 5
                RandomDistanceDisplace 20
            }
        }
    }
    2 {
        desc "PASSIVE_ESCAPESEQUENCE2_DESC"
        passives {
            EscapeSequence {
                SafeExplosionIfHitSomething 10
                RandomDistanceDisplace 20
            }
        }
    }
}
```

---

### `ItemProxy`
**Name:** Item Proxy  
**Description:** You need one fewer piece of equipment to get set bonuses.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_ITEMPROXY2_DESC`: "You need two fewer pieces of equipment to get set bonuses."

```
ItemProxy {
    //PART OF THIS IS HARD CODED
    name "PASSIVE_ITEMPROXY_NAME"
    desc "PASSIVE_ITEMPROXY_DESC"
    class Tinkerer

    1 {
        passives {
            EquipmentSetBonusBonus 1
        }
    }
    2 {
        desc "PASSIVE_ITEMPROXY2_DESC"
        passives {
            EquipmentSetBonusBonus 2
        }
    }
}
```

---

### `LightningRod`
**Name:** Lightning Rod  
**Description:** You have Electric immunity and are conductive.
Electric damage you deal is increased by 1. Gain 1 Tech when you are hit with electric damage.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_LIGHTNINGROD2_DESC`: "You have Electric immunity and are conductive. <br/> Electric damage you deal is increased by 2. Gain 1 Tech and become Energized when you are hit with electric damage."

```
LightningRod {
    name "PASSIVE_LIGHTNINGROD_NAME"
    desc "PASSIVE_LIGHTNINGROD_DESC"
    class Tinkerer

    1 {
        passives {
            LightningRod {
                Tech 1
            }
            Metal 1

            AddDamageToElementDamage {
                element Electric
                damage 1
            }
        }
    }
    2 {
        desc "PASSIVE_LIGHTNINGROD2_DESC"
        passives {
            LightningRod {
                Tech 1
            }
            Metal 1
            Robot {
                allow_energize_self true
            }

            AddDamageToElementDamage {
                element Electric
                damage 2
            }
        }
    }
}
```

---

### `ItsAlive`
**Name:** IT'S ALIVE!  
**Description:** Hitting a body with electric damage revives it with 1 HP. The revived corpse is charmed and takes an extra turn, then dies.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_ITSALIVE2_DESC`: "Hitting a body with electric damage revives it with 1 HP, +8 [img:spd], and +2 Damage. The revived corpse is charmed and takes an extra turn, then dies."

```
ItsAlive {
    name "PASSIVE_ITSALIVE_NAME"
    desc "PASSIVE_ITSALIVE_DESC"
    class Tinkerer

    1 {
        passives {
            AddStatusToElementDamage {
                element Electric
                Conditional_Corpse {
                    OverrideDamage 0
                    Revive 1
                    TakeExtraTurn 1
                    Charmed 1
                    SafeDoomed 1
                }
            }
        }
    }
    2 {
        desc "PASSIVE_ITSALIVE2_DESC"
        passives {
            AddStatusToElementDamage {
                element Electric
                Conditional_Corpse {
                    OverrideDamage 0
                    Revive 1
                    TakeExtraTurn 1
                    Charmed 1
                    SafeDoomed 1
                    DamageUp 2
                    SpeedUp 8
                }
            }
        }
    }
}
```

---

### `Energizer`
**Name:** Energizer  
**Description:** When you cast a spell, your weapon gets +1 Damage.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_ENERGIZER2_DESC`: "When you cast a spell, your weapon gets +1 Damage. <br/> Every third spell you cast, repair 1 use to your weapon."

```
Energizer  {
    name "PASSIVE_ENERGIZER_NAME"
    desc "PASSIVE_ENERGIZER_DESC"
    class Tinkerer

    1 {
        passives {
            StatusOnCastSpell {
                CurrentWeaponDamageUp 1
            }
        }
    }
    2 {
        desc "PASSIVE_ENERGIZER2_DESC"
        passives {
            StatusOnCastSpell {
                CurrentWeaponDamageUp 1
            }

            StatusEveryXSpellCasts {
                stacks 3
                RepairWeapon 1
                RepairWeaponCondition 1
            }
        }
    }
}
```

---

### `ReactiveArmor`
**Name:** Reactive Armor  
**Description:** When you take damage, craft a Tinkerer weapon or armor piece and equip it in an empty slot.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_REACTIVEARMOR2_DESC`: "When you take damage, craft a Tinkerer weapon or armor piece and equip it in an empty slot and gain +1 [img:shield]."

```
ReactiveArmor  {
    name "PASSIVE_REACTIVEARMOR_NAME"
    desc "PASSIVE_REACTIVEARMOR_DESC"
    class Tinkerer

    1 {
        passives {
            StatusOnTookDamage {
                Craft {
                    pool tinkerer_default
                    slot random_empty_armor_or_weapon
                }
            }
        }
    }
    2 {
        desc "PASSIVE_REACTIVEARMOR2_DESC"
        passives {
            StatusOnTookDamage {
                Craft {
                    pool tinkerer_default
                    slot random_empty_armor_or_weapon
                }
                Shield 1
            }
        }
    }
}
```

---

### `Nanobots`
**Name:** Nanobots  
**Description:** Gain +2 Diminishing Health Regeneration every time you take damage from an attack or spell.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_NANOBOTS2_DESC`: "Gain +2 Diminishing Health Regeneration every time you take damage from an attack or spell and +1 Diminishing Health Regeneration each time you take damage from any other source."

```
Nanobots  {
    name "PASSIVE_NANOBOTS_NAME"
    desc "PASSIVE_NANOBOTS_DESC"
    class Tinkerer

    1 {
        passives {
            StatusOnTookDamageFromAbility {
                DiminishingHealthRegen 2
            }
        }
    }
    2 {
        desc "PASSIVE_NANOBOTS2_DESC"
        passives {
            StatusOnTookDamageFromAbility {
                DiminishingHealthRegen 1
            }
            StatusOnTookDamage {
                DiminishingHealthRegen 1
            }
        }
    }
}
```

---

### `Scrapper`
**Name:** Scrapper  
**Description:** Find an extra consumable item at the end of each battle.
When you use up a consumable or trinket, equip a new consumable from your inventory if you have any.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_SCRAPPER2_DESC`: "Find an extra item at the end of each battle. <br/> When you use up a consumable or trinket, equip a new consumable from your inventory if you have any."

```
Scrapper  {
    name "PASSIVE_SCRAPPER_NAME"
    desc "PASSIVE_SCRAPPER_DESC"
    class Tinkerer

    1 {
        passives {
            StatusOnBattleEnd {
                FindItemFromPool consumables
            }
            AutoEquipConsumables 1
        }
    }
    2 {
        desc "PASSIVE_SCRAPPER2_DESC"
        passives {
            StatusOnBattleEnd {
                FindItemFromPool chapter
            }
            AutoEquipConsumables 1
        }
    }
}
```

---

### `DemoMan`
**Name:** Demo Man  
**Description:** Always craft a bomb at Tech 1 or less.
+2 Blast Resistance.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_DEMOMAN2_DESC`: "Always craft a bomb at Tech 1 or less. You can use your basic action an additional time on each of your turns. <br/> +3 Blast Resistance."

```
DemoMan  {
    name "PASSIVE_DEMOMAN_NAME"
    desc "PASSIVE_DEMOMAN_DESC"
    class Tinkerer

    1 {
        passives {
            AlternateCraftingPools {
                tinkerer_0 tinkerer_0_bombs
                tinkerer_1 tinkerer_1_bombs
            }
            BlastResistance 2
        }
    }
    2 {
        desc "PASSIVE_DEMOMAN2_DESC"
        passives {
            AlternateCraftingPools {
                tinkerer_0 tinkerer_0_bombs
                tinkerer_1 tinkerer_1_bombs
            }
            ExtraBasicAttacks 1
            BlastResistance 3
        }
    }
}
```

---

### `DuctTape`
**Name:** Duct Tape  
**Description:** Items you craft stay with you between battles, but become cursed.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_DUCTTAPE2_DESC`: "Items you craft stay with you between battles."

```
DuctTape  {
    name "PASSIVE_DUCTTAPE_NAME"
    desc "PASSIVE_DUCTTAPE_DESC"
    class Tinkerer

    1 {
        passives {
            PermanentItems 1
        }
    }
    2 {
        desc "PASSIVE_DUCTTAPE2_DESC"
        passives {
            PermanentItems 2
        }
    }
}
```

---

### `ArmoredPlating`
**Name:** Armored Plating  
**Description:** Robots you spawn gain the stats and [img:shield] of your equipped armor.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_ARMOREDPLATING2_DESC`: "Robots you spawn gain the stats, [img:shield] and passive effects of your equipped armor."

```
ArmoredPlating  {
    name "PASSIVE_ARMOREDPLATING_NAME"
    desc "PASSIVE_ARMOREDPLATING_DESC"
    class Tinkerer

    1 {
        passives {
            RobotsInheritArmor 1
        }
    }
    2 {
        desc "PASSIVE_ARMOREDPLATING2_DESC"
        passives {
            RobotsInheritArmor 2
        }
    }
}
```

---

### `BoobyTrap`
**Name:** Booby Trap  
**Description:** When an item you have equipped breaks, it explodes!  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_BOOBYTRAP2_DESC`: "When an item you have equipped breaks, it explodes with bonus damage!"

```
BoobyTrap  {
    name "PASSIVE_BOOBYTRAP_NAME"
    desc "PASSIVE_BOOBYTRAP_DESC"
    class Tinkerer

    1 {
        passives {
            BoobyTrapItems {
                on_throw {
                    HitExplosion 5
                }
                on_break {
                    SafeExplosionIfHitSomething 5
                }
            }
        }
    }
    2 {
        desc "PASSIVE_BOOBYTRAP2_DESC"
        passives {
            BoobyTrapItems {
                on_throw {
                    HitExplosion 10
                }
                on_break {
                    SafeExplosionIfHitSomething 10
                }
            }
        }
    }
}
```

---

### `RobotArms`
**Name:** Robot Arms  
**Description:** You can use your weapon an additional time each turn.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_ROBOTARMS2_DESC`: "You can use your weapon and trinket an additional time each turn. <br/> Whenever you equip a new item during battle it gains +1 use."

```
RobotArms  {
    name "PASSIVE_ROBOTARMS_NAME"
    desc "PASSIVE_ROBOTARMS_DESC"
    class Tinkerer

    1 {
        passives {
            ExtraWeaponAttacks 1
        }
    }
    2 {
        desc "PASSIVE_ROBOTARMS2_DESC"
        passives {
            ExtraWeaponAttacks 1
            ExtraTrinketUses 1
            IncreaseItemUsesOnEquip 1
        }
    }
}
```

---

### `Conductor`
**Name:** Conductor  
**Description:** Electric damage you deal is increased by 2 for each piece of metal armor you have equipped.
If you are wearing metal, your weapon deals electric damage.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_CONDUCTOR2_DESC`: "Electric damage you deal is increased by 2 for each piece of metal armor you have equipped. You have +2 Mana Regeneration for each piece of metal armor. <br/> If you are wearing metal, your weapon deals electric damage."

```
Conductor  {
    name "PASSIVE_CONDUCTOR_NAME"
    desc "PASSIVE_CONDUCTOR_DESC"
    class Tinkerer

    1 {
        passives {
            Conductor 2
            PassiveWhileWearingMetal {
                AddElementsToWeapon Electric
            }
        }
    }
    2 {
        desc "PASSIVE_CONDUCTOR2_DESC"
        passives {
            Conductor 2
            ConductorManaRegen 2
            PassiveWhileWearingMetal {
                AddElementsToWeapon Electric
            }
        }
    }
}
```

---

### `Napalm`
**Name:** Napalm  
**Description:** Your explosions inflict Burn 3 and light tiles on fire.
+2 Blast Resistance.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_NAPALM2_DESC`: "Your explosions inflict Burn 6 and light tiles on fire. <br/> +3 Blast Resistance."

```
Napalm  {
    name "PASSIVE_NAPALM_NAME"
    desc "PASSIVE_NAPALM_DESC"
    class Tinkerer

    1 {
        passives {
            AddStatusToExplosions {
                AddElement Napalm
                AddElement Fire
                Burn 3
            }
            AddPassivesToMinions {
                AddStatusToExplosions {
                    AddElement Napalm
                    AddElement Fire
                    Burn 3
                }
            }
            BlastResistance 2
        }
    }
    2 {
        desc "PASSIVE_NAPALM2_DESC"
        passives {
            AddStatusToExplosions {
                AddElement Napalm
                AddElement Fire
                Burn 6
            }
            AddPassivesToMinions {
                AddStatusToExplosions {
                    AddElement Napalm
                    AddElement Fire
                    Burn 6
                }
            }
            BlastResistance 3
        }
    }
}
```

---

### `Ingenuity`
**Name:** Ingenuity  
**Description:** Pickups give you +1 Tech in addition to their other effects.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_INGENUITY2_DESC`: "Pickups give you +1 Tech in addition to their other effects. <br/> 10 extra pickups spawn at the start of each battle."

```
Ingenuity {
    name "PASSIVE_INGENUITY_NAME"
    desc "PASSIVE_INGENUITY_DESC"
    class Tinkerer

    1 {
        passives {
            StatusOnCollectPickup {
                Tech 1
            }
        }
    }
    2 {
        desc "PASSIVE_INGENUITY2_DESC"
        passives {
            StatusOnCollectPickup {
                Tech 1
            }
            SpawnOnBattleStartRandomEmptyTile {
                object RandomPickup
                number 10
            }
        }
    }
}
```

---

### `Shrapnel_Tinkerer`
**Name:** Shrapnel  
**Description:** When you break an item, gain +1 Thorns.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_SHRAPNEL2_TINKERER_DESC`: "When you break an item, gain +2 Thorns and +3 [img:shield]."

```
Shrapnel_Tinkerer {
    name "PASSIVE_SHRAPNEL_TINKERER_NAME"
    desc "PASSIVE_SHRAPNEL_TINKERER_DESC"
    class Tinkerer

    1 {
        passives {
            StatusOnBreakItem {
                Thorns 1
            }
        }
    }
    2 {
        desc "PASSIVE_SHRAPNEL2_TINKERER_DESC"
        passives {
            StatusOnBreakItem {
                Thorns 2
                Shield 3
            }
        }
    }
}
```

---

### `Blacksmith`
**Name:** Blacksmith  
**Description:** If you have a weapon, your basic attack becomes Hone.  
**Source:** `tinkerer_passives.gon`  

**Localization Strings:**
- `PASSIVE_BLACKSMITH2_DESC`: "If you have a weapon, your basic attack becomes Hone+."

```
Blacksmith {
    name "PASSIVE_BLACKSMITH_NAME"
    desc "PASSIVE_BLACKSMITH_DESC"
    class Tinkerer

    1 {
        passives {
            ReplaceBasicAttackWhenCastable Hone
        }
    }
    2 {
        desc "PASSIVE_BLACKSMITH2_DESC"

        passives {
            ReplaceBasicAttackWhenCastable Hone2
        }
    }
}
```

---

## File: `util_passives.gon`

### `STARTER_PLACEHOLDER_Fighter`
**Name:** ???  
**Description:** Becomes a random Fighter passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Fighter {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_FIGHTER_DESC"
    class Fighter

}
```

---

### `STARTER_PLACEHOLDER_Thief`
**Name:** ???  
**Description:** Becomes a random Thief passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Thief {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_THIEF_DESC"
    class Thief
    
}
```

---

### `STARTER_PLACEHOLDER_Tank`
**Name:** ???  
**Description:** Becomes a random Tank passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Tank {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_TANK_DESC"
    class Tank
    
}
```

---

### `STARTER_PLACEHOLDER_Mage`
**Name:** ???  
**Description:** Becomes a random Mage passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Mage {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_MAGE_DESC"
    class Mage
    
}
```

---

### `STARTER_PLACEHOLDER_Medic`
**Name:** ???  
**Description:** Becomes a random Cleric passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Medic {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_MEDIC_DESC"
    class Medic
    
}
```

---

### `STARTER_PLACEHOLDER_Hunter`
**Name:** ???  
**Description:** Becomes a random Hunter passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Hunter {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_HUNTER_DESC"
    class Hunter
    
}
```

---

### `STARTER_PLACEHOLDER_Necromancer`
**Name:** ???  
**Description:** Becomes a random Necromancer passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Necromancer {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_NECROMANCER_DESC"
    class Necromancer
    
}
```

---

### `STARTER_PLACEHOLDER_Butcher`
**Name:** ???  
**Description:** Becomes a random Butcher passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Butcher {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_BUTCHER_DESC"
    class Butcher
    
}
```

---

### `STARTER_PLACEHOLDER_Monk`
**Name:** ???  
**Description:** Becomes a random Monk passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Monk {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_MONK_DESC"
    class Monk
    
}
```

---

### `STARTER_PLACEHOLDER_Druid`
**Name:** ???  
**Description:** Becomes a random Druid passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Druid {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_DRUID_DESC"
    class Druid
    
}
```

---

### `STARTER_PLACEHOLDER_Psychic`
**Name:** ???  
**Description:** Becomes a random Psychic passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Psychic {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_PSYCHIC_DESC"
    class Psychic
    
}
```

---

### `STARTER_PLACEHOLDER_Tinkerer`
**Name:** ???  
**Description:** Becomes a random Tinkerer passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Tinkerer {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_TINKERER_DESC"
    class Tinkerer
    
}
```

---

### `STARTER_PLACEHOLDER_Colorless`
**Name:** ???  
**Description:** Becomes a random Collarless passive when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Colorless {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_COLORLESS_DESC"
    class Colorless
    
}
```

---

### `STARTER_PLACEHOLDER_Jester`
**Name:** ???  
**Description:** Becomes a random passive from any class when you lock in your team's collars.  
**Source:** `util_passives.gon`  

```
STARTER_PLACEHOLDER_Jester {

    name "PASSIVE_STARTER_PLACEHOLDER_NAME"
    desc "PASSIVE_STARTER_PLACEHOLDER_JESTER_DESC"
    class Colorless
    
}
```

---

