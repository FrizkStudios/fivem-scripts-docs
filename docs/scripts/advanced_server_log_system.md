---
title: "Home"
nav_order: 3
---

# Important

### Do not change the script name

# Configs
You can find configs in `/server/configs/`

`player_logs.lua` - contains templates for players logs

`server_logs.lua` - contains templates for server logs

`ranks.lua` - contains naming for ranks

`server_config.lua` - contains some variables you can edit

# Player logs

### Each log must have:

`name` - short name for logs without white spaces, it's not visible in UI

`id` - you can choose any number lower than 1000000

`actionName` - Short name for log displayed in UI

`details` - Longer description of log

`actionType` - 1 or 2 or 3. It colors the log and create opportunity to filter logs by action types. 1 is Green, 2 is Blue, 3 is Red.

`removeAfter` - 1-999. Put here number of days after log can be removed. If you put 0 here it is never removed. If you don't assign any value to it, it use value from server_config.lua

### Each log can have:

`access` - numbers from 1 to 4. Number 4 is default access and log is visible for each admin, lower number is equal to more restriction for visibility. 1 access is only for superadmin.


### Details can contains arguments:
```
details = "Removed money ${amount} from player",
```

In this case amount can be different in each player log.


### Example logs:
```lua
Player_Logs = {
    {
        name = "joined_server", -- Unique log name
        id = 1, -- Unique log id
        actionName = "Player joined server", -- Log action name displayed in the menu/tablet
        details = "Player has joined the server", -- Log details displayed in the menu/tablet
        actionType = 2, -- Log action type (1 = Green, 2 = Blue, 3 = Red)
        access = 1, -- Log access level (1 = Superadmin, 2 = Admin, 3 = Moderator, 4 = Support)
        removeAfter = 0, -- Number of days after log can be removed. If you put 0 here it is never removed. If you don't assign any value to it, it use value from server_config.lua
    },
    {
        name = "left_server",
        id = 2,
        actionName = "Player left server",
        details = "Player has left the server",
        actionType = 2,
        removeAfter = 7 -- Log will removed after 7 days.
    },
    {
        name = "money_added",
        id = 3,
        actionName = "Added money",
        details = "Added money {arg1} to player. Reason: {args2}", -- You can arguments inside details like here, Use {} and put inside arg1 or arg2 etc. Example here: Added money 500 to player where 500 can differ in each log
        actionType = 2,
    },
    {
        name = "money_removed",
        id = 4,
        actionName = "Removed money",
        details = "Removed money {arg1} from player",
        actionType = 2,
    }
}

```

### Example send player log in any script

```lua
RegisterNetEvent('taxijob:payReward', function()
    local _source = source
    local reward = 5000
    exports.ox_inventory:AddItem(_source, 'money', 5000)

    --Log sending start

    --Creating a table with log data
    local logData = {
        reward, 'Job pay',
    }

    -- Sending a log
    -- money_added should be the same as any name from our logs config
    -- We have to pass player server id here
    -- logData is not required if log doesnt has any arguments
    exports.kaiser_logs_tablet:SendPlayerLog(_source, 'money_added', logData)
end)

AddEventHandler('playerJoining', function(source)
       -- Sending log without any data
       exports.kaiser_logs_tablet:SendPlayerLog(source, 'joined_server') 
end)
```




# Server_logs


Server Logs works the same as players logs. 
The difference is these logs are not assigned to any player.

```lua
Server_Logs = {
    {
        id = 1,
        name = 'server_start',
        actionName = "Server started",
        details = 'The server has started successfully',
        actionType = 3, 
        access = 1,
    },
    {
        id = 2,
        name = 'server_stop',
        actionName = "Server Stopped",
        details = 'The server has stopped successfully. Reason: {arg1}', -- Same like in player logs you can use arguments here
        actionType = 1,
        access = 1,
    },
        {
        id = 2,
        name = 'airdrop_spawn',
        actionName = "Airdrop spawned",
        details = 'The airdrop has spawned at coords: {arg1}.', -- Same like in player logs you can use arguments here
        actionType = 1,
        access = 1,
    },
}
```

### Example send server log in any script

```lua
RegisterNetEvent('air_drops:spawnedDrop', function(coords)
    local logData = {
        coords
    }

    exports.kaiser_logs_tablet:SendServerLog('airdrop_spawn', logData)
end)

RegisterNetEvent('core:serverStarted', function(source)
       -- Sending log without any data
       exports.kaiser_logs_tablet:SendServerLog('server_start') 
end)
```
