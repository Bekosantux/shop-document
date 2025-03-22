---
sidebar_position: 2
---

# 設定（B、Cセット）
<hr/>

## 導入手順
_BekoShop/VirtualCelestialRenderer/Main/Materials_ にある BかCの対応するマテリアルをスカイボックスに適用します。任意のメッシュに適用したい場合は、 _Mesh が付いている方を使用してください。  
次に、Main/Prefabs 内にある対応するプレハブをヒエラルキーの任意の場所に配置します。  
最後に、Cセットの場合はタブレットとポインターをワールド内の配置したい場所に移動してください。

### 太陽を同期させる  
太陽として動かしたいリアルタイムのディレクショナルライトを、  
Bプレハブは _VCR_B_Limited/Scripts/SkyController_  
Cプレハブは _VCR_C_Full/VCR_ControlTablet/Controller/SkyController_  
のオブジェクトに付いているスクリプトの Sun にアタッチしてください。
指定されたライトは回転、色、明るさが自動制御されます。
![Sun](contents/SetTheSun.png)

---
## マテリアル設定
一部設定はAセットと共通ですが、現在時刻の同期機能によりスクリプトによっていくつかの項目が上書きされます。

### 上書きされる設定
- Sky Color セクションの色に関する設定  
プレハブ内の Sky Controller によって上書きされます。スクリプト設定から時間経過によるそれぞれの色を変更可能です。
- Celestial Sphere セクションの Obliquity, Precession, GMST  
それぞれ黄道傾斜角、歳差運動、グリニッジ平均恒星時です。スクリプトによって自動制御されるため、特に設定は必要ありません。
- Sun および Moon セクション  
太陽と月はスクリプトによって位置、明るさ等が自動制御されます。
なお、太陽と月の大きさは自由に設定可能です。
- Planet 及び Laser Pointer (Cのみ) セクション  
スクリプトによって自動制御されます。


### SkyColor
- Sky Brightness  
空の明るさを指定します。0で真っ暗、1で指定した空色が反映されます。
### Celestial Sphere
- Base Rotation  
天球の方角を指定します。デフォルトでは+Z軸方向が北です。
### Stars
- Star Size  
星の大きさを指定します。値が大きいほど星が小さくなります。
- Star Brightness  
星の明るさを指定します。1以上では(有効な場合は)Bloomがかかります。
- Medium / Dim Star Brightness  
普通な星と暗い星の明るさをそれぞれ指定します。暗い星はギリギリ見えるくらいがおすすめです。
- Color Boost  
星の色を増幅します。0だと全ての星が白色になります。
- Twinkle Speed / Intensity  
星のきらめきの速さと強さを指定します。
### Sun
- Sun Size  
太陽の大きさを指定します。
### Moon
- Draw the moon  
月を描画するか否かを設定します。
- Moon Color  
月の色をHDRカラーで指定します。強さを上げるとより強く発光します。
- Moon Size  
月の大きさを指定します。
### Milky Way
- Milky Way Brightness / Color / Color Factor  
天の川の明るさ、色、色の濃さを指定します。
- Milky Way Noise Scale  
天の川を描画するためのノイズのスケールを設定します。
### Constellation Lines
- Line Color / Blur  
星座線の色と柔らかさを指定します。星座線の透明度はアルファチャンネルで指定します。
### Constellation Arts
- Constellation Arts ドロップダウン  
表示する星座アートを選択します。表示しない、黄道12星座、トレミーの48星座、現代の88星座から選択できます。
- Constellation Art Color  
星座アートの色と透明度を指定します。

---
## スクリプト設定
スクリプトはAセットには付属しません。  
Bセットの場合は _VRC_B_Limited/Scripts_  
Cセットの場合は _VCR_C_Full/VCR_ControlTablet/Controller_  
に格納されています。  

設定が可能なスクリプトは以下の２つです。
### Time Controller  
- Use Custom Time  
チェックボックスをマークすると、下にある入力欄に設定した日時から時刻がスタートします。チェックしなければ自動で現在時刻に同期されます。未来や過去の星空を再現する際に有用です。

### Sky Controller  
- Sun  
同期させるディレクショナルライトを指定します。  
- Day Night Cycle  
チェックを外すと太陽位置に関わらず常に夜空になります。  
- グラデーションエディタ  
太陽高度によって変わる空色を自由に設定できます。  
**左が太陽が頂点の時、右が最も低い時の色** になっています。太陽がちょうど水平線にあるときにグラデーションの真ん中になります。  
その下の太陽とライトの色についても同様に設定できます。  
![SkyController](contents/SkyController.png)

---
## 天体名・方角表示をオフにする  
以下のように、NameLabelの子にある対応するオブジェクトを再生前にオフにすることで可能です。  
![NameLabel](contents/LabelToggle.png)