---
title: "Text Formatting and Effects"
description: "Reference guide for BBCode-like tags used in localization strings"
---

# Text Formatting and Effects

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
| `[s:X]` | Scales the text to `X` size (where 1.0 is normal). | `[s:.7](Can only be used once.)[/s]` |

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
