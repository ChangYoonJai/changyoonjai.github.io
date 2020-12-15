---
title: "[BeeWare] Build Android App"
categories:
  - BeeWare
tags:
  - Python
  - BeeWare
---

## Links

[Official Tutorial](
  https://docs.beeware.org/en/latest/tutorial/tutorial-5/android.html#
  )

## Setup

### Create Android Templeate

It takse 10 mins or longer for the first time

```shell
briefcase create android
```

### Build into Android APK

```shell
briefcase build android
```

```shell
BUILD SUCCESSFUL in 5m 14s
28 actionable tasks: 28 executed
```

## Run the App
  
  ```shell
  briefcase run android
  ```

  If you run app on physical device for the first time, you'll prebably have to run command twice.

  ```shell
  Select device:

  1) Unknown device (not authorized for development) (R3CM803LEFJ)
  2) @Pixel_3a_API_29_x86 (emulator)
  3) Create a new Android emulator

  > 1

  The device you have selected (R3CM803LEFJ) has not had developer options and
  USB debugging enabled. These must be enabled before a device can be used  as a
  target for deployment. For details on how to enable Developer Options, visit:

    https://developer.android.com/studio/debug/dev-options#enable

  Once you have enabled these options on your device, you will be able to select
  this device as a deployment targe
  ```
