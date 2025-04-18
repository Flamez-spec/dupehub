local slotsEvent = game.ReplicatedStorage:WaitForChild("rerolls"):WaitForChild("Slots")
local TS = game:GetService("TeleportService")
local pl = game:GetService("Players").LocalPlayer
local player = game.Players.LocalPlayer.Character

local PlaceId = game.PlaceId
local humanoid = pl.Character:FindFirstChildOfClass("Humanoid")

local function dupe()
    print("122121")
    humanoid.Health = 0
    task.wait(7)
    slotsEvent:FireServer(1)
    TS:Teleport(PlaceId, player)
end

dupe()
