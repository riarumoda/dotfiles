![banner](https://github.com/Putu-Justine/dotfiles/blob/master/.github-assets/banner/main.png)
# What's this?
This is my personal config files for i3-gaps. Based on EvanKoe & rxyhn dotfiles.
# Purpose of this rice
I actually used rxyhn dots before, and i like it. but his awesome modules spawned on the second monitor if i plug a second monitor to my laptop and got annoyed by it. After some researching, i3 does not do this and used EvanKoe dots on it (2022 one). But my head went "Frick it. Combine both of them." And this dots born.
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