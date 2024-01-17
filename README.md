local Creator = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors%20Entity%20Spawner/Source.lua"))()

-- Create entity
local entity = Creator.createEntity({
    CustomName = "A-60", -- Custom name of your entity
    Model = "rbxassetid://11463891411", -- Can be GitHub file or rbxassetid
    Speed = 400, -- Percentage, 100 = default Rush speed
    DelayTime = 3, -- Time before starting cycles (seconds)
    HeightOffset = 4,
    CanKill = true,
    BreakLights = false,
    KillRange = 30000,
    BackwardsMovement = false,
    FlickerLights = {
        false, -- Enabled
        0.1, -- Time (seconds)
    },
    Cycles = {
        Min = 1,
        Max = 1,
    },
    CamShake = {
        true, -- Enabled
        {5, 15, 0.1, 1}, -- Shake values (don't change if you don't know)
        100, -- Shake start distance (from Entity to you)
    },
    Jumpscare = {
        true, -- Enabled ('false' if you don't want jumpscare)
        {
            Image1 = "https://www.roblox.com/library/8372", -- Image1 url
            Image2 = "11867753039", -- Image2 url
            Shake = false,
            Sound1 = {
                6459610652, -- SoundId
                { Volume = 5 }, -- Sound properties
            },
            Sound2 = {
                6459610652, -- SoundId
                { Volume = 5 }, -- Sound properties
            },
            Sound3 = {
                6459610652, -- SoundId
                { Volume = 5 }, -- Sound properties
            },
            Flashing = {
                true, -- Enabled
                Color3.fromRGB(6, 38, 135), -- Color
            },
            Tease = {
                false, -- Enabled ('false' if you don't want tease)
                Min = 1,
                Max = 3,
            },
        },
    },
    CustomDialog = {"You died to Multi_A-60..."}, -- Custom death message (can be as long as you want)
})


Spawner.runEntity(entityTable)
