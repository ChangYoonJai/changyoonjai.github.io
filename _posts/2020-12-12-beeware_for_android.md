---
title: "Start BeeWare on Android"
categories:
  - BeeWare
tags:
  - Python
  - BeeWare
---

### Links

  [Tutorial](
    https://docs.beeware.org/en/latest/tutorial/tutorial-5/android.html#
    )
  
### Setup

+ Downloads an Android App Template & Add Python Codes
  (*It takse 10 mins or longer for the first time*)

  ```shell
  briefcase create android
  ```

+ Build into Android APK

  ```shell
  briefcase build android
  ```

  + Result

    ```shell
    BUILD SUCCESSFUL in 5m 14s
    28 actionable tasks: 28 executed

    [helloworld] Built android\Hello World\app\build\outputs\apk\debug\app-debug.apk
    ```

+ Run the App on Virtual or Physical Device
  
  ```shell
  briefcase run android
  ```

  + Result

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

  *If you run app on physical device for the first time, you'll prebably have to run command twice.*
