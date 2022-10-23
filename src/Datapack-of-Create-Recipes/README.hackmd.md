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
  "type": String,
  "ingredients": Array[Object],
  "results": Array[Object]
}
```

### `type`
| Machine            | Type Name               | ID                           | Additional Attributes                                  | Remark |
|--------------------|-------------------------|------------------------------|--------------------------------------------------------|--------|
| Encased Fan        | Bluk Haunting           | `create:haunting`            |                                                        |        |
| \                  | Bluk Washing            | `create:splashing`           |                                                        |        |
| Millstone          | Milling                 | `create:milling`             | `{"processingTime": Number}`                           | *1     |
| Curshing Wheel     | Crushing                | `create:crushing`            | `{"processingTime": Number}`                           | *1     |
| Mechanical Press   | Compacting              | `create:compacting`          | `{"heatRequirement": "superheated \| heated \| none"}` |        |
| \                  | Pressing                | `create:pressing`            |                                                        |        |
| Mechanical Mixer   | Mixing                  | `create:mixing`              | `{"heatRequirement": "superheated \| heated \| none"}` | *2     |
| Item Drain         | Item Draining           | `create:emptying`            |                                                        |        |
| Spout              | Filling by Spout        | `create:filling`             |                                                        |        |
| Mechanical Saw     | Sawing                  | `create:cutting`             | `{"processingTime": Number}`                           | *1     |
| Deployer           | Deploying               | `create:deploying`           |                                                        |        |
| (Red) Sand Paper   | Sandpaper Polishing     | `create:sandpaper_polishing` |                                                        |        |
| Hand               | Manual Item Application | `create:item_application`    |                                                        |        |
<!-- |  |  | `create:` |       | -->
<small>*1: processingTime\<Ticks></small>  
<small>*2: For ingredients: `{"return_chance": Number[Double]}`</small>

### `ingredients`
```json=
{
  "item | fluid | tag | fluidTag": String,
  "nbt": Object,
  "count | amount": Number // "item | tag": count, "fluid | fluidTag": amount
}
```

### `results`
```json=
{
  "item | fluid": String,
  "nbt": Object,
  "chance": Number,
  "count | amount": Number // "item": count, "fluid": amount
}
```

##  Mechanical Crafting
```json=
{
  "type": "create:mechanical_crafting",
  "pattern": Array[Shape with Keys],
  "key": Object[key: item | tag],
  "result": Object["item" only],
  "acceptMirrored": Boolen
}
```

## Recipe Sequence
```json=
{
  "type": "create:sequenced_assembly",
  "transitionalItem": Object["item" only],
  "sequence": Array[Step],
  "loops": Number
}
```

---

<small>Copyright © 2022 Mango Side Project. All rights reserved.</small>

{%hackmd @Luminous-Coder/dark-theme %}
<!-- the theme made by Luminous-Coder -->