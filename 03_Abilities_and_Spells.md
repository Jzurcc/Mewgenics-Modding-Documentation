# Mewgenics Mod Developer Documentation: Ability & Spell Engineering

In Mewgenics, every active skill in combat is defined as an "Ability." This document outlines the official API for architecting custom abilities using the core `template` system.

## 1. The Core Schema
Every custom ability must be defined inside an `abilities.gon` file and should inherit from a base `template`.

```gon
MyCustomSpell {
    template template_spell
    
    // You override the template's default values here
    meta {
        name "SPELL_MY_SPELL_NAME"
        desc "SPELL_MY_SPELL_DESC"
    }

    cost {
        mana 2
    }

    damage_instance {
        damage 4
        type spell
        elements [fire]
    }
}
```

---

## 2. The Official Ability Templates
The engine provides 20+ master templates. By inheriting from these, you gain access to complex internal logic without having to write engine code.

### Combat Templates
* **`template_melee_attack`**: Standard adjacent attack. Cleaves/hits in a `line` by default.
* **`template_ranged_attack`**: Standard projectile attack. Requires line of sight.
* **`template_lobbed_attack`**: Fires a projectile over obstacles in an arc.
* **`template_spell`**: Standard ranged magic. Targets a tile, defaults to no knockback.
* **`template_melee_spell`**: Point-blank magical attack.
* **`template_dash_attack` / `template_trample_dash`**: Movement integrated with an attack line.
* **`template_laser`**: High-speed, piercing beam attack.
* **`template_spawn`**: Summons a new character/entity onto the grid.

### Utility & Movement Templates
* **`template_move`**: Standard walking action.
* **`template_teleport`**: Instantaneous movement ignoring pathing.
* **`template_swap`**: Swaps positions with a target tile.
* **`template_self_buff`**: Targets only the caster, applies status effects.
* **`template_targeted_status`**: Applies a status effect to a target without dealing damage.

---

## 3. The `cost` API
Determines the resource requirements to execute the ability.
```gon
cost {
    move_points 0  // Consumes movement (usually 0 for attacks)
    act_points 1   // Consumes the main action point
    mana 2         // Consumes mana (for spells)
    
    // Optional Flags
    infcantrip true // Can be used an infinite number of times per turn if you have the resources
}
```

---

## 4. The `target` API
This complex block handles the targeting logic, range, and Area of Effect (AOE).

```gon
target {
    target_mode tile  // Can be: tile, direction, none

    // Range Logic
    min_range 1
    max_range 4+bonus_range // Supports dynamic scaling
    
    // AOE Logic
    aoe_mode cross // Can be: standard, line, cross, custom
    min_aoe 1
    max_aoe 1

    // Restrictions
    restrictions must_have_line_of_sight
    knockback_mode character_to_tile
    can_multihit true
}
```

---

## 5. The `damage_instance` API
Defines what actually happens when the ability connects with a target.

```gon
damage_instance {
    damage 5+bonus_ranged_damage  // Base damage + scaling
    type ranged                   // Damage type (melee, ranged, spell, trample)
    elements [fire]               // Applies elemental modifiers

    // Applying status effects on hit
    statuses {
        Burn 1
        Stun 2
    }
}
```

---

## 6. Upgrades and Tiers (`variant_of`)
The game engine handles ability upgrades (Tier 1 -> Tier 2 -> Tier 3) seamlessly using the `variant_of` tag. You do not need to rewrite the entire ability for the upgraded version; it inherits everything from the base ability.

```gon
MyCustomSpell_2 {
    variant_of MyCustomSpell // Inherits everything from Tier 1

    // Override only what changes
    damage_instance {
        damage 8 // Increased damage for Tier 2
    }
}
```

---

## 7. Theorycrafting: Advanced Possibilities
Because `.gon` acts as a highly modular property schema, you can combine templates and parameters to create mechanics that do not exist in the base 12 classes.

**Untapped Potentials:**
1. **The Teleporting Strike**: Inherit from `template_teleport` but override its `damage_instance` block to deal heavy `melee` damage to the occupied tile upon arrival.
2. **The Laser Healer**: Inherit from `template_laser`, but set `damage` to `0` and inject `statuses { Healing 5 }` to fire a piercing beam that heals multiple allies in a line.
3. **The Global Sniper**: Inherit from `template_lobbed_attack` (ignoring line of sight) and set `max_range` to `99`. 
