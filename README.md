# YT_Downloader ( V1.1.0 )

A clean, lightweight, and zero-dependency desktop application for downloading YouTube videos (MP4) and high-quality audio (MP3). Built-in FFmpeg integration ensures seamless processing out of the box without requiring manual dependencies.

---

Choose the package compatible with your operating system:

| Platform | File Name | Download Link | Instructions |
| :--- | :--- | :--- | :--- |
| **Windows** | `YT_Downloader_Windows.zip` | [Download for Windows](https://drive.google.com/drive/folders/1aIwHc4I6IrnaH-da6q3thSmA72SVYO9P?usp=sharing) | Extract `.zip` and run `YT_Downloader.exe`. *(If SmartScreen appears, click "More info" → "Run anyway")* |
| **Linux** | `YT_Downloader_Linux.zip` | [Download for Linux](https://drive.google.com/drive/folders/1OdcbNkQ3X6BU-r-KNXEukF-89739aXMy?usp=sharing) | Extract `.zip` and launch the application executable. |

---
## 🐧 Linux Setup Guide
#### Step 1: Remove the Old Version ( if you have )
Run these commands in your terminal to delete cached shortcut entries, leftover icon assets, and previous installation directories:

    # 1. Remove old desktop shortcuts
    rm -f ~/.local/share/applications/*yt*downloader*.desktop
    rm -f ~/.local/share/applications/*YT*Downloader*.desktop
    
    # 2. Remove stored persistent icons
    rm -f ~/.local/share/icons/yt_downloader_logo.png
    
    # 3. Remove previous application directories
    rm -rf ~/.local/bin/YT_Downloader
    rm -rf ~/.local/share/YT_Downloader
    rm -rf ~/YT_Downloader
    
    # 4. Refresh your Linux application launcher cache
    update-desktop-database ~/.local/share/applications

#### Step 2: Install the New Version
Download YT_Downloader_Linux.zip and extract it to your preferred location

---
## 🪟 Windows Setup Guide
#### Step 1: Remove the Old Version ( if you have )

Close YT_Downloader if it is currently running.

Delete the old YT_Downloader folder from your system (e.g., in Downloads, Program Files, or your Desktop).

If you pinned the old executable or created a shortcut:

  Right-click the old shortcut on your Desktop or Start Menu and select Delete.
  
  Right-click the old Taskbar icon and select Unpin from taskbar.

#### Step 2: Install the New Version

Download YT_Downloader_Windows.zip and extract the .zip archive.

Move the extracted YT_Downloader folder to your desired location

Open the folder and locate YT_Downloader.exe.
    
---

## Technical Overview

For developers interested in the technology behind the app:

* **Language**: Built entirely with **Python**.
* **User Interface**: Designed using **CustomTkinter** for a modern, responsive desktop interface with automatic dark/light mode support.
* **Core Engine**: Powered by **yt-dlp** for fast and reliable YouTube video/audio stream processing.
* **Media Handling**: Leverages **FFmpeg** for high-quality MP3 extraction and MP4 merging.
* **Deployment**: Packaged into standalone, single-file executables for simple distribution across supported operating systems.
