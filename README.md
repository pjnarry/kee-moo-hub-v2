local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/GreenDeno/Venyx-UI-Library/main/source.lua"))()
local venyx = library.new("Keemo HUB", 5013109572)

local themes = {
	Background = Color3.fromRGB(25, 25, 25),
	Glow = Color3.fromRGB(0, 255, 255),
	Accent = Color3.fromRGB(10, 10, 10),
	LightContrast = Color3.fromRGB(21, 21, 21),
	DarkContrast = Color3.fromRGB(15, 15, 15),  
	TextColor = Color3.fromRGB(0, 255, 255)
}

local page = venyx:addPage("Auto Farm", 5012544693)
local section1 = page:addSection("AutoFarm")
local section2 = page:addSection("bypass")
local section3 = page:addSection("Auto Punch")
local section4 = page:addSection("Auto Legendary Sword")

section1:addToggle("Auto Farm", false, function(value)
    _G.AutoFarm = value
end)

_G.AutoQuest = true
section1:addToggle("Auto Quest",_G.AutoQuest,function(x)
    _G.AutoQuest = x
end)

section1:addToggle("AutoNewWorld",_G.AutoNew,function(value)
    _G.AutoNew = value
end)

section1:addToggle("Fast Attack", _G.FastAttack, function(value)
    _G.FastAttack = value
end)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
section2:addButton("bypass", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(30, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(5343.9809570312, 38.501129150391, 3976.4897460938)})
    tween:Play()
end)

local placeId = game.PlaceId
Magnet = true
if placeId == 2753915549 then
    OldWorld = true
elseif placeId == 4442272183 then
    NewWorld = true
elseif placeId == 7449423635 then
    ThreeWorld = true
end

_G.FarmSwiish = true
spawn(function()
    while wait() do
        pcall(function()
        _G.FarmSwiish = true
        wait(3)
        _G.FarmSwiish = false
        wait(3)
        end)
    end
end)


function Click()
    game:GetService'VirtualUser':CaptureController()
    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end
