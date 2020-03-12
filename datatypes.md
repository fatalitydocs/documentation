# Datatypes



### lag\_record\_t

| member | description |
| :--- | :--- |
| sim\_time : int | The players' time on the server |
| matrix : matrix3x4\_t | The players' bone matrix |
| dormant : boolean | Wether the player is networked on the record |
| origin : vector3 | The position of the player |
| velocity : vector3 | The players' velocity |
| eye\_angles : angle | The players' resolved eye angles |

### record\_shot\_info\_t

| member | description |
| :--- | :--- |
| has\_info : boolean | Shows if the values have been initialized |
| extrapolated : boolean | Shows if the player was being extrapolated on hit |
| breaking\_lc : boolean | Shows if the player was breaking lagcomp |
| delayed\_shot : boolean | Shows wether the shot was delayed |
| backtrack\_ticks : int | The amount of ticks the player was backtracked |

### shot\_t

| member | description |
| :--- | :--- |
| victim : int | The victim's index |
| target\_hitgroup : int | The targeted hitgroup |
| hit : boolean | Shows wether the bullet hit the victim |
| shotpos : csgo.vector3 | The shooting position |
| target\_hitpos : csgo.vector3 | The targeted hit position |
| target\_damage : int | The amount of damage given |
| shot\_info : record\_shot\_info\_t | Additional information about the shot |
| inaccuracy : float | The inaccuracy |
| hitchance : float | The hitchance |
| hurt : boolean | Shows wether the player was hurt or not |

### value

| member | description |
| :--- | :--- |
| get\_int\( \) : int | Returns the int of the value |
| get\_bool\( \) : boolean | Returns the boolean of the value |
| get\_float\( \) : float | Returns the float of the value |
| get\_color\( \) : csgo.color | Returns the color of the value |
| set\_int\( value : int \) : int | Sets the int of the value |
| set\_bool\( value : bool \) : boolean | Sets the boolean of the value |
| set\_float\( value : float \) : float | Sets the float of the value |
| set\_color\( value : color \) : csgo.color | Sets the color of the value |

### color

| member | description |
| :--- | :--- |
| constructor\( r : int, g : int, b : int, a : int \) | Creates and returns a color value |

### game\_event

| member | description |
| :--- | :--- |
| get\_name\( \) : string | Returns the name of the event |
| get\_bool\( aspect : string \) : boolean | Returns the boolean of the specified aspect |
| get\_int\( aspect : string \) : int | Returns the int of the specified aspect |
| get\_float\( aspect : string \) : boolean | Returns the float of the specified aspect |
| get\_string\( aspect : string \) : int | Returns the string of the specified aspect |

### vector3

| member | description |
| :--- | :--- |
| constructor\( x : float, y : float, z : float \) | Creates and returns a vector3 value |
| x : float | The x value |
| y : float | The y value |
| z : float | The z value |
| to\_screen\( \) : bool | Converts the vector3 into a vector2 with the screen position |

### angle

derives from vector3

| member | description |
| :--- | :--- |
| constructor\( x : float, y : float, z : float \) | Creates and returns a angle value |

### convar

| member | description |
| :--- | :--- |
| get\_int\( \) : int | Returns the int value of the convar |
| get\_float\( \) : float | Returns the float value of the convar |
| unlock\( \) : void | Unlock the convar so it can be changed \(WARNING! THIS CAN BAN YOU FROM SECURE SERVERS\) |
| set\_int\( value : int \) : void | Sets the int of the convar |
| set\_string\( value : string \) : void | Sets the string of the convar |
| set\_float\( value : float \) : void | Sets the float of the convar |
| set\_color\( value : color \) : void | Sets the color of the convar |

### entity

[netvar dump](https://fatality.win/attachments/netvar_dump-txt.254/)

| member | description |
| :--- | :--- |
| get\_var\_bool\( netvar : string \) : boolean | Returns the boolean value of the netvar |
| get\_var\_int\( netvar : string \) : int | Returns the int value of the netvar |
| get\_var\_float\( netvar : string \) : float | Returns the float value of the netvar |
| get\_var\_short\( netvar : string \) : short | Returns the short value of the netvar |
| get\_var\_handle\( netvar : string \) : handle | Returns the handle value of the netvar |
| get\_var\_angle\( netvar : string \) : csgo.angle | Returns the angle value of the netvar |
| get\_var\_vector\( netvar : string \) : csgo.vector3 | Returns the vector value of the netvar |
| is\_player\( \) : boolean | Shows wether the entity is a player or not |
| is\_dormant\( \) : boolean | Shows wether the entity is being networked \(false=networked\) |
| get\_index\( \) : int | Returns the index for the entity |
| get\_class\_id\( \) : int | Returns the class id of the entity |

### player

derives from entity

| member | description |
| :--- | :--- |
| get\_name\( \) : string | Returns the player name |
| get\_eye\_pos\( \) : csgo.vector3 | Returns the player's eye position |
| is\_alive\( \) : boolean | Shows wether the player is alive or not |

