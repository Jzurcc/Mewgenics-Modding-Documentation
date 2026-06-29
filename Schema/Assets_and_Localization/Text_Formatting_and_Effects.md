---
title: "Text Formatting and Effects"
description: "Reference guide for BBCode-like tags used in localization strings"
---

# Text Formatting and Effects


<details open>
<summary><strong>Quick Navigation</strong></summary>

<table>
  <tr>
    <td width="22%"><strong>Core Entities & Combat</strong></td>
    <td><a href="../Core_Entities_and_Combat/Abilities_and_Spells.md">Abilities & Spells</a> • <a href="../Core_Entities_and_Combat/Characters_and_Bosses.md">Characters & Bosses</a> • <a href="../Core_Entities_and_Combat/Items_and_Equipment.md">Items & Equipment</a> • <a href="../Core_Entities_and_Combat/Passives_and_Statuses.md">Passives & Statuses</a> • <a href="../Core_Entities_and_Combat/Elite_Buffs.md">Elite Buffs</a> • <a href="../Core_Entities_and_Combat/Enemy_AI.md">Enemy AI</a> • <a href="../Core_Entities_and_Combat/Status_Effect_Keywords.md">Status Keywords</a></td>
  </tr>
  <tr>
    <td><strong>Engine Scripts & Logic</strong></td>
    <td><a href="../Engine_Scripts_and_Logic/Engine_LogicKeys.md">Logic Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_EventKeys.md">Event Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_DamagingKeys.md">Damaging Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_StatusAndPassiveKeys.md">Status & Passive Keys</a> • <a href="../Engine_Scripts_and_Logic/Engine_GlobalModifierKeys.md">Global Modifiers</a> • <a href="../Engine_Scripts_and_Logic/Math_Equations.md">Math Equations</a></td>
  </tr>
  <tr>
    <td><strong>Player Progression & Cats</strong></td>
    <td><a href="../Player_Progression_and_Cats/Cat_Classes.md">Cat Classes</a> • <a href="../Player_Progression_and_Cats/Cat_Mutations.md">Cat Mutations</a> • <a href="../Player_Progression_and_Cats/Custom_Cats.md">Custom Cats</a> • <a href="../Player_Progression_and_Cats/Injuries.md">Injuries</a> • <a href="../Player_Progression_and_Cats/Progression_Unlocks.md">Progression Unlocks</a> • <a href="../Player_Progression_and_Cats/Combat_Rewards.md">Combat Rewards</a></td>
  </tr>
  <tr>
    <td><strong>World, Maps & Events</strong></td>
    <td><a href="../World_Maps_and_Events/Events_and_Encounters.md">Events & Encounters</a> • <a href="../World_Maps_and_Events/House_and_Environment.md">House & Environment</a> • <a href="../World_Maps_and_Events/Map_Generation_and_Routing.md">Map Gen & Routing</a> • <a href="../World_Maps_and_Events/Furniture_and_Metaprogression.md">Furniture & Meta</a> • <a href="../World_Maps_and_Events/Shops.md">Shops</a> • <a href="../World_Maps_and_Events/Spawns_and_Enemy_Pools.md">Spawns & Enemy Pools</a> • <a href="../World_Maps_and_Events/Boss_Cutscene_Info.md">Boss Cutscenes</a> • <a href="../World_Maps_and_Events/NPC_Scripts.md">NPC Scripts</a></td>
  </tr>
  <tr>
    <td><strong>Assets & Localization</strong></td>
    <td><a href="../Assets_and_Localization/Audio_SFX_Dictionary.md">Audio SFX</a> • <a href="../Assets_and_Localization/Particles_and_VFX_Dictionary.md">Particles & VFX</a> • <a href="../Assets_and_Localization/Damage_Text_Styles.md">Damage Text</a> • <a href="../Assets_and_Localization/Localization_Guide.md">Localization Guide</a> • <a href="../Assets_and_Localization/Text_Formatting_and_Effects.md">Text Formatting</a> • <a href="../Assets_and_Localization/Strings.md">Strings</a></td>
  </tr>
  <tr>
    <td><strong>Reference & Meta</strong></td>
    <td><a href="../Reference_and_Meta/Enums.md">Enums</a> • <a href="../Reference_and_Meta/Arrays.md">Arrays</a> • <a href="../Reference_and_Meta/Item_Pools.md">Item Pools</a> • <a href="../Reference_and_Meta/Difficulties.md">Difficulties</a> • <a href="../Reference_and_Meta/Engine_Hidden_Passives_and_Statuses.md">Hidden Passives</a> • <a href="../Reference_and_Meta/Passive_Identifiers_Audit.md">Passive Audit</a> • <a href="../Reference_and_Meta/Engine_Uncategorized_Resources.md">Uncategorized Keys</a> • <a href="../Reference_and_Meta/Miscellaneous.md">Miscellaneous</a></td>
  </tr>
</table>

</details>

> **Context: `Strings` (Localization)**

