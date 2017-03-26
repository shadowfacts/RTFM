---
layout: project-post
title: "Configuration"
date: 2016-06-21 16:11:27 -0400
category: ye-olde-tanks
project: ye-olde-tanks
project-name: "Ye Olde Tanks"
---

# **`autoOutputBottom`**
If `true`, the Barrel will automatically output fluid to the handler below it, if there is one.
By default, this is `true`.

# **`barrelCapacity`**
The capacity, in milibuckets (1 bucket is 1000 milibuckets), of the Barrel.
By default, this is `55000` millibuckets.

# **`drainFromAnySide`**
If `true`, pipes will be able to drain the barrel from any side. Otherwise, the barrel will only be drainable from the bottom.
By default, this is `false`.

# **`fillFromAnySide`**
If `true`, pipes will be able to fill the barrel from any side. Otherwise, the barrel will only be fillable from the top if the lid is off.
By default, this is `false`.

# **`obsidianBarrelCapacity`**
The capacity, in millibuckets, of the Obsidian Barrel.
By default, this is `110000` millibuckets.

# **`renderFluid`**
If `true`, the client will render the fluid inside the barrel in the world. Otherwise, nothing will be rendered inside the barrel.
By default this is `false`.