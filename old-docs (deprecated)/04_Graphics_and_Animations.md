# Mewgenics Mod Developer Documentation: Visuals & Graphics API

Visual integration in Mewgenics modding is incredibly robust. You do not actually need to edit `.swf` files to create highly customized visual abilities or classes. The `.gon` engine provides an API to hook into existing animations, scale them, tint them, and combine particles.

## 1. Class-Level Animations (`alt_animations`)

When you create a custom class that inherits the standard `_CAT` movieclip, the engine expects standard animation labels (`idle`, `walk`, etc.). You can intercept these calls and reroute them to custom animations using the `alt_animations` array inside the class's `graphics` block.

```gon
graphics {
    // The base cat movieclip
    movieclip _CAT 

    // Rerouting the standard 'idle' call to 'werecatIdle'
    alt_animations [
        [idle, werecatIdle]
        [walk, werecatWalk]
        [ClassToNeutral, FighterToNeutral]
    ]
}
```

### The Custom `movieclip` Property (Advanced)
Some enemies in the base game (like the `HumanCat`) do **not** use the `_CAT` movieclip. They use their own dedicated symbol. If you are creating a class based on these characters, `alt_animations` will fail. You must override the base movieclip entirely:

```gon
graphics {
    movieclip HumanCat
    // No alt_animations needed, because it inherently uses its own idle/walk cycle.
}
```

---

## 2. Ability-Level Visuals

Inside an ability's `graphics` block, you define exactly what the character and the attack look like when executed.

```gon
MyCustomSpell {
    graphics {
        animation meow          // The animation the cat plays when casting
        projectile FireballProj // The projectile object to spawn
        particle Spike          // A particle effect to trigger on hit
        
        delay 0                 // Frames to wait before firing
        speed 15                // Projectile speed (if applicable)
        lob_height 0            // Arc height for lobbed attacks
    }
}
```

### Supported Graphic Parameters
* **`animation`**: The animation label triggered on the caster's movieclip. (e.g., `shoot`, `attack`, `meow`, `throwobject`).
* **`projectile`**: References a projectile entity. Look in `_unpacked/data/characters/particles2d.gon` or `particles.gon` for official projectile IDs.
* **`particle`**: References a particle effect triggered upon impact or casting.
* **`animation_suffix`**: An advanced property often used by form-changing passives to append a string to every animation call (e.g., if suffix is `Big`, `idle` becomes `idleBig`).

---

## 3. Form Changing and Suffixes

The base game handles massive visual overhauls (like Druid shapeshifting) using the `FormChanger` passive. This is an incredibly powerful API for modders.

```gon
passives {
    FormChanger {
        Default {
            passives { ... }
        }
        BigForm {
            // Appends "Big" to the end of ALL animation calls
            // Example: "attack" becomes "attackBig"
            animation_suffix Big
            
            attack BigSlam // Overrides the basic attack
        }
        initial_form Default
    }
}
```

---

## 4. Theorycrafting: Visual Compositing
Because you can stack `projectile` and `particle` tags, you can create completely new spell visuals. 

**Untapped Potentials:**
1. **The Poison Laser**: Use a standard `template_laser`, but inject `beam_clip greenlaser` and trigger a toxic `particle` on the target.
2. **Ghost Projectiles**: Utilize a fast-moving projectile but apply a heavy `lob_height` value on a `template_ranged_attack`, creating a bizarre, looping visual pathing that still adheres to standard line-of-sight targeting.
