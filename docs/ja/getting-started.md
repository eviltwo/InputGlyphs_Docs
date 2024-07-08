---
id: ja-overview
title: 基本設定
previous_page: overview
next_page: ja-texture-map
---

Input Glyphsを使うための準備と、実際にグリフ画像が表示されるまでの手順です。

# Input Systemの設定
- [Unityの公式ドキュメント](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/Installation.html)に従ってInput Systemをインポート・有効化をしてください。
- ゲーム中のキャラクターの動きは[Player Input](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.4/manual/Components.html)のイベントを使用してください。

# Input Glyphsのインストール
- Unity Package Managerから最新のInput Glyphsをインポートしてください。

# 初期化用のオブジェクトを配置
- `InputGlyphs/Prefabs/InputGlyphsSetup`プレハブを最初のシーンに配置してください。

> [!NOTE]  
> `InputGlyphsSetup`プレハブには、`Keyboard Glyph Initializer`コンポーネントなどのデバイスごとの初期化処理が含まれています。

# グリフ画像を描画
プロジェクトに合う描画方法を選んでください。
## Sprite Renderer
- 任意のオブジェクトに`Sprite Renderer`コンポーネントをアタッチしてください。
- 同じオブジェクトに`Input Glyph Sprite`コンポーネントをアタッチしてください。
  - `Player Input`フィールドに表示したいプレイヤーをアサインしてください。
  - `Input ACtion Reference`フィールドに表示したいアクションをアサインしてください。

![Sprite Renderer settings]({{site.baseurl}}/assets/input_glyph_sprite.png)

## UI Image
- Canvas内の任意のオブジェクトに`UI Image`コンポーネントをアタッチしてください。
- 同じオブジェクトに`Input Glyph Image`コンポーネントをアタッチしてください。
  - `Player Input`フィールドに表示したいプレイヤーをアサインしてください。
  - `Input ACtion Reference`フィールドに表示したいアクションをアサインしてください。
 
![UI Image settings]({{site.baseurl}}/assets/input_glyph_image.png)

## Text Mesh Pro
- Canvas内の任意のオブジェクトに`Text Mesh Pro - UI`コンポーネントをアタッチしてください。
- 同じオブジェクトに`Input Glyph Text`コンポーネントをアタッチしてください。
  - `Player Input`フィールドに表示したいプレイヤーをアサインしてください。
  - `Input ACtion References`フィールドに表示したいアクションをアサインしてください。
- `Text Mesh Pro`コンポーネントに`<sprite name=ActionName>`のようなタグを記述してください。タグがGlyph画像に置換されます。

![TMPro text settings]({{site.baseurl}}/assets/input_glyph_text_1.png)
![TMPro glyph settings]({{site.baseurl}}/assets/input_glyph_text_2.png)
