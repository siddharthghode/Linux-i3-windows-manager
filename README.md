```bash
"These are Just some files to use them properly" — because obviously, that clarifies everything — and you'll need to dig deep into your itty-bitty, microscopic, imaginary particles of a brain... that is, if you’re lucky enough to have any at all.
```

# 🪟 i3 Window Manager Config
Personal i3wm configuration — minimal, keyboard-driven, dual-monitor ready(important if you are getting problems while switching screens).

## ✨ Features

- **Mod key**: Super (Win)
- **Terminal**: Alacritty
- **Launcher**: dmenu
- **Bar**: py3status
- **Wallpaper**: feh
- **Display management**: autorandr + custom `display-manager.sh`
- **Lock screen**: i3lock (Mod+F4)
- **Natural scrolling**: xinput
- **Volume**: pactl (F5/F6/F7 + media keys)
- **Brightness**: brightnessctl

## 📦 Dependencies
```bash
sudo apt install i3 alacritty dmenu py3status feh autorandr brightnessctl i3lock xss-lock dex
```
## 🚀 Install
```bash
git clone https://github.com/siddharthghode/Linux-i3-windows-manager.git
cp config ~/.config/i3/config
cp display-manager.sh ~/.config/i3/display-manager.sh
chmod +x ~/.config/i3/display-manager.sh
```

⚠️ First Launch — Set Your Mod Key

Before starting i3, open ~/.config/i3/config and confirm the mod key:
bashset $mod Mod4   # Mod4 = Super/Win key  |  Mod1 = Alt key
Change Mod4 → Mod1 if you prefer Alt. Wrong mod = no keybinds work.

**Fix before use:**
- Replace `<device-id>` in `xinput` line with your actual touchpad ID
- Run `xinput list` to find it
- Update wallpaper path to your own image

## ⌨️ Key Bindings  (these are the main ones look carefully with two buttons)
| Keys | Action |
|------|--------|
| `Mod+Enter` | Open terminal |
| `Mod+d` | dmenu launcher |
| `Mod+q` | Kill window |
| `Mod+F4` | Lock screen |
| `Mod+f` | Fullscreen toggle |
| `Mod+h/v` | Split horizontal/vertical |
| `Mod+s/w/e` | Stacking/tabbed/split layout |
| `Mod+Shift+Space` | Float toggle |
| `Mod+r` | Resize mode |
| `Mod+1–0` | Switch workspace |
| `Mod+Shift+1–0` | Move to workspace |
| `Mod+Shift+c` | Reload config |
| `Mod+Shift+r` | Restart i3 |

## 📁 Structure
```
~/.config/i3/
├── config              # Main i3 config
└── display-manager.sh  # Auto display hotplug script
```

## 🖥️ Multi-Monitor
Uses `autorandr` for auto profile switching + custom `display-manager.sh` for hotplug handling via udev.
---

*Built on i3 v4.x | Tested on Ubuntu/Debian*

