---
layout: post
title: The PiCaSU - updates on the build
---

## Good morning, reality! Thanks! Fu** you, too!
Since one of the reasons to start building the PiCaSU was to reacquaint me with coding through a project, I was very happy to recieve the components and get started. Developing on/for a remote RPi seems to be quiet a hassle, though. The most effecient way for development seems to be a remote desktop-session, which I strongly dislike. As soon as I achieved a working app-core and changes become less frequent, I will try to switch to a purely git-based workflow - thus allowing anyone interested to join in.

My learning-curve regarding Python is starting out somewhat flat, to be honest; the resulting level of frustration is high. I successfully soothe myself by telling me that the project is an ambitious one, for someone who has not coded a single line for years.
Let's stay on track...

## An update on the parts list
While ordering the parts, I included a somewhat major change: The [original display](https://www.adafruit.com/product/2298), that was intended as a mere viewfinder, was exchanged for the [official RPi-touchscreen](https://shop.pimoroni.de/products/raspberry-pi-7-touchscreen-display-with-frame). This will allow a better image-quality in the viewfinder and controlling the entire device via a touch-UI. On the plus-side, this frees more GPIO-pins. Sadly, it also added to the total price. I'm positive though, that it's going to turn out as a good investment.

A second change, though of a more preliminary character, happend regarding the camera. For ease of support and the price, I started to develop the PiCaSU around the [original RPi-camera v2.1](https://shop.pimoroni.de/collections/raspberry-pi/products/raspberry-pi-camera-module-v2-1-with-mount). Image-quality seems reasonable at a first glance and the issues regarding focus seem to have been properly adressed, based on my observations (n=1, it doesn't get more significant ;-) ). As soon as I established a decent touch-control, I will try different focus settings and cheap smartphone lenes. Depending on the results, I may even skip the more expensive [module](http://www.arducam.com/8mp-sony-imx219-camera-raspberry-pi/) in the final build.

## Whats ahead?
I will use my spare time to get the coding done. Since I have a major exam coming up in spring, I will need to focus my attention on rather un-techie matters, though. My next fix of nerdstuff, electric radiation and mate-drinks will be the [34th Chaos Communication Congress - 34C3](https://events.ccc.de/congress/2017/wiki/index.php/Main_Page), which I was looking forward to since last december.

## TL;DR
+ Re-Learning how to code is giving me trouble
+ The project turns out to be more complex than expected
+ Remote development feels uncomfortable
+ I upgraded the display to the official RPi-display
+ For development - and possibly for future productive use - I switched to the original RPi-cam v2.1
+ My professional life will keep me occupied, all builds will continue in the scarce, remaining spare time
+ I am attending 34C3 as a visitor. It's gonna be awesome.