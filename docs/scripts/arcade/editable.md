---
title: "Editable functions"
nav_order: 3
parent: "Arcade Arenas"
---

# Editable functions in The Arcade Arenas

# Client Functions

`client/your_functions.lua`

## Is dead function

```lua
`client/your_functions.lua`
-- Checks if the local player is dead.
-- @return {boolean} - Returns true if the local player is dead, false otherwise.
function isDead()
    return LocalPlayer.state.isDead
end
```

## Revive function

```lua
-- Revives the local player at the specified coordinates.
-- @param {Vector3} coords - The coordinates where the player should be revived.
function revive(coords)
    TriggerEvent('esx_ambulancejob:revivee', coords)
end
```

## Notify function

```lua
-- Sends a notification with the given text.
-- @param {string} text - The text to be displayed in the notification.
function notify(text)
    TriggerEvent('esx:showNotification', text)
end
```

# Server Functions

`server/your_functions.lua`

## Revive function

```lua
-- Revives the player on the server side.
-- @param {number} src - The source ID of the player to be revived.
function revive(src)
    TriggerClientEvent('esx_ambulancejob:revivee', src)
end
```