function CheckQuest()
local MyLevel = game.Players.LocalPlayer.Data.Level.Value
if OldWorld then
    if MyLevel == 1 or MyLevel <= 9 then 
        Ms = "Bandit [Lv. 5]"
        NaemQuest = "BanditQuest1"
        LevelQuest = 1
        NameMon = "Bandit"
        CFrameQuest = CFrame.new(1061.66699, 16.5166187, 1544.52905)
        PosQuest = Vector3.new(1061.66699, 16.5166187, 1544.52905)
        CFrameMon = CFrame.new(1199.31287, 52.2717781, 1536.91516)
        PosMon = Vector3.new(1199.31287, 52.2717781, 1536.91516)
    elseif MyLevel == 10 or MyLevel <= 14 then 
        Ms = "Monkey [Lv. 14]"
        NaemQuest = "JungleQuest"
        LevelQuest = 1
        NameMon = "Monkey"
        CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732)
        PosQuest = Vector3.new(-1604.12012, 36.8521118, 154.23732)
        CFrameMon = CFrame.new(-1772.4093017578, 60.860641479492, 54.872589111328)
        PosMon = Vector3.new(-1772.4093017578, 60.860641479492, 54.872589111328)
    elseif MyLevel == 15 or MyLevel <= 29 then 
        Ms = "Gorilla [Lv. 20]"
        NaemQuest = "JungleQuest"
        LevelQuest = 2
        NameMon = "Gorilla"
        CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732)
        PosQuest = Vector3.new(-1604.12012, 36.8521118, 154.23732)
        CFrameMon = CFrame.new(-1223.52808, 6.27936459, -502.292664)
        PosMon = Vector3.new(-1223.52808, 6.27936459, -502.292664)
    elseif MyLevel == 30 or MyLevel <= 39 then 
        Ms = "Pirate [Lv. 35]"
        NaemQuest = "BuggyQuest1"
        LevelQuest = 1
        NameMon = "Pirate"
        CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.16211)
        PosQuest = Vector3.new(-1139.59717, 4.75205183, 3825.16211)
        CFrameMon = CFrame.new(-1219.32324, 4.75205183, 3915.63452)
        PosMon = Vector3.new(-1219.32324, 4.75205183, 3915.63452)
    elseif MyLevel == 40 or MyLevel <= 59 then 
        Ms = "Brute [Lv. 45]"
        NaemQuest = "BuggyQuest1"
        LevelQuest = 2
        NameMon = "Brute"
        CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.1621)
        PosQuest = Vector3.new(-1139.59717, 4.75205183, 3825.1621)
        CFrameMon = CFrame.new(-1146.49646, 96.0936813, 4312.1333)
        PosMon = Vector3.new(-1146.49646, 96.0936813, 4312.1333)
    elseif MyLevel == 60 or MyLevel <= 74 then 
        Ms = "Desert Bandit [Lv. 60]"
        NaemQuest = "DesertQuest"
        LevelQuest = 1
        NameMon = "Desert Bandit"
        CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.9716)
        PosQuest = Vector3.new(897.031128, 6.43846416, 4388.9716)
        CFrameMon = CFrame.new(932.788818, 6.4503746, 4488.24609)
        PosMon = Vector3.new(932.788818, 6.4503746, 4488.24609)
    elseif MyLevel == 75 or MyLevel <= 89 then 
        Ms = "Desert Officer [Lv. 70]"
        NaemQuest = "DesertQuest"
        LevelQuest = 2
        NameMon = "Desert Officer"
        CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.9716)
        PosQuest = Vector3.new(897.031128, 6.43846416, 4388.9716)
        CFrameMon = CFrame.new(1580.03198, 4.61375761, 4366.86426)
        PosMon = Vector3.new(1580.03198, 4.61375761, 4366.86426)
    elseif MyLevel == 90 or MyLevel <= 99 then 
        Ms = "Snow Bandit [Lv. 90]"
        NaemQuest = "SnowQuest"
        LevelQuest = 1
        NameMon = "Snow Bandits"
        CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482)
        PosQuest = Vector3.new(1384.14001, 87.272789, -1297.06482)
        CFrameMon = CFrame.new(1370.24316, 102.403511, -1411.52905)
        PosMon = Vector3.new(1370.24316, 102.403511, -1411.52905)
    elseif MyLevel == 100 or MyLevel <= 119 then 
        Ms = "Snowman [Lv. 100]"
        NaemQuest = "SnowQuest"
        LevelQuest = 2
        NameMon = "Snowman"
        CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482)
        PosQuest = Vector3.new(1384.14001, 87.272789, -1297.06482)
        CFrameMon = CFrame.new(1370.24316, 102.403511, -1411.52905)
        PosMon = Vector3.new(1370.24316, 102.403511, -1411.52905)
    elseif MyLevel == 120 or MyLevel <= 149 then 
        Ms = "Chief Petty Officer [Lv. 120]"
        NaemQuest = "MarineQuest2"
        LevelQuest = 1
        NameMon = "Chief Petty Officer"
        CFrameQuest = CFrame.new(-5035.0835, 28.6520386, 4325.29443)
        PosQuest = Vector3.new(-5035.0835, 28.6520386, 4325.29443)
        CFrameMon = CFrame.new(-4882.8623, 22.6520386, 4255.53516)
        PosMon = Vector3.new(-4882.8623, 22.6520386, 4255.53516)
    elseif MyLevel == 150 or MyLevel <= 174 then 
        Ms = "Sky Bandit [Lv. 150]"
        NaemQuest = "SkyQuest"
        LevelQuest = 1
        NameMon = "Sky Bandit"
        CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436)
        PosQuest = Vector3.new(-4841.83447, 717.669617, -2623.96436)
        CFrameMon = CFrame.new(-4970.74219, 294.544342, -2890.11353)
        PosMon = Vector3.new(-4970.74219, 294.544342, -2890.11353)
    elseif MyLevel == 175 or MyLevel <= 224 then 
        Ms = "Dark Master [Lv. 175]"
        NaemQuest = "SkyQuest"
        LevelQuest = 2
        NameMon = "Dark Master"
        CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436)
        PosQuest = Vector3.new(-4841.83447, 717.669617, -2623.96436)
        CFrameMon = CFrame.new(-5220.58594, 430.693298, -2278.17456)
        PosMon = Vector3.new(-5220.58594, 430.693298, -2278.17456)
    elseif MyLevel == 225 or MyLevel <= 274 then 
        Ms = "Toga Warrior [Lv. 225]"
        NaemQuest = "ColosseumQuest"
        LevelQuest = 1
        NameMon = "Toga Warrior"
        CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762)
        PosQuest = Vector3.new(-1576.11743, 7.38933945, -2983.30762)
        CFrameMon = CFrame.new(-1779.97583, 44.6077499, -2736.35474)
        PosMon = Vector3.new(-1779.97583, 44.6077499, -2736.35474)
    elseif MyLevel == 275 or MyLevel <= 299 then 
        Ms = "Gladiator [Lv. 275]"
        NaemQuest = "ColosseumQuest"
        LevelQuest = 2
        NameMon = "Gladiato"
        CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762)
        PosQuest = Vector3.new(-1576.11743, 7.38933945, -2983.30762)
        CFrameMon = CFrame.new(-1274.75903, 58.1895943, -3188.16309)
        PosMon = Vector3.new(-1274.75903, 58.1895943, -3188.16309)
    elseif MyLevel == 300 or MyLevel <= 329 then 
        Ms = "Military Soldier [Lv. 300]"
        NaemQuest = "MagmaQuest"
        LevelQuest = 1
        NameMon = "Military Soldier"
        CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998)
        PosQuest = Vector3.new(-5316.55859, 12.2370615, 8517.2998)
        CFrameMon = CFrame.new(-5363.01123, 41.5056877, 8548.47266)
        PosMon = Vector3.new(-5363.01123, 41.5056877, 8548.47266)
    elseif MyLevel == 300 or MyLevel <= 374 then 
        Ms = "Military Spy [Lv. 330]"
        NaemQuest = "MagmaQuest"
        LevelQuest = 2
        NameMon = "Military Spy"
        CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998)
        PosQuest = Vector3.new(-5316.55859, 12.2370615, 8517.2998)
        CFrameMon = CFrame.new(-5787.99023, 120.864456, 8762.25293)
        PosMon = Vector3.new(-5787.99023, 120.864456, 8762.25293)
    elseif MyLevel == 375 or MyLevel <= 399 then 
        Ms = "Fishman Warrior [Lv. 375]"
        NaemQuest = "FishmanQuest"
        LevelQuest = 1
        NameMon = "Fishman Warrior"
        CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504)
        PosQuest = Vector3.new(61122.5625, 18.4716396, 1568.16504)
        CFrameMon = CFrame.new(61163.8515625, 5.3073043823242, 1819.7841796875)
        PosMon = Vector3.new(61163.8515625, 5.3073043823242, 1819.7841796875)
    elseif MyLevel == 400 or MyLevel <= 449 then 
        Ms = "Fishman Commando [Lv. 400]"
        NaemQuest = "FishmanQuest"
        LevelQuest = 2
        NameMon = "Fishman Commando"
        CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504)
        PosQuest = Vector3.new(61122.5625, 18.4716396, 1568.16504)
        CFrameMon = CFrame.new(61163.8515625, 5.3073043823242, 1819.7841796875)
        PosMon = Vector3.new(61163.8515625, 5.3073043823242, 1819.7841796875)
    elseif MyLevel == 450 or MyLevel <= 474 then 
        Ms = "God's Guard [Lv. 450]"
        NaemQuest = "SkyExp1Quest"
        LevelQuest = 1
        NameMon = "God's Guards"
        CFrameQuest = CFrame.new(-4721.71436, 845.277161, -1954.20105)
        PosQuest = Vector3.new(-4721.71436, 845.277161, -1954.20105)
        CFrameMon = CFrame.new(-4716.95703, 853.089722, -1933.925427)
        PosMon = Vector3.new(-4716.95703, 853.089722, -1933.925427)
    elseif MyLevel == 475 or MyLevel <= 524 then 
        Ms = "Shanda [Lv. 475]"
        NaemQuest = "SkyExp1Quest"
        LevelQuest = 2
        NameMon = "Shandas"
        CFrameQuest = CFrame.new(-7863.63672, 5545.49316, -379.826324)
        PosQuest = Vector3.new(-7863.63672, 5545.49316, -379.826324)
        CFrameMon = CFrame.new(-7685.12354, 5601.05127, -443.171509)
        PosMon = Vector3.new(-7685.12354, 5601.05127, -443.171509)
    elseif MyLevel == 525 or MyLevel <= 549 then 
        Ms = "Royal Squad [Lv. 525]"
        NaemQuest = "SkyExp2Quest"
        LevelQuest = 1
        NameMon = "Royal Squad"
        CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802)
        PosQuest = Vector3.new(-7902.66895, 5635.96387, -1411.71802)
        CFrameMon = CFrame.new(-7685.02051, 5606.87842, -1442.729)
        PosMon = Vector3.new(-7685.02051, 5606.87842, -1442.729)
    elseif MyLevel == 550 or MyLevel <= 624 then 
        Ms = "Royal Soldier [Lv. 550]"
        NaemQuest = "SkyExp2Quest"
        LevelQuest = 2
        NameMon = "Royal Soldier"
        CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802)
        PosQuest = Vector3.new(-7902.66895, 5635.96387, -1411.71802)
        CFrameMon = CFrame.new(-7864.44775, 5661.94092, -1708.22351)
        PosMon = Vector3.new(-7864.44775, 5661.94092, -1708.22351)
    elseif MyLevel == 625 or MyLevel <= 649 then 
        Ms = "Galley Pirate [Lv. 625]"
        NaemQuest = "FountainQuest"
        LevelQuest = 1
        NameMon = "Galley Pirate"
        CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678)
        PosQuest = Vector3.new(5254.60156, 38.5011406, 4049.69678)
        CFrameMon = CFrame.new(5595.06982, 41.5013695, 3961.47095)
        PosMon = Vector3.new(5595.06982, 41.5013695, 3961.47095)
    elseif MyLevel >= 650 then 
        Ms = "Galley Captain [Lv. 650]"
        NaemQuest = "FountainQuest"
        LevelQuest = 2
        NameMon = "Galley Captain"
        CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678)
        PosQuest = Vector3.new(5254.60156, 38.5011406, 4049.69678)
        CFrameMon = CFrame.new(5658.5752, 38.5361786, 4928.93506)
        PosMon = Vector3.new(5658.5752, 38.5361786, 4928.93506)
    end
