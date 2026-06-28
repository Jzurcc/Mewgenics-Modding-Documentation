# Mewgenics Mod Developer Documentation: Class Architecture API

This document outlines the master schema for defining a custom Class in Mewgenics. It breaks down the internal structure of the `classes.gon` format and the API expected by the game engine.

## The Master Class Schema

Every class in Mewgenics is defined as a root object in `classes.gon`. A fully realized class definition is constructed using several distinct data blocks.

```gon
MyCustomClass {
    meta { ... }
    graphics { ... }
    
    // (Optional) Hardcoded starting items or passives
    innate_items { ... }
    innate_passives { ... }

    // Core combat definitions
    attack_pool [ ... ]
    ability_pool [ ... ]
    complicated_abilities [ ... ]
    starter_abilities [ ... ]
    ability_groups { ... }

    // Passive skill tree
    passive_pool [ ... ]
    complicated_passives [ ... ]

    // Stat definitions
    stat_mods { ... }
    levelup_stats [ ... ]
}
```

---

## 1. Metadata and UI (`meta`)
The `meta` block defines the UI text for the class selection screen.

```gon
meta {
    name "CAT_CLASS_MYCLASS_NAME"
    description "CAT_CLASS_MYCLASS_DESC"
}
```
> [!TIP]
> Do not hardcode strings here. Use localization IDs mapping to your `data/text/*.csv` file to support multi-language modding.

---

## 2. Visuals and Identity (`graphics`)
Defines the palette, animations, and UI portraits. 

```gon
graphics {
    palette 54 // Base color index
    
    // Maps base game animations or custom movieclip labels
    alt_animations [
        [idle, werecatIdle]
        [ClassToNeutral, FighterToNeutral]
        [ClassFromNeutral, FighterFromNeutral]
        [StartTurn, FighterStartTurn]
        [Victory, fighterVictory]
    ]

    portrait_face fighter_portrait
}
```

---

## 3. Innate Overrides (Advanced Potential)
You can inject permanent items or passives into a class. The base game uses this for the Tinkerer and Monk classes.
```gon
innate_items {
    weapon ButcherHook
}

innate_passives {
    SpawnOnBattleStart Crow
    // Or even complex logic blocks
    TinkererBasicAttackSwitching {
        craft_ability TinkererCraft
        throw_ability TinkererThrow
    }
}
```

---

## 4. The Ability Pools
This section dictates exactly what active abilities the class has access to during gameplay.

* **`attack_pool`**: Contains the basic, zero-cost cantrip attack the class defaults to (e.g., `BasicMelee_Fighter`).
* **`ability_pool`**: The master array of every spell/ability the class can ever learn. A standard base class contains exactly 60 abilities here.
* **`complicated_abilities`**: A sub-array of abilities from the pool that are flagged as "complex". These are hidden from the player until they level up the class enough to unlock advanced mechanics.
* **`starter_abilities`**: An array of 10 abilities. The game pulls from this list when generating a Level 1 cat of this class.

### `ability_groups`
The game engine requires you to categorize your `ability_pool` into distinct strategic buckets for UI and AI sorting:
```gon
ability_groups {
    attack [ ... ]  // Primarily damage-dealing
    defense [ ... ] // Shields, healing, traps
    move [ ... ]    // Movement, dashes, teleports
    misc [ ... ]    // Status effects, utility
}
```

---

## 5. The Passive Pools
Similar to abilities, this defines the passive skill tree.

* **`passive_pool`**: The master array of all passive skills the class can learn (standard base game classes have 25 passives).
* **`complicated_passives`**: Passives hidden behind class mastery progression.

---

## 6. Stat Modifiers and Scaling
Defines base stats and how the class scales upon leveling up.

* **`stat_mods`**: Static integer modifiers applied to the base Level 1 cat stats.
* **`levelup_stats`**: An array dictating which stats this class prioritizes when leveling up.

```gon
stat_mods {
    str 2   // +2 Base Strength
    spd 1   // +1 Base Speed
    int -1  // -1 Base Intelligence
}

levelup_stats [str con spd] // Prioritizes Strength, Constitution, and Speed on level up
```
