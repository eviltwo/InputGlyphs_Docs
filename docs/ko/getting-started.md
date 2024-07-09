---
id: ko-getting-started
title: 기본 설정
previous_page: ko-overview
next_page: ko-texture-map
---

Input Glyphs를 사용하기 위한 준비와 게임에 글리프 이미지를 표시하기까지의 절차를 안내합니다.

# Input System 설정
- [Unity의 공식 문서](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/Installation.html)에 따라 Input System을 가져와서 활성화하세요.
- 게임 내 캐릭터의 움직임은 [Player Input](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/Components.html) 이벤트를 사용하세요.

# Input Glyphs 설치
- Unity Package Manager에서 최신 Input Glyphs를 가져오세요.

# 초기화용 오브젝트 배치
- `InputGlyphs/Prefabs/InputGlyphsSetup` 프리팹을 첫 번째 장면에 배치하세요.

> `InputGlyphsSetup` 프리팹에는 `Keyboard Glyph Initializer` 컴포넌트 등의 디바이스별 초기화 처리가 포함되어 있습니다.

# 글리프 이미지 그리기
글리프 이미지는 Sprite Renderer, UI Image, Text Mesh Pro로 그릴 수 있습니다.
## Sprite Renderer
- 임의의 오브젝트에 `Sprite Renderer` 컴포넌트를 붙이세요.
- 같은 오브젝트에 `Input Glyph Sprite` 컴포넌트를 붙이세요.
  - `Player Input` 필드에 표시할 플레이어를 지정하세요.
  - `Input ACtion Reference` 필드에 표시할 동작을 지정하세요.

![Sprite Renderer settings]({{site.baseurl}}/assets/input_glyph_sprite.png)

## UI Image
- Canvas 내 임의의 오브젝트에 `UI Image` 컴포넌트를 붙이세요.
- 같은 오브젝트에 `Input Glyph Image` 컴포넌트를 붙이세요.
  - `Player Input` 필드에 표시할 플레이어를 지정하세요.
  - `Input ACtion Reference` 필드에 표시할 동작을 지정하세요.
 
![UI Image settings]({{site.baseurl}}/assets/input_glyph_image.png)

## Text Mesh Pro
- Canvas 내 임의의 오브젝트에 `Text Mesh Pro - UI` 컴포넌트를 붙이세요.
- 같은 오브젝트에 `Input Glyph Text` 컴포넌트를 붙이세요.
  - `Player Input` 필드에 표시할 플레이어를 지정하세요.
  - `Input ACtion References` 필드에 표시할 동작을 지정하세요.
- `Text Mesh Pro` 컴포넌트에 `<sprite name=ActionName>` 태그를 작성하세요. 태그가 글리프 이미지로 변환됩니다.

![TMPro text settings]({{site.baseurl}}/assets/input_glyph_text_1.png)

![TMPro glyph settings]({{site.baseurl}}/assets/input_glyph_text_2.png)

# 게임을 실행하세요
게임을 실행하면 글리프 이미지가 표시됩니다. 표시되지 않는 경우 에러 로그를 확인하세요.