end
if NewWorld then
    if MyLevel == 700 or MyLevel <= 724 then 
        Ms = "Raider [Lv. 700]"
        NaemQuest = "Area1Quest"
        LevelQuest = 1
        NameMon = "Raider"
        CFrameQuest = CFrame.new(-424.080078, 73.0055847, 1836.91589)
        PosQuest = Vector3.new(-424.080078, 73.0055847, 1836.91589)
        CFrameMon = CFrame.new(-737.026123, 39.1748352, 2392.57959)
        PosMon = Vector3.new(-737.026123, 39.1748352, 2392.57959)
    elseif MyLevel == 725 or MyLevel <= 774 then 
        Ms = "Mercenary [Lv. 725]"
        NaemQuest = "Area1Quest"
        LevelQuest = 2
        NameMon = "Mercenary"
        CFrameQuest = CFrame.new(-424.080078, 73.0055847, 1836.91589)
        PosQuest = Vector3.new(-424.080078, 73.0055847, 1836.91589)
        CFrameMon = CFrame.new(-973.731995, 95.8733215, 1836.46936)
        PosMon = Vector3.new(-973.731995, 95.8733215, 1836.46936)
    elseif MyLevel == 775 or MyLevel <= 874 then 
        Ms = "Swan Pirate [Lv. 775]"
        NaemQuest = "Area2Quest"
        LevelQuest = 1
        NameMon = "Swan Pirate"
        CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321)
        PosQuest = Vector3.new(632.698608, 73.1055908, 918.666321)
        CFrameMon = CFrame.new(970.369446, 142.653198, 1217.3667)
        PosMon = Vector3.new(970.369446, 142.653198, 1217.3667)
    elseif MyLevel == 875 or MyLevel <= 899 then 
        Ms = "Marine Lieutenant [Lv. 875]"
        NaemQuest = "MarineQuest3"
        LevelQuest = 1
        NameMon = "Marine Lieutenant"
        CFrameQuest = CFrame.new(-2442.65015, 73.0511475, -3219.11523)
        PosQuest = Vector3.new(-2442.65015, 73.0511475, -3219.11523)
        CFrameMon = CFrame.new(-2913.26367, 73.0011826)
        PosMon = Vector3.new(-2913.26367, 73.0011826)
    elseif MyLevel == 900 or MyLevel <= 949 then 
        Ms = "Marine Captain [Lv. 900]"
        NaemQuest = "MarineQuest3"
        LevelQuest = 2
        NameMon = "Marine Captain"
        CFrameQuest = CFrame.new(-2442.65015, 73.0511475, -3219.11523)
        PosQuest = Vector3.new(-2442.65015, 73.0511475, -3219.11523)
        CFrameMon = CFrame.new(-1868.67688, 73.0011826, -3321.66333)
        PosMon = Vector3.new(-1868.67688, 73.0011826, -3321.66333)
    elseif MyLevel == 950 or MyLevel <= 974 then 
        Ms = "Zombie [Lv. 950]"
        NaemQuest = "ZombieQuest"
        LevelQuest = 1
        NameMon = "Zombie"
        CFrameQuest = CFrame.new(-5492.79395, 48.5151672, -793.710571)
        PosQuest = Vector3.new(-5492.79395, 48.5151672, -793.710571)
        CFrameMon = CFrame.new(-5634.83838, 126.067039, -697.665039)
        PosMon = Vector3.new(-5634.83838, 126.067039, -697.665039)
    elseif MyLevel == 975 or MyLevel <= 999 then 
        Ms = "Vampire [Lv. 975]"
        NaemQuest = "ZombieQuest"
        LevelQuest = 2
        NameMon = "Vampire"
        CFrameQuest = CFrame.new(-5492.79395, 48.5151672, -793.710571)
        PosQuest = Vector3.new(-5492.79395, 48.5151672, -793.710571)
        CFrameMon = CFrame.new(-6030.32031, 6.4377408, -1313.5564)
        PosMon = Vector3.new(-6030.32031, 6.4377408, -1313.5564)
    elseif MyLevel == 1000 or MyLevel <= 1049 then 
        Ms = "Snow Trooper [Lv. 1000]"
        NaemQuest = "SnowMountainQuest"
        LevelQuest = 1
        NameMon = "Snow Trooper"
        CFrameQuest = CFrame.new(604.964966, 401.457062, -5371.69287)
        PosQuest = Vector3.new(604.964966, 401.457062, -5371.69287)
        CFrameMon = CFrame.new(535.893433, 401.457062, -5329.6958)
        PosMon = Vector3.new(535.893433, 401.457062, -5329.6958)
    elseif MyLevel == 1050 or MyLevel <= 1099 then 
        Ms = "Winter Warrior [Lv. 1050]"
        NaemQuest = "SnowMountainQuest"
        LevelQuest = 2
        NameMon = "Winter Warrior"
        CFrameQuest = CFrame.new(604.964966, 401.457062, -5371.69287)
        PosQuest = Vector3.new(604.964966, 401.457062, -5371.69287)
        CFrameMon = CFrame.new(1223.7417, 454.575226, -5170.02148)
        PosMon = Vector3.new(1223.7417, 454.575226, -5170.02148)
    elseif MyLevel == 1100 or MyLevel <= 1124 then 
        Ms = "Lab Subordinate [Lv. 1100]"
        NaemQuest = "IceSideQuest"
        LevelQuest = 1
        NameMon = "Lab Subordinate"
        CFrameQuest = CFrame.new(-6060.10693, 15.9868021, -4904.7876)
        PosQuest = Vector3.new(-6060.10693, 15.9868021, -4904.7876)
        CFrameMon = CFrame.new(-5769.2041, 37.9288292, -4468.38721)
        PosMon = Vector3.new(-5769.2041, 37.9288292, -4468.38721)
    elseif MyLevel == 1125 or MyLevel <= 1174 then 
        Ms = "Horned Warrior [Lv. 1125]"
        NaemQuest = "IceSideQuest"
        LevelQuest = 2
        NameMon = "Horned Warrior"
        CFrameQuest = CFrame.new(-6060.10693, 15.9868021, -4904.7876)
        PosQuest = Vector3.new(-6060.10693, 15.9868021, -4904.7876)
        CFrameMon = CFrame.new(-6400.85889, 24.7645149, -5818.63574)
        PosMon = Vector3.new(-6400.85889, 24.7645149, -5818.63574)
    elseif MyLevel == 1175 or MyLevel <= 1199 then 
        Ms = "Magma Ninja [Lv. 1175]"
        NaemQuest = "FireSideQuest"
        LevelQuest = 1
        NameMon = "Magma Ninja"
        CFrameQuest = CFrame.new(-5431.09473, 15.9868021, -5296.53223)
        PosQuest = Vector3.new(-5431.09473, 15.9868021, -5296.53223)
        CFrameMon = CFrame.new(-5496.65576, 58.6890411, -5929.76855)
        PosMon = Vector3.new(-5496.65576, 58.6890411, -5929.76855)
    elseif MyLevel == 1200 or MyLevel <= 1349 then 
        Ms = "Lava Pirate [Lv. 1200]"
        NaemQuest = "FireSideQuest"
        LevelQuest = 2
        NameMon = "Lava Pirate"
        CFrameQuest = CFrame.new(-5431.09473, 15.9868021, -5296.53223)
        PosQuest = Vector3.new(-5431.09473, 15.9868021, -5296.53223)
        CFrameMon = CFrame.new(-5169.71729, 34.1234779, -4669.73633)
        PosMon = Vector3.new(-5169.71729, 34.1234779, -4669.73633)
    elseif MyLevel == 1350 or MyLevel <= 1374 then 
        Ms = "Arctic Warrior [Lv. 1350]"
        NaemQuest = "FrostQuest"
        LevelQuest = 1
        NameMon = "Arctic Warrior"
        CFrameQuest = CFrame.new(5669.43506, 28.2117786, -6482.60107)
        PosQuest = Vector3.new(5669.43506, 28.2117786, -6482.60107)
        CFrameMon = CFrame.new(5995.07471, 57.3188477, -6183.47314)
        PosMon = Vector3.new(5995.07471, 57.3188477, -6183.47314)
    elseif MyLevel == 1375 or MyLevel <= 1424 then 
        Ms = "Snow Lurker [Lv. 1375]"
        NaemQuest = "FrostQuest"
        LevelQuest = 2
        NameMon = "Snow Lurker"
        CFrameQuest = CFrame.new(5669.43506, 28.2117786, -6482.60107)
        PosQuest = Vector3.new(5669.43506, 28.2117786, -6482.60107)
        CFrameMon = CFrame.new(5518.00684, 60.5559731, -6828.80518)
        PosMon = Vector3.new(5518.00684, 60.5559731, -6828.80518)
    elseif MyLevel == 1425 or MyLevel <= 1449 then 
        Ms = "Sea Soldier [Lv. 1425]"
        NaemQuest = "ForgottenQuest"
        LevelQuest = 1
        NameMon = "Sea Soldier"
        CFrameQuest = CFrame.new(-3052.99097, 236.881363, -10148.1943)
        PosQuest = Vector3.new(-3052.99097, 236.881363, -10148.1943)
        CFrameMon = CFrame.new(-3030.3696289063, 191.13464355469, -9859.7958984375)
        PosMon = Vector3.new(-3030.3696289063, 191.13464355469, -9859.7958984375)
    elseif MyLevel >= 1450 then 
        Ms = "Water Fighter [Lv. 1450]"
        NaemQuest = "ForgottenQuest"
        LevelQuest = 2
        NameMon = "Water Fighter"
        CFrameQuest = CFrame.new(-3052.99097, 236.881363, -10148.1943)
        PosQuest = Vector3.new(-3052.99097, 236.881363, -10148.1943)
        CFrameMon = CFrame.new(-3436.7727050781, 290.52191162109, -10503.438476563)
        PosMon = Vector3.new(-3436.7727050781, 290.52191162109, -10503.438476563)
    end
