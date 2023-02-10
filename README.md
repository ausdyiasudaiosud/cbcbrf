

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()


                        local Window = Library.CreateLib("Penis Ware (BY KLO EW HE LIKES DICK UP HIS BUTT)", "BloodTheme")


                        local Tab = Window:NewTab("Da Hood Locks!")


              local Section = Tab:NewSection("ez kid")

                Section:NewButton("W silent aim", "this shit is so op on high ping too", function()
                    -- 0.138
-- 0.11243
loadstring(game:HttpGet("https://raw.githubusercontent.com/topillesrevenge/Streamable-Silent/main/Main"))()
DaHoodSettings.Prediction = 0.121
Aiming.TargetPart = {"Head", "LeftHand", "RightHand", "LeftLowerArm", "RightLowerArm", "LeftUpperArm", "RightUpperArm", "LeftFoot", "LeftLowerLeg", "UpperTorso", "HumanoidRootPart", "LeftUpperLeg", "RightLowerLeg", "RightFoot", "LowerTorso"}
Aiming.FOV = 50
Aiming.FOVSides = 25
Aiming.HitChance = 400
Aiming.ShowFOV = false
    print("Clicked")
end)

Section:NewButton("Anti-Lock Resolver", "resolver only works on some antis", function()
    local RunService = game:GetService("RunService")
 
RunService.Heartbeat:Connect(function()
    pcall(function()
        for i,v in pairs(game.Players:GetChildren()) do
            if v.Name ~= game.Players.LocalPlayer.Name then
                local hrp = v.Character.HumanoidRootPart
                hrp.Velocity = Vector3.new(hrp.Velocity.X, 0, hrp.Velocity.Z)
                hrp.AssemblyLinearVelocity = Vector3.new(hrp.Velocity.X, 0, hrp.Velocity.Z)
            end
        end
    end)
end)
    print("Clicked")
end)

Section:NewButton("Purple DOT", "OPPPPPPOPP", function()
    local Settings = { AimLock = { Enabled = true, Aimlockkey = "q", Prediction = 0.130340, Aimpart = 'HumanoidRootPart', Notifications = true }, Settings = { Thickness = 3.5, Transparency = 1, Color = Color3.fromRGB(106, 13, 173), FOV = true } } local CurrentCamera = game:GetService("Workspace").CurrentCamera local Inset = game:GetService("GuiService"):GetGuiInset().Y local RunService = game:GetService("RunService") local Mouse = game.Players.LocalPlayer:GetMouse() local LocalPlayer = game.Players.LocalPlayer local Line = Drawing.new("Line") local Circle = Drawing.new("Circle") local Plr = game.Players.LocalPlayer Mouse.KeyDown:Connect(function(KeyPressed) if KeyPressed == (Settings.AimLock.Aimlockkey) then if Settings.AimLock.Enabled == true then Settings.AimLock.Enabled = false if Settings.AimLock.Notifications == true then Plr = FindClosestPlayer() game.StarterGui:SetCore("SendNotification", { Title = "p", Text = "Unlocked" }) end else Plr = FindClosestPlayer() Settings.AimLock.Enabled = true if Settings.AimLock.Notifications == true then game.StarterGui:SetCore("SendNotification", { Title = "p", Text = "Locked On : " .. tostring(Plr.Character.Humanoid.DisplayName) }) end end end end) function FindClosestPlayer() local ClosestDistance, ClosestPlayer = math.huge, nil; for _, Player in next, game:GetService("Players"):GetPlayers() do if Player ~= LocalPlayer then local Character = Player.Character if Character and Character.Humanoid.Health > 1 then local Position, IsVisibleOnViewPort = CurrentCamera:WorldToViewportPoint(Character.HumanoidRootPart .Position) if IsVisibleOnViewPort then local Distance = (Vector2.new(Mouse.X, Mouse.Y) - Vector2.new(Position.X, Position.Y)).Magnitude if Distance < ClosestDistance then ClosestPlayer = Player ClosestDistance = Distance end end end end end return ClosestPlayer, ClosestDistance end RunService.Heartbeat:connect(function() if Settings.AimLock.Enabled == true then local Vector = CurrentCamera:WorldToViewportPoint(Plr.Character[Settings.AimLock.Aimpart].Position + (Plr.Character[Settings.AimLock.Aimpart].Velocity * Settings.AimLock.Prediction)) Line.Color = Settings.Settings.Color Line.Transparency = Settings.Settings .Transparency Line.Thickness = Settings.Settings .Thickness Line.From = Vector2.new(Mouse.X, Mouse.Y + Inset) Line.To = Vector2.new(Vector.X, Vector.Y) Line.Visible = true Circle.Position = Vector2.new(Mouse.X, Mouse.Y + Inset) Circle.Visible = Settings.Settings.FOV Circle.Thickness = 1.5 Circle.Thickness = 2 Circle.Radius = 60 Circle.Color = Settings.Settings.Color elseif Settings.AimLock.FOV == true then Circle.Visible = true else Circle.Visible = false Line.Visible = false end end) local mt = getrawmetatable(game) local old = mt.__namecall setreadonly(mt, false) mt.__namecall = newcclosure(function(...) local args = {...} if Settings.AimLock.Enabled and getnamecallmethod() == "FireServer" and args[2] == "MousePos" then args[3] = Plr.Character[Settings.AimLock.Aimpart].Position + (Plr.Character[Settings.AimLock.Aimpart].Velocity * Settings.AimLock.Prediction) return old(unpack(args)) end return old(...) end)
    print("Clicked")
end)

