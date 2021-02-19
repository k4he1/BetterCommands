#Using Notifications
---

=== "Script"
    ```lua
        local cmdUtil = require(path)

        cmdUtil.send("notification", {
            ["receiver"] = game.Players.RiverCryptz, -- You can always use only the player name.
            ["title"] = "Title",
            ["text"] = "This is a very cool module!"
        })
    ```
=== "Game"
    ![Placeholder](https://cdn.discordapp.com/attachments/809905878240723005/812065067381162014/notifexample.JPG){: align=left }
    This is how the notificacion should see in the game.


???+ warning 
    Notification system does not uses tweens. **(FOR NOW)**

---

!!! abstract "End"
    Here's the setup section end.