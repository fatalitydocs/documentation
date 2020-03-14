---
description: All functions and variables from csgo.engine_client
---

# engine\_client

### engine\_client:client\_cmd\_unrestricted

`fatality.engine_client:client_cmd_unrestricted(cmd)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| cmd | string | The command |

Executes a console command without restrictions.

### engine\_client:client\_cmd

`fatality.engine_client:client_cmd(cmd)` : void

| ARGUMENT | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| cmd | string | The command |

Executes a console command with restrictions.

### engine\_client:is\_in\_game

`fatality.engine_client:is_in_game()` : void

Returns a boolean, if true, you are in a game

### engine\_client:is\_in\_thirdperson <a id="engine_client-is_in_game"></a>

`fatality.engine_client:is_in_thirdperson()` : boolean

Returns a boolean, if true, you are in a thirdperson

### engine\_client:is\_connected <a id="engine_client-is_in_game"></a>

`fatality.engine_client:is_connected()` : boolean

Returns a boolean, if true, you are connected

### engine\_client:get\_ping <a id="engine_client-is_in_game"></a>

`fatality.engine_client:get_ping()` : int

Returns your ping

### engine\_client:get\_map\_name <a id="engine_client-is_in_game"></a>

`fatality.engine_client:get_map_name()` : string

Returns the map name

### example

```lua
local engine = csgo.interface_handler:get_engine_client()

engine:client_cmd_unrestricted( "+voicerecord" )
```

