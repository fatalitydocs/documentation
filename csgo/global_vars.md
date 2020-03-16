---
description: All functions and variables from csgo.global_vars
---

# global\_vars

### csgo.global\_vars.realtime

`csgo.interface_handler:get_global_vars().realtime : float`  
The absolute time

### csgo.global\_vars.framecount

`csgo.interface_handler:get_global_vars().framecount : int`  
The absolute frame count

### csgo.global\_vars.curtime

`csgo.interface_handler:get_global_vars().curtime : float`  
The current time

### csgo.global\_vars.frametime

`csgo.interface_handler:get_global_vars().frametime : float`  
The time spent on the last server or client frame

### csgo.global\_vars.tickcount

 `csgo.interface_handler:get_global_vars().tickcount : int`  
The tick count

### csgo.global\_vars.interval\_per\_tick

`csgo.interface_handler:get_global_vars().interval_per_tick`  
The time between ticks

### example

```lua
local global_vars = csgo.interface_handler:get_global_vars()

print(global_var.realtime)
```

