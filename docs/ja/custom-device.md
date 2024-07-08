---
id: ja-custom-device
title: 独自デバイスのグリフ画像
previous_page: ja-texture-map
next_page: ja-steamworks
---

Input Systemは、独自のデバイスを登録できる仕組みがあります。詳しくは[公式ドキュメント](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/HowDoI.html#create-my-own-custom-devices)をご確認ください。

上記の方法でデバイスを登録した後、Input Glyphsを拡張することでそのデバイスのグリフ画像を表示できます。拡張にはC# Scriptを扱う必要があります。

# 概要
- `IInputGlyphLoader`を実装するクラスを作成します。これはデバイスの種類とボタンの情報を受け取り、グリフ画像の`Texture2D`を返すクラスです。
  - 例：`GamepadGlyphLoader.cs`
- `Awake()`のタイミングで上記のLoaderインスタンスを`InputGlyphManager`に登録します。
  - 例：`GamepadGlyphInitializer.cs`

# 簡単な方法
簡単な方法は、`DeviceGlyphLoaderInitializer<T>`を継承することです。Loaderの処理、TextureMapの受け渡し、Managerへの登録などが全て実装されています。`KeyboardGlyphInitializer.cs`や`MouseGlyphInitializer.cs`はこの方法で実装されています。

```
using InputGlyphs.Loaders.Utils;

public class MyDeviceGlyphInitializer : DeviceGlyphLoaderInitializer<MyDevice>
{
}
```

このコンポーネントを最初のシーンの任意のオブジェクトにアタッチし、`InputGlyphTextureMap`アセットを設定します。`InputGlyphTextureMap`アセットの作成ついては[グリフ画像の追加や変更](texture-map)をご確認ください。

