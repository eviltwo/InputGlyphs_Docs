---
id: steamworks
title: Steamworks
previous_page: custom-device
next_page: questions
---

The Steamworks API [provides gamepad glyph images](https://partner.steamgames.com/doc/api/isteaminput#GetGlyphForActionOrigin). Input Glyphs has a mechanism for Steam game developers to display these glyph images.

> Background of why we created this mechanism:
> 
> Steamworks has a similar feature to the Input System, which is the Steam Input API.
> However, we do not recommend implementing the Steam Input API for game developers using Unity. This is because enabling the Steam Input API completely disables gamepad input, rendering Unity's Event System non-functional and preventing users from operating the UI.
> 
> That said, the glyph images provided by the Steam Input API are of high quality and are reliably updated continuously. Therefore, we created a mechanism to obtain Steam glyph images from the Input System's device information using part of the Steam Input API.

# Place the initialization object
Place the `InputGlyphs/Prefabs/InputGlyphsSetup_Steamworks` prefab in the first scene.
If you have already placed the `InputGlyphsSetup` prefab, please remove it.

# Install additional packages
The `SteamGamepadGlyphInitializer` component will display the packages that need to be installed. Click the Import button for packages marked as (Not installed).

![Required packages]({{site.baseurl}}/assets/steamworks_required_packages.png)

# Set up Steamworks
This feature uses [Steamworks.NET](https://steamworks.github.io/). Set up Steamworks by following pages like [Getting Started](https://steamworks.github.io/gettingstarted). As long as `SteamAPI.Init()` is executed at the start of the game, this feature will work.

# Play the game
Play the game with the Steam.exe client running. If Steamworks is initialized successfully, the glyph images provided by Steam will be displayed when you operate the gamepad.
