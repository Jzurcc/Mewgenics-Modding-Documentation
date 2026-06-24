# Statuses & Disorders Directory

## Disorders

### `Rabies`
**Name:** Rabies  
**Description:** Your basic attack is a melee attack. You can't equip face armor.
After each battle, gain +2 [img:str] and -1 [img:int].
If your [img:int] is 0 or less, you have Madness.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Boils`
**Name:** Boils  
**Description:** +1 Brace.
You spawn a puddle of creep whenever you get hit. You can't equip face armor.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Depression`
**Name:** Depression  
**Description:** Adjacent units get All Stats Down 2.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `BrokenLimb`
**Name:** Broken Limb  
**Description:** You can't equip trinkets or consumables. +2 Thorns.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `WrenchedNeck`
**Name:** Wrenched Neck  
**Description:** You can't equip neck armor. Double the effects of your head armor.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Declawed`
**Name:** Declawed  
**Description:** You can't equip weapons.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `HeadTrauma`
**Name:** Head Trauma  
**Description:** You can't equip head armor. Your Collarless spells cost -2 mana.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `DeepCut`
**Name:** Deep Cut  
**Description:** Bleed 1.
You can't equip trinkets or consumables. 
Bonus ability: Bloodzerk.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `PuncturedEye`
**Name:** Punctured Eye  
**Description:** +10% miss chance.
You can't equip face armor. Gain an eyeball trinket.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `OCD`
**Name:** Obsessive Compulsive Disorder  
**Description:** Bonus Ability: Groom
At the end of your turn, if you didn't use Groom, take 2 damage.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Distemper`
**Name:** Distemper  
**Description:** At the end of each battle gain +10% crit chance, +25% crit damage, and +5% miss chance. Permanently.
You can't equip face armor.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `BrainDamage`
**Name:** Brain Damage  
**Description:** You can't use item actions. +2 Brace.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `SeveredThumb`
**Name:** Severed Thumb  
**Description:** You can't equip weapons. Spawn a Food pickup at the start of each battle.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `PTSD`
**Name:** Post-Traumatic Stress Disorder  
**Description:** When you take damage, gain Fear and +2 Damage.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `IBS`
**Name:** Irritable Bowel Syndrome  
**Description:** When you take damage, poop.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Dyskinesia`
**Name:** Dyskinesia  
**Description:** When you end your movement, knockback all adjacent units 1 tile.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Anemia`
**Name:** Anemia  
**Description:** When you take damage, you have a 10% chance to gain Bleed 1.
Gain 2 Charge for each damage you take from Bleed.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Empath`
**Name:** Empath  
**Description:** Take 1 damage when you deal damage.
Your heals heal for 1 extra.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Infestation`
**Name:** Infestation  
**Description:** At the start of your turn, you have a 50% chance to spawn a Maggot Familiar and 15% chance to spawn an enemy Flea.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Leprosy`
**Name:** Leprosy  
**Description:** Bruise 2. When you get hit, spawn a food pickup.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `ASRFight`
**Name:** Acute Stress Reaction: Fight  
**Description:** Gain +6 [img:str] while you have 5 or fewer HP.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `ASRFlight`
**Name:** Acute Stress Reaction: Flight  
**Description:** Gain +6 [img:spd] while you have 5 or fewer HP.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `BloodFrenzy`
**Name:** Blood Frenzy  
**Description:** When you kill a unit, take an extra turn with Madness.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Shunned`
**Name:** Shunned  
**Description:** Take your turn last.
Your heals heal for 2 less. +15% dodge chance.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Dysentery`
**Name:** Dysentery  
**Description:** 50% chance to make a burning poop directly behind you when you end your turn.  

<details>
<summary><b>Raw .gon</b></summary>

```
Dysentery {
    name "DISORDER_DYSENTERY_NAME"
    desc "DISORDER_DYSENTERY_DESC"
    class Disorder

    passives {
        
        StatusEachTurnEnd {
            ForceUseAbility {
                chance .5
                ability DysenteryPoop
            }
        }
    }
}
```

</details>

---

### `Anxiety`
**Name:** Anxiety  
**Description:** +10% Dodge chance. When you take damage, run away from the source.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Kamikazee`
**Name:** Kamikaze  
**Description:** You explode when you are downed.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Traumatophobia`
**Name:** Traumatophobia  
**Description:** Whenever you take damage, move 1 tile away from the source.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `StockholmSyndrome`
**Name:** Stockholm Syndrome  
**Description:** Whenever you take damage, move toward the source.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `ViolentOutbursts`
**Name:** Violent Outbursts  
**Description:** When you end your turn, dash forward 2 tiles, attack with Knockback, and take 1 damage.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `GamblingAddict`
**Name:** Gambling Addiction  
**Description:** +33% miss chance.
100% critical hit chance.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Scleroderma`
**Name:** Scleroderma  
**Description:** At the start of each battle, you lose all but 1 HP, but gain that much [img:shield].  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Pacifist`
**Name:** Pacifist  
**Description:** You can't kill units. If you end your turn without using your basic attack gain 7 mana.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Gigachad`
**Name:** GIGACHAD  
**Description:** DISORDER_GIGACHAD_DESC  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `ImposterSyndrome`
**Name:** Impostor Syndrome  
**Description:** You're quite suspicious…  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Vegan`
**Name:** Vegan  
**Description:** You don't eat meat.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `FrozenKnee`
**Name:** The Zoomies  
**Description:** Your movement action is a dash attack.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `SchrodingerDisorder`
**Name:** Schrödinger's Syndrome  
**Description:** 50% chance to start each battle dead, or alive with max hp and All Stats Up 2 and an extra turn at the start of the battle.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `ScalyScabs`
**Name:** Scaly Scabs  
**Description:** DISORDER_SCALYSCABS_DESC  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `FattyLiver`
**Name:** Fatty Liver  
**Description:** Whenever you lose HP, you permanently lose 1 [img:con].  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `CommonCold`
**Name:** The Common Cold  
**Description:** Start each battle with All Stats Down. 30% chance of recovering at the end of each round. Contagious.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Pox`
**Name:** Pox  
**Description:** 10% chance to skip your turn to scratch yourself. Your basic attack has a 50% chance to inflict Poison 1. 5% chance of recovering at the end of each round. Contagious.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Psychosis`
**Name:** Psychosis  
**Description:** After your first turn, you have permanent madness.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Necrosis`
**Name:** Necrosis  
**Description:** When you take damage, you get -1 [img:con], -1 [img:str], and spawn poisoned food.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Touched`
**Name:** Touched  
**Description:** You can no longer heal HP.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Charred`
**Name:** Charred  
**Description:** Bruise 1. You cannot be Burned.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Invincible`
**Name:** Immortal  
**Description:** All damage you take is reduced to 1.
When you take damage, suffer a random injury.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `ExplosiveGas`
**Name:** Bad Gas  
**Description:** On the first round, take your turn last. At the start of that turn, do a Mega Fart attack that inflicts Poison 2.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Toxoplasmosis`
**Name:** Toxoplasmosis  
**Description:** Start each battle with a Rat Familiar. Your basic attack charms Rat enemies.  

<details>
<summary><b>Raw .gon</b></summary>

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
    
}
```

</details>

---

### `Ebola`
**Name:** Ebola  
**Description:** Start each battle with Bleed 3. Your basic attack inflicts Bleed 2.
5% chance of recovering at the end of each round. Contagious.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Fidgety`
**Name:** Fidgety  
**Description:** When you end your turn, automatically use your weapon on a random unit in range, for free.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Narcolepsy`
**Name:** Narcolepsy  
**Description:** At the end of your turn, fall asleep, heal 10 HP and gain 7 mana.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Paranoia`
**Name:** Paranoia  
**Description:** When a unit ends its movement directly behind you, attack it and gain Fear.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `EatingDisorder`
**Name:** Eating Disorder  
**Description:** Double the effects of your consumables but you are confused on how to eat them.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Gastritis`
**Name:** Gastritis  
**Description:** At the end of your turn, fart and Poison all adjacent units.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Hypomania`
**Name:** Hypomania  
**Description:** Start each battle with 3 bonus turns, then never take a turn.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Hypersomnia`
**Name:** Hypersomnia  
**Description:** Start each battle asleep and with full health.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `KidneyStones`
**Name:** Kidney Stone  
**Description:** When you end your turn take 1 damage and pass a kidney stone.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Cancer`
**Name:** Cancer  
**Description:** At the end of each battle, lose 3 random stats permanently and gain a random mutation.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Stinky`
**Name:** Stinky  
**Description:** Adjacent units move away from you at the start of their turns.  

<details>
<summary><b>Raw .gon</b></summary>

```
Stinky {
    name "DISORDER_STINKY_NAME"
    desc "DISORDER_STINKY_DESC"
    class Disorder

    passives {
        StatusAdjacentOnTheirTurnBegin {
            ForceMoveAway {
                free false 
            }
        }
    }
}
```

</details>

---

### `Incontinence`
**Name:** Incontinence  
**Description:** When you take damage, pee yourself.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Fossilized`
**Name:** Fossilized  
**Description:** +2 Brace. Slide like a rock whenever you get hit.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Triskaidekaphobia`
**Name:** Triskaidekaphobia  
**Description:** Your spells cost 0 mana. The 13th spell you cast on an adventure kills you and destroys your body.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Autism`
**Name:** Autism  
**Description:** Spells you were born with cost -2 mana. Other spells cost +1 mana.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Tourettes`
**Name:** Tourette's Syndrome  
**Description:** At the start of your turn, you have a 33% chance to cast one of your spells at a random target for free.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Albinism`
**Name:** Albinism  
**Description:** Fire damage you take inflicts +3 Burn.
Your basic attack has a 25% chance to inflict Fear.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `SleepParalysis`
**Name:** Sleep Paralysis  
**Description:** When you fall asleep, a Sleep Paralysis Demon with Madness spawns! You can't wake up until it's killed.
Learn the spell Rest (if you have a free spell slot).  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Diabetes`
**Name:** Diabetes  
**Description:** When you end your turn, if you haven't eaten food, gain All Stats Down and Confusion 1. Each time you eat food, cleanse all your debuffs and gain +1 [img:int].  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Bipolar`
**Name:** Bipolar Disorder  
**Description:** Start each battle with either
 +5 [img:int], +5 [img:cha], and +5 [img:spd]
or 
All Stats Down 2.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Soulless`
**Name:** Soulless  
**Description:** You are immune to buffs and debuffs. When you die, you don't leave a corpse.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Premonitions`
**Name:** The Shining  
**Description:** Your attacks can't miss.
+15% dodge chance and +15% chance to gain Fear at the start of each turn.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `PillPopper`
**Name:** Addict  
**Description:** Start each battle with All Stats Down 2.
Gain All Stats Up 3 whenever you eat a pill.
You have a 50% chance to find a pill at the end of each battle.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `BorrowedTime`
**Name:** Borrowed Time  
**Description:** +50% dodge chance. Doomed 3.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Brave`
**Name:** Brave  
**Description:** Take your turn earlier.
Immune to Fear and Madness.
Attacks against you never miss.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Scatological`
**Name:** Scatological  
**Description:** Heal 5 HP when you damage poop.
At the start of your turn, if you're near poop, you automatically move toward it and eat it.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Cannibal`
**Name:** Necrophage  
**Description:** At the start of your turn, if there's a dead body near you, move towards it and eat it to gain All Stats Up and heal 4 HP.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `CrohnsDisease`
**Name:** Crohn's Disease  
**Description:** At the end of your turn, you have a 20% chance to poop all over the place!  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Pica`
**Name:** Pica  
**Description:** When you collect a coin or scrap pickup, heal instead of gaining the pickup's normal effect.  

<details>
<summary><b>Raw .gon</b></summary>

```
Pica {
    name "DISORDER_PICA_NAME"
    desc "DISORDER_PICA_DESC"
    class Disorder

    passives {
        TaggedPickupEffectReplacement {
            tag money

            HealthGain 3*X 
        }
        TaggedPickupEffectReplacement {
            tag scrap

            HealthGain 2*X 
        }
    }
}
```

</details>

---

### `FelineAids`
**Name:** Feline Aids  
**Description:** Your basic attack inflicts Poison 3 and Weakness 1.
Inflict Poison 3 and Weakness 1 on units that contact you.
Gain -1 [img:con] and -1 [img:spd] at the end of each battle permanently.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Dyslexia`
**Name:** Dyslexia  
**Description:** Swap 3's and 5's in the mana costs and damage values of your spells while in a battle. 6's and 9's are also swapped.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Covid`
**Name:** Covid  
**Description:** Start each battle with All Stats Down, Poison 1, and Weakness 1.
Your basic attack inflicts Poison 1 and Weakness 1.
15% chance of recovering at the end of each round. Contagious.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Flu`
**Name:** The Flu  
**Description:** Start each battle with Slow 5 and Weakness 5.
Your basic attack inflicts Slow 1 and Weakness 1.
20% chance of recovering at the end of each round. Contagious.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `BirdFlu`
**Name:** Bird Flu  
**Description:** Start each battle in Mockingbird Form.
You have a 20% chance to recover at the end of each battle.
Contagious.  

<details>
<summary><b>Raw .gon</b></summary>

```
BirdFlu {
    name "DISORDER_BIRDFLU_NAME"
    desc "DISORDER_BIRDFLU_DESC"
    class Disorder

    passives {
        
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

</details>

---

### `Nudist`
**Name:** Nudist  
**Description:** +50% dodge chance.
You can't wear armor.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Elephantiasis`
**Name:** Elephantiasis  
**Description:** At the end of each battle, gain -1 [img:spd] and +2 starting [img:shield] permanently. After 8 battles, gain Trample.  