end
if ThreeWorld then
    if MyLevel == 1500 or MyLevel <= 1524 then
        Ms = "Pirate Millionaire [Lv. 1500]"
        NameQuest = "PiratePortQuest"
        LevelQuest = 1
        NameMon = "Pirate Millionaire"
        CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
        PosQuest = Vector3.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
        CFrameMon = CFrame.new(81.164993286133, 43.755737304688, 5724.7021484375)
        PosMon = Vector3.new(81.164993286133, 43.755737304688, 5724.7021484375)
    elseif MyLevel == 1525 or MyLevel <= 1574 then
        Ms = "Pistol Billionaire [Lv. 1525]"
        NameQuest = "PiratePortQuest"
        LevelQuest = 2
        NameMon = "Pistol Billionaire"
        CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
        CFrameMon = CFrame.new(81.164993286133, 43.755737304688, 5724.7021484375)
    elseif MyLevel == 1575 or MyLevel <= 1599 then
        Ms = "Dragon Crew Warrior [Lv. 1575]"
        NameQuest = "AmazonQuest"
        LevelQuest = 1
        NameMon = "Dragon Crew Warrior"
        CFrameQuest = CFrame.new(5832.83594, 51.6806107, -1101.51563, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)
        CFrameMon = CFrame.new(6241.9951171875, 51.522083282471, -1243.9771728516)
    elseif MyLevel == 1600 or MyLevel <= 1624 then
        Ms = "Dragon Crew Archer [Lv. 1600]"
        NameQuest = "AmazonQuest"
        LevelQuest = 2
        NameMon = "Dragon Crew Archer"
        CFrameQuest = CFrame.new(5832.83594, 51.6806107, -1101.51563, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)
        CFrameMon = CFrame.new(6488.9155273438, 383.38375854492, -110.66246032715)
    elseif MyLevel == 1625 or MyLevel <= 1649 then
        Ms = "Female Islander [Lv. 1625]"
        NameQuest = "AmazonQuest2"
        LevelQuest = 1
        NameMon = "Female Islander"
        CFrameQuest = CFrame.new(5448.86133, 601.516174, 751.130676, 0, 0, 1, 0, 1, -0, -1, 0, 0)
        CFrameMon = CFrame.new(4770.4990234375, 758.95520019531, 1069.8680419922)
    elseif MyLevel == 1650 or MyLevel <= 1699 then
        Ms = "Giant Islander [Lv. 1650]"
        NameQuest = "AmazonQuest2"
        LevelQuest = 2
        NameMon = "Giant Islander"
        CFrameQuest = CFrame.new(5448.86133, 601.516174, 751.130676, 0, 0, 1, 0, 1, -0, -1, 0, 0)
        CFrameMon = CFrame.new(4530.3540039063, 656.75695800781, -131.60952758789)
    elseif MyLevel == 1700 or MyLevel <= 1724 then
        Ms = "Marine Commodore [Lv. 1700]"
        NameQuest = "MarineTreeIsland"
        LevelQuest = 1
        NameMon = "Marine Commodore"
        CFrameQuest = CFrame.new(2180.54126, 27.8156815, -6741.5498, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)
        CFrameMon = CFrame.new(2490.0844726563, 190.4232635498, -7160.0502929688)
    elseif MyLevel == 1725 or MyLevel <= 1774 then
        Ms = "Marine Rear Admiral [Lv. 1725]"
        NameQuest = "MarineTreeIsland"
        LevelQuest = 2
        NameMon = "Marine Rear Admiral"
        CFrameQuest = CFrame.new(2180.54126, 27.8156815, -6741.5498, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)
        CFrameMon = CFrame.new(3951.3903808594, 229.11549377441, -6912.81640625)
    elseif MyLevel == 1775 or MyLevel <= 1799 then
        Ms = "Fishman Raider [Lv. 1775]"
        NameQuest = "DeepForestIsland3"
        LevelQuest = 1
        NameMon = "Fishman Raider"
        CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
        CFrameMon = CFrame.new(-10322.400390625, 390.94473266602, -8580.0908203125)
    elseif MyLevel == 1800 or MyLevel <= 1824 then
        Ms = "Fishman Captain [Lv. 1800]"
        NameQuest = "DeepForestIsland3"
        LevelQuest = 2
        NameMon = "Fishman Captain"
        CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
        CFrameMon = CFrame.new(-11194.541992188, 442.02795410156, -8608.806640625)
    elseif MyLevel == 1825 or MyLevel <= 1849 then
        Ms = "Forest Pirate [Lv. 1825]"
        NameQuest = "DeepForestIsland"
        LevelQuest = 1
        NameMon = "Forest Pirate"
        CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
        CFrameMon = CFrame.new(-13225.809570313, 428.19387817383, -7753.1245117188)
    elseif MyLevel == 1850 or MyLevel <= 1899 then
        Ms = "Mythological Pirate [Lv. 1850]"
        NameQuest = "DeepForestIsland"
        LevelQuest = 2
        NameMon = "Mythological Pirate"
        CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
        CFrameMon = CFrame.new(-13869.172851563, 564.95251464844, -7084.4135742188)
    elseif MyLevel == 1900 or MyLevel <= 1924 then
        Ms = "Jungle Pirate [Lv. 1900]"
        NameQuest = "DeepForestIsland2"
        LevelQuest = 1
        NameMon = "Jungle Pirate"
        CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
        CFrameMon = CFrame.new(-11982.221679688, 376.32522583008, -10451.415039063)
    elseif MyLevel == 1925 or MyLevel <= 1974 then
        Ms = "Musketeer Pirate [Lv. 1925]"
        NameQuest = "DeepForestIsland2"
        LevelQuest = 2
        NameMon = "Musketeer Pirate"
        CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
        CFrameMon = CFrame.new(-13282.3046875, 496.23684692383, -9565.150390625)
    elseif MyLevel == 1975 or MyLevel <= 1999 then
        Ms = "Reborn Skeleton [Lv. 1975]"
        NameQuest = "HauntedQuest1"
        LevelQuest = 1
        NameMon = "Reborn Skeleton"
        CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
        CFrameMon = CFrame.new(-8761.3154296875, 164.85829162598, 6161.1567382813)
    elseif MyLevel == 2000 or MyLevel <= 2024 then
        Ms = "Living Zombie [Lv. 2000]"
        NameQuest = "HauntedQuest1"
        LevelQuest = 2
        NameMon = "Living Zombie"
        CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
        CFrameMon = CFrame.new(-10093.930664063, 237.38233947754, 6180.5654296875)
    elseif MyLevel == 2025 or MyLevel <= 2049 then
        Ms = "Demonic Soul [Lv. 2025]"
        NameQuest = "HauntedQuest2"
        LevelQuest = 1
        NameMon = "Demonic Soul"
        CFrameQuest = CFrame.new(-9514.78027, 171.162918, 6078.82373, 0.301918149, 7.4535027e-09, 0.953333855, -3.22802141e-09, 1, -6.79604995e-09, -0.953333855, -1.02553133e-09, 0.301918149)
        CFrameMon = CFrame.new(-9466.72949, 171.162918, 6132.01514)
    elseif MyLevel >= 2050 then
        Ms = "Posessed Mummy [Lv. 2050]" 
        NameQuest = "HauntedQuest2"
        LevelQuest = 2
        NameMon = "Posessed Mummy"
        CFrameQuest = CFrame.new(-9514.78027, 171.162918, 6078.82373, 0.301918149, 7.4535027e-09, 0.953333855, -3.22802141e-09, 1, -6.79604995e-09, -0.953333855, -1.02553133e-09, 0.301918149)
        PosQuest = CFrame.new(-9514.78027, 171.162918, 6078.82373, 0.301918149, 7.4535027e-09, 0.953333855, -3.22802141e-09, 1, -6.79604995e-09, -0.953333855, -1.02553133e-09, 0.301918149)
        CFrameMon = CFrame.new(-9589.93848, 4.85058546, 6190.27197)
        PosMon = Vector3.new(-9589.93848, 4.85058546, 6190.27197)
    end
