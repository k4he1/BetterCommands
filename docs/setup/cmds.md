#Commands
---

##Basic Commands
=== "Script"
    ```lua
    local cmdUtil = require(path)

    cmdUtil.listen(
        {
            ["command"] = "test",
            ["callback"] = function(info)
                print(info)
            end)
        }
    )
    ```
=== "Expected Output"
    ```lua
    {
        ["caller"] = game.Players.PLAYERNAME,
        ["arguments"] = {
            [1] = "arguments"
        }
    }
    ```

!!! hint
    Check **Commands API** documentation for complex usage.