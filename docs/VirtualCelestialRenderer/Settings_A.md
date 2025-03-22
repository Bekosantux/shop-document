---
sidebar_position: 1
---

# 設定（Aセット）
<hr/>

## 導入手順
_BekoShop/VirtualCelestialRenderer/Main/Materials_ にある VCR_StarOnly マテリアルをスカイボックスに適用します。任意のメッシュに適用したい場合は、　_Mesh が付いている方を使用してください。

---
## マテリアル設定
### SkyColor
- Sky Brightness  
空の明るさを指定します。0で真っ暗、1で指定した空色が反映されます。
- Use Solid Color  
スカイボックス全体で均一な色にするか、グラデーションを用いるかを選択します。
- Color top/middle/bottom  
グラデーションを用いる場合の空色を指定します。
- Middle / Top offset  
空色の境目の高さを指定します。
### Celestial Sphere
- Base Rotation  
天球の方角を指定します。デフォルトでは+Z軸方向が北です。
- Latitude  
緯度を指定します。東京は35.689°です。
- Longitude  
経度を指定しますが、後述の回転によって変動するためあまり意味はありません。
- Rotation Speed  
天球の自然回転速度を指定します。Bセット以上の時刻同期とは違い、現在時刻は考慮されません。
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
### Moon
- Draw the moon  
月を描画するか否かを設定します。
- Moon Color  
月の色をHDRカラーで指定します。強さを上げるとより強く発光します。
- Moon Size  
月の大きさを指定します。
- Phase of the moon  
月相を指定します。
- Moon Longitude / Latitude  
月の天球上での経度と緯度を指定します。
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