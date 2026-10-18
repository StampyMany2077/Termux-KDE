# Termux-KDE
this guide is for how to run kde on your android phone
| Functions | Do They Work ? |   
|------------|--------------
| Sound | Yes ✅ |   
| Wi-Fi | Yes ✅ |   
| KDE Connect to phone | Mostly ✅ |   
| 3d Acceleration | Yes ✅ (Though VirGL) |   
| Brightness and Volume control | Yes ✅ (Requires Termux:API) |   
# Prerequisites   
First for minimum use you will need [Termux](https://f-droid.org/repo/com.termux_1022.apk) and [Termux:X11](https://github.com/termux/termux-x11/releases/download/nightly/termux-x11-universal-debug.apk)   
If you want the controlls such as the Brightness and Volume controll you will need [Termux:API](https://github.com/termux/termux-api/releases/download/v0.53.0/termux-api-app_v0.53.0+github.debug.apk)   
# Setup Prerequisites   
To setup Termux for installing kde you will need to do this   
```
pkg upate && pkg upgrade -y
# It updates its core packages to the lastest version

pkg install x11-repo tur-repo -y
# It installs the packages thats needed to install kde and its componets

pkg termux-x11-nightly pulseaudio dbus -y
# Its required to get the display and sound to work
```

