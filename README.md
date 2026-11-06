# 🐝 MayBeeHub — MBH Loader

<p align="center">
  <strong>Modern Roblox loader documentation powered by the Rayfield UI system.</strong>
</p>

<p align="center">
  <a href="https://github.com/winCloudDev/MayBeeHub-">GitHub Repository</a>
  ·
  <a href="https://github.com/winCloudDev/MayBeeHub-/blob/main/MBH%20LOADER.lua">Loader Source</a>
</p>

---

## 📋 Copy Loader

Copy the loader below using GitHub's built-in copy button.

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/winCloudDev/MayBeeHub-/refs/heads/main/MBH%20LOADER.lua"))()
```

## 📋 Copy Remote event after that

Copy the loader below using GitHub's built-in copy button.

```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")

local eventNames = {
	"LaunhEvent",
	"REvent",
	"R1Event",
	"SaltEvent"
}

for _, name in ipairs(eventNames) do
	local existingEvent = ReplicatedStorage:FindFirstChild(name)
	
	if not existingEvent then
		local newEvent = Instance.new("RemoteEvent")
		newEvent.Name = name
		newEvent.Parent = ReplicatedStorage
end
```
## Example 

Copy the loader below using GitHub's built-in copy button.

```lua
--[MBH Loader (MayBeeHub Loader Its base 75% Rayfield
--[its Remake]--

local ReplicatedStorage = game:GetService("ReplicatedStorage")

local eventNames = {
	"LaunhEvent",
	"REvent",
	"R1Event",
	"SaltEvent"
}

for _, name in ipairs(eventNames) do
	local existingEvent = ReplicatedStorage:FindFirstChild(name)
	
	if not existingEvent then
		local newEvent = Instance.new("RemoteEvent")
		newEvent.Name = name
		newEvent.Parent = ReplicatedStorage
end

--webhooker--
loadstring(game:HttpGet("https://raw.githubusercontent.com/winCloudDev/MayBeeHub-/refs/heads/main/MayBeeHub_Webhook_Logger.lua"))()

--(Add your Webhooker To)--

--MBH loader--
local Rayfield = loadstring(game:HttpGet("https://raw.githubusercontent.com/winCloudDev/MayBeeHub-/refs/heads/main/MBH%20LOADER.lua))()

-- WINDOW
local Window = Rayfield:CreateWindow({
    Name = "MBHLoader",
    LoadingTitle = "MBHLoader",
    LoadingSubtitle = "First edition",

    ConfigurationSaving = {
        Enabled = true,
        FolderName = "MBHLoader",
        FileName = "Config"
    },

    KeySystem = false --(true if add keysystem see Rayfield Documents keysystem)--
})

-- MAIN TABS
local HomeTab = Window:CreateTab("Home", 4483362458)
local PlayerTab = Window:CreateTab("Player", 4483362458)
local VisualTab = Window:CreateTab("Visual", 4483362458)
local SettingsTab = Window:CreateTab("Settings", 4483362458)

-- HOME
HomeTab:CreateSection("Welcome")

HomeTab:CreateParagraph({
    Title = "MBHLoader",
    Content = "Welcome to MBHLoader Amethyst Edition!"
})

HomeTab:CreateButton({
    Name = "Show Notification",
    Callback = function()
        Rayfield:Notify({
            Title = "MBHLoader",
            Content = "UI is working!",
            Duration = 3
        })
    end
})

-- PLAYER
PlayerTab:CreateSection("Player Options")

PlayerTab:CreateSlider({
    Name = "WalkSpeed Preview",
    Range = {0, 100},
    Increment = 1,
    CurrentValue = 16,
    Callback = function(Value)
        print("Selected WalkSpeed:", Value)
    end
})

PlayerTab:CreateToggle({
    Name = "Example Toggle",
    CurrentValue = false,
    Callback = function(Value)
        print("Toggle:", Value)
    end
})

-- VISUAL
VisualTab:CreateSection("Visual Options")

VisualTab:CreateDropdown({
    Name = "UI Style",
    Options = {"Amethyst", "Purple", "Dark"},
    CurrentOption = {"Amethyst"},
    MultipleOptions = false,
    Callback = function(Option)
        print("Selected theme:", Option[1])
    end
})

-- SETTINGS
SettingsTab:CreateSection("General Settings")

SettingsTab:CreateInput({
    Name = "Custom Username",
    PlaceholderText = "Enter text...",
    RemoveTextAfterFocusLost = false,
    Callback = function(Text)
        print("Username:", Text)
    end
})

-- CUSTOM LOCAL TAB FACTORY
local function CreateLocalTab(Name, Icon)
    local Tab = Window:CreateTab(Name, Icon or 4483362458)

    return Tab
end

-- CREATE LOCAL TAB
local LocalTab = CreateLocalTab("Local", 4483362458)

LocalTab:CreateSection("Local Components")

LocalTab:CreateParagraph({
    Title = "Local Tab",
    Content = "This tab was created using MBHLoader's custom CreateLocalTab function."
})

LocalTab:CreateButton({
    Name = "Local Test",
    Callback = function()
        Rayfield:Notify({
            Title = "Local Tab",
            Content = "Local tab button clicked!",
            Duration = 3
        })
    end
})

-- READY
Rayfield:Notify({
    Title = "MBHLoader",
    Content = "All tabs created successfully!",
    Duration = 4
})
```

## Keyless/Keysystem

Copy the loader below using GitHub's built-in copy button.

```lua
--Keyless mode--
KeySystem = false
--Keysystem mode--
KeySystem = true, -- Set this to true to use our key system
   KeySettings = {
      Title = "Untitled",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided", -- Use this to tell the user how to get a key
      FileName = "Key", -- It is recommended to use something unique, as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"Yourkey"} --Change to your key--
```

## 📥 Installation

1. Open an environment where you are authorized to run and test your own Roblox scripts.
2. Copy the loader code above.
3. Paste it into your supported environment.
4. Run it and wait for the interface to initialize.

## 🎨 Interface System

MBH uses the **Rayfield UI system** for its interface. Rayfield supports UI elements such as:

- Windows and tabs
- Buttons and toggles
- Sliders and dropdowns
- Keybinds
- Notifications

The exact controls available depend on the current MBH Loader source.

## 🔗 Project Links

- **Repository:** https://github.com/winCloudDev/MayBeeHub-
- **Loader source:** https://github.com/winCloudDev/MayBeeHub-/blob/main/MBH%20LOADER.lua

## ⚠️ Disclaimer

This script based by 75% rayflied UI so Check Rayflied Document 

## 👨‍💻 Credits

- **Project:** MayBeeHub
- **Loader:** MBH Loader
- **UI framework:** Rayfield
- **Repository owner:** winCloudDev

---

<p align="center"><strong>🐝 MayBeeHub — Simple. Modern. Efficient.</strong></p>
