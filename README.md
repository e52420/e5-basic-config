# post-install-arch-basic-setup

# Basic system utilities


## Programs

```bash
sudo pacman -S pulseaudio pavucontrol libnotify notification-daemon udiskie ntfs-3g volumeicon glib2 gvfs picom lxappearance nitrogen lxsession neovim rofi ranger thunar trayer vlc kvantum-qt5 libmtp simple-mtpfs kdenlive obs-studio discord ttf-dejavu ttf-liberation noto-fonts
```

## Xprofile

Now you can use *~/.xprofile* to run programs before your window manager starts:

```bash
touch ~/.xprofile
```

```bash
setxkbmap es &
nm-applet &
udiskie -t &
nitrogen --restore &
lxsession &
```



## Notifications

```bash
sudo pacman -S libnotify notification-daemon
```

```bash
# Create this file with nano or vim
sudo nvim /usr/share/dbus-1/services/org.freedesktop.Notifications.service
# Paste these lines
[D-BUS Service]
Name=org.freedesktop.Notifications
Exec=/usr/lib/notification-daemon-1.0/notification-daemon
```

Test it like so:

```bash
notify-send "Hello World"
```

