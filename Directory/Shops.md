# Shops Directory

## File: `combat_shops.gon`

### `ItemShopSmall`
**Source:** `combat_shops.gon`  

```
ItemShopSmall {
    meta {
        movieclip Shop
        npc_script tracy_adventure_shop_script.gon
        delay_enable_tooltips true
        keeper 0
        shopkeeper_fights [
            test.lvl
        ]
    }

    item_rarity_costs {
        consumable_common 5
        consumable_uncommon 7
        consumable_rare 10
        consumable_very_rare 20
        common 7
        uncommon 10
        rare 20
        very_rare 40
    }

    item_groups {
        mandatory {
            Item {
                pool rare 
            }
        }
        levelup {
            LevelUp {
                cost 10
            }
        }
        pool {
            Item {
                pool shop_common
            }
        }
    }

    breakdown {
        levelup 1
        pool 2
    }

    stock_fill_order {
        //0 1 2
        // 3 4

        1 [1]
        2 [0 2]
        3 [1 3 4]
        4 [0 2 3 4]
        5 [1 0 2 3 4]
    }

    button_nav {
        //up down left right, x = no connection
        default {
            0 [x 3 x 1]
            1 [x 3 0 2]
            2 [x 4 1 x]
            3 [0 x x 4]
            4 [2 x 3 x]
        }
        //stock fill overrides
        3 { //if exactly 3 items in stock
            3 [1 x x 4]
            4 [1 x 3 x]
        }
    }
}
```

---

### `ItemShopMedium`
**Source:** `combat_shops.gon`  

```
ItemShopMedium {
    meta {
        movieclip Shop
        npc_script tracy_adventure_shop_script.gon
        delay_enable_tooltips true
        keeper 0
        shopkeeper_fights [
            test.lvl
        ]
    }

    item_rarity_costs {
        consumable_common 5
        consumable_uncommon 7
        consumable_rare 10
        consumable_very_rare 20
        common 7
        uncommon 10
        rare 20
        very_rare 40
    }

    item_groups {
        mandatory {
            Item {
                pool rare 
            }
        }
        levelup {
            LevelUp {
                cost 10
            }
        }
        pool {
            Item {
                pool shop_common
            }
        }
    }

    breakdown {
        levelup 1
        pool 3
    }

    stock_fill_order {
        //0 1 2
        // 3 4

        1 [1]
        2 [0 2]
        3 [1 3 4]
        4 [0 2 3 4]
        5 [1 0 2 3 4]
    }

    button_nav {
        //up down left right, x = no connection
        default {
            0 [x 3 x 1]
            1 [x 3 0 2]
            2 [x 4 1 x]
            3 [0 x x 4]
            4 [2 x 3 x]
        }
        //stock fill overrides
        3 { //if exactly 3 items in stock
            3 [1 x x 4]
            4 [1 x 3 x]
        }
    }
}
```

---

### `ItemShopLarge`
**Source:** `combat_shops.gon`  

```
ItemShopLarge {
    meta {
        movieclip Shop
        npc_script tracy_adventure_shop_script.gon
        delay_enable_tooltips true
        keeper 0
        shopkeeper_fights [
            test.lvl
        ]
    }

    item_rarity_costs {
        consumable_common 5
        consumable_uncommon 7
        consumable_rare 10
        consumable_very_rare 20
        common 7
        uncommon 10
        rare 20
        very_rare 40
    }

    item_groups {
        mandatory {
            Item {
                pool rare 
            }
        }
        levelup {
            LevelUp {
                cost 10
            }
        }
        pool {
            Item {
                pool shop_common
            }
        }
    }

    breakdown {
        levelup 1
        mandatory 1
        pool 3
    }

    stock_fill_order {
        //0 1 2
        // 3 4

        1 [1]
        2 [0 2]
        3 [1 3 4]
        4 [0 2 3 4]
        5 [1 0 2 3 4]
    }
    button_nav {
        //up down left right, x = no connection
        default {
            0 [x 3 x 1]
            1 [x 3 0 2]
            2 [x 4 1 x]
            3 [0 x x 4]
            4 [2 x 3 x]
        }
        //stock fill overrides
        3 { //if exactly 3 items in stock
            3 [1 x x 4]
            4 [1 x 3 x]
        }
    }
}
```

