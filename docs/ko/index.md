---
id: ko-overview
title: Input Glyphs
next_page: ko-getting-started
---

![Title]({{site.baseurl}}/assets/Card.png)

InputGlyphs는 Unity의 InputSystem이 감지한 입력 장치의 버튼 글리프 이미지(아이콘)를 표시하기 위한 [오픈 소스](https://github.com/eviltwo/InputGlyphs) 패키지입니다. 통합이 간편하며, 장치 및 글리프 이미지의 확장도 가능하도록 설계되었습니다.

게임 중의 글리프 이미지는 입력 중인 장치에 맞춰 자동으로 전환됩니다.

패키지에는 키보드 & 마우스, 다양한 컨트롤러에 대응한 설정 완료된 글리프 이미지가 포함되어 있지만, 독자의 글리프 이미지를 추가하거나 변경하거나 Steamworks가 제공하는 글리프를 사용할 수도 있습니다.

# 특징
## 버튼 글리프 이미지를 표시
당신의 프로젝트의 InputActions나 PlayerInput에 맞춰 글리프 이미지가 표시됩니다. 글리프 이미지는 Sprite Renderer, UI Image, Text Mesh Pro로 표시할 수 있습니다.

![Duo player glyphs]({{site.baseurl}}/assets/duo_glyphs.png)

게임 플레이 중에는 입력(PlayerInput)의 변화를 감지하여 글리프 이미지가 자동으로 전환됩니다. 예를 들어, 입력 장치를 전환했을 때나, 두 번째 로컬 플레이어가 생성되었을 때, 버튼 할당을 변경했을 때 등입니다.

## 다양한 입력 장치에 대응
기본적으로는 다음 장치의 글리프 이미지에 대응합니다. 다른 장치를 위해 확장할 수도 있습니다.
- 키보드 & 마우스
- Xbox 컨트롤러
- Playstation 컨트롤러
- Switch Pro 컨트롤러

기본 글리프 이미지는 [Xelu's FREE Controller Prompts](https://thoseawesomeguys.com/prompts) (Creative Commons 0)을 사용하고 있습니다. Steam용으로 게임을 개발하고 있는 경우, Steamworks가 제공하는 풍부한 게임패드용 글리프 이미지를 로드할 수도 있습니다.

## 여러 버튼 할당에 대응
「이동:WASD」 등, 하나의 액션에 여러 버튼이 할당된 경우, 연결된 글리프 이미지를 생성합니다.

![Multiple Glyph]({{site.baseurl}}/assets/multi_glyph.png)

# 샘플
- SoloPlayerSample : 1인 플레이를 상정한 샘플입니다. 입력이 있었던 장치의 글리프 이미지로 전환됩니다.
- DuoPlayerSample : 2인 플레이를 상정한 샘플입니다. 1인과 2인에서 다른 글리프 이미지가 표시됩니다.
- InputCheckSample : 장치의 버튼을 누르면 그 버튼의 글리프 이미지가 표시됩니다.
- SteamworksSample : Steam이 제공하는 글리프 이미지를 표시합니다. Steamworks 설정이 필요합니다.
