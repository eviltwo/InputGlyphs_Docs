---
id: ja-overview
title: Input Glyphs
next_page: ja-getting-started
---

![Title]({{site.baseurl}}/assets/SocialMedia.png)

InputGlyphsは、UnityのInputSystemが検知した入力デバイスのボタンのグリフ画像(アイコン)を表示するためのパッケージです。導入が簡単で、デバイスやグリフ画像の拡張もできるように設計されています。

ゲーム中のグリフ画像は入力中のデバイスに合わせて自動で切り替わります。

パッケージにはキーボード＆マウス、各種コントローラに対応したセットアップ済みのグリフ画像を同梱していますが、独自のグリフ画像を追加や変更したり、Steamworksが提供するグリフを使用することもできます。

# 特徴
## ボタンのグリフ画像を表示
あなたのプロジェクトのInputActionsやPlayerInputに合わせてグリフ画像が表示されます。グリフ画像はSprite Renderer、UI Image、Text Mesh Proで表示できます。

![Duo player glyphs]({{site.baseurl}}/assets/duo_glyphs.png)

ゲームのプレイ中は入力(PlayerInput)の変化を検知してグリフ画像が自動で切り替わります。例えば、入力デバイスを切り替えたときや、２人目のローカルプレイヤーが作成されたとき、ボタンの割り当てを変更したときなどです。

## 様々な入力デバイスに対応
デフォルトでは以下のデバイスのグリフ画像に対応しています。その他のデバイスのために拡張することもできます。
- キーボード & マウス
- Xbox コントローラ
- Playstation コントローラ
- Switch Pro コントローラ

デフォルトのグリフ画像は[Xelu's FREE Controller Prompts](https://thoseawesomeguys.com/prompts) (Creative Commons 0)を使用しています。Steam向けにゲームを開発している場合は、Steamworksが提供している豊富なゲームパッド用のグリフ画像を読み込むこともできます。

## 複数のボタン割り当てに対応
「移動:WASD」など、１つのアクションに複数のボタンが割り当てられている場合、連結されたグリフ画像を生成します。

![Multiple Glyph]({{site.baseurl}}/assets/multi_glyph.png)

# サンプル
- SoloPlayerSample : １人プレイを想定したサンプルです。入力があったデバイスのグリフ画像に切り替わります。
- DuoPlayerSample : ２人プレイを想定したサンプルです。１人目と２人目で異なるグリフ画像が表示されます。
- InputCheckSample : デバイスのボタンを押すとそのボタンのグリフ画像が表示されます。
- SteamworksSample : Steamが提供するグリフ画像を表示します。Steamworksの設定が必要です。