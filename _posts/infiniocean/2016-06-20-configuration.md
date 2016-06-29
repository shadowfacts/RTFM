---
layout: project-post
title: "Configuration"
date: 2016-06-21 10:33:18 -0400
category: infiniocean
project: infiniocean
project-name: "InfiniOcean"
---

The InfiniOcean configuration file is located at `config/shadowfacts/InfiniOcean/InfiniOcean.cfg`.

The configuration file is divided into four sections, one for each vanilla dimension and one more.

# General
The `general` section contains all the non-dimension specific settings for InfiniOcean.

- `force` is a boolean which, if `true`, will force the InfiniOcean world to be generated no matter what the user-specified world type is.
By default, force is disabled.

# Overworld
The `overworld` section contains all the settings related to InfiniOcean generation in the overworld.

- `bottomBlocks` is a list of strings identifying blocks that will be generated at the bottom of the overworld. This identifiers are in the format of `modid:name:meta` and specifying the metadata is optional.
By default, one layer of bedrock will be generated at the bottom and then 3 layers of gravel on top of that.

- `oceanHeight` is an integer specifying the maximum height of the ocean. Anything below this will be filled with water and anything above will be left as air.
By default, the ocean height is 64.

- `spawnStructure` is a string specifying the path to the spawn structure for the overworld relative to `config/shadowfacts/InfiniOcean/`. The file at this location will be parsed by the ShadowMC structure system and generated at the spawn point of the overworld.
By default, the spawn structure is `spawn-overworld.json` which is a 5 by 5 cobblestone platform

# Nether
The `nether` section contains all the settings related to InfiniOcean generation in the nether.

- `bottomBlocks` is a list of strings identifying blocks that will be generated at the bottom of the overworld. This identifiers are in the format of `modid:name:meta` and specifying the metadata is optional.
By default, one layer of bedrock will be generated at the bottom and then 3 layers of gravel on top of that.

- `enabled` is a boolean stating whether or not InfiniOcean nether generation is enabled.
By default, nether generation is enabled.

- `oceanHeight` is an integer specifying the maximum height of the ocean. Anything below this will be filled with lava and anything above will be left as air.
By default, the ocean height is 64.

- `spawnFortresses` is a boolean specifying whether or not to allow [Nether Fortresses](http://minecraft.gamepedia.com/Nether_fortress) to spawn in the nether.
By default, spawning fortresses is enabled.

- `spawnStructure` is a string specifying the path to the spawn structure for the nether relative to `config/shadowfacts/InfiniOcean/`. The file at this location will be parsed by the ShadowMC structure system and generated at the spawn point of the nether.
By default, the spawn structure is `spawn-nether.json` which is a 5 by 5 netherrack platform.

# End
The `end` section contains all the settings related to InfiniOcean generation in the End.

- `enabled` is a boolean stating whether or not InfiniOcean end generation is enabled.
By default, end generation is disabled.

- `spawnStructure` is a string specifying the path to the spawn structure for the end relative to `config/shadowfacts/InfiniOcean/`. The file at this location will be parsed by the ShadowMC structure system and generated at the spawn point of the end.
By default, the spawn structure is `spawn-end.json` which is a 5 by 5 end stone platform.