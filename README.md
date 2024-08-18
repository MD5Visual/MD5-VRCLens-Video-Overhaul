# MD5 VRCLens Videography Overhaul Extension

![2023-09-07_00-20-29-min](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/e282e135-29ba-44ec-8e5c-c63b6b96610a)

Created by **MD5 Visual**

Twitter: [https://twitter.com/MD5Visual](https://twitter.com/MD5Visual)

Instagram: [https://www.instagram.com/MD5Visual/](https://www.instagram.com/MD5Visual/)

Discord: Mrdanslite

## Overview
This system is designed to allow enchanced control over video recording in VRChat utilizing Hirabiki's VRCLens as a foundation.

### Tools utilized in the system:
*General*
* [Hirabiki's VRCLens](https://hirabiki.gumroad.com/l/rpnel)
* [TouchOSC](https://hexler.net/touchosc)
* Apple Device (iPhone/iPad) *PREFERRED*
  
  __*or*__ Android Device (Phone/Tablet)
  
  __*or*__ PC/Mac

* Xbox Controller *PREFFERED*
* [OBS](https://obsproject.com/download)
  
*For Desktop Recording:*
* [ImgOverlay](https://github.com/Apprehentice/ImgOverlay/releases/tag/1.1.0)
* [Sizer](http://www.brianapps.net/sizer/)

## Automatic Setup Instructions

**WIP**

## Manual Setup instructions

### VRCLens Setup

> Video guide to go along with the written guide: **[VIDEO GUIDE](https://www.youtube.com/watch?v=mWhpjYjM0os)**

![vrcldc_tutorial_8 1 1](https://github.com/user-attachments/assets/57e0b5e0-3af6-4463-aa31-c53dd267433c)

1. Purchase a copy of [Hirabiki's VRCLens](https://hirabiki.gumroad.com/l/rpnel)
2. Download the latest `VRCL-DC Controller Update.unitypackage` from the Releases
3. Select an avatar that you wish to add VRCLens to
4. Import VRCLens .unitypackage into your Unity project
5. Add VRCLens prefab to your scene
6. Select the prefab
7. Set `Target Avatar` to be the avatar that you want to add the VRCLens to
8. *REQUIRED* When setting up the VRCLens prefab, these following settings have to be set correctly:

| For lowest performance hit: | *For best quality:** |
|---|---|
| Max Blur Size (Performance Adjustment): **Medium - RTX 2060/GTX 1080/ RX 6600** | Max Blur Size (Performance Adjustment): **Large - RTX 3060/RTX 2070 Super/ RX 6600 XT** |
| Enable drone controls: **ON** | Enable drone controls: **ON** |
| Sensor resolution: **2.1MP HD (1920x1080)** | Sensor resolution: **3.7MP QHD (2560x1440)**  |
| Anti-aliasing: **Off** | Anti-aliasing: **Auto** |

> *This "Best quality" is best ratio of performance hit to final shot result. If you have a 4K screen and a rig with multiple 4090s you can increase the sensor resolution to `8.3MP 4K (3840x2160)`, but that will only allow you to record a couple of people in the world at once.

9. *OPTIONAL* You can set `Camera Model: **None**` to save on materials
9. Click `Apply VRCLens`
10. Import `VRCL-DC Controller Update.unitypackage` into your Unity Project
11. Delete ALL `vCNT_*`, `vCNR_*`, `vCNG_*` and `vCNP_*` layers from your avatar `FX` controller
12. Delete ALL `VRCL_____` parameters from your avatar `FX` controller
13. Merge `VRCL_DC_FX` controller with your avatar `FX` controller
14. Replace/merge your `Expression Menu`/`Expression Parameters` on your avatar with `VRCL_DC_Menu`/`VRCL_DC_Parameters` respectivelly
15. Your avatar is ready for upload!

### TouchOSC Setup

1. Download and install [TouchOSC](https://hexler.net/touchosc) on a device of your choosing
2. Download the correct file for your platform

| Platform | File |
|---|---|
| Android Phone | VRCL-DC_Android_Win_X.XX.X_XXXXX.tosc |
| Android Tablet/PC/Mac | VRCL-DC_Android_Win_X.XX.X_XXXXX.tosc |
| iPad | VRCL-DC_iPad_X.XX.X_XXXXX.tosc |
| iPhone | VRCL-DC_iPad_X.XX.X_XXXXX.tosc |

3. Load the file corresponding to your device into TouchOSC
4. Go to the ![TouchOSC_2023-09-06_20-29-10](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/bc02fc8e-7f22-4d99-b464-9c1ae4745b44) menu and setup `OSC` and `GAMEPAD` sections

    ![TouchOSC_2023-09-06_20-29-42](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/34ecb53d-77f6-4814-874b-7b89b104c3a3)


  > If you are using any device that is not the PC on which you are running VRChat, you have to download TouchOSC on your PC and have it running.
  Once you've done that, on your device press the `Browse` button next to the `Host:` input.
  It should show your computer on the list. Click on your PC name, and then select the `192.168.XXX.XXX` IP address. Otherwise, if your are using TouchOSC on your PC, use `127.0.0.1` like on the screenshot.

   ![TouchOSC_2023-09-06_20-29-58](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/ce4b7999-1c4f-409a-af46-eafe5279e274)


   > Once you have connected your gamepad to your device, press the checkbox next to `Connection 1` and then click `Browse` and select the controller that you have connected from the list.

5. Press ![TouchOSC_2023-09-06_20-30-14](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/ba91f1b8-6885-4735-9df5-b8dedcc10a0e) to launch the TouchOSC controller
6. TouchOSC is setup!

### VRChat Recording Setup
> This is optional, but following this guide will provide you with the highest quality recording and maximum flexibility for editing the footage afterwards.

1. Go to VRChat Steam Properties and add these `launch options` depending on your screen resolution:

   | Screen Size | Launch Option |
   |---|---|
   | 2560x1440 | `-screen-width 2561 -screen-height 1440` |
   | 1920x1080 | `-screen-width 1921 -screen-height 1080` |

2. In OBS, add a new scene
3. Add `Game Capture` for VRChat
4. Add `Application Audio Capture` and select VRChat as the Window
5. Your "Audio Mixer" should look something like this:

![obs64_2023-09-06_20-59-24](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/898f7cc7-88c7-4cb0-a5c1-ee131d6a26a4)


6. Open up `Advanced Audio Properties`

![obs64_2023-09-06_21-04-33](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/c1671232-9eaa-435d-81ea-a8f707be7597)


7. And setup the tracks of different inputs like this:

![obs64_2023-09-06_21-10-14](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/f1c8670f-c0ab-40e9-95e8-08e004c92368)


8. Close `Advanced Audio Propertis`
9. Open OBS Settings
10. In `Video` set the `Base (Canvas) Resolution` and `Output (Canvas) Resolution` to `2560x1440` if you have a `2560x1440` resolution screen or `1920x1080` if you have a `1920x1080` resolution screen
11. Set the `Common FPS Values` to `30`, if not set by default

![obs64_2023-09-06_21-11-59](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/ad1966bf-24fd-49d1-83f5-d328e311ab45)


12. In `Output` set the `Output Mode` to `Advanced` and go to `Recording` tab
13. Set the settings to be like the screenshot

![obs64_2023-09-06_21-15-13](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/fd55894b-6d20-4956-994b-800e05ffd88a)


14. Click `Save`
14. You are ready to record!

> This is next section is only if you want to record while in desktop VRChat for increased performance (meaning more people shown in world)
> For VR Recording you can just jump in VR and start recording.

## Additional Desktop Only Recording setup instructions

### Pre-setup Instructions (ONLY NEEDED TO DO ONCE)

0. Download [ImgOverlay](https://github.com/Apprehentice/ImgOverlay/releases/tag/1.1.0) and [Sizer](http://www.brianapps.net/sizer/)
1. Install `Sizer` and unzip `ImgOverlay` to a convenient folder
2. Run both programs

### Sizer Instructions (ONLY NEEDED TO DO ONCE)

1. Right-click the `Sizer` icon from the `Show Hidden Icons` section in your taskbar and press `Configure Sizer...`

![chrome_2023-09-06_21-39-07](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/906e5d55-dd9e-4a5c-a5a6-c52de2276c8e)

2. Once in Sizer, click `Add Size` and a new window should pop up.
3. Set the `Description` to something like `VRCL-DC Overlay`
4. Set `Width` to `2561` and `Height` to `1480` for 2560x1440 screen size, or `Width` to `1921` and `Height` to `1080` for 1920x1080 screen size

![image](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/449f6a12-e3ed-4cf7-8d79-6c113c0c3618)



  
5. Click `OK*` to save

### ImgOverlay Instructions

1. In `ImgOverlay`, press `Load...` and load the `VRCL-DC Desktop Overlay.png`
2. Once loaded, press `Move Image` in ImgOverlay
3. Hover over the overlay image and press `Ctrl+Win+Z` to open up Sizer popup menu and press the `VRCL-DC Overlay` option in the menu that appears

![chrome_2023-09-06_21-53-46](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/823eb41d-3458-43ee-b9d4-fcf5851e3deb)


4. Once the overlay is resized, move it to match the overlay top left corner with VRChat window top left corner
5. After alignment, click `Move Image` again to disable the ability to move the overlay
6. Minimize the `Image Overlay` window and the overlay is ready to be used.

### VRChat instructions
1. When in `VRChat`, launch the `MD5 Camera System`, ensure all the settings are correct in the top right corner preview.
6. When you are ready to record, press `Shift+F3` to toggle fullscreen display of the camera.
8. Record!

# VRChat Controls Overview
> This guide assumes that you are familiar with VRCLens and the way it works. If not the instructions for it are bundled with the VRCLens purchase.

The radial menu has a new addition in form of `Quick Access`

![VRChat_2023-09-06_22-04-35](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/cf8c65e7-ce52-4acd-83c9-a12716c26178)


`Quick access` has links to Exposure, VR Monitor HUD, Zoom and Focus for easier access to these setting while in VR

![VRChat_2023-09-06_22-04-58](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/8bf6da31-8f34-4c39-8a4d-145510d2ce64)


When you want to control the VRCLens drone in VR, you are required to have both radial menus open on both controllers, one controlling the `Move Camera` and the other controlling the `Change Angle` at the same time

![VRChat_2023-09-06_22-04-50](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/6da1cd0d-43fe-4d20-9563-88c3f0a4f9aa)
![VRChat_2023-09-06_22-04-46](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/e8fb496c-1188-4cdd-b96d-1738b0c82d51)

When you have VRCLens enabled, make sure that `DirectCast` icon is shown ![ApplicationFrameHost_2023-09-06_22-18-30](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/58e2f95f-b6a4-4d69-8297-f0b5564a3ea3)


![VRChat_2023-09-06_22-06-38](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/ba9f52e8-944a-4c24-9f16-eddc17cbf8e9)


# TouchOSC Overview

![TouchOSC_2023-09-06_22-09-01](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/d4e3efa2-8376-4a50-b3b6-3bcf02c4df77)


The control surface is divided into 3 main sections: `Top Bar` `Camera Control` `Drone Control`

## Top Bar

![ApplicationFrameHost_2023-09-06_22-24-59](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/c5372c4c-aa3e-46f2-84d6-503b23cdf68d)


This section has information about the current version as well platforms this TouchOSC file is designed for. W - Windows/Mac, A - Android, I - Apple devices

![ApplicationFrameHost_2023-09-06_22-28-44](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/547983a2-646f-47cf-8941-c8bff4209731)


This section shows current time, battery percentage as well as On/Off buttons for the camera system in VRChat.
The `OFF` button only triggers on double click.

## Camera controls

![ApplicationFrameHost_2023-09-06_22-30-17](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/1c86c088-f280-4b16-8b47-b1afc164e624)


Here are the aperture and Focus controls. The slider can be adjusted with touch, as well as holding down the `Inc`/`Dec` buttons to Increase/Decrease the value

![ApplicationFrameHost_2023-09-06_22-32-42](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/7088d913-c981-4bb4-8958-042f9cfd9510)


The main button pad houses most common buttons that are used when doing recordings.
`Drone Reset` re-locks the camera back to the initial position and stops the drone operation. To move the drone again `Drone ON` button has to be toggled on and off and on again.

![ApplicationFrameHost_2023-09-06_22-35-37](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/64684af3-6ef9-4d2e-a399-d999ed055682)


The focus control section has preset buttons for 50mm focal length and 22mm focal length, as well as `Inc`/`Dec` buttons with regular slider touch control.

## Drone Controls

![ApplicationFrameHost_2023-09-06_22-37-40](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/b5145b3b-2b4c-4164-a629-33089982f579)
![ApplicationFrameHost_2023-09-06_22-37-34](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/a33d489a-9bc7-46c5-a0ff-48886d061524)


This displays the current state of the sticks that control the drone movement. The farther they are to the edges the faster the drone moves/rotates.

![ApplicationFrameHost_2023-09-06_22-39-04](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/3d5d2e24-edaa-4fcc-b98d-38d24b3feaae)


This section shows the current rate of the `Up`/`Down` movement

![ApplicationFrameHost_2023-09-06_22-40-34](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/6119d6fd-7e6e-4ef9-8fdf-17302b93541c)


The main drone speed move speed adjustment slider, only affects the movement, not the rotation of the drone.

![ApplicationFrameHost_2023-09-06_22-41-24](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/b58d4ca4-dbbc-44f3-82cc-025b3adc29b8)


The button that toggles the movement of the drone on or off.
> Sadly, does not react to the actual state of the drone, so if the drone is not moving, but the button says `Drone ON`, just press it off and on again and it should work.

![ApplicationFrameHost_2023-09-06_22-43-18](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/dec7c12c-2de6-403e-85ef-751ac3376deb)


The `Boost` button BOOOOOOOOOOOOOOOOOSTS the drone speed. Effectively sets the `Drone Move Speed` to `1` while the button is pressed.

# Controller Layout

![Photoshop_2023-09-06_23-23-28](https://github.com/MD5Visual/MD5-VRCLens-Video-Overhaul/assets/134655923/95c9fb4f-f6e8-486d-bc9b-3be99866a310)



