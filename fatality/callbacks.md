---
description: All functions and variables from fatality.callbacks
---

# callbacks

### callbacks

| KEYWORD | DESCRIPTION | PARAMETERS |
| :--- | :--- | :--- |
| paint | called every frame | \( \) |
| events | called whenever the server sends an event to you \(e.g. player\_hurt\) | \( event: game\_event\) |
| registered\_shot | called whenever a shot from the rage- or legit- bot gets registered on the server | \( shot: shot\_t\) |
| level\_init | called once map and all entities have been initialized | \( \) |

### callbacks:add

`fatality.callbacks:add(callback, function)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| callback | string | The name of the callback being used |
| function | function | The function to call when the callback is fired |

Fires the function when the callback is called

### example

```lua
function on_paint()
    -- Paint code
end

fatality.callbacks:add("paint", on_paint)
```

