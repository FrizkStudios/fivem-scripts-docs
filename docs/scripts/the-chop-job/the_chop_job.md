---
layout: default
title: "The Chop Job"
nav_order: 2
has_children: true
permalink: /docs/scripts/the-chop-job
---

# The Chop Job
## Dependiencies:

- `ox_inventory`
- `ox_lib`
- `ox_target`
- [kaiser_recycler](https://kaiser-shop.tebex.io/package/6496196)

## Installation:
- Put script in your resources directory and start in server config. 
- If you want to use trackify app to locate vehicles then start that script also
- Add items to ox_inventory
- Configure script config
- Setup your own functions in editable directory

## How to:
- Start mission
- Locate vehicle by using phone app "arrow up" bind and you can change it in fivem keys settings 
- or if you've chosen that vehicle is findable by map blip then locate in the area on the map
- Escape the police
- Deliver the vehicle
- Dismantle vehicle
- Scrap parts of the vehicle in recycler from `kaiser_recycler`

## Items list:

```
    ['wheel0'] = {
        label = 'Koło przednie lewe',
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
        label = 'Koło przednie prawe',
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
        label = 'Koło tylne lewe',
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
        label = 'Koło tylne prawe',
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
        label = 'Siedzenie przednie lewe',
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
        label = 'Siedzenie przednie prawe',
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
        label = 'Siedzenie tylne lewe',
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
        label = 'Siedzenie tylne prawe',
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
        label = 'Drzwi przednie lewe',
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
        label = 'Drzwi przednie prawe',
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
        label = 'Drzwi tylne lewe',
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
        label = 'Drzwi tylne prawe',
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
        label = 'Silnik',
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
