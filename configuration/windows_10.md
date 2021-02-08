## Introduction
This document contains my personal configuration for Windows 10 based with Razer Blade 15 2018 laptop.

## Table of Content
* [General Setting](#general-setting)
* [Install Essential Applications](#install-essential-applications)
* [Install Font](#install-font)
* [Gaming](#gaming)
* [Set Up Windows Subsystem for Linux 2](#set-up-windows-subsystem-for-linux-2)

## General Setting
<sub>[Back to Top](#introduction)</sub>
* Configure Sound Card
```bash
# Realtek Audio Console -> Device advanced settings -> Playback Device -> Make internal and external output devices playback two different audio streams simultaneously
```
* Display Scaling
```bash
# Windows Setting -> System -> Display -> Scale and Layout -> Advanced scaling settings -> 110%
```
* Enable Clipboard
```bash
# Windows Setting -> System -> Clipboard -> Clipboard history -> On
```
* Enable Dark Mode
```bash
# Windows Setting -> Personalization -> Colors -> Choose your color -> Dark
```

* Configure Start
```bash
# Windows Setting -> Personalization -> Start
    # Show more tiles on Start (Off)
    # Show app list in Start menu (On)
    # Show recent added apps (Off)
    # Show most used apps (Off)
    # Show suggestions occasionally in Start (Off)
    # Use Start full screen (On)
    # Show recently opened items in Jump Lists on Start or the taskbar and in File Explorer Quick Access (Off)
```

* Configure Taskbar
```bash
# Windows Setting -> Personalization -> Taskbar
    # Lock the taskbar (On)
    # Automatically hide the taskbar in desktop mode (Off)
    # Automatically hide the taskbar in tablet mode (On)
    # Use small taskbar buttons (Off)
    # Show Peek to preview the desktop when you move your mouse to the Show desktop button at the end of the taskbar (On)
    # Replace Command Prompt with PowerShell in the menu when I right-click the start button or press Windows key+X (On)
    # Show badges on taskbar buttons (On)
```

* Configure Privacy
```bash
# Windows Setting -> Privacy -> Activity history
    # Store my activity history on this device (Off)
    # Send my activity hihstory to Microsoft (Off)
    # Show activities from these accounts (Off)
```

* Change Cursor
```
# Download Entis Cursor from https://www.deviantart.com/zhorak/art/Entis-Cursors-58265625
# Extract the file, right click on install.inf, select install
# Windows Setting -> Devices -> Mouse -> Additional mouse options -> pointers -> Scheme -> Entis Cursor
```

## Install Essential Applications
<sub>[Back to Top](#introduction)</sub>
* Install [Google Chrome](https://www.google.com/chrome/)
* Install [Google Backup and Sync](https://www.google.com/intl/zh-TW_ALL/drive/download/backup-and-sync/)
* Install [Avira Free Security](https://www.avira.com/zh-tw)
* Install [Nvidia Driver](https://www.nvidia.com/Download/index.aspx)
* Install [.NET Core Runtime](https://dotnet.microsoft.com/download/dotnet-core/current/runtime)
* Install [Adobe Acrobat Pro DC](https://acrobat.adobe.com/us/en/acrobat/acrobat-pro.html)
* Install [Imagine Edge](https://imagingedge.sony.net/en/ie-desktop.html)
* Install [Razer Synapse](https://www.razer.com/synapse-3)
* Install [Line](https://www.microsoft.com/zh-tw/p/line/9wzdncrfj2g6?cid=msft_web_appsforwindows_chart&activetab=pivot:overviewtab) from Windows Store.
* Install [Free Color Picker](https://www.microsoft.com/zh-tw/p/free-color-picker-color-picker-from-screen-html-color-picker-hex-color-picker/9p9qkfj0fh21?activetab=pivot:overviewtab) from Windows Store.
* Install [Skype](https://www.microsoft.com/zh-tw/p/skype/9wzdncrfj364?activetab=pivot:overviewtab) from Windows Store.
* Install [Slack](https://www.microsoft.com/zh-tw/p/slack/9wzdncrdk3wp?activetab=pivot:overviewtab) from Windows Store
* Install [Spotify](https://www.microsoft.com/zh-tw/p/spotify-music/9ncbcszsjrsb?activetab=pivot:overviewtab) from Windows Store
* Install [Evernote](https://www.microsoft.com/zh-tw/p/evernote/9wzdncrfj3mb?activetab=pivot:overviewtab) from Windows Store.
* Install [ScreenToGif](https://www.microsoft.com/zh-tw/p/screentogif/9n3sqk8pds8g?activetab=pivot:overviewtab) from Windows Store.
* Install [Windows Terminal](https://www.microsoft.com/zh-tw/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) from Windows Store.
* Install [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) from Windows Store
```json
# Settings: 
     "defaults":
        {
            "colorScheme": "One Half Dark",
            "fontFace": "Fira Mono",
            "useAcrylic": true,
            "acrylicOpacity": 0.75,
            "scrollbarState": "visible"
        }
```
* Install [Windows Office 365](http://uio.no/tjenester/it/lagring-samarbeid/o365/) from University of Oslo
* Install EndNote X9
* Install Chocolatey
```
Set-ExecutionPolicy AllSigned
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
* Install WinCompose
```bash
choco install wincompose.install
# Options -> Composing -> Compose Key -> Right Alt
```    
* Install Git
```
choco install git
git config --global user.name  (name)
git config --global user.email (email)
```
* Install 7-Zip
```
choco install 7zip
```
* Install Visual Studio Code
```
choco install vscode
```
* Install Postman
```
choco install postman
```
* Install VLC Player
```bash
choco install vlc
# Download skin from https://www.deviantart.com/maverick07x/art/VLC-MinimalX-385698882
# Put the file to C:\Program Files\VideoLAN\VLC\skins
# Tools -> Preference -> Use custom skin
```
* Install Zoom
```
choco install zoom
```
* Install Sublime Text 3
```bash
choco install sublimetext3
# Tools -> Install Package Control
# Preferences -> Package Control: Install Package -> Dracula Color Scheme
# Preferences -> Package Control: Install Package -> ConvertToUTF8
# Preferences -> Package Control: Install Package -> Advanced CSV
```
* Install Docker Desktop
```
choco install docker-desktop
```
* Install Grammarly
```
choco install grammarly
```
* Install Intel Extreme Tuning Utility
```bash
choco install intel-xtu
# Advance Tuning -> Core Voltage Offset: -0.125V
```
* Install Microsoft PowerToys
```
choco install powertoys
```
* Install Paste Into File
```
choco install pasteintofile
```
* Install MikTex
```
choco install MikTex
```
* Install Darktable
```
choco install darktable
```

## Install Font
<sub>[Back to Top](#introduction)</sub>
* [Noto Sans JP](https://fonts.google.com/specimen/Noto+Sans+JP?query=Noto+Sans+#standard-styles)
* [Noto Sans TC](https://fonts.google.com/specimen/Noto+Sans+TC?query=Noto+Sans+)
* [Gen Jyuu Gothic](http://jikasei.me/font/genjyuu/)
* [Fira Sans](https://fonts.google.com/specimen/Fira+Sans?query=Fira)
* [Fira Sans Mono](https://fonts.google.com/specimen/Fira+Mono?query=Fira)
* [Redressed](https://fonts.google.com/specimen/Redressed?query=Redressed)
* Configure Font in PowerShell
```bash
# Windows + R -> regedit
# Navigate to HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Console\TrueTypeFont
# Right click -> New -> String Value
    # Value Name: 000
    # Value Data: Fira Mono
# Powershell -> Right click on title bar -> Font -> Fira Mono
```

## Gaming
<sub>[Back to Top](#introduction)</sub>
* Install [Razer Wolverine for Xbox](https://www.microsoft.com/zh-tw/p/razer-wolverine-for-xbox/9nsxxh05pfrq?activetab=pivot:overviewtab) from Windows Store
* Install [Final Fantasy XIV](https://www.finalfantasyxiv.com/playersdownload/eu/)
* Install Steam
```
choco install steam
```
* Install Epic Gaming Launcher
```
choco install epicgameslauncher
```
* Install Uplay
```
choco install uplay
```

## Set Up Windows Subsystem for Linux 2
<sub>[Back to Top](#introduction)</sub>
* Join Windows Insider Program
```bash
# Windows Setting -> Update and Security ->Windows Insider Program -> Slow
```
* Enable Windows Subsystem for Linux 2
```bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
# Restart computer
```
* Update [kernel](https://docs.microsoft.com/zh-tw/windows/wsl/wsl2-kernel) for Windows Subsystem for Linux 2
```
wsl --set-default-version 2
```
* Install [Ubuntu 20.04 LTS](
https://www.microsoft.com/zh-tw/p/ubuntu-2004-lts/9n6svws3rx71?rtc=1&activetab=pivot:overviewtab) from Windows Store
* Enable Docker on Windows Subsystem for Linux 2
```
# Docker Desktop -> Settings -> Resources -> WSL Integration -> Ubuntu 20.04
```

* Install Ensential Packages
```bash
sudo apt update
sudo apt upgrade
sudo apt install build-essential zsh
```

* Configure ZSH
```bash
sudo chsh -s $(which zsh)
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
vim $HOME/.zshrc
    # ZSH_THEME="ys"
    # alias ls="ls --color -h --group-directories-first" 
```

* Install Anaconda
```
wget https://repo.anaconda.com/archive/Anaconda3-2020.02-Linux-x86_64.sh
sh Anaconda3-2020.02-Linux-x86_64.sh
conda init zsh

conda config --add channels conda-forge
```
* Install Git Flow
```
sudo apt install git-flow
```
* Install tmux
```bash
sudo apt install tmux
vim $HOME/.tmux.conf
    # set -g mouse on 
```
* Install Apache2 ([contig](https://ubuntu.com/tutorials/install-and-configure-apache#4-setting-up-the-virtualhost-configuration-file))
```bash
sudo apt install apache2
```