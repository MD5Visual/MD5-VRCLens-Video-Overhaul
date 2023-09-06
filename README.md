# MD5 VRCLens Videography Overhaul Extension

## Overview
This system is designed to allow enchanced control over video recording in VRChat utilizing Hirabiki's VRCLens as a foundation.

### Tools utilized in the system:
*General*
* [Hirabiki's VRCLens](https://hirabiki.gumroad.com/l/rpnel)
* [TouchOSC](https://hexler.net/touchosc)
* Apple Device (iPhone/iPad) *PREFERRED*
  __*or*__ Android Device (Phone/Tablet)
  __*or*__ PC or Mac
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

1. Download
   For Android/PC: VRCL-DC_Android_Win_X.XX.
