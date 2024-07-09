---
id: zh-CN-overview
title: Input Glyphs
next_page: zh-CN-getting-started
---

![Title]({{site.baseurl}}/assets/Card.png)

InputGlyphs是一个用于显示Unity的InputSystem检测到的输入设备按钮的字形图像（图标）的包。它易于安装，并且设计为可以扩展设备和字形图像。

游戏中的字形图像会根据输入设备自动切换。

包中包含了适用于键盘和鼠标、各种控制器的预设字形图像，但也可以添加或更改自定义字形图像，或使用Steamworks提供的字形图像。

# 特点
## 显示按钮字形图像
根据您的项目的InputActions或PlayerInput显示字形图像。字形图像可以通过Sprite Renderer、UI Image、Text Mesh Pro来显示。

![Duo player glyphs]({{site.baseurl}}/assets/duo_glyphs.png)

游戏过程中，字形图像会根据输入(PlayerInput)的变化自动切换。例如，当切换输入设备，创建第二个本地玩家，或更改按钮分配时。

## 支持各种输入设备
默认支持以下设备的字形图像，并且可以扩展以支持其他设备。
- 键盘和鼠标
- Xbox 控制器
- Playstation 控制器
- Switch Pro 控制器

默认字形图像使用的是[Xelu's FREE Controller Prompts](https://thoseawesomeguys.com/prompts) (Creative Commons 0)。如果您正在为Steam开发游戏，还可以加载Steamworks提供的大量游戏手柄字形图像。

## 支持多按钮分配
例如，“移动:WASD”等，为一个动作分配多个按钮时，会生成连接的字形图像。

![Multiple Glyph]({{site.baseurl}}/assets/multi_glyph.png)

# 示例
- SoloPlayerSample : 针对单人游戏的示例。会切换到检测到输入设备的字形图像。
- DuoPlayerSample : 针对双人游戏的示例。第一和第二玩家会显示不同的字形图像。
- InputCheckSample : 按下设备按钮时会显示该按钮的字形图像。
- SteamworksSample : 显示Steam提供的字形图像。需要Steamworks设置。
