---
sidebar_position: 3
---

# よくある質問
<hr/>

## 全セット共通
### 星だけにしたいです。
[星座線](../settings-a/#constellation-lines)と[星座アート](../settings-a/#constellation-arts)を非表示にします。  
B、Cセットの場合は、追加で[天体名・方角表示](../settings-bc/#turn-off-name-labels)をオフにします。

## B, Cセット共通
### 常に夜にしたいです。
スクリプト設定で、[Day Night Cycle](../settings-bc/#sky-color-settings)トグルをオフにします。

## Cセット固有
### マテリアル設定を変えても、再生すると元に戻ってしまいます。
Persistence機能によって、シーンを起動したことがある場合は前回のものに上書きされてしまいます。

Unity上では、`上部メニュー→VRChat SDK→ClientSim PlayerData→開いたウィンドウ` でゴミ箱マークを押してデータをリセットする、またはPlayerDataの値を直接変更する
ことで変更が可能です。

一度公開したワールドに変更を適応したい場合、そのワールドのUserDataを削除してワールドをアップロードし直すとUnityで設定された座標が反映されます。