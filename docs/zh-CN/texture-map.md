---
id: zh-CN-texture-map
title: 添加或更改图标图片
previous_page: zh-CN-getting-started
next_page: zh-CN-custom-device
---

图标图片已注册到`InputGlyphTextureMap`资产中，在大多数情况下，您无需进行修改即可使用。如果需要添加默认情况下没有的按钮图标，或者更改现有的图标图片，请按照本页面的步骤进行操作。

# 图标图片的构成
首先，解释在Input Glyphs包中图标图片是如何注册的。

按钮和图标图片在`InputGlyphs/Data/`中的`xxxGlyphTextureMap`资产中绑定。在`InputLayoutLocalPath`中输入Input System定义的Control名称，在`GlyphTexture`中输入实际图片的引用。Control名称可以在Input Debugger窗口的Name列中确认。

各设备和`xxxGlyphTextureMap`资产在`InputGlyphsSetup`预制件中绑定。通过将前述的`xxxGlyphTextureMap`资产分配给例如`KeyboardGlyphInitializer`组件，Input Glyphs可以从设备和按钮的信息中搜索图标图片。

# 图标图片的导入设置
请务必启用图标图片导入设置的Read/Write。

# 添加图标图片
以下步骤示例介绍如何添加键盘图标。
- 从Unity的顶部菜单中选择`Assets > Create > InputGlyphs > InputGlyphTextureMap`，创建资产。
- 按下创建的资产列表的`+`按钮。
- 在`InputLayoutLocalPath`中输入要添加的按钮的Control名称，在`GlyphTexture`中输入要添加的图片。
- 按下配置在场景中的`InputGlyphsSetup`预制件的`KeyboardGlyphInitializer`组件列表中的`+`按钮。
- 将列表的最后一项替换为创建的资产。

# 更改图标图片
以下步骤示例介绍如何更改键盘图标。
- 将`InputGlyphs/Data/KeyboardAlphabetGlyphTextureMap`复制到您的项目中。（例如使用Ctrl+拖拽）
- 将复制的资产中的`GlyphTexture`替换为要更改的图片。
- 将配置在场景中的`InputGlyphsSetup`预制件的`KeyboardGlyphInitializer`组件列表中的element 0替换为复制的资产。
