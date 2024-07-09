---
id: ko-steamworks
title: Steamworks의 글리프 이미지
previous_page: ko-custom-device
next_page: false
---

Steamworks API는 [컨트롤러의 글리프 이미지를 제공합니다](https://partner.steamgames.com/doc/api/isteaminput#GetGlyphForActionOrigin). Input Glyphs에는 Steam 게임 개발자가 이 글리프 이미지를 표시할 수 있는 메커니즘이 있습니다.

> 우리가 이 메커니즘을 만든 이유:
> 
> Input System과 거의 동일한 기능이 Steamworks에도 존재하며, 그것이 Steam Input API입니다.
> 그러나 우리는 Unity를 사용하는 게임 개발자에게 Steam Input API의 구현을 권장하지 않습니다. 왜냐하면 Steam Input API를 활성화하면 게임 패드의 입력이 완전히 비활성화되고, Unity의 Event System이 작동하지 않아 사용자가 UI를 조작할 수 없기 때문입니다.
> 
> 그렇지만 Steam Input API에서 제공되는 글리프 이미지는 품질이 높고 지속적으로 업데이트된다는 신뢰성이 있습니다. 그래서 우리는 Steam Input API의 일부를 사용하여 Input System의 디바이스 정보에서 Steam의 글리프 이미지를 가져오는 메커니즘을 만들었습니다.

# 초기화용 오브젝트 배치
`InputGlyphs/Prefabs/InputGlyphsSetup_Steamworks` 프리팹을 첫 번째 씬에 배치하세요.
이미 `InputGlyphsSetup` 프리팹을 배치한 경우 삭제하세요.

# 추가 패키지 설치
`SteamGamepadGlyphInitializer` 컴포넌트에 설치가 필요한 패키지가 표시됩니다. (Not installed)로 표시된 패키지의 Import 버튼을 누르세요.

![Required packages]({{site.baseurl}}/assets/steamworks_required_packages.png)

# Steamworks 설정
이 기능은 [Steamworks.NET](https://steamworks.github.io/)을 사용합니다. [Getting Started](https://steamworks.github.io/gettingstarted) 등의 페이지를 읽으며 Steamworks를 설정하세요. 적어도 게임 시작 시 `SteamAPI.Init()`가 실행되고 있다면 이 기능이 작동합니다.

# 게임 재생하기
Steam.exe 클라이언트를 실행한 상태에서 게임을 재생합니다. Steamworks 초기화에 성공하면 컨트롤러를 조작하면 Steam이 제공하는 글리프 이미지가 표시됩니다.
