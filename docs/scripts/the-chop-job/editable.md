---
title: "Editable functions"
nav_order: 4
parent: "The Chop Job"
---

# Editable functions in The Chop Job

# Client Functions

`editable/client/your_functions.lua`

## Send dispatch

```lua
-- Sends a dispatch with the given vehicle information.
-- @param {Vehicle} vehicle - The vehicle involved in the dispatch.
-- @param {Vector3} coords - The coordinates of the vehicle.
-- @param {string} model - The model of the vehicle.
-- @param {string} displayModel - The display model of the vehicle.
-- @param {string} plate - The license plate of the vehicle.

function SendDispatch(vehicle, coords, model, displayModel, plate)
    Logger(vehicle, coords, model, displayModel, plate)
end
```

# Server Functions

`editable/server/your_functions.lua`

## Notify player

```lua
-- Example function that sends a message to a player.
-- @param {number} source - The source player ID.
-- @param {string} message - The message to send.

function NotifyPlayer(source, message)
    TriggerClientEvent('esx:showNotification', source, message)
end
```

# Send SMS

```lua
-- Example function that sends an SMS to a player.
-- You can implement a notify function if you don't want to send SMS.
-- @param {number} source - The source player ID.
-- @param {string} message - The message to send.

function SendSMS(source, message)
    TriggerClientEvent('esx:showNotification', source, message)
end
```

## Get police amount

```lua
-- Implement your own functions here to get the amount of police officers.
-- @returns {number} - The amount of police officers.

function GetPoliceAmount()
    return 4
end
```

## Has item

```lua
-- Checks if a player has a specific item in their inventory.
-- @param {number} _source - The source player ID.
-- @param {string} itemName - The name of the item.
-- @param {number} amount - The amount of the item.
-- @returns {boolean} - True if the player has the item, false otherwise.

function HasItem(_source, itemName, amount)
    local item = exports.ox_inventory:GetItem(_source, itemName, false, true)

    if not item then
        return false
    end

    return item >= amount
end
```

## Lock vehicle

```lua
-- Implement your own functions to lock a vehicle.
-- @param {Vehicle} vehicle - The vehicle to lock.

function LockVehicle(vehicle)
    if not Config.LockVehicle then
        return
    end

    SetVehicleDoorsLocked(vehicle, 2)
end
```

## Remove item

```lua
-- Removes a specific item from a player's inventory.
-- @param {number} _source - The source player ID.
-- @param {string} itemName - The name of the item.
-- @param {number} amount - The amount of the item to remove.

function RemoveItem(_source, itemName, amount)
    exports.ox_inventory:RemoveItem(_source, itemName, amount)
end

```

## Send discord log

```lua
-- Sends a log message to a Discord webhook.
-- @param {number} _source - The source player ID.
-- @param {string} message - The log message to send.

DiscordWebhook = 'https://discord.com/api/' -- put here your discord webhook

function SendDiscordLog(_source, message)
    if DiscordWebhook == 'https://discord.com/api/' then -- DO NOT CHANGE THIS
        return
    end

    PerformHttpRequest(Config.DiscordWebhook, function(err, text, headers) end, 'POST', json.encode({content = message}), { ['Content-Type'] = 'application/json' })
end

```