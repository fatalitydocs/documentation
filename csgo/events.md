---
description: All functions and variables from csgo.engine_client
---

# events

### [events](https://wiki.alliedmods.net/Counter-Strike:_Global_Offensive_Events)

### events:add\_event

`csgo.events:add_event( event_name : string ) : void`  
Adds a callback registered to the specified event.

### example

```lua
local events = csgo.interface_handler:get_events()
function on_event(e)
    if e:get_name() == "bomb_planted" then
        print'bomb planted B)'
    end
end

events:add_event("bomb_planted")

fatality.callbacks:add("events", on_event)
```

