local blacklisted = {
	2330443164
}

local blacklistReason = "Blacklisted."

game.Players.PlayerAdded:Connect(function(player)
	for i,v in pairs(blacklisted) do
		if v == player.UserId then
			player:Kick(blacklistReason)
		end
	end
end)