---

### `TreasureEasy`
**Source:** `combat_shops.gon`  

```
TreasureEasy {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool treasure_easy
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `TreasureHard`
**Source:** `combat_shops.gon`  

```
TreasureHard {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool treasure_hard
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Event_SmallShop`
**Source:** `combat_shops.gon`  

```
Event_SmallShop {
    meta {
        movieclip Shop
        npc_script tracy_adventure_shop_script.gon
        delay_enable_tooltips true
        keeper 0
        shopkeeper_fights [
            test.lvl
        ]
    }

    item_rarity_costs {
        consumable_common 5
        consumable_uncommon 7
        consumable_rare 10
        consumable_very_rare 20
        common 7
        uncommon 10
        rare 20
        very_rare 40
    }

    item_groups {
        pool {
            Item {
                pool shop_common
            }
        }
    }

    breakdown {
        pool 3
    }

    stock_fill_order {
        //0 1 2
        // 3 4

        1 [1]
        2 [0 2]
        3 [1 3 4]
        4 [0 2 3 4]
        5 [1 0 2 3 4]
    }
}
```

---

### `Event_RareShop`
**Source:** `combat_shops.gon`  

```
Event_RareShop {
    meta {
        movieclip Shop
        npc_script tracy_adventure_shop_script.gon
        delay_enable_tooltips true
        keeper 0
        shopkeeper_fights [
            test.lvl
        ]
    }

    item_rarity_costs {
        consumable_common 3
        consumable_uncommon 5
        consumable_rare 8
        consumable_very_rare 12
        common 5
        uncommon 8
        rare 10
        very_rare 15
    }

    item_groups {
        mandatory {
            Item {
                pool rare 
            }
        }
    }

    breakdown {
        mandatory 3
    }

    stock_fill_order {
        //0 1 2
        // 3 4

        1 [1]
        2 [0 2]
        3 [1 3 4]
        4 [0 2 3 4]
        5 [1 0 2 3 4]
    }
}
```

---

### `WaterShop`
**Source:** `combat_shops.gon`  

```
WaterShop {
    meta {
        movieclip Shop
        npc_script tracy_adventure_shop_script.gon
        delay_enable_tooltips true
        welcome_message welcome_water
        keeper 0
        shopkeeper_fights [
            test.lvl
        ]
    }

    item_rarity_costs {
        consumable_common 5
        consumable_uncommon 7
        consumable_rare 10
        consumable_very_rare 20
        common 7
        uncommon 10
        rare 20
        very_rare 40
    }

    item_groups {
        pool {
            Item {
                pool [WaterBottle_Full]
                cost 15
            }
            Item {
                pool [WaterBottle_Half]
                cost 10
            }
            Item {
                pool [WaterBottle_Empty]
                cost 5
            }
        }
    }

    breakdown {
        pool 5
    }
}
```

---

### `WaterShopCheap`
**Source:** `combat_shops.gon`  

```
WaterShopCheap {
    meta {
        movieclip Shop
        npc_script tracy_adventure_shop_script.gon
        delay_enable_tooltips true
        welcome_message welcome_water_cheap
        keeper 0
        shopkeeper_fights [
            test.lvl
        ]
    }

    item_rarity_costs {
        consumable_common 5
        consumable_uncommon 7
        consumable_rare 10
        consumable_very_rare 20
        common 7
        uncommon 10
        rare 20
        very_rare 40
    }

    item_groups {
        pool {
            Item {
                pool [WaterBottle_Full]
                cost 5
            }
            Item {
                pool [WaterBottle_Half]
                cost 3
            }
            Item {
                pool [WaterBottle_Empty]
                cost 1
            }
        }
        empty {
            Item {
                pool [WaterBottle_Empty]
                cost 1
            }
        }
    }

    breakdown {
        pool 4
        empty 1
    }
}
```

---

### `TreasureTutorial`
**Source:** `combat_shops.gon`  

```
TreasureTutorial {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [TutorialStick]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_SmallMoneyBag`
**Source:** `combat_shops.gon`  

```
Treasure_SmallMoneyBag {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [MoneyBag_Medium MoneyBag_Large]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_LargeMoneyBag`
**Source:** `combat_shops.gon`  

```
Treasure_LargeMoneyBag {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [MoneyBag_Huge]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_FurnitureBox`
**Source:** `combat_shops.gon`  

```
Treasure_FurnitureBox {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [FurnitureBox]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_MedFurnitureBox`
**Source:** `combat_shops.gon`  

```
Treasure_MedFurnitureBox {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [FurnitureBox FurnitureBox_Rare]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_RareFurnitureBox`
**Source:** `combat_shops.gon`  

```
Treasure_RareFurnitureBox {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [FurnitureBox_Rare]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_SmallMeteor`
**Source:** `combat_shops.gon`  

```
Treasure_SmallMeteor {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [SmallMeteor]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_LargeMeteor`
**Source:** `combat_shops.gon`  

```
Treasure_LargeMeteor {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [LargeMeteor]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_GlowingBone`
**Source:** `combat_shops.gon`  

```
Treasure_GlowingBone {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [GlowingBone]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_AncestorsSkull`
**Source:** `combat_shops.gon`  

```
Treasure_AncestorsSkull {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [AncestorsSkull AncestorsJaw AncestorsBones]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_IrradiatedObject`
**Source:** `combat_shops.gon`  

```
Treasure_IrradiatedObject {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [
                    IrradiatedObject_Burn
                    IrradiatedObject_Poison
                    IrradiatedObject_Bleed
                    IrradiatedObject_Fear
                    IrradiatedObject_Sleep
                    IrradiatedObject_Stun
                    IrradiatedObject_Charmed
                    IrradiatedObject_Weakness
                    IrradiatedObject_Bruise
                    IrradiatedObject_Confusion
                ]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

### `Treasure_AbilityNeedle`
**Source:** `combat_shops.gon`  

```
Treasure_AbilityNeedle {
    meta {
        movieclip TreasureRoom
        treasure_room true
    }

    item_groups {
        treasure {
            Item {
                pool [LearnAbility LearnAbility LearnPassive]
                cost 0
                mandatory true
            }
        }
    }

    breakdown {
        treasure 1
    }
}
```

---

## File: `jack_shop.gon`

### `JackShop`
**Source:** `jack_shop.gon`  

```
JackShop {
    meta {
        movieclip JackOffice
        house_shop true
    }

    item_groups {
        mandatory {
            Furniture {
            }
        }
    }

    breakdown {
        mandatory 6
    }

    stock_fill_order {
        //0 1 2
        //3 4 5

        1 [4]
        2 [3 5]
        3 [3 4 5]
        4 [1 3 4 5]
        5 [1 2 3 4 5]
        6 [0 1 2 3 4 5]
    }
    button_nav {
        //up down left right, x = no connection
        default {
            0 [x 3 x 1]
            1 [x 4 0 2]
            2 [x 5 1 x]
            3 [0 x x 4]
            4 [1 x 3 5]
            5 [2 x 4 x]
        }
        //stock fill overrides
        4 { 
            3 [1 x x 4]
            5 [1 x 4 x]
        }
        5 { 
            3 [1 x x 4]
        }
    }
}
```

---

## File: `organ_shop.gon`

### `OrganShop`
**Source:** `organ_shop.gon`  

```
OrganShop {
    meta {
        movieclip OrganOffice
        house_shop true
        pick_n 1
    }

    stock_fill_order {
        //3  1  4
        // 0   2

        1 [1]
        2 [0 2]
        3 [0 2 1]
        4 [0 2 3 4]
        5 [0 2 1 3 4]
    }

    button_nav {
        //up down left right, x = no connection
        default {
            0 [3 x x 2]
            1 [x 0 3 4]
            2 [4 x 0 x]
            3 [x 0 x 1]
            4 [x 2 1 x]
        }
        //stock fill overrides
        3 { //if exactly 3 items in stock
            0 [1 x x 2]
            2 [1 x 0 x]
        }
    }
}
```

---

## File: `tracy_house_shop.gon`

### `TracyHouseShop`
**Source:** `tracy_house_shop.gon`  

```
TracyHouseShop {
    meta {
        movieclip TracyOffice
        house_shop true
    }

    item_rarity_costs {
        consumable_common 10
        consumable_uncommon 14
        consumable_rare 20
        consumable_very_rare 40
        common 14
        uncommon 20
        rare 40
        very_rare 80
    }

    item_groups {
        guaranteed_food {
            Food {
                amount 10
                cost 5
                allow_duplicates true
            }
        }
        mostly_food {
            Food {
                amount 10
                cost 5
                weight 5
                allow_duplicates true
            }
            Item {
                pool tracy_houseshop_common
                weight 1
            }
        }
        consumable {
            Item {
                pool tracy_houseshop_common
            }
        }
        common_item {
            Item {
                pool tracy_houseshop_common_item
            }
        }
        item {
            Item {
                pool tracy_houseshop_item
            }
        }
    }

    breakdown { //0 to 4
        guaranteed_food 1
        mostly_food 2
        consumable 1
    }
    breakdown2 { //5 to 9
        guaranteed_food 1
        mostly_food 1
        consumable 1
        common_item 1
    }
    breakdown3 { //10 to 14
        guaranteed_food 1
        consumable 1
        common_item 2
    }
    breakdown4 { //15+
        guaranteed_food 1
        consumable 1
        common_item 2
        item 1
    }

    stock_fill_order {
        //0 1 2
        //3 4 5

        1 [4]
        2 [3 5]
        3 [3 4 5]
        4 [1 3 4 5]
        5 [1 2 3 4 5]
        6 [0 1 2 3 4 5]
    }
    button_nav {
        //up down left right, x = no connection
        default {
            0 [x 3 x 1]
            1 [x 4 0 2]
            2 [x 5 1 x]
            3 [0 x x 4]
            4 [1 x 3 5]
            5 [2 x 4 x]
        }
        //stock fill overrides
        4 { 
            3 [1 x x 4]
            5 [1 x 4 x]
        }
        5 { 
            3 [1 x x 4]
        }
    }
}
```

---

### `TracyHouseShopSpecialDay`
**Source:** `tracy_house_shop.gon`  

```
TracyHouseShopSpecialDay {
    meta {
        movieclip TracyOffice
        house_shop true
    }

    item_rarity_costs {
        consumable_common 10
        consumable_uncommon 14
        consumable_rare 20
        consumable_very_rare 40
        common 14
        uncommon 20
        rare 40
        very_rare 80
    }

    item_groups {
        guaranteed_food {
            Food {
                amount 10
                cost 5
                allow_duplicates true
            }
        }
        mostly_food {
            Food {
                amount 10
                cost 5
                weight 5
                allow_duplicates true
            }
            Item {
                pool tracy_houseshop_rare
                weight 1
            }
        }
        consumable {
            Item {
                pool tracy_houseshop_rare
            }
        }
        item {
            Item {
                pool tracy_houseshop_item
            }
        }
        common_item {
            Item {
                pool tracy_houseshop_common_item
            }
        }
    }

    breakdown { //0 to 4
        guaranteed_food 1
        mostly_food 1
        consumable 2
        item 1
    }
    breakdown2 { //5 to 9
        guaranteed_food 1
        mostly_food 1
        consumable 1
        common_item 1
        item 1
    }
    breakdown3 { //10 to 14
        guaranteed_food 1
        consumable 1
        common_item 2
        item 1
    }
    breakdown4 { //15+
        guaranteed_food 1
        consumable 1
        common_item 2
        item 2
    }

    stock_fill_order {
        //0 1 2
        //3 4 5

        1 [4]
        2 [3 5]
        3 [3 4 5]
        4 [1 3 4 5]
        5 [1 2 3 4 5]
        6 [0 1 2 3 4 5]
    }
    button_nav {
        //up down left right, x = no connection
        default {
            0 [x 3 x 1]
            1 [x 4 0 2]
            2 [x 5 1 x]
            3 [0 x x 4]
            4 [1 x 3 5]
            5 [2 x 4 x]
        }
        //stock fill overrides
        4 { 
            3 [1 x x 4]
            5 [1 x 4 x]
        }
        5 { 
            3 [1 x x 4]
        }
    }
}
```

---

