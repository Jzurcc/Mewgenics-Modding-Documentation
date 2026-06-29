# Items and Passives/Passive Pools Directory

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

## File: `passive_pools.gon`

### `all_disorders`
**Source:** `passive_pools.gon`  

```
all_disorders [
    Rabies
    Boils
    Depression
    BrokenLimb
    WrenchedNeck
    Declawed
    HeadTrauma
    DeepCut
    PuncturedEye
    OCD
    Distemper
    BrainDamage
    SeveredThumb
    PTSD
    IBS
    Dyskinesia
    Anemia
    Empath
    Infestation
    Leprosy
    ASRFight
    ASRFlight
    BloodFrenzy
    Shunned
    Dysentery
    Anxiety
    Kamikazee
    Traumatophobia
    StockholmSyndrome
    ViolentOutbursts
    GamblingAddict
    Scleroderma
    Pacifist
    Gigachad
    ImposterSyndrome
    Vegan
    FrozenKnee
    SchrodingerDisorder
    ScalyScabs
    FattyLiver
    CommonCold
    Pox
    Psychosis
    Necrosis
    Touched //unique
    Charred
    Invincible
    ExplosiveGas
    Toxoplasmosis
    Ebola
    Fidgety
    Narcolepsy
    Paranoia
    EatingDisorder
    Gastritis
    Hypomania
    Hypersomnia
    KidneyStones
    Cancer
    Stinky
    Incontinence
    Fossilized
    Triskaidekaphobia
    Tourettes
    SleepParalysis
    Diabetes
    Bipolar
    Soulless //unique
    Premonitions
    PillPopper
    BorrowedTime
    Brave
    Scatological
    Cannibal
    CrohnsDisease
    Pica
    FelineAids
    Dyslexia
    Covid
    Flu
    BirdFlu
    Nudist
    Elephantiasis
    Sociopathy
    SkillShare_Disorder
    Schizophrenia
    Lycanthropy
    WobblyCat
    Singleton
    Insomnia
    Phony
    AcidReflux
    SpontaneousCombustion
    TheHunger
    Paralyzed
    GlassBones
    ADHD
    IntestinalProlapse
    //Autism //birth defects that arent in the general pool
    //Albinism
    //Dwarfism
    //PrimordialDwarf
]
```

---

### `birth_defects`
**Source:** `passive_pools.gon`  

```
birth_defects [ //not all birth defects need to be put in the all_disorders category (these ones can only be acquired if a cat is born with them)
    Autism
    Tourettes
    Narcolepsy
    Albinism
    Diabetes
    Dyslexia
    Dwarfism
    PrimordialDwarf
    WobblyCat
    GlassBones
    Anemia
	SpinaBifida
	WilliamsSyndrome
	SavantSyndrome
	Tachysensia
	DownsSyndrome
	Depression
    OCD
	Tourettes
	Bipolar
	Schizophrenia
    ADHD
]
```

---

### `mental_disorders`
**Source:** `passive_pools.gon`  

```
mental_disorders [
    Depression
    OCD
    PTSD
    Dyskinesia
    Empath
    ASRFight
    ASRFlight
    BloodFrenzy
    Shunned
    BrainDamage
    Anxiety
    Traumatophobia
    StockholmSyndrome
    ViolentOutbursts
    GamblingAddict
    Pacifist
    ImposterSyndrome
    Vegan
    Psychosis
    Fidgety
    Narcolepsy
    Paranoia
    EatingDisorder
    Hypomania
    Hypersomnia
    Triskaidekaphobia
    Tourettes
    SleepParalysis
    Bipolar
    Premonitions
    Brave
    Scatological
    Cannibal
    Pica
    Dyslexia
    Nudist
    Sociopathy
    SkillShare_Disorder
    Schizophrenia
    Lycanthropy
    Singleton
    Insomnia
    Phony
    ADHD
]
```

---

### `physical_disorders`
**Source:** `passive_pools.gon`  

```
physical_disorders [
    BrokenLimb
    WrenchedNeck
    Declawed
    HeadTrauma
    DeepCut
    PuncturedEye
    BrainDamage
    SeveredThumb
    IBS
    Dysentery
    Infestation
    Kamikazee
    Scleroderma
    Gigachad
    FrozenKnee
    SchrodingerDisorder
    ScalyScabs
    FattyLiver
    Charred
    Invincible
    Gastritis
    KidneyStones
    Stinky
    Incontinence
    Fossilized
    SleepParalysis
    Diabetes
    CrohnsDisease
    FelineAids
    Lycanthropy
    WobblyCat
    AcidReflux
    SpontaneousCombustion
    Paralyzed
    GlassBones
    IntestinalProlapse
]
```

---

### `diseases`
**Source:** `passive_pools.gon`  

```
diseases [
    Rabies
    Boils
    Distemper
    Infestation
    IBS
    Dysentery
    Scleroderma
    CommonCold
    Pox
    Necrosis
    Leprosy
    ExplosiveGas
    Toxoplasmosis
    Ebola
    Gastritis
    Cancer
    FelineAids
    Covid
    Flu
    BirdFlu
    Elephantiasis
    Lycanthropy
]
```

---

### `magic_disorders`
**Source:** `passive_pools.gon`  

```
magic_disorders [
    Touched
    Triskaidekaphobia
    Soulless
    Premonitions
    BorrowedTime
    TheHunger
]
```

---

### `forbidden_spell_consequences`
**Source:** `passive_pools.gon`  

```
forbidden_spell_consequences [
    Depression
    Anemia
    Kamikazee
    Necrosis
    PTSD
]
```

---

### `forbidden_spell_consequences_crippling`
**Source:** `passive_pools.gon`  

```
forbidden_spell_consequences_crippling [
    Psychosis
    BorrowedTime
    Schizophrenia
    Insomnia
    TheHunger
]
```

---

### `stomach_disorders`
**Source:** `passive_pools.gon`  

```
stomach_disorders [
    Dysentery
    IBS
    ExplosiveGas
    Gastritis
    CrohnsDisease
    AcidReflux
]
```

---

### `low_hygeine_in_house_disorders`
**Source:** `passive_pools.gon`  

```
low_hygeine_in_house_disorders [
    Boils
    Depression
    OCD
    PTSD
    IBS
    Infestation
    Leprosy
    Dysentery
    Anxiety
    StockholmSyndrome
    CommonCold
    Pox
    Necrosis
    ExplosiveGas
    Toxoplasmosis
    Paranoia
    EatingDisorder
    Gastritis
    KidneyStones
    Cancer
    Stinky
    Incontinence
    PillPopper
    Scatological
    Cannibal
    CrohnsDisease
    Pica
    Covid
    Flu
    BirdFlu
    AcidReflux
]
```

---

### `Steven_disorders`
**Source:** `passive_pools.gon`  

```
Steven_disorders [
	Invincible
	Paranoia
	Triskaidekaphobia
	Autism
	Bipolar
	Premonitions
	Dyslexia
	Schizophrenia
	Insomnia
	ADHD
]
```

---

### `Crazy_disorders`
**Source:** `passive_pools.gon`  

```
Crazy_disorders [
	Rabies
	PTSD
	ASRFight
	ASRFlight
	BloodFrenzy
	Anxiety
	Kamikazee
	ViolentOutbursts
	Paranoia
	Hypomania
	Cannibal
]
```

---

