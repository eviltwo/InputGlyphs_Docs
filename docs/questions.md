---
id: questions
title: FAQ
previous_page: steamworks
next_page: false
---

# Can I display glyph images of future gamepads?
Yes, you can. If the InputDevice class of that gamepad is added to the InputSystem, we will also update this package. If there are no updates to the InputSystem or this package, [you can add it yourself.](custom-device)

If you are displaying glyph images provided by Steamworks, we will also update the [Steam Input Adapter package](https://github.com/eviltwo/UnitySteamInputAdapter) when images are added to Steamworks.

If the above is not supported, glyph images for the Xbox controller will be displayed.

# Glyph images sometimes get messed up when connecting multiple gamepads to play Steam games.
When users enable [Steam Input](https://partner.steamgames.com/doc/features/steam_controller/getting_started_for_players) and connect multiple gamepads to play a game, the glyphs of the gamepads may get swapped. For example, the Xbox controller may display DualSense controller glyphs, and the DualSense controller may display Xbox controller glyphs. This issue can be resolved by disabling Steam Input, restarting the game, or unplugging and re-plugging all controllers while playing the game.

This issue occurs because Steam hijacks the gamepads when Steam Input is enabled. There is nothing we or Unity can do to solve the problem, and only Steam can fix it.