end
end

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

CheckQuest()
function EquipWeapon(ToolSe)
    if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
        local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
        wait(.4)
        game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
    end
end

spawn(function()
    while wait() do
        if _G.AutoFarm then
            autofarm()
        end
    end
end)


game:GetService("RunService").Heartbeat:Connect(
	function()
		if _G.AutoFarm then
			if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") then
				game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
			end
		end
	end
	)


local LocalPlayer = game:GetService("Players").LocalPlayer
local VirtualUser = game:GetService('VirtualUser')

function totarget(CFgo)
local tween_s = game:service"TweenService"
local info = TweenInfo.new((game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.Position - CFgo.Position).Magnitude/300, Enum.EasingStyle.Linear)
local tween, err = pcall(function()
    tween = tween_s:Create(game.Players.LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = CFgo})
    tween:Play()
end)
if not tween then return err end
end

function StopTween()
pcall(function()
    tween:Cancel()
    _G.StopTween = true
    wait()
    _G.StopTween = false
end)
end

function autofarm()
if _G.AutoFarm then
    if _G.AutoQuest then
        if LocalPlayer.PlayerGui.Main.Quest.Visible == false then
            StopTween()
            StatrMagnet = false
            CheckQuest()
            repeat totarget(CFrameQuest) wait() until _G.StopTween == true or not _G.AutoFarm or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQuest.Position).Magnitude <= 4
                wait(1.1)
                for i=1,10 do
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
                end
        elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
            CheckQuest()
            if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                pcall(
                    function()
                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            CheckQuest()  
                            if v.Name == Ms then
                                repeat wait()
                                    spawn(function()
                                        if game:GetService("Workspace").Enemies:FindFirstChild(Ms) and v.Humanoid.Health > 0 and v:FindFirstChild("Humanoid") then
                                            if LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text:find(NameMon) then
                                                totarget(v.HumanoidRootPart.CFrame * CFrame.new(0,45,0))
                                                PosHee = v.HumanoidRootPart.CFrame
                                                EquipWeapon(_G.SelectToolWeapon)
                                                PosHee = v.HumanoidRootPart.CFrame
                                                v.HumanoidRootPart.CanCollide = false
                                                v.HumanoidRootPart.Size = Vector3.new(50, 50, 50)
                                                StatrMagnet = true
                                            else
                                                StopTween()
                                                local args = {
                                                    [1] = "AbandonQuest"
                                                 }
                                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            end  
                                        else
                                            CheckQuest() 
                                            StatrMagnet = false
                                            repeat totarget(CFrameMon) wait() until _G.StopTween == true or not _G.AutoFarm or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameMon.Position).Magnitude <= 5
                                        end 
                                    end)
                                until not v.Parent or v.Humanoid.Health <= 0 or _G.AutoFarm == false or LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                CheckQuest() 
                                StatrMagnet = false
                            end
                        end
                    end
                )
            else
                CheckQuest()
                StatrMagnet = false
                repeat totarget(CFrameMon) wait() until _G.StopTween == true or not _G.AutoFarm or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameMon.Position).Magnitude <= 5
            end 
        end
    else
        CheckQuest()
        if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
            pcall(
                function()
                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        CheckQuest() 
                        if v.Name == Ms then
                            repeat wait()
                                if game:GetService("Workspace").Enemies:FindFirstChild(Ms) and v.Humanoid.Health > 0 and v:FindFirstChild("Humanoid") then
                                    totarget(v.HumanoidRootPart.CFrame * CFrame.new(0,45,0))
                                    EquipWeapon(_G.SelectToolWeapon)
                                    PosHee = v.HumanoidRootPart.CFrame
                                    v.HumanoidRootPart.CanCollide = false
                                    v.HumanoidRootPart.Size = Vector3.new(55, 55, 55)
                                    StatrMagnet = true
                                else
                                    CheckQuest() 
                                    StatrMagnet = false
                                    repeat totarget(CFrameMon) wait() until _G.StopTween == true or not _G.AutoFarm or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameMon.Position).Magnitude <= 8
                                end 
                            until not v.Parent or v.Humanoid.Health <= 0 or _G.AutoFarm == false
                            CheckQuest() 
                            StatrMagnet = false
                        end
                    end
                end
            )
        else
            CheckQuest()
            StatrMagnet = false
            repeat totarget(CFrameMon) wait() until _G.StopTween == true or not _G.AutoFarm or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameMon.Position).Magnitude <= 8
        end 
    end
end
end

function bring2()
    local plr = game.Players.LocalPlayer
    pcall(function()
        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
    end)
end
spawn(function()
    while wait(.1) do
        if _G.AutoFarm then
            bring2()
        end
    end
end)

spawn(function()
    while true do
        pcall(function()
            if _G.AutoFarm and StatrMagnet then
                CheckQuest()
                for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                    if v.Name == Ms and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                        if v.Name == "Factory Staff [Lv. 800]" or v.Name == "Dragon Crew Warrior [Lv. 1575]" or v.Name == "Dragon Crew Archer [Lv. 1600]" and (v.HumanoidRootPart.Position-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 200 then
                            if HideHitBlox then
                                v.HumanoidRootPart.Transparency = 1
                            else
                                v.HumanoidRootPart.Transparency = 70
                            end
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                            v.HumanoidRootPart.CFrame = PosHee
                        elseif v.Name == Ms and (v.HumanoidRootPart.Position-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 400 then
                            if HideHitBlox then
                                v.HumanoidRootPart.Transparency = 1
                            else
                                v.HumanoidRootPart.Transparency = 70
                            end
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                            v.HumanoidRootPart.CFrame = PosHee
                        end
                    end
                end
            end 
        end)
        wait()
    end
end)

coroutine.wrap(function()
    local Combat = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)
    local Cemara = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework.CameraShaker)
    Cemara.CameraShakeInstance.CameraShakeState = {FadingIn = 3, FadingOut = 2, Sustained = 0, Inactive = 1}
    function aa()
             Combat.activeController.timeToNextAttack = 0
             Combat.activeController.hitboxMagnitude = 150
             Combat.activeController.increment = 3
    end
    game:GetService("RunService").RenderStepped:Connect(function()
            if _G.FastAttack then
                pcall(function()
                    aa()
                end)
            end
    end) 
end)()
 
