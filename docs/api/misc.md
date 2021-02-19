#Miscellaneous
---

##.catch() `usage`
`.catch()` is a function which returns in every function you fire, this function is useful to handle errors.
###Example
=== "Script"
    ```lua
    module.listen(
        ["command"] = "hello",
        ["callback"] = function()
            error("Error")
        end
    ).catch(function(err)
        print("error detected: "..err)
    end)
    ```
=== "Output"
    ```
    error detected: Error
    ```
---
##.then_do() `usage`
`.then_do()` is a function which returns in every function you fire(like .catch) but this is more a callback that fires when the first function you fired
ends.
###Example
=== "Script"
    ```lua
    module.listen(
        ["command"] = "hello",
        ["callback"] = function()
            error("Error")
        end
    ).then_do(function()
        print("command created")
    end)
    ```
=== "Output"
    ```
    command created
    ```

???+ tip
    You can use 
    ```lua
    local cmd = module.listen() -- Every function returns a table which has "then_do" and "catch" functions.

    cmd.then_do(callback)
    cmd.catch(callback)
    ```

---
##.getcommands() `usage`
Returns all commands with their properties.

| Return |
|-|
| commands `<table>`|

---
##.getroles() `usage`
Returns all roles with their properties.

| Return |
|-|
| roles `<table>`|

