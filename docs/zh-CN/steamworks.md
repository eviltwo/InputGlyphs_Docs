---
id: zh-CN-steamworks
title: Steamworks的图形图标
previous_page: zh-CN-custom-device
next_page: false
---

Steamworks API提供了[控制器的图形图标](https://partner.steamgames.com/doc/api/isteaminput#GetGlyphForActionOrigin)。Input Glyphs中有一个机制，允许Steam游戏开发者显示这些图形图标。

> 我们设计这个机制的背景：
> 
> Steamworks中存在与Input System几乎相同的功能，即Steam Input API。
> 然而，我们不推荐使用Unity的游戏开发者实现Steam Input API。因为启用Steam Input API会完全禁用游戏手柄输入，导致Unity的Event System无法工作，用户无法操作UI。
> 
> 尽管如此，Steam Input API提供的图形图标质量高且可靠更新。因此，我们利用Steam Input API的一部分，创建了从Input System的设备信息获取Steam图形图标的机制。

# 放置初始化对象
请在第一个场景中放置`InputGlyphs/Prefabs/InputGlyphsSetup_Steamworks`预制件。如果已经放置了`InputGlyphsSetup`预制件，请将其删除。

# 安装附加包
`SteamGamepadGlyphInitializer`组件会显示需要安装的包。请点击显示(Not installed)的包的Import按钮。

![Required packages]({{site.baseurl}}/assets/steamworks_required_packages.png)

# 设置Steamworks
此功能使用[Steamworks.NET](https://steamworks.github.io/)。请参阅[Getting Started](https://steamworks.github.io/gettingstarted)等页面来设置Steamworks。至少在游戏开始时执行`SteamAPI.Init()`，此功能才能工作。

# 运行游戏
在启动Steam.exe客户端的状态下运行游戏。如果Steamworks初始化成功，操作控制器时会显示Steam提供的图形图标。
