---
id: 20250217-asahi-linux
aliases:
  - asahi-linux
tags: []
---

# asahi-linux

[(51) Asahi Lina / 朝日リナ - YouTube](https://www.youtube.com/@AsahiLina/featured)

---

[[20250215-hypr-fedora-key|hypr-fedora-key]]
[“csinc”, the AArch64 instruction you didn’t know you wanted – Experimental chill](https://danlark.org/2023/06/06/csinc-the-arm-instruction-you-didnt-know-you-wanted/)
[“csinc”, the AArch64 instruction you didn’t know you wanted Hacker News](https://news.ycombinator.com/item?id=36223283)
[GitHub - ibhagwanfzf-lua Improved fzf.vim written in lua](https://github.com/ibhagwan/fzf-lua)

---

[Asahi Linux - krun + FEX + Steam · GitHub](https://gist.github.com/teohhanhui/042a395010d9946ceee14768736e3780#create-distrobox-container)
[From the diary of AArch64 porter — drive-by coding – Marcin Juszkiewicz](https://marcin.juszkiewicz.com.pl/2020/09/16/from-the-diary-of-aarch64-porter-drive-by-coding/)

swaylock -> work fine in here

# sway active window screenshot

```bash
grim -g "$(swaymsg -t get_tree | jq -r '.. | select(.focused?) | .rect | "\(.x),\(.y) \(.width)x\(.height)"')" - | pngquant --quality=65-80 - | wl-copy -t image/png
```

# making mpv work :D

- sudo dnf install libavcodec-freeworld

---

sudo dnf swap ffmpeg-free ffmpeg --allowerasing

[Howto/Multimedia - RPM Fusion](https://rpmfusion.org/Howto/Multimedia)

---

# keyboard switching like other linux laptop:

I'm not sure why they set the default layout to be this way (fn/ctrl/meta/alt) it doesn't match up with the functionality of mac nor the convention of windows. The devs probably had a reason but I'm not aware of it.

This should be a quick and simple guide, it should take about 5 mins to do everything since this is just copy-pasting commands. I just didn't see any single guide/post online explaining ALL of this so I thought I'd write something real quick to explain all of the reformatting in 1 place, written specifically for asahi fedora.
Part 1/2: Swap fn and ctrl
Method 1:

Not sure if this method works reliably, please let me know your results.

    sudo grubby --update-kernel=ALL --args="hid_apple.swap_fn_leftctrl=1" Just passes this option as a boot parameter into grub.
    reboot

Method 2:

Courtesy of the Arch wiki

    sudo -i Log into root shell
    (Optional) echo 1 > /sys/bus/hid/drivers/apple/module/parameters/swap_fn_leftctrl Temporarily swaps fn and ctrl until next boot
    sudo nano /etc/modprobe.d/hid_apple.conf make a new empty config file at the right spot
    ctrl+shift+v and paste options hid_apple swap_fn_leftctrl=1 to paste in the config option. Then do ctrl+s and ctrl+x to save and exit.
    sudo dracut --regenerate-all --force - This is the part that was missing from the guides I checked. Arch wiki uses arch-specific tools, which aren't available on asahi fedora. This should regenerate the initramfs and make the option stick on the next reboot.

Part 2/2: Swap alt and meta

Courtesy of kind asahi fourms post.

    echo "1" > /sys/module/hid_apple/parameters/swap_opt_cmd Same as before. Temporarily changes the setting to swap opt and cmd keys.
    grubby --update-kernel=ALL --args="hid_apple.swap_opt_cmd=1" Sets this change to be permanent on reboot (works on grub only).

Ahhhhhh, much better. Should be pretty easy to do! That's pretty much all you need to do to make the configuration just like in most linux-laptops! :D also if u have a new boot make sure to run sudo widevine-installer just to be able to use DRM content. Hope all of this helps! If I get anything wrong please let me know so I can fix it.

---

# great sway config with picture available

```bash
# Default config for sway
#
# Copy this to ~/.config/sway/config and edit it to your liking.
#
# Read `man 5 sway` for a complete reference.

font pango: Maple Mono Normal NF CN 0.001
# make window bar disapper
# default_border none
# default_floating_border none
titlebar_padding 1
titlebar_border_thickness 0
### Variables
#
# Logo key. Use Mod1 for Alt.
# font pango: Maple Mono Normal NF CN
set $mod Mod4
# Home row direction keys, like vim
set $left h
set $down j
set $up k
set $right l
# Your preferred terminal emulator
set $term kitty
# Your preferred application launcher
# set $menu wmenu-run
set $menu rofi -show run

### Output configuration
#
# Default wallpaper (more resolutions are available in /usr/share/backgrounds/sway/)
# output * bg /usr/share/backgrounds/sway/Sway_Wallpaper_Blue_1920x1080.png fill
output * bg /home/peter/Pictures/wallpapers/Lofi - Chill Room2.jpeg fill
#
# Example configuration:
#
#   output HDMI-A-1 resolution 1920x1080 position 1920,0
#
# You can get the names of your outputs by running: swaymsg -t get_outputs

### Idle configuration
#
# Example configuration:
#
# exec swayidle -w \
#          timeout 300 'swaylock -f -c 000000' \
#          timeout 600 'swaymsg "output * power off"' resume 'swaymsg "output * power on"' \
#          before-sleep 'swaylock -f -c 000000'
#
# This will lock your screen after 300 seconds of inactivity, then turn off
# your displays after another 300 seconds, and turn your screens back on when
# resumed. It will also lock your screen before your computer goes to sleep.

### Input configuration
#
# Example configuration:
#
#   input "2:14:SynPS/2_Synaptics_TouchPad" {
#       dwt enabled
#       tap enabled
#       natural_scroll enabled
#       middle_emulation enabled
#   }
input type:touchpad {
    # tap enabled
    natural_scroll enabled
}

#
input "type:keyboard" xkb_options caps:escape
input "type:keyboard" repeat_delay 300
input "type:keyboard" repeat_rate 50
# You can get the names of your inputs by running: swaymsg -t get_inputs
# Read `man 5 sway-input` for more information about this section.
#

# monitor setup:
workspace 1 output HDMI-A-1
workspace 2 output HDMI-A-1
workspace 3 output HDMI-A-1
workspace 4 output HDMI-A-1
workspace 5 output HDMI-A-1
workspace 6 output HDMI-A-1
workspace 7 output HDMI-A-1
workspace 8 output HDMI-A-1
workspace 9 output eDP-1

# cliphist:
exec wl-paste --type text --watch cliphist store
exec wl-paste --type image --watch cliphist store

bindsym $mod+Alt+v exec ~/.config/sway/ClipManager.sh
# Screenshot bindings
bindsym Alt+Shift+3 exec ~/.local/bin/swayshot
bindsym $mod+c exec ~/.local/bin/ocrmypic
bindsym Alt+Shift+4 exec ~/.local/bin/macpic

### Key bindings
#
# Basics:
#
    # Start a terminal
    bindsym $mod+Return exec $term

    # Kill focused window
    bindsym $mod+q kill

    # Start your launcher
    bindsym $mod+d exec $menu

    # Drag floating windows by holding down $mod and left mouse button.
    # Resize them with right mouse button + $mod.
    # Despite the name, also works for non-floating windows.
    # Change normal to inverse to use left mouse button for resizing and right
    # mouse button for dragging.
    floating_modifier $mod normal

    # Reload the configuration file
    bindsym $mod+Shift+c reload

    # Exit sway (logs you out of your Wayland session)
    bindsym $mod+Shift+e exec swaynag -t warning -m 'You pressed the exit shortcut. Do you really want to exit sway? This will end your Wayland session.' -B 'Yes, exit sway' 'swaymsg exit'
#
# Moving around:
#
    # Move your focus around
    bindsym $mod+$left focus left
    bindsym $mod+$down focus down
    bindsym $mod+$up focus up
    bindsym $mod+$right focus right
    # Or use $mod+[up|down|left|right]
    bindsym $mod+Left focus left
    bindsym $mod+Down focus down
    bindsym $mod+Up focus up
    bindsym $mod+Right focus right

    # Move the focused window with the same, but add Shift
    bindsym $mod+Shift+$left move left
    bindsym $mod+Shift+$down move down
    bindsym $mod+Shift+$up move up
    bindsym $mod+Shift+$right move right
    # Ditto, with arrow keys
    bindsym $mod+Shift+Left move left
    bindsym $mod+Shift+Down move down
    bindsym $mod+Shift+Up move up
    bindsym $mod+Shift+Right move right
#
# Workspaces:
#
    # Switch to workspace
    bindsym $mod+1 workspace number 1
    bindsym $mod+2 workspace number 2
    bindsym $mod+3 workspace number 3
    bindsym $mod+4 workspace number 4
    bindsym $mod+5 workspace number 5
    bindsym $mod+6 workspace number 6
    bindsym $mod+7 workspace number 7
    bindsym $mod+8 workspace number 8
    bindsym $mod+9 workspace number 9
    bindsym $mod+0 workspace number 10
    # Move focused container to workspace
    bindsym $mod+Shift+1 move container to workspace number 1
    bindsym $mod+Shift+2 move container to workspace number 2
    bindsym $mod+Shift+3 move container to workspace number 3
    bindsym $mod+Shift+4 move container to workspace number 4
    bindsym $mod+Shift+5 move container to workspace number 5
    bindsym $mod+Shift+6 move container to workspace number 6
    bindsym $mod+Shift+7 move container to workspace number 7
    bindsym $mod+Shift+8 move container to workspace number 8
    bindsym $mod+Shift+9 move container to workspace number 9
    bindsym $mod+Shift+0 move container to workspace number 10
    # Note: workspaces can have any name you want, not just numbers.
    # We just use 1-10 as the default.
#
# Layout stuff:
#
    # You can "split" the current object of your focus with
    # $mod+b or $mod+v, for horizontal and vertical splits
    # respectively.
    bindsym $mod+b splith
    bindsym $mod+v splitv

    # Switch the current container between different layout styles
    bindsym $mod+s layout stacking
    bindsym $mod+w layout tabbed
    bindsym $mod+e layout toggle split

    # Make the current focus fullscreen
    bindsym $mod+f fullscreen

    # Toggle the current focus between tiling and floating mode
    bindsym $mod+Shift+space floating toggle

    # Swap focus between the tiling area and the floating area
    bindsym $mod+space focus mode_toggle

    # Move focus to the parent container
    bindsym $mod+a focus parent
#
# Scratchpad:
#
    # Sway has a "scratchpad", which is a bag of holding for windows.
    # You can send windows there and get them back later.

    # Move the currently focused window to the scratchpad
    bindsym $mod+Shift+minus move scratchpad

    # Show the next scratchpad window or hide the focused scratchpad window.
    # If there are multiple scratchpad windows, this command cycles through them.
    bindsym $mod+minus scratchpad show
#
# Resizing containers:
#
mode "resize" {
    # left will shrink the containers width
    # right will grow the containers width
    # up will shrink the containers height
    # down will grow the containers height
    bindsym $left resize shrink width 10px
    bindsym $down resize grow height 10px
    bindsym $up resize shrink height 10px
    bindsym $right resize grow width 10px

    # Ditto, with arrow keys
    bindsym Left resize shrink width 10px
    bindsym Down resize grow height 10px
    bindsym Up resize shrink height 10px
    bindsym Right resize grow width 10px

    # Return to default mode
    bindsym Return mode "default"
    bindsym Escape mode "default"
}
bindsym $mod+r mode "resize"
#
# Utilities:
#
    # Special keys to adjust volume via PulseAudio
    bindsym --locked XF86AudioMute exec pactl set-sink-mute \@DEFAULT_SINK@ toggle
    bindsym --locked XF86AudioLowerVolume exec pactl set-sink-volume \@DEFAULT_SINK@ -5%
    bindsym --locked XF86AudioRaiseVolume exec pactl set-sink-volume \@DEFAULT_SINK@ +5%
    bindsym --locked XF86AudioMicMute exec pactl set-source-mute \@DEFAULT_SOURCE@ toggle
    # Special keys to adjust brightness via brightnessctl
    bindsym --locked XF86MonBrightnessDown exec brightnessctl set 5%-
    bindsym --locked XF86MonBrightnessUp exec brightnessctl set 5%+
    # Special key to take a screenshot with grim
    bindsym Print exec grim
#
# Status Bar:
#
# Read `man 5 sway-bar` for more information about this section.
bar {
    position top
    swaybar_command waybar
    # swaybar_command i3status

    # When the status_command prints a new line to stdout, swaybar updates.
    # The default just shows the current date and time.
    # status_command while date +'%Y-%m-%d %X'; do sleep 1; done
    #
     colors {
         statusline #ffffff
         background #323232
         inactive_workspace #32323200 #32323200 #5c5c5c
    }
}

include /etc/sway/config.d/*

```

---

# chrome with 16k and netflix

```bash
[The Quest for Netflix on Asahi Linux | Blog](https://www.da.vidbuchanan.co.uk/blog/netflix-on-asahi.html)
```

[NixOS Server on M1 Mac Mini – @heywoodlh – heywoodlh thoughts](https://heywoodlh.io/nixos-mac-mini)

- another great resource of ashai linux (NixOS)

---

# typora linux (arm)

[Typora — macOS release channel](https://typora.io/releases/all)

[Overview - rpms/alien - src.fedoraproject.org](https://src.fedoraproject.org/rpms/alien)
use alien to convert deb -> to rpm :
rpm2cpio typora-1.10.6-2.arm64.rpm | cpio -idmv
extract that thing manually

- Move the files to appropriate locations (e.g., /usr/local/bin for the binary, /usr/local/share for data).
- Avoid overwriting system directories like /usr/share.

- can use alien to convert deb file to rpm

```desktop
[Desktop Entry]
Name=Typora
Comment=a minimal Markdown reading & writing app. Change Log: (https://typora.io/releases/all)
GenericName=Markdown Editor
Exec=typora %U
Icon=typora
Type=Application
StartupNotify=true
Categories=Office;WordProcessor;
MimeType=text/markdown;text/x-markdown;

```

---

# using android tools:

[GitHub - lzhiyong/android-sdk-tools: building android-sdk tools for Android](https://github.com/lzhiyong/android-sdk-tools)

aarch64 -> android packages
