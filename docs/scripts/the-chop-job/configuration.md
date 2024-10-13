---
title: "Configuration"
nav_order: 5
parent: "The Chop Job"
---

# Example Configuration file for The Chop Job

```lua
-- lockpick to start in config.lua
-- vehicles locked in config.lua
Config = {}
Config.Debug = true -- Enable or disable console logging
Config.Language = 'en' -- List of languages in translations.lua

--These are for getting player's job name
Config.esx = true -- Set to false if you don't use ESX 
Config.qb = false -- Set to true if you use QBCore
Config.standalone = false -- Set to true if you don't use any framework, but you have to use your own functions

Config.IdentifierType = 'steam' -- Identifier type to use for saving data to database
                                -- You can use steam or license

Config.MissionCooldown = 60 * 60 -- Cooldown in seconds between missions (1 hour)
Config.RequiredPolice = 2 -- Minimum amount of police required to start a mission
Config.MaxMissions = 3 -- Maximum amount of missions that can be active at the same time
                       -- Each mission require RequiredPolice amount of police officers

-- NPC to start a mission settings
Config.NPC = {
    model = 's_m_m_highsec_01',
    coords = vec3(1010.5169677734, 101.60792541504, 89.240409851074),
    heading = 152.92573761940002
}

-- Item required to start a mission
Config.IsItemRequired = true
Config.RequiredItem = {
    itemName = 'money',
    amount = 1
}

Config.Trackify = true -- enable trackify app to find vehicle to steal
Config.MapBlip = true -- enable map blip for target vehicle
Config.LockVehicle = false -- lock vehicle? if true, vehicle will be locked

Config.VehiclesSpawnPoints = {
    {coords = vector3(804.09320068359,-1126.2213134766,28.901966094971), heading = 3.92573761940002},
    {coords = vector3(-1091.92, 436.29, 74.33), heading = 83.0},
    {coords = vector3(-1080.93, 462.9, 76.59), heading = 145.0},
    {coords = vector3(-1106.93, 554.04, 101.64), heading = 210.0},
    {coords = vector3(-1302.44, -191.65, 46.09), heading = 30.74},
    {coords = vector3(-356.68, -756.74, 37.83), heading = 92.4},
    {coords = vector3(876.2, -44.1, 77.81), heading = 60.93},
    {coords = vector3(-1777.4, -667.42, 9.43), heading = 138.9},
    {coords = vector3(-1644.62, -236.11, 53.86), heading = 75.5},
    {coords = vector3(-1027.11, -515.40, 35.22), heading = 26.0},
    {coords = vector3(-786.6, -570.24, 29.17), heading = 34.0},
    {coords = vector3(1287.2, -1951.86, 42.61), heading = 204.18},
    {coords = vector3(1126.55, -1295.84, 33.73), heading = 87.4},
    {coords = vector3(1130.11, -488.93, 64.43), heading = 76.41},
    {coords = vector3(615.24, 122.43, 91.97), heading = 251.0},
    {coords = vector3(318.58, 496.66, 151.78), heading = 109.36},
    {coords = vector3(227.24, 680.27, 188.54), heading = 287.14},
    {coords = vector3(55.19, 468.56, 145.93), heading = 21.59},
    {coords = vector3(-67.89, 894.85, 234.59), heading = 295.42},
    {coords = vector3(-385.3, 1210.72, 324.69), heading = 284.33},
    {coords = vector3(-1023.87, 812.73, 171.19), heading = 11.28},
    {coords = vector3(-1123.23, 789.89, 162.41), heading = 59.9},
    {coords = vector3(-177.19, 6442.29, 29.81), heading = 226.52},
    {coords = vector3(-548.11, -1801.64, 20.36), heading = 59.72},
    {coords = vector3(-1207.25, -1058.77, 6.58), heading = 6.5882},
    {coords = vector3(1902.04, 3891.64, 31.04), heading = 115.59},
    {coords = vector3(1909.53, 3725.09, 31.02), heading = 23.2},
    {coords = vector3(-384.87, 6189.93, 29.82), heading = 45.25},
    {coords = vector3(-208.88, 6364.50, 29.82), heading = 29.82},
    {coords = vector3(-205.84, 6100.37, 30.045), heading = 227.13},
    {coords = vector3(997.8896, -1384.6820, 31.3594), heading = 299.6963},
    {coords = vector3(565.1382, -2320.5559, 5.9084), heading = 208.8506},
}

Config.PoliceJobs = {
    'police',
    'sheriff',
    'highway'
}

Config.StagesTime = {
    [1] = 60 * 10, -- 10 minutes to find vehicle
    [2] = 60 * 7, -- 7 minutes escaping from police while having gps
    [3] = 60 * 25, -- 25 minutes to drive vehicle to destination
    [4] = 60 * 5, -- 5 minutes to remove parts of vehicle OPTIONAL
    [5] = 60, -- Do not change
    [6] = 60 -- Do not change
}

Config.DestinationsCoords = {
    {coords = vector3(-470.29486083984,-1674.9046630859,19.075384140015), size = 20.0},
    {coords = vec3(2418.5361328125, 3146.6745605469, 47.950397491455), size = 20.0},
}

-- Time to remove a part of vehicle
Config.PartRemoveTime = 5000

-- Experience to get from mission
Config.ExpMin = 50
Config.ExpMax = 60

-- Experience needed to level up
Config.expTable = {
    250, 750, 1250, 2000, 3000, 5000, 7500, 10000, 15000, 20000
}

-- Maximum level - do not change
Config.maxLevel = #Config.expTable

-- Vehicle models for each level of player
Config.VehicleModels = {
    [0] = { 'baller3', 'brioso', 'mesa', 'jester', 'kanjo', 'jb7002', 'sultan', 'ruston', 'voltic' },
    [1] = { 'baller3', 'brioso', 'felon2', 'jester', 'imorgon', 'sultan', 'ruston', 'sentinel', 'voltic', 'kuruma' },
    [2] = { 'jubilee', 'cog55', 'felon2', 'jester', 'imorgon', 'sultan', 'ruston', 'omnisegt', 'dominator3' },
    [3] = { 'jubilee', 'cog55', 'felon2', 'jester', 'imorgon', 'sultan', 'superd', 'omnisegt', 'xls' },
    [4] = { 'xls', 'euros', 'felon2', 'jester', 'imorgon', 'sultan', 'superd', 'khamelion', 'feltzer2' },
    [5] = { 'novak', 'euros', 'tailgater2', 'jester4', 'imorgon', 'sultan', 'banshee', 'khamelion', 'feltzer2', 'alpha' },
    [6] = { 'sultan2', 'raiden', 'elegy', 'sugoi', 'pariah', 'comet6', 'coquette4', 'paragon', 'cyclone', 'rebla' },
    [7] = { 'sultan2', 'raiden', 'elegy2', 'sugoi', 'pariah', 'infernus', 'coquette4', 'ninef', 'cyclone', 'entity2', 'vacca' },
    [8] = { 't20', 'raiden', 'elegy2', 'turismor', 'pariah', 'infernus', 'coquette4', 'ninef', 'fmj', 'entity2', 'vacca' },
    [9] = { 't20', 'fmj', 'elegy2', 'turismor', 'nero2', 'infernus', 'visione', 'thrax', 'fmj', 'entity2', 'vacca' },
    [10] = { 't20', 'fmj', 'elegy2', 'turismor', 'nero2', 'infernus', 'visione', 'thrax', 'fmj', 'entity2', 'vacca' }
}

-- Rewards for each level of player
Config.Rewards = {
    [0] = { ['money'] = { chance = 100, min = 1500, max = 2000 }, },
    [1] = { ['money'] = { chance = 100, min = 1750, max = 2250 }, },
    [2] = { ['money'] = { chance = 100, min = 2000, max = 2500 }, },
    [3] = { ['money'] = { chance = 100, min = 2250, max = 2750 }, },
    [4] = { ['money'] = { chance = 100, min = 2500, max = 3000 }, },
    [5] = { ['money'] = { chance = 100, min = 2750, max = 3250 }, },
    [6] = { ['money'] = { chance = 100, min = 3000, max = 3500 }, },
    [7] = { ['money'] = { chance = 100, min = 3250, max = 3750 }, },
    [8] = { ['money'] = { chance = 100, min = 3500, max = 4000 }, },
    [9] = { ['money'] = { chance = 100, min = 3750, max = 4250 }, },
    [10] = { ['money'] = { chance = 100, min = 4000, max = 4500},
             ['lockpick'] = { chance = 40, min = 1, max = 2 }    },
}

```