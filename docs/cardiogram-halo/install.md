---
sidebar_position: 1
---

# 導入方法
---
## 導入に必要なもの
- Unity 2022.3.22f1
- VRCSDK 最新バージョン
- Modular Avatar 最新バージョン
- [VRC Heart Rate](/category/vrc-heart-rate/) 最新バージョン

## 手順
---
1. [導入に必要なもの](#requirements) を全てインポートします。[VRC Heart Rate](/vrc-heart-rate/install/)の入れ忘れが多発しております！ご注意下さい。
1. *"BekoShop/CardiogramHalo"* の中にある "CardiogramHalo_..." プレハブをアバター直下に配置します。  
    OSC心拍計を使用する場合は `_OSC`, そうでない場合は `_Manual` プレハブを使用してください。
1. `HeadAnchor` オブジェクトの位置、回転、スケールを調整します。

:::tip
最初から表示されている緑のヘイローは位置・大きさ合わせのためのダミーです。   
アップロード時に自動で削除されますが、手動で削除しても問題ありません。  
:::

## 設定
---
### ヘイローの太さを変える
`CardiogramHalo/HeadAnchor/Base/ParticleRoot/Particle` のスケールを変更します。

### 透過を有効にする
`CardiogramHalo/HeadAnchor/Base/ParticleRoot/Particle` の `Particle System` コンポーネントの `レンダラー` タブで **トレイルマテリアル** をTransparentマテリアルに変更します。  
このマテリアルは透明度が変更可能な他、顔（カメラ）を近づけるとフェードアウトする機能が付いています。

### その他
`MA Parameter` コンポーネントの初期値を変えることでヘイローに関する設定が可能です。
- `ColorMode`
  - 0: 心拍数に応じて色が 青→緑→赤 に変化します。
  - 1: 時間経過でレインボーになります。
  - 2: Unity上で設定したパーティクルの色が一定で表示されます。
- `HideWhenZero`
  - 心拍数が0になったときにヘイローを非表示にします。なお、心拍数が0のときは波形が直線になり文字通りヘイローっぽくなるという小ネタがあります。