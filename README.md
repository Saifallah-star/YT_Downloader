# YT_Downloader 

A clean, lightweight, and zero-dependency desktop application for downloading YouTube videos (MP4) and high-quality audio (MP3). Built-in FFmpeg integration ensures seamless processing out of the box without requiring manual dependencies.

---

##  Downloads

Choose the package compatible with your operating system:

| Platform | File Name | Download Link | Instructions |
| :--- | :--- | :--- | :--- |
| **Windows** | `YT_Downloader_Windows.zip` | [Download for Windows]([https://your-drive-or-github-link-here](https://drive.google.com/file/d/1hKSbsAI_FcymwP4I3wR8N3zwgDf7148L/view?usp=sharing)) | Extract `.zip` and run `YT_Downloader.exe`. *(If SmartScreen appears, click "More info" → "Run anyway")* |
| **Linux** | `YT_Downloader_Linux.zip` | [Download for Linux]([https://your-drive-or-github-link-here](https://drive.google.com/file/d/1Gc3v0TrAkRwZ-wEl0ycxUqISXJSclSTY/view?usp=sharing)) | Extract `.zip` and launch the application executable. |

---

---

## Technical Overview (For Python Developers)

here is how the application is built under the hood:

* **GUI Framework (`customtkinter` & `tkinter`)**: Built on `customtkinter` (a modern wrapper around Tkinter) for native, auto-adjusting dark/light mode UI components. Thread-safe Tkinter updates are handled using `.after()` callbacks to prevent GUI freezing.
* **Core Downloader (`yt-dlp`)**: Utilizes `yt-dlp` programmatically via its Python API (`YoutubeDL`). Video/audio streams are fetched and processed asynchronously using Python's `threading` module to keep the UI fully responsive during downloads.
* **Media Processing (Embedded FFmpeg)**: Audio conversion (`FFmpegExtractAudio` post-processor for `.mp3`) and video/audio merging (`bestvideo+bestaudio`) are executed by routing `yt-dlp`'s `ffmpeg_location` option dynamically to bundled `ffmpeg` and `ffprobe` binaries.
* **Dynamic Asset Resolution (`sys._MEIPASS`)**: Features a custom path resolver (`get_resource_path()`) that dynamically toggles between standard relative local paths during development and the temporary extracted PyInstaller directory (`_MEIPASS`) in runtime bundles.
* **Single-File Packaging (`PyInstaller`)**: Standalone, portable binaries are generated using PyInstaller, bundling the Python runtime, all UI resources, and cross-platform native FFmpeg binaries via `--add-data` and `--add-binary` flags.
