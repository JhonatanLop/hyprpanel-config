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
  "menus.dashboard.directories.left.directory1.command": "hyprctl dispatch exec \"kitty -e ranger ~/Downloads\"",
  "menus.dashboard.directories.left.directory2.command": "hyprctl dispatch exec \"kitty -e ranger ~/Videos\"",
  "menus.dashboard.directories.left.directory3.label": " Git projects",
  "menus.dashboard.directories.left.directory3.command": "hyprctl dispatch exec \"kitty -e ranger ~/github\"",
  "menus.dashboard.directories.right.directory1.command": "hyprctl dispatch exec \"kitty -e ranger ~/Documents\"",
  "menus.dashboard.directories.right.directory2.command": "hyprctl dispatch exec \"kitty -e ranger ~/Pictures\"",
  "menus.dashboard.directories.right.directory3.command": "hyprctl dispatch exec \"kitty -e ranger ~/\"",
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
        "cpu",
        "ram",
        "updates",
        "hyprsunset"
      ],
      "middle": [
        "media"
      ],
      "right": [
        "volume",
        "network",
        "bluetooth",
        "battery",
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
  "bar.clock.format": "%d/%m/%y  %I:%M %p",
  "theme.bar.transparent": true,
  "bar.bluetooth.label": true,
  "bar.customModules.updates.autoHide": false,
  "bar.workspaces.showAllActive": true,
  "theme.bar.buttons.workspaces.smartHighlight": true,
  "bar.windowtitle.truncation_size": 44,
  "bar.customModules.updates.rightClick": "",
  "bar.customModules.storage.labelType": "used",
  "bar.customModules.ram.labelType": "used",
  "bar.customModules.updates.leftClick": "kitty --hold -e yay -Syu",
  "menus.transitionTime": 200,
  "menus.transition": "crossfade",
  "scalingPriority": "hyprland",
  "menus.clock.weather.location": "São José dos Campos",
  "menus.clock.weather.unit": "metric",
  "theme.bar.menus.menu.volume.scaling": 100,
  "hyprpanel.restartAgs": false,
  "bar.launcher.autoDetectIcon": true,
  "menus.power.showLabel": true,
  "menus.power.confirmation": false,
  "theme.bar.floating": false,
  "bar.autoHide": "never",
  "theme.bar.outer_spacing": "1em",
  "theme.bar.buttons.y_margins": "0.4em",
  "theme.bar.layer": "top",
  "theme.bar.buttons.padding_x": "0.7rem",
  "bar.launcher.rightClick": "alacritty -e fish",
  "bar.customModules.hyprsunset.temperature": "3000k"
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