Section:NewButton("Anti-Lock (Z)", "W anti lock", function()
    
--// Created By Nosssa supports mostly, all hood games!
 
--// Roblox Group ( TeamNosss! ): https://www.roblox.com/groups/16003304/TeamNosss#!/about
 
getgenv().AntiLockKeybind = (  "z"  )
 
getgenv().Notifications = true
 
loadstring(game:HttpGet("https://raw.githubusercontent.com/Nosssa/NossLock/main/My600lbLife", true))();

    print("Clicked")
end)

Section:NewButton("Best Cam-Lock (E)", "Hold E", function()
    local Aiming = loadstring(game:HttpGet("https://pastebin.com/raw/YmUFTisy", true))()
    Aiming.TeamCheck(false)
     
    
    local Workspace = game:GetService("Workspace")
    local Players = game:GetService("Players")
    local RunService = game:GetService("RunService")
    local UserInputService = game:GetService("UserInputService")
    
    
    local LocalPlayer = Players.LocalPlayer
    local Mouse = LocalPlayer:GetMouse()
    local CurrentCamera = Workspace.CurrentCamera
    
    local DaHoodSettings = {
        SilentAim = true,
        AimLock = true,
        Prediction = 0.11923,
        AimLockKeybind = Enum.KeyCode.E
    }
    getgenv().DaHoodSettings = DaHoodSettings
    
    
    function Aiming.Check()
    -------------
        if not (Aiming.Enabled == true and Aiming.Selected ~= LocalPlayer and Aiming.SelectedPart ~= nil) then
            return false
        end
    
        -- // Check if downed
        local Character = Aiming.Character(Aiming.Selected)
        local KOd = Character:WaitForChild("BodyEffects")["K.O"].Value
        local Grabbed = Character:FindFirstChild("GRABBING_CONSTRAINT") ~= nil
    
        -- // Check B
        if (KOd or Grabbed) then
            return false
        end
    
        -- //
        return true
    end
    
    -- // Hook
    local __index
    __index = hookmetamethod(game, "__index", function(t, k)
        -- // Check if it trying to get our mouse's hit or target and see if we can use it
        if (t:IsA("Mouse") and (k == "Hit" or k == "Target") and Aiming.Check()) then
            local SelectedPart = Aiming.SelectedPart
    
            -- // Hit/Target
            if (DaHoodSettings.SilentAim and (k == "Hit" or k == "Target")) then
                -- // Hit to account prediction
                local Hit = SelectedPart.CFrame + (SelectedPart.Velocity * DaHoodSettings.Prediction)
    
                -- // Return modded val
                return (k == "Hit" and Hit or SelectedPart)
            end
        end
    
        -- // Return
        return __index(t, k)
    end)
    
    -- // Aimlock
    RunService:BindToRenderStep("AimLock", 0, function()
        if (DaHoodSettings.AimLock and Aiming.Check() and UserInputService:IsKeyDown(DaHoodSettings.AimLockKeybind)) then
            -- // Vars
            local SelectedPart = Aiming.SelectedPart
    
            -- // Hit to account prediction
            local Hit = SelectedPart.CFrame + (SelectedPart.Velocity * DaHoodSettings.Prediction)
    
            CurrentCamera.CFrame = CFrame.lookAt(CurrentCamera.CFrame.Position, Hit.Position)
        end
        end)

    print("Clicked")
end)

