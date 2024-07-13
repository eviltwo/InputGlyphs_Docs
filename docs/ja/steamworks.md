---
id: ja-steamworks
title: Steamworksのグリフ画像
previous_page: ja-custom-device
next_page: ja-questions
---

Steamworks APIは[コントローラのグリフ画像を提供しています](https://partner.steamgames.com/doc/api/isteaminput#GetGlyphForActionOrigin)。
このページでは、Steamが提供するグリフ画像を表示する手順をご案内します。

> ご注意ください：
>
> Steamworksには[Steam Input API](https://partner.steamgames.com/doc/api/isteaminput)というInput Systemと似た仕組みが存在しますが、Input GlyphsはInput Systemのためのパッケージであり、Steam Input APIをサポートしていません。
> 現在、Steam Input APIはUnityのEvent System(UIの操作)に対応していないため、私たちはSteam Input APIの使用を推奨しません。
>
> このページの通りにセットアップすれば、Input Systemを使いながらもSteamが提供するグリフを表示できます。

# 初期化用のオブジェクトを配置
`InputGlyphs/Prefabs/InputGlyphsSetup_Steamworks`プレハブを最初のシーンに配置してください。
すでに`InputGlyphsSetup`プレハブを配置している場合は削除してください。

# 追加パッケージをインストール
`SteamGamepadGlyphInitializer`コンポーネントにインストールが必要なパッケージが表示されます。(Not installed)と表示されているパッケージのImportボタンを押してください。

![Required packages]({{site.baseurl}}/assets/steamworks_required_packages.png)

# Steamworksのセットアップ
この機能は[Steamworks.NET](https://steamworks.github.io/)を利用しています。[Getting Started](https://steamworks.github.io/gettingstarted)などのページなどを読みながらSteamworksをセットアップしてください。少なくともゲーム開始時に`SteamAPI.Init()`と`SteamInput.Init(false)`が実行されていればこの機能は動作します。

# ゲームを再生する
Steam.exeクライアントを起動した状態でゲームを再生します。Steamworksの初期化に成功していれば、コントローラを操作するとSteamが提供するグリフ画像が表示されます。
