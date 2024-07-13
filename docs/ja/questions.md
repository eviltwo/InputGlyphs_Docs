---
id: ja-questions
title: Q&A
previous_page: ja-steamworks
next_page: false
---

# 将来のゲームパッドのグリフ画像を表示できますか？
はい、できます。InputSystemにそのゲームパッドのInputDeviceクラスが追加された場合は、私たちもこのパッケージを更新します。もしInputSystemまたはこのパッケージの更新がない場合は、[ご自身で追加することもできます。](custom-device)

Steamworksが提供するグリフ画像を表示している場合は、Steamworksに画像が追加されると私たちも[Steam Input Adapterパッケージ](https://github.com/eviltwo/UnitySteamInputAdapter)を更新します。

上記が対応されていない場合は、XBoxコントローラのグリフ画像が表示されます。

# 複数のゲームパッドを繋げてSteamのゲームをプレイすると、時々グリフ画像がおかしくなります。
ユーザが[Steam Input](https://partner.steamgames.com/doc/features/steam_controller/getting_started_for_players)を有効にして、複数のゲームパッドを繋げてゲームをプレイすると、ゲームパッドのグリフが入れ替わってしまう場合があります。例えば、XBoxコントローラにDualSenseコントローラのグリフ画像が表示され、DualSenseコントローラにXBoxコントローラのグリフ画像が表示されます。この問題は、ユーザがSteamInputを無効にすると解決します。または、ゲームを再起動するか、ゲームをプレイ中にコントローラを全て抜いて差し直すと解決する場合があります。

Steam Inputを有効にすると、Steamがゲームパッドをハイジャックしてしまうのが原因です。問題解決のために私たちやUnityにできることはなく、Steamが修正をするしかありません。
