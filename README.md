What I need to do after installing Arch Linux:
  Setting up Wi-Fi:
    1. pacman -S wpa_supplicant netctl dhdpcd dialog ppp 
    2. wifi-menu, connecting to Wi-Fi
    3. ip link set wlp7s0 down
       netctl start wlp7s0-network_name
       wpa_cli status

  Install xorg, wm and other stuff
  pacman -S xorg xorg-xinit xorg-server bspwm sxhkd polybar ttf-jetbrains-mono alacritty nvim picom git pavucontrol pulseaudio sxiv rofi ranger

  Add sxhkd & exec bspwm to  ~/.xinitrc or install dm like sddm, don't forget to enable dm service 

  Configure bspwm & sxhkd:
  mkdir ~/.config/bspwm
  mkdir ~/.config/sxhkd
  cp /usr/share/doc/bspwm/examples/bspwmrc ~/.config/bspwm/
  cp /usr/share/doc/bspwm/examples/sxhkdrc ~/.config/sxhkd/

  Setting up AUR:
  git clone https://aur.archlinux.org/yay-git.git
  cd yay
  makepkg -si

  Setting up double monitors:
  xrandr --output HDMI-1 --auto --left-of DP-2

  Add second keyboard layout:
  setxkbmap -option grp:alt_shift_toggle us,ru

  Add background:
  feh --bg-fill ~/backgrounds/background.jpg

  Configure Alacritty:
  mkdir ~/.config/alacritty
  touch ~/.config/alacritty/alacritty.yml
  
  window:
    padding:
      x: 10
      y: 10
    opacity: 0.8
  font:
    normal:
      family: Jetbrains Mono
      style: Regular
    size: 12

	
  Configure picom:
  mkdir ~/.config/picom
  cp /etc/xdg/picom/conf ~/.config/picom

  don't forget to enable picom autoexec

  Increase saturation:
  yay -S vibrant-cli
  vibrant-cli HDMI-1 1.45
  vibrant-cli DP-2 1.45

~
~
~
~


