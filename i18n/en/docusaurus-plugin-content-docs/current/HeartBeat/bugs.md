---
sidebar_position: 5
---

# Known Issues
<hr/>
### Avatars with Known Issues

[Yoru the Dragon](https://skd-noratama.booth.pm/items/3923094)
Conflicts with the blinking layer. This is caused by incorrect animation settings on the avatar side.
<details>
<summary>Solution</summary>

1. Open the animator specified in the avatar's FX layer, and open the Blink layer.
1. Right-click in the project → Create → Animation to create a new animation with any name and location.
1. Select the "idol 0" state in the Blink layer, and in the field labeled "None (Motion)", specify the animation you just created.

![](contents\Bugfix_a.png)
</details>

### Assets with Known Issues
[IntParameterCompressor](https://booth.pm/ja/items/5575099)
The heartbeat will not be audible to other players.
You need to remove the Compressor (currently they cannot coexist).

### Other Issues
#### The heartbeat sound is irregularly interrupted
- This may occur if other avatar audio is being played.
This is unavoidable because VRChat limits the number of simultaneously playing sounds within an avatar. Please remove other sound sources or avoid playing them constantly.

- This may occur when using HRToVRChat.
The OSC signal may be interrupted due to unknown causes. It may resolve itself over time.

#### OSC is being received, but the heart rate counter does not appear / the heartbeat sound does not play
- This may occur when using OSC sending apps not mentioned in this manual. The cause is the difference in OSC addresses. Please use the ones mentioned in the manual as much as possible.

- The conditions for this to occur are unknown. It did not work even with an unmodified avatar, but it was resolved by recreating the project.
