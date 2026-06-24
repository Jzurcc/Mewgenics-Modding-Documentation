# Disorders Directory

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
                free false 
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

            HealthGain 3*X 
        }
        TaggedPickupEffectReplacement {
            tag scrap

            HealthGain 2*X 
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

            Trample [3, X-8] 
        }
    }
}
```

---

### `Gigantism`
**Name:** Gigantism  
**Description:** Trample.  
**Source:** `disorders.gon`  

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
SkillShare_Disorder { 
    name "DISORDER_SKILLSHAREDISORDER_NAME"
    desc "DISORDER_SKILLSHAREDISORDER_DESC"
    class Disorder

    passives {
        
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

---

### `BrainDead`
**Name:** Brain Dead  
**Description:** Gain twice as many stats when you level up. +1 Reroll when leveling up.  
**Source:** `disorders.gon`  

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

---

### `TamperedGenes`
**Name:** Tainted Genes  
**Description:** At the end of each battle gain a random mutation. When you're downed, your corpse is destroyed.  
**Source:** `disorders.gon`  

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

---

### `SensoryOverloadFace`
**Name:** Sensory Overload  
**Description:** All but your face slot is locked. Your face item's effects are tripled!  
**Source:** `disorders.gon`  

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

---

### `SensoryOverloadTrinket`
**Name:** Sensory Overload  
**Description:** All but your trinket slot is locked. Your trinket's effects are tripled!  
**Source:** `disorders.gon`  

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

---

### `SensoryOverloadHead`
**Name:** Sensory Overload  
**Description:** All but your head slot is locked. Your head item's effects are tripled!  
**Source:** `disorders.gon`  

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

---

### `SensoryOverloadNeck`
**Name:** Sensory Overload  
**Description:** All but your neck slot is locked. Your neck item's effects are tripled!  
**Source:** `disorders.gon`  

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

---

### `SensoryOverloadWeapon`
**Name:** Sensory Overload  
**Description:** All but your weapon slot is locked. Your weapon's effects are tripled!  
**Source:** `disorders.gon`  

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

---

### `EternalYouth`
**Name:** Eternal Youth  
**Description:** You are a kitten... forever!
+1 [img:comfort], +1 [img:stimulation], +1 [img:appeal]  
**Source:** `disorders.gon`  

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

---

### `DejaVu`
**Name:** Deja Vu  
**Description:** 10% chance to cancel actions.
[s:.7]Deja Vu will go away when this cat returns to the house.[/s]  
**Source:** `disorders.gon`  

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

