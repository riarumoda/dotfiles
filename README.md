![banner](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/banner/main.png)
# What's this?
This is my personal config files for i3-gaps. Based on EvanKoe & rxyhn dotfiles.
# Purpose of this rice
I actually used rxyhn dots before, and i like it. but his awesome modules spawned on the second monitor if i plug a second monitor to my laptop and got annoyed by it. After some researching, i3 does not do this and used EvanKoe dots on it (2022 one). But my head went "Frick it. Combine both of them." And this dots born.
# Status of this rice
- i3-gaps : ✅
- alacritty : ✅
- polybar : ✅
- picom : ✅
- rofi : ✅
- GTK2 Theming : 🚸 (Buggy, mainly used to translate GTK theme to QT5 Only.)
- GTK3 Theming : ✅
- GTK4 Theming : ✅
- QT5 Theming : 🚸 (See GTK2 Theming.)

# Screenshots
| Location | Screenshots |
| --- | --- |
| **Desktop** | ![desktop](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/screenshots/desktop.png) |
| **App Menu** | ![rofi](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/screenshots/rofi.png) |
| **Terminal & GTK3 Apps** | ![alacritty](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/screenshots/alacritty-and-gtk-apps.png) |
| **QT5 Apps** | ![audacious](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/screenshots/qt-apps.png) |
| **Login Screen/Lockscreen** | ![lightdm](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/screenshots/loginscreen.png) |

# Installation (Arch Linux Only, fresh install)
Install the deps first :
```
xorg-server i3-gaps nitrogen xfce4-notifyd brightnessctl dex light-locker alacritty pcmanfm-gtk3 scrot rofi dmenu lxappearance-gtk3 lightdm lightdm-gtk-greeter noto-fonts noto-fonts-cjk noto-fonts-emoji noto-fonts-extra ttf-font-awesome gtk-engine-murrine polybar papirus-icon-theme
```
Optional but recommended :
```
arandr gpicview l3afpad lxtask-gtk3
```
Then from AUR :
```
picom-git volantes-cursors
```
Optional but recommended from AUR :
```
uwufetch polkit-dumb-agent-git qt5-styleplugins gtk3-classic cava libxfce4ui-nocsd
```
Clone my dots and copy to the desired folders
```
git clone https://github.com/Putu-Justine/dotfiles.git
cd dotfiles
cp -r configs/* ~/.config
sudo cp -r themes/* /usr/share/themes
sudo cp -r wallpapers/* /usr/share/pixmaps
```
And you are done! Continue to the post-install section.
# Post Install
On the first login, polybar and i3 will load successfuly, but nitrogen does not. 

To fix it, Open Nitrogen (via Super+D, from rofi) and click preferences. Add directory for wallpapers (on my setup i put it on ```/usr/share/pixmaps```) and click OK. Select the wallpapers and click apply.

For GTK themes, open lxappearance, under "Widget", select ```Materia-moredark-compact```, for fonts select ```Noto Sans CJK JP Regular```, under "Icon theme" select ```Papirus Dark```, under "Mouse cursor" select ```Volantes Cursors```.

For Qt themes, (i assumed you installed qt5-styleplugins) open ```/etc/environment``` using your favourite text editor and put this lines on the bottom of the text : ```QT_QPA_PLATFORMTHEME=gtk2```

For notifications, run ```xfce4-notifyd-config``` from rofi, and change default position to bottom right.

For LightDM, open/create ```/etc/lightdm/lightdm-gtk-greeter.conf``` with your favourite text editor, remove all stuff inside the file, and paste with this new config :
```
[greeter]
theme-name = Materia-moredark-compact
icon-theme-name = Papirus-Dark
font-name = Noto Sans CJK JP Medium 11
xft-rgba = rgb
xft-hintstyle = hintfull
indicators =
background = /usr/share/pixmaps/main.png
```
Save it and reboot.

# Keybindings
- ```Super + L``` Loackscreen
- ```Super + W``` Terminal
- ```Super + E``` File Manager
- ```Super + D``` Application Menu
- ```Print``` Screenshot
- ```Super + Q``` Quit an app
- ```Super + 1 ... 0``` Switch workspace

For more keybindings, go to ```~/.config/i3/config```

# Special: STFU Mode
This feature is actually from EvanKoe dots and it still used in this dots!

To access it, press ```Super + BackSpace``` key to enter STFU Mode.

Press again ```Super + BackSpace``` key to exit STFU Mode.

On this Mode, pressing :
- ```Ctrl + S``` to shutdown the system.
- ```r``` key to reboot.
- ```l``` key to log out. like as EvanKoe intended to.

# Special: Display Manager (Switcher?)
I don't even know EvanKoe dots had this until i see it under his i3 configs. and of course this thing still being used on this dots.

To access it, press ```Super + P``` to enter this mode.

Press ```Super + P``` again to exit.

On this mode, pressing :
- ```R``` key to extend display to the right side.
- ```L``` key to extend display to the left side.
- ```D``` key to duplicate main display to the second display.
- ```N``` key to disable the second display.

# Special thanks
- [rxyhn](https://github.com/rxyhn) For Picom config files and Rofi custom theme.
- [EvanKoe](https://github.com/EvanKoe) For i3-gaps & alacritty config files.
- [ldy3112](https://github.com/ldy3112) For helping me on polybar stuff and make me stay on i3-gaps.
- [nana-4](https://github.com/nana-4) For the Materia GTK Theme. (dark-compact variant)
- Rectify11 Team for the wallpapers.