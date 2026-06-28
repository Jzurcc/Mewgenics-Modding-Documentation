# Injuries Directory

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

