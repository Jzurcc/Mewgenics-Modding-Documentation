# Mewgenics Mod Developer Documentation: Localization & String Management

The most significant architectural difference between amateur mods and production-ready mods is how text is handled. Hardcoding dialogue, spell descriptions, or class names directly into `.gon` files is highly discouraged. 

The Mewgenics engine natively supports a full string localization system via `.csv` files.

## 1. The Hardcoded Approach (Anti-Pattern)

When rapidly prototyping, you might inject text directly into a class `meta` block:
```gon
// AVOID doing this for release versions!
meta {
    name "Vampire Class"
    description "Drains the blood of its enemies to restore health."
}
```
**Why this is an anti-pattern:**
1. You cannot translate the mod.
2. If you want to change the text later, you have to dig through complex ability arrays and logic files to find the string.

---

## 2. The Localization API (Best Practice)

The correct approach is to separate logic from presentation. 

### Step 1: Assign a String ID in `.gon`
Replace the hardcoded text with a unique string ID. 

```gon
// inside data/abilities/vampire_abilities.gon
meta {
    name "ABILITY_VAMPIRE_BITE_NAME"
    desc "ABILITY_VAMPIRE_BITE_DESC"
}
```

### Step 2: Create a `.csv` Dictionary
Inside your mod's `data/text/` folder, create a comma-separated values (`.csv`) file. Example: `data/text/my_mod_text.csv`.

The first line must define the keys and language columns (e.g., `KEY`, `en`, `ko`, `es`).

```csv
KEY,en
ABILITY_VAMPIRE_BITE_NAME,Blood Drain
ABILITY_VAMPIRE_BITE_DESC,Deals 5 melee damage and restores 2 health to the caster.
CAT_CLASS_VAMPIRE_NAME,The Vampire
CAT_CLASS_VAMPIRE_DESC,A creature of the night that sustains itself through combat.
```

When the game boots up, the engine maps every string ID in your `.gon` files to the actual text inside your `.csv` file.

---

## 3. Formatting Text in CSVs

Mewgenics allows for specific formatting rules within the translated strings inside the `.csv`.

* **Newlines**: You cannot use actual line breaks inside standard CSV cells without breaking the parsing. Instead, use specific formatting tags provided by the engine (if supported) or rely on the engine's auto-wrapping for long descriptions.
* **Keywords**: The engine automatically highlights specific terms if they match official mechanics (e.g., if you type "Poison" or "Bleed", the game will auto-link the tooltip for that mechanic). Ensure you capitalize these terms correctly according to the base game's `keyword_tooltips.gon`.

---

## 4. Theorycrafting: Dynamic Text
While standard descriptions are static, the engine handles numeric scaling dynamically through the UI. When you write `damage 5+bonus_melee_damage` in an ability's `damage_instance`, you **do not** need to write "Deals 5 (+ bonuses) damage" in your CSV. 

The game automatically injects the calculated damage value into the ability's UI panel during combat based on the cat's current stats. Keep your CSV descriptions focused on the *flavor* and the *mechanics* rather than hardcoding exact numbers that the engine scales dynamically.
