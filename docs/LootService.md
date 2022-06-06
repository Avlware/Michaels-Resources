**How it works**

- [x]  Create Loot Containers
- [ ]  Bind Loot to Nodes
- [ ]  Setup Container GUI

[Download LootService]([https://octodex.github.com/images/minion.png](https://raw.githubusercontent.com/github-username/project/master/filename](https://github.com/PringleCPP/Michaels-Resources/blob/main/Downloadables/LootService.rbxm?raw=true) "download")

---

Step 1: Place LootService in ServerStorage as the client will not need to access it
Step 2: Customize your loot tables in the loot tables folder (Example:)
```lua
--// ["Item"] = Spawn percent (Singular item)
local LootTable = {
    ["10mm Pistol"] = 50,
    ["10mm Auto"] = 25,
    ["Combat Rifle"] = 15,
}
```
```lua
--// ["Item"] = Spawn percent (multiple items)
local LootTable = {
    Container1 = {
        Rarity = 50,
        Items = {
            ["10mm Pistol"] = 50,
            ["10mm Auto"] = 25,
            ["Combat Rifle"] = 15,
        }
    },
    Container2 = {
        Rarity = 50,
        Items = {
            ["10mm Pistol"] = 50,
            ["10mm Auto"] = 25,
            ["Combat Rifle"] = 15,
        }
    }
}```

Step 4: Initializing the script
```lua
--// Get the module (place this script in ScriptService)
local ServerStorage = game:GetService("ServerStorage")
local LootService = require(ServerStorage:WaitForChild("LootService"))

--// Run the function to initialize the module
LootService.Initialize()
```

**Notes**
This system is not complete and will only print out the items, this can be easily implemented into a node based generation system and will be in the future when I have open time, if you have scripting knowledge putting my weighted loot generation system into nodes is as easy as 1 2 3.

**Open Source** (C) Under Apache https://en.wikipedia.org/wiki/Apache_License (In short, you can use but credit is required somewhere even if its just in game code as long as it exists it is approved upon it is not required to be visible)