Section:NewButton("Dot + Block Lock (Only for DH)", "ONYL FOR DH U FUCKING  RETARD", function()
    -- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local TextLabel = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

TextLabel.Parent = ScreenGui
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 0.700
TextLabel.Position = UDim2.new(0, 0, 0.3, 0)
TextLabel.Size = UDim2.new(0, 151, 0, 31)
TextLabel.Font = Enum.Font.ArialBold
TextLabel.TextColor3 = Color3.fromRGB(155, 25, 65)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

_G.KEY = "q"
_G.PART = "LowerTorso"
_G.PRED = 0.043
_G.Frame = Vector3.new(0,0.53,0)
_G.AIR = -0.5
_G.SHIT = 0.1


local CC = game:GetService "Workspace".CurrentCamera
local Plr
local enabled = false
local accomidationfactor = 0.155
local mouse = game.Players.LocalPlayer:GetMouse()
local placemarker = Instance.new("Part", game.Workspace)
local guimain = Instance.new("Folder", game.CoreGui)

getgenv().makemarker = function(Parent, Adornee, Color, Size, Size2)
    local e = Instance.new("BillboardGui", Parent)
    e.Name = "PP"
    e.Adornee = Adornee
    e.Size = UDim2.new(Size, Size2, Size, Size2)
    e.AlwaysOnTop = true
    local a = Instance.new("Frame", e)
    a.Size = UDim2.new(4, 0, 4, 0)
    a.BackgroundTransparency = 0.1
    a.BackgroundColor3 = Color
    local g = Instance.new("UICorner", a)
    g.CornerRadius = UDim.new(50, 50)
    return (e)
end

local data = game.Players:GetPlayers()
function noob(player)
    local character
    repeat
        wait()
    until player.Character
    local handler = makemarker(guimain, player.Character:WaitForChild(_G.PART), Color3.fromRGB(255, 255, 255), 0.0, 0)
    handler.Name = player.Name
    player.CharacterAdded:connect(
        function(Char)
            handler.Adornee = Char:WaitForChild(_G.PART)
        end
    )

    local TextLabel = Instance.new("TextLabel", handler)
    TextLabel.BackgroundTransparency = 1
    TextLabel.Position = UDim2.new(0, 0, 0, -50)
    TextLabel.Size = UDim2.new(0, 100, 0, 100)
    TextLabel.Font = Enum.Font.SourceSansSemibold
    TextLabel.TextSize = 14
    TextLabel.TextColor3 = Color3.new(1, 1, 1)
    TextLabel.TextStrokeTransparency = 0
    TextLabel.TextYAlignment = Enum.TextYAlignment.Bottom
    TextLabel.Text = "Name: " .. player.Name
    TextLabel.ZIndex = 10

    spawn(
        function()
            while wait() do
                if player.Character then
                --TextLabel.Text = player.Name.." | Bounty: "..tostring(player:WaitForChild("leaderstats").Wanted.Value).." | "..tostring(math.floor(player.Character:WaitForChild("Humanoid").Health))
                end
            end
        end
    )
end

for i = 1, #data do
    if data[i] ~= game.Players.LocalPlayer then
        noob(data[i])
    end
end

game.Players.PlayerAdded:connect(
    function(Player)
        noob(Player)
    end
)

game.Players.PlayerRemoving:Connect(
    function(player)
        guimain[player.Name]:Destroy()
    end
)

spawn(
    function()
        placemarker.Anchored = true
        placemarker.CanCollide = false
        placemarker.Size = Vector3.new(0.1, 0.1, 0.1)
        placemarker.Transparency = _G.SHIT
        makemarker(placemarker, placemarker, Color3.fromRGB(255, 255, 255), 0.20, 0)
    end
)

mouse.KeyDown:Connect(
    function(k)
        if k ~= _G.KEY then
            return
        end
        if enabled then
            -- guimain[Plr.Name].Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            enabled = false
            TextLabel.TextColor3 = Color3.fromRGB(255, 20, 75)
            TextLabel.Text = "------"
        else
            --guimain[Plr.Name].Frame.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
            enabled = true
            Plr = getClosestPlayerToCursor()
            TextLabel.TextColor3 = Color3.fromRGB(12, 255, 0)
            TextLabel.Text = Plr.Character.Humanoid.DisplayName
        end
    end)

function getClosestPlayerToCursor()
    local closestPlayer
    local shortestDistance = math.huge

    for i, v in pairs(game.Players:GetPlayers()) do
        if
            v ~= game.Players.LocalPlayer and v.Character and v.Character:FindFirstChild("Humanoid") and
                v.Character.Humanoid.Health ~= 0 and
                v.Character:FindFirstChild(_G.PART)
         then
            local pos = CC:WorldToViewportPoint(v.Character.PrimaryPart.Position)
            local magnitude = (Vector2.new(pos.X, pos.Y) - Vector2.new(mouse.X, mouse.Y)).magnitude
            if magnitude < shortestDistance then
                closestPlayer = v
                shortestDistance = magnitude
            end
        end
    end
    return closestPlayer
end

game:GetService "RunService".Stepped:connect(
    function()
        if enabled and Plr.Character and Plr.Character:FindFirstChild(_G.PART) then
            placemarker.CFrame =
                CFrame.new(Plr.Character[_G.PART].Position + _G.Frame + (Plr.Character[_G.PART].Velocity * accomidationfactor))
        else
            placemarker.CFrame = CFrame.new(0, 9999, 0)
        end
    end
)

local mt = getrawmetatable(game)
local old = mt.__namecall
setreadonly(mt, false)
mt.__namecall =
    newcclosure(
    function(...)
        local args = {...}
        if enabled and getnamecallmethod() == "FireServer" and args[2] == "UpdateMousePos" then
            args[3] = Plr.Character[_G.PART].Position+ _G.Frame + (Plr.Character[_G.PART].Velocity * accomidationfactor)
            return old(unpack(args))
        end
        return old(...)
    end
)

game.Players.LocalPlayer.Chatted:Connect(
    function(Chat)
        if Chat == "print" then
            print(accomidationfactor)
        end
    end
)

game.Players.LocalPlayer.Chatted:Connect(
    function(Chat)
        if Chat == "Code:1029" then

            _G.KEY = nil
            _G.AIR = nil
            _G.PART = nil
            _G.PRED = nil
            TextLabel.Visible = false


        end
    end
)

game.Players.LocalPlayer.Chatted:Connect(
    function(Chat)
        if Chat == "Code:1030" then

        _G.KEY = "q"
        _G.PART = "Humanoid"
        _G.PRED = 0.12945
        _G.Frame = Vector3.new(0,0.0,0)
        _G.AIR = -0.5
        _G.SHIT = 1


        end
    end
)



game.Players.LocalPlayer.Chatted:Connect(
    function(Chat)
        if Chat == "P+" then


            _G.PRED = _G.PRED+0.001



        end
    end
)

game.Players.LocalPlayer.Chatted:Connect(
    function(Chat)
        if Chat == "P-" then

            _G.PRED = _G.PRED-0.001



        end
    end
)




while wait() do
    local ping = game:GetService("Stats").Network.ServerStatsItem["Data Ping"]:GetValueString()
    local Value = tostring(ping)
    local pingValue = Value:split(" ")
    local PingNumber = pingValue[1]
    
 accomidationfactor = PingNumber / 1000 + _G.PRED
end
    print("Clicked")
end)

                        local Tab = Window:NewTab("Extras")

            local Section = Tab:NewSection("Extra shit")
