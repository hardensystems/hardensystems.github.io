---
title: "Stop AirPlay from Opening Fullscreen on Mac"
date: 2026-11-11
tags: [tech-tips]
platform: "YouTube"
video_id: "9fi4ZnR_wGQ"
description: "Use Terminal on macOS Sequoia to make incoming AirPlay mirroring open in a movable, resizable window."
---

When AirPlay mirroring opens fullscreen, it takes over the Mac display. On macOS Sequoia, you can change a setting in Terminal so incoming mirroring opens in a window you can move and resize. That lets you keep the rest of your desktop visible while you mirror an iPhone or another Mac.

## Open AirPlay mirroring in a window

1. On the Mac receiving the AirPlay stream, press **Command–Space**, search for **Terminal**, and open it.
2. Paste the command below and press **Return**. Enter your Mac administrator password if prompted. Terminal keeps the password hidden as you type.
3. Restart your Mac, then start mirroring again.

```sh
sudo mkdir -p /Library/Preferences/FeatureFlags/Domain && sudo defaults write /Library/Preferences/FeatureFlags/Domain/ControlCenter APReceiverInWindow -dict Enabled -bool true
```

## Restore fullscreen mirroring

Run the following command in Terminal on the receiving Mac, then restart it.

```sh
sudo defaults delete /Library/Preferences/FeatureFlags/Domain/ControlCenter APReceiverInWindow
```
