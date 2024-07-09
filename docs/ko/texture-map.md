---
id: ko-texture-map
title: 글리프 이미지 추가 및 변경
previous_page: ko-getting-started
next_page: ko-custom-device
---

글리프 이미지는 `InputGlyphTextureMap` 자산에 등록되어 있으며, 대부분의 경우 수정 없이 사용할 수 있습니다. 기본 설정에 없는 버튼 이미지를 추가하거나 기존 이미지를 변경하고자 할 때의 작업 절차를 이 페이지에서 안내합니다.

# 글리프 이미지의 구성
먼저, Input Glyphs 패키지에서 글리프 이미지가 어떻게 등록되어 있는지 설명합니다.

버튼과 글리프 이미지는 `InputGlyphs/Data/`에 있는 `xxxGlyphTextureMap` 자산으로 연결되어 있습니다. `InputLayoutLocalPath`에는 Input System이 정의하는 Control 이름을, `GlyphTexture`에는 실제 이미지의 참조를 입력합니다. Control 이름은 Input Debugger 창의 Name 열에서 확인할 수 있습니다.

각 장치와 `xxxGlyphTextureMap` 자산은 `InputGlyphsSetup` 프리팹에서 연결되어 있습니다. `KeyboardGlyphInitializer` 컴포넌트 등에 앞서 언급한 `xxxGlyphTextureMap` 자산을 할당하여, Input Glyphs는 장치와 버튼 정보를 바탕으로 글리프 이미지를 검색할 수 있습니다.

# 글리프 이미지의 임포트 설정
글리프 이미지의 임포트 설정에서 Read/Write는 반드시 활성화해야 합니다.

# 글리프 이미지 추가하기
예를 들어, 키보드 글리프를 추가하는 절차를 안내합니다.
- Unity 상단 메뉴에서 `Assets > Create > InputGlyphs > InputGlyphTextureMap`을 선택하여 자산을 생성합니다.
- 생성한 자산 목록의 `+` 버튼을 누릅니다.
- `InputLayoutLocalPath`에 추가할 버튼의 Control 이름, `GlyphTexture`에 추가할 이미지를 입력합니다.
- 씬에 배치한 `InputGlyphsSetup` 프리팹의 `KeyboardGlyphInitializer` 컴포넌트 목록의 `+` 버튼을 누릅니다.
- 목록의 마지막 항목을 생성한 자산으로 교체합니다.

# 글리프 이미지 변경하기
예를 들어, 키보드 글리프를 변경하는 절차를 안내합니다.
- `InputGlyphs/Data/KeyboardAlphabetGlyphTextureMap`을 자신의 프로젝트에 복제합니다.(Ctrl+드래그 등)
- 복제한 자산의 `GlyphTexture`를 변경할 이미지로 교체합니다.
- 씬에 배치한 `InputGlyphsSetup` 프리팹의 `KeyboardGlyphInitializer` 컴포넌트 목록의 element 0을 복제한 자산으로 교체합니다.
