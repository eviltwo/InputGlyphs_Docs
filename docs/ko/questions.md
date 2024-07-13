---
id: ko-questions
title: FAQ
previous_page: ko-steamworks
next_page: false
---

# 장래의 게임패드 글리프 이미지를 표시할 수 있습니까?
네, 가능합니다. InputSystem에 그 게임패드의 InputDevice 클래스가 추가된 경우, 저희도 이 패키지를 업데이트합니다. 만약 InputSystem 또는 이 패키지의 업데이트가 없는 경우는, [스스로 추가할 수 있습니다.](custom-device)

Steamworks가 제공하는 글리프 이미지를 표시하고 있는 경우, Steamworks에 이미지가 추가되면 저희도 [Steam Input Adapter 패키지](https://github.com/eviltwo/UnitySteamInputAdapter)를 업데이트합니다.

위의 것이 대응되지 않는 경우는, XBox 컨트롤러의 글리프 이미지가 표시됩니다.

# 여러 게임패드를 연결하여 Steam의 게임을 플레이하면, 때때로 글리프 이미지가 이상해집니다.
사용자가 [Steam Input](https://partner.steamgames.com/doc/features/steam_controller/getting_started_for_players)을 활성화하고, 여러 게임패드를 연결하여 게임을 플레이하면, 게임패드의 글리프가 바뀌는 경우가 있습니다. 예를 들어, XBox 컨트롤러에 DualSense 컨트롤러의 글리프 이미지가 표시되고, DualSense 컨트롤러에 XBox 컨트롤러의 글리프 이미지가 표시됩니다. 이 문제는 사용자가 SteamInput을 비활성화하면 해결됩니다. 또는, 게임을 재시작하거나, 게임을 플레이 중에 컨트롤러를 모두 빼고 다시 꽂으면 해결되는 경우가 있습니다.

Steam Input을 활성화하면, Steam이 게임패드를 하이잭하는 것이 원인입니다. 문제 해결을 위해 저희나 Unity가 할 수 있는 것은 없으며, Steam이 수정을 해야 합니다.
