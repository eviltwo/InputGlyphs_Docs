---
id: zh-CN-custom-device
title: 独自设备的图形图像
previous_page: zh-CN-texture-map
next_page: zh-CN-steamworks
---

Input System有一个机制可以注册独自的设备。详情请参阅[官方文档](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/HowDoI.html#create-my-own-custom-devices)。

在使用上述方法注册设备后，可以通过扩展Input Glyphs来显示该设备的图形图像。扩展需要使用C# Script。

# 概要
- 创建一个实现`IInputGlyphLoader`的类。该类接收设备类型和按钮信息，并返回图形图像的`Texture2D`。
  - 例：`GamepadGlyphLoader.cs`
- 在`Awake()`时将上述Loader实例注册到`InputGlyphManager`。
  - 例：`GamepadGlyphInitializer.cs`

# 简单方法
简单的方法是继承`DeviceGlyphLoaderInitializer<T>`。Loader的处理、TextureMap的传递、Manager的注册等都已实现。`KeyboardGlyphInitializer.cs`和`MouseGlyphInitializer.cs`就是用这种方法实现的。


```
using InputGlyphs.Loaders.Utils;

public class MyDeviceGlyphInitializer : DeviceGlyphLoaderInitializer<MyDevice>
{
}
```

将此组件附加到第一个场景中的任意对象，并设置`InputGlyphTextureMap`资产。关于创建`InputGlyphTextureMap`资产，请参阅[添加或更改图形图像](texture-map)。
