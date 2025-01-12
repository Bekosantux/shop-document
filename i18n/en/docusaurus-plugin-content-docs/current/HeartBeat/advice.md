---
sidebar_position: 3
---

# Precautions
<hr/>
- Except for the optional prefabs, do not adjust the sound range settings in Unity. They will be overwritten by the animation. Please operate it from the Pie Menu within VRChat.

- The avatar's ears (Audio Listener) are located at the viewpoint. Since it is located inward by the radius of the head, and considering the possibility of the face clipping, it is recommended to set a larger range for the sound source.

- The OSC prefab uses 28 bits of parameter memory, and the manual prefab uses 19 bits. Please ensure that the total does not exceed 256 bits within the avatar.

- Due to the special structure, you cannot change the heartbeat sound to other arbitrary sounds (music, sound effects, etc.). If you want to replace it with other heartbeat sound materials, editing with software such as Audacity is required.

- All states in the animator are unified with Write Defaults OFF (except DBT). There will be no problem if WD is properly unified on the avatar side, but if WD is mixed, problems may occur.

- Due to the specifications, when manually adjusting the heart rate, there may be a ±1 difference in heart rate between you and the other person.