coroutine.wrap(function()
    function Click()
        game:GetService'VirtualUser':CaptureController()
        game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
    end
    game:GetService("RunService").RenderStepped:Connect(function()
        if _G.FastAttack then
            pcall(function()
                Click() 
            end)
        end
    end) 
end)()

local CombatFrameworkR = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework) 

local CameraShakerR = require(game.ReplicatedStorage.Util.CameraShaker)

spawn(function()
	for i = 1,math.huge do
		game:GetService("RunService").Heartbeat:wait()
		if _G.FastFarm then
			pcall(function()
                CameraShakerR:Stop()
                CombatFrameworkR.activeController.attacking = false
                CombatFrameworkR.activeController.timeToNextAttack = 120
                CombatFrameworkR.activeController.increment = 3
                CombatFrameworkR.activeController.hitboxMagnitude = 120
			end)
		end
		game:GetService("RunService").Heartbeat:wait()
	end
end)

spawn(function()
	game:GetService("RunService").Heartbeat:connect(function()
		pcall(function()
			if _G.FastFarm then
					VirtualUser:CaptureController()
					VirtualUser:ClickButton1(Vector2.new(851, 158), game:GetService("Workspace").Camera.CFrame)
			end
		end)
	end)
	game:GetService("RunService").Heartbeat:connect(function()
		pcall(function()
			if _G.FastFarm then
					VirtualUser:CaptureController()
					VirtualUser:ClickButton1(Vector2.new(851, 158), game:GetService("Workspace").Camera.CFrame)
			end
		end)
	end)
end)


Wapon = {}

spawn(function()
    while wait(1) do
        table.clear(Wapon)
        for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
            if v:IsA("Tool") then
                table.insert(Wapon ,v.Name)
            end
        end
        for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
            if v:IsA("Tool") then
                table.insert(Wapon, v.Name)
            end
        end
    end
end)

local SelectWeapona = section1:addDropdown("Select Weapon",Wapon,function(Value)
    _G.SelectToolWeapon = Value
    SelectToolWeaponOld = Value
end)

section1:addButton("Refresh Weapon", function()
end)

setfflag("HumanoidParallelRemoveNoPhysics", "False")
setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
setfflag("CrashPadUploadToBacktraceToBacktraceBaseUrl", "")
setfflag("CrashUploadToBacktracePercentage", "0")
setfflag("CrashUploadToBacktraceBlackholeToken", "")
setfflag("CrashUploadToBacktraceWindowsPlayerToken", "")

spawn(function()
    while true do game:GetService("RunService").RenderStepped:Wait()
        if Clip or _G.AutoFarm or _G.autoraid or _G.AutoFarmBone or _G.AutoFarmBon or _G.AutoHallowScythe or _G.FramBoss or _G.FarmLevel or _G.AutoNew or _G.AutoThird or _G.AutoSwan or _G.AutoSwanHop or _G.AutoPole or _G.AutoPoleHop or _G.AutoHakiRainbow or _G.AutoFastAttack or _G.AutoEliteHunter or _G.AutoEliteHunterHop or _G.AutoTushitaSword or _G.AutoTushitaSword or  _G.FramBoss or _G.AutoFarmAllBoss or _G.AutoCavender or _G.AutoCavenderHop or _G.Tween then
            if syn and  game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
                game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
            else
                pcall(function()
                    if not game:GetService("Workspace"):FindFirstChild("LOL") then
                        local LOL = Instance.new("Part")
                        LOL.Name = "LOL"
                        LOL.Parent = game.Workspace
                        LOL.Anchored = true
                        LOL.Transparency = 0.8
                        LOL.Size = Vector3.new(10,0.5,10)
                    elseif game:GetService("Workspace"):FindFirstChild("LOL") then
                        for _, v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
                            if v.Name == "HumanoidRootPart" or v.Name == "Head" or v.Name == "LeftHand" or v.Name == "RightHand" or v.Name == "LeftLowerArm" or v.Name == "RightLowerArm" or v.Name == "LeftUpperArm" or v.Name == "RightUpperArm" or v.Name == "LeftFoot" or v.Name == "LeftLowerLeg" or v.Name == "UpperTorso" or v.Name == "LeftUpperLeg" or v.Name == "RightFoot" or v.Name == "RightLowerLeg" or v.Name == "LowerTorso" or v.Name == "RightUpperLeg" then
                                v.CanCollide = false
                            end
                        end
                        game.Workspace["LOL"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 4,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
                    end
                end)
            end
        end
    end
end)

spawn(function()
    while wait(.1) do
        if _G.AutoNew then
            local MyLevel = game.Players.localPlayer.Data.Level.Value
            if MyLevel >= 700 and OldWorld then
                _G.AutoFarm = false
                _G.SelectToolWeapon = "Key"
                wait(0.5)
                local args = {
                    [1] = "DressrosaQuestProgress",
                    [2] = "Detective"
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                wait(0.5)
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Key") then
                    getgenv().tool = game.Players.LocalPlayer.Backpack:FindFirstChild("Key")
                    wait(.4)
                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
                end
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1347.7124, 37.3751602, -1325.6488)
                wait(0.5)
                function Click()
                    game:GetService'VirtualUser':CaptureController()
                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                end
                if game.Workspace.Enemies:FindFirstChild("Ice Admiral [Lv. 700] [Boss]") and game.Workspace.Map.Ice.Door.CanCollide == false and game.Workspace.Map.Ice.Door.Transparency == 1 then
                    CheckBoss = true
                    _G.SelectToolWeapon = SelectToolWeaponOld
                    for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                        if CheckBoss and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and v.Name == "Ice Admiral [Lv. 700] [Boss]" then
                            repeat wait(.1)
                                pcall(function() 
                                    v.HumanoidRootPart.Transparency = 0.5
                                    v.HumanoidRootPart.Size = Vector3.new(50, 50, 50)
                                    v.HumanoidRootPart.BrickColor = BrickColor.new("White")
                                    v.HumanoidRootPart.CanCollide = false
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame*CFrame.new(0, 45, 0)
                                    game:GetService'VirtualUser':CaptureController()
                                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                end)
                            until not CheckBoss or not v.Parent or v.Humanoid.Health <= 0
                        end
                    end
                    CheckBoss = false
                    wait(0.5)
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1166.23743, 7.65220165, 1728.36487)
                    wait(0.5)
                    local args = {
                        [1] = "TravelDressrosa" -- OLD WORLD to NEW WORLD
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                else
                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Key") then
                        getgenv().tool = game.Players.LocalPlayer.Backpack:FindFirstChild("Key")
                        wait(.4)
                        game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
                    end
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1347.7124, 37.3751602, -1325.6488)
                end 
            end
        end 
    end
end)


section4:addToggle("Auto Pole",false,function(value)
    _G.Pole = value
end)

