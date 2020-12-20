---
title: "[Kivy] Ubuntu on Windows 10"
categories:
  - Kivy
tags:
  - Python
  - Android
  - Kivy
  - Ubuntu
  - 우분투
  - Python-for-Android
---

## References

+ [python-for-android documents](
  https://python-for-android.readthedocs.io/en/latest/quickstart/
  )

## [Tip] Install Ubuntu on Windows 10

1. Microsoft Store에서 **Ubuntu** 를 검색하고 설치
*Install **Ubuntu** in Microsoft Store*

2. Windows 기능에서 "Linux 용 Windows 하위 시스템" 기능 켜기
*Turn on "Windows subsystem for Linux"*

## Install python-for-android

```bash
pip install python-for-android
```

```bash
sudo dpkg --add-architecture i386
sudo apt-get update
sudo apt-get install -y build-essential ccache git zlib1g-dev python3 python3-dev libncurses5:i386 libstdc++6:i386 zlib1g:i386 openjdk-8-jdk unzip ant ccache autoconf libtool libssl-dev
```

```bash
sudo pacman -S core/autoconf core/automake core/gcc core/make core/patch core/pkgconf extra/cmake extra/jdk8-openjdk extra/python-pip extra/unzip extra/zip
```

## Install Android NDK

Download from: [android-developer-ndk](https://developer.android.com/ndk/downloads/)

## Install Android SDK (command)

Download "Command line tools only" from: [android-downloads](https://developer.android.com/studio?#downloads)
```bash
sudo apt update && sudo apt install android-sdk
```

## Set Paths for Android

```bash
ls $HOME\android
android-ndk-r21d  cmdline-tools
```

```bash
~/.bashrc
```

```bash
################################################################
# Android Environment
export ANDROIDNDKVER="r21d"  # Version of the NDK you installed
export ANDROIDAPI="27"  # Target API version of your application
export NDKAPI="21"  # Minimum supported API version of your application
export ANDROIDNDK="$HOME/android/android-ndk-$ANDROIDNDKVER"
export ANDROIDSDK="$HOME/android/cmdline-tools/bin"
export SDKMANAGER="$ANDROIDSDK/sdkmanager"
```

## Donwload Adnroid SDK Platforms

```bash
$SDKMANAGER "platforms;android-21" --sdk_root=$ANDROIDSDK  # minimum version
$SDKMANAGER "platforms;android-27" --sdk_root=$ANDROIDSDK  # target version
$SDKMANAGER "platforms;android-30" --sdk_root=$ANDROIDSDK  # latest version
```

```bash
$SDKMANAGER --list --sdk_root=$ANDROIDSDK
$SDKMANAGER "build-tools;30.0.3" --sdk_root=$ANDROIDSDK
```
