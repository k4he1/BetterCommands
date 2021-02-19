# Commands API
`.listen()` is the function used to create commands

---


## .listen() `settings`
|  Params |                                             |
|---------|                                             |
| command `<string>` | This is the command name **(not optional)** |
| callback `<function>` | Function to fire after the command was executed **(not optional)** |
| roles `<table>` | Roles who can use the command **(leave this nil and everyone will be able)** |
| min_params `<number>` | Minimun params acceptable in the command **(leave this nil and will be 1)** |

###Example
```lua
module.listen(
    { -- settings
        ["command"] = "help" -- Not optional
        ["roles"] = {"admin"},
        ["min_params"] = 4,
        ["callback"] = function(info)
            print(info)
        end
    }
)
```

---

##.listen() `callback return`
Return-type of the command callback.

| Return-type | |
|--------|    |                                       
| caller `<instance; player>` | Player who fired the command |
| arguments `<table>` | Arguments have no index, these are just `<string>` values. |

###Example

=== "Script"
    ```lua
        ["callback"] = function(info)
            print(info.arguments)
        end
    ```
=== "Output"
    Arguments have no `<string>` index, these have `<number>` index.
    ```lua
    {
        [1] = "param"
    }
    ```

---
