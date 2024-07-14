---
id: ko-steamworks
title: Steamworks의 글리프 이미지
previous_page: ko-custom-device
next_page: ko-questions
---

Steamworks API는 [컨트롤러의 글리프 이미지를 제공합니다](https://partner.steamgames.com/doc/api/isteaminput#GetGlyphForActionOrigin). 이 페이지에서는 Steam이 제공하는 글리프 이미지를 표시하는 절차를 안내합니다.

> 주의해주세요:
>
> Steamworks에는 [Steam Input API](https://partner.steamgames.com/doc/api/isteaminput)라는 Input System과 유사한 메커니즘이 존재하지만, Input Glyphs는 Input System을 위한 패키지이며 Steam Input API를 지원하지 않습니다.
> 현재 Steam Input API는 Unity의 Event System(UI 조작)에 대응하지 않기 때문에, 우리는 Steam Input API의 사용을 권장하지 않습니다.
>
> 이 페이지의 절차에 따라 설정하면 Input System을 사용하면서도 Steam이 제공하는 글리프를 표시할 수 있습니다.

# 초기화용 오브젝트 배치
`InputGlyphs/Prefabs/InputGlyphsSetup_Steamworks` 프리팹을 첫 번째 씬에 배치하세요.
이미 `InputGlyphsSetup` 프리팹을 배치한 경우 삭제하세요.

# 추가 패키지 설치
`SteamGamepadGlyphInitializer` 컴포넌트에 설치가 필요한 패키지가 표시됩니다. (Not installed)로 표시된 패키지의 Import 버튼을 누르세요.

![Required packages]({{site.baseurl}}/assets/steamworks_required_packages.png)

# Steamworks 설정
이 기능은 [Steamworks.NET](https://steamworks.github.io/)을 이용합니다. [Getting Started](https://steamworks.github.io/gettingstarted) 등의 페이지를 참조하여 Steamworks를 설정하십시오. 적어도 게임 시작 시 `SteamAPI.Init()` 및 `SteamInput.Init(false)`가 실행되면 이 기능이 작동합니다.

# 게임 재생하기
Steam.exe 클라이언트를 실행한 상태에서 게임을 재생합니다. Steamworks 초기화에 성공하면 컨트롤러를 조작하면 Steam이 제공하는 글리프 이미지가 표시됩니다.
