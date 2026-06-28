# Mewgenics Mod Developer Documentation: Passives & Status Effects

While active abilities define what a class *does*, passives and status effects define *how the class bends the rules of the game*. This document covers the architecture of complex passive mechanics, reactive conditionals, and the status effect API.

## 1. Complicated Passives & Behaviors
In `classes.gon`, passives are split into `passive_pool` and `complicated_passives`. 

* **Standard Passives**: Simple stat bumps, basic immunities, or straightforward bonuses (e.g., `MaxHealthUp`, `FireImmunity`).
* **Complicated Passives**: Highly conditional behaviors that fundamentally change how the character interacts with the grid or abilities. These are hidden until the player achieves mastery in the class to prevent overwhelming new players.

**Example of a Complicated Passive Architecture:**
```gon
// FormChanger allows a character to dynamically swap their entire moveset
FormChanger {
    Default {
        passives {
            // Logic applied only while in Default form
            AbilityReaction {
                ability MyCounterAttackSpell
                ability_damage_only true
                only_when_not_your_turn true
            }
        }
    }
    EnragedForm {
        animation_suffix Enraged
        attack EnragedMelee // Completely overwrites the basic attack
        
        passives {
            Brace 99 // Takes 99 less damage
        }
    }
}
```

---

## 2. Conditional Effects & Reactions
The Mewgenics engine is built on a highly reactive event system. You do not write `if/else` code statements; instead, you utilize the engine's built-in conditional blocks.

### The `AbilityReaction` Template
One of the most powerful tools for modders is `AbilityReaction` or `ImmediateAbilityReaction`. This allows a character to automatically cast an ability without spending action points when specific conditions are met.

```gon
passives {
    AbilityReaction {
        ability TargetSpell   // The spell to cast automatically
        
        // Triggers
        only_when_not_your_turn true
        ability_damage_only true
        
        // Targeting overrides
        target_furthest_valid true
    }
}
```

### Health and Death Triggers
You can trigger behaviors based on a unit's lifecycle:
* **`AbilityHealthThreshold`**: Triggers an ability the moment the character's health crosses a specific threshold.
* **`DeathRattle`**: Triggers an ability immediately upon dying.
* **`DeathRattleRevive`**: Triggers an ability upon death, but prevents the death state entirely.

---

## 3. Getting Creative with Status Effects
Status effects (e.g., `Burn`, `Poison`, `Stun`) are modular state-changes applied via abilities or passives. You can manipulate how they interact using specific properties.

### Applying Statuses via Passives
You can permanently attach status effects to a character's basic attacks without creating an entirely new active ability using `AddStatusToBasicAttack`.

```gon
passives {
    AddStatusToBasicAttack {
        Poison 2  // Applies 2 stacks of Poison on every basic melee hit
    }
}
```

### Advanced Status Theorycrafting
You can combine status effects with custom abilities to create totally new mechanics:
1. **The Life-Drainer**: Use a `template_melee_attack` that deals low damage, but applies a custom `Bleed` status while simultaneously applying `Healing` to the caster using `statuses` block inside `damage_instance`.
2. **The Plague Bearer**: Create a passive that triggers an AOE `template_spell` on death (via `DeathRattle`), where the spell deals 0 damage but applies `Disorder` and `Poison` to every adjacent tile.

---

## 4. Key Properties & Keywords Dictionary
Here are specific properties the engine natively understands, which you can inject into character definitions or abilities to dramatically alter behavior:

* **`knockback_mode`**: Can be set to `character_to_tile`, `push_away_from_center`, etc., to control exactly how physics respond to an ability.
* **`move_block`**: Added to a character's properties (e.g., `move_block everything_even_when_dead`). Creates characters that act as permanent walls.
* **`dispersed_bonus_turns`**: Grants the character innate extra action points/turns.
* **`banned_elite_buffs`**: An array (e.g., `[Protected]`) that prevents the engine from randomly assigning specific modifiers if this character spawns as an elite enemy.
* **`corpse_health 0`**: Instantly removes the body upon death, preventing revival mechanics.
* **`AggroTargetIsLastEnemyThatDealtDamage 1`**: A passive property that forces the AI's targeting priority.
* **`SupportDieInsteadOfRun`**: Forces an AI character to play their death animation instead of attempting to flee when their morale breaks.
