---
description: All functions and variables from fatality.config
---

# config

### config:add\_item

`fatality.config:add_item(name, default_value)` : fatality.value

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| name | string | The item name |
| default\_value | float | The default item value |

Creates a config item and returns it's value

### config:get\_item

`fatality.config:get_item(name)` : fatality.value

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| name | string | The item name |

Gets and returns a config item's value

### example

```lua
local config = fatality.config;

local yaw_add_item = fatality.config:add_item( "lua_yaw_add", 0 )
```

