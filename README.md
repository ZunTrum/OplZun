loadstring(game:HttpGet("https://raw.githubusercontent.com/Trolo2014/IntrestingScript/refs/heads/main/SniperByShawn4444.lua"))()
------------Debug Files Include So Far Players/Servers Collected And Rate Limit Status
--for i,v in pairs(workspace.ShawnSniper:GetChildren()) do
--print(v)
--end


local PlaceId = 8737602449
local Username = "Roblox"

workspace.ShawnSniper.SearchTarget.Value = tostring(tostring(PlaceId)..":"..Username)
local Status = workspace.ShawnSniper.OutPut.Changed:Wait() -- Changes After Scan Is Finished

if string.find(Status, "-") then 
game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceId,Status)
else
wait(0) game.StarterGui:SetCore("SendNotification", {Title = "ShawnSniper";Text = Status;Duration = 10;})
end
