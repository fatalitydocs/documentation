---
description: All functions and variables from fatality.input
---

# input

### input:is\_key\_down

`fatality.input:is_key_down(key)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| key | int | The key |

Returns a boolean, if true the key is down

### example

```lua
local input = fatality.input;

-- 72 -> 0x47 -> G key
local is_down = input:is_key_down( 72 )
```



