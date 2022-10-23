---
title: Datapack of Create Recipes Docs
description: Create Datapack
tags: Public, Tutorial, Minecraft, Datapack
langs: en-us
---

# Datapack of Create Recipes

\> English < | [繁體中文]() | [简体中文]()

[TOC]

---

## Mod Loader Conditions

### Forge
```json=
{
  "conditions": [
    {
      "type": "forge:mod_loaded",
      "modid": ""
    }
  ]
}
```

### Fabric
```json=
{
  "fabric:load_conditions": [
    {
      "condition": "fabric:all_mods_loaded",
      "values": []
    }
  ]
}
```

## Base Format
```json=
{
  "type": String["create:{TYPE}"],
  "ingredients": Array[Object],
  "results": Array[Object]
}
```

### `TYPE`
| Machine            | Type Name               | ID                           | Additional Attributes                                  | Remark |
|--------------------|-------------------------|------------------------------|--------------------------------------------------------|--------|
| Encased Fan        | Bluk Haunting           | `create:haunting`            |                                                        |        |
| \                  | Bluk Washing            | `create:splashing`           |                                                        |        |
| Millstone          | Milling                 | `create:milling`             |                                                        |        |
| Curshing Wheel     | Crushing                | `create:crushing`            |                                                        |        |
| Mechanical Press   | Compacting              | `create:compacting`          | `{"heatRequirement": "superheated \| heated \| none"}` |        |
| \                  | Pressing                | `create:pressing`            |                                                        |        |
| Mechanical Mixer   | Mixing                  | `create:mixing`              | `{"heatRequirement": "superheated \| heated \| none"}` |        |
| Item Drain         | Item Draining           | `create:emptying`            |                                                        |        |
| Spout              | Filling by Spout        | `create:filling`             |                                                        |        |
| Mechanical Saw     | Sawing                  | `create:cutting`             |                                                        |        |
| Deployer           | Deploying               | `create:deploying`           |                                                        |        |
| Mechanical Crafter | Mechanical Crafting     | `create:mechanical_crafting` |                                                        |        |
| (Red) Sand Paper   | Sandpaper Polishing     | `create:sandpaper_polishing` |                                                        |        |
| Hand               | Manual Item Application | `create:item_application`    |                                                        |        |
<!-- |  |  | `create:` |       | -->

### `ingredients`
```json=
{
  "item | fluid | tag | fluidTag": String,
  "nbt": Object,
  "amount": Number
}
```

### `results`
```json=
{
  "item | fluid": String,
  "nbt": Object,
  "chance": Number,
  "amount": Number
}
```

## Recipe Sequence
```json=
{
  "type": "create:sequenced_assembly",
  "transitionalItem": { 
    "item": "" // Unfinished assembly items
  },
  "sequence": [], // Array[Step]
  "loops": 1 // Repetitions
}
```

---

<small>Copyright © 2022 Mango Side Project. All rights reserved.</small>

{%hackmd @Luminous-Coder/dark-theme %}
<!-- the theme made by Luminous-Coder -->