# Red's-Guide-on-Installing-G.A.M.M.A.-on-Linux
Red's guide on Installing G.A.M.M.A. (Anomaly modpack) on Linux.

# Alternative instalation guide by DravenusRex (older): https://github.com/DravenusRex/stalker-gamma-linux-guide

# Installation Guide

## Video-companion: [youtube-guide](https://youtu.be/luAceiXojiU?si=3LdfAVYyoU9-OS7-)

## !!! This guide assumes that you have solid general understanding of CLI and how to install/fix stuff on your system. If you need more hand-holding - refer to the video guide.

## 1 - Bottles (Source: [usebottles.com](https://usebottles.com))
- **1.1** - Install Flatpak.
- **1.2** - Install Bottles with `flatpak install flathub com.usebottles.bottles`
- **1.3** - Run (Verify it) with `flatpak run com.usebottles.bottles`
- **1.4** - Give Bottles access to filesystem with `sudo flatpak override com.usebottles.bottles --filesystem=host`

## 2 - Setup dir for GAMMA
- **2.1** - Create folder where you will be installing GAMMA (You need 200GB to be safe).
- **2.2** - Open it in terminal.
    - **2.2.1** - Copy path of said folder.
    - **2.2.2** - Open terminal and do `cd {path-of-your-folder}` (without {}).

## 3 - Installation of GAMMA
- **3.1** - Use https://github.com/FaithBeam/stalker-gamma-cli to install GAMMA.

## 5 - GAMMA Configuration
- **5.1** - Configure Bottles
    - **5.1.1** - Download runner (proton-ge-9-20)
    - **5.1.2** - Create bottle (Gaming)
    - **5.1.3** - Configure bottle (change it's runner to proton-ge-9-20)
- **5.2** - Configure prefix
    - **5.2.1** - Find prefix of the bottle that you created
    - **5.2.2** - Install dependencies with `WINEPREFIX={your-prefix's-path} winetricks cmd d3dx9 dx8vb d3dcompiler_42 d3dcompiler_43 d3dcompiler_46 d3dcompiler_47 d3dx10_43 d3dx10 d3dx11_42 d3dx11_43 vcrun2022 dxvk quartz`

## 6 - Making GAMMA run
- **6.1** - First run
    - **6.1.1** - Add mod organ shortcut.
    - **6.1.2** - Start it.
    - **6.1.3** - Press next.
    - **6.1.9** - Follow through.
    - **6.1.10** - You can close it (if you want)
- **6.2** - Second run (or continuation)
    - **6.2.1** - (Ultrawide fix (only for people with Ultrawide)).
    - **6.2.2** - Try to start GAMMA.
    - **6.2.3** - It works.

## 7 - End note
- **7.1** - Additional help (Source: [AnomalyMod](https://anomalymod.com/repacks/stalker-gamma))
    - **7.1.1** - Discord - @red007master (me)
    - **7.1.2** - Discord - [Stalker-GAMMA Server](https://discord.com/invite/stalker-gamma)
    - **7.1.3** - Discord - Linux support thread: [Linux Support Thread](https://discord.com/channels/912320685949300746/932079012547270746)
- **7.2** - My Hardware/Software: AMD GPU(7900xtx)/CPU(r9), kernel - (6.12.8-arch1-1), tested on: Hyprland/KDE/Cinamon, date:12.01.2025.
- **7.3** - Good luck in Zone and have a good day.

# Troubleshooting: [here](CommonProblems/index.md)
# Distro-specific: [here](Distros/index.md)
# Updating: [here](Updating.md)
