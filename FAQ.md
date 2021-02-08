---
layout: single
title: FAQ
---

## Is this better than Reelsteady Go for GoPro?
No.

## Is this better than SteadXP?
Probably not, but I haven't tried SteadXP.

## Any other tools/ressources I should know about?
* [BlackboxToGPMF](https://github.com/Cleric-K/BlackboxToGPMF/tree/gui) by Attilafustos and Cleric-K for emulating GoPro files for use with Reelsteady Go. Works best for action-style cameras with similar distortions as the GoPro.
* [blackbox2gpmf](https://github.com/jaromeyer/blackbox2gpmf) By jaromeyer. Similar to BlackboxToGPMF but specifically for Hero 7 files.
* [Virtual Gimbal](https://github.com/yossato/virtualGimbal) by Yoshiaki Sato. Another gyro-assisted stabilization tool that is in many ways much more advanced than Gyroflow at the moment (has rolling shutter correction). Although it has no graphical UI and I haven't tried it myself.
* [FPV stabilization tools Facebook group](https://www.facebook.com/groups/fpvtools)
* [RSgoBlackbox discord server](https://discord.gg/6Yk2dJQv)

## Are these questions actually "frequently asked"?
No, but they could be.

## How does gyro-based image stabilization work?
Not sure how many are wondering this, but I'm going to answer anyways :). Classic video stabilization methods work by estimating the camera motion using optical flow, but this involves "guesswork" so to speak.
MEMS gyroscopes can be used to determine the rotation of the camera very accurately. The first step is to sync the gyro and the video. Then a virtual camera cam be created that moves just like the physical camera, which "projects" the image onto an imaginary plane or sphere. Another (smoothed) camera can recapture the view, resulting in a stabilized video. In practice the projection and recapture can be combined using some fancy mathematics. 

This [companion video](https://youtu.be/I54X4NRuB-Q) to the the paper _Digital Video Stabilization and Rolling Shutter Correction using Gyroscopes_ by Karpenko et al. explains the basic concepts quite well. 

## I can't get X to work, what do?
Watch the tutorial if you haven't (note: tutorial is currently being made) and try asking in the Discord or Facebook group.

## There is no lens profile for X. What do I do?
Create a new lens profile by following the guide (in the works). If it works well, please submit it to be added as a default profile so others can use it.
Since you can add a name to the profile, future users can tell who the awesome calibrator was.

## I tried out a lens profile for my camera, but it doesn't work very well?
Try making a new lens profile to see if that helps. If it works better, please submit the new profile as well. Bad lens profiles typically move too much or too little during panning or tilting, and has "wobbling" at the edges.

## Does this work for DSLR/handheld footage?
It works *alright* for wide angle footage, but rolling shutter artifacts will be present in handheld/walking footage, especially at longer focal lengths.

## Will rolling shutter correction be added?
Soon™

## Why did you spend so much time/effort setting up a nice website and all that instead of adding features to Gyroflow?
Ultimately I'm working on all of this to try out/learn about various things, whether that be computer vision, image processing, orientation math, or in this case Jekyll. Since I don't actually have a serious need for a fancy stabilization tool, the goal is instead to have "fun" and make cool stuff, not rush out computer applications. I do admit that the website looks decent, but that's all thanks to the [Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/).