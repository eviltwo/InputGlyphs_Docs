---
id: steamworks
title: Steamworks
previous_page: custom-device
next_page: questions
---

The Steamworks API provides [controller glyph images](https://partner.steamgames.com/doc/api/isteaminput#GetGlyphForActionOrigin).
This page will guide you through the steps to display glyph images provided by Steam.

> Note:
>
> Steamworks has a similar mechanism called [Steam Input API](https://partner.steamgames.com/doc/api/isteaminput), but Input Glyphs is a package for the Input System and does not support the Steam Input API.
> Currently, the Steam Input API does not support Unity's Event System (UI operation), so we do not recommend using the Steam Input API.
>
> By setting up as described on this page, you can display the glyphs provided by Steam while using the Input System.

# Place the initialization object
Place the `InputGlyphs/Prefabs/InputGlyphsSetup_Steamworks` prefab in the first scene.
If you have already placed the `InputGlyphsSetup` prefab, please remove it.

# Install additional packages
The `SteamGamepadGlyphInitializer` component will display the packages that need to be installed. Click the Import button for packages marked as (Not installed).

![Required packages]({{site.baseurl}}/assets/steamworks_required_packages.png)

# Set up Steamworks
This function utilizes [Steamworks.NET](https://steamworks.github.io/). Please follow the setup instructions on pages such as [Getting Started](https://steamworks.github.io/gettingstarted). At the very least, ensure that `SteamAPI.Init()` and `SteamInput.Init(false)` are executed at the start of the game for this function to work.

# Play the game
Play the game with the Steam.exe client running. If Steamworks is initialized successfully, the glyph images provided by Steam will be displayed when you operate the gamepad.
