local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Alpha script prtty much v3", HidePremium = false, Introtext = "script", SaveConfig = true, ConfigFolder = "script"})

OrionLib:MakeNotification({
	Name = "open gui",
	Content = "loading",
	Image = "rbxassetid://4483345998",
	Time = 5
})

function autofarmF()
    while _G.autofarmF == true do
game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("Shop"):FireServer("fish",false,true)
game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("Shop"):FireServer("fish",false,false)
        wait(12)
     end
    end

function autofarmG()
    while _G.autofarmG == true do
game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("Shop"):FireServer("gold",false,true)
game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("Shop"):FireServer("gold",false,false)
        wait(12)
     end
    end

function autofarmGP()
    while _G.autofarmGP == true do
game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("Shop"):FireServer("gunpowder",false,true)
game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("Shop"):FireServer("gunpowder",false,false)
        wait(12)
     end
    end

local TutTab = Window:MakeTab({
	Name = "auto farm money",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = TutTab:AddSection({
	Name = "auto farm money"
})

TutTab:AddToggle({
	Name = "AutoFish",
	Default = false,
	Callback = function(Value)
	   _G.autofarmF = Value
    autofarmF()
	end    
})

TutTab:AddToggle({
	Name = "AutoGold",
	Default = false,
	Callback = function(Value)
	   _G.autofarmG = Value
    autofarmG()
	end    
})

TutTab:AddToggle({
	Name = "AutoGunpowder",
	Default = false,
	Callback = function(Value)
	   _G.autofarmGP = Value
    autofarmGP()
	end    
})

Tab:AddToggle({
	Name = "a",
	Default = false,
	Callback = function(Value)
		print("Sus")
	end    
})

Tab:AddColorpicker({
	Name = "Colorpicker",
	Default = Color3.fromRGB(255,255,255),
	Callback = function(Value)
		print(Value)
	end	  
})

OrionLib:Init()
