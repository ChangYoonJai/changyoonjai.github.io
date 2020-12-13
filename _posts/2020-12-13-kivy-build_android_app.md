---
title: "[Kivy] Build Android App"
categories:
  - Kivy
tags:
  - Python
  - Kivy
  - Android
---

## References

+ [Getting StartedGetting Started » Packaging](
    https://kivy.org/doc/stable/gettingstarted/packaging.html
  )
+ [Buildozer (GitHub)](
    https://github.com/kivy/buildozer
  )
+ [Buildozer (wiki)](
    https://buildozer.readthedocs.io/en/latest/
  )
  
## Buildozer

### Install buildoze

  ```pip install buildozer```

## Init buildozer

  ```buildozer init```

  This creates a buildozer.spec file controlling your build configuration.

## Update spec file

  ```text
  [app]

  # (str) Title of your application
  title = My Application

  # (str) Package name
  package.name = myapp

  # (str) Package domain (needed for android/ios packaging)
  package.domain = org.test

  # (str) Source code where the main.py live
  source.dir = .\app

  ...
  ```

## Building isn't supported yet on Windows (OMG)

  "Android: via Python for Android. You must have a Linux or OSX computer to be able to compile for Android."
