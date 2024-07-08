---
id: ja-steamworks
title: Steamworksのグリフ画像
previous_page: ja-custom-device
next_page: false
---

Steamworks APIは[コントローラのグリフ画像を提供しています](https://partner.steamgames.com/doc/api/isteaminput#GetGlyphForActionOrigin)。Input GlyphsにはSteamゲーム開発者がこのグリフ画像を表示するための仕組みがあります。

> [!NOTE]  
> 私たちがこの仕組みを作った経緯：
> 
> Input Systemとほぼ同じ機能がSteamworksにも存在し、それがSteam Input APIです。
> しかし、私たちはUnity開発者にSteam Input APIの実装をお勧めしません。
> なぜなら、Steam Input APIを有効にするとゲームパッドの入力が完全に無効化され、UnityのEvent Systemが機能しなくなり、ユーザはUIの操作ができなくなるためです。
> 
> とはいえ、Steam Input APIで提供されるグリフ画像はクオリティが高く、継続して更新されるという信頼性があります。そこで私たちは、Steam Input APIの一部を利用して、Input Systemのデバイス情報からSteamのグリフ画像を取得する仕組みを作りました。

# 初期化用のオブジェクトを配置
`InputGlyphs/Prefabs/InputGlyphsSetup_Steamworks`プレハブを最初のシーンに配置してください。
すでに`InputGlyphsSetup`プレハブを配置している場合は削除してください。

# 追加パッケージをインストール
`SteamGamepadGlyphInitializer`コンポーネントにインストールが必要なパッケージが表示されます。(Not installed)と表示されているパッケージのImportボタンを押してください。

![Required packages]({{site.baseurl}}/assets/steamworks_required_packages.png)

# Steamworksのセットアップ
この機能は[Steamworks.NET](https://steamworks.github.io/)を利用しています。[Getting Started](https://steamworks.github.io/gettingstarted)などのページなどを読みながらSteamworksをセットアップしてください。少なくともゲーム開始時に`SteamAPI.Init()`が実行されていればこの機能は動作します。

# ゲームを再生する
Steam.exeクライアントを起動した状態でゲームを再生します。Steamworksの初期化に成功していれば、コントローラを操作するとSteamが提供するグリフ画像が表示されます。
