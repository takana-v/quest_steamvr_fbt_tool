# Quest SteamVR FBT Tool

SteamVRに認識されているトラッカーをOSC経由でVRChatで使えるようにするソフトです。  
Questと名がついていますが別にPCでも使えます。（Oculus PC版VRChatなど）  
VIVE Trackerで動作を確認していますが、他のトラッカーでも動くかもしれません。  

## 事前準備

### 1.QuestとPCの接続

PCとQuestを同じネットワークに接続します。  
Questが繋がっているルーターにPCも繋がっていればOKです。

### 2.SteamVRの設定

HMD無しでSteamVRを使えるようにする設定が必要です。  
設定ファイルを編集します。（デフォルトでは`C:\Program Files (x86)\Steam\config\steamvr.vrsettings`）  
`activateMultipleDrivers`をtrueに設定し、`driver_null`を追加します。  

```json
{
   ...（略）
   "steamvr" : {
      "activateMultipleDrivers" : true,
      ...(略)
   },
   "driver_null" : {
      "enable" : true
   },
   ...（略）
}
```

### 3.qsft_config.iniの編集

[releasesのページ](https://github.com/takana-v/quest_steamvr_fbt_tool/releases)から、最新バージョンのzipファイルをダウンロードして解凍します。  
その中に入っているqsft_config.iniを編集する必要があります。  
説明を入れているので、それに従って編集してください。  

## 使い方

### 1.SteamVRの起動

SteamVRを起動し、トラッカーを認識させておいてください。  

### 2.このソフトの起動

`quest_steamvr_fbt_tool.exe`を実行してください。

### 3.VRChatの起動

VRChatを起動し、OSC機能を有効にしてください。

タスクバーのアイコンを右クリック→Exitから終了できます。  
また、SteamVRを終了すると、このソフトも終了します。  

## その他

### デバイス名の確認

ログファイル内でデバイス名を確認することができます。(内容がDevices:から始まる行)

## ライセンス

MITライセンスです。  
詳しくはLICENSEファイルをご確認ください。  
