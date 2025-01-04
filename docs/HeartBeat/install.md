---
sidebar_position: 1
---

# 導入方法
<hr/>
## 導入に必要なもの
- Unity 2022.3.22f1
- VRCSDK 最新バージョン
- Modular Avatar 最新バージョン

## 手順
1. *BekoShop/HeartBeat_Gimmick/Prefabs* の中にあるプレハブをアバター直下に配置します。OSC機能を利用する場合はHeartBeat_OSC、そうでなければHeartBeat_Manualプレハブを選択してください。

1. プレハブ内の **AudioSources(プレハブ本体ではない)** をアバターの胸あたりに配置します。  
とりあえず配置しておき、後でVRChat内での範囲調整をおすすめします。
![音源の配置](contents\HBSetting_d.png)
:::caution
アニメーションによって上書きされてしまうため、Unity上での範囲調整はできません。VRChat内でパイメニューから操作してください。
:::

1. HRCounter をほっぺたや頭上など心拍数を表示したい場所に配置します。デフォルトではHeadボーンに追従する設定になっています。  
![心拍計の配置](contents\HBSetting_b.png)

**導入完了！**

<details>
<summary>オプションプレハブについて</summary>

:::tip
オプションプレハブは、一部機能を削除してパラメータ使用量を削減しています。  
よくわからない場合は通常プレハブを使用してください。
:::
- _NS (No Scaling)
    VRChat内での音源の範囲設定を廃したバージョンです。代わりにUnity上で設定が必要です。  
    `Audio Source` コンポーネントの最長距離(Max Distance)を設定し、その **2倍** の数値を `HBG/SoundRadius_Float` の初期値として設定してください。
    ![音源の設定](contents\HBSetting_e.png)

- _NM (No Manual)
    手動調整機能を削除したバージョンです。  
    OSC機能のみを利用し、手動調整機能は一切使用しないという方におすすめです。

- _NS_MS
    上記2つの機能を削減したバージョンです。  
    上級者向けです。


それぞれのパラメータ使用量は以下の通りです。
- Manual_NS: 11bit
- OSC_NM: 19bit
- OSC_NS: 20bit
- OSC_NS_MS: 11bit
</details>

### 心音の変え方
![心音の変え方](contents\HBSetting_c.png)  
*Assets/BekoShop/HeartBeat_Gimmick/Resources/Sounds* にA,B,C,Dの4種類の心音が2つに分割されて入っています。プレハブ内のAudio Sourceに0と1に対応するものを適用してください。0→1の順番で繰り返し再生されるように設計していますが、お好みで違う種類・順番の心音を適用しても大丈夫です。
