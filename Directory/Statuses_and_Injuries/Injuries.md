# Statuses and Injuries/Injuries Directory

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

## File: `injuries.gon`

### `str`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_BROKENPAW`: "Broken Paw"

```
str {
    text "INJURY_NAME_BROKENPAW"
    id 0

    stats {
        str -1
    }

    scars {
        arms [10 20]
    }

    alt_animations [
        [dying, brokenPaw]
        [dead, brokenPawLoop]
        [deadhit, brokenPawHit]
        [weak, brokenPawIdle]
        [walk, brokenPawWalk]
        //hit_brokenPaw
    ]

    deathsound Injury_BrokenPaw
}
```

---

### `dex`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_TORNTENDON`: "Torn Tendon"

```
dex {
    text "INJURY_NAME_TORNTENDON"
    id 1

    stats {
        dex -1
    }

    scars {
        limbs [21 31]
    }

    alt_animations [
        [dying, dislocatedShoulder]
        [dead, dislocatedShoulderLoop]
        [deadhit, dislocatedShoulderHit]
        [weak, dislocatedShoulderIdle]
        [walk, dislocatedShoulderWalk]
        //hit_brokenShoulder
    ]

    deathsound Injury_TornTendon
}
```

---

### `con`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_BROKENRIB`: "Broken Rib"

```
con {
    text "INJURY_NAME_BROKENRIB"
    id 2

    stats {
        con -1
    }

    scars {
        body [2 9]
    }

    alt_animations [
        [dying, intestinalProlapse]
        [dead, intestinalProlapseLoop]
        [deadhit, intestinalProlapseHit]
        //hit_brokenRib
    ]

    deathsound Injury_BrokenRib
}
```

---

### `int`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_CONCUSSION`: "Concussion"

```
int {
    text "INJURY_NAME_CONCUSSION"
    id 3

    stats {
        int -1
    }

    scars {
        head [23 33]
    }

    alt_animations [
        [dying, concussion]
        [dead, concussionLoop]
        [deadhit, concussionHit]
        //hit_concussion
    ]

    deathsound Injury_Concussion
}
```

---

### `cha`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_DISFIGURED`: "Disfigured"

```
cha {
    text "INJURY_NAME_DISFIGURED"
    id 4

    stats {
        cha -1
    }

    scars {
        head [23 33]
    }

    alt_animations [
        [dying, disfigured]
        [dead, disfiguredLoop]
        [deadhit, disfiguredHit]
        //hit_disfigured
    ]

    deathsound Injury_Disfigured
}
```

---

### `spd`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_BROKENLEG`: "Broken Leg"

```
spd {
    text "INJURY_NAME_BROKENLEG"
    id 5

    stats {
        spd -1
    }

    scars {
        legs [2 9]
    }

    alt_animations [
        [dying, brokenLeg]
        [dead, brokenLegLoop]
        [deadhit, brokenLegHit]
        [weak, brokenLegIdle]
        [walk, brokenLegWalk]
        //hit_brokenLeg
    ]

    deathsound Injury_BrokenLeg
}
```

---

### `lck`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_JINXED`: "Jinxed"

```
lck {
    text "INJURY_NAME_JINXED"
    id 6

    stats {
        lck -1
    }

    scars {
        head [15 22]
    }

    alt_animations [
        [dying, cursed]
        [dead, cursedLoop]
        [deadhit, cursedHit]
        //hit_jinxed
    ]

    deathsound Injury_Cursed
}
```

---

### `burned`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_IMMOLATED`: "Immolated"

```
burned {
    text "INJURY_NAME_IMMOLATED"
    id 7

    stats {
        cha -1
        lck -1
    }

    scars {
        body [16 25]
        head [34 41]
    }

    deathsound Injury_Burn
}
```

---

### `bleeding`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_EXSANGUINATED`: "Exsanguinated"

```
bleeding {
    text "INJURY_NAME_EXSANGUINATED"
    id 8

    stats {
        str -1
        dex -1
    }

    deathsound Injury_Bleed
}
```

---

### `poisoned`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_POISONED`: "Poisoned"

```
poisoned {
    text "INJURY_NAME_POISONED"
    id 9

    stats {
        con -1
        int -1
    }

    deathsound Injury_Poison
}
```

---

### `cursed`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_CURSED`: "Cursed"

```
cursed { //copy of "lck" injury except says "Cursed" instead of "Jinxed," and is -2 luck.
    text "INJURY_NAME_CURSED"
    id 10

    stats {
        lck -2
    }

    scars {
        head [15 22]
    }

    alt_animations [
        [dying, cursed]
        [dead, cursedLoop]
        [deadhit, cursedHit]
    ]

    deathsound Injury_Cursed
}
```

---

### `radiated`
**Source:** `injuries.gon`  

**Localization Strings:**
- `INJURY_NAME_RADIATED`: "Radiated"

```
radiated { //TODO: made this for an event (EliphantsFoot) but it doesn't have unique art yet
    text "INJURY_NAME_RADIATED"
    id 11
    
    scars {
        body [26 30] //copied from burned injury
        head [42 46]
    }

    stats {
        con -1
    }
    
    deathsound Injury_Burn
}
```

---

### `fade`
**Source:** `injuries.gon`  

```
fade {
    text ""
    id -1

    alt_animations [
        [dying, poofOutOfExistance]
        [dead, blank]
    ]

    deathsound Shade_Fade
}
```

---

