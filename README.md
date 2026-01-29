-- Salir del juego al presionar la tecla T

local UserInputService = game:GetService("UserInputService")
local Players = game:GetService("Players")

local player = Players.LocalPlayer

UserInputService.InputBegan:Connect(function(input, gameProcessed)
	if gameProcessed then return end

	if input.KeyCode == Enum.KeyCode.T then
		player:Kick("Saliste del juego con la tecla T")
	end
end)
