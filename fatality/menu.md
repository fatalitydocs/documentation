---
description: All functions and variables from fatality.menu
---

# menu

### menu:add\_checkbox

`fatality.menu:add_checkbox(control, tab, sub_tab, child, item)` : fatality.checkbox

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| control | string | The name of the control |
| tab | string | The name of the tab |
| sub\_tab | string | The name of the sub tab |
| child | string | The name of the child |
| item | fatality.value | The config item |

Creates and returns a checkbox

### menu:add\_slider

`fatality.menu:add_slider(control, tab, sub_tab, child, item, min, max, step)` : fatality.slider

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| control | string | The name of the control |
| tab | string | The name of the tab |
| sub\_tab | string | The name of the sub tab |
| child | string | The name of the child |
| item | fatality.value | The config item |
| min | float | The minimum value |
| max | float | The maximum value |
| step | float | The increasing step |

Creates and returns a slider

### menu:add\_combo

`fatality.menu:add_combo(control, tab, sub_tab, child, item)` : fatality.combobox

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| control | string | The name of the control |
| tab | string | The name of the tab |
| sub\_tab | string | The name of the sub tab |
| child | string | The name of the child |
| item | fatality.value | The config item |

Creates and returns a combo

### menu:add\_multi\_combo

 `fatality.menu:add_multi_combo(control, tab, sub_tab, child, item)` : fatality.combobox

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| control | string | The name of the control |
| tab | string | The name of tab |
| sub\_tab | string | The name of the sub tab |
| child | string | The name of the child |
| item | fatality.value | The config item |

Creates and returns a multi combo

### menu:get\_reference

`fatality.menu:get_reference(tab, sub_tab, group, control)` : fatality.value

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| tab | string | The name of the tab |
| sub\_tab | string | The name of the sub tab |
| group | string | The name of the group |
| control | string | The name of the control |

Returns a reference to the specified gui object

### example

```lua
-- Get menu & config instance
local menu = fatality.menu
local config = fatality.config

-- Create config item               (  name,          default )
local example_item = config:add_item( "example_item", 1.0 )

-- Add menu item                          ( Control name, tab_name, sub_tab_name, child_name, config_item )
local example_checkbox = menu:add_checkbox( "Example", "visuals", "misc", "various", example_item )

-- Same can be done for various other menu items
-- Slider:
-- local example_slider = menu:add_slider( "Example", "visuals", "misc", "various", example_item, 0.0, 100.0, 1.0 )
-- Combobox:
-- local example_combo = menu:add_combo( "Example", "visuals", "misc", "various", example_item )
-- example_combo:add_item( "Item 1", example_item )
-- example_combo:add_item( "Item 2", example_item )
-- Multicombo:
-- For this you must create multiple separate config items in addition
-- local item_1 = config:add_item( "item_1", 1.0 )
-- local item_2 = config:add_item( "item_2", 1.0 )
-- local example_multicombo = menu:add_multi_combo( "Example", "visuals", "misc", "various", example_item, 0.0, 100.0, 1.0 )
-- example_multicombo:add_item( "Item 1", item_1 )
-- example_multicombo:add_item( "Item 2", item_2 )

-- More info regarding menu can be found here: https://fatality.win/threads/fatality-menu.504/
```

