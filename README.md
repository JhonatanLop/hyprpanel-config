# hyprpanel

Customizing my Linux with hyprpanel.

## 1. Config file

I'm using Arch Linux with Hyprland. I also use [hyprpanel](https://hyprpanel.com) for a prettier appearance and good customization.<br>
By default, hyprpanel generates an empty file in ~/.config/hyprpanel/. To configure it, you can use the visual tool for customization or write in the file.<br>

My config.json file right now and how it looks:
```json
{
  "bar.customModules.updates.pollingInterval": 1440000,
  "theme.font.size": "1rem",
  "theme.font.name": "Source Code Pro",
  "theme.font.weight": 400,
  "theme.bar.buttons.enableBorders": true,
  "theme.bar.buttons.radius": "10em",
  "menus.clock.weather.enabled": false,
  "menus.clock.time.military": true,
  "menus.dashboard.powermenu.avatar.image": "/home/jhonatan/Pictures/satoru-gojo.jpg",
  "menus.dashboard.shortcuts.left.shortcut1.command": "brave",
  "menus.dashboard.shortcuts.left.shortcut1.tooltip": "Brave",
  "menus.dashboard.shortcuts.left.shortcut3.command": "brave https://discord.com/channels/@me",
  "menus.dashboard.shortcuts.left.shortcut4.icon": "",
  "menus.dashboard.shortcuts.left.shortcut4.command": "steam",
  "menus.dashboard.shortcuts.left.shortcut4.tooltip": "Steam",
  "menus.dashboard.directories.left.directory1.command": "thunar $HOME/Downloads/",
  "menus.dashboard.directories.left.directory2.command": "thunar $HOME/Videos/",
  "menus.dashboard.directories.left.directory3.label": " Git projects",
  "menus.dashboard.directories.left.directory3.command": "thunar $HOME/github",
  "menus.dashboard.directories.right.directory1.command": "thunar $HOME/Documents/",
  "menus.dashboard.directories.right.directory2.command": "thunar $HOME/Pictures/",
  "menus.dashboard.directories.right.directory3.command": "thunar $HOME/",
  "menus.power.lowBatteryNotification": true,
  "bar.customModules.netstat.networkInterface": "cat /proc/net/dev",
  "bar.customModules.netstat.dynamicIcon": true,
  "menus.power.options": {
    "shutdown": "systemctl poweroff",
    "reboot": "systemctl reboot",
    "logout": "hyprctl dispatch exit",
    "suspend": "systemctl suspend"
  },
  "bar.customModules.power.icon": "",
  "bar.customModules.power.onLeftClick": "menu:powerdropdown",
  "bar.customModules.power.tooltip": "Opções de Energia",
  "bar.layouts": {
    "0": {
      "left": [
        "dashboard",
        "workspaces",
        "windowtitle"
      ],
      "middle": [
        "media"
      ],
      "right": [
        "volume",
        "network",
        "bluetooth",
        "battery",
        "systray",
        "clock",
        "notifications",
        "power"
      ]
    },
    "1": {
      "left": [
        "dashboard",
        "workspaces",
        "windowtitle"
      ],
      "middle": [
        "media"
      ],
      "right": [
        "volume",
        "clock",
        "notifications",
        "power"
      ]
    },
    "2": {
      "left": [
        "dashboard",
        "workspaces",
        "windowtitle"
      ],
      "middle": [
        "media"
      ],
      "right": [
        "volume",
        "clock",
        "notifications",
        "power"
      ]
    }
  },
  "wallpaper.image": "/home/jhonatan/Pictures/dark_dune.jpeg",
  "wallpaper.enable": true,
  "bar.clock.format": "%d/%m/%y  %I:%M:%S %p",
  "theme.bar.transparent": true
}
```

![screenshot_2024-12-28_21-43-00](https://github.com/user-attachments/assets/b593d026-cf11-4b18-9356-ec690605a690)

For the power button on top-right, i needed to add it code in the customization tool. `hyprpanel toggleWindow settings-dialog`.<br>
paht: Configuration > Bar > Bar Layouts for Monitors<br>

```json
{
  "0": {
    "left": [
      "dashboard",
      "workspaces",
      "windowtitle"
    ],
    "middle": [
      "media"
    ],
    "right": [
      "volume",
      "network",
      "bluetooth",
      "battery",
      "systray",
      "clock",
      "notifications",
      "power"
    ]
  },
  "1": {
    "left": [
      "dashboard",
      "workspaces",
      "windowtitle"
    ],
    "middle": [
      "media"
    ],
    "right": [
      "volume",
      "clock",
      "notifications",
      "power"
    ]
  },
  "2": {
    "left": [
      "dashboard",
      "workspaces",
      "windowtitle"
    ],
    "middle": [
      "media"
    ],
    "right": [
      "volume",
      "clock",
      "notifications",
      "power"
    ]
  }
}
```
