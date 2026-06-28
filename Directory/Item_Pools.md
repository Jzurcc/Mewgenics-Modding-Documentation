# Item Pools Directory

## File: `bird_pools.gon`

### `blackbird_pool`
**Source:** `bird_pools.gon`  

```
blackbird_pool {
	chapter_common 1
	BagOfSeeds .3
	MagicSeed .3
	GlowingSeed .3
}
```

---

### `pigeon_pool`
**Source:** `bird_pools.gon`  

```
pigeon_pool {
	chapter_common 1
	BirdFeed .3
}
```

---

### `chicken_pool`
**Source:** `bird_pools.gon`  

```
chicken_pool {
	chapter_common 1
    Chicken 2
	WeirdEgg .3
	GoldenEgg .3
	RaptorEgg .1
}
```

---

### `dove_pool`
**Source:** `bird_pools.gon`  

```
dove_pool {
	chapter 1
	PeaceSymbol .3
	TieDyeBandana .3
	PeaceSymbolFacePaint .3
}
```

---

### `seagull_pool`
**Source:** `bird_pools.gon`  

```
seagull_pool {
	chapter 1
	BirdPoopHat .3
}
```

---

### `turkey_pool`
**Source:** `bird_pools.gon`  

```
turkey_pool {
	Turkey 2
	chapter 1
	WishBone .3
}
```

---

### `hummingbird_pool`
**Source:** `bird_pools.gon`  

```
hummingbird_pool {
	chapter_rare 1
	DeadHummingbird .3
}
```

---

### `raven_pool`
**Source:** `bird_pools.gon`  

```
raven_pool {
	chapter_rare 1
	RavenFeather .3
}
```

---

### `cherub_pool`
**Source:** `bird_pools.gon`  

```
cherub_pool {
	chapter_rare 1
	LostSoul .5
}
```

---

### `mutant_pool`
**Source:** `bird_pools.gon`  

```
mutant_pool {
	chapter_rare 1
	Parousworm .5
}
```

---

### `harpy_pool`
**Source:** `bird_pools.gon`  

```
harpy_pool {
	chapter_rare 1
	HarpysClaw .5
}
```

---

## File: `general_pools.gon`

### `basic_consumables`
**Source:** `general_pools.gon`  

```
basic_consumables {
    FoodMedium 5
    FoodBig 2
    Catnip 3
    CatnipBig 2
    pills 7 //since pills is weightless this should be an even chance of any pill
    Antidote 1
    Chicken .1
}
```

---

### `consumables`
**Source:** `general_pools.gon`  

```
consumables {
    basic_consumables 100
    consumables_consumable_common 50
    consumables_consumable_uncommon 35
    consumables_consumable_rare 15
    consumables_consumable_very_rare 1
}
```

---

### `food`
**Source:** `general_pools.gon`  

```
food {
    FoodMedium 1
    FoodBig 1
    Chicken .01
}
```

---

## File: `scaffolding.gon`

### `chapter`
**Source:** `scaffolding.gon`  

```
chapter {
    common 55
    uncommon 35
    rare 10
    very_rare 1
}
```

---

### `chapter_common`
**Source:** `scaffolding.gon`  

```
chapter_common {
    common 55
    uncommon 35
}
```

---

### `chapter_rare`
**Source:** `scaffolding.gon`  

```
chapter_rare {
    rare 15
    very_rare 1
}
```

---

### `treasure_easy`
**Source:** `scaffolding.gon`  

```
treasure_easy {
    uncommon 75
    rare 15
}
```

---

### `treasure_hard`
**Source:** `scaffolding.gon`  

```
treasure_hard {
    uncommon 60
    rare 40
    very_rare 2
}
```

---

### `shop_rare`
**Source:** `scaffolding.gon`  

```
shop_rare {
    rare 25
    very_rare 1
}
```

---

### `shop_common`
**Source:** `scaffolding.gon`  

