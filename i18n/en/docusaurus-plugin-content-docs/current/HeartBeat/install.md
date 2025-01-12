---
sidebar_position: 1
---

# Installation Guide
<hr/>
## Requirements
- Unity 2022.3.22f1
- VRCSDK Latest version
- Modular Avatar Latest version

<details>
<summary>What is the Modular Avatar?</summary>

Modular Avatar, MA for short, is a system that allows you to easily add and remove assets to your avatar.  
This tool automates the animator's merging process and other tasks.  
Just put it in and you're good to go!  

You can install it in VCC at the following link.  
https://modular-avatar.nadena.dev/  

</details>

## Steps
1. Drag and drop the prefab located in *BekoShop/HeartBeat_Gimmick/Prefabs* directly under your avatar. If you want to use OSC functionality, select the HeartBeat_OSC prefab. Otherwise, choose the HeartBeat_Manual prefab.

1. Place the **AudioSources (not the prefab itself)** within the prefab around the chest area of your avatar. 
It's recommended to place them tentatively and adjust the range within VRChat later. 
![Audio Source Placement](contents\HBSetting_d.png)
:::caution
The range cannot be adjusted on Unity because it will be overwritten by the animation. Please adjust it using the Pie Menu in VRChat.
:::

1. Place the HR_Counter where you want to display the heart rate, such as on the cheek or above the head. By default, it is set to follow the Head bone. 
It will remain visible by default, but will automatically be hidden when the heart rate is 0. 
![Heart Rate Counter Placement](contents\HBSetting_b.png)

**Installation Complete!**
<details>
<summary>What if I want to add more heart rate counters?</summary>

Simply duplicating the HR_Counter object will not work. Please use the CounterOnly prefab instead. 
The CounterOnly prefab does not produce a heartbeat sound and only displays the heart rate.
:::caution
You can place as many CounterOnly prefabs as you like, anywhere you like, but be sure to install it alongside the main prefab. 
It will not work on its own.
:::
</details>

<details>
<summary>About the Optional Prefabs</summary>

:::tip
The optional prefabs have reduced parameter usage by removing some features. 
If you are unsure, please use the regular prefab.
:::
- _NS (No Scaling)
    This version eliminates the in-VRChat sound range setting. Instead, you need to configure it in Unity. 
    Set the Max Distance of the `Audio Source` component, and then set the initial value of `HBG/SoundRadius_Float` to **twice** that number.
    ![Audio Source Setting](contents\HBSetting_e.png)

- _NM (No Manual)
    This version removes the manual adjustment feature. 
    Recommended for those who only use the OSC function and do not use the manual adjustment function at all.

- _NS_MS
    This version has the above two features removed. 
    For advanced users.

The parameter usage for each is as follows:
- Manual_NS: 11bit
- OSC_NM: 19bit
- OSC_NS: 20bit
- OSC_NS_MS: 11bit
</details>

### How to Change the Heartbeat Sound
![How to Change Heartbeat Sound](contents\HBSetting_c.png)  
In *Assets/BekoShop/HeartBeat_Gimmick/Resources/Sounds*, you will find four types of heartbeat sounds (A, B, C, D) split into two parts each. Apply the sounds corresponding to 0 and 1 to the Audio Sources in the prefab. It is designed to play repeatedly in the order of 0 → 1, but you can apply different types or orders of heartbeat sounds as you like. 
Please refer to the video for how they sound. 

<iframe src="https://www.youtube.com/embed/C5gtQQ9TYmc" title="Heartbeat Sound Samples" allow="accelerometer; clipboard-write; encrypted-media; gyroscope;web-share" referrerpolicy="strict-origin-when-cross-origin"></iframe>

### How to Change the Appearance of the Heart Rate Counter
You can change the appearance by replacing the materials in BekoShop/HeartBeat_Gimmick/RED_SIM_modd/Materials.
