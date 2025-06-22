---
sidebar_position: 2
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# OSC機能について
<hr/>
<Tabs>
    <TabItem value="def" label="概要" default>
        :::note
        心音ギミックの使用に必須ではありません。
        :::
        心拍数をVRChatに送信することで、心拍数をリアルタイムでアバターと同期させることができます。  
        PulsoidとHRtoVRChatを組み合わせる方法と、それを介さず直接送信する方法があります。（それ以外にもありますがここでは省略します）  
        よろしければこちらも参考にしてください。  
        [VRChatに心拍数を送る時の環境メモ](https://note.com/bekosan/n/nf6a976867771)

        <hr/>
        お手持ちのスマートウォッチを介したPulsoidを使用する方法と、Bluetooth LE対応の心拍計を使用する方法があります。  
        ||Pulsoid|Bluetooth LE|
        |:---|:---|:---|
        |長所|スマートウォッチをそのまま使用可能|心拍数取得精度が良い<br />電池が長く持つ <br />|
        |短所|スマートウォッチの電池持ちが悪い<br />導入と起動が面倒|導入と起動が簡単|

        MibandやApple Watchなどのスマートウォッチをお持ちの場合は、まずはPulsoidを試してみることをオススメします。  
        機能性ではBLEの方が優れているので、お気に召したらBLE対応の心拍計を購入してみるのも良いでしょう。

    </TabItem>
    <TabItem value="pulsoid" label="Pulsoid">
        :::caution
        ！必ず端末がPulsoidに対応しているか確認してください！  
        https://www.blog.pulsoid.net/monitors
        :::
        <hr />
        1. Pulsoidの設定
            1. https://note.com/kendesu/n/n81275f17986a の 3.2 までを真似する  

            1. PulsoidKey(access_token)の取得  
            [ココ](https://pulsoid.net/oauth2/authorize?response_type=token&client_id=8c48435f-a0c6-4512-9bf7-6768678b625c&redirect_uri=&scope=data:heart_rate:read&state=&response_mode=web_page)に移動して、先程作ったアカウントでログイン。  
            右下の Authorize App を押すとトークンが伏せ字で表示されるので、Copy to clipboard でコピーしておきます。  
            **トークンが漏れると他人から心拍数が取得出来てしまうので取り扱いには注意してください。**  
        1. HRToVRChatの設定
            1. https://hrtovrchat.fortnite.lol/download#h.ha8hgsfz56g2  
            から一番上のWindowsのLauncherをダウンロード

            1. Launcherを起動したらConfigタブを開き、hrTypeを pulsoidsocket に変更して、SAVEボタンを押す。  
            ⚠️**すべて小文字です！前後に空白が入らないように注意してください。**⚠️  
            ![](contents\HRtoVRChat_a.png)

            1. 加えてpulsoidkeyを選び、先ほどコピーしたトークンを貼り付け、SAVEボタンを押す。  
            ⚠️**hrTypeにはトークンは貼り付けません！**⚠️  

            1. 設定が完了しました！Pulsoidを起動した状態でProgramタブからSTARTボタンを押すとOSC信号がVRChatに送信されます。

            :::note
            「HRtoVRChat_OSC is not installed! Please navigate to the Updates tab and install it.」  
            というエラーが出た場合は、Updatesタブから「UPDATE SOFTWARE」ボタンを押してください。
            :::
    </TabItem>
    <TabItem value="ble" label="Bluetooth LE">
        :::note
        Bluetooth Low Energy（BLE）に対応した心拍計が必要です。
        :::
        専用の心拍計であればスマートウォッチよりも精度が高く電池の持ちも良いことが多いです。  
        導入や起動もPulsoidに比べてかなりシンプルで非常に楽です。  
        [オススメの心拍計](https://www.amazon.co.jp/dp/B08882MGXD) です。安いタイミングなら4000円以下で買えます。  
        
        <hr/>
        https://github.com/Bekosantux/Beko.BluetoothHeartRateOSC

        1. WindowsにBLE心拍計をペアリングします。  
        :::caution
        Windows11 22H2, 23H2の場合、「Bluetoothデバイスの検出」設定を「詳細」に変更してください。  
        24H2では、Bluetoothデバイスの検索で、Bluetoothデバイスのリストを下にスクロールして「すべてのデバイスを表示」を選択してください。
        :::

        2. 画面右のReleaseからダウンロードしたzipを展開して、exeファイルを実行するだけで使えます。（数字が出てきたら成功。ウィンドウを閉じても裏で動きます。）
    </TabItem>
</Tabs>