```
shop_common {
    consumables 60
    common 50
    uncommon 35
    rare 1
    very_rare .01
}
```

---

### `any_chapter`
**Source:** `scaffolding.gon`  

```
any_chapter { //this will be changed later once "chapter" becomes actual chapter-specific items, need this for an event
    common 55
    uncommon 35
    rare 10
    very_rare 1
}
```

---

### `combat_reward_easy`
**Source:** `scaffolding.gon`  

```
combat_reward_easy {
    common 60
    uncommon 35
    rare 5
}
```

---

### `combat_reward_hard`
**Source:** `scaffolding.gon`  

```
combat_reward_hard {
    common 50
    uncommon 30
    rare 15
    very_rare 1
}
```

---

### `combat_reward_miniboss`
**Source:** `scaffolding.gon`  

```
combat_reward_miniboss {
    common 50
    uncommon 40
    rare 10
    very_rare 1
}
```

---

### `combat_reward_boss`
**Source:** `scaffolding.gon`  

```
combat_reward_boss {
    common 50
    uncommon 40
    rare 10
    very_rare 1
}
```

---

### `tracy_houseshop_common`
**Source:** `scaffolding.gon`  

```
tracy_houseshop_common {
    basic_consumables 90
    consumables 10
    shop_common 1
}
```

---

### `tracy_houseshop_common_item`
**Source:** `scaffolding.gon`  

```
tracy_houseshop_common_item {
    common 50
    uncommon 35
}
```

---

### `tracy_houseshop_rare`
**Source:** `scaffolding.gon`  

```
tracy_houseshop_rare {
    consumables 10
    shop_common 1
}
```

---

### `tracy_houseshop_item`
**Source:** `scaffolding.gon`  

```
tracy_houseshop_item {
    common 100
    uncommon 10
    rare 1
    very_rare .01
}
```

---

### `tracy_houseshop_bonusrare`
**Source:** `scaffolding.gon`  

```
tracy_houseshop_bonusrare {
    rare 15
    very_rare 1
}
```

---

### `current_chapter_common`
**Source:** `scaffolding.gon`  

```
current_chapter_common {
}
```

---

### `current_chapter_uncommon`
**Source:** `scaffolding.gon`  

```
current_chapter_uncommon {
}
```

---

### `current_chapter_rare`
**Source:** `scaffolding.gon`  

```
current_chapter_rare {
}
```

---

### `current_chapter_very_rare`
**Source:** `scaffolding.gon`  

```
current_chapter_very_rare {
}
```

---

### `chapter_specific_item`
**Source:** `scaffolding.gon`  

```
chapter_specific_item {
    current_chapter_common 55
    current_chapter_uncommon 35
    current_chapter_rare 10
    current_chapter_very_rare 1
}
```

---

### `common`
**Source:** `scaffolding.gon`  

```
common {
    general_common auto
    current_chapter_common auto
    current_chapter_common auto
    current_chapter_common auto
    current_chapter_common auto
    current_chapter_common auto
}
```

---

### `uncommon`
**Source:** `scaffolding.gon`  

```
uncommon {
    general_uncommon auto
    current_chapter_uncommon auto
    current_chapter_uncommon auto
    current_chapter_uncommon auto
    current_chapter_uncommon auto
    current_chapter_uncommon auto
}
```

---

### `rare`
**Source:** `scaffolding.gon`  

```
rare {
    general_rare auto
    current_chapter_rare auto
    current_chapter_rare auto
    current_chapter_rare auto
    current_chapter_rare auto
    current_chapter_rare auto
}
```

---

### `very_rare`
**Source:** `scaffolding.gon`  

```
very_rare {
    general_very_rare auto
    current_chapter_very_rare auto
    current_chapter_very_rare auto
    current_chapter_very_rare auto
    current_chapter_very_rare auto
    current_chapter_very_rare auto
}
```

---

