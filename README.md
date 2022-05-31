![banner](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/banner/main.png)
# What's this?
This is my personal config files for i3-gaps. Based on EvanKoe & rxyhn dotfiles.
# Purpose of this rice
I actually used rxyhn dots before, and i like it. but his awesome modules spawned on the second monitor if i plug a second monitor to my laptop and got annoyed by it. After some researching, i3 does not do this and used EvanKoe dots on it (2022 one). But my head went "Frick it. Combine both of them." And this dots born.
# Status of this rice
i3-gaps : ✅

alacritty : ✅

polybar : ✅

picom : ✅

rofi : ✅

GTK2 Theming : 🚸 (Buggy, mainly used to translate GTK theme to Qt Only.)

GTK3 Theming : ✅

GTK4 Theming : ✅

QT5 Theming : 🚸 (See GTK2 Theming.)

# Screenshots
Desktop
![desktop](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/screenshots/desktop.png)

Rofi Menu
![rofi](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/screenshots/rofi.png)

Alacritty and PCManFM (GTK3)
![alacritty](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/screenshots/alacritty-and-gtk-apps.png)

Audacious (QT5)
![audacious](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/screenshots/qt-apps.png)

# Installation (Arch Linux Only, fresh install)
Install the deps first :
```
i3-gaps nitrogen xfce4-notifyd brightnessctl dex light-locker alacritty pcmanfm-gtk3 lxtask-gtk3 scrot rofi dmenu lxappearance-gtk3 lightdm lightdm-gtk-greeter noto-fonts noto-fonts-cjk noto-fonts-emoji noto-fonts-extra ttf-font-awesome gtk-engine-murrine polybar papirus-icon-theme
```
Optional but recommended :
```
arandr gpicview l3afpad
```
Then from AUR :
```
picom-git polkit-dumb-agent-git volantes-cursors
```
Optional but recommended from AUR :
```
uwufetch qt5-styleplugins gtk3-classic cava
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
