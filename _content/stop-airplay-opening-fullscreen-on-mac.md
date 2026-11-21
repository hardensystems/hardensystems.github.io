---
title: "Stop AirPlay from Opening Fullscreen on Mac"
date: 2026-11-11
tags: [tech-tips]
platform: "YouTube"
video_id: "9fi4ZnR_wGQ"
description: "Use your Mac as a wireless viewfinder for iPhone filming by opening incoming AirPlay in a resizable window on macOS Sequoia."
---

When I film on my iPhone, I want to check the framing without walking back to the phone between takes. A Mac makes a handy wireless monitor, but I ran into two problems. Apple’s iPhone Mirroring feature stopped working when I opened the camera, and standard AirPlay took over the whole Mac display.

On macOS Sequoia, I used a Terminal setting to make incoming AirPlay open in a window I could move and resize. That gave me a viewfinder on my desktop while I kept the iPhone unlocked and adjusted the camera settings on the phone.

## Open AirPlay mirroring in a window

1. On the Mac receiving the AirPlay stream, press **Command–Space**, search for **Terminal**, and open it.
2. Paste the command below and press **Return**. Enter your Mac administrator password if prompted. Terminal keeps the password hidden as you type.
3. Restart your Mac.

```sh
sudo mkdir -p /Library/Preferences/FeatureFlags/Domain && sudo defaults write /Library/Preferences/FeatureFlags/Domain/ControlCenter APReceiverInWindow -dict Enabled -bool true
```

## Use your Mac as a viewfinder

On your iPhone, open **Control Center**, tap **Screen Mirroring**, and select your Mac. Move or resize the AirPlay window on your Mac, then open the camera on your iPhone. You can check the framing on the Mac while adjusting camera settings directly on the phone.

## Restore fullscreen mirroring

Run the following command in Terminal on the receiving Mac, then restart it.

```sh
sudo defaults delete /Library/Preferences/FeatureFlags/Domain/ControlCenter APReceiverInWindow
```
