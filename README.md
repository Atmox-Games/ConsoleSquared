# Introduction
This project was made completely out of boredom and wanted to share it as open source with anyone who might be interested. This is not a professional project meant for public distribution to live experiences, as it may contain vulnerabilities, bugs, and glitches.

# The Design
The design of Console² is largely inspired by the iconic developer console from the [Source](https://en.wikipedia.org/wiki/Source_(game_engine)) game engine.

# Setup
1. Get the main model from one of the sources below and insert it to your Roblox project.
2. Ungroup every folder under their respective [Data Models](https://create.roblox.com/docs/projects/data-model) labeled on every folders name.
3. Well it's done.

# Configuration
You can configure the console visually and auditory with the values on the path `StarterGui.ConsoleSquared.Configuration`:

![](https://github.com/Atmox-Games/ConsoleSquared/blob/main/Media/image_2025-09-17_203852683.png)

# Features
## Custom Commands
You can add or remove your own and built-in, client and server-sided commands freely by going to the modules ConsoleSquaredServer(.Commands) in ServerScriptService and ConsoleSquaredClient(.Commands) in ReplicatedStorage. The built-in commands there would give you the rough idea of how you create a command.

## Autocomplete
Every command you create will be autocompleteable and autofillable.

You can press Tab key to fill the selected autocompletion in the TextBox or press enter to directly submit it.

![](https://github.com/Atmox-Games/ConsoleSquared/blob/main/Media/AutocompleteDemo.gif)

## Rich Text
Outputs are compatible with [rich text](https://create.roblox.com/docs/ui/rich-text), which means that you can achieve outputs like this:

![](https://github.com/Atmox-Games/ConsoleSquared/blob/main/Media/image_2025-09-17_204708958.png)

## Accessible Commands
Since the commands are stored in ModuleScripts, you can access and utilize them from any other script in your project, provided the script meets the necessary context level:
```luau
local ServerScriptService = game:GetService("ServerScriptService")
local ConsoleSquaredServer = require(ServerScriptService.ConsoleSquared:WaitForChild("ServerHandler"):WaitForChild("ConsoleSquaredServer"))

ConsoleSquaredServer.Commands.kick.func("Server", "troublemaker5000", "You are making a big mess!")
```

# Testing Place
You can test Console² in this experience with the built-in commands.
**The place is uncopylocked.**
https://www.roblox.com/games/75747502289977/Console-Testing
