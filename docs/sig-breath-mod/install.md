---
sidebar_position: 0
---

# 導入方法
---

## 導入に必要なもの {#requirements}
---

- Unity 2022.3.22f1
- VRChat Avatar SDK3: 最新バージョン
- [Modular Avatar](https://modular-avatar.nadena.dev/ja): 最新バージョン  
- [VRC Heart Rate](/vrc-heart-rate/install/): 最新バージョン  

## 導入手順
---

1. Boothよりzipファイルを開き、展開します。
1. [導入に必要なもの](#requirements) を全てインポートします。
1. `Sig_BreathMod_v3.x.x.unitypackage` をインポートします。  
**v2.x.xからアップデートする方は、一度プロジェクトの *BekoShop/Sig_Breath_Mod* を削除してからインポートしてください。**
1. プロジェクト上で *BekoShop/Sig_BreathMod/* フォルダを選択し、`Sig_BreathMod_...` プレハブをアバター内にD&Dします。  
OSC心拍計を使う場合は `_OSC` を、そうでない場合は `_Manual` を使用してください。
1. D&Dした同階層に `VRCHeartRate_Core` プレハブが自動で追加されます。（既にアバター内にある場合は追加されません）  
このプレハブはギミックの動作に必須なので削除しないで下さい。アバター内であればどこに動かしても問題ありません。

## OSCについて  {#osc}
:::caution
2.x.xからアップデートする方へ  
**OSC送信アプリが変更されました！** 3.0.0からはPulsoidとBLEの両方で共通のアプリを使用します。古いアプリは使用できませんのでご注意ください。  
古いアバターでも使用する方法を [**こちら**](/heart-beat/osc/#old-avatar) で案内しています。
:::

## [OSCの設定方法はこちら](/vrc-heart-rate/vrcosc)