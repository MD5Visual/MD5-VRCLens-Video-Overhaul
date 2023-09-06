# MD5 VRCLens Videography Overhaul Extension

## Overview
This system is designed to allow enchanced control over video recording in VRChat utilizing Hirabiki's VRCLens as a foundation.

### Tools utilized in the system:
*General*
* [Hirabiki's VRCLens](https://hirabiki.gumroad.com/l/rpnel)
* [TouchOSC](https://hexler.net/touchosc)
* Apple Device (iPhone/iPad) *PREFERRED*
  
  __*or*__ Android Device (Phone/Tablet)
  
  __*or*__ PC
  
  __*or*__ Mac
* [OBS](https://obsproject.com/download)
  
*For Desktop Recording:*
* [ImgOverlay](https://github.com/Apprehentice/ImgOverlay/releases/tag/1.1.0)
* [Sizer](http://www.brianapps.net/sizer/)

## Automatic Setup Instructions

**WIP**

## Manual Setup instructions

### VRCLens Setup

1. Purchase a copy of [Hirabiki's VRCLens](https://hirabiki.gumroad.com/l/rpnel)
2. Download VRCL-DC Controller Update.unitypackage from the Releases
3. Select an avatar that you wish to add VRCLens to
4. import VRCLens .unitypackage into your Unity project
5. Add VRCLens prefab to your scene
6. Select the prefab
7. Set `Target Avatar` to be the avatar that you want to add the VRCLens to
8. *REQUIRED* When setting up the VRCLens prefab, these following settings have to be set correctly:

| For lowest performance hit: | *For best quality:* |
|---|---|
| Max Blur Size (Performance Adjustment): **Medium - RTX 2060/GTX 1080/ RX 6600** | Max Blur Size (Performance Adjustment): **Large - RTX 3060/RTX 2070 Super/ RX 6600 XT** |
| Enable drone controls: **ON** | Enable drone controls: **ON** |
| Sensor resolution: **2.1MP HD (1920x1080)** | Sensor resolution: **3.7MP QHD (2560x1440)**  |
| Anti-aliasing: **Off** | Anti-aliasing: **Auto** |

8. *OPTIONAL* You can set `Camera Model: **None**` to save on materials
9. Click "Apply VRCLens"
10. Import VRCL-DC Controller Update.unitypackage into your Unity Project
11. Replace/merge your `FX`/`Expression Menu`/`Expression Parameters` on your avatar with `VRCL_DC_Menu`/`VRCL_DC_Menu`/`VRCL_DC_Parameters` respectivelly
12. Your avatar is ready for upload!

### TouchOSC Setup

1. Download and install [TouchOSC](https://hexler.net/touchosc) on a device of your choosing
2. Download

| Platform | File |
|---|---|
| Android Phone | VRCL-DC_Android_X.XX.X_XXXXX.tosc |
| Android Tablet/PC/Mac | VRCL-DC_Android_Tab_Win_Mac_X.XX.X_XXXXX.tosc |
| iPad | VRCL-DC_iPad_X.XX.X_XXXXX.tosc |
| iPhone | VRCL-DC_iPhone_X.XX.X_XXXXX.tosc |

3. Load the file corresponding to your device into TouchOSC
4. Go to the ![TouchOSC_2023-09-06_20-29-10](https://github.com/MD5Visual/VRCL-DC/assets/134655923/8f6e0b12-77e9-4f91-99b9-4f68206021aa) menu and setup `OSC` and `GAMEPAD` sections
   ![TouchOSC_2023-09-06_20-29-42](https://github.com/MD5Visual/VRCL-DC/assets/134655923/432230e0-1bc4-4269-813e-6ecb76d188ea)

  > If you are using any device that is not the PC on which you are running VRChat, you have to download TouchOSC on your PC and have it running.
  Once you've done that, on your device press the `Browse` button next to the `Host:` input.
  It should show your computer on the list. Click on your PC name, and then select the `192.168.XXX.XXX` IP address. Otherwise, if your are using TouchOSC on your PC, use `127.0.0.1` like on the screenshot.

   ![TouchOSC_2023-09-06_20-29-58](https://github.com/MD5Visual/VRCL-DC/assets/134655923/b4c9df78-212a-48e9-88f5-46e7ea39a87e)

   > Once you have connected your gamepad to your device, press the checkbox next to `Connection 1` and then click `Browse` and select the controller that you have connected from the list.

5. Press ![TouchOSC_2023-09-06_20-30-14](https://github.com/MD5Visual/VRCL-DC/assets/134655923/d0dc3415-38a1-434b-ae76-b55480cc78c6) to launch the TouchOSC controller
6. TouchOSC is setup!

### VRChat Recording Setup



