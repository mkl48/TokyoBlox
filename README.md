# TokyoBlox
A Roblox Script Editor Theme.

# Install
Run
```lua
local json = [[{
  "Background Color":[26,27,38],
  "Text Color":[192,202,245],
  "Selection Color":[192,202,245],
  "Selection Background Color":[40,52,87],
  "Find Selection Background Color":[61,89,161],
  "Matching Word Background Color":[40,52,87],
  "Current Line Highlight Color":[31,35,53],
  "Whitespace Color":[59,66,97],
  "Ruler Color":[59,66,97],
  "Error Color":[247,118,142],
  "Warning Color":[224,175,104],
  "Bracket Color":[137,221,255],
  "Operator Color":[137,221,255],
  "Number Color":[255,158,100],
  "String Color":[158,206,106],
  "Comment Color":[86,95,137],
  "Bool Color":[255,158,100],
  "\"nil\" Color":[255,158,100],
  "Function Name Color":[122,162,247],
  "\"function\" Color":[187,154,247],
  "\"local\" Color":[187,154,247],
  "\"self\" Color":[247,118,142],
  "Luau Keyword Color":[187,154,247],
  "Keyword Color":[187,154,247],
  "Built-in Function Color":[42,195,222],
  "Method Color":[122,162,247],
  "Property Color":[115,218,202],
  "\"TODO\" Color":[224,175,104]
}]]

local theme = game:GetService("HttpService"):JSONDecode(json)
local studio = settings().Studio

for name, color in pairs(theme) do
      color = Color3.fromRGB(color[1], color[2], color[3])
      local success = pcall(function()
              studio[name] = color
      end)
      if not success then
              warn(("%s is not a valid theme color"):format(name))
      end
end

print("Successfully applied the TokyoNight (Night) Script Editor theme!")

```

In the Roblox Studio command line.
