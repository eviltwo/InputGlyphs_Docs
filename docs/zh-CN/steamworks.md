---
id: zh-CN-steamworks
title: Steamworks的图形图标
previous_page: zh-CN-custom-device
next_page: zh-CN-questions
---

Steamworks API 提供了[控制器的图标图片](https://partner.steamgames.com/doc/api/isteaminput#GetGlyphForActionOrigin)。
本页面将指导您如何显示 Steam 提供的图标图片。

> 请注意：
>
> Steamworks 具有类似于 Input System 的[Steam Input API](https://partner.steamgames.com/doc/api/isteaminput)，但 Input Glyphs 是为 Input System 准备的包，不支持 Steam Input API。
> 目前，Steam Input API 不支持 Unity 的 Event System（UI 操作），因此我们不推荐使用 Steam Input API。
>
> 按照本页面的设置，可以在使用 Input System 的同时显示 Steam 提供的图标。

# 放置初始化对象
请在第一个场景中放置`InputGlyphs/Prefabs/InputGlyphsSetup_Steamworks`预制件。如果已经放置了`InputGlyphsSetup`预制件，请将其删除。

# 安装附加包
`SteamGamepadGlyphInitializer`组件会显示需要安装的包。请点击显示(Not installed)的包的Import按钮。

![Required packages]({{site.baseurl}}/assets/steamworks_required_packages.png)

# 设置Steamworks
此功能使用[Steamworks.NET](https://steamworks.github.io/)。请参阅[Getting Started](https://steamworks.github.io/gettingstarted)等页面来设置Steamworks。至少在游戏开始时执行`SteamAPI.Init()`，此功能才能工作。

# 运行游戏
在启动Steam.exe客户端的状态下运行游戏。如果Steamworks初始化成功，操作控制器时会显示Steam提供的图形图标。
