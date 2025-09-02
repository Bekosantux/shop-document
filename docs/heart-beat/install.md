---
sidebar_position: 1
---

# 導入方法
---

## 導入に必要なもの {#requirements}
- Unity 2022.3.22f1
- VRChat Avatar SDK3: 最新バージョン
- [Modular Avatar](https://modular-avatar.nadena.dev/ja): 最新バージョン  
- [VRC Heart Rate](/vrc-heart-rate/install/): 最新バージョン 

## 手順
1. Boothからダウンロードしたzipファイルを開き、展開します。
1. [導入に必要なもの](#requirements) を全てインポートします。
1. `なめらか心音ギミック_v3.x.x.unitypackage` をインポートします。  
**v2.x.xからアップデートする方は、プロジェクトの *BekoShop/HeatBeat_Gimmick* を削除してからインポートしてください。**
1. *BekoShop/HeartBeatGimmick/Prefabs/* フォルダを選択し、`HeatBeat_...` プレハブをアバター内にD&Dします。  
OSC機能を利用する場合は `_OSC`、そうでなければ `_Manual` プレハブを選択してください。  
1. D&Dした同階層に `VRCHeartRate_Core` プレハブが自動で追加されます。（既にアバター内にある場合は追加されません）  
このプレハブはギミックの動作に必須なので削除しないで下さい。アバター内であればどこに動かしても問題ありません。

1. プレハブ内の **`AudioSources`(プレハブ本体ではない)** をアバターの胸の少し下あたりに配置します。  
とりあえず配置しておき、後でVRChat内での範囲調整をすることをおすすめします。  
![音源の配置](contents\HBSetting_d.png)
:::caution
アニメーションによって上書きされてしまうため、Unity上での範囲調整はできません。VRChat内で聞こえ方を確認しながら、パイメニューから操作してください。
:::

1. **`HR_Counter`** をほっぺたや頭上など心拍数を表示したい場所に配置します。デフォルトではHeadボーンに追従する設定になっています。  
デフォルトでは表示されたままですが、心拍数が0の場合は自動で非表示になります。  
ステンシルを設定すると、顔や髪に埋まって隠れるのを防ぐことが可能です。[参考](https://lilxyzw.github.io/lilToon/ja_JP/advanced/stencil.html)
![心拍計の配置](contents\HBSetting_b.png)

:::caution
心拍数カウンターのTransform(特にスケール)を変更する場合、HeartRateCounterの子であるHR_Counterの方を変更してください。  
どちらかのXYZスケールが揃っていないと、大きく歪んでしまう場合があります。
:::


**導入完了！**

<details>
    <summary>心拍数カウンターを別の場所にも置きたい場合は？</summary>

    プレハブ一覧から `HeartRateCounter` をアバターにD&Dし、 `HR_Counter` を任意の位置に配置してください。  
    動かしたあとは、 `MA Bone Proxy` コンポーネントでボーン追従先を変更してください。
</details>

<details>
<summary>同期パラメーターを削減する</summary>

:::tip
この項では、ギミックの一部機能を削減して同期パラメーターの使用量を減らす方法を説明します。  
よくわからない場合は読み飛ばしてください。
:::

- 音源の範囲設定を削減する  
    Optionフォルダ内にある _NS プレハブを使用します。VRChat内での音源の範囲設定を廃したバージョンです。  
    代わりにUnity上で設定が必要です。あらかじめVRChatで良い感じの範囲を見つけておいてください。  
    `Audio Source` コンポーネントの最長距離(Max Distance)を設定し、その **2倍** の数値を `HBG/SoundRadius_Float` の初期値として設定してください。
    ![音源の設定](contents\HBSetting_e.png)

- 心拍数の手動調整機能を廃止する（OSCプレハブのみ）  
    心拍数は心拍計から取得して自動でしか使わないという方は、手動調整機能を削減することが出来ます。  
    自動配置される `VRCHeartRate_Core` プレハブを選択し、`心拍数手動制御機能を削除` にチェックを入れてください。  
    また、それに伴い不要になる VRC Heart Rate のメニューも削除されます。


それぞれのパラメータ使用量は以下の通りです。
- 心音ギミック(OSC、マニュアル共通)
  - デフォルト: 11bit
  - 音源範囲削減版: 3bit
- VRC Heart Rate
  - デフォルト(OSC): 17bit
  - デフォルト(マニュアル): 8bit
  - 手動調整機能削減版(OSC): 8bit

</details>

### 心音の変え方
![心音の変え方](contents\HBSetting_c.png)  
*Assets/BekoShop/HeartBeat_Gimmick/Resources/Sounds* にA,B,C,Dの4種類の心音が2つに分割されて入っています。プレハブ内のAudio Sourceに0と1に対応するものを適用してください。0→1の順番で繰り返し再生されるように設計していますが、お好みで違う種類・順番の心音を適用しても大丈夫です。  
聞こえ方については動画を御覧ください。  

<iframe src="https://www.youtube.com/embed/C5gtQQ9TYmc" title="心音サンプル" allow="accelerometer; clipboard-write; encrypted-media; gyroscope;web-share" referrerpolicy="strict-origin-when-cross-origin"></iframe>

### 心拍数カウンターの見た目の変え方
BekoShop/HeartBeat_Gimmick/RED_SIM_mod/Materials にあるマテリアルと入れ替えることで見た目を変えることができます。