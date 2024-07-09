---
id: overview
title: Input Glyphs
next_page: getting-started
---

![Title]({{site.baseurl}}/assets/Card.png)

InputGlyphs is a package designed to display button glyph images (icons) of input devices detected by Unity's InputSystem. It is easy to install and designed to allow for the extension of devices and glyph images.

The glyph images in the game will automatically switch according to the device in use.

The package includes pre-configured glyph images for keyboard & mouse and gamepads, but you can add or change your own glyph images or use the glyphs provided by Steamworks.

# Features
## Display Button Glyph Images
Glyph images will be displayed according to your project's InputActions and PlayerInput. Glyph images can be displayed using Sprite Renderer, UI Image, or Text Mesh Pro.

![Duo player glyphs]({{site.baseurl}}/assets/duo_glyphs.png)

During gameplay, glyph images will automatically switch by detecting changes in input (PlayerInput). For example, when switching input devices, creating a second local player, or changing button assignments.

## Support for Various Input Devices
By default, glyph images for the following devices are supported. It can also be extended for other devices.
- Keyboard & Mouse
- Xbox Controller
- Playstation Controller
- Switch Pro Controller

Default glyph images use [Xelu's FREE Controller Prompts](https://thoseawesomeguys.com/prompts) (Creative Commons 0). If you are developing a game for Steam, you can also load the abundant gamepad glyph images provided by Steamworks.

## Support for Multiple Button Assignments
When multiple buttons are assigned to one action, such as "Move: WASD", concatenated glyph images are generated.

![Multiple Glyph]({{site.baseurl}}/assets/multi_glyph.png)

# Samples
- SoloPlayerSample: A sample assuming single-player. The glyph image switches to the device that received input.
- DuoPlayerSample: A sample assuming two players. Different glyph images are displayed for the first and second players.
- InputCheckSample: When you press a device button, the glyph image of that button is displayed.
- SteamworksSample: Displays the glyph images provided by Steam. Steamworks setup is required.