Mewgenics uses a custom rich-text renderer for its localization strings. Whenever you are writing text (whether it's for an ability description, an event prompt, or NPC dialogue), you can use these special tags to animate text, scale it, insert icons, or dynamically inject variables.

These tags are primarily found in `data/text/combined.csv` or directly inside `quotes []` blocks.

---

## 1. Text Animations

Wrap your text in these tags to give them motion. Remember to close the tag with `[/a]`!

| Tag | Effect | Example Usage |
| :--- | :--- | :--- |
| `[a:pulse]` | The text slowly pulses in size. | `[a:pulse]Warning![/a]` |
| `[a:shake]` | The text shakes violently. | `[a:shake]IT BURNS![/a]` |
| `[a:wave]` | The text moves up and down in a sine wave. | `[a:wave]Wooooo...[/a]` |

---

## 2. Text Scaling

You can scale the size of the text (useful for fine-print or auxiliary info).

| Tag | Effect | Example Usage |
| :--- | :--- | :--- |
| `[s:X]` | Scales the text to `X` size (where 1.0 is normal). | `\[s:.7\](Can only be used once.)\[/s\]` |

---

## 3. Inline Icons

You can embed UI icons directly into the text using `[img:name]`. These are heavily used in ability and item descriptions.

| Category | Available Tags |
| :--- | :--- |
| **Stats** | `[img:str]`, `[img:spd]`, `[img:int]`, `[img:con]`, `[img:dex]`, `[img:lck]`, `[img:cha]` |
| **Combat** | `[img:health]`, `[img:shield]`, `[img:divineshield]` |
| **Cat Info** | `[img:male]`, `[img:female]`, `[img:retired]`, `[img:elite]`, `[img:champion]` |
| **House** | `[img:comfort]`, `[img:stimulation]` |
| **Other** | `[img:evolution]` |

*Example:* `Gain +2 [img:shield] and +1 [img:str].`

---

## 4. NPC Portrait Modifiers

When writing dialogue (e.g., in `NPC_Scripts` or Events), you can change the emotional state/portrait of the speaker by prepending the line with an `[m:state]` tag.

| Tag | Description |
| :--- | :--- |
| `[m:default]` | Resets to normal. |
| `[m:happy]`, `[m:veryhappy]` | Happy expressions. |
| `[m:angry]`, `[m:veryangry]` | Angry expressions. |
| `[m:sad]` | Sad expression. |
| `[m:shocked]` | Shocked or surprised. |
| `[m:questioning]`, `[m:pondering]` | Thinking or confused. |
| `[m:paranoid]`, `[m:scared]`, `[m:worried]` | Fearful expressions. |
| `[m:bored]`, `[m:spacedout]` | Disinterested. |
| `[m:mocking]`, `[m:winking]` | Cheeky or mocking. |
| `[m:grossedout]` | Disgusted. |
| `[m:whispering]` | Conspiratorial or quiet. |
| `[m:pointright]`, `[m:pointleft]`, `[m:pointdiagonal]` | Gesturing. |

*Example:* `[m:happy]Wow, you saved us! [m:angry]But you broke my vase!`

---

## 5. String Interpolation (Variables)

The engine can dynamically inject variables into strings. These are most commonly used in Event Prompts or dynamic item descriptions.

### Pronouns
These automatically map to the target's actual pronouns (he/she/they, him/her/them, etc.).

| Variable | Example Usage |
| :--- | :--- |
| `{he}` | `{he} runs fast.` *(He runs fast.)* |
| `{him}` | `Give it to {him}.` *(Give it to him.)* |
| `{his}` | `That is {his} item.` *(That is his item.)* |
| `{himself}` | `{he} hurt {himself}.` *(He hurt himself.)* |

### Entities
Used to dynamically insert the names of game objects or actors.

| Variable | Example Usage |
| :--- | :--- |
| `{catname}` | `{catname} tries to get into the bin!` |
| `{buddyname}` | `Your friend, {buddyname}, arrived.` |
| `{aux_cat_name}` | `Summon a ghost copy of {aux_cat_name}.` |
| `{applier}` | `Applied by {applier}.` |
| `{furniturename}` | `You placed the {furniturename}.` |
| `{itemname}` | `You found a {itemname}!` |
| `{ability}` | `Cast {ability}.` |
| `{passive}` | `Gained the {passive} trait.` |
| `{injury}` | `Suffered a {injury}.` |
| `{disorder}` | `Diagnosed with {disorder}.` |

### Numbers
Used to dynamically display calculated values like stacks or damage amounts.

| Variable | Example Usage |
| :--- | :--- |
| `{aux}` | `Heal {aux} HP.` |
| `{amount}` | `Deal {amount} damage.` |
| `{count}` | `Spawn {count} enemies.` |
| `{level}` | `Upgrades to Level {level}.` |
| `{stacks}` | `Applies {stacks} Poison.` |
| `{absstacks}` | `Remove {absstacks} debuffs.` |

### Dates and Time
Used primarily in calendar-based UI or events.

| Variable | Example Usage |
| :--- | :--- |
| `{year}` | `Year: {year}` |
| `{month}` | `Month: {month}` |
| `{weekday}` | `Today is {weekday}.` |
| `{day}` | `Day {day} of the journey.` |
| `{round}` | `Round {round} begins!` |
| `{rounds}` | `Survived for {rounds} rounds.` |

### Mechanics
Used to display complex systemic results.

| Variable | Example Usage |
| :--- | :--- |
| `{statchanges}` | `You feel different: {statchanges}` |
| `{reward}` | `You earned: {reward}` |
| `{questreward}` | `Quest complete! Received {questreward}.` |
| `{questdestination}` | `Travel to {questdestination}.` |
| `{percent}` | `Chance: {percent}%` |
