#Role API
Roles are useful for commands, right?

???+ warning
    Roles are not removable (There's no `.removerole()` function.)

---

##.newrole() `usage`

| Function Arguments |
|-|
| properties `<table>` |

| Properties | |
|-| |
| color `<color3>` | Role color (optional & **useless for now**) |
| name `<string>` | Role name (not optional) |
| permissions `<table>` | Role permissions (not optional) |

| Permissions Available | |
|-||
| OPEN_COMMAND_BAR | Determines if player can open the command bar. |

###Example
```lua
.newrole(
    { -- Properties
        color = Color3.fromRGB(255, 0, 0),
        name = "admin",
        permissions = {
            "OPEN_COMMAND_BAR"
        }
    }
)
```

---

##player.roles.add() `usage`

| Function Arguments |
|-|
| role name `<string>`|

###Example
```lua
module.players["playername"].roles.add("Admin")
```

???+ warning
    This isn't the player `<instance>` is a function array in the "players" array of the module.

---
##player.roles.remove() `usage`

| Function Arguments |
|-|
| role name `<string>`|

###Example
```lua
module.players["playername"].roles.remove("Admin") -- bye bye admin
```

???+ danger
    Wrap this with ``.catch()`` to catch errors. (Constants will throw error if you don't update them)
    ###Repair
    ```lua
    local roles = module.players["playername"].roles

    module.players["playername"].roles.remove("Admin").then_do(function()
        roles = module.players["playername"].roles -- Re-set the value
    end)
    ```
