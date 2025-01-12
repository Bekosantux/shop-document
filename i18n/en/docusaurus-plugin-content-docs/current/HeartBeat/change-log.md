---
sidebar_position: 999
---

# Update History
<hr/>
2025/1/4 v2.1.0
- Added local mute function
- Added a prefab for only the heart rate counter
- Added optional prefabs
- Added parameters `HBG/Local_Mute_Bool` and `HBG/Local_nBeatTime`
- Unified the animator for manual and OSC
- Corrected the sound range change to be linear
- Fixed an issue where the `VRC Animator Play Audio` component was not working correctly

2024/6/16 v2.0.0
- Added 3 new heartbeat sounds
- Changed the pitch to change randomly within a certain range when playing the sound source
- Supported avatar scaling
- Supported non-uniform scale changes of the parent object
- Reduced CPU load by using Direct Blend Tree
- Used Animated Animator Parameter instead of Contact for parameter calculation
- Changed to directly placing the Audio Sources object
- Changed and organized parameter names
- Eliminated playback waiting time when loading avatars
- Changed the prefab name of the OSC prefab
- Changed the shader for the sound range display sphere

2023/12/10 v1.0.0
- Initial release