<details>
<summary><b>Raw .gon</b></summary>

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

            Trample [3, X-8] 
        }
    }
}
```

</details>

---

### `Gigantism`
**Name:** Gigantism  
**Description:** Trample.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Dwarfism`
**Name:** Dwarfism  
**Description:** +10% dodge chance.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `PrimordialDwarf`
**Name:** Primordial Dwarf  
**Description:** DISORDER_PRIMORDIALDWARF_DESC  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Sociopathy`
**Name:** Sociopathy  
**Description:** You have Madness on your first turn.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `SkillShare_Disorder`
**Name:** Munchausen by Proxy  
**Description:** If you have a 2nd disorder, all other cats in your party gain it at the start of each battle.  

<details>
<summary><b>Raw .gon</b></summary>

```
SkillShare_Disorder { 
    name "DISORDER_SKILLSHAREDISORDER_NAME"
    desc "DISORDER_SKILLSHAREDISORDER_DESC"
    class Disorder

    passives {
        
    }
}
```

</details>

---

### `Schizophrenia`
**Name:** Schizophrenia  
**Description:** At the end of your turn, spawn a hallucination. It has Madness, attacks any unit except you, and fades after its turn.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Lycanthropy`
**Name:** Lycanthropy  
**Description:** 33% chance to enter Wolf Form at the start of your turn.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `WobblyCat`
**Name:** Wobbly Cat Syndrome  
**Description:** 25% chance to block attacks and get knocked back 10 tiles instead.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Singleton`
**Name:** Singleton  
**Description:** Your max HP and mana are reduced to 1.
Damage you take is reduced to 1.
Your spells cost 1 mana.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Insomnia`
**Name:** Insomnia  
**Description:** You can't fall asleep.
You can move an extra time each turn. Exhaustion sets in on round 3.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Phony`
**Name:** Phony  
**Description:** Start each battle with full mana.
You can't regenerate mana.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `AcidReflux`
**Name:** Acid Reflux  
**Description:** Your basic attack becomes a lobbed shot with splash damage but deals 2 damage to you.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `SpontaneousCombustion`
**Name:** Spontaneous Combustion  
**Description:** When you take damage from an ability, you have a 15% chance to inflict Burn 5 on yourself and adjacent units.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `TheHunger`
**Name:** The Hunger  
**Description:** Your basic attack has lifesteal.
If you don't deal damage to a unit on your turn, gain Madness 1.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Paralyzed`
**Name:** Paraplegic  
**Description:** The range of all your movement, dash, and jump abilities are capped at 1 unless they teleport.
Enemies won't prioritize attacking you.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `GlassBones`
**Name:** Osteogenesis Imperfecta  
**Description:** +2 Bruise, +2 Bleed Thorns, and +2 Thorns.
When you're downed, you get injured an extra time.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Gargantuan`
**Name:** Gargantuan  
**Description:** You are permanently immobile.  

<details>
<summary><b>Raw .gon</b></summary>