Section:NewButton("Fly (X)", "fuck u think", function()
local plr = game.Players.LocalPlayer
local mouse = plr:GetMouse()

localplayer = plr

if workspace:FindFirstChild("Core") then
workspace.Core:Destroy()
end

local Core = Instance.new("Part")
Core.Name = "Core"
Core.Size = Vector3.new(0.05, 0.05, 0.05)

spawn(function()
Core.Parent = workspace
local Weld = Instance.new("Weld", Core)
Weld.Part0 = Core
Weld.Part1 = localplayer.Character.LowerTorso
Weld.C0 = CFrame.new(0, 0, 0)
end)

workspace:WaitForChild("Core")

local torso = workspace.Core
flying = true
local speed=10
local keys={a=false,d=false,w=false,s=false}
local e1
local e2
local function start()
local pos = Instance.new("BodyPosition",torso)
local gyro = Instance.new("BodyGyro",torso)
pos.Name="EPIXPOS"
pos.maxForce = Vector3.new(math.huge, math.huge, math.huge)
pos.position = torso.Position
gyro.maxTorque = Vector3.new(9e9, 9e9, 9e9)
gyro.cframe = torso.CFrame
repeat
wait()
localplayer.Character.Humanoid.PlatformStand=true
local new=gyro.cframe - gyro.cframe.p + pos.position
if not keys.w and not keys.s and not keys.a and not keys.d then
speed=5
end
if keys.w then
new = new + workspace.CurrentCamera.CoordinateFrame.lookVector * speed
speed=speed+0
end
if keys.s then
new = new - workspace.CurrentCamera.CoordinateFrame.lookVector * speed
speed=speed+0
end
if keys.d then
new = new * CFrame.new(speed,0,0)
speed=speed+0
end
if keys.a then
new = new * CFrame.new(-speed,0,0)
speed=speed+0
end
if speed>10 then
speed=5
end
pos.position=new.p
if keys.w then
gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(-math.rad(speed*0),0,0)
elseif keys.s then
gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(math.rad(speed*0),0,0)
else
gyro.cframe = workspace.CurrentCamera.CoordinateFrame
end
until flying == false
if gyro then gyro:Destroy() end
if pos then pos:Destroy() end
flying=false
localplayer.Character.Humanoid.PlatformStand=false
speed=10
end
e1=mouse.KeyDown:connect(function(key)
if not torso or not torso.Parent then flying=false e1:disconnect() e2:disconnect() return end
if key=="w" then
keys.w=true
elseif key=="s" then
keys.s=true
elseif key=="a" then
keys.a=true
elseif key=="d" then
keys.d=true
elseif key=="x" then
if flying==true then
flying=false
else
flying=true
start()
end
end
end)
e2=mouse.KeyUp:connect(function(key)
if key=="w" then
keys.w=false
elseif key=="s" then
keys.s=false
elseif key=="a" then
keys.a=false
elseif key=="d" then
keys.d=false
end
end)
start()

    print("Clicked")
end)

