<h1 align="center">Lilia - Snippets Extension</h1>

<p align="center">
  <img src="https://i.imgur.com/yY3wT30.png" alt="Lilia Icon">
</p>
 
## Overview

The Lilia Snippets extension provides a set of code snippets for the Lilia programming language. Easily insert common code patterns and improve your development efficiency with this Visual Studio Code extension.

## Features

- **Snippet Library:** A collection of useful snippets for Lilia development.
- **Easy Insertion:** Quickly insert code snippets with just a few keystrokes.
- **Visual Studio Code Integration:** Seamlessly integrates with Visual Studio Code for a smooth coding experience.

## Usage

1. Install the Lilia Snippets extension from the Visual Studio Code Marketplace.
2. Open a LUA file.
3. Type the snippet prefix and press `Tab` to insert the snippet.

## Contributors

1. Fedox (Creator of the Helix version)
2. Samael (Re-did & implemented most hooks)
3. B0zy (Fixed several hooks & added new ones)

## Snippet Examples

### lilia.module

```lua
local MODULE = MODULE

MODULE.name = "NAME"
MODULE.desc = "DESCRIPTION"
MODULE.author = "AUTHOR"
MODULE.schema = "SCHEMA"
```

### lilia.item

```lua
ITEM.name = "NAME"
ITEM.desc = "DESCRIPTION"
ITEM.model = "MODEL"
ITEM.width = 1
ITEM.height = 1
ITEM.price = 1
ITEM.category = "CategoryName"

ITEM.iconCam = {pos = Vector(0, 0, 0), ang = Angle(0, 0, 0), fov = 70}

ITEM.functions.Option = {
    name = "OptionName",
    onClick = function(item)
        -- onClick functionality here
    end,
    onRun = function(item)
        -- onRun functionality here
        return false
    end,
    onCanRun = function(item)
        -- onCanRun checks here
    end,
}

function ITEM:getName()
    return self.name
end

function ITEM:getDesc()
    return self.desc
end
```

### lilia.item.outfit

```lua
ITEM.name = "NAME"
ITEM.desc = "DESCRIPTION"
ITEM.model = "MODEL"
ITEM.width = 1
ITEM.height = 1
ITEM.outfitCategory = "CATEGORY"
ITEM.newSkin = 1
ITEM.bodyGroups = {
    ["BODYGROUPNAME"] = 1,
}
ITEM.replacements = "MODEL"
```

### lilia.item.pacoutfit

```lua
ITEM.name = "NAME"
ITEM.desc = "DESCRIPTION"
ITEM.model = "MODEL"
ITEM.width = 1
ITEM.height = 1
ITEM.outfitCategory = "CATEGORY"
ITEM.pacData = {}
```

### lilia.item.bag

```lua
ITEM.name = "NAME"
ITEM.desc = "DESCRIPTION"
ITEM.model = "MODEL"
ITEM.width = 1
ITEM.height = 1
ITEM.invWidth = 1
ITEM.invHeight = 1
```

### lilia.item.ammo

```lua
ITEM.name = "NAME"
ITEM.desc = "DESCRIPTION"
ITEM.model = "MODEL"
ITEM.width = 1
ITEM.height = 1
ITEM.ammo = "AMMO"
ITEM.ammoAmount = 1
```

### lilia.item.weapon

```lua
ITEM.name = "NAME"
ITEM.desc = "DESCRIPTION"
ITEM.model = "MODEL"
ITEM.width = 1
ITEM.height = 1
ITEM.class = "WEAPONCLASS"
ITEM.weaponCategory = "CATEGORY"
```

### lilia.class

```lua
CLASS.name = "NAME"
CLASS.faction = FACTION_NAME
CLASS.isDefault = true

function CLASS:OnCanBe(client)
end

if (SERVER) then
    function CLASS:OnLeave(client)
    end

    function CLASS:OnSet(client)
    end

    function CLASS:OnSpawn(client)
    end
end

CLASS_NAME = CLASS.index
```

### lilia.faction

```lua
FACTION.name = "NAME"
FACTION.desc = "DESCRIPTION"
FACTION.color = Color(255, 255, 255, 255)
FACTION.isDefault = true
FACTION.models = {
	"MODEL",
}

function FACTION:OnGetDefaultName(client)
end

if (SERVER) then
    function FACTION:OnCharCreated(client, character)
    end

    function FACTION:OnSpawn(client)
    end
end

FACTION_NAME = FACTION.index
```
