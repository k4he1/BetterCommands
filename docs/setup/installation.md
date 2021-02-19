<h1>Installation</h1>
-----------
## Common Method
<a href="https://www.roblox.com/library/6413343401/BetterCommand" 
style="
color: orange
"
target="_blank">
    > Click here to get the module
</a>
```lua
local cmdUtil = require(path)

-- CODE
```
???+ tip
    This is the most stable and easy method of installation. (Client & server friendly)
--------
## Loading via ID
```lua
local cmdUtil = game:GetService("InsertService"):LoadAsset(6413343401)
cmdUtil.Parent = game:GetService("ReplicatedStorage")
cmdUtil = require(cmdUtil)

-- CODE
```

!!! warning 
    This method only can be used from the server-side.