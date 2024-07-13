---
id: zh-CN-questions
title: Q&A
previous_page: zh-CN-steamworks
next_page: false
---

# 将来可以显示游戏手柄的图像吗？
是的，可以。如果InputSystem中添加了该游戏手柄的InputDevice类，我们也会更新此软件包。如果InputSystem或此软件包没有更新，可以[自行添加。](custom-device)

如果显示Steamworks提供的图像，一旦Steamworks添加图像，我们也会更新[Steam Input Adapter软件包](https://github.com/eviltwo/UnitySteamInputAdapter)。

如果上述情况未能解决，将显示XBox控制器的图像。

# 连接多个游戏手柄玩Steam游戏时，图像有时会变得不正常。
用户启用[Steam Input](https://partner.steamgames.com/doc/features/steam_controller/getting_started_for_players)，连接多个游戏手柄玩游戏时，游戏手柄的图像可能会互换。例如，XBox控制器上显示DualSense控制器的图像，DualSense控制器上显示XBox控制器的图像。此问题可以通过禁用SteamInput来解决，或者重新启动游戏，或在玩游戏时拔出所有控制器然后重新连接也能解决。

启用Steam Input会导致Steam劫持游戏手柄。对此问题，我们或Unity无法解决，只能等待Steam修复。
