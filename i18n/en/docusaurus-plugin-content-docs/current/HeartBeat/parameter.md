---
sidebar_position: 7
---

# Parameters
<hr/>
- HR (OSC only)
    Int value of heart rate. From 0 to 255.
    **Recommended for customization.** Recommended for creating gimmicks that are triggered by a certain heart rate, such as sleep detection.

- HBG/HRCounter_Bool
    Bool value for whether to display the heart rate counter.

- HBG/Sound_Bool
    Bool value for whether to play the heartbeat sound.

- HBG/SoundRadius_Float
    Float value for adjusting the audible range of the heartbeat sound.

- HBG/ManualHR_Float
    Float value for controlling the heart rate with a radial puppet. Converts from 0 to 1 within the heart rate range of 50 to 177.
    (For customization, please use HBG/Local_FullHR_Float below if possible)

- HBG/HRCounterFlash_Bool
    Bool value for whether to blink the heart rate counter.

- HBG/AutoControlHR_Bool (OSC only)
    Bool value for whether to control the heart rate with the OSC signal.

Parameters with the prefix "Local_" are for local operation.

- HBG/Local_AdjustingRadius_Bool
    Bool value for whether the heartbeat sound range is being changed. Used to display the sphere indicating the sound source range.

- HBG/Local_FullHR_Float
    Float value with HR converted to a range of 0 to 1. Synchronized with high accuracy.
    **Recommended for customization.** Can be used when creating gimmicks that are proportional to the heart rate, such as changing the redness of the face.

- HBG/Local_Mute_Bool
    Bool value for whether to mute your own heartbeat sound.

- HBG/Local_ListenOwnHB_Bool
    Bool value for whether to hear your own heartbeat sound.

- HBG/Local_nSoundRadius
    Used to make the heartbeat range follow avatar scaling.

- HBG/Local_nBeatTime
    Contains the normalized playback time of the heartbeat sound.
    **Recommended for customization.** By using it in the Motion Time of an animation, you can play any animation in sync with the heartbeat sound.

- ScaleFactor
    VRChat standard parameter. Used to maintain consistency with avatar scaling.

- Blend
    Used to enable Direct Blend Tree (DBT).
