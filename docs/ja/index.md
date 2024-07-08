---
id: ja-overview
title: Input Glyphs
next_page: ja-getting-started
---

InputGlyphsは、UnityのInputSystemが検知した入力デバイスのボタンのグリフ画像(アイコン)を表示するためのパッケージです。導入が簡単で、デバイスやグリフ画像の拡張もできるように設計されています。

ゲーム中のグリフ画像はInputSystem.PlayerInputの変化を検知して自動で切り替わります。例えば、入力デバイスを切り替えたときや、２人目のローカルプレイヤーが作成されたとき、ボタンの割り当てを変更したときなどです。

パッケージにはキーボード＆マウス・各種コントローラに対応したセットアップ済みのグリフ画像を同梱しています。Steam向けにゲームを開発している場合は、Steamworksが提供している豊富なゲームパッド用のグリフ画像を読み込むこともできます。

# 特徴
## グリフ画像の表示
あなたのプロジェクトのInputActionsやPlayerInputに合わせてグリフ画像が表示されます。グリフ画像はSprite Renderer、UI Image、Text Mesh Proで表示できます。

![Duo player glyphs]({{site.baseurl}}/assets/duo_glyphs.png)

## 様々な入力デバイスに対応
デフォルトでは以下のデバイスのグリフを表示できます。その他のデバイスのために拡張することもできます。
- キーボード & マウス
- Xbox コントローラ
- Playstation コントローラ
- Switch Pro コントローラ

デフォルトのグリフ画像は[Xelu's FREE Controller Prompts](https://thoseawesomeguys.com/prompts) (CC0)を使用しています。

## 複数のボタン割り当てに対応
「移動:WASD」など、１アクションに複数のボタンが割り当てられている場合、連結されたグリフ画像を生成します。

![image](https://github.com/eviltwo/InputGlyphs_Docs/assets/7721151/1a352351-6d75-4133-a23d-a6d2198d8785)


# 事前準備

## Input System
1. 最新のInputSystem packageをUnityPackageManagerからインポートしてください。
TODO: overview of inputsystem, InputActionMap and PlayerInput

## Place initializer
Place InputGlyphSetup.prefab in the first scene.

TODO: xxxInitializer tutorial and SteamGlyph tutorial

## Create Texture Map
If you are using a prefab, you do not need to do anything.

TODO: InputGlyphTextureMap custom tutorial. Texture Read/Write must be enabled.

# Display glyphs
TODO: overview of display components

TODO: detail of glyph layout (Single, Horizontal)

## Sprite Renderer

## UI Image

## Text Mesh Pro

# Samples
TODO: Sample scene list and description
