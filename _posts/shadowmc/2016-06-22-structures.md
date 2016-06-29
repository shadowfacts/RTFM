---
layout: project-post
title: "Structures"
date: 2016-06-29 11:51:22 -0400
category: shadowmc
project: shadowmc
project-name: "ShadowMC"
---

ShadowMC provides a structure system for loading structures from JSON and generating them in the world.

The root JSON element contains a child for `blocks` which is a nested array 3 levels deep (one for each dimension, Y, X, and Z) which contains the information for the blocks. The first array is the Y plane, the second nested array is the x plane, and the third nested array is the z plane.

Each element in the third nested array is a block, the x-y-z coordinates for which are index of the second array for the X coordinate, the index of the first array for the Y coordinate, and the index of the third array for the Z coordinate.

Each block has 2 required properties, `id`, and `properties`. The `id` is the ID of the block in the form of `modid:name`. `properties` is an object which contains key-value pairs of property names to property values in the block state.

There are two additional optional properites, `lootId` and `inventory`. 

If `lootId` is present, the inventory of the block will be populated using the loot table specified by the `lootId` property. A list of vanilla loot tables can be found [here](https://minecraft.gamepedia.com/Loot_table#List_of_loot_tables).

If `inventory` is present, the inventory of the block will be populated using the entries in the `inventory` array. Each entry in the `inventory` array has three required properties, `item`, `amount`, and `slot`. `item` is the item to use in the form of `modid:name:meta` where `meta` is optional. `amount` is the number of that item to use (the stack size). `slot` is the slot in the inventory to place the stack in.

{% highlight json linenos %}
{
    "blocks": [
        [
            [
                {
                    "id": "minecraft:chest",
                    "properties": {
                        "facing": "south"
                    },
                    "lootId": "minecraft:chests/simple_dungeon"
                },
                {
                    "id": "minecraft:furnace",
                    "properties": {
                        "facing": "south"
                    },
                    "inventory": [
                        {
                            "item": "minecraft:iron_ore",
                            "amount": 7,
                            "slot": 0
                        }
                    ]
                },
                {
                    "id": "minecraft:diamond_block",
                    "properties": {}
                }
            ]
        ]
    ]
}
{% endhighlight %}

This structure represents a west-east line of three blocks. When looking at them from the south, the leftmost one is a chest which is facing south and has been populated from the `minecraft:chests/simple_dungeon` loot table. The middle one is a furnace that is also facing south that contains 7 Iron Ores in its input slot. The rightmost one is a diamond block.