```
Gargantuan { 
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

</details>

---

### `BrainDead`
**Name:** Brain Dead  
**Description:** Gain twice as many stats when you level up. +1 Reroll when leveling up.  

<details>
<summary><b>Raw .gon</b></summary>

```
BrainDead { 
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

</details>

---

### `TamperedGenes`
**Name:** Tainted Genes  
**Description:** At the end of each battle gain a random mutation. When you're downed, your corpse is destroyed.  

<details>
<summary><b>Raw .gon</b></summary>

```
TamperedGenes { 
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

</details>

---

### `SensoryOverloadFace`
**Name:** Sensory Overload  
**Description:** All but your face slot is locked. Your face item's effects are tripled!  

<details>
<summary><b>Raw .gon</b></summary>

```
SensoryOverloadFace { 
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

</details>

---

### `SensoryOverloadTrinket`
**Name:** Sensory Overload  
**Description:** All but your trinket slot is locked. Your trinket's effects are tripled!  

<details>
<summary><b>Raw .gon</b></summary>

```
SensoryOverloadTrinket { 
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

</details>

---

### `SensoryOverloadHead`
**Name:** Sensory Overload  
**Description:** All but your head slot is locked. Your head item's effects are tripled!  

<details>
<summary><b>Raw .gon</b></summary>

```
SensoryOverloadHead { 
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

</details>

---

### `SensoryOverloadNeck`
**Name:** Sensory Overload  
**Description:** All but your neck slot is locked. Your neck item's effects are tripled!  

<details>
<summary><b>Raw .gon</b></summary>

```
SensoryOverloadNeck { 
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

</details>

---

### `SensoryOverloadWeapon`
**Name:** Sensory Overload  
**Description:** All but your weapon slot is locked. Your weapon's effects are tripled!  

<details>
<summary><b>Raw .gon</b></summary>

```
SensoryOverloadWeapon { 
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

</details>

---

### `EternalYouth`
**Name:** Eternal Youth  
**Description:** You are a kitten... forever!
+1 [img:comfort], +1 [img:stimulation], +1 [img:appeal]  

<details>
<summary><b>Raw .gon</b></summary>

```
EternalYouth { 
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

</details>

---

### `DejaVu`
**Name:** Deja Vu  
**Description:** 10% chance to cancel actions.
[s:.7]Deja Vu will go away when this cat returns to the house.[/s]  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `DownsSyndrome`
**Name:** Down's Syndrome  
**Description:** DISORDER_DOWNSSYNDROME_DESC  

<details>
<summary><b>Raw .gon</b></summary>

```
DownsSyndrome {
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

</details>

---

### `Tachysensia`
**Name:** Tachysensia  
**Description:** DISORDER_TACHYSENSIA_DESC  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `SavantSyndrome`
**Name:** Savant Syndrome  
**Description:** DISORDER_SAVANTSYNDROME_DESC  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `WilliamsSyndrome`
**Name:** Williams Syndrome  
**Description:** Your attacks may Charm.  

<details>
<summary><b>Raw .gon</b></summary>

```
WilliamsSyndrome {
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

</details>

---

### `SpinaBifida`
**Name:** Spina Bifida  
**Description:** DISORDER_SPINABIFIDA_DESC  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `DarkOne`
**Name:** Dark One  
**Description:** At end of your turn, deal 1 damage to all units and heal for the damage dealt. Whenever you down an ally gain All Stats Up.  

<details>
<summary><b>Raw .gon</b></summary>

```
DarkOne { 
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

</details>

---

### `ADHD`
**Name:** ADHD  
**Description:** You have 5 seconds to make decisions, or else this cat acts on its own.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `FlamingFists`
**Name:** Flaming Fists  
**Description:** Your basic attacks inflict Burn 1. Start with Burn 1.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `IntestinalProlapse`
**Name:** Intestinal Prolapse  
**Description:** You receive double damage from behind.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `BlessingOfGlorg`
**Name:** Blessing of Glorg  
**Description:** You can unequip cursed items.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `BlackFetin`
**Name:** Black Fetin  
**Description:** You have a 10% to be AI controlled each turn.
When an ally cat is downed, restore all your mana.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `OrangeFetin`
**Name:** Orange Fetin  
**Description:** You have a 10% to be AI controlled each turn.
When you kill an enemy, gain 3 mana and heal 2 hp.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `PurpleFetin`
**Name:** Purple Fetin  
**Description:** You have a 10% to be AI controlled each turn.
You can reroll your level up options 3 times.  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

### `Chungus`
**Name:** Chungus  
**Description:** DISORDER_CHUNGUS_DESC  

<details>
<summary><b>Raw .gon</b></summary>

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

</details>

---

## Status Keywords (from keyword_tooltips.gon)

### `Adrenaline`
**Name:** Adrenaline  

<details>
<summary><b>Raw .gon</b></summary>

```
Adrenaline {
    name "KEYWORD_ADRENALINE_NAME"
    tooltip "KEYWORD_ADRENALINE_DESC"
}
```

</details>

---

### `AllStatsUp`
**Name:** AllStatsUp  

<details>
<summary><b>Raw .gon</b></summary>

```
AllStatsUp {
    name "KEYWORD_ALLSTATSUP_NAME"
    name_stacks_neg "KEYWORD_ALLSTATSDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_ALLSTATSUP_DESC"
    tooltip_stacks_neg "KEYWORD_ALLSTATSDOWN_DESC"

    tooltip_stackless none
    
    
}
```

</details>

---

### `AlphaAllStatsUp`
**Name:** AlphaAllStatsUp  

| Field | Value |
| :--- | :--- |
| Alias | AllStatsUp |

<details>
<summary><b>Raw .gon</b></summary>

```
AlphaAllStatsUp {
    alias AllStatsUp
}
```

</details>

---

### `AlphaDodgeChance`
**Name:** AlphaDodgeChance  

| Field | Value |
| :--- | :--- |
| Alias | DodgeChance_Status |

<details>
<summary><b>Raw .gon</b></summary>

```
AlphaDodgeChance {
    alias DodgeChance_Status
}
```

</details>

---

### `AlphaCat`
**Name:** AlphaCat  

<details>
<summary><b>Raw .gon</b></summary>

```
AlphaCat {
    name "KEYWORD_ALPHA_NAME"
    tooltip "KEYWORD_ALPHA_DESC"
    tooltip_stackless "KEYWORD_ALPHA_DESC_STACKLESS"
}
```

</details>

---

### `AllyDodgeChanceAura`
**Name:** AllyDodgeChanceAura  

| Field | Value |
| :--- | :--- |
| Alias | DodgeChance_Status |

<details>
<summary><b>Raw .gon</b></summary>

```
AllyDodgeChanceAura {
    alias DodgeChance_Status
}
```

</details>

---

### `LowHealthAllyDodgeChanceAura`
**Name:** LowHealthAllyDodgeChanceAura  

| Field | Value |
| :--- | :--- |
| Alias | DodgeChance_Status |

<details>
<summary><b>Raw .gon</b></summary>

```
LowHealthAllyDodgeChanceAura {
    alias DodgeChance_Status
}
```

</details>

---

### `AllyInfested`
**Name:** AllyInfested  

| Field | Value |
| :--- | :--- |
| Alias | Infested |

<details>
<summary><b>Raw .gon</b></summary>

```
AllyInfested {
    alias Infested
}
```

</details>

---

### `Ammo`
**Name:** Ammo  

<details>
<summary><b>Raw .gon</b></summary>

```
Ammo { 
    name "KEYWORD_AMMO_NAME"
    tooltip_stacks "KEYWORD_AMMO_DESC"
    tooltip_stackless none 
}
```

</details>

---

### `Attraction`
**Name:** Attraction  

<details>
<summary><b>Raw .gon</b></summary>

```
Attraction {
    name "KEYWORD_ATTRACTION_NAME"
    name_reference_applier "KEYWORD_ATTRACTION_REF"
    tooltip_stacks "KEYWORD_ATTRACTION_DESC"
    tooltip_reference_applier "KEYWORD_ATTRACTION_DESC_REF"

    tooltip_stackless "KEYWORD_ATTRACTION_DESC_STACKLESS"
}
```

</details>

---

### `BackflipWhenTargeted`
**Name:** BackflipWhenTargeted  

<details>
<summary><b>Raw .gon</b></summary>

```
BackflipWhenTargeted {
    name "KEYWORD_BACKFLIP_NAME"
    tooltip "KEYWORD_BACKFLIP_DESC"
}
```

</details>

---

### `BlastResistance`
**Name:** BlastResistance  

<details>
<summary><b>Raw .gon</b></summary>

```
BlastResistance {
    name "KEYWORD_BLASTRESISTANCE_NAME"
    tooltip_stacks "KEYWORD_BLASTRESISTANCE_DESC"
    tooltip_stackless "KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"
}
```

</details>

---

### `Bleed`
**Name:** Bleed  

<details>
<summary><b>Raw .gon</b></summary>

```
Bleed {
    name "KEYWORD_BLEED_NAME"
    tooltip_stacks "KEYWORD_BLEED_DESC"
    tooltip_stackless "KEYWORD_BLEED_DESC_STACKLESS"
}
```

</details>

---

### `BleedThorns`
**Name:** BleedThorns  

<details>
<summary><b>Raw .gon</b></summary>

```
BleedThorns { 
    name "KEYWORD_BLEEDTHORNS_NAME"
    tooltip_stacks "KEYWORD_BLEEDTHORNS_DESC"

    tooltip_stackless "KEYWORD_BLEEDTHORNS_DESC_STACKLESS"
}
```

</details>

---

### `BlessingOfPeace`
**Name:** BlessingOfPeace  

<details>
<summary><b>Raw .gon</b></summary>

```
BlessingOfPeace {
    name "KEYWORD_BLESSINGOFPEACE_NAME"
    tooltip "KEYWORD_BLESSINGOFPEACE_DESC"

    tooltip_stackless "KEYWORD_BLESSINGOFPEACE_DESC_STACKLESS"
}
```

</details>

---

### `Blind`
**Name:** Blind  

<details>
<summary><b>Raw .gon</b></summary>

```
Blind {
    name "KEYWORD_BLIND_NAME"
    tooltip_stacks "KEYWORD_BLIND_DESC"
    tooltip_stacks_singular "KEYWORD_BLIND_DESC_STACKLESS"
    tooltip_stacks_neg "KEYWORD_PERMABLIND_DESC"
}
```

</details>

---

### `Bloodzerked`
**Name:** Bloodzerked  

<details>
<summary><b>Raw .gon</b></summary>

```
Bloodzerked {
    name "KEYWORD_BLOODZERK_NAME"
    tooltip_stacks "KEYWORD_BLOODZERK_DESC"
}
```

</details>

---

### `Blur`
**Name:** Blur  

| Field | Value |
| :--- | :--- |
| Alias | DodgeChance_Status |

<details>
<summary><b>Raw .gon</b></summary>

```
Blur {
    alias DodgeChance_Status
}
```

</details>

---

### `BodyGuard`
**Name:** BodyGuard  

<details>
<summary><b>Raw .gon</b></summary>

```
BodyGuard {
    name "KEYWORD_BODYGUARD_NAME"
    tooltip "KEYWORD_BODYGUARD_DESC"
}
```

</details>

---

### `BoostDamageAura`
**Name:** BoostDamageAura  

| Field | Value |
| :--- | :--- |
| Alias | DamageUp |

<details>
<summary><b>Raw .gon</b></summary>

```
BoostDamageAura {
    alias DamageUp
}
```

</details>

---

### `BoostDamageGlobalAura`
**Name:** BoostDamageGlobalAura  

| Field | Value |
| :--- | :--- |
| Alias | DamageUp |

<details>
<summary><b>Raw .gon</b></summary>

```
BoostDamageGlobalAura {
    alias DamageUp
}
```

</details>

---

### `Bounty`
**Name:** Bounty  

<details>
<summary><b>Raw .gon</b></summary>

```
Bounty {
    name "KEYWORD_BOUNTY_NAME"
    tooltip_stacks "KEYWORD_BOUNTY_DESC"
    tooltip_stackless "KEYWORD_BOUNTY_DESC_STACKLESS"
}
```

</details>

---

### `Brace`
**Name:** Brace  

<details>
<summary><b>Raw .gon</b></summary>

```
Brace {
    name "KEYWORD_BRACE_NAME"
    tooltip_stacks "KEYWORD_BRACE_DESC"
    tooltip_stackless "KEYWORD_BRACE_DESC_STACKLESS"
}
```

</details>

---

### `BraceForEachNeighboringEnemy`
**Name:** BraceForEachNeighboringEnemy  

| Field | Value |
| :--- | :--- |
| Alias | Brace |

<details>
<summary><b>Raw .gon</b></summary>

```
BraceForEachNeighboringEnemy {
    alias Brace
}
```

</details>

---

### `Bruise`
**Name:** Bruise  

<details>
<summary><b>Raw .gon</b></summary>

```
Bruise {
    name "KEYWORD_BRUISE_NAME"
    tooltip_stacks "KEYWORD_BRUISE_DESC"
    tooltip_stackless "KEYWORD_BRUISE_DESC_STACKLESS"
}
```

</details>

---

### `Burn`
**Name:** Burn  

<details>
<summary><b>Raw .gon</b></summary>

```
Burn {
    name "KEYWORD_BURN_NAME"
    tooltip_stacks "KEYWORD_BURN_DESC"
    tooltip_stackless "KEYWORD_BURN_DESC_STACKLESS"
}
```

</details>

---

### `ChampionUpgradeNextMinion`
**Name:** ChampionUpgradeNextMinion  

<details>
<summary><b>Raw .gon</b></summary>

```
ChampionUpgradeNextMinion {
    name "KEYWORD_PROMOTE_NAME"
    tooltip "KEYWORD_PROMOTE_DESC"
}
```

</details>

---

### `EliteUpgradeNextMinion`
**Name:** EliteUpgradeNextMinion  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteUpgradeNextMinion {
    name "KEYWORD_PROMOTE2_NAME"
    tooltip "KEYWORD_PROMOTE2_DESC"
}
```

</details>

---

### `Charge`
**Name:** Charge  

<details>
<summary><b>Raw .gon</b></summary>

```
Charge {
    name "KEYWORD_CHARGE_NAME"
    tooltip_stacks "KEYWORD_CHARGE_DESC"
    tooltip_stackless "KEYWORD_CHARGE_DESC_STACKLESS"
}
```

</details>

---

### `ChargeFists`
**Name:** ChargeFists  

<details>
<summary><b>Raw .gon</b></summary>

```
ChargeFists {
    name "KEYWORD_CHARGEFISTS_NAME"
    tooltip_stacks "KEYWORD_CHARGEFISTS_DESC"
    tooltip_stacks_singular "KEYWORD_CHARGEFISTS_DESC_SINGULAR"
    tooltip_stackless "KEYWORD_CHARGEFISTS_DESC_STACKLESS"
}
```

</details>

---

### `CharismaUp`
**Name:** CharismaUp  

<details>
<summary><b>Raw .gon</b></summary>

```
CharismaUp {
    name "KEYWORD_CHAUP_NAME"
    name_stacks_neg "KEYWORD_CHADOWN_NAME"
    tooltip_stacks_pos "KEYWORD_CHAUP_DESC"
    tooltip_stacks_neg "KEYWORD_CHADOWN_DESC"

    tooltip_stackless none 
}
```

</details>

---

### `CharmAllFlies`
**Name:** CharmAllFlies  

| Field | Value |
| :--- | :--- |
| Alias | Charmed |

<details>
<summary><b>Raw .gon</b></summary>

```
CharmAllFlies {
    alias Charmed
}
```

</details>

---

### `Charmed`
**Name:** Charmed  

<details>
<summary><b>Raw .gon</b></summary>

```
Charmed { 
    name "KEYWORD_CHARMED_NAME"
    tooltip "KEYWORD_CHARMED_DESC"

    tooltip_stackless "KEYWORD_CHARMED_DESC_STACKLESS"
}
```

</details>

---

### `Cleave`
**Name:** Cleave  

<details>
<summary><b>Raw .gon</b></summary>

```
Cleave {
    name "KEYWORD_CLEAVE_NAME"
    tooltip "KEYWORD_CLEAVE_DESC"

    icon_frame 152
}
```

</details>

---

### `ProbeCharmed`
**Name:** ProbeCharmed  

<details>
<summary><b>Raw .gon</b></summary>

```
ProbeCharmed { 
    name "KEYWORD_PROBED_NAME"
    tooltip "KEYWORD_PROBED_DESC" 

    tooltip_stackless "KEYWORD_PROBED_DESC_STACKLESS"
}
```

</details>

---

### `Confusion`
**Name:** Confusion  

<details>
<summary><b>Raw .gon</b></summary>

```
Confusion {
    name "KEYWORD_CONFUSION_NAME"
    tooltip_stacks "KEYWORD_CONFUSION_DESC"

    tooltip_stackless "KEYWORD_CONFUSION_DESC_STACKLESS"
}
```

</details>

---

### `PermanentConfusion`
**Name:** PermanentConfusion  

<details>
<summary><b>Raw .gon</b></summary>

```
PermanentConfusion {
    name "KEYWORD_CONFUSION_NAME"
    tooltip_stacks "KEYWORD_CONFUSION_DESC_STACKLESS"

    tooltip_stackless "KEYWORD_CONFUSION_DESC_STACKLESS"
}
```

</details>

---

### `ConstitutionUp`
**Name:** ConstitutionUp  

<details>
<summary><b>Raw .gon</b></summary>

```
ConstitutionUp {
    name "KEYWORD_CONUP_NAME"
    name_stacks_neg "KEYWORD_CONDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_CONUP_DESC"
    tooltip_stacks_neg "KEYWORD_CONDOWN_DESC"

    tooltip_stackless none 
}
```

</details>

---

### `CounterNextAttacks`
**Name:** CounterNextAttacks  

<details>
<summary><b>Raw .gon</b></summary>

```
CounterNextAttacks {
    name "KEYWORD_COUNTER_NAME"
    tooltip_stacks_singular "KEYWORD_COUNTER_DESC"
    tooltip_stacks "KEYWORD_COUNTER_DESC_STACKS"
}
```

</details>

---

### `CritChanceUp`
**Name:** CritChanceUp  

<details>
<summary><b>Raw .gon</b></summary>

```
CritChanceUp {
    name "KEYWORD_CRITCHANCE_NAME"
    tooltip_stacks "KEYWORD_CRITCHANCE_DESC"

    tooltip_stackless none 
}
```

</details>

---

### `DamageReductionAura`
**Name:** DamageReductionAura  

| Field | Value |
| :--- | :--- |
| Alias | Brace |

<details>
<summary><b>Raw .gon</b></summary>

```
DamageReductionAura {
    alias Brace
}
```

</details>

---

### `DamageUp`
**Name:** DamageUp  

<details>
<summary><b>Raw .gon</b></summary>

```
DamageUp {
    name "KEYWORD_DAMAGEUP_NAME"
    name_stacks_neg "KEYWORD_DAMAGEDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_DAMAGEUP_DESC"
    tooltip_stacks_neg "KEYWORD_DAMAGEDOWN_DESC"

    tooltip_stackless_pos "KEYWORD_DAMAGEUP_DESC_STACKLESS"
    tooltip_stackless_neg "KEYWORD_DAMAGEDOWN_DESC_STACKLESS"
}
```

</details>

---

### `DelayedStatusApplication`
**Name:** DelayedStatusApplication  

<details>
<summary><b>Raw .gon</b></summary>

```
DelayedStatusApplication {
    name "KEYWORD_DELAYEDSTATUS_NAME"
    tooltip "KEYWORD_DELAYEDSTATUS_DESC"
}
```

</details>

---

### `DelayedPain`
**Name:** DelayedPain  

<details>
<summary><b>Raw .gon</b></summary>

```
DelayedPain {
    name "KEYWORD_DELAYEDPAIN_NAME"
    tooltip_stacks "KEYWORD_DELAYEDPAIN_DESC"

    tooltip_stackless "KEYWORD_DELAYEDPAIN_DESC_STACKLESS"
}
```

</details>

---

### `DexterityUp`
**Name:** DexterityUp  

<details>
<summary><b>Raw .gon</b></summary>

```
DexterityUp {
    name "KEYWORD_DEXUP_NAME"
    name_stacks_neg "KEYWORD_DEXDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_DEXUP_DESC"
    tooltip_stacks_neg "KEYWORD_DEXDOWN_DESC"

    tooltip_stackless none 
}
```

</details>

---

### `DiminishingHealthRegen`
**Name:** DiminishingHealthRegen  

<details>
<summary><b>Raw .gon</b></summary>

```
DiminishingHealthRegen {
    name "KEYWORD_DIMINISHREGEN_NAME"
    tooltip_stacks "KEYWORD_DIMINISHREGEN_DESC"

    tooltip_stackless "KEYWORD_DIMINISHREGEN_DESC_STACKLESS"
}
```

</details>

---

### `DivineShield`
**Name:** DivineShield  

<details>
<summary><b>Raw .gon</b></summary>

```
DivineShield {
    name "KEYWORD_DIVINESHIELD_NAME"
    tooltip "KEYWORD_DIVINESHIELD_DESC"

    icon_frame 141
}
```

</details>

---

### `divine_shield`
**Name:** divine_shield  

| Field | Value |
| :--- | :--- |
| Alias | DivineShield |

<details>
<summary><b>Raw .gon</b></summary>

```
divine_shield {
    alias DivineShield
}
```

</details>

---

### `NonStackingDivineShield`
**Name:** NonStackingDivineShield  

| Field | Value |
| :--- | :--- |
| Alias | DivineShield |

<details>
<summary><b>Raw .gon</b></summary>

```
NonStackingDivineShield {
    alias DivineShield
}
```

</details>

---

### `Dodge`
**Name:** Dodge  

<details>
<summary><b>Raw .gon</b></summary>

```
Dodge { 
    name "KEYWORD_DODGE_NAME"
    tooltip_stacks "KEYWORD_DODGE_DESC"

    tooltip_stackless "KEYWORD_DODGE_DESC_STACKLESS"
}
```

</details>

---

### `DodgeChance_Status`
**Name:** DodgeChance_Status  

<details>
<summary><b>Raw .gon</b></summary>

```
DodgeChance_Status {
    name "KEYWORD_DODGECHANCE_NAME"
    tooltip_stacks "KEYWORD_DODGECHANCE_DESC"

    tooltip_stackless none 
}
```

</details>

---

### `Doomed`
**Name:** Doomed  

<details>
<summary><b>Raw .gon</b></summary>

```
Doomed {
    name "KEYWORD_DOOMED_NAME"
    tooltip "KEYWORD_DOOMED_DESC" 
}
```

</details>

---

### `DoubleCast`
**Name:** DoubleCast  

<details>
<summary><b>Raw .gon</b></summary>

```
DoubleCast { 
    name "KEYWORD_DOUBLECAST_NAME"
    tooltip "KEYWORD_DOUBLECAST_DESC"
}
```

</details>

---

### `DoubleCastSpell`
**Name:** DoubleCastSpell  

<details>
<summary><b>Raw .gon</b></summary>

```
DoubleCastSpell {
    name "KEYWORD_DOUBLECASTSPELL_NAME"
    tooltip "KEYWORD_DOUBLECASTSPELL_DESC"
}
```

</details>

---

### `DoubleCastSpellThisTurn`
**Name:** DoubleCastSpellThisTurn  

<details>
<summary><b>Raw .gon</b></summary>

```
DoubleCastSpellThisTurn {
    name "KEYWORD_DOUBLECASTTHISTURN_NAME"
    tooltip "KEYWORD_DOUBLECASTTHISTURN_DESC"
}
```

</details>

---

### `DoubleLoot`
**Name:** DoubleLoot  

<details>
<summary><b>Raw .gon</b></summary>

```
DoubleLoot { 
    name "Double Loot"
    tooltip "The next pickup you collect does double its effects"
}
```

</details>

---

### `Drowsy`
**Name:** Drowsy  

<details>
<summary><b>Raw .gon</b></summary>

```
Drowsy {
    name "KEYWORD_DROWSY_NAME"
    tooltip "KEYWORD_DROWSY_DESC"
}
```

</details>

---

### `DybbukPossessed`
**Name:** DybbukPossessed  

<details>
<summary><b>Raw .gon</b></summary>

```
DybbukPossessed {
    name "KEYWORD_DYBBUKED_NAME"
    tooltip "KEYWORD_DYBBUKED_DESC"
}
```

</details>

---

### `EmptyMind`
**Name:** EmptyMind  

<details>
<summary><b>Raw .gon</b></summary>

```
EmptyMind {
    name "KEYWORD_EMPTYMIND_NAME"
    tooltip "KEYWORD_EMPTYMIND_DESC"
}
```

</details>

---

### `Enrage`
**Name:** Enrage  

<details>
<summary><b>Raw .gon</b></summary>

```
Enrage { 
    name "Enrage"
    tooltip None
}
```

</details>

---

### `EventBounty`
**Name:** EventBounty  

<details>
<summary><b>Raw .gon</b></summary>

```
EventBounty {
    name "KEYWORD_EVENTBOUNTY_NAME"
    tooltip_stacks "KEYWORD_EVENTBOUNTY_DESC"
}
```

</details>

---

### `Exhaustion`
**Name:** Exhaustion  

<details>
<summary><b>Raw .gon</b></summary>

```
Exhaustion {
    name "KEYWORD_EXHAUSTION_NAME"
    tooltip_stacks "KEYWORD_EXHAUSTION_DESC"
    tooltip_stackless "KEYWORD_EXHAUSTION_DESC_STACKLESS"
}
```

</details>

---

### `ExtraBasicAttacks_Status`
**Name:** ExtraBasicAttacks_Status  

<details>
<summary><b>Raw .gon</b></summary>

```
ExtraBasicAttacks_Status {
    name "KEYWORD_EXTRAATTACK_NAME"
    tooltip_stacks "KEYWORD_EXTRAATTACK_DESC"
    tooltip_stackless none 
}
```

</details>

---

### `ExtraBasicMoves_Status`
**Name:** ExtraBasicMoves_Status  

<details>
<summary><b>Raw .gon</b></summary>

```
ExtraBasicMoves_Status {
    name "KEYWORD_EXTRAMOVE_NAME"
    tooltip_stacks "KEYWORD_EXTRAMOVE_DESC"
    tooltip_stackless none 
}
```

</details>

---

### `Fear`
**Name:** Fear  

<details>
<summary><b>Raw .gon</b></summary>

```
Fear {
    name "KEYWORD_FEAR_NAME"
    tooltip "KEYWORD_FEAR_DESC"
}
```

</details>

---

### `FireArmor`
**Name:** FireArmor  

<details>
<summary><b>Raw .gon</b></summary>

```
FireArmor { 
    name "FireArmor"
    tooltip None
}
```

</details>

---

### `FireArmor2`
**Name:** FireArmor2  

<details>
<summary><b>Raw .gon</b></summary>

```
FireArmor2 { 
    name "FireArmor2"
    tooltip None
}
```

</details>

---

### `FlyDamageIncrease`
**Name:** FlyDamageIncrease  

| Field | Value |
| :--- | :--- |
| Alias | DamageUp |

<details>
<summary><b>Raw .gon</b></summary>

```
FlyDamageIncrease {
    alias DamageUp
}
```

</details>

---

### `FreeSpell`
**Name:** FreeSpell  

<details>
<summary><b>Raw .gon</b></summary>

```
FreeSpell { 
    name "KEYWORD_FREESPELL_NAME"
    tooltip "KEYWORD_FREESPELL_DESC"
}
```

</details>

---

### `Freeze`
**Name:** Freeze  

<details>
<summary><b>Raw .gon</b></summary>

```
Freeze {
    name "KEYWORD_FREEZE_NAME"
    tooltip "KEYWORD_FREEZE_DESC"
}
```

</details>

---

### `GlobalFamiliarDamageBoost`
**Name:** GlobalFamiliarDamageBoost  

| Field | Value |
| :--- | :--- |
| Alias | DamageUp |

<details>
<summary><b>Raw .gon</b></summary>

```
GlobalFamiliarDamageBoost {
    alias DamageUp
}
```

</details>

---

### `GlobalFamiliarMoveBoost`
**Name:** GlobalFamiliarMoveBoost  

| Field | Value |
| :--- | :--- |
| Alias | MovementUp |

<details>
<summary><b>Raw .gon</b></summary>

```
GlobalFamiliarMoveBoost {
    alias MovementUp
}
```

</details>

---

### `Grappled`
**Name:** Grappled  

<details>
<summary><b>Raw .gon</b></summary>

```
Grappled {
    name "KEYWORD_GRAPPLED_NAME"
    tooltip "KEYWORD_GRAPPLED_DESC"
}
```

</details>

---

### `HealthRegenUp`
**Name:** HealthRegenUp  

<details>
<summary><b>Raw .gon</b></summary>

```
HealthRegenUp {
    name "KEYWORD_HEALTHREGEN_NAME"
    tooltip_stacks "KEYWORD_HEALTHREGEN_DESC"
    tooltip_stackless "KEYWORD_HEALTHREGEN_DESC_STACKLESS"
}
```

</details>

---

### `HeatWave`
**Name:** HeatWave  

<details>
<summary><b>Raw .gon</b></summary>

```
HeatWave {
    name "KEYWORD_DEHYDRATED_NAME"
    tooltip "KEYWORD_DEHYDRATED_DESC"
}
```

</details>

---

### `HeavierHits`
**Name:** HeavierHits  

<details>
<summary><b>Raw .gon</b></summary>

```
HeavierHits {
    name "KEYWORD_HEAVIERHITS_NAME"
    tooltip_stacks "KEYWORD_HEAVIERHITS_DESC_STACKS"
    tooltip_stackless none
}
```

</details>

---

### `HeavyHits`
**Name:** HeavyHits  

<details>
<summary><b>Raw .gon</b></summary>

```
HeavyHits {
    name "KEYWORD_HEAVYHITS_NAME"
    tooltip_stacks "KEYWORD_HEAVYHITS_DESC_STACKS"
    tooltip_stackless none
}
```

</details>

---

### `Hex`
**Name:** Hex  

<details>
<summary><b>Raw .gon</b></summary>

```
Hex {
    name "KEYWORD_HEX_NAME"
    tooltip_stacks "KEYWORD_HEX_DESC"

    tooltip_stackless "KEYWORD_HEX_DESC_STACKLESS"
}
```

</details>

---

### `IceArmor`
**Name:** IceArmor  

<details>
<summary><b>Raw .gon</b></summary>

```
IceArmor { 
    name "IceArmor"
    tooltip None
}
```

</details>

---

### `ImbueBleed`
**Name:** ImbueBleed  

<details>
<summary><b>Raw .gon</b></summary>

```
ImbueBleed { 
    name "ImbueBleed"
    tooltip_stacks "Next physical attack inflicts Bleed {stacks}"
    tooltip_stackless "Next physical attack inflicts Bleed"
}
```

</details>

---

### `ImbueKnockOutCoin`
**Name:** ImbueKnockOutCoin  

<details>
<summary><b>Raw .gon</b></summary>

```
ImbueKnockOutCoin { 
    name "ImbueKnockOutCoin"
    tooltip None
}
```

</details>

---

### `ImbueManaLeech`
**Name:** ImbueManaLeech  

<details>
<summary><b>Raw .gon</b></summary>

```
ImbueManaLeech { 
    name "ImbueManaLeech"
    tooltip None
}
```

</details>

---

### `ImbuePoison`
**Name:** ImbuePoison  

<details>
<summary><b>Raw .gon</b></summary>

```
ImbuePoison { 
    name "ImbuePoison"
    tooltip None
}
```

</details>

---

### `ImbueRandomStatDown`
**Name:** ImbueRandomStatDown  

<details>
<summary><b>Raw .gon</b></summary>

```
ImbueRandomStatDown { 
    name "ImbueRandomStatDown"
    tooltip None
}
```

</details>

---

### `ImbueWeakness`
**Name:** ImbueWeakness  

<details>
<summary><b>Raw .gon</b></summary>

```
ImbueWeakness { 
    name "ImbueWeakness"
    tooltip None
}
```

</details>

---

### `Immobile`
**Name:** Immobile  

<details>
<summary><b>Raw .gon</b></summary>

```
Immobile {
    name "KEYWORD_IMMOBILE_NAME"
    tooltip "KEYWORD_IMMOBILE_DESC"
}
```

</details>

---

### `Infested`
**Name:** Infested  

<details>
<summary><b>Raw .gon</b></summary>

```
Infested {
    name "KEYWORD_INFESTED_NAME"
    tooltip "KEYWORD_INFESTED_DESC"
}
```

</details>

---

### `IntelligenceUp`
**Name:** IntelligenceUp  

<details>
<summary><b>Raw .gon</b></summary>

```
IntelligenceUp {
    name "KEYWORD_INTUP_NAME"
    name_stacks_neg "KEYWORD_INTDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_INTUP_DESC"
    tooltip_stacks_neg "KEYWORD_INTDOWN_DESC"

    tooltip_stackless none 
}
```

</details>

---

### `Invulnerable`
**Name:** Invulnerable  

<details>
<summary><b>Raw .gon</b></summary>

```
Invulnerable {
    name "KEYWORD_INVULNERABLE_NAME"
    tooltip "KEYWORD_INVULNERABLE_DESC"
}
```

</details>

---

### `KineticSpikes`
**Name:** KineticSpikes  

<details>
<summary><b>Raw .gon</b></summary>

```
KineticSpikes {
    name "KEYWORD_KINETICSPPIKES_NAME"
    tooltip_stacks "KEYWORD_KINETICSPPIKES_DESC"
    tooltip_stacks_singular "KEYWORD_KINETICSPPIKES_DESC_SINGULAR"
    tooltip_stackless "KEYWORD_KINETICSPPIKES_DESC_STACKLESS"
}
```

</details>

---

### `Knockback`
**Name:** Knockback  

<details>
<summary><b>Raw .gon</b></summary>

```
Knockback { 
    name "Knockback"
    tooltip None
}
```

</details>

---

### `LateBloomer`
**Name:** LateBloomer  

<details>
<summary><b>Raw .gon</b></summary>

```
LateBloomer {
    name "KEYWORD_LATEBLOOMER_NAME"
    tooltip_stacks "KEYWORD_LATEBLOOMER_DESC"
    tooltip_stacks_singular "KEYWORD_LATEBLOOMER_SINGULAR_DESC"

    tooltip_stackless none
}
```

</details>

---

### `Leeches`
**Name:** Leeches  

<details>
<summary><b>Raw .gon</b></summary>

```
Leeches {
    name "KEYWORD_LEECHES_NAME"
    name_reference_applier "KEYWORD_LEECHES_NAME_APPLIER"
    tooltip_stacks "KEYWORD_LEECHES_DESC"
    tooltip_reference_applier "KEYWORD_LEECHES_DESC_APPLIER"

    tooltip_stackless "KEYWORD_LEECHES_DESC_STACKLESS"
}
```

</details>

---

### `Lifesteal`
**Name:** Lifesteal  

<details>
<summary><b>Raw .gon</b></summary>

```
Lifesteal {
    name "KEYWORD_LIFESTEAL_NAME"
    tooltip_stacks "KEYWORD_LIFESTEAL_DESC"

    tooltip_stackless "KEYWORD_LIFESTEAL_DESC_STACKLESS"
}
```

</details>

---

### `Leech`
**Name:** Leech  

<details>
<summary><b>Raw .gon</b></summary>

```
Leech {
    name "KEYWORD_LIFESTEAL_NAME"
    tooltip "KEYWORD_LIFESTEAL2_DESC"

    icon_frame 17
}
```

</details>

---

### `LoseShieldNextTurn`
**Name:** LoseShieldNextTurn  

<details>
<summary><b>Raw .gon</b></summary>

```
LoseShieldNextTurn { 
    name "LoseShieldNextTurn"
    tooltip None
}
```

</details>

---

### `LuckUp`
**Name:** LuckUp  

<details>
<summary><b>Raw .gon</b></summary>

```
LuckUp {
    name "KEYWORD_LCKUP_NAME"
    name_stacks_neg "KEYWORD_LCKDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_LCKUP_DESC"
    tooltip_stacks_neg "KEYWORD_LCKDOWN_DESC"

    tooltip_stackless none 
}
```

</details>

---

### `Madness`
**Name:** Madness  

<details>
<summary><b>Raw .gon</b></summary>

```
Madness {
    name "KEYWORD_MADNESS_NAME"
    tooltip "KEYWORD_MADNESS_DESC"
}
```

</details>

---

### `MagicWeakness`
**Name:** MagicWeakness  

<details>
<summary><b>Raw .gon</b></summary>

```
MagicWeakness {
    name "KEYWORD_MAGICWEAKNESS_NAME"
    tooltip "KEYWORD_MAGICWEAKNESS_DESC"
}
```

</details>

---

### `ManaLeeches`
**Name:** ManaLeeches  

<details>
<summary><b>Raw .gon</b></summary>

```
ManaLeeches {
    name "KEYWORD_MANALEECHES_NAME"
    name_reference_applier "KEYWORD_MANALEECHES_NAME_APPLIER"
    tooltip_stacks "KEYWORD_MANALEECHES_DESC"
    tooltip_reference_applier "KEYWORD_MANALEECHES_DESC_APPLIER"

    tooltip_stackless "KEYWORD_MANALEECHES_DESC_STACKLESS"
}
```

</details>

---

### `Marked`
**Name:** Marked  

<details>
<summary><b>Raw .gon</b></summary>

```
Marked {
    name "KEYWORD_MARKED_NAME"
    tooltip "KEYWORD_MARKED_DESC"
}
```

</details>

---

### `Meaty`
**Name:** Meaty  

<details>
<summary><b>Raw .gon</b></summary>

```
Meaty {
    name "KEYWORD_MEATY_NAME"
    tooltip "KEYWORD_MEATY_DESC"
}
```

</details>

---

### `MissChance`
**Name:** MissChance  

<details>
<summary><b>Raw .gon</b></summary>

```
MissChance {
    name "KEYWORD_MISSCHANCE_NAME"
    tooltip_stacks "KEYWORD_MISSCHANCE_DESC"
    tooltip_stackless none 
}
```

</details>

---

### `MovementUp`
**Name:** MovementUp  

<details>
<summary><b>Raw .gon</b></summary>

```
MovementUp {
    name "KEYWORD_MOVEMENTUP_NAME"
    name_stacks_neg "KEYWORD_MOVEMENTDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_MOVEMENTUP_DESC"
    tooltip_stacks_neg "KEYWORD_MOVEMENTDOWN_DESC"

    tooltip_stackless_pos "KEYWORD_MOVEMENTUP_DESC_STACKLESS"
    tooltip_stackless_neg "KEYWORD_MOVEMENTDOWN_DESC_STACKLESS"
}
```

</details>

---

### `MoveQuivered`
**Name:** MoveQuivered  

<details>
<summary><b>Raw .gon</b></summary>

```
MoveQuivered {
    name "KEYWORD_BONUSMOVE_NAME"
    tooltip_stacks_singular "KEYWORD_BONUSMOVE_DESC"
    tooltip_stacks "KEYWORD_BONUSMOVE_DESC_STACKS"
}
```

</details>

---

### `MutateAfterXTurns`
**Name:** MutateAfterXTurns  

| Field | Value |
| :--- | :--- |
| Alias | TransformInXTurns |

<details>
<summary><b>Raw .gon</b></summary>

```
MutateAfterXTurns {
    alias TransformInXTurns
}
```

</details>

---

### `Muted`
**Name:** Muted  

<details>
<summary><b>Raw .gon</b></summary>

```
Muted { 
    name "KEYWORD_MUTED_NAME"
    tooltip_stacks_singular "KEYWORD_MUTED_DESC_SINGULAR"
    tooltip_stacks "KEYWORD_MUTED_DESC"

    tooltip_stackless "KEYWORD_MUTED_DESC_STACKLESS"
}
```

</details>

---

### `NextAbilityHeals`
**Name:** NextAbilityHeals  

<details>
<summary><b>Raw .gon</b></summary>

```
NextAbilityHeals { 
    name "NextAbilityHeals"
    tooltip None
}
```

</details>

---

### `NextAbilityIncreaseRange`
**Name:** NextAbilityIncreaseRange  

<details>
<summary><b>Raw .gon</b></summary>

```
NextAbilityIncreaseRange { 
    name "NextAbilityIncreaseRange"
    tooltip None
}
```

</details>

---

### `NextActionLuckUp`
**Name:** NextActionLuckUp  

| Field | Value |
| :--- | :--- |
| Alias | LuckUp |

<details>
<summary><b>Raw .gon</b></summary>

```
NextActionLuckUp {
    alias LuckUp
}
```

</details>

---

### `NextAttackBonusRange`
**Name:** NextAttackBonusRange  

<details>
<summary><b>Raw .gon</b></summary>

```
NextAttackBonusRange {
    name "KEYWORD_BONUSRANGE_NAME"
    tooltip_stacks "KEYWORD_BONUSRANGE_DESC"
    tooltip_stackless "KEYWORD_BONUSRANGE_DESC_STACKLESS"
}
```

</details>

---

### `NextDamageReduceAndHealAllies`
**Name:** NextDamageReduceAndHealAllies  

<details>
<summary><b>Raw .gon</b></summary>

```
NextDamageReduceAndHealAllies { 
    name "NextDamageReduceAndHealAllies"
    tooltip None
}
```

</details>

---

### `NextDamageReduceAndPushback`
**Name:** NextDamageReduceAndPushback  

<details>
<summary><b>Raw .gon</b></summary>

```
NextDamageReduceAndPushback { 
    name "NextDamageReduceAndPushback"
    tooltip None
}
```

</details>

---

### `NextDamageReduceThisTurn`
**Name:** NextDamageReduceThisTurn  

<details>
<summary><b>Raw .gon</b></summary>

```
NextDamageReduceThisTurn { 
    name "NextDamageReduceThisTurn"
    tooltip None
}
```

</details>

---

### `NextMoveRangeIncrease`
**Name:** NextMoveRangeIncrease  

<details>
<summary><b>Raw .gon</b></summary>

```
NextMoveRangeIncrease { 
    name "NextMoveRangeIncrease"
    tooltip None
}
```

</details>

---

### `NextSpellHealEqualToMana`
**Name:** NextSpellHealEqualToMana  

<details>
<summary><b>Raw .gon</b></summary>

```
NextSpellHealEqualToMana { 
    name "NextSpellHealEqualToMana"
    tooltip None
}
```

</details>

---

### `NextTurnDoubleRangedDamage`
**Name:** NextTurnDoubleRangedDamage  

<details>
<summary><b>Raw .gon</b></summary>

```
NextTurnDoubleRangedDamage { 
    name "KEYWORD_DOUBLERANGEDDMG_NAME"
    tooltip "KEYWORD_DOUBLERANGEDDMG_DESC"
}
```

</details>

---

### `NoHealthRegen`
**Name:** NoHealthRegen  

<details>
<summary><b>Raw .gon</b></summary>

```
NoHealthRegen {
    name "KEYWORD_NOHEALTHREGEN_NAME"
    tooltip "KEYWORD_NOHEALTHREGEN_DESC"
}
```

</details>

---

### `NoManaRegen`
**Name:** NoManaRegen  

<details>
<summary><b>Raw .gon</b></summary>

```
NoManaRegen {
    name "KEYWORD_NOMANAREGEN_NAME"
    tooltip "KEYWORD_NOMANAREGEN_DESC"
}
```

</details>

---

### `OldStealth`
**Name:** OldStealth  

<details>
<summary><b>Raw .gon</b></summary>

```
OldStealth { 
    name "OldStealth"
    tooltip None
}
```

</details>

---

### `OneUseSpellDamageUp`
**Name:** OneUseSpellDamageUp  

| Field | Value |
| :--- | :--- |
| Alias | SpellDamageUp |

<details>
<summary><b>Raw .gon</b></summary>

```
OneUseSpellDamageUp {
    alias SpellDamageUp
}
```

</details>

---

### `Ostracized`
**Name:** Ostracized  

<details>
<summary><b>Raw .gon</b></summary>

```
Ostracized {
    name "KEYWORD_OSTRACIZED_NAME"
    tooltip "KEYWORD_OSTRACIZED_DESC"
}
```

</details>

---

### `PassiveBrace`
**Name:** PassiveBrace  

| Field | Value |
| :--- | :--- |
| Alias | Brace |

<details>
<summary><b>Raw .gon</b></summary>

```
PassiveBrace {
    alias Brace
}
```

</details>

---

### `PermanentCharm`
**Name:** PermanentCharm  

| Field | Value |
| :--- | :--- |
| Alias | Charmed |

<details>
<summary><b>Raw .gon</b></summary>

```
PermanentCharm {
    alias Charmed
}
```

</details>

---

### `CapturedFamiliarIcon`
**Name:** CapturedFamiliarIcon  

<details>
<summary><b>Raw .gon</b></summary>

```
CapturedFamiliarIcon {
    name "KEYWORD_CAPTUREDFAMILIAR_NAME"
    tooltip "KEYWORD_CAPTUREDFAMILIAR_DESC"
}
```

</details>

---

### `PermanentImmobile`
**Name:** PermanentImmobile  

| Field | Value |
| :--- | :--- |
| Alias | Immobile |

<details>
<summary><b>Raw .gon</b></summary>

```
PermanentImmobile {
    alias Immobile
}
```

</details>

---

### `PermanentMadness`
**Name:** PermanentMadness  

| Field | Value |
| :--- | :--- |
| Alias | Madness |

<details>
<summary><b>Raw .gon</b></summary>

```
PermanentMadness {
    alias Madness
}
```

</details>

---

### `Petrify`
**Name:** Petrify  

<details>
<summary><b>Raw .gon</b></summary>

```
Petrify {
    name "KEYWORD_PETRIFY_NAME"
    tooltip_stacks "KEYWORD_PETRIFY_DESC"
    tooltip_stacks_singular KEYWORD_PETRIFY_DESC_SINGULAR
    tooltip_stackless "KEYWORD_PETRIFY_DESC_STACKLESS"
}
```

</details>

---

### `Poison`
**Name:** Poison  

<details>
<summary><b>Raw .gon</b></summary>

```
Poison {
    name "KEYWORD_POISON_NAME"
    tooltip_stacks "KEYWORD_POISON_DESC"
    tooltip_stackless "KEYWORD_POISON_DESC_STACKLESS"
}
```

</details>

---

### `PoisonLace`
**Name:** PoisonLace  

<details>
<summary><b>Raw .gon</b></summary>

```
PoisonLace {
    name "KEYWORD_POISONLACE_NAME"
    tooltip_stacks "KEYWORD_POISONLACE_DESC"
    tooltip_stackless "KEYWORD_POISONLACE_DESC_STACKLESS"
}
```

</details>

---

### `CurrentWeaponAddPoison`
**Name:** CurrentWeaponAddPoison  

<details>
<summary><b>Raw .gon</b></summary>

```
CurrentWeaponAddPoison {
    name "KEYWORD_WPOISONLACE_NAME"
    tooltip_stacks "KEYWORD_WPOISONLACE_DESC"
    tooltip_stackless "KEYWORD_WPOISONLACE_DESC_STACKLESS"
}
```

</details>

---

### `PoisonThorns`
**Name:** PoisonThorns  

<details>
<summary><b>Raw .gon</b></summary>

```
PoisonThorns {
    name "KEYWORD_POISONOUS_NAME"
    tooltip_stacks "KEYWORD_POISONOUS_DESC"
    tooltip_stackless "KEYWORD_POISONOUS_DESC_STACKLESS"
}
```

</details>

---

### `Possessed`
**Name:** Possessed  

<details>
<summary><b>Raw .gon</b></summary>

```
Possessed {
    name "KEYWORD_POSSESED_NAME"
    tooltip_stacks "KEYWORD_POSSESSED_DESC"
    tooltip_stacks_singular KEYWORD_POSSESSED_DESC_SIGNULAR
    tooltip_stackless "KEYWORD_POSSESSED_DESC_STACKLESS"
}
```

</details>

---

### `PreEmptiveCounterNextAttacks`
**Name:** PreEmptiveCounterNextAttacks  

<details>
<summary><b>Raw .gon</b></summary>

```
PreEmptiveCounterNextAttacks {
    name "KEYWORD_PREEMTIVECOUNTER_NAME"
    tooltip_stacks "KEYWORD_PREEMTIVECOUNTER_DESC"
    tooltip_stacks_singular "KEYWORD_PREEMTIVECOUNTER_DESC_STACKLESS"
    tooltip_stackless "KEYWORD_PREEMTIVECOUNTER_DESC_STACKLESS"
}
```

</details>

---

### `Quivered`
**Name:** Quivered  

<details>
<summary><b>Raw .gon</b></summary>

```
Quivered {
    name "KEYWORD_QUIVERED_NAME"
    tooltip_stacks_singular "KEYWORD_QUIVERED_DESC_STACKLESS"
    tooltip_stacks "KEYWORD_QUIVERED_DESC"
}
```

</details>

---

### `RandomInjury`
**Name:** RandomInjury  

<details>
<summary><b>Raw .gon</b></summary>

```
RandomInjury {
    name "KEYWORD_RANDOMINJURY_NAME"
    tooltip "KEYWORD_RANDOMINJURY_DESC"

    icon_frame 58
}
```

</details>

---

### `HealRandomInjury`
**Name:** HealRandomInjury  

<details>
<summary><b>Raw .gon</b></summary>

```
HealRandomInjury {
    name "KEYWORD_HEALRANDOMINJURY_NAME"
    tooltip "KEYWORD_HEALRANDOMINJURY_DESC"

    icon_frame 158
}
```

</details>

---

### `RandomMagicMissile`
**Name:** RandomMagicMissile  

<details>
<summary><b>Raw .gon</b></summary>

```
RandomMagicMissile {
    name "KEYWORD_SPARKLE_NAME"
    tooltip "KEYWORD_SPARKLE_DESC"

    icon_frame 154
}
```

</details>

---

### `RangeUp`
**Name:** RangeUp  

<details>
<summary><b>Raw .gon</b></summary>

```
RangeUp {
    name "KEYWORD_RANGEUP_NAME"
    tooltip_stacks "KEYWORD_RANGEUP_DESC"
    tooltip_stackless "KEYWORD_RANGEUP_DESC_STACKLESS"
}
```

</details>

---

### `TempBonusKnockback`
**Name:** TempBonusKnockback  

<details>
<summary><b>Raw .gon</b></summary>

```
TempBonusKnockback {
    name "KEYWORD_BONUSKNOCKBACK_NAME"
    tooltip_stacks "KEYWORD_BONUSKNOCKBACK_DESC"
    tooltip_stackless None
}
```

</details>

---

### `TempBonusKnockbackDamage`
**Name:** TempBonusKnockbackDamage  

<details>
<summary><b>Raw .gon</b></summary>

```
TempBonusKnockbackDamage {
    name "KEYWORD_BONUSKNOCKBACKDAMAGE_NAME"
    tooltip_stacks "KEYWORD_BONUSKNOCKBACKDAMAGE_DESC"
    tooltip_stackless None
}
```

</details>

---

### `TemporaryItem`
**Name:** TemporaryItem  

<details>
<summary><b>Raw .gon</b></summary>

```
TemporaryItem {
    name "KEYWORD_TEMPITEM_NAME"
    tooltip "KEYWORD_TEMPITEM_DESC"

    icon_frame 164
}
```

</details>

---

### `TempRangeUp`
**Name:** TempRangeUp  

<details>
<summary><b>Raw .gon</b></summary>

```
TempRangeUp {
    name "KEYWORD_TEMPRANGE_NAME"
    tooltip_stacks "KEYWORD_TEMPRANGE_DESC"
    tooltip_stackless "KEYWORD_TEMPRANGE_DESC_STACKLESS"
}
```

</details>

---

### `Reduce`
**Name:** Reduce  

<details>
<summary><b>Raw .gon</b></summary>

```
Reduce { 
    name "Reduce"
    tooltip None
}
```

</details>

---

### `ReduceManaCost`
**Name:** ReduceManaCost  

<details>
<summary><b>Raw .gon</b></summary>

```
ReduceManaCost {
    name "KEYWORD_REDUCEMANACOST_NAME"
    tooltip_stacks "KEYWORD_REDUCEMANACOST_DESC"
    tooltip_stackless "KEYWORD_REDUCEMANACOST_DESC_STACKLESS"
}
```

</details>

---

### `ReduceManaCostExcludeBrainstorm`
**Name:** ReduceManaCostExcludeBrainstorm  

<details>
<summary><b>Raw .gon</b></summary>

```
ReduceManaCostExcludeBrainstorm {
    name "KEYWORD_INSIGHT_NAME"
    tooltip_stacks "KEYWORD_INSIGHT_DESC"
    tooltip_stackless "KEYWORD_INSIGHT_DESC_STACKLESS"
}
```

</details>

---

### `Reflect`
**Name:** Reflect  

<details>
<summary><b>Raw .gon</b></summary>

```
Reflect {
    name "KEYWORD_REFLECT_NAME"
    tooltip_stacks "KEYWORD_REFLECT_DESC"
    tooltip_stacks_singular "KEYWORD_REFLECT_DESC_STACKLESS"
}
```

</details>

---

### `ReviveNextRound`
**Name:** ReviveNextRound  

<details>
<summary><b>Raw .gon</b></summary>

```
ReviveNextRound {
    name "KEYWORD_AUTOREVIVE_NAME"
    tooltip_stacks_singular "KEYWORD_AUTOREVIVE_DESC_SINGULAR"
    tooltip_stacks "KEYWORD_AUTOREVIVE_DESC"
    tooltip_stackless KEYWORD_AUTOREVIVE_DESC
}
```

</details>

---

### `Robot`
**Name:** Robot  

<details>
<summary><b>Raw .gon</b></summary>

```
Robot { 
    name "KEYWORD_ENERGIZED_NAME"
    tooltip "KEYWORD_ENERGIZED_DESC"
    tooltip_stackless none
}
```

</details>

---

### `Rot`
**Name:** Rot  

<details>
<summary><b>Raw .gon</b></summary>

```
Rot { 
    name "KEYWORD_ROT_NAME"
    tooltip "KEYWORD_ROT_DESC"
}
```

</details>

---

### `SafeDoomed`
**Name:** SafeDoomed  

<details>
<summary><b>Raw .gon</b></summary>

```
SafeDoomed {
    name "KEYWORD_SAFEDOOMED_NAME"
    tooltip "KEYWORD_SAFEDOOMED_DESC"
}
```

</details>

---

### `Scrambled`
**Name:** Scrambled  

<details>
<summary><b>Raw .gon</b></summary>

```
Scrambled { 
    name "KEYWORD_SCRAMBLED_NAME"
    tooltip "KEYWORD_SCRAMBLED_DESC"
}
```

</details>

---

### `SerratedClaws`
**Name:** SerratedClaws  

<details>
<summary><b>Raw .gon</b></summary>

```
SerratedClaws {
    name "KEYWORD_SERRATED_NAME"
    tooltip_stacks "KEYWORD_SERRATED_DESC"
    tooltip_stackless "KEYWORD_SERRATED_DESC_STACKLESS"
}
```

</details>

---

### `Shield`
**Name:** Shield  

<details>
<summary><b>Raw .gon</b></summary>

```
Shield { 
    name "KEYWORD_SHIELD_NAME"
    tooltip None

    tooltip_stackless "KEYWORD_SHIELD_DESC_STACKLESS"
}
```

</details>

---

### `shield`
**Name:** shield  

| Field | Value |
| :--- | :--- |
| Alias | Shield |

<details>
<summary><b>Raw .gon</b></summary>

```
shield {
    alias Shield
}
```

</details>

---

### `ShortCircuit`
**Name:** ShortCircuit  

<details>
<summary><b>Raw .gon</b></summary>

```
ShortCircuit {
    name "KEYWORD_SHORTCIRCUIT_NAME"
    tooltip "KEYWORD_SHORTCIRCUIT_DESC"
}
```

</details>

---

### `SkipNextTurn`
**Name:** SkipNextTurn  

<details>
<summary><b>Raw .gon</b></summary>

```
SkipNextTurn { 
    name "SkipNextTurn"
    tooltip None
}
```

</details>

---

### `Sleep`
**Name:** Sleep  

<details>
<summary><b>Raw .gon</b></summary>

```
Sleep {
    name "KEYWORD_SLEEP_NAME"
    tooltip_stacks "KEYWORD_SLEEP_DESC"

    tooltip_stackless "KEYWORD_SLEEP_DESC_STACKLESS"
}
```

</details>

---

### `SleepParalysis`
**Name:** SleepParalysis  

<details>
<summary><b>Raw .gon</b></summary>

```
SleepParalysis {
    name "KEYWORD_SLEEPPAR_NAME"
    tooltip_stacks "KEYWORD_SLEEPPAR_DESC"
}
```

</details>

---

### `Slow`
**Name:** Slow  

<details>
<summary><b>Raw .gon</b></summary>

```
Slow {
    name "KEYWORD_SLOW_NAME"
    tooltip_stacks "KEYWORD_SLOW_DESC"
    tooltip_stackless "KEYWORD_SLOW_DESC_STACKLESS"
    tooltip_stacks_neg "KEYWORD_SLOW_DESC_STACKLESS"
}
```

</details>

---

### `SoulLink`
**Name:** SoulLink  

<details>
<summary><b>Raw .gon</b></summary>

```
SoulLink {
    name "KEYWORD_SOULLINK_NAME"
    tooltip "KEYWORD_SOULLINK_DESC"
}
```

</details>

---

### `SpeedUp`
**Name:** SpeedUp  

<details>
<summary><b>Raw .gon</b></summary>

```
SpeedUp {
    name "KEYWORD_SPDUP_NAME"
    name_stacks_neg "KEYWORD_SPDDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_SPDUP_DESC"
    tooltip_stacks_neg "KEYWORD_SPWDDOWN_DESC"

    tooltip_stackless none 
}
```

</details>

---

### `SpeedUp_WithoutInitiative`
**Name:** SpeedUp_WithoutInitiative  

| Field | Value |
| :--- | :--- |
| Alias | SpeedUp |

<details>
<summary><b>Raw .gon</b></summary>

```
SpeedUp_WithoutInitiative {
    alias SpeedUp
}
```

</details>

---

### `SpellDamageUp`
**Name:** SpellDamageUp  

<details>
<summary><b>Raw .gon</b></summary>

```
SpellDamageUp { 
    name "KEYWORD_MAGICDMGUP_NAME"
    tooltip_stacks "KEYWORD_MAGICDMGUP_DESC"

    tooltip_stackless "KEYWORD_MAGICDMGUP_DESC_STACKLESS"
}
```

</details>

---

### `SpellShield`
**Name:** SpellShield  

<details>
<summary><b>Raw .gon</b></summary>

```
SpellShield { 
    name "SpellShield"
    tooltip None
}
```

</details>

---

### `SpiderInfested`
**Name:** SpiderInfested  

<details>
<summary><b>Raw .gon</b></summary>

```
SpiderInfested {
    name "KEYWORD_SPIDERINFESTED_NAME"
    tooltip "KEYWORD_SPIDERINFESTED_DESC"
}
```

</details>

---

### `SproutsGrantMovement`
**Name:** SproutsGrantMovement  

| Field | Value |
| :--- | :--- |
| Alias | MovementUp |

<details>
<summary><b>Raw .gon</b></summary>

```
SproutsGrantMovement {
    alias MovementUp
}
```

</details>

---

### `StatBounty`
**Name:** StatBounty  

<details>
<summary><b>Raw .gon</b></summary>

```
StatBounty {
    name "KEYWORD_STATBOUNTY_NAME"
    tooltip_stacks "KEYWORD_STATBOUNTY_DESC"
    tooltip_stackless "KEYWORD_STATBOUNTY_DESC_STACKLESS"
}
```

</details>

---

### `Stealth`
**Name:** Stealth  

<details>
<summary><b>Raw .gon</b></summary>

```
Stealth {
    name "KEYWORD_STEALTH_NAME"
    tooltip "KEYWORD_STEALTH_DESC"
}
```

</details>

---

### `StealthUntilBasicAttack`
**Name:** StealthUntilBasicAttack  

<details>
<summary><b>Raw .gon</b></summary>

```
StealthUntilBasicAttack {
    name "KEYWORD_STEALTHUNTIL_NAME"
    tooltip "KEYWORD_STEALTHUNTIL_DESC"
}
```

</details>

---

### `StrDownAura`
**Name:** StrDownAura  

| Field | Value |
| :--- | :--- |
| Alias | StrengthUp |

<details>
<summary><b>Raw .gon</b></summary>

```
StrDownAura {
    alias StrengthUp
}
```

</details>

---

### `DexDownAura`
**Name:** DexDownAura  

| Field | Value |
| :--- | :--- |
| Alias | DexterityUp |

<details>
<summary><b>Raw .gon</b></summary>

```
DexDownAura {
    alias DexterityUp
}
```

</details>

---

### `SpdDownAura`
**Name:** SpdDownAura  

| Field | Value |
| :--- | :--- |
| Alias | SpeedUp |

<details>
<summary><b>Raw .gon</b></summary>

```
SpdDownAura {
    alias SpeedUp
}
```

</details>

---

### `StrengthForEachNeighboringEnemy`
**Name:** StrengthForEachNeighboringEnemy  

| Field | Value |
| :--- | :--- |
| Alias | StrengthUp |

<details>
<summary><b>Raw .gon</b></summary>

```
StrengthForEachNeighboringEnemy {
    alias StrengthUp
}
```

</details>

---

### `StrengthUp`
**Name:** StrengthUp  

<details>
<summary><b>Raw .gon</b></summary>

```
StrengthUp {
    name "KEYWORD_STRUP_NAME"
    name_stacks_neg "KEYWORD_STRDOWN_NAME"
    tooltip_stacks_pos "KEYWORD_STRUP_DESC"
    tooltip_stacks_neg "KEYWORD_STRDOWN_DESC"

    tooltip_stackless none 
}
```

</details>

---

### `Stun`
**Name:** Stun  

<details>
<summary><b>Raw .gon</b></summary>

```
Stun {
    name "KEYWORD_STUN_NAME"
    tooltip_stacks "KEYWORD_STUN_DESC"

    tooltip_stackless "KEYWORD_STUN_DESC_STACKLESS"
}
```

</details>

---

### `Switcheroo`
**Name:** Switcheroo  

<details>
<summary><b>Raw .gon</b></summary>

```
Switcheroo { 
    name "Switcheroo"
    tooltip None
}
```

</details>

---

### `Tarred`
**Name:** Tarred  

<details>
<summary><b>Raw .gon</b></summary>

```
Tarred {
    name "KEYWORD_TARRED_NAME"
    tooltip_stacks "KEYWORD_TARRED_DESC"

    tooltip_stackless "KEYWORD_TARRED_DESC_STACKLESS"
}
```

</details>

---

### `Taunted`
**Name:** Taunted  

<details>
<summary><b>Raw .gon</b></summary>

```
Taunted { 
    name "Taunted"
    tooltip None
}
```

</details>

---

### `Taunting`
**Name:** Taunting  

<details>
<summary><b>Raw .gon</b></summary>

```
Taunting { 
    name "Taunting"
    tooltip None
}
```

</details>

---

### `Tech`
**Name:** Tech  

<details>
<summary><b>Raw .gon</b></summary>

```
Tech {
    name "KEYWORD_TECH_NAME"
    tooltip "KEYWORD_TECH_DESC"
}
```

</details>

---

### `TempBackstab`
**Name:** TempBackstab  

<details>
<summary><b>Raw .gon</b></summary>

```
TempBackstab {
    name "KEYWORD_TEMPBACKSTAB_NAME"
    tooltip_stacks "KEYWORD_TEMPBACKSTAB_DESC"

    tooltip_stackless "KEYWORD_TEMPBACKSTAB_DESC_STACKLESS"
}
```

</details>

---

### `TempCharmed`
**Name:** TempCharmed  

| Field | Value |
| :--- | :--- |
| Alias | Charmed |

<details>
<summary><b>Raw .gon</b></summary>

```
TempCharmed {
    alias Charmed
}
```

</details>

---

### `TempCounterAttack`
**Name:** TempCounterAttack  

<details>
<summary><b>Raw .gon</b></summary>

```
TempCounterAttack { 
    name "KEYWORD_TEMPCOUNTER_NAME"
    tooltip "KEYWORD_TEMPCOUNTER_DESC"
}
```

</details>

---

### `TempCritChanceUp`
**Name:** TempCritChanceUp  

| Field | Value |
| :--- | :--- |
| Alias | CritChanceUp |

<details>
<summary><b>Raw .gon</b></summary>

```
TempCritChanceUp {
    alias CritChanceUp
}
```

</details>

---

### `TempDamageUp`
**Name:** TempDamageUp  

| Field | Value |
| :--- | :--- |
| Alias | DamageUp |

<details>
<summary><b>Raw .gon</b></summary>

```
TempDamageUp {
    alias DamageUp
}
```

</details>

---

### `TempDexterityUp`
**Name:** TempDexterityUp  

| Field | Value |
| :--- | :--- |
| Alias | DexterityUp |

<details>
<summary><b>Raw .gon</b></summary>

```
TempDexterityUp {
    alias DexterityUp
}
```

</details>

---

### `TempInitiativeChange`
**Name:** TempInitiativeChange  

<details>
<summary><b>Raw .gon</b></summary>

```
TempInitiativeChange {
    name "KEYWORD_TEMPINIT_NAME"
    tooltip "KEYWORD_TEMPINIT_DESC"
    name_stacks_neg "KEYWORD_TEMPINITDOWN_NAME"
    tooltip_stacks_neg "KEYWORD_TEMPINITDOWN_DESC"
    tooltip_stackless_neg "KEYWORD_TEMPINITDOWN_DESC"
}
```

</details>

---

### `TempInjuryImmunity`
**Name:** TempInjuryImmunity  

<details>
<summary><b>Raw .gon</b></summary>

```
TempInjuryImmunity {
     name "KEYWORD_TEMPIMMUNE_NAME"
     tooltip_stacks "KEYWORD_TEMPIMMUNE_DESC"
     tooltip_stacks_singular "KEYWORD_TEMPIMMUNE_DESC_SINGULAR"
     tooltip_stackless none 
}
```

</details>

---

### `TempManaCostReduction`
**Name:** TempManaCostReduction  

<details>
<summary><b>Raw .gon</b></summary>

```
TempManaCostReduction {
    name "KEYWORD_TEMPMANAREDUCTION_NAME"
    tooltip_stacks "KEYWORD_TEMPMANAREDUCTION_DESC"
    tooltip_stackless "KEYWORD_TEMPMANAREDUCTION_DESC_STACKLESS"
}
```

</details>

---

### `TempMovement`
**Name:** TempMovement  

| Field | Value |
| :--- | :--- |
| Alias | MovementUp |

<details>
<summary><b>Raw .gon</b></summary>

```
TempMovement {
    alias MovementUp
}
```

</details>

---

### `TempPreEmptiveCounterAttack`
**Name:** TempPreEmptiveCounterAttack  

<details>
<summary><b>Raw .gon</b></summary>

```
TempPreEmptiveCounterAttack { 
    name "KEYWORD_PRECOUNTER_NAME"
    tooltip "KEYWORD_PRECOUNTER_DESC"
}
```

</details>

---

### `TempSpeedUp`
**Name:** TempSpeedUp  

| Field | Value |
| :--- | :--- |
| Alias | SpeedUp |

<details>
<summary><b>Raw .gon</b></summary>

```
TempSpeedUp {
    alias SpeedUp
}
```

</details>

---

### `TempSpellDamageUp`
**Name:** TempSpellDamageUp  

| Field | Value |
| :--- | :--- |
| Alias | SpellDamageUp |

<details>
<summary><b>Raw .gon</b></summary>

```
TempSpellDamageUp { 
    alias SpellDamageUp
}
```

</details>

---

### `TempStrengthUp`
**Name:** TempStrengthUp  

| Field | Value |
| :--- | :--- |
| Alias | StrengthUp |

<details>
<summary><b>Raw .gon</b></summary>

```
TempStrengthUp {
    alias StrengthUp
}
```

</details>

---

### `Thorns`
**Name:** Thorns  

<details>
<summary><b>Raw .gon</b></summary>

```
Thorns {
    name "KEYWORD_THORNS_NAME"
    tooltip_stacks "KEYWORD_THORNS_DESC"

    tooltip_stackless "KEYWORD_THORNS_DESC_STACKLESS"
}
```

</details>

---

### `TilesMovedToCritChance`
**Name:** TilesMovedToCritChance  

<details>
<summary><b>Raw .gon</b></summary>

```
TilesMovedToCritChance { 
    name "TilesMovedToCritChance"
    tooltip None
}
```

</details>

---

### `TilesMovedToHealth`
**Name:** TilesMovedToHealth  

<details>
<summary><b>Raw .gon</b></summary>

```
TilesMovedToHealth { 
    name "TilesMovedToHealth"
    tooltip None
}
```

</details>

---

### `TilesMovedToMana`
**Name:** TilesMovedToMana  

<details>
<summary><b>Raw .gon</b></summary>

```
TilesMovedToMana { 
    name "TilesMovedToMana"
    tooltip None
}
```

</details>

---

### `TilesMovedToNeighborHeal`
**Name:** TilesMovedToNeighborHeal  

<details>
<summary><b>Raw .gon</b></summary>

```
TilesMovedToNeighborHeal { 
    name "TilesMovedToNeighborHeal"
    tooltip None
}
```

</details>

---

### `TilesMovedToStrength`
**Name:** TilesMovedToStrength  

<details>
<summary><b>Raw .gon</b></summary>

```
TilesMovedToStrength { 
    name "TilesMovedToStrength"
    tooltip None
}
```

</details>

---

### `TowerDefenseStatus`
**Name:** TowerDefenseStatus  

<details>
<summary><b>Raw .gon</b></summary>

```
TowerDefenseStatus {
    name "KEYWORD_SENTRY_NAME"
    tooltip "KEYWORD_SENTRY_DESC"
}
```

</details>

---

### `TowerDefenseStatus2`
**Name:** TowerDefenseStatus2  

<details>
<summary><b>Raw .gon</b></summary>

```
TowerDefenseStatus2 {
    name "KEYWORD_SENTRYPLUS_NAME"
    tooltip_stacks "KEYWORD_SENTRYPLUS_DESC"

    tooltip_stackless "KEYWORD_SENTRYPLUS_DESC_STACKLESS"
}
```

</details>

---

### `TrailBlazer`
**Name:** TrailBlazer  

<details>
<summary><b>Raw .gon</b></summary>

```
TrailBlazer { 
    name "Trail Blazer"
    tooltip None
}
```

</details>

---

### `Trample`
**Name:** Trample  

<details>
<summary><b>Raw .gon</b></summary>

```
Trample { 
    name "KEYWORD_TRAMPLE_NAME"
    tooltip None

    tooltip_stackless "KEYWORD_TRAMPLE_DESC_STACKLESS"

    icon_frame 153
}
```

</details>

---

### `TransformInXTurns`
**Name:** TransformInXTurns  

<details>
<summary><b>Raw .gon</b></summary>

```
TransformInXTurns { 
    name "KEYWORD_TRANSFORM_NAME"
    tooltip "KEYWORD_TRANSFORM_DESC"
}
```

</details>

---

### `VeinyBonus`
**Name:** VeinyBonus  

| Field | Value |
| :--- | :--- |
| Alias | StrengthUp |

<details>
<summary><b>Raw .gon</b></summary>

```
VeinyBonus {
    alias StrengthUp
}
```

</details>

---

### `Weakness`
**Name:** Weakness  

<details>
<summary><b>Raw .gon</b></summary>

```
Weakness {
    name "KEYWORD_WEAKNESS_NAME"
    tooltip_stacks "KEYWORD_WEAKNESS_DESC"
    tooltip_stacks_singular "KEYWORD_WEAKNESS_DESC_SINGULAR"
    tooltip_stackless "KEYWORD_WEAKNESS_DESC_STACKLESS"
}
```

</details>

---

### `DepressionAura`
**Name:** DepressionAura  

| Field | Value |
| :--- | :--- |
| Alias | AllStatsUp |

<details>
<summary><b>Raw .gon</b></summary>

```
DepressionAura { 
    alias AllStatsUp
}
```

</details>

---

### `Webbed`
**Name:** Webbed  

<details>
<summary><b>Raw .gon</b></summary>

```
Webbed {
    name "KEYWORD_WEBBED_NAME"
    tooltip "KEYWORD_WEBBED_DESC"
}
```

</details>

---

### `Tangled`
**Name:** Tangled  

<details>
<summary><b>Raw .gon</b></summary>

```
Tangled {
    name "KEYWORD_TANGLED_NAME"
    tooltip "KEYWORD_TANGLED_DESC"
}
```

</details>

---

### `Wet`
**Name:** Wet  

<details>
<summary><b>Raw .gon</b></summary>

```
Wet {
    name "KEYWORD_WET_NAME"
    tooltip "KEYWORD_WET_DESC"
}
```

</details>

---

### `Zombie`
**Name:** Zombie  

<details>
<summary><b>Raw .gon</b></summary>

```
Zombie {
    name "KEYWORD_ZOMBIE_NAME"
    tooltip "KEYWORD_ZOMBIE_DESC"
}
```

</details>

---

### `Metal`
**Name:** Metal  

<details>
<summary><b>Raw .gon</b></summary>

```
Metal {
    name "KEYWORD_METAL_NAME"
    tooltip "KEYWORD_METAL_DESC"

    icon_frame 151
}
```

</details>

---

### `Fragile`
**Name:** Fragile  

<details>
<summary><b>Raw .gon</b></summary>

```
Fragile {
    name "KEYWORD_FRAGILE_NAME"
    tooltip "KEYWORD_FRAGILE_DESC"

    icon_frame 149
}
```

</details>

---

### `FragileDuringElement`
**Name:** FragileDuringElement  

| Field | Value |
| :--- | :--- |
| Alias | Fragile |

<details>
<summary><b>Raw .gon</b></summary>

```
FragileDuringElement {
    alias Fragile
}
```

</details>

---

### `Brittle`
**Name:** Brittle  

<details>
<summary><b>Raw .gon</b></summary>

```
Brittle {
    name "KEYWORD_BRITTLE_NAME"
    tooltip "KEYWORD_BRITTLE_DESC"

    icon_frame 150
}
```

</details>

---

### `BrittleDuringElement`
**Name:** BrittleDuringElement  

| Field | Value |
| :--- | :--- |
| Alias | Brittle |

<details>
<summary><b>Raw .gon</b></summary>

```
BrittleDuringElement {
    alias Brittle
}
```

</details>

---

### `Flammable`
**Name:** Flammable  

<details>
<summary><b>Raw .gon</b></summary>

```
Flammable {
    name "KEYWORD_FLAMMABLE_NAME"
    tooltip "KEYWORD_FLAMMABLE_DESC"

    icon_frame 148
}
```

</details>

---

### `Cursed`
**Name:** Cursed  

<details>
<summary><b>Raw .gon</b></summary>

```
Cursed {
    name "KEYWORD_CURSED_NAME"
    tooltip "KEYWORD_CURSED_DESC"

    icon_frame 156
}
```

</details>

---

### `Reload`
**Name:** Reload  

<details>
<summary><b>Raw .gon</b></summary>

```
Reload {
    name "KEYWORD_RELOAD_NAME"
    tooltip "KEYWORD_RELOAD_DESC"

    icon_frame 159
}
```

</details>

---

### `ReloadB`
**Name:** ReloadB  

<details>
<summary><b>Raw .gon</b></summary>

```
ReloadB {
    name "KEYWORD_RELOAD_NAME"
    tooltip "KEYWORD_RELOADB_DESC"

    icon_frame 159
}
```

</details>

---

### `Flying`
**Name:** Flying  

<details>
<summary><b>Raw .gon</b></summary>

```
Flying {
    name "KEYWORD_FLYING_NAME"
    tooltip "KEYWORD_FLYING_DESC"

    icon_frame 157
}
```

</details>

---

### `Comfort`
**Name:** Comfort  

<details>
<summary><b>Raw .gon</b></summary>

```
Comfort {
    name "KEYWORD_COMFORT_NAME"
    tooltip "KEYWORD_COMFORT_DESC"
}
```

</details>

---

### `Stimulation`
**Name:** Stimulation  

<details>
<summary><b>Raw .gon</b></summary>

```
Stimulation {
    name "KEYWORD_STIMULATION_NAME"
    tooltip "KEYWORD_STIMULATION_DESC"
}
```

</details>

---

### `Appeal`
**Name:** Appeal  

<details>
<summary><b>Raw .gon</b></summary>

```
Appeal {
    name "KEYWORD_APPEAL_NAME"
    tooltip "KEYWORD_APPEAL_DESC"
}
```

</details>

---

### `Evolution`
**Name:** Evolution  

<details>
<summary><b>Raw .gon</b></summary>

```
Evolution {
    name "KEYWORD_EVOLUTION_NAME"
    tooltip "KEYWORD_EVOLUTION_DESC"
}
```

</details>

---

### `Health`
**Name:** Health  

<details>
<summary><b>Raw .gon</b></summary>

```
Health {
    name "KEYWORD_HEALTH_NAME"
    tooltip "KEYWORD_HEALTH_DESC"
}
```

</details>

---

### `DemonicGlyph_Bite`
**Name:** DemonicGlyph_Bite  

<details>
<summary><b>Raw .gon</b></summary>

```
DemonicGlyph_Bite {
    name "KEYWORD_TOR_BITE_NAME"
    tooltip "KEYWORD_TOR_BITE_DESC"
}
```

</details>

---

### `DemonicGlyph_Fire`
**Name:** DemonicGlyph_Fire  

<details>
<summary><b>Raw .gon</b></summary>

```
DemonicGlyph_Fire {
    name "KEYWORD_TOR_FIRE_NAME"
    tooltip "KEYWORD_TOR_FIRE_DESC"
}
```

</details>

---

### `DemonicGlyph_Summon`
**Name:** DemonicGlyph_Summon  

<details>
<summary><b>Raw .gon</b></summary>

```
DemonicGlyph_Summon {
    name "KEYWORD_TOR_SUMMON_NAME"
    tooltip "KEYWORD_TOR_SUMMON_DESC"
}
```

</details>

---

### `DemonicGlyph_Movement`
**Name:** DemonicGlyph_Movement  

<details>
<summary><b>Raw .gon</b></summary>

```
DemonicGlyph_Movement {
    name "KEYWORD_TOR_MOVE_NAME"
    tooltip "KEYWORD_TOR_MOVE_DESC"
}
```

</details>

---

### `DemonicGlyph_Bounce`
**Name:** DemonicGlyph_Bounce  

<details>
<summary><b>Raw .gon</b></summary>

```
DemonicGlyph_Bounce {
    name "KEYWORD_TOR_BOUNCE_NAME"
    tooltip "KEYWORD_TOR_BOUNCE_DESC"
}
```

</details>

---

### `FinalBossHitCountdownHoly`
**Name:** FinalBossHitCountdownHoly  

<details>
<summary><b>Raw .gon</b></summary>

```
FinalBossHitCountdownHoly {
    name "KEYWORD_CHILDHOLY_NAME"
    tooltip "KEYWORD_CHILDHOLY_DESC"
}
```

</details>

---

### `FinalBossHitCountdownBoris`
**Name:** FinalBossHitCountdownBoris  

<details>
<summary><b>Raw .gon</b></summary>

```
FinalBossHitCountdownBoris {
    name "KEYWORD_CHILDPULSE_NAME"
    tooltip "KEYWORD_CHILDPULSE_DESC"
}
```

</details>

---

### `FinalBossHitCountdownExplosive`
**Name:** FinalBossHitCountdownExplosive  

<details>
<summary><b>Raw .gon</b></summary>

```
FinalBossHitCountdownExplosive {
    name "KEYWORD_CHILDWRATH_NAME"
    tooltip "KEYWORD_CHILDWRATH_DESC"
}
```

</details>

---

### `TVBotObey`
**Name:** TVBotObey  

<details>
<summary><b>Raw .gon</b></summary>

```
TVBotObey {
    name "ENEMY_TVBOT_OBEY_NAME"
    tooltip "ENEMY_TVBOT_OBEY_DESC"

    icon_frame 155
}
```

</details>

---

### `TVBotStop`
**Name:** TVBotStop  

<details>
<summary><b>Raw .gon</b></summary>

```
TVBotStop {
    name "ENEMY_TVBOT_STOP_NAME"
    tooltip "ENEMY_TVBOT_STOP_DESC"

    icon_frame 155
}
```

</details>

---

### `TVBotDumb`
**Name:** TVBotDumb  

<details>
<summary><b>Raw .gon</b></summary>

```
TVBotDumb {
    name "ENEMY_TVBOT_DUMB_NAME"
    tooltip "ENEMY_TVBOT_DUMB_DESC"

    icon_frame 155
}
```

</details>

---

### `TVBotDie`
**Name:** TVBotDie  

<details>
<summary><b>Raw .gon</b></summary>

```
TVBotDie {
    name "ENEMY_TVBOT_DIE_NAME"
    tooltip "ENEMY_TVBOT_DIE_DESC"

    icon_frame 155
}
```

</details>

---

### `EliteBuff_Spiky`
**Name:** EliteBuff_Spiky  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Spiky {
    name "KEYWORD_ELITE_SPIKY_NAME"
    tooltip "KEYWORD_ELITE_SPIKY_DESC"
}
```

</details>

---

### `EliteBuff_BossSpiky`
**Name:** EliteBuff_BossSpiky  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossSpiky {
    name "KEYWORD_ELITE_BOSSSPIKY_NAME"
    tooltip "KEYWORD_ELITE_BOSSSPIKY_DESC"
}
```

</details>

---

### `EliteBuff_Reactive`
**Name:** EliteBuff_Reactive  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Reactive {
    name "KEYWORD_ELITE_REACTIVE_NAME"
    tooltip "KEYWORD_ELITE_REACTIVE_DESC"
}
```

</details>

---

### `EliteBuff_BossReactive`
**Name:** EliteBuff_BossReactive  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Reactive |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossReactive {
    alias EliteBuff_Reactive
}
```

</details>

---

### `EliteBuff_Damaging`
**Name:** EliteBuff_Damaging  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Damaging {
    name "KEYWORD_ELITE_DAMAGING_NAME"
    tooltip "KEYWORD_ELITE_DAMAGING_DESC"
}
```

</details>

---

### `EliteBuff_BossDamaging`
**Name:** EliteBuff_BossDamaging  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Damaging |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossDamaging {
    alias EliteBuff_Damaging
}
```

</details>

---

### `EliteBuff_Tough`
**Name:** EliteBuff_Tough  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Tough {
    name "KEYWORD_ELITE_TOUGH_NAME"
    tooltip "KEYWORD_ELITE_TOUGH_DESC"
}
```

</details>

---

### `EliteBuff_BossTough`
**Name:** EliteBuff_BossTough  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossTough {
    name "KEYWORD_ELITE_BOSSTOUGH_NAME"
    tooltip "KEYWORD_ELITE_BOSSTOUGH_DESC"
}
```

</details>

---

### `EliteBuff_Shielded1`
**Name:** EliteBuff_Shielded1  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Shielded1 {
    name "KEYWORD_ELITE_SHIELDED1_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED1_DESC"
}
```

</details>

---

### `EliteBuff_BossShielded1`
**Name:** EliteBuff_BossShielded1  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossShielded1 {
    name "KEYWORD_ELITE_BOSSSHIELDED1_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED1_DESC"
}
```

</details>

---

### `EliteBuff_Shielded2`
**Name:** EliteBuff_Shielded2  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Shielded2 {
    name "KEYWORD_ELITE_SHIELDED2_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED2_DESC"
}
```

</details>

---

### `EliteBuff_BossShielded2`
**Name:** EliteBuff_BossShielded2  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossShielded2 {
    name "KEYWORD_ELITE_BOSSSHIELDED2_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED2_DESC"
}
```

</details>

---

### `EliteBuff_Shielded3`
**Name:** EliteBuff_Shielded3  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Shielded3 {
    name "KEYWORD_ELITE_SHIELDED3_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED3_DESC"
}
```

</details>

---

### `EliteBuff_BossShielded3`
**Name:** EliteBuff_BossShielded3  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossShielded3 {
    name "KEYWORD_ELITE_BOSSSHIELDED3_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED3_DESC"
}
```

</details>

---

### `EliteBuff_Shielded4`
**Name:** EliteBuff_Shielded4  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Shielded4 {
    name "KEYWORD_ELITE_SHIELDED4_NAME"
    tooltip "KEYWORD_ELITE_SHIELDED4_DESC"
}
```

</details>

---

### `EliteBuff_BossShielded4`
**Name:** EliteBuff_BossShielded4  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossShielded4 {
    name "KEYWORD_ELITE_BOSSSHIELDED4_NAME"
    tooltip "KEYWORD_ELITE_BOSSSHIELDED4_DESC"
}
```

</details>

---

### `EliteBuff_Protected`
**Name:** EliteBuff_Protected  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Protected {
    name "KEYWORD_ELITE_PROTECTED_NAME"
    tooltip "KEYWORD_ELITE_PROTECTED_DESC"
}
```

</details>

---

### `EliteBuff_BossProtected`
**Name:** EliteBuff_BossProtected  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Protected |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossProtected {
    alias EliteBuff_Protected
}
```

</details>

---

### `EliteBuff_Speedy`
**Name:** EliteBuff_Speedy  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Speedy {
    name "KEYWORD_ELITE_SPEEDY_NAME"
    tooltip "KEYWORD_ELITE_SPEEDY_DESC"
}
```

</details>

---

### `EliteBuff_BossSpeedy`
**Name:** EliteBuff_BossSpeedy  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Speedy |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossSpeedy {
    alias EliteBuff_Speedy
}
```

</details>

---

### `EliteBuff_Flaming`
**Name:** EliteBuff_Flaming  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Flaming {
    name "KEYWORD_ELITE_FLAMING_NAME"
    tooltip "KEYWORD_ELITE_FLAMING_DESC"
}
```

</details>

---

### `EliteBuff_BossFlaming`
**Name:** EliteBuff_BossFlaming  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossFlaming {
    name "KEYWORD_ELITE_BOSSFLAMING_NAME"
    tooltip "KEYWORD_ELITE_BOSSFLAMING_DESC"
}
```

</details>

---

### `EliteBuff_Creepy`
**Name:** EliteBuff_Creepy  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Creepy {
    name "KEYWORD_ELITE_CREEPY_NAME"
    tooltip "KEYWORD_ELITE_CREEPY_DESC"
}
```

</details>

---

### `EliteBuff_Lucky`
**Name:** EliteBuff_Lucky  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Lucky {
    name "KEYWORD_ELITE_LUCKY_NAME"
    tooltip "KEYWORD_ELITE_LUCKY_DESC"
}
```

</details>

---

### `EliteBuff_BossLucky`
**Name:** EliteBuff_BossLucky  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Lucky |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossLucky {
    alias EliteBuff_Lucky
}
```

</details>

---

### `EliteBuff_Static`
**Name:** EliteBuff_Static  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Static {
    name "KEYWORD_ELITE_STATIC_NAME"
    tooltip "KEYWORD_ELITE_STATIC_DESC"
}
```

</details>

---

### `EliteBuff_BossStatic`
**Name:** EliteBuff_BossStatic  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Static |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossStatic {
    alias EliteBuff_Static
}
```

</details>

---

### `EliteBuff_Bouncy`
**Name:** EliteBuff_Bouncy  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Bouncy {
    name "KEYWORD_ELITE_BOUNCY_NAME"
    tooltip "KEYWORD_ELITE_BOUNCY_DESC"
}
```

</details>

---

### `EliteBuff_BossBouncy`
**Name:** EliteBuff_BossBouncy  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Bouncy |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossBouncy {
    alias EliteBuff_Bouncy
}
```

</details>

---

### `EliteBuff_Mirror`
**Name:** EliteBuff_Mirror  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Mirror {
    name "KEYWORD_ELITE_MIRROR_NAME"
    tooltip "KEYWORD_ELITE_MIRROR_DESC"
}
```

</details>

---

### `EliteBuff_Resonant`
**Name:** EliteBuff_Resonant  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Resonant {
    name "KEYWORD_ELITE_RESONANT_NAME"
    tooltip "KEYWORD_ELITE_RESONANT_DESC"
}
```

</details>

---

### `EliteBuff_Undying`
**Name:** EliteBuff_Undying  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Undying {
    name "KEYWORD_ELITE_UNDYING_NAME"
    tooltip "KEYWORD_ELITE_UNDYING_DESC"
}
```

</details>

---

### `EliteBuff_SubUndying`
**Name:** EliteBuff_SubUndying  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_SubUndying {
    name "KEYWORD_ELITE_SUBUNDYING_NAME"
    tooltip "KEYWORD_ELITE_SUBUNDYING_DESC"
}
```

</details>

---

### `EliteBuff_Healthy`
**Name:** EliteBuff_Healthy  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Healthy {
    name "KEYWORD_ELITE_HEALTHY_NAME"
    tooltip "KEYWORD_ELITE_HEALTHY_DESC"
}
```

</details>

---

### `EliteBuff_Sandy`
**Name:** EliteBuff_Sandy  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Sandy {
    name "KEYWORD_ELITE_SANDY_NAME"
    tooltip "KEYWORD_ELITE_SANDY_DESC"
}
```

</details>

---

### `EliteBuff_Infested`
**Name:** EliteBuff_Infested  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Infested {
    name "KEYWORD_ELITE_INFESTED_NAME"
    tooltip "KEYWORD_ELITE_INFESTED_DESC"
}
```

</details>

---

### `EliteBuff_Absorbant`
**Name:** EliteBuff_Absorbant  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Absorbant {
    name "KEYWORD_ELITE_ABSORBANT_NAME"
    tooltip "KEYWORD_ELITE_ABSORBANT_DESC"
}
```

</details>

---

### `EliteBuff_BossAbsorbant`
**Name:** EliteBuff_BossAbsorbant  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Absorbant |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossAbsorbant {
    alias EliteBuff_Absorbant
}
```

</details>

---

### `EliteBuff_Depressing`
**Name:** EliteBuff_Depressing  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Depressing {
    name "KEYWORD_ELITE_DEPRESSING_NAME"
    tooltip "KEYWORD_ELITE_DEPRESSING_DESC"
}
```

</details>

---

### `EliteBuff_BossDepressing`
**Name:** EliteBuff_BossDepressing  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Depressing |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossDepressing {
    alias EliteBuff_Depressing
}
```

</details>

---

### `EliteBuff_SlightlyDepressing`
**Name:** EliteBuff_SlightlyDepressing  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_SlightlyDepressing {
    name "KEYWORD_ELITE_SLIGHTLYDEPRESSING_NAME"
    tooltip "KEYWORD_ELITE_SLIGHTLYDEPRESSING_DESC"
}
```

</details>

---

### `EliteBuff_BossSlightlyDepressing`
**Name:** EliteBuff_BossSlightlyDepressing  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_SlightlyDepressing |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossSlightlyDepressing {
    alias EliteBuff_SlightlyDepressing
}
```

</details>

---

### `EliteBuff_Evolving`
**Name:** EliteBuff_Evolving  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Evolving {
    name "KEYWORD_ELITE_EVOLVING_NAME"
    tooltip "KEYWORD_ELITE_EVOLVING_DESC"
}
```

</details>

---

### `EliteBuff_Plow`
**Name:** EliteBuff_Plow  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Plow {
    name "KEYWORD_ELITE_PLOW_NAME"
    tooltip "KEYWORD_ELITE_PLOW_DESC"
}
```

</details>

---

### `EliteBuff_Mega`
**Name:** EliteBuff_Mega  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Mega {
    name "KEYWORD_ELITE_MEGA_NAME"
    tooltip "KEYWORD_ELITE_MEGA_DESC"
}
```

</details>

---

### `EliteBuff_Mad`
**Name:** EliteBuff_Mad  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Mad {
    name "KEYWORD_ELITE_MAD_NAME"
    tooltip "KEYWORD_ELITE_MAD_DESC"
}
```

</details>

---

### `EliteBuff_BossMad`
**Name:** EliteBuff_BossMad  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossMad {
    name "KEYWORD_ELITE_BOSSMAD_NAME"
    tooltip "KEYWORD_ELITE_BOSSMAD_DESC"
}
```

</details>

---

### `EliteBuff_Twin`
**Name:** EliteBuff_Twin  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Twin {
    name "KEYWORD_ELITE_TWIN_NAME"
    tooltip "KEYWORD_ELITE_TWIN_DESC"
}
```

</details>

---

### `EliteBuff_BossTwin`
**Name:** EliteBuff_BossTwin  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Twin |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossTwin {
    alias EliteBuff_Twin
}
```

</details>

---

### `EliteBuff_SubTwin`
**Name:** EliteBuff_SubTwin  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Twin |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_SubTwin {
    alias EliteBuff_Twin
}
```

</details>

---

### `EliteBuff_BossSubTwin`
**Name:** EliteBuff_BossSubTwin  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Twin |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossSubTwin {
    alias EliteBuff_Twin
}
```

</details>

---

### `EliteBuff_Hardy`
**Name:** EliteBuff_Hardy  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Hardy {
    name "KEYWORD_ELITE_HARDY_NAME"
    tooltip "KEYWORD_ELITE_HARDY_DESC"
}
```

</details>

---

### `EliteBuff_BossHardy`
**Name:** EliteBuff_BossHardy  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Hardy |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossHardy {
    alias EliteBuff_Hardy
}
```

</details>

---

### `EliteBuff_Sticky`
**Name:** EliteBuff_Sticky  

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_Sticky {
    name "KEYWORD_ELITE_STICKY_NAME"
    tooltip "KEYWORD_ELITE_STICKY_DESC"
}
```

</details>

---

### `EliteBuff_BossSticky`
**Name:** EliteBuff_BossSticky  

| Field | Value |
| :--- | :--- |
| Alias | EliteBuff_Sticky |

<details>
<summary><b>Raw .gon</b></summary>

```
EliteBuff_BossSticky {
    alias EliteBuff_Sticky
}
```

</details>

---

