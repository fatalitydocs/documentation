---
description: All functions and variables from fatality.render
---

# render

### render:create\_font

`fatality.render:create_font(font_family, size, weight, height, color)` : csgo.font

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| font\_family | string | The name of the font family |
| size | int | The size of the font |
| weight | int | The weight of the font |
| outline | boolean | If true the font will have a outline |

Creates and returns a font

### render:text

`fatality.render:text(font, x, y, text, color)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| font | csgo.font | The font used on the text |
| x | float | The X position of the text |
| y | float | The Y position of the text |
| text | string | The text to render |
| color | csgo.color | The color to render the text in |

Renders text with font

### render:text\_size

`fatality.render:text_size(font, text)` : csgo.vector2

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| font | csgo.font | The font of the text |
| text | string | The text |

Calculates the text size and returns it in a vector2

### render:rect

`fatality.render:rect(x, y, width, height, color)` : void  

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| x | float | The X position of the rectangle |
| y | float | The Y position of the rectangle |
| width | float | The width of the rectangle |
| height | float | The height of the rectangle |
| color | csgo.color | The color of the rectangle |

Draws a rectangle

### render:rect\_filled

`fatality.render:rect_filled(x, y, width, height, color)`: void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| x | float | The X position of the rectangle |
| y | float | The Y position of the rectangle |
| width | float | The width of the rectangle |
| height | float | The height of the rectangle |
| color | csgo.color | The color of the rectangle |

Draws a filled rectangle

### render:rect\_fade

`fatality.render:rect_fade(x, y, width, height, col1, col2, horizontal)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| x | float | The X position of the rectangle |
| y | float | The Y position of the rectangle |
| width | float | The width of the rectangle |
| height | float | The height of the rectangle |
| col1 | csgo.color | The first color on the fade |
| col2 | csgo.color | The second color on the fade |
| horizontal | boolean | If true, the fade goes horizontally |

Draws a rectangle with a fade \(gradient\)

### render:indicator

`fatality.render:indicator(x, y, text, is_active, bar_progress)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| x | float | The X position of the indicator |
| y | float | The Y position of the indicator |
| text | string | The text |
| is\_active | boolean | If true the indicator is active \(no clue what to put here\) |
| bar\_progress | float | The progress of the bar |

Draws a indicator with a bar below \(0 - 1, -1 for no bar\)

### render:draw\_hitgroup

`fatality.render:draw_hitgroup(player, matrixes, hitgroup, duration, color)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| player | csgo.player | The player to draw the hitgroup on |
| matrixes | csgo.matrix3x4\_t | The matrixes of the hitgroup |
| hitgroup | int | The hitgroup |
| duration | float | The duration |
| color | csgo.color | The color |

Draws a hitgroup

### render:screen\_size

`fatality.render:screen_size()` : csgo.vector2

Returns the screen size

### example

```lua
-- Get render instance
local render = fatality.render

-- Will be called every time a frame is rendered
function on_paint( )

    -- Create color
    local dark_blue = csgo.color( 33, 27, 70, 255 )

    -- Draw filled rectangle at position 10, 10 with size 100, 100
    render:rect_filled( 10, 10, 100, 100, dark_blue )

end

-- Register all callback functions that should be called
local callbacks = fatality.callbacks
callbacks:add( "paint", "on_paint" )
```

