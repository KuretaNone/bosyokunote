---
id: Window Terminalをカスタマイズしよう
aliases:
  - Window Terminalをカスタマイズしよう
tags: []
created: 2025-10-16
updated: 2025-10-16
---
# Window Terminalをカスタマイズしよう

[モテるターミナルにカスタマイズしよう（WezTerm）](https://zenn.dev/mozumasu/articles/mozumasu-wezterm-customization) を読んで

[[Windows Terminal]]でもそういうことをしたいなぁと思ったので、設定します。

## 最終成果物

```json
{
    "$help": "https://aka.ms/terminal-documentation",
    "$schema": "https://aka.ms/terminal-profiles-schema",
    "actions": 
    [
        {
            "command": 
            {
                "action": "copy",
                "singleLine": false
            },
            "id": "User.copy.644BA8F2"
        },
        {
            "command": "paste",
            "id": "User.paste"
        },
        {
            "command": "find",
            "id": "User.find"
        },
        {
            "command": 
            {
                "action": "splitPane",
                "split": "auto",
                "splitMode": "duplicate"
            },
            "id": "User.splitPane.A6751878"
        },
        {
            "command": "markMode",
            "id": "User.markMode"
        }
    ],
    "alwaysShowNotificationIcon": false,
    "alwaysShowTabs": true,
    "copyFormatting": "html",
    "copyOnSelect": false,
    "defaultProfile": "{574e775e-4f2a-5b96-ac1e-a2962a402336}",
    "disableAnimations": false,
    "focusFollowMouse": false,
    "keybindings": 
    [
        {
            "id": "User.copy.644BA8F2",
            "keys": "ctrl+c"
        },
        {
            "id": "User.paste",
            "keys": "ctrl+v"
        },
        {
            "id": "User.find",
            "keys": "ctrl+shift+f"
        },
        {
            "id": "User.markMode",
            "keys": "ctrl+shift+space"
        },
        {
            "id": "User.splitPane.A6751878",
            "keys": "alt+shift+d"
        }
    ],
    "newTabMenu": 
    [
        {
            "type": "remainingProfiles"
        }
    ],
    "profiles": 
    {
        "defaults": 
        {
            "font": 
            {
                "face": "HackGen Console NF"
            },
            "opacity": 60,
            "padding": "1",
            "rightClickContextMenu": false,
            "scrollbarState": "hidden",
            "startingDirectory": ".",
            "useAcrylic": true
        },
        "list": 
        [
            {
                "commandline": "%SystemRoot%\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
                "font": 
                {
                    "face": "HackGen Console NF"
                },
                "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
                "hidden": false,
                "name": "Windows PowerShell"
            },
            {
                "colorScheme": "One Half Dark",
                "commandline": "%SystemRoot%\\System32\\cmd.exe",
                "font": 
                {
                    "face": "HackGen Console NF"
                },
                "guid": "{0caa0dad-35be-5f56-a8ff-afceeeaa6101}",
                "hidden": false,
                "name": "\u30b3\u30de\u30f3\u30c9 \u30d7\u30ed\u30f3\u30d7\u30c8"
            },
            {
                "guid": "{b453ae62-4e3d-5e58-b989-0a998ec441b8}",
                "hidden": false,
                "name": "Azure Cloud Shell",
                "source": "Windows.Terminal.Azure"
            },
            {
                "guid": "{f00e9259-53c8-58ee-9f53-0bd9c324dc75}",
                "hidden": false,
                "name": "Developer Command Prompt for VS 2022",
                "source": "Windows.Terminal.VisualStudio"
            },
            {
                "guid": "{d1e123ca-bb57-5b43-867e-7d7e5d20cb7f}",
                "hidden": false,
                "name": "Developer PowerShell for VS 2022",
                "source": "Windows.Terminal.VisualStudio"
            },
            {
                "colorScheme": "One Half Dark",
                "font": 
                {
                    "face": "HackGen Console NF"
                },
                "guid": "{16208362-94fc-5b1f-a491-5b2624d5ab56}",
                "hidden": true,
                "name": "Visual Studio Debug Console",
                "source": "VSDebugConsole"
            },
            {
                "colorScheme": "One Half Dark",
                "font": 
                {
                    "face": "HackGen Console NF"
                },
                "guid": "{574e775e-4f2a-5b96-ac1e-a2962a402336}",
                "hidden": false,
                "name": "PowerShell",
                "opacity": 70,
                "source": "Windows.Terminal.PowershellCore"
            },
            {
                "backgroundImage": "desktopWallpaper",
                "backgroundImageOpacity": 0.75,
                "colorScheme": "One Half Dark",
                "font": 
                {
                    "face": "HackGen Console NF",
                    "size": 12
                },
                "guid": "{e8da1cd2-783b-56ba-9271-0b541eed65a4}",
                "hidden": false,
                "name": "Ubuntu",
                "opacity": 70,
                "source": "Microsoft.WSL"
            }
        ]
    },
    "schemes": [],
    "showTabsInTitlebar": true,
    "tabWidthMode": "titleLength",
    "theme": "dark no close button",
    "themes": 
    [
        {
            "name": "dark no close button",
            "tab": 
            {
                "background": "terminalBackground",
                "iconStyle": "default",
                "showCloseButton": "never",
                "unfocusedBackground": "#00000000"
            },
            "tabRow": 
            {
                "background": null,
                "unfocusedBackground": "#333333FF"
            },
            "window": 
            {
                "applicationTheme": "dark",
                "experimental.rainbowFrame": false,
                "frame": null,
                "unfocusedFrame": null,
                "useMica": false
            }
        }
    ],
    "trimBlockSelection": true,
    "useAcrylicInTabRow": true
}
```

