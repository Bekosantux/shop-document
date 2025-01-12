---
sidebar_position: 2
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# About OSC Functionality
<hr/>
<Tabs>
    <TabItem value="def" label="Overview" default>
        :::note
        This is not required to use the heartbeat system.
        :::
        By sending your heart rate to VRChat, you can synchronize your heart rate with your avatar in real-time.
        There are two methods: using Pulsoid in combination with HRtoVRChat, or sending it directly without using them (there are other methods, but they are omitted here).
        Please also refer to this if you like:
        [Notes on the environment when sending heart rate to VRChat (Japanese)](https://note.com/bekosan/n/nf6a976867771)
    </TabItem>
    <TabItem value="pulsoid" label="Pulsoid">
        :::caution
        ! Please make sure your device is compatible with Pulsoid !
        https://www.blog.pulsoid.net/monitors
        :::
        <hr />
        1. Pulsoid Setup
            1. Follow the instructions up to 3.2 in this guide (Japanese): https://note.com/kendesu/n/n81275f17986a

            1. Obtaining your Pulsoid Key (access_token)
            Go to [this link](https://pulsoid.net/oauth2/authorize?response_type=token&client_id=8c48435f-a0c6-4512-9bf7-6768678b625c&redirect_uri=&scope=data:heart_rate:read&state=&response_mode=web_page) and log in with the account you just created.
            Click the "Authorize App" button in the bottom right corner. Your token will be displayed in censored form. Click "Copy to clipboard" to copy it.
            **Be careful when handling your token, as others can access your heart rate if it leaks.**
        1. HRToVRChat Setup
            1. Download the latest Windows Launcher from: https://hrtovrchat.fortnite.lol/download#h.ha8hgsfz56g2

            1. Launch the Launcher, open the Config tab, change hrType to "pulsoidsocket", and press the SAVE button.
            ![](contents\HRtoVRChat_a.png)

            1. Select "pulsoidkey", paste the token you copied earlier, and press the SAVE button.

            1. Setup is complete! With Pulsoid running, press the START button from the Program tab to send OSC signals to VRChat.
    </TabItem>
    <TabItem value="ble" label="Bluetooth LE">
        :::note
        Requires a heart rate monitor that supports Bluetooth Low Energy (BLE).
        :::
        Dedicated heart rate monitors are often more accurate and have better battery life than smartwatches.
        Setup and startup are much simpler and easier compared to Pulsoid.
        Here is a [recommended heart rate monitor](https://www.amazon.co.jp/dp/B08882MGXD). You can buy it for under 4000 yen when it's cheap.

        <hr/>
        https://github.com/Bekosantux/Beko.BluetoothHeartRateOSC

        1. Pair your BLE heart rate monitor with Windows.
        :::caution
        In Windows 11, you may need to change the "Bluetooth device discovery" setting to "Advanced" for it to appear in the list.
        :::

        2. Download the zip from the "Release" section on the right side of the screen, extract it, and simply run the exe file. (If you see numbers, it's successful. The program will continue to run in the background even if you close the window.)
    </TabItem>
</Tabs>
