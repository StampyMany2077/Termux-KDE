# Termux-KDE
This guide is for how to run kde on your android phone
| Functions | Do They Work ? |   
|------------|--------------
| Sound | Yes ✅ |   
| Wi-Fi | Yes ✅ |   
| KDE Connect to phone | Mostly ✅ |   
| 3d Acceleration | Yes ✅ (Though VirGL) |   
| Brightness and Volume control | Yes ✅ (Requires Termux:API) |   
# Prerequisites   
First for minimal use you will need [Termux](https://f-droid.org/repo/com.termux_1022.apk) and [Termux:X11](https://github.com/termux/termux-x11/releases/download/nightly/termux-x11-universal-debug.apk)   
If you want the controls such as the Brightness and Volume control you will need [Termux:API](https://github.com/termux/termux-api/releases/download/v0.53.0/termux-api-app_v0.53.0+github.debug.apk)   
# Setup Prerequisites   
To setup Termux for installing kde you will need to do this   
```
pkg upate && pkg upgrade -y
# It updates its core packages to the lastest version

pkg install x11-repo tur-repo -y
# It installs the packages thats needed to install KDE and its componets

pkg termux-x11-nightly pulseaudio dbus curl -y   
# Its required to get the display and sound to work
```
# Setup   
In order to run kde you will need to run this   
For full install   
```
pkg install plasma kde-applications -y
# this installs KDE plasma (the desktop envirment) and its applications
```
For a minimal installation   
```
pkg install plasma-desktop -y
# It only installs the core essentals needed for KDE to run
```
Next you will need 3d acceleration   
To install it run this   
```
pkg install mesa-zink virglrenderer-mesa-zink vulkan-loader-android -y
```
# Run KDE   
In order to run KDE you will need to get the install sh script   
To download the script you will need to run   
```
curl -fsSL https://github.com/StampyMany2077/Termux-KDE/releases/download/Autorun-scripts/start-kde.sh -o start-kde.sh
# This innstalls the start script

chmod +x start-kde.sh
# This allows termux to run the .sh file

./start-kde.sh
# This runs the script
```
The last thing to do is to open up Termux:X11 and it should just work   


