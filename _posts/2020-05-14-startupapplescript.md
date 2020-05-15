---
layout: post
title:  "Delay Services launch until external drive mount is complete."
date:   2020-05-14 14:30:00 +0900
author: Adam Spann
categories: [Coding, AppleScript, Automation]
tags: [AppleScript, Mac Mini, Automation]
---

## The Challenge:
How to give Drobo time to mount before processes that need access to it begin and hence
block it's mounting by having the mount point in use.
## Solution:
AppleScript

Why was this an issue for me. Well I have a Drobo drive which is over 75% full.
As a result it can take a while to mount and be detected by my old Mac Mini. This would mean that processes that use files from the Drobo would start before it was mounted. And a mount point is use can not be mounted.

{% gist 1abb5dafe36f0f06f727b00a214e855e %}

So let's break this down a little.

- line 1 sets a boolean that is false until "Finder" indicates that "Drobo" is seen. Drobo is the name that I have given to my Drobo drive, yes not very original.
- Lines 2 through to 9 wait for the Drobo to be mounted. Checking every 30 seconds. Once it's been found. The loop condition ends.
- Lines 12 to 14 then tell each application in turn to launch.

## Installation
  - Open Apple's Script Editor and export as an Application.
  - Open your "Users and Groups" manager.
  - Select your user account and add the application to your "Login Items".
  - Remove any applcations that you have added to the script from the "Login Items" if they are already present. You should be ok to go next time you reboot your machine.
