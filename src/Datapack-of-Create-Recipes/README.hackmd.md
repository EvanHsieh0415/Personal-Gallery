---
title: Datapack of Create Recipes Docs
description: Create Datapack
tags: Public
langs: en-us
---

# Datapack of Create Recipes

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
| Machine     | Type Name     | ID                  | other |
|-------------|---------------|---------------------|-------|
| Encased Fan | Bulk Blasting | `create:blasting` ||
|  | Bluk Haunting | `create:haunting` ||
|  | Bluk Smoking | `create:smoking` ||
|  | Bluk Washing | `create:splashing` ||
| Millstone | Milling | `create:milling` ||
| Curshing Wheel | Crushing | `create:crushing` ||
| Mechanical Press | Compacting | `create:compacting` ||
|  | Pressing | `create:pressing` ||
| Mechanical Mixer | Mixing | `create:mixing` ||
| Item Drain | Item Draining | `create:emptying` ||
| Spout | Filling by Spout | `create:filling` ||
|  |  | `create:` ||
|  |  | `create:` ||
|  |  | `create:` ||
|  |  | `create:` ||
|  |  | `create:` ||
|  |  | `create:` ||
|  |  | `create:` ||
|  |  | `create:` ||
|  |  | `create:` ||
|  |  | `create:` ||
|  |  | `create:` ||


---

<small>Copyright © 2022 Mango Side Project. All rights reserved.</small>

{%hackmd @Luminous-Coder/dark-theme %}
<!-- the theme made by Luminous-Coder -->