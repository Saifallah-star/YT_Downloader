# YT_Downloader 

A clean, lightweight, and zero-dependency desktop application for downloading YouTube videos (MP4) and high-quality audio (MP3). Built-in FFmpeg integration ensures seamless processing out of the box without requiring manual dependencies.

---

Choose the package compatible with your operating system:

| Platform | File Name | Download Link | Instructions |
| :--- | :--- | :--- | :--- |
| **Windows** | `YT_Downloader_Windows.zip` | [Download for Windows](https://drive.google.com/drive/folders/1aIwHc4I6IrnaH-da6q3thSmA72SVYO9P?usp=sharing) | Extract `.zip` and run `YT_Downloader.exe`. *(If SmartScreen appears, click "More info" → "Run anyway")* |
| **Linux** | `YT_Downloader_Linux.zip` | [Download for Linux](https://drive.google.com/drive/folders/1OdcbNkQ3X6BU-r-KNXEukF-89739aXMy?usp=sharing) | Extract `.zip` and launch the application executable. |

---

---

## Technical Overview

For developers interested in the technology behind the app:

* **Language**: Built entirely with **Python**.
* **User Interface**: Designed using **CustomTkinter** for a modern, responsive desktop interface with automatic dark/light mode support.
* **Core Engine**: Powered by **yt-dlp** for fast and reliable YouTube video/audio stream processing.
* **Media Handling**: Leverages **FFmpeg** for high-quality MP3 extraction and MP4 merging.
* **Deployment**: Packaged into standalone, single-file executables for simple distribution across supported operating systems.
