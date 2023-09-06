# MD5 VRCLens Videography Overhaul Extension

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

8. *OPTIONAL* You can set `Camera Model: **None**` to save on materials
9. Click `Apply VRCLens`
10. Import `VRCL-DC Controller Update.unitypackage` into your Unity Project
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

![obs64_2023-09-06_20-59-24](https://github.com/MD5Visual/VRCL-DC/assets/134655923/2f36f859-54e3-42ad-b489-0e338306c25a)

6. Open up `Advanced Audio Properties`

![obs64_2023-09-06_21-04-33](https://github.com/MD5Visual/VRCL-DC/assets/134655923/94a862ef-6fe3-41f8-896e-ae330674acda)

7. And setup the tracks of different inputs like this:

![obs64_2023-09-06_21-10-14](https://github.com/MD5Visual/VRCL-DC/assets/134655923/8a6d02a1-9037-4acf-bfeb-8ff310156d7e)

8. Close `Advanced Audio Propertis`
9. Open OBS Settings
10. In `Video` set the `Base (Canvas) Resolution` and `Output (Canvas) Resolution` to `2560x1440` if you have a `2560x1440` resolution screen or `1920x1080` if you have a `1920x1080` resolution screen
11. Set the `Common FPS Values` to `30`, if not set by default

    ![obs64_2023-09-06_21-11-59](https://github.com/MD5Visual/VRCL-DC/assets/134655923/3527ea0d-a106-45e0-9662-8820bd8f1515)

12. In `Output` set the `Output Mode` to `Advanced` and go to `Recording` tab
13. Set the settings to be like the screenshot

    ![obs64_2023-09-06_21-15-13](https://github.com/MD5Visual/VRCL-DC/assets/134655923/bcc87f1f-e41e-46b4-9e7b-c80670126170)

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

![chrome_2023-09-06_21-39-07](https://github.com/MD5Visual/VRCL-DC/assets/134655923/5953f887-7d34-4ce9-85e0-3d40911b2b4e)

2. Once in Sizer, click `Add Size` and a new window should pop up.
3. Set the `Description` to something like `VRCL-DC Overlay`
4. Set `Width` to `2561` and `Height` to `1440` for 2560x1440 screen size, or `Width` to `1921` and `Height` to `1080` for 1920x1080 screen size

![sizer_2023-09-06_21-50-51](https://github.com/MD5Visual/VRCL-DC/assets/134655923/46b8457c-fb8e-4fcc-a4e4-25d2dfa555d9)
  
5. Click `OK*` to save

### ImgOverlay Instructions

1. In `ImgOverlay`, press `Load...` and load the `VRCL-DC Desktop Overlay.png`
2. Once loaded, press `Move Image` in ImgOverlay
3. Hover over the overlay image and press `Ctrl+Win+Z` to open up Sizer popup menu and press the `VRCL-DC Overlay` option in the menu that appears

![chrome_2023-09-06_21-53-46](https://github.com/MD5Visual/VRCL-DC/assets/134655923/442e3eeb-dac2-4a79-99c6-bc9f3b3e5da2)

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

![VRChat_2023-09-06_22-04-35](https://github.com/MD5Visual/VRCL-DC/assets/134655923/b4bf771e-ed1e-4c2b-8cd3-17521a62cfce)

`Quick access` has links to Exposure, VR Monitor HUD, Zoom and Focus for easier access to these setting while in VR

![VRChat_2023-09-06_22-04-58](https://github.com/MD5Visual/VRCL-DC/assets/134655923/fb3d6c34-6ea3-4457-89f1-8e91ee95b554)

When you want to control the VRCLens drone in VR, you are required to have both radial menus open on both controllers, one controlling the `Move Camera` and the other controlling the `Change Angle` at the same time

![VRChat_2023-09-06_22-04-50](https://github.com/MD5Visual/VRCL-DC/assets/134655923/5f75798d-2cdf-48ed-b758-7af865831af1)
![VRChat_2023-09-06_22-04-46](https://github.com/MD5Visual/VRCL-DC/assets/134655923/3f8ce432-54d3-4050-906a-ec388433b4fc)

When you have VRCLens enabled, make sure that `DirectCast` icon is shown ![ApplicationFrameHost_2023-09-06_22-18-30](https://github.com/MD5Visual/VRCL-DC/assets/134655923/00f43096-f690-4e21-ada9-671c14e84535)

![VRChat_2023-09-06_22-06-38](https://github.com/MD5Visual/VRCL-DC/assets/134655923/164fb908-cb8b-45bf-9ff6-54ab4afb661f)

# TouchOSC Overview

![TouchOSC_2023-09-06_22-09-01](https://github.com/MD5Visual/VRCL-DC/assets/134655923/a1dd51ef-692d-41a5-834a-e50e8b0016e9)

The control surface is divided into 3 main sections: `Top Bar` `Camera Control` `Drone Control`

## Top Bar

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/4f94e164-b6aa-41ad-bbe4-30394d6aecf5)

This section has information about the current version as well platforms this TouchOSC file is designed for. W - Windows/Mac, A - Android, I - Apple devices

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/99b3a71e-0eeb-44d7-b34e-061d93a7c085)

This section shows current time, battery percentage as well as On/Off buttons for the camera system in VRChat.
The `OFF` button only triggers on double click.

## Camera controls

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/b3e234c1-fef5-47ca-9c2b-11b4004591a1)

Here are the aperture and Focus controls. The slider can be adjusted with touch, as well as holding down the `Inc`/`Dec` buttons to Increase/Decrease the value

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/1053bc5f-c5c5-4cab-a69c-265792ce5377)

The main button pad houses most common buttons that are used when doing recordings.
`Drone Reset` re-locks the camera back to the initial position and stops the drone operation. To move the drone again `Drone ON` button has to be toggled on and off and on again.

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/3e24ebfb-0481-4929-887b-6170ec2a87a8)

The focus control section has preset buttons for 50mm focal length and 22mm focal length, as well as `Inc`/`Dec` buttons with regular slider touch control.

## Drone Controls

![ApplicationFrameHost_2023-09-06_22-37-34](https://github.com/MD5Visual/VRCL-DC/assets/134655923/19979199-7956-4284-bb00-28aaf6e87609)
![ApplicationFrameHost_2023-09-06_22-37-40](https://github.com/MD5Visual/VRCL-DC/assets/134655923/b2590e2e-a778-4c61-b951-4981674752bb)

This displays the current state of the sticks that control the drone movement. The farther they are to the edges the faster the drone moves/rotates.

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/bd5a99bb-cf01-4685-a834-08d95b776c7a)

This section shows the current rate of the `Up`/`Down` movement

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/75caada8-a09a-4f9e-86f3-ec967925e517)

The main drone speed move speed adjustment slider, only affects the movement, not the rotation of the drone.

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/2d4af2e7-3f21-4794-8f25-31c12f57871e)

The button that toggles the movement of the drone on or off.
> Sadly, does not react to the actual state of the drone, so if the drone is not moving, but the button says `Drone ON`, just press it off and on again and it should work.

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/f6f97ea9-d290-4bd8-a33c-af290481c554)

The `Boost` button BOOOOOOOOOOOOOOOOOSTS the drone speed. Effectively sets the `Drone Move Speed` to `1` while the button is pressed.

# Controller Layout

![image](https://github.com/MD5Visual/VRCL-DC/assets/134655923/f777486e-067c-4259-8f12-10b734ec43f7)


