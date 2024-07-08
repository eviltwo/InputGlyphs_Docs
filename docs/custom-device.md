---
id: custom-device
title: Custom devices
previous_page: texture-map
next_page: steamworks
---


The Input System provides a mechanism to register custom devices. For more details, please refer to the [official documentation](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/HowDoI.html#create-my-own-custom-devices).

After registering a device using the method above, you can display the glyph images for that device by extending Input Glyphs. Extending requires handling C# scripts.

# Overview
- Create a class that implements `IInputGlyphLoader`. This class takes the device type and button information and returns a `Texture2D` of the glyph image.
  - Example: `GamepadGlyphLoader.cs`
- Register the loader instance to `InputGlyphManager` at the `Awake()` timing.
  - Example: `GamepadGlyphInitializer.cs`

# Simple Method
The simplest method is to inherit from `DeviceGlyphLoaderInitializer<T>`. This covers the loader processing, texture map passing, and manager registration. `KeyboardGlyphInitializer.cs` and `MouseGlyphInitializer.cs` are implemented in this way.

```
using InputGlyphs.Loaders.Utils;

public class MyDeviceGlyphInitializer : DeviceGlyphLoaderInitializer<MyDevice>
{
}
```

Attach this component to any object in the first scene and set the `InputGlyphTextureMap` asset. For details on creating the `InputGlyphTextureMap` asset, please refer to [Glyph textures](texture-map).