spawn(function()
    while wait() do
        if _G.Pole then
            pcall(function()
                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                    if v.Name == "Thunder God [Lv. 575] [Boss]" then
                        repeat wait()
                            v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                            v.HumanoidRootPart.Transparency = 1
                            v.HumanoidRootPart.CanCollide = false
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(25, 0, 7)
                            if sethiddenproperty then
                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                            end
                        until v.Humanoid.Health == 0 or not _G.Pole
                    else
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-7911.14453, 5613.89795, -2272.67822, -0.585544586, -6.38371889e-09, 0.810640216, -2.4883267e-08, 1, -1.00988613e-08, -0.810640216, -2.60847095e-08, -0.585544586)
                    end
                end
            end)
        end
    end
end)
spawn(function()
    while wait() do
        if _G.Pole then
            pcall(function()
                game:GetService'VirtualUser':Button1Down(Vector2.new(0.9,0.9))
                game:GetService'VirtualUser':Button1Up(Vector2.new(0.9,0.9))
            end)
        end
    end
end)
spawn(function()
    while wait() do
        if _G.Pole then
            pcall(function ()
                EquipWeapon(_G.SelectToolWeapon)
            end)
        end
    end
end)

section3:addToggle("Auto Superhuman",false,function(value)
    Superhuman = value
    while Superhuman do wait()
        if Superhuman then
            if game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") or game.Players.LocalPlayer.Character:FindFirstChild("Combat") then
                local args = {
                    [1] = "BuyBlackLeg"
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end   
            if game.Players.LocalPlayer.Character:FindFirstChild("Superhuman") or game.Players.LocalPlayer.Backpack:FindFirstChild("Superhuman") then
                SelectToolWeapon = "Superhuman"
            end  
            if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") or game.Players.LocalPlayer.Character:FindFirstChild("Electro") or game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") or game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") or game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") or game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") then
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value <= 299 then
                    SelectToolWeapon = "Black Leg"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value <= 299 then
                    SelectToolWeapon = "Electro"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value <= 299 then
                    SelectToolWeapon = "Fishman Karate"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value <= 299 then
                    SelectToolWeapon = "Dragon Claw"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 300 then
                    local args = {
                        [1] = "BuyElectro"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 300 then
                    local args = {
                        [1] = "BuyElectro"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 300 then
                    local args = {
                        [1] = "BuyFishmanKarate"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 300 then
                    local args = {
                        [1] = "BuyFishmanKarate"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 300 then
                    local args = {
                        [1] = "BlackbeardReward",
                        [2] = "DragonClaw",
                        [3] = "1"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    local args = {
                        [1] = "BlackbeardReward",
                        [2] = "DragonClaw",
                        [3] = "2"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args)) 
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate").Level.Value >= 300 then
                    local args = {
                        [1] = "BlackbeardReward",
                        [2] = "DragonClaw",
                        [3] = "1"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    local args = {
                        [1] = "BlackbeardReward",
                        [2] = "DragonClaw",
                        [3] = "2"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args)) 
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 300 then
                    local args = {
                        [1] = "BuySuperhuman"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 300 then
                    local args = {
                        [1] = "BuySuperhuman"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end 
            end
        end
    end
end)

section3:addToggle("Auto Death Step",false,function(value)
    DeathStep = value
    while DeathStep do wait()
        if DeathStep then
            if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Backpack:FindFirstChild("Death Step") or game.Players.LocalPlayer.Character:FindFirstChild("Death Step") then
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 450 then
                    local args = {
                        [1] = "BuyDeathStep"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    SelectToolWeapon = "Death Step"
                end  
                if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 450 then
                    local args = {
                        [1] = "BuyDeathStep"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

                    SelectToolWeapon = "Death Step"
                end  
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value <= 449 then
                    SelectToolWeapon = "Black Leg"
                end 
            else 
                local args = {
                    [1] = "BuyBlackLeg"
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end
    end
end)

section4:addToggle("Auto LegebdarySword", nil, function(value)
	_G.LegebdarySword = Value    
end)

spawn(function()
	while wait(.1) do
		if _G.LegebdarySword then
			local args = {
				[1] = "LegendarySwordDealer",
				[2] = "1"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end 
	end
end)
spawn(function()
	while wait(.1) do
		if _G.LegebdarySword then
			local args = {
				[1] = "LegendarySwordDealer",
				[2] = "2"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end 
	end
end)
spawn(function()
	while wait(.1) do
		if _G.LegebdarySword then
			local args = {
				[1] = "LegendarySwordDealer",
				[2] = "3"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end 
	end
end)

local page = venyx:addPage("Stats", 5012544693)
local section1 = page:addSection("stats")

_G.Autostats = true
section1:addToggle("Auto stats", nil, function(value)
    _G.Autostats = Hee
end)

_G.Melee = false
section1:addToggle("Melee", nil, function(value)
    _G.Melee = value 
end)

_G.Defense = false
section1:addToggle("Defense", nil, function(value)
    _G.Defense = value 
end)

_G.Sword = false
section1:addToggle("Sword", nil, function(value)
    _G.Sword = value 
end)

_G.Gun = false
section1:addToggle("Gun", nil, function(value)
    _G.Gun = value
end)

_G.Fruit = false
section1:addToggle("Fruit", nil, function(value)
    _G.Fruit = value
end)

                                spawn(function()
                                    while wait(.1) do
                                        if _G.Autostats then
                                            pcall(function()
                                                local args = {
                                                    [1] = "AddPoint",
                                                    [2] = "Autostate",
                                                    [3] = PointStats
                                                }
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            end)
                                        end
                                    end
                                end)
                                spawn(function()
                                    while wait(.1) do
                                        if _G.Melee then
                                            pcall(function()
                                                local args = {
                                                    [1] = "AddPoint",
                                                    [2] = "Melee",
                                                    [3] = PointStats
                                                }
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            end)
                                        end
                                    end
                                end)
                                spawn(function()
                                    while wait(.1) do
                                        if _G.Gun then
                                            pcall(function()
                                                local args = {
                                                    [1] = "AddPoint",
                                                    [2] = "Gun",
                                                    [3] = PointStats
                                                }
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            end)
                                        end
                                    end
                                end)
                                spawn(function()
                                    while wait(.1) do
                                        if _G.Sword then
                                            pcall(function()
                                                local args = {
                                                    [1] = "AddPoint",
                                                    [2] = "Sword",
                                                    [3] = PointStats
                                                }
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            end)
                                        end
                                    end
                                end)
                                spawn(function()
                                    while wait(.1) do
                                        if _G.Fruit then
                                            pcall(function()
                                                local args = {
                                                    [1] = "AddPoint",
                                                    [2] = "Demon Fruit",
                                                    [3] = PointStats
                                                }
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            end)
                                        end
                                    end
                                end)

local page = venyx:addPage("Players", 5012544693)
local section1 = page:addSection("Auto Players")

section1:addToggle("Auto Bounty", nil, function(value)

end)

section1:addToggle("Auto Bounty Hop", nil, function(value)
end)

local SelectWeapona = section1:addDropdown("Select Weapon",Wapon,function(Value)
    _G.SelectToolWeapon = Value
    SelectToolWeaponOld = Value
end)

section1:addButton("Refresh Weapon", function()
end)

local page = venyx:addPage("Teleport", 5012544693)
local section1 = page:addSection("Teleport")

if OldWorld then
 section1:addButton("Sky", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(25, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-4910.12939, 0.0402221233, -2364.89673, 0.656839848, -1.20746089e-08, -0.754030108, -7.11362702e-08, 1, -7.798063e-08, 0.754030108, 1.0485968e-07, 0.656839848)})
    tween:Play()
 end)

section1:addButton("Colosseum", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(25, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-1441.97754, 7.28718901, -2853.65869, -0.616300642, 6.60886368e-09, -0.787510991, -3.19537357e-08, 1, 3.33988623e-08, 0.787510991, 4.57476581e-08, -0.616300642)})
    tween:Play()
end)

 section1:addButton("Ice", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(25, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(1127.5072, 7.30372715, -1160.7345, -0.900806129, 1.05486864e-08, 0.434221506, -4.50489246e-09, 1, -3.36388695e-08, -0.434221506, -3.2258221e-08, -0.900806129)})
    tween:Play()
 end)

 section1:addButton("Middle town", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(25, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-672.940308, 8.71331787, 1588.39099, 0.000854491896, 0, 0.999999642, -0, 1, -0, -0.999999642, 0, 0.000854491896)})
    tween:Play()
 end)

 section1:addButton("Jungle", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(25, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-1503.98962, 22.8521042, 356.070618, -0.952782273, -3.86338783e-08, -0.303654373, -2.50802934e-08, 1, -4.85348544e-08, 0.303654373, -3.86274053e-08, -0.952782273)})
    tween:Play()
 end)

 section1:addButton("Pirate Village", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(25, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-1163.81921, 4.7520504, 3813.68945, 0.963280737, 1.67412324e-08, -0.268496305, -7.28495619e-09, 1, 3.62156705e-08, 0.268496305, -3.29298757e-08, 0.963280737)})
    tween:Play()
 end)

 section1:addButton("Marine Fortress", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(20, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-4829.66455, 20.6520348, 4373.99951, 0.719505787, 6.85520618e-08, -0.694486439, -3.11971498e-08, 1, 6.63879476e-08, 0.694486439, -2.61005191e-08, 0.719505787)})
    tween:Play()
 end)

 section1:addButton("underwater city", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(20, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(3866.46606, 15.9686079, -1962.96741, 0.984092712, 7.21467019e-09, -0.177655771, 8.78178597e-09, 1, 8.92555363e-08, 0.177655771, -8.93958614e-08, 0.984092712)})
    tween:Play()
 end)

