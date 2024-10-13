---
title: "Configuration"
nav_order: 4
parent: "Arcade Arenas"
---

# Configuration for The Arcade Arenas

```lua
Config = {}

-- TO OPEN TABLET YOU HAVE TO TRIGGER CLIENT EVENT 'arenas:openTablet' IN YOUR SCRIPT

Config.OX = true -- if you have ox_inventory, ox_target IT SHOULD BE true, ELSE set it to false
Config.requiredItemToPlay = true --Is item required to play on arena, ox_inventory required
Config.requiredItemToPlayName = 'arcade_token'
Config.OxWeaponFix = true -- set it to true if you have ox_inventory and weapon not spawn after joining arena

Config.SpawnPoint = vector3(142.17314147949,-2962.0258789062,7.2421579360962)
Config.MaxRounds = 20
Config.MaxPlayers = 20
Config.DefaultBucket = 0 -- If you have different routing bucket than 0 as default on you server you have to change it
Config.MaxEntryFee = 5000 -- It works nnly if Config.OX is true

Config.Maps = {
    ['xvsx'] = {
        
        {
            label = 'Cbble',
            value = 'cbble',
            spawnMap = true,
            mapCoords = vec3(-900.1, -3341.01, 23.93),
            mapModel = 'esevoo_arena_kaiser',
            spawnpoints = {
                [1] = vec3(-877.81, -3341.07, 25.85),
                [2] = vec3(-922.7, -3341.18, 25.85),
            }
        },


        {
            label = 'Lost Dino',
            value = 'lost_dino',
            spawnpoints = {
                [1] = vector3(2315.5251464844,2524.3376464844,46.66773223877),
                
                [2] = vector3(2355.81640625,2621.0329589844,46.667625427246),
            }
        },
        {
            label = 'Sandy Airport',
            value = 'lotnisko_sandy',
            spawnpoints = {
                [1] = vector3(1669.6245117188,3160.5793457031,46.375118255615),
                
                [2] = vector3(1725.9187011719,3323.7407226562,41.223453521729),
            }
        },
        {
            label = 'Big Lost',
            value = 'duze_losty',
            spawnpoints = {
                [1] = vector3(83.098937988281,3757.0561523438,39.752635955811),
                
                [2] = vector3(28.610416412354,3611.9265136719,39.761318206787),
            }
        },
        {
            label = 'Fisher',
            value = 'rybak',
            spawnpoints = {
                [1] = vector3(1290.6605224609,4377.4467773438,40.997352600098),
                
                [2] = vector3(1439.98046875,4368.3071289062,43.868301391602),
            }
        },
        {
            label = 'Human Labs',
            value = 'human_labs',
            spawnpoints = {
                [1] = vector3(3420.7868652344,3758.1499023438,30.562593460083),
                
                [2] = vector3(3602.0827636719,3714.1010742188,36.642673492432),
            }
        },
        {
            label = 'Pacific Standard',
            value = 'pacific_standard',
            spawnpoints = {
                [1] = vector3(271.00128173828,216.38256835938,110.17333984375),
                
                [2] = vector3(227.78816223145,213.0943145752,105.52807617188),
            }
        },
        {
            label = 'Sandy',
            value = 'sandy',
            spawnpoints = {
                [1] = vector3(1557.5434570312, 3599.5224609375, 38.775230407715),
                
                [2] = vector3(1508.0427246094, 3575.5766601562, 38.736461639404),
            }
        },
        {
            label = 'ONeal',
            value = 'oneal',
            spawnpoints = {
                [1] = vector3(2445.6584472656, 4986.857421875, 51.726058959961),
                
                [2] = vector3(2434.2509765625, 4964.7250976562, 42.347625732422),
            }
        },
    },

    ['gungame'] = {
        {
            label = 'Cbble',
            value = 'cbble',
            spawnMap = true,
            mapCoords = vec3(-900.1, -3341.01, 23.93),
            mapModel = 'esevoo_arena_kaiser',
            spawnpoints = {
                [1] = vec3(-877.81, -3341.07, 25.85),
                [2] = vec3(-922.7, -3341.18, 25.85),
            }
        },


        {
            label = 'Lost Dino',
            value = 'lost_dino',
            spawnpoints = {
                [1] = vector3(2315.5251464844,2524.3376464844,46.66773223877),
                
                [2] = vector3(2355.81640625,2621.0329589844,46.667625427246),
            }
        },
        {
            label = 'Sandy airport',
            value = 'lotnisko_sandy',
            spawnpoints = {
                [1] = vector3(1669.6245117188,3160.5793457031,46.375118255615),
                
                [2] = vector3(1725.9187011719,3323.7407226562,41.223453521729),
            }
        },
        {
            label = 'Big lost',
            value = 'duze_losty',
            spawnpoints = {
                [1] = vector3(83.098937988281,3757.0561523438,39.752635955811),
                
                [2] = vector3(28.610416412354,3611.9265136719,39.761318206787),
            }
        },
        {
            label = 'Sandy',
            value = 'sandy',
            spawnpoints = {
                [1] = vector3(1557.5434570312, 3599.5224609375, 38.775230407715),
                
                [2] = vector3(1508.0427246094, 3575.5766601562, 38.736461639404),
            }
        },
        {
            label = 'ONeal',
            value = 'oneal',
            spawnpoints = {
                [1] = vector3(2445.6584472656, 4986.857421875, 51.726058959961),
                
                [2] = vector3(2434.2509765625, 4964.7250976562, 42.347625732422),
            }
        },
        {
            label = 'Humane Labs',
            value = 'humane_labs',
            spawnpoints = {
                [1] = vector3(3616.7214355469, 3735.4157714844, 28.690097808838),
                
                [2] = vector3(3531.5698242188, 3648.1174316406, 27.521585464478),
            }
        },
    },
}

Config.Weapons = {
    {
        label = 'Pistol mk2',
        value = 'weapon_pistol_mk2'
    },
    {
        label = 'Pistolet',
        value = 'weapon_pistol'
    },
    {
        label = 'Combat Pistol',
        value = 'weapon_combatpistol'
    },
    {
        label = 'Pistolet Vintage',
        value = 'weapon_vintagepistol'
    },
    {
        label = 'Pistolet SNS MK2',
        value = 'weapon_snspistol_mk2'
    },
    {
        label = 'Pistolet Marksman',
        value = 'weapon_marksmanpistol'
    },
    {
        label = 'Pistolet .50',
        value = 'weapon_pistol50'
    },
    {
        label = 'Pistolet APP',
        value = 'weapon_appistol'
    },
    {
        label = 'Pistolet CeramicPistol',
        value = 'weapon_ceramicpistol'
    }, 
}

Config.GunGame = {
    kills_per_level = 1, -- how many kills to level up weapon

    Weapons = {
        {
            value = 'weapon_sniperrifle',
            label = 'Snajperka'
        },
        {
            value = 'weapon_combatmg_mk2',
            label = 'MG'
        },
        {
            value = 'weapon_assaultrifle',
            label = 'Assault rifle'
        },
        {
            value = 'weapon_advancedrifle',
            label = 'Advanced rifle'
        },
        {
            value = 'weapon_tacticalrifle',
            label = 'Tactical Rifle'
        },
        {
            value = 'weapon_combatpdw',
            label = 'Combat PDW'
        },
        {
            value = 'weapon_assaultsmg',
            label = 'Assault SMG'
        },
        {
            value = 'weapon_smg',
            label = 'SMG'
        },
        {
            value = 'weapon_microsmg',
            label = 'Micro SMG'
        },
        {
            value = 'weapon_minismg',
            label = 'Mini SMG'
        },
        {
            value = 'weapon_combatshotgun',
            label = 'Combat Shotgun'
        },
        {
            value = 'weapon_assaultshotgun',
            label = 'Assault shotgun'
        },
        {
            value = 'weapon_sawnoffshotgun',
            label = 'Sawn off'
        },
        {
            value = 'weapon_dbshotgun',
            label = 'DB shotgun'
        },
        {
            value = 'weapon_precisionrifle',
            label = 'Precision Rifle'
        },
        {
            value = 'weapon_doubleaction',
            label = 'Double action'
        },
        {
            value = 'weapon_revolver_mk2',
            label = 'Revolver MK2'
        },
        {
            value = 'weapon_heavypistol',
            label = 'Heavy pistol'
        },
        {
            value = 'weapon_pistol50',
            label = 'Pistol 50'
        },
        {
            value = 'weapon_vintagepistol',
            label = 'Vintage pistol'
        },        
        {
            value = 'weapon_pistol_mk2',
            label = 'Pistol MK2'
        },   
        {  ---FINAL WEAPON
            value = 'weapon_knife',
            label = 'Kosa'
        },
    }
}

Config.LobbySettings = {
    {
      name = 'game_name',
      label = 'Game name',
      type = 'text',
      minLength = 3,
      maxLength = 24,
      placeholder = 'Lobby name',
      types = 'all', -- or specify game type if applicable
    },
    {
      name = 'password',
      label = 'Password',
      type = 'password',
      minLength = 3,
      maxLength = 24,
      placeholder = '*****',
      types = 'all', -- or specify game type if applicable
    },
    {
      name = 'game_type',
      label = 'Game Type',
      type = 'select',
      options = {
        { label = 'XvsX', value = 'xvsx' },
        { label = 'GunGame', value = 'gungame' },
      },
      types = 'all', -- or specify game type if applicable
    },
    {
      name = 'max_players',
      label = 'Max players',
      type = 'number',
      min = 2,
      max = 12,
      defaultValue = 4,
      types = 'all', -- or specify game type if applicable
    },
    {
      name = 'map',
      label = 'Map',
      type = 'select',
      options = Config.Maps['xvsx'],
      types = 'xvsx', -- or specify game type if applicable
    },
    {
        name = 'map',
        label = 'Map',
        type = 'select',
        options = Config.Maps['gungame'],
        types = 'gungame', -- or specify game type if applicable
      },
    {
        name = 'max_rounds',
        label = 'Max rounds',
        type = 'number',
        min = 2,
        max = 16,
        defaultValue = 8,
        types = 'xvsx', -- or specify game type if applicable
      },
    {
      name = 'weapon',
      label = 'Weapon',
      type = 'select',
      options = Config.Weapons,
      types = 'xvsx', -- or specify game type if applicable
    },
    {
        name = 'entry_fee',
        label = 'Entry fee',
        type = 'number',
        min = 0,
        max = 5000,
        defaultValue = 0,
        types = 'all', -- or specify game type if applicable
      },
  }
  
```