---
title: Datapack of Create Recipes Docs
description: Create Datapack
tags: Public
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
  "type": "create:{xxx}",
  "ingredients": [],
  "results": []]
}
```

### `Type`
| Machine            | Type Name               | ID                           | other |
|--------------------|-------------------------|------------------------------|-------|
| Encased Fan        | Bluk Haunting           | `create:haunting`            |       |
| \                  | Bluk Washing            | `create:splashing`           |       |
| Millstone          | Milling                 | `create:milling`             |       |
| Curshing Wheel     | Crushing                | `create:crushing`            |       |
| Mechanical Press   | Compacting              | `create:compacting`          |       |
| \                  | Pressing                | `create:pressing`            |       |
| Mechanical Mixer   | Mixing                  | `create:mixing`              |       |
| Item Drain         | Item Draining           | `create:emptying`            |       |
| Spout              | Filling by Spout        | `create:filling`             |       |
| Mechanical Saw     | Sawing                  | `create:cutting`             |       |
| Deployer           | Deploying               | `create:deploying`           |       |
| Mechanical Crafter | Mechanical Crafting     | `create:mechanical_crafting` |       |
| (Red) Sand Paper   | Sandpaper Polishing     | `create:sandpaper_polishing` |       |
| Hand               | Manual Item Application | `create:item_application`    |       |
<!-- |  |  | `create:` |       | -->

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