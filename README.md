# Arch_Installs
These are instructions on how to install arch linux onto an HP Elitebook 8460p and a Macbook Air 13 inch.

**For the HP Elitebook:**
This one is not as well documented because it was my first try. Late nights really did the documentation in. Will need to improve.

1. Boot from USB
2. use fdisk to wipe drive and create Boot, Home, Root, and Swap
3. create filesystems on each partition
4. mount them!
5. install arch base on root
6. grub install!!! on the MBR not the partition ;)
7. Reboot

* So it booted up…
* Installed 
  * video driver for intel (xf86-video-intel)], fbdev driver,
  * allow multilib
  * sudo (omg why is this not already here)
  * xserver or xorg-server w/ xinit
  * alsa for sound
  * i3 and dmenu
  * So \*\*NEED FONT FOR i3 \*\*
  * added repo and installed yaourt
  * got xterm
  * attempting waterfox… nvm let’s get firefox
* Installed 
  * cool-retro-term plus dependencies (q5 stuff)
  * installed vlc
  * Installing more 
    * atom
    * typora
    * libreoffice
    * tmux
    * p7zip unrar tar rsync
    * base-devel
    * xrandr for screen
    * feh for background
    * networkmanager
* Plot twist, get rid of yaourt
* ABS; learn to install from scratch
* working on networking (networking seems good)
* get xev to determine keys
* **need TO DO** 
  * Make it PRETTY get compton DONE
  * notes app DONE (atom or typora)
  * pdf app(evince) not saving.. okular? Yep okular
  * volume (pulseaudio backend). just use CLI for now
  * **bluetooth.. later**
  * new stat bar-\> polybar-\> work DONE (can use work)
  * **multi monitor STARTUP SCRIPTS**
    * \*\*feh --bg-scale --no-xinerama image.png (Assigns image across all monitors)
   \*\*
    * xrandr --output HDMI3 --auto --right-of LVDS1
    * May need udev rule!
  * Screen lock DONE
  * Using chromium for flash DONE
  * Font! DONE
  * new terminal-\> urxvt(nope)-\> maybe but need C/P DONE
  * App manager. meh. DONE
  * **SERVICE SCRIPTS FOR WINDOWS APPS**
  * **mps-youtube**
* Attempting CDM 
  * installing subversion
  * installed from git
  * nvm just gonna auto startx after login
* inversing mouse DID IT
* background 
  * installing feh
  * did it
* networking widget(cool, dmenu)
* auto startx(DONE) 
  * got flameshot for screenshots. added shortcut to i3 config
  * getting discord need libc++ 
    * adding pgp key source because keys are missing.. —skippgpcheck
* edited for background color and no scrollbar in urxv
* got conky
* installed acpi. didn’t need it. Have service file
* Wine? wine-staging installed... that was easy. so wine [exe file] and it kinda just works.
* installing bluez and bluez-utils
* installing cups common and for UFRII
* warhammer dawn of war? satellite reign? dead cells? ..vagante? Heavy Bullets. ronin.
* let’s try getting laptop-mode-tools.. removed. that’s just power stuff
* got xorg-xev for keys and xorg-xbacklight
* autofs to auto mount that stuffs
* installing ssh because... cmon man
* openresolv!! DNS is beyond the scope of oVPN
* .. sigh networkmanager-openvpn
* unzip/ zip
* So the VPN script worked, added the lines to the .ovpn
* alsa 32 bit drivers for wine sound
* more libraries for dead cells
* autofs scripts.. udisk.. devmon and exfat-utils. Got it working
* still working on blues alsa
* bluetooth is cool i think. setting to auto
  * adjusted /etc/pulse/default.pa
  * /etc/bluetooth/main.conf
  * enabled trusted device
* using mps-youtube, getting mplayer
* set a2dp_sink for headset (clear audio)

THINGS TO DO
* Setup scripts for zabbix
* Service for winapps
* auto start bluetooth 
* mps-youtube DONE
* multi-monitor

  mailpile :) needed pypgpdump
  
  
  
  
**This is for the Mac**
Sadly I did not include the installation part, but I was able to install it with an encrypted drive. 
Will need to work to include that.

So far only used modprobe-wl-dkms to get wifi driver. just base, vim, and base devel.

* Back-end
  * installed the intel video driver
  * added sudo user! wheel and stuff
  * openresolv. openvpn-update-resolv-conf-git
  * netcat
  * installed git
  * tmux
  * udevil for devmon mounting
  * fuse-exfat for exfat
  * moved xinitrc, Xdefaults, i3 config
  * xbacklight
  * let's try the mac touchpad driver.. ohhh noooo
  * replaced with xf86-input-ssynaptics
  * configuring touchpad
  * lib32-alsa-lib, lib32-alsa-plugins for wine audio
  * let's get some bluetooth audio! bluez and bluez-utils
  * bluez-alsa-git. sound is choppy.. not sure
  * mplayer! mps-youtube
  * pavucontrol.. make life easier



* UI/ease of use
  * installed i3 group packages
  * installed xorg-xinit
  * installing xorg-server
  * dmenu!
  * chromium
  * pepper-flash for chromium
  * vlc
  * p7zip, unrar, tar, rsync
  * networkmanager, wpa_supp for backup (enable networkmanager)
  * networkmanager-openvpn
  * feh
  * starting with xterm
  * getting noto-emoji
  * getting polybar and conky
  * ef it, got dejavu font
  * dmenu netman
  * installing compton
  * pulseaudio-bluetooth
  * alsa-utils (also is kernel level)
  * discord, libc++ --skippgpcheck
  * flameshot,  libreoffice and other ABS
  * set autostart for devmon, i3lock, get cupsd
  * also getting some fonts
  * got cups. working on drivers. common, then cndrvcups-lb
  * wine-staging
  * got okular and pixeluvo
  * lidlock.service! not working..
  * got gimp instead..
  * mailpile. python2-pgp needed
  * tps. powertop

