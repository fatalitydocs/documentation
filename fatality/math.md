---
description: All functions and variables from fatality.math
---

# math

### math:calc\_angle

`fatality.math:calc_angle(origin, destination)` : csgo.angle

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| origin | csgo.vector3 | The origin |
| destination | csgo.vector3 | The destination |

Calculates the angle betwoon 2 vector3's

### example

```lua
-- Get math instance
local math = fatality.math

-- Calculates angle between two vectors
local angle = math:calc_angle( csgo.vector3( 0, 0, 0 ), csgo.vector3( 100, 50, 300 ) )
```

