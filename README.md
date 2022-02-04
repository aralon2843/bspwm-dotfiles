# What I need to do after installing Arch Linux:
  ## Setting up Wi-Fi:
    $ sudo pacman -S wpa_supplicant netctl dhdpcd dialog ppp 
    $ wifi-menu
    $ ip link set wlp7s0 down
    $ netctl start wlp7s0-network_name
    $ wpa_cli status
    
  ## Install xorg, wm and other stuff:
    pacman -S xorg xorg-xinit xorg-server bspwm sxhkd polybar ttf-jetbrains-mono alacritty nvim picom git pavucontrol pulseaudio sxiv rofi ranger feh lxappearance xfce4-screenshooter

  ## Add sxhkd & exec bspwm to  ~/.xinitrc or install dm like sddm, don't forget to enable dm service 

  ## Configure bspwm & sxhkd:
    $ mkdir ~/.config/bspwm
    $ mkdir ~/.config/sxhkd
    $ cp /usr/share/doc/bspwm/examples/bspwmrc ~/.config/bspwm/
    $ cp /usr/share/doc/bspwm/examples/sxhkdrc ~/.config/sxhkd/

  ## Setting up AUR:
    $ git clone https://aur.archlinux.org/yay-git.git
    $ cd yay
    $ makepkg -si

  ## Setting up double monitors:
    $ xrandr --output HDMI-1 --auto --left-of DP-2

  ## Add second keyboard layout:
    $ setxkbmap -option grp:alt_shift_toggle us,ru

  ## Add background:
    $ feh --bg-fill ~/backgrounds/background.jpg

  ## Configure Alacritty:
    $ mkdir ~/.config/alacritty
    $ touch ~/.config/alacritty/alacritty.yml

  ## Configure picom:
    $ mkdir ~/.config/picom
    $ cp /etc/xdg/picom/conf ~/.config/picom

    Don't forget to enable picom autoexec

  ## Increase saturation:
    $ yay -S vibrant-cli
    $ vibrant-cli HDMI-1 1.45
    $ vibrant-cli DP-2 1.45
  
  ## Making fonts better:
    Everything is well explained in this article - https://wiki.manjaro.org/index.php?title=Improve_Font_Rendering