section1:addButton("Prison", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(20, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(4849.91553, 5.65205431, 735.943298, 0.192715883, 7.91147272e-08, 0.981254578, -4.15859098e-08, 1, -7.24587252e-08, -0.981254578, -2.68424181e-08, 0.192715883)})
    tween:Play()
 end)

 section1:addButton("Fountain City", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(20, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(5041.84277, 1.50127494, 4050.78296, 0.698421359, 1.49165214e-09, 0.715686798, -3.14754409e-08, 1, 2.86318915e-08, -0.715686798, -4.25236806e-08, 0.698421359)})
    tween:Play()
 end)

 section1:addButton("Desert", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(20, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(939.97113, 6.59366369, 4203.4209, 0.915271401, 5.87556359e-09, 0.402837723, -1.35914995e-08, 1, 1.62952638e-08, -0.402837723, -2.03897574e-08, 0.915271401)})
    tween:Play()
 end)
end

if NewWorld then

end

if ThreeWorld then
 section1:addButton("Port Town", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(30, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-276.035461, 8.25954914, 5337.32178, 0.972617269, -0.00287928735, -0.232394725, 0, 0.999923229, -0.0123886894, 0.232412577, 0.0120494533, 0.972542)})
    tween:Play()
 end)

 section1:addButton("Haunted Castle", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(30, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-9515.19629, 149.366547, 5759.15674, 0.999511123, 0.0012438203, 0.0312405042, 0, 0.999208331, -0.0397828296, -0.0312652551, 0.0397633798, 0.998719871)})
    tween:Play()
 end)

 section1:addButton("Hydra lsland", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(30, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(5229.1708984375, 603.91656494141, 344.92098999023)})
    tween:Play()
 end)

 section1:addButton("Floating Turtle", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(30, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-12017.297851562, 599.79119873047, -8523.1201171875)})
    tween:Play()
 end)

 section1:addButton("Mansionn", function()
    tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(30, Enum.EasingStyle.Linear)
    tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-12549.383789062, 337.1940612793, -7494.0498046875)})
    tween:Play()
 end)
end
local page = venyx:addPage("Misc", 5012544693)
local section1 = page:addSection("Buy")
local section2 = page:addSection("BuyHaki")
local section3 = page:addSection("NoClip")
local section4 = page:addSection("Redeem Code")

section1:addButton("BuyBlackLeg", function()
    local A_1 = "BuyBlackLeg"
    local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
    Event:InvokeServer(A_1)
end)

section1:addButton("BuyElectro", function()
    local A_1 = "BuyElectro"
    local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
    Event:InvokeServer(A_1)print("Clicked")
end)

section1:addButton("BuyFishmanKarate", function()
 local A_1 = "BuyFishmanKarate"
 local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
 Event:InvokeServer(A_1)print("Clicked")
end)

section1:addButton("BuyDragon Claw", function()
 local A_1 = "BlackbeardReward"
 local A_2 = "DragonClaw"
 local A_3 = "2"
 local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
Event:InvokeServer(A_1, A_2, A_3)
end)

section1:addButton("BuySuperhuman", function()
 local A_1 = "BuySuperhuman"
 local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
 Event:InvokeServer(A_1)print("Clicked")
end)

section1:addButton("BuySharkmankarate", function()
 local A_1 = "BuySharkmankarate"
 local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
 Event:InvokeServer(A_1)print("Clicked")
end)

section1:addButton("BuyDeathStep", function()
 local A_1 = "BuyDeathStep"
 local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
 Event:InvokeServer(A_1)print("Clicked")
end)

section1:addButton("BuyDragonTalon", function()
 local A_1 = "BuyDragonTalon"
 local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
 Event:InvokeServer(A_1)print("Clicked")
end)

section2:addButton("BuyGeppo", function()
local A_1 = "BuyHaki"
local A_2 = "Geppo"
local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
Event:InvokeServer(A_1, A_2)
end)

section2:addButton("BuySoru", function()
local A_1 = "BuyHaki"
local A_2 = "Soru"
local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
Event:InvokeServer(A_1, A_2)
end)

section2:addButton("BuyBuso", function()
local A_1 = "BuyHaki"
local A_2 = "Buso"
local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
Event:InvokeServer(A_1, A_2)
end)


_G.NoClip = true
section3:addToggle("NoClip", false, function(value)
    _G.NoClip = value
end)

section4:addButton("Redeem Code", function()
    function Redeem(Code)
        local args = {
            [1] = Code
        }
        game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(unpack(args))
        end
         
        local Code = {
            "3BVISITS",
            "UPD16",
            "THEGREATACE",
            "SUB2GAMERROBOT_EXP1",
            "StrawHatMaine",
            "Sub2OfficialNoobie",
            "SUB2NOOBMASTER123",
            "Sub2Daigrock",
            "Axiore",
            "TantaiGaming",
            "STRAWHATMAINE"
        }
    end)

game:GetService("RunService").Heartbeat:Connect(
function()
    if _G.NoClip or _G.Pole or _G.SwanGlasses then
        game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
    end
end)

local theme = venyx:addPage("Settinngs", 5012544693)
local colors = theme:addSection("Colors")
    
for theme, color in pairs(themes) do -- all in one theme changer, i know, im cool
	colors:addColorPicker(theme, color, function(color3)
	venyx:setTheme(theme, color3)
end)
end

local colors = theme:addSection("UI")

colors:addKeybind("Open / Close", Enum.KeyCode.RightControl, function()s
    venyx:toggle()
end)

colors:addButton("คนตึง",function()
    game.CoreGui:FindFirstChild("venyx"):Destroy()
end)

MaxHub:SelectPage(KEEMOHUBFRAM.pages[1], true)
