#Notifications API
???+ warning
    Notifications were explained in the "setup" section; this page only explains the function params.

---

##.send() `settings`
| Params | |
|-----| |
| receiver `<instance; player>` | Player who will receive the notification **(not optional)**|
| title `<string>` | This is the title of the notification **(leave nil and will be "Alert") ** |
| text `<string>` | This is the text of the notification **(not optional)** |
| color `<color3>` | Color of the notification **(leave it nil and will be "Pink-red")** |

???+ hint
    Color `property` accepts `<brickcolor>` constructor.