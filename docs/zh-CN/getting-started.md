---
id: zh-CN-getting-started
title: 基本设置
previous_page: zh-CN-overview
next_page: zh-CN-texture-map
---

为了使用Input Glyphs，介绍准备工作以及在游戏中显示Glyph图像的步骤。

# Input System的设置
- 请按照[Unity的官方文档](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/Installation.html)导入和启用Input System。
- 游戏中的角色移动使用[Player Input](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/Components.html)的事件。
  - Player Input的行为需要选择Invoke C Sharp Events或Invoke Unity Events。

# 安装Input Glyphs
- 从Unity Package Manager导入最新的Input Glyphs。

# 配置初始化对象
- 请在第一个场景中放置`InputGlyphs/Prefabs/InputGlyphsSetup`预制件。

> `InputGlyphsSetup`预制件包含了`Keyboard Glyph Initializer`组件等设备的初始化处理。

# 绘制Glyph图像
Glyph图像可以使用Sprite Renderer、UI Image和Text Mesh Pro绘制。
## Sprite Renderer
- 请在任意对象上附加`Sprite Renderer`组件。
- 在同一对象上附加`Input Glyph Sprite`组件。
  - 在`Player Input`字段中分配要显示的玩家。
  - 在`Input ACtion Reference`字段中分配要显示的动作。

![Sprite Renderer settings]({{site.baseurl}}/assets/input_glyph_sprite.png)

## UI Image
- 在Canvas内的任意对象上附加`UI Image`组件。
- 在同一对象上附加`Input Glyph Image`组件。
  - 在`Player Input`字段中分配要显示的玩家。
  - 在`Input ACtion Reference`字段中分配要显示的动作。

![UI Image settings]({{site.baseurl}}/assets/input_glyph_image.png)

## Text Mesh Pro
- 在Canvas内的任意对象上附加`Text Mesh Pro - UI`组件。
- 在同一对象上附加`Input Glyph Text`组件。
  - 在`Player Input`字段中分配要显示的玩家。
  - 在`Input ACtion References`字段中分配要显示的动作。
- 在`Text Mesh Pro`组件中编写`<sprite name=ActionName>`标签。标签会被替换为Glyph图像。

![TMPro text settings]({{site.baseurl}}/assets/input_glyph_text_1.png)

![TMPro glyph settings]({{site.baseurl}}/assets/input_glyph_text_2.png)

# 运行游戏
运行游戏后会显示Glyph图像。如果未显示，请检查错误日志。
