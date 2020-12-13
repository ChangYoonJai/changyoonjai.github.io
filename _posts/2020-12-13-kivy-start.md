---
title: "[Kivy] Start"
categories:
  - Kivy
tags:
  - Python
  - Kivy
---

## Links

  [Official Site](
    https://kivy.org/doc/stable/gettingstarted/installation.html
    )
  
## Setup Environment

+ Install modules
  ```pip install --upgrade pip setuptools virtualenv```
  </br>

+ Creat virutal enviromnet for kivy *(Optional but **Stronly Recommend**)*
  ```python -m virtualenv kivy_venv```
  </br>

+ Activate Virutal Environment

  ```kivy_venv\Scripts\activate```

## Install Kivy

```python -m pip install kivy```

### [Tip] Backup & Restore Virutal Environment

```pip freeze > kivy_venv.txt```
```pip install -r kivy_venv.txt```

## Create "Hello World" Project

  ```python
  from kivy.app import App
  from kivy.uix.button import Label

  class MainApp(App):
    def build(self):
        return Label(text='Hello World')

  MainApp().run()
  ```
