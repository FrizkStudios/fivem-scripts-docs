---
title: "Items list"
nav_order: 3
parent: "The Chop Job"
---


# Items list:

### ox_inventory/data/items.lua

```
    ['wheel0'] = {
        label = 'Front Left Wheel',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('wheel0')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('wheel0')
            end,
        },
    },

    ['wheel1'] = {
        label = 'Front Right Wheel',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('wheel1')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('wheel1')
            end,
        },
    },

    ['wheel2'] = {
        label = 'Rear Left Wheel',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('wheel2')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('wheel2')
            end,
        },
    },

    ['wheel3'] = {
        label = 'Rear Right Wheel',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('wheel3')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('wheel3')
            end,
        },
    },

    ['seat0'] = {
        label = 'Front Left Seat',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('seat0')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('seat0')
            end,
        },
    },

    ['seat1'] = {
        label = 'Front Right Seat',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('seat1')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('seat1')
            end,
        },
    },

    ['seat2'] = {
        label = 'Rear Left Seat',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('seat2')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('seat2')
            end,
        },
    },

    ['seat3'] = {
        label = 'Rear Right Seat',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('seat3')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('seat3')
            end,
        },
    },

    ['door0'] = {
        label = 'Front Left Door',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('door0')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('door0')
            end,
        },
    },

    ['door1'] = {
        label = 'Front Right Door',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('door1')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('door1')
            end,
        },
    },

    ['door2'] = {
        label = 'Rear Left Door',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('door2')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('door2')
            end,
        },
    },

    ['door3'] = {
        label = 'Rear Right Door',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('door3')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('door3')
            end,
        },
    },

    ['engine'] = {
        label = 'Engine',
        weight = 100,
        consume = 0,
        client = {
            remove = function(total)
               exports.kaiser_advanced_tracker:removePart('engine')
            end,
            add = function(total)
                exports.kaiser_advanced_tracker:addPart('engine')
            end,
        },
    },
```
