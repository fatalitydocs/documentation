---
description: All functions and variables from csgo.debug_overlay
---

# debug\_overlay

### csgo.debug\_overlay:add\_box\_overlay

`csgo.debug_overlay:add_box_overlay(origin, mins, maxs, orientation, color, duration)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| origin | csgo.vector3 | The origin of the debug overlay |
| mins | csgo.vector3 | The mins of the overlay |
| maxs | csgo.vector3 | The maxs of the overlay |
| orientation | csgo.angle | The orientation of the overlay |
| color | csgo.color | The color of the overlay |
| duration | float | The duration of the overlay |

Draws a box

### csgo.debug\_overlay:add\_line\_overlay <a id="csgo-debug_overlay-add_box_overlay"></a>

`csgo.debug_overlay:add_line_overlay(start, dest, color, skip_occlusion, duration)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| start | csgo.vector3 | From where to start the overlay |
| dest | csgo.vector3 | To where the overlay should stop |
| color | csgo.color | The color of the overlay |
| skip\_occlusion | boolean | If true, the overlay will skip occlusion |
| duration | float | The duration of the overlay |

Draws a line

### example

```lua
local debug_overlay = csgo.debug_overlay

debug_overlay:add_line_overlay( csgo.vector3( 0, 0, 0 ), csgo.vector3( 10, 10, 10 ), csgo.color( 255, 255, 255 ), true, 10 )
```

