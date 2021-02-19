#Result

!!! danger
    Use this script under your own risk.
        This script was made while coding the module (It can have errors)

---

###Example script of the module.
```lua
local cmdUtil = require(game:GetService("ReplicatedStorage"):FindFirstChild('Command'))

cmdUtil.newrole({
	["color"] = Color3.fromRGB(255, 255, 0),
	["name"] = "Owner",
	["permissions"] = {
		"OPEN_COMMAND_BAR"
	}
})

game.Players.PlayerAdded:Connect(function(player)
	if player.Name == "RiverCryptz" then
		wait(2)
		cmdUtil.players[player.Name].roles.add("Owner").catch(function(err)
			warn(err)
		end)
	end
end)

cmdUtil.listen(
	{
		["command"] = "print",
		["callback"] = function(cmd)
			
			cmdUtil.send("message", {
				player = cmd.caller,
				text = "5 seconds left to receive a reply",
				color = "yellow"
			})
			
			cmdUtil.await("response", {
				["command"] = cmd,
				["timeout"] = 5,
				["callback"] = function(message)
					print("reply: "..message)
				end
			})
			
		end
	}
).catch(function(err)
	-- NOTE: If you use the .catch method on any function that have callbacks, don't use .catch inside of any callback function.
	print("ERROR: "..err)
end)
```