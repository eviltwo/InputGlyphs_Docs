---
id: ja-texture-map
title: グリフ画像の追加や変更
previous_page: ja-getting-started
next_page: ja-custom-device
---

グリフ画像は`InputGlyphTextureMap`アセットに登録されており、ほとんどの場合は手を加えずにお使いいただけます。デフォルトにないボタンの画像を追加したい場合や既存の画像を変更したい場合の作業手順をこのページでご案内します。

# グリフ画像の構成
まず、Input Glyphsパッケージでグリフ画像がどのように登録されているかをご説明します。

ボタンとグリフ画像は`InputGlyphs/Data/`の中にある`xxxGlyphTextureMap`アセットで紐づけています。`InputLayoutLocalPath`にはInput Systemが定義するControl名を、`GlyphTexture`には実際の画像の参照を入力しています。Control名はInput DebuggerウィンドウのName列で確認することができます。

各デバイスと`xxxGlyphTextureMap`アセットは`InputGlyphsSetup`プレハブで紐づけています。`KeyboardGlyphInitializer`コンポーネントなどに先ほどの`xxxGlyphTextureMap`アセットをアサインすることで、Input Glyphsはデバイスとボタンの情報からグリフ画像を検索することができます。

# グリフ画像のインポート設定
追加や変更をする画像は、必ずRead/Writeを有効にしてください。

# グリフ画像を追加する
例として、キーボードのグリフを追加する手順をご案内します。
- Unityの上部メニューから`Assets > Create > InputGlyphs > InputGlyphTextureMap`を選択し、アセットを作成します。
- 作成したアセットのリストの`+`ボタンを押します。
- `InputLayoutLocalPath`に追加したいボタンのControl名、`GlyphTexture`に追加したい画像を入力します。
- シーンに配置した`InputGlyphsSetup`プレハブの`KeyboardGlyphInitializer`コンポーネントのリストの`+`ボタンを押します。
- リストの最後を作成したアセットに置き換えます。

# グリフ画像を変更する
例として、キーボードのグリフを変更する手順をご案内します。
- `InputGlyphs/Data/KeyboardAlphabetGlyphTextureMap`をご自身のプロジェクトに複製します。(Ctrl+ドラッグなど)
- 複製したアセットの`GlyphTexture`を変更したい画像に置き換えます。
- シーンに配置した`InputGlyphsSetup`プレハブの`KeyboardGlyphInitializer`コンポーネントのリストのうちelement 0を複製したアセットに置き換えます。
