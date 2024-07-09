---
id: getting-started
title: Getting started
previous_page: overview
next_page: texture-map
---

This guide explains how to prepare for using Input Glyphs and the steps to display glyph images in the game.

# Set up the Input System
- Please import and enable the Input System according to [Unity's official documentation](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/Installation.html).
- Use [Player Input](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/Components.html) events for character movement in the game.
  - For the Behavior of Player Input, you need to select either Invoke C Sharp Events or Invoke Unity Events.

# Install Input Glyphs
- Import the latest Input Glyphs from the Unity Package Manager.

# Place the Initialization Object
- Place the `InputGlyphs/Prefabs/InputGlyphsSetup` prefab in the first scene.

> The `InputGlyphsSetup` prefab includes initialization processes for each device, such as the `Keyboard Glyph Initializer` component.

# Draw Glyph Images
Glyph images can be rendered with Sprite Renderer, UI Image, or Text Mesh Pro.
## Sprite Renderer
- Attach the `Sprite Renderer` component to any object.
- Attach the `Input Glyph Sprite` component to the same object.
  - Assign the player you want to display in the `Player Input` field.
  - Assign the action you want to display in the `Input Action Reference` field.

![Sprite Renderer settings]({{site.baseurl}}/assets/input_glyph_sprite.png)

## UI Image
- Attach the `UI Image` component to any object within the Canvas.
- Attach the `Input Glyph Image` component to the same object.
  - Assign the player you want to display in the `Player Input` field.
  - Assign the action you want to display in the `Input Action Reference` field.

![UI Image settings]({{site.baseurl}}/assets/input_glyph_image.png)

## Text Mesh Pro
- Attach the `Text Mesh Pro - UI` component to any object within the Canvas.
- Attach the `Input Glyph Text` component to the same object.
  - Assign the player you want to display in the `Player Input` field.
  - Assign the action you want to display in the `Input Action References` field.
- Write tags like `<sprite name=ActionName>` in the `Text Mesh Pro` component. The tag will be replaced with the Glyph image.

![TMPro text settings]({{site.baseurl}}/assets/input_glyph_text_1.png)

![TMPro glyph settings]({{site.baseurl}}/assets/input_glyph_text_2.png)

# Play the Game
When you play the game, the glyph images will be displayed. If they are not displayed, check the error log.
