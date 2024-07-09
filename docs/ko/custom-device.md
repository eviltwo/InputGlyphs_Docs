---
id: ko-custom-device
title: 독자 디바이스의 글리프 이미지
previous_page: ko-texture-map
next_page: ko-steamworks
---

Input System은 독자적인 디바이스를 등록할 수 있는 메커니즘이 있습니다. 자세한 내용은 [공식 문서](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/HowDoI.html#create-my-own-custom-devices)를 참조하십시오.

위의 방법으로 디바이스를 등록한 후, Input Glyphs를 확장하여 해당 디바이스의 글리프 이미지를 표시할 수 있습니다. 확장에는 C# 스크립트를 다루어야 합니다.

# 개요
- `IInputGlyphLoader`를 구현하는 클래스를 작성합니다. 이는 디바이스의 종류와 버튼 정보를 받아 글리프 이미지의 `Texture2D`를 반환하는 클래스입니다.
  - 예: `GamepadGlyphLoader.cs`
- `Awake()` 시점에서 위의 로더 인스턴스를 `InputGlyphManager`에 등록합니다.
  - 예: `GamepadGlyphInitializer.cs`

# 간단한 방법
간단한 방법은 `DeviceGlyphLoaderInitializer<T>`를 상속하는 것입니다. 로더의 처리, TextureMap의 전달, Manager에의 등록 등이 모두 구현되어 있습니다. `KeyboardGlyphInitializer.cs`나 `MouseGlyphInitializer.cs`는 이 방법으로 구현되었습니다.

```
using InputGlyphs.Loaders.Utils;

public class MyDeviceGlyphInitializer : DeviceGlyphLoaderInitializer<MyDevice>
{
}
```

이 컴포넌트를 첫 번째 씬의 임의의 오브젝트에 첨부하고, `InputGlyphTextureMap` 애셋을 설정합니다. `InputGlyphTextureMap` 애셋의 생성에 대해서는 [글리프 이미지 추가 및 변경](texture-map)을 참조하십시오.
