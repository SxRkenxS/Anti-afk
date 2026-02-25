local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local Stats = game:GetService("Stats")

rconsoleprint("\n=== Server Information ===\n")
rconsoleprint("Server Job ID: " .. game.JobId .. "\n")
rconsoleprint("Place ID: " .. game.PlaceId .. "\n")
rconsoleprint("Server FPS: " .. math.floor(1/RunService.Heartbeat:Wait()) .. "\n")
rconsoleprint("Memory Usage: " .. math.floor(Stats:GetTotalMemoryUsageMb()) .. "MB\n")

rconsoleprint("\n=== Players Information ===\n")

for _, player in ipairs(Players:GetPlayers()) do
    rconsoleprint("\nPlayer: " .. player.Name .. "\n")
    rconsoleprint("- Display Name: " .. player.DisplayName .. "\n")
    rconsoleprint("- User ID: " .. player.UserId .. "\n")
    rconsoleprint("- Account Age: " .. player.AccountAge .. " days\n")
    rconsoleprint("- Team: " .. (player.Team and player.Team.Name or "None") .. "\n")
    
    local char = player.Character
    if char then
        local humanoid = char:FindFirstChild("Humanoid")
        if humanoid then
            rconsoleprint("- Health: " .. humanoid.Health .. "/" .. humanoid.MaxHealth .. "\n")
        end
        rconsoleprint("- Position: " .. tostring(char:GetPivot().Position) .. "\n")
    end
end

rconsoleprint("\n=== Game Statistics ===\n")
rconsoleprint("Active Players: " .. #Players:GetPlayers() .. "\n")
rconsoleprint("Max Players: " .. Players.MaxPlayers .. "\n")
rconsoleprint("Server Uptime: " .. math.floor(Stats.DataReceiveKbps:GetValue()) .. " seconds\n")
rconsoleprint("Network Receive: " .. math.floor(Stats.DataReceiveKbps:GetValue()) .. " KB/s\n")
rconsoleprint("Network Send: " .. math.floor(Stats.DataSendKbps:GetValue()) .. " KB/s\n")
