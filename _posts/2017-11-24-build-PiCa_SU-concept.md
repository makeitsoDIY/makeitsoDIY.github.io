---
layout: post
title: The PiCa_SU - a RasPi-based IP-cam for streaming and more
---

## Introduction
I would very much like to document my projects in still images and video. Having live-footage to stream via OBS would make me able to engage in more social making, i.e. via [twitch](https://twitch.tv/creative).
The main purpose of a suitable camera is to capture my workspace in an overhead view. However, I would like the opportunity to hardware-zoom to a detail or to change the angle. An electric viewfinder would aid a lot with achieving this on-the-fly.
My current housing calls for a wireless solution, but I want the device to support wired comnication, for the future.
Since streaming live is one central use-case of the cam, I would like to control the camera without leaving the workbench and perhaps even hands-free. Lighting is poor in my workspace but essential for quality images. The cam needs a light-source, too.

### My wishlist
- IP-based camera
- Recording and streaming video in 1080p
- Taking still images while recording
- supporting WiFi and LAN
- SFTP-server to access still images
- Optical lenses to zoom and/or swap
- Electrical viewfinder / display
- Control-panel +/- pedals for hands-free control
- Status-display inside control-panel
- Mounting-system for overhead recording and adjusting angles:
 - female 1/4'' thread for mounting to a tripod
 - ball-head mount for quick adjustments 
- Rugged, suitable case for a dusty workshop
- reasonably powerful, detachable LED ringlight
- No 3D-printing, CNC-routing or lasers (pewpew!) required

### What's on the market?
Since my wishlist is somewhat long and specific, I do not expect the market to offer a pre-made solution that perfectly suits my needs or my wallet. However, a few products exist that a maker should be aware of before re-inventing the wheel:  
[ModMyPi](https://www.modmypi.com/raspberry-pi/cases-183/raspberry-pi-b-plus2-and-3-cases-1122/nwazet-pi-camera-box-bundle-case,-lens-and-wall-mount-b-plus) offers a solution that comes reasonably close to my wishlist, it lacks the viewfinder and controls, though. It also has no lighting.
The design looks thoughtful and -just by its looks- is likely to suffice for your average surveillance-project. Most of the missing features could be added as peripherals, but I would like a tailored and integrated solution. So off to the drawing-board it is...

## Turning my whishes into a concept
The RaspberryPi and its camera-modules easily cover the five first (and central!) items of my list. The combination of my need for LAN-support, "decent" computing-power for streaming and the ability to connect peripherals of my own design (both via USB and GPIO)
let the RasPi3 appear to be the best solution, despite some promising [results](https://hackaday.com/2017/03/26/turn-that-pi-zero-into-a-streaming-camera-step-by-step/) achieved with the RasPi zero.

The electrical viewfinder could be created by connecting any HDMI-capable screen. GPIO-based solutions, like in [this](https://www.adafruit.com/product/2298) example, will leave the HDMI-port free to use, while effectively blocking only a small amount of GPIO-pins. While a resolution of 320x240 px is certainly not
enough to set a correct focus for footage recorded in 1920x1080 px, it would suffice as a viewfinder in situations where the focus is set to infinity and therefore will not need to be adjusted. Besides, because of the nature of a streaming cam, any device with a 1080px-display and a connection to the network can be used
to set the focus, if necessary. Since this kind of viewfinder is only requiered when adjusting the view, the TFT could double as a status-display.

For reasons of compatibility and ease, I want to integrate as many pre-made solutions from photo/video-sector as possible. [This](https://www.amazon.de/dp/B014F6G2TM/ref=cm_sw_r_tw_dp_x_m6agAbJHCDVN2) flexible arm seems like a good solution to center the mounting system around.

Now for the central part, the camera itself, decisions are tricky: While the the original v2-camera had some issues regarding its [focus](https://www.reddit.com/r/raspberry_pi/comments/6hr5qn/fixing_the_blurry_focus_on_some_raspberry_pi/), the sensor looks decent and I want a solution of equal or better specs. As far as lenses go, people have achieved interesting [results](https://www.instructables.com/id/The-SnapPiCam-A-Raspberry-Pi-Camera/) with magnetic smartphone-accesoirs like [these](https://www.modmypi.com/raspberry-pi/camera/camera-lenses
).Changing lenses constantly and thereby exposing the sensor or lens-mount to the dusty environment seems less than ideal, though. Recently however, inofficial camera-modules are being released, that carry C- or M12-mounts as are used in CCTV-applications, allowing for a wide range of zoom-lenses to be used.
[This](http://www.arducam.com/8mp-sony-imx219-camera-raspberry-pi/ ) model by Arducam features the very same sensor that is used in the v2.1-original while providing a CS-mount. My weapon of choice...
http://www.arducam.com/8mp-sony-imx219-camera-raspberry-pi/ 

As for the case, lens-mount and lighting, I will have to come up with my own design - at another time...

For now, the tasks ahead are:
- obtain the first and central batch of components:
  - RasPi3
  - Arducam 8MP module with CS-mount
  - piTFT+ display
- set up hard- and software to demonstrate the working concept
- obtain remaining components
- design control-panel
- design pedals
- design enclosure(s)
- build the thing
- bask in video-awesomeness

This is going to take a while. Off we go!