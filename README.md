-- GUI to Lua
-----
-- Version: 2.0.
-- Made by chrisopdemobiel.

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local BuyItem = Instance.new("TextButton")
local ItemName = Instance.new("TextBox")
local DupeItems = Instance.new("TextButton")
local DupeMoney = Instance.new("TextButton")
local X = Instance.new("TextButton")

--Properties:

ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(66, 66, 66)
Frame.Position = UDim2.new(0.391850233, 0, 0.281355917, 0)
Frame.Size = UDim2.new(0, 391, 0, 223)
Frame.Active = true
Frame.Draggable = true

BuyItem.Name = "Buy  Item"
BuyItem.Parent = Frame
BuyItem.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
BuyItem.Position = UDim2.new(0.258312017, 0, 0.355140209, 0)
BuyItem.Size = UDim2.new(0, 175, 0, 50)
BuyItem.Font = Enum.Font.SourceSans
BuyItem.Text = "Buy Item"
BuyItem.TextColor3 = Color3.fromRGB(0, 0, 0)
BuyItem.TextScaled = true
BuyItem.TextSize = 14.000
BuyItem.TextWrapped = true

ItemName.Name = "Item Name"
ItemName.Parent = Frame
ItemName.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
ItemName.Position = UDim2.new(0.143222511, 0, 0.0373090059, 0)
ItemName.Size = UDim2.new(0, 266, 0, 50)
ItemName.Font = Enum.Font.SourceSans
ItemName.Text = "Item Name"
ItemName.TextColor3 = Color3.fromRGB(0, 0, 0)
ItemName.TextScaled = true
ItemName.TextSize = 14.000
ItemName.TextWrapped = true

DupeItems.Name = "Dupe Items"
DupeItems.Parent = Frame
DupeItems.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
DupeItems.Position = UDim2.new(0.0306905378, 0, 0.691588759, 0)
DupeItems.Size = UDim2.new(0, 157, 0, 50)
DupeItems.Font = Enum.Font.SourceSans
DupeItems.Text = "Dupe Items"
DupeItems.TextColor3 = Color3.fromRGB(0, 0, 0)
DupeItems.TextScaled = true
DupeItems.TextSize = 14.000
DupeItems.TextWrapped = true
DupeItems.MouseButton1Down:connect(function()

 if state then
_G.on = true

while _G.on == true do
    wait()

wait(0.2)
local args = {
        [1] = "The banana"
    }
    game:GetService("ReplicatedStorage").RemoteEvents.Sell:FireServer(unpack(args))
        local args = {
        [1] = "The banana"
    }
    game:GetService("ReplicatedStorage").RemoteEvents.BuyItemCash:FireServer(unpack(args))

wait(0.2)

    end
    else
_G.on = false
        
    end
end)

DupeMoney.Name = "Dupe Money"
DupeMoney.Parent = Frame
DupeMoney.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
DupeMoney.Position = UDim2.new(0.529411733, 0, 0.691588759, 0)
DupeMoney.Size = UDim2.new(0, 154, 0, 50)
DupeMoney.Font = Enum.Font.SourceSans
DupeMoney.Text = "Dupe Money"
DupeMoney.TextColor3 = Color3.fromRGB(0, 0, 0)
DupeMoney.TextScaled = true
DupeMoney.TextSize = 14.000
DupeMoney.TextWrapped = true

X.Name = "X"
X.Parent = Frame
X.BackgroundColor3 = Color3.fromRGB(170, 0, 0)
X.Position = UDim2.new(0.923273683, 0, -0.0921052694, 0)
X.Size = UDim2.new(0, 52, 0, 50)
X.Font = Enum.Font.SourceSans
X.Text = "X"
X.TextColor3 = Color3.fromRGB(0, 0, 0)
X.TextScaled = true
X.TextSize = 14.000
X.TextWrapped = true
