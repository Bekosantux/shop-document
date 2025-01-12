---
sidebar_position: 6
---

# Troubleshooting

<hr/>
## Common Issues
### An error occurs during upload (Avatar Validation Failed)
    - This occurs when the avatar's parameter count exceeds 256 bits.
    This can happen especially when trying to install it at the same time as complex assets such as smartphone.
    Consider removing unnecessary assets or using the Option prefabs.

### OSC signal is not reflected
    - Basically, OSC sending apps other than those recommended in this manual are not supported.
    This is because the parameter names do not match. Please use the apps listed.
    (For advanced users) If for some reason you cannot use the recommended apps, rewrite "HR" registered in MA, Animator, and DBT to the parameter name you want to use.

<hr/>
If it still doesn't work after clearing all of the following items, it's a bug. Please send a DM via Booth.
Feel free to contact us if you need help with the installation.
:::note
When contacting us, it would be very helpful if you could also include information about the avatar you are using and other assets (including outfits) you have installed.
Also, please try installing only the heartbeat system in an unmodified state.
Your cooperation will help us resolve the issue quickly.
:::

### Heartbeat sound cannot be heard / Heart rate counter is not displayed
- Manual heart rate control is not 0%
- Both "Heartbeat Sound" and "My Heartbeat (Local)" are turned on in the menu, but you can't hear it
- The heart rate counter is placed correctly and is not buried in the body
- Avatar volume is 100%
- You can't hear it in other worlds either (sounds may be drowned out in some worlds)
- It doesn't work even if you only install the system in an unmodified state

### OSC signal is not reflected
- Go to Pie Menu → Options → OSC in VRChat and enable OSC.
- Furthermore, if you select OSC Debug, a blue square frame labeled "HR" will flash below.
→ If "Not receiving any OSC messages?" is displayed, the transmission has failed.
- (For Pulsoid) All related programs are running (Pulsoid on smartwatch, Pulsoid on smartphone, HRtoVRChat)
- HRtoVRChat cannot be started before VRChat without changing the settings, and an error will be displayed.
- (For Bluetooth LE) Numbers are displayed in the window.
- If you close the window, you can redisplay it from the small icon in the system tray of the taskbar. If it's not there, restart the app.
