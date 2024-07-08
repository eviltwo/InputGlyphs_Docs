---
id: texture-map
title: Glyph textures
previous_page: getting-started
next_page: custom-device
---

Glyph images are registered in the `InputGlyphTextureMap` asset, and in most cases, you can use them without any modifications. This page guides you through the steps to add button images that are not in the default or to change existing images.

# Structure of Glyph Images
First, let's explain how glyph images are registered in the Input Glyphs package.

Buttons and glyph images are linked with the `xxxGlyphTextureMap` asset located in `InputGlyphs/Data/`. Enter the Control name defined by the Input System in `InputLayoutLocalPath` and the actual image reference in `GlyphTexture`. You can check the Control name in the Name column of the Input Debugger window.

Each device and the `xxxGlyphTextureMap` asset are linked in the `InputGlyphsSetup` prefab. By assigning the `xxxGlyphTextureMap` asset to components such as `KeyboardGlyphInitializer`, Input Glyphs can search for glyph images from the device and button information.

# Import Settings for Glyph Images
Make sure to enable Read/Write for the import settings of glyph images.

# Adding Glyph Images
As an example, here are the steps to add keyboard glyphs.
- From Unity's top menu, select `Assets > Create > InputGlyphs > InputGlyphTextureMap` to create an asset.
- Press the `+` button on the list of the created asset.
- Enter the Control name of the button you want to add in `InputLayoutLocalPath` and the image you want to add in `GlyphTexture`.
- Press the `+` button on the list of the `KeyboardGlyphInitializer` component of the `InputGlyphsSetup` prefab placed in the scene.
- Replace the last item in the list with the created asset.

# Changing Glyph Images
As an example, here are the steps to change keyboard glyphs.
- Duplicate `InputGlyphs/Data/KeyboardAlphabetGlyphTextureMap` to your project. (Ctrl+drag, etc.)
- Replace the `GlyphTexture` of the duplicated asset with the image you want to change.
- Replace element 0 of the list of the `KeyboardGlyphInitializer` component of the `InputGlyphsSetup` prefab placed in the scene with the duplicated asset.
