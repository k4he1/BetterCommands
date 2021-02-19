#Await API
???+ danger
    `.await()` will wait using `loops` and this may cause lag (**timeout: 100s**)
???+ hint
    `.await()` does not generates yielding in script.

---

##.await() `usage`

| Params | |
|-||
| method `<string>` | Method to wait for |
| settings `<table>` | Method settings |

| Methods | |
|-||
| response | `settings` `command (not optional)` `timeout (optional)` `callback (not optional)` |

###Example
```lua
function(info) -- callback of listen()
    module.await("response", 
        { -- Method settings
            command = info,
            timeout = 5, -- in seconds
            callback = function(response)
                print(response)
            end
        }
    )
end
```