Section:NewButton("SPEEEEEEEDDD", "lol superman", function()
    getgenv().WalkSpeedValue = 100; --set your desired walkspeed here
    local Player = game:service'Players'.LocalPlayer;
    Player.Character.Humanoid:GetPropertyChangedSignal'WalkSpeed':Connect(function()
    Player.Character.Humanoid.WalkSpeed = getgenv().WalkSpeedValue;
    end)
    Player.Character.Humanoid.WalkSpeed = getgenv().WalkSpeedValue;
    
    print("Clicked")
end)

Section:NewButton("Fake OP Macro", "BRRRR", function()
local Player = game:GetService("Players").LocalPlayer
            local Mouse = Player:GetMouse()
            local SpeedGlitch = false
            Mouse.KeyDown:Connect(function(Key)
                if Key == "q" then
                    SpeedGlitch = not SpeedGlitch
                    if SpeedGlitch == true then
                        repeat game:GetService("RunService").Heartbeat:wait()
                            keypress(0x49)
                            game:GetService("RunService").Heartbeat:wait()
                            keypress(0x4F)
                            game:GetService("RunService").Heartbeat:wait()
                            keyrelease(0x49)
                            game:GetService("RunService").Heartbeat:wait()
                            keyrelease(0x4F)
                            game:GetService("RunService").Heartbeat:wait()
                        until SpeedGlitch == false
                    end
                end
            end)
    print("Clicked")
end)

local Tab = Window:NewTab("Look rich")

            local Section = Tab:NewSection("broke ass nigga")

            Section:NewButton("Look rich (V)", "V to Toggle", function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/RobloxHackerProLuaStuff/avatar-editor-thing/main/headless.lua"))()

    print("Clicked